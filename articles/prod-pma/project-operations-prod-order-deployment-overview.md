---
title: Omówienie wdrożenia aplikacji Project Operations dla scenariuszy obejmujących magazynowanie/opartych na produkcji
description: Ten temat zawiera informacje o typie wdrożenia, Project Operations dla scenariuszy opartych na zasobach / produkcji.
author: rumant
manager: Annbe
ms.date: 11/02/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 7bad4de10a508f0c1aa2cc6bb0c41081f81fb259
ms.sourcegitcommit: d33ef0ae39f90fe3b0f6b4524f483e8052057361
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 11/03/2020
ms.locfileid: "4365576"
---
# <a name="project-operations-for-stockedproduction-based-scenarios-deployment-overview"></a><span data-ttu-id="510b6-103">Omówienie wdrożenia aplikacji Project Operations dla scenariuszy obejmujących magazynowanie/opartych na produkcji</span><span class="sxs-lookup"><span data-stu-id="510b6-103">Project Operations for stocked/production-based scenarios deployment overview</span></span>

<span data-ttu-id="510b6-104">_**Dotyczy:** Project Operations dla scenariuszy obejmujących magazynowanie/zlecenia produkcyjne_</span><span class="sxs-lookup"><span data-stu-id="510b6-104">_**Applies To:** Project Operations for stocked/production-based scenarios_</span></span>


<span data-ttu-id="510b6-105">Ten typ wdrożenia ma następujące możliwości dla firm opartych na projektach:</span><span class="sxs-lookup"><span data-stu-id="510b6-105">This deployment type has the following capabilities for project-based companies:</span></span>

- <span data-ttu-id="510b6-106">Planowanie projektów przy użyciu [Struktur podziału prac](work-breakdown-structures.md)</span><span class="sxs-lookup"><span data-stu-id="510b6-106">Project planning using the [Work breakdown structures](work-breakdown-structures.md)</span></span>
- <span data-ttu-id="510b6-107">Pozyskiwanie i korzystanie z zapasów magazynowych dla projektów</span><span class="sxs-lookup"><span data-stu-id="510b6-107">Procure and consume stocked inventory for projects</span></span>
- <span data-ttu-id="510b6-108">Zarządzanie sprzedażą opartą na projektach przy użyciu modułu **Sprzedaży i marketingu** w aplikacjach Dynamics 365 Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="510b6-108">Managing project-based sales using the **Sales and marketing** module in Dynamics 365 Finance and Operations apps</span></span>
- <span data-ttu-id="510b6-109">Kalkulacja cen i kosztów projektu przy użyciu konfiguracji stawek kosztów i stawki rachunku w aplikacjach Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="510b6-109">Project pricing and costing using the cost rate and bill rate configurations in Finance and Operations apps</span></span>
- <span data-ttu-id="510b6-110">Zarządzanie zasobami dla projektów w aplikacjach Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="510b6-110">Resource management for projects in Finance and Operations apps</span></span>
- <span data-ttu-id="510b6-111">Postęp projektu i śledzenie czasu w aplikacjach Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="510b6-111">Project progress and time tracking in Finance and Operations apps</span></span>
- <span data-ttu-id="510b6-112">Funkcje zarządzania wydatkami dla kosztów projektów i innych niż Project, w tym również przechwytywania odbioru za pomocą funkcji OCR</span><span class="sxs-lookup"><span data-stu-id="510b6-112">Expense management experiences for project and non-project expenses with receipt capture using OCR capabilities</span></span>
- <span data-ttu-id="510b6-113">Fakturowanie z wykorzystaniem podatku od sprzedaży klasy korporacyjnej i systemu kursów wymiany walut</span><span class="sxs-lookup"><span data-stu-id="510b6-113">Invoicing using an enterprise-class sales tax and date-effective exchange rates system</span></span>
- <span data-ttu-id="510b6-114">Grupy projektów z konfigurowalnymi na potrzeby księgowania PWT i naliczania</span><span class="sxs-lookup"><span data-stu-id="510b6-114">Configurable project groups for WIP accounting and accruals</span></span>
- <span data-ttu-id="510b6-115">Rozpoznawanie przychodów z projektu</span><span class="sxs-lookup"><span data-stu-id="510b6-115">Project revenue recognition</span></span>

<span data-ttu-id="510b6-116">Ten typ wdrożenia zapewnia rozszerzenie funkcjonalności zapewnianej przez aplikacje Dynamics 365 Finance i Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="510b6-116">This deployment type also provides an extension to the functionality provided by the Dynamics 365 Finance and Dynamics 365 Supply Chain Management applications.</span></span>

<span data-ttu-id="510b6-117">Wybierz ten typ wdrożenia, aby używać Dynamics 365 Project Operations przez cały cykl życia projektu, w tym następujące kluczowe wymagania:</span><span class="sxs-lookup"><span data-stu-id="510b6-117">Select this deployment type to use Dynamics 365 Project Operations for the full project lifecycle, including the following key requirements:</span></span>

- <span data-ttu-id="510b6-118">Rozległy system zarządzania projektami, który zarządza podlegającymi inwentaryzacją kosztami i zadaniami zlecenia produkcyjnego w odniesieniu do wewnętrznego i zafakturowanego projektu dotyczącego zestawień i finansów.</span><span class="sxs-lookup"><span data-stu-id="510b6-118">An extensive Project management system that manages inventoried items and job/production order costing for internal and billable projects for schedules and financials.</span></span>
- <span data-ttu-id="510b6-119">Organizacja ma już Dynamics 365 Finance lub Dynamics 365 Supply Chain i Manufacturing integrowanie transakcji opartych na projektach będzie uprościć dostęp do danych oraz potrzeby raportowania.</span><span class="sxs-lookup"><span data-stu-id="510b6-119">The organization already has Dynamics 365 Finance or Dynamics 365 Supply Chain and Manufacturing apps and integrating project-based transactions will simplify data access and reporting needs.</span></span>
- <span data-ttu-id="510b6-120">W pełni funkcjonalny system zarządzania wydatkami, który obejmuje egzekwowanie zasad i zwrot kosztów za śledzenie wydatków związanych z projektami i innymi niż projektami.</span><span class="sxs-lookup"><span data-stu-id="510b6-120">A fully functional Expense management system that includes policy enforcements and reimbursements for tracking project and non-project expenses.</span></span>
- <span data-ttu-id="510b6-121">Wieloklasowy i dwukursowy aparat do generowania faktur dostępnych dla klienta w celu tworzenia projektów.</span><span class="sxs-lookup"><span data-stu-id="510b6-121">An enterprise-class sales tax and exchange rate engine to generate customer-facing invoices for projects.</span></span>
- <span data-ttu-id="510b6-122">System księgowania projektów i rozpoznawania przychodów zgodny z Międzynarodowymi Standardami Sprawozdawczości Finansowej (Financial Reporting Standards - MSSF).</span><span class="sxs-lookup"><span data-stu-id="510b6-122">An International Financial Reporting Standards(IFRS)-compliant project accounting and revenue recognition system.</span></span>

