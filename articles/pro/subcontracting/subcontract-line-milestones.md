---
title: Punkty kontrolne wiersza podumowy
description: W tym artykule opisano sposób tworzenia i obsługi harmonogramu faktur opartego na punktach kontrolnych dla podwykonawcy z dostawcą.
author: rumant
ms.date: 08/06/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: b146bf0becff5d0fa0da59f50c0d04aafaf5115f
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8927617"
---
# <a name="subcontract-line-milestones"></a>Punkty kontrolne wiersza podumowy

[!include [banner](../../includes/dataverse-preview.md)]

_**Zastosowane w:** Wdrażanie uproszczone — od okazji do faktury pro forma_

W aplikacji Dynamics 365 Project Operations wiersz umowy z metody rozliczania o stałej cenie może określać harmonogram faktur oparty na punktach kontrolnych dla dostawcy.

Punkty kontrolne dla faktur dostawcy mogą być generowane automatycznie z ustawioną częstotliwością lub można je tworzyć ręcznie.

## <a name="automatically-create-a-milestone-based-invoice-schedule-for-a-subcontract-line"></a>Automatyczne tworzenie harmonogramu faktur opartego na punktach kontrolnych dla wiersza podumowy

Wykonaj następujące kroki, aby automatycznie wygenerować harmonogram faktur oparty na punktach kontrolnych dla stałego zestawu równomiernie rozproszonych punktów kontrolnych.

1. Przejdź do pozycji **Ustawienia** > **Częstotliwości faktur** i skonfiguruj częstotliwość faktur dla wierszy podumowy.
2. Otwórz stronę **Podumowy**, otwórz podumowę, z którą chcesz pracować, a następnie otwórz wiersz podumowy o stałej cenie, dla którego chcesz utworzyć harmonogram punktów kontrolnych.
3. Na karcie **Punkty kontrolne wiersza podumowy** wybierz opcję **Generuj okresowe punkty kontrolne**.
4. W oknie dialogowym wprowadź lub wybierz zakres dat, liczbę punktów kontrolnych i częstotliwość faktur. Możesz wybrać datę rozpoczęcia lub wybrać liczbę punktów kontrolnych, częstotliwość faktur lub datę rozpoczęcia albo wybrać datę zakończenia i częstotliwość faktur. Nie można wybrać daty zakończenia i liczby punktów kontrolnych.
Na podstawie tych informacji system tworzy punkty kontrolne i rekordy widoczne w siatce **Punkty kontrolne**.

   - **Nazwa punktu kontrolnego** — nazwa punktu kontrolnego jest ustawiana na datę punktu kontrolnego w zależności od częstotliwości faktur.
   - **Data punktu kontrolnego** — data na podstawie częstotliwości faktur.
   - **Kwota punktu kontrolnego** — obliczana przez podzielenie na kwoty sumy częściowej w wierszu podumowy przez liczbę punktów kontrolnych.

Jeśli wiersz podumowy ma wartość w polu **Szacowana kwota podatku**, ta wartość jest równo dodawana do każdego punktu kontrolnego podczas generowania okresowych punktów kontrolnych.

Suma kwot punktów kontrolnych wiersza podumowy musi być równa wartości w wierszu podumowy. Jeśli nie są równe, wystąpi błąd. Można naprawić błąd i sprawdzić, czy suma punktów kontrolnych jest równa wartości wiersza podumowy, tworząc, edytując lub usuwając kwoty punktów kontrolnych i podatku. Po wprowadzeniu zmian zapisz i odśwież stronę, aby się upewnić, że nie ma kolejnych błędów.

## <a name="manually-create-subcontract-line-milestones"></a>Ręczne tworzenie punktów kontrolnych wiersza podumowy

Punkty kontrolny o stałej cenie w wierszu podumowy można tworzyć ręcznie, gdy nie są one okresowo dzielone. Aby ręcznie utworzyć punkt kontrolny wiersza podumowy, należy wykonać następujące kroki.

1. W okienku nawigacji wybierz pozycję **Podumowy** i otwórz podumowę, z którą chcesz pracować.
2. Otwórz wiersz podumowy o stałej cenie, dla którego chcesz utworzyć punkt kontrolny.
3. Na karcie **Punkty kontrolne wiersza podumowy** na siatce podrzędnej wybierz opcję **+ Nowy punkt kontrolny wiersza podumowy**.
4. Na stronie **Nowy punkt kontrolny wiersza podumowy** wprowadź wymagane informacje zgodnie z następującą tabelą.

    | Pole | Opis |Wpływ funkcjonalny|
    | --- | --- |----------------------|
    | Nazwa punktu kontrolnego | Nazwa punktu kontrolnego. |Ta kolumna będzie wyświetlana jako pierwsza we wszystkich wyszukiwaniach na podstawie punktów kontrolnych wierszy podumów. Wiersz faktury od dostawcy utworzony na podstawie tego punktu kontrolnego będzie również używać nazwy punktów kontrolnych wiersza podumowy jako nazwy domyślnej wiersza faktury od dostawcy.|
    | Opis | Opis punktu kontrolnego. |Wiersz faktury od dostawcy utworzony na podstawie tego punktu kontrolnego będzie również używać opisu punktów kontrolnych wiersza podumowy jako opisu domyślnej wiersza faktury od dostawcy.|
    | Data punktu kontrolnego | Data, od kiedy proces automatycznego tworzenia faktur powinien szukać stanu tego punktu kontrolnego i rozważyć jego użycie podczas fakturowania.| Ta wartość będzie używana jako domyślna data w wierszu faktury od dostawcy podczas fakturowania tego wiersza podumowy. |
    | Kwota | Kwoty lub wartości punktów kontrolnych, które będą zafakturowane na klientach. |Ta wartość jest używana jako domyślna kwota w wierszu faktury od dostawcy podczas fakturowania tego wiersza podumowy. |
    | Podatek | Kwota podatku stosowana względem punktu kontrolnego.| Ta wartość jest używana jako domyślna kwota podatku w wierszu faktury od dostawcy podczas fakturowania tego wiersza podumowy. |
    | Kwota po opodatkowaniu | To pole tylko do odczytu jest obliczane jako Kwota + Podatek.|Ta wartość jest używana jako domyślna wartość w wierszu faktury od dostawcy podczas fakturowania tego wiersza podumowy. |
    | Stan faktury | Podczas tworzenia punktu kontrolnego dla tego stanu jest zawsze ustawiana wartość **Nieprzygotowane do fakturowania**.|  Gdy stan to **Przygotowane do fakturowania**, proces tworzenia faktury dostawcy obejmuje ten punkt kontrolny na fakturze dostawcy. |

5. Wybierz pozycję **Zapisz i zamknij**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
