---
title: Zarządzanie fakturą proforma opartej na projekcie
description: W tym artykule podano informacje na temat sposobu zarządzania fakturami proforma opartymi na projektach i pracy z nimi.
author: rumant
ms.date: 04/05/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 31822947a4fbb60218ce1c3c9415a60491f6d8fa
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8932125"
---
# <a name="manage-a-proforma-project-based-invoice"></a>Zarządzanie fakturą proforma opartej na projekcie

_**Zastosowane do:** Project Operations dla zasobów/scenariuszy nieopartych na zaopatrzeniu_

W rozwiązaniu Dynamics 365 Project Operations faktury proforma są budowane jako rozszerzenie faktur w Dynamics 365 Sales. However, there are many differences in the invoicing process between Sales i Project Operations when it comes to invoicing. Nie można na przykład utworzyć nowej faktury na stronie **Listy faktur** w Project Operations, ale może to zrobić w przypadku sprzedaży. Te różnice i rozszerzenia służą do obsługi procesów fakturowania projektów, które różnią się od typowej faktury za zamówienie sprzedaży.

> [!IMPORTANT]
> Ze względu na różnice między Sales i Project Operations nie można zamiennie używać faktur.

## <a name="invoice-header"></a>Nagłówek faktury

Poniższe informacje są dostępne w nagłówku faktury proforma w Project Operations.

| Pole | Lokalizacja | Opis |
| --- | --- | --- | 
| **Identyfikator faktury** | Karta **Podsumowanie** | Identyfikator generowany automatycznie podczas tworzenia faktury proforma. Pole tylko do odczytu, które można edytować jako zablokowane. To pole służy jako odniesienie dla każdej faktury proforma. |
| **Nazwa/nazwisko** | Karta **Podsumowanie** | Ustaw domyślnie nazwę umowy dotyczącej projektu. Pole to można edytować. | 
| **Waluta** | Karta **Podsumowanie** | Ustaw domyślnie walutę dotyczącą projektu. Pole tylko do odczytu, które można edytować jako zablokowane. |
| **Cennik** | Karta **Podsumowanie** | Ustaw domyślnie cennik dotyczący projektu. Pole tylko do odczytu, które można edytować jako zablokowane. | 
| **Szansa sprzedaży** | Karta **Podsumowanie** | Odwołanie do połączonej szansy sprzedaży. Pole tylko do odczytu, które można edytować jako zablokowane. | 
| **Kontrakt** | Karta **Podsumowanie** | Odniesienie do połączonej umowy dotyczącej projektu. Pole tylko do odczytu, które można edytować jako zablokowane. | 
| **Klient** | Karta **Podsumowanie** | Odniesienie do połączonej umowy dotyczącej projektu. Pole tylko do odczytu, które można edytować jako zablokowane. |
| **Opis** | Karta **Podsumowanie** | Pole tekstowe, które opisuje fakturę. Pole to można edytować. | 
| **Adres płatnika** i pokrewne pola | **Karta Podsumowanie** | Wartości domyślne są ustawiane przez klienta umowy projektu. Pole to można edytować.  | 
| **Status** | Karta **Podsumowanie** | Ustawia następujące opcje: **Aktywne**, **Zamknięte**, **Zapłacone** i **Anulowane**, i można je edytować. Nieobsługiwane stany Project Operations zawierają **Zamknięte** i **Anulowane**. </br> Stan jest ustawiany na **Aktywny** w czasie tworzenia faktury. </br>Stan powinien zostać ustawiony na **Zapłacony** tylko po potwierdzeniu faktury.  | 
| **Stan faktury projektu** | Karta **Podsumowanie** | Ustawia następujące opcje: **Wersja robocza**, **W trakcie przeglądu** i **Potwierdzone**, i można je edytować. W obydwu stanach **Wersja robocza** i **W trakcie przeglądu** faktura może być edytowana. Faktura nie może być edytowana po jej potwierdzeniu. | 
| **Kwota szczegółowa** | Karta **Podsumowanie** | Suma kwot we wszystkich wierszach faktury po zaliczkach i potrąceniach. Pole tylko do odczytu, które można edytować jako zablokowane.  To pole jest używane do obliczania kwoty końcowej. | 
| **Rabat (%)** | Karta **Podsumowanie** | To pole można edytować, aby wprowadzić stawkę procentową rabatu. To pole nie jest obsługiwane przez funkcje Project Operations. To jest nieobsługiwane pole.|  
| **Kwota rabatu** | Karta **Podsumowanie** | To pole można edytować, aby wprowadzić kwotę rabatu. To pole nie jest obsługiwane przez funkcje Project Operations. To jest nieobsługiwane pole. |  
| **Kwota bez frachtu** | **Karta Podsumowanie** | Łączna kwota faktury po zastosowaniu rabatów. Pole tylko do odczytu, które można edytować jako zablokowane. To pole jest używane do obliczania kwoty końcowej.  | 
| **Kwota frachtu** | Karta **Podsumowanie** | To pole można edytować, aby wprowadzić kwotę frachtu. To pole nie jest obsługiwane przez funkcje Project Operations. To jest nieobsługiwane pole. |
| **Łączny podatek** | Karta **Podsumowanie** | Całkowity podatek ze wszystkich pozycji faktury na fakturze. Pole tylko do odczytu, które można edytować jako zablokowane. | 
| **Łączna kwota** | Karta **Podsumowanie** | Suma kwot po rabatach i podatkach. Suma oznacza kwotę, jaką musi zapłacić klient. | 

