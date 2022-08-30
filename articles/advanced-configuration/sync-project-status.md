---
title: Stan projektu synchronizacji, aby zapobiec wprowadzania do zamkniętych projektów
description: W tym artykule wyjaśniono, jak zsynchronizować stan projektu, aby zapobiec w wprowadzaniem nieaktywnych lub zamkniętych projektów.
author: ryansandnessMSFT
ms.date: 08/09/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ryansandnessMSFT
ms.openlocfilehash: 7a306da164235f36d9ed5e69196508dce6d257de
ms.sourcegitcommit: 6b6c2bfd04e3e613ed1f38355c7cd47c3a56748d
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/24/2022
ms.locfileid: "9348040"
---
# <a name="sync-project-status-to-prevent-entry-against-closed-projects"></a>Stan projektu synchronizacji, aby zapobiec wprowadzania do zamkniętych projektów

_**Zastosowane do:** Project Operations dla zasobów/scenariuszy nieopartych na zaopatrzeniu_

## <a name="scenario"></a>Scenariusz

Firma Contoso będzie hostowana w Microsoft Dynamics 365 Project Operations w przypadku scenariuszy niezabędowych. W ramach zwykłej działalności biznesowej projekty mogą być zakończone lub wstrzymane. Można dezaktywować projekt, aby nie generować wydatków ani faktur.

## <a name="solution"></a>Rozwiązanie

### <a name="prerequisites"></a>Wymagania wstępne

-   Microsoft Dynamics 365 Finance 10.0.29 lub nowszy musi zostać zainstalowany.
-   Mapa podwójnego zapisu 1.0.0.3 dla projektów V2 (msdyn\_projects) musi być zainstalowana lub skonfigurowana ręcznie w sposób opisany poniżej.

### <a name="create-an-updated-version-of-the-project-operations-integration-projects-v2-dual-write-map"></a>Utwórz zaktualizowaną wersję mapy podwójnego zapisu Project Operations Integration Projects V2

Aby zaktualizować mapę podwójnego zapisu Project Operations Projects V2:

1. W obszarze roboczym **Zarządzania danymi** wybierz opcję **Podwójny zapis**.
2. Wybierz kafelek **Podwójny zapis**.
3. w kolumnie **Mapowania tabeli** znajdź i wybierz **Projekt V2 (msdyn\_projects)**, a następnie wybierz opcję Zatrzymaj.
4. Wybierz nazwę mapowania, aby otworzyć mapowanie, a następnie wybierz opcję **[Brak]**.
5. W oknie dialogowym Wybierz kolumnę wybierz **stan kodu \[stanu projektu\]**, a następnie wybierz opcję OK. W celu zawężenia listy można wpisać **stan** w wartości filtru.
6.  Wybierz opcję **Dodaj lub edytuj przekształcenie** w kolumnie **typu mapowania**, aby wyedytować przekształcenie.
7.  W polu **Typ przekształcenia** wybierz **ValueMap**.
8.  Wybierz opcję **Dodaj mapowanie** wartości, a następnie dodaj następujące **Klucze** i **Wartości**:

   Key       | Wartość 
   ----------|-------
   InProcess | 0     
   zakończona | 1     

![Zrzut ekranu przedstawiający mapowanie podwójnego zapisu](media/projectstage-dw-mapping.png)

9. Wybierz pozycję **Zapisz**.
10. U góry strony **Podwójny zapis > Projekty V2 (msdyn_projects)** wybierz **Zapisz jako**.
11. W okienku **Dodaj tabelę** w polu **Wydawca** wybierz opcję **Domyślny wydawca usługi CDS**.
12. Ustaw pole **Wersja** na 1.0.0.3.
13. Wpisz **Opis** i wybierz opcję **Zapisz**.
14. U góry strony **Podwójny zapis > Projects V2 (msdyn_projects)** wybierz **Uruchom**, aby uruchomić mapę, a następnie wybierz **Tak**, jeśli pojawi się prośba o potwierdzenie przed uruchomieniem. 

### <a name="close-a-newly-completed-project"></a>Zamykanie nowo zakończonego projektu

Usługa Dynamics 365 Finance używa pola **etapu projektu** do rozróżniania projektów **w toku** lub projektów **zakończonych**. **W zakończonych** projektach nie można określić wydatków ani zafakturować klientów.

1. Otwórz projekt, który ma zostać dezaktywowany.
2. Ze wstążki wybierz **Dezaktywuj**.

> [!NOTE]
> Możesz dezaktywować lub zamknąć projekt, ponieważ oba będą zachowywać się tak samo w kontekście finansów.

3. W finansach otwórz stronę listy **Wszystkie projekty**.
4. Sprawdź, czy zdezaktywowany projekt nie jest widoczny na liście.
5. W filtrze **pokaż projekty** nad listą zmień wartość **z Aktywna** na **Wszystkie**.
6. Teraz będzie wyświetlony zdezaktywowany projekt.

Jeśli użytkownik podejmie próbę zalogowania czasu lub wydatku w stosunku do tego projektu w Finance, nie powinien zobaczyć tego projektu do wyboru. Jeśli ręcznie wprowadzisz numer projektu na wydatku, zobaczysz komunikat „Zakończony etap projektu nie pozwala na nagrywanie w projekcie”. Fakturowanie i inne funkcje rozliczeniowe należy wyłączyć, ponieważ będą one w kontekście zamkniętego projektu.

