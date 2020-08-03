---
title: Overzicht van de evaluatieomgeving voor Dynamics 365 Commerce
description: Dit onderwerp biedt een overzicht van de evaluatieomgeving van Microsoft Dynamics 365 Commerce.
author: v-chgri
manager: annbe
ms.date: 07/16/2020
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
ms.openlocfilehash: 25c0574e8d4502bcb846fba0ddf913d81eded87b
ms.sourcegitcommit: 5175e3fae432016246244cf70fe05465f43de88c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 07/17/2020
ms.locfileid: "3599747"
---
# <a name="dynamics-365-commerce-evaluation-environment-overview"></a><span data-ttu-id="e314f-103">Overzicht van de evaluatieomgeving voor Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="e314f-103">Dynamics 365 Commerce evaluation environment overview</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="e314f-104">Dit onderwerp biedt een overzicht van de evaluatieomgeving van Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="e314f-104">This topic gives an overview of the Microsoft Dynamics 365 Commerce evaluation environment.</span></span>

> [!NOTE]
> <span data-ttu-id="e314f-105">Commerce-evaluatieomgevingen zijn doorgaans niet beschikbaar en worden aan partners en klanten op aanvraag ter beschikking gesteld.</span><span class="sxs-lookup"><span data-stu-id="e314f-105">Commerce evaluation environments aren't generally available, and are granted to partners and customers on a per-request basis.</span></span> <span data-ttu-id="e314f-106">Neem contact op met uw Microsoft-partner voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="e314f-106">For more information, reach out to your Microsoft partner contact.</span></span>

## <a name="overview"></a><span data-ttu-id="e314f-107">Overzicht</span><span class="sxs-lookup"><span data-stu-id="e314f-107">Overview</span></span>

<span data-ttu-id="e314f-108">De evaluatieomgeving van Commerce is een optionele end-to-end omgeving van Dynamics 365 Commerce waarmee partners en potentiële klanten het Commerce-product kunnen uitproberen.</span><span class="sxs-lookup"><span data-stu-id="e314f-108">The Commerce evaluation environment is an optional end-to-end environment of Dynamics 365 Commerce that lets partners and potential customers try out the Commerce product.</span></span>

<span data-ttu-id="e314f-109">Evaluatieomgevingen zijn gedeeltelijk vooraf geconfigureerd om de vereiste stappen na inrichting te verminderen.</span><span class="sxs-lookup"><span data-stu-id="e314f-109">Evaluation environments are partially preconfigured to reduce the required post-provisioning steps.</span></span>

<span data-ttu-id="e314f-110">Afgezien van enkele kleine beperkingen die geen invloed hebben op functies of functionaliteit, biedt de evaluatieomgeving van Commerce de volledige Commerce-ervaring en deze kan worden gebruikt door klanten en implementatiepartners om het product te evalueren, feedback te geven en geschiktheids-/hiaatanalyses uit te voeren.</span><span class="sxs-lookup"><span data-stu-id="e314f-110">Aside from some minor limitations that don't affect features or functionality, the Commerce evaluation environment provides the complete Commerce experience, and can be used by customers and implementation partners to evaluate the product, provide feedback, and do fit/gap analysis.</span></span>

## <a name="limitations-of-the-commerce-evaluation-environment"></a><span data-ttu-id="e314f-111">Beperkingen van de evaluatieomgeving van Commerce</span><span class="sxs-lookup"><span data-stu-id="e314f-111">Limitations of the Commerce evaluation environment</span></span>

<span data-ttu-id="e314f-112">Hoewel de evaluatieomgeving van Commerce alle Commerce-functies en -functionaliteit biedt, zijn er enkele kleine beperkingen:</span><span class="sxs-lookup"><span data-stu-id="e314f-112">Although the Commerce evaluation environment provides the full set of Commerce features and functionality, there are some minor limitations:</span></span>

- <span data-ttu-id="e314f-113">Hoewel de evaluatieomgeving van Commerce zelf geen geografische beperkingen heeft, kunnen onderdelen van de omgeving, zoals Retail Cloud Scale Unit (RCSU) en e-Commerce, alleen in de Verenigde Staten worden ingericht.</span><span class="sxs-lookup"><span data-stu-id="e314f-113">Although the Commerce evaluation environment itself has no geographical limitations, components of the environment, such as the Retail Cloud Scale Unit (RCSU) and e-Commerce applications, should be provisioned only in the United States.</span></span>
- <span data-ttu-id="e314f-114">De evaluatieomgeving van Commerce heeft een tijdslimiet van 30 dagen vanaf de datum waarop e-Commerce wordt ingericht.</span><span class="sxs-lookup"><span data-stu-id="e314f-114">Use of the Commerce evaluation environment is limited to 30 days from the date when e-Commerce is provisioned.</span></span>
- <span data-ttu-id="e314f-115">De evaluatieomgeving van Commerce kan alleen worden geïmplementeerd en geïnitialiseerd in een omgeving die gebruikmaakt van de demotopologie, waarbij alle onderdelen van een omgeving worden geïmplementeerd in één VM (virtuele machine) die in de cloud wordt gehost.</span><span class="sxs-lookup"><span data-stu-id="e314f-115">The Commerce evaluation environment can be successfully deployed and initialized only in an environment that uses the demo topology, where all components of an environment are deployed on a single cloud-hosted virtual machine (VM).</span></span> <span data-ttu-id="e314f-116">De belangrijkste beperking van deze topologie is het aantal gebruikers dat de omgeving gelijktijdig kan ondersteunen.</span><span class="sxs-lookup"><span data-stu-id="e314f-116">The main limitation of this topology is the number of concurrent users that the environment can support.</span></span>

## <a name="get-started"></a><span data-ttu-id="e314f-117">Aan de slag</span><span class="sxs-lookup"><span data-stu-id="e314f-117">Get started</span></span>

<span data-ttu-id="e314f-118">Zie [Een evaluatieomgeving van Commerce inrichten](provisioning-guide.md) om de evaluatieomgeving van Commerce in te richten.</span><span class="sxs-lookup"><span data-stu-id="e314f-118">To provision the Commerce evaluation environment, see [Provision a Commerce evaluation environment](provisioning-guide.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e314f-119">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="e314f-119">Additional resources</span></span>

[<span data-ttu-id="e314f-120">Een evaluatieomgeving voor Dynamics 365 Commerce inrichten</span><span class="sxs-lookup"><span data-stu-id="e314f-120">Provision a Dynamics 365 Commerce evaluation environment</span></span>](provisioning-guide.md)

[<span data-ttu-id="e314f-121">Een Dynamics 365 Commerce-evaluatieomgeving configureren</span><span class="sxs-lookup"><span data-stu-id="e314f-121">Configure a Dynamics 365 Commerce evaluation environment</span></span>](cpe-post-provisioning.md)

[<span data-ttu-id="e314f-122">BOPIS configureren in een Dynamics 365 Commerce-evaluatieomgeving</span><span class="sxs-lookup"><span data-stu-id="e314f-122">Configure BOPIS in a Dynamics 365 Commerce evaluation environment</span></span>](cpe-bopis.md)

[<span data-ttu-id="e314f-123">Optionele functies voor een Dynamics 365 Commerce-evaluatieomgeving configureren</span><span class="sxs-lookup"><span data-stu-id="e314f-123">Configure optional features for a Dynamics 365 Commerce evaluation environment</span></span>](cpe-optional-features.md)

[<span data-ttu-id="e314f-124">Veelgestelde vragen over evaluatieomgeving voor Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="e314f-124">Dynamics 365 Commerce evaluation environment FAQ</span></span>](cpe-faq.md)
