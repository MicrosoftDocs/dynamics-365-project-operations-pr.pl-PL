---
title: Kupuj materiały lub kategorie zaopatrzenia, których nie ma w magazynie, korzystając z oczekującej faktury od dostawcy
description: W tym artykule wyjaśniono sposób rejestrowania oczekujących faktur od dostawcy.
author: sigitac
ms.date: 09/13/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: b1c05755f6759e90e031a11261f15a2c4b6b716e
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8922005"
---
# <a name="purchase-non-stocked-materials-or-procurement-categories-using-a-pending-vendor-invoice"></a>Kupuj materiały lub kategorie zaopatrzenia, których nie ma w magazynie, korzystając z oczekującej faktury od dostawcy

_**Zastosowane do:** Project Operations dla zasobów/scenariuszy nieopartych na zaopatrzeniu_

W związku z tym, że firma nabywa materiały niezabezpieczone lub kategorie, które są kwalifikowane do projektu, można od razu zarejestrować koszty związane z projektem. 

Na przykład firma Contoso Robotics US wykonuje projekt odnowienia sprzętu i potrzebuje licencji na oprogramowanie. Te licencje można uzyskać od innych dostawców.  Korzystając z Dynamics 365 Finance, pracownik działu rozrachunków z dostawcami rejestruje oczekujący dokument faktury od dostawcy i przypisuje koszty licencji bezpośrednio do projektu odnowienia sprzętu. 

> [!IMPORTANT]
> Przed użyciem funkcji opisanych w tym artykule należy przejrzeć i zastosować wymagane konfiguracje. Aby uzyskać więcej informacji, zobacz [włączanie materiałów niezabędowych](configure-materials-nonstocked.md) i [oczekujących faktur od dostawcy oraz używanie kategorii materiałów i kategorii materiałów, które oczekują na dostawcy, w przypadku zamówień zakupu projektu i oczekujących faktur od dostawcy](configure-procurement-categories.md)

## <a name="post-a-project-related-pending-vendor-invoice"></a>Publikowanie oczekującej faktury związanej z projektem 

Oczekujące faktury dostawcy można zarejestrować na stronie **Oczekujące faktury dostawcy** (**Rozrachunki z dostawccami** > **Faktury** > **Oczekujące faktury od dostawców**). Wykonaj następujące kroki, aby opublikować oczekującą fakturę od dostawcy związaną z projektem:

1. Wybierz opcję **Rozrachunki z dostawcami** > **Faktury** i wybierz opcję **Nowa**. 
1. W polu **Konto faktury** wybierz dostawcę, a następnie w polu **Numer** wprowadź identyfikator faktury dostawcy.
1. Dodaj wiersz do faktury dostawcy, a następnie w polu **Numer pozycji** wybierz pozycję niezabędową, która została zakupiona od dostawcy. Alternatywnie, w polu **Kategoria kategorii Kategorię** postępowania wybierz kategorię, która została zakupiona od dostawcy.   
1. Dodaj ilość zakupionych produktów. System uzupełnia cenę jednostkową na podstawie konfiguracji ceny towaru niemagazynowanego. 
1. Sprawdź łączną kwotę i inne wymagane szczegóły dotyczące wiersza.
1. W szczegółach wiersza na karcie **Projekt** wybierz identyfikator projektu, do który zostanie zarejestrowany element.
1. Opcjonalnie: wybierz numer działania i zaktualizuj właściwość kategorii i wiersza projektu.
1. Zaksięguj oczekującą fakturę od dostawcy. Podczas fakturowania faktura jest rejestrowana przez system następujące informacje:
    
    - Kwotę salda dostawcy.
    - Kwotę podatku od sprzedaży.
    - Koszt w ramach projektu jest rejestrowany na koncie integracji.
    - Transakcja kosztów rzeczywistych projektu w programie Dataverse.  Ta transakcja jest dalej przetwarzana przy użyciu [dziennika integracji Project Operations](../project-accounting/project-operations-integration-journal.md). Umieszczenie tej kwoty powoduje przeniesienie kwoty z konta integracji na konto kosztów projektu. 
    - Zakupy rozliczane klientowi projektu przy użyciu metody rozliczania czasu i materiałów. Ponadto dla zakupów w programie Dataverse są tworzone niezrealizowane transakcje sprzedaży. Cennik produktów w programie Dataverse jest używany do cen sprzedaży i kwot dla nierozliczonych transakcji sprzedaży.
