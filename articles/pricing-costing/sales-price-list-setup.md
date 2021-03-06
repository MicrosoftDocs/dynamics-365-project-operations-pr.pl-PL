---
title: Ustawianie cennika sprzedaży
description: Ta temat zawiera informacje na temat list cen sprzedaży w ramach cen projektowych.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 2a66802adfcadab7b4d34149b146ca3cb27c903e
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 09/28/2020
ms.locfileid: "3896474"
---
# <a name="sales-price-list-setup"></a>Ustawianie cennika sprzedaży

_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_

W przypadku ofert i kontraktów projektów cennik projektu zawiera inny wzorzec zastąpienia cen niż cennik produktu. W przypadku wiersza oferty opartej na katalogu produktów można zmienić cenę na role i kategorie bezpośrednio w wierszu oferty, ponieważ każdy wiersz oferty wskazuje dokładnie jeden element katalogu. Jednak w wierszu oferty opartej na projekcie nie można zamienić ceny na role i kategorie bezpośrednio w wierszu oferty. Cennik projektu może służyć do pracy z dwoma różnymi wzorcami zastąpienia.

> [!NOTE]
> Zaleca się, aby w przypadku zasobów projektu i elementów katalogu można było korzystać z osobnego cennika z powodu różnic między nimi podczas ręcznej kalkulacji cen.

Z poszczególnymi encjami może być związany jeden lub więcej cenników skojarzonych z ceną sprzedaży projektu:

- Klient (konto) 
- Szansa sprzedaży 
- Oferta 
- Kontrakt projektu

Skojarzenie tych encji z cennikiem jest wskazane przez cenniki projektu. Istnieje możliwość skojarzenia jednego lub kilku cenników z encjami sprzedaży Klient, Szansa sprzedaży, Oferta i Kontrakt projektu.

Domyślny cennik nie jest automatycznie wprowadzany w rekordzie klienta. Można jednak ręcznie dołączyć Cennik projektu do rekordu klienta. Jednak Cennik należy dołączać ręcznie tylko wtedy, gdy użytkownik ma zainstalowaną niestandardową umowę cenową z klientem. 

Gdy Cennik projektu jest dołączony do encji sprzedaży, program sprawdza poprawność następujących informacji:

- Cennik ma kontekst **Sprzedaż**. 
- Waluta cennika jest zgodna z walutą klienta. 

W kontrakcie dotyczącym projektu, wykorzystywana jest następująca kolejność pierwszeństwa, aby automatycznie określać powiązane z nimi cenniki projektu:

1. Oferta
2. Szansa sprzedaży
3. Klient 
4. Ustawienia globalne 

Kiedy Cennik projektu jest wprowadzany domyślnie, system sprawdza poprawność waluty odpowiadającej walucie klienta i, że wprowadzone cenniki domyślne mają kontekst **sprzedaży**.

Istnieje możliwość skojarzenia kilku cenników projektów z encjami sprzedaży Klient, Szansa sprzedaży, Oferta i Kontrakt projektu. Ta funkcja obsługuje specyficzne dla konkretnego kontraktu ceny domyślne na długo działającym kontrakcie projektu, w którym może zaistnieć potrzeba więcej niż jednego cennika w celu zaktualizowania cen ze względu na inflację. Jeśli jednak cenniki skojarzone z encją klient, szansa sprzedaży, oferta lub kontrakt projektu mają nachodzącą na nią datę obowiązywania, cena domyślna może być nieprawidłowa. Dlatego należy się upewnić, że cenniki z nakładającymi się datami nie są skojarzone z tymi encjami.
