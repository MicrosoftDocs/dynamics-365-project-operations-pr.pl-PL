---
title: Skonfiguruj i zastosuj dane konfiguracyjne w usłudze Common Data Service
description: W tym temacie zamieszczono informacje dotyczące ustawienia i zastosowania danych konfiguracyjnych Project Operations.
author: sigitac
ms.date: 05/10/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 2ea00df6112fb69b61f1889463424fdfee79aec9
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 05/10/2021
ms.locfileid: "6001304"
---
# <a name="set-up-and-apply-configuration-data-in-the-common-data-service"></a><span data-ttu-id="d1405-103">Skonfiguruj i zastosuj dane konfiguracyjne w usłudze Common Data Service</span><span class="sxs-lookup"><span data-stu-id="d1405-103">Set up and apply configuration data in the Common Data Service</span></span> 

<span data-ttu-id="d1405-104">_**Zastosowane do:** Project Operations dla zasobów/scenariuszy nieopartych na zaopatrzeniu_</span><span class="sxs-lookup"><span data-stu-id="d1405-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

## <a name="prerequisites"></a><span data-ttu-id="d1405-105">Wymagania wstępne</span><span class="sxs-lookup"><span data-stu-id="d1405-105">Prerequisites</span></span>

<span data-ttu-id="d1405-106">Przed rozpoczęciem konfigurowania danych w ramach Common Data Service (CDS) należy spełnić następujące warunki wstępne:</span><span class="sxs-lookup"><span data-stu-id="d1405-106">Before you begin to configure data in the Common Data Service (CDS), the following prerequisites must be met:</span></span>

1.  <span data-ttu-id="d1405-107">Udostępnij środowisko CDS i środowisko Dynamics 365 Finance na potrzeby Project Operations.</span><span class="sxs-lookup"><span data-stu-id="d1405-107">Provision a CDS environment and a Dynamics 365 Finance environment for Project Operations.</span></span>
2.  <span data-ttu-id="d1405-108">Informacje o osobach prawnych z Dynamics 365 Finance są udostępniane środowisku CDS.</span><span class="sxs-lookup"><span data-stu-id="d1405-108">Legal entity information from Dynamics 365 Finance is shared to the CDS environment.</span></span> <span data-ttu-id="d1405-109">Oznacza to, że **Firma** z CDS zawiera następujące rekordy firm:</span><span class="sxs-lookup"><span data-stu-id="d1405-109">This means that the **Company** entity in CDS has the following company records:</span></span>
  - <span data-ttu-id="d1405-110">THPM</span><span class="sxs-lookup"><span data-stu-id="d1405-110">THPM</span></span>
  - <span data-ttu-id="d1405-111">USPM</span><span class="sxs-lookup"><span data-stu-id="d1405-111">USPM</span></span>
  - <span data-ttu-id="d1405-112">GBPM</span><span class="sxs-lookup"><span data-stu-id="d1405-112">GBPM</span></span>

## <a name="install-setup-and-configuration-data"></a><span data-ttu-id="d1405-113">Zainstaluj konfigurację i dane konfiguracyjne</span><span class="sxs-lookup"><span data-stu-id="d1405-113">Install setup and configuration data</span></span>

