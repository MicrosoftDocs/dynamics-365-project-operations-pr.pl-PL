---
title: Tworzenie zaawansowanych kontraktów dotyczących rozliczeń na podstawie postępu
description: W tym temacie wyjaśniono, jak tworzyć kontrakty projektów, tak aby można było generować faktury dla klientów na podstawie procentu wykonanej pracy.
author: RadhikaRS
manager: AnnBe
ms.date: 03/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: b1de330df8cf85ed30c0ee4e4f2f2fe74d05dbff
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5289517"
---
# <a name="create-advanced-contracts-for-billing-based-on-progress"></a>Tworzenie zaawansowanych kontraktów dotyczących rozliczeń na podstawie postępu
[!include [banner](../includes/banner.md)]

W tym temacie wyjaśniono, jak tworzyć kontrakty projektów, tak aby można było tworzyć faktury dla klientów na podstawie procentu wykonanej pracy. Kwoty na fakturze są obliczane automatycznie w odniesieniu do kategorii budżetu pracy skonfigurowanej dla projektu. Harmonogram faktury jest ustawiany podczas negocjowania kontraktu dotyczącego projektu z klientem.

Procedury opisane w tym temacie służą do konfigurowania kontraktu, skojarzonego projektu oraz reguł fakturowania, które obliczają kwoty faktur dla kategorii budżetów pracy skonfigurowanych dla danego projektu.

Po utworzeniu kontraktu i projektu można skonfigurować szczegółowe informacje o projekcie. Na przykład można zdefiniować działania i przypisać pracowników do projektu.

## <a name="example"></a>Przykład

Twoja organizacja jest przedsiębiorstwem rozwijającym oprogramowanie. Wyrażasz zgodę na opracowywanie pakietu obsługi kont płacy dla klienta z łączną opłatą na kwotę 20 000 USD. Twoja organizacja wyraża zgodę na fakturowanie klienta w miarę wykonywania określonych wartości procentowych projektu. Konfigurowanie poniższych kategorii projektu dla pracy jest możliwe w taki sposób, że można z nich korzystać w procesie fakturowania:

- Doradztwo
- Zaprojektuj
- Instalacja

Skonfigurujesz także reguły rozliczeniowe, które automatycznie obliczają kwoty faktur dla procentu pracy projektowej wykonanej dla każdej kategorii.

Menedżer budżetu tworzy budżet dla kategorii projektów. Ilość pracy wykonanej jest automatycznie obliczana jako wartość procentowa pracy rzeczywistej w porównaniu z wartościami zabudżetowanymi.

## <a name="prerequisites"></a>Wymagania wstępne

Przed utworzeniem projektu, który korzysta z reguł fakturowania, należy skonfigurować sekwencje numerów dla reguł fakturowania i arkusz opłat używany do księgowania postępu fakturowania.

1. Przejdź do **Zarządzanie projektami i księgowanie** \> **Ustawienia** \> **Parametry zarządzania projektami i księgowanie**.
2. Na stronie **Zarządzanie projektami i parametry księgowania**, na karcie **Sekwencje numerów** skonfiguruj sekwencję numerów, która ma być używana podczas tworzenia reguł fakturowania.
3. Wybierz kolejno pozycje **Zarządzanie projektami i księgowanie** \> **Arkusze** \> **Opłaty**.
4. Na stronie **Arkusz opłat** wybierz opcję **Nowy** i wprowadź nazwę arkusza.

## <a name="create-a-contract-for-progress-billings"></a>Tworzenie kontraktu dotyczącego fakturowania postępu

Ta procedura służy do tworzenia kontraktu projektu dotyczącego projektów o stałej cenie. Faktura jest tworzona w momencie, gdy praca wykonana w projekcie osiągnie określoną wartość procentową.

