---
title: Ustawienia oferty projektu
description: W tym temacie zamieszczono informacje na temat informacji i ustawień mających zastosowanie do ofert projektów i na nie wpływających.
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 3f11188a47c6f0c7de9fb591fd3be3e22f8f7d842fb6d075c1f43d9baea4d225
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/06/2021
ms.locfileid: "6993479"
---
# <a name="header-details-for-project-based-quotes"></a>Szczegóły nagłówka dla ofert opartych na projekcie

_**Zastosowane do:** Project Operations dla zasobów/scenariuszy nieopartych na zaopatrzeniu_


W tym artykule opisano informacje dotyczące oferty projektu. Obejmuje ona ustawienia mające wpływ na wszystkie wiersze oferty oraz informacje o ofercie, które są podsumowanie we wszystkich pozycjach produktu, aby utworzyć wskaźniki KPI oferty projektu.

W poniższej tabeli wymieniono pola informacji podsumowującej w ofercie projektu, które są unikatowe dla rozwiązania Dynamics 365 Project Operations lub zawierają pewne istotne zmiany w zachowaniu z ofert systemu Dynamics 365 Sales.

| **Pole** | **Lokalizacja** | **Opis** | **Wpływ zmian w dalszych etapach** |
| --- | --- | --- | --- |
| Pisz | Karta Podsumowanie (ukryte) | To pole zestawu opcji hashuje następujące opcje:</br>- Na podstawie pracy (dostępne tylko wtedy, gdy Project Operations jest zainstalowane)</br>- Na podstawie towaru (dostępne tylko wtedy, gdy jest zainstalowane Project Operations i Sales)</br>- Na podstawie wykonania usługi (dostępne po zainstalowaniu Dynamics 365 Field Service) | W przypadku korzystania z aplikacji Project Operations, wartość tego pola jest automatycznie ustawiana na **Na podstawie pracy**. To klasyfikuje tę ofertę jako ofertę opartą na projekcie. Oferta powinna być oparta na projekcie, aby można było włączyć wszystkie rozszerzenia i funkcjonalności specyficzne dla konkretnego projektu. |
| Firma będąca właścicielem | Podsumowanie | Podmiot prawny, który będzie pokrywał koszty i przychody uzyskane z tego projektu lub projektów skojarzonych z ofertą. Gdy oferta jest tworzona z szansy sprzedaży, to pole jest kopiowane z odpowiedniego pola w szansie sprzedaży. | Firma będąca właścicielem to to samo, co koncept osoby prawnej w module **Zarządzanie projektami i księgowaniem** w Project Operations. Wszystkie koszty i przychód powstałe w wyniku tego projektu będą uwzględnione w księdze głównej firmy będącej właścicielem. |
| Ewentualny klient | Karta Podsumowanie | Odwołanie do rekordu firmy lub konta klienta. Prawidłowa identyfikacja klienta w ofercie projektu musi zostać ustawiona na klienta w firmie będącej właścicielem oferty. Firma będąca właścicielem pokazuje listę osób prawnych, które zapisane są w module **Zarządzanie projektami i księgowanie** w Project Operations. Gdy oferta jest tworzona z szansy sprzedaży, to pole jest kopiowane z odpowiedniego pola w szansie sprzedaży. | Waluta w ofercie projektu jest domyślnie oparta na walucie klienta. Można to zmienić przed zapisaniem rekordu. |
| Kierownik ds. klientów | Karta Podsumowanie | Nazwa kierownika ds. klientów odpowiedzialnego za tę transakcję. Gdy oferta jest tworzona z szansy sprzedaży, to pole jest kopiowane z odpowiedniego pola w szansie sprzedaży. | Kierownik ds. klientów jest odpowiedzialny za zarządzanie relacjami z klientem podczas realizacji tego projektu. Bazując na zasobie możliwym do rezerwacji powiązanym z kierownikiem ds. klientów, jednostka kontraktująca będzie domyślnie używać oferty projektowej.|
| Jednostka kontraktująca | Karta Podsumowanie | Jednostka organizacyjna odpowiedzialna za realizację projektu lub projektów skojarzonych z tą ofertą. Gdy oferta jest tworzona z szansy sprzedaży, to pole jest kopiowane z odpowiedniego pola w szansie sprzedaży. | Jednostka zamawiająca to wydział firmy, który będzie odpowiedzialny za wykonanie projektu po zamknięciu transakcji. Każda jednostka zamawiająca korzysta z jakiejś waluty, i ta waluta jest używana do raportowania szacowanych i rzeczywistych kosztów poniesionych podczas wykonywania projektu. |
| Cennik produktu | Karta Podsumowanie | Jest to cennik używany z do domyślnego ustawienia cen w wierszach oferty opartej na produkcie. Lista opcji w tym polu zawiera listę cenników, w których walutą cennika odpowiada walucie w ofercie. Gdy oferta jest tworzona z szansy sprzedaży, to pole jest kopiowane z odpowiedniego pola w szansie sprzedaży. To pole jest domyślnie umieszczone na szansie sprzedaży z poziomu rekordu konta, ale można zmienić jego wartość. | Po wykorzystaniu oferty wartość pola jest kopiowana do tworzonego kontraktu projektu. |
| Waluta | Karta Podsumowanie | Wskazuje to walutę, która będzie używana przy raportowaniu wartości tej transakcji. Jest to również waluta, w której klient będzie fakturowany w przypadku zrealizowania transakcji. Gdy oferta jest tworzona z szansy sprzedaży, to pole jest kopiowane z odpowiedniego pola w szansie sprzedaży. To pole jest domyślnie umieszczone na szansie sprzedaży z poziomu rekordu konta, ale użytkownik może zmienić jego wartość.  | Tego pola nie będzie już można edytować po zapisaniu oferty. Ta funkcja jest używana do tworzenia domyślnych cenników produktów i projektu na ofercie. Waluta w ofercie musi być zgodna z walutą używaną w cenniku. |
| Nieprzekraczalny limit | Karta Podsumowanie | Oznacza to wynegocjowany limit wartości końcowej, który został podany przez klienta podczas negocjowania warunków transakcji. | Ten limit jest oceniana podczas wykonywania i ma zastosowanie we wszystkich pozycjach i projektach skojarzonych z tą transakcją. |
| Żądana data dostawy | Karta Podsumowanie | Gdy oferta jest tworzona z szansy sprzedaży, to pole jest kopiowane z odpowiedniego pola w szansie sprzedaży. | Ta data jest używana jako data zakończenia na potrzeby harmonogramów generowania fakturowania. |

Poniżej przedstawiono karty i wskaźniki KPI dostępne w ofercie projektu, które są unikatowe dla Project Operations, lub dla których istnieją istotne zmiany w stosunku do ofert Sales:

| **Pole** | **Lokalizacja** | **Opis** |
| --- | --- | --- |
| Analiza rentowności | Karta w ofercie | Karta ta zawiera poniższe metryki:</br>- Łączny koszt odpłatny</br></br>- Łączny koszt nieodpłatny</br>- Łączny przychód</br>- Łączny przychód (podstawowy)</br>- Marża brutto</br>- Skorygowana marża brutto|
| Porównanie z oczekiwaniami klienta | Karta w ofercie | Ta karta ta zawiera poniższe metryki:</br>- Szacowane zakończenie</br>- Żądane zakończenie</br>- Budżet klienta</br>- Wartość oferowana |
| Analiza ofert | Karta w ofercie | Na tej karcie są podsumowane poniższe kluczowe wskaźniki wydajności (KPI) dotyczące oferty projektu</br>- Porównanie oczekiwań klientów związanych z budżetem i harmonogramem</br>- Marża brutto</br>- Skorygowana marża brutto |


[!INCLUDE[footer-include](../includes/footer-banner.md)]
