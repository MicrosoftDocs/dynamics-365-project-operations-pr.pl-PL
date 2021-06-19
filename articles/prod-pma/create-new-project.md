---
title: Tworzenie nowego projektu
description: W tym temacie zamieszczono informacje dotyczące tworzenia nowego projektu.
author: Yowelle
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8218747366be8536601cb007318c642ac122536b
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 05/10/2021
ms.locfileid: "6006254"
---
# <a name="create-a-new-project"></a>Tworzenie nowego projektu

[!include [banner](../includes/banner.md)]

Wykonaj poniższe kroki, aby utworzyć nowy projekt.

1. Na stronie **Zarządzanie projektem** wybierz **Nowy projekt**, a następnie wprowadź następujące wartości:

    - **Typ projektu:** czas i materiały
    - **Nazwa projektu:** faza uaktualniania w XYZ 2
    - **Grupa projektów:** TM\_WIP
    - **Identyfikator kontraktu projektu:** 00000002

2. Wybierz pozycję **Utwórz projekt**.

## <a name="assign-a-resource-to-a-project"></a>Przypisywanie zasobu do projektu

1. Na stronie **Pracownicy** na liście **Pracownicy** wybierz rekord pracownika, dla którego wcześniej skonfigurowano kompetencje, i otwórz rekord pracownika.
2. W okienku akcji na karcie **Projekt** w grupie **Ustawienia** kliknij opcję **Przypisz projekty**.
3. Na stronie **Przypisania projektów walidacji zasobów**, na karcie **Projekty**, w polu **Dodaj projekt do wybranych projektów** wybierz Filtr w projekcie **XYZ faza aktualizacji 2**.
4. W okienku **Pozostałe projekty** wybierz projekt, a następnie wybierz przycisk strzałki, aby dodać go do okienka **Wybrane projekty**.

Kategorie zasobu można również przypisać w zależności od potrzeb. Kategoria typu to albo **Koszt**, albo **Przychód**. Typ kategorii jest określany przez organizację. Jeśli do zasobu nie są przypisane żadne kategorie, Finance wyszukuje domyślną kategorię według cen godzinowych dla kosztów i przychodów.

## <a name="set-up-project-resource-and-role-characteristics"></a>Skonfiguruj zasoby projektu i cechy roli

Menedżer projektu może używać funkcji zasobów projektu do tworzenia ról wymaganych w projekcie. Role mogą być używane, jeśli potwierdzone zasoby są nadal nieznane podczas rezerwowania zasobów. Role mogą być tymczasowo rezerwowane jako planowane zasoby, aby można było kontynuować etapy planowania projektów.

[![Przykład roli](./media/projectresourcing05.jpg)](./media/projectresourcing05.jpg) 

**Scenariusz:** Contoso zostało zatrudnione do realizacji projektu typu Czas i materiał, który posiada zatwierdzoną kartę projektu. Młodszy kierownik projektu nadal kończy zakres projektu. Menedżer zasobów obecnie identyfikuje konkretne zasoby, które będą zastrzeżone do pracy nad nowym projektem. Ze względu na krytyczny charakter projektu, sponsor projektu poprosił starszego kierownika projektu jako jedną z ról. Menedżer zasobów musi nabyć nowy zasób i zdefiniować rolę w systemie na wypadek, gdyby młodszy kierownik projektu potrzebował informacji o zasobach podczas planowania projektu.

Poniższe kroki pokazują, jak menedżer zasobów może skonfigurować rolę starszego kierownika projektu i skojarzyć z nią cechy zasobu. Później roli można użyć do wyszukiwania dostępnych zasobów, które pasują do wymaganych kompetencji zasobów.

1. Na stronie **Role ustawień** wybierz **Nowy**, a następnie wprowadź następujące wartości:

    - **Identyfikator roli:** starszy kierownik projektu
    - **Opis:** starszy kierownik projektu

2. Wybierz pozycję **Utwórz**.
3. Zaznacz rolę **Starszy kierownik projektu**, a następnie wybierz pozycję **Konfigurowanie charakterystyki**.
4. W polu **Typ charakterystyki** wybierz opcję **Umiejętności**.
5. W polu **Dostępne charakterystyki** wprowadź umiejętność, która ma zostać wyszukana.
6. W polu **Typ charakterystyki** wybierz opcję **Certyfikat**.
7. W polu **Dostępne charakterystyki** wprowadź typ certyfikatu, który ma zostać wyszukany.

## <a name="assign-a-project-resource-to-a-project"></a>Przypisz zasób projektu do projektu

1. Na stronie **Wszystkie projekty** wybierz projekt **XYZ uaktualnianie faza 2**.
2. Na karcie **Zespół projektowy i planowanie** wybierz opcję **Dodaj**.
3. W polu **Rola** wybierz pozycję **Członek zespołu**.
4. Wybierz **Rezerwuj z kalendarza**.
5. Na stronie **Dostępność zasobów** wybierz **Ustawienia widoku**.
6. Na stronie **Dostosowywanie ustawień widoku** wprowadź następujące wartości:

    - **Format widoku zakresu dat:** Dzień
    - **Wyświetlanie opisów dostępności:** Tak
    - **Wyświetl wydajność pozostałą:** Tak

7. Na liście zasobów wybierz zasób.
8. Wybierz opcję **Ostateczna rezerwacja** i **Pełna dyspozycyjność**.

## <a name="assign-a-resource-to-a-default-role"></a>Przypisz zasób do roli domyślnej

Aby pomóc menedżerom projektów lub zasobów, można dokładniej przeanalizować zasoby, które można zarezerwować dla projektu. Możesz skojarzyć rolę domyślną z istniejącym zasobem lub nowo nabytym zasobem. Na przykład, kiedy Daniel został zatrudniony, posiadał doświadczenia i umiejętności umożliwiające wypełnienie roli analityka biznesowego. Kierownik zasobów przypisał tę rolę jako domyślną rolę Daniela. Dlatego kierownik ds. zasobów dodał Daniela do puli analityków biznesowych, którzy są dostępni do pracy nad projektami.

Podczas rezerwacji zasobów kierownicy projektów mogą filtrować zasoby ról, które są dostępne do pracy nad projektami. Mogą one wykorzystywać te informacje jako kryterium podczas wykonywania wielokryteriówowych analiz decyzji podczas realizacji zasobów. W celu wyszukania zasobów z określonymi umiejętnościami, edukacją i doświadczeniem dla danego projektu mogą również dodać inne charakterystyki zasobów.

**Scenariusz:** Rozpoczął się zatwierdzony projekt, a rola starszego kierownika projektu została zarezerwowana jako planowany zasób na etapie planowania projektu. Kierownik zasobów uzyskał teraz zasób do pełnienia roli starszego kierownika projektu.

1. Na stronie **Lista zasobów** wybierz pozycję **Daniel Goldschmidt**.
2. Na stronie **Rola zasobu** wybierz **Nowy**, a następnie wprowadź następujące wartości:

    - **Efektywność:** wprowadź aktualną datę.
    - **Data wygaśnięcia:** wprowadź **nigdy**.
    - **Rola:** Wpisz **starszy kierownik projektu**.

3. Wybierz **Zapisz**, a następnie zamknij stronę.
4. Na karcie **kompetencje** dodaj umiejętność **ProjectMgmt** i certyfikat **PMP**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]