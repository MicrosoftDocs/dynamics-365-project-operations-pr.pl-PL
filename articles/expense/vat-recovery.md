---
title: Odzyskiwanie podatku VAT w zarządzaniu wydatkami
description: W tym temacie wyjaśniono, jak otrzymywać zwroty od kwalifikujących się transakcji podatkowych (VAT).
author: suvaidya
ms.date: 10/10/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: suvaidya
ms.openlocfilehash: 7c961763d3d670117c5a576db485ebcfdcf9ec9f
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/14/2022
ms.locfileid: "8581159"
---
# <a name="vat-recovery-in-expense-management"></a>Odzyskiwanie podatku VAT w zarządzaniu wydatkami

_**Zastosowane do:** Project Operations dla zasobów/scenariuszy nieopartych na zaopatrzeniu_

Aby otrzymywać zwrot kwalifikujących się transakcji VAT, firma lub organizacja musi identyfikować, gromadzić, sprawdzać i przedkładać dokładne informacje. Ten proces obejmuje wiele zadań i, w zależności od wielkości firmy, może wymagać współpracy wielu pracowników lub ról.

Aby odzyskać podatek VAT w module **Zarządzania wydatkami**, należy wykonać następujące wymagania wstępne:

- Kody podatku muszą zostać utworzone dla krajów/regionów przydzielonych do kategorii wydatków.
- Dla każdego kodu podatku musi zostać utworzona grupa podatku.
- Dla każdego grupy podatku musi zostać utworzony kod podatku od sprzedaży.

Po spełnieniu wymagań wstępnych należy wykonać następujące czynności, aby móc żądać zwrotów za transakcje VAT.

1. W przypadku raportu z wydatków wprowadź informacje podatkowe dotyczące transakcji kartą kredytową, aby zidentyfikować kwalifikujące się do zwrotu transakcje VAT.
2. Upewnij się, że wszystkie informacje o podatkach są kompletne, a następnie kliknij polecenie księgowanie raportu z wydatków.
3. Przetwórz wydatek, który może kwalifikować się do zwrotu międzynarodowego podatku VAT.
4. Wyślij dane zwrotu podatku VAT do dostawcy strony trzeciej, aby wystąpić o międzynarodowy zwrot.
5. Przetwarzanie wydatków na potrzeby krajowego zwrotu VAT.

W poniższej sekcji zamieszczono przykłady pokazujące sposób wykonywania poszczególnych czynności przez pracowników firmy Contoso.

## <a name="enter-tax-information-about-credit-card-transactions-to-identify-eligible-vat-refunds"></a>Wprowadź informacje podatkowe dotyczące transakcji kartą kredytową, aby zidentyfikować kwalifikujące się do zwrotu transakcje VAT

Nancy jest pracownikiem działu sprzedaży firmy Contoso, który jest zlokalizowany w Stanach Zjednoczonych, ale ostatnio wróciła z podróży służbowej do Zjednoczonego Królestwa. Podczas podróży, Nancy musiałą zapłacić kartą kredytową za posiłki. Nancy musi teraz utworzyć raport wydatków, aby odzyskać koszty.

Kiedy Nancy wprowadza informacje w raporcie wydatków, wybiera **Zjednoczone Królestwo** w polu **Kraju/regionu** na stronie **Edytowanie raportu wydatków**. Lista grup podatku jest następnie filtrowana w taki sposób, aby pokazywała tylko grupy mające zastosowanie do Zjednoczonego Królestwa. Nancy wybiera grupę podatkową **Zjednoczone Królestwo 001**, a następnie wybiera grupę podatkową **Posiłki**. Następnie Nancy dodaje nową transakcję do przetworzenia. Ponieważ w Zjednoczonym Królestwie istnieje tylko jedna grupa podatkowa i grupa podatkowa dla towarów, te informacje są automatycznie wypełniane w raporcie z wydatków Nancy.

Dla każdej zasady z firmy Contoso wszystkie wydatki muszą mieć pasujący przychód. Z tego powodu przy zapisywaniu raportu z wydatków jest wyświetlany komunikat informujący o tym, że musi dołączyć potwierdzenie dla każdej transakcji, która jest wymieniona w raporcie z wydatków. Nancy potwierdza, że dołączyła cyfrowe zdjęcie paragonu każdej transakcji do raportu i przesyła go do zatwierdzenia. Następnie wysyła paragony do zespołu back-office, zajmującego się przetworzeniem zgłoszenia. Ten zespół prześle dane związane ze zwrotem VAT dostawcom strony trzeciej, którzy obsługują zwrot międzynarodowego podatku VAT dla firmy Contoso.

