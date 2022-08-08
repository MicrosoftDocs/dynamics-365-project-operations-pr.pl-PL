---
title: Używaj kategorii zaopatrzenia z zamówieniami zakupu projektu i oczekującymi fakturami od dostawców
description: W tym artykule opisano sposób konfigurowania kategorii zaopatrzenia, których można używać z zamówieniami zakupu projektu i oczekującymi fakturami od dostawców.
author: sigitac
ms.date: 04/07/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: f71c6bfcd183613471a4cc10e16a5a54571fac31
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 06/18/2022
ms.locfileid: "9028623"
---
# <a name="use-procurement-categories-with-project-purchase-orders-and-pending-vendor-invoices"></a>Używaj kategorii zaopatrzenia z zamówieniami zakupu projektu i oczekującymi fakturami od dostawców

_**Zastosowane do:** Project Operations dla zasobów/scenariuszy nieopartych na zaopatrzeniu_

Specjaliści ds. zakupów mogą tworzyć i obsługiwać katalogi towarów i usług, których można używać w zamówieniach zakupu projektu i oczekujących fakturach od dostawców. [Katalogi, w](/dynamics365/supply-chain/procurement/procurement-catalogs) których katalogu produktów można łatwo sklasyfikować zakup bez konieczności konfigurowania i używania dostępnego katalogu produktów. Każda kategoria kategorii kategorii można zamapować na kategorię projektu dla transakcji czasu, wydatków lub elementów. Po utworzeniu faktury dostawcy oczekującej na kategorię materiałów, która korzysta z kategorii materiałów, system utworzy wartości rzeczywiste czasu, wydatków lub materiałów, transakcji projektu i pozycji podrzędnego.

## <a name="minimum-version-requirements"></a>Minimalne wymagania dotyczące wersji

Do użycia kategorii kategorii w projektach są wymagane następujące wersje do stosowania zamówień zakupu produktów niesekwowanych/opartych na zasobach Microsoft Dynamics 365 Project Operations:

- Rozwiązanie Dataverse Project Operations w wersji 4.41.0.45 lub nowszej
- Środowisko aplikacji finansowych i operacyjnych w wersji 10.0.26 lub nowszej

## <a name="run-dual-write-maps-for-procurement-category-support"></a>Uruchamianie map dwue write dla pomocy technicznej dotyczącej kategorii

Upewnij się, że mapowanie dla encji **eksportu wiersza faktury dostawcy projektu służącej do integracji Project Operations msdyn\_projectvendorinvoicelines** w tym celu używa wersji 1.0.0.4 lub nowszej.

## <a name="enable-the-feature-key-for-procurement-categories"></a>Włącz klucz funkcji dla kategorii, które nie są dostępne w programie

Wykonaj te kroki, aby włączyć funkcję używania kategorii w zamówieniach zakupu projektu.

1. W programie Dynamics 365 Finance przejdź do obszaru roboczego **Zarządzanie funkcjami**.
1. Na liście funkcji znajdź funkcję **Użyj kategorii zaopatrzenia w Project Operations dla scenariuszy opartych na zasobach/niemagazynowanych**, a następnie wybierz **Włącz**.

> [!IMPORTANT]
> Ze wstępnie wymaganego warunku należy też **włączyć funkcję włączania oczekujących faktur od dostawcy w Project Operations dla funkcji scenariuszy opartych na zasobach/brakach** magazynowych.

## <a name="map-project-categories-in-the-procurement-category-hierarchy"></a>Mapuj kategorie projektów w hierarchii kategorii Zaopatrzenie

Wykonaj te kroki, aby zamapować kategorie projektu na kategorie kategorii temat tematu **Kategoria zaopatrzenia**:

1. Wybierz kolejno opcje **Zaopatrzenie i sourcing \> Kategorie zaopatrzenia**.
1. Wybierz **Edytuj hierarchię kategorii**.
1. Wybierz żądany węzeł hierarchii kategorii, a następnie na karcie **Przypisywanie kategorii projektu** skojarz węzeł z kategorią projektu z kategorią **Czas**, **Wydatek** lub **Projekt pozycji** (czyli kategoria **Domyślny-czas** lub **Domyślny-wydatek**).
1. Wybierz pozycję **Zapisz**.
1. Zamyknij stronę.

> [!NOTE]
> Mapowanie kategorii kategorii projektu jest opcjonalne. Jeśli kategoria zaopatrzenia nie jest zmapowana, system użyje wartości ustawionej w polu **Pozycja** w sekcji **Domyślne wartości kategorii projektu** na karcie **Project Operations na Dynamics 365 Customer Engagement** na stronie **Zarządzanie projektem i parametry księgowe**.
