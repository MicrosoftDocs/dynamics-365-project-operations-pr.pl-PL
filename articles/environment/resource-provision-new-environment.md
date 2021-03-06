---
title: Ustanowienie nowego środowiska
description: W tym temacie zamieszczono informacje dotyczące tworzenia nowego środowiska w Project Operations.
author: sigitac
manager: Annbe
ms.date: 10/02/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 45700371c50e3b5a840df45fc24fa8a5b4584b61
ms.sourcegitcommit: 87b7a8d793c19c50f3765b8d788cde24a6a0ca24
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/02/2020
ms.locfileid: "3949375"
---
# <a name="provision-a-new-environment"></a>Ustanowienie nowego środowiska

_**Zastosowane do:** Project Operations dla zasobów/scenariuszy nieopartych na zaopatrzeniu_

W tym temacie zamieszczono informacje dotyczące sposobu ustanawiania nowego środowiska Dynamics 365 Project Operations do obsługi zasobów i niemagazynowanych scenariuszy.

## <a name="enable-project-operations-automated-provisioning-in-an-lcs-project"></a>Włączanie zautomatyzowanego ustanawiania Project Operations w ramach projektu LCS

Wykonaj poniższe kroki, aby włączyć zautomatyzowany przepływ ustanawiania Project Operations w ramach LCS.

