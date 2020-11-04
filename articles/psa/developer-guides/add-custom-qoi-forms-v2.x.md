---
title: Dodawanie nowych niestandardowych formularzy encji (Project Service Automation wer. 2.x)
description: W tym temacie przedstawiono informacje na temat dodawania niestandardowych formularzy encji szans sprzedaży, ofert, zamówień lub faktur w programie Dynamics 365 Project Service Automation w wersji 2.x.
author: makk
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 3/14/2019
ms.topic: article
ms.service: business-applications
ms.author: makk
audience: admin
search.audienceType:
- admin
- customizer
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 57d4b9aad433af6d3e73369c76f2793f349c6965
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082206"
---
# <a name="add-new-custom-entity-forms-project-service-automation-2x"></a><span data-ttu-id="197af-103">Dodawanie nowych niestandardowych formularzy encji (Project Service Automation wer. 2.x)</span><span class="sxs-lookup"><span data-stu-id="197af-103">Add new custom entity forms (Project Service Automation 2.x)</span></span>

## <a name="type-field"></a><span data-ttu-id="197af-104">Pole Typ</span><span class="sxs-lookup"><span data-stu-id="197af-104">Type field</span></span> 

<span data-ttu-id="197af-105">Program Dynamics 365 Project Service Automation wykorzystuje pole **Typ** ( **msdyn\_ordertype** ) w encjach Szansa sprzedaży, Oferta, Zamówienie i Faktury do rozróżniania między wersjami tych encji **opartymi na pracy** , **opartymi na towarach** i **opartymi na usługach**.</span><span class="sxs-lookup"><span data-stu-id="197af-105">Dynamics 365 Project Service Automation relies on the **Type** ( **msdyn\_ordertype** ) field of the Opportunity, Quote, Order, and Invoice entities to distinguish **work-based** versions of these entities from **item-based** and **service-based** versions.</span></span> <span data-ttu-id="197af-106">Wersje tych encji oparte na pracy są zarządzane przez program PSA.</span><span class="sxs-lookup"><span data-stu-id="197af-106">Work-based versions of these entities are handled by PSA.</span></span> <span data-ttu-id="197af-107">Od pola **Typ** zależy wiele aspektów logiki biznesowej po stronach klienta i serwera rozwiązania.</span><span class="sxs-lookup"><span data-stu-id="197af-107">Lots of business logic on the client side and server side of the solution depends on the **Type** field.</span></span> <span data-ttu-id="197af-108">Dlatego ważne jest, aby podczas tworzenia encji pole było inicjowane z poprawną wartością.</span><span class="sxs-lookup"><span data-stu-id="197af-108">Therefore, it's important that the field be initialized with a correct value when the entities are created.</span></span> <span data-ttu-id="197af-109">Niepoprawna wartość może spowodować nieprawidłowe zachowanie, a część logiki biznesowej może nie działać poprawnie.</span><span class="sxs-lookup"><span data-stu-id="197af-109">An incorrect value can cause incorrect behaviors, and some business logic might not run correctly.</span></span>

## <a name="automatic-form-switching"></a><span data-ttu-id="197af-110">Automatyczne przełączanie formularzy</span><span class="sxs-lookup"><span data-stu-id="197af-110">Automatic form switching</span></span>

<span data-ttu-id="197af-111">Aby uniknąć potencjalnego uszkodzenia danych i nieoczekiwanych zachowań spowodowanych niepoprawną inicjalizacją i zmodyfikowaniem rekordów encji sprzedaży, program PSA zawiera teraz logikę automatycznego przełączania gotowych formularzy.</span><span class="sxs-lookup"><span data-stu-id="197af-111">To avoid potential data corruption and unexpected behaviors that are caused by incorrect initialization and editing of the sales entity records, PSA now includes logic for automatic form switching in out-of-box forms.</span></span> <span data-ttu-id="197af-112">Logika powoduje przeniesienie użytkownika do formularza odpowiedniego do pracy z wersją opartą na pracy lub z dowolnym innym typem encji Szansa sprzedaży, Oferta, Zamówienie lub Faktura.</span><span class="sxs-lookup"><span data-stu-id="197af-112">This logic takes users to the correct form for working with the work-based version or any other type of Opportunity, Quote, Order, or Invoice entity.</span></span> <span data-ttu-id="197af-113">Kiedy użytkownik otworzy wersję encji Szansa sprzedaży, Oferta, Zamówienie lub Faktura opartą na pracy, formularz jest przełączany na **Informacje o projekcie**.</span><span class="sxs-lookup"><span data-stu-id="197af-113">When a user opens the work-based version of an Opportunity, Quote, Order, or Invoice entity, the form is switched to **Project Information**.</span></span>

