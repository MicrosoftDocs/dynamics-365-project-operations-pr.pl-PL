---
title: Nowości i zmiany w Project Service Automation, wydanie 21, wer. 3
description: W tym temacie przedstawiono funkcje i poprawki, które są dostepne w Project Service Automation, aktualizacja 21, wer. 3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 06/19/2020
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
ms.openlocfilehash: ad44f6747486222cc1f48c7b645f2525d382dca3
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/27/2021
ms.locfileid: "5949062"
---
# <a name="project-service-automation-update-release-21-v3"></a><span data-ttu-id="960ee-103">Project Service Automation, wydanie 21, wer. 3</span><span class="sxs-lookup"><span data-stu-id="960ee-103">Project Service Automation Update Release 21, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="960ee-104">Mamy przyjemność ogłosić najnowszą aktualizację aplikacji Project Service Automation dla Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="960ee-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="960ee-105">To wydanie obejmuje znaczną poprawę jakości, wydajności i użyteczności.</span><span class="sxs-lookup"><span data-stu-id="960ee-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="960ee-106">To wydanie jest zgodne z systemem Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="960ee-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="960ee-107">Aby zaktualizować do tej wersji, odwiedź centrum administracyjne Dynamics 365 online i przejdź na stronę rozwiązań, aby zainstalować aktualizację.</span><span class="sxs-lookup"><span data-stu-id="960ee-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="960ee-108">By uzyskać więcej informacji, zobacz [Instalowanie, aktualizowanie lub usuwanie preferowanego rozwiązania](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="960ee-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="960ee-109">W tym temacie przedstawiono funkcje i poprawki, które są nowe lub zostały zmienione w Project Service Automation, wer. 3, aktualizacja 21.</span><span class="sxs-lookup"><span data-stu-id="960ee-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 21.</span></span> <span data-ttu-id="960ee-110">Ta wersja ma numer kompilacji wer. 3.10.32.50 i zazwyczaj jest dostępna za pośrednictwem samoaktualizacji w czerwcu 2020 r.</span><span class="sxs-lookup"><span data-stu-id="960ee-110">This version has a build number of V 3.10.32.50 and is generally available through a self-update in June 2020.</span></span>

## <a name="update-release-21"></a><span data-ttu-id="960ee-111">Wydanie 21</span><span class="sxs-lookup"><span data-stu-id="960ee-111">Update Release 21</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="960ee-112">Poprawki błędów</span><span class="sxs-lookup"><span data-stu-id="960ee-112">Bug fixes</span></span>

<span data-ttu-id="960ee-113">**Czas i wydatek**</span><span class="sxs-lookup"><span data-stu-id="960ee-113">**Time and Expense**</span></span>

<span data-ttu-id="960ee-114">Rozwiązano następujące problemy:</span><span class="sxs-lookup"><span data-stu-id="960ee-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="960ee-115">Podczas obsługi **Kontrolki siatki wpisu czasu** w pulpitach nawigacyjnych siatka nie używa pełnej szerokości kontenera siatki pulpitu nawigacyjnego.</span><span class="sxs-lookup"><span data-stu-id="960ee-115">When hosting the **Time Entry Grid Control** in Dashboards, the grid does not utilize the full width of the dashboard grid container.</span></span>
- <span data-ttu-id="960ee-116">W przypadku określonych stref czasowych kontrolka siatki **Wpisu czasu** nie wyświetla rekordów.</span><span class="sxs-lookup"><span data-stu-id="960ee-116">For specific time zones, the **Time Entry** grid control does not display records.</span></span>
- <span data-ttu-id="960ee-117">Wpisy czasu o godzinie 9:00 są wyświetlane w złym dniu.</span><span class="sxs-lookup"><span data-stu-id="960ee-117">Time entries that are after 9:00 PM appear on the wrong day.</span></span>
- <span data-ttu-id="960ee-118">Użytkownicy nie są w stanie przesłać kosztów, jeśli kategoria wydatku, **Wymagany paragon wydatków** nie zawiera wartości.</span><span class="sxs-lookup"><span data-stu-id="960ee-118">Users are unable to submit expenses if the expense category, **Expense receipt required** has no value.</span></span>

<span data-ttu-id="960ee-119">**Zarządzanie zasobami**</span><span class="sxs-lookup"><span data-stu-id="960ee-119">**Resource Management**</span></span>

<span data-ttu-id="960ee-120">Rozwiązano następujące problemy:</span><span class="sxs-lookup"><span data-stu-id="960ee-120">The following issues have been fixed:</span></span>

- <span data-ttu-id="960ee-121">Nieaktywne rezerwacje są wyświetlane w widoku **Uzgodnienie**.</span><span class="sxs-lookup"><span data-stu-id="960ee-121">Inactive bookings are displayed in the **Reconciliation** view.</span></span>
- <span data-ttu-id="960ee-122">Podczas sprawdzania poprawności zasobu rodzajowego nie jest sprawdzana wartość, aby mieć pewność, że istnieje prawidłowy stan rezerwacji.</span><span class="sxs-lookup"><span data-stu-id="960ee-122">Generic resource fulfillment was missing validation to ensure that a valid booking status exists.</span></span>

<span data-ttu-id="960ee-123">**Zarządzanie projektem**</span><span class="sxs-lookup"><span data-stu-id="960ee-123">**Project Management**</span></span>

<span data-ttu-id="960ee-124">Rozwiązano następujące problemy:</span><span class="sxs-lookup"><span data-stu-id="960ee-124">The following issues have been fixed:</span></span>

