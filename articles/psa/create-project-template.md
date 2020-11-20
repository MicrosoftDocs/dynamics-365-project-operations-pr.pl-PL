---
title: Tworzeniu szablonu projektu
description: Tworzenie szablonu projektu w Project Service
author: ruhercul
manager: kfend
ms.service: project-operations
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
ms.openlocfilehash: 78d25183aad8d86593d3f2582295db59eb84cf14
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/28/2020
ms.locfileid: "4133201"
---
# <a name="create-a-project-template-project-service"></a>Utwórz szablon projektu (Project Service)

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Szablony projektu pozwalają Ci zaoszczędzić czas, jeśli Twoja firma regularnie bierze udział w licytacji podobnych typów projektów. Zapewniają one standardowy zestaw ról oraz szacowane godziny dla typu projektu. Menedżerowie kont i menedżerowie projektów mogą tworzyć projekty na podstawie szablonu projektu lub mogą skopiować szablon i tworzyć własne.  
  
## <a name="components-of-project-template"></a>Składniki szablonu projektu
 Szablon projektu składa się z trzech elementów:  
  
- **Struktura podziału pracy**: Struktura podziału pracy w szablonie projektu ma ten sam zestaw elementów, co projekt. Możesz utworzyć hierarchię zadań, powiązać role z zadaniem, zdefiniować atrybuty harmonogramu, ustawić zależności i wyświetlić wszystkie dane na wykresie Gantta. Struktura podziału pracy w szablonach projektu obsługuje również tryby zadań dla każdego zadania. Podczas tworzenia harmonogramu pracy nie ma różnicy między szablonem projektu a projektem.  
  
- **Szacowania projektu**: Szacowania projektu w szablonach działają tak samo, jak w projektach, z takim wyjątkiem, że cenniki za domyślne koszty i ceny sprzedaży są zawsze domyślnym kosztem i cenami sprzedaży zdefiniowanymi w parametrach [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]. Reszta funkcji jest taka sama, jak w projekcie.  
  
- **Tworzenie zespołu projektu**: Podczas tworzenia zespołu projektu dla szablonu projektu, nie można dokonać rezerwacji nazwanego zasobu w szablonie. Można użyć **Generuj zespół projektu** w strukturze podziału pracy, aby wygenerować zestaw zasobów rodzajowych. Można również określić wymagane umiejętności i poziomy biegłości dla zasobów rodzajowych. Nie można zastąpić zasobu rodzajowego zasobem możliwym do zarezerwowania w szablonach projektu.  
  
## <a name="create-a-project-from-a-template"></a>Utwórz projekt na podstawie szablonu  
 Oto różne sposoby, w jakie można tworzyć projekt na podstawie szablonu:  
  
-   Podczas tworzenia projektu z oferty, można wybrać szablon projektu w formularzu szybkiego tworzenia.  
  
-   Podczas tworzenia projektu po kliknięciu **Nowy projekt**, formularz projektu jest wyświetlany przed zapisaniem rekordu. W tym miejscu, można kliknąć pole **Wybierz szablon**, aby wybrać z listy wstępnie zdefiniowanych szablonów projektu w organizacji.  
  
-   Kliknij **Utwórz projekt na podstawie szablonu** na stronie **Szablon projektu**, aby utworzyć projekt z szablonu.  
  
## <a name="copying-components-of-a-template-to-a-project"></a>Kopiowanie elementów szablonu do projektu  
 Podczas kopiowania elementów szablonu do projektu, istnieje kilka rzeczy, o których należy wiedzieć.  
  
 **Kopiowanie struktury podziału pracy**: Podczas kopiowania struktury podziału pracy z szablonu projektu, jeśli projekt ma inny kalendarz projektu niż szablon, godziny pracy z kalendarza projektu zostaną zastosowane dla harmonogramu zadań. Dopasowuje to harmonogram do kopii kalendarza projektu. Pierwsze zadanie na strukturze podziału pracy przyjmuje datę rozpoczęcia projektu, więc pozostała część harmonogramu hierarchii zadania jest aktualizowana na podstawie czasu trwania i zależności określone w strukturze podziału pracy szablonu.  
  
 **Kopiowanie oszacowań projektu**: Podczas kopiowania wierszy szacowania projektu, cenniki są aktualizowane na podstawie jednostki będącej właścicielem projektu dla listy koszt własny i klient dla listy cen sprzedaży. Koszt jednostkowy i ceny sprzedaży są ustalane na podstawie tych cenników dla projektów, które są skojarzone z encją sprzedaży.  
  
 **Kopiowanie członków zespołu projektu**: Podczas kopiowania członków zespołu projektu z szablonu do projektu, kopiowane są również zasoby rodzajowe, wraz z umiejętnościami i poziomami biegłości zdefiniowanymi w szablonie. Przydziały zasobów rodzajowych są także obsługiwane jak w szablonie projektu.  
  
### <a name="see-also"></a>Zobacz także  
 [Przewodnik menedżera projektu](../psa/project-manager-guide.md)
