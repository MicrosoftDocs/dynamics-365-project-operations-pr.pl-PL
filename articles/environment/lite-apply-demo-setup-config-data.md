---
title: Zastosowanie konfiguracji demonstracyjnej i danych konfiguracyjnych — wersja uproszczona
description: W tym temacie zamieszczono informacje dotyczące sposobu stosowania konfiguracji demonstracyjnej i danych konfiguracyjnych Project Operations.
author: sigitac
manager: Annbe
ms.date: 01/27/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 762b0cf317d442565a033f56033a53a5b5cc435c
ms.sourcegitcommit: b4298ca4729643c1040ef35dde8c67f829461ce7
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2021
ms.locfileid: "5089132"
---
# <a name="apply-demo-setup-and-configuration-data-for-project-operations---lite"></a><span data-ttu-id="d59f0-103">Zastosowanie konfiguracji demonstracyjnej i danych konfiguracyjnych dla Project Operations — wersja uproszczona</span><span class="sxs-lookup"><span data-stu-id="d59f0-103">Apply demo setup and configuration data for Project Operations - lite</span></span> 

<span data-ttu-id="d59f0-104">_\*\*Wdrażanie uproszczone — od oferty do faktury pro forma_</span><span class="sxs-lookup"><span data-stu-id="d59f0-104">_\*\*Lite deployment - deal to proforma invoicing_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

## <a name="prerequisites"></a><span data-ttu-id="d59f0-105">Wymagania wstępne</span><span class="sxs-lookup"><span data-stu-id="d59f0-105">Prerequisites</span></span>

<span data-ttu-id="d59f0-106">Przed rozpoczęciem konfiguracji należy dysponować środowiskiem usługi Common Data Service (CDS) ustanowionym dla aplikacji Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="d59f0-106">Before you begin the configuration, you must have a Common Data Service (CDS) environment provisioned for Dynamics 365 Project Operations.</span></span>


## <a name="instructions"></a><span data-ttu-id="d59f0-107">Instrukcje</span><span class="sxs-lookup"><span data-stu-id="d59f0-107">Instructions</span></span>

1. <span data-ttu-id="d59f0-108">Pobierz [pakiet Master Data Package](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData%20-%20CE%20only%20CMT.zip).</span><span class="sxs-lookup"><span data-stu-id="d59f0-108">Download the [Master Data Package](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData%20-%20CE%20only%20CMT.zip).</span></span> 
2. <span data-ttu-id="d59f0-109">Przejdź do folderu *ProjOpsDemoDataSetupAndMaster - Integrated CMT*, a następnie uruchom plik wykonywalny *DataMigrationUtility*.</span><span class="sxs-lookup"><span data-stu-id="d59f0-109">Navigate to the folder *ProjOpsDemoDataSetupAndMaster - Integrated CMT* and run the executable file, *DataMigrationUtility*.</span></span>
3. <span data-ttu-id="d59f0-110">Na stronie 1 Kreatora migracji konfiguracji Common Data Service (CMT) wybierz pozycję **Importuj dane**, a następnie wybierz pozycję **Kontynuuj**.</span><span class="sxs-lookup"><span data-stu-id="d59f0-110">On page 1 of the Common Data Service Configuration Migration (CMT) Wizard, select **Import Data** and then select **Continue**.</span></span>

    ![Migracja konfiguracji](./media/1ConfigurationMigration.png)

4. <span data-ttu-id="d59f0-112">Na stronie 2 kreatora CMT wybierz **Microsoft 365** jako **Typ wdrożenia**.</span><span class="sxs-lookup"><span data-stu-id="d59f0-112">On Page 2 of the CMT Wizard, select **Microsoft 365** as the **Deployment Type**.</span></span>
5. <span data-ttu-id="d59f0-113">Wybierz pola wyboru **Wyświetl listę dostępnych organizacji** i **Wyświetl zaawansowane**.</span><span class="sxs-lookup"><span data-stu-id="d59f0-113">Select the **Display a list of available organizations** and **Show Advanced** check boxes.</span></span>
6. <span data-ttu-id="d59f0-114">Wybierz region dzierżawy, wprowadź swoje poświadczenia, a następnie wybierz pozycję **Zaloguj**.</span><span class="sxs-lookup"><span data-stu-id="d59f0-114">Select the region of your tenant, enter your credentials, and then select **Login**.</span></span>

   ![Konfiguracja logowania](./media/2ConfigurationSignin.png)

