---
title: Potwierdź fakturę od dostawcy projektu
description: W temat wyjaśniono, jak w Microsoft Dynamics 365 Project Operations potwierdzić fakturę dostawcy projektu oraz wpływ finansowy potwierdzenia faktury dostawcy projektu.
author: rumant
ms.date: 03/30/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: c248b3baec6d3f14a020e4fa93f3dad50c65b263
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/14/2022
ms.locfileid: "8595741"
---
# <a name="confirm-a-project-vendor-invoice"></a>Potwierdź fakturę od dostawcy projektu

[!include [banner](../../includes/dataverse-preview.md)]

_**Zastosowane w:** Wdrażanie uproszczone — od okazji do faktury pro forma_

Po sprawdzeniu wszystkich wierszy na fakturze dostawcy w programie Microsoft Dynamics 365 Project Operations można użyć akcji Potwierdź, aby potwierdzić fakturę dostawcy.

Po wybraniu opcji **Potwierdź** na fakturze dostawcy występuje następujące zachowanie:

1. Stan faktury dostawcy zostanie zaktualizowany do **Potwierdzony**.
2. Potwierdzona faktura dostawcy i związane z nią rekordy staje się dostępna tylko do odczytu i nie można jej edytować ani usunąć.
3. Jeśli jakiś koszt rzeczywisty odwołuje się do wiersza faktury dostawcy w ramach procesu dopasowywania, wszystkie wartości rzeczywiste kosztów skojarzone z linią faktury dostawcy, do których odwołuje się odwołanie, są cofane.
4. Nowe wartości rzeczywiste kosztów są tworzone na podstawie informacji z wiersza faktury dostawcy.
5. Po zatwierdzeniu faktury dostawcy nie można już tworzyć poprawek, wprowadzania godzin procesów ani anulować zatwierdzania pierwotnego czasu, wydatku lub wartości rzeczywistych materiałów, które zostały wycofane.

> [!NOTE]
> Jeśli stan weryfikacji dowolnego wiersza na fakturze dostawcy jest inny niż **Ukończony**, nie można potwierdzić faktury dostawcy.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
