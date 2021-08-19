---
title: Szacowania finansowe dotyczące materiałów w projektach
description: Ten temat zawiera informacje na temat definiowania lub szacowania materiałów opartych na projektach.
author: rumant
ms.date: 03/30/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 1717abb8f37acb7ab5f4e24b9323b3d958b40b13d7da44c0bbfa88eea28b99ef
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/06/2021
ms.locfileid: "6992624"
---
# <a name="financial-estimates-for-materials-on-projects"></a>Szacowania finansowe dotyczące materiałów w projektach

_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_

Dynamics 365 Project Operations umożliwia kierownikom projektów definiowanie kosztów materiałów opartych na projektach dla każdego projektu lub zadania. Każdy kosztorys materiałowy można powiązać z konkretnym zadaniem projektowym. Wydatki są podzielone na różne kategorie wydatków, które są definiowane na poziomie organizacyjnym. Ceny i kosztorysowanie dla każdej kategorii wydatków są określone w cenniku. 

Każdy kosztorys materiałowy można powiązać z konkretnym projektemowym.

1. Przejdź do opcji **Projekty** i wybierz projekt, który chcesz zaktualizować.
2. Na karcie **Szacowanie materiałów** wyświetl listę szacowań materiałów projektowych.
3. Wybierz opcję **Nowe szacowanie materiałów**, aby utworzyć nowy szacunek materiałowy. Można też wybrać szacowanie materiałów do usunięcia, a następnie wybrać opcję **Usuń szacowania materiałów**.

W poniższej tabeli przedstawiono informacje o polach w obszarze **Wiersz szacowania materiałów** dla projektu. 

| **Pole** | **Opis** | **Wpływ zmian w dalszych etapach** |
| --- | --- | --- |
| Zadanie | Lista zadań w projekcie. Obejmuje to zadania podsumowujące i węzły-liścia. | Po wybraniu zadania dla wiersza szacowania materiałów ma to wpływ na szacowany koszt materiałów i szacowaną sprzedaż materiałów dla zadania. Jeśli to pole jest puste, oszacowanie materiału jest śledzone i podsumowywane tylko na poziomie projektu. |
| Wybierz produkt |  Możesz określić, czy wiersz wyceny dotyczy istniejącego (katalogu) czy zapisywanego produktu. | To pole określa, czy wybierzesz produkt z katalogu, czy produkt do zapisu. |
| Produkt | Identyfikator produktu z katalogu produktów. Po wybraniu identyfikatora produktu pole **Wybierz produkt** jest automatycznie aktualizowane na **Istniejący produkt**. Identyfikator jest używany do pobierania kosztów i cen sprzedaży z cennika. | W tym polu nie ma wpływu zmian na dalsze etapy. |
| Opis produktu dopisanego | Pole tekstowe dopisania nazwy produktu. To pole powinno być używane, gdy wybrano **Dopisanie** w polu **Wybierz produkt**.| W tym polu nie ma wpływu zmian na dalsze etapy. |
| Data rozpoczęcia | Przewidywany termin, w którym materiał będzie używany. | W tym polu nie ma wpływu zmian na dalsze etapy. |
| Grupa jednostek | Wartość domyślna w tym polu pochodzi z domyślnej grupy jednostek w produkcie z katalogu. Możesz zaktualizować to pole, aby wybrać inną grupę jednostek. | W tym polu nie ma wpływu zmian na dalsze etapy. |
| Jednostka | Wartość w tym polu pochodzi z domyślnej jednostki wybranego produktu. Możesz zaktualizować to pole, aby wybrać inną jednostkę. | Zmiana jednostki powoduje inną domyślną cenę jednostkową i koszt. |
| Ilość | Szacunkowa ilość produktu, która zostanie wykorzystana w projekcie. | W tym polu nie ma wpływu zmian na dalsze etapy. |
| Koszt jednostkowy | Koszt jednostkowy wybranego produktu i kombinacji jednostek, zgodnie z obowiązującym cennikiem. | Koszt jednostkowy jest zawsze wyświetlany w walucie kosztu projektu. Jeśli w cenniku nie ma ustawienia kosztu jednostkowego dla kombinacji produktu i ustawienia jednostki, koszt jednostkowy będzie domyślnie wynosił 0,00. |
| Cena jednostkowa | Cena wybranego produktu i kombinacji jednostek zgodnie z obowiązującym cennikiem sprzedaży. | Cena jednostkowa jest zawsze wyświetlana w walucie sprzedaży projektu. Jeśli w cenniku nie ma ustawienia ceny jednostkowej dla kombinacji produktu i ustawienia jednostki, cena jednostkowa będzie domyślnie wynosić 0,00.|
| Łączny koszt | Kwota kosztu obliczana jako ilość \* koszt jednostkowy.| Kwota kosztu jest zawsze wyświetlana w walucie kosztu projektu. |
| Łączna sprzedaż | Kwota sprzedaży obliczana jako ilość \* cena jednostki. | Kwota sprzedaży jest zawsze wyświetlana w walucie sprzedaży projektu. |


[!INCLUDE[footer-include](../includes/footer-banner.md)]
