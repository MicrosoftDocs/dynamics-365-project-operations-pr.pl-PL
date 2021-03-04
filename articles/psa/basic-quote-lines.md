---
title: Oferty i wiersze ofert
description: Ta temat zawiera informacje o ofertach i wierszach oferty.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 3/01/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 024a7cdb81340a077e839d92c4321c8b0051404b
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/10/2021
ms.locfileid: "5145146"
---
# <a name="quotes-and-quote-lines"></a>Oferty i wiersze ofert

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

W Dynamics 365 Project Service Automation istnieją dwa typy ofert: oferty projektu i oferty sprzedaży. Te dwa typy różnią się w następujących obszarach:

- W ofercie sprzedaży jest tylko jedna siatka dla pozycji. W ofercie projektu istnieją dwie siatki dla pozycji: jedna dla wierszy projektu, a druga dla wierszy produktów.
- Oferta sprzedaży obsługuje aktywację i poprawki. Oferta projektu nie obsługuje tych procesów.
- Istnieje możliwość dołączenia wielu zamówień do oferty sprzedaży. Do oferty projektu można dołączyć tylko jeden kontrakt dotyczący projektu.
- Istnieje możliwość wygrania oferty sprzedaży i zachowania pokrewnej szansy sprzedaży. Po wygraniu oferty projektu pokrewna szansa sprzedaży jest zamykana.
- Oferta sprzedaży nie zawiera żadnych pól i koncepcji zawartych w ofercie projektu. Pola obejmują **jednostkę kontraktującą**, **menedżera klienta** oraz **Imię i nazwisko kontaktu u płatnika**.  
- Oferty sprzedaży i oferty projektu są również identyfikowane za pośrednictwem pola opartego na zestawie opcji pod nazwą **Typ**. W przypadku oferty sprzedaży w tym polu jest określana wartość **na podstawie towaru**. W przypadku oferty projektu jest to wartość **na podstawie pracy**.

Temat ten będzie ukierunkowany na szczegółowe informacje o ofertach projektów.

Oferta projektu w programie PSA może zawierać wiele pozycji lub wierszy oferty. W rzeczywistości oferta projektu zawiera dwie siatki dla pozycji w wierszu. Jedna siatka jest oparta na wierszach opartych na projekcie, które umożliwiają szczegółowe oszacowanie. Druga siatka dotyczy wierszy opartych na produktach, które używają jednej ceny jednostkowej i podejścia opartego na ilościach.

- **Na podstawie projektu** — kwota (w cytowanych wartościach) jest określana po oszacowaniu ilości wymaganych prac. Można oszacować pracę na wysokim poziomie albo można oszacować ją bezpośrednio jako wiersz oferty poniżej każdego wiersza. Na koniec można oszacować prace na podstawie szacowań od podstaw, korzystając z planu projektu i projektu. Wiersze oferty oparte na projekcie są dostępne tylko w ofertach opartych na projekcie, które są tworzone przy użyciu rozwiązania Project Service Automation. Ten typ wiersza oferty jest dostosowaną formą wierszy oferty zapisu, które są dostępne w Microsoft Dynamics 365 Sales.
- **Na podstawie produktu** – kwota (w cytowanych wartościach) jest określana na podstawie ilości sprzedanych jednostek oraz jednostkowej ceny sprzedaży produktu. Produkt z wiersza opartego na produkcie może pochodzić z katalogu produktów w sprzedaży lub stanowić produkt definiowany przez użytkownika. Ten typ wiersza oferty jest także dostępny w ofertach opartych na projekcie, które są tworzone przy użyciu PSA.

Kwota oferty to suma w wierszach na podstawie produktu i na podstawie projektu.

> [!NOTE]
> Oferty i wiersze oferty nie są wymagane w PSA. Można rozpocząć proces projektu z kontraktem dotyczącym projektu (projektem sprzedawanym). Jednak szansa sprzedaży jest zawsze wymagana, bez względu na to, czy zaczyna się od oferty, czy do kontraktu dotyczącego projektu.

## <a name="project-based-quote-lines"></a>Wiersze ofert oparte na projekcie

Wiersz oferty opartej na projekcie w PSA ma następujące metody fakturowania:

- Czas i materiał
- Stała cena

### <a name="time-and-material"></a>Czas i materiał

Metoda fakturowania czasu i materiału jest oparta na zużyciu. Po wybraniu tej metody fakturowania będą wystawiane faktury dla klienta w miarę pojawiania siw kosztów w projekcie. Faktury są tworzone na podstawie okresowej częstotliwości opartej na datach. W trakcie procesu sprzedaży oferowana wartość komponentu typu czas i materiał daje tylko szacunek kosztów końcowych dla klienta. Dostawca nie zobowiązuje się do sfinalizowania projektu dokładnie za kwotę podaną w ofercie. Komponenty czasu i materiału zwiększają ryzyko po stronie klienta. Klienci mogą wynegocjować dodatkowe klauzule o limitach nie-do-przekroczenia, aby zminimalizować ich ryzyko. PSA nie obsługuje ustawiania klauzul nieprzekraczalności.

