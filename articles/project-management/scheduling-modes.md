---
title: Tryby planowania
description: Ten temat zawiera informacje o trybach planowania.
author: ruhercul
manager: AnnBe
ms.date: 05/04/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: fe54944999617b248ff925148a78601dd4be7aca
ms.sourcegitcommit: c45ceda833b30ad39861f5bcd3ba1bbfff11fe7a
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 05/04/2021
ms.locfileid: "5981448"
---
# <a name="scheduling-modes"></a>Tryby planowania

_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_


Dynamics 365 Project Operations umożliwia organizacjom definiowanie sposobu zarządzania zmianami w kluczowych zmiennych w zadaniach w strukturze organizacyjnej pracy. W zależności od konkretnych potrzeb organizacji menedżerowie projektów mogą wprowadzać zmiany w trybie planowania podczas tworzenia projektu.

W Project Operations dostępne są trzy tryby planowania:

  - Stały czas trwania (jest to tryb domyślny)
  - Stała praca
  - Stałe jednostki

Wartości, na które mają wpływ definicje określonego trybu planowania, są określane za pomocą następującej formuły:

  Nakład pracy (*Praca*) = Czas trwania x jednostki

Podczas definiowania trybu planowania projektu jest ustawiana jedna z tych wartości, której nie można już zmienić. Utrzymywanie tej wartości jako stałej nadaje jej priorytet, co powiadamia system, aby nie zmieniał jej, gdy zmienią się dwie pozostałe wartości. W poniższej tabeli przedstawiono informacje o wpływie wyboru konkretnego trybu.

| **W tym zadaniu**             | **Jeśli poprawiono jednostki**   | **Jeśli poprawiono czas trwania** | **Jeśli poprawiono nakład pracy**  |
|----------------------|---------------------------|----------------------------|---------------------------|
| Zadanie — stałe jednostki     | Czas trwania jest ponownie przeliczany. | Nakład pracy jest ponownie przeliczany.    | Czas trwania jest ponownie przeliczany. |
| Zadanie — stały nakład pracy    | Czas trwania jest ponownie przeliczany. | Jednostki są ponownie przeliczane.    | Czas trwania jest ponownie przeliczany. |
| Zadanie — stały czas trwania  | Nakład pracy jest ponownie przeliczany.   | Nakład pracy jest ponownie przeliczany.    | Jednostki są ponownie przeliczane.   |

Aby uzyskać więcej informacji dotyczących konsekwencji danego trybu, zobacz temat [Zmiana typu zadania w celu dokładniejszego planowania](https://support.microsoft.com/en-us/office/change-the-task-type-for-more-accurate-scheduling-b0b969ad-45bc-4e9e-8967-435587548a72). W tym temacie termin **Praca** jest używany zamiast terminu **Nakład pracy**.

## <a name="change-the-organizations-scheduling-mode"></a>Zmienianie trybu planowania organizacji

Wykonaj następujące kroki, aby zdefiniować tryb planowania organizacji.

1. Wybierz **Ustawienia** \> **Ogólne** \> **Parametry**, a następnie wybierz parametr projektowy. 
2. Na stronie **Parametry projektu** wybierz domyślny tryb planowania dla organizacji, a następnie zdefiniuj możliwość zastępowania ustawienia przez menedżera projektu podczas tworzenia nowego projektu.

## <a name="change-the-scheduling-mode-setting-on-a-project"></a>Zmienianie ustawienia trybu planowania w projekcie

Jeśli organizacja zezwala menedżerowi projektu na zastępowanie domyślnego trybu planowania, menedżer projektu może dokonać tej zmiany podczas tworzenia nowego projektu. Jednak po zapisaniu projektu nie można zmienić trybu planowania.

## <a name="copied-projects"></a>Skopiowane projekty

Ponieważ projekt jest tworzony po utworzeniu akcji kopiowania, menedżer projektu nie może ustawić trybu planowania. Projekt docelowy będzie zawsze domyślnie ustawiony na tryb zdefiniowany na poziomie organizacyjnym.

## <a name="copied-tasks"></a>Skopiowane zadania

Po skopiowaniu zadania z jednego projektu do innego zadanie dziedziczy tryb planowania docelowego projektu.
