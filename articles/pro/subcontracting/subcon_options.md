---
title: Opcje podwykonawstwa dla członków zespołu projektu
description: W tym temacie wyjaśniono opcje podwykonawstwa dla członków zespołu projektu w aplikacji Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: tonyafehr
ms.author: rumant
ms.openlocfilehash: 4db283db728b50ccf76eafabfd643313620bbce2
ms.sourcegitcommit: 45893132bd8bfaf944ee0ac855484684dd1ee945
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/09/2021
ms.locfileid: "7902916"
---
# <a name="subcontracting-options-for-project-team-members"></a>Opcje podwykonawstwa dla członków zespołu projektu

[!include [banner](../../includes/dataverse-preview.md)]

_**Zastosowane w:** Wdrażanie uproszczone — od okazji do faktury pro forma_

W aplikacji Microsoft Dynamics 365 Project Operations można ocenić opcje podwykonawstwa dostępne dla co najmniej jednego członka zespołu projektu. Dostępne opcje podwykonawstwa umożliwiają:

- Tworzenie nowej podumowy i/lub tworzenie nowych wierszu istniejącej podumowy dla wybranych członków zespołu projektu. 
- Rezerwowanie względem już istniejącej podumowy i wiersza podumowy. 

Można wybierać spośród dostępnych opcji podwykonawstwa dla ogólnych członków zespołu projektu lub wybierać spośród członków zespołu projektu, których nazwany zasób jest pracownikiem kontraktowym. 

Nie ma opcji podwykonawstwa dostępnych dla następujących osób:

- Członkowie zespołu projektu, którzy są pracownikami w ramach personelu. 
- Członkowie zespołu projektu już skojarzenie i podumową i pozycją podumowy. 

## <a name="subcontracting-an-unstaffed-project-team-member"></a>Podwykonawstwo dla nieobsadzonego członka zespołu projektu

Aby przejrzeć i wybrać dostępne opcje podwykonawstwa dla ogólnego lub niezatwierdzonego członka zespołu projektu, wykonaj następujące kroki:

1. Wybierz co najmniej jeden rekord członka zespołu projektu, w którym zasób jest zasobem ogólnym.
2. Upewnij się, że żaden z wybranych rekordów członków zespołu projektu nie jest już podwykonawcą. 
3. Wybierz pozycję **Opcje podwyonawstwa** w siatce podrzędnej członków zespołu projektu. Otworzy się okno dialogowe **Opcje podwykonawstwa**. 
4. Jeśli w kroku 1 wybrano tylko jeden rekord członka zespołu projektu, dostępne będą następujące opcje:
    - Tworzenie nowych pozycji podumowy. 
    - Rezerwowanie w ramach istniejącej podumowy Jeśli w kroku 1 wybrano wiele rekordów członków zespołu projektu, jedyną dostępną opcją jest utworzenie nowych pozycji podumowy.
5. Opcja rezerwacji względem istniejącej pozycji podumowy umożliwia wybranie podumowy i pozycji podumowy, względem której odbędzie się rezerwacja. Wybierając pozycję podumowy w celu zarezerwowania dyspozycyjności, należy się upewnić, że wybrano pozycję podumowy dla czasu, a rola wymagana przez członka zespołu projektu odpowiada roli zakupionej w pozycji podumowy.
6. Po wybraniu opcji utworzenia nowych pozycji podumowy dla członków zespołu projektu system umożliwi wybranie podumowy, która ma utworzyć te wiersze. Podumowa, którą użytkownik wybierze w celu utworzenia nowych wierszy, powinna mieć stan **Wersja robocza**. Po wybraniu tej opcji w celu utworzenia nowych pozycji podumowy dla wybranych członków zespołu projektu system utworzy po jednej pozycji podumowy dla każdego członka zespołu projektu. Rola, godziny i daty zostaną skopiowane z członka zespołu projektu do każdej tworzonej pozycji podumowy. 
7. Gdy ogólny członek zespołu jest skojarzony z podumową i pozycją podumowy, pole **Typ pracownika** w wierszu członka zespołu ogólnego zostanie zaktualizowane do wartości **Pracownik kontraktowy**, a wartość **Ważność podumowy** zostanie ustawiona na **Ważna**.

