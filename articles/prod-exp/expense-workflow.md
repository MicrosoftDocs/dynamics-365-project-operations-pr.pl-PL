---
title: Przepływ pracy zarządzania wydatkami
description: W tym artykule wyjaśniono, jak korzystać z systemu przepływu pracy w rozwiązaniu Microsoft Dynamics 365 Finance w celu skonfigurowania procesu kontroli dla raportu wydatków w funkcji Zarządzanie wydatkami.
author: ShylaThompson
ms.date: 09/13/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WorkflowtableListPageRnr
audience: Application User
ms.reviewer: johnmichalak
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 71efc89d9167ef1ee546c67c123efeb37125cc02
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8929733"
---
# <a name="expense-management-workflow"></a>Przepływ pracy zarządzania wydatkami

Sposób korzystania z systemu przepływu pracy można dostosować w celu skonfigurowania procesu przeglądu raportów o wydatkach w zarządzaniu wydatkami. Użytkownik może skonfigurować przepływ pracy, który korzysta z następujących kryteriów w celu określenia, kto zatwierdza raporty o wydatkach:

- Hierarchia raportowania pracowników i wstępnie zdefiniowane ograniczenia zatwierdzania
- Zatwierdzanie na wielu poziomach, które obsługuje zatwierdzanie tymczasowe i ostateczną osobę zatwierdzającą
- Zakres finansowy i zakres odpowiedzialności projektu
- Przypisywanie do określonych użytkowników lub grup użytkowników

Zatwierdzanie przepływu pracy można utworzyć na potrzeby raportów z wydatków, wniosków wyjazdowych, zaliczek w gotówce oraz zwrotu podatku VAT.

**Przykład**

Poniższy proces stanowi przykład przepływu pracy Zarządzanie wydatkami w ramach raportu z wydatków.

1. Pracownik tworzy i zapisuje raport wydatków.
2. Pracownik przesyła raport do zatwierdzenia. Osoba zatwierdzająca jest identyfikowana na podstawie reguł zdefiniowanych podczas konfigurowania przepływu pracy.
3. Osoba zatwierdzająca otrzymuje powiadomienie o przygotowaniu raportu o wydatkach do zatwierdzenia. Sprawdza, a następnie zatwierdza raport z wydatków i potwierdza, że są spełnione następujące warunki:

    - Koszty nie naruszają żadnych zasad dotyczących wydatków. Jeśli wydatek narusza zasadę, osoba zatwierdzająca weryfikuje, czy raport z wydatków zawiera prawidłowe uzasadnienie biznesowe.
    - Do raportu z wydatków są dołączone paragony w wersji cyfrowej.

4. Osoba zatwierdzająca zatwierdza raport o wydatkach.
5. Raport o wydatkach jest przypisywany do koordynatora rozrachunków z klientami w celu zaksięgowania.
6. W zależności od tego, czy skonfigurowane jest automatyczne księgowanie, czy nie, ma miejsce jedno z następujących:

    - Jeśli skonfigurowano automatyczne księgowanie, raport o wydatkach jest przetwarzany w celu dokonania płatności, a stan raportu o wydatkach jest zaktualizowany.
    - Jeśli automatyczne księgowanie nie jest skonfigurowane, wtedy koordynator ds. rozrachunków z dostawcami weryfikuje, że wszystkie oryginalne paragony zostały przesłane i że zgadzają się z kosztami w raporcie z wydatków. Wszystkie kody podatków wprowadzone w raporcie z wydatkami również muszą zostać sprawdzone pod kątem poprawności.

Dopiero po sprawdzeniu tych wymagań raport jest księgowany.

Po zaksięgowaniu raportu o wydatkach płatność jest zatwierdzana, a pracownik otrzymuje zwrot.


[!INCLUDE[footer-include](../includes/footer-banner.md)]