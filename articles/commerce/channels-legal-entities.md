---
title: Rechtspersonen maken
description: In dit onderwerp wordt beschreven hoe u rechtspersonen kunt maken in Microsoft Dynamics 365 Commerce. Deze moeten worden gemaakt en geconfigureerd voordat u afzetkanalen gaat maken.
author: samjarawan
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 225fd6a07fee29414ac30a4602b4dfccdc4d742b
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/31/2021
ms.locfileid: "5800609"
---
# <a name="create-legal-entities"></a><span data-ttu-id="3dab5-103">Rechtspersonen maken</span><span class="sxs-lookup"><span data-stu-id="3dab5-103">Create legal entities</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="3dab5-104">In dit onderwerp wordt beschreven hoe u rechtspersonen kunt maken in Microsoft Dynamics 365 Commerce. Deze moeten worden gemaakt en geconfigureerd voordat u afzetkanalen gaat maken.</span><span class="sxs-lookup"><span data-stu-id="3dab5-104">This topic describes how to create legal entities in Microsoft Dynamics 365 Commerce, which must be created and configured before creating channels.</span></span>

<span data-ttu-id="3dab5-105">Een rechtspersoon is een organisatie met een geregistreerde of wettelijke juridische structuur.</span><span class="sxs-lookup"><span data-stu-id="3dab5-105">A legal entity is an organization that has a registered or legislated legal structure.</span></span> <span data-ttu-id="3dab5-106">Rechtspersonen kunnen wettelijk bindende overeenkomsten aangaan en zijn verplicht prestatieoverzichten te overleggen.</span><span class="sxs-lookup"><span data-stu-id="3dab5-106">Legal entities can enter into legal contracts and are required to prepare statements that report on their performance.</span></span>

<span data-ttu-id="3dab5-107">Een bedrijf is een type rechtspersoon.</span><span class="sxs-lookup"><span data-stu-id="3dab5-107">A company is a type of legal entity.</span></span> <span data-ttu-id="3dab5-108">Momenteel zijn bedrijven het enige type rechtspersoon dat u kunt maken. Aan elke rechtspersoon is een bedrijfs-id gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="3dab5-108">Currently, companies are the only kind of legal entity that you can create, and every legal entity is associated with a company ID.</span></span> <span data-ttu-id="3dab5-109">Deze koppeling bestaat omdat een aantal functionele gebieden in het programma een bedrijfs-id of *DataAreaId* in hun gegevensmodellen gebruiken.</span><span class="sxs-lookup"><span data-stu-id="3dab5-109">This association exists because some functional areas in the program use a company ID, or *DataAreaId*, in their data models.</span></span> <span data-ttu-id="3dab5-110">In deze functionele gebieden worden bedrijven gebruikt als begrenzing voor gegevensbeveiliging.</span><span class="sxs-lookup"><span data-stu-id="3dab5-110">In these functional areas, companies are used as a boundary for data security.</span></span> <span data-ttu-id="3dab5-111">Gebruikers hebben alleen toegang tot gegevens voor het bedrijf waarbij ze momenteel zijn aangemeld.</span><span class="sxs-lookup"><span data-stu-id="3dab5-111">Users can access data only for the company that they are currently logged on to.</span></span> 

<span data-ttu-id="3dab5-112">Wanneer u een kanaal maakt, moet u opgeven tot welke rechtspersoon het afzetkanaal behoort.</span><span class="sxs-lookup"><span data-stu-id="3dab5-112">When creating a channel, you must specify which legal entity that channel belongs to.</span></span>

## <a name="create-a-new-legal-entity"></a><span data-ttu-id="3dab5-113">Een nieuwe rechtspersoon maken</span><span class="sxs-lookup"><span data-stu-id="3dab5-113">Create a new legal entity</span></span>

<span data-ttu-id="3dab5-114">Ga als volgt te werk om een nieuwe rechtspersoon te maken in Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="3dab5-114">To create a new legal entity in Dynamics 365 Commerce, follow these steps.</span></span>

