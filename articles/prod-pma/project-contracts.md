---
title: Kontrakty projektów
description: W tym temat przedstawiono przykłady kontraktów dotyczących projektów, które można tworzyć dla różnych typów projektów i źródeł finansowania oraz sposób zarządzania kontraktami i klientami projektu fakturowania.
author: Yowelle
ms.date: 11/03/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjProjectContractsListPage, ProjProjectsListPage
audience: Application User, IT Pro
ms.reviewer: johnmichalak
ms.custom: 23561
ms.assetid: bfd18d9b-d9a6-4e21-bc95-bf4af45f617f
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8cfc5183ce28574d865389eba72cafd3528741cc
ms.sourcegitcommit: 2c2a5a11d446adec2f21030ab77a053d7e2da28e
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 05/04/2022
ms.locfileid: "8683505"
---
# <a name="project-contracts"></a>Kontrakty projektów

[!include [banner](../includes/banner.md)]

W tym artykule przedstawiono przykłady kontraktów dotyczących projektów, które można tworzyć dla różnych typów projektów i źródeł finansowania oraz sposób zarządzania kontraktami i klientami projektu fakturowania.

Typ projektu utworzonego dla umowy dotyczącej projektu określa metodę używaną do fakturowania odbiorców projektu. Istnieje możliwość zmodyfikowania kontraktu projektu i powiązanego z nim projektu, ale nie można zmienić typu projektu. 

Korzystając z kontraktu projektu, można zafakturować jeden lub więcej projektów jednocześnie. Kontrakt dotyczący projektu ułatwia również zagwarantowanie spójnej procedury fakturowania dla każdego podprojektu w strukturze projektu. 

Każdy projekt, który ma zostać wystawiony, musi być skojarzony z kontraktem dotyczącym projektu. Ustawienia kontraktu dotyczącego projektu mają zastosowanie do wszystkich projektów i podprojektów skojarzonych z danym kontraktem dotyczącym projektu. 

Kontrakt dotyczący projektu może określać jeden lub więcej źródeł finansowania. Z tego względu można podzielić rozliczanie na wielu funduszach, skonfigurować limity finansowania, aby źródła finansowania nie były wystawiane więcej niż określona kwota, a także skonfigurować reguły finansowania dotyczące ładowania wydatków.

## <a name="funding-for-project-contracts"></a>Finansowanie kontraktów dotyczących projektów
Niektóre kontrakty dotyczące projektów określają, że w przypadku finansowania kosztów projektu wiele stron ma obowiązek podzielić się obowiązkiem. Oto kilka przykładów:

-   Duża wartość klienta mającego wielu działów wynosi zażądania podziału finansowania danego projektu na dział.
-   Firma współużytkuje koszty dużego projektu z zewnętrzną organizacją.
-   Projekt drogowy jest współfinansowany przez dwie gminy.
-   Projekt mostkowy jest finansowany przez władzę rządową i organizację prywatną.

W Dynamics 365 Finance można podzielić rozliczenie jednej transakcji lub całego projektu między wielu klientów, wiele grantów i organizacji. 

W projektach mających wielu funduszach wszystkie strony, które przynoszą finansowanie zaawansowanego projektu finansowania, noszą nazwę źródeł finansowania. Jeśli klient, organizacja lub dotacja została zdefiniowana jako źródło finansowania, może zostać przypisana do jednej lub więcej reguł finansowania. Reguły finansowania zawierają kryteria określające sposób przydzielania kosztów na różne źródła finansowania dotyczące danego projektu. 

Ze względu na fakt, że towary magazynowane, takie jak te, które są wyświetlane w założeniach zakupu i zamówieniach zakupu, nie mogą zostać podzielone, nie można ich podzielić na wiele źródeł finansowania w czasie dystrybucji. Dlatego wartość źródła finansowania pozostaje 0 (zero) do momentu zaksięgowania wydania magazynu. Po zaksięgowaniu rozchodu magazynowego koszt jest dystrybuowany zgodnie z regułami dystrybucji klientów dotyczącymi projektu.

Oto kilka kroków, które można podjąć w celu ułatwienia podziału rozliczenia między wiele źródeł finansowania:

