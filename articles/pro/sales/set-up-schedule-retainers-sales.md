---
title: Konfigurowanie harmonogramu honorariów — wersja uproszczona
description: Ten temat zawiera informacje o tym, jak skonfigurować harmonogram honorariów w Project Operations.
author: rumant
manager: Annbe
ms.date: 10/22/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 5e0312b89d9969f140146b6aaaa9bdcfde702c0b
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/31/2020
ms.locfileid: "4181285"
---
# <a name="set-up-a-retainer-schedule---lite"></a>Konfigurowanie harmonogramu honorariów — wersja uproszczona

_**Zastosowane w:** Wdrażanie uproszczone — od okazji do faktury pro forma_

Harmonogramy honorariów są ustawiane na stronie **Kontrakt projektu** w Dynamics 365 Project Operations.

1. Na stronie **Kontrakt projektu** na karcie **Zatrzymania i zaliczki** wybierz opcję **Konfigurowanie harmonogramu honorariów**.
2. Na stronie dialogu, który zostanie otwarty, zostaną wyświetlone pola wymienione w poniższej tabeli. Tabela zawiera informacje na temat wpływu wprowadzonych wartości lub na harmonogram, który zostanie utworzony.

| Pole | Opis | Wpływ zmian w dalszych etapach |
| --- | --- | --- |
| Klient kontraktu projektu | Klient w umowie, któremu zostanie wystawiona faktura za to honorarium lub zaliczkę. | Jeśli masz wielu klientów na umowie i musisz zafakturować każdego z nich na określoną kwotę honorarium lub zaliczki, ręcznie utwórz jedną fakturę dla każdego klienta. |
| Harmonogram zatrzymania (początek) | Wprowadź datę rozpoczęcia harmonogramu honorariów. | Data ta może nie być datą utworzenia pierwszego honorarium lub zaliczki. W dniu utworzenia pierwszego honorarium lub zaliczki jest również uzależnione od częstotliwości faktur. |
| Harmonogram zatrzymania – koniec | Wprowadź datę zakończenia harmonogramu honorariów. | Data ta może nie być datą utworzenia ostatniego honorarium lub zaliczki. W dniu utworzenia ostatniego honorarium lub zaliczki jest również uzależnione od częstotliwości faktur. |
| Liczba elementów zatrzymania do utworzenia | Kiedy wprowadzana jest liczba honorariów do utworzenia, system używa daty i częstotliwości rozpoczęcia do utworzenia numeru w tym polu. | Jeśli pole jest aktualizowane ręcznie, system zignoruje wartość w polu **Koniec harmonogramu honorarium** i utworzy określoną liczbę zatrzymań lub zaliczek. |
| Częstotliwość faktur | Jak często aplikacja będzie tworzyć honoraria i zaliczki. | Wartość ta ma bezpośredni wpływ na liczbę honorariów i zaliczek oraz daty utworzenia. |
| Łączna kwota | Łączna kwota to kwota, która jest podzielona na poszczególne honoraria lub zaliczki, które zostaną utworzone. | W tym polu nie ma wpływu zmian na dalsze etapy. |