---
title: Jak dostosować przepływ procesów biznesowych etapów projektu?
description: Omówienie dostosowywania przepływu procesów biznesowych Etapy projektu.
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 10/11/2018
ms.topic: article
author: JohnPBurrows
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 0f95677c56b745bf7900ad503596c93f1e722281
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286171"
---
# <a name="how-do-i-customize-the-project-stages-business-process-flow"></a>Jak dostosować przepływ procesów biznesowych etapów projektu?

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-2-4x-9-0-platform](../includes/cc-applies-to-psa-app-2-4x-9-0-platform.md)]
[!INCLUDE[cc-applies-to-psa-app-1x-8-2-platform](../includes/cc-applies-to-psa-app-1x-8-2-platform.md)]

Jest znane ograniczenie we wcześniejszych wersjach aplikacji Project Service, przez które nazwy etapów w przepływie procesów biznesowych etapów projektu muszą dokładnie odpowiadać oczekiwanym nazwom w języku angielskim (**Quote**, **Plan**, **Close**). W przeciwnym razie logika biznesowa, która bazuje na nazwach etapów w języku angielskim nie będzie działała zgodnie z oczekiwaniami. Dlatego nie widzisz znanych akcji, takich jak **Przełącz proces** lub **Edytuj proces** dostępnych w formularzu projektu, i dostosowywanie przepływu procesów biznesowych nie jest zalecane. 

Tym ograniczeniem zajęto się w wersji 2.4.5.48 lub nowszej. Ten artykuł zawiera sugerowane obejścia tego problemu, jeśli musisz dostosować domyślny przepływ procesów biznesowych dla wcześniejszych wersji.  

## <a name="business-logic-requires-an-exact-match-with-english-stage-names"></a>Logika biznesowa wymaga dokładnego dopasowania z nazwami etapów w jeżyku angielskim

Przepływ procesów biznesowych etapów projektu zawiera logikę biznesową, która kieruje następującymi zachowaniami w aplikacji:
- Gdy projekt jest skojarzony z ofertą, kod ustawia przepływ procesów biznesowych na etap **Quote**.
- Gdy projekt jest skojarzony z kontraktem, kod ustawia przepływ procesów biznesowych na etap **Plan**.
- Gdy przepływ procesów biznesowych zostanie przeniesiony do etapu **Close**, rekord projektu jest dezaktywowany. Po zdezaktywowaniu projektu, formularz projektu i struktura podziału pracy (SPP) są ustawiane na Tylko do odczytu, wypuszczane są rezerwacje nazwanego zasobu, a wszelkie skojarzone cenniki zostają wyłączone.

Ta logika biznesowe bazuje na nazwach w języku angielskim dla etapów projektu. Ta zależność od nazw etapów wyrażonych w języku angielskim jest główną przyczyną, dlaczego nie jest zalecane dostosowywanie przepływu procesów biznesowych etapów projektu, oraz dlaczego nie widzisz typowych działań przepływu procesów biznesowych, takich jak **Przełącz proces** lub **Edytuj proces** na encji projektu.

## <a name="what-happens-if-the-stage-names-dont-match-the-english-names"></a>Co się dzieje, jeśli nazwy etapu nie pasują do nazw w języku angielskim?

W aplikacji Project Service 1.x na platformie 8.2 jeśli nazwy etapów przepływu procesu biznesowego nie są zgodne z wyrażonymi w języku angielskim nazw etapów, logika biznesowa, która określa odpowiedni etap dla ofert lub kontraktów, lub która zamyka projekt, jest pomijana. Nie są wyświetlane żadne komunikaty o błędach. W związku z tym wydaje się, że jesteś w stanie dostosować przepływ procesów biznesowych etapów projektu. Jednak nie będziesz widział żadnych automatycznych procesów pracujących dla ofert, kontraktów, i zamknięcia projektu.

W aplikacji Project Service 2.4.4.30 lub wcześniej na platformie 9.0 wystąpiła znacząca zmiana architektury przepływu procesów biznesowych, która wymagała ponownego zapisania logiki biznesowej przepływu procesów biznesowych. W wyniku tego nazwy etapów projektu nie są zgodne z oczekiwanymi nazwami w języku angielski i otrzymujesz komunikat o błędzie. 

W związku z tym, jeśli chcesz dostosować przepływ procesów biznesowych etapów projektu dla encji projekt, możesz dodać tylko zupełnie nowe etapy do domyślnego przepływu procesów biznesowych dla encji projekt, przy zachowaniu **Quote**, **Plan**, i **Close** bez żadnych zmian. To ograniczenie pozwala zagwarantować, że nie wystąpią błędy z logiki biznesowej, która spodziewa się nazw etapów w języku angielskim w przepływie procesów biznesowych.

W wersji 2.4.5.48 lub nowszej opisana w tym artykule logika biznesowa została usunięta z domyślnego przepływu procesów biznesowych dla encji projektu. Uaktualnianie do tej wersji lub nowszej umożliwi dostosowywanie lub zastępowanie domyślnego przepływu procesów biznesowych jakimś własnym. 

