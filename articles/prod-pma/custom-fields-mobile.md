---
title: Zaimplementuj pola niestandardowe dla aplikacji mobilnej Microsoft Dynamics 365 Project Timesheet w systemie iOS i Android
description: W tym temat przedstawiono popularne wzorce umożliwiające korzystanie z rozszerzeń w celu implementowania pól niestandardowych.
author: Yowelle
ms.date: 05/29/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 10.0.3
ms.search.validFrom: 2019-05-29
ms.openlocfilehash: 23b002559dcbb9118ccb2b36d70707ccb37b19ad
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 05/10/2021
ms.locfileid: "6003058"
---
# <a name="implement-custom-fields-for-the-microsoft-dynamics-365-project-timesheet-mobile-app-on-ios-and-android"></a>Zaimplementuj pola niestandardowe dla aplikacji mobilnej Microsoft Dynamics 365 Project Timesheet w systemie iOS i Android

[!include [banner](../includes/banner.md)]

W tym temat przedstawiono popularne wzorce umożliwiające korzystanie z rozszerzeń w celu implementowania pól niestandardowych. Omówiono następujące tematy:

- Różne typy danych obsługiwane przez niestandardową strukturę pól
- Jak wyświetlać pola tylko do odczytu lub edytowalne we wpisach grafiku i zapisywać wartości podane przez użytkownika z powrotem w bazie danych
- Wyświetlanie pól tylko do odczytu w nagłówku karty czasu pracy
- Sposób integrowania innej niestandardowej logiki biznesowej z wprowadzaniem wartości domyślnych w polach i wykonywania dodatkowych czynności sprawdzających

## <a name="audience"></a>Odbiorcy

Ten temat jest przeznaczony dla deweloperów, którzy integrujący własne pola niestandardowe z aplikacją mobilną Microsoft Dynamics 365 Project Timesheet dostępną dla systemów Apple iOS i Google Android. Założenie jest takie, że czytelnicy są zaznajomieni z rozwojem X ++ i funkcjonalnością grafiku projektów.

## <a name="data-contract--tstimesheetcustomfield-x-class"></a>Kontrakt dotyczący danych — Klasa TSTimesheetCustomField X++

Klasa **TSTimesheetCustomField** jest klasą kontraktu danych X++, która reprezentuje informacje o niestandardowym polu funkcji grafiku. Listy obiektów w polach niestandardowych są przekazywane zarówno do kontraktu danych TSTimesheetDetails, jak i kontraktu danych TSTimesheetEntry w celu wyświetlenia pól niestandardowych w aplikacji mobilnej.

- **TSTimesheetDetails** — kontrakt nagłówka karty czasu pracy.
- **TSTimesheetEntry** — kontrakt transakcji na karcie czasu pracy. Grupy tych obiektów, które mają te same informacje o projekcie i wartość **timesheetLineRecId** tworzą wiersz.

### <a name="fieldbasetype-types"></a>fieldBaseType (typy)

Właściwość **FieldBaseType** obiektu **TsTimesheetCustom** określa typ pola, które będzie wyświetlane w aplikacji. Obsługiwane są następujące **Typy** wartości:

| Typy wartości | Typ              | Uwagi |
|-------------|-------------------|-------|
| 0           | Ciąg (i Wyliczenie) | Pole jest wyświetlane jako pole tekstowe. |
| 1           | Integer           | Wartość jest wyświetlana jako liczba bez miejsc dziesiętnych. |
| 2           | Rzeczywista              | Wartość jest wyświetlana jako liczba z miejscami dziesiętnymi.<p>Aby wyświetlić wartość rzeczywistą jako walutę w aplikacji, należy użyć właściwości **fieldExtenededType**. Aby ustawić liczbę wyświetlanych miejsc dziesiętnych, można użyć właściwości **numberOfDecimals**.</p> |
| 3           | Date              | Formaty dat są określane przez ustawienie użytkownika **Data, godziny i format liczb** określone w **preferencjach języka i kraju / regionu** w **opcjach użytkownika**. |
| 100           | Boolean           | |
| 15          | GUID              | |
| 16          | Int64             | |

- Jeśli właściwość **stringOptions** nie jest podana w obiekcie **TSTimesheetCustomField**, użytkownikowi zostanie udostępnione pole dowolnego tekstu.

    Właściwość **stringLength** może służyć do ustawiania maksymalnej długości ciągu, jaką użytkownicy mogą wprowadzać.

