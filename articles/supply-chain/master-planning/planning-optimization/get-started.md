---
title: Aan de slag met Planningsoptimalisatie
description: In dit onderwerp wordt uitgelegd hoe u aan de slag gaat met de functionaliteit Planningsoptimalisatie.
author: ChristianRytt
manager: tfehr
ms.date: 05/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: MpsIntegrationParameters, MpsFitAnalysis
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 04b39469ccf4f088bb33bdfc73ce40eece6f5f2e
ms.sourcegitcommit: cde71bc7d14ea6cdff2c4e991057d39a6a0473d9
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/24/2020
ms.locfileid: "3887259"
---
# <a name="get-started-with-planning-optimization"></a><span data-ttu-id="6315d-103">Aan de slag met Planningsoptimalisatie</span><span class="sxs-lookup"><span data-stu-id="6315d-103">Get started with Planning Optimization</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="6315d-104">De functie Planningsoptimalisatie ondersteunt momenteel niet alle functies die beschikbaar zijn in de planningsengine die is ingebouwd in Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="6315d-104">The Planning Optimization functionality doesn't currently support all the features that are available in the planning engine that is built into Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="6315d-105">Het is daarom belangrijk dat u evalueert of de functieset die momenteel beschikbaar is in Planningsoptimalisatie voldoet aan uw behoeften.</span><span class="sxs-lookup"><span data-stu-id="6315d-105">Therefore, it's important that you evaluate whether the feature set that is currently available in Planning Optimization will meet your requirements.</span></span> <span data-ttu-id="6315d-106">Standaard is de functionaliteit Planningsoptimalisatie niet ingeschakeld in Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="6315d-106">By default, the Planning Optimization functionality isn't turned on in Dynamics Lifecycle Services (LCS) by default.</span></span> <span data-ttu-id="6315d-107">Daarom hebt u de mogelijkheid om uw beoordeling uit te voeren voordat deze is ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="6315d-107">Therefore, you have an opportunity to do your evaluation before it's turned on.</span></span>

<span data-ttu-id="6315d-108">Uiteindelijk vervangt Planningsoptimalisatie de bestaande ingebouwde Supply Chain Management-planningsengine.</span><span class="sxs-lookup"><span data-stu-id="6315d-108">Eventually, Planning Optimization will replace the existing built-in Supply Chain Management planning engine.</span></span>

