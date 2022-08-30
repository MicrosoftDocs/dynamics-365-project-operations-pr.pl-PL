---
title: Potwierdź fakturę od dostawcy projektu
description: W tym artykule wyjaśniono, jak w Microsoft Dynamics 365 Project Operations potwierdzić fakturę dostawcy projektu oraz wpływ finansowy potwierdzenia faktury dostawcy projektu.
author: rumant
ms.date: 03/30/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 4dafbe64e0727957068d68f510202a12871b62aa
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261526"
---
# <a name="confirm-a-project-vendor-invoice"></a>Potwierdź fakturę od dostawcy projektu

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
