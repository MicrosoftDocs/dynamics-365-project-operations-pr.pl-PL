---
title: Nowości i zmiany w aplikacji Project Service Automation, wydanie 31, wer. 3
description: W tym temacie przedstawiono funkcje i poprawki, które są dostepne w programie Project Service Automation, aktualizacja 31, wer. 3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 04/26/2021
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
ms.openlocfilehash: a595c0a129ac35d3416984e57908e73e1eaef2fd
ms.sourcegitcommit: 6e1498502461e86cff722ccaf8795ff11c7c47ad
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/27/2021
ms.locfileid: "5945548"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-31-v3"></a><span data-ttu-id="d24d9-103">Nowości i zmiany w aplikacji Project Service Automation, wydanie 31, wer. 3</span><span class="sxs-lookup"><span data-stu-id="d24d9-103">What's new or changed in Project Service Automation Update Release 31, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="d24d9-104">Mamy przyjemność ogłosić najnowszą aktualizację aplikacji Project Service Automation dla Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="d24d9-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="d24d9-105">To wydanie obejmuje znaczną poprawę jakości, wydajności i użyteczności.</span><span class="sxs-lookup"><span data-stu-id="d24d9-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="d24d9-106">To wydanie jest zgodne z systemem Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="d24d9-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="d24d9-107">Aby zaktualizować do tej wersji, odwiedź centrum administracyjne Dynamics 365 online i przejdź na stronę rozwiązań, aby zainstalować aktualizację.</span><span class="sxs-lookup"><span data-stu-id="d24d9-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="d24d9-108">By uzyskać więcej informacji, zobacz [Instalowanie, aktualizowanie lub usuwanie preferowanego rozwiązania](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="d24d9-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="d24d9-109">W tym temacie przedstawiono funkcje i poprawki, które są nowe lub zostały zmienione w programie Project Service Automation, wer. 3, aktualizacja 31.</span><span class="sxs-lookup"><span data-stu-id="d24d9-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 31.</span></span> <span data-ttu-id="d24d9-110">Ta wersja ma numer kompilacji wer. 3.10.52.77 i zazwyczaj jest dostępna za pośrednictwem samoaktualizacji w maju 2021 r.</span><span class="sxs-lookup"><span data-stu-id="d24d9-110">This version has a build number of V3.10.52.77 and is generally available through a self-update in May 2021.</span></span>

## <a name="update-release-31"></a><span data-ttu-id="d24d9-111">Wydanie 31</span><span class="sxs-lookup"><span data-stu-id="d24d9-111">Update Release 31</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="d24d9-112">Poprawki błędów</span><span class="sxs-lookup"><span data-stu-id="d24d9-112">Bug fixes</span></span>

<span data-ttu-id="d24d9-113">**Czas i wydatek**</span><span class="sxs-lookup"><span data-stu-id="d24d9-113">**Time and Expense**</span></span>

<span data-ttu-id="d24d9-114">Rozwiązano następujące problemy:</span><span class="sxs-lookup"><span data-stu-id="d24d9-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="d24d9-115">Przyciski poleceń formantu wprowadzania czasu na stronie **Zasoby do zarezerwowania** nie były mylące.</span><span class="sxs-lookup"><span data-stu-id="d24d9-115">Time entry control command buttons on the **Bookable Resource** page were confusing.</span></span>
- <span data-ttu-id="d24d9-116">Podczas zatwierdzania wpisu czasowego w **Project.SetTrackingFields** generowany był wyjątek null reference.</span><span class="sxs-lookup"><span data-stu-id="d24d9-116">A null reference exception was generated in **Project.SetTrackingFields** when approving a time entry.</span></span>

<span data-ttu-id="d24d9-117">**Zarządzanie zasobami**</span><span class="sxs-lookup"><span data-stu-id="d24d9-117">**Resource Management**</span></span>

<span data-ttu-id="d24d9-118">Rozwiązano następujące problemy:</span><span class="sxs-lookup"><span data-stu-id="d24d9-118">The following issues have been fixed:</span></span>

- <span data-ttu-id="d24d9-119">**Utwórz członka zespołu** nie wyświetla poprawnie ustawienia metadanych ustawień rezerwacji dla **Domyślnego statusu rezerwacji zaangażowanej**.</span><span class="sxs-lookup"><span data-stu-id="d24d9-119">**Create Team Member** doesn't correctly display the booking setup metadata setting for **Default Booking Committed Status**.</span></span>
- <span data-ttu-id="d24d9-120">W przypadku uaktualnienia z wersji PSA 1.X do 3.X proces uaktualniania kończy się niepowodzeniem: **UpgradeResourceRequirements**.</span><span class="sxs-lookup"><span data-stu-id="d24d9-120">When upgrading from PSA 1.X to 3.X, the upgrade process fails at **UpgradeResourceRequirements**.</span></span>


<span data-ttu-id="d24d9-121">**Sprzedaż**</span><span class="sxs-lookup"><span data-stu-id="d24d9-121">**Sales**</span></span>

<span data-ttu-id="d24d9-122">Rozwiązano następujące problemy:</span><span class="sxs-lookup"><span data-stu-id="d24d9-122">The following issues have been fixed:</span></span>

- <span data-ttu-id="d24d9-123">Przychód rzeczywisty konwertuje kwoty na walutę projektu w siatce śledzenia.</span><span class="sxs-lookup"><span data-stu-id="d24d9-123">Actual revenue converts the amounts to the project currency in the tracking grid.</span></span>
- <span data-ttu-id="d24d9-124">Domyślna waluta jest niejasna podczas tworzenia wierszy dziennika, wierszy wyceny i wierszy umowy w scenariuszach, w których waluta podstawowa organizacji różni się od waluty projektu.</span><span class="sxs-lookup"><span data-stu-id="d24d9-124">The currency default is unclear when creating journal lines, quote lines, and contract lines in scenarios where an organization's base currency differs from the project currency.</span></span>
- <span data-ttu-id="d24d9-125">**Oczekiwanie na korektę weryfikacji dziennika** — zapytanie nie jest filtrowane według projektu.</span><span class="sxs-lookup"><span data-stu-id="d24d9-125">**Pending correction journal validation** query doesn't filter by project.</span></span>
- <span data-ttu-id="d24d9-126">Pozostała sprzedaż jest obliczana niepoprawnie w projekcie.</span><span class="sxs-lookup"><span data-stu-id="d24d9-126">Remaining sales are calculated incorrectly on a project.</span></span>
- <span data-ttu-id="d24d9-127">Oferty oparte na kontakcie nie są tworzone bez cennika.</span><span class="sxs-lookup"><span data-stu-id="d24d9-127">Quotes based on a contact fail when they are created without a price list.</span></span>
- <span data-ttu-id="d24d9-128">Po wybraniu opcji **Potwierdź fakturę** nie jest wyświetlana ikona przetwarzania.</span><span class="sxs-lookup"><span data-stu-id="d24d9-128">No processing spinner is shown when you select **Confirm Invoice**.</span></span>
- <span data-ttu-id="d24d9-129">Po wybraniu opcji **Utwórz fakturę** nie jest wyświetlana ikona przetwarzania.</span><span class="sxs-lookup"><span data-stu-id="d24d9-129">No processing spinner is shown when you select **Create Invoice**.</span></span>
- <span data-ttu-id="d24d9-130">Zamknięcie oferty jako utraconej nie anulowało rezerwacji.</span><span class="sxs-lookup"><span data-stu-id="d24d9-130">Closing a quote as lost doesn't cancel the bookings.</span></span>







