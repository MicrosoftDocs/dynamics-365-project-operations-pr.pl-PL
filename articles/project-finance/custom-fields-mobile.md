---
title: Zaimplementuj pola niestandardowe dla aplikacji mobilnej Microsoft Dynamics 365 Project Timesheet w systemie iOS i Android
description: W tym temat przedstawiono popularne wzorce umożliwiające korzystanie z rozszerzeń w celu implementowania pól niestandardowych.
author: KimANelson
manager: AnnBe
ms.date: 05/29/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: 4564bbda-34ea-4647-a9bc-f6ef17b1038b
ms.search.region: Global
ms.search.industry: Service industries
ms.author: knelson
ms.dyn365.ops.version: 10.0.3
ms.search.validFrom: 2019-05-29
ms.openlocfilehash: 16c3b79dcaaf8c5c491587618256694f82f44753
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/24/2020
ms.locfileid: "3754286"
---
# <a name="implement-custom-fields-for-the-microsoft-dynamics-365-project-timesheet-mobile-app-on-ios-and-android"></a><span data-ttu-id="1f81f-103">Zaimplementuj pola niestandardowe dla aplikacji mobilnej Microsoft Dynamics 365 Project Timesheet w systemie iOS i Android</span><span class="sxs-lookup"><span data-stu-id="1f81f-103">Implement custom fields for the Microsoft Dynamics 365 Project Timesheet mobile app on iOS and Android</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1f81f-104">W tym temat przedstawiono popularne wzorce umożliwiające korzystanie z rozszerzeń w celu implementowania pól niestandardowych.</span><span class="sxs-lookup"><span data-stu-id="1f81f-104">This topic provides common patterns for using extensions to implement custom fields.</span></span> <span data-ttu-id="1f81f-105">Omówiono następujące tematy:</span><span class="sxs-lookup"><span data-stu-id="1f81f-105">The following topics are covered:</span></span>

- <span data-ttu-id="1f81f-106">Różne typy danych obsługiwane przez niestandardową strukturę pól</span><span class="sxs-lookup"><span data-stu-id="1f81f-106">The various data types that the custom field framework supports</span></span>
- <span data-ttu-id="1f81f-107">Jak wyświetlać pola tylko do odczytu lub edytowalne we wpisach grafiku i zapisywać wartości podane przez użytkownika z powrotem w bazie danych</span><span class="sxs-lookup"><span data-stu-id="1f81f-107">How to show read-only or editable fields on timesheet entries, and save user-provided values back to the database</span></span>
- <span data-ttu-id="1f81f-108">Wyświetlanie pól tylko do odczytu w nagłówku karty czasu pracy</span><span class="sxs-lookup"><span data-stu-id="1f81f-108">How to show read-only fields on the timesheet header</span></span>
- <span data-ttu-id="1f81f-109">Sposób integrowania innej niestandardowej logiki biznesowej z wprowadzaniem wartości domyślnych w polach i wykonywania dodatkowych czynności sprawdzających</span><span class="sxs-lookup"><span data-stu-id="1f81f-109">How to integrate other custom business logic to enter default values in fields and do additional validation</span></span>

## <a name="audience"></a><span data-ttu-id="1f81f-110">Odbiorcy</span><span class="sxs-lookup"><span data-stu-id="1f81f-110">Audience</span></span>

<span data-ttu-id="1f81f-111">Ten temat jest przeznaczony dla deweloperów, którzy integrujący własne pola niestandardowe z aplikacją mobilną Microsoft Dynamics 365 Project Timesheet dostępną dla systemów Apple iOS i Google Android.</span><span class="sxs-lookup"><span data-stu-id="1f81f-111">This topic is intended for developers who are integrating their custom fields into the Microsoft Dynamics 365 Project Timesheet mobile application that is available for Apple iOS and Google Android.</span></span> <span data-ttu-id="1f81f-112">Założenie jest takie, że czytelnicy są zaznajomieni z rozwojem X ++ i funkcjonalnością grafiku projektów.</span><span class="sxs-lookup"><span data-stu-id="1f81f-112">The assumption is that readers are familiar with X++ development and project timesheet functionality.</span></span>

## <a name="data-contract--tstimesheetcustomfield-x-class"></a><span data-ttu-id="1f81f-113">Kontrakt dotyczący danych — Klasa TSTimesheetCustomField X++</span><span class="sxs-lookup"><span data-stu-id="1f81f-113">Data contract – TSTimesheetCustomField X++ class</span></span>

<span data-ttu-id="1f81f-114">Klasa **TSTimesheetCustomField** jest klasą kontraktu danych X++, która reprezentuje informacje o niestandardowym polu funkcji grafiku.</span><span class="sxs-lookup"><span data-stu-id="1f81f-114">The **TSTimesheetCustomField** class is the X++ data contract class that represents information about a custom field for timesheet functionality.</span></span> <span data-ttu-id="1f81f-115">Listy obiektów w polach niestandardowych są przekazywane zarówno do kontraktu danych TSTimesheetDetails, jak i kontraktu danych TSTimesheetEntry w celu wyświetlenia pól niestandardowych w aplikacji mobilnej.</span><span class="sxs-lookup"><span data-stu-id="1f81f-115">Lists of the custom field objects are passed on both the TSTimesheetDetails data contract and the TSTimesheetEntry data contract to show custom fields in the mobile app.</span></span>

- <span data-ttu-id="1f81f-116">**TSTimesheetDetails** — kontrakt nagłówka karty czasu pracy.</span><span class="sxs-lookup"><span data-stu-id="1f81f-116">**TSTimesheetDetails** - The timesheet header contract.</span></span>
- <span data-ttu-id="1f81f-117">**TSTimesheetEntry** — kontrakt transakcji na karcie czasu pracy.</span><span class="sxs-lookup"><span data-stu-id="1f81f-117">**TSTimesheetEntry** - The timesheet transaction contract.</span></span> <span data-ttu-id="1f81f-118">Grupy tych obiektów, które mają te same informacje o projekcie i wartość **timesheetLineRecId** tworzą wiersz.</span><span class="sxs-lookup"><span data-stu-id="1f81f-118">Groups of these objects that have the same project information and **timesheetLineRecId** value constitute a line.</span></span>

### <a name="fieldbasetype-types"></a><span data-ttu-id="1f81f-119">fieldBaseType (typy)</span><span class="sxs-lookup"><span data-stu-id="1f81f-119">fieldBaseType (Types)</span></span>

<span data-ttu-id="1f81f-120">Właściwość **FieldBaseType** obiektu **TsTimesheetCustom** określa typ pola, które będzie wyświetlane w aplikacji.</span><span class="sxs-lookup"><span data-stu-id="1f81f-120">The **FieldBaseType** property on the **TsTimesheetCustom** object determines the type of the field that appears in the app.</span></span> <span data-ttu-id="1f81f-121">Obsługiwane są następujące **Typy** wartości:</span><span class="sxs-lookup"><span data-stu-id="1f81f-121">The following **Types** values that are supported.</span></span>

