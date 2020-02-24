---
title: Overzicht van de previewomgeving voor Dynamics 365 Commerce
description: Dit onderwerp biedt een overzicht van de preview-omgeving van Microsoft Dynamics 365 Commerce.
author: v-chgri
manager: annbe
ms.date: 12/10/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: v-chgri
ms.search.validFrom: 2019-12-10
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 1ff96aeb5963df9ddee56783a089dad129bbb71c
ms.sourcegitcommit: 4ed1d8ad8a0206a4172dbb41cc43f7d95073059c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/04/2020
ms.locfileid: "3024678"
---
# <a name="dynamics-365-commerce-preview-environment-overview"></a><span data-ttu-id="56137-103">Overzicht van de previewomgeving voor Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="56137-103">Dynamics 365 Commerce preview environment overview</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="56137-104">Dit onderwerp biedt een overzicht van de preview-omgeving van Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="56137-104">This topic gives an overview of the Microsoft Dynamics 365 Commerce preview environment.</span></span>

## <a name="overview"></a><span data-ttu-id="56137-105">Overzicht</span><span class="sxs-lookup"><span data-stu-id="56137-105">Overview</span></span>

<span data-ttu-id="56137-106">De preview-omgeving van Commerce is een optionele end-to-end preview-omgeving van Dynamics 365 Commerce waarmee potentiële klanten het Commerce-product kunnen uitproberen voordat dit product algemeen wordt uitgebracht.</span><span class="sxs-lookup"><span data-stu-id="56137-106">The Commerce preview environment is an optional end-to-end preview environment of Dynamics 365 Commerce that lets potential customers try out the Commerce product before its general release to the public.</span></span>

<span data-ttu-id="56137-107">Afgezien van enkele kleine beperkingen die geen invloed hebben op functies of functionaliteit, biedt de preview-omgeving van Commerce de volledige Commerce-ervaring en deze kan worden gebruikt door klanten en implementatiepartners om het product te evalueren, feedback te geven en geschiktheids-/hiaatanalyses uit te voeren.</span><span class="sxs-lookup"><span data-stu-id="56137-107">Aside from some minor limitations that don't affect features or functionality, the Commerce preview environment provides the complete Commerce experience, and can be used by customers and implementation partners to evaluate the product, provide feedback, and do fit/gap analysis.</span></span>

## <a name="limitations-of-the-commerce-preview-environment"></a><span data-ttu-id="56137-108">Beperkingen van de preview-omgeving van Commerce</span><span class="sxs-lookup"><span data-stu-id="56137-108">Limitations of the Commerce preview environment</span></span>

<span data-ttu-id="56137-109">Hoewel de preview-omgeving van Commerce alle Commerce-functies en -functionaliteit biedt, zijn er enkele kleine beperkingen:</span><span class="sxs-lookup"><span data-stu-id="56137-109">Although the Commerce preview environment provides the full set of Commerce features and functionality, there are some minor limitations:</span></span>

- <span data-ttu-id="56137-110">Hoewel de preview-omgeving van Commerce zelf geen geografische beperkingen heeft, kunnen onderdelen van de omgeving, zoals Retail Cloud Scale Unit (RCSU) en e-Commerce, alleen in de Verenigde Staten worden ingericht.</span><span class="sxs-lookup"><span data-stu-id="56137-110">Although the Commerce preview environment itself has no geographical limitations, components of the environment, such as the Retail Cloud Scale Unit (RCSU) and e-Commerce applications, can be provisioned only in the United States.</span></span>
- <span data-ttu-id="56137-111">De preview-omgeving van Commerce heeft een tijdslimiet van 30 dagen vanaf de datum waarop e-Commerce wordt ingericht.</span><span class="sxs-lookup"><span data-stu-id="56137-111">Use of the Commerce preview environment is limited to 30 days from the date when e-Commerce is provisioned.</span></span>
- <span data-ttu-id="56137-112">De preview-omgeving van Commerce kan alleen worden geïmplementeerd en geïnitialiseerd in een omgeving die gebruikmaakt van de demotopologie, waarbij alle onderdelen van een omgeving worden geïmplementeerd in één VM (virtuele machine).</span><span class="sxs-lookup"><span data-stu-id="56137-112">The Commerce preview environment can be successfully deployed and initialized only in an environment that uses the demo topology, where all components of an environment are deployed in a single virtual machine (VM).</span></span> <span data-ttu-id="56137-113">De belangrijkste beperking van deze OneBox VM-topologie is het aantal gebruikers dat de preview-omgeving gelijktijdig kan ondersteunen.</span><span class="sxs-lookup"><span data-stu-id="56137-113">The main limitation of this OneBox VM topology is the number of concurrent users that the preview environment can support.</span></span>
- <span data-ttu-id="56137-114">De preview-omgeving van Commerce kan alleen worden geëvalueerd tot het Commerce-product algemeen beschikbaar wordt.</span><span class="sxs-lookup"><span data-stu-id="56137-114">The Commerce preview environment can be evaluated only until the general availability (GA) of the Commerce product.</span></span> <span data-ttu-id="56137-115">Zodra het Commerce-product algemeen beschikbaar wordt, worden weer andere demo-omgevingen beschikbaar.</span><span class="sxs-lookup"><span data-stu-id="56137-115">New demo environments will be available after GA.</span></span>

## <a name="get-started"></a><span data-ttu-id="56137-116">Aan de slag</span><span class="sxs-lookup"><span data-stu-id="56137-116">Get started</span></span>

<span data-ttu-id="56137-117">Zie [Een preview-omgeving van Commerce inrichten](provisioning-guide.md) om de preview-omgeving van Commerce in te richten.</span><span class="sxs-lookup"><span data-stu-id="56137-117">To provision the Commerce preview environment, see [Provision a Commerce preview environment](provisioning-guide.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="56137-118">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="56137-118">Additional resources</span></span>

[<span data-ttu-id="56137-119">Een previewomgeving voor Dynamics 365 Commerce inrichten</span><span class="sxs-lookup"><span data-stu-id="56137-119">Provision a Dynamics 365 Commerce preview environment</span></span>](provisioning-guide.md)

[<span data-ttu-id="56137-120">Een Dynamics 365 Commerce-preview-omgeving configureren</span><span class="sxs-lookup"><span data-stu-id="56137-120">Configure a Dynamics 365 Commerce preview environment</span></span>](cpe-post-provisioning.md)

[<span data-ttu-id="56137-121">Optionele functies voor een Dynamics 365 Commerce-preview-omgeving configureren</span><span class="sxs-lookup"><span data-stu-id="56137-121">Configure optional features for a Dynamics 365 Commerce preview environment</span></span>](cpe-optional-features.md)

[<span data-ttu-id="56137-122">Veelgestelde vragen over Dynamics 365 Commerce-preview-omgeving</span><span class="sxs-lookup"><span data-stu-id="56137-122">Dynamics 365 Commerce preview environment FAQ</span></span>](cpe-faq.md)
