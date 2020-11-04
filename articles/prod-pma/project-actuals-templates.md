---
title: Synchronizuj dane rzeczywiste projektu bezpośrednio z programu Project Service Automation do dziennika integracji projektu w celu księgowania w Finance and Operations
description: Ta temat opisuje szablony i podstawowe zadania używane do synchronizowania wartości rzeczywiste projektu bezpośrednio z Microsoft Dynamics 365 Project Service Automation do Finance and Operations.
author: Yowelle
manager: AnnBe
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: cff62e739e88dc45e7c3d1ea044875f0600f2bc1
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082144"
---
# <a name="synchronize-project-actuals-directly-from-project-service-automation-to-the-project-integration-journal-for-posting-in-finance-and-operations"></a>Synchronizuj dane rzeczywiste projektu bezpośrednio z programu Project Service Automation do dziennika integracji projektu w celu księgowania w Finance and Operations

[!include[banner](../includes/banner.md)]

W tym temacie opisano szablony i podstawowe zadania, które są używane do synchronizowania danych rzeczywistych projektu bezpośrednio z Microsoft Dynamics 365 Project Service Automation do Dynamics 365 Finance.

Szablon synchronizuje transakcje z rozwiązania Project Service Automation w tabeli tymczasowych w Finance. Po zakończeniu synchronizacji dane z tabeli tymczasowej **muszą** zostać zaimportowane do arkusza integracji.

> [!NOTE]
> - Rzeczywista integracja projektów jest dostępna począwszy od wersji 8.0.1.
> - Jeśli używasz wersji Enterprise edition 7.3.0, po zainstalowaniu KB 4132657 i KB 4132660 będziesz mógł używać szablonów do integracji zadań projektowych, kategorii transakcji wydatków, szacunków godzinowych, szacunków wydatków i danych rzeczywistych oraz do konfigurowania funkcji zamykający. Jeśli musisz zresetować dystrybucje rozliczeń, zalecamy również zainstalowanie KB 4131710.
> - Jeśli używasz wersji 7.3.0 i przenosisz transakcje opłat z Project Service Automation, musisz zainstalować KB 4345320, aby uwzględnić te opłaty na fakturze za projekt.
> - Jeśli wprowadzasz kwoty podatku od sprzedaży na czas lub transakcje wydatków w Project Service Automation, musisz zainstalować Project Service Automation Update 7. W przeciwnym razie wartości rzeczywiste podatku nie będą powiązane z powiązanymi danymi rzeczywistymi dotyczącymi czasu lub wydatków i nie zostaną zsynchronizowane z Finance. Aby uzyskać więcej informacji, skontaktuj się z pomocą techniczną.

## <a name="data-flow-for-project-service-automation-to-finance"></a>Przepływ danych dla Project Service Automation do Finance

Rozwiązanie do integracji Project Service Automation to Finance wykorzystuje funkcję integracji danych do synchronizowania danych między wystąpieniami Project Service Automation i Finance. Szablony integracji, które są dostępne z funkcją integracji danych, umożliwiają przepływ danych o rzeczywistych danych projektowych z Project Service Automation do Finance.

Na poniższej ilustracji przedstawiono sposób synchronizowania danych między Project Service Automation a Finance.

[![Przepływ danych do integracji Project Service Automation z Finance and Operations](./media/ProjectActualsFlow.jpg)](./media/ProjectActualsFlow.jpg)

## <a name="project-actuals-from-project-service-automation"></a>Aktualne dane projektowe z Project Service Automation

### <a name="template-and-tasks"></a>Szablon i zadania

Aby uzyskać dostęp do dostępnych szablonów, w centrum administracyjnym Microsoft Power Apps wybierz pozycję **Projekty** , a następnie w prawym górnym rogu wybierz opcję **Nowy projekt** , aby wybrać szablony publiczne.

Następujący szablon i podstawowe zadania są używane do synchronizowania danych rzeczywistych projektu z Project Service Automation do Finance:

- **Nazwa szablonu podczas integracji danych:** wartości rzeczywiste projektu (PSA do Fin i Ops)
- **Nazwa zadań w projekcie:**

    - Wartości rzeczywiste
    - TransactionConnections

