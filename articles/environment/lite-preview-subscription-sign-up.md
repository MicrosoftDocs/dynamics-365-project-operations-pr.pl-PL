---
title: Tworzenie konta dla subskrypcji w wersji zapoznawczej — wersja uproszczona
description: W tym temacie zamieszczono informacje dotyczące sposobu subskrypcji programu Project Operations w wersji okrojonej— od oferty do faktury pro forma.
author: sigitac
ms.date: 10/07/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 4de51277e5a08690cc16497e3916f40498b39fb8
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 05/10/2021
ms.locfileid: "5997434"
---
# <a name="sign-up-for-a-preview-subscription---lite"></a><span data-ttu-id="591f5-103">Tworzenie konta dla subskrypcji w wersji zapoznawczej — wersja uproszczona</span><span class="sxs-lookup"><span data-stu-id="591f5-103">Sign up for a preview subscription - lite</span></span> 

<span data-ttu-id="591f5-104">W tym temat wyjaśniono, jak subskrybować ofertę partnera w wersji zapoznawczej i wdrożyć w wersji uproszczonej Dynamics 365 Project Operations — od umowy do fakturowania proforma.</span><span class="sxs-lookup"><span data-stu-id="591f5-104">This topic explains how to subscribe to the preview partner offer and deploy Dynamics 365 Project Operations lite deployment - deal to proforma invoicing.</span></span>

> [!NOTE]
> <span data-ttu-id="591f5-105">Ten proces będzie się zmieniać w nadchodzących wersjach Project Operations.</span><span class="sxs-lookup"><span data-stu-id="591f5-105">This process will change in upcoming releases of Project Operations.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="591f5-106">Wymagania wstępne</span><span class="sxs-lookup"><span data-stu-id="591f5-106">Prerequisites</span></span>

- <span data-ttu-id="591f5-107">Otrzymasz wiadomość e-mail z zaproszeniem do skorzystania z wersji zapoznawczej.</span><span class="sxs-lookup"><span data-stu-id="591f5-107">You'll receive an email inviting you to participate in the preview.</span></span> <span data-ttu-id="591f5-108">O dostęp do wersji zapoznawczej można wystąpić na [stronie internetowej Project Operations](https://dynamics.microsoft.com/en-us/project-operations/overview/).</span><span class="sxs-lookup"><span data-stu-id="591f5-108">You can request a preview on the [Project Operations website](https://dynamics.microsoft.com/en-us/project-operations/overview/).</span></span>
- <span data-ttu-id="591f5-109">Użytkownik wdrażający wersję zapoznawczą musi posiadać prawa administratora globalnego dzierżawy Azure.</span><span class="sxs-lookup"><span data-stu-id="591f5-109">The user who deploys the preview must have Azure tenant global administrator rights.</span></span>
- <span data-ttu-id="591f5-110">Przejrzyj cały regulamin.</span><span class="sxs-lookup"><span data-stu-id="591f5-110">Review all terms and conditions.</span></span>

## <a name="subscribe"></a><span data-ttu-id="591f5-111">Subskrybuj</span><span class="sxs-lookup"><span data-stu-id="591f5-111">Subscribe</span></span>

<span data-ttu-id="591f5-112">Po zatwierdzeniu żądania [dostępu do wersji zapoznawczej](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUMkRDV1NYQU5TNjE2VjhKOVBUNVg2R0s1NC4u), otrzymasz 2 wiadomości e-mail z ofertą od firmy Microsoft.</span><span class="sxs-lookup"><span data-stu-id="591f5-112">When you receive a [preview request](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUMkRDV1NYQU5TNjE2VjhKOVBUNVg2R0s1NC4u) approval, you'll receive two offers from Microsoft by email.</span></span> <span data-ttu-id="591f5-113">Te oferty umożliwiają wdrożenie wersji zapoznawczej Project Operations:</span><span class="sxs-lookup"><span data-stu-id="591f5-113">These offers allow you to deploy the Project Operations Preview:</span></span>

- <span data-ttu-id="591f5-114">Dynamics 365 Project Operations (CRM) — próbna wersja zapoznawcza</span><span class="sxs-lookup"><span data-stu-id="591f5-114">Dynamics 365 Project Operations (CRM) - Preview Trial</span></span>
- <span data-ttu-id="591f5-115">Office 365 Project Operations — (wersja zapoznawcza)</span><span class="sxs-lookup"><span data-stu-id="591f5-115">Office 365 Project Operations - Preview Trial</span></span>

