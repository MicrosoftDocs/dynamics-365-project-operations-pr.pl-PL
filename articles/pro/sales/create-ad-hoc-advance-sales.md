---
title: Tworzenie przedpłaty ad hoc w kontrakcie — wersja uproszczona
description: W tym temat zamieszczono informacje dotyczące tworzenia zaliczki na temat kontraktu w zależności od potrzeb.
author: rumant
manager: Annbe
ms.date: 10/26/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: a6bf02c2e2ab2f3c696b1eab1b92a20272187bf5
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/31/2020
ms.locfileid: "4181375"
---
# <a name="creating-an-ad-hoc-advance-on-a-contract---lite"></a>Tworzenie przedpłaty ad hoc w kontrakcie — wersja uproszczona

_**Zastosowane w:** Wdrażanie uproszczone — od okazji do faktury pro forma_

Microsoft Dynamics 365 Project Operations jest obsługiwany w scenariuszach fakturowania obejmujących przede wszystkim płatności i nadpłaty. Proces korzystania z **Zaliczek** w **Project Operations** przypomina kontrakty **Zatrzymania**. 

Wykonaj poniższe kroki, aby zafakturować klienta z zaliczą na poczet oferty.

1. Przejdź do strony **Kontrakt projektu**, a następnie wybierz kartę **Zatrzymania i zaliczki**.
2. W podsiatce z listą wszystkich poprzednio nagranych przedpłat i przedpłat wybierz pozycję **+ Podpowiedź nowego kontraktu dotyczącego projektu**. 

    Zostanie otwarty formularz **Szybkie tworzenie** w celu zarejestrowania przedpłaty lub wcześniejszej płatności.
    
3. W poniższej tabeli wymieniono pola umożliwiające rejestrowanie zaliczki oraz kwestie, które należy uwzględnić podczas tworzenia nowych elementów:

    | Pole | Opis | Wpływ zmian w dalszych etapach |
    | --- | --- | --- |
    | **Klient kontraktu projektu** | To pole wskazuje nabywcę objęty kontraktem, który ma być wystawiony na fakturę zaliczkową. | Jeśli w kontrakcie znajduje się wielu klientów i zachodzi konieczność zafakturowania każdego z nich dla określonego oddziału lub kwoty zaliczki, należy utworzyć zaliczki osobno dla każdego klienta. |
    | **Opis** | Opis celu lub chronometrażu wyprzedzenia ułatwiający identyfikację tej zaliczki. | Ten opis jest wyświetlany w wierszu faktury dotyczącym tej wypłaty. |
    | **Kwota** | Kwota przed zapłatą lub zaliczką. | Ta suma jest wyświetlana w wierszu faktury dotyczącym tej wypłaty. |
    | **Data faktury** | Data zafakturowania zaliczki na klienta. | Jest to data automatycznej operacji tworzenia faktury w celu utworzenia wiersza faktury dla tej zaliczky. |
    | **Stan faktury** | Jest to ustawienie opcji, które wskazuje, czy ta zaliczka jest dodawana do wersji roboczej faktury danego klienta. Możliwe wartości to:</br>- **Nieprzygotowane do fakturowania**</br>- **Przygotowane do fakturowania** | Jeśli zaliczkowa lub przedpłata jest oznaczona jako **Przygotowane do fakturowania**, jest dodawana jako wiersz dla wersji roboczej na fakturze. Do uzgodnienia kosztów projektu z kolejnym okresem faktury można użyć tylko całkowicie zafakturowanej zaliczki. |

4. Wybierz opcję **Zapisz i Zamknij** w oknie dialogowym szybkie tworzenie, aby zarejestrować zaliczkę lub przedpłatę przed realizacją.