7. <span data-ttu-id="d59f0-116">Na stronie 3 z poziomu listy organizacji w dzierżawie wybierz nazwę organizacji, do której chcesz zaimportować dane demonstracyjne, a następnie wybierz pozycję **Zaloguj**.</span><span class="sxs-lookup"><span data-stu-id="d59f0-116">On page 3, from the list of Organizations on the Tenant, select which organization you want to import the demo data into and then select **Login**.</span></span>
8. <span data-ttu-id="d59f0-117">Na stronie 4 wybierz plik zip *MasterAndSetupData*, który znajduje się w rozpakowanym folderze *ProjOpsDemoDataSetupAndMaster - Integrated CMT*.</span><span class="sxs-lookup"><span data-stu-id="d59f0-117">On page 4, select the zip file, *MasterAndSetupData* from the unpacked folder, *ProjOpsDemoDataSetupAndMaster - Integrated CMT*.</span></span>

   ![Plik ZIP](./media/3ZipFile.png)

   ![Wybierz plik](./media/4SelectAFile.png)

9. <span data-ttu-id="d59f0-120">Po zaznaczeniu pliku zip wybierz pozycję **Importuj dane**.</span><span class="sxs-lookup"><span data-stu-id="d59f0-120">After the zip file is selected, select **Import Data**.</span></span>

   ![Importuj dane](./media/5ImportData.png)

10. <span data-ttu-id="d59f0-122">Importowanie potrwa około dwóch sekund, w zależności od szybkości sieci.</span><span class="sxs-lookup"><span data-stu-id="d59f0-122">Import will run for approximately two-ten minutes depending on your network speed.</span></span> <span data-ttu-id="d59f0-123">Po zakończeniu pracy zakończ działanie kreatora CMT.</span><span class="sxs-lookup"><span data-stu-id="d59f0-123">After it completes, exit the CMT Wizard.</span></span> 
11. <span data-ttu-id="d59f0-124">Należy sprawdzić w ramach organizacji dane z następujących 20 encji:</span><span class="sxs-lookup"><span data-stu-id="d59f0-124">Check your organization for data in the following 20 entities:</span></span>

    -   <span data-ttu-id="d59f0-125">Waluta</span><span class="sxs-lookup"><span data-stu-id="d59f0-125">Currency</span></span>
    -   <span data-ttu-id="d59f0-126">Konto</span><span class="sxs-lookup"><span data-stu-id="d59f0-126">Account</span></span>
    -   <span data-ttu-id="d59f0-127">Jednostka organizacyjna</span><span class="sxs-lookup"><span data-stu-id="d59f0-127">Organizational Unit</span></span>
    -   <span data-ttu-id="d59f0-128">Kontakt</span><span class="sxs-lookup"><span data-stu-id="d59f0-128">Contact</span></span>
    -   <span data-ttu-id="d59f0-129">Jednostka</span><span class="sxs-lookup"><span data-stu-id="d59f0-129">Unit</span></span>
    -   <span data-ttu-id="d59f0-130">Grupa jednostek</span><span class="sxs-lookup"><span data-stu-id="d59f0-130">Unit Group</span></span>
    -   <span data-ttu-id="d59f0-131">Cennik</span><span class="sxs-lookup"><span data-stu-id="d59f0-131">Price List</span></span>
    -   <span data-ttu-id="d59f0-132">Cennik parametrów projektu</span><span class="sxs-lookup"><span data-stu-id="d59f0-132">Project Parameter Price List</span></span> 
    -   <span data-ttu-id="d59f0-133">Częstotliwość faktur</span><span class="sxs-lookup"><span data-stu-id="d59f0-133">Invoice Frequency</span></span>
    -   <span data-ttu-id="d59f0-134">Kategoria zasobów, które można zarezerwować</span><span class="sxs-lookup"><span data-stu-id="d59f0-134">Bookable Resource Category</span></span>
    -   <span data-ttu-id="d59f0-135">Kategoria transakcji</span><span class="sxs-lookup"><span data-stu-id="d59f0-135">Transaction Category</span></span>
    -   <span data-ttu-id="d59f0-136">Kategoria wydatków</span><span class="sxs-lookup"><span data-stu-id="d59f0-136">Expense Category</span></span>
    -   <span data-ttu-id="d59f0-137">Cena roli</span><span class="sxs-lookup"><span data-stu-id="d59f0-137">Role Price</span></span>
    -   <span data-ttu-id="d59f0-138">Cena kategorii transakcji</span><span class="sxs-lookup"><span data-stu-id="d59f0-138">Transaction Category Price</span></span>
    -   <span data-ttu-id="d59f0-139">Charakterystyka</span><span class="sxs-lookup"><span data-stu-id="d59f0-139">Characteristic</span></span>
    -   <span data-ttu-id="d59f0-140">Zasób, który można zarezerwować</span><span class="sxs-lookup"><span data-stu-id="d59f0-140">Bookable Resource</span></span>
    -   <span data-ttu-id="d59f0-141">Skojarzenie kategorii zasobów, które można zarezerwować</span><span class="sxs-lookup"><span data-stu-id="d59f0-141">Bookable resource category Assn</span></span>
    -   <span data-ttu-id="d59f0-142">Charakterystyka zasobu, który można zarezerwować</span><span class="sxs-lookup"><span data-stu-id="d59f0-142">Bookable Resource Characteristic</span></span>

    ![Zakończ importowanie](./media/6CompleteImport.png)
