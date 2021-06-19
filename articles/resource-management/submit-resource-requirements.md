---
title: Przesyłanie żądania zasobów
description: Wygenerowane wymaganie zasobu można przesłać jako żądanie zasobu. Żądanie jest następnie wysyłane do menedżera zasobów w celu zrealizowania.
author: ruhercul
ms.date: 10/04/2020
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 6ac0044a27d1e506c9c62c477014017fd0ca06cb
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 05/10/2021
ms.locfileid: "6014039"
---
# <a name="submit-a-resource-request"></a>Przesyłanie żądania zasobów

_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_

Wygenerowane wymaganie zasobu można przesłać jako żądanie zasobu. Żądanie jest następnie wysyłane do menedżera zasobów w celu zrealizowania.

1. W rozwiązaniu Dynamics 365 Project Operations na stronie **Projekty** kliknij kartę **Zespół**, aby wyświetlić listę zasobów możliwych do zarezerwowania. 
2. Z listy wybierz zasób ogólny, który ma wymaganie zasobu, a następnie kliknij opcję **Prześlij żądanie**.

Stan żądania o ogólnego członka zespołu zmieni się na **"Przesłano**.

Gdy żądanie zostanie zrealizowane, ogólny zasób zostanie zastąpiony nazwanym zasobem, jeśli menedżer zasobów zrealizował żądanie poprzez zarezerwowanie nazwanego zasobu. W przeciwnym razie, jeśli menedżer zaproponuje nazwany zasób, zasób ogólny pozostanie w zespole, a stan żądania zmieni się na **Wymaga przeglądu**, jeśli menedżer zasobów zaproponował nazwany zasób.


[!INCLUDE[footer-include](../includes/footer-banner.md)]