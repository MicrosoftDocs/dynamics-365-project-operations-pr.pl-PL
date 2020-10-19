---
title: Szacowanie wydatków
description: W tym temacie zamieszczono informacje dotyczące definiowania lub szacowania kosztów opartych na projektach.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 2afe4ff2f84fc5426c409e6314da73b11a4de281
ms.sourcegitcommit: 56c42d7f5995a674426a1c2a81bae897dceb391c
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/01/2020
ms.locfileid: "3908450"
---
# <a name="expense-estimates"></a>Szacowanie wydatków
_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_

Oprócz definiowania oszacowań opartych na zasobach Dynamics 365 Project Operations umożliwia menedżerom projektów definiowanie kosztów opartych na projekcie dla każdego projektu. Każdy element wydatków może być skojarzony z określoną kategorią zadania lub wydatku projektu. Kategorie wydatków są zwykle definiowane na poziomie organizacji. Kalkulacja cen dla każdej kategorii wydatków jest zwykle definiowane w poniższej hierarchii:

- Organizacja
- Klient
- Oferta / kontrakt

Wykonaj poniższe kroki, aby wyświetlić, dodać lub usunąć koszty projektu.

1. Przejdź do obszaru **Projekty** i wybierz projekt, który chcesz edytować.
2. Wybierz **Oszacowania projektów** i wyświetl listę wydatków projektowych.
3. Wybierz opcję **Nowe koszty**, aby dodać wydatek. Możesz też wybrać wydatek, który ma zostać usunięty, a następnie wybrać pozycję **Usuń wydatek**.

Dla każdego elementu wiersza wydatków są definiowane następujące atrybuty:

- **Kategoria**: wspólne zgrupowania używane do opisywania wszystkich kosztów poniesionych w związku z projektem.
- **Data rozpoczęcia**: data, kiedy zakłada się, że wydatek zostanie poniesiony.
- **Ilość**: szacowana liczba pozycji wydatku dla określonej kategorii.
- **Jednostkowy koszt własny**: cena jednostkowa użyta do obliczenia kosztu wydatku.
- **Jednostkowa cena sprzedaży**: cena jednostkowa użyta do obliczenia ceny sprzedaży danego wydatku.