| <span data-ttu-id="1f81f-122">Typy wartości</span><span class="sxs-lookup"><span data-stu-id="1f81f-122">Types value</span></span> | <span data-ttu-id="1f81f-123">Typ</span><span class="sxs-lookup"><span data-stu-id="1f81f-123">Type</span></span>              | <span data-ttu-id="1f81f-124">Uwagi</span><span class="sxs-lookup"><span data-stu-id="1f81f-124">Notes</span></span> |
|-------------|-------------------|-------|
| <span data-ttu-id="1f81f-125">0</span><span class="sxs-lookup"><span data-stu-id="1f81f-125">0</span></span>           | <span data-ttu-id="1f81f-126">Ciąg (i Wyliczenie)</span><span class="sxs-lookup"><span data-stu-id="1f81f-126">String (and Enum)</span></span> | <span data-ttu-id="1f81f-127">Pole jest wyświetlane jako pole tekstowe.</span><span class="sxs-lookup"><span data-stu-id="1f81f-127">The field appears as a text field.</span></span> |
| <span data-ttu-id="1f81f-128">1</span><span class="sxs-lookup"><span data-stu-id="1f81f-128">1</span></span>           | <span data-ttu-id="1f81f-129">Integer</span><span class="sxs-lookup"><span data-stu-id="1f81f-129">Integer</span></span>           | <span data-ttu-id="1f81f-130">Wartość jest wyświetlana jako liczba bez miejsc dziesiętnych.</span><span class="sxs-lookup"><span data-stu-id="1f81f-130">The value is shown as a number without decimal places.</span></span> |
| <span data-ttu-id="1f81f-131">2</span><span class="sxs-lookup"><span data-stu-id="1f81f-131">2</span></span>           | <span data-ttu-id="1f81f-132">Rzeczywista</span><span class="sxs-lookup"><span data-stu-id="1f81f-132">Real</span></span>              | <span data-ttu-id="1f81f-133">Wartość jest wyświetlana jako liczba z miejscami dziesiętnymi.</span><span class="sxs-lookup"><span data-stu-id="1f81f-133">The value is shown as a number that has decimal places.</span></span><p><span data-ttu-id="1f81f-134">Aby wyświetlić wartość rzeczywistą jako walutę w aplikacji, należy użyć właściwości **fieldExtenededType**.</span><span class="sxs-lookup"><span data-stu-id="1f81f-134">To show the real value as a currency in the app, use the **fieldExtenededType** property.</span></span> <span data-ttu-id="1f81f-135">Aby ustawić liczbę wyświetlanych miejsc dziesiętnych, można użyć właściwości **numberOfDecimals**.</span><span class="sxs-lookup"><span data-stu-id="1f81f-135">You can use the **numberOfDecimals** property to set the number of decimal places that are shown.</span></span></p> |
| <span data-ttu-id="1f81f-136">3</span><span class="sxs-lookup"><span data-stu-id="1f81f-136">3</span></span>           | <span data-ttu-id="1f81f-137">Date</span><span class="sxs-lookup"><span data-stu-id="1f81f-137">Date</span></span>              | <span data-ttu-id="1f81f-138">Formaty dat są określane przez ustawienie użytkownika **Data, godziny i format liczb** określone w **preferencjach języka i kraju / regionu** w **opcjach użytkownika**.</span><span class="sxs-lookup"><span data-stu-id="1f81f-138">Date formats are determined by the user's **Date, times, and number format** setting that is specified under **Language and country/region preference** in **User options**.</span></span> |
| <span data-ttu-id="1f81f-139">100</span><span class="sxs-lookup"><span data-stu-id="1f81f-139">4</span></span>           | <span data-ttu-id="1f81f-140">Boolean</span><span class="sxs-lookup"><span data-stu-id="1f81f-140">Boolean</span></span>           | |
| <span data-ttu-id="1f81f-141">15</span><span class="sxs-lookup"><span data-stu-id="1f81f-141">15</span></span>          | <span data-ttu-id="1f81f-142">GUID</span><span class="sxs-lookup"><span data-stu-id="1f81f-142">GUID</span></span>              | |
| <span data-ttu-id="1f81f-143">16</span><span class="sxs-lookup"><span data-stu-id="1f81f-143">16</span></span>          | <span data-ttu-id="1f81f-144">Int64</span><span class="sxs-lookup"><span data-stu-id="1f81f-144">Int64</span></span>             | |

- <span data-ttu-id="1f81f-145">Jeśli właściwość **stringOptions** nie jest podana w obiekcie **TSTimesheetCustomField**, użytkownikowi zostanie udostępnione pole dowolnego tekstu.</span><span class="sxs-lookup"><span data-stu-id="1f81f-145">If the **stringOptions** property isn't provided on the **TSTimesheetCustomField** object, a free-text field is provided to the user.</span></span>

    <span data-ttu-id="1f81f-146">Właściwość **stringLength** może służyć do ustawiania maksymalnej długości ciągu, jaką użytkownicy mogą wprowadzać.</span><span class="sxs-lookup"><span data-stu-id="1f81f-146">The **stringLength** property can be used to set the maximum string length that users can enter.</span></span>

- <span data-ttu-id="1f81f-147">Jeśli właściwość **stringOptions** jest podana dla obiektu **TSTimesheetCustomField**, te elementy listy są jedynymi wartościami, które mogą być wybierane przez użytkowników za pomocą przycisków opcji (przycisków radiowych).</span><span class="sxs-lookup"><span data-stu-id="1f81f-147">If the **stringOptions** property is provided on the **TSTimesheetCustomField** object, those list elements are the only values that users can select by using option buttons (radio buttons).</span></span>

    <span data-ttu-id="1f81f-148">W takim przypadku pole ciągu może działać jako wartość wyliczenia na potrzeby wprowadzania danych przez użytkownika.</span><span class="sxs-lookup"><span data-stu-id="1f81f-148">In this case, the string field can act as an enum value for the purpose of user entry.</span></span> <span data-ttu-id="1f81f-149">Aby zapisać wartość w bazie danych jako wyliczenie, ręcznie zamapuj wartość ciągu z powrotem na wartość wyliczenia przed zapisaniem do bazy danych za pomocą łańcucha poleceń (zobacz „Użyj łańcucha poleceń w klasie TSTimesheetEntryService, aby zapisać wpis grafiku z aplikacja z powrotem do bazy danych ”w dalszej części tego tematu, aby zapoznać się z przykładem).</span><span class="sxs-lookup"><span data-stu-id="1f81f-149">To save the value to the database as an enum, manually map the string value back to the enum value before you save to the database by using chain of command (see the “Use chain of command on the TSTimesheetEntryService class to save a timesheet entry from the app back to the database” section later in this topic for an example).</span></span>

### <a name="fieldextendedtype-tscustomfieldextendedtype"></a><span data-ttu-id="1f81f-150">fieldExtendedType (TSCustomFieldExtendedType)</span><span class="sxs-lookup"><span data-stu-id="1f81f-150">fieldExtendedType (TSCustomFieldExtendedType)</span></span>

<span data-ttu-id="1f81f-151">Za pomocą tej właściwości można formatować wartości rzeczywiste jako walutę.</span><span class="sxs-lookup"><span data-stu-id="1f81f-151">You can use this property to format real values as currency.</span></span> <span data-ttu-id="1f81f-152">To podejście ma zastosowanie tylko wtedy, gdy wartość **fieldBaseType** jest **Rzeczywista**.</span><span class="sxs-lookup"><span data-stu-id="1f81f-152">This approach is applicable only when the **fieldBaseType** value is **Real**.</span></span>

