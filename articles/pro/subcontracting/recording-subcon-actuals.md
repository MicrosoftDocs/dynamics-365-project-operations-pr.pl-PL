---
title: Rejestrowanie czasu, wydatków i użycia materiałów w przypadku składników podwykonawców
description: W tym artykule wyjaśniono, w jaki sposób czas, koszty i materiały zarejestrowane w projektach z poszczególnych składników podumowy są śledzone w aplikacji Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 1c05b941fb51c8b56422e3b5d3868c9b69197187
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8927663"
---
# <a name="recording-time-expenses-and-material-usage-on-projects-for-subcontracted-components"></a>Rejestrowanie czasu, wydatków i użycia materiałów dla projektów w przypadku składników podwykonawców

[!include [banner](../../includes/dataverse-preview.md)]

_**Zastosowane w:** Wdrażanie uproszczone — od okazji do faktury pro forma_

W tym artykule wyjaśniono, w jaki sposób czas, koszty i materiały zarejestrowane w projektach z poszczególnych składników podumowy są śledzone w aplikacji Microsoft Dynamics 365 Project Operations.

## <a name="costing-for-subcontractor-time-on-projects"></a>Wycena czasu podwykonawców w ramach projektów
W aplikacji Project Operations pracownicy kontraktowi mogą rejestrować czas w projektach w podobny sposób jak pracownicy. Podczas wprowadzania czasu w projektach i/lub zadaniach projektów pracownik kontraktowy może wybrać określoną podumowę i pozycję podumowy.

Po zatwierdzeniu czasu przesłanego przez pracowników kontraktowych koszt projektu jest rejestrowany przy użyciu kosztu jednostkowego skonfigurowanego dla tego zasobu pracownika kontraktowego w sekcji **Ceny ról** cen zakupu w ramach podumowy.

## <a name="costing-for-subcontracted-expenses-on-projects"></a>Wycena wydatków podwykonawców w ramach projektów
Podczas wprowadzania wydatków ponoszonych w ramach projektów można wybrać podumowę i pozycję podumowy we wpisie wydatku. 

Po przesłaniu i zatwierdzeniu tego wpisu wydatku koszt wydatku jest rejestrowany w projekcie w oparciu o koszt jednostkowy skonfigurowany dla tej kategorii transakcji w sekcji **Ceny kategorii** cennika zakupu w ramach podumowy.

## <a name="costing-for-subcontracted-materials-on-projects"></a>Wycena materiałów podwykonawców w ramach projektów
Podczas wprowadzania użycia materiałów w ramach projektów można wybrać podumowę i pozycję podumowy w dzienniku użycia materiałów. Po przesłaniu i zatwierdzeniu dziennika użycia materiału koszt materiału jest rejestrowany w projekcie w oparciu o koszt jednostkowy skonfigurowany dla tego produktu w sekcji **Pozycje cennika** dla cennika podumowy.

Użycie materiałów może być również rejestrowane dla produktów dopisanych w projektach. Ten typ użycia materiałów można również połączyć z podumową lub pozycją podumowy. Podczas rejestrowania użycia materiałów dla produktów dopisanych należy wprowadzić jednostkowy koszt produktu dopisanego. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
