---
title: Rejestracja w przeglądzie subskrypcji Project Operations w ramach scenariuszy zasobów / zasobów niemagazynowanych
description: W tym temacie zamieszczono informacje dotyczące sposobu subskrypcji i wdrożenia Project Operations do obsługi zasobów i zasobów niemagazynowanych.
author: sigitac
ms.date: 07/02/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: f47d5a29c0e40a49aed7b3e52c5d52a9c27b8dbc
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323429"
---
# <a name="sign-up-for-project-operations-preview-subscriptions-for-resource-non-stocked-scenarios"></a>Rejestracja w przeglądzie subskrypcji Project Operations w ramach scenariuszy zasobów / zasobów niemagazynowanych

_**Zastosowane do:** Project Operations dla zasobów/scenariuszy nieopartych na zaopatrzeniu_

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Ten temat wyjaśnia, jak subskrybować ofertę wersji próbnej i wdrożyć środowisko aplikacji Project Operations dla scenariuszy obejmujących zasoby/nieobejmujących magazynowania.

## <a name="prerequisites"></a>Wymagania wstępne
- Użytkownik wdrażający wersję zapoznawczą musi posiadać prawa administratora globalnego dzierżawy Azure. Dzierżawcę można utworzyć podczas realizowania pierwszej oferty. 
- Wdrożenie środowiska Finance wymaga poprawnej subskrypcji Azure, która będzie rozliczana w ramach poszczególnego środowiska. Aby rozpocząć, należy użyć istniejącej subskrypcji lub [wersji próbnej usługi Azure](https://azure.microsoft.com/free/). Środowisko CDS jest dostępne bezpłatnie przez okres 30 dni.

> [!IMPORTANT]
> To zadanie musi wykonać tylko jedna osoba — administrator dzierżawy w organizacji. Jeśli nie jesteś subskrybentem tej wersji, zaczekaj, aż organizacja się zarejestruje i otrzymasz swoje poświadczenia użytkownika.
> 
> Wersje próbne można używać raz w ramach dzierżawcy. Wersję próbną można uruchomić tylko raz. Na potrzeby wersji próbnej zalecamy utworzenie nowego dzierżawcy.


### <a name="dynamics-365-project-operations-ce---preview-trial"></a>Dynamics 365 Project Operations (CE) — wersja próbna w wersji zapoznawczej 

Przed rozpoczęciem pracy należy się upewnić, że użytkownik jest zalogowany w przeglądarce i ma konto pracy użytkownika w dzierżawie, w której ma zostać wyświetlona wersja zapoznawcza Project Operations.

1. Zrealizuj tutaj kod pierwszej oferty, czyli aplikacji **Dynamics 365 Project Operations** [Wersja próbna aplikacji Project Operations](https://aka.ms/try-po).
2. Potwierdź zamówienie.

  Zobaczysz, że oferta potwierdzenia została zrealizowana pomyślnie.

### <a name="dynamics-365-finance-preview-trial"></a>Dynamics 365 Finance — próbna wersja zapoznawcza

Przejdź do [wersji próbnej aplikacji Dynamics 365 for Finance w wersji zapoznawczej](https://aka.ms/trypoche) i powtórz kroki z poprzedniej sekcji wraz z ofertą. Zarejestruj się w środowisku hostowanym w chmurze.  

## <a name="assign-licenses"></a>Przypisywanie licencji

> [!IMPORTANT]
> Aby wykonać poniższe kroki, potrzebny jest dostęp administracyjny do portalu Microsoft 365 swojej organizacji.

1. Przejdź do [Centrum administracyjnego Microsoft 365](https://portal.office.com/), aby przypisać licencje do użytkowników.

2. Na stronie **Aktywni użytkownicy** wybierz użytkownika, któremu chcesz przypisać licencję.

3. Sprawdź, czy wybrano licencję aplikacji **Dynamics 365 Project Operations**, i wybierz opcję **Zapisz zmiany**.

> [!NOTE]
> Oferta wersji próbnej Finance nie musi być przypisana do użytkownika.

## <a name="start-a-new-project-in-lcs"></a>Rozpoczęcie nowego projektu w LCS

Utwórz nowy projekt LCS, tak jak to opisano w temacie [Rozpoczynanie nowego projektu w LCS](create-lcs-project.md)

## <a name="add-an-azure-subscription-to-an-lcs-project"></a>Dodaj subskrypcję Azure do projektu LCS

Aby wykonać to zadanie, należy wykonać kroki opisane w temacie [Dodawanie subskrypcji Azure do projektu LCS](resource-add-azure-subscription-lcs-project.md).

## <a name="deploy-finance-demo-environment-with-project-operations-for-resourcenon-stocked-scenarios"></a>Wdrażanie środowiska demonstracyjnego Finance z Project Operations dla scenariuszy zasobów / zasobów niemagazynowanych

Postępuj zgodnie z instrukcjami w temacie [Ustanowienie nowego środowiska](resource-provision-new-environment.md), aby zakończyć wdrażanie. Skorzystaj z typu wdrożenia: [wersja demonstracyjna](/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) w celu zapoznania się z funkcjami. 

## <a name="install-cds-setup-and-configuration-data"></a>Zainstaluj konfigurację CDS i dane konfiguracyjne

Zainstaluj konfigurację CDS i dane konfiguracyjne, tak jak to opisano w temacie [Konfiguracja i stosowanie danych konfiguracyjnych w usłudze Common Data Service](resource-apply-pro-setup-config-data.md).
Wykonaj ten krok dopiero po wdrożeniu środowiska pokazowego aplikacji Finance i przygotowaniu danych do pokazu.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
