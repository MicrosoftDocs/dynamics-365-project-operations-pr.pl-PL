---
title: Wymagania dotyczące pozycji dla umów projektowych z wieloma źródłami finansowania
description: Ten artykuł zawiera informacje na temat konfigurowania i używania wymagań dotyczących przedmiotów z wieloma źródłami finansowania.
author: sigitac
ms.date: 05/04/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: a54ca1ec5e78d9d0af7b67914f6a63154c7347d3
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8931205"
---
# <a name="item-requirements-for-project-contracts-with-multiple-funding-sources"></a>Wymagania dotyczące pozycji dla umów projektowych z wieloma źródłami finansowania

_**Dotyczy:** Project Operations dla scenariuszy obejmujących magazynowanie/zlecenia produkcyjne_

Niektóre umowy umowne dotyczące wyników projektu mogą wymagać wielu źródeł finansowania. W artykule wyjaśniono sposób wybierania i konfigurowania żądanych źródeł źródła, gdy dla kontraktu projektu lub projektu jest wymagane wiele źródeł.

## <a name="terminology"></a>Terminologia

- **Źródło źródeł źródeł** — encja, która finansuje pracę kontraktu projektu. Może to być organizacja wewnętrzna lub zewnętrzne konto na fakturze (klient lub grant).
- **Klient projektu** — encja, do która jest dostarczana praca nad projektem.
- **Konto faktury** — encja zewnętrzna, która płaci za prace nad projektem.

## <a name="example"></a>Przykład

Firma Contoso wygrała umowę na odnowienie sprzętu z dwoma swoimi klientami: Adatum US i Adatum Corporate. Umowa obejmuje usługi sprzętowe i instalacyjne, które zostaną dostarczone do Adatum US (klient projektu). Sprzęt zostanie sfinansowany przez Adatum Corporate (rachunek nr 1), a prace instalacyjne zostaną sfinansowane przez Adatum US (rachunek nr 2).

## <a name="set-up-invoice-account-defaulting-rules-for-item-requirements"></a>Konfigurowanie reguł domyślnych dla kont na fakturach dla wymagań dotyczących elementów

### <a name="prerequisites"></a>Wymagania wstępne

- Microsoft Dynamics 365 Finance and Operations **wersja 10.0.27 lub nowsza** jest wymagana do korzystania z wymagań dotyczących pozycji, które mają wiele kont faktur.
- Administrator systemu musi włączyć funkcję **Zezwalaj na wymagania dotyczące pozycji z wieloma źródłami finansowania dla scenariuszy Project Operations opartych na zapasach/produkcji** w obszarze roboczym **Zarządzanie funkcjami**.

### <a name="set-up-the-invoice-account-defaulting-rules"></a>Konfigurowanie reguł domyślnych dla konta faktury

Aby skonfigurować reguły domyślne dla konta zafakturowego, wykonaj następujące kroki.

1. Przejdź do **Zarządzanie projektami i księgowanie** \> **Ustawienia** \> **Parametry zarządzania projektami i księgowanie**.
1. Na karcie **Ogólne** w sekcji **Zamówienia sprzedaży** i Wymagania pozycji ustaw opcję **Zezwalaj na projekty z wieloma źródłami źródeł** na wartość **Tak**.
1. W polu **Klient** domyślny określ, skąd domyślnie pochodzi klient dostawy projektu dotyczący wymagania elementu:

    - **Ze źródła danych** — domyślny klient realizacji projektu pochodzi ze źródła źródła. Jeśli z kontraktem projektów jest skojarzonych wiele źródeł źródeł, zostanie użyte pierwsze źródło źródeł źródeł.
    - **Z projektu** — domyślny klient dostawy projektu pochodzi od klienta, który jest wybrany w polu **Konta rekordu** Projektu.

1. Opcjonalnie: ustawianie lub zmienianie domyślnego konta faktury dla rekordów projektu:

    1. Przejdź do menu **Zarządzanie projektami i rozliczeniami** \> **projekty** \> **Wszystkie projekty** i otwórz szczegóły rekordu projektu.
    2. Na karcie **Ogólne** ustaw lub zaktualizuj pole **Domyślne konto faktury**. Określone konto będzie używane jako domyślne konto faktury dla nowych wymagań dotyczących elementów, które zostaną utworzone dla projektu. Jeśli pole pozostaw puste, domyślnie będzie używane konto faktury dla pierwszego źródła poszukania kontraktu projektu. Użytkownicy mogą jednak zmienić konto podczas zapisywania rekordu.

