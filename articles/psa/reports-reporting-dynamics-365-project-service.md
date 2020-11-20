---
title: Strona główna raportowania
description: Ten temat zawiera informacje o raportowaniu w programie Dynamics 365 Project Service Automation.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: e1a645b157c56066e56b22ea8cf0324fbc1ddd2c
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/28/2020
ms.locfileid: "4120331"
---
# <a name="reporting-home-page"></a><span data-ttu-id="4d25d-103">Strona główna raportowania</span><span class="sxs-lookup"><span data-stu-id="4d25d-103">Reporting home page</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="4d25d-104">Program Microsoft Dynamics 365 Project Service Automation umożliwia organizacjom działającym poprzez realizowanie projektów skuteczne zarządzanie bieżącymi operacjami.</span><span class="sxs-lookup"><span data-stu-id="4d25d-104">Microsoft Dynamics 365 Project Service Automation lets project-based organizations efficiently manage the operations of their business.</span></span> <span data-ttu-id="4d25d-105">W każdym projekcie członkowie zespołu muszą zarządzać szansami sprzedaży, sporządzać oferty, planować pracę, pozyskiwać zasoby do projektów, zarządzać pracą według planu, rozliczać pracę oraz wykonywać pracę w celu zrealizowania projektu.</span><span class="sxs-lookup"><span data-stu-id="4d25d-105">On any project, team members must manage the opportunity, quote and plan the work, resource the projects, manage the work according to the plan, bill for the work, and then do the work to complete the project.</span></span> <span data-ttu-id="4d25d-106">Zdolność tworzenia raportów z operacji ma kluczowe znaczenie dla określenia kondycji organizacji i możliwości podjęcia koniecznych działań naprawczych.</span><span class="sxs-lookup"><span data-stu-id="4d25d-106">The ability to report on operations is key to determining the health of the organization and taking any corrective action that's required.</span></span> <span data-ttu-id="4d25d-107">Do swoich wszystkich funkcji sprawozdawczych program PSA wykorzystuje metody i technologie raportowania systemu Microsoft Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="4d25d-107">PSA uses Microsoft Dynamics 365 reporting methods and technologies for all its reporting.</span></span> <span data-ttu-id="4d25d-108">Aby uzyskać więcej informacji na temat opcji raportowania, zobacz [Przewodnik po pisaniu raportu dla programu Dynamics 365 Customer Engagement (on-premises), wersja 9](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/analytics/reporting-analytics-with-dynamics-365).</span><span class="sxs-lookup"><span data-stu-id="4d25d-108">For more information about the options for reporting, see the [Report writing guide for Dynamics 365 Customer Engagement (on-premises), version 9](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/analytics/reporting-analytics-with-dynamics-365).</span></span>

## <a name="report-wizard"></a><span data-ttu-id="4d25d-109">Kreator raportów</span><span class="sxs-lookup"><span data-stu-id="4d25d-109">Report Wizard</span></span>

<span data-ttu-id="4d25d-110">Kreator raportów pozwala tworzyć proste raporty osobom, które nie są informatykami.</span><span class="sxs-lookup"><span data-stu-id="4d25d-110">The Report Wizard lets non-developers create simple reports.</span></span> <span data-ttu-id="4d25d-111">Ponieważ aplikacja jest zbudowana na istniejącej platformie, jej działanie jest takie samo jak opisane w temacie [Tworzenie i edytowanie raportu przy użyciu Kreatora raportów](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/basics/create-edit-copy-report-wizard).</span><span class="sxs-lookup"><span data-stu-id="4d25d-111">Because the app is built on an existing platform, the experience is the same as the experience that is documented in [Create or edit a report using the Report Wizard](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/basics/create-edit-copy-report-wizard).</span></span> <span data-ttu-id="4d25d-112">Będziesz jednak używać encji specyficznych dla rozwiązania Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="4d25d-112">However, you will use the Project Service Automation-specific entities.</span></span>

