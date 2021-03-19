---
title: Zarządzanie fakturą proforma - wersja uproszczona
description: Ten temat zawiera informacje dotyczące pracy z fakturami Proforma.
author: rumant
manager: Annbe
ms.date: 10/27/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: ca6c2cc8855cfed592057ca129b436450104af99
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5274062"
---
# <a name="manage-a-proforma-invoice---lite"></a>Zarządzanie fakturą proforma - wersja uproszczona

_**Zastosowane w:** Wdrażanie uproszczone — od okazji do faktury pro forma_

W rozwiązaniu Dynamics 365 Project Operations faktury proforma są budowane jako rozszerzenie faktur w Dynamics 365 Sales. However, there are many differences in the invoicing process between Sales i Project Operations when it comes to invoicing. Nie można na przykład utworzyć nowej faktury na stronie **Listy faktur** w Project Operations, ale może to zrobić w przypadku sprzedaży. Te różnice i rozszerzenia służą do obsługi procesów fakturowania projektów, które różnią się od typowej faktury za zamówienie sprzedaży.

> [!IMPORTANT]
> Ze względu na różnice między Sales i Project Operations nie można zamiennie używać faktur.

## <a name="invoice-header"></a>Nagłówek faktury

Poniższe informacje są dostępne w nagłówku faktury proforma w Project Operations.

| Pole | Lokalizacja | Opis | Wpływ zmian w dalszych etapach |
| --- | --- | --- | --- |
| **Identyfikator faktury** | Karta **Podsumowanie** | Identyfikator generowany automatycznie podczas tworzenia faktury proforma. Pole tylko do odczytu, które można edytować jako zablokowane. | To pole służy jako odniesienie dla każdej faktury proforma. |
| **Nazwa/nazwisko** | Karta **Podsumowanie** | Ustaw domyślnie nazwę umowy dotyczącej projektu. To pole może być edytowane przez użytkownika. | &nbsp;  |
| **Waluta** | Karta **Podsumowanie** | Ustaw domyślnie walutę dotyczącą projektu. Pole tylko do odczytu, które można edytować jako zablokowane. |&nbsp; |
| **Cennik** | Karta **Podsumowanie** | Ustaw domyślnie cennik dotyczący projektu. Pole tylko do odczytu, które można edytować jako zablokowane. | &nbsp; |
| **Szansa sprzedaży** | Karta **Podsumowanie** | Odwołanie do połączonej szansy sprzedaży. Pole tylko do odczytu, które można edytować jako zablokowane. | &nbsp;  |
| **Kontrakt** | Karta **Podsumowanie** | Odniesienie do połączonej umowy dotyczącej projektu. Pole tylko do odczytu, które można edytować jako zablokowane. | &nbsp; |
| **Klient** | Karta **Podsumowanie** | Odniesienie do połączonej umowy dotyczącej projektu. Pole tylko do odczytu, które można edytować jako zablokowane. |&nbsp;  |
| **Opis** | Karta **Podsumowanie** | Pole tekstowe, które opisuje fakturę. To pole może być edytowane przez użytkownika. | &nbsp; |
| **Adres płatnika** i pokrewne pola | **Karta Podsumowanie** | Wartości domyślne są ustawiane przez klienta umowy projektu. To pole może być edytowane przez użytkownika.  | &nbsp; |
| **Stan** | Karta **Podsumowanie** | Powoduje ustawienie następujących opcji: **Aktywny**, **Zamknięty**, **Zapłacony** i **Anulowany**, który może być edytowany przez użytkownika. | Nieobsługiwane stany Project Operations zawierają **Zamknięte** i **Anulowane**. </br> Stan jest ustawiany na **Aktywny** w czasie tworzenia faktury. </br>Stan powinien zostać ustawiony na **Zapłacony** tylko po potwierdzeniu faktury. |
| **Stan faktury projektu** | Karta **Podsumowanie** | Powoduje ustawienie następujących opcji: **Wersja robocza**, **W trakcie przeglądu** i **Potwierdzono**, który może być edytowany przez użytkownika. | W obydwu stanach **Wersja robocza** i **W trakcie przeglądu** faktura może być edytowana. Faktura nie może być edytowana po jej potwierdzeniu. |
| **Kwota szczegółowa** | Karta **Podsumowanie** | Suma kwot we wszystkich wierszach faktury po zaliczkach i potrąceniach. Pole tylko do odczytu, które można edytować jako zablokowane. | To pole jest używane do obliczania kwoty końcowej. |
| **Rabat (%)** | Karta **Podsumowanie** | To pole można edytować, aby wprowadzić stawkę procentową rabatu. To pole nie jest obsługiwane przez funkcje Project Operations. | To jest nieobsługiwane pole. |
| **Kwota rabatu** | Karta **Podsumowanie** | To pole można edytować, aby wprowadzić kwotę rabatu. To pole nie jest obsługiwane przez funkcje Project Operations. | To jest nieobsługiwane pole. |
| **Kwota bez frachtu** | **Karta Podsumowanie** | Łączna kwota faktury po zastosowaniu rabatów. Pole tylko do odczytu, które można edytować jako zablokowane. | To pole jest używane do obliczania kwoty końcowej. |
| **Kwota frachtu** | Karta **Podsumowanie** | To pole można edytować, aby wprowadzić kwotę frachtu. To pole nie jest obsługiwane przez funkcje Project Operations. | To jest nieobsługiwane pole. |
| **Łączny podatek** | Karta **Podsumowanie** | Całkowity podatek ze wszystkich pozycji faktury na fakturze. Pole tylko do odczytu, które można edytować jako zablokowane. | Brak. |
| **Łączna kwota** | Karta **Podsumowanie** | Suma kwot po rabatach i podatkach. | Suma oznacza kwotę, jaką musi zapłacić klient. |
## <a name="project-based-invoice-lines"></a>Wiersze faktur na podstawie projektu

