---
title: Kopiowanie projektu
description: W tym temacie zamieszczono informacje o kopiowaniu projektu w Dynamics 365 Project Operations.
author: ruhercul
manager: AnnBe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: e35dc725e7938e9f59f7151dd1b37500fabf77a4
ms.sourcegitcommit: 56c42d7f5995a674426a1c2a81bae897dceb391c
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/01/2020
ms.locfileid: "3908451"
---
# <a name="copy-a-project"></a>Kopiowanie projektu

_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_

Korzystając z Dynamics 365 Project Operations można szybko budować nowe projekty, dzięki działaniu o nazwie **Kopiowanie projektów**, dostępnej w formularzu **Projekty**. Aby skopiować projekt, wybierz go, a następnie wybierz pozycję **Kopiuj**. Zostaną skopiowane następujące elementy:

- Właściwości projektu
- Struktura podziału pracy
- Członkowie zespołu projektu
- Szacowania projektu
- Szacunki kosztów projektu

## <a name="project-properties"></a>Właściwości projektu

Podczas kopiowania projektu są kopiowane wartości z następujących pól:

- Nazwa/nazwisko
- Opis
- Klient
- Szablon kalendarza
- Waluta
- Jednostka kontraktująca
- Menedżer projektu
- Status
- Ogólny stan projektu
- Komentarze
- Szacunki
- Szacowana data rozpoczęcia
- Data zakończenia
- Nakład pracy (godziny)
- Szacowany koszt robocizny
- Szacowany koszt wydatków

## <a name="work-breakdown-structure"></a>Struktura podziału pracy

Podczas kopiowania projektu zostanie skopiowana cała struktura podziału prac załadowana do zasobu. Nazwane zasoby zostaną zastąpione zasobami ogólnymi. Jeśli nazwane zasoby nie korzystają z takich samych godzin pracy, jak zasób ogólny, harmonogram zostanie ponownie obliczony, a czas trwania zadań mogą ulec zmianie.

## <a name="project-team-members"></a>Członkowie zespołu projektu

W przypadku kopiowania zespołu projektu z projektu źródłowego, zasoby ogólne zostaną także skopiowane. Przypisania zasobów ogólnych są także obsługiwane jak w projekcie źródłowym. Nazwane zasoby zostaną przekonwertowane dla ogólnych członków zespołu.

## <a name="estimates"></a>Szacunki

Po skopiowaniu projektu wiersze szacowania zasobu i wydatku są kopiowane z projektu źródłowego.