---
title: Aan de slag met de service kostprijsboekhouding
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
ms.openlocfilehash: cbbce7eaac264973bf0b95ad5175bf70ed2b4ae9
ms.sourcegitcommit: e06da171b9cba8163893e30244c52a9ce0901146
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/21/2020
ms.locfileid: "3276904"
---
# <a name="get-started-with-the-cost-accounting-service"></a><span data-ttu-id="a36a7-103">Aan de slag met de service kostprijsboekhouding</span><span class="sxs-lookup"><span data-stu-id="a36a7-103">Get started with the cost accounting service</span></span>

[!INCLUDE [banner](../includes/banner.md)]

> [!IMPORTANT]
> <span data-ttu-id="a36a7-104">De functionaliteit die in dit onderwerp wordt vermeld, is beschikbaar als onderdeel van een beperkte preview-versie.</span><span class="sxs-lookup"><span data-stu-id="a36a7-104">The functionality that is described in this topic is available as part of a private preview release.</span></span> <span data-ttu-id="a36a7-105">De inhoud van dit onderwerp en de functionaliteit die dit onderwerp beschrijft, kunnen worden gewijzigd.</span><span class="sxs-lookup"><span data-stu-id="a36a7-105">The content of this topic and the functionality that it describes are subject to change.</span></span> <span data-ttu-id="a36a7-106">Meer informatie over preview-versies vindt u in [Veelgestelde vragen over updates van service met één versie](../../fin-ops-core/fin-ops/get-started/one-version.md).</span><span class="sxs-lookup"><span data-stu-id="a36a7-106">For more information about preview releases, see [One version service updates FAQ](../../fin-ops-core/fin-ops/get-started/one-version.md).</span></span>

<span data-ttu-id="a36a7-107">Met de service kostprijsboekhouding kunt u meerdere voorraadboekingen uitvoeren in de grootboeken voor kostprijsboekhouding die u hebt ingesteld.</span><span class="sxs-lookup"><span data-stu-id="a36a7-107">The cost accounting service lets you do multiple inventory accounting in the cost accounting ledgers that you've set up.</span></span> <span data-ttu-id="a36a7-108">U koppelt alle grootboeken voor de kostenboekhouding aan een *conventie*.</span><span class="sxs-lookup"><span data-stu-id="a36a7-108">You associate each cost accounting ledger with a *convention*.</span></span> <span data-ttu-id="a36a7-109">Een conventie is een verzameling van de volgende typen boekhoudbeleidsregels:</span><span class="sxs-lookup"><span data-stu-id="a36a7-109">A convention is a collection of the following types of accounting policies:</span></span>

- <span data-ttu-id="a36a7-110">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="a36a7-110">Cost object</span></span>
- <span data-ttu-id="a36a7-111">Basis van invoermeting</span><span class="sxs-lookup"><span data-stu-id="a36a7-111">Input measurement basis</span></span>
- <span data-ttu-id="a36a7-112">Veronderstelling van kostenstroom</span><span class="sxs-lookup"><span data-stu-id="a36a7-112">Cost flow assumption</span></span>
- <span data-ttu-id="a36a7-113">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="a36a7-113">Cost element</span></span>

> [!NOTE]
> <span data-ttu-id="a36a7-114">Zelfs nadat u de service kostprijsboekhouding hebt ingeschakeld, kunt u nog gewoon voorraadboekhouding uitvoeren in Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="a36a7-114">Even after you've turned on the cost accounting service, you can still do  inventory accounting in Microsoft Dynamics 365 Supply Chain Management, as usual.</span></span>

<span data-ttu-id="a36a7-115">De service kostprijsboekhouding is een invoegtoepassing.</span><span class="sxs-lookup"><span data-stu-id="a36a7-115">The cost accounting service is an add-in.</span></span> <span data-ttu-id="a36a7-116">Om de functies beschikbaar te maken, moet u deze installeren vanuit Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="a36a7-116">To makes its features available, you must install it from Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="a36a7-117">Daarom kunt u ervoor kiezen om deze te evalueren in een testomgeving voordat u ze voor productie-omgevingen inschakelt.</span><span class="sxs-lookup"><span data-stu-id="a36a7-117">Therefore, you can choose to evaluate it in a test environment before you turn it on for production environments.</span></span>

<span data-ttu-id="a36a7-118">De kostprijsboekhouding biedt momenteel geen ondersteuning voor alle functies voor kostenbeheer die in Dynamics 365 Supply Chain Management zijn ingebouwd.</span><span class="sxs-lookup"><span data-stu-id="a36a7-118">The cost accounting service doesn't currently support all the cost management features that are built into Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="a36a7-119">Het is daarom belangrijk dat u evalueert of de functieset die momenteel beschikbaar is, voldoet aan uw behoeften.</span><span class="sxs-lookup"><span data-stu-id="a36a7-119">Therefore, it's important that you evaluate whether the set of features that is currently available will meet your requirements.</span></span>