- <span data-ttu-id="1f81f-153">**TSCustomFieldExtendedType:None** — Formatowanie nie jest stosowane.</span><span class="sxs-lookup"><span data-stu-id="1f81f-153">**TSCustomFieldExtendedType:None** – No formatting is applied.</span></span>
- <span data-ttu-id="1f81f-154">**TSCustomFieldExtendedType::Waluta** – sformatuj wartość jako walutę.</span><span class="sxs-lookup"><span data-stu-id="1f81f-154">**TSCustomFieldExtendedType::Currency** – Format the value as currency.</span></span>

    <span data-ttu-id="1f81f-155">Kiedy formatowanie waluty jest aktywne, można użyć pola **stringValue**, aby przekazać kod waluty, który ma być wyświetlony w aplikacji.</span><span class="sxs-lookup"><span data-stu-id="1f81f-155">When currency formatting is active, the **stringValue** field can be used pass the currency code that should be shown in the app.</span></span> <span data-ttu-id="1f81f-156">Jest to wartość tylko do odczytu.</span><span class="sxs-lookup"><span data-stu-id="1f81f-156">The value is a read-only value.</span></span>

    <span data-ttu-id="1f81f-157">Pole **realValue** zawiera kwotę pieniężną, która powinna zostać zapisana w bazie danych.</span><span class="sxs-lookup"><span data-stu-id="1f81f-157">The **realValue** field contains the money amount that should be saved to the database.</span></span>

### <a name="fieldsection-tscustomfieldsection"></a><span data-ttu-id="1f81f-158">fieldSection (TSCustomFieldSection)</span><span class="sxs-lookup"><span data-stu-id="1f81f-158">fieldSection (TSCustomFieldSection)</span></span>

<span data-ttu-id="1f81f-159">Tej właściwości można użyć w celu określenia miejsc, w których ma być wyświetlane pole niestandardowe w aplikacji.</span><span class="sxs-lookup"><span data-stu-id="1f81f-159">You can use this property specify where the custom field should appear in the app.</span></span>

- <span data-ttu-id="1f81f-160">**TSCustomFieldSection::Nagłowek** – pole zostanie wyświetlone w sekcji **Wyświetl więcej szczegółów** w aplikacji.</span><span class="sxs-lookup"><span data-stu-id="1f81f-160">**TSCustomFieldSection::Header** – The field will appear in the **View more details** section in the app.</span></span> <span data-ttu-id="1f81f-161">Te pola są zawsze tylko do odczytu.</span><span class="sxs-lookup"><span data-stu-id="1f81f-161">These fields are always read-only.</span></span>
- <span data-ttu-id="1f81f-162">**TSCustomFieldSection::Wiersz** – pole będzie wyświetlane po wszystkich polach wiersza karty czasu pracy znajdujących się na wszystkich polach.</span><span class="sxs-lookup"><span data-stu-id="1f81f-162">**TSCustomFieldSection::Line** – The field will appear after all the out-of-box line fields on timesheet entries.</span></span> <span data-ttu-id="1f81f-163">Te pola można edytować lub tylko do odczytu.</span><span class="sxs-lookup"><span data-stu-id="1f81f-163">These fields can be either editable or read-only.</span></span>

### <a name="fieldname-fieldnameshort"></a><span data-ttu-id="1f81f-164">fieldName (FieldNameShort)</span><span class="sxs-lookup"><span data-stu-id="1f81f-164">fieldName (FieldNameShort)</span></span>

<span data-ttu-id="1f81f-165">Ta właściwość identyfikuje pole, gdy wartości dostarczane przez aplikację są zapisywane z powrotem w bazie danych.</span><span class="sxs-lookup"><span data-stu-id="1f81f-165">This property identifies the field when values that the app provides are saved back to the database.</span></span>

### <a name="tablename-tablenameshort"></a><span data-ttu-id="1f81f-166">tableName (TableNameShort)</span><span class="sxs-lookup"><span data-stu-id="1f81f-166">tableName (TableNameShort)</span></span>

<span data-ttu-id="1f81f-167">Ta właściwość identyfikuje pole, gdy wartości dostarczane przez aplikację są zapisywane z powrotem w bazie danych.</span><span class="sxs-lookup"><span data-stu-id="1f81f-167">This property identifies the field when values that the app provides are saved back to the database.</span></span>

### <a name="iseditable-noyes"></a><span data-ttu-id="1f81f-168">isEditable (NoYes)</span><span class="sxs-lookup"><span data-stu-id="1f81f-168">isEditable (NoYes)</span></span>

<span data-ttu-id="1f81f-169">Ustaw tę właściwość na **Tak**, aby określić, że pole w sekcji wpisu grafiku powinno być edytowalne przez użytkowników.</span><span class="sxs-lookup"><span data-stu-id="1f81f-169">Set this property to **Yes** to specify that the field in the timesheet entry section should be editable by users.</span></span> <span data-ttu-id="1f81f-170">Ustaw właściwość na **Nie**, aby uczynić pole tylko do odczytu.</span><span class="sxs-lookup"><span data-stu-id="1f81f-170">Set the property to **No** to make the field read-only.</span></span>

### <a name="ismandatory-noyes"></a><span data-ttu-id="1f81f-171">isMandatory (NoYes)</span><span class="sxs-lookup"><span data-stu-id="1f81f-171">isMandatory (NoYes)</span></span>

<span data-ttu-id="1f81f-172">Ustaw tę właściwość na **Tak**, aby określić, że pole w sekcji wpisu grafiku powinno być obowiązkowe.</span><span class="sxs-lookup"><span data-stu-id="1f81f-172">Set this property to **Yes** to specify that the field in the timesheet entry section should be mandatory.</span></span>

### <a name="label-str"></a><span data-ttu-id="1f81f-173">label (str)</span><span class="sxs-lookup"><span data-stu-id="1f81f-173">label (str)</span></span>

<span data-ttu-id="1f81f-174">Właściwość ta określa etykietę widoczną obok pola w aplikacji.</span><span class="sxs-lookup"><span data-stu-id="1f81f-174">This property specifies the label that is shown next the field in the app.</span></span>

### <a name="stringoptions-list-of-strings"></a><span data-ttu-id="1f81f-175">stringOptions (lista ciągów)</span><span class="sxs-lookup"><span data-stu-id="1f81f-175">stringOptions (List of Strings)</span></span>

<span data-ttu-id="1f81f-176">Ta właściwość jest stosowana tylko wtedy, gdy **fieldBaseType** jest ustawiona na wartość **Ciąg**.</span><span class="sxs-lookup"><span data-stu-id="1f81f-176">This property is applicable only when **fieldBaseType** is set to **String**.</span></span> <span data-ttu-id="1f81f-177">Jeśli ustawiona jest opcja **stringOptions**, wartości ciągów, które są dostępne do wyboru za pomocą przycisków opcji (przycisków radiowych), są określane przez ciągi na liście.</span><span class="sxs-lookup"><span data-stu-id="1f81f-177">If **stringOptions** is set, the string values that are available for selection via option buttons (radio buttons) are specified by the strings in the list.</span></span> <span data-ttu-id="1f81f-178">Jeśli nie podano żadnych ciągów, dozwolone jest wprowadzanie dowolnego tekstu w polu ciągu (przykład można znaleźć w sekcji „Używanie łańcucha poleceń w klasie TSTimesheetEntryService do zapisywania wpisu grafiku z aplikacji z powrotem do bazy danych” w dalszej części tego tematu). .</span><span class="sxs-lookup"><span data-stu-id="1f81f-178">If no strings are provided, free-text entry in the string field is allowed (see the “Use chain of command on the TSTimesheetEntryService class to save a timesheet entry from the app back to the database” section later in this topic for an example).</span></span>

