---
title: Rejestracja w przeglądzie subskrypcji Project Operations w ramach scenariuszy zasobów / zasobów niemagazynowanych
description: W tym temacie zamieszczono informacje dotyczące sposobu subskrypcji i wdrożenia Project Operations do obsługi zasobów i zasobów niemagazynowanych.
author: sigitac
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 4c2cd4c5d4dfbb95398932d432864cf0d4d5d54d
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5276856"
---
# <a name="sign-up-for-project-operations-preview-subscriptions-for-resource-non-stocked-scenarios"></a><span data-ttu-id="3cb84-103">Rejestracja w przeglądzie subskrypcji Project Operations w ramach scenariuszy zasobów / zasobów niemagazynowanych</span><span class="sxs-lookup"><span data-stu-id="3cb84-103">Sign up for Project Operations preview subscriptions for resource/ non-stocked scenarios</span></span>

<span data-ttu-id="3cb84-104">_**Zastosowane do:** Project Operations dla zasobów/scenariuszy nieopartych na zaopatrzeniu_</span><span class="sxs-lookup"><span data-stu-id="3cb84-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="3cb84-105">W tym temacie przedstawiono sposób subskrybowania wersji zapoznawczej / partnerskiej i wdrożenie Project Operations na potrzeby scenariuszy zasobów i zasobów niemagazynowanych.</span><span class="sxs-lookup"><span data-stu-id="3cb84-105">This topic explains how to subscribe to the preview/partner offer and deploy Project Operations environment for resource/ non-stocked based scenarios.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="3cb84-106">Wymagania wstępne</span><span class="sxs-lookup"><span data-stu-id="3cb84-106">Prerequisites</span></span>

