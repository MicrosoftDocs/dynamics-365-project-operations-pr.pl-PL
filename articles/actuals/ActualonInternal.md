---
title: Rzeczywisty wpływ na projekt wewnętrzny
description: Ten temat zawiera informacje o wpływie na tabelę Rzeczywiste na różne zdarzenia dla projektu wewnętrznego w Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 02/22/2022
ms.topic: overview
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.assetid: ''
ms.search.region: ''
ms.search.industry: ''
ms.author: rumant
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 66a9ac4d2f56ae95313ed6731c3e51926105cff7
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/14/2022
ms.locfileid: "8579779"
---
# <a name="actuals-impact-for-an-internal-project"></a>Rzeczywisty wpływ na projekt wewnętrzny

_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_

W poniższej tabeli wymieniono dane rzeczywiste różnych typów transakcji, które są tworzone podczas różnych wydarzeń w ramach wewnętrznego zaangażowania projektowego.

| Wydarzenie | Wartość rzeczywista kosztu | Przykład |
|---|---|---|
| Czas jest stworzony. | Nie dotyczy | <p>Bob Kozack z jednostki organizacyjnej Fabrikam US ze stawką kosztów 100 USD (100 USD) na godzinę pracuje nad projektem o nazwie „Instalacja ramienia w Adatum”. Ten projekt jest mapowany na metodę rozliczania stałej ceny w ramach wiersza kontraktu. Oto przykładowy wpis dotyczący czasu od Boba Kozaka:</p><p>Bob Kozack — 8 godzin</p> |
| Czas jest zgłoszony. | Nie dotyczy | W przypadku wprowadzenia czasu jest tworzona pozycja kosztów. Domyślny koszt jest wprowadzany w wpisie daty. |
| Wpis godziny jest przechowany przed zatwierdzonego. | Nie dotyczy | |
| Czas jest zatwierdzony. | Tworzony jest koszt. | <p>Nowe wartości rzeczywiste, które są tworzone:</p><ul><li>**Koszt rzeczywisty:** Bob Kozack, 8 godzin, 800 USD</li></ul> |
| Zatwierdzenie czasu jest anulowane. | <p>Stan korekty oryginalnego kosztu jest aktualizowany do wartości **Skorygowano**.</p><p>Tworzony jest koszt ponownego kosztu, który ma stan **Nieskorygowano**.</p> | <p>Istniejące wartości rzeczywiste, które zostały zaktualizowane:</p><ul><li>**Koszt rzeczywisty**: Bob Kozack, 8 godzin, 800 USD *Skorygowano*</li></ul><p>Nowa wartość rzeczywista tworzona w celu odwrócenia poprzedniego wpływu finansowego:</p><ul><li>**Koszt rzeczywisty**: Bob Kozack, (8 godzin), (800 USD), *Nieskorygowano*</li></ul> |
| Wpis czasu jest przywoływany po zatwierdzeniu. | <p>Stan korekty oryginalnego kosztu jest aktualizowany do wartości **Skorygowano**.</p><p>Tworzony jest koszt ponownego kosztu, który ma stan **Nieskorygowano**.</p> | <p>Istniejące wartości rzeczywiste, które zostały zaktualizowane:</p><ul><li>**Koszt rzeczywisty**: Bob Kozack, 8 godzin, 800 USD *Skorygowano*</li></ul><p>Nowa wartość rzeczywista tworzona w celu odwrócenia poprzedniego wpływu finansowego:</p><ul><li>**Koszt rzeczywisty**: Bob Kozack, (8 godzin), (800 USD), *Nieskorygowano*</li></ul> |

[!INCLUDE[footer-include](../includes/footer-banner.md)]
