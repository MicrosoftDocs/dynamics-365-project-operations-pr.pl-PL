---
title: Potwierdzenie faktur od dostawcy projektu
description: W tym artykule wyjaśniono, jak w Microsoft Dynamics 365 Project Operations potwierdzić fakturę dostawcy projektu oraz wpływ finansowy potwierdzenia faktury dostawcy projektu.
author: suvaidya
ms.date: 8/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: suvaidya
ms.openlocfilehash: 9739b15753aa34c51a0aa1e6dfeb7f590655ca7a
ms.sourcegitcommit: 60a34a00e2237b377c6f777612cebcd6380b05e1
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 09/13/2022
ms.locfileid: "9475449"
---
# <a name="confirm-project-vendor-invoices"></a>Potwierdzenie faktur od dostawcy projektu

**Zastosowane do:** Project Operations dla zasobów/scenariuszy nieopartych na zaopatrzeniu

Po włączeniu parametru **Ręczne potwierdzenie przez pm jest wymagane** faktury dostawcy utworzone w momencie ich utworzenia w Microsoft Dataverse mają stan **Wersja robocza**. Faktury dostawcy utworzone w ten sposób należy przejrzeć i ręcznie potwierdzić. Po wyłączeniu parametru **Ręczne potwierdzenie przez pm jest wymagane** faktury dostawcy utworzone w momencie ich utworzenia w Dataverse są automatycznie potwierdzane. Wykonywanie dalszych akcji nie jest wymagane. 

Po sprawdzeniu wszystkich wierszy na fakturze dostawcy w Dynamics 365 Project Operations, wybierz **Potwierdź**, aby potwierdzić fakturę dostawcy.

Po wybraniu opcji **Potwierdź** na fakturze dostawcy występuje następujące zachowanie:

1. Stan faktury dostawcy zostanie zaktualizowany do **Potwierdzony**.
1. Potwierdzona faktura dostawcy i związane z nią rekordy staje się dostępna tylko do odczytu i nie można jej edytować ani usunąć.
1. Jeśli jakiś koszt rzeczywisty odwołuje się do wiersza faktury dostawcy w ramach procesu dopasowywania, wszystkie wartości rzeczywiste kosztów skojarzone z linią faktury dostawcy, do których odwołuje się odwołanie, są cofane.
1. Nowe wartości rzeczywiste kosztów są tworzone na podstawie informacji z wiersza faktury dostawcy.
1. Nie można już tworzyć poprawek, przetwarzać anulowań wpisów czasu ani anulować zatwierdzania pierwotnego czasu, wydatku lub wartości rzeczywistych materiałów, które zostały wycofane.
1. W programie Dynamics 365 Finance wartość **Koszt projektu** jest aktualizowana przy użyciu narzędzia Integracja projektu, a konto integracji Zaopatrzenie jest *cofane* po zaksięgowaniu wpisu integracji projektu.

> [!NOTE]
> Jeśli stan weryfikacji dowolnego wiersza na fakturze dostawcy jest inny niż **Ukończony**, nie można potwierdzić faktury dostawcy.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
