---
title: Nowości i zmiany w aplikacji Project Service Automation, wydanie 17, wer. 3
description: W tym temacie przedstawiono funkcje i poprawki, które są dostepne w programie Project Service Automation, aktualizacja 17, wer. 3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 03/06/2020
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
ms.openlocfilehash: 364a64e0ea501ac5b7faaf254c7af3648cfe1f9b
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 05/10/2021
ms.locfileid: "6006704"
---
# <a name="project-service-automation-update-release-17-v3"></a>Project Service Automation, wydanie 17, wer. 3

[!include [banner](../includes/psa-now-project-operations.md)]

Mamy przyjemność ogłosić najnowszą aktualizację aplikacji Project Service Automation dla Dynamics 365. To wydanie obejmuje znaczną poprawę jakości, wydajności i użyteczności.  To wydanie jest zgodne z systemem Dynamics 365 9.x. Aby zaktualizować do tej wersji, odwiedź Centrum administracyjne Dynamics 365 online i przejdź na stronę rozwiązań, aby zainstalować aktualizację. By uzyskać więcej informacji, zobacz [Instalowanie, aktualizowanie lub usuwanie preferowanego rozwiązania](/power-platform/admin/install-remove-preferred-solution).

W tym temacie przedstawiono funkcje i poprawki, które są nowe lub zostały zmienione w programie PSA, wer. 3, aktualizacja 17. Numer tej kompilacji to V3.10.6.34 i jest on zazwyczaj dostępny za pośrednictwem samoaktualizacji w marcu 2020 r.


## <a name="update-release-17"></a>Wydanie 17

### <a name="bug-fixes"></a>Poprawki błędów

**Ogólne**

- Naprawione: aktualizowanie rozwiązania Project Service Automation w celu wdrożenia licencji dla Członków zespołu (centrum Project Resource będzie obejmował plan Usługi dla Człownków zespołu 3.x)
 
**Czas i wydatki**

- Naprawione: Nie jest możliwe zmodyfikowanie oszacowania kosztów z ceną wyższą niż zero na zero (0). Zmiana została zignorowana.

**Zarządzanie projektem**

- Naprawione: sprawdzanie wartości null zostało dodane względem nazwy pozycji członka zespołu.
- Naprawione: pole **msdyn_userresourceid** w encji **msdyn_resourceassignment** jest przestarzałe.
- Naprawione: Uaktualnianie z 2.x do wersji 3.x obsługuje teraz puste zarysy nakładów pracy dla przydziałów zadań.

**Sales**

- Naprawione: **Invoice.PreValidateInvoiceUpdate** teraz poprawnie obsługuje scenariusz ponownego przypisania właścicieli rekordów.
- Naprawione: Kiedy klasa transakcji to **Czas** **UnitGroup** nie można edytować dla wszystkich encji, w tym **QuoteLineDetails**, **JournalLine**, **InvoiceLineDetail** i **ContractLineDetails**. **Jednostka** nie jest jednak edytowana wyłącznie dla **JournalLine** i **InvoiceLineDetails**.




[!INCLUDE[footer-include](../includes/footer-banner.md)]