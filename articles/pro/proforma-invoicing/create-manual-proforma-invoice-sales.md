---
title: Tworzenie ręcznej faktury proforma - wersja uproszczona
description: Ta temat zawiera informacje na temat tworzenia ręcznej faktury proforma w Project Operations.
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 5a924de6efc377e28a20e038e7deac04616b95aa
ms.sourcegitcommit: 2b74edd31f38410024a01124c9202a4d94464d04
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/17/2020
ms.locfileid: "4764516"
---
# <a name="create-a-manual-proforma-invoice---lite"></a><span data-ttu-id="1322d-103">Tworzenie ręcznej faktury proforma - wersja uproszczona</span><span class="sxs-lookup"><span data-stu-id="1322d-103">Create a manual proforma invoice - lite</span></span>

<span data-ttu-id="1322d-104">_**Zastosowane w:** Wdrażanie uproszczone — od okazji do faktury pro forma_</span><span class="sxs-lookup"><span data-stu-id="1322d-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="1322d-105">W Dynamics 365 Project Operations, faktury proforma mogą być tworzone ręcznie, zgodnie z potrzebami.</span><span class="sxs-lookup"><span data-stu-id="1322d-105">In Dynamics 365 Project Operations, proforma invoices can be created manually as needed.</span></span> <span data-ttu-id="1322d-106">Fakturę proforma można utworzyć ręcznie na stronie list **Kontraktów projektu** lub na stronie szczegółów **Kontraktów projektu**.</span><span class="sxs-lookup"><span data-stu-id="1322d-106">You can manually create a proforma invoice from the **Project Contracts** list page or from the **Project Contract** details page.</span></span>

##  <a name="project-contracts-list-page"></a><span data-ttu-id="1322d-107">Strona list Kontraktów projektu</span><span class="sxs-lookup"><span data-stu-id="1322d-107">Project Contracts list page</span></span>

<span data-ttu-id="1322d-108">Z poziomu strony listy **Kontraktów projektu** wybierz co najmniej jeden kontrakt projektu i utwórz faktury dla wszystkich wybranych rekordów.</span><span class="sxs-lookup"><span data-stu-id="1322d-108">From **Project Contracts** list page, select one or more project contracts, and create invoices for all of the selected records.</span></span>

<span data-ttu-id="1322d-109">System sprawdzi, który z wybranych kontraktów projektu ma zaległości typu **Gotowe do fakturowania** datowane przed dzisiejszą datą.</span><span class="sxs-lookup"><span data-stu-id="1322d-109">The system checks to see which of the selected project contracts has a **Ready to Invoice** backlog dated before today's date.</span></span> <span data-ttu-id="1322d-110">Na bazie tych kontraktów system tworzy projekt faktury proforma.</span><span class="sxs-lookup"><span data-stu-id="1322d-110">From those contracts, the system creates draft proforma invoices.</span></span> <span data-ttu-id="1322d-111">Jeśli kontrakt dotyczący projektu ma wielu klientów, dla każdego klienta zostanie utworzona faktura, a wiele faktur zostanie utworzonych na kontrakt projektu.</span><span class="sxs-lookup"><span data-stu-id="1322d-111">If a project contract has multiple customers, there may be one invoice created per customer, and multiple invoices per project contract.</span></span>

<span data-ttu-id="1322d-112">Wszystkie utworzone faktury projektu są dostępne na stronie **Faktura** w sekcji **Fakturowanie** w obszarze **Sprzedaż**.</span><span class="sxs-lookup"><span data-stu-id="1322d-112">All of the created project invoices are available on the **Invoice** page in the **Billing** section of the **Sales** area.</span></span>

## <a name="project-contract-details-page"></a><span data-ttu-id="1322d-113">Strona szczegółów Kontraktu projektu</span><span class="sxs-lookup"><span data-stu-id="1322d-113">Project Contract details page</span></span>

<span data-ttu-id="1322d-114">Fakturę proforma można również utworzyć na stronie szczegółów **Kontrakt projektu**.</span><span class="sxs-lookup"><span data-stu-id="1322d-114">A proforma invoice can also be created from the **Project Contract** details page.</span></span> <span data-ttu-id="1322d-115">System weryfikuje, czy umowa w sprawie projektu zawiera zaległości typu **Gotowe do fakturowania** datowane przed dzisiejszą datą.</span><span class="sxs-lookup"><span data-stu-id="1322d-115">The system verifies the project contract has a **Ready to Invoice** backlog dated before today's date.</span></span> <span data-ttu-id="1322d-116">Na bazie tychże kontraktów system tworzy faktury proforma w wersji roboczej na podstawie liczby klientów w każdej pozycji kontraktu.</span><span class="sxs-lookup"><span data-stu-id="1322d-116">From these contracts, the system creates draft proforma invoices based on the number of customers on each contract line.</span></span>

<span data-ttu-id="1322d-117">W przypadku utworzenia jednej faktury proforma zostanie otwarta strona **Faktura**.</span><span class="sxs-lookup"><span data-stu-id="1322d-117">When there's a single proforma invoice created, the **Invoice** page opens.</span></span> <span data-ttu-id="1322d-118">Jeśli dla tej umowy dotyczącej projektu zostanie utworzonych wiele faktur, zostanie otwarta strona z listą **Faktur**, na której będą widoczne wszystkie utworzone faktury.</span><span class="sxs-lookup"><span data-stu-id="1322d-118">If multiple invoices are created for that project contract, the **Invoices** list page opens to show all of the created invoices.</span></span>
