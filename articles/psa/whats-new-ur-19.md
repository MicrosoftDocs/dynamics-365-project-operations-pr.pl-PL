---
title: Nowości i zmiany w aplikacji Project Service Automation, wydanie 19, wer. 3
description: W tym temacie przedstawiono funkcje i poprawki, które są dostępne w programie Project Service Automation, aktualizacja 19, wer. 3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 05/05/2020
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
ms.openlocfilehash: ad61589125e42e8dceb462290f65ddc05e171bd828d26d34ebd548ca285e9aa4
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/06/2021
ms.locfileid: "6993659"
---
# <a name="project-service-automation-update-release-19-v3"></a>Project Service Automation, wydanie 19, wer. 3

[!include [banner](../includes/psa-now-project-operations.md)]

Mamy przyjemność ogłosić najnowszą aktualizację aplikacji Project Service Automation dla Dynamics 365. To wydanie obejmuje znaczną poprawę jakości, wydajności i użyteczności. To wydanie jest zgodne z systemem Dynamics 365 9.x. Aby zaktualizować do tej wersji, odwiedź centrum administracyjne Dynamics 365 online i przejdź na stronę rozwiązań, aby zainstalować aktualizację. By uzyskać więcej informacji, zobacz [Instalowanie, aktualizowanie lub usuwanie preferowanego rozwiązania](/power-platform/admin/install-remove-preferred-solution).

W tym temacie przedstawiono funkcje i poprawki, które są nowe lub zostały zmienione w programie PSA, wer. 3, aktualizacja 19. Ta wersja ma numer kompilacji wer. 3.10.30.41 i zazwyczaj jest dostępna za pośrednictwem samoaktualizacji w maju 2020 r.

## <a name="update-release-19"></a>Wydanie 19

### <a name="bug-fixes"></a>Poprawki błędów

**Czas i wydatek**

Rozwiązano następujące problemy: 

- Błędy pochodzące z importu wpisów godzin nie są poprawnie opisane.
- Siatka wprowadzania czasu nie obsługuje zachowania pola **Tylko data**.
- Zasoby projektu nie mogą utworzyć wydatku dla projektu.

**Zarządzanie projektem**

Rozwiązano następujące problemy: 

-  Zadanie podrzędne powoduje nieprawidłowe szacowanie kosztów przy zakończeniu (EAC).

**Sales**

Rozwiązano następujące problemy: 

- Akcja **Oblicz ponownie** nie działa ze szczegółami pozycji kontraktu wydatków lub informacjami o wierszach oferty.
- Brak **Cen aktualizacji** dla szacowań wydatków.
-  Klienci nie mogą wybierać niestandardowych przyczyn stanu kontraktu na stronie **Kontrakt projektu**.
- Klienci doświadczają spadku wydajności podczas tworzenia cennika niestandardowego na podstawie oferty.
- Klienci doświadczają niespójności z domyślnymi **jednostkami** dotyczącymi stron **Szczegółów wiersza oferty** i **Szczegółów pozycji kontraktu**.
- Dodanie pozycji kategorii niepłatnych transakcji do płatnej pozycji kontraktu nie będzie brać pod uwagę **Niepłatnego** rozliczeniowego typu kategorii transakcji.
- Klienci nie mogą korzystać z nowo dodanych ról i kategorii w poprzednio utworzonych kontraktach.
- Klienci doświadczają spadku wydajności podczas niepotrzebnego pobierania w PreValidateProjectTeamMemberUpdate.cs
- Role skonfigurowane jako niepłatne na liście **Kategorie zasobów** powinny zostać dodane do karty **Role płatne** jako **Niepłatne** w pozycji kontraktu projektu.
- Podczas tworzenia projektu klienci mogą doświadczyć spadku wydajności, ponieważ **GetBookableResourceIdFromUser** pobiera wszystkie kolumny zasobów możliwych do zarezerwowania, a nie tylko podstawowy identyfikator.
- W encji **TransactionType** brak dodatku wstępnej weryfikacji aktualizacji, aby zapobiec wprowadzaniu przez użytkowników **jednostek** i **UnitGroups**, które są nieprawidłowe dla typów transakcji.
- Krok **Usuń** nie działa w przypadku importowania wpisów czasu.


[!INCLUDE[footer-include](../includes/footer-banner.md)]