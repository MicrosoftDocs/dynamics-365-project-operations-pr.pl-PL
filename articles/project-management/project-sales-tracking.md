---
title: Śledzenie sprzedaży projektu
description: W tym artykule przedstawiono informacje na temat sposobu, w jaki aplikacja Project Operations śledzi postęp w zakresie przychodów z pracy w ramach projektu.
author: rumant
ms.date: 03/24/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: ce61acf95ee5e9ac10047406c9d4a5c9b1f92aad
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8911287"
---
# <a name="project-sales-tracking"></a>Śledzenie sprzedaży projektu

_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_

Dynamics 365 Project Operations śledzi szacowane przychodu w najmniejszym wymaganym poziomie szczegółowości w planie projektu. Oszacowanie przychodów z pracy jest oparte na planowanym wysiłku i zasobach ogólnych lub nazwanych, które są przypisane do każdego zadania węzła-liścia w planie projektu. Kiedy projekt się rozpoczyna i ludzie zaczynają raportować czas wykonywania różnych zadań projektowych, podsumowywane są rzeczywiste przychody z pracy, co rozpoczyna obliczanie prognoz.

## <a name="labor-revenue-tracking-view"></a>Widok śledzenia przychodów z pracy

Na stronie **Projekty** na karcie **Śledzenie** możesz wybrać opcję **Śledzenie** > **Koszt**, aby otworzyć widok **Śledzenie kosztów**. Można też wybrać opcję **Użyj** > **Stawka faktury** w celu otwarcia widoku **Śledzenie przychodów**, który pokazuje postęp przychodu z pracy dla każdego zadania w planie projektu. W tym widoku porównuje się również rzeczywisty dochód z pracy wydany na zadanie z planowanym dochodem z pracy dla zadania. Project Operations używa następujących formuł do obliczania metryk przychodów z pracy:

- **Planowany przychód**: Szacowane wartości sprzedaży wszystkich przydziałów zasobów dla każdego zadania węzła-liścia
- **Przychód rzeczywisty**: Suma wszystkich niezafakturowanych danych rzeczywistych sprzedaży dla czasu zarejestrowanego w zadaniu
- **% przychodu fakturowalnego**: Rzeczywiste przychody ÷ Szacunkowe przychody w momencie ukończenia
- **Pozostałe przychody**: Szacunkowe przychody zakończone - Rzeczywiste przychody
- **Szacowany przychód w momencie zakończenia**: Pozostałe przychody + Rzeczywiste przychod
- **Odchylenie dochodów**: Planowane przychody - szacowane przychody na ukończeniu


> [!NOTE]
> Project Operations pokazują przychody pracy tylko na stronie **Projekt** na karcie **Śledzenie**. Podczas gdy materiały i koszty można szacują i śledzić na potrzeby konwersji, koszty te nie są uwzględniane w przychodach widocznych na karcie **Śledzenie**. Ta karta jest przeznaczona wyłącznie do ponownego projektu przychodów pracy przez ponowne projektunie nakładu pracy.  
> Wszystkie wyświetlane kwoty przychodów są przeliczane na walutę kosztów projektu. Waluta kosztów projektu jest walutą jednostki kontraktu w projekcie. W przypadku projektów o stałej cenie numery przychodów w widoku **Śledzenie przychodów** robocizna nie są odpowiednie, ponieważ wartości rzeczywiste sprzedaży nie są rejestrowane w zatwierdzeniu czasu.
> Wartości szacowanej sprzedaży dla czasu wyświetlane na karcie **Szacowanie** projektu mogą nie zostać dodane do planowanej wartości przychodu na karcie **Śledzenie**. Źródło tej rozbieżności wynika z dwóch możliwych przyczyn:
><ol>
   ><li> Na karcie <b>Szacowane</b> są pokazy szacowanego przychodu w walucie sprzedaży, a na karcie <b>Śledzenie</b> są widać planowane przychody przekonwertowane na walutę kosztów. </li>
   ><li> Podczas konwertowania szacowanej sprzedaży na walutę kontraktu, jak pokazano na karcie <b>Szacowane</b>, na walutę projektu konwersja obejmuje kroki, które mogą spowodować utratę dokładności: </li>
><ol>
><li> Szacunkowa kwota sprzedaży w walucie kontraktu jest najpierw przeliczana na walutę bazową (przeliczenie 1).</li>
><li> Szacunkowa kwota sprzedaży w walucie bazowej jest przeliczana na walutę kosztu projektu (konwersja 2). </li>
></ol>
></ol>
> Precyzja walutowa stosowana jest w obu krokach, co skutkuje odchyleniem planowanego przychodu w walucie projektu od planowanej sprzedaży w walucie kontraktu.
   

## <a name="reprojecting-revenues-on-leaf-node-tasks"></a>Ponowne projektowanie przychodów w zadaniach węźle głównym

