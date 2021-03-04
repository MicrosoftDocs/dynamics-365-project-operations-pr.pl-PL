---
title: Wstępne rezerwowanie wymagań
description: W tym temacie zamieszczono informacje dotyczące wstępnego rezerwowania wymagań.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/28/2019
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
ms.openlocfilehash: 09f7acb95be014034cc03d7eed9d37363d430601
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/10/2021
ms.locfileid: "5147396"
---
# <a name="soft-book-requirements"></a>Wstępne rezerwowanie wymagań

[!include [banner](../includes/psa-now-project-operations.md)]

Wymaganie zasobu może być zarezerwowane ostatecznie. Rezerwacja ostateczna powoduje utworzenie propozycji zużywającej dyspozycyjność zasobu. Następnie propozycja jest odsyłana z powrotem do wnioskodawcy w celu zatwierdzenia. Wstępna rezerwacja powoduje wstępne dodanie zasobu do zespołu projektu i ma inny status na tablicy harmonogramu, ale nie zużywa dyspozycyjności zasobu. Aby wstępnie zarezerwować zasób z tablicy harmonogramu, w polu **Stan rezerwacji** ustaw wartość **Wstępna**.

![Stan rezerwacji ustawiony na Wstępna](media/Resource-Management-image77.png)

Gdy karta **Zespół** jest wyświetlana w widoku **Nazwani członkowie zespołu**, zasób jest tam widoczny. Wstępnie zarezerwowane godziny są raportowane w kolumnie **Wstępnie zarezerwowane godziny**.

![Wstępnie zarezerwowane godziny w widoku Nazwani członkowie zespołu](media/Resource-Management-image78.png)

Wstępnie zarezerwowani członkowie zespołu mogą być przypisywani do zadań.

![Wstępnie zarezerwowany członek zespołu przypisany do zadania](media/Resource-Management-image79.png)

Na karcie **Uzgadnianie** nie są widoczne żadne rezerwacje dla wstępie zarezerwowanego zasobu, ponieważ karta **Uzgadnianie** bierze pod uwagę tylko rezerwacje ostateczne.

![Wstępnie zarezerwowany zasób bez rezerwacji na karcie Uzgadnianie](media/Resource-Management-image80.png)

> [!NOTE]
> Nie można dokonać wstępnej rezerwacji zasobu z wymagania wygenerowanego przez ogólnego członka zespołu.

W tablicy harmonogramu do wstępnych rezerwacji zasobu są używane inne kolory.

![Wstępne rezerwacje na tablicy harmonogramu](media/Resource-Management-image81.png)

Aby przekonwertować rezerwację wstępną na rezerwację ostateczną, na tablicy harmonogramu kliknij prawym przyciskiem rezerwację wstępną, a następnie wybierz kolejno polecenia **Zmień stan** \> **Zarezerwuj ostatecznie** \> **Ostateczna**.

![Zmiana stanu rezerwacji na Ostateczna](media/Resource-Management-image82.png)

Rezerwacja zostanie zmieniona, a stan zmieni się w tablicy harmonogramu. Ze względu na fakt, że stanem rezerwacji jest teraz **Ostateczna**, zasób jest pokazany jako zarezerwowany, a jego dyspozycyjność i dostępność są skorygowane.

Korzystając z tej samej metody, można anulować rezerwację ostateczną lub wstępną z tablicy harmonogramu.

Aby przekonwertować wstępnie zarezerwowany zasób na ostatecznie zarezerwowany zasób na karcie **Zespół** dla projektu, zaznacz zasób i kliknij przycisk **Potwierdź**.

![Polecenie Potwierdź](media/Resource-Management-image83.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]