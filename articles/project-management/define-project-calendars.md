---
title: Definiowanie kalendarzy projektu
description: Ta temat zawiera informacje na temat korzystania z kalendarza projektu w celu śledzenia jego harmonogramu.
author: ruhercul
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 774399f2c02d8434c9c042c3a9f995792893bfce
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082186"
---
# <a name="define-project-calendars"></a>Definiowanie kalendarzy projektu

_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_

Aby utworzyć harmonogram projektu, należy utworzyć szablon kalendarza projektu, który definiuje liczbę godzin pracy w ciągu dnia i wszystkie dni wolne od pracy. Aby utworzyć szablon kalendarza projektu, należy skojarzyć szablon pracy z polem **Szablon kalendarza** dotyczącym projektu. Aby utworzyć szablon pracy, wykonaj następujące czynności.

1. W lewym okienku nawigacji wybierz **Zasoby**. 
2. Na stronie listy **Zasoby** otwórz rekord użytkownika, a następnie wybierz pozycję **Pokaż godziny pracy**.

  > [!NOTE]
  > Upewnij się, że zezwolono na wyświetlanie wyskakujących okienek na stronie przeglądarki. Dzięki temu będziesz widzieć godzin pracy ustawione dla zasobu.
  
3. Na karcie **Widok miesięczny** wybierz **Konfiguracja**. Zostanie wyświetlona lista z trzema opcjami: 

  - Nowy harmonogram tygodniowy
  - Harmonogram pracy na jeden dzień
  - Czas wolny

4. Zaznacz opcję **Nowy harmonogram tygodniowy** , a następnie ustaw opcje dla tego harmonogramu zasobów. Można określić cykliczny harmonogram tygodniowy, dzienne parametry godzinowe, dni wolne od pracy itd.
5. Ustaw zakres dat, kliknij przycisk **Zapisz** , a następnie wybierz **Zamknij**. 
6. Wróć do strony listy **Zasoby** i wybierz zasób, dla którego ustawiono godziny pracy. 
7. W ustawieniu **Ustaw kalendarz jako** określ szablon pracy. 
8. W oknie dialogowym **Szablon pracy** nadaj nazwę szablonowi pracy, a następnie kliknij przycisk **Zastosuj**. 

Szablon pracy można teraz skojarzyć z szablonem kalendarza projektu.
