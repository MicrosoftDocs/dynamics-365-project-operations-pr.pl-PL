---
title: Konfigurowanie materiałów niemagazynowanych i oczekujących faktur od dostawcy
description: W tym temacie wyjaśniono, jak włączyć obsługę materiałów niebędących na stanie magazynowym i oczekujących na faktury dostawcy.
author: sigitac
ms.date: 06/22/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 9b55d959228062fc3577cf7f12d8926f51e9791f98c73fdc4b78251312a8a77a
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/06/2021
ms.locfileid: "7003244"
---
# <a name="configure-non-stocked-materials-and-pending-vendor-invoices"></a>Konfigurowanie materiałów niemagazynowanych i oczekujących faktur od dostawcy

_**Zastosowane do:** Project Operations dla zasobów/scenariuszy nieopartych na zaopatrzeniu_

## <a name="minimum-version-requirement"></a>Wymagana wersja

Korzystanie z materiałów niebędących na stanie magazynowym i oczekujących na faktury dostawców w scenariuszach Dynamics 365 Project Operations opartych na materiałach niebędących na stanie magazynowym / w zasobach wymaga następujących wersji:

Rozwiązania Dynamics 365 Dataverse:

- Project Operations – 4.9.0.221 lub nowsze
- Rozwiązanie aranżacji aplikacji podwójnego zapisu - 2.2.2.23 lub nowsze

Dynamics 365 Finance:
- 10.0.18 (10.0.793.52) lub nowsza. Upewnij się, że środowisko Finance jest aktualne, a wszystkie aktualizacje jakościowe zostały zastosowane w celu spełnienia minimalnych wymagań dotyczących wersji.

## <a name="run-dual-write-maps-for-non-stocked-materials-and-vendor-invoice-integration"></a>Uruchom mapy podwójnego zapisu dla materiałów nie będących na stanie magazynowym oraz integrację faktur dostawców

