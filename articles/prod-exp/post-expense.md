---
title: Księgowanie raportu wydatków
description: W tym temacie przedstawiono sposób księgowania raportu z wydatków w księdze głównej.
author: saraschi2
manager: AnnBe
ms.date: 02/26/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvPerDiems
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2d008ef8dd55550431fbb9e329cd7d9428a08831
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082158"
---
# <a name="post-an-expense-report"></a>Księgowanie raportu wydatków

[!include [banner](../includes/banner.md)]

Po zatwierdzeniu i przeniesieniu raportu wydatków do dziennika głównego można go opublikować w księdze głównej. Podczas księgowania raportu wydatków są identyfikowane wydatki kwalifikujące się do zwrotu podatku VAT. Zadanie sprawdzania i odzyskiwania płatności VAT jest przypisywane do pracownika, który jest odpowiedzialny za sprawdzanie raportu z wydatków.

Jeśli wydatki w raporcie obciążają inną firmę niż ta, zatrudniająca pracownika, należy sprawdzić zarówno firmę obciążającą, jak i firmę obciążaną wydatkami. Na przykład pracownik, który przedstawił raport z wydatków, pracuje dla firmy DAT, ale ponosił koszty względem firmy DIR. W tym przypadku DAT to firma obciążająca a DIR to firma obciążana. Po sprawdzeniu wierszy dziennika można je zaksięgować w księdze głównej.

W celu zaksięgowania raportu z wydatków na stronie **Zatwierdzone raporty o wydatkach** wybierz raport o wydatkach, a następnie w okienku akcji wybierz pozycję **Księguj**.

Można również zaksięgować wszystkie raporty o wydatkach na liście w tym samym czasie. Zaznacz wszystkie raporty o wydatkach, a następnie wybierz pozycję **Księguj**.
