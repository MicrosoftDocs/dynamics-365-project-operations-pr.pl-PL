---
title: Mobilna aplikacja wydatków
description: Ten temat zawiera informacje o mobilnym obszarze roboczym Zarządzanie wydatkami.
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 2cbce8fbfa622a143f3ebfc34d7d60a7da4a9171
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/27/2021
ms.locfileid: "5950899"
---
# <a name="mobile-expense-app"></a>Mobilna aplikacja wydatków

_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_

Ten temat zawiera informacje o mobilnym obszarze roboczym **Zarządzanie wydatkami**. Ten obszar roboczy umożliwia zapisywanie i przesyłanie paragonów, dzięki czemu mogą być dołączone do raportu o wydatkach w późniejszym terminie. Użytkownicy mogą również szybko tworzyć wiersze wydatków, korzystając z dołączonego paragonu i tworząc raporty dotyczące wydatków i zarządzając nimi. Ponadto osoby zatwierdzające mogą korzystać z obszaru roboczego **Zarządzania wydatkami** w celu wyświetlania przydzielonych im raportów z wydatków i zatwierdzania lub odrzucania tych raportów z wydatków.

Ten mobilny obszar roboczy jest przeznaczony do użytku z aplikacją mobilną Dynamics 365 Unified Ops.

Wiele organizacji wymaga, aby kopia paragonu była dołączana do raportu z wydatków związanych z podróżą lub z pozostałymi działaniami związanymi z działalnością pracownika, gdy pracownik składa wniosek o zwrot kosztów. Obszar roboczy **Zarządzanie wydatkami** umożliwia szybkie tworzenie nowych wierszy na wybranym urządzeniu przenośnym za pomocą dołączenia zdjęcia z paragonem. Użytkownicy mogą również zapisać zdjęcie z paragonu i później dołączyć je do raportu z wydatków. Pracownicy mogą również tworzyć raporty dotyczące wydatków i zarządzać nimi, a następnie przesyłać je do zatwierdzania i zwrotów przy użyciu swoich urządzeń przenośnych.

Obszar roboczy **Zarządzanie wydatkami** umożliwia użytkownikom wykonywanie następujących zadań:

- Zrobienie zdjęcia paragonu. Przekazanie zdjęcia z paragonu i dołączenie go do raportu o wydatkach w późniejszym terminie.
- Przesłanie pliku zapisanego paragonu. Później można dołączyć ten plik do raportu z wydatkami.
- Utworzenie nowego wiersza wydatku, korzystając z dołączonego paragonu. Później można dodać wiersz do raportu z wydatków i przesłać go do zatwierdzenia i zwrotu.

Można również użyć następujących funkcji:

- Tworzenie nowego raportu z wydatków.
- Dołączenia transakcji kartą kredytową i innych uprzednio utworzonych wydatków do raportu z wydatków.
- Tworzenia nowych kosztów na potrzeby raportu z wydatków.
- Dołączenia paragonu do dowolnego raportu z wydatków polega na zrobieniu zdjęcia lub przesłaniu pliku ze zdjęciem paragonu.
- W zależności od zasady wydatków w firmie, możesz czasami dodać koszty gości do swoich wydatków.
- W zależności od zasad wydatków w firmie może zaistnieć potrzeba podzielenia/rozbicia kosztów na pozycje.
- Wyślij raport z wydatków na potrzeby zatwierdzenia i zwrotów.
- Zatwierdź lub odrzuć raporty o wydatkach, dla których użytkownik jest przypisaną osobą zatwierdzającą.

## <a name="prerequisites"></a>Wymagania wstępne
Te wymagania są różne, zależnie od wersji, która została wdrożona w danej organizacji.

### <a name="prerequisites-if-you-use-dynamics-365-finance"></a>Wymagania wstępne dotyczące korzystania z Dynamics 365 Finance 
Jeśli w organizacji wdrożono rozwiązanie Finance, administrator systemu musi opublikować mobilny obszar roboczy **Zarządzanie wydatkami**. 

