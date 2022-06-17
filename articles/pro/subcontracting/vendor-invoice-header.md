---
title: Szczegóły nagłówka faktur dostawcy
description: Ten artykuł zawiera objaśnienie funkcji, które są dostępne w nagłówku faktury dostawcy w Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 03/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 95f84f2d2a357abbd8d507705412a0434b44f658
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8929871"
---
# <a name="header-details-for-vendor-invoices"></a>Szczegóły nagłówka faktur dostawcy

[!include [banner](../../includes/dataverse-preview.md)]

_**Zastosowane w:** Wdrażanie uproszczone — od okazji do faktury pro forma_

Ten artykuł zawiera objaśnienie funkcji, które są dostępne w nagłówku faktury dostawcy w Microsoft Dynamics 365 Project Operations.

Jako menedżerowie projektów planują i realizują projekty, mogą zatrudniać podwykonawców oraz nabywać produkty i usługi od dostawców. Podczas wykonywania projektu koszty są ponoszone w ramach kategorii usług, materiałów i wydatków, które są wykorzystywane w ramach kontraktów dodatkowych z dostawcami. Dostawcy wystawiają te koszty na projekty za pomocą tworzenia faktur od dostawców.

Poniższa tabela zawiera informacje o polach w nagłówkach faktur od dostawców w Project Operations.

| Pole | Description | Wpływ funkcjonalny |
| --- | --- | --- |
| Imię i nazwisko/nazwa | Nazwa faktury od dostawcy. | Na wszystkich listach rozwijanych faktur od dostawcy nazwa faktury od dostawcy jest wymieniona w pierwszej kolumnie, aby ułatwić identyfikację faktury od dostawcy. Domyślnie podczas tworzenia faktury dostawcy na podstawie kontraktu podrzędnego w polu **Nazwa** faktury dostawcy jest ustawiana wartość utworzona na podstawie nazwy podwykonawcy oraz bieżącej daty. |
| Description | Krótki opis usług i produktów, które są fakturowane na fakturze dostawcy. | None |
| Dostawca (sprzedawca) | Nazwa firmy fakturowania produktów i usług. Ta firma powinna być rekordem konta typu **Dostawca** lub **Dostawca** w relacji . | <p>W zależności od wybranego dostawcy wartości domyślne są automatycznie wprowadzane w następujących polach:</p><ul><li>Waluta</li><li>Cenniki</li><li>Warunki płatności</li><li>Adres płatności</li></ul> |
| Podumowa | Odwołanie do podwykonawcy faktury dostawcy. | <p>Na podstawie wybranej umowy podwykonawczej w następujących polach automatycznie wprowadzane są wartości domyślne:</p><ul><li>Waluta</li><li>Cenniki</li><li>Warunki płatności</li><li>Adres płatności</li></ul><p>Kontrakt podrzędny wybrany w nagłówku faktury dostawcy jest wprowadzany domyślnie w wierszach faktury dostawcy i nie można go tam zmienić.</p> |
| Data faktury | Data wartości rzeczywistych kosztów, która zostanie utworzona po potwierdzenie faktury dostawcy. | Data faktury służy również do wybrania prawidłowego cennika zakupu z cenników dołączonych do powiązanego dostawcy lub z parametrów projektu. |
| Przyczyna stanu | Stan faktury od dostawcy projektu. | <p>Stan określa, gdzie w procesie biznesowym znajduje się faktura od dostawcy i czy można ją edytować. Oto niektóre z dostępnych wartości:</p><ul><li>**Wersja robocza** — fakturę dostawcy można edytować.</li><li>**Potwierdzone** — faktura dostawcy została sprawdzona i potwierdzone. Faktur dostawcy w tym stanie nie można edytować ani usuwać.</li><li>**W procesie** — faktura dostawcy jest sprawdzana. Faktury dostawcy w tym statusie można edytować, ale nie można ich usunąć.</li><li>**Anulowano** — faktura dostawcy została anulowana. Faktur dostawcy w tym stanie nie można edytować ani usuwać.</li></ul> |
| Waluta | Waluta, w jakiej dostawca fakturowania produktów i usług na fakturze dostawcy. | Na fakturze dostawcy, która odwołuje się do kontraktu podrzędnego, waluta kontraktu podrzędnego jest domyślnie wprowadzana jako waluta faktury dostawcy. Na fakturze dostawcy, która nie odwołuje się do kontraktu podrzędnego, wartość domyślna jest wprowadzana z rekordu konta dostawcy i można ją zmienić. Po zapisaniu faktury dostawcy nie można edytować waluty. |
| Jednostka kontraktująca | Wydział firmy odpowiedzialny za otrzymywanie usług i/lub produktów od dostawcy. | None |
| Warunki płatności | Warunki płatności na wystawianych fakturach od dostawcy. Wartość domyślna jest wprowadzana automatycznie z rekordu konta dostawcy. | Warunki płatności z umowy podwykonawczej są kopiowane do wszystkich faktur od dostawców powiązanych z umową podwykonawczą. Warunki płatności można zaktualizować, jeśli faktura od dostawcy ma status **Wersja robocza**. |
| Adres płatności | Adres dostawcy, na który należy wysłać płatności. Wartość domyślna jest wprowadzana automatycznie z rekordu konta dostawcy. | Adres płatności z umowy podwykonawczej jest kopiowany jako adres płatności do wszystkich faktur od dostawcy, które są tworzone dla tej umowy podwykonawczej. Adres płatności można zaktualizować, jeśli faktura dostawcy ma status **Wersja robocza**. |
| Suma częściowa | Jeśli faktura dostawcy nie ma żadnych wierszy, wprowadź suma częściowa faktury przed podatkami. Jeśli faktura dostawcy ma wiersze, to pole jest tylko do odczytu. W takim przypadku wyświetlana kwota jest sumą częściową ze wszystkich wierszy na fakturze od dostawcy. | None |
| Łączny podatek | Jeśli faktura od dostawcy nie zawiera wierszy, wprowadź łączną kwotę podatków w umowie podwykonawczej. Jeśli faktura dostawcy ma wiersze, to pole jest tylko do odczytu. W takim przypadku wyświetlana kwota jest sumą kwot podatku ze wszystkich wierszy na fakturze od dostawcy. | None |
| Łączna kwota | To pole obliczane pokazuje łączną kwotę faktury dostawcy po wliczonej fakturze. | None |

> [!NOTE]
> Po zapisaniu faktury dostawcy nie można zmienić następujących pól: **Dostawca**, **Podwykonawca**, **Waluta**, **Jednostka kontraktu** i **Warunki płatności**. Jeśli są wymagane zmiany tych pól na fakturze dostawcy, należy usunąć fakturę dostawcy i utworzyć nową fakturę dla dostawcy.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
