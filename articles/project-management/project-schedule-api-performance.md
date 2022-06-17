---
title: Wydajność interfejsu API harmonogramu projektu
description: Ten artykuł zawiera informacje o testach porównawczych wydajności interfejsów API harmonogramu projektu i identyfikuje najlepsze rozwiązania dotyczące optymalnego użycia.
author: ruhercul
ms.date: 11/03/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 1ee1bd8e4412ee1d10f445628c5dc87cc9fa91d3
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8911195"
---
# <a name="project-schedule-api-performance"></a>Wydajność interfejsu API harmonogramu projektu

_**Dotyczy**: Project Operations dla scenariuszy opartych na zasobach/nieopartych na zaopatrzeniu, wdrażanie w wersji uproszczonej — od okazji do faktury pro forma, Project for the Web_

Ten artykuł zawiera informacje o testach porównawczych wydajności interfejsów programowania aplikacji (API) harmonogramu projektu i identyfikuje najlepsze rozwiązania dotyczące optymalizacji użycia.

## <a name="project-scheduling-service"></a>Usługa planowania projektów
Usługa planowania projektów to usługa wielodostępna działająca na platformie Microsoft Azure. Został zaprojektowany, aby poprawić interakcję, zapewniając szybkie i płynne działanie podczas pracy użytkowników nad projektami. Udoskonalenie to osiąga się poprzez akceptowanie wniosków o zmianę, przetwarzanie ich, a następnie natychmiastowe zwracanie wyniku. Usługa asynchronicznie utrzymuje się w Dataverse i nie blokuje użytkownikom wykonywania innych operacji.

Interfejsy API harmonogramu projektów opierają się na usłudze planowania projektów do uruchamiania żądań, które są opisane bardziej szczegółowo w dalszych sekcjach tego artykułu.

Interfejsy API harmonogramu projektu są przeznaczone do pracy z następującymi jednostkami struktury podziału pracy (WBS):

  - Project
  - Zadanie projektu
  - Zależność zadania projektu
  - Członek zespołu projektu
  - Przypisanie zasobu
  
Obsługiwane są zarówno pola out-of-box, jak i pola niestandardowe. O ile nie zaznaczono inaczej, obsługiwane są wszystkie typowe operacje, takie jak tworzenie, aktualizacja i usuwanie. Aby uzyskać więcej informacji, zobacz [Użyj interfejsów API harmonogramu projektu do wykonywania operacji z encjami planowania](schedule-api-preview.md).

W ramach interfejsów API harmonogramu projektu dodano wzorzec jednostki pracy. Ten wzorzec jest znany jako OperationSet i może być używany, gdy kilka żądań musi zostać przetworzonych w jednej transakcji.

Na poniższej ilustracji przedstawiono przepływ, który będzie odczuwany przez partnera, gdy ta funkcja jest używana.

![Dataverse i usługa planowania projektów.](./media/dataverse-project-scheduling-service-flow.png)

**Krok 1**: klient wywołujący interfejs API do punktu końcowego Open Data Protocol (OData) w Dataverse w celu utworzenia zestawu OperationSet.

**Krok 2**: Po utworzeniu nowego zestawu OperationSet jest zwracana wartość **OperationSetId**.

**Krok 3**: klient używa wartości **OperationSetId** do żądania innego interfejsu API harmonogramu projektów. Wynikiem jest żądanie utworzenia, zaktualizowania lub usunięcia w encji planowania. Po wysłaniu tego żądania wykonywana jest weryfikacja metadanych. Jeśli weryfikacja się nie powiedzie, żądanie zostanie zakończone i zostanie zwrócony błąd.

**Kroki 4a–4c:** Te kroki reprezentują etap ZAAKCEPTOWANIE. Klient uruchamia interfejs API **ExecuteOperationSetV1**, który wysyła wszystkie zmiany do Usługi planowania projektów w jednej partii. Usługa planowania projektów uruchamia własne weryfikacje żądań w partii. Wszelkie błędy walidacji cofają partię i zwracają wyjątek do wywołującego. Jeśli partia zostanie pomyślnie zaakceptowana przez usługę planowania projektów, stan OperationSet jest aktualizowany w celu odzwierciedlenia faktu, że OperationSet jest przetwarzana przez usługę planowania projektów.

**Krok 5**: Ten krok reprezentuje etap UTRWALENIA. Usługa planowania projektów asynchronicznie zapisuje partię w Dataverse w transakcji. Jeśli operacja zapisu zakończy się pomyślnie, operacja OperationSet jest oznaczona jako **Zakończono**. Wszelkie błędy cofną transakcję i partię, a OperationSet jest oznaczony jako **Nieudany**.

