---
title: Tworzenie faktur międzyfirmowych dla klienta i dostawcy
description: Ten artykuł zawiera informacje na temat tworzenia międzyfirmowych faktur dla klientów i od dostawców.
author: sigitac
ms.date: 04/12/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: fd7696c32760423c876362ca3ae0ee2c7b5716e9
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8916393"
---
# <a name="create-intercompany-customer-and-vendor-invoices"></a>Tworzenie faktur międzyfirmowych dla klienta i dostawcy

_**Zastosowane do:** Project Operations dla zasobów/scenariuszy nieopartych na zaopatrzeniu_

Osoba zajmująca się księgowaniem projektu w firmie wypożyczającej tworzy fakturę międzyfirmową na koszty projektu, która jest przekazywana do firmy pożyczającej. Gdy faktura międzyfirmowa dla klienta zostanie zatwierdzona i zaksięgowana, firma wypożyczająca wysyła fakturę międzyfirmową do firmy pożyczającej.

Osoba zajmująca się księgowaniem projektu w firmie wypożyczającej może skonfigurować proces przetwarzania wsadowego, który będzie cyklicznie generował faktury międzyfirmowe. Osoba zajmująca się księgowaniem projektu w firmie wypożyczającej określa kryteria, takie jak konkretne projekty, aby tworzyć faktury międzyfirmowe w partii.

## <a name="manually-create-an-intercompany-customer-invoice-for-project-transactions"></a>Ręczne tworzenie faktury międzyfirmowej dla klienta na potrzeby transakcji projektu 

Ta procedura służy do ręcznego tworzenia faktury międzyfirmowej dla klienta na potrzeby transakcji projektu. Wyszukaj godziny zaksięgowane przez pracowników w ramach projektów w firmach pożyczających oraz wydatki poniesione przez firmy wypożyczające w imieniu firm wypożyczających. Wyszukiwanie może być przeprowadzone według nazwy firmy, numeru kontraktu projektu, numeru projektu, zakresu dat lub dowolnej kombinacji tych opcji. W wynikach wyszukiwania wybierz transakcje, które mają zostać dodane do faktury międzyfirmowej. 

Następujące czynności muszą być wykonane w podmiocie prawnym udzielającym pożyczki. 

1. W programie Dynamics 365 Finance **Zarządzanie projektami i księgowość** > **Faktury projektów** > **Międzyfirmowe faktury dla odbiorcy**. Na stronie listy **Międzyfirmowe faktury dla odbiorcy** w okienku akcji wybierz pozycję **Nowy**.
2. Na stronie **Tworzenie faktury międzyfirmowej** w polu **Firma** wybierz firmę pożyczającą.
3. Opcjonalnie: wprowadź konkretny kontrakt dotyczący projektu i numer projektu.
4. Zawęź wyniki wyszukiwania, wybierając zakres dat. Wprowadź określone daty w polach **Data rozpoczęcia** i **Data zakończenia**. W wynikach wyszukiwania będą wyświetlane tylko transakcje międzyfirmowe zaksięgowane w tym zakresie dat.
5. Ustaw **parametr zaawansowanego wiersza arkusza projektu** na **Tak** i wybierz pozycję **Wyszukaj**.
6. W wynikach wyszukiwania wybierz transakcje, które mają zostać uwzględnione w propozycji faktury międzyfirmowej, a następnie kliknij przycisk **OK**.
7. Na stronie **międzyfirmowy fakturze dla odbiorcy** zostaną wyświetlone transakcje międzyfirmowe dotyczące projektu, które wybrano z wyników wyszukiwania. W celu zmodyfikowania transakcji przed wysłaniem faktury do firmy pożyczającej należy wykonać następujące czynności:
  
    1. Na stronie **Faktura dla klienta międzyfirmowego** otwórz szczegóły faktury, a następnie wybierz opcję **Dodaj wiersz**.
    2. Aby usunąć wiersz, wybierz go, a następnie wybierz pozycję **Usuń**.
    3. Wyświetlanie komentarzy, przyczyn, rozmiarów finansowych i innych informacji o wybranym wierszu faktury.
    
