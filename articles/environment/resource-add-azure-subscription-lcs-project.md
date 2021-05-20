---
title: Dodaj subskrypcję Azure do projektu LCS
description: W tym temat zamieszczono informacje dotyczące sposobu łączenia subskrypcji usługi Azure z projektem LCS.
author: sigitac
manager: Annbe
ms.date: 04/12/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: a80c926ba67a1620e39d8c7677a05678454e6340
ms.sourcegitcommit: 7468d668c48c1d87934aab9a034decd51e56dec6
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/13/2021
ms.locfileid: "5880551"
---
# <a name="add-an-azure-subscription-to-an-lcs-project"></a><span data-ttu-id="f2cc9-103">Dodaj subskrypcję Azure do projektu LCS</span><span class="sxs-lookup"><span data-stu-id="f2cc9-103">Add an Azure subscription to an LCS project</span></span>

<span data-ttu-id="f2cc9-104">_**Zastosowane do:** Project Operations dla zasobów/scenariuszy nieopartych na zaopatrzeniu_</span><span class="sxs-lookup"><span data-stu-id="f2cc9-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="f2cc9-105">Środowiska hostowane w chmurze muszą zostać wdrożone za pomocą istniejącej subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="f2cc9-105">Cloud-hosted environments must be deployed using an existing Azure subscription.</span></span> <span data-ttu-id="f2cc9-106">W tym temacie zamieszczono informacje dotyczące sposobu łączenia istniejącej subskrypcji usługi Azure z projektem LCS.</span><span class="sxs-lookup"><span data-stu-id="f2cc9-106">This topic explains how to connect your existing Azure subscription to an LCS project.</span></span> 

## <a name="grant-admin-consent"></a><span data-ttu-id="f2cc9-107">Wyrażanie zgody administratora</span><span class="sxs-lookup"><span data-stu-id="f2cc9-107">Grant admin consent</span></span>

1. <span data-ttu-id="f2cc9-108">W projekcie LCS, w sekcji **Środowiska** wybierz pozycję **Ustawienia Microsoft Azure**.</span><span class="sxs-lookup"><span data-stu-id="f2cc9-108">In your LCS project, in the **Environments** section, select **Microsoft Azure settings**.</span></span>

![Ustawienia aplikacji Microsoft Azure](./media/1MicrosoftAzureSettings.png)

2. <span data-ttu-id="f2cc9-110">Na stronie **Ustawienia projektu** na karcie **Łączniki Azure** wybierz opcję **Autoryzuj**.</span><span class="sxs-lookup"><span data-stu-id="f2cc9-110">On the **Project settings** page, on the **Azure connectors** tab, select **Authorize**.</span></span> <span data-ttu-id="f2cc9-111">Pozwala to na wdrażanie środowiska w tym projekcie.</span><span class="sxs-lookup"><span data-stu-id="f2cc9-111">This allows environments to be deployed to this project.</span></span>

![Łączniki Azure](./media/2AzureConnectors.png)

3. <span data-ttu-id="f2cc9-113">Wybierz **Autoryzuj**, aby wydać zgodę administratora.</span><span class="sxs-lookup"><span data-stu-id="f2cc9-113">Select **Authorize** again to provide admin consent.</span></span>

![Wyrażanie zgody administratora](./media/3GrantAdminConsent.png)

4. <span data-ttu-id="f2cc9-115">Zaakceptuj prośbę o uprawnienia.</span><span class="sxs-lookup"><span data-stu-id="f2cc9-115">Accept the permissions request.</span></span>

![Zaakceptowanie prośby o uprawnienia](./media/4AcceptPermissionRequest.png)

<span data-ttu-id="f2cc9-117">Autoryzacja jest teraz ukończona.</span><span class="sxs-lookup"><span data-stu-id="f2cc9-117">The authorization is now complete.</span></span> 

![Pomyślna autoryzacja](./media/5AuthorizationComplete.png)

