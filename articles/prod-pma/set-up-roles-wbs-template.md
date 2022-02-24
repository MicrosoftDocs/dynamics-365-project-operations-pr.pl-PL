---
title: Konfigurowanie ról w szablonach struktury podziału pracy
description: Ten temat zawiera informacje na temat konfigurowania informacji o rolach w szablonach struktury podziału pracy.
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 143f1094c653fb7ac0e026b7875aa162a3eb83f7
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081992"
---
# <a name="set-up-roles-on-work-breakdown-structure-templates"></a>Konfigurowanie ról w szablonach struktury podziału pracy

[!include [banner](../includes/banner.md)]

Menedżerowie projektów mogą konfigurować szablony struktury podziału pracy (SPP), które mogą stosować podczas tworzenia SPP dla nowych projektów. Menedżerowie projektów mogą dodawać role, tworząc szablon. Poniższa procedura służy do przypisywania ról do szablonów SPP.

1. Wybierz **Zarządzanie projektami i księgowanie** > **Ustawienia** > **Projekty** > **Szablony struktury podziału pracy**.
2. Wybierz **Szczegóły** wybranego szablonu SPP.
3. Wybierz zadanie z listy, a następnie w polu **Rola** wybierz rolę, która ma zostać przypisana do zadania.

## <a name="work-with-a-wbs"></a>Praca z SPP

Istnieje możliwość utworzenia nowego SPP lub skopiowania SPP z istniejącego szablonu SPP. Menedżer projektu może łatwo zarządzać zasobami, przypisując role do nowych zadań w SPP. Role można zamieniać po uzyskaniu zasobu lub po zidentyfikowaniu potwierdzonego zasobu, który posłuży do jego poprawnego wykonania. Ta elastyczność umożliwia kierownikom projektów wykonywanie następujących zadań:

- Określ liczbę zasobów wymaganych przez pakiety pracy spp.
- Oszacuj koszty projektu.
- Ustalenie wstępnego budżetu.
- Szacowana wartość czasu trwania działania oparta na rolach i zasobach.
- Opracowywanie planów zarządzania projektami na podstawie dostępnych informacji o projekcie.

W SPP dodano dodatkowe opcje, aby lepiej wykorzystać funkcję pozyskiwania zasobów.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Opcja</th>
<th>Opis</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Przypisania zasobów</td>
<td>Wyświetl przydzielone zasoby, daty, liczbę godzin i typ rezerwacji dla zadań w SPP.</td>
</tr>
<tr class="even">
<td>Automatycznie generuj zespół</td>
<td>Zaplanowano automatyczne dodanie zasobów za pomocą ról skojarzonych z zadaniem. Finance automatycznie sugeruje planowane zasoby, korzystając z wielokryterialnej analizy decyzji opartej na rolach. Po ustawieniu ról i wysiłku (godzin) dla zadań w SPP i po zwolnieniu struktury wybierz opcję <strong>Automatycznie generuj zespół</strong>. Wymagana liczba zaplanowanych zasobów jest dodawana do listy SPP oraz na karcie <strong>Planowanie projektów i zespołów</strong>.</td>
</tr>
<tr class="odd">
<td>Zasób (lista rozwijana)</td>
<td>Na stronie <strong>Uruchom przypisanie zasobów</strong> można wybrać zasoby do rezerwacji ostatecznych lub wstępnych zależnie od określonego czasu trwania. Można dostosować ustawienia widoku w celu wyświetlenia i ustawienia czasu trwania działań zasobu. Możesz wybrać i przypisać zasoby na poziomie pakietu roboczego, korzystając z następujących opcji:
<ul>
<li><strong>Zaakceptuj</strong> — Potwierdzanie zmian zasobu przydzielonego do zadania.</li>
<li><strong>Anuluj</strong> — Anulowanie zmian zasobu przydzielonego do zadania.</li>
<li><strong>Automatyczne przypisywanie</strong> — dostępny zasób pracowniczy, który ma zgodną rolę, jest automatycznie wybierany i przypisywany wybranemu zadaniu.</li>
</ul></td>
</tr>
</tbody>
</table>

1. Na stronie **Wszystkie projekty** wybierz projekt **XYZ uaktualnianie faza 2**.
2. Wybierz **Plan** > **Działania** > **Struktura podziału pracy**.
3. Wybierz opcję **Nowy**, aby dodać następujące działania poziomu pierwszego do WBS:

    - Inicjowanie
    - Planowanie
    - Wykonywanie
    - Monitorowanie i kontrolowanie
    - Zamykanie

4. Ustaw daty i nakład pracy (godziny), tak jak to pokazano na poniższej ilustracji.

    [![Ustawianie dat i wysiłku](./media/projectresourcing10.jpg)](./media/projectresourcing10.jpg)

5. Zaznacz wiersz zadania **Inicjowanie**, a następnie w polu **Rola** wybierz pozycję **Starszy kierownik projektu**.
6. Wybierz **Publikuj**.
7. W tym samym wierszu w polu **Zasób** wybierz opcję **Daniel Goldschmidt**, a następnie wybierz opcję **Zaakceptuj**.
8. Wybierz wiersz zadania **Planowania**, a następnie w polu **Rola** wybierz pozycję **Analityk biznesowy**.
9. Wybierz opcję **Opublikuj**, a następnie wybierz opcję **Automatyczne generowanie zespołu**.
10. W oknie z komunikatem potwierdzenia wyświetlany wybierz **Tak**.
11. W polu **Zasób** sprawdź, czy wartość jest **Analitykiem biznesowym 1**.
12. W przypadku zasobu **Analityk biznesowy 1** otwórz wyszukiwanie i wybierz opcję **Uruchom przydziały zasobów**. Następnie wybierz pracownika do wykonania zadania.
13. Wybierz opcję **Wstępne przypisanie** &gt; **Pełna wydajność**.

    > [!NOTE] 
    > Nie otrzymasz ostrzeżenia, że określony zasób wynosi teraz 2, ponieważ liczba zasobów pozostaje 1.

14. Na stronie **Struktura podziału pracy** sprawdź poprawność przydziału zasobu w SPP, a następnie wybierz pozycję **Zapisz**.