<span data-ttu-id="197af-114">Logika automatycznego przełączania formularzy wykorzystuje mapowanie między wartością **formId** a polem **msdyn\_ordertype**.</span><span class="sxs-lookup"><span data-stu-id="197af-114">The automatic form switching logic relies on the mapping between the **formId** value and the **msdyn\_ordertype** field.</span></span> <span data-ttu-id="197af-115">Wszystkie gotowe formularze są dodane do tego mapowania.</span><span class="sxs-lookup"><span data-stu-id="197af-115">All out-of-box forms have been added to that mapping.</span></span> <span data-ttu-id="197af-116">Natomiast formularze niestandardowe należy dodać ręcznie, aby wskazać, którą wersję encji mają obsługiwać.</span><span class="sxs-lookup"><span data-stu-id="197af-116">However, custom forms must be manually added to indicate which version of the entity they are intended to handle.</span></span> <span data-ttu-id="197af-117">Zależy to od pola **msdyn\_ordertype**.</span><span class="sxs-lookup"><span data-stu-id="197af-117">This is based on the **msdyn\_ordertype** field.</span></span> <span data-ttu-id="197af-118">Jeśli opcji przełączania formularzy nie ma w mapowaniu, logika przełączy na gotowy formularz na podstawie wartości zapisanej w polu **msdyn\_ordertype** w encji.</span><span class="sxs-lookup"><span data-stu-id="197af-118">If the form switching is missing from the mapping, logic will switch to the out-of-box form, based on the value that is saved in the **msdyn\_ordertype** field of the entity.</span></span>

## <a name="add-custom-forms-and-turn-on-the-form-switching-logic"></a><span data-ttu-id="197af-119">Dodawanie niestandardowych formularzy i włączanie logiki przełączania formularzy</span><span class="sxs-lookup"><span data-stu-id="197af-119">Add custom forms and turn on the form switching logic</span></span>

<span data-ttu-id="197af-120">W poniższym przykładzie pokazano, jak dodać niestandardowy formularz **Moje informacje o projekcie** przeznaczony dla szans sprzedaży opartych na pracy.</span><span class="sxs-lookup"><span data-stu-id="197af-120">The following example shows how to add a custom form, **My Project Information** , so that it works with work-based opportunities.</span></span> <span data-ttu-id="197af-121">Ten sam proces służy do dodawania niestandardowych formularzy dla ofert, zamówień i faktur.</span><span class="sxs-lookup"><span data-stu-id="197af-121">The same process is used to add custom forms so that they work with quotes, orders, and invoices.</span></span>

<span data-ttu-id="197af-122">Wykonaj te kroki, aby utworzyć niestandardową wersję formularza **Informacje o projekcie**.</span><span class="sxs-lookup"><span data-stu-id="197af-122">Follow these steps to create a custom version of the **Project Information** form.</span></span>

1. <span data-ttu-id="197af-123">W encji Szansa sprzedaży otwórz formularz **Informacje o projekcie** i zapisz jego kopię pod nazwą **Moje informacje o projekcie**.</span><span class="sxs-lookup"><span data-stu-id="197af-123">In the Opportunity entity, open the **Project Information** form, and save a copy under the name **My Project Information**.</span></span>
2. <span data-ttu-id="197af-124">Otwórz nowy formularz, a następnie w oknie właściwości sprawdź, czy są obecne skrypty inicjowania formularza pochodzące z formularza **Informacje o projekcie**.</span><span class="sxs-lookup"><span data-stu-id="197af-124">Open the new form, and then, in the properties, make sure that the form initialization scripts from the **Project Information** form are present.</span></span> 

    > [!IMPORTANT]
    > <span data-ttu-id="197af-125">Nie należy usuwać skryptów.</span><span class="sxs-lookup"><span data-stu-id="197af-125">Don't remove the scripts.</span></span> <span data-ttu-id="197af-126">W przeciwnym razie niektóre dane mogą być niepoprawnie inicjowane.</span><span class="sxs-lookup"><span data-stu-id="197af-126">Otherwise, some data might be initialized incorrectly.</span></span>

