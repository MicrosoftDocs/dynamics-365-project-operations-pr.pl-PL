---
title: Synchronizuj kontrakty projektowe i projekty bezpośrednio z Project Service Automation do Finance
description: W tym artykule opisano szablon i podstawowe zadania używane do synchronizacji umów projektowych i projektów bezpośrednio z Microsoft Dynamics 365 Project Service Automation do Dynamics 365 Finance.
author: Yowelle
ms.date: 12/17/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: johnmichalak
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2017-12-13
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: 62a24f3af823d474cbb4d63f8d079c708256a75e
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8933873"
---
# <a name="synchronize-project-contracts-and-projects-directly-from-project-service-automation-to-finance"></a>Synchronizuj kontrakty projektowe i projekty bezpośrednio z Project Service Automation do Finance 

[!include[banner](../includes/banner.md)]



W tym artykule opisano szablon i podstawowe zadania używane do synchronizacji umów projektowych i projektów bezpośrednio z Dynamics 365 Project Service Automation do Dynamics 365 Finance.

> [!NOTE] 
> Jeśli jest używana wersja Enterprise edition 7.3.0, należy zainstalować 4074835 KB.

## <a name="data-flow-for-project-service-automation-to-finance"></a>Przepływ danych dla Project Service Automation do Finance

> [!NOTE]
> Zanim zaczniesz używać rozwiązania integracji Project Service Automation z Finance, powinieneś zapoznać się z funkcją integracji Dynamics 365 Data.

Rozwiązanie do integracji Project Service Automation to Finance wykorzystuje funkcję integracji danych do synchronizowania danych między wystąpieniami Project Service Automation i Finance. Szablon integracji, który jest dostępny z funkcją integracji danych, umożliwia przepływ danych o umowach projektowych, projektach, wierszach umowy na projekt i punktach kontrolnych linii umowy na projekt z Project Service Automation do Finance.

Na poniższej ilustracji przedstawiono sposób synchronizowania danych między Project Service Automation a Finance.

[![Przepływ danych do integracji Project Service Automation z Finance.](./media/ProjectsAndContractsFlow_upd.JPG)](./media/ProjectsAndContractsFlow.JPG)

## <a name="templates-and-tasks"></a>Szablony i zadania

Aby uzyskać dostęp do dostępnych szablonów, w centrum administracyjnym Microsoft Power Apps wybierz pozycję **Projekty**, a następnie w prawym górnym rogu wybierz opcję **Nowy projekt**, aby wybrać szablony publiczne.

Następujące szablony i podstawowe zadania służą do synchronizowania umów dotyczących projektów i projektów z usługi Project Service Automation do Finance:

### <a name="integrating-with-dynamics-365-project-service-automation-v2x"></a>Integrowanie z Dynamics 365 Project Service Automation v2.x
- **Nazwa szablonu w integracji danych:** Projekty i kontrakty (Project Service Automation to Finance)
- **Nazwa zadań w projekcie:**

    - Umowy dotyczące projektów Project Service Automation to Finance
    - Projekty Project Service Automation to Finance
    - Wiersze umowy dotyczącej projektu Project Service Automation to Finance
    - Punkty kontrolne linii umowy na projekt Project Service Automation to Finance
  
### <a name="integrating-with-dynamics-365-project-service-automation-v3x"></a>Integrowanie z Dynamics 365 Project Service Automation v3.x
Nastąpiła zmiana schematu w Project Service Automation, która ma wpływ na szablon punktu kontrolnego wiersza umowy dotyczącej projektu i użycie wersji v2 szablonu jest wymagane do integracji Project Service Automation v3.x z Dynamics 365.

- **Nazwa szablonu w integracji danych:** Projekty i kontrakty (Project Service Automation 3.x to Finance) - v2
- **Nazwa zadań w projekcie:**

    - Umowy dotyczące projektów Project Service Automation to Finance
    - Projekty Project Service Automation to Finance
    - Wiersze umowy dotyczącej projektu Project Service Automation to Finance
    - Punkty kontrolne linii umowy na projekt Project Service Automation to Finance

Przed synchronizacją umów dotyczących projektów i projektów należy zsynchronizować konta.

## <a name="entity-set"></a>Zestaw encji