## <a name="performance-methodology"></a>Metodyki wydajności
Czas wykonania jest zdefiniowany jako czas od wywołania interfejsu API **ExecuteOperationSetV1** do momentu zakończenia przez usługę planowania projektów zapisywania w Dataverse. Wszystkie operacje są wykonywane łącznie 2200 razy, a pomiary czasu wykonania P99 są zgłaszane. Mierzone są operacje jedno-rekordowe i zbiorcze.

W przypadku operacji na jednym rekordzie OperationSet zawiera jedno żądanie. W przypadku operacji zbiorczych zawiera 20, 50 lub 100 żądań. Każdy rozmiar zbiorczy jest zgłaszany oddzielnie.

Operacje te są prowadzone na wdrożeniu UR 15 Project Operations Lite w Ameryce Północnej.

## <a name="results"></a>Wyniki
### <a name="create-operations"></a>Tworzenie operacji
#### <a name="single-record-create-operations"></a>Operacje tworzenia pojedynczych rekordów
W poniższej tabeli przedstawiono czasy wykonywania dla utworzenia jednego rekordu. Czasy są w sekundach.

<table class="tg">
<thead>
  <tr>
    <th class="tg-0lax" rowspan="2">Typ&nbsp;&nbsp;&nbsp;rekordu</th>
    <th class="tg-0lax" colspan="2">Czas</th>
  </tr>
  <tr>
    <th class="tg-0lax">Pola wymagane</th>
    <th class="tg-0lax">Wszystkie obsługiwane pola</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-0lax">Project</td>
    <td class="tg-0lax">2.5</td>
    <td class="tg-0lax">3.78</td>
  </tr>
  <tr>
    <td class="tg-0lax">Zadanie</td>
    <td class="tg-0lax">8.82</td>
    <td class="tg-0lax">9.34</td>
  </tr>
  <tr>
    <td class="tg-0lax">Przypisywanie</td>
    <td class="tg-0lax">9.19</td>
    <td class="tg-0lax">9.19</td>
  </tr>
  <tr>
    <td class="tg-0lax">Członek zespołu</td>
    <td class="tg-0lax">0.84</td>
    <td class="tg-0lax">4.2</td>
  </tr>
  <tr>
    <td class="tg-0lax">Zależność</td>
    <td class="tg-0lax">8.84</td>
    <td class="tg-0lax">8.84</td>
  </tr>
</tbody>
</table>

#### <a name="bulk-create-operations"></a>Operacje tworzenia zbiorczego
W poniższej tabeli przedstawiono czasy wykonywania dla utworzenia wielu rekordów. W szczególności firma Microsoft mierzy czasy wykonywania 20, 50 i 100 rekordów w jednej operacji OperationSet. Czasy są w sekundach.

<table class="tg">
<thead>
  <tr>
    <th class="tg-0lax" rowspan="3">Typ&nbsp;&nbsp;&nbsp;rekordu</th>
    <th class="tg-0lax" colspan="6">Czas</th>
  </tr>
  <tr>
    <th class="tg-0lax" colspan="2">20 rekordów</th>
    <th class="tg-0lax" colspan="2">50 rekordów</th>
    <th class="tg-0lax" colspan="2">100 rekordów</th>
  </tr>
  <tr>
    <th class="tg-0lax">Pola wymagane</th>
    <th class="tg-0lax">Wszystkie obsługiwane pola</th>
    <th class="tg-0lax">Pola wymagane</th>
    <th class="tg-0lax">Wszystkie obsługiwane pola</th>
    <th class="tg-0lax">Pola wymagane</th>
    <th class="tg-0lax">Wszystkie obsługiwane pola</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-0lax">Zadanie</td>
    <td class="tg-0lax">19.92</td>
    <td class="tg-0lax">38.35</td>
    <td class="tg-0lax">36.67</td>
    <td class="tg-0lax">99.13</td>
    <td class="tg-0lax">116.77</td>
    <td class="tg-0lax">174.06</td>
  </tr>
  <tr>
    <td class="tg-0lax">Przypisywanie</td>
    <td class="tg-0lax">13.94</td>
    <td class="tg-0lax">13.94</td>
    <td class="tg-0lax">43.95</td>
    <td class="tg-0lax">43.95</td>
    <td class="tg-0lax">69.38</td>
    <td class="tg-0lax">69.38</td>
  </tr>
  <tr>
    <td class="tg-0lax">Zależność</td>
    <td class="tg-0lax">30.04</td>
    <td class="tg-0lax">30.04</td>
    <td class="tg-0lax">77.82</td>
    <td class="tg-0lax">77.82</td>
    <td class="tg-0lax">176.89</td>
    <td class="tg-0lax">176.89</td>
  </tr>
</tbody>
</table>

