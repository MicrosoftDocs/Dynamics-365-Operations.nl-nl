---
title: Positiestatus voor wervingsaanvragen
description: In dit onderwerp wordt de optieset voor Positiestatus voor wervingsaanvragen voor Dynamics 365 Human Resources beschreven.
author: jaredha
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: e287ec4b9b78194b76ef3c993c6ce32f808e26f9
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/18/2021
ms.locfileid: "6051876"
---
# <a name="recruiting-request-position-status"></a><span data-ttu-id="52e06-103">Positiestatus voor wervingsaanvragen</span><span class="sxs-lookup"><span data-stu-id="52e06-103">Recruiting request position status</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="52e06-104">In dit onderwerp wordt de optieset voor Positiestatus voor wervingsaanvragen voor Dynamics 365 Human Resources beschreven.</span><span class="sxs-lookup"><span data-stu-id="52e06-104">This topic describes the Recruiting request position status option set for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="52e06-105">Fysieke naam: mshr_hcmrecruitingrequestpositionstatus</span><span class="sxs-lookup"><span data-stu-id="52e06-105">Physical name: mshr_hcmrecruitingrequestpositionstatus</span></span>

<span data-ttu-id="52e06-106">Deze opsomming bevat de optieset voor de statuswaarden van elke positie een wervingsaanvraag in de entiteit Positie van wervingsaanvraag.</span><span class="sxs-lookup"><span data-stu-id="52e06-106">This enumeration provides the option set for the status values of each position a recruiting request in the RecruitingRequestPosition entity.</span></span>

| <span data-ttu-id="52e06-107">Waarde</span><span class="sxs-lookup"><span data-stu-id="52e06-107">Value</span></span> | <span data-ttu-id="52e06-108">Etiket</span><span class="sxs-lookup"><span data-stu-id="52e06-108">Label</span></span> | <span data-ttu-id="52e06-109">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="52e06-109">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="52e06-110">200000000</span><span class="sxs-lookup"><span data-stu-id="52e06-110">200000000</span></span> | <span data-ttu-id="52e06-111">Openstaande</span><span class="sxs-lookup"><span data-stu-id="52e06-111">Open</span></span> | <span data-ttu-id="52e06-112">De positie in de wervingsaanvraag is open voor werving.</span><span class="sxs-lookup"><span data-stu-id="52e06-112">The position in the recruiting request is open for recruiting.</span></span> <span data-ttu-id="52e06-113">Dit geeft niet aan dat er momenteel geen actieve positietoewijzing voor de positie bestaat.</span><span class="sxs-lookup"><span data-stu-id="52e06-113">This does not indicate that there is no currently active position assignment for the position.</span></span> <span data-ttu-id="52e06-114">Op het moment van werving kan er een werknemer in de positie zijn.</span><span class="sxs-lookup"><span data-stu-id="52e06-114">There may be an employee in the position at the time of recruiting.</span></span> <span data-ttu-id="52e06-115">Dit geeft alleen aan dat de positie beschikbaar is voor werving in de context van de wervingsaanvraag.</span><span class="sxs-lookup"><span data-stu-id="52e06-115">It indicates only that the position is available for recruiting in the context of the recruiting request.</span></span> |
| <span data-ttu-id="52e06-116">200000001</span><span class="sxs-lookup"><span data-stu-id="52e06-116">200000001</span></span> | <span data-ttu-id="52e06-117">Ingevuld</span><span class="sxs-lookup"><span data-stu-id="52e06-117">Filled</span></span> | <span data-ttu-id="52e06-118">Er is een werknemer geselecteerd voor toewijzing aan de positie.</span><span class="sxs-lookup"><span data-stu-id="52e06-118">A worker has been selected for assignment to the position.</span></span> |
| <span data-ttu-id="52e06-119">200000002</span><span class="sxs-lookup"><span data-stu-id="52e06-119">200000002</span></span> | <span data-ttu-id="52e06-120">Geannuleerd</span><span class="sxs-lookup"><span data-stu-id="52e06-120">Canceled</span></span> | <span data-ttu-id="52e06-121">De aanvraag om personeel voor deze positie te werven is geannuleerd.</span><span class="sxs-lookup"><span data-stu-id="52e06-121">The request to recruit for this position has been canceled.</span></span> |

## <a name="see-also"></a><span data-ttu-id="52e06-122">Zie ook</span><span class="sxs-lookup"><span data-stu-id="52e06-122">See also</span></span>

[<span data-ttu-id="52e06-123">Integratie-API voor sollicitantenvolgsysteem - Inleiding</span><span class="sxs-lookup"><span data-stu-id="52e06-123">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="52e06-124">Voorbeeldquery voor wervingsaanvraag</span><span class="sxs-lookup"><span data-stu-id="52e06-124">Example query for Recruiting request</span></span>](hr-admin-integration-ats-api-recruiting-request-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]