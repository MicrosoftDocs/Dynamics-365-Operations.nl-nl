---
title: Mobiel werkgebied Goedkeuring van inkooporder
description: In dit onderwerp vindt u informatie over het mobiele werkgebied Goedkeuring van inkooporders waarin u inkooporders kunt weergeven en op ze reageren via acties. U kunt bijvoorbeeld een inkooporder goedkeuren of afwijzen.
author: mkirknel
manager: tfehr
ms.date: 12/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchVendorPortalRequests
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations, Retail
ms.custom: 30211
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 68676fba895dcc91fd3dba065788f3be3a6e9ee4
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/13/2020
ms.locfileid: "4425612"
---
# <a name="purchase-order-approval-mobile-workspace"></a><span data-ttu-id="52e1c-104">Mobiel werkgebied Goedkeuring van inkooporder</span><span class="sxs-lookup"><span data-stu-id="52e1c-104">Purchase order approval mobile workspace</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="52e1c-105">Dit onderwerp biedt informatie over het mobiele werkgebied **Goedkeuring van inkooporders**.</span><span class="sxs-lookup"><span data-stu-id="52e1c-105">This topic provides information about the **Purchase order approval** mobile workspace.</span></span> <span data-ttu-id="52e1c-106">In deze werkruimte kunt u inkooporders weergeven en op ze reageren via acties.</span><span class="sxs-lookup"><span data-stu-id="52e1c-106">This workspace lets you view purchase orders and respond to them through actions.</span></span> <span data-ttu-id="52e1c-107">U kunt bijvoorbeeld een inkooporder goedkeuren of afwijzen.</span><span class="sxs-lookup"><span data-stu-id="52e1c-107">For example, you can approve or reject a purchase order.</span></span>
 
## <a name="overview"></a><span data-ttu-id="52e1c-108">Overzicht</span><span class="sxs-lookup"><span data-stu-id="52e1c-108">Overview</span></span> 
<span data-ttu-id="52e1c-109">Inkooporders die moet worden goedgekeurd doorlopen een goedkeuringswerkstroom.</span><span class="sxs-lookup"><span data-stu-id="52e1c-109">Purchase orders that requires approval go through an approval workflow.</span></span> <span data-ttu-id="52e1c-110">De werkstroom kan verschillende stappen omvatten, waarin één of meer mensen actie moeten ondernemen.</span><span class="sxs-lookup"><span data-stu-id="52e1c-110">The workflow can include various steps that require that one or more people take action.</span></span> <span data-ttu-id="52e1c-111">Een persoon moet bijvoorbeeld mogelijk een taak uitvoeren of de inkooporder goedkeuren.</span><span class="sxs-lookup"><span data-stu-id="52e1c-111">For example, a person might have to complete a task or approve the purchase order.</span></span> 

<span data-ttu-id="52e1c-112">In het mobiele werkgebied **Goedkeuring van inkooporders** kunt u eenvoudig op uw mobiele apparaat inkooporders bekijken en op ze reageren.</span><span class="sxs-lookup"><span data-stu-id="52e1c-112">The **Purchase order approval** mobile workspace lets you easily view and respond to purchase orders from your mobile device.</span></span> <span data-ttu-id="52e1c-113">Hier kunt u ook dezelfde werkstroomacties uitvoeren als vanuit de webclient.</span><span class="sxs-lookup"><span data-stu-id="52e1c-113">This workspace also lets you take the same workflow actions that you can take from the web client.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="52e1c-114">Vereisten</span><span class="sxs-lookup"><span data-stu-id="52e1c-114">Prerequisites</span></span>
<span data-ttu-id="52e1c-115">De vereisten verschillen, afhankelijk van de versie van Supply Chain Management die voor uw organisatie is geïmplementeerd.</span><span class="sxs-lookup"><span data-stu-id="52e1c-115">The prerequisites vary, depending on the version of Supply Chain Management that has been deployed for your organization.</span></span>

