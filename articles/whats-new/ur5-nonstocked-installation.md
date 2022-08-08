---
title: Aktualizowanie Project Operations w środowisku Finance
description: Ten artykuł zawiera informacje na temat aktualizowania Project Operations w środowisku Dynamics 365 Finance.
author: ruhercul
ms.date: 12/11/2020
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: aedfd815521054d58944496500aa03a27be9267b
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 06/18/2022
ms.locfileid: "9030048"
---
# <a name="update-project-operations-in-your-finance-environment"></a>Aktualizowanie Project Operations w środowisku Finance

_**Zastosowane do:** Project Operations dla zasobów/scenariuszy nieopartych na zaopatrzeniu_


Ten artykuł zawiera informacje na temat aktualizowania Dynamics 365 Project Operations w środowisku Dynamics 365 Finance. Istnieją trzy procedury, które są wymagane do aktualizacji Project Operations do aktualizacji 5 (UR5):

- [Importowanie pakietu do projektu w wersji zapoznawczej](#import)
- [Stosowanie aktualizacji](#apply)
- [Aktualizacja środowiska Dataverse](#update)

## <a name="import-the-package-into-your-lcs-project"></a><a name="import"></a>Importowanie pakietu do projektu LCS

1. Zaloguj się do [Lifecycle Services (LCS)](https://lcs.dynamics.com/) jako właściciel projektu lub menedżer środowiska.
2. Z listy projektów wybierz swój projekt LCS.
3. Na stronie **Projekt** w grupie **Środowiska** otwórz środowisko, które chcesz zaktualizować.
4. Sprawdź, czy środowisko jest uruchomione. Jeśli nie zostało uruchomione, uruchom środowisko.
5. W sekcji **Nowa wersja** w obszarze **Dostępne aktualizacje** wybierz pozycję **Wyświetl aktualizację** dla wersji 10.0.15.

![Wyświetl przycisk aktualizacji.](media/view-update.png)

6. Na stronie **Aktualizacje binarne** wybierz pozycję **Zapisz pakiet**.
7. Na stronie **Przejrzyj i zapisz aktualizacje** wybierz pozycję **Zapisz pakiet**.
8. W okienku **Zapisz pakiet do biblioteki elementów zawartości**, które się otworzy, wprowadź nazwę pakietu, a następnie wybierz pozycję **Zapisz pakiet**.
9. Po zakończeniu zapisywania pakietu przez LCS przycisk **Gotowe** jest włączony. Wybierz pozycję **Gotowe**. LCS zweryfikuje pakiet. Weryfikacja może potrwać kilka minut lub do jednej godziny.


## <a name="apply-the-package-update"></a><a name="apply"></a>Zastosuj aktualizację pakietu

1. W LCS na stronie **Szczegóły środowiska** wybierz pozycję **Zachowaj** > **Zastosuj aktualizacje**.
2. Z listy wybierz pakiet zapisany wcześniej, a następnie wybierz pozycję **Zastosuj**.
3. Wybierz pozycję **Tak**, aby potwierdzić, że chcesz wdrożyć pakiet.

![Okno dialogowe Potwierdzanie wdrażania pakietu.](media/confirm-package-deployment.png)

4. Wybierz pozycję **Tak**, aby potwierdzić, że chcesz aktualizować aplikację.

![Okno dialogowe Potwierdzanie aktualizacji aplikacji.](media/confirm-application-update.png)

Rozpocznie się aktualizacja wdrożenia i aplikacji. 

Na stronie **Szczegóły środowiska** w prawym górnym rogu stan środowiska zostanie zaktualizowany do **Serwisu**. Za około dwie godziny aktualizacja zostanie zakończona. Informacje o wersji aplikacji zostaną zaktualizowane do **Microsoft Dynamics 365 for Finance and Operations 10.0.15)**, a stan środowiska zostanie zaktualizowany do **Wdrożonego**.


## <a name="update-your-dataverse-environment"></a><a name="update"></a>Aktualizacja środowiska Dataverse

1. Zaloguj się w [Centrum administracyjnym Power Platform](https://admin.powerplatform.com/).
2. Na liście znajdź i otwórz środowisko używane do instalowania Project Operations.
3. Na stronie **Środowiska** wybierz **Zasób** > **aplikacje Dynamics 365**.
4. Na liście znajdź pozycję **Microsoft Dynamics 365 Project Operations**, a następnie w kolumnie **Stan** wybierz opcję **Dostępna aktualizacja**.
5. Zaznacz pole wyboru **Wyrażam zgodę na warunki usługi**, a następnie wybierz opcję **Aktualizuj**. Zostanie zainstalowana najnowsza wersja rozwiązania.

Po zakończeniu instalacji zostanie zainstalowana wersja 4.5.0.134.

## <a name="configure-new-features"></a>Konfigurowanie nowych funkcji

### <a name="enable-dual-write-mapping"></a>Włącz mapowanie z podwójnym zapisem

Po zakończeniu aktualizacji w środowiskach Finance i Dataverse można włączyć wymagane mapowania z podwójnym zapisem. Wykonaj następujące procedury, aby włączyć mapowanie z podwójnym zapisem.

- [Aktualizowanie ustawień zabezpieczeń w środowisku Customer Engagement](#security)
- [Odśwież encje danych](#refresh)
- [Aktualizowanie i uruchamianie mapowań z podwójnym zapisem](#run)

### <a name="update-security-settings-on-the-dataverse-environment"></a><a name="security"></a>Aktualizowanie ustawień zabezpieczeń w środowisku Dataverse

W ramach aktualizacji UR5 są wymagane następujące aktualizacje uprawnień zabezpieczeń encji.

1. W środowisku Dataverse wybierz opcję **Ustawienia** i w grupie **System** wybierz opcję **Zabezpieczenia**.

![Ustawienia środowiska Dataverse.](media/Picture21.png)

2. Wybierz **Role zabezpieczeń**.
3. Z listy ról wybierz **użytkownik aplikacji z podwójnym zapisem** i wybierz kartę **Encje niestandardowe**. 
4. Sprawdź, czy rola ma uprawnienia **Odczyt** i **Dołączanie do** dla:

      - **Typ kursu wymiany waluty**
      - **Plan kont** 
      - **Kalendarz obrachunkowy** 
      - **Księga**

5. Po rola zabezpieczeń należy wybrać pozycję **Ustawienia** > **Zabezpieczenia** > **Teams**. Sprawdź, czy do zespołu została zastosowana rola **użytkownika aplikacji z podwójnym zapisem**. 

### <a name="refresh-data-entities-from-the-update"></a><a name="refresh"></a>Odświeżanie encji danych z aktualizacji

1. W środowisku Finance otwórz obszar roboczy **Zarządzania danymi**, a następnie otwórz stronę **parametrów Framework**.
2. Na karcie **Ustawienia encji** wybierz opcję **Odśwież listę encji**.
3. Wybierz opcję **Zamknij**, aby potwierdzić odświeżenie encji.

 > [!NOTE]
 > Ten proces zajmie około 20 minut. Po zakończeniu odświeżania otrzymasz powiadomienie.

### <a name="update-dual-write-mappings"></a><a name="run"></a>Zaktualizuj mapowania z podwójnym zapisem

1. W obszarze roboczym **Zarządzania danymi** wybierz opcję **Podwójny zapis**.
2. Wybierz opcję **Zastosuj rozwiązania**, wybierz oba rozwiązania z listy, a następnie wybierz opcję **Zastosuj**.
3. Na stronie **Podwójny zapis** wybierz poniższe mapowania tabeli, a następnie wybierz opcję **Zatrzymaj**.

    - **Wartości rzeczywiste integracji Project Operations (msdyn_actuals)**
    - **Kategorie kosztów projektu integracji z Project Operations (msdyn_expensecategories)**
    - **Integracja Project Operations aktualizuje jednostkę eksportu kosztów projektu (msdyn_expenses)**

4. Na stronie **Wersja mapowania tabeli** można zastosować nową wersję mapowania do każdej z trzech encji.
5. Na stronie **Podwójny zapis** wybierz opcję Uruchom, aby ponownie uruchomić mapowania.
6. Z listy map wybierz mapowanie **Księga (msdyn_ledgers)** ze wszystkimi wymaganiami wstępnymi i zaznacz pole wyboru **Synchronizacja początkowa**. 
7. W polu **Główny dla początkowej synchronizacji** wybierz **Aplikacje finansowe i operacyjne**, a następnie wybierz opcję **Uruchom**.
 
 ![Synchronizacja mapowania księgi.](media/DW6.png)
 


[!INCLUDE[footer-include](../includes/footer-banner.md)]