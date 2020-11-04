---
title: Konfigurowanie księgowania projektów do zafakturowania
description: Ten temat zawiera informacje o opcjach księgowania projektów podlegających rozliczeniu.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 32031742b1a9580b9ebdbaf6952a998733be5e8f
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081926"
---
# <a name="configure-accounting-for-billable-projects"></a>Konfigurowanie księgowania projektów do zafakturowania

_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_

Dynamics 365 Project Operations obsługuje różne opcje księgowania projektów podlegających rozliczeniu, które zawierają transakcje o stałej cenie oraz transakcje typu czas i materiały.

- **Transakcje typu czas i materiały** : te transakcje są fakturowane w miarę postępu prac i w zależności od zużycia godzin, wydatków, zapasów lub opłat w projekcie. Te koszty transakcji można dopasować do przychodu z każdej transakcji, a projekt jest fakturowany w miarę postępu prac. Przychód z projektu może być również naliczony w momencie, gdy dana transakcja ma miejsce. Podczas fakturowania w programie jest rozpoznawany przychód, a w odpowiednim przypadku jest zastosowane odwrócenie naliczonego przychodu.
- **Transakcje o stałej cenie** : Te transakcje są fakturowane zgodnie z harmonogramem fakturowania utworzonym na podstawie kontraktu dotyczącego projektu. Przychód z transakcji o stałej cenie może być rozpoznawany na fakturze, lub lub obliczany i okresowo księgowany — zgodnie z metodami **Wykonanego kontraktu** lub **Procentu ukończenia projektu**.

Projekt jest traktowany jako możliwy do rozliczenia, gdy jest skojarzony z co najmniej jednym wierszem kontraktu. Pozycja kontraktu w projekcie określa dozwolone metody fakturowania i typy transakcji.

W naszym przykładzie firma Fabrikam Robotic zdobyła kontrakt dotyczący optymalizacji sprzętu firmy Adatum corporation. Adatum zapłaci ustaloną kwotę w wysokości 10 tys. USD i pokryje koszty wynikające z projektu. Taka transakcja to „metoda rozliczania transakcji ze stałą ceną”. Czasy i opłaty projektowe będą rozliczane na każde użycie. Taka transakcja to „metoda rozliczania transakcji czasu i materiałów”. Wszystkie prace będą śledzone w jednym projekcie o nazwie Adatum — optymalizacja sprzętu.

Członek zespołu projektu zgłosi osiem godzin pracy nad projektem Adatum — optymalizacja sprzętu. Kiedy Menedżer projektu zatwierdza podany czas pracy, system używa metody fakturowania czasu i materiału do utworzenia transakcji rzeczywistych, faktury i konta. Transakcja nie zostanie uwzględniona w kalkulacji szacowanego przychodu z ceną ustaloną.

Inny członek zespołu projektu przesyła koszty podróży w wysokości 2000 USD jako część projektu Adatum — optymalizacja sprzętu. Kiedy Menedżer projektu zatwierdza przesłane dane, system używa metody fakturowania kosztów o stałej cenie do utworzenia transakcji rzeczywistych, faktury i konta, jako części wydatków projektowych. Klient nie otrzyma faktury na podstawie tej transakcji. Zamiast tego otrzyma on faktury na podstawie oddzielnie skonfigurowanych kamieni milowych rozliczeń. Transakcja wydatków, wraz z szacunkami wydatków, nie zostanie uwzględniona w kalkulacji szacowanego przychodu z ceną ustaloną.

Reguły księgowania dotyczące transakcji projektowych są definiowane w profilu kosztu projektu i przychodu. W przypadku każdej transakcji projektu system określa odpowiedni profil kosztu projektu i przychodu korzystając ze skonfigurowanych reguł dotyczących tych danych.

## <a name="define-project-cost-and-revenue-profiles"></a>Ustalanie profilu kosztu projektu i przychodu 

Reguły kosztów projektu i profili przychodów określają reguły księgowania transakcji projektowych. Te profile są konfigurowane w Informacjach o zarządzaniu projektami i ich księgowaniu. 

Wykonaj poniższe kroki, aby utworzyć nowy profil kosztu projektu i przychodu. 

