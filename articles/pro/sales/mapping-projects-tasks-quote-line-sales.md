---
title: Mapowanie projektów i zadań do wiersza oferty opartej na projekcie
description: W tym temacie zamieszczono informacje dotyczące sposobu mapowania projektów i zadań na pozycje zadań oparte na projektach.
author: rumant
manager: Annbe
ms.date: 10/05/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d726ab09da0e502da99191f7e7469c47f79b6e7c
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081904"
---
# <a name="map-projects-and-tasks-to-a-project-based-quote-line"></a>Mapowanie projektów i zadań do wiersza oferty opartej na projekcie

_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_

W wierszach oferty opartej na projektach można zamapować określone zadania projektu, które są już skojarzone z wierszem oferty.

W przypadku mapowania zadań na wiersz oferty poniższe pozycje, które zdefiniowano w wierszu oferty, będą miały zastosowanie tylko do tych zadań:

- Metoda rozliczania
- Opcje naliczania opłat
- Nieprzekraczalne limity
- Klienci

Na przykład może istnieć projekt z jedną fazą w cenie stałej i wszystkimi innymi etapami rozliczanymi na podstawie czasu i materiałów. W tym przypadku pierwszą fazę i wszystkie jej zadania podrzędne można skojarzyć z wierszem oferty w tej fazie z metodą fakturowania przy użyciu ustalonej ceny. Następnie można skojarzyć wszystkie pozostałe fazy z wierszem oferty opartej na czasie i na materiałach.

## <a name="associate-tasks-to-project-based-quote-lines"></a>Powiązanie zadań do wierszy oferty opartej na projekcie

Zadania można kojarzyć z wierszami oferty z następujących lokalizacji:

- Strona **Projekt** > karta **Fakturowanie zadania** (optymalne)
- Strona **Wiersz oferty** > karta **Zadania płatne** 

### <a name="from-the-project-page"></a>Z poziomu strony projektu

Na stronie **Projekt** można korzystać z optymalnego sposobu kojarzenia zadań z wierszami oferty. Tej strony można użyć do wybrania wielu zadań i skojarzenia wszystkich rekordów wraz z ich zadaniami podrzędnymi z wybranym wierszem oferty.

1. Na karcie **Ogólne** wiersza oferty opartej na projekcie sprawdź, czy pole **Projekt** jest wypełnione.
2. W polu **Uwzględnione zadania** wybierz opcję **Tylko zaznaczone zadania**.
3. Zapisz wiersz oferty opartej na projekcie. Po odświeżeniu formularza zostanie wyświetlona karta **Odpłatne zadania**.
4. Na karcie **Ogólne** wybierz łącze projektu z pola **Projekt**.
5. Na stronie **Projekt** wybierz kartę **Rozliczanie zadania**.
6. W drugiej siatce dotyczącej konfigurowania fakturowania dla konkretnego zadania należy wybrać jedno lub więcej zadań, a następnie wybrać opcję **Przypisz wiersze oferty**.
7. Na wyświetlonej stronie dialogowej wybierz wiersz oferty, w którym są wyświetlane wiersze oferty oparte na projekcie w danej ofercie.
8. W polu **Typ rozliczenia** wybierz, czy te zadania są płatne, czy niepłatne.
9. Zaznacz pole wyboru, aby określić, czy skojarzenie powinno zawierać zadania podrzędne zaznaczonych zadań. Zaznaczenie pola spowoduje skojarzenie zadań podrzędnych zaznaczonych zadań z wierszem oferty.
10. Wybierz **OK** , aby zamknąć okno dialogowe.

### <a name="from-the-quote-line-page"></a>Ze strony wiersz oferty

Zadania projektu można kojarzyć z wierszami oferty na karcie **Opłatne zadania** na stronie **Wiersz oferty**.

>[!NOTE]
>Optymalne miejsce do kojarzenia zadań projektu z wierszami oferty znajduje się na karcie **Rozliczanie zadań** na stronie **Projekt**. Jeśli zadania zostaną skojarzone z kartą **Odpłatne zadania** na stronie **Wiersz oferty** , należy ręcznie skojarzyć poszczególne projekty.

1. Na karcie **Ogólne** wiersza oferty opartej na projekcie sprawdź, czy w polu **Projekt** jest wybrany projekt.
2. W polu **Uwzględnione zadania** wybierz opcję **Tylko zaznaczone zadania**.
3. Zapisz wiersz oferty opartej na projekcie. Po odświeżeniu formularza zostanie wyświetlona karta **Odpłatne zadania**.
4. Na karcie **Odpłatne zadania** wybierz pozycję **Dodaj zadanie wiersza oferty**.
5. Na stronie **Zadanie z wierszem oferty** w polu **Zadania** wybierz zadanie, a następnie w polu **Typ rozliczenia** wybierz **Zapisz**. 
6. Zamyknij stronę. Wybrane zadanie jest teraz skojarzone z wierszem oferty.

## <a name="disassociate-tasks-from-projectbased-quote-lines"></a>Anulowanie powiązań zadań z wierszami oferty opartej na projekcie

### <a name="from-the-project-page"></a>Z poziomu strony projektu

Ta metoda pozwala w optymalny sposób anulować powiązania zadań z wierszami oferty. Tej strony można użyć do wybrania wielu zadań i anulowania skojarzenia wszystkich rekordów wraz z ich zadaniami podrzędnymi z wybranym wierszem oferty.

1. Na karcie **Ogólne** wiersza oferty opartej na projekcie, w polu **Projekt** wybierz link do projektu.
2. Na stronie **Projekt** wybierz kartę **Rozliczanie zadania**.
3. W drugiej siatce dotyczącej konfigurowania fakturowania dla konkretnego zadania należy wybrać jedno lub więcej zadań, a następnie wybrać opcję **Anuluj przypisanie wierszy oferty**.
4. Na wyświetlonej stronie dialogowej wybierz wiersz oferty.
5. Zaznacz pole wyboru, aby określić, czy skojarzenie powinno być usunięte z zadań podrzędnych dla zaznaczonych zadań. Zaznaczenie pola spowoduje anulowanie skojarzenia zadań podrzędnych zaznaczonych zadań z wierszem oferty.
6. Wybierz pozycję **OK**. Komunikat ostrzegawczy informuje, że jeśli to skojarzenie zostanie usunięte, wszystkie wartości rzeczywiste zarejestrowane wcześniej w tym zadaniu mogą też zostać cofnięte. 
7. Wybierz przycisk **OK** , aby kontynuować, i usuń skojarzenie między zadaniem a wierszem oferty opartej na projekcie.

### <a name="from-the-quote-line-page"></a>Ze strony wiersz oferty

Skojarzenia zadań projektu można także anulować odnośnie do wierszy oferty na karcie **Opłatne zadania** na stronie **Wiersz oferty**.

1. Na karcie **Odpłatne zadania** wybierz pozycję **Usuń zadanie wiersza oferty**.
2. Wybierz pozycję **OK**. Komunikat ostrzegawczy informuje, że jeśli to skojarzenie zostanie usunięte, wszystkie wartości rzeczywiste zarejestrowane wcześniej w tym zadaniu mogą też zostać cofnięte. 
3. Wybierz przycisk **OK** , aby kontynuować, i usuń skojarzenie między zadaniem a wierszem oferty opartej na projekcie.

>[!NOTE]
> Ta procedura nie powoduje usunięcia zadania z projektu. Usuwane jest tylko powiązanie zadania z wiersza oferty opartej na projekcie.
