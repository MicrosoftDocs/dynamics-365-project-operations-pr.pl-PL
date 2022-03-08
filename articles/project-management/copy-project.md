---
title: Kopiowanie projektu
description: Ten temat zawiera informacje o kopiowaniu projektów w rozwiązaniu Dynamics 365 Project Operations.
author: ruhercul
ms.date: 05/21/2021
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: fe76f59b315fd0f46b25e1d116acde1f6b2864d1753e01d6311ea93ae7d116fc
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/06/2021
ms.locfileid: "7007204"
---
# <a name="copy-a-project"></a>Kopiowanie projektu

_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_

Za pomocą programu Dynamics 365 Project Operations można szybko tworzyć nowe projekty, wybierając pozycję **Kopiuj projekt** w formularzu **Projekty**. Aby skopiować projekt, otwórz go, a następnie wybierz opcję **Kopiuj projekt**. Czynność ta skopiuje:

- Właściwości projektu 
- Struktura podziału pracy
- Członkowie zespołu projektu
- Szacowania projektu
- Szacunki kosztów projektu
- Oszacowanie materiałów projektowych

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
- Szacowana data rozpoczęcia: Jest to data, kiedy projekt zostanie utworzony z kopii.
- Szacowana data zakończenia: Ta data jest dostosowywana na podstawie daty rozpoczęcia nowego projektu, który został wykonany na podstawie kopii.
- Nakład pracy (godziny)
- Szacowany koszt robocizny
- Szacowany koszt wydatków
- Szacowany koszt materiałowy

> [!NOTE]
> Kopiowanie projektu to operacja, która trwa długi czas. Kopiowane są również rekordy projektu, ich odpowiednie atrybuty oraz wiele powiązanych z nimi encji. Ze względu na długi czas trwania operacji, po rozpoczęciu kopiowania docelowa strona projektu jest zablokowana do edycji aż do zakończenia operacji kopiowania.

## <a name="work-breakdown-structure"></a>Struktura podziału pracy

Podczas kopiowania projektu zostanie skopiowana cała struktura podziału prac załadowana do zasobu. Nazwane zasoby zostaną zastąpione zasobami ogólnymi. Jeśli nazwane zasoby nie korzystają z takich samych godzin pracy, jak zasób ogólny, harmonogram zostanie ponownie obliczony, a czas trwania zadań mogą ulec zmianie.

## <a name="project-team-members"></a>Członkowie zespołu projektu

W przypadku kopiowania zespołu projektu z projektu źródłowego, zasoby ogólne zostaną także skopiowane. Przypisania zasobów ogólnych są także obsługiwane jak w projekcie źródłowym. Nazwane zasoby zostaną przekonwertowane dla ogólnych członków zespołu.

## <a name="estimates"></a>Szacunki

Podczas kopiowania projektu z projektu źródłowego kopiowane są wiersze kosztorysu zasobów, wydatków i materiałów. 

Informacje na temat sposobu programowego uzyskiwania dostępu do kopiowania projektów można znaleźć w artykule [projektowanie szablonów projektów przy użyciu narzędzia do kopiowania projektów](dev-copy-project.md).


[!INCLUDE[footer-include](../includes/footer-banner.md)]
