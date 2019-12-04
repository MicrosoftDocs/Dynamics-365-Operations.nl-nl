---
title: Aan de slag met Planningsoptimalisatie
description: In dit onderwerp wordt uitgelegd hoe u aan de slag gaat met de functionaliteit Planningsoptimalisatie.
author: ChristianRytt
manager: AnnBe
ms.date: 10/29/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 37c2acb2397b2a0ad69272c0645bd200a8d7910d
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/06/2019
ms.locfileid: "2773931"
---
[!include [banner](../../includes/preview-banner.md)]
[!include [banner](../../includes/banner.md)]

# <a name="get-started-with-planning-optimization"></a><span data-ttu-id="88fb4-103">Aan de slag met Planningsoptimalisatie</span><span class="sxs-lookup"><span data-stu-id="88fb4-103">Get started with Planning Optimization</span></span>

<span data-ttu-id="88fb4-104">De functie Planningsoptimalisatie ondersteunt momenteel niet alle functies die beschikbaar zijn in de planningsengine die is ingebouwd in Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="88fb4-104">The Planning Optimization functionality doesn't currently support all the features that are available in the planning engine that is built into Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="88fb4-105">Het is daarom belangrijk dat u evalueert of de functieset die momenteel beschikbaar is in Planningsoptimalisatie voldoet aan uw behoeften.</span><span class="sxs-lookup"><span data-stu-id="88fb4-105">Therefore, it's important that you evaluate whether the feature set that is currently available in Planning Optimization will meet your requirements.</span></span> <span data-ttu-id="88fb4-106">Standaard is de functionaliteit Planningsoptimalisatie niet ingeschakeld in Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="88fb4-106">By default, the Planning Optimization functionality isn't turned on in Dynamics Lifecycle Services (LCS) by default.</span></span> <span data-ttu-id="88fb4-107">Daarom hebt u de mogelijkheid om uw beoordeling uit te voeren voordat deze is ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="88fb4-107">Therefore, you have an opportunity to do your evaluation before it's turned on.</span></span>

<span data-ttu-id="88fb4-108">Uiteindelijk vervangt Planningsoptimalisatie de bestaande ingebouwde Supply Chain Management-planningsengine.</span><span class="sxs-lookup"><span data-stu-id="88fb4-108">Eventually, Planning Optimization will replace the existing built-in Supply Chain Management planning engine.</span></span>