## <a name="subcontracting-a-staffed-project-team-member"></a>Podwykonawstwo dla obsadzonego członka zespołu projektu

Podobnie jak ogólni lub niezatwierdzeni członkowie zespołu, można również wyświetlać opcje podwykonawstwa dla zatwierdzonego pracownika zespołu projektu, o ile pracownikiem tego zespołu jest pracownik kontraktowy. Aby przejrzeć i wybrać dostępne opcje podwykonawstwa dla zatwierdzonego lub nazwanego członka zespołu projektu, wykonaj następujące kroki:

1. Wybierz co najmniej jeden rekord członka zespołu projektu, w którym zasób jest nazwanym pracownikiem kontraktowym.
2. Upewnij się, że żaden wybrany rekord członków zespołu projektu nie jest już podwykonawcą. 
3. Wybierz pozycję **Opcje podwyonawstwa** w siatce podrzędnej członków zespołu projektu. Otworzy się okno dialogowe **Opcje podwykonawstwa**. 
4. Jeśli w kroku 1 wybrano tylko jeden rekord członka zespołu projektu, dostępne będą następujące opcje:
      - Tworzenie nowych pozycji podumowy.
      - Rezerwowanie względem istniejącej podumowy.
  Jeśli w kroku 1 wybrano wiele rekordów członków zespołu projektu, jedyną dostępną opcją jest utworzenie nowych pozycji podumowy.
5. Opcja rezerwacji względem istniejącej pozycji podumowy umożliwia wybranie podumowy i pozycji podumowy, względem której odbędzie się rezerwacja. Wybierając pozycję podumowy w celu zarezerwowania dyspozycyjności, należy się upewnić, że:
      - Wybrana pozycja podumowy dotyczy czasu. 
      - Rola wymagana dla członka zespołu projektu odpowiada roli, która została zakupiona w pozycji podumowy. 
      - Dostawca, z który jest skojarzony pracownik kontraktowe, jest tym samym dostawcą w przypadku podumowy.
6. Po wybraniu opcji utworzenia nowych pozycji podumowy dla członków zespołu projektu system umożliwi wybranie podumowy, która ma utworzyć te wiersze. W przypadku tej opcji należy upewnić się, że dostawca, do którego należy pracownik kontraktowy jest tym samym dostawcą w przypadku podumowy. 
7. Podumowa, którą użytkownik wybierze w celu utworzenia nowych wierszy, powinna mieć stan **Wersja robocza**. Po wybraniu tej opcji w celu utworzenia nowych pozycji podumowy dla wybranych członków zespołu projektu system utworzy po jednej pozycji podumowy dla każdego członka zespołu projektu. Rola, godziny i daty zostaną skopiowane z członka zespołu projektu do każdej tworzonej pozycji podumowy.  
8. Gdy nazwany członek zespołu jest skojarzony z podumową i pozycją podumowy, pole **Typ pracownika** w wierszu nazwanego członka zespołu zostanie zaktualizowane do wartości **Pracownik kontraktowy**, a wartość **Ważność podumowy** zostanie ustawiona na **Ważna**.

## <a name="re-costing-subcontractor-assignments"></a>Ponowna wycena przypisań podwykonawców

Jeśli członek zespołu projektu (ogólny lub nazwany) zostanie połączony z pozycjami podumowy w sesji dialogowej **Opcje podwykonawstwa**, wszelkie przypisania do zadań członka zespołu zostaną ponownie wycenione na podstawie cennika zakupu dołączonego do podumowy. Na karcie **Szacowania** na stronie **Szczegóły projektu** wybierz przycisk **Aktualizuj ceny**, aby wyświetlić zaktualizowane ceny i/lub wycenę kosztów wynikających z podjęcia decyzji o zleceniu podwykonawcy.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]