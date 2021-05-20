---
title: Nowości i zmiany w aplikacji Project Service Automation, wydanie 13, wer. 3
description: W tym temacie przedstawiono informacje na temat nowości w aktualizacji usługi Project Service Automation, wydanie 13, wer. 3.
author: ruhercul
manager: kfend
ms.service: project-operations
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
ms.openlocfilehash: a4ebc2e6ca3f6be0a05a7240d762d7a8cf92d81b
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/27/2021
ms.locfileid: "5949467"
---
# <a name="project-service-automation-update-release-13-v3"></a><span data-ttu-id="ebdbb-103">Project Service Automation, wydanie 13, wer. 3</span><span class="sxs-lookup"><span data-stu-id="ebdbb-103">Project Service Automation Update Release 13, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="ebdbb-104">Mamy przyjemność przedstawić najnowszą aktualizację dotyczącą aplikacji Dynamics 365 Project Service Automation (PSA).</span><span class="sxs-lookup"><span data-stu-id="ebdbb-104">We’re pleased to announce the latest update for the Dynamics 365 Project Service Automation (PSA) application.</span></span> <span data-ttu-id="ebdbb-105">To wydanie obejmuje znaczną poprawę jakości, wydajności i użyteczności.</span><span class="sxs-lookup"><span data-stu-id="ebdbb-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="ebdbb-106">To wydanie jest zgodne z systemem Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="ebdbb-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="ebdbb-107">Aby zaktualizować do tej wersji, odwiedź Centrum administracyjne programu Dynamics 365 online i przejdź na stronę rozwiązań, aby zainstalować aktualizację.</span><span class="sxs-lookup"><span data-stu-id="ebdbb-107">To update to this release, visit the Admin Center for Dynamics 365 online, and go to the solutions page to install the update.</span></span> <span data-ttu-id="ebdbb-108">By uzyskać więcej informacji, zobacz [Instalowanie, aktualizowanie lub usuwanie preferowanego rozwiązania](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="ebdbb-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="ebdbb-109">W tym temacie przedstawiono funkcje i poprawki, które są nowe lub zostały zmienione w programie Project Service Automation, wer. 3, aktualizacja 13.</span><span class="sxs-lookup"><span data-stu-id="ebdbb-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 13.</span></span> <span data-ttu-id="ebdbb-110">Numer tej kompilacji to V3.10.3.18 i jest on dostępny w następującym harmonogramie:</span><span class="sxs-lookup"><span data-stu-id="ebdbb-110">This version has a build number of V3.10.3.18 and is available on the following schedule:</span></span>

- <span data-ttu-id="ebdbb-111">**Powszechne udostępnienie (samoaktualizacja):** listopad 2019</span><span class="sxs-lookup"><span data-stu-id="ebdbb-111">**General availability (self-update):** November 2019</span></span>
- <span data-ttu-id="ebdbb-112">**Automatyczna aktualizacja:** grudzień 2019</span><span class="sxs-lookup"><span data-stu-id="ebdbb-112">**Auto-update:** December 2019</span></span>


## <a name="update-release-13"></a><span data-ttu-id="ebdbb-113">Wydanie 13</span><span class="sxs-lookup"><span data-stu-id="ebdbb-113">Update Release 13</span></span> 

### <a name="bug-fixes"></a><span data-ttu-id="ebdbb-114">Poprawki błędów</span><span class="sxs-lookup"><span data-stu-id="ebdbb-114">Bug fixes</span></span>

- <span data-ttu-id="ebdbb-115">Czas i wydatek</span><span class="sxs-lookup"><span data-stu-id="ebdbb-115">Time and Expense</span></span>

     - <span data-ttu-id="ebdbb-116">Naprawione: funkcja wyszukiwania na stronie **zatwierdzania wydatków** nie działa podczas wyszukiwania według przeznaczenia wydatku.</span><span class="sxs-lookup"><span data-stu-id="ebdbb-116">Fixed: Search functionality on the **Expense approval** page does not work when searching by expense purpose.</span></span>

- <span data-ttu-id="ebdbb-117">Zarządzanie zasobami</span><span class="sxs-lookup"><span data-stu-id="ebdbb-117">Resource Management</span></span>

     - <span data-ttu-id="ebdbb-118">Naprawione: liczby w uzgodnieniu zostały zaktualizowane w celu wyjustowania do prawej.</span><span class="sxs-lookup"><span data-stu-id="ebdbb-118">Fixed: Numbers in the reconciliation have been updated to be right justified.</span></span>
     - <span data-ttu-id="ebdbb-119">Naprawione: na karcie **harmonogram** nie można przypisywać nazwanych zasobów do zadań.</span><span class="sxs-lookup"><span data-stu-id="ebdbb-119">Fixed: Named Resources can't be assigned to tasks through the **Schedule** tab.</span></span>

- <span data-ttu-id="ebdbb-120">Zarządzanie projektem</span><span class="sxs-lookup"><span data-stu-id="ebdbb-120">Project Management</span></span>

     - <span data-ttu-id="ebdbb-121">Naprawione: wyjątek odwołania zerowego podczas przypisywania członka zespołu w przypadku braku informacji konfiguracyjnych **TransactionType** dla **Jednostki** i **DefaultGroup**.</span><span class="sxs-lookup"><span data-stu-id="ebdbb-121">Fixed: Null reference exception when assigning team member when the **TransactionType** is missing setup information for **Unit** and **DefaultGroup**.</span></span>

- <span data-ttu-id="ebdbb-122">Sales</span><span class="sxs-lookup"><span data-stu-id="ebdbb-122">Sales</span></span>

     - <span data-ttu-id="ebdbb-123">Naprawione: duplikaty rekordów typów transakcji zwracają błąd podczas tworzenia rekordów cen ról.</span><span class="sxs-lookup"><span data-stu-id="ebdbb-123">Fixed: Duplicate transaction type records return an error when role price records are created.</span></span>
     - <span data-ttu-id="ebdbb-124">Naprawione: dodatkowe przyciski dla **Nowa szansa sprzedaży**, **Oferta**, **Wiersz zamówienia** i **Dodaj produkt** są widoczne dla poleceń dotyczących szans sprzedaży, ofert, produktów zamówionych i podsiatki wierszy opartych na projekcie.</span><span class="sxs-lookup"><span data-stu-id="ebdbb-124">Fixed: Extra buttons for **New Opportunity**, **Quote**, **Order Line**, and **Add Product** are visible in commands for Opportunities, Quotes, Order Products, and the project-based Lines subgrid.</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]