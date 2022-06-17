---
title: Nowości i zmiany w Project Service Automation, wydanie 21, wer. 3
description: W tym artykule przedstawiono funkcje i poprawki dostępne w programie Project Service Automation, wydanie aktualizacji 21, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 06/19/2020
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
ms.openlocfilehash: 7d7c098a4572aa4f5730ffdbdab77b2897cdfeff
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8918831"
---
# <a name="project-service-automation-update-release-21-v3"></a>Project Service Automation, wydanie 21, wer. 3

[!include [banner](../includes/psa-now-project-operations.md)]

Mamy przyjemność ogłosić najnowszą aktualizację aplikacji Project Service Automation dla Dynamics 365. To wydanie obejmuje znaczną poprawę jakości, wydajności i użyteczności. To wydanie jest zgodne z systemem Dynamics 365 9.x. Aby zaktualizować do tej wersji, odwiedź centrum administracyjne Dynamics 365 online i przejdź na stronę rozwiązań, aby zainstalować aktualizację. By uzyskać więcej informacji, zobacz [Instalowanie, aktualizowanie lub usuwanie preferowanego rozwiązania](/power-platform/admin/install-remove-preferred-solution).

W tym artykule przedstawiono funkcje i poprawki, które są nowe lub zostały zmienione w programie Project Service Automation V3, wydanie aktualizacji 21. Ta wersja ma numer kompilacji wer. 3.10.32.50 i zazwyczaj jest dostępna za pośrednictwem samoaktualizacji w czerwcu 2020 r.

## <a name="update-release-21"></a>Wydanie 21

### <a name="bug-fixes"></a>Poprawki błędów

**Czas i wydatek**

Rozwiązano następujące problemy:

- Podczas obsługi **Kontrolki siatki wpisu czasu** w pulpitach nawigacyjnych siatka nie używa pełnej szerokości kontenera siatki pulpitu nawigacyjnego.
- W przypadku określonych stref czasowych kontrolka siatki **Wpisu czasu** nie wyświetla rekordów.
- Wpisy czasu o godzinie 9:00 są wyświetlane w złym dniu.
- Użytkownicy nie są w stanie przesłać kosztów, jeśli kategoria wydatku, **Wymagany paragon wydatków** nie zawiera wartości.

**Zarządzanie zasobami**

Rozwiązano następujące problemy:

- Nieaktywne rezerwacje są wyświetlane w widoku **Uzgodnienie**.
- Podczas sprawdzania poprawności zasobu rodzajowego nie jest sprawdzana wartość, aby mieć pewność, że istnieje prawidłowy stan rezerwacji.

**Zarządzanie projektem**

Rozwiązano następujące problemy:

- Siatki formularzy **Projektu** (**Przydział zasobów**, **Zadanie**, widok **Uzgodnienie**, **Oszacowania kosztów**) można edytować nawet wtedy, gdy projekt nie jest aktywny.
- Nie można łączyć duplikatów klientów z klientami, którzy są połączeni z potwierdzonymi kontraktami projektu.
- Gdy dodawany jest zasób niezawierający prawidłowego kalendarza, system nie zwraca przyjaznego użytkownika komunikatu o błędzie.
- Przycisk **Dodaj zadanie** w siatce zadań jest włączony, jeśli projekt jest połączony z **dodatkiem Microsoft Project**.
- Coraz więcej nakład pracy zwiększa się w momencie, gdy zadanie z kategorią jest przypisywane do zasobu z rolą, dla której zdefiniowano cenę kosztową.

**Sales**

Wprowadzono następujące ulepszenia:

- **Częstotliwość fakturowania** i **Rozpoczęcie fakturowania** zostały przeniesione na kartę **Harmonogram faktur**.

Rozwiązano następujące problemy:

- **Łączna cena sprzedaży** wynosi zero (0) dla **Kategorii**, mimo że dana **Rola** ma całkowitą cenę sprzedaży nie równą zero.
- Klienci nie mogą zmieniać wartości pola **Status faktury** w celu **Gotowe do fakturowania**, kiedy inny dostosowany proces aktualizuje pole dodatkowe.
- Przycisk **Odśwież wiersze faktury** może spowodować utworzenie wielu zduplikowanych wierszy, jeśli jest ciągle zaznaczonych.
- Przycisk **Aktualizuj ceny** nie działa w przypadku podsiatki **Ceny ról** w formularzu **Szybki podgląd**.
- Logika **Rozpoznawania cennika sprzedaży** nieprawidłowo obsługuje strefy czasowe, co powoduje nieprawidłowe wybór cenników.
- **Łączny koszt rzeczywisty** projektu może być wyłączony o kwotę ułamkową po zaakceptowaniu jednego wpisu czasowego.
- Logika **Rozwiązywania cen** nie zawiera przyjaznych dla użytkownika komunikatów o błędach, jeśli **Pobieranie Ceny Ról** nie ma wartości w polach **„Jednostka podstawowa”** i **„Cena w jednostce podstawowej”**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
