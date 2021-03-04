---
title: Nowości i zmiany w aplikacji Project Service Automation, wydanie 24, wer. 3
description: W tym temacie przedstawiono funkcje i poprawki, które są dostępne w programie Project Service Automation, aktualizacja 24, wer. 3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 10/02/2020
ms.topic: article
ms.author: stsporen
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 15fe1c3482de66331dd543ee73391638919b2595
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/10/2021
ms.locfileid: "5146721"
---
# <a name="project-service-automation-update-release-24-v3"></a>Project Service Automation, wydanie 24, wer. 3

[!include [banner](../includes/psa-now-project-operations.md)]

Mamy przyjemność ogłosić najnowszą aktualizację aplikacji Project Service Automation dla Dynamics 365. To wydanie obejmuje znaczną poprawę jakości, wydajności i użyteczności. To wydanie jest zgodne z systemem Dynamics 365 9.x. Aby zaktualizować do tej wersji, odwiedź centrum administracyjne Dynamics 365 online i przejdź na stronę rozwiązań, aby zainstalować aktualizację. By uzyskać więcej informacji, zobacz [Instalowanie, aktualizowanie lub usuwanie preferowanego rozwiązania](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

W tym temacie przedstawiono funkcje i poprawki, które są nowe lub zostały zmienione w programie Project Service Automation, wer. 3, aktualizacja 24. Numer tej kompilacji to V3.10.42.43 i jest on zazwyczaj dostępny za pośrednictwem samoaktualizacji w październiku 2020 r.

## <a name="update-release-24"></a>Wydanie 24

### <a name="bug-fixes"></a>Poprawki błędów

**Sales**

Rozwiązano następujące problemy:

- Wystąpił problem podczas ustawiania domyślnego cennika produktów.
- Wydajność licytacji jest niska z powodu osadzonych cenników i kopii rekordów cen ról.
- **Kontrakt projektu/Centrum sprzedaży** > **Pozycja wiersza produktu/Ilość wiersza zamówienia** jest automatycznie zaokrąglana do najbliższej liczby całkowitej.
- Podnieś uprawnienia do uprawnień systemowych podczas odczytywania cenników.
- Kopiuj pola adresu klienta **address1_freighttermscode** i **address1_shippingmethodcode** do oferty/zamówienia. 


**Czas i wydatek**

Rozwiązano następujące problemy:

- **Siatka wprowadzania godzin** nie obsługuje zachowania czasowego **Tylko data**.
- **Wpis czasu** nie jest odświeżany automatycznie. Wymagane jest ręczne odświeżenie.
- Nie można zaimportować wpisów czasu z przypisania, jeśli w przypisaniach zasobu występuje przerwa (0 godzin).
- Podczas tworzenia wpisu czasu ustaw początek na taki sam, jak **msdyn_date**.
- Ponownie włącz edycję zbiorczą dla wpisu czasu.

**Zarządzanie zasobami**

Rozwiązano następujące problemy:

- Próba zaktualizowania stanu rezerwacji międzydniowej bez wymagania spowoduje zgłoszenie wyjątku odwołania o wartości null.
- Wystąpił błąd podczas ładowania **Widoku uzgadniania**.


**Zarządzanie projektem**

Rozwiązano następujące problemy:

- W **Harmonogramie projektu** podczas zmiany z **Ręczne** na **Automatyczne** nie jest dokonywane automatyczne zapisywanie.
- Koszty wydatków nie powinny być obliczane względem wariancji w **Siatce śledzenia projektu**.
- Niespójne zachowanie dotyczące kolumn **Tag oszacować** podczas ładowania i zmiany typu **Fazy czasu**.
- Koszt rzeczywisty w projekcie może nie odzwierciedlać sum w **Wartościach rzeczywistych**.
- **Szacowana data zakończenia** na karcie **Podsumowanie** nie jest zgodna z **Harmonogramem SPP**.
- **Zaktualizowanie rzeczywistych godzin** na zmniejszeniu wcięcia nie działa poprawnie.
- Menedżer projektu spoza katalogu głównego **JB** nie może utworzyć projektu.
- Zmiany w zadaniach i kategoriach w **Szacunkach wydatków** nie są trwałe.
- **Kopia kontraktu** kopiuje harmonogramy faktur oraz stanu przebiegu.
- **Przycisk odświeżanie wartości rzeczywistych** powoduje nieprawidłowe obliczenie zadań sumarycznych.
- Dodatek programu Microsoft Project: rozwiąż błąd odwołania do wartości null, jeśli dowolny członek zespołu ma pustą jednostkę ponownego pozyskania zasobów.

