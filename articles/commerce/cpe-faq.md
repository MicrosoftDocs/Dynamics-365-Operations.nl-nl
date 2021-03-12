---
title: Veelgestelde vragen over evaluatieomgeving voor Dynamics 365 Commerce
description: Dit onderwerp biedt antwoorden op veelgestelde vragen over de evaluatieomgeving van Microsoft Dynamics 365 Commerce.
author: v-chgri
manager: annbe
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: v-chgri
ms.search.validFrom: 2019-12-10
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 6b8d7d7364087dacf3b4479ab008609ecffeaacb
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2021
ms.locfileid: "5000970"
---
# <a name="dynamics-365-commerce-evaluation-environment-faq"></a><span data-ttu-id="fb016-103">Veelgestelde vragen over evaluatieomgeving voor Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="fb016-103">Dynamics 365 Commerce evaluation environment FAQ</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="fb016-104">Dit onderwerp biedt antwoorden op veelgestelde vragen over de evaluatieomgeving van Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="fb016-104">This topic provides answers to frequently asked questions about the Microsoft Dynamics 365 Commerce evaluation environment.</span></span>

<span data-ttu-id="fb016-105">**Kunnen we de evaluatieomgeving van Commerce gebruiken als e-Commerce-winkel voor klanten die momenteel Retail implementeren?**</span><span class="sxs-lookup"><span data-stu-id="fb016-105">**Can we use the Commerce evaluation environment as an e-Commerce storefront for customers that currently implement Retail?**</span></span>

<span data-ttu-id="fb016-106">Nr.</span><span class="sxs-lookup"><span data-stu-id="fb016-106">No.</span></span> <span data-ttu-id="fb016-107">De Commerce-evaluatieomgeving is alleen bedoeld voor evaluatie.</span><span class="sxs-lookup"><span data-stu-id="fb016-107">The Commerce evaluation environment is only for evaluation.</span></span> <span data-ttu-id="fb016-108">Neem contact op met Microsoft als u een omgeving nodig hebt voor een klant die Retail implementeert.</span><span class="sxs-lookup"><span data-stu-id="fb016-108">If you require an environment for a customer that implements Retail, contact Microsoft.</span></span>

<span data-ttu-id="fb016-109">**Kan de evaluatieomgeving van Commerce worden gebruikt om de e-Commerce-functies in te richten boven op een bestaande toepassing/omgeving die Retail implementeert?**</span><span class="sxs-lookup"><span data-stu-id="fb016-109">**Can the Commerce evaluation environment be used to provision the e-Commerce features on top of an existing application/environment that implements Retail?**</span></span>

<span data-ttu-id="fb016-110">Nee (meestal).</span><span class="sxs-lookup"><span data-stu-id="fb016-110">No (mostly).</span></span> <span data-ttu-id="fb016-111">De onderdelen van Commerce-evaluatie zijn alleen beschikbaar voor omgevingen die overeenkomen met de configuraties die zijn opgegeven in de vereisten en inrichtingshandleiding.</span><span class="sxs-lookup"><span data-stu-id="fb016-111">The Commerce evaluation components are available only to environments that match the configurations that are specified in the prerequisites and provisioning guide.</span></span> <span data-ttu-id="fb016-112">Bovendien zijn de vereiste basisdemogegevens niet beschikbaar in omgevingen die zijn geïmplementeerd met een oorspronkelijke release die ouder is dan 10.0.8.</span><span class="sxs-lookup"><span data-stu-id="fb016-112">Additionally, the required base demo data won't be available in environments that were deployed with an initial release that is earlier than 10.0.8.</span></span> 

<span data-ttu-id="fb016-113">**Wat zijn de kosten van het implementeren van de evaluatieomgeving van Commerce op Microsoft Azure via Microsoft Dynamics Lifecycle Services (LCS)?**</span><span class="sxs-lookup"><span data-stu-id="fb016-113">**What costs are involved in deploying the Commerce evaluation environment on Microsoft Azure via Microsoft Dynamics Lifecycle Services (LCS)?**</span></span>

