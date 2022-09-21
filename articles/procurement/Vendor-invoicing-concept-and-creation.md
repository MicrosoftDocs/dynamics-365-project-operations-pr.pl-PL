---
title: Tworzenie faktur od dostawcy
description: W tym artykule opisano pojęcia faktur dostawcy, objaśniono sposób tworzenia ich w Microsoft Dynamics 365 Project Operations.
author: suvaidya
ms.date: 9/12/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: suvaidya
ms.openlocfilehash: 7f6c1ec46f23b6823734b28755b80ced4e3f9325
ms.sourcegitcommit: 60a34a00e2237b377c6f777612cebcd6380b05e1
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 09/13/2022
ms.locfileid: "9475434"
---
# <a name="create-vendor-invoices"></a>Tworzenie faktur od dostawcy

_**Zastosowane do:** Project Operations dla zasobów/scenariuszy nieopartych na zaopatrzeniu_

Aby skorzystać z funkcji opisanych w tym artykule, należy włączyć funkcję **Włącz przetwarzanie wartości rzeczywistych dotyczących podwykonawców z Project Operations dla scenariuszy opartych na zasobach** w obszarze roboczym **Zarządzanie funkcją**.

Fakturowanie dostawcy w Microsoft Dynamics 365 Project Operations może być wykorzystywane do rejestrowanie kosztów związanych z dostarczaniem usług i/lub materiałów w ramach projektu wykonywanego przez dostawców.

Jeśli usługi i/lub materiały są podwykonawcy świadczone dostawcy, podwykonawca reprezentuje umowę kontraktową z tym dostawcą. Gdy dostawca zapewnia usługi, ponieważ materiały są odbierane i wykorzystywane do zadań projektów, koszty są rejestrowane w ramach projektu. Dostawca może następnie okresowo wysyłać faktury. Te faktury są sprawdzane i dopasowywane do kosztów zarejestrowanych w projekcie. Po zakończeniu procesu weryfikacji faktura dostawcy jest potwierdzana i wystawiana do płatności.

## <a name="scenarios-for-use"></a>Scenariusze użycia

Faktury dostawcy w Project Operations mogą być używane do obsługi dwóch różnych scenariuszy:

- Klienci korzystają z pełnych funkcji obsługi podrzędnej.
- Klienci nie używają pełnych funkcji obsługi podrzędnej, ale chcą mieć ujednolicony widok kosztów w ramach projektów w Project Operations.

### <a name="customers-use-the-full-subcontracting-experiences"></a>Klienci korzystają z pełnych funkcji obsługi podrzędnej

Faktury od dostawcy mogą weryfikować i dopasować wpisy czasu, użycie materiałów oraz wpisy wydatków, które odwołują się do składników kontraktów podwykonawców, a także do pozycji faktury dostawcy. Ten proces może służyć do sprawdzania rzetelności wierszy faktur dostawcy. Po zakończeniu procesu weryfikacji i zweryfikowaniu faktury dostawcy system wycofa wartości rzeczywiste zarejestrowane w zatwierdzonych dziennikach czasu, wydatków i materiałów oraz utworzy nowe wartości rzeczywiste kosztów przy użyciu wierszy faktur dostawcy.

### <a name="customers-dont-use-the-full-subcontracting-experiences-but-want-to-have-a-unified-view-of-costs-on-projects-in-project-operations"></a>Klienci nie używają pełnych funkcji obsługi podrzędnej, ale chcą mieć ujednolicony widok kosztów w ramach projektów w Project Operations

W przypadku śledzenia procesu podwykonawcy w systemie innych firm można zarejestrować koszty z systemu innych firm do Project Operations, tworząc faktury dostawców, które nie odwołują się do kontraktów dodatkowych. W ten sposób menedżerowie projektów mogą mieć pojedynczy, ujednolicony widok wszystkich kosztów w ramach danego projektu.

## <a name="create-vendor-invoices-in-project-operations"></a>Tworzenie faktur od dostawców w Project Operations

Faktury od dostawców są tworzone w usłudze Dynamics 365 Finance przy użyciu modułu **Rozrachunki z dostawcami** . Nie można tworzyć faktur od dostawców bezpośrednio w programie Dataverse.

### <a name="set-up-vendor-invoice-verification"></a>Ustawianie weryfikacji faktur od dostawców

Jeśli faktura dostawcy jest przeznaczona dla podwykonawcy w Dataverse, należy włączyć parametr **Ręczna weryfikacja przez PM jest wymagana**. Ustawienie opcji określa, czy faktura dostawcy ma być automatycznie potwierdzana w Dataverse, czy też wymaga ręcznego potwierdzenia. Nagłówek każdej faktury dostawcy projektu zawiera opcję o tej samej nazwie. Domyślnie opcja w nagłówku wszystkich faktur dostawcy projektu jest ustawiona na wartość ustawioną w tym miejscu. Można jednak zaktualizować tę wartość w nagłówku poszczególnych faktur dostawcy.

Jeśli ta opcja ma wartość **Tak**, faktura dostawcy, która jest tworzona w programie Finanse i synchronizowana z Dataverse ma stan **Wersja robocza**. Następnie menedżer projektu musi sprawdzić fakturę i potwierdzić ją, zanim zostanie ona przetworzona i zaksięgowana do określonych kont projektów i księgowego w programie Finanse.

