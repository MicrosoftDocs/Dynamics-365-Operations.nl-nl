---
title: Startpagina mobiele app
description: In dit onderwerp wordt de mobiele app voor Finance and Operations (Dynamics 365) beschreven en worden koppelingen verstrekt naar bronnen die u kunnen helpen deze toe te passen in uw organisatie.
author: ChrisGarty
manager: AnnBe
ms.date: 01/22/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.custom: 272853
ms.assetid: c99f818f-27b3-4e45-92b4-74272dad0e17
ms.search.region: Global
ms.author: cgarty
ms.dyn365.ops.version: Platform update 4
ms.search.validFrom: 2017-02-28
ms.openlocfilehash: 65254ac09a01e1ed2486d8f1324f564b3cd800c6
ms.sourcegitcommit: 9a053d020e672a87b660f27009a492544e6c81a9
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 07/30/2020
ms.locfileid: "3641467"
---
# <a name="mobile-app-home-page"></a><span data-ttu-id="1553b-103">Startpagina mobiele app</span><span class="sxs-lookup"><span data-stu-id="1553b-103">Mobile app home page</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1553b-104">In dit onderwerp wordt de mobiele app voor **Finance and Operations (Dynamics 365)** beschreven en worden koppelingen verstrekt naar bronnen die u kunnen helpen deze toe te passen in uw organisatie.</span><span class="sxs-lookup"><span data-stu-id="1553b-104">This topic describes the **Finance and Operations (Dynamics 365)** mobile app and provides links to resources that can help you implement it in your organization.</span></span>

<a name="overview"></a><span data-ttu-id="1553b-105">Overzicht</span><span class="sxs-lookup"><span data-stu-id="1553b-105">Overview</span></span>
--------

<span data-ttu-id="1553b-106">De mobiele app stelt uw organisatie in staat de eigen bedrijfsprocessen beschikbaar te maken op mobiele apparaten.</span><span class="sxs-lookup"><span data-stu-id="1553b-106">The mobile app enables your organization to make its business processes available on mobile devices.</span></span> <span data-ttu-id="1553b-107">Nadat uw IT-beheerder de mobiele werkgebieden voor uw organisatie heeft ingeschakeld, kunnen gebruikers zich aanmelden bij de app en direct beginnen met het uitvoeren van bedrijfsprocessen vanaf hun mobiele apparaten.</span><span class="sxs-lookup"><span data-stu-id="1553b-107">After your IT admin enables the mobile workspaces for your organization, users can sign in to the app and immediately begin to run business processes from their mobile devices.</span></span> <span data-ttu-id="1553b-108">De mobiele app omvat de volgende functies waarmee de productiviteit kan worden verhoogd:</span><span class="sxs-lookup"><span data-stu-id="1553b-108">The mobile app includes the following features that can help increase productivity:</span></span>

