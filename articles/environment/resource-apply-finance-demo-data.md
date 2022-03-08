---
title: Stosowanie danych demonstracyjnych do środowiska hostowanego w chmurze rozwiązania Finance
description: W tym temacie wyjaśniono, jak stosować dane demonstracyjne pochodzące z Project Operations w środowisku w chmurze Dynamics 365 Finance.
author: sigitac
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: c04aab6ffb332a3095ca2a7890deb73f15a8b5e3713021c60eec02eb13dbd0cb
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/06/2021
ms.locfileid: "7009679"
---
# <a name="apply-demo-data-to-a-finance-cloud-hosted-environment"></a>Stosowanie danych demonstracyjnych do środowiska hostowanego w chmurze rozwiązania Finance

_**Zastosowane do:** Project Operations dla zasobów/scenariuszy nieopartych na zaopatrzeniu_

> [!IMPORTANT]
> Ten temat ma zastosowanie tylko do Microsoft Dynamics 365 Finance w wersji 10.0.13 i dotyczy tylko środowiska hostowanego w chmurze. Wykonaj czynności opisane w tym temacie **PRZED** zastosowaniem aktualizacji dotyczących jakości w środowisku.

1. W projekcie LCS otwórz stronę **Szczegóły środowiska**. Należy zwrócić uwagę, że informacje wymagane do łączenia się ze środowiskiem za pomocą protokołu RDP (Remote Desktop Protocol) są także zawarte.

![Szczegóły środowiska.](./media/1EnvironmentDetails.png)

Pierwszy zestaw podświetlonych poświadczeń to lokalne poświadczenia konta, które zawierają hiperłącza do podłączania pulpitu zdalnego. Poświadczenia zawierają nazwę użytkownika i hasło administratora środowiska. Drugi zestaw poświadczeń jest używany do logowania się w programie SQL Server w tym środowisku.

2. Połącz się z środowiskiem za pomocą hiperłącza znajdującego się w sekcji **Konta lokalne** i użyj **poświadczeń konta lokalnego** do uwierzytelnienia.
3. Wybierz pozycję **Internet Information Services (IIS)** > **Pule aplikacji** > **AOSService** i zatrzymaj usługę. Zatrzymujesz usługę w tym punkcie, aby móc zastępować bazę danych SQL.

![Zatrzymaj AOS.](./media/2StopAOS.png)

4. Przejdź do sekcji **Usługi** i zatrzymaj następujące dwa elementy:

- Microsoft Dynamics 365 Unified Operations: Batch Management Service
- Microsoft Dynamics 365 Unified Operations: Data Import Export Framework

![Zatrzymaj usługi.](./media/3StopServices.png)

5. Otwórz Microsoft SQL Server Management Studio. Zaloguj się przy użyciu poświadczeń programu SQL Server i użyj konta axdbadmin i hasła ze strony **Szczegóły środowiska** LCS.

![SQL Server Management Studio.](./media/4SSMS.png)

6. W przypadku korzystania z Eksploratora obiektów, **Bazy danych** i zlokalizuj **AXDB**. Baza danych zostanie zamieniona na nową, która znajduje się w [Centrum pobierania](https://download.microsoft.com/download/1/a/3/1a314bd2-b082-4a87-abdc-1ba26c92b63d/ProjOpsDemoDataFOGARelease.zip). 
7. Skopiuj plik zip na maszynę wirtualną, która jest zdalnie przydzielone do programu, a następnie wyodrębnij zawartość zip.
8. W programie SQL Server Management Studio kliknij prawym przyciskiem myszy opcję **AxDB**, a następnie wybierz kolejno pozycje **Zadania** > **Przywracanie** > **Bazy danych**.

![Przywróć bazę danych.](./media/5RestoreDatabase.png)

9. Wybierz **Urządzenie źródłowe** i przejdź do pliku wyodrębnionego z kodu zip, który został skopiowany.

![Urządzenia źródłowe.](./media/6SourceDevice.png)

10. Wybierz **Opcje**, a następnie wybierz opcję **Zastąp istniejącą bazę danych** i **Zamknij istniejące połączenia z docelową bazą danych**. 
11. Wybierz pozycję **OK**.

![Przywracanie ustawień.](./media/7RestoreSetting.png)

Otrzymasz potwierdzenie, że przywracanie AXDB zakończyło się sukcesem. Po otrzymaniu tego potwierdzenia można zamknąć program SQL Services Management Studio.

12. Wybierz ponownie pozycję **Internet Information Services (IIS)** > **Pule aplikacji** > **AOSService** i uruchom AOSService.
13. Wybierz kolejno pozycje **Usługi** i uruchom dwie usługi, które zatrzymałeś wcześniej.

14. Znajdź narzędzie AdminUserProvisioning na tej maszynie wirtualnej. Szukaj w K:\AosService\PackagesLocalDirectory\bin\AdminUserProvisioning.exe.
15. Uruchom plik .ext, korzystając z adresu użytkownika w polu **adresu e-mail**. 
16. Wybierz **Prześlij**.

![Inicjowanie obsługi administratora.](./media/8AdminUserProvisioning.png)

Wykonanie tej czynności może potrwać do kilku minut. Powinien zostać wyświetlony komunikat z potwierdzeniem, że użytkownik administrator został pomyślnie zaktualizowany.

17. Na koniec należy uruchomić wiersz polecenia jako administrator i wykonać polecenie iisreset

![Reset usługi IIS.](./media/9IISReset.png)

18. Zamknij sesję pulpitu zdalnego i na stronie **Szczegóły środowiska** LCS zaloguj się w celu potwierdzenia, że wszystko działa zgodnie z oczekiwaniami.

![Finance and Operations.](./media/10FinanceAndOperations.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]