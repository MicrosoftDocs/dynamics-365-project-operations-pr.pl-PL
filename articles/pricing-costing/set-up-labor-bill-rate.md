---
title: Konfigurowanie stawek rozliczania wykonanej pracy
description: W tym temacie zamieszczono informacje dotyczące konfigurowania stawek rozliczania wykonanej pracy w Project Operations.
author: rumant
manager: Annbe
ms.date: 10/16/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 501458510efca6434a51577aacd1f09d1a4faa25
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/31/2020
ms.locfileid: "4180719"
---
# <a name="set-up-labor-bill-rates"></a>Konfigurowanie stawek weksli robocizny

**Zastosowane do:** Project Operations dla zasobów/scenariuszy nieopartych na zaopatrzeniu

Każdy cennik ma zestaw stawek pracy, inaczej cen ról, które obowiązują w ramach kontekstu i daty obowiązywania z nagłówka danego cennika. Stawki za koszty fakturowania w Dynamics 365 Project Operations można skonfigurować tylko w jednej walucie, która jest walutą w nagłówku cennika.

1. Aby skonfigurować stawki sprzedaży wykonanej pracy w cenniku, należy utworzyć Cennik na podstawie nagłówka cennika. 
2. Na karcie **Ceny ról**. w podsiatce, wybierz pozycję **+ Nowa cena roli**. 
3. W okienku **Szybkie tworzenie** wprowadź kombinację roli i jednostka organizacyjnej, dla której konieczne jest skonfigurowanie stawki rozliczenia.

   W poniższej tabeli podano pola na karcie **Ogólne** oraz w okienku **Szybkie tworzenie** z wiersza cen z rolami, o których trzeba pamiętać, podczas tworzenia cen ról w cenniku sprzedaży:

    | Pole | Lokalizacja | Opis | Wpływ zmian w dalszych etapach |
    | --- | --- | --- | --- |
    | Rola | Karta **Ogólne** i okienko **Szybkie tworzenie** | Wybierz rolę, dla której chcesz ustawić stawkę rozliczenia. | Rola na oszacowaniu przychodzącym lub wartości rzeczywistej, dopasowana do tego wiersza domyślnej stawki rozliczeń za rolę. |
    | Firma zasobów | Karta **Ogólne** i okienko **Szybkie tworzenie** | Wybierz firmę lub podmiot prawny, do którego należy rola. Na przykład deweloper z firmy Fabrikam India lub deweloper z firmy Fabrikam USA. | Firma zasobów na oszacowaniu przychodzącym lub wartości rzeczywistej, dopasowana do tego wiersza domyślnej stawki rozliczeń za rolę. |
    | Jednostka zasobów | Karta **Ogólne** i okienko **Szybkie tworzenie** | Wybierz jednostkę organizacyjną lub wydział firmy, do której należy rola. Na przykład deweloper z działu robotyki w Fabrikam India lub deweloper z działu oprogramowania w Fabrikam USA. | Jednostka zasobów na oszacowaniu przychodzącym lub wartości rzeczywistej, dopasowana do tego wiersza domyślnej stawki rozliczeń za rolę. |
    | Cena | Karta **Ogólne** i okienko **Szybkie tworzenie** | Skonfiguruj stawkę rozliczenia dla połączenia jednostki zasobów i firmy zasobów. Na przykład deweloper z firmy Fabrikam India korzysta z rozliczenia w wysokości 100 USD a deweloper z Fabrikam USA ze stawki 150 USD. | To jest domyślna stawka rozliczeniowa dla każdego kosztu jednostkowego w szacowaniu przychodzącym lub wartości rzeczywistej dla klasy transakcji Czas. |
    | Waluta | Karta **Ogólne** i okienko **Szybkie tworzenie**| Domyślnie wartość waluty pochodzi z waluty w nagłówku cennika. Nie można zastąpić waluty w cenniku sprzedaży. | Ta waluta to domyślna waluta każdego kosztu jednostkowego w przychodzącej wartości rzeczywistej dla klasy transakcji Czas. |
    | Harmonogram jednostek | Karta **Ogólne** i okienko **Szybkie tworzenie** | Domyślna wartość tego harmonogramu określa czas i nie można jej zmienić, ponieważ jest ona używana do wyrażania stawek na jednostkę czasu. | W tym polu nie ma wpływu zmian na dalsze etapy. |
    | Jednostka | Karta **Ogólne** i okienko **Szybkie tworzenie** | Wartość jednostki pochodzi z pola **Jednostka czasu** z nagłówka cennika sprzedaży. Ta wartość może być zastąpiona. Na przykład deweloper z firmy Fabrikam India ma stawkę rozliczenia 1000 USD na **dzień w Indiach**. Deweloper z firmy Fabrikam USA ma stawkę rozliczenia 1500 USD za **dzień w USA**. | W przypadku domyślnych wartości opcji na cenę jednostkową w szacowaniu przychodzącym lub rzeczywistym wierszu używany jest system jednostek i konwersja w jednostkach podstawowych w celu obliczenia ceny jednostkowej. Na przykład wartość szacunkowa wynosi 10 jednostek **Dni w Indiach** dla dewelopera z Indii, a jednostka Dni w Indiach jest definiowana jako 10 godzin. Podczas kalkulacji cen w wierszu szacowania aplikacja oblicza cenę jednostkową w szacowaniu jako 1000 USD/10 godzin = 100 USD na godzinę. |