## <a name="project-based-invoice-lines"></a>Wiersze faktur na podstawie projektu

W Project Operations zawsze istnieje jeden wiersz faktury dla każdego wiersza umowy dotyczącej projektu. Wiersz faktury zostanie utworzony nawet w przypadku braku wartości rzeczywistych. Poniższe informacje są dostępne w wierszu faktury proforma.

| Pole | Lokalizacja | Opis | 
| --- | --- | --- |
| **Identyfikator faktury** | Karta **Ogólne** | Odwołanie do identyfikatora faktury. Pole tylko do odczytu, które można edytować jako zablokowane. Link do identyfikatora faktury umożliwia powrót do nagłówka faktury. | 
| **Nazwa/nazwisko** | Karta **Ogólne** | Nazwa wiersza faktury ustawiona domyślnie na podstawie nazwy pozycji kontraktu. Pole to można edytować. |
| **Project** | Karta **Ogólne** | Projekt w pokrewnej pozycji kontraktu projektu. Pole tylko do odczytu, które można edytować jako zablokowane. Za pomocą łącza do projektu można przechodzić do projektu. | 
| **Metoda rozliczania** | Karta **Ogólne** | Metoda rozliczania w pokrewnej pozycji kontraktu projektu. Pole tylko do odczytu, które można edytować jako zablokowane. |
| **Kwota pozycji kontraktu** | Karta **Ogólne** | Kwota umowy w powiązanej pozycji kontraktu projektu. Pole tylko do odczytu, które można edytować jako zablokowane. | 
| **Zafakturowano do daty** | Karta **Ogólne** | Suma kwot wszystkich informacji dotyczących wiersza faktury. Pole tylko do odczytu, które można edytować jako zablokowane. | 
| **Kwota** | Karta **Ogólne** | Suma kwot wszystkich danych wiersza faktury podlegającej opłacie na tej fakturze. Pole tylko do odczytu, które można edytować jako zablokowane. To pole jest używane do obliczania kwoty końcowej w nagłówku faktury. | 
| **Podatek** | Karta **Ogólne** | Suma kwot podatku dotyczących wiersza faktury dla tego wiersza faktury. Pole tylko do odczytu, które można edytować jako zablokowane. To pole jest używane do obliczania końcowej kwoty podatku w nagłówku faktury. | 
| **Kwota rozszerzona** | Karta **Ogólne** | Suma całkowitych kwot (**Podatek + Kwoty**) wszystkich szczegółów linii faktury podlegających opłacie w tym wierszu faktury. Pole tylko do odczytu, które można edytować jako zablokowane. To pole jest używane do obliczania kwoty końcowej w nagłówku faktury. |

## <a name="invoice-line-details"></a>Szczegóły wiersza faktury

Każdy wiersz faktury na fakturze projektu zawiera szczegóły wiersza faktury. Te szczegóły wierszy są powiązane z wartościami rzeczywistymi i punktami kontrolnymi niefakturowanymi, które są powiązane z pozycją kontraktu, do której odwołuje się wiersz faktury. Wszystkie te transakcje są oznaczone jako **Przygotowane do fakturowania**.

W przypadku wiersza **Faktura czasowa i materiałowa** szczegóły wiersza faktury są zgrupowane jako **Odpłatne**, **Nieodpłatne** i **Bezpłatne** na stronie **Wiersz faktury**. Szczegóły **Wypłacanego wiersza na fakturze** są dodawane do sumy wiersza faktury. **Uzupełniające** i **Wartości rzeczywiste niepodlegające obciążeniu** nie są dodawane do sumy wiersza faktury.

W przypadku wiersza **Faktura ze stalą ceną** szczegóły wiersza faktury są tworzone na podstawie punktów kontrolnych oznaczonych jako **Gotowe do zafakturowania** w powiązanym wierszu umowy. Po utworzeniu szczegółów wiersza faktury z punktu kontrolnego stan fakturowania w punktach kontrolnych zostanie zaktualizowany na podstawie **Utworzono fakturę dla klienta**.