W Project Operations zawsze istnieje jeden wiersz faktury dla każdego wiersza umowy dotyczącej projektu. Wiersz faktury zostanie utworzony nawet w przypadku braku wartości rzeczywistych. Poniższe informacje są dostępne w wierszu faktury proforma.

| Pole | Lokalizacja | Opis | Wpływ zmian w dalszych etapach |
| --- | --- | --- | --- |
| **Identyfikator faktury** | Karta **Ogólne** | Odwołanie do identyfikatora faktury. Pole tylko do odczytu, które można edytować jako zablokowane. | Link do identyfikatora faktury umożliwia powrót do nagłówka faktury. |
| **Nazwa/nazwisko** | Karta **Ogólne** | Nazwa wiersza faktury ustawiona domyślnie na podstawie nazwy pozycji kontraktu. To pole może być edytowane przez użytkownika. | &nbsp; |
| **Project** | Karta **Ogólne** | Projekt w pokrewnej pozycji kontraktu projektu. Pole tylko do odczytu, które można edytować jako zablokowane. | Za pomocą łącza do projektu można przechodzić do projektu. |
| **Metoda rozliczania** | Karta **Ogólne** | Metoda rozliczania w pokrewnej pozycji kontraktu projektu. Pole tylko do odczytu, które można edytować jako zablokowane. | &nbsp; |
| **Kwota pozycji kontraktu** | Karta **Ogólne** | Kwota umowy w powiązanej pozycji kontraktu projektu. Pole tylko do odczytu, które można edytować jako zablokowane. | &nbsp; |
| **Zafakturowano do daty** | Karta **Ogólne** | Suma kwot wszystkich informacji dotyczących wiersza faktury. Pole tylko do odczytu, które można edytować jako zablokowane. | &nbsp; |
| **Kwota** | Karta **Ogólne** | Suma kwot wszystkich danych wiersza faktury podlegającej opłacie na tej fakturze. Pole tylko do odczytu, które można edytować jako zablokowane. | To pole jest używane do obliczania kwoty końcowej w nagłówku faktury. |
| **Podatek** | Karta **Ogólne** | Suma kwot podatku dotyczących wiersza faktury dla tego wiersza faktury. Pole tylko do odczytu, które można edytować jako zablokowane. | To pole jest używane do obliczania końcowej kwoty podatku w nagłówku faktury. |
| **Kwota rozszerzona** | Karta **Ogólne** | Suma całkowitych kwot (**Podatek + Kwoty**) wszystkich szczegółów linii faktury podlegających opłacie w tym wierszu faktury. Pole tylko do odczytu, które można edytować jako zablokowane. | To pole jest używane do obliczania kwoty końcowej w nagłówku faktury. |


## <a name="invoice-line-details"></a>Szczegóły wiersza faktury

Każdy wiersz faktury na fakturze projektu zawiera szczegóły wiersza faktury. Te szczegóły wierszy są powiązane z wartościami rzeczywistymi i punktami kontrolnymi niefakturowanymi, które są powiązane z pozycją kontraktu, do której odwołuje się wiersz faktury. Wszystkie te transakcje są oznaczone jako **Przygotowane do fakturowania**.

