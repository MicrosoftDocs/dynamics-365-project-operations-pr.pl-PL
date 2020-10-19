---
title: Stosowanie danych demonstracyjnych Project Operations do środowiska hostowanego w chmurze rozwiązania Finance
description: W tym temacie wyjaśniono, jak stosować dane demonstracyjne pochodzące z Project Operations w środowisku w chmurze Dynamics 365 Finance.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 1a94862d5a024eb1630f33c0c96699e8b4b49bf2
ms.sourcegitcommit: b9d8bf00239815f31686e9b28998ac684fd2fca4
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/02/2020
ms.locfileid: "3949015"
---
# <a name="apply-project-operations-demo-data-to-a-finance-cloud-hosted-environment"></a><span data-ttu-id="11278-103">Stosowanie danych demonstracyjnych Project Operations do środowiska hostowanego w chmurze rozwiązania Finance</span><span class="sxs-lookup"><span data-stu-id="11278-103">Apply Project Operations demo data to a Finance Cloud-hosted environment</span></span>

<span data-ttu-id="11278-104">_**Zastosowane do:** Project Operations dla zasobów/scenariuszy nieopartych na zaopatrzeniu_</span><span class="sxs-lookup"><span data-stu-id="11278-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

><span data-ttu-id="11278-105">[Uwaga] Ten temat ma zastosowanie tylko do Microsoft Dynamics 365 Finance w wersji 10.0.13 i dotyczy tylko środowiska hostowanego w chmurze.</span><span class="sxs-lookup"><span data-stu-id="11278-105">[Important] This topic is only applicable only Microsoft Dynamics 365 Finance version 10.0.13 and can be performed only on a Cloud-hosted environment.</span></span> <span data-ttu-id="11278-106">Wykonaj czynności opisane w tym temacie **PRZED** zastosowaniem aktualizacji dotyczących jakości w środowisku.</span><span class="sxs-lookup"><span data-stu-id="11278-106">Complete the steps in this topic **BEFORE** you apply quality updates to the environment.</span></span>

1. <span data-ttu-id="11278-107">W projekcie LCS otwórz stronę **Szczegóły środowiska**.</span><span class="sxs-lookup"><span data-stu-id="11278-107">In your LCS project, open the **Environment details** page.</span></span> <span data-ttu-id="11278-108">Należy zwrócić uwagę, że informacje wymagane do łączenia się ze środowiskiem za pomocą protokołu RDP (Remote Desktop Protocol) są także zawarte.</span><span class="sxs-lookup"><span data-stu-id="11278-108">Notice that it includes the details needed to connect to the environment by using Remote Desktop Protocol (RDP).</span></span>

![Szczegóły środowiska ](./media/1EnvironmentDetails.png)

<span data-ttu-id="11278-110">Pierwszy zestaw podświetlonych poświadczeń to lokalne poświadczenia konta, które zawierają hiperłącza do podłączania pulpitu zdalnego.</span><span class="sxs-lookup"><span data-stu-id="11278-110">The first set of highlighted credentials are the local account credentials and contain a hyperlink to the remote desktop connection.</span></span> <span data-ttu-id="11278-111">Poświadczenia zawierają nazwę użytkownika i hasło administratora środowiska.</span><span class="sxs-lookup"><span data-stu-id="11278-111">The credentials include the environment admin username and password.</span></span> <span data-ttu-id="11278-112">Drugi zestaw poświadczeń jest używany do logowania się w programie SQL Server w tym środowisku.</span><span class="sxs-lookup"><span data-stu-id="11278-112">The second set of credentials are used to log in to SQL Server in this environment.</span></span>

2. <span data-ttu-id="11278-113">Połącz się z środowiskiem za pomocą hiperłącza znajdującego się w sekcji **Konta lokalne** i użyj **poświadczeń konta lokalnego** do uwierzytelnienia.</span><span class="sxs-lookup"><span data-stu-id="11278-113">Remote to the environment by the hyperlink in **Local Accounts**, and use the **Local Account credentials** to authenticate.</span></span>
3. <span data-ttu-id="11278-114">Wybierz pozycję **Internet Information Services (IIS)** > **Pule aplikacji** > **AOSService** i zatrzymaj usługę.</span><span class="sxs-lookup"><span data-stu-id="11278-114">Go to **Internet Information Services** > **Application Pools** > **AOSService** and stop the service.</span></span> <span data-ttu-id="11278-115">Zatrzymujesz usługę w tym punkcie, aby móc zastępować bazę danych SQL.</span><span class="sxs-lookup"><span data-stu-id="11278-115">You are stopping the service at this point so that you can continue to replace the SQL database.</span></span>