### <a name="select-the-invoice-account-to-use-when-you-create-an-item-requirement"></a>Wybieranie konta faktury do użycia podczas tworzenia wymagania dotyczącego elementu

Aby wybrać konto faktury, które będzie używane podczas tworzenia zapotrzebowania na pozycję, wykonaj poniższe kroki.

1. Przejdź do menu **Zarządzanie projektami i rozliczeniami** \> **projekty** \> **Wszystkie projekty** i otwórz rekord projektu.
1. Na karcie **Plan** wybierz pozycję **Wymagania elementu**.
1. Utwórz nowy rekord zapotrzebowania na pozycję.

    - Domyślnie pole **Konto faktury** w rekordzie ma ustawioną wartość konta faktury ustawionego dla projektu. Możesz zmienić wartość pola **konto faktury**, a następnie zapisać rekord. Po zapisaniu rekordu nie można już zaktualizować wartości **konto faktury**. Jeśli wartość **konto Faktury** musi zostać zaktualizowana dla wymagania elementu, należy usunąć istniejące wymaganie dotyczące elementu, a następnie utworzyć nowe wymaganie o wymaganej wartości.
    - Domyślnie pole **Klient** dla wymagania elementu jest ustawiane na podstawie **wartości domyślnej klienta** ustawionej na stronie **Zarządzanie projektami i parametry księgowe**.

    Po zapisaniu rekordu wymagania elementu system kojarzy go z rekordem nagłówka **zamówienia sprzedaży dotyczącego wymagania pozycji**. Jeśli żaden otwarty nagłówek zamówienia sprzedaży nie zawiera wybranego konta faktury, system utworzy je i skojarzy z nim wiersz wymagań elementu.

> [!NOTE]
> Wymagania dotyczące pozycji są zawsze w pełni zafakturowane dla konta faktury ustawionego w rekordzie. System nie obsługuje obecnie reguł konfigurowania reguł rozdzielania części, które mają wymagania dotyczące elementów, i nie rozdziela wpisy na podstawie konfiguracji reguł tego procesu.

### <a name="create-an-item-requirement-from-an-item-forecast-record"></a>Tworzenie wymagania elementu z rekordu prognozy elementów

Aby utworzyć zapotrzebowanie na pozycję z rekordu prognozy pozycji, należy wykonać poniższe kroki.

1. Przejdź do menu **Zarządzanie projektami i rozliczeniami** \> **projekty** \> **Wszystkie projekty** i otwórz rekord projektu.
1. Na karcie **Plan** wybierz pozycję **Prognozy pozycji**.
1. Utwórz nowy rekord prognozy pozycji.
1. Opcjonalnie: na karcie **Projekt**, w polu **Źródło po fakturze** wybierz żądane konto faktury.
1. Wybierz **opcję Utwórz wymaganie elementu** i potwierdź wyświetlony komunikat.

    > [!NOTE]
    > System kopiuje wartość **Źródło finansowania** z rekordu prognozy pozycji do nowo utworzonego rekordu zapotrzebowania na pozycję.

### <a name="default-invoice-account-when-the-system-automatically-creates-an-item-requirement-from-a-purchase-order-line"></a>Domyślne konto faktury, gdy system automatycznie tworzy wymaganie pozycji z wiersza zamówienia zakupu

Jeśli opcja **Utwórz zapotrzebowanie na pozycję** jest ustawiona na **Tak** na stronie **Parametry zarządzania projektem i księgowości**, system automatycznie tworzy zapotrzebowanie na pozycję podczas zapisywania nowej linii zamówienia zakupu projektu. Domyślnie pola **Konto faktury** i **Wymagania pozycji** są ustawione na wartość pola Konto faktury **Domyślne w rekordzie projektu**. System nie obsługuje obecnie aktualizowania ani zmieniania konta faktury dla rekordów tego typu.