W przypadku wiersza **Faktura czasowa i materiałowa** szczegóły wiersza faktury są zgrupowane jako **Odpłatne**, **Niepodlegające opłatom** i **Uzupełniające** na stronie **Wiersz faktury**. Szczegóły **Wypłacanego wiersza na fakturze** są dodawane do sumy wiersza faktury. **Uzupełniające** i **Wartości rzeczywiste niepodlegające obciążeniu** nie są dodawane do sumy wiersza faktury.

W przypadku wiersza **Faktury o stałej cenie** szczegóły wiersza faktury są tworzone na podstawie punktów kontrolnych oznaczonych jako **Przygotowane do fakturowania** w pokrewnej pozycji kontraktu. Po utworzeniu szczegółów wiersza faktury z punktu kontrolnego stan fakturowania w punktach kontrolnych zostanie zaktualizowany na podstawie **Utworzono fakturę dla klienta**.

### <a name="edit-invoice-line-details"></a>Edytuj szczegóły linii faktury

Następujące pola są dostępne w szczegółach wiersza faktury, które są poparte niezafakturowaną faktyczną sprzedażą:

| Pole | Opis | Wpływ zmian w dalszych etapach |
| --- | --- | --- |
| **Identyfikator wiersza** | Odwołanie do **Identyfikatora wiersza faktury**. Pole tylko do odczytu, zablokowane do edycji. | Ten link umożliwia powrót do nagłówka faktury. |
| **Opis** | Opis szczegółów wiersza faktury. Domyślne ustawienie jest ustawiane na podstawie pola **Komentarze wewnętrzne** w **Wpis czasu** oraz pola **Opis** w **Wpis wydatków**. To pole może być edytowane przez użytkownika.| &nbsp; |
| **Opis zewnętrzny** | Opis szczegółów wiersza faktury. Domyślne ustawienie jest ustawiane na podstawie pola **Komentarze zewnętrzne** w **Wpis czasu** oraz pola **Opis** w **Wpis wydatków**. To pole może być edytowane przez użytkownika. | Na podstawie tego opisu można określić, co powinno znajdować się na wydrukowanej fakturze, która zostanie wysłana do klienta. W Project Operations faktura proforma nie ma wszystkich funkcji wymaganych do skonfigurowania ustawień drukowania faktury. |
| **Data rozpoczęcia** | Domyślnie jest ustawiona wartość z wartości źródłowej. Pole tylko do odczytu, które można edytować jako zablokowane. | To pole można edytować w nowym szczególe wiersza faktury, który nie jest poparty faktycznym źródłem. |
| **Project** | Domyślnie jest ustawiona wartość z wartości źródłowej. Pole tylko do odczytu, które można edytować jako zablokowane. | Ustaw domyślnie na projekt w powiązanej pozycji kontraktu. |
| **Zadanie** | Domyślnie jest ustawiona wartość z wartości źródłowej. Pole tylko do odczytu, które można edytować jako zablokowane. | To pole można edytować w nowym szczególe wiersza faktury, który nie jest poparty faktycznym źródłem. Lista rozwijana zawiera wszystkie zadania skojarzone z pokrewną pozycją kontraktu projektu.  |
| **Kategoria transakcji** | Domyślnie jest ustawiona wartość z wartości źródłowej. Pole tylko do odczytu, które można edytować jako zablokowane. | To pole można edytować w nowym szczególe wiersza faktury, który nie jest poparty wartością źródłową. |
| **Rola** | Domyślnie jest ustawiona wartość z wartości źródłowej. Pole tylko do odczytu, które można edytować jako zablokowane. | To pole można edytować w nowym szczególe wiersza faktury, który nie jest poparty wartością źródłową. |
| **Zasób, który można zarezerwować** | Domyślnie jest ustawiona wartość z wartości źródłowej. Pole tylko do odczytu, które można edytować jako zablokowane. | To pole można edytować w nowym szczególe wiersza faktury, który nie jest poparty wartością źródłową. |
| **Jednostka zasobów** | Domyślnie jest ustawiona wartość z wartości źródłowej. Pole tylko do odczytu, które można edytować jako zablokowane. | To pole można edytować w nowym szczególe wiersza faktury, który nie jest poparty wartością źródłową. |
| **Ilość** | Domyślnie jest ustawiona wartość z wartości źródłowej. Pole tylko do odczytu, które można edytować jako zablokowane. | To pole można edytować w nowym szczególe wiersza faktury, który nie jest poparty wartością źródłową. |
| **Harmonogram jednostek** | W przypadku szczegółów wiersza faktury dla czasu jest zawsze ustawiony czas i nie można jej edytować. W przypadku wydatków jest ono domyślnie ustawiane na podstawie wartości w polu kosztów źródłowych. Pole tylko do odczytu, które można edytować jako zablokowane. | Domyślnie Ustaw **Czas** w nowych wierszach faktury, które nie są poparty wartością źródłową. |
| **Jednostka** | Domyślnie jest ustawiona wartość z wartości źródłowej. Pole tylko do odczytu, które można edytować jako zablokowane. | To pole można edytować w nowym szczególe wiersza faktury, który nie jest poparty wartością źródłową |
| **Cena** | Domyślnie jest ustawiona wartość z wartości źródłowej. Pole tylko do odczytu, które można edytować jako zablokowane. | To pole można edytować w nowym szczególe wiersza faktury, który nie jest poparty wartością źródłową. Jeśli nie wprowadzono żadnej wartości, będzie ona domyślnie ustawiana po **Zapisaniu**. |
| **Waluta** | Domyślnie jest ustawiona wartość z wartości źródłowej. Pole tylko do odczytu, które można edytować jako zablokowane. | Domyślne ustawienie z nagłówka faktury podczas tworzenia nowej faktury bez rzeczywistej kopii zapasowej.  Pole tylko do odczytu, które można edytować jako zablokowane. |
| **Kwota** | Domyślnie jest ustawiona wartość z wartości źródłowej. Pole tylko do odczytu, które można edytować jako zablokowane. | Obliczane jako **Cena ilościowa \* Cena** podczas tworzenia nowej faktury bez potrzeby wykonywania kopii zapasowych. Jest on obliczany po **Zapisaniu**. Pole tylko do odczytu, które można edytować jako zablokowane. |
| **Podatek** | Domyślnie jest ustawiona wartość z wartości źródłowej. To pole może być edytowane przez użytkownika | Pole może być edytowane przez użytkownika podczas tworzenia nowych szczegółów wiersza faktury bez potrzeby wykonywania kopii zapasowej. |
| **Kwota rozszerzona** | Pole obliczane, które jest obliczane jako **Kwota + podatek**. Pole tylko do odczytu, które można edytować jako zablokowane. | &nbsp; |
| **Typ rozliczeń** | Domyślnie jest ustawiona wartość z wartości źródłowej. To pole może być edytowane przez użytkownika. | Wybranie opcji **Płatny** powoduje dodanie wiersza do sumy wiersza faktury. **Uzupełniające** i **Nieodpłatne** wykluczą go z sumy wiersza faktury. |
| **Typ transakcji** | Domyślnie jest ustawiona wartość z wartości źródłowej. Pole tylko do odczytu, które można edytować jako zablokowane. | Ustaw domyślnie na **Sprzedaż zafakturowaną** i zablokowane podczas tworzenia nowego **Szczegółu wiersza faktury** bez faktycznej kopii zapasowej.  |
| **Klasa transakcji** | Domyślnie jest ustawiona wartość z wartości źródłowej. Pole tylko do odczytu, które można edytować jako zablokowane. | Ustawiany domyślnie w oparciu o to, czy użytkownik zdecyduje się utworzyć szczegóły wiersza faktury **Czasu**, **Wydatków** lub **Opłat**, jednocześnie tworząc nowy **Szczegół wiersza faktury** bez faktycznego zaplecza. Zablokowano możliwość edycji. |