### <a name="stringlength-int"></a><span data-ttu-id="1f81f-179">stringLength (int)</span><span class="sxs-lookup"><span data-stu-id="1f81f-179">stringLength (int)</span></span>

<span data-ttu-id="1f81f-180">Ta właściwość określa maksymalną długość pola w postaci ciągu.</span><span class="sxs-lookup"><span data-stu-id="1f81f-180">This property specifies the maximum length for a string field.</span></span> <span data-ttu-id="1f81f-181">Jest stosowana tylko wtedy, gdy **fieldBaseType** jest ustawiona na wartość **Ciąg**.</span><span class="sxs-lookup"><span data-stu-id="1f81f-181">It's applicable only when **fieldBaseType** is set to **String**.</span></span>

### <a name="numberofdecimals-int"></a><span data-ttu-id="1f81f-182">numberOfDecimals (int)</span><span class="sxs-lookup"><span data-stu-id="1f81f-182">numberOfDecimals (int)</span></span>

<span data-ttu-id="1f81f-183">Ta właściwość określa liczbę miejsc dziesiętnych wyświetlanych dla pola rzeczywistego.</span><span class="sxs-lookup"><span data-stu-id="1f81f-183">This property specifies the number of decimal places that are shown for a real field.</span></span> <span data-ttu-id="1f81f-184">Jest stosowana tylko wtedy, gdy **fieldBaseType** jest ustawiona na wartość **Rzeczywiste**.</span><span class="sxs-lookup"><span data-stu-id="1f81f-184">It's applicable only when **fieldBaseType** is set to **Real**.</span></span>

### <a name="ordersequence-int"></a><span data-ttu-id="1f81f-185">orderSequence (int)</span><span class="sxs-lookup"><span data-stu-id="1f81f-185">orderSequence (int)</span></span>

<span data-ttu-id="1f81f-186">Ta właściwość steruje kolejnością, w jakiej pola niestandardowe są prezentowane w aplikacji po określeniu więcej niż jednego pola niestandardowego.</span><span class="sxs-lookup"><span data-stu-id="1f81f-186">This property controls the order in which the custom fields are shown in the app when more than one custom field is specified.</span></span> <span data-ttu-id="1f81f-187">Pola z mniejszymi numerami są prezentowane w pierwszej kolejności.</span><span class="sxs-lookup"><span data-stu-id="1f81f-187">Fields that have lower numbers are shown first.</span></span>

### <a name="booleanvalue-boolean"></a><span data-ttu-id="1f81f-188">booleanValue (wartość logiczna)</span><span class="sxs-lookup"><span data-stu-id="1f81f-188">booleanValue (boolean)</span></span>

<span data-ttu-id="1f81f-189">W przypadku pól typu **logiczna** ta właściwość przekazuje wartość logiczną pola między serwerem a aplikacją.</span><span class="sxs-lookup"><span data-stu-id="1f81f-189">For fields of the **Boolean** type, this property passes the Boolean value of the field between the server and the app.</span></span>

### <a name="guidvalue-guid"></a><span data-ttu-id="1f81f-190">guidValue (identyfikator GUID)</span><span class="sxs-lookup"><span data-stu-id="1f81f-190">guidValue (guid)</span></span>

<span data-ttu-id="1f81f-191">W przypadku pól typu **GUID** ta właściwość przekazuje wartość unikatowy identyfikator globalny (GUID) pola między serwerem a aplikacją.</span><span class="sxs-lookup"><span data-stu-id="1f81f-191">For fields of the **GUID** type, this property passes the globally unique identifier (GUID) value of the field between the server and the app.</span></span>

### <a name="int64value-int64"></a><span data-ttu-id="1f81f-192">int64Value (Int64)</span><span class="sxs-lookup"><span data-stu-id="1f81f-192">int64Value (int64)</span></span>

<span data-ttu-id="1f81f-193">W przypadku pól typu **Int64** ta właściwość przekazuje wartość Int64 pola między serwerem a aplikacją.</span><span class="sxs-lookup"><span data-stu-id="1f81f-193">For fields of the **Int64** type, this property passes the int64 value of the field between the server and the app.</span></span>

### <a name="intvalue-int"></a><span data-ttu-id="1f81f-194">intValue (int)</span><span class="sxs-lookup"><span data-stu-id="1f81f-194">intValue (int)</span></span>

<span data-ttu-id="1f81f-195">W przypadku pól typu **Int** ta właściwość przekazuje wartość int pola między serwerem a aplikacją.</span><span class="sxs-lookup"><span data-stu-id="1f81f-195">For fields of the **Int** type, this property passes the int value of the field between the server and the app.</span></span>

### <a name="realvalue-real"></a><span data-ttu-id="1f81f-196">realValue (rzeczywista)</span><span class="sxs-lookup"><span data-stu-id="1f81f-196">realValue (real)</span></span>

<span data-ttu-id="1f81f-197">W przypadku pól typu **Rzeczywista** ta właściwość przekazuje wartość rzeczywistą pola między serwerem a aplikacją.</span><span class="sxs-lookup"><span data-stu-id="1f81f-197">For fields of the **Real** type, this property passes the real value of the field between the server and the app .</span></span>

### <a name="stringvalue-str"></a><span data-ttu-id="1f81f-198">stringValue (str)</span><span class="sxs-lookup"><span data-stu-id="1f81f-198">stringValue (str)</span></span>

<span data-ttu-id="1f81f-199">W przypadku pól typu **Ciąg** ta właściwość przekazuje wartość ciąg pola między serwerem a aplikacją.</span><span class="sxs-lookup"><span data-stu-id="1f81f-199">For fields of the **String** type, this property passes the string value of the field between the server and the app.</span></span> <span data-ttu-id="1f81f-200">Jest on również używany w przypadku pól o typie **rzeczywistym**, które są sformatowane jako waluta.</span><span class="sxs-lookup"><span data-stu-id="1f81f-200">It's also used for fields of the **Real** type that are formatted as currency.</span></span> <span data-ttu-id="1f81f-201">W przypadku tych pól właściwość jest używana do przekazania kodu waluty do aplikacji.</span><span class="sxs-lookup"><span data-stu-id="1f81f-201">For those fields, the property is used to pass the currency code to the app.</span></span>

### <a name="datevalue-date"></a><span data-ttu-id="1f81f-202">dateValue (data)</span><span class="sxs-lookup"><span data-stu-id="1f81f-202">dateValue (date)</span></span>

<span data-ttu-id="1f81f-203">W przypadku pól typu **Data** ta właściwość przekazuje wartość daty pola między serwerem a aplikacją.</span><span class="sxs-lookup"><span data-stu-id="1f81f-203">For fields of the **Date** type, this property passes the date value of the field between the server and the app.</span></span>

## <a name="show-and-save-a-custom-field-in-the-timesheet-entry-section"></a><span data-ttu-id="1f81f-204">Wyświetlanie i zapisywanie pola niestandardowego w sekcji wpisu grafiku</span><span class="sxs-lookup"><span data-stu-id="1f81f-204">Show and save a custom field in the timesheet entry section</span></span>

<span data-ttu-id="1f81f-205">Poniżej znajduje się zrzut ekranu z aplikacji mobilnej utworzenia wpisu karty czasu pracy.</span><span class="sxs-lookup"><span data-stu-id="1f81f-205">Below is a screenshot from the mobile app of a timesheet entry creation.</span></span> <span data-ttu-id="1f81f-206">Pokazuje gotowe pola i pole niestandardowe w sekcji „Wprowadzanie czasu” o nazwie „Ciąg testowy” z już ustawioną wartością wyliczenia „Druga opcja”.</span><span class="sxs-lookup"><span data-stu-id="1f81f-206">It shows the out-of-box fields and a custom field in the "Time entry" section called "Test string" with an enum value of "Second option" already set.</span></span>

