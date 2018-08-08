---
title: "Toegangsrechten definiëren voor controllers voor kostenobjecten"
description: Dit onderwerp bevat informatie over toegangsrechten voor controllers voor kostenobjecten.
author: AndersGirke
manager: AnnBe
ms.date: 06/24/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CAMCostControlWorkspace, CAMParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: 290b16eeb99ac7ddb9b552b289215c99a0451660
ms.contentlocale: nl-nl
ms.lasthandoff: 08/07/2018

---

# <a name="access-rights-of-a-cost-object-controller"></a><span data-ttu-id="53970-103">Toegangsrechten voor een controller voor kostenobjecten</span><span class="sxs-lookup"><span data-stu-id="53970-103">Access rights of a cost object controller</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="53970-104">Het werkgebied **Kostenbeheer** is een centraal punt waar managers de prestaties van hun kostenobjecten kunnen bekijken.</span><span class="sxs-lookup"><span data-stu-id="53970-104">The **Cost control** workspace is a central point where managers can view the performance of their cost objects.</span></span> <span data-ttu-id="53970-105">In dit werkgebied kunnen managers gebruikmaken van gegevens over Kostprijsboekhouding, zelfs als ze geen kostenaccountants zijn.</span><span class="sxs-lookup"><span data-stu-id="53970-105">This workspace lets managers consume Cost accounting data even though they aren't cost accountants.</span></span> <span data-ttu-id="53970-106">Uit veiligheidsoverwegingen dienen managers alleen de gegevens over Kostprijsboekhouding te mogen zien die betrekking hebben op de specifieke kostenobjecten waarvoor ze verantwoordelijk zijn.</span><span class="sxs-lookup"><span data-stu-id="53970-106">For security reasons, managers should be allowed to see only the Cost accounting data that is related to the specific cost objects that they are responsible for.</span></span>

<span data-ttu-id="53970-107">Er zijn vier unieke rollen in Kostprijsboekhouding.</span><span class="sxs-lookup"><span data-stu-id="53970-107">There are four unique roles in Cost accounting.</span></span>

| <span data-ttu-id="53970-108">Rolnaam</span><span class="sxs-lookup"><span data-stu-id="53970-108">Role name</span></span>               | <span data-ttu-id="53970-109">Licentie</span><span class="sxs-lookup"><span data-stu-id="53970-109">License</span></span>      |
|-------------------------|--------------|
| <span data-ttu-id="53970-110">Manager van kostprijsboekhouding</span><span class="sxs-lookup"><span data-stu-id="53970-110">Cost accounting manager</span></span> | <span data-ttu-id="53970-111">Activiteit</span><span class="sxs-lookup"><span data-stu-id="53970-111">Activity</span></span>     |
| <span data-ttu-id="53970-112">Kostenaccountant</span><span class="sxs-lookup"><span data-stu-id="53970-112">Cost accountant</span></span>         | <span data-ttu-id="53970-113">Operations</span><span class="sxs-lookup"><span data-stu-id="53970-113">Operations</span></span>   |
| <span data-ttu-id="53970-114">Assistent kostenaccountant</span><span class="sxs-lookup"><span data-stu-id="53970-114">Cost accountant clerk</span></span>   | <span data-ttu-id="53970-115">Operations</span><span class="sxs-lookup"><span data-stu-id="53970-115">Operations</span></span>   |
| <span data-ttu-id="53970-116">Controller voor kostenobjecten</span><span class="sxs-lookup"><span data-stu-id="53970-116">Cost object controller</span></span>  | <span data-ttu-id="53970-117">Teamleden</span><span class="sxs-lookup"><span data-stu-id="53970-117">Team members</span></span> |

<span data-ttu-id="53970-118">In dit onderwerp wordt uitgelegd hoe de rol **Controller voor kostenobjecten** aan een manager kan worden toegewezen.</span><span class="sxs-lookup"><span data-stu-id="53970-118">This topic explains how to assign the **Cost object controller** role to a manager.</span></span>

<span data-ttu-id="53970-119">Wanneer de **Controller voor kostenobjecten** wordt toegewezen aan een manager, kan de manager de volgende taken uitvoeren:</span><span class="sxs-lookup"><span data-stu-id="53970-119">When the **Cost object controller** role is assigned to a manager, the manager can perform the following tasks:</span></span>

- <span data-ttu-id="53970-120">Toegang verkrijgen tot het werkgebied **Kostenbeheer** (in de client).</span><span class="sxs-lookup"><span data-stu-id="53970-120">Access the **Cost control** workspace (in the client).</span></span>

    - <span data-ttu-id="53970-121">Gedetailleerd bekijken van en weergaverechten verkrijgen voor de pagina's die ondersteuning bieden aan de detailanalyse-ervaring.</span><span class="sxs-lookup"><span data-stu-id="53970-121">Drill through and have view access to the pages that support the drill-through experience.</span></span>

