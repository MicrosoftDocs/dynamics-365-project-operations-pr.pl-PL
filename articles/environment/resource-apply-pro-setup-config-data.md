---
title: Konfiguracja i stosowanie danych konfiguracyjnych w usłudze Common Data Service do aplikacji Project Operations
description: W tym temacie zamieszczono informacje dotyczące ustawienia i zastosowania danych konfiguracyjnych Project Operations.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: d99ab4c7b2ebf6ba56b86a3e0151036c6247e484
ms.sourcegitcommit: b9d8bf00239815f31686e9b28998ac684fd2fca4
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/02/2020
ms.locfileid: "3949010"
---
# <a name="set-up-and-apply-configuration-data-in-the-common-data-service-for-project-operations"></a><span data-ttu-id="bf640-103">Konfiguracja i stosowanie danych konfiguracyjnych w usłudze Common Data Service do aplikacji Project Operations</span><span class="sxs-lookup"><span data-stu-id="bf640-103">Set up and apply configuration data in the Common Data Service for Project Operations</span></span>

<span data-ttu-id="bf640-104">_**Zastosowane do:** Project Operations dla zasobów/scenariuszy nieopartych na zaopatrzeniu_</span><span class="sxs-lookup"><span data-stu-id="bf640-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

## <a name="install-setup-and-configuration-data"></a><span data-ttu-id="bf640-105">Zainstaluj konfigurację i dane konfiguracyjne</span><span class="sxs-lookup"><span data-stu-id="bf640-105">Install setup and configuration data</span></span>

