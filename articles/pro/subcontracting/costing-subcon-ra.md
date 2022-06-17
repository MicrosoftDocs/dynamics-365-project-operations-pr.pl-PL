---
title: Szacowanie kosztów przypisań zasobów w ramach podwykonawstwa
description: W tym artykule objaśniono, jak aplikacja Microsoft Dynamics 365 Project Operations oblicza szacowanie kosztów przypisań zasobów w ramach podwykonawstwa.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 40603c1d2dfdd49909d9a4bf5085f43201e8f6bd
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8932355"
---
# <a name="cost-estimation-of-subcontracted-resource-assignments"></a>Szacowanie kosztów przypisań zasobów w ramach podwykonawstwa

[!include [banner](../../includes/dataverse-preview.md)]

_**Zastosowane w:** Wdrażanie uproszczone — od okazji do faktury pro forma_

Przypisania zadań członków zespołu projektowego w ramach podwykonawstwa są wyceniane przy użyciu cennika **Zakup** dołączonego do podumowy w pokrewnym rekordzie członka zespołu. Jest to inny sposób niż w przypadku przypisań zasobów pracowników, gdzie przypisania zadań z zasobów pracowników są wyceniane przy użyciu cennika **Koszt** dołączonego do jednostki kontraktowania projektu. 

W przypadku członków ogólnego zespołu projektowego w ramach podwykonawstwa wycena jest przeprowadzana przy użyciu konfiguracji cen opartej na rolach w cenniku zakupów dołączonym do podumowy. Ceny zakupu można także skonfigurować specjalnie dla każdego zasobu. Te ceny specyficzne dla zasobów będą mieć priorytet podczas wyceny przypisań zadań nazwanych członków zespołu projektowego, którzy są pracownikami kontraktowymi. 

Priorytet używania ceny zakupu specyficznej dla roli w porównaniu z ceną specyficzną dla zasobu opiera się na konfiguracji priorytetu wymiarów cen w obszarze **Parametry > Wymiary kalkulacji cen oparte na kwocie**.

Ta funkcja dynamicznego określanie cen pochodny w oparciu o konfigurację wymiarów cen zakupu dla podwykonawców jest podobna do sposobu, w jaki są określane pochodne wskaźniki kosztów i rozliczeń dla pracowników pełnoetatowych. 

## <a name="creating-task-assignments-for-getting-cost-estimates-of-subcontractor-resources"></a>Tworzenie przypisań zadań na potrzeby uzyskiwania szacowań kosztów zasobów podwykonawców

Przypisania zadań do podwykonawców można tworzyć na dwa sposoby: 
- Przy użyciu karty **Zadania**.
- Przy użyciu karty **Zespół**.

### <a name="creating-resources-assignments-using-the-tasks-tab"></a>Tworzenie przypisań zasobów przy użyciu karty Zadania
Korzystając z listy **Zasoby** na karcie **Zadania** dla określonego zadania, można utworzyć przypisanie zadania dla zasobu nazwanego lub ogólnego. Jeśli z listy rozwijanej **Przypisane zasoby** wybierzesz zasób nazwany dla zadania, a ten zasób jest pracownikiem kontraktowym, nazwany zasób zostanie przypisany do zadania, a odpowiedni rekord członka zespołu projektowego zostanie utworzony z typem pracownika ustawionym na **Pracownik kontraktowy** i **ważnością** ustawioną na **Nieprawidłowy**. W następnym kroku będzie trzeba otworzyć rekord członka zespołu projektowego, a następnie wybrać podumowę i wiersz podumowy. Spowoduje to zaktualizowanie przypisania zadania w taki sposób, aby zawierało odwołanie do podumowy i wiersza podumowy, a także zaktualizowanie stanu członka zespołu do wartości **Prawidłowa**.

W przypadku utworzenia członka zespołu ogólnego z listy rozwijanej **Przypisane zasoby** dla zadania okno dialogowe **Tworzenie ogólnego członka zespołu** umożliwi wybranie podumowy i wiersza podumowy. Gdy zasób ogólny zostanie przypisany do zadania i zostanie utworzony odpowiedni rekord członka zespołu projektowego, zauważysz, że utworzony rekord członka zespołu projektowego ma typ pracownika ustawiony na **Pracownik kontraktowy** i **ważność** ustawioną na **Prawidłowy**.

### <a name="creating-project-team-members-using-the-team-tab"></a>Tworzenie członków zespołu projektowego przy użyciu karty Zespół
Korzystając z karty Zespół w projekcie, można utworzyć ogólnego lub nazwanego członka zespołu. Podczas tworzenia członka zespołu można wybrać podumowę i wiersz podumowy. Po utworzeniu członka zespołu należy przypisać go do zadania przy użyciu listy rozwijanej **Przypisane zasoby** dla zadania. 

## <a name="updating-estimates"></a>Aktualizowanie szacowań
Po przypisaniu członków zespołu projektowego do zadań należy przejść do karty **Szacowania** w projekcie i wybrać opcję **Aktualizuj ceny**, aby zagwarantować, że wskaźniki kosztów przypisań zasobów podwykonawców są aktualizowane na podstawie cennika zakupu dołączonego do podumowy. Szacowanie nie są generowane dla nieprzypisanych zadań w aplikacji Microsoft Dynamics 365 Project Operations. W wyniku należy utworzyć przypisania zadań do różnych zadań związanych z ceną i kosztami projektów. 

> [UWAGA!] Członkowie zespołu projektowego, którzy mają **Typ pracownika** ustawiony na **Pracownik kontraktowy**, ale nie mają odwołania podumowy, są oznaczani jako **Nieprawidłowy** w siatce **Członkowie zespołu projektowego**. Jeśli któryś z członków zespołu projektowego ma ten stan, otwórz rekord członka zespołu projektowego i ręcznie zaktualizuj pola podumowy i wiersza podumowy, aby szacowanie kosztu finansowego dokładnie odzwierciedlało koszt podwykonawcy na karcie **Szacowania**. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
