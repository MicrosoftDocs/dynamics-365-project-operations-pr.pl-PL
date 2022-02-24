---
title: Koszty i przychody w projekcie
description: Ten temat zawiera informacje o szacowaniu kosztów i przychodów w projekcie.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 279c1119d334a7f60906e33b3fc7ca22ff9a360d
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/10/2021
ms.locfileid: "5148341"
---
# <a name="project-costs-and-revenue"></a>Koszty i przychody w projekcie

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Szacowania projektu zapewniają widok finansowy dla prac oszacowanych i zaplanowanych w harmonogramie projektu. Karta **Szacunki** na stronie **Projekty** pokazuje wpływ planowanej pracy na koszty i przychody. Zawiera także informacje o wielu wstępnie zdefiniowanych wymiarach. 

> ![Karta Szacunki](media/project-5.png)

## <a name="cost-and-sales-values-of-the-project"></a>Wartości kosztu i sprzedaży w projekcie

Cenniki określają stawki kosztów i rozliczania dla ról w projekcie. Wpływ pracy na koszt i sprzedaż można określić na podstawie ról skojarzonych z nazwą stanowiska oraz na podstawie nazwanego zasobu przypisanego do zadania. Jeśli istnieją zadania bez żadnych przypisań (ogólnych ani nazwanych), nie można oszacować kosztów ani sprzedaży. Wartości kosztu i sprzedaży uwzględniają daty zdefiniowane w cennikach.

### <a name="default-cost-price"></a>Domyślny koszt własny  

Każdy projekt należy do organizacji. Ta organizacja jest wyświetlana w polu **Jednostka kontraktująca** w ustawieniach projektu. Cennik skojarzony z jednostką kontraktującą jest używany do określania jednostkowego kosztu własnego. Aby ustalić poprawne koszty własne dla ról w dniu określonym w wierszach szacowania, należy poszukać kombinacji roli, jednostki i jednostki organizacyjnej na liście kosztów własnych. 

Aby można było obliczyć koszty własne zadań, muszą one być przypisane do zasobów. Każde zadanie nieprzypisane będzie miało koszt własny równy 0,00.

Jeśli kombinacja roli, jednostki i jednostki organizacyjnej nie zwraca kosztu własnego z cennika jednostki kontraktującej, system zignoruje tę jednostkę. Zamiast tego poszuka kombinacji jedynie roli i jednostki organizacyjnej. W przypadku znalezienia kosztu własnego system za pomocą współczynników konwersji przelicza go na jednostkę wybraną w wierszu szacowania.

Jeśli kombinacja roli i jednostki organizacyjnej nie zwraca kosztu własnego, system zignoruje tę jednostkę organizacyjną. Zamiast tego wyszuka kombinację roli i jednostki, aby ustawić cenę domyślną (po zastosowaniu niezbędnego przeliczenia).

Jeśli system nie znajdzie ceny dla roli, w polu kosztu własnego w wierszu szacowania zostanie ustawiona domyślna wartość **0,00**. Wszystkie kwoty kosztów w wierszach szacowania kosztów projektu są zarejestrowane w walucie jednostki kontraktującej.

> [!NOTE]
> Domyślnie program Microsoft Dynamics 365 przechowuje kwoty kosztów w walucie podstawowej. Jednak kwoty kosztów wyświetlane na karcie **Szacunki** są wyrażone w walucie jednostki kontraktującej.  

### <a name="default-sales-price"></a>Domyślna cena sprzedaży 

Treść cennika sprzedaży zależy od encji sprzedaży, do której jest dołączony projekt, lub od odbiorcy projektu. Kiedy encja sprzedaży, na przykład Szansa sprzedaży, Oferta lub Kontrakt, jest skojarzona z projektem, cena sprzedaży dla encji sprzedaży jest określana na podstawie cennika skojarzonego z ofertą lub kontraktem. Jeśli oferta lub kontrakt mają cennik niestandardowy, będzie to domyślny cennik sprzedaży dla oszacowań projektu. Jeśli nie istnieje skojarzenie z encjami sprzedaży, domyślny cennik sprzedaży z parametrów jest używany jako domyślny cennik sprzedaży w projekcie dla waluty odbiorcy określonej w projekcie.

Każdy wiersz szacowania jest skojarzony z jednostką zasobów. Jednostka zasobów wskazuje jednostkę organizacyjną, która zarezerwowała zasoby w celu wykonania zadania. Aby określić cenę sprzedaży dla skojarzonych ról, należy wyszukać kombinację roli, jednostki i jednostki zasobów na liście cenników. Jeśli w zadaniu nie ma żadnych przypisań, cena sprzedaży dla zadania wynosi 0,00.

Jeśli kombinacja roli, jednostki i jednostki zasobów nie zwraca ceny sprzedaży z cennika sprzedaży, system zignoruje tę jednostkę. Zamiast tego poszuka kombinacji jedynie roli i jednostki zasobów. W przypadku znalezienia ceny sprzedaży system za pomocą współczynników konwersji przelicza go na jednostkę wybraną w wierszu szacowania sprzedaży. 

