---
title: Rejestracja w przeglądzie subskrypcji Project Operations w ramach scenariuszy zasobów / zasobów niemagazynowanych
description: W tym temacie zamieszczono informacje dotyczące sposobu subskrypcji i wdrożenia Project Operations do obsługi zasobów i zasobów niemagazynowanych.
author: sigitac
ms.date: 07/02/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: da93fcf23ee3f255812842e31cb22b5d39daa963
ms.sourcegitcommit: 52b26950bb3b1596ad81aa4ff91745ee9615d1b0
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/02/2021
ms.locfileid: "6334840"
---
# <a name="sign-up-for-project-operations-preview-subscriptions-for-resource-non-stocked-scenarios"></a><span data-ttu-id="c47c9-103">Rejestracja w przeglądzie subskrypcji Project Operations w ramach scenariuszy zasobów / zasobów niemagazynowanych</span><span class="sxs-lookup"><span data-stu-id="c47c9-103">Sign up for Project Operations preview subscriptions for resource/ non-stocked scenarios</span></span>

<span data-ttu-id="c47c9-104">_**Zastosowane do:** Project Operations dla zasobów/scenariuszy nieopartych na zaopatrzeniu_</span><span class="sxs-lookup"><span data-stu-id="c47c9-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="c47c9-105">Ten temat wyjaśnia, jak subskrybować ofertę wersji próbnej i wdrożyć środowisko aplikacji Project Operations dla scenariuszy obejmujących zasoby/nieobejmujących magazynowania.</span><span class="sxs-lookup"><span data-stu-id="c47c9-105">This topic explains how to subscribe to the trial offer and deploy Project Operations environment for resource/non-stocked based scenarios.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="c47c9-106">Wymagania wstępne</span><span class="sxs-lookup"><span data-stu-id="c47c9-106">Prerequisites</span></span>
- <span data-ttu-id="c47c9-107">Użytkownik wdrażający wersję zapoznawczą musi posiadać prawa administratora globalnego dzierżawy Azure.</span><span class="sxs-lookup"><span data-stu-id="c47c9-107">The user who deploys the preview must have Azure tenant global administrator rights.</span></span> <span data-ttu-id="c47c9-108">Dzierżawcę można utworzyć podczas realizowania pierwszej oferty.</span><span class="sxs-lookup"><span data-stu-id="c47c9-108">You can create a tenant during the first offer redemption.</span></span> 
- <span data-ttu-id="c47c9-109">Wdrożenie środowiska Finance wymaga poprawnej subskrypcji Azure, która będzie rozliczana w ramach poszczególnego środowiska.</span><span class="sxs-lookup"><span data-stu-id="c47c9-109">Deploying a Finance environment requires a valid Azure subscription that will be billed per environment.</span></span> <span data-ttu-id="c47c9-110">Aby rozpocząć, należy użyć istniejącej subskrypcji lub [wersji próbnej usługi Azure](https://azure.microsoft.com/en-us/free/).</span><span class="sxs-lookup"><span data-stu-id="c47c9-110">You can use your organizations existing subscription or use an [Azure trial](https://azure.microsoft.com/en-us/free/) to get started.</span></span> <span data-ttu-id="c47c9-111">Środowisko CDS jest dostępne bezpłatnie przez okres 30 dni.</span><span class="sxs-lookup"><span data-stu-id="c47c9-111">The CDS environment will be provided free for a limited 30 day period.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c47c9-112">To zadanie musi wykonać tylko jedna osoba — administrator dzierżawy w organizacji.</span><span class="sxs-lookup"><span data-stu-id="c47c9-112">Only one person, the tenant administrator, in an organization needs to perform this task.</span></span> <span data-ttu-id="c47c9-113">Jeśli nie jesteś subskrybentem tej wersji, zaczekaj, aż organizacja się zarejestruje i otrzymasz swoje poświadczenia użytkownika.</span><span class="sxs-lookup"><span data-stu-id="c47c9-113">If you aren't the subscriber to this release, wait until your organization has been signed up and you've received your user credentials.</span></span>
> 
> <span data-ttu-id="c47c9-114">Wersje próbne można używać raz w ramach dzierżawcy.</span><span class="sxs-lookup"><span data-stu-id="c47c9-114">Trials are single use in the tenant.</span></span> <span data-ttu-id="c47c9-115">Wersję próbną można uruchomić tylko raz.</span><span class="sxs-lookup"><span data-stu-id="c47c9-115">You can only run a trial one time.</span></span> <span data-ttu-id="c47c9-116">Na potrzeby wersji próbnej zalecamy utworzenie nowego dzierżawcy.</span><span class="sxs-lookup"><span data-stu-id="c47c9-116">We recommend that you create a new tenant for the purpose of the trial.</span></span>


### <a name="dynamics-365-project-operations-ce---preview-trial"></a><span data-ttu-id="c47c9-117">Dynamics 365 Project Operations (CE) — wersja próbna w wersji zapoznawczej</span><span class="sxs-lookup"><span data-stu-id="c47c9-117">Dynamics 365 Project Operations (CE) - Preview Trial</span></span> 

<span data-ttu-id="c47c9-118">Przed rozpoczęciem pracy należy się upewnić, że użytkownik jest zalogowany w przeglądarce i ma konto pracy użytkownika w dzierżawie, w której ma zostać wyświetlona wersja zapoznawcza Project Operations.</span><span class="sxs-lookup"><span data-stu-id="c47c9-118">Before you begin, make sure you are logged in to a browser with the user work account in the tenant where you want the Project Operations preview.</span></span>

1. <span data-ttu-id="c47c9-119">Zrealizuj tutaj kod pierwszej oferty, czyli aplikacji **Dynamics 365 Project Operations** [Wersja próbna aplikacji Project Operations](https://aka.ms/try-po).</span><span class="sxs-lookup"><span data-stu-id="c47c9-119">Redeem the first offer code, **Dynamics 365 Project Operations** here [Project Operations Trial](https://aka.ms/try-po).</span></span>
2. <span data-ttu-id="c47c9-120">Potwierdź zamówienie.</span><span class="sxs-lookup"><span data-stu-id="c47c9-120">Confirm your order.</span></span>

  <span data-ttu-id="c47c9-121">Zobaczysz, że oferta potwierdzenia została zrealizowana pomyślnie.</span><span class="sxs-lookup"><span data-stu-id="c47c9-121">You will see confirmation offer was successfully redeemed.</span></span>

### <a name="dynamics-365-finance-preview-trial"></a><span data-ttu-id="c47c9-122">Dynamics 365 Finance — próbna wersja zapoznawcza</span><span class="sxs-lookup"><span data-stu-id="c47c9-122">Dynamics 365 Finance preview trial</span></span>

<span data-ttu-id="c47c9-123">Przejdź do [wersji próbnej aplikacji Dynamics 365 for Finance w wersji zapoznawczej](https://aka.ms/trypoche) i powtórz kroki z poprzedniej sekcji wraz z ofertą. Zarejestruj się w środowisku hostowanym w chmurze.</span><span class="sxs-lookup"><span data-stu-id="c47c9-123">Go to [Dynamics 365 for Finance Preview Trial](https://aka.ms/trypoche) and repeat the steps from the previous section with the offer, Sign up for the Cloud Hosted Environment.</span></span>  

## <a name="assign-licenses"></a><span data-ttu-id="c47c9-124">Przypisywanie licencji</span><span class="sxs-lookup"><span data-stu-id="c47c9-124">Assign licenses</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c47c9-125">Aby wykonać poniższe kroki, potrzebny jest dostęp administracyjny do portalu Microsoft 365 swojej organizacji.</span><span class="sxs-lookup"><span data-stu-id="c47c9-125">You will need administrative access to your organization's Microsoft 365 Portal to complete the following steps.</span></span>

1. <span data-ttu-id="c47c9-126">Przejdź do [Centrum administracyjnego Microsoft 365](https://portal.office.com/), aby przypisać licencje do użytkowników.</span><span class="sxs-lookup"><span data-stu-id="c47c9-126">Go to [Microsoft 365 admin center](https://portal.office.com/) to assign the licenses to your users.</span></span>

2. <span data-ttu-id="c47c9-127">Na stronie **Aktywni użytkownicy** wybierz użytkownika, któremu chcesz przypisać licencję.</span><span class="sxs-lookup"><span data-stu-id="c47c9-127">On the **Active users** page, select the users that you want to assign a license to.</span></span>

3. <span data-ttu-id="c47c9-128">Sprawdź, czy wybrano licencję aplikacji **Dynamics 365 Project Operations**, i wybierz opcję **Zapisz zmiany**.</span><span class="sxs-lookup"><span data-stu-id="c47c9-128">Verify that the **Dynamics 365 Project Operations** license has been selected and select **Save changes**.</span></span>

> [!NOTE]
> <span data-ttu-id="c47c9-129">Oferta wersji próbnej Finance nie musi być przypisana do użytkownika.</span><span class="sxs-lookup"><span data-stu-id="c47c9-129">The Finance trial offer does not need to be assigned to a user.</span></span>

## <a name="start-a-new-project-in-lcs"></a><span data-ttu-id="c47c9-130">Rozpoczęcie nowego projektu w LCS</span><span class="sxs-lookup"><span data-stu-id="c47c9-130">Start a new project in LCS</span></span>

<span data-ttu-id="c47c9-131">Utwórz nowy projekt LCS, tak jak to opisano w temacie [Rozpoczynanie nowego projektu w LCS](create-lcs-project.md)</span><span class="sxs-lookup"><span data-stu-id="c47c9-131">Create a new LCS project as described in the topic, [Start a new project in LCS](create-lcs-project.md)</span></span>

## <a name="add-an-azure-subscription-to-an-lcs-project"></a><span data-ttu-id="c47c9-132">Dodaj subskrypcję Azure do projektu LCS</span><span class="sxs-lookup"><span data-stu-id="c47c9-132">Add an Azure subscription to an LCS project</span></span>

<span data-ttu-id="c47c9-133">Aby wykonać to zadanie, należy wykonać kroki opisane w temacie [Dodawanie subskrypcji Azure do projektu LCS](resource-add-azure-subscription-lcs-project.md).</span><span class="sxs-lookup"><span data-stu-id="c47c9-133">To complete this task, follow the steps in the topic, [Add an Azure subscription to LCS project](resource-add-azure-subscription-lcs-project.md).</span></span>

## <a name="deploy-finance-demo-environment-with-project-operations-for-resourcenon-stocked-scenarios"></a><span data-ttu-id="c47c9-134">Wdrażanie środowiska demonstracyjnego Finance z Project Operations dla scenariuszy zasobów / zasobów niemagazynowanych</span><span class="sxs-lookup"><span data-stu-id="c47c9-134">Deploy Finance demo environment with Project Operations for resource/non-stocked scenarios</span></span>

<span data-ttu-id="c47c9-135">Postępuj zgodnie z instrukcjami w temacie [Ustanowienie nowego środowiska](resource-provision-new-environment.md), aby zakończyć wdrażanie.</span><span class="sxs-lookup"><span data-stu-id="c47c9-135">Follow the guidance in the topic, [Provision a new environment](resource-provision-new-environment.md) to complete the deployment.</span></span> <span data-ttu-id="c47c9-136">Skorzystaj z typu wdrożenia: [wersja demonstracyjna](/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) w celu zapoznania się z funkcjami.</span><span class="sxs-lookup"><span data-stu-id="c47c9-136">Use the [demo environment](/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) deployment type for preview.</span></span> 

## <a name="install-cds-setup-and-configuration-data"></a><span data-ttu-id="c47c9-137">Zainstaluj konfigurację CDS i dane konfiguracyjne</span><span class="sxs-lookup"><span data-stu-id="c47c9-137">Install CDS setup and configuration data</span></span>

<span data-ttu-id="c47c9-138">Zainstaluj konfigurację CDS i dane konfiguracyjne, tak jak to opisano w temacie [Konfiguracja i stosowanie danych konfiguracyjnych w usłudze Common Data Service](resource-apply-pro-setup-config-data.md).</span><span class="sxs-lookup"><span data-stu-id="c47c9-138">Install CDS setup and configuration data as described in the topic, [Set up and apply configuration data in the Common Data Service](resource-apply-pro-setup-config-data.md).</span></span>
<span data-ttu-id="c47c9-139">Wykonaj ten krok dopiero po wdrożeniu środowiska pokazowego aplikacji Finance i przygotowaniu danych do pokazu.</span><span class="sxs-lookup"><span data-stu-id="c47c9-139">Complete this step only after Finance demo environment is deployed and demo data is ready.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