> [!NOTE] 
> Operacje zbiorczego tworzenia encji **Projektów** i **Członków zespołu** nie są uwzględnione w tej tabeli, ponieważ środowisko wykonawcze tych operacji przypomina środowisko wykonawcze, gdy interfejs API do tworzenia jednego rekordu jest wywoływany wiele razy. Te interfejsy API są uruchamiane natychmiast w Dataverse.

Na poniższym rysunku pokazano czasy wykonywania encji **Zadanie**, **Przypisanie** i **Zależność** w momencie tworzenia 20, 50 i 100 rekordów i używane są wszystkie obsługiwane pola.

![Tworzenie wykresu czasu wykonywania rekordów.](./media/create-record-execution-time.png)

### <a name="update-operations"></a>Operacje aktualizacji
#### <a name="single-record-update-operations"></a>Operacje aktualizacji pojedynczego rekordu
W poniższej tabeli przedstawiono czasy wykonania aktualizacji pojedynczego rekordu. Czasy są w sekundach.

<table class="tg">
<thead>
  <tr>
    <th class="tg-0lax" rowspan="2">Typ&nbsp;&nbsp;&nbsp;rekordu</th>
    <th class="tg-0lax" colspan="2">Czas</th>
  </tr>
  <tr>
    <th class="tg-0lax">Pola wymagane </th>
    <th class="tg-0lax">Wszystkie obsługiwane pola</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-0lax">Project</td>
    <td class="tg-0lax">9.53</td>
    <td class="tg-0lax">13.91</td>
  </tr>
  <tr>
    <td class="tg-0lax">Zadanie</td>
    <td class="tg-0lax">8.82</td>
    <td class="tg-0lax">9.91</td>
  </tr>
  <tr>
    <td class="tg-0lax">Członek zespołu</td>
    <td class="tg-0lax">9</td>
    <td class="tg-0lax">8.96</td>
  </tr>
</tbody>
</table>

> [!NOTE]
> Operacje aktualizacji encji **Przypisania zasobów** i **Zależności zadań projektów** nie są obsługiwane.

#### <a name="bulk-update-operations"></a>Operacje aktualizacji zbiorczej
W poniższej tabeli przedstawiono czasy wykonania aktualizacji wielu rekordów. W szczególności firma Microsoft zmierzyła czasy wykonania aktualizacji 20, 50 i 100 rekordów w jednym OperationSet. Czasy są w sekundach.

<table class="tg">
<thead>
  <tr>
    <th class="tg-0lax" rowspan="3">Typ&nbsp;&nbsp;&nbsp;rekordu</th>
    <th class="tg-0lax" colspan="6">Czas</th>
  </tr>
  <tr>
    <th class="tg-0lax" colspan="2">20 rekordów</th>
    <th class="tg-0lax" colspan="2">50 rekordów</th>
    <th class="tg-0lax" colspan="2">100 rekordów</th>
  </tr>
  <tr>
    <th class="tg-0lax">Pola wymagane</th>
    <th class="tg-0lax">Wszystkie obsługiwane pola</th>
    <th class="tg-0lax">Pola wymagane</th>
    <th class="tg-0lax">Wszystkie obsługiwane pola</th>
    <th class="tg-0lax">Pola wymagane</th>
    <th class="tg-0lax">Wszystkie obsługiwane pola</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-0lax">Zadanie</td>
    <td class="tg-0lax">8.91</td>
    <td class="tg-0lax">38.71</td>
    <td class="tg-0lax">20.92</td>
    <td class="tg-0lax">87.13</td>
    <td class="tg-0lax">36.68</td>
    <td class="tg-0lax">190.34</td>
  </tr>
  <tr>
    <td class="tg-0lax">Członek zespołu</td>
    <td class="tg-0lax">20.52</td>
    <td class="tg-0lax">26.06</td>
    <td class="tg-0lax">41.93</td>
    <td class="tg-0lax">44.51</td>
    <td class="tg-0lax">38.63</td>
    <td class="tg-0lax">66.53</td>
  </tr>
</tbody>
</table>

> [!NOTE]
> Operacje aktualizacji encji **Przypisania zasobów** i **Zależności zadań projektów** nie są obsługiwane.

Na poniższej ilustracji przedstawiono wykres czasów wykonania dla encji Zadanie i Członek zespołu, gdy aktualizowane są rekordy 20, 50 i 100 i używane są wszystkie obsługiwane pola.

![Zaktualizuj wykres czasu wykonania rekordu.](./media/update-record-execution-time.png)

### <a name="delete-operations"></a>Operacje usuwania
#### <a name="single-record-delete-operations"></a>Operacje usuwania pojedynczego rekordu
W poniższej tabeli przedstawiono czasy wykonywania dla usuwania jednego rekordu. Czasy są w sekundach.

| Typ rekordów | Czas  |
|-------------|-------|
| Zadanie        | 20.12 |
| Przypisywanie  | 10.86 |
| Członek zespołu | 12.52 |
| Zależność  | 20.89 |

