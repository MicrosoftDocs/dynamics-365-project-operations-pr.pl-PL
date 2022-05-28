---
title: Śledzenie kosztu projektu
description: Ten temat zawiera informacje o tym, jak Project Operations śledzą postęp w stosunku do kosztów pracy i wydatków na projekt.
author: rumant
ms.date: 03/22/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: f724ee29728a363c58ed0e69087f4c18be89ea2d
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/14/2022
ms.locfileid: "8591463"
---
# <a name="labor-cost-tracking-on-projects"></a>Śledzenie kosztów robocizny w projektach

_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_

Dynamics 365 Project Operations śledzi szacowane robocizny i wydatków w najmniejszym wymaganym poziomie szczegółowości w planie projektu. Oszacowanie finansowe kosztu pracy jest oparte na planowanym wysiłku i ogólnych lub nazwanych zasobach, które są przypisane do każdego zadania węzła-liścia w planie projektu. Gdy projekt się rozpoczyna, a ludzie zaczynają raportować czas poświęcony różnym zadaniom projektowym, podsumowywane są rzeczywiste wydatki na pracę, co rozpoczyna obliczanie prognoz.

## <a name="labor-cost-tracking-view"></a>Widok śledzenia kosztów pracy

Na stronie **Projekty** na karcie **Śledzenie** można wybrać opcję **Śledzenie** > **Koszt**, aby otworzyć widok **Śledzenie kosztów** i zobaczyć postęp prac poświęcanych na każde zadanie w planie projektu. W tym widoku porównuje się również rzeczywisty koszt pracy wydany na zadanie z planowanym kosztem pracy zadania. Project Operations używa następujących formuł do obliczania metryk kosztów pracy:

- **Planowany koszt**: szacowany koszt wszystkich przypisań zasobów w każdym z zadań węzła głównego
- **Koszt rzeczywisty**: suma wszystkich wartości rzeczywistych kosztów dla czasu zarejestrowanego w zadaniu
- **Procent szacowania kosztu**: koszt ÷ szacowany koszt na zakończenie
- **Pozostały koszt**: Całkowity kosztorys - rzeczywisty koszt
- **Koszt przy zakończeniu**: Pozostały koszt + Koszt rzeczywisty
- **Odchylenie kosztów**: Planowany koszt - kosztorys zakończony

Każde zadanie przedstawia prognozę wariancji kosztów zadania. Jeśli szacowany koszt w momencie ukończenia jest wyższy niż koszt planowany, przewiduje się, że zadanie przekroczy budżet. Jeśli szacowany koszt w momencie ukończenia jest niższy niż koszt planowany, przewiduje się, że zadanie zakończy się w ramach budżetu.

>[!NOTE]
> Project Operations pokazują koszty pracy tylko na stronie **Projekt** na karcie **Śledzenie**. Podczas gdy materiały i koszty można szacują i śledzić na potrzeby konwersji, koszty te nie są uwzględniane w kosztach widocznych na karcie **Śledzenie**. Ta karta jest przeznaczona wyłącznie do ponownego projektu kosztów pracy przez ponowne projektunie nakładu pracy.
Wszystkie pokazane kwoty kosztów są konwertowane na walutę kosztu projektu z waluty kosztu projektu używanej do określenia stawki kosztu. Waluta kosztów projektu jest walutą jednostki kontraktu w projekcie. Wartości szacowanego kosztu dla czasu wyświetlane na karcie **Szacowanie** na stronie **Projekt** mogą nie zostać wyświetlone na karcie **Śledzenie**. Przyczyną tego rozbieżności są różnice w sposób sumowany szacowanego kosztu w siatce **Szacowanie** oraz sposób obliczania planowanego kosztu w siatce **Śledzenie**. 
>
> - Na karcie **Szacowany koszt** jest obliczany na podstawie tej samej waluty, w jakiej jest obliczany koszt w cenniku. Następnie szacowany koszt w walucie cennika jest konwertowany na szacowany koszt w walucie kosztu projektu. Szacowany koszt w walucie projektu jest wyświetlany zaokrąglony do 2 miejsc dziesiętnych. W żadnym momencie podczas tej konwersji nie jest stosowana dokładność waluty. 
> - Na karcie **Śledzenie** planowane obliczenia kosztów wynika z nieco innego zlecenia obliczania, które obejmuje zastosowanie dokładności waluty w dwóch etapach: 
   ><ol>
   ><li>Kwota szacowanego kosztu w walucie cennika jest konwertowana na walutę podstawową (konwersja 1).</li>
   ><li>Szacunkowa kwota kosztu w walucie bazowej jest konwertowana na walutę kosztu projektu (konwersja 2). </li>
   ></ol>
   >Dokładność waluty jest stosowana w obu krokach w celu uzyskania planowanego kosztu (na karcie **Śledzenie**), który różni się nieco od szacowanego kosztu (w widoku **Czas — etapami** na karcie **Szacowanie**). 
   
