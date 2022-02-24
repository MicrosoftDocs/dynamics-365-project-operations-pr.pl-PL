---
title: Tworzenie ręcznej faktury proforma - wersja uproszczona
description: Ta temat zawiera informacje na temat tworzenia ręcznej faktury proforma w Project Operations.
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 5a924de6efc377e28a20e038e7deac04616b95aa
ms.sourcegitcommit: 2b74edd31f38410024a01124c9202a4d94464d04
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/17/2020
ms.locfileid: "4764516"
---
# <a name="create-a-manual-proforma-invoice---lite"></a>Tworzenie ręcznej faktury proforma - wersja uproszczona

_**Zastosowane w:** Wdrażanie uproszczone — od okazji do faktury pro forma_

W Dynamics 365 Project Operations, faktury proforma mogą być tworzone ręcznie, zgodnie z potrzebami. Fakturę proforma można utworzyć ręcznie na stronie list **Kontraktów projektu** lub na stronie szczegółów **Kontraktów projektu**.

##  <a name="project-contracts-list-page"></a>Strona list Kontraktów projektu

Z poziomu strony listy **Kontraktów projektu** wybierz co najmniej jeden kontrakt projektu i utwórz faktury dla wszystkich wybranych rekordów.

System sprawdzi, który z wybranych kontraktów projektu ma zaległości typu **Gotowe do fakturowania** datowane przed dzisiejszą datą. Na bazie tych kontraktów system tworzy projekt faktury proforma. Jeśli kontrakt dotyczący projektu ma wielu klientów, dla każdego klienta zostanie utworzona faktura, a wiele faktur zostanie utworzonych na kontrakt projektu.

Wszystkie utworzone faktury projektu są dostępne na stronie **Faktura** w sekcji **Fakturowanie** w obszarze **Sprzedaż**.

## <a name="project-contract-details-page"></a>Strona szczegółów Kontraktu projektu

Fakturę proforma można również utworzyć na stronie szczegółów **Kontrakt projektu**. System weryfikuje, czy umowa w sprawie projektu zawiera zaległości typu **Gotowe do fakturowania** datowane przed dzisiejszą datą. Na bazie tychże kontraktów system tworzy faktury proforma w wersji roboczej na podstawie liczby klientów w każdej pozycji kontraktu.

W przypadku utworzenia jednej faktury proforma zostanie otwarta strona **Faktura**. Jeśli dla tej umowy dotyczącej projektu zostanie utworzonych wiele faktur, zostanie otwarta strona z listą **Faktur**, na której będą widoczne wszystkie utworzone faktury.