### <a name="edit-invoice-line-details"></a>Edytuj szczegóły linii faktury

Następujące pola są dostępne w szczegółach wiersza faktury, które są poparte niezafakturowaną faktyczną sprzedażą.

| Pole | Opis |
| --- | --- | 
| **Identyfikator wiersza** | Odwołanie do **Identyfikatora wiersza faktury**. To pole jest tylko do odczytu i zablokowane do edycji. Ten link umożliwia powrót do nagłówka faktury. | 
| **Opis** | Opis szczegółów wiersza faktury. Domyślne ustawienie jest ustawiane na podstawie pola **Komentarze wewnętrzne** w **Wpis czasu** oraz pola **Opis** w **Wpis wydatków**. Pole to można edytować.| 
| **Opis zewnętrzny** | Opis szczegółów wiersza faktury. Domyślne ustawienie jest ustawiane na podstawie pola **Komentarze zewnętrzne** w **Wpis czasu** oraz pola **Opis** w **Wpis wydatków**. Pole to można edytować. Na podstawie tego opisu można określić, co powinno znajdować się na wydrukowanej fakturze, która zostanie wysłana do klienta. W Project Operations faktura proforma nie ma wszystkich funkcji wymaganych do skonfigurowania ustawień drukowania faktury. | 
| **Data rozpoczęcia** | Jest to pole tylko do odczytu, które jest domyślnie ustawione na podstawie rzeczywistego źródła. |
| **Project** | Jest to pole tylko do odczytu, które jest domyślnie ustawiane od rzeczywistego źródła do projektu w powiązanym wierszu umowy. |  
| **Zadanie** | Domyślnie jest ustawiona wartość z wartości źródłowej. Pole tylko do odczytu, które można edytować jako zablokowane. |
| **Kategoria transakcji** | Domyślnie jest ustawiona wartość z wartości źródłowej. Pole tylko do odczytu, które można edytować jako zablokowane. | 
| **Rola** | Domyślnie jest ustawiona wartość z wartości źródłowej. Pole tylko do odczytu, które można edytować jako zablokowane. |  
| **Zasób, który można zarezerwować** | Domyślnie jest ustawiona wartość z wartości źródłowej. Pole tylko do odczytu, które można edytować jako zablokowane. | 
| **Firma zasobów** | Domyślnie jest ustawiona wartość z wartości źródłowej. Pole tylko do odczytu, które można edytować jako zablokowane. | 
| **Jednostka zasobów** | Domyślnie jest ustawiona wartość z wartości źródłowej. Pole tylko do odczytu, które można edytować jako zablokowane. | 
| **Ilość** | Domyślnie jest ustawiona wartość z wartości źródłowej. Pole tylko do odczytu, które można edytować jako zablokowane. |  
| **Harmonogram jednostek** | W przypadku szczegółów wiersza faktury dla czasu jest zawsze ustawiony czas i nie można jej edytować. W przypadku wydatków jest ono domyślnie ustawiane na podstawie wartości w polu kosztów źródłowych. Pole tylko do odczytu, które można edytować jako zablokowane. | 
| **Jednostka** | Domyślnie jest ustawiona wartość z wartości źródłowej. Pole tylko do odczytu, które można edytować jako zablokowane. |  
| **Cena** | Domyślnie jest ustawiona wartość z wartości źródłowej. Pole tylko do odczytu, które można edytować jako zablokowane. |
| **Waluta** | Domyślnie jest ustawiona wartość z wartości źródłowej. Pole tylko do odczytu, które można edytować jako zablokowane. | 
| **Kwota** | Domyślnie jest ustawiona wartość z wartości źródłowej. Pole tylko do odczytu, które można edytować jako zablokowane. | 
| **Podatek** | Domyślnie jest ustawiona wartość z wartości źródłowej. Pole to można edytować.| 
| **Wartość** | Pole obliczane, które jest obliczane jako **Kwota + podatek**. Pole tylko do odczytu, które można edytować jako zablokowane. | 
| **Typ rozliczeń** | Domyślnie jest ustawiona wartość z wartości źródłowej. Pole to można edytować. Wybranie opcji **Płatny** powoduje dodanie wiersza do sumy wiersza faktury. **Uzupełniające** i **Nieodpłatne** wykluczą go z sumy wiersza faktury.| 
| **Wybierz produkt** | Domyślnie jest ustawiona wartość z wartości źródłowej. Pole tylko do odczytu, które można edytować jako zablokowane. |
| **Produkt** | Domyślnie jest ustawiona wartość z wartości źródłowej. Pole tylko do odczytu, które można edytować jako zablokowane. | 
| **Nazwa produktu** | Domyślnie jest ustawiona wartość z wartości źródłowej. Pole tylko do odczytu, które można edytować jako zablokowane. |  
| **Opis dopisanego** | Domyślnie jest ustawiona wartość z wartości źródłowej. Pole tylko do odczytu, które można edytować jako zablokowane. |
| **Typ transakcji** | To jest pole tylko do odczytu, które jest domyślnie ustawiane z rzeczywistego źródła na **Fakturowana sprzedaż**. |  
| **Klasa transakcji** | Domyślnie jest ustawiona wartość z wartości źródłowej. Pole tylko do odczytu, które można edytować jako zablokowane. | 

