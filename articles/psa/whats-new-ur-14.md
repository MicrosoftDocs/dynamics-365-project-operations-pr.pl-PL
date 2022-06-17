---
title: Nowości i zmiany w aplikacji Project Service Automation, wydanie 14, wer. 3
description: W tym artykule przedstawiono informacje na temat nowości w wydaniu aktualizacji programu Project Service Automation 14 V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 01/29/2020
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
ms.reviewer: johnmichalak
ms.openlocfilehash: e8e5132f970e3ec5742842175c118faf98a7b079
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8926559"
---
# <a name="project-service-automation-update-release-14-v3"></a>Project Service Automation, wydanie 14, wer. 3

[!include [banner](../includes/psa-now-project-operations.md)]

Mamy przyjemność przedstawić najnowszą aktualizację dotyczącą aplikacji Dynamics 365 Project Service Automation (PSA). To wydanie obejmuje znaczną poprawę jakości, wydajności i użyteczności. To wydanie jest zgodne z systemem Dynamics 365 9.x. Aby zaktualizować do tej wersji, odwiedź Centrum administracyjne programu Dynamics 365 online i przejdź na stronę rozwiązań, aby zainstalować aktualizację. By uzyskać więcej informacji, zobacz [Instalowanie, aktualizowanie lub usuwanie preferowanego rozwiązania](/power-platform/admin/install-remove-preferred-solution).

W tym artykule przedstawiono funkcje i poprawki, które są nowe lub zostały zmienione w programie PSA V3, wydanie aktualizacji 14. Numer tej kompilacji to 3.10.4.21 i jest on dostępny w następującym harmonogramie:

- **Powszechne udostępnienie (samoaktualizacja):** styczeń 2020
- **Automatyczna aktualizacja:** luty 2020

## <a name="update-release-14"></a>Wydanie 14

### <a name="enhancements"></a>Ulepszenia

- Sales

     - Wartości pól niestandardowych z **Szczegóły wiersza oferty** są kopiowane do **Szczegóły wiersza kontraktu projektu** podczas aktualizowania oferty do **Zamknięta jako wykorzystana**.
     - Potwierdzone projekty można **Zamknąć jako utracone**.

- Zarządzanie zasobami

     - Podczas rozszerzania rezerwacji użytkownicy będą proszeni o potwierdzenie, aby podsumować wyniki rezerwacji i podać łącze do obsługi rezerwacji.


### <a name="bug-fixes"></a>Poprawki błędów

- Czas i wydatek

     - Poprawione: udoskonalony sposób pracy użytkownika, jeśli użytkownik nie wybrał żadnych wpisów do skorygowania.

- Zarządzanie zasobami

     - Stałe: wielokrotna rezerwacja zasobu przepełnia nazwę rezerwowanego zasobu.

- Sales

     - Ustalone: Łączna cena sprzedaży nie jest obliczana, dopóki użytkownik nie wprowadzi kosztu własnego dla oszacowania kosztów projektu.
     - Naprawione: zamknięcie oferty jako **wykorzystanej** kończy się niepowodzeniem, jeśli skojarzony kontrakt dotyczący projektu nie znajduje się w stanie **roboczym**.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
