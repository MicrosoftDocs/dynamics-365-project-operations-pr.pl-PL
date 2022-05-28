---
title: Anuluj fakturę od dostawcy projektu
description: W tym temacie wyjaśniono, jak anulować fakturę od dostawcy projektu w programie Microsoft Dynamics 365 Project Operations oraz jaki wpływ finansowy ma anulowanie faktury od dostawcy projektu.
author: rumant
ms.date: 03/30/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 87f6bdca30c5779e3d70922e75609ff4cdfca167
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/14/2022
ms.locfileid: "8580653"
---
# <a name="cancel-a-project-vendor-invoice"></a>Anuluj fakturę od dostawcy projektu

[!include [banner](../../includes/dataverse-preview.md)]

_**Zastosowane w:** Wdrażanie uproszczone — od okazji do faktury pro forma_

Po potwierdzenie faktury dostawcy nie można jej edytować ani usunąć. Jeśli wystąpił błąd na fakturze dostawcy, która została potwierdzina, można użyć akcji Anuluj, aby odwrócić wpływ faktury dostawcy i utworzyć nową fakturę od dostawcy.

Po wybraniu opcji **Anuluj** na fakturze dostawcy występuje następujące zachowanie:

1. Stan faktury dostawcy zostanie zaktualizowany do **Anulowane**.
2. Anulowana faktura od dostawcy i powiązane z nią rekordy stają się tylko do odczytu i nie można ich edytować ani usuwać.
3. Wszelkie wartości rzeczywiste kosztów utworzone na podstawie wierszy faktur dostawcy w ramach potwierdzenia faktury dostawcy są cofane.
4. Jeśli w ramach procesu dopasowywania wartości rzeczywiste kosztów zostały połączone z wierszami faktur dostawcy, pierwotne potwierdzenie faktury dostawcy wycofało je. Podczas anulowania faktury od dostawcy te wartości rzeczywiste kosztów są ponownie tworzone. Pochodzenia wskazują czas, koszt lub wpisy użycia materiałów.
5. Po anulowaniu faktury od dostawcy można ponownie utworzyć arkusze korekt, wycofania wprowadzania czasu przetwarzania i anulować zatwierdzenie oryginalnego czasu, wydatków lub rzeczywistych danych materiałowych.

> [!NOTE]
> Tylko potwierdzone faktury od dostawcy projektu mogą zostać anulowane. Faktur od dostawcy w innych stanach nie można anulować.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