Jeśli opcja jest ustawiona na **Nie**, faktura dostawcy jest automatycznie potwierdzana. Wykonywanie dalszych akcji nie jest wymagane.

Aby skonfigurować weryfikację faktur dostawcy, należy wykonać następujące czynności:

1. W programie Finance przejdź do **Zarządzanie projektami i księgowanie** \> **Ustawienia** \> **Parametry zarządzania projektami i księgowanie**.
1. Na karcie **Finanse** ustaw opcję **Weryfikacja ręczna PM jest wymagana** na **Tak**, jeśli zasady firmy wymagają weryfikacji faktur dostawców podwykonawców. Jeśli weryfikacja przez menedżera projektu nie jest wymagana w Dataverse, zostaw ustawienie **Nie**. Domyślnie to ustawienie będzie używane na stronie **Oczekująca faktura dostawcy**.

> [!NOTE]
> Faktury dostawcy utworzone dla podwykonawców w Dataversemogą być przetwarzane poprawnie tylko wtedy, gdy opcja **Weryfikacja ręczna przez PM jest wymagana** jest ustawiona na **Tak**. Wartości rzeczywiste czasu, materiałów i wydatków tworzone przez podwykonawców mogą być ręcznie dopasowane do wierszy faktury dostawcy przez menedżera projektu, jeśli ta opcja jest ustawiona na **Tak**.

### <a name="set-up-a-procurement-integration-account-for-vendor-invoices"></a>Konfigurowanie konta integracji zamówień dla faktur dostawcy

Gdy faktura dostawcy jest księgowana w programie Finanse dla zintegrowanego środowiska Project Operations (niemagazynowego), dane finansowe są księgowane na koncie integracji zamówień. System generuje wartości rzeczywiste w Dataverse dla zaksięgowanych faktur. Te wartości rzeczywiste są księgowane w programie Finanse przy użyciu dziennika Integracja projektu. Księgowanie pozycji dziennika Integracja projektu powoduje zaksięgowanie kosztu rzeczywistego i cofa konto integracji zamówień.

Aby skonfigurować konto integracyjne zamówień dla faktur dostawcy, wykonaj następujące kroki.

1. W programie Finance przejdź do **Zarządzanie projektami i księgowanie** \> **Ustawienia** \> **Parametry zarządzania projektami i księgowanie**.
1. Na karcie **Project Operations w u klientach usługi Dynamics 365 Customer Engagement** wybierz **Materiały** \> **Konto integracji zamówień**.

### <a name="create-and-post-subcontract-vendor-invoices"></a>Tworzenie i księgowanie faktur dostawcy podwykonawcy

Gdy pracownik obsługujący Rozrachunki z dostawcami otrzymuje fakturę od podwykonawcy, w programie Finance tworzona jest nowa faktura.

1. W programie Finance przejdź do **Rozrachunki z dostawcami** \> **Faktury** \> **Oczekujące faktury od dostawcy**.
1. W **okienku akcji** wybierz opcję **Nowy**, aby utworzyć fakturę dostawcy.
1. W nagłówku faktury w polu **Konto faktury** wybierz opcję **Podwykonawca**.
1. Wybierz datę faktury.
1. Na karcie **Nagłówek** ustaw opcję **Weryfikacja ręczna przez PM jest wymagana** na **Tak**. Domyślne ustawienie tej opcji znajduje się na stronie **Parametry zarządzania projektem i parametrów księgowania**. Można je jednak zmienić na poziomie faktury dostawcy.
1. Na skróconej karcie **Wiersz faktury** wybierz **Dodaj wiersz**, aby utworzyć wiersz faktury dostawcy.
1. Wybierz kategorię, która została utworzona dla wierszy podumowy, i wprowadź cenę jednostkową, jednostkę miary i ilość.
1. W sekcji wierszy faktur dostawcy na karcie **Projekt** wybierz projekt dla którego podwykonawca udostępnia fakturę podumowy.
1. Wybierz kategorię projektu. Może to być dowolny typ **Element**, **Wydatek**, **Materiały** lub **Godziny**.
1. Wybierz rolę tylko wtedy, gdy wybranym typem kategorii projektu są **Godziny**.
1. Wybierz opcję **Księguj**, aby zaksięgować fakturę dostawcy.

Można też utworzyć fakturę dostawcy, przechodząc do **Rozrachunki z dostawcami** \> **Faktury** \> **Otwarte faktury dostawcy** i wybierając **Nowa**.

Po zaksięgowaniu faktury staje się ona dostępna w Dataverse do weryfikacji i przetworzenia przez menedżera projektu.

## <a name="vendor-invoice-processing-in-dataverse"></a>Przetwarzanie faktur dostawców w usłudze Dataverse

Na fakturze dostawcy utworzonej w Dataverse niektóre wartości pól pochodzą z faktury dostawcy zarejestrowanej w programie Finance. Inne wartości to wartości domyślne pochodzące z podumowy.

Następujące pola i rekordy pokrewne zostaną skopiowane z kontraktu podrzędnego do nagłówka faktury dostawcy:

- Waluta
- Jednostka kontraktująca
- Warunki płatności

W wierszach faktury dostawcy Project Operations używa następujących wartości pól w celu wprowadzenia domyślnego odwołania do podumowy i wiersza podumowy:

- Klasa transakcji
- Rola
- Kategoria transakcji
- Pola produktu
- Project
- Zadanie

> [!NOTE]
> Stałe wiersze podumowy nie są obsługiwane w Project Operations.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
