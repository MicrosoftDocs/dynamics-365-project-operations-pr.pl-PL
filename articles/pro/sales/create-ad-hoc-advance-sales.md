---
title: Tworzenie zaliczki ad hoc w kontrakcie
description: W tym temat zamieszczono informacje dotyczące tworzenia zaliczki na temat kontraktu w zależności od potrzeb.
author: rumant
ms.date: 10/26/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: bceed1372dbaf523426a4c34da7152d77fe108240c8c3e4e1390c43b1cf536a4
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/06/2021
ms.locfileid: "6999149"
---
# <a name="creating-an-ad-hoc-advance-on-a-contract"></a>Tworzenie zaliczki ad hoc w kontrakcie

_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_

Aplikacja Microsoft Dynamics 365 Project Operations obsługuje scenariusze fakturowania obejmujące przedpłaty i zaliczki. Proces korzystania z **Zaliczek** w **Project Operations** przypomina kontrakty **Zatrzymania**. 

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


[!INCLUDE[footer-include](../../includes/footer-banner.md)]