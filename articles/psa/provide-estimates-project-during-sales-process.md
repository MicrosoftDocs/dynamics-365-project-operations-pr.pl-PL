---
title: Podaj szacowaną ilość pracy dla projektu w czasie procesu sprzedaży
description: Podawanie szacowanej ilość pracy dla projektu w czasie procesu sprzedaży w Project Service
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
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
ms.openlocfilehash: ddb7f8c0ff8c7fd7e51edb42f9d227f2b91a811b
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082062"
---
# <a name="provide-work-estimates-for-a-project-during-the-sales-process-project-service"></a>Podaj szacowaną ilość pracy dla projektu w czasie procesu sprzedaży (Project Service)

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Podczas procesu sprzedaży możesz od podstaw opracowywać szacunki sprzedaży korzystając z wierszy oferty. Możliwości [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] w [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] zapewniają bardziej naukowy i deterministyczny sposób przygotowywania szacunków sprzedaży polegający na rozbijaniu pozycji roboczych i kojarzeniu odpowiednich atrybutów, które przyczyniają się do szacunków dla projektu, ze strukturą podziału pracy.  
  
 Gdy już wygrasz sprzedaż, możesz użyć skojarzonej struktury podziału pracy w planie projektu, dopracowując ją, jeśli jest to niezbędne dla pomyślnego zakończenia projektu.  
  
## <a name="link-a-project-to-a-quote-line"></a>Połącz projekt z wierszem oferty  
 Podczas tworzenia wiersza oferty związanego z projektem możesz tworzyć nowy projekt z wiersza oferty. Następnie możesz użyć szablonów projektu, które są wstępnie skonfigurowanymi standardowymi planami projektu i prognoz finansowych wspólnych dla organizacji lub kopii planu projektu i oszacowań z ostatniego projektu. Podczas tworzenia projektu, wybór szablonu projektu stanowi podstawę do dopracowania projektu planu, szacunków i wymagań roli. W przypadku tworzenia projektu z oferty, projekt jest automatycznie kojarzony z wierszem oferty.  
  
## <a name="project-estimate-components"></a>Składniki szacowania projektu  
 Struktura podziału pracy dla projektu zapewnia sposób podziału prac na zadania, utrzymania hierarchii zadań i przypisywania oszacowania nakładu prac wymaganych do wykonania każdego zadania. Możesz także powiązać role z zadaniem, aby wskazać oszacowanie typu zasobu wymaganego do ukończenia zadania oraz harmonogram.  
  
 Struktura podziału pracy pomaga określić nakład pracy i zaplanować oszacowania. Domyślnie projekt używa cenników domyślnych, które zostały przez Ciebie zdefiniowane wcześniej. Koszt i ceny sprzedaży określone w cennikach pomagają określać szacunki finansowe dla podziału pracy projektu.  
  
 Jeśli projekt jest skojarzony z ofertą, a oferta ma inny cennik niż cennik domyślny, cennik oferty jest używany do sporządzania szacunków finansowych.  
  
## <a name="import-estimates-from-a-project-into-a-quote"></a>Importuj oszacowania z projektu do oferty  
 Po przygotowaniu oszacowań projektu w projekcie, możesz zaimportować te oszacowania do wiersza oferty:  
  
-   W **Szczegóły wiersza oferty** , kliknij **Importuj z oszacowań**. 

-   Określ, czy chcesz importować oszacowania projektu podsumowane według typu transakcji, roli czy poziomu węzła struktury podziału pracy.  
  
### <a name="see-also"></a>Zobacz także  
 [Przewodnik menedżera projektu](../psa/project-manager-guide.md)
