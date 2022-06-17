---
title: Przejścia stanów na fakturze od dostawcy
description: W tym artykule wyjaśniono przejścia stanów na fakturze od dostawcy w Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 03/30/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 58b07322fb6480fdeb07eb867a7aabc0eff7b955
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8934333"
---
# <a name="state-transitions-on-a-vendor-invoice"></a>Przejścia stanów na fakturze od dostawcy

[!include [banner](../../includes/dataverse-preview.md)]

_**Zastosowane w:** Wdrażanie uproszczone — od okazji do faktury pro forma_

W tym artykule wyjaśniono przejścia stanów na fakturze od dostawcy w Microsoft Dynamics 365 Project Operations. Używane są następujące stany: **Wersja robocza**, **W przeglądzie**, **Potwierdzenie**, **Wstrzymanie** i **Anulowano**.

Poniższe ilustracje przedstawiają przejścia między stanami.

![Model przejścia stanu podwykonawstwa.](../media/VI_State_Model.jpg)

W poniższej tabeli wyjaśniono, jakie poszczególne stany reprezentują w cyklu życia faktury dostawcy w Project Operations.

| State | Description | Dozwolone przejścia |
| --- | --- | --- |
| Wersja robocza | Ten stan jest stanem początkowym faktury dostawcy. Linie i ceny mogą ulec zmianie. Fakturę dostawcy w tym stanie można edytować i usuwać. | W toku |
| W trakcie przeglądu | Ten stan reprezentuje stan przetwarzania faktury dostawcy. Co najmniej jedna wiersz faktury dostawcy ma stan weryfikacji **w toku**. | Potwierdzone, Wstrzymane |
| Potwierdzone | Ten stan reprezentuje etap faktury dostawcy, na którym aplikacja utworzyła wartości rzeczywiste kosztów dla każdego wiersza faktury dostawcy. Wszystkie połączone wartości rzeczywiste kosztów, które zostały dopasowane do wierszy faktur dostawcy, zostały wycofane i zastąpione wartościami rzeczywistymi kosztów z tych wierszy faktury dostawcy. Fakturę dostawcy w tym stanie nie można edytować ani usuwać. Przycisk **Anuluj** można wykorzystać do anulowania potwierdzonej faktury dostawcy. Akcja Anuluj cofa wpływ akcji Potwierdzenie. | Anulowane |
| Wstrzymano | <p>Ten stan reprezentuje etap faktury dostawcy, na którym nie można przenieść faktury dostawcy z powodu problemu z fakturą lub stanem dostawcy. Faktury od dostawcy w tym stanie nie można potwierdzić, anulować, edytować ani usunąć.</p><p>Akcji Ponowne otwieranie można użyć do przeniesienia faktury dostawcy do stanu **Wersja robocza** lub **W przeglądzie**. Jeśli co najmniej jeden wiersz na fakturze dostawcy ma stan weryfikacji **W toku** lub **Ukończony**, faktura dostawcy zostanie ponownie otwarta w stanie **Przeglądu**. Jeśli wszystkie wiersze na fakturze dostawcy mają stan weryfikacji **Nie rozpoczęto**, faktura dostawcy zostanie ponownie otwarta w stanie **Wersja robocza**.</p> | Wersja robocza, W przeglądzie |
| Anulowane | Ten stan reprezentuje etap podwykonawstwa, na którym nie jest już wymagana rzeczywista dostawa materiałów i/lub pracy przez zasoby zlecone podwykonawcom. Umowy podwykonawczej w tym stanie nie można używać do szacowania i zatrudniania wymagań projektu dotyczących zasobów i materiałów, a także nie można odwoływać się do czasu, kosztów i zużycia materiałów w projekcie. Umowy podwykonawczej w tym stanie nie można edytować ani usunąć. | None |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
