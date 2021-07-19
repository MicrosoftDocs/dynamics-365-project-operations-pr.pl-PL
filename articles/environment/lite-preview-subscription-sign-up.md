---
title: Tworzenie konta dla subskrypcji w wersji zapoznawczej — wersja uproszczona
description: W tym temacie zamieszczono informacje dotyczące sposobu subskrypcji programu Project Operations w wersji okrojonej— od oferty do faktury pro forma.
author: sigitac
ms.date: 07/02/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 2b5a65f5e29915c349d40400ebbf3e4923b36a67
ms.sourcegitcommit: 52b26950bb3b1596ad81aa4ff91745ee9615d1b0
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/02/2021
ms.locfileid: "6334795"
---
# <a name="sign-up-for-a-preview-subscription---lite"></a><span data-ttu-id="aa41b-103">Tworzenie konta dla subskrypcji w wersji zapoznawczej — wersja uproszczona</span><span class="sxs-lookup"><span data-stu-id="aa41b-103">Sign up for a preview subscription - lite</span></span> 

<span data-ttu-id="aa41b-104">Ten temat wyjaśnia, jak subskrybować ofertę wersji próbnej i przeprowadzić uproszczone wdrożenie aplikacji Dynamics 365 Project Operations — od transakcji do faktury proforma.</span><span class="sxs-lookup"><span data-stu-id="aa41b-104">This topic explains how to subscribe to the trial offer and deploy Dynamics 365 Project Operations lite deployment - deal to proforma invoicing.</span></span>

> [!NOTE]
> <span data-ttu-id="aa41b-105">Ten proces będzie się zmieniać w nadchodzących wersjach Project Operations.</span><span class="sxs-lookup"><span data-stu-id="aa41b-105">This process will change in upcoming releases of Project Operations.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="aa41b-106">Wymagania wstępne</span><span class="sxs-lookup"><span data-stu-id="aa41b-106">Prerequisites</span></span>
- <span data-ttu-id="aa41b-107">Użytkownik wdrażający wersję zapoznawczą musi posiadać prawa administratora globalnego dzierżawy Azure.</span><span class="sxs-lookup"><span data-stu-id="aa41b-107">The user who deploys the preview must have Azure tenant global administrator rights.</span></span> <span data-ttu-id="aa41b-108">Dzierżawcę można utworzyć podczas realizowania pierwszej oferty.</span><span class="sxs-lookup"><span data-stu-id="aa41b-108">You can create a tenant during the first offer redemption.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="aa41b-109">To zadanie musi wykonać tylko jedna osoba — administrator dzierżawy w organizacji.</span><span class="sxs-lookup"><span data-stu-id="aa41b-109">Only one person, the tenant administrator, in an organization needs to perform this task.</span></span> <span data-ttu-id="aa41b-110">Jeśli nie jesteś subskrybentem tej wersji, zaczekaj, aż organizacja się zarejestruje i otrzymasz swoje poświadczenia użytkownika.</span><span class="sxs-lookup"><span data-stu-id="aa41b-110">If you aren't the subscriber to this release, wait until your organization has been signed up and you've received your user credentials.</span></span>
> 
> <span data-ttu-id="aa41b-111">Wersje próbne można używać raz w ramach dzierżawcy.</span><span class="sxs-lookup"><span data-stu-id="aa41b-111">Trials are single use in the tenant.</span></span> <span data-ttu-id="aa41b-112">Wersję próbną można uruchomić tylko raz.</span><span class="sxs-lookup"><span data-stu-id="aa41b-112">You can only run a trial one time.</span></span> <span data-ttu-id="aa41b-113">Na potrzeby wersji próbnej zalecamy utworzenie nowego dzierżawcy.</span><span class="sxs-lookup"><span data-stu-id="aa41b-113">We recommend that you create a new tenant for the purpose of the trial.</span></span>

### <a name="dynamics-365-project-operations-trial"></a><span data-ttu-id="aa41b-114">Wersja próbna Dynamics 365 Project Operations</span><span class="sxs-lookup"><span data-stu-id="aa41b-114">Dynamics 365 Project Operations trial</span></span> 

<span data-ttu-id="aa41b-115">Przed rozpoczęciem pracy należy się upewnić, że użytkownik jest zalogowany w przeglądarce i ma konto pracy użytkownika w dzierżawie, w której ma zostać wyświetlona wersja zapoznawcza Project Operations.</span><span class="sxs-lookup"><span data-stu-id="aa41b-115">Before you begin, make sure you are logged in to a browser with the user work account in the tenant where you want the Project Operations preview.</span></span>

