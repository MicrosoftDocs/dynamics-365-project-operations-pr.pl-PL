---
title: Prognozy i budżety projektów
description: Microsoft Dynamics 365 Finance zapewnia prognozy projektów i budżety projektów umożliwiające zarządzanie projektami i kontrolowanie ich.
author: Yowelle
ms.date: 10/25/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ForecastModel, ProjYearEndProcess
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 23501
ms.assetid: 4e6d1384-19a2-4232-b3f3-d2590c218bd7
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c1c1cde984334af8cc30e7899e3cf0b38467666f
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 05/10/2021
ms.locfileid: "5999639"
---
# <a name="project-forecasts-and-budgets"></a>Prognozy i budżety projektów

[!include [banner](../includes/banner.md)]

Istnieją dwa sposoby zarządzania i kontroli nad projektami: prognozy projektów i budżety projektów. 

Jeśli organizacja ma perspektywę operacyjna i koncentruje się na przychodach i kosztach pochodzących z określonych transakcji, można użyć prognozowania. Użyj budżetowania projektu, jeśli Twoja organizacja koncentruje się bardziej na kwotach finansowych. 

Prognozy projektów i budżety projektów używają modeli prognoz do przechowywania prognozowanych kwot transakcji. 

Każda metoda ma swoje zalety. Przed wybraniem metody dla organizacji warto rozważyć następujące kwestie.

|   Metoda alokacji       |           Prognozowanie projektu            |        Budżetowanie projektu                           |
|---------------------------|------------------------------------------|----------------------------------------------------|
| **Alokacja okresu**     | Nie można jawnie alokować transakcji w okresie obrachunkowym. Zamiast tego prognozy i kontrola prognozy są oparte na okresie trwania projektu. Ponieważ prognozy są obliczane na podstawie konkretnego dnia, okres należy wywnioskować z poziomu daty. | Możesz alokować transakcje w całym projekcie lub okresie fiskalnym. Jeśli dokonasz alokacji w okresie, możesz przenieść niewykorzystane kwoty do następnego okresu podatkowego. |
| **Wyświetlanie transakcji**  | Możesz przeglądać transakcje w formularzach prognoz, w których widzisz prognozy dla całej firmy i wszystkich projektów, niezależnie od hierarchii. Aby skupić się na konkretnym projekcie, należy filtrować dane.                                       | Istnieje możliwość wyświetlenia transakcji budżetowych na jedną hierarchię projektów. Z tego powodu użytkownik może wyświetlić szczegółowe informacje dotyczące transakcji dla projektu nadrzędnego lub jego podprojektów.                 |
| **Zmienne transakcji** | Po wprowadzeniu transakcji prognozy można użyć wszystkich atrybutów, które istnieją w przypadku transakcji rzeczywistej. Pozwala to na większą szczegółowość prognozy. Można na przykład wprowadzić szczegóły dotyczące ilości, pracowników, towarów lub właściwości wiersza.         | Podczas wprowadzania informacji o budżecie można korzystać wyłącznie z kwot, kategorii i działań.                    |
| **Zabezpieczenia**              | Prognoza jest oparta na transakcjach wprowadzonych w formularzach prognozy i polegających na tym, że nie ma mechanizmu kontroli procesów. Każdy pracownik, który ma uprawnienia do formularza prognozy, może skorygować informacje bez zatwierdzania.                                        | Budżetowanie powoduje użycie systemu przepływu pracy, który umożliwia zarządzanie zmianami i umożliwia zachowanie historii zmian.         |
| **Typy encji**           | Zapisy transakcji prognozy są oparte na liczbie jednostek oraz w cenach kosztów i jednostkowych sprzedaży.  | Szczegóły budżetu są obliczane na podstawie kwot, które są dzielone między koszty i przychody.                                          |
| **Modele prognoz**       | Ze względu na fakt, że każda prognoza musi być skojarzona z modelem, można utworzyć wiele modeli prognoz oraz zdefiniować podmodele.           | W budżecie projektu są ograniczone modele prognoz używane podczas budżetowania. Mniejsza liczba modeli prognozy może zwiększyć spójność w projekcjach.                           |
| **Przekroczenia kosztów**         | Można zezwalać lub zabraniać na wprowadzanie transakcji, które spowodują przekroczenie kosztu.   | W budżecie projektu są dostępne dodatkowe opcje kontrolne dotyczące użytkowników. Można zezwolić na ostrzeżenia i przekroczenia.                    |
| **Formant**               | Sterowanie prognozami odbywa się za pomocą redukcji prognozy. Kwoty rzeczywiste są odejmowane od sald transakcji prognozowanych bez żadnego dowodu inspekcji. Może to utrudnić śledzenie miejsc, w których wystąpiły faktyczne transakcje.                   | W kontrolce budżet projektu kwoty rzeczywiste są odejmowane od kwot w pozostałym budżecie. Pozwala to na jaśniejszą historię inspekcji.                                   |

