---
title: Een gegevensintegratorproject maken (preview)
description: In dit onderwerp wordt uitgelegd hoe u een gegevensintegratorproject maakt.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 07/24/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-07-24
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: fb17d5e82709a34ff088774d9e9034adb714b58c
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/25/2020
ms.locfileid: "4646248"
---
# <a name="create-a-data-integrator-project-preview"></a><span data-ttu-id="82bc6-103">Een gegevensintegratorproject maken (preview)</span><span class="sxs-lookup"><span data-stu-id="82bc6-103">Create a data integrator project (preview)</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="82bc6-104">In dit onderwerp wordt uitgelegd hoe u een gegevensintegratorproject maakt.</span><span class="sxs-lookup"><span data-stu-id="82bc6-104">This topic explains how to create a data integrator project.</span></span>

1. <span data-ttu-id="82bc6-105">Meld u aan bij Microsoft Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="82bc6-105">Sign in to Microsoft Dynamics 365 Finance.</span></span>
2. <span data-ttu-id="82bc6-106">Ga naar **Werkgebieden \> Gegevensbeheer** en selecteer **Gegevensentiteiten**.</span><span class="sxs-lookup"><span data-stu-id="82bc6-106">Go to **Workspaces \> Data management**, and select **Data entities**.</span></span> <span data-ttu-id="82bc6-107">Wacht totdat alle gegevensentiteiten zijn vernieuwd voordat u naar de volgende stap gaat.</span><span class="sxs-lookup"><span data-stu-id="82bc6-107">Wait until all the data entities have been refreshed before you move on to the next step.</span></span>
3. <span data-ttu-id="82bc6-108">Open de [Power Apps portal](https://make.powerapps.com/) en voer de volgende stappen uit:</span><span class="sxs-lookup"><span data-stu-id="82bc6-108">Open the [Power Apps portal](https://make.powerapps.com/), and follow these steps:</span></span>

    1. <span data-ttu-id="82bc6-109">Selecteer de gewenste omgeving.</span><span class="sxs-lookup"><span data-stu-id="82bc6-109">Select the appropriate environment.</span></span>
    2. <span data-ttu-id="82bc6-110">Selecteer in het linkernavigatievenster **Gegevens \> Verbindingen**.</span><span class="sxs-lookup"><span data-stu-id="82bc6-110">In the left navigation pane, select **Data \> Connections**.</span></span>
    3. <span data-ttu-id="82bc6-111">Verbinding maken met de juiste instanties van de volgende items:</span><span class="sxs-lookup"><span data-stu-id="82bc6-111">Connect to appropriate instances of the following items:</span></span>

        - <span data-ttu-id="82bc6-112">Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="82bc6-112">Dynamics 365</span></span>
        - <span data-ttu-id="82bc6-113">Dynamics 365 voor Fin & Ops</span><span class="sxs-lookup"><span data-stu-id="82bc6-113">Dynamics 365 for Fin & Ops</span></span>

4. <span data-ttu-id="82bc6-114">Open de [Power Apps omgevingen](https://admin.powerapps.com/environments) en voer de volgende stappen uit:</span><span class="sxs-lookup"><span data-stu-id="82bc6-114">Open the [Power Apps environments](https://admin.powerapps.com/environments), and follow these steps:</span></span>

    1. <span data-ttu-id="82bc6-115">Selecteer **Gegevensintegrator**.</span><span class="sxs-lookup"><span data-stu-id="82bc6-115">Select **Data Integrator**.</span></span>
    2. <span data-ttu-id="82bc6-116">Selecteer **Verbindingssets**.</span><span class="sxs-lookup"><span data-stu-id="82bc6-116">Select **Connection sets**.</span></span>
    3. <span data-ttu-id="82bc6-117">Selecteer **Nieuwe verbindingsset**.</span><span class="sxs-lookup"><span data-stu-id="82bc6-117">Select **New connection set**.</span></span>
    4. <span data-ttu-id="82bc6-118">Geef een naam op voor de verbinding.</span><span class="sxs-lookup"><span data-stu-id="82bc6-118">Enter a name for the connection.</span></span>
    5. <span data-ttu-id="82bc6-119">Selecteer de juiste verbindingen voor de volgende items:</span><span class="sxs-lookup"><span data-stu-id="82bc6-119">Select the appropriate connections for the following items:</span></span>

        - <span data-ttu-id="82bc6-120">Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="82bc6-120">Dynamics 365</span></span>
        - <span data-ttu-id="82bc6-121">Dynamics 365 voor Fin & Ops</span><span class="sxs-lookup"><span data-stu-id="82bc6-121">Dynamics 365 for Fin & Ops</span></span>

    6. <span data-ttu-id="82bc6-122">Selecteer de juiste organisatietoewijzing.</span><span class="sxs-lookup"><span data-stu-id="82bc6-122">Select the appropriate organization mapping.</span></span>
    7. <span data-ttu-id="82bc6-123">Selecteer **Maken**.</span><span class="sxs-lookup"><span data-stu-id="82bc6-123">Select **Create**.</span></span>

5. <span data-ttu-id="82bc6-124">Open de [Power Apps omgevingen](https://admin.powerapps.com/environments) en voer de volgende stappen uit:</span><span class="sxs-lookup"><span data-stu-id="82bc6-124">Open the [Power Apps environments](https://admin.powerapps.com/environments), and follow these steps:</span></span>  

    1. <span data-ttu-id="82bc6-125">Maak gegevensintegratieprojecten voor de volgende sjablonen met de verbindingsset die u zojuist hebt gemaakt:</span><span class="sxs-lookup"><span data-stu-id="82bc6-125">Create data integration projects for the following templates by using the connection set that you just created:</span></span>

        - <span data-ttu-id="82bc6-126">Resultaten van inzichten voor klantbetalingen (CDS naar Fin and OPS)</span><span class="sxs-lookup"><span data-stu-id="82bc6-126">Customer payment insights results (CDS to Fin and Ops)</span></span>
        - <span data-ttu-id="82bc6-127">Resultaten van cashflowtijdreeksen (CDS naar Fin and Ops)</span><span class="sxs-lookup"><span data-stu-id="82bc6-127">Cash flow time series results (CDS to Fin and Ops)</span></span>
        - <span data-ttu-id="82bc6-128">Resultaten van budgettijdreeksen (CDS naar Fin and OPS)</span><span class="sxs-lookup"><span data-stu-id="82bc6-128">Budget time series results (CDS to Fin and Ops)</span></span>

    2. <span data-ttu-id="82bc6-129">Stel de juiste planning in voor elk project.</span><span class="sxs-lookup"><span data-stu-id="82bc6-129">Set the appropriate scheduling for each project.</span></span>

> [!NOTE]
> <span data-ttu-id="82bc6-130">Als de vereiste entiteiten niet in CDS worden weergeven, gaat u naar **Credit en aanmaningen > Instellen > Financiële inzichten > Parameters voor financiële inzichten**, schakelt u de functie Voorspellingen klantbetalingen in en klikt u op **Voorspellingsmodel maken**.</span><span class="sxs-lookup"><span data-stu-id="82bc6-130">If you do not see the required entities in CDS, please go to **Credit and collections > Setup > Finance Insights > Finance insights parameters**, enable Customer payment predictions feature and click on **Create prediction model** button.</span></span> <span data-ttu-id="82bc6-131">Wanneer de implementatie van het AI-model is voltooid (geslaagd of mislukt), worden de CDS-entiteiten die nodig zijn om integratie te maken, geïmplementeerd in CDS.</span><span class="sxs-lookup"><span data-stu-id="82bc6-131">When the deployment of AI model is completed (successful or failed), the CDS entities needed to create integration will be deployed in CDS.</span></span>

## <a name="privacy-notice"></a><span data-ttu-id="82bc6-132">Privacyverklaring</span><span class="sxs-lookup"><span data-stu-id="82bc6-132">Privacy notice</span></span>

<span data-ttu-id="82bc6-133">Previews (1) bieden mogelijk minder privacy- en beveiligingsmaatregelen dan de service Dynamics 365 Finance and Operations, (2) worden niet opgenomen in de serviceovereenkomst voor deze service, (3) mogen niet worden gebruikt voor de verwerking van persoonsgegevens of andere gegevens die aan juridische of wettelijke nalevingvereisten zijn onderworpen en (4) worden slechts beperkt ondersteund.</span><span class="sxs-lookup"><span data-stu-id="82bc6-133">Previews (1) might use less privacy and fewer security measures than the Dynamics 365 Finance and Operations service, (2) aren't included in the service level agreement (SLA) for this service, (3) should not be used to process personal data or other data that is subject to legal or regulatory compliance requirements, and (4) have limited support.</span></span>
