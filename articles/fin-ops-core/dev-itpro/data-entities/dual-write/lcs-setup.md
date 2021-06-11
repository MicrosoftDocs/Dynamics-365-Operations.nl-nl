---
title: Instellingen voor twee keer wegschrijven van Lifecycle Services
description: In dit onderwerp wordt uitgelegd hoe u een verbinding voor twee keer wegschrijven kunt instellen vanuit Microsoft Dynamics Lifecycle Services (LCS).
author: RamaKrishnamoorthy
ms.date: 05/11/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.region: global
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: eb4170ef6cb09c862f6a4163670c519d5d8077fb
ms.sourcegitcommit: 365092f735310990e82516110141d42aaf04e654
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/27/2021
ms.locfileid: "6103564"
---
# <a name="dual-write-setup-from-lifecycle-services"></a><span data-ttu-id="e14d8-103">Instellingen voor twee keer wegschrijven van Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="e14d8-103">Dual-write setup from Lifecycle Services</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="e14d8-104">In dit onderwerp wordt uitgelegd hoe u twee keer wegschrijven kunt inschakelen vanuit Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="e14d8-104">This topic explains how to enable dual-write from Microsoft Dynamics Lifecycle Services (LCS).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="e14d8-105">Vereisten</span><span class="sxs-lookup"><span data-stu-id="e14d8-105">Prerequisites</span></span>

<span data-ttu-id="e14d8-106">U moet de integratie van Power Platform voltooien zoals beschreven in de volgende onderwerpen:</span><span class="sxs-lookup"><span data-stu-id="e14d8-106">You must complete the Power Platform integration as described in the following topics:</span></span>

