---
title: Scenariusze obsługi wielu walut (wersja 3.x)
description: Ten temat zawiera informacje na temat scenariuszy wielowalutowych.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 12/26/2018
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
ms.openlocfilehash: 89a91cf3dbbcf81dbb089ee88c8c177c73afb694914ca7d95eae96776d38abed
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/06/2021
ms.locfileid: "7005134"
---
# <a name="multiple-currency-scenarios"></a>Scenariusze obsługi wielu walut

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

W usłudze Microsoft Dynamics 365 istnieją dwie koncepcje walut:

- **Waluta transakcji** — waluta, w której jest wykonywana transakcja. 
- **Waluta podstawowa** — waluta wystąpienia usługi Dynamics 365. Ta waluta jest konfigurowana podczas inicjowania obsługi administracyjnej wystąpienia usługi Dynamics 365. Nie można jej później zmienić.

Załóżmy na przykład, że firma Contoso sprzedała 100 koszulek odbiorcy w Wielkiej Brytanii w cenie 15 funtów szterlingów (GBP) za sztukę. W poniższej tabeli zaprezentowano sposób zarejestrowania tej transakcji w encji Produkt zamówiony.

| Produkt | Ilość | Cena jednostkowa | Waluta | Kwota | Kurs wymiany | Cena jednostkowa (podstawowa)| Kwota (podstawowa)|
|---------|----------|----------------|----------|--------|---------------|----------------------|--------------|
| Koszulka | 100      | 15             | GBP      | 1500   | 0.94          | 17,25 USD               | 1,725 USD       |

W kolumnie **Waluta** jest wyświetlana waluta transakcji, czyli waluta, w której miała miejsce sprzedaż. Kolumna **Kurs wymiany** zawiera kurs wymiany między walutą transakcji a walutą podstawową. Walutą podstawową jest dolar amerykański (USD). Ta waluta podstawowa została konfigurowana podczas inicjowania obsługi administracyjnej wystąpienia usługi Dynamics 365.
Jak widać w tabeli, każda transakcja jest rejestrowana zarówno w walucie transakcji, jak i w walucie podstawowej. Usługa Dynamics 365 wykorzystuje walutę podstawową do obliczania kwot w walucie podstawowej.

## <a name="project-service-automation-extensions"></a>Rozszerzenia rozwiązania Project Service Automation

Usługa Dynamics 365 Project Service Automation ma wpływ na walutę transakcji, ponieważ transakcje biznesowe mają zwykle dwa aspekty: koszt i sprzedaż.

Poniższe encje są traktowane jako transakcje biznesowe:

- Szczegóły wiersza oferty
- Szczegóły pozycji kontraktu projektu
- Wiersz szacowania
- Wiersz arkusza
- Szczegóły wiersza faktury
- Wartość rzeczywista

W każdej z tych encji istnieje rekord reprezentujący kwotę kosztu lub kwotę sprzedaży. Podobnie jak w każdej innej encji usługi Dynamics 365 zawierającej pole **Kwota** każdy rekord zawiera kwotę zarówno w walucie transakcji, jak i w walucie podstawowej. 

Rozwiązanie PSA poszerza koncepcję waluty transakcji w koszcie i sprzedaży w następujący sposób:

- Waluta transakcji kosztowej w transakcjach rozliczanych według czasu jest zawsze pobierana z waluty jednostki organizacyjnej, która jest właścicielem projektu lub nim zarządza. Ta jednostka organizacyjna jest nazywana jednostką kontraktującą.
- Waluta transakcji sprzedaży w transakcjach rozliczanych według czasu i wydatków jest zawsze pobierana z waluty kontraktu na projekt.
- Waluta transakcji kosztowej dla wydatków pochodzi z waluty, w której utworzono wpis wydatku.

## <a name="multiple-currency-scenario"></a>Scenariusz obsługi wielu walut

W tej sekcji opisano przykład projektu, który firma Contoso UK realizuje dla klienta o nazwie Fabrikam – Japonia. Oto opis konfiguracji scenariusza:

