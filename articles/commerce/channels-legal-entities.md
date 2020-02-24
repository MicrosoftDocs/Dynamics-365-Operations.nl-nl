---
title: Rechtspersonen maken
description: In dit onderwerp wordt beschreven hoe u rechtspersonen kunt maken in Microsoft Dynamics 365 Commerce. Deze moeten worden gemaakt en geconfigureerd voordat u afzetkanalen gaat maken.
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 28cbcc42505f1dc90c420adc812735841541c8e0
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/01/2020
ms.locfileid: "3002399"
---
# <a name="create-legal-entities"></a><span data-ttu-id="47971-103">Rechtspersonen maken</span><span class="sxs-lookup"><span data-stu-id="47971-103">Create legal entities</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="47971-104">In dit onderwerp wordt beschreven hoe u rechtspersonen kunt maken in Microsoft Dynamics 365 Commerce. Deze moeten worden gemaakt en geconfigureerd voordat u afzetkanalen gaat maken.</span><span class="sxs-lookup"><span data-stu-id="47971-104">This topic describes how to create legal entities in Microsoft Dynamics 365 Commerce, which must be created and configured before creating channels.</span></span>

## <a name="overview"></a><span data-ttu-id="47971-105">Overzicht</span><span class="sxs-lookup"><span data-stu-id="47971-105">Overview</span></span>

<span data-ttu-id="47971-106">Een rechtspersoon is een organisatie met een geregistreerde of wettelijke juridische structuur.</span><span class="sxs-lookup"><span data-stu-id="47971-106">A legal entity is an organization that has a registered or legislated legal structure.</span></span> <span data-ttu-id="47971-107">Rechtspersonen kunnen wettelijk bindende overeenkomsten aangaan en zijn verplicht prestatieoverzichten te overleggen.</span><span class="sxs-lookup"><span data-stu-id="47971-107">Legal entities can enter into legal contracts and are required to prepare statements that report on their performance.</span></span>

<span data-ttu-id="47971-108">Een bedrijf is een type rechtspersoon.</span><span class="sxs-lookup"><span data-stu-id="47971-108">A company is a type of legal entity.</span></span> <span data-ttu-id="47971-109">Momenteel zijn bedrijven het enige type rechtspersoon dat u kunt maken. Aan elke rechtspersoon is een bedrijfs-id gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="47971-109">Currently, companies are the only kind of legal entity that you can create, and every legal entity is associated with a company ID.</span></span> <span data-ttu-id="47971-110">Deze koppeling bestaat omdat een aantal functionele gebieden in het programma een bedrijfs-id of *DataAreaId* in hun gegevensmodellen gebruiken.</span><span class="sxs-lookup"><span data-stu-id="47971-110">This association exists because some functional areas in the program use a company ID, or *DataAreaId*, in their data models.</span></span> <span data-ttu-id="47971-111">In deze functionele gebieden worden bedrijven gebruikt als begrenzing voor gegevensbeveiliging.</span><span class="sxs-lookup"><span data-stu-id="47971-111">In these functional areas, companies are used as a boundary for data security.</span></span> <span data-ttu-id="47971-112">Gebruikers hebben alleen toegang tot gegevens voor het bedrijf waarbij ze momenteel zijn aangemeld.</span><span class="sxs-lookup"><span data-stu-id="47971-112">Users can access data only for the company that they are currently logged on to.</span></span> 

<span data-ttu-id="47971-113">Wanneer u een kanaal maakt, moet u opgeven tot welke rechtspersoon het afzetkanaal behoort.</span><span class="sxs-lookup"><span data-stu-id="47971-113">When creating a channel, you must specify which legal entity that channel belongs to.</span></span>

## <a name="create-a-new-legal-entity"></a><span data-ttu-id="47971-114">Een nieuwe rechtspersoon maken</span><span class="sxs-lookup"><span data-stu-id="47971-114">Create a new legal entity</span></span>

<span data-ttu-id="47971-115">Ga als volgt te werk om een nieuwe rechtspersoon te maken in Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="47971-115">To create a new legal entity in Dynamics 365 Commerce, follow these steps.</span></span>

