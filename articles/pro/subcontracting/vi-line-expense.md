---
title: Wiersze faktury dostawcy dla kategorii wydatków
description: W tym artykule wyjaśniono sposób rejestrowania wierszy faktur od dostawcy dla kategorii wydatków.
author: rumant
ms.date: 03/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 2c3cd2fab87af1cbfccd81e543f2cea0278978f6
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261713"
---
# <a name="vendor-invoice-lines-for-expense-categories"></a>Wiersze faktury dostawcy dla kategorii wydatków

_**Zastosowane w:** Wdrażanie uproszczone — od okazji do faktury pro forma_

Faktura dostawcy w Microsoft Dynamics 365 Project Operations może zawierać wiersze faktury od dostawcy dla kategorii wydatków. Menedżerowie projektów mogą używać wierszy faktur dostawcy w kategoriach wydatków w celu rejestrowanie kosztów usług, które są rozliczane jako kategorie wydatków.

Wiersze faktury dostawcy dla kategorii wydatków mogą, ale nie muszą odwoływać się do wiersza umowy podwykonawczej dla kategorii wydatków. Jeśli wiersz faktury od dostawcy dla kategorii wydatków odwołuje się do umowy podwykonawczej, kierownicy projektów będą mogli dopasować i zweryfikować wydatki, które są fakturowane w wierszu faktury od dostawcy z wydatkami, które są rejestrowane w tych kategoriach wydatków i zatwierdzane przez kierowników projektów w projekcie.

Poniższa tabela zawiera informacje o polach w wierszach faktury od dostawcy dla kategorii wydatków.

| Pole | Description | Wpływ funkcjonalny |
| --- | --- | --- |
| Imię i nazwisko/nazwa | Nazwa wiersza faktury dostawcy w celu pomocy w identyfikacji. | Ta nazwa będzie wyświetlana jako pierwsza kolumna we wszystkich wyszukiwaniach opartych na wierszach faktury dostawcy. |
| Description | Krótki opis usług zafakturowany przez dostawcę w wierszu faktury dostawcy. | None |
| Podumowa | Umowa podwykonawcza, w ramach której usługi zostały pierwotnie zlecone. | Jeśli dla faktury dostawcy zostanie wybrany kontrakt podrzędny, wszystkie wiersze na fakturze dostawcy dziedziczą ten wybór. Na fakturze dostawcy nie mogą być faktury od dostawcy, które odwołują się do różnych kontraktów podrzędnych. |
| Wiersz podumowy | Linia podwykonawcza, na której zlecono usługi. Lista wierszy kontraktu podrzędnego, które można wybrać, jest ograniczona do wierszy na wybranym podwykonawcy. | Po wybraniu wiersza podwykonawstwa w wierszu faktury od dostawcy dla kategorii wydatków wartości domyślne pól **Projekt**, **Zadaanie** i **Kategoria transakcji** są wprowadzane z odpowiednich pól w wierszu kontraktu podrzędnego. Jeśli wybrany wiersz kontraktu podrzędnego ma wartości w polach **Projekt**, **Zadanie projrktu** i **Kategoria transakcji**, wartości odpowiednich pól w wierszu faktury dostawcy nie mogą się różnić od tych wartości. |
| Data transakcji | Data, w dniu, w którym koszt rzeczywisty wiersza faktury dostawcy będzie rejestrowany w projekcie. |None |
| Klasa transakcji | Wybierz pozycję **Koszt**, aby zarejestrować fakturę dostawcy dla danej kategorii wydatków. | Wartość **Wydatek** wskazuje, że wiersz faktury od dostawcy jest używany do rejestrowania kwoty faktury za usługi, które zostały nabyte jako kategorie wydatków. |
| Project | Nazwa projektu, dla którego zostały użyte usługi, które są fakturowane. | To pole jest wymagane i nie może być puste. |
| Zadanie | Nazwa zadania projektu, dla którego zostały użyte usługi, które są fakturowane. To pole jest dostępne tylko po wybraniu projektu. Wybór zadania projektowego jest opcjonalny. | Jeśli to pole pozostanie puste, kierownik projektu może dopasować wiersz faktury od dostawcy do wydatków, które są rejestrowane w dowolnym zadaniu projektu. Jeśli wiersz faktury od dostawcy nie odwołuje się do wiersza umowy podwykonawstwa, a to pole pozostanie puste, rzeczywisty koszt utworzony przez wiersz faktury od dostawcy nie zostanie połączony z żadnymi nierozliczonymi wartościami rzeczywistymi sprzedaży. W takim przypadku, jeśli skonfigurowano rozliczanie oparte na zadaniach, koszty mogą nie być możliwe do zafakturowania na klienta końcowego. |
| Kategoria transakcji | Kategoria transakcji, która jest zafakturowana. Dla wybranej kategorii transakcji należy utworzyć odpowiednią kategorię wydatków. | Kombinacja wartości **Kategoria transakcji** i **jednostka** będzie używana jako wartość domyślna lub obliczona w polu **Cena jednostkowa** w wierszu faktury dostawcy. |
| Ilość | Wprowadź ilość zafakturowana przez dostawcę w tym wierszu faktury. |None|
| Grupa jednostek | Wartość domyślna jest wprowadzana na podstawie grupy jednostek wybranej kategorii transakcji. | None |
| Jednostka | Wartość domyślna to jednostka podstawowa wybranej grupy jednostek. Możesz zmienić tę wartość, aby kupić dowolną jednostkę z grupy jednostek. | Kombinacja wartości **Kategoria transakcji** i **jednostka** będzie używana jako wartość domyślna lub obliczona w polu **Cena jednostkowa** w wierszu faktury dostawcy. |
| Cena jednostkowa | Domyślna cena jednostkowa wykorzystuje kombinację wartości **Kategoria transakcji** i **Jednostki** z cennika projektu, który ma zastosowanie do daty transakcji w wierszu faktury od dostawcy. | Jeśli cena dla odpowiedniego cennika projektu jest ustawiona w jednostce różniącej się od jednostki w wierszu faktury dostawcy, system używa konwersji jednostek do obliczenia ceny za jednostkę. |
| Suma częściowa | To pole tylko do odczytu jest obliczane jako *Ilość* &times; *Cena jednostkowa*, jeśli wartości są wprowadzone zarówno w polu **Ilość**, jak i **Cena jednostkowa**. Jeśli jedno lub oba te pola są puste, możesz wprowadzić w tym polu wartość.| None |
| Podatek | Wprowadź kwotę podatku. | None |
| Łączna kwota | Łączna kwota wiersza faktury dostawcy, w tym podatków. To pole jest obliczane jako *Suma częściowa* + *Podatek*. | None |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
