---
title: Przesyłanie żądania zasobów
description: Wygenerowane wymaganie zasobu można przesłać jako żądanie zasobu. Żądanie jest następnie wysyłane do menedżera zasobów w celu zrealizowania.
author: ruhercul
ms.date: 10/04/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: 1e09d92de310dbe09e53ae134e5bb195fd64178f
ms.sourcegitcommit: 341192e1e45eb42d6b18a8370ac2e1100c4a4ca4
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/12/2022
ms.locfileid: "9137194"
---
# <a name="submit-a-resource-request"></a>Przesyłanie żądania zasobów

_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_

Wygenerowane wymaganie zasobu można przesłać jako żądanie zasobu. Żądanie jest następnie wysyłane do menedżera zasobów w celu zrealizowania.

1. W rozwiązaniu Dynamics 365 Project Operations na stronie **Projekty** kliknij kartę **Zespół**, aby wyświetlić listę zasobów możliwych do zarezerwowania. 
2. Z listy wybierz zasób ogólny, który ma wymaganie zasobu, a następnie kliknij opcję **Prześlij żądanie**.

Stan żądania o ogólnego członka zespołu zmieni się na **"Przesłano**.

Odbiorca żądania zasobu może albo częściowo wypełnić żądanie przy użyciu jednego lub więcej zasobów, albo całkowicie spełnić żądanie zasobu.

Po spełnieniu żądania co najmniej jeden nazwany zasób zostanie dodany do projektu jako członkowie zespołu projektowego. Jeśli wymóg dotyczący zasobu jest spełniony przez jeden zasób, ogólny członek zespołu powiązany z żądaniem zasobu jest usuwany. 

Gdy odbiorca żądania zasobów zaproponuje zasoby i jest gotowy, aby kierownik projektu mógł przejrzeć zaproponowane zasoby, powinien zaktualizować stan żądania zasobów na **Wymaga przeglądu**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