## <a name="verify-tax-information-and-post-an-expense-report"></a>Sprawdzanie poprawności informacji podatkowych i księgowanie raportu z wydatków

Zanim April, koordynator ds. rozrachunków z dostawcami firmy Contoso będzie mogła zaksięgować raport wydatków, musi podać w nim informacje podatkowe, których póki co brakuje. Otwiera stronę **Szczegółów raportu z wydatków** i widzi zatwierdzony raport o wydatkach Nancy. April otworzy raport wydatków, aby wyświetlić szczegółowe informacje o transakcjach. Widzi, że Nancy nie wprowadziła grupy podatku dla towaru w jednej z transakcji. Ponieważ te informacje nie są dostępne, April nie może opublikować raportu z wydatków. Sprawdza więc stronę **Konfiguracje podatku** w zarządzaniu wydatkami i znajduje grupę podatku dla towaru dla danego kraju/regionu oraz typu transakcji. April może teraz zaksięgować raport z wydatków w księdze głównej.

Po zaksięgowaniu przez April raportu z wydatków tworzony jest element roboczy odzyskiwania VAT. Ten element roboczy jest przypisany do członka zespołu back-office, zajmującego się przetwarzaniem. April otrzymuje komunikat potwierdzający, że księgowanie zakończyło się powodzeniem. W tym komunikacie znajduje się również liczba transakcji VAT zidentyfikowanych podczas zwrotu.

## <a name="process-expenses-that-are-eligible-for-international-vat-recovery"></a>Przetwarzanie wydatku, który może kwalifikować się do międzynarodowego zwrotu podatku VAT

Arnie, członek zespołu back-office w Contoso odpowiedzialny za przetwarzanie wniosków o zwrot potwierdza, czy wszystkie wymagane informacje dotyczące zwrotu podatku VAT są zawarte w raportach wydatków. Otwiera stronę **Zwrotu podatku z wydatków** i wybiera raport o wydatkach, który Nancy przedłożyła. Arnie następnie sprawdza, czy zostały dołączone wszystkie wymagane paragony oraz czy wprowadzono poprawne kody podatku i kodów podatku towaru.

Kiedy Arnie otrzymuje papierowe paragony od Nancy, weryfikuje je względem tych cyfrowych, a następnie zmienia stan raportu z wydatków na **Gotowe do zwrotu**.

## <a name="send-vat-recovery-data-to-the-third-party-vendor"></a>Wysyłanie danych zwrotnych z podatku VAT do strony trzeciej

Kiedy Arnie jest gotowy do wysłania danych z raportu o wydatkach do dostawcy strony trzeciej, który zgłosi się po zwrot podatku VAT, otwiera stronę **Zwrotu podatku od wydatków**. Przefiltruje stronę w taki sposób, aby pokazywały się wyłącznie raporty o kosztach oznaczone jako **Gotowe do zwrotu**. Arnie następnie wybierze opcję **Plik** &gt; **Eksportuj jako plik Excel**. Informacje o podatku VAT z raportów z wydatków są eksportowane do arkusza programu Microsoft Excel. Arnie przesyła ten arkusz do dostawcy strony trzeciej i dodaje wiadomość o tym, że paragony zostały wysyłane za pomocą kuriera.

## <a name="process-expenses-for-domestic-vat-recovery"></a>Przetwarzanie wydatków na potrzeby krajowego zwrotu VAT

Arnie musi sprawdzić, czy transakcje raportu z wydatków są objęte zwrotem podatku VAT, oraz czy paragony cyfrowe są dołączone do raportów. Aby rozpocząć przetwarzanie kwalifikujących się kosztów dla celów krajowych, Arnie otwiera stronę **Zwrotu podatku od wydatków** i wybiera raport o wydatkach, który wymaga weryfikacji. Weryfikuje, że paragony są wystawione na firmę, nie na pracownika. (Na potrzeby zwrotu VAT paragony muszą być wystawione na firmę.) Arnie następnie sprawdza, czy zostały dołączone wszystkie wymagane paragony oraz czy wprowadzono poprawne kody podatku i kodów podatku towaru.

Kiedy Arnie otrzymuje paragony na papierze, zmienia stan raportu z wydatków na **Gotowy do zwrotu**. Następnie może zgłosić zwrot w odpowiednim urzędzie skarbowym. W tym przypadku odpowiednim urzędem skarbowym w Stanach Zjednoczonych jest Internal Revenue Service (IRS).


[!INCLUDE[footer-include](../includes/footer-banner.md)]