- <span data-ttu-id="1553b-109">Gebruikers kunnen zakelijke gegevens bekijken, bewerken en hierop reageren, zelfs als zij niet voortdurend een netwerkverbinding hebben of als hun mobiele apparaten volledig offline zijn.</span><span class="sxs-lookup"><span data-stu-id="1553b-109">Users can view, edit, and act on business data, even if they have intermittent network connectivity or their mobile devices are completely offline.</span></span> <span data-ttu-id="1553b-110">Als een apparaat de netwerkverbinding herstelt, worden offline gegevensbewerkingen automatisch gesynchroniseerd.</span><span class="sxs-lookup"><span data-stu-id="1553b-110">When a device reestablishes a network connection, offline data operations are automatically synchronized.</span></span>
- <span data-ttu-id="1553b-111">IT-beheerders of ontwikkelaars kunnen mobiele werkgebieden bouwen en publiceren die zijn op maat zijn gemaakt voor hun organisatie.</span><span class="sxs-lookup"><span data-stu-id="1553b-111">IT admins or developers can build and publish mobile workspaces that have been tailored to their organization.</span></span> <span data-ttu-id="1553b-112">De app gebruikt uw bestaande code-elementen.</span><span class="sxs-lookup"><span data-stu-id="1553b-112">The app uses your existing code assets.</span></span> <span data-ttu-id="1553b-113">Daarom hoeft u uw validatieprocedures, bedrijfslogica of beveiligingsconfiguratie niet opnieuw te implementeren.</span><span class="sxs-lookup"><span data-stu-id="1553b-113">Therefore, you don't have to re-implement your validation procedures, business logic, or security configuration.</span></span>
- <span data-ttu-id="1553b-114">IT-beheerders of ontwikkelaars kunnen op eenvoudige wijze mobiele werkgebieden ontwerpen met behulp van de ontwerper voor werkgebieden, die werkt via aanwijzen en klikken, die deel uitmaakt van de webclient.</span><span class="sxs-lookup"><span data-stu-id="1553b-114">IT admins or developers can easily design mobile workspaces by using the point-and-click workspace designer that is included with the web client.</span></span>
- <span data-ttu-id="1553b-115">IT-beheerders of ontwikkelaars kunnen desgewenst de offline mogelijkheden van werkgebieden optimaliseren met behulp van het raamwerk voor uitbreiding van bedrijfslogica.</span><span class="sxs-lookup"><span data-stu-id="1553b-115">IT admins or developers can optionally optimize the offline capabilities of workspaces by using the Business logic extensibility framework.</span></span> <span data-ttu-id="1553b-116">Omdat gegevens nog steeds worden verwerkt terwijl een apparaat offline is, blijven uw mobiele scenario's rijk en vloeiend, zelfs als apparaten geen constante netwerkverbinding hebben.</span><span class="sxs-lookup"><span data-stu-id="1553b-116">Because data continues to be processed while a device is offline, your mobile scenarios remain rich and fluid, even if devices don't have constant network connectivity.</span></span>

## <a name="elements-of-the-mobile-app"></a><span data-ttu-id="1553b-117">Elementen van de mobiele app</span><span class="sxs-lookup"><span data-stu-id="1553b-117">Elements of the mobile app</span></span>
<span data-ttu-id="1553b-118">Navigeren in de mobiele app omvat vier basisconcepten: het dashboard, de werkgebieden, de pagina's en de acties.</span><span class="sxs-lookup"><span data-stu-id="1553b-118">Navigation in the mobile app consists of four basic concepts: the dashboard, workspaces, pages, and actions.</span></span> 

<span data-ttu-id="1553b-119">[![Navigatieconcepten in de mobiele app](./media/mobilephoneapp1-1024x536.png)](./media/mobilephoneapp1.png)</span><span class="sxs-lookup"><span data-stu-id="1553b-119">[![Navigation concepts in the mobile app](./media/mobilephoneapp1-1024x536.png)](./media/mobilephoneapp1.png)</span></span>

1. <span data-ttu-id="1553b-120">Wanneer u de app start, gaat u naar het **dashboard**.</span><span class="sxs-lookup"><span data-stu-id="1553b-120">When you start the app, you go to the **dashboard**.</span></span>
2. <span data-ttu-id="1553b-121">Op het dashboard ziet u een lijst met **werkgebieden** die zijn gepubliceerd.</span><span class="sxs-lookup"><span data-stu-id="1553b-121">On the dashboard, you can see a list of **workspaces** that have been published.</span></span>
3. <span data-ttu-id="1553b-122">In elk werkgebied ziet u een lijst met **pagina's** die beschikbaar zijn voor dat werkgebied.</span><span class="sxs-lookup"><span data-stu-id="1553b-122">In each workspace, you can see a list of **pages** that are available for that workspace.</span></span>
4. <span data-ttu-id="1553b-123">Nadat u op een pagina bent aangekomen, kunt u verschillende acties uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="1553b-123">After you're on a page, you can perform several actions.</span></span> <span data-ttu-id="1553b-124">Hieronder vindt u enkele voorbeelden:</span><span class="sxs-lookup"><span data-stu-id="1553b-124">Here are some examples:</span></span>

    - <span data-ttu-id="1553b-125">Gedetailleerde gegevens bekijken.</span><span class="sxs-lookup"><span data-stu-id="1553b-125">View detailed data.</span></span>
    - <span data-ttu-id="1553b-126">Naar andere pagina's navigeren voor gerelateerde gegevens, zoals entiteitsdetails of regels.</span><span class="sxs-lookup"><span data-stu-id="1553b-126">Navigate to other pages for related data, such as entity details or lines.</span></span>
    - <span data-ttu-id="1553b-127">Een overzicht van **acties** bekijken, die beschikbaar zijn voor die pagina.</span><span class="sxs-lookup"><span data-stu-id="1553b-127">See a list of **actions** that are available for that page.</span></span> <span data-ttu-id="1553b-128">Via acties kunt u gegevens maken of bestaande gegevens bewerken.</span><span class="sxs-lookup"><span data-stu-id="1553b-128">Actions let you create or edit existing data.</span></span>

