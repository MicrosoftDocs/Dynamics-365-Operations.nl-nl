---
title: Toegangsrechten definiëren voor controllers voor kostenobjecten
description: Dit onderwerp bevat informatie over toegangsrechten voor controllers voor kostenobjecten.
author: AndersGirke
manager: AnnBe
ms.date: 06/24/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CAMCostControlWorkspace, CAMParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: e86f087a1df0f133dbaa5491cf5ba9e57b0e12d9
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/03/2019
ms.locfileid: "2551721"
---
# <a name="define-access-rights-for-cost-object-controllers"></a><span data-ttu-id="d82e6-103">Toegangsrechten definiëren voor controllers voor kostenobjecten</span><span class="sxs-lookup"><span data-stu-id="d82e6-103">Define access rights for cost object controllers</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d82e6-104">Het werkgebied **Kostenbeheer** is een centraal punt waar managers de prestaties van hun kostenobjecten kunnen bekijken.</span><span class="sxs-lookup"><span data-stu-id="d82e6-104">The **Cost control** workspace is a central point where managers can view the performance of their cost objects.</span></span> <span data-ttu-id="d82e6-105">In dit werkgebied kunnen managers gebruikmaken van gegevens over Kostprijsboekhouding, zelfs als ze geen kostenaccountants zijn.</span><span class="sxs-lookup"><span data-stu-id="d82e6-105">This workspace lets managers consume Cost accounting data even though they aren't cost accountants.</span></span> <span data-ttu-id="d82e6-106">Uit veiligheidsoverwegingen dienen managers alleen de gegevens over Kostprijsboekhouding te mogen zien die betrekking hebben op de specifieke kostenobjecten waarvoor ze verantwoordelijk zijn.</span><span class="sxs-lookup"><span data-stu-id="d82e6-106">For security reasons, managers should be allowed to see only the Cost accounting data that is related to the specific cost objects that they are responsible for.</span></span>

<span data-ttu-id="d82e6-107">Er zijn vier unieke rollen in Kostprijsboekhouding.</span><span class="sxs-lookup"><span data-stu-id="d82e6-107">There are four unique roles in Cost accounting.</span></span>

| <span data-ttu-id="d82e6-108">Rolnaam</span><span class="sxs-lookup"><span data-stu-id="d82e6-108">Role name</span></span>               | <span data-ttu-id="d82e6-109">Licentie</span><span class="sxs-lookup"><span data-stu-id="d82e6-109">License</span></span>      |
|-------------------------|--------------|
| <span data-ttu-id="d82e6-110">Manager van kostprijsboekhouding</span><span class="sxs-lookup"><span data-stu-id="d82e6-110">Cost accounting manager</span></span> | <span data-ttu-id="d82e6-111">Activiteit</span><span class="sxs-lookup"><span data-stu-id="d82e6-111">Activity</span></span>     |
| <span data-ttu-id="d82e6-112">Kostenaccountant</span><span class="sxs-lookup"><span data-stu-id="d82e6-112">Cost accountant</span></span>         | <span data-ttu-id="d82e6-113">Operations</span><span class="sxs-lookup"><span data-stu-id="d82e6-113">Operations</span></span>   |
| <span data-ttu-id="d82e6-114">Assistent kostenaccountant</span><span class="sxs-lookup"><span data-stu-id="d82e6-114">Cost accountant clerk</span></span>   | <span data-ttu-id="d82e6-115">Operations</span><span class="sxs-lookup"><span data-stu-id="d82e6-115">Operations</span></span>   |
| <span data-ttu-id="d82e6-116">Controller voor kostenobjecten</span><span class="sxs-lookup"><span data-stu-id="d82e6-116">Cost object controller</span></span>  | <span data-ttu-id="d82e6-117">Teamleden</span><span class="sxs-lookup"><span data-stu-id="d82e6-117">Team members</span></span> |

