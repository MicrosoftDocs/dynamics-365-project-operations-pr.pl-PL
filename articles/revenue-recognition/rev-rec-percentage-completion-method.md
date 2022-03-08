---
title: Projekty szacowanych przychodów o stałej cenie
description: Ten temat zawiera informacje o przychodach o stałej cenie w projektach.
author: sigitac
ms.date: 11/16/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 451f0403f0111b5ea4de6c91b54eae157830e413d3a21f23bd841a66905e147b
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/06/2021
ms.locfileid: "7006439"
---
# <a name="fixed-price-revenue-estimate-projects"></a>Projekty szacowanych przychodów o stałej cenie 

_**Zastosowane do:** Project Operations dla zasobów/scenariuszy nieopartych na zaopatrzeniu_

Podczas tworzenia pozycji kontraktu projektu z następującymi atrybutami w aplikacji Dynamics 365 Project Operations w usłudze Microsoft Dataverse system automatycznie tworzy projekt szacowanych przychodów o stałej cenie. Informacje zawarte w tym projekcie są oparte na następujących elementach:

  - Metoda rozliczania stałych cen.
  - Skojarzony projekt.
  - Co najmniej jeden punkt kontrolny zdefiniowany na karcie **Harmonogram faktur** na stronie **Pozycja kontraktu projektu**.

## <a name="review-fixed-price-revenue-estimates-projects"></a>Przeglądanie projektów szacowanych przychodów o stałej cenie
Aby przejrzeć projekty szacowanych przychodów o stałej cenie, wykonaj następujące czynności:

1. W środowisku aplikacji Dynamics 365 Finance przejdź do pozycji **Zarządzanie projektami i księgowanie** > **Projekty** > **Projekty szacowanych przychodów o stałej cenie**.
2. Wybierz projekt, który chcesz wyświetlić, i kliknij dwukrotnie **identyfikator projektu szacowania**, aby otworzyć rekord i przejrzeć szczegóły projektu.
3. Rozwiń kartę **Projekt**. Jeden projekt zostanie wyświetlony w siatce **Wybrane projekty**. System używa tego jako projektu domyślnego, ponieważ jest to projekt skojarzony z pozycją kontraktu projektu. 
4. Aby zmienić skojarzenie, wybierz dodatkowe projekty i dodaj je do siatki **Wybrane projekty**. Jeśli w tej siatce wybrano wiele projektów, procent wykonania projektu i szacowane przychody są obliczane razem dla wszystkich wybranych projektów.

  Koszt projektu, profil przychodów, szablon kosztów i kod okresu można ustawić ręcznie. Jeśli nie są one ustawione ręcznie, wartości domyślne zostaną ustawione podczas pierwszego obliczenia szacowania dla projektu przy użyciu reguł skonfigurowanych dla profilów przychodów i kosztów projektu.



[!INCLUDE[footer-include](../includes/footer-banner.md)]