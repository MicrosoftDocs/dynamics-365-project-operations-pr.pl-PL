---
title: Odzyskiwanie podatku VAT
description: W tym temacie wyjaśniono, jak otrzymywać zwrot od kwalifikujących się transakcji podatkowych (VAT).
author: saraschi2
ms.date: 02/26/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TrvPerDiems
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 20e29a47d73d28c0bf8dbb3495ad301481c529cd
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 05/10/2021
ms.locfileid: "5993609"
---
# <a name="vat-recovery"></a>Odzyskiwanie podatku VAT 

Aby otrzymywać zwrot kwalifikujących się transakcji VAT, firma lub organizacja musi identyfikować, gromadzić, sprawdzać i przedkładać dokładne informacje. Ten proces obejmuje wiele zadań i, w zależności od wielkości firmy, może wymagać współpracy wielu pracowników lub ról.

Aby odzyskać podatek VAT w module Zarządzania wydatkami, należy spełnić następujące wymagania wstępne:

- Kody podatku muszą zostać utworzone dla krajów/regionów przydzielonych do kategorii wydatków.
- Dla każdego kodu podatku musi zostać utworzona grupa podatku.
- Dla każdego grupy podatku musi zostać utworzony kod podatku od sprzedaży.

Po spełnieniu wymagań wstępnych pracownik musi wykonać następujące czynności, aby móc żądać zwrotów za transakcje VAT.

1. W przypadku raportu z wydatków wprowadź informacje podatkowe dotyczące transakcji kartą kredytową, aby zidentyfikować kwalifikujące się do zwrotu transakcje VAT.
2. Upewnij się, że wszystkie informacje o podatkach są kompletne, a następnie kliknij polecenie księgowanie raportu z wydatków.
3. Przetwórz wydatek, który może kwalifikować się do zwrotu międzynarodowego podatku VAT.
4. Wyślij dane zwrotu podatku VAT do dostawcy strony trzeciej, aby wystąpić o międzynarodowy zwrot.
5. Przetwarzanie wydatków na potrzeby krajowego zwrotu VAT.

Poniższe sekcje zawierają przykłady, które pokazują, jak pracownicy Contoso wykonują poszczególne kroki.

## <a name="on-an-expense-report-enter-tax-information-about-credit-card-transactions-to-identify-eligible-vat-refunds"></a>W przypadku raportu z wydatków wprowadź informacje podatkowe dotyczące transakcji kartą kredytową, aby zidentyfikować kwalifikujące się do zwrotu transakcje VAT

Nancy, przedstawicielka handlowa firmy Contoso pracująca w Stanach Zjednoczonych, wróciła niedawno z podróży handlowej do Wielkiej Brytanii. Podczas podróży, Nancy musiała zapłacić kartą kredytową za posiłki. Nancy musi teraz utworzyć raport wydatków, aby odzyskać koszty.

Kiedy Nancy wprowadza informacje w raporcie wydatków, wybiera **Zjednoczone Królestwo** w polu **Kraju/regionu** na stronie **Edytowanie raportu wydatków**. Lista grup podatku jest następnie filtrowana w taki sposób, aby pokazywała tylko grupy mające zastosowanie do Zjednoczonego Królestwa. Nancy wybiera grupę podatkową **Zjednoczone Królestwo 001**, a następnie wybiera grupę podatkową **Posiłki**. Następnie dodaje nową transakcję do przetworzenia. Ponieważ w Zjednoczonym Królestwie istnieje tylko jedna grupa podatkowa i grupa podatkowa dla towarów, te informacje są automatycznie wypełniane w raporcie z wydatków Nancy.

Zgodnie z zasadami firmy Contoso wszystkie wydatki muszą mieć odpowiedni paragon. Z tego powodu przy zapisywaniu raportu z wydatków jest wyświetlany komunikat informujący o tym, że musi dołączyć potwierdzenie dla każdej transakcji, która jest wymieniona w raporcie z wydatków. Nancy potwierdza, że dołączyła cyfrowe zdjęcie paragonu każdej transakcji do raportu i przesyła go do zatwierdzenia. Następnie wysyła paragony do zespołu back-office, zajmującego się przetworzeniem zgłoszenia. Zespół ten prześle dane dotyczące odzyskiwania podatku VAT do zewnętrznego dostawcy, który składa międzynarodowe deklaracje VAT dla Contoso.

