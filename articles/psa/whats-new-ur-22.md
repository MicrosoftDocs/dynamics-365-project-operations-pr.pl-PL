---
title: Nowości i zmiany w Project Service Automation, wydanie 22, wer. 3
description: W tym temacie przedstawiono funkcje i poprawki, które są dostepne w Project Service Automation, aktualizacja 22, wer. 3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 07/28/2020
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
ms.openlocfilehash: 389897c2604974a0bf7f221758dd03e1748ffeb5
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5280591"
---
# <a name="project-service-automation-update-release-22-v3"></a>Project Service Automation, wydanie 22, wer. 3

[!include [banner](../includes/psa-now-project-operations.md)]

Mamy przyjemność ogłosić najnowszą aktualizację aplikacji Project Service Automation dla Dynamics 365. To wydanie obejmuje znaczną poprawę jakości, wydajności i użyteczności. To wydanie jest zgodne z systemem Dynamics 365 9.x. Aby zaktualizować do tej wersji, odwiedź centrum administracyjne Dynamics 365 online i przejdź na stronę rozwiązań, aby zainstalować aktualizację. By uzyskać więcej informacji, zobacz [Instalowanie, aktualizowanie lub usuwanie preferowanego rozwiązania](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

W tym temacie przedstawiono funkcje i poprawki, które są nowe lub zostały zmienione w Project Service Automation, wer. 3, aktualizacja 22. Ta wersja ma numer kompilacji wer. 3.10.33.48 i zazwyczaj jest dostępna za pośrednictwem samoaktualizacji w czerwcu 2020 r.

## <a name="update-release-22"></a>Wydanie 22

### <a name="bug-fixes"></a>Poprawki błędów



**Czas i wydatek**

Rozwiązano następujące problemy:

- **Wpisy czasu** nie są automatycznie dodawane do harmonogramu wpisów godzin po zaimportowaniu.
- Selektor dat siatki **Wpisów czasu** nie rozpoznaje ustawień regionalnych użytkownika.

**Zarządzanie zasobami**

Rozwiązano następujące problemy:

- W trybie ręcznym zmiany rozkładu **Przydziału zasobu** nie są rozpoznawane przy generowaniu **Wymagań dotyczących zasobów**.
- **Żądania zasobów** nie obsługują niestandardowych stanów żądań.

**Zarządzanie projektem**

Rozwiązano następujące problemy:

- Korzystanie z dwukrotnego kliknięcia opcji EstimateGridControl nie spowoduje zaprogramowania poprawnie analizy liczb w formacie holenderskim.
- Przypisane godziny nie są poprawnie aktualizowane, gdy przydziały są zmieniane za pomocą dodatku klienta klasycznego Microsoft Project.
- Siatki śledzenia projektu i szacowania wyświetlają niepoprawny kod waluty sprzedaży, gdy waluta umowy jest inna niż waluta klienta, a organizacja jest skonfigurowana do wyświetlania kodów walut zamiast symboli walut.
- Data zakończenia członka zespołu doda jeden dzień, jeśli harmonogram godzin pracy wynosi 24 godziny na dobę.
- W harmonogramie projektu dodanie kategorii transakcji do zadania nie powoduje uruchomienia automatycznego zapisu.
- Podczas dodawania członka zespołu do szablonu projektu wyświetlany jest następujący błąd: „Wymagania dotyczące zasobów nie mogą być powiązane z szablonami projektu”. 
- Skrypt reguły wstążki „msdyn.Approval.CanApproveOrReject” wyświetla błąd przekroczenia limitu czasu.

**Sales**

Rozwiązano następujące problemy:

- Komunikat o błędzie walidacji nie jest wyświetlany, gdy cennik kosztów jest wybrany w wyszukiwaniu cennika w formularzu / encji „Nowy cennik projektu oferty”.
- Zamknięcie oferty jako wygranej nie powoduje przejścia do utworzonego kontraktu, jeśli BPF dołączony do oferty jest na ostatnim etapie.
- Wycofanie **Niezafakturowanej sprzedaży** jest powiązane z oryginalnym kosztem po odwołaniu wpisu czasu.
- Po wybraniu przycisku **Potwierdź** status faktury nie zmieni się na **Potwierdzony**, chyba że faktura jest odświeżana.


[!INCLUDE[footer-include](../includes/footer-banner.md)]