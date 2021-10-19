---
title: Omówienie przechowywania danych dostawców
description: Ten temat umożliwia omówienie funkcji przechowywania danych dostawców.
author: sigitac
ms.date: 10/01/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 5f89904af5fb00eac46de834a438f412b371e74e
ms.sourcegitcommit: 098ea345ecfaf4445520094c32f5511b67e7953c
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/02/2021
ms.locfileid: "7594615"
---
# <a name="vendor-retention-overview"></a>Omówienie przechowywania danych dostawców

_**Zastosowane do:** Project Operations dla zasobów/scenariuszy nieopartych na zaopatrzeniu_

Organizacja może chcieć zachować część płatności dla dostawców, którzy pracują nad projektami w organizacji. Na przykład przed zapłaceniem dostawcy można się upewnić, że dostarczone przez niego towary i usługi spełniają oczekiwania użytkownika.

W przypadku negocjacji zakupów w ramach projektów z dostawcami można określić postanowienia przechowywania danych dostawcy, które zawierają wartość procentową lub kwotę, która ma zostać przechowana. W związku z tym, że dostawca dostarcza towary i usługi, odliczany jest określony procent przechowywania lub kwota od płatności dla dostawcy. Po zakończeniu projektu lub osiągnięciu etapu tymczasowego określonego w kontrakcie dostawcy użytkownik zwalnia zatrzymaną kwotę i tworzy płatność dla dostawcy.

## <a name="vendor-retention-example"></a>Przykład przechowywania danych dostawców

W następującym przykładzie pokazano, jak zachowywany jest procent kwoty na fakturze od dostawcy na podstawie procentu realizacji projektu.

Firma Contoso Robotics USA ma kontrakt z dostawcą Fabrikam w celu zapewnienia 100 godzin szkoleń dla projektu odnawianiu sprzętu. Łączna wartość kontraktu wynosi 30 000 USD z uzgodnioną ceną zakupu 300 USD na godzinę.

Szkolenia będą realizowane w trzech etapach z następującym harmonogramem:

- Etap 1: 50 godzin lub 50 procent projektu
- Etap 2: 30 godzin lub 80 procent projektu w sumie
- Etap 3: 20 godzin lub 100 procent projektu

W poniższej tabeli przedstawiono warunki przechowywania.

| **Procent dostarczanych jednostek** | **Procent do przechowania** | **Procent do zwolnienia** |
| --- | --- | --- |
| 50% | 20% | 0% |
| 80% | 10% | 10% |
| 100% | 0% | 100% |

W wyniku transakcji są następujące kwoty:

- Faza 1:
  - Kwota do zapłaty to 50 x 300 lub 15 000.
  - 20 procent kwoty, czyli 3000, pozostaje i zostanie zwolnione na późniejszym etapie.
  - Kwota, która zostanie zapłacona dostawcy to 12 000.
- Faza 2:
  - Kwota do zapłaty to 30 x 300 lub 9000.
  - 10 procent kwoty, czyli 900, pozostaje.
  - 10 procent z 3000, które zostały wstrzymane w fazie 1, czyli 300, jest zwalniane.
  - Kwota, która zostanie zapłacona dostawcy to 8400. Jest to kwota 9000 pomniejszona o zatrzymane 900 plus 300, które zostało zwolnione z zatrzymania fazy 1.
- Faza 3:
  - Kwota do zapłaty to 20 x 300 lub 6000.
  - Żadna kwota nie pozostaje zatrzymana.
  - Kwota, która jest zwalniana to 3600. Ta kwota składa się z 3000, które zostały zatrzymane w etapie 1, pomniejszone o 300 z fazy 1, które zostały zwolnione w fazie 2, plus 900 zatrzymane w fazie 2.
  - Kwota, która zostanie zapłacona dostawcy to 9600. Ta kwota składa się z zatrzymanej kwoty 3600 plus 6000 na zakończenie fazy 3.

Łączna kwota zapłacona dostawcy po zakończeniu trzech etapów wynosi 30 000, co stanowi łączną kwotę zamówienia (15 000 + 9000 + 6000).