## <a name="make-sure-that-all-tax-information-is-complete-and-then-post-the-expense-report"></a>Upewnij się, że wszystkie informacje o podatkach są kompletne, a następnie kliknij polecenie księgowanie raportu z wydatków

April, koordynator ds. zobowiązań w firmie Contoso musi wprowadzić brakujące informacje podatkowe, zanim będzie mogła zaksięgować raport wydatków. Otwiera stronę **Szczegółów raportu z wydatków** i widzi zatwierdzony raport o wydatkach Nancy. April otworzy raport wydatków, aby wyświetlić szczegółowe informacje o transakcjach. Widzi, że Nancy nie wprowadziła grupy podatku dla towaru w jednej z transakcji. Ponieważ te informacje nie są dostępne, April nie może opublikować raportu z wydatków. April sprawdza więc stronę **Konfiguracje podatku** w zarządzaniu wydatkami i znajduje grupę podatku dla towaru dla danego kraju/regionu oraz typu transakcji. April może teraz zaksięgować raport z wydatków w księdze głównej.

Po zaksięgowaniu przez April raportu z wydatków tworzony jest element roboczy odzyskiwania VAT. Ten element roboczy jest przypisany do członka zespołu back-office, zajmującego się przetwarzaniem. April otrzymuje komunikat potwierdzający, że księgowanie zakończyło się powodzeniem. W tym komunikacie znajduje się również liczba transakcji VAT zidentyfikowanych podczas zwrotu.

## <a name="process-expenses-that-are-eligible-for-international-vat-recovery"></a>Przetwarzanie wydatku, który może kwalifikować się do międzynarodowego zwrotu podatku VAT

Arnie, członek zespołu Back-office w Contoso, jest odpowiedzialny za sprawdzanie, czy na raportach wydatków znajdują się wszystkie informacje wymagane do odzyskania podatku VAT. Otwiera stronę **Zwrotu podatku z wydatków** i wybiera raport o wydatkach, który Nancy przedłożyła. Arnie sprawdza, czy zostały dołączone wszystkie wymagane paragony oraz czy wprowadzono poprawne kody podatku i kodów podatku towaru.

Kiedy Arnie otrzymuje papierowe paragony od Nancy, weryfikuje je w stosunku do tych cyfrowych, a następnie zmienia stan raportu z wydatków na **Gotowe do zwrotu**.

## <a name="send-vat-recovery-data-to-the-third-party-vendor-to-file-international-recovery-returns"></a>Wyślij dane zwrotu podatku VAT do dostawcy strony trzeciej, aby wystąpić o międzynarodowy zwrot

Kiedy Arnie jest gotowy do wysłania danych z raportu o wydatkach do dostawcy strony trzeciej, który zgłosi się po zwrot podatku VAT, otwiera stronę **Zwrotu podatku od wydatków**. Przefiltruje stronę w taki sposób, aby pokazywały się wyłącznie raporty o kosztach oznaczone jako **Gotowe do zwrotu**. Arnie następnie wybierze opcję **Plik** &gt; **Eksportuj jako plik Excel**. Informacje o podatku VAT z raportów z wydatków są eksportowane do arkusza programu Microsoft Excel. Arnie przesyła ten arkusz do dostawcy strony trzeciej i dodaje wiadomość o tym, że paragony zostały wysyłane za pomocą kuriera.

## <a name="process-expenses-for-domestic-vat-recovery"></a>Przetwarzanie wydatków na potrzeby krajowego zwrotu VAT

Arnie musi sprawdzić, czy transakcje raportu z wydatków są objęte zwrotem podatku VAT, oraz czy paragony cyfrowe są dołączone do raportów. Aby rozpocząć przetwarzanie kwalifikujących się kosztów dla celów krajowych, Arnie otwiera stronę **Zwrotu podatku od wydatków** i wybiera raport o wydatkach, który wymaga weryfikacji. Weryfikuje, że paragony są wystawione na firmę, nie na pracownika. Podczas otrzymywania zwrotu podatku VAT paragony muszą być wystawione na firmę. Arnie następnie potwierdza, że zostały zastosowane poprawne grupy podatku od sprzedaży podatku i kody podatków dla danego towaru.

Kiedy Arnie otrzymuje paragony na papierze, zmienia stan raportu z wydatków na **Gotowy do zwrotu**. Następnie może zgłosić zwrot w odpowiednim urzędzie skarbowym. W tym przypadku odpowiednim urzędem skarbowym w Stanach Zjednoczonych jest Internal Revenue Service (IRS).


[!INCLUDE[footer-include](../includes/footer-banner.md)]