---
title: Jak dostosować przepływ procesów biznesowych etapów projektu?
description: Omówienie dostosowywania przepływu procesów biznesowych Etapy projektu.
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 10/11/2018
ms.topic: article
author: JohnPBurrows
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
ms.openlocfilehash: 1d0168f187e6b0880713aac04bd87dbc2209197d
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/10/2021
ms.locfileid: "5149016"
---
# <a name="how-do-i-customize-the-project-stages-business-process-flow"></a><span data-ttu-id="dec70-103">Jak dostosować przepływ procesów biznesowych etapów projektu?</span><span class="sxs-lookup"><span data-stu-id="dec70-103">How do I customize the Project Stages business process flow?</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-2-4x-9-0-platform](../includes/cc-applies-to-psa-app-2-4x-9-0-platform.md)]
[!INCLUDE[cc-applies-to-psa-app-1x-8-2-platform](../includes/cc-applies-to-psa-app-1x-8-2-platform.md)]

<span data-ttu-id="dec70-104">Jest znane ograniczenie we wcześniejszych wersjach aplikacji Project Service, przez które nazwy etapów w przepływie procesów biznesowych etapów projektu muszą dokładnie odpowiadać oczekiwanym nazwom w języku angielskim (**Quote**, **Plan**, **Close**).</span><span class="sxs-lookup"><span data-stu-id="dec70-104">There's a known limitation in earlier versions of the Project Service application that the names of the stages in the Project Stages business process flow must exactly match the expected English names (**Quote**, **Plan**, **Close**).</span></span> <span data-ttu-id="dec70-105">W przeciwnym razie logika biznesowa, która bazuje na nazwach etapów w języku angielskim nie będzie działała zgodnie z oczekiwaniami.</span><span class="sxs-lookup"><span data-stu-id="dec70-105">Otherwise, the business logic, which relies on the English stage names, doesn't work as expected.</span></span> <span data-ttu-id="dec70-106">Dlatego nie widzisz znanych akcji, takich jak **Przełącz proces** lub **Edytuj proces** dostępnych w formularzu projektu, i dostosowywanie przepływu procesów biznesowych nie jest zalecane.</span><span class="sxs-lookup"><span data-stu-id="dec70-106">That's why you don't see familiar actions such as **Switch Process** or **Edit Process** available on the project form, and customizing the business process flow isn't encouraged.</span></span> 

<span data-ttu-id="dec70-107">Tym ograniczeniem zajęto się w wersji 2.4.5.48 lub nowszej.</span><span class="sxs-lookup"><span data-stu-id="dec70-107">This limitation has been addressed in version 2.4.5.48 and later.</span></span> <span data-ttu-id="dec70-108">Ten artykuł zawiera sugerowane obejścia tego problemu, jeśli musisz dostosować domyślny przepływ procesów biznesowych dla wcześniejszych wersji.</span><span class="sxs-lookup"><span data-stu-id="dec70-108">This article provides suggested workarounds if you need to customize the default business process flow for earlier versions.</span></span>  

## <a name="business-logic-requires-an-exact-match-with-english-stage-names"></a><span data-ttu-id="dec70-109">Logika biznesowa wymaga dokładnego dopasowania z nazwami etapów w jeżyku angielskim</span><span class="sxs-lookup"><span data-stu-id="dec70-109">Business logic requires an exact match with English stage names</span></span>

