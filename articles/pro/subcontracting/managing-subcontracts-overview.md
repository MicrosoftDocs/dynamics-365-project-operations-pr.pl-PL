---
title: Zarządzanie podumowami w rozwiązaniu Project Operations
description: Ten temat zawiera omówienie procesu kompleksowego zarządzania umowami podwykonawstwa w Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 08/02/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 6ffceb0886fdc841ea01a099243cf4eeb43e5374a18414576f3639a3e50857fd
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/06/2021
ms.locfileid: "6994244"
---
# <a name="subcontract-management-in-project-operations"></a>Zarządzanie podumowami w rozwiązaniu Project Operations

[!include [banner](../../includes/dataverse-preview.md)]

_**Zastosowane w:** Wdrażanie uproszczone — od okazji do faktury pro forma_

Podwykonawstwo w Microsoft Dynamics 365 Project Operations obsługuje następujący przepływ procesów biznesowych.

![Przepływ procesu podrzędnego](../media/SubcontractingProcessFlow.png)

Oto szczegółowy opis procesu podwykonawstwa.

1. Kierownik projektu tworzy umowę podwykonawczą z dostawcą. Domyślnie dla umowy podwykonawczej używane są cenniki dołączone do rekordu dostawcy. Konto dostawcy ma typ relacji **Dostawca** lub **Dostawca (producent)**.
2. Kierownik projektu może wyszczególnić wszystkie zakupy jako pozycje w umowie podwykonawczej. Wiersze podwykonawstwa mogą dotyczyć czasu, wydatków lub produktów. Klasa transakcji wybrana w każdym wierszu umowy podwykonawczej określa, do czego służy wiersz.
3. Menedżer klienta dostawcy i kierownik projektu mogą iterować po umowie podwykonawczej. Ceny można dostosować w cennikach zakupu dołączonych do umowy podwykonawczej.
4. Na tym lub późniejszym etapie procesu, jeśli wiersz umowy podwykonawczej dotyczy czasu, kierownik ds. klienta dostawcy kojarzy kontakty z każdym wierszem umowy podwykonawczej. To stowarzyszenie dostarcza informacji kierownikowi projektu, który pracuje nad umową podwykonawczą. Gdy kontakt jest skojarzony z wierszem umowy podwykonawczej, system automatycznie tworzy zasób, który można zarezerwować, na podstawie kontaktu, jeśli zasób, który można zarezerwować, jeszcze nie istnieje.
5. Metodą rozliczania dla każdego wiersza podwykonawcy może być **Cena stała** lub **Godziny i Materiały**. W przypadku wierszy z podwykonawcami o stałej cenie można skonfigurować harmonogram faktur oparty na kamieniach milowych.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
