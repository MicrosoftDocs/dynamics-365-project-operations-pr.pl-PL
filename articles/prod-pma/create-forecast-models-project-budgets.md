---
title: Tworzenie modeli prognoz dla budżetów projektów
description: W tym temacie opisano sposób tworzenia modelu prognozy dla pozostałego budżetu.
author: Yowelle
ms.date: 04/24/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 3549b41fce72b44230ab27de081dade15a912266
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 05/10/2021
ms.locfileid: "6006305"
---
# <a name="create-forecast-models-for-project-budgets"></a><span data-ttu-id="777b6-103">Tworzenie modeli prognoz dla budżetów projektów</span><span class="sxs-lookup"><span data-stu-id="777b6-103">Create forecast models for project budgets</span></span> 

[!include [banner](../includes/banner.md)]

<span data-ttu-id="777b6-104">W tym temacie opisano sposób tworzenia modelu prognozy dla pozostałego budżetu.</span><span class="sxs-lookup"><span data-stu-id="777b6-104">This topic describes how to create a forecast model for remaining budgets.</span></span> <span data-ttu-id="777b6-105">W projekcie, który jest objęty kontrolą budżetu, są używane dwa typy budżetów: początkowy i pozostały.</span><span class="sxs-lookup"><span data-stu-id="777b6-105">A project that is subject to budget control uses two types of budgets: original and remaining.</span></span> <span data-ttu-id="777b6-106">Podczas tworzenia budżetu projektu należy określić modele prognoz budżetu pierwotnego i pozostałego utworzone na stronie **Modele prognozy**.</span><span class="sxs-lookup"><span data-stu-id="777b6-106">When you create a project budget, you must specify the original and remaining budget forecast models that were created in the **Forecast models** page.</span></span> <span data-ttu-id="777b6-107">Budżety projektu oparte na określonych modelach są tworzone podczas zatwierdzania budżetu projektu.</span><span class="sxs-lookup"><span data-stu-id="777b6-107">Project budgets based on the specified models are created when you commit the project budget.</span></span>

> [!NOTE]
> <span data-ttu-id="777b6-108">Model prognozy używany w przypadku kontroli budżetu nie może mieć pod-modelu ani być używanym w ramach pod-modelu.</span><span class="sxs-lookup"><span data-stu-id="777b6-108">A forecast model that is used for budget control can’t have a submodel or be used as a submodel.</span></span>