<span data-ttu-id="dec70-110">Przepływ procesów biznesowych etapów projektu zawiera logikę biznesową, która kieruje następującymi zachowaniami w aplikacji:</span><span class="sxs-lookup"><span data-stu-id="dec70-110">The Project Stages business process flow includes business logic that drives the following behaviors in the app:</span></span>
- <span data-ttu-id="dec70-111">Gdy projekt jest skojarzony z ofertą, kod ustawia przepływ procesów biznesowych na etap **Quote**.</span><span class="sxs-lookup"><span data-stu-id="dec70-111">When the project is associated with a quote, the code sets the business process flow to the **Quote** stage.</span></span>
- <span data-ttu-id="dec70-112">Gdy projekt jest skojarzony z kontraktem, kod ustawia przepływ procesów biznesowych na etap **Plan**.</span><span class="sxs-lookup"><span data-stu-id="dec70-112">When the project is associated with a contract, the code sets the business process flow to the **Plan** stage.</span></span>
- <span data-ttu-id="dec70-113">Gdy przepływ procesów biznesowych zostanie przeniesiony do etapu **Close**, rekord projektu jest dezaktywowany.</span><span class="sxs-lookup"><span data-stu-id="dec70-113">When the business process flow is advanced to the **Close** stage, the project record is deactivated.</span></span> <span data-ttu-id="dec70-114">Po zdezaktywowaniu projektu, formularz projektu i struktura podziału pracy (SPP) są ustawiane na Tylko do odczytu, wypuszczane są rezerwacje nazwanego zasobu, a wszelkie skojarzone cenniki zostają wyłączone.</span><span class="sxs-lookup"><span data-stu-id="dec70-114">When the project is deactivated, the project form and work breakdown structure (WBS) are set to read-only, the named resource bookings are released, and any associated price lists are deactivated.</span></span>

<span data-ttu-id="dec70-115">Ta logika biznesowe bazuje na nazwach w języku angielskim dla etapów projektu.</span><span class="sxs-lookup"><span data-stu-id="dec70-115">This business logic relies on the English names for the project stages.</span></span> <span data-ttu-id="dec70-116">Ta zależność od nazw etapów wyrażonych w języku angielskim jest główną przyczyną, dlaczego nie jest zalecane dostosowywanie przepływu procesów biznesowych etapów projektu, oraz dlaczego nie widzisz typowych działań przepływu procesów biznesowych, takich jak **Przełącz proces** lub **Edytuj proces** na encji projektu.</span><span class="sxs-lookup"><span data-stu-id="dec70-116">This dependency on the English stage names is the main reason why customization of the Project Stages business process flow isn't encouraged, as well as why you don’t see the common business process flow actions like **Switch Process** or **Edit Process** on the project entity.</span></span>

## <a name="what-happens-if-the-stage-names-dont-match-the-english-names"></a><span data-ttu-id="dec70-117">Co się dzieje, jeśli nazwy etapu nie pasują do nazw w języku angielskim?</span><span class="sxs-lookup"><span data-stu-id="dec70-117">What happens if the stage names don't match the English names?</span></span>

<span data-ttu-id="dec70-118">W aplikacji Project Service 1.x na platformie 8.2 jeśli nazwy etapów przepływu procesu biznesowego nie są zgodne z wyrażonymi w języku angielskim nazw etapów, logika biznesowa, która określa odpowiedni etap dla ofert lub kontraktów, lub która zamyka projekt, jest pomijana.</span><span class="sxs-lookup"><span data-stu-id="dec70-118">In the Project Service app version 1.x on the 8.2 platform, when the stage names in the business process flow don’t match the English stage names exactly, the business logic that sets the right stage for quotes or contracts, or that closes the project, is skipped.</span></span> <span data-ttu-id="dec70-119">Nie są wyświetlane żadne komunikaty o błędach.</span><span class="sxs-lookup"><span data-stu-id="dec70-119">No error messages are displayed.</span></span> <span data-ttu-id="dec70-120">W związku z tym wydaje się, że jesteś w stanie dostosować przepływ procesów biznesowych etapów projektu.</span><span class="sxs-lookup"><span data-stu-id="dec70-120">Therefore it appears that you are able to customize the Project Stages business process flow.</span></span> <span data-ttu-id="dec70-121">Jednak nie będziesz widział żadnych automatycznych procesów pracujących dla ofert, kontraktów, i zamknięcia projektu.</span><span class="sxs-lookup"><span data-stu-id="dec70-121">However, you won’t see any of the automatic processes working for quotes, contracts, and project close.</span></span>

