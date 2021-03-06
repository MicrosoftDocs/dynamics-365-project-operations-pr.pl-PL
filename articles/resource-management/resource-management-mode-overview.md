---
title: Omówienie trybów zarządzania zasobami
description: W tym temacie zamieszczono informacje o funkcjach Zarządzania zasobami w Dynamics 365 Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 4a8e605109e48b50da68abeee989f8ac8d3d659c
ms.sourcegitcommit: cf79185c8c84c55fbae55f9cfc1b17840e072b49
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/01/2020
ms.locfileid: "3930104"
---
# <a name="resource-management-modes-overview"></a>Omówienie trybów zarządzania zasobami

_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_


Dynamics 365 Project Operations obsługuje dwa tryby w celu wykonania całościowego przepływu rezerwacji. Tryb zarządzania jest definiowany jako parametr projektu i może zostać zmodyfikowany, jeśli wystąpi taka konieczność.    

## <a name="central-mode"></a>Tryb centralny
W przypadku organizacji, w których scentralizowano alokację zasobów do projektów, tryb centralny umożliwia zapewnienie menedżerom projektów możliwości definiowania wymagań dotyczących zasobów na poziomie projektu. Realizacja zapotrzebowania na zasoby jest przekazywana do menedżera zasobów. Menedżerowie projektów mogą akceptować lub odrzucać zasoby, które zaproponował menedżer zasobów.

![Tryb centralny](./media/resource-management-central.png)

Aby zarządzać zasobami w trybie Centralnym, zobacz:

- [Przypisywanie ogólnego zasobu możliwego do zarezerwowania do zadania i generowanie wymagań zasobów](https://docs.microsoft.com/dynamics365/project-service/assign-generic-bookable-resource)
- [Rezerwowanie nazwanych zasobów z poziomu wymagań zasobów](https://docs.microsoft.com/dynamics365/project-service/book-named-resource)
- [Przesyłanie żądania zasobów](https://docs.microsoft.com/dynamics365/project-service/submit-resource-request)
- [Realizowanie żądania zasobów](https://docs.microsoft.com/dynamics365/project-service/resource-management-fulfill-requests)
- [Akceptowanie lub odrzucanie proponowanego zasobu projektu z poziomu żądania zasobu](https://docs.microsoft.com/dynamics365/project-service/accept-reject-proposed-resource)

## <a name="hybrid-mode"></a>Tryb hybrydowy
W organizacjach, które potrzebują elastyczności w zakresie alokacji zasobów, tryb hybrydowy umożliwia menedżerom projektów i menedżerom zasobów możliwość tworzenia rezerwacji zasobów.

![Tryb hybrydowy](./media/resource-management-hybrid.png)

Poza obsługiwanym procesem w trybie centralnym można także skorzystać z następujących tematów, aby zarządzać wszystkimi innymi obsługiwanymi przepływami rezerwacji w trybie hybrydowym:

Rezerwacja zasobu bezpośrednio do projektu:
- [Rezerwowanie nazwanych zasobów możliwych do zarezerwowania dla zespołu projektu i przypisywanie zadań](https://docs.microsoft.com/dynamics365/project-service/assign-named-bookable-resource)

Rezerwowanie zasobów z poziomu wymagań zasobów:
- [Przypisywanie ogólnego zasobu możliwego do zarezerwowania do zadania i generowanie wymagań zasobów](https://docs.microsoft.com/dynamics365/project-service/assign-generic-bookable-resource)
- [Rezerwowanie nazwanych zasobów z poziomu wymagań zasobów](https://docs.microsoft.com/dynamics365/project-service/book-named-resource)
