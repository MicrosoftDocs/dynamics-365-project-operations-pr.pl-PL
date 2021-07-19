---
title: Omówienie wydatków
description: Ta temat zawiera informacje na temat funkcji Wydatków w Project Operations.
author: stsporen
ms.date: 10/06/2020
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: stsporen
ms.custom: intro-internal
ms.openlocfilehash: 921df6fa8f1eb33bd01792c0b7c787fc74604adf
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/07/2021
ms.locfileid: "6368579"
---
# <a name="expense-home-page"></a><span data-ttu-id="18a06-103">Strona główna wydatku</span><span class="sxs-lookup"><span data-stu-id="18a06-103">Expense home page</span></span>

<span data-ttu-id="18a06-104">_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_</span><span class="sxs-lookup"><span data-stu-id="18a06-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="18a06-105">Dynamics 365 Project Operations wspiera zdolność do przetwarzania wydatków.</span><span class="sxs-lookup"><span data-stu-id="18a06-105">Dynamics 365 Project Operations supports the ability to process expenses.</span></span> <span data-ttu-id="18a06-106">Przetwarzanie wydatków jest realizowane z projektami lub bez nich, dzięki możliwemu do dostosowania przepływowi pracy w ramach zasad, kategorii transakcji i zatwierdzeń.</span><span class="sxs-lookup"><span data-stu-id="18a06-106">Expense processing occurs with or without projects by using a customizable workflow of policies, transaction categories, and approvals.</span></span>

<span data-ttu-id="18a06-107">W Project Operations istnieją dwa modele wdrożeń obsługiwanych na potrzeby wydatkowania:</span><span class="sxs-lookup"><span data-stu-id="18a06-107">In Project Operations, there are two supported deployment models for Expense:</span></span> 

- <span data-ttu-id="18a06-108">**Pełne**: pełne wdrażanie jest dostępne dla **Project Operations dla zasobów/scenariuszy nieopartych na zaopatrzeniu** lub **Project Operations dla scenariuszy opartych na zamówieniach produkcyjnych**.</span><span class="sxs-lookup"><span data-stu-id="18a06-108">**Full**: Full deployment is available for **Project Operations for resource/non-stocked based scenarios** or **Project Operations for production order-based scenarios**.</span></span>
- <span data-ttu-id="18a06-109">**Podstawowe**: wdrażanie podstawowe jest dostępne dla **Project Operations dla zasobów/scenariuszy nieopartych na zaopatrzeniu** oraz **Wdrożenia uproszczonego — od oferty do faktury pro forma**.</span><span class="sxs-lookup"><span data-stu-id="18a06-109">**Basic**: Basic deployment is available for **Project Operations for resource/non-stocked based scenarios** and **Lite deployment – deal to proforma invoicing**.</span></span>

## <a name="full"></a><span data-ttu-id="18a06-110">Pełny</span><span class="sxs-lookup"><span data-stu-id="18a06-110">Full</span></span> 
<span data-ttu-id="18a06-111">Wdrożenie pełnego kosztu zapewnia pełne egzekwowanie zasad, które obejmuje możliwość tworzenia zasad, takich jak:</span><span class="sxs-lookup"><span data-stu-id="18a06-111">Full Expense deployment provides a complete policy enforcement that includes the ability to create policies, such as:</span></span>

  - <span data-ttu-id="18a06-112">Tworzenie limitów wydatków w kategorii</span><span class="sxs-lookup"><span data-stu-id="18a06-112">Expense category limits</span></span>
  - <span data-ttu-id="18a06-113">Podróż</span><span class="sxs-lookup"><span data-stu-id="18a06-113">Travel</span></span>
  - <span data-ttu-id="18a06-114">Dieta</span><span class="sxs-lookup"><span data-stu-id="18a06-114">Per diem</span></span>
  - <span data-ttu-id="18a06-115">Pobieranie danych z karty kredytowej</span><span class="sxs-lookup"><span data-stu-id="18a06-115">Credit card imports</span></span>
  - <span data-ttu-id="18a06-116">Optyczne rozpoznawanie znaków z paragonów (OCR)</span><span class="sxs-lookup"><span data-stu-id="18a06-116">Receipt optical character recognition</span></span>

## <a name="basic"></a><span data-ttu-id="18a06-117">Podstawowy</span><span class="sxs-lookup"><span data-stu-id="18a06-117">Basic</span></span> 
<span data-ttu-id="18a06-118">Scenariusz podstawowego wdrażania wydatków umożliwia tylko rejestrowanie w projekcie podstawowych kosztów.</span><span class="sxs-lookup"><span data-stu-id="18a06-118">Basic Expense deployment scenario only allows you to record basic expenses against a project.</span></span> 

<span data-ttu-id="18a06-119">Aby uzyskać więcej informacji, zobacz temat [Pozycja wydatek (uproszczone)](basic-expense.md)</span><span class="sxs-lookup"><span data-stu-id="18a06-119">For more information, see [Expense entry (lite)](basic-expense.md)</span></span>

## <a name="determine-your-expense-deployment"></a><span data-ttu-id="18a06-120">Określenie typu wdrażania wydatków</span><span class="sxs-lookup"><span data-stu-id="18a06-120">Determine your Expense deployment</span></span>
<span data-ttu-id="18a06-121">Aby sprawdzić, czy uruchomiono podstawowe wdrożenie zarządzania wydatkami, należy sprawdzić, czy adres URL programu kończy się rozszerzeniem **.crm.dynamics.com**.</span><span class="sxs-lookup"><span data-stu-id="18a06-121">To determine if you're running the Basic Expense management deployment, verify that the address URL ends with **.crm.dynamics.com**.</span></span> 


[!INCLUDE[footer-include](../includes/footer-banner.md)]