![Zatrzymaj AOS](./media/2StopAOS.png)

4. <span data-ttu-id="11278-117">Przejdź do sekcji **Usługi** i zatrzymaj następujące dwa elementy:</span><span class="sxs-lookup"><span data-stu-id="11278-117">Go to **Services** and stop the following two items:</span></span>

- <span data-ttu-id="11278-118">Microsoft Dynamics 365 Unified Operations: Batch Management Service</span><span class="sxs-lookup"><span data-stu-id="11278-118">Microsoft Dynamics 365 Unified Operations: Batch Management Service</span></span>
- <span data-ttu-id="11278-119">Microsoft Dynamics 365 Unified Operations: Data Import Export Framework</span><span class="sxs-lookup"><span data-stu-id="11278-119">Microsoft Dynamics 365 Unified Operations: Data Import Export Framework</span></span>

![Zatrzymaj usługi](./media/3StopServices.png)

5. <span data-ttu-id="11278-121">Otwórz Microsoft SQL Server Management Studio.</span><span class="sxs-lookup"><span data-stu-id="11278-121">Open Microsoft SQL Server Management Studio.</span></span> <span data-ttu-id="11278-122">Zaloguj się przy użyciu poświadczeń programu SQL Server i użyj konta axdbadmin i hasła ze strony **Szczegóły środowiska** LCS.</span><span class="sxs-lookup"><span data-stu-id="11278-122">Log in with SQL server credentials and use the axdbadmin user and password from the LCS **Environments details** page.</span></span>

![SQL Server Management Studio](./media/4SSMS.png)

