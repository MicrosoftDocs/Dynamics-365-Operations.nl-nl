---
title: Toegangsrechten voor controllers voor kostenobjecten
description: Dit onderwerp bevat informatie over toegangsrechten voor controllers voor kostenobjecten.
author: AndersGirke
ms.date: 06/24/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CAMCostControlWorkspace, CAMParameters
audience: Application User
ms.reviewer: roschlom
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roschlom
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: fa8faf0f0f45f901151b3b20a1792b3d8f264fa6
ms.sourcegitcommit: 7d0cfb359a4abc7392ddb3f0b3e9539c40b7204d
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/14/2021
ms.locfileid: "5897619"
---
# <a name="access-rights-for-cost-object-controllers"></a><span data-ttu-id="25e00-103">Toegangsrechten voor controllers voor kostenobjecten</span><span class="sxs-lookup"><span data-stu-id="25e00-103">Access rights for cost object controllers</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="25e00-104">Het werkgebied **Kostenbeheer** is een centraal punt waar managers de prestaties van hun kostenobjecten kunnen bekijken.</span><span class="sxs-lookup"><span data-stu-id="25e00-104">The **Cost control** workspace is a central point where managers can view the performance of their cost objects.</span></span> <span data-ttu-id="25e00-105">In dit werkgebied kunnen managers gebruikmaken van gegevens over Kostprijsboekhouding, zelfs als ze geen kostenaccountants zijn.</span><span class="sxs-lookup"><span data-stu-id="25e00-105">This workspace lets managers consume Cost accounting data even though they aren't cost accountants.</span></span> <span data-ttu-id="25e00-106">Uit veiligheidsoverwegingen dienen managers alleen de gegevens over Kostprijsboekhouding te mogen zien die betrekking hebben op de specifieke kostenobjecten waarvoor ze verantwoordelijk zijn.</span><span class="sxs-lookup"><span data-stu-id="25e00-106">For security reasons, managers should be allowed to see only the Cost accounting data that is related to the specific cost objects that they are responsible for.</span></span>

<span data-ttu-id="25e00-107">Er zijn vier unieke rollen in Kostprijsboekhouding.</span><span class="sxs-lookup"><span data-stu-id="25e00-107">There are four unique roles in Cost accounting.</span></span>

| <span data-ttu-id="25e00-108">Rolnaam</span><span class="sxs-lookup"><span data-stu-id="25e00-108">Role name</span></span>               | <span data-ttu-id="25e00-109">Licentie</span><span class="sxs-lookup"><span data-stu-id="25e00-109">License</span></span>      |
|-------------------------|--------------|
| <span data-ttu-id="25e00-110">Manager van kostprijsboekhouding</span><span class="sxs-lookup"><span data-stu-id="25e00-110">Cost accounting manager</span></span> | <span data-ttu-id="25e00-111">Activiteit</span><span class="sxs-lookup"><span data-stu-id="25e00-111">Activity</span></span>     |
| <span data-ttu-id="25e00-112">Kostenaccountant</span><span class="sxs-lookup"><span data-stu-id="25e00-112">Cost accountant</span></span>         | <span data-ttu-id="25e00-113">Operations</span><span class="sxs-lookup"><span data-stu-id="25e00-113">Operations</span></span>   |
| <span data-ttu-id="25e00-114">Assistent kostenaccountant</span><span class="sxs-lookup"><span data-stu-id="25e00-114">Cost accountant clerk</span></span>   | <span data-ttu-id="25e00-115">Operations</span><span class="sxs-lookup"><span data-stu-id="25e00-115">Operations</span></span>   |
| <span data-ttu-id="25e00-116">Controller voor kostenobjecten</span><span class="sxs-lookup"><span data-stu-id="25e00-116">Cost object controller</span></span>  | <span data-ttu-id="25e00-117">Teamleden</span><span class="sxs-lookup"><span data-stu-id="25e00-117">Team members</span></span> |

<span data-ttu-id="25e00-118">In dit onderwerp wordt uitgelegd hoe de rol **Controller voor kostenobjecten** aan een manager kan worden toegewezen.</span><span class="sxs-lookup"><span data-stu-id="25e00-118">This topic explains how to assign the **Cost object controller** role to a manager.</span></span>

<span data-ttu-id="25e00-119">Wanneer de **Controller voor kostenobjecten** wordt toegewezen aan een manager, kan de manager de volgende taken uitvoeren:</span><span class="sxs-lookup"><span data-stu-id="25e00-119">When the **Cost object controller** role is assigned to a manager, the manager can perform the following tasks:</span></span>