![Pole niestandardowe ciągu testowego w aplikacji](media/timesheet-entry.jpg)



<span data-ttu-id="1f81f-208">Poniżej znajduje się zrzut ekranu z aplikacji mobilnej użytkownika, który wybiera jedną z opcji wyliczenia dostępnych dla pola niestandardowego „Ciąg testowy”.</span><span class="sxs-lookup"><span data-stu-id="1f81f-208">Below is a screenshot from the mobile app of the user selecting one of the enum options available for the "Test string" custom field.</span></span>  <span data-ttu-id="1f81f-209">Dwie opcje to „Pierwsza opcja” i „Druga opcja” pokazane jako przyciski opcji.</span><span class="sxs-lookup"><span data-stu-id="1f81f-209">The two options are "First option" and "Second option" shown as radio buttons.</span></span> <span data-ttu-id="1f81f-210">Druga opcja jest obecnie zaznaczona.</span><span class="sxs-lookup"><span data-stu-id="1f81f-210">The second option is currently selected.</span></span>

![Przyciski opcji (przyciski radiowe) dla pola niestandardowego ciągu testowego](media/enum-option.jpg)



### <a name="extend-the-tstimesheetline-table-so-that-it-has-a-custom-field"></a><span data-ttu-id="1f81f-212">Rozszerzanie tabeli TSTimesheetLine tak, aby zawiera pole niestandardowe</span><span class="sxs-lookup"><span data-stu-id="1f81f-212">Extend the TSTimesheetLine table so that it has a custom field</span></span>

<span data-ttu-id="1f81f-213">W typowych scenariuszach jest prawdopodobne, że dane pola niestandardowego w sekcji wpisu grafiku zostaną zapisane w tabeli TSTimesheetLine.</span><span class="sxs-lookup"><span data-stu-id="1f81f-213">In typical scenarios, it's likely that the data for a custom field in the timesheet entry section will be saved to the TSTimesheetLine table.</span></span> <span data-ttu-id="1f81f-214">W przypadku, gdy dane mogą zostać pobrane na podstawie określonego rekordu TSTimesheetTrans lub jeśli nie ma określonego kontekstu rekordów (na przykład jeśli pole jest ustawione jako tylko do odczytu w parametrach projektu), można użyć innych tabel.</span><span class="sxs-lookup"><span data-stu-id="1f81f-214">However, other tables can be used if the data can be retrieved based on a TSTimesheetTrans record that is provided, or if it doesn't have specific record context (for example, if the field is set as read-only in the project parameters).</span></span>

<span data-ttu-id="1f81f-215">Należy pamiętać, że pola niestandardowe nie muszą zawierać żadnych kopii zapasowych rekordów bazy danych.</span><span class="sxs-lookup"><span data-stu-id="1f81f-215">Note that custom fields don't have to have any backing database records.</span></span> <span data-ttu-id="1f81f-216">Można je dynamicznie generować na podstawie logiki X++.</span><span class="sxs-lookup"><span data-stu-id="1f81f-216">They can be dynamically generated based on X++ logic.</span></span> <span data-ttu-id="1f81f-217">Takie podejście może być przydatne w scenariuszach tylko do odczytu (zobacz sekcję „Używanie łańcucha poleceń w klasie TSTimesheetDetails, metoda buildCustomFieldListForHeader do wypełniania szczegółów karty czasu pracy”, aby zapoznać się z przykładem dynamicznie generowanych wartości pól niestandardowych).</span><span class="sxs-lookup"><span data-stu-id="1f81f-217">This approach can be useful in read-only scenarios (see the “Use chain of command on the TSTimesheetDetails class, buildCustomFieldListForHeader method to fill in timesheet details” section for an example of dynamically generated custom field values.)</span></span>

<span data-ttu-id="1f81f-218">Poniżej znajduje się zrzut ekranu z Visual Studio drzewa obiektów aplikacji.</span><span class="sxs-lookup"><span data-stu-id="1f81f-218">Below is a screenshot from Visual Studio of the Application Object Tree.</span></span> <span data-ttu-id="1f81f-219">Wskazuje ono rozszerzenie tabeli TSTimesheetLine z polem TestLineString dodany jako pole niestandardowe.</span><span class="sxs-lookup"><span data-stu-id="1f81f-219">It shows an extension of the TSTimesheetLine table with the TestLineString field added as a custom field.</span></span>

![Ciąg wiersza](media/b6756b4a3fc5298093327a088a7710fd.png)

### <a name="use-chain-of-command-on-the-buildcustomfieldlist-method-of-the-tstimesheetsettings-class-to-show-a-field-in-the-timesheet-entry-section"></a><span data-ttu-id="1f81f-221">W celu wyświetlenia pola w sekcji wpisu grafiku Użyj łańcucha poleceń dla metody buildCustomFieldList klasy TSTimesheetSettings</span><span class="sxs-lookup"><span data-stu-id="1f81f-221">Use chain of command on the buildCustomFieldList method of the TSTimesheetSettings class to show a field in the timesheet entry section</span></span>

<span data-ttu-id="1f81f-222">Ten kod Steruje ustawieniami wyświetlania pola w aplikacji.</span><span class="sxs-lookup"><span data-stu-id="1f81f-222">This code controls the display settings for the field in the app.</span></span> <span data-ttu-id="1f81f-223">Na przykład kontroluje typ pola, etykietę, czy pole jest obowiązkowe oraz w jakiej sekcji pojawia się pole.</span><span class="sxs-lookup"><span data-stu-id="1f81f-223">For example, it controls the type of field, the label, whether the field is mandatory, and what section the field appears in.</span></span>

<span data-ttu-id="1f81f-224">W poniższym przykładzie przedstawiono pole ciągu na wpisach czasowych.</span><span class="sxs-lookup"><span data-stu-id="1f81f-224">The following example shows a string field on time entries.</span></span> <span data-ttu-id="1f81f-225">W tym polu są dostępne dwie opcje, **Pierwsza opcja** i **Druga opcja**, dostępnych za pośrednictwem przycisków opcji (przycisków radiowych).</span><span class="sxs-lookup"><span data-stu-id="1f81f-225">This field has two options, **First option** and **Second option**, that are available via option buttons (radio buttons).</span></span> <span data-ttu-id="1f81f-226">Pole w aplikacji jest skojarzone z polem **TestLineString** dodawanym do tabeli TSTimesheetLine.</span><span class="sxs-lookup"><span data-stu-id="1f81f-226">The field in the app is associated with the **TestLineString** field that is added to the TSTimesheetLine table.</span></span>

<span data-ttu-id="1f81f-227">Zwróć uwagę na użycie metody **TSTimesheetCustomField::newFromMetatdata()** w celu uproszczenia inicjowania niestandardowych właściwości pola: **fieldBaseType**, **tableName**, **fieldname**, **label**, **isEditable**, **isMandatory**, **stringLength** i **numberOfDecimals**.</span><span class="sxs-lookup"><span data-stu-id="1f81f-227">Note the use of the **TSTimesheetCustomField::newFromMetatdata()** method to simplify the initialization of the custom field properties: **fieldBaseType**, **tableName**, **fieldname**, **label**, **isEditable**, **isMandatory**, **stringLength**, and **numberOfDecimals**.</span></span> <span data-ttu-id="1f81f-228">Te parametry można również ustawić ręcznie, zależnie od preferencji.</span><span class="sxs-lookup"><span data-stu-id="1f81f-228">You can also set these parameters manually, as you prefer.</span></span>

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