### <a name="prerequisites-if-you-use-supply-chain-management"></a><span data-ttu-id="52e1c-116">Vereisten als u Supply Chain Management gebruikt</span><span class="sxs-lookup"><span data-stu-id="52e1c-116">Prerequisites if you use Supply Chain Management</span></span> 
<span data-ttu-id="52e1c-117">Als Supply Chain Management is geïmplementeerd in uw organisatie, moet de systeembeheerder het mobiele werkgebied **Goedkeuring van inkooporder** publiceren.</span><span class="sxs-lookup"><span data-stu-id="52e1c-117">If Supply Chain Management has been deployed for your organization, the system administrator must publish the **Purchase order approval** mobile workspace.</span></span> <span data-ttu-id="52e1c-118">Zie voor meer informatie [Een mobiel werkgebied publiceren](../../dev-itpro/mobile-apps/publish-mobile-workspace.md).</span><span class="sxs-lookup"><span data-stu-id="52e1c-118">For instructions, see [Publish a mobile workspace](../../dev-itpro/mobile-apps/publish-mobile-workspace.md).</span></span>

### <a name="prerequisites-if-you-use-microsoft-dynamics-365-for-operations-version-1611-with-platform-update-3-or-later"></a><span data-ttu-id="52e1c-119">Vereisten als u versie Microsoft Dynamics 365 for Operations 1611 met platformupdate 3 of hoger gebruikt</span><span class="sxs-lookup"><span data-stu-id="52e1c-119">Prerequisites if you use Microsoft Dynamics 365 for Operations version 1611 with Platform update 3 or later</span></span>
<span data-ttu-id="52e1c-120">Als Microsoft Dynamics 365 for Operations versie 1611, met platformupdate 3 of hoger voor uw organisatie is geïmplementeerd, moet de systeembeheerder de volgende vereisten uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="52e1c-120">If Microsoft Dynamics 365 for Operations version 1611 with Platform update 3 or later has been deployed for your organization, the system administrator must complete the following prerequisites.</span></span> 

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="52e1c-121">Vereiste</span><span class="sxs-lookup"><span data-stu-id="52e1c-121">Prerequisite</span></span></th>
<th><span data-ttu-id="52e1c-122">Rol</span><span class="sxs-lookup"><span data-stu-id="52e1c-122">Role</span></span></th>
<th><span data-ttu-id="52e1c-123">Omschrijving</span><span class="sxs-lookup"><span data-stu-id="52e1c-123">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="52e1c-124">KB 4017918 implementeren.</span><span class="sxs-lookup"><span data-stu-id="52e1c-124">Implement KB 4017918.</span></span></td>
<td><span data-ttu-id="52e1c-125">Systeembeheerder</span><span class="sxs-lookup"><span data-stu-id="52e1c-125">System administrator</span></span></td>
<td><span data-ttu-id="52e1c-126">KB 4017918 is een X++-update of metagegevenshotfix die het mobiele werkgebied <strong>Goedkeuring van inkooporders</strong> bevat.</span><span class="sxs-lookup"><span data-stu-id="52e1c-126">KB 4017918 is an X++ update or metadata hotfix that contains the <strong>Purchase order approval</strong> mobile workspace.</span></span> <span data-ttu-id="52e1c-127">Uw systeembeheerder moet de volgende stappen uitvoeren voor het implementeren van KB 4017918.</span><span class="sxs-lookup"><span data-stu-id="52e1c-127">To implement KB 4017918, your system administrator must follow these steps.</span></span>
<ol>
<li><span data-ttu-id="52e1c-128"><a href="../../dev-itpro/migration-upgrade/download-hotfix-lcs.md">Metagegevens-hotfix downloaden uit Microsoft Dynamics Lifecycle Services (LCS)</a>.</span><span class="sxs-lookup"><span data-stu-id="52e1c-128"><a href="../../dev-itpro/migration-upgrade/download-hotfix-lcs.md">Download the metadata hotfix from Microsoft Dynamics Lifecycle Services (LCS)</a>.</span></span></li>
<li><span data-ttu-id="52e1c-129"><a href="../../dev-itpro/migration-upgrade/install-metadata-hotfix-package.md">De metagegevenshotfix installeren</a>.</span><span class="sxs-lookup"><span data-stu-id="52e1c-129"><a href="../../dev-itpro/migration-upgrade/install-metadata-hotfix-package.md">Install the metadata hotfix</a>.</span></span></li>
<li><span data-ttu-id="52e1c-130"><a href="../../dev-itpro/deployment/create-apply-deployable-package.md">Een implementeerbaar pakket maken</a> dat de ApplicationSuite en <strong>SCMMobile</strong>-modellen bevat en het implementeerbare pakket vervolgens uploaden naar LCS.</span><span class="sxs-lookup"><span data-stu-id="52e1c-130"><a href="../../dev-itpro/deployment/create-apply-deployable-package.md">Create a deployable package</a> that contains the <strong>SCMMobile</strong> model, and then upload the deployable package to LCS.</span></span></li>
<li><span data-ttu-id="52e1c-131"><a href="../../dev-itpro/deployment/apply-deployable-package-system.md">Het implementeerbare pakket toepassen</a></span><span class="sxs-lookup"><span data-stu-id="52e1c-131"><a href="../../dev-itpro/deployment/apply-deployable-package-system.md">Apply the deployable package</a>.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="52e1c-132">Publiceer het werkgebied <strong>Goedkeuring van inkooporders</strong>.</span><span class="sxs-lookup"><span data-stu-id="52e1c-132">Publish the <strong>Purchase order approval</strong> mobile workspace.</span></span></td>
<td><span data-ttu-id="52e1c-133">Systeembeheerder</span><span class="sxs-lookup"><span data-stu-id="52e1c-133">System administrator</span></span></td>
<td><span data-ttu-id="52e1c-134">Zie <a href="../../dev-itpro/mobile-apps/publish-mobile-workspace.md">Mobiel werkgebied publiceren</a>.</span><span class="sxs-lookup"><span data-stu-id="52e1c-134">See <a href="../../dev-itpro/mobile-apps/publish-mobile-workspace.md">Publish a mobile workspace</a>.</span></span></td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-mobile-app"></a><span data-ttu-id="52e1c-135">De mobiele app downloaden en installeren</span><span class="sxs-lookup"><span data-stu-id="52e1c-135">Download and install the mobile app</span></span>
<span data-ttu-id="52e1c-136">Download en installeer de mobiele Finance and Operations-app:</span><span class="sxs-lookup"><span data-stu-id="52e1c-136">Download and install the Finance and Operations mobile app:</span></span>