### <a name="entity-set"></a>Zestaw encji

| Project Service Automation | Finanse                                   |
|----------------------------|----------------------------------------------------------|
| Wartości rzeczywiste                    | Encja integracyjna dla wartości rzeczywistych projektów                   |
| Połączenia transakcji    | Encja integrująca dla transakcji projektu relacje |

### <a name="entity-flow"></a>Przepływ encji

Dane rzeczywiste projektu są zarządzane w Project Service Automation i synchronizowane z dziennikiem integracji projektu w Finance. Księgowanie zostanie zastosowane na podstawie domyślnych wymiarów finansowych i konfiguracji księgowania.

### <a name="prerequisites"></a>Wymagania wstępne

Przed synchronizacją danych rzeczywistych należy skonfigurować parametry integracji usługi Project Service Automation oraz zsynchronizować projekty, zadania projektu i kategorie transakcji wydatków w projekcie.

### <a name="power-query"></a>Power Query

Aby wykonać te zadania, należy użyć Microsoft Power Query dla Excel w szablonie wartości rzeczywiste:

- Przekształć typ transakcji w Project Service Automation na prawidłowy typ transakcji w Finance. Ta transformacja jest już zdefiniowana w szablonie wartości rzeczywiste projektu (PSA do Fin and Ops).
- Przekształć typ rozliczenia w Project Service Automation na właściwy typ rozliczenia w Finance. Ta transformacja jest już zdefiniowana w szablonie wartości rzeczywiste projektu (PSA do Fin and Ops). Typ fakturowania jest mapowany na właściwość wiersza w zależności od konfiguracji na stronie **parametrów integracji rozwiązania Project Service Automation**.
- Należy filtrować do określonych jednostek organizacyjnych zasobu, które muszą zostać zsynchronizowane z tym szablonem.
- Jeśli międzyfirmowe dane rzeczywiste dotyczące czasu lub międzyfirmowe wartości rzeczywiste wydatków zostaną zsynchronizowane z Finance, należy przekształcić jednostkę organizacyjną kontraktu w odpowiednią firmę w Finance. W szablonie wartości rzeczywistych (PSA do Fin i Ops) kolumna warunkowa jest definiowana na podstawie danych demonstracyjnych. Ostatnią wstawioną kolumnę warunkową należy zaktualizować do odpowiednich firm. W przeciwnym razie może wystąpić błąd integracji lub nieprawidłowe rzeczywiste transakcje mogą zostać zaimportowane do Finance.
- Jeśli międzyfirmowe lub międzyfirmowe wartości rzeczywiste wydatków nie zostaną zsynchronizowane z programem Finance, należy usunąć z szablonu ostatnią wstawioną kolumnę warunkową. W przeciwnym razie może wystąpić błąd integracji lub nieprawidłowe rzeczywiste transakcje mogą zostać zaimportowane do Finance.

#### <a name="contract-organizational-unit"></a>Jednostka organizacyjna kontraktowa
Aby zaktualizować wstawioną kolumnę warunkową w szablonie, kliknij strzałkę na **mapie** , aby otworzyć mapowanie. Zaznacz łącze **Zaawansowane zapytania i filtrowania** , aby otworzyć Power Query.

- Jeśli są używane szablony domyślne projektów rzeczywistych (PSA do Fin lub Ops), w Power Query wybierz ostatnio **Wstawiony warunek** z sekcji **Zastosowane kroki**. We wpisie **Funkcja** zamień **USSI** na nazwę firmy, która ma być używana podczas integracji. Dodaj dodatkowe warunki do wpisu **Funkcji** , gdy jest to wymagane, i zaktualizuj warunek **else** z **USMF** do właściwej firmy.
- Jeśli tworzysz nowy szablon, musisz dodać kolumnę, aby wspierać czas i koszty międzyfirmowe. Wybierz opcję **Dodaj kolumnę warunkową** i wprowadź nazwę kolumny, na przykład **LegalEntity**. Wprowadź warunek dla kolumny, gdzie, jeśli **msdyn\_contractorganizationalunitid.msdyn\_name** to \<organizational unit\>, wtedy \<enter the legal entity\>. W przeciwnym razie ma wartość null.