Następujące pola są dostępne w szczegółach wiersza faktury, które są poparte punktem kontrolnym.

| Pole | Opis |
| --- | --- | 
| **Identyfikator wiersza** | Odwołanie do **Identyfikatora wiersza faktury**. Pole tylko do odczytu, które można edytować jako zablokowane. Ten link umożliwia powrót do nagłówka faktury.  | 
| **Opis** | Opis szczegółów wiersza faktury. Domyślnie jest ustawiona wartość na podstawie opisu źródłowego punktu kontrolnego. | 
|**Opis zewnętrzny** | Opis szczegółów wiersza faktury ustawiany domyślnie na podstawie opisu źródłowego punktu kontrolnego. Na podstawie tego pola można określić, co powinno znajdować się na wydrukowanej fakturze, która zostanie wysłana do klienta. Faktura proforma w Project Operations nie ma wszystkich funkcji wymaganych do skonfigurowania ustawień drukowania faktury. | 
| **Data rozpoczęcia** | Domyślnie jest ustawiana wartość z daty **Punktów kontrolnych** we źródłowym punktach kontrolnych. Pole tylko do odczytu, które można edytować jako zablokowane. | 
| **Project** | Domyślnie jest ustawiona wartość z punktu kontrolnego. Pole tylko do odczytu, które można edytować jako zablokowane. |
| **Zadanie** | Domyślnie jest ustawiona wartość z punktu kontrolnego. Pole tylko do odczytu, które można edytować jako zablokowane. | 
| **Kategoria transakcji** | Pole tylko do odczytu, które można edytować jako zablokowane. |
| **Rola** | Pole tylko do odczytu, które można edytować jako zablokowane. | 
| **Zasób, który można zarezerwować** | Pole tylko do odczytu, które można edytować jako zablokowane. | 
| **Jednostka zasobów** | Pole tylko do odczytu, które można edytować jako zablokowane. | 
| **Harmonogram jednostek** | Pole tylko do odczytu, które można edytować jako zablokowane. | 
| **Jednostka** | Pole tylko do odczytu, które można edytować jako zablokowane. | 
| **Cena** | Domyślnie jest ustawiona wartość na podstawie kwoty źródłowego punktu kontrolnego. Pole tylko do odczytu, które można edytować jako zablokowane. |
| **Waluta** | Domyślnie jest ustawiona wartość z punktu kontrolnego. Pole tylko do odczytu, które można edytować jako zablokowane. |
| **Kwota** | Domyślnie jest ustawiona wartość na podstawie kwoty źródłowego punktu kontrolnego. Pole tylko do odczytu, które można edytować jako zablokowane. | 
| **Podatek** | Domyślnie jest ustawiona wartość na podstawie kwoty podatku źródłowego punktu kontrolnego. Pole tylko do odczytu, które można edytować jako zablokowane. |
| **Kwota rozszerzona** | Domyślnie jest ustawiona wartość na podstawie kwoty rozszerzonej źródłowego punktu kontrolnego. Pole to można edytować. | 
| **Typ rozliczeń** | Zawsze domyślnie ustawiona na **Odpłatne**. Pole tylko do odczytu, które można edytować jako zablokowane. |
| **Typ transakcji** | Domyślnie jest ustawiona wartość z punktu kontrolnego. Pole tylko do odczytu, które można edytować jako zablokowane. | 
| **Klasa transakcji** | Domyślnie jest ustawiona wartość z punktu kontrolnego. Pole tylko do odczytu, które można edytować jako zablokowane. | 

## <a name="refresh-invoice-transactions"></a>Odśwież transakcje faktury

Jeśli po utworzeniu faktury istnieją wartości rzeczywiste, na fakturze można uwzględnić te wartości rzeczywiste.

1. W **Widok rejestru rozliczeń** zaznacz dane jako **Przygotowane do fakturowania**.   
2. Otwórz roboczą fakturę proforma i na wstążce **Akcje** wybierz opcję **Odśwież transakcje wiersza faktury**.

  Szczegółowe informacje o wierszu faktury są tworzone dla wszystkich danych rzeczywistych z datą z przeszłości i oznaczonych jako **Przygotowane do fakturowania**, ale nie są one uwzględnione na fakturze.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