- <span data-ttu-id="3cb84-107">Otrzymasz wiadomość e-mail z zaproszeniem do skorzystania z wersji zapoznawczej.</span><span class="sxs-lookup"><span data-stu-id="3cb84-107">You will receive an email inviting you to participate in the preview.</span></span> <span data-ttu-id="3cb84-108">O dostęp do wersji zapoznawczej można wystąpić na [stronie internetowej Project Operations](https://dynamics.microsoft.com/en-us/project-operations/overview/).</span><span class="sxs-lookup"><span data-stu-id="3cb84-108">You can request a preview on the [Project Operations website](https://dynamics.microsoft.com/en-us/project-operations/overview/).</span></span>
- <span data-ttu-id="3cb84-109">Użytkownik wdrażający wersję zapoznawczą musi posiadać prawa administratora globalnego dzierżawy Azure.</span><span class="sxs-lookup"><span data-stu-id="3cb84-109">The user who deploys the preview must have Azure tenant global administrator rights.</span></span>
- <span data-ttu-id="3cb84-110">Wdrożenie środowiska Finance wymaga poprawnej subskrypcji Azure, która będzie rozliczana w ramach poszczególnego środowiska.</span><span class="sxs-lookup"><span data-stu-id="3cb84-110">Deploying a Finance environment requires a valid Azure subscription that will be billed per environment.</span></span> <span data-ttu-id="3cb84-111">Aby rozpocząć, należy użyć istniejącej subskrypcji lub [wersji próbnej usługi Azure](https://azure.microsoft.com/en-us/free/).</span><span class="sxs-lookup"><span data-stu-id="3cb84-111">You can use your organizations existing subscription or use an [Azure trial](https://azure.microsoft.com/en-us/free/) to get started.</span></span> <span data-ttu-id="3cb84-112">Środowisko CDS jest dostępne bezpłatnie przez okres 30 dni.</span><span class="sxs-lookup"><span data-stu-id="3cb84-112">The CDS environment will be provided free for a limited 30 day period.</span></span>

## <a name="subscribe"></a><span data-ttu-id="3cb84-113">Subskrybuj</span><span class="sxs-lookup"><span data-stu-id="3cb84-113">Subscribe</span></span>

<span data-ttu-id="3cb84-114">Po zatwierdzeniu [żądania wersji zapoznawczej](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUMkRDV1NYQU5TNjE2VjhKOVBUNVg2R0s1NC4u), otrzymasz 3 wiadomości e-mail z ofertą od firmy Microsoft.</span><span class="sxs-lookup"><span data-stu-id="3cb84-114">When your [preview request](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUMkRDV1NYQU5TNjE2VjhKOVBUNVg2R0s1NC4u) is approved, you will receive three offers from Microsoft by email.</span></span> <span data-ttu-id="3cb84-115">Te oferty umożliwiają wdrożenie wersji zapoznawczej Project Operations:</span><span class="sxs-lookup"><span data-stu-id="3cb84-115">These offers allow you to deploy the Project Operations Preview:</span></span>

- <span data-ttu-id="3cb84-116">Dynamics 365 Project Operations (CRM) — próbna wersja zapoznawcza</span><span class="sxs-lookup"><span data-stu-id="3cb84-116">Dynamics 365 Project Operations (CRM) - Preview Trial</span></span>
- <span data-ttu-id="3cb84-117">Office 365 Project Operations — (wersja zapoznawcza)</span><span class="sxs-lookup"><span data-stu-id="3cb84-117">Office 365 Project Operations - Preview Trial</span></span>
- <span data-ttu-id="3cb84-118">Dynamics 365 Finance — próbna wersja zapoznawcza</span><span class="sxs-lookup"><span data-stu-id="3cb84-118">Dynamics 365 Finance - Preview Trial</span></span>

> [!IMPORTANT]
> <span data-ttu-id="3cb84-119">To zadanie musi wykonać tylko jedna osoba — administrator dzierżawy w organizacji.</span><span class="sxs-lookup"><span data-stu-id="3cb84-119">Only one person, the tenant administrator, in an organization needs to perform this task.</span></span> <span data-ttu-id="3cb84-120">Jeśli nie jesteś subskrybentem tej wersji, zaczekaj, aż organizacja się zarejestruje i otrzymasz swoje poświadczenia użytkownika.</span><span class="sxs-lookup"><span data-stu-id="3cb84-120">If you aren't the subscriber to this release, wait until your organization has been signed up and you've received your user credentials.</span></span>

### <a name="dynamics-365-project-operations-crm---preview-trial"></a><span data-ttu-id="3cb84-121">Dynamics 365 Project Operations (CRM) — próbna wersja zapoznawcza</span><span class="sxs-lookup"><span data-stu-id="3cb84-121">Dynamics 365 Project Operations (CRM) - Preview Trial</span></span> 

<span data-ttu-id="3cb84-122">Przed rozpoczęciem pracy należy się upewnić, że użytkownik jest zalogowany w przeglądarce i ma konto pracy użytkownika w dzierżawie, w której ma zostać wyświetlona wersja zapoznawcza Project Operations.</span><span class="sxs-lookup"><span data-stu-id="3cb84-122">Before you begin, make sure you are logged in to a browser with the user work account in the tenant where you want the Project Operations preview.</span></span>

1. <span data-ttu-id="3cb84-123">Zrealizuj pierwszy kod oferty, **Dynamics 365 Project Operations (CRM) — próbna wersja zapoznawcza**, wklejając go do adresu URL przeglądarki.</span><span class="sxs-lookup"><span data-stu-id="3cb84-123">Redeem the first offer code, **Dynamics 365 Project Operations (CRM) - Preview Trial** by pasting it into the browser URL.</span></span>

![Realizacja oferty](./media/16RedeemFirstOfferNew.png)

2. <span data-ttu-id="3cb84-125">Potwierdź zamówienie.</span><span class="sxs-lookup"><span data-stu-id="3cb84-125">Confirm your order.</span></span>

![Potwierdź zamówienie](./media/17ConfirmOrderNew.png)

<span data-ttu-id="3cb84-127">Zobaczysz, że oferta potwierdzenia została zrealizowana pomyślnie.</span><span class="sxs-lookup"><span data-stu-id="3cb84-127">You will see confirmation offer was successfully redeemed.</span></span>

![Potwierdzenie](./media/18OrderConfirmationNew.png)

### <a name="office-365-project-operations---preview-trial"></a><span data-ttu-id="3cb84-129">Office 365 Project Operations — (wersja zapoznawcza)</span><span class="sxs-lookup"><span data-stu-id="3cb84-129">Office 365 Project Operations - Preview Trial</span></span>

<span data-ttu-id="3cb84-130">Powtórz te kroki, tak jak w przypadku pierwszego kodu oferty.</span><span class="sxs-lookup"><span data-stu-id="3cb84-130">Repeat the same steps as with the first offer code.</span></span> <span data-ttu-id="3cb84-131">Należy pamiętać, aby dodać drugi kod oferty, korzystając z tego samego konta użytkownika, które zostało użyte za pierwszym razem.</span><span class="sxs-lookup"><span data-stu-id="3cb84-131">Make sure to add the second offer code using the same user account that was used with the first offer code.</span></span>

### <a name="dynamics-365-finance-preview-trial"></a><span data-ttu-id="3cb84-132">Dynamics 365 Finance — próbna wersja zapoznawcza</span><span class="sxs-lookup"><span data-stu-id="3cb84-132">Dynamics 365 Finance preview trial</span></span>

<span data-ttu-id="3cb84-133">Powtórz te same kroki dla ostatniej oferty z powitalnej wiadomości e-mail.</span><span class="sxs-lookup"><span data-stu-id="3cb84-133">Repeat the same steps with the last offer from the Welcome email.</span></span>

## <a name="assign-licenses"></a><span data-ttu-id="3cb84-134">Przypisywanie licencji</span><span class="sxs-lookup"><span data-stu-id="3cb84-134">Assign licenses</span></span>

> [!IMPORTANT]
> <span data-ttu-id="3cb84-135">Aby wykonać poniższe kroki, potrzebny jest dostęp administracyjny do portalu Microsoft 365 swojej organizacji.</span><span class="sxs-lookup"><span data-stu-id="3cb84-135">You will need administrative access to your organization's Microsoft 365 Portal to complete the following steps.</span></span>

1. <span data-ttu-id="3cb84-136">Przejdź do [Centrum administracyjnego Microsoft 365](https://portal.office.com/), aby przypisać licencje do użytkowników.</span><span class="sxs-lookup"><span data-stu-id="3cb84-136">Go to [Microsoft 365 admin center](https://portal.office.com/) to assign the licenses to your users.</span></span>

![Strona Centrum administracyjnego](./media/14AdminPortal.png)

2. <span data-ttu-id="3cb84-138">Na stronie **Aktywni użytkownicy** wybierz użytkownika, któremu chcesz przypisać licencję.</span><span class="sxs-lookup"><span data-stu-id="3cb84-138">On the **Active users** page, select the users that you want to assign a license to.</span></span>

![Przypisywanie licencji](./media/15AssignLicenses.png)

3. <span data-ttu-id="3cb84-140">Sprawdź, czy wybrano licencję rozwiązań **Dynamics 365 Project Operations (CRM) — wersja zapoznawcza** i **Office 365 Project Operations — wersja zapoznawcza**, i wybierz pozycję **Zapisz zmiany**.</span><span class="sxs-lookup"><span data-stu-id="3cb84-140">Verify that the **Dynamics 365 Project Operations (CRM) Preview** and **Office 365 Project Operations - Preview** license have been selected and select **Save changes**.</span></span>

> [!NOTE]
> <span data-ttu-id="3cb84-141">Oferta wersji próbnej Finance nie musi być przypisana do użytkownika.</span><span class="sxs-lookup"><span data-stu-id="3cb84-141">The Finance trial offer does not need to be assigned to a user.</span></span>

## <a name="start-a-new-project-in-lcs"></a><span data-ttu-id="3cb84-142">Rozpoczęcie nowego projektu w LCS</span><span class="sxs-lookup"><span data-stu-id="3cb84-142">Start a new project in LCS</span></span>

<span data-ttu-id="3cb84-143">Utwórz nowy projekt LCS, tak jak to opisano w temacie [Rozpoczynanie nowego projektu w LCS](create-lcs-project.md)</span><span class="sxs-lookup"><span data-stu-id="3cb84-143">Create a new LCS project as described in the topic, [Start a new project in LCS](create-lcs-project.md)</span></span>

## <a name="add-an-azure-subscription-to-an-lcs-project"></a><span data-ttu-id="3cb84-144">Dodaj subskrypcję Azure do projektu LCS</span><span class="sxs-lookup"><span data-stu-id="3cb84-144">Add an Azure subscription to an LCS project</span></span>

<span data-ttu-id="3cb84-145">Aby wykonać to zadanie, należy wykonać kroki opisane w temacie [Dodawanie subskrypcji Azure do projektu LCS](resource-add-azure-subscription-lcs-project.md).</span><span class="sxs-lookup"><span data-stu-id="3cb84-145">To complete this task, follow the steps in the topic, [Add an Azure subscription to LCS project](resource-add-azure-subscription-lcs-project.md).</span></span>

## <a name="deploy-finance-demo-environment-with-project-operations-for-resourcenon-stocked-scenarios"></a><span data-ttu-id="3cb84-146">Wdrażanie środowiska demonstracyjnego Finance z Project Operations dla scenariuszy zasobów / zasobów niemagazynowanych</span><span class="sxs-lookup"><span data-stu-id="3cb84-146">Deploy Finance demo environment with Project Operations for resource/non-stocked scenarios</span></span>

<span data-ttu-id="3cb84-147">Postępuj zgodnie z instrukcjami w temacie [Ustanowienie nowego środowiska](resource-provision-new-environment.md), aby zakończyć wdrażanie.</span><span class="sxs-lookup"><span data-stu-id="3cb84-147">Follow the guidance in the topic, [Provision a new environment](resource-provision-new-environment.md) to complete the deployment.</span></span> <span data-ttu-id="3cb84-148">Skorzystaj z typu wdrożenia: [wersja demonstracyjna](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) w celu zapoznania się z funkcjami.</span><span class="sxs-lookup"><span data-stu-id="3cb84-148">Use the [demo environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) deployment type for preview.</span></span> 

## <a name="install-cds-setup-and-configuration-data"></a><span data-ttu-id="3cb84-149">Zainstaluj konfigurację CDS i dane konfiguracyjne</span><span class="sxs-lookup"><span data-stu-id="3cb84-149">Install CDS setup and configuration data</span></span>

<span data-ttu-id="3cb84-150">Zainstaluj konfigurację CDS i dane konfiguracyjne, tak jak to opisano w temacie [Konfiguracja i stosowanie danych konfiguracyjnych w usłudze Common Data Service](resource-apply-pro-setup-config-data.md).</span><span class="sxs-lookup"><span data-stu-id="3cb84-150">Install CDS setup and configuration data as described in the topic, [Set up and apply configuration data in the Common Data Service](resource-apply-pro-setup-config-data.md).</span></span>
<span data-ttu-id="3cb84-151">Tę czynność należy wykonać tylko po wdrożeniu środowiska pokazowego Finance i przygotowaniu danych demonstracyjnych w FO.</span><span class="sxs-lookup"><span data-stu-id="3cb84-151">Complete this step only after Finance demo environment is deployed and demo data in FO is ready.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]