<span data-ttu-id="d82e6-118">In dit onderwerp wordt uitgelegd hoe de rol **Controller voor kostenobjecten** aan een manager kan worden toegewezen.</span><span class="sxs-lookup"><span data-stu-id="d82e6-118">This topic explains how to assign the **Cost object controller** role to a manager.</span></span>

<span data-ttu-id="d82e6-119">Wanneer de **Controller voor kostenobjecten** wordt toegewezen aan een manager, kan de manager de volgende taken uitvoeren:</span><span class="sxs-lookup"><span data-stu-id="d82e6-119">When the **Cost object controller** role is assigned to a manager, the manager can perform the following tasks:</span></span>

- <span data-ttu-id="d82e6-120">Toegang verkrijgen tot het werkgebied **Kostenbeheer** (in de client).</span><span class="sxs-lookup"><span data-stu-id="d82e6-120">Access the **Cost control** workspace (in the client).</span></span>

    - <span data-ttu-id="d82e6-121">Gedetailleerd bekijken van en weergaverechten verkrijgen voor de pagina's die ondersteuning bieden aan de detailanalyse-ervaring.</span><span class="sxs-lookup"><span data-stu-id="d82e6-121">Drill through and have view access to the pages that support the drill-through experience.</span></span>

- <span data-ttu-id="d82e6-122">Toegang verkrijgen tot het werkgebied **Kostenbeheer** (in de mobiele toepassing).</span><span class="sxs-lookup"><span data-stu-id="d82e6-122">Access the **Cost control** workspace (in the mobile application).</span></span>

> [!NOTE]
> <span data-ttu-id="d82e6-123">De rol **Controller voor kostenobjecten** bepaalt niet de kostenobjecten tot welke de gebruiker toegang kan krijgen en waarvoor gegevens kunnen worden weergegeven.</span><span class="sxs-lookup"><span data-stu-id="d82e6-123">The **Cost object controller** role doesn't control which cost objects the user can access and view data for.</span></span> <span data-ttu-id="d82e6-124">Beveiliging op rijniveau wordt geleverd via dimensiehiërarchieën en de hiërarchie van toegangslijsten.</span><span class="sxs-lookup"><span data-stu-id="d82e6-124">Row-level security is provided via dimension hierarchies and the Access list hierarchy.</span></span>

## <a name="grant-access-rights"></a><span data-ttu-id="d82e6-125">Toegangsrechten toekennen</span><span class="sxs-lookup"><span data-stu-id="d82e6-125">Grant access rights</span></span>
<span data-ttu-id="d82e6-126">In het volgende voorbeeld ziet u hoe een dimensiehiërarchie eruit kan zien.</span><span class="sxs-lookup"><span data-stu-id="d82e6-126">The following example shows what a dimension hierarchy can look like.</span></span>

<span data-ttu-id="d82e6-127">**Gegevens van dimensiehiërarchie**</span><span class="sxs-lookup"><span data-stu-id="d82e6-127">**Dimension hierarchy details**</span></span>

| <span data-ttu-id="d82e6-128">Naam van dimensiehiërarchie</span><span class="sxs-lookup"><span data-stu-id="d82e6-128">Dimension hierarchy name</span></span> | <span data-ttu-id="d82e6-129">Dimensie</span><span class="sxs-lookup"><span data-stu-id="d82e6-129">Dimension</span></span>    | <span data-ttu-id="d82e6-130">Naam van type dimensiehiërarchie</span><span class="sxs-lookup"><span data-stu-id="d82e6-130">Dimension hierarchy type name</span></span>      | <span data-ttu-id="d82e6-131">Hiërarchie van toegangslijsten</span><span class="sxs-lookup"><span data-stu-id="d82e6-131">Access list hierarchy</span></span> |
|--------------------------|--------------|------------------------------------|-----------------------|
| <span data-ttu-id="d82e6-132">Organisatie</span><span class="sxs-lookup"><span data-stu-id="d82e6-132">Organization</span></span>             | <span data-ttu-id="d82e6-133">Kostenplaatsen</span><span class="sxs-lookup"><span data-stu-id="d82e6-133">Cost centers</span></span> | <span data-ttu-id="d82e6-134">Hiërarchie dimensieclassificatie</span><span class="sxs-lookup"><span data-stu-id="d82e6-134">Dimension classification hierarchy</span></span> | <span data-ttu-id="d82e6-135">**Ja**</span><span class="sxs-lookup"><span data-stu-id="d82e6-135">**Yes**</span></span>               |

