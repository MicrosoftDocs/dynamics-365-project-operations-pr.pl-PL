---
title: Kopiowanie projektu
description: W tym temacie zamieszczono informacje o kopiowaniu projektu w Dynamics 365 Project Operations.
author: ruhercul
manager: AnnBe
ms.date: 10/07/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: cf80f2a1cd27aae33d123e45dee70d94ea4d01a9
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081953"
---
# <a name="copy-a-project"></a>Kopiowanie projektu

_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_

Korzystając z Dynamics 365 Project Operations można szybko budować nowe projekty, wybierając opcję **Kopiowanie projektów** w formularzu **Projekty**. Aby skopiować projekt, otwórz go, a następnie wybierz opcję **Kopiuj projekt**. Zostaną skopiowane następujące elementy:

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

Informacje na temat sposobu programowego uzyskiwania dostępu do kopiowania projektów można znaleźć w artykule [projektowanie szablonów projektów przy użyciu narzędzia do kopiowania projektów](dev-copy-project.md).
