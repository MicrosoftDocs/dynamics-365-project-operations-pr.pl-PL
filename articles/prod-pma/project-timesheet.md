---
title: Aplikacja mobilna grafik projektu
description: Ten artykuł zawiera informacje o aplikacji mobilnej Microsoft Dynamics 365 Project Timesheet. Aplikacja mobilna Project Timesheet umożliwia użytkownikom przesyłanie i zatwierdzanie kart czasu pracy dla projektów na ich urządzeniu przenośnym.
author: abruer
ms.date: 06/29/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: johnmichalak
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 10
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 730ed36841d07df60e8a8f343126209f0edcc593
ms.sourcegitcommit: 5c971b15295046b3c92ff6638dd1352129f1c390
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/01/2022
ms.locfileid: "9110988"
---
# <a name="project-timesheet-mobile-application"></a>Aplikacja mobilna grafik projektu

[!include [banner](../includes/banner.md)]

## <a name="overview"></a>Omówienie

Aplikacja mobilna Microsoft Dynamics 365 Project Timesheet umożliwia użytkownikom przesyłanie i zatwierdzanie kart czasu pracy dla projektów na ich urządzeniu przenośnym (iPhone lub Android). Tej aplikacja mobilna zapewnia dostęp do funkcji karty czasu pracy w obszarze zarządzania projektami i księgowania w Dynamics 365 Finance. Zwiększa ona wydajność i efektywność użytkowników oraz ułatwia wprowadzanie i zatwierdzanie grafików projektów.

## <a name="download-and-install-the-mobile-app"></a>Pobierz i zainstaluj aplikację mobilną

Pobierz i zainstaluj aplikację mobilną Microsoft Dynamics 365 Project Timesheet dla systemu Android lub iPhone ze sklepu mobilnego na swoje urządzenie.

## <a name="enable-the-app"></a>Włączanie aplikacji 

W Finance musi być włączona aplikacja mobilna Project Timesheet. Aby włączyć tę funkcję, przejdź do **Parametry Zarządzanie projektami i księgowanie \> Grafik** i wybierz parametr **Włącz Microsoft Dynamics 365 Project Timesheet**.

### <a name="resolve-sign-in-issues"></a>Rozwiązywanie problemów z logowaniem

**Problem:** Podczas logowania do aplikacji mobilnej Project Timesheet użytkownicy otrzymują komunikat o błędzie informujący, że „nie mogą uzyskać dostępu do aplikacji '2bc50526-cdc3-4e36-a970-c284c34cbd6e' w tej dzierżawie”.

**Problem:** Podczas logowania do aplikacji mobilnej Project Timesheet użytkownicy otrzymują błąd podobny do jednego z następujących przykładów:

- „AADSTS50020: Konto użytkownika „[nazwa użytkownika]” od dostawcy tożsamości „https://sts.windows.net/[identyfikator aplikacji]” nie istnieje w dzierżawie „[identyfikator dzierżawy]” i nie może uzyskać dostępu do aplikacji „[aplikacja id]” w tym najemcy”.
- "Wybrane konto użytkownika nie istnieje w dzierżawie" [identyfikator dzierżawy]" i nie może uzyskać dostępu do aplikacji "[identyfikator aplikacji]" w tej dzierżawie."

**Wyjaśnienie:** Te problemy są powodowane przez zmianę w Azure Active Directory (Azure AD) z maja 2022 r. i powiązaną z użytkownikami zewnętrznymi. Ponieważ ta zmiana nie została wprowadzona w aplikacjach finansowych i operacyjnych, może mieć wpływ na klientów korzystających z dowolnej wersji platformy lub aplikacji.

**Poprawka:** Wszyscy użytkownicy zewnętrzni muszą zostać zaproszeni do dzierżawy za pośrednictwem usługi Azure AD. Aby uzyskać więcej informacji, zobacz [Zapraszanie użytkowników korzystających ze współpracy B2B z Azure Active Directory](/power-platform/admin/invite-users-azure-active-directory-b2b-collaboration).

## <a name="sign-in-to-the-app"></a>Zaloguj się do aplikacji

1.  Uruchom aplikację na swoim urządzeniu mobilnym.

2.  Wprowadź adres URL Finance.

3.  Po pierwszym zalogowaniu się jest wyświetlany monit o podanie nazwy użytkownika i hasła. Wprowadź poświadczenia.

4. Użytkownik zostanie zalogowany w firmie domyślnej.

## <a name="submit-a-project-timesheet"></a>Przesyłanie grafiku projektu

W aplikacji można utworzyć i przesłać grafik z projektu. Istnieje możliwość utworzenia nowego grafiku na podstawie informacji z poprzedniej karty czasu pracy, zapisanych wierszy lub przydziałów projektu. Jeśli użytkownik został wyznaczony jako pełnomocnik, może również wprowadzić grafik innego pracownika. Aby utworzyć grafik jako pełnomocnik, wybierz przycisk **Menu**, a następnie wybierz nazwę zasobu.

