---
title: Waluta
description: W tym temat zamieszczono informacje dotyczące sposobu dodawania i usuwania typów waluty w Project Operations.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 093eaa78b5f88aee364a753374a56c33e20a5ce3
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 11/25/2020
ms.locfileid: "4642286"
---
# <a name="currency"></a>Waluta

_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

W walutach wyrażane są ceny produktów w katalogu produktów oraz koszty transakcji, takich jak zamówienia sprzedaży. Jeśli klienci znajdują się w różnych lokalizacjach geograficznych, dodaj ich waluty, aby zarządzać transakcjami. Dodaj waluty, które są najbardziej odpowiednie dla Twoich bieżących i przyszłych potrzeb biznesowych.  

> [!NOTE]
> Jeśli Twoje środowisko to środowisko Common Data Service, znajdujesz się w centrum administracyjnym Power Platform i wybierasz stronę **Waluty** (**Środowiska** > [wybierz środowisko] > **Ustawienia** > **Biznes** > **Waluty**), strona będzie pusta. Dzieje się tak, ponieważ ustawianie waluty nie jest obsługiwane w środowiskach usługi Common Data Service.

## <a name="add-a-currency"></a>Dodawanie waluty  
Przed przystąpieniem do rozpoczęcia tej procedury należy sprawdzić, czy Twoja rola zabezpieczeń zawiera uprawnienia administratora systemu. 

1. W Centrum administracyjnym Power Platform wybierz środowisko. 
2. Wybierz **Ustawienia** > **Biznesowe**.
3. Wybierz **Waluty**.  
4. Wybierz **Nowy**.  
5. Wprowadź wymagane informacje.  


   |          Pole          |                                                                                                                                                                                                                                                                                                                                                                            Opis                                                                                                                                                                                                                                                                                                                                                                            |
   |-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
   |    **Typ waluty**    | - **System** - Wybierz tę opcję, jeśli chcesz użyć walut dostępnych w aplikacjach opartych na modelach w usłudze Dynamics 365. Wybierz przycisk **Wyszukaj**, aby wyszukać walutę. Po wybraniu kodu waluty, **Nazwa waluty** i **Symbol waluty** są automatycznie dodawane dla wybranej waluty.<br />- **Niestandardowa** - Wybierz tę opcję, jeśli chcesz dodać walutę, która nie jest dostępna w aplikacjach opartych na modelach w usłudze Dynamics 365. W takim przypadku musisz ręcznie wprowadzić wartości dla **Kod waluty**, **Dokładność waluty**, **Nazwa waluty**, **Symbol waluty**, i **Konwersja waluty**. |
   |    **Kod waluty**    |                                                                                                                                                                                                                                                                                                                                            Forma krótka dla waluty. Na przykład **USD** dla dolara amaerykańskiego.                                                                                                                                                                                                                                                                                                                                            |
   | **Dokładność waluty**  |                                                                                                                                                                                  Podaj liczbę miejsc dziesiętnych wyświetlanych dla waluty.  Można dodać wartość z przedziału od 0 do 4. **Uwaga:**  Jeśli ustawiono wartość precyzji w oknie dialogowym **Ustawienia systemu**, wartość ta pojawi się tutaj.                                                                                                                                                                                  |
   |    **Nazwa waluty**    |                                                                                                                                                                                                                                         Jeśli wybrano kod waluty z listy dostępnych walut w aplikacjach opartych na modelach w usłudze Dynamics 365, w tym polu będzie wyświetlana nazwa waluty dla wybranego kodu. W przypadku wybrania **Niestandardowy** jako typ waluty, wpisz nazwę waluty.                                                                                                                                                                                                                                          |
   |   **Symbol waluty**   |                                                                                                                                                                                                                                                                      Jeśli wybrano kod waluty z listy dostępnych walut w tym polu będzie wyświetlany symbol wybranej waluty. W przypadku wybrania **Niestandardowy** jako typ waluty, wprowadź symbol nowej waluty.                                                                                                                                                                                                                                                                       |
   | **Konwersja walut** |                                                                                                                                                                                                                                     Wpisz wartość wybranej waluty w stosunku do dolara amerykańskiego. Jest to kwota, dla której wybrana waluta jest konwertowana do waluty podstawowej. **Ważne:**  Upewnij się, że aktualizujesz tę wartość odpowiednio często, aby uniknąć nieprawidłowych obliczeń w transakcjach.                                                                                                                                                                                                                                      |


6. Po zakończeniu na pasku poleceń wybierz **Zapisz** lub **Zapisz i zamknij**.  

   > [!TIP]
   >  Aby edytować waluty, wybierz walutę i wprowadź lub wybierz nowe wartości.  

## <a name="delete-a-currency"></a>Usuń walutę  

1. W Centrum administracyjnym Power Platform wybierz środowisko. 
2. Wybierz **Ustawienia** > **Biznesowe**.
3. Wybierz **Waluty**.  
4. Z listy walut wybierz walutę do usunięcia.  
5. Wybierz **Usuń**.  
6. Potwierdź usunięcie.  

> [!IMPORTANT]
>  Nie możesz usunąć walut używanych przez inne rekordy, możesz je jedynie dezaktywować. Dezaktywowanie rekordów walutowych nie powoduje usunięcia informacji o walutach przechowywanych w istniejących rekordach, takich jak szanse sprzedaży czy zamówienia. Jednakże nie będziesz mógł wybrać dezaktywowanej waluty dla nowych transakcji.  


[!INCLUDE[footer-include](../includes/footer-banner.md)]