1. Przejdź do **Zarządzanie projektami i księgowanie** \> **Wszystkie projekty** \> **Kontrakty projektu**.
2. Na stronie szczegółów **Kontraktu projektu** wybierz opcję **Nowy**.
3. W oknie dialogowym **Nowy kontrakt dotyczący projektu** ustaw następujące pola:

    - **Nazwa/nazwisko**
    - **Typ finansowania**
    - **Źródło finansowania**
    - **Waluta sprzedaży** — Domyślnie ta waluta jest używana na fakturach klienta skojarzonych z kontraktem dotyczącym projektu. Można jednak zmienić walutę sprzedaży na określonej fakturze dla danego klienta.

4. Wybierz pozycję **OK**. Informacje zostaną skopiowane do nagłówka strony **Kontrakty projektów**.
5. Na stronie **Kontrakty projektu** wypełnij pozostałe informacje wymagane do projektu.

## <a name="create-a-project-for-progress-billings"></a>Tworzenie projektu dotyczącego fakturowania postępu

Wykonaj te kroki, aby utworzyć projekt i wszystkie podprojekty skojarzone z kontraktem dotyczącym projektu.

1. Przejdź do **Zarządzanie projektami i księgowanie** \> **Projekty** \> **Wszystkie projekty**.
2. Na stronie **Wszystkie projekty** wybierz **Nowy**.
3. W oknie dialogowym **Nowy projekt**, w polu **Typ projektu** wybierz opcję **Czas i materiały**.
4. Wybierz grupę projektu. Grupa projektu definiuje informacje dotyczące księgowania dla projektów przypisanych do grupy.
5. Wybierz pozycję **Utwórz projekt**.
6. Po utworzeniu projektu ustaw etap projektu na **W toku**.

## <a name="create-a-budget-for-a-project"></a>Utwórz budżet dla projektu

kategorie budżetowe automatycznie obliczają kwoty faktur dla procentu pracy wykonanej dla każdej kategorii. Wykonaj te kroki, aby utworzyć kategorie budżetu dla kosztów szacunkowych.

1. Przejdź do **Zarządzanie projektami i księgowanie** \> **Projekty** \> **Wszystkie projekty**.
2. Na stronie **Wszystkie projekty** wybierz odpowiedni projekt i otwórz go.
3. Na stronie **Projekty** w okienku akcji na karcie **Plan**, w grupie **Budżet** wybierz pozycję **Budżet projektu**.
4. Na stronie **Budżet projektu** wprowadź szacowany koszt dla każdej kategorii w projekcie.

## <a name="create-billing-rules-for-progress-billings"></a>Tworzenie reguł fakturowania dla fakturowania postępu

1. Przejdź do **Zarządzanie projektami i księgowanie** \> **Wszystkie projekty** \> **Kontrakty projektu**.
2. Na stronie listy **Kontrakty projektów** wybierz i otwórz kontrakt projektu.
3. Na stronie kontrakt projektu na skróconej karcie **Reguły fakturowania** wybierz pozycję **Dodaj**.
4. Na stronie **Reguła fakturowania** w polu **Typ wiersza** wybierz pozycję **Postęp**.
5. Na skróconej karcie **Szczegóły wiersza reguły fakturowania**, w polu **Wartość kontraktu** wprowadź łączną wartość kontraktu.
6. W polu **Kategoria** wybierz kategorię, w której ma zostać zaksięgowana transakcja opłat.
7. W polu **Projekt** wybierz projekt korzystający z reguły fakturowania.
8. Opcjonalnie: Przypisz regułę fakturowania do dodatkowych projektów. Na skróconej karcie **Projekt**, w sekcji **Dostępne projekty** wybierz projekt, a następnie wybierz przycisk strzałki w prawo, aby dodać projekt do sekcji **Wybrane projekty**.
9. Opcjonalnie: należy obliczyć kwotę procentową zatrzymania przez klienta na fakturze. Na skróconej karcie **Warunki zatrzymania płatności** wybierz źródło finansowania, a następnie w polu **Procent zatrzymania** wprowadź wartość procentową zatrzymania.
10. Powtórz te kroki, aby utworzyć dodatkowe reguły fakturowania dla kontraktu dotyczącego projektu.


[!INCLUDE[footer-include](../includes/footer-banner.md)]