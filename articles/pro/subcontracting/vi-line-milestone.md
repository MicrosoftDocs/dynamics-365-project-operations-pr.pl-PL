---
title: Wiersze faktury dostawcy dla punktów kontrolnych
description: W temat wyjaśniono sposób tworzenia wierszy faktur dostawcy dla punktów kontrolnych dla podwykonawcy.
author: rumant
ms.date: 03/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 4fa11e2a4f459016b3ce141b03fe97e55c9a2759
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/14/2022
ms.locfileid: "8590635"
---
# <a name="vendor-invoice-lines-for-milestones"></a>Wiersze faktury dostawcy dla punktów kontrolnych

[!include [banner](../../includes/dataverse-preview.md)]

_**Zastosowane w:** Wdrażanie uproszczone — od okazji do faktury pro forma_

Faktura dostawcy w Microsoft Dynamics 365 Project Operations może mieć wiersze faktur dostawcy dla punktów kontrolnych zdefiniowanych w wierszu kontraktu podrzędnego. Menedżerowie projektów mogą używać wierszy faktur od dostawców w celu punktów kontrolnych w celu rejestrowanie kosztów usług, które są kwalifikowane jako koszty oparte na punktów kontrolnych ponoszonech w przypadku usług lub produktów wymaganych do realizacji projektu.

Wiersze faktur dostawcy dla punktów kontrolnych zawsze muszą odwoływać się do wiersza kontraktu podrzędnego o stałej cenie. Gdy wiersz faktury dostawcy dla kamieni milowych odwołuje się do wiersza umowy podwykonawczej, kierownicy projektu będą mogli dopasować i zweryfikować podstawowe koszty czasu, wydatków lub materiałów, które odwołują się do tego wiersza umowy podwykonawczej z kamieniem milowym fakturowanym przez dostawcę.

Poniższa tabela zawiera informacje o polach w wierszach faktury dostawcy dla kamieni milowych.

| Pole | Description | Wpływ funkcjonalny |
| --- | --- | --- |
| Imię i nazwisko/nazwa | Nazwa wiersza faktury dostawcy w celu pomocy w identyfikacji. | Ta nazwa będzie wyświetlana jako pierwsza kolumna we wszystkich wyszukiwaniach opartych na wierszach faktury dostawcy. |
| Description | Krótki opis usług zafakturowany przez dostawcę w wierszu faktury dostawcy. | None |
| Podumowa | Umowa podwykonawcza, w ramach której usługi zostały pierwotnie zlecone. | Jeśli dla faktury dostawcy zostanie wybrany kontrakt podrzędny, wszystkie wiersze na fakturze dostawcy dziedziczą ten wybór. Na fakturze dostawcy nie mogą być faktury od dostawcy, które odwołują się do różnych kontraktów podrzędnych. |
| Wiersz podumowy | Linia podwykonawcza, na której zlecono usługi. Lista wierszy kontraktu podrzędnego, które można wybrać, jest ograniczona do wierszy na wybranym podwykonawcy. | Po wybraniu wiersza kontraktu podrzędnego w wierszu faktury dostawcy dla punktów kontrolnych pola **Rola** i **Kategoria transakcji** oraz pola związane z produktem są niedostępne i nie są dostępne. Pola **Ilość**, **Jednostka** i **Grupa jednostek** także nie mają znaczenia dla wierszy faktur opartych na punktów kontrolnych dla dostawców. |
| Data transakcji | Data, w dniu, w którym koszt rzeczywisty wiersza faktury dostawcy będzie rejestrowany w projekcie. | None |
| Klasa transakcji | Wybierz **punkt kontrolny**, aby zarejestrować fakturę dostawcy dla zakończonego punktów kontrolnych zdefiniowanych w wierszu podwykonawcy. | None |
| Punkt kontrolny | Wybierz punkt kontrolny zdefiniowany w pokrewnym wierszu kontraktu podrzędnego oznaczonym jako **Gotowy do faktury**. | Punkty kontrolne wiersza podwykonawstwa, które mają stan **Gotowe do wystawienia faktury** można wybrać w wierszu faktury dostawcy. |
| Project | Nazwa projektu, dla którego zostały użyte usługi, które są fakturowane. | To pole jest wymagane i nie może być puste. |
| Zadanie | Nazwa zadania projektu, dla którego zostały użyte usługi, które są fakturowane. To pole jest dostępne tylko po wybraniu projektu. Wybór zadania projektowego jest opcjonalny. | Jeśli to pole nie jest puste, menedżer projektu może dopasować wiersz faktury dostawcy do klasy transakcji w pokrewnym wierszu podwykonawcy zarejestrowanym dla dowolnego zadania projektu. Jeśli wiersz faktury od dostawcy nie odwołuje się do wiersza umowy podwykonawstwa, a to pole pozostanie puste, rzeczywisty koszt utworzony przez wiersz faktury od dostawcy nie zostanie połączony z żadnymi nierozliczonymi wartościami rzeczywistymi sprzedaży. W takim przypadku, jeśli skonfigurowano rozliczanie oparte na zadaniach, koszty mogą nie być możliwe do zafakturowania na klienta końcowego. |
| Kwota punktu kontrolnego | Wprowadź wartość kamienia milowego zdefiniowanego w wierszu umowy podwykonawczej, który jest gotowy do zafakturowania. | None |
| Podatek | Wprowadź kwotę podatku. | None |
| Łączna kwota | Łączna kwota wiersza faktury dostawcy, w tym podatków. To pole jest obliczane jako *Kwota kamienia milowego* + *Podatek od sprzedaży*. | None |

> [!NOTE]
> Po utworzeniu wiersza faktury dostawcy, który odwołuje się do punktu kontrolnego wiersza podrzędnego kontraktu, **stan punktów kontrolnych kontraktu podrzędnego jest aktualizowany do faktury dostawcy utworzonej**. Następnie, po potwierdzeniem faktury dostawcy, stan punktów kontrolnych wiersza kontraktu podrzędnego zostanie **zaktualizowany do faktury dostawcy**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
