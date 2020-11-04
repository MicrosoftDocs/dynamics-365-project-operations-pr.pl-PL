---
title: Konfigurowanie pól niestandardowych Project Operations jako wymiarów kalkulacji cen
description: W tym temacie zamieszczono informacje na temat używania istniejących pól programu Dynamics 365 Project Operations jako wymiarów kalkulacji cen.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 56ff45169058d96d7ef81a710de309eec698a75f
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082075"
---
# <a name="project-operations-fields-as-pricing-dimensions"></a>Konfigurowanie pól niestandardowych Project Operations jako wymiarów kalkulacji cen

_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_

Encja **Wartości rzeczywiste** zawiera wiele pól, które mogą być używane jako wymiary kalkulacji cen w przypadku kalkulacji cen opartej na zasobach. Na przykład popularnym polem jest **Zasób, który można zarezerwować**. Mniejsze firmy, które mają mniej niż 20–30 zasobów podlegających rozliczaniu, mogą uznać, że zdefiniowanie stawek rozliczania i kosztów specyficznych dla poszczególnych zasobów jest najprostsze. Jednakże wraz z wzrastającą liczbą pracowników, stawki zawierające konkretne koszty mogą stać się trudne w obsłudze. Koszty zasobów i stawki kosztów na początku zaczynają się różnić z czasem, gdyż pracownicy otrzymują awanse, zdobywają doświadczenie lub nowe umiejętności. 

Innym przykładem jest kategoria transakcji. Klienci i wdrożeniowcy używają kategorii transakcji do klasyfikowania pracy, a tego pola do określania cen i kosztów na podstawie kategorii pracy.
