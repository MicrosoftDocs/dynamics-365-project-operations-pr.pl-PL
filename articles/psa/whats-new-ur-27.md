---
title: Nowości i zmiany w Project Service Automation, wydanie aktualizacji 27, wer. 3
description: W tym temacie wymieniono funkcje i poprawki, które są dostępne w aktualizacji Project Service Automation, wydanie 27, wersja 3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 01/12/2021
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
ms.openlocfilehash: 6b9da3ec54ec10408774945d26db9e702c858d05
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/10/2021
ms.locfileid: "5146676"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-27-v3"></a>Nowości i zmiany w Project Service Automation, wydanie aktualizacji 27, wer. 3

[!include [banner](../includes/psa-now-project-operations.md)]

Mamy przyjemność ogłosić najnowszą aktualizację aplikacji Project Service Automation dla Dynamics 365. To wydanie obejmuje znaczną poprawę jakości, wydajności i użyteczności. To wydanie jest zgodne z systemem Dynamics 365 9.x. Aby zaktualizować do tej wersji, odwiedź centrum administracyjne Dynamics 365 online i przejdź na stronę rozwiązań, aby zainstalować aktualizację. By uzyskać więcej informacji, zobacz [Instalowanie, aktualizowanie lub usuwanie preferowanego rozwiązania](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

W tym temacie wymieniono funkcje i poprawki, które są nowe lub zmienione w programie Project Service Automation V3, aktualizacja wydanie 27. Numer tej kompilacji to V3.10.45.98 i jest on zazwyczaj dostępny za pośrednictwem samoaktualizacji w styczniu 2021 r.

## <a name="update-release-27"></a>Wydanie 27

### <a name="bug-fixes"></a>Poprawki błędów

**Ogólne**

Rozwiązano następujące problemy:

- Dzienniki generowane przez wtyczki w Project Service Automation nie zostały ustawione na automatyczne usuwanie.
- Automatyczne uaktualnianie kończy się niepowodzeniem, ponieważ rozwiązanie Project Service Automation zawiera starszą wartość null NavBarArea i element tytułu.

**Czas i wydatek**

Rozwiązano następujące problemy:

- W siatce **Wpis czasu** są wyświetlane nieprawidłowe dane dla zachowania daty **Niezależna od strefy czasowej**.
- W siatce **Wpis czasu** wytwarza nieprawidłowe godziny dla zachowania daty **Niezależna od strefy czasowej**.
- Wyszukiwania zadań nie są ograniczone do wybranego projektu na stronie **Edytowanie wpisu czasu**.
- Zatwierdzanie czasu dla wpisów czasu niezwiązanych z projektem jest blokowane, ponieważ system szuka osoby zatwierdzającej projekt.
- Prawidłowe wpisy w danych rzeczywistych powodują wyświetlenie nieprawidłowego komunikatu o błędzie.
- Gdy zadanie zawiera wartość null dla kosztu rzeczywistego, a sumy projektu są odświeżane, pojawia się następujący błąd: „Podanego klucza nie ma w słowniku”.
- W określonych przypadkach filtry **Grupuj według** na karcie **Szacowanie projektu** nie wyświetlają szacowania wydatków.
- Interwał **Czasu letniego** jest błędnie poprawny w przypadku wpisów czasu.

**Zarządzanie projektem**

Rozwiązano następujące problemy:

- Udoskonalenia buforowania, które zwiększają wydajność związaną z ładowaniem strony **Projekt**.
- Przestarzała reguła biznesowa uniemożliwiająca wykonanie zadań projektowych.
- Kontury dodatku Microsoft Project nie są zgodne z kalendarzem dodatku, co powoduje nieprawidłowe wymagania dotyczące zasobów.
- Tworzenie projektów z szablonów powoduje nieprawidłowe ustawienie dat przydziałów i uniemożliwia generowanie wymagań dotyczących zasobów.
- Użytkownik nie może uzyskać dostępu do opcji **Kategoria**, **Opis** i **Stan** za pomocą klawiatury.
- Rzeczywiste wartości sprzedaży projektu nie obejmują wartości sprzedaży opłat i materiałów.
- Agregacja rzeczywistej sprzedaży i rzeczywistego kosztu jest nieprawidłowa przy różnych kursach wymiany.
- Opis w **Domyślny szablon godzin pracy** jest mylący.
- Wcięcie zadania nie powoduje usunięcia **Kategorii** w interfejsie użytkownika, dopóki nie zostanie odświeżony.
- Brak weryfikacji zapewniającej przeniesienie projektu poza jego datę zakończenia jest niedozwolony.

**Sales**

Rozwiązano następujące problemy:

- Wyjątek odniesienia zerowego jest generowany w wierszu oferty projektu, ponieważ **Importuj z szacowania projektu** jest widoczny, gdy projekt nie został wybrany.
- Następujący błąd „Odwołanie do obiektu nie jest ustawione na wystąpienie obiektu” występuje podczas zamykania cudzysłowu jako **Wykorzystane**.
- Stan korekty nie jest ustawiany podczas rzeczywistego wycofania podczas odłączania projektu od wiersza umowy.
- Gdy są zainstalowane zarówno Dynamics 365 Field Service, jak i Project Service Automation, opcje **Zablokuj ceny** i **Użyj aktualnej ceny** nie są wyświetlane w tym samym czasie na stronie **Faktura**.
- W przypadku języka japońskiego istnieje niespójne tłumaczenie z innymi stronami opartymi na kalendarzu.
- **Uaktywnij** i **Dezaktywuj** zostały usunięte z encji **Skojarzenie cennika** w Project Service Automation.
