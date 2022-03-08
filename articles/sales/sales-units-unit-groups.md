---
title: Jednostki i grupy jednostek
description: W tym temacie przedstawiono informacje dotyczące sposobu tworzenia jednostek i grup jednostek w rozwiązaniu Dynamics 365 Project Operations.
author: rumant
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 6a0aec1cc32ebdea9d2dbc7cc891f82da07e044f5c5655e008068f72dd198587
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/06/2021
ms.locfileid: "6999554"
---
# <a name="units-and-unit-groups"></a>Jednostki i grupy jednostek

_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_

Jednostki to ilości lub wielkości, w jakich sprzedajesz swoje produkty lub usługi. Na przykład jeśli sprzedajesz zaopatrzenie ogrodnicze, możesz sprzedawać nasiona w paczkach, pudełkach oraz na paletach. Grupa jednostek jest zbiorem tych różnych jednostek.

Aby wykonać czynności opisane w tym temacie należy się upewnić, że użytkownik został przypisany do roli administratora systemu lub menedżer ds. sprzedaży, lub że posiada równoważne uprawnienia.

## <a name="create-a-unit-group"></a>Tworzenie grupy jednostek

1. Na mapie witryny, wybierz **Jednostki**.
2. Wybierz **Nowa** w oknie dialogowym **Utwórz grupę jednostek** i wprowadź nazwę jednostki.
3. W polu **Jednostka podstawowa** wpisz najmniejszą wspólną jednostkę miary, w której produkt będzie sprzedawany. Można na przykład wprowadzić „sztukę” lub „uncję”.
4. Wybierz pozycję **OK**.

## <a name="add-units-to-a-unit-group"></a>Grupy jednostek i dodawanie do nich jednostek

1. Otwórz grupę jednostek, a następnie na karcie **Powiązane** wybierz pozycję **Jednostki**. Zobaczysz, że jednostka podstawowa została już dodana.
2. Wybierz opcję **Dodaj nową jednostkę** i na stronie **Szybkie tworzenie: jednostka** w polu **Nazwa** wprowadź nazwę jednostki.
3. W polu **Ilość** wprowadź ilość, jaką będzie zawierać dana jednostka. Na przykład jeśli pudełko zawiera dwie sztuki, należy wpisać „2”. 
4. W polu **Jednostka podstawowa** wybierz jednostkę podstawową, aby ustanowić najmniejszą jednostkę miary w jednostce. Można na przykład wybrać pozycję „sztuka”.
5. Wybierz pozycję **Zapisz**:


[!INCLUDE[footer-include](../includes/footer-banner.md)]