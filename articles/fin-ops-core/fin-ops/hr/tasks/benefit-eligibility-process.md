---
title: Proces voor geschiktheid voor vergoeding
description: Deze procedure toont hoe het geschiktheidsproces voor vergoedingen werkt.
author: andreabichsel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysPolicySourceDocumentRuleType, SysPolicyListPage, SysPolicy, HcmBenefitEligibilityPolicy, HcmBenefit
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b842d76d2c02b7f5daa45c5a34c8f61029f6c035
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/27/2019
ms.locfileid: "2177274"
---
# <a name="benefit-eligibility-process"></a><span data-ttu-id="fea1b-103">Proces voor geschiktheid voor vergoeding</span><span class="sxs-lookup"><span data-stu-id="fea1b-103">Benefit eligibility process</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="fea1b-104">Deze procedure toont hoe het geschiktheidsproces voor vergoedingen werkt.</span><span class="sxs-lookup"><span data-stu-id="fea1b-104">This procedure shows how the benefit eligibility process works.</span></span> <span data-ttu-id="fea1b-105">U kunt de resultaten bekijken zodra het proces is voltooid.</span><span class="sxs-lookup"><span data-stu-id="fea1b-105">When the process is complete you can view the results.</span></span> <span data-ttu-id="fea1b-106">Het bedrijf van de demogegevens dat wordt gebruikt om deze procedure te maken is USMF.</span><span class="sxs-lookup"><span data-stu-id="fea1b-106">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="fea1b-107">Ga naar Human resources > Vergoedingen > Vergoedingen.</span><span class="sxs-lookup"><span data-stu-id="fea1b-107">Go to Human resources > Benefits > Benefits.</span></span>
2. <span data-ttu-id="fea1b-108">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="fea1b-108">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="fea1b-109">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="fea1b-109">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="fea1b-110">Klik op Bewerken.</span><span class="sxs-lookup"><span data-stu-id="fea1b-110">Click Edit.</span></span>
5. <span data-ttu-id="fea1b-111">Selecteer in het veld Geschiktheid de optie 'Op basis van regels'.</span><span class="sxs-lookup"><span data-stu-id="fea1b-111">In the Eligibility field, select 'Rule based'.</span></span>
6. <span data-ttu-id="fea1b-112">Selecteer in het veld Regeltype de vergoedingsbeleidsregel die u op de vergoeding wilt toepassen.</span><span class="sxs-lookup"><span data-stu-id="fea1b-112">In the Rule type field, select the benefit policy rule you would like applied to the benefit.</span></span>
7. <span data-ttu-id="fea1b-113">Klik in het actievenster op Vergoeding.</span><span class="sxs-lookup"><span data-stu-id="fea1b-113">On the Action Pane, click Benefit.</span></span>
8. <span data-ttu-id="fea1b-114">Klik op Geschiktheidsgebeurtenis maken om het dialoogvenster voor beëindigen te openen.</span><span class="sxs-lookup"><span data-stu-id="fea1b-114">Click Create eligibility event to open the drop dialog.</span></span>
9. <span data-ttu-id="fea1b-115">Typ een waarde in het veld Gebeurtenis.</span><span class="sxs-lookup"><span data-stu-id="fea1b-115">In the Event field, type a value.</span></span>
10. <span data-ttu-id="fea1b-116">Typ een waarde in het veld Omschrijving.</span><span class="sxs-lookup"><span data-stu-id="fea1b-116">In the Description field, type a value.</span></span>
11. <span data-ttu-id="fea1b-117">Selecteer 'Inschrijving openen' in het veld Gebeurtenistype.</span><span class="sxs-lookup"><span data-stu-id="fea1b-117">In the Event type field, select 'Open enrollment'.</span></span>
12. <span data-ttu-id="fea1b-118">Typ een datum en tijd in het veld Begindatum dekking.</span><span class="sxs-lookup"><span data-stu-id="fea1b-118">In the Coverage start date field, enter a date and time.</span></span>
13. <span data-ttu-id="fea1b-119">Typ een datum en een tijd in het veld Begindatum inschrijvingsperiode.</span><span class="sxs-lookup"><span data-stu-id="fea1b-119">In the Enrollment period start date field, enter a date and time.</span></span>
14. <span data-ttu-id="fea1b-120">Typ een nummer in het veld Dagen om in te schrijven.</span><span class="sxs-lookup"><span data-stu-id="fea1b-120">In the Days to enroll field, enter a number.</span></span>
15. <span data-ttu-id="fea1b-121">Klik op Gebeurtenis maken.</span><span class="sxs-lookup"><span data-stu-id="fea1b-121">Click Create event.</span></span>
16. <span data-ttu-id="fea1b-122">Klik op Toevoegen aan het sneltabblad Medewerkers.</span><span class="sxs-lookup"><span data-stu-id="fea1b-122">Click Add in the Workers FastTab.</span></span>
17. <span data-ttu-id="fea1b-123">Selecteer 'Werknemers' in het veld Weergeven per type.</span><span class="sxs-lookup"><span data-stu-id="fea1b-123">In the Show by type field, select 'Employees'.</span></span>
18. <span data-ttu-id="fea1b-124">Selecteer 'Huidige rechtspersoon' in het veld Weergeven per rechtspersoon.</span><span class="sxs-lookup"><span data-stu-id="fea1b-124">In the Show by legal entity field, select 'Current legal entity'.</span></span>
19. <span data-ttu-id="fea1b-125">Selecteer of deselecteer alle rijen in de lijst.</span><span class="sxs-lookup"><span data-stu-id="fea1b-125">In the list, mark or unmark all rows.</span></span>
20. <span data-ttu-id="fea1b-126">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="fea1b-126">Click OK.</span></span>
21. <span data-ttu-id="fea1b-127">Klik op Verwerken.</span><span class="sxs-lookup"><span data-stu-id="fea1b-127">Click Process.</span></span>
22. <span data-ttu-id="fea1b-128">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="fea1b-128">Click OK.</span></span>
23. <span data-ttu-id="fea1b-129">Vernieuw de pagina.</span><span class="sxs-lookup"><span data-stu-id="fea1b-129">Refresh the page.</span></span>
24. <span data-ttu-id="fea1b-130">Klik op Resultaten weergeven.</span><span class="sxs-lookup"><span data-stu-id="fea1b-130">Click Show results.</span></span>
25. <span data-ttu-id="fea1b-131">Open kolomfilter Status.</span><span class="sxs-lookup"><span data-stu-id="fea1b-131">Open Status column filter.</span></span>
26. <span data-ttu-id="fea1b-132">Sorteren van A naar Z</span><span class="sxs-lookup"><span data-stu-id="fea1b-132">Sort A to Z</span></span>

