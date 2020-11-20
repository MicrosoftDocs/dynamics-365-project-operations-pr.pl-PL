---
title: Tworzenie ręcznej faktury proforma - wersja uproszczona
description: Ta temat zawiera informacje na temat tworzenia ręcznej faktury proforma w Project Operations.
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 87ef090454b2a7ab997e7c21d8d10badc31c8235
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/30/2020
ms.locfileid: "4176399"
---
# <a name="create-a-manual-proforma-invoice---lite"></a>Tworzenie ręcznej faktury proforma - wersja uproszczona

_**Zastosowane w:** Wdrażanie uproszczone — od okazji do faktury pro forma_

W przypadku Dynamics 365 Project Operations faktury proforma mogą być tworzone ręcznie. Fakturę proforma można utworzyć ręcznie na stronie list **Kontraktów projektu** lub na stronie szczegółów **Kontraktów projektu**.

##  <a name="project-contracts-list-page"></a>Strona list Kontraktów projektu

Z poziomu strony listy **Kontraktów projektu** wybierz co najmniej jeden kontrakt projektu i utwórz faktury dla wszystkich wybranych rekordów.

System sprawdzi, który z wybranych kontraktów projektu ma zaległości typu **Gotowe do fakturowania** datowane przed dzisiejszą datą. Na bazie tych kontraktów system tworzy projekt faktury proforma. Jeśli kontrakt dotyczący projektu ma wielu klientów, dla każdego klienta zostanie utworzona faktura, a wiele faktur zostanie utworzonych na kontrakt projektu.

Wszystkie utworzone faktury projektu są dostępne na stronie **Faktura** w sekcji **Fakturowanie** w obszarze **Sprzedaż**.

## <a name="project-contract-details-page"></a>Strona szczegółów Kontraktu projektu

Fakturę proforma można również utworzyć z poziomu strony szczegółów **Kontraktu projektu**, co utworzy fakturę dla tego konkretnego kontraktu dotyczącego projektu. System weryfikuje, że wybrany kontrakt projektu ma zaległości typu **Gotowe do fakturowania** datowane przed dzisiejszą datą. Na bazie tychże kontraktów system tworzy faktury proforma w wersji roboczej na podstawie liczby klientów w każdej pozycji kontraktu.

W przypadku utworzenia jednej faktury proforma zostanie otwarta strona **Faktura**. Jeśli dla danego kontraktu projektu utworzono wiele faktur, zostanie wyświetlona strona z listą **Faktur**, która wyświetli wszystkie utworzone faktury.