1. <span data-ttu-id="777b6-109">Wybierz **Zarządzanie projektem i księgowanie** > **Konfiguracja** > **Prognozy**  > **Modele prognozowania**.</span><span class="sxs-lookup"><span data-stu-id="777b6-109">Select **Project management and accounting** > **Setup** > **Forecasts**  > **Forecast models**.</span></span>
2. <span data-ttu-id="777b6-110">Wybierz opcję **Nowy**, aby utworzyć nowy model prognozy, a następnie wprowadź numer identyfikatora i nazwę nowego modelu.</span><span class="sxs-lookup"><span data-stu-id="777b6-110">Select **New** to create a new forecast model, and then enter a model ID number and name for the new model.</span></span> 
3. <span data-ttu-id="777b6-111">Ustawienie opcji **Zatrzymane** na **Tak** powoduje, że nie są wprowadzane żadne zmiany w wierszach prognozy dla modelu prognozy.</span><span class="sxs-lookup"><span data-stu-id="777b6-111">Set the **Stopped** option to **Yes** to prevent any changes to the forecast lines for the forecast model.</span></span> 
4. <span data-ttu-id="777b6-112">Jeśli wiersze prognozy, z którymi jest skojarzony model, powinny generować prognozy przepływów pieniężnych w księdze głównej, należy ustawić pole **Dodaj do prognoz przepływów pieniężnych** na wartość **Tak**.</span><span class="sxs-lookup"><span data-stu-id="777b6-112">If the forecast lines that the model is associated with should generate cash flow forecasts in the general ledger, set **Include in Cash flow forecasts** to **Yes.**</span></span> 
5. <span data-ttu-id="777b6-113">Aby użyć daty projektu jako daty faktury, ustaw wartość w polu **Prognozowanie daty faktury** na **Tak**.</span><span class="sxs-lookup"><span data-stu-id="777b6-113">To use the project date as the invoice date, set **Forecast Invoice date** to **Yes**.</span></span> 
6. <span data-ttu-id="777b6-114">W polu **Typ budżetu** wybierz jeden z następujących typów modeli:</span><span class="sxs-lookup"><span data-stu-id="777b6-114">In the **Budget type** field, select one of the following model types:</span></span>

   - <span data-ttu-id="777b6-115">**Budżet początkowy**: Użyj kwot z budżetu początkowego podanych podczas tworzenia i zatwierdzania budżetu początkowego.</span><span class="sxs-lookup"><span data-stu-id="777b6-115">**Original budget**: Use the original budget amounts that are committed when the initial budget is created and approved.</span></span>
   - <span data-ttu-id="777b6-116">**Pozostały budżet**: Użyj kwot z pozostałego budżetu w czasie trwania projektu.</span><span class="sxs-lookup"><span data-stu-id="777b6-116">**Remaining budget**: Use the remaining budget amounts during the life of the project.</span></span> <span data-ttu-id="777b6-117">Salda w tym modelu prognozy są redukowane o rzeczywiste transakcje, zwiększane lub zmniejszane na podstawie korekt budżetu.</span><span class="sxs-lookup"><span data-stu-id="777b6-117">The balances in this forecast model are reduced by actual transactions and increased or decreased by budget revisions.</span></span>
   - <span data-ttu-id="777b6-118">**Przeniesienie na następny okres**: Użyj kwot budżetu przeniesienia na następny okres w projekcie.</span><span class="sxs-lookup"><span data-stu-id="777b6-118">**Carry-forward**: Use the carry-forward budget amounts for the project.</span></span> <span data-ttu-id="777b6-119">Przeniesienie na następny okres jest procesem opcjonalnym, który można uruchomić w celu przeniesienia niewykorzystanych kwot budżetu z jednego roku obrachunkowego do innego.</span><span class="sxs-lookup"><span data-stu-id="777b6-119">Carry-forward is an optional process that can be run to transfer unused budget amounts from one fiscal year to another.</span></span>

7. <span data-ttu-id="777b6-120">W razie potrzeby określ następujące opcje:</span><span class="sxs-lookup"><span data-stu-id="777b6-120">Set the following options as required:</span></span>

   - <span data-ttu-id="777b6-121">Aby użyć daty projektu jako daty faktury, włącz **Prognozowanie daty faktury**.</span><span class="sxs-lookup"><span data-stu-id="777b6-121">Enable **Forecast invoice date** to use the project date as the invoice date.</span></span>
   - <span data-ttu-id="777b6-122">Włącz **Prognozę PWT** na podstawie pracy w toku (PWT), a następnie wybierz typ PWT.</span><span class="sxs-lookup"><span data-stu-id="777b6-122">Enable **Forecast with WIP** to forecast based on work in progress (WIP), and then select the type of WIP.</span></span> 
   - <span data-ttu-id="777b6-123">Można zachować domyślny **Typ budżetu** jako **Brak** lub wprowadzić nowy typ.</span><span class="sxs-lookup"><span data-stu-id="777b6-123">You can keep the default **Budget type** as **None** or enter a new type.</span></span> <span data-ttu-id="777b6-124">Nie można zmienić typu budżetu po zmianie rekordu.</span><span class="sxs-lookup"><span data-stu-id="777b6-124">The budget type can't be changed after you change a record.</span></span>     
    > [!NOTE]
    > <span data-ttu-id="777b6-125">Zmiana domyślnego typu budżetu spowoduje, że wszystkie pozostałe opcje staną się niedostępne do aktualizacji i nie będzie można korzystać z tego modelu prognozy.</span><span class="sxs-lookup"><span data-stu-id="777b6-125">If you change the default budget type, all other options will become unavailable for updates, and you can't reuse this forecast model.</span></span> 
   


 



[!INCLUDE[footer-include](../includes/footer-banner.md)]