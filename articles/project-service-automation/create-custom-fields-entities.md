---
title: Tworzenie niestandardowych pól i encji
description: W tym temacie przedstawiono sposób tworzenia zestawów opcji i encji we własnym rozwiązaniu na platformie Power Apps.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/26/2018
ms.topic: article
ms.prod: Project Service
ms.service: business-applications
ms.assetid: fb160bfd-e037-4a21-a968-3ff2e6e16481
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
ms.openlocfilehash: 7ee30e3bb6b8034ef226e2e9181195685355011f
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/24/2020
ms.locfileid: "3754391"
---
# <a name="create-custom-fields-and-entities"></a>Tworzenie niestandardowych pól i encji 

Poniższe kroki można wykonać w dowolnym momencie, kiedy zechcesz utworzyć niestandardowy zestaw opcji lub encję na platformie Power Apps.  
Procedury w tym temacie należy wykonać przy użyciu interfejsu internetowego usługi Project Service Automation (PSA).

> [!IMPORTANT]
> Zalecamy, aby wszelkie niestandardowe modyfikacje wymiarów kalkulacji cen wykonywać w osobnym rozwiązaniu. Ta ważna najlepsza praktyka zapewnia elastyczność umożliwiającą w przyszłości wprowadzanie aktualizacji lub usuwanie zmian w razie potrzeby, pomaga wykorzystywać utworzone obiekty do innych celów oraz ułatwia przenoszenie zmian do innych wystąpień. Po wprowadzeniu wszystkich wymaganych zmian należy wyeksportować rozwiązanie jako **Rozwiązanie zarządzane**, a następnie je zaimportować do innych wystąpień i tam wykorzystywać.


## <a name="create-a-custom-solution-for-pricing-dimensions"></a>Tworzenie niestandardowego rozwiązania dla wymiarów kalkulacji cen
1. W programie PSA kliknij kolejno opcje **Ustawienia** > **Rozwiązania**, a następnie kliknij przycisk **Nowy**, aby utworzyć nowe rozwiązanie. 
2. Nazwij rozwiązanie **\<nazwa Twojej organizacji> — wymiary kalkulacji cen**, wprowadź pozostałe wymagane informacje, a następnie kliknij przycisk **Zapisz**.

> ![Tworzenie niestandardowego rozwiązania dla wymiarów kalkulacji cen](media/Creation-of-custom-pricing-dimension-solution.PNG)
  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a>Tworzenie niestandardowych pól i zestawów opcji w rozwiązaniu do zarządzania wymiarami kalkulacji cen

Wymiarem kalkulacji cen może być zestaw opcji lub encja. Oba rodzaje wymiarów muszą być utworzone w rozwiązaniu do zarządzania kalkulacjami cen. Etapy tej procedury pokazują, jak tworzyć wymiary oparte na encjach i wymiary oparte na zestawach opcji.

### <a name="entity-based-dimensions"></a>Wymiary oparte na encjach

1. W programie PSA kliknij kolejno opcje **Ustawienia** > **Rozwiązania**, a następnie kliknij dwukrotnie pozycję **\<nazwa Twojej organizacji> — wymiary finansowe**.
2. W Eksploratorze rozwiązań w lewym okienku nawigacji kliknij pozycję **Encje**.
3. Kliknij przycisk **Nowy**, aby utworzyć nową encję o nazwie **Standardowe stanowisko**. Wprowadź pozostałe wymagane informacje, a następnie kliknij przycisk **Zapisz**.

> ![Definicja encji Standardowe stanowisko](media/Standard-Title-entity-definition.png)


### <a name="option-set-based-dimensions"></a>Wymiary oparte na zestawach opcji 
Można utworzyć dwa wymiary oparte na zestawach opcji. Wymiar **Lokalizacja pracy zasobu** umożliwia śledzenie pracy w lokalizacjach **Główna** i **Na miejscu**, a wymiar **Godziny pracy zasobu** z wartościami **Regularny** i **Nadgodziny** pozwala stosować narzut po zakończeniu pracy.


1. W programie PSA kliknij kolejno opcje **Ustawienia** > **Rozwiązania**, a następnie kliknij dwukrotnie pozycję **\<nazwa Twojej organizacji> — wymiary kalkulacji cen**. 
2. W Eksploratorze rozwiązań w lewym okienku nawigacji kliknij pozycję **Zestawy opcji**. 
3. Kliknij przycisk **Nowy**, aby utworzyć nowy zestaw opcji, wprowadź pozostałe wymagane informacje, a następnie kliknij przycisk **Zapisz**.

> ![Wymiar kalkulacji cen oparty na zestawie opcji zatytułowany Lokalizacja pracy zasobu ](media/Option-set-PD-called-Resource-Work-Location.png)

> ![Wymiar kalkulacji cen oparty na zestawie opcji zatytułowany Godziny pracy zasobu ](media/Option-set-PD-called-Resource-Work-Hours.PNG)


## <a name="create-data-for-entity-based-dimensions"></a>Tworzenie danych dla wymiarów opartych na encjach

Dane wymiarów opartych na encjach można tworzyć ręcznie, poprzez import z programu Microsoft Excel lub za pomocą wywołań usług. Czynności opisane w tej procedurze umożliwiają utworzenie dwóch standardowych stanowisk — **Inżynier systemów** i **Starszy inżynier systemów** — na podstawie wymiaru opartego na encji noszącego nazwę **Standardowe stanowisko**. Jeśli ilość danych, które mają zostać utworzone, jest niewielka, jak w poniższym przykładzie, można użyć standardowego formularza.

1. W programie PSA kliknij opcję **Szukanie zaawansowane**. Zaznacz encję **Standardowe stanowisko** i kliknij przycisk **Wyniki**. Zostaną wyświetlone wszystkie wiersze encji **Standardowe stanowisko**.
2. Kliknij pozycję **Nowy**. W polu **Nazwa** wpisz treść „Inżynier systemów”, a następnie kliknij przycisk **Zapisz**.
3. Zamknij formularz. 
4. Powtórz kroki 1–3, aby utworzyć kolejne nowe stanowisko „Starszy inżynier systemów”.

> ![Przykładowe dane encji Standardowe stanowisko ](media/ST-data.png)

## <a name="add-all-required-psa-entities-and-related-components-to-the-pricing-dimension-solution"></a>Dodawanie wszystkich wymaganych encji i pokrewnych składników programu PSA do rozwiązania do zarządzania wymiarami kalkulacji cen
Następujące encje usługi Project Service trzeba będzie dodać do rozwiązania do zarządzania wymiarami kalkulacji cen. Czynności opisane w tej procedurze umożliwiają wprowadzenie pewnych istotnych zmian w schemacie rozwiązania do zarządzania kalkulacjami cen, tak aby encje dowiedziały się o nowych wymiarach kalkulacji cen.

1. W programie PSA kliknij kolejno opcje **Ustawienia** > **Rozwiązania**, a następnie kliknij dwukrotnie pozycję **\<nazwa Twojej organizacji> — wymiary finansowe**. 
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

> ![Dodawanie istniejących encji do rozwiązania do zarządzania wymiarami kalkulacji cen](media/Existing-entities-to-PD-solution.png)

> ![Wybieranie składników rozwiązania](media/Dimension-Components.png)

> [!NOTE]
> Upewnić się, dla każdej wybranej encji dołączono wszystkie formularze i widoki.

4. Gdy zobaczysz monit o dodanie wszelkich encji zależnych od encji zaznaczonych powyżej, kliknij opcję **Nie**.

> ![Opcja niedołączania pokrewnych składników](media/Do-not-include-required.png)