## <a name="licensing"></a><span data-ttu-id="a36a7-120">Licenties</span><span class="sxs-lookup"><span data-stu-id="a36a7-120">Licensing</span></span>

<span data-ttu-id="a36a7-121">De service voor kostprijsboekhouding wordt samengevoegd met de standaardfuncties van voorraadboekhouding die beschikbaar zijn voor Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="a36a7-121">The cost accounting service is licensed together with the standard features of inventory accounting that are available for Supply Chain Management.</span></span> <span data-ttu-id="a36a7-122">U hoeft geen extra licentie aan te schaffen voor het gebruik van de service kostprijsboekhouding.</span><span class="sxs-lookup"><span data-stu-id="a36a7-122">You don't have to purchase an additional license to use the cost accounting service.</span></span>

## <a name="install-the-add-in"></a><span data-ttu-id="a36a7-123">De invoegtoepassing installeren</span><span class="sxs-lookup"><span data-stu-id="a36a7-123">Install the add-in</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a36a7-124">Als u de service kostprijsboekhouding wilt gebruiken, moet u beschikken over een omgeving met hoge beschikbaarheid voor LCS (geen OneBox-omgeving) en moet u Dynamics 365 Supply Chain Management versie 10.0.11 of hoger uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="a36a7-124">To use the cost accounting service, you must have an LCS-enabled high-availability environment (not a OneBox environment), and you must be running Dynamics 365 Supply Chain Management version 10.0.11 or later.</span></span>

<span data-ttu-id="a36a7-125">Als u de service kostprijsboekhouding wilt gebruiken, installeert u de invoegtoepassing voor kostprijsboekhouding in Supply Chain Management, zoals wordt beschreven in de volgende procedure.</span><span class="sxs-lookup"><span data-stu-id="a36a7-125">To use the cost accounting service, install the cost accounting service add-in for Supply Chain Management as described in the following procedure.</span></span>

1. <span data-ttu-id="a36a7-126">Meld u aan bij LCS.</span><span class="sxs-lookup"><span data-stu-id="a36a7-126">Sign in to LCS.</span></span>

1. <span data-ttu-id="a36a7-127">Ga naar **Beheer van previewfuncties**.</span><span class="sxs-lookup"><span data-stu-id="a36a7-127">Go to **Preview feature management**.</span></span>

1. <span data-ttu-id="a36a7-128">Selecteer het plusteken (**+**).</span><span class="sxs-lookup"><span data-stu-id="a36a7-128">Select the plus sign (**+**).</span></span>

1. <span data-ttu-id="a36a7-129">Voer in het veld **Code** de bètasleutel van de invoegtoepassing voor de kostprijsboekhouding in.</span><span class="sxs-lookup"><span data-stu-id="a36a7-129">In the **Code** field, enter your add-in beta key for the cost accounting service.</span></span> <span data-ttu-id="a36a7-130">(U hebt de sleutel per e-mail ontvangen.)</span><span class="sxs-lookup"><span data-stu-id="a36a7-130">(You should have received your key by email.)</span></span>

1. <span data-ttu-id="a36a7-131">Selecteer **Deblokkeren**.</span><span class="sxs-lookup"><span data-stu-id="a36a7-131">Select **Unblock**.</span></span>

1. <span data-ttu-id="a36a7-132">Open de LCS-omgeving waar u de service wilt toevoegen.</span><span class="sxs-lookup"><span data-stu-id="a36a7-132">Open the LCS environment where you want to add the service.</span></span>

1. <span data-ttu-id="a36a7-133">Ga naar **Volledige details**.</span><span class="sxs-lookup"><span data-stu-id="a36a7-133">Go to **Full details**.</span></span>

1. <span data-ttu-id="a36a7-134">Schuif omlaag naar het sneltabblad **Invoegtoepassingen voor omgeving**.</span><span class="sxs-lookup"><span data-stu-id="a36a7-134">Scroll down to the **Environment add-ins** FastTab.</span></span>

1. <span data-ttu-id="a36a7-135">Selecteer **Een nieuwe invoegtoepassing installeren**.</span><span class="sxs-lookup"><span data-stu-id="a36a7-135">Select **Install a new add-in**.</span></span>

1. <span data-ttu-id="a36a7-136">Selecteer **Service kostprijsboekhouding**.</span><span class="sxs-lookup"><span data-stu-id="a36a7-136">Select **Cost accounting service**.</span></span>

1. <span data-ttu-id="a36a7-137">Volg de installatiehandleiding en ga akkoord met de voorwaarden en bepalingen.</span><span class="sxs-lookup"><span data-stu-id="a36a7-137">Follow the installation guide, and agree to the terms and conditions.</span></span>