<span data-ttu-id="fb016-114">Een traditionele demo-omgeving voor Dynamics 365 Finance/Dynamics 365 Supply Chain Management/Dynamics 365 Commerce Headquarters (virtuele machine \[VM\]) wordt gehost in uw Azure-abonnement.</span><span class="sxs-lookup"><span data-stu-id="fb016-114">A traditional Dynamics 365 Finance/Dynamics 365 Supply Chain Management/Dynamics 365 Commerce headquarters demo environment (virtual machine \[VM\]) will be hosted in your Azure subscription.</span></span> <span data-ttu-id="fb016-115">U kunt de [Azure-prijscalculator](https://azure.microsoft.com/pricing/calculator/) gebruiken om deze kosten te schatten.</span><span class="sxs-lookup"><span data-stu-id="fb016-115">You can use the [Azure pricing calculator](https://azure.microsoft.com/pricing/calculator/) to estimate this cost.</span></span>

<span data-ttu-id="fb016-116">Andere onderdelen, zoals Commerce Scale Unit, Commerce Site Builder en uw e-commerce-site zijn beschikbaar als software als een dienst (SaaS) en worden door Microsoft gehost.</span><span class="sxs-lookup"><span data-stu-id="fb016-116">Other components such as Commerce Scale Unit, Commerce site builder, and your e-Commerce site will be available as software as a service (SaaS) and hosted by Microsoft.</span></span>

<span data-ttu-id="fb016-117">**Welke Azure-regio's worden momenteel ondersteund voor de evaluatieomgeving van Commerce?**</span><span class="sxs-lookup"><span data-stu-id="fb016-117">**Which Azure geographies are currently supported for the Commerce evaluation environment?**</span></span>

<span data-ttu-id="fb016-118">De evaluatieomgeving van Commerce kan alleen worden geïmplementeerd in de regio Noord-Amerika.</span><span class="sxs-lookup"><span data-stu-id="fb016-118">The Commerce evaluation environment can be deployed only in the North America geography.</span></span>

<span data-ttu-id="fb016-119">**Is er een downloadbare virtuele harde schijf (VHD) met de volledige OneBox VM-optie (virtuele machine)?**</span><span class="sxs-lookup"><span data-stu-id="fb016-119">**Is there a downloadable virtual hard disk (VHD) that has the complete OneBox virtual machine (VM) option?**</span></span>

<span data-ttu-id="fb016-120">Dynamics 365 Commerce en Commerce Scale Unit zijn volledig SaaS en moeten in de cloud worden gehost.</span><span class="sxs-lookup"><span data-stu-id="fb016-120">Dynamics 365 Commerce and Commerce Scale Unit are completely software as a service (SaaS) and must be cloud-hosted.</span></span>

<span data-ttu-id="fb016-121">**Hoe lang kan de evaluatieomgeving van Commerce worden gebruikt?**</span><span class="sxs-lookup"><span data-stu-id="fb016-121">**How long can the Commerce evaluation environment be used?**</span></span>

<span data-ttu-id="fb016-122">De Commerce-evaluatieomgeving heeft een tijdslimiet van 30 dagen na de datum waarop SaaS-componenten, zoals Commerce Scale Unit, Commerce Site Builder en uw e-commerce-site zijn ingericht.</span><span class="sxs-lookup"><span data-stu-id="fb016-122">The Commerce evaluation environment has a 30-day time limit from the date when SaaS components such as Commerce Scale Unit, Commerce site builder, and your e-Commerce site are provisioned.</span></span>

<span data-ttu-id="fb016-123">**Kan ik de tijdslimiet voor mijn evaluatieomgeving van Commerce verlengen?**</span><span class="sxs-lookup"><span data-stu-id="fb016-123">**Can I extend the time limit for my Commerce evaluation environment?**</span></span>

<span data-ttu-id="fb016-124">Verlenging van de tijds limiet wordt bij uitzondering verleend en wordt per geval beschouwd.</span><span class="sxs-lookup"><span data-stu-id="fb016-124">Extension of the time limit is an exception to the norm and is considered on a case-by-case basis.</span></span> <span data-ttu-id="fb016-125">Neem contact op met uw Microsoft-partner voor hulp.</span><span class="sxs-lookup"><span data-stu-id="fb016-125">You should reach out to your Microsoft partner contact for assistance.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="fb016-126">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="fb016-126">Additional resources</span></span>

[<span data-ttu-id="fb016-127">Overzicht van de evaluatieomgeving voor Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="fb016-127">Dynamics 365 Commerce evaluation environment overview</span></span>](cpe-overview.md)

[<span data-ttu-id="fb016-128">Een evaluatieomgeving voor Dynamics 365 Commerce inrichten</span><span class="sxs-lookup"><span data-stu-id="fb016-128">Provision a Dynamics 365 Commerce evaluation environment</span></span>](provisioning-guide.md)

[<span data-ttu-id="fb016-129">Een Dynamics 365 Commerce-evaluatieomgeving configureren</span><span class="sxs-lookup"><span data-stu-id="fb016-129">Configure a Dynamics 365 Commerce evaluation environment</span></span>](cpe-post-provisioning.md)

[<span data-ttu-id="fb016-130">BOPIS configureren in een Dynamics 365 Commerce-evaluatieomgeving</span><span class="sxs-lookup"><span data-stu-id="fb016-130">Configure BOPIS in a Dynamics 365 Commerce evaluation environment</span></span>](cpe-bopis.md)

[<span data-ttu-id="fb016-131">Optionele functies voor een Dynamics 365 Commerce-evaluatieomgeving configureren</span><span class="sxs-lookup"><span data-stu-id="fb016-131">Configure optional features for a Dynamics 365 Commerce evaluation environment</span></span>](cpe-optional-features.md)
