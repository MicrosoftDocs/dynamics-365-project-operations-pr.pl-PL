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
ms.openlocfilehash: c521fb4000b4856fc5c2fbf3275bf3b3e0dfa458
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/27/2021
ms.locfileid: "5950592"
---
# <a name="sample-data-installation-for-the-project-service-application"></a>Instalowanie danych przykładowych dla aplikacji Project Service

[!include [banner](../includes/psa-now-project-operations.md)]

W celu ułatwienia budowy własnych środowisk pokazowych, firma Microsoft dostarcza gotowe do pobrania pakiety danych przykładowych, które opisują możliwości aplikacji użytkownika. Istnieją dwa typy pakietów danych przykładowych:
- odwołanie/dane konfiguracji
- dane demonstracyjne (odwołanie/konfiguracja i dane transakcji, takie jak zlecenia pracy i projekty)

Pakiety danych przykładowych **odwołanie** można pobrać w trzech osobnych pakietach, więc można zainstalować dane tylko dla Project Service lub tylko dla Field Service, lub można zainstalować przykładowe dane dla obu aplikacji jednocześnie.

Pakiety danych przykładowych konfiguracja/odwołanie to:

- [**V902PSMasterData** - Project Service, tylko wersja 3.x](https://go.microsoft.com/fwlink/?linkid=2026540&clcid=0x409)

- [**V902FSMasterData** - Field Service, tylko wersja 8.x](https://go.microsoft.com/fwlink/?linkid=2026536&clcid=0x409)

- [**V902FPSMasterData** — Field Service 8.x i Project Service 3.x](https://go.microsoft.com/fwlink/?linkid=2026041&clcid=0x409)

Najnowszy pakiet danych **demo** to:

 - [**FPSDemoData** - Field Service 8.x and Project Service 3.x](https://aka.ms/fpsdemodatapackage)

   Instrukcje dotyczące instalacji różnią się nieco w użytkownikach do tworzenia i konfigurowania sekcji, ale reszta jest taka sama, jak w poprzednim [**wpisie na blogu**](https://aka.ms/fpsdemodatablog). Ten pakiet zawiera mniejszy zestaw danych demonstracyjnych, a cała operacja instalacji trwa około 3 godzin.

Te pakiety danych przykładowych są dostępne tylko w języku angielskim.

> [!IMPORTANT]
> **Nie można odinstalować danych przykładowych.** Pakiet te należy instalować wyłącznie w systemach demonstracyjnych, szkoleniowych lub testowych. Należy również zauważyć, że zainstalowanie dowolnego pakietu, a następnie instalowanie innego pakietu nie jest obsługiwane. (Innymi słowy, nie można zainstalować **FSMasterData** a następnie **PSMasterData**, i na odwrót.) Jeśli pojawi konieczność posiadania przykładowych danych dla obu aplikacji w dowolnym czasie w przyszłości, należy zainstalować pakiet **v902FPSMasterData**.

Podczas instalowania pakietów danych przykładowych proces instalowania wykonuje następujące operacje:

- Tworzy lub ustawia domyślne parametry dla Project Service, Field Service lub obu aplikacji (jeśli ma to zastosowanie).

- Importuje przykładowe dane dla aplikacji, takie jak zasoby, które można zarezerwować, role charakterystyczne dla poszczególnych aplikacji, sprzedaży i cenniki, jednostki organizacyjne, rekordy procesu sprzedaży i inne encje, aby zeprezentować kluczowe funkcje.  

Wraz z pakietem **dane demonstracyjne** otrzymujesz powyższe i dodatkowe dane dotyczące transakcji, takich jak zlecenia pracy i projekty.

Zastanawiasz się, jakie możliwości można zaprezentować przy użyciu przykładowych danych? Zobacz fikcyjny scenariusz Fabrikam Robotics w [Uwagi techniczne](#technical-notes).

Jeśli masz pytania dotyczące instalowania tych przykładowych pakietów danych [wyśij do nas wiadomość e-mail na adres fpsdemodata@microsoft.com](mailto:fpsdemodata@microsoft.com).

## <a name="requirements"></a>Wymagania

Protokół instalacji przyjmuje następujące informacje o wystąpieniu programu docelowego (organizacji):

- Język podstawowy to angielski a waluta podstawowa to Dolar Amerykański (USD, $)

- Organizacja nie ma już danych Project Service lub Field Service, lub ma tylko standardowe dane domyśle, które posiadają wszystkie nowe organizacje.

- Właściwa wersję aplikacji biznesowej jest już zainstalowana:
       
    - **Dla FPSDemoData or v902FPSMasterData:** Organizacja ma zainstalowaną wersję Field Service 8.x i Project Service 3.x.

    - **Dla v902PSMasterData:** Organizacja ma zainstalowaną wersję Project Service 3.x.

    - **For v902FSMasterData:** Organizacja ma zainstalowaną wersję Field Service 8.x.

> [!NOTE]
> Jeśli zachodzi konieczność zainstalowania przykładowych danych na istniejącym środowisku próbnym lub demonstracyjnym Project Service i Field Service które zawiera już dane (niezalecane), trzeba będzie zawiesić wstępne kontrole bezpieczeństwa wykonywane przez Instalatora. Aby uzyskać więcej informacji, zobacz Uwagi techniczne poniżej.

## <a name="prepare-for-installation"></a>Przygotuj do instalacji

Musisz uruchomić program instalacyjny na komputerze z najnowszą wersją systemu Windows (preferowany Windows 10).

Należy zaplanować, że komputer będzie podłączony do sieci a instalacja będzie trwała maksymalnie **1 godzinę** dla **dane konfiguracja/odwołanie**. (Zwykle instalacja trwa około 30 minut dla **FPSMasterData**, co obejmuje dane przykładowe dla obu aplikacji.) Dla **FPSDemoData**, instalacja potrwa około **3 godzin**.

Komputer powinien mieć wyłączoną funkcję wygaszacza ekranu. W przeciwnym razie poświadczenia sesji podczas instalacji mogą zostać utracone po uruchomieniu wygaszacza ekranu (chyba że zachowasz przez cały czas aktywną sesję).

> [!div class="mx-imgBorder"]
> ![Zrzut ekranu przedstawiający ustawienia wygaszacza ekranu, z wygaszaczem ekranu wyłączonym](media/sample-data-1.png)

## <a name="download-and-unpack"></a>Pobierz i rozpakuj

Instalator danych przykładowych Project Service i Field Service jest dystrybuowany jako samowyodrębniający się plik wykonywalny. Nazwy plików mogą się różnić w zależności od pakietu danych przykładowych, ale kroki są takie same, bez względu na to, jaki pakiet instalujesz.

Po pobraniu pakietu, uruchom plik .exe, a następnie zaakceptuj warunki, aby rozpakować skompresowany plik zip. Następnie musisz wyodrębnić zawartość pliku do folderu na komputerze.

W zależności od systemu operacyjnego i ustawień zabezpieczeń po rozpakowanie pliku zip może być konieczne wykonanie następujących czynności:

1. Znajdź i kliknij prawym przyciskiem myszy plik **FPSDemoData.dll** w folderze **v902FPSMasterData** / **PackageDeployer_FPSDemoData**.

2. Wybierz **Odblokuj**.

3. Wybierz **Zastosuj**.

4. Wybierz pozycję **OK**.


## <a name="create-or-configure-users"></a>Tworzenie i konfigurowanie użytkowników

Pakiet **FPSDemoData** wymaga sześciu użytkowników, a pakiet **FPSMasterData** wymaga jednego użytkownika. Zwróć się so właściwego po pakiet danych przykładowych.

## <a name="create-or-configure-users---setupreference-data-packages"></a>Tworzenie lub konfigurowanie użytkowników — / pakiety danych konfiguracja/odwołanie

Pakiet **FPSMasterData** jest przeznaczony do zainstalowania z jednym użytkownikiem nazywającym się Spencer Low z ustawieniami opisanymi w tym miejscu. Aby poprawnie zainstalować pakiet, użytkownik musi utworzyć (lub tymczasowo zmienić) użytkowników w swoim środowisku, aby odpowiadali oni nadchodzącej konfiguracji danych przykładowych.

Aby utworzyć lub skonfigurować użytkowników, przejdź do **Ustawienia** > **Zabezpieczenia** > **Użytkownicy**, i wykonaj następujące czynności:

1. Ustaw UserFullname = "Spencer Low" z nazwą użytkownika "spencerl" (**lowercase**) dla ról Menedżer projektu i Menedżer praktyk.

2. Wybierz użytkownika **Spencer Low**, a następnie wybierz **Zarządzaj rolami**. Znajdź i wybierz rolę **Administrator systemu**, a następnie wybierz **OK**, aby udzielić pełnych praw administratora dla użytkownika Spencer Low. Ten krok jest niezbędny w celu zapewnienia, że przykładowe rekordy są tworzone z własnością odpowiednich użytkowników co gwarantuje poprawne wypełnianie widoków.

3. Z pobranego pakietu musisz zaktualizować plik mapowania danych z adresami e-mail domyślnego kontekstu użytkownika. Aby to zrobić otwórz **PkgFolder**, następnie znajdź i otwórz plik **ImportUserMapFile.xml** w Notatniku (lub Visual Studio lub innym edytorze XML). Ustaw pole **DefaultUserToMapTo =** na adres e-mail użytkownika Spencer Low.

4. Jeśli nie używasz Spencer Low z nazwą użytkownika **spencerl**, musisz zaktualizować dodatkowy plik. Otwórz plik **DemoDataPreImportConfig.xml**, a następnie znajdź tag **userstocreateandconfigure**. Zaktualizuj tag **\<login\>** nazwą użytkownika swojego użytkownika Ludwik Kamiński. Aby uzyskać dodatkowe informacje, zobacz [Uwagi techniczne](#technical-notes).

## <a name="create-or-configure-users---demo-data-package"></a>Tworzenie i konfigurowanie użytkowników - pakiet danych demonstracyjnych

Pakiet danych demonstracyjnych wymaga sześciu użytkowników. Aby pakiet został prawidłowo zainstalowany wykonaj następujące czynności:

 1. Tworzenie i tymczasowa zmiana nazw istniejących użytkowników, aby odpowiadały przychodzącym przykładowym danym konfiguracji, przez przechodzenie do **Ustawienia** > **Zabezpieczenia** > **Użytkownicy**.
 
    Te role są potrzebne tylko dla prezentacji bazujących na osobach.  
    - Imię i nazwisko użytkownika = "David So" jako Technik usługi Field Service   
    - Imię i nazwisko użytkownika = "Jamie Reding" jako Dyspozytor usługi Field Service i Customer Sevice   
    - Imię i nazwisko użytkownika = "Molly Clark" jako Menedżer kont   
    - Imię i nazwisko użytkownika = "Spencer Low" jako Menedżer praktyk oraz Menedżer projektu  
    - Imię i nazwisko użytkownika = "Veronica Quek" jako Członek zespołu   
    - Imię i nazwisko użytkownika = "William Contoso"
  
2. Do potrzeb importu danych demonstracyjnych przypisz sześciu użytkowników powyżej roli Administratora, aby przykładowe rekordy zostały zaimportowane poprawnie. 

3. Otwórz **PkgFolder** i znajdź i otwórz **ImportUserMapFile.xml**. Zaktualizuj pola **Nowy=** do adresów e-mail odpowiednich użytkowników w systemie.

   > [!div class="mx-imgBorder"]
   > ![Zrzut ekranu UserMapFile](media/sample-data-7.png)

4. Jeśli użytkownik "Spencer Low" ma Identyfikator użytkownika inny niż **"spencerl"**, musisz zaktualizować dodatkowy plik. Otwórz **DemoDataPreImportConfig.xml**, a następnie znajdź znacznik **userstocreateandconfigure**. Zaktualizuj znacznik **\<login\>** za pomocą loginId (wielkość liter jest uwzględniana). 

5. Kalendarz pierwszego użytkownika (w znaczniku **userstocreateandconfigure**) jest używany do wypełnienia godzin pracy dla wszystkich zasobów, które można zarezerwować przy importowaniu danych demonstracyjnych. Przejdź do **Ustawienia** > **Zabezpieczenia** > **Użytkownicy**, znajdź użytkownika "Spencer Low" i otwórz opcję "Godziny pracy". Edytuj istniejące godziny pracy, wybierając opcję **Cały cykliczny harmonogram tygodniowy - od początku do końca**. Zapewnij **Godziny pracy są ustawione na 8:00 - 17:00 (9 godzin), od poniedziałku do piątku dla strefy czasowej ustawionej na czas pacyficzny (Stany Zjednoczone i Kanada)**. Jest to niezbędne do zapewnienia, że tablice Projekt i Harmonogram prezentują dane zgodne z oczekiwaniami.

**Rekomendacja:** Rozważ utworzenie kopii zapasowej organizacji teraz, na wypadek wystąpienia konieczność powrotu do punktu początkowego, jeśli wystąpią problemy podczas na instalowania danych przykładowych. Aby uzyskać więcej informacji, zobacz [Kopia zapasowa i przywracanie wystąpień](/dynamics365/customer-engagement/admin/backup-restore-instances).

## <a name="run-the-package-deployer"></a>Uruchom Package Deployer

1. Znajdź i uruchom **PackageDeployer.exe** w folderze **v902FPSMasterData** LUB **PackageDeployer_FPSDemoData**.

2. Zaakceptuj postanowienia.

3. W następnym oknie:

   a. Wybierz typ wdrożenia **Office 365**.

   b. Użyj użytkownika i hasła użytkownika administrator systemu skonfigurowanego w "Tworzenie i konfigurowanie użytkowników" ("Spencer Low" z nazwą użytkownika "spencerl").

   c. Upewnij się, że zaznaczono **Wyświetl listę dostępnych organizacji**.

      > [!div class="mx-imgBorder"]
      > ![Zrzut ekranu przedstawiający okno Package Deployer z zaznaczonym „Wyświetl listę dostępnych organizacji”](media/sample-data-2.png)

4. Wybierz organizację, w której chcesz zainstalować przykładowe dane.

5. Wybierz **Dalej** aż pojawi się dialog **Instalator danych pokazowych**.

   > [!div class="mx-imgBorder"]
   > ![Zrzut ekranu przedstawiający okno statusu Instalatora danych przykładowych](media/sample-data-3.png)

6. Zanim przejdziesz dalej, pamiętaj, że instalowanie danych przykładowych może trwać maksymalnie godzinę (zwykle ~ 10 min). Należy się upewnić, że komputer pozostaje włączony i podłączony do sieci w trakcie procesu instalowania, i że sesja pozostaje aktywna.   

7. Kiedy jesteś gotowy, kliknij **Dalej**, aby rozpocząć proces instalacji przykładowych danych. Po załadowaniu przykładowych danych, kliknij **Zakończ**.

## <a name="verify-the-sample-data-installation"></a>Zweryfikuj prawidłowość instalacji danych przykładowych

Sprawdzając upewnij się, że liczba rekordów i typy encji wymienione w scenariuszu fikcyjnym Fabrikam Robotics wydają się być zgodne z oczekiwaniami.

Po całkowitym pobraniu danych przykładowych zaloguj się jako użytkownik Spencer Low i potwierdzić następujące informacje:

- Jeśli zainstalowana jest aplikacja Project Service, przejdź do **Project Service** > **Ustawienia** > **Cenniki**. Potwierdź, czy istnieją stawki kosztów i rachunków, w odpowiedniej walucie, dla każdego kraju/regionu w zestawie danych.

- Jeśli zainstalowana jest aplikacja Project Service, przejdź do **Universal Resource Scheduling** > **Ustawienia** > **Jednostki organizacyjne**. Upewnij się, że lista kosztów własnych z odpowiednią walutą została skojarzona z każdą jednostką organizacyjną (z wyjątkiem wpis dotyczących miast). Jeżeli jakichkolwiek brakuje znajdź i powiąż odpowiedni cennik kosztów własnych.

- Jeśli zainstalowana jest aplikacja Field Service, przejdź do **Project Service** > **Ustawienia** > **Cenniki**. Upewnij się, istnieją stawki kosztów i rachunków. Przejdź do **Field Service** > **Ustawienia** > **Cenniki** i sprawdź, czy istnieją stawki kosztów i rachunków, w odpowiedniej walucie, dla każdego kraju/regionu w zestawie danych.

  > [!div class="mx-imgBorder"]
  > ![Zrzut ekranu przedstawiający aktywne cenniki](media/sample-data-4.png)

  > [!div class="mx-imgBorder"]
  > ![Zrzut ekranu przedstawiający aktywne jednostki organizacyjne](media/sample-data-5.png)

## <a name="technical-notes"></a>Uwagi techniczne

Poniżej znajduje się więcej szczegółów technicznych dotyczących instalacji tych danych.

### <a name="installing-sample-data-on-top-of-existing-data-not-recommended"></a>Instalowanie danych przykładowych na istniejących danych (niezalecane)

Uwaga: Jeśli zachodzi konieczność zainstalowania przykładowych danych na istniejącym środowisku próbnym lub demonstracyjnym Field Service i Project Service które zawiera już dane (niezalecane), trzeba będzie zawiesić wstępne kontrole bezpieczeństwa wykonywane przez Instalatora.

W tym celu należy przejść do folderu **PkgFolder**, aby znaleźć i otworzyć plik **DemoDataPreImportConfig.xml** z danymi Notepad (lub inny edytor XML).

Znajdź następujące wartości, a następnie zmień ustawienie z true na false:

```alias
<TerminateOnPreCheckFailure>true</TerminateOnPreCheckFailure>
```

Ta zmiana powoduje, że program instalacyjny pomija niektóre testy bezpieczeństwa, w tym:

- Potwierdzenie, że jest nie więcej niż jeden aktywny rekord **Jednostka organizacyjna**, a następnie zmień jego nazwę na **Fabrikam USA**.

- Potwierdzenie, że jest nie więcej niż jeden aktywny rekord **Szablon pracy**.

- Potwierdź, że jest nie więcej niż jeden aktywny rekord **Parametr projektu**, a następnie zmień jego nazwę na **Parametry**.

### <a name="configuration-components"></a>Składniki konfiguracji

Istnieje wiele innych składników konfiguracji, w tym pliku konfiguracji sprzed importu. Dla użytkowników techniczne tych należą:

- **\<RequiredSolutions\>** określa wstępne instalacje rozwiązania oraz ich numery wersji.

- **\<InstallSampleData\>** określa, czy standardowe dane przykładowe dla aplikacji zostały zainstalowane.

    - false — pomija instalację tych wbudowanych danych (co można usunąć)

    - true — instaluje wbudowane dane z jednoczesną instalacją przykładowych danych FS i PSA

- **\<PreImportDataCollection\>** określa stałe Mapy danych i skojarzone Rekordy, aby można było je zaimportować przed zainstalowaniem głównych danych przykładowych.

- **\<EntitiesToEnableScheduling\>** określa encje, które powinny być włączone dla Rezerwowanie w aplikacji Microsoft Dynamics Scheduling (alias Universal Resource Scheduling).

- **\<UsersToCreateAndConfigure\>** określa zasoby, które można zarezerwować, które będą tworzone (jeśli jeszcze nie istnieją) zanim nastąpi zaimportowanie przykładowych danych. Należy pamiętać, że przykładowe dane Zasoby, które można zarezerwować systemu źródłowego odpowiadają rekordom Zasoby, które można zarezerwować systemu docelowego jeśli chodzi o pełną nazwę i login każdego zasobu. Z tego powodu NIE można zmieniać nazw w tym pliku konfiguracji wstępnej, chyba że wcześniej zaimportujesz dane przykładowe do systemu docelowego przy użyciu tych nazw, a następnie zmienisz nazwę Zasoby, które można zarezerwować na żądaną nazwę wraz z rekordami Włączeni użytkownicy, a następnie wyeksportujesz dane ponownie do zaimportowania do systemu przeznaczenia (aktualizując odpowiednio stare i nowe wpisy **ImportUserMapFile.xml**).

- **\<PluginsToDisable\>** określa bardzo zindywidualizowanej dodatki plug-in pozycji, które muszą być wyłączone podczas importowania danych przykładowych i następnie ponownie włączone.

### <a name="fabrikam-robotics-fictitious-scenario"></a>Fikcyjny scenariusz Fabrikam Robotics

Pakiety danych przykładowych typu odwołanie Field Service i Project Service instalują **Rozwiązanie Fabrikam Manufacturing Master Data (v3.0.0.0)**, wraz z około 4000 rekordów i około 40 różnymi encjami. Pakiety przykładowych danych dla Field Service lub Project Service zawierają podzbiór danych przykładowych **v902FPSMasterData** dla tej aplikacji. Pakiet **Dane demonstracyjne** instaluje rozwiązanie **Rozwiązane Fabrikam Manufacturing Demo Data (v3.0.0.7)** z około 22000 rekordów w 148 encjach.

Fikcyjna firma, Fabrikam Robotics, jest producentem robotów z linii produkcyjnej urządzeń elektronicznych i jest znana z jakości produktów, innowacji oraz obsługi klienta, w tym planowania instalacji, implementacji i bieżących prac konserwacyjnych. Firma Fabrikam ma swoją centralę w Stanach Zjednoczonych (Fabrikam US), i prowadzi działania związane z projektami we Francji, w Indiach, Wielkiej Brytanii i Szwajcarii.

Operacje usługi Field Service skupiają się na terenie Stanów Zjednoczonych, zwłaszcza w okolicach Seattle. Firma skupia się na wykorzystaniu połączenia Internet rzeczy (IoT) do monitorowania wydajności zasobu klienta i dostarczania coraz aktywniejszych usług sieciowych.

Omówienie przykładowych danych:

- Typowe elementy danych przykładowych (uwzględnione w obu aplikacjach)

    - 1 użytkownik

    - 71 kont

    - 137 kontaktów

    - Różne typy transakcji i kategorii

    - 50 produktów i 1 cennik produktów

    - 14 list kosztów własnych

    - 31 właściwości (umiejętności zasobu) w 2 modelach klasyfikacja o 3 poziomach (wartości ocen)

- Project Service

    - 8 jednostek organizacyjnych

    - 6 poziomów wykorzystania dla poszczególnych ról

    - 2,8k + specyfikacje dla poszczególnych ról

- Rozwiązanie Field Service

    - 4 obszary

    - 5 typów zleceń pracy

    - 22 zasoby klienta

    - 9 typów zgłoszeń z charakterystyka skojarzonego zasobu (9), usługi (13) i zadań serwisowych (13)
   
Pakiet **Dane demonstracyjne** instaluje około 179 zleceń pracy, 12 projektów i skojarzonych z nim danych transakcji. 

### <a name="change-the-work-hours-for-sample-resources"></a>Zmienianie godzin pracy dla zasobów przykładowych

Domyślnie wszystkie zasoby, które można zarezerwować, mają ustawiony kalendarz pracy na 24 godziny.

Jeśli zachodzi konieczność zmiany godzin pracy dla przykładowych zasobów, które można zarezerwować, przejdź do **Universal Resource Scheduling** > **Planowanie** > **Zasoby**.

Wybierz użytkownika (na przykład Spencer Low) i zmień godzin pracy użytkownika Spencer na godziny, które chcesz zastosować do wielu użytkowników. Przejdź do **Universal Resource Scheduling** > **Ustawienia** > **Szablony godzin pracy** i edytuj rekord **Domyślny szablon pracy**. W polu **Szablon zasobu** wybierz użytkownika z godzinami pracy, które chcesz zastosować dla innych zasobów. Przejdź do **Universal Resource Scheduling** > **Planowanie** > **Zasoby** > **Aktywne zasoby, które można zarezerwować**. Wybierz zasoby, które chcesz zmienić, a następnie wybierz **Ustaw kalendarz**. Z listy rozwijanej **Szablon pracy** wybierz szablon **Domyślne godziny pracy** lub inny szablon z poprawnym zasobem szablonu. Po przejściu do tablicy harmonogramu, powinieneś zobaczyć, że zasoby mają zaktualizowane godziny pracy.

> [!div class="mx-imgBorder"]
> ![Zrzut ekranu przedstawiający aktywne zasoby, które można zarezerwować](media/sample-data-6.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]