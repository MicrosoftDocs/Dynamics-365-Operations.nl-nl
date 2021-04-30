---
title: Een werkstroom maken voor het aanvragen voor het kopen en verkopen van verlof
description: Maak een werkstroom voor aanvragen voor het kopen en verkopen van verlof om aanvragen voor het kopen en verkopen van verlof op consistente wijze te beheren in Dynamics 365 Human Resources.
author: andreabichsel
ms.date: 08/20/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-08-20
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 15cedc16fbdbb5d25daa262f094a56bb8fe2f5cc
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/13/2021
ms.locfileid: "5892700"
---
# <a name="create-a-buy-and-sell-leave-request-workflow"></a><span data-ttu-id="9c4e2-103">Een werkstroom maken voor het aanvragen voor het kopen en verkopen van verlof</span><span class="sxs-lookup"><span data-stu-id="9c4e2-103">Create a buy and sell leave request workflow</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="9c4e2-104">U kunt in Dynamics 365 Human Resources een werkstroom maken om aanvragen voor het kopen en verkopen van verlof op consistente wijze te beheren.</span><span class="sxs-lookup"><span data-stu-id="9c4e2-104">You can create a workflow in Dynamics 365 Human Resources to consistently manage your buy and sell leave requests.</span></span> <span data-ttu-id="9c4e2-105">Met een werkstroom voor het **kopen en verkopen van verlof** kunt u:</span><span class="sxs-lookup"><span data-stu-id="9c4e2-105">A **Buy and sell leave** workflow lets you:</span></span>

- <span data-ttu-id="9c4e2-106">Taken definiëren</span><span class="sxs-lookup"><span data-stu-id="9c4e2-106">Define tasks</span></span>
- <span data-ttu-id="9c4e2-107">Bepalen wie de taken moet voltooien</span><span class="sxs-lookup"><span data-stu-id="9c4e2-107">Determine who must complete the tasks</span></span>
- <span data-ttu-id="9c4e2-108">Opgeven wie aanvragen kan goedkeuren of afwijzen</span><span class="sxs-lookup"><span data-stu-id="9c4e2-108">Specify who can approve or reject requests</span></span>

## <a name="create-a-buy-and-sell-leave-request-workflow"></a><span data-ttu-id="9c4e2-109">Een werkstroom maken voor het aanvragen voor het kopen en verkopen van verlof</span><span class="sxs-lookup"><span data-stu-id="9c4e2-109">Create a buy and sell leave request workflow</span></span>

1. <span data-ttu-id="9c4e2-110">Selecteer op de pagina **Verlof en verzuim** het tabblad **Koppelingen**.</span><span class="sxs-lookup"><span data-stu-id="9c4e2-110">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="9c4e2-111">Selecteer onder **Instellen** de optie **Workflows voor Human resources**.</span><span class="sxs-lookup"><span data-stu-id="9c4e2-111">Under **Setup**, select **Human resource workflows**.</span></span>

3. <span data-ttu-id="9c4e2-112">Selecteer **Nieuw** en selecteer vervolgens **Aanvraag om verlof te kopen en verkopen**.</span><span class="sxs-lookup"><span data-stu-id="9c4e2-112">Select **New**, and then select **Buy and sell leave request**.</span></span> 

4. <span data-ttu-id="9c4e2-113">Wanneer het berichtvenster **Dit bestand openen?** verschijnt, selecteert u **Openen** en meldt u zich aan en met uw bedrijfsreferenties.</span><span class="sxs-lookup"><span data-stu-id="9c4e2-113">When the **Open this file?** message box appears, select **Open** and sign in with your company credentials.</span></span>

5. <span data-ttu-id="9c4e2-114">Gebruik de workflow-editor om een workflow voor uw verlofaanvragen te maken.</span><span class="sxs-lookup"><span data-stu-id="9c4e2-114">Use the workflow editor to create a workflow for your leave requests.</span></span> <span data-ttu-id="9c4e2-115">Zie [Overzicht van workflows maken](../fin-ops-core/fin-ops/organization-administration/create-workflow.md?toc=%2fdynamics365%2fcommerce%2ftoc.json.) voor meer informatie over het werken met workflows.</span><span class="sxs-lookup"><span data-stu-id="9c4e2-115">For more information about working with workflows, see [Create workflows overview](../fin-ops-core/fin-ops/organization-administration/create-workflow.md?toc=%2fdynamics365%2fcommerce%2ftoc.json.)</span></span>

## <a name="leave-and-absence-request-workflow-data-elements"></a><span data-ttu-id="9c4e2-116">Gegevenselementen van workflow voor verlof- en verzuimaanvragen</span><span class="sxs-lookup"><span data-stu-id="9c4e2-116">Leave and absence request workflow data elements</span></span>

<span data-ttu-id="9c4e2-117">U kunt de volgende gegevenselementen gebruiken om voorwaardelijke of automatische goedkeuringen te maken in werkstromen voor aanvragen om verlof te kopen en verkopen:</span><span class="sxs-lookup"><span data-stu-id="9c4e2-117">You can use the following data elements to create conditional or automatic approvals in workflows for buy and sell leave requests:</span></span>