> [!IMPORTANT]
> <span data-ttu-id="591f5-116">To zadanie musi wykonać tylko jedna osoba — administrator dzierżawy w organizacji.</span><span class="sxs-lookup"><span data-stu-id="591f5-116">Only one person, the tenant administrator, in an organization needs to perform this task.</span></span> <span data-ttu-id="591f5-117">Jeśli nie jesteś subskrybentem tej wersji, zaczekaj, aż organizacja się zarejestruje i otrzymasz swoje poświadczenia użytkownika.</span><span class="sxs-lookup"><span data-stu-id="591f5-117">If you aren't the subscriber to this release, wait until your organization has been signed up and you've received your user credentials.</span></span>

### <a name="dynamics-365-project-operations-crm---preview-trial"></a><span data-ttu-id="591f5-118">Dynamics 365 Project Operations (CRM) — próbna wersja zapoznawcza</span><span class="sxs-lookup"><span data-stu-id="591f5-118">Dynamics 365 Project Operations (CRM) - Preview Trial</span></span> 

<span data-ttu-id="591f5-119">Przed rozpoczęciem pracy należy się upewnić, że użytkownik jest zalogowany w przeglądarce i ma konto pracy użytkownika w dzierżawie, w której ma zostać wyświetlona wersja zapoznawcza Project Operations.</span><span class="sxs-lookup"><span data-stu-id="591f5-119">Before you begin, make sure you are logged in to a browser with the user work account in the tenant where you want the Project Operations preview.</span></span>

1. <span data-ttu-id="591f5-120">Zrealizuj pierwszy kod oferty, **Dynamics 365 Project Operations (CRM) — próbna wersja zapoznawcza**, wklejając go do adresu URL przeglądarki.</span><span class="sxs-lookup"><span data-stu-id="591f5-120">Redeem the first offer code, **Dynamics 365 Project Operations (CRM) - Preview Trial** by pasting it into the browser URL.</span></span>

![Realizacja oferty](./media/16RedeemFirstOfferNew.png)

2. <span data-ttu-id="591f5-122">Potwierdź zamówienie.</span><span class="sxs-lookup"><span data-stu-id="591f5-122">Confirm your order.</span></span>
<span data-ttu-id="591f5-123">![Potwierdź zamówienie](./media/17ConfirmOrderNew.png)</span><span class="sxs-lookup"><span data-stu-id="591f5-123">![Confirm the order](./media/17ConfirmOrderNew.png)</span></span>

<span data-ttu-id="591f5-124">Zobaczysz, że oferta potwierdzenia została zrealizowana pomyślnie.</span><span class="sxs-lookup"><span data-stu-id="591f5-124">You'll see confirmation offer was successfully redeemed.</span></span>

![Potwierdzenie](./media/18OrderConfirmationNew.png)

### <a name="office-365-project-operations---preview-trial"></a><span data-ttu-id="591f5-126">Office 365 Project Operations — (wersja zapoznawcza)</span><span class="sxs-lookup"><span data-stu-id="591f5-126">Office 365 Project Operations - Preview Trial</span></span>

<span data-ttu-id="591f5-127">Powtórz te kroki, tak jak w przypadku pierwszego kodu oferty.</span><span class="sxs-lookup"><span data-stu-id="591f5-127">Repeat the same steps as with the first offer code.</span></span> <span data-ttu-id="591f5-128">Należy pamiętać, aby dodać drugi kod oferty, korzystając z tego samego konta użytkownika, które zostało użyte za pierwszym razem.</span><span class="sxs-lookup"><span data-stu-id="591f5-128">Make sure to add the second offer code using the same user account that was used with the first offer code.</span></span>

## <a name="assign-licenses"></a><span data-ttu-id="591f5-129">Przypisywanie licencji</span><span class="sxs-lookup"><span data-stu-id="591f5-129">Assign licenses</span></span>

> [!IMPORTANT]
> <span data-ttu-id="591f5-130">Aby wykonać poniższe kroki, potrzebny jest dostęp administracyjny do portalu Microsoft 365 swojej organizacji.</span><span class="sxs-lookup"><span data-stu-id="591f5-130">You will need administrative access to your organization's Microsoft 365 Portal to complete the following steps.</span></span>


