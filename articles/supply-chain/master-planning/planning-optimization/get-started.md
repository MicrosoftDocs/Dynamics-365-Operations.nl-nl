---
title: Aan de slag met Planningsoptimalisatie
description: In dit onderwerp wordt uitgelegd hoe u aan de slag gaat met de functionaliteit Planningsoptimalisatie.
author: ChristianRytt
manager: AnnBe
ms.date: 01/17/2020
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
ms.openlocfilehash: 3e0371c6addc0412dc2fc105891b012941e92a06
ms.sourcegitcommit: e5a3c85a322a9216b8f176536d664fef40ae0bec
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/17/2020
ms.locfileid: "2971459"
---
[!include [banner](../../includes/preview-banner.md)]
[!include [banner](../../includes/banner.md)]

# <a name="get-started-with-planning-optimization"></a><span data-ttu-id="c1430-103">Aan de slag met Planningsoptimalisatie</span><span class="sxs-lookup"><span data-stu-id="c1430-103">Get started with Planning Optimization</span></span>

<span data-ttu-id="c1430-104">De functie Planningsoptimalisatie ondersteunt momenteel niet alle functies die beschikbaar zijn in de planningsengine die is ingebouwd in Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="c1430-104">The Planning Optimization functionality doesn't currently support all the features that are available in the planning engine that is built into Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="c1430-105">Het is daarom belangrijk dat u evalueert of de functieset die momenteel beschikbaar is in Planningsoptimalisatie voldoet aan uw behoeften.</span><span class="sxs-lookup"><span data-stu-id="c1430-105">Therefore, it's important that you evaluate whether the feature set that is currently available in Planning Optimization will meet your requirements.</span></span> <span data-ttu-id="c1430-106">Standaard is de functionaliteit Planningsoptimalisatie niet ingeschakeld in Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="c1430-106">By default, the Planning Optimization functionality isn't turned on in Dynamics Lifecycle Services (LCS) by default.</span></span> <span data-ttu-id="c1430-107">Daarom hebt u de mogelijkheid om uw beoordeling uit te voeren voordat deze is ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="c1430-107">Therefore, you have an opportunity to do your evaluation before it's turned on.</span></span>

<span data-ttu-id="c1430-108">Uiteindelijk vervangt Planningsoptimalisatie de bestaande ingebouwde Supply Chain Management-planningsengine.</span><span class="sxs-lookup"><span data-stu-id="c1430-108">Eventually, Planning Optimization will replace the existing built-in Supply Chain Management planning engine.</span></span>