<span data-ttu-id="dec70-122">W aplikacji Project Service 2.4.4.30 lub wcześniej na platformie 9.0 wystąpiła znacząca zmiana architektury przepływu procesów biznesowych, która wymagała ponownego zapisania logiki biznesowej przepływu procesów biznesowych.</span><span class="sxs-lookup"><span data-stu-id="dec70-122">In the Project Service app version 2.4.4.30 or earlier on the 9.0 platform, there was a significant architectural change to business process flows, which required a re-write of the business process flow business logic.</span></span> <span data-ttu-id="dec70-123">W wyniku tego nazwy etapów projektu nie są zgodne z oczekiwanymi nazwami w języku angielski i otrzymujesz komunikat o błędzie.</span><span class="sxs-lookup"><span data-stu-id="dec70-123">As a result, if the process stage names don’t match the expected English names, you do receive an error message.</span></span> 

<span data-ttu-id="dec70-124">W związku z tym, jeśli chcesz dostosować przepływ procesów biznesowych etapów projektu dla encji projekt, możesz dodać tylko zupełnie nowe etapy do domyślnego przepływu procesów biznesowych dla encji projekt, przy zachowaniu **Quote**, **Plan**, i **Close** bez żadnych zmian.</span><span class="sxs-lookup"><span data-stu-id="dec70-124">Therefore, if you want to customize the Project Stages business process flow for the project entity, you can only add brand new stages to the default business process flow for the project entity, while keeping the **Quote**, **Plan**, and **Close** stages as-is.</span></span> <span data-ttu-id="dec70-125">To ograniczenie pozwala zagwarantować, że nie wystąpią błędy z logiki biznesowej, która spodziewa się nazw etapów w języku angielskim w przepływie procesów biznesowych.</span><span class="sxs-lookup"><span data-stu-id="dec70-125">This restriction ensures that you don’t get errors from the business logic that expects the English stage names in the business process flow.</span></span>

<span data-ttu-id="dec70-126">W wersji 2.4.5.48 lub nowszej opisana w tym artykule logika biznesowa została usunięta z domyślnego przepływu procesów biznesowych dla encji projektu.</span><span class="sxs-lookup"><span data-stu-id="dec70-126">In version 2.4.5.48 or later, the business logic described in this article has been removed from the default business process flow for the project entity.</span></span> <span data-ttu-id="dec70-127">Uaktualnianie do tej wersji lub nowszej umożliwi dostosowywanie lub zastępowanie domyślnego przepływu procesów biznesowych jakimś własnym.</span><span class="sxs-lookup"><span data-stu-id="dec70-127">Upgrading to that version or later will let you customize or replace the default business process flow with one of your own.</span></span> 

## <a name="workarounds-for-earlier-versions"></a><span data-ttu-id="dec70-128">Obejścia dla wcześniejszych wersji</span><span class="sxs-lookup"><span data-stu-id="dec70-128">Workarounds for earlier versions</span></span>

<span data-ttu-id="dec70-129">Jeśli uaktualnienie nie jest możliwe, można dostosować przepływu procesów biznesowych etapów projektu dla encji projektu na jeden z tych dwóch sposobów:</span><span class="sxs-lookup"><span data-stu-id="dec70-129">If upgrading isn't an option, you can customize the Project Stages business process flow for the project entity in one of these two ways:</span></span>

1. <span data-ttu-id="dec70-130">Dodaj dodatkowe etapy do konfiguracji domyślnej, zachowując nazwy w języku angielskim dla **Quote**, **Plan**, i **Close**.</span><span class="sxs-lookup"><span data-stu-id="dec70-130">Add additional stages to the default configuration, while retaining the English stage names for **Quote**, **Plan**, and **Close**.</span></span>


![Zrzut ekranu przedstawiający dodawanie etapów do konfiguracji domyślnej](media/FAQ-Customize-BPF-1.png)
 
