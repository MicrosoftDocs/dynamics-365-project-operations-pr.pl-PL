---
title: Jednostki organizacyjne
description: W tym artykule opisano pojęcie jednostek organizacyjnych oraz sposób tworzenia i obsługi jednostek organizacyjnych w Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 1/31/2022
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
ms.reviewer: johnmichalak
ms.openlocfilehash: a20a37b61db68d70869a11e10bef5d30c422b1eb
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8921637"
---
# <a name="organizational-units-overview"></a>Przegląd jednostek organizacyjnych

W programie Microsoft Dynamics 365 Project Operations *jednostka organizacyjna* to odrębna grupa lub oddział w firmie świadczącej usługi profesjonalne, która zatrudnia płatne zasoby ze stawkami kosztów.

W przypadku firm świadczących usługi profesjonalne, które zatrudniają zasoby techniczne w różnych obszarach praktyki lub liniach biznesowych, koszt wypełnienia roli może się różnić w zależności od obszaru praktyki lub linii biznesowej, w której dana rola jest pełniona. W tym scenariuszu koncepcja jednostek organizacyjnych pomaga, zapewniając sposób grupowania zestawu ról podlegających rozliczeniu w dziale firmy, który ma odrębną strukturę kosztów dla tych ról.

## <a name="the-concept-of-organizational-units-in-project-operations"></a>Pojęcie jednostek organizacyjnych w Project Operations

W usłudze Project Operations jednostka organizacyjna w PSA ma określoną listę z określonymi walutami i listami kosztów własnych.

Waluta jednostki organizacyjnej to podstawowa waluta, która jest używana do śledzenia kosztów.

Do każdej jednostki organizacyjnej może być dołączona co najmniej jedna lista kosztów własnych. Program Project Operations stosuje następujące ograniczenia dotyczące cenników, które można dołączać do jednostki organizacyjnej:

- Cenniki muszą znajdować się w walucie jednostki organizacyjnej.
- Cenniki muszą być cenami z list kosztów własnych.

Ponadto encja Zasób zawiera atrybut dla jednostki organizacyjnej. Każdy zasób można przypisać do jednej jednostki organizacyjnej.

### <a name="roles-of-organizational-units"></a>Role jednostki organizacyjnej

Jednostka organizacyjna pełni dwie role w Project Operations:

- **Jednostka zamawiająca** — jednostka organizacyjna reprezentująca grupę lub oddział firmy, która jest głównie odpowiedzialna za sprzedaż i zarządzanie dostawą pracy i usług do klienta. Jednostka zamawiająca jest identyfikowana za pomocą pola **Jednostka zamawiająca** w sekcji nagłówka na stronach **Szansa sprzedaży**, **Oferta**, **Umowa na projekt** i **Projekt**.
- **Jednostka zasobów** jednostka organizacyjna, do której należy zasób lub która jest przypisana do danego zasobu. Dana jednostka organizacyjna może dostarczać swoich zasobów rolom w instrukcjach akcji pracy (SOW) i projektach, których właścicielem jest jednostka zamawiająca.

![Jednostki zamawiające i jednostki zasobów.](media/OrgUnits.png)

### <a name="organizational-unit-faq"></a>Często zadawane pytania dotyczące jednostek organizacyjnych

Poniżej znajdują się odpowiedzi na kilka najczęściej zadawanych pytań dotyczących jednostek organizacyjnych.

#### <a name="how-is-the-organizational-unit-entity-in-project-operations-related-to-the-organization-entity-that-already-exists-in-dynamics-365"></a>W jaki sposób encja jednostki organizacyjnej w Project Operations powiązana z encją organizacji już istniejącej w programie Dynamics 365?

Encja organizacji w Dynamics 365 reprezentuje nazwę wystąpienia globalnego Dynamics 365. Nazwą tą jest z reguły nazwa globalnego przedsiębiorstwa.

Encja jednostki organizacyjnej reprezentuje grupę lub oddział globalnego przedsiębiorstwa. Ta grupa lub oddział zawiera zestaw ról i listę kosztów własnych tych ról, a role i cennik są różne w zależności od ról i cennika innych grup lub oddziałów w przedsiębiorstwie.