### <a name="template-mapping-in-data-integration"></a>Mapowanie szablonów w integracji danych

Poniższe ilustracje przedstawiają przykład odwzorowania zadań szablonu w integracji danych. Mapowanie przedstawia informacje o polach, które zostaną zsynchronizowane z Project Service Automation do Finance.

[![Mapowanie szablonu — wartości rzeczywiste](./media/ActualsMapping.jpg)](./media/ActualsMapping.jpg)

[![Mapowanie szablonu — połączenia transakcji](./media/TransactionConnections.jpg)](./media/TransactionConnections.jpg)

## <a name="import-from-staging-table-after-integration-from-project-service-automation"></a>Importuj z tabeli przemieszczania po integracji z Project Service Automation

Okresowy proces importu z tabeli pomostowej należy uruchomić po zsynchronizowaniu danych rzeczywistych z Project Service Automation do Finance. Ten proces spowoduje zaimportowanie transakcji projektu z tabeli pomostowej do arkusza integracji Project Service Automation, w którym stosowane jest rozliczanie i można zaksięgować zaimportowane transakcje. Zalecamy uruchomienie tego procesu w trybie wsadowym; opcjonalnie można go skonfigurować tak, aby działał jako cykliczna partia.

## <a name="update-actuals-from-finance"></a>Aktualizowanie wartości rzeczywistych z poziomu Finance

### <a name="template-and-tasks"></a>Szablon i zadania

Poniższe szablony i podstawowe zadania służą do synchronizowania numeru załącznika i podatków z zaksięgowanych transakcji projektów z finansów do rozwiązania Project Service Automation:

- **Nazwa szablonu podczas integracji danych:** Aktualizacja danych rzeczywistych projektu (od Fin Ops do PSA)
- **Nazwa zadań w projekcie:**

    - Wartości rzeczywiste 
    - TransactionConnections

### <a name="entity-set"></a>Zestaw encji

| Finanse                                                  | Project Service Automation |
|----------------------------------------------------------|----------------------------|
| Encja integracyjna dla wartości rzeczywistych projektów                   | Wartości rzeczywiste                    |
| Encja integrująca dla transakcji projektu relacje | Połączenia transakcji    |

### <a name="entity-flow"></a>Przepływ encji

Dane rzeczywiste projektu są zarządzane w Project Service Automation i synchronizowane z dziennikiem integracji projektu w Finance. Po zaksięgowaniu danych rzeczywistych w Finance, są one aktualizowane w Project Service Automation przy użyciu numeru załącznika z Finance. Jeśli w Finance dodano podatki od sprzedaży, nowe wartości rzeczywiste podatku są tworzone w Project Service Automation.

### <a name="power-query"></a>Power Query

W szablonie aktualizacji danych rzeczywistych projektu należy użyć dodatku Power Query, aby wykonać następujące zadania:

- Przekształć typ transakcji w Finance na prawidłowy typ transakcji w Project Service Automation. Ta transformacja jest już zdefiniowana w szablonie Aktualizacja danych rzeczywistych projektu (Fin Ops to PSA).
- Przekształć typ rozliczenia w Finance na właściwy typ rozliczenia w Project Service Automation. Ta transformacja jest już zdefiniowana w szablonie Aktualizacja danych rzeczywistych projektu (Fin Ops to PSA).

### <a name="template-mapping-in-data-integration"></a>Mapowanie szablonów w integracji danych

Poniższe ilustracje przedstawiają przykłady odwzorowań zadań szablonu w integracji danych. Mapowanie przedstawia informacje o polach, które zostaną zsynchronizowane z rozwiązania Finance do Project Service Automation.

[![Mapowanie szablonu — aktualizacja wartości rzeczywistych](./media/ActualsUpdateMapping.jpg)](./media/ActualsUpdateMapping.jpg)

[![Mapowanie szablonu — aktualizacja transakcji](./media/TransactionConnectionsUpdate.jpg)](./media/TransactionConnectionsUpdate.jpg)