1. <span data-ttu-id="d1405-114">Pobierz, odblokuj i rozpakuj [pakiet danych instalacyjnych i konfiguracyjnych](https://download.microsoft.com/download/e/2/d/e2da6c98-d5dd-450c-aabe-fd6bf2ba374b/ProjOpsSampleSetupData-%20Integrated%20Latest.zip).</span><span class="sxs-lookup"><span data-stu-id="d1405-114">Download, unblock, and unzip the [Setup and Configuration Data Package](https://download.microsoft.com/download/e/2/d/e2da6c98-d5dd-450c-aabe-fd6bf2ba374b/ProjOpsSampleSetupData-%20Integrated%20Latest.zip).</span></span>
2. <span data-ttu-id="d1405-115">Przejdź do wyodrębnionego folderu, a następnie uruchom plik wykonywalny *DataMigrationUtility*.</span><span class="sxs-lookup"><span data-stu-id="d1405-115">Navigate to the unzipped folder and run the executable file, *DataMigrationUtility*.</span></span>
3. <span data-ttu-id="d1405-116">Na stronie 1 Kreatora migracji konfiguracji Common Data Service (CMT) wybierz pozycję **Importuj dane**, a następnie wybierz pozycję **Kontynuuj**.</span><span class="sxs-lookup"><span data-stu-id="d1405-116">On page 1 of the Common Data Service Configuration Migration (CMT) Wizard, select **Import Data** and then select **Continue**.</span></span>

![Migracja konfiguracji](./media/1ConfigurationMigration.png)

4. <span data-ttu-id="d1405-118">Na stronie 2 kreatora CMT wybierz **Microsoft 365** jako **Typ wdrożenia**.</span><span class="sxs-lookup"><span data-stu-id="d1405-118">On Page 2 of the CMT Wizard, select **Microsoft 365** as the **Deployment Type**.</span></span>
5. <span data-ttu-id="d1405-119">Wybierz pola wyboru **Wyświetl listę dostępnych organizacji** i **Wyświetl zaawansowane**.</span><span class="sxs-lookup"><span data-stu-id="d1405-119">Select the **Display a list of available organizations** and **Show Advanced** check boxes.</span></span>
6. <span data-ttu-id="d1405-120">Wybierz region dzierżawy, wprowadź swoje poświadczenia, a następnie wybierz pozycję **Zaloguj**.</span><span class="sxs-lookup"><span data-stu-id="d1405-120">Select the region of your tenant, enter your credentials, and select **Login**.</span></span>

![Konfiguracja logowania](./media/2ConfigurationSignin.png)

7. <span data-ttu-id="d1405-122">Na stronie 3 z poziomu listy organizacji w dzierżawie wybierz nazwę organizacji, do której chcesz zaimportować dane demonstracyjne, a następnie wybierz pozycję **Zaloguj**.</span><span class="sxs-lookup"><span data-stu-id="d1405-122">On page 3, from the list of organizations on the tenant, select the organization you want to import the demo data into and select **Login**.</span></span>
8. <span data-ttu-id="d1405-123">Na stronie 4 wybierz plik zip *SampleSetupAndConfigData*, który znajduje się w rozpakowanym folderze.</span><span class="sxs-lookup"><span data-stu-id="d1405-123">On page 4, select the zip file, *SampleSetupAndConfigData* from the unpacked folder.</span></span>

![Wybieranie pliku zip](./media/3ZipFile.png)

![Wybierz plik](./media/4SelectAFile.png)

9. <span data-ttu-id="d1405-126">Po zaznaczeniu pliku zip wybierz pozycję **Importuj dane**.</span><span class="sxs-lookup"><span data-stu-id="d1405-126">After the zip file is selected, select **Import Data**.</span></span>

![Importuj dane](./media/5ImportData.png)

10. <span data-ttu-id="d1405-128">Importowanie potrwa około dwóch sekund, w zależności od szybkości sieci.</span><span class="sxs-lookup"><span data-stu-id="d1405-128">Import will run for approximately two-ten minutes depending on your network speed.</span></span> <span data-ttu-id="d1405-129">Po zakończeniu importu zakończ działanie kreatora CMT.</span><span class="sxs-lookup"><span data-stu-id="d1405-129">After import completes, exit the CMT Wizard.</span></span> 
11. <span data-ttu-id="d1405-130">Należy sprawdzić w ramach organizacji dane z następujących 26 encji:</span><span class="sxs-lookup"><span data-stu-id="d1405-130">Check your organization for data in the following 26 entities:</span></span>

  - <span data-ttu-id="d1405-131">Waluta</span><span class="sxs-lookup"><span data-stu-id="d1405-131">Currency</span></span>
  - <span data-ttu-id="d1405-132">Plan kont</span><span class="sxs-lookup"><span data-stu-id="d1405-132">Chart of Accounts</span></span>
  - <span data-ttu-id="d1405-133">Kalendarz obrachunkowy</span><span class="sxs-lookup"><span data-stu-id="d1405-133">Fiscal Calendar</span></span>
  - <span data-ttu-id="d1405-134">Rodzaje kursów walutowych</span><span class="sxs-lookup"><span data-stu-id="d1405-134">Currency Exchange Rate Types</span></span>
  - <span data-ttu-id="d1405-135">Dzień płatności</span><span class="sxs-lookup"><span data-stu-id="d1405-135">Payment Day</span></span>
  - <span data-ttu-id="d1405-136">Harmonogram płatności</span><span class="sxs-lookup"><span data-stu-id="d1405-136">Payment Schedule</span></span>
  - <span data-ttu-id="d1405-137">Termin płatności</span><span class="sxs-lookup"><span data-stu-id="d1405-137">Payment Term</span></span>
  - <span data-ttu-id="d1405-138">Jednostka organizacyjna</span><span class="sxs-lookup"><span data-stu-id="d1405-138">Organizational Unit</span></span>
  - <span data-ttu-id="d1405-139">Kontakt</span><span class="sxs-lookup"><span data-stu-id="d1405-139">Contact</span></span>
  - <span data-ttu-id="d1405-140">Grupa podatku</span><span class="sxs-lookup"><span data-stu-id="d1405-140">Tax Group</span></span>
  - <span data-ttu-id="d1405-141">Grupa klientów</span><span class="sxs-lookup"><span data-stu-id="d1405-141">Customer Group</span></span>
  - <span data-ttu-id="d1405-142">Grupa dostawców</span><span class="sxs-lookup"><span data-stu-id="d1405-142">Vendor Group</span></span>
  - <span data-ttu-id="d1405-143">Jednostka</span><span class="sxs-lookup"><span data-stu-id="d1405-143">Unit</span></span>
  - <span data-ttu-id="d1405-144">Grupa jednostek</span><span class="sxs-lookup"><span data-stu-id="d1405-144">Unit Group</span></span>
  - <span data-ttu-id="d1405-145">Cennik</span><span class="sxs-lookup"><span data-stu-id="d1405-145">Price List</span></span>
  - <span data-ttu-id="d1405-146">Cennik parametrów projektu</span><span class="sxs-lookup"><span data-stu-id="d1405-146">Project Parameter Price List</span></span>
  - <span data-ttu-id="d1405-147">Częstotliwość faktur</span><span class="sxs-lookup"><span data-stu-id="d1405-147">Invoice Frequency</span></span>
  - <span data-ttu-id="d1405-148">Kategoria zasobów, które można zarezerwować</span><span class="sxs-lookup"><span data-stu-id="d1405-148">Bookable Resource Category</span></span>
  - <span data-ttu-id="d1405-149">Kategoria transakcji</span><span class="sxs-lookup"><span data-stu-id="d1405-149">Transaction Category</span></span>
  - <span data-ttu-id="d1405-150">Kategoria wydatków</span><span class="sxs-lookup"><span data-stu-id="d1405-150">Expense Category</span></span>
  - <span data-ttu-id="d1405-151">Cena roli</span><span class="sxs-lookup"><span data-stu-id="d1405-151">Role Price</span></span>
  - <span data-ttu-id="d1405-152">Cena kategorii transakcji</span><span class="sxs-lookup"><span data-stu-id="d1405-152">Transaction Category Price</span></span>
  - <span data-ttu-id="d1405-153">Charakterystyka</span><span class="sxs-lookup"><span data-stu-id="d1405-153">Characteristic</span></span>
  - <span data-ttu-id="d1405-154">Zasób, który można zarezerwować</span><span class="sxs-lookup"><span data-stu-id="d1405-154">Bookable Resource</span></span>
  - <span data-ttu-id="d1405-155">Skojarzenie kategorii zasobów, które można zarezerwować</span><span class="sxs-lookup"><span data-stu-id="d1405-155">Bookable resource category Assn</span></span>
  - <span data-ttu-id="d1405-156">Charakterystyka zasobu, który można zarezerwować</span><span class="sxs-lookup"><span data-stu-id="d1405-156">Bookable Resource Characteristic</span></span>

![Zakończ importowanie](./media/6CompleteImport.png)

## <a name="update-project-operations-configurations"></a><span data-ttu-id="d1405-158">Aktualizowanie konfiguracji Project Operations</span><span class="sxs-lookup"><span data-stu-id="d1405-158">Update Project Operations configurations</span></span>

1. <span data-ttu-id="d1405-159">Przejdź do środowiska CE.</span><span class="sxs-lookup"><span data-stu-id="d1405-159">Navigate to the CE environment.</span></span> <span data-ttu-id="d1405-160">Można je znaleźć otwierając [centrum administracyjne Power Platform](https://admin.powerplatform.microsoft.com/environments), wybierając środowisko i wybierając pozycję **Otwórz środowisko**.</span><span class="sxs-lookup"><span data-stu-id="d1405-160">You can find it by opening the [Power Platform Admin Center](https://admin.powerplatform.microsoft.com/environments), selecting the environment, and then selecting **Open Environment**.</span></span> 

![Otwórz środowisko](./media/7OpenEnvironment.png)

2. <span data-ttu-id="d1405-162">Przejdź do obszaru **Projekty** > **Zasoby** i wybierz opcję **Nowy**, aby utworzyć zasób zaksięgowany dla użytkownika.</span><span class="sxs-lookup"><span data-stu-id="d1405-162">Go to **Projects** > **Resources** and then select **New** to create a bookable resource for your user.</span></span>

![Zasoby, które można zarezerwować](./media/8BookableResources.png)

3. <span data-ttu-id="d1405-164">Na karcie **Ogólne** wybierz użytkownika administracyjnego.</span><span class="sxs-lookup"><span data-stu-id="d1405-164">On the **General** tab, select your admin user.</span></span> <span data-ttu-id="d1405-165">Sprawdź, czy strefa czasowa jest zgodna z strefą, w której się znajdujesz.</span><span class="sxs-lookup"><span data-stu-id="d1405-165">Verify that the time zone matches the one you are in.</span></span> 

![Nowy zasób, który można zarezerwować](./media/9NewBookableResource.png)

4. <span data-ttu-id="d1405-167">Na karcie **Planowanie**, w polu **Firma** wybierz firmę **USPM**, a następnie wybierz pozycję **Zapisz**.</span><span class="sxs-lookup"><span data-stu-id="d1405-167">On the **Scheduling** tab, in the **Company** field, pick the **USPM** company, and then select **Save**.</span></span> 

![Karta planowania](./media/10SchedulingTab.png)

5. <span data-ttu-id="d1405-169">Wybierz kartę **Godziny pracy**.</span><span class="sxs-lookup"><span data-stu-id="d1405-169">Select the **Work hours** tab.</span></span>  

![Godziny pracy](./media/11WorkHours.png)

6. <span data-ttu-id="d1405-171">Kliknij dwukrotnie dowolną wartość w kalendarzu i wybierz pozycję **Edytuj** > **Wszystkie zdarzenia z serii**.</span><span class="sxs-lookup"><span data-stu-id="d1405-171">Double-click on any value in the calendar and select **Edit** > **All events in the series**.</span></span> 

![Kalendarz pracy](./media/12WorkCalendar.png)

7. <span data-ttu-id="d1405-173">Zmień godziny pracy na osiem (8) godzin w trakcie dnia pracy i zaznacz weekendy jako dni wolne od pracy i upewnij się, że strefa czasowa odpowiada Twojej.</span><span class="sxs-lookup"><span data-stu-id="d1405-173">Change work hours to an eight (8) hour work day, mark weekends as non-work days, and make sure time zone matches yours.</span></span> 
8. <span data-ttu-id="d1405-174">Wybierz **Zapisz i zamknij**.</span><span class="sxs-lookup"><span data-stu-id="d1405-174">Select **Save and close**.</span></span>

![Aktualizacja kalendarza](./media/13UpdateCalendar.png)

9. <span data-ttu-id="d1405-176">Wybierz kolejno pozycje **Ustawienia** > **Szablony kalendarza** i utwórz **Nowy**.</span><span class="sxs-lookup"><span data-stu-id="d1405-176">Go to **Settings** > **Calendar templates** and select **New**.</span></span>
 
 ![Szablony kalendarzy](./media/14CalendarTemplates.png)
 
 10. <span data-ttu-id="d1405-178">Wprowadź nazwę, zaznacz utworzony szablon zasobu, a następnie wybierz pozycję **Zapisz**.</span><span class="sxs-lookup"><span data-stu-id="d1405-178">Enter a name, select the template resource you created, and then select **Save**.</span></span> 
 
 ![Zapisz szablon kalendarza](./media/15SaveCalendarTemplate.png)
 
 11. <span data-ttu-id="d1405-180">Przejdź do obszaru **Parametry** i kliknij dwukrotnie rekord.</span><span class="sxs-lookup"><span data-stu-id="d1405-180">Go to **Parameters** and double-click the record.</span></span> 
 
 ![Parametry projektu](./media/16ProjectParameters.png)
 
12. <span data-ttu-id="d1405-182">Zaktualizuj następujące pola:</span><span class="sxs-lookup"><span data-stu-id="d1405-182">Update the following fields:</span></span>

 - <span data-ttu-id="d1405-183">**Domyślna firma**: USPM</span><span class="sxs-lookup"><span data-stu-id="d1405-183">**Default company**: USPM</span></span>
 - <span data-ttu-id="d1405-184">**Domyślna jednostka organizacyjna**: Contoso Robotics Global</span><span class="sxs-lookup"><span data-stu-id="d1405-184">**Default Organizational Unit**: Contoso Robotics Global</span></span>
 - <span data-ttu-id="d1405-185">**Częstotliwość fakturowania**: siódmy i ostatni dzień</span><span class="sxs-lookup"><span data-stu-id="d1405-185">**Invoice Frequency**: Seventh and Last day</span></span>
 - <span data-ttu-id="d1405-186">**Szablon godzin pracy**: Zmień na utworzony szablon.</span><span class="sxs-lookup"><span data-stu-id="d1405-186">**Work hour template**: Change to the template you created.</span></span>

13. <span data-ttu-id="d1405-187">Wybierz pozycję **Zapisz**.</span><span class="sxs-lookup"><span data-stu-id="d1405-187">Select **Save**.</span></span> 

![Zaktualizowane parametry projektu](./media/17UpdatedProjectParameters.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