- Jeśli właściwość **stringOptions** jest podana dla obiektu **TSTimesheetCustomField**, te elementy listy są jedynymi wartościami, które mogą być wybierane przez użytkowników za pomocą przycisków opcji (przycisków radiowych).

    W takim przypadku pole ciągu może działać jako wartość wyliczenia na potrzeby wprowadzania danych przez użytkownika. Aby zapisać wartość w bazie danych jako wyliczenie, ręcznie zamapuj wartość ciągu z powrotem na wartość wyliczenia przed zapisaniem do bazy danych za pomocą łańcucha poleceń (zobacz „Użyj łańcucha poleceń w klasie TSTimesheetEntryService, aby zapisać wpis grafiku z aplikacja z powrotem do bazy danych ”w dalszej części tego tematu, aby zapoznać się z przykładem).

### <a name="fieldextendedtype-tscustomfieldextendedtype"></a>fieldExtendedType (TSCustomFieldExtendedType)

Za pomocą tej właściwości można formatować wartości rzeczywiste jako walutę. To podejście ma zastosowanie tylko wtedy, gdy wartość **fieldBaseType** jest **Rzeczywista**.

- **TSCustomFieldExtendedType:None** — Formatowanie nie jest stosowane.
- **TSCustomFieldExtendedType::Waluta** – sformatuj wartość jako walutę.

    Kiedy formatowanie waluty jest aktywne, można użyć pola **stringValue**, aby przekazać kod waluty, który ma być wyświetlony w aplikacji. Jest to wartość tylko do odczytu.

    Pole **realValue** zawiera kwotę pieniężną, która powinna zostać zapisana w bazie danych.

### <a name="fieldsection-tscustomfieldsection"></a>fieldSection (TSCustomFieldSection)

Tej właściwości można użyć w celu określenia miejsc, w których ma być wyświetlane pole niestandardowe w aplikacji.

- **TSCustomFieldSection::Nagłowek** – pole zostanie wyświetlone w sekcji **Wyświetl więcej szczegółów** w aplikacji. Te pola są zawsze tylko do odczytu.
- **TSCustomFieldSection::Wiersz** – pole będzie wyświetlane po wszystkich polach wiersza karty czasu pracy znajdujących się na wszystkich polach. Te pola można edytować lub tylko do odczytu.

### <a name="fieldname-fieldnameshort"></a>fieldName (FieldNameShort)

Ta właściwość identyfikuje pole, gdy wartości dostarczane przez aplikację są zapisywane z powrotem w bazie danych.

### <a name="tablename-tablenameshort"></a>tableName (TableNameShort)

Ta właściwość identyfikuje pole, gdy wartości dostarczane przez aplikację są zapisywane z powrotem w bazie danych.

### <a name="iseditable-noyes"></a>isEditable (NoYes)

Ustaw tę właściwość na **Tak**, aby określić, że pole w sekcji wpisu grafiku powinno być edytowalne przez użytkowników. Ustaw właściwość na **Nie**, aby uczynić pole tylko do odczytu.

### <a name="ismandatory-noyes"></a>isMandatory (NoYes)

Ustaw tę właściwość na **Tak**, aby określić, że pole w sekcji wpisu grafiku powinno być obowiązkowe.

### <a name="label-str"></a>label (str)

Właściwość ta określa etykietę widoczną obok pola w aplikacji.

### <a name="stringoptions-list-of-strings"></a>stringOptions (lista ciągów)

Ta właściwość jest stosowana tylko wtedy, gdy **fieldBaseType** jest ustawiona na wartość **Ciąg**. Jeśli ustawiona jest opcja **stringOptions**, wartości ciągów, które są dostępne do wyboru za pomocą przycisków opcji (przycisków radiowych), są określane przez ciągi na liście. Jeśli nie podano żadnych ciągów, dozwolone jest wprowadzanie dowolnego tekstu w polu ciągu (przykład można znaleźć w sekcji „Używanie łańcucha poleceń w klasie TSTimesheetEntryService do zapisywania wpisu grafiku z aplikacji z powrotem do bazy danych” w dalszej części tego tematu). .

### <a name="stringlength-int"></a>stringLength (int)

Ta właściwość określa maksymalną długość pola w postaci ciągu. Jest stosowana tylko wtedy, gdy **fieldBaseType** jest ustawiona na wartość **Ciąg**.

