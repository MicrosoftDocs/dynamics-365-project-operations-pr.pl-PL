---
title: Zarządzanie cennikami projektu w ofercie
description: W tym artykule przedstawiono informacje na temat encji Cennik projektu.
author: rumant
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 8439a03e6557ec531405048ec4149344e283242e
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8933167"
---
# <a name="manage-project-price-lists-on-a-quote"></a>Zarządzanie cennikami projektu w ofercie

_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_

Dynamics 365 Project Operations rozszerza encję cennika w Dynamics 365 Sales. 

## <a name="key-entities"></a>Kluczowe encje

Cennik zawiera informacje dostarczane przez cztery encje:

- **Cennik**: w tej encji są przechowywane informacje o kontekście, walucie, dacie i godzinie dla czasu cennika. Kontekst wskazuje, czy cennik zawiera stawki kosztów ekspresowych i stawki sprzedaży. 
- **Waluta**: ta encja zawiera walutę cen z cennika. 
- **Data**: ta encja jest używana, gdy system próbuje wprowadzić domyślną cenę transakcji. Wybrany jest cennik, który zawiera datę obowiązywania uwzględniającą datę transakcji. Jeśli zostanie znaleziony więcej niż jeden cennik z datą obowiązywania w dniu transakcji dołączony do powiązanej oferty, umowy lub jednostki organizacyjnej, wtedy żadna cena nie będzie domyślna. 
- **Czas**: ta encja służy do przechowywania jednostki czasu, dla której są wyrażane ceny, na przykład stawki dziennej lub godzinowej. 

Encja cennika składa się z trzech tabel pokrewnych przechowujących ceny:

  - **Cena według roli**: w tej tabeli jest przechowywana stawka dla kombinacji wartości ról i jednostek organizacyjnych oraz jest używana do konfigurowania cen opartych na rolach dla zasobów ludzkich.
  - **Cena kategorii transakcji**: w tej tabeli są przechowywane ceny według kategorii transakcji i są używane do konfigurowania cen kategorii wydatków.
  - **Pozycje cennika**: w tej tabeli są przechowywane ceny na produkty z katalogu.
 
Cennik jest kartą stawki. Stawka jest kombinacją encji cennika i pokrewnych wierszy w tabelach cena roli, Cena kategorii transakcji i pozycje cennika.

## <a name="resource-roles"></a>Role zasobu

Termin *rola zasobu* odnosi się do zestawu umiejętności, kompetencji i certyfikacji koniecznych do wykonania określonego zestawu zadań w projekcie.

Czas zasobów ludzkich jest podawany na podstawie roli, którą dany zasób pełni w określonym projekcie. W przypadku czasu zasobu ludzkiego obsługiwana jest wycena i rozliczanie oparte na roli zasobu. Czas może być określany jako cena w dowolnej jednostce w grupie jednostek **czasu**.

Grupa jednostek **Czas** jest tworzona podczas instalowania Project Operations. Jego domyślna jednostka **Godzina**. Nie można usuwać, zmieniać nazw ani edytować atrybutów grupy jednostek **Czas** lub jednostki **Godzina**. Do grupy jednostek **Czas** można jednak dodać inne jednostki. Jeśli użytkownik próbuje usunąć grupę jednostek **czasu** lub jednostkę **godzinową**, może wystąpić awaria logiki biznesowej.
 
## <a name="transaction-categories-and-expense-categories"></a>Kategorie transakcji i kategorie wydatków

Koszty podróży i inne wydatki, które ponosi konsultant projektu, są rozliczane w fakturach dla klientów. Program tworzy cenniki dotyczące kategorii wydatków, korzystając z cenników. Bilet lotniczy, hotel i wynajem samochodu są przykładami kategorii wydatków. Każdy wiersz cennika dla wydatków określa ceny w konkretnej kategorii wydatku. Do wyceny kategorii wydatków są używane trzy następujące metody:

- **Po kosztach**: koszt wydatku jest naliczany klientowi i nie są stosowane żadne marże.
- **Procent narzutu**: procent ponad rzeczywisty koszt jest naliczany klientowi. 
- **Cena jednostkowa**: cena na fakturze jest ustalana dla każdej jednostki w kategorii wydatków. Kwota, która jest naliczana klientowi, jest obliczana na podstawie liczby jednostek wydatku zgłoszonych przez konsultanta. W przebiegu stosowana jest metoda kalkulacji cen na jednostkę. Na przykład kategoria wydatków przebiegu może być skonfigurowana jako 30 USD na dobę lub na 2 USD za jeden kilometr. Kiedy konsultant raportuje mile w projekcie, kwota do rozliczenia jest obliczana na podstawie liczby mil zgłoszonych przez konsultanta.
 
## <a name="project-sales-pricing-and-overrides"></a>Ceny sprzedaży i zastąpienia projektu

W przypadku ofert i kontraktów projektów cennik projektu zawiera inny wzorzec zastąpienia cen niż cennik produktu. W przypadku wiersza oferty opartej na katalogu produktów można zmienić cenę na role i kategorie bezpośrednio w wierszu oferty, ponieważ każdy wiersz oferty wskazuje dokładnie jeden element katalogu. Jednak w wierszu oferty opartej na projekcie nie można zamienić ceny na role i kategorie bezpośrednio w wierszu oferty. Cennik projektu może służyć do obsługi dwóch różnych wzorców zastąpienia.