- <span data-ttu-id="53970-122">Toegang verkrijgen tot het werkgebied **Kostenbeheer** (in de mobiele toepassing).</span><span class="sxs-lookup"><span data-stu-id="53970-122">Access the **Cost control** workspace (in the mobile application).</span></span>

> [!NOTE]
> <span data-ttu-id="53970-123">De rol **Controller voor kostenobjecten** bepaalt niet de kostenobjecten tot welke de gebruiker toegang kan krijgen en waarvoor gegevens kunnen worden weergegeven.</span><span class="sxs-lookup"><span data-stu-id="53970-123">The **Cost object controller** role doesn't control which cost objects the user can access and view data for.</span></span> <span data-ttu-id="53970-124">Beveiliging op rijniveau wordt geleverd via dimensiehiërarchieën en de hiërarchie van toegangslijsten.</span><span class="sxs-lookup"><span data-stu-id="53970-124">Row-level security is provided via dimension hierarchies and the Access list hierarchy.</span></span>

## <a name="grant-access-rights"></a><span data-ttu-id="53970-125">Toegangsrechten toekennen</span><span class="sxs-lookup"><span data-stu-id="53970-125">Grant access rights</span></span>
<span data-ttu-id="53970-126">In het volgende voorbeeld ziet u hoe een dimensiehiërarchie eruit kan zien.</span><span class="sxs-lookup"><span data-stu-id="53970-126">The following example shows what a dimension hierarchy can look like.</span></span>

<span data-ttu-id="53970-127">**Gegevens van dimensiehiërarchie**</span><span class="sxs-lookup"><span data-stu-id="53970-127">**Dimension hierarchy details**</span></span>

| <span data-ttu-id="53970-128">Naam van dimensiehiërarchie</span><span class="sxs-lookup"><span data-stu-id="53970-128">Dimension hierarchy name</span></span> | <span data-ttu-id="53970-129">Dimensie</span><span class="sxs-lookup"><span data-stu-id="53970-129">Dimension</span></span>    | <span data-ttu-id="53970-130">Naam van type dimensiehiërarchie</span><span class="sxs-lookup"><span data-stu-id="53970-130">Dimension hierarchy type name</span></span>      | <span data-ttu-id="53970-131">Hiërarchie van toegangslijsten</span><span class="sxs-lookup"><span data-stu-id="53970-131">Access list hierarchy</span></span> |
|--------------------------|--------------|------------------------------------|-----------------------|
| <span data-ttu-id="53970-132">Organisatie</span><span class="sxs-lookup"><span data-stu-id="53970-132">Organization</span></span>             | <span data-ttu-id="53970-133">Kostenplaatsen</span><span class="sxs-lookup"><span data-stu-id="53970-133">Cost centers</span></span> | <span data-ttu-id="53970-134">Hiërarchie dimensieclassificatie</span><span class="sxs-lookup"><span data-stu-id="53970-134">Dimension classification hierarchy</span></span> | <span data-ttu-id="53970-135">**Ja**</span><span class="sxs-lookup"><span data-stu-id="53970-135">**Yes**</span></span>               |

<span data-ttu-id="53970-136">U kunt het sneltabblad **Gebruikers** in de hiërarchieontwerper gebruiken om een of meer gebruikers-id's op elk knooppunt in te voegen.</span><span class="sxs-lookup"><span data-stu-id="53970-136">You can use the **Users** FastTab in the hierarchy designer to insert one or more user IDs on each node.</span></span>

