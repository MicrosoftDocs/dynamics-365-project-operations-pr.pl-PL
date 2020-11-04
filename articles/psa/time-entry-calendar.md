---
title: Kalendarz wpisów czasu
description: W tym temacie zamieszczono informacje dotyczące używania kalendarza wpisów czasu.
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 05/20/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: afc31609c51f48db61ce359c18707b5a92211082
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082102"
---
# <a name="time-entry-calendar"></a>Kalendarz wpisów czasu

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Na stronie **Wpisy czasu** można przeglądać wpisy czasu istniejące w kalendarzu, wybierając kolejno opcje **Zapisz jako** \> **Formant kalendarza**.

## <a name="updated-calendar-control"></a>Zaktualizowana kontrolka kalendarza

Program Dynamics 365 Project Service Automation oferuje nowy, rozszerzalny mechanizm obsługi wpisów czasu. Ten nowy mechanizm zastępuje kontrolkę kalendarza niestandardowego, która była używana we wcześniejszych wersjach. Można jednak nadal wyświetlać wpisy czasu za pośrednictwem kontrolki kalendarza tylko do odczytu, którą struktura ujednoliconego interfejsu udostępnia dla widoków dziennych, tygodniowych i miesięcznych.

Kalendarz nie obsługuje akcji na poszczególnych elementach kalendarza i nie można zaznaczyć jednego lub więcej elementów kalendarza do przesłania lub usunięcia. Zamiast tego należy zaznaczyć element kalendarza, aby otworzyć stronę encji **Wpis czasu** , gdzie można wykonać wymagane czynności.

## <a name="extensibility"></a>Możliwości rozszerzania

Na stronie **Wpisy czasu** zawierającej siatkę godzin można dodać pola niestandardowe, skonfigurować pola wyszukiwania i utworzyć widoki niestandardowe. Istnieje również możliwość skonfigurowania niestandardowej logiki biznesowej, która jest oparta na wartościach wybranych lub wprowadzonych w polach niestandardowych.