Strona grafiku spowoduje utworzenie nowego grafiku dla okresu w grafiku w oparciu o bieżącą datę. Zostanie wyświetlony tydzień roboczy. Jeśli okres grafiku obejmuje wiele tygodni, można z kart tygodnia roboczego wybrać inny tydzień roboczy.
Jeśli istnieje grafik dla bieżącej daty, zostanie wyświetlona. Jeśli zachodzi konieczność utworzenia nowego grafiku w innym okresie na karcie czasu pracy, należy wybrać przycisk **Menu**, a następnie wybrać **Nowy grafik**.

Aby wprowadzić informacje o projekcie, kliknij akcję **Dodaj czas** lub akcję **Kopiuj czas z**. Akcja **Kopiuj czas z** powoduje skopiowanie informacji o wierszu projektu, ale nie jego godzin. W menu **Kopiuj czas z** dostępne są następujące opcje:

- **Skopiowanie z istniejącego grafiku** - skopiowanie wierszy grafiku z istniejącego grafiku.

- **Skopiuj z Ulubione** - Utwórz nowe wiersze karty czasu pracy, korzystając z ustawień karty czasu pracy wybranych jako ulubione.

- **Kopiowanie z przypisania** - Tworzenie nowych wierszy grafiku z przypisanych projektów.

Wyświetlane informacje o projekcie są zależne od parametrów mobilnych zdefiniowanych na stronie **Parametry Zarządzanie projektami i księgowanie**.

W polu **Firma** wybierz firmę, dla której wykonana została praca nad projektem. Pole **Firma** jest dostępne tylko wtedy, gdy dla Twojej firmy włączono obsługę międzyfirmowego grafiku.

Wybierz klienta skojarzonego z projektem dla grafiku. W przypadku początkowej wersji na Android, wprowadzanie przez klienta nie jest obsługiwane, ponieważ należy najpierw wybrać projekt. W przypadku wcześniejszego wybrania projektu pole **Klient** zostanie wypełnione automatycznie.

W polu **Projekt** wybierz projekt, dla którego wprowadzany jest czas. Pole **Klient** jest wypełniane automatycznie.

Podczas wyszukiwania klienta i projektu są włączane wyszukiwanie na poziomie zarówno klientów, jak i projektów.

W zależności od potrzeb należy wybrać informacje w polach **Kategoria**, **Działanie**, **Właściwość wiersza**, **Grupa podatku** i **Grupa podatku dla towaru**. Te pola mogą zostać zastąpione.

W polu **Właściwości wiersza** zostanie ustawiona wartość domyślna, która jest oparta na parametrach zarządzania projektami i księgowaniu. Kiedy parametry projektu/kategorii i kategorii/zasobu są włączone, wartość **Właściwości wiersza** zostanie ustawiona na wartość domyślną, która została zdefiniowana dla tego sprawdzania poprawności. Kiedy parametry projektu/kategorii i kategorii/zasobu nie są włączone, wartość **Właściwości wiersza** będzie domyślna zgodnie z polem **Włącz domyślną właściwość wiersza** na stronie **Parametry Zarządzanie projektami i księgowanie**. Wartość **Właściwości wiersza** może zostać zastąpiona.

Wybierz dzień, aby dodać godzinę. Wprowadź liczbę godzin przepracowanych w każdym dniu.

Aby dodać komentarze dotyczące wprowadzanych godzin, kliknij przycisk **Dodaj komentarze**, a następnie wprowadź komentarze odbiorcy wewnętrznego, odbiorcy klienta lub oba te elementy.
Komentarze wewnętrzne mogą być wyświetlane przez kierowników projektów. Komentarze klienta są uwzględnione na fakturach.

Aby zapisać wiersz jako ulubiony, zaznacz pole wyboru, a następnie kliknij pozycję **Zapisz jako ulubioną**.

W aplikacji mobilnej nie są dostarczane żadne funkcje dotyczące wymiarów finansowych i załączników.

Kontynuuj dodawanie wierszy projektów w celu wykonania grafiku.

Kliknij przycisk **Prześlij**, aby wysłać grafik do przepływu pracy zatwierdzania.

## <a name="review-timesheets"></a>Przeglądanie grafików

Lista grafików, które należy przejrzeć, jest dostępna w menu. Ta opcja jest dostępna tylko wtedy, gdy została wyznaczona osoba zatwierdzająca przepływ pracy. Obsługiwane jest zarówno zatwierdzanie nagłówków, jak i wierszy. Zatwierdzanie na poziomie wiersza umożliwia oznaczenie jednego lub większej liczby wierszy do zatwierdzenia. Po przejrzeniu informacji z grafiku kliknij przycisk **Zatwierdź**, **Deleguj** lub **Wróć**, aby kontynuować przepływ pracy.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
