---
title: Wyświetlanie odpłatnego wykorzystania zasobów
description: W tym artykule zamieszczono informacje dotyczące widoku wykorzystania zasobów.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 9/26/2019
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
ms.reviewer: johnmichalak
ms.openlocfilehash: 57203ecff99ab4434dacdded04245435d31bc8e4
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8921867"
---
# <a name="view-chargeable-utilization-for-resources"></a>Wyświetlanie odpłatnego wykorzystania zasobów

[!include [banner](../includes/psa-now-project-operations.md)]
 
**Widok wykorzystania** dostępny na stronie **Wykorzystanie zasobów w usłudze Project Service** pokazuje odpłatne wykorzystanie każdego zasobu możliwego do zarezerwowania. Widok jest oparty na tablicy harmonogramu, więc zawiera wiele tych samych funkcji.

> ![Zrzut ekranu przedstawiający Widok wykorzystania.](media/FAQ-utilization-1.png)
 

Obliczenia odpłatnego wykorzystania działają w następujący sposób:

   Odpłatne wykorzystanie = (Odpłatne rzeczywiste godziny pracy) / (Dyspozycyjność zasobu)

Komórki reprezentują obliczone odpłatne wykorzystanie dla wybranego okresu (dni, tygodnie lub miesiące).

Kolory w każdej komórce ukazują odpłatne wykorzystanie zasobu w porównaniu z docelowym odpłatnym wykorzystaniem. 

Wykorzystanie docelowe można ustawić w domyślnej roli zasobu lub w samym zasobie. Obliczenia analizują najpierw osobę dla wykorzystania docelowego, a następnie domyślną rolę zasobu.

## <a name="set-target-on-a-resource"></a>Ustawianie domyślnego wykorzystania zasobu

1. Wybierz kolejno opcje **Zasoby** \> **Zasoby**. 
2. Zaznacz zasób, aby otworzyć jego rekord. 
3. Na karcie **Project Service** możesz ustawić docelowe wykorzystanie zasobu.

> ![Zrzut ekranu przedstawiający wykorzystanie karty Project Service do ustawiania wykorzystania zasobu.](media/FAQ-utilization-2.png)
 
## <a name="set-target-utilization-on-a-role"></a>Ustawianie docelowego wykorzystania dla roli

1. Wybierz kolejno opcje **Zasoby** \> **Role zasobu**. 
2. Zaznacz rolę i otwórz rekord. 
3. Wybierz docelowe wykorzystanie dla roli.

> ![Zrzut ekranu przedstawiający wykorzystanie Ról zasobów do ustawiania wykorzystania zasobu.](media/FAQ-utilization-3.png)
 
## <a name="calculate-chargeable-utilization-for-a-resource"></a>Obliczanie odpłatnego wykorzystania zasobu

Aby obliczyć odpłatne wykorzystanie zasobu, należy spełnić kilka warunków wstępnych. 

### <a name="set-default-role-for-individual-resource"></a>Ustawianie domyślnej roli dla pojedynczego zasobu

Po pierwsze wykorzystanie docelowe musi zostać ustawione dla konkretnego zasobu lub dla ról zasobów. Jeśli korzystasz z ról zasobów dla celów to każdy pojedynczy zasób musi mieć rolę domyślną. 

1. Aby to ustawić, wybierz kolejno opcje **Zasoby** \> **Zasoby**. 
2. Wybierz zasób, otwórz rekord, a następnie wybierz kartę **Project Service**. 
3. W siatce **Rola zasobu** upewnij się, że istnieje tylko jedna rola dla zasobu, a pole **Jest domyślne** zawiera wartość **Tak**.
 
### <a name="change-billing-type-for-resource-role"></a>Zmiana typu rozliczania roli zasobu

Role zasobów muszą mieć ustawiony typ rozliczania **Odpłatne**. 

1. Wybierz kolejno opcje **Zasoby** \> **Role zasobu**. 
2. Otwórz rekord, który chcesz zaktualizować, a następnie ustaw typ rozliczania domyślnie na **Odpłatne**.

### <a name="set-working-hours-for-resource-role"></a>Określanie godzin pracy dla roli zasobów
 
Zasób musi mieć określone godziny pracy dla obliczania wydajności. 

1. Wybierz kolejno opcje **Zasoby** \> **Zasoby**. 
2. Zaznacz zasób, aby otworzyć rekord, a następnie kliknij opcję **Pokaż godziny pracy**. 
3. Możesz zbiorczo zaktualizować listę zasobów, stosując polecenie **Szablon czasu pracy** z poziomu widoku **Lista zasobów**.

## <a name="troubleshooting-chargeable-actual-hours"></a>Rozwiązywanie problemów z odpłatnymi rzeczywistymi godzinami

Odpłatne rzeczywiste godziny pracy pochodzą z encji **Wartości rzeczywiste**. Wartości rzeczywiste z typem rozliczania **Odpłatne** są uwzględniane w obliczeniach, więc musisz posiadać projekty, gdzie wartości rzeczywiste są odpłatne.

Jeśli nie widzisz wykorzystania odpłatnego, oto co możesz sprawdzić:

- Zasób ma godziny pracy zdefiniowane dla wydajności.
- Zasób ma indywidualnie zdefiniowane docelowe wykorzystanie lub ma przypisaną rolę domyślną. Rola ma zdefiniowane dla niej docelowe wykorzystanie.
- Wartości rzeczywiste mają typ rozliczania **Odpłatne** dla okresu, dla którego zamierzasz obliczyć wykorzystanie. Sprawdź następujące parametry, jeśli widzisz wartości rzeczywiste z typem rozliczania innym niż Odpłatne:

  - Rola użyta dla wartości rzeczywistej ma domyślny typ rozliczania inny niż odpłatne.
  - Rola dla pozycji kontraktu projektu, z kopią projektu została ustawiona na nieodpłatne.
  - Projekt nie posiada skojarzonej pozycji kontraktu.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
