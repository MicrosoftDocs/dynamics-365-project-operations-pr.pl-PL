---
title: Skonfiguruj i zastosuj dane konfiguracyjne w usłudze Common Data Service
description: W tym temacie zamieszczono informacje dotyczące ustawienia i zastosowania danych konfiguracyjnych Project Operations.
author: sigitac
manager: Annbe
ms.date: 11/04/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 1651d3b3b85d3dc581bf61976fada249bafd6b7b
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5289832"
---
# <a name="set-up-and-apply-configuration-data-in-the-common-data-service"></a><span data-ttu-id="cfc74-103">Skonfiguruj i zastosuj dane konfiguracyjne w usłudze Common Data Service</span><span class="sxs-lookup"><span data-stu-id="cfc74-103">Set up and apply configuration data in the Common Data Service</span></span> 

<span data-ttu-id="cfc74-104">_**Zastosowane do:** Project Operations dla zasobów/scenariuszy nieopartych na zaopatrzeniu_</span><span class="sxs-lookup"><span data-stu-id="cfc74-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

## <a name="prerequisites"></a><span data-ttu-id="cfc74-105">Wymagania wstępne</span><span class="sxs-lookup"><span data-stu-id="cfc74-105">Prerequisites</span></span>

<span data-ttu-id="cfc74-106">Przed przystąpieniem do konfigurowania danych z Common Data Service (CDS) muszą spełnione następujące wymagania wstępne:</span><span class="sxs-lookup"><span data-stu-id="cfc74-106">Before you beging to configure data in the Common Data Service (CDS), the following prerequisites must be met:</span></span>

1.  <span data-ttu-id="cfc74-107">Udostępnij środowisko CDS i środowisko Dynamics 365 Finance na potrzeby Project Operations.</span><span class="sxs-lookup"><span data-stu-id="cfc74-107">Provision a CDS environment and a Dynamics 365 Finance environment for Project Operations.</span></span>
2.  <span data-ttu-id="cfc74-108">Informacje o osobach prawnych z Dynamics 365 Finance są udostępniane środowisku CDS.</span><span class="sxs-lookup"><span data-stu-id="cfc74-108">Legal entity information from Dynamics 365 Finance is shared to the CDS environment.</span></span> <span data-ttu-id="cfc74-109">Oznacza to, że **Firma** z CDS zawiera następujące rekordy firm:</span><span class="sxs-lookup"><span data-stu-id="cfc74-109">This means that the **Company** entity in CDS has the following company records:</span></span>
  - <span data-ttu-id="cfc74-110">THPM</span><span class="sxs-lookup"><span data-stu-id="cfc74-110">THPM</span></span>
  - <span data-ttu-id="cfc74-111">USPM</span><span class="sxs-lookup"><span data-stu-id="cfc74-111">USPM</span></span>
  - <span data-ttu-id="cfc74-112">GBPM</span><span class="sxs-lookup"><span data-stu-id="cfc74-112">GBPM</span></span>

## <a name="install-setup-and-configuration-data"></a><span data-ttu-id="cfc74-113">Zainstaluj konfigurację i dane konfiguracyjne</span><span class="sxs-lookup"><span data-stu-id="cfc74-113">Install setup and configuration data</span></span>

