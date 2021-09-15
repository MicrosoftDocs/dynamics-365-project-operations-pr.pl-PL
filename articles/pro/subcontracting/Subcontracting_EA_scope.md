---
title: Podwykonawstwo — wydanie z października 2021 r., wczesny dostęp
description: To temat zawiera omówienie możliwości podwykonawstwa w aplikacji Project Operations, które będą częścią wydania z października 2021 r. z wczesnym dostępem.
author: rumant
ms.date: 08/02/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 21ec8355487b5e69fc5b68b11dca029e6dc04f3c
ms.sourcegitcommit: c7f891adb5c81654c01d00c6b39beed403058eb1
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/14/2021
ms.locfileid: "7383708"
---
# <a name="subcontracting-in-october-2021-early-access-release"></a>Podwykonawstwo — wydanie z października 2021 r., wczesny dostęp

[!include [banner](../../includes/dataverse-preview.md)]

_**Zastosowane w:** Wdrażanie uproszczone — od okazji do faktury pro forma_

To temat zawiera omówienie możliwości podwykonawstwa w aplikacji Dynamics 365 Project Operations, które będą częścią wydania z października 2021 r. z wczesnym dostępem. Ten zestaw funkcji nie jest gotowy do środowiska produkcyjnego lub działającego na żywo, więc pozostaje we wczesnym dostępie do czasu wydania pełnego zestawu funkcji. Zdecydowanie zalecamy, aby do momentu usunięcia banera wersji zapoznawczej nie używać funkcji podwykonawstwa ustawionej w scenariuszach produkcyjnych w wersji na żywo. 

Oto lista produktów dostępnych obecnie w wydaniu z października 2021 r. z wczesnym dostępem:

1. Kierownik projektu tworzy umowę podwykonawczą z dostawcą. Domyślnie dla umowy podwykonawczej używane są cenniki dołączone do rekordu dostawcy. Konto dostawcy ma typ relacji **Dostawca** lub **Dostawca (producent)**.

2. Kierownik projektu może wyszczególnić wszystkie zakupy jako pozycje w umowie podwykonawczej. Wiersze podwykonawstwa mogą dotyczyć czasu, wydatków lub produktów. Klasa transakcji w pozycji podumowy określa, do czego służy wiersz.

3. Menedżer klienta dostawcy i kierownik projektu mogą iterować po umowie podwykonawczej. Ceny można dostosować w cennikach zakupu dołączonych do umowy podwykonawczej.

4. Na tym lub późniejszym etapie procesu, jeśli pozycja podumowy dotyczy czasu, kierownik ds. klienta dostawcy kojarzy kontakty dostawcy z każdą pozycją podumowy. To stowarzyszenie dostarcza informacji kierownikowi projektu, który pracuje nad umową podwykonawczą. Gdy kontakt dostawcy jest skojarzony z pozycją podumowy, system automatycznie tworzy zasób, który można zarezerwować, na podstawie kontaktu, jeśli zasób, który można zarezerwować, jeszcze nie istnieje.

5. Metodą rozliczania dla każdego wiersza podwykonawcy może być **Cena stała** lub **Godziny i Materiały**. W przypadku pozycji podumowy o stałej cenie jest konfigurowany harmonogram faktur oparty na kamieniach milowych.

Pozostałe kroki w przepływie procesów biznesowych dotyczące podwykonawstwa opisane w omówieniu są obecnie niedostępne. Po dodaniu nowych funkcji to temat zostanie zaktualizowany. 

Na poniższym rysunku pokazano podwykonawstwo w wydaniu z wczesnym dostępem jako kontrastujące z kompleksowym procesem biznesowym.

![Przepływ procesu podrzędnego](../media/SubcontractingEAFlow.png)  


## <a name="quantity-based-and-work-based-subcontract-lines-early-access-release"></a>Pozycje podumowy oparte na ilości oparte na pracy — wydanie z wczesnym dostępem
W wersji z października 2021 r. z wczesnym dostępem obsługiwane są tylko wiersze podumowy oparte na ilości. Oznacza to, że wiersz podumowy może być używany do zakupu czasu, wydatków lub materiałów od dostawcy, ale nie do zakupu całości pracy. Oznacza to również, że w każdym projekcie w systemie można wykorzystać ilość zakupioną (jednostki czasu, koszty lub ilość materiałów) w wierszu podumowy.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
