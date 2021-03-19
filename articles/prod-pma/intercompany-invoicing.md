---
title: Faktura międzyfirmowa
description: W tym artykule zamieszczono informacje i przykłady dotyczące międzyfirmowego fakturowania projektów.
author: Yowelle
manager: AnnBe
ms.date: 09/14/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerInterCompany
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 94153
ms.assetid: 33e98da7-01c1-4369-923d-aa1c8326cb80
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 76eba87e7cc78dcc14510a8fb53677d626bf204f
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5270781"
---
# <a name="intercompany-invoicing"></a>Faktura międzyfirmowa

[!include [banner](../includes/banner.md)]

W tym artykule zamieszczono informacje i przykłady dotyczące międzyfirmowego fakturowania projektów.

Organizacja może dysponować wieloma oddziałami, podmiotami zależnymi i innymi firmami, które przekazują sobie produkty i usługi do projektów. Podmiot prawny, który świadczy usługę lub produkt, jest nazywany *firmą udzielającą pożyczki*, a podmiot prawny, który otrzymuje usługę lub produkt, jest nazywany *firmą pożyczającą*. 

Na poniższej ilustracji przedstawiono typowy scenariusz, w którym dwie osoby prawne, SI FR (firma pożyczająca) i SI USA (firma udzielająca pożyczki) współużytkują zasoby w celu dostarczenia projektu dla klienta A. praca dla klienta A. 

[![Przykład faktury międzyfirmowej](./media/interco.invoicing-01.jpg)](./media/interco.invoicing-01.jpg) 

Celem jest uczynienie kontroli kosztów, rozpoznawania przychodów, podatków i ceny transferowej transakcji międzyfirmowych w ramach bardziej elastycznych i wydajnych. Ponadto dostępne są następujące możliwości:

-   Twórz faktury dla odbiorców dotyczące projektu w firmie pożyczającej, używając międzyfirmowych kart czasu pracy, wydatków i faktur od dostawcy w firmie pożyczającej.
-   Obsługuj obliczenia podatku i koszty pośrednie.
-   Odroczenie ujęcia przychodów w firmie udzielającej pożyczki oraz w momencie, gdy firma pożyczająca powinien ująć koszt.
-   Przychód z pracy w toku (PWT) w firmie pożyczającej.
-   Ustaw ceny przeniesienia, które mogą być oparte na różnych modelach kalkulacji cen. Oto kilka przykładów:
    -   **Ilość** – Kwota wprowadzana w polu **Cenly** jest rzeczywistym kosztem dla ilości lub jednostki.
    -   **Kwota opłaty** — cena/koszt na transakcję powiększona o kwotę opłaty, jaką wprowadzono w polu **Ceny**.
    -   **Procent opłat** — cena przeniesienia jest ceną sprzedaży na transakcję pomnożoną przez stawkę procentową opłaty wprowadzonej w polu **Ceny**.
    -   **Procent ceny sprzedaży** — wyrażony w procentach cena sprzedaży, która jest przekazywana do firmy użyczającej pożyczki.
    -   **Kwota niższa niż cena sprzedaży** — Kwota, którą firma pożyczająca zatrzymuje z cen sprzedaży przed przeniesieniem do firmy udzielającej pożyczki.
    -   **Współczynnik marży** — numer wprowadzony w polu **Ceny** to współczynnik marży wyrażony jako procent ceny sprzedaży.

## <a name="example-1-set-up-parameters-for-intercompany-invoicing"></a>Przykład 1. Konfigurowanie parametrów fakturowania międzyfirmowego
W tym przykładzie USSI jest osobą prawną udzielającą pożyczki, a jej zasoby raportują czas w stosunku do firmy pożyczającej FRSI, która jest właścicielem umowy z klientem końcowym. Godziny i wydatki, które USSI raport dotyczący pracowników, mogą być uwzględnione w fakturze projektu, która FRSI generowana. Ponadto istnieje trzecie źródło transakcji, które może pochodzić od podmiotu prawnego udzielającego pożyczki (w tym przykładzie USSI), gdy świadczy on usługi wspólnych dostawców spółkom zależnym (takim jak FRSI), a następnie przenosi te koszty na projekty w tych spółkach zależnych. Wszystkie pasujące dokumenty faktur i obliczenia podatku są uzupełniane przez Finance. 

W tym przykładzie FRSI musi być klientem w firmie USSI, a USSI musi być dostawcą w firmie FRSI. Następnie można skonfigurować relację międzyfirmową między dwiema firmami. Poniższa procedura pokazuje, jak skonfigurować parametry, aby obie firmy mogły uczestniczyć w fakturowaniu międzyfirmowym.

