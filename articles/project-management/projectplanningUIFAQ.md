---
title: Rozwiązywanie problemów z pracą w siatce Zadanie
description: Ten artykuł zawiera informacje dotyczące rozwiązywania problemów podczas pracy z siatką zadań.
author: ruhercul
ms.date: 04/05/2022
ms.topic: article
ms.product: ''
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: e6ab4f34fe3f6732f7bef252f298671e07a3c3ca
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8911057"
---
# <a name="troubleshoot-working-in-the-task-grid"></a>Rozwiązywanie problemów z pracą w siatce Zadanie 


_**Dotyczy**: Project Operations dla scenariuszy opartych na zasobach/nieopartych na zaopatrzeniu, wdrażanie w wersji uproszczonej — od okazji do faktury pro forma, Project for the Web_

Siatka Zadanie obsługiwana przez rozwiązanie Dynamics 365 Project Operations jest hostowaną ramką iframe w programie Microsoft Dataverse. W wyniku tego zastosowania, aby uwierzytelnianie i autoryzacja działały poprawnie, muszą zostać spełnione określone wymagania. Ten artykuł opisuje typowe problemy, które mogą mieć wpływ na możliwość renderowania siatki lub zarządzania zadaniami w strukturze podziału pracy (WBS).

Do typowych problemów należą:

- Karta **Zadanie** w siatce Zadanie jest pusta.
- Po otwarciu projektu projekt nie zostanie załadowany, a interfejs użytkownika (UI) zatrzymał się na ładowaniu.
- Administrowanie uprawnieniami dla **Project for the Web**.
- Zmiany nie są zapisywane podczas tworzenia, aktualizowania lub usuwania zadania.

## <a name="issue-the-task-tab-is-empty"></a>Problem: karta Zadanie jest pusta

### <a name="mitigation-1-enable-cookies"></a>Rozwiązanie 1: włącz pliki cookie

Program Project Operations do renderowania struktury podziału pracy wymaga obsługi plików cookie innych firm. Jeśli pliki cookie innych firm nie są włączone, zamiast zadań, po wybraniu karty **Zadania** na stronie **Projekt** zobaczysz pustą stronę.

W przypadku przeglądarek Microsoft Edge lub Google Chrome poniższe procedury opisują sposób aktualizacji ustawień przeglądarki, aby włączyć pliki cookie innych firm.

#### <a name="microsoft-edge"></a>Microsoft Edge

1. Otwórz przeglądarkę Edge.
2. W prawym górnym rogu wybierz pozycję **wielokropka** (...), a następnie pozycję **Ustawienia**.
3. W obszarze **Pliki cookie i uprawnienia witryny** wybierz pozycję **Pliki cookie i dane witryny**.
4. Wyłącz **Blokuj wszystkie pliki cookie innych firm**.
5. Odśwież przeglądarkę. 

#### <a name="google-chrome"></a>Google Chrome

1. Otwórz przeglądarkę Chrome.
2. W prawym górnym rogu zaznacz trzy pionowe kropki,, a następnie wybierz **Ustawienia**.
3. W obszarze **Prywatność i zabezpieczenia** wybierz pozycję **Pliki cookie i inne dane witryny**.
4. Wybierz **Zezwalaj na wszystkie pliki cookie**.
5. Odśwież przeglądarkę. 

> [!NOTE]
> Jeśli zablokujesz pliki cookie innych firm, wszystkie pliki cookie i dane witryn z innych witryn zostaną zablokowane, nawet jeśli witryna jest dozwolona na liście wyjątków.

### <a name="mitigation-2-validate-the-pex-endpoint-has-been-correctly-configured"></a>Rozwiązanie 2: sprawdź, czy punkt końcowy PEX został poprawnie skonfigurowany