<span data-ttu-id="d82e6-136">U kunt het sneltabblad **Gebruikers** in de hiërarchieontwerper gebruiken om een of meer gebruikers-id's op elk knooppunt in te voegen.</span><span class="sxs-lookup"><span data-stu-id="d82e6-136">You can use the **Users** FastTab in the hierarchy designer to insert one or more user IDs on each node.</span></span>

|                                   | <span data-ttu-id="d82e6-137">Gebruikers</span><span class="sxs-lookup"><span data-stu-id="d82e6-137">Users</span></span>            | <span data-ttu-id="d82e6-138">Bereiken van dimensieleden</span><span class="sxs-lookup"><span data-stu-id="d82e6-138">Dimension member ranges</span></span>   |                         |
|-----------------------------------|------------------|---------------------------|-------------------------|
| <span data-ttu-id="d82e6-139">**Knooppunten**</span><span class="sxs-lookup"><span data-stu-id="d82e6-139">**Nodes**</span></span>                         | <span data-ttu-id="d82e6-140">**Gebruikers-id**</span><span class="sxs-lookup"><span data-stu-id="d82e6-140">**User ID**</span></span>      | <span data-ttu-id="d82e6-141">**Van dimensielid**</span><span class="sxs-lookup"><span data-stu-id="d82e6-141">**From dimension member**</span></span> | <span data-ttu-id="d82e6-142">**Tot dimensielid**</span><span class="sxs-lookup"><span data-stu-id="d82e6-142">**To dimension member**</span></span> |
| <span data-ttu-id="d82e6-143">Organisatie</span><span class="sxs-lookup"><span data-stu-id="d82e6-143">Organization</span></span>                      | <span data-ttu-id="d82e6-144">Benjamin, Claire</span><span class="sxs-lookup"><span data-stu-id="d82e6-144">Benjamin, Claire</span></span> |                           |                         |
| <span data-ttu-id="d82e6-145">&nbsp;&nbsp;Beheer</span><span class="sxs-lookup"><span data-stu-id="d82e6-145">&nbsp;&nbsp;Admin</span></span>                 | <span data-ttu-id="d82e6-146">april</span><span class="sxs-lookup"><span data-stu-id="d82e6-146">April</span></span>            |                           |                         |
| <span data-ttu-id="d82e6-147">&nbsp;&nbsp;&nbsp;&nbsp;Financiën</span><span class="sxs-lookup"><span data-stu-id="d82e6-147">&nbsp;&nbsp;&nbsp;&nbsp;Finance</span></span>   | <span data-ttu-id="d82e6-148">Alicia</span><span class="sxs-lookup"><span data-stu-id="d82e6-148">Alicia</span></span>           | <span data-ttu-id="d82e6-149">CC002</span><span class="sxs-lookup"><span data-stu-id="d82e6-149">CC002</span></span>                     | <span data-ttu-id="d82e6-150">CC003</span><span class="sxs-lookup"><span data-stu-id="d82e6-150">CC003</span></span>                   |
|                                   |                  | <span data-ttu-id="d82e6-151">CC007</span><span class="sxs-lookup"><span data-stu-id="d82e6-151">CC007</span></span>                     | <span data-ttu-id="d82e6-152">CC007</span><span class="sxs-lookup"><span data-stu-id="d82e6-152">CC007</span></span>                   |
| <span data-ttu-id="d82e6-153">&nbsp;&nbsp;&nbsp;&nbsp;HR</span><span class="sxs-lookup"><span data-stu-id="d82e6-153">&nbsp;&nbsp;&nbsp;&nbsp;HR</span></span>        | <span data-ttu-id="d82e6-154">Arnie</span><span class="sxs-lookup"><span data-stu-id="d82e6-154">Arnie</span></span>            | <span data-ttu-id="d82e6-155">CC001</span><span class="sxs-lookup"><span data-stu-id="d82e6-155">CC001</span></span>                     | <span data-ttu-id="d82e6-156">CC001</span><span class="sxs-lookup"><span data-stu-id="d82e6-156">CC001</span></span>                   |
| <span data-ttu-id="d82e6-157">&nbsp;&nbsp;Productie</span><span class="sxs-lookup"><span data-stu-id="d82e6-157">&nbsp;&nbsp;Production</span></span>            | <span data-ttu-id="d82e6-158">David</span><span class="sxs-lookup"><span data-stu-id="d82e6-158">David</span></span>            |                           |                         |
| <span data-ttu-id="d82e6-159">&nbsp;&nbsp;&nbsp;&nbsp;Verpakking</span><span class="sxs-lookup"><span data-stu-id="d82e6-159">&nbsp;&nbsp;&nbsp;&nbsp;Packaging</span></span> | <span data-ttu-id="d82e6-160">Ellen</span><span class="sxs-lookup"><span data-stu-id="d82e6-160">Ellen</span></span>            | <span data-ttu-id="d82e6-161">CC005</span><span class="sxs-lookup"><span data-stu-id="d82e6-161">CC005</span></span>                     | <span data-ttu-id="d82e6-162">CC005</span><span class="sxs-lookup"><span data-stu-id="d82e6-162">CC005</span></span>                   |
| <span data-ttu-id="d82e6-163">&nbsp;&nbsp;&nbsp;&nbsp;Assembleren</span><span class="sxs-lookup"><span data-stu-id="d82e6-163">&nbsp;&nbsp;&nbsp;&nbsp;Assembly</span></span>  | <span data-ttu-id="d82e6-164">Chris</span><span class="sxs-lookup"><span data-stu-id="d82e6-164">Chris</span></span>            | <span data-ttu-id="d82e6-165">CC006</span><span class="sxs-lookup"><span data-stu-id="d82e6-165">CC006</span></span>                     | <span data-ttu-id="d82e6-166">CC006</span><span class="sxs-lookup"><span data-stu-id="d82e6-166">CC006</span></span>                   |

