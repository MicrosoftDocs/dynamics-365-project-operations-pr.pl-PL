---
title: Nowości i zmiany w aplikacji Project Service Automation, wydanie 17, wer. 3
description: W tym temacie przedstawiono funkcje i poprawki, które są dostepne w programie Project Service Automation, aktualizacja 17, wer. 3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 03/06/2020
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
ms.openlocfilehash: bb93208217972639f91b39b7b6705d9897373ef7
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/28/2020
ms.locfileid: "4126813"
---
# <a name="project-service-automation-update-release-17-v3"></a><span data-ttu-id="1cd97-103">Project Service Automation, wydanie 17, wer. 3</span><span class="sxs-lookup"><span data-stu-id="1cd97-103">Project Service Automation Update Release 17, V3</span></span>

<span data-ttu-id="1cd97-104">Mamy przyjemność ogłosić najnowszą aktualizację aplikacji Project Service Automation dla Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="1cd97-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="1cd97-105">To wydanie obejmuje znaczną poprawę jakości, wydajności i użyteczności.</span><span class="sxs-lookup"><span data-stu-id="1cd97-105">This release includes some important improvements to quality, performance, and usability.</span></span>  <span data-ttu-id="1cd97-106">To wydanie jest zgodne z systemem Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="1cd97-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="1cd97-107">Aby zaktualizować do tej wersji, odwiedź Centrum administracyjne Dynamics 365 online i przejdź na stronę rozwiązań, aby zainstalować aktualizację.</span><span class="sxs-lookup"><span data-stu-id="1cd97-107">To update to this release, visit the Admin Center for Dynamics 365 online, solutions page to install the update.</span></span> <span data-ttu-id="1cd97-108">By uzyskać więcej informacji, zobacz [Instalowanie, aktualizowanie lub usuwanie preferowanego rozwiązania](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="1cd97-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="1cd97-109">W tym temacie przedstawiono funkcje i poprawki, które są nowe lub zostały zmienione w programie PSA, wer. 3, aktualizacja 17.</span><span class="sxs-lookup"><span data-stu-id="1cd97-109">This topic lists the features and fixes that are new or changed for PSA V3, Update Release 17.</span></span> <span data-ttu-id="1cd97-110">Numer tej kompilacji to V3.10.6.34 i jest on zazwyczaj dostępny za pośrednictwem samoaktualizacji w marcu 2020 r.</span><span class="sxs-lookup"><span data-stu-id="1cd97-110">This version has a build number of V3.10.6.34 and is generally available through a self-update in March 2020.</span></span>


## <a name="update-release-17"></a><span data-ttu-id="1cd97-111">Wydanie 17</span><span class="sxs-lookup"><span data-stu-id="1cd97-111">Update Release 17</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="1cd97-112">Poprawki błędów</span><span class="sxs-lookup"><span data-stu-id="1cd97-112">Bug fixes</span></span>

<span data-ttu-id="1cd97-113">**Ogólne**</span><span class="sxs-lookup"><span data-stu-id="1cd97-113">**General**</span></span>

- <span data-ttu-id="1cd97-114">Naprawione: aktualizowanie rozwiązania Project Service Automation w celu wdrożenia licencji dla Członków zespołu (centrum Project Resource będzie obejmował plan Usługi dla Człownków zespołu 3.x)</span><span class="sxs-lookup"><span data-stu-id="1cd97-114">Fixed: Update Project Service Automation to enforce Team Member licenses (Project Resource Hub will include Team Member Service plan metadata 3.x)</span></span>
 
<span data-ttu-id="1cd97-115">**Czas i wydatki**</span><span class="sxs-lookup"><span data-stu-id="1cd97-115">**Time and Expense**</span></span>

- <span data-ttu-id="1cd97-116">Naprawione: Nie jest możliwe zmodyfikowanie oszacowania kosztów z ceną wyższą niż zero na zero (0).</span><span class="sxs-lookup"><span data-stu-id="1cd97-116">Fixed: It is not possible to change an expense estimate from a non-zero price to zero (0).</span></span> <span data-ttu-id="1cd97-117">Zmiana została zignorowana.</span><span class="sxs-lookup"><span data-stu-id="1cd97-117">The change is ignored.</span></span>

<span data-ttu-id="1cd97-118">**Zarządzanie projektem**</span><span class="sxs-lookup"><span data-stu-id="1cd97-118">**Project Management**</span></span>

- <span data-ttu-id="1cd97-119">Naprawione: sprawdzanie wartości null zostało dodane względem nazwy pozycji członka zespołu.</span><span class="sxs-lookup"><span data-stu-id="1cd97-119">Fixed: A check for null values has been added on a team member's position name.</span></span>
- <span data-ttu-id="1cd97-120">Naprawione: pole **msdyn_userresourceid** w encji **msdyn_resourceassignment** jest przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="1cd97-120">Fixed: **msdyn_userresourceid** field on the **msdyn_resourceassignment** entity has been deprecated.</span></span>
- <span data-ttu-id="1cd97-121">Naprawione: Uaktualnianie z 2.x do wersji 3.x obsługuje teraz puste zarysy nakładów pracy dla przydziałów zadań.</span><span class="sxs-lookup"><span data-stu-id="1cd97-121">Fixed: Upgrade from 2.x to 3.x now handles empty effort contours on task assignments.</span></span>

<span data-ttu-id="1cd97-122">**Sales**</span><span class="sxs-lookup"><span data-stu-id="1cd97-122">**Sales**</span></span>

- <span data-ttu-id="1cd97-123">Naprawione: **Invoice.PreValidateInvoiceUpdate** teraz poprawnie obsługuje scenariusz ponownego przypisania właścicieli rekordów.</span><span class="sxs-lookup"><span data-stu-id="1cd97-123">Fixed: **Invoice.PreValidateInvoiceUpdate** now handles the scenario of reassigning record owners properly.</span></span>
- <span data-ttu-id="1cd97-124">Naprawione: Kiedy klasa transakcji to **Czas** **UnitGroup** nie można edytować dla wszystkich encji, w tym **QuoteLineDetails**, **JournalLine**, **InvoiceLineDetail** i **ContractLineDetails**.</span><span class="sxs-lookup"><span data-stu-id="1cd97-124">Fixed: When the transaction class is **Time**, **UnitGroup** is non-editable for all entities including, **QuoteLineDetails**, **JournalLine**, **InvoiceLineDetail**, and **ContractLineDetails**.</span></span> <span data-ttu-id="1cd97-125">**Jednostka** nie jest jednak edytowana wyłącznie dla **JournalLine** i **InvoiceLineDetails**.</span><span class="sxs-lookup"><span data-stu-id="1cd97-125">However, **Unit** is non-editable only for **JournalLine** and **InvoiceLineDetails**.</span></span>


