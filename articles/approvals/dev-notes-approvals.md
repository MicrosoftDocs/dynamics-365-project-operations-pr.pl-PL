---
title: Uwagi dotyczące deweloperów na temat zatwierdzeń
description: Ta temat zawiera dodatkowe informacje dla deweloperów, na temat pracy z zatwierdzaniem.
author: stsporen
manager: Annbe
ms.date: 11/09/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: d58c776b0341c08b0292e1b459a7d7ebac550bcc
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5290282"
---
# <a name="developer-notes-for-approvals"></a><span data-ttu-id="31111-103">Uwagi dotyczące deweloperów na temat zatwierdzeń</span><span class="sxs-lookup"><span data-stu-id="31111-103">Developer notes for Approvals</span></span>

<span data-ttu-id="31111-104">_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_</span><span class="sxs-lookup"><span data-stu-id="31111-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="31111-105">Rozwiązaniu Dynamics 365 Project Operations zawiera logikę walidacji, która zapewnia prawidłowe przejście rekordów przez etapy zatwierdzania.</span><span class="sxs-lookup"><span data-stu-id="31111-105">Dynamics 365 Project Operations includes validation logic that ensures correct record transition through the approval stages.</span></span> <span data-ttu-id="31111-106">Poprawne przejścia między rekordami upewnij się, że:</span><span class="sxs-lookup"><span data-stu-id="31111-106">Correct record transitions ensure:</span></span> 

  - <span data-ttu-id="31111-107">Wszystkie wiersze obsługi są tworzone w tabelach pokrewnych, takich jak arkusze i wartości rzeczywiste.</span><span class="sxs-lookup"><span data-stu-id="31111-107">All supporting rows are created in related tables, such as journals and actuals.</span></span>
  - <span data-ttu-id="31111-108">Przed kontynuowaniem osoba zatwierdzająca jest oznaczona jako **Osoba zatwierdzająca projekt** w projekcie.</span><span class="sxs-lookup"><span data-stu-id="31111-108">The approver is marked as a **Project Approver** in the project before proceeding.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]