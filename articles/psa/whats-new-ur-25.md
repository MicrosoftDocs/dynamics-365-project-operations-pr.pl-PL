---
title: Nowości i zmiany w aplikacji Project Service Automation, wydanie 25, wer. 3
description: W tym temacie przedstawiono funkcje i poprawki, które są dostepne w programie Project Service Automation, wydanie 25, wer. 3.
author: ruhercul
manager: kfend
ms.service: project-operations
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
ms.openlocfilehash: a5a81893c4a804deb09cf33e0ac3f1a25b8bca36
ms.sourcegitcommit: a2b810219d381716d3eedb14c4eb6cdefb5b5845
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 11/02/2020
ms.locfileid: "4183556"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-25-v3"></a>Nowości i zmiany w aplikacji Project Service Automation, wydanie 25, wer. 3

Mamy przyjemność ogłosić najnowszą aktualizację aplikacji Project Service Automation dla Dynamics 365. To wydanie obejmuje znaczną poprawę jakości, wydajności i użyteczności. To wydanie jest zgodne z systemem Dynamics 365 9.x. Aby zaktualizować do tej wersji, odwiedź centrum administracyjne Dynamics 365 online i przejdź na stronę rozwiązań, aby zainstalować aktualizację. By uzyskać więcej informacji, zobacz [Instalowanie, aktualizowanie lub usuwanie preferowanego rozwiązania](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

W tym temacie wymieniono funkcje i poprawki, które są nowe lub zmienione w programie Project Service Automation V3, aktualizacja wydanie 25. Ta wersja ma numer kompilacji 3.10.43.76 i jest ogólnie dostępna po samodzielnej aktualizacji w październiku 2020 r.

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