-   Określa, że wszystkie transakcje wprowadzone dla projektu korzystają z tej samej waluty sprzedaży, co kontrakt dotyczący projektu.
-   Skonfiguruj limity finansowania, aby źródło finansowania nie było fakturowane na więcej niż określoną kwotę w ramach projektu.
-   Konfigurowanie reguł finansowania i ograniczeń finansowania dla każdego pracownika, elementu, kategorii, grupy kategorii i typu transakcji (lub we wszystkich typach transakcji).
-   Wybierz opcjonalne daty rozpoczęcia i zakończenia, aby zdefiniować okres, w którym każda reguła finansowania będzie ważna.
-   Podaj procent, za który jest odpowiedzialny każde źródło finansowania.
-   Określ, które źródło finansowania jest odpowiedzialne za różnice zaokrągleń wynikające z obliczeń alokacji finansowania.
-   Skonfiguruj reguły, które określają, w jaki sposób koszty projektu są fakturowane dla klientów zewnętrznych i naliczane organizacjom wewnętrznym.
-   Rejestruj transakcje na koncie ze środkami wstrzymanymi do czasu uzyskania dodatkowego finansowania lub do czasu, gdy zdecydujesz się pokryć koszty wewnętrznie.

Aby określić, która grupa podatkowa ma zostać powiązana z transakcją, w projekcie wyszukiwane jest przypisanie do grupy podatkowej. Jeśli na poziomie projektu nie dokonano przypisania grupy podatkowej, przeszukiwana jest umowa dotycząca projektu.

### <a name="example-multiple-funding-sources-simple"></a>Przykład: wiele źródeł finansowania (proste)

W poniższej tabeli przedstawiono scenariusze zarządzania alokacją środków na wiele źródeł finansowania. Te scenariusze są oparte na następujących założeniach:

-   Ustawienia priorytetów są uwzględniane przy alokacji środków przed zastosowaniem innych kryteriów reguły finansowania.
-   Nie podano zakresu dat w celu zdefiniowania okresu d, kiedy reguła finansowania jest prawidłowa.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<tbody>
<tr class="odd">
<td><strong>Scenariusz</strong></td>
<td><strong>Źródło finansowania</strong></td>
<td><strong>Procent alokacji</strong></td>
<td><strong>Priorytet alokacji</strong></td>
</tr>
<tr class="even">
<td>Chcesz przypisać koszty do jednego źródła finansowania aż do wyczerpania jego środków, przypisać koszty do drugiego źródła finansowania, aż do wyczerpania jego środków, a na koniec alokować pozostałe koszty do trzeciego źródła finansowania.</td>
<td><ul>
<li>Źródło　finansowania　1</li>
<li>Źródło　finansowania　2</li>
<li>Źródło　finansowania　3</li>
</ul></td>
<td><ul>
<li>100%</li>
<li>100%</li>
<li>100%</li>
</ul></td>
<td><ul>
<li>1</li>
<li>2</li>
<li>3</li>
</ul></td>
</tr>
<tr class="odd">
<td>Alokacja 75 procent kosztów do jednego źródła finansowania i 25 procent ma zostać zaalokowana do drugiego źródła finansowania. W przypadku wyczerpania któregokolwiek z tych źródeł finansowania użytkownik chce zapłacić pozostałe koszty w trzecim źródle finansowania.</td>
<td><ul>
<li>Źródło　finansowania　1</li>
<li>Źródło　finansowania　2</li>
<li>Źródło　finansowania　3</li>
</ul></td>
<td><ul>
<li>75%</li>
<li>25%</li>
<li>100%</li>
</ul></td>
<td><ul>
<li>1</li>
<li>1</li>
<li>2</li>
</ul></td>
</tr>
<tr class="even">
<td>Alokacja 75 procent kosztów do jednego źródła finansowania i 25 procent ma zostać zaalokowana do drugiego źródła finansowania. Gdy jedno z tych źródeł finansowania zostanie wyczerpane, chcesz podzielić pozostałe koszty między trzecie i czwarte źródło finansowania.</td>
<td><ul>
<li>Źródło　finansowania　1</li>
<li>Źródło　finansowania　2</li>
<li>Źródło　finansowania　3</li>
<li>Źródło　finansowania　4</li>
</ul></td>
<td><ul>
<li>75%</li>
<li>25%</li>
<li>50%</li>
<li>50%</li>
</ul></td>
<td><ul>
<li>1</li>
<li>1</li>
<li>2</li>
<li>2</li>
</ul></td>
</tr>
<tr class="odd">
<td>Chcesz przeznaczyć pierwsze 25% kosztów na jedno źródło finansowania, a resztę na drugie źródło finansowania.</td>
<td><ul>
<li>Źródło　finansowania　1</li>
<li>Źródło　finansowania　2</li>
</ul></td>
<td><ul>
<li>25%</li>
<li>100%</li>
</ul></td>
<td><ul>
<li>1</li>
<li>2</li>
</ul></td>
</tr>
</tbody>
</table>

