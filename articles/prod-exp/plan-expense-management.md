---
title: Konfiguracja zarządzania wydatkami
description: W tym artykule opisano zagadnienia i decyzje, które należy uwzględnić w procesie planowania przed skonfigurowaniem modułu Zarządzanie wydatkami w Microsoft Dynamics 365 Finance.
author: KimANelson
ms.date: 08/29/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: GlobalCategory, ProjCategory, TrvLocations, TrvParameters, TrvPaymethod, TrvPerDiems
audience: Application User
ms.reviewer: johnmichalak
ms.custom: 23001
ms.assetid: aa3fd14d-7e94-4603-985f-ca26d6f860ea
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d919a26000b127dd6fb2fd8a49d79e3087f1c403
ms.sourcegitcommit: 7e419a5f73f80fa887084e3b212c90586fc397dd
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 05/05/2022
ms.locfileid: "8710009"
---
# <a name="configure-expense-management"></a>Konfiguracja zarządzania wydatkami

W tym temacie opisano kwestie i decyzje, które należy wziąć pod uwagę w procesie planowania, zanim użytkownik skonfiguruje Zarządzanie wydatkami. W zarządzaniu wydatkami są przechowywane informacje o metodach płatności, zapotrzebowaniach na wyjazdy raportach o wydatkach, zasadach itp.

Z uwagi na fakt, że podczas planowania konfiguracji w celu zarządzania wydatkami wiele decyzji jest opartych na hierarchiach organizacji i strukturze finansowej, należy odwołać się do tych obszarów w dokumentach planowania.

## <a name="intercompany-expenses"></a>Wydatki międzyfirmowe

W przypadku włączania kosztów międzyfirmowych można zezwolić firmom i pracownikom na otrzymywanie kosztów w imieniu innego podmiotu prawnego i gromadzenie płatności od podmiotu prawnego w ramach Twojej organizacji. Na przykład pracownik w firmie A wykona projekt dla podmiotu prawnego B, a w projekcie poniesie koszty związane z podróżą. Jeśli są włączone koszty międzyfirmowe, pracownik będzie mógł zaraportować koszty księgowania kosztów w firmie B, a koszty muszą zostać zapłacone przez firmę prawną. Jeśli organizacja nie ma wielu osób prawnych, nie trzeba włączać kosztów międzyfirmowych.

**Decyzja:** Czy chcesz włączyć koszty międzyfirmowe?

## <a name="financial-management"></a>Zarządzanie finansami

Zarządzanie wydatkami jest ściśle zintegrowane z zarządzaniem finansami organizacji. Wiele konfiguracji w celu zarządzania wydatkami będzie oparte na decyzjach podjętych przez użytkownika o finansach organizacji. W poniższych sekcjach przedstawiono różne obszary, które wymagają planowania i podejmowania decyzji na podstawie decyzji finansowych i wytycznych zespołu kierowniczego.

### <a name="per-diems"></a>Każdego dnia

Należy zdefiniować dzienną dietę pracownika wykorzystywaną w danej organizacji. Z uwagi na fakt, że diety zwykle pokrywają koszty, takie jak posiłki, zakwaterowanie i inne koszty dodatkowe, można utworzyć reguły dotyczące diet w danej organizacji. stawki dzienne mogą być oparte na porze roku, miejscu podróży lub obydwu tych danych. Podczas tworzenia reguły diety dziennej można określić, że procent stawki diety będzie wstrzymany, jeśli pracownik otrzymuje dodatkowe posiłki lub usługi. Można również ustawić przedziały stawek dziennych oraz maksymalne i minimalne godziny, gdy może być zastosowana stawka dzienna do kosztów podróży pracownika.

**Decyzja:**