### <a name="numberofdecimals-int"></a>numberOfDecimals (int)

Ta właściwość określa liczbę miejsc dziesiętnych wyświetlanych dla pola rzeczywistego. Jest stosowana tylko wtedy, gdy **fieldBaseType** jest ustawiona na wartość **Rzeczywiste**.

### <a name="ordersequence-int"></a>orderSequence (int)

Ta właściwość steruje kolejnością, w jakiej pola niestandardowe są prezentowane w aplikacji po określeniu więcej niż jednego pola niestandardowego. Pola z mniejszymi numerami są prezentowane w pierwszej kolejności.

### <a name="booleanvalue-boolean"></a>booleanValue (wartość logiczna)

W przypadku pól typu **logiczna** ta właściwość przekazuje wartość logiczną pola między serwerem a aplikacją.

### <a name="guidvalue-guid"></a>guidValue (identyfikator GUID)

W przypadku pól typu **GUID** ta właściwość przekazuje wartość unikatowy identyfikator globalny (GUID) pola między serwerem a aplikacją.

### <a name="int64value-int64"></a>int64Value (Int64)

W przypadku pól typu **Int64** ta właściwość przekazuje wartość Int64 pola między serwerem a aplikacją.

### <a name="intvalue-int"></a>intValue (int)

W przypadku pól typu **Int** ta właściwość przekazuje wartość int pola między serwerem a aplikacją.

### <a name="realvalue-real"></a>realValue (rzeczywista)

W przypadku pól typu **Rzeczywista** ta właściwość przekazuje wartość rzeczywistą pola między serwerem a aplikacją.

### <a name="stringvalue-str"></a>stringValue (str)

W przypadku pól typu **Ciąg** ta właściwość przekazuje wartość ciąg pola między serwerem a aplikacją. Jest on również używany w przypadku pól o typie **rzeczywistym**, które są sformatowane jako waluta. W przypadku tych pól właściwość jest używana do przekazania kodu waluty do aplikacji.

### <a name="datevalue-date"></a>dateValue (data)

W przypadku pól typu **Data** ta właściwość przekazuje wartość daty pola między serwerem a aplikacją.

## <a name="show-and-save-a-custom-field-in-the-timesheet-entry-section"></a>Wyświetlanie i zapisywanie pola niestandardowego w sekcji wpisu grafiku

Poniżej znajduje się zrzut ekranu z aplikacji mobilnej utworzenia wpisu karty czasu pracy. Pokazuje gotowe pola i pole niestandardowe w sekcji „Wprowadzanie czasu” o nazwie „Ciąg testowy” z już ustawioną wartością wyliczenia „Druga opcja”.

![Pole niestandardowe ciągu testowego w aplikacji](media/timesheet-entry.jpg)



Poniżej znajduje się zrzut ekranu z aplikacji mobilnej użytkownika, który wybiera jedną z opcji wyliczenia dostępnych dla pola niestandardowego „Ciąg testowy”.  Dwie opcje to „Pierwsza opcja” i „Druga opcja” pokazane jako przyciski opcji. Druga opcja jest obecnie zaznaczona.

![Przyciski opcji (przyciski radiowe) dla pola niestandardowego ciągu testowego](media/enum-option.jpg)



### <a name="extend-the-tstimesheetline-table-so-that-it-has-a-custom-field"></a>Rozszerzanie tabeli TSTimesheetLine tak, aby zawiera pole niestandardowe

W typowych scenariuszach jest prawdopodobne, że dane pola niestandardowego w sekcji wpisu grafiku zostaną zapisane w tabeli TSTimesheetLine. W przypadku, gdy dane mogą zostać pobrane na podstawie określonego rekordu TSTimesheetTrans lub jeśli nie ma określonego kontekstu rekordów (na przykład jeśli pole jest ustawione jako tylko do odczytu w parametrach projektu), można użyć innych tabel.

Należy pamiętać, że pola niestandardowe nie muszą zawierać żadnych kopii zapasowych rekordów bazy danych. Można je dynamicznie generować na podstawie logiki X++. Takie podejście może być przydatne w scenariuszach tylko do odczytu (zobacz sekcję „Używanie łańcucha poleceń w klasie TSTimesheetDetails, metoda buildCustomFieldListForHeader do wypełniania szczegółów karty czasu pracy”, aby zapoznać się z przykładem dynamicznie generowanych wartości pól niestandardowych).