> [!NOTE]
> <span data-ttu-id="d82e6-167">Kostenaccountants moeten worden toegewezen op het hoogste niveau van de hiërarchie, zodat ze alle vermeldingen in Kostprijsboekhouding kunnen zien.</span><span class="sxs-lookup"><span data-stu-id="d82e6-167">Cost accountants should be assigned to the top level of the hierarchy, so that they can see all entries in Cost accounting.</span></span>

<span data-ttu-id="d82e6-168">Voordat de hiërarchie van toegangslijsten en de beveiligingsinstellingen kunnen worden toegepast, moet de optie **Weergavetoegang voor dimensieleden voor kostenobject inschakelen** op **Ja** worden ingesteld op het tabblad **Algemeen** van de pagina **Parameters voor kostprijsboekhouding** (**Kostprijsboekhouding** > **Instellen** > **Parameters**).</span><span class="sxs-lookup"><span data-stu-id="d82e6-168">Before the Access list hierarchy and its security settings can be applied, the **Enable view access for cost object dimension members** option must be set to **Yes** on the **General** tab of the **Cost accounting parameters** page (**Cost accounting** > **Setup** > **Parameters**).</span></span>

<span data-ttu-id="d82e6-169">De instellingen voor de hiërarchie van toegangslijsten worden gebruikt voor het bepalen van de gegevens die in de volgende gebieden worden weergegeven:</span><span class="sxs-lookup"><span data-stu-id="d82e6-169">The settings for the Access list hierarchy are used to control the data that is shown in following areas:</span></span>

