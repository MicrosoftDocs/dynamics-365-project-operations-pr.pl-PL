---
title: Zarządzanie dostawcami i cennikami zakupu w Project Operations
description: W tym artykule znajdziesz informacje pomocne w tworzeniu i obsłudze danych dostawców oraz cenników zakupu dla podwykonawców.
author: rumant
ms.date: 08/02/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 6840ffcbc510fe6385dd3fdaf881e9700c4fdd18
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8914139"
---
# <a name="vendor-and-purchase-price-list-management-in-project-operations"></a>Zarządzanie dostawcami i cennikami zakupu w Project Operations

[!include [banner](../../includes/dataverse-preview.md)]

_**Zastosowane w:** Wdrażanie uproszczone — od okazji do faktury pro forma_

## <a name="vendors-in-project-operations"></a>Dostawcy w Project Operations

W Microsoft Dynamics 365 Project Operations konta dostawcy mają typ relacji **Dostawca** lub **Dostawca (producent)**. Jako dostawcę w umowie podwykonawczej można wybrać tylko rekord podmiotu, który ma jeden z tych typów relacji.

Z rekordem dostawcy można powiązać jeden lub więcej cenników zakupu. Jednak każdy cennik zakupu skojarzony z rekordem dostawcy powinien mieć odrębną datę obowiązywania. Project Operations nie obsługuje nakładania się dat dla cenników zakupu.

Domyślnie dla każdej umowy podwykonawczej tworzonej dla dostawcy używane są następujące pola i pojęcia w rekordzie dostawcy:

- Warunki płatności
- Rachunek do kontaktu
- Kontakt podstawowy

    > [!NOTE]
    > Domyślnie główny kontakt dostawcy jest używany jako menedżer konta dostawcy w umowie podwykonawczej.

- Waluta
- Aktualne cenniki zakupu

## <a name="purchase-price-lists-in-project-operations"></a>Cenniki zakupu w Project Operations

Cennik, dla którego pole **Kontekst** zawiera wartość **Zakup**, jest cennikiem zakupu. Cenniki zakupu można zdefiniować w taki sposób, aby przedstawiały katalog cen zakupu dla czasu, wydatków i materiałów. Cenniki zakupu przypominają cenniki kosztów i sprzedaży w Project Operations. Poniższe koncepcje dotyczą cenników zakupu w taki sam sposób, jak mają zastosowanie do cenników kosztów i sprzedaży:

- **Data ważności** — Cenniki zakupu mają datę ważności. Data ważności jest reprezentowana przez pola daty rozpoczęcia i daty zakończenia w każdym cenniku. Czas między datą początkową a datą końcową to okres obowiązywania daty.
- **Waluta** — Waluta w nagłówku cennika jest używana jako waluta, w której wyrażone są ceny zakupu dla kategorii robocizny, wydatków i produktów w katalogu.
- **Domyślna jednostka czasu** — domyślna jednostka czasu wyraża ceny pracy przy zakupach. Pole jednostki czasu w cenniku służy tylko do podania wartości domyślnej. Wartość tę można zmienić w poszczególnych wierszach cen roli.

Cenniki zakupu można dołączać do rekordów dostawców jako powiązania znane jako cenniki projektu. Te cenniki służą do wprowadzania cen domyślnych w wierszach kontraktów. Domyślnie, gdy do rekordu dostawcy dołączonych jest wiele cenników zakupu, dla umów podwykonawczych tworzonych dla dostawcy używany jest najbardziej aktualny cennik. Tylko cenniki, dla których pole **Kontekst** zawiera wartość **Zakup**, można dołączać do rekordów dostawców.

### <a name="subcontract-specific-purchase-price-lists"></a>Cenniki zakupu specyficzne dla podwykonawców

Cenniki zakupu można również dołączać do umów podwykonawczych jako stowarzyszenia, zwane cennikami projektów. Te cenniki służą do wprowadzania cen domyślnych w wierszach kontraktów. Domyślnie, gdy do umowy podwykonawczej dołączonych jest wiele cenników zakupu, każdy z nich musi mieć odrębną datę obowiązywania. Project Operations nie obsługują cenników zakupu, które mają nakładającą się datę ważności. Tylko cenniki, dla których pole **Kontekst** zawiera wartość **Zakup**, można dołączać do podwykonawców.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
