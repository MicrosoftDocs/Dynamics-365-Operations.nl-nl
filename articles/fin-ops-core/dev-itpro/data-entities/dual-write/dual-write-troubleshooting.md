---
title: Gids voor het oplossen van problemen met gegevensintegratie
description: Dit onderwerp bevat informatie voor het oplossen van problemen met gegevensintegratie tussen Finance and Operations-apps en Common Data Service.
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
ms.openlocfilehash: 87bdb72024c1c3844ff61e832a92f7edcc77c5d6
ms.sourcegitcommit: 54baab2a04e5c534fc2d1fd67b67e23a152d4e57
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/04/2020
ms.locfileid: "3019721"
---
# <a name="troubleshooting-guide-for-data-integration"></a><span data-ttu-id="4d165-103">Gids voor het oplossen van problemen met gegevensintegratie</span><span class="sxs-lookup"><span data-stu-id="4d165-103">Troubleshooting guide for data integration</span></span>

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]

## <a name="enable-plug-in-trace-logs-in-common-data-service-and-inspect-the-dual-write-plug-in-error-details"></a><span data-ttu-id="4d165-104">Schakel logboeken voor invoegtoepassing traceren in Common Data Service in en controleer de foutgegevens met betrekking tot de invoegtoepassing voor Twee keer wegschrijven</span><span class="sxs-lookup"><span data-stu-id="4d165-104">Enable plug-in trace logs in Common Data Service and inspect the dual-write plug-in error details</span></span>

<span data-ttu-id="4d165-105">Als er een probleem of fout optreedt tijdens de synchronisatie van twee keer wegschrijven, voert u de volgende stappen uit om de fouten in het traceerlogboek te controleren.</span><span class="sxs-lookup"><span data-stu-id="4d165-105">If you experience an issue or error during dual-write synchronization, follow these steps to inspect the errors in the trace log.</span></span>

