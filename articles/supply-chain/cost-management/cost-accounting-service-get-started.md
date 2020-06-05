---
title: Aan de slag met de service voor kostprijsboekhouding (particuliere preview)
description: In dit onderwerp vindt u informatie over licenties en installatie-instructies voor de service kostprijsboekhouding.
author: AndersGirke
manager: tfehr
ms.date: 04/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2020-04-17
ms.dyn365.ops.version: Release 10.0.12
ms.openlocfilehash: a82af9e8ec1806f470103897389d0316d33a4a06
ms.sourcegitcommit: 7fec9dc5297ed6e687d4a0dff099922d59d6a830
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/13/2020
ms.locfileid: "3372731"
---
# <a name="get-started-with-the-cost-accounting-service-private-preview"></a><span data-ttu-id="9b164-103">Aan de slag met de service voor kostprijsboekhouding (particuliere preview)</span><span class="sxs-lookup"><span data-stu-id="9b164-103">Get started with the cost accounting service (private preview)</span></span>

[!INCLUDE [banner](../includes/banner.md)]

> [!IMPORTANT]
> <span data-ttu-id="9b164-104">De functionaliteit die in dit onderwerp wordt vermeld, is beschikbaar als onderdeel van een beperkte preview-versie.</span><span class="sxs-lookup"><span data-stu-id="9b164-104">The functionality that is described in this topic is available as part of a private preview release.</span></span> <span data-ttu-id="9b164-105">De inhoud van dit onderwerp en de functionaliteit die dit onderwerp beschrijft, kunnen worden gewijzigd.</span><span class="sxs-lookup"><span data-stu-id="9b164-105">The content of this topic and the functionality that it describes are subject to change.</span></span> <span data-ttu-id="9b164-106">Meer informatie over preview-versies vindt u in [Veelgestelde vragen over updates van service met één versie](../../fin-ops-core/fin-ops/get-started/one-version.md).</span><span class="sxs-lookup"><span data-stu-id="9b164-106">For more information about preview releases, see [One version service updates FAQ](../../fin-ops-core/fin-ops/get-started/one-version.md).</span></span>

<span data-ttu-id="9b164-107">Met de service kostprijsboekhouding kunt u meerdere voorraadboekingen uitvoeren in de grootboeken voor kostprijsboekhouding die u hebt ingesteld.</span><span class="sxs-lookup"><span data-stu-id="9b164-107">The cost accounting service lets you do multiple inventory accounting in the cost accounting ledgers that you've set up.</span></span> <span data-ttu-id="9b164-108">U koppelt alle grootboeken voor de kostenboekhouding aan een *conventie*.</span><span class="sxs-lookup"><span data-stu-id="9b164-108">You associate each cost accounting ledger with a *convention*.</span></span> <span data-ttu-id="9b164-109">Een conventie is een verzameling van de volgende typen boekhoudbeleidsregels:</span><span class="sxs-lookup"><span data-stu-id="9b164-109">A convention is a collection of the following types of accounting policies:</span></span>

- <span data-ttu-id="9b164-110">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="9b164-110">Cost object</span></span>
- <span data-ttu-id="9b164-111">Basis van invoermeting</span><span class="sxs-lookup"><span data-stu-id="9b164-111">Input measurement basis</span></span>
- <span data-ttu-id="9b164-112">Veronderstelling van kostenstroom</span><span class="sxs-lookup"><span data-stu-id="9b164-112">Cost flow assumption</span></span>
- <span data-ttu-id="9b164-113">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="9b164-113">Cost element</span></span>

> [!NOTE]
> <span data-ttu-id="9b164-114">Zelfs nadat u de service kostprijsboekhouding hebt ingeschakeld, kunt u nog gewoon voorraadboekhouding uitvoeren in Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="9b164-114">Even after you've turned on the cost accounting service, you can still do  inventory accounting in Microsoft Dynamics 365 Supply Chain Management, as usual.</span></span>