1. <span data-ttu-id="a36a7-138">Selecteer **Installeren**.</span><span class="sxs-lookup"><span data-stu-id="a36a7-138">Select **Install**.</span></span>

1. <span data-ttu-id="a36a7-139">Op het sneltabblad **Invoegtoepassingen voor omgeving** ziet u dat de service kostprijsboekhouding wordt geïnstalleerd.</span><span class="sxs-lookup"><span data-stu-id="a36a7-139">On the **Environment add-ins** FastTab, you should see that the cost accounting service is being installed.</span></span> <span data-ttu-id="a36a7-140">Na enkele minuten verandert de status van **Bezig met installeren** in **Geïnstalleerd**.</span><span class="sxs-lookup"><span data-stu-id="a36a7-140">After a few minutes, the status should change from **Installing** to **Installed**.</span></span> <span data-ttu-id="a36a7-141">(Mogelijk moet u de pagina vernieuwen om deze wijziging te zien.) Op dat moment is de service voor kostprijsboekhouding klaar voor gebruik.</span><span class="sxs-lookup"><span data-stu-id="a36a7-141">(You might have to refresh the page to see this change.) At that point, the cost accounting service is ready for use.</span></span>

## <a name="set-up-the-integration"></a><span data-ttu-id="a36a7-142">De integratie instellen</span><span class="sxs-lookup"><span data-stu-id="a36a7-142">Set up the integration</span></span>

<span data-ttu-id="a36a7-143">De integratie instellen tussen de service kostprijsboekhouding en Dynamics 365 Supply Chain Management:</span><span class="sxs-lookup"><span data-stu-id="a36a7-143">To set up the integration between the cost accounting service and Dynamics 365 Supply Chain Management:</span></span>

1. <span data-ttu-id="a36a7-144">Ga naar **Systeembeheer > Functiebeheer**.</span><span class="sxs-lookup"><span data-stu-id="a36a7-144">Go to **System administration > Feature Management**.</span></span>

1. <span data-ttu-id="a36a7-145">Selecteer **Controleren op updates**.</span><span class="sxs-lookup"><span data-stu-id="a36a7-145">Select **Check for updates**.</span></span>

1. <span data-ttu-id="a36a7-146">Open het tabblad **Alles** en zoek de functie met de naam *Service kostprijsboekhouding*.</span><span class="sxs-lookup"><span data-stu-id="a36a7-146">Open the **All** tab and search for the feature named *Cost accounting service*.</span></span>

1. <span data-ttu-id="a36a7-147">Selecteer **Nu inschakelen**.</span><span class="sxs-lookup"><span data-stu-id="a36a7-147">Select **Enable now**.</span></span>

1. <span data-ttu-id="a36a7-148">Ga naar **Kostenbeheer > Service kostprijsboekhouding > Instellen > Parameters service kostprijsboekhouding > Integratieparameters**.</span><span class="sxs-lookup"><span data-stu-id="a36a7-148">Go to **Cost management > Cost accounting service > Setup > Cost accounting service parameters > Integrations parameters**.</span></span>

1. <span data-ttu-id="a36a7-149">Voer in het veld **Toepassings-id** de volgende code in:</span><span class="sxs-lookup"><span data-stu-id="a36a7-149">In the **Application ID** field, enter the following code:</span></span><br> <span data-ttu-id="a36a7-150">08231eb2-a501-4edb-b3c5-aede5e5e0c3f</span><span class="sxs-lookup"><span data-stu-id="a36a7-150">08231eb2-a501-4edb-b3c5-aede5e5e0c3f</span></span>

1. <span data-ttu-id="a36a7-151">Voer in het veld **Eindpunt gegevensservice** de volgende URL in:</span><span class="sxs-lookup"><span data-stu-id="a36a7-151">In the **Data service endpoint** field, enter the following URL:</span></span><br>https://operationsdataservice.operations365.dynamics.com/

1. <span data-ttu-id="a36a7-152">Voer in het veld **Eindpunt service kostenboekhouding** de volgende URL in:</span><span class="sxs-lookup"><span data-stu-id="a36a7-152">In the **Cost accounting service endpoint** field, enter the following URL:</span></span><br>https://costaccountingservice.operations365.dynamics.com/

1. <span data-ttu-id="a36a7-153">De service kostprijsboekhouding is nu klaar voor gebruik.</span><span class="sxs-lookup"><span data-stu-id="a36a7-153">The cost accounting service is now ready for use.</span></span>

## <a name="related-resources"></a><span data-ttu-id="a36a7-154">Gerelateerde bronnen</span><span class="sxs-lookup"><span data-stu-id="a36a7-154">Related resources</span></span>

[<span data-ttu-id="a36a7-155">Startpagina van service Kostprijsboekhouding</span><span class="sxs-lookup"><span data-stu-id="a36a7-155">Cost accounting service home page</span></span>](cost-accounting-service-home.md)