## <a name="provide-dynamics-deployment-services-access-to-your-azure-subscription"></a><a name="provide"></a><span data-ttu-id="f2cc9-119">Umożliw dostęp Dynamics Deployment Services do Twojej subskrypcji Azure</span><span class="sxs-lookup"><span data-stu-id="f2cc9-119">Provide Dynamics Deployment Services access to your Azure subscription</span></span>

1. <span data-ttu-id="f2cc9-120">Przejdź do [Rozliczeń Microsoft Azure](https://portal.azure.com/#blade/Microsoft\_Azure\_Billing/SubscriptionsBlade) i wybierz swoją subskrypcję.</span><span class="sxs-lookup"><span data-stu-id="f2cc9-120">Go to [Microsoft Azure billing](https://portal.azure.com/#blade/Microsoft\_Azure\_Billing/SubscriptionsBlade) and select your subscription.</span></span> <span data-ttu-id="f2cc9-121">Usługi wdrażania Dynamics Deployment Services muszą mieć dostęp do tej subskrypcji w celu umożliwienia wdrażania środowisk.</span><span class="sxs-lookup"><span data-stu-id="f2cc9-121">Dynamics Deployment Services needs to access this subscription to be able to deploy environments.</span></span>

![Szczegóły subskrypcji Azure](./media/6AzureSubscription.png)

2. <span data-ttu-id="f2cc9-123">Wybierz pozycję **Kontrola dostępu (IAM)** w okienku nawigacji, a następnie wybierz pozycję **Dodaj przypisanie roli**.</span><span class="sxs-lookup"><span data-stu-id="f2cc9-123">Select **Access control (IAM)** in the navigation pane, and then select **Add role assignment**.</span></span>
3. <span data-ttu-id="f2cc9-124">Korzystając z suwaka po prawej stronie wybierz opcję **Rola współautora**, a następnie na liście znajdź i wybierz pozycję **Dynamics Deployment Services**.</span><span class="sxs-lookup"><span data-stu-id="f2cc9-124">In the slider on the right side, select **Contributor role**, and in the list provided, find and select **Dynamics Deployment Services**.</span></span> 
4. <span data-ttu-id="f2cc9-125">Wybierz pozycję **Zapisz**.</span><span class="sxs-lookup"><span data-stu-id="f2cc9-125">Select **Save**.</span></span>

![Dostęp do subskrypcji](./media/7SubscriptionAccess.png)

### <a name="add-a-subscription-connector-to-an-lcs-project"></a><span data-ttu-id="f2cc9-127">Dodawanie łącznika subskrypcji Azure do projektu LCS</span><span class="sxs-lookup"><span data-stu-id="f2cc9-127">Add a subscription connector to an LCS project</span></span>

1. <span data-ttu-id="f2cc9-128">W projekcie LCS na stronie **Ustawień Microsoft Azure** wybierz pozycję **Dodaj**, aby dodać nowy łącznik.</span><span class="sxs-lookup"><span data-stu-id="f2cc9-128">In your LCS project, on the **Microsoft Azure settings** page, select **Add** to add a new connector.</span></span>
2. <span data-ttu-id="f2cc9-129">Wprowadź identyfikator subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="f2cc9-129">Enter your Azure subscription ID.</span></span> <span data-ttu-id="f2cc9-130">Identyfikator subskrypcji platformy Azure można znaleźć w [portalu Azure](https://ms.portal.azure.com/), w obszarze **Ustawienia** w lewej dolnej części ekranu.</span><span class="sxs-lookup"><span data-stu-id="f2cc9-130">You can find your Azure subscription ID in the [Azure portal](https://ms.portal.azure.com/), under  **Settings**  in the lower left of the screen.</span></span>
3. <span data-ttu-id="f2cc9-131">W polu **Konfiguruj, aby korzystać z Azure Resource Manager** wybierz opcję **Tak**.</span><span class="sxs-lookup"><span data-stu-id="f2cc9-131">In the **Configure to use Azure Resource Manager** field, select **Yes**.</span></span>
4. <span data-ttu-id="f2cc9-132">Upewnij się, że domena dzierżawy subskrypcji Azure usługi AAD pasuje do używanej przez użytkownika domeny subskrypcji platformy Azure i wybierz opcję **Dalej**.</span><span class="sxs-lookup"><span data-stu-id="f2cc9-132">Make sure Azure's Subscription AAD Tenant Domain matches the domain-owning Azure subscription that you are using, and select **Next**.</span></span>
5. <span data-ttu-id="f2cc9-133">Na ekranie **Konfiguracji Microsoft Azure** wybierz pozycję **Dalej**, aby potwierdzić.</span><span class="sxs-lookup"><span data-stu-id="f2cc9-133">On the **Microsoft Azure Setup** screen, select **Next** to confirm.</span></span> <span data-ttu-id="f2cc9-134">Jeśli na tym ekranie zostanie wyświetlony komunikat o błędzie, powróć do sekcji [Umożliw dostęp Dynamics Deployment Services do Twojej subskrypcji Azure](#provide) w tym temacie i upewnij się, że zostały zakończone wszystkie opisane czynności.</span><span class="sxs-lookup"><span data-stu-id="f2cc9-134">If you receive an error on this screen, return to the section [Provide Dynamics Deployment Services access to Azure subscription](#provide) in this topic and make sure you have completed all of the steps.</span></span>
6. <span data-ttu-id="f2cc9-135">Pobierz Azure Management Certificate do folderu lokalnego na komputerze.</span><span class="sxs-lookup"><span data-stu-id="f2cc9-135">Download the Azure Management Certificate to a local folder on your computer.</span></span> <span data-ttu-id="f2cc9-136">Poproś administratora Azure o przesłanie certyfikatu do Azure Management Portal, wybierając subskrypcję i przechodząc do **Ustawienia** > **Certyfikaty zarządzania**.</span><span class="sxs-lookup"><span data-stu-id="f2cc9-136">Ask your Azure subscription administrator to upload the certificate to Azure Management Portal by selecting the subscription and going to **Settings** > **Management Certificates**.</span></span> <span data-ttu-id="f2cc9-137">Ten certyfikat umożliwia usługom LCS komunikację z platformą Azure w imieniu użytkownika.</span><span class="sxs-lookup"><span data-stu-id="f2cc9-137">This certificate enables LCS to communicate with Azure on your behalf.</span></span> <span data-ttu-id="f2cc9-138">Jeśli użytkownik ma dostęp do subskrypcji, można pominąć ten krok.</span><span class="sxs-lookup"><span data-stu-id="f2cc9-138">You can skip this step if your user has access to the subscription.</span></span>
7. <span data-ttu-id="f2cc9-139">Wybierz **Dalej**.</span><span class="sxs-lookup"><span data-stu-id="f2cc9-139">Select  **Next**.</span></span>
8. <span data-ttu-id="f2cc9-140">Wybierz obszar Azure, którego wdrożenie ma zostać wdrożone, i wybierz centrum danych, które znajduje się w pobliżu miejsca, w którym zamierzasz używać tego systemu.</span><span class="sxs-lookup"><span data-stu-id="f2cc9-140">Select the Azure region to deploy in and select a data center that is close to where you plan to use this system.</span></span>
9.  <span data-ttu-id="f2cc9-141">Wybierz pozycję **Połącz**.</span><span class="sxs-lookup"><span data-stu-id="f2cc9-141">Select  **Connect**.</span></span>

<span data-ttu-id="f2cc9-142">Pomyślnie połączono Twoją subskrypcję Azure.</span><span class="sxs-lookup"><span data-stu-id="f2cc9-142">You have successfully connected your Azure subscription.</span></span> <span data-ttu-id="f2cc9-143">Można teraz wdrażać środowiska Dynamics 365 Finance hostowane w chmurze.</span><span class="sxs-lookup"><span data-stu-id="f2cc9-143">You can now deploy Dynamics 365 Finance cloud-hosted environments.</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]
