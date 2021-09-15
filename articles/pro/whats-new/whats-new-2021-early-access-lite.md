---
title: Co nowego w drugim wydaniu aktualizacji na 2021 r. z wczesnym dostępem — wdrażanie aplikacji Project Operations w wersji uproszczonej
description: To temat zawiera informacje o funkcjach dostępnych w drugim wydaniu wdrożenia wersji uproszczonej aplikacji Project Operations z 2021 r.
author: sigitac
ms.date: 08/10/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: a201e3e4333b8892eea72387222d64e18b74d71b
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323924"
---
# <a name="whats-new-2021-wave-2-early-access---project-operations-lite-deployment"></a>Co nowego w drugim wydaniu aktualizacji na 2021 r. z wczesnym dostępem — wdrażanie aplikacji Project Operations w wersji uproszczonej

_Zastosowane do: Wdrażanie uproszczone — od okazji do faktury pro forma_

Ten temat dotyczy następujących składników i wersji aplikacji Dynamics 365 Project Operations:

  - Project Operations w środowisku Dataverse w wersji 4.23.0.4

Wydanie jest stosowane tylko wtedy, gdy środowisko [zostanie uwzględnione w opcji wczesnego dostępu](/power-platform/admin/opt-in-early-access-updates#how-to-enable-early-access-updates).

## <a name="features-included-in-this-release"></a>Funkcje uwzględnione w tym wydaniu

[Zarządzanie podumowami](../subcontracting/subcontracting_EA_scope.md) — ta funkcja zapewnia lepszą widoczność i kontrolę nad wszystkimi aspektami pracy nad projektem. Wersja zapoznawcza zarządzania kontraktami podumowami zawiera następujące możliwości:

  - Menedżer projektu może utworzyć podumowę z dostawcą. Domyślnie dla umowy podwykonawczej używane są cenniki dołączone do rekordu dostawcy. Konto dostawcy ma typ relacji **Dostawca** lub **Dostawca (producent)**.
  - Menedżer projektu może wyszczególnić wszystkie zakupy jako pozycje w podumowie. Wiersze podwykonawstwa mogą dotyczyć czasu, wydatków lub produktów. Klasa transakcji w pozycji podumowy określa, do czego służy wiersz.
  - Menedżer klienta dostawcy i kierownik projektu mogą iterować po umowie podwykonawczej. Ceny można dostosować w cennikach zakupu dołączonych do umowy podwykonawczej.
  - Podczas procesu, jeśli wiersz podumowy dotyczy czasu, menedżer ds. klienta dostawcy może skojarzyć kontakty dostawcy z każdym wierszem podumowy. To stowarzyszenie dostarcza informacji kierownikowi projektu, który pracuje nad umową podwykonawczą. Gdy kontakt dostawcy jest skojarzony z pozycją podumowy, system automatycznie tworzy zasób, który można zarezerwować, na podstawie kontaktu, jeśli zasób, który można zarezerwować, jeszcze nie istnieje.
  - Metodą rozliczania dla każdego wiersza podumowy może być stała cena lub czas i materiały. W przypadku pozycji podumowy o stałej cenie jest konfigurowany harmonogram faktur oparty na kamieniach milowych.
