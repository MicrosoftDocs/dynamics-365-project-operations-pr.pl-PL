---
title: Nowości i zmiany w aplikacji Project Service Automation, wydanie 13, wer. 3
description: W tym temacie przedstawiono informacje na temat nowości w aktualizacji usługi Project Service Automation, wydanie 13, wer. 3.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom: dyn365-projectservice
ms.date: 02/04/2020
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
ms.openlocfilehash: 435b70255dd0053a496362c9ced9e742cfcca843
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081972"
---
# <a name="project-service-automation-update-release-13-v3"></a><span data-ttu-id="6d46a-103">Project Service Automation, wydanie 13, wer. 3</span><span class="sxs-lookup"><span data-stu-id="6d46a-103">Project Service Automation Update Release 13, V3</span></span>
<span data-ttu-id="6d46a-104">Mamy przyjemność przedstawić najnowszą aktualizację dotyczącą aplikacji Dynamics 365 Project Service Automation (PSA).</span><span class="sxs-lookup"><span data-stu-id="6d46a-104">We’re pleased to announce the latest update for the Dynamics 365 Project Service Automation (PSA) application.</span></span> <span data-ttu-id="6d46a-105">To wydanie obejmuje znaczną poprawę jakości, wydajności i użyteczności.</span><span class="sxs-lookup"><span data-stu-id="6d46a-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="6d46a-106">To wydanie jest zgodne z systemem Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="6d46a-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="6d46a-107">Aby zaktualizować do tej wersji, odwiedź Centrum administracyjne programu Dynamics 365 online i przejdź na stronę rozwiązań, aby zainstalować aktualizację.</span><span class="sxs-lookup"><span data-stu-id="6d46a-107">To update to this release, visit the Admin Center for Dynamics 365 online, and go to the solutions page to install the update.</span></span> <span data-ttu-id="6d46a-108">By uzyskać więcej informacji, zobacz [Instalowanie, aktualizowanie lub usuwanie preferowanego rozwiązania](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="6d46a-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="6d46a-109">W tym temacie przedstawiono funkcje i poprawki, które są nowe lub zostały zmienione w programie Project Service Automation, wer. 3, aktualizacja 13.</span><span class="sxs-lookup"><span data-stu-id="6d46a-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 13.</span></span> <span data-ttu-id="6d46a-110">Numer tej kompilacji to V3.10.3.18 i jest on dostępny w następującym harmonogramie:</span><span class="sxs-lookup"><span data-stu-id="6d46a-110">This version has a build number of V3.10.3.18 and is available on the following schedule:</span></span>

- <span data-ttu-id="6d46a-111">**Powszechne udostępnienie (samoaktualizacja):** listopad 2019</span><span class="sxs-lookup"><span data-stu-id="6d46a-111">**General availability (self-update):** November 2019</span></span>
- <span data-ttu-id="6d46a-112">**Automatyczna aktualizacja:** grudzień 2019</span><span class="sxs-lookup"><span data-stu-id="6d46a-112">**Auto-update:** December 2019</span></span>


## <a name="update-release-13"></a><span data-ttu-id="6d46a-113">Wydanie 13</span><span class="sxs-lookup"><span data-stu-id="6d46a-113">Update Release 13</span></span> 

### <a name="bug-fixes"></a><span data-ttu-id="6d46a-114">Poprawki błędów</span><span class="sxs-lookup"><span data-stu-id="6d46a-114">Bug fixes</span></span>

- <span data-ttu-id="6d46a-115">Czas i wydatek</span><span class="sxs-lookup"><span data-stu-id="6d46a-115">Time and Expense</span></span>

     - <span data-ttu-id="6d46a-116">Naprawione: funkcja wyszukiwania na stronie **zatwierdzania wydatków** nie działa podczas wyszukiwania według przeznaczenia wydatku.</span><span class="sxs-lookup"><span data-stu-id="6d46a-116">Fixed: Search functionality on the **Expense approval** page does not work when searching by expense purpose.</span></span>

- <span data-ttu-id="6d46a-117">Zarządzanie zasobami</span><span class="sxs-lookup"><span data-stu-id="6d46a-117">Resource Management</span></span>

     - <span data-ttu-id="6d46a-118">Naprawione: liczby w uzgodnieniu zostały zaktualizowane w celu wyjustowania do prawej.</span><span class="sxs-lookup"><span data-stu-id="6d46a-118">Fixed: Numbers in the reconciliation have been updated to be right justified.</span></span>
     - <span data-ttu-id="6d46a-119">Naprawione: na karcie **harmonogram** nie można przypisywać nazwanych zasobów do zadań.</span><span class="sxs-lookup"><span data-stu-id="6d46a-119">Fixed: Named Resources can't be assigned to tasks through the **Schedule** tab.</span></span>

- <span data-ttu-id="6d46a-120">Zarządzanie projektem</span><span class="sxs-lookup"><span data-stu-id="6d46a-120">Project Management</span></span>

     - <span data-ttu-id="6d46a-121">Naprawione: wyjątek odwołania zerowego podczas przypisywania członka zespołu w przypadku braku informacji konfiguracyjnych **TransactionType** dla **Jednostki** i **DefaultGroup**.</span><span class="sxs-lookup"><span data-stu-id="6d46a-121">Fixed: Null reference exception when assigning team member when the **TransactionType** is missing setup information for **Unit** and **DefaultGroup**.</span></span>

- <span data-ttu-id="6d46a-122">Sales</span><span class="sxs-lookup"><span data-stu-id="6d46a-122">Sales</span></span>

     - <span data-ttu-id="6d46a-123">Naprawione: duplikaty rekordów typów transakcji zwracają błąd podczas tworzenia rekordów cen ról.</span><span class="sxs-lookup"><span data-stu-id="6d46a-123">Fixed: Duplicate transaction type records return an error when role price records are created.</span></span>
     - <span data-ttu-id="6d46a-124">Naprawione: dodatkowe przyciski dla **Nowej szansy sprzedaży** , **Oferty** , **Wiersza oferty** i **Dodania produktu** są widoczne dla poleceń dotyczących szans sprzedaży, ofert, produktów zamówionych i podsiatki wierszy opartych na projekcie.</span><span class="sxs-lookup"><span data-stu-id="6d46a-124">Fixed: Extra buttons for **New Opportunity** , **Quote** , **Order Line** , and **Add Product** are visible in commands for Opportunities, Quotes, Order Products, and the project-based Lines sub-grid.</span></span>


