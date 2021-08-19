---
title: Poprawianie księgowania propozycji faktur dla projektów wersji roboczej
description: W tym temacie wyjaśniono sposób dopasowywania informacji księgowych do wersji roboczej propozycji faktury.
author: sigitac
ms.date: 06/07/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 153a239d4b88906909ee0bfae8a18cabebc3766399290d83bb79f5d6375a942c
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/06/2021
ms.locfileid: "6999329"
---
# <a name="correct-the-accounting-on-draft-project-invoice-proposals"></a>Poprawianie księgowania propozycji faktur dla projektów wersji roboczej

_**Zastosowane do:** Project Operations dla zasobów/scenariuszy nieopartych na zaopatrzeniu_

*Szczegóły operacyjne* faktur projektów są obsługiwane przez menedżera projektu na fakturze pro forma. Szczegółowe informacje to m.in. decyzja o godzinach, kosztach, materiałach lub kamieniach milowych, które muszą być zafakturowane, kursach oraz stosowaniu kwot z góry i pozostałych kwot. Po potwierdzeniu oryginalnej faktury pro forma możesz dostosować szczegóły operacyjne, tworząc i potwierdzając [korygującą fakturę pro forma](../proforma-invoicing/corrective-invoices.md).

*Szczegóły księgowania* faktur projektów są zachowywane w dokumencie faktury dostępnej dla klienta. Szczegóły te obejmują obliczenia podatku sprzedaży oraz wymiary finansowe stosowane do faktury. Ten temat zawiera szczegółowe informacje dotyczące sposobu dostosowania tych szczegółów księgowych w wersji roboczej propozycji faktury projektu.

## <a name="adjust-sales-tax"></a>Korekta podatku

Domyślne grupy podatku dla rozliczeń i grupy podatku dla pozycji można dostosowywać bezpośrednio w dokumencie propozycji faktury. Aby dostosować te grupy, wybierz opcję **Edytuj**, a następnie w każdym wierszu propozycji faktury projektu wprowadź nową wartość w polu **Grupa podatku** lub **Grupa pozycji dla pozycji**.

## <a name="adjust-financial-dimensions"></a>Korekta wymiarów finansowych

Nie można edytować wymiarów finansowych bezpośrednio w wierszu propozycji faktury projektu. Zamiast tego należy wykonać poniższe kroki w celu dostosowania wymiarów finansowych w propozycji faktury projektu.

1. W propozycji faktury projektu wybierz opcję **Usuń wszystko**, aby usunąć wiersze propozycji faktury projektu.

    > [!NOTE]
    > Przycisk **Usuń wszystko** jest dostępny tylko wtedy, gdy administrator systemu włączy funkcję **Usuń wierszy propozycji faktury w przypadku korzystania z aplikacji Project Operations dla scenariuszy obejmujących zasobów/nieobejmujących magazynowania** w obszarze roboczym **Zarządzanie funkcjami**.

2. Korekta wymiarów finansowych:

    - **Transakcje konta (kamienie milowe rozliczeń):** przejdź do pozycji **Wszystkie projekty** \> **Zarządzaj** \> **Transakcje konta** wybierz kamień milowy, który wymaga korekty. Następnie na karcie **Wymiary finansowe** zaktualizuj wartości zgodnie z wymaganiami.
    - **Transakcje czasu, wydatków i materiałów:** na stronie **Zaksięgowane transakcje projektu** wybierz opcję **Dostosuj księgowanie** w celu zaktualizowania wymiarów finansowych.

3. Po zakończeniu przetwarzania wartości wymiarów finansowych przejdź do obszaru **Zarządzanie projektami i księgowanie** \> **Okresowe** \> **Integracja aplikacji Project Operations** i wybierz opcję **Import z tabeli przejściowej**, aby uruchomić proces okresowy. W tym procesie do ponownego utworzenia wierszy propozycji faktury projektu są używane zaktualizowane wartości wymiarów finansowych. Zaktualizowane wartości są następnie używane w podrzędnej i głównej księdze projektu podczas księgowania faktury projektu.