### <a name="example-multiple-funding-sources-complex"></a>Przykład: wiele źródeł finansowania (złożone)

Istnieją trzy źródła finansowania, które mają zostać użyte w następującej kolejności:

1.  Źródła finansowania 2 i źródło finansowania 3 należy stosować po równo do wyczerpania źródła finansowania 2.
2.  Kontynuuj korzystanie ze źródła finansowania 3, aż zostanie wyczerpane.
3.  Użyj źródła finansowania 1 po wyczerpaniu źródła finansowania 3.

Aby osiągnąć ten cel, musisz wykonać następujące czynności:

-   Ustal limity finansowania dla źródła finansowania 2 i źródła finansowania 3 dla ich odpowiednich kwot.
-   Utwórz następujące zasady finansowania:
    -   Reguła 1 (priorytet 1): Alokacja 50 procent transakcji do źródła finansowania 2 i 50 procent do źródła finansowania 3.
    -   Reguła 2 (priorytet 2): alokowanie 100 procent transakcji dla źródła finansowania 3.
    -   Reguła 3 (priorytet 3): alokowanie 100 procent transakcji dla źródła finansowania 1.

Ta instalacja działa, ponieważ sprawdzanie transakcji względem reguł i ograniczeń polega na określeniu, czy którykolwiek z nich ma zastosowanie do transakcji. Jeśli do transakcji nie są stosowane żadne konkretne reguły lub ograniczenia, stosowana jest reguła Wszystkie transakcje. Reguła Wszystkich transakcji jest zgodna ze wszystkimi transakcjami. 

Jeśli zostanie znaleziona reguła, która pasuje do transakcji, wartość procentowa, która została przydzielona w tej regule, jest stosowana jako pierwsza, ale dopiero po sprawdzeniu zgodności z wszelkimi ustawionymi limitami. Jeśli limit został osiągnięty, a środki źródła finansowania są wyczerpane, reguła finansowania powiązana z limitem finansowania jest ignorowana, a program sprawdza następną regułę, która ma zastosowanie. 

W niektórych przypadkach tylko część transakcji może zostać zaalokowana na regułę. Powodem może być to, że podczas alokowania transakcji został osiągnięty limit. W tym przypadku tylko pewna kwota jest alokowana według tej reguły, na przykład do 50 procent dla każdego źródła finansowania. Tak jest w zasadzie 1, która jest opisana we wcześniejszej części tej sekcji. Pozostała część jest alokowana według następnej reguły w sekwencji. 

