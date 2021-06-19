---
title: Nowości i zmiany w aplikacji Project Service Automation, wydanie 32, wer. 3
description: W tym temacie przedstawiono funkcje i poprawki, które są dostepne w programie Project Service Automation, aktualizacja 32, wer. 3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 06/01/2021
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
ms.openlocfilehash: 11bf451ef4f24e2301ffde4f86a556a8a4fe30b0
ms.sourcegitcommit: 886102894244887d72e5a6213071e8d8a52c9d48
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 06/01/2021
ms.locfileid: "6129679"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-32-v3"></a>Nowości i zmiany w aplikacji Project Service Automation, wydanie 32, wer. 3

[!include [banner](../includes/psa-now-project-operations.md)]

Z zadowoleniem informujemy, że jest to najnowsza aktualizacja aplikacji Microsoft Dynamics 365 Project Service Automation. To wydanie obejmuje znaczną poprawę jakości, wydajności i użyteczności. Jest ona kompatybilna z Dynamics 365 9.x. Aby dokonać aktualizacji do tego wydania, należy odwiedzić stronę Centrum administracyjnego dla rozwiązań Dynamics 365 online i zainstalować aktualizację. By uzyskać więcej informacji, zobacz [Instalowanie, aktualizowanie lub usuwanie preferowanego rozwiązania](/power-platform/admin/install-remove-preferred-solution).

W tym temacie przedstawiono funkcje i poprawki, które są nowe lub zostały zmienione w programie Project Service Automation, wer. 3, aktualizacja 32. Ta wersja ma numer kompilacji wer. 3.10.53.108 i zazwyczaj jest dostępna za pośrednictwem samoaktualizacji w czerwcu 2021 r.

## <a name="update-release-32"></a>Wydanie 32

### <a name="bug-fixes"></a>Poprawki błędów

#### <a name="general"></a>Ogólne

- W przypadku niepowodzenia poważnej aktualizacji należy zablokować tylko główne punkty wejścia do aplikacji, aby zapewnić, że współdzielone elementy są nadal dostępne.

#### <a name="time-and-expense"></a>Czas i wydatek

Rozwiązano następujące problemy:

- **TimeEntriesImportFromResourceAssignment** nie zachowuje czasu rozpoczęcia i zakończenia wycinka konturu przydziału zasobów.
- Wybór opcji **Otwórz wpis** w siatce **wprowadzania czasu** może uniemożliwić wybranie innych formularzy.
- Podczas importowania zadań do wpisów czasu, zapytanie o kod klienta może wygenerować długi adres URL, który nie powiedzie się w zapytaniu.
- Po usunięciu wartości z komórki w **siatce czasu** fokus nie pozostaje w siatce.
- Przycisk **Odrzucanie** został usunięty z widoku **Przetwarzanie zatwierdzeń** dla nowych zatwierdzeń.
- Na stabilność i wydajność zbiorczego zatwierdzania wpisów czasu pracy mają wpływ martwe punkty i brak odpowiedniej obsługi dostosowań, które są związane z podmiotem **Wpis czasu**.

#### <a name="project-planning"></a>Planowanie projektu

- Podczas aktualizacji projektu, który ma wartość null w polu **Jednostka kontraktująca**, generowany jest wyjątek odwołania do wartości null.
- **Odświeżenie sumy projektu** w niepoprawny sposób oblicza pozostały koszt i pozostałą sprzedaż w projekcie.
- Nadmiarowe obliczenia cenowe wpływają na wydajność związaną z aktualizacjami konturów przydziału zasobów.

#### <a name="resource-management"></a>Zarządzanie zasobami

Naprawiono następujący problem:

- Gdy pojemność kalendarza zasobu, który można zarezerwować jest większa niż 1, Project Service Automation błędnie rozpoznaje pojemność jako 0 (zero). Dlatego w widoku harmonogramu pojawia się nieskończona pętla.

#### <a name="sales"></a>Sprzedaż

Rozwiązano następujące problemy:

- Gdy tworzona jest linia dziennika z niestandardowym typem transakcji, występuje następujący wyjątek null reference: *Microsoft.Dynamics.ProjectService.Plugins.JournalLinePlugins.ValidateUnitScheduleAndUnitWithTransactionType(TransactionTypetransactionType, TransactionTypeCode transTypeCodeFromPlugin)*.
- Role i kategorie, które zostały dezaktywowane przed skopiowaniem oferty nie powinny być dodawane do ról i kategorii płatnych w nowo skopiowanej ofercie.
- Data dokumentu i data księgowania nie są zgodne z datą początkową, która jest podawana na elemencie linii faktury, który jest tworzony bezpośrednio na projekcie faktury.
- Wyjątki typu null reference generowane są w scenariuszach związanych z dezaktywacją ról i kategorii przed skopiowaniem oferty.
- W akcji **Aktualizowanie cen** na stronie **Projekty** nie są aktualizowane szacowania wydatków i szacowania materiałowe.
