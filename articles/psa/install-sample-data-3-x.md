---
title: Instalacja przykładowych danych
description: W tym temacie zamieszczono informacje dotyczące instalowania danych przykładowych w programie Project Service Automation.
ms.custom: dyn365-projectservice
ms.date: 11/08/2018
ms.service: project-operations
ms.reviewer: kfend
ms.suite: ''
applies_to: Dynamics 365 Project Service Automation
author: ruhercul
ms.author: ruhercul
search.audienceType: IT Pro, Developer
search.app: ''
ms.openlocfilehash: 377e50fc5772c4dc146ccee098bf2806bbc8c6b7
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5275101"
---
# <a name="sample-data-installation-for-the-project-service-application"></a><span data-ttu-id="c597e-103">Instalowanie danych przykładowych dla aplikacji Project Service</span><span class="sxs-lookup"><span data-stu-id="c597e-103">Sample data installation for the Project Service application</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="c597e-104">W celu ułatwienia budowy własnych środowisk pokazowych, firma Microsoft dostarcza gotowe do pobrania pakiety danych przykładowych, które opisują możliwości aplikacji użytkownika.</span><span class="sxs-lookup"><span data-stu-id="c597e-104">To help you build your own demo environments, Microsoft provides downloadable sample data packages that showcase the capabilities of your apps.</span></span> <span data-ttu-id="c597e-105">Istnieją dwa typy pakietów danych przykładowych:</span><span class="sxs-lookup"><span data-stu-id="c597e-105">There are two types of sample data packages:</span></span>
- <span data-ttu-id="c597e-106">odwołanie/dane konfiguracji</span><span class="sxs-lookup"><span data-stu-id="c597e-106">reference/setup data</span></span>
- <span data-ttu-id="c597e-107">dane demonstracyjne (odwołanie/konfiguracja i dane transakcji, takie jak zlecenia pracy i projekty)</span><span class="sxs-lookup"><span data-stu-id="c597e-107">demo data (reference/setup and transactional data such as work orders and projects)</span></span>

<span data-ttu-id="c597e-108">Pakiety danych przykładowych **odwołanie** można pobrać w trzech osobnych pakietach, więc można zainstalować dane tylko dla Project Service lub tylko dla Field Service, lub można zainstalować przykładowe dane dla obu aplikacji jednocześnie.</span><span class="sxs-lookup"><span data-stu-id="c597e-108">The sample **reference** data packages are downloadable in three different packages, so you can install data only for Project Service, or only for Field Service, or you can install sample data for both applications at once.</span></span>

<span data-ttu-id="c597e-109">Pakiety danych przykładowych konfiguracja/odwołanie to:</span><span class="sxs-lookup"><span data-stu-id="c597e-109">The sample setup/reference data packages are:</span></span>