Po zainstalowaniu Project Operations jest tworzona domyślna jednostka organizacyjna na podstawie organizacji. Wszystkie istniejące zasoby są przypisane do domyślnej jednostki organizacyjnej. Jeśli do programu Dynamics 365 zostaną zaimportowani nowi użytkownicy Active Directory lub zasoby, proces importu użytkowników przypisze ich do domyślnej jednostki organizacyjnej w Project Operations.

#### <a name="how-does-the-organizational-unit-entity-differ-from-the-business-unit-entity"></a>Jaka jest różnica między encjami jednostek organizacyjnych i biznesowych?

W usłudze Dynamics 365 encja jednostki biznesowej jest konstrukcją zabezpieczeń. Skojarzenie użytkownika z jednostką biznesową determinuje encje i rekordy encji, do których użytkownik ma dostęp. Określa również uprawnienia (tworzenie, odczyt, zapis, usuwanie, dołączanie, dołączanie do, przypisywanie lub udostępnianie) danego użytkownika względem rekordów encji.

Encja jednostki organizacyjnej reprezentuje grupę lub oddział firmy, które mają różne stawki kosztów dla pracowników, którzy są do nich przypisani. Skojarzenie zasobu z jednostką organizacyjną określa koszt zasobu w kontekście udziału w projekcie.

W przypadku implementacji Dynamics 365 należy zoptymalizować autoryzację zabezpieczeń dla hierarchii jednostek biznesowych i przydział użytkowników do jednostek biznesowych. Przypisz wszystkich użytkowników, którzy muszą zwykle korzystać z tego samego zestawu rekordów, do tej samej jednostki biznesowej. Jednostka organizacyjna nie ma wpływu na autoryzację zabezpieczeń lub na dostęp.

**Przykład pokazuje jedną potencjalną różnicę w modelowaniu jednostek organizacyjnych i jednostek biznesowych**

Firma Contoso Ltd. w praktyce stosuje technologię firmy Microsoft. Jakub i Emilia są projektantami C\#, ale Emilia jest w Stanach Zjednoczonych, podczas gdy Jakub znajduje się w Indiach. Większość zakontraktowań projektów wymaga zasobów firmy Contoso Indie i contoso US, a Jakub i Emilia wymagają takiego samego poziomu zabezpieczeń w stosunku do projektów w tym obszarze. Jednak koszty deweloperów z firmy Contoso Indie różnią się znacznie od kosztów deweloperów w firmie Contoso US.

Oto optymalny sposób projektowania w tym scenariuszu przy użyciu aplikacji Dynamics 365 i Project Operations.

1. Utwórz praktykę technologiczną Microsoft jako jednostka biznesowa, i przypisz do niej Jakuba i Emilię. W ten sposób pomożesz zagwarantować, że oboje będą mieli taki sam poziom zabezpieczeń, jak w przypadku wszystkich projektów w tym obszarze. Oboje będą mogli sprawdzać postępy i raportować czas, wydatki, zużycie materiałów i aktualizacje zadań.
2. Utwórz dwie jednostki organizacyjne, aby zagwarantować rzetelne odwzorowanie kosztu projektu.
3. Skojarz Emilię z firmą Contoso US i skojarz Jakuba z firmą Contoso Indie.
4. Przypisz odpowiednie listy kosztów własnych do obu jednostek organizacyjnych. Dzięki temu można zagwarantować, że koszty zarejestrowane w projekcie dotyczące Jakuba i Emilii precyzyjnie odzwierciedlają różnicę kosztów między Contoso US a Contoso Indie.

#### <a name="are-organizational-units-related-to-sales-territories-in-dynamics-365"></a>Czy jednostki organizacyjne są związane z obszarami sprzedaży w usłudze Dynamics 365?

Między obszarami lub jednostkami organizacyjnymi nie istnieją żadne skojarzenia ani relacje. Obszar sprzedaży jest zwykle obszarem geograficznym, w którym występuje sprzedaż. Cennik sprzedaży może być skojarzony z każdym obszarem sprzedaży.

Jednostka organizacyjna jest grupą wewnętrzną lub działem w firmie, która śledzi koszty zbioru przydziałów sprzedawanych innym osobom lub klientom zewnętrznym.

**Przykład pokazujący jedną potencjalną różnicę w modelowaniu jednostek organizacyjnych i terytoriów sprzedaży**