1. Wybierz kolejno pozycje **Zarządzanie projektami i księgowanie** > **Konfiguracja** > **Księgowanie** > **Profile kosztów projektów i przychodów**. 
2. Wybierz opcję **Nowy** , aby utworzyć nowy profil kosztu projektu i przychodu.
3. W polu **Nazwa** wprowadź nazwę i krótki opis profilu.
4. W polu **Metoda fakturowania** wybierz opcję **Czas i materiały** lub **Ustalona cena**.
5. Rozwiń skróconą kartę **Księga główna**. Pola na tej karcie definiują reguły księgowania używane podczas rejestrowania transakcji projektu przy użyciu arkusza integracji w Project Operations, a następnie fakturowania za pośrednictwem propozycji faktury projektu.
6. Wybierz odpowiednie informacje w następujących polach na skróconej karcie **Księga główna** :

    - **Księgowanie kosztów — godzina** :

       - *Brak księgi głównej* : koszt związany z transakcjami czasowymi nie jest odnotowany w księdze głównej, gdy wykorzystywane jest księgowanie integracji dziennika Project Operations. Księgowy może jednak księgować koszty, korzystając z funkcji Księgowanie kosztów w późniejszym czasie.
       - **Saldo** : koszt związany z transakcjami czasowymi będzie obciążał konto księgi głównej typu *PWT — wartość kosztu* i zostanie zaksięgowany w sekcji *Konto alokacji płac* w ustawieniach księgi głównej. Korzystając z funkcji księgowanie kosztów, program klienta będzie okresowo przesuwać ten koszt z konta bilansowego na konto zysków i strat.
       - **Zyski i straty** : podczas księgowania arkusza integracji Project Operations koszty czasu transakcji będą obciążały konto księgi głównej typu *Koszt* , a dodawane będą do *Konta alokacji płac* , zdefiniowanego karcie **Koszt** znajdującej się na stronie **Konfiguracja zapisów księgi głównej** ( **Informacje o zarządzaniu projektami i ich księgowaniu** \> **Konfiguracja** \> **Księgowanie** \> **Konfiguracja zapisów księgi głównej** ). Jest to najczęstsza konfiguracja transakcji dotyczących czasu i materiałów.
        - *Nigdy w księdze głównej* : koszt transakcji czasu nigdy nie jest księgowany w księdze głównej.

    - **Księgowanie wydatków po kosztach** :

         - **Saldo** : podczas księgowania dziennika integracji Project Operations koszt transakcji wydatkowej będzie obciążał konto księgi głównej typu *PWT — wartość kosztu* zdefiniowane na karcie **Koszt** na stronie **Konfiguracja zapisów księgi głównej** i zaksięgowana na koncie rozliczeniowym w wierszu arkusza. Domyślne konta rozliczeniowe kosztów są definiowane w ustawieniach sekcji **Informacje o zarządzaniu projektami i ich księgowaniu** > **Konfiguracja** \> **Księgowanie** \> **Domyślne konta rozliczeniowe wydatków**. Korzystając z funkcji **księgowanie kosztów** , program klienta będzie okresowo przesuwać ten koszt z konta bilansowego na konto zysków i strat.
        - **Zyski i straty** : podczas księgowania dziennika integracji Project Operations koszt transakcji wydatkowej będzie obciążał konto księgi głównej typu *Koszt* zdefiniowanego na karcie **Koszt** na stronie **Konfiguracja zapisów księgi głównej** i zaksięgowana na koncie rozliczeniowym w wierszu arkusza. Domyślne konta rozliczeniowe kosztów są definiowane w ustawieniach sekcji **Informacje o zarządzaniu projektami i ich księgowaniu** \> **Konfiguracja** \> **Księgowanie** \> **Domyślne konta rozliczeniowe wydatków**.
       
    - **Faktury akonto** :

        - **Saldo** : podczas księgowania propozycji faktury projektu transakcja akonto (punkt milowy w rozliczeniach) będzie księgowana na koncie księgi głównej typu *Faktura PWT — akonto* , zdefiniowanym na karcie **Przychód** , która znajduje się na stronie **Konfiguracja dodawania zapisów księgi głównej** , i zaksięgowany po stronie debetowej dla konta bilansowego klienta.
         - **Zysk i strata** : podczas księgowania propozycji faktury projektu transakcja akonto (punkt milowy w rozliczeniach) będzie księgowana na koncie księgi głównej typu *Faktura PWT — akonto* , zdefiniowanym na karcie **Przychód na fakturze — akonto** , która znajduje się na stronie **Konfiguracja dodawania zapisów księgi głównej** , i zaksięgowany po stronie debetowej dla konta bilansowego klienta. Konta bilansowe klientów są określone w sekcji **Rozrachunki z odbiorcami** \> **Konfiguracja** \> **Profile rozrachunków z klientami**.

   Podczas definiowania profili księgowania dla metod fakturowania typu czas i materiały użytkownik ma możliwość naliczenia przychodu na typ transakcji (godzina, wydatek i opłata). Jeśli opcja **Naliczany przychód** ma wartość **Tak** , niezafakturowane transakcje sprzedaży w arkuszu integracji operacji projektu będą rejestrowane w księdze głównej. Wartość sprzedaży obciąża konto **PWT — konto wartości sprzedaży** , a uznanie naliczane jest na koncie **Naliczony przychód — wartość sprzedaży** , które zostało skonfigurowane na karcie **Przychód** w sekcji **Konfiguracja księgowania w rejestrze**. 
  
  > [!NOTE]
  > Ta opcja powoduje, że **Przychód naliczony** jest dostępny tylko wtedy, gdy odpowiedni typ transakcji **Koszt** jest księgowany na rachunku zysków i strat.
    
