---
title: Nagłówek szansy sprzedaży
description: Ten temat zawiera informacje na temat ogólnych informacji o transakcjach opartych na projektach oraz o wierszach szans sprzedaży opartych na projektach.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 2f08de54767f49c308d0ccc7f2e1c6ef880b7f99
ms.sourcegitcommit: a0f80d024a5d3112a39781815bd31d0c05ddaf6f
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 09/30/2020
ms.locfileid: "3906279"
---
# <a name="opportunity-header"></a>Nagłówek szansy sprzedaży

_**Zastosowane w:** Wdrażanie uproszczone — od okazji do faktury pro forma_

Nagłówek szansy sprzedaży zawiera ogólne informacje dotyczące transakcji opartej na projekcie, które dotyczą wszystkich wierszy z szansy sprzedaży opartej na projekcie.

Szanse sprzedaży w programie Dynamics 365 Project Operations są rozszerzeniami szans sprzedaży w Dynamics 365 Sales. Te rozszerzenia zapewniają dodatkowe funkcje, które są właściwe dla i wymagane w przypadku szans sprzedaży na podstawie projektów. Rozszerzenia mogą zawierać nowe pola i czynności dostępne na wstążce, dostępne w szansach sprzedaży opartych na projektach. Niektóre pola, funkcje i logika domyślna, które są dostępne w Sales, mogą nie być dostępne w Project Operations.

Poniższa tabela zawiera pola szansy sprzedaży opartej na projekcie, które są unikatowe dla Project Operations lub mają istotne zmiany w sposobie zachowania się z szans sprzedaży z Sales.

| **Pole** | **Lokalizacja** | **Stopień zgodności, cel i wskazówki** | **Wpływ zmian w dalszych etapach** |
| --- | --- | --- | --- |
| Pisz | Karta Ogólne (ukryta) | To pole zestawu opcji zawiera następujące opcje:</br>- Na podstawie pracy (dostępne tylko w Project Operations)</br>- Na podstawie towaru (dostępne tylko wtedy, gdy jest zainstalowane Project Operations i Sales)</br>- Na podstawie wykonania usługi (dostępne po zainstalowaniu Field Service) | W przypadku korzystania z aplikacji Project Operations, wartość tego pola jest automatycznie ustawiana na **Na podstawie pracy**, co klasyfikuje szansę sprzedaży jako opartą na projekcie. Szansa sprzedaży oparta na projekcie jest wymagana do włączenia wszystkich rozszerzeń specyficznych dla danego projektu i funkcji w ramach procesu sprzedaży na niższym szczeblu w zakresie omawianej transakcji. |
| Kontakt biznesowy | Karta Ogólne | Odwołanie do podstawowego kontaktu klienta związanego z daną transakcją. | |
| Konto | Karta Ogólne | Odwołanie do rekordu firmy lub konta klienta. | |
| Kierownik ds. klientów | Karta Ogólne | Nazwa kierownika ds. klientów odpowiedzialnego za tę szansę sprzedaży opartą na projekcie. | Kierownik ds. klientów jest odpowiedzialny za zarządzanie relacjami z klientem podczas realizacji tego projektu. Bazując na zasobie możliwym do rezerwacji powiązanym z kierownikiem ds. klientów, jednostka kontraktująca będzie domyślnie wybrana. |
| Jednostka kontraktująca | Karta Ogólne | Jednostka organizacyjna odpowiedzialna za realizację projektu lub projektów skojarzonych z tą transakcją. | Jednostka zamawiająca to wydział firmy, który będzie odpowiedzialny za ukończenie projektu po zamknięciu transakcji. Każda jednostka zamawiająca korzysta z jakiejś waluty, i ta waluta jest używana do raportowania szacowanych i rzeczywistych kosztów poniesionych podczas projektu. |

W przypadku wszystkich innych pól i sekcji na karcie **Podsumowanie** w szansy sprzedaży zobacz [Tworzenie i edytowanie szans sprzedaży (Sales i Centrum sprzedaży)](https://docs.microsoft.com/dynamics365/sales-enterprise/create-edit-opportunity-sales)