## <a name="implementation-process"></a><span data-ttu-id="1553b-129">Implementatieproces</span><span class="sxs-lookup"><span data-stu-id="1553b-129">Implementation process</span></span>
<span data-ttu-id="1553b-130">In de volgende afbeelding ziet u het proces voor de implementatie van zowel mobiele werkgebieden die door Microsoft worden geleverd als ook aangepaste mobiele werkgebieden.</span><span class="sxs-lookup"><span data-stu-id="1553b-130">The following illustration shows the process for implementing both mobile workspaces that are provided by Microsoft and custom mobile workspaces.</span></span> 

<span data-ttu-id="1553b-131">[![Implementatieproces voor mobiele apps](./media/Mobile-implementation-process-5.png)](./media/Mobile-implementation-process-5.png)</span><span class="sxs-lookup"><span data-stu-id="1553b-131">[![Mobile apps implementation process](./media/Mobile-implementation-process-5.png)](./media/Mobile-implementation-process-5.png)</span></span>

<span data-ttu-id="1553b-132">De volgende tabel bevat koppelingen naar resources die u kunnen helpen bij de implementatie van zowel mobiele werkgebieden die door Microsoft worden geleverd als ook aangepaste mobiele werkgebieden.</span><span class="sxs-lookup"><span data-stu-id="1553b-132">The following table includes links to resources that can help you implement both mobile workspaces that are provided by Microsoft and custom mobile workspaces.</span></span> <span data-ttu-id="1553b-133">De nummers in de eerste kolom komen overeen met de genummerde stappen in de bovenstaande afbeelding.</span><span class="sxs-lookup"><span data-stu-id="1553b-133">The numbers in the first column correspond to the numbered steps in the previous illustration.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="1553b-134">Stap</span><span class="sxs-lookup"><span data-stu-id="1553b-134">Step</span></span></th>
<th><span data-ttu-id="1553b-135">Rol</span><span class="sxs-lookup"><span data-stu-id="1553b-135">Role</span></span></th>
<th><span data-ttu-id="1553b-136">Actie</span><span class="sxs-lookup"><span data-stu-id="1553b-136">Action</span></span></th>
<th><span data-ttu-id="1553b-137">Bronnen die u helpen de actie te voltooien</span><span class="sxs-lookup"><span data-stu-id="1553b-137">Resources to help you complete the action</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1553b-138">1</span><span class="sxs-lookup"><span data-stu-id="1553b-138">1</span></span></td>
<td><span data-ttu-id="1553b-139">Systeembeheerder</span><span class="sxs-lookup"><span data-stu-id="1553b-139">System administrator</span></span></td>
<td><span data-ttu-id="1553b-140">Implementeer de Finance and Operations-app in uw organisatie.</span><span class="sxs-lookup"><span data-stu-id="1553b-140">Implement the Finance and Operations app in your organization.</span></span></td>
<td><ul><li><span data-ttu-id="1553b-141">Als u nog geen versie van Microsoft Dynamics 365 hebt geïmplementeerd, raadpleeg dan <a href="../deployment/deploy-demo-environment.md">Een demo-omgeving implementeren</a>.</span><span class="sxs-lookup"><span data-stu-id="1553b-141">If you haven&#39;t yet deployed a version of Microsoft Dynamics 365, see <a href="../deployment/deploy-demo-environment.md">Deploy a demo environment</a>.</span></span></li><li><span data-ttu-id="1553b-142">Een lijst met mobiele werkgebieden die u kunt gebruiken, vindt u in <a href="mobile-workspaces-released.md">Recentelijk gepubliceerde mobiele werkgebieden</a>.</span><span class="sxs-lookup"><span data-stu-id="1553b-142">To see a list of mobile workspaces that can be used, see <a href="mobile-workspaces-released.md">Mobile workspaces recently released</a>.</span></span></li></ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1553b-143">2</span><span class="sxs-lookup"><span data-stu-id="1553b-143">2</span></span></td>
<td><span data-ttu-id="1553b-144">Systeembeheerder</span><span class="sxs-lookup"><span data-stu-id="1553b-144">System administrator</span></span></td>
<td><span data-ttu-id="1553b-145"><strong>Als u Microsoft Dynamics 365 for Operations versie 1611 gebruikt:</strong> Download en installeer KB's waarmee de mobiele werkgebieden die door Microsoft worden geleverd worden ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="1553b-145"><strong>If you&#39;re using Microsoft Dynamics 365 for Operations version 1611:</strong> Download and install KBs that enable the mobile workspaces that are provided by Microsoft.</span></span></td>
<td><span data-ttu-id="1553b-146">Zie de volgende onderwerpen voor meer informatie:</span><span class="sxs-lookup"><span data-stu-id="1553b-146">See the following topics for more information:</span></span>
<ul>

