---
title: Konfigurowanie szablonów kosztów
description: Ten temat zawiera informacje o tym, jak skonfigurować utworzyć szablony kosztów i używać ich w aplikacji Project Operations.
author: sigitac
ms.date: 11/18/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: b3a9f1e4f5ea0abe34dc860db87ef349daa46c487b03d271bfe207868c521f39
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/06/2021
ms.locfileid: "6993569"
---
# <a name="set-up-cost-templates"></a>Konfigurowanie szablonów kosztów

_**Zastosowane do:** Project Operations dla zasobów/scenariuszy nieopartych na zaopatrzeniu_


Ten temat zawiera informacje o tym, jak skonfigurować utworzyć szablony kosztów i używać ich w aplikacji Project Operations. Szablon kosztów określa:

- Kategorie projektu dotyczące prognozowanych i rzeczywistych transakcji, które mają zostać uwzględnione w wartości procentowej obliczenia wykonania projektu. Wartość procentu wykonania jest następnie używana do obliczenia wielkości rozpoznanego przychodu.
- Określa, czy wartość procentu wykonania może zostać zmodyfikowana, jeśli jest obliczana automatycznie.
- Określa, czy procent wykonania jest obliczany na podstawie kwot czy jednostek.

## <a name="cost-template-example"></a>Przykład szablonu kosztów

Pracujesz nad projektem witryny internetowej klienta, za co pobierasz stała opłatę w wysokości 10 000 USD. Prognozujesz, że wykonanie projektu zajmie 100 godzin (5000 USD). Przewidujesz również zakup dwóch biletów na samolot i czterech nocy w hotelu w ramach podróży do siedziby klienta (1800 USD). Powoduje to obliczenie całkowitego przewidywanego kosztu w wysokości 6800 USD.

Po uruchomieniu procesu uznawania przychodów dla stałej ceny w celu utworzenia oszacowania na koniec miesiąca można stwierdzić, że praca nad projektem trwała 35 godzin. Nie obejmuje to jeszcze cen lotów ani kosztów hotelu. Twój asystent wykonał również pięć godzin prac badawczych związanych z projektem, a jego koszty wyniosły 100 USD, które nie zostały jeszcze zaplanowane.

Podczas obliczania procentowej wartości wykonania projektu możesz wykonać następujące czynności:

- Czy chcesz uwzględnić wszystkie koszty (godziny i wydatki) czy tylko godziny?
- Czy chcesz uwzględnić wszystkie godziny czy tylko godziny planowane?
- Czy chcesz obliczyć procent wykonania na podstawie kosztu zaplanowanych godzin w dolarach (5000 USD) czy tylko na podstawie liczby godzin (100)?

Odpowiedzi na te pytania określają opcje ustawiane dla szablonu kosztów oraz kategorie wybierane w wierszach szablonu kosztów.

W poniższej tabeli przedstawiono wyniki różnych metod obliczania procentowej wartości wykonania w tym scenariuszu.

| Wykonanie oparte na | Koszt w dolarach lub jednostki | Procent wykonania | Obliczenie |
| --- | --- | --- | --- |
| Wszystkie godziny, brak wydatków | Koszt w dolarach | 37% 35 x 50 USD + 100 USD = 1850 USD 1850 USD/5000 USD |
| Wszystkie godziny, brak wydatków | Jednostki | 40% | 40 godzin/100 godzin (w tym pięć nieplanowanych godzin) |
| Planowane godziny, brak wydatków | Koszt w dolarach lub jednostka | 35% | 35/100 godzin lub 35 x 50/5000 USD |
| Wszystkie godziny i wydatki | Koszt w dolarach | 27,2% | 1850 USD/6800 USD |

Decydowanie o sposobie tworzenia szablonu kosztów może zależeć od kilku kwestii:

