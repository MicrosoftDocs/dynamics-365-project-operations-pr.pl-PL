---
title: Nowości i zmiany w programie Project Service Automation, wydanie 13, wer. 3
description: W tym temacie przedstawiono informacje na temat nowości w aktualizacji usługi Project Service Automation, wydanie 13, wer. 3.
author: ruhercul
manager: kfend
ms.service: business-applications
ms.custom: dyn365-projectservice
ms.date: 02/04/2020
ms.topic: article
ms.prod: ''
ms.technology: Microsoft Dynamics 365 Project Service Automation 3.x
ms.assetid: c6f6a5b6-b5bb-467c-b7c7-7fb962504c6d
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 5f1b6b3879c94a77ab62082aad1e470a3ba66552
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/24/2020
ms.locfileid: "3754325"
---
# <a name="project-service-automation-v3-update-release-13"></a><span data-ttu-id="fc908-103">Project Service Automation, wer. 3, wydanie 13</span><span class="sxs-lookup"><span data-stu-id="fc908-103">Project Service Automation V3, Update Release 13</span></span>
<span data-ttu-id="fc908-104">Mamy przyjemność przedstawić najnowszą aktualizację dotyczącą aplikacji Dynamics 365 Project Service Automation (PSA).</span><span class="sxs-lookup"><span data-stu-id="fc908-104">We’re pleased to announce the latest update for the Dynamics 365 Project Service Automation (PSA) application.</span></span> <span data-ttu-id="fc908-105">To wydanie obejmuje znaczną poprawę jakości, wydajności i użyteczności.</span><span class="sxs-lookup"><span data-stu-id="fc908-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="fc908-106">To wydanie jest zgodne z systemem Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="fc908-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="fc908-107">Aby zaktualizować do tej wersji, odwiedź Centrum administracyjne programu Dynamics 365 online i przejdź na stronę rozwiązań, aby zainstalować aktualizację.</span><span class="sxs-lookup"><span data-stu-id="fc908-107">To update to this release, visit the Admin Center for Dynamics 365 online, and go to the solutions page to install the update.</span></span> <span data-ttu-id="fc908-108">By uzyskać więcej informacji, zobacz [Instalowanie, aktualizowanie lub usuwanie preferowanego rozwiązania](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="fc908-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="fc908-109">W tym temacie przedstawiono funkcje i poprawki, które są nowe lub zostały zmienione w programie Project Service Automation, wer. 3, aktualizacja 13.</span><span class="sxs-lookup"><span data-stu-id="fc908-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 13.</span></span> <span data-ttu-id="fc908-110">Numer tej kompilacji to V3.10.3.18 i jest on dostępny w następującym harmonogramie:</span><span class="sxs-lookup"><span data-stu-id="fc908-110">This version has a build number of V3.10.3.18 and is available on the following schedule:</span></span>

- <span data-ttu-id="fc908-111">**Powszechne udostępnienie (samoaktualizacja):** listopad 2019</span><span class="sxs-lookup"><span data-stu-id="fc908-111">**General availability (self-update):** November 2019</span></span>
- <span data-ttu-id="fc908-112">**Automatyczna aktualizacja:** grudzień 2019</span><span class="sxs-lookup"><span data-stu-id="fc908-112">**Auto-update:** December 2019</span></span>


## <a name="update-release-13"></a><span data-ttu-id="fc908-113">Wydanie 13</span><span class="sxs-lookup"><span data-stu-id="fc908-113">Update Release 13</span></span> 

### <a name="bug-fixes"></a><span data-ttu-id="fc908-114">Poprawki błędów</span><span class="sxs-lookup"><span data-stu-id="fc908-114">Bug fixes</span></span>

- <span data-ttu-id="fc908-115">Czas i wydatek</span><span class="sxs-lookup"><span data-stu-id="fc908-115">Time and Expense</span></span>

     - <span data-ttu-id="fc908-116">Naprawione: funkcja wyszukiwania na stronie **zatwierdzania wydatków** nie działa podczas wyszukiwania według przeznaczenia wydatku.</span><span class="sxs-lookup"><span data-stu-id="fc908-116">Fixed: Search functionality on the **Expense approval** page does not work when searching by expense purpose.</span></span>

- <span data-ttu-id="fc908-117">Zarządzanie zasobami</span><span class="sxs-lookup"><span data-stu-id="fc908-117">Resource Management</span></span>

     - <span data-ttu-id="fc908-118">Naprawione: liczby w uzgodnieniu zostały zaktualizowane w celu wyjustowania do prawej.</span><span class="sxs-lookup"><span data-stu-id="fc908-118">Fixed: Numbers in the reconciliation have been updated to be right justified.</span></span>
     - <span data-ttu-id="fc908-119">Naprawione: na karcie **harmonogram** nie można przypisywać nazwanych zasobów do zadań.</span><span class="sxs-lookup"><span data-stu-id="fc908-119">Fixed: Named Resources can't be assigned to tasks through the **Schedule** tab.</span></span>

- <span data-ttu-id="fc908-120">Zarządzanie projektem</span><span class="sxs-lookup"><span data-stu-id="fc908-120">Project Management</span></span>

     - <span data-ttu-id="fc908-121">Naprawione: wyjątek odwołania zerowego podczas przypisywania członka zespołu w przypadku braku informacji konfiguracyjnych **TransactionType** dla **Jednostki** i **DefaultGroup**.</span><span class="sxs-lookup"><span data-stu-id="fc908-121">Fixed: Null reference exception when assigning team member when the **TransactionType** is missing setup information for **Unit** and **DefaultGroup**.</span></span>

- <span data-ttu-id="fc908-122">Sales</span><span class="sxs-lookup"><span data-stu-id="fc908-122">Sales</span></span>

     - <span data-ttu-id="fc908-123">Naprawione: duplikaty rekordów typów transakcji zwracają błąd podczas tworzenia rekordów cen ról.</span><span class="sxs-lookup"><span data-stu-id="fc908-123">Fixed: Duplicate transaction type records return an error when role price records are created.</span></span>
     - <span data-ttu-id="fc908-124">Naprawione: dodatkowe przyciski dla **Nowej szansy sprzedaży**, **Oferty**, **Wiersza oferty** i **Dodania produktu** są widoczne dla poleceń dotyczących szans sprzedaży, ofert, produktów zamówionych i podsiatki wierszy opartych na projekcie.</span><span class="sxs-lookup"><span data-stu-id="fc908-124">Fixed: Extra buttons for **New Opportunity**, **Quote**, **Order Line**, and **Add Product** are visible in commands for Opportunities, Quotes, Order Products, and the project-based Lines sub-grid.</span></span>


