---
title: De invoegtoepassing IoT-intelligentie installeren in LCS
description: In dit onderwerp wordt uitgelegd hoe u de invoegtoepassing IoT-intelligentie kunt installeren in Microsoft Dynamics Lifecycle Services (LCS).
author: robinarh
manager: AnnBe
ms.date: 08/16/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: ''
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: ''
ms.search.validFrom: 2020-04-04
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 04333b3659f090b15cc0d0ee216f14dabc588883
ms.sourcegitcommit: 261b70ea358b2c231e20f320ed8bd6adc1e7d715
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/19/2020
ms.locfileid: "3386501"
---
# <a name="install-the-iot-intelligence-add-in-in-lcs"></a><span data-ttu-id="772a2-103">De invoegtoepassing IoT-intelligentie installeren in LCS</span><span class="sxs-lookup"><span data-stu-id="772a2-103">Install the IoT Intelligence add-in in LCS</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="772a2-104">In dit onderwerp wordt uitgelegd hoe u de invoegtoepassing IoT-intelligentie kunt installeren in Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="772a2-104">This topic explains how to install the IoT Intelligence add-in in Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="772a2-105">Voordat u de invoeg toepassing kunt installeren, moet u [de Azure-resources maken](iot-azure-setup.md).</span><span class="sxs-lookup"><span data-stu-id="772a2-105">Before you can install the add-in, you must [create the Azure resources](iot-azure-setup.md).</span></span>

## <a name="set-up-the-lcs-environment"></a><span data-ttu-id="772a2-106">De LCS-omgeving instellen</span><span class="sxs-lookup"><span data-stu-id="772a2-106">Set up the LCS environment</span></span>

1. <span data-ttu-id="772a2-107">Open LCS en ga naar uw Microsoft Dynamics 365 Supply Chain Management-omgeving.</span><span class="sxs-lookup"><span data-stu-id="772a2-107">Open LCS, and go to your Microsoft Dynamics 365 Supply Chain Management environment.</span></span>
2. <span data-ttu-id="772a2-108">Schuif naar de sectie **Invoegtoepassingen voor omgeving**.</span><span class="sxs-lookup"><span data-stu-id="772a2-108">Scroll to the **Environment add-ins** section.</span></span>
3. <span data-ttu-id="772a2-109">Selecteer **Een nieuwe invoegtoepassing installeren** om de lijst met invoegtoepassingen weer te geven die zijn ingeschakeld voor de omgeving.</span><span class="sxs-lookup"><span data-stu-id="772a2-109">Select **Install a new add-in** to show the list of add-ins that have been enabled for the environment.</span></span>
4. <span data-ttu-id="772a2-110">Selecteer in het dialoogvenster **Een invoegtoepassing selecteren voor installatie** de optie **IoT-intelligentie**.</span><span class="sxs-lookup"><span data-stu-id="772a2-110">In the **Select an add-in to install** dialog box, select **IoT Intelligence**.</span></span>
5. <span data-ttu-id="772a2-111">Geef in het dialoogvenster **Invoegtoepassing instellen** de details op van uw IOT-hub en Redis-cache.</span><span class="sxs-lookup"><span data-stu-id="772a2-111">In the **Setup add-in** dialog box, provide the details of your IoT hub and Redis cache.</span></span> <span data-ttu-id="772a2-112">U kunt de vereiste waarden vinden in de sleutelkluis die u hebt gemaakt in [Azure-resources maken](iot-azure-setup.md).</span><span class="sxs-lookup"><span data-stu-id="772a2-112">You can find the required values in the key vault that you created in [Create Azure resources](iot-azure-setup.md).</span></span>

    + <span data-ttu-id="772a2-113">**Tenant-id**: ga in de Azure-portal naar de sleutelkluis en selecteer vervolgens in het linkernavigatiedeelvenster de optie **Overzicht** en kopieer de waarde voor **Directory-id**.</span><span class="sxs-lookup"><span data-stu-id="772a2-113">**Tenant ID** – In the Azure portal, go to the key vault, and then, in the left navigation pane, select **Overview**, and copy the **Directory ID** value.</span></span> <span data-ttu-id="772a2-114">Plak die waarde in het dialoogvenster **Invoegtoepassing instellen**.</span><span class="sxs-lookup"><span data-stu-id="772a2-114">Paste that value in the **Setup add-in** dialog box.</span></span>
    + <span data-ttu-id="772a2-115">**URI van sleutelkluis voor eindpunt dat compatibel is met IoT Event hub**: ga naar de sleutelkluis en selecteer vervolgens in het linkernavigatiedeelvenster de optie **Overzicht** en kopieer de waarde voor **DNS-naam**.</span><span class="sxs-lookup"><span data-stu-id="772a2-115">**IoT Event Hub-compatible endpoint Key Vault URI** – Go to the key vault, and then, in the left navigation pane, select **Overview**, and copy the **DNS name** value.</span></span> <span data-ttu-id="772a2-116">Plak die waarde in het dialoogvenster **Invoegtoepassing instellen**.</span><span class="sxs-lookup"><span data-stu-id="772a2-116">Paste that value in the **Setup add-in** dialog box.</span></span>
    + <span data-ttu-id="772a2-117">**Geheime naam van eindpunt dat compatibel is met IoT Event hub**: ga naar de sleutelkluis, selecteer in het linkernavigatiedeelvenster de optie **Geheimen** en kopieer de naam van het geheim waar de verbindingsreeks van de Event hub voor de IoT-hub is opgeslagen.</span><span class="sxs-lookup"><span data-stu-id="772a2-117">**IoT Event Hub-compatible endpoint secret name** – Go to the key vault, and then, in the left navigation pane, select **Secrets**, and copy the name of the secret where the event hub connection string for the IoT hub is stored.</span></span> <span data-ttu-id="772a2-118">Plak die waarde in het dialoogvenster **Invoegtoepassing instellen**.</span><span class="sxs-lookup"><span data-stu-id="772a2-118">Paste that value in the **Setup add-in** dialog box.</span></span>
    + <span data-ttu-id="772a2-119">**URI van sleutelkluis voor Redis-cache**: ga naar de sleutelkluis en selecteer vervolgens in het linkernavigatiedeelvenster de optie **Overzicht** en kopieer de waarde voor **DNS-naam**.</span><span class="sxs-lookup"><span data-stu-id="772a2-119">**Redis cache key vault URI** – Go to the key vault, and then, in the left navigation pane, select **Overview**, and copy the **DNS name** value.</span></span> <span data-ttu-id="772a2-120">Plak die waarde in het dialoogvenster **Invoegtoepassing instellen**.</span><span class="sxs-lookup"><span data-stu-id="772a2-120">Paste that value in the **Setup add-in** dialog box.</span></span>
    + <span data-ttu-id="772a2-121">**Geheime naam van eindpunt voor Redis-cache**: ga naar de sleutelkluis, selecteer in het linkernavigatiedeelvenster de optie **Geheimen** en kopieer de naam van het geheim waar de verbindingsreeks voor de Redis-cache is opgeslagen.</span><span class="sxs-lookup"><span data-stu-id="772a2-121">**Redis cache endpoint secret name** – Go to the key vault, and then, in the left navigation pane, select **Secrets**, and copy the name of the secret where the connection string for the Redis cache is stored.</span></span> <span data-ttu-id="772a2-122">Plak die waarde in het dialoogvenster **Invoegtoepassing instellen**.</span><span class="sxs-lookup"><span data-stu-id="772a2-122">Paste that value in the **Setup add-in** dialog box.</span></span>

