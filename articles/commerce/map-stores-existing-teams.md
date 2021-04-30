---
title: Winkels en teams toewijzen als er reeds bestaande teams in Microsoft Teams zijn
description: In dit onderwerp wordt beschreven hoe u winkels en bijbehorende teams in Dynamics 365 Commerce Headquarters toewijst als uw organisatie al teams heeft gemaakt in Microsoft Teams vóór de Commerce-integratie.
author: gvrmohanreddy
manager: annbe
ms.date: 03/31/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-01-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 5a711c1057b87bd792755ef91a84d1c28879c590
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/16/2021
ms.locfileid: "5908490"
---
# <a name="map-stores-and-teams-if-there-are-pre-existing-teams-in-microsoft-teams"></a><span data-ttu-id="b0c53-103">Winkels en teams toewijzen als er reeds bestaande teams in Microsoft Teams zijn</span><span class="sxs-lookup"><span data-stu-id="b0c53-103">Map stores and teams if there are pre-existing teams in Microsoft Teams</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="b0c53-104">In dit onderwerp wordt beschreven hoe u winkels en bijbehorende teams in Dynamics 365 Commerce Headquarters toewijst als uw organisatie al teams heeft gemaakt in Microsoft Teams vóór de Commerce-integratie.</span><span class="sxs-lookup"><span data-stu-id="b0c53-104">This topic covers how to map stores and corresponding teams in Dynamics 365 Commerce headquarters if your organization has already created teams in Microsoft Teams before Commerce integration.</span></span>

<span data-ttu-id="b0c53-105">Uw organisatie heeft mogelijk teams gemaakt voor sommige of al uw winkels voordat de integratie van Dynamics 365 Commerce en Microsoft Teams plaatsvindt.</span><span class="sxs-lookup"><span data-stu-id="b0c53-105">Your organization may have teams created for some or all of your stores before integrating Dynamics 365 Commerce and Microsoft Teams.</span></span> <span data-ttu-id="b0c53-106">Als dit het geval is, moet u de toewijzing van winkels en het bijbehorende team in Commerce Headquarters opgeven om taaksynchronisatie tot stand te brengen tussen Commerce POS en Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="b0c53-106">If this is the case, to establish task synchronization between Commerce POS and Microsoft Teams you must provide the mapping of stores and corresponding team in Commerce headquarters.</span></span>

## <a name="map-stores-and-corresponding-teams-in-commerce-headquarters"></a><span data-ttu-id="b0c53-107">Winkels en bijbehorende teams toewijzen in Commerce Headquarters</span><span class="sxs-lookup"><span data-stu-id="b0c53-107">Map stores and corresponding teams in Commerce headquarters</span></span> 