- <span data-ttu-id="960ee-125">Siatki formularzy **Projektu** (**Przydział zasobów**, **Zadanie**, widok **Uzgodnienie**, **Oszacowania kosztów**) można edytować nawet wtedy, gdy projekt nie jest aktywny.</span><span class="sxs-lookup"><span data-stu-id="960ee-125">The **Project** form grids (**Resource Assignment**, **Task**, **Reconciliation** view, **Expense Estimates**) remain editable even when a project is not active.</span></span>
- <span data-ttu-id="960ee-126">Nie można łączyć duplikatów klientów z klientami, którzy są połączeni z potwierdzonymi kontraktami projektu.</span><span class="sxs-lookup"><span data-stu-id="960ee-126">Duplicate customers can't be merged with customers that are linked to confirmed project contracts.</span></span>
- <span data-ttu-id="960ee-127">Gdy dodawany jest zasób niezawierający prawidłowego kalendarza, system nie zwraca przyjaznego użytkownika komunikatu o błędzie.</span><span class="sxs-lookup"><span data-stu-id="960ee-127">When a resource who does not have a valid calendar is added, the system does not return a user friendly-error message.</span></span>
- <span data-ttu-id="960ee-128">Przycisk **Dodaj zadanie** w siatce zadań jest włączony, jeśli projekt jest połączony z **dodatkiem Microsoft Project**.</span><span class="sxs-lookup"><span data-stu-id="960ee-128">The **Add Task** button on the task grid is enabled when the project is linked to **Microsoft Project add-in**.</span></span>
- <span data-ttu-id="960ee-129">Coraz więcej nakład pracy zwiększa się w momencie, gdy zadanie z kategorią jest przypisywane do zasobu z rolą, dla której zdefiniowano cenę kosztową.</span><span class="sxs-lookup"><span data-stu-id="960ee-129">Effort grows uncontrollably when a task with a category is assigned to a resource with a role for which there is a cost price defined.</span></span>

<span data-ttu-id="960ee-130">**Sales**</span><span class="sxs-lookup"><span data-stu-id="960ee-130">**Sales**</span></span>

<span data-ttu-id="960ee-131">Wprowadzono następujące ulepszenia:</span><span class="sxs-lookup"><span data-stu-id="960ee-131">The following enhancements have been made:</span></span>

- <span data-ttu-id="960ee-132">**Częstotliwość fakturowania** i **Rozpoczęcie fakturowania** zostały przeniesione na kartę **Harmonogram faktur**.</span><span class="sxs-lookup"><span data-stu-id="960ee-132">**Invoice Frequency** and **Billing Start** have been moved to the **Invoice Schedule** tab.</span></span>

<span data-ttu-id="960ee-133">Rozwiązano następujące problemy:</span><span class="sxs-lookup"><span data-stu-id="960ee-133">The following issues have been fixed:</span></span>

- <span data-ttu-id="960ee-134">**Łączna cena sprzedaży** wynosi zero (0) dla **Kategorii**, mimo że dana **Rola** ma całkowitą cenę sprzedaży nie równą zero.</span><span class="sxs-lookup"><span data-stu-id="960ee-134">**Total Sales Price** is zero (0) for **Category** even though **Role** has a total sales price that is not zero.</span></span>
- <span data-ttu-id="960ee-135">Klienci nie mogą zmieniać wartości pola **Status faktury** w celu **Gotowe do fakturowania**, kiedy inny dostosowany proces aktualizuje pole dodatkowe.</span><span class="sxs-lookup"><span data-stu-id="960ee-135">Customers can't change the value of the **Invoice Status** field to **Ready for invoicing** when another customized process is updating an additional field.</span></span>
- <span data-ttu-id="960ee-136">Przycisk **Odśwież wiersze faktury** może spowodować utworzenie wielu zduplikowanych wierszy, jeśli jest ciągle zaznaczonych.</span><span class="sxs-lookup"><span data-stu-id="960ee-136">The **Refresh Invoice Lines** button can create multiple duplicated lines if it is repeatedly selected.</span></span>
- <span data-ttu-id="960ee-137">Przycisk **Aktualizuj ceny** nie działa w przypadku podsiatki **Ceny ról** w formularzu **Szybki podgląd**.</span><span class="sxs-lookup"><span data-stu-id="960ee-137">The **Update Prices** button doesn't work on the **Role Prices** subgrid in the **Quick View** form.</span></span>
- <span data-ttu-id="960ee-138">Logika **Rozpoznawania cennika sprzedaży** nieprawidłowo obsługuje strefy czasowe, co powoduje nieprawidłowe wybór cenników.</span><span class="sxs-lookup"><span data-stu-id="960ee-138">The **Sales Price List Resolution** logic improperly handles time zones, resulting in the incorrect selection of price lists.</span></span>
- <span data-ttu-id="960ee-139">**Łączny koszt rzeczywisty** projektu może być wyłączony o kwotę ułamkową po zaakceptowaniu jednego wpisu czasowego.</span><span class="sxs-lookup"><span data-stu-id="960ee-139">A project’s **Total Actual Cost** can be off by a fractional amount after a single time entry is approved.</span></span>
- <span data-ttu-id="960ee-140">Logika **Rozwiązywania cen** nie zawiera przyjaznych dla użytkownika komunikatów o błędach, jeśli **Pobieranie Ceny Ról** nie ma wartości w polach **„Jednostka podstawowa”** i **„Cena w jednostce podstawowej”**.</span><span class="sxs-lookup"><span data-stu-id="960ee-140">The **Price Resolution** logic does not provide a user-friendly error message if **Retrieved RolePrice** doesn't have values in **'Primary Unit'** and **'Price In Primary Unit'** fields.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]