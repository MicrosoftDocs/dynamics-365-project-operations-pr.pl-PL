---
title: Co nowego w lipcu 2021 r. — wdrażanie wersji uproszczonej aplikacji Project Operations
description: To temat zawiera informacje o istotnych aktualizacjach dostępnych w wydaniu aplikacji wdrożenia wersji uproszczonej aplikacji Project Operations z lipca 2021 r.
author: sigitac
ms.date: 07/07/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 475ceea3a6c6db9fe63e3950eaca5d9074faa766
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/14/2022
ms.locfileid: "8583965"
---
# <a name="whats-new-july-2021---project-operations-lite-deployment"></a>Co nowego w lipcu 2021 r. — wdrażanie wersji uproszczonej aplikacji Project Operations

_Zastosowane do: Wdrażanie uproszczone — od okazji do faktury pro forma_

Ten temat dotyczy następujących składników i wersji aplikacji Dynamics 365 Project Operations:

  - Project Operations w środowisku Dataverse w wersji 4.12.0.148 lub 4.12.0.152.

## <a name="quality-updates"></a>Aktualizacje dotyczące jakości
| **Obszar funkcji**              | **Numer referencyjny** | **Aktualizacja dotycząca jakości**                                                                                                                                                                                             |
|-------------------------------|----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Rozliczenia i ceny           | 2224046              | Pole **Klasa transakcji** można edytować na karcie **Szczegóły wiersza oferty**, ale jest zablokowane w przypadku pracy na stronie **Szczegóły wiersza oferty**.                                                                     |
| Rozliczenia i ceny           | 2224400              | Akcja **Zamknij ofertę jako wykorzystaną** kończy się niepowodzeniem, gdy oferta nie ma kamieni milowych związanych z datami.                                                                                                                                    |
| Rozliczenia i ceny           | 2234089              | Po ręcznym wprowadzeniu opisu produktu jest ono czyszczony po wprowadzeniu ilości dla szacowania materiału.                                                                                                                         |
| Rozliczenia i ceny           | 2234100              | Siatka **Ustawienie rozliczeń zadań** nie zawiera kolumny **Materiały** ani jej wartości na karcie **Fakturowanie zadania** projektu.                                                                                                       |
| Rozliczenia i ceny           | 2277409              | Identyfikator produktu jest niedostępny w szczegółach pozycji kontraktu dla wiersza materiałów.                                                                                                                                        |
| Rozliczenia i ceny           | 2281728              | Tworzenie niepotrzebnej pozycji kontraktu powoduje ponowną ocenę wartości rzeczywistych, co znacząco zwiększa ilość danych i wpływa na wydajność.                                                                                |
| Rozliczenia i ceny           | 2298668              | Wiersze arkusza skojarzone z wycofanym i usuniętym wydatkiem nie są usuwane.                                                                                                                                     |
| Rozliczenia i ceny           | 2300192              | Gdy wielu użytkowników edytuje fakturę, istnieje możliwość utworzenia nowych szczegółów wiersza faktury na potwierdzonej fakturze.                                                                                   |
| Rozliczenia i ceny           | 2301569              | Nie można skorygować faktur, jeśli zastosowano zachowanie kwoty \$0.                                                                                                                                        |
| Rozliczenia i ceny           | 2307965              | Błąd występuje, jeśli cena kategorii jest tworzona z brakującymi wartościami.                                                                                                                           |
| Rozliczenia i ceny           | 2326870              | Występuje błąd w elemencie **Microsoft.Dynamics.ProjectService.Plugins.PostInvoiceLineDelete**, jeśli opcja **producttypecode** ma wartość null.                                                                            |
| Rozliczenia i ceny           | 2332732              | Błąd występuje w przypadku utworzenia kamienia milowego pozycji kontraktu bez wiersza zamówienia.                                                                                                                |
| Planowanie i śledzenie projektu | 2181094              | Interfejs API planowania projektów obsługuje teraz dzienniki programu PSS i dzienniki zestawu operacji, które są przechowywane przez 90 dni.                                                                                                                  |
| Planowanie i śledzenie projektu | 2254201              | Etykieta **Tryb harmonogramu** zostanie zaktualizowana przy użyciu szczegółów opisujących logikę ustalania wartości domyślnych.                                                                                                                                      |
| Planowanie i śledzenie projektu | 2300252              | Pamięć podręczna odpowiedzi **openProject** zostanie zaktualizowana i będzie uwzględniać właściciela tokenu w kluczu pamięci podręcznej oraz **bazowym adresie URL** i **adresie URL segmentu**, można będzie zawsze odtworzyć **adres URL żądania**, jeśli **bazowy adres URL** zmieni się. |
| Planowanie i śledzenie projektu | 2301312              | Element **msdyn_membershipstatus** zostały usunięte z widoku **członka zespołu projektu**.                                                                                                                                        |
| Planowanie i śledzenie projektu | 2302759              | Produkty są niepotrzebnie pobierane na kartach **Przypisania zasobów**, **Szacowania** i **Szacowania wydatków**.                                                                                                        |
| Planowanie i śledzenie projektu | 2308050              | Akcja **CopyProject** kończy się niepowodzeniem i jest wyświetlany komunikat o błędzie „Nie można pobrać tokenu umożliwiającego wymianę informacji z usługą zdalną”.                                                                                                                           |
| Planowanie i śledzenie projektu | 2322650              | Widok **Lista zadań projektu** został zaktualizowany w celu domyślnego wyświetlania daty zadania.                                                                                                            |
| Planowanie i śledzenie projektu | 2327266              | Akcja **CopyProject** generuje błąd „Nie znaleziono klucza w słowniku” podczas kopiowania szacowanych wartości.                                                                                                      |
| Planowanie i śledzenie projektu | 2328123              | Akcja **CopyProject** generuje błąd „Nie można pobrać tokenu umożliwiającego wymianę informacji z usługą zdalną”.                                                                                                                          |
| Planowanie i śledzenie projektu | 2336258              | Akcja **CopyProject** niepoprawnie kopiuje nazwy położenia zasobów.                                                                                                                                                 |
| Rozliczenia i ceny           | 2224476              | Pole **Zasób, który można zarezerwować** nie jest poprawnie ustawione domyślnie na zalogowanego użytkownika na stronie **Użycie materiałów**.                                                                                                            |
| Zarządzanie zasobami           | 2277249              | Błąd występuje, gdy jest aktualizowane wymaganie zasobów nieoparte na projekcie.                                                                                                            |
| Zarządzanie zasobami           | 2323869              | Wykorzystanie zasobów nie rozpoznaje poprawnie filtrowanych zasobów.                                                                                                                                             |
| Czas i wydatek              | 2176538              | Do kontrolki **Wpis czasu** są stosowane nieprawidłowe operatory filtrów.                                                                                                                                                   |
| Czas i wydatek              | 2177462              | Usunięcie wpisu czasu w siatce nie powoduje zaktualizowania stanu przycisku **Prześlij**, **Wycofaj**, **Usuń** i **Edytuj wpis** zgodnie z oczekiwaniami.                                                                                        |
| Czas i wydatek              | 2299985              | Element **TimeEntriesImportFromResourceAssignment** nie zachowuje czasu rozpoczęcia/zakończenia z rozkładów przypisania.                                                                                                  |
| Czas i wydatek              | 2318426              | Po przesłaniu wpisu czasu zablokowane pola można nadal edytować.                                                                                                                                   |
| Czas i wydatek              | 2323749              | Błąd występuje, gdy na karcie **Pokrewne** zasobu, który można zarezerwować, tworzony jest wydatek.                                                                                                      |
| Czas i wydatek              | 2327678              | Po utworzeniu wpisu czasu z karty **Pokrewne** zasobu, który można zarezerwować, zasób nadrzędny nie jest przekazywany do kontrolki wpisu czasu.                                                                            |
| Ogólne                       | 2296857              | Śledzenie postępu w przypadku długotrwałych zadań.                                                                                                                                                                        |
| Ogólne                       | 2253682              | Rozwiązania do podwójnego zapisu Project Operations nie należy instalować, jeśli rdzeń podwójnego zapisu jest instalowany w środowisku bez rozwiązania do aranżacji podwójnego zapisu.                                                |
| Ogólne                       | 2316420              | Aprowizowanie rdzenia aplikacji Project Service kończy się niepowodzeniem, jeśli zostanie zmieniona jednostka biznesowa użytkownika aplikacji.                                                                                                                     |
| Ogólne                       | 2376405              | Rozwiązany problem z aktualizacją oparty na wydawcy (aktualizacja Quality jest dostępna w wersji 4.12.0.152)                                                                                                                     |
