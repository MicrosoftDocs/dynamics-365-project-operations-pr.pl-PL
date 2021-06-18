---
title: Nowości i zmiany w aplikacji Project Service Automation, wydanie 31, wer. 3
description: W tym temacie przedstawiono funkcje i poprawki, które są dostepne w programie Project Service Automation, aktualizacja 31, wer. 3.
author: ruhercul
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
ms.openlocfilehash: 160187ba7b96547e85a7a4ec4bf84c86d8fd8257
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 05/10/2021
ms.locfileid: "5999144"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-31-v3"></a><span data-ttu-id="326a5-103">Nowości i zmiany w aplikacji Project Service Automation, wydanie 31, wer. 3</span><span class="sxs-lookup"><span data-stu-id="326a5-103">What's new or changed in Project Service Automation Update Release 31, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="326a5-104">Mamy przyjemność ogłosić najnowszą aktualizację aplikacji Project Service Automation dla Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="326a5-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="326a5-105">To wydanie obejmuje znaczną poprawę jakości, wydajności i użyteczności.</span><span class="sxs-lookup"><span data-stu-id="326a5-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="326a5-106">To wydanie jest zgodne z systemem Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="326a5-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="326a5-107">Aby zaktualizować do tej wersji, odwiedź centrum administracyjne Dynamics 365 online i przejdź na stronę rozwiązań, aby zainstalować aktualizację.</span><span class="sxs-lookup"><span data-stu-id="326a5-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="326a5-108">By uzyskać więcej informacji, zobacz [Instalowanie, aktualizowanie lub usuwanie preferowanego rozwiązania](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="326a5-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="326a5-109">W tym temacie przedstawiono funkcje i poprawki, które są nowe lub zostały zmienione w programie Project Service Automation, wer. 3, aktualizacja 31.</span><span class="sxs-lookup"><span data-stu-id="326a5-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 31.</span></span> <span data-ttu-id="326a5-110">Ta wersja ma numer kompilacji wer. 3.10.52.77 i zazwyczaj jest dostępna za pośrednictwem samoaktualizacji w maju 2021 r.</span><span class="sxs-lookup"><span data-stu-id="326a5-110">This version has a build number of V3.10.52.77 and is generally available through a self-update in May 2021.</span></span>

## <a name="update-release-31"></a><span data-ttu-id="326a5-111">Wydanie 31</span><span class="sxs-lookup"><span data-stu-id="326a5-111">Update Release 31</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="326a5-112">Poprawki błędów</span><span class="sxs-lookup"><span data-stu-id="326a5-112">Bug fixes</span></span>

<span data-ttu-id="326a5-113">**Czas i wydatek**</span><span class="sxs-lookup"><span data-stu-id="326a5-113">**Time and Expense**</span></span>

<span data-ttu-id="326a5-114">Rozwiązano następujące problemy:</span><span class="sxs-lookup"><span data-stu-id="326a5-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="326a5-115">Przyciski poleceń formantu wprowadzania czasu na stronie **Zasoby do zarezerwowania** nie były mylące.</span><span class="sxs-lookup"><span data-stu-id="326a5-115">Time entry control command buttons on the **Bookable Resource** page were confusing.</span></span>
- <span data-ttu-id="326a5-116">Podczas zatwierdzania wpisu czasowego w **Project.SetTrackingFields** generowany był wyjątek null reference.</span><span class="sxs-lookup"><span data-stu-id="326a5-116">A null reference exception was generated in **Project.SetTrackingFields** when approving a time entry.</span></span>

<span data-ttu-id="326a5-117">**Zarządzanie zasobami**</span><span class="sxs-lookup"><span data-stu-id="326a5-117">**Resource Management**</span></span>

<span data-ttu-id="326a5-118">Rozwiązano następujące problemy:</span><span class="sxs-lookup"><span data-stu-id="326a5-118">The following issues have been fixed:</span></span>

- <span data-ttu-id="326a5-119">**Utwórz członka zespołu** nie wyświetla poprawnie ustawienia metadanych ustawień rezerwacji dla **Domyślnego statusu rezerwacji zaangażowanej**.</span><span class="sxs-lookup"><span data-stu-id="326a5-119">**Create Team Member** doesn't correctly display the booking setup metadata setting for **Default Booking Committed Status**.</span></span>
- <span data-ttu-id="326a5-120">W przypadku uaktualnienia z wersji PSA 1.X do 3.X proces uaktualniania kończy się niepowodzeniem: **UpgradeResourceRequirements**.</span><span class="sxs-lookup"><span data-stu-id="326a5-120">When upgrading from PSA 1.X to 3.X, the upgrade process fails at **UpgradeResourceRequirements**.</span></span>


<span data-ttu-id="326a5-121">**Sprzedaż**</span><span class="sxs-lookup"><span data-stu-id="326a5-121">**Sales**</span></span>

<span data-ttu-id="326a5-122">Rozwiązano następujące problemy:</span><span class="sxs-lookup"><span data-stu-id="326a5-122">The following issues have been fixed:</span></span>

- <span data-ttu-id="326a5-123">Przychód rzeczywisty konwertuje kwoty na walutę projektu w siatce śledzenia.</span><span class="sxs-lookup"><span data-stu-id="326a5-123">Actual revenue converts the amounts to the project currency in the tracking grid.</span></span>
- <span data-ttu-id="326a5-124">Domyślna waluta jest niejasna podczas tworzenia wierszy dziennika, wierszy wyceny i wierszy umowy w scenariuszach, w których waluta podstawowa organizacji różni się od waluty projektu.</span><span class="sxs-lookup"><span data-stu-id="326a5-124">The currency default is unclear when creating journal lines, quote lines, and contract lines in scenarios where an organization's base currency differs from the project currency.</span></span>
- <span data-ttu-id="326a5-125">**Oczekiwanie na korektę weryfikacji dziennika** — zapytanie nie jest filtrowane według projektu.</span><span class="sxs-lookup"><span data-stu-id="326a5-125">**Pending correction journal validation** query doesn't filter by project.</span></span>
- <span data-ttu-id="326a5-126">Pozostała sprzedaż jest obliczana niepoprawnie w projekcie.</span><span class="sxs-lookup"><span data-stu-id="326a5-126">Remaining sales are calculated incorrectly on a project.</span></span>
- <span data-ttu-id="326a5-127">Oferty oparte na kontakcie nie są tworzone bez cennika.</span><span class="sxs-lookup"><span data-stu-id="326a5-127">Quotes based on a contact fail when they are created without a price list.</span></span>
- <span data-ttu-id="326a5-128">Po wybraniu opcji **Potwierdź fakturę** nie jest wyświetlana ikona przetwarzania.</span><span class="sxs-lookup"><span data-stu-id="326a5-128">No processing spinner is shown when you select **Confirm Invoice**.</span></span>
- <span data-ttu-id="326a5-129">Po wybraniu opcji **Utwórz fakturę** nie jest wyświetlana ikona przetwarzania.</span><span class="sxs-lookup"><span data-stu-id="326a5-129">No processing spinner is shown when you select **Create Invoice**.</span></span>
- <span data-ttu-id="326a5-130">Zamknięcie oferty jako utraconej nie anulowało rezerwacji.</span><span class="sxs-lookup"><span data-stu-id="326a5-130">Closing a quote as lost doesn't cancel the bookings.</span></span>