1. <span data-ttu-id="bf640-106">Pobierz, odblokuj i rozpakuj [pakiet danych instalacyjnych i konfiguracyjnych](https://download.microsoft.com/download/1/3/4/1349369c-6209-42b7-b3b4-5be0e67cacd8/ProjOpsSampleSetupData-%20Integrated%20UR1.zip).</span><span class="sxs-lookup"><span data-stu-id="bf640-106">Download, unblock, and unzip the [Setup and Configuration Data Package](https://download.microsoft.com/download/1/3/4/1349369c-6209-42b7-b3b4-5be0e67cacd8/ProjOpsSampleSetupData-%20Integrated%20UR1.zip).</span></span>
2. <span data-ttu-id="bf640-107">Przejdź do wyodrębnionego folderu, a następnie uruchom plik wykonywalny *DataMigrationUtility*.</span><span class="sxs-lookup"><span data-stu-id="bf640-107">Navigate to the unzipped folder and run the executable file, *DataMigrationUtility*.</span></span>
3. <span data-ttu-id="bf640-108">Na stronie 1 Kreatora migracji konfiguracji Common Data Service (CMT) wybierz pozycję **Importuj dane**, a następnie wybierz pozycję **Kontynuuj**.</span><span class="sxs-lookup"><span data-stu-id="bf640-108">On page 1 of the Common Data Service Configuration Migration (CMT) Wizard, select **Import Data** and then select **Continue**.</span></span>

![Migracja konfiguracji](./media/1ConfigurationMigration.png)

4. <span data-ttu-id="bf640-110">Na stronie 2 kreatora CMT wybierz **Office 365** jako **Typ wdrożenia**.</span><span class="sxs-lookup"><span data-stu-id="bf640-110">On Page 2 of the CMT Wizard, select **Office 365** as the **Deployment Type**.</span></span>
5. <span data-ttu-id="bf640-111">Wybierz pola wyboru **Wyświetl listę dostępnych organizacji** i **Wyświetl zaawansowane**.</span><span class="sxs-lookup"><span data-stu-id="bf640-111">Select the **Display a list of available organizations** and **Show Advanced** check boxes.</span></span>
6. <span data-ttu-id="bf640-112">Wybierz region dzierżawy, wprowadź swoje poświadczenia, a następnie wybierz pozycję **Zaloguj**.</span><span class="sxs-lookup"><span data-stu-id="bf640-112">Select the region of your tenant, enter your credentials, and select **Login**.</span></span>

![Konfiguracja logowania](./media/2ConfigurationSignin.png)

7. <span data-ttu-id="bf640-114">Na stronie 3 z poziomu listy organizacji w dzierżawie wybierz nazwę organizacji, do której chcesz zaimportować dane demonstracyjne, a następnie wybierz pozycję **Zaloguj**.</span><span class="sxs-lookup"><span data-stu-id="bf640-114">On page 3, from the list of organizations on the tenant, select the organization you want to import the demo data into and select **Login**.</span></span>
8. <span data-ttu-id="bf640-115">Na stronie 4 wybierz plik zip *SampleSetupAndConfigData*, który znajduje się w rozpakowanym folderze.</span><span class="sxs-lookup"><span data-stu-id="bf640-115">On page 4, select the zip file, *SampleSetupAndConfigData* from the unpacked folder.</span></span>

![Wybieranie pliku zip](./media/3ZipFile.png)

![Wybierz plik](./media/4SelectAFile.png)

9. <span data-ttu-id="bf640-118">Po zaznaczeniu pliku zip wybierz pozycję **Importuj dane**.</span><span class="sxs-lookup"><span data-stu-id="bf640-118">After the zip file is selected, select **Import Data**.</span></span>

![Importuj dane](./media/5ImportData.png)

10. <span data-ttu-id="bf640-120">Importowanie potrwa około dwóch sekund, w zależności od szybkości sieci.</span><span class="sxs-lookup"><span data-stu-id="bf640-120">Import will run for approximately two-ten minutes depending on your network speed.</span></span> <span data-ttu-id="bf640-121">Po zakończeniu importu zakończ działanie kreatora CMT.</span><span class="sxs-lookup"><span data-stu-id="bf640-121">After import completes, exit the CMT Wizard.</span></span> 
11. <span data-ttu-id="bf640-122">Należy sprawdzić w ramach organizacji dane z następujących 19 encji:</span><span class="sxs-lookup"><span data-stu-id="bf640-122">Check your organization for data in the following 19 entities:</span></span>

  - <span data-ttu-id="bf640-123">Waluta</span><span class="sxs-lookup"><span data-stu-id="bf640-123">Currency</span></span>
  - <span data-ttu-id="bf640-124">Jednostka organizacyjna</span><span class="sxs-lookup"><span data-stu-id="bf640-124">Organizational Unit</span></span>
  - <span data-ttu-id="bf640-125">Kontakt biznesowy</span><span class="sxs-lookup"><span data-stu-id="bf640-125">Contact</span></span>
  - <span data-ttu-id="bf640-126">Grupa podatku</span><span class="sxs-lookup"><span data-stu-id="bf640-126">Tax Group</span></span>
  - <span data-ttu-id="bf640-127">Grupa klientów</span><span class="sxs-lookup"><span data-stu-id="bf640-127">Customer Group</span></span>
  - <span data-ttu-id="bf640-128">Jednostka</span><span class="sxs-lookup"><span data-stu-id="bf640-128">Unit</span></span>
  - <span data-ttu-id="bf640-129">Grupa jednostek</span><span class="sxs-lookup"><span data-stu-id="bf640-129">Unit Group</span></span>
  - <span data-ttu-id="bf640-130">Cennik</span><span class="sxs-lookup"><span data-stu-id="bf640-130">Price List</span></span>
  - <span data-ttu-id="bf640-131">Cennik parametrów projektu</span><span class="sxs-lookup"><span data-stu-id="bf640-131">Project Parameter Price List</span></span>
  - <span data-ttu-id="bf640-132">Częstotliwość faktur</span><span class="sxs-lookup"><span data-stu-id="bf640-132">Invoice Frequency</span></span>
  - <span data-ttu-id="bf640-133">Kategoria zasobów, które można zarezerwować</span><span class="sxs-lookup"><span data-stu-id="bf640-133">Bookable Resource Category</span></span>
  - <span data-ttu-id="bf640-134">Kategoria transakcji</span><span class="sxs-lookup"><span data-stu-id="bf640-134">Transaction Category</span></span>
  - <span data-ttu-id="bf640-135">Kategoria wydatków</span><span class="sxs-lookup"><span data-stu-id="bf640-135">Expense Category</span></span>
  - <span data-ttu-id="bf640-136">Cena roli</span><span class="sxs-lookup"><span data-stu-id="bf640-136">Role Price</span></span>
  - <span data-ttu-id="bf640-137">Cena kategorii transakcji</span><span class="sxs-lookup"><span data-stu-id="bf640-137">Transaction Category Price</span></span>
  - <span data-ttu-id="bf640-138">Charakterystyka</span><span class="sxs-lookup"><span data-stu-id="bf640-138">Characteristic</span></span>
  - <span data-ttu-id="bf640-139">Zasób, który można zarezerwować</span><span class="sxs-lookup"><span data-stu-id="bf640-139">Bookable Resource</span></span>
  - <span data-ttu-id="bf640-140">Skojarzenie kategorii zasobów, które można zarezerwować</span><span class="sxs-lookup"><span data-stu-id="bf640-140">Bookable resource category Assn</span></span>
  - <span data-ttu-id="bf640-141">Charakterystyka zasobu, który można zarezerwować</span><span class="sxs-lookup"><span data-stu-id="bf640-141">Bookable Resource Characteristic</span></span>

![Zakończ importowanie](./media/6CompleteImport.png)

## <a name="update-project-operations-configurations"></a><span data-ttu-id="bf640-143">Aktualizowanie konfiguracji Project Operations</span><span class="sxs-lookup"><span data-stu-id="bf640-143">Update Project Operations configurations</span></span>

1. <span data-ttu-id="bf640-144">Przejdź do środowiska CE.</span><span class="sxs-lookup"><span data-stu-id="bf640-144">Navigate to the CE environment.</span></span> <span data-ttu-id="bf640-145">Można je znaleźć otwierając [centrum administracyjne Power Platform](https://admin.powerplatform.microsoft.com/environments), wybierając środowisko i wybierając pozycję **Otwórz środowisko**.</span><span class="sxs-lookup"><span data-stu-id="bf640-145">You can find it by opening the [Power Platform Admin Center](https://admin.powerplatform.microsoft.com/environments), selecting the environment, and then selecting **Open Environment**.</span></span> 

![Otwórz środowisko](./media/7OpenEnvironment.png)

2. <span data-ttu-id="bf640-147">Przejdź do obszaru **Projekty** > **Zasoby** i wybierz opcję **Nowy**, aby utworzyć zasób zaksięgowany dla użytkownika.</span><span class="sxs-lookup"><span data-stu-id="bf640-147">Go to **Projects** > **Resources** and then select **New** to create a bookable resource for your user.</span></span>

![Zasoby, które można zarezerwować](./media/8BookableResources.png)

3. <span data-ttu-id="bf640-149">Na karcie **Ogólne** wybierz użytkownika administracyjnego.</span><span class="sxs-lookup"><span data-stu-id="bf640-149">On the **General** tab, select your admin user.</span></span> <span data-ttu-id="bf640-150">Sprawdź, czy strefa czasowa jest zgodna z strefą, w której się znajdujesz.</span><span class="sxs-lookup"><span data-stu-id="bf640-150">Verify that the time zone matches the one you are in.</span></span> 

![Nowy zasób, który można zarezerwować](./media/9NewBookableResource.png)

4. <span data-ttu-id="bf640-152">Na karcie **Planowanie**, w polu **Firma** wybierz firmę **USPM**, a następnie wybierz pozycję **Zapisz**.</span><span class="sxs-lookup"><span data-stu-id="bf640-152">On the **Scheduling** tab, in the **Company** field, pick the **USPM** company, and then select **Save**.</span></span> 

![Karta planowania](./media/10SchedulingTab.png)

5. <span data-ttu-id="bf640-154">Wybierz kartę **Godziny pracy**.</span><span class="sxs-lookup"><span data-stu-id="bf640-154">Select the **Work hours** tab.</span></span>  

![Godziny pracy](./media/11WorkHours.png)

6. <span data-ttu-id="bf640-156">Kliknij dwukrotnie dowolną wartość w kalendarzu i wybierz pozycję **Edytuj** > **Wszystkie zdarzenia z serii**.</span><span class="sxs-lookup"><span data-stu-id="bf640-156">Double-click on any value in the calendar and select **Edit** > **All events in the series**.</span></span> 

![Kalendarz pracy](./media/12WorkCalendar.png)

7. <span data-ttu-id="bf640-158">Zmień godziny pracy na osiem (8) godzin w trakcie dnia pracy i zaznacz weekendy jako dni wolne od pracy i upewnij się, że strefa czasowa odpowiada Twojej.</span><span class="sxs-lookup"><span data-stu-id="bf640-158">Change work hours to an eight (8) hour work day, mark weekends as non-work days, and make sure time zone matches yours.</span></span> 
8. <span data-ttu-id="bf640-159">Wybierz **Zapisz i zamknij**.</span><span class="sxs-lookup"><span data-stu-id="bf640-159">Select **Save and close**.</span></span>

![Aktualizacja kalendarza](./media/13UpdateCalendar.png)

9. <span data-ttu-id="bf640-161">Wybierz kolejno pozycje **Ustawienia** > **Szablony kalendarza** i utwórz **Nowy**.</span><span class="sxs-lookup"><span data-stu-id="bf640-161">Go to **Settings** > **Calendar templates** and select **New**.</span></span>
 
 ![Szablony kalendarzy](./media/14CalendarTemplates.png)
 
 10. <span data-ttu-id="bf640-163">Wprowadź nazwę, zaznacz utworzony szablon zasobu, a następnie wybierz pozycję **Zapisz**.</span><span class="sxs-lookup"><span data-stu-id="bf640-163">Enter a name, select the template resource you created, and then select **Save**.</span></span> 
 
 ![Zapisz szablon kalendarza](./media/15SaveCalendarTemplate.png)
 
 11. <span data-ttu-id="bf640-165">Przejdź do obszaru **Parametry** i kliknij dwukrotnie rekord.</span><span class="sxs-lookup"><span data-stu-id="bf640-165">Go to **Parameters** and double-click the record.</span></span> 
 
 ![Parametry projektu](./media/16ProjectParameters.png)
 
12. <span data-ttu-id="bf640-167">Zaktualizuj następujące pola:</span><span class="sxs-lookup"><span data-stu-id="bf640-167">Update the following fields:</span></span>

 - <span data-ttu-id="bf640-168">**Domyślna firma**: USPM</span><span class="sxs-lookup"><span data-stu-id="bf640-168">**Default company**: USPM</span></span>
 - <span data-ttu-id="bf640-169">**Domyślna jednostka organizacyjna**: Contoso Robotics Global</span><span class="sxs-lookup"><span data-stu-id="bf640-169">**Default Organizational Unit**: Contoso Robotics Global</span></span>
 - <span data-ttu-id="bf640-170">**Częstotliwość fakturowania**: siódmy i ostatni dzień</span><span class="sxs-lookup"><span data-stu-id="bf640-170">**Invoice Frequency**: Seventh and Last day</span></span>
 - <span data-ttu-id="bf640-171">**Szablon godzin pracy**: Zmień na utworzony szablon.</span><span class="sxs-lookup"><span data-stu-id="bf640-171">**Work hour template**: Change to the template you created.</span></span>

13. <span data-ttu-id="bf640-172">Wybierz pozycję **Zapisz**.</span><span class="sxs-lookup"><span data-stu-id="bf640-172">Select **Save**.</span></span> 

![Zaktualizowane parametry projektu](./media/17UpdatedProjectParameters.png)
