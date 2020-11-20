---
title: Rozwiązywanie kosztów sprzedaży dla oszacowań i wartości rzeczywistych
description: W tym temacie przedstawiono informacje na temat sposobu rozwiązywania stawek sprzedaży na szacunkach i wartościach rzeczywistych.
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 8c18dd734312b2dd147381169f5c3dc38a68a601
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/28/2020
ms.locfileid: "4119566"
---
# <a name="resolve-sales-prices-for-estimates-and-actuals"></a>Rozwiązywanie kosztów sprzedaży dla oszacowań i wartości rzeczywistych

_**Zastosowane do:** Project Operations dla zasobów/scenariuszy nieopartych na zaopatrzeniu_

W przypadku rozwiązywania cen sprzedaży dla oszacowań i wartości rzeczywistych w Dynamics 365 Project Operations w pierwszej kolejności jest używana data i waluta pokrewnej oferty projektu lub kontraktu w celu rozwiązania cennika sprzedaży. Po rozwiązaniu cennika w systemie jest w nim rozpoznawana cena sprzedaży lub stawka rozliczana.

## <a name="resolve-sales-rates-on-actual-and-estimate-lines-for-time"></a>Rozwiązywanie stawek kosztów w wartościach rzeczywistych i oszacowaniach dla wiersza czas

W Project Operations są używane wiersze szacowania czasu w celu określenia wiersza oferty i szczegółów pozycji kontraktu na czas oraz przydziałów zasobów w projekcie.

Po rozwiązaniu cennika na potrzeby sprzedaży system wykonuje poniższe kroki, aby ustawić stawkę rozliczeń.

1. System korzysta z pól **Rola**, **Firma zasobów** oraz **Jednostka zasobów** z wiersza szacowania dla czasu, w celu dopasowania do wierszy rozwiązanego cennika ról. To dopasowanie zakłada, że używasz przygotowanych wymiarów kalkulacji dla stawek rozliczeń. Jeśli system został skonfigurowany w taki sposób, aby odpowiadał innym polom niż **Rola**, **Firma zasobów** i **Jednostka zasobów**, to nastąpi połączenie, które będzie pobierało pasującą cena kategorii roli.
2. Jeśli aplikacja znajdzie wiersz ceny roli, który ma stawkę kosztu dla połączenia **Rola**, **Firma zasobów** oraz **Jednostką zasobów**, to będzie to domyślna stawka kosztu.
3. Jeśli aplikacja nie może dopasować wartości pól **Rola**, **Firma zasobów** i **Jednostka zasobów**, program pobiera pasujące wiersze z rolą, ale ustawiane są wartości null **Jednostki zasobów**. Gdy system znajdzie pasujący rekord ceny, będzie domyślnie określać stawkę z rekordu. To dopasowanie zakłada konfigurację wstępną dla względnego priorytetu **Roli** vs **Jednostki zasobów** jako wymiaru ceny sprzedaży.

> [!NOTE]
> W przypadku konfiguracji innej prioretyzacji **Roli**, **Firmy zasobów** i **Jednostki zasobów** lub jeśli istnieją inne wymiary mające wyższy priorytet, to zachowanie odpowiednio się zmieni. System pobiera rekordy cen ról wraz z wartościami odpowiadającymi poszczególnym wartościom wymiarów kalkulacji cen w kolejności według priorytetu. Wiersze, które mają wartości null dla tych wymiarów są ostatnie.

## <a name="resolve-sales-rates-on-actual-and-estimate-lines-for-expense"></a>Rozwiązywanie stawek kosztów w wartościach rzeczywistych i oszacowaniach dla wydatku

W Project Operations są używane wiersze szacowania wydatków w celu określenia wiersza oferty i szczegółów pozycji kontraktu na wydatki oraz wierszy oszacowania wydatków w projekcie.

Po rozwiązaniu cennika na potrzeby sprzedaży system wykonuje poniższe kroki, aby ustawić cenę jednostkową sprzedaży.

1. System korzysta z połączenia pól **Kategoria** oraz **Jednostka** z wiersza szacowania dla wydatku, w celu dopasowania do wiersza ceny kategorii w rozwiązanym cenniku.
2. Jeśli system znajdzie wiersz ceny kategorii, który ma stawkę sprzedaży dla połączenia pól **Kategoria** oraz **Jednostką zasobów**, wtedy będzie to domyślna stawka sprzedaży.
3. Jeśli system znajdzie pasujący wiersz cena kategorii, może użyć metody kalkulacji cen do domyślnego podania ceny sprzedaży. W poniższej tabeli podano domyślne zachowanie cen kosztów w Project Operations.

    | Kontekst | Metoda kalkulacji cen | Cena domyślna |
    | --- | --- | --- |
    | Szacowanie | Cena jednostkowa | Na podstawie wiersza cena kategorii |
    | &nbsp; | Po kosztach | 0.00 |
    | &nbsp; | Narzut na koszt | 0.00 |
    | Rzeczywiste | Cena jednostkowa | Na podstawie wiersza cena kategorii |
    | &nbsp; | Po kosztach | Na podstawie wartości rzeczywistych powiązanych z kosztem |
    | &nbsp; | Narzut na koszt | Stosując narzut zdefiniowany w wierszu kategoria cena na stawce kosztu jednostkowego dla pokrewnego kosztu |

4. Jeśli system nie jest w stanie dopasować wartości pól **Kategorii** oraz **Jednostki**, domyślna stawka sprzedaży wynosi zero (0).