1. <span data-ttu-id="3dab5-115">Ga in het navigatiedeelvenster naar **Modules \> Headquarters instellen \> Rechtspersonen**.</span><span class="sxs-lookup"><span data-stu-id="3dab5-115">In the navigation pane, go to  **Modules \> Headquarters setup \> Legal entities**.</span></span>
1. <span data-ttu-id="3dab5-116">Selecteer **Nieuw** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="3dab5-116">On the action pane, select **New**.</span></span> <span data-ttu-id="3dab5-117">Het deelvenster **Nieuwe rechtspersoon** verschijnt aan de rechterkant.</span><span class="sxs-lookup"><span data-stu-id="3dab5-117">The **New legal entity** pane appears on the right.</span></span>
1. <span data-ttu-id="3dab5-118">Voer een waarde in het veld **Naam** in.</span><span class="sxs-lookup"><span data-stu-id="3dab5-118">In the **Name** field, enter a value.</span></span>
1. <span data-ttu-id="3dab5-119">Voer een waarde in het veld **Bedrijf** in.</span><span class="sxs-lookup"><span data-stu-id="3dab5-119">In the **Company** field, enter a value.</span></span>
1. <span data-ttu-id="3dab5-120">Typ of selecteer een waarde in het **veld Land/regio**.</span><span class="sxs-lookup"><span data-stu-id="3dab5-120">In the **Country/region** field, enter or select a value.</span></span>
1. <span data-ttu-id="3dab5-121">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="3dab5-121">Select **OK**.</span></span> 

   ![Het maken van een rechtspersoon](media/legal-entities.png)

1. <span data-ttu-id="3dab5-123">Geef in de sectie **Algemeen** de volgende algemene informatie op over de rechtspersoon:</span><span class="sxs-lookup"><span data-stu-id="3dab5-123">In the **General** section, provide the following general information about the legal entity:</span></span> 
   1. <span data-ttu-id="3dab5-124">Voer een zoeknaam in als een zoeknaam is vereist.</span><span class="sxs-lookup"><span data-stu-id="3dab5-124">Enter a search name, if a search name is required.</span></span> <span data-ttu-id="3dab5-125">Een zoeknaam is een alternatieve naam waarmee u naar deze rechtspersoon kunt zoeken.</span><span class="sxs-lookup"><span data-stu-id="3dab5-125">A search name is an alternate name that can be used to search for this legal entity.</span></span> 
   1. <span data-ttu-id="3dab5-126">Selecteer of deze rechtspersoon wordt gebruikt als consolidatiebedrijf.</span><span class="sxs-lookup"><span data-stu-id="3dab5-126">Select whether this legal entity is being used as a consolidation company.</span></span>
   1. <span data-ttu-id="3dab5-127">Selecteer of deze rechtspersoon wordt gebruikt als eliminatiebedrijf.</span><span class="sxs-lookup"><span data-stu-id="3dab5-127">Select whether this legal entity is being used as an elimination company.</span></span> 
   1. <span data-ttu-id="3dab5-128">Selecteer de **standaardtaal** voor de rechtspersoon.</span><span class="sxs-lookup"><span data-stu-id="3dab5-128">Select the **default language** for the entity.</span></span> 
   1. <span data-ttu-id="3dab5-129">Selecteer de **tijdzone** voor de rechtspersoon.</span><span class="sxs-lookup"><span data-stu-id="3dab5-129">Select the **time zone** for the entity.</span></span>