|                                   | <span data-ttu-id="53970-137">Gebruikers</span><span class="sxs-lookup"><span data-stu-id="53970-137">Users</span></span>            | <span data-ttu-id="53970-138">Bereiken van dimensieleden</span><span class="sxs-lookup"><span data-stu-id="53970-138">Dimension member ranges</span></span>   |                         |
|-----------------------------------|------------------|---------------------------|-------------------------|
| <span data-ttu-id="53970-139">**Knooppunten**</span><span class="sxs-lookup"><span data-stu-id="53970-139">**Nodes**</span></span>                         | <span data-ttu-id="53970-140">**Gebruikers-id**</span><span class="sxs-lookup"><span data-stu-id="53970-140">**User ID**</span></span>      | <span data-ttu-id="53970-141">**Van dimensielid**</span><span class="sxs-lookup"><span data-stu-id="53970-141">**From dimension member**</span></span> | <span data-ttu-id="53970-142">**Tot dimensielid**</span><span class="sxs-lookup"><span data-stu-id="53970-142">**To dimension member**</span></span> |
| <span data-ttu-id="53970-143">Organisatie</span><span class="sxs-lookup"><span data-stu-id="53970-143">Organization</span></span>                      | <span data-ttu-id="53970-144">Benjamin, Claire</span><span class="sxs-lookup"><span data-stu-id="53970-144">Benjamin, Claire</span></span> |                           |                         |
| <span data-ttu-id="53970-145">&nbsp;&nbsp;Beheer</span><span class="sxs-lookup"><span data-stu-id="53970-145">&nbsp;&nbsp;Admin</span></span>                 | <span data-ttu-id="53970-146">april</span><span class="sxs-lookup"><span data-stu-id="53970-146">April</span></span>            |                           |                         |
| <span data-ttu-id="53970-147">&nbsp;&nbsp;&nbsp;&nbsp;Financiën</span><span class="sxs-lookup"><span data-stu-id="53970-147">&nbsp;&nbsp;&nbsp;&nbsp;Finance</span></span>   | <span data-ttu-id="53970-148">Alicia</span><span class="sxs-lookup"><span data-stu-id="53970-148">Alicia</span></span>           | <span data-ttu-id="53970-149">CC002</span><span class="sxs-lookup"><span data-stu-id="53970-149">CC002</span></span>                     | <span data-ttu-id="53970-150">CC003</span><span class="sxs-lookup"><span data-stu-id="53970-150">CC003</span></span>                   |
|                                   |                  | <span data-ttu-id="53970-151">CC007</span><span class="sxs-lookup"><span data-stu-id="53970-151">CC007</span></span>                     | <span data-ttu-id="53970-152">CC007</span><span class="sxs-lookup"><span data-stu-id="53970-152">CC007</span></span>                   |
| <span data-ttu-id="53970-153">&nbsp;&nbsp;&nbsp;&nbsp;HR</span><span class="sxs-lookup"><span data-stu-id="53970-153">&nbsp;&nbsp;&nbsp;&nbsp;HR</span></span>        | <span data-ttu-id="53970-154">Arnie</span><span class="sxs-lookup"><span data-stu-id="53970-154">Arnie</span></span>            | <span data-ttu-id="53970-155">CC001</span><span class="sxs-lookup"><span data-stu-id="53970-155">CC001</span></span>                     | <span data-ttu-id="53970-156">CC001</span><span class="sxs-lookup"><span data-stu-id="53970-156">CC001</span></span>                   |
| <span data-ttu-id="53970-157">&nbsp;&nbsp;Productie</span><span class="sxs-lookup"><span data-stu-id="53970-157">&nbsp;&nbsp;Production</span></span>            | <span data-ttu-id="53970-158">David</span><span class="sxs-lookup"><span data-stu-id="53970-158">David</span></span>            |                           |                         |
| <span data-ttu-id="53970-159">&nbsp;&nbsp;&nbsp;&nbsp;Verpakking</span><span class="sxs-lookup"><span data-stu-id="53970-159">&nbsp;&nbsp;&nbsp;&nbsp;Packaging</span></span> | <span data-ttu-id="53970-160">Ellen</span><span class="sxs-lookup"><span data-stu-id="53970-160">Ellen</span></span>            | <span data-ttu-id="53970-161">CC005</span><span class="sxs-lookup"><span data-stu-id="53970-161">CC005</span></span>                     | <span data-ttu-id="53970-162">CC005</span><span class="sxs-lookup"><span data-stu-id="53970-162">CC005</span></span>                   |
| <span data-ttu-id="53970-163">&nbsp;&nbsp;&nbsp;&nbsp;Assembleren</span><span class="sxs-lookup"><span data-stu-id="53970-163">&nbsp;&nbsp;&nbsp;&nbsp;Assembly</span></span>  | <span data-ttu-id="53970-164">Chris</span><span class="sxs-lookup"><span data-stu-id="53970-164">Chris</span></span>            | <span data-ttu-id="53970-165">CC006</span><span class="sxs-lookup"><span data-stu-id="53970-165">CC006</span></span>                     | <span data-ttu-id="53970-166">CC006</span><span class="sxs-lookup"><span data-stu-id="53970-166">CC006</span></span>                   |

> [!NOTE]
> <span data-ttu-id="53970-167">Kostenaccountants moeten worden toegewezen op het hoogste niveau van de hiërarchie, zodat ze alle vermeldingen in Kostprijsboekhouding kunnen zien.</span><span class="sxs-lookup"><span data-stu-id="53970-167">Cost accountants should be assigned to the top level of the hierarchy, so that they can see all entries in Cost accounting.</span></span>

