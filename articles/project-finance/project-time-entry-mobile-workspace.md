---
title: Mobilny obszar roboczy wprowadzania czasu projektu
description: Ten temat zawiera informacje o mobilnym obszarze roboczym Wpis czasu projektu. Ten obszar roboczy umożliwia użytkownikom wejście do projektu i zaoszczędzenie czasu przy użyciu urządzenia mobilnego.
author: KimANelson
manager: AnnBe
ms.date: 12/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 272101
ms.assetid: 4505f021-b9bb-4b87-be24-6bf0bd88ee60
ms.search.region: Global
ms.search.industry: Service industries
ms.author: knelson
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: ee11f7f392676adb59bd25f6549737482faf5fdb
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/24/2020
ms.locfileid: "3754338"
---
# <a name="project-time-entry-mobile-workspace"></a>Mobilny obszar roboczy wprowadzania czasu projektu

[!include [banner](../includes/banner.md)]

Ten temat zawiera informacje o mobilnym obszarze roboczym **Wpis czasu projektu**. Ten obszar roboczy umożliwia użytkownikom wejście do projektu i zaoszczędzenie czasu przy użyciu urządzenia mobilnego.

Ten mobilny obszar roboczy jest przeznaczony do użytku z aplikacją mobilną Dynamics 365 Unified Ops. 

## <a name="overview"></a>Omówienie
W ramach codziennej pracy zasoby projektów zwykle są na terenie lub podróżują. Mobilny obszar roboczy **Wpis czasu projektu** umożliwia użytkownikom wprowadzanie czasu do rozliczenia lub nierozliczenia w stosunku do projektu na wybranym urządzeniu mobilnym. Zasoby projektu mogą więc rejestrować wpisy czasu w dowolnym czasie i z dowolnego miejsca. Mogą również wyświetlać wpisy godzin, które już zostały zarejestrowane. 

W szczególności w obszarze roboczym **Wpis czasu projektu** użytkownicy mogą wykonywać następujące zadania:

-   W przypadku każdej wybranej daty wprowadź liczbę godzin poświęconego na wykonanie określonego zadania.
-   Wyszukaj według nazwy projektu lub klienta w celu wyszukania projektu i wprowadzenia czasu na nie.
-   Określ kategorię i działanie na czas spędzony przez użytkownika.
-   Umożliwia rejestrowanie czasu jako faktury lub opłaty niepodlegającego rozliczaniu w projekcie.
-   Opcjonalnie wprowadź komentarze zewnętrzne lub wewnętrzne.

## <a name="prerequisites"></a>Wymagania wstępne
Te wymagania są różne, zależnie od wersji Microsoft Dynamics 365, która została wdrożona w danej organizacji.

### <a name="prerequisites-if-you-use-dynamics-365-finance"></a>Wymagania wstępne dotyczące korzystania z Dynamics 365 Finance
Jeśli w organizacji wdrożono rozwiązanie Finance, administrator systemu musi opublikować mobilny obszar roboczy **Wprowadzanie czasu projektu**. Aby uzyskać instrukcje, zobacz [Publikowanie przestrzeni roboczej dla urządzeń przenośnych](../../dev-itpro/mobile-apps/publish-mobile-workspace.md).

### <a name="prerequisites-if-you-use-version-1611-with-platform-update-3-or-later"></a>Wymagania wstępne, jeśli używasz wersji 1611 z aktualizacją platformy 3 lub nowszą
Jeśli w organizacji wdrożono wersję 1611 z aktualizacją platformy 3 lub nowszą, administrator systemu musi spełnić następujące wymagania wstępne. 

<table>
<thead>
<tr class="header">
<th>Warunek wstępny</th>
<th>Rola</th>
<th>Opis</th>
</tr>
</thead>
<tbody>
<tr class="odd">

