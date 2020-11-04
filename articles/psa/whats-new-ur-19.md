---
title: Nowości i zmiany w aplikacji Project Service Automation, wydanie 19, wer. 3
description: W tym temacie przedstawiono funkcje i poprawki, które są dostępne w programie Project Service Automation, aktualizacja 19, wer. 3.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom: dyn365-projectservice
ms.date: 05/05/2020
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
ms.openlocfilehash: ecc923cccfad21985025ab9d8006aaff16afc25f
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081965"
---
# <a name="project-service-automation-update-release-19-v3"></a><span data-ttu-id="11a3e-103">Project Service Automation, wydanie 19, wer. 3</span><span class="sxs-lookup"><span data-stu-id="11a3e-103">Project Service Automation Update Release 19, V3</span></span>

<span data-ttu-id="11a3e-104">Mamy przyjemność ogłosić najnowszą aktualizację aplikacji Project Service Automation dla Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="11a3e-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="11a3e-105">To wydanie obejmuje znaczną poprawę jakości, wydajności i użyteczności.</span><span class="sxs-lookup"><span data-stu-id="11a3e-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="11a3e-106">To wydanie jest zgodne z systemem Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="11a3e-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="11a3e-107">Aby zaktualizować do tej wersji, odwiedź centrum administracyjne Dynamics 365 online i przejdź na stronę rozwiązań, aby zainstalować aktualizację.</span><span class="sxs-lookup"><span data-stu-id="11a3e-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="11a3e-108">By uzyskać więcej informacji, zobacz [Instalowanie, aktualizowanie lub usuwanie preferowanego rozwiązania](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="11a3e-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="11a3e-109">W tym temacie przedstawiono funkcje i poprawki, które są nowe lub zostały zmienione w programie PSA, wer. 3, aktualizacja 19.</span><span class="sxs-lookup"><span data-stu-id="11a3e-109">This topic lists the features and fixes that are new or changed for PSA V3, Update Release 19.</span></span> <span data-ttu-id="11a3e-110">Ta wersja ma numer kompilacji wer. 3.10.30.41 i zazwyczaj jest dostępna za pośrednictwem samoaktualizacji w maju 2020 r.</span><span class="sxs-lookup"><span data-stu-id="11a3e-110">This version has a build number of V3.10.30.41 and is generally available through a self-update in May 2020.</span></span>

## <a name="update-release-19"></a><span data-ttu-id="11a3e-111">Wydanie 19</span><span class="sxs-lookup"><span data-stu-id="11a3e-111">Update Release 19</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="11a3e-112">Poprawki błędów</span><span class="sxs-lookup"><span data-stu-id="11a3e-112">Bug fixes</span></span>

<span data-ttu-id="11a3e-113">**Czas i wydatek**</span><span class="sxs-lookup"><span data-stu-id="11a3e-113">**Time and Expense**</span></span>

<span data-ttu-id="11a3e-114">Rozwiązano następujące problemy:</span><span class="sxs-lookup"><span data-stu-id="11a3e-114">The following issues have been fixed:</span></span> 

- <span data-ttu-id="11a3e-115">Błędy pochodzące z importu wpisów godzin nie są poprawnie opisane.</span><span class="sxs-lookup"><span data-stu-id="11a3e-115">Errors derived from time entry imports are not surfaced correctly.</span></span>
- <span data-ttu-id="11a3e-116">Siatka wprowadzania czasu nie obsługuje zachowania pola **Tylko data**.</span><span class="sxs-lookup"><span data-stu-id="11a3e-116">Time Entry Grid does not support **Date Only** field behavior.</span></span>
- <span data-ttu-id="11a3e-117">Zasoby projektu nie mogą utworzyć wydatku dla projektu.</span><span class="sxs-lookup"><span data-stu-id="11a3e-117">Project Resources are unable to create an expense with a project.</span></span>

<span data-ttu-id="11a3e-118">**Zarządzanie projektem**</span><span class="sxs-lookup"><span data-stu-id="11a3e-118">**Project Management**</span></span>

<span data-ttu-id="11a3e-119">Rozwiązano następujące problemy:</span><span class="sxs-lookup"><span data-stu-id="11a3e-119">The following issues have been fixed:</span></span> 

-  <span data-ttu-id="11a3e-120">Zadanie podrzędne powoduje nieprawidłowe szacowanie kosztów przy zakończeniu (EAC).</span><span class="sxs-lookup"><span data-stu-id="11a3e-120">Grandchild task causes an incorrect effort estimate during the Completion (EAC) Calculation.</span></span>

<span data-ttu-id="11a3e-121">**Sales**</span><span class="sxs-lookup"><span data-stu-id="11a3e-121">**Sales**</span></span>

<span data-ttu-id="11a3e-122">Rozwiązano następujące problemy:</span><span class="sxs-lookup"><span data-stu-id="11a3e-122">The following issues have been fixed:</span></span> 

- <span data-ttu-id="11a3e-123">Akcja **Oblicz ponownie** nie działa ze szczegółami pozycji kontraktu wydatków lub informacjami o wierszach oferty.</span><span class="sxs-lookup"><span data-stu-id="11a3e-123">The **Recalculate** action does not work with expense contract line details or quote line details.</span></span>
- <span data-ttu-id="11a3e-124">Brak **Cen aktualizacji** dla szacowań wydatków.</span><span class="sxs-lookup"><span data-stu-id="11a3e-124">**Update Prices** is missing for expense estimates.</span></span>
-  <span data-ttu-id="11a3e-125">Klienci nie mogą wybierać niestandardowych przyczyn stanu kontraktu na stronie **Kontrakt projektu**.</span><span class="sxs-lookup"><span data-stu-id="11a3e-125">Customers are unable to select custom contract status reasons from the **Project Contract** page.</span></span>
- <span data-ttu-id="11a3e-126">Klienci doświadczają spadku wydajności podczas tworzenia cennika niestandardowego na podstawie oferty.</span><span class="sxs-lookup"><span data-stu-id="11a3e-126">Customers experience degraded performance when creating a custom price list from a quote.</span></span>
- <span data-ttu-id="11a3e-127">Klienci doświadczają niespójności z domyślnymi **jednostkami** dotyczącymi stron **Szczegółów wiersza oferty** i **Szczegółów pozycji kontraktu**.</span><span class="sxs-lookup"><span data-stu-id="11a3e-127">Customers experience inconsistency with **unit** defaults on **Quote Line Details** and **Contract Line Details** pages.</span></span>
- <span data-ttu-id="11a3e-128">Dodanie pozycji kategorii niepłatnych transakcji do płatnej pozycji kontraktu nie będzie brać pod uwagę **Niepłatnego** rozliczeniowego typu kategorii transakcji.</span><span class="sxs-lookup"><span data-stu-id="11a3e-128">Adding non-chargeable transaction category items to a chargeable contract line will not respect the **Non-chargeable** billing type of the transaction category.</span></span>
- <span data-ttu-id="11a3e-129">Klienci nie mogą korzystać z nowo dodanych ról i kategorii w poprzednio utworzonych kontraktach.</span><span class="sxs-lookup"><span data-stu-id="11a3e-129">Customers can't use the newly added roles and category on previously created contracts.</span></span>
- <span data-ttu-id="11a3e-130">Klienci doświadczają spadku wydajności podczas niepotrzebnego pobierania w PreValidateProjectTeamMemberUpdate.cs</span><span class="sxs-lookup"><span data-stu-id="11a3e-130">Customers experience degraded performance Unnecessary retrieve in PreValidateProjectTeamMemberUpdate.cs</span></span>
- <span data-ttu-id="11a3e-131">Role skonfigurowane jako niepłatne na liście **Kategorie zasobów** powinny zostać dodane do karty **Role płatne** jako **Niepłatne** w pozycji kontraktu projektu.</span><span class="sxs-lookup"><span data-stu-id="11a3e-131">Roles set up as non-chargeable in the **Resource Categories** list should be added to the **Chargeable Roles** tab as **Non0chargeable** on the contract line for a project.</span></span>
- <span data-ttu-id="11a3e-132">Podczas tworzenia projektu klienci mogą doświadczyć spadku wydajności, ponieważ **GetBookableResourceIdFromUser** pobiera wszystkie kolumny zasobów możliwych do zarezerwowania, a nie tylko podstawowy identyfikator.</span><span class="sxs-lookup"><span data-stu-id="11a3e-132">Customers may experience degraded performance when creating a project because **GetBookableResourceIdFromUser** retrieves all columns of bookable resources instead of just the primary ID.</span></span>
- <span data-ttu-id="11a3e-133">W encji **TransactionType** brak dodatku wstępnej weryfikacji aktualizacji, aby zapobiec wprowadzaniu przez użytkowników **jednostek** i **UnitGroups** , które są nieprawidłowe dla typów transakcji.</span><span class="sxs-lookup"><span data-stu-id="11a3e-133">**TransactionType** entity missing the pre-validation update plug-in to prevent users from entering **Units** and **UnitGroups** that are not valid for transaction types.</span></span>
- <span data-ttu-id="11a3e-134">Krok **Usuń** nie działa w przypadku importowania wpisów czasu.</span><span class="sxs-lookup"><span data-stu-id="11a3e-134">The **Remove** step does not work for time entry import.</span></span>