Project Operations wymaga, aby parametr projektu odwoływał się do punktu końcowego PEX. Ten punkt końcowy jest wymagany do komunikacji z usługą używaną do renderowania struktury podziału pracy. Jeśli parametr nie jest włączony, pojawi się błąd „Parametr projektu jest nieprawidłowy”. Aby zaktualizować punkt końcowy PEX, należy wykonać następujące kroki.

1. Dodaj pole **punkt końcowy PEX** do strony **Parametry projektu**.
2. Określ typ produktu, którego używasz. Ta wartość jest używana, gdy ustawiony jest punkt końcowy PEX. Po pobraniu typ produktu jest już zdefiniowany w PEX Endpoint. Zachowaj tę wartość.
3. Zaktualizuj pole za pomocą następującej wartości: `https://project.microsoft.com/<lang>/?org=<cdsServer>#/taskgrid?projectId=<id>&type=2`. W poniższej tabeli przedstawiono parametr typu, który ma być używany na podstawie typu produktu.

      | **Typ produktu**                     | **Typ parametru** |
      |--------------------------------------|--------------------|
      | Project for the Web w organizacji domyślnej   | typ=0             |
      | Project for the Web w organizacji o nazwie CDS | typ=1             |
      | Project Operations                   | typ=2             |

4. Usuń pole ze strony **Parametry projektu**.

### <a name="mitigation-3-sign-in-to-projectmicrosoftcom"></a>Rozwiązanie problemu 3: Zaloguj się w witrynie project.microsoft.com
W przeglądarce Microsoft Edge otwórz nową kartę, przejdź do okna project.microsoft.com i zaloguj się, używając roli użytkownika, za pomocą funkcji uzyskiwania dostępu do Project Operations.

## <a name="issue-the-project-doesnt-load-and-the-ui-is-stuck-on-the-spinner"></a>Problem: projekt nie zostanie załadowany, a interfejs użytkownika zatrzymał się na ładowaniu

Do celów uwierzytelniania należy włączyć wyskakujące okienka, aby siatka Zadanie się ładowała. Jeśli wyskakujące okienka nie są włączone, ekran zatrzyma się na kursorze ładowania. Na poniższej ilustracji pokazano adres URL z zablokowanym wyskakującym okienkiem na pasku adresu, przez co podczas próby ładowania strony pojawia się kursor ładowania. 

   ![Kursor ładowania i blokada wyskakujących okienek.](media/popupsblocked.png)

### <a name="mitigation-1-enable-pop-ups"></a>Rozwiązanie 1: włącz wyskakujące okienka

Gdy projekt zatrzyma się na kursorze ładowania, możliwe, że wyskakujące okienka są wyłączone.

#### <a name="microsoft-edge"></a>Microsoft Edge

Są dwa sposoby włączenia wyskakujących okienek w przeglądarce Edge.

1. W przeglądarce Edge wybierz powiadomienie w prawym górnym rogu przeglądarki.
2. Zaznacz opcję **Zawsze zezwalaj na wyskakujące okienka i przekierowywania z** określonego środowiska Dataverse.
 
     ![Wyskakujące okienka zablokowały okno.](media/enablepopups.png)

Alternatywnie możesz też wykonać jeden z następujących kroków.

1. Otwórz przeglądarkę Edge.
2. W prawym górnym rogu wybierz z **wielokropek** (...), a następnie wybierz uprawnienia witryny **Ustawienia** > **Uprawnienia strony** > **Wyskakujące okienka i przekierowania**.
3. Wyłącz **Wyskakujące okienka i przekierowanie** w celu blokowania wyskakujących okienek lub włącz, aby zezwolić na wyskakujące okienka na urządzeniu.
4. Po włączeniu wyskakujących okienek odśwież przeglądarkę. 

#### <a name="google-chrome"></a>Google Chrome
1. Otwórz przeglądarkę Chrome.
2. Przejdź do strony, na której są blokowane wyskakujące okienka.
3. Na pasku adresu wybierz opcję **Blokowanie wyskakujących okienek**.
4. Wybierz łącze do wyskakujących okienek, które chcesz wyświetlić.
5. Po włączeniu wyskakujących okienek odśwież przeglądarkę. 

