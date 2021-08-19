---
title: Tworzenie cennika
description: Tworzenie cennika w Project Service
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
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
ms.openlocfilehash: 049b36beed34ada5758d47a40a1126e0599e23e50afac83eb7ef0e37daaaaa65
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/06/2021
ms.locfileid: "6990914"
---
# <a name="create-a-price-list-project-service"></a>Utwórz cennik (Project Service)

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Cenniki zapewniają szablon, którego menedżerowie kont mogą używać do tworzenia projektów i ofert, i do określania kosztów projektu. Zapewniają one listę ról i wydatków, oraz ich ceny. Można utworzyć wiele cenników, aby obsługiwać wiele struktur cenowych przeznaczonych dla różnych regionów, w których są sprzedawane produkty, lub różnych kanałów sprzedaży. Jest to dobry pomysł, aby utworzyć co najmniej jeden cennik dla każdej waluty, w jakiej planujesz rozliczać się z klientami.  
  
Aby utworzyć szacunki finansowe dla prac, które mają zostać zrealizowane, upewnij się, że każdy projekt ma zapasowy cennik kosztów i sprzedaży. Zdefiniuj domyślny cennik sprzedaży i kosztów, który ma zastosowanie do wszystkich projektów utworzonych w Twojej organizacji.  
  
Cenniki opierają się na kategoriach wydatków i ról, więc przed utworzeniem cennika, upewnij się, że skonfigurowałeś już role i kategorie wydatków, które mają zostać użyte podczas tworzenia cennika.  
  
1.  Przejdź do **Project Service > Cennik**.  
  
2.  Kliknij pozycję **Nowy**.  
  
3.  W **Kontekst**, wybierz, czy jest to cennik dla **Koszty**, **Zakupy**, czy **Sprzedaż**.  
  
4.  W **Nazwa**, wprowadź nazwę cennika.  
  
5.  W **Waluta**, wybierz walutę, której masz zamiar użyć podczas fakturowania lub wyceny.  
  
6.  W **Jednostka czasu**, podaj okres czasu, którego dotyczy cena, taki jak dzień lub godzina.  
  
7.  W zależności od potrzeb wypełnij **Data rozpoczęcia**, **Data zakończenia**, i **Opis**.  
  
8.  Kliknij **Zapisz**, aby utworzyć rekord i móc kontynuować jego edycję.  
  
9. Aby dodać cenę roli do cennika, kliknij **+** w **Ceny ról**.  
  
10. W okienku **Cena roli** podaj szczegółowe informacje, a następnie kliknij **Zapisz**. W razie potrzeby kontynuuj dodawanie cen ról. Po skończeniu kliknij **Zapisz** w prawym dolnym rogu ekranu.  
  
11. Aby dodać cenę kategorii wydatek do cennika, kliknij **+** w **Ceny kategorii**.  
  
12. W okienku **Cena kategorii transakcji** podaj szczegółowe informacje, a następnie kliknij **Zapisz**. W razie potrzeby kontynuuj dodawanie cen kategorii. Po skończeniu kliknij **Zapisz** w prawym dolnym rogu ekranu.  
  
13. Aby dodać pozycje cennika do cennika, kliknij **+** w **Pozycje cennika**.  
  
14. W okienku **Pozycja cennika** podaj szczegółowe informacje, a następnie kliknij **Zapisz**. W razie potrzeby kontynuuj dodawanie pozycji cennika. Po skończeniu kliknij **Zapisz** w prawym dolnym rogu ekranu.  
  
15. Aby dodać relacje terytoriów do cennika, kliknij **+** w **Relacje terytoriów**.  
  
16. W okienku **Nowe połączenie** podaj szczegółowe informacje, a następnie kliknij **Zapisz**. W razie potrzeby kontynuuj dodawanie relacji terytoriów. Po skończeniu kliknij **Zapisz** w prawym dolnym rogu ekranu.  
  
### <a name="see-also"></a>Zobacz także  
 [Skonfiguruj Project Service Automation](../psa/configure.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]