1. Skonfiguruj FRSI jako klienta w firmie USSI i skonfiguruj USSI jako dostawcę w firmie FRSI. Istnieją trzy punkty wejścia dotyczące kroków, które są wymagane w przypadku tego zadania.

   | Krok |                                                       Punkt wejścia                                                        |                                                                                                                                                                                               Opis                                                                                                                                                                                               |
   |------|--------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
   |  A   | W USSI kliknij <strong>Należności</strong> &gt; <strong>Klienci</strong> &gt; <strong>Wszyscy klienci</strong>. |                                                                                                                                                                  Utwórz nowy rekord klienta dla FRSI i wybierz grupę klientów.                                                                                                                                                                  |
   |  B   |    W FRSI kliknij <strong>Rozrachunki z dostawcami</strong> &gt; <strong>Dostawcy</strong> &gt; <strong>Wszyscy dostawcy</strong>.     |                                                                                                                                                                    Utwórz nowy rekord dostawcy dla USSI i wybierz grupę dostawców.                                                                                                                                                                    |
   |  C   |                                  W FRSI otwórz właśnie utworzony rekord dostawcy.                                  | W okienku akcji na karcie <strong>Ogólne</strong> w grupie <strong>Konfiguracja</strong> kliknij opcję <strong>Międzyfirmowe</strong>. Na stronie <strong>Międzyfirmowe</strong> na karcie <strong>Relacja handlowa</strong> ustaw suwak <strong>Aktywny</strong> na <strong>Tak</strong>. W polu <strong>Firma klienta</strong> wybierz rekord klienta utworzony w kroku A. |


2. Kliknij **Zarządzanie projektami i księgowanie** &gt; **Ustawienia** &gt; **Parametry Zarządzanie projektami i księgowanie**, a następnie kliknij kartę **Międzyfirmowe**. Sposób konfigurowania parametrów zależy od tego, czy jest to osoba prawna lub osoba prawna, która jest pożyczana.
   -   Jeśli jesteś firmą pożyczającą, wybierz kategorię zaopatrzenia, która ma być używana do dopasowywania faktur od dostawcy, które są generowane automatycznie.
   -   Jeśli jesteś firmą udzielającą pożyczki, dla każdego podmiotu pożyczającego wybierz domyślną kategorię projektu dla każdego typu transakcji. Kategorie projektów są używane do konfiguracji podatku, gdy zafakturowana kategoria w transakcjach międzyfirmowych istnieje tylko w firmie wypożyczającej. Istnieje możliwość naliczenia przychodu z transakcji międzyfirmowych. To naliczanie jest wykonywane po zaksięgowaniu transakcji, a następnie jest wycofywane po zaksięgowaniu faktury międzyfirmowej.

3. Kliknij **Zarządzanie projektami i księgowanie** &gt; **Ustawienia** &gt; **Ceny** &gt; **Przeniesienie ceny**.
4. Wybierz walutę, typ transakcji i model ceny przeniesienia. Waluta używana na fakturze to waluta, która jest konfigurowana w rekordzie klienta dla osoby prawnej zaciągania pożyczek w firmie kredytowej. Ta waluta jest używana do dopasowywania wpisów w tabeli cena przeniesienia.
5. Kliknij kolejno pozycje **Księga główna** &gt; **Konfiguracja księgowania** &gt; **Księgowość międzyfirmowa** i skonfiguruj relację dla USSI i FRSI.

## <a name="example-2-create-and-post-an-intercompany-timesheet"></a>Przykład 2. Tworzenie i księgowanie grafiku międzyfirmowego
USSI, firma udzielająca pożyczki, musi utworzyć i zaksięgować grafik dla projektu od FRSI, firmy pożyczającej. Istnieją dwa punkty wejścia dotyczące kroków, które są wymagane w przypadku tego zadania.

| Krok | Punkt wejścia                                                                       | Opis                                                                                                                                                                                       |
|------|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| A    | **Zarządzanie projektami i księgowanie** &gt; **Grafik** &gt; **Wszystkie grafiki** | Powoduje utworzenie nowego grafika. W wierszu grafiku w polu **Firma** wybierz **FRSI**. W polu **Identyfikator projektu** wybierz projekt w FRSI. Wprowadź godziny dla każdego dnia tygodnia. |
| B    | Strona **Grafiku**                                                                | Po rozpoczęciu przepływu pracy zaksięguj grafik i zanotuj numer załącznika.                                                                                                               |