Poniższa tabela zawiera szczegółowe informacje o tym scenariuszu.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><strong>Fokus</strong></td>
<td><strong>Szczegóły</strong></td>
</tr>
<tr class="even">
<td>Reguły finansowania</td>
<td><ul>
<li>Reguła 1 (priorytet 1): wszystkie transakcje. Przydziel źródło finansowania 2 na 50% i źródło finansowania 3 na 50%.</li>
<li>Reguła 2 (priorytet 2): wszystkie transakcje. Przydziel Źródło finansowania 3 na 100%.</li>
<li>Reguła 3 (priorytet 2): wszystkie transakcje. Przydziel Źródło finansowania 1 na 100%.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Limity finansowania</td>
<td><ul>
<li>Limit źródła finansowania 1 = 10 000,00</li>
<li>Limit źródła finansowania 2 = 500,00</li>
<li>Limit źródła finansowania 3 = 750,00</li>
</ul></td>
</tr>
<tr class="even">
<td>Transakcja 1</td>
<td><strong>Kwota transakcji:</strong> 100,00<strong>Fundusze:</strong> Transakcja jest płatna zgodnie z regułą 1, ponieważ transakcja jest całkowicie zapłacona po zastosowaniu reguły 1. Transakcja jest finansowana równo między źródłem finansowania 2 a źródłem finansowania 3.
<ul>
<li>Źródło finansowania 2: 50,00</li>
<li>Źródło finansowania 3: 50,00</li>
</ul></td>
</tr>
<tr class="odd">
<td>Transakcja 2</td>
<td><strong>Kwota transakcji:</strong> 5 000,00<strong>Finansowanie:</strong> Transakcja jest wypłacana według wszystkich trzech reguł. <strong>Reguła 1</strong>
<ul>
<li>Źródło finansowania 2: 450,00</li>
<li>Źródło finansowania 3: 450,00</li>
</ul>
<strong>Reguła 2</strong>
<ul>
<li>Źródło finansowania 3: 250,00 (= 750,00 - 50,00 - 450,00)</li>
</ul>
<strong>Reguła 3</strong>
<ul>
<li>Źródło finansowania 1: 3850,00 (= 5000,00 - 450,00 - 450,00 - 250,00)</li>
</ul></td>
</tr>
<tr class="even">
<td>Suma środków dystrybuowanych na każde źródło finansowania</td>
<td><ul>
<li>Źródło finansowania 1: 3 850,00</li>
<li>Źródło finansowania 2: 500,00</li>
<li>Źródło finansowania 3: 750,00</li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="billing-rules"></a>Reguły fakturowania
Podczas negocjowania kontraktu dotyczącego projektu z klientem użytkownik określa, jak i kiedy można zafakturować klienta w celu wykonania prac nad projektem. Po skonfigurowaniu kontraktu projektu i projektu można skonfigurować reguły fakturowania dla projektu. Reguły fakturowania są tworzone na podstawie terminów projektu określonych w kontrakcie dotyczącym projektu. Reguły fakturowania, które można utworzyć, zależą od warunków umowy dotyczącej projektu i typu projektu, takiego jak czas i materiał lub stała cena, który jest skojarzony z regułą fakturowania. Dla kontraktu dotyczącego projektu można utworzyć więcej niż jedną regułę fakturowania. Możesz również przypisać regułę fakturowania do wielu projektów, które są skojarzone z tą samą umową dotyczącą projektu i mają podobne warunki płatności. 

Użytkownik może zdefiniować następujące typy reguł fakturowania:

-   **Jednostka dostawy** — Faktura dla klienta po wykonaniu jednostki dostawy. Jednostki dostawy są definiowane w kontrakcie.
-   **Postęp** — wystawianie faktury dla klienta po wykonaniu określonej wartości procentowej projektu. Użytkownik może skonfigurować regułę fakturowania, aby automatycznie obliczać procent wykonanej pracy, lub ręcznie obliczyć procent wykonania pracy oraz kwotę, aby zafakturować klienta.
-   **Punkt kontrolny** — Faktura dla klienta w celu uzyskania pełnej kwoty punktów kontrolnych projektu, gdy zostanie osiągnięty punkt kontrolny.
-   **Opłata** — Faktura klienta dla usługi wraz z opłatą za zarządzanie, czyli zazwyczaj procent kosztu usług.
-   **Czas i materiały** — Faktura klienta dla wartości czasu i materiałów używanych w projekcie.

W przypadku wszystkich typów reguł rozliczeniowych można określić procent zatrzymania, który jest odejmowany od faktur klientów, dopóki projekt nie osiągnie uzgodnionego etapu. Procent zatrzymania płatności jest określany w kontrakcie projektu. Kwota jest obliczana na podstawie i odjęta od wartości łącznej wierszy na fakturze dla klienta. 

Aby zmienić reguły fakturowania **Czasu i materiału** oraz **Postępu**, można przypisać kategorie wymagalności. Kategorie podlegające opłacie wskazują transakcje, które powinny być uwzględnione na fakturach odbiorcy. 

Gdy jesteś gotowy do wystawienia faktury na klienta, kwota do faktury za projekt jest obliczana na podstawie reguł fakturowania i generowana jest propozycja faktury za projekt. 

Poniższe sekcje zawierają przykłady dotyczące konfigurowania reguł fakturowania i zarządzania nimi.

### <a name="example-create-a-billing-rule-that-is-based-on-the-number-of-units-delivered"></a>Przykład: Tworzenie reguły fakturowania opartej na liczbie dostarczonych jednostek