6. <span data-ttu-id="11278-124">W przypadku korzystania z Eksploratora obiektów, **Bazy danych** i zlokalizuj **AXDB**.</span><span class="sxs-lookup"><span data-stu-id="11278-124">In Object Explorer, **Databases** and locate **AXDB**.</span></span> <span data-ttu-id="11278-125">Baza danych zostanie zamieniona na nową, która znajduje się w [Centrum pobierania](https://download.microsoft.com/download/1/a/3/1a314bd2-b082-4a87-abdc-1ba26c92b63d/ProjOpsDemoDataFOGARelease.zip).</span><span class="sxs-lookup"><span data-stu-id="11278-125">You will replace database with a new database that is located in the [Download Center](https://download.microsoft.com/download/1/a/3/1a314bd2-b082-4a87-abdc-1ba26c92b63d/ProjOpsDemoDataFOGARelease.zip).</span></span> 
7. <span data-ttu-id="11278-126">Skopiuj plik zip na maszynę wirtualną, która jest zdalnie przydzielone do programu, a następnie wyodrębnij zawartość zip.</span><span class="sxs-lookup"><span data-stu-id="11278-126">Copy the zip file to the VM you are remoted into and extract zip contents.</span></span>
8. <span data-ttu-id="11278-127">W programie SQL Server Management Studio kliknij prawym przyciskiem myszy opcję **AxDB**, a następnie wybierz kolejno pozycje **Zadania** > **Przywracanie** > **Bazy danych**.</span><span class="sxs-lookup"><span data-stu-id="11278-127">In SQL Server Management Studio, right-click **AxDB**, and then select **Tasks** > **Restore** > **Database**.</span></span>

![Przywróć bazę danych](./media/5RestoreDatabase.png)

9. <span data-ttu-id="11278-129">Wybierz **Urządzenie źródłowe** i przejdź do pliku wyodrębnionego z kodu zip, który został skopiowany.</span><span class="sxs-lookup"><span data-stu-id="11278-129">Select **Source Device** and navigate to the file extracted from zip you copied.</span></span>

![Urządzenia źródłowe](./media/6SourceDevice.png)

10. <span data-ttu-id="11278-131">Wybierz **Opcje**, a następnie wybierz opcję **Zastąp istniejącą bazę danych** i **Zamknij istniejące połączenia z docelową bazą danych**.</span><span class="sxs-lookup"><span data-stu-id="11278-131">Select **Options**, and then select **Overwrite the existing database** and **Close existing connections to destination database**.</span></span> 
11. <span data-ttu-id="11278-132">Wybierz pozycję **OK**.</span><span class="sxs-lookup"><span data-stu-id="11278-132">Select **OK**.</span></span>

![Przywracanie ustawień](./media/7RestoreSetting.png)

<span data-ttu-id="11278-134">Otrzymasz potwierdzenie, że przywracanie AXDB zakończyło się sukcesem.</span><span class="sxs-lookup"><span data-stu-id="11278-134">You will receive confirmation that the AXDB restore was successful.</span></span> <span data-ttu-id="11278-135">Po otrzymaniu tego potwierdzenia można zamknąć program SQL Services Management Studio.</span><span class="sxs-lookup"><span data-stu-id="11278-135">After you receive this confirmation, you can close SQL Services Management Studio.</span></span>

12. <span data-ttu-id="11278-136">Wybierz ponownie pozycję **Internet Information Services (IIS)** > **Pule aplikacji** > **AOSService** i uruchom AOSService.</span><span class="sxs-lookup"><span data-stu-id="11278-136">Go back to **Internet Information Services** > **Application Pools** > **AOSService** and start the AOSService.</span></span>
13. <span data-ttu-id="11278-137">Wybierz kolejno pozycje **Usługi** i uruchom dwie usługi, które zatrzymałeś wcześniej.</span><span class="sxs-lookup"><span data-stu-id="11278-137">Go to **Services** and start the two services you stopped earlier.</span></span>

14. <span data-ttu-id="11278-138">Znajdź narzędzie AdminUserProvisioning na tej maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="11278-138">Locate the AdminUserProvisioning tool on this VM.</span></span> <span data-ttu-id="11278-139">Szukaj w K:\AosService\PackagesLocalDirectory\bin\AdminUserProvisioning.exe.</span><span class="sxs-lookup"><span data-stu-id="11278-139">Look under, K:\AosService\PackagesLocalDirectory\bin\AdminUserProvisioning.exe.</span></span>
15. <span data-ttu-id="11278-140">Uruchom plik .ext, korzystając z adresu użytkownika w polu **adresu e-mail**.</span><span class="sxs-lookup"><span data-stu-id="11278-140">Run the .ext file using your user address in the **Email Address** field.</span></span> 
16. <span data-ttu-id="11278-141">Wybierz **Prześlij**.</span><span class="sxs-lookup"><span data-stu-id="11278-141">Select **Submit**.</span></span>

![Inicjowanie obsługi administratora](./media/8AdminUserProvisioning.png)

<span data-ttu-id="11278-143">Wykonanie tej czynności może potrwać do kilku minut.</span><span class="sxs-lookup"><span data-stu-id="11278-143">This takes a couple of minutes to complete.</span></span> <span data-ttu-id="11278-144">Powinien zostać wyświetlony komunikat z potwierdzeniem, że użytkownik administrator został pomyślnie zaktualizowany.</span><span class="sxs-lookup"><span data-stu-id="11278-144">You should receive a confirmation message that the Admin user was successfully updated.</span></span>

17. <span data-ttu-id="11278-145">Na koniec należy uruchomić wiersz polecenia jako administrator i wykonać polecenie iisreset</span><span class="sxs-lookup"><span data-stu-id="11278-145">Lastly, run Command Prompt as Administrator and perform iisreset</span></span>

![IIS Reset](./media/9IISReset.png)

18. <span data-ttu-id="11278-147">Zamknij sesję pulpitu zdalnego i na stronie **Szczegóły środowiska** LCS zaloguj się w celu potwierdzenia, że wszystko działa zgodnie z oczekiwaniami.</span><span class="sxs-lookup"><span data-stu-id="11278-147">Close the remote desktop session and use the LCS **Environment details** page to log in to the environment to confirm it is working as expected.</span></span>

![Finance and Operations](./media/10FinanceAndOperations.png)
