---
title: Strona główna uaktualnienia
description: W tym temacie przedstawiono miejsca, w których można znaleźć ważne informacje dotyczące nowych i zmienionych funkcji w programie Dynamics 365 Project Service Automation, oraz proces uaktualniania do najnowszej wersji.
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 05/30/2019
ms.topic: article
author: rumant
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: fa25d069de8098c0e8788c9ebb8aa3426eec5db9
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/28/2020
ms.locfileid: "4121771"
---
# <a name="upgrade-home-page"></a><span data-ttu-id="e547e-103">Strona główna uaktualnienia</span><span class="sxs-lookup"><span data-stu-id="e547e-103">Upgrade home page</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

## <a name="upgrade-from-psa-version-2x-or-1x-to-version-3x"></a><span data-ttu-id="e547e-104">Uaktualnij aplikację PSA z wersji 2.x lub 1.x do wersji 3.x</span><span class="sxs-lookup"><span data-stu-id="e547e-104">Upgrade from PSA version 2.x or 1.x to version 3.x</span></span>

### <a name="new-instances"></a><span data-ttu-id="e547e-105">Nowe wystąpienia</span><span class="sxs-lookup"><span data-stu-id="e547e-105">New instances</span></span>

<span data-ttu-id="e547e-106">Od 17 maja 2019 r. po wybraniu programu Project Service Automation podczas inicjowania obsługi administracyjnej nowego wystąpienia domyślnie będzie instalowana wersja 3.x.</span><span class="sxs-lookup"><span data-stu-id="e547e-106">As of May 17, 2019, when Project Service Automation is selected during the provisioning of a new instance, version 3.x is installed by default.</span></span>

### <a name="existing-instances"></a><span data-ttu-id="e547e-107">Istnieją wystąpienia</span><span class="sxs-lookup"><span data-stu-id="e547e-107">Existing instances</span></span>

<span data-ttu-id="e547e-108">Wcześniej klienci, którzy mieli wystąpienie programu PSA w wersji 2.x i potrzebowali aktualizacji do wersji 3.x, która jest wersją programu PSA wyposażoną w ujednolicony interfejs klienta (UCI), musieli się skontaktować z działem pomocy technicznej firmy Microsoft i przekazać informacje dotyczące posiadanego wystąpienia, tak aby dział pomocy technicznej mógł przygotować uaktualnienie do wersji 3.x.</span><span class="sxs-lookup"><span data-stu-id="e547e-108">Previously, customers who have an instance of PSA version 2.x and needed to upgrade to version 3.x, which is the Unified client interface-based (UCI) version of PSA , had to contact Microsoft Support and provide the details of thier instance so that support could enable the instance for upgrade to version 3.x.</span></span> <span data-ttu-id="e547e-109">Od 1 marca, 2020, klienci, którzy mają wystąpienie PSA w wersji 2.x, muszą uaktualnić je do wersji 3. x, będą mogli uaktualnić swoje wystąpienia bezpośrednio z portalu administracyjnego bez konieczności kontaktowania się z pomocą techniczną firmy Microsoft.</span><span class="sxs-lookup"><span data-stu-id="e547e-109">As of March 1st, 2020, customers who have an instance of PSA version 2.x and need to upgrade to version 3.x, will able to upgrade their instances directly from the Admin portal without having to contact Microsoft Support.</span></span>  

