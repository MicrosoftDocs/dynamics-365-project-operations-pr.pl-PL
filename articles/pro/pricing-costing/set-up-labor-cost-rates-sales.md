---
title: Konfigurowanie stawek kosztów robocizny — wersja uproszczona
description: W tym temacie zamieszczono informacje dotyczące sposobu konfigurowania stawek wykonanej pracy w Project Operations.
author: rumant
manager: Annbe
ms.date: 10/12/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: e6b1265e5e4d29ccc3f620da364fc9554285a176
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5274381"
---
# <a name="set-up-labor-cost-rates---lite"></a>Konfigurowanie stawek kosztów robocizny — wersja uproszczona

_**Zastosowane w:** Wdrażanie uproszczone — od okazji do faktury pro forma_

Każdy cennik ma zestaw stawek pracy (ceny ról), który jest wyrównany do treści i daty obowiązywania danego cennika.

1. Utwórz Cennik i na karcie **Cena ról** w podsiatce wybierz opcję **Nowa rola**.
2. Na stronie **Szybkie tworzenie** wybierz rolę i jednostkę organizacyjną.
3. Wprowadź inne informacje w wymaganych polach.

Poniższa tabela zawiera pola, które są istotne podczas tworzenia stawek pracy w cenniku kosztów.

| Pole | Lokalizacja | Opis | Wpływ zmian w dalszych etapach |
| --- | --- | --- | --- |
| Rola | Karta **Ogólne** i strony **Szybkie tworzenie** | Wybierz rolę, której dotyczy stawka kosztu. | Rola na oszacowaniu przychodzącym lub wartości rzeczywistej, dopasowana do tego wiersza domyślnej stawki kosztu za rolę. |
| Jednostka zasobów | Karta **Ogólne** i strony **Szybkie tworzenie** | Wybierz jednostkę organizacyjną lub wydział firmy, gdzie ta rola będzie wykorzystana. Na przykład deweloper z działu robotyki w Fabrikam India lub deweloper z działu oprogramowania w Fabrikam USA. | Jednostka zasobów na oszacowaniu przychodzącym lub wartości rzeczywistej, dopasowana do tego wiersza domyślnej stawki kosztu za rolę. |
| Cena | Karta **Ogólne** i strony **Szybkie tworzenie** | Skonfiguruj stawkę kosztu dla połączenia jednostki zasobów i firmy zasobów. Na przykład deweloper z firmy Fabrikam India kosztuje 1000 INR lub deweloper z firmy Fabrikam USA kosztuje 150 USD. | Cena jest stawką kosztową domyślną dla każdego kosztu jednostkowego w szacowaniu przychodzącym lub wartości rzeczywistej dla klasy transakcji **Czas**. |
| Waluta | Karta **Ogólne** i strony **Szybkie tworzenie** | Domyślnie wartość waluty pochodzi z waluty w nagłówku cennika kosztów, ale ta wartość może być nadpisana. Na przykład deweloper z firmy Fabrikam India kosztuje 1000 INR. Deweloper z firmy Fabrikam USA kosztuje 150 USD. | Domyślna wartość waluty każdego kosztu jednostkowego w przychodzącej wartości rzeczywistej dla klasy transakcji **Czas**. W przypadku oszacowania projektu wartość waluty jest konwertowana na walutę projektu i wyświetlana w widoku okresowym oszacowania. |
| Harmonogram jednostek | Karta **Ogólne** i strony **Szybkie tworzenie** | Domyślna wartość tego harmonogramu określa czas i nie można jej zmienić, ponieważ jest ona używana do wyrażania stawek na jednostkę czasu. | Nie ma to wpływu na podrzędne procesy. |
| Jednostka | Karta **Ogólne** i strony **Szybkie tworzenie** | Domyślnie wartość jednostki pochodzi z pola **Jednostka czasu** z nagłówka cennika kosztów. Ta wartość może być zastąpiona. Na przykład deweloper z firmy Fabrikam India kosztuje 1000 INR na **dzień w Indiach**. Deweloper z firmy Fabrikam USA kosztuje 150 USD za **Dzień w USA**. | System używa żywany jest jednostek i dokonywana jest konwersja w jednostkach podstawowych w celu obliczenia domyślnej ceny jednostkowej dla przychodzącego oszacowania lub wiersza rzeczywistego. Na przykład wartość szacunkowa wynosi 10 jednostek **Dni w Indiach** dla dewelopera z Indii, a jednostka **Dni w Indiach** jest definiowana jako 10 godzin. Przy ustalaniu kosztów w wierszu szacowania aplikacja oblicza koszt jednostkowy w szacowaniu jako: 1000 INR/10 godzin = 100 INR na godzinę, która to wartość jest konwertowana na USD i wyświetlana jako koszt jednostkowy na stronie **Oszacowania projektu**. |

