---
title: De invoegtoepassing IoT-intelligentie installeren in LCS
description: In dit onderwerp wordt uitgelegd hoe u de invoegtoepassing IoT-intelligentie kunt installeren in Microsoft Dynamics Lifecycle Services (LCS).
author: robinarh
manager: tfehr
ms.date: 07/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2020-04-04
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: ad8b33633646f27bc368dc4bbedc1eb64c150a9f
ms.sourcegitcommit: 092ef6a45f515b38be2a4481abdbe7518a636f85
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4425755"
---
# <a name="install-the-iot-intelligence-add-in-in-lcs"></a><span data-ttu-id="42ad6-103">De invoegtoepassing IoT-intelligentie installeren in LCS</span><span class="sxs-lookup"><span data-stu-id="42ad6-103">Install the IoT Intelligence add-in in LCS</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="42ad6-104">In dit onderwerp wordt uitgelegd hoe u de invoegtoepassing IoT-intelligentie kunt installeren in Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="42ad6-104">This topic explains how to install the IoT Intelligence add-in in Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="42ad6-105">Invoegtoepassingen kunnen niet worden geïnstalleerd in een demo-/proefomgeving.</span><span class="sxs-lookup"><span data-stu-id="42ad6-105">Note that add-ins cannot be installed on a demo/trial environment.</span></span> <span data-ttu-id="42ad6-106">Voordat u de invoeg toepassing kunt installeren, moet u [de Azure-resources maken](iot-azure-setup.md).</span><span class="sxs-lookup"><span data-stu-id="42ad6-106">Before you can install the add-in, you must [create the Azure resources](iot-azure-setup.md).</span></span>

## <a name="set-up-the-lcs-environment"></a><span data-ttu-id="42ad6-107">De LCS-omgeving instellen</span><span class="sxs-lookup"><span data-stu-id="42ad6-107">Set up the LCS environment</span></span>

1. <span data-ttu-id="42ad6-108">Open LCS en ga naar uw Microsoft Dynamics 365 Supply Chain Management-omgeving.</span><span class="sxs-lookup"><span data-stu-id="42ad6-108">Open LCS, and go to your Microsoft Dynamics 365 Supply Chain Management environment.</span></span>
2. <span data-ttu-id="42ad6-109">Schuif naar de sectie **Invoegtoepassingen voor omgeving**.</span><span class="sxs-lookup"><span data-stu-id="42ad6-109">Scroll to the **Environment add-ins** section.</span></span>
3. <span data-ttu-id="42ad6-110">Selecteer **Een nieuwe invoegtoepassing installeren** om de lijst met invoegtoepassingen weer te geven die zijn ingeschakeld voor de omgeving.</span><span class="sxs-lookup"><span data-stu-id="42ad6-110">Select **Install a new add-in** to show the list of add-ins that have been enabled for the environment.</span></span>
4. <span data-ttu-id="42ad6-111">Selecteer in het dialoogvenster **Een invoegtoepassing selecteren voor installatie** de optie **IoT-intelligentie**.</span><span class="sxs-lookup"><span data-stu-id="42ad6-111">In the **Select an add-in to install** dialog box, select **IoT Intelligence**.</span></span>
5. <span data-ttu-id="42ad6-112">Geef in het dialoogvenster **Invoegtoepassing instellen** de details op van uw IOT-hub en Redis-cache.</span><span class="sxs-lookup"><span data-stu-id="42ad6-112">In the **Setup add-in** dialog box, provide the details of your IoT hub and Redis cache.</span></span> <span data-ttu-id="42ad6-113">U kunt de vereiste waarden vinden in de sleutelkluis die u hebt gemaakt in [Azure-resources maken](iot-azure-setup.md).</span><span class="sxs-lookup"><span data-stu-id="42ad6-113">You can find the required values in the key vault that you created in [Create Azure resources](iot-azure-setup.md).</span></span>

    + <span data-ttu-id="42ad6-114">**Tenant-id**: ga in de Azure-portal naar de sleutelkluis en selecteer vervolgens in het linkernavigatiedeelvenster de optie **Overzicht** en kopieer de waarde voor **Directory-id**.</span><span class="sxs-lookup"><span data-stu-id="42ad6-114">**Tenant ID** – In the Azure portal, go to the key vault, and then, in the left navigation pane, select **Overview**, and copy the **Directory ID** value.</span></span> <span data-ttu-id="42ad6-115">Plak die waarde in het dialoogvenster **Invoegtoepassing instellen**.</span><span class="sxs-lookup"><span data-stu-id="42ad6-115">Paste that value in the **Setup add-in** dialog box.</span></span>
    + <span data-ttu-id="42ad6-116">**URI van sleutelkluis voor eindpunt dat compatibel is met IoT Event hub**: ga naar de sleutelkluis en selecteer vervolgens in het linkernavigatiedeelvenster de optie **Overzicht** en kopieer de waarde voor **DNS-naam**.</span><span class="sxs-lookup"><span data-stu-id="42ad6-116">**IoT Event Hub-compatible endpoint Key Vault URI** – Go to the key vault, and then, in the left navigation pane, select **Overview**, and copy the **DNS name** value.</span></span> <span data-ttu-id="42ad6-117">Plak die waarde in het dialoogvenster **Invoegtoepassing instellen**.</span><span class="sxs-lookup"><span data-stu-id="42ad6-117">Paste that value in the **Setup add-in** dialog box.</span></span>
    + <span data-ttu-id="42ad6-118">**Geheime naam van eindpunt dat compatibel is met IoT Event hub**: ga naar de sleutelkluis, selecteer in het linkernavigatiedeelvenster de optie **Geheimen** en kopieer de naam van het geheim waar de verbindingsreeks van de Event hub voor de IoT-hub is opgeslagen.</span><span class="sxs-lookup"><span data-stu-id="42ad6-118">**IoT Event Hub-compatible endpoint secret name** – Go to the key vault, and then, in the left navigation pane, select **Secrets**, and copy the name of the secret where the event hub connection string for the IoT hub is stored.</span></span> <span data-ttu-id="42ad6-119">Plak die waarde in het dialoogvenster **Invoegtoepassing instellen**.</span><span class="sxs-lookup"><span data-stu-id="42ad6-119">Paste that value in the **Setup add-in** dialog box.</span></span>
    + <span data-ttu-id="42ad6-120">**URI van sleutelkluis voor Redis-cache**: ga naar de sleutelkluis en selecteer vervolgens in het linkernavigatiedeelvenster de optie **Overzicht** en kopieer de waarde voor **DNS-naam**.</span><span class="sxs-lookup"><span data-stu-id="42ad6-120">**Redis cache key vault URI** – Go to the key vault, and then, in the left navigation pane, select **Overview**, and copy the **DNS name** value.</span></span> <span data-ttu-id="42ad6-121">Plak die waarde in het dialoogvenster **Invoegtoepassing instellen**.</span><span class="sxs-lookup"><span data-stu-id="42ad6-121">Paste that value in the **Setup add-in** dialog box.</span></span>
    + <span data-ttu-id="42ad6-122">**Geheime naam van eindpunt voor Redis-cache**: ga naar de sleutelkluis, selecteer in het linkernavigatiedeelvenster de optie **Geheimen** en kopieer de naam van het geheim waar de verbindingsreeks voor de Redis-cache is opgeslagen.</span><span class="sxs-lookup"><span data-stu-id="42ad6-122">**Redis cache endpoint secret name** – Go to the key vault, and then, in the left navigation pane, select **Secrets**, and copy the name of the secret where the connection string for the Redis cache is stored.</span></span> <span data-ttu-id="42ad6-123">Plak die waarde in het dialoogvenster **Invoegtoepassing instellen**.</span><span class="sxs-lookup"><span data-stu-id="42ad6-123">Paste that value in the **Setup add-in** dialog box.</span></span>

