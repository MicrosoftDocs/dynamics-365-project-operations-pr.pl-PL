---
title: Zaawansowane jednostki organizacyjne
description: Ten artykuł zawiera informacje o jednostkach organizacyjnych w programie Dynamics 365 Project Service Automation.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 03/04/2019
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
ms.openlocfilehash: dd9de490b7d6d847e3226b371e06ac671a7836a8
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8927111"
---
# <a name="about-organizational-units"></a>O jednostkach organizacyjnych 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Dynamics 365 Project Service Automation, jednostka organizacyjna, jest odrębną grupą lub oddziałem w firmie świadczącej usługi, która korzysta z zasobów rozliczanych, które mają stawki kosztów.

W przypadku firm zajmujących się specjalistycznymi usługami, korzystającej z zasobów technicznych w różnych dziedzinach praktyk lub linii biznesowych, koszt wypełniania roli w jednej praktyce lub linii biznesowej może się różnić od kosztów w celu wypełnienia roli w innej praktyce lub linii biznesowej. Jednostki organizacyjne typu koncepcja ułatwiają w tym scenariuszu stworzenie metody grupowania zestawu ról do rozliczania w oddziale firmy z odrębnymi strukturami kosztów dla tych ról.

## <a name="key-attributes-and-associations-of-organizational-units"></a>Podstawowe atrybuty i skojarzenia jednostek organizacyjnych

W usłudze PSA jednostka organizacyjna w PSA ma określoną listę z określonymi walutami i listami kosztów własnych.

Waluta jednostki organizacyjnej to podstawowa waluta, która jest używana do śledzenia kosztów.

Do każdej jednostki organizacyjnej może być dołączona co najmniej jedna lista kosztów własnych. Program PSA stosuje następujące ograniczenia dotyczące cenników, które można dołączać do jednostki organizacyjnej:

- Cenniki muszą znajdować się w walucie jednostki organizacyjnej.
- Cenniki muszą być cenami z list kosztów własnych

Ponadto w encji zasobu znajduje się atrybut jednostki organizacyjnej. Każdy zasób można przypisać do jednej jednostki organizacyjnej.

## <a name="roles-of-organizational-units"></a>Role jednostki organizacyjnej

Jednostka organizacyjna pełni dwie role w PSA:

- **Jednostka zamawiająca** — jednostka organizacyjna reprezentująca grupę lub oddział firmy, która jest głównie odpowiedzialna za sprzedaż i zarządzanie dostawą pracy i usług do klienta. Jednostka zamawiająca jest identyfikowana za pomocą pola **Jednostka zamawiająca** w sekcji nagłówka na stronach **Szansa sprzedaży**, **Oferta**, **Umowa na projekt** i **Projekt**.
- **Jednostka zasobów** jednostka organizacyjna, do której należy zasób lub która jest przypisana do danego zasobu. Dana jednostka organizacyjna może dostarczać swoich zasobów rolom w instrukcjach akcji pracy (SOW) i projektach, których właścicielem jest jednostka zamawiająca.

> ![Jednostki zamawiające i jednostki zasobów.](media/advanced-1.png)

## <a name="organizational-unit-faqs"></a>Jednostka organizacyjna — często zadawane pytania

Poniżej znajdują się odpowiedzi na kilka najczęściej zadawanych pytań dotyczących jednostek organizacyjnych.

### <a name="how-is-the-organizational-unit-entity-in-psa-related-to-the-organization-entity-that-already-exists-in-dynamics-365"></a>W jaki sposób encja jednostki organizacyjnej w PSA powiązana z encją organizacji już istniejącej w programie Dynamics 365?

Encja organizacji w Microsoft Dynamics 365 reprezentuje nazwę wystąpienia globalnego Dynamics 365. Nazwą tą jest z reguły nazwa globalnego przedsiębiorstwa.

