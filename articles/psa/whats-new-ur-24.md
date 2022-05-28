---
title: Nowości i zmiany w aplikacji Project Service Automation, wydanie 24, wer. 3
description: W tym temacie przedstawiono funkcje i poprawki, które są dostępne w programie Project Service Automation, aktualizacja 24, wer. 3.
author: ruhercul
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
ms.reviewer: johnmichalak
ms.openlocfilehash: 63bf96bfeed30ceefab072640172a6a0dafd20f5
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/14/2022
ms.locfileid: "8581573"
---
# <a name="project-service-automation-update-release-24-v3"></a>Project Service Automation, wydanie 24, wer. 3

[!include [banner](../includes/psa-now-project-operations.md)]

Mamy przyjemność ogłosić najnowszą aktualizację aplikacji Project Service Automation dla Dynamics 365. To wydanie obejmuje znaczną poprawę jakości, wydajności i użyteczności. To wydanie jest zgodne z systemem Dynamics 365 9.x. Aby zaktualizować do tej wersji, odwiedź centrum administracyjne Dynamics 365 online i przejdź na stronę rozwiązań, aby zainstalować aktualizację. By uzyskać więcej informacji, zobacz [Instalowanie, aktualizowanie lub usuwanie preferowanego rozwiązania](/power-platform/admin/install-remove-preferred-solution).

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



[!INCLUDE[footer-include](../includes/footer-banner.md)]