- <span data-ttu-id="9c4e2-118">**Bedrag**</span><span class="sxs-lookup"><span data-stu-id="9c4e2-118">**Amount**</span></span>
- <span data-ttu-id="9c4e2-119">**Beleid voor verlof inkopen/verkopen**</span><span class="sxs-lookup"><span data-stu-id="9c4e2-119">**Buy and sell leave policy**</span></span>
- <span data-ttu-id="9c4e2-120">**Bedrijf**</span><span class="sxs-lookup"><span data-stu-id="9c4e2-120">**Company**</span></span>
- <span data-ttu-id="9c4e2-121">**Gemaakt door**</span><span class="sxs-lookup"><span data-stu-id="9c4e2-121">**Created by**</span></span>
- <span data-ttu-id="9c4e2-122">**Aanmaakdatum en -tijd**</span><span class="sxs-lookup"><span data-stu-id="9c4e2-122">**Created date and time**</span></span>
- <span data-ttu-id="9c4e2-123">**Einddatum**</span><span class="sxs-lookup"><span data-stu-id="9c4e2-123">**End date**</span></span>
- <span data-ttu-id="9c4e2-124">**Verloftype**</span><span class="sxs-lookup"><span data-stu-id="9c4e2-124">**Leave type**</span></span>
- <span data-ttu-id="9c4e2-125">**Gewijzigd door**</span><span class="sxs-lookup"><span data-stu-id="9c4e2-125">**Modified by**</span></span>
- <span data-ttu-id="9c4e2-126">**Wijzigingsdatum en -tijd**</span><span class="sxs-lookup"><span data-stu-id="9c4e2-126">**Modified date and time**</span></span>
- <span data-ttu-id="9c4e2-127">**Aanvraag-ID**</span><span class="sxs-lookup"><span data-stu-id="9c4e2-127">**Request ID**</span></span>
- <span data-ttu-id="9c4e2-128">**Begindatum**</span><span class="sxs-lookup"><span data-stu-id="9c4e2-128">**Start date**</span></span>
- <span data-ttu-id="9c4e2-129">**Status**</span><span class="sxs-lookup"><span data-stu-id="9c4e2-129">**Status**</span></span> 
- <span data-ttu-id="9c4e2-130">**Datum van indiening**</span><span class="sxs-lookup"><span data-stu-id="9c4e2-130">**Submission date**</span></span>
- <span data-ttu-id="9c4e2-131">**Ingediend door**</span><span class="sxs-lookup"><span data-stu-id="9c4e2-131">**Submitted by**</span></span>
- <span data-ttu-id="9c4e2-132">**Ingediend door Human Resources**</span><span class="sxs-lookup"><span data-stu-id="9c4e2-132">**Submitted by Human resources**</span></span>
- <span data-ttu-id="9c4e2-133">**Ingediend door manager**</span><span class="sxs-lookup"><span data-stu-id="9c4e2-133">**Submitted by Manager**</span></span>
- <span data-ttu-id="9c4e2-134">**Ingediend namens**</span><span class="sxs-lookup"><span data-stu-id="9c4e2-134">**Submitted on behalf**</span></span>
- <span data-ttu-id="9c4e2-135">**Werknemer**</span><span class="sxs-lookup"><span data-stu-id="9c4e2-135">**Worker**</span></span>

## <a name="workflow-examples"></a><span data-ttu-id="9c4e2-136">Voorbeelden van werkstromen</span><span class="sxs-lookup"><span data-stu-id="9c4e2-136">Workflow examples</span></span>

<span data-ttu-id="9c4e2-137">In deze voorbeelden ziet u hoe u verschillende typen workflowvoorwaarden kunt maken met behulp van deze gegevenselementen:</span><span class="sxs-lookup"><span data-stu-id="9c4e2-137">These examples show how you can create different types of workflow conditions by using these data elements:</span></span>

- <span data-ttu-id="9c4e2-138">Gebruik **Ingediend door Human Resources** en **Ingediend door manager** in een automatische actie om aanvragen voor het kopen en verkopen van verlof die deze rollen namens werknemers indienen, automatisch goed te keuren.</span><span class="sxs-lookup"><span data-stu-id="9c4e2-138">Use **Submitted by Human resources** and **Submitted by manager** in an automatic action to automatically approve buy and sell leave requests that these roles submit on behalf of employees.</span></span> <span data-ttu-id="9c4e2-139">Zie [Goedkeuringsprocessen in een workflow configureren](../fin-ops-core/fin-ops/organization-administration/configure-approval-process-workflow.md) voor meer informatie over deze automatische acties.</span><span class="sxs-lookup"><span data-stu-id="9c4e2-139">For more information about automatic actions, see [Configure approval processes in a workflow](../fin-ops-core/fin-ops/organization-administration/configure-approval-process-workflow.md).</span></span>

- <span data-ttu-id="9c4e2-140">Gebruik **Verloftype** in een voorwaardelijke instructie of automatische actie om te bepalen hoe aanvragen met bepaalde verloftypen door de workflow worden gerouteerd.</span><span class="sxs-lookup"><span data-stu-id="9c4e2-140">Use **Leave type** in a conditional statement or automatic action to control how the workflow routes requests with certain leave types.</span></span>

## <a name="see-also"></a><span data-ttu-id="9c4e2-141">Zie ook</span><span class="sxs-lookup"><span data-stu-id="9c4e2-141">See also</span></span>

[<span data-ttu-id="9c4e2-142">Overzicht van verlof en verzuim</span><span class="sxs-lookup"><span data-stu-id="9c4e2-142">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)<br>
[<span data-ttu-id="9c4e2-143">Beleid voor verlof inkopen/verkopen beheren</span><span class="sxs-lookup"><span data-stu-id="9c4e2-143">Manage buy and sell leave policies</span></span>](hr-leave-and-absence-manage-buy-and-sell-leave-policies.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]