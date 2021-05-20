---
title: Zarządzanie szansami sprzedaży opartymi na projektach
description: W tym temacie zamieszczono informacje dotyczące pracy z szansami sprzedaży związanymi z projektami.
author: rumant
manager: Annbe
ms.date: 10/21/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 5ce9ad1458d338d63469c3d6fddb98b9cbbced31
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/27/2021
ms.locfileid: "5948433"
---
# <a name="manage-project-based-opportunities"></a>Zarządzanie szansami sprzedaży opartymi na projektach

_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_

Przedsiębiorstwa oparte na projektach zwykle mają swoje działania w wielu krajach i lokalizacjach. Koszty wykonania i dostawy projektu mogą się różnić zależnie od tego, gdzie projekt jest wykonywany, i który oddział się nim zajmuje. Może to wpłynąć na marże transakcji. Dostarczanie usług opartych na projektach zwykle polega na dużym poziomie zasobów ludzkich, znaczących kosztach podróży, kosztach materiałowych i innych kosztach.

Możliwości oparte na projekcie w rozwiązaniu Dynamics 365 Project Operations są zaprojektowane z rozszerzeniami do systemu Dynamics 365 Sales. Temat zawiera szczegółowe informacje o różnych polach i regułach biznesowych dołączonych do dodatkowych funkcji wymaganych przez firmy oparte na projektach, aby zarządzać szansami sprzedaży opartymi na projektach.

## <a name="view-all-project-based-opportunities"></a>Wyświetlanie wszystkich szans sprzedaży opartych na projektach

Listę wszystkich szans sprzedaży opartych na projektach można zobaczyć na stronie listy **Szansy sprzedaży**. 

1. Wybierz kolejno pozycje **Sprzedaż** > **Szanse sprzedaży**.
2. Użyj **Przełączników widoku**, aby wybrać inne filtrowane widoki szans sprzedaży. Aby skonfigurować te widoki i opcje nawigacji, można utworzyć własne widoki z kryteriami filtrowania niestandardowego.

Szanse sprzedaży projektu mogą być tworzone lub usuwane na stronie listy lub na stronie szczegółów.

## <a name="business-process-flow-for-project-based-deals"></a>Przepływ procesów biznesowych w transakcjach opartych na projektach

Poniższe przepływy procesów biznesowych są obsługiwane w przypadku transakcji opartych na projektach w Project Operations:

- Proces biznesowy Od potencjalnego klienta do szansy sprzedaży
- Proces sprzedaży w ramach szansy sprzedaży

### <a name="lead-to-opportunity-business-process"></a>Proces biznesowy — od potencjalnego klienta do szansy sprzedaży 
Proces biznesowy — od potencjalnego klienta do szansy sprzedaży obsługuje następujące etapy:

| Etap | Mapowana encja | Funkcje |
| --- | --- | --- |
| Kwalifikuj | Potencjalny klient | Kwalifikowanie potencjalnego klienta tworzy konto, kontakt oraz szansę sprzedaży. |
| Opracuj | Szansa sprzedaży | Rozwijanie szansy sprzedaży w celu dodania informacji o związanej pracy, kluczowych udziałowcach i konkurencji. |
| Zaproponuj | Szansa sprzedaży | Opracowanie i uzyskanie zgody zespołu na przegląd wewnętrzny. |
| Zamykanie | Szansa sprzedaży | Wykorzystaj szansę sprzedaży, aby zamknąć ofertę. |

### <a name="opportunity-sales-process"></a>Proces sprzedaży w ramach szansy sprzedaży
Proces sprzedaży szans sprzedaży w Project Operations jest rozszerzeniem przepływu pracy procesu sprzedaży w aplikacji Sales. Ten proces biznesowy został zaprojektowany z myślą o obsłudze poniższych etapów w szansie sprzedaży opartej na projekcie.

| Etap | Mapowana encja | Funkcje |
| --- | --- | --- |
| Kwalifikuj | Szansa sprzedaży | Kwalifikowanie potencjalnego klienta tworzy konto, kontakt oraz szansę sprzedaży. |
| Zaproponuj | Oferta | Opracowanie za pomocą oferty projektu i uzyskanie zgody zespołu na przegląd wewnętrzny. |
| Kontrakt | Kontrakt projektu | Aby utworzyć kontrakt i rozpocząć jego realizację, należy wygrać ofertę. |
| Zamykanie | Kontrakt projektu | Z powodzeniem zakończ pracę i zamknij kontrakt projektu. |

> [!NOTE]
> Jeśli transakcja oparta na projekcie została wyzwolona przez potencjalnego klienta, pierwszeństwo w procesie biznesowym ma proces „Od potencjalnego klienta do szansy sprzedaży”.
>
> Jeśli transakcja oparta na projekcie została wyzwolona przez szansę sprzedaży, pierwszeństwo w procesie biznesowym ma proces „Szansy sprzedaży”.

Użytkownik może edytować przepływ procesów biznesowych produktu lub tworzyć własne przepływy procesów biznesowych umożliwiające śledzenie procesu sprzedaży w zależności od potrzeb. Aby uzyskać więcej informacji na temat przepływu procesów biznesowych, zobacz [Omówienie przepływu procesów biznesowych](/dynamics365/customerengagement/on-premises/customize/business-process-flows-overview).


[!INCLUDE[footer-include](../includes/footer-banner.md)]