---
title: Gids voor het oplossen van problemen met gegevensintegratie
description: Dit onderwerp bevat informatie over het oplossen van problemen met gegevensintegratie tussen Microsoft Dynamics 365 for Finance and Operations en Common Data Service.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: ca62a6b3aa64ec2383ee3ded3b7bbf4650a41166
ms.sourcegitcommit: efcc0dee8bde5f8f93f6291e7f059ad426843e57
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 07/31/2019
ms.locfileid: "1797270"
---
# <a name="troubleshooting-guide-for-data-integration"></a><span data-ttu-id="1ed09-103">Gids voor het oplossen van problemen met gegevensintegratie</span><span class="sxs-lookup"><span data-stu-id="1ed09-103">Troubleshooting guide for data integration</span></span>

## <a name="enable-plugin-trace-in-common-data-service-and-check-the-dual-write-plugin-error-details"></a><span data-ttu-id="1ed09-104">Schakel Plug-in traceren in Common Data Service in en controleer de foutgegevens met betrekking tot de invoegtoepassing voor Twee keer wegschrijven</span><span class="sxs-lookup"><span data-stu-id="1ed09-104">Enable Plugin Trace in Common Data Service and check the dual-write Plugin error details</span></span>

<span data-ttu-id="1ed09-105">Als er zich een probleem of fout voordoet met de synchronisatie van Twee keer wegschrijven, kunt u de fouten in het traceerlogboek controleren:</span><span class="sxs-lookup"><span data-stu-id="1ed09-105">If you are facing an issue or error with dual-write synchronization, you can inspect the errors in the trace log:</span></span>