<span data-ttu-id="6315d-109">Voordat u Planningsoptimalisatie inschakelt, kunt u het beste de resultaten van de analyse voor passende Planningsoptimalisatie evalueren.</span><span class="sxs-lookup"><span data-stu-id="6315d-109">Before you turn on Planning Optimization, we strongly recommend that you evaluate the results of the Planning Optimization fit analysis.</span></span> <span data-ttu-id="6315d-110">Zie [Analyse voor passende Planningsoptimalisatie](planning-optimization-fit-analysis.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="6315d-110">For more information, see [Planning Optimization fit analysis](planning-optimization-fit-analysis.md).</span></span>

### <a name="availability"></a><span data-ttu-id="6315d-111">Beschikbaarheid</span><span class="sxs-lookup"><span data-stu-id="6315d-111">Availability</span></span>
<span data-ttu-id="6315d-112">Planningsoptimalisatie is momenteel beschikbaar in de volgende Azure-regio's: Verenigde Staten, Canada, Europa, Verenigd Koninkrijk en Australië.</span><span class="sxs-lookup"><span data-stu-id="6315d-112">Planning Optimization is currently available in the following Azure geographies: United States, Canada, Europe, United Kingdom, and Australia.</span></span> <span data-ttu-id="6315d-113">Als u de invoegtoepassing vanuit een andere geografische regio probeert te installeren, wordt in LCS een bericht weergegeven dat deze niet wordt ondersteund.</span><span class="sxs-lookup"><span data-stu-id="6315d-113">If you try to install the add-in from another geographic region, then LCS will show a message that this geographic is not supported.</span></span>

<span data-ttu-id="6315d-114">Planningsoptimalisatie wordt niet ondersteund voor on-premises implementaties van Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="6315d-114">Note that Planning Optimization does not support on-premises deployments of Dynamics 365 Supply Chain Management.</span></span>

### <a name="licensing"></a><span data-ttu-id="6315d-115">Licenties</span><span class="sxs-lookup"><span data-stu-id="6315d-115">Licensing</span></span>

<span data-ttu-id="6315d-116">Als u de hoofdplanning kunt uitvoeren met uw huidige licentie, hoeft u geen extra licentie aan te schaffen om Planningsoptimalisatie te kunnen gebruiken.</span><span class="sxs-lookup"><span data-stu-id="6315d-116">If you can run master planning by using your current license, you don't have to buy an additional license to start to use Planning Optimization.</span></span>

### <a name="install-the-add-in"></a><span data-ttu-id="6315d-117">De invoegtoepassing installeren</span><span class="sxs-lookup"><span data-stu-id="6315d-117">Install the add-in</span></span>

<span data-ttu-id="6315d-118">Als u Planningsoptimalisatie wilt gebruiken, moet u de invoegtoepassing Planningsoptimalisatie voor Dynamics 365 Supply Chain Management gebruiken.</span><span class="sxs-lookup"><span data-stu-id="6315d-118">To use Planning Optimization, install the Planning Optimization Add-in for Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="6315d-119">U kunt de invoegtoepassing openen vanuit uw LCS-project en de functie Planningsoptimalisatie inschakelen via de gebruikersinterface van Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="6315d-119">You can access the add-in from your LCS project and turn on the Planning Optimization functionality from the Supply Chain Management user interface (UI).</span></span>

> [!NOTE]
> <span data-ttu-id="6315d-120">De vereiste voor Planningsoptimalisatie is een omgeving met grote beschikbaarheid voor LCS, tier 2 of hoger (geen OneBox-omgeving), met Dynamics 365 Supply Chain Management versie 10.0.7 of hoger.</span><span class="sxs-lookup"><span data-stu-id="6315d-120">The requirement for Planning Optimization is an LCS enabled high-availability environment, tier 2 or higher (not a OneBox environment), with Dynamics 365 Supply Chain Management version 10.0.7 or later.</span></span> <span data-ttu-id="6315d-121">Als u de invoegtoepassing in een OneBox-omgeving probeert te installeren, wordt de installatie niet voltooid en moet u de installatie annuleren.</span><span class="sxs-lookup"><span data-stu-id="6315d-121">If you try to install the add-in on a OneBox environment, the installation will not complete and you will need to cancel the installation.</span></span>

1. <span data-ttu-id="6315d-122">Meld u aan bij LCS en open de gewenste omgeving.</span><span class="sxs-lookup"><span data-stu-id="6315d-122">Sign in to LCS, and open the desired environment.</span></span>
1. <span data-ttu-id="6315d-123">Ga naar **Volledige details**.</span><span class="sxs-lookup"><span data-stu-id="6315d-123">Go to **Full details**.</span></span>
1. <span data-ttu-id="6315d-124">Schuif omlaag naar het sneltabblad **Invoegtoepassingen voor omgeving**.</span><span class="sxs-lookup"><span data-stu-id="6315d-124">Scroll down to the **Environment add-ins** FastTab.</span></span>
1. <span data-ttu-id="6315d-125">Selecteer **Een nieuwe invoegtoepassing installeren**.</span><span class="sxs-lookup"><span data-stu-id="6315d-125">Select **Install a new add-in**.</span></span>
1. <span data-ttu-id="6315d-126">Selecteer **Planningsoptimalisatie**.</span><span class="sxs-lookup"><span data-stu-id="6315d-126">Select **Planning Optimization**.</span></span>
1. <span data-ttu-id="6315d-127">Volg de installatiehandleiding en ga akkoord met de voorwaarden en bepalingen.</span><span class="sxs-lookup"><span data-stu-id="6315d-127">Follow the installation guide, and agree to the terms and conditions.</span></span>
1. <span data-ttu-id="6315d-128">Selecteer **Installeren**.</span><span class="sxs-lookup"><span data-stu-id="6315d-128">Select **Install**.</span></span>
1. <span data-ttu-id="6315d-129">Op het sneltabblad **Invoegtoepassingen voor omgeving** zou u moeten zien dat planningsoptimalisatie wordt geïnstalleerd.</span><span class="sxs-lookup"><span data-stu-id="6315d-129">On the **Environment add-ins** FastTab you should see that Planning Optimization is installing.</span></span>
1. <span data-ttu-id="6315d-130">Na een paar minuten moet **Installeren** veranderen in **Geïnstalleerd** (u moet de pagina mogelijk vernieuwen).</span><span class="sxs-lookup"><span data-stu-id="6315d-130">After a few minutes **Installing** should change to **Installed** (you may need to refresh the page).</span></span> <span data-ttu-id="6315d-131">Wanneer Planningsoptimalisering is geïnstalleerd, kunt u het activeren in Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="6315d-131">When installed, you are ready to activate Planning Optimization in Dynamics 365 Supply Chain Management.</span></span>

### <a name="planning-optimization-integration"></a><span data-ttu-id="6315d-132">Integratie van Planningsoptimalisatie</span><span class="sxs-lookup"><span data-stu-id="6315d-132">Planning Optimization integration</span></span>

<span data-ttu-id="6315d-133">Als u wilt configureren of de invoegtoepassing Planningsoptimalisatie moet worden gebruikt voor hoofdplanning, gaat u naar **Hoofdplanning** \> **Instellen** \> **Integratie van Planningsoptimalisatie**.</span><span class="sxs-lookup"><span data-stu-id="6315d-133">To configure whether the Planning Optimization Add-in should be used for master planning, go to **Master planning** \> **Setup** \> **Planning Optimization parameters**.</span></span>

#### <a name="connection-status"></a><span data-ttu-id="6315d-134">Verbindingsstatus</span><span class="sxs-lookup"><span data-stu-id="6315d-134">Connection status</span></span>

<span data-ttu-id="6315d-135">De verbindingsstatus geeft de huidige status aan van de verbinding tussen Supply Chain Management en de service Planningsoptimalisatie.</span><span class="sxs-lookup"><span data-stu-id="6315d-135">The connection status indicates the current status of the connection between Supply Chain Management and the Planning Optimization service.</span></span> <span data-ttu-id="6315d-136">De volgende tabel bevat de mogelijke waarden.</span><span class="sxs-lookup"><span data-stu-id="6315d-136">The following table shows the possible values.</span></span>

| <span data-ttu-id="6315d-137">Verbindingsstatus</span><span class="sxs-lookup"><span data-stu-id="6315d-137">Connection status</span></span> | <span data-ttu-id="6315d-138">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="6315d-138">Description</span></span> | <span data-ttu-id="6315d-139">Kan Planningsoptimalisatie worden gebruikt?</span><span class="sxs-lookup"><span data-stu-id="6315d-139">Can Planning Optimization be used?</span></span> |
|---|---|---|
| <span data-ttu-id="6315d-140">Verbonden</span><span class="sxs-lookup"><span data-stu-id="6315d-140">Connected</span></span> | <span data-ttu-id="6315d-141">Er is een verbinding tot stand gebracht tussen de service Planningsoptimalisatie en Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="6315d-141">A connection has been established between the Planning Optimization service and Supply Chain Management.</span></span> | <span data-ttu-id="6315d-142">Ja</span><span class="sxs-lookup"><span data-stu-id="6315d-142">Yes</span></span> |
| <span data-ttu-id="6315d-143">Verbinding wordt ingeschakeld</span><span class="sxs-lookup"><span data-stu-id="6315d-143">Enabling connection</span></span> | <span data-ttu-id="6315d-144">Een aanvraag om de verbinding met de service Planningsoptimalisatie in te schakelen, wordt momenteel uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="6315d-144">A request to turn on the connection to the Planning Optimization service is currently in progress.</span></span> | <span data-ttu-id="6315d-145">Nee</span><span class="sxs-lookup"><span data-stu-id="6315d-145">No</span></span> |
| <span data-ttu-id="6315d-146">Niet verbonden</span><span class="sxs-lookup"><span data-stu-id="6315d-146">Disconnected</span></span> | <span data-ttu-id="6315d-147">Er is geen verbinding met de service Planningsoptimalisatie.</span><span class="sxs-lookup"><span data-stu-id="6315d-147">There is no connection to the Planning Optimization service.</span></span> <span data-ttu-id="6315d-148">De verbinding kan worden ingeschakeld vanuit LCS, zoals eerder in dit onderwerp is beschreven.</span><span class="sxs-lookup"><span data-stu-id="6315d-148">The connection can be turned on from LCS, as described earlier in this topic.</span></span> | <span data-ttu-id="6315d-149">Nee</span><span class="sxs-lookup"><span data-stu-id="6315d-149">No</span></span> |
| <span data-ttu-id="6315d-150">Verbinding wordt uitgeschakeld</span><span class="sxs-lookup"><span data-stu-id="6315d-150">Disabling connection</span></span> | <span data-ttu-id="6315d-151">Een aanvraag om de verbinding met de service Planningsoptimalisatie uit te schakelen, wordt momenteel uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="6315d-151">A request to turn off the connection to the Planning Optimization service is currently in progress.</span></span> | <span data-ttu-id="6315d-152">Nee</span><span class="sxs-lookup"><span data-stu-id="6315d-152">No</span></span> |
| <span data-ttu-id="6315d-153">Status ophalen</span><span class="sxs-lookup"><span data-stu-id="6315d-153">Getting status</span></span> | <span data-ttu-id="6315d-154">Het systeem wacht op statusinformatie van de service Planningsoptimalisatie.</span><span class="sxs-lookup"><span data-stu-id="6315d-154">The system is waiting for status information from the Planning Optimization service.</span></span> | <span data-ttu-id="6315d-155">Nee</span><span class="sxs-lookup"><span data-stu-id="6315d-155">No</span></span> |

#### <a name="the-use-planning-optimization-option"></a><span data-ttu-id="6315d-156">De optie Planningsoptimalisatie gebruiken</span><span class="sxs-lookup"><span data-stu-id="6315d-156">The Use Planning Optimization option</span></span>

<span data-ttu-id="6315d-157">De instelling van de optie **Planningsoptimalisatie gebruiken** bepaalt welke planningsengine wordt gebruikt voor de hoofdplanning:</span><span class="sxs-lookup"><span data-stu-id="6315d-157">The setting of the **Use Planning Optimization** option determines which planning engine is used for master planning:</span></span>

- <span data-ttu-id="6315d-158">**Ja**: Planningsoptimalisatie wordt gebruikt voor de hoofdplanning.</span><span class="sxs-lookup"><span data-stu-id="6315d-158">**Yes** – Planning Optimization is used for master planning.</span></span>
- <span data-ttu-id="6315d-159">**Nee**: de ingebouwde planningsengine voor Supply Chain Management wordt gebruikt voor de hoofdplanning.</span><span class="sxs-lookup"><span data-stu-id="6315d-159">**No** – The built-in Supply Chain Management planning engine is used for master planning.</span></span>

> [!NOTE]
> <span data-ttu-id="6315d-160">Als bestaande planningsbatchtaken die zijn gemaakt voor de ingebouwde Supply Chain Management-planningsengine worden geactiveerd terwijl de optie **Planningsoptimalisatie gebruiken** is ingesteld op **Ja**, mislukken deze taken.</span><span class="sxs-lookup"><span data-stu-id="6315d-160">If existing planning batch jobs that were created for the built-in Supply Chain Management planning engine are triggered while the **Use Planning Optimization** option is set to **Yes**, those jobs will fail.</span></span>

### <a name="integration-with-the-setup"></a><span data-ttu-id="6315d-161">Integratie met de setup</span><span class="sxs-lookup"><span data-stu-id="6315d-161">Integration with the setup</span></span>

<span data-ttu-id="6315d-162">Als de Planningsoptimalisatie is ingeschakeld, wordt de hoofdplanning uitgevoerd met behulp van de invoegtoepassing Planningsoptimalisatie.</span><span class="sxs-lookup"><span data-stu-id="6315d-162">If the Planning Optimization preview is turned on, master planning is done by using the Planning Optimization Add-in.</span></span> <span data-ttu-id="6315d-163">In dit geval worden de resultaten en functies van de hoofdplanning beïnvloed.</span><span class="sxs-lookup"><span data-stu-id="6315d-163">In this case, master planning results and features are affected.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="6315d-164">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="6315d-164">Additional resources</span></span>

[<span data-ttu-id="6315d-165">Algemene voorwaarden voor de preview</span><span class="sxs-lookup"><span data-stu-id="6315d-165">Terms and conditions for the preview</span></span>](https://go.microsoft.com/fwlink/?linkid=2015274)

[<span data-ttu-id="6315d-166">Overzicht van Planningsoptimalisatie</span><span class="sxs-lookup"><span data-stu-id="6315d-166">Planning Optimization overview</span></span>](planning-optimization-overview.md)

[<span data-ttu-id="6315d-167">Analyse voor passende Planningsoptimalisatie</span><span class="sxs-lookup"><span data-stu-id="6315d-167">Planning Optimization fit analysis</span></span>](planning-optimization-fit-analysis.md)

[<span data-ttu-id="6315d-168">Planhistorie en planningslogboeken weergeven</span><span class="sxs-lookup"><span data-stu-id="6315d-168">View plan history and planning logs</span></span>](plan-history-logs.md)

[<span data-ttu-id="6315d-169">Filters op een plan toepassen</span><span class="sxs-lookup"><span data-stu-id="6315d-169">Apply filters to a plan</span></span>](plan-filters.md)

[<span data-ttu-id="6315d-170">Een planningstaak annuleren</span><span class="sxs-lookup"><span data-stu-id="6315d-170">Cancel a planning job</span></span>](cancel-planning-job.md)