## <a name="project-forecasts"></a>prognozy projektu
Korzystając z prognozowania projektu, można wprowadzać transakcje prognozy w formularzach prognoz dla każdego typu transakcji. Każdy atrybut dostępny dla rzeczywistej transakcji może być użyty do prognozowanej transakcji - na przykład rentowność linii, atrybuty linii, pracownicy lub opisy. Możesz także przewidzieć, po jakim czasie po poniesieniu kosztów wystawisz fakturę klientowi. 

Transakcje prognozowania projektów są oparte na jednostkach i kwotach. 

Każda prognoza projektu musi być skojarzona z modelem prognozy. Wprowadzenie transakcji planowania powoduje automatyczne sugerowanie modelu prognozy. Model prognozy pełni rolę kontenera transakcji prognozy. 

Modele prognozy można wyznaczyć jako podmodeli dla modelu. Pozwala to na prognozowanie według regionu, okresu lub działu. Możesz skopiować transakcje prognozy w modelu, aby utworzyć nowy model, a także możesz przenieść transakcje do księgi głównej. Ponieważ istnieje relacja jeden do jednego między prognozą a modelem, każdy model prognozy stanowi oddzielny budżet dla projektu. 

W modelach prognoz do obsługi projektów może służyć redukcja prognozowana. W redukcji prognozy rzeczywiste transakcje zmniejszają prognozowane salda transakcji. Jednak ponieważ redukcja prognozy jest stosowana do najwyższego projektu w hierarchii, zapewnia ograniczony widok zmian w prognozie. Jeśli na przykład pracownik jest skojarzony z podprojektem, rzeczywiste transakcje dotyczące pracownika są księgowane w projekcie nadrzędnym. Może to utrudnić śledzenie zmian, ponieważ nie można łatwo określić transakcji, w której podprojekt spowodował obniżkę kwoty prognozy. Z tego powodu dobrze jest utworzyć kopię modelu prognozy, która będzie używana do obniżenia prognozy. Następnie można używać raportów do wyświetlania pierwotnie prognozowanych wartości. 

Prognozy projektów można korygować, kopiować, usuwać i przenosić do księgi głównej budżetu. Nie ma jednak żadnych kontrolnych procesów. Każdy pracownik, który ma uprawnienia do formularza prognozy, może wprowadzać poprawki bez przeglądu.

-   **Popraw**– Prognozowaną transakcję można skorygować w tych samych formularzach, w których wprowadzono oryginalne wpisy.
-   **Kopiowanie lub usuwanie** — podczas kopiowania transakcji planowania kopiowane są wiersze transakcji z jednego modelu prognozy do innego modelu prognozy. Usunięcie prognozy powoduje usunięcie transakcji prognozy z modelu prognozy. Aby ograniczyć sposób kopiowania lub usuwania transakcji prognozowanych, wybierz konkretne typy transakcji i daty. Pozwala to na skopiowanie lub usunięcie tylko określonych części prognozy.
-   **Przeniesienie** — Po przeniesieniu prognozy projektu do budżetu księgi głównej przenosi się transakcje prognozy modelu prognozy do budżetu księgi głównej. Istnieje możliwość zastąpienia wszystkich przetransferowanych wcześniej transakcji w budżecie księgi głównej, do której ma zostać przesunięta prognoza projektu.

## <a name="project-budgets"></a>Budżety projektu
Budżetowanie projektów jest prostszym sposobem niż Prognoza, ale jest integrowana z modelami prognoz. Używa pojedynczego formularza wprowadzania oryginalnych szczegółów i poprawek budżetu oraz pozwala na prognozy oparte wyłącznie na kwocie, kategorii lub działaniu. 

W budżetowaniu projektu wszystkie pierwotne budżety i poprawki muszą zostać przesłane do przepływu pracy projektu w celu zatwierdzenia. Przepływy pracy zapewniają większą kontrolę nad procesem i tworzą rekord historii zmian. 

Budżetowanie projektu przypomina budżetowanie księgi głównej, ale jest ono szybsze i łatwiejsze w konfigurowaniu. Wiele opcji budżetowania księgi głównej, takich jak sekwencje numerów lub waluta, nie należy konfigurować oddzielnie dla projektów.

Budżety projektów są automatycznie skojarzone z dwoma modelami prognozowania, jednym dla pierwszego budżetu i jednym na pozostały budżetem. Z tego powodu raporty oparte na modelach prognoz mogą używać danych budżetu. Podczas zatwierdzania budżetu projektu są tworzone transakcje prognoz oparte na modelach skojarzonych, które są używane na potrzeby raportowania i kontroli.

## <a name="forecast-models"></a>Modele prognoz
Modele prognozy mają hierarchię z jedną warstwą. Oznacza to, że jedna prognoza projektu musi być skojarzona z jednym modelem prognozy.

Jeśli używasz prognozowania projektu, możesz identyfikować modele jako modele podrzędne. Następnie możesz tworzyć prognozy według działu, okresu lub regionu. Na przykład można utworzyć model prognozy na rok, a następnie utworzyć podmodele dla prognoz regionalnych północno-wschodnich, południowo-wschodnich, północno-zachodnich i południowo-zachodnich, które przesyłają szefowie regionów. Wybierając różne opcje w dostępnych raportach, możesz przeglądać informacje według prognozy całkowitej lub podmodelu.





[!INCLUDE[footer-include](../includes/footer-banner.md)]