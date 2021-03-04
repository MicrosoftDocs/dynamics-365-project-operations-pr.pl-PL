---
title: Konfigurowanie i korzystanie z płatności dla dostawcy po uiszczonej opłacie
description: W tym temacie przedstawiono sposób tworzenia terminów płatnych po uiszczonej opłacie (PWP), aby można było zwolnić częściowe płatności dostawcy na podstawie płatności klientów.
author: RadhikaRS
manager: AnnBe
ms.date: 03/30/2020
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
ms.openlocfilehash: e872c4a2d35cef4cddc6851615c6c4d73b4e9d9a
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081991"
---
# <a name="set-up-and-use-pay-when-paid-vendor-payments"></a>Konfigurowanie i korzystanie z płatności dla dostawcy po uiszczonej opłacie

[!include [banner](../includes/banner.md)]

Jeśli dostawca został zatwierdzony do pracy w charakterze podwykonawcy, może wstrzymać zapłatę dla dostawcy do momentu zapłacenia nabywcy na pokrycie danego projektu. Aby obsłużyć ten scenariusz, można skonfigurować warunki płatne po otrzymaniu zapłaty (PWP) podczas konfigurowania zamówienia zakupu (PO) u dostawcy.

Jeśli na przykład klient uiszcza kwotę na fakturze projektu, można zwolnić pewną część lub całość kwoty faktury dostawcy. Wystarczy skonfigurować warunki PWP, które spowodują, że dostawca zostanie spłacony po otrzymaniu procentu powiązanej płatności od danego klienta. Jeśli od klienta jest pobierana płatność częściowa, użytkownik może ręcznie zwolnić niektóre z powiązanych faktur od dostawcy w celu dokonania płatności.

W poniższym przykładzie proces jest przedstawiany w trakcie korzystania z warunków PWP.

## <a name="example"></a>Przykład

Organizacja wyraża zgodę na dostarczenie klientowi 100 komputerów, na których zainstalowano oprogramowanie, za cenę 150 USD (USD) za komputer. Następnie zatrudniany jest dostawca, który zapewnia komputery z zainstalowanym oprogramowaniem. Zgodnie z umową klient musi zatwierdzić stan komputerów przed podjęciem zgody na wypłatę. Zasady Twojej organizacji polegają na wstrzymaniu wypłaty dostawcy do czasu zapłacenia przez klienta. Z tego powodu projekt jest skonfigurowany w taki sposób, aby wartość PWP wynosiła 100 procent.

Dostawca wysyła 100 komputerów, na których zainstalowano oprogramowanie, oraz fakturę na 10 000 USD. Ponieważ warunki PWP są ustawiane dla Twojego projektu, dostawca nie jest spłacany po otrzymaniu tych komputerów. Zamiast tego komputery są wysyłane do klienta wraz z fakturą na 15 000 USD. Klient sprawdza komputery i zatwierdza całą kwotę faktury projektu.

Po otrzymaniu pełnej płatności od klienta płacisz 10 000 USD dostawcy — pełną kwotę na fakturze zakupu.

## <a name="set-up-pwp-terms-for-a-project"></a>Konfigurowanie warunków PWP dla projektu

Podczas konfigurowania warunków PWP dla projektu należy określić jako stawkę procentową minimalną kwotę, którą klient musi zapłacić za projekt, aby dostawca otrzymał pieniądze. Kwota progowa jest obliczana automatycznie na fakturach dla klienta projektu. Wykonaj te kroki, aby skonfigurować próg procentowy progu dla warunków PWP.

1. Przejdź do **Zarządzanie projektami i księgowanie** \> **Projekty** \> **Wszystkie projekty**.
2. Znajdź i otwórz projekt, dla którego chcesz skonfigurować warunki PWP.
3. Na skróconej karcie **Kontrakty z dostawcami** wybierz pozycję **Dodaj wiersz**.
3. W polu **Kod konta** wybierz jedną z następujących opcji:

    - **Tabela** : warunki PWP dotyczące dostawcy stosuje się do jednego dostawcy.
    - **Grupa** : warunki PWP dotyczące dostawcy stosuje się do wszystkich dostawców w grupie.
    - **Wszyscy** : warunki PWP dotyczące dostawcy stosuje się do wszystkich dostawców.