Organizacja wejdzie w umowę w celu udzielenia łącznej liczby pięciu sesji szkoleniowych pracownikom klienta z kosztem 10 000 na sesję szkoleniową. Klient otrzymuje wystawioną fakturę po każdej sesji szkoleniowej. 

Konfigurując reguły fakturowania dla kontraktu, należy użyć następujących wartości:

-   Jednostką z dostawy jest jedna sesja szkoleniowa.
-   Cena jednostkowa wynosi 10 000 na sesję szkoleniową.
-   Łączna liczba jednostek wynosi pięć sesji szkoleniowych.

Po ukończeniu jednej sesji szkoleniowej możesz utworzyć fakturę na 10 000 za pierwszą dostarczoną jednostkę i wysłać fakturę do klienta.

### <a name="example-create-a-billing-rule-that-is-based-on-a-specified-percentage-of-project-completion-manual-calculation"></a>Przykład: Utwórz regułę rozliczeniową opartą na określonym odsetku ukończenia projektu (obliczenie ręczne)

Twoja organizacja, firma konsultingowa w zakresie oprogramowania, zawiera umowę z klientem na opracowanie części produktu, który ten klient opracowuje. Twoja organizacja zgadza się dostarczać kod oprogramowania przez okres sześciu miesięcy. Klient zgadza się zapłacić za tę pracę organizacji sumę 100 000. Tworzysz regułę fakturowania, aby fakturować klienta na podstawie procentu pracy wykonanej w projekcie, zgodnie z umową.

-   Pod koniec pierwszego miesiąca spotykasz się z klientem, aby określić procent wykonanej pracy. Po przejrzeniu projektu z klientem decydujesz, że projekt został ukończony w 15%.
-   Tworzysz fakturę na 15 000 (15% ze 100 000) i wysyłasz ją do klienta.

### <a name="example-create-a-billing-rule-that-is-based-on-a-specified-percentage-of-project-completion-automatic-calculation"></a>Przykład: Utwórz regułę rozliczeniową opartą na określonym odsetku ukończenia projektu (obliczenie automatyczne)

Twoja organizacja, firma programistyczna, zgadza się opracować pakiet rozliczeń płac dla klienta za 30 000. Klient zgadza się zapłacić Twojej organizacji na podstawie procentu wykonanej pracy. Szacujemy, że koszty projektów są 20 000. Kontrakt dotyczący projektu określa kategorie pracy używane w procesie fakturowania. Skonfigurujesz reguły rozliczeniowe, które automatycznie obliczają kwoty faktur dla procentu pracy wykonanej dla każdej kategorii. Użytkownik konfiguruje budżet dla każdej kategorii.

-   **Opracowywanie** — koszt 15 000 i przychód 20 000
-   **Instalacja** — koszt 5 000 i przychód 10 000

Podczas tworzenia faktury dla odbiorcy po raz pierwszy kwota faktury jest obliczana automatycznie na podstawie następujących informacji:

-   Po upływie miesiąca pracownik projektu przesyła grafik do projektu. Koszt godzin pracy pracownika wynosi 5 000 w przypadku opracowania i 1 000 instalacji. Prace rozwojowe ukończono w 33% (5000 kosztów rzeczywistych/15000 kosztów budżetowych), a prace instalacyjne ukończono w 20% (1000 kosztów rzeczywistych/5000 kosztów budżetowych).
-   Kwota faktury 8 667 jest obliczana automatycznie (33 procent z 20 000 + 20 procent z 10 000).
-   Tworzysz fakturę na 8667 i wysyłasz ją do klienta.

### <a name="example-create-a-billing-rule-that-is-based-on-agreed-upon-milestones"></a>Przykład: Tworzenie reguły fakturowania opartej na uzgodnionych punktach kontrolnych

Twoja organizacja, firma konsultingowa w zakresie zarządzania, zgadza się na przeprowadzenie badań rynkowych produktu konsumenckiego, który klient planuje sprzedać. Klient zgadza się korzystać z Twoich usług przez okres trzech miesięcy, począwszy od marca, i zgadza się zapłacić Twojej organizacji 50 000. Projekt ma trzy punkty kontrolne:

-   Punkt kontrolny 1: zbieranie danych o klientach – 31 marca
-   Punkt kontrolny 2: analizowanie danych o klientach — 30 Kwiecień
-   Punkt kontrolny 3: Przedstaw propozycję opłacalności produktu — 31 maja