Następujące pola są dostępne w szczegółach wiersza faktury, które są poparte punktem kontrolnym:.

| Pole | Opis | Wpływ zmian w dalszych etapach |
| --- | --- | --- |
| **Identyfikator wiersza** | Odwołanie do **Identyfikatora wiersza faktury**. Pole tylko do odczytu, które można edytować jako zablokowane. | Ten link umożliwia powrót do nagłówka faktury. |
| **Opis** | Opis szczegółów wiersza faktury. Domyślnie jest ustawiona wartość na podstawie opisu źródłowego punktu kontrolnego. | &nbsp; |
|**Opis zewnętrzny** | Opis szczegółów wiersza faktury ustawiany domyślnie na podstawie opisu źródłowego punktu kontrolnego. | Na podstawie tego pola można określić, co powinno znajdować się na wydrukowanej fakturze, która zostanie wysłana do klienta. Faktura proforma w Project Operations nie ma wszystkich funkcji wymaganych do skonfigurowania ustawień drukowania faktury. |
| **Data rozpoczęcia** | Domyślnie jest ustawiana wartość z daty **Punktów kontrolnych** we źródłowym punktach kontrolnych. Pole tylko do odczytu, które można edytować jako zablokowane. | &nbsp; |
| **Project** | Domyślnie jest ustawiona wartość z punktu kontrolnego. Pole tylko do odczytu, które można edytować jako zablokowane. | &nbsp; |
| **Zadanie** | Domyślnie jest ustawiona wartość z punktu kontrolnego. Pole tylko do odczytu, które można edytować jako zablokowane. | &nbsp; |
| **Kategoria transakcji** | Pole tylko do odczytu, które można edytować jako zablokowane. | &nbsp; |
| **Rola** | Pole tylko do odczytu, które można edytować jako zablokowane. | &nbsp; |
| **Zasób, który można zarezerwować** | Pole tylko do odczytu, które można edytować jako zablokowane. | &nbsp; |
| **Jednostka zasobów** | Pole tylko do odczytu, które można edytować jako zablokowane. | &nbsp; |
| **Harmonogram jednostek** | Pole tylko do odczytu, które można edytować jako zablokowane. | &nbsp; |
| **Jednostka** | Pole tylko do odczytu, które można edytować jako zablokowane. | &nbsp; |
| **Cena** | Domyślnie jest ustawiona wartość na podstawie kwoty źródłowego punktu kontrolnego. Pole tylko do odczytu, które można edytować jako zablokowane. | &nbsp; |
| **Waluta** | Domyślnie jest ustawiona wartość z punktu kontrolnego. Pole tylko do odczytu, które można edytować jako zablokowane. |&nbsp; |
| **Kwota** | Domyślnie jest ustawiona wartość na podstawie kwoty źródłowego punktu kontrolnego. Pole tylko do odczytu, które można edytować jako zablokowane. | &nbsp; |
| **Podatek** | Domyślnie jest ustawiona wartość na podstawie kwoty podatku źródłowego punktu kontrolnego. Pole tylko do odczytu, które można edytować jako zablokowane. | &nbsp; |
| **Kwota rozszerzona** | Domyślnie jest ustawiona wartość na podstawie kwoty rozszerzonej źródłowego punktu kontrolnego. To pole może być edytowane przez użytkownika | &nbsp; |
| **Typ rozliczeń** | Zawsze domyślnie ustawiona na **Odpłatne**. Pole tylko do odczytu, które można edytować jako zablokowane. | &nbsp; |
| **Typ transakcji** | Domyślnie jest ustawiona wartość z punktu kontrolnego. Pole tylko do odczytu, które można edytować jako zablokowane. | &nbsp; |
| **Klasa transakcji** | Domyślnie jest ustawiona wartość z punktu kontrolnego. Pole tylko do odczytu, które można edytować jako zablokowane. | &nbsp; |