<span data-ttu-id="53970-168">Voordat de hiërarchie van toegangslijsten en de beveiligingsinstellingen kunnen worden toegepast, moet de optie **Weergavetoegang voor dimensieleden voor kostenobject inschakelen** op **Ja** worden ingesteld op het tabblad **Algemeen** van de pagina **Parameters voor kostprijsboekhouding** (**Kostprijsboekhouding** > **Instellen** > **Parameters**).</span><span class="sxs-lookup"><span data-stu-id="53970-168">Before the Access list hierarchy and its security settings can be applied, the **Enable view access for cost object dimension members** option must be set to **Yes** on the **General** tab of the **Cost accounting parameters** page (**Cost accounting** > **Setup** > **Parameters**).</span></span>

<span data-ttu-id="53970-169">De instellingen voor de hiërarchie van toegangslijsten worden gebruikt voor het bepalen van de gegevens die in de volgende gebieden worden weergegeven:</span><span class="sxs-lookup"><span data-stu-id="53970-169">The settings for the Access list hierarchy are used to control the data that is shown in following areas:</span></span>

- <span data-ttu-id="53970-170">Werkgebied **Kostenbeheer** (in de client):</span><span class="sxs-lookup"><span data-stu-id="53970-170">**Cost control** workspace (in the client):</span></span>

    - <span data-ttu-id="53970-171">Gegevens op de pagina's die worden gebruikt voor detailanalyse</span><span class="sxs-lookup"><span data-stu-id="53970-171">Data on the pages that are used for drill-through</span></span>

- <span data-ttu-id="53970-172">Werkgebied **Kostenbeheer** (in de mobiele toepassing):</span><span class="sxs-lookup"><span data-stu-id="53970-172">**Cost control** workspace (in the mobile application):</span></span>

    - <span data-ttu-id="53970-173">Saldi in kaarten</span><span class="sxs-lookup"><span data-stu-id="53970-173">Balances in cards</span></span>

- <span data-ttu-id="53970-174">Microsoft Power BI:</span><span class="sxs-lookup"><span data-stu-id="53970-174">Microsoft Power BI:</span></span>

    - <span data-ttu-id="53970-175">Gegevens die worden weergegeven in Power BI-visualisaties</span><span class="sxs-lookup"><span data-stu-id="53970-175">Data that is shown in Power BI visualizations</span></span>
    - <span data-ttu-id="53970-176">Gegevens van Power BI-visualisaties die worden ingesloten in Microsoft Dynamics 365 for Finance and Operations, client</span><span class="sxs-lookup"><span data-stu-id="53970-176">Data Power BI visualizations that are embedded in the Microsoft Dynamics 365 for Finance and Operations, client</span></span>

> [!IMPORTANT]
> - <span data-ttu-id="53970-177">Voordat de hiërarchie van toegangslijsten van invloed kan zijn op gegevens in Power BI, moeten de hiërarchie van toegangslijsten en beveiliging op rijniveau in Power BI worden gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="53970-177">Before the Access list hierarchy can affect data in Power BI, the Access list hierarchy and row-level security in Power BI must be paired.</span></span> <span data-ttu-id="53970-178">Zie [Beveiliging instellen voor het inhoudpakket Kostprijsboekhouding](../../dev-itpro/analytics/setup-security-cost-accounting-content-pack.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="53970-178">For more information, see [Set up security for Cost accounting content pack](../../dev-itpro/analytics/setup-security-cost-accounting-content-pack.md).</span></span>
> - <span data-ttu-id="53970-179">Dit onderwerp bevat de vereisten waaraan moet worden voldaan voordat u het werkgebied **Kostenbeheer** kunt gebruiken.</span><span class="sxs-lookup"><span data-stu-id="53970-179">This topic shows the prerequisites that must be in place before you can use the **Cost control** workspace.</span></span>

<span data-ttu-id="53970-180">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="53970-180">Additional resources</span></span>

- [<span data-ttu-id="53970-181">Werkgebied voor kostenbeheer</span><span class="sxs-lookup"><span data-stu-id="53970-181">Cost control workspace</span></span>](cost-control-workspace.md)
- [<span data-ttu-id="53970-182">Dimensiehiërarchie</span><span class="sxs-lookup"><span data-stu-id="53970-182">Dimension hierarchy</span></span>](dimension-hierarchy.md)
- [<span data-ttu-id="53970-183">Beveiliging instellen voor het inhoudpakket Kostprijsboekhouding</span><span class="sxs-lookup"><span data-stu-id="53970-183">Set up security for Cost accounting content pack</span></span>](../../dev-itpro/analytics/setup-security-cost-accounting-content-pack.md)