4. W przypadku wybrania **Tabeli** lub **Grupy** z poprzedniego kroku w polu **Grupa dostawca/dostawca** wybierz dostawcę lub grupę dostawców, której mają dotyczyć warunki PWP. W przypadku wybrania opcji **Wszystkie** w poprzednim kroku nie można edytować pola **Grupa dostawca/dostawca**.
5. Jeśli warunki zatrzymania dostawcy są ustawione dla dostawcy w polu **Warunki zatrzymania dostawcy** wybierz identyfikator reguły dla warunków zatrzymania.
6. W polu **Procent progu PWP** wprowadź wartość procentową progu projektu. Procent wprowadzony w projekcie określa minimalną kwotę, którą klient musi zapłacić przed uiszczeniem opłaty dla dostawcy.

## <a name="create-a-po-that-has-pwp-terms"></a>Utwórz zamówienie zakupu z warunkami PWP

W przypadku księgowania faktury dostawcy, jeśli dostawcę obowiązują warunki PWP, warunki te są widoczne w wierszach zamówienia zakupu. Aby utworzyć zamówienie zakupu z warunkami PWP wykonaj następujące kroki.

1. Przejdź do **Zaopatrzenie i sourcing** \> **Zamówienia zakupu** \> **Wszystkie zamówienia zakupu**.
2. W okienku akcji wybierz pozycję **Nowe**. Następnie w oknie dialogowym **Tworzenie zamówienia zakupu** wprowadź wymagane informacje i wybierz przycisk **OK**.

    Innym rozwiązaniem jest otworzenie istniejącego zamówienia zakupu na stronie listy **Wszystkich zamówień zakupu**.

4. Na stronie **Zamówienia zakupu** , na skróconej karcie **Wiersze zamówienia zakupu** przejrzyj szczegóły dotyczące wiersza zakupu danego dostawcy. Opcja **Zapłać po otrzymaniu zapłaty** jest wybierana automatycznie, a wartość w polu **Procent progu PWP** jest automatycznie kopiowana z pola **Procent progu PWP** ze strony **Projekty**.
6. Jeśli nie chcesz stosować PWP względem dostawcy w wierszu zamówienia zakupu, wyczyść opcję **Płać po otrzymaniu zapłaty**. W tym przypadku **Procent progu PWP** dla wiersza zakupu zostanie zresetowany do wartości 0 (zero).

## <a name="update-a-customer-payment-and-pay-the-vendor"></a>Aktualizowanie płatności u klienta i spłata

Gdy dostawca wykona swoją pracę nad projektem i prześle fakturę, należy przejrzeć stan projektu i faktury klienta w celu ustalenia, czy dla danego projektu spełniono warunki PWP. Jeśli zostały spełnione warunki PWP dla danego dostawcy, można ustalić, które wiersze na fakturze opłacić na podstawie płatności z tytułu klienta dla danego projektu. W przypadku wybrania opcji zapłaty dostawcy pomimo braku spełnienia warunków PWP, warunki PWP można zastąpić na stronie **Faktura dostawcy z opcją płać po otrzymaniu zapłaty**.

1. Przejdź do obszaru **Zarządzanie projektami i księgowanie** \> **Zapytania i raporty** \> **Zapytania zachowania** \> **Faktura dostawcy z opcją płać po otrzymaniu zapłaty**.
2. Na stronie **Faktura dostawcy z opcją płać po otrzymaniu zapłaty** , w polu wyszukiwania wprowadź wartości, aby znaleźć fakturę zakupu, którą chcesz przejrzeć, a następnie wybierz pozycję **Wyszukaj**.
3. Na skróconej karcie **Wiersze faktury dostawcy** zaznacz wiersze, które chcesz zmienić.
4. Jeśli wartości **Zapłać po uiszczeniu zapłaty** są spełnione, wybierz **Zwolnij płatność dla dostawcy**. Opcja **Zapłać po otrzymaniu zapłaty** jest wyczyszczona, a wartość pola **Gotowe do zapłaty** jest zamieniana na **Tak**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]