1. <span data-ttu-id="47971-116">Ga in het navigatiedeelvenster naar **Modules \> Headquarters instellen \> Rechtspersonen**.</span><span class="sxs-lookup"><span data-stu-id="47971-116">In the navigation pane, go to  **Modules \> Headquarters setup \> Legal entities**.</span></span>
1. <span data-ttu-id="47971-117">Selecteer **Nieuw** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="47971-117">On the action pane, select **New**.</span></span> <span data-ttu-id="47971-118">Het deelvenster **Nieuwe rechtspersoon** verschijnt aan de rechterkant.</span><span class="sxs-lookup"><span data-stu-id="47971-118">The **New legal entity** pane appears on the right.</span></span>
1. <span data-ttu-id="47971-119">Voer een waarde in het veld **Naam** in.</span><span class="sxs-lookup"><span data-stu-id="47971-119">In the **Name** field, enter a value.</span></span>
1. <span data-ttu-id="47971-120">Voer een waarde in het veld **Bedrijf** in.</span><span class="sxs-lookup"><span data-stu-id="47971-120">In the **Company** field, enter a value.</span></span>
1. <span data-ttu-id="47971-121">Typ of selecteer een waarde in het **veld Land/regio**.</span><span class="sxs-lookup"><span data-stu-id="47971-121">In the **Country/region** field, enter or select a value.</span></span>
1. <span data-ttu-id="47971-122">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="47971-122">Select **OK**.</span></span> 

   ![Het maken van een rechtspersoon](media/legal-entities.png)

1. <span data-ttu-id="47971-124">Geef in de sectie **Algemeen** de volgende algemene informatie op over de rechtspersoon:</span><span class="sxs-lookup"><span data-stu-id="47971-124">In the **General** section, provide the following general information about the legal entity:</span></span> 
   1. <span data-ttu-id="47971-125">Voer een zoeknaam in als een zoeknaam is vereist.</span><span class="sxs-lookup"><span data-stu-id="47971-125">Enter a search name, if a search name is required.</span></span> <span data-ttu-id="47971-126">Een zoeknaam is een alternatieve naam waarmee u naar deze rechtspersoon kunt zoeken.</span><span class="sxs-lookup"><span data-stu-id="47971-126">A search name is an alternate name that can be used to search for this legal entity.</span></span> 
   1. <span data-ttu-id="47971-127">Selecteer of deze rechtspersoon wordt gebruikt als consolidatiebedrijf.</span><span class="sxs-lookup"><span data-stu-id="47971-127">Select whether this legal entity is being used as a consolidation company.</span></span>
   1. <span data-ttu-id="47971-128">Selecteer of deze rechtspersoon wordt gebruikt als eliminatiebedrijf.</span><span class="sxs-lookup"><span data-stu-id="47971-128">Select whether this legal entity is being used as an elimination company.</span></span> 
   1. <span data-ttu-id="47971-129">Selecteer de **standaardtaal** voor de rechtspersoon.</span><span class="sxs-lookup"><span data-stu-id="47971-129">Select the **default language** for the entity.</span></span> 
   1. <span data-ttu-id="47971-130">Selecteer de **tijdzone** voor de rechtspersoon.</span><span class="sxs-lookup"><span data-stu-id="47971-130">Select the **time zone** for the entity.</span></span>
