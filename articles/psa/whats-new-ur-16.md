---
title: Nowości i zmiany w aplikacji Project Service Automation, wydanie 16, wer. 3
description: W tym temacie przedstawiono funkcje i poprawki, które są dostepne w programie Project Service Automation, aktualizacja 16, wer. 3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 02/18/2020
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
ms.openlocfilehash: 882ee6c25e5d88db22e051254c7fd82dc787ab73
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/10/2021
ms.locfileid: "5143646"
---
# <a name="project-service-automation-update-release-16-v3"></a><span data-ttu-id="d3541-103">Project Service Automation, wydanie 16, wer. 3</span><span class="sxs-lookup"><span data-stu-id="d3541-103">Project Service Automation Update Release 16, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="d3541-104">Mamy przyjemność ogłosić najnowszą aktualizację aplikacji Project Service Automation dla Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="d3541-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="d3541-105">To wydanie obejmuje znaczną poprawę jakości, wydajności i użyteczności.</span><span class="sxs-lookup"><span data-stu-id="d3541-105">This release includes some important improvements to quality, performance, and usability.</span></span>  <span data-ttu-id="d3541-106">To wydanie jest zgodne z systemem Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="d3541-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="d3541-107">Aby zaktualizować do tej wersji, odwiedź Centrum administracyjne Dynamics 365 online i przejdź na stronę rozwiązań, aby zainstalować aktualizację.</span><span class="sxs-lookup"><span data-stu-id="d3541-107">To update to this release, visit the Admin Center for Dynamics 365 online, solutions page to install the update.</span></span> <span data-ttu-id="d3541-108">By uzyskać więcej informacji, zobacz [Instalowanie, aktualizowanie Preferowanego rozwiązania](https://docs.microsoft.com/dynamics365/project-service/upgrade-psa-home-page).</span><span class="sxs-lookup"><span data-stu-id="d3541-108">For more information, see [Install, Update a Preferred Solution](https://docs.microsoft.com/dynamics365/project-service/upgrade-psa-home-page).</span></span>
<span data-ttu-id="d3541-109">W tym temacie przedstawiono funkcje i poprawki, które są nowe lub zostały zmienione w programie PSA, wer. 3, aktualizacja 16.</span><span class="sxs-lookup"><span data-stu-id="d3541-109">This topic lists the features and fixes that are new or changed for PSA V3, Update Release 16.</span></span> <span data-ttu-id="d3541-110">Numer tej kompilacji to V3.10.6.34 i jest on zazwyczaj dostępny za pośrednictwem samoaktualizacji w styczniu 2020 r.</span><span class="sxs-lookup"><span data-stu-id="d3541-110">This version has a build number of V3.10.6.34 and is generally available through a self-update in January 2020.</span></span>


## <a name="update-release-16"></a><span data-ttu-id="d3541-111">Wydanie 16</span><span class="sxs-lookup"><span data-stu-id="d3541-111">Update Release 16</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="d3541-112">Poprawki błędów</span><span class="sxs-lookup"><span data-stu-id="d3541-112">Bug fixes</span></span>

-   <span data-ttu-id="d3541-113">Czas i wydatek</span><span class="sxs-lookup"><span data-stu-id="d3541-113">Time and Expense</span></span>

    -   <span data-ttu-id="d3541-114">Naprawione: Użytkownicy próbujący przesłać usunięte wpisy czasu i wydatków na potrzeby zatwierdzenia będą otrzymywać odpowiednie komunikaty o błędach.</span><span class="sxs-lookup"><span data-stu-id="d3541-114">Fixed: Users attempting to submit deleted time and expense entries for approvals will now receive relevant error messages.</span></span>

-   <span data-ttu-id="d3541-115">Zarządzanie projektem</span><span class="sxs-lookup"><span data-stu-id="d3541-115">Project Management</span></span>

    -   <span data-ttu-id="d3541-116">Poprawione: Jednostki zasobów zdefiniowane dla członków zespołu w szablonach są przestrzegane wraz z szablonami stosowanymi w nowym projekcie.</span><span class="sxs-lookup"><span data-stu-id="d3541-116">Fixed: The resourcing units defined for team members in templates are respected with the templates are applied to a new project.</span></span>

    -   <span data-ttu-id="d3541-117">Naprawione: poprawiono sposób obsługi ponownego przypisywania własności rekordu.</span><span class="sxs-lookup"><span data-stu-id="d3541-117">Fixed: Improved handling of the re-assignment of record ownership.</span></span>

    -   <span data-ttu-id="d3541-118">Naprawione: Projekty, które są w trakcie procesu kopiowania, nie będą dozwolone do skopiowania do momentu ukończenia wszystkich operacji kopiowania.</span><span class="sxs-lookup"><span data-stu-id="d3541-118">Fixed: Projects that are in the process of being copied will not be permitted to copied until all copy operations are complete.</span></span>

