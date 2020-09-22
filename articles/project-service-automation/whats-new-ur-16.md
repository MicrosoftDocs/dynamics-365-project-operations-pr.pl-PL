---
title: Nowości i zmiany w Project Service Automation, wydanie aktualizacji 16, wer. 3
description: W tym temacie przedstawiono funkcje i poprawki, które są dostepne w programie Project Service Automation, aktualizacja 16, wer. 3.
author: ruhercul
manager: kfend
ms.service: business-applications
ms.custom: dyn365-projectservice
ms.date: 02/18/2020
ms.topic: article
ms.prod: ''
ms.technology: Microsoft Dynamics 365 Project Service Automation 3.x
ms.assetid: b890a7b6-1664-4812-8732-fed77653cc05
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 0f4c206fd5b7a36d940e966b28c2437525812a98
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/24/2020
ms.locfileid: "3754322"
---
# <a name="project-service-automation-v3-update-release-16"></a><span data-ttu-id="363b9-103">Project Service Automation, wer. 3, aktualizacja wydania 16</span><span class="sxs-lookup"><span data-stu-id="363b9-103">Project Service Automation V3, Update Release 16</span></span>
<span data-ttu-id="363b9-104">Mamy przyjemność ogłosić najnowszą aktualizację aplikacji Project Service Automation dla Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="363b9-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="363b9-105">To wydanie obejmuje znaczną poprawę jakości, wydajności i użyteczności.</span><span class="sxs-lookup"><span data-stu-id="363b9-105">This release includes some important improvements to quality, performance, and usability.</span></span>

<span data-ttu-id="363b9-106">To wydanie jest zgodne z systemem Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="363b9-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="363b9-107">Aby zaktualizować do tej wersji, odwiedź Centrum administracyjne Dynamics 365 online i przejdź na stronę rozwiązań, aby zainstalować aktualizację.</span><span class="sxs-lookup"><span data-stu-id="363b9-107">To update to this release, visit the Admin Center for Dynamics 365 online, solutions page to install the update.</span></span> <span data-ttu-id="363b9-108">By uzyskać więcej informacji, zobacz [Instalowanie, aktualizowanie Preferowanego rozwiązania](https://docs.microsoft.com/dynamics365/project-service/upgrade-psa-home-page).</span><span class="sxs-lookup"><span data-stu-id="363b9-108">For more information, see [Install, Update a Preferred Solution](https://docs.microsoft.com/dynamics365/project-service/upgrade-psa-home-page).</span></span> <span data-ttu-id="363b9-109">W tym temacie przedstawiono funkcje i poprawki, które są nowe lub zostały zmienione w programie PSA, wer. 3, aktualizacja 16.</span><span class="sxs-lookup"><span data-stu-id="363b9-109">This topic lists the features and fixes that are new or changed for PSA V3, Update Release 16.</span></span> <span data-ttu-id="363b9-110">Numer tej kompilacji to V3.10.6.34 i jest on zazwyczaj dostępny za pośrednictwem samoaktualizacji w styczniu 2020 r.</span><span class="sxs-lookup"><span data-stu-id="363b9-110">This version has a build number of V3.10.6.34 and is generally available through a self-update in January 2020</span></span>

## <a name="update-release-16"></a><span data-ttu-id="363b9-111">Wydanie 16</span><span class="sxs-lookup"><span data-stu-id="363b9-111">Update Release 16</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="363b9-112">Poprawki błędów</span><span class="sxs-lookup"><span data-stu-id="363b9-112">Bug fixes</span></span>

-   <span data-ttu-id="363b9-113">Czas i wydatek</span><span class="sxs-lookup"><span data-stu-id="363b9-113">Time and Expense</span></span>

    -   <span data-ttu-id="363b9-114">Naprawione: Użytkownicy próbujący przesłać usunięte wpisy czasu i wydatków na potrzeby zatwierdzenia będą otrzymywać odpowiednie komunikaty o błędach.</span><span class="sxs-lookup"><span data-stu-id="363b9-114">Fixed: Users attempting to submit deleted time and expense entries for approvals will now receive relevant error messages.</span></span>