1. W oknie **Ustawienia** \> **Zarządzanie podmiotem gospodarczym** \> **Waluty** konfiguruje się waluty GBP i japońskiego jena (JPY). 
2. Jest konfigurowane konto klienta o nazwie **Fabrikam – Japonia**, a JPY wybiera się jako walutę dla konta.
3. Jest konfigurowana jednostka organizacyjna o nazwie **Contoso UK**, a GBP wybiera się jako walutę.
4. Jest tworzony kontrakt na projekt, w którym firma **Contoso UK** jest określana jako kontraktująca, a firma **Fabrikam – Japonia** jest określana jako odbiorca.
5. Są tworzone pozycje kontraktu na projekt na podstawie uzgodnień dotyczących fakturowania dla poszczególnych klas transakcji w projekcie, takich jak rozliczanie według czasu czy rozliczania według kosztów.
6. Jest tworzony projekt, w którym firma **Contoso UK** jest określana jako jednostka kontraktująca. Ten projekt jest tworzony i mapowany na pozycje kontraktu projektu.


Podczas szacowania wykorzystującego szczegóły wierszy oferty, szczegóły pozycji kontraktu projektu lub wiersz szacowania z harmonogramu w encji zawsze są tworzone dwa rekordy. Jeden rekord jest przeznaczony dla kosztu, a drugi dla sprzedaży.

- Domyślnie walutą transakcji w rekordzie kosztu jest waluta jednostki kontraktującej w projekcie. W tym przykładzie walutą jest GBP.
- Domyślnie walutą transakcji w rekordzie sprzedaży jest waluta kontraktu na projekt. W tym przykładzie walutą jest JPY.

Podczas tworzenia wartości rzeczywistych dla rozliczania według czasu przy użyciu wpisu czasu lub wiersza arkusza występuje następujące zachowanie:

- Domyślnie walutą transakcji w rekordzie kosztu jest waluta jednostki kontraktującej w projekcie.
- Domyślnie walutą transakcji w rekordzie sprzedaży jest waluta kontraktu na projekt.

Podczas tworzenia wartości rzeczywistych dla wydatków przy użyciu wpisu wydatku lub wiersza arkusza występuje następujące zachowanie:

- Kwotę wydatku można zarejestrować w dowolnej walucie. Wybierz walutę, korzystając z selektora walut na stronie **Wpis wydatków** lub **Wiersz arkusza**. Domyślnie walutą transakcji w rekordzie kosztu jest waluta wpisu wydatku. 
- Domyślnie walutą transakcji w rekordzie sprzedaży jest waluta kontraktu na projekt. Aby ustawić tę walutę, system najpierw przelicza kwotę transakcji z waluty wprowadzonej przez użytkownika na walutę podstawową. Następnie wynik przelicza na walutę kontraktu projektu. 

### <a name="computing-roll-ups-when-project-actuals-are-recorded-in-multiple-transaction-currencies"></a>Obliczanie zestawień podczas rejestrowania wartości rzeczywistych projektu w wielu walutach transakcji

Usługa Dynamics 365 automatycznie przetwarza zestawienia kwot w różnych walutach. Oto przykład.

| Klasa transakcji | Typ transakcji| Date   | Zasób | Kategoria transakcji | Ilość | Cena jednostkowa | Kwota      | Kurs wymiany | Kwota w walucie podstawowej |
|-------------------|------------------|--------|----------|----------------------|----------|--------------|-------------|---------------|----------------|
| Time              | Nierozliczona sprzedaż   | 14-cze | Jakub  |                      | 8 godz.    | 20 000 JPY    | 160 000 JPY | 123           | 1300,81 USD    |
| Time              | Nierozliczona sprzedaż   | 15-cze | Jakub  |                      | 8 godz.    | 20 000 JPY    | 160 000 JPY | 123           | 1300,81 USD    |
| Wydatek           | Nierozliczona sprzedaż   | 16-cze | Jakub  | Hotel                | 1 szt.     | 250 EUR      | 250 EUR     | 0.94          | 265,95 USD     |
| Wydatek           | Nierozliczona sprzedaż   | 17-cze | Jakub  | Wypożyczenie samochodu           | 1 szt.     | 150 EUR      | 150 EUR     | 0.94          | 159,57 USD     |

Aby obliczyć wartość łącznej nierozliczonej sprzedaży w projekcie, można utworzyć pole zestawienia dla pola **Kwota** we wszystkich pokrewnych wartościach rzeczywistych nierozliczonej sprzedaży. Pole zestawienia to konstrukcja w usłudze Dynamics 365, która umożliwia stosowanie szybkich formuł do pokrewnych rekordów.


[!INCLUDE[footer-include](../includes/footer-banner.md)]