### <a name="use-chain-of-command-on-the-buildcustomfieldlistforentry-method-of-the-tstimesheetentry-class-to-enter-values-in-a-timesheet-entry"></a><span data-ttu-id="1f81f-229">Użyj łańcucha poleceń w metodzie buildCustomFieldListForEntry klasy TSTimesheetEntry do wprowadzania wartości we wpisie grafiku</span><span class="sxs-lookup"><span data-stu-id="1f81f-229">Use chain of command on the buildCustomFieldListForEntry method of the TSTimesheetEntry class to enter values in a timesheet entry</span></span>

<span data-ttu-id="1f81f-230">Metoda **buildCustomFieldListForEntry** służy do wprowadzania wartości w zapisanych wierszach karty czasu pracy w aplikacji mobilnej.</span><span class="sxs-lookup"><span data-stu-id="1f81f-230">The **buildCustomFieldListForEntry** method is used to enter values on the saved timesheet lines in the mobile app.</span></span> <span data-ttu-id="1f81f-231">Jako parametr przyjmuje rekord TSTimesheetTrans.</span><span class="sxs-lookup"><span data-stu-id="1f81f-231">It takes a TSTimesheetTrans record as a parameter.</span></span> <span data-ttu-id="1f81f-232">Pól z tego rekordu można użyć do wypełnienia wartości pola niestandardowego w aplikacji.</span><span class="sxs-lookup"><span data-stu-id="1f81f-232">Fields from that record can be used to fill in the custom field value in the app.</span></span>

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

### <a name="use-chain-of-command-on-the-tstimesheetentryservice-class-to-save-a-timesheet-entry-from-the-app-back-to-the-database"></a><span data-ttu-id="1f81f-233">W celu zapisania wpisu grafiku z powrotem do bazy danych należy użyć łańcuchu poleceń klasy TSTimesheetEntryService</span><span class="sxs-lookup"><span data-stu-id="1f81f-233">Use chain of command on the TSTimesheetEntryService class to save a timesheet entry from the app back to the database</span></span>

<span data-ttu-id="1f81f-234">Aby zapisać pole niestandardowe z powrotem do bazy danych przy użyciu programu w typowy sposób, należy rozszerzyć wiele metod:</span><span class="sxs-lookup"><span data-stu-id="1f81f-234">To save a custom field back to the database in typical usage, you must extend multiple methods:</span></span>

- <span data-ttu-id="1f81f-235">Metoda **timesheetLineNeedsUpdating** jest używana w celu ustalenia, czy rekord wiersza został zmieniony przez użytkownika w aplikacji i musi zostać zapisany w bazie danych.</span><span class="sxs-lookup"><span data-stu-id="1f81f-235">The **timesheetLineNeedsUpdating** method is used to determine whether the line record has been changed by the user in the app and must be saved to the database.</span></span> <span data-ttu-id="1f81f-236">Jeśli wydajność nie jest istotna, można ją uprościć, aby zawsze zwracała wartość **true** (prawda).</span><span class="sxs-lookup"><span data-stu-id="1f81f-236">If performance isn't a concern, this method can be simplified so that it always returns **true**.</span></span>
- <span data-ttu-id="1f81f-237">Metody **populateTimesheetLineFromEntryDuringCreate** i **populateTimesheetLineFromEntryDuringUpdate** mogą być rozszerzane w taki sposób, aby były wprowadzane w rekordzie TSTimesheetLine bazy danych z dostarczonego rekordu dotyczącego kontraktu danych TSTimesheetEntry.</span><span class="sxs-lookup"><span data-stu-id="1f81f-237">The **populateTimesheetLineFromEntryDuringCreate** and **populateTimesheetLineFromEntryDuringUpdate** methods can be extended so that they enter values in the TSTimesheetLine database record from the TSTimesheetEntry data contract record that is provided.</span></span> <span data-ttu-id="1f81f-238">W poniższym przykładzie pokazano, jak ręczne mapowanie między polem bazy danych a polem wprowadzania jest wykonywane ręcznie za pomocą kodu X++.</span><span class="sxs-lookup"><span data-stu-id="1f81f-238">In the example that follows, notice how the mapping between the database field and the entry field is manually done via X++ code.</span></span>
- <span data-ttu-id="1f81f-239">Metodę **populateTimesheetWeekFromEntry** można również rozszerzyć, jeśli pole niestandardowe mapowane na obiekt **TSTimesheetEntry** musi zostać zapisane z powrotem do tabeli bazy danych TSTimesheetLineweek.</span><span class="sxs-lookup"><span data-stu-id="1f81f-239">The **populateTimesheetWeekFromEntry** method can also be extended if the custom field that is mapped to the **TSTimesheetEntry** object must write back to the TSTimesheetLineweek database table.</span></span>

> [!NOTE]
> <span data-ttu-id="1f81f-240">Poniższy przykład zapisuje wartość **firstOption** lub **secondOption**, która jest wybierana przez użytkownika do bazy danych w postaci nieprzetworzonej wartości ciągu.</span><span class="sxs-lookup"><span data-stu-id="1f81f-240">The following example saves the **firstOption** or **secondOption** value that the user selects to the database as a raw string value.</span></span> <span data-ttu-id="1f81f-241">Jeśli pole bazy danych jest polem typu **Wyliczenie**, można je ręcznie zamapować na wartość enum, a następnie zapisać w polu wyliczenia w tabeli bazy danych.</span><span class="sxs-lookup"><span data-stu-id="1f81f-241">If the database field is a field of the **Enum** type, those values can be manually mapped to an enum value and then saved to an enum field on the database table.</span></span>

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

## <a name="show-a-custom-field-in-the-timesheet-header-section"></a><span data-ttu-id="1f81f-242">Pokaż pole niestandardowe w sekcji nagłówka grafiku</span><span class="sxs-lookup"><span data-stu-id="1f81f-242">Show a custom field in the timesheet header section</span></span>

<span data-ttu-id="1f81f-243">Poniżej znajduje się zrzut ekranu z aplikacji mobilnej użytkownika przeglądającego grafik.</span><span class="sxs-lookup"><span data-stu-id="1f81f-243">Below is a screenshot from the mobile app of a user viewing a timesheet.</span></span> <span data-ttu-id="1f81f-244">W prawym górnym rogu został wybrany przycisk „Więcej informacji”, aby wyświetlić opcję „Wyświetl więcej szczegółów”.</span><span class="sxs-lookup"><span data-stu-id="1f81f-244">The "More information" button has been selected in the upper-right corner to show the "View more details" option.</span></span>  

![Wyświetl więcej szczegółów polecenia](media/show-more.png)