- <span data-ttu-id="d82e6-170">Werkgebied **Kostenbeheer** (in de client):</span><span class="sxs-lookup"><span data-stu-id="d82e6-170">**Cost control** workspace (in the client):</span></span>

    - <span data-ttu-id="d82e6-171">Gegevens op de pagina's die worden gebruikt voor detailanalyse</span><span class="sxs-lookup"><span data-stu-id="d82e6-171">Data on the pages that are used for drill-through</span></span>

- <span data-ttu-id="d82e6-172">Werkgebied **Kostenbeheer** (in de mobiele toepassing):</span><span class="sxs-lookup"><span data-stu-id="d82e6-172">**Cost control** workspace (in the mobile application):</span></span>

    - <span data-ttu-id="d82e6-173">Saldi in kaarten</span><span class="sxs-lookup"><span data-stu-id="d82e6-173">Balances in cards</span></span>

- <span data-ttu-id="d82e6-174">Microsoft Power BI:</span><span class="sxs-lookup"><span data-stu-id="d82e6-174">Microsoft Power BI:</span></span>

    - <span data-ttu-id="d82e6-175">Gegevens die worden weergegeven in Power BI-visualisaties</span><span class="sxs-lookup"><span data-stu-id="d82e6-175">Data that is shown in Power BI visualizations</span></span>
    - <span data-ttu-id="d82e6-176">Power BI-gegevensvisualisaties die zijn ingesloten in de Dynamics 365 Finance-client</span><span class="sxs-lookup"><span data-stu-id="d82e6-176">Data Power BI visualizations that are embedded in the Dynamics 365 Finance client</span></span>

> [!IMPORTANT]
> - <span data-ttu-id="d82e6-177">Voordat de hiërarchie van toegangslijsten van invloed kan zijn op gegevens in Power BI, moeten de hiërarchie van toegangslijsten en beveiliging op rijniveau in Power BI worden gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="d82e6-177">Before the Access list hierarchy can affect data in Power BI, the Access list hierarchy and row-level security in Power BI must be paired.</span></span> <span data-ttu-id="d82e6-178">Zie [Beveiliging instellen voor het inhoudpakket Kostprijsboekhouding](../../dev-itpro/analytics/setup-security-cost-accounting-content-pack.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="d82e6-178">For more information, see [Set up security for Cost accounting content pack](../../dev-itpro/analytics/setup-security-cost-accounting-content-pack.md).</span></span>
> - <span data-ttu-id="d82e6-179">Dit onderwerp bevat de vereisten waaraan moet worden voldaan voordat u het werkgebied **Kostenbeheer** kunt gebruiken.</span><span class="sxs-lookup"><span data-stu-id="d82e6-179">This topic shows the prerequisites that must be in place before you can use the **Cost control** workspace.</span></span>

<span data-ttu-id="d82e6-180">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="d82e6-180">Additional resources</span></span>

- [<span data-ttu-id="d82e6-181">Werkgebied voor kostenbeheer</span><span class="sxs-lookup"><span data-stu-id="d82e6-181">Cost control workspace</span></span>](cost-control-workspace.md)
- [<span data-ttu-id="d82e6-182">Dimensiehiërarchie</span><span class="sxs-lookup"><span data-stu-id="d82e6-182">Dimension hierarchy</span></span>](dimension-hierarchy.md)
- [<span data-ttu-id="d82e6-183">Beveiliging instellen voor het inhoudpakket Kostprijsboekhouding</span><span class="sxs-lookup"><span data-stu-id="d82e6-183">Set up security for Cost accounting content pack</span></span>](../../dev-itpro/analytics/setup-security-cost-accounting-content-pack.md)
