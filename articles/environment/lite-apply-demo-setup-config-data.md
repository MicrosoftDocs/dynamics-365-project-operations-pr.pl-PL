---
title: Zastosowanie konfiguracji demonstracyjnej i danych konfiguracyjnych
description: W tym temacie zamieszczono informacje dotyczące sposobu stosowania konfiguracji demonstracyjnej i danych konfiguracyjnych Project Operations.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 42e02f393e89d20b2a462645f519a3792bee8f2f
ms.sourcegitcommit: b9d8bf00239815f31686e9b28998ac684fd2fca4
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/02/2020
ms.locfileid: "3949007"
---
# <a name="apply-demo-setup-and-configuration-data-for-project-operations-lite-deployment---deal-to-proforma-invoicing"></a><span data-ttu-id="e1cad-103">Zastosowanie konfiguracji demonstracyjnej i danych konfiguracyjnych do wdrożenia uproszczonej wersji Project Operations — oferta do fakturowania proforma</span><span class="sxs-lookup"><span data-stu-id="e1cad-103">Apply demo setup and configuration data for Project Operations lite deployment - deal to proforma invoicing</span></span>

<span data-ttu-id="e1cad-104">_\*\*Wdrażanie uproszczone — od oferty do faktury pro forma_</span><span class="sxs-lookup"><span data-stu-id="e1cad-104">_\*\*Lite deployment - deal to proforma invoicing_</span></span>

1. <span data-ttu-id="e1cad-105">Pobierz [pakiet Master Data Package](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData%20-%20CE%20only%20CMT.zip).</span><span class="sxs-lookup"><span data-stu-id="e1cad-105">Download the [Master Data Package](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData%20-%20CE%20only%20CMT.zip).</span></span> 
2. <span data-ttu-id="e1cad-106">Przejdź do folderu *ProjOpsDemoDataSetupAndMaster - Integrated CMT*, a następnie uruchom plik wykonywalny *DataMigrationUtility*.</span><span class="sxs-lookup"><span data-stu-id="e1cad-106">Navigate to the folder *ProjOpsDemoDataSetupAndMaster - Integrated CMT* and run the executable file, *DataMigrationUtility*.</span></span>
3. <span data-ttu-id="e1cad-107">Na stronie 1 Kreatora migracji konfiguracji Common Data Service (CMT) wybierz pozycję **Importuj dane**, a następnie wybierz pozycję **Kontynuuj**.</span><span class="sxs-lookup"><span data-stu-id="e1cad-107">On page 1 of the Common Data Service Configuration Migration (CMT) Wizard, select **Import Data** and then select **Continue**.</span></span>

![Migracja konfiguracji](./media/1ConfigurationMigration.png)

4. <span data-ttu-id="e1cad-109">Na stronie 2 kreatora CMT wybierz **Office 365** jako **Typ wdrożenia**.</span><span class="sxs-lookup"><span data-stu-id="e1cad-109">On Page 2 of the CMT Wizard, select **Office 365** as the **Deployment Type**.</span></span>
5. <span data-ttu-id="e1cad-110">Wybierz pola wyboru **Wyświetl listę dostępnych organizacji** i **Wyświetl zaawansowane**.</span><span class="sxs-lookup"><span data-stu-id="e1cad-110">Select the **Display a list of available organizations** and **Show Advanced** check boxes.</span></span>
6. <span data-ttu-id="e1cad-111">Wybierz region dzierżawy, wprowadź swoje poświadczenia, a następnie wybierz pozycję **Zaloguj**.</span><span class="sxs-lookup"><span data-stu-id="e1cad-111">Select the region of your tenant, enter your credentials, and then select **Login**.</span></span>

![Konfiguracja logowania](./media/2ConfigurationSignin.png)

7. <span data-ttu-id="e1cad-113">Na stronie 3 z poziomu listy organizacji w dzierżawie wybierz nazwę organizacji, do której chcesz zaimportować dane demonstracyjne, a następnie wybierz pozycję **Zaloguj**.</span><span class="sxs-lookup"><span data-stu-id="e1cad-113">On page 3, from the list of Organizations on the Tenant, select which organization you want to import the demo data into and then select **Login**.</span></span>
8. <span data-ttu-id="e1cad-114">Na stronie 4 wybierz plik zip *MasterAndSetupData*, który znajduje się w rozpakowanym folderze *ProjOpsDemoDataSetupAndMaster - Integrated CMT*.</span><span class="sxs-lookup"><span data-stu-id="e1cad-114">On page 4, select the zip file, *MasterAndSetupData* from the unpacked folder, *ProjOpsDemoDataSetupAndMaster - Integrated CMT*.</span></span>

![Plik ZIP](./media/3ZipFile.png)

