---
title: Zarządzanie propozycjami faktur projektu
description: Ten temat zawiera szczegółowe informacje na temat przetwarzania faktur wystawianych dla klientów za pomocą Project Operations dla scenariuszy opartych na zasobach / braku zapasów.
author: sigitac
manager: Annbe
ms.date: 01/29/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 83e5af60d0a3baf0b59da2a97c6b156ef5b2b7ed
ms.sourcegitcommit: b4298ca4729643c1040ef35dde8c67f829461ce7
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2021
ms.locfileid: "5089284"
---
# <a name="manage-project-invoice-proposals"></a>Zarządzanie propozycjami faktur projektu

_**Zastosowane do:** Project Operations dla zasobów/scenariuszy nieopartych na zaopatrzeniu_

Propozycje faktur projektu mogą być przetwarzane przez dział rozliczeń, jeśli spełnione są następujące dwa warunki:

  - Menedżer projektu potwierdza fakturę proforma w Microsoft Dataverse.
  - Wszystkie nierozliczone transakcje sprzedaży i materiały zawarte na fakturze proforma są publikowane przy użyciu arkusza **integracji aplikacji Project Operations** usługi Dynamics 365.

Aby dokończyć propozycje faktury projektu w programie Dynamics 365 Finance, wykonaj następujące kroki.

1. Przeglądanie informacji dotyczących fakturowania dotyczących transakcji czasowych i materiałowych oraz publikowane w arkuszu **integracji aplikacji Project Operations**.
2. Przeglądanie informacji o fakturowaniu dla punktów kontrolnych rozliczania o stałej cenie.
3. Przejrzyj i sformatuj propozycję faktury za projekt.
4. Księgowanie i drukowanie faktur projektu.

## <a name="manage-billing-information-in-the-project-operations-integration-journal"></a>Zarządzanie informacjami dotyczących fakturowania w arkuszu integracji aplikacji Project Operations

Dane rzeczywiste projektu utworzone w Dataverse są przeglądane i księgowane w Finance przez księgowego projektu. Aby uzyskać więcej informacji na temat pracy z arkuszem integracji, zobacz [Arkusz integracji w aplikacji Project Operations](../project-accounting/project-operations-integration-journal.md).

Wartości rzeczywiste kosztów i niezafakturowane wartości rzeczywiste sprzedaży są dodawane do arkusza Integracja jako oddzielne wiersze:

  - Cena kosztu jednostkowego i kwota kosztu rzeczywistego kosztu domyślnego z transakcji kosztu rzeczywistego projektu w Dataverse.
  - Jednostkowa cena sprzedaży i kwota sprzedaży w niezafakturowanej transakcji sprzedaży są domyślne z rzeczywistej niezafakturowanej transakcji sprzedaży projektu w Dataverse.

### <a name="billing-sales-tax"></a>Rozliczanie podatku sprzedaży

Obliczenia podatku dla fakturowania są określane przez kombinację pola **Grupa podatku fakturowania** i **Grupa podatku towaru do rozliczania** dla nieunikatowego rekordu sprzedaży w wierszu arkusza **integracji aplikacji Project Operations**. System domyślnych wartości tych pól jest oparty na ustawieniach na karcie **Finanse** na stronie **Parametry zarządzania projektami i parametrów księgowania**.

- **Metoda grupy podatku fakturowania** służy do określania domyślnej logiki grupy podatku fakturowania:
  
  - **Projekt**: zawsze będzie domyślną grupą podatku fakturowania dla projektu. Aby przejrzeć lub zmienić domyślną grupę podatku fakturowania w projekcie, wybierz opcję **Pokaż domyślne księgowanie** na stronie **Wszystkie projekty**.
  - **Kontrakt projektu**: zawsze będzie domyślną grupą podatku fakturowania dla kontraktu projektu. Aby przejrzeć lub zmienić domyślną grupę podatku fakturowania w kontrakcie projekcie, wybierz opcję **Pokaż domyślne księgowanie** na stronie **Kontrakty projektów**.
  - **Klient**: zawsze będzie domyślną grupą podatku fakturowania dla klienta.
  - **Wyszukiwanie**: przeszuka wszystkie powyższe encje i wybierz pierwszą dostępną wartość. Wyszukiwanie rozpoczyna się od encji **Projekt**, encji **Kontrakt projektu** oraz encji **Klient**.