-   <span data-ttu-id="d3541-119">Zarządzanie zasobami</span><span class="sxs-lookup"><span data-stu-id="d3541-119">Resource Management</span></span>

    -   <span data-ttu-id="d3541-120">Naprawione: Rozszerz rezerwacje teraz poprawnie obsługuje krótkie czasy trwania i nie tworzy już zero godzin dla przedłużonych rezerwacji.</span><span class="sxs-lookup"><span data-stu-id="d3541-120">Fixed: Extend bookings now handles short durations correctly and no longer creates zero hours for extended bookings.</span></span>

    -   <span data-ttu-id="d3541-121">Naprawione: Widok uzgadniania jest teraz renderowany, gdy strefa czasowa projektu będzie wynosić +5:30 GMT, a tylko czas użytkownika jest inny.</span><span class="sxs-lookup"><span data-stu-id="d3541-121">Fixed: The reconciliation view now renders when the project time zone is +5:30 GMT and the user’s time aone is different.</span></span>

-   <span data-ttu-id="d3541-122">Sales</span><span class="sxs-lookup"><span data-stu-id="d3541-122">Sales</span></span>

    -   <span data-ttu-id="d3541-123">Naprawione: Po usunięciu projektu zamapowanego do pozycji kontraktu i zamapowaniu nowego projektu nie można ponownie oszacować rzeczywistych rekordów w nowym projekcie na podstawie reguł fakturowania i kalkulacji cen zdefiniowanych w pozycji kontraktu.</span><span class="sxs-lookup"><span data-stu-id="d3541-123">Fixed: When a project mapped to a contract line is removed and a new project is mapped, the actual records on the new project were not getting re-evaluated based on the billing and pricing rules defined on the contract line.</span></span> <span data-ttu-id="d3541-124">Ta funkcja została naprawiona w tym wydaniu.</span><span class="sxs-lookup"><span data-stu-id="d3541-124">This has been fixed in this release.</span></span> <span data-ttu-id="d3541-125">Zmiana cen i rzeczywistych rekordów w nowym zamapowanym projekcie zostanie zmieniona i poprawnie odtworzona na podstawie reguł kalkulacji cen i fakturowania w pozycji kontraktu.</span><span class="sxs-lookup"><span data-stu-id="d3541-125">Pricing and actual records on the newly mapped project will get reversed and re-created correctly based on the pricing and billing rules of the contract line.</span></span> <span data-ttu-id="d3541-126">Rzeczywista liczba rekordów zamapowanego projektu będzie również wyznaczona ponownie i w konsekwencji ponownie utworzona.</span><span class="sxs-lookup"><span data-stu-id="d3541-126">The actual records of the un-mapped project will also get re-evaluated and re-created as a consequence.</span></span>

    -   <span data-ttu-id="d3541-127">Naprawione: Dodano dodatkowe sprawdzanie w polu **Kwota** wiersza oszacowania, aby mieć pewność, że wartości puste nie będą utrwalone.</span><span class="sxs-lookup"><span data-stu-id="d3541-127">Fixed: Additional validation has been added to an estimate line’s **Amount** field to ensure that null values are not persisted.</span></span>

    -   <span data-ttu-id="d3541-128">Naprawione: Po zaktualizowaniu wartości rzeczywistych w projekcie w głównym formularzu projektu dodano przycisk Odśwież, który umożliwia użytkownikom ponowne zsynchronizowanie wartości rzeczywistych.</span><span class="sxs-lookup"><span data-stu-id="d3541-128">Fixed: When actuals have been updated on a project, a refresh button has been added to the project main form to allow users to re-sync the actuals.</span></span>

    -   <span data-ttu-id="d3541-129">Naprawione: Kiedy użytkownicy uaktualnią wersję z od 2.X do 3.X, dozwolone będą projekty o wartości PUSTEJ dla nazwy projektu.</span><span class="sxs-lookup"><span data-stu-id="d3541-129">Fixed: When users upgrade from 2.X to 3.X, projects with a NULL value for project name will be permitted.</span></span>