## <a name="workarounds-for-earlier-versions"></a>Obejścia dla wcześniejszych wersji

Jeśli uaktualnienie nie jest możliwe, można dostosować przepływu procesów biznesowych etapów projektu dla encji projektu na jeden z tych dwóch sposobów:

1. Dodaj dodatkowe etapy do konfiguracji domyślnej, zachowując nazwy w języku angielskim dla **Quote**, **Plan**, i **Close**.


![Zrzut ekranu przedstawiający dodawanie etapów do konfiguracji domyślnej](media/FAQ-Customize-BPF-1.png)
 
2. Utwórz własny przepływ procesów biznesowych i uczyń z niego główny przepływ procesów biznesowych dla encji projektu, co pozwoli na dowolne nazwy etapów. Jednak, jeśli chcesz użyć tych samych standardowych etapów projektu **Quote**, **Plan**, i **Close**, musisz wykonać kilka dostosowań, które wywodzą się od niestandardowych nazw etapów. Bardziej skomplikowana logika jest na zamknięciu projektu, co możesz nadal uruchomić po prostu wyłączając rekord projektu.

![Dostosowanie BPF](media/FAQ-Customize-BPF-2.png)

### <a name="additional-considerations-for-project-service-app-version-24430-or-earlier-on-platform-90"></a>Dodatkowe rozważania dotyczące aplikacji Project Service w wersji 2.4.4.30 lub wcześniejszej na platformie 9.0

W Project Service 2.4.4.30 lub w wersji wcześniejszej na platformie 9.0, z niestandardowym przepływem procesów biznesowych pole **Nazwa etapu** na encji projektu używana w wykresie **Projekt według etapu** i widoki list projektu nie ulegnie zaktualizowaniu, ponieważ jest połączona z domyślnym przepływem procesów biznesowych etapów projektu. Można zająć się tym problemem wykonując następujące kroki:

- Dodaj pole niestandardowe, aby uchwycić bieżący etap przepływu procesów biznesowych, który jest aktualizowany gdy użytkownik przechodzi przez przepływ procesów biznesowych.

- Zmodyfikuj wykres **Projekt według etapu** do pracy z niestandardowym polem zamiast domyślnej konfiguracji.

### <a name="steps-to-create-your-own-business-process-flow-for-the-project-entity"></a>Kroki w celu utworzenia własnego przepływu procesów biznesowych dla encji projektu

Aby utworzyć własny przepływ procesów biznesowych dla encji projektu przeprowadź następujące kroki:

1. Przejdź do **Ustawienia** > **Centrum procesu**. Nie kopiuj przepływu procesów biznesowych etapów projektu, ponieważ kopiuje to również logikę biznesową Project Service.

  ![Utwórz proces](media/FAQ-Customize-BPF-3.png)

2. Użyj Projektanta procesów, aby utworzyć nazwy etapu, który chcesz utworzyć. Jeśli chcesz, aby były dostępne takie same funkcje, jak na etapach domyślnych dla **Quote**, **Plan**, i **Close**, będziesz musiał to utworzyć w oparciu o swoje niestandardowe nazw etapów przepływu procesów biznesowych.

   ![Zrzut ekranu przedstawiający okno Projektant procesów używane w celu dostosowania przepływu procesów biznesowych](media/FAQ-Customize-BPF-4.png) 

3. W Projektancie procesów kliknij **Określanie kolejności przepływu procesów**, aby sprawić, że niestandardowy przepływ procesów biznesowych stanie się podstawowym przepływem procesów biznesowych przenosząc go ponad przepływ procesów biznesowych etapy projektu do górnej części listy.


   [Zrzut ekranu przedstawiający korzystanie z Określanie kolejności przepływu procesów](media/FAQ-Customize-BPF-5-720.png)

### <a name="the-following-steps-apply-to-project-service-app-24430-or-earlier-on-the-90-platform"></a>Poniższe kroki odnoszą się do aplikacji Project Service 2.4.4.30 lub wcześniej na platformie 9.0

4. Dodaj nowe pole niestandardowe do encji projektu, aby przechwycić niestandardowe etapy w niestandardowym przepływie procesów biznesowych. Będziesz musiał dodać logikę biznesową (plug-in/przepływ pracy), aby zaktualizować to pole po zaktualizowaniu etapu w przepływie procesów biznesowych.

   ![Zrzut ekranu przedstawiający dostosowywanie encji projektu](media/FAQ-Customize-BPF-6-720.png)

5. Zmodyfikuj wykres **Projekt według etapu**, aby użyć nowego pola niestandardowego dla etapów.

   ![Zrzut ekranu przedstawiający użycie wykresu Projekt według etapu](media/FAQ-Customize-BPF-7-720.png)

6. Zmodyfikuj wszystkie widoki dla encji projekt, aby objąć nowego niestandardowe pole dla etapów.

   ![Zrzut ekranu przedstawiający modyfikowanie widoków an encji projektu](media/FAQ-Customize-BPF-8-720.png)



[!INCLUDE[footer-include](../includes/footer-banner.md)]