Klient zgadza się zapłacić Twojej organizacji 10 000 za pierwszy kamień milowy, 20 000 za drugi i 20 000 za trzeci. 

Podczas konfigurowania kontraktu dotyczącego projektu użytkownik zgadza się wystawić fakturę na podstawie spełnionego punktu kontrolnego. Konfiguracja reguły fakturowania obejmuje następujące kroki:

-   Definiowanie punktów kontrolnych projektu.
-   W tym polu należy zdefiniować kwotę, która ma zostać zafakturowana dla klienta po zakończeniu poszczególnych punktów kontrolnych.

Gdy pierwszy kamień milowy zostanie ukończony 31 marca, oznaczasz go jako ukończony, a następnie tworzysz fakturę na 10 000 i wysyłasz ją do klienta. Nie możesz utworzyć faktury za kamień milowy, dopóki nie oznaczysz go jako ukończonego.

### <a name="example-create-a-billing-rule-that-is-based-on-services-plus-a-management-fee"></a>Przykład: Utwórz regułę rozliczeń opartą na usługach plus opłata za zarządzanie

Twoja organizacja, firma konsultingowa w zakresie zarządzania, zgadza się na przeprowadzenie badań rynkowych w celu oceny rentowności produktu opracowywanego przez klienta, firmę zajmującą się sprzedażą detaliczną. Warunki umowy określają, że będziesz świadczył usługi trzech najlepszych konsultantów ds. Zarządzania, którzy przeprowadzą badanie na podstawie czasu i materiałów. Klient zgadza się zapłacić 100 za godzinę plus 10 procent opłaty za zarządzanie za godziny konsultacji naliczane w ramach projektu. 

Podczas konfigurowania umowy dotyczącej projektu utwórz regułę fakturowania, aby dodać 10-procentową opłatę za zarządzanie do godzin konsultacji naliczanych w ramach projektu. 

Kiedy tworzysz fakturę dla klienta, klient jest obciążany 10-procentową opłatą za zarządzanie plus koszt godzin konsultacji. Na przykład, jeśli trzech konsultantów przepracowało łącznie 200 godzin nad projektem, faktura na 22 000 jest tworzona na podstawie następujących obliczeń:

-   200 godzin za 100 na godzinę = 20 000
-   10 procent opłaty za zarządzanie = 2 000
-   Łączna kwota na fakturze = 22 000

Jeśli opłaty podlegają opodatkowaniu dla odbiorcy i wybierzesz grupę podatków w umowie dotyczącej projektu, grupa podatków zostanie automatycznie wprowadzona do reguły rozliczeniowej dla opłat.

### <a name="example-create-a-billing-rule-for-the-value-of-time-and-materials"></a>Przykład: Utwórz regułę rozliczeniową dla wartości czasu i materiałów

Twoja organizacja, firma konsultingowa w zakresie oprogramowania, zgadza się zapewnić pięciu konsultantów technicznych do pracy nad projektem rozwoju oprogramowania dla klienta przez następne sześć miesięcy. Klient zgadza się na płatę kwoty 150 za każdą godzinę konsultacji, a także koszt materiałów biurowych. Na koniec każdego miesiąca organizacja wysyła fakturę do klienta. 

Konfigurując umowę dotyczącą projektu, zgadzasz się co miesiąc wystawiać klientowi fakturę za czas i materiały związane z projektem. Użytkownik tworzy regułę fakturowania zawierającą następujące informacje:

-   Okres objęty umową wynosi sześć miesięcy.
-   Czas konsultacji jest obliczany na podstawie stawki 150 na godzinę.
-   Materiały biurowe są fakturowane po kosztach, a całkowity koszt projektu nie może przekraczać 10 000.
-   Tworzysz fakturę dla klienta na koniec każdego miesiąca kalendarzowego w trakcie trwania projektu.

W pierwszym miesiącu konsultanci projektu rejestrują łącznie 800 godzin. Koszt materiałów biurowych obciążających projekt wynosi 2000. Dlatego na koniec miesiąca tworzysz fakturę na 122 000, która jest obliczana jako 800 godzin przy 150 na godzinę plus 2 000 na materiały biurowe.





[!INCLUDE[footer-include](../includes/footer-banner.md)]