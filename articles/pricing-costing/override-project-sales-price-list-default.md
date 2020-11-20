---
title: Zastępowanie cenników sprzedaży projektu
description: Ten temat zawiera informacje na temat tworzenia niestandardowych cenników sprzedaży.
author: rumant
manager: Annbe
ms.date: 10/22/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: c97dca8685c2db7d256017cf4442416feb0e005b
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/28/2020
ms.locfileid: "4130861"
---
# <a name="override-project-sales-price-lists"></a>Zastępowanie cenników sprzedaży projektu

_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_

## <a name="customer-specific-project-price-lists"></a>Cenniki projektów dostosowane do potrzeb klienta

Umowy cenowe specyficzne dla klienta można skonfigurować jako cenniki projektu w rekordzie konta w Dynamics 365 Project Operations.

W celu skonfigurowania cennika projektu specyficznego dla klienta w obszarze **Sprzedaż** przejdź do rekordu klienta.

1. Otwórz stronę listy **Konta**.
2. Znajdź i kliknij dwukrotnie rekord klienta, aby otworzyć stronę szczegóły **Konta**.
3. Na karcie **Cenniki projektów** wybierz **+ Nowy cennik projektu^^.
4. Na stronie **Nowy cennik projektu** wybierz cennik z listy rozwijanej. Uwzględnione zostaną tylko te cenniki, dla których ustawiono wartość **Sprzedaż** i z której walutą jest zgodna waluta klienta.
5. Nazwij powiązanie, a następnie wybierz **Zapisz**. Tworzony jest cennik projektu dla klienta. Ten cennik będzie używany do domyślnych cen projektu w ofertach projektu lub umowach utworzonych dla tego klienta, jeśli data utworzenia oferty lub umowy dotyczącej projektu przypada w okresie obowiązywania cennika.

## <a name="custom-pricing-on-project-quotes"></a>Niestandardowa kalkulacja cen w ofertach projektu

Na ofertach w ramach projektu można mieć cenę, która zaczyna się od domyślnego cennika standardowego, który jest wybierany domyślnie z klienta lub z parametrów projektu.

Kiedy potrzebna jest cena niestandardowa w odniesieniu do prac związanych z projektem dla określonej oferty, można ją uzyskać z poziomu encji skojarzonych z cennikami projektu.

Wykonaj następujące kroki, aby skonfigurować konkretne oferty dotyczące kalkulacji cen w projekcie.

1. Otwórz ofertę projektu i wybierz kartę **Cenniki projektów**.
2. W podsiatce wybierz **Utwórz niestandardowy cennik**.

Wszystkie cenniki projektu dołączone do oferty zostaną skopiowane na nowe cenniki. Nazwy nowych cenników odzwierciedlają nazwę oferty zawierającą sygnaturę Data/godzina, dla której utworzono te cenniki.

Można użyć poszczególnych cenników i wprowadzić zmiany dotyczące robocizny (cena roli) i koszty (cena kategorii). Ceny te będą miały zastosowanie tylko do tej wyceny projektu.

## <a name="price-lists-on-a-project-contract"></a>Cenniki na umowie projektowej

W kontrakcie projektu cena projektu zawsze jest domyślnie ustawiona jako cennik niestandardowy z nazwą kontraktu i sygnaturą czasową utworzenia dołączaną do nazwy. Jest to prawdą, czy kontrakt został utworzony w czasie, gdy oferta została wykorzystana lub kiedy kontrakt został utworzony od podstaw. Jeśli jest to konieczne, można usunąć to skojarzenie z cennika niestandardowego i zamiast niego skojarzyć cennik standardowy z kontraktem dotyczącym projektu.

Po skojarzeniu standardowego cennika z cennikami dotyczącymi oferty lub kontraktu wszelkie zmiany cen w cenniku będą miały wpływ na wszystkie oferty i kontrakty, w których jest używany cennik.