<li><span data-ttu-id="1553b-147"><a href="../../../finance/cost-accounting/cost-controlling-mobile-workspace.md">Mobiel werkgebied voor kostenbeheer</a></span><span class="sxs-lookup"><span data-stu-id="1553b-147"><a href="../../../finance/cost-accounting/cost-controlling-mobile-workspace.md">Cost controlling mobile workspaces</a></span></span></li>
<li><span data-ttu-id="1553b-148"><a href="../../../supply-chain/inventory/inventory-on-hand-mobile-workspace.md">Mobiel werkgebied voorhanden voorraad</a></span><span class="sxs-lookup"><span data-stu-id="1553b-148"><a href="../../../supply-chain/inventory/inventory-on-hand-mobile-workspace.md">Inventory on-hand mobile workspace</a></span></span></li>
<li><span data-ttu-id="1553b-149"><a href="../../../supply-chain/sales-marketing/sales-orders-mobile-workspace.md">Mobiele werkbieden voor verkooporders</a></span><span class="sxs-lookup"><span data-stu-id="1553b-149"><a href="../../../supply-chain/sales-marketing/sales-orders-mobile-workspace.md">Sales orders mobile workspaces</a></span></span></li>
<li><span data-ttu-id="1553b-150"><a href="../../../supply-chain/procurement/vendor-collaboration-mobile-workspace.md">Mobiel werkgebied voor leverancierssamenwerking</a></span><span class="sxs-lookup"><span data-stu-id="1553b-150"><a href="../../../supply-chain/procurement/vendor-collaboration-mobile-workspace.md">Vendor collaboration mobile workspace</a></span></span></li>
<li><span data-ttu-id="1553b-151"><a href="../../../finance/project-management/project-time-entry-mobile-workspace.md">Tijdinvoer voor project voor mobiel werkgebied</a></span><span class="sxs-lookup"><span data-stu-id="1553b-151"><a href="../../../finance/project-management/project-time-entry-mobile-workspace.md">Project time entry mobile workspace</a></span></span></li>
<li><span data-ttu-id="1553b-152"><a href="../../../finance/expense-management/expense-management-mobile-workspace.md">Mobiel werkgebied voor onkostenbeheer</a></span><span class="sxs-lookup"><span data-stu-id="1553b-152"><a href="../../../finance/expense-management/expense-management-mobile-workspace.md">Expense management mobile workspace</a></span></span></li>

