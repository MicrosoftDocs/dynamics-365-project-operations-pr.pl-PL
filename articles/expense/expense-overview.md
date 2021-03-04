---
title: Omówienie wydatków
description: Ta temat zawiera informacje na temat funkcji Wydatków w Project Operations.
author: stsporen
manager: AnnBe
ms.date: 10/06/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: d946a8dcbf3b2369631d83e80788eed4904be95d
ms.sourcegitcommit: 2b74edd31f38410024a01124c9202a4d94464d04
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/17/2020
ms.locfileid: "4764922"
---
# <a name="expense-home-page"></a><span data-ttu-id="baf85-103">Strona główna wydatku</span><span class="sxs-lookup"><span data-stu-id="baf85-103">Expense home page</span></span>

<span data-ttu-id="baf85-104">_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_</span><span class="sxs-lookup"><span data-stu-id="baf85-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="baf85-105">Dynamics 365 Project Operations wspiera zdolność do przetwarzania wydatków.</span><span class="sxs-lookup"><span data-stu-id="baf85-105">Dynamics 365 Project Operations supports the ability to process expenses.</span></span> <span data-ttu-id="baf85-106">Przetwarzanie wydatków jest realizowane z projektami lub bez nich, dzięki możliwemu do dostosowania przepływowi pracy w ramach zasad, kategorii transakcji i zatwierdzeń.</span><span class="sxs-lookup"><span data-stu-id="baf85-106">Expense processing occurs with or without projects by using a customizable workflow of policies, transaction categories, and approvals.</span></span>

<span data-ttu-id="baf85-107">W Project Operations istnieją dwa modele wdrożeń obsługiwanych na potrzeby wydatkowania:</span><span class="sxs-lookup"><span data-stu-id="baf85-107">In Project Operations, there are two supported deployment models for Expense:</span></span> 

- <span data-ttu-id="baf85-108">**Pełne**: pełne wdrażanie jest dostępne dla **Project Operations dla zasobów/scenariuszy nieopartych na zaopatrzeniu** lub **Project Operations dla scenariuszy opartych na zamówieniach produkcyjnych**.</span><span class="sxs-lookup"><span data-stu-id="baf85-108">**Full**: Full deployment is available for **Project Operations for resource/non-stocked based scenarios** or **Project Operations for production order-based scenarios**.</span></span>
- <span data-ttu-id="baf85-109">**Podstawowe**: wdrażanie podstawowe jest dostępne dla **Project Operations dla zasobów/scenariuszy nieopartych na zaopatrzeniu** oraz **Wdrożenia uproszczonego — od oferty do faktury pro forma**.</span><span class="sxs-lookup"><span data-stu-id="baf85-109">**Basic**: Basic deployment is available for **Project Operations for resource/non-stocked based scenarios** and **Lite deployment – deal to proforma invoicing**.</span></span>

## <a name="full"></a><span data-ttu-id="baf85-110">Pełny</span><span class="sxs-lookup"><span data-stu-id="baf85-110">Full</span></span> 
<span data-ttu-id="baf85-111">Wdrożenie pełnego kosztu zapewnia pełne egzekwowanie zasad, które obejmuje możliwość tworzenia zasad, takich jak:</span><span class="sxs-lookup"><span data-stu-id="baf85-111">Full Expense deployment provides a complete policy enforcement that includes the ability to create policies, such as:</span></span>

  - <span data-ttu-id="baf85-112">Tworzenie limitów wydatków w kategorii</span><span class="sxs-lookup"><span data-stu-id="baf85-112">Expense category limits</span></span>
  - <span data-ttu-id="baf85-113">Podróż</span><span class="sxs-lookup"><span data-stu-id="baf85-113">Travel</span></span>
  - <span data-ttu-id="baf85-114">Dieta</span><span class="sxs-lookup"><span data-stu-id="baf85-114">Per diem</span></span>
  - <span data-ttu-id="baf85-115">Pobieranie danych z karty kredytowej</span><span class="sxs-lookup"><span data-stu-id="baf85-115">Credit card imports</span></span>
  - <span data-ttu-id="baf85-116">Optyczne rozpoznawanie znaków z paragonów (OCR)</span><span class="sxs-lookup"><span data-stu-id="baf85-116">Receipt optical character recognition</span></span>

## <a name="basic"></a><span data-ttu-id="baf85-117">Podstawowy</span><span class="sxs-lookup"><span data-stu-id="baf85-117">Basic</span></span> 
<span data-ttu-id="baf85-118">Scenariusz podstawowego wdrażania wydatków umożliwia tylko rejestrowanie w projekcie podstawowych kosztów.</span><span class="sxs-lookup"><span data-stu-id="baf85-118">Basic Expense deployment scenario only allows you to record basic expenses against a project.</span></span> 

<span data-ttu-id="baf85-119">Aby uzyskać więcej informacji, zobacz temat [Pozycja wydatek (uproszczone)](basic-expense.md)</span><span class="sxs-lookup"><span data-stu-id="baf85-119">For more information, see [Expense entry (lite)](basic-expense.md)</span></span>

## <a name="determine-your-expense-deployment"></a><span data-ttu-id="baf85-120">Określenie typu wdrażania wydatków</span><span class="sxs-lookup"><span data-stu-id="baf85-120">Determine your Expense deployment</span></span>
<span data-ttu-id="baf85-121">Aby sprawdzić, czy uruchomiono podstawowe wdrożenie zarządzania wydatkami, należy sprawdzić, czy adres URL programu kończy się rozszerzeniem **.crm.dynamics.com**.</span><span class="sxs-lookup"><span data-stu-id="baf85-121">To determine if you're running the Basic Expense management deployment, verify that the address URL ends with **.crm.dynamics.com**.</span></span> 
