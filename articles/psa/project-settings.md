---
title: Ustawienia projektu
description: Ten temat zawiera informacje o ustawieniach zarządzania projektami.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: ca5fc63d56ddd84871949e38f421bcdfe38d478e
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/10/2021
ms.locfileid: "5148161"
---
# <a name="project-settings"></a>Ustawienia projektu

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Użyj poniższych ustawień, aby uzyskać dostęp do funkcji planowania projektów.

## <a name="work-template"></a>Szablon pracy

Aby utworzyć harmonogram projektu, należy utworzyć szablon kalendarza projektu, który definiuje liczbę godzin pracy w ciągu dnia i wszystkie dni wolne od pracy. Aby utworzyć szablon kalendarza projektu, należy skojarzyć szablon pracy z polem **Szablon kalendarza** dotyczącym projektu. Aby utworzyć szablon pracy, wykonaj następujące czynności.

1. W programie PSA w lewym okienku nawigacji kliknij pozycję **Zasoby**. 
2. Na stronie listy **Zasoby** otwórz rekord użytkownika, a następnie wybierz pozycję **Pokaż godziny pracy**.

  > [!NOTE]
  > Upewnij się, że zezwolono na wyświetlanie wyskakujących okienek na stronie przeglądarki. Dzięki temu będziesz widzieć godzin pracy ustawione dla zasobu.
  
3. Na karcie **Widok miesięczny** kliknij opcję **Konfiguracja**. Zostanie wyświetlona lista z trzema opcjami: 

  - Nowy harmonogram tygodniowy
  - Harmonogram pracy na jeden dzień
  - Czas wolny

> ![Opcje konfigurowania](media/project-13.png)

4. Zaznacz opcję **Nowy harmonogram tygodniowy**, a następnie ustaw opcje dla tego harmonogramu zasobów. Można określić cykliczny harmonogram tygodniowy, dzienne parametry godzinowe, dni wolne od pracy itd.
5. Ustaw zakres dat, kliknij przycisk **Zapisz**, a następnie kliknij przycisk **Zamknij**. 
6. Wróć do strony listy **Zasoby** i wybierz zasób, dla którego ustawiono godziny pracy. 
7. W ustawieniu **Ustaw kalendarz jako** określ szablon pracy. 
8. W oknie dialogowym **Szablon pracy** nadaj nazwę szablonowi pracy, a następnie kliknij przycisk **Zastosuj**. 

Szablon pracy można teraz skojarzyć z szablonem kalendarza projektu.

## <a name="resource-roles"></a>Role zasobu

Termin *rola zasobu* odnosi się do zestawu umiejętności, kompetencji i certyfikacji koniecznych do wykonania określonego zestawu zadań w projekcie. Program PSA umożliwia określenie kosztów i rozliczenia czasu pracy zasobu na podstawie roli, z którą zasób jest skojarzony. Każda organizacja musi skonfigurować te role, korzystając z lewego okienka nawigacji w menu **Project Service**.

Każda organizacja musi skonfigurować te role na stronie **Aktywne kategorie zasobów**. Aby otworzyć tę stronę, w lewym okienku nawigacji wybierz pozycję **Role zasobów**.

## <a name="price-lists"></a>Cenniki

Cenniki umożliwiają określanie kosztów i cen sprzedaży dla ról zasobów, kategorii wydatków, produktów i innych elementów w organizacji. Przed utworzeniem szacunków finansowych dla prac, które muszą zostać wykonane w projekcie, należy utworzyć zapasową listę kosztów i cennik sprzedaży. W sekcji parametrów należy także skonfigurować domyślną listę kosztów i cennik sprzedaży, które mają zastosowanie do wszystkich projektów tworzonych w organizacji. Na stronie **Aktywne parametry projektu** upewnij się, że skonfigurowano domyślną listę kosztów i cennik sprzedaży.


[!INCLUDE[footer-include](../includes/footer-banner.md)]