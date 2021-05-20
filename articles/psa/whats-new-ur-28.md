---
title: Nowości i zmiany w aplikacji Project Service Automation, wydanie aktualizacji 28, wer. 3
description: W tym temacie wymieniono funkcje i poprawki, które są dostępne w aktualizacji Project Service Automation, wydanie 28, wersja 3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 01/26/2021
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
ms.openlocfilehash: 2d5e8c629f8108ed039948ca70842c9d8afebfa6
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/27/2021
ms.locfileid: "5948702"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-28-v3"></a>Nowości i zmiany w aplikacji Project Service Automation, wydanie aktualizacji 28, wer. 3

[!include [banner](../includes/psa-now-project-operations.md)]

Mamy przyjemność ogłosić najnowszą aktualizację aplikacji Project Service Automation dla Dynamics 365. To wydanie obejmuje znaczną poprawę jakości, wydajności i użyteczności. To wydanie jest zgodne z systemem Dynamics 365 9.x. Aby zaktualizować do tej wersji, odwiedź centrum administracyjne Dynamics 365 online i przejdź na stronę rozwiązań, aby zainstalować aktualizację. By uzyskać więcej informacji, zobacz [Instalowanie, aktualizowanie lub usuwanie preferowanego rozwiązania](/power-platform/admin/install-remove-preferred-solution).

W tym temacie wymieniono funkcje i poprawki, które są nowe lub zmienione w programie Project Service Automation V3, aktualizacja wydanie 28. Ta wersja ma numer kompilacji V3.10.46.32 i jest ogólnie dostępna po samodzielnej aktualizacji w styczniu 2021.

## <a name="update-release-28"></a>Wydanie 28

### <a name="bug-fixes"></a>Poprawki błędów

**Czas i wydatek**

Rozwiązano następujące problemy:

- Użytkownicy mogą używać **Edycji zbiorczej** do aktualizowania wpisów czasu, które zostały zatwierdzone i przesłane.

**Zarządzanie projektem**

Rozwiązano następujące problemy:

- W przypadkach, gdy identyfikator GUID zadania jest zinterpretowany jako liczba, nie można otworzyć zadań do edycji przy użyciu funkcji **Edytuj zadanie** na wstążce na stronie **Struktura podziału zadania**.

**Sales**

Rozwiązano następujące problemy:

- Wyjątek odwołania do null jest generowany, gdy jest wywoływany dodatek plug-in **GetEstimatesForProject**.
- **Oznacz jako przygotowane do fakturowania** w siatce punktów kontrolnych tylko częściowo aktualizowane atrybuty, z wyjątkiem aktualizowanego atrybutu **InvoiceStatus**.



[!INCLUDE[footer-include](../includes/footer-banner.md)]