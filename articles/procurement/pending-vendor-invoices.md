---
title: Zakup materiałów niemagazynowanych za pomocą oczekujących faktur od dostawcy
description: W tym temacie wyjaśniono, jak rejestrować oczekujące faktury od dostawcy.
author: sigitac
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: b5e6632d73c8a211b1f0d568be8e10ef47be77e2
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 05/10/2021
ms.locfileid: "5993819"
---
# <a name="purchase-non-stocked-materials-using-a-pending-vendor-invoice"></a>Zakup materiałów niemagazynowanych za pomocą oczekujących faktur od dostawcy

_**Zastosowane do:** Project Operations dla zasobów/scenariuszy nieopartych na zaopatrzeniu_

W związku z tym, że firma nabywa niezabezpieczone materiały dla projektu, można od razu zarejestrować koszty związane z projektem. 

Na przykład Contoso Robotics US wykonuje projekt odnowienia sprzętu i potrzebuje licencji na oprogramowanie. Te licencje można uzyskać od innych dostawców.  Korzystając z funkcji Dynamics 365 Finance, pracownik odpowiedzialny za rozrachunki z dostawcami dodaje fakturę od dostawcy i przypisuje koszty licencji bezpośrednio w ramach projektu odnowienia sprzętu. 

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
    - Rzeczywista transakcja projektu w Dataverse. Ta transakcja jest dalej przetwarzana przy użyciu [dziennika integracji Project Operations](../project-accounting/project-operations-integration-journal.md). Umieszczenie tej kwoty powoduje przeniesienie kwoty z konta integracji na konto kosztów projektu.
