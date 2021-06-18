---
title: Skonfiguruj zasoby projektu
description: W tym temacie zamieszczono informacje dotyczące ustalania lub żądania zasobów w ramach projektu.
author: Yowelle
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 49e0ca6254518079d2e01d92ac2e31d119468c4b
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 05/10/2021
ms.locfileid: "5997704"
---
# <a name="set-up-project-resources"></a>Skonfiguruj zasoby projektu

[!include [banner](../includes/banner.md)]

Należy skonfigurować kalendarz i skojarzyć go z pracownikiem lub robotnikiem. Kalendarz jest używany do zaplanowania projektu i czasu pracy zasobów, które są zarezerwowane dla projektu. Podczas konfigurowania kalendarza kierownicy projektów mogą przeprowadzać bilansowanie zasobów w ramach optymalizacji zasobów. Na podstawie harmonogramu kalendarza można przystąpić do umieszczania ograniczeń zasobów. Kalendarz można skonfigurować na stronie **Kalendarze**.

Po skonfigurowaniu pracownika jako zasobu projektu możesz wybrać spośród pracowników pracujących w firmie, dla której konfigurujesz zasoby. Alternatywnie można wybrać pracowników z innych firm należących do organizacji. Ci pracownicy są określani jako zasoby międzyfirmowe.

Poniższe procedury wyjaśniają, jak skonfigurować pracownika jako zasób projektu w firmie i jak skonfigurować zasób projektu międzyfirmowego.

## <a name="set-up-a-worker-as-a-project-resource"></a>Konfigurowanie pracownika jako zasobu projektu

1. Na stronie **Pracownicy** na liście **Pracownicy** wybierz pracownika, który ma być dodawany jako zasób projektu, i otwórz rekord pracownika.
2. W okienku akcji wybierz **Projekt** &gt; **Ustawienia** &gt; **Ustawienia projektu**.
3. Zaznacz kalendarz i zamknij stronę.

Można również określić domyślne projekty zasobu jako typ przypisywania wstępnego. Przypisań wstępnych można użyć, gdy menedżer zasobów lub kierownik projektu wie z wyprzedzeniem, nad którymi projektami będzie pracował zasób. Przypisania wstępne mogą być również oparte na żądaniu sponsora lub klienta projektu. Aby wstępnie przydzielić projekt, na stronie **Przypisywanie projektów**, na karcie **Projekty**, na liście **Pozostałe projekty** wybierz odpowiedni projekt.

## <a name="set-up-an-intercompany-resource"></a>Konfigurowanie zasobu międzyfirmowego

W przypadku konfigurowania pracownika jako zasobu międzyfirmowego należy przeprowadzić konfigurację zarówno w firmie pożyczającej, jak i firmie pożyczającej.

### <a name="in-the-lending-company"></a>W firmie pożyczkowej

1. W Finance sprawdź, czy wybrano firmę pożyczkową, a następnie wykonaj procedurę opisaną w poprzedniej sekcji „Konfigurowanie pracownika jako zasobu projektu”.
2. Na stronie **Księgowość międzyfirmowa** kliknij przycisk **Nowy**.
3. W polu **Identyfikator firmy** wybierz firmę pożyczkową. Wypełnij odpowiednio pozostałe pola, a następnie wybierz **Zapisz**.
4. Na stronie **Cena przeniesienia** kliknij przycisk **Nowy**.
5. W polu **Firma pożyczająca** wybierz odpowiednią firmę.
6. Aby pożyczyć firmie pożyczającej tylko zasób utworzony na początku tej sekcji, w polu **Zasób** wybierz nazwę utworzonego zasobu. Aby udostępnić wszystkim zasobom w firmie wypożyczanie spółce zażyczania, pole **Zasobu** powinno pozostać puste.
7. Na stronie **Parametry Zarządzanie projektami i księgowanie** na karcie **Międzyfirmowe** ustaw opcję **Włącz Międzyfirmowe planowanie zasobów i grafiki** na **Tak**.

### <a name="in-the-borrowing-company"></a>W firmie pożyczającej

- Na stronie **Lista zasobów** w filtrze wyszukiwania wprowadź nazwę zasobu utworzonego dla firmy służącej do wypożyczania, aby sprawdzić, czy nazwa znajduje się na liście zasobów dla firmy, która jest pożyczana.

## <a name="request-project-resources"></a>Żądanie zasobów projektu
Funkcjonalność planowania zasobów projektu pozwala tylko menedżerom zasobów na dystrybucję zasobów personelu w ramach zleceń lub projektów. Aby włączyć tę funkcję, należy wykonać następujące zadania lub sprawdzić, czy zostały wykonane:

- Konfigurowanie sekwencji numerów.
- Konfigurowanie przepływu pracy dotyczącego zarządzania projektami i księgowań.
- Włączanie przepływu pracy żądania zasobu.

Po wykonaniu powyższych czynności można wykonać następujące zadania, które są wymagane:

- Utwórz zlecenie zasobu na podstawie wstępnie zarezerwowanego zasobu pracowniczego.
- Monitoruj żądania zasobów.
- Realizowanie żądań zasobów.
- Zażądanie zasobu pracowniczego z SPP.
- Zarezerwuj zasoby do projektu bez żądania zasobu pracowniczego.


[!INCLUDE[footer-include](../includes/footer-banner.md)]