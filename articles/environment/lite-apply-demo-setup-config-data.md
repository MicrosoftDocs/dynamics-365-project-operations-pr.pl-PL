---
title: Zastosowanie konfiguracji demonstracyjnej i danych konfiguracyjnych — wersja uproszczona
description: W tym temacie zamieszczono informacje dotyczące sposobu stosowania konfiguracji demonstracyjnej i danych konfiguracyjnych Project Operations.
author: sigitac
manager: Annbe
ms.date: 11/04/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 421c9d28088c92617687641d93b3ad5d6bfea73c
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 11/25/2020
ms.locfileid: "4642106"
---
# <a name="apply-demo-setup-and-configuration-data-for-project-operations---lite"></a><span data-ttu-id="62c20-103">Zastosowanie konfiguracji demonstracyjnej i danych konfiguracyjnych dla Project Operations — wersja uproszczona</span><span class="sxs-lookup"><span data-stu-id="62c20-103">Apply demo setup and configuration data for Project Operations - lite</span></span> 

<span data-ttu-id="62c20-104">_\*\*Wdrażanie uproszczone — od oferty do faktury pro forma_</span><span class="sxs-lookup"><span data-stu-id="62c20-104">_\*\*Lite deployment - deal to proforma invoicing_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

## <a name="prerequisites"></a><span data-ttu-id="62c20-105">Wymagania wstępne</span><span class="sxs-lookup"><span data-stu-id="62c20-105">Prerequisites</span></span>

<span data-ttu-id="62c20-106">Przed rozpoczęciem konfiguracji należy dysponować środowiskiem usługi Common Data Service (CDS) ustanowionym dla aplikacji Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="62c20-106">Before you begin the configuration, you must have a Common Data Service (CDS) environment provisioned for Dynamics 365 Project Operations.</span></span>


## <a name="instructions"></a><span data-ttu-id="62c20-107">Instrukcje</span><span class="sxs-lookup"><span data-stu-id="62c20-107">Instructions</span></span>

1. <span data-ttu-id="62c20-108">Pobierz [pakiet Master Data Package](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData%20-%20CE%20only%20CMT.zip).</span><span class="sxs-lookup"><span data-stu-id="62c20-108">Download the [Master Data Package](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData%20-%20CE%20only%20CMT.zip).</span></span> 
2. <span data-ttu-id="62c20-109">Przejdź do folderu *ProjOpsDemoDataSetupAndMaster - Integrated CMT*, a następnie uruchom plik wykonywalny *DataMigrationUtility*.</span><span class="sxs-lookup"><span data-stu-id="62c20-109">Navigate to the folder *ProjOpsDemoDataSetupAndMaster - Integrated CMT* and run the executable file, *DataMigrationUtility*.</span></span>
3. <span data-ttu-id="62c20-110">Na stronie 1 Kreatora migracji konfiguracji Common Data Service (CMT) wybierz pozycję **Importuj dane**, a następnie wybierz pozycję **Kontynuuj**.</span><span class="sxs-lookup"><span data-stu-id="62c20-110">On page 1 of the Common Data Service Configuration Migration (CMT) Wizard, select **Import Data** and then select **Continue**.</span></span>

![Migracja konfiguracji](./media/1ConfigurationMigration.png)

4. <span data-ttu-id="62c20-112">Na stronie 2 kreatora CMT wybierz **Microsoft 365** jako **Typ wdrożenia**.</span><span class="sxs-lookup"><span data-stu-id="62c20-112">On Page 2 of the CMT Wizard, select **Microsoft 365** as the **Deployment Type**.</span></span>
5. <span data-ttu-id="62c20-113">Wybierz pola wyboru **Wyświetl listę dostępnych organizacji** i **Wyświetl zaawansowane**.</span><span class="sxs-lookup"><span data-stu-id="62c20-113">Select the **Display a list of available organizations** and **Show Advanced** check boxes.</span></span>
6. <span data-ttu-id="62c20-114">Wybierz region dzierżawy, wprowadź swoje poświadczenia, a następnie wybierz pozycję **Zaloguj**.</span><span class="sxs-lookup"><span data-stu-id="62c20-114">Select the region of your tenant, enter your credentials, and then select **Login**.</span></span>

![Konfiguracja logowania](./media/2ConfigurationSignin.png)

7. <span data-ttu-id="62c20-116">Na stronie 3 z poziomu listy organizacji w dzierżawie wybierz nazwę organizacji, do której chcesz zaimportować dane demonstracyjne, a następnie wybierz pozycję **Zaloguj**.</span><span class="sxs-lookup"><span data-stu-id="62c20-116">On page 3, from the list of Organizations on the Tenant, select which organization you want to import the demo data into and then select **Login**.</span></span>
8. <span data-ttu-id="62c20-117">Na stronie 4 wybierz plik zip *MasterAndSetupData*, który znajduje się w rozpakowanym folderze *ProjOpsDemoDataSetupAndMaster - Integrated CMT*.</span><span class="sxs-lookup"><span data-stu-id="62c20-117">On page 4, select the zip file, *MasterAndSetupData* from the unpacked folder, *ProjOpsDemoDataSetupAndMaster - Integrated CMT*.</span></span>

