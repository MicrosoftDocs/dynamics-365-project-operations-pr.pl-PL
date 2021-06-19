---
title: Nowości i zmiany w aplikacji Project Service Automation, wydanie 20, wer. 3
description: W tym temacie przedstawiono funkcje i poprawki, które są dostępne w programie Project Service Automation, aktualizacja 20, wer. 3
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 06/12/2020
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
ms.openlocfilehash: 5562b1de1d655328cfbb22e46c7fed53525507b3
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 05/10/2021
ms.locfileid: "6006524"
---
# <a name="project-service-automation-update-release-20-v3"></a><span data-ttu-id="9ab81-103">Project Service Automation, wydanie 20, wer. 3</span><span class="sxs-lookup"><span data-stu-id="9ab81-103">Project Service Automation Update Release 20, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="9ab81-104">Mamy przyjemność ogłosić najnowszą aktualizację aplikacji Project Service Automation dla Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="9ab81-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="9ab81-105">To wydanie obejmuje znaczną poprawę jakości, wydajności i użyteczności.</span><span class="sxs-lookup"><span data-stu-id="9ab81-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="9ab81-106">To wydanie jest zgodne z systemem Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="9ab81-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="9ab81-107">Aby zaktualizować do tej wersji, odwiedź centrum administracyjne Dynamics 365 online i przejdź na stronę rozwiązań, aby zainstalować aktualizację.</span><span class="sxs-lookup"><span data-stu-id="9ab81-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="9ab81-108">By uzyskać więcej informacji, zobacz [Instalowanie, aktualizowanie lub usuwanie preferowanego rozwiązania](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="9ab81-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="9ab81-109">W tym temacie przedstawiono funkcje i poprawki, które są nowe lub zostały zmienione w programie Project Service Automation, wer. 3, aktualizacja 20.</span><span class="sxs-lookup"><span data-stu-id="9ab81-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 20.</span></span> <span data-ttu-id="9ab81-110">Ta wersja ma numer kompilacji wer. 3.10.31.37 i zazwyczaj jest dostępna za pośrednictwem samoaktualizacji w czerwcu 2020 r.</span><span class="sxs-lookup"><span data-stu-id="9ab81-110">This version has a build number of V 3.10.31.37 and is generally available through a self-update in June 2020.</span></span>

## <a name="update-release-20"></a><span data-ttu-id="9ab81-111">Wydanie 20</span><span class="sxs-lookup"><span data-stu-id="9ab81-111">Update Release 20</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="9ab81-112">Poprawki błędów</span><span class="sxs-lookup"><span data-stu-id="9ab81-112">Bug fixes</span></span>

<span data-ttu-id="9ab81-113">**Zarządzanie projektem**</span><span class="sxs-lookup"><span data-stu-id="9ab81-113">**Project Management**</span></span>

<span data-ttu-id="9ab81-114">Rozwiązano następujące problemy:</span><span class="sxs-lookup"><span data-stu-id="9ab81-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="9ab81-115">Importowanie członków zespołu projektu przy użyciu metody alokacji, która wymaga użycia godzin, powoduje wyczyszczenie niejasnych komunikatów o błędach, kiedy określona liczba godzin jest równa zero.</span><span class="sxs-lookup"><span data-stu-id="9ab81-115">Importing project team members with an allocation method that requires hours results in an unclear error message when the specified hours are zero.</span></span>
- <span data-ttu-id="9ab81-116">Podczas wprowadzania przez użytkownika maksymalnej liczby znaków w polu **Opis** dla zadania w projekcie jest wyświetlany nieprawidłowy błąd.</span><span class="sxs-lookup"><span data-stu-id="9ab81-116">Users receive an incorrect error when the maximum number of characters have been entered into the **Description** field for a project task.</span></span>
- <span data-ttu-id="9ab81-117">Strona **Pobierz dodatek Microsoft Dynamics 365 Project Service Automation** przekierowuje do strony pobierania w języku angielskim, gdy ustawienia języka użytkownika są ustawione na japoński.</span><span class="sxs-lookup"><span data-stu-id="9ab81-117">The **Microsoft Dynamics 365 Project Service Automation add-in download** page redirects to the English download page when the user’s language settings are set to Japanese.</span></span>
- <span data-ttu-id="9ab81-118">Kiedy wystąpi błąd serwera, etykieta synchronizacji na karcie **Harmonogram** w formularzu **Projekty** pozostaje niekiedy w programie.</span><span class="sxs-lookup"><span data-stu-id="9ab81-118">When a server error occurs, the synchronization label on the **Schedule** tab of the **Projects** form sometimes remains.</span></span>
- <span data-ttu-id="9ab81-119">Gdy zadanie jest modyfikowane, nadmiarowe aktualizacje zadań są wysyłane na serwer.</span><span class="sxs-lookup"><span data-stu-id="9ab81-119">Redundant task updates are being sent to the server when a task is modified.</span></span>

<span data-ttu-id="9ab81-120">**Sales**</span><span class="sxs-lookup"><span data-stu-id="9ab81-120">**Sales**</span></span>