-   <span data-ttu-id="363b9-115">Zarządzanie projektem</span><span class="sxs-lookup"><span data-stu-id="363b9-115">Project Management</span></span>

    -   <span data-ttu-id="363b9-116">Poprawione: Jednostki zasobów zdefiniowane dla członków zespołu w szablonach są przestrzegane wraz z szablonami stosowanymi w nowym projekcie.</span><span class="sxs-lookup"><span data-stu-id="363b9-116">Fixed: The resourcing units defined for team members in templates are respected with the templates are applied to a new project.</span></span>

    -   <span data-ttu-id="363b9-117">Naprawione: poprawiono sposób obsługi ponownego przypisywania własności rekordu.</span><span class="sxs-lookup"><span data-stu-id="363b9-117">Fixed: Improved handling of the re-assignment of record ownership.</span></span>

    -   <span data-ttu-id="363b9-118">Naprawione: Projekty, które są w trakcie procesu kopiowania, nie będą dozwolone do skopiowania do momentu ukończenia wszystkich operacji kopiowania.</span><span class="sxs-lookup"><span data-stu-id="363b9-118">Fixed: Projects that are in the process of being copied will not be permitted to copied until all copy operations are complete.</span></span>

-   <span data-ttu-id="363b9-119">Zarządzanie zasobami</span><span class="sxs-lookup"><span data-stu-id="363b9-119">Resource Management</span></span>

    -   <span data-ttu-id="363b9-120">Naprawione: Rozszerz rezerwacje teraz poprawnie obsługuje krótkie czasy trwania i nie tworzy już zero godzin dla przedłużonych rezerwacji.</span><span class="sxs-lookup"><span data-stu-id="363b9-120">Fixed: Extend bookings now handles short durations correctly and no longer creates zero hours for extended bookings.</span></span>

    -   <span data-ttu-id="363b9-121">Naprawione: Widok uzgadniania jest teraz renderowany, gdy strefa czasowa projektu będzie wynosić +5:30 GMT, a tylko czas użytkownika jest inny.</span><span class="sxs-lookup"><span data-stu-id="363b9-121">Fixed: The reconciliation view now renders when the project time zone is +5:30 GMT and the user’s time aone is different.</span></span>

-   <span data-ttu-id="363b9-122">Sales</span><span class="sxs-lookup"><span data-stu-id="363b9-122">Sales</span></span>

    -   <span data-ttu-id="363b9-123">Naprawione: Po usunięciu projektu zamapowanego do pozycji kontraktu i zamapowaniu nowego projektu nie można ponownie oszacować rzeczywistych rekordów w nowym projekcie na podstawie reguł fakturowania i kalkulacji cen zdefiniowanych w pozycji kontraktu.</span><span class="sxs-lookup"><span data-stu-id="363b9-123">Fixed: When a project mapped to a contract line is removed and a new project is mapped, the actual records on the new project were not getting re-evaluated based on the billing and pricing rules defined on the contract line.</span></span> <span data-ttu-id="363b9-124">Ta funkcja została naprawiona w tym wydaniu.</span><span class="sxs-lookup"><span data-stu-id="363b9-124">This has been fixed in this release.</span></span> <span data-ttu-id="363b9-125">Zmiana cen i rzeczywistych rekordów w nowym zamapowanym projekcie zostanie zmieniona i poprawnie odtworzona na podstawie reguł kalkulacji cen i fakturowania w pozycji kontraktu.</span><span class="sxs-lookup"><span data-stu-id="363b9-125">Pricing and actual records on the newly mapped project will get reversed and re-created correctly based on the pricing and billing rules of the contract line.</span></span> <span data-ttu-id="363b9-126">Rzeczywista liczba rekordów zamapowanego projektu będzie również wyznaczona ponownie i w konsekwencji ponownie utworzona.</span><span class="sxs-lookup"><span data-stu-id="363b9-126">The actual records of the un-mapped project will also get re-evaluated and re-created as a consequence.</span></span>

    -   <span data-ttu-id="363b9-127">Naprawione: Dodano dodatkowe sprawdzanie w polu **Kwota** wiersza oszacowania, aby mieć pewność, że wartości puste nie będą utrwalone.</span><span class="sxs-lookup"><span data-stu-id="363b9-127">Fixed: Additional validation has been added to an estimate line’s **Amount** field to ensure that null values are not persisted.</span></span>

    -   <span data-ttu-id="363b9-128">Naprawione: Po zaktualizowaniu wartości rzeczywistych w projekcie w głównym formularzu projektu dodano przycisk Odśwież, który umożliwia użytkownikom ponowne zsynchronizowanie wartości rzeczywistych.</span><span class="sxs-lookup"><span data-stu-id="363b9-128">Fixed: When actuals have been updated on a project, a refresh button has been added to the project main form to allow users to re-sync the actuals.</span></span>

    -   <span data-ttu-id="363b9-129">Naprawione: Kiedy użytkownicy uaktualnią wersję z od 2.X do 3.X, dozwolone będą projekty o wartości PUSTEJ dla nazwy projektu.</span><span class="sxs-lookup"><span data-stu-id="363b9-129">Fixed: When users upgrade from 2.X to 3.X, projects with a NULL value for project name will be permitted.</span></span>

