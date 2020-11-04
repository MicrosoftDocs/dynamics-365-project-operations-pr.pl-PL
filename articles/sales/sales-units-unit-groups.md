---
title: Jednostki i grupy jednostek
description: W tym temat zamieszczono informacje dotyczące sposobu tworzenia jednostek i grup jednostek w Dynamics 365 Project Operations.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
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
ms.openlocfilehash: 345a4f38ad0bc5acddb90cfd8cb3e92154e46513
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082135"
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
5. Wybierz pozycję **Zapisz** :