- <span data-ttu-id="25e00-120">Toegang verkrijgen tot het werkgebied **Kostenbeheer** (in de client).</span><span class="sxs-lookup"><span data-stu-id="25e00-120">Access the **Cost control** workspace (in the client).</span></span>

    - <span data-ttu-id="25e00-121">Gedetailleerd bekijken van en weergaverechten verkrijgen voor de pagina's die ondersteuning bieden aan de detailanalyse-ervaring.</span><span class="sxs-lookup"><span data-stu-id="25e00-121">Drill through and have view access to the pages that support the drill-through experience.</span></span>

- <span data-ttu-id="25e00-122">Toegang verkrijgen tot het werkgebied **Kostenbeheer** (in de mobiele toepassing).</span><span class="sxs-lookup"><span data-stu-id="25e00-122">Access the **Cost control** workspace (in the mobile application).</span></span>

> [!NOTE]
> <span data-ttu-id="25e00-123">De rol **Controller voor kostenobjecten** bepaalt niet de kostenobjecten tot welke de gebruiker toegang kan krijgen en waarvoor gegevens kunnen worden weergegeven.</span><span class="sxs-lookup"><span data-stu-id="25e00-123">The **Cost object controller** role doesn't control which cost objects the user can access and view data for.</span></span> <span data-ttu-id="25e00-124">Beveiliging op rijniveau wordt geleverd via dimensiehiërarchieën en de hiërarchie van toegangslijsten.</span><span class="sxs-lookup"><span data-stu-id="25e00-124">Row-level security is provided via dimension hierarchies and the Access list hierarchy.</span></span>

## <a name="grant-access-rights"></a><span data-ttu-id="25e00-125">Toegangsrechten toekennen</span><span class="sxs-lookup"><span data-stu-id="25e00-125">Grant access rights</span></span>
<span data-ttu-id="25e00-126">In het volgende voorbeeld ziet u hoe een dimensiehiërarchie eruit kan zien.</span><span class="sxs-lookup"><span data-stu-id="25e00-126">The following example shows what a dimension hierarchy can look like.</span></span>

<span data-ttu-id="25e00-127">**Gegevens van dimensiehiërarchie**</span><span class="sxs-lookup"><span data-stu-id="25e00-127">**Dimension hierarchy details**</span></span>

| <span data-ttu-id="25e00-128">Naam van dimensiehiërarchie</span><span class="sxs-lookup"><span data-stu-id="25e00-128">Dimension hierarchy name</span></span> | <span data-ttu-id="25e00-129">Dimensie</span><span class="sxs-lookup"><span data-stu-id="25e00-129">Dimension</span></span>    | <span data-ttu-id="25e00-130">Naam van type dimensiehiërarchie</span><span class="sxs-lookup"><span data-stu-id="25e00-130">Dimension hierarchy type name</span></span>      | <span data-ttu-id="25e00-131">Hiërarchie van toegangslijsten</span><span class="sxs-lookup"><span data-stu-id="25e00-131">Access list hierarchy</span></span> |
|--------------------------|--------------|------------------------------------|-----------------------|
| <span data-ttu-id="25e00-132">Organisatie</span><span class="sxs-lookup"><span data-stu-id="25e00-132">Organization</span></span>             | <span data-ttu-id="25e00-133">Kostenplaatsen</span><span class="sxs-lookup"><span data-stu-id="25e00-133">Cost centers</span></span> | <span data-ttu-id="25e00-134">Hiërarchie dimensieclassificatie</span><span class="sxs-lookup"><span data-stu-id="25e00-134">Dimension classification hierarchy</span></span> | <span data-ttu-id="25e00-135">**Ja**</span><span class="sxs-lookup"><span data-stu-id="25e00-135">**Yes**</span></span>               |

<span data-ttu-id="25e00-136">U kunt het sneltabblad **Gebruikers** in de hiërarchieontwerper gebruiken om een of meer gebruikers-id's op elk knooppunt in te voegen.</span><span class="sxs-lookup"><span data-stu-id="25e00-136">You can use the **Users** FastTab in the hierarchy designer to insert one or more user IDs on each node.</span></span>