<span data-ttu-id="c1430-109">Voordat u Planningsoptimalisatie inschakelt, kunt u het beste de resultaten van de analyse voor passende Planningsoptimalisatie evalueren.</span><span class="sxs-lookup"><span data-stu-id="c1430-109">Before you turn on Planning Optimization, we strongly recommend that you evaluate the results of the Planning Optimization fit analysis.</span></span> <span data-ttu-id="c1430-110">Zie [Analyse voor passende Planningsoptimalisatie](planning-optimization-fit-analysis.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="c1430-110">For more information, see [Planning Optimization fit analysis](planning-optimization-fit-analysis.md).</span></span>

### <a name="licensing"></a><span data-ttu-id="c1430-111">Licenties</span><span class="sxs-lookup"><span data-stu-id="c1430-111">Licensing</span></span>

<span data-ttu-id="c1430-112">Als u de hoofdplanning kunt uitvoeren met uw huidige licentie, hoeft u geen extra licentie aan te schaffen om Planningsoptimalisatie te kunnen gebruiken.</span><span class="sxs-lookup"><span data-stu-id="c1430-112">If you can run master planning by using your current license, you don't have to buy an additional license to start to use Planning Optimization.</span></span>

### <a name="install-the-add-in"></a><span data-ttu-id="c1430-113">De invoegtoepassing installeren</span><span class="sxs-lookup"><span data-stu-id="c1430-113">Install the add-in</span></span>

<span data-ttu-id="c1430-114">Als u Planningsoptimalisatie wilt gebruiken, moet u de invoegtoepassing Planningsoptimalisatie voor Dynamics 365 Supply Chain Management gebruiken.</span><span class="sxs-lookup"><span data-stu-id="c1430-114">To use Planning Optimization, install the Planning Optimization Add-in for Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="c1430-115">U kunt de invoegtoepassing openen vanuit uw LCS-project en de functie Planningsoptimalisatie inschakelen via de gebruikersinterface van Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="c1430-115">You can access the add-in from your LCS project and turn on the Planning Optimization functionality from the Supply Chain Management user interface (UI).</span></span>

1. <span data-ttu-id="c1430-116">Meld u aan bij LCS en open de gewenste omgeving.</span><span class="sxs-lookup"><span data-stu-id="c1430-116">Sign in to LCS, and open the desired environment.</span></span>
1. <span data-ttu-id="c1430-117">Ga naar **Volledige details**.</span><span class="sxs-lookup"><span data-stu-id="c1430-117">Go to **Full details**.</span></span>
1. <span data-ttu-id="c1430-118">Schuif omlaag naar het sneltabblad **Invoegtoepassingen voor omgeving**.</span><span class="sxs-lookup"><span data-stu-id="c1430-118">Scroll down to the **Environment add-ins** FastTab.</span></span>
1. <span data-ttu-id="c1430-119">Selecteer **Een nieuwe invoegtoepassing installeren**.</span><span class="sxs-lookup"><span data-stu-id="c1430-119">Select **Install a new add-in**.</span></span>
1. <span data-ttu-id="c1430-120">Selecteer **Planningsoptimalisatie**.</span><span class="sxs-lookup"><span data-stu-id="c1430-120">Select **Planning Optimization**.</span></span>
1. <span data-ttu-id="c1430-121">Volg de installatiehandleiding en ga akkoord met de voorwaarden en bepalingen.</span><span class="sxs-lookup"><span data-stu-id="c1430-121">Follow the installation guide, and agree to the terms and conditions.</span></span>
1. <span data-ttu-id="c1430-122">Selecteer **Installeren**.</span><span class="sxs-lookup"><span data-stu-id="c1430-122">Select **Install**.</span></span>
1. <span data-ttu-id="c1430-123">Op het sneltabblad **Invoegtoepassingen voor omgeving** zou u moeten zien dat planningsoptimalisatie wordt geïnstalleerd.</span><span class="sxs-lookup"><span data-stu-id="c1430-123">On the **Environment add-ins** FastTab you should see that Planning Optimization is installing.</span></span>
1. <span data-ttu-id="c1430-124">Na een paar minuten moet **Installeren** veranderen in **Geïnstalleerd** (u moet de pagina mogelijk vernieuwen).</span><span class="sxs-lookup"><span data-stu-id="c1430-124">After a few minutes **Installing** should change to **Installed** (you may need to refresh the page).</span></span> <span data-ttu-id="c1430-125">Wanneer Planningsoptimalisering is geïnstalleerd, kunt u het activeren in Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="c1430-125">When installed, you are ready to activate Planning Optimization in Dynamics 365 Supply Chain Management.</span></span>

### <a name="planning-optimization-integration"></a><span data-ttu-id="c1430-126">Integratie van Planningsoptimalisatie</span><span class="sxs-lookup"><span data-stu-id="c1430-126">Planning Optimization integration</span></span>

<span data-ttu-id="c1430-127">Als u wilt configureren of de invoegtoepassing Planningsoptimalisatie moet worden gebruikt voor hoofdplanning, gaat u naar **Hoofdplanning** \> **Instellen** \> **Integratie van Planningsoptimalisatie**.</span><span class="sxs-lookup"><span data-stu-id="c1430-127">To configure whether the Planning Optimization Add-in should be used for master planning, go to **Master planning** \> **Setup** \> **Planning Optimization parameters**.</span></span>

#### <a name="connection-status"></a><span data-ttu-id="c1430-128">Verbindingsstatus</span><span class="sxs-lookup"><span data-stu-id="c1430-128">Connection status</span></span>

<span data-ttu-id="c1430-129">De verbindingsstatus geeft de huidige status aan van de verbinding tussen Supply Chain Management en de service Planningsoptimalisatie.</span><span class="sxs-lookup"><span data-stu-id="c1430-129">The connection status indicates the current status of the connection between Supply Chain Management and the Planning Optimization service.</span></span> <span data-ttu-id="c1430-130">De volgende tabel bevat de mogelijke waarden.</span><span class="sxs-lookup"><span data-stu-id="c1430-130">The following table shows the possible values.</span></span>

| <span data-ttu-id="c1430-131">Verbindingsstatus</span><span class="sxs-lookup"><span data-stu-id="c1430-131">Connection status</span></span> | <span data-ttu-id="c1430-132">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="c1430-132">Description</span></span> | <span data-ttu-id="c1430-133">Kan Planningsoptimalisatie worden gebruikt?</span><span class="sxs-lookup"><span data-stu-id="c1430-133">Can Planning Optimization be used?</span></span> |
|---|---|---|
| <span data-ttu-id="c1430-134">Verbonden</span><span class="sxs-lookup"><span data-stu-id="c1430-134">Connected</span></span> | <span data-ttu-id="c1430-135">Er is een verbinding tot stand gebracht tussen de service Planningsoptimalisatie en Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="c1430-135">A connection has been established between the Planning Optimization service and Supply Chain Management.</span></span> | <span data-ttu-id="c1430-136">Ja</span><span class="sxs-lookup"><span data-stu-id="c1430-136">Yes</span></span> |
| <span data-ttu-id="c1430-137">Verbinding wordt ingeschakeld</span><span class="sxs-lookup"><span data-stu-id="c1430-137">Enabling connection</span></span> | <span data-ttu-id="c1430-138">Een aanvraag om de verbinding met de service Planningsoptimalisatie in te schakelen, wordt momenteel uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="c1430-138">A request to turn on the connection to the Planning Optimization service is currently in progress.</span></span> | <span data-ttu-id="c1430-139">Nee</span><span class="sxs-lookup"><span data-stu-id="c1430-139">No</span></span> |
| <span data-ttu-id="c1430-140">Niet verbonden</span><span class="sxs-lookup"><span data-stu-id="c1430-140">Disconnected</span></span> | <span data-ttu-id="c1430-141">Er is geen verbinding met de service Planningsoptimalisatie.</span><span class="sxs-lookup"><span data-stu-id="c1430-141">There is no connection to the Planning Optimization service.</span></span> <span data-ttu-id="c1430-142">De verbinding kan worden ingeschakeld vanuit LCS, zoals eerder in dit onderwerp is beschreven.</span><span class="sxs-lookup"><span data-stu-id="c1430-142">The connection can be turned on from LCS, as described earlier in this topic.</span></span> | <span data-ttu-id="c1430-143">Nee</span><span class="sxs-lookup"><span data-stu-id="c1430-143">No</span></span> |
| <span data-ttu-id="c1430-144">Verbinding wordt uitgeschakeld</span><span class="sxs-lookup"><span data-stu-id="c1430-144">Disabling connection</span></span> | <span data-ttu-id="c1430-145">Een aanvraag om de verbinding met de service Planningsoptimalisatie uit te schakelen, wordt momenteel uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="c1430-145">A request to turn off the connection to the Planning Optimization service is currently in progress.</span></span> | <span data-ttu-id="c1430-146">Nee</span><span class="sxs-lookup"><span data-stu-id="c1430-146">No</span></span> |
| <span data-ttu-id="c1430-147">Status ophalen</span><span class="sxs-lookup"><span data-stu-id="c1430-147">Getting status</span></span> | <span data-ttu-id="c1430-148">Het systeem wacht op statusinformatie van de service Planningsoptimalisatie.</span><span class="sxs-lookup"><span data-stu-id="c1430-148">The system is waiting for status information from the Planning Optimization service.</span></span> | <span data-ttu-id="c1430-149">Nee</span><span class="sxs-lookup"><span data-stu-id="c1430-149">No</span></span> |

#### <a name="the-use-planning-optimization-option"></a><span data-ttu-id="c1430-150">De optie Planningsoptimalisatie gebruiken</span><span class="sxs-lookup"><span data-stu-id="c1430-150">The Use Planning Optimization option</span></span>

<span data-ttu-id="c1430-151">De instelling van de optie **Planningsoptimalisatie gebruiken** bepaalt welke planningsengine wordt gebruikt voor de hoofdplanning:</span><span class="sxs-lookup"><span data-stu-id="c1430-151">The setting of the **Use Planning Optimization** option determines which planning engine is used for master planning:</span></span>

- <span data-ttu-id="c1430-152">**Ja**: Planningsoptimalisatie wordt gebruikt voor de hoofdplanning.</span><span class="sxs-lookup"><span data-stu-id="c1430-152">**Yes** – Planning Optimization is used for master planning.</span></span>
- <span data-ttu-id="c1430-153">**Nee**: de ingebouwde planningsengine voor Supply Chain Management wordt gebruikt voor de hoofdplanning.</span><span class="sxs-lookup"><span data-stu-id="c1430-153">**No** – The built-in Supply Chain Management planning engine is used for master planning.</span></span>

> [!NOTE]
> <span data-ttu-id="c1430-154">Als bestaande planningsbatchtaken die zijn gemaakt voor de ingebouwde Supply Chain Management-planningsengine worden geactiveerd terwijl de optie **Planningsoptimalisatie gebruiken** is ingesteld op **Ja**, mislukken deze taken.</span><span class="sxs-lookup"><span data-stu-id="c1430-154">If existing planning batch jobs that were created for the built-in Supply Chain Management planning engine are triggered while the **Use Planning Optimization** option is set to **Yes**, those jobs will fail.</span></span>

### <a name="integration-with-the-setup"></a><span data-ttu-id="c1430-155">Integratie met de setup</span><span class="sxs-lookup"><span data-stu-id="c1430-155">Integration with the setup</span></span>

<span data-ttu-id="c1430-156">Als de Planningsoptimalisatie is ingeschakeld, wordt de hoofdplanning uitgevoerd met behulp van de invoegtoepassing Planningsoptimalisatie.</span><span class="sxs-lookup"><span data-stu-id="c1430-156">If the Planning Optimization preview is turned on, master planning is done by using the Planning Optimization Add-in.</span></span> <span data-ttu-id="c1430-157">In dit geval worden de resultaten en functies van de hoofdplanning beïnvloed.</span><span class="sxs-lookup"><span data-stu-id="c1430-157">In this case, master planning results and features are affected.</span></span>

## <a name="related-resources"></a><span data-ttu-id="c1430-158">Gerelateerde bronnen</span><span class="sxs-lookup"><span data-stu-id="c1430-158">Related resources</span></span>

[<span data-ttu-id="c1430-159">Algemene voorwaarden voor de preview</span><span class="sxs-lookup"><span data-stu-id="c1430-159">Terms and conditions for the preview</span></span>](https://go.microsoft.com/fwlink/?linkid=2015274)

[<span data-ttu-id="c1430-160">Overzicht van Planningsoptimalisatie</span><span class="sxs-lookup"><span data-stu-id="c1430-160">Planning Optimization overview</span></span>](planning-optimization-overview.md)

[<span data-ttu-id="c1430-161">Analyse voor passende Planningsoptimalisatie</span><span class="sxs-lookup"><span data-stu-id="c1430-161">Planning Optimization fit analysis</span></span>](planning-optimization-fit-analysis.md)

[<span data-ttu-id="c1430-162">Planhistorie en planningslogboeken weergeven</span><span class="sxs-lookup"><span data-stu-id="c1430-162">View plan history and planning logs</span></span>](plan-history-logs.md)

[<span data-ttu-id="c1430-163">Filters op een plan toepassen</span><span class="sxs-lookup"><span data-stu-id="c1430-163">Apply filters to a plan</span></span>](plan-filters.md)

[<span data-ttu-id="c1430-164">Een planningstaak annuleren</span><span class="sxs-lookup"><span data-stu-id="c1430-164">Cancel a planning job</span></span>](cancel-planning-job.md)