Encja jednostki organizacyjnej reprezentuje grupę lub oddział globalnego przedsiębiorstwa. Ta grupa lub oddział zawiera zestaw ról i listę kosztów własnych tych ról, a role i cennik są różne w zależności od ról i cennika innych grup lub oddziałów w przedsiębiorstwie.

Po zainstalowaniu PSA jest tworzona domyślna jednostka organizacyjna na podstawie organizacji. Wszystkie istniejące zasoby są przypisane do domyślnej jednostki organizacyjnej. Jeśli do programu Dynamics 365 zostaną zaimportowani nowi użytkownicy Active Directory lub zasoby, proces importu użytkowników przypisze ich do domyślnej jednostki organizacyjnej w PSA.
 
### <a name="how-does-the-organizational-unit-entity-differ-from-the-business-unit-entity"></a>Jaka jest różnica między encjami jednostek organizacyjnych i biznesowych?

W usłudze Dynamics 365 encja jednostki biznesowej jest konstrukcją zabezpieczeń. Skojarzenie użytkownika z jednostką biznesową determinuje encje i rekordy encji, do których użytkownik ma dostęp. Określa również uprawnienia (tworzenie, odczyt, zapis, usuwanie, dołączanie, dołączanie do, przypisywanie lub udostępnianie) danego użytkownika względem rekordów encji.

Encja jednostki organizacyjnej reprezentuje grupę lub oddział firmy, które mają różne stawki kosztów dla pracowników, którzy są do nich przypisani. Skojarzenie zasobu z jednostką organizacyjną określa koszt zasobu w kontekście udziału w projekcie.

W przypadku implementacji Dynamics 365 należy zoptymalizować autoryzację zabezpieczeń dla hierarchii jednostek biznesowych i przydział użytkowników do jednostek biznesowych. Przypisz wszystkich użytkowników, którzy muszą zwykle korzystać z tego samego zestawu rekordów, do tej samej jednostki biznesowej. Jednostka organizacyjna nie ma wpływu na autoryzację zabezpieczeń lub na dostęp.

#### <a name="example-of-organizational-units-and-business-units"></a>Przykład jednostek organizacyjnych i jednostek biznesowych

Firma Contoso Ltd. w praktyce stosuje technologię firmy Microsoft. Jakub i Emilia są projektantami C\#, ale Emilia jest w Stanach Zjednoczonych, podczas gdy Jakub znajduje się w Indiach. Większość zakontraktowań projektów wymaga zasobów firmy Contoso Indie i contoso US, a Jakub i Emilia wymagają takiego samego poziomu zabezpieczeń w stosunku do projektów w tym obszarze. Jednak koszty deweloperów z firmy Contoso Indie różnią się znacznie od kosztów deweloperów w firmie Contoso US.

Oto optymalny sposób projektowania w tym scenariuszu przy użyciu aplikacji Dynamics 365 i PSA.

1. Utwórz praktykę technologiczną Microsoft jako jednostka biznesowa, i przypisz do niej Jakuba i Emilię. W ten sposób pomożesz zagwarantować, że oboje będą mieli taki sam poziom zabezpieczeń, jak w przypadku wszystkich projektów w tym obszarze. Będą oboje mogli sprawdzić postęp i zgłosić czas, wydatki oraz aktualizacje zadań. 
2. Utwórz dwie jednostki organizacyjne, aby zagwarantować rzetelne odwzorowanie kosztu projektu. 
3. Skojarz Emilię z firmą Contoso US i skojarz Jakuba z firmą Contoso Indie.
4. Przypisz odpowiednie listy kosztów własnych do obu jednostek organizacyjnych. Dzięki temu można zagwarantować, że koszty zarejestrowane w projekcie dotyczące Jakuba i Emilii precyzyjnie odzwierciedlają różnicę kosztów między Contoso US a Contoso Indie.

### <a name="are-organizational-units-related-to-sales-territories-in-dynamics-365"></a>Czy jednostki organizacyjne są związane z obszarami sprzedaży w usłudze Dynamics 365?

