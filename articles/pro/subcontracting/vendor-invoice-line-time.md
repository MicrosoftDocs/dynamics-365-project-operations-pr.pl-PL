---
title: Wiersze faktury dostawcy na czas
description: W temat tym temat jest wyjaśnione, jak zarejestrować wiersze faktur dostawcy na koszty czasu wprowadzone przez podwykonawców.
author: rumant
ms.date: 03/15/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: ac598dff7b0b4a29ac0397a31130ada3b197fe44
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/14/2022
ms.locfileid: "8597213"
---
# <a name="vendor-invoice-lines-for-time"></a>Wiersze faktury dostawcy na czas

[!include [banner](../../includes/dataverse-preview.md)]

_**Zastosowane w:** Wdrażanie uproszczone — od okazji do faktury pro forma_

Faktura dostawcy w Microsoft Dynamics 365 Project Operations może mieć czas w wierszach faktur dostawcy. Menedżerowie projektów mogą używać wierszy faktur dostawcy w czasie do rekordu kosztów czasu podwykonawców w projektach.

Wiersze faktury dostawcy dotyczące czasu mogą lub nie odwoływać się do wiersza kontraktu podrzędnego. Jeśli wiersz faktury od dostawcy dla czasu odwołuje się do umowy podwykonawczej, kierownicy projektów będą mogli dopasować i zweryfikować czas fakturowany w wierszu faktury od dostawcy z czasem zarejestrowanym przez podwykonawców i zatwierdzonym przez kierowników projektów w projekcie.

Poniższa tabela zawiera informacje o polach w wierszach faktury dostawcy dla czasu.

| Pole | Description | Wpływ funkcjonalny |
| --- | --- | --- |
| Imię i nazwisko/nazwa | Nazwa wiersza faktury dostawcy w celu pomocy w identyfikacji. | Ta nazwa będzie wyświetlana jako pierwsza kolumna we wszystkich wyszukiwaniach opartych na wierszach faktury dostawcy. |
| Description | Krótki opis usług zafakturowany przez dostawcę w wierszu faktury dostawcy. | None |
| Podumowa | Umowa podwykonawcza, w ramach której usługi zostały pierwotnie zlecone. | Jeśli dla faktury dostawcy zostanie wybrany kontrakt podrzędny, wszystkie wiersze na fakturze dostawcy dziedziczą ten wybór. Na fakturze dostawcy nie mogą być faktury od dostawcy, które odwołują się do różnych kontraktów podrzędnych. |
| Wiersz podumowy | Linia podwykonawcza, na której zlecono usługi. Lista wierszy kontraktu podrzędnego, które można wybrać, jest ograniczona do wierszy na wybranym podwykonawcy. | Po wybraniu wiersza kontraktu podrzędnego w wierszu faktury dostawcy na czas wartości domyślne pól Zasobów **Projekt**, **Rola** i **Rezerwacja** są wprowadzane z odpowiednich pól w wierszu kontraktu podrzędnego. Jeśli wybrany wiersz kontraktu podrzędnego ma wartości w polach **Projekt**, **Rola** i **Zarezerwowany**, wartości odpowiednich pól w wierszu faktury dostawcy nie mogą się różnić od tych wartości. |
| Data transakcji | Data, w dniu, w którym koszt rzeczywisty wiersza faktury dostawcy będzie rejestrowany w projekcie. | None |
| Klasa transakcji | Wartość domyślna to **Czas**. | Wartość Godzina **wskazuje**, że wiersz faktury dostawcy jest używany do rejestrowanie kwoty czasu podwykonawcy na fakturze. |
| Project | Nazwa projektu, dla którego zostały użyte usługi, które są fakturowane. | To pole jest wymagane i nie może być puste. |
| Zadanie | Nazwa zadania projektu, dla którego zostały użyte usługi, które są fakturowane. To pole jest dostępne tylko po wybraniu projektu. Wybór zadania projektowego jest opcjonalny. | Jeśli to pole pozostanie puste, kierownik projektu może dopasować wiersz faktury od dostawcy do czasu zarejestrowanego przez zasoby podwykonawcy w dowolnym zadaniu projektu. Jeśli wiersz faktury od dostawcy nie odwołuje się do wiersza umowy podwykonawstwa, a to pole pozostanie puste, rzeczywisty koszt utworzony przez wiersz faktury od dostawcy nie zostanie połączony z żadnymi nierozliczonymi wartościami rzeczywistymi sprzedaży. W takim przypadku, jeśli skonfigurowano rozliczanie oparte na zadaniach, koszty mogą nie być możliwe do zafakturowania na klienta końcowego. |
| Rola | Rola zasobów zleconych podwykonawcom, których czas jest fakturowany. | To pole określa rolę, która jest wykonywana przez zasoby podwykonawcy, których czas jest zafakturowany na fakturze dostawcy. |
| Zasób, który można zarezerwować | Nazwa podwykonawcy, którego czas jest fakturowany. Wybór zasobu, który można zarezerwować, jest opcjonalny. | Jeśli to pole pozostanie puste, kierownik projektu może dopasować wiersz faktury od dostawcy do czasu zarejestrowanego przez dowolny zasób należący do dostawcy w wierszu faktury od dostawcy. |
| Ilość | Wprowadź liczbę godzin czasu, które są fakturowane przez dostawcę w wierszu faktury. |None |
| Grupa jednostek | Wartość domyślna to **Grupa jednostek czasu** i nie można jej zmieniać. | None |
| Jednostka | Wartość domyślna to podstawowa jednostka godzin z grupy jednostek czasu. Możesz zmienić tę wartość, aby kupić dowolną jednostkę z grupy jednostek czasu, taką jak dzień lub tydzień. | Kombinacja wartości **rola** i **jednostka** będzie używana jako wartość domyślna lub obliczona w polu **Cena jednostkowa** w wierszu faktury dostawcy. |
| Cena jednostkowa | Domyślna cena jednostkowa wykorzystuje kombinację wartości **Rola** i **Jednostki** z cennika projektu, który ma zastosowanie do daty transakcji w wierszu faktury od dostawcy. | Jeśli cena dla odpowiedniego cennika projektu jest ustawiona w jednostce różniącej się od jednostki w wierszu faktury dostawcy, system używa konwersji jednostek do obliczenia ceny za jednostkę. |
| Suma częściowa | To pole tylko do odczytu jest obliczane jako *Ilość* &times; *Cena jednostkowa*, jeśli wartości są wprowadzone zarówno w polu **Ilość**, jak i **Cena jednostkowa**. Jeśli jedno lub oba te pola są puste, możesz wprowadzić w tym polu wartość. | None |
| Podatek | Wprowadź kwotę podatku. | None |
| Łączna kwota | Łączna kwota wiersza faktury dostawcy, w tym podatków. To pole jest obliczane jako *Suma częściowa* + *Podatek*. | None |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