W tej sekcji przedstawiono informacje na temat map wymaganych dla materiałów nie będących w magazynie oraz na fakturach od dostawców. Sprawdź, czy mapy warunków wstępnych wymienione w temacie [Konfiguracja nowego środowiska](../environment/resource-provision-new-environment.md#run-project-operations-dual-write-maps) są uruchomione w twoim środowisku.

1. Przejdź do Lifecycle Services (LCS), przejdź do swojego projektu LCS i przejdź do strony **szczegółów środowiska**.
2. W sekcji **Informacje o środowisku Common Data Service** wybierz pozycję **Łącze do CDS dla aplikacji**. Po wybraniu łącza nastąpi przekierowanie do listy encji w mapowaniach.
3. Upewnij się, że są uruchomione następujące mapowania. Jeśli nie są uruchomione, uruchom je i upewnij się, że zawierają wszystkie powiązane mapowania tabel.

    - Wydane produkty odrębne CDS (products)
    - Vendors v2 (msdyn_vendors)
    - Tabela Project Operations dla szacowania materiałów (msdyn_estimatelines)
    - Integracja w Project Operations encji eksportu faktury dostawcy projektu (msdyn_projectvendorinvoices)
    - Integracja w Project Operations encji eksportu wiersza faktury dostawcy projektu (msdyn_projectvendorinvoicelines)
    - Wartości rzeczywiste integracji Project Operations (msdyn_actuals). Upewnij się, że mapa jest uruchomiona w wersji 1.0.0.14 lub nowszej. Aktywną wersję mapy można zobaczyć w kolumnie **Wersja** na stronie **Zapis podwójny**. Aby uaktywnić nową wersję mapy, należy wybrać **wersję mapowania tabeli**, a następnie zapisać wybraną wersję.

Jeśli korzystasz ze standardowych danych demonstracyjnych, podczas początkowej synchronizacji konieczne może być również zatrzymanie i ponowne uruchomienie następujących mapowanych encji:
  - Dni płatności CDS V2 (msdyn_paymentdays)
  - Harmonogram płatności (msdyn_paymentschedules)
  - Warunki płatności (msdyn_paymentterms)
  - Grupy dostawców (msdyn_vendorgroups)
  - Jednostki (uom)

> [!NOTE]
> Początkowa synchronizacja grup i jednostek dostawcy może nie powieść się w przypadku kilku rekordów w istniejącym zestawie danych demonstracyjnych. Możesz zignorować te błędy, ponieważ nie przeszkodzą Ci one w użyciu danych demo z Project Operations.

## <a name="configure-prerequisites-in-dataverse"></a>Konfigurowanie wymagań wstępnych w Dataverse

### <a name="activate-workflow-to-create-accounts-based-on-vendor-entity"></a>Aktywowanie przepływu pracy w celu utworzenia kont na podstawie encji dostawcy

Rozwiązanie Aranżacji podwójnego zapisu zapewnia [Integracja główną dostawców](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/vendor-mapping). Warunkiem działania tej funkcji jest utworzenie danych sprzedawcy w encji **Konta**. Aktywuj proces przepływu pracy szablonu, aby utworzyć dostawców w tabeli **Konta** w sposób opisany w temacie [Przełączanie się pomiędzy projektami dostawców](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/vendor-switch).

### <a name="set-products-to-be-created-as-active"></a>Ustawianie produktów, które mają być utworzone jako aktywne

Materiały nie magazynowane muszą być skonfigurowane jako **Produkty wydane** w programie Finance. Rozwiązanie Aranżacji podwójnego zapisu daje gotową opcję [integracji wydanych produktów z katalogiem produktów Dataverse](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/product-mapping). Domyślnie produkty z programu Finance są synchronizowane z Dataverse w stanie roboczym. Aby zsynchronizować produkt ze stanem aktywnym, który może być bezpośrednio używany w dokumentach użycia materiałów lub oczekujących fakturach od dostawcy, przejdź do menu **System** > **Administracja** > **Administracja systemu** > **Ustawienia systemowe** i na karcie **Sprzedaż** ustaw opcję **Tworzenie produktów w stanie aktywnym** na **Tak**.

## <a name="configure-prerequisites-in-finance"></a>Konfigurowanie wymagań wstępnych w Finance

### <a name="enable-the-feature-key-for-pending-vendor-invoices"></a>Włączanie klucza funkcji dla oczekujących faktur dostawcy

Wykonaj następujące kroki, aby włączyć funkcję dodawania szczegółów projektu w oczekujących wierszach faktury dostawcy.

1. W Finance przejdź do obszaru roboczego **Zarządzanie funkcjami**.
2. Na liście funkcji znajdź funkcję **Włączanie oczekujących faktur od dostawcy w Project Operations w scenariuszach zasobów magazynowanych/niemagazynowanych** i wybierz opcję **Włącz**.

### <a name="define-category-groups-and-project-categories-for-items"></a>Definiowanie grup kategorii i kategorii projektu dla elementów

Skonfiguruj co najmniej jedną grupę kategorii dla typu transakcji **Pozycja** i co najmniej jedną kategorię projektu przy użyciu tej grupy. Aby uzyskać więcej informacji, zobacz [Konfigurowanie kategorii projektu](../project-accounting/configure-project-categories.md#category-groups).

Przejrzyj profile kosztów i przychodów projektu oraz skonfiguruj konfigurację publikowania księgowego dla transakcji pozycji. Aby uzyskać więcej informacji, zobacz temat [Konfigurowanie rozliczania projektów rozliczanych](../project-accounting/configure-accounting-billable-projects.md).

### <a name="set-up-a-write-in-product"></a>Dodawanie produktu dopisanego

W Project Operations można rejestrować szacowanie materiałów i użycie produktów katalogu produktów skonfigurowanych w dostępnym katalogu produktów i dla produktów dodawanych. Używanie produktów dodatkowych wymaga jednego wydanego produktu skonfigurowanego w Finance. Wykonaj następujące kroki, aby skonfigurować produkt dodatkowy. Powtórz te kroki dla każdego podmiotu prawnego, który korzysta z Project Operations w sytuacjach produktów magazynowych/niemagazynowych.

1. W Finance wybierz pozycję **Zarządzanie informacjami o produkcie** > **Produkty** > **Wydane produkty** i wybierz opcję **Nowy**.
2. W polu **Typ produktu** wybierz opcję **Element**, a w polu **Podtyp produktu** wybierz opcję **Produkt**.
3. Wprowadź numer produktu (WRITEIN) i nazwę produktu (Write-in Product).
4. Wybierz grupę modeli elementów. Upewnij się, że dla wybranej grupy modeli elementów pole **Zasady magazynowe — produkt w magazynie** ma ustawioną wartość **False**.
5. Wybierz wartości w polach **grupy elementów**, **Grupa rozmiarów magzynowych** i **Śledzenie grupy rozmiarów**. Użyj opcji **Wymiar magazynu** tylko dla wartości **Witryna**, a w polu **Śledzenie wymiarów** wybierz opcję **Brak**.
6. Wybierz wartości w polu **Jednostka magazynowa**, **Jednostka zakupu** i **Jednostka sprzedaży**, a następnie zapisz zmiany.
7. Na karcie **Plan** ustaw domyślne ustawienia zamówienia, a następnie na karcie **Zapasy** ustaw domyślną witrynę i magazyn.
8. Przejdź do strony **Zarządzanie projektami i księgowanie** > **Konfiguracja** > **Zarządzanie parametrami projektów i księgowania** oraz otwórz **Project Operations w Dynamics 365 Dataverse**. 
9. Na karcie **Materiały** w polu **Produkt dodatkowy** wybierz utworzony produkt.
10. W środowisku Dataverse na mapie witryny otwórz encję **Produkty** i znajdź rekord do zapisu produktu. 
11. Otwórz szczegóły rekordu i ustaw stan produktu **Wycofane**. Ten stan produktu uniemożliwia przypadkowe użycie tego rekordu bezpośrednio w szacunkach materiałowych i dokumentach użycia.

### <a name="set-up-a-procurement-integration-account"></a>Załóż konto integracji zamówień

Konto integracji z integracją środowiska jest używane jako konto rozsyłania podczas publikowania oczekującej faktury dostawcy z wierszami w projekcie.

Gdy system publikuje oczekującą fakturę dostawcy, to konto jest używane dla kwoty kosztu projektu. Szczegóły faktury dostawcy są przetwarzane w Dataverse i tworzony jest odpowiedni projekt. Informacje rzeczywiste projektu są dodawane do arkusza integracji w Project Operations. Po zaksięgowaniu dziennika integracji, kwota zostaje wyczyszczona z konta integracji zamówień i zaksięgowana w kosztach projektu.

1. Aby skonfigurować konto integracji zamówień, przejdź do strony **Zarządzanie projektami i księgowanie** > **Konfiguracja** > **Zarządzanie parametrami projektów i księgowania** oraz otwórz **Project Operations w Dynamics 365 Dataverse**. 
2. Wybierz kartę **Materiały** i wybierz wartość w polu **Konto integracji zamówień**.

#### <a name="set-up-project-category-defaults-for-an-item"></a>Konfigurowanie domyślnych ustawień kategorii projektu dla elementu

1. W Finance przejdź do strony **Zarządzanie projektami i księgowanie** > **Konfiguracja** > **Zarządzanie parametrami projektów i księgowania** oraz otwórz **Project Operations w Dynamics 365 Dataverse**. 
2. Na karcie **Domyślne ustawienia kategorii projektu** w polu **Element** wybierz wartość. Ta kategoria projektu jest używana dla transakcji materiałowych, jeśli kategoria projektu nie zostanie ustawiona w rekordzie wartości rzeczywistych projektu.
