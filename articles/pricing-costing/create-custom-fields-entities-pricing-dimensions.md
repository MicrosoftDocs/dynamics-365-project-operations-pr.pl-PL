---
title: Tworzenie pól niestandardowych i encji jako wymiarów kalkulacji cen
description: W tym temat przedstawiono informacje na temat tworzenia niestandardowych zestawów opcji lub encji.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 9dd43be79f8e906298578911b3bff03e66c2f1e5
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082050"
---
# <a name="create-custom-fields-and-entities-as-pricing-dimensions"></a>Tworzenie pól niestandardowych i encji jako wymiarów kalkulacji cen

_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_

Poniższe kroki można wykonać w dowolnym momencie, kiedy zechcesz utworzyć niestandardowy zestaw opcji lub encję.

> [!IMPORTANT]
> Zalecamy, aby wszelkie niestandardowe modyfikacje wymiarów kalkulacji cen wykonywać w osobnym rozwiązaniu. Ta ważna najlepsza praktyka zapewnia elastyczność umożliwiającą w przyszłości wprowadzanie aktualizacji lub usuwanie zmian w razie potrzeby, pomaga wykorzystywać utworzone obiekty do innych celów oraz ułatwia przenoszenie zmian do innych wystąpień. Po wprowadzeniu wszystkich wymaganych zmian należy wyeksportować rozwiązanie jako **Rozwiązanie zarządzane** , a następnie je zaimportować do innych wystąpień i tam wykorzystywać.


## <a name="create-a-custom-solution-for-pricing-dimensions"></a>Tworzenie niestandardowego rozwiązania dla wymiarów kalkulacji cen
1. Wybierz kolejno opcje **Ustawienia** > **Rozwiązania** , a następnie wybierz **Nowy** , aby utworzyć nowe rozwiązanie. 
2. Nazwij rozwiązanie **\<your organization name>nazwa Twojej organizacji> — wymiary kalkulacji cen** , wprowadź pozostałe wymagane informacje, a następnie wybierz **Zapisz**.
  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a>Tworzenie niestandardowych pól i zestawów opcji w rozwiązaniu do zarządzania wymiarami kalkulacji cen

Wymiarem kalkulacji cen może być zestaw opcji lub encja. Oba rodzaje wymiarów muszą być utworzone w rozwiązaniu do zarządzania kalkulacjami cen. Etapy tej procedury pokazują, jak tworzyć wymiary oparte na encjach i wymiary oparte na zestawach opcji.

### <a name="entity-based-dimensions"></a>Wymiary oparte na encjach

1. Przejdź kolejno do: **Ustawienia** > **Rozwiązania** , a następnie kliknij dwukrotnie opcję **Wymiary kalkulacji cen \<your organization name>**.
2. W Eksploratorze rozwiązań w lewym okienku nawigacji kliknij pozycję **Encje**.
3. Wybierz **Nowy** , aby utworzyć nową encję o nazwie **Standardowe stanowisko**. 
4. Wprowadź pozostałe wymagane informacje, a następnie wybierz **Zapisz**.


### <a name="option-set-based-dimensions"></a>Wymiary oparte na zestawach opcji 
Można utworzyć dwa wymiary oparte na zestawach opcji. Wymiar **Lokalizacja pracy zasobu** umożliwia śledzenie pracy w lokalizacjach **Główna** i **Na miejscu** , a wymiar **Godziny pracy zasobu** z wartościami **Regularny** i **Nadgodziny** pozwala stosować narzut po zakończeniu pracy.


1. Przejdź kolejno do: **Ustawienia** > **Rozwiązania** , a następnie kliknij dwukrotnie opcję **Wymiary kalkulacji cen \<your organization name>**. 
2. W Eksploratorze rozwiązań w lewym okienku nawigacji kliknij pozycję **Zestawy opcji**. 
3. Wybierz **Nowy** , aby utworzyć nowy zestaw opcji, wprowadź pozostałe wymagane informacje, a następnie wybierz **Zapisz**.

## <a name="create-data-for-entity-based-dimensions"></a>Tworzenie danych dla wymiarów opartych na encjach

Dane wymiarów opartych na encjach można tworzyć ręcznie, poprzez import z programu Microsoft Excel lub za pomocą wywołań usług. Czynności opisane w tej procedurze umożliwiają utworzenie dwóch standardowych stanowisk — **Inżynier systemów** i **Starszy inżynier systemów** — na podstawie wymiaru opartego na encji noszącego nazwę **Standardowe stanowisko**. Jeśli ilość danych, które mają zostać utworzone, jest niewielka, jak w poniższym przykładzie, można użyć standardowego formularza.

1. Wybierz pozycję **Szukanie zaawansowane** , wybierz **Tytuł standardowy** encji, a następnie wybierz pozycję **Wyniki**. Zostaną wyświetlone wszystkie wiersze encji **Standardowe stanowisko**.
2. Wybierz **Nowe** , w polu **Nazwa** wpisz treść „Inżynier systemów”, a następnie wybierz **Zapisz**.
3. Zamknij formularz. 
4. Powtórz kroki 1–3, aby utworzyć kolejne nowe stanowisko „Starszy inżynier systemów”.

## <a name="add-all-required-entities-and-related-components-to-the-pricing-dimension-solution"></a>Dodawanie wszystkich wymaganych encji i pokrewnych składników do rozwiązania do zarządzania wymiarami kalkulacji cen
Następujące encje usługi trzeba będzie dodać do rozwiązania do zarządzania wymiarami kalkulacji cen. Czynności opisane w tej procedurze umożliwiają wprowadzenie pewnych istotnych zmian w schemacie rozwiązania do zarządzania kalkulacjami cen, tak aby encje dowiedziały się o nowych wymiarach kalkulacji cen.

1. Wybierz **Ustawienia** > **Rozwiązania** , a następnie kliknij dwukrotnie opcję **Wymiary kalkulacji cen \<your organization name>**. 
2. W Eksploratorze rozwiązań w lewym okienku nawigacji kliknij kolejno opcje **Dodaj istniejący** > **Encje**.
3. W oknie dialogowym **Składniki rozwiązania** zaznacz następujące encje:

  - Wartość rzeczywista
  - Zasób, który można zarezerwować
  - Wiersz szacowania
  - Szczegóły wiersza faktury
  - Wiersz arkusza
  - Szczegóły pozycji kontraktu projektu
  - Członek zespołu projektu
  - Szczegóły wiersza oferty
  - Narzut na cenę dla roli
  - Cena roli 
  - Wpis czasu 


> [!NOTE]
> Upewnić się, dla każdej wybranej encji dołączono wszystkie formularze i widoki.

4. Gdy zobaczysz monit o dodanie wszelkich encji zależnych od encji zaznaczonych powyżej, wybierz opcję **Nie**.