- Domyślne reguły diety dla pierwszego i ostatniego dnia:

    - Jaka jest minimalna liczba godzin, jaką pracownik może zgłosić w ciągu dnia i czy wciąż otrzyma dietę?
    - Czy istnieje redukcja kwoty oferowanej za pierwszy lub ostatni dzień? W przypadku zmniejszenia o ile procent jest zmniejszona dieta?
    - Czy istnieje redukcja kwoty oferowanej za pierwszy lub ostatni dzień, jeśli chodzi o hotel? W przypadku zmniejszenia o ile procent jest zmniejszona dieta?
    - Czy istnieje redukcja kwoty oferowanej za pierwszy lub ostatni dzień, jeśli chodzi o inne wydatki? W przypadku zmniejszenia o ile procent jest zmniejszona dieta?

- Domyślne reguły diety:

    - Czy istnieje procentowa redukcja diety na posiłek, jeśli np. posiłek jest bezpłatny? W przypadku zmniejszenia, o ile procent jest zmniejszona dieta za każdy posiłek?
    - Czy zmniejszenie posiłku jest obliczane na dzień, na podróż czy zależnie od liczby dań dziennie?
    - Czy kwoty diety powinny być zaokrąglane w zwykły sposób, czy zaokrąglane w górę?
    - Czy diety są obliczane w ramach okresu 24 godzin lub w ramach dnia kalendarzowego?

- Reguły diety oparte na lokalizacji:

    - Czy stawki diety są różne, zależnie od lokalizacji? Jakie lokalizacje są uwzględnione?
    - Jeśli stawki diety są różne w zależności od lokalizacji, dla każdej lokalizacji jest podawana procentowa kwota dla następujących typów kosztów:

        - Posiłki
        - Hotel
        - Inne wydatki

### <a name="expense-management-journals-and-accounts"></a>Dzienniki zarządzania wydatkami i konta

Do zarządzania wydatkami jest wymagane użycie wielu arkuszy i kont. Należy zdecydować, na przykład, czy to same konto jest używane w przypadku zaliczek gotówkowych i sporów związanych z kartą kredytową.

**Decyzja:**

- Które arkusze księgi otrzymują zaksięgowane arkusze z wydatków?
- Które konto jest używane na potrzeby zaliczek?
- Czy zaliczki gotówkowe mają być od razu księgowane?

### <a name="payment-methods"></a>Formy płatności

W przypadku umożliwienia pracownikom ponoszenia kosztów w imieniu firmy należy zdefiniować metody płatności, które mogą być używane przez pracowników. Użytkownik może na przykład zezwolić pracownikom na korzystanie z gotówki lub firmowej karty kredytowej. Użytkownik może również zezwolić pracownikom na korzystanie z osobistych kart kredytowych, a następnie zwracać im koszty. Konieczne jest podjęcie następujących decyzji dla każdej dozwolonej metody płatności.

**Decyzja:**

- Jakie formy płatności są dozwolone?
- Do kogo jest przypisana forma płatności?
- Czy istnieje typ konta rozliczeniowego? Jeśli istnieje typ konta rozliczeniowego, to jaki jest?
- Jeśli istnieje typ konta rozliczeniowego, to co to za konto?
- Jeśli forma płatności to karta kredytowa, czy metoda płatności ma być używana tylko wraz z importowanymi transakcjami?

### <a name="expense-categories-and-shared-categories"></a>Kategorie wydatków i dzielone kategorie

Kiedy pracownicy tworzą raport o wydatkach, każdy z tych rekordów musi być skojarzony z kategorią wydatku. Kategorie wydatków są pobierane z kategorii udostępnionych, które mogą być współużytkowane przez osoby prawne należące do organizacji. Te kategorie mogą być również udostępniane w programie Project Management and Accounting w zależności od sposobu pracy w organizacji. W zależności od definicji organizacji i wskazówek dotyczących zespołu implementacji należy określić, czy kategorie używane w zarządzaniu wydatkami będą używane tylko w zarządzaniu wydatkami, czy powinny być wspólne dla zarządzania projektem i księgowania oraz zarządzania wydatkami. Należy pamiętać, że kategorie te mogą być współużytkowane przez zarządzanie projektami oraz zarządzanie wydatkami i kosztami, a także między zarządzaniem projektami oraz ich księgowaniem i produkcją, ale nie pomiędzy wydatkami a produkcją. Konieczne jest podjęcie następujących decyzji dla każdej kategorii wydatku.

