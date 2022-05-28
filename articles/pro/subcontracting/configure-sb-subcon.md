---
title: Konfigurowanie tablicy harmonogramu do wyświetlania dyspozycyjności pracowników kontraktowych i podwykonawców
description: W tym temacie opisano sposób konfigurowania tablicy harmonogramu w aplikacji Microsoft Dynamics 365 Project Operations w celu pokazywania dyspozycyjności zasobów podczas określania wymagań dotyczących przydzielania zasobów projektu.
author: rumant
ms.date: 08/02/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 6e382b33fafe91c8b96a91d033fe12b998114bdc
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/14/2022
ms.locfileid: "8587859"
---
# <a name="configure-schedule-board-to-show-contract-workers-and-subcontracted-capacity"></a>Konfigurowanie tablicy harmonogramu do wyświetlania dyspozycyjności pracowników kontraktowych i podwykonawców 

[!include [banner](../../includes/dataverse-preview.md)]

_**Zastosowane w:** Wdrażanie uproszczone — od okazji do faktury pro forma_

Tablica harmonogramu w aplikacji Microsoft Dynamics 365 Project Operations może być używana do wyszukiwania zasobów na dwa sposoby:

- Wyszukiwanie ogólne zasobów bez kontekstu określonych wymagań zasobów opartych na projektach.
- Wyszukiwanie zasobów dla określonych wymagań, w którym wymaganie projektu zapewnia kontekst dla sugerowanych zasobów.

Aby powiadomić tablicę harmonogramu dyspozycyjności podwykonawców i pracowników kontraktowych, należy dokonać aktualizacji ustawień tablicy harmonogramu. Aktualizacje te obejmują: 
- Aktualizowanie ustawień tablicy harmonogramu dla ogólnego wyszukiwania zasobów.
- Aktualizowanie ustawień tablicy harmonogramu dla wyszukiwania zasobów opartego na wymaganiach.

## <a name="update-schedule-board-settings-for-general-resource-search"></a>Aktualizowanie ustawień tablicy harmonogramu dla ogólnego wyszukiwania zasobów
### <a name="update-filters-for-general-resource-search"></a>Aktualizowanie filtrów dla ogólnego wyszukiwania zasobów
Podczas wyszukiwania zasobu należy zaktualizować filtry dostępne w tablicy harmonogramu, tak aby można było także wyszukać zasoby zewnętrzne, określając co najmniej następujące informacje:
  - Typ pracownika, czy wyświetlane zasoby powinny być pracownikami kontraktowymi, czy pracownikami.
  - Firma dostawcy, do której powinien należeć zasób.
  - Zasoby należące do określonej podumowy lub pozycji podumowy.
    
### <a name="update-retrieve-resource-query"></a>Aktualizowanie zapytania dotyczącego pobierania zasobów
Zapytanie używane do wyszukiwania należy także zaktualizować, tak aby korzystało z dodatkowych atrybutów filtru. Aby zaktualizować konfigurację tablicy harmonogramu dla ogólnego wyszukiwania zasobów, należy wykonać następujące kroki:  
1. Otwórz **ustawienia tablicy harmonogramu** dla określonej tablicy harmonogramu.
2. Otwórz kartę **Ustawienia ogólne** i przewiń do pozycji **Inne ustawienia**.
3. Z listy ustawień w tej sekcji można zaktualizować **układ filtru** do pozycji **Domyślny układ filtrów dla usługi Project Operations — wersja uproszczona**.
4. Zaktualizuj **zapytanie dotyczące pobierania zasobów** do pozycji **Domyślne zapytanie dotyczące pobierania zasobów dla usługi Project Operations — wersja uproszczona**.

![Aktualizowanie ustawień tablicy harmonogramu dla ogólnego wyszukiwania zasobów](../media/BoardSettings.png)  

## <a name="update-schedule-board-settings-for-requirementbased-resource-search"></a>Aktualizowanie ustawień tablicy harmonogramu dla wyszukiwania zasobów opartego na wymaganiach
### <a name="update-filters-for-requirement-specific-resource-search"></a>Aktualizowanie filtrów dla wyszukiwania zasobów opartego na wymaganiach 
Podczas wyszukiwania zasobu należy zaktualizować filtry dostępne w tablicy harmonogramu, tak aby można było także wyszukać zasoby zewnętrzne, określając co najmniej następujące informacje:
 - Typ pracownika, czy wyświetlane zasoby powinny być pracownikami kontraktowymi, czy pracownikami.
 - Firma dostawcy, do której powinien należeć zasób.
 - Zasoby należące do określonej podumowy lub pozycji podumowy.

### <a name="update-retrieve-resource-query-for-requirement-specific-resource-search"></a>Aktualizowanie zapytania dotyczącego pobierania zasobów dla wyszukiwania zasobów opartego na wymaganiach 
Zapytanie używane do wyszukiwania należy także zaktualizować, tak aby korzystało z dodatkowych atrybutów filtru. Aby zaktualizować konfigurację tablicy harmonogramu dla wyszukiwania zasobów opartego na wymaganiach, należy wykonać następujące kroki:

1. Otwórz **ustawienia tablicy harmonogramu** dla określonej tablicy harmonogramu, a następnie wybierz opcję **Otwórz ustawienia domyślne**, aby otworzyć ustawienia wyszukiwania opartego na wymaganiach.
2. Otwórz kartę **Ustawienia ogólne** i przewiń do pozycji **Inne ustawienia**.
3. Z listy ustawień w tej sekcji można zaktualizować **układ filtru** do pozycji **Domyślny układ filtrów dla usługi Project Operations — wersja uproszczona**.
4. Zaktualizuj **zapytanie dotyczące pobierania zasobów** do pozycji **Domyślne zapytanie dotyczące pobierania zasobów dla usługi Project Operations — wersja uproszczona**.
5. Otwórz kartę **Typy harmonogramów** i przejdź do obszaru **Projekt**.
6. W obszarze ustawień **projektu** zaktualizuj **Zapytanie dotyczące zasobów asystenta planowania** do pozycji **Domyślne zapytanie dotyczące pobierania zasobów dla usługi Project Operations — wersja uproszczona** , a następnie zaktualizuj **Zapytanie dotyczące ograniczeń asystenta planowania** do pozycji **Domyślne zapytanie dotyczące pobierania ograniczeń dla usługi Project Operations — wersja uproszczona**.

![Aktualizowanie ustawień tablicy harmonogramu dla wyszukiwania zasobów opartego na wymaganiach](../media/SASettings.png)  

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