### <a name="fixed-price"></a>Stała cena

W metodzie fakturowania z ustaloną ceną dostawca zobowiązuje się do dostarczania do klienta projektu ze stałym kosztem. Klientowi jest wystawiany rachunek na oferowaną wartość wiersza oferty o stałej cenie, niezależnie od kosztów, które dostawca ponosi w celu dostarczenia danego wiersza oferty. Wartość wiersza oferty o stałej cenie jest rozliczana na jeden z następujących sposobów: 

- Suma ryczałtowa na początku lub na końcu projektu albo po osiągnięciu punktu kontrolnego projektu. 
- Na opartej na datach częstotliwościach równym stopom rat ustalonej wartości w wierszu oferty. Te raty są nazywane okresowymi punktami kontrolnymi.
- W ramach rat mających wartość pieniężną, która jest dostosowywana do postępu prac lub określonych punktów kontrolnych, które są osiągnięte w projekcie. W tym przypadku wartość każdej raty może się różnić, ale wszystkie muszą zostać dodane do ustalonej wartości w wierszu oferty.

PSA obsługuje wszystkie trzy typy harmonogramów fakturowania dla wierszy oferty o stałej cenie.

## <a name="transaction-classification"></a>Klasyfikacja transakcji

Profesjonalne organizacje obsługi klienta zazwyczaj składają oferty i wystawiają faktury swoim klientom według klasyfikacji kosztów. W przypadku PSA koszty są reprezentowane przez następujące klasyfikacje transakcji:

- **Czas** — ta klasyfikacja odzwierciedla koszt robocizny lub czasu zasobu ludzkiego w projekcie.
- **Wydatek**: — Ta klasyfikacja odzwierciedla wszystkie pozostałe rodzaje wydatków w projekcie. Ponieważ koszty mogą być szeroko zaklasyfikowane, większość organizacji tworzy podkategorie, takie jak podróże, wynajem samochodów, hotele lub materiały biurowe.
- **Opłata** — ta klasyfikacja reprezentuje narzuty dodatkowe, kary i inne pozycje obciążające klienta. 
- **Podatek** — ta klasyfikacja reprezentuje kwoty podatku dodawane przez użytkowników w czasie, gdy wprowadzają koszty.
- **Transakcja materiałowa** — ta klasyfikacja reprezentuje wartości rzeczywiste z wierszy produktów na potwierdzonej fakturze projektu.
- **Punkt kontrolny** — ta klasyfikacja jest używana przez logikę fakturowania według stałej ceny w PSA.

Jedną lub więcej klasyfikacji transakcji można skojarzyć z każdym wierszem oferty. Po wygraniu oferty mapowanie między wierszem klasyfikacji transakcji a pozycją oferty jest przenoszone do pozycji kontraktu.
 
> ![Zrzut ekranu z mapowaniami typów transakcji na oferty i pozycje kontraktu](media/basic-guide-5.png)
  
Na przykład oferta może zawierać następujące dwa wiersze: 
- Konsultacja, w której stosowana jest metoda fakturowania czasu i materiałów, w której stosuje się klasyfikacje dotyczące godzin i transakcji opłat. Na przykład wszystkie transakcje czasu i opłaty dotyczące przykładowego projektu **implementacji systemu Dynamics AX** są zafakturowane na klienta na podstawie użytego czasu i materiałów. 
- Pokrewne koszty podróży, które korzystają z metody fakturowania o stałej cenie. Na przykład wszystkie koszty podróży dla przykładowego projektu **implementacji Dynamics AX** są zafakturowane ze stałą wartością pieniężną.

> [!NOTE]
> Kombinacja projektów i klasyfikacji transakcji **czasu**, **wydatku** i **opłaty** skojarzonych z wierszem oferty lub pozycją kontraktu musi być unikatowa. Jeśli ta sama kombinacja klas projektów i transakcji jest skojarzona z więcej niż jedną pozycją kontraktu lub wierszem oferty, PSA nie będzie działać poprawnie.

## <a name="billing-types"></a>Typy rozliczania

W polu **Typ fakturowania** jest definiowana koncepcja ładowania PSA. To zestaw opcji o następujących możliwych wartościach:

