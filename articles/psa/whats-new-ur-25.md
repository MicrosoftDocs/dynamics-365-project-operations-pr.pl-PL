---
title: Nowości i zmiany w aplikacji Project Service Automation, wydanie 25, wer. 3
description: W tym artykule przedstawiono funkcje i poprawki dostępne w programie Project Service Automation, wydanie aktualizacji 25, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 10/26/2020
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
ms.openlocfilehash: 2330c7dc5d2dfb148d5c7fb9a5ce643fded84dde
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8922557"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-25-v3"></a>Nowości i zmiany w aplikacji Project Service Automation, wydanie 25, wer. 3

[!include [banner](../includes/psa-now-project-operations.md)]

Mamy przyjemność ogłosić najnowszą aktualizację aplikacji Project Service Automation dla Dynamics 365. To wydanie obejmuje znaczną poprawę jakości, wydajności i użyteczności. To wydanie jest zgodne z systemem Dynamics 365 9.x. Aby zaktualizować do tej wersji, odwiedź centrum administracyjne Dynamics 365 online i przejdź na stronę rozwiązań, aby zainstalować aktualizację. By uzyskać więcej informacji, zobacz [Instalowanie, aktualizowanie lub usuwanie preferowanego rozwiązania](/power-platform/admin/install-remove-preferred-solution).

W tym artykule przedstawiono listę funkcji i poprawek, które zostały nowe lub zmienione w programie Project Service Automation V3, aktualizacja 25. Ta wersja ma numer kompilacji V 3.10.43.76 i jest ogólnie dostępna w ramach samoobsługowej aktualizacji w październiku 2020 r.

## <a name="update-release-25"></a>Wydanie 25

### <a name="bug-fixes"></a>Poprawki błędów

**Czas i wydatek**

Naprawiono następujący problem:

- Wykres wprowadzania czasu pokazujący dodatkowe dane na podstawie zbyt dużego zakresu pobieranych danych.

**Zarządzanie zasobami**

Naprawiono następujący problem:

- Dodano kod wdrożeniowy pakietu w celu pominięcia importu poprawki Universal Resource Scheduling, jeśli nowsza wersja poprawki już istnieje.

**Zarządzanie projektem**

Rozwiązano następujące problemy:

- Poprawiono rozbieżności w zaokrąglaniu i kursach wymiany powodujące nieprawidłowy planowany koszt w siatce śledzenia projektu.
- Umożliwia wyświetlanie w formularzu **Projektu** dwóch lub więcej siatek reagujących na zareagowanie.
- Przy sprawdzeniu poprawności zaadresowano zdolność przypisywania zadania poza datą zakończenia kalendarza, co powoduje niepowodzenie przypisania zasobu.
- Ulepszona obsługa błędów w celu wygenerowania wyjątków dotyczących odwołań null z następujących programów:

    - Dodatek plug-in **PreValidateProjectTeamMemberCreate**
    - **PreValidateProjectTaskCreate** kiedy zadanie projektu zostanie utworzone bez skojarzonego projektu
    - Dodatek plug-in **PreProjectTeamMemberCreate**
    - Dodatek plug-in **PostProjectTeamMemberDelete**
    - Dodatek plug-in **PreValidateProjectTaskDelete**

**Sales**

Rozwiązano następujące problemy:

- Ulepszona obsługa błędów w celu rozwiązania wyjątków odwołań null wygenerowanych z **Kopii projektu: szacuje zarządzanie HelperResource**.
- **Nie jest gotowy do zafakturowania** w **Rozliczeniu na czas i materiały** nie czyści stanu fakturowania.
- przyciski z błędnie etykietowanymi **Cenami** zostały poprawione na karcie **Cena roli** i **Elementy katalogu**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