1. <span data-ttu-id="1ed09-106">Voordat u de fouten kunt inspecteren, moet u Plug-in traceren inschakelen met behulp van de instructies in [Plug-in registreren](https://docs.microsoft.com/en-us/powerapps/developer/common-data-service/tutorial-write-plug-in#view-trace-logs).</span><span class="sxs-lookup"><span data-stu-id="1ed09-106">Before you can inspect the errors, you must enable Plugin trace using the instructions in [Register plug-in](https://docs.microsoft.com/en-us/powerapps/developer/common-data-service/tutorial-write-plug-in#view-trace-logs) to enable Plugin trace.</span></span> <span data-ttu-id="1ed09-107">Nu kunt u de fouten inspecteren.</span><span class="sxs-lookup"><span data-stu-id="1ed09-107">Now you can inspect the errors.</span></span>
2. <span data-ttu-id="1ed09-108">Meld u aan bij Dynamics 365 for Sales.</span><span class="sxs-lookup"><span data-stu-id="1ed09-108">Login to Dynamics 365 for Sales.</span></span>
3. <span data-ttu-id="1ed09-109">Klik op het pictogram Instellingen (een tandwiel) en selecteer **Geavanceerde instellingen**.</span><span class="sxs-lookup"><span data-stu-id="1ed09-109">Click on the Settings icon (a gear), and select **Advanced Settings**.</span></span>
4. <span data-ttu-id="1ed09-110">Kies in het menu **Instellingen** de optie **Aanpassen > Traceerlogboek plug-in**.</span><span class="sxs-lookup"><span data-stu-id="1ed09-110">In the **Settings** menu, choose **Customization > Plug-In Trace Log**.</span></span>
5. <span data-ttu-id="1ed09-111">Klik op de typenaam **Microsoft.Dynamics.Integrator.CrmPlugins.Plugin** om de foutdetails weer te geven.</span><span class="sxs-lookup"><span data-stu-id="1ed09-111">Click the type name **Microsoft.Dynamics.Integrator.CrmPlugins.Plugin** to display the error details.</span></span>

## <a name="check-dual-write-synchronization-errors-in-finance-and-operations"></a><span data-ttu-id="1ed09-112">De synchronisatiefouten voor Twee keer wegschrijven controleren in Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="1ed09-112">Check dual-write synchronization errors in Finance and Operations</span></span>

<span data-ttu-id="1ed09-113">U kunt de fouten tijdens het testen controleren met behulp van de volgende stappen:</span><span class="sxs-lookup"><span data-stu-id="1ed09-113">You can check the errors during testing by following these steps:</span></span>

+ <span data-ttu-id="1ed09-114">Meld u aan bij LCS (LifeCycle Services).</span><span class="sxs-lookup"><span data-stu-id="1ed09-114">Login to LifeCycle Services (LCS).</span></span>
+ <span data-ttu-id="1ed09-115">Open het LCS-project dat u hebt gekozen om tests met twee keer wegschrijven uit te voeren.</span><span class="sxs-lookup"><span data-stu-id="1ed09-115">Open the LCS project that you chose to perform dual-write testing.</span></span>
+ <span data-ttu-id="1ed09-116">Ga naar Cloudomgevingen.</span><span class="sxs-lookup"><span data-stu-id="1ed09-116">Go to Cloud Hosted Environments.</span></span>
+ <span data-ttu-id="1ed09-117">VM voor extern bureaublad naar Finance and Operations met lokaal account dat wordt weergegeven in LCS.</span><span class="sxs-lookup"><span data-stu-id="1ed09-117">Remote desktop to Finance and Operations VM using local account that is displayed in LCS.</span></span>
+ <span data-ttu-id="1ed09-118">Open Logboeken.</span><span class="sxs-lookup"><span data-stu-id="1ed09-118">Open the event viewer.</span></span> 
+ <span data-ttu-id="1ed09-119">Navigeer naar **Logboeken Toepassingen en Services > Microsoft > Dynamics > AX-DualWriteSync > Operationeel**.</span><span class="sxs-lookup"><span data-stu-id="1ed09-119">Navigate to **Applications and Services logs > Microsoft > Dynamics > AX-DualWriteSync > Operational**.</span></span> <span data-ttu-id="1ed09-120">De fouten en details worden weergegeven.</span><span class="sxs-lookup"><span data-stu-id="1ed09-120">The errors and details are displayed.</span></span>

## <a name="how-to-unlink-and-link-another-common-data-service-environment-from-finance-and-operations"></a><span data-ttu-id="1ed09-121">Een andere Common Data Service-omgeving (los)koppelen vanuit Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="1ed09-121">How to unlink and link another Common Data Service environment from Finance and Operations</span></span>

<span data-ttu-id="1ed09-122">U kunt koppelingen bijwerken door de volgende stappen uit te voeren:</span><span class="sxs-lookup"><span data-stu-id="1ed09-122">You can update links by following these steps:</span></span>

+ <span data-ttu-id="1ed09-123">Navigeer naar de Finance and Operations-omgeving.</span><span class="sxs-lookup"><span data-stu-id="1ed09-123">Navigate to the Finance and Operations environment.</span></span>
+ <span data-ttu-id="1ed09-124">Open Gegevensbeheer.</span><span class="sxs-lookup"><span data-stu-id="1ed09-124">Open Data Management.</span></span>
+ <span data-ttu-id="1ed09-125">Klik op **Koppeling naar CDS for Apps**.</span><span class="sxs-lookup"><span data-stu-id="1ed09-125">Click on **Link to CDS for apps**.</span></span>
+ <span data-ttu-id="1ed09-126">Selecteer alle actieve toewijzingen en klik op **Stoppen**.</span><span class="sxs-lookup"><span data-stu-id="1ed09-126">Select all the running mappings and click **Stop**.</span></span> 
+ <span data-ttu-id="1ed09-127">Selecteer alle toewijzingen en klik op **Verwijderen**.</span><span class="sxs-lookup"><span data-stu-id="1ed09-127">Select all the mappings and click **Delete**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="1ed09-128">De optie **Verwijderen** wordt niet weergegeven als de sjabloon **CustomerV3-account** is geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="1ed09-128">The **Delete** option will not appear if **CustomerV3-Account** template is selected.</span></span> <span data-ttu-id="1ed09-129">Hef de selectie zo nodig op.</span><span class="sxs-lookup"><span data-stu-id="1ed09-129">Unselect it if needed.</span></span> <span data-ttu-id="1ed09-130">**CustomerV3-account** is een oudere ingerichte sjabloon en werkt met de oplossing Prospect naar contant geld.</span><span class="sxs-lookup"><span data-stu-id="1ed09-130">**CustomerV3-Account** is an older provisioned template and works with the Prospect to Cash solution.</span></span> <span data-ttu-id="1ed09-131">Omdat deze wereldwijd is vrijgegeven, wordt deze weergegeven onder alle sjablonen.</span><span class="sxs-lookup"><span data-stu-id="1ed09-131">Because it is globally released, it shows up under all templates.</span></span>

+ <span data-ttu-id="1ed09-132">Klik op **Koppeling met omgeving verbreken**.</span><span class="sxs-lookup"><span data-stu-id="1ed09-132">Click **Unlink environment**.</span></span>
+ <span data-ttu-id="1ed09-133">Klik ter bevestiging op **Ja**.</span><span class="sxs-lookup"><span data-stu-id="1ed09-133">Click **Yes** for confirmation.</span></span>
+ <span data-ttu-id="1ed09-134">Volg de stappen in de [installatiehandleiding](https://aka.ms/dualwrite-docs) om de nieuwe omgeving te koppelen.</span><span class="sxs-lookup"><span data-stu-id="1ed09-134">To link the new environment, follow the steps in the [installation guide](https://aka.ms/dualwrite-docs).</span></span>

