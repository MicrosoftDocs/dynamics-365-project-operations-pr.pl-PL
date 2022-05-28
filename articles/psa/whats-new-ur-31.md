---
title: Nowości i zmiany w aplikacji Project Service Automation, wydanie 31, wer. 3
description: W tym temacie przedstawiono funkcje i poprawki, które są dostepne w programie Project Service Automation, aktualizacja 31, wer. 3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 04/26/2021
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
ms.openlocfilehash: 70a8bd381c27c9a3dd3b33c582e5616fad280e95
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/14/2022
ms.locfileid: "8586771"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-31-v3"></a>Nowości i zmiany w aplikacji Project Service Automation, wydanie 31, wer. 3

[!include [banner](../includes/psa-now-project-operations.md)]

Mamy przyjemność ogłosić najnowszą aktualizację aplikacji Project Service Automation dla Dynamics 365. To wydanie obejmuje znaczną poprawę jakości, wydajności i użyteczności. To wydanie jest zgodne z systemem Dynamics 365 9.x. Aby zaktualizować do tej wersji, odwiedź centrum administracyjne Dynamics 365 online i przejdź na stronę rozwiązań, aby zainstalować aktualizację. By uzyskać więcej informacji, zobacz [Instalowanie, aktualizowanie lub usuwanie preferowanego rozwiązania](/power-platform/admin/install-remove-preferred-solution).

W tym temacie przedstawiono funkcje i poprawki, które są nowe lub zostały zmienione w programie Project Service Automation, wer. 3, aktualizacja 31. Ta wersja ma numer kompilacji wer. 3.10.52.77 i zazwyczaj jest dostępna za pośrednictwem samoaktualizacji w maju 2021 r.

## <a name="update-release-31"></a>Wydanie 31

### <a name="bug-fixes"></a>Poprawki błędów

**Czas i wydatek**

Rozwiązano następujące problemy:

- Przyciski poleceń formantu wprowadzania czasu na stronie **Zasoby do zarezerwowania** nie były mylące.
- Podczas zatwierdzania wpisu czasowego w **Project.SetTrackingFields** generowany był wyjątek null reference.

**Zarządzanie zasobami**

Rozwiązano następujące problemy:

- **Utwórz członka zespołu** nie wyświetla poprawnie ustawienia metadanych ustawień rezerwacji dla **Domyślnego statusu rezerwacji zaangażowanej**.
- W przypadku uaktualnienia z wersji PSA 1.X do 3.X proces uaktualniania kończy się niepowodzeniem: **UpgradeResourceRequirements**.


**Sprzedaż**

Rozwiązano następujące problemy:

- Przychód rzeczywisty konwertuje kwoty na walutę projektu w siatce śledzenia.
- Domyślna waluta jest niejasna podczas tworzenia wierszy dziennika, wierszy wyceny i wierszy umowy w scenariuszach, w których waluta podstawowa organizacji różni się od waluty projektu.
- **Oczekiwanie na korektę weryfikacji dziennika** — zapytanie nie jest filtrowane według projektu.
- Pozostała sprzedaż jest obliczana niepoprawnie w projekcie.
- Oferty oparte na kontakcie nie są tworzone bez cennika.
- Po wybraniu opcji **Potwierdź fakturę** nie jest wyświetlana ikona przetwarzania.
- Po wybraniu opcji **Utwórz fakturę** nie jest wyświetlana ikona przetwarzania.
- Zamknięcie oferty jako utraconej nie anulowało rezerwacji.