<span data-ttu-id="9b164-115">De service kostprijsboekhouding is een invoegtoepassing.</span><span class="sxs-lookup"><span data-stu-id="9b164-115">The cost accounting service is an add-in.</span></span> <span data-ttu-id="9b164-116">Om de functies beschikbaar te maken, moet u deze installeren vanuit Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="9b164-116">To makes its features available, you must install it from Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="9b164-117">Daarom kunt u ervoor kiezen om deze te evalueren in een testomgeving voordat u ze voor productie-omgevingen inschakelt.</span><span class="sxs-lookup"><span data-stu-id="9b164-117">Therefore, you can choose to evaluate it in a test environment before you turn it on for production environments.</span></span>

<span data-ttu-id="9b164-118">De kostprijsboekhouding biedt momenteel geen ondersteuning voor alle functies voor kostenbeheer die in Dynamics 365 Supply Chain Management zijn ingebouwd.</span><span class="sxs-lookup"><span data-stu-id="9b164-118">The cost accounting service doesn't currently support all the cost management features that are built into Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="9b164-119">Het is daarom belangrijk dat u evalueert of de functieset die momenteel beschikbaar is, voldoet aan uw behoeften.</span><span class="sxs-lookup"><span data-stu-id="9b164-119">Therefore, it's important that you evaluate whether the set of features that is currently available will meet your requirements.</span></span>

## <a name="how-to-get-the-cost-accounting-service-private-preview"></a><a name="sign-up"></a><span data-ttu-id="9b164-120">Aan de slag met de service voor kostprijsboekhouding (particuliere preview)</span><span class="sxs-lookup"><span data-stu-id="9b164-120">How to get the cost accounting service (private preview)</span></span>

> [!IMPORTANT]
> <span data-ttu-id="9b164-121">Als u de service kostprijsboekhouding wilt gebruiken, moet u beschikken over een omgeving met hoge beschikbaarheid voor LCS (geen OneBox-omgeving) en moet u Dynamics 365 Supply Chain Management versie 10.0.11 of hoger uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="9b164-121">To use the cost accounting service, you must have an LCS-enabled high-availability environment (not a OneBox environment), and you must be running Dynamics 365 Supply Chain Management version 10.0.11 or later.</span></span>

