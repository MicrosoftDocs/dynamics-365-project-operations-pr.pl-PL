---
title: Kopiowanie projektu
description: Ten temat zawiera informacje o kopiowaniu projektów w rozwiązaniu Dynamics 365 Project Operations.
author: ruhercul
ms.date: 03/07/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: e9b637d2d282d123dfacb8a295292ea06549aa1e
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/14/2022
ms.locfileid: "8574443"
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
- Listy kontrolne projektu
- Zasobniki projektów

## <a name="project-properties"></a>Właściwości projektu

Podczas kopiowania projektu są kopiowane wartości z następujących pól.

| Pole | Project Operations materiały niemagazynowane | Project Operations Lite | Project for the Web |
|-------|------------------------------------------|-------------------------|---------------------|
| Imię i nazwisko/nazwa | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: |
| Description | :heavy_check_mark: | :heavy_check_mark: | |
| kliencie | :heavy_check_mark: | :heavy_check_mark: | |
| Szablon kalendarza | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: |
| Waluta | :heavy_check_mark: | :heavy_check_mark: | |
| Jednostka kontraktująca | :heavy_check_mark: | :heavy_check_mark: | |
| Firma będąca właścicielem | :heavy_check_mark: | | |
| Menedżer projektu | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: |
| Status | :heavy_check_mark: | :heavy_check_mark: | |
| Ogólny stan projektu | :heavy_check_mark: | :heavy_check_mark: | |
| Komentarze | :heavy_check_mark: | :heavy_check_mark: | |
| Szacunki | :heavy_check_mark: | :heavy_check_mark: | |
| <p>Szacowana data rozpoczęcia</p><p><strong>Uwaga:</strong> to pole określa datę utworzenia projektu na podstawie kopii. | :heavy_check_mark: | :heavy_check_mark: | |
| <p>Szacowana data zakończenia</p><p><strong>Uwaga:</strong> data w tym polu jest dostosowywana na podstawie daty rozpoczęcia nowego projektu wykonanego z kopii.</p> | :heavy_check_mark: | :heavy_check_mark: | |
| Nakład pracy (godziny) | :heavy_check_mark: | :heavy_check_mark: | |
| Szacowany koszt robocizny | :heavy_check_mark: | :heavy_check_mark: | |
| Szacowany koszt wydatków | :heavy_check_mark: | :heavy_check_mark: | |
| Szacowany koszt materiałowy | | :heavy_check_mark: | |

> [!NOTE]
> Kopiowanie projektu to operacja, która trwa długi czas. Kopiowane są również rekordy projektu, ich odpowiednie atrybuty oraz wiele powiązanych z nimi encji. Ze względu na długi czas trwania operacji, po rozpoczęciu kopiowania docelowa strona projektu jest zablokowana do edycji aż do zakończenia operacji kopiowania.

## <a name="work-breakdown-structure"></a>Struktura podziału pracy

Podczas kopiowania projektu zostanie skopiowana cała struktura podziału prac załadowana do zasobu. Nazwane zasoby zostaną zastąpione zasobami ogólnymi. Jeśli nazwane zasoby nie mają tych samych godzin pracy co zasób ogólny, harmonogram zostanie przeliczone i mogą ulec zmianie czasy trwania zadania.

## <a name="project-team-members"></a>Członkowie zespołu projektu

W przypadku kopiowania zespołu projektu z projektu źródłowego, zasoby ogólne zostaną także skopiowane. Przypisania zasobów ogólnych są także obsługiwane jak w projekcie źródłowym. Nazwane zasoby zostaną przekonwertowane dla ogólnych członków zespołu.

> [!NOTE]
> Członkowie zespołu i przypisania nie są kopiowane do witryny Project for the Web.

## <a name="estimates"></a>Szacunki

Podczas kopiowania projektu z projektu źródłowego kopiowane są wiersze kosztorysu zasobów, wydatków i materiałów. 

Informacje na temat sposobu programowego uzyskiwania dostępu do kopiowania projektów można znaleźć w artykule [projektowanie szablonów projektów przy użyciu narzędzia do kopiowania projektów](dev-copy-project.md).

## <a name="quotes-and-contracts"></a>Oferty i kontrakty

Oferty i kontrakty nie są łączone z projektem docelowym.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
