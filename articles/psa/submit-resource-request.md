---
title: Przesyłanie żądania zasobu
description: W tym temacie zamieszczono informacje dotyczące przesyłania wniosku o zasób do projektu.
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 12/1/2018
ms.topic: article
author: JohnPBurrows
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 50f076b89c5ac7fee4866534cbd47d81f92f3ab3
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/28/2020
ms.locfileid: "4131293"
---
# <a name="submitting-a-resource-request"></a>Przesyłanie żądania zasobu

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Wygenerowane wymaganie zasobu można przesłać jako żądanie zasobu. Żądanie jest następnie wysyłane do menedżera zasobów w celu zrealizowania.

1. W usłudze Project Service Automation (PSA) na stronie **Projekty** kliknij kartę **Zespół**, aby wyświetlić listę zasobów możliwych do zarezerwowania. 
2. Z listy wybierz zasób ogólny, który ma wymaganie zasobu, a następnie kliknij opcję **Prześlij żądanie**.

![Przesyłanie żądania zasobu](media/RM-how-to-18.png)

Stan żądania o ogólnego członka zespołu zmieni się na **"Przesłano**.

Gdy menedżer zasobów zrealizuje żądanie, ogólny zasób zostanie zastąpiony nazwanym zasobem, jeśli menedżer zasobów zrealizował żądanie poprzez zarezerwowanie nazwanego zasobu. W przeciwnym razie zasób ogólny pozostanie w zespole, a stan żądania zmieni się na **Wymaga przeglądu**, jeśli menedżer zasobów zaproponował nazwany zasób.
