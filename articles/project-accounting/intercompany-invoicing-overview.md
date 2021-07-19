---
title: Omówienie faktury międzyfirmowej
description: W tym temacie przedstawiono informacje i przykłady dotyczące fakturowania międzyfirmowego dla projektów.
author: sigitac
ms.date: 11/19/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.custom: intro-internal
ms.openlocfilehash: c1dcf642f79ce64cb83285ac6dc6d7eaf815145c
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/07/2021
ms.locfileid: "6369389"
---
# <a name="intercompany-invoicing-overview"></a><span data-ttu-id="64a5d-103">Omówienie faktury międzyfirmowej</span><span class="sxs-lookup"><span data-stu-id="64a5d-103">Intercompany invoicing overview</span></span>

<span data-ttu-id="64a5d-104">_**Zastosowane do:** Project Operations dla zasobów/scenariuszy nieopartych na zaopatrzeniu_</span><span class="sxs-lookup"><span data-stu-id="64a5d-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="64a5d-105">Organizacja może dysponować wieloma oddziałami, podmiotami zależnymi i innymi firmami, które przekazują sobie produkty i usługi do projektów.</span><span class="sxs-lookup"><span data-stu-id="64a5d-105">Your organization might have multiple divisions, subsidiaries, and other legal entities that transfer products and services to each other for projects.</span></span> <span data-ttu-id="64a5d-106">Podmiot prawny, który dostarcza usługę lub produkt, nosi nazwę *firmy wypożyczającej*.</span><span class="sxs-lookup"><span data-stu-id="64a5d-106">The legal entity that provides the service or product is called the *lending legal entity*.</span></span> <span data-ttu-id="64a5d-107">Podmiot prawny, który otrzymuje usługę lub produkt, nosi nazwę *firmy pożyczającej*.</span><span class="sxs-lookup"><span data-stu-id="64a5d-107">The legal entity that receives the service or product is called the *borrowing legal entity*.</span></span>

<span data-ttu-id="64a5d-108">Poniższa ilustracja przedstawia typowy scenariusz, w którym dwa podmioty prawne, Contoso Robotics USA (podmiot prawny pożyczający) i Contoso Robotics UK (podmiot prawny wypożyczający) dzielą się zasobami w celu realizacji projektu dla klienta, firmy Adventure works.</span><span class="sxs-lookup"><span data-stu-id="64a5d-108">The following illustration shows a typical scenario where two legal entities, Contoso Robotics USA (the borrowing legal entity) and Contoso Robotics UK (the lending legal entity) share resources to deliver a project for the customer, Adventure works.</span></span> <span data-ttu-id="64a5d-109">W tym scenariuszu firma Contoso Robotics USA została zakontraktowana na dostawę robót do Adventure Works.</span><span class="sxs-lookup"><span data-stu-id="64a5d-109">For this scenario, Contoso Robotics USA is contracted to deliver the work to Adventure Works.</span></span>

![Faktura międzyfirmowa](./media/IntercompanyScenario.png) 

<span data-ttu-id="64a5d-111">W aplikacji Dynamics 365 Project Operations do przetwarzania transakcji międzyfirmowych jest używany następujący przepływ:</span><span class="sxs-lookup"><span data-stu-id="64a5d-111">Dynamics 365 Project Operations uses the following flow to process intercompany transactions:</span></span>