</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1553b-153">3</span><span class="sxs-lookup"><span data-stu-id="1553b-153">3</span></span></td>
<td><span data-ttu-id="1553b-154">Systeembeheerder</span><span class="sxs-lookup"><span data-stu-id="1553b-154">System administrator</span></span></td>
<td><span data-ttu-id="1553b-155">Publiceer de mobiele werkgebieden die worden geleverd door Microsoft.</span><span class="sxs-lookup"><span data-stu-id="1553b-155">Publish the mobile workspaces that are provided by Microsoft.</span></span></td>
<td><span data-ttu-id="1553b-156"><a href="publish-mobile-workspace.md">Een mobiel werkgebied publiceren</a>
</span><span class="sxs-lookup"><span data-stu-id="1553b-156"><a href="publish-mobile-workspace.md">Publish a mobile workspace</a>
</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1553b-157">4</span><span class="sxs-lookup"><span data-stu-id="1553b-157">4</span></span></td>
<td><span data-ttu-id="1553b-158">Ontwikkelaar of onafhankelijke softwareleveranciers (Independent software vendors - ISV's)</span><span class="sxs-lookup"><span data-stu-id="1553b-158">Developer or independent software vendor (ISV)</span></span></td>
<td><span data-ttu-id="1553b-159">Gebruik het mobiele plaftorm om aangepaste mobiele werkgebieden te maken.</span><span class="sxs-lookup"><span data-stu-id="1553b-159">Use the mobile platform to create custom mobile workspaces.</span></span></td>
<td><span data-ttu-id="1553b-160"><a href="platform/mobile-platform-home-page.md">Mobiel platform</a></span><span class="sxs-lookup"><span data-stu-id="1553b-160"><a href="platform/mobile-platform-home-page.md">Mobile platform</a></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1553b-161">5</span><span class="sxs-lookup"><span data-stu-id="1553b-161">5</span></span></td>
<td><span data-ttu-id="1553b-162">ISV</span><span class="sxs-lookup"><span data-stu-id="1553b-162">ISV</span></span></td>
<td><span data-ttu-id="1553b-163">Maak een implementeerbaar pakket met aangepaste mobiele werkgebieden en upload het pakket naar Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="1553b-163">Create a deployable package that contains custom mobile workspaces, and upload the package to Microsoft Dynamics Lifecycle Services (LCS).</span></span></td>
<td><span data-ttu-id="1553b-164"><a href="../deployment/create-apply-deployable-package.md">Een implementeerbaar pakket maken</a></span><span class="sxs-lookup"><span data-stu-id="1553b-164"><a href="../deployment/create-apply-deployable-package.md">Create a deployable package</a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1553b-165">6</span><span class="sxs-lookup"><span data-stu-id="1553b-165">6</span></span></td>
<td><span data-ttu-id="1553b-166">Systeembeheerder</span><span class="sxs-lookup"><span data-stu-id="1553b-166">System administrator</span></span></td>
<td><span data-ttu-id="1553b-167">Pas het implementeerbare pakket toe met de aangepaste werkbieden die worden geleverd door uw onafhankelijke sofwareleverancier (ISV).</span><span class="sxs-lookup"><span data-stu-id="1553b-167">Apply the deployable package that contains the custom workspaces that are provided by the independent software vendor (ISV).</span></span></td>
<td><span data-ttu-id="1553b-168"><a href="../deployment/apply-deployable-package-system.md">Een implementeerbaar pakket toepassen</a></span><span class="sxs-lookup"><span data-stu-id="1553b-168"><a href="../deployment/apply-deployable-package-system.md">Apply a deployable package</a></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1553b-169">7</span><span class="sxs-lookup"><span data-stu-id="1553b-169">7</span></span></td>
<td><span data-ttu-id="1553b-170">Systeembeheerder</span><span class="sxs-lookup"><span data-stu-id="1553b-170">System administrator</span></span></td>
<td><span data-ttu-id="1553b-171">Publiceer de aangepaste mobiele werkgebieden die worden geleverd door de ISV.</span><span class="sxs-lookup"><span data-stu-id="1553b-171">Publish the custom mobile workspaces that are provided by the ISV.</span></span></td>
<td><span data-ttu-id="1553b-172"><a href="publish-mobile-workspace.md">Mobiel werkgebied publiceren</a></span><span class="sxs-lookup"><span data-stu-id="1553b-172"><a href="publish-mobile-workspace.md">Publish a mobile workspace</a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1553b-173">8</span><span class="sxs-lookup"><span data-stu-id="1553b-173">8</span></span></td>
<td><span data-ttu-id="1553b-174">Gebruiker</span><span class="sxs-lookup"><span data-stu-id="1553b-174">User</span></span></td>
<td><span data-ttu-id="1553b-175">Download en installeer de mobiele app.</span><span class="sxs-lookup"><span data-stu-id="1553b-175">Download and install the mobile app.</span></span></td>
<td><span data-ttu-id="1553b-176">
<a href="https://go.microsoft.com/fwlink/?linkid=850662">Finance and Operations-app voor Android</a></span><span class="sxs-lookup"><span data-stu-id="1553b-176">
<a href="https://go.microsoft.com/fwlink/?linkid=850662">Finance and Operations app for Android</a></span></span><BR/><span data-ttu-id="1553b-177">
<a href="https://go.microsoft.com/fwlink/?linkid=850663">Finance and Operations-app voor iOS</a></span><span class="sxs-lookup"><span data-stu-id="1553b-177">
<a href="https://go.microsoft.com/fwlink/?linkid=850663">Finance and Operations app for iOS</a></span></span><BR/>
<span data-ttu-id="1553b-178">(Windows Phone wordt niet ondersteund)</span><span class="sxs-lookup"><span data-stu-id="1553b-178">(Windows Phone unsupported)</span></span>
</td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1553b-179">9</span><span class="sxs-lookup"><span data-stu-id="1553b-179">9</span></span></td>
<td><span data-ttu-id="1553b-180">Gebruiker</span><span class="sxs-lookup"><span data-stu-id="1553b-180">User</span></span></td>
<td><span data-ttu-id="1553b-181">Meld u aan en gebruik de mobiele app.</span><span class="sxs-lookup"><span data-stu-id="1553b-181">Sign in, and use the mobile app.</span></span> <span data-ttu-id="1553b-182">De app omvat de mobiele werkgebieden die zijn gepubliceerd door de systeembeheerder.</span><span class="sxs-lookup"><span data-stu-id="1553b-182">The app includes the mobile workspaces that have been published by the system administrator.</span></span></td>
<td><span data-ttu-id="1553b-183">Een lijst met mobiele werkgebieden die door Microsoft worden geleverd, vindt u in <a href="mobile-workspaces-released.md">Recentelijk gepubliceerde mobiele werkgebieden</a>.</span><span class="sxs-lookup"><span data-stu-id="1553b-183">To see a list of mobile workspaces that are provided by Microsoft, see <a href="mobile-workspaces-released.md">Mobile workspaces recently released</a>.</span></span>
</td>
</tr>
</tbody>
</table>

## <a name="troubleshooting"></a><span data-ttu-id="1553b-184">Problemen oplossen</span><span class="sxs-lookup"><span data-stu-id="1553b-184">Troubleshooting</span></span>
[<span data-ttu-id="1553b-185">Resources voor mobiel platform</span><span class="sxs-lookup"><span data-stu-id="1553b-185">Mobile platform resources</span></span>](platform/mobile-platform-home-page.md#troubleshooting-the-app)
