---
title: Rejestracja w przeglądzie subskrypcji Project Operations w ramach scenariuszy zasobów / zasobów niemagazynowanych
description: W tym temacie zamieszczono informacje dotyczące sposobu subskrypcji i wdrożenia Project Operations do obsługi zasobów i zasobów niemagazynowanych.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 4d35a8bf9e8a841b45808b26ae2587c5b7d99d72
ms.sourcegitcommit: b9d8bf00239815f31686e9b28998ac684fd2fca4
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/02/2020
ms.locfileid: "3949012"
---
# <a name="sign-up-for-project-operations-preview-subscriptions-for-resource-non-stocked-scenarios"></a><span data-ttu-id="9312b-103">Rejestracja w przeglądzie subskrypcji Project Operations w ramach scenariuszy zasobów / zasobów niemagazynowanych</span><span class="sxs-lookup"><span data-stu-id="9312b-103">Sign up for Project Operations preview subscriptions for resource/ non-stocked scenarios</span></span>

<span data-ttu-id="9312b-104">_**Zastosowane do:** Project Operations dla zasobów/scenariuszy nieopartych na zaopatrzeniu_</span><span class="sxs-lookup"><span data-stu-id="9312b-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="9312b-105">W tym temacie przedstawiono sposób subskrybowania wersji zapoznawczej / partnerskiej i wdrożenie Project Operations na potrzeby scenariuszy zasobów i zasobów niemagazynowanych.</span><span class="sxs-lookup"><span data-stu-id="9312b-105">This topic explains how to subscribe to the preview/partner offer and deploy Project Operations environment for resource/ non-stocked based scenarios.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="9312b-106">Wymagania wstępne</span><span class="sxs-lookup"><span data-stu-id="9312b-106">Prerequisites</span></span>

