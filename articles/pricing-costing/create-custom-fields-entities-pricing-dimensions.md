---
title: Tworzenie pól niestandardowych i encji jako wymiarów kalkulacji cen
description: W tym temat przedstawiono informacje na temat tworzenia niestandardowych zestawów opcji lub encji.
author: rumant
manager: AnnBe
ms.date: 11/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
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
ms.openlocfilehash: fc5917856b8f28d36dc55593a68eba7823a00b36
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 11/25/2020
ms.locfileid: "4642826"
---
# <a name="create-custom-fields-and-entities-as-pricing-dimensions"></a>Tworzenie pól niestandardowych i encji jako wymiarów kalkulacji cen

_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_

Poniższe kroki można wykonać, gdy zechcesz utworzyć niestandardowy zestaw opcji lub encję do użycia jako wymiaru kalkulacji cen. Aby uzyskać więcej informacji, zobacz [Omówienie wymiarów kalkulacji cen](pricing-dimensions-overview.md).  

> [!IMPORTANT]
> Zalecamy, aby wszelkie niestandardowe modyfikacje wymiarów kalkulacji cen wykonywać w osobnym rozwiązaniu. Ta ważna najlepsza praktyka zapewni w przyszłości elastyczność aktualizowania lub usuwania wybranych zmian. Ułatwi ona również ponowne użycie pracy oraz przenoszenie tych zmian do innego wystąpienia. Po wprowadzeniu wszystkich wymaganych zmian wyeksportuj to rozwiązanie jako **rozwiązanie zarządzane** i zaimportuj je do innych wystąpień, aby ponownie użyć ustawień kalkulacji cen.

  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a>Tworzenie niestandardowych pól i zestawów opcji w rozwiązaniu do zarządzania wymiarami kalkulacji cen

Wymiarem kalkulacji cen może być zestaw opcji lub encja. Oba rodzaje wymiarów muszą być utworzone w rozwiązaniu do zarządzania kalkulacjami cen. Etapy tej procedury pokazują, jak tworzyć wymiary oparte na encjach i wymiary oparte na zestawach opcji.

### <a name="entity-based-dimensions"></a>Wymiary oparte na encjach
Aby utworzyć wymiary oparte na encjach, należy wykonać następujące kroki:

1. Przejdź kolejno do: **Ustawienia** > **Rozwiązania**, a następnie kliknij dwukrotnie opcję **Wymiary kalkulacji cen \<your organization name>**.
2. W Eksploratorze rozwiązań w lewym okienku nawigacji kliknij pozycję **Encje**.
3. Wybierz **Nowy**, aby utworzyć nową encję o nazwie **Standardowe stanowisko**. 
4. Wprowadź pozostałe wymagane informacje, a następnie wybierz **Zapisz**.

> ![Definicja encji Standardowe stanowisko](media/Standard-Title-entity-definition.png)

### <a name="option-set-based-dimensions"></a>Wymiary oparte na zestawach opcji 
Można utworzyć dwa wymiary oparte na zestawach opcji. 

- Użyj **lokalizacji pracy zasobu** do śledzenia ceny pracy w lokalizacji **Główna** i **Na miejscu**. 
- Użyj **godzin pracy zasobu** z wartościami **Regularne** i **Nadgodziny**, aby zastosować narzut po zakończeniu pracy.

Poniższa ilustracja zawiera widok wymiaru **Lokalizacja pracy zasobu**. 

> ![Wymiar kalkulacji cen oparty na zestawie opcji zatytułowany Lokalizacja pracy zasobu](media/Option-set-PD-called-Resource-Work-Location.png)

Poniższa ilustracja zawiera widok wymiaru **Godziny pracy zasobu**. 

> ![Wymiar kalkulacji cen oparty na zestawie opcji zatytułowany Godziny pracy zasobu](media/Option-set-PD-called-Resource-Work-Hours.png)

1. Przejdź kolejno do: **Ustawienia** > **Rozwiązania**, a następnie kliknij dwukrotnie opcję **Wymiary kalkulacji cen \<your organization name>**. 
2. W Eksploratorze rozwiązań w lewym okienku nawigacji kliknij pozycję **Zestawy opcji**. 
3. Wybierz **Nowy**, aby utworzyć nowy zestaw opcji, wprowadź pozostałe wymagane informacje, a następnie wybierz **Zapisz**.

## <a name="create-data-for-entity-based-dimensions"></a>Tworzenie danych dla wymiarów opartych na encjach

Dane wymiarów opartych na encjach można tworzyć ręcznie, poprzez import z programu Microsoft Excel lub za pomocą wywołań usług. Czynności opisane w tej procedurze umożliwiają utworzenie dwóch standardowych stanowisk — **Inżynier systemów** i **Starszy inżynier systemów** — na podstawie wymiaru opartego na encji noszącego nazwę **Standardowe stanowisko**. Jeśli ilość danych, które mają zostać utworzone, jest niewielka, jak w poniższym przykładzie, można użyć standardowego formularza.

1. Wybierz pozycję **Szukanie zaawansowane**.
2. Wybierz encję **Standardowe stanowisko** i wybierz pozycję **Wyniki**. Zostaną wyświetlone wszystkie wiersze encji **Standardowe stanowisko**.
3. Wybierz **Nowe**, w polu **Nazwa** wpisz treść „Inżynier systemów”, a następnie wybierz **Zapisz**.
4. Zamyknij stronę. 
5. Powtórz kroki 1–3, aby utworzyć kolejne nowe stanowisko „Starszy inżynier systemów”.

> ![Przykładowe dane encji Standardowe stanowisko](media/ST-data.png)
