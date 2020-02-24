---
title: Organisatiehiërarchieën instellen
description: In dit onderwerp wordt beschreven hoe u organisatiehiërarchieën instelt in Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: 6c19542089526c1e17fb1133d52cf042f244fb80
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/01/2020
ms.locfileid: "3002330"
---
# <a name="set-up-organization-hierarchies"></a><span data-ttu-id="7376e-103">Organisatiehiërarchieën instellen</span><span class="sxs-lookup"><span data-stu-id="7376e-103">Set up organization hierarchies</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="7376e-104">In dit onderwerp wordt beschreven hoe u organisatiehiërarchieën instelt in Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="7376e-104">This topic descibes how to set up organization hierarchies in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="7376e-105">Overzicht</span><span class="sxs-lookup"><span data-stu-id="7376e-105">Overview</span></span>

<span data-ttu-id="7376e-106">Voordat u kanalen gaat maken, moet u controleren of uw organisatiehiërarchieën zijn ingesteld.</span><span class="sxs-lookup"><span data-stu-id="7376e-106">Before creating channels, you'll want to ensure you have set up your organization hierarchies.</span></span>

<span data-ttu-id="7376e-107">Met organisatiehiërarchieën kunt u vanuit verschillende gezichtspunten kijken naar en rapporteren over uw bedrijf.</span><span class="sxs-lookup"><span data-stu-id="7376e-107">You can use organization hierarchies to view and report on your business from various perspectives.</span></span> <span data-ttu-id="7376e-108">U kunt bijvoorbeeld een hiërarchie instellen voor belastingaangifte.</span><span class="sxs-lookup"><span data-stu-id="7376e-108">For example, you can set up one hierarchy for tax, legal, or statutory reporting.</span></span> <span data-ttu-id="7376e-109">Vervolgens kunt u een andere hiërarchie instellen voor het rapporteren van financiële gegevens die niet wettelijk vereist zijn, maar die voor interne rapportage worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="7376e-109">You can then set up another hierarchy to report financial information that is not legally required, but that is used for internal reporting.</span></span>

<span data-ttu-id="7376e-110">Voordat u een organisatiehiërarchie maakt, moet u organisaties maken.</span><span class="sxs-lookup"><span data-stu-id="7376e-110">Before you create an organization hierarchy, you must create organizations.</span></span> <span data-ttu-id="7376e-111">Zie voor meer informatie [Rechtspersonen maken](channels-legal-entities.md) of [Operationele eenheden maken](../fin-ops-core/fin-ops/organization-administration/tasks/create-operating-unit.md?toc=/dynamics365/commerce/toc.json).</span><span class="sxs-lookup"><span data-stu-id="7376e-111">For more information, see [Create legal entities](channels-legal-entities.md) or [Create operating units](../fin-ops-core/fin-ops/organization-administration/tasks/create-operating-unit.md?toc=/dynamics365/commerce/toc.json).</span></span>