- **Odpłatna** — koszt naliczany według tej roli/kategorii jest kosztem bezpośrednim, który polega na przeniesieniu wykonywania projektu, a klient ponosi wynagrodzenie za tę pracę. Płatność może być podawana jako układ czasu i materiału lub porozumienie o stałej cenie. Pracownik wykonujący tę godzinę otrzyma odpowiedni zwrot za jego lub jego zafakturowanego wykorzystania.
- **Nieodpłatna** — koszt naliczany według tej roli/kategorii jest kosztem bezpośrednim, który polega na przeniesieniu wykonywania projektu, nawet jeżeli klient nie płaci za tę pracę i nie rozpoznaje tego faktu. Pracownik, który spędza tę godzinę, nie zostanie zaksięgowany na potrzeby korzystania z fakturowania.
- **Uzupełnione** — koszt naliczany według tej roli/kategorii jest kosztem bezpośrednim, który polega na przeniesieniu wykonywania projektu, a klient rozpoznaje ten fakt. Pracownik, który spędza tę godzinę, zostanie zaksięgowany na potrzeby korzystania z fakturowania. Niemniej koszty te nie są naliczane klientowi.
- **Niedostępne** — przy użyciu tej opcji śledzone są koszty poniesione w ramach projektów wewnętrznych, które nie wymagają śledzenia przychodów.

## <a name="invoice-schedule"></a>Harmonogram fakturowania

Harmonogram fakturowania jest szeregiem dat podczas fakturowania w projekcie. Istnieje możliwość opcjonalnego utworzenia harmonogramu faktur w wierszu oferty programu PSA. Każdy wiersz oferty może mieć własny plan fakturowania. Aby utworzyć harmonogram fakturowania, należy określić następujące wartości atrybutów:

- Data rozpoczęcia rozliczania 
- Data dostawy oznaczająca datę zakończenia fakturowania projektu
- Częstotliwość faktur

Program PSA korzysta z tych trzech wartości atrybutów w celu wygenerowania wstępnie zdefiniowanego zestawu dat w celu ustalenia, czy fakturowanie ma zostać ustalone.

## <a name="invoice-frequency"></a>Częstotliwość faktur

Częstotliwość faktur to encja, w której są przechowywane wartości atrybutów ułatwiające wyrażanie częstotliwości tworzenia faktur. Poniższe atrybuty wyrażają lub definiują encję częstotliwości fakturowania:

- **Okres** — Obsługiwane są okresy w postaci comiesięcznej, dwutygodniowej i tygodniowej. 
- **Działa na okres** — na okres tygodniowy i dwutygodniowy można zdefiniować tylko jeden przebieg dla każdego okresu. W przypadku okresów miesięcznych można zdefiniować między jednym i czterema cyklami dla każdego okresu. 
- **Dni przebiegów** — dni, w których ma zostać wykonane fakturowanie. Możesz konfigurować ten atrybut na dwa różne sposoby:
  - **Dni tygodnia** — na przykład można wybrać, że fakturowanie będzie wykonywane co poniedziałek lub co drugi poniedziałek. Klienci, którzy muszą ustalić fakturę, która ma być uruchamiana w dniu roboczym, mogą preferować ten rodzaj konfiguracji. 
  - **Dni kalendarzowe** — można na przykład określić, że fakturowanie ma być wykonywane w siódmych i dwudziestych pierwszych dniach każdego miesiąca. W niektórych organizacjach ten rodzaj konfiguracji może być preferowany, ponieważ ułatwia zagwarantowanie, że fakturowanie jest wykonywane w ramach stałego harmonogramu co miesiąc.
  
### <a name="invoice-schedule-for-a-fixed-price-quote-line"></a>Harmonogram faktur dla wiersza oferty o stałej cenie

W przypadku wiersza oferty o stałej cenie można użyć siatki **harmonogramu faktur** do utworzenia punktów kontrolnych rozliczania, które są równe wartościom wiersza oferty.

- Aby utworzyć zestawienia faktur, które są równo podzielone, wybierz częstotliwość faktur, wprowadź datę rozpoczęcia fakturowania w wierszu oferty i wybierz **żądaną datę wykonania** dla oferty w sekcji **podsumowania** nagłówka oferty. Następnie należy wybrać opcję **generowania okresowych punktów kontrolnych** w celu utworzenia równo podziału punktów kontrolnych na podstawie wybranej częstotliwości faktur. 
- Aby utworzyć ryczałtowy punkt kontrolny, utwórz punkt kontrolny, a następnie wprowadź wartość w wierszu oferty jako wartość pola punkt kontrolny.
- W celu utworzenia punktów kontrolnych na podstawie określonych zadań w planie projektu utwórz punkt kontrolny i zamapuj go na element harmonogramu projektu w interfejsie użytkownika punktów kontrolnych fakturowania.


[!INCLUDE[footer-include](../includes/footer-banner.md)]