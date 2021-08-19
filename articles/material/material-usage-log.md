---
title: Rejestrowanie użycia materiałów w projektach i zadaniach projektów
description: Ten temat zawiera informacje na temat sposobu logowania użycia materiałów do projektów i zadań projektów.
author: rumant
ms.date: 03/31/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 4d8757049953fab0ad8bf6ee1a1d695fcb6df75b1be52641ad4af3b3137d7a0a
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/06/2021
ms.locfileid: "6999284"
---
# <a name="record-material-usage-on-projects-and-project-tasks"></a>Rejestrowanie użycia materiałów w projektach i zadaniach projektów

_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_

Gdy zespół projektowy pracuje nad zadaniami w projekcie, konsumuje lub wykorzystuje materiały. Dziennik zużycia materiałów umożliwia rejestrowanie tego wykorzystania, tak aby mógł zostać zatwierdzony przez kierownika projektu i ostatecznie zafakturowany klientowi. 

Aby zarejestrować użycie katalogu lub materiałów do zapisu i przesłać je do osoby zatwierdzającej, wykonaj następujące kroki: 

1. W okienku nawigacyjnym wybierz opcję **Użycie materiałów**, a następnie wybierz opcję **Nowy**.
2. Na stronie **Nowe użycie materiałów** wprowadź wymagane informacje dotyczące użycia materiałów, a następnie wybierz opcję **Zapisz**.

W poniższej tabeli przedstawiono informacje o polach na stronie **Dziennik użycia materiałów**. 

| **Pole** | **Opis** | **Wpływ zmian w dalszych etapach** |
| --- | --- | --- |
| Opis | Opis konkretnego zastosowania materiałów. | W tym polu nie ma wpływu zmian na dalsze etapy. |
| Data | Data, w której materiał ma być używany. | W tym polu nie ma wpływu zmian na dalsze etapy. |
| Project | Listy projektów, które są aktywne. | Wybranie projektu do dziennika użycia materiałów wpływa na pole **Zadanie**, tak aby wyświetlane było tylko zadania związane z projektem. |
| Zadanie | Lista zadań projektu łącznie z podsumowaniem i zadaniami węzła liścia. | Wybranie zadania do dziennika zużycia materiałów ma wpływ na rzeczywisty koszt materiałów i rzeczywistą sprzedaż materiałów dla zadania. Jeśli to pole jest puste, odpowiednie koszty zużycia materiałów i sprzedaży są śledzone i podsumowywane tylko na poziomie projektu. |
| Wybierz produkt | Należy określić, czy to użycie materiałów dotyczy **Istniejącego** produktu (katalogu), czy też **Dopisane** produktu. | To pole określa typ produktu. |
| Produkt | Identyfikator produktu z katalogu produktów. Po wybraniu identyfikatora produktu pole **Wybierz produkt** automatycznie aktualizuje **Istniejący produkt**. Identyfikator jest używany do pobierania kosztów i cen sprzedaży z cennika. | W tym polu nie ma wpływu zmian na dalsze etapy. |
| Opis produktu dopisanego | Pole tekstowe dopisania nazwy produktu. To pole jest dostępne po wybraniu opcji **Dopisanie** w polu **Wybierz produkt**.| W tym polu nie ma wpływu zmian na dalsze etapy. |
| Zasób, który można zarezerwować| Zasób, który wykorzystać ten materiał do projektu. Domyślną wartością tego pola jest zarezerwowany zasób zalogowanego użytkownika, ale można go zmienić na użycie rekordów w imieniu innych członków zespołu projektu. | W tym polu nie ma wpływu zmian na dalsze etapy. |
| Grupa jednostek | Wartość domyślna w tym polu pochodzi z grupy jednostek ustawionej jako domyślna dla produktu katalogu. Możesz zaktualizować to pole, aby wybrać inną grupę jednostek. | W tym polu nie ma wpływu zmian na dalsze etapy. |
| Jednostka | Domyślna wartość w tym polu jest jednostką domyślną wybranego produktu. Możesz zaktualizować to pole, aby wybrać inną jednostkę. | Zmiana jednostki powoduje inną domyślną cenę jednostkową i koszt. |
| Ilość | Ilość produktu użytego w projekcie lub zadaniu projektu. | W tym polu nie ma wpływu zmian na dalsze etapy. |
| Koszt jednostkowy | Koszt jednostkowy wybranego produktu i kombinacji jednostek, zgodnie z obowiązującym cennikiem. | Koszt jednostkowy jest zawsze wyświetlany w walucie kosztu projektu. Jeśli w cenniku nie ma kosztu jednostkowego produktu i jednostki, koszt jednostkowy zostanie domyślnie wartości 0,00. |
| Łączny koszt | Kwota kosztu obliczana jako ilość \* koszt jednostkowy.| Kwota kosztu jest zawsze wyświetlana w walucie kosztu projektu. |


## <a name="submit-material-usage-for-review-and-approval"></a>Przesyłanie materiałów do przeglądu i zatwierdzenia 
Po przechwytywaniu wszystkich materiałów i przygotowaniu się do zatwierdzenia należy przesłać informacje o użyciu do przeglądu.

1. Należy przejść do **Dziennik użycia materiałów** i wybrać jeden lub więcej wpisów. Można również zaznaczyć wszystkie rekordy użycia materiałów przy użyciu pola wyboru w nagłówku.
2. Wybierz **Prześlij**. System przetwarza wybrane pozycje, a następnie tworzy żądania zatwierdzenia użycia materiałów.

## <a name="recall-a-material-usage-log"></a>Odwołaj dany wpis zużycia materiałów

W razie potrzeby można sprawdzić, czy został przekazany materiał. Czas potrzebny na wycofanie wpisu dotyczącego wykorzystania materiału zależy od etapu zatwierdzania.  Jeśli osoba zatwierdzająca jeszcze nie zatwierdziła wpisu, odwołanie może nastąpić natychmiast. Jeśli jednak wpis został już zatwierdzony, należy poprosić osobę zatwierdzającą o zatwierdzenie wycofania i odwrócenie transakcji.

1. Wybierz opcję **Użycie materiałów** i z listy dzienników użycia materiałów wybierz użycie materiałów, które chcesz przechować.
2. Wybierz pozycję **Odwołaj**. Jeśli wpis o zużyciu materiału nie został jeszcze zatwierdzony, system natychmiast go wycofuje. Jeśli pozycja materiału została już zatwierdzona, tworzone jest żądanie wycofania w celu powiadomienia osoby zatwierdzającej, że chcesz wycofać użycie materiału. Osoba zatwierdzająca potwierdzi również, że można dokonać odwrócenia, a wpis zostanie cofnięty.

## <a name="delete-a-material-usage-log"></a>Usuń dany wpis zużycia materiałów

Nie można usuwać dzienników użycia materiałów, które nie zostały przesłane. Aby usunąć przesłany wcześniej dziennik użycia materiałów, należy najpierw go usunąć.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