<span data-ttu-id="7376e-112">Zie de volgende onderwerpen voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="7376e-112">For more information, see the following topics.</span></span>
- [<span data-ttu-id="7376e-113">Overzicht van Organisaties en organisatiehiërarchieën</span><span class="sxs-lookup"><span data-stu-id="7376e-113">Organizations and organizational hierarchies overview</span></span>](https://docs.microsoft.com/en-us/dynamics365/fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies)
- [<span data-ttu-id="7376e-114">Uw organisatiehiërarchie plannen</span><span class="sxs-lookup"><span data-stu-id="7376e-114">Plan your organization hierarchy</span></span>](https://docs.microsoft.com/en-us/dynamics365/fin-ops-core/fin-ops/organization-administration/plan-organizational-hierarchy?toc=/dynamics365/commerce/toc.json)
- [<span data-ttu-id="7376e-115">Een organisatiehiërarchie maken</span><span class="sxs-lookup"><span data-stu-id="7376e-115">Create an organization hierarchy</span></span>](https://docs.microsoft.com/en-us/dynamics365/fin-ops-core/fin-ops/organization-administration/tasks/create-organization-hierarchy?toc=/dynamics365/commerce/toc.json)

## <a name="create-an-organizational-hierarchy"></a><span data-ttu-id="7376e-116">Een organisatiehiërarchie maken</span><span class="sxs-lookup"><span data-stu-id="7376e-116">Create an organizational hierarchy</span></span>

<span data-ttu-id="7376e-117">Volg deze stappen om om een organisatiehiërarchie te maken.</span><span class="sxs-lookup"><span data-stu-id="7376e-117">To create an organizational hierarchy, follow these steps.</span></span>

1. <span data-ttu-id="7376e-118">Ga in het navigatievenster naar **Modules \> Retail en Commerce \> Afzetkanaalinstellingen \> Organisatiehiërarchieën**.</span><span class="sxs-lookup"><span data-stu-id="7376e-118">In the navigation pane, go to **Modules \> Retail and commerce \> Channel Setup \> Organization hierarchies**.</span></span>
1. <span data-ttu-id="7376e-119">Selecteer **Nieuw** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="7376e-119">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="7376e-120">Voer een waarde in het veld **Naam** in.</span><span class="sxs-lookup"><span data-stu-id="7376e-120">In the **Name** field, enter a value.</span></span>
1. <span data-ttu-id="7376e-121">Selecteer in de sectie **Doel** de optie **Doel toewijzen**.</span><span class="sxs-lookup"><span data-stu-id="7376e-121">In the **Purpose** section, select **Assign purpose**.</span></span>
1. <span data-ttu-id="7376e-122">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="7376e-122">In the list, find and select the desired record.</span></span> <span data-ttu-id="7376e-123">Selecteer een doel om aan uw organisatiehiërarchie toe te wijzen.</span><span class="sxs-lookup"><span data-stu-id="7376e-123">Select a purpose to assign to your organization hierarchy.</span></span>
1. <span data-ttu-id="7376e-124">Selecteer in de sectie **Toegewezen hiërarchieën** de optie **Toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="7376e-124">In the **Assigned hierarchies** section, select **Add**.</span></span>
1. <span data-ttu-id="7376e-125">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="7376e-125">In the list, mark the selected row.</span></span> <span data-ttu-id="7376e-126">Zoek de hiërarchie u zojuist hebt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="7376e-126">Find the hierarchy you just created.</span></span>
1. <span data-ttu-id="7376e-127">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="7376e-127">Select **OK**.</span></span>

<span data-ttu-id="7376e-128">De volgende afbeelding toont een voorbeeld van een organisatiehiërarchie die is gemaakt voor een fictieve reeks winkels van Adventure Works.</span><span class="sxs-lookup"><span data-stu-id="7376e-128">The following image shows an example organizational hierarchy created for a fictitious "Adventure Works" set of stores.</span></span>

![Voorbeeld van een organisatiehiërarchie](media/organizational-hierarchies.png)

### <a name="add-organizations-to-a-hierarchy"></a><span data-ttu-id="7376e-130">Organisaties aan een hiërarchie toevoegen</span><span class="sxs-lookup"><span data-stu-id="7376e-130">Add organizations to a hierarchy</span></span>

<span data-ttu-id="7376e-131">Volg deze stappen om organisaties toe te voegen aan een hiërarchie.</span><span class="sxs-lookup"><span data-stu-id="7376e-131">To add organizations to a hierarchy, follow these steps.</span></span>

1. <span data-ttu-id="7376e-132">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="7376e-132">In the list, find and select the desired record.</span></span> <span data-ttu-id="7376e-133">Selecteer uw hiërarchie.</span><span class="sxs-lookup"><span data-stu-id="7376e-133">Select your hierarchy.</span></span>
1. <span data-ttu-id="7376e-134">Selecteer **Weergeven** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="7376e-134">On the action pane, select **View**.</span></span>
1. <span data-ttu-id="7376e-135">Voer zo nodig organisaties toe.</span><span class="sxs-lookup"><span data-stu-id="7376e-135">Add organizations, as necessary.</span></span>
1. <span data-ttu-id="7376e-136">Als u een organisatie wilt toevoegen, selecteert u **Bewerken** en vervolgens **Invoegen**.</span><span class="sxs-lookup"><span data-stu-id="7376e-136">To add an organization, select **Edit** and then select **Insert**.</span></span> <span data-ttu-id="7376e-137">Wanneer u klaar bent met het aanbrengen van wijzigingen, kunt u een concept opslaan en de wijzigingen publiceren.</span><span class="sxs-lookup"><span data-stu-id="7376e-137">When you are done making changes you can save a draft and publish the changes.</span></span>

<span data-ttu-id="7376e-138">De volgende afbeelding toont een rechtspersoon die is toegevoegd aan de hiërarchiebasis. Er zijn vier kostenplaatsen toegevoegd: de kanalen winkelcentrum, outlet, online en callcenter.</span><span class="sxs-lookup"><span data-stu-id="7376e-138">The following image shows a legal entity added at the hierarchy root with four cost centers added for "Mall", "Outlet", "Online" and "Call Center" channels.</span></span> <span data-ttu-id="7376e-139">Aan elke winkel kunnen diverse detailhandels-, callcenter- en onlinekanalen worden toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="7376e-139">Various retail, call center and online channels can then be added to each.</span></span>

![Voorbeeld van hiërarchieontwerper](media/hierarchy-designer.png)

## <a name="additional-resources"></a><span data-ttu-id="7376e-141">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="7376e-141">Additional resources</span></span>

[<span data-ttu-id="7376e-142">Overzicht van Organisaties en organisatiehiërarchieën</span><span class="sxs-lookup"><span data-stu-id="7376e-142">Organizations and organizational hierarchies overview</span></span>](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="7376e-143">Uw organisatiehiërarchie plannen</span><span class="sxs-lookup"><span data-stu-id="7376e-143">Plan your organizational hierarchy</span></span>](../fin-ops-core/fin-ops/organization-administration/plan-organizational-hierarchy.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="7376e-144">Rechtspersonen maken</span><span class="sxs-lookup"><span data-stu-id="7376e-144">Create legal entities</span></span>](channels-legal-entities.md)

[<span data-ttu-id="7376e-145">Operationele eenheden maken</span><span class="sxs-lookup"><span data-stu-id="7376e-145">Create operating units</span></span>](../fin-ops-core/fin-ops/organization-administration/tasks/create-operating-unit.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="7376e-146">Overzicht van kanalen</span><span class="sxs-lookup"><span data-stu-id="7376e-146">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="7376e-147">Vereisten voor het instellen van kanalen</span><span class="sxs-lookup"><span data-stu-id="7376e-147">Channel setup prerequisites</span></span>](channels-prerequisites.md)
