---
title: Obsadzanie projektu na podstawie dyspozycyjności pracowników kontraktowych i podwykonawców
description: W tym artykule wyjaśniono, w jaki sposób wymagania projektów można spełniać przy użyciu dyspozycyjności pracowników kontraktowych lub podwykonawców w aplikacji Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 8edb053467ef200ca3e051e2fd78106734318389
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261268"
---
# <a name="staffing-a-project-with-contract-workers-and-subcontracted-capacity"></a>Obsadzanie projektu na podstawie dyspozycyjności pracowników kontraktowych i podwykonawców

_**Zastosowane w:** Wdrażanie uproszczone — od okazji do faktury pro forma_

Ogólni członkowi zespołu projektu mogą być obsadzani przez pracowników lub pracowników kontraktowych. Podczas obsadzania projektu pracownikami kontraktowymi można ograniczyć opcje obsadzania do określonych pracowników kontraktowych przypisanych do pozycji podumowy. 

## <a name="search-for-staff-resource-requirements-with-contract-workers-that-belong-to-a-specific-subcontract-line"></a>Wyszukiwanie wymagań dotyczących obsadzania zasobów pracownikami kontraktowymi należącymi do określonej pozycji podumowy

Aby wyszukać i obsadzić wymagania dotyczące obsadzania zasobów pracownikami kontraktowymi należącymi do określonej pozycji podumowy, wykonaj następujące kroki:

1. Utwórz członka ogólnego zespołu projektu odwołującego się do podumowy i pozycji podumowy.
2. Wygeneruj wymaganie dotyczące zasobu dla tego członka ogólnego zespołu projektu, używając przycisku **Generuj wymaganie** w siatce podrzędnej członków zespołu projektu.
3. Zaznacz wiersz członka zespołu, a następnie wybierz przycisk **Zarezerwuj** w siatce podrzędnej. 
4. Spowoduje to otwarcie tablicy harmonogramu z kontekstem wymagań. Oprócz innych atrybutów, takich jak pola dat, roli i jednostek organizacyjnych, filtry tablicy harmonogramu są również automatycznie wypełniane polami wiersza dostawcy, podumowy i pozycji podumowy z wymagania dotyczącego zasobu.
5. System wyszukuje zasoby spełniające kryteria filtrowania i wyświetla je. 
6. Wybierz jeden z filtrowanych zasobów i zarezerwuj zasób na potrzeby wymagania. 
7. Członek zespołu projektu zostanie utworzony, a następnie zaktualizowany przy użyciu odwołań do podumowy i pozycji podumowy. Przejdź do opcji **Szacowania projektu** i wybierz opcję **Aktualizuj ceny**, aby zobaczyć zaktualizowany koszt przypisania zasobów. 

> [!NOTE]
> Aktualizacja członka zespołu projektu przy użyciu odwołania do podumowy i pozycji podumowy może być nie zawsze możliwa podczas rezerwacji, jeśli zasób zostanie przypisany do wielu pozycji podumowy. Jeśli system nie może zaktualizować członka zespołu projektu przy użyciu podumowy i pozycji podumowy, otwórz rekord członka zespołu projektowego i ręcznie zaktualizuj te pola, aby szacowanie kosztu finansowego dokładnie odzwierciedlało koszt podwykonawcy.

## <a name="search-for-and-staff-resource-requirements-with-any-contract-worker"></a>Wyszukiwanie wymagań dotyczących zasobów i obsadzanie ich przy użyciu dowolnego pracownika kontraktowego

Aby wyszukać wymagania dotyczące zasobów i obsadzić je przy użyciu dowolnego pracownika kontraktowego, wykonaj następujące kroki:

1. Utwórz ogólnego członka zespołu projektu.
2. Wygeneruj wymaganie dotyczące zasobu dla tego członka ogólnego zespołu projektu, używając przycisku **Generuj wymaganie** w siatce podrzędnej członków zespołu projektu.
3. Zaznacz wiersz członka zespołu, a następnie wybierz przycisk **Zarezerwuj** w siatce podrzędnej. 
4. Spowoduje to otwarcie tablicy harmonogramu z kontekstem wymagań. Oprócz innych atrybutów, takich jak pola dat, roli i jednostek organizacyjnych, filtry tablicy harmonogramu są również automatycznie wypełniane polami wiersza dostawcy, podumowy i pozycji podumowy z wymagania dotyczącego zasobu. Ponieważ wymaganie nie miało wypełnionych wartości podumowy lub pozycji podumowy, atrybuty te będą puste w okienku filtru.
5. System wyszukuje zasoby spełniające kryteria filtrowania i wyświetla je.
6. Zaktualizuj pole **Typ pracownika** w okienku filtru na **Pracownik kontraktowy**, aby ograniczyć wyszukiwanie do pracowników kontraktowych. Zaktualizuj **dostawcę** w okienku filtrów, aby wybrać dostawcę w celu ograniczenia wyszukiwania tylko do pracowników kontraktowych należących do określonej firmy dostawcy.
7. Wybierz z listy pracownika kontraktowego i zarezerwuj zasób na potrzeby wymagania.
8. Członek zespołu projektu został utworzony. Jednak członek zespołu projektu nie jest aktualizowany przy użyciu podumowy lub pozycji podumowy, i w związku z tym przypisanie zasobów nie będzie wyceniane przy użyciu kalkulacji cen podumowy. Ręcznie zaktualizuj członka zespołu projektu przy użyciu pozycji podumowy, przejdź do obszaru **Szacowania projektu** i wybierz opcję **Aktualizuj ceny**, aby wyświetlić zaktualizowany koszt przypisania zasobów.

> [!NOTE]
> Członkowie zespołu projektu, którzy mają **Typ pracownika** ustawiony na **Pracownik kontraktowy**, ale nie mają odwołania podumowy, są oznaczani jako **Nieprawidłowy** w siatce **Członkowie zespołu projektowego**. Jeśli któryś z członków zespołu projektowego ma ten stan, otwórz rekord członka zespołu projektowego i ręcznie zaktualizuj pola podumowy i wiersza podumowy, aby szacowanie kosztu finansowego dokładnie odzwierciedlało koszt podwykonawcy na karcie **Szacowania**. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