1. <span data-ttu-id="4d165-106">Voordat u de fouten kunt inspecteren, moet u traceerlogboeken voor invoegtoepassingen inschakelen.</span><span class="sxs-lookup"><span data-stu-id="4d165-106">Before you can inspect the errors, you must enable plug-in trace logs.</span></span> <span data-ttu-id="4d165-107">Zie voor instructies de sectie "Traceerlogboek weergeven" in de [Zelfstudie: een invoegtoepassing schrijven en registreren](https://docs.microsoft.com/powerapps/developer/common-data-service/tutorial-write-plug-in#view-trace-logs).</span><span class="sxs-lookup"><span data-stu-id="4d165-107">For instructions, see the "View trace logs" section of [Tutorial: Write and register a plug-in](https://docs.microsoft.com/powerapps/developer/common-data-service/tutorial-write-plug-in#view-trace-logs).</span></span>

    <span data-ttu-id="4d165-108">Nu kunt u de fouten inspecteren.</span><span class="sxs-lookup"><span data-stu-id="4d165-108">You can now inspect the errors.</span></span>

2. <span data-ttu-id="4d165-109">Meld u aan bij Microsoft Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="4d165-109">Sign in to Microsoft Dynamics 365 Sales.</span></span>
3. <span data-ttu-id="4d165-110">Selecteer de knop **Instellingen** (het tandwielsymbool) en selecteer **Geavanceerde instellingen**.</span><span class="sxs-lookup"><span data-stu-id="4d165-110">Select the **Settings** button (the gear symbol), and then select **Advanced Settings**.</span></span>
4. <span data-ttu-id="4d165-111">Kies in het menu **Instellingen** de optie **Aanpassen \> Traceerlogboek invoegtoepassing**.</span><span class="sxs-lookup"><span data-stu-id="4d165-111">On the **Settings** menu, select **Customization \> Plug-In Trace Log**.</span></span>
5. <span data-ttu-id="4d165-112">Selecteer de typenaam **Microsoft.Dynamics.Integrator.CrmPlugins.Plugin** om de foutdetails weer te geven.</span><span class="sxs-lookup"><span data-stu-id="4d165-112">Select **Microsoft.Dynamics.Integrator.CrmPlugins.Plugin** as the type name to show the error details.</span></span>

## <a name="inspect-dual-write-synchronization-errors"></a><span data-ttu-id="4d165-113">Synchronisatiefouten met twee schrijfbewerkingen controleren</span><span class="sxs-lookup"><span data-stu-id="4d165-113">Inspect dual-write synchronization errors</span></span>

<span data-ttu-id="4d165-114">Volg deze stappen om fouten tijdens het testen te controleren.</span><span class="sxs-lookup"><span data-stu-id="4d165-114">Follow these steps to inspect errors during testing.</span></span>

1. <span data-ttu-id="4d165-115">Meld u aan bij Microsoft Dynamics LCS (LifeCycle Services).</span><span class="sxs-lookup"><span data-stu-id="4d165-115">Sign in to Microsoft Dynamics Lifecycle Services (LCS).</span></span>
2. <span data-ttu-id="4d165-116">Open het LCS-project waarvoor u tests met twee keer wegschrijven wilt uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="4d165-116">Open the LCS project to do dual-write testing for.</span></span>
3. <span data-ttu-id="4d165-117">Selecteer **Cloudomgevingen**.</span><span class="sxs-lookup"><span data-stu-id="4d165-117">Select **Cloud-hosted environments**.</span></span>
4. <span data-ttu-id="4d165-118">Maak een verbinding van een extern bureaublad met de virtuele machine (VM) van de toepassing door gebruik te maken van een lokaal account in LCS.</span><span class="sxs-lookup"><span data-stu-id="4d165-118">Make a Remote desktop connection to the application virtual machine (VM) by using local account that is shown in LCS.</span></span>
5. <span data-ttu-id="4d165-119">Open Logboeken.</span><span class="sxs-lookup"><span data-stu-id="4d165-119">Open Event Viewer.</span></span> 
6. <span data-ttu-id="4d165-120">Ga naar **Logboeken Toepassingen en Services \> Microsoft \> Dynamics \> AX-DualWriteSync \> Operationeel**.</span><span class="sxs-lookup"><span data-stu-id="4d165-120">Go to **Applications and Services Logs \> Microsoft \> Dynamics \> AX-DualWriteSync \> Operational**.</span></span> <span data-ttu-id="4d165-121">De fouten en details worden weergegeven.</span><span class="sxs-lookup"><span data-stu-id="4d165-121">The errors and details are shown.</span></span>

## <a name="unlink-one-common-data-service-environment-from-the-application-and-link-another-environment"></a><span data-ttu-id="4d165-122">Een Common Data Service-omgeving (los)koppelen van de toepassing en een andere omgeving koppelen</span><span class="sxs-lookup"><span data-stu-id="4d165-122">Unlink one Common Data Service environment from the application and link another environment</span></span>

<span data-ttu-id="4d165-123">Voer de volgende stappen uit om de koppelingen bij te werken.</span><span class="sxs-lookup"><span data-stu-id="4d165-123">Follow these steps to update links.</span></span>

1. <span data-ttu-id="4d165-124">Ga naar de toepassingsomgeving.</span><span class="sxs-lookup"><span data-stu-id="4d165-124">Go to the application environment.</span></span>
2. <span data-ttu-id="4d165-125">Open Gegevensbeheer.</span><span class="sxs-lookup"><span data-stu-id="4d165-125">Open Data Management.</span></span>
3. <span data-ttu-id="4d165-126">Selecteer **Koppeling naar CDS for Apps**.</span><span class="sxs-lookup"><span data-stu-id="4d165-126">Select **Link to CDS for apps**.</span></span>
4. <span data-ttu-id="4d165-127">Selecteer alle toewijzingen die worden uitgevoerd en selecteer **Stoppen**.</span><span class="sxs-lookup"><span data-stu-id="4d165-127">Select all the mappings that are running, and then select **Stop**.</span></span>
5. <span data-ttu-id="4d165-128">Selecteer alle toewijzingen en selecteer vervolgens **Verwijderen**.</span><span class="sxs-lookup"><span data-stu-id="4d165-128">Select all the mappings, and then select **Delete**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="4d165-129">De optie **Verwijderen** is niet beschikbaar als de sjabloon **CustomerV3-account** is geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="4d165-129">The **Delete** option isn't available if the **CustomerV3-Account** template is selected.</span></span> <span data-ttu-id="4d165-130">Maak de selectie van deze sjabloon waar nodig leeg.</span><span class="sxs-lookup"><span data-stu-id="4d165-130">Clear the selection of this template as required.</span></span> <span data-ttu-id="4d165-131">**CustomerV3-account** is een oudere ingerichte sjabloon en werkt met de oplossing Prospect naar contant geld.</span><span class="sxs-lookup"><span data-stu-id="4d165-131">**CustomerV3-Account** is an older provisioned template and works with the Prospect to Cash solution.</span></span> <span data-ttu-id="4d165-132">Omdat deze wereldwijd is vrijgegeven, wordt deze weergegeven onder alle sjablonen.</span><span class="sxs-lookup"><span data-stu-id="4d165-132">Because it's globally released, it appears under all templates.</span></span>

6. <span data-ttu-id="4d165-133">Selecteer **Koppeling met omgeving verbreken**.</span><span class="sxs-lookup"><span data-stu-id="4d165-133">Select **Unlink environment**.</span></span>
7. <span data-ttu-id="4d165-134">Selecteer **Ja** om de bewerking te bevestigen.</span><span class="sxs-lookup"><span data-stu-id="4d165-134">Select **Yes** to confirm the operation.</span></span>
8. <span data-ttu-id="4d165-135">Volg de stappen in de [installatiehandleiding](https://aka.ms/dualwrite-docs) om de nieuwe omgeving te koppelen.</span><span class="sxs-lookup"><span data-stu-id="4d165-135">To link the new environment, follow the steps in the [installation guide](https://aka.ms/dualwrite-docs).</span></span>
