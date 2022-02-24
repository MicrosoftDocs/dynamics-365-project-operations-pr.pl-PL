---
title: Szacowania finansowe dotyczące wydatków w projektach
description: W tym temacie zamieszczono informacje dotyczące definiowania lub szacowania kosztów opartych na projektach.
author: rumant
manager: Annbe
ms.date: 03/19/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: ad4901b1264289f1da881154bc147fc3f8da698f
ms.sourcegitcommit: 386921f44f1e9a8a828b140206d52945de07aee7
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/22/2021
ms.locfileid: "5701795"
---
# <a name="financial-estimates-for-expenses-on-projects"></a>Szacowania finansowe dotyczące wydatków w projektach
_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_

Dynamics 365 Project Operations umożliwia menedżerom projektów definiowanie wydatków opartych na projektach dla każdego projektu lub zadania. Każda pozycja wydatkowa może być powiązana z konkretnym zadaniem projektu. Wydatki są podzielone na różne kategorie wydatków, które są definiowane na poziomie organizacyjnym. Ceny i kosztorysowanie dla każdej kategorii wydatków są określone w cenniku. 

Wykonaj poniższe kroki, aby wyświetlić, dodać lub usunąć koszty projektu.

1. Przejdź do obszaru **Projekty** i wybierz projekt, który chcesz edytować.
2. Wybierz **Oszacowania projektów** i wyświetl listę wydatków projektowych.
3. Wybierz opcję **Nowe koszty**, aby dodać wydatek. Możesz też wybrać wydatek, który ma zostać usunięty, a następnie wybrać pozycję **Usuń wydatek**.

W poniższej tabeli przedstawiono informacje o polach w obszarze **Linia szacowania wydatków** dla projektu. 

| **Pole** | **Opis** | **Wpływ zmian w dalszych etapach** |
| --- | --- | --- |
| Zadanie | Lista zadań w projekcie. Obejmuje to zadania podsumowujące i węzły-liścia. | Wybranie zadania dla wiersza szacowania kosztów wpłynie na szacowany koszt i szacowany koszt sprzedaży dla zadania. Jeśli to pole pozostanie puste, szacunek wydatków jest śledzony i podsumowywany tylko na poziomie projektu. |
| Kategoria | Lista kategorii transakcji, które mają połączone kategorie wydatków w aplikacji. | Wybór kategorii wpływa na ustalanie cen i kosztów w wierszu szacowania wydatków. |
| Data rozpoczęcia | Przewidywana data, w której wydatek wystąpi. | W tym polu nie ma wpływu zmian na dalsze etapy. |
| Grupa jednostek | Wartość domyślna w tym polu pochodzi z grupy jednostek skonfigurowanej jako domyślna w wybranej kategorii. Możesz zaktualizować to pole, aby wybrać inną grupę jednostek. | W tym polu nie ma wpływu zmian na dalsze etapy. |
| Jednostka | Wartość w tym polu jest domyślną jednostką wybranej kategorii. Możesz zaktualizować to pole, aby wybrać inną jednostkę. | Zmiana jednostki powoduje inną domyślną cenę jednostkową i koszt. |
| Ilość | Ilość szacowanego wydatku. | W tym polu nie ma wpływu zmian na dalsze etapy. |
| Koszt jednostkowy | Koszt wybranej kategorii i kombinacji jednostek zgodnie z obowiązującym cennikiem kosztów | Koszt jednostkowy jest zawsze wyświetlany w walucie kosztu projektu. |
| Cena jednostkowa | Cena wybranej kategorii i kombinacji jednostek zgodnie z ustawieniami w obowiązującym cenniku sprzedaży. | Cena jednostkowa jest zawsze wyświetlana w walucie sprzedaży projektu. |
| Łączny koszt | Kwota kosztu obliczana jako ilość \* koszt jednostkowy.| Kwota kosztu jest zawsze wyświetlana w walucie kosztu projektu. |
| Łączna sprzedaż | Kwota sprzedaży obliczana jako ilość \* cena jednostki. | Kwota sprzedaży jest zawsze wyświetlana w walucie sprzedaży projektu. |


[!INCLUDE[footer-include](../includes/footer-banner.md)]
