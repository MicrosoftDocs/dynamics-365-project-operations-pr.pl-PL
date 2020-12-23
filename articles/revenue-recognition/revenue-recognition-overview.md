---
title: Omówienie rozpoznawania przychodów
description: W tym temacie zamieszczono informacje dotyczące rozpoznawania przychodów w aplikacji Project Operations.
author: sigitac
manager: Annbe
ms.date: 11/16/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 6844f4c5d4cda8a6a901b0302448f70f4c597f5d
ms.sourcegitcommit: 2d399bc9d07807626f0d6b2d0cf304240c47591c
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 11/17/2020
ms.locfileid: "4531512"
---
# <a name="revenue-recognition-overview"></a>Omówienie rozpoznawania przychodów

_**Zastosowane do:** Project Operations dla zasobów/scenariuszy nieopartych na zaopatrzeniu_

W aplikacji Dynamics 365 Project Operations zasady rozpoznawania przychodów różnią się w zależności od wybranej metody fakturowania dla projektu lub części projektu. W tym temacie zamieszczono informacje dotyczące rozpoznawania przychodów w aplikacji Project Operations.

## <a name="transactions-accounted-using-time-and-material-billing-method"></a>Transakcje rozliczane za pomocą metody rozliczania transakcji czasu i materiałów

- Funkcje rozpoznawania kosztów i przychodów są połączone. Koszt transakcji i sprzedaż nierozliczona są księgowane przy użyciu [arkusza integracja aplikacji Project Operations](../project-accounting/project-operations-integration-journal.md).
- Koszty projektu i profil przychodów określają, czy nierozliczone transakcje sprzedaży są księgowane w księdze głównej. Jeśli wybrano pozycję **Przychód naliczony**, system używa kont **Wartość sprzedaży PWT** i **Wartość sprzedaży naliczonego przychodu** podczas księgowania. Poniżej znajduje się przykład tej metody.  

  | Typ transakcji | Obciążenie/uznanie | Kwota |
  | --- | --- | --- |
  | Wartość sprzedaży PWT | Obciążenie | 100 |
  | Wartość sprzedaży naliczonego przychodu | Uznanie | 100 |

- Przychód jest rozpoznawany podczas fakturowania. System używa konta **Zafakturowany przychód** podczas księgowania. Poniżej znajduje się przykład tej metody.  

  | Typ transakcji | Obciążenie/uznanie | Kwota |
  | --- | --- | --- |
  | Saldo klienta | Obciążenie | 120 |
  | Podatek do zapłacenia | Uznanie | 20 |
  | Zafakturowany przychód | Uznanie | 100 |

- Jeśli przychód został naliczony podczas księgowania sprzedaży nierozliczonej, system wycofa przychód naliczony przy fakturowaniu.

  | Typ transakcji | Obciążenie/uznanie | Kwota |
  | --- | --- | --- |
  | Wartość sprzedaży PWT | Uznanie | 100 |
  | Wartość sprzedaży naliczonego przychodu | Obciążenie | 100 |

## <a name="transactions-accounted-using-the-fixed-price-billing-method"></a>Transakcje rozliczane za pomocą metody rozliczania transakcji o stałej cenie

- Funkcje rozpoznawania kosztów i przychodów są rozdzielone. Koszt transakcji jest księgowany przy użyciu [arkusza integracja aplikacji Project Operations](../project-accounting/project-operations-integration-journal.md). Nierozliczone transakcje sprzedaży nie są tworzone.
- Przychód można rozpoznać podczas fakturowania, jeśli koszty projektu i profil przychodów mają **zasadę używaną do obliczeń wykonania projektu** ustawioną na **Brak PWT**. Używaj tej metody tylko dla krótkoterminowych, prostych projektów.
- Przychody można rozpoznać przy użyciu szacowanych przychodów o stałej cenie za pomocą metody **Kontrakt ukończony** lub **Procent ukończenia — rozpoznawanie przychodów**.

## <a name="additional-resources"></a>Dodatkowe zasoby
[Konfigurowanie księgowania projektów do zafakturowania (artykuł)](../project-accounting/configure-accounting-billable-projects.md)

[Szacowane projekty przychodów o stałej cenie](rev-rec-percentage-completion-method.md)

[Zarządzanie szacowaniami przychodów](rev-rec-completed-contract-method.md)

[Metody dotyczące kosztów wykonania](cost-complete-methods.md)
