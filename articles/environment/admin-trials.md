---
title: Rejestrowanie się w celu korzystania z wersji próbnych aplikacji Project Operations
description: W tym temacie znajdują się informacje dotyczące sposobu wdrażania wersji próbnej rozwiązania Dynamics 365 Project Operations.
author: ruhercul
ms.date: 01/10/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: a0c2532370c99cfe75b54da42c329f5b244a47e7
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/14/2022
ms.locfileid: "8584287"
---
# <a name="sign-up-for-project-operations-trials"></a>Rejestrowanie się w celu korzystania z wersji próbnych aplikacji Project Operations 

_**Ma zastosowanie do:** Project Operations dla scenariuszy opartych na zasobach/braku zapasów, wdrożenie w wersji uproszczonej — fakturowanie proforma dla transakcji i Project Operations dla scenariuszy magazynowych/opartych na produkcji_ 



W tym temacie wyjaśniono sposób subskrybowania oferty dla partnera w wersji zapoznawczej i wdrażania środowiska aplikacji Dynamics 365 Project Operations.

W nowej wersji próbnej aplikacji Project Operations można automatycznie wdrożyć dowolny z trzech obsługiwanych scenariuszy wdrażania, wykonując kwestionariusz zalecający najlepsze podejście do wdrażania. Ten temat zawiera informacje o sposobach wykonywania następujących czynności:

- Realizowanie oferty wersji próbnej.
- Inicjowanie obsługi.
- Konfigurowanie podwójnego zapisu.
- Dowiedz się więcej o aplikacji Project Operations. 

W poniższej tabeli przedstawiono szczegóły nowej oferty wersji próbnej.

| **Element oferty**               | **Szczegóły**                                  |
|------------------------------|----------------------------------------------|
| Typ oferty                   | Ten typ oferty jest potencjalnym klientem administratorem, więc do realizacji wymagany jest administrator dzierżawcy. |
| Korzystanie z oferty                    | Jeden raz na dzierżawcę                          |
| Czas trwania oferty               | 30 dni kalendarzowych                             |
| Realizacje na dzierżawcę       | 1                                            |
| Numer wewnętrzny                    | 1 rozszerzenie, 30 dni kalendarzowych               |
| Liczba środowisk wersji próbnej | 3                                            |


## <a name="admin-trial-details"></a>Szczegóły wersji próbnej administratora
W poniższej tabeli przedstawiono szczegóły wersji próbnej oraz sposób ich stosowania dla poszczególnych typów wdrożeń.

| **Produkt**                      | **Uproszczone**                                     | **Materiały niemagazynowane** | **Materiały magazynowane** |
|-------------------------------|----------------------------------------------|---------------------------|-----------------------|
| Podane dane dotyczące konfiguracji           | Tak                                          | Tak                       | Tak (USSI)            |
| Dane transakcyjne            | Brak                                           | Brak                        | Brak                    |
| Czas aprowizacji w minutach  | 15                                           | 90                        | 30                    |
 
## <a name="prerequisites"></a>Wymagania wstępne
Aby wdrożyć wersję próbną aplikacji Dynamics 365 Project Operations, wymagane są następujące wymagania wstępne.

