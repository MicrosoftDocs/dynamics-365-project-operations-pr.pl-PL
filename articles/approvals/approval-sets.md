---
title: Zestawy zatwierdzenia
description: W tym temacie omówiono sposób pracy z zestawami zatwierdzeń, żądaniami i podzestawami tych operacji.
author: stsporen
manager: tfehr
ms.date: 08/10/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 1d9333033eb2b03966c6531d0fd6ad5b878acd93
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323249"
---
# <a name="approval-sets"></a>Zestawy zatwierdzenia

_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_

Zestawy zatwierdzeń grupują żądania zatwierdzenia w mniejsze podzbiory operacji. Takie grupowanie umożliwia przetwarzanie zatwierdzeń według projektu, w określonej kolejności oraz umożliwia ponowne przetwarzanie i sekwencjonowanie. Grupowanie żądań zatwierdzeń poprawia niezawodność i możliwość śledzenia przetwarzania zatwierdzeń w przypadku dużej liczby zatwierdzeń.

Zestawy zatwierdzeń wskazują ogólny stan przetwarzania powiązanych z nimi rekordów. Kiedy rekord zatwierdzenia jest przetwarzany przy użyciu zestawu zatwierdzeń, rekord zmienia stan z **Przesłany** na **Zatwierdzony** i nie jest już połączony z zestawem zatwierdzeń. Jeśli zapis nie powiedzie się podczas przekazywania go do zatwierdzenia, zapis pozostaje w statusie **Przesłany**, a zestaw zatwierdzający jest oznaczony jako nieudany. Zestaw zatwierdzający rejestruje komunikat błędu o niepowodzeniu.

## <a name="processing-approvals-and-approval-sets"></a>Przetwarzanie zatwierdzeń i zestawów zatwierdzeń
Zatwierdzenia oczekujące w kolejce do przetwarzania widoczne są w widoku **Opracowywanie zatwierdzeń**. W systemie wszystkie wpisy są przetwarzane wiele razy asynchronicznie, co obejmuje ponawianie prób, jeśli poprzednie próby zakończyły się niepowodzeniem.

Pole **Próby zatwierdzenia ogółem** określa ilość prób, które pozostały do przetworzenia zestawu, zanim zostanie on oznaczony jako nieudany.

## <a name="failed-approvals-and-approval-sets"></a>Nieudane zatwierdzenia i zestawy zatwierdzeń
Widok **Zatwierdzenia zakończone niepowodzeniem** zawiera listę wszystkich zatwierdzeń wymagających interwencji użytkownika. Otwórz dzienniki powiązanych zestawów zatwierdzeń, aby zidentyfikować przyczynę niepowodzenia.
Wybranie opcji **Ponów próbę** dodaje wartość do licznika prób zestawu zatwierdzeń, przywraca zestawowi zatwierdzeń status **Przetwarzanie** i próbuje przetworzyć pozostałe rekordy.

## <a name="configure-approval-sets"></a>Konfiguracja zestawów zatwierdzeń

### <a name="enable-the-approval-sets-feature"></a>Włączanie funkcji Zestawów zatwierdzających
Przed włączeniem funkcji Zestawy zatwierdzeń należy sprawdzić, czy nie są aktualnie przetwarzane żadne zatwierdzenia.

- Przejdź na stronę **Parametry projektu** i wybierz **Kontrola właściwości** > **Włącz nowe zatwierdzenia**.

### <a name="turn-off-the-approval-sets-feature"></a>Wyłączanie funkcji Zestawów zatwierdzających
Przed wyłączeniem funkcji Zestawy zatwierdzeń należy sprawdzić, czy nie są aktualnie przetwarzane żadne zatwierdzenia.

- Przejdź na stronę **Parametry projektu** i wybierz **Kontrola właściwości** > **Wyłącz nowe zatwierdzenia**.

### <a name="configuring-the-asynchronous-threshold"></a>Konfiguracja progu asynchronicznego 
Podczas tworzenia zestawów zatwierdzeń przetwarzanie przechodzi na drugi plan, gdy wybrana liczba rekordów do zatwierdzenia przekroczy wskazany próg. Użyj pola **Próg asynchroniczności**, aby ustalić, czy przetwarzanie zatwierdzeń ma się odbywać synchronicznie czy asynchronicznie. Wybierz jedną z poniższych wartości:

  - Zero: Wszystkie żądania powinny być przetwarzane asynchronicznie. 
  - Wartość większa od zera: Zatwierdzenia są przetwarzane asynchronicznie tylko wtedy, gdy przesłana liczba zatwierdzeń przekracza tę wartość.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