## <a name="example-3-create-and-post-an-intercompany-vendor-invoice"></a>Przykład 3: Tworzenie i księgowanie międzyfirmowej faktury od dostawcy
USSI, firma pożyczająca, musi utworzyć i zaksięgować międzyfirmową fakturę od dostawcy dla projektu od FRSI, firmy pożyczającej. Ta faktura dostawcy przedstawia zleconą na zewnątrz pracę i wydatki, które zostały wykonane przez dostawców opłacanych przez USSI. Istnieją dwa punkty wejścia dotyczące kroków, które są wymagane w przypadku tego zadania.

| Krok | Punkt wejścia                                                                                      | Opis                                                                                                                                                                                                                                                                          |
|------|--------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| A    | **Rozrachunki z dostawcami** &gt; **Faktury** &gt; **Otwarte faktury dostawcy** &gt; **Nowa faktura dostawcy** | Utwórz nową fakturę od dostawcy i wprowadź usługi, które zostały zamówione w imieniu projektu FRSI.                                                                                                                                                                                  |
| B    | Strona **Faktura od dostawcy**                                                                      | Wprowadź wiersze reprezentujące usługi zewnętrznie w imieniu FRSI. Na skróconej karcie **Szczegóły wiersza** na karcie **Projekt** wiersza faktury w polu **Firma projektu** wprowadź **FRSI**. Wprowadzenie projektu i odpowiednich informacji. Następnie należy zaksięgować fakturę od dostawcy. |

## <a name="example-4-create-and-post-the-intercompany-invoice"></a>Przykład 4: Tworzenie i księgowanie międzyfirmowej faktury
USSI, firma udzielająca pożyczki, musi utworzyć i zaksięgować fakturę międzyfirmową. Istnieją dwa punkty wejścia dotyczące kroków, które są wymagane w przypadku tego zadania.

| Krok | Punkt wejścia                                                                                             | Opis                                                                                                                                      |
|------|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| A    | **Zarządzanie projektami i księgowanie** &gt; **Faktury projektów** &gt; **Faktura międzyfirmowa dla klienta**  | Kliknij pozycję **Nowy**, aby otworzyć stronę **Utwórz fakturę międzyfirmową**.                                                                                  |
| B    | **Zarządzanie projektami i księgowanie** &gt; **Faktury projektów** &gt; **Faktury międzyfirmowe dla klienta** | Na stronie **Tworzenie faktury międzyfirmowej** wprowadź firmę, określ transakcję, która ma zostać uwzględniona, a następnie kliknij opcję **Wyszukaj**. |
| C    | **Zarządzanie projektami i księgowanie** &gt; **Faktury projektów** &gt; **Faktury międzyfirmowe dla klienta** | Wybierz transakcje do zafakturowania lub kliknij pozycję **Zaznacz wszystko**, aby zafakturować wszystkie transakcje z listy, a następnie kliknij przycisk **OK**.                  |
| D    | Strona **Faktura międzyfirmowa**                                                                       | Zostanie wyświetlona oferta międzyfirmowej faktury dla klienta.                                                                                             |
| E    | Strona **Faktura międzyfirmowa**                                                                       | Kliknij pozycję **Wpis**.                                                                                                                                  |

## <a name="example-5-post-the-vendor-invoice-and-invoice-the-customer"></a>Przykład 5: Księgowanie faktury dostawcy i faktury dla klienta
Gdy firma pożyczająca, USSI, księguje międzyfirmową fakturę dla odbiorcy, w firmie pożyczającej FRSI tworzona jest zgodna oczekująca faktura od dostawcy. Po zaksięgowaniu tej faktury od dostawcy FRSI fakturuje również klienta projektu za godziny wprowadzone przez USSI. Istnieją trzy punkty wejścia dotyczące kroków, które są wymagane w przypadku tego zadania.

| Krok | Punkt wejścia                                                                                        | Opis                                                                                                             |
|------|----------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| A    | **Rozrachunki z dostawcami** &gt; **Faktury** &gt; **Oczekujące faktury od dostawcy**                            | Przejrzyj fakturę, aby sprawdzić, czy są uwzględnione wartości grafiku, a następnie kliknij opcję księguj fakturę od dostawcy.                  |
| B    | **Zarządzanie projektami i księgowanie** &gt; **Faktury projektów** &gt; **Propozycje faktur projektowych** | Utwórz nową fakturę projektu dla projektu i sprawdź, czy są na nim zaksięgowane transakcje godzinowe.            |
| C    | Strona **Faktura projektu**                                                                       | Wybierz fakturę projektu, a następnie kliknij opcję **Wyświetl szczegóły**, aby przejrzeć koszty i kwotę sprzedaży. Następnie należy zaksięgować fakturę. |


Aby uzyskać więcej informacji, zobacz temat [Konfigurowanie międzyfirmowego fakturowania projektu](tasks/configure-intercompany-project-invoicing.md).




[!INCLUDE[footer-include](../includes/footer-banner.md)]