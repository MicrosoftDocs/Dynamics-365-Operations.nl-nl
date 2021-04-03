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
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 490d466c10cfe0640f8fbcf8fe2298536e499d9b
ms.sourcegitcommit: c88b54ba13a4dfe39b844ffaced4dc435560c47d
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/19/2021
ms.locfileid: "5477991"
---
# <a name="set-up-organization-hierarchies"></a><span data-ttu-id="e4bdc-103">Organisatiehiërarchieën instellen</span><span class="sxs-lookup"><span data-stu-id="e4bdc-103">Set up organization hierarchies</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="e4bdc-104">In dit onderwerp wordt beschreven hoe u organisatiehiërarchieën instelt in Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="e4bdc-104">This topic describes how to set up organization hierarchies in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="e4bdc-105">Voordat u kanalen gaat maken, moet u controleren of uw organisatiehiërarchieën zijn ingesteld.</span><span class="sxs-lookup"><span data-stu-id="e4bdc-105">Before creating channels, you'll want to ensure you have set up your organization hierarchies.</span></span>

<span data-ttu-id="e4bdc-106">Met organisatiehiërarchieën kunt u vanuit verschillende gezichtspunten kijken naar en rapporteren over uw bedrijf.</span><span class="sxs-lookup"><span data-stu-id="e4bdc-106">You can use organization hierarchies to view and report on your business from various perspectives.</span></span> <span data-ttu-id="e4bdc-107">U kunt bijvoorbeeld een hiërarchie instellen voor belastingaangifte.</span><span class="sxs-lookup"><span data-stu-id="e4bdc-107">For example, you can set up one hierarchy for tax, legal, or statutory reporting.</span></span> <span data-ttu-id="e4bdc-108">Vervolgens kunt u een andere hiërarchie instellen voor het rapporteren van financiële gegevens die niet wettelijk vereist zijn, maar die voor interne rapportage worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="e4bdc-108">You can then set up another hierarchy to report financial information that is not legally required, but that is used for internal reporting.</span></span>

<span data-ttu-id="e4bdc-109">Voordat u een organisatiehiërarchie maakt, moet u organisaties maken.</span><span class="sxs-lookup"><span data-stu-id="e4bdc-109">Before you create an organization hierarchy, you must create organizations.</span></span> <span data-ttu-id="e4bdc-110">Zie voor meer informatie [Rechtspersonen maken](channels-legal-entities.md) of [Operationele eenheden maken](../fin-ops-core/fin-ops/organization-administration/tasks/create-operating-unit.md?toc=/dynamics365/commerce/toc.json).</span><span class="sxs-lookup"><span data-stu-id="e4bdc-110">For more information, see [Create legal entities](channels-legal-entities.md) or [Create operating units](../fin-ops-core/fin-ops/organization-administration/tasks/create-operating-unit.md?toc=/dynamics365/commerce/toc.json).</span></span>


<span data-ttu-id="e4bdc-111">Zie de volgende onderwerpen voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="e4bdc-111">For more information, see the following topics.</span></span>
- [<span data-ttu-id="e4bdc-112">Overzicht van Organisaties en organisatiehiërarchieën</span><span class="sxs-lookup"><span data-stu-id="e4bdc-112">Organizations and organizational hierarchies overview</span></span>](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)
- [<span data-ttu-id="e4bdc-113">Uw organisatiehiërarchie plannen</span><span class="sxs-lookup"><span data-stu-id="e4bdc-113">Plan your organization hierarchy</span></span>](../fin-ops-core/fin-ops/organization-administration/plan-organizational-hierarchy.md?toc=/dynamics365/commerce/toc.json)
- [<span data-ttu-id="e4bdc-114">Een organisatiehiërarchie maken</span><span class="sxs-lookup"><span data-stu-id="e4bdc-114">Create an organization hierarchy</span></span>](../fin-ops-core/fin-ops/organization-administration/tasks/create-organization-hierarchy.md?toc=/dynamics365/commerce/toc.json)

## <a name="create-an-organizational-hierarchy"></a><span data-ttu-id="e4bdc-115">Een organisatiehiërarchie maken</span><span class="sxs-lookup"><span data-stu-id="e4bdc-115">Create an organizational hierarchy</span></span>

<span data-ttu-id="e4bdc-116">Volg deze stappen om om een organisatiehiërarchie te maken.</span><span class="sxs-lookup"><span data-stu-id="e4bdc-116">To create an organizational hierarchy, follow these steps.</span></span>

1. <span data-ttu-id="e4bdc-117">Ga in het navigatievenster naar **Modules \> Retail en Commerce \> Afzetkanaalinstellingen \> Organisatiehiërarchieën**.</span><span class="sxs-lookup"><span data-stu-id="e4bdc-117">In the navigation pane, go to **Modules \> Retail and commerce \> Channel Setup \> Organization hierarchies**.</span></span>
1. <span data-ttu-id="e4bdc-118">Selecteer **Nieuw** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="e4bdc-118">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="e4bdc-119">Voer een waarde in het veld **Naam** in.</span><span class="sxs-lookup"><span data-stu-id="e4bdc-119">In the **Name** field, enter a value.</span></span>
1. <span data-ttu-id="e4bdc-120">Selecteer in de sectie **Doel** de optie **Doel toewijzen**.</span><span class="sxs-lookup"><span data-stu-id="e4bdc-120">In the **Purpose** section, select **Assign purpose**.</span></span>
1. <span data-ttu-id="e4bdc-121">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="e4bdc-121">In the list, find and select the desired record.</span></span> <span data-ttu-id="e4bdc-122">Selecteer een doel om aan uw organisatiehiërarchie toe te wijzen.</span><span class="sxs-lookup"><span data-stu-id="e4bdc-122">Select a purpose to assign to your organization hierarchy.</span></span>
1. <span data-ttu-id="e4bdc-123">Selecteer in de sectie **Toegewezen hiërarchieën** de optie **Toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="e4bdc-123">In the **Assigned hierarchies** section, select **Add**.</span></span>
1. <span data-ttu-id="e4bdc-124">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="e4bdc-124">In the list, mark the selected row.</span></span> <span data-ttu-id="e4bdc-125">Zoek de hiërarchie u zojuist hebt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="e4bdc-125">Find the hierarchy you just created.</span></span>
1. <span data-ttu-id="e4bdc-126">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="e4bdc-126">Select **OK**.</span></span>