## <a name="transfer-pricing-or-set-up-bill-rates-for-resources-from-other-organizational-units-or-divisions"></a>Przeniesienie kalkulacji cen lub konfigurowanie stawek naliczanych dla zasobów z innych jednostek organizacyjnych lub oddziałów 

Przedsiębiorstwa oparte na projektach często korzystają z pracowników pochodzących z różnych firm i różnych działów w firmie w celu pracy nad projektami. Projekty mogą być wykonywane z poziomu określonego podmiotu prawnego i działu, podczas gdy pracownicy lub konsultanci pracujący nad projektami mogą pochodzić z tego samego lub innego podmiotu bądź działu. Projekt może również zawierać kombinacje osób z różnych oddziałów i podmiotów prawnych. W operacjach projektu podmiot prawny, który jest właścicielem usługi dostarczania projektu, jest nazywany **Firmą będącą właścicielem**, natomiast dział, któremu należy dostarczyć usługi to **Jednostka zamawiająca**. Każdy inny podmiot prawny, który zawiera zasoby, jest zwany **Firmami zasobów**, a wydziały, które zawierają zasoby, to **Jednostki zasobów**. Z uwagi na fakt, że koszty pracy na różnych rynkach na całym świecie, stawki za pracę są również różne w różnych miejscach.

Na przykład deweloper z działu robotyki firmy Fabrikam Indie pracujący w ramach projektu w USA jest rozliczany według stawki 100 USD na godzinę. Deweloper z działu robotyki w Fabrikam US pracujący nad projektem w USA otrzymuje 150 USD na godzinę. 

### <a name="example-set-up-a-bill-rate"></a>Przykład: Konfigurowanie stawki rozliczenia 

1. Utwórz cennik o nazwie *Stawki rozliczania Fabrikam US* i ustaw datę obowiązywania.
2. W formularzu cennik sprzedaży wprowadź następujące informacje dotyczące stawki:

    | Rola | Firma zasobów | Jednostka zasobów | Stawka rozliczania |
    | --- | --- | --- | --- |
    | Developer | Fabrikam India | Fabrikam India - Robotics | 100 USD |
    | Developer | Fabrikam Philippines | Fabrikam Philippines - Robotics | 90 USD |
    | Developer | Fabrikam US | Fabrikam US - Robotics | 150 USD |

3. Dołącz cennik sprzedaży **Stawki rozliczania Fabrikam US** do cennika projektu lub kontraktu projektu bądź danego konta.