## <a name="custom-sql-server-reporting-services-reports"></a><span data-ttu-id="4d25d-113">Niestandardowe raporty usługi SQL Server Reporting Services</span><span class="sxs-lookup"><span data-stu-id="4d25d-113">Custom SQL Server Reporting Services reports</span></span>

<span data-ttu-id="4d25d-114">Jeśli firma wymaga konkretnego raportu, którego nie można utworzyć przy użyciu Kreatora raportów, można utworzyć raport niestandardowy.</span><span class="sxs-lookup"><span data-stu-id="4d25d-114">If your business requires a specific report that can't be created by using the Report Wizard, you can create a custom report.</span></span> <span data-ttu-id="4d25d-115">Na komputerze musi być zainstalowany program Visual Studio Microsoft wraz z odpowiednimi narzędziami Microsoft SQL Server Data Tools i rozszerzeniami Report Authoring.</span><span class="sxs-lookup"><span data-stu-id="4d25d-115">You must have Microsoft Visual Studio installed, together with the appropriate Microsoft SQL Server Data Tools and Report Authoring Extensions.</span></span> <span data-ttu-id="4d25d-116">Aby uzyskać więcej informacji o narzędziach i wersjach, zobacz [Środowisko pisania raportów przy użyciu SQL Server Data Tools](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/analytics/report-writing-environment-using-sql-server-data-tools).</span><span class="sxs-lookup"><span data-stu-id="4d25d-116">For more information about tools and versions, see [Report writing environment using SQL Server Data Tools](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/analytics/report-writing-environment-using-sql-server-data-tools).</span></span> <span data-ttu-id="4d25d-117">Aby uzyskać informacje na temat tworzenia raportu niestandardowego, zobacz [Tworzenie nowego raportu przy użyciu SQL Server Data Tools](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/analytics/create-a-new-report-using-sql-server-data-tools).</span><span class="sxs-lookup"><span data-stu-id="4d25d-117">For information about how to create a custom report, see [Create a new report using SQL Server Data Tools](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/analytics/create-a-new-report-using-sql-server-data-tools).</span></span>

## <a name="power-bi-insights-apps"></a><span data-ttu-id="4d25d-118">Aplikacje Power BI do uzyskiwania wglądu</span><span class="sxs-lookup"><span data-stu-id="4d25d-118">Power BI insights apps</span></span>

<span data-ttu-id="4d25d-119">Wspólnie usługi Microsoft Power BI i Dynamics 365 umożliwiają zaawansowaną pracę z posiadanymi danymi przy użyciu aplikacji wglądu.</span><span class="sxs-lookup"><span data-stu-id="4d25d-119">Together, Microsoft Power BI and Dynamics 365 give you a powerful way to work with your data, in the form of insights apps.</span></span> <span data-ttu-id="4d25d-120">Informacje na temat dostępności aplikacji wglądu można znaleźć na [stronie aplikacji Power BI do uzyskiwania wglądu](https://powerbi.microsoft.com/power-bi-insights-apps/).</span><span class="sxs-lookup"><span data-stu-id="4d25d-120">For information about the availability of insights apps, see the [Power BI insights apps page](https://powerbi.microsoft.com/power-bi-insights-apps/).</span></span>


## <a name="additional-resources"></a><span data-ttu-id="4d25d-121">Dodatkowe zasoby</span><span class="sxs-lookup"><span data-stu-id="4d25d-121">Additional resources</span></span>
<span data-ttu-id="4d25d-122">Więcej informacji na temat sprawozdawczości w programie PSA można znaleźć w następujących tematach:</span><span class="sxs-lookup"><span data-stu-id="4d25d-122">For more information about reporting in PSA, see the following topics:</span></span>

- [<span data-ttu-id="4d25d-123">Praca z modelem danych usługi Project Service</span><span class="sxs-lookup"><span data-stu-id="4d25d-123">Working with the Project Service data model</span></span>](reports-working-project-service-data-model.md)
- [<span data-ttu-id="4d25d-124">Pulpity nawigacyjne</span><span class="sxs-lookup"><span data-stu-id="4d25d-124">Dashboards</span></span>](reports-dashboards.md)