3. <span data-ttu-id="197af-127">Sprawdź, czy w formularzu jest obecne pole **Typ** ( **msdyn\_ordertype** ).</span><span class="sxs-lookup"><span data-stu-id="197af-127">Verify that the **Type** ( **msdyn\_ordertype** ) field is present in the form.</span></span> 

    > [!IMPORTANT]
    > <span data-ttu-id="197af-128">Nie należy usuwać tego pola.</span><span class="sxs-lookup"><span data-stu-id="197af-128">Don't remove this field.</span></span> <span data-ttu-id="197af-129">W przeciwnym razie skrypty inicjalizacji nie zadziałają.</span><span class="sxs-lookup"><span data-stu-id="197af-129">Otherwise, the initialization scripts will fail.</span></span>

4. <span data-ttu-id="197af-130">Znajdź wartość **formId** dotyczącą nowego formularza.</span><span class="sxs-lookup"><span data-stu-id="197af-130">Find the **formId** value of the new form.</span></span> <span data-ttu-id="197af-131">Ten krok można wykonać na dwa sposoby:</span><span class="sxs-lookup"><span data-stu-id="197af-131">You can complete this step in two ways:</span></span>

    - <span data-ttu-id="197af-132">Wyeksportuj formularz **Moje informacje o projekcie** jako część niezarządzanego rozwiązania, a następnie poszukaj wartości **formId** w pliku customization.xml wyeksportowanego rozwiązania.</span><span class="sxs-lookup"><span data-stu-id="197af-132">Export the **My Project Information** form as part of an unmanaged solution, and then look up the **formId** value in the customization.xml file of the exported solution.</span></span>
    - <span data-ttu-id="197af-133">Otwórz formularz **Moje informacje o projekcie** w edytorze formularzy, a następnie wyszukaj unikatowy identyfikator globalny (GUID) obok parametru **fromId** w adresie URL, jak przedstawiono na poniższym rysunku.</span><span class="sxs-lookup"><span data-stu-id="197af-133">Open the **My Project Information** form in the form editor, and then look for the globally unique identifier (GUID) next to the **fromId** parameter in the URL, as shown in the following illustration.</span></span>

    ![Wartość formId nowego formularza w adresie URL](media/how-to-add-custom-forms-in-v2.0.png)

5. <span data-ttu-id="197af-135">Utwórz mapowanie pola **msdyn\_ordertype** dla wartości **formId** , odpowiednio modyfikując zasób internetowy msdyn\_/SalesDocument/PSSalesDocumentCustomFormIds.js.</span><span class="sxs-lookup"><span data-stu-id="197af-135">Create an **msdyn\_ordertype** mapping for the **formId** value by editing the msdyn\_/SalesDocument/PSSalesDocumentCustomFormIds.js web resource.</span></span> <span data-ttu-id="197af-136">Usuń kod z zasobu i zastąp go następującym kodem.</span><span class="sxs-lookup"><span data-stu-id="197af-136">Remove the code from the resource, and replace it with the following code.</span></span>

    ```javascript
    define(["require", "exports"], function (require, exports) {
        "use strict";
        var SalesDocumentCustomFormIds = (function () {
            function SalesDocumentCustomFormIds() {
            }
            SalesDocumentCustomFormIds.overwriteFormIds = function (mappedFormIds) {
                /*
                ---- Notes ----
                mappedFormIds[SalesEntity][OrderType] => The array of forms IDs that support particular entity and order type
                Add or overwrite customized formId for the particular entity and order type by calling:
                    mappedFormIds[<EntityType>][<msdyn_ordertype>].push("<formId>");
                Allowed msdyn_ordertype values for reference:
                    ServiceBased: 690970002 (Field Service version of the entity)
                    WorkBased: 192350001 (PSA version of the entity)
                    ItemBased: 192350000 (Regular out of the box entity)
                Uncomment and update one of the following lines to register custom PSA form for required entity:
                */      
                //mappedFormIds[1][192350001].push("<formId>"); //Quote
                //mappedFormIds[5][192350001].push("<formId>"); //Quote Line
                //mappedFormIds[2][192350001].push("<formId>"); //Sales Order
                //mappedFormIds[6][192350001].push("<formId>"); //Sales Order Line
                // In this example we have added new form for Opportunity
                mappedFormIds[0][192350001].push("192EE537-DCC4-45D3-B7AF-EA694B9113D2"); //Opportunity
                //mappedFormIds[4][192350001].push("<formId>"); //Opportunity Line
            };
            return SalesDocumentCustomFormIds;
        }());
        exports.default = SalesDocumentCustomFormIds;
    });
    ```

6. <span data-ttu-id="197af-137">Zapisz i opublikuj dostosowania.</span><span class="sxs-lookup"><span data-stu-id="197af-137">Save and then publish the customizations.</span></span>