+ [<span data-ttu-id="e14d8-107">Power Platform-integratie: inschakelen tijdens de implementatie van de omgeving</span><span class="sxs-lookup"><span data-stu-id="e14d8-107">Power Platform Integration - Enable during environment deployment</span></span>](../../power-platform/overview.md#enable-during-environment-deployment)
+ [<span data-ttu-id="e14d8-108">Power Platform-integratie: instellen na de implementatie van de omgeving</span><span class="sxs-lookup"><span data-stu-id="e14d8-108">Power Platform integration - Set up after environment deployment</span></span>](../../power-platform/overview.md#set-up-after-environment-deployment)

## <a name="set-up-dual-write-for-new-dataverse-environments"></a><span data-ttu-id="e14d8-109">Twee keer wegschrijven instellen voor nieuwe Dataverse-omgevingen</span><span class="sxs-lookup"><span data-stu-id="e14d8-109">Set up dual-write for new Dataverse environments</span></span>

<span data-ttu-id="e14d8-110">Voer de volgende stappen uit om twee keer wegschrijven via de pagina **Omgevingsdetails** in LCS in te stellen:</span><span class="sxs-lookup"><span data-stu-id="e14d8-110">Follow these steps to set up dual-write from LCS **Environment Details** page:</span></span>

1. <span data-ttu-id="e14d8-111">Vouw op de pagina **Omgevingsdetails** de sectie **Power Platform-integratie** uit.</span><span class="sxs-lookup"><span data-stu-id="e14d8-111">On the **Environment Details** page, expand the **Power Platform Integration** section.</span></span>

2. <span data-ttu-id="e14d8-112">Selecteer de knop **Toepassing twee keer wegschrijven**.</span><span class="sxs-lookup"><span data-stu-id="e14d8-112">Select the **Dual-write application** button.</span></span>

    ![Power Platform-integratie](media/powerplat_integration_step2.png)

3. <span data-ttu-id="e14d8-114">Neem de algemene voorwaarden door en selecteer vervolgens **Configureren**.</span><span class="sxs-lookup"><span data-stu-id="e14d8-114">Review the terms and conditions, and then select **Configure**.</span></span>

4. <span data-ttu-id="e14d8-115">Selecteer **OK** om door te gaan.</span><span class="sxs-lookup"><span data-stu-id="e14d8-115">Select **OK** to continue.</span></span>

5. <span data-ttu-id="e14d8-116">U kunt de voortgang controleren door de pagina met details van de omgeving periodiek te vernieuwen.</span><span class="sxs-lookup"><span data-stu-id="e14d8-116">You can monitor the progress by periodically refreshing the environment details page.</span></span> <span data-ttu-id="e14d8-117">De instelling duurt doorgaans 30 minuten of minder.</span><span class="sxs-lookup"><span data-stu-id="e14d8-117">Setup typically takes 30 minutes or less.</span></span>  

6. <span data-ttu-id="e14d8-118">Wanneer de instelling is voltooid, wordt u in een bericht geïnformeerd of het proces is geslaagd of dat er een fout is gevonden.</span><span class="sxs-lookup"><span data-stu-id="e14d8-118">When the setup is complete, a message will inform you if the process was successful or if there was a failure.</span></span> <span data-ttu-id="e14d8-119">Als de instelling is mislukt, wordt een bijbehorend foutbericht weergegeven.</span><span class="sxs-lookup"><span data-stu-id="e14d8-119">If the setup failed, then a related error message is displayed.</span></span> <span data-ttu-id="e14d8-120">U moet alle fouten oplossen voordat u naar de volgende stap gaat.</span><span class="sxs-lookup"><span data-stu-id="e14d8-120">You must fix any errors before moving to the next step.</span></span>

7. <span data-ttu-id="e14d8-121">Selecteer **Koppeling naar Power Platform-omgeving** om een koppeling te maken tussen Dataverse en de databases van de huidige omgeving.</span><span class="sxs-lookup"><span data-stu-id="e14d8-121">Select **Link to Power Platform environment** to create a link between Dataverse and the current environment's databases.</span></span> <span data-ttu-id="e14d8-122">Dit duurt doorgaans 5 minuten of minder.</span><span class="sxs-lookup"><span data-stu-id="e14d8-122">This typically takes less than 5 minutes.</span></span>

    :::image type="content" source="media/powerplat_integration_step3.png" alt-text="Koppeling naar Power Platform-omgeving":::

8. <span data-ttu-id="e14d8-124">Wanneer de koppeling is voltooid, wordt er een hyperlink weergegeven.</span><span class="sxs-lookup"><span data-stu-id="e14d8-124">When the linking is complete, a hyperlink is displayed.</span></span> <span data-ttu-id="e14d8-125">Gebruik de koppeling om u aan te melden bij het beheergebied voor twee keer wegschrijven in de Finance and Operations-omgeving.</span><span class="sxs-lookup"><span data-stu-id="e14d8-125">Use the link to sign in to the dual-write administration area in the Finance and Operations environment.</span></span> <span data-ttu-id="e14d8-126">Vanaf hier kunt u entiteitstoewijzingen instellen.</span><span class="sxs-lookup"><span data-stu-id="e14d8-126">From there, you can set up entity mappings.</span></span>

## <a name="set-up-dual-write-for-an-existing-dataverse-environment"></a><span data-ttu-id="e14d8-127">Twee keer wegschrijven instellen voor een bestaande Dataverse-omgeving</span><span class="sxs-lookup"><span data-stu-id="e14d8-127">Set up dual-write for an existing Dataverse environment</span></span>

<span data-ttu-id="e14d8-128">Als u twee keer wegschrijven wilt instellen voor een bestaande Dataverse-omgeving, moet u een Microsoft-[ondersteuningsticket](../../lifecycle-services/lcs-support.md) maken.</span><span class="sxs-lookup"><span data-stu-id="e14d8-128">To set up dual-write for an existing Dataverse environment, you must create a Microsoft [support ticket](../../lifecycle-services/lcs-support.md).</span></span> <span data-ttu-id="e14d8-129">Het ticket moet het volgende bevatten:</span><span class="sxs-lookup"><span data-stu-id="e14d8-129">The ticket must include:</span></span>

+ <span data-ttu-id="e14d8-130">Uw ID voor de Finance and Operations-omgeving.</span><span class="sxs-lookup"><span data-stu-id="e14d8-130">Your Finance and Operations environment ID.</span></span>
+ <span data-ttu-id="e14d8-131">Uw omgevingsnaam van Lifecycle Services.</span><span class="sxs-lookup"><span data-stu-id="e14d8-131">Your environment name from Lifecycle Services.</span></span>
+ <span data-ttu-id="e14d8-132">De Dataverse-organisatie-ID of Power Platform-omgevings-ID van Power Platform Beheercentrum.</span><span class="sxs-lookup"><span data-stu-id="e14d8-132">The Dataverse organization ID or Power Platform Environment ID from Power Platform Admin Center.</span></span> <span data-ttu-id="e14d8-133">Vraag in uw ticket om de ID te gebruiken voor Power Platform-integratie.</span><span class="sxs-lookup"><span data-stu-id="e14d8-133">In your ticket, request that the ID be the instance used for Power Platform integration.</span></span>

> [!NOTE]
> <span data-ttu-id="e14d8-134">U kunt omgevingen niet ontkoppelen met behulp van LCS.</span><span class="sxs-lookup"><span data-stu-id="e14d8-134">You can't unlink environments by using LCS.</span></span> <span data-ttu-id="e14d8-135">Als u een omgeving wilt ontkoppelen, opent u het werkgebied **Gegevensintegratie** in de Finance and Operations-omgeving en selecteert u **Koppeling verbreken**.</span><span class="sxs-lookup"><span data-stu-id="e14d8-135">To unlink an environment, open the **Data integration** workspace in the Finance and Operations environment, and then select **Unlink**.</span></span>

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
