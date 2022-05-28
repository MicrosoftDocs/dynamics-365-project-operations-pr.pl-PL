---
title: Nowości i zmiany w aplikacji Project Service Automation, wydanie 23, wer. 3
description: W tym temacie przedstawiono funkcje i poprawki, które są dostępne w programie Project Service Automation, aktualizacja 23, wer. 3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 08/25/2020
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
ms.openlocfilehash: cc918f1516d4751b3f8e70a93d8fc66058201f22
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/14/2022
ms.locfileid: "8581619"
---
# <a name="project-service-automation-update-release-23-v3"></a>Project Service Automation, wydanie 23, wer. 3

[!include [banner](../includes/psa-now-project-operations.md)]

Mamy przyjemność ogłosić najnowszą aktualizację aplikacji Project Service Automation dla Dynamics 365. To wydanie obejmuje znaczną poprawę jakości, wydajności i użyteczności. To wydanie jest zgodne z systemem Dynamics 365 9.x. Aby zaktualizować do tej wersji, odwiedź centrum administracyjne Dynamics 365 online i przejdź na stronę rozwiązań, aby zainstalować aktualizację. By uzyskać więcej informacji, zobacz [Instalowanie, aktualizowanie lub usuwanie preferowanego rozwiązania](/power-platform/admin/install-remove-preferred-solution).

W tym temacie przedstawiono funkcje i poprawki, które są nowe lub zostały zmienione w programie Project Service Automation, wer. 3, aktualizacja 23. Numer tej kompilacji to V3.10.34.30 i jest on zazwyczaj dostępny za pośrednictwem samoaktualizacji w sierpniu 2020 r.

## <a name="update-release-23"></a>Wydanie 23

### <a name="bug-fixes"></a>Poprawki błędów

**Czas i wydatek**

Rozwiązano następujące problemy:
- Obsługa przypadków krawędzi w programie **Usuwanie członka zespołu projektu** w celu utworzenia zrozumiałego wyjątku.
- W wyniku importu przydziałów jest pusty ekran usuwania.

**Zarządzanie zasobami**

Rozwiązano następujące problemy:

- **Karta zasobu siatki wykorzystania zasobów** zawiera nieprawidłowe dane, gdy skala czasu jest dłuższa niż pięć dni.
- Kiedy klienci tworzą zasób z możliwością rezerwacji, dodatek nie może automatycznie dodać zasobu do grupy Microsoft Office 365.
- W widoku **Uzgadnianie** nieprawidłowo wyświetlane są ręczne rozkłady w widoku **Tydzień** lub **Miesiąc**.

**Zarządzanie projektem**

Rozwiązano następujące problemy:

- Zbyt duża liczba jednostek **retrievemultiple dla usersettings** powoduje spadek wydajności zatwierdzania projektów i innych operacji.
- Wyszukiwanie zasobu w siatce **Planowania zadań** jest ograniczone, aby było widocznych tylko pięciu członków zespołu z zespołu projektu. 
- Funkcja **wyszukiwania zasobów** w siatce planowania zadań nie filtruje zasobów nieaktywnych.
- Tryb ręczny nie działa zgodnie z oczekiwaniami w strukturze podziału pracy planowania projektu.
- W siatce **Planowania zadań** są wyświetlane **Nieaktywne kategorie transakcji**.
- Siatka **Przypisania zasobu** jest zaokrąglana nieprawidłowo, gdy zadanie ma wiele przypisań.
- Wartości zaokrąglania są różne między kosztem planowanym i kosztem rzeczywistym jednego zadania.

**Sales**

Rozwiązano następujące problemy:

- Dwukrotne kliknięcie **Pobierania wszystkich kategorii transakcji** powoduje utworzenie wielu wierszy.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