1. <span data-ttu-id="3dab5-130">Selecteer in de sectie **Adressen** de optie **Bewerken** om adresgegevens in te vullen, zoals straatnaam en -nummer, postcode en plaats.</span><span class="sxs-lookup"><span data-stu-id="3dab5-130">In the **Addresses** section, select **Edit** to enter address information, such as the street name and number, postal code, and city.</span></span>
1. <span data-ttu-id="3dab5-131">Voer in de sectie **Contactgegevens** informatie in over communicatiemethoden, zoals e-mailadressen, URL's en telefoonnummers.</span><span class="sxs-lookup"><span data-stu-id="3dab5-131">In the **Contact information** section, enter information about methods of communication, such as email addresses, URLs, and telephone numbers.</span></span>
1. <span data-ttu-id="3dab5-132">Voer in de sectie **Wettelijke rapportage** de registratienummers in die worden gebruikt voor wettelijke aangiften.</span><span class="sxs-lookup"><span data-stu-id="3dab5-132">In the **Statutory reporting** section, enter the registration numbers that are used for statutory reporting.</span></span>
1. <span data-ttu-id="3dab5-133">Voer in de sectie **Registratienummers** informatie in die door de rechtspersoon wordt vereist.</span><span class="sxs-lookup"><span data-stu-id="3dab5-133">In the **Registration numbers** section, enter any information required by the legal entity.</span></span>
1. <span data-ttu-id="3dab5-134">Voer in de sectie **Bankrekeninggegevens** bankrekeningen en routenummers in voor de rechtspersoon.</span><span class="sxs-lookup"><span data-stu-id="3dab5-134">In the **Bank account information** section, enter bank accounts and routing numbers for the legal entity.</span></span>
1. <span data-ttu-id="3dab5-135">Voer in de sectie **Buitenlandse handel en logistiek** verzendingsgegevens voor de rechtspersoon in.</span><span class="sxs-lookup"><span data-stu-id="3dab5-135">In the **Foreign trade and logistics** section, enter shipping information for the legal entity.</span></span>
1. <span data-ttu-id="3dab5-136">In de sectie **Nummerreeksen** kunt u de nummerreeksen weergeven die aan de rechtspersoon zijn gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="3dab5-136">In the **Number sequences** section, you can view the number sequences that are associated with the legal entity.</span></span> <span data-ttu-id="3dab5-137">Deze is in eerste instantie leeg.</span><span class="sxs-lookup"><span data-stu-id="3dab5-137">This will be empty to start with.</span></span>
1. <span data-ttu-id="3dab5-138">In de sectie **Dashboardafbeelding** kunt u het logo en/of de dashboardafbeelding bekijken of wijzigen die aan de rechtspersoon zijn gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="3dab5-138">In the **Dashboard image** section, view or change the logo and dashboard image associated with the legal entity.</span></span>
1. <span data-ttu-id="3dab5-139">Voer in de sectie **Belastingregistratie** de registratienummers in die worden gebruikt om te rapporteren aan de belastingdienst.</span><span class="sxs-lookup"><span data-stu-id="3dab5-139">In the **Tax registration** section, enter the registration numbers that are used to report to tax authorities.</span></span>
1. <span data-ttu-id="3dab5-140">Voer in de **1099-belasting** 1099-gegevens voor de rechtspersoon in.</span><span class="sxs-lookup"><span data-stu-id="3dab5-140">In the **Tax 1099** section, enter 1099 information for the legal entity.</span></span>
1. <span data-ttu-id="3dab5-141">In de sectie **Belastinginformatie** voert u de belastinginformatie voor de rechtspersoon in.</span><span class="sxs-lookup"><span data-stu-id="3dab5-141">In the **Tax invormation** section, enter tax information for the legal entity.</span></span>
1. <span data-ttu-id="3dab5-142">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="3dab5-142">Select **Save**.</span></span>

<span data-ttu-id="3dab5-143">In de volgende afbeelding ziet u voorbeeldgegevens van een rechtspersoon.</span><span class="sxs-lookup"><span data-stu-id="3dab5-143">The following image shows details of an example legal entity.</span></span>

![Sectie Algemeen van rechtspersoon](media/legal-entities-general.png)
   
## <a name="additional-resources"></a><span data-ttu-id="3dab5-145">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="3dab5-145">Additional resources</span></span>

[<span data-ttu-id="3dab5-146">Overzicht van Organisaties en organisatiehiërarchieën</span><span class="sxs-lookup"><span data-stu-id="3dab5-146">Organizations and organizational hierarchies overview</span></span>](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="3dab5-147">Uw organisatiehiërarchie plannen</span><span class="sxs-lookup"><span data-stu-id="3dab5-147">Plan your organizational hierarchy</span></span>](../fin-ops-core/fin-ops/organization-administration/plan-organizational-hierarchy.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="3dab5-148">Organisatiehiërarchieën</span><span class="sxs-lookup"><span data-stu-id="3dab5-148">Organization hierarchies</span></span>](channels-org-hierarchies.md)

[<span data-ttu-id="3dab5-149">Overzicht van kanalen</span><span class="sxs-lookup"><span data-stu-id="3dab5-149">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="3dab5-150">Vereisten voor het instellen van kanalen</span><span class="sxs-lookup"><span data-stu-id="3dab5-150">Channel setup prerequisites</span></span>](channels-prerequisites.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