**Decyzja:**

- Jaka jest kategoria wydatków? Mogą to być np. kategorie dla lotów, hotelu lub trasy.
- Czy kategoria wydatków może być używana także w zarządzaniu projektami i księgowaniu?
- Jaki jest typ wydatków?
- Jaka jest domyślna metoda płatności dla tej kategorii wydatków?
- Czy wydatki w tej kategorii muszą zostać wyszczególnione?
- Jaka jest główne domyślne konto dla tej kategorii wydatków?
- Jaka jest domyślna grupa podatków od sprzedaży w danej kategorii wydatku?
- Czy dla kategorii wydatków są dozwolone dodatkowe formy płatności? Czy jeśli są dozwolone dodatkowe formy płatności, to jakie?
- Czy w tej kategorii wydatków znajdują się podkategorie? Jeśli tak, to należy także podjąć następujące decyzje:

    - Czy któraś z podkategorii jest wykluczona ze zwrotu podatku?
    - Jaka jest grupa podatku od sprzedaży w tych podkategoriach?

Jeśli kategoria wydatków jest używana także w zarządzaniu projektami i księgowaniu, odpowiedz na pozostałe pytania. W przeciwnym razie przejdź do następnej sekcji.

- Które konta kosztów będą używane w następujących wydatkach?

    - Koszt
    - Alokacja płac
    - PWT-koszt wartość
    - Koszt przedmiotu
    - PWT-koszt wartość-przedmiotu
    - Naliczona strata
    - PWT-naliczona strata

- Które konta przychodów będą używane w następujących kategoriach?

    - Zafakturowany przychód
    - Naliczony przychód — wartość sprzedaży
    - PWT — wartość sprzedaży
    - Naliczony przychód — produkcja
    - PWT-produkcja
    - Naliczony przychód — zysk
    - PWT-zysk
    - Naliczony przychód — subskrypcja
    - PWT-subskrypcja

### <a name="taxes"></a>Podatki

W przypadku podatków powiązanych z wydatkami należy określić, co ma zostać uwzględnione lub włączone w raportach o wydatkach.

**Decyzja:**

- Czy kwoty wydatków uwzględniają podatki?
- Czy ma być włączone odzyskiwanie podatku z wydatków?

    > [!NOTE]
    > Po zaplanowaniu księgi głównej, jeśli postanowiono stosować amerykańskie stawki podatku i używajać reguł podatkowych, nie można włączyć zwrotu podatku na pokrycie kosztów. (Aby zastosować amerykańskie reguły podatkowe i podatek amerykański, należy ustawić opcję **Stosowanie reguł opodatkowania podatku** na **Tak**.)

## <a name="policies"></a>Zasady

Tworząc zasady raportów o wydatkach, można pomóc organizacji w zaoszczędzeniu czasu i pieniędzy w momencie, gdy pracownicy ponoszą koszty w jej imieniu. Zasady pomagają zagwarantować, że pracownicy nie przekroczą budżetu, pomagają udostępniać wszystkie wymagane informacje i wydawać pieniądze wyłącznie wtedy, gdy rzeczywiście trzeba. Konieczne jest podjęcie następujących decyzji dla każdej zasady raportu dotyczącego wydatków oraz wszystkich utworzonych przez użytkownika zasad zatwierdzania raportów o wydatkach.

**Decyzja:**

- Jaka jest nazwa zasady?
- Czego dotyczy zasada wydatków?
- Jeśli zdecydowano się na włączenie kosztów międzyfirmowych, które firmy z organizacji będą stosować te zasady?
- Kiedy zasady wejdą w życie?
- Kiedy zasady wygasną?
- Czym jest reguła zasad?
- Jaki jest wynik reguły zasad?


[!INCLUDE[footer-include](../includes/footer-banner.md)]