6. <span data-ttu-id="772a2-123">Schakel het selectievakje in om de voorwaarden te accepteren.</span><span class="sxs-lookup"><span data-stu-id="772a2-123">Select the check box to accept the terms and conditions.</span></span>
7. <span data-ttu-id="772a2-124">Selecteer **Installeren**.</span><span class="sxs-lookup"><span data-stu-id="772a2-124">Select **Install**.</span></span>
8. <span data-ttu-id="772a2-125">Er verschijnt een berichtvenster met de mededeling dat de invoegtoepassing is geactiveerd voor installatie.</span><span class="sxs-lookup"><span data-stu-id="772a2-125">A message box appears that states, "Add-in has been successfully triggered for installation."</span></span> <span data-ttu-id="772a2-126">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="772a2-126">Select **OK**.</span></span>

<span data-ttu-id="772a2-127">LCS-instelling is nu voltooid.</span><span class="sxs-lookup"><span data-stu-id="772a2-127">LCS setup is now completed.</span></span> <span data-ttu-id="772a2-128">De volgende stap is het [instellen van de scenario's](iot-scenario-setup.md).</span><span class="sxs-lookup"><span data-stu-id="772a2-128">The next step is to [set up the scenarios](iot-scenario-setup.md).</span></span>

## <a name="uninstall-the-add-in"></a><a id="uninstall-addin"></a><span data-ttu-id="772a2-129">De invoegtoepassing verwijderen</span><span class="sxs-lookup"><span data-stu-id="772a2-129">Uninstall the add-in</span></span>

1. <span data-ttu-id="772a2-130">[Schakel de scenario's uit](iot-scenario-setup.md#how-to-disable-a-scenario) in Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="772a2-130">In Supply Chain Management, [disable the scenarios](iot-scenario-setup.md#how-to-disable-a-scenario).</span></span>
2. <span data-ttu-id="772a2-131">Ga in LCS naar de details van uw Supply Chain Management-omgeving.</span><span class="sxs-lookup"><span data-stu-id="772a2-131">In LCS, go to your Supply Chain Management environment details.</span></span>
3. <span data-ttu-id="772a2-132">Schuif naar de sectie **Invoegtoepassingen voor omgeving**.</span><span class="sxs-lookup"><span data-stu-id="772a2-132">Scroll to the **Environment add-ins** section.</span></span>
4. <span data-ttu-id="772a2-133">Selecteer **Verwijderen** voor de invoegtoepassing IoT-intelligentie.</span><span class="sxs-lookup"><span data-stu-id="772a2-133">Select **Uninstall** for the IoT Intelligence add-in.</span></span>