<span data-ttu-id="9b164-122">Als u zich wilt inschrijven voor de particuliere preview van de service voor kostprijsboekhouding, verzendt u uw LCS-omgeving-id via e-mail naar [Service kostprijsboekhouding (particuliere preview)](mailto:aevengir@microsoft.com?subject=Cost%20accounting%20service%20%28private%20preview%29).</span><span class="sxs-lookup"><span data-stu-id="9b164-122">To sign up for the cost accounting service private preview, please send your LCS environment ID by email to [Cost accounting service (private preview)](mailto:aevengir@microsoft.com?subject=Cost%20accounting%20service%20%28private%20preview%29).</span></span> <span data-ttu-id="9b164-123">Nadat u bent goedgekeurd voor het programma, ontvangt u een opvolgings-e-mailbericht met een bètasleutel voor de service voor kostprijsboekhouding.</span><span class="sxs-lookup"><span data-stu-id="9b164-123">On approving you for the program, we will send you a follow up email that contains a cost accounting service beta key.</span></span> <span data-ttu-id="9b164-124">Wanneer u de bètasleutel ontvangt, kunt u doorgaan door [de invoegtoepassing](#install) te installeren.</span><span class="sxs-lookup"><span data-stu-id="9b164-124">On receiving the beta key, you can proceed by [installing the add-in](#install).</span></span>

## <a name="licensing"></a><span data-ttu-id="9b164-125">Licenties</span><span class="sxs-lookup"><span data-stu-id="9b164-125">Licensing</span></span>

<span data-ttu-id="9b164-126">De service voor kostprijsboekhouding wordt samengevoegd met de standaardfuncties van voorraadboekhouding die beschikbaar zijn voor Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="9b164-126">The cost accounting service is licensed together with the standard features of inventory accounting that are available for Supply Chain Management.</span></span> <span data-ttu-id="9b164-127">U hoeft geen extra licentie aan te schaffen voor het gebruik van de service kostprijsboekhouding.</span><span class="sxs-lookup"><span data-stu-id="9b164-127">You don't have to purchase an additional license to use the cost accounting service.</span></span>

## <a name="install-the-add-in"></a><a name="install"></a><span data-ttu-id="9b164-128">De invoegtoepassing installeren</span><span class="sxs-lookup"><span data-stu-id="9b164-128">Install the add-in</span></span>

<span data-ttu-id="9b164-129">Als u de service kostprijsboekhouding wilt gebruiken, installeert u de invoegtoepassing voor kostprijsboekhouding in Supply Chain Management, zoals wordt beschreven in de volgende procedure.</span><span class="sxs-lookup"><span data-stu-id="9b164-129">To use the cost accounting service, install the cost accounting service add-in for Supply Chain Management as described in the following procedure.</span></span>

1. <span data-ttu-id="9b164-130">[Meld u aan](#sign-up) voor de service voor kostprijsboekhouding (particuliere preview).</span><span class="sxs-lookup"><span data-stu-id="9b164-130">[Sign up](#sign-up) for the cost accounting service (private preview).</span></span>

1. <span data-ttu-id="9b164-131">Meld u aan bij LCS.</span><span class="sxs-lookup"><span data-stu-id="9b164-131">Sign in to LCS.</span></span>

1. <span data-ttu-id="9b164-132">Ga naar **Beheer van previewfuncties**.</span><span class="sxs-lookup"><span data-stu-id="9b164-132">Go to **Preview feature management**.</span></span>

1. <span data-ttu-id="9b164-133">Selecteer het plusteken (**+**).</span><span class="sxs-lookup"><span data-stu-id="9b164-133">Select the plus sign (**+**).</span></span>

1. <span data-ttu-id="9b164-134">Voer in het veld **Code** de bètasleutel van de invoegtoepassing voor de kostprijsboekhouding in.</span><span class="sxs-lookup"><span data-stu-id="9b164-134">In the **Code** field, enter your add-in beta key for the cost accounting service.</span></span> <span data-ttu-id="9b164-135">(U hebt de sleutel per e-mail ontvangen.)</span><span class="sxs-lookup"><span data-stu-id="9b164-135">(You should have received your key by email.)</span></span>

1. <span data-ttu-id="9b164-136">Selecteer **Deblokkeren**.</span><span class="sxs-lookup"><span data-stu-id="9b164-136">Select **Unblock**.</span></span>

1. <span data-ttu-id="9b164-137">Open de LCS-omgeving waar u de service wilt toevoegen.</span><span class="sxs-lookup"><span data-stu-id="9b164-137">Open the LCS environment where you want to add the service.</span></span>

1. <span data-ttu-id="9b164-138">Ga naar **Volledige details**.</span><span class="sxs-lookup"><span data-stu-id="9b164-138">Go to **Full details**.</span></span>

1. <span data-ttu-id="9b164-139">Schuif omlaag naar het sneltabblad **Invoegtoepassingen voor omgeving**.</span><span class="sxs-lookup"><span data-stu-id="9b164-139">Scroll down to the **Environment add-ins** FastTab.</span></span>

1. <span data-ttu-id="9b164-140">Selecteer **Een nieuwe invoegtoepassing installeren**.</span><span class="sxs-lookup"><span data-stu-id="9b164-140">Select **Install a new add-in**.</span></span>

1. <span data-ttu-id="9b164-141">Selecteer **Service kostprijsboekhouding**.</span><span class="sxs-lookup"><span data-stu-id="9b164-141">Select **Cost accounting service**.</span></span>

1. <span data-ttu-id="9b164-142">Volg de installatiehandleiding en ga akkoord met de voorwaarden en bepalingen.</span><span class="sxs-lookup"><span data-stu-id="9b164-142">Follow the installation guide, and agree to the terms and conditions.</span></span>

1. <span data-ttu-id="9b164-143">Selecteer **Installeren**.</span><span class="sxs-lookup"><span data-stu-id="9b164-143">Select **Install**.</span></span>

1. <span data-ttu-id="9b164-144">Op het sneltabblad **Invoegtoepassingen voor omgeving** ziet u dat de service kostprijsboekhouding wordt geïnstalleerd.</span><span class="sxs-lookup"><span data-stu-id="9b164-144">On the **Environment add-ins** FastTab, you should see that the cost accounting service is being installed.</span></span> <span data-ttu-id="9b164-145">Na enkele minuten verandert de status van **Bezig met installeren** in **Geïnstalleerd**.</span><span class="sxs-lookup"><span data-stu-id="9b164-145">After a few minutes, the status should change from **Installing** to **Installed**.</span></span> <span data-ttu-id="9b164-146">(Mogelijk moet u de pagina vernieuwen om deze wijziging te zien.) Op dat moment is de service voor kostprijsboekhouding klaar voor gebruik.</span><span class="sxs-lookup"><span data-stu-id="9b164-146">(You might have to refresh the page to see this change.) At that point, the cost accounting service is ready for use.</span></span>

## <a name="set-up-the-integration"></a><span data-ttu-id="9b164-147">De integratie instellen</span><span class="sxs-lookup"><span data-stu-id="9b164-147">Set up the integration</span></span>

<span data-ttu-id="9b164-148">De integratie instellen tussen de service kostprijsboekhouding en Dynamics 365 Supply Chain Management:</span><span class="sxs-lookup"><span data-stu-id="9b164-148">To set up the integration between the cost accounting service and Dynamics 365 Supply Chain Management:</span></span>

1. <span data-ttu-id="9b164-149">Ga naar **Systeembeheer > Functiebeheer**.</span><span class="sxs-lookup"><span data-stu-id="9b164-149">Go to **System administration > Feature Management**.</span></span>

1. <span data-ttu-id="9b164-150">Selecteer **Controleren op updates**.</span><span class="sxs-lookup"><span data-stu-id="9b164-150">Select **Check for updates**.</span></span>

1. <span data-ttu-id="9b164-151">Open het tabblad **Alles** en zoek de functie met de naam *Service kostprijsboekhouding*.</span><span class="sxs-lookup"><span data-stu-id="9b164-151">Open the **All** tab and search for the feature named *Cost accounting service*.</span></span>

1. <span data-ttu-id="9b164-152">Selecteer **Nu inschakelen**.</span><span class="sxs-lookup"><span data-stu-id="9b164-152">Select **Enable now**.</span></span>

1. <span data-ttu-id="9b164-153">Ga naar **Kostenbeheer > Service kostprijsboekhouding > Instellen > Parameters service kostprijsboekhouding > Integratieparameters**.</span><span class="sxs-lookup"><span data-stu-id="9b164-153">Go to **Cost management > Cost accounting service > Setup > Cost accounting service parameters > Integrations parameters**.</span></span>

1. <span data-ttu-id="9b164-154">Voer in het veld **Toepassings-id** de volgende code in:</span><span class="sxs-lookup"><span data-stu-id="9b164-154">In the **Application ID** field, enter the following code:</span></span><br> <span data-ttu-id="9b164-155">08231eb2-a501-4edb-b3c5-aede5e5e0c3f</span><span class="sxs-lookup"><span data-stu-id="9b164-155">08231eb2-a501-4edb-b3c5-aede5e5e0c3f</span></span>

1. <span data-ttu-id="9b164-156">Voer in het veld **Eindpunt gegevensservice** de volgende URL in:</span><span class="sxs-lookup"><span data-stu-id="9b164-156">In the **Data service endpoint** field, enter the following URL:</span></span><br>https://operationsdataservice.operations365.dynamics.com/

1. <span data-ttu-id="9b164-157">Voer in het veld **Eindpunt service kostenboekhouding** de volgende URL in:</span><span class="sxs-lookup"><span data-stu-id="9b164-157">In the **Cost accounting service endpoint** field, enter the following URL:</span></span><br>https://costaccountingservice.operations365.dynamics.com/

1. <span data-ttu-id="9b164-158">De service kostprijsboekhouding is nu klaar voor gebruik.</span><span class="sxs-lookup"><span data-stu-id="9b164-158">The cost accounting service is now ready for use.</span></span>

## <a name="related-resources"></a><span data-ttu-id="9b164-159">Gerelateerde bronnen</span><span class="sxs-lookup"><span data-stu-id="9b164-159">Related resources</span></span>

[<span data-ttu-id="9b164-160">Startpagina van service Kostprijsboekhouding</span><span class="sxs-lookup"><span data-stu-id="9b164-160">Cost accounting service home page</span></span>](cost-accounting-service-home.md)
