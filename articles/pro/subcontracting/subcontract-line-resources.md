---
title: Zasoby wiersza podumowy
description: W tym artykule wyjaśniono sposób określania dedykowanych zasobów dostarczanych przez dostawcę na określony czas z konkretną pozycją podumowy.
author: rumant
ms.date: 09/14/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 04e3e5ee70c50068304a8a6c8f7e93df48ed7e85
ms.sourcegitcommit: 08eb3be9eda44e9446c43ed9b6aefd58d77927c5
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 09/15/2022
ms.locfileid: "9522386"
---
# <a name="subcontract-line-resources"></a>Zasoby wiersza podumowy

_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_

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