## <a name="reprojecting-costs-on-leaf-node-tasks"></a>Ponowne projektunie kosztów w zadaniach węźle głównym

Nie można bezpośrednio przeprojektować kosztów robocizna w zadaniach węzła i na karcie **Śledzenie** na stronie **Projekt**. Można jednak użyć widoku **Śledzenie nakładu pracy** w celu ponownego omierzenia pozostałego nakładu pracy w zadaniu. Powoduje to ponowne obliczanie pozostałego kosztu zadania. Poniżej przedstawiono opis działania tego działania.

1. Menedżer projektu może ponownie zaplanować nakład pracy związany z zadaniami, aktualizując wartość domyślną w polu **Pozostały nakład pracy** za pomocą nowego oszacowania pozostałego nakładu pracy nad zadaniem. Ponowne odwzorowanie powoduje ponowne obliczenie oszacowanego nakładu pracy zadania przy ukończeniu (EAC), procentu postępu i przewidywanej wariancji nakładu pracy dla zadania. SPZ, oszacowanie do ukończenia (ETC) i procent postępu w zadaniach sumarycznych są również ponownie obliczane i generują nową prognozę wariancji nakładu.
2. Na podstawie nowej wartości pozostałego nakładu pracy w zadaniu system oblicza pozostały koszt w widoku **Śledzenie kosztów**. Aby obliczyć pozostały koszt na podstawie pozostałego nakładu pracy, system najpierw oblicza średni koszt jednej godziny pracy nad zadaniem jako koszt planowany lub nakład pracy planowanej. Planowany koszt jest sumą kosztu wszystkich przypisań do zasobów w ramach zadania. Średni koszt na godzinę jest używany do obliczenia pozostałego kosztu nowego projektu pozostałego nakładu pracy w ramach zadania.
3. Całkowity koszt i procent zużycia kosztów w zadaniu węzła-liścia są ponownie obliczane.
4. Koszt przy pełnej wartości zadań sumarycznych aż do węzła głównego jest ponownie obliczany.

## <a name="reprojecting-costs-on-summary-tasks"></a>Ponowne projektowanie kosztów zadań sumarycznych

Koszty pracy można ponownie rzutować na zadania sumaryczne lub zadania kontenera. Nie można jednak bezpośrednio odwzorować kosztów pracy w zadaniu sumarycznym projektu na karcie **Śledzenie** na stronie **Projekt**. Podobnie jak w przypadku zadań węzła głównego, ponowne wykonywanie zadań podsumowania i kontenerów można wykonać przy użyciu widoku **Śledzenie nakładów pracy**. W tym widoku można ponownie zaplanować pozostały nakład pracy w zadaniu sumarycznym, powodując ponowne obliczenie pozostałego kosztu zadania sumarycznego. Poniżej przedstawiono opis działania tego działania.

1. Kierownik projektu może przeprojektować nakład pracy w zadaniach sumarycznych, aktualizując domyślną wartość pozostałego nakładu pracy o nowe oszacowanie zadania. Ta aktualizacja powoduje ponowne obliczenie oszacowania zadania sumarycznego przy ukończeniu (EAC), procentu postępu i przewidywanej wariancji nakładu pracy w zadaniu. Wartości SPZ, ETC i procent postępu w zadaniach sumarycznych są również obliczane ponownie i dają nową projekcję odchylenia.
2. Na podstawie nowej wartości pozostałego nakładu pracy w zadaniu sumarycznym system oblicza pozostały koszt w widoku **Śledzenie kosztów**. Aby obliczyć pozostały koszt na podstawie pozostałego nakładu pracy, system najpierw oblicza średni koszt jednej godziny pracy nad zadaniem podumowującym jako koszt planowany lub nakład pracy planowanej. Średni koszt na godzinę jest używany do obliczania kosztu nowo przewidywanego pozostałego nakładu pracy w zadaniu sumarycznym.
3. Całkowity koszt i procent zużycia kosztów w zadaniu sumarycznym węzła-liścia są ponownie obliczane.
4. Nowy koszt w momencie ukończenia jest rozdzielany na zadania podrzędne w takiej samej proporcji, w jakiej pierwotnie zaplanowany koszt był w zadaniu.
5. Obliczany jest nowy koszt z pełną wartością dla każdego z poszczególnych zadań aż do zadań węzła-liścia. Na podstawie tej wartości zadania podrzędne, których dotyczy problem, aż do węzłów liści, będą miały ponownie obliczony pozostały koszt i procent zużycia kosztów na podstawie kosztu przy pełnej wartości. Ta wartość powoduje nową prognozę wariancji kosztów zadania. 


Pole **Wydajność kosztów** można ustawić na pomocą danych śledzenia. Gdy zmienność kosztów dla węzła głównego w widoku **śledzenia kosztu** jest ujemna, w tym polu można ustawić wartość **W budżecie**. Gdy zmienność kosztów w węźle głównym jest dodatnia, można ustawić wartość **Ponad budżet**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
