---
title: Vrijstellingsstatus taak
description: In dit onderwerp wordt de optieset voor Vrijstellingsstatus taak voor Dynamics 365 Human Resources beschreven.
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
ms.openlocfilehash: 8e91fbb420009d5131e2faa7dbea8a302a027e0a
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/18/2021
ms.locfileid: "6053846"
---
# <a name="job-exempt-status"></a><span data-ttu-id="3ae42-103">Vrijstellingsstatus taak</span><span class="sxs-lookup"><span data-stu-id="3ae42-103">Job exempt status</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="3ae42-104">In dit onderwerp wordt de optieset voor Vrijstellingsstatus taak voor Dynamics 365 Human Resources beschreven.</span><span class="sxs-lookup"><span data-stu-id="3ae42-104">This topic describes the Job exempt status option set for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="3ae42-105">Fysieke naam: cdm_jobexemptstatus</span><span class="sxs-lookup"><span data-stu-id="3ae42-105">Physical name: cdm_jobexemptstatus</span></span>

<span data-ttu-id="3ae42-106">Deze opsomming specificeert de optieset voor de waarden voor FLSA-vrijstellingsstatussen voor taken.</span><span class="sxs-lookup"><span data-stu-id="3ae42-106">This enumeration specifies the option set for FLSA job exempt status values.</span></span> <span data-ttu-id="3ae42-107">Dit wordt opgegeven in de bestaande optieset voor cdm_jobexemptstatus.</span><span class="sxs-lookup"><span data-stu-id="3ae42-107">This is provided in the existing cdm_jobexemptstatus option set.</span></span>

| <span data-ttu-id="3ae42-108">Waarde</span><span class="sxs-lookup"><span data-stu-id="3ae42-108">Value</span></span> | <span data-ttu-id="3ae42-109">Etiket</span><span class="sxs-lookup"><span data-stu-id="3ae42-109">Label</span></span> | <span data-ttu-id="3ae42-110">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="3ae42-110">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="3ae42-111">200000000</span><span class="sxs-lookup"><span data-stu-id="3ae42-111">200000000</span></span> | <span data-ttu-id="3ae42-112">Vrijstelling</span><span class="sxs-lookup"><span data-stu-id="3ae42-112">Exempt</span></span> | <span data-ttu-id="3ae42-113">De taak heeft een vrijstellingsstatus op basis van de FLSA-richtlijnen.</span><span class="sxs-lookup"><span data-stu-id="3ae42-113">The job has an exempt status based on FLSA guidelines.</span></span> |
| <span data-ttu-id="3ae42-114">200000001</span><span class="sxs-lookup"><span data-stu-id="3ae42-114">200000001</span></span> | <span data-ttu-id="3ae42-115">Geen vrijstelling</span><span class="sxs-lookup"><span data-stu-id="3ae42-115">NonExempt</span></span> | <span data-ttu-id="3ae42-116">De taak heeft de status Geen vrijstelling op basis van de FLSA-richtlijnen.</span><span class="sxs-lookup"><span data-stu-id="3ae42-116">The job has a non-exempt status based on FLSA guidelines.</span></span> |
| <span data-ttu-id="3ae42-117">200000002</span><span class="sxs-lookup"><span data-stu-id="3ae42-117">200000002</span></span> | <span data-ttu-id="3ae42-118">Niet van toepassing</span><span class="sxs-lookup"><span data-stu-id="3ae42-118">Does Not Apply</span></span> | <span data-ttu-id="3ae42-119">De richtlijnen voor de FLSA-status zijn niet van toepassing op de taak.</span><span class="sxs-lookup"><span data-stu-id="3ae42-119">FLSA status guidelines do not apply to the job.</span></span> |

## <a name="see-also"></a><span data-ttu-id="3ae42-120">Zie ook</span><span class="sxs-lookup"><span data-stu-id="3ae42-120">See also</span></span>

[<span data-ttu-id="3ae42-121">Integratie-API voor sollicitantenvolgsysteem - Inleiding</span><span class="sxs-lookup"><span data-stu-id="3ae42-121">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="3ae42-122">Voorbeeldquery voor wervingsaanvraag</span><span class="sxs-lookup"><span data-stu-id="3ae42-122">Example query for Recruiting request</span></span>](hr-admin-integration-ats-api-recruiting-request-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]