### <a name="prerequisites-if-you-use-version-1611-with-platform-update-3-or-later"></a>Wymagania wstępne, jeśli używasz wersji 1611 z aktualizacją platformy 3 lub nowszą
Jeśli w organizacji wdrożono wersję 1611 z aktualizacją platformy 3 lub nowszą, administrator systemu musi spełnić następujące wymagania wstępne. 

<table>
<thead>
<tr class="header">
<th>Warunek wstępny</th>
<th>Rola</th>
<th>Opis</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Implementowanie 4019015 KB.</td>
<td>Administrator systemu</td>
<td>KB 4019015 to aktualizacja X ++ lub poprawka metadanych, która zawiera mobilny obszar roboczy <strong>Zarządzanie wydatkami</strong>. Aby zaimplementować KB 4019015, administrator systemu musi wykonać następujące kroki.
<ol>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/download-hotfix-lcs">Pobieranie aktualizacji z Lifecycle Services</a>.</li>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/install-metadata-hotfix-package">Zainstaluj poprawkę metadanych</a>.</li>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/deployment/create-apply-deployable-package">Utwórz pakiet wdrożeniowy</a> zawierający <strong>ApplicationSuite</strong> i <strong>ExpenseMobile</strong>, a następnie przekaż pakiet wdrożeniowy na LCS.</li>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/deployment/apply-deployable-package-system">Zastosowanie pakietu, który ma zostać wdrożony</a>.</li>
</ol></td>
</tr>
<tr class="even">
<td>Opublikuj obszar roboczy <strong>Zarządzanie wydatkami</strong>.</td>
<td>Administrator systemu</td>
<td>Zobacz <a href="/dynamics365/fin-ops-core/dev-itpro/mobile-apps/publish-mobile-workspace">Publikowanie przestrzeni roboczej dla urządzeń przenośnych</a>.</td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-dynamics-365-unified-ops-mobile-app"></a>Pobierz i zainstaluj aplikację mobilną Dynamics 365 Unified Ops
Pobierz i zainstaluj aplikację mobilną Dynamics 365 Unified Ops:

