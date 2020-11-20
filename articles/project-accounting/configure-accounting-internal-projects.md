---
title: Konfigurowanie księgowania projektów wewnętrznych
description: W tym temacie zamieszczono informacje dotyczące sposobu konfigurowania zasad księgowania w odniesieniu do projektów wewnętrznych w Project Operations.
author: sigitac
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: ea04178d4327ccd701ab431f172463a13a55154e
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/28/2020
ms.locfileid: "4132391"
---
# <a name="configure-accounting-for-internal-projects"></a><span data-ttu-id="8d1ec-103">Konfigurowanie księgowania projektów wewnętrznych</span><span class="sxs-lookup"><span data-stu-id="8d1ec-103">Configure accounting for internal projects</span></span>

<span data-ttu-id="8d1ec-104">_**Zastosowane do:** Project Operations dla zasobów/scenariuszy nieopartych na zaopatrzeniu_</span><span class="sxs-lookup"><span data-stu-id="8d1ec-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="8d1ec-105">Projekty wewnętrzne umożliwiają firmom śledzenie kosztów związanych z działaniami, które nie są rozliczane z klientem.</span><span class="sxs-lookup"><span data-stu-id="8d1ec-105">Internal projects allow companies track cost related to activities that aren't being billed to a customer.</span></span> <span data-ttu-id="8d1ec-106">Przykładowe projekty wewnętrzne to między innymi:</span><span class="sxs-lookup"><span data-stu-id="8d1ec-106">Examples of internal projects include:</span></span>

- <span data-ttu-id="8d1ec-107">Opracowywanie produktu, takiego jak aplikacja mobilna oraz śledzenie kosztów związanych z rozwojem projektu.</span><span class="sxs-lookup"><span data-stu-id="8d1ec-107">Developing a product, such as a mobile app, and tracking the cost associated with the development.</span></span>
- <span data-ttu-id="8d1ec-108">Zarządzanie czasem i wydatkami przed sprzedażą.</span><span class="sxs-lookup"><span data-stu-id="8d1ec-108">Managing pre-sale time and expense.</span></span> <span data-ttu-id="8d1ec-109">Projekty wewnętrzne przed sprzedażą można przekonwertować później na projekt rozliczany, jeśli oferta została wykorzystana.</span><span class="sxs-lookup"><span data-stu-id="8d1ec-109">This pre-sale internal project can be converted later to a billable project if quote is won.</span></span>

<span data-ttu-id="8d1ec-110">Każdy projekt nieskojarzony z kontraktem w Dynamics 365 Project Operations jest traktowany jako wewnętrzny.</span><span class="sxs-lookup"><span data-stu-id="8d1ec-110">Any project not associated with a contract in Dynamics 365 Project Operations is treated as internal.</span></span> <span data-ttu-id="8d1ec-111">Reguły kosztów projektu i profili przychodów nie określają reguły księgowania transakcji dla tego projektu.</span><span class="sxs-lookup"><span data-stu-id="8d1ec-111">Project cost and revenue profiles aren't used to determine accounting rules for the project.</span></span> <span data-ttu-id="8d1ec-112">Koszt projektu wewnętrznego jest zawsze księgowany przy użyciu reguł zysków i strat.</span><span class="sxs-lookup"><span data-stu-id="8d1ec-112">Internal project cost is always posted using profit and loss principles.</span></span> <span data-ttu-id="8d1ec-113">Konta księgowe na potrzeby księgowania są definiowane na stronie **Konfiguracja księgowania w rejestrze**.</span><span class="sxs-lookup"><span data-stu-id="8d1ec-113">Ledger accounts for postings are defined on the **Ledger posting setup** page.</span></span>

- <span data-ttu-id="8d1ec-114">Transakcje czasowe są księgowane: obciążenia na koncie **Kosztów**, a uznania na koncie **Alokacja płac**.</span><span class="sxs-lookup"><span data-stu-id="8d1ec-114">Time transactions are posted by debiting the **Cost** account and crediting the **Payroll allocation** account.</span></span>
- <span data-ttu-id="8d1ec-115">Transakcje wydatkowe są księgowane: obciążenia na koncie **Kosztów**, a uznania na koncie **rozliczeniowym dla wydatku**.</span><span class="sxs-lookup"><span data-stu-id="8d1ec-115">Expense transactions are posted by debiting the **Cost** account and crediting the **Offset account for expense**.</span></span>

<span data-ttu-id="8d1ec-116">Jeśli projekt jest skojarzony z kontraktem projektu po zaksięgowaniu transakcji, system cofnie wszystkie transakcje skumulowane i tworzy nowe transakcje fakturowania.</span><span class="sxs-lookup"><span data-stu-id="8d1ec-116">After transactions are posted to the project, if the project is associated with a project contract, the system reverses all accumulated transactions and creates new billable transactions.</span></span> <span data-ttu-id="8d1ec-117">Transakcje podlegające rozliczaniu podążają za regułami księgowania zdefiniowanymi w odpowiednim profilu kosztów projektów i przychodów.</span><span class="sxs-lookup"><span data-stu-id="8d1ec-117">The billable transactions follow the accounting rules defined in respective Project cost and revenue profile.</span></span>