Poniżej znajduje się zrzut ekranu z Visual Studio drzewa obiektów aplikacji. Wskazuje ono rozszerzenie tabeli TSTimesheetLine z polem TestLineString dodany jako pole niestandardowe.

![Ciąg wiersza](media/b6756b4a3fc5298093327a088a7710fd.png)

### <a name="use-chain-of-command-on-the-buildcustomfieldlist-method-of-the-tstimesheetsettings-class-to-show-a-field-in-the-timesheet-entry-section"></a>W celu wyświetlenia pola w sekcji wpisu grafiku Użyj łańcucha poleceń dla metody buildCustomFieldList klasy TSTimesheetSettings

Ten kod Steruje ustawieniami wyświetlania pola w aplikacji. Na przykład kontroluje typ pola, etykietę, czy pole jest obowiązkowe oraz w jakiej sekcji pojawia się pole.

W poniższym przykładzie przedstawiono pole ciągu na wpisach czasowych. W tym polu są dostępne dwie opcje, **Pierwsza opcja** i **Druga opcja**, dostępnych za pośrednictwem przycisków opcji (przycisków radiowych). Pole w aplikacji jest skojarzone z polem **TestLineString** dodawanym do tabeli TSTimesheetLine.

Zwróć uwagę na użycie metody **TSTimesheetCustomField::newFromMetatdata()** w celu uproszczenia inicjowania niestandardowych właściwości pola: **fieldBaseType**, **tableName**, **fieldname**, **label**, **isEditable**, **isMandatory**, **stringLength** i **numberOfDecimals**. Te parametry można również ustawić ręcznie, zależnie od preferencji.