1. <span data-ttu-id="47971-131">Selecteer in de sectie **Adressen** de optie **Bewerken** om adresgegevens in te vullen, zoals straatnaam en -nummer, postcode en plaats.</span><span class="sxs-lookup"><span data-stu-id="47971-131">In the **Addresses** section, select **Edit** to enter address information, such as the street name and number, postal code, and city.</span></span>
1. <span data-ttu-id="47971-132">Voer in de sectie **Contactgegevens** informatie in over communicatiemethoden, zoals e-mailadressen, URL's en telefoonnummers.</span><span class="sxs-lookup"><span data-stu-id="47971-132">In the **Contact information** section, enter information about methods of communication, such as email addresses, URLs, and telephone numbers.</span></span>
1. <span data-ttu-id="47971-133">Voer in de sectie **Wettelijke rapportage** de registratienummers in die worden gebruikt voor wettelijke aangiften.</span><span class="sxs-lookup"><span data-stu-id="47971-133">In the **Statutory reporting** section, enter the registration numbers that are used for statutory reporting.</span></span>
1. <span data-ttu-id="47971-134">Voer in de sectie **Registratienummers** informatie in die door de rechtspersoon wordt vereist.</span><span class="sxs-lookup"><span data-stu-id="47971-134">In the **Registration numbers** section, enter any information required by the legal entity.</span></span>
1. <span data-ttu-id="47971-135">Voer in de sectie **Bankrekeninggegevens** bankrekeningen en routenummers in voor de rechtspersoon.</span><span class="sxs-lookup"><span data-stu-id="47971-135">In the **Bank account information** section, enter bank accounts and routing numbers for the legal entity.</span></span>
1. <span data-ttu-id="47971-136">Voer in de sectie **Buitenlandse handel en logistiek** verzendingsgegevens voor de rechtspersoon in.</span><span class="sxs-lookup"><span data-stu-id="47971-136">In the **Foreign trade and logistics** section, enter shipping information for the legal entity.</span></span>
1. <span data-ttu-id="47971-137">In de sectie **Nummerreeksen** kunt u de nummerreeksen weergeven die aan de rechtspersoon zijn gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="47971-137">In the **Number sequences** section, you can view the number sequences that are associated with the legal entity.</span></span> <span data-ttu-id="47971-138">Deze is in eerste instantie leeg.</span><span class="sxs-lookup"><span data-stu-id="47971-138">This will be empty to start with.</span></span>
1. <span data-ttu-id="47971-139">In de sectie **Dashboardafbeelding** kunt u het logo en/of de dashboardafbeelding bekijken of wijzigen die aan de rechtspersoon zijn gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="47971-139">In the **Dashboard image** section, view or change the logo and dashboard image associated with the legal entity.</span></span>
1. <span data-ttu-id="47971-140">Voer in de sectie **Belastingregistratie** de registratienummers in die worden gebruikt om te rapporteren aan de belastingdienst.</span><span class="sxs-lookup"><span data-stu-id="47971-140">In the **Tax registration** section, enter the registration numbers that are used to report to tax authorities.</span></span>
1. <span data-ttu-id="47971-141">Voer in de **1099-belasting** 1099-gegevens voor de rechtspersoon in.</span><span class="sxs-lookup"><span data-stu-id="47971-141">In the **Tax 1099** section, enter 1099 information for the legal entity.</span></span>
1. <span data-ttu-id="47971-142">In de sectie **Belastinginformatie** voert u de belastinginformatie voor de rechtspersoon in.</span><span class="sxs-lookup"><span data-stu-id="47971-142">In the **Tax invormation** section, enter tax information for the legal entity.</span></span>
1. <span data-ttu-id="47971-143">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="47971-143">Select **Save**.</span></span>

<span data-ttu-id="47971-144">In de volgende afbeelding ziet u voorbeeldgegevens van een rechtspersoon.</span><span class="sxs-lookup"><span data-stu-id="47971-144">The following image shows details of an example legal entity.</span></span>

![Sectie Algemeen van rechtspersoon](media/legal-entities-general.png)
   
## <a name="additional-resources"></a><span data-ttu-id="47971-146">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="47971-146">Additional resources</span></span>

[<span data-ttu-id="47971-147">Overzicht van Organisaties en organisatiehiërarchieën</span><span class="sxs-lookup"><span data-stu-id="47971-147">Organizations and organizational hierarchies overview</span></span>](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="47971-148">Uw organisatiehiërarchie plannen</span><span class="sxs-lookup"><span data-stu-id="47971-148">Plan your organizational hierarchy</span></span>](../fin-ops-core/fin-ops/organization-administration/plan-organizational-hierarchy.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="47971-149">Organisatiehiërarchieën</span><span class="sxs-lookup"><span data-stu-id="47971-149">Organization hierarchies</span></span>](channels-org-hierarchies.md)

[<span data-ttu-id="47971-150">Overzicht van kanalen</span><span class="sxs-lookup"><span data-stu-id="47971-150">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="47971-151">Vereisten voor het instellen van kanalen</span><span class="sxs-lookup"><span data-stu-id="47971-151">Channel setup prerequisites</span></span>](channels-prerequisites.md)
