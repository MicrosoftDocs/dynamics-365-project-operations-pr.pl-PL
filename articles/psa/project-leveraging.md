---
title: Szacowania sprzedaży w projektach
description: W tym temacie zamieszczono informacje dotyczące sposobu korzystania z mechanizmów harmonogramów i szacunków w procesie sprzedaży.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 76e21f80e51e6f3092880dc629ba90b400805486
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/10/2021
ms.locfileid: "5148386"
---
# <a name="sales-estimates-and-projects"></a>Szacowania sprzedaży w projektach

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Podczas procesu sprzedaży można tworzyć oszacowania sprzedaży poprzez powiązanie projektu z ofertą sprzedaży. W ten sposób w procesie sprzedaży może nastąpić oszacowanie deterministyczne wykorzystujące funkcje planowania i szacowania dostępne w projektach. Jeśli sprzedaż zostanie pomyślnie sfinalizowana, harmonogramu użytego do celów oszacowania sprzedaży można użyć jako bazy do dalszego dopracowywania planu projektu.

## <a name="linking-a-project-to-a-quote-line"></a>Łączenie projektu z wierszem oferty

Podczas tworzenia wiersza oferty opartej na projekcie można na stronie **Wiersz oferty** utworzyć nowy projekt lub skojarzyć istniejący projekt. 

> ![Formularz Wiersz oferty](media/project-8.png)
 
Podczas tworzenia nowego projektu na podstawie szczegółów wiersza oferty można skorzystać z szablonów projektów. Szablony projektów są projektami modelowymi, które reprezentują standardowe plany projektów i oszacowania finansowe typowe w organizacji. Mogą one także stanowić kopie planów projektów i oszacowań z przeszłych projektów.

> ![Szczegóły wiersza oferty](media/project-9.png)
  
Podczas tworzenia projektu z oferty projekt jest automatycznie kojarzony z wierszem oferty.

## <a name="components-of-estimates-in-a-project"></a>Składniki oszacowań w projekcie

W harmonogramie można dzielić prace na zadania, zarządzać hierarchią zadań, określać, jakie zasoby są niezbędne do wykonania danego zadania, oraz przypisywać szacowany nakład pracy wymagany do wykonania zadania.

Do definiowania oszacowań nakładu pracy i harmonogramów można używać pól na karcie **Harmonogram** na stronie **Projekt**. Ze względu na fakt, że cennik jest skojarzony z projektem, szacunki finansowe są obliczane na podstawie kosztów własnych i cen sprzedaży zdefiniowanych w cenniku.

## <a name="importing-estimates-from-a-project-into-a-quote"></a>Importowanie oszacowań z projektu do oferty

Po zdefiniowaniu szacunków dla projektu można je zaimportować do wiersza oferty. Na stronie **Szczegóły wiersza oferty** na wstążce kliknij przycisk **Importuj z oszacowań**, aby podsumować szacunki projektu według typu zadania, roli lub poziomu zadania.


[!INCLUDE[footer-include](../includes/footer-banner.md)]