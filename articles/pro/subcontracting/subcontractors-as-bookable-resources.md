---
title: Skonfiguruj podwykonawców jako zasoby, które można zarezerwować
description: W tym temacie wyjaśniono, jak skonfigurować i obsługiwać zasoby podwykonawców, które są tworzone na podstawie użytkowników i kontaktów w systemie, aby można je było powiązać z umowami podwykonawstwa w Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 07/28/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 6d2f250063afc24de99e308d8d7583d1822bcabb
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/14/2022
ms.locfileid: "8597259"
---
# <a name="set-up-subcontractors-as-bookable-resources"></a>Skonfiguruj podwykonawców jako zasoby, które można zarezerwować

[!include [banner](../../includes/dataverse-preview.md)]

_**Zastosowane w:** Wdrażanie uproszczone — od okazji do faktury pro forma_

Wykonaj poniższe czynności, aby skonfigurować podwykonawców jako zasoby, które można zarezerwować w Microsoft Dynamics 365 Project Operations.

1. Wybierz opcję **Projekt** \> **Zasoby** i wybierz **Nowy**.
2. Na stronie **Nowy zasób** można zarezerwować w polu **Typ zasobu** wybierz jedną z następujących opcji:

    - **Użytkownik** — wybierz ten typ zasobu, jeśli podwykonawca musi uzyskać dostęp do rozwiązania Project Operations w celu wprowadzenia czasu lub wydatków. Jeśli wybierzesz **opcję Użytkownik**, podwykonawca wymaga prawidłowej licencji dostępu do systemu.
    - **Kontakt** lub **Konto** — Wybierz jeden z tych typów zasobów, jeśli podwykonawca nie wymaga dostępu do Project Operations, ale musi być dostępny dla przydziałów zadań lub rezerwacji w projektach. Żaden z tych typów zasobów nie zapewnia dostępu do systemu. Wybierz **Konto**, aby reprezentować firmę dostawcy jako zasób, który można zarezerwować. Wybierz **Kontakt**, aby reprezentować poszczególnych pracowników dostawcy.

3. W zależności od wybranego typu zasobu zostanie wyświetlony monit o wybranie odpowiedniego rekordu użytkownika, konta lub kontaktu.
4. W polu **Typ pracownika** wybierz „Pracownik kontraktowy”, aby ustawić podwykonawcę jako zasób, który można zarezerwować.

    > [!NOTE]
    > Jeśli pozostawisz pole **Typ pracownika** puste, zasób, który można zarezerwować, zostanie uznany za pracownika.

5. Jeśli jako typ pracownika wybrano **Pracownik kontraktowy**, wybierz dostawcę, dla którego pracuje zasób..
6. Wybierz strefę czasową zasobu, a następnie wybierz opcję **Zapisz**. Aby przypisać szablon godziny pracy do zasobu, który można zarezerwować, można wybrać opcję **Ustaw kalendarz** na stronie listy **Zasoby do rezerwacji**.

Aby można było powiązać z linią podwykonawstwa, zasób, który można zarezerwować, musi spełniać następujące warunki:

- Zasób, który można zarezerwować, musi być pracownikiem kontraktowym.
- Zasób możliwy do rezerwacji typu **Kontakt** musi być skojarzony z kontem dostawcy jako kontaktem. Zasób możliwy do rezerwacji typu **Użytkownik** nie musi być skojarzony z kontem dostawcy jako kontaktem.
- Wartość pola **Dostawca** dla zasobu, który można zarezerwować, musi być zgodna z wartością pola **Dostawca** dla umowy podwykonawczej.

## <a name="update-the-type-of-worker-and-vendor-mapping-for-bookable-resources"></a>Zaktualizuj typ mapowania pracowników i dostawców dla zasobów, które można zarezerwować

Pole **Typ pracownika** dla zasobu, który można zarezerwować, określa, czy zasób, który można zarezerwować, jest pracownikiem kontraktowym, czy pracownikiem. Pole **Dostawca** definiuje konto dostawcy, z którym jest skojarzony zasób, który można zarezerwować. Kojarząc zasób, który można zarezerwować z dostawcą jako kontaktem, wskazujesz, że kontakt jest pracownikiem firmy dostawcy.

Jeśli pola **Typ pracownika** i **Dostawca** dla zasobu możliwego do zaksięgowania ulegną zmianie, zmiany wpłyną na wszelkie przyszłe walidacje nowych rekordów, które tworzy zasób możliwy do zaksięgowania, takich jak wpisy czasu. Jednak zmiany nie unieważniają istniejących rekordów.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