7. Rozwiń skróconą kartę **Szacunek**. Pola na tej karcie definiują ustawienia obliczeń dla szacowanego przychodu z ustalonymi cenami. Pola na tej karcie dotyczą tylko profilów kosztu projektu i przychodu z metodą fakturowania **Stała cena**.
8. Wybierz odpowiednie informacje w następujących polach na skróconej karcie **Szacunek** :

    - **Reguła używana do obliczania ukończenia projektów** :

        - **Kontrakt ukończony** : uzgadnianie kosztów i przychodu nie jest wykonywane, aż do końca projektu. Koszty pokazywane są jako PWT na saldzie, aż do zakończenia projektu.
        - **Procent realizacji** : naliczony przychód jest obliczany i księgowany w księdze głównej dla każdego okresu, w zależności od procentowego wykonania projektu. Istnieje wiele metod, które można wykorzystać do obliczenia wartości procentowej wykonania projektu. Metody te mogą być automatyczne — oparte na konfiguracji — lub ręczne.
        - **Brak PWT** : to ustawienie jest używane w przypadku projektów o stałej cenie z krótkim przedziałem czasu oraz lokalizacji, w której faktura i koszty występują w tym samym okresie. W tym przypadku wartość pola **Fakturowanie akonto** na skróconej karcie **Księga główna** jest automatycznie ustawiana jako **Zysk i strata** w celu zapewnienia, że przychód będzie reprezentowany na fakturach. Proces szacowania przychodu nie będzie używany w przypadku tego profilu kosztów projektów i przychodów.

    - **Reguła uzgadniania** : to pole określa sposób księgowania obliczonej wartości sprzedaży (przychód naliczony) w księdze głównej.

        - Przy użyciu reguły **Wartości sprzedaży** system obliczy wartość sprzedaży, dopasowując koszty i przychody, a następnie ogłosi ją jako jedną kwotę.
        - Przy użyciu reguły **Produkcja i zysk** , system podzieli wartość sprzedaży na zrealizowane koszty i obliczoną marżę. Te elementy są księgowane osobno.

    - **Szablony kosztów** : Zezwala na grupowanie transakcji projektu na podstawie typu transakcji i kategorii projektu oraz definiuje reguły obliczania procentu wykonania dla tych grup.
    - **Kody okresów** : umożliwia zdefiniowanie częstotliwości, z jaką są obliczane oszacowania przychodu dla określonego profilu kosztów projektu i przychodów.
    - **Kategorie oszacowania** : używane przy księgowaniu wartości sprzedaży (naliczany przychód) w transakcjach projektów. Najpierw skonfiguruj dedykowaną kategorię projektu dla typu transakcji **Opłata** , a następnie ustaw flagę, **Szacowanie** dla tej kategorii projektu. Następnie należy wybrać tę kategorię w zależności od wybranej reguły uzgadniania w wartości **Sprzedaż** pola **Zysk** dla określonego profilu kosztów projektu i przychodów.

### <a name="sample-configurations-for-project-cost-and-revenue-profiles"></a>Przykładowe konfiguracje profili kosztów projektu i przychodów

Rozliczanie według czasu i materiałów — brak PWT

![Profil kosztów i przychodów: czas i materiały — brak PWT](media/time-material-no-wip.png)