```xpp
...
[ExtensionOf(classStr(TsTimesheetSettings))]
final class TSTimesheetSettings_Extension
{
    protected List buildCustomFieldList()
    {
        List customFieldList = next buildCustomFieldList();
        TSTimesheetCustomField tsTimesheetCustomField;
        tsTimesheetCustomField =
        TSTimesheetCustomField::newFromMetadata(tableNum(TsTimesheetLine),
        fieldNum(TSTimesheetLine, TestLineString));
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Line);
        tsTimesheetCustomField.parmOrderSequence(1);
        List stringOptions = new List(Types::String);
        stringOptions.addEnd('First option');
        stringOptions.addEnd('Second option');
        tsTimesheetCustomField.parmStringOptions(stringOptions);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

### <a name="use-chain-of-command-on-the-buildcustomfieldlistforentry-method-of-the-tstimesheetentry-class-to-enter-values-in-a-timesheet-entry"></a>Użyj łańcucha poleceń w metodzie buildCustomFieldListForEntry klasy TSTimesheetEntry do wprowadzania wartości we wpisie grafiku

Metoda **buildCustomFieldListForEntry** służy do wprowadzania wartości w zapisanych wierszach karty czasu pracy w aplikacji mobilnej. Jako parametr przyjmuje rekord TSTimesheetTrans. Pól z tego rekordu można użyć do wypełnienia wartości pola niestandardowego w aplikacji.

```xpp
...
[ExtensionOf(classStr(TsTimesheetEntry))]
final class TsTimesheetEntry_Extension
{
    protected List buildCustomFieldListForEntry(TSTimesheetTrans _tsTimesheetTrans)
    {
        List customFieldList = next buildCustomFieldListForEntry(_tsTimesheetTrans);
        TSTimesheetLine tsTimesheetLine = _tsTimesheetTrans.timesheetLine();
        TSTimesheetCustomField tsTimesheetCustomField;
        tsTimesheetCustomField =
        TSTimesheetCustomField::newFromMetadata(tableNum(TsTimesheetLine),
        fieldNum(TSTimesheetLine, TestLineString));
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Line);
        tsTimesheetCustomField.parmOrderSequence(1);
        tsTimesheetCustomField.parmStringValue(tsTimesheetLine.TestLineString);
        List stringOptions = new List(Types::String);
        stringOptions.addEnd('First option');
        stringOptions.addEnd('second option;);
        tsTimesheetCustomField.parmStringOptions(stringOptions);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

### <a name="use-chain-of-command-on-the-tstimesheetentryservice-class-to-save-a-timesheet-entry-from-the-app-back-to-the-database"></a>W celu zapisania wpisu grafiku z powrotem do bazy danych należy użyć łańcuchu poleceń klasy TSTimesheetEntryService

Aby zapisać pole niestandardowe z powrotem do bazy danych przy użyciu programu w typowy sposób, należy rozszerzyć wiele metod:

- Metoda **timesheetLineNeedsUpdating** jest używana w celu ustalenia, czy rekord wiersza został zmieniony przez użytkownika w aplikacji i musi zostać zapisany w bazie danych. Jeśli wydajność nie jest istotna, można ją uprościć, aby zawsze zwracała wartość **true** (prawda).
- Metody **populateTimesheetLineFromEntryDuringCreate** i **populateTimesheetLineFromEntryDuringUpdate** mogą być rozszerzane w taki sposób, aby były wprowadzane w rekordzie TSTimesheetLine bazy danych z dostarczonego rekordu dotyczącego kontraktu danych TSTimesheetEntry. W poniższym przykładzie pokazano, jak ręczne mapowanie między polem bazy danych a polem wprowadzania jest wykonywane ręcznie za pomocą kodu X++.
- Metodę **populateTimesheetWeekFromEntry** można również rozszerzyć, jeśli pole niestandardowe mapowane na obiekt **TSTimesheetEntry** musi zostać zapisane z powrotem do tabeli bazy danych TSTimesheetLineweek.

> [!NOTE]
> Poniższy przykład zapisuje wartość **firstOption** lub **secondOption**, która jest wybierana przez użytkownika do bazy danych w postaci nieprzetworzonej wartości ciągu. Jeśli pole bazy danych jest polem typu **Wyliczenie**, można je ręcznie zamapować na wartość enum, a następnie zapisać w polu wyliczenia w tabeli bazy danych.

```xpp
...
[ExtensionOf(classStr(TSTimesheetEntryService))]
final class TSTimesheetEntryService_Extension
{
    protected boolean timesheetLineNeedsUpdating(TSTimesheetLine _tsTimesheetLine,
    TsTimesheetEntry _tsTimesheetEntry)
    {
        boolean ret = next timesheetLineNeedsUpdating(_tsTimesheetLine,
        _tsTimesheetEntry);
        if (!ret)
        {
            */ Loop through custom fields to see if value needs updating*/
            ListEnumerator enumerator =  _tsTimesheetEntry.parmCustomFields().getEnumerator();
            while (enumerator.moveNext())
            {
                TSTimesheetCustomField customField = enumerator.current();
                if (customField.parmFieldName() == fieldId2Name(tableNum(TsTimesheetLine),
                fieldNum(TSTimesheetLine, TestLineString)))
                {
                    */ If Custom field value for TestLineString field has changed, We need to update the timesheet line.*/
                    if (_tsTimesheetLine.TestLineString != customField.parmStringValue())
                    {
                        ret = true;
                    }
                }
            }
        }
        return ret;
    }
    protected void populateTimesheetLineFromEntryDuringCreate(TSTimesheetLine
    _tsTimesheetLine, TSTimesheetEntry _tsTimesheetEntry)
    {
        next populateTimesheetLineFromEntryDuringCreate(_tsTimesheetLine,
        _tsTimesheetEntry);
        this.populateTimesheetLineFromCustomFields(_tsTimesheetLine,
        _tsTimesheetEntry);
        }
        protected void populateTimesheetLineFromEntryDuringUpdate(TSTimesheetLine
        \_tsTimesheetLine, TSTimesheetEntry _tsTimesheetEntry)
        {
            next populateTimesheetLineFromEntryDuringUpdate(_tsTimesheetLine,
            _tsTimesheetEntry);
            this.populateTimesheetLineFromCustomFields(_tsTimesheetLine,
            _tsTimesheetEntry);
        }
        private void populateTimesheetLineFromCustomFields(TSTimesheetLine
        _tsTimesheetLine, TSTimesheetEntry _tsTimesheetEntry)
        {
            ListEnumerator enumerator =
            _tsTimesheetEntry.parmCustomFields().getEnumerator();
            while (enumerator.moveNext())
            {
                TSTimesheetCustomField customField = enumerator.current();
                if (customField.parmFieldName() == fieldId2Name(tableNum(TsTimesheetLine),
                fieldNum(TSTimesheetLine, TestLineString)))
                {
                    _tsTimesheetLine.TestLineString = customField.parmStringValue();
                }
            }
        }
    }
...
```

## <a name="show-a-custom-field-in-the-timesheet-header-section"></a>Pokaż pole niestandardowe w sekcji nagłówka grafiku

Poniżej znajduje się zrzut ekranu z aplikacji mobilnej użytkownika przeglądającego grafik. W prawym górnym rogu został wybrany przycisk „Więcej informacji”, aby wyświetlić opcję „Wyświetl więcej szczegółów”.  

![Wyświetl więcej szczegółów polecenia](media/show-more.png)

Poniżej znajduje się zrzut ekranu z aplikacji mobilnej pokazujący sekcję „Więcej” grafiku. Do sekcji nagłówka grafiku dodano pole niestandardowe o nazwie „Stopień wykorzystania tego grafiku (obliczone pole niestandardowe)”. W polu niestandardowym ustawiono wartość tylko do odczytu „0,667”.

![Więcej sekcji](media/more-section.jpg)

### <a name="extend-the-tstimesheettable-table-so-that-it-has-a-custom-field"></a>Rozszerzanie tabeli TSTimesheetTable tak, aby zawiera pole niestandardowe

W typowych scenariuszach jest prawdopodobne, że dane dla pola niestandardowego w sekcji nagłówka zostaną pobrane z tabeli TSTimesheetHeader. W przypadku, gdy dane mogą zostać pobrane na podstawie określonego rekordu TSTimesheetTable lub jeśli nie ma określonego kontekstu rekordów (na przykład jeśli pole jest ustawione jako tylko do odczytu w parametrach projektu), można użyć innych tabel.

Należy pamiętać, że pola niestandardowe nie muszą zawierać żadnych kopii zapasowych rekordów bazy danych. Można je dynamicznie generować na podstawie logiki X++. Poniższy przykład ilustruje tę metodę.

Pola znajdujące się w sekcji nagłówka są zawsze tylko do odczytu w aplikacji.

### <a name="use-chain-of-command-on-the-buildcustomfieldlist-method-of-the-tstimesheetsettings-class-to-show-a-field-in-the-header-section"></a>Użyj łańcucha poleceń w metodzie buildCustomFieldList klasy TSTimesheetSettings, aby wyświetlić pole w sekcji nagłówka

Ten kod Steruje ustawieniami wyświetlania pola w aplikacji. Na przykład kontroluje typ pola, etykietę, czy pole jest obowiązkowe oraz w jakiej sekcji pojawia się pole.

W poniższym przykładzie pokazano obliczoną wartość w sekcji nagłówka w aplikacji.

```xpp
...
[ExtensionOf(classStr(TsTimesheetSettings))]
final class TSTimesheetSettings_Extension
{
    protected List buildCustomFieldList()
    {
        List customFieldList = next buildCustomFieldList();
        TSTimesheetCustomField tsTimesheetCustomField;

        */ Computed utilization rate*/
        tsTimesheetCustomField = new TSTimesheetCustomField();
        tsTimesheetCustomField.parmFieldBaseType(Types::Real);
        tsTimesheetCustomField.parmLabel("Utilization rate of this timesheet (computed
        custom field)");
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Header);
        tsTimesheetCustomField.parmOrderSequence(2);
        tsTimesheetCustomField.parmNumberOfDecimals(3);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

### <a name="use-chain-of-command-on-the-buildcustomfieldlistforheader-method-of-the-tstimesheetdetails-class-to-fill-in-timesheet-details"></a>Użyj łańcucha poleceń w metodzie buildCustomFieldListForHeader klasy TSTimesheetDetails, aby wypełnić szczegóły grafiku

Metoda **buildCustomFieldListForHeader** służy do wypełniania szczegółów nagłówka karty czasu pracy w aplikacji mobilnej. Jako parametr przyjmuje rekord TSTimesheetTable. Pól z tego rekordu można użyć do wypełnienia wartości pola niestandardowego w aplikacji. W poniższym przykładzie nie są odczytywane żadne wartości z bazy danych. Zamiast tego używa logiki X ++ do generowania wartości obliczonej, która jest następnie wyświetlana w aplikacji.


```xpp
...
[ExtensionOf(classStr(TSTimesheetDetails))]
final class TSTimesheetDetails_Extension
{
    protected List buildCustomFieldListForHeader(TSTimesheetTable
    _tsTimesheetTable)
    {
        List customFieldList = next buildCustomFieldListForHeader(_tsTimesheetTable);
        TSTimesheetCustomField tsTimesheetCustomField;

        */ Computed utilization rate*/
        tsTimesheetCustomField = new TSTimesheetCustomField();
        tsTimesheetCustomField.parmFieldBaseType(Types::Real);
        tsTimesheetCustomField.parmLabel("Utilization rate of this timesheet (computed
        custom field)");
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Header);
        tsTimesheetCustomField.parmOrderSequence(2);
        tsTimesheetCustomField.parmNumberOfDecimals(3);
        real utilizationRate = 0;
        if (_tsTimesheetTable.totalHours() != 0)
        {
            utilizationRate = _tsTimesheetTable.totalHoursBillable() /
            _tsTimesheetTable.totalHours();
        }
        tsTimesheetCustomField.parmRealValue(utilizationRate);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

## <a name="other-configurabilityextensibility-opportunities"></a>Inne możliwości konfigurowalności/rozszerzalności

### <a name="adding-additional-validation-for-the-app"></a>Trwa dodawanie dodatkowych poprawność aplikacji

Istniejąca logika funkcji grafiku na poziomie bazy danych będzie nadal działać zgodnie z oczekiwaniami. Aby przerwać wykonywanie operacji zapisywania lub przesyłania i wyświetlać określony komunikat o błędzie, można dodać do kodu **błąd typu throw („wiadomość do użytkownika”)** za pośrednictwem łańcucha rozszerzeń poleceń. Oto trzy przykłady przydatnych metod rozszerzalności:

- Jeśli **validateWrite** w tabeli TSTimesheetLine zwróci **false** podczas operacji zapisywania wiersza grafiku, w aplikacji mobilnej zostanie wyświetlony komunikat o błędzie.
- Jeśli **validateSubmit** w tabeli TSTimesheetTable zwróci **false** podczas przesyłania grafiku w aplikacji wyświetlany jest komunikat o błędzie.
- Logika, która wypełni pola (na przykład **Właściwość wiersza**) podczas metody **wstawiania** w tabeli TSTimesheetLine, będzie nadal działać.

### <a name="hiding-and-marking-out-of-box-fields-as-read-only-via-configuration"></a>Ukrywanie i oznaczanie pól wbudowanych jako tylko do odczytu za pośrednictwem konfiguracji

Z poziomu parametrów projektu można w aplikacji mobilnej udostępniać pola, które są tylko do odczytu lub ukryte. Ustaw opcje w sekcji **Mobilne grafiki** na karcie **Grafik** na stronie **Zarządzanie projektem i parametry księgowe**.

![Parametry projektu](media/5753b8ecccd1d8bb2b002dd538b3f762.png)

### <a name="changing-the-activities-that-are-available-for-selection-via-extensions"></a>Zmiana działania, które są dostępne do wybrania za pomocą rozszerzeń

Działania dostępne do wybrania w projekcie są wprowadzane za pośrednictwem metod **getActivitiesForProject()** i **getActivityQuery()** w klasie **TsTimesheetProjectService**. Możesz użyć łańcucha poleceń, aby zmienić to zachowanie, aby dopasować je do scenariusza biznesowego dla działań, które są dostępne do wyboru dla określonego projektu.

### <a name="entering-a-default-project-category-on-timesheet-entries"></a>Wprowadzanie domyślnej kategorii projektu we wpisach grafiku

Zapisanie domyślnej kategorii projektu we wpisach grafiku ma miejsce na trzech poziomach. Aby osiągnąć wybrane zachowanie, można użyć łańcucha polecenia, który rozszerza zachowanie na dowolnym z tych poziomów lub na wszystkich tych poziomach. Stosowana jest następująca hierarchia:

1. Aplikacja próbuje umieścić kategorię domyślną z zasobu projektu. Ta kategoria domyślna jest ustawiana w metodach **getCurrentUserResource** i **getDelegatedResourcesForCurrentUser** w klasie **TSTimesheetSettingsService**.
2. Jeśli kategoria domyślna nie jest podana na poziomie zasobu projektu, aplikacja próbuje ją ściągnąć z działania projektu. Ta kategoria domyślna jest ustawiana w metodzie **getActivitiesForProject** w klasie **TSTimesheetProjectService**.
3. Jeśli domyślna kategoria nie jest podana na poziomie działania projektu, domyślna kategoria została pobrana z parametrów projektu. Ta kategoria domyślna jest ustawiana w metodzie **getProjectDetailsbyRule** w klasie **TSTimesheetProjectService**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]