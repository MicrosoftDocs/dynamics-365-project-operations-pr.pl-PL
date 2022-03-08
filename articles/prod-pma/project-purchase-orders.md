---
title: Zamówienia zakupu dla projektu
description: W tym artykule opisano różne metody korzystania z programu w celu tworzenia zamówień zakupu dla projektu. Użycie metody zależy od celu zamówienia zakupu oraz wtedy, gdy zakupione towary są konsumowane i pobierane z projektu.
author: Yowelle
ms.date: 09/14/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 83972
ms.assetid: 247e4d72-610b-4fa5-9873-601ed0f4b2d6
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5de28f3844b802a980c811411cae75549c697538f89e8c3d2495ea171a188524
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/06/2021
ms.locfileid: "7009004"
---
# <a name="purchase-orders-for-a-project"></a>Zamówienia zakupu dla projektu

[!include [banner](../includes/banner.md)]

W tym artykule opisano różne metody korzystania z programu w celu tworzenia zamówień zakupu dla projektu. Użycie metody zależy od celu zamówienia zakupu oraz wtedy, gdy zakupione towary są konsumowane i pobierane z projektu.

### <a name="methods-for-creating-a-purchase-order"></a>Metody tworzenia zamówienia zakupu

Aby utworzyć zamówienie zakupu w programie Zarządzanie projektami i ich księgowanie, można użyć jednej z następujących metod. Cel zamówienia zakupu określa, kiedy zamówienie zakupu jest zużywane, a tym samym, kiedy towary są rozliczane w projekcie.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>Metoda</th>
<th>Przeznaczenie</th>
<th>Zużycie towarów</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Utwórz zamówienie zakupu bezpośrednio z poziomu projektu.</td>
<td>Tej metody należy użyć w celu zakupienia towarów z zewnętrznego dostawcy w celu zużycia w projekcie. Zamówienie zakupu można utworzyć na dwa sposoby:
<ul>
<li>Z poziomu samego projektu. W tym przypadku projekt jest już zdefiniowany dla zamówienia zakupu.</li>
<li>Przejście do zamówienia zakupu dotyczącego projektu. Należy wybrać zarówno dostawcę, jak i projekt, dla którego ma zostać utworzone zamówienie zakupu.</li>
</ul></td>
<td>Towary są pobierane podczas aktualizacji faktury zakupu.</td>
</tr>
<tr class="even">
<td>Utwórz zamówienie zakupu na podstawie zamówienia sprzedaży.</td>
<td>Tej metody należy użyć w celu zakupienia towarów podczas tworzenia zamówienia sprzedaży na podstawie projektu.</td>
<td>Towary są zużywane, kiedy zamówienie sprzedaży jest zafakturowane na klienta.</td>
</tr>
<tr class="odd">
<td>Utwórz zamówienie zakupu z zapotrzebowania na towary.</td>
<td>Ta metoda służy do kupowania towarów podczas tworzenia zapotrzebowania na towary z projektu.</td>
<td>Towary są zużywane podczas aktualizacji dokumentu dostawy zapotrzebowania na towary.</td>
</tr>
</tbody>
</table>

> [!NOTE] 
> W przypadku aktualizowania faktury dostawcy lub dokumentu dostawy jest wyświetlany monit o zaktualizowanie dokumentu dostawy w zapotrzebowaniu na towary.

Aby uzyskać więcej informacji, zobacz temat [Pobierz towary w zamówieniu zakupu z zapotrzebowania na towary](tasks/receive-items-purchase-order-item-requirement.md).



[!INCLUDE[footer-include](../includes/footer-banner.md)]