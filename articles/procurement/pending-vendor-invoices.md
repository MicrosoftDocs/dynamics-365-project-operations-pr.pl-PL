---
title: Zakup materiałów niemagazynowanych za pomocą oczekujących faktur od dostawcy
description: W tym temacie wyjaśniono, jak rejestrować oczekujące faktury od dostawcy.
author: sigitac
ms.date: 09/13/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: e95f7dabe597968707fdd2dead40bfb93d7f1f95
ms.sourcegitcommit: 74a7e1c9c338fb8a4b0ad57c5560a88b6e02d0b2
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 09/23/2021
ms.locfileid: "7547302"
---
# <a name="purchase-non-stocked-materials-using-a-pending-vendor-invoice"></a>Zakup materiałów niemagazynowanych za pomocą oczekujących faktur od dostawcy

_**Zastosowane do:** Project Operations dla zasobów/scenariuszy nieopartych na zaopatrzeniu_

W związku z tym, że firma nabywa niezabezpieczone materiały dla projektu, można od razu zarejestrować koszty związane z projektem. 

Na przykład firma Contoso Robotics US wykonuje projekt odnowienia sprzętu i potrzebuje licencji na oprogramowanie. Te licencje można uzyskać od innych dostawców.  Korzystając z funkcji Dynamics 365 Finance, pracownik odpowiedzialny za rozrachunki z dostawcami dodaje fakturę od dostawcy i przypisuje koszty licencji bezpośrednio w ramach projektu odnowienia sprzętu. 

> [!IMPORTANT]
> Przed użyciem funkcji opisanych w tym temacie należy przejrzeć i zastosować wymagane konfiguracje. Aby uzyskać więcej informacji, zobacz [jak włączyć obsługę materiałów niebędących na stanie magazynowym i oczekujących na faktury dostawcy.](configure-materials-nonstocked.md). 

## <a name="post-a-project-related-pending-vendor-invoice"></a>Publikowanie oczekującej faktury związanej z projektem 

Oczekujące faktury dostawcy można zarejestrować na stronie **Oczekujące faktury dostawcy** (**Rozrachunki z dostawccami** > **Faktury** > **Oczekujące faktury od dostawców**). Wykonaj następujące kroki, aby opublikować oczekującą fakturę od dostawcy związaną z projektem:

1. Wybierz opcję **Rozrachunki z dostawcami** > **Faktury** i wybierz opcję **Nowa**. 
2. W polu **Konto faktury** wybierz dostawcę, a następnie w polu **Numer** wprowadź identyfikator faktury dostawcy.
3. Dodaj wiersz do faktury dostawcy i w polu **Numer pozycji** wybierz pozycję zakupioną od dostawcy, której brak w magazynie. 

    > [!NOTE]
    > W ramach projektu nie można rejestrować wierszy faktur dostawcy opartych na kategorii. 
    
5. Dodaj ilość kupionego towaru. System wypełni cenę jednostkową w zależności od konfiguracji ceny produktu, którego nie ma w magazynie. 
6. Sprawdź łączną kwotę i inne wymagane szczegóły dotyczące wiersza.
7. W szczegółach wiersza na karcie **Projekt** wybierz identyfikator projektu, do którego zostanie zarejestrowany element.
8. Opcjonalnie wybierz numer działania i zaktualizuj właściwość kategorii i wiersza projektu.
9. Opublikuj oczekującą fakturę dostawcy. Po zaksięgowaniu faktury system zapisuje:
    
    - Kwotę salda dostawcy.
    - Kwotę podatku od sprzedaży.
    - Koszt w ramach projektu jest rejestrowany na koncie integracji.
    - Transakcja kosztów rzeczywistych projektu w programie Dataverse.  Ta transakcja jest dalej przetwarzana przy użyciu [dziennika integracji Project Operations](../project-accounting/project-operations-integration-journal.md). Umieszczenie tej kwoty powoduje przeniesienie kwoty z konta integracji na konto kosztów projektu. 
    - Zakupy rozliczane klientowi projektu przy użyciu metody rozliczania czasu i materiałów. Ponadto dla zakupów w programie Dataverse są tworzone niezrealizowane transakcje sprzedaży. Cennik produktów w programie Dataverse jest używany do cen sprzedaży i kwot dla nierozliczonych transakcji sprzedaży.