Między obszarami lub jednostkami organizacyjnymi nie istnieją żadne skojarzenia ani relacje. Obszar sprzedaży jest zwykle obszarem geograficznym, w którym występuje sprzedaż. Cennik sprzedaży może być skojarzony z każdym obszarem sprzedaży.

Jednostka organizacyjna jest grupą wewnętrzną lub działem w firmie, która śledzi koszty zbioru przydziałów sprzedawanych innym osobom lub klientom zewnętrznym.

#### <a name="example-of-organizational-units-and-sales-territories"></a>Przykład jednostek organizacyjnych i obszarów sprzedaży

Contoso, Ltd. ma dwa centra opracowywania: Contoso US i Contoso Indie. Koszty zasobów różnią się znacząco między tymi dwoma centrami rozwoju.

Contoso sprzedaje usługi IT na wielu międzynarodowych rynkach, takich jak Ameryka Łacińska, Ameryka Północna, Azja, Pacyfik, Europa Zachodnia i Bliski Wschód. Stawka rozliczania za te same role projektów mogą się znacznie różnić między tymi rynkami.

Contoso US i Contoso India powinny zostać skonfigurowane jako jednostki organizacyjne, a każda jednostka organizacyjna powinna mieć własną listę kosztów. Azja (Pacyfik), Ameryka Łacińska, Ameryka Północna, Europa Zachodnia i Bliski Wschód powinny być konfigurowane jako obszary sprzedaży, a każdy obszar sprzedaży powinien mieć własny cennik sprzedaży.

### <a name="why-is-there-a-restriction-on-the-association-of-price-lists-with-organizational-units"></a>Dlaczego istnieje ograniczenie dotyczące skojarzenia cenników z jednostkami organizacyjnymi? 

Ceny sprzedaży są zwykle unikatowe dla obszarów geograficznych lub na rynkach, na których są sprzedawane usługi. Oddziały wewnętrzne firmy zwykle nie mają własnych cen sprzedaży za ten sam typ usług. Natomiast oddziały wewnętrzne mogą mieć różne koszty sprzedaży, w zależności od kwalifikacji zatrudnionych osób oraz warunków robocizny w tym samym regionie, w którym działają. Ponieważ jednostki organizacyjne są modelowane jako oddziały wewnętrzne firmy, mogą mieć tylko cenniki kosztów.

### <a name="why-cant-we-associate-sales-price-lists-to-organizational-units"></a>Dlaczego nie można kojarzyć cenników sprzedaży z jednostkami organizacyjnymi?

W usłudze PSA cenniki sprzedaży można skojarzyć z klientami i obszarami sprzedaży. Encje transakcyjne, takie jak szansa sprzedaży, oferta, kontrakt dotyczący projektu i projektu, używają list cen sprzedaży dołączonych do konta odbiorcy lub obszaru sprzedaży w celu określenia stawek i potencjalnego przychodu w projekcie.

Listy kosztów własnych są skojarzone z jednostkami organizacyjnymi. W przypadku encji transakcyjnych, takich jak szansa sprzedaży, oferta, kontrakt dotyczący projektu i projekt, można użyć list kosztów dołączonych do jednostki zamawiającej w celu określenia kosztów zakontraktowania projektu.

### <a name="are-organizational-units-hierarchical-in-psa"></a>Czy jednostki organizacyjne są hierarchiczne w PSA?

Nr W bieżącej wersji PSA jednostki organizacyjne nie są hierarchiczne. Oznacza to, że nie można:

- Konfigurować wzorca dla domyślnych kosztów własnych, które przechodzą na hierarchię. 
- Przychód z raportu lub koszt został zestawiony na różnych poziomach hierarchii jednostek organizacyjnych.