> [!NOTE]
> <span data-ttu-id="e547e-110">Program PSA w wersji 3.x zawiera istotne zmiany.</span><span class="sxs-lookup"><span data-stu-id="e547e-110">PSA version 3.x includes significant changes.</span></span> <span data-ttu-id="e547e-111">Został oparty na strukturze ujednoliconego interfejsu w celu ułatwienia obsługi użytkownikom.</span><span class="sxs-lookup"><span data-stu-id="e547e-111">It has been built on the Unified Interface framework to help provide an improved user experience.</span></span> <span data-ttu-id="e547e-112">Przeprojektowana aplikacja oferuje spójny, jednolity interfejs użytkownika, który jest łatwy w obsłudze i zapewnia dobrą widoczność na wszystkich ekranach bez względu na ich wielkość.</span><span class="sxs-lookup"><span data-stu-id="e547e-112">The redesigned app delivers a consistent, uniform user interface (UI), and it follows responsive design principles for optimal viewing on any screen size or device.</span></span> <span data-ttu-id="e547e-113">W całej aplikacji wprowadzono wiele innych zmian.</span><span class="sxs-lookup"><span data-stu-id="e547e-113">There have been other changes throughout the application.</span></span> <span data-ttu-id="e547e-114">Zmodyfikowane obszary obejmują kalkulację cen, rezerwację i przypisywanie zasobów oraz zarządzanie okresami, wydatkami i zatwierdzeniami.</span><span class="sxs-lookup"><span data-stu-id="e547e-114">Some of the areas that have been changed include pricing, booking and assigning resources, time, expenses, and approvals.</span></span>

<span data-ttu-id="e547e-115">Zalecamy, aby przed rozpoczęciem procesu uaktualniania wykonać następujące zadania:</span><span class="sxs-lookup"><span data-stu-id="e547e-115">Before you begin the upgrade process, we recommend that you complete the following tasks:</span></span>

