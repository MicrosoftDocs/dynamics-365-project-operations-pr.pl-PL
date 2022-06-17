---
title: Wartości rzeczywiste
description: W tym artykule podano informacje na temat pracy z wartościami rzeczywistymi w aplikacji Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 02/22/2022
ms.topic: overview
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.assetid: ''
ms.search.region: ''
ms.search.industry: ''
ms.author: rumant
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 2551b7d6d20df170c913e302e734583135265529
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8924811"
---
# <a name="actuals"></a>Wartości rzeczywiste

_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_

Dane rzeczywiste reprezentują sprawdzony i zatwierdzony postęp finansowy i harmonogram projektu. Są one tworzone w momencie zatwierdzenia pozycji czasu, wydatków i użycia materiałów, wpisy i faktury.

> [!IMPORTANT]
> Nie należy edytować ani usuwać wartości rzeczywistych z systemu. W przeciwnym razie integralność finansowa i integracja z innymi systemami finansowymi i księgowymi może mieć niekorzystny wpływ na spójność. Microsoft Dynamics 365 Project Operations umożliwia zamianę i zamianę wartości rzeczywistych na potrzeby edycji wartości rzeczywistych w różnych punktach cyklu życia procesu biznesowego projektów.

## <a name="recording-actuals-based-on-project-events"></a>Rejestrowanie wartości rzeczywistych na podstawie zdarzeń projektu

Project Operations rejestruje wartości rzeczywiste transakcji finansowych, które występują w cyklu życia zobowiązania w ramach projektu. Tworzenie wartości rzeczywistych w różnych zdarzeniach w cyklu życia zależy od tego, czy w ramach zobowiązania w ramach projektu jest używany model rozliczania czasu i materiałów, czy modelu rozliczania stałej ceny, oraz od tego, czy jest to etap przed sprzedażą, czy projekt wewnętrzny.

W poniższych artykułach przedstawiono wpływ tabeli wartości rzeczywistych na różne zdarzenia dla różnych odmian:

- [Wartości rzeczywiste mają wpływ na czas i zaangażowanie materiałów](ActualsonTM.md)
- [Wartości rzeczywiste mają wpływ na zaangażowanie w stałą cenę](ActualonFP.md)
- [Wartość rzeczywista ma wpływ na etapie przed sprzedażą zobowiązania](ActualonPreSales.md)
- [Rzeczywisty wpływ na projekt wewnętrzny](ActualonInternal.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
