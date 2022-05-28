---
title: Dodawanie nowych niestandardowych formularzy encji (Project Service Automation wer. 2.x)
description: W tym temacie przedstawiono informacje na temat dodawania niestandardowych formularzy encji szans sprzedaży, ofert, zamówień lub faktur w programie Dynamics 365 Project Service Automation w wersji 2.x.
author: makk
ms.custom:
- dyn365-projectservice
ms.date: 3/14/2019
ms.topic: article
ms.author: makk
audience: admin
search.audienceType:
- admin
- customizer
search.app:
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: ffc702bbe9cedb2a0cc8da8d8f58e48005950127
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/14/2022
ms.locfileid: "8584333"
---
# <a name="add-new-custom-entity-forms-project-service-automation-2x"></a>Dodawanie nowych niestandardowych formularzy encji (Project Service Automation wer. 2.x)

[!include [banner](../../includes/psa-now-project-operations.md)]

## <a name="type-field"></a>Pole Typ 

Program Dynamics 365 Project Service Automation wykorzystuje pole **Typ** (**msdyn\_ordertype**) w encjach Szansa sprzedaży, Oferta, Zamówienie i Faktury do rozróżniania między wersjami tych encji **opartymi na pracy**, **opartymi na towarach** i **opartymi na usługach**. Wersje tych encji oparte na pracy są zarządzane przez program PSA. Od pola **Typ** zależy wiele aspektów logiki biznesowej po stronach klienta i serwera rozwiązania. Dlatego ważne jest, aby podczas tworzenia encji pole było inicjowane z poprawną wartością. Niepoprawna wartość może spowodować nieprawidłowe zachowanie, a część logiki biznesowej może nie działać poprawnie.

## <a name="automatic-form-switching"></a>Automatyczne przełączanie formularzy

Aby uniknąć potencjalnego uszkodzenia danych i nieoczekiwanych zachowań spowodowanych niepoprawną inicjalizacją i zmodyfikowaniem rekordów encji sprzedaży, program PSA zawiera teraz logikę automatycznego przełączania gotowych formularzy. Logika powoduje przeniesienie użytkownika do formularza odpowiedniego do pracy z wersją opartą na pracy lub z dowolnym innym typem encji Szansa sprzedaży, Oferta, Zamówienie lub Faktura. Kiedy użytkownik otworzy wersję encji Szansa sprzedaży, Oferta, Zamówienie lub Faktura opartą na pracy, formularz jest przełączany na **Informacje o projekcie**.

Logika automatycznego przełączania formularzy wykorzystuje mapowanie między wartością **formId** a polem **msdyn\_ordertype**. Wszystkie gotowe formularze są dodane do tego mapowania. Natomiast formularze niestandardowe należy dodać ręcznie, aby wskazać, którą wersję encji mają obsługiwać. Zależy to od pola **msdyn\_ordertype**. Jeśli opcji przełączania formularzy nie ma w mapowaniu, logika przełączy na gotowy formularz na podstawie wartości zapisanej w polu **msdyn\_ordertype** w encji.

## <a name="add-custom-forms-and-turn-on-the-form-switching-logic"></a>Dodawanie niestandardowych formularzy i włączanie logiki przełączania formularzy

W poniższym przykładzie pokazano, jak dodać niestandardowy formularz **Moje informacje o projekcie** przeznaczony dla szans sprzedaży opartych na pracy. Ten sam proces służy do dodawania niestandardowych formularzy dla ofert, zamówień i faktur.

Wykonaj te kroki, aby utworzyć niestandardową wersję formularza **Informacje o projekcie**.

1. W encji Szansa sprzedaży otwórz formularz **Informacje o projekcie** i zapisz jego kopię pod nazwą **Moje informacje o projekcie**.
2. Otwórz nowy formularz, a następnie w oknie właściwości sprawdź, czy są obecne skrypty inicjowania formularza pochodzące z formularza **Informacje o projekcie**. 

    > [!IMPORTANT]
    > Nie należy usuwać skryptów. W przeciwnym razie niektóre dane mogą być niepoprawnie inicjowane.

3. Sprawdź, czy w formularzu jest obecne pole **Typ** (**msdyn\_ordertype**). 

    > [!IMPORTANT]
    > Nie należy usuwać tego pola. W przeciwnym razie skrypty inicjalizacji nie zadziałają.

4. Znajdź wartość **formId** dotyczącą nowego formularza. Ten krok można wykonać na dwa sposoby:

    - Wyeksportuj formularz **Moje informacje o projekcie** jako część niezarządzanego rozwiązania, a następnie poszukaj wartości **formId** w pliku customization.xml wyeksportowanego rozwiązania.
    - Otwórz formularz **Moje informacje o projekcie** w edytorze formularzy, a następnie wyszukaj unikatowy identyfikator globalny (GUID) obok parametru **fromId** w adresie URL, jak przedstawiono na poniższym rysunku.

    ![Wartość formId nowego formularza w adresie URL.](media/how-to-add-custom-forms-in-v2.0.png)

5. Utwórz mapowanie pola **msdyn\_ordertype** dla wartości **formId**, odpowiednio modyfikując zasób internetowy msdyn\_/SalesDocument/PSSalesDocumentCustomFormIds.js. Usuń kod z zasobu i zastąp go następującym kodem.

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

6. Zapisz i opublikuj dostosowania.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