- <span data-ttu-id="9312b-107">Otrzymasz wiadomość e-mail z zaproszeniem do skorzystania z wersji zapoznawczej.</span><span class="sxs-lookup"><span data-stu-id="9312b-107">You will receive an email inviting you to participate in the preview.</span></span> <span data-ttu-id="9312b-108">O dostęp do wersji zapoznawczej można wystąpić na [stronie internetowej Project Operations](https://dynamics.microsoft.com/en-us/project-operations/overview/).</span><span class="sxs-lookup"><span data-stu-id="9312b-108">You can request a preview on the [Project Operations website](https://dynamics.microsoft.com/en-us/project-operations/overview/).</span></span>
- <span data-ttu-id="9312b-109">Użytkownik wdrażający wersję zapoznawczą musi posiadać prawa administratora globalnego dzierżawy Azure.</span><span class="sxs-lookup"><span data-stu-id="9312b-109">The user who deploys the preview must have Azure tenant global administrator rights.</span></span>
- <span data-ttu-id="9312b-110">Wdrożenie środowiska Finance wymaga poprawnej subskrypcji Azure, która będzie rozliczana w ramach poszczególnego środowiska.</span><span class="sxs-lookup"><span data-stu-id="9312b-110">Deploying a Finance environment requires a valid Azure subscription that will be billed per environment.</span></span> <span data-ttu-id="9312b-111">Aby rozpocząć, należy użyć istniejącej subskrypcji lub [wersji próbnej usługi Azure](https://azure.microsoft.com/en-us/free/).</span><span class="sxs-lookup"><span data-stu-id="9312b-111">You can use your organizations existing subscription or use an [Azure trial](https://azure.microsoft.com/en-us/free/) to get started.</span></span> <span data-ttu-id="9312b-112">Środowisko CDS jest dostępne bezpłatnie przez okres 30 dni.</span><span class="sxs-lookup"><span data-stu-id="9312b-112">The CDS environment will be provided free for a limited 30 day period.</span></span>

## <a name="subscribe"></a><span data-ttu-id="9312b-113">Subskrybuj</span><span class="sxs-lookup"><span data-stu-id="9312b-113">Subscribe</span></span>

<span data-ttu-id="9312b-114">Po zatwierdzeniu [żądania wersji zapoznawczej](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUMkRDV1NYQU5TNjE2VjhKOVBUNVg2R0s1NC4u), otrzymasz 2 wiadomości e-mail z ofertą od firmy Microsoft.</span><span class="sxs-lookup"><span data-stu-id="9312b-114">When your [preview request](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUMkRDV1NYQU5TNjE2VjhKOVBUNVg2R0s1NC4u) is approved, you will receive two offers from Microsoft by email.</span></span> <span data-ttu-id="9312b-115">Te oferty umożliwiają wdrożenie wersji zapoznawczej Project Operations:</span><span class="sxs-lookup"><span data-stu-id="9312b-115">These offers allow you to deploy the Project Operations Preview:</span></span>

- <span data-ttu-id="9312b-116">Dynamics 365 Project Operations — próbna wersja zapoznawcza</span><span class="sxs-lookup"><span data-stu-id="9312b-116">Dynamics 365 Project Operations – Preview Trial</span></span>
- <span data-ttu-id="9312b-117">Dynamics 365 for Finance and Operations — próbna wersja zapoznawcza.</span><span class="sxs-lookup"><span data-stu-id="9312b-117">Dynamics 365 for Finance and Operations Preview Trial.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="9312b-118">To zadanie musi wykonać tylko jedna osoba — administrator dzierżawy w organizacji.</span><span class="sxs-lookup"><span data-stu-id="9312b-118">Only one person, the tenant administrator, in an organization needs to perform this task.</span></span> <span data-ttu-id="9312b-119">Jeśli nie jesteś subskrybentem tej wersji, zaczekaj, aż organizacja się zarejestruje i otrzymasz swoje poświadczenia użytkownika.</span><span class="sxs-lookup"><span data-stu-id="9312b-119">If you aren't the subscriber to this release, wait until your organization has been signed up and you've received your user credentials.</span></span>

### <a name="dynamics-365-project-operations--preview-trial"></a><span data-ttu-id="9312b-120">Dynamics 365 Project Operations — próbna wersja zapoznawcza</span><span class="sxs-lookup"><span data-stu-id="9312b-120">Dynamics 365 Project Operations – Preview trial</span></span>

1. <span data-ttu-id="9312b-121">Zrealizuj pierwszą ofertę o nazwie **Dynamics 365 Project Operations — wersja próbna**, używając adresu URL podanego w powitalnej wiadomości e-mail.</span><span class="sxs-lookup"><span data-stu-id="9312b-121">Redeem the first offer, **Dynamics 365 Project Operations Trial**, with the URL provided in your welcome email.</span></span>

![Pierwsza oferta](./media/1FirstOffer.png)

2. <span data-ttu-id="9312b-123">Sprawdź, czy nastąpiło zalogowanie jako użytkownika należącego do organizacji, która będzie subskrybowała tę usługę.</span><span class="sxs-lookup"><span data-stu-id="9312b-123">Verify that you are logged in as the user who belongs to the organization who will be subscribing to the service.</span></span>
3. <span data-ttu-id="9312b-124">Kontynuuj realizowanie oferty.</span><span class="sxs-lookup"><span data-stu-id="9312b-124">Proceed with redeeming the offer.</span></span> 
4. <span data-ttu-id="9312b-125">Wybierz opcję **Tak, dodajesz do mojego konta**.</span><span class="sxs-lookup"><span data-stu-id="9312b-125">Select **Yes, add it to my account**.</span></span>

![Realizacja oferty](./media/2RedeemFirstOffer.png)

![Potwierdzenie oferty](./media/3ConfirmFirstOffer.png)

![Oferta zrealizowana](./media/4OfferSuccessfulyRedeemed.png)

### <a name="dynamics-365-finance-preview-trial"></a><span data-ttu-id="9312b-129">Dynamics 365 Finance — próbna wersja zapoznawcza</span><span class="sxs-lookup"><span data-stu-id="9312b-129">Dynamics 365 Finance preview trial</span></span>

<span data-ttu-id="9312b-130">Powtórz te same kroki dla drugiej oferty z powitalnej wiadomości e-mail.</span><span class="sxs-lookup"><span data-stu-id="9312b-130">Repeat the same steps with the second offer from the Welcome email.</span></span>

## <a name="assign-licenses"></a><span data-ttu-id="9312b-131">Przypisywanie licencji</span><span class="sxs-lookup"><span data-stu-id="9312b-131">Assign Licenses</span></span>

> [!IMPORTANT]
> <span data-ttu-id="9312b-132">Aby wykonać poniższe kroki, potrzebny jest dostęp administracyjny do portalu Office 365 swojej organizacji.</span><span class="sxs-lookup"><span data-stu-id="9312b-132">You will need administrative access to your organization's Office 365 Portal to complete the following steps.</span></span>

1. <span data-ttu-id="9312b-133">Przejdź do [Centrum administracyjnego Microsoft 365](https://portal.office.com/), aby przypisać licencje do użytkowników.</span><span class="sxs-lookup"><span data-stu-id="9312b-133">Go to [Microsoft 365 admin center](https://portal.office.com/) to assign licenses to your users.</span></span>

![Portal administracyjny usługi Office](./media/5OfficeAdminPortal.png)

2. <span data-ttu-id="9312b-135">Na stronie **Aktywni użytkownicy** wybierz użytkownika, któremu chcesz przypisać licencję.</span><span class="sxs-lookup"><span data-stu-id="9312b-135">On the **Active users** page, select the users that you want to assign a license to.</span></span>

![Przypisywanie licencji](./media/6AssignLicenses.png)

3. <span data-ttu-id="9312b-137">Sprawdź, czy wybrano licencję na Project Operations i wybierz pozycję **Zapisz zmiany**.</span><span class="sxs-lookup"><span data-stu-id="9312b-137">Verify that the Project Operations license has been selected and select **Save changes**.</span></span> 

> [!NOTE]
> <span data-ttu-id="9312b-138">Oferta wersji próbnej Finance nie musi być przypisana do użytkownika.</span><span class="sxs-lookup"><span data-stu-id="9312b-138">The Finance trial offer does not need to be assigned to a user.</span></span>

## <a name="start-a-new-project-in-lcs"></a><span data-ttu-id="9312b-139">Rozpoczęcie nowego projektu w LCS</span><span class="sxs-lookup"><span data-stu-id="9312b-139">Start a new project in LCS</span></span>

<span data-ttu-id="9312b-140">Utwórz nowy projekt LCS, tak jak to opisano w temacie [Rozpoczynanie nowego projektu w LCS](create-lcs-project.md)</span><span class="sxs-lookup"><span data-stu-id="9312b-140">Create a new LCS project as described in the topic, [Start a new project in LCS](create-lcs-project.md)</span></span>

## <a name="add-an-azure-subscription-to-an-lcs-project"></a><span data-ttu-id="9312b-141">Dodaj subskrypcję Azure do projektu LCS</span><span class="sxs-lookup"><span data-stu-id="9312b-141">Add an Azure subscription to an LCS project</span></span>

<span data-ttu-id="9312b-142">Aby wykonać to zadanie, należy wykonać kroki opisane w temacie [Dodawanie subskrypcji Azure do projektu LCS](resource-add-azure-subscription-lcs-project.md).</span><span class="sxs-lookup"><span data-stu-id="9312b-142">To complete this task, follow the steps in the topic, [Add an Azure subscription to LCS project](resource-add-azure-subscription-lcs-project.md).</span></span>

## <a name="deploy-finance-demo-environment-with-project-operations-for-resourcenon-stocked-scenarios"></a><span data-ttu-id="9312b-143">Wdrażanie środowiska demonstracyjnego Finance z Project Operations dla scenariuszy zasobów / zasobów niemagazynowanych</span><span class="sxs-lookup"><span data-stu-id="9312b-143">Deploy Finance demo environment with Project Operations for resource/non-stocked scenarios</span></span>

<span data-ttu-id="9312b-144">Postępuj zgodnie z instrukcjami w temacie [Ustanowienie nowego środowiska](resource-provision-new-environment.md), aby zakończyć wdrażanie.</span><span class="sxs-lookup"><span data-stu-id="9312b-144">Follow the guidance in the topic, [Provision a new environment](resource-provision-new-environment.md) to complete the deployment.</span></span> <span data-ttu-id="9312b-145">Skorzystaj z typu wdrożenia: [wersja demonstracyjna](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) w celu zapoznania się z funkcjami.</span><span class="sxs-lookup"><span data-stu-id="9312b-145">Use the [demo environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) deployment type for preview.</span></span>

## <a name="install-cds-setup-and-configuration-data"></a><span data-ttu-id="9312b-146">Zainstaluj konfigurację CDS i dane konfiguracyjne</span><span class="sxs-lookup"><span data-stu-id="9312b-146">Install CDS setup and configuration data</span></span>

<span data-ttu-id="9312b-147">Zainstaluj konfigurację CDS i dane konfiguracyjne, tak jak to opisano w temacie [Konfiguracja i stosowanie danych konfiguracyjnych w usłudze Common Data Service](resource-apply-pro-setup-config-data.md).</span><span class="sxs-lookup"><span data-stu-id="9312b-147">Install CDS setup and configuration data as described in the topic, [Set up and apply configuration data in the Common Data Service](resource-apply-pro-setup-config-data.md).</span></span>

