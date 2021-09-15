---
title: Zasoby wiersza podumowy
description: W tym temacie opisano sposób określania dedykowanych zasobów dostarczanych przez dostawcę dla określonego wiersza podumowy na pewien czas.
author: rumant
ms.date: 08/06/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 48440f82170bde7f0a0a45f8f9849d688b232949
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323384"
---
# <a name="subcontract-line-resources"></a>Zasoby wiersza podumowy

[!include [banner](../../includes/dataverse-preview.md)]

_**Zastosowane w:** Wdrażanie uproszczone — od okazji do faktury pro forma_

W aplikacji Dynamics 365 Project Operations dostawca może określić zasoby wykorzystywane do dostarczania zakupionej wydajności zasobów w wierszu podumowy na pewien czas.

## <a name="create-subcontract-line-resources"></a>Tworzenie zasobów wiersza podumowy

Aby utworzyć zasoby wiersza podumowy, wykonaj następujące kroki.

1. W okienku nawigacji wybierz pozycję **Podumowy** i otwórz podumowę, z którą chcesz pracować.
2. Otwórz wiersz podumowy, dla którego chcesz określić zasoby dostawców.
3. Na karcie **Zasoby wiersza podumowy** na siatce podrzędnej wybierz opcję **+ Nowy zasób wiersza podumowy**.
4. Na stronie **Nowy punkt kontrolny wiersza podumowy** wprowadź wymagane informacje, a następnie wybierz pozycję **Zapisz i zamknij**.

W poniższej tabeli omówiono pola dotyczące zasobu wiersza podumowy.

| Pole |  Opis |
| ----- | ------------ |
| Zasób, który można zarezerwować | Wybierz zasób typu „Pracownik kontraktowy” z możliwością rezerwacji, którego można używać jako zasobu w wierszu podumowy. Jeśli dla pracownika kontraktowego nie utworzono jeszcze zasobu, który można zarezerwować, to pole pozostaw puste. Podczas zapisywania rekordu jest tworzony zasób, który można zarezerwować.  |
| Kontakt | Jeśli pole **Zasób, który można zarezerwować** jest puste, można utworzyć zasób wiersza podumowy na podstawie istniejącego kontaktu. Przy użyciu wyszukiwania można wyświetlić listę aktywnych kontaktów w systemie. Wybierz kontakt dla dostawcy tej podumowy. Poprawność wybranego kontaktu jest sprawdzana podczas zapisywania rekordu. Jeśli wybrany kontakt nie jest prawidłowym kontaktem, rekord nie zostanie zapisany. Jeśli nie ma zasobu, który można zarezerwować, dla wybranego kontaktu, system tworzy taki zasób dla wybranego kontaktu przed utworzeniem zasobu wiersza podumowy. |
| Użytkownika | Jeśli pole **Zasób, który można zarezerwować** jest puste, można utworzyć zasób wiersza podumowy, wybierając aktywnego użytkownika. Przy użyciu wyszukiwania można wyświetlić listę aktywnych użytkowników w systemie. Jeśli nie ma zasobu, który można zarezerwować, dla wybranego użytkownika, system tworzy taki zasób dla wybranego użytkownika przed utworzeniem zasobu wiersza podumowy. |
| Data rozpoczęcia | Data rozpoczęcia przypisania pracownika z podumowy. Jeśli zasób jest zarezerwowany na okres, który upłynie przed tym zakresem dat, pojawi się ostrzeżenie. |
| Data zakończenia | Data zakończenia przypisania pracownika z podumowy. Jeśli zasób jest zarezerwowany na okres, który upłynie po tym zakresie dat, pojawi się ostrzeżenie. |
| Nakład pracy | Łączna liczba godzin pracy pracownika z podumowy, która zostanie poświęcona na ten wiersz podumowy. Jeśli zasób jest zarezerwowany poza nakład pracy, na który został przydzielony w ramach tej podumowy, pojawi się ostrzeżenie. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