Contoso, Ltd. ma dwa centra opracowywania: Contoso US i Contoso Indie. Koszt zasobów różni się znacznie między tymi dwoma centrami rozwoju. Firma Contoso sprzedaje swoje usługi informatyczne (IT) na wielu rynkach międzynarodowych, takich jak Ameryka Łacińska, Ameryka Północna, Azja i Pacyfik, Europa Zachodnia i Bliski Wschód. Stawka rozliczania za te same role projektów mogą się znacznie różnić między tymi rynkami. Contoso US i Contoso India powinny zostać skonfigurowane jako jednostki organizacyjne, a każda jednostka organizacyjna powinna mieć własną listę kosztów. Azja (Pacyfik), Ameryka Łacińska, Ameryka Północna, Europa Zachodnia i Bliski Wschód powinny być konfigurowane jako obszary sprzedaży, a każdy obszar sprzedaży powinien mieć własny cennik sprzedaży.

#### <a name="why-is-there-a-restriction-on-the-association-of-price-lists-with-organizational-units"></a>Dlaczego istnieje ograniczenie dotyczące skojarzenia cenników z jednostkami organizacyjnymi?

Ceny sprzedaży są zwykle unikatowe dla obszarów geograficznych lub na rynkach, na których są sprzedawane usługi. Oddziały wewnętrzne firmy zwykle nie mają własnych cen sprzedaży za ten sam typ usług. Natomiast oddziały wewnętrzne mogą mieć różne koszty sprzedaży, w zależności od kwalifikacji zatrudnionych osób oraz warunków robocizny w tym samym regionie, w którym działają. Ponieważ jednostki organizacyjne są modelowane jako oddziały wewnętrzne firmy, mogą mieć tylko cenniki kosztów.

#### <a name="why-cant-we-associate-sales-price-lists-with-organizational-units"></a>Dlaczego nie można kojarzyć cenników sprzedaży z jednostkami organizacyjnymi?

W Project Operations cenniki sprzedaży można skojarzyć z klientami i obszarami sprzedaży. Encje transakcyjne, takie jak szansa sprzedaży, oferta, kontrakt dotyczący projektu i projektu, używają list cen sprzedaży dołączonych do konta odbiorcy lub obszaru sprzedaży w celu określenia stawek i potencjalnego przychodu w projekcie.

Listy kosztów własnych są skojarzone z jednostkami organizacyjnymi. W przypadku encji transakcyjnych, takich jak szansa sprzedaży, oferta, kontrakt dotyczący projektu i projekt, można użyć list kosztów dołączonych do jednostki zamawiającej w celu określenia kosztów zakontraktowania projektu.

#### <a name="are-organizational-units-hierarchical-in-project-operations"></a>Czy jednostki organizacyjne są hierarchiczne w Project Operations?

Nie W bieżącej wersji Project Operations jednostki organizacyjne nie są hierarchiczne. Dlatego nie możesz wykonywać następujących zadań:

- Skonfiguruj wzorzec do wprowadzania domyślnych cen kosztów własnych, które przechodzą w górę hierarchii.
- Przychód z raportu lub koszt został zestawiony na różnych poziomach hierarchii jednostek organizacyjnych.

#### <a name="were-a-big-multinational-firm-that-has-a-complex-multilevel-hierarchy-of-cost-centers-divisions-and-billing-offices-how-can-we-best-use-the-concept-of-organizational-units-in-the-current-version-of-project-operations"></a>Jesteśmy dużą firmą wielonarodowych, która ma złożoną, wielonadniową hierarchię centrów kosztów, oddziałów i biur rozliczeniowych. Jak najlepiej wykorzystać koncepcję jednostek organizacyjnych w obecnej wersji Project Operations?

Jeśli istnieje złożona hierarchia centrów kosztów, działy, oddziały fakturowania itd., jako odrębne jednostki organizacyjne należy skonfigurować węzły liści z tej hierarchii.

W poniższym przykładzie przedstawiono typową hierarchię.

**Contoso India**

- Praktyka SAP

    - Konsultanci techniczni
    - Konsultanci funkcjonalni

- Microsoft Technology Practice

    - Konsultanci techniczni
    - Konsultanci funkcjonalni

**Contoso US**

- Praktyka SAP

    - Konsultanci techniczni
    - Konsultanci funkcjonalni

- Microsoft Technology Practice

    - Konsultanci techniczni
    - Konsultanci funkcjonalni

Jeśli twoja hierarchia przypomina ten przykład, musisz ustawić ją jako płaską listę, jak pokazano tutaj:

