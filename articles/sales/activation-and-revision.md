---
title: Aktywowanie i poprawianie oferty projektu
description: W tym artykule podano informacje na temat aktywowania i poprawiania ofert w aplikacji Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 09/01/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: e71102078832ac7d5f8e5edb40cc484df927eda4
ms.sourcegitcommit: 16c9eded66d60d4c654872ff5a0267cccae9ef0e
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 09/07/2022
ms.locfileid: "9410352"
---
# <a name="activate-and-revise-a-project-quote"></a>Aktywowanie i poprawianie oferty projektu

_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_

Funkcje aktywacji i poprawek ułatwiają śledzenie wersji ofert opartych na projektach na etapach szacowania i negocjacji. Po aktywowaniu wersji roboczej oferty staje się ona dostępna tylko do odczytu.

Funkcje aktywacji i poprawek umożliwiają wykonywanie następujących czynności:

- Oferty można wykorzystaną lub utracić tylko po aktywowaniu.
- Poprawianie oferty, aby wprowadzić zmiany w istniejącej ofercie lub utworzyć nową wersję.

> [!NOTE]
> Po włączeniu funkcji aktywacji i poprawek ofert nie można jej wyłączyć.

Aby włączyć możliwość aktywowania i poprawiania ofert opartych na projektach, wykonaj następujące kroki.

1. Przejdź do pozycji **Ustawienia** \> **Parametry**.
1. Otwórz rekord **Parametry**.
1. W okienku Akcje na karcie **Kontrola funkcji** wybierz opcję **Włącz aktywację i poprawki ofert**.
1. W oknie dialogowym z monitem o potwierdzenie wybierz **OK**.
1. Po kilku chwilach odśwież przeglądarkę. Funkcje aktywacji i poprawek powinny być teraz dostępne. Zobaczysz, że te funkcje zostały włączone, jeśli przycisk **Włącz aktywację i poprawki ofert** nie jest już wyświetlany w okienku akcji.

## <a name="activating-a-quote"></a>Aktywowanie oferty

Po włączeniu funkcji aktywacji i poprawki ofert przyciski **Zamknij ofertę jako wykorzystaną** i **Zamknij ofertę jako utraconą** w okienku akcji nie są dostępne dla ofert projektu w wersji roboczej. Są one dostępne dopiero po aktywowaniu oferty.

Aktywacja reprezentuje etap procesu oferty, kiedy użytkownik chce zapobiec większej liczbie zmian w ofercie. Na tym etapie oferta jest wysyłana do wewnętrznej recenzji lub do klienta.

Przyciski **Zamknij ofertę jako wykorzystaną** i **Zamknij ofertę jako utraconą** są dostępne dla aktywowanych ofert. W zależności od wyników recenzji wewnętrznego lub przeprowadzonej przez klienta można użyć jednego z tych przycisków w celu zamknięcia aktywowanej oferty. Po wybraniu opcji **Popraw ofertę** można dokonać negocjacji i zmian w aktywowanych ofertach.

## <a name="revising-a-quote"></a>Poprawianie oferty

Jeśli musisz wprowadzić zmiany aktywowanej oferty, wybierz opcję **Popraw ofertę**. Oferta zostanie zamknięta i zostanie użyty kod przyczyny **poprawiono**. Tworzona jest nowa oferta o tym samym identyfikatorze i zwiększonym numerze poprawki. Wszystkie informacje z oryginalnej oferty są kopiowane do nowej oferty. Nowa oferta ma stan wersji roboczej i można ją edytować w razie potrzeby.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
