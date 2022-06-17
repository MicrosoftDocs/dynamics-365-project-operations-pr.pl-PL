---
title: Ustanowienie nowego środowiska
description: W tym artykule zamieszczono informacje dotyczące sposobu ustanawiania nowego środowiska aplikacji Project Operations.
author: sigitac
ms.date: 09/13/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 9cc3dafd6a2b6f92b585643c5d43ab52a3faf59e
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8931619"
---
# <a name="provision-a-new-environment"></a>Ustanowienie nowego środowiska

_**Zastosowane do:** Project Operations dla zasobów/scenariuszy nieopartych na zaopatrzeniu_



W tym artykule zawarto informacje na temat ustanawiania nowego środowiska Dynamics 365 Project Operations na potrzeby scenariuszy zasobów/scenariuszy nieopartych na zaopatrzeniu.

## <a name="enable-project-operations-automated-provisioning-in-an-lcs-project"></a>Włączanie zautomatyzowanego ustanawiania Project Operations w ramach projektu LCS

Wykonaj poniższe kroki, aby włączyć zautomatyzowany przepływ ustanawiania Project Operations w ramach LCS.

1. Przejdź do [LCS](https://lcs.dynamics.com/v2) i wybierz kafelek **Zarządzanie podglądem funkcji**.
2. Na liście **Wersji zapoznawczej funkcji** wybierz **Funkcja Project Operations** i wybierz **Włącz wersje zapoznawcze funkcji**, aby włączyć Project Operations.

   > [!NOTE]
   > Ten krok jest wykonywany tylko raz dla każdego projektu LCS.

## <a name="provision-a-project-operations-environment"></a>Obsługiwanie środowiska Project Operations

1. Otwórz nowe środowisko [demonstracyjne usługi Dynamics 365 Finance](/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) lub [piaskownicę/wdrożenie środowiska produkcyjnego](/dynamics365/fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure). 
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

     ![Ustawienia wdrażania.](./media/1DeploymentSettings.png)

    > [!IMPORTANT]
    > Wybierz opcję **Zgoda**, aby wyrazić zgodę na potwierdzenie warunków świadczenia usługi, a następnie wybierz opcję **Gotowy**, aby powrócić do ustawień wdrażania.
    >
    >![Zgoda na wdrożenia.](./media/2DeploymentConsent.png)

7. Opcjonalnie — zastosuj dane demonstracyjne do środowiska. Przejdź do **Ustawienia zaawansowane**, wybierz pozycję **Dostosuj konfigurację bazy danych SQL** i ustaw opcję **Określ zestaw danych dla bazy danych aplikacji** na **Demo**.
8. Wykonaj pozostałe wymagane pola kreatora i potwierdź wdrożenie. Czas udostępnienia środowiska różni się w zależności od typu środowiska. Inicjowanie obsługi może potrwać do sześciu godzin.

   Po pomyślnym zakończeniu wdrożenia środowisko będzie widoczne jako **Wdrożone**.

9. Aby potwierdzić pomyślne wdrożenie środowiska, wybierz pozycję **Zaloguj się** i zaloguj się do środowiska, aby potwierdzić.

    ![Szczegóły środowiska.](./media/3EnvironmentDetails.png)

## <a name="apply-updates-to-the-finance-environment"></a>Stosowanie aktualizacji środowiska Finance

Project Operations wymaga środowiska Finance korzystającego z aplikacji w wersji **10.0.13 (10.0.569.20009)** lub nowszej.

W celu uzyskania tej wersji może być konieczne zastosowanie aktualizacji dotyczących jakości w środowisku Finance.

1. W programie LCS na stronie **Szczegóły środowiska** w sekcji **Dostępne aktualizacje** wybierz pozycję **Wyświetl aktualizacje**.

    ![Wyświetl aktualizacje.](./media/5ViewUpdates.png)

2. Na stronie **Aktualizacje binarne** wybierz pozycję **Zapisz pakiet.**

    ![Zapisz pakiet.](./media/6SavePackage.png)

3. Wybierz pozycje **Wybierz wszystko**, a następnie wybierz **Zapisz pakiet**.

    ![Przeglądanie i zapisywanie aktualizacji.](./media/7ReviewAndSaveUpdates.png)

4. Wprowadź nazwę i opis pakietu, a następnie wybierz pozycję **Zapisz**. W zależności od jakości połączenia internetowego, proces ten może potrwać dłużej.

    ![Prześlij pakiet do biblioteki zasobów.](./media/8UploadPackageToAssetsLibrary.png)

5. Po zapisaniu pakietu wybierz opcję **Zrobione** i zapisz ten pakiet w bibliotece zasobów w projekcie programu LCS.

   Zapisanie i sprawdzanie poprawności pakietu może zająć około 15 minut.

6. Aby zastosować aktualizację, przejdź na stronę **Szczegółów środowiska** w programie LCS i wybierz pozycję **Obsługa** > **Zastosuj aktualizacje**.

    ![Obsługa środowisk.](./media/9MaintainEnvironment.png)

7. Na liście aktualizacji zaznacz utworzony pakiet i wybierz przycisk **Zastosuj**.

    ![Stosowanie aktualizacji.](./media/10ApplyUpdates.png)

   Obsługa środowiska zajmie trochę czasu. Po zakończeniu środowisko powróci do stanu wdrożonego.

    ![Wdrożone środowisko.](./media/11EnvironmentDeployed.png)

## <a name="establish-a-dual-write-connection"></a>Ustanawianie połączenia podwójnego zapisu 

1. W projekcie LCS przejdź na stronę **Szczegóły środowiska**.
2. W obszarze **Informacje o środowisku Common Data Service** wybierz pozycję **Połącz z CDS dla aplikacji**.
3. Po zakończeniu tworzenia łącza wybierz ponownie opcję **Połącz z CDS dla aplikacji**. Nastąpi przekierowanie do podwójnego zapisu w Finance.

    ![Link do systemu CDS.](./media/12LinktoCDS.png)

4. Wybierz opcję **Zastosuj rozwiązanie**, aby uzyskać dostęp do encji, które zostaną zamapowane na integrację.

    ![Zastosuj rozwiązania.](./media/13ApplySolutions.png)

5. Wybierz oba rozwiązania **Mapowanie encji podwójnych zapisu Dynamics 365 Finance and Operations** oraz **Mapowanie encji podwójnych zapisu Dynamics 365 Project Operations**, a następnie wybierz opcję **Zastosuj**.

    ![Potwierdzanie rozwiązań.](./media/14ConfirmSolutions.png)

    Po zastosowaniu rozwiązań do środowiska jest stosowana encja podwójnego zapisu.

    ![Stosowanie rozwiązań.](./media/15ApplyingSolutions.png)

    Po zastosowaniu encji wszystkie dostępne mapowania będą wyświetlane w środowisku.

    ![Mapy podwójnego zapisu.](./media/15DWMappings.png)

## <a name="refresh-the-data-entities-after-the-update"></a>Odśwież encje danych po aktualizacji

1. W Finance przejdź do obszaru roboczego **Zarządzanie danymi**.

    ![Obszar roboczy Zarządzanie danymi.](./media/16DataManagement.png)

2. Wybierz kafelek **Parametry struktury**.

    ![Parametry struktury.](./media/17FrameworkParameters.png)

3. Na stronie **Ustawienia encji** wybierz pozycję **Odśwież listę encji**.

    ![Odśwież listę encji.](./media/18RefreshEntityList.png)

Odświeżenie zajmie około 20 minut. Po jego zakończeniu otrzymasz alert.

  ![Potwierdzenie odświeżenia.](./media/19RefreshConfirmation.png)

## <a name="update-security-settings-on-project-operations-on-dataverse"></a>Aktualizowanie ustawień zabezpieczeń w programie Project Operations w Dataverse

1. Przejdź do Project Operations w swoim środowisku Dataverse. 
2. Przejdź do **Ustawienia** > **Zabezpieczenia** > **Role zabezpieczeń**. 
3. Na stronie **Role zabezpieczeń** z listy ról wybierz **użytkownik aplikacji z podwójnym zapisem** i wybierz kartę **Encje niestandardowe**.  
4. Sprawdź, czy rola ma uprawnienia **Odczyt** i **Dołącz do** dla następujących encji:
      
      - **Typ kursu wymiany waluty**
      - **Plan kont**
      - **Kalendarz obrachunkowy**
      - **Księga**
      - **Firma**
      - **Wydatek**

5. Po zaktualizowaniu rola zabezpieczeń przejdź do **Ustawienia** > **Zabezpieczenia** > **Teams** i wybierz domyślny zespół w widoku zespołu **Lokalnego właściciela firmy**.
6. Wybierz pozycję **Zarządzaj rolami** i sprawdź, czy uprawnienie zabezpieczeń **użytkownika aplikacji z podwójnym zapisem** jest stosowane do tego zespołu.

## <a name="run-project-operations-dual-write-maps"></a>Uruchomienie map podwójnego zapisu Project Operations

1. W projekcie LCS przejdź na stronę **Szczegóły środowiska**.
2. W obszarze **Informacje o środowisku Common Data Service** wybierz pozycję **Połącz z CDS dla aplikacji.** Po wybraniu łącza nastąpi przekierowanie do listy encji w mapowaniach.
3. Uruchom mapy. Aby uzyskać więcej informacji, zobacz temat [Wersje mapowania podwójnego zapisu w aplikacji Project Operations](resource-dual-write-maps.md#project-operations-dual-write-maps)
4. Sprawdź poprawność wszystkich mapowań powiązanych z projektem.

    ![Wszystkie mapowania uruchomione.](./media/22AllMapsRunning.png)


## <a name="apply-configuration-data-in-cds-for-project-operations-optional"></a>Stosowanie danych konfiguracyjnych w usłudze CDS do aplikacji Project Operations (opcjonalne)

Jeśli dane demonstracyjne zostały zastosowane do środowiska Finance, zobacz [Konfigurowanie i stosowanie danych konfiguracyjnych w Common Data Service dla Project Operations](resource-apply-pro-setup-config-data.md) w celu zastosowania danych demonstracyjnych w środowisku CDS.


Środowisko Project Operations jest teraz obsługiwane i konfigurowane. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
