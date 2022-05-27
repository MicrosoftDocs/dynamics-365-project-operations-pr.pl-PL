---
title: Konfigurowanie harmonogramu zatrzymania
description: Ten temat zawiera informacje o tym, jak skonfigurować harmonogram honorariów w Project Operations.
author: rumant
ms.date: 10/22/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: b1c48f04aa47d50c9f3ab46031ef0d6cd68619d5
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/14/2022
ms.locfileid: "8574765"
---
# <a name="set-up-a-retainer-schedule"></a>Konfigurowanie harmonogramu zatrzymania

_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_

Harmonogramy zatrzymania są konfigurowane na stronie **Kontrakt projektu** w aplikacji Dynamics 365 Project Operations.

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


[!INCLUDE[footer-include](../../includes/footer-banner.md)]