> [!NOTE]
> Zaleca się, aby w przypadku zasobów projektu i elementów katalogu można było korzystać z osobnego cennika z powodu różnic między nimi podczas ręcznej kalkulacji cen.

Z poszczególnymi encjami może być związany jeden lub więcej cenników skojarzonych z ceną sprzedaży projektu:

- Klient (konto) 
- Szansa sprzedaży 
- Oferta 
- Kontrakt projektu

Skojarzenie tych encji z cennikiem jest wskazane przez cenniki projektu. Istnieje możliwość skojarzenia jednego lub kilku cenników z encjami sprzedaży Klient, Szansa sprzedaży, Oferta i Kontrakt projektu.

Domyślny cennik nie jest automatycznie wprowadzany w rekordzie klienta. Można jednak ręcznie dołączyć Cennik projektu do rekordu klienta. Jednak Cennik należy dołączać ręcznie tylko wtedy, gdy użytkownik ma zainstalowaną niestandardową umowę cenową z klientem. 

Gdy Cennik projektu jest dołączony do encji sprzedaży, program sprawdza poprawność następujących informacji:

- Cennik ma kontekst **Sprzedaż**. 
- Waluta cennika jest zgodna z walutą klienta. 

W kontrakcie dotyczącym projektu program korzysta z następującej kolejności pierwszeństwa, aby automatycznie określać powiązane z nimi cenniki projektu:

1. Oferta
2. Szansa sprzedaży
3. Klient 
4. Ustawienia globalne 

Kiedy Cennik projektu jest wprowadzany domyślnie, system sprawdza poprawność waluty odpowiadającej walucie klienta i, że wprowadzone cenniki domyślne mają kontekst **sprzedaży**.

Istnieje możliwość skojarzenia kilku cenników projektów z encjami sprzedaży Klient, Szansa sprzedaży, Oferta i Kontrakt projektu. Ta funkcja obsługuje specyficzne dla konkretnego kontraktu ceny domyślne na długo działającym kontrakcie projektu, w którym może zaistnieć potrzeba więcej niż jednego cennika w celu zaktualizowania cen ze względu na inflację. Jeśli jednak cenniki skojarzone z encją klient, szansa sprzedaży, oferta lub kontrakt projektu mają nachodzącą na nią datę obowiązywania, cena domyślna może być nieprawidłowa. Dlatego należy się upewnić, że cenniki z nakładającymi się datami nie są skojarzone z tymi encjami.

### <a name="deal-specific-price-overrides"></a>Zastąpienia cen właściwe dla umowy

Można tworzyć specjalne zastąpienia dotyczące wybranych cen w cennikach projektów wprowadzanych domyślnie w ofercie lub kontrakcie projektu.

Domyślnie kontrakt projektu zawsze otrzymuje kopię głównego cennika sprzedaży zamiast bezpośredniego łącza do niego. To zachowanie pozwala zagwarantować, że umowy cenowe ustalone z klientem w celu zestawienia pracy (SOW) nie ulegają zmianie w przypadku zmiany cennika głównego.

W przypadku oferty można jednak skorzystać z cennika głównego. Alternatywnie można skopiować główny cennik i przeprowadzić jego edycję w celu utworzenia niestandardowego cennika, który ma zastosowanie wyłącznie do oferty. Aby utworzyć nowy cennik specyficzny dla oferty, na stronie **oferty** zaznacz pole wyboru **Utwórz niestandardową cenę.** Dostęp do cennika konkretnego projektu można uzyskać tylko z poziomu oferty. 

Po utworzeniu niestandardowego cennika projektu kopiowane są tylko składniki projektu wymienione w cenniku. Innymi słowy — nowy Cennik utworzony jako kopia istniejącego cennika projektu jest dołączony do oferty, a nowy Cennik ma tylko pokrewne ceny ról i ceny w kategoriach transakcji.
  
## <a name="tracking-costs"></a>Śledzenie kosztów

Project Operations śledzi koszty czasu zasobów ludzkich w projektach. Umożliwia również śledzenie kosztów innych kosztów w projekcie, takich jak koszty podróży.

Podobnie jak stawki naliczania, stawki kosztów dla zasobów ludzkich są również konfigurowane przy użyciu cenników. Oto podstawowe różnice w zachowaniu listy kosztów własnych i cennika sprzedaży:

- Stawki kosztu zasobu nie można zastąpić na poziomie określonego projektu, kontraktu czy oferty. Stawki fakturowania mogą być jednak zastępowane na podstawie poszczególnych transakcji, jeśli wprowadzono zmiany dotyczące charakteru transakcji. 

- Do rozpoznawania cennika służy następująca kolejność:

    1. Lista kosztów własnych dołączonych do jednostki organizacyjnej.
    2. Lista kosztów własnych dołączonych do parametrów usługi Project Operations. Ponieważ z parametrami usługi projektów można łączyć listy kosztów własnych w wielu różnych walutach, system dopasowuje walutę kontraktującą jednostki organizacyjnej, kontrakt lub ofertę z walutą z listą kosztów własnych.
    3. W przypadku kosztów metody kalkulacji po kosztach i z marżą nie są stosowane do list kosztów własnych. Nawet w przypadku, gdy te metody kalkulacji cen są używane w wierszach list kosztów własnych w celu skonfigurowania kosztów kategorii transakcji, system zignoruje je i nie zostanie wprowadzony domyślny koszt własny.


[!INCLUDE[footer-include](../includes/footer-banner.md)]