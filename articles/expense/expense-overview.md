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
ms.sourcegitcommit: 0874b3d89e1dc0e65a51cedb82bf8f80831ca0bb
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/06/2020
ms.locfileid: "3967379"
---
# <a name="expense-home-page"></a><span data-ttu-id="8701d-103">Strona główna wydatku</span><span class="sxs-lookup"><span data-stu-id="8701d-103">Expense home page</span></span>

<span data-ttu-id="8701d-104">_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_</span><span class="sxs-lookup"><span data-stu-id="8701d-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="8701d-105">Dynamics 365 Project Operations obsługuje możliwość przetwarzania wydatków.</span><span class="sxs-lookup"><span data-stu-id="8701d-105">Dynamics 365 Project Operations supports the ability to process expenses.</span></span> <span data-ttu-id="8701d-106">Przetwarzanie wydatków jest realizowane z projektami lub bez nich, dzięki możliwemu do dostosowania przepływowi pracy w ramach zasad, kategorii transakcji i zatwierdzeń.</span><span class="sxs-lookup"><span data-stu-id="8701d-106">Expense processing occurs with or without projects by using a customizable workflow of policies, transaction categories, and approvals.</span></span>

<span data-ttu-id="8701d-107">W Project Operations istnieją dwa modele wdrożeń obsługiwanych na potrzeby wydatkowania:</span><span class="sxs-lookup"><span data-stu-id="8701d-107">In Project Operations, there are two supported deployment models for Expense:</span></span> 

- <span data-ttu-id="8701d-108">**Pełne**: pełne wdrażanie jest dostępne dla **Project Operations dla zasobów/scenariuszy nieopartych na zaopatrzeniu** lub **Project Operations dla scenariuszy opartych na zamówieniach produkcyjnych**.</span><span class="sxs-lookup"><span data-stu-id="8701d-108">**Full**: Full deployment is available for **Project Operations for resource/non-stocked based scenarios** or **Project Operations for production order based scenarios**.</span></span>
- <span data-ttu-id="8701d-109">**Podstawowe**: wdrażanie podstawowe jest dostępne dla **Project Operations dla zasobów/scenariuszy nieopartych na zaopatrzeniu** oraz **Wdrożenia uproszczonego — od oferty do faktury pro forma**.</span><span class="sxs-lookup"><span data-stu-id="8701d-109">**Basic**: Basic deployment is available for **Project Operations for resource/non-stocked based scenarios** and **Lite deployment – deal to proforma invoicing**.</span></span>

## <a name="full"></a><span data-ttu-id="8701d-110">Pełny</span><span class="sxs-lookup"><span data-stu-id="8701d-110">Full</span></span> 
<span data-ttu-id="8701d-111">W pełnym wdrożeniu kosztów program dostarcza kompleksowego egzekwowania zasad, który zawiera możliwość tworzenia zasad, takich jak:</span><span class="sxs-lookup"><span data-stu-id="8701d-111">Full Expense deployment provides a complete policy enforcement which includes the ability to create policies, such as:</span></span>

  - <span data-ttu-id="8701d-112">Tworzenie limitów wydatków w kategorii</span><span class="sxs-lookup"><span data-stu-id="8701d-112">Expense category limits</span></span>
  - <span data-ttu-id="8701d-113">Podróż</span><span class="sxs-lookup"><span data-stu-id="8701d-113">Travel</span></span>
  - <span data-ttu-id="8701d-114">Dieta</span><span class="sxs-lookup"><span data-stu-id="8701d-114">Per diem</span></span>
  - <span data-ttu-id="8701d-115">Pobieranie danych z karty kredytowej</span><span class="sxs-lookup"><span data-stu-id="8701d-115">Credit card imports</span></span>
  - <span data-ttu-id="8701d-116">Optyczne rozpoznawanie znaków z paragonów (OCR)</span><span class="sxs-lookup"><span data-stu-id="8701d-116">Receipt optical character recognition</span></span>

## <a name="basic"></a><span data-ttu-id="8701d-117">Podstawowy</span><span class="sxs-lookup"><span data-stu-id="8701d-117">Basic</span></span> 
<span data-ttu-id="8701d-118">Scenariusz podstawowego wdrażania wydatków umożliwia tylko rejestrowanie w projekcie podstawowych kosztów.</span><span class="sxs-lookup"><span data-stu-id="8701d-118">Basic Expense deployment scenario only allows you to record basic expenses against a project.</span></span> 

<span data-ttu-id="8701d-119">Aby uzyskać więcej informacji, zobacz temat [Pozycja wydatek (uproszczone)](basic-expense.md)</span><span class="sxs-lookup"><span data-stu-id="8701d-119">For more information, see [Expense entry (lite)](basic-expense.md)</span></span>

## <a name="determine-your-expense-deployment"></a><span data-ttu-id="8701d-120">Określenie typu wdrażania wydatków</span><span class="sxs-lookup"><span data-stu-id="8701d-120">Determine your Expense deployment</span></span>
<span data-ttu-id="8701d-121">Aby sprawdzić, czy uruchomiono podstawowe wdrożenie zarządzania wydatkami, należy sprawdzić, czy adres URL programu kończy się rozszerzeniem **.crm.dynamics.com**.</span><span class="sxs-lookup"><span data-stu-id="8701d-121">To determine if you're running the Basic Expense management deployment, verify that the address URL ends with **.crm.dynamics.com**.</span></span> 
