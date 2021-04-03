---
title: Een workflow voor verlofaanvragen maken
description: Maak een workflow voor verlof- en verzuimaanvragen om verlofaanvragen op consistente wijze te beheren in Dynamics 365 Human Resources.
author: andreabichsel
manager: tfehr
ms.date: 05/08/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: c2c2020c68c4aca3594a2532d32f968ab76f6b7b
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/17/2021
ms.locfileid: "5463305"
---
# <a name="create-a-leave-request-workflow"></a><span data-ttu-id="d54e6-103">Een workflow voor verlofaanvragen maken</span><span class="sxs-lookup"><span data-stu-id="d54e6-103">Create a leave request workflow</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="d54e6-104">U kunt een workflow maken in Dynamics 365 Human Resources voor het op consistente wijze beheren van uw verlof- en verzuimaanvragen.</span><span class="sxs-lookup"><span data-stu-id="d54e6-104">You can create a workflow in Dynamics 365 Human Resources to consistently manage your leave and absence requests.</span></span> <span data-ttu-id="d54e6-105">Met een workflow voor **Verlof en verzuim** kunt u:</span><span class="sxs-lookup"><span data-stu-id="d54e6-105">A **Leave and absence** workflow lets you:</span></span>

- <span data-ttu-id="d54e6-106">Taken definiëren</span><span class="sxs-lookup"><span data-stu-id="d54e6-106">Define tasks</span></span>
- <span data-ttu-id="d54e6-107">Bepalen wie de taken moet voltooien</span><span class="sxs-lookup"><span data-stu-id="d54e6-107">Determine who must complete the tasks</span></span>
- <span data-ttu-id="d54e6-108">Opgeven wie aanvragen kan goedkeuren of afwijzen</span><span class="sxs-lookup"><span data-stu-id="d54e6-108">Specify who can approve or reject requests</span></span>

## <a name="create-a-leave-and-absence-request-workflow"></a><span data-ttu-id="d54e6-109">Een workflow voor verlof- en verzuimaanvragen maken</span><span class="sxs-lookup"><span data-stu-id="d54e6-109">Create a Leave and absence request workflow</span></span>

1. <span data-ttu-id="d54e6-110">Selecteer op de pagina **Verlof en verzuim** het tabblad **Koppelingen**.</span><span class="sxs-lookup"><span data-stu-id="d54e6-110">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="d54e6-111">Selecteer onder **Instellen** de optie **Workflows voor Human resources**.</span><span class="sxs-lookup"><span data-stu-id="d54e6-111">Under **Setup**, select **Human resource workflows**.</span></span>

3. <span data-ttu-id="d54e6-112">Selecteer **Nieuw** en selecteer vervolgens **Verlof- en verzuimaanvraag**.</span><span class="sxs-lookup"><span data-stu-id="d54e6-112">Select **New**, and then select **Leave and absence request**.</span></span> 

4. <span data-ttu-id="d54e6-113">Wanneer het berichtvenster **Dit bestand openen?** verschijnt, selecteert u **Openen** en meldt u zich aan en met uw bedrijfsreferenties.</span><span class="sxs-lookup"><span data-stu-id="d54e6-113">When the **Open this file?** message box appears, select **Open** and sign in with your company credentials.</span></span>

5. <span data-ttu-id="d54e6-114">Gebruik de workflow-editor om een workflow voor uw verlofaanvragen te maken.</span><span class="sxs-lookup"><span data-stu-id="d54e6-114">Use the workflow editor to create a workflow for your leave requests.</span></span> <span data-ttu-id="d54e6-115">Zie [Overzicht van workflows maken](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/create-workflow?toc=/dynamics365/commerce/toc.json.) voor meer informatie over het werken met workflows.</span><span class="sxs-lookup"><span data-stu-id="d54e6-115">For more information about working with workflows, see [Create workflows overview](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/create-workflow?toc=/dynamics365/commerce/toc.json.)</span></span>

## <a name="leave-and-absence-request-workflow-data-elements"></a><span data-ttu-id="d54e6-116">Gegevenselementen van workflow voor verlof- en verzuimaanvragen</span><span class="sxs-lookup"><span data-stu-id="d54e6-116">Leave and absence request workflow data elements</span></span>

<span data-ttu-id="d54e6-117">U kunt de volgende gegevenselementen gebruiken om voorwaardelijke of automatische goedkeuringen te maken in workflows voor verlof- en verzuimaanvragen:</span><span class="sxs-lookup"><span data-stu-id="d54e6-117">You can use the following data elements to create conditional or automatic approvals in workflows for leave and absence requests:</span></span>

