---
title: Wartości rzeczywiste
description: Ten temat zawiera informacje dotyczące pracy z wartościami rzeczywistymi w rozwiązaniu Microsoft Dynamics 365 Project Operations.
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
ms.openlocfilehash: 3f0cb8c478e2ce6fba589d51d95649f53f62e883
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/14/2022
ms.locfileid: "8581297"
---
# <a name="actuals"></a>Wartości rzeczywiste

_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_

Dane rzeczywiste reprezentują sprawdzony i zatwierdzony postęp finansowy i harmonogram projektu. Są one tworzone w momencie zatwierdzenia pozycji czasu, wydatków i użycia materiałów, wpisy i faktury.

> [!IMPORTANT]
> Nie należy edytować ani usuwać wartości rzeczywistych z systemu. W przeciwnym razie integralność finansowa i integracja z innymi systemami finansowymi i księgowymi może mieć niekorzystny wpływ na spójność. Microsoft Dynamics 365 Project Operations umożliwia zamianę i zamianę wartości rzeczywistych na potrzeby edycji wartości rzeczywistych w różnych punktach cyklu życia procesu biznesowego projektów.

## <a name="recording-actuals-based-on-project-events"></a>Rejestrowanie wartości rzeczywistych na podstawie zdarzeń projektu

Project Operations rejestruje wartości rzeczywiste transakcji finansowych, które występują w cyklu życia zobowiązania w ramach projektu. Tworzenie wartości rzeczywistych w różnych zdarzeniach w cyklu życia zależy od tego, czy w ramach zobowiązania w ramach projektu jest używany model rozliczania czasu i materiałów, czy modelu rozliczania stałej ceny, oraz od tego, czy jest to etap przed sprzedażą, czy projekt wewnętrzny.

W poniższych tematach przedstawiono wpływ tabeli wartości rzeczywistych na różne zdarzenia dla różnych odmian:

- [Wartości rzeczywiste mają wpływ na czas i zaangażowanie materiałów](ActualsonTM.md)
- [Wartości rzeczywiste mają wpływ na zaangażowanie w stałą cenę](ActualonFP.md)
- [Wartość rzeczywista ma wpływ na etapie przed sprzedażą zobowiązania](ActualonPreSales.md)
- [Rzeczywisty wpływ na projekt wewnętrzny](ActualonInternal.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
