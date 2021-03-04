---
title: Nowości i zmiany w aplikacji Project Service Automation, wydanie 24, wer. 3
description: W tym temacie przedstawiono funkcje i poprawki, które są dostępne w programie Project Service Automation, aktualizacja 24, wer. 3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 10/02/2020
ms.topic: article
ms.author: stsporen
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 15fe1c3482de66331dd543ee73391638919b2595
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/10/2021
ms.locfileid: "5146721"
---
# <a name="project-service-automation-update-release-24-v3"></a><span data-ttu-id="51e87-103">Project Service Automation, wydanie 24, wer. 3</span><span class="sxs-lookup"><span data-stu-id="51e87-103">Project Service Automation Update Release 24, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="51e87-104">Mamy przyjemność ogłosić najnowszą aktualizację aplikacji Project Service Automation dla Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="51e87-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="51e87-105">To wydanie obejmuje znaczną poprawę jakości, wydajności i użyteczności.</span><span class="sxs-lookup"><span data-stu-id="51e87-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="51e87-106">To wydanie jest zgodne z systemem Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="51e87-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="51e87-107">Aby zaktualizować do tej wersji, odwiedź centrum administracyjne Dynamics 365 online i przejdź na stronę rozwiązań, aby zainstalować aktualizację.</span><span class="sxs-lookup"><span data-stu-id="51e87-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="51e87-108">By uzyskać więcej informacji, zobacz [Instalowanie, aktualizowanie lub usuwanie preferowanego rozwiązania](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="51e87-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="51e87-109">W tym temacie przedstawiono funkcje i poprawki, które są nowe lub zostały zmienione w programie Project Service Automation, wer. 3, aktualizacja 24.</span><span class="sxs-lookup"><span data-stu-id="51e87-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 24.</span></span> <span data-ttu-id="51e87-110">Numer tej kompilacji to V3.10.42.43 i jest on zazwyczaj dostępny za pośrednictwem samoaktualizacji w październiku 2020 r.</span><span class="sxs-lookup"><span data-stu-id="51e87-110">This version has a build number of V 3.10.42.43 and is generally available through a self-update in October 2020.</span></span>

## <a name="update-release-24"></a><span data-ttu-id="51e87-111">Wydanie 24</span><span class="sxs-lookup"><span data-stu-id="51e87-111">Update Release 24</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="51e87-112">Poprawki błędów</span><span class="sxs-lookup"><span data-stu-id="51e87-112">Bug fixes</span></span>

<span data-ttu-id="51e87-113">**Sales**</span><span class="sxs-lookup"><span data-stu-id="51e87-113">**Sales**</span></span>

<span data-ttu-id="51e87-114">Rozwiązano następujące problemy:</span><span class="sxs-lookup"><span data-stu-id="51e87-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="51e87-115">Wystąpił problem podczas ustawiania domyślnego cennika produktów.</span><span class="sxs-lookup"><span data-stu-id="51e87-115">Problem while setting default price list of products.</span></span>
- <span data-ttu-id="51e87-116">Wydajność licytacji jest niska z powodu osadzonych cenników i kopii rekordów cen ról.</span><span class="sxs-lookup"><span data-stu-id="51e87-116">Performance of Quote win is slow due to the embedded price list and role price records copy.</span></span>
- <span data-ttu-id="51e87-117">**Kontrakt projektu/Centrum sprzedaży** > **Pozycja wiersza produktu/Ilość wiersza zamówienia** jest automatycznie zaokrąglana do najbliższej liczby całkowitej.</span><span class="sxs-lookup"><span data-stu-id="51e87-117">**Project Contract/Sales Hub** > **Product Line Item/Order Line Quantity** is automatically rounded to the nearest integer.</span></span>
- <span data-ttu-id="51e87-118">Podnieś uprawnienia do uprawnień systemowych podczas odczytywania cenników.</span><span class="sxs-lookup"><span data-stu-id="51e87-118">Elevate to system privileges when reading price lists.</span></span>
- <span data-ttu-id="51e87-119">Kopiuj pola adresu klienta **address1_freighttermscode** i **address1_shippingmethodcode** do oferty/zamówienia.</span><span class="sxs-lookup"><span data-stu-id="51e87-119">Copy customer address fields **address1_freighttermscode** and **address1_shippingmethodcode** to Quote/Order.</span></span> 


<span data-ttu-id="51e87-120">**Czas i wydatek**</span><span class="sxs-lookup"><span data-stu-id="51e87-120">**Time and Expense**</span></span>

<span data-ttu-id="51e87-121">Rozwiązano następujące problemy:</span><span class="sxs-lookup"><span data-stu-id="51e87-121">The following issues have been fixed:</span></span>

- <span data-ttu-id="51e87-122">**Siatka wprowadzania godzin** nie obsługuje zachowania czasowego **Tylko data**.</span><span class="sxs-lookup"><span data-stu-id="51e87-122">The **Time Entry Grid** doesn't support **Date Only** time behavior.</span></span>
- <span data-ttu-id="51e87-123">**Wpis czasu** nie jest odświeżany automatycznie.</span><span class="sxs-lookup"><span data-stu-id="51e87-123">**Time Entry** is not refreshing automatically.</span></span> <span data-ttu-id="51e87-124">Wymagane jest ręczne odświeżenie.</span><span class="sxs-lookup"><span data-stu-id="51e87-124">A manual refresh is required.</span></span>
- <span data-ttu-id="51e87-125">Nie można zaimportować wpisów czasu z przypisania, jeśli w przypisaniach zasobu występuje przerwa (0 godzin).</span><span class="sxs-lookup"><span data-stu-id="51e87-125">Unable to import the time entries from an assignment when there is a break (0 hours) in a resource's assignments.</span></span>
- <span data-ttu-id="51e87-126">Podczas tworzenia wpisu czasu ustaw początek na taki sam, jak **msdyn_date**.</span><span class="sxs-lookup"><span data-stu-id="51e87-126">When creating a time entry, set the start to the same as **msdyn_date**.</span></span>
- <span data-ttu-id="51e87-127">Ponownie włącz edycję zbiorczą dla wpisu czasu.</span><span class="sxs-lookup"><span data-stu-id="51e87-127">Re-enable bulk edit for time entry.</span></span>