<td>Implementowanie 4018050 KB.</td>
<td>Administrator systemu</td>
<td>KB 4018050 to aktualizacja X ++ lub poprawka metadanych, która zawiera mobilny obszar roboczy <strong>Wpis czasu projektu</strong>. Aby zaimplementować KB 4018050, administrator systemu musi wykonać następujące kroki.
<ol>
<li><a href="../../dev-itpro/migration-upgrade/download-hotfix-lcs.md">Pobierz poprawkę metadanych z Microsoft Dynamics Lifecycle Services (LCS)</a>.</li>
<li><a href="../../dev-itpro/migration-upgrade/install-metadata-hotfix-package.md">Zainstaluj poprawkę metadanych</a>.</li>
<li><a href="../../dev-itpro/deployment/create-apply-deployable-package.md">Utwórz pakiet wdrożeniowy</a> zawierający <strong>ApplicationSuite</strong> i <strong>ProjectMobile</strong>, a następnie przekaż pakiet wdrożeniowy na LCS.</li>
<li><a href="../../dev-itpro/deployment/apply-deployable-package-system.md">Zastosowanie pakietu, który ma zostać wdrożony</a>.</li>

</ol></td>
</tr>
<tr class="even">
<td>Opublikuj mobilny obszar roboczy <strong>Wpis czasu projektu</strong>.</td>
<td>Administrator systemu</td>
<td>Zobacz <a href="../../dev-itpro/mobile-apps/publish-mobile-workspace.md">Publikowanie przestrzeni roboczej dla urządzeń przenośnych</a>.</td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-mobile-app"></a>Pobierz i zainstaluj aplikację mobilną

Pobierz i zainstaluj aplikację mobilną Finance and Operations:

-   [Na telefony Android](https://go.microsoft.com/fwlink/?linkid=850662)
-   [Dla telefonów iPhone](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a>Zaloguj się do aplikacji mobilnej
1.  Uruchom aplikację na swoim urządzeniu mobilnym.
2.  Wprowadź swój adres URL Dynamics 365.
3.  Po pierwszym zalogowaniu się jest wyświetlany monit o podanie nazwy użytkownika i hasła. Wprowadź poświadczenia.
4.  Po zalogowaniu się zostaną wyświetlone dostępne obszary robocze dla firmy. Należy pamiętać, że jeśli system Administrator opublikuje nowy obszar roboczy później, konieczne będzie odświeżenie listy obszarów roboczych urządzeń przenośnych.

[![Przeciągnij, aby odświeżyć](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)

## <a name="enter-time-by-using-the-project-time-entry-mobile-workspace"></a>Wprowadź czas za pomocą mobilnego obszaru roboczego Wpis czasu projektu
1.  Na urządzeniu przenośnym wybierz obszar roboczy **Wpisu czasu projektu**.
2.  Wybierz **Wpis czasu**. Zostaną wyświetlone daty w kalendarzu dla bieżącego tygodnia.
3.  W przypadku wybranej daty wybierz **Akcje** &gt; **Nowy wpis**.
4.  Wprowadź liczbę godzin do nagrania.
5.  Wybierz projekt dla wpisu czasu. Lista zawiera projekty, które są ładowane do aplikacji do użytku w trybie offline. Domyślnie ładowanych jest 50 elementów, ale programista może zmienić tę liczbę. Aby uzyskać więcej informacji, zobacz [Platforma mobilna](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md).
6.  Jeśli projekt nie znajduje się na liście, wybierz pozycję **Wyszukaj**. Wyszukaj według nazwy lub przejdź do wyszukiwania według nazwy projektu lub klienta.
7.  Wybierz kategorię. Lista zawiera kategorie, które są ładowane do aplikacji do użytku w trybie offline. Domyślnie ładowanych jest 50 elementów, ale programista może zmienić tę liczbę. Aby uzyskać więcej informacji, zobacz [Platforma mobilna](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md).
8.  Jeśli kategoria nie znajduje się na liście, wybierz pozycję **Wyszukaj**. Wyszukaj według kategorii lub przejdź do wyszukiwania według nazwy kategorii.
9.  Wybierz działanie. Lista zawiera działania, które są ładowane do aplikacji do użytku w trybie offline. Domyślnie ładowanych jest 50 elementów, ale programista może zmienić tę liczbę. Aby uzyskać więcej informacji, zobacz [Platforma mobilna](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md).
10. Jeśli działanie nie znajduje się na liście, wybierz pozycję **Wyszukaj**. Wyszukaj według numeru działania lub przejdź do wyszukiwania według przeznaczenia.

11. Wybierz właściwość wiersza.
12. Opcjonalnie: wprowadź wszelkie komentarze zewnętrzne i wewnętrzne.
13. Wybierz **Gotowe**.
