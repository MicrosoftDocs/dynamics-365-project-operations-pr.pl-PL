---
title: Weryfikacja faktur dostawców przy użyciu zatwierdzonych wartości rzeczywistych
description: W tym artykule wyjaśniono, w jaki sposób Microsoft Dynamics 365 Project Operations umożliwia kierownikom projektów weryfikację faktur od dostawców z wartościami rzeczywistymi, które zostały zatwierdzone jako wykonawcy wykonali pracę i zarejestrowany czas, oraz wydatki i materiały, które były używane przez członków zespołu projektowego.
author: rumant
ms.date: 03/30/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 43f47a44260d1a47437846f2764b56f680d4b682
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8914231"
---
# <a name="verification-of-vendor-invoices-with-approved-actuals"></a>Weryfikacja faktur dostawców przy użyciu zatwierdzonych wartości rzeczywistych

[!include [banner](../../includes/dataverse-preview.md)]

_ **Zastosowane w:** Wdrażanie uproszczone — od okazji do faktury pro forma

W Microsoft Dynamics 365 Project Operations menedżerowie projektów sprawdzają wiersze faktur dostawcy na następujące sposoby:

- Użyj pola Stan **weryfikacji** w wierszach faktur dostawcy.
- Jeśli wiersze faktury dostawcy odwołują się do wiersza kontraktu podrzędnego, wartości rzeczywiste kosztu z działania podwykonawcy należy połączyć z tymi wierszami faktury dostawcy. Łącze jest tworzone przez dopasowanie wartości rzeczywistych kosztu do wierszy faktury dostawcy.

    > [!NOTE]
    > Wprawdzie można śledzić stan weryfikacji w wierszach faktur dostawcy, które nie odwołują się do kontraktu podrzędnego, ale nie można połączyć wartości rzeczywistych kosztów z tymi wierszami faktur dostawcy.

## <a name="verification-status"></a>Stan weryfikacji

Pole **Stanu weryfikacji** w wierszu faktury dostawcy wskazuje na stan weryfikacji. Następujące stany postępu są obsługiwane:

1. Nie rozpoczęto
2. W toku
3. Zakończony

Można edytować wiersze faktury dostawcy o statusie weryfikacji **Nierozpoczęte**.

Nie można edytować wiersze faktury dostawcy o statusie weryfikacji **W toku**. W przypadku wiersza faktury od dostawcy, który odwołuje się do umowy podwykonawstwa, stan weryfikacji jest automatycznie ustawiany na **W toku**, gdy tylko pierwszy koszt rzeczywisty zostanie dopasowany do wiersza faktury od dostawcy.

Nie można edytować wiersze faktury dostawcy o statusie weryfikacji **Zakończony**. Gdy wszystkie wiersze na fakturze od dostawcy mają ten stan weryfikacji, można potwierdzić fakturę od dostawcy.

## <a name="match-cost-actuals-to-vendor-invoice-lines"></a>Dopasuj rzeczywiste koszty do wierszy faktury dostawcy

Dopasowywanie wartości rzeczywistych kosztów pomaga w procesie weryfikacji w wierszu faktury dostawcy. Aby dopasować wartości rzeczywiste kosztów do wiersza faktury dostawcy, wykonaj następujące kroki.

1. Otwórz wiersz faktury dostawcy i wybierz kartę **Niedopasowane wartości rzeczywiste kosztów**. W siatce jest wyświetlona lista wartości rzeczywistych kosztów, które odwołują się do tej samej wiersza kontraktu podrzędnego co wiersz faktury dostawcy.
2. Wybierz co najmniej jeden z wartości rzeczywistych kosztów, a następnie wybierz opcję **Dopasowania na pasku narzędzi nad siatką**. System sprawdza, czy można dopasować wybrane wartości rzeczywiste kosztów. Po weryfikacji wartości rzeczywiste kosztów są łączone z linią faktur dostawcy.

### <a name="validation-criteria-that-are-used-to-link-cost-actuals-to-vendor-invoice-lines"></a>Kryteria weryfikacji używane do łączenia wartości rzeczywistych kosztów z wierszami faktur dostawcy

Podczas procesu dopasowywania między wartością rzeczywistą kosztu a linią faktur dostawcy można ustalić tylko wtedy, gdy zostaną spełnione oba poniższe warunki:

- Pole **Stanu Dostosowania** dla każdego wybranego kosztu musi być puste. Innymi słowy, wartości rzeczywiste kosztów nie muszą być zastępowane innymi wartościami rzeczywistymi kosztów podczas procesu zatwierdzania, anulowania lub poprawki.
- Wartości następujących pól są dopasowane między linią faktur dostawcy a wybranym kosztem. Jeśli dowolne pole nie jest ustawione w wierszu faktury dostawcy, nie jest uważane za pasujące.

    - Kontrakt projektu
    - Pozycja kontraktu projektu
    - Klasa transakcji
    - Project
    - Zadanie
    - Kategoria zasobów
    - Kategoria transakcji
    - Produkt
    - Wiersz podumowy
    - Zasób, który można zarezerwować

## <a name="unmatch-cost-actuals-from-a-vendor-invoice-line"></a>Niezgodność rzeczywistych kosztów z wiersza faktury dostawcy

Niedopasowanie wartości rzeczywistych kosztów może także pomóc w procesie weryfikacji faktury dostawcy, umożliwiając usunięcie wcześniej ustalonych łączy. Rzeczywiste koszty mogą być niedopasowane tylko z wierszy faktur od dostawcy, które mają stan weryfikacji **W toku**. Aby usunąć rzeczywiste koszty z wiersza faktury dostawcy, wykonaj następujące kroki.

1. Otwórz wiersz faktury dostawcy i wybierz kartę **Dopasowane wartości rzeczywiste kosztów**. W siatce jest wyświetlona lista wartości rzeczywistych kosztów, które odwołują się kontraktu podrzędnego co wiersz faktury dostawcy.
2. Wybierz co najmniej jeden z wartości rzeczywistych kosztów, a następnie wybierz opcję **Usuń dopasowanie**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