1. <span data-ttu-id="aa41b-116">Przejdź do tematu [Wersja próbna aplikacji Project Operations](https://aka.ms/try-po), aby zrealizować kod pierwszej oferty, czyli aplikacji **Dynamics 365 Project Operations**.</span><span class="sxs-lookup"><span data-stu-id="aa41b-116">Go to [Project Operations Trial](https://aka.ms/try-po) to redeem the first offer code, **Dynamics 365 Project Operations**.</span></span>
2. <span data-ttu-id="aa41b-117">Potwierdź zamówienie.</span><span class="sxs-lookup"><span data-stu-id="aa41b-117">Confirm your order.</span></span>

  <span data-ttu-id="aa41b-118">Zobaczysz potwierdzenie z informację, że oferta została pomyślnie zrealizowana.</span><span class="sxs-lookup"><span data-stu-id="aa41b-118">You'll see the confirmation offer was successfully redeemed.</span></span>

## <a name="assign-licenses"></a><span data-ttu-id="aa41b-119">Przypisywanie licencji</span><span class="sxs-lookup"><span data-stu-id="aa41b-119">Assign licenses</span></span>

> [!IMPORTANT]
> <span data-ttu-id="aa41b-120">Aby wykonać poniższe kroki, potrzebny jest dostęp administracyjny do portalu Microsoft 365 swojej organizacji.</span><span class="sxs-lookup"><span data-stu-id="aa41b-120">You will need administrative access to your organization's Microsoft 365 Portal to complete the following steps.</span></span>


1. <span data-ttu-id="aa41b-121">Przejdź do [Centrum administracyjnego Microsoft 365](https://portal.office.com/), aby przypisać licencje do użytkowników.</span><span class="sxs-lookup"><span data-stu-id="aa41b-121">Go to [Microsoft 365 admin center](https://portal.office.com/) to assign the licenses to your users.</span></span>
2. <span data-ttu-id="aa41b-122">Na stronie **Aktywni użytkownicy** wybierz użytkownika, któremu chcesz przypisać licencję.</span><span class="sxs-lookup"><span data-stu-id="aa41b-122">On the **Active users** page, select the users that you want to assign a license to.</span></span>
3. <span data-ttu-id="aa41b-123">Sprawdź, czy licencja **Dynamics 365 Project Operations** została wybrana.</span><span class="sxs-lookup"><span data-stu-id="aa41b-123">Verify that the **Dynamics 365 Project Operations** license is selected.</span></span> 
4. <span data-ttu-id="aa41b-124">Wybierz **Zapisz zmiany**.</span><span class="sxs-lookup"><span data-stu-id="aa41b-124">Select **Save changes**.</span></span>

## <a name="create-a-new-dataverse-environment"></a><span data-ttu-id="aa41b-125">Utwórz nowe środowisko Dataverse</span><span class="sxs-lookup"><span data-stu-id="aa41b-125">Create a new Dataverse environment</span></span>

1. <span data-ttu-id="aa41b-126">Aprowizuj nowe środowisko wdrożenia usługi Project Operations Dataverse dzięki instrukcjom w temacie [Model wdrożenia usługi Dataverse](lite-deployment.md).</span><span class="sxs-lookup"><span data-stu-id="aa41b-126">Provision a new Project Operations Dataverse deployment environment by following instructions in the topic, [Dataverse deployment model](lite-deployment.md).</span></span> <span data-ttu-id="aa41b-127">Podczas wybierania typu środowiska należy pamiętać o użyciu **wersji próbnej (opartej na subskrypcji)**.</span><span class="sxs-lookup"><span data-stu-id="aa41b-127">When you select the environment type, make sure to use **Trial (Subscription based)**.</span></span>

  ![Nowe środowisko](./media/19CreateEnvironment.png)

2. <span data-ttu-id="aa41b-129">Zaznacz ustawienie **Włącz aplikacje Dynamics 365** i pozostaw pole **Automatycznie wdrażaj te aplikacje** pustym.</span><span class="sxs-lookup"><span data-stu-id="aa41b-129">Select the **Enable Dynamics 365 apps** setting, and leave **Automatically deploy these apps** blank.</span></span>  
3. <span data-ttu-id="aa41b-130">Wybierz **Zapisz**, aby utworzyć nowe środowisko.</span><span class="sxs-lookup"><span data-stu-id="aa41b-130">Select **Save** to create the environment.</span></span>

  ![Dodaj bazę danych](./media/20CreateEnvironment1.png)

4. <span data-ttu-id="aa41b-132">Po utworzeniu środowiska zainstaluj rozwiązanie **Microsoft Dynamics 365 Project Operations**.</span><span class="sxs-lookup"><span data-stu-id="aa41b-132">After the environment is created, install **Microsoft Dynamics 365 Project Operations** solution.</span></span> 

![Instalacja rozwiązania](./media/21InstallSolution.png)

## <a name="install-a-cds-configuration-and-setup-demo-data"></a><span data-ttu-id="aa41b-134">Zainstaluj konfigurację CDS i dane wersji demonstracyjnej</span><span class="sxs-lookup"><span data-stu-id="aa41b-134">Install a CDS configuration and setup demo data</span></span>

<span data-ttu-id="aa41b-135">Zainstaluj konfigurację CDS i skonfiguruj dane demonstracyjne, wykonując poniższe instrukcje opisane w temacie [zastosowanie konfiguracji demonstracyjnej i danych konfiguracyjnych](lite-apply-demo-setup-config-data.md).</span><span class="sxs-lookup"><span data-stu-id="aa41b-135">Install the CDS configuration and set up demo data by following instructions in the topic, [Apply demo setup and configuration data](lite-apply-demo-setup-config-data.md).</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