| Project Service Automation       | Finanse                                                |
|----------------------------------|--------------------------------------------------------|
| Zamówienia                           | Encja integrująca dla kontraktu projektu                |
| Projekty                         | Encja integrująca dla projektu                         |
| Wiersze zamówienia                      | Encja integrująca dla pozycji kontraktu projektu           |
| Punkty kontrolne pozycji kontraktu projektu | Encja integrująca dla punktu kontrolnego pozycji kontraktu projektu |

## <a name="entity-flow"></a>Przepływ encji

Kontraktami projektu zarządza się w Project Service Automation i są one synchronizowane z Finance jako kontrakty projektów. W ramach szablonu integracji można ustawić źródło integracji w programie Finance dla umowy dotyczącej projektu.

Projekty czasowe i materiałowe oraz projekty o stałej cenie są zarządzane w programie Project Service Automation i synchronizowane z programem Finance jako projekty. W ramach integracji szablonu możesz ustawić źródło integracji dla projektu w Finance. Obecnie obsługiwane są tylko projekty czasowe i materiałowe oraz projekty o stałej cenie.


Pozycjami kontraktu projektu zarządza się w Project Service Automation i są one synchronizowane z Finance jako reguły rozliczeniowe kontraktu dotyczącego projektu. Jeśli metoda rozliczenia różni się od domyślnego typu projektu, synchronizacja aktualizuje typ projektu dla projektu w wierszu umowy i grupy projektów.

Punktami kontrolnymi pozycji kontraktu projektu zarządza się w Project Service Automation i są one synchronizowane z Finance jako reguły rozliczeniowe punktów kontrolnych kontraktu dotyczącego projektu.

## <a name="project-service-automation-to-finance-integration-solution"></a>Rozwiązanie integracji Project Service Automation z Finance

Pole **identyfikator kontraktu projektu** jest dostępne na stronie **kontrakty projektów**. To pole zostało wykonane jako klucz fizyczny i unikatowy do obsługi integracji.

Po utworzeniu nowego kontraktu projektu, jeśli wartość **identyfikatora kontraktu projektu** już nie istnieje, jest generowana automatycznie za pomocą sekwencji numerów. Wartość składa się z **ORD**, po którym następuje rosnąca sekwencja liczb, a następnie sufiks składający się z sześciu znaków. Oto przykład: **ORD-01022-Z4M9Q0**.

Pole **Numer projektu** jest dostępne na stronie **Projekty**. To pole zostało wykonane jako klucz fizyczny i unikatowy do obsługi integracji.

Po utworzeniu nowego projektu, jeśli wartość **Numer projektu** już nie istnieje, jest generowana automatycznie za pomocą sekwencji numerów. Wartość składa się z **PRJ**, po którym następuje rosnąca sekwencja liczb, a następnie sufiks składający się z sześciu znaków. Oto przykład: **PRJ-01049-CCNID0**.

Po zastosowaniu rozwiązania integracji Project Service Automation z Finance skrypt uaktualnienia ustawia pole **Identyfikator kontraktu** projektu dla istniejących umów dotyczących projektu oraz pole **Numer projektu** dla istniejących projektów w programie Project Service Automation.

## <a name="prerequisites-and-mapping-setup"></a>Wymagania wstępne i ustawienia mapowania

- Przed synchronizacją umów dotyczących projektów i projektów należy zsynchronizować konta.
- W zestawie połączeń Dodaj mapowanie pola klucza integracji dla **msdyn\_organizationalunits** do **msdyn\_name \[Name\]**. Konieczne może być dodanie projektu do zestawu połączeń. Aby uzyskać więcej informacji, zobacz [Integrowanie danych z Common Data Service dla aplikacji](/powerapps/administrator/data-integrator).
- W zestawie połączeń Dodaj mapowanie pola klucza integracji dla **msdyn\_projects** do **msdynce\_projectnumber \[Project Number\]**. Konieczne może być dodanie projektu do zestawu połączeń. Aby uzyskać więcej informacji, zobacz [Integrowanie danych z Common Data Service dla aplikacji](/powerapps/administrator/data-integrator).
- **SourceDataID** w przypadku umów dotyczących projektów i projektów można zaktualizować do innej wartości lub usunąć z mapowania. Domyślna wartość szablonu to **Project Service Automation**.
- Mapowanie **PaymentTerms** musi być aktualizowane, aby odzwierciedlać prawidłowe warunki płatności w Finance. Użytkownik może również usunąć mapowanie z zadania projektu. Domyślna mapa wartości zawiera wartości domyślne dla danych demonstracyjnych. W poniższej tabeli przedstawiono wartości w Project Service Automation.

    | Wartość | Description   |
    |-------|---------------|
    | 1     | 30-dniowy termin płatności        |
    | 2     | 2% 10, 30 dni |
    | 3     | 45-dniowy termin płatności        |
    | 100     | 60-dniowy termin płatności        |