1. <span data-ttu-id="64a5d-112">Zasoby z firmy wypożyczającej rejestrują międzyfirmowe transakcje dotyczące czasu lub wydatków, rezerwując czas i wydatki względem projektów w firmie pożyczającej.</span><span class="sxs-lookup"><span data-stu-id="64a5d-112">Resources from the lending legal entity record intercompany time or expense transactions by booking time and expense against projects in the borrowing legal entity.</span></span>
2. <span data-ttu-id="64a5d-113">Koszty związane z czasem i wydatkami są rejestrowane w firmie wypożyczającej przy użyciu listy kosztów własnych firmy pożyczającej.</span><span class="sxs-lookup"><span data-stu-id="64a5d-113">Time and expense costs are recorded in the lending company by using the borrowing company's unit cost price list.</span></span>
3. <span data-ttu-id="64a5d-114">Międzyfirmowe transakcje niezafakturowanej sprzedaży są rejestrowane w firmie wypożyczającej przy użyciu listy kosztów własnych firmy pożyczającej.</span><span class="sxs-lookup"><span data-stu-id="64a5d-114">Intercompany unbilled sale transactions are recorded in the lending company by using the borrowing company's unit cost price list.</span></span>
4. <span data-ttu-id="64a5d-115">Przychód niezafakturowany jest rejestrowany w firmie pożyczającej przy użyciu cennika sprzedaży z kontraktu dotyczącego projektu.</span><span class="sxs-lookup"><span data-stu-id="64a5d-115">Unbilled revenue is recorded in the borrowing company using the project contract sales price list.</span></span> <span data-ttu-id="64a5d-116">Klienta można fakturować podczas rejestrowania niezafakturowanego przychodu.</span><span class="sxs-lookup"><span data-stu-id="64a5d-116">The customer can be billed when unbilled revenue is recorded.</span></span> <span data-ttu-id="64a5d-117">Klient nie musi czekać na zakończenie przetwarzania faktury międzyfirmowej.</span><span class="sxs-lookup"><span data-stu-id="64a5d-117">The customer doesn't have to wait until intercompany invoice processing is complete.</span></span>
5. <span data-ttu-id="64a5d-118">Międzyfirmowe faktury dla klientów są tworzone w sposób okresowy w firmie wypożyczającej.</span><span class="sxs-lookup"><span data-stu-id="64a5d-118">Intercompany customer invoices are created on a periodic basis in the lending company.</span></span> <span data-ttu-id="64a5d-119">Faktury są tworzone ręcznie lub przy użyciu zautomatyzowanego procesu okresowego.</span><span class="sxs-lookup"><span data-stu-id="64a5d-119">The invoices are created manually or by using a periodic automated process.</span></span> <span data-ttu-id="64a5d-120">Można utworzyć jedną fakturę dla każdej firmy pożyczającej lub oddzielne faktury mogą być tworzone w ramach projektu.</span><span class="sxs-lookup"><span data-stu-id="64a5d-120">A single invoice can be created for each borrowing legal entity or separate invoices can be created by project.</span></span>
6. <span data-ttu-id="64a5d-121">Gdy międzyfirmowa faktura dla klienta jest księgowana w firmie wypożyczającej, równocześnie w firmie pożyczającej jest tworzona odpowiadająca jej oczekująca faktura od dostawcy.</span><span class="sxs-lookup"><span data-stu-id="64a5d-121">When the intercompany customer invoice is posted in the lending legal entity, the corresponding pending vendor invoice is created in the borrowing legal entity.</span></span> <span data-ttu-id="64a5d-122">Koszty na oczekującej fakturze od dostawcy będą rejestrowane w księdze podrzędnej projektu podczas księgowania faktury.</span><span class="sxs-lookup"><span data-stu-id="64a5d-122">The costs in the pending vendor invoice will be recorded to the project subledger when the invoice is posted.</span></span>

<span data-ttu-id="64a5d-123">Na poniższym diagramie przedstawiono fakturowanie międzyfirmowe w zależności od zdarzeń księgowania oraz oczekiwane zapisy księgowe w księdze głównej.</span><span class="sxs-lookup"><span data-stu-id="64a5d-123">The following diagram illustrates intercompany invoicing as it relates to accounting events and expected postings to the general ledger.</span></span>

![Przepływ międzyfirmowy](./media/IntercompanyFlow.png)

## <a name="additional-resources"></a><span data-ttu-id="64a5d-125">Dodatkowe zasoby</span><span class="sxs-lookup"><span data-stu-id="64a5d-125">Additional resources</span></span>

- [<span data-ttu-id="64a5d-126">Konfigurowanie faktury międzyfirmowej</span><span class="sxs-lookup"><span data-stu-id="64a5d-126">Configure intercompany invoicing</span></span>](configure-intercompany-invoicing.md)
- [<span data-ttu-id="64a5d-127">Rejestrowanie transakcji międzyfirmowych</span><span class="sxs-lookup"><span data-stu-id="64a5d-127">Record intercompany transactions</span></span>](create-intercompany-transactions.md)
- [<span data-ttu-id="64a5d-128">Tworzenie faktur międzyfirmowych dla klienta i dostawcy</span><span class="sxs-lookup"><span data-stu-id="64a5d-128">Create intercompany customer and vendor invoices</span></span>](create-intercompany-customer-vendor-invoices.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]