- <span data-ttu-id="d54e6-118">**Bedrag**</span><span class="sxs-lookup"><span data-stu-id="d54e6-118">**Amount**</span></span>
- <span data-ttu-id="d54e6-119">**Opmerking**</span><span class="sxs-lookup"><span data-stu-id="d54e6-119">**Comment**</span></span>
- <span data-ttu-id="d54e6-120">**Bedrijf**</span><span class="sxs-lookup"><span data-stu-id="d54e6-120">**Company**</span></span>
- <span data-ttu-id="d54e6-121">**Gemaakt door**</span><span class="sxs-lookup"><span data-stu-id="d54e6-121">**Created by**</span></span>
- <span data-ttu-id="d54e6-122">**Aanmaakdatum en -tijd**</span><span class="sxs-lookup"><span data-stu-id="d54e6-122">**Created date and time**</span></span>
- <span data-ttu-id="d54e6-123">**Einddatum**</span><span class="sxs-lookup"><span data-stu-id="d54e6-123">**End date**</span></span>
- <span data-ttu-id="d54e6-124">**Verloftype**</span><span class="sxs-lookup"><span data-stu-id="d54e6-124">**Leave type**</span></span>
- <span data-ttu-id="d54e6-125">**Gewijzigd door**</span><span class="sxs-lookup"><span data-stu-id="d54e6-125">**Modified by**</span></span>
- <span data-ttu-id="d54e6-126">**Wijzigingsdatum en -tijd**</span><span class="sxs-lookup"><span data-stu-id="d54e6-126">**Modified date and time**</span></span>
- <span data-ttu-id="d54e6-127">**Redencode**</span><span class="sxs-lookup"><span data-stu-id="d54e6-127">**Reason code**</span></span>
- <span data-ttu-id="d54e6-128">**Aanvraag-ID**</span><span class="sxs-lookup"><span data-stu-id="d54e6-128">**Request ID**</span></span>
- <span data-ttu-id="d54e6-129">**Begindatum**</span><span class="sxs-lookup"><span data-stu-id="d54e6-129">**Start date**</span></span>
- <span data-ttu-id="d54e6-130">**Status**</span><span class="sxs-lookup"><span data-stu-id="d54e6-130">**Status**</span></span> 
- <span data-ttu-id="d54e6-131">**Datum van indiening**</span><span class="sxs-lookup"><span data-stu-id="d54e6-131">**Submission date**</span></span>
- <span data-ttu-id="d54e6-132">**Ingediend door**</span><span class="sxs-lookup"><span data-stu-id="d54e6-132">**Submitted by**</span></span>
- <span data-ttu-id="d54e6-133">**Ingediend door Human Resources**</span><span class="sxs-lookup"><span data-stu-id="d54e6-133">**Submitted by Human resources**</span></span>
- <span data-ttu-id="d54e6-134">**Ingediend door manager**</span><span class="sxs-lookup"><span data-stu-id="d54e6-134">**Submitted by Manager**</span></span>
- <span data-ttu-id="d54e6-135">**Ingediend namens**</span><span class="sxs-lookup"><span data-stu-id="d54e6-135">**Submitted on behalf**</span></span>
- <span data-ttu-id="d54e6-136">**Werknemer**</span><span class="sxs-lookup"><span data-stu-id="d54e6-136">**Worker**</span></span>
- <span data-ttu-id="d54e6-137">**Type medewerker**</span><span class="sxs-lookup"><span data-stu-id="d54e6-137">**Worker type**</span></span>

<span data-ttu-id="d54e6-138">In deze voorbeelden ziet u hoe u verschillende typen workflowvoorwaarden kunt maken met behulp van deze gegevenselementen:</span><span class="sxs-lookup"><span data-stu-id="d54e6-138">These examples show how you can create different types of workflow conditions by using these data elements:</span></span>

- <span data-ttu-id="d54e6-139">Met **Redencode** in een voorwaardelijke instructie kunt u ziekteverlofaanvragen met de redencode **Operatie** naar HR routeren voor goedkeuring, terwijl u alle andere redencodes aan de manager doorstuurt.</span><span class="sxs-lookup"><span data-stu-id="d54e6-139">Use **Reason code** in a conditional statement to route sick leave requests with the reason code **Surgery** to HR for approval, while routing all other reason codes to the manager.</span></span> <span data-ttu-id="d54e6-140">Zie [Voorwaardelijke beslissingen in een workflow configureren](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-conditional-decision-workflow) voor meer informatie over voorwaardelijke instructies.</span><span class="sxs-lookup"><span data-stu-id="d54e6-140">For more information about conditional statements, see [Configure conditional decisions in a workflow](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-conditional-decision-workflow).</span></span> 

- <span data-ttu-id="d54e6-141">Gebruik **Ingediend door Human Resources** en **Ingediend door manager** in een automatische actie om verlofaanvragen die deze rollen namens werknemers indienen, automatisch goed te keuren.</span><span class="sxs-lookup"><span data-stu-id="d54e6-141">Use **Submitted by Human resources** and **Submitted by manager** in an automatic action to automatically approve leave requests that these roles submit on behalf of employees.</span></span> <span data-ttu-id="d54e6-142">Zie [Goedkeuringsprocessen in een workflow configureren](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-approval-process-workflow) voor meer informatie over deze automatische acties.</span><span class="sxs-lookup"><span data-stu-id="d54e6-142">For more information about automatic actions, see [Configure approval processes in a workflow](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-approval-process-workflow).</span></span>

- <span data-ttu-id="d54e6-143">Gebruik **Verloftype** in een voorwaardelijke instructie of automatische actie om te bepalen hoe aanvragen met bepaalde verloftypen door de workflow worden gerouteerd.</span><span class="sxs-lookup"><span data-stu-id="d54e6-143">Use **Leave type** in a conditional statement or automatic action to control how the workflow routes requests with certain leave types.</span></span>

## <a name="see-also"></a><span data-ttu-id="d54e6-144">Zie ook</span><span class="sxs-lookup"><span data-stu-id="d54e6-144">See also</span></span>

- [<span data-ttu-id="d54e6-145">Overzicht van verlof en verzuim</span><span class="sxs-lookup"><span data-stu-id="d54e6-145">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]