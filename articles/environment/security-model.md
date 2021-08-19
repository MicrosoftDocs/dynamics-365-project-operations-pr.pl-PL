---
title: Model zabezpieczeń
description: Ta temat zawiera informacje o modelu zabezpieczeń w aplikacji Dynamics 365 Project Operations.
author: stsporen
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 2f283771921504dc29ddcc26ca659d4e151598840339bd8c1a857e8bf5dde9ed
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/06/2021
ms.locfileid: "6991499"
---
# <a name="security-model"></a>Model zabezpieczeń

_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Aplikacja Microsoft Dynamics 365 Project Operations zawiera unikatowy model zabezpieczeń, który umożliwia współpracę modelu zabezpieczeń opartego na rolach z grupami pakietu Microsoft Office. 


## <a name="security-roles"></a>Role zabezpieczeń
Funkcje front-end w Project Operations są następujące:

| Rola                          | Opis                                                                                                                                                                 | Scope |
|-------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------|
| Menedżer praktyk              | Obsługuje raportowanie pomiędzy projektami.                                                                                                            | Jednostka biznesowa              |
| Osoba zatwierdzająca w projekcie              | Zatwierdza czas i wydatki w projekcie.                                                                                                                              | Jednostka biznesowa |
| Administrator fakturowania w projekcie | Tworzy propozycje faktury.                                                                                                                                                 | Jednostka biznesowa |
| Menedżer projektu               | Tworzy plan projektu i żądania zasobów.                                                                                                                              | Jednostka biznesowa |
| Zasób projektu              | Członkowie zespołu, którzy mogą być rezerwowani i raportować czas.                                                                                                          | Jednostka biznesowa|
| Menedżer zasobów              | Wszystkie funkcje zarządzania zasobami, takie jak realizację żądań zasobów i rezerwacje, rozdzielone na potrzeby obsługi hybrydowej konfiguracji menedżera projektu + menedżera zasobów oraz jednej i scentralizowanej roli menedżera zasobów. | Jednostka biznesowa |


Program Microsoft Project dla sieci Web zawiera następujące role:

| Rola           | Opis                                                                                                        | Scope  |
|----------------|--------------------------------------------------------------------------------------------------------------------|--------|
| Użytkownik projektu   | Użytkownik będący częścią zespołu projektu, który może tworzyć własne projekty i wyświetlać wszystkie udostępnione mu projekty. | Użytkownik   |
| System projektów | Rola używana w kontekście aplikacji. Klienci nie powinni używać tej roli systemowej.                                    | Globalne |

## <a name="security-enforcement"></a>Egzekwowanie zabezpieczeń
Akcje wykonywane na poziomie projektu są wykonywane w kontekście zalogowanego użytkownika. Oznacza to, że w celu tworzenia, otwierania i usuwania projektu użytkownik musi mieć dostęp do programu, który jest dostępny w CDS. Dostęp w CDS może być przyznany za pośrednictwem dowolnego z możliwych mechanizmów zawartych w platformie. Na przykład użytkownik z większym zakresem może mieć dostęp do projektu lub też została wykonana jawna akcja udzielenia projektu, która daje użytkownikowi dostęp do programu.

Należy o tym pamiętać podczas tworzenia projektów w Project Operations.

## <a name="modern-group-collaboration-with-project-operations"></a>Nowoczesna grupowa współpraca w Project Operations
Projekty dla sieci Web i Project Operations obsługują nowoczesne grupy w ramach współpracy. Użytkownicy dodani do projektu za pośrednictwem grupy mogą edytować plan projektu.

W projekcie sieci Web użytkownicy automatycznie są dodawani do grupy po przypisaniu.

Grupy umożliwiają wspólną pracę nad uprawieniami w ramach projektu i artefaktami obsługującymi współpracę. Na poniższym diagramie przedstawiono zmiany dotyczące zdarzeń i stanu, jakie nastąpią w trakcie procesu przypisywania grupy.

Project Operations nie tworzy grupy niejawną operacją i działa wyłącznie w ramach wyraźnego działania w grupach.

Wyszukiwanie członka grupy w oknie dialogowym **Zarządzanie grupami** jest ograniczone do użytkowników, którzy są ustawiani jako część grupy zabezpieczeń środowiska. Aby uzyskać więcej informacji, zobacz [Kontrolowanie dostępu użytkowników do środowisk: grupy zabezpieczeń i licencje](/power-platform/admin/control-user-access).

![Tryb Grupowy.](./media/groupsmode.png)

1. Właścicielem projektu jest użytkownik tworzący i należący do niego.
2. Właściciel projektu zostanie przypisany do zespołu.
3. Zespół właściciela jest zamapowany do określonej lub utworzoną grupy Office.
4. Pierwotny właściciel projektu jest dodawany do grupy Office.

## <a name="deployment-recommendation"></a>Rekomendacja wdrażania
W miarę rozwoju modelu współdziałania w grupie Office, dodawana jest funkcja zapewniająca dokładniejszą kontrolę czasu. Klienci wdrażający dzisiaj Project Operations są zachęcani do korzystania z tradycyjnych modeli zabezpieczeń Microsoft Dynamics 365.

Aby uzyskać więcej informacji o zabezpieczeniach, zobacz: [Zabezpieczenia w Common Data Service](/power-platform/admin/wp-security).

## <a name="project-operations-and-microsoft-dynamics-365-finance-security"></a>Project Operations i zabezpieczenia Microsoft Dynamics 365 Finance
Project Operations zawiera następujące role:

- Menedżer projektu
- Księgowy projektu

Aby uzyskać więcej informacji na temat zabezpieczeń w Finance, zobacz temat [zabezpieczenia oparte na rolach](/dynamics365/fin-ops-core/dev-itpro/sysadmin/role-based-security).




[!INCLUDE[footer-include](../includes/footer-banner.md)]