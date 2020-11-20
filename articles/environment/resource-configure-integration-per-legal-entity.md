---
title: Konfigurowanie integracji aplikacji Project Operations według firm
description: W tym temacie zamieszczono informacje dotyczące ustawienia integracji danych dotyczących podmiotu prawnego w Project Operations.
author: sigitac
manager: Annbe
ms.date: 10/21/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 5d2bb415362a088e01253fbe54f9f06569b4a921
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/28/2020
ms.locfileid: "4122896"
---
# <a name="configure-project-operations-integration-per-legal-entity"></a><span data-ttu-id="d7405-103">Konfigurowanie integracji aplikacji Project Operations według firm</span><span class="sxs-lookup"><span data-stu-id="d7405-103">Configure Project Operations integration per legal entity</span></span> 

<span data-ttu-id="d7405-104">_**Zastosowane do:** Project Operations dla zasobów/scenariuszy nieopartych na zaopatrzeniu_</span><span class="sxs-lookup"><span data-stu-id="d7405-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="d7405-105">Ten temat zapozna użytkownika z krokami wymaganymi do skonfigurowania Dynamics 365 Project Operations dla każdego podmiotu prawnego.</span><span class="sxs-lookup"><span data-stu-id="d7405-105">This topic walks you through the steps required to configure Dynamics 365 Project Operations per legal entity.</span></span>

## <a name="enable-feature-keys-in-dynamics-365-finance"></a><span data-ttu-id="d7405-106">Uruchamianie klawiszy funkcji w Dynamics 365 Finance</span><span class="sxs-lookup"><span data-stu-id="d7405-106">Enable feature keys in Dynamics 365 Finance</span></span>

<span data-ttu-id="d7405-107">Wykonaj poniższe kroki w celu włączenia wymaganych funkcji.</span><span class="sxs-lookup"><span data-stu-id="d7405-107">Complete the following steps to enable required features.</span></span>

1. <span data-ttu-id="d7405-108">W Dynamics 365 Finance przejdź do obszaru roboczego **Zarządzanie danymi**.</span><span class="sxs-lookup"><span data-stu-id="d7405-108">In Dynamics 365 Finance, go to the **Feature Management** workspace.</span></span>
2. <span data-ttu-id="d7405-109">Na liście **Funkcji** znajdź i włącz następujące funkcje:</span><span class="sxs-lookup"><span data-stu-id="d7405-109">In **Feature list**, find and enable the following features:</span></span>
  
    - <span data-ttu-id="d7405-110">**Włączanie wielu pozycji kontraktu dla projektu**</span><span class="sxs-lookup"><span data-stu-id="d7405-110">**Enable multiple contract lines for a project**</span></span>
    - <span data-ttu-id="d7405-111">**Włączanie Project Operations w Dynamics 365 Customer Engagement**</span><span class="sxs-lookup"><span data-stu-id="d7405-111">**Enable Project Operations on Dynamics 365 Customer Engagement**</span></span>

> [!NOTE]
> <span data-ttu-id="d7405-112">Jeśli nie są widoczne **Klawisze funkcji**, należy sprawdzić, czy wersja Finance spełnia minimalne wymagania dotyczące wersji (wersja aplikacji 10.0.13 wraz ze wszystkimi zastosowanymi aktualizacjami lub wyższa).</span><span class="sxs-lookup"><span data-stu-id="d7405-112">If you don't see **Feature keys** listed, verify that your Finance version meets the minimum version requirement (application version 10.0.13 with all quality updates applied or higher).</span></span> <span data-ttu-id="d7405-113">Wybierz opcję **Wyszukaj aktualizacje** aby odświeżyć listę funkcji.</span><span class="sxs-lookup"><span data-stu-id="d7405-113">Select **Check for updates** to refresh the feature list.</span></span>

## <a name="define-the-project-operations-deployment-scenario-for-a-legal-entity"></a><span data-ttu-id="d7405-114">Definiowanie scenariusza wdrażania Project Operations dla podmiotu prawnego</span><span class="sxs-lookup"><span data-stu-id="d7405-114">Define the Project Operations deployment scenario for a legal entity</span></span>

<span data-ttu-id="d7405-115">Project Operations można włączyć na poziomie podmiotu prawnego w Dynamics 365 Customer Engagement.</span><span class="sxs-lookup"><span data-stu-id="d7405-115">You can enable Project Operations on Dynamics 365 Customer Engagement on a legal entity level.</span></span> <span data-ttu-id="d7405-116">Użytkownik może dysponować jedną firmą korzystającą z Project Operations w Dynamics 365 Customer Engagement na potrzeby scenariuszy dla zasobów/scenariuszy nieopartych na zaopatrzeniu.</span><span class="sxs-lookup"><span data-stu-id="d7405-116">You can have one legal entity using Project Operations on Dynamics 365 Customer Engagement for resource/non-stocked based scenarios.</span></span> <span data-ttu-id="d7405-117">W tym samym środowisku inna firma może korzystać z Project Operations na potrzeby scenariuszy opartych na zaopatrzeniu / scenariuszy zamówień produkcyjnych.</span><span class="sxs-lookup"><span data-stu-id="d7405-117">In the same environment, you can have another legal entity using Project Operations for stocked/production order scenarios.</span></span>

