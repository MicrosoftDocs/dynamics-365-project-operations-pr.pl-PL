---
title: Project Operations — integracja podwójnego zapisu
description: Ten temat umożliwia omówienie integracji podwójnego zapisu w Project Operations.
author: sigitac
ms.date: 04/28/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.custom: intro-internal
ms.openlocfilehash: 540b6f74d8e79116e5fdb2ceffaa4bbb487ff08f
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/07/2021
ms.locfileid: "6368444"
---
# <a name="project-operations-dual-write-integration-overview"></a><span data-ttu-id="b7ec9-103">Omówienie: Project Operations — integracja podwójnego zapisu</span><span class="sxs-lookup"><span data-stu-id="b7ec9-103">Project Operations dual-write integration overview</span></span>

<span data-ttu-id="b7ec9-104">_**Zastosowane do:** Project Operations dla zasobów/scenariuszy nieopartych na zaopatrzeniu_</span><span class="sxs-lookup"><span data-stu-id="b7ec9-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="b7ec9-105">Project Operations używa [funkcji podwójnego zapisu](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page) do synchronizowania danych między Microsoft Dataverse i Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="b7ec9-105">Project Operations uses [dual-write capabilities](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page) to synchronize data across Microsoft Dataverse and Dynamics 365 Finance.</span></span>

<span data-ttu-id="b7ec9-106">Na poniższym rysunku pokazano, jak są synchronizowane dane w ramach integracji między Dataverse a Finance.</span><span class="sxs-lookup"><span data-stu-id="b7ec9-106">The following illustration shows how data is synchronized as part of this integration between Dataverse and Finance.</span></span>

![Omówienie przepływów danych Project Operations](./media/ProjectOperationsFlows.jpg)

<span data-ttu-id="b7ec9-108">Project Operations w Dataverse zapewnia nowoczesny interfejs użytkownika (UI) i łatwą rozszerzalność bez kodu/niskokodowo z wykorzystaniem możliwości Power Platform.</span><span class="sxs-lookup"><span data-stu-id="b7ec9-108">Project Operations on Dataverse provides a modern user interface (UI) and easy no-code/low-code extensibility using Power Platform capabilities.</span></span> <span data-ttu-id="b7ec9-109">Menedżerowie projektów, menedżerowie zasobów, członkowie zespołu projektu i inne osoby front office mogą wykonywać swoje działania Project Operations w Dataverse.</span><span class="sxs-lookup"><span data-stu-id="b7ec9-109">Project managers, Resource managers, Project team members, and other front-office personas, perform their activities in Project Operations on Dataverse.</span></span>

<span data-ttu-id="b7ec9-110">Project Operations w Finanse umożliwia obsługę księgowych projektów i rozpoznawanie przychodów.</span><span class="sxs-lookup"><span data-stu-id="b7ec9-110">Project Operations in Finance provides project accounting and revenue recognition support.</span></span> <span data-ttu-id="b7ec9-111">Project Operations włącza się do struktury finansowej w Finance na potrzeby obliczania podatku, kursów wymiany walut, raportowania rozmiarów finansowych itp.</span><span class="sxs-lookup"><span data-stu-id="b7ec9-111">Project Operations plugs in to the financial framework in Finance for sales tax calculation, currency exchange rates, financial dimension reporting, and more.</span></span> <span data-ttu-id="b7ec9-112">Środowisko obsługi klienta projektu w większości jest oparte na Finance.</span><span class="sxs-lookup"><span data-stu-id="b7ec9-112">The Project accountant experiences are mostly based in Finance.</span></span>

<span data-ttu-id="b7ec9-113">Integracja Project Operations składa się z następującej integracji składników:</span><span class="sxs-lookup"><span data-stu-id="b7ec9-113">Project Operations integration consists of the following component integration:</span></span>


- [<span data-ttu-id="b7ec9-114">Integracja danych instalacji i konfiguracji aplikacji Project Operations</span><span class="sxs-lookup"><span data-stu-id="b7ec9-114">Project Operations setup and configuration data integration</span></span>](resource-dual-write-setup-integration.md) 
- [<span data-ttu-id="b7ec9-115">Szacowania projektu i wartości rzeczywistych</span><span class="sxs-lookup"><span data-stu-id="b7ec9-115">Project estimates and actuals</span></span>](resource-dual-write-estimates-actuals.md)
- [<span data-ttu-id="b7ec9-116">Faktury projektu</span><span class="sxs-lookup"><span data-stu-id="b7ec9-116">Project invoices</span></span>](resource-dual-write-project-invoice.md)
- [<span data-ttu-id="b7ec9-117">Zarządzanie wydatkami</span><span class="sxs-lookup"><span data-stu-id="b7ec9-117">Expense management</span></span>](resource-dual-write-expense.md)
- [<span data-ttu-id="b7ec9-118">Faktura od dostawcy</span><span class="sxs-lookup"><span data-stu-id="b7ec9-118">Vendor invoice</span></span>](resource-dual-write-vendor-invoice.md)