- Rejestrowanie się w celu uzyskania aplikacji [Dynamics 365 Project Operations — wersja zapoznawcza w wersji próbnej](https://www.aka.ms/try-po).
- Użytkownik wdrażający wersję zapoznawczą musi posiadać prawa administratora globalnego dzierżawy Azure.

> [!IMPORTANT]
> To zadanie musi wykonać tylko jedna osoba w organizacji, administrator dzierżawcy. Jeśli nie jesteś subskrybentem tej wersji, zaczekaj, aż organizacja się zarejestruje i otrzymasz swoje poświadczenia użytkownika.

### <a name="dynamics-365-project-operations---preview-trial"></a>Dynamics 365 Project Operations — wersja zapoznawcza w wersji próbnej 

Przed rozpoczęciem należy zalogować się do przeglądarki, przy użyciu konta służbowego użytkownika w dzierżawie, w której ma działać wersja zapoznawcza aplikacji Project Operations.

1. Zrealizuj pierwszy kod oferty, **Dynamics 365 Project Operations — próbna wersja zapoznawcza**, wklejając go do adresu URL przeglądarki.

    ![Realizacja oferty](./media/16RedeemFirstOfferNew.png)

2. Potwierdź zamówienie.

    ![Potwierdź zamówienie](./media/17ConfirmOrderNew.png)

  Zobaczysz potwierdzenie z informacją, że oferta została pomyślnie zrealizowana.

   ![Potwierdzenie](./media/18OrderConfirmationNew.png)

  Nastąpi przekierowanie do [centrum administracyjnego platformy Power Platform](https://admin.powerplatform.microsoft.com/projectoperationstrial).

## <a name="questionnaire-and-provisioning"></a>Kwestionariusz i aprowizacja

1.  Przejdź do [centrum administracyjnego platformy Power Platform](https://admin.powerplatform.com/projectoperationstrial) i wypełnij kwestionariusz.  
2.  Przejrzyj zalecany typ wdrożenia i wybierz opcję **Rozpocznij instalację** w celu zainicjowania aprowizacji.
3.  Przejrzyj warunki, a następnie wybierz **Rozpocznij**.

   Po zakończeniu inicjowania aprowizacji nastąpi przekierowanie do listy środowiska w centrum administracyjnym Power Platform. W trakcie aprowizacji stan środowiska to **PreparingInstance**.
 
  Po zakończeniu inicjowania obsługi administracyjnej stan środowiska jest **Gotowy**. Inicjowanie obsługi środowiska obejmuje wdrożenie danych demonstracyjnych.
 
4.  Wybierz odpowiedni adres URL Microsoft Dataverse oraz adresy URL aplikacji finansowych i operacyjnych, aby zatwierdzić obraz stanowiska.

## <a name="configuring-dual-write"></a>Konfigurowanie podwójnego zapisu
- Aby skonfigurować role zabezpieczeń do podwójnego zapisu, zobacz temat [Aktualizowanie ustawień zabezpieczeń aplikacji Project Operations w usłudze Dataverse](resource-provision-new-environment.md).
- Aby skonfigurować mapy podwójnego zapisu, zobacz temat [Uruchamianie map podwójnego zapisu w aplikacji Project Operations](resource-provision-new-environment.md#run-project-operations-dual-write-maps).

## <a name="assign-licenses"></a>Przypisywanie licencji

Aby wykonać poniższe kroki, potrzebny jest dostęp administracyjny do portalu Microsoft 365 swojej organizacji.

1. Przejdź do [Centrum administracyjnego Microsoft 365](https://portal.office.com/), aby przypisać licencje do użytkowników.

   ![Strona Centrum administracyjnego](./media/14AdminPortal.png)

2. Na stronie **Aktywni użytkownicy** wybierz użytkownika, któremu chcesz przypisać licencję.

   ![Przypisywanie licencji](./media/15AssignLicenses.png)

3. Sprawdź, czy wybrano licencję **Wersja zapoznawcza aplikacji Dynamics 365 Project Operations**, i wybierz opcję **Zapisz zmiany**.

## <a name="additional-resources"></a>Dodatkowe zasoby

Poniższe zasoby zawierają wskazówki pomocne podczas rozpoczynania pracy z aplikacją Project Operations:

- [Seria filmów wideo — omówienie, szczegółowe opisy funkcji i plan rozwoju aplikacji Project Operations](https://youtube.com/playlist?list=PLcakwueIHoT_LJ3Fr1tHnkPk5lioqE6uH)
- [Dynamics 365 Project Operations](/learn/modules/examine-dynamics-365-project-operations/)
- [Określenie typu wdrażania](determine-deployment-type.md)

## <a name="frequently-asked-questions"></a>Często zadawane pytania

### <a name="what-if-i-require-alm-or-elm-for-my-finance-and-operations-apps-environment"></a>Co zrobić, jeśli potrzebuję ALM lub ELM dla mojego środowiska aplikacji finansowych i operacyjnych?

- Dla partnerów, którzy wymagają pełnych funkcji zarządzania cyklem życia środowiska, zobacz temat [Żądanie licencji w piaskownicy partnerów](https://experience.dynamics.com/requestlicense) w celu przejrzenia nowej oferty dla partnerów. 
- Aby uzyskać więcej informacji na temat praw do użytku wewnętrznego, zobacz temat [Korzyści z oprogramowania i chmury praw do użytku wewnętrznego (microsoft.com)](https://partner.microsoft.com/membership/internal-use-software).

### <a name="can-i-extend-my-trial-beyond-30-days"></a>Czy mogę przedłużyć okres mojej wersji próbnej poza 30 dni?
Aby przedłużyć okres próbny, należy wykonać następujące czynności.

1. W **Centrum administracyjnym Microsoft 365** przejdź do strony **Rozliczenia** > **Twoje produkty**.
2. Wybierz **Dynamics 365 Project Operations (CE) — wersja próbna w wersji zapoznawczej**.
3. W obszarze **Data wygaśnięcia** wybierz opcję **Przesuń datę**.

### <a name="can-i-upgrade-from-the-lite-deployment-to-the-resourcenon-stocked-based-scenario-deployment"></a>Czy można dokonać uaktualnienia z wdrożenia w wersji uproszczonej do wdrożenia scenariusza opartego na zasobach/materiałach niemagazynowanych?
Obecnie uaktualnienie środowiska z wdrożenia uproszczonego do opartego na materiałach niemagazynowanych nie jest obsługiwane.

### <a name="can-i-access-lifecycle-services-lcs-for-my-finance-environments"></a>Czy mogę uzyskać dostęp do usług Lifecycle Services (LCS) dla moich środowisk aplikacji Finance?  
Nr W przypadku tych próbnych wdrożenie jest obsługiwane za pośrednictwem centrum administracyjnego platformy Power Platform. Dostęp do środowiska aplikacji Finance jest ograniczony.

### <a name="can-i-install-my-trial-on-an-existing-environment"></a>Czy mogę zainstalować swoją wersję próbną w istniejącym środowisku?
Jeśli masz istniejące środowisko, będzie można zainstalować to wdrożenie w istniejącym środowisku sprzedaży usługi Dataverse z centrum administracyjnego platformy Power Platform.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
