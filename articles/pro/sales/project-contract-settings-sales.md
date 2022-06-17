---
title: Ustawienia kontraktu projektu - wersja uproszczona
description: W tym artykule przedstawiono informacje o polach, które mają wpływ na pozycje kontraktu, oraz informacje dotyczące kontraktu sumowane dla wszystkich pozycji.
author: rumant
ms.date: 03/08/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 6123cbc028cf49cc198173697969f415b0789256
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8917083"
---
# <a name="header-details-for-project-contracts"></a>Szczegóły nagłówka dla kontraktów projektu

_**Zastosowane w:** Wdrażanie uproszczone — od okazji do faktury pro forma_

W tym artykule opisano pola dotyczące całego kontraktu projektu, w tym ustawienia, które mają wpływ na wszystkie pozycję kontraktu. Dołączone są również informacje na temat kontraktu, który został podsumowany we wszystkich sumach pozycji w celu tworzenia wskaźników KPI kontraktu projektu.

W poniższej tabeli wymieniono pola informacji podsumowującej w kontrakcie projektu, które są unikatowe dla rozwiązania Dynamics 365 Project Operations lub zawierają pewne istotne zmiany w zachowaniu z zamówień sprzedaży w systemie Dynamics 365 Sales.

| Pole | Lokalizacja | Opis | Wpływ zmian w dalszych etapach |
| --- | --- | --- | --- |
| Pisz | Karta **Podsumowanie** (ukryte) | To pole zestawu opcji zawiera następujące opcje:</br>- **Na podstawie pracy** (dostępne tylko wtedy, gdy Project Operations jest zainstalowane)</br>- **Na podstawie towaru** (dostępne tylko wtedy, gdy jest zainstalowane Project Operations i Sales)</br>- **Na podstawie wykonania usługi** (dostępne po zainstalowaniu Dynamics 365 Field Service) | W Project Operations wartość domyślna tego pola jest określana jako **Oparta na pracy** i klasyfikuje kontrakt jako oparty na projektach. Kontrakt powinna być oparty na projekcie, aby można było włączyć wszystkie rozszerzenia i funkcjonalności specyficzne dla konkretnego projektu. |
| Ewentualny klient | Karta **Podsumowanie** | Odwołanie do rekordu firmy klienta lub konta klienta. Gdy kontrakt jest tworzony z oferty, to pole jest kopiowane z odpowiedniego pola w ofercie. | Waluta w kontrakcie projektu jest domyślnie oparta na walucie klienta. Można to zmienić przed zapisaniem kontraktu. |
| Kierownik ds. klientów | Karta **Podsumowanie** | Nazwa kierownika ds. klientów odpowiedzialnego za tę transakcję. Gdy kontrakt jest tworzony z oferty, to pole jest kopiowane z odpowiedniego pola w ofercie. | Kierownik ds. klientów jest odpowiedzialny za zarządzanie relacjami z klientem podczas realizacji tego projektu. Bazując na zasobie możliwym do rezerwacji powiązanym z kierownikiem ds. klientów, jednostka kontraktująca będzie domyślnie używać kontraktu. |
| Jednostka kontraktująca | Karta **Podsumowanie** | Jednostka organizacyjna odpowiedzialna za realizację projektów skojarzonych z tym kontraktem. Gdy kontrakt jest tworzony z oferty, to pole jest kopiowane z odpowiedniego pola w ofercie. | Jednostka zamawiająca to wydział firmy, który wykonuje projekt. Każda jednostka zamawiająca korzysta z jakiejś waluty, i ta waluta jest używana do raportowania szacowanych i rzeczywistych kosztów poniesionych podczas projektu. |
| Cennik produktu | Karta **Podsumowanie** | Jest to cennik używany do domyślnego ustawienia cen w pozycjach kontraktu opartego na produkcie. Lista opcji w tym polu zawiera rozwijaną listę cenników, w których walutą cennika odpowiada walucie w kontrakcie. Gdy kontrakt jest tworzony z oferty, to pole jest kopiowane z odpowiedniego pola w ofercie. To pole jest domyślnie umieszczone w kontrakcie z poziomu rekordu konta, ale można zmienić jego wartość. | W tym polu nie ma wpływu zmian na dalsze etapy. |
| Waluta | Karta **Podsumowanie** | Waluta użyta do zaraportowania wartości tej transakcji oraz waluta, w której klient będzie fakturowany. Gdy kontrakt jest tworzony z oferty, to pole jest kopiowane z odpowiedniego pola w ofercie. To pole jest domyślnie umieszczone w kontrakcie z poziomu rekordu konta, ale można zmienić jego wartość. | Tego pola nie będzie już można edytować po zapisaniu kontraktu. To pole jest używane do tworzenia domyślnych cenników produktów i projektu w kontrakcie. Waluta w kontrakcie musi być zgodna z walutą używaną w cenniku. |
| Nieprzekraczalny limit | Karta **Podsumowanie** | To pole zawiera wynegocjowany limit wartości końcowej, który został potwierdzony przez klienta podczas negocjowania warunków transakcji. | Ten limit jest oceniany podczas wykonywania i ma zastosowanie we wszystkich pozycjach i projektach skojarzonych z tą transakcją. |
| Żądana data dostawy | Karta **Podsumowanie** | Gdy kontrakt jest tworzony z oferty projektowej, to pole jest kopiowane z odpowiedniego pola w ofercie projektowej. | Ta data jest używana jako data zakończenia na potrzeby tworzenia harmonogramów fakturowania. |

