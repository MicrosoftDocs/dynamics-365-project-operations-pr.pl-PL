---
title: Wartość rzeczywista ma wpływ na etapie przed sprzedażą zobowiązania
description: To artykuł zawiera informacje o wpływie na tabelę wartości rzeczywistych przy różnych zdarzeniach, podczas gdy zamówienie znajduje się na etapie przedsprzedaży w Microsoft Dynamics 365 Project Operations.
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
ms.openlocfilehash: d03d6ac2154806189d0d9d0b232bb317f51071ba
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8922373"
---
# <a name="actuals-impact-during-the-pre-sales-stage-of-an-engagement"></a>Wartość rzeczywista ma wpływ na etapie przed sprzedażą zobowiązania

_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_

W poniższej tabeli przedstawiono wartości rzeczywiste różnych typów transakcji tworzone podczas różnych zdarzeń na etapie przedsprzedaażowym zobowiązania w ramach projektu.

| Wydarzenie | Wartość rzeczywista kosztu | Przykład |
|---|---|---|
| Czas jest stworzony. | Nie dotyczy | <p>Bob Kozack z jednostki organizacyjnej Fabrikam US ze stawką kosztów 100 USD (100 USD) na godzinę pracuje nad projektem o nazwie „Instalacja ramienia w Adatum”. Ten projekt jest mapowany na metodę rozliczania stałej ceny w ramach wiersza kontraktu. Oto przykładowy wpis dotyczący czasu od Boba Kozaka:</p><p>Bob Kozack — 8 godzin</p> |
| Czas jest zgłoszony. | Nie dotyczy | W przypadku wprowadzenia czasu jest tworzona pozycja kosztów. Domyślny koszt jest wprowadzany w wpisie daty. |
| Wpis godziny jest przechowany przed zatwierdzonego. | Nie dotyczy | |
| Czas jest zatwierdzony. | Tworzony jest koszt. | <p>Nowe wartości rzeczywiste, które są tworzone:</p><ul><li>**Koszt rzeczywisty:** Bob Kozack, 8 godzin, 800 USD</li></ul> |
| Zatwierdzenie czasu jest anulowane. | <p>Stan korekty oryginalnego kosztu jest aktualizowany do wartości **Skorygowano**.</p><p>Tworzony jest koszt ponownego kosztu, który ma stan **Nieskorygowano**.</p> | <p>Istniejące wartości rzeczywiste, które zostały zaktualizowane:</p><ul><li>**Koszt rzeczywisty**: Bob Kozack, 8 godzin, 800 USD *Skorygowano*</li></ul><p>Nowa wartość rzeczywista tworzona w celu odwrócenia poprzedniego wpływu finansowego:</p><ul><li>**Koszt rzeczywisty**: Bob Kozack, (8 godzin), (800 USD), *Nieskorygowano*</li></ul> |
| Wpis czasu jest przywoływany po zatwierdzeniu. | <p>Stan korekty oryginalnego kosztu jest aktualizowany do wartości **Skorygowano**.</p><p>Tworzony jest koszt ponownego kosztu, który ma stan **Nieskorygowano**.</p> | <p>Istniejące wartości rzeczywiste, które zostały zaktualizowane:</p><ul><li>**Koszt rzeczywisty**: Bob Kozack, 8 godzin, 800 USD *Skorygowano*</li></ul><p>Nowa wartość rzeczywista tworzona w celu odwrócenia poprzedniego wpływu finansowego:</p><ul><li>**Koszt rzeczywisty**: Bob Kozack, (8 godzin), (800 USD), *Nieskorygowano*</li></ul> |
| Oferta została wonna i tworzony jest kontrakt. | <p>Status korekty starych faktur kosztowych jest aktualizowany do **Skorygowano**.</p><p>Tworzone są faktyczne koszty odwrócenia, które mają status korekty **Nieskorygowano**.</p><p>Nowe wartości rzeczywiste kosztów są tworzone po przesądzeniu reguł kontraktu.</p> | <p>Istniejące wartości rzeczywiste, które zostały zaktualizowane:</p><ul><li>**Koszt rzeczywisty**: Bob Kozack, 8 godzin, 800 USD *Skorygowano*</li></ul><p>Nowa wartość rzeczywista tworzona w celu odwrócenia poprzedniego wpływu finansowego:</p><ul><li>**Koszt rzeczywisty**: Bob Kozack, (8 godzin), (800 USD), *Nieskorygowano*</li></ul><p>Nowe wartości rzeczywiste, które są tworzone dla przesądzonych wpływów finansowych po wykorzystaniu oferty i utworzeniu kontraktu:</p><ul><li>**Koszt rzeczywisty:** Bob Kozack, 8 godzin, 800 USD</li><li>**Niezwiązane ze sprzedażą wartości rzeczywiste:** Bob Kozack, 8 godzin, USD 1600</li></ul> |

[!INCLUDE[footer-include](../includes/footer-banner.md)]