- **Metoda grupy podatku towaru** służy do określania domyślnej logiki grupy podatku towaru do rozliczenia:
  
  - W przypadku typów transakcji dotyczących czasu, wydatków i opłat grupa podatku dla elementu rozliczeniowego będzie zawsze domyślną encja **Kategoria projektu**.
  - W przypadku typów transakcji materiałowych domyślne wartości grupy podatku dla pozycji rozliczeń są oparte na ustawieniu **Metody grupy podatku** w **Parametrach zarządzania projektami i księgowania**. Numer pozycji jest domyślnie pobiera grupę podatku dla pozycji rozliczeń dla encji **Produkt wydany**. Kategoria domyślnie określa grupę podatków dla towaru z encji **Kategoria projektu**.

### <a name="financial-dimensions"></a>Wymiary finansowe

Wymiary finansowe dla niezafakturowanych rekordów sprzedaży w arkuszu **Integracja Project Operations** domyślnie z encji **Projekt**. Wymiary finansowe można przejrzeć i dostosować, wybierając opcję **Dystrybuuj kwoty**. Jeśli potrzebujesz zmienić wymiary finansowe niezafakturowanego rekordu sprzedaży po zaksięgowaniu arkusza integracji, ale przed potwierdzeniem faktury Proforma, przejdź do **Wszystkie projekty** > **Zarządzaj** > **Transakcje zaksięgowane**, wybierz transakcję, a następnie wybierz **Proces** > **Koryguj Księgowanie**.

### <a name="exchange-rates"></a>Kursy wymiany

Niezafakturowana waluta transakcji w Dataverse jest używana jako waluta transakcji w Finance i konwertowana na walutę księgową firmy przy użyciu kursów wymiany zdefiniowanych w Finance.


## <a name="manage-the-financial-attributes-of-billing-milestones"></a>Zarządzanie atrybutami finansowymi punktów kontrolnych rozliczania 

