---
title: Omówienie wdrożenia aplikacji Project Operations dla zasobów/scenariuszy nieopartych na zaopatrzeniu
description: Ten temat zawiera informacje o typie wdrożenia, Project Operations dla scenariuszy opartych na zasobach / niezamieszczonych.
author: rumant
manager: Annbe
ms.date: 11/02/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 035ad22d2b51182c11e5c29d35f74f499fc903d5
ms.sourcegitcommit: d33ef0ae39f90fe3b0f6b4524f483e8052057361
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 11/03/2020
ms.locfileid: "4365573"
---
# <a name="project-operations-for-resourcenon-stocked-based-scenarios-deployment-overview"></a><span data-ttu-id="bba42-103">Omówienie wdrożenia aplikacji Project Operations dla zasobów/scenariuszy nieopartych na zaopatrzeniu</span><span class="sxs-lookup"><span data-stu-id="bba42-103">Project Operations for resource/non-stocked based scenarios deployment overview</span></span>

<span data-ttu-id="bba42-104">_**Zastosowane do:** Project Operations dla zasobów/scenariuszy nieopartych na zaopatrzeniu_</span><span class="sxs-lookup"><span data-stu-id="bba42-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="bba42-105">Typ wdrożenia, Dynamics 365 Project Operations dla scenariuszy opartych na zasobach / braku zapasów, ma następujące możliwości dla firm opartych na projektach:</span><span class="sxs-lookup"><span data-stu-id="bba42-105">The deployment type, Dynamics 365 Project Operations for resource/non-stocked based scenarios has the following capabilities for project-based companies:</span></span>

- <span data-ttu-id="bba42-106">Planowanie projektów przy użyciu programu Microsoft Project dla sieci Web</span><span class="sxs-lookup"><span data-stu-id="bba42-106">Project planning using Microsoft Project for the Web</span></span>
- <span data-ttu-id="bba42-107">Wielowymiarowa kalkulacja cen i wycena zasobów na robociznę</span><span class="sxs-lookup"><span data-stu-id="bba42-107">Multi-dimensional pricing and costing for labor resources</span></span>
- <span data-ttu-id="bba42-108">Wycena oparta na kategoriach dla kategorii wydatków</span><span class="sxs-lookup"><span data-stu-id="bba42-108">Category-based pricing for expense categories</span></span>
- <span data-ttu-id="bba42-109">Zarządzanie sprzedażą oparte na projektach przy użyciu funkcji Dynamics 365 Sales</span><span class="sxs-lookup"><span data-stu-id="bba42-109">Project-based sales management using Dynamics 365 Sales capabilities</span></span>
- <span data-ttu-id="bba42-110">Universal resource scheduling integruje się z innymi aplikacjami, takimi jak Dynamics 365 Field Service i Dynamics 365 Customer Service</span><span class="sxs-lookup"><span data-stu-id="bba42-110">Universal resource scheduling that integrates with other applications such as Dynamics 365 Field Service and Dynamics 365 Customer Service</span></span>
- <span data-ttu-id="bba42-111">Postęp projektu i śledzenie czasu</span><span class="sxs-lookup"><span data-stu-id="bba42-111">Project progress and Time Tracking</span></span>
- <span data-ttu-id="bba42-112">Podstawowe i pełne funkcje zarządzania wydatkami dla kosztów projektów i innych niż Project, w tym również przechwytywania odbioru za pomocą funkcji OCR</span><span class="sxs-lookup"><span data-stu-id="bba42-112">Basic and full Expense management experiences for project and non-project expenses including receipt capture using OCR capabilities</span></span>
- <span data-ttu-id="bba42-113">Fakturowania, które rozciągają się od formularza do klienta i są podparte dodziałaniem podatku dla przedsiębiorstwa i systemu wymiany walut z datami i rzeczywistą stawką.</span><span class="sxs-lookup"><span data-stu-id="bba42-113">Invoicing that extends from proforma to customer-facing and is backed by an enterprise-class sales tax and date-effective exchange rate system.</span></span>
- <span data-ttu-id="bba42-114">Konfigurowalny koszt projektu, profile przychodu i reguły księgowania pracy w trakcie wykonywania (PWT) i naliczania</span><span class="sxs-lookup"><span data-stu-id="bba42-114">Configurable project cost, revenue profiles, and rules for work in progress (WIP) accounting and accruals</span></span>
- <span data-ttu-id="bba42-115">Rozpoznawanie przychodów z projektu</span><span class="sxs-lookup"><span data-stu-id="bba42-115">Project revenue recognition</span></span>
- <span data-ttu-id="bba42-116">Rozszerzalności dzięki Power Platform</span><span class="sxs-lookup"><span data-stu-id="bba42-116">Extensibility through the Power Platform</span></span>

<span data-ttu-id="bba42-117">Ten typ wdrożenia zapewnia rozszerzenie funkcjonalności zapewnianej przez aplikacje Dynamics 365 Finance i Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="bba42-117">This deployment type provides an extension to the functionality provided by Dynamics 365 Finance and Dynamics 365 Supply Chain Management applications.</span></span>

<span data-ttu-id="bba42-118">To wdrożenie powinno zostać wybrane, ponieważ oczekuje się, że Project Operations będą wykorzystywać pełny cykl życia projektu, który obejmuje następujące wymagania:</span><span class="sxs-lookup"><span data-stu-id="bba42-118">This deployment should be chosen the expectation of Project Operations is to use the full project lifecycle that includes the following requirements:</span></span>

- <span data-ttu-id="bba42-119">Możliwość zarządzania sprzedażą opartą na projektach z innymi typami sprzedaży przy użyciu możliwości aplikacji Sales.</span><span class="sxs-lookup"><span data-stu-id="bba42-119">Ability to manage project-based sales with other types of sales using the capabilities in the Sales application.</span></span>
- <span data-ttu-id="bba42-120">Zintegrowany system zarządzania projektami, który zarządza wewnętrznymi i płatnymi projektami w zakresie harmonogramów i finansów, od sprzedaży projektów po księgowość.</span><span class="sxs-lookup"><span data-stu-id="bba42-120">An integrated project management system that manages internal and billable projects for schedules and financials from project sales to accounting.</span></span>
- <span data-ttu-id="bba42-121">System zarządzania wydatkami zawierający wymuszanie polis i zwrot kosztów w celu śledzenia wydatków na projekty i poza projektem.</span><span class="sxs-lookup"><span data-stu-id="bba42-121">An expense management system that includes policy enforcements and reimbursements for tracking project and non-project expenses.</span></span>
- <span data-ttu-id="bba42-122">Konieczne jest rozbudowany, wieloklasowy i dwukursowy aparat do generowania faktur dostępnych dla klienta w celu tworzenia projektów.</span><span class="sxs-lookup"><span data-stu-id="bba42-122">Require a rich, enterprise-class sales tax and exchange rate engine to generate customer-facing invoices for projects.</span></span>
- <span data-ttu-id="bba42-123">System księgowania projektów i rozpoznawania przychodów zgodny z Międzynarodowymi Standardami Sprawozdawczości Finansowej (Financial Reporting Standards - MSSF).</span><span class="sxs-lookup"><span data-stu-id="bba42-123">An International Financial Reporting Standards(IFRS)-compliant project accounting and revenue recognition system.</span></span>
- <span data-ttu-id="bba42-124">Aplikacje Finance lub Supply Chain Management oraz integracja transakcji opartych na projektach.</span><span class="sxs-lookup"><span data-stu-id="bba42-124">Finance or Supply Chain Management applications and integration of project-based transactions.</span></span>
