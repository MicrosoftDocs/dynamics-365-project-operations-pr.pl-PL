---
title: Zarządzanie cennikami projektu w ofertach projektu
description: Ta temat zawiera informacje na temat pracy z cennikami projektowymi w ofertach. (Sales)
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 4013d2e8cc0d2329f824a17484ee6f4a054a390e
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081935"
---
# <a name="manage-project-price-lists-on-project-quotes-sales"></a>Zarządzanie cennikami projektu w ofertach projektu (sprzedaż)

_**Zastosowane w:** Wdrażanie uproszczone — od okazji do faktury pro forma_

Oferty projektów są zaprojektowane w taki sposób, aby obsługiwały cenniki sprzedaży z wieloma efektywnymi datami. W Dynamics 365 Project Operations dodano nową skojarzoną encję o nazwie **Cenniki projektu**. Ta encja ma relację 1-do-wielu z ofertą projektu.

Cenniki projektu są używane do wyceny transakcji dotyczących godzin i kosztów w projekcie. Jeśli oferta zawiera jeden lub więcej cenników projektu, te cenniki są używane do szacowania czasu i wydatków oraz wartości rzeczywistych w projektach skojarzonych z ofertą za pośrednictwem wiersza oferty.

W przypadku braku cenników projektu dla oferty zostanie wyświetlony komunikat ostrzegawczy. Wiadomość ta zawiera informację, że z powodu braku cenników projektu, szacunkowa i rzeczywista praca nad projektem i koszty nie będą wyceniane. Zamiast tego będą one miały zerową (0) cenę wartości sprzedaży.

## <a name="associate-or-disassociate-a-project-price-list-on-a-project-quote"></a>Kojarzenie lub usuwanie skojarzenia cennika projektu z ofertą projektu

W celu utworzenia lub wybrania określonego cennika służącego do oszacowania pracy i kosztów na podstawie projektu należy wykonać następujące kroki.

1. Z poziomu oferty wybierz kartę **Cena projektu** i w podsiatce wybierz pozycję **+ Dodaj nowy cennik projektu**.
2. Na stronie szybkiego tworzenia wybierz Cennik. Lista rozwijana zawiera wszystkie cenniki, dla których ustawiono wartość **Sprzedaż** , a waluta jest zgodna z walutą z oferty.
4. Wprowadź opis skojarzenia z cennikiem projektu i wybierz pozycję **Zapisz i zamknij**.

Utworzenie skojarzenia cennika projektu.

Aby z ofertą projektu skojarzyć więcej niż jeden cennik projektu, można powtórzyć wcześniejszy proces. Jeśli na skojarzonych cennikach projektu istnieją różne daty efektywne, powinno utworzyć się wiele cenników projektu.

> [!NOTE]
> Project Operations nie obsługuje nachodzących na siebie efektywnych dat cenników projektu. Jeśli istnieje wiele cenników projektu dotyczących transakcji z określonym terminem, cena w tej transakcji będzie domyślnie ustawiona na zero (0).
Aby usunąć skojarzenie cennika projektu, wybierz Cennik projektu, a następnie wybierz pozycję **Usuń cennik projektu oferty**. Cennik jest usuwany z cenników projektu oferty, ale sam cennik nie jest usuwany kompletnie. Usuwane jest tylko skojarzenie z ofertą.

## <a name="set-up-default-project-price-lists-on-a-quote"></a>Konfigurowanie domyślnych cenników projektu dla oferty

Cenniki projektu mogą być ustawiane jako domyślne dla oferty projektu. Dzięki tej konfiguracji wszystkie oferty w organizacji zawsze zaczynają od standardowych cenników dla danego okresu.

### <a name="set-up-organizational-default-for-project-price-lists"></a>Konfigurowanie domyślnych ustawień organizacji dla cenników projektu oferty

1. Wybierz kolejno pozycje **Ustawienia** > **Ogólne** > **Parametry**.
2. Na stronie listy **Aktywne parametry** znajdź rekord i kliknij go dwukrotnie, aby go otworzyć. 
3. Na stronie **Parametry** wybierz kartę **Cennik**. Można zobaczyć listę domyślnych cenników, która jest wyświetlana. To jest lista kosztów standardowych i cenników sprzedaży. Posiadanie cennika sprzedaży powiązanego z każdą walutą, w której prowadzi się transakcje sprawi, że to ten cennik sprzedaży będzie domyślnie używany w każdej utworzonej ofercie, która korzysta z tej waluty.

### <a name="set-up-customer-specific-project-price-lists"></a>Konfigurowanie cenników właściwych dla określonego klienta

Cenniki projektu mogą również zostać skonfigurowane po wynegocjowaniu głównej umowy cenowej z klientem..

W celu skonfigurowania cennika projektu dla konkretnego klienta należy wykonać następujące kroki.

1. W obszarze **Sprzedaż** kliknij przycisk **Klienci** i zaznacz opcję .
2. Na liście aktywnych klientów wybierz i otwórz rekord klienta, dla którego ma zostać wystawiony specjalny cennik.
3. Na karcie **Cenniki projektu** można utworzyć nowe skojarzenie cennika, aby dysponować cennikiem określonym dla danego klienta.

## <a name="create-custom-pricing-on-a-project-quote"></a>Tworzenie niestandardowej kalkulacji cen dla oferty projektu

Po utworzeniu cenników organizacji i domyślnych cenników projektu dla konkretnego klienta, oferty projektowe będą automatycznie utworzone automatycznie za korzystając z tych skojarzeń z cennikami projektu. Jednak w niektórych przypadkach może zaistnieć konieczność utworzenia niestandardowej kalkulacji cen dla określonej oferty projektu. 

1. Z poziomu **Oferty projektu** na karcie **Cennik projektu** sprawdź, czy w podsiatce nie został wybrany konkretny rekord cennika.
2. Wybierz **Utwórz niestandardową kalkulację cen**. Spowoduje to utworzenie kopii wszystkich standardowych cenników skojarzonych z obecną ofertą i skojarzenie tych kopii z ofertą. Istniejące skojarzenia z cennikami standardowymi zostaną usunięte. Sprzedawca może następnie rozpocząć edycję cen w tych kopiach. Te zmienione ceny będą dotyczyć wyłącznie tej oferty projektu.
