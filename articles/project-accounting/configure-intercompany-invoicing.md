---
title: Konfigurowanie fakturowania międzyfirmowego
description: Ten artykuł zawiera informacje i przykłady dotyczące konfigurowania międzyfirmowego fakturowania projektów.
author: sigitac
ms.date: 04/12/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: ae0c2662bb6b2789ab520f08c7c21935b651ced5
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8929411"
---
# <a name="configure-intercompany-invoicing"></a>Konfigurowanie fakturowania międzyfirmowego

_**Zastosowane do:** Project Operations dla zasobów/scenariuszy nieopartych na zaopatrzeniu_

Wykonaj następujące kroki, aby skonfigurować fakturowanie międzyfirmowe dla projektów w aplikacji Dynamics 365 Project Operations. Transakcje międzyfirmowe są transakcjami dotyczącymi czasu i wydatków z kontraktu projektu należącego do jednej firmy lub jednostki organizacyjnej, a zasoby w kontrakcie projektu stanowią część innej firmy lub jednostki organizacyjnej.

## <a name="example-configure-intercompany-invoicing"></a>Przykład: konfigurowanie fakturowania międzyfirmowego

W poniższym przykładzie Contoso Robotics USA (USPM) jest firmą pożyczającą, a Contoso Robotics UK (GBPM) jest firmą wypożyczającą. 

1. **Konfigurowanie księgowania międzyfirmowego między firmami**. Każda para firm wypożyczających i pożyczających musi zostać skonfigurowana na stronie [Księgowanie międzyfirmowe](/dynamics365/finance/general-ledger/intercompany-accounting-setup) księgi głównej.
    
    1. W programie Dynamics 365 Finance przejdź do **Księga główna** > **Ustawienia księgowania** > **Księgowanie międzyfirmowe**. Utwórz rekord zawierający następujące informacje:

        - **Firma źródłowa** = **GBPM**
        - **Firma docelowa** = **USPM**

2. **Skonfiguruj relacje handlowe między firmami**. Rekord klienta reprezentujący firmę pożyczającą musi zostać utworzony w ramach firmy wypożyczającej. Rekord dostawcy reprezentujący firmę udzielającą pożyczki musi zostać utworzony w ramach firmy pożyczającej.

     1. W aplikacji Finanse wybierz firmę **GBPM**.
     2. Przejdź do obszaru **Rozrachunki z odbiorcami** > **Klient** > **Wszyscy klienci**. Utwórz nowy rekord dla firmy **USPM**.
     3. Rozwiń pole **Nazwa**, odfiltruj rekordy według **typu** i wybierz pozycję **Firmy**. 
     4. Znajdź i wybierz rekord klienta dla firmy **Contoso Robotics USA (USPM)**.
     5. Wybierz opcję **Użyj dopasowania**. 
     6. Wybierz grupę klientów **50 — klienci międzyfirmowi**, a następnie zapisz rekord.
     7. Wybierz firmę **USPM**.
     8. Przejdź do pozycji **Rozrachunki z dostawcami** > **Dostawcy** > **Wszyscy dostawcy**. Utwórz nowy rekord dla firmy **GBPM**.
     9. Rozwiń pole **Nazwa**, odfiltruj rekordy według **typu** i wybierz pozycję **Firmy**. 
     10. Znajdź i wybierz rekord klienta dla firmy **Contoso Robotics UK (GBPM)**.
     11. Wybierz opcję **Użyj dopasowania**, wybierz grupę dostawców, a następnie zapisz rekord.
     12. W rekordzie dostawcy wybierz pozycję **Ogólne** > **Konfiguruj** > **Międzyfirmowe**.
     13. Na karcie **Relacja handlowa** ustaw pozycję **Aktywna** na **Tak**.
     14. W polu **Firma klienta** ustaw wartość **GBPM**, a następnie w polu **Rekord mojego konta** wybierz rekord klienta utworzony wcześniej w procedurze.

3. **Skonfiguruj ustawienia międzyfirmowe w parametrach zarządzania projektami i księgowania**. 

    1. Wybierz firmę **USPM** i przejdź do pozycji **Zarządzanie projektami i księgowanie** > **Konfiguracja** > **Parametry zarządzania projektami i księgowania**.
    2. Na karcie **Międzyfirmowe** wybierz kategorię zaopatrzenia, która ma być dopasowana do automatycznie wygenerowanych faktur od dostawcy.
    3. W obszarze **Kategoria domyślna** wybierz pozycję **Zasoby międzyfirmowe**.
    4. Wybierz firmę **GBPM** i przejdź do pozycji **Zarządzanie projektami i księgowanie** > **Konfiguracja** > **Parametry zarządzania projektami i księgowania**.
    5. Na karcie **Międzyfirmowe** wybierz domyślną kategorię projektu dla każdego typu transakcji. Kategorie projektów są używane do konfiguracji podatku, gdy zafakturowana kategoria w transakcjach międzyfirmowych istnieje tylko w firmie wypożyczającej. Istnieje możliwość naliczenia przychodu z transakcji międzyfirmowych. Naliczanie występuje podczas księgowania transakcji za pośrednictwem arkusza integracji aplikacji Project Operations w firmie wypożyczającej. Arkusz jest wycofywany podczas księgowania faktury międzyfirmowej.
    6. W grupie **Podczas wypożyczania zasobów innym podmiotom** wybierz opcję **...** > **Nowy**. 
    7. W siatce wybierz poniższe informacje:

          - **Firma pożyczająca** = **USPM**
          - **Przychód naliczony** = **Tak**
          - **Domyślna kategoria grafiku** = **Domyślny — godzina**
          - **Domyślna kategoria wydatku** = **Domyślny — wydatek**