Poniższe wskaźniki KPI są dostępne na karcie **Wydajność kontraktu** w kontrakcie projektu. 

>[!NOTE]
>Wszystkie kwoty na karcie **Wydajność kontraktu** są wyrażane w domyślnej walucie środowiska.

| Pole | Lokalizacja | Description |
| --- | --- | --- |
| Wartość kontraktu | Kontrakt ogólny | Łączna wartość kontraktu dotyczącego projektu.|
| Rozliczona kwota | Kontrakt ogólny | Suma kwot na wszystkich fakturach objętych tym kontraktem.|
| Koszt poniesiony | Kontrakt ogólny | Suma wszystkich wartości rzeczywistych kosztów zarejestrowanych we wszystkich projektach, które są zamapowane na dany kontrakt. |
| Marża brutto | Kontrakt ogólny | Kwota na fakturze — koszt poniesiony do dnia / koszt rozliczony |
| Oczekiwana marża | Kontrakt ogólny | (Wartość kontraktu — koszty szacowane) / wartość kontraktu szacowane koszty = suma wszystkich kosztów szacunkowych dla wszystkich projektów zamapowanych na dany kontrakt.|
| Wartość kontraktu | Wiersze oparte na projektach | Wartość pozycji kontraktu. |
| Kwota rozliczona | Wiersze oparte na projektach | W przypadku pozycji kontraktu o stałej cenie: suma kwot wszystkich wartości rzeczywistych punktów kontrolnych fakturowania sprzedaży w stosunku do tej pozycji kontraktu na różnych fakturach tworzonych dla danego kontraktu. W przypadku pozycji kontraktu czasu i materiałów: suma kwot wszystkich odpłatnych wartości rzeczywistych fakturowania sprzedaży w stosunku do tej pozycji kontraktu na różnych fakturach tworzonych dla danego kontraktu. |
| Koszt poniesiony | Wiersze oparte na projektach | Suma wszystkich wartości rzeczywistych kosztów zarejestrowanych we wszystkich projektach, które są zamapowane na daną pozycję kontraktu. |
| Marża brutto | Wiersze oparte na projektach | (Kwota na fakturze — koszt poniesiony do dnia) / koszt rozliczony |
| Oczekiwana marża | Wiersze oparte na projektach | (Kwota pozycji kontraktu w walucie podstawowej — koszty szacowane dla pozycji kontraktu w walucie podstawowej) / kwota pozycji kontraktu w walucie podstawowej |
| Koszt poniesiony | Szczegóły wiersza opartego na projekcie | Czas: suma ilości czasu rzeczywistych kosztów zarejestrowanych dla roli w projekcie zamapowana na tę pozycję kontraktu. Wydatki: suma ilości czasu wszystkich wydatków zarejestrowanych dla kategorii w projekcie zamapowana na tę pozycję kontraktu. |
| Zarejestrowana ilość | Szczegóły wiersza opartego na projekcie | Czas: łączna ilość czasu dla rzeczywistych kosztów dla roli w projekcie zamapowanej na tę pozycję kontraktu. Wydatki: wszystkie ilości czasu dla kategorii wydatków w ramach wartości rzeczywistych kosztów w projekcie zamapowana na tę pozycję kontraktu. |
| Rozliczona kwota | Szczegóły wiersza opartego na projekcie | W przypadku pozycji kontraktu o stałej cenie to pole pozostaje puste na poziomie szczegółowości i będzie widoczne tylko na poziomie pozycji kontraktu. W przypadku pozycji kontraktu typu czas i materiały obliczenia są wykonywane na poziomie szczegółów. Szczegóły pokazują sumę kwoty we wszystkich wierszach przychodu na podstawie wszystkich odpłatnych pozycji kontraktu. |
| Rozliczona ilość | Szczegóły wiersza opartego na projekcie | W przypadku pozycji kontraktu o stałej cenie to pole pozostaje puste na poziomie szczegółowości i będzie widoczne tylko na poziomie pozycji kontraktu. W przypadku pozycji kontraktu typu czas i materiały obliczenia są wykonywane na poziomie szczegółów dla czasu i wydatków. Czas: Szczegóły pokazują godziny we wszystkich wierszach przychodu dla roli względem wszystkich odpłatnych pozycji kontraktu. Wydatki: wszystkie ilości czasu dla kategorii wydatków w ramach wartości rzeczywistych kosztów w projekcie zamapowana na tę pozycję kontraktu. |
| Wartość kontraktu | Wiersze oparte na produktach | Wartość pozycji kontraktu w stosunku do tej pozycji kontraktu opartej na produkcie. |
| Rozliczona kwota | Wiersze oparte na produktach | Suma kwot we wszystkich wierszach faktury względem pozycji kontraktu opartego na produkcie na różnych fakturach tworzonych dla danego kontraktu. |
| Koszt poniesiony | Wiersze oparte na produktach | Suma wszystkich wartości rzeczywistych dla pozycji kontraktu opartego na produktach. |
| Marża brutto | Wiersze oparte na projektach | Kwota na fakturze — koszt poniesiony do dnia / koszt rozliczony |
| Oczekiwana marża | Wiersze oparte na produktach | (Wartość pozycji kontraktu — szacowane koszty pozycji kontraktu) / wartość pozycji kontraktu |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