<span data-ttu-id="51e87-128">**Zarządzanie zasobami**</span><span class="sxs-lookup"><span data-stu-id="51e87-128">**Resource Management**</span></span>

<span data-ttu-id="51e87-129">Rozwiązano następujące problemy:</span><span class="sxs-lookup"><span data-stu-id="51e87-129">The following issues have been fixed:</span></span>

- <span data-ttu-id="51e87-130">Próba zaktualizowania stanu rezerwacji międzydniowej bez wymagania spowoduje zgłoszenie wyjątku odwołania o wartości null.</span><span class="sxs-lookup"><span data-stu-id="51e87-130">Trying to update the status of an inter-day booking without a requirement will throw a null-ref exception.</span></span>
- <span data-ttu-id="51e87-131">Wystąpił błąd podczas ładowania **Widoku uzgadniania**.</span><span class="sxs-lookup"><span data-stu-id="51e87-131">Error loading the **Reconciliation View**.</span></span>


<span data-ttu-id="51e87-132">**Zarządzanie projektem**</span><span class="sxs-lookup"><span data-stu-id="51e87-132">**Project Management**</span></span>

<span data-ttu-id="51e87-133">Rozwiązano następujące problemy:</span><span class="sxs-lookup"><span data-stu-id="51e87-133">The following issues have been fixed:</span></span>

- <span data-ttu-id="51e87-134">W **Harmonogramie projektu** podczas zmiany z **Ręczne** na **Automatyczne** nie jest dokonywane automatyczne zapisywanie.</span><span class="sxs-lookup"><span data-stu-id="51e87-134">In the **Project Schedule**, when changing from **Manual** to **Auto**, auto save is not completing.</span></span>
- <span data-ttu-id="51e87-135">Koszty wydatków nie powinny być obliczane względem wariancji w **Siatce śledzenia projektu**.</span><span class="sxs-lookup"><span data-stu-id="51e87-135">Expense costs should not calculate toward variance on the **Project Tracking Grid**.</span></span>
- <span data-ttu-id="51e87-136">Niespójne zachowanie dotyczące kolumn **Tag oszacować** podczas ładowania i zmiany typu **Fazy czasu**.</span><span class="sxs-lookup"><span data-stu-id="51e87-136">Inconsistent behavior for **Estimates tag** columns during load versus changing the **Time-Phase** type.</span></span>
- <span data-ttu-id="51e87-137">Koszt rzeczywisty w projekcie może nie odzwierciedlać sum w **Wartościach rzeczywistych**.</span><span class="sxs-lookup"><span data-stu-id="51e87-137">The actual cost on a project may not reflect the totals from **Actuals**.</span></span>
- <span data-ttu-id="51e87-138">**Szacowana data zakończenia** na karcie **Podsumowanie** nie jest zgodna z **Harmonogramem SPP**.</span><span class="sxs-lookup"><span data-stu-id="51e87-138">**Estimated Finish Date** on the **Summary** tab does not match the **WBS Schedule**.</span></span>
- <span data-ttu-id="51e87-139">**Zaktualizowanie rzeczywistych godzin** na zmniejszeniu wcięcia nie działa poprawnie.</span><span class="sxs-lookup"><span data-stu-id="51e87-139">**Update Actual Hours** on outdent does not work correctly.</span></span>
- <span data-ttu-id="51e87-140">Menedżer projektu spoza katalogu głównego **JB** nie może utworzyć projektu.</span><span class="sxs-lookup"><span data-stu-id="51e87-140">A Project manager outside of root **BU** can't create a project.</span></span>
- <span data-ttu-id="51e87-141">Zmiany w zadaniach i kategoriach w **Szacunkach wydatków** nie są trwałe.</span><span class="sxs-lookup"><span data-stu-id="51e87-141">Changes to task or category on **Expense Estimates** are not persisted.</span></span>
- <span data-ttu-id="51e87-142">**Kopia kontraktu** kopiuje harmonogramy faktur oraz stanu przebiegu.</span><span class="sxs-lookup"><span data-stu-id="51e87-142">**Copy of contract** copies the invoice schedules and the run status.</span></span>
- <span data-ttu-id="51e87-143">**Przycisk odświeżanie wartości rzeczywistych** powoduje nieprawidłowe obliczenie zadań sumarycznych.</span><span class="sxs-lookup"><span data-stu-id="51e87-143">**Refresh Actuals** button incorrectly calculates summary tasks.</span></span>
- <span data-ttu-id="51e87-144">Dodatek programu Microsoft Project: rozwiąż błąd odwołania do wartości null, jeśli dowolny członek zespołu ma pustą jednostkę ponownego pozyskania zasobów.</span><span class="sxs-lookup"><span data-stu-id="51e87-144">Microsoft Project Add-in: Fix null reference error if any team member has an empty resourcing unit.</span></span>