1. <span data-ttu-id="cfc74-114">Pobierz, odblokuj i rozpakuj [pakiet danych instalacyjnych i konfiguracyjnych](https://download.microsoft.com/download/1/3/4/1349369c-6209-42b7-b3b4-5be0e67cacd8/ProjOpsSampleSetupData-%20Integrated%20UR1.zip).</span><span class="sxs-lookup"><span data-stu-id="cfc74-114">Download, unblock, and unzip the [Setup and Configuration Data Package](https://download.microsoft.com/download/1/3/4/1349369c-6209-42b7-b3b4-5be0e67cacd8/ProjOpsSampleSetupData-%20Integrated%20UR1.zip).</span></span>
2. <span data-ttu-id="cfc74-115">Przejdź do wyodrębnionego folderu, a następnie uruchom plik wykonywalny *DataMigrationUtility*.</span><span class="sxs-lookup"><span data-stu-id="cfc74-115">Navigate to the unzipped folder and run the executable file, *DataMigrationUtility*.</span></span>
3. <span data-ttu-id="cfc74-116">Na stronie 1 Kreatora migracji konfiguracji Common Data Service (CMT) wybierz pozycję **Importuj dane**, a następnie wybierz pozycję **Kontynuuj**.</span><span class="sxs-lookup"><span data-stu-id="cfc74-116">On page 1 of the Common Data Service Configuration Migration (CMT) Wizard, select **Import Data** and then select **Continue**.</span></span>

![Migracja konfiguracji](./media/1ConfigurationMigration.png)

4. <span data-ttu-id="cfc74-118">Na stronie 2 kreatora CMT wybierz **Microsoft 365** jako **Typ wdrożenia**.</span><span class="sxs-lookup"><span data-stu-id="cfc74-118">On Page 2 of the CMT Wizard, select **Microsoft 365** as the **Deployment Type**.</span></span>
5. <span data-ttu-id="cfc74-119">Wybierz pola wyboru **Wyświetl listę dostępnych organizacji** i **Wyświetl zaawansowane**.</span><span class="sxs-lookup"><span data-stu-id="cfc74-119">Select the **Display a list of available organizations** and **Show Advanced** check boxes.</span></span>
6. <span data-ttu-id="cfc74-120">Wybierz region dzierżawy, wprowadź swoje poświadczenia, a następnie wybierz pozycję **Zaloguj**.</span><span class="sxs-lookup"><span data-stu-id="cfc74-120">Select the region of your tenant, enter your credentials, and select **Login**.</span></span>

![Konfiguracja logowania](./media/2ConfigurationSignin.png)

7. <span data-ttu-id="cfc74-122">Na stronie 3 z poziomu listy organizacji w dzierżawie wybierz nazwę organizacji, do której chcesz zaimportować dane demonstracyjne, a następnie wybierz pozycję **Zaloguj**.</span><span class="sxs-lookup"><span data-stu-id="cfc74-122">On page 3, from the list of organizations on the tenant, select the organization you want to import the demo data into and select **Login**.</span></span>
8. <span data-ttu-id="cfc74-123">Na stronie 4 wybierz plik zip *SampleSetupAndConfigData*, który znajduje się w rozpakowanym folderze.</span><span class="sxs-lookup"><span data-stu-id="cfc74-123">On page 4, select the zip file, *SampleSetupAndConfigData* from the unpacked folder.</span></span>

![Wybieranie pliku zip](./media/3ZipFile.png)

![Wybierz plik](./media/4SelectAFile.png)

9. <span data-ttu-id="cfc74-126">Po zaznaczeniu pliku zip wybierz pozycję **Importuj dane**.</span><span class="sxs-lookup"><span data-stu-id="cfc74-126">After the zip file is selected, select **Import Data**.</span></span>

![Importuj dane](./media/5ImportData.png)

10. <span data-ttu-id="cfc74-128">Importowanie potrwa około dwóch sekund, w zależności od szybkości sieci.</span><span class="sxs-lookup"><span data-stu-id="cfc74-128">Import will run for approximately two-ten minutes depending on your network speed.</span></span> <span data-ttu-id="cfc74-129">Po zakończeniu importu zakończ działanie kreatora CMT.</span><span class="sxs-lookup"><span data-stu-id="cfc74-129">After import completes, exit the CMT Wizard.</span></span> 
11. <span data-ttu-id="cfc74-130">Należy sprawdzić w ramach organizacji dane z następujących 19 encji:</span><span class="sxs-lookup"><span data-stu-id="cfc74-130">Check your organization for data in the following 19 entities:</span></span>

  - <span data-ttu-id="cfc74-131">Waluta</span><span class="sxs-lookup"><span data-stu-id="cfc74-131">Currency</span></span>
  - <span data-ttu-id="cfc74-132">Jednostka organizacyjna</span><span class="sxs-lookup"><span data-stu-id="cfc74-132">Organizational Unit</span></span>
  - <span data-ttu-id="cfc74-133">Kontakt biznesowy</span><span class="sxs-lookup"><span data-stu-id="cfc74-133">Contact</span></span>
  - <span data-ttu-id="cfc74-134">Grupa podatku</span><span class="sxs-lookup"><span data-stu-id="cfc74-134">Tax Group</span></span>
  - <span data-ttu-id="cfc74-135">Grupa klientów</span><span class="sxs-lookup"><span data-stu-id="cfc74-135">Customer Group</span></span>
  - <span data-ttu-id="cfc74-136">Jednostka</span><span class="sxs-lookup"><span data-stu-id="cfc74-136">Unit</span></span>
  - <span data-ttu-id="cfc74-137">Grupa jednostek</span><span class="sxs-lookup"><span data-stu-id="cfc74-137">Unit Group</span></span>
  - <span data-ttu-id="cfc74-138">Cennik</span><span class="sxs-lookup"><span data-stu-id="cfc74-138">Price List</span></span>
  - <span data-ttu-id="cfc74-139">Cennik parametrów projektu</span><span class="sxs-lookup"><span data-stu-id="cfc74-139">Project Parameter Price List</span></span>
  - <span data-ttu-id="cfc74-140">Częstotliwość faktur</span><span class="sxs-lookup"><span data-stu-id="cfc74-140">Invoice Frequency</span></span>
  - <span data-ttu-id="cfc74-141">Kategoria zasobów, które można zarezerwować</span><span class="sxs-lookup"><span data-stu-id="cfc74-141">Bookable Resource Category</span></span>
  - <span data-ttu-id="cfc74-142">Kategoria transakcji</span><span class="sxs-lookup"><span data-stu-id="cfc74-142">Transaction Category</span></span>
  - <span data-ttu-id="cfc74-143">Kategoria wydatków</span><span class="sxs-lookup"><span data-stu-id="cfc74-143">Expense Category</span></span>
  - <span data-ttu-id="cfc74-144">Cena roli</span><span class="sxs-lookup"><span data-stu-id="cfc74-144">Role Price</span></span>
  - <span data-ttu-id="cfc74-145">Cena kategorii transakcji</span><span class="sxs-lookup"><span data-stu-id="cfc74-145">Transaction Category Price</span></span>
  - <span data-ttu-id="cfc74-146">Charakterystyka</span><span class="sxs-lookup"><span data-stu-id="cfc74-146">Characteristic</span></span>
  - <span data-ttu-id="cfc74-147">Zasób, który można zarezerwować</span><span class="sxs-lookup"><span data-stu-id="cfc74-147">Bookable Resource</span></span>
  - <span data-ttu-id="cfc74-148">Skojarzenie kategorii zasobów, które można zarezerwować</span><span class="sxs-lookup"><span data-stu-id="cfc74-148">Bookable resource category Assn</span></span>
  - <span data-ttu-id="cfc74-149">Charakterystyka zasobu, który można zarezerwować</span><span class="sxs-lookup"><span data-stu-id="cfc74-149">Bookable Resource Characteristic</span></span>

![Zakończ importowanie](./media/6CompleteImport.png)

## <a name="update-project-operations-configurations"></a><span data-ttu-id="cfc74-151">Aktualizowanie konfiguracji Project Operations</span><span class="sxs-lookup"><span data-stu-id="cfc74-151">Update Project Operations configurations</span></span>

1. <span data-ttu-id="cfc74-152">Przejdź do środowiska CE.</span><span class="sxs-lookup"><span data-stu-id="cfc74-152">Navigate to the CE environment.</span></span> <span data-ttu-id="cfc74-153">Można je znaleźć otwierając [centrum administracyjne Power Platform](https://admin.powerplatform.microsoft.com/environments), wybierając środowisko i wybierając pozycję **Otwórz środowisko**.</span><span class="sxs-lookup"><span data-stu-id="cfc74-153">You can find it by opening the [Power Platform Admin Center](https://admin.powerplatform.microsoft.com/environments), selecting the environment, and then selecting **Open Environment**.</span></span> 

![Otwórz środowisko](./media/7OpenEnvironment.png)

2. <span data-ttu-id="cfc74-155">Przejdź do obszaru **Projekty** > **Zasoby** i wybierz opcję **Nowy**, aby utworzyć zasób zaksięgowany dla użytkownika.</span><span class="sxs-lookup"><span data-stu-id="cfc74-155">Go to **Projects** > **Resources** and then select **New** to create a bookable resource for your user.</span></span>

![Zasoby, które można zarezerwować](./media/8BookableResources.png)

3. <span data-ttu-id="cfc74-157">Na karcie **Ogólne** wybierz użytkownika administracyjnego.</span><span class="sxs-lookup"><span data-stu-id="cfc74-157">On the **General** tab, select your admin user.</span></span> <span data-ttu-id="cfc74-158">Sprawdź, czy strefa czasowa jest zgodna z strefą, w której się znajdujesz.</span><span class="sxs-lookup"><span data-stu-id="cfc74-158">Verify that the time zone matches the one you are in.</span></span> 

![Nowy zasób, który można zarezerwować](./media/9NewBookableResource.png)

4. <span data-ttu-id="cfc74-160">Na karcie **Planowanie**, w polu **Firma** wybierz firmę **USPM**, a następnie wybierz pozycję **Zapisz**.</span><span class="sxs-lookup"><span data-stu-id="cfc74-160">On the **Scheduling** tab, in the **Company** field, pick the **USPM** company, and then select **Save**.</span></span> 

![Karta planowania](./media/10SchedulingTab.png)

5. <span data-ttu-id="cfc74-162">Wybierz kartę **Godziny pracy**.</span><span class="sxs-lookup"><span data-stu-id="cfc74-162">Select the **Work hours** tab.</span></span>  

![Godziny pracy](./media/11WorkHours.png)

6. <span data-ttu-id="cfc74-164">Kliknij dwukrotnie dowolną wartość w kalendarzu i wybierz pozycję **Edytuj** > **Wszystkie zdarzenia z serii**.</span><span class="sxs-lookup"><span data-stu-id="cfc74-164">Double-click on any value in the calendar and select **Edit** > **All events in the series**.</span></span> 

![Kalendarz pracy](./media/12WorkCalendar.png)

7. <span data-ttu-id="cfc74-166">Zmień godziny pracy na osiem (8) godzin w trakcie dnia pracy i zaznacz weekendy jako dni wolne od pracy i upewnij się, że strefa czasowa odpowiada Twojej.</span><span class="sxs-lookup"><span data-stu-id="cfc74-166">Change work hours to an eight (8) hour work day, mark weekends as non-work days, and make sure time zone matches yours.</span></span> 
8. <span data-ttu-id="cfc74-167">Wybierz **Zapisz i zamknij**.</span><span class="sxs-lookup"><span data-stu-id="cfc74-167">Select **Save and close**.</span></span>

![Aktualizacja kalendarza](./media/13UpdateCalendar.png)

9. <span data-ttu-id="cfc74-169">Wybierz kolejno pozycje **Ustawienia** > **Szablony kalendarza** i utwórz **Nowy**.</span><span class="sxs-lookup"><span data-stu-id="cfc74-169">Go to **Settings** > **Calendar templates** and select **New**.</span></span>
 
 ![Szablony kalendarzy](./media/14CalendarTemplates.png)
 
 10. <span data-ttu-id="cfc74-171">Wprowadź nazwę, zaznacz utworzony szablon zasobu, a następnie wybierz pozycję **Zapisz**.</span><span class="sxs-lookup"><span data-stu-id="cfc74-171">Enter a name, select the template resource you created, and then select **Save**.</span></span> 
 
 ![Zapisz szablon kalendarza](./media/15SaveCalendarTemplate.png)
 
 11. <span data-ttu-id="cfc74-173">Przejdź do obszaru **Parametry** i kliknij dwukrotnie rekord.</span><span class="sxs-lookup"><span data-stu-id="cfc74-173">Go to **Parameters** and double-click the record.</span></span> 
 
 ![Parametry projektu](./media/16ProjectParameters.png)
 
12. <span data-ttu-id="cfc74-175">Zaktualizuj następujące pola:</span><span class="sxs-lookup"><span data-stu-id="cfc74-175">Update the following fields:</span></span>

 - <span data-ttu-id="cfc74-176">**Domyślna firma**: USPM</span><span class="sxs-lookup"><span data-stu-id="cfc74-176">**Default company**: USPM</span></span>
 - <span data-ttu-id="cfc74-177">**Domyślna jednostka organizacyjna**: Contoso Robotics Global</span><span class="sxs-lookup"><span data-stu-id="cfc74-177">**Default Organizational Unit**: Contoso Robotics Global</span></span>
 - <span data-ttu-id="cfc74-178">**Częstotliwość fakturowania**: siódmy i ostatni dzień</span><span class="sxs-lookup"><span data-stu-id="cfc74-178">**Invoice Frequency**: Seventh and Last day</span></span>
 - <span data-ttu-id="cfc74-179">**Szablon godzin pracy**: Zmień na utworzony szablon.</span><span class="sxs-lookup"><span data-stu-id="cfc74-179">**Work hour template**: Change to the template you created.</span></span>

13. <span data-ttu-id="cfc74-180">Wybierz pozycję **Zapisz**.</span><span class="sxs-lookup"><span data-stu-id="cfc74-180">Select **Save**.</span></span> 

![Zaktualizowane parametry projektu](./media/17UpdatedProjectParameters.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]