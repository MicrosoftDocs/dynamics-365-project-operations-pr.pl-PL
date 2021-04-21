---
title: Nowości i zmiany w aplikacji Project Service Automation, wydanie 30, wer. 3
description: W tym temacie przedstawiono funkcje i poprawki, które są dostepne w programie Project Service Automation, aktualizacja 30, wer. 3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 04/01/2021
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
ms.openlocfilehash: 1169ee13c42e982cb30a40d92df660f8933786a9
ms.sourcegitcommit: b4a05c7d5512d60abdb0d05bedd390e288e8adc9
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/02/2021
ms.locfileid: "5852881"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-30-v3"></a>Nowości i zmiany w aplikacji Project Service Automation, wydanie 30, wer. 3

[!include [banner](../includes/psa-now-project-operations.md)]

Mamy przyjemność ogłosić najnowszą aktualizację aplikacji Project Service Automation dla Dynamics 365. To wydanie obejmuje znaczną poprawę jakości, wydajności i użyteczności. To wydanie jest zgodne z systemem Dynamics 365 9.x. Aby zaktualizować do tej wersji, odwiedź centrum administracyjne Dynamics 365 online i przejdź na stronę rozwiązań, aby zainstalować aktualizację. By uzyskać więcej informacji, zobacz [Instalowanie, aktualizowanie lub usuwanie preferowanego rozwiązania](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

W tym temacie przedstawiono funkcje i poprawki, które są nowe lub zostały zmienione w programie Project Service Automation, wer. 3, aktualizacja 30. Ta wersja ma numer kompilacji V3.10.51.61 i zazwyczaj jest dostępna za pośrednictwem samoaktualizacji w kwietniu 2021 r.

## <a name="update-release-30"></a>Wydanie 30

### <a name="bug-fixes"></a>Poprawki błędów

**Czas i wydatek**

Rozwiązano następujące problemy:

- Podczas tworzenia i zapisywania pozycji czasu na stronie **Szybkie tworzenie**, jeśli pole **Rola** zostanie usunięte, występuje błąd.
- Filtr Time Entry powoduje zastosowanie niewłaściwego operatora filtru.
- Kopiowane czasokopi nie są automatycznie wyświetlane po wybraniu opcji **Kopiuj tydzień** w kontrolce wpisu godziny.

**Zarządzanie zasobami**

Rozwiązano następujące problemy:

- Gdy przedłużasz rezerwację, status rezerwacji przypisany do twardej rezerwacji jest nieprawidłowy. Rozszerzenie rezerwacji obejmuje stan rezerwacji zdefiniowany jako **Zatwierdzone** w metadanych konfiguracji rezerwacji.
- Jeśli nie zostanie określony prawidłowy stan rezerwacji, komunikat o błędzie nie jest poprawnie zlokalizowany.

**Zarządzanie projektem**

Rozwiązano następujące problemy:

- Nie można tworzyć projektów w jednej walucie i zawierać zadań pokrewnych w innej walucie.

**Sprzedaż**

Rozwiązano następujące problemy:

- Podczas kopiowania cennika ceny nie są aktualizowane.
- Zamknięcie oferty jako wygranej kończy się niepowodzeniem, gdy szczegóły kosztu mają wartość pochodzenia.
- W encji **Zadanie projektu** nazwa **Szacowanego kosztu** została zmieniona na **Planowany koszt (podstawowy)**.
- Wyjątek zerowego odwołania jest generowany podczas tworzenia lub usuwania faktur.