8. Aby zaksięgować międzyfirmową fakturę dla klienta, w okienku akcji wybierz pozycję **Księguj**.

> [!NOTE]
> Jeśli organizacja wymaga, aby faktury międzyfirmowe były przeglądane przed zaksięgowaniem, administrator systemu może skonfigurować przepływ pracy na potrzeby faktur międzyfirmowych. Jeśli przepływ pracy nie jest skonfigurowany dla faktur międzyfirmowych, można zaksięgować fakturę międzyfirmową.

## <a name="create-a-batch-job-for-intercompany-invoices"></a>Tworzenie zadania wsadowego na potrzeby faktur międzyfirmowych

W tym samym czasie można utworzyć wiele faktur międzyfirmowych dla wszystkich firm pożyczających. Korzystając z funkcji wyszukiwania, można na przykład wyszukać wszystkie transakcje zaksięgowane przez pożyczonych pracowników i związanych z projektami zarządzanymi przez inne firmy. Następnie dla każdej firmy pożyczającej można utworzyć fakturę międzyfirmową zawierającą transakcje dostępne w wynikach wyszukiwania.

1. Przejdź do pozycji **Zarządzanie projektami i księgowanie** > **Okresowe** > **Faktury projektu** > **Tworzenie międzyfirmowych faktur dla odbiorcy**.
2. Na stronie **Tworzenie międzyfirmowej faktury dla odbiorcy** w polu **Firma** wybierz firmę wypożyczającą do zafakturowania. Jeśli nie zostanie wybrana żadna firma, wszystkie transakcje spełniające kryteria wyszukiwania zostaną wyświetlone dla wszystkich firm pożyczających.
3. W obszarze **Tworzenie jednej faktury na** wybierz, czy faktura dla transakcji międzyfirmowych ma zostać utworzona na podstawie projektu, czy w oparciu o firmę pożyczającą.
4. Opcjonalnie: aby wybrać konkretny projekt i kontrakt dotyczący projektu, dla którego chcesz utworzyć faktury międzyfirmowe, kliknij opcję **Wybierz**. Na stronie **Zapytanie** w polu **Kryteria** wybierz kontrakt projektu, numer projektu lub oba te elementy, a następnie kliknij przycisk **OK**.
5. Na karcie **Partia** skonfiguruj proces przetwarzania wsadowego w celu tworzenia cyklicznych faktur międzyfirmowych. Aby uzyskać więcej informacji, zobacz artykuł [Przesyłanie zadania przetwarzania wsadowego z formularza](/dynamicsax-2012/appuser-itpro/submit-a-batch-processing-job-from-a-form).
6. Aby księgować faktury międzyfirmowe, w okienku akcji wybierz pozycję **Księguj**.

> [!NOTE]
> Jeśli organizacja wymaga, aby faktury międzyfirmowe były przeglądane przed zaksięgowaniem, administrator systemu może skonfigurować przepływ pracy na potrzeby faktur międzyfirmowych. Jeśli przepływ pracy nie jest skonfigurowany dla faktur międzyfirmowych, można zaksięgować faktury międzyfirmowe.

## <a name="post-the-intercompany-vendor-invoice"></a>Księgowanie międzyfirmowej faktury od dostawcy

Osoba zajmująca się księgowaniem projektu w firmie pożyczającej może przeglądać międzyfirmowe, oczekujące faktur dla dostawców podczas księgowania międzyfirmowej faktury dla klienta. W aplikacji Finance w firmie pożyczającej przejdź do pozycji **Rozrachunki z dostawcami** > **Faktury** > **Oczekująca faktura od dostawcy**. Numer faktury oczekującej będzie taki sam jak numer międzyfirmowej faktury dla klienta. Upewnij się, że faktura jest poprawna, a następnie zaksięguj fakturę. Zaksięgowanie międzyfirmowej faktury od dostawcy powoduje utworzenie księgi podrzędnej projektu i transakcji księgi głównej, która odzwierciedla koszty transakcji w firmie pożyczającej.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