|             <span data-ttu-id="25e00-137">Knooppunten</span><span class="sxs-lookup"><span data-stu-id="25e00-137">Nodes</span></span>                 | <span data-ttu-id="25e00-138">Gebruikers</span><span class="sxs-lookup"><span data-stu-id="25e00-138">Users</span></span>            | <span data-ttu-id="25e00-139">Van dimensielid</span><span class="sxs-lookup"><span data-stu-id="25e00-139">From dimension member</span></span>     |   <span data-ttu-id="25e00-140">Tot dimensielid</span><span class="sxs-lookup"><span data-stu-id="25e00-140">To dimension member</span></span>   |
|-----------------------------------|------------------|---------------------------|-------------------------|
| <span data-ttu-id="25e00-141">Organisatie</span><span class="sxs-lookup"><span data-stu-id="25e00-141">Organization</span></span>                      | <span data-ttu-id="25e00-142">Benjamin, Claire</span><span class="sxs-lookup"><span data-stu-id="25e00-142">Benjamin, Claire</span></span> |                           |                         |
| <span data-ttu-id="25e00-143">&nbsp;&nbsp;Beheer</span><span class="sxs-lookup"><span data-stu-id="25e00-143">&nbsp;&nbsp;Admin</span></span>                 | <span data-ttu-id="25e00-144">april</span><span class="sxs-lookup"><span data-stu-id="25e00-144">April</span></span>            |                           |                         |
| <span data-ttu-id="25e00-145">&nbsp;&nbsp;&nbsp;&nbsp;Financiën</span><span class="sxs-lookup"><span data-stu-id="25e00-145">&nbsp;&nbsp;&nbsp;&nbsp;Finance</span></span>   | <span data-ttu-id="25e00-146">Alicia</span><span class="sxs-lookup"><span data-stu-id="25e00-146">Alicia</span></span>           | <span data-ttu-id="25e00-147">CC002</span><span class="sxs-lookup"><span data-stu-id="25e00-147">CC002</span></span>                     | <span data-ttu-id="25e00-148">CC003</span><span class="sxs-lookup"><span data-stu-id="25e00-148">CC003</span></span>                   |
|                                   |                  | <span data-ttu-id="25e00-149">CC007</span><span class="sxs-lookup"><span data-stu-id="25e00-149">CC007</span></span>                     | <span data-ttu-id="25e00-150">CC007</span><span class="sxs-lookup"><span data-stu-id="25e00-150">CC007</span></span>                   |
| <span data-ttu-id="25e00-151">&nbsp;&nbsp;&nbsp;&nbsp;HR</span><span class="sxs-lookup"><span data-stu-id="25e00-151">&nbsp;&nbsp;&nbsp;&nbsp;HR</span></span>        | <span data-ttu-id="25e00-152">Arnie</span><span class="sxs-lookup"><span data-stu-id="25e00-152">Arnie</span></span>            | <span data-ttu-id="25e00-153">CC001</span><span class="sxs-lookup"><span data-stu-id="25e00-153">CC001</span></span>                     | <span data-ttu-id="25e00-154">CC001</span><span class="sxs-lookup"><span data-stu-id="25e00-154">CC001</span></span>                   |
| <span data-ttu-id="25e00-155">&nbsp;&nbsp;Productie</span><span class="sxs-lookup"><span data-stu-id="25e00-155">&nbsp;&nbsp;Production</span></span>            | <span data-ttu-id="25e00-156">David</span><span class="sxs-lookup"><span data-stu-id="25e00-156">David</span></span>            |                           |                         |
| <span data-ttu-id="25e00-157">&nbsp;&nbsp;&nbsp;&nbsp;Verpakking</span><span class="sxs-lookup"><span data-stu-id="25e00-157">&nbsp;&nbsp;&nbsp;&nbsp;Packaging</span></span> | <span data-ttu-id="25e00-158">Ellen</span><span class="sxs-lookup"><span data-stu-id="25e00-158">Ellen</span></span>            | <span data-ttu-id="25e00-159">CC005</span><span class="sxs-lookup"><span data-stu-id="25e00-159">CC005</span></span>                     | <span data-ttu-id="25e00-160">CC005</span><span class="sxs-lookup"><span data-stu-id="25e00-160">CC005</span></span>                   |
| <span data-ttu-id="25e00-161">&nbsp;&nbsp;&nbsp;&nbsp;Assembleren</span><span class="sxs-lookup"><span data-stu-id="25e00-161">&nbsp;&nbsp;&nbsp;&nbsp;Assembly</span></span>  | <span data-ttu-id="25e00-162">Chris</span><span class="sxs-lookup"><span data-stu-id="25e00-162">Chris</span></span>            | <span data-ttu-id="25e00-163">CC006</span><span class="sxs-lookup"><span data-stu-id="25e00-163">CC006</span></span>                     | <span data-ttu-id="25e00-164">CC006</span><span class="sxs-lookup"><span data-stu-id="25e00-164">CC006</span></span>                   |

> [!NOTE]
> <span data-ttu-id="25e00-165">Kostenaccountants moeten worden toegewezen op het hoogste niveau van de hiërarchie, zodat ze alle vermeldingen in Kostprijsboekhouding kunnen zien.</span><span class="sxs-lookup"><span data-stu-id="25e00-165">Cost accountants should be assigned to the top level of the hierarchy, so that they can see all entries in Cost accounting.</span></span>

