---
title: Positiestatus voor wervingsaanvragen
description: In dit onderwerp wordt de optieset voor Positiestatus voor wervingsaanvragen voor Dynamics 365 Human Resources beschreven.
author: jaredha
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 7e59e9381fb15b339095d6a71296813e0141e9ab
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/31/2021
ms.locfileid: "5789727"
---
# <a name="recruiting-request-position-status"></a><span data-ttu-id="0232c-103">Positiestatus voor wervingsaanvragen</span><span class="sxs-lookup"><span data-stu-id="0232c-103">Recruiting request position status</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="0232c-104">In dit onderwerp wordt de optieset voor Positiestatus voor wervingsaanvragen voor Dynamics 365 Human Resources beschreven.</span><span class="sxs-lookup"><span data-stu-id="0232c-104">This topic describes the Recruiting request position status option set for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="0232c-105">Fysieke naam: mshr_hcmrecruitingrequestpositionstatus</span><span class="sxs-lookup"><span data-stu-id="0232c-105">Physical name: mshr_hcmrecruitingrequestpositionstatus</span></span>

<span data-ttu-id="0232c-106">Deze opsomming bevat de optieset voor de statuswaarden van elke positie een wervingsaanvraag in de entiteit Positie van wervingsaanvraag.</span><span class="sxs-lookup"><span data-stu-id="0232c-106">This enumeration provides the option set for the status values of each position a recruiting request in the RecruitingRequestPosition entity.</span></span>

| <span data-ttu-id="0232c-107">Waarde</span><span class="sxs-lookup"><span data-stu-id="0232c-107">Value</span></span> | <span data-ttu-id="0232c-108">Etiket</span><span class="sxs-lookup"><span data-stu-id="0232c-108">Label</span></span> | <span data-ttu-id="0232c-109">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="0232c-109">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="0232c-110">200000000</span><span class="sxs-lookup"><span data-stu-id="0232c-110">200000000</span></span> | <span data-ttu-id="0232c-111">Openstaande</span><span class="sxs-lookup"><span data-stu-id="0232c-111">Open</span></span> | <span data-ttu-id="0232c-112">De positie in de wervingsaanvraag is open voor werving.</span><span class="sxs-lookup"><span data-stu-id="0232c-112">The position in the recruiting request is open for recruiting.</span></span> <span data-ttu-id="0232c-113">Dit geeft niet aan dat er momenteel geen actieve positietoewijzing voor de positie bestaat.</span><span class="sxs-lookup"><span data-stu-id="0232c-113">This does not indicate that there is no currently active position assignment for the position.</span></span> <span data-ttu-id="0232c-114">Op het moment van werving kan er een werknemer in de positie zijn.</span><span class="sxs-lookup"><span data-stu-id="0232c-114">There may be an employee in the position at the time of recruiting.</span></span> <span data-ttu-id="0232c-115">Dit geeft alleen aan dat de positie beschikbaar is voor werving in de context van de wervingsaanvraag.</span><span class="sxs-lookup"><span data-stu-id="0232c-115">It indicates only that the position is available for recruiting in the context of the recruiting request.</span></span> |
| <span data-ttu-id="0232c-116">200000001</span><span class="sxs-lookup"><span data-stu-id="0232c-116">200000001</span></span> | <span data-ttu-id="0232c-117">Ingevuld</span><span class="sxs-lookup"><span data-stu-id="0232c-117">Filled</span></span> | <span data-ttu-id="0232c-118">Er is een werknemer geselecteerd voor toewijzing aan de positie.</span><span class="sxs-lookup"><span data-stu-id="0232c-118">A worker has been selected for assignment to the position.</span></span> |
| <span data-ttu-id="0232c-119">200000002</span><span class="sxs-lookup"><span data-stu-id="0232c-119">200000002</span></span> | <span data-ttu-id="0232c-120">Geannuleerd</span><span class="sxs-lookup"><span data-stu-id="0232c-120">Canceled</span></span> | <span data-ttu-id="0232c-121">De aanvraag om personeel voor deze positie te werven is geannuleerd.</span><span class="sxs-lookup"><span data-stu-id="0232c-121">The request to recruit for this position has been canceled.</span></span> |

## <a name="see-also"></a><span data-ttu-id="0232c-122">Zie ook</span><span class="sxs-lookup"><span data-stu-id="0232c-122">See also</span></span>

[<span data-ttu-id="0232c-123">Integratie-API voor sollicitantenvolgsysteem - Inleiding</span><span class="sxs-lookup"><span data-stu-id="0232c-123">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="0232c-124">Voorbeeldquery voor wervingsaanvraag</span><span class="sxs-lookup"><span data-stu-id="0232c-124">Example query for Recruiting request</span></span>](hr-admin-integration-ats-api-recruiting-request-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]