2. <span data-ttu-id="dec70-132">Utwórz własny przepływ procesów biznesowych i uczyń z niego główny przepływ procesów biznesowych dla encji projektu, co pozwoli na dowolne nazwy etapów.</span><span class="sxs-lookup"><span data-stu-id="dec70-132">Create your own business process flow and make it the primary business process flow for the project entity, which lets you have any stage names you want.</span></span> <span data-ttu-id="dec70-133">Jednak, jeśli chcesz użyć tych samych standardowych etapów projektu **Quote**, **Plan**, i **Close**, musisz wykonać kilka dostosowań, które wywodzą się od niestandardowych nazw etapów.</span><span class="sxs-lookup"><span data-stu-id="dec70-133">However, if you want to use the same standard project stages **Quote**, **Plan**, and **Close**, you need to do some customizations that are driven off your custom stage names.</span></span> <span data-ttu-id="dec70-134">Bardziej skomplikowana logika jest na zamknięciu projektu, co możesz nadal uruchomić po prostu wyłączając rekord projektu.</span><span class="sxs-lookup"><span data-stu-id="dec70-134">The more complex logic is in the closing of the project, which you can still trigger by just deactivating the project record.</span></span>

![Dostosowanie BPF](media/FAQ-Customize-BPF-2.png)

### <a name="additional-considerations-for-project-service-app-version-24430-or-earlier-on-platform-90"></a><span data-ttu-id="dec70-136">Dodatkowe rozważania dotyczące aplikacji Project Service w wersji 2.4.4.30 lub wcześniejszej na platformie 9.0</span><span class="sxs-lookup"><span data-stu-id="dec70-136">Additional considerations for Project Service app version 2.4.4.30 or earlier on platform 9.0</span></span>

<span data-ttu-id="dec70-137">W Project Service 2.4.4.30 lub w wersji wcześniejszej na platformie 9.0, z niestandardowym przepływem procesów biznesowych pole **Nazwa etapu** na encji projektu używana w wykresie **Projekt według etapu** i widoki list projektu nie ulegnie zaktualizowaniu, ponieważ jest połączona z domyślnym przepływem procesów biznesowych etapów projektu.</span><span class="sxs-lookup"><span data-stu-id="dec70-137">In Project Service 2.4.4.30 or earlier on platform 9.0, with a custom business process flow the **Stage Name** field on the project entity used in the **Project By Stage** chart and project list views won’t update, because it’s coupled to the default Project Stages business process flow.</span></span> <span data-ttu-id="dec70-138">Można zająć się tym problemem wykonując następujące kroki:</span><span class="sxs-lookup"><span data-stu-id="dec70-138">You can address this issue with the following steps:</span></span>

- <span data-ttu-id="dec70-139">Dodaj pole niestandardowe, aby uchwycić bieżący etap przepływu procesów biznesowych, który jest aktualizowany gdy użytkownik przechodzi przez przepływ procesów biznesowych.</span><span class="sxs-lookup"><span data-stu-id="dec70-139">Add a custom field to capture the current business process flow stage that is updated as the user advances through the custom business process flow.</span></span>

- <span data-ttu-id="dec70-140">Zmodyfikuj wykres **Projekt według etapu** do pracy z niestandardowym polem zamiast domyślnej konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="dec70-140">Modify the **Project By Stage** chart to work with your custom field instead of the default configuration.</span></span>

### <a name="steps-to-create-your-own-business-process-flow-for-the-project-entity"></a><span data-ttu-id="dec70-141">Kroki w celu utworzenia własnego przepływu procesów biznesowych dla encji projektu</span><span class="sxs-lookup"><span data-stu-id="dec70-141">Steps to create your own business process flow for the project entity</span></span>

<span data-ttu-id="dec70-142">Aby utworzyć własny przepływ procesów biznesowych dla encji projektu przeprowadź następujące kroki:</span><span class="sxs-lookup"><span data-stu-id="dec70-142">To create your own business process flow for the project entity do the following:</span></span>

1. <span data-ttu-id="dec70-143">Przejdź do **Ustawienia** > **Centrum procesu**.</span><span class="sxs-lookup"><span data-stu-id="dec70-143">Go to **Settings** > **Process Center**.</span></span> <span data-ttu-id="dec70-144">Nie kopiuj przepływu procesów biznesowych etapów projektu, ponieważ kopiuje to również logikę biznesową Project Service.</span><span class="sxs-lookup"><span data-stu-id="dec70-144">Don’t copy the Project Stages business process flow because that also copies the Project Service business logic.</span></span>

  ![Utwórz proces](media/FAQ-Customize-BPF-3.png)