Wiersze kontraktu dotyczącego projektu korzystające z metody fakturowania ze stałą ceną są fakturowane za pośrednictwem [punktach kontrolnych z ustalonymi cenami](../sales/invoice-schedules-contract-line.md#create-a-fixed-price-invoice-schedule-for-a-contract-line). Księgowy projektu może przeglądać etapy rozliczeń w programie Finance, przechodząc do **Zarządzanie projektami i księgowanie** > **Wszystkie projekty** > **Zarządzaj** > **Transakcje dotyczące klienta**.

### <a name="billing-sales-tax"></a>Rozliczanie podatku sprzedaży

Wartości **Grupa podatków** i **Grupa podatku towaru** są domyślnie ustawione na podstawie ustawień, gdy nowy punkt kontrolny fakturowania jest tworzony w Dataverse. System domyślnie ustawia wartości w tych polach na podstawie ustawień na karcie **Finanse** na stronie **parametrach zarządzania projektami i księgowania**.

- **Metoda grupy podatku fakturowania** określa domyślną logikę **Grupy rozliczenia podatków**:

    - **Projekt** zawsze będzie domyślną grupą podatku fakturowania dla projektu. Aby przejrzeć lub zmienić domyślną grupę podatku w projekcie, wybierz opcję **Pokaż domyślne księgowanie** na stronie **Wszystkie projekty**.
    - **Kontrakt projektu** zawsze będzie domyślną grupą podatku fakturowania dla kontraktu projektu. Aby przejrzeć lub zmienić domyślną grupę podatku fakturowania w kontrakcie projekcie, wybierz opcję **Pokaż domyślne księgowanie** na stronie **Kontrakty projektów**.
    - **Klient** zawsze będzie domyślną grupą podatku fakturowania dla klienta.
    - **Wyszukiwanie**:przeszuka wszystkie powyższe encje na tej liście i wybierz pierwszą dostępną wartość. Wyszukiwanie rozpoczyna się od encji **Projekt**, encji **Kontrakt projektu** oraz encji **Klient**.

- **Grupa podatku produktu o stałej cenie punktów kontrolnych** jest używana, aby domyślna wartość pola wynosiła **Grupa podatku towaru do rozliczania**.

### <a name="financial-dimensions"></a>Wymiary finansowe

Domyślne wymiary finansowe dla punktu kontrolnego fakturowania ze stałą ceną są ustawiane w wierszach umowy dotyczącej projektu. Wybierz pozycję **Kontrakty projektów** > **Pokaż domyślne księgowanie**, a na karcie **Wiersze kontraktu** wybierz **wiersz umowy cenowej**, a następnie ustaw wartości wymiarów finansowych, których chcesz użyć jako domyślnych.

Księgowy projektu może edytować informacje o podatku od sprzedaży i wymiarach finansowych w punktach kontrolnych faktur do momentu utworzenia propozycji faktury projektu.


## <a name="create-project-invoice-proposals"></a>Utwórz propozycje faktur za projekt

Oferty na fakturę projektu można przejrzeć w module **Zarządzanie projektami i księgowanie**, przechodząc do **Faktury projektu** > **Propozycje faktur projektu**.

Nagłówek propozycji faktury projektu jest tworzony w Finance, gdy faktura Proforma jest potwierdzana w Dataverse. Aby ułatwić uzgodnienie, system ustawia numer propozycji faktury za projekt w programie Finance na taki sam numer, jak identyfikator faktury Proforma w Dataverse. Ponieważ faktury Proforma niekoniecznie są potwierdzane w tej samej kolejności, w jakiej są tworzone, sekwencja numerów propozycji faktury projektu w programie Finance musi zezwalać na zmiany w coraz niższych i wyższych numerach. Skonfiguruj sekwencje numerów, korzystając z następujących kroków:

1. W Finance przejdź do **Administracja organizacji** > **Sekwencje numerów** > **Sekwencje numerów**.
2. W filtrze **Obszar** wybierz opcję **Projekty**.
3. W filtrze **Odwołania** wybierz opcję **Propozycja faktury**.
4. Pole **Firma** umożliwia filtrowanie poszczególnych firm, dla których włączono integrację Project Operations Dataverse.
5. Otwórz **Szczegóły sekwencji numerów** i na karcie **Ogólne**:

    - **Zezwalaj na zmiany użytkownika: Do niższej liczby** = **Tak**
    - **Zezwalaj na zmiany użytkownika: Do wyższej liczby** = **Tak**

Wiersze propozycji faktury projektu są dodawane przez system przy użyciu procesu okresowego **Import z tabeli przemieszczania** (**Zarządzanie projektami i księgowanie** > **Okresowe** > **Integracja Project Operations** > **Import z tabeli przemieszczania**). Ten proces można uruchomić ręcznie lub przy użyciu harmonogramu okresowego. System nie doda wierszy do dokumentu propozycji faktury, dopóki wszystkie wiersze nie będą gotowe do zafakturowania. Transakcje czasowe i materiałowe są gotowe do zafakturowania tylko wtedy, gdy są zaksięgowane przy użyciu arkusza **Integracja Project Operations**.

## <a name="format-and-print-invoice-proposals"></a>Formatowanie i drukowanie propozycji faktur

Księgowy projektu może dostosować wydruk faktury za projekt, korzystając z propozycji faktury **Formatowanie propozycji faktury** oraz funkcji zarządzania drukowaniem.

### <a name="format-invoice-proposals"></a>Formatowanie propozycji faktur

Strona **Formatowanie ofert faktur** umożliwia wyświetlanie niestandardowych transakcji grupowania na fakturze projektu klienta.

1. Na stronie **Propozycje faktury projektu** wybierz opcję **Drukuj** > **Formatowanie propozycji faktur**.
2. Wybierz opcję **Nowy**, aby utworzyć nowe grupowanie dla wydruku faktury Projektu.
3. W polu **Szczegóły/Podsumowanie** wybierz opcje dotyczące tego grupowania:

    - Wybierz opcję **Szczegóły**, aby wydrukować szczegóły transakcji na fakturze klienta.
    - Wybierz opcję **Podsumowanie**, aby wydrukować podsumowanie transakcji na fakturze klienta.

> [!NOTE]
> Wybór w polu **Szczegóły/Podsumowanie** na stronie **Formatowanie propozycji faktury** zastępuje opcję wybraną w polu **IFormat faktury** na stronie **Propozycje faktur**, aby wydrukować szczegółową fakturę lub fakturę podsumowania.

- Wybierz wiersze transakcji, które chcesz uwzględnić w tej sekcji na karcie **Dostępne transakcje** i wybierz opcję **Uwzględnij transakcje**, aby przenieść je na kartę **Wybrane transakcje**.
- Wybierz opcję **Przenieś w górę** i **Przenieś w dół**, aby zmienić kolejność sekcji.
- Wybierz **Podgląd wydruku**, aby wyświetlić podgląd sformatowanych faktur.

### <a name="print-management"></a>Zarządzanie drukowaniem

Zarządzanie drukowaniem wykorzystuje różne pliki raportów do drukowania, określania miejsc docelowych i dostosowywania tekstu stopki faktury. Zarządzanie drukowaniem można skonfigurować na poziomie modułu, jednak ustawienia te można zastąpić dla konkretnego klienta, umowy lub propozycji faktury. Aby uzyskać dostęp do tej funkcji na stronie **Propozycji fakturowania projektu**, wybierz **Drukuj** > **Zarządzanie drukowaniem**.

Konfiguracja zarządzania drukowaniem jest wyświetlana jako widok drzewa, w którym na każdym poziomie węzła są wyświetlane dokumenty dostępne do dostosowania. Możesz przypisać niestandardowe wydruki na poziomie modułu, klienta, umowy lub dokumentu propozycji faktury. Aby zmodyfikować wydruk oryginalnego dokumentu, rozwiń żądany węzeł i wybierz **Oryginalny element**. W polu **Format raportu** wybierz format raportu, który ma być używany do drukowania. Możesz użyć niestandardowych formatów raportów, używając [struktury zarządzania dokumentami biznesowymi](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/er-business-document-management).

## <a name="post-invoice-proposals"></a>Księgowanie propozycji faktur

Po przejrzeniu i edycji faktury, a wiersze propozycji faktury są zadowalające, sprawdź sumy faktur i podatek. W grupie **Szczegóły** wybierz opcję **Sumy**, a następnie wybierz opcję **Zaksięguj** w celu zafakturowania faktury.

Aby wyświetlić fakturę przed opublikowaniem, wyczyść pole wyboru **Księgowanie**. **Pro forma** zostanie wydrukowane na fakturze, aby zaznaczyć, że jest to faktura przykładowa. Aby wydrukować fakturę, zaznacz pole wyboru **Wydrukuj fakturę**.

Oprócz strony **Propozycja faktury** można także wystawić propozycję faktury, uruchamiając zadanie okresowe **Księgowanie propozycji faktur**. Aby znaleźć to zadanie, przejdź do **Zarządzanie projektami i księgowanie** > **Okresowe** > **Faktury projektów** > **Zaksięguj propozycje faktur**.

Ta strona zawiera wszystkie propozycje faktur, które są gotowe do zaksięgowania. Ofertę na fakturę można zaplanować, wybierając opcję **Partia**. Ustaw parametr **Przetwarzanie wsadowe** na wartość **Tak** i ustaw cykl przetwarzania wsadowego, wybierając opcję **Cykl**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]