---
title: Tworzenie niestandardowych pól i encji
description: W tym temacie przedstawiono sposób tworzenia zestawów opcji i encji we własnym rozwiązaniu na platformie Power Apps.
author: Rumant
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 3d838bde8a3d7cbc15e06fb3289924468c284a8a
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 05/10/2021
ms.locfileid: "5998964"
---
# <a name="create-custom-fields-and-entities"></a>Tworzenie niestandardowych pól i encji 

[!include [banner](../includes/psa-now-project-operations.md)]

Poniższe kroki można wykonać w dowolnym momencie, kiedy zechcesz utworzyć niestandardowy zestaw opcji lub encję na platformie Power Apps.  
Procedury w tym temacie należy wykonać przy użyciu interfejsu internetowego usługi Project Service Automation (PSA).

> [!IMPORTANT]
> Zalecamy, aby wszelkie niestandardowe modyfikacje wymiarów kalkulacji cen wykonywać w osobnym rozwiązaniu. Ta ważna najlepsza praktyka zapewnia elastyczność umożliwiającą w przyszłości wprowadzanie aktualizacji lub usuwanie zmian w razie potrzeby, pomaga wykorzystywać utworzone obiekty do innych celów oraz ułatwia przenoszenie zmian do innych wystąpień. Po wprowadzeniu wszystkich wymaganych zmian należy wyeksportować rozwiązanie jako **Rozwiązanie zarządzane**, a następnie je zaimportować do innych wystąpień i tam wykorzystywać.

  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a>Tworzenie niestandardowych pól i zestawów opcji w rozwiązaniu do zarządzania wymiarami kalkulacji cen

Wymiarem kalkulacji cen może być zestaw opcji lub encja. Oba rodzaje wymiarów muszą być utworzone w rozwiązaniu do zarządzania kalkulacjami cen. Etapy tej procedury pokazują, jak tworzyć wymiary oparte na encjach i wymiary oparte na zestawach opcji.

### <a name="entity-based-dimensions"></a>Wymiary oparte na encjach

1. W programie PSA kliknij opcję **Ustawienia** > **Rozwiązania**, a następnie kliknij dwukrotnie opcję **Wymiary kalkulacji cen \<your organization name>**.
2. W Eksploratorze rozwiązań w lewym okienku nawigacji kliknij pozycję **Encje**.
3. Kliknij przycisk **Nowy**, aby utworzyć nową encję o nazwie **Standardowe stanowisko**. Wprowadź pozostałe wymagane informacje, a następnie kliknij przycisk **Zapisz**.

> ![Definicja encji Standardowe stanowisko](media/Standard-Title-entity-definition.png)


### <a name="option-set-based-dimensions"></a>Wymiary oparte na zestawach opcji 
Można utworzyć dwa wymiary oparte na zestawach opcji. Wymiar **Lokalizacja pracy zasobu** umożliwia śledzenie pracy w lokalizacjach **Główna** i **Na miejscu**, a wymiar **Godziny pracy zasobu** z wartościami **Regularny** i **Nadgodziny** pozwala stosować narzut po zakończeniu pracy.


1. W programie PSA kliknij opcję **Ustawienia** > **Rozwiązania**, a następnie kliknij dwukrotnie opcję **Wymiary kalkulacji cen \<your organization name>**. 
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




[!INCLUDE[footer-include](../includes/footer-banner.md)]