- <span data-ttu-id="e547e-116">Sprawdź, czy na wybranym urządzeniu są zainstalowane programy Dynamics 365 Field Service i Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="e547e-116">Verify whether both Dynamics 365 Field Service and Project Service Automation are installed on the identified instance.</span></span> <span data-ttu-id="e547e-117">Jeśli są zainstalowane oba rozwiązania, należy zaplanować ich uaktualnienie przed wznowieniem regularnego korzystania z wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="e547e-117">If both solutions are installed, you should plan to upgrade both before you resume regular use of the instance.</span></span>
- <span data-ttu-id="e547e-118">Uważnie przejrzyj poniższe tematy.</span><span class="sxs-lookup"><span data-stu-id="e547e-118">Carefully review the following topics.</span></span> <span data-ttu-id="e547e-119">Znajomość i zrozumienie zmian dokonanych między wersjami pomogą w prawidłowym uaktualnieniu.</span><span class="sxs-lookup"><span data-stu-id="e547e-119">Awareness and understanding of the changes between versions will help you with the upgrade process.</span></span> <span data-ttu-id="e547e-120">Te tematy zawierają informacje o zasadniczych zmianach w programie PSA oraz uwagi i zalecenia dotyczące planowania uaktualnienia do wersji 3.x.</span><span class="sxs-lookup"><span data-stu-id="e547e-120">These topics provide information about the major changes in PSA, together with considerations and recommendations for planning your upgrade to version 3.x.</span></span>

    - [<span data-ttu-id="e547e-121">Nowości i zmiany w programie Project Service Automation w wersji 3</span><span class="sxs-lookup"><span data-stu-id="e547e-121">What's new or changed in Project Service Automation version 3</span></span>](whats-new-changed-v3.md)
    - [<span data-ttu-id="e547e-122">Zagadnienia dotyczące uaktualniania — Project Service Automation z wersji 2.x lub 1.x do wersji 3.x</span><span class="sxs-lookup"><span data-stu-id="e547e-122">Upgrade considerations - Project Service Automation version 2.x or 1.x to version 3</span></span>](upgrade-v3.md)

- <span data-ttu-id="e547e-123">Uaktualnij wystąpienie piaskownicy, aby ocenić zmiany w posiadanej implementacji przed uaktualnieniem wystąpienia produkcyjnego.</span><span class="sxs-lookup"><span data-stu-id="e547e-123">Upgrade your sandbox instance to evaluate the changes in your implementation before you upgrade your production instance.</span></span>

<span data-ttu-id="e547e-124">Gdy już przejrzysz tematy wspomniane wcześniej i przygotujesz wszystko do uaktualnienia do programu PSA w wersji 3.x lub innej wersji z interfejsem UCI, prześlij do działu pomocy technicznej Microsoft prośbę o dodanie opcji uaktualnienia do Centrum administracyjnego.</span><span class="sxs-lookup"><span data-stu-id="e547e-124">After you've reviewed the topics that were mentioned earlier and are ready to upgrade to PSA version 3.x or the UCI-based version, submit a request to Microsoft support to make the upgrade available from Admin center.</span></span> <span data-ttu-id="e547e-125">We wniosku wprowadź szczegółowe informacje o swoim wystąpieniu.</span><span class="sxs-lookup"><span data-stu-id="e547e-125">In your request, provide the details of your instance.</span></span>

## <a name="older-versions-of-psa-psa-version-2x-in-a-newly-created-instance"></a><span data-ttu-id="e547e-126">Starsze wersje rozwiązania PSA (PSA 2.x) w nowo utworzonym wystąpieniu</span><span class="sxs-lookup"><span data-stu-id="e547e-126">Older versions of PSA (PSA version 2.x) in a newly created instance</span></span>

<span data-ttu-id="e547e-127">Od 17 maja 2019 r. wszystkie nowe wystąpienia będą domyślnie używały klienta UCI.</span><span class="sxs-lookup"><span data-stu-id="e547e-127">As of May 17, 2019, all new instances will have UCI as the default client.</span></span> <span data-ttu-id="e547e-128">W celu zapewnienia zgodności z tą zmianą domyślnie będzie inicjowana obsługa administracyjna programów PSA w wersji 3.x i Field Service w wersji 8.x, ponieważ te wersje są przewidziane do współpracy z klientem UCI.</span><span class="sxs-lookup"><span data-stu-id="e547e-128">For alignment with this change, PSA version 3.x and Field Service version 8.x will be provisioned by default, because these versions are designed to work with the UCI client.</span></span>

<span data-ttu-id="e547e-129">Począwszy od pierwszego marce 2020, klienci aplikacji Dynamics PSA nie będą mogli tworzyć nowych środowisk z programem PSA w starszych wersjach, na przykład PSA w wersji 2.x lub starszej.</span><span class="sxs-lookup"><span data-stu-id="e547e-129">Starting March 1st 2020, customers of Dynamics PSA will no longer be able to create a new environments with older versions of PSA, for example PSA version 2.x or lower.</span></span> <span data-ttu-id="e547e-130">Każde nowe środowisko będzie wyłącznie w wersji 3.x PSA.</span><span class="sxs-lookup"><span data-stu-id="e547e-130">Any new environment will be to get only version 3.x of PSA.</span></span>

> [!NOTE]
> <span data-ttu-id="e547e-131">Aby osiągnąć najlepszy efekt podczas korzystania ze starszych wersji aplikacji Field Service i PSA, przejdź do strony **Ustawienia systemu** i w polu **Używaj tylko nowego ujednoliconego interfejsu (zalecane)** zaznacz wartość **Nie**, ponieważ te wersje nie są zaprojektowane do poprawnego ładowania w interfejsie UCI.</span><span class="sxs-lookup"><span data-stu-id="e547e-131">For the best experience when you use older versions of the Field Service and PSA applications, go to the **System settings** page and for the field, **Use the new Unified Interface only (recommended)** field, select **No** as these versions aren't designed to be correctly loaded in UCI.</span></span> <span data-ttu-id="e547e-132">Po wyłączeniu interfejsu UCI można otwierać i uruchamiać te wersje programów Field Service i PSA przy użyciu starego klienta sieci Web.</span><span class="sxs-lookup"><span data-stu-id="e547e-132">After you have turned off UCI, you can open and run these versions of Field Service and PSA by using the old web client.</span></span> 
