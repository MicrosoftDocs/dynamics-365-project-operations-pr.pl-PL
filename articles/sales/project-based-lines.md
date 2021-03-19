---
title: Wiersze szansy sprzedaży opartej na projekcie
description: Ten temat zawiera informacje na temat pracy z wierszami szans sprzedaży opartych na projekcie.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 91c53c917846a2b4e4fd64c14bb91782e9d05d66
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5277666"
---
# <a name="project-based-opportunity-lines"></a>Wiersze szansy sprzedaży opartej na projekcie

_**Zastosowane do:** Project Operations dla zasobów/scenariuszy nieopartych na zaopatrzeniu_


Wiersze szans sprzedaży opartych na projekcie są dostępne tylko dla szans sprzedaży opartych na projektach. Szansa sprzedaży oparta na projekcie z polem **Typ** ustawionym na wartość **Oparte na pracy**.

Wiersze szans sprzedaży opartych na projektach są wierszami pozycji, które będą dostarczane do klienta za pomocą projektu. Projekty nie mogą być jednak powiązane z wierszem szansy sprzedaży opartym na projekcie. Projekty mogą być powiązane z pozycjami wiersza na etapie **Oferty** i dalszym, ponieważ zazwyczaj szansa sprzedaży znajduje się na wczesnym etapie cyklu życia transakcji. Określenie liczby projektów, które zostaną użyte do dostarczenia pracy dla klienta, jest decyzją podejmowaną później w fazie sprzedaży. Fazy szansy sprzedaży należy użyć w celu zidentyfikowania odrębnych składników dostawy dla klienta. Decyzje dotyczące rzeczywistej liczby projektów służących do dostarczania tych składników mogą zostać opóźnione do momentu otrzymania dodatkowych informacji o samej pracy do wykonania.

Poniżej wymieniono pola w wierszu szansy sprzedaży opartej na projekcie:

| **Pole** | **Lokalizacja** | **Opis** | **Wpływ zmian w dalszych etapach** |
| --- | --- | --- | --- |
| Typ produktu | Karta Ogólne (ukryta) | Oto pole zestawu opcji. Jeśli korzystasz z Dynamics 365 Project Operations, jedna z dostępnych opcji to **Usługa oparta na projekcie**.  | Wartość tego pola jest ustawiona na **Usługę opartą na projekcie** podczas tworzenia wiersza szansy sprzedaży opartej na projekcie z poziomu siatki wierszy opartych na projekcie w sekcji szansy sprzedaży. <br> Zmiana lub zastąpienie tej wartości spowoduje, że w wierszach opartych na projekcie nie zostaną włączone funkcje projektu. |
| Szansa sprzedaży | Karta Ogólne | To pole jest w trybie do odczytu i zawiera odwołanie do rekordu szansy sprzedaży nadrzędnej, do którego należy ten element wiersza. | W tym polu nie ma wpływu zmian na dalsze etapy. |
| Nazwa/nazwisko | Karta Ogólne | To edytowalne pole tekstowe może służyć jako krótka identyfikacja elementu wiersza | Ta wartość jest przenoszona na wiersz oferty podczas tworzenia oferty na podstawie tej szansy sprzedaży |
| Budżet klienta | Karta Ogólne | To pola można edytować w celu śledzenia kwoty, jaką dany nabywca jest skłonny zapłacić za dany wiersz. | Ta wartość jest przenoszona na odpowiedni wiersz oferty podczas tworzenia oferty na podstawie tej szansy sprzedaży |
| Metoda rozliczania | Karta Ogólne | To edytowalne pole ma następujące wartości:</br>- Czas i materiał</br>- Stała cena | Ta wartość jest przenoszona na odpowiedni wiersz oferty podczas tworzenia oferty na podstawie tej szansy sprzedaży. Po utworzeniu wiersza oferty pole jest zablokowane i nie można go zmienić. Wartość tego pola należy przypisać możliwie najdokładniej. Jeśli zachodzi konieczność zmiany wartości tego pola w wierszu oferty, należy usunąć wiersz oferty i utworzyć go ponownie. |


[!INCLUDE[footer-include](../includes/footer-banner.md)]