4. **Skonfiguruj międzyfirmowe konta kosztów i przychodów w ustawieniach księgowania księgi**. W przypadku księgowania międzyfirmowej faktury dla klienta w firmie wypożyczającej uznawane jest konto przychodu międzyfirmowego. W przypadku księgowania pasującej oczekującej faktury dla dostawcy w firmie pożyczającej obciążane jest konto kosztu międzyfirmowego. Te konta są konfigurowane w odpowiednich firmach. 
      
     1. W aplikacji Finanse wybierz firmę wypożyczającą **USPM**. 
     2. Przejdź do pozycji **Zarządzania projektami i księgowanie** > **Konfiguracja** > **Księgowanie** > **Konfiguracja księgowania w księdze**. 
     3. Na karcie **Konta kosztów** w polu **Typ konta księgi** wybierz opcję **Koszt międzyfirmowy**. Utwórz nowy rekord zawierający następujące informacje:
      
        - **Firma wypożyczająca** = **GBPM**
        - **Konto główne** = wybierz konto głównego dla kosztu międzyfirmowego. Ta konfiguracja jest wymagana. Konfiguracja jest używana dla przepływów międzyfirmowych w Finance, ale nie w przepływach międzyfirmowych związanych z projektem. Wybór ten nie ma wpływu na procesy podrzędne. 
        
     4. Wybierz firmę wypożyczającą **GBPM**. 
     5. Przejdź do pozycji **Zarządzania projektami i księgowanie** > **Konfiguracja** > **Księgowanie** > **Konfiguracja księgowania w księdze**. 
     6. Na karcie **Konta przychodów** w polu **Typ konta księgi** wybierz opcję **Przychód międzyfirmowy**. Utwórz nowy rekord zawierający następujące informacje:

        - **Firma pożyczająca** = **USPM**
        - **Konto główne** = wybierz konto głównego dla przychodu międzyfirmowego. Ta konfiguracja jest wymagana. Konfiguracja jest używana dla przepływów międzyfirmowych w Finance, ale nie w przepływach międzyfirmowych związanych z projektem. Wybór ten nie ma wpływu na procesy podrzędne. 

5. **Skonfiguruj kalkulację cen przeniesienia na robociznę**. Kalkulacja cen przeniesienia międzyfirmowego jest konfigurowana w aplikacji Project Operations w usłudze Dataverse. Skonfiguruj [stawki kosztów robocizny](../pricing-costing/set-up-labor-cost-rate.md#transfer-pricing-and-costs-for-resources-outside-of-your-division-or-legal-entity) i [stawki rozliczania robocizny](../pricing-costing/set-up-labor-bill-rate.md#transfer-pricing-or-set-up-bill-rates-for-resources-from-other-organizational-units-or-divisions) na potrzeby fakturowania międzyfirmowego. Ceny przeniesienia nie są obsługiwane w międzyfirmowych transakcjach dotyczących wydatków. Cena sprzedaży między jednostkami organizacyjnymi będzie zawsze ustawiona na wartość identycznej jak koszt własny jednostki zasobów.

      Koszt zasobów dotyczący deweloperów w firmie Contoso Robotics UK to 88 GBP za godzinę. Contoso Robotics UK wystawi fakturę dla firmy Contoso Robotics USA na 120 USD za każdą godzinę, przez którą zasób pracował nad projektami dla Stanów Zjednoczonych. Firma Contoso Robotics USA wystawia fakturę dla klienta Adventure Works na 200 USD za pracę wykonaną zasobu dewelopera Robotics UK.

      1. W aplikacji Project Operations w usłudze Dataverse przejdź do obszaru **Sprzedaż** > **Cenniki**. Utwórz nową listę kosztów własnych o nazwie **Stawki kosztów firmy Contoso Robotics UK**. 
      2. Na liście kosztów własnych utwórz rekord zawierający następujące informacje:
         - **Rola** = **Deweloper**
         - **Koszt** = **88 GBP**
      3. Wybierz kolejno pozycje **Ustawienia** > **Jednostki organizacyjne** i dołącz tę listę kosztów własnych do jednostki organizacyjnej **Contoso Robotics UK**.
      4. Wybierz kolejno pozycje **Sprzedaż** > **Cenniki**. Utwórz listę kosztów własnych o nazwie **Stawki kosztów firmy Contoso Robotics USA**. 
      5. Na liście kosztów własnych utwórz rekord zawierający następujące informacje:
          - **Rola** = **Deweloper**
          - **Firma zasobów** = **Contoso Robotics UK**
          - **Koszt** = **120 USD**
      6. Wybierz kolejno pozycje **Ustawienia** > **Jednostki organizacyjne** i dołącz listę kosztów własnych **Stawki kosztów firmy Contoso Robotics USA** do jednostki organizacyjnej **Contoso Robotics USA**.
      7. Wybierz kolejno pozycje **Sprzedaż** > **Cenniki**. Utwórz cennik sprzedaży o nazwie **Stawki rozliczeń Adventure Works**. 
      8. W cenniku sprzedaży utwórz rekord zawierający następujące informacje:
          - **Rola** = **Deweloper**
          - **Firma zasobów** = **Contoso Robotics UK**
          - **Stawka rozliczania** = **200 USD**
      9. Przejdź do pozycji **Sprzedaż** > **Kontrakty sprzedaży** i dołącz cennik **Stawki rozliczeń Adventure Works** do cennika projektu Adventure Works w kontrakcie projektu.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
