---
title: Wiesze szansy sprzedaży opartej na projekcie - wersja uproszczona
description: Ten temat zawiera informacje na temat wierszy szans sprzedaży opartych na projekcie. (Pro)
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: bba555003b76e3e87412679b274f74f68ac7203b
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/31/2020
ms.locfileid: "4181025"
---
# <a name="project-based-opportunity-lines---lite"></a>Wiesze szansy sprzedaży opartej na projekcie - wersja uproszczona

_**Zastosowane w:** Wdrażanie uproszczone — od okazji do faktury pro forma_

Wiersze szans sprzedaży opartych na projekcie są dostępne tylko dla szans sprzedaży opartych na projektach. Szansa sprzedaży oparta na projekcie z polem **Typ** ustawionym na wartość **Oparte na pracy**.

Wiersze szans sprzedaży opartych na projektach są wierszami pozycji, które będą dostarczane do klienta za pomocą projektu. Projekty nie mogą być jednak powiązane z wierszem szansy sprzedaży opartym na projekcie. Projekty mogą być powiązane z pozycjami wiersza na etapie **Oferty** i dalszym, ponieważ zazwyczaj szansa sprzedaży znajduje się na wczesnym etapie cyklu życia transakcji. Określenie liczby projektów, które zostaną użyte do dostarczenia pracy dla klienta, jest decyzją podejmowaną później w fazie sprzedaży. Fazy szansy sprzedaży można użyć w celu zidentyfikowania odrębnych składników dostawy dla klienta. Decyzje dotyczące rzeczywistej liczby projektów służących do dostarczania tych składników mogą zostać opóźnione do momentu otrzymania dodatkowych informacji o samej pracy do wykonania.

Poniżej wymieniono pola w wierszu szansy sprzedaży opartej na projekcie:

| **Pole** | **Lokalizacja** | **Opis** | **Wpływ zmian w dalszych etapach** |
| --- | --- | --- | --- |
| Typ produktu | Karta Ogólne (ukryta) | W obszarze możesz wybrać jedną z następujących opcji:</br>- Usługa oparta na projekcie (dostępne tylko wtedy, gdy Dynamics 365 Project Operations jest zainstalowane)</br>- Produkt (dostępne tylko wtedy, gdy jest zainstalowane Project Operations i Dynamics 365 Sales) | Wartość tego pola jest ustawiona na **Usługę opartą na projekcie** podczas tworzenia wiersza szansy sprzedaży opartej na projekcie z poziomu siatki wierszy opartych na projekcie w sekcji szansy sprzedaży. <br> Zmiana lub zastąpienie tej wartości spowoduje, że w wierszach opartych na projekcie nie zostaną włączone funkcje projektu. |
| Szansa sprzedaży | Karta Ogólne | To pole jest w trybie do odczytu i zawiera odwołanie do rekordu szansy sprzedaży nadrzędnej, do którego należy ten element wiersza. | To pole nie ma wpływu na dalsze etapy. |
| Nazwa/nazwisko | Karta Ogólne | To edytowalne pole tekstowe może służyć jako krótka identyfikacja elementu wiersza. | Ta wartość jest przenoszona na wiersz oferty podczas tworzenia oferty na podstawie tej szansy sprzedaży. |
| Budżet klienta | Karta Ogólne | To pola można edytować w celu śledzenia kwoty, jaką dany nabywca jest skłonny zapłacić za dany wiersz. | Ta wartość jest przenoszona na odpowiedni wiersz oferty podczas tworzenia oferty na podstawie tej szansy sprzedaży. |
| Metoda rozliczania | Karta Ogólne | To edytowalne pole ma następujące wartości:</br>- Czas i materiał</br>- Stała cena | Ta wartość jest przenoszona na odpowiedni wiersz oferty podczas tworzenia oferty na podstawie tej szansy sprzedaży. Po utworzeniu wiersza oferty pole jest zablokowane i nie można go zmienić. Wartość tego pola należy przypisać możliwie najdokładniej. Jeśli zachodzi konieczność zmiany wartości tego pola w wierszu oferty, należy usunąć wiersz oferty i utworzyć go ponownie. |