## <a name="power-query"></a>Power Query

Użyj narzędzia Microsoft Power Query dla programu Excel, aby filtrować dane, jeśli spełnione są następujące warunki:

- W Dynamics 365 Sales jest zamówienie sprzedaży.
- Masz wiele jednostek organizacyjnych w Project Service Automation, a te jednostki organizacyjne zostaną zamapowane na wiele firm w Finance.

Jeśli musisz używać narzędzia Power Query, przestrzegaj następujące wytyczne:

- Szablon projektów i kontraktów (PSA to fin i Ops) zawiera filtr domyślny zawierający tylko zamówienia sprzedaży z typem **Work item (msdyn\_ordertype = 192350001)**. Ten filtr ułatwia zagwarantowanie, że kontrakty projektów nie są tworzone dla zamówień sprzedaży w Finance. W przypadku utworzenia własnego szablonu należy dodać ten filtr.
- Należy utworzyć filtr do narzędzia Power Query uwzględniający tylko organizacje umowy, które mają być synchronizowane z firmą integrującą zestaw połączenia. Na przykład umowy dotyczące projektów, które masz z jednostką organizacyjną kontraktu firmy Contoso US, powinny być synchronizowane z firmą USSI, ale umowy dotyczące projektów, które masz z jednostką organizacyjną kontraktu firmy Contoso Global, powinny być synchronizowane z firmą USMF. Jeśli nie dodasz tego filtru do mapowania zadań, wszystkie umowy dotyczące projektu zostaną zsynchronizowane z firmą zdefiniowaną dla zestawu połączeń, niezależnie od jednostki organizacyjnej kontraktu.

## <a name="template-mapping-in-data-integration"></a>Mapowanie szablonów w integracji danych

> [!NOTE] 
> Pola **CustomerReference**, **AddressCity**, **AddressCountryRegionID**, **AddressDescription**, **AddressLine1**, **AddressLine2**, **AddressState** i **AddressZipCode** nie są zawarte w domyślnym mapowaniu kontraktów dotyczących projektów. Można dodać mapowania, jeśli jest wymagane, aby te dane były synchronizowane z kontraktami dotyczącymi projektów.
>
> Pola **Description**, **ParentID**, **ProjectGroup**, **ProjectManagerPersonnelNumber** i **ProjectType** nie są uwzględnione w domyślnym mapowaniu projektów. Można dodać mapowania, jeśli jest wymagane, aby te dane były synchronizowane z projektami.

Poniższe ilustracje przedstawiają przykłady odwzorowań zadań szablonu w integracji danych. Mapowanie przedstawia informacje o polach, które zostaną zsynchronizowane z Project Service Automation do Finance.

[![Mapowanie szablonu kontraktu projektu.](./media/ProjectContractTemplateMapping.JPG)](./media/ProjectContractTemplateMapping.JPG)

[![Mapowanie szablonu projektu.](./media/ProjectTemplateMapping.JPG)](./media/ProjectTemplateMapping.JPG)

[![Mapowanie szablonu pozycji kontraktu.](./media/ProjectContractLinesMapping.JPG)](./media/ProjectContractLinesMapping.JPG)

[![Mapowanie szablonu pozycji kontraktu punktu kontrolnego.](./media/ProjectContractLineMilestonesMapping.JPG)](./media/ProjectContractLineMilestonesMapping.JPG)

#### <a name="project-contract-line-milestone-mapping-in-the-projects-and-contracts-psa-3x-to-dynamics---v2-template"></a>Mapowanie punktów kontrolnych pozycja kontraktu projektu w szablonie projekty i kontrakty (PSA 3.x do Dynamics) - v2:

[![Mapowanie pozycji kontraktu punktu kontrolnego za pomocą szablonu wersji 2.](./media/ProjectContractLineMilestoneMapping_v2.jpg)](./media/ProjectContractLineMilestoneMapping_v2.jpg)


[!INCLUDE[footer-include](../includes/footer-banner.md)]