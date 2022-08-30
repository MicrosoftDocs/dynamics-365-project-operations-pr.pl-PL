---
title: Wiersze faktury dostawcy dla produktów
description: W tym artykule wyjaśniono, jak rejestrować wiersze faktur dostawcy dla produktów i używać różnych pól do rekordów zakupów produktów od dostawców.
author: rumant
ms.date: 03/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: d38a447c576c095a7bbe2f5ed84342a88bf69a9b
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261572"
---
# <a name="vendor-invoice-lines-for-products"></a>Wiersze faktury dostawcy dla produktów

_**Zastosowane w:** Wdrażanie uproszczone — od okazji do faktury pro forma_

Na fakturze dostawcy w Microsoft Dynamics 365 Project Operations mogą się znaleźć wiersze faktur dla produktów (nazywane również materiałami). Menedżerowie projektów mogą używać wierszy faktur od dostawców dla produktów do rejestrowania kosztów produktów, które zostały zakupione w projektach.

Wiersze faktury dostawcy dla produktów mogą, ale nie muszą odwoływać się do wiersza umowy podwykonawstwa dla materiałów. Jeśli wiersz faktury od dostawcy dla produktów odwołuje się do umowy podwykonawstwa, kierownicy projektów będą mogli dopasować i zweryfikować produkty, które są fakturowane w wierszu faktury od dostawcy, z użyciem zakupionych produktów, które są rejestrowane i zatwierdzane przez kierowników projektów.

Poniższa tabela zawiera informacje o polach w wierszach faktur od dostawców dla produktów.

| Pole | Description | Wpływ funkcjonalny |
| --- | --- | --- |
| Imię i nazwisko/nazwa | Nazwa wiersza faktury dostawcy w celu pomocy w identyfikacji. | Ta nazwa będzie wyświetlana jako pierwsza kolumna we wszystkich wyszukiwaniach opartych na wierszach faktury dostawcy. |
| Description | Krótki opis produktów, które są fakturowane przez dostawcę w wierszu faktury od dostawcy. | None |
| Podumowa | Podwykonawca, na podstawie którego produkty były pierwotnie zamówione. | Jeśli dla faktury dostawcy zostanie wybrany kontrakt podrzędny, wszystkie wiersze na fakturze dostawcy dziedziczą ten wybór. Na fakturze dostawcy nie mogą być faktury od dostawcy, które odwołują się do różnych kontraktów podrzędnych. |
| Wiersz podumowy | Linia podwykonawcza, na której zostały zamówione produkty. Lista wierszy kontraktu podrzędnego, które można wybrać, jest ograniczona do wierszy na wybranym podwykonawcy. | Po wybraniu wiersza kontraktu podrzędnego w wierszu faktury dostawcy na produkty wartości domyślne pól Zasobów **Projekt**, **Zadanie** i **Produkt** są wprowadzane z odpowiednich pól w wierszu kontraktu podrzędnego. Jeśli wybrany wiersz kontraktu podrzędnego ma wartości w polach **Projekt**, **Zadanie** i **Produkt**, wartości odpowiednich pól w wierszu faktury dostawcy nie mogą się różnić od tych wartości. |
| Data transakcji | Data, w dniu, w którym koszt rzeczywisty wiersza faktury dostawcy będzie rejestrowany w projekcie. | None|
| Klasa transakcji | Podczas fakturowania produktów w tym polu należy ustawić wartość **Materiał**. | Wartość **Materiał** wskazuje, że wiersz faktury od dostawcy jest używany do rejestrowania kwoty faktury za zakupione materiały. |
| Project | Nazwa projektu, na podstawie który zostały użyte zafakturowane produkty. | To pole jest wymagane i nie może być puste. |
| Zadanie | Nazwa zadania projektowego, dla którego zostały użyte produkty, które są fakturowane. To pole jest dostępne tylko po wybraniu projektu. Wybór zadania projektowego jest opcjonalny. | Jeśli to pole pozostanie puste, kierownik projektu może dopasować wiersz faktury od dostawcy do zakupionego produktu, który jest używany w dowolnym zadaniu projektu. Jeśli wiersz faktury od dostawcy nie odwołuje się do wiersza umowy podwykonawstwa, a to pole pozostanie puste, rzeczywisty koszt utworzony przez wiersz faktury od dostawcy nie zostanie połączony z żadnymi nierozliczonymi wartościami rzeczywistymi sprzedaży. W takim przypadku skonfigurowanie rozliczania opartego na zadaniach nie spowoduje, że klientowi końcoweowi nie będzie można zafakturować kosztów. |
| Wybierz produkt | Wybierz, czy produkt, który jest fakturowany, jest produktem istniejącym z katalogu, czy produktem dopisanym. | Wartość domyślna jest wprowadzana z wiersza kontraktu podrzędnego po wybraniu wiersza podwykonawcy. |
| Produkt | Wybierz produkt z katalogu. Jeśli produkt jest produktem do wpisania, wprowadź nazwę produktu. | To pole służy do wprowadzania domyślnych cen zakupu istniejących produktów. |
| Ilość | Wprowadź ilość materiałów zafakturowany przez dostawcę w tym wierszu faktury. | None |
| Grupa jednostek | Wybierz grupę jednostek dla jednostki, w których wyrażana jest ilość w fakturze. | None |
| Jednostka | Wartość domyślna to jednostka podstawowa wybranej grupy jednostek. Tę wartość można zmienić, aby płaciła dowolna jednostka z wybranej grupy jednostek. | Kombinacja wartości **Produkt** i **jednostka** będzie używana jako wartość domyślna lub obliczona w polu **Cena jednostkowa** w wierszu faktury dostawcy. |
| Cena jednostkowa | Domyślna cena jednostkowa wykorzystuje kombinację wartości **Produkt** i **Jednostki** z cennika projektu, który ma zastosowanie do daty transakcji w wierszu faktury od dostawcy. | None |
| Suma częściowa | To pole tylko do odczytu jest obliczane jako *Ilość* &times; *Cena jednostkowa*, jeśli wartości są wprowadzone zarówno w polu **Ilość**, jak i **Cena jednostkowa**. Jeśli jedno lub oba te pola są puste, możesz wprowadzić w tym polu wartość. | None |
| Podatek | Wprowadź kwotę podatku. | None |
| Łączna kwota | Łączna kwota wiersza faktury dostawcy, w tym podatków. To pole jest obliczane jako *Suma częściowa* + *Podatek*. | None |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