1. Przejdź do [LCS](https://lcs.dynamics.com/v2) i wybierz kafelek **Zarządzanie podglądem funkcji**.
2. Na liście **Wersji zapoznawczej funkcji** wybierz **Project Operations** i wybierz **Włącz wersje zapoznawcze funkcji**, aby włączyć Project Operations.

> [!NOTE]
> Ten krok jest wykonywany tylko raz dla każdego projektu LCS.

## <a name="provision-a-project-operations-environment"></a>Obsługiwanie środowiska Project Operations

1. Otwórz nowe [środowisko pokazowe](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) Dynamics 365 Finance lub [piaskownicę/wdrożenie środowiska produkcyjnego](https://docs.microsoft.com/edynamics365/fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure). 
2. Wykonaj kroki kreatora **Inicjowania obsługi środowiska**. 

> [!IMPORTANT]
> Upewnij się, że wybrana wersja aplikacji to 10.0.13 lub wyższa.

3. Aby zainicjować obsługę Project Operations, w obszarze **Ustawienia zaawansowane** wybierz opcję **Common Data Service**. 
4. Aby włączyć to **Ustawienie Common Data Service**, należy wybrać opcję **Tak** i wprowadzić informacje w wymaganych polach:

  - Nazwa/nazwisko
  - Region
  - Język
  - Waluta
 
5. W polu **Szablon Common Data Service** wybierz **Project Operations** 

6. Wybierz typ środowiska dla swojego wdrożenia. Wersja próbna oparta na subskrypcji umożliwia wdrożenie środowiska CDS przez 30 dni. 

![Ustawienia wdrażania](./media/1DeploymentSettings.png)

> [!IMPORTANT]
> Wybierz opcję **Zgoda**, aby wyrazić zgodę na potwierdzenie warunków świadczenia usługi, a następnie wybierz opcję **Gotowy**, aby powrócić do ustawień wdrażania.

![Zgoda na wdrożenia](./media/2DeploymentConsent.png)

7. Wykonaj pozostałe wymagane pola kreatora i potwierdź wdrożenie. Czas inicjowania obsługi środowiska jest różny w zależności od typu środowiska. Inicjowanie obsługi może potrwać do sześciu godzin.

  Po pomyślnym zakończeniu wdrożenia środowisko będzie widoczne jako **Wdrożone**.

8. Aby upewnić się, że środowisko zostało pomyślnie wdrożone, wybierz opcję **Logowanie** i zaloguj się do środowiska w celu potwierdzenia.

![Szczegóły środowiska ](./media/3EnvironmentDetails.png)

## <a name="apply-project-operations-finance-demo-data-optional-step"></a>Stosowanie finansowych danych demonstracyjnych Finance w Project Operations (opcjonalny krok)

Umożliwia zastosowanie danych demonstracyjnych Finance w Project Operations do hostowanego w chmurze środowiska w wersji 10.0.13, jak to opisano w [tym artykule](resource-apply-finance-demo-data.md).

## <a name="apply-updates-to-the-finance-environment"></a>Stosowanie aktualizacji środowiska Finance

Project Operations wymaga środowiska Finance korzystającego z aplikacji w wersji **10.0.13 (10.0.569.20009)** lub nowszej.

W celu uzyskania tej wersji może być konieczne zastosowanie aktualizacji dotyczących jakości w środowisku Finance.

1. W programie LCS na stronie **Szczegóły środowiska** w sekcji **Dostępne aktualizacje** wybierz pozycję **Wyświetl aktualizacje**.

![Wyświetl aktualizacje](./media/5ViewUpdates.png)

2. Na stronie **Aktualizacje binarne** wybierz pozycję **Zapisz pakiet.**

![Zapisz pakiet](./media/6SavePackage.png)

3. Wybierz pozycje **Wybierz wszystko**, a następnie wybierz **Zapisz pakiet**.

![Przeglądanie i zapisywanie aktualizacji](./media/7ReviewAndSaveUpdates.png)

4. Wprowadź nazwę i opis pakietu, a następnie wybierz pozycję **Zapisz**. W zależności od jakości połączenia internetowego, proces ten może potrwać dłużej.

![Prześlij pakiet do biblioteki zasobów](./media/8UploadPackageToAssetsLibrary.png)

5. Po zapisaniu pakietu wybierz opcję **Zrobione** i zapisz ten pakiet w bibliotece zasobów w projekcie programu LCS.

Zapisanie i sprawdzanie poprawności pakietu może zająć około 15 minut.

6. Aby zastosować aktualizację, przejdź na stronę **Szczegółów środowiska** w programie LCS i wybierz pozycję **Obsługa** > **Zastosuj aktualizacje**.

![Obsługa środowisk](./media/9MaintainEnvironment.png)

7. Na liście aktualizacji zaznacz utworzony pakiet i wybierz przycisk **Zastosuj**.

![Stosowanie aktualizacji](./media/10ApplyUpdates.png)

Obsługa środowiska zajmie trochę czasu. Po zakończeniu środowisko powróci do stanu wdrożonego.

![Wdrożone środowisko](./media/11EnvironmentDeployed.png)

## <a name="establish-a-dual-write-connection"></a>Ustanawianie połączenia podwójnego zapisu 

1. W projekcie LCS przejdź na stronę **Szczegóły środowiska**.
2. W obszarze **Informacje o środowisku Common Data Service** wybierz pozycję **Połącz z CDS dla aplikacji**.
3. Po zakończeniu tworzenia łącza wybierz ponownie opcję **Połącz z CDS dla aplikacji**. Nastąpi przekierowanie do podwójnego zapisu w Finance.

![Link do systemu CDS](./media/12LinktoCDS.png)

4. Wybierz opcję **Zastosuj rozwiązanie**, aby uzyskać dostęp do encji, które zostaną zamapowane na integrację.

![Zastosuj rozwiązania](./media/13ApplySolutions.png)

5. Zaznacz oba rozwiązania, **Mapowanie encji z podwójnym zapisem Dynamics 365 Finance and Operations** i **Mapowanie encji z podwójnym zapisem Dynamics 365 Project Operations**, a następnie kliknij przycisk **Zastosuj**.

![Potwierdzanie rozwiązań](./media/14ConfirmSolutions.png)

Po zastosowaniu rozwiązań do środowiska jest stosowana encja podwójnego zapisu.

![Stosowanie rozwiązań](./media/15ApplyingSolutions.png)

Po zastosowaniu encji wszystkie dostępne mapowania będą wyświetlane w środowisku.

![Mapy podwójnego zapisu](./media/15DWMappings.png)

## <a name="refresh-the-data-entities-after-the-update"></a>Odśwież encje danych po aktualizacji

1. W Finance przejdź do obszaru roboczego **Zarządzanie danymi**.

![Obszar roboczy Zarządzanie danymi](./media/16DataManagement.png)

2. Wybierz kafelek **Parametry struktury**.

![Parametry struktury](./media/17FrameworkParameters.png)

3. Na stronie **Ustawienia encji** wybierz pozycję **Odśwież listę encji**.

![Odśwież listę encji](./media/18RefreshEntityList.png)

Odświeżenie zajmie około 20 minut. Po jego zakończeniu otrzymasz alert.

![Potwierdzenie odświeżenia](./media/19RefreshConfirmation.png)

## <a name="run-project-operations-dual-write-maps"></a>Uruchomienie map podwójnego zapisu Project Operations

1. W projekcie LCS przejdź na stronę **Szczegóły środowiska**.
2. W obszarze **Informacje o środowisku Common Data Service** wybierz pozycję **Połącz z CDS dla aplikacji.** Po wybraniu łącza nastąpi przekierowanie do listy encji w mapowaniach.
3. Uruchom mapowanie w sposób opisany w poniższej tabeli. Upewnij się, że kolejność jest zgodna z tą na liście.

| **Mapowanie encji** | **Odśwież encje** | **Synchronizacja początkowa** | **Wzorzec dla synchronizacji początkowej** | **Uruchom wymagania wstępne** | **Synchronizacja początkowa wymagań** |
| --- | --- | --- | --- | --- | --- |
| **Role zasobów projektu dla wszystkich firm (bookableresourcecategories)** | No | Tak | Common Data Service | No | nie dotyczy |
| **Firmy (cdm\_companies)** | No | Tak | Aplikacje rozwiązania Finance and Operations | No | nie dotyczy |
| **Wartości rzeczywiste integracji Project Operations (msdyn\_actuals)** | No | No | nie dotyczy | Tak | No |
| **Pozycje kontraktu w projekcie (salesorderdetails)** | No | No | nie dotyczy | No | No |
| **Encja integrująca dla transakcji projektu relacje (msdyn\_transactionconnections)** | No | No | nie dotyczy | No | nie dotyczy |
| **Punkty kontrolne pozycji kontraktu w integracji Project Operations (msdyn\_contractlinesscheduleofvalues)** | No | No | nie dotyczy | No | nie dotyczy |
| **Encja integracji Project Operations na potrzeby oszacowania kosztów (msdyn\_estimateslines)** | No | No | nie dotyczy | No | nie dotyczy |
| **Encja integracji Project Operations na potrzeby oszacowania godzinowego (msdyn\_resourceassignments)** | No | No | nie dotyczy | No | nie dotyczy |
| **Encja integracji wydatków projektowych Project Operations (msdyn\_expenses)** | Tak | No | nie dotyczy | No | nie dotyczy |
| **Encja integracji Project Operations na potrzeby oszacowania godzinowego (msdyn\_resourceassignments)** | Tak | No | nie dotyczy | No | nie dotyczy |

4. Aby odświeżyć encję, wybierz nazwę mapowania, a następnie wybierz opcję **Odśwież encje**. 
5. Wykonaj czynności, aby uruchomić mapowanie po zakończeniu odświeżania.

![Odśwież mapowanie](./media/20RefreshMapping.png)

Przed włączeniem następnego mapowania należy sprawdzić, czy mapowanie w tabeli jest w stanie **Działającym**. Uruchamianie mapowania z większą liczbą wstępnie wymaganych programów może zająć dużo czasu.

Aby uruchomić mapowanie z wymaganiami wstępnymi, włącz przełącznik **Pokaż mapowania encji pokrewnych**. Jeśli tabela wskazuje , że **Wymagana wstępna synchronizacja** ma stan **Nie** sprawdź, czy flaga **Wstępna synchronizacja** jest **wyłączona** we wszystkich mapowaniach wymagań wstępnych, zanim zostanie ono uruchomione.

![Uruchom mapowanie](./media/21RunMap.png)

6. Sprawdź poprawność wszystkich mapowań powiązanych z projektem.

![Wszystkie mapowania uruchomione](./media/22AllMapsRunning.png)

Środowisko Project Operations jest teraz obsługiwane i konfigurowane.
