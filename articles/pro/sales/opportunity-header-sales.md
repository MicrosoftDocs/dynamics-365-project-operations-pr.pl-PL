---
title: Ustawienia szansy sprzedaży - wersja uproszczona
description: Ta temat zawiera informacje na temat transakcji opartych na projektach oraz wierszach szans sprzedaży opartych na projektach.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: ed82cb511337d9f6286e13b244d049022a184eef
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/27/2021
ms.locfileid: "5950637"
---
# <a name="header-details-for-project-opportunities"></a>Szczegóły nagłówka dla szans sprzedaży projektu

_**Zastosowane w:** Wdrażanie uproszczone — od okazji do faktury pro forma_

Nagłówek szansy sprzedaży zawiera ogólne informacje dotyczące transakcji opartej na projekcie, które dotyczą wszystkich wierszy z szansy sprzedaży opartej na projekcie.

Możliwości oparte na projekcie w rozwiązaniu Dynamics 365 Project Operations są rozszerzeniami szans sprzedaży w systemie Dynamics 365 Sales. Te rozszerzenia zapewniają dodatkowe funkcje, które są właściwe dla i wymagane w przypadku szans sprzedaży na podstawie projektów. Rozszerzenia mogą zawierać nowe pola i czynności dostępne na wstążce, dostępne w szansach sprzedaży opartych na projektach. Niektóre pola, funkcje i logika domyślna, które są dostępne w Sales, mogą nie być dostępne w Project Operations.

Poniższa tabela zawiera pola szansy sprzedaży opartej na projekcie, które są unikatowe dla Project Operations lub mają istotne zmiany w sposobie zachowania się z szans sprzedaży z Sales.

| **Pole** | **Lokalizacja** | **Opis** | **Wpływ zmian w dalszych etapach** |
| --- | --- | --- | --- |
| Pisz | Karta Ogólne (ukryta) | To pole zestawu opcji zawiera następujące opcje:</br>- Na podstawie pracy (dostępne tylko w Project Operations)</br>- Na podstawie towaru (dostępne tylko wtedy, gdy jest zainstalowane Project Operations i Sales)</br>- Na podstawie wykonania usługi (dostępne po zainstalowaniu Field Service) | W przypadku korzystania z aplikacji Project Operations, wartość tego pola jest automatycznie ustawiana na **Na podstawie pracy**, co klasyfikuje szansę sprzedaży jako opartą na projekcie. Szansa sprzedaży oparta na projekcie jest wymagana do włączenia wszystkich rozszerzeń specyficznych dla danego projektu i funkcji w ramach procesu sprzedaży na niższym szczeblu w zakresie omawianej transakcji. |
| Kontakt biznesowy | Karta Ogólne | Odwołanie do podstawowego kontaktu klienta związanego z daną transakcją. | |
| Konto | Karta Ogólne | Odwołanie do rekordu firmy lub konta klienta. | |
| Kierownik ds. klientów | Karta Ogólne | Nazwa kierownika ds. klientów odpowiedzialnego za tę szansę sprzedaży opartą na projekcie. | Kierownik ds. klientów jest odpowiedzialny za zarządzanie relacjami z klientem podczas realizacji tego projektu. Bazując na zasobie możliwym do rezerwacji powiązanym z kierownikiem ds. klientów, jednostka kontraktująca będzie domyślnie wybrana. |
| Jednostka kontraktująca | Karta Ogólne | Jednostka organizacyjna odpowiedzialna za realizację projektu lub projektów skojarzonych z tą transakcją. | Jednostka zamawiająca to wydział firmy, który będzie odpowiedzialny za ukończenie projektu po zamknięciu transakcji. Każda jednostka zamawiająca korzysta z jakiejś waluty, i ta waluta jest używana do raportowania szacowanych i rzeczywistych kosztów poniesionych podczas projektu. |

W przypadku wszystkich innych pól i sekcji na karcie **Podsumowanie** w szansy sprzedaży zobacz [Tworzenie i edytowanie szans sprzedaży (Sales i Centrum sprzedaży)](/dynamics365/sales-enterprise/create-edit-opportunity-sales)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