<span data-ttu-id="25e00-166">Voordat de hiërarchie van toegangslijsten en de beveiligingsinstellingen kunnen worden toegepast, moet de optie **Weergavetoegang voor dimensieleden voor kostenobject inschakelen** op **Ja** worden ingesteld op het tabblad **Algemeen** van de pagina **Parameters voor kostprijsboekhouding** (**Kostprijsboekhouding** > **Instellen** > **Parameters**).</span><span class="sxs-lookup"><span data-stu-id="25e00-166">Before the Access list hierarchy and its security settings can be applied, the **Enable view access for cost object dimension members** option must be set to **Yes** on the **General** tab of the **Cost accounting parameters** page (**Cost accounting** > **Setup** > **Parameters**).</span></span>

<span data-ttu-id="25e00-167">De instellingen voor de hiërarchie van toegangslijsten worden gebruikt voor het bepalen van de gegevens die in de volgende gebieden worden weergegeven:</span><span class="sxs-lookup"><span data-stu-id="25e00-167">The settings for the Access list hierarchy are used to control the data that is shown in following areas:</span></span>

- <span data-ttu-id="25e00-168">Werkgebied **Kostenbeheer** (in de client):</span><span class="sxs-lookup"><span data-stu-id="25e00-168">**Cost control** workspace (in the client):</span></span>

    - <span data-ttu-id="25e00-169">Gegevens op de pagina's die worden gebruikt voor detailanalyse</span><span class="sxs-lookup"><span data-stu-id="25e00-169">Data on the pages that are used for drill-through</span></span>

- <span data-ttu-id="25e00-170">Werkgebied **Kostenbeheer** (in de mobiele toepassing):</span><span class="sxs-lookup"><span data-stu-id="25e00-170">**Cost control** workspace (in the mobile application):</span></span>

    - <span data-ttu-id="25e00-171">Saldi in kaarten</span><span class="sxs-lookup"><span data-stu-id="25e00-171">Balances in cards</span></span>

- <span data-ttu-id="25e00-172">Microsoft Power BI:</span><span class="sxs-lookup"><span data-stu-id="25e00-172">Microsoft Power BI:</span></span>

    - <span data-ttu-id="25e00-173">Gegevens die worden weergegeven in Power BI-visualisaties</span><span class="sxs-lookup"><span data-stu-id="25e00-173">Data that is shown in Power BI visualizations</span></span>
    - <span data-ttu-id="25e00-174">Power BI-gegevensvisualisaties die zijn ingesloten in de Dynamics 365 Finance-client</span><span class="sxs-lookup"><span data-stu-id="25e00-174">Data Power BI visualizations that are embedded in the Dynamics 365 Finance client</span></span>

> [!IMPORTANT]
> - <span data-ttu-id="25e00-175">Voordat de hiërarchie van toegangslijsten van invloed kan zijn op gegevens in Power BI, moeten de hiërarchie van toegangslijsten en beveiliging op rijniveau in Power BI worden gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="25e00-175">Before the Access list hierarchy can affect data in Power BI, the Access list hierarchy and row-level security in Power BI must be paired.</span></span> <span data-ttu-id="25e00-176">Zie [Beveiliging instellen voor het inhoudpakket Kostprijsboekhouding](../../fin-ops-core/dev-itpro/analytics/setup-security-cost-accounting-content-pack.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="25e00-176">For more information, see [Set up security for Cost accounting content pack](../../fin-ops-core/dev-itpro/analytics/setup-security-cost-accounting-content-pack.md).</span></span>
> - <span data-ttu-id="25e00-177">Dit onderwerp bevat de vereisten waaraan moet worden voldaan voordat u het werkgebied **Kostenbeheer** kunt gebruiken.</span><span class="sxs-lookup"><span data-stu-id="25e00-177">This topic shows the prerequisites that must be in place before you can use the **Cost control** workspace.</span></span>

<span data-ttu-id="25e00-178">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="25e00-178">Additional resources</span></span>

- [<span data-ttu-id="25e00-179">Werkgebied voor kostenbeheer</span><span class="sxs-lookup"><span data-stu-id="25e00-179">Cost control workspace</span></span>](cost-control-workspace.md)
- [<span data-ttu-id="25e00-180">Dimensiehiërarchie</span><span class="sxs-lookup"><span data-stu-id="25e00-180">Dimension hierarchy</span></span>](dimension-hierarchy.md)
- [<span data-ttu-id="25e00-181">Beveiliging instellen voor het inhoudpakket Kostprijsboekhouding</span><span class="sxs-lookup"><span data-stu-id="25e00-181">Set up security for Cost accounting content pack</span></span>](../../fin-ops-core/dev-itpro/analytics/setup-security-cost-accounting-content-pack.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
