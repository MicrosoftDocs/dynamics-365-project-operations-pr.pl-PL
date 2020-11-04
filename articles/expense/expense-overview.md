---
title: Omówienie wydatków
description: Ta temat zawiera informacje na temat funkcji Wydatków w Project Operations.
author: stsporen
manager: AnnBe
ms.date: 10/06/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 6da831fef5dba060b8019d7689645405c7ebdbed
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081892"
---
# <a name="expense-home-page"></a>Strona główna wydatku

_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_


Dynamics 365 Project Operations obsługuje możliwość przetwarzania wydatków. Przetwarzanie wydatków jest realizowane z projektami lub bez nich, dzięki możliwemu do dostosowania przepływowi pracy w ramach zasad, kategorii transakcji i zatwierdzeń.

W Project Operations istnieją dwa modele wdrożeń obsługiwanych na potrzeby wydatkowania: 

- **Pełne** : pełne wdrażanie jest dostępne dla **Project Operations dla zasobów/scenariuszy nieopartych na zaopatrzeniu** lub **Project Operations dla scenariuszy opartych na zamówieniach produkcyjnych**.
- **Podstawowe** : wdrażanie podstawowe jest dostępne dla **Project Operations dla zasobów/scenariuszy nieopartych na zaopatrzeniu** oraz **Wdrożenia uproszczonego — od oferty do faktury pro forma**.

## <a name="full"></a>Pełny 
W pełnym wdrożeniu kosztów program dostarcza kompleksowego egzekwowania zasad, który zawiera możliwość tworzenia zasad, takich jak:

  - Tworzenie limitów wydatków w kategorii
  - Podróż
  - Dieta
  - Pobieranie danych z karty kredytowej
  - Optyczne rozpoznawanie znaków z paragonów (OCR)

## <a name="basic"></a>Podstawowy 
Scenariusz podstawowego wdrażania wydatków umożliwia tylko rejestrowanie w projekcie podstawowych kosztów. 

Aby uzyskać więcej informacji, zobacz temat [Pozycja wydatek (uproszczone)](basic-expense.md)

## <a name="determine-your-expense-deployment"></a>Określenie typu wdrażania wydatków
Aby sprawdzić, czy uruchomiono podstawowe wdrożenie zarządzania wydatkami, należy sprawdzić, czy adres URL programu kończy się rozszerzeniem **.crm.dynamics.com**. 
