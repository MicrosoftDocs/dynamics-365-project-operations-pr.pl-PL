---
title: Zarządzanie szansami sprzedaży projektu
description: W tym artykule przedstawiono informacje na temat pracy z szansami sprzedaży powiązanymi z projektami.
author: rumant
ms.date: 10/21/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 56eba38476dd5b49f0043eee5d411d51f9bf56b8
ms.sourcegitcommit: e0cbbe7c6f03d4978134405cf04bd8bc1d019f65
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/05/2022
ms.locfileid: "9825345"
---
# <a name="manage-project-opportunities"></a>Zarządzanie szansami sprzedaży projektu

_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_

Przedsiębiorstwa oparte na projektach zwykle mają swoje działania w wielu krajach i lokalizacjach. Koszty wykonania i dostawy projektu mogą się różnić zależnie od tego, gdzie projekt jest wykonywany, i który oddział się nim zajmuje. Może to wpłynąć na marże transakcji. Dostarczanie usług opartych na projektach zwykle polega na dużym poziomie zasobów ludzkich, znaczących kosztach podróży, kosztach materiałowych i innych kosztach.

Możliwości oparte na projekcie w rozwiązaniu Dynamics 365 Project Operations są zaprojektowane z rozszerzeniami do systemu Dynamics 365 Sales. W artykule przedstawiono szczegółowe informacje na temat różnych pól i logiki biznesowej, które są dostępne w ramach dodatkowych funkcji wymaganych przez firmy korzystające z projektów w celu zarządzania szansami sprzedaży opartymi na projektach.

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
