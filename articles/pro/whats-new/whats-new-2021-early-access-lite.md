---
title: Co nowego w drugim wydaniu aktualizacji na 2021 r. z wczesnym dostępem — wdrażanie aplikacji Project Operations w wersji uproszczonej
description: Ten artykuł zawiera informacje o funkcjach dostępnych w wydaniu Project Operations — wersja uproszczona w lutym 2021 r., 2. aktualizacja z wczesnym dostępem.
author: sigitac
ms.date: 08/10/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: d245868c8bd9ff332707a81c074d6c7ae3649378
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8924121"
---
# <a name="whats-new-2021-wave-2-early-access---project-operations-lite-deployment"></a>Co nowego w drugim wydaniu aktualizacji na 2021 r. z wczesnym dostępem — wdrażanie aplikacji Project Operations w wersji uproszczonej

_Zastosowane do: Wdrażanie uproszczone — od okazji do faktury pro forma_

Ten artykuł dotyczy następujących składników i wersji oprogramowania Dynamics 365 Project Operations:

  - Project Operations w środowisku Dataverse w wersji 4.23.0.4

Wydanie jest stosowane tylko wtedy, gdy środowisko [zostanie uwzględnione w opcji wczesnego dostępu](/power-platform/admin/opt-in-early-access-updates#how-to-enable-early-access-updates).

## <a name="features-included-in-this-release"></a>Funkcje uwzględnione w tym wydaniu

[Zarządzanie podumowami](/dynamics365/project-operations/pro/subcontracting/managing-subcontracts-overview) — ta funkcja zapewnia lepszą widoczność i kontrolę nad wszystkimi aspektami pracy nad projektem. Wersja zapoznawcza zarządzania kontraktami podumowami zawiera następujące możliwości:

  - Menedżer projektu może utworzyć podumowę z dostawcą. Domyślnie dla umowy podwykonawczej używane są cenniki dołączone do rekordu dostawcy. Konto dostawcy ma typ relacji **Dostawca** lub **Dostawca (producent)**.
  - Menedżer projektu może wyszczególnić wszystkie zakupy jako pozycje w podumowie. Wiersze podwykonawstwa mogą dotyczyć czasu, wydatków lub produktów. Klasa transakcji w pozycji podumowy określa, do czego służy wiersz.
  - Menedżer klienta dostawcy i kierownik projektu mogą iterować po umowie podwykonawczej. Ceny można dostosować w cennikach zakupu dołączonych do umowy podwykonawczej.
  - Podczas procesu, jeśli wiersz podumowy dotyczy czasu, menedżer ds. klienta dostawcy może skojarzyć kontakty dostawcy z każdym wierszem podumowy. To stowarzyszenie dostarcza informacji kierownikowi projektu, który pracuje nad umową podwykonawczą. Gdy kontakt dostawcy jest skojarzony z pozycją podumowy, system automatycznie tworzy zasób, który można zarezerwować, na podstawie kontaktu, jeśli zasób, który można zarezerwować, jeszcze nie istnieje.
  - Metodą rozliczania dla każdego wiersza podumowy może być stała cena lub czas i materiały. W przypadku pozycji podumowy o stałej cenie jest konfigurowany harmonogram faktur oparty na kamieniach milowych.