> [!NOTE]
> Operacje usuwania encji **Projekt** nie są obsługiwane.

#### <a name="bulk-delete-operations"></a>Operacje usuwania zbiorczego
W poniższej tabeli przedstawiono czasy wykonywania dla usuwania wielu rekordów. W szczególności firma Microsoft mierzy czasy wykonywania usuwania 20, 50 i 100 rekordów w jednej operacji OperationSet. Czasy są w sekundach.

<table class="tg">
<thead>
  <tr>
    <th class="tg-0lax" rowspan="2">Typ&nbsp;&nbsp;&nbsp;rekordu</th>
    <th class="tg-0lax" colspan="3">Czas</th>
  </tr>
  <tr>
    <th class="tg-0lax">20 rekordów</th>
    <th class="tg-0lax">50 rekordów</th>
    <th class="tg-0lax">100 rekordów</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-0lax">Zadanie</td>
    <td class="tg-0lax">20.91</td>
    <td class="tg-0lax">67.43</td>
    <td class="tg-0lax">71.96</td>
  </tr>
  <tr>
    <td class="tg-0lax">Przypisywanie</td>
    <td class="tg-0lax">11.75</td>
    <td class="tg-0lax">25.79</td>
    <td class="tg-0lax">47.66</td>
  </tr>
  <tr>
    <td class="tg-0lax">Członek zespołu</td>
    <td class="tg-0lax">9.78</td>
    <td class="tg-0lax">39.73</td>
    <td class="tg-0lax">24.33</td>
  </tr>
  <tr>
    <td class="tg-0lax">Zależność</td>
    <td class="tg-0lax">24.61</td>
    <td class="tg-0lax">54.9</td>
    <td class="tg-0lax">109.16</td>
  </tr>
</tbody>
</table>

> [!NOTE]
> Operacje usuwania encji **Projekt** nie są obsługiwane.

Na poniższym rysunku pokazano czasy wykonywania encji **Zadanie**, **Przypisanie**, **Członek zespołu** i **Zależność** w momencie usuwania 20, 50 i 100 rekordów.

![Usuń wykres czasu wykonania rekordu.](./media/delete-record-execution-time.png)

## <a name="observations"></a>Obserwacje
W przypadku każdej operacji na rekordzie wysłanie żądania do usługi planowania projektów przez interfejs API **ExecuteOperationSet** zajmuje około 800 milisekund. Usługa planowania projektów wymaga wtedy około pięciu sekund na przetwarzanie ładunku i wywołanie Dataverse. Resztę czasu wykonywania zajmuje uruchamianie logiki biznesowej i zapisywanie danych w bazie danych w Dataverse.

Po utworzeniu, zaktualizowaniu lub usunięciu 100 rekordów interfejs API **ExecuteOperationSet** zajmuje około trzech sekund, aby wysłać żądanie do usługi planowania projektów. Usługa planowania projektów wymaga wtedy około pięciu sekund na przetwarzanie żądań i wywołanie Dataverse. Operacje zbiorcze muszą płacić jeden raz podatku **Usługa planowania projektów** dla wszystkich rekordów w ramach zestawu OperationSet. W związku z tym operacje zbiorcze mają znacznie krótszy średni czas wykonania niż operacje z jednym rekordem.

## <a name="scenarios"></a>Scenariusze
W poniższej tabeli przedstawiono czasy wykonania, gdy interfejsy API harmonogramu projektu są używane do realizacji określonych scenariuszy. Czasy są w sekundach.

| Scenariusz                                                                   | Czas  |
|----------------------------------------------------------------------------|-------|
| Utwórz projekt z 40 zadaniami.                                      | 36.01 |
| Utwórz projekt, który ma 40 zadań i 20 zależności.                  | 38.11 |
| Utwórz projekt, który ma 40 zadań i 30 przydziałów.                   | 60.17 |
| Utwórz projekt, który ma 40 zadań, 20 zależności i 30 przydziałów. | 60.27 |

## <a name="best-practices"></a>Najlepsze rozwiązania
Na podstawie wyników poprzedniego scenariusza interfejsy API działają lepiej w następujących warunkach:

  - Należy zgrupować możliwie najwięcej operacji. Średni czas wykonywania operacji zbiorczych jest lepszy niż średni czas wykonywania operacji z jednym rekordem. Im mniejsza liczba używanych OperationSets, tym szybszy będzie średni czas wykonania.
  - Ustaw tylko minimalne atrybuty, które są wymagane do wykonania scenariusza. Wybieraj typy niewymaganych pól zawartych w żądaniu OperationSet. Pola zawierające klucze obce lub pola zestawień będą miały negatywny wpływ na wydajność.