<span data-ttu-id="e4bdc-127">De volgende afbeelding toont een voorbeeld van een organisatiehiërarchie die is gemaakt voor een fictieve reeks winkels van Adventure Works.</span><span class="sxs-lookup"><span data-stu-id="e4bdc-127">The following image shows an example organizational hierarchy created for a fictitious "Adventure Works" set of stores.</span></span>

![Voorbeeld van een organisatiehiërarchie](media/organizational-hierarchies.png)

### <a name="add-organizations-to-a-hierarchy"></a><span data-ttu-id="e4bdc-129">Organisaties aan een hiërarchie toevoegen</span><span class="sxs-lookup"><span data-stu-id="e4bdc-129">Add organizations to a hierarchy</span></span>

<span data-ttu-id="e4bdc-130">Volg deze stappen om organisaties toe te voegen aan een hiërarchie.</span><span class="sxs-lookup"><span data-stu-id="e4bdc-130">To add organizations to a hierarchy, follow these steps.</span></span>

1. <span data-ttu-id="e4bdc-131">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="e4bdc-131">In the list, find and select the desired record.</span></span> <span data-ttu-id="e4bdc-132">Selecteer uw hiërarchie.</span><span class="sxs-lookup"><span data-stu-id="e4bdc-132">Select your hierarchy.</span></span>
1. <span data-ttu-id="e4bdc-133">Selecteer **Weergeven** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="e4bdc-133">On the action pane, select **View**.</span></span>
1. <span data-ttu-id="e4bdc-134">Voer zo nodig organisaties toe.</span><span class="sxs-lookup"><span data-stu-id="e4bdc-134">Add organizations, as necessary.</span></span>
1. <span data-ttu-id="e4bdc-135">Als u een organisatie wilt toevoegen, selecteert u **Bewerken** en vervolgens **Invoegen**.</span><span class="sxs-lookup"><span data-stu-id="e4bdc-135">To add an organization, select **Edit** and then select **Insert**.</span></span> <span data-ttu-id="e4bdc-136">Wanneer u klaar bent met het aanbrengen van wijzigingen, kunt u een concept opslaan en de wijzigingen publiceren.</span><span class="sxs-lookup"><span data-stu-id="e4bdc-136">When you are done making changes you can save a draft and publish the changes.</span></span>

<span data-ttu-id="e4bdc-137">De volgende afbeelding toont een rechtspersoon die is toegevoegd aan de hiërarchiebasis. Er zijn vier kostenplaatsen toegevoegd: de kanalen winkelcentrum, outlet, online en callcenter.</span><span class="sxs-lookup"><span data-stu-id="e4bdc-137">The following image shows a legal entity added at the hierarchy root with four cost centers added for "Mall", "Outlet", "Online" and "Call Center" channels.</span></span> <span data-ttu-id="e4bdc-138">Aan elke winkel kunnen diverse detailhandels-, callcenter- en onlinekanalen worden toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="e4bdc-138">Various retail, call center and online channels can then be added to each.</span></span>

![Voorbeeld van hiërarchieontwerper](media/hierarchy-designer.png)

## <a name="additional-resources"></a><span data-ttu-id="e4bdc-140">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="e4bdc-140">Additional resources</span></span>

[<span data-ttu-id="e4bdc-141">Overzicht van Organisaties en organisatiehiërarchieën</span><span class="sxs-lookup"><span data-stu-id="e4bdc-141">Organizations and organizational hierarchies overview</span></span>](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="e4bdc-142">Uw organisatiehiërarchie plannen</span><span class="sxs-lookup"><span data-stu-id="e4bdc-142">Plan your organizational hierarchy</span></span>](../fin-ops-core/fin-ops/organization-administration/plan-organizational-hierarchy.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="e4bdc-143">Rechtspersonen maken</span><span class="sxs-lookup"><span data-stu-id="e4bdc-143">Create legal entities</span></span>](channels-legal-entities.md)

[<span data-ttu-id="e4bdc-144">Operationele eenheden maken</span><span class="sxs-lookup"><span data-stu-id="e4bdc-144">Create operating units</span></span>](../fin-ops-core/fin-ops/organization-administration/tasks/create-operating-unit.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="e4bdc-145">Overzicht van kanalen</span><span class="sxs-lookup"><span data-stu-id="e4bdc-145">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="e4bdc-146">Vereisten voor het instellen van kanalen</span><span class="sxs-lookup"><span data-stu-id="e4bdc-146">Channel setup prerequisites</span></span>](channels-prerequisites.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
