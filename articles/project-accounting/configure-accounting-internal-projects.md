---
title: Konfigurowanie księgowania projektów wewnętrznych
description: W tym temacie zamieszczono informacje dotyczące sposobu konfigurowania zasad księgowania w odniesieniu do projektów wewnętrznych w Project Operations.
author: sigitac
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 504e7481cb2aee6310cb4ace2d0791d1c7fe360d
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081946"
---
# <a name="configure-accounting-for-internal-projects"></a>Konfigurowanie księgowania projektów wewnętrznych

_**Zastosowane do:** Project Operations dla zasobów/scenariuszy nieopartych na zaopatrzeniu_

Projekty wewnętrzne umożliwiają firmom śledzenie kosztów związanych z działaniami, które nie są rozliczane z klientem. Przykładowe projekty wewnętrzne to między innymi:

- Opracowywanie produktu, takiego jak aplikacja mobilna oraz śledzenie kosztów związanych z rozwojem projektu.
- Zarządzanie czasem i wydatkami przed sprzedażą. Projekty wewnętrzne przed sprzedażą można przekonwertować później na projekt rozliczany, jeśli oferta została wykorzystana.

Każdy projekt nieskojarzony z kontraktem w Dynamics 365 Project Operations jest traktowany jako wewnętrzny. Reguły kosztów projektu i profili przychodów nie określają reguły księgowania transakcji dla tego projektu. Koszt projektu wewnętrznego jest zawsze księgowany przy użyciu reguł zysków i strat. Konta księgowe na potrzeby księgowania są definiowane na stronie **Konfiguracja księgowania w rejestrze**.

- Transakcje czasowe są księgowane: obciążenia na koncie **Kosztów** , a uznania na koncie **Alokacja płac**.
- Transakcje wydatkowe są księgowane: obciążenia na koncie **Kosztów** , a uznania na koncie **rozliczeniowym dla wydatku**.

Jeśli projekt jest skojarzony z kontraktem projektu po zaksięgowaniu transakcji, system cofnie wszystkie transakcje skumulowane i tworzy nowe transakcje fakturowania. Transakcje podlegające rozliczaniu podążają za regułami księgowania zdefiniowanymi w odpowiednim profilu kosztów projektów i przychodów.