![Wybierz plik](./media/4SelectAFile.png)

9. <span data-ttu-id="e1cad-117">Po zaznaczeniu pliku zip wybierz pozycję **Importuj dane**.</span><span class="sxs-lookup"><span data-stu-id="e1cad-117">After the zip file is selected, select **Import Data**.</span></span>

![Importuj dane](./media/5ImportData.png)

10. <span data-ttu-id="e1cad-119">Importowanie potrwa około dwóch sekund, w zależności od szybkości sieci.</span><span class="sxs-lookup"><span data-stu-id="e1cad-119">Import will run for approximately two-ten minutes depending on your network speed.</span></span> <span data-ttu-id="e1cad-120">Po zakończeniu pracy zakończ działanie kreatora CMT.</span><span class="sxs-lookup"><span data-stu-id="e1cad-120">After it completes, exit the CMT Wizard.</span></span> 
11. <span data-ttu-id="e1cad-121">Należy sprawdzić w ramach organizacji dane z następujących 20 encji:</span><span class="sxs-lookup"><span data-stu-id="e1cad-121">Check your organization for data in the following 20 entities:</span></span>

- <span data-ttu-id="e1cad-122">Waluta</span><span class="sxs-lookup"><span data-stu-id="e1cad-122">Currency</span></span>
- <span data-ttu-id="e1cad-123">Jednostka organizacyjna</span><span class="sxs-lookup"><span data-stu-id="e1cad-123">Organizational Unit</span></span>
- <span data-ttu-id="e1cad-124">Kontakt biznesowy</span><span class="sxs-lookup"><span data-stu-id="e1cad-124">Contact</span></span>
- <span data-ttu-id="e1cad-125">Grupa podatku</span><span class="sxs-lookup"><span data-stu-id="e1cad-125">Tax Group</span></span>
- <span data-ttu-id="e1cad-126">Grupa klientów</span><span class="sxs-lookup"><span data-stu-id="e1cad-126">Customer Group</span></span>
- <span data-ttu-id="e1cad-127">Jednostka</span><span class="sxs-lookup"><span data-stu-id="e1cad-127">Unit</span></span>
- <span data-ttu-id="e1cad-128">Grupa jednostek</span><span class="sxs-lookup"><span data-stu-id="e1cad-128">Unit Group</span></span>
- <span data-ttu-id="e1cad-129">Cennik</span><span class="sxs-lookup"><span data-stu-id="e1cad-129">Price List</span></span>
- <span data-ttu-id="e1cad-130">Cennik parametrów projektu</span><span class="sxs-lookup"><span data-stu-id="e1cad-130">Project Parameter Price List</span></span>
- <span data-ttu-id="e1cad-131">Częstotliwość faktur</span><span class="sxs-lookup"><span data-stu-id="e1cad-131">Invoice Frequency</span></span>
- <span data-ttu-id="e1cad-132">Szczegóły częstotliwości faktur</span><span class="sxs-lookup"><span data-stu-id="e1cad-132">Invoice Frequency Detail</span></span>
- <span data-ttu-id="e1cad-133">Kategoria zasobów, które można zarezerwować</span><span class="sxs-lookup"><span data-stu-id="e1cad-133">Bookable Resource Category</span></span>
- <span data-ttu-id="e1cad-134">Kategoria transakcji</span><span class="sxs-lookup"><span data-stu-id="e1cad-134">Transaction Category</span></span>
- <span data-ttu-id="e1cad-135">Kategoria wydatków</span><span class="sxs-lookup"><span data-stu-id="e1cad-135">Expense Category</span></span>
- <span data-ttu-id="e1cad-136">Cena roli</span><span class="sxs-lookup"><span data-stu-id="e1cad-136">Role Price</span></span>
- <span data-ttu-id="e1cad-137">Cena kategorii transakcji</span><span class="sxs-lookup"><span data-stu-id="e1cad-137">Transaction Category Price</span></span>
- <span data-ttu-id="e1cad-138">Charakterystyka</span><span class="sxs-lookup"><span data-stu-id="e1cad-138">Characteristic</span></span>
- <span data-ttu-id="e1cad-139">Zasób, który można zarezerwować</span><span class="sxs-lookup"><span data-stu-id="e1cad-139">Bookable Resource</span></span>
- <span data-ttu-id="e1cad-140">Skojarzenie kategorii zasobów, które można zarezerwować</span><span class="sxs-lookup"><span data-stu-id="e1cad-140">Bookable resource category Assn</span></span>
- <span data-ttu-id="e1cad-141">Charakterystyka zasobu, który można zarezerwować</span><span class="sxs-lookup"><span data-stu-id="e1cad-141">Bookable Resource Characteristic</span></span>

![Zakończ importowanie](./media/6CompleteImport.png)