1. <span data-ttu-id="d7405-118">W Dynamics 365 Finance przejdź do **Zarządzanie projektami i księgowanie** > **Ustawienia** > **Parametry zarządzania projektami i księgowania**.</span><span class="sxs-lookup"><span data-stu-id="d7405-118">In Dynamics 365 Finance, go to **Project management and accounting** > **Setup** > **Global project management and accounting parameters**.</span></span>
2. <span data-ttu-id="d7405-119">Z poziomu listy dostępnych podmiotów prawnych wybierz podmioty, w których będzie włączone wiele pozycji kontraktu i funkcje Project Operations w Dynamics 365 Customer Engagement.</span><span class="sxs-lookup"><span data-stu-id="d7405-119">In the list of available legal entities, select entities where multiple contract lines and Project Operations on Dynamics 365 Customer Engagement features will be enabled.</span></span> <span data-ttu-id="d7405-120">Pozostaw osoby prawne, które będą używać Project Operations dla scenariuszy magazynowych/zleceń produkcyjnych, jako niezaznaczone.</span><span class="sxs-lookup"><span data-stu-id="d7405-120">Leave legal entities that will be using Project Operations for stocked/production order scenarios unselected.</span></span>

> [!NOTE]
> <span data-ttu-id="d7405-121">Podmiot prawny można wybrać tylko wtedy, gdy nie ma dla niego żadnych istniejących projektów.</span><span class="sxs-lookup"><span data-stu-id="d7405-121">A legal entity can be selected only if it doesn't have any existing projects.</span></span>

## <a name="configure-project-management-and-accounting-parameters"></a><span data-ttu-id="d7405-122">Konfiguracja zarządzania projektem i parametrów księgowania</span><span class="sxs-lookup"><span data-stu-id="d7405-122">Configure Project management and accounting parameters</span></span>

<span data-ttu-id="d7405-123">Każdy podmiot prawny korzystający z Project Operations w Dynamics 365 Customer Engagement musi mieć zestaw parametrów domyślnych.</span><span class="sxs-lookup"><span data-stu-id="d7405-123">Each legal entity using Project Operations on Dynamics 365 Customer Engagement needs a set of default parameters.</span></span> <span data-ttu-id="d7405-124">Te parametry są konfigurowane na karcie **Project Operations** na stronie **Zarządzanie projektami i parametry księgowania**.</span><span class="sxs-lookup"><span data-stu-id="d7405-124">These parameters are configured on the **Project Operations** tab on the **Project management and accounting parameters** page.</span></span> <span data-ttu-id="d7405-125">Te parametry to:</span><span class="sxs-lookup"><span data-stu-id="d7405-125">The parameters are:</span></span>

  - <span data-ttu-id="d7405-126">**Domyślne ustawienia typu fakturowania**: Project Operations korzysta ze stałego zestawu wartości domyślnych typu fakturowania, które muszą być mapowane na właściwości wierszy Finance.</span><span class="sxs-lookup"><span data-stu-id="d7405-126">**Billing type defaults**: Project Operations uses a fixed set of billing type defaults that must be mapped to line properties Finance.</span></span> <span data-ttu-id="d7405-127">Utwórz rekord dla każdego typu fakturowania: **nieokreślony**, **odpłatny**, **nieodpłatny**, **bezpłatny** i **niedostępny**.</span><span class="sxs-lookup"><span data-stu-id="d7405-127">Create a record for each billing type: **Not specified**, **Chargeable**, **Non-chargeable**, **Complimentary**, and **Not available**.</span></span>
  - <span data-ttu-id="d7405-128">**Wartości domyślne kategorii projektów**: należy wybrać domyślne kategorie projektów, które mają być używane dla poszczególnych typów transakcji.</span><span class="sxs-lookup"><span data-stu-id="d7405-128">**Project category defaults**: Select the default project categories to be used for each transaction type.</span></span> <span data-ttu-id="d7405-129">Te wartości domyślne będą używane w **Arkuszu integracji Project Operations** i w oszacowaniach, w których kategoria transakcji nie jest określona dla wartości rzeczywistej projektu.</span><span class="sxs-lookup"><span data-stu-id="d7405-129">These defaults will be used in the **Project Operations Integration journal** and in estimates where no transaction category is specified for the project actual.</span></span>
  - <span data-ttu-id="d7405-130">**Prognozy**: należy wybrać model prognozy, który ma być używana na potrzeby oszacowań czasu i wydatków.</span><span class="sxs-lookup"><span data-stu-id="d7405-130">**Forecasts**: Select the forecast model to be used for time and expense estimates.</span></span>
