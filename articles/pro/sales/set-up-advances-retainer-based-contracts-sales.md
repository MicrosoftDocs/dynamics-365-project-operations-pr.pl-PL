---
title: Kontrakty oparte na zaliczkach i zatrzymaniach
description: Ten temat zawiera informacje na temat modeli kontraktowania opartych na zatrzymaniach lub zaliczkach w Project Operations.
author: rumant
ms.date: 10/20/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 87e275cb72f1edc5a2a9913b4aa47d461d1f3d3d9bf177bf0ffba8b463f4ce01
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/06/2021
ms.locfileid: "6994424"
---
# <a name="advances-and-retainer-based-contracts"></a>Kontrakty oparte na zaliczkach i zatrzymaniach


_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_

Aplikacja Dynamics 365 Project Operations obsługuje kontrakty oparte na zatrzymaniach. Kontrakt oparty na zatrzymania jest wynegocjowanym zestawem równych płatności, które będą zafakturowane klientowi w czasie trwania projektu. Ten typ kontraktu jest zwykle używany w przypadku modeli fakturowania typu czas i materiały lub modelach rozliczania opartych na zużyciu, w przypadku których istnieje konieczność nadania klientowi prognozowanego harmonogramu fakturowania i płatności. Rzeczywiste przychody za każdy okres są uzgadniane względem płatności otrzymanej od klienta na początku okresu. W zależności od koncepcji modelu fakturowania czasu i materiału wartości przychodów naliczane w każdym okresie mogą być różne od poniesionych kosztów. Jeśli naliczany przychód wynosi więcej niż przyjęta kwota na początku okresu, firma dostarczająca projekt może:

- Wystawić klientowi fakturę za kwotę ponad limit 
- Odroczyć uzgodnienie przychodu do następnego okresu fakturowania, a następnie wykonać jedną końcową fakturę na końcu projektu w odniesieniu do pozostałych nieuzgodnionych przychodów

Główna różnica między modelem kontraktu opartego na zatrzymaniu i modelem kontraktu o stałej cenie w Project Operations polega na tym, że w modelu kontraktu o stałej cenie kwota faktury nie jest powiązana z kosztami poniesionymi. Fakturowanie wynika z podejścia opartego na punktach kontrolnych, które jest wyrównane do kosztów poniesionych za dany okres. W kontrakcie opartym na zatrzymaniu przychód, który można zafakturować, jest rejestrowany na podstawie metody fakturowania w pozycji kontraktu. Kiedy metodą fakturowania jest czas i materiały, przychód fakturowany jest związany z kosztami poniesionymi w danym okresie i może być różny w poszczególnych okresach. Jednak klient jest zafakturowany tylko w odniesieniu do kwoty w ramach okresowego przytrzymania. System używa na koniec okresu innej faktury, aby uzgodnić zafakturowany przychód zarejestrowany w okresie względem kwoty zafakturowanej dla klienta na początku okresu.

Korzystanie z tej metody polega na tym, że koszty klienta stają się przewidywalne w harmonogramie programu do przechowywania w sposób różny od typowego modelu czasu i materiałów. Organizacja dostarczająca projektu ponosi w pewnym zakresie ryzyko odzyskania kosztów poniesionych z powodu jakichkolwiek zmian w zakresie projektu, w przypadku których model ceny ustalonej nie zezwoliłby na taką sytuację.

Poza okresowym harmonogramem zatrzymań Project Operations mogą polegać na jednorazowym zarejestrowaniu z klienta i uzgodnieniu z różnymi składnikami kosztów projektów.

Operacja zatrzymania w Project Operations jest niedostępna do momentu zafakturowania klienta. Jest to wskazane w poniższych polach w podsiatce dla zaliczek i zatrzymań.

| Pole | Opis | Wpływ zmian w dalszych etapach |
| --- | --- | --- |
| Dostępna kwota | Kwota, która jest dostępna do użycia w odniesieniu do rekordu zatrzymania lub zaliczki. | Do momentu zafakturowania zaliczki lub zatrzymania nie będzie można tego korzystać, co oznacza, że dostępna kwota będzie wynosić zero. |
| Kwota użyta | Kwota, która jest już użyta w odniesieniu do rekordu zatrzymania lub zaliczki. | Zaliczka lub zatrzymanie na fakturze z kosztami rzeczywistymi, które będą stanowić część oznaczoną jako już wykorzystana lub zużyta, może zostać częściowo uzgodniona. Pozostała część kwoty zaliczki lub zatrzymania jest dostępna do uzgodnienia na przyszłej fakturze z kosztami rzeczywistymi. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]