Czas i materiały — PWT (przychód)

![Profil kosztów i przychodów: czas i materiały — PWT](media/time-material-with-wip.png)

Stała cena — brak PWT

![Profil kosztów i przychodów: stała cena — brak PWT](media/fixed-price-no-wip.png)

Stała cena — kontrakt gotowy

![Profil kosztów i przychodów: stała cena — kontrakt gotowy](media/fixed-price-completed-contract.png)

Stała cena — wypełnienie procentowe

![Profil kosztów i przychodów: stała cena — wypełnienie procentowe](media/fixed-price-completed-percentage.png)


## <a name="accounting-event-examples-for-sample-project-cost-and-revenue-profiles"></a>Przykładowe wydarzenia księgowania profili kosztów projektu i przychodów.

| Wydarzenie dotyczące księgowania                  | Czas i materiał — brak PWT                       | Czas i materiał — PWT                                                                                           | Stała cena — brak PWT                                            | Stała cena — kontrakt gotowy                                                                            | Stała cena — wypełnienie procentowe                             |
|-----------------------------------|--------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| Generowanie arkuszy transakcji czasowych    | Obciążenie — koszt <br>Uznanie — alokacja płac          | Obciążenie — koszt <br>Uznanie — alokacja płac <br>Obciążenie — wartość sprzedaży PWT <br>Uznanie — wartość sprzedaży naliczonego przychodu                | Obciążenie — koszt <br>Uznanie — alokacja płac                         | Obciążenie — koszt <br>Uznanie — alokacja płac                                                                    | Obciążenie — koszt <br>Uznanie — alokacja płac                       |
| Generowanie transakcji wydatków | Obciążenie — koszt <br>Uznanie — konto rozliczeniowe dla wydatku | Obciążenie — koszt <br>Uznanie — konto rozliczeniowe dla wydatku <br>Obciążenie — wartość sprzedaży PWT <br>Uznanie — wartość sprzedaży naliczonego przychodu      | Obciążenie — koszt <br>Uznanie — konto rozliczeniowe dla wydatku                 | Obciążenie — koszt<br> Uznanie — konto rozliczeniowe dla wydatku                                                            | Obciążenie — koszt <br>Uznanie — konto rozliczeniowe dla wydatku               |
| Faktura dla klientów                | Obciążenie — saldo klienta <br>Uznanie — Zafakturowany przychód | Obciążenie — saldo klienta <br>Uznanie — Zafakturowany przychód <br>Uznanie — PWT wg wartości sprzedaży — Obciążenie — wartość sprzedaży naliczonego przychodu | Obciążenie — saldo klienta <br>Uznanie — Zafakturowany przychód — akonto | Obciążenie — saldo klienta <br>Uznanie — PWT — Zafakturowany przychód — akonto                                                  | Obciążenie — saldo klienta <br>Uznanie — PWT — Zafakturowane akonto    |
| Szacunek po przychodzie             | Nie dotyczy                                   | Nie dotyczy                                                                                                    | Nie dotyczy                                                  | Obciążenie — wartość kosztu PWT <br>Uznanie — koszt                                                                         | Obciążenie — PWT — wartość sprzedaży <br>Uznanie — wartość sprzedaży naliczonego przychodu |
| Eliminuj                         | Nie dotyczy                                   | Nie dotyczy                                                                                                    | Nie dotyczy                                                  | Uznanie — wartość kosztu PWT <br>Obciążenie — koszt <br>Uznanie — naliczony przychód — wartość sprzedaży <br>Obciążenie — Zafakturowane akonto PWT | Obciążenie — Zafakturowane akonto PWT <br>Uznanie — wartość sprzedaży PWT     |

## <a name="configure-project-cost-and-revenue-profile-rules"></a>Konfigurowanie reguł profilu kosztu projektu i przychodu

Reguły profilu koszt projektu i przychodu określają profil kosztu i przychodu projektu, który musi zostać użyty podczas przetwarzania transakcji projektu do zafakturowania. Zdefiniuj reguły, korzystając z opcji **Zarządzania projektami i ich księgowania** \> **Konfiguracja** \> **Księgowanie** \> **Reguły profilu kosztu projektu i przychodu**.

Reguły mogą być definiowane przez kontrakt dotyczący projektu, grupę projektów lub według określonego projektu. System będzie zawsze wybierał najbardziej dokładną regułę.