1. <span data-ttu-id="591f5-131">Przejdź do [Centrum administracyjnego Microsoft 365](https://portal.office.com/), aby przypisać licencje do użytkowników.</span><span class="sxs-lookup"><span data-stu-id="591f5-131">Go to [Microsoft 365 admin center](https://portal.office.com/) to assign the licenses to your users.</span></span>

![Strona Centrum administracyjnego](./media/14AdminPortal.png)

2. <span data-ttu-id="591f5-133">Na stronie **Aktywni użytkownicy** wybierz użytkownika, któremu chcesz przypisać licencję.</span><span class="sxs-lookup"><span data-stu-id="591f5-133">On the **Active users** page, select the users that you want to assign a license to.</span></span>

![Przypisywanie licencji](./media/15AssignLicenses.png)

3. <span data-ttu-id="591f5-135">Sprawdź, czy zaznaczone są licencje **Dynamics 365 Project Operations (CRM) w wersji zapoznawczej** i **Project Operations Office 365 — wersja zapoznawcza**.</span><span class="sxs-lookup"><span data-stu-id="591f5-135">Verify that the **Dynamics 365 Project Operations (CRM) Preview** and **Office 365 Project Operations - Preview** licenses are selected.</span></span> 
4. <span data-ttu-id="591f5-136">Wybierz **Zapisz zmiany**.</span><span class="sxs-lookup"><span data-stu-id="591f5-136">Select **Save changes**.</span></span>

## <a name="create-a-new-cds-environment"></a><span data-ttu-id="591f5-137">Utwórz nowe środowisko CDS</span><span class="sxs-lookup"><span data-stu-id="591f5-137">Create a new CDS environment</span></span>

1. <span data-ttu-id="591f5-138">Ustanów nowe środowisko Project Operations CDS dzięki instrukcjom w temacie [model wdrożenia CDS](lite-deployment.md).</span><span class="sxs-lookup"><span data-stu-id="591f5-138">Provision a new Project Operations CDS deployment environment by following instructions in the topic, [CDS deployment model](lite-deployment.md).</span></span> <span data-ttu-id="591f5-139">Podczas wybierania typu środowiska należy pamiętać o użyciu **wersji próbnej (opartej na subskrypcji)**.</span><span class="sxs-lookup"><span data-stu-id="591f5-139">When you select the environment type, make sure to use **Trial (Subscription based)**.</span></span>
<span data-ttu-id="591f5-140">![Nowe środowisko](./media/19CreateEnvironment.png)</span><span class="sxs-lookup"><span data-stu-id="591f5-140">![New environment](./media/19CreateEnvironment.png)</span></span>

2. <span data-ttu-id="591f5-141">Zaznacz ustawienie **Włącz aplikacje Dynamics 365** i pozostaw pole **Automatycznie wdrażaj te aplikacje** pustym.</span><span class="sxs-lookup"><span data-stu-id="591f5-141">Select the **Enable Dynamics 365 apps** setting, and leave **Automatically deploy these apps** blank.</span></span>  
3. <span data-ttu-id="591f5-142">Wybierz **Zapisz**, aby utworzyć nowe środowisko.</span><span class="sxs-lookup"><span data-stu-id="591f5-142">Select **Save** to create the environment.</span></span>

![Dodaj bazę danych](./media/20CreateEnvironment1.png)

4. <span data-ttu-id="591f5-144">Po utworzeniu środowiska zainstaluj rozwiązanie **Microsoft Dynamics 365 Project Operations**.</span><span class="sxs-lookup"><span data-stu-id="591f5-144">After the environment is created, install **Microsoft Dynamics 365 Project Operations** solution.</span></span> 

![Instalacja rozwiązania](./media/21InstallSolution.png)

## <a name="install-a-cds-configuration-and-setup-demo-data"></a><span data-ttu-id="591f5-146">Zainstaluj konfigurację CDS i dane wersji demonstracyjnej</span><span class="sxs-lookup"><span data-stu-id="591f5-146">Install a CDS configuration and setup demo data</span></span>

<span data-ttu-id="591f5-147">Zainstaluj konfigurację CDS i skonfiguruj dane demonstracyjne, wykonując poniższe instrukcje opisane w temacie [zastosowanie konfiguracji demonstracyjnej i danych konfiguracyjnych](lite-apply-demo-setup-config-data.md).</span><span class="sxs-lookup"><span data-stu-id="591f5-147">Install the CDS configuration and set up demo data by following instructions in the topic, [Apply demo setup and configuration data](lite-apply-demo-setup-config-data.md).</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]