<span data-ttu-id="1f81f-246">Poniżej znajduje się zrzut ekranu z aplikacji mobilnej pokazujący sekcję „Więcej” grafiku.</span><span class="sxs-lookup"><span data-stu-id="1f81f-246">Below is a screenshot from the mobile app showing the “More” section of a timesheet.</span></span> <span data-ttu-id="1f81f-247">Do sekcji nagłówka grafiku dodano pole niestandardowe o nazwie „Stopień wykorzystania tego grafiku (obliczone pole niestandardowe)”.</span><span class="sxs-lookup"><span data-stu-id="1f81f-247">A custom field called “Utilization rate of this timesheet (computed custom field)” has been added to the timesheet header section.</span></span> <span data-ttu-id="1f81f-248">W polu niestandardowym ustawiono wartość tylko do odczytu „0,667”.</span><span class="sxs-lookup"><span data-stu-id="1f81f-248">A read-only value of "0.667" is set on the custom field.</span></span>

![Więcej sekcji](media/more-section.jpg)

### <a name="extend-the-tstimesheettable-table-so-that-it-has-a-custom-field"></a><span data-ttu-id="1f81f-250">Rozszerzanie tabeli TSTimesheetTable tak, aby zawiera pole niestandardowe</span><span class="sxs-lookup"><span data-stu-id="1f81f-250">Extend the TSTimesheetTable table so that it has a custom field</span></span>

<span data-ttu-id="1f81f-251">W typowych scenariuszach jest prawdopodobne, że dane dla pola niestandardowego w sekcji nagłówka zostaną pobrane z tabeli TSTimesheetHeader.</span><span class="sxs-lookup"><span data-stu-id="1f81f-251">In typical scenarios, it's likely that the data for a custom field in the header section will be pulled from the TSTimesheetHeader table.</span></span> <span data-ttu-id="1f81f-252">W przypadku, gdy dane mogą zostać pobrane na podstawie określonego rekordu TSTimesheetTable lub jeśli nie ma określonego kontekstu rekordów (na przykład jeśli pole jest ustawione jako tylko do odczytu w parametrach projektu), można użyć innych tabel.</span><span class="sxs-lookup"><span data-stu-id="1f81f-252">However, other tables can be used if the data can be retrieved based on a TSTimesheetTable record that is provided, or if it doesn't have specific record context (for example, if the field is set as read-only in the project parameters).</span></span>

<span data-ttu-id="1f81f-253">Należy pamiętać, że pola niestandardowe nie muszą zawierać żadnych kopii zapasowych rekordów bazy danych.</span><span class="sxs-lookup"><span data-stu-id="1f81f-253">Note that custom fields don't have to have any backing database records.</span></span> <span data-ttu-id="1f81f-254">Można je dynamicznie generować na podstawie logiki X++.</span><span class="sxs-lookup"><span data-stu-id="1f81f-254">They can be dynamically generated based on X++ logic.</span></span> <span data-ttu-id="1f81f-255">Poniższy przykład ilustruje tę metodę.</span><span class="sxs-lookup"><span data-stu-id="1f81f-255">The example that follows shows this approach.</span></span>

<span data-ttu-id="1f81f-256">Pola znajdujące się w sekcji nagłówka są zawsze tylko do odczytu w aplikacji.</span><span class="sxs-lookup"><span data-stu-id="1f81f-256">Fields in the header section are always read-only in the app.</span></span>

### <a name="use-chain-of-command-on-the-buildcustomfieldlist-method-of-the-tstimesheetsettings-class-to-show-a-field-in-the-header-section"></a><span data-ttu-id="1f81f-257">Użyj łańcucha poleceń w metodzie buildCustomFieldList klasy TSTimesheetSettings, aby wyświetlić pole w sekcji nagłówka</span><span class="sxs-lookup"><span data-stu-id="1f81f-257">Use chain of command on the buildCustomFieldList method of the TSTimesheetSettings class to show a field in the header section</span></span>

<span data-ttu-id="1f81f-258">Ten kod Steruje ustawieniami wyświetlania pola w aplikacji.</span><span class="sxs-lookup"><span data-stu-id="1f81f-258">This code controls the display settings for the field in the app.</span></span> <span data-ttu-id="1f81f-259">Na przykład kontroluje typ pola, etykietę, czy pole jest obowiązkowe oraz w jakiej sekcji pojawia się pole.</span><span class="sxs-lookup"><span data-stu-id="1f81f-259">For example, it controls the type of field, the label, whether the field is mandatory, and what section the field appears in.</span></span>

<span data-ttu-id="1f81f-260">W poniższym przykładzie pokazano obliczoną wartość w sekcji nagłówka w aplikacji.</span><span class="sxs-lookup"><span data-stu-id="1f81f-260">The following example shows a computed value in the header section in the app.</span></span>

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

### <a name="use-chain-of-command-on-the-buildcustomfieldlistforheader-method-of-the-tstimesheetdetails-class-to-fill-in-timesheet-details"></a><span data-ttu-id="1f81f-261">Użyj łańcucha poleceń w metodzie buildCustomFieldListForHeader klasy TSTimesheetDetails, aby wypełnić szczegóły grafiku</span><span class="sxs-lookup"><span data-stu-id="1f81f-261">Use chain of command on the buildCustomFieldListForHeader method of the TSTimesheetDetails class to fill in timesheet details</span></span>

<span data-ttu-id="1f81f-262">Metoda **buildCustomFieldListForHeader** służy do wypełniania szczegółów nagłówka karty czasu pracy w aplikacji mobilnej.</span><span class="sxs-lookup"><span data-stu-id="1f81f-262">The **buildCustomFieldListForHeader** method is used to fill in the timesheet header details in the mobile app.</span></span> <span data-ttu-id="1f81f-263">Jako parametr przyjmuje rekord TSTimesheetTable.</span><span class="sxs-lookup"><span data-stu-id="1f81f-263">It takes a TSTimesheetTable record as a parameter.</span></span> <span data-ttu-id="1f81f-264">Pól z tego rekordu można użyć do wypełnienia wartości pola niestandardowego w aplikacji.</span><span class="sxs-lookup"><span data-stu-id="1f81f-264">Fields from that record can be used to fill in the custom field value in the app.</span></span> <span data-ttu-id="1f81f-265">W poniższym przykładzie nie są odczytywane żadne wartości z bazy danych.</span><span class="sxs-lookup"><span data-stu-id="1f81f-265">The following example doesn't read any values from the database.</span></span> <span data-ttu-id="1f81f-266">Zamiast tego używa logiki X ++ do generowania wartości obliczonej, która jest następnie wyświetlana w aplikacji.</span><span class="sxs-lookup"><span data-stu-id="1f81f-266">Instead, it uses X++ logic to generate a computed value that is then shown in the app.</span></span>


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

## <a name="other-configurabilityextensibility-opportunities"></a><span data-ttu-id="1f81f-267">Inne możliwości konfigurowalności/rozszerzalności</span><span class="sxs-lookup"><span data-stu-id="1f81f-267">Other configurability/extensibility opportunities</span></span>

### <a name="adding-additional-validation-for-the-app"></a><span data-ttu-id="1f81f-268">Trwa dodawanie dodatkowych poprawność aplikacji</span><span class="sxs-lookup"><span data-stu-id="1f81f-268">Adding additional validation for the app</span></span>

<span data-ttu-id="1f81f-269">Istniejąca logika funkcji grafiku na poziomie bazy danych będzie nadal działać zgodnie z oczekiwaniami.</span><span class="sxs-lookup"><span data-stu-id="1f81f-269">Existing logic for timesheet functionality at the database level will still work as expected.</span></span> <span data-ttu-id="1f81f-270">Aby przerwać wykonywanie operacji zapisywania lub przesyłania i wyświetlać określony komunikat o błędzie, można dodać do kodu **błąd typu throw („wiadomość do użytkownika”)** za pośrednictwem łańcucha rozszerzeń poleceń.</span><span class="sxs-lookup"><span data-stu-id="1f81f-270">To interrupt the completion of save or submit operations and show a specific error message, you can add **throw error("message to user")** to the code via a chain of command extension.</span></span> <span data-ttu-id="1f81f-271">Oto trzy przykłady przydatnych metod rozszerzalności:</span><span class="sxs-lookup"><span data-stu-id="1f81f-271">Here are three examples of useful extensible methods:</span></span>