6. <span data-ttu-id="42ad6-124">Schakel het selectievakje in om de voorwaarden te accepteren.</span><span class="sxs-lookup"><span data-stu-id="42ad6-124">Select the check box to accept the terms and conditions.</span></span>
7. <span data-ttu-id="42ad6-125">Selecteer **Installeren**.</span><span class="sxs-lookup"><span data-stu-id="42ad6-125">Select **Install**.</span></span>
8. <span data-ttu-id="42ad6-126">Er verschijnt een berichtvenster met de mededeling dat de invoegtoepassing is geactiveerd voor installatie.</span><span class="sxs-lookup"><span data-stu-id="42ad6-126">A message box appears that states, "Add-in has been successfully triggered for installation."</span></span> <span data-ttu-id="42ad6-127">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="42ad6-127">Select **OK**.</span></span>

<span data-ttu-id="42ad6-128">LCS-instelling is nu voltooid.</span><span class="sxs-lookup"><span data-stu-id="42ad6-128">LCS setup is now completed.</span></span> <span data-ttu-id="42ad6-129">De volgende stap is het [instellen van de scenario's](iot-scenario-setup.md).</span><span class="sxs-lookup"><span data-stu-id="42ad6-129">The next step is to [set up the scenarios](iot-scenario-setup.md).</span></span>

## <a name="uninstall-the-add-in"></a><a id="uninstall-addin"></a><span data-ttu-id="42ad6-130">De invoegtoepassing verwijderen</span><span class="sxs-lookup"><span data-stu-id="42ad6-130">Uninstall the add-in</span></span>

1. <span data-ttu-id="42ad6-131">[Schakel de scenario's uit](iot-scenario-setup.md#disable-a-scenario) in Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="42ad6-131">In Supply Chain Management, [disable the scenarios](iot-scenario-setup.md#disable-a-scenario).</span></span>
2. <span data-ttu-id="42ad6-132">Ga in LCS naar de details van uw Supply Chain Management-omgeving.</span><span class="sxs-lookup"><span data-stu-id="42ad6-132">In LCS, go to your Supply Chain Management environment details.</span></span>
3. <span data-ttu-id="42ad6-133">Schuif naar de sectie **Invoegtoepassingen voor omgeving**.</span><span class="sxs-lookup"><span data-stu-id="42ad6-133">Scroll to the **Environment add-ins** section.</span></span>
4. <span data-ttu-id="42ad6-134">Selecteer **Verwijderen** voor de invoegtoepassing IoT-intelligentie.</span><span class="sxs-lookup"><span data-stu-id="42ad6-134">Select **Uninstall** for the IoT Intelligence add-in.</span></span>