## <a name="transfer-pricing-and-costs-for-resources-outside-of-your-division-or-legal-entity"></a>Przenieś ceny i koszty zasobów poza dział lub podmiot prawny

Przedsiębiorstwa oparte na projektach często używają pracowników z różnych działów firmy lub różnych podmiotów prawnych w pracy nad projektami. Projekty mogą być wykonywane w ramach określonego podmiotu prawnego, podczas gdy pracownicy lub konsultanci pracujący nad projektem mogą pochodzić z tego samego lub innego podmiotu bądź działu. Może też istnieć połączenie tych możliwości. W rozwiązaniu Dynamics 365 Project Operations podmiot prawny, który jest właścicielem dostawy projektu, jest **Firmą będącą właścicielem**, a dział, który jest właścicielem dostawy, jest **Jednostką kontraktującą**. Każdy inny podmiot prawny, który zawiera zasoby, jest zwany **Firmami zasobów**, a wydziały, które zawierają zasoby, to **Jednostki zasobów**. W większości krajów firma jest zobowiązana zapewnić, że osoba lub oddział prawny, który chce skorzystać z tej osoby, obciążą firmę będącą właścicielem oraz jednostkę zamawiającą do korzystania z zasobów.

Na przykład firma Fabrikam Corporation musi zagwarantować, że firma Fabrikam India-Robotics wynegocjowała stawkę kosztów z Fabrikam US-Robotics lub Fabrikam UK-Robotics.

Deweloper z Fabrikam India pobiera 100 USD, gdy jest wypożyczony do Fabrikam US-Robotics, ale 150 USD gdy jest wypożyczony do Fabrikam U-Robotics.

### <a name="set-up-costs-for-outside-resources"></a>Konfigurowanie kosztów zasobów zewnętrznych

1. Utwórz cennik o nazwie, *stawki kosztów US Fabrikam-Robotics*, a następnie ustaw obowiązujące daty.
2. Korzystając z informacji zawartych w tabeli można ustawić stawki na liście kosztów. 

| Rola | Firma zasobów | Jednostka zasobów | Stawka kosztów |
| --- | --- | --- | --- |
| Developer | Fabrikam India | Fabrikam India-Robotics | 100 USD |
| Developer | Fabrikam Philippines | Fabrikam Philippines-Robotics | 90 USD |
| Developer | Fabrikam US | Fabrikam US-Robotics | 150 USD |

3. Dołącz tą listę kosztów do jednostki organizacyjnej Fabrikam US-Robotics.

### <a name="set-up-transfer-pricing-for-a-resource-in-the-appropriate-currency"></a>Konfigurowanie kalkulacji cen z przeniesienia dla zasobu w odpowiedniej walucie 

W przypadku Project Operations cena zasobu może zostać ustawiona w dowolnej walucie. Domyślnie waluta zawiera wartość, która znajduje się w nagłówku cennika, ale można ją zmienić.

Korzystając z przykładu dotyczącego konfiguracji ceny przeniesienia, można zmienić informacje na następujące:

Firma Fabrikam Corporation musi zagwarantować, że firma Fabrikam India-Robotics wynegocjowała stawkę kosztów z Fabrikam US-Robotics lub Fabrikam UK-Robotics.

Deweloper z Fabrikam India kosztuje 5000 INR, gdy jest wypożyczony do Fabrikam US-Robotics, ale 5500 INR gdy jest wypożyczony do Fabrikam UK-Robotics.

W liście cenników dla Fabrikam US-Robotics, stawki kosztów mogą być wyrażone w następujących postaciach:

| Rola | Firma zasobów | Koszt |
| --- | --- | --- |
| Developer | Fabrikam India | 5000 INR |
| Developer | Fabrikam US | 115 USD |

W liście cenników dla Fabrikam UK-Robotics, stawki kosztów mogą być wyrażone w następujących postaciach poniżej:

| Rola | Firma zasobów | Koszt |
| --- | --- | --- |
| Developer | Fabrikam India | 5500 INR |
| Developer | Fabrikam UK | 115 GBP |

Lista kosztów własnych może udostępniać stawki pracy w wielu walutach. Podczas generowania oszacowania kosztów projektu są one konwertowane na walutę projektu i wyświetlane dla użytkownika. Po zatwierdzeniu wpisu czasu i utworzeniu kosztu wartości rzeczywistej koszt rzeczywisty jest wyceniany w walucie odpowiadającej tej pozycji z wiersza z ceną z listy cenników. Koszt rzeczywisty czasu w pojedynczym projekcie może być rejestrowany w wielu walutach. Jednak podczas zestawiania lub podsumowywania rzeczywistych kosztów wykonanej pracy na poziomie projektu Project Operations wykonają konwersję wszystkich kosztów pracy na walutę projektu, która może być wyświetlana przez użytkownika.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]