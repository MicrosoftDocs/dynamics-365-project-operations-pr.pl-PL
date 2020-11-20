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
ms.openlocfilehash: 9e4e910d0ff0a5f2603148fcc5daa0d423a4d174
ms.sourcegitcommit: a9dbcd3aff4c6ae495412e4980e105ae160fd1ec
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 11/10/2020
ms.locfileid: "4483961"
---
# <a name="developer-notes-for-approvals"></a><span data-ttu-id="48990-103">Uwagi dotyczące deweloperów na temat zatwierdzeń</span><span class="sxs-lookup"><span data-stu-id="48990-103">Developer notes for Approvals</span></span>

<span data-ttu-id="48990-104">_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_</span><span class="sxs-lookup"><span data-stu-id="48990-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="48990-105">Dynamics 365 Project Operations zawiera logikę walidacji, która zapewnia prawidłowe przejście rekordów przez etapy zatwierdzania.</span><span class="sxs-lookup"><span data-stu-id="48990-105">Dynamics 365 Project Operations includes validation logic that ensures correct record transition through the approval stages.</span></span> <span data-ttu-id="48990-106">Poprawne przejścia między rekordami upewnij się, że:</span><span class="sxs-lookup"><span data-stu-id="48990-106">Correct record transitions ensure:</span></span> 

  - <span data-ttu-id="48990-107">Wszystkie wiersze obsługi są tworzone w tabelach pokrewnych, takich jak arkusze i wartości rzeczywiste.</span><span class="sxs-lookup"><span data-stu-id="48990-107">All supporting rows are created in related tables, such as journals and actuals.</span></span>
  - <span data-ttu-id="48990-108">Przed kontynuowaniem osoba zatwierdzająca jest oznaczona jako **Osoba zatwierdzająca projekt** w projekcie.</span><span class="sxs-lookup"><span data-stu-id="48990-108">The approver is marked as a **Project Approver** in the project before proceeding.</span></span>
