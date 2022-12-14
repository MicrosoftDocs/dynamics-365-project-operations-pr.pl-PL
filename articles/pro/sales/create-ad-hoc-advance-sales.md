---
title: Tworzenie przedpłaty ad hoc w kontrakcie projektu
description: W tym artykule podano informacje na temat tworzenia przedpłaty w kontrakcie.
author: rumant
ms.date: 10/26/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 62e41e5faeb5e40143e26e2cdf48c1279941a6b4
ms.sourcegitcommit: e0cbbe7c6f03d4978134405cf04bd8bc1d019f65
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/05/2022
ms.locfileid: "9824875"
---
# <a name="create-an-ad-hoc-advance-on-a-project-contract"></a>Tworzenie przedpłaty ad hoc w kontrakcie projektu

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
