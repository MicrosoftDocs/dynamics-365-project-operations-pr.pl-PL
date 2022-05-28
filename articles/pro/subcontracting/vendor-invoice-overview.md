---
title: Fakturowanie dostawcy — koncepcja i tworzenie
description: W temat opisano pojęcia faktur dostawcy, scenariusze użycia oraz sposób tworzenia faktur od dostawców w firmie Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 03/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: dc9b3954b237294f52aa0bb74f8008a5dfdf78fd
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/14/2022
ms.locfileid: "8580561"
---
# <a name="vendor-invoicing---concept-and-creation"></a>Fakturowanie dostawcy — koncepcja i tworzenie

[!include [banner](../../includes/dataverse-preview.md)]

_**Zastosowane w:** Wdrażanie uproszczone — od okazji do faktury pro forma_

Fakturowanie dostawcy w Microsoft Dynamics 365 Project Operations może być wykorzystywane do rejestrowanie kosztów związanych z dostarczaniem usług i/lub materiałów w ramach projektu przez dostawców.

Jeśli usługi i/lub materiały są podwykonawcy świadczone dostawcy, podwykonawca reprezentuje umowę kontraktową z tym dostawcą. Gdy dostawca zapewnia usługi, ponieważ materiały są odbierane i wykorzystywane do zadań projektów, koszty są rejestrowane w ramach projektu. Co pewien czas dostawca wysyła faktury, które są sprawdzone i dopasowane do kosztów zarejestrowanych w projekcie. Po zakończeniu procesu weryfikacji faktura dostawcy jest potwierdzana i wystawiana do płatności.

## <a name="scenarios-for-use"></a>Scenariusze użycia

Faktury dostawcy w Project Operations mogą być używane do obsługi dwóch różnych scenariuszy.

### <a name="customers-use-the-full-subcontracting-experiences"></a>Klienci korzystają z pełnych funkcji obsługi podrzędnej

Faktury od dostawcy mogą weryfikować i dopasować wpisy czasu, użycie materiałów oraz wpisy wydatków, które odwołują się do składników kontraktów podwykonawców, a także do pozycji faktury dostawcy. Ten proces może służyć do sprawdzania rzetelności wierszy faktur dostawcy. Po zakończeniu procesu weryfikacji i zweryfikowaniu faktury dostawcy aplikacja wycofa wartości rzeczywiste zarejestrowane w zatwierdzonych dziennikach czasu, wydatków i materiałów oraz utworzy nowe wartości rzeczywiste kosztów przy użyciu wierszy faktur dostawcy.

### <a name="customers-dont-use-the-full-subcontracting-experiences-but-want-to-have-a-unified-view-of-costs-on-projects-in-project-operations"></a>Klienci nie używają pełnych funkcji obsługi podrzędnej, ale chcą mieć ujednolicony widok kosztów w ramach projektów w Project Operations

W przypadku śledzenia procesu podwykonawcy w systemie innych firm można zarejestrować koszty z systemu innych firm do Project Operations, tworząc faktury dostawców, które nie odwołują się do kontraktów dodatkowych. W ten sposób menedżerowie projektów mogą mieć pojedynczy, ujednolicony widok wszystkich kosztów w ramach danego projektu.

## <a name="creation-of-vendor-invoices-in-project-operations"></a>Tworzenie faktur od dostawcy w Project Operations

Faktury dostawcy można tworzyć na dwa sposoby:

- Na stronie listy faktur dostawcy lub na stronie szczegółów jednej faktury od dostawcy
- Na stronie listy podwykonawców lub na stronie szczegółów dotyczących pojedynczego kontraktu podrzędnego

### <a name="creation-from-the-vendor-invoice-list-page-or-details-page"></a>Tworzenie ze strony listy lub szczegółów listy faktur dostawcy

1. Przejdź do **zakupu** \> **faktury dostawcy**.
2. Na stronie listy faktur dostawcy lub na stronie szczegółów pojedynczej faktury dostawcy wybierz opcję **Nowy**, aby utworzyć nową fakturę dla dostawcy.

Faktury dostawcy utworzone w ten sposób mogą także odwoływać się do kontraktu podrzędnego.

### <a name="creation-from-the-subcontract-list-page-or-details-page"></a>Tworzenie ze strony z listą podwykonawców lub strony ze szczegółami

1. Przejdź do **Zakupy** \> **Podumowy**.
2. Wybierz co najmniej jedną umowę podwykonawczą.
3. Na stronie listy umów podwykonawczych lub stronie szczegółów pojedynczej umowy podwykonawczej wybierz **Utwórz fakturę od dostawcy**, aby utworzyć nową fakturę od dostawcy.

Dla każdego wybranego kontraktu podrzędnego zostanie utworzona nowa faktura dostawcy w stanie **wersja robocza**.

Faktury dostawcy tworzące w ten sposób zawsze odwołują się do kontraktu podrzędnego w nagłówku faktury dostawcy. Każdy wiersz w podwykonawcy z metodą rozliczania godzin i materiałów spowoduje utworzenia wiersza na fakturze dostawcy. Każdy wiersz w podwykonawcy, który ma metodę rozliczania ze stałą ceną, spowoduje utworzenia wiersza na fakturze dostawcy dla każdego punktu kontrolnygo wiersza podrzędnego, który ma stan **Gotowy do zafakturowania**.

Następujące pola i rekordy pokrewne zostaną skopiowane z kontraktu podrzędnego do nagłówka faktury dostawcy:

- Dostawca.
- Pokrewne cenniki zostaną skopiowane na fakturę dostawcy jako cenniki.
- Waluta.
- Jednostka kontraktująca.
- Warunki płatności.

W przypadku wierszy podwykonawców dotyczących godziny i materiałów następujące pola i rekordy pokrewne zostaną skopiowane z wiersza kontraktu podrzędnego do wiersza faktury dostawcy:

- Odwołania do kontraktów podwykonawców i podwykonawców
- Klasa transakcji
- Rola
- Kategoria transakcji
- Pola produktu
- Project
- Zadanie
- Zasób, który można zarezerwować

W przypadku wierszy umowy podwykonawstwa o ustalonej cenie następujące pola zostaną skopiowane z wiersza podwykonawstwa i kamienia milowego wiersza podwykonawstwa do wiersza faktury dostawcy:

- Odwołania do kontraktów podwykonawców i podwykonawców.
- Klasa transakcji. Domyślnie wartość będzie **punktem kontrolnym**.
- Nazwa i kwota punktu kontrolnygo zostaną skopiowane z powiązanego punktu kontrolnego wiersza podrzędnego.
- Użytkownik będzie mógł wybrać projekt i zadanie w wierszu faktury dostawcy.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