- Jeśli w szablonie kosztów zostaną uwzględnione nieplanowane godziny, występuje ryzyko osiągnięcia 100 procent wykonania przed zakończeniem projektu. Wynika to z faktu, że rzeczywista liczba godzin będzie większa niż godziny planowane. W przypadku korzystania z dwóch pierwszych metod wymienionych w tabeli musisz zmienić plan (jednostki prognozowane), gdy dowiesz się o odchyleniach. W takim przypadku należy dodać lub odjąć godziny, korzystając z wiedzy o tym, co jest wymagane do zakończenia projektu. Jeśli wykonanie projektu wymaga kolejnych 65 godzin, należy dodać pięć godzin do planu, aby uzyskać sumę 105. Jeśli wiesz, że asystent wykona kolejne pięć godzin badań, suma wyniesie 110 godzin.
- W przypadku korzystania z trzeciej metody wymienionej w tabeli planowane godziny są aktualizowane tylko na własne potrzeby, aby zapewnić dokładną wartość procentu wykonania. Rentowność będzie się zmieniać po zarejestrowaniu niezaplanowanych godzin wolnych od pracy, ale Ty pozostaniesz na znanej trajektorii procentu wykonania.
- W przypadku korzystania z czwartej metody wymienionej w tabeli ryzyko polega na tym, że wydatki będą wypadać w nieregularnych odstępach czasu i mogą nie zostać odzwierciedlonej w ramach postępu wykonania. W związku z tym, jeśli wydatki zostaną uwzględnione, mogą spowodować wahania procentu wykonania o więcej niż jest to pożądane. Na przykład ponieważ lot się jeszcze nie odbył, procent wykonania wynosił 27 procent, a nie 35 procent lub 37 procent, jeśli obliczenia są oparte wyłącznie na samym czasie. Jeśli odbyła się jedna podróż obejmująca dwie noce w hotelu, a koszty lotów i hotelu były dokładnie prognozowane, procent wykonania wynosił 40,4 procenta (1850 USD na robociznę i 900 USD na wydatki kosztów = 2750 USD/6800 USD = 40,4 procenta). Z tego powodu koszty dotyczące tylko jednej podróży samolotem mogą zmienić procent wykonania z 27 na 40 procent.

## <a name="create-cost-templates"></a>Tworzenie szablonów kosztów
Aby utworzyć szablon kosztów, wykonaj następujące kroki:

1. Aby uzyskać dostęp do szablonów kosztów, w środowisku aplikacji Dynamics 365 Finance przejdź do pozycji **Zarządzanie projektami i ich księgowanie** > **Ustawienia** > **Szacowania** > **Szablon kosztów**.
2. Wybierz pozycję **Nowy**, aby utworzyć nowy szablon kosztów. Wprowadź nazwę i opis.
3. Podaj identyfikator wiersza kosztu dla każdego typu transakcji.
4. Wybierz domyślną metodę obliczania wartości wykonania:

  - **Automatycznie**: procent wykonania jest obliczany automatycznie w projekcie. Nie można zmienić wartości wynikowej.
  - **Ręcznie**: procent wykonania jest obliczany ręcznie w projekcie. Można zmienić wartość wynikową.

  > [!NOTE]
  > W przypadku obliczeń ręcznych procent wykonania jest zachowywany podczas **obliczeń ręcznych** na karcie **Ogólne** na stronie **Szacowanie**.

5. W obszarze **Wykonanie oparte na** wybierz jedną z następujących wartości:

  - **Kwota**: kwota w walucie rozliczeniowej jest obliczana jako procent wykonania.
  - **Jednostka**: ilość jest obliczana jako procent wykonania.
  - **Liniowo**: system oblicza procent wykonania proporcjonalnie, korzystając z dat rozpoczęcia i zakończenia projektu w celu określenia długości projektu.

6. Wybierz pozycję **Wiersze kosztu**, aby przejrzeć wiersze kosztów w szablonie kosztów. Dla każdego typu transakcji wymagany jest co najmniej jeden wiersz kosztów. Można jednak utworzyć wiele wierszy kosztów dla tych samych typów transakcji i ustawić wymagane atrybuty tych wierszy.
7. Na karcie **Kategorie** wybierz kategorie projektów, które mają być uwzględnione w wierszu szablonu kosztów.
8. Na karcie **Ogólne** wybierz opcję, aby wskazać, czy wiersz będzie uwzględniany w obliczeniach procentu wykonania.
9. Wybierz metodę kosztów wykonania, która ma być używana przy obliczaniu procentu wykonania.


[!INCLUDE[footer-include](../includes/footer-banner.md)]