<span data-ttu-id="b0c53-108">Voer de volgende stappen uit om winkels en bijbehorende teams toe te wijzen in Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="b0c53-108">To map stores and corresponding teams in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="b0c53-109">Ga naar **Systeembeheer \> Werkruimte \> Gegevensbeheer**.</span><span class="sxs-lookup"><span data-stu-id="b0c53-109">Go to **System Administration \> Workspace \> Data management**.</span></span>
1. <span data-ttu-id="b0c53-110">Selecteer **Exporteren**.</span><span class="sxs-lookup"><span data-stu-id="b0c53-110">Select **Export**.</span></span> 
1. <span data-ttu-id="b0c53-111">Selecteer **Nieuw** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="b0c53-111">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="b0c53-112">Voer onder **Groepsnaam** 'Teams-toewijzing exporteren' in.</span><span class="sxs-lookup"><span data-stu-id="b0c53-112">Under **Group name**, enter "Export Teams mapping".</span></span>
1. <span data-ttu-id="b0c53-113">Selecteer op het sneltabblad **Geselecteerde entiteiten** de optie **Entiteit toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="b0c53-113">On the **Selected entities** FastTab, select **Add entity**.</span></span> <span data-ttu-id="b0c53-114">Het dialoogvenster **Entiteit toevoegen** wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="b0c53-114">The **Add entity** dialog box appears.</span></span>  
1. <span data-ttu-id="b0c53-115">Selecteer **Teams-toewijzing tussen bron en team** in de vervolgkeuzelijst **Entiteitsnaam**.</span><span class="sxs-lookup"><span data-stu-id="b0c53-115">In the **Entity name** drop-down list, select **Teams mapping between source and team**.</span></span>
1. <span data-ttu-id="b0c53-116">Selecteer **CSV** in de vervolgkeuzelijst **Indeling doelgegevens**.</span><span class="sxs-lookup"><span data-stu-id="b0c53-116">In the **Target data format** drop-down list, select **CSV**.</span></span>
1. <span data-ttu-id="b0c53-117">Selecteer **Toevoegen** en vervolgens **Sluiten**.</span><span class="sxs-lookup"><span data-stu-id="b0c53-117">Select **Add**, and then select **Close**.</span></span>
1. <span data-ttu-id="b0c53-118">Selecteer de optie **Nu exporteren** linksboven onder het actievenster.</span><span class="sxs-lookup"><span data-stu-id="b0c53-118">On the top left under the Action Pane, select **Export now**.</span></span>
1. <span data-ttu-id="b0c53-119">Selecteer **Bestand downloaden** onder **Verwerkingsstatus entiteit**.</span><span class="sxs-lookup"><span data-stu-id="b0c53-119">Under **Entity processing status**, select **Download file**.</span></span>
1. <span data-ttu-id="b0c53-120">Voer in het geëxporteerde CSV-bestand als volgt de waarden voor **SOURCETYPE**, **SOURCEID** en **TEAMID** in:</span><span class="sxs-lookup"><span data-stu-id="b0c53-120">In the exported CSV file, enter values for **SOURCETYPE**, **SOURCEID**, and **TEAMID** as follows:</span></span>
    - <span data-ttu-id="b0c53-121">Voer voor **SOURCETYPE** de waarde 'RetailStore' in.</span><span class="sxs-lookup"><span data-stu-id="b0c53-121">For **SOURCETYPE**, enter "RetailStore".</span></span> 
    - <span data-ttu-id="b0c53-122">Voer voor **SOURCEID** het winkelnummer in (bijvoorbeeld '000135' voor de winkel in San Francisco).</span><span class="sxs-lookup"><span data-stu-id="b0c53-122">For **SOURCEID**, enter the store number (for example, "000135" for the San Francisco store).</span></span> <span data-ttu-id="b0c53-123">U kunt winkelnummers vinden bij **Retail en commerce \> Afzetkanalen \> Winkels**.</span><span class="sxs-lookup"><span data-stu-id="b0c53-123">You can find store numbers at **Retail and Commerce \> Channels \> Stores**.</span></span>
    - <span data-ttu-id="b0c53-124">Voer voor **TEAMID** de bijbehorende team-id in vanuit Microsoft Teams (bijvoorbeeld '5f8bc92b-6aa8-451e-85d1-3949c01ddc6c').</span><span class="sxs-lookup"><span data-stu-id="b0c53-124">For **TEAMID**, enter the corresponding team ID from Microsoft Teams (for example, "5f8bc92b-6aa8-451e-85d1-3949c01ddc6c").</span></span> <span data-ttu-id="b0c53-125">U kunt informatie over de team-id vinden op [admin.teams.microsoft.com](https://admin.teams.microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="b0c53-125">You can find team ID information at [admin.teams.microsoft.com](https://admin.teams.microsoft.com).</span></span>
1. <span data-ttu-id="b0c53-126">Sla het CSV-bestand op uw lokale computer op.</span><span class="sxs-lookup"><span data-stu-id="b0c53-126">Save the CSV file to your local machine.</span></span>
1. <span data-ttu-id="b0c53-127">Ga naar **Systeembeheern \> Werkruimte \> Gegevensbeheer** en selecteer vervolgens **Importeren**.</span><span class="sxs-lookup"><span data-stu-id="b0c53-127">Go to **System Administration \> Workspace \> Data management**, and then select **Import**.</span></span>
1. <span data-ttu-id="b0c53-128">Selecteer op het sneltabblad **Geselecteerde entiteiten** de optie **Bestand toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="b0c53-128">On the **Selected entities** FastTab, select **Add file**.</span></span> <span data-ttu-id="b0c53-129">Het dialoogvenster **Bestand toevoegen** wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="b0c53-129">The **Add file** dialog box appears.</span></span>
1. <span data-ttu-id="b0c53-130">Selecteer **Teams-toewijzing tussen bron en team** in de vervolgkeuzelijst **Entiteitsnaam**.</span><span class="sxs-lookup"><span data-stu-id="b0c53-130">In the **Entity name** drop-down list, select **Teams mapping between source and team**.</span></span>
1. <span data-ttu-id="b0c53-131">Selecteer **CSV** in de vervolgkeuzelijst **Indeling brongegevens**.</span><span class="sxs-lookup"><span data-stu-id="b0c53-131">In the **Source data format** drop-down list, select **CSV**.</span></span>
1. <span data-ttu-id="b0c53-132">Selecteer **Uploaden en toevoegen**, selecteer het CSV-bestand dat u eerder hebt opgeslagen en selecteer vervolgens **Openen**.</span><span class="sxs-lookup"><span data-stu-id="b0c53-132">Select **Upload and add**, select the CSV file that you saved previously, and then select **Open**.</span></span>
1. <span data-ttu-id="b0c53-133">Selecteer in het dialoogvenster **Bestand toevoegen** de optie **Sluiten**.</span><span class="sxs-lookup"><span data-stu-id="b0c53-133">In the **Add file** dialog box, select **Close**.</span></span>
1. <span data-ttu-id="b0c53-134">Selecteer in het actievenster **Opslaan** en vervolgens **Importeren**.</span><span class="sxs-lookup"><span data-stu-id="b0c53-134">On the Action Pane, select **Save** , and then select **Import**.</span></span>

<span data-ttu-id="b0c53-135">In de volgende voorbeeldafbeelding ziet u de groep **Teams-toewijzing exporteren** in Commerce met de elementen **Entiteit toevoegen** en de geëxporteerde CSV-bestandskoppen gemarkeerd.</span><span class="sxs-lookup"><span data-stu-id="b0c53-135">The following example image shows the **Export teams mapping** group in Commerce with **Add entity** elements and the exported CSV file headers highlighted.</span></span>

![Groep Teams-toewijzing exporteren in Commerce met de elementen Entiteit toevoegen en de geëxporteerde CSV-bestandskoppen gemarkeerd](media/d365-commerce-data-mgmt-export-entity.png)

> [!NOTE]
> <span data-ttu-id="b0c53-137">Nadat u de voorafgaande stappen hebt voltooid, volgt u de stappen in [Taakbeheer synchroniseren tussen Microsoft Teams en POS](synchronize-tasks-teams-pos.md) om taakbeheer te synchroniseren.</span><span class="sxs-lookup"><span data-stu-id="b0c53-137">After you complete the preceeding steps, follow the steps in [Synchronize task management between Microsoft Teams and POS](synchronize-tasks-teams-pos.md) to synchronize task management.</span></span> 

## <a name="additional-resources"></a><span data-ttu-id="b0c53-138">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="b0c53-138">Additional resources</span></span>

[<span data-ttu-id="b0c53-139">Overzicht van integratie van Dynamics 365 Commerce en Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="b0c53-139">Dynamics 365 Commerce and Microsoft Teams integration overview</span></span>](commerce-teams-integration.md)

[<span data-ttu-id="b0c53-140">Integratie van Dynamics 365 Commerce en Microsoft Teams inschakelen</span><span class="sxs-lookup"><span data-stu-id="b0c53-140">Enable Dynamics 365 Commerce and Microsoft Teams integration</span></span>](enable-teams-integration.md)

[<span data-ttu-id="b0c53-141">Microsoft Teams inrichten vanuit Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="b0c53-141">Provision Microsoft Teams from Dynamics 365 Commerce</span></span>](provision-teams-from-commerce.md)

[<span data-ttu-id="b0c53-142">Taakbeheer synchroniseren tussen Microsoft Teams en Dynamics 365 Commerce POS</span><span class="sxs-lookup"><span data-stu-id="b0c53-142">Synchronize task management between Microsoft Teams and Dynamics 365 Commerce POS</span></span>](synchronize-tasks-teams-pos.md)

[<span data-ttu-id="b0c53-143">Gebruikersrollen beheren in Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="b0c53-143">Manage user roles in Microsoft Teams</span></span>](manage-user-roles-teams.md)

[<span data-ttu-id="b0c53-144">Veelgestelde vragen over integratie van Dynamics 365 Commerce en Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="b0c53-144">Dynamics 365 Commerce and Microsoft Teams integration FAQ</span></span>](teams-integration-faq.md)