- [Na telefony Android](https://go.microsoft.com/fwlink/?linkid=850662)
- [Dla telefonów iPhone](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a>Zaloguj się do aplikacji mobilnej
1. Uruchom aplikację na swoim urządzeniu mobilnym.
2. Wprowadź swój adres URL Dynamics 365.
4. Po pierwszym zalogowaniu się jest wyświetlany monit o podanie nazwy użytkownika i hasła. Wprowadź poświadczenia.
5. Po zalogowaniu się zostaną wyświetlone dostępne obszary robocze dla firmy. Jeśli administrator systemu opublikuje nowy obszar roboczy później, konieczne będzie odświeżenie listy obszarów roboczych urządzeń przenośnych.

## <a name="capture-a-receipt-by-using-the-expense-management-mobile-workspace"></a>Zapisywanie paragonów za pomocą mobilnego obszaru roboczego zarządzania wydatkami

1. Otwórz obszar roboczy **Zarządzanie wydatkami** na swoim urządzeniu przenośnym.
2. Wybierz pozycję **Zapisz paragon**.
3. Wybierz opcję **Zrób zdjęcie** lub **Wybierz obraz**.
4. Wykonaj jedną z następujących czynności:

   - W przypadku wybrania **Zrób zdjęcie** należy:

      1. Otworzy się aparat urządzenia, aby można było zrobić zdjęcie paragonu. 
      2. Po zakończeniu robienia zdjęcia kliknij przycisk **OK**, aby zaakceptować zdjęcie.
      3. Opcjonalnie: Wprowadź nazwę zdjęcia i wprowadź wszelkie notatki.

    - W przypadku wybrania **Wybierz zdjęcie** należy:

        1. Wybrać zdjęcie z listy.
        2. Opcjonalnie: Wprowadź nazwę zdjęcia i wprowadź wszelkie notatki.

5. Wybierz **Gotowe**.

## <a name="quickly-enter-expenses-by-using-the-expense-management-mobile-workspace"></a>Szybkie zapisywanie paragonów za pomocą mobilnego obszaru roboczego zarządzania wydatkami

1. Otwórz obszar roboczy **Zarządzanie wydatkami** na swoim urządzeniu przenośnym.
2. Wybierz pozycję **Szybki zapis wydatków**.
3. Wybierz kategorię identyfikatora wydatku. Zobaczysz kategorie wydatków, które są ładowane do aplikacji do użytku w trybie offline. Domyślnie ładowanych jest 50 elementów, ale programista może zmienić tę liczbę. Aby uzyskać więcej informacji, zobacz [Platforma mobilna](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-getting-started). Jeśli kategoria nie znajduje się na liście, wybierz pozycję **Wyszukaj**, aby dokonać wyszukiwania online. Wyszukaj według kategorii wydatków lub przejdź do wyszukiwania według typu wydatków.
4. Wprowadź datę transakcji wydatkowej.
5. Opcjonalnie: Wprowadź nazwę handlową dla wydatku.
6. Wprowadź pieniężną wartość wydatku.
7. Wybierz walutę i wydatek. Zobaczysz kody walut, które są ładowane do aplikacji do użytku w trybie offline. Domyślnie ładowanych jest 400 walut, ale programista może zmienić tę liczbę. Aby uzyskać więcej informacji, zobacz [Platforma mobilna](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-getting-started). Jeśli waluta nie znajduje się na liście, wybierz pozycję **Wyszukaj**, aby dokonać wyszukiwania online. Wyszukaj według waluty lub przejdź do wyszukiwania według nazwy.
8. Wybierz opcję **Zrób zdjęcie** lub **Wybierz obraz**.
9. Wykonaj jedną z następujących czynności:

    - Jeśli wybrano opcję **Zrób zdjęcie** otworzy się aparat urządzenia, aby można było zrobić zdjęcie paragonu. Po zakończeniu robienia zdjęcia kliknij przycisk **OK**, aby zaakceptować zdjęcie.
    - W przypadku wybrania **Wybierz obraz** wybierz odpowiedni obraz na liście.

10. Wybierz **Gotowe**.

## <a name="approve-an-expense-report-by-using-the-expense-management-mobile-workspace-if-you-use-the-july-2017-update"></a>Zatwierdzanie raportu z wydatków za pośrednictwem obszaru roboczego mobilnego zarządzania wydatkami (w przypadku korzystania z aktualizacji z lipca 2017 roku)

1. Otwórz obszar roboczy **Zarządzanie wydatkami** na swoim urządzeniu przenośnym.
2. **Zatwierdzanie wydatków** wskazuje liczbę raportów o wydatkach przypisanych do użytkownika w celu zatwierdzenia. Liczba ta jest aktualizowana co ok. 30 minut. Wybierz **Zatwierdzenia wydatków**.

    Wyświetlona jest lista raportów o wydatkach przypisanych do użytkownika w celu zatwierdzenia.
    
3. Wybierz jakiś raport z wydatków, aby wyświetlić jego szczegóły.
4. Wybierz jakiś wydatek, aby wyświetlić jego szczegóły. Informacje widoczne dla wydatku zawierają wszelkie informacje o paragonie, gościu i szczegółach podziału na pozycje.
5. Na stronie **Raport o wydatkach** wybierz opcję zatwierdzania lub odrzucania raportu o wydatkach.
6. Wprowadź komentarze dotyczące akcji zatwierdzania.
7. Wybierz **Gotowe**.

## <a name="create-a-new-expense-report-and-submit-it-for-approval-by-using-the-expense-management-mobile-workspace-if-you-use-the-july-2017-update"></a>Tworzenie nowego raportu z wydatków za pośrednictwem obszaru roboczego mobilnego zarządzania wydatkami i przesłanie go do zatwierdzenia (w przypadku korzystania z aktualizacji z lipca 2017 roku)

1. Otwórz obszar roboczy **Zarządzanie wydatkami** na swoim urządzeniu przenośnym.
2. Wybierz pozycję **Zapis wydatków**.
3. Wybierz opcję **Nowy raport** lub na liście wybierz istniejący raport o wydatkach.
4. W przypadku nowych raportów z wydatków wprowadź przeznaczenie oraz wszystkie dostępne dodatkowe informacje. Te informacje różnią się w zależności od sposobu, w jaki skonfigurowano funkcję zarządzanie wydatkami dla firmy użytkownika.
5. Wybierz **Gotowe**.
6. Aby dodać istniejące koszty, takie jak transakcje kartą kredytową, w raporcie z wydatków wybierz opcję **Dołącz**.
7. Z listy wybierz jeden lub więcej wydatków.
8. Wybierz **Gotowe**.
9. W celu dodania nowego wydatku do raportu z wydatków wybierz opcję **Nowy wydatek**.
10. Wybierz kategorię wydatku. Zobaczysz kategorie wydatków, które są ładowane do aplikacji do użytku w trybie offline. Domyślnie ładowanych jest 50 elementów, ale programista może zmienić tę liczbę. Aby uzyskać więcej informacji, zobacz [Platforma mobilna](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-getting-started). Jeśli kategoria nie znajduje się na liście, wybierz pozycję **Wyszukaj**, aby dokonać wyszukiwania online. Wyszukaj według kategorii wydatków lub przejdź do wyszukiwania według typu wydatków.
11. Opcjonalnie: Wprowadź nazwę handlową dla wydatku.
12. Wprowadź datę transakcji wydatkowej.
13. Wprowadź pieniężną wartość wydatku.
14. Wybierz walutę i wydatek. Zobaczysz kody walut, które są ładowane do aplikacji do użytku w trybie offline. Domyślnie ładowanych jest 400 walut, ale programista może zmienić tę liczbę. Aby uzyskać więcej informacji, zobacz [Platforma mobilna](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-getting-started). Jeśli waluta nie znajduje się na liście, wybierz pozycję **Wyszukaj**, aby dokonać wyszukiwania online. Wyszukaj według waluty lub przejdź do wyszukiwania według nazwy.
15. Wybierz **Gotowe**.
16. Aby dodać więcej szczegółów do wydatku, wybierz pozycję **Dodaj więcej szczegółów**. Dostępne pola zależą od konfiguracji zarządzania wydatkami w firmie użytkownika.
17. Jeśli zasady firmy wymagają otrzymania paragonu na wydatek, wybierz pozycję **Paragony**, a następnie wykonaj następujące kroki:

    1. Wybierz polecenie **Zapisz paragon** lub **Dołącz paragon**.
    2. Wykonaj jedną z następujących czynności:

        - W przypadku wybrania **Zapisz paragon** należy:

            1. Wybierz opcję **Zrób zdjęcie** lub **Wybierz obraz**.
            2. Wykonaj jedną z następujących czynności:

                - W przypadku wybrania **Zrób zdjęcie** należy:

                    1. Otworzy się aparat urządzenia, aby można było zrobić zdjęcie paragonu. Po zakończeniu robienia zdjęcia kliknij przycisk **OK**, aby zaakceptować zdjęcie.
                    2. Opcjonalnie: Wprowadź nazwę zdjęcia i wprowadź wszelkie notatki.

                - W przypadku wybrania **Wybierz zdjęcie** należy:

                    1. Wybrać zdjęcie z listy.
                    2. Opcjonalnie: Wprowadź nazwę zdjęcia i wprowadź wszelkie notatki.

            3.  Wybierz **Gotowe**.

        - W przypadku wybrania **Dołącz paragon** należy:

            1.  Z listy wybrać jeden lub więcej obrazów.
            2.  Wybierz **Gotowe**.

    3. Wybierz przycisk **Wstecz**, aby powrócić do szczegółów wydatku.

18. Jeśli zasady firmy wymagają zaproszenia gościa w celu przetworzenia wydatku, wybierz pozycję **Goście**, a następnie wykonaj następujące kroki:

    1. Wybierz opcję **Gość**, **Poprzedni gość** lub **Współpracownik**.
    2. Wykonaj jedną z następujących czynności:

        - W przypadku wybrania **Gość** należy:

            1. Wprowadź imię i nazwisko gościa.
            2. Opcjonalnie: Wprowadź nazwę organizacji i/lub kraju gościa.
            3. Opcjonalnie: Wprowadź imię i nazwisko gościa.
            4. Wybierz **Gotowe**.

        - W przypadku wybrania **Poprzedni gość** należy:

            1. Z listy wybierz jednego lub więcej poprzednich gości. Zostanie wyświetlona lista poprzednich gości, których dodano do poprzednich raportów z wydatków załadowanych do aplikacji w celu korzystania z nich w trybie offline. Domyślnie ładowanych jest 50 elementów, ale programista może zmienić tę liczbę. Aby uzyskać więcej informacji, zobacz [Platforma mobilna](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-getting-started). Jeśli poprzedni gość nie znajduje się na liście, wybierz pozycję **Wyszukaj**, aby dokonać wyszukiwania online. Wyszukaj według nazwy lub przejdź do wyszukiwania według organizacji, kraju lub tytułu.
            2. Wybierz **Gotowe**.

        - W przypadku wybrania **Współpracownicy** należy:

            1. Z listy wybierz jednego lub większą liczbę współpracowników. Zobaczysz kategorie współpracowników, które są ładowane do aplikacji do użytku w trybie offline. Domyślnie ładowanych jest 50 elementów, ale programista może zmienić tę liczbę. Aby uzyskać więcej informacji, zobacz [Platforma mobilna](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-getting-started). Jeśli współpracownik nie znajduje się na liście, wybierz pozycję **Wyszukaj**, aby dokonać wyszukiwania online. Wyszukaj według nazwy lub przejdź do wyszukiwania według firmy lub tytułu.
            2. Wybierz **Gotowe**.

    3. Wybierz przycisk **Wstecz**, aby powrócić do szczegółów wydatku.

19. Jeśli zasady firmy wymagają utworzenia podzielonej listy wydatków, wybierz pozycję **Rozbij**, a następnie wykonaj następujące kroki:

    1. Wybierz pierwszą datę do podziału na pozycje.
    2. Wybierz pozycję **Dodaj podział na pozycje**.
    3. Wybierz podkategorię podziału na pozycje. Zobaczysz podkategorie wydatków, które są ładowane do aplikacji do użytku w trybie offline. Domyślnie ładowanych jest 50 elementów, ale programista może zmienić tę liczbę. Aby uzyskać więcej informacji, zobacz [Platforma mobilna](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-getting-started). Jeśli podkategoria nie znajduje się na liście, wybierz pozycję **Wyszukaj**, aby dokonać wyszukiwania online. Wyszukaj według nazwy podkategorii wydatku.
    4. Wprowadź kwotę transakcji do podziału na pozycje.
    5. Jeśli trzeba, zmień datę transakcji.
    6. Wybierz **Gotowe**.
    7. Powtarzaj powyższe kroki do momentu ukończenia dodawania wszystkich pozycji dla wybranej daty.
    8. W przypadku dodatkowych dni można wybrać **Skopiuj na następny dzień** w celu skopiowania podziału na elementy następnego dnia. Można też wybrać datę w polu rozbicia na elementy, a następnie dodać podział, tak jak miało to miejsce dla pierwszej daty.
    9. Po zakończeniu rozbijania elementów wydatków wybierz przycisk **Wstecz**, aby powrócić do szczegółów wydatku.

20. Wybierz przycisk **Wstecz**, aby powrócić do strony **Raportu z wydatków**.
21. Powtarzaj powyższe kroki do momentu ukończenia dodawania wszystkich kosztów.
22. Wybierz **Prześlij**.
23. Wprowadź komentarze dla osoby zatwierdzającej.
24. Wybierz **Gotowe**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]