### <a name="create-new-invoice-line-details"></a>Utwórz nowe szczegóły wierszy faktur

W wierszach faktur dotyczących czasu i materiałów można tworzyć nowe szczegóły wiersza faktury. Informacje o wierszach tej faktury nie są wartościami rzeczywistymi. W wierszu faktury wiersza faktury godzinowej i materiałowej można wybrać opcję **Nowy**, aby utworzyć nowe informacje o wierszach faktury dla klas transakcji zawartych w pozycji kontraktu.

## <a name="refresh-invoice-transactions"></a>Odśwież transakcje faktury

Jeśli po utworzeniu faktury istnieją wartości rzeczywiste, na fakturze można uwzględnić te wartości rzeczywiste.

1. W **Widok rejestru rozliczeń** zaznacz dane jako **Przygotowane do fakturowania**.   
2. Otwórz roboczą fakturę proforma i na wstążce **Akcje** kliknij polecenie **Odśwież transakcje w wierszu faktury**.

  Spowoduje to utworzenie szczegółów wiersza faktury dla dowolnych wartości rzeczywistych i oznaczonych jako **Przygotowane do fakturowania**, ale nie są one uwzględnione na fakturze.

## <a name="product-based-invoice-lines"></a>Wiersze faktur na podstawie produktu

W Project Operations można tworzyć wiersze faktur dla produktów, których nie stosuje się do żadnego projektu lub dla wszystkich projektów z wierszami faktur opartych na projektach. Te wiersze są tworzone jako wiersze kontraktu opartego na produktach i po ich oznaczeniu jako gotowy do zafakturowania są dodawane jako wiersze faktury opartej na produktach.

Po dodaniu wierszy faktury produktów nie można ich zmienić. Można je jednak usunąć z wersji roboczej faktury.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]