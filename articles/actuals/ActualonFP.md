---
title: Wartości rzeczywiste mają wpływ na zaangażowanie w stałą cenę
description: Ten artykuł zawiera informacje o wpływie na tabelę Rzeczywiste w różnych wydarzeniach w cyklu życia zobowiązania o ustalonej cenie w Microsoft Dynamics 365 Project Operations.
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
ms.openlocfilehash: 50819d77d56935bfe5438d7d9dae99562bcc0b49
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8918141"
---
# <a name="actuals-impact-in-a-fixed-price-engagement"></a>Wartości rzeczywiste mają wpływ na zaangażowanie w stałą cenę

_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_

W poniższej tabeli wymieniono dane rzeczywiste różnych typów transakcji, które są tworzone podczas różnych wydarzeń w ramach zobowiązania o ustalonej cenie.

| Wydarzenie | Wartość rzeczywista kosztu | Wartość rzeczywista nierozliczonej sprzedaży | Wartość rzeczywista rozliczonej sprzedaży | Przykład |
|---|---|---|---|---|
| Czas jest stworzony. | Nie dotyczy | Nie dotyczy | Nie dotyczy | <p>Bob Kozack z jednostki organizacyjnej Fabrikam US ze stawką kosztów 100 USD (100 USD) na godzinę pracuje nad projektem o nazwie „Instalacja ramienia w Adatum”. Ten projekt jest mapowany na metodę rozliczania stałej ceny w ramach wiersza kontraktu. Oto przykładowy wpis dotyczący czasu od Boba Kozaka:</p><p>Bob Kozack — 8 godzin</p> |
| Czas jest zgłoszony. | Nie dotyczy | Nie dotyczy | Nie dotyczy | W przypadku wprowadzenia czasu jest tworzona pozycja kosztów. Domyślny koszt jest wprowadzany w wpisie daty. |
| Wpis godziny jest przechowany przed zatwierdzonego. | Nie dotyczy | Nie dotyczy | Nie dotyczy | |
| Czas jest zatwierdzony. | Tworzony jest koszt. | Nie dotyczy | Nie dotyczy | <p>Nowe wartości rzeczywiste, które są tworzone:</p><ul><li>**Koszt rzeczywisty:** Bob Kozack, 8 godzin, 800 USD</li></ul> |
| Zatwierdzenie czasu jest anulowane. | <p>Stan korekty oryginalnego kosztu jest aktualizowany do wartości **Skorygowano**.</p><p>Tworzony jest koszt ponownego kosztu, który ma stan **Nieskorygowano**.</p> | Nie dotyczy | Nie dotyczy | <p>Istniejące wartości rzeczywiste, które zostały zaktualizowane:</p><ul><li>**Koszt rzeczywisty**: Bob Kozack, 8 godzin, 800 USD *Skorygowano*</li></ul><p>Nowa wartość rzeczywista tworzona w celu odwrócenia poprzedniego wpływu finansowego:</p><ul><li>**Koszt rzeczywisty**: Bob Kozack, (8 godzin), (800 USD), *Nieskorygowano*</li></ul> |
| Wpis czasu jest przywoływany po zatwierdzeniu. | <p>Stan korekty oryginalnego kosztu jest aktualizowany do wartości **Skorygowano**.</p><p>Tworzony jest koszt ponownego kosztu, który ma stan **Nieskorygowano**.</p> | Nie dotyczy | Nie dotyczy | <p>Istniejące wartości rzeczywiste, które zostały zaktualizowane:</p><ul><li>**Koszt rzeczywisty**: Bob Kozack, 8 godzin, 800 USD *Skorygowano*</li></ul><p>Nowa wartość rzeczywista tworzona w celu odwrócenia poprzedniego wpływu finansowego:</p><ul><li>**Koszt rzeczywisty**: Bob Kozack, (8 godzin), (800 USD), *Nieskorygowano*</li></ul> |
| Umowa została potwierdzona. | <p>Status korekty starych faktur kosztowych jest aktualizowany do **Skorygowano**.</p><p>Tworzone są faktyczne koszty odwrócenia, które mają status korekty **Nieskorygowano**.</p><p>Nowe wartości rzeczywiste kosztów są tworzone po przesądzeniu reguł kontraktu.</p> | Nie dotyczy | Nie dotyczy | <p>Istniejące wartości rzeczywiste, które zostały zaktualizowane:</p><ul><li>**Koszt rzeczywisty**: Bob Kozack, 8 godzin, 800 USD *Skorygowano*</li></ul><p>Nowa wartość rzeczywista tworzona w celu odwrócenia poprzedniego wpływu finansowego:</p><ul><li>**Koszt rzeczywisty**: Bob Kozack, (8 godzin), (800 USD), *Nieskorygowano*</li></ul><p>Nowe wartości rzeczywiste, które są tworzone dla przesądzonych wpływów finansowych:</p><ul><li>**Koszt rzeczywisty:** Bob Kozack, 8 godzin, 800 USD</li></ul> |
| Zostanie utworzona faktura. | Nie dotyczy | Nie dotyczy | Nie dotyczy | |
| Faktura została potwierdzina za pomocą punktów kontrolnych. | Nie dotyczy | Nie dotyczy | Tworzone są nowe wartości rzeczywiste sprzedaży rozliczane na podstawie punktów kontrolnych. | <p>Istniejące wartości rzeczywiste, które pozostają niezmienione:</p><ul><li>**Koszt rzeczywisty:** Bob Kozack, 8 godzin, 800 USD</li></ul><p>Nowe wartości rzeczywiste tworzone w celu zarejestrowanego za fakturowanych wartości sprzedaży:</p><ul><li>**Rzeczywista rozliczona sprzedaż:** kamień milowy, 5000 USD</li></ul> |
| Faktura zostanie poprawiona w celu kredytu punktów kontrolnych. | Nie dotyczy | Nie dotyczy | Tworzone są rzeczywiste dane sprzedaży rozliczanej odwrotnie. | <p>Istniejące wartości rzeczywiste, które pozostają niezmienione:</p><ul><li>**Koszt rzeczywisty:** Bob Kozack, 8 osób, 800 USD</li></ul><p>Istniejące wartości rzeczywiste, które zostały zaktualizowane:</p><ul><li>**Rzeczywista rozliczona sprzedaż:** kamień milowy, 5000 USD, *Skorygowano*</li></ul><p>Nowy stan faktyczny, który jest tworzony w celu odwrócenia poprzednich wartości sprzedaży rozliczanej:</p><ul><li>**Rzeczywista rozliczona sprzedaż:** kamień milowy, (5000 USD), *Nieskorygowano*</li></ul> |

[!INCLUDE[footer-include](../includes/footer-banner.md)]