Nie można bezpośrednio przeprojektować przychodów w zadaniach węzła i na karcie **Śledzenie** na stronie **Projekt**. Można jednak użyć widoku **Śledzenie nakładu pracy** w celu ponownego omierzenia pozostałego nakładu pracy w zadaniu. Powoduje to ponowne obliczanie pozostałego przychodu zadania. Poniżej przedstawiono opis działania tego działania.

1. Menedżer projektu może ponownie zaplanować nakład pracy związany z zadaniami, aktualizując wartość domyślną w polu **Pozostały nakład pracy** za pomocą nowego oszacowania pozostałego nakładu pracy nad zadaniem. Ponowne odwzorowanie powoduje ponowne obliczenie oszacowanego nakładu pracy zadania przy ukończeniu (EAC), procentu postępu i przewidywanej wariancji nakładu pracy dla zadania. SPZ, oszacowanie do ukończenia (ETC) i procent postępu w zadaniach sumarycznych są również ponownie obliczane i generują nową prognozę wariancji nakładu.
2. Na podstawie nowej wartości pozostałego nakładu pracy w zadaniu system oblicza pozostały przychód w widoku **Śledzenie przychodów**. Aby obliczyć pozostały przychód na podstawie pozostałego wysiłku, system najpierw oblicza średni przychód z jednej godziny wysiłku związanego z zadaniem jako przychód planowany lub wysiłek planowany. Planowany przychód to suma przychodów ze wszystkich przydziałów zasobów w zadaniu. Średni przychód na godzinę jest używany do obliczania pozostałego przychodu dla nowo przewidywanego pozostałego nakładu pracy w zadaniu.
3. Szacowany przychód przy ukończeniu i procent zużycia przychodów w zadaniu węzła-liścia są ponownie obliczane.
4. Przychód przy pełnej wartości zadań sumarycznych aż do węzła głównego jest ponownie obliczany.

## <a name="reprojecting-revenues-on-summary-tasks"></a>Ponowne projektowanie przychodów zadań sumarycznych

Przychód z pracy można ponownie rzutować na zadania sumaryczne lub zadania kontenera. Nie można jednak bezpośrednio odwzorować przychodów w zadaniu sumarycznym projektu na karcie **Śledzenie** na stronie **Projekt**. Podobnie jak w przypadku zadań węzła głównego, ponowne wykonywanie zadań podsumowania i kontenerów można wykonać przy użyciu widoku **Śledzenie nakładów pracy**. W tym widoku można ponownie zaplanować pozostały nakład pracy w zadaniu sumarycznym, powodując ponowne obliczenie pozostałego przychodu z zadania sumarycznego. Poniżej przedstawiono opis działania tego działania.

1. Menedżer projektu może ponownie zaplanować nakład pracy związany z zadaniami, aktualizując wartość domyślną w polu **Pozostały nakład pracy** za pomocą nowego oszacowania **Pozostałego nakładu pracyt** nad zadaniem. Ponowne odwzorowanie powoduje ponowne obliczenie oszacowanego nakładu pracy zadania przy ukończeniu (SPZ), procentu postępu i przewidywanej wariancji nakładu pracy dla zadania. Wartości SPZ, ETC i procent postępu w zadaniach sumarycznych są również obliczane ponownie i dają nową projekcję odchylenia.
2. Na podstawie nowej wartości **pozostałego nakładu pracy** w zadaniu system oblicza pozostały przychód w widoku **Śledzenie przychodów**. Aby obliczyć pozostały przychód na podstawie pozostałego wysiłku, system najpierw oblicza średni przychód z jednej godziny wysiłku związanego z zadaniem jako przychód planowany lub wysiłek planowany. Planowany przychód to suma przychodów ze wszystkich przydziałów zasobów w zadaniu. Ten średni przychód na godzinę jest następnie używany do obliczania przychodu z nowo prognozowanego pozostałego nakładu pracy w zadaniu.
3. Szacowany przychód przy ukończeniu i procentach zużycia przychodów w zadaniu sumarycznym są ponownie obliczane.
4. Nowa wartość szacowanego przychodu po ukończeniu jest rozdzielana na zadania podrzędne w takim samym stosunku, w jakim pierwotnie planowany przychód przypadał na zadanie.
5. Obliczany jest nowy szacowany przychód po zakończeniu każdego z poszczególnych zadań aż do zadań węzła-liścia. Na podstawie tej wartości zadania podrzędne, których dotyczy problem, aż do węzłów liści, będą miały ponownie obliczony pozostały przychód i procent wykorzystania przychodów na podstawie całkowitego przychodu. Powoduje to nową prognozę odchylenia dochodów z zadania. 
6. Przychód przy pełnej wartości zadań sumarycznych aż do węzła głównego jest ponownie obliczany.


[!INCLUDE[footer-include](../includes/footer-banner.md)]