- Contoso India - Praktyka SAP - Konsultanci techniczni
- Contoso India - Praktyka SAP - Konsultanci funkcjonalni
- Contoso India - Konsultanci funkcjonalni praktyki Microsoft Technology
- Contoso India - Konsultanci funkcjonalni praktyki Microsoft Technology
- Contoso US - Praktyka SAP - Konsultanci techniczni
- Contoso US - Praktyka SAP - Konsultanci funkcjonalni
- Contoso US - Konsultanci techniczni praktyki Microsoft Technology
- Contoso US - Konsultanci funkcjonalni praktyki Microsoft Technology

#### <a name="were-a-small-professional-services-company-that-operates-as-only-one-division-how-can-we-best-use-the-concept-of-organizational-units-in-the-current-version-of-project-operations"></a>Jesteśmy małą firmą świadczącą usługi profesjonalne i mamy tylko jeden oddział. Jak najlepiej wykorzystać koncepcję jednostek organizacyjnych w obecnej wersji Project Operations?

Jeśli firma ma jeden oddział z jednym cennikiem, nie trzeba konfigurować żadnych jednostek organizacyjnych. Podczas instalacji Project Operations tworzy jedną domyślną jednostkę organizacyjną mającą taką samą nazwę jak organizacja. Domyślnie wszyscy użytkownicy są przypisani do tej jednostki organizacyjnej. Kiedy system wymaga wybrania jednostki organizacyjnej, ta jednostka organizacyjna jest domyślnie zaznaczona.

#### <a name="when-a-project-is-created-from-a-quote-or-project-contract-line-the-default-contracting-unit-comes-from-the-quote-or-project-contract-what-is-the-default-contracting-unit-if-a-project-is-created-before-sales-entities-such-as-quote-or-project-contract"></a>W przypadku tworzenia projektu z poziomu oferty lub pozycji kontraktu projektu domyślna jednostka zamawiana jest dostarczana z oferty lub z kontraktu dotyczącego projektu. Jaka jest domyślna jednostka zamawiająca, jeśli projekt jest tworzony przed encjami sprzedaży, takimi jak oferta lub umowa na projekt?

W przypadku tworzenia projektu jego domyślna jednostka jest określana na podstawie użytkownika, który ją utworzył. Taki użytkownik jest również domyślnym menedżerem projektu. Jeśli projekt jest zamapowany na encję sprzedaży, taki jak oferta lub kontrakt dotyczący projektu, jednostka zamawiająca w projekcie jest oparta na encji sprzedaży. W takim przypadku oszacowania projektów mogą być obliczane ponownie, ponieważ lista kosztów kosztu jest używana do obliczania oszacowania kosztów w przypadku zmiany jednostki zamawiającej. Cennik jest używany do obliczania oszacowań sprzedaży, które zostaną zmienione w taki sposób, aby były zsynchronizowane z cennikiem projektu na ofercie.

Pola **Jednostka kontraktująca** i **Waluta** w projekcie są zablokowane do edycji, ponieważ muszą być zsynchronizowane z wartościami w kontrakcie dotyczącym sprzedaży (oferta lub kontrakt projektu), na które ma zostać zamapowany projekt.

## <a name="create-and-maintain-organizational-units-in-project-operations"></a>Tworzenie i utrzymywanie jednostek organizacyjnych w Project Operations

Aby utworzyć jednostkę organizacyjną w Project Operations, wykonaj następujące czynności.

1. Przejdź do **Ustawienia \> jednostki organizacyjne**.
2. Wybierz **Nowy**.
3. W obszarze **Ogólne** wprowadź wpisz nazwę jednostki organizacyjnej w **Nazwa**. Następnie ustaw inne pola zgodnie z wymaganiami.
4. Wybierz **Zapisz**, aby utworzyć rekord i kontynuować jego edycję.
5. W **Cenniki kosztowe**, wybierz znak plus (**+**), aby dodać cennik. Tutaj możesz dodać tylko cenniki, które mają kontekst **Koszt**.
6. W polu **Nazwa**, kliknij przycisk **Szukaj** i wybierz cennik, który chcesz udostępnić tej jednostce organizacyjnej. Kontynuuj dodawanie cenników zgodnie z wymaganiami.
7. Po zakończeniu dodawania cenników wybierz **Zapisz** w prawym dolnym rogu ekranu.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