<span data-ttu-id="88fb4-109">Voordat u Planningsoptimalisatie inschakelt, kunt u het beste de resultaten van de analyse voor passende Planningsoptimalisatie evalueren.</span><span class="sxs-lookup"><span data-stu-id="88fb4-109">Before you turn on Planning Optimization, we strongly recommend that you evaluate the results of the Planning Optimization fit analysis.</span></span> <span data-ttu-id="88fb4-110">Zie [Analyse voor passende Planningsoptimalisatie](planning-optimization-fit-analysis.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="88fb4-110">For more information, see [Planning Optimization fit analysis](planning-optimization-fit-analysis.md).</span></span>

### <a name="licensing"></a><span data-ttu-id="88fb4-111">Licenties</span><span class="sxs-lookup"><span data-stu-id="88fb4-111">Licensing</span></span>

<span data-ttu-id="88fb4-112">Als u de hoofdplanning kunt uitvoeren met uw huidige licentie, hoeft u geen extra licentie aan te schaffen om Planningsoptimalisatie te kunnen gebruiken.</span><span class="sxs-lookup"><span data-stu-id="88fb4-112">If you can run master planning by using your current license, you don't have to buy an additional license to start to use Planning Optimization.</span></span>

### <a name="install-the-add-in"></a><span data-ttu-id="88fb4-113">De invoegtoepassing installeren</span><span class="sxs-lookup"><span data-stu-id="88fb4-113">Install the add-in</span></span>

<span data-ttu-id="88fb4-114">Als u Planningsoptimalisatie wilt gebruiken, moet u de invoegtoepassing Planningsoptimalisatie voor Dynamics 365 Supply Chain Management gebruiken.</span><span class="sxs-lookup"><span data-stu-id="88fb4-114">To use Planning Optimization, install the Planning Optimization Add-in for Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="88fb4-115">U kunt de invoegtoepassing openen vanuit uw LCS-project en de functie Planningsoptimalisatie inschakelen via de gebruikersinterface van Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="88fb4-115">You can access the add-in from your LCS project and turn on the Planning Optimization functionality from the Supply Chain Management user interface (UI).</span></span>

1. <span data-ttu-id="88fb4-116">Meld u aan bij LCS en open de gewenste omgeving.</span><span class="sxs-lookup"><span data-stu-id="88fb4-116">Sign in to LCS, and open the desired environment.</span></span>
1. <span data-ttu-id="88fb4-117">Ga naar **Volledige details**.</span><span class="sxs-lookup"><span data-stu-id="88fb4-117">Go to **Full details**.</span></span>
1. <span data-ttu-id="88fb4-118">Selecteer **Onderhouden** of ga omlaag naar het sneltabblad **Invoegtoepassingen voor omgeving**.</span><span class="sxs-lookup"><span data-stu-id="88fb4-118">Select **Maintain**, or scroll down to the **Environment add-ins** FastTab.</span></span>
1. <span data-ttu-id="88fb4-119">Selecteer **Een nieuwe invoegtoepassing installeren**.</span><span class="sxs-lookup"><span data-stu-id="88fb4-119">Select **Install a new add-in**.</span></span>
1. <span data-ttu-id="88fb4-120">Selecteer **Planningsoptimalisatie**.</span><span class="sxs-lookup"><span data-stu-id="88fb4-120">Select **Planning Optimization**.</span></span>
1. <span data-ttu-id="88fb4-121">Volg de installatiehandleiding en ga akkoord met de voorwaarden en bepalingen.</span><span class="sxs-lookup"><span data-stu-id="88fb4-121">Follow the installation guide, and agree to the terms and conditions.</span></span>
1. <span data-ttu-id="88fb4-122">Selecteer **Installeren**.</span><span class="sxs-lookup"><span data-stu-id="88fb4-122">Select **Install**.</span></span>

### <a name="planning-optimization-integration"></a><span data-ttu-id="88fb4-123">Integratie van Planningsoptimalisatie</span><span class="sxs-lookup"><span data-stu-id="88fb4-123">Planning Optimization integration</span></span>

<span data-ttu-id="88fb4-124">Als u wilt configureren of de invoegtoepassing Planningsoptimalisatie moet worden gebruikt voor de hoofdplanning, gaat u naar **Hoofdplanning** \> **Instellen** \> **Integratie van Planningsoptimalisatie** \> **Integratieparameters**.</span><span class="sxs-lookup"><span data-stu-id="88fb4-124">To configure whether the Planning Optimization Add-in should be used for master planning, go to **Master planning** \> **Setup** \> **Planning Optimization integration** \> **Integration parameters**.</span></span>

#### <a name="connection-status"></a><span data-ttu-id="88fb4-125">Verbindingsstatus</span><span class="sxs-lookup"><span data-stu-id="88fb4-125">Connection status</span></span>

<span data-ttu-id="88fb4-126">De verbindingsstatus geeft de huidige status aan van de verbinding tussen Supply Chain Management en de service Planningsoptimalisatie.</span><span class="sxs-lookup"><span data-stu-id="88fb4-126">The connection status indicates the current status of the connection between Supply Chain Management and the Planning Optimization service.</span></span> <span data-ttu-id="88fb4-127">De volgende tabel bevat de mogelijke waarden.</span><span class="sxs-lookup"><span data-stu-id="88fb4-127">The following table shows the possible values.</span></span>

| <span data-ttu-id="88fb4-128">Verbindingsstatus</span><span class="sxs-lookup"><span data-stu-id="88fb4-128">Connection status</span></span> | <span data-ttu-id="88fb4-129">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="88fb4-129">Description</span></span> | <span data-ttu-id="88fb4-130">Kan Planningsoptimalisatie worden gebruikt?</span><span class="sxs-lookup"><span data-stu-id="88fb4-130">Can Planning Optimization be used?</span></span> |
|---|---|---|
| <span data-ttu-id="88fb4-131">Verbonden</span><span class="sxs-lookup"><span data-stu-id="88fb4-131">Connected</span></span> | <span data-ttu-id="88fb4-132">Er is een verbinding tot stand gebracht tussen de service Planningsoptimalisatie en Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="88fb4-132">A connection has been established between the Planning Optimization service and Supply Chain Management.</span></span> | <span data-ttu-id="88fb4-133">Ja</span><span class="sxs-lookup"><span data-stu-id="88fb4-133">Yes</span></span> |
| <span data-ttu-id="88fb4-134">Verbinding wordt ingeschakeld</span><span class="sxs-lookup"><span data-stu-id="88fb4-134">Enabling connection</span></span> | <span data-ttu-id="88fb4-135">Een aanvraag om de verbinding met de service Planningsoptimalisatie in te schakelen, wordt momenteel uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="88fb4-135">A request to turn on the connection to the Planning Optimization service is currently in progress.</span></span> | <span data-ttu-id="88fb4-136">Nee</span><span class="sxs-lookup"><span data-stu-id="88fb4-136">No</span></span> |
| <span data-ttu-id="88fb4-137">Niet verbonden</span><span class="sxs-lookup"><span data-stu-id="88fb4-137">Disconnected</span></span> | <span data-ttu-id="88fb4-138">Er is geen verbinding met de service Planningsoptimalisatie.</span><span class="sxs-lookup"><span data-stu-id="88fb4-138">There is no connection to the Planning Optimization service.</span></span> <span data-ttu-id="88fb4-139">De verbinding kan worden ingeschakeld vanuit LCS, zoals eerder in dit onderwerp is beschreven.</span><span class="sxs-lookup"><span data-stu-id="88fb4-139">The connection can be turned on from LCS, as described earlier in this topic.</span></span> | <span data-ttu-id="88fb4-140">Nee</span><span class="sxs-lookup"><span data-stu-id="88fb4-140">No</span></span> |
| <span data-ttu-id="88fb4-141">Verbinding wordt uitgeschakeld</span><span class="sxs-lookup"><span data-stu-id="88fb4-141">Disabling connection</span></span> | <span data-ttu-id="88fb4-142">Een aanvraag om de verbinding met de service Planningsoptimalisatie uit te schakelen, wordt momenteel uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="88fb4-142">A request to turn off the connection to the Planning Optimization service is currently in progress.</span></span> | <span data-ttu-id="88fb4-143">Nee</span><span class="sxs-lookup"><span data-stu-id="88fb4-143">No</span></span> |
| <span data-ttu-id="88fb4-144">Status ophalen</span><span class="sxs-lookup"><span data-stu-id="88fb4-144">Getting status</span></span> | <span data-ttu-id="88fb4-145">Het systeem wacht op statusinformatie van de service Planningsoptimalisatie.</span><span class="sxs-lookup"><span data-stu-id="88fb4-145">The system is waiting for status information from the Planning Optimization service.</span></span> | <span data-ttu-id="88fb4-146">Nee</span><span class="sxs-lookup"><span data-stu-id="88fb4-146">No</span></span> |

#### <a name="the-use-planning-optimization-option"></a><span data-ttu-id="88fb4-147">De optie Planningsoptimalisatie gebruiken</span><span class="sxs-lookup"><span data-stu-id="88fb4-147">The Use Planning Optimization option</span></span>

<span data-ttu-id="88fb4-148">De instelling van de optie **Planningsoptimalisatie gebruiken** bepaalt welke planningsengine wordt gebruikt voor de hoofdplanning:</span><span class="sxs-lookup"><span data-stu-id="88fb4-148">The setting of the **Use Planning Optimization** option determines which planning engine is used for master planning:</span></span>

- <span data-ttu-id="88fb4-149">**Ja**: Planningsoptimalisatie wordt gebruikt voor de hoofdplanning.</span><span class="sxs-lookup"><span data-stu-id="88fb4-149">**Yes** – Planning Optimization is used for master planning.</span></span>
- <span data-ttu-id="88fb4-150">**Nee**: de ingebouwde planningsengine voor Supply Chain Management wordt gebruikt voor de hoofdplanning.</span><span class="sxs-lookup"><span data-stu-id="88fb4-150">**No** – The built-in Supply Chain Management planning engine is used for master planning.</span></span>

> [!NOTE]
> <span data-ttu-id="88fb4-151">Als bestaande planningsbatchtaken die zijn gemaakt voor de ingebouwde Supply Chain Management-planningsengine worden geactiveerd terwijl de optie **Planningsoptimalisatie gebruiken** is ingesteld op **Ja**, mislukken deze taken.</span><span class="sxs-lookup"><span data-stu-id="88fb4-151">If existing planning batch jobs that were created for the built-in Supply Chain Management planning engine are triggered while the **Use Planning Optimization** option is set to **Yes**, those jobs will fail.</span></span>

### <a name="integration-with-the-setup"></a><span data-ttu-id="88fb4-152">Integratie met de setup</span><span class="sxs-lookup"><span data-stu-id="88fb4-152">Integration with the setup</span></span>

<span data-ttu-id="88fb4-153">Als de Planningsoptimalisatie is ingeschakeld, wordt de hoofdplanning uitgevoerd met behulp van de invoegtoepassing Planningsoptimalisatie.</span><span class="sxs-lookup"><span data-stu-id="88fb4-153">If the Planning Optimization preview is turned on, master planning is done by using the Planning Optimization Add-in.</span></span> <span data-ttu-id="88fb4-154">In dit geval worden de resultaten en functies van de hoofdplanning beïnvloed.</span><span class="sxs-lookup"><span data-stu-id="88fb4-154">In this case, master planning results and features are affected.</span></span>

## <a name="related-resources"></a><span data-ttu-id="88fb4-155">Gerelateerde bronnen</span><span class="sxs-lookup"><span data-stu-id="88fb4-155">Related resources</span></span>

[<span data-ttu-id="88fb4-156">Algemene voorwaarden voor de preview</span><span class="sxs-lookup"><span data-stu-id="88fb4-156">Terms and conditions for the preview</span></span>](https://go.microsoft.com/fwlink/?linkid=2015274)

[<span data-ttu-id="88fb4-157">Overzicht van Planningsoptimalisatie</span><span class="sxs-lookup"><span data-stu-id="88fb4-157">Planning Optimization overview</span></span>](planning-optimization-overview.md)

[<span data-ttu-id="88fb4-158">Analyse voor passende Planningsoptimalisatie</span><span class="sxs-lookup"><span data-stu-id="88fb4-158">Planning Optimization fit analysis</span></span>](planning-optimization-fit-analysis.md)

[<span data-ttu-id="88fb4-159">Planhistorie en planningslogboeken weergeven</span><span class="sxs-lookup"><span data-stu-id="88fb4-159">View plan history and planning logs</span></span>](plan-history-logs.md)

[<span data-ttu-id="88fb4-160">Filters op een plan toepassen</span><span class="sxs-lookup"><span data-stu-id="88fb4-160">Apply filters to a plan</span></span>](plan-filters.md)

[<span data-ttu-id="88fb4-161">Een planningstaak annuleren</span><span class="sxs-lookup"><span data-stu-id="88fb4-161">Cancel a planning job</span></span>](cancel-planning-job.md)