2. <span data-ttu-id="dec70-146">Użyj Projektanta procesów, aby utworzyć nazwy etapu, który chcesz utworzyć.</span><span class="sxs-lookup"><span data-stu-id="dec70-146">Use the Process Designer to create the stage names you want.</span></span> <span data-ttu-id="dec70-147">Jeśli chcesz, aby były dostępne takie same funkcje, jak na etapach domyślnych dla **Quote**, **Plan**, i **Close**, będziesz musiał to utworzyć w oparciu o swoje niestandardowe nazw etapów przepływu procesów biznesowych.</span><span class="sxs-lookup"><span data-stu-id="dec70-147">If you want the same functionality as the default stages for **Quote**, **Plan**, and **Close**, you’ll have to create that based on your custom business process flow’s stage names.</span></span>

   ![Zrzut ekranu przedstawiający okno Projektant procesów używane w celu dostosowania przepływu procesów biznesowych](media/FAQ-Customize-BPF-4.png) 

3. <span data-ttu-id="dec70-149">W Projektancie procesów kliknij **Określanie kolejności przepływu procesów**, aby sprawić, że niestandardowy przepływ procesów biznesowych stanie się podstawowym przepływem procesów biznesowych przenosząc go ponad przepływ procesów biznesowych etapy projektu do górnej części listy.</span><span class="sxs-lookup"><span data-stu-id="dec70-149">In the Process Designer, click **Order Process Flow** to make the custom business process flow the primary business process flow for the project entity by moving it above the Project Stages business process flow to the top of the list.</span></span>


   [<span data-ttu-id="dec70-150">Zrzut ekranu przedstawiający korzystanie z Określanie kolejności przepływu procesów</span><span class="sxs-lookup"><span data-stu-id="dec70-150">Screenshot of using Order Process Flow</span></span>](media/FAQ-Customize-BPF-5-720.png)

### <a name="the-following-steps-apply-to-project-service-app-24430-or-earlier-on-the-90-platform"></a><span data-ttu-id="dec70-151">Poniższe kroki odnoszą się do aplikacji Project Service 2.4.4.30 lub wcześniej na platformie 9.0</span><span class="sxs-lookup"><span data-stu-id="dec70-151">The following steps apply to Project Service app 2.4.4.30 or earlier on the 9.0 platform</span></span>

4. <span data-ttu-id="dec70-152">Dodaj nowe pole niestandardowe do encji projektu, aby przechwycić niestandardowe etapy w niestandardowym przepływie procesów biznesowych.</span><span class="sxs-lookup"><span data-stu-id="dec70-152">Add a new custom field to the project entity to capture the custom stages in your custom business process flow.</span></span> <span data-ttu-id="dec70-153">Będziesz musiał dodać logikę biznesową (plug-in/przepływ pracy), aby zaktualizować to pole po zaktualizowaniu etapu w przepływie procesów biznesowych.</span><span class="sxs-lookup"><span data-stu-id="dec70-153">You’ll need to add business logic (plugin/workflow) to update this field when the stage on the custom business process flow is updated.</span></span>

   ![Zrzut ekranu przedstawiający dostosowywanie encji projektu](media/FAQ-Customize-BPF-6-720.png)

5. <span data-ttu-id="dec70-155">Zmodyfikuj wykres **Projekt według etapu**, aby użyć nowego pola niestandardowego dla etapów.</span><span class="sxs-lookup"><span data-stu-id="dec70-155">Modify the **Project By Stage** chart to use your new custom field for stages.</span></span>

   ![Zrzut ekranu przedstawiający użycie wykresu Projekt według etapu](media/FAQ-Customize-BPF-7-720.png)

6. <span data-ttu-id="dec70-157">Zmodyfikuj wszystkie widoki dla encji projekt, aby objąć nowego niestandardowe pole dla etapów.</span><span class="sxs-lookup"><span data-stu-id="dec70-157">Modify any views for the project entity to include your new custom field for stages.</span></span>

   ![Zrzut ekranu przedstawiający modyfikowanie widoków an encji projektu](media/FAQ-Customize-BPF-8-720.png)