> [!NOTE]
> Aby zawsze zobaczyć wyskakujące okienka dla witryny, zaznacz opcję **Zawsze zezwalaj na wyskakujące okienka i przekierowywanie z [witryny]**, a następnie wybierz opcję **Wykonane**.

## <a name="issue-3-administration-of-privileges-for-project-for-the-web"></a>Problem 3: administrowanie uprawnieniami dla Project for the Web

Project Operations są związane z zewnętrzną usługą planowania. Usługa wymaga przypisania użytkownikowi kilku ról, które zezwalają mu na odczytywanie i zapis danych w encjach związanych z SPP. Te encje obejmują zadania projektu, przydziały zasobów i zależności zadań. Jeśli użytkownik nie może wyrenderować SPP podczas przechodzenia na kartę **Zadania**, dzieje się tak prawdopodobnie dlatego, że **Projekt** dla **Project Operations** nie został włączony. Użytkownik może otrzymać błąd roli zabezpieczeń lub błąd związany z odmową dostępu.

### <a name="mitigation-1-validate-the-application-user-and-end-user-security-roles"></a>Rozwiązanie 1: sprawdź poprawność ról zabezpieczeń użytkownika aplikacji i użytkownika końcowego

1. Przejdź do **Ustawienia** > **Zabezpieczenia** > **Użytkownicy** > **Użytkownicy aplikacji**.  

   ![Czytnik aplikacji.](media/applicationuser.jpg)
   
2. Kliknij dwukrotnie rekord użytkownika aplikacji, aby sprawdzić, czy:

     - Użytkownik ma dostęp do projektu. Można to zrobić, sprawdzając, czy użytkownik ma rolę zabezpieczeń **Menedżera projektu**.
     - Użytkownik aplikacji Microsoft Project istnieje i jest poprawnie skonfigurowany.
 
3. Jeśli ten użytkownik nie istnieje, utwórz nowy rekord użytkownika. 
4. Wybierz opcję **Nowi użytkownicy**, zmień formularz wprowadzania na **Użytkownik aplikacji**, a następnie dodaj **Identyfikator aplikacji**.

   ![Dane użytkownika aplikacji.](media/applicationuserdetails.jpg)


## <a name="issue-4-changes-arent-saved-when-you-create-update-or-delete-a-task"></a>Problem 4: zmiany nie są zapisywane podczas tworzenia, aktualizowania lub usuwania zadania

Jeśli jedna lub więcej aktualizacji zostanie wprowadzonych w SPP, zmiany nie zostaną wprowadzone ani zapisane. W siatce harmonogramu pojawia się błąd z komunikatem „Nie można zapisać ostatnio wprowadzonej zmiany”.

### <a name="mitigation-1-validate-the-license-assignment"></a>Rozwiązanie 1: sprawdź poprawność przypisania licencji

1. Sprawdź, czy użytkownikowi przypisano poprawną licencję i czy usługa jest włączona w szczegółach planu usług licencji.  
2. Sprawdź, czy użytkownik może otworzyć **project.microsoft.com**.
    
### <a name="mitigation-2-validation-configuration-of-the-project-application-user"></a>Rozwiązanie 2: konfiguracja sprawdzania poprawności użytkownika aplikacji projektu
1. Sprawdź, czy utworzono użytkownika aplikacji projektu.
2. Zastosuj następujące role zabezpieczeń do użytkownika:
  
  - Użytkownik Dataverse lub użytkownik podstawowy
  - System Project Operations
  - System projektów
  - System podwójnego zapisu rozwiązania Project Operations. Ta rola jest wymagana dla wdrożenia aplikacji Project Operations dla zasobów/scenariuszy wdrażania nieopartych na zaopatrzeniu.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