<span data-ttu-id="9ab81-121">Rozwiązano następujące problemy:</span><span class="sxs-lookup"><span data-stu-id="9ab81-121">The following issues have been fixed:</span></span>

- <span data-ttu-id="9ab81-122">W formularzu **Kontraktu** dwukrotne kliknięcie pozycji **Utwórz fakturę** tworzy dwie faktury dla pojedynczego rekordu wartości rzeczywistych.</span><span class="sxs-lookup"><span data-stu-id="9ab81-122">On the **Contract** form, double-clicking **Create Invoice** creates two invoices for a single actuals record.</span></span>
- <span data-ttu-id="9ab81-123">Użytkownicy przeglądarki Internet Explorer 11 nie mają możliwości utworzenia wpisów wydatków.</span><span class="sxs-lookup"><span data-stu-id="9ab81-123">In Internet Explorer 11, users are unable to create expense entries.</span></span>
- <span data-ttu-id="9ab81-124">Wycofanie kosztów i wycofanie z niezfakturowanych wartości rzeczywistych nie jest powiązane.</span><span class="sxs-lookup"><span data-stu-id="9ab81-124">Reversal of Cost and reversal of Unbilled Sales Actuals are not linked.</span></span>
- <span data-ttu-id="9ab81-125">Przycisk **Odśwież rzeczywiste** w formularzu **Projekt** nie powoduje odświeżenia **Godzin rzeczywistych zadania**.</span><span class="sxs-lookup"><span data-stu-id="9ab81-125">The **Refresh Actuals** button on the **Project** form does not refresh **Task Actual Hours**.</span></span>
- <span data-ttu-id="9ab81-126">Dodatek **PreValidateProjectTeamMemberCreate** może tworzyć duplikaty ogólych zasobów możliwych do zarezerwowania, gdy atrybut **msdyn_isgenericresourceprojectscoped** jest ustawiony na **Fałsz**.</span><span class="sxs-lookup"><span data-stu-id="9ab81-126">The **PreValidateProjectTeamMemberCreate** plug-in can create duplicate generic bookable resources when the attribute **msdyn_isgenericresourceprojectscoped** is set to **False**.</span></span>
- <span data-ttu-id="9ab81-127">**Ponowne obliczenie** czyści koszty zakupu dotyczące szczegółów wiersza oferty opartej na produkcie i szczegółów pozycji kontraktu.</span><span class="sxs-lookup"><span data-stu-id="9ab81-127">**Recalculate** clears chargeable costs of product-based quote line details and contract line details.</span></span>
- <span data-ttu-id="9ab81-128">W określonych scenariuszach dodatek **PostEstimateLineUpdate** wyświetla wartość null i błąd wyjątków odwołania.</span><span class="sxs-lookup"><span data-stu-id="9ab81-128">In specific scenarios, the **PostEstimateLineUpdate** plug-in displays a null teference exception error.</span></span>
- <span data-ttu-id="9ab81-129">Czas trwania fazy czasu na **Wykresie analizy wydajności** nie pasuje do czasu trwania kosztów w szczegółach wiersza oferty z ceną ustaloną dla oferty.</span><span class="sxs-lookup"><span data-stu-id="9ab81-129">Time phase duration on the **Profitability Analysis Chart** does not match duration of the costs in the fixed-price quote line detail of the quote.</span></span>
- <span data-ttu-id="9ab81-130">Wartości jednostek i grupy jednostek nie są poprawnie domyślne dla kategorii wydatków w formularzach **Szczegółów pozycji kontraktu** i **Szczegółów wiersza oferty**.</span><span class="sxs-lookup"><span data-stu-id="9ab81-130">Unit and unit group values do not default correctly for expense categories on the **Contract Line Details** and **Quote Line Details** forms.</span></span>
- <span data-ttu-id="9ab81-131">**Zestawienie kosztów własnych jednostki organizacyjnej** zezwalają na nakładanie się dnia wejścia w życie.</span><span class="sxs-lookup"><span data-stu-id="9ab81-131">**Org Unit Cost Price** lists permit overlaps in the date effectivity.</span></span>
- <span data-ttu-id="9ab81-132">Użytkownicy nie mogą zmieniać składnika **OrgUnit**, kiedy typ zamówienia nie jest związany z pracą, ponieważ jego wartość powoduje błąd wyjątku odwołania do wartości null.</span><span class="sxs-lookup"><span data-stu-id="9ab81-132">Users are not permitted to change the **OrgUnit** when the order type is not work-based because it will lead to a null reference exception error.</span></span>
- <span data-ttu-id="9ab81-133">Podczas próby przejścia do nawigacji z poziomu formularza **Szczegóły wiersza oferty,** powrót do karty **Oferta** powoduje odświeżenie formularza i wyświetlenie karty **Podsumowanie**.</span><span class="sxs-lookup"><span data-stu-id="9ab81-133">When attempting to navigate from the **Quote Line Details** form, back to the **Quote** tab, the form refreshes and displays the **Summary** tab.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]