- <span data-ttu-id="1f81f-272">Jeśli **validateWrite** w tabeli TSTimesheetLine zwróci **false** podczas operacji zapisywania wiersza grafiku, w aplikacji mobilnej zostanie wyświetlony komunikat o błędzie.</span><span class="sxs-lookup"><span data-stu-id="1f81f-272">If **validateWrite** on the TSTimesheetLine table returns **false** during a save operation for a timesheet line, an error message is shown in the mobile app.</span></span>
- <span data-ttu-id="1f81f-273">Jeśli **validateSubmit** w tabeli TSTimesheetTable zwróci **false** podczas przesyłania grafiku w aplikacji wyświetlany jest komunikat o błędzie.</span><span class="sxs-lookup"><span data-stu-id="1f81f-273">If **validateSubmit** on the TSTimesheetTable table returns **false** during timesheet submission in the app, an error message is shown to the user.</span></span>
- <span data-ttu-id="1f81f-274">Logika, która wypełni pola (na przykład **Właściwość wiersza**) podczas metody **wstawiania** w tabeli TSTimesheetLine, będzie nadal działać.</span><span class="sxs-lookup"><span data-stu-id="1f81f-274">Logic that fills in fields (for example, **Line Property**) during the **insert** method on the TSTimesheetLine table will still run.</span></span>

### <a name="hiding-and-marking-out-of-box-fields-as-read-only-via-configuration"></a><span data-ttu-id="1f81f-275">Ukrywanie i oznaczanie pól wbudowanych jako tylko do odczytu za pośrednictwem konfiguracji</span><span class="sxs-lookup"><span data-stu-id="1f81f-275">Hiding and marking out-of-box fields as read-only via configuration</span></span>

<span data-ttu-id="1f81f-276">Z poziomu parametrów projektu można w aplikacji mobilnej udostępniać pola, które są tylko do odczytu lub ukryte.</span><span class="sxs-lookup"><span data-stu-id="1f81f-276">From the project parameters, you can make out-of-box fields read-only or hidden in the mobile app.</span></span> <span data-ttu-id="1f81f-277">Ustaw opcje w sekcji **Mobilne grafiki** na karcie **Grafik** na stronie **Zarządzanie projektem i parametry księgowe**.</span><span class="sxs-lookup"><span data-stu-id="1f81f-277">Set the options in the **Mobile timesheets** section on the **Timesheet** tab of the **Project management and accounting parameters** page.</span></span>

![Parametry projektu](media/5753b8ecccd1d8bb2b002dd538b3f762.png)

### <a name="changing-the-activities-that-are-available-for-selection-via-extensions"></a><span data-ttu-id="1f81f-279">Zmiana działania, które są dostępne do wybrania za pomocą rozszerzeń</span><span class="sxs-lookup"><span data-stu-id="1f81f-279">Changing the activities that are available for selection via extensions</span></span>

<span data-ttu-id="1f81f-280">Działania dostępne do wybrania w projekcie są wprowadzane za pośrednictwem metod **getActivitiesForProject()** i **getActivityQuery()** w klasie **TsTimesheetProjectService**.</span><span class="sxs-lookup"><span data-stu-id="1f81f-280">The activities that are available for selection for a project are filled in via the **getActivitiesForProject()** and **getActivityQuery()** methods in the **TsTimesheetProjectService** class.</span></span> <span data-ttu-id="1f81f-281">Możesz użyć łańcucha poleceń, aby zmienić to zachowanie, aby dopasować je do scenariusza biznesowego dla działań, które są dostępne do wyboru dla określonego projektu.</span><span class="sxs-lookup"><span data-stu-id="1f81f-281">You can use chain of command to change this behavior to match your business scenario for the activities that are available for selection for a specific project.</span></span>

### <a name="entering-a-default-project-category-on-timesheet-entries"></a><span data-ttu-id="1f81f-282">Wprowadzanie domyślnej kategorii projektu we wpisach grafiku</span><span class="sxs-lookup"><span data-stu-id="1f81f-282">Entering a default project category on timesheet entries</span></span>

<span data-ttu-id="1f81f-283">Zapisanie domyślnej kategorii projektu we wpisach grafiku ma miejsce na trzech poziomach.</span><span class="sxs-lookup"><span data-stu-id="1f81f-283">Entry of a default project category on timesheet entries occurs at three levels.</span></span> <span data-ttu-id="1f81f-284">Aby osiągnąć wybrane zachowanie, można użyć łańcucha polecenia, który rozszerza zachowanie na dowolnym z tych poziomów lub na wszystkich tych poziomach.</span><span class="sxs-lookup"><span data-stu-id="1f81f-284">You can use chain of command to extend the behavior at any or all of these levels to achieve the desired behavior.</span></span> <span data-ttu-id="1f81f-285">Stosowana jest następująca hierarchia:</span><span class="sxs-lookup"><span data-stu-id="1f81f-285">The following hierarchy is used:</span></span>

1. <span data-ttu-id="1f81f-286">Aplikacja próbuje umieścić kategorię domyślną z zasobu projektu.</span><span class="sxs-lookup"><span data-stu-id="1f81f-286">The app tries to put the default category from the project resource.</span></span> <span data-ttu-id="1f81f-287">Ta kategoria domyślna jest ustawiana w metodach **getCurrentUserResource** i **getDelegatedResourcesForCurrentUser** w klasie **TSTimesheetSettingsService**.</span><span class="sxs-lookup"><span data-stu-id="1f81f-287">This default category is set in the **getCurrentUserResource** and **getDelegatedResourcesForCurrentUser** methods in the **TSTimesheetSettingsService** class.</span></span>
2. <span data-ttu-id="1f81f-288">Jeśli kategoria domyślna nie jest podana na poziomie zasobu projektu, aplikacja próbuje ją ściągnąć z działania projektu.</span><span class="sxs-lookup"><span data-stu-id="1f81f-288">If the default category isn't provided at the project resource level, the app tries to pull it from the project activity.</span></span> <span data-ttu-id="1f81f-289">Ta kategoria domyślna jest ustawiana w metodzie **getActivitiesForProject** w klasie **TSTimesheetProjectService**.</span><span class="sxs-lookup"><span data-stu-id="1f81f-289">This default category is set in the **getActivitiesForProject** method in the **TSTimesheetProjectService** class.</span></span>
3. <span data-ttu-id="1f81f-290">Jeśli domyślna kategoria nie jest podana na poziomie działania projektu, domyślna kategoria została pobrana z parametrów projektu.</span><span class="sxs-lookup"><span data-stu-id="1f81f-290">If the default category isn't provided at the project activity level, the default category it taken from the project parameters.</span></span> <span data-ttu-id="1f81f-291">Ta kategoria domyślna jest ustawiana w metodzie **getProjectDetailsbyRule** w klasie **TSTimesheetProjectService**.</span><span class="sxs-lookup"><span data-stu-id="1f81f-291">This default category is set in the **getProjectDetailsbyRule** method in the **TSTimesheetProjectService** class.</span></span>