### <a name="were-a-big-multinational-firm-with-a-complex-multilevel-hierarchy-of-cost-centers-divisions-and-billing-offices-how-can-we-make-the-best-use-of-the-organizational-unit-concept-in-this-version-of-the-project-service-app"></a>Jesteśmy dużą międzynarodową firmą ze złożoną, wielopoziomową hierarchią centrów kosztów, wydziałów i biur fakturowania. Jak najlepiej wykorzystać koncepcję jednostki organizacyjnej w tej wersji aplikacji Project Service?

Jeśli istnieje złożona hierarchia centrów kosztów, działy, oddziały fakturowania itd., jako odrębne jednostki organizacyjne należy skonfigurować węzły liści z tej hierarchii.
W poniższym przykładzie przedstawiono typową hierarchię:

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
 
Jeśli hierarchia w Twojej firmie jest podobna, należy ją ustawić jako płaską listę, tak jak przedstawiono tutaj:
- Contoso India - Praktyka SAP - Konsultanci techniczni 
- Contoso India - Praktyka SAP - Konsultanci funkcjonalni       
- Contoso India - Konsultanci funkcjonalni praktyki Microsoft Technology 
- Contoso India - Konsultanci funkcjonalni praktyki Microsoft Technology 
- Contoso US - Praktyka SAP - Konsultanci techniczni  
- Contoso US - Praktyka SAP - Konsultanci funkcjonalni  
- Contoso US - Konsultanci techniczni praktyki Microsoft Technology 
- Contoso US - Konsultanci funkcjonalni praktyki Microsoft Technology

### <a name="were-a-small-professional-services-company-that-operates-as-only-one-division-how-can-we-best-use-the-organizational-unit-concept-in-the-current-version-of-psa"></a>Jesteśmy małą firmą świadczącą usługi profesjonalne i mamy tylko jeden oddział. Jak najlepiej wykorzystać koncepcję jednostki organizacyjnej w bieżącej wersji PSA?

Jeśli firma ma jeden oddział z jednym cennikiem, nie trzeba konfigurować żadnych jednostek organizacyjnych. Podczas instalacji PSA Dynamics 365 tworzy jedną domyślną jednostkę organizacyjną mającą taką samą nazwę jak organizacja. Domyślnie wszyscy użytkownicy są przypisani do tej jednostki organizacyjnej. Kiedy system wymaga wybrania jednostki organizacyjnej, ta jednostka organizacyjna jest domyślnie zaznaczona.

### <a name="when-a-project-is-created-from-a-quote-or-project-contract-line-the-default-contracting-unit-comes-from-the-quote-or-project-contract-if-a-project-is-created-before-sales-entities-such-as-quote-or-project-contract-what-is-the-default-contracting-unit"></a>W przypadku tworzenia projektu z poziomu oferty lub pozycji kontraktu projektu domyślna jednostka zamawiana jest dostarczana z oferty lub z kontraktu dotyczącego projektu. W przypadku tworzenia projektu przed encjami sprzedażowymi, takimi jak oferta lub kontrakt dotyczący projektu, co to jest domyślna jednostka umowna?

W przypadku tworzenia projektu jego domyślna jednostka jest określana na podstawie użytkownika, który ją utworzył. Taki użytkownik jest również domyślnym menedżerem projektu. Jeśli projekt jest zamapowany na encję sprzedaży, taki jak oferta lub kontrakt dotyczący projektu, jednostka zamawiająca w projekcie jest oparta na encji sprzedaży. W takim przypadku oszacowania projektów mogą być obliczane ponownie, ponieważ lista kosztów kosztu jest używana do obliczania oszacowania kosztów w przypadku zmiany jednostki zamawiającej. Cennik jest używany do obliczania oszacowań sprzedaży, które zostaną zmienione w taki sposób, aby były zsynchronizowane z cennikiem projektu na ofercie.

Pola **Jednostka kontraktująca** i **Waluta** w projekcie są zablokowane do edycji, ponieważ muszą być zsynchronizowane z wartościami w kontrakcie dotyczącym sprzedaży (oferta lub kontrakt projektu), na które ma zostać zamapowany projekt.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