![Plik ZIP](./media/3ZipFile.png)

![Wybierz plik](./media/4SelectAFile.png)

9. <span data-ttu-id="62c20-120">Po zaznaczeniu pliku zip wybierz pozycję **Importuj dane**.</span><span class="sxs-lookup"><span data-stu-id="62c20-120">After the zip file is selected, select **Import Data**.</span></span>

![Importuj dane](./media/5ImportData.png)

10. <span data-ttu-id="62c20-122">Importowanie potrwa około dwóch sekund, w zależności od szybkości sieci.</span><span class="sxs-lookup"><span data-stu-id="62c20-122">Import will run for approximately two-ten minutes depending on your network speed.</span></span> <span data-ttu-id="62c20-123">Po zakończeniu pracy zakończ działanie kreatora CMT.</span><span class="sxs-lookup"><span data-stu-id="62c20-123">After it completes, exit the CMT Wizard.</span></span> 
11. <span data-ttu-id="62c20-124">Należy sprawdzić w ramach organizacji dane z następujących 20 encji:</span><span class="sxs-lookup"><span data-stu-id="62c20-124">Check your organization for data in the following 20 entities:</span></span>

-   <span data-ttu-id="62c20-125">Waluta</span><span class="sxs-lookup"><span data-stu-id="62c20-125">Currency</span></span>
-   <span data-ttu-id="62c20-126">Konto</span><span class="sxs-lookup"><span data-stu-id="62c20-126">Account</span></span>
-   <span data-ttu-id="62c20-127">Jednostka organizacyjna</span><span class="sxs-lookup"><span data-stu-id="62c20-127">Organizational Unit</span></span>
-   <span data-ttu-id="62c20-128">Kontakt biznesowy</span><span class="sxs-lookup"><span data-stu-id="62c20-128">Contact</span></span>
-   <span data-ttu-id="62c20-129">Grupa podatku</span><span class="sxs-lookup"><span data-stu-id="62c20-129">Tax Group</span></span>
-   <span data-ttu-id="62c20-130">Grupa klientów</span><span class="sxs-lookup"><span data-stu-id="62c20-130">Customer Group</span></span>
-   <span data-ttu-id="62c20-131">Jednostka</span><span class="sxs-lookup"><span data-stu-id="62c20-131">Unit</span></span>
-   <span data-ttu-id="62c20-132">Grupa jednostek</span><span class="sxs-lookup"><span data-stu-id="62c20-132">Unit Group</span></span>
-   <span data-ttu-id="62c20-133">Cennik</span><span class="sxs-lookup"><span data-stu-id="62c20-133">Price List</span></span>
-   <span data-ttu-id="62c20-134">Cennik parametrów projektu</span><span class="sxs-lookup"><span data-stu-id="62c20-134">Project Parameter Price List</span></span> 
-   <span data-ttu-id="62c20-135">Częstotliwość faktur</span><span class="sxs-lookup"><span data-stu-id="62c20-135">Invoice Frequency</span></span>
-   <span data-ttu-id="62c20-136">Kategoria zasobów, które można zarezerwować</span><span class="sxs-lookup"><span data-stu-id="62c20-136">Bookable Resource Category</span></span>
-   <span data-ttu-id="62c20-137">Kategoria transakcji</span><span class="sxs-lookup"><span data-stu-id="62c20-137">Transaction Category</span></span>
-   <span data-ttu-id="62c20-138">Kategoria wydatków</span><span class="sxs-lookup"><span data-stu-id="62c20-138">Expense Category</span></span>
-   <span data-ttu-id="62c20-139">Cena roli</span><span class="sxs-lookup"><span data-stu-id="62c20-139">Role Price</span></span>
-   <span data-ttu-id="62c20-140">Cena kategorii transakcji</span><span class="sxs-lookup"><span data-stu-id="62c20-140">Transaction Category Price</span></span>
-   <span data-ttu-id="62c20-141">Charakterystyka</span><span class="sxs-lookup"><span data-stu-id="62c20-141">Characteristic</span></span>
-   <span data-ttu-id="62c20-142">Zasób, który można zarezerwować</span><span class="sxs-lookup"><span data-stu-id="62c20-142">Bookable Resource</span></span>
-   <span data-ttu-id="62c20-143">Skojarzenie kategorii zasobów, które można zarezerwować</span><span class="sxs-lookup"><span data-stu-id="62c20-143">Bookable resource category Assn</span></span>
-   <span data-ttu-id="62c20-144">Charakterystyka zasobu, który można zarezerwować</span><span class="sxs-lookup"><span data-stu-id="62c20-144">Bookable Resource Characteristic</span></span>

![Zakończ importowanie](./media/6CompleteImport.png)
