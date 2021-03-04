---
title: Rozwiązywanie problemów z pracą w siatce Zadanie
description: Ten temat zawiera informacje na temat rozwiązywania problemów potrzebne podczas pracy w siatce Zadanie.
author: ruhercul
manager: tfehr
ms.date: 01/19/2021
ms.topic: article
ms.product: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 89bbad62c2a0a5693a57cf5c9a812ab644486469
ms.sourcegitcommit: c9edb4fc3042d97cb1245be627841e0a984dbdea
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/19/2021
ms.locfileid: "5031550"
---
# <a name="troubleshoot-working-in-the-task-grid"></a>Rozwiązywanie problemów z pracą w siatce Zadanie 

_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_

W tym temacie opisano, jak rozwiązać problemy, które mogą wystąpić podczas pracy z zarządzaniem kosztami.

## <a name="enable-cookies"></a>Włącz obsługę plików cookie

Project Operations wymaga włączenia plików cookie innych firm w celu renderowania struktury podziału pracy. Jeśli pliki cookie innych firm nie są włączone, zamiast zadań, po wybraniu karty **Zadania** na stronie **Projekt** zobaczysz pustą stronę.

![Pusta karta w przypadku, gdy nie są włączone pliki cookie innych firm](media/blankschedule.png)


### <a name="workaround"></a>Rozwiązanie
W przypadku przeglądarek Microsoft Edge lub Google Chrome poniższe procedury opisują sposób aktualizacji ustawień przeglądarki, aby włączyć pliki cookie innych firm.

#### <a name="microsoft-edge"></a>Microsoft Edge

1. Otwórz przeglądarkę Edge.
2. W prawym górnym rogu wybierz pozycję **wielokropka** (...), a następnie pozycję **Ustawienia**.
3. W obszarze **Pliki cookie i uprawnienia witryny** wybierz pozycję **Pliki cookie i dane witryny**.
4. Wyłącz **Blokuj wszystkie pliki cookie innych firm**.

#### <a name="google-chrome"></a>Google Chrome

1. Otwórz przeglądarkę Chrome.
2. W prawym górnym rogu zaznacz trzy pionowe kropki,, a następnie wybierz **Ustawienia**.
3. W obszarze **Prywatność i zabezpieczenia** wybierz pozycję **Pliki cookie i inne dane witryny**.
4. Wybierz **Zezwalaj na wszystkie pliki cookie**.

> [!IMPORTANT]
> Jeśli zablokujesz pliki cookie innych firm, wszystkie pliki cookie i dane witryn z innych witryn zostaną zablokowane, nawet jeśli witryna jest dozwolona na liście wyjątków.

## <a name="pex-endpoint"></a>Punkt końcowy systemu PEX

Project Operations wymaga, aby parametr projektu odwoływał się do punktu końcowego PEX. Ten punkt końcowy jest wymagany do komunikacji z usługą używaną do renderowania struktury podziału pracy. Jeśli parametr nie jest włączony, pojawi się błąd „Parametr projektu jest nieprawidłowy”. 

### <a name="workaround"></a>Rozwiązanie
 ![Pole PEX Endpoint w parametrze projektu](media/projectparameter.png)

1. Dodaj pole **punkt końcowy PEX** do strony **Parametry projektu**.
2. Zaktualizuj pole za pomocą następującej wartości: `https://project.microsoft.com/<lang>/?org=<cdsServer>#/taskgrid?projectId=\<id>&type=2`
3. Usuń pole ze strony **Parametry projektu**.

## <a name="privileges-for-project-for-the-web"></a>Uprawnienia dotyczące projektu w sieci Web

Project Operations są związane z zewnętrzną usługą planowania. W usłudze jest wymagane przypisanie użytkownikowi kilku ról do odczytu i zapisu encji związanych z strukturą zabezpieczeń pracy. Te encje obejmują zadania projektu, przydziały zasobów i zależności zadań. Jeśli użytkownik nie może wyrenderować struktury podziału pracy po przejściu do karty **Zadania**, prawdopodobnie jest to spowodowane tym, że nie włączono programu Project for Project Operations. Użytkownik może otrzymać błąd roli zabezpieczeń lub błąd związany z odmową dostępu.


## <a name="workaround"></a>Rozwiązanie

1. Przejdź do **Ustawienia > Zabezpieczenia > Użytkownicy > Użytkownicy aplikacji**.  

   ![Czytnik aplikacji](media/applicationuser.jpg)
   
2. Kliknij dwukrotnie rekord użytkownika aplikacji, aby sprawdzić, czy:

 - Użytkownik ma dostęp do projektu. Weryfikacja ta zwykle polega na upewnieniu się, że użytkownik ma rolę zabezpieczeń **Menedżer projektu**.
 - Użytkownik aplikacji Microsoft Project istnieje i jest poprawnie skonfigurowany.
 
3. Jeśli ten użytkownik nie istnieje, możesz utworzyć nowy rekord użytkownika. Wybierz **Nowi użytkownicy**. Zmień formularz wprowadzania na **Użytkownik aplikacji**, a następnie dodaj **Identyfikator aplikacji**.

   ![Dane użytkownika aplikacji](media/applicationuserdetails.jpg)

4. Sprawdź, czy użytkownikowi przypisano poprawną licencję i czy usługa jest włączona w szczegółach planu usług licencji.
5. Sprawdź, czy użytkownik może otworzyć project.microsoft.com.
6. Sprawdź za pomocą parametrów projektu, czy system wskazuje prawidłowy punkt końcowy projektu.
7. Sprawdź, czy utworzono użytkownika aplikacji projektu.
8. Zastosuj następujące role zabezpieczeń do użytkownika:

  - Użytkownik Dataverse
  - System Project Operations
  - System projektów

## <a name="error-when-updating-the-work-breakdown-structure"></a>Błąd podczas aktualizacji struktury podziału pracy

Po wprowadzeniu co najmniej jednej aktualizacji struktury podziału pracy zmiany ostatecznie kończą się niepowodzeniem i nie są zapisywane. W siatce harmonogramu pojawia się błąd informujący, że „Nie można zapisać ostatniej wprowadzonej zmiany”.

### <a name="workaround"></a>Rozwiązanie

1. Sprawdź, czy użytkownikowi przypisano poprawną licencję i czy usługa jest włączona w szczegółach planu usług licencji.
2. Sprawdź, czy użytkownik może otworzyć project.microsoft.com.
3. Sprawdź, czy system wskazuje prawidłowy punkt końcowy projektu.
4. Sprawdź, czy utworzono użytkownika aplikacji Project.
5. Zastosuj następujące role zabezpieczeń do użytkownika:
  
  - Użytkownik Dataverse lub grupa użytkowników
  - System Project Operations
  - System projektów
  - System podwójnego zapisu Project Operations (ta rola jest wymagana w przypadku wdrażania scenariusza dotyczącego zasobów/braku zapasów w ramach Project Operations).


[!INCLUDE[footer-include](../includes/footer-banner.md)]