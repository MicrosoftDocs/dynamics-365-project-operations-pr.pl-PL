---
title: Przechwytywanie potwierdzenia za pomocą funkcji OCR
description: W tym temat przedstawiono informacje na temat przetwarzania paragonów za pomocą technologii OCR.
author: suvaidya
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 3cfd88acec9df8468668bedbb55b399d100650e765a6ed647ed528ecca9f1554
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/06/2021
ms.locfileid: "7007744"
---
# <a name="capture-a-receipt-using-ocr"></a>Przechwytywanie potwierdzenia za pomocą funkcji OCR

_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_

Zapis wydatków został ulepszony poprzez wprowadzenie przetwarzania paragonów za pomocą technologii OCR. Ta funkcja ma na celu usprawnienie pracy użytkownika podczas tworzenia raportów o wydatkach.

## <a name="key-features"></a>Kluczowe cechy i funkcje

- System wyodrębni nazwę handlową, datę i łączną kwotę z paragonów.
- Podejmie także próbę dopasowania niedołączonych paragonów do niedołączonych transakcji wydatkowych.
- Użytkownik może tworzyć ręcznie wprowadzone transakcje wydatkowe z paragonów.

## <a name="attach-receipts-to-an-expense-report"></a>Dołączanie paragonów do raportu o wydatkach

Aby automatycznie dołączać paragony z uwzględnieniem transakcji kartą kredytową podczas tworzenia raportu z wydatków, należy wykonać następujące kroki.

  1. Otwórz obszar roboczy **Zarządzanie wydatkami**.
  2. Na karcie **Paragony** sprawdź, czy istnieją niedołączone paragony. Możesz również przekazać paragony za pomocą karty **Paragony**.
  3. Na karcie **Wydatki** sprawdź, czy istnieją niedołączone wydatki. Zazwyczaj administrator kosztów importuje te koszty, które otrzymuje od dostawcy karty kredytowej.
  4. Wybierz **Nowy raport o wydatkach**. Należy pamiętać, że podczas tworzenia raportu o wydatkach mogą zostać uwzględnione zarówno koszty, jak i przychody. W przypadku dodawania zarówno wydatków jak i paragonów zostanie wyzwolone automatyczne dopasowanie paragonów do wydatków.

## <a name="create-or-match-receipts-to-an-expense-report"></a>Tworzenie lub dopasowanie paragonów do raportu o wydatkach
W celu utworzenia wydatku lub dopasowania go do paragonu należy wykonać następujące kroki.

  1. W raporcie z wydatków na karcie **Paragony** dołącz paragon, zaznaczając pole wyboru **Dodaj paragony**.
  2. W obszarze przekazanego obrazu paragonu zwróć uwagę na opcję **Utwórz** i **Dopasuj**.

      - Wybierz opcję **Utwórz**, aby utworzyć ręcznie wprowadzoną transakcję wydatkową i wypełnij wartości wyodrębnione z paragonu.
      - W przypadku wybrania opcji **Dopasuj** system podejmie próbę dopasowania istniejących kosztów do paragonu.

## <a name="installation"></a>Instalacja

Aby wykorzystać te zaawansowane funkcje wydatkowe, należy zainstalować dodatek usługi zarządzania wydatkami (Expense Management Service) dla programu Microsoft Dynamics 365 Finance i włączyć funkcje w wystąpieniu użytkownika. Użytkownik może uzyskać dostęp do dodatku z poziomu projektu, korzystając z Microsoft Dynamics Lifecycle Services (LCS).

1. Zaloguj się do programu LCS i otwórz wybrane środowisko.
2. Wybierz pozycję **Wszystkie szczegóły**.
3. Wybierz opcję **Zachowaj** lub przewiń w dół do skróconej karty **Dodatków środowiskowych**.
4. Wybierz opcję **Zainstaluj nowy dodatek**.
5. Wybierz **Expense Management Service**.
6. Postępuj zgodnie z instrukcjami zawartymi w przewodniku po instalacji i zgódź się na warunki.
7. Wybierz **Zainstaluj**.

W obszarze **Zarządzanie funkcjami** włącz następujące funkcje:

- Przebudowane raporty wydatków
- Automatycznie dopasuj koszty i utwórz wydatek z paragonu

Po włączeniu tych funkcji zostaną wykonane następujące akcje:

- Istniejący obszar roboczy **Zarządzanie wydatkami** zostanie zastąpiony nowym obszarem roboczym.
- Dodawany jest nowy element menu z widocznością pola wydatku.
- W dalszym ciągu można otworzyć stronę **Raportów wydatków**, przechodząc do **Zarządzania wydatkami > Moje wydatki > Raporty dotyczące wydatków**.
- Przepływy pracy i wszelkie zatwierdzenia wciąż przenoszą użytkownika na stronę istniejących raportów z wydatków.
- Paragony będą przetwarzane za pośrednictwem Microsoft Azure Cognitive Services, a metadane zostaną wyodrębnione i dodane.
- Dodana jest opcja umożliwiająca utworzenie raportu z wydatków, który zawiera dopasowanie do niedołączonych paragonów.
- Opcja dodana do raportów z wydatków umożliwia utworzenie wiersza wydatku na podstawie paragonu lub podjęcie próby dopasowania istniejącego paragonu do istniejącego wiersza wydatku.

## <a name="frequently-asked-questions"></a>Często zadawane pytania

**Czy firma Microsoft używa moich danych w swoich modelach?**

Nie, firma Microsoft opracowała ogólny model uczenia maszynowego na potrzeby usługi przetwarzania paragonów. Ten model nie jest oparty na analizie przesyłanych przez użytkowników paragonów.

**Gdzie jest udostępniona ta funkcja i gdzie można przetwarzać dane?**

Obecnie obsługiwana lokalizacja to Stany Zjednoczone.

**Gdzie przesyłane są moje paragony?**

W celu wyodrębnienia danych, Finance kontaktuje się z usługami Cognitive Services. Cognitive Services zachowają kopie otrzymanego paragonu przez maksymalnie 24 godziny, w czasie których trwać będzie przetwarzanie. Po zakończeniu przetwarzania usługi Cognitive Services usuną paragon. Paragony są przechowywane w usłudze Finance.

Aby uzyskać więcej informacji, zobacz temat [Włączanie funkcji rozumienia paragonów korzystając z nowej funkcji dostępnej w Form Recognizer](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/).


[!INCLUDE[footer-include](../includes/footer-banner.md)]