Jeśli kombinacja roli i jednostki zasobów nie zwraca ceny sprzedaży z cennika sprzedaży, system zignoruje jednostkę zasobów. Zamiast tego wyszuka kombinację roli i jednostki, aby ustawić cenę domyślną (po zastosowaniu niezbędnego przeliczenia).

Jeśli system nie znajdzie ceny dla roli, w polu ceny sprzedaży w wierszu szacowania zostanie ustawiona domyślna wartość **0,00**.

Karta **Szacunki** zawiera widok siatki, który pokazuje wiersze szacowania. Siatka zawiera kolumny dla jednostki, łączny koszt własny oraz łączną cenę sprzedaży, jak przedstawiono na poniższej ilustracji. 

> ![Widok siatki na karcie Szacunki](media/project-6.png)

## <a name="time-phased-view-of-project-estimates"></a>Widok faz czasowych oszacowań projektu

Widok faz czasowych oszacowań projektu pokazuje dane szacunkowe w widoku siatki na osi czasu, według skali czasu wybranej przez użytkownika. Domyślnie dane szacunkowe są prezentowane względem wymiaru **Rola**.

> ![Widok faz czasowych oszacowań projektu](media/project-7.png)

## <a name="allocating-estimated-effort-based-on-the-task-mode"></a>Alokacja szacowania nakładu pracy w oparciu o tryb zadania

W widoku faz czasowych całkowity nakład pracy szacowany dla zadania jest rozkładany przez przydzielenie liczby godzin nakładu pracy na jednostkowy przedział czasu w wybranej skali czasu. Tryb zadania określa sposób alokacji nakładu pracy przez czas trwania zadania. Dwa rodzaje alokacji to **Równomiernie** i **W oparciu o godziny pracy**.

### <a name="work-hours-based-allocation"></a>Alokacja w oparciu o godziny pracy
 
W trybie zadania planowanego automatycznie domyślne dzienne godziny pracy dla zasobów wykonujących zadania są ustawiane na pełne obciążenie godzinowe pracą. To zachowanie jest stosowane podczas przydzielania nakładu pracy poprzez rozłożenie go na czas trwania zadania w widoku faz czasowych. Na przykład jeśli szacujesz, że zadanie zostanie wykonane przez jeden zasób w granicach skali czasu **Dzień**, nakład pracy przydzielony na dzień nie przekroczy godzin pracy na dzień określonych w kalendarzu projektu. W związku z tym przydział nakładu pracy zawsze gwarantuje, że zasoby zostaną wykorzystane w ciągu pełnego dnia.

### <a name="even-allocation"></a>Alokacja równomierna

W trybie zadania planowanego ręczne nie są używane godziny pracy z kalendarza projektu. Zamiast tego harmonogram zadania bazuje na danych wprowadzonych przez użytkownika. W przypadku tego typu zadań rozdział nakładu pracy na jednostkowy przedział czasu w wybranej skali czasu nie ma żadnych czynników ograniczających. Całkowity nakład pracy dla zadania jest rozdzielony równomiernie i przydzielony dla każdego jednostkowego przedziału czasu w wybranej skali czasu. W efekcie tryb zadania określony dla zadania określa rozkład nakładu pracy lub przydział nakładu pracy na jednostkowy przedział czasu w szacunkach faz czasowych.

## <a name="grouping-and-time-phasing-options"></a>Opcje grupowania i faz czasowych

Ten widok faz czasowych pokazuje rozkład szacunków nakładu pracy, kosztów i sprzedaży dla dnia, tygodnia, miesiąca lub roku. Domyślnie dane szacunkowe są prezentowane względem wymiaru **Rola**. Można jednak użyć opcji **Grupuj według**, aby pokazać widok według dwóch innych wymiarów: **Kategoria** i **Zasób**.

W obu rodzajach widoków — siatki i faz czasowych — można wybrać pola, które będą wyświetlane. Sumy każdego bloku czasu są widoczne u dołu projektu. Pokazują one łączny szacowany nakład pracy, koszt i sprzedaż w dniu, tygodniu, miesiącu lub roku. Domyślny koszt własny i cena sprzedaży mają daty obowiązywania. Innymi słowy zmieniają się dla każdego zasobu w zależności od wybranego widoku faz czasowych.

## <a name="expense-estimates"></a>Szacowanie wydatków

Przycisk **Dodaj nowe szacowanie wydatków** dostępny w widoku siatki umożliwia rejestrowanie wszystkich wydatków, które zostały poniesione w projekcie, ale nie są bezpośrednio związane z robocizną. Szacunki wydatków można rejestrować dla określonego zadania lub dla całego projektu. Należy wybrać kategorię wydatków i datę wstępną, kiedy jest spodziewane poniesienie wydatku. Jeśli na powiązanej liście kosztów własnych i w cenniku sprzedaży znajdują się ceny domyślne (lub jeśli dla kategorii wydatków zdefiniowano wartości procentowe narzutu), zostaną one automatycznie wprowadzone w wierszu szacowania po zaistnieniu powiązania.
