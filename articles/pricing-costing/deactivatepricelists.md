---
title: Dezaktywowanie cenników
description: W temat wyjaśniono sposób dezaktywowania lub usuwania niewykorzystanych lub starych cenników.
author: rumant
manager: AnnBe
ms.date: 03/19/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Professional Service industries
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 3fa902e93815002be7d6915880cd7759dbbde5ef
ms.sourcegitcommit: 386921f44f1e9a8a828b140206d52945de07aee7
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/22/2021
ms.locfileid: "5701960"
---
# <a name="deactivate-price-lists"></a>Dezaktywowanie cenników 

_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_

Aby usunąć stare lub nieużywane cenniki z Dynamics 365 Project Operations, należy wykonać dwa kroki. 

1. Usuń lub usuń cennik z określonych stron.
2. Zdezaktywowanie lub usunięcie cennika z listy Aktywne cenniki na stronie **Cenniki**.

>[!IMPORTANT]
> Aby całkowicie usunąć cennik, należy wykonać oba kroki. Samo wykonanie kroku 2, czyli bezpośredniego usunięcia lub dezaktywacji cennika z widoku Aktywne cenniki, nie jest wystarczające. Musisz również usunąć powiązanie tego cennika ze wszystkich miejsc wymienionych w kroku 1.

## <a name="delete-the-price-list-from-specific-pages"></a>Usuń cennik z określonych stron
1. Aby usunąć cennik z programu Project Operations, przejdź do następujących stron:  

      - Strona **Parametry projektu** > karta **Cenniki**
      - Strona **Jednostka organizacyjna** > Siatka **Cenniki**
      - Strona **Konto** > Siatka **Cenniki projektu**
      - Strona **Oferty projektu** > Siatka **Cenniki projektu**: Dotyczy to wszystkich aktywnych ofert projektu.
      - Strona **Kontrakty projektów** > Siatka **Cenniki projektu**: Dotyczy to wszystkich aktywnych kontraktów projektu.

 2. Dla każdej strony należy wybrać cennik do usunięcia, a następnie wybrać opcję **Usuń**. 
 
## <a name="delete-or-deactivate-the-price-list-from-the-price-lists-page"></a>Usuń lub dezaktywuj cennik na stronie Cenniki
 
1. Aby usunąć cennik z aktywnych cenników, wybierz **Sprzedaż** > **Klienci** > **Cenniki**. 
2. Wybierz cenniki, które chcesz usunąć, i naciśnij **Usuń**. Jeśli do cennika przywołano jakiekolwiek istniejące transakcje, nie będzie można go usunąć. W takim przypadku możesz dezaktywować cennik, aby nie pojawiał się w żadnych widokach. 
3. Aby dezaktywować cennik, ponownie go zaznacz, a następnie wybierz opcję **Dezaktywuj**.   
