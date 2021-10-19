---
title: Zasoby wiersza podumowy
description: W tym temacie opisano sposób określania dedykowanych zasobów dostarczanych przez dostawcę dla określonego wiersza podumowy na pewien czas.
author: rumant
ms.date: 08/06/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 4a929b985a51ab49d3e34ce4a5c277af4c05c216
ms.sourcegitcommit: d507a75a19c992a9421e4f3605162a2faa84a445
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 09/27/2021
ms.locfileid: "7558470"
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
4. Na stronie **Nowy zasób wiersza podumowy** wprowadź wymagane informacje, a następnie wybierz opcję **Zapisz i zamknij**.

W poniższej tabeli omówiono pola dotyczące zasobu wiersza podumowy.

| Pole | Opis | Wpływ funkcjonalny |
| ----- | ----------- | ----------------- |
| Zasób, który można zarezerwować | Wybierz zasób typu **Pracownik kontraktowy** z możliwością rezerwacji, którego można używać jako zasobu w wierszu podumowy.| Jeśli dla pracownika umowy nie utworzono zasobu, który można zarezerwować, to pole pozostaw puste. Przy zapisywaniu rekordu zostanie utworzony zasób, który można zarezerwować.  |
| Kontakt | Zasób wiersza podumowy można utworzyć na podstawie istniejącej umowy. Przy użyciu wyszukiwania można wyświetlić listę aktywnych kontaktów w systemie. Wybierz kontakt dla dostawcy tej podumowy. Jeśli wybrana umowa nie jest prawidłową umową dla dostawcy w podumowie, rekord zasobu wiersza podumowy nie zostanie zapisany.| Jeśli nie ma zasobu, który można zarezerwować, dla wybranego kontaktu, system tworzy taki zasób dla wybranego kontaktu przed utworzeniem zasobu wiersza podumowy. |
| Użytkownika | Zasób wiersza podumowy można utworzyć, wybierając aktywnego użytkownika. Przy użyciu wyszukiwania można wyświetlić listę aktywnych użytkowników w systemie.| Jeśli nie ma zasobu, który można zarezerwować, dla wybranego użytkownika, system tworzy taki zasób dla wybranego użytkownika przed utworzeniem zasobu wiersza podumowy. |
| Data rozpoczęcia | Data rozpoczęcia przypisania pracownika z podumowy.| Jeśli zasób jest zarezerwowany na okres, który upłynie przed tym zakresem dat, pojawi się ostrzeżenie. |
| Data zakończenia | Data zakończenia przypisania pracownika z podumowy.| Jeśli zasób jest zarezerwowany na okres, który upłynie po tym zakresie dat, pojawi się ostrzeżenie. |
| Nakład pracy | Łączna liczba godzin pracy, które pracownik kontraktowy poświęci na ten wiersz podumowy.| Jeśli zasób jest zarezerwowany poza nakład pracy przydzielony dla tej podumowy, pojawi się ostrzeżenie. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