- [<span data-ttu-id="c597e-110">**V902PSMasterData** - Project Service, tylko wersja 3.x</span><span class="sxs-lookup"><span data-stu-id="c597e-110">**V902PSMasterData** - Project Service version 3.x only</span></span>](https://go.microsoft.com/fwlink/?linkid=2026540&clcid=0x409)

- [<span data-ttu-id="c597e-111">**V902FSMasterData** - Field Service, tylko wersja 8.x</span><span class="sxs-lookup"><span data-stu-id="c597e-111">**V902FSMasterData** - Field Service version 8.x only</span></span>](https://go.microsoft.com/fwlink/?linkid=2026536&clcid=0x409)

- [<span data-ttu-id="c597e-112">**V902FPSMasterData** — Field Service 8.x i Project Service 3.x</span><span class="sxs-lookup"><span data-stu-id="c597e-112">**V902FPSMasterData** - Field Service 8.x and Project Service 3.x</span></span>](https://go.microsoft.com/fwlink/?linkid=2026041&clcid=0x409)

<span data-ttu-id="c597e-113">Najnowszy pakiet danych **demo** to:</span><span class="sxs-lookup"><span data-stu-id="c597e-113">The latest **demo** data package is:</span></span>

 - [<span data-ttu-id="c597e-114">**FPSDemoData** - Field Service 8.x and Project Service 3.x</span><span class="sxs-lookup"><span data-stu-id="c597e-114">**FPSDemoData** - Field Service 8.x and Project Service 3.x</span></span>](https://aka.ms/fpsdemodatapackage)

   <span data-ttu-id="c597e-115">Instrukcje dotyczące instalacji różnią się nieco w użytkownikach do tworzenia i konfigurowania sekcji, ale reszta jest taka sama, jak w poprzednim [**wpisie na blogu**](https://aka.ms/fpsdemodatablog).</span><span class="sxs-lookup"><span data-stu-id="c597e-115">Installation instructions differ slightly in the users to create and configure section but the rest is the same as in the previous [**blog post**](https://aka.ms/fpsdemodatablog).</span></span> <span data-ttu-id="c597e-116">Ten pakiet zawiera mniejszy zestaw danych demonstracyjnych, a cała operacja instalacji trwa około 3 godzin.</span><span class="sxs-lookup"><span data-stu-id="c597e-116">This package features a reduced demo data set and takes approximately 3 hours to install.</span></span>

<span data-ttu-id="c597e-117">Te pakiety danych przykładowych są dostępne tylko w języku angielskim.</span><span class="sxs-lookup"><span data-stu-id="c597e-117">These sample data packages are available in English only.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c597e-118">**Nie można odinstalować danych przykładowych.**</span><span class="sxs-lookup"><span data-stu-id="c597e-118">**There is no way to uninstall the sample data.**</span></span> <span data-ttu-id="c597e-119">Pakiet te należy instalować wyłącznie w systemach demonstracyjnych, szkoleniowych lub testowych.</span><span class="sxs-lookup"><span data-stu-id="c597e-119">You should only install these packages on demonstration, evaluation, training, or test systems.</span></span> <span data-ttu-id="c597e-120">Należy również zauważyć, że zainstalowanie dowolnego pakietu, a następnie instalowanie innego pakietu nie jest obsługiwane.</span><span class="sxs-lookup"><span data-stu-id="c597e-120">Also note that installing an individual package, and then installing the other individual package, is not supported.</span></span> <span data-ttu-id="c597e-121">(Innymi słowy, nie można zainstalować **FSMasterData** a następnie **PSMasterData**, i na odwrót.) Jeśli pojawi konieczność posiadania przykładowych danych dla obu aplikacji w dowolnym czasie w przyszłości, należy zainstalować pakiet **v902FPSMasterData**.</span><span class="sxs-lookup"><span data-stu-id="c597e-121">(In other words, you can't install **FSMasterData** followed by **PSMasterData**, or vice versa.) If you see yourself needing sample data for both applications at any point in the future, you should install the **v902FPSMasterData** package.</span></span>

<span data-ttu-id="c597e-122">Podczas instalowania pakietów danych przykładowych proces instalowania wykonuje następujące operacje:</span><span class="sxs-lookup"><span data-stu-id="c597e-122">When you install any of the sample data packages, the installation process performs the following actions:</span></span>

- <span data-ttu-id="c597e-123">Tworzy lub ustawia domyślne parametry dla Project Service, Field Service lub obu aplikacji (jeśli ma to zastosowanie).</span><span class="sxs-lookup"><span data-stu-id="c597e-123">Creates or sets default parameters for using Project Service, Field Service, or both applications (if applicable).</span></span>

- <span data-ttu-id="c597e-124">Importuje przykładowe dane dla aplikacji, takie jak zasoby, które można zarezerwować, role charakterystyczne dla poszczególnych aplikacji, sprzedaży i cenniki, jednostki organizacyjne, rekordy procesu sprzedaży i inne encje, aby zeprezentować kluczowe funkcje.</span><span class="sxs-lookup"><span data-stu-id="c597e-124">Imports sample data for the applications, such as bookable resources, application-specific roles, sales and cost price lists, organizational units, sales process records, and other entities to demonstrate key capabilities.</span></span>  

<span data-ttu-id="c597e-125">Wraz z pakietem **dane demonstracyjne** otrzymujesz powyższe i dodatkowe dane dotyczące transakcji, takich jak zlecenia pracy i projekty.</span><span class="sxs-lookup"><span data-stu-id="c597e-125">With the **demo data** package, you get the above and additional transactional data such as work orders and projects.</span></span>

<span data-ttu-id="c597e-126">Zastanawiasz się, jakie możliwości można zaprezentować przy użyciu przykładowych danych?</span><span class="sxs-lookup"><span data-stu-id="c597e-126">Wondering what capabilities you can demo with the sample data?</span></span> <span data-ttu-id="c597e-127">Zobacz fikcyjny scenariusz Fabrikam Robotics w [Uwagi techniczne](#technical-notes).</span><span class="sxs-lookup"><span data-stu-id="c597e-127">See the Fabrikam Robotics fictitious scenario in [Technical notes](#technical-notes).</span></span>

<span data-ttu-id="c597e-128">Jeśli masz pytania dotyczące instalowania tych przykładowych pakietów danych [wyśij do nas wiadomość e-mail na adres fpsdemodata@microsoft.com](mailto:fpsdemodata@microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="c597e-128">If you have questions about installing these sample data packages, [send us an email at fpsdemodata@microsoft.com](mailto:fpsdemodata@microsoft.com).</span></span>

## <a name="requirements"></a><span data-ttu-id="c597e-129">Wymagania</span><span class="sxs-lookup"><span data-stu-id="c597e-129">Requirements</span></span>

<span data-ttu-id="c597e-130">Protokół instalacji przyjmuje następujące informacje o wystąpieniu programu docelowego (organizacji):</span><span class="sxs-lookup"><span data-stu-id="c597e-130">The installation protocol assumes the following about your target instance (org):</span></span>

- <span data-ttu-id="c597e-131">Język podstawowy to angielski a waluta podstawowa to Dolar Amerykański (USD, $)</span><span class="sxs-lookup"><span data-stu-id="c597e-131">Base language is English and base currency is US dollar (USD,$).</span></span>

- <span data-ttu-id="c597e-132">Organizacja nie ma już danych Project Service lub Field Service, lub ma tylko standardowe dane domyśle, które posiadają wszystkie nowe organizacje.</span><span class="sxs-lookup"><span data-stu-id="c597e-132">The org has no Project Service or Field Service data already, or only has barebones default data that comes with any new org.</span></span>

- <span data-ttu-id="c597e-133">Właściwa wersję aplikacji biznesowej jest już zainstalowana:</span><span class="sxs-lookup"><span data-stu-id="c597e-133">The correct version of the business application is already installed:</span></span>
       
    - <span data-ttu-id="c597e-134">**Dla FPSDemoData or v902FPSMasterData:** Organizacja ma zainstalowaną wersję Field Service 8.x i Project Service 3.x.</span><span class="sxs-lookup"><span data-stu-id="c597e-134">**For FPSDemoData or v902FPSMasterData:** The org has Field Service version 8.x and Project Service version 3.x installed.</span></span>

    - <span data-ttu-id="c597e-135">**Dla v902PSMasterData:** Organizacja ma zainstalowaną wersję Project Service 3.x.</span><span class="sxs-lookup"><span data-stu-id="c597e-135">**For v902PSMasterData:** The org has Project Service version 3.x installed.</span></span>

    - <span data-ttu-id="c597e-136">**For v902FSMasterData:** Organizacja ma zainstalowaną wersję Field Service 8.x.</span><span class="sxs-lookup"><span data-stu-id="c597e-136">**For v902FSMasterData:** The org has Field Service version 8.x installed.</span></span>

> [!NOTE]
> <span data-ttu-id="c597e-137">Jeśli zachodzi konieczność zainstalowania przykładowych danych na istniejącym środowisku próbnym lub demonstracyjnym Project Service i Field Service które zawiera już dane (niezalecane), trzeba będzie zawiesić wstępne kontrole bezpieczeństwa wykonywane przez Instalatora.</span><span class="sxs-lookup"><span data-stu-id="c597e-137">If you need to install the sample data on top of an existing Project Service and Field Service trial or demo environment that already has data (not recommended), you'll need to suspend the safety prechecks performed by the installer.</span></span> <span data-ttu-id="c597e-138">Aby uzyskać więcej informacji, zobacz Uwagi techniczne poniżej.</span><span class="sxs-lookup"><span data-stu-id="c597e-138">For more information, see the technical notes below.</span></span>

## <a name="prepare-for-installation"></a><span data-ttu-id="c597e-139">Przygotuj do instalacji</span><span class="sxs-lookup"><span data-stu-id="c597e-139">Prepare for installation</span></span>

<span data-ttu-id="c597e-140">Musisz uruchomić program instalacyjny na komputerze z najnowszą wersją systemu Windows (preferowany Windows 10).</span><span class="sxs-lookup"><span data-stu-id="c597e-140">You need to run the installer on a computer with a recent version of Windows (Windows 10 preferred).</span></span>

<span data-ttu-id="c597e-141">Należy zaplanować, że komputer będzie podłączony do sieci a instalacja będzie trwała maksymalnie **1 godzinę** dla **dane konfiguracja/odwołanie**.</span><span class="sxs-lookup"><span data-stu-id="c597e-141">You should plan for the computer to remain connected to a network, and for the installation to run for up to **1 hour** for **setup/reference data**.</span></span> <span data-ttu-id="c597e-142">(Zwykle instalacja trwa około 30 minut dla **FPSMasterData**, co obejmuje dane przykładowe dla obu aplikacji.) Dla **FPSDemoData**, instalacja potrwa około **3 godzin**.</span><span class="sxs-lookup"><span data-stu-id="c597e-142">(Normally the installation takes around 30 minutes for **FPSMasterData**, which includes sample data for both applications.) For the **FPSDemoData**, the installation will take around **3 hours**.</span></span>

<span data-ttu-id="c597e-143">Komputer powinien mieć wyłączoną funkcję wygaszacza ekranu.</span><span class="sxs-lookup"><span data-stu-id="c597e-143">The computer should have the screen saver function turned off.</span></span> <span data-ttu-id="c597e-144">W przeciwnym razie poświadczenia sesji podczas instalacji mogą zostać utracone po uruchomieniu wygaszacza ekranu (chyba że zachowasz przez cały czas aktywną sesję).</span><span class="sxs-lookup"><span data-stu-id="c597e-144">Otherwise, session credentials for the installation may be lost when the screen saver engages (unless you keep your session active throughout).</span></span>

> [!div class="mx-imgBorder"]
> <span data-ttu-id="c597e-145">![Zrzut ekranu przedstawiający ustawienia wygaszacza ekranu, z wygaszaczem ekranu wyłączonym](media/sample-data-1.png)</span><span class="sxs-lookup"><span data-stu-id="c597e-145">![Screenshot of screen saver settings, with screen saver turned off](media/sample-data-1.png)</span></span>

## <a name="download-and-unpack"></a><span data-ttu-id="c597e-146">Pobierz i rozpakuj</span><span class="sxs-lookup"><span data-stu-id="c597e-146">Download and unpack</span></span>

<span data-ttu-id="c597e-147">Instalator danych przykładowych Project Service i Field Service jest dystrybuowany jako samowyodrębniający się plik wykonywalny.</span><span class="sxs-lookup"><span data-stu-id="c597e-147">The Project Service and Field Service sample data installer is distributed as a self-extracting executable.</span></span> <span data-ttu-id="c597e-148">Nazwy plików mogą się różnić w zależności od pakietu danych przykładowych, ale kroki są takie same, bez względu na to, jaki pakiet instalujesz.</span><span class="sxs-lookup"><span data-stu-id="c597e-148">The file names may vary depending on the sample data package, but otherwise the steps are the same no matter which package you install.</span></span>

<span data-ttu-id="c597e-149">Po pobraniu pakietu, uruchom plik .exe, a następnie zaakceptuj warunki, aby rozpakować skompresowany plik zip.</span><span class="sxs-lookup"><span data-stu-id="c597e-149">After downloading a package, run the .exe file, and then accept terms and conditions to unpack the compressed zip file.</span></span> <span data-ttu-id="c597e-150">Następnie musisz wyodrębnić zawartość pliku do folderu na komputerze.</span><span class="sxs-lookup"><span data-stu-id="c597e-150">You then need to extract contents of that file to a folder on the computer.</span></span>

<span data-ttu-id="c597e-151">W zależności od systemu operacyjnego i ustawień zabezpieczeń po rozpakowanie pliku zip może być konieczne wykonanie następujących czynności:</span><span class="sxs-lookup"><span data-stu-id="c597e-151">Depending on the operating system and security settings, you may need to perform the following steps after unpacking the zip file:</span></span>

1. <span data-ttu-id="c597e-152">Znajdź i kliknij prawym przyciskiem myszy plik **FPSDemoData.dll** w folderze **v902FPSMasterData** / **PackageDeployer_FPSDemoData**.</span><span class="sxs-lookup"><span data-stu-id="c597e-152">Find and right-click the **FPSDemoData.dll** file in the **v902FPSMasterData** / **PackageDeployer_FPSDemoData** folder.</span></span>

2. <span data-ttu-id="c597e-153">Wybierz **Odblokuj**.</span><span class="sxs-lookup"><span data-stu-id="c597e-153">Choose **Unblock**.</span></span>

3. <span data-ttu-id="c597e-154">Wybierz **Zastosuj**.</span><span class="sxs-lookup"><span data-stu-id="c597e-154">Select **Apply**.</span></span>

4. <span data-ttu-id="c597e-155">Wybierz pozycję **OK**.</span><span class="sxs-lookup"><span data-stu-id="c597e-155">Select **OK**.</span></span>


## <a name="create-or-configure-users"></a><span data-ttu-id="c597e-156">Tworzenie i konfigurowanie użytkowników</span><span class="sxs-lookup"><span data-stu-id="c597e-156">Create or configure users</span></span>

<span data-ttu-id="c597e-157">Pakiet **FPSDemoData** wymaga sześciu użytkowników, a pakiet **FPSMasterData** wymaga jednego użytkownika.</span><span class="sxs-lookup"><span data-stu-id="c597e-157">The **FPSDemoData** package requires six users while **FPSMasterData** packages require one user.</span></span> <span data-ttu-id="c597e-158">Zwróć się so właściwego po pakiet danych przykładowych.</span><span class="sxs-lookup"><span data-stu-id="c597e-158">Refer to the correct one for your sample data package.</span></span>

## <a name="create-or-configure-users---setupreference-data-packages"></a><span data-ttu-id="c597e-159">Tworzenie lub konfigurowanie użytkowników — / pakiety danych konfiguracja/odwołanie</span><span class="sxs-lookup"><span data-stu-id="c597e-159">Create or configure users - setup/reference data packages</span></span>

<span data-ttu-id="c597e-160">Pakiet **FPSMasterData** jest przeznaczony do zainstalowania z jednym użytkownikiem nazywającym się Spencer Low z ustawieniami opisanymi w tym miejscu.</span><span class="sxs-lookup"><span data-stu-id="c597e-160">The **FPSMasterData** package is designed to install with one user named Spencer Low with the settings described here.</span></span> <span data-ttu-id="c597e-161">Aby poprawnie zainstalować pakiet, użytkownik musi utworzyć (lub tymczasowo zmienić) użytkowników w swoim środowisku, aby odpowiadali oni nadchodzącej konfiguracji danych przykładowych.</span><span class="sxs-lookup"><span data-stu-id="c597e-161">To install the package correctly, you need to create (or temporarily rename) users in your environment to match the incoming sample data configuration.</span></span>

<span data-ttu-id="c597e-162">Aby utworzyć lub skonfigurować użytkowników, przejdź do **Ustawienia** > **Zabezpieczenia** > **Użytkownicy**, i wykonaj następujące czynności:</span><span class="sxs-lookup"><span data-stu-id="c597e-162">To create or configure users, go to **Settings** > **Security** > **Users**, and do the following:</span></span>

1. <span data-ttu-id="c597e-163">Ustaw UserFullname = "Spencer Low" z nazwą użytkownika "spencerl" (**lowercase**) dla ról Menedżer projektu i Menedżer praktyk.</span><span class="sxs-lookup"><span data-stu-id="c597e-163">Set UserFullname="Spencer Low" with username "spencerl" (**lowercase**) to the Project Manager and Practice Manager roles.</span></span>

2. <span data-ttu-id="c597e-164">Wybierz użytkownika **Spencer Low**, a następnie wybierz **Zarządzaj rolami**.</span><span class="sxs-lookup"><span data-stu-id="c597e-164">Select the **Spencer Low** user, and then select **Manage Roles**.</span></span> <span data-ttu-id="c597e-165">Znajdź i wybierz rolę **Administrator systemu**, a następnie wybierz **OK**, aby udzielić pełnych praw administratora dla użytkownika Spencer Low.</span><span class="sxs-lookup"><span data-stu-id="c597e-165">Find and select the **System Administrator** role, and then select **OK** to grant full admin rights to Spencer Low.</span></span> <span data-ttu-id="c597e-166">Ten krok jest niezbędny w celu zapewnienia, że przykładowe rekordy są tworzone z własnością odpowiednich użytkowników co gwarantuje poprawne wypełnianie widoków.</span><span class="sxs-lookup"><span data-stu-id="c597e-166">This step is necessary to ensure that sample records are created with the correct user ownership and therefore populate views correctly.</span></span>

3. <span data-ttu-id="c597e-167">Z pobranego pakietu musisz zaktualizować plik mapowania danych z adresami e-mail domyślnego kontekstu użytkownika.</span><span class="sxs-lookup"><span data-stu-id="c597e-167">From the downloaded package, you need to update a data mapping file with email addresses of the default user context.</span></span> <span data-ttu-id="c597e-168">Aby to zrobić otwórz **PkgFolder**, następnie znajdź i otwórz plik **ImportUserMapFile.xml** w Notatniku (lub Visual Studio lub innym edytorze XML).</span><span class="sxs-lookup"><span data-stu-id="c597e-168">To do this, open **PkgFolder**, and then find and open the **ImportUserMapFile.xml** file in Notepad (or Visual Studio or another XML editor).</span></span> <span data-ttu-id="c597e-169">Ustaw pole **DefaultUserToMapTo =** na adres e-mail użytkownika Spencer Low.</span><span class="sxs-lookup"><span data-stu-id="c597e-169">Set the **DefaultUserToMapTo=** field to the email address of the Spencer Low user.</span></span>

4. <span data-ttu-id="c597e-170">Jeśli nie używasz Spencer Low z nazwą użytkownika **spencerl**, musisz zaktualizować dodatkowy plik.</span><span class="sxs-lookup"><span data-stu-id="c597e-170">If you aren't using Spencer Low with username **spencerl**, you need to update an additional file.</span></span> <span data-ttu-id="c597e-171">Otwórz plik **DemoDataPreImportConfig.xml**, a następnie znajdź tag **userstocreateandconfigure**.</span><span class="sxs-lookup"><span data-stu-id="c597e-171">Open the **DemoDataPreImportConfig.xml** file, and then find the **userstocreateandconfigure** tag.</span></span> <span data-ttu-id="c597e-172">Zaktualizuj tag **\<login\>** nazwą użytkownika swojego użytkownika Ludwik Kamiński.</span><span class="sxs-lookup"><span data-stu-id="c597e-172">Update the **\<login\>** tag with the username of your Spencer Low user.</span></span> <span data-ttu-id="c597e-173">Aby uzyskać dodatkowe informacje, zobacz [Uwagi techniczne](#technical-notes).</span><span class="sxs-lookup"><span data-stu-id="c597e-173">For additional details, see [Technical notes](#technical-notes).</span></span>

## <a name="create-or-configure-users---demo-data-package"></a><span data-ttu-id="c597e-174">Tworzenie i konfigurowanie użytkowników - pakiet danych demonstracyjnych</span><span class="sxs-lookup"><span data-stu-id="c597e-174">Create or configure users - demo data package</span></span>

<span data-ttu-id="c597e-175">Pakiet danych demonstracyjnych wymaga sześciu użytkowników.</span><span class="sxs-lookup"><span data-stu-id="c597e-175">The demo data package requires six users.</span></span> <span data-ttu-id="c597e-176">Aby pakiet został prawidłowo zainstalowany wykonaj następujące czynności:</span><span class="sxs-lookup"><span data-stu-id="c597e-176">For the package to install correctly, do the following:</span></span>

 1. <span data-ttu-id="c597e-177">Tworzenie i tymczasowa zmiana nazw istniejących użytkowników, aby odpowiadały przychodzącym przykładowym danym konfiguracji, przez przechodzenie do **Ustawienia** > **Zabezpieczenia** > **Użytkownicy**.</span><span class="sxs-lookup"><span data-stu-id="c597e-177">Create or temporarily rename existing users to match incoming sample data configuration by going to **Settings** > **Security** > **Users**.</span></span>
 
    <span data-ttu-id="c597e-178">Te role są potrzebne tylko dla prezentacji bazujących na osobach.</span><span class="sxs-lookup"><span data-stu-id="c597e-178">These roles are only needed for persona-based demos.</span></span>  
    - <span data-ttu-id="c597e-179">Imię i nazwisko użytkownika = "David So" jako Technik usługi Field Service</span><span class="sxs-lookup"><span data-stu-id="c597e-179">User Fullname="David So" as Field Service Technician</span></span>   
    - <span data-ttu-id="c597e-180">Imię i nazwisko użytkownika = "Jamie Reding" jako Dyspozytor usługi Field Service i Customer Sevice</span><span class="sxs-lookup"><span data-stu-id="c597e-180">User Fullname="Jamie Reding" as Customer Service & Field Service Dispatcher</span></span>   
    - <span data-ttu-id="c597e-181">Imię i nazwisko użytkownika = "Molly Clark" jako Menedżer kont</span><span class="sxs-lookup"><span data-stu-id="c597e-181">User Fullname="Molly Clark" as Account Manager</span></span>   
    - <span data-ttu-id="c597e-182">Imię i nazwisko użytkownika = "Spencer Low" jako Menedżer praktyk oraz Menedżer projektu</span><span class="sxs-lookup"><span data-stu-id="c597e-182">User Fullname="Spencer Low" as Practice and Project Manager</span></span>  
    - <span data-ttu-id="c597e-183">Imię i nazwisko użytkownika = "Veronica Quek" jako Członek zespołu</span><span class="sxs-lookup"><span data-stu-id="c597e-183">User Fullname="Veronica Quek" as Team Member</span></span>   
    - <span data-ttu-id="c597e-184">Imię i nazwisko użytkownika = "William Contoso"</span><span class="sxs-lookup"><span data-stu-id="c597e-184">User Fullname="William Contoso"</span></span>
  
2. <span data-ttu-id="c597e-185">Do potrzeb importu danych demonstracyjnych przypisz sześciu użytkowników powyżej roli Administratora, aby przykładowe rekordy zostały zaimportowane poprawnie.</span><span class="sxs-lookup"><span data-stu-id="c597e-185">For the purposes of demo data import, assign the six users above the Administrator role so sample records import correctly.</span></span> 

3. <span data-ttu-id="c597e-186">Otwórz **PkgFolder** i znajdź i otwórz **ImportUserMapFile.xml**.</span><span class="sxs-lookup"><span data-stu-id="c597e-186">Open **PkgFolder** and then find and open **ImportUserMapFile.xml**.</span></span> <span data-ttu-id="c597e-187">Zaktualizuj pola **Nowy=** do adresów e-mail odpowiednich użytkowników w systemie.</span><span class="sxs-lookup"><span data-stu-id="c597e-187">Update the **New=** fields to the email addresses of corresponding Users in your system.</span></span>

   > [!div class="mx-imgBorder"]
   > <span data-ttu-id="c597e-188">![Zrzut ekranu UserMapFile](media/sample-data-7.png)</span><span class="sxs-lookup"><span data-stu-id="c597e-188">![Screen shot of UserMapFile](media/sample-data-7.png)</span></span>

4. <span data-ttu-id="c597e-189">Jeśli użytkownik "Spencer Low" ma Identyfikator użytkownika inny niż **"spencerl"**, musisz zaktualizować dodatkowy plik.</span><span class="sxs-lookup"><span data-stu-id="c597e-189">If your "Spencer Low" full name user has a different user ID than **"spencerl"**, then you need to update an additional file.</span></span> <span data-ttu-id="c597e-190">Otwórz **DemoDataPreImportConfig.xml**, a następnie znajdź znacznik **userstocreateandconfigure**.</span><span class="sxs-lookup"><span data-stu-id="c597e-190">Open **DemoDataPreImportConfig.xml** and find the **userstocreateandconfigure** tag.</span></span> <span data-ttu-id="c597e-191">Zaktualizuj znacznik **\<login\>** za pomocą loginId (wielkość liter jest uwzględniana).</span><span class="sxs-lookup"><span data-stu-id="c597e-191">Update the **\<login\>** tag with the loginId (case-sensitive).</span></span> 

5. <span data-ttu-id="c597e-192">Kalendarz pierwszego użytkownika (w znaczniku **userstocreateandconfigure**) jest używany do wypełnienia godzin pracy dla wszystkich zasobów, które można zarezerwować przy importowaniu danych demonstracyjnych.</span><span class="sxs-lookup"><span data-stu-id="c597e-192">The first user's calendar (in the **userstocreateandconfigure** tag) is used to populate the work hours for all bookable resources on import of demo data.</span></span> <span data-ttu-id="c597e-193">Przejdź do **Ustawienia** > **Zabezpieczenia** > **Użytkownicy**, znajdź użytkownika "Spencer Low" i otwórz opcję "Godziny pracy".</span><span class="sxs-lookup"><span data-stu-id="c597e-193">Navigate to **Settings** > **Security** > **Users**, find your "Spencer Low" user, and open the "Work Hours" option.</span></span> <span data-ttu-id="c597e-194">Edytuj istniejące godziny pracy, wybierając opcję **Cały cykliczny harmonogram tygodniowy - od początku do końca**.</span><span class="sxs-lookup"><span data-stu-id="c597e-194">Edit the existing work hours, selecting the **Entire recurring weekly schedule from start to end** option.</span></span> <span data-ttu-id="c597e-195">Zapewnij **Godziny pracy są ustawione na 8:00 - 17:00 (9 godzin), od poniedziałku do piątku dla strefy czasowej ustawionej na czas pacyficzny (Stany Zjednoczone i Kanada)**.</span><span class="sxs-lookup"><span data-stu-id="c597e-195">Ensure the **Work hours are set to 8 AM - 5 PM (9 Hours), Monday to Friday and with the Timezone set to Pacific Time (US & Canada)**.</span></span> <span data-ttu-id="c597e-196">Jest to niezbędne do zapewnienia, że tablice Projekt i Harmonogram prezentują dane zgodne z oczekiwaniami.</span><span class="sxs-lookup"><span data-stu-id="c597e-196">This is needed to ensure that the Project and Schedule board show as expected.</span></span>

<span data-ttu-id="c597e-197">**Rekomendacja:** Rozważ utworzenie kopii zapasowej organizacji teraz, na wypadek wystąpienia konieczność powrotu do punktu początkowego, jeśli wystąpią problemy podczas na instalowania danych przykładowych.</span><span class="sxs-lookup"><span data-stu-id="c597e-197">**Recommendation:** Consider creating a backup of your org now, in case you need to revert to your starting point if something goes wrong during the sample data installation.</span></span> <span data-ttu-id="c597e-198">Aby uzyskać więcej informacji, zobacz [Kopia zapasowa i przywracanie wystąpień](https://docs.microsoft.com/dynamics365/customer-engagement/admin/backup-restore-instances).</span><span class="sxs-lookup"><span data-stu-id="c597e-198">For more information, see [Backup and restore instances](https://docs.microsoft.com/dynamics365/customer-engagement/admin/backup-restore-instances).</span></span>

## <a name="run-the-package-deployer"></a><span data-ttu-id="c597e-199">Uruchom Package Deployer</span><span class="sxs-lookup"><span data-stu-id="c597e-199">Run the Package Deployer</span></span>

1. <span data-ttu-id="c597e-200">Znajdź i uruchom **PackageDeployer.exe** w folderze **v902FPSMasterData** LUB **PackageDeployer_FPSDemoData**.</span><span class="sxs-lookup"><span data-stu-id="c597e-200">Find and run **PackageDeployer.exe** in the **v902FPSMasterData** OR **PackageDeployer_FPSDemoData** folder.</span></span>

2. <span data-ttu-id="c597e-201">Zaakceptuj postanowienia.</span><span class="sxs-lookup"><span data-stu-id="c597e-201">Accept the terms and conditions.</span></span>

3. <span data-ttu-id="c597e-202">W następnym oknie:</span><span class="sxs-lookup"><span data-stu-id="c597e-202">On the next window:</span></span>

   <span data-ttu-id="c597e-203">a.</span><span class="sxs-lookup"><span data-stu-id="c597e-203">a.</span></span> <span data-ttu-id="c597e-204">Wybierz typ wdrożenia **Office 365**.</span><span class="sxs-lookup"><span data-stu-id="c597e-204">Select deployment type **Office 365**.</span></span>

   <span data-ttu-id="c597e-205">b.</span><span class="sxs-lookup"><span data-stu-id="c597e-205">b.</span></span> <span data-ttu-id="c597e-206">Użyj użytkownika i hasła użytkownika administrator systemu skonfigurowanego w "Tworzenie i konfigurowanie użytkowników" ("Spencer Low" z nazwą użytkownika "spencerl").</span><span class="sxs-lookup"><span data-stu-id="c597e-206">Use the user and password of the system administrator user configured in "Create or configure users" ("Spencer Low" with "spencerl" username).</span></span>

   <span data-ttu-id="c597e-207">c.</span><span class="sxs-lookup"><span data-stu-id="c597e-207">c.</span></span> <span data-ttu-id="c597e-208">Upewnij się, że zaznaczono **Wyświetl listę dostępnych organizacji**.</span><span class="sxs-lookup"><span data-stu-id="c597e-208">Make sure **Display list of available organizations** is selected.</span></span>

      > [!div class="mx-imgBorder"]
      > <span data-ttu-id="c597e-209">![Zrzut ekranu przedstawiający okno Package Deployer z zaznaczonym „Wyświetl listę dostępnych organizacji”](media/sample-data-2.png)</span><span class="sxs-lookup"><span data-stu-id="c597e-209">![Screenshot of Package Deployer window with "Display list of available organizations" selected](media/sample-data-2.png)</span></span>

4. <span data-ttu-id="c597e-210">Wybierz organizację, w której chcesz zainstalować przykładowe dane.</span><span class="sxs-lookup"><span data-stu-id="c597e-210">Select the organization where you want to install the sample data.</span></span>

5. <span data-ttu-id="c597e-211">Wybierz **Dalej** aż pojawi się dialog **Instalator danych pokazowych**.</span><span class="sxs-lookup"><span data-stu-id="c597e-211">Select **Next** until you see the **Demo Data Setup** dialog.</span></span>

   > [!div class="mx-imgBorder"]
   > <span data-ttu-id="c597e-212">![Zrzut ekranu przedstawiający okno statusu Instalatora danych przykładowych](media/sample-data-3.png)</span><span class="sxs-lookup"><span data-stu-id="c597e-212">![Screenshot of the demo data installer status window](media/sample-data-3.png)</span></span>

6. <span data-ttu-id="c597e-213">Zanim przejdziesz dalej, pamiętaj, że instalowanie danych przykładowych może trwać maksymalnie godzinę (zwykle ~ 10 min).</span><span class="sxs-lookup"><span data-stu-id="c597e-213">Before proceeding, note that installing sample data could take up to one hour (normally ~10 minutes).</span></span> <span data-ttu-id="c597e-214">Należy się upewnić, że komputer pozostaje włączony i podłączony do sieci w trakcie procesu instalowania, i że sesja pozostaje aktywna.</span><span class="sxs-lookup"><span data-stu-id="c597e-214">You'll need to make sure the computer remains on and connected to a network throughout the installation process, and that your session remains active.</span></span>   

7. <span data-ttu-id="c597e-215">Kiedy jesteś gotowy, kliknij **Dalej**, aby rozpocząć proces instalacji przykładowych danych.</span><span class="sxs-lookup"><span data-stu-id="c597e-215">When you're ready, click **Next** to start the sample data installation process.</span></span> <span data-ttu-id="c597e-216">Po załadowaniu przykładowych danych, kliknij **Zakończ**.</span><span class="sxs-lookup"><span data-stu-id="c597e-216">After the sample data is loaded, click **Finish**.</span></span>

## <a name="verify-the-sample-data-installation"></a><span data-ttu-id="c597e-217">Zweryfikuj prawidłowość instalacji danych przykładowych</span><span class="sxs-lookup"><span data-stu-id="c597e-217">Verify the sample data installation</span></span>

<span data-ttu-id="c597e-218">Sprawdzając upewnij się, że liczba rekordów i typy encji wymienione w scenariuszu fikcyjnym Fabrikam Robotics wydają się być zgodne z oczekiwaniami.</span><span class="sxs-lookup"><span data-stu-id="c597e-218">For a sanity check, verify that the number of records and types of entities listed in Fabrikam Robotics fictitious scenario appear as expected.</span></span>

<span data-ttu-id="c597e-219">Po całkowitym pobraniu danych przykładowych zaloguj się jako użytkownik Spencer Low i potwierdzić następujące informacje:</span><span class="sxs-lookup"><span data-stu-id="c597e-219">After the sample data completely loads, sign in as the Spencer Low user and confirm the following:</span></span>

- <span data-ttu-id="c597e-220">Jeśli zainstalowana jest aplikacja Project Service, przejdź do **Project Service** > **Ustawienia** > **Cenniki**.</span><span class="sxs-lookup"><span data-stu-id="c597e-220">If the Project Service application is installed, go to **Project Service** > **Settings** > **Price Lists**.</span></span> <span data-ttu-id="c597e-221">Potwierdź, czy istnieją stawki kosztów i rachunków, w odpowiedniej walucie, dla każdego kraju/regionu w zestawie danych.</span><span class="sxs-lookup"><span data-stu-id="c597e-221">Confirm that bill rates and costs rates exist with the appropriate currency for each country/region in the data set.</span></span>

- <span data-ttu-id="c597e-222">Jeśli zainstalowana jest aplikacja Project Service, przejdź do **Universal Resource Scheduling** > **Ustawienia** > **Jednostki organizacyjne**.</span><span class="sxs-lookup"><span data-stu-id="c597e-222">If the Project Service application is installed, go to **Universal Resource Scheduling** > **Settings** > **Organizational Units**.</span></span> <span data-ttu-id="c597e-223">Upewnij się, że lista kosztów własnych z odpowiednią walutą została skojarzona z każdą jednostką organizacyjną (z wyjątkiem wpis dotyczących miast).</span><span class="sxs-lookup"><span data-stu-id="c597e-223">Confirm that a cost price list with the appropriate currency has been associated with each org unit (excluding city entries).</span></span> <span data-ttu-id="c597e-224">Jeżeli jakichkolwiek brakuje znajdź i powiąż odpowiedni cennik kosztów własnych.</span><span class="sxs-lookup"><span data-stu-id="c597e-224">If any are missing, find and associate the correct cost price list.</span></span>

- <span data-ttu-id="c597e-225">Jeśli zainstalowana jest aplikacja Field Service, przejdź do **Project Service** > **Ustawienia** > **Cenniki**.</span><span class="sxs-lookup"><span data-stu-id="c597e-225">If the Field Service application is installed, go to **Project Service** > **Settings** > **Price Lists**.</span></span> <span data-ttu-id="c597e-226">Upewnij się, istnieją stawki kosztów i rachunków.</span><span class="sxs-lookup"><span data-stu-id="c597e-226">Confirm that bill rates and costs rates exist.</span></span> <span data-ttu-id="c597e-227">Przejdź do **Field Service** > **Ustawienia** > **Cenniki** i sprawdź, czy istnieją stawki kosztów i rachunków, w odpowiedniej walucie, dla każdego kraju/regionu w zestawie danych.</span><span class="sxs-lookup"><span data-stu-id="c597e-227">Go to **Field Service** > **Settings** > **Price Lists** and check that bill rates and costs rates exist, with the appropriate currency, for each country/region in the data set.</span></span>

  > [!div class="mx-imgBorder"]
  > <span data-ttu-id="c597e-228">![Zrzut ekranu przedstawiający aktywne cenniki](media/sample-data-4.png)</span><span class="sxs-lookup"><span data-stu-id="c597e-228">![Screenshot of active price lists](media/sample-data-4.png)</span></span>

  > [!div class="mx-imgBorder"]
  > <span data-ttu-id="c597e-229">![Zrzut ekranu przedstawiający aktywne jednostki organizacyjne](media/sample-data-5.png)</span><span class="sxs-lookup"><span data-stu-id="c597e-229">![Screenshot of active organizational units](media/sample-data-5.png)</span></span>

## <a name="technical-notes"></a><span data-ttu-id="c597e-230">Uwagi techniczne</span><span class="sxs-lookup"><span data-stu-id="c597e-230">Technical notes</span></span>

<span data-ttu-id="c597e-231">Poniżej znajduje się więcej szczegółów technicznych dotyczących instalacji tych danych.</span><span class="sxs-lookup"><span data-stu-id="c597e-231">See below for more technical details on the installation of this data.</span></span>

### <a name="installing-sample-data-on-top-of-existing-data-not-recommended"></a><span data-ttu-id="c597e-232">Instalowanie danych przykładowych na istniejących danych (niezalecane)</span><span class="sxs-lookup"><span data-stu-id="c597e-232">Installing sample data on top of existing data (not recommended)</span></span>

<span data-ttu-id="c597e-233">Uwaga: Jeśli zachodzi konieczność zainstalowania przykładowych danych na istniejącym środowisku próbnym lub demonstracyjnym Field Service i Project Service które zawiera już dane (niezalecane), trzeba będzie zawiesić wstępne kontrole bezpieczeństwa wykonywane przez Instalatora.</span><span class="sxs-lookup"><span data-stu-id="c597e-233">If you need to install sample data on top of an existing Field Service or Project Service trial or demo environment that already has data, you'll need to suspend the safety prechecks performed by the installer.</span></span>

<span data-ttu-id="c597e-234">W tym celu należy przejść do folderu **PkgFolder**, aby znaleźć i otworzyć plik **DemoDataPreImportConfig.xml** z danymi Notepad (lub inny edytor XML).</span><span class="sxs-lookup"><span data-stu-id="c597e-234">To do this, go to the **PkgFolder** folder to find and open the **DemoDataPreImportConfig.xml** file with Notepad (or another XML editor).</span></span>

<span data-ttu-id="c597e-235">Znajdź następujące wartości, a następnie zmień ustawienie z true na false:</span><span class="sxs-lookup"><span data-stu-id="c597e-235">Find the following value, and then change the setting from true to false:</span></span>

```alias
<TerminateOnPreCheckFailure>true</TerminateOnPreCheckFailure>
```

<span data-ttu-id="c597e-236">Ta zmiana powoduje, że program instalacyjny pomija niektóre testy bezpieczeństwa, w tym:</span><span class="sxs-lookup"><span data-stu-id="c597e-236">This change causes the installer to bypass some important safety checks, including:</span></span>

- <span data-ttu-id="c597e-237">Potwierdzenie, że jest nie więcej niż jeden aktywny rekord **Jednostka organizacyjna**, a następnie zmień jego nazwę na **Fabrikam USA**.</span><span class="sxs-lookup"><span data-stu-id="c597e-237">Confirming that there is no more than one active **Organizational Unit** record, and then renaming it to **Fabrikam US**.</span></span>

- <span data-ttu-id="c597e-238">Potwierdzenie, że jest nie więcej niż jeden aktywny rekord **Szablon pracy**.</span><span class="sxs-lookup"><span data-stu-id="c597e-238">Confirming that there is no more than one active **Work Template** record.</span></span>

- <span data-ttu-id="c597e-239">Potwierdź, że jest nie więcej niż jeden aktywny rekord **Parametr projektu**, a następnie zmień jego nazwę na **Parametry**.</span><span class="sxs-lookup"><span data-stu-id="c597e-239">Confirming that there is no more than one active **Project Parameter** record, and then renaming that entry to **Parameters**.</span></span>

### <a name="configuration-components"></a><span data-ttu-id="c597e-240">Składniki konfiguracji</span><span class="sxs-lookup"><span data-stu-id="c597e-240">Configuration components</span></span>

<span data-ttu-id="c597e-241">Istnieje wiele innych składników konfiguracji, w tym pliku konfiguracji sprzed importu.</span><span class="sxs-lookup"><span data-stu-id="c597e-241">There are a number of other configuration components in this pre-import configuration file.</span></span> <span data-ttu-id="c597e-242">Dla użytkowników techniczne tych należą:</span><span class="sxs-lookup"><span data-stu-id="c597e-242">For technical users, some of these include:</span></span>

- <span data-ttu-id="c597e-243">**\<RequiredSolutions\>** określa wstępne instalacje rozwiązania oraz ich numery wersji.</span><span class="sxs-lookup"><span data-stu-id="c597e-243">**\<RequiredSolutions\>** specifies prerequisite solution installations and their version numbers.</span></span>

- <span data-ttu-id="c597e-244">**\<InstallSampleData\>** określa, czy standardowe dane przykładowe dla aplikacji zostały zainstalowane.</span><span class="sxs-lookup"><span data-stu-id="c597e-244">**\<InstallSampleData\>** controls whether out-of-the-box sample data for the apps is installed.</span></span>

    - <span data-ttu-id="c597e-245">false — pomija instalację tych wbudowanych danych (co można usunąć)</span><span class="sxs-lookup"><span data-stu-id="c597e-245">false - skips installation of this built-in data (which is removable)</span></span>

    - <span data-ttu-id="c597e-246">true — instaluje wbudowane dane z jednoczesną instalacją przykładowych danych FS i PSA</span><span class="sxs-lookup"><span data-stu-id="c597e-246">true - installs the built-in data concurrent with installation of the FS and PSA sample data</span></span>

- <span data-ttu-id="c597e-247">**\<PreImportDataCollection\>** określa stałe Mapy danych i skojarzone Rekordy, aby można było je zaimportować przed zainstalowaniem głównych danych przykładowych.</span><span class="sxs-lookup"><span data-stu-id="c597e-247">**\<PreImportDataCollection\>** specifies flat-file Data Maps and associated Records to be imported ahead of the main sample data installation.</span></span>

- <span data-ttu-id="c597e-248">**\<EntitiesToEnableScheduling\>** określa encje, które powinny być włączone dla Rezerwowanie w aplikacji Microsoft Dynamics Scheduling (alias Universal Resource Scheduling).</span><span class="sxs-lookup"><span data-stu-id="c597e-248">**\<EntitiesToEnableScheduling\>** specifies which entities should be enabled for Booking in Microsoft Dynamics Scheduling (aka Universal Resource Scheduling).</span></span>

- <span data-ttu-id="c597e-249">**\<UsersToCreateAndConfigure\>** określa zasoby, które można zarezerwować, które będą tworzone (jeśli jeszcze nie istnieją) zanim nastąpi zaimportowanie przykładowych danych.</span><span class="sxs-lookup"><span data-stu-id="c597e-249">**\<UsersToCreateAndConfigure\>** specifies Bookable Resources that will be created (if they don't exist already) before the sample data import executes.</span></span> <span data-ttu-id="c597e-250">Należy pamiętać, że przykładowe dane Zasoby, które można zarezerwować systemu źródłowego odpowiadają rekordom Zasoby, które można zarezerwować systemu docelowego jeśli chodzi o pełną nazwę i login każdego zasobu.</span><span class="sxs-lookup"><span data-stu-id="c597e-250">Note that the source system sample data Bookable Resource match with the target system Bookable Resource records on the FullName and login of each resource.</span></span> <span data-ttu-id="c597e-251">Z tego powodu NIE można zmieniać nazw w tym pliku konfiguracji wstępnej, chyba że wcześniej zaimportujesz dane przykładowe do systemu docelowego przy użyciu tych nazw, a następnie zmienisz nazwę Zasoby, które można zarezerwować na żądaną nazwę wraz z rekordami Włączeni użytkownicy, a następnie wyeksportujesz dane ponownie do zaimportowania do systemu przeznaczenia (aktualizując odpowiednio stare i nowe wpisy **ImportUserMapFile.xml**).</span><span class="sxs-lookup"><span data-stu-id="c597e-251">Therefore, it is NOT possible to change the names in this preconfiguration file unless you first import sample data into a target system using these names, then rename the Bookable Resources to your desired name set along with the Enabled User records, and then export the data again for import into your final destination system (updating the **ImportUserMapFile.xml** Old and New entries accordingly).</span></span>

- <span data-ttu-id="c597e-252">**\<PluginsToDisable\>** określa bardzo zindywidualizowanej dodatki plug-in pozycji, które muszą być wyłączone podczas importowania danych przykładowych i następnie ponownie włączone.</span><span class="sxs-lookup"><span data-stu-id="c597e-252">**\<PluginsToDisable\>** specifies very discrete line-item plug-ins that must be disabled during the sample data import and then reenabled afterwards.</span></span>

### <a name="fabrikam-robotics-fictitious-scenario"></a><span data-ttu-id="c597e-253">Fikcyjny scenariusz Fabrikam Robotics</span><span class="sxs-lookup"><span data-stu-id="c597e-253">Fabrikam Robotics fictitious scenario</span></span>

<span data-ttu-id="c597e-254">Pakiety danych przykładowych typu odwołanie Field Service i Project Service instalują **Rozwiązanie Fabrikam Manufacturing Master Data (v3.0.0.0)**, wraz z około 4000 rekordów i około 40 różnymi encjami.</span><span class="sxs-lookup"><span data-stu-id="c597e-254">The Field Service and Project Service sample reference data packages install the **Fabrikam Manufacturing Master Data (v3.0.0.0) solution**, along with approximately 4,000 records and approximately 40 different entities.</span></span> <span data-ttu-id="c597e-255">Pakiety przykładowych danych dla Field Service lub Project Service zawierają podzbiór danych przykładowych **v902FPSMasterData** dla tej aplikacji.</span><span class="sxs-lookup"><span data-stu-id="c597e-255">The separate sample data packages for Field Service or Project Service contain a subset of the **v902FPSMasterData** sample data for that application.</span></span> <span data-ttu-id="c597e-256">Pakiet **Dane demonstracyjne** instaluje rozwiązanie **Rozwiązane Fabrikam Manufacturing Demo Data (v3.0.0.7)** z około 22000 rekordów w 148 encjach.</span><span class="sxs-lookup"><span data-stu-id="c597e-256">The **Demo Data** package installs the **Fabrikam Manufacturing Demo Data (v3.0.0.7) solution** with approximately 22,000 records across 148 entities.</span></span>

<span data-ttu-id="c597e-257">Fikcyjna firma, Fabrikam Robotics, jest producentem robotów z linii produkcyjnej urządzeń elektronicznych i jest znana z jakości produktów, innowacji oraz obsługi klienta, w tym planowania instalacji, implementacji i bieżących prac konserwacyjnych.</span><span class="sxs-lookup"><span data-stu-id="c597e-257">The fictional company, Fabrikam Robotics, is a manufacturer of electronic device assembly line robots and is known for their product quality, innovation, and solid customer service, including installation planning, implementation, and ongoing maintenance services.</span></span> <span data-ttu-id="c597e-258">Firma Fabrikam ma swoją centralę w Stanach Zjednoczonych (Fabrikam US), i prowadzi działania związane z projektami we Francji, w Indiach, Wielkiej Brytanii i Szwajcarii.</span><span class="sxs-lookup"><span data-stu-id="c597e-258">Fabrikam is headquartered in the United States (Fabrikam US), and has project-based service operations in France, India, the United Kingdom, and Switzerland.</span></span>

<span data-ttu-id="c597e-259">Operacje usługi Field Service skupiają się na terenie Stanów Zjednoczonych, zwłaszcza w okolicach Seattle.</span><span class="sxs-lookup"><span data-stu-id="c597e-259">Field service operations are centered in the United States, mostly in the greater Seattle area.</span></span> <span data-ttu-id="c597e-260">Firma skupia się na wykorzystaniu połączenia Internet rzeczy (IoT) do monitorowania wydajności zasobu klienta i dostarczania coraz aktywniejszych usług sieciowych.</span><span class="sxs-lookup"><span data-stu-id="c597e-260">The company is focused on leveraging Internet of Things (IoT) connectivity to monitor customer asset performance and deliver increasingly proactive onsite services.</span></span>

<span data-ttu-id="c597e-261">Omówienie przykładowych danych:</span><span class="sxs-lookup"><span data-stu-id="c597e-261">A high-level overview of the sample data is as follows:</span></span>

- <span data-ttu-id="c597e-262">Typowe elementy danych przykładowych (uwzględnione w obu aplikacjach)</span><span class="sxs-lookup"><span data-stu-id="c597e-262">Common sample data elements (included for both applications)</span></span>

    - <span data-ttu-id="c597e-263">1 użytkownik</span><span class="sxs-lookup"><span data-stu-id="c597e-263">1 user</span></span>

    - <span data-ttu-id="c597e-264">71 kont</span><span class="sxs-lookup"><span data-stu-id="c597e-264">71 accounts</span></span>

    - <span data-ttu-id="c597e-265">137 kontaktów</span><span class="sxs-lookup"><span data-stu-id="c597e-265">137 contacts</span></span>

    - <span data-ttu-id="c597e-266">Różne typy transakcji i kategorii</span><span class="sxs-lookup"><span data-stu-id="c597e-266">Various transaction types and categories</span></span>

    - <span data-ttu-id="c597e-267">50 produktów i 1 cennik produktów</span><span class="sxs-lookup"><span data-stu-id="c597e-267">50 products with 1 product price list</span></span>

    - <span data-ttu-id="c597e-268">14 list kosztów własnych</span><span class="sxs-lookup"><span data-stu-id="c597e-268">14 price/cost lists</span></span>

    - <span data-ttu-id="c597e-269">31 właściwości (umiejętności zasobu) w 2 modelach klasyfikacja o 3 poziomach (wartości ocen)</span><span class="sxs-lookup"><span data-stu-id="c597e-269">31 characteristics (resource skills) in 2 rating models with 3 levels (rating values)</span></span>

- <span data-ttu-id="c597e-270">Project Service</span><span class="sxs-lookup"><span data-stu-id="c597e-270">Project Service</span></span>

    - <span data-ttu-id="c597e-271">8 jednostek organizacyjnych</span><span class="sxs-lookup"><span data-stu-id="c597e-271">8 organizational units</span></span>

    - <span data-ttu-id="c597e-272">6 poziomów wykorzystania dla poszczególnych ról</span><span class="sxs-lookup"><span data-stu-id="c597e-272">6 role-specific utilization levels</span></span>

    - <span data-ttu-id="c597e-273">2,8k + specyfikacje dla poszczególnych ról</span><span class="sxs-lookup"><span data-stu-id="c597e-273">2.8k+ role-price specifications</span></span>

- <span data-ttu-id="c597e-274">Rozwiązanie Field Service</span><span class="sxs-lookup"><span data-stu-id="c597e-274">Field Service</span></span>

    - <span data-ttu-id="c597e-275">4 obszary</span><span class="sxs-lookup"><span data-stu-id="c597e-275">4 territories</span></span>

    - <span data-ttu-id="c597e-276">5 typów zleceń pracy</span><span class="sxs-lookup"><span data-stu-id="c597e-276">5 work order types</span></span>

    - <span data-ttu-id="c597e-277">22 zasoby klienta</span><span class="sxs-lookup"><span data-stu-id="c597e-277">22 customer assets</span></span>

    - <span data-ttu-id="c597e-278">9 typów zgłoszeń z charakterystyka skojarzonego zasobu (9), usługi (13) i zadań serwisowych (13)</span><span class="sxs-lookup"><span data-stu-id="c597e-278">9 incident types with a range of associated resource characteristics (9), services (13) and service tasks (13)</span></span>
   
<span data-ttu-id="c597e-279">Pakiet **Dane demonstracyjne** instaluje około 179 zleceń pracy, 12 projektów i skojarzonych z nim danych transakcji.</span><span class="sxs-lookup"><span data-stu-id="c597e-279">The **Demo Data** package installs approximately 179 work orders, 12 projects, and associated transactional data.</span></span> 

### <a name="change-the-work-hours-for-sample-resources"></a><span data-ttu-id="c597e-280">Zmienianie godzin pracy dla zasobów przykładowych</span><span class="sxs-lookup"><span data-stu-id="c597e-280">Change the work hours for sample resources</span></span>

<span data-ttu-id="c597e-281">Domyślnie wszystkie zasoby, które można zarezerwować, mają ustawiony kalendarz pracy na 24 godziny.</span><span class="sxs-lookup"><span data-stu-id="c597e-281">By default, all bookable resources have a 24 work hours calendar.</span></span>

<span data-ttu-id="c597e-282">Jeśli zachodzi konieczność zmiany godzin pracy dla przykładowych zasobów, które można zarezerwować, przejdź do **Universal Resource Scheduling** > **Planowanie** > **Zasoby**.</span><span class="sxs-lookup"><span data-stu-id="c597e-282">If you need to change the work hours for sample bookable resources, go to **Universal Resource Scheduling** > **Scheduling** > **Resources**.</span></span>

<span data-ttu-id="c597e-283">Wybierz użytkownika (na przykład Spencer Low) i zmień godzin pracy użytkownika Spencer na godziny, które chcesz zastosować do wielu użytkowników.</span><span class="sxs-lookup"><span data-stu-id="c597e-283">Select a user (for example, Spencer Low) and change Spencer's work hours to the hours you want to apply to multiple users.</span></span> <span data-ttu-id="c597e-284">Przejdź do **Universal Resource Scheduling** > **Ustawienia** > **Szablony godzin pracy** i edytuj rekord **Domyślny szablon pracy**.</span><span class="sxs-lookup"><span data-stu-id="c597e-284">Go to **Universal Resource Scheduling** > **Settings** > **Work Hour Templates** and edit the **Default Work Template** record.</span></span> <span data-ttu-id="c597e-285">W polu **Szablon zasobu** wybierz użytkownika z godzinami pracy, które chcesz zastosować dla innych zasobów.</span><span class="sxs-lookup"><span data-stu-id="c597e-285">In the **Template Resource** field, select a user with work hours that you want to apply to other resources.</span></span> <span data-ttu-id="c597e-286">Przejdź do **Universal Resource Scheduling** > **Planowanie** > **Zasoby** > **Aktywne zasoby, które można zarezerwować**.</span><span class="sxs-lookup"><span data-stu-id="c597e-286">Go to **Universal Resource Scheduling** > **Scheduling** > **Resources** > **Active Bookable Resources**.</span></span> <span data-ttu-id="c597e-287">Wybierz zasoby, które chcesz zmienić, a następnie wybierz **Ustaw kalendarz**.</span><span class="sxs-lookup"><span data-stu-id="c597e-287">Select the resources you want to change, and then select **Set Calendar**.</span></span> <span data-ttu-id="c597e-288">Z listy rozwijanej **Szablon pracy** wybierz szablon **Domyślne godziny pracy** lub inny szablon z poprawnym zasobem szablonu.</span><span class="sxs-lookup"><span data-stu-id="c597e-288">On the **Work Template** drop-down list, select the **Default Work Hour** template or another template with the correct templating resource.</span></span> <span data-ttu-id="c597e-289">Po przejściu do tablicy harmonogramu, powinieneś zobaczyć, że zasoby mają zaktualizowane godziny pracy.</span><span class="sxs-lookup"><span data-stu-id="c597e-289">When you go to the schedule board, you should see that the resources now have updated work hours.</span></span>

> [!div class="mx-imgBorder"]
> <span data-ttu-id="c597e-290">![Zrzut ekranu przedstawiający aktywne zasoby, które można zarezerwować](media/sample-data-6.png)</span><span class="sxs-lookup"><span data-stu-id="c597e-290">![Screenshot of active bookable resources](media/sample-data-6.png)</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]