- [<span data-ttu-id="52e1c-137">Voor Android-telefoons</span><span class="sxs-lookup"><span data-stu-id="52e1c-137">For Android phones</span></span>](https://go.microsoft.com/fwlink/?linkid=850662)
- [<span data-ttu-id="52e1c-138">Voor iPhones</span><span class="sxs-lookup"><span data-stu-id="52e1c-138">For iPhones</span></span>](https://go.microsoft.com/fwlink/?linkid=850663)


## <a name="sign-in-to-the-mobile-app"></a><span data-ttu-id="52e1c-139">Aanmelden bij de mobiele app</span><span class="sxs-lookup"><span data-stu-id="52e1c-139">Sign in to the mobile app</span></span>

1. <span data-ttu-id="52e1c-140">Start de app op uw mobiele apparaat.</span><span class="sxs-lookup"><span data-stu-id="52e1c-140">Start the app on your mobile device.</span></span>
2. <span data-ttu-id="52e1c-141">Voer uw URL voor Microsoft Dynamics 365 in.</span><span class="sxs-lookup"><span data-stu-id="52e1c-141">Enter your Microsoft Dynamics 365 URL.</span></span>
3. <span data-ttu-id="52e1c-142">De eerste keer dat u zich aanmeldt, wordt u gevraagd uw gebruikersnaam en wachtwoord in te voeren.</span><span class="sxs-lookup"><span data-stu-id="52e1c-142">The first time that you sign in, you're prompted for your user name and password.</span></span> <span data-ttu-id="52e1c-143">Voer uw referenties in.</span><span class="sxs-lookup"><span data-stu-id="52e1c-143">Enter your credentials.</span></span>
4. <span data-ttu-id="52e1c-144">Nadat u zich hebt aangemeld, worden de beschikbare werkgebieden voor uw bedrijf weergegeven.</span><span class="sxs-lookup"><span data-stu-id="52e1c-144">After you sign in, the available workspaces for your company are shown.</span></span> <span data-ttu-id="52e1c-145">Houd er rekening mee dat als uw systeembeheerder later een nieuw werkgebied publiceert, u de lijst met mobiele werkgebieden moet vernieuwen.</span><span class="sxs-lookup"><span data-stu-id="52e1c-145">Note that if your system administrator publishes a new workspace later, you will have to refresh the list of mobile workspaces.</span></span>

![Werkgebied Goedkeuring van inkooporders in de lijst van beschikbare werkgebieden](./media/po-workspaces.png)

## <a name="view-orders-that-are-assigned-to-you"></a><span data-ttu-id="52e1c-147">Orders weergeven die aan u zijn toegewezen</span><span class="sxs-lookup"><span data-stu-id="52e1c-147">View orders that are assigned to you</span></span>
1. <span data-ttu-id="52e1c-148">Selecteer op uw mobiele apparaat het werkgebied **Goedkeuring van inkooporders**.</span><span class="sxs-lookup"><span data-stu-id="52e1c-148">On your mobile device, select the **Purchase order approval** workspace.</span></span>
2. <span data-ttu-id="52e1c-149">Selecteer **Orders die aan mij zijn toegewezen** om alle inkooporders weer te geven waarvoor u een actie moet uitvoeren in de werkstroom Goedkeuring van inkooporders.</span><span class="sxs-lookup"><span data-stu-id="52e1c-149">Select **Orders assigned to me** to view all the purchase orders for which you've been asked to take action in the purchase order approval workflow.</span></span>
3. <span data-ttu-id="52e1c-150">Selecteer een order.</span><span class="sxs-lookup"><span data-stu-id="52e1c-150">Select an order.</span></span> <span data-ttu-id="52e1c-151">Op de pagina **Ordergegevens** ziet u de koptekst en de regels van de order.</span><span class="sxs-lookup"><span data-stu-id="52e1c-151">On the **Order details** page, you will see the order header information and lines.</span></span> <span data-ttu-id="52e1c-152">Ook vindt u hier de richtlijnen van de werkstroomtaak.</span><span class="sxs-lookup"><span data-stu-id="52e1c-152">You can also find guidelines from the workflow task.</span></span>
4. <span data-ttu-id="52e1c-153">Selecteer **Boekhoudingsverdelingen** en open de pagina **Koptekst boekhoudingsverdeling**.</span><span class="sxs-lookup"><span data-stu-id="52e1c-153">Select **Accounting distributions** to open the **Header accounting distributions** page.</span></span>
5. <span data-ttu-id="52e1c-154">Ga terug naar de pagina **Ordergegevens** en selecteer een regel.</span><span class="sxs-lookup"><span data-stu-id="52e1c-154">Return to the **Order details** page, and select a line.</span></span> <span data-ttu-id="52e1c-155">Vanuit de orderregelgegevens kunt u ook de boekhoudingsverdelingen voor de specifieke regel bekijken.</span><span class="sxs-lookup"><span data-stu-id="52e1c-155">From the order line details, you can also explore the line-specific accounting distributions.</span></span>

## <a name="complete-an-action-on-the-purchase-order"></a><span data-ttu-id="52e1c-156">Een actie op de inkooporder uitvoeren</span><span class="sxs-lookup"><span data-stu-id="52e1c-156">Complete an action on the purchase order</span></span>
<span data-ttu-id="52e1c-157">Nadat u de inkooporder die aan u is toegewezen hebt bekeken en de workflowinstructies hebt gelezen, zou u gereed moeten zijn om actie te ondernemen.</span><span class="sxs-lookup"><span data-stu-id="52e1c-157">After you've viewed the purchase order that is assigned to you and read the workflow instructions, you should be ready to take action.</span></span>

1. <span data-ttu-id="52e1c-158">Selecteer op uw mobiele apparaat het werkgebied **Goedkeuring van inkooporders**.</span><span class="sxs-lookup"><span data-stu-id="52e1c-158">On your mobile device, select the **Purchase order approval** workspace.</span></span>
2. <span data-ttu-id="52e1c-159">Selecteer **Orders die aan mij zijn toegewezen** om alle inkooporders weer te geven waarvoor u een actie moet uitvoeren in de werkstroom Goedkeuring van inkooporders.</span><span class="sxs-lookup"><span data-stu-id="52e1c-159">Select **Orders assigned to me** to view all the purchase orders for which you've been asked to take action in the purchase order approval workflow.</span></span>
3. <span data-ttu-id="52e1c-160">Selecteer een order en geef de detailpagina weer.</span><span class="sxs-lookup"><span data-stu-id="52e1c-160">Select an order, and view the details page.</span></span>
4. <span data-ttu-id="52e1c-161">Selecteer **acties** om de beschikbare acties weer te geven.</span><span class="sxs-lookup"><span data-stu-id="52e1c-161">Select **Actions** to show the available actions.</span></span> <span data-ttu-id="52e1c-162">Welke acties beschikbaar zijn, is afhankelijk van de taak die aan u is toegewezen.</span><span class="sxs-lookup"><span data-stu-id="52e1c-162">The actions that are available depend on the task that has been assigned to you.</span></span>

    | <span data-ttu-id="52e1c-163">Taakactie</span><span class="sxs-lookup"><span data-stu-id="52e1c-163">Task action</span></span>    | <span data-ttu-id="52e1c-164">Goedkeuringsactie</span><span class="sxs-lookup"><span data-stu-id="52e1c-164">Approval action</span></span>  |
    |----------------|------------------|
    | <span data-ttu-id="52e1c-165">Volledig</span><span class="sxs-lookup"><span data-stu-id="52e1c-165">Complete</span></span>       | <span data-ttu-id="52e1c-166">Goedkeuren</span><span class="sxs-lookup"><span data-stu-id="52e1c-166">Approve</span></span>          |
    | <span data-ttu-id="52e1c-167">Retour</span><span class="sxs-lookup"><span data-stu-id="52e1c-167">Return</span></span>         | <span data-ttu-id="52e1c-168">Afwijzen</span><span class="sxs-lookup"><span data-stu-id="52e1c-168">Reject</span></span>           |
    | <span data-ttu-id="52e1c-169">Wijziging aanvraag</span><span class="sxs-lookup"><span data-stu-id="52e1c-169">Request change</span></span> | <span data-ttu-id="52e1c-170">Wijziging aanvraag</span><span class="sxs-lookup"><span data-stu-id="52e1c-170">Request change</span></span>   |
    | <span data-ttu-id="52e1c-171">Machtigen</span><span class="sxs-lookup"><span data-stu-id="52e1c-171">Delegate</span></span>       | <span data-ttu-id="52e1c-172">Machtigen</span><span class="sxs-lookup"><span data-stu-id="52e1c-172">Delegate</span></span>         |

5. <span data-ttu-id="52e1c-173">Selecteer de gewenste actie.</span><span class="sxs-lookup"><span data-stu-id="52e1c-173">Select the appropriate action.</span></span>
6. <span data-ttu-id="52e1c-174">Voer op de pagina **Taak voltooien** een opmerking in.</span><span class="sxs-lookup"><span data-stu-id="52e1c-174">On the **Complete task** page, enter a comment.</span></span> <span data-ttu-id="52e1c-175">Houd er rekening mee dat als u de actie **Delegeren** kiest, u een gebruiker moet selecteren aan wie de taak wordt gedelegeerd.</span><span class="sxs-lookup"><span data-stu-id="52e1c-175">Note that if you select the **Delegate** action, you must select a user to delegate the task to.</span></span>
7. <span data-ttu-id="52e1c-176">Selecteer **Gereed**.</span><span class="sxs-lookup"><span data-stu-id="52e1c-176">Select **Done**.</span></span> <span data-ttu-id="52e1c-177">Nadat u uw werkruimte hebt vernieuwd, staat de inkooporder niet meer in de lijst.</span><span class="sxs-lookup"><span data-stu-id="52e1c-177">After you refresh your workspace, the purchase order will no longer be in your list.</span></span> 
