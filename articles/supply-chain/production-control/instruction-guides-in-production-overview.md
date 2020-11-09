---
title: Productiemedewerkers voorzien van mixed reality-guides
description: In dit onderwerp wordt uitgelegd hoe u de productiebeheermodule in Microsoft Dynamics 365 Supply Chain Management integreert met Dynamics 365 Guides.
author: cabeln
manager: tfehr
ms.date: 09/29/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WorkGuidesManufacturing
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 61943
ms.assetid: a3847f07-fca4-4140-a26f-d83c6ac68dde
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: cabeln
ms.search.validFrom: 2020-08-01
ms.dyn365.ops.version: AX 10.0.15
ms.openlocfilehash: 14645f592275d07a6b633146bb6da35b89c1bf77
ms.sourcegitcommit: 6d2fc497c8a7f49c48e7662995e27b5f8cc10296
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/14/2020
ms.locfileid: "4000973"
---
# <a name="provide-mixed-reality-guides-for-workers-in-production"></a><span data-ttu-id="f641a-103">Productiemedewerkers voorzien van mixed reality-guides</span><span class="sxs-lookup"><span data-stu-id="f641a-103">Provide mixed-reality Guides for workers in production</span></span>

<span data-ttu-id="f641a-104">Medewerkers in productieprocessen zullen gebruikmaken van relevante instructies die op het juiste moment in het context van hun werk worden geleverd.</span><span class="sxs-lookup"><span data-stu-id="f641a-104">Workers in production processes will benefit from relevant instructions that are provided at the right time in the context of their work.</span></span> <span data-ttu-id="f641a-105">*Instructies* zijn van toepassing op verschillende domeinen van werkzaamheden, waaronder: assemblage, service, bewerkingen, certificering en veiligheid.</span><span class="sxs-lookup"><span data-stu-id="f641a-105">*Instructions* apply in several domains of work, including: assembly, service, operations, certification, and safety.</span></span> <span data-ttu-id="f641a-106">In al deze belangrijke bedrijfsfuncties kunnen doorlopende trainingsinstructies worden gebruikt om medewerkers te helpen meer te bereiken en beter te werken.</span><span class="sxs-lookup"><span data-stu-id="f641a-106">Across all of these core business functions, ongoing training instructions can help empower workers to achieve more and work better.</span></span>

## <a name="introduction"></a><span data-ttu-id="f641a-107">Inleiding</span><span class="sxs-lookup"><span data-stu-id="f641a-107">Introduction</span></span>

<span data-ttu-id="f641a-108">U kunt instructies op verschillende manieren verstrekken.</span><span class="sxs-lookup"><span data-stu-id="f641a-108">You can provide instructions in different ways.</span></span> <span data-ttu-id="f641a-109">Eén efficiënt systeem dat kant en klaar wordt geleverd maakt gebruik van [Dynamics 365 Guides](https://dynamics.microsoft.com/mixed-reality/guides/).</span><span class="sxs-lookup"><span data-stu-id="f641a-109">One efficient system that ships out of the box uses [Dynamics 365 Guides](https://dynamics.microsoft.com/mixed-reality/guides/).</span></span>

<span data-ttu-id="f641a-110">Dynamics 365 Guides kan u helpen uw medewerkers beter te leren werken via praktijktraining.</span><span class="sxs-lookup"><span data-stu-id="f641a-110">Dynamics 365 Guides can help empower your employees with hands-on learning.</span></span> <span data-ttu-id="f641a-111">U kunt gestandaardiseerde processen definiëren met stapsgewijze instructies in de vorm van guides die uw medewerkers begeleiden bij het werken met de gereedschappen en onderdelen die ze nodig hebben en die medewerkers laten zien hoe ze deze gereedschappen moeten gebruiken in concrete werksituaties.</span><span class="sxs-lookup"><span data-stu-id="f641a-111">You can define standardized processes with step-by-step instructions that guide your employees to the tools and parts they need and show employees how to use these tools in real work situations.</span></span>

<span data-ttu-id="f641a-112">U kunt guides koppelen aan verschillende aspecten van productiebeheer, waaronder:</span><span class="sxs-lookup"><span data-stu-id="f641a-112">You can attach guides to various aspects of production control including:</span></span>

- [<span data-ttu-id="f641a-113">Bronnen</span><span class="sxs-lookup"><span data-stu-id="f641a-113">Resources</span></span>](#resources)
- [<span data-ttu-id="f641a-114">Resourcegroepen</span><span class="sxs-lookup"><span data-stu-id="f641a-114">Resource groups</span></span>](#resource-groups)
- [<span data-ttu-id="f641a-115">Vrijgegeven producten</span><span class="sxs-lookup"><span data-stu-id="f641a-115">Released products</span></span>](#released-products)
- [<span data-ttu-id="f641a-116">Formules</span><span class="sxs-lookup"><span data-stu-id="f641a-116">Formulas</span></span>](#formulas)
- [<span data-ttu-id="f641a-117">Formuleversies</span><span class="sxs-lookup"><span data-stu-id="f641a-117">Formula versions</span></span>](#formula-versions)
- [<span data-ttu-id="f641a-118">Stuklijsten</span><span class="sxs-lookup"><span data-stu-id="f641a-118">Bills of material (BOMs)</span></span>](#bom)
- [<span data-ttu-id="f641a-119">Stuklijstversies</span><span class="sxs-lookup"><span data-stu-id="f641a-119">BOM versions</span></span>](#bom-versions)
- [<span data-ttu-id="f641a-120">Routes</span><span class="sxs-lookup"><span data-stu-id="f641a-120">Routes</span></span>](#routes)
- [<span data-ttu-id="f641a-121">Routeversies</span><span class="sxs-lookup"><span data-stu-id="f641a-121">Route versions</span></span>](#route-versions)
- [<span data-ttu-id="f641a-122">Routebewerkingsrelaties</span><span class="sxs-lookup"><span data-stu-id="f641a-122">Route operation relations</span></span>](#route-operation-relations)

> [!NOTE]
> <span data-ttu-id="f641a-123">U kunt ook guides aan activabeheer koppelen.</span><span class="sxs-lookup"><span data-stu-id="f641a-123">You can also attach Guides with Asset Management.</span></span> <span data-ttu-id="f641a-124">Zie [Dynamics 365 Supply Chain Management (Activabeheer) integreren met Dynamics 365 Guides](../asset-management/asset-management-guides-integration.md) voor meer informatie over die optie.</span><span class="sxs-lookup"><span data-stu-id="f641a-124">For more information about that option, see [Integrate Dynamics 365 Supply Chain Management (Asset Management) with Dynamics 365 Guides](../asset-management/asset-management-guides-integration.md).</span></span>

<span data-ttu-id="f641a-125">Wanneer een eerstelijnsmedewerker een taak kiest voor de werkvloer via Supply Chain Management, kan de medewerker [de relevante guides](#logic) op de taakkaart zien.</span><span class="sxs-lookup"><span data-stu-id="f641a-125">When a first-line worker chooses a job on the shop floor through Supply Chain Management, the worker can see [the relevant guides](#logic) on the job card.</span></span> <span data-ttu-id="f641a-126">Wanneer de medewerker een specifieke guide kiest, wordt op het scherm een QR-code voor die guide weergegeven.</span><span class="sxs-lookup"><span data-stu-id="f641a-126">When the worker chooses a specific guide, a QR code for that guide is shown on the screen.</span></span> <span data-ttu-id="f641a-127">De medewerker gebruikt vervolgens de eigen HoloLens om de QR-code te scannen, waarmee guides worden gestart en de vereiste instructies worden weergegeven.</span><span class="sxs-lookup"><span data-stu-id="f641a-127">The worker then uses their HoloLens to scan the QR code, which launches Guides and shows the required instructions.</span></span>

<span data-ttu-id="f641a-128">In de volgende subsecties wordt een aantal geselecteerde scenario's beschreven waarbij bedrijven in verschillende bedrijfstakken de grootste toegevoegde waarde kunnen leveren bij het gebruik van guides voor het presenteren van instructies voor de productie.</span><span class="sxs-lookup"><span data-stu-id="f641a-128">The following subsections describe a few selected scenarios where companies across industries can see the biggest value when using Guides to present instructions for manufacturing.</span></span>

### <a name="assembly"></a><span data-ttu-id="f641a-129">Assembly</span><span class="sxs-lookup"><span data-stu-id="f641a-129">Assembly</span></span>

<span data-ttu-id="f641a-130">![Guides gebruiken in assemblagetaken](media/instruction-guides-hero-assembly.png "Guides gebruiken in servicetaken")</span><span class="sxs-lookup"><span data-stu-id="f641a-130">![Use Guides in assembly tasks](media/instruction-guides-hero-assembly.png "Use Guides in service tasks")</span></span>

<span data-ttu-id="f641a-131">Guides voor assemblagebewerkingen tonen medewerkers de benodigde gereedschappen en onderdelen en geven aan hoe ze deze in concrete werksituaties moeten gebruiken.</span><span class="sxs-lookup"><span data-stu-id="f641a-131">Instructions in assembly operations show workers the tools and parts they need and how to use them in real work situations.</span></span>

<span data-ttu-id="f641a-132">Productiemanagers kunnen guides maken en toewijzen, bijvoorbeeld voor [productieroutes](routes-operations.md), [bewerkingsrelaties](routes-operations.md#operation-relations) of [stuklijsten](bill-of-material-bom.md).</span><span class="sxs-lookup"><span data-stu-id="f641a-132">Production managers can create and assign Guides, for example, for [production routes](routes-operations.md), [operation relations](routes-operations.md#operation-relations), or [bills of material](bill-of-material-bom.md).</span></span> <span data-ttu-id="f641a-133">Medewerkers vinden hier de relevante instructies voor de bewerkingservaring op de werkvloer.</span><span class="sxs-lookup"><span data-stu-id="f641a-133">Workers will find the relevant instructions on the respective operation experience on the shop floor.</span></span>

### <a name="service"></a><span data-ttu-id="f641a-134">Service</span><span class="sxs-lookup"><span data-stu-id="f641a-134">Service</span></span>

<span data-ttu-id="f641a-135">![Guides gebruiken in servicetaken](media/instruction-guides-hero-service.png "Guides gebruiken in servicetaken")</span><span class="sxs-lookup"><span data-stu-id="f641a-135">![Use Guides in service tasks](media/instruction-guides-hero-service.png "Use Guides in service tasks")</span></span>

<span data-ttu-id="f641a-136">Voorzie technici van begeleide instructies op de werkplek, zodat er geen extra bezoeken hoeven te worden gepland.</span><span class="sxs-lookup"><span data-stu-id="f641a-136">Equip technicians with guided instructions at the job site, eliminating the need to schedule additional visits.</span></span>

<span data-ttu-id="f641a-137">Servicemanagers kunnen bijvoorbeeld guides toewijzen aan specifieke [producten](../../commerce/product.md) die de kwaliteitscontrole-routines doorlopen.</span><span class="sxs-lookup"><span data-stu-id="f641a-137">Service managers can assign Guides, for example, to specific [products](../../commerce/product.md) that walk through routines of quality assessment.</span></span>

### <a name="quality"></a><span data-ttu-id="f641a-138">Kwaliteit</span><span class="sxs-lookup"><span data-stu-id="f641a-138">Quality</span></span>

<span data-ttu-id="f641a-139">![Guides gebruiken in kwaliteitscontroletaken](media/instruction-guides-hero-quality.png "Guides gebruiken in kwaliteitscontroletaken")</span><span class="sxs-lookup"><span data-stu-id="f641a-139">![Use Guides in quality assurance tasks](media/instruction-guides-hero-quality.png "Use Guides in quality assurance tasks")</span></span>

<span data-ttu-id="f641a-140">Implementeer nieuwe processen en zorg voor een betere consistentie door de kennis van medewerkers in een herhaalbaar hulpmiddel te veranderen.</span><span class="sxs-lookup"><span data-stu-id="f641a-140">Rollout new processes and ensure increased consistency by turning employee knowledge into a repeatable tool.</span></span>

<span data-ttu-id="f641a-141">Managers voor kwaliteitscontrole kunnen bijvoorbeeld guides toewijzen aan specifieke [producten](../../commerce/product.md) die de routines van de kwaliteitscontrole doorlopen.</span><span class="sxs-lookup"><span data-stu-id="f641a-141">Quality assurance managers can assign guides, for example, to [products](../../commerce/product.md) that walk through routines of quality assessment.</span></span>

### <a name="certifications"></a><span data-ttu-id="f641a-142">Certificaten</span><span class="sxs-lookup"><span data-stu-id="f641a-142">Certifications</span></span>

<span data-ttu-id="f641a-143">![Guides gebruiken voor aan certificering gerelateerde taken](media/instruction-guides-hero-certification.png "Guides gebruiken voor aan certificering gerelateerde taken")</span><span class="sxs-lookup"><span data-stu-id="f641a-143">![Use Guides for certification related tasks](media/instruction-guides-hero-certification.png "Use Guides for certification related tasks")</span></span>

<span data-ttu-id="f641a-144">Zorg ervoor dat elke medewerker aan hoge normen voldoet door snel te identificeren wie hulp nodig heeft en waar.</span><span class="sxs-lookup"><span data-stu-id="f641a-144">Ensure every employee meets high standards by quickly identifying who needs help and where.</span></span>

### <a name="safety"></a><span data-ttu-id="f641a-145">Veiligheid</span><span class="sxs-lookup"><span data-stu-id="f641a-145">Safety</span></span>

<span data-ttu-id="f641a-146">![Guides gebruiken in instructies voor veilig werken](media/instruction-guides-hero-safety.png "Guides gebruiken in instructies voor veilig werken")</span><span class="sxs-lookup"><span data-stu-id="f641a-146">![Use Guides in work safety instructions](media/instruction-guides-hero-safety.png "Use Guides in work safety instructions")</span></span>

<span data-ttu-id="f641a-147">Verstrek instructies die gevaarlijke procedures doorlopen, vrijwel voordat u deze probeert in de fysieke omgeving.</span><span class="sxs-lookup"><span data-stu-id="f641a-147">Provide instructions that walk through dangerous procedures virtually before attempting in the physical environment.</span></span> <span data-ttu-id="f641a-148">Met een methode met mixed reality kunnen medewerkers virtueel gevaarlijke procedures uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="f641a-148">With a mixed reality approach, workers can experience dangerous procedures virtually.</span></span>

<span data-ttu-id="f641a-149">Productiemanagers kunnen speciale verwerkingsinstructies bieden voor werken met gevaarlijke materiaal of delicate-afhandelingsprocedures door instructies toe te wijzen aan [productartikelen](../../commerce/product.md), [routes](routes-operations.md) en [bewerkingen](routes-operations.md#operation-relations).</span><span class="sxs-lookup"><span data-stu-id="f641a-149">Production managers can provide dedicated handling instructions for hazardous material handling or delicate handling procedures by assigning instructions to [product items](../../commerce/product.md), [routes](routes-operations.md), and [operations](routes-operations.md#operation-relations).</span></span>

## <a name="get-started-with-instructions-and-guides"></a><span data-ttu-id="f641a-150">Aan de slag met instructies en Guides</span><span class="sxs-lookup"><span data-stu-id="f641a-150">Get started with instructions and Guides</span></span>

<span data-ttu-id="f641a-151">Om instructies in productieprocessen in te schakelen, biedt Supply Chain Management een kant en klare integratie met Dynamics 365 Guides.</span><span class="sxs-lookup"><span data-stu-id="f641a-151">To enable instructions in production processes, Supply Chain Management provides an out-of-the-box integration with Dynamics 365 Guides.</span></span> <span data-ttu-id="f641a-152">Een gelicentieerd en geïnstalleerd toepassingsexemplaar van Guides is vereist voor het maken, onderhouden en toewijzen van instructies met mixed reality voor productieactiva en werk.</span><span class="sxs-lookup"><span data-stu-id="f641a-152">A licensed and installed application instance of Guides is required to build, maintain, and assign mixed reality instructions to production assets and work.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="f641a-153">Vereisten</span><span class="sxs-lookup"><span data-stu-id="f641a-153">Prerequisites</span></span>

<span data-ttu-id="f641a-154">Als u deze functie wilt gebruiken, moet uw systeem het volgende bevatten:</span><span class="sxs-lookup"><span data-stu-id="f641a-154">To use this feature, your system must include the following:</span></span>

- <span data-ttu-id="f641a-155">Dynamics 365 Supply Chain Management versie 10.0.15 of hoger</span><span class="sxs-lookup"><span data-stu-id="f641a-155">Dynamics 365 Supply Chain Management version 10.0.15 or later</span></span>
- <span data-ttu-id="f641a-156">[Twee keer wegschrijven](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/enable-dual-write) voor Supply Chain Management-apps.</span><span class="sxs-lookup"><span data-stu-id="f641a-156">[Dual-write](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/enable-dual-write) for Supply Chain Management apps.</span></span>
- <span data-ttu-id="f641a-157">[Dynamics 365 Guides](https://docs.microsoft.com/dynamics365/mixed-reality/guides/setup#step-2-create-a-common-data-service-environment-and-install-the-dynamics-365-guides-solution) versie 400.0.1.48 of hoger</span><span class="sxs-lookup"><span data-stu-id="f641a-157">[Dynamics 365 Guides](https://docs.microsoft.com/dynamics365/mixed-reality/guides/setup#step-2-create-a-common-data-service-environment-and-install-the-dynamics-365-guides-solution) version 400.0.1.48 or later</span></span>

### <a name="turn-on-the-feature"></a><span data-ttu-id="f641a-158">De functie inschakelen</span><span class="sxs-lookup"><span data-stu-id="f641a-158">Turn on the feature</span></span>

<span data-ttu-id="f641a-159">Als u de functie beschikbaar wilt maken op uw systeem, moet u de bijbehorende configuratiesleutels inschakelen.</span><span class="sxs-lookup"><span data-stu-id="f641a-159">To make the feature available on your system, you must enable its configuration keys.</span></span> <span data-ttu-id="f641a-160">U hoeft dit maar één keer te doen.</span><span class="sxs-lookup"><span data-stu-id="f641a-160">You only need to do this once.</span></span> <span data-ttu-id="f641a-161">Hiertoe moet een beheerder het volgende doen:</span><span class="sxs-lookup"><span data-stu-id="f641a-161">To do this, an administrator must do the following:</span></span>

1. <span data-ttu-id="f641a-162">Plaats het systeem in de onderhoudsmodus, zoals wordt beschreven in [Onderhoudsmodus](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).</span><span class="sxs-lookup"><span data-stu-id="f641a-162">Place your system into maintenance mode as described in [Maintenance mode](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).</span></span>
1. <span data-ttu-id="f641a-163">Ga naar **Systeembeheer \> Instellingen \> Licentieconfiguratie**.</span><span class="sxs-lookup"><span data-stu-id="f641a-163">Go to **System administration \> Setup \> License configuration**.</span></span>
1. <span data-ttu-id="f641a-164">Vouw de sectie **Mixed reality** uit en schakel vervolgens het selectievakje **Mixed reality-guide** in.</span><span class="sxs-lookup"><span data-stu-id="f641a-164">Expand the **Mixed reality** section and then select the **Mixed reality guide** check box.</span></span>
1. <span data-ttu-id="f641a-165">Vouw de sectie **Productiebeheer** uit en schakel vervolgens het selectievakje **Productie-instructies** in.</span><span class="sxs-lookup"><span data-stu-id="f641a-165">Expand the **Production management** section and then select the **Production instructions** check box.</span></span>
1. <span data-ttu-id="f641a-166">Schakel de onderhoudsmodus uit, zoals wordt beschreven in [Onderhoudsmodus](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).</span><span class="sxs-lookup"><span data-stu-id="f641a-166">Turn off maintenance mode as described in [Maintenance mode](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).</span></span>
  
## <a name="configure-how-guides-appear-on-the-shop-floor"></a><span data-ttu-id="f641a-167">Configureren hoe guides op de werkvloer worden weergegeven</span><span class="sxs-lookup"><span data-stu-id="f641a-167">Configure how Guides appear on the shop floor</span></span>

<span data-ttu-id="f641a-168">Als u wilt configureren hoe guides worden weergegeven op de werkvloer, gaat u naar **Mixed reality \> Dynamics 365 Guides \> Integratie van Guides configureren**.</span><span class="sxs-lookup"><span data-stu-id="f641a-168">To configure how Guides appear on the shop floor, go to **Mixed Reality \> Dynamics 365 Guides \> Configure Guides integration**.</span></span>

<span data-ttu-id="f641a-169">![Integratie van guides configureren voor productie](media/instruction-guides-configure-integration.png "Integratie van guides configureren voor productie")</span><span class="sxs-lookup"><span data-stu-id="f641a-169">![Configure Guide integration for manufacturing](media/instruction-guides-configure-integration.png "Configure Guide integration for manufacturing")</span></span>

<span data-ttu-id="f641a-170">Stel de volgende velden in:</span><span class="sxs-lookup"><span data-stu-id="f641a-170">Set the following fields:</span></span>

- <span data-ttu-id="f641a-171">Subdomein van **Common Data Service** : dit veld moet al een waarde bevatten.</span><span class="sxs-lookup"><span data-stu-id="f641a-171">**Common Data Service subdomain** - This field should already show a value.</span></span> <span data-ttu-id="f641a-172">Dit veld bevat het subdomein voor de Common Data Service-omgeving waarin u uw guides maakt.</span><span class="sxs-lookup"><span data-stu-id="f641a-172">This field holds the subdomain for the Common Data Service environment where you create your Guides.</span></span> <span data-ttu-id="f641a-173">Het subdomein is het eerste deel van de URL en heeft meestal de naam van uw organisatie.</span><span class="sxs-lookup"><span data-stu-id="f641a-173">The subdomain is the first part of the URL and is typically named after your organization.</span></span> <span data-ttu-id="f641a-174">Als uw Common Data Service-URL bijvoorbeeld 'contoso.crm4.dynamics.com' is, moet u hier *contoso* invoeren.</span><span class="sxs-lookup"><span data-stu-id="f641a-174">For example, if your Common Data Service URL is "contoso.crm4.dynamics.com", you should enter *contoso* here.</span></span> <span data-ttu-id="f641a-175">Deze waarde wordt gebruikt om adressen voor uw guides samen te stellen en wordt gecodeerd in de QR-codes.</span><span class="sxs-lookup"><span data-stu-id="f641a-175">This value is used to compose addresses for your guides and will be encoded into the QR codes.</span></span>
- <span data-ttu-id="f641a-176">**Grootte van QR-code** : stel de grootte van de gegenereerde QR-code in.</span><span class="sxs-lookup"><span data-stu-id="f641a-176">**QR code size** - Set the size of the rendered QR code.</span></span> <span data-ttu-id="f641a-177">Het is raadzaam om een grootte te kiezen waarbij uw beeldscherm grotendeels gevuld is, maar niet meer.</span><span class="sxs-lookup"><span data-stu-id="f641a-177">We recommend choosing a size that will fill most of your display screen, but not more.</span></span> <span data-ttu-id="f641a-178">Meestal is *15* een goede waarde.</span><span class="sxs-lookup"><span data-stu-id="f641a-178">Typically, *15* is a good value.</span></span>
- <span data-ttu-id="f641a-179">**Foutcorrectieniveau QR-code** : stel de gedetailleerdheid van de QR-code in.</span><span class="sxs-lookup"><span data-stu-id="f641a-179">**QR code error correction level** - Set the granularity of the QR code.</span></span> <span data-ttu-id="f641a-180">Een hogere mate van gedetailleerdheid kan de betrouwbaarheid van de code helpen verhogen, maar uw **grootte van de QR-code** moet groot genoeg zijn om het detailniveau voor uw geselecteerde correctieniveau te ondersteunen.</span><span class="sxs-lookup"><span data-stu-id="f641a-180">Higher granularity can help increase the code's reliability, but your **QR code size** must be large enough to support the level of detail required by your selected correction level.</span></span>


> [!TIP]
> - <span data-ttu-id="f641a-181">Het weergeven van QR-codes die te groot zijn voor uw beeldscherm duurt iets langer en de QR-codes worden vervolgens aangepast aan uw beeldscherm.</span><span class="sxs-lookup"><span data-stu-id="f641a-181">QR codes sizes that are too large for your display will take a bit longer to render and then be scaled down to fit your display.</span></span> <span data-ttu-id="f641a-182">Deze bieden geen voordeel.</span><span class="sxs-lookup"><span data-stu-id="f641a-182">These do not provide a benefit.</span></span>
> - <span data-ttu-id="f641a-183">QR-codes die te klein zijn, kunnen de mogelijkheid van HoloLens verminderen om de code goed te lezen in bepaalde omgevingen.</span><span class="sxs-lookup"><span data-stu-id="f641a-183">QR code sizes that are too small may decrease the ability of HoloLens to read the code properly in some environments.</span></span>
> - <span data-ttu-id="f641a-184">Het is raadzaam om de instellingen te testen voor elk apparaat waarin QR-codes voor HoloLens-gebruikers worden weergegeven.</span><span class="sxs-lookup"><span data-stu-id="f641a-184">We recommend that you test the settings for each device that will display QR codes for HoloLens users.</span></span> <span data-ttu-id="f641a-185">Kies instellingen die voldoende leesbaarheid bieden in uw werkvloeromgeving.</span><span class="sxs-lookup"><span data-stu-id="f641a-185">Choose settings that provide sufficient readability in your shop floor environment.</span></span>  

## <a name="get-an-overview-of-all-guide-assignments"></a><span data-ttu-id="f641a-186">Een overzicht weergeven van alle toewijzingen van guides</span><span class="sxs-lookup"><span data-stu-id="f641a-186">Get an overview of all Guide assignments</span></span>

<span data-ttu-id="f641a-187">Gebruik de pagina **Alle guides** om de lijst met alle beschikbare guides in uw organisatie en alle toewijzingen aan productieprocessen en resources weer te geven.</span><span class="sxs-lookup"><span data-stu-id="f641a-187">Use the **All Guides** page to see the list of all available Guides in your organization and all assignments to your production processes and resources.</span></span> <span data-ttu-id="f641a-188">Ga naar **Mixed reality \> Guides \> Alle guides** om deze te openen.</span><span class="sxs-lookup"><span data-stu-id="f641a-188">To open it, go to **Mixed reality \> Guides \> All Guides**.</span></span> <span data-ttu-id="f641a-189">In de lijst boven worden alle beschikbare guides weergegeven en kunt u het veld hier gebruiken om de lijst te filteren.</span><span class="sxs-lookup"><span data-stu-id="f641a-189">The list at the top shows all the available Guides and you can use the field here to filter the list.</span></span> <span data-ttu-id="f641a-190">In de lijst onderaan ziet u alle toewijzingen van guides en een werkbalk voor het beheren hiervan.</span><span class="sxs-lookup"><span data-stu-id="f641a-190">The list at the bottom shows all Guide assignments and provides a toolbar for managing them.</span></span>

<span data-ttu-id="f641a-191">![Guides beheren](media/instruction-guides-allguides.png "Guides beheren")</span><span class="sxs-lookup"><span data-stu-id="f641a-191">![Manage Guides](media/instruction-guides-allguides.png "Manage Guides")</span></span>

<span data-ttu-id="f641a-192">In de volgende secties worden de typen objecten beschreven waaraan u guides kunt toewijzen.</span><span class="sxs-lookup"><span data-stu-id="f641a-192">The following sections describe the types of objects that you can assign Guides to.</span></span> <span data-ttu-id="f641a-193">Elke toegewezen guide bevat instructies die automatisch worden gekoppeld aan de respectieve productietaken en die beschikbaar zijn op de werkvloer.</span><span class="sxs-lookup"><span data-stu-id="f641a-193">Each assigned guide provides instructions that are automatically attached to the respective production jobs and will be available on the shop floor.</span></span>

## <a name="associate-a-guide-to-a-resource"></a><a name="resources"></a><span data-ttu-id="f641a-194">Een guide aan een resource koppelen</span><span class="sxs-lookup"><span data-stu-id="f641a-194">Associate a Guide to a resource</span></span>

<span data-ttu-id="f641a-195">Voeg een guide toe aan een [resource](operations-resources.md) om de guide aan te bieden in de context van relevante productietaken.</span><span class="sxs-lookup"><span data-stu-id="f641a-195">Add a Guide to a [resource](operations-resources.md) to offer the Guide in the context of relevant production jobs.</span></span>

### <a name="typical-scenario-using-resources"></a><span data-ttu-id="f641a-196">Standaardscenario met resources</span><span class="sxs-lookup"><span data-stu-id="f641a-196">Typical scenario using resources</span></span>

<span data-ttu-id="f641a-197">U kunt bijvoorbeeld een guide koppelen aan algemene machinebeveiligings- of verwerkingsinstructies voor een resource van het type machine.</span><span class="sxs-lookup"><span data-stu-id="f641a-197">For example, you could attach a Guide with general machine security or handling instructions to a resource of type machine.</span></span> <span data-ttu-id="f641a-198">Vervolgens is de guide beschikbaar voor alle taken die op de computer worden uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="f641a-198">Then, the Guide will be available on every job that is performed on the machine.</span></span>

### <a name="add-a-guide-to-a-resource"></a><span data-ttu-id="f641a-199">Een guide toevoegen aan een resource</span><span class="sxs-lookup"><span data-stu-id="f641a-199">Add a Guide to a resource</span></span>

<span data-ttu-id="f641a-200">Voeg als volgt een guide toe aan een resource:</span><span class="sxs-lookup"><span data-stu-id="f641a-200">To add a Guide to a resource:</span></span>

1. <span data-ttu-id="f641a-201">Ga naar **Productiebeheer \> Instellen \> Resources \> Resources**.</span><span class="sxs-lookup"><span data-stu-id="f641a-201">Go to **Production control \> Setup \> Resources \> Resources**.</span></span>
1. <span data-ttu-id="f641a-202">Selecteer in het lijstvenster de resource waaraan u een guide wilt toewijzen.</span><span class="sxs-lookup"><span data-stu-id="f641a-202">From the list pane, select the resource you want to assign a Guide to.</span></span>
1. <span data-ttu-id="f641a-203">Vouw het sneltabblad **Gekoppelde guides** uit.</span><span class="sxs-lookup"><span data-stu-id="f641a-203">Expand the **Associated Guides** FastTab.</span></span>
1. <span data-ttu-id="f641a-204">Selecteer **Toevoegen** op de werkbalk **Gekoppelde guides**.</span><span class="sxs-lookup"><span data-stu-id="f641a-204">Select **Add** from the **Associated Guides** toolbar.</span></span> <span data-ttu-id="f641a-205">Er wordt een nieuwe regel aan het raster toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="f641a-205">A new line is added to the grid.</span></span>
1. <span data-ttu-id="f641a-206">Voor de nieuwe regel gebruikt u de vervolgkeuzelijst in de kolom **Naam** om de guide te kiezen die u wilt toewijzen.</span><span class="sxs-lookup"><span data-stu-id="f641a-206">For the new line, use the drop-down list in the **Name** column to choose the Guide you want to assign.</span></span> <span data-ttu-id="f641a-207">Als u een groot aantal guides hebt, kunt u de lijst filteren om de gewenste te zoeken.</span><span class="sxs-lookup"><span data-stu-id="f641a-207">If you have a large number of Guides, then you can filter the list to find the one you are looking for.</span></span>
    <span data-ttu-id="f641a-208">![Guides beheren](media/instruction-guides-allguides.png "Guides beheren")</span><span class="sxs-lookup"><span data-stu-id="f641a-208">![Manage Guides](media/instruction-guides-allguides.png "Manage Guides")</span></span>

## <a name="associate-a-guide-to-a-resource-group"></a><a name="resource-groups"></a><span data-ttu-id="f641a-209">Een guide aan een resourcegroep koppelen</span><span class="sxs-lookup"><span data-stu-id="f641a-209">Associate a Guide to a resource group</span></span>

<span data-ttu-id="f641a-210">U kunt een guide aan [resourcegroepen](tasks/define-discrete-manufacturing-resource-group.md) toevoegen als u deze gebruikt om groepen machines, productielijnen of werkcellen te beheren.</span><span class="sxs-lookup"><span data-stu-id="f641a-210">You can add a guide to [resource groups](tasks/define-discrete-manufacturing-resource-group.md) if you use them to manage groups of machines, production lines, or work cells.</span></span>

### <a name="typical-scenarios-using-resource-groups"></a><span data-ttu-id="f641a-211">Standaardscenario's met resourcegroepen</span><span class="sxs-lookup"><span data-stu-id="f641a-211">Typical scenarios using resource groups</span></span>

<span data-ttu-id="f641a-212">**Voorbeeld 1:** u hebt een resourcegroep gedefinieerd voor meerdere machines van hetzelfde model.</span><span class="sxs-lookup"><span data-stu-id="f641a-212">**Example 1:** You have defined a resource group for several machines of the same model.</span></span> <span data-ttu-id="f641a-213">In plaats van de relevante guide met verwerkingsinstructies voor het machinemodel aan elke relevante resource toe te wijzen, kunt u de guide ook toewijzen aan de resourcegroep waartoe het machinemodel behoort.</span><span class="sxs-lookup"><span data-stu-id="f641a-213">Instead of assigning the relevant handling instruction guide for the machine model to every relevant resource, you could instead assign the Guide to the resource group that reflects that machine model.</span></span>

<span data-ttu-id="f641a-214">**Voorbeeld 2:** u hebt een resourcegroep gedefinieerd voor een werkcel die verschillende machines bevat en u beschikt over een guide waarin algemene instructies worden geboden voor het onderhouden van de werkcel.</span><span class="sxs-lookup"><span data-stu-id="f641a-214">**Example 2:** You have defined a resource group for a work cell that contains different machines and you have a Guide that provides general instructions for how to maintain the work cell.</span></span> <span data-ttu-id="f641a-215">De guide is van toepassing op elke productieactiviteit in deze werkcel.</span><span class="sxs-lookup"><span data-stu-id="f641a-215">The Guide applies to any production activity in this work cell.</span></span>

### <a name="add-a-guide-to-a-resource-group"></a><span data-ttu-id="f641a-216">Een guide toevoegen aan een resourcegroep</span><span class="sxs-lookup"><span data-stu-id="f641a-216">Add a Guide to a resource group</span></span>

<span data-ttu-id="f641a-217">U kunt als volgt een guide toevoegen aan een resourcegroep:</span><span class="sxs-lookup"><span data-stu-id="f641a-217">To add a Guide to a resource group:</span></span>

1. <span data-ttu-id="f641a-218">Ga naar **Productiebeheer \> Instellen \> Resources \> Resourcegroepen**.</span><span class="sxs-lookup"><span data-stu-id="f641a-218">Go to **Production control \> Setup \> Resources \> Resource groups**.</span></span>
1. <span data-ttu-id="f641a-219">Selecteer in het lijstvenster de resourcegroep waaraan u een guide wilt toewijzen.</span><span class="sxs-lookup"><span data-stu-id="f641a-219">From the list pane, select the resource group you want to assign a Guide to.</span></span>
1. <span data-ttu-id="f641a-220">Vouw het sneltabblad **Gekoppelde guides** uit.</span><span class="sxs-lookup"><span data-stu-id="f641a-220">Expand the **Associated Guides** FastTab.</span></span>
1. <span data-ttu-id="f641a-221">Selecteer **Toevoegen** op de werkbalk **Gekoppelde guides**.</span><span class="sxs-lookup"><span data-stu-id="f641a-221">Select **Add** from the **Associated Guides** toolbar.</span></span> <span data-ttu-id="f641a-222">Er wordt een nieuwe regel aan het raster toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="f641a-222">A new line is added to the grid.</span></span>
1. <span data-ttu-id="f641a-223">Voor de nieuwe regel gebruikt u de vervolgkeuzelijst in de kolom **Naam** om de guide te kiezen die u wilt toewijzen.</span><span class="sxs-lookup"><span data-stu-id="f641a-223">For the new line, use the drop-down list in the **Name** column to choose the Guide you want to assign.</span></span> <span data-ttu-id="f641a-224">Als u een groot aantal guides hebt, kunt u de lijst filteren om de gewenste te zoeken.</span><span class="sxs-lookup"><span data-stu-id="f641a-224">If you have a large number of Guides, then you can filter the list to find the one you are looking for.</span></span>
    <span data-ttu-id="f641a-225">![Een guide toevoegen aan een resourcegroep](media/instruction-guides-resourcegroup.png "Een guide toevoegen aan een resourcegroep")</span><span class="sxs-lookup"><span data-stu-id="f641a-225">![Adding a Guide to a resource group](media/instruction-guides-resourcegroup.png "Adding a Guide to a resource group")</span></span>

## <a name="associate-a-guide-to-a-released-product"></a><a name="released-products"></a><span data-ttu-id="f641a-226">Een guide aan een vrijgegeven product koppelen</span><span class="sxs-lookup"><span data-stu-id="f641a-226">Associate a Guide to a released product</span></span>

<span data-ttu-id="f641a-227">U kunt een guide toevoegen aan een willekeurig [vrijgegeven product](../pim/tasks/create-released-product-single-company.md).</span><span class="sxs-lookup"><span data-stu-id="f641a-227">You can add a guide to any [released product](../pim/tasks/create-released-product-single-company.md).</span></span>

### <a name="typical-scenario-using-released-products"></a><span data-ttu-id="f641a-228">Standaardscenario bij het gebruik van vrijgegeven producten</span><span class="sxs-lookup"><span data-stu-id="f641a-228">Typical scenario using released products</span></span>

<span data-ttu-id="f641a-229">Via guides op productniveau kunt u medewerkers op de werkvloer helpen met instructies voor het werken of verwerken van een bepaald vrijgegeven product of artikel.</span><span class="sxs-lookup"><span data-stu-id="f641a-229">Product-level Guides help shop floor workers with instructions relevant to operating or handling a specific released product or item.</span></span>

### <a name="add-a-guide-to-a-released-product"></a><span data-ttu-id="f641a-230">Een guide toevoegen aan een vrijgegeven product</span><span class="sxs-lookup"><span data-stu-id="f641a-230">Add a Guide to a released product</span></span>

<span data-ttu-id="f641a-231">U kunt als volgt een guide toevoegen aan een vrijgegeven product:</span><span class="sxs-lookup"><span data-stu-id="f641a-231">To add a Guide to a released product:</span></span>

1. <span data-ttu-id="f641a-232">Ga naar **Productiegegevensbeheer \> Producten \> Vrijgegeven producten**.</span><span class="sxs-lookup"><span data-stu-id="f641a-232">Go to **Production information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="f641a-233">Open het product waaraan u een guide wilt toewijzen.</span><span class="sxs-lookup"><span data-stu-id="f641a-233">Open the product you want to assign a Guide to.</span></span>
1. <span data-ttu-id="f641a-234">Open in het actievenster het tabblad **Technicus** en selecteer in de groep **Weergeven** **Gekoppelde guides**.</span><span class="sxs-lookup"><span data-stu-id="f641a-234">On the Action Pane, open the **Engineer** tab and from the **View** group, select **Associated Guides**.</span></span>
1. <span data-ttu-id="f641a-235">De pagina **Gekoppelde guides** worden geopend voor uw geselecteerde product.</span><span class="sxs-lookup"><span data-stu-id="f641a-235">The **Associated Guides** page opens for your selected product.</span></span>
1. <span data-ttu-id="f641a-236">Selecteer **Toevoegen** in het actievenster om nieuwe regel toe te voegen aan het raster.</span><span class="sxs-lookup"><span data-stu-id="f641a-236">Select **Add** on the Action Pane to add a new line to the grid.</span></span> 
1. <span data-ttu-id="f641a-237">Voor de nieuwe regel gebruikt u de vervolgkeuzelijst in de kolom **Naam** om de guide te kiezen die u wilt toewijzen.</span><span class="sxs-lookup"><span data-stu-id="f641a-237">For the new line, use the drop-down list in the **Name** column to choose the Guide you want to assign.</span></span>
    <span data-ttu-id="f641a-238">![Een guide toevoegen aan een vrijgegeven product](media/instruction-guides-ReleasedProduct-AddGuides.png "Een guide toevoegen aan een vrijgegeven product")</span><span class="sxs-lookup"><span data-stu-id="f641a-238">![Adding a Guide to a released product](media/instruction-guides-ReleasedProduct-AddGuides.png "Adding a Guide to a released product")</span></span>

## <a name="associate-a-guide-to-a-formula"></a><a name="formulas"></a><span data-ttu-id="f641a-239">Een guide aan een formule koppelen</span><span class="sxs-lookup"><span data-stu-id="f641a-239">Associate a Guide to a formula</span></span>

<span data-ttu-id="f641a-240">U kunt een guide toevoegen aan een willekeurige [formule](bill-of-material-bom.md#formulas-co-products-and-by-products).</span><span class="sxs-lookup"><span data-stu-id="f641a-240">You can add a guide to any [formula](bill-of-material-bom.md#formulas-co-products-and-by-products).</span></span>

### <a name="typical-scenario-using-formulas"></a><span data-ttu-id="f641a-241">Standaardscenario met formules</span><span class="sxs-lookup"><span data-stu-id="f641a-241">Typical scenario using formulas</span></span>
  
<span data-ttu-id="f641a-242">Guides op formuleniveau bieden medewerkers op de werkvloer begeleide verwerkingsinstructies in de context van een formule of recept.</span><span class="sxs-lookup"><span data-stu-id="f641a-242">Formula-level Guides provide shop floor workers with guided handling instructions in the context of a formula or recipe.</span></span> <span data-ttu-id="f641a-243">Er kunnen ook guides worden toegewezen aan versies van een formule.</span><span class="sxs-lookup"><span data-stu-id="f641a-243">Guides can also be assigned to versions of a formula.</span></span>

> [!NOTE]
> <span data-ttu-id="f641a-244">U kunt relevante richtlijnen toewijzen voor productieprocessen die zijn gebaseerd op een formule voor een route, routeversie of routebewerkingsrelaties.</span><span class="sxs-lookup"><span data-stu-id="f641a-244">You can assign guidance relevant for production processes based on a formula to a route, route version, or route operation relations.</span></span>  

> <span data-ttu-id="f641a-245">Er kunnen momenteel geen guides aan afzonderlijke formuleregels worden gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="f641a-245">Guides can't currently be attached to individual formula lines.</span></span>

### <a name="add-a-guide-to-a-formula"></a><span data-ttu-id="f641a-246">Een guide toevoegen aan een formule</span><span class="sxs-lookup"><span data-stu-id="f641a-246">Add a Guide to a formula</span></span>

<span data-ttu-id="f641a-247">U kunt als volgt een guide toevoegen aan een formule:</span><span class="sxs-lookup"><span data-stu-id="f641a-247">To add a Guide to a formula:</span></span>

1. <span data-ttu-id="f641a-248">Ga naar **Productiegegevensbeheer \> Stuklijsten en formules \> Formules**.</span><span class="sxs-lookup"><span data-stu-id="f641a-248">Go to **Production information management \> Bills of materials and formulas \> Formulas**.</span></span>
1. <span data-ttu-id="f641a-249">Open de formule waaraan u een guide wilt toewijzen.</span><span class="sxs-lookup"><span data-stu-id="f641a-249">Open the formula you want to assign a Guide to.</span></span>
1. <span data-ttu-id="f641a-250">Open het tabblad **Koptekst** boven het bovenste sneltabblad.</span><span class="sxs-lookup"><span data-stu-id="f641a-250">Open the **Header** tab above the top FastTab.</span></span>
1. <span data-ttu-id="f641a-251">Vouw het sneltabblad **Gekoppelde guides** uit.</span><span class="sxs-lookup"><span data-stu-id="f641a-251">Expand the **Associated Guides** FastTab.</span></span>
1. <span data-ttu-id="f641a-252">Selecteer **Toevoegen** op de werkbalk **Gekoppelde guides**.</span><span class="sxs-lookup"><span data-stu-id="f641a-252">Select **Add** from the **Associated Guides** toolbar.</span></span> <span data-ttu-id="f641a-253">Er wordt een nieuwe regel aan het raster toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="f641a-253">A new line is added to the grid.</span></span>
1. <span data-ttu-id="f641a-254">Voor de nieuwe regel gebruikt u de vervolgkeuzelijst in de kolom **Naam** om de guide te kiezen die u wilt toewijzen.</span><span class="sxs-lookup"><span data-stu-id="f641a-254">For the new line, use the drop-down list in the **Name** column to choose the Guide you want to assign.</span></span>
    <span data-ttu-id="f641a-255">![Een guide toevoegen aan een formule](media/instruction-guides-Formula.png "Een guide toevoegen aan een formule")</span><span class="sxs-lookup"><span data-stu-id="f641a-255">![Adding a Guide to a formula](media/instruction-guides-Formula.png "Adding a Guide to a formula")</span></span>

## <a name="associate-a-guide-to-a-formula-version"></a><a name="formula-versions"></a><span data-ttu-id="f641a-256">Een guide aan een formuleversie koppelen</span><span class="sxs-lookup"><span data-stu-id="f641a-256">Associate a Guide to a formula version</span></span>

<span data-ttu-id="f641a-257">U kunt een guide toevoegen aan een willekeurige [formuleversie](bill-of-material-bom.md#bom-and-formula-versions).</span><span class="sxs-lookup"><span data-stu-id="f641a-257">You can add a guide to any [formula version](bill-of-material-bom.md#bom-and-formula-versions).</span></span>

### <a name="typical-scenario-using-formula-versions"></a><span data-ttu-id="f641a-258">Standaardscenario met formuleversies</span><span class="sxs-lookup"><span data-stu-id="f641a-258">Typical scenario using formula versions</span></span>

<span data-ttu-id="f641a-259">Guides die aan een afzonderlijke versie van een formule zijn gekoppeld, voorzien medewerkers van instructies voor het doorlopen van de productie van die versie van het recept van de formule.</span><span class="sxs-lookup"><span data-stu-id="f641a-259">Guides attached to an individual version of a formula provide shop floor workers with instructions that walk through the production of that version of the formula recipe.</span></span>

> [!TIP]
> <span data-ttu-id="f641a-260">U kunt relevante richtlijnen toewijzen voor productieprocessen die zijn gebaseerd op deze formuleversie voor een route, routeversie of routebewerkingsrelaties.</span><span class="sxs-lookup"><span data-stu-id="f641a-260">You can assign guidance relevant for production processes based on this formula version to a route, route version, or route operation relations.</span></span>  

> [!NOTE]
> <span data-ttu-id="f641a-261">Er kunnen momenteel geen guides aan afzonderlijke formuleregels worden gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="f641a-261">Guides can't currently be attached to individual formula lines.</span></span>

### <a name="add-a-guide-to-a-formula-version"></a><span data-ttu-id="f641a-262">Een guide toevoegen aan een formuleversie</span><span class="sxs-lookup"><span data-stu-id="f641a-262">Add a Guide to a formula version</span></span>

<span data-ttu-id="f641a-263">U kunt als volgt een guide toevoegen aan een formuleversie:</span><span class="sxs-lookup"><span data-stu-id="f641a-263">To add a Guide to a formula version:</span></span>

1. <span data-ttu-id="f641a-264">Ga naar **Productiegegevensbeheer \> Stuklijsten en formules \> Formules**.</span><span class="sxs-lookup"><span data-stu-id="f641a-264">Go to **Production information management \> Bills of materials and formulas \> Formulas**.</span></span>
1. <span data-ttu-id="f641a-265">Open de formule die een versie bevat waaraan u een guide wilt toewijzen.</span><span class="sxs-lookup"><span data-stu-id="f641a-265">Open the formula that includes a version that you want to assign a Guide to.</span></span>
1. <span data-ttu-id="f641a-266">Open het tabblad **Koptekst** boven het bovenste sneltabblad.</span><span class="sxs-lookup"><span data-stu-id="f641a-266">Open the **Header** tab above the top FastTab.</span></span>
1. <span data-ttu-id="f641a-267">Selecteer op het sneltabblad **Formuleversies** de versie waaraan u een guide wilt toewijzen.</span><span class="sxs-lookup"><span data-stu-id="f641a-267">On the **Formula versions** FastTab, select the version you want to assign a Guide to.</span></span>
1. <span data-ttu-id="f641a-268">Selecteer op de werkbalk **Formuleversies** de optie **Gekoppelde guides**.</span><span class="sxs-lookup"><span data-stu-id="f641a-268">On the **Formula versions** toolbar, select **Associated Guides**.</span></span>
    <span data-ttu-id="f641a-269">![De guides openen die aan een geselecteerde formuleversie zijn gekoppeld](media/instruction-guides-FormulaVersion.png "De guides openen die aan een geselecteerde formuleversie zijn gekoppeld")</span><span class="sxs-lookup"><span data-stu-id="f641a-269">![Open the Guides associated with a selected formula version](media/instruction-guides-FormulaVersion.png "Open the Guides associated with a selected formula version")</span></span>
1. <span data-ttu-id="f641a-270">De pagina **Gekoppelde guides** worden geopend voor uw formuleversie.</span><span class="sxs-lookup"><span data-stu-id="f641a-270">The **Associated Guides** page opens for your formula version.</span></span>
1. <span data-ttu-id="f641a-271">Selecteer **Toevoegen** in het actievenster om nieuwe regel toe te voegen aan het raster.</span><span class="sxs-lookup"><span data-stu-id="f641a-271">Select **Add** on the Action Pane to add a new line to the grid.</span></span> 
1. <span data-ttu-id="f641a-272">Voor de nieuwe regel gebruikt u de vervolgkeuzelijst in de kolom **Naam** om de guide te kiezen die u wilt toewijzen.</span><span class="sxs-lookup"><span data-stu-id="f641a-272">For the new line, use the drop-down list in the **Name** column to choose the Guide you want to assign.</span></span>
    <span data-ttu-id="f641a-273">![Een guide toevoegen aan een formuleversie](media/instruction-guides-FormulaVersionAddGuide.png "Een guide toevoegen aan een formuleversie")</span><span class="sxs-lookup"><span data-stu-id="f641a-273">![Adding a Guide to a formula version](media/instruction-guides-FormulaVersionAddGuide.png "Adding a Guide to a formula version")</span></span>

## <a name="associate-a-guide-to-a-bill-of-materials"></a><a name="bom"></a><span data-ttu-id="f641a-274">Een guide aan een stuklijst koppelen</span><span class="sxs-lookup"><span data-stu-id="f641a-274">Associate a Guide to a bill of materials</span></span>

<span data-ttu-id="f641a-275">U kunt een guide toevoegen aan elke willekeurige [stuklijst](bill-of-material-bom.md).</span><span class="sxs-lookup"><span data-stu-id="f641a-275">You can add a guide to any [bill of materials](bill-of-material-bom.md) (BOM).</span></span>

### <a name="typical-scenario-using-bills-of-materials"></a><span data-ttu-id="f641a-276">Standaardscenario met stuklijsten</span><span class="sxs-lookup"><span data-stu-id="f641a-276">Typical scenario using bills of materials</span></span>

<span data-ttu-id="f641a-277">Guides die aan een stuklijst zijn gekoppeld, voorzien medewerkers van instructies waarin wordt uitgelegd hoe materiaal van een stuklijst kan worden voorbereid en verwerkt.</span><span class="sxs-lookup"><span data-stu-id="f641a-277">Guides attached to a BOM provide shop floor workers with instructions that explain how to prepare and handle material from a BOM.</span></span> <span data-ttu-id="f641a-278">Er kunnen ook guides worden toegewezen aan versies van een stuklijst.</span><span class="sxs-lookup"><span data-stu-id="f641a-278">Guides can also be assigned to versions of a BOM.</span></span>

> [!NOTE]
> <span data-ttu-id="f641a-279">Er kunnen momenteel geen guides aan afzonderlijke stuklijstregels worden gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="f641a-279">Guides can't currently be attached to individual BOM lines.</span></span>

### <a name="add-a-guide-to-a-bill-of-materials"></a><span data-ttu-id="f641a-280">Een guide toevoegen aan een stuklijst</span><span class="sxs-lookup"><span data-stu-id="f641a-280">Add a Guide to a bill of materials</span></span>

<span data-ttu-id="f641a-281">U kunt als volgt een guide toevoegen aan een stuklijst:</span><span class="sxs-lookup"><span data-stu-id="f641a-281">To add a Guide to a bill of material:</span></span>

1. <span data-ttu-id="f641a-282">Ga naar **Productiegegevensbeheer \> Stuklijsten en formules \> Stuklijsten**.</span><span class="sxs-lookup"><span data-stu-id="f641a-282">Go to **Production information management \> Bills of materials and formulas \> Bills of materials**.</span></span>
1. <span data-ttu-id="f641a-283">Open de stuklijst waaraan u een guide wilt toewijzen.</span><span class="sxs-lookup"><span data-stu-id="f641a-283">Open the bill of materials that you want to assign a Guide to.</span></span>
1. <span data-ttu-id="f641a-284">Open het tabblad **Koptekst** boven het bovenste sneltabblad.</span><span class="sxs-lookup"><span data-stu-id="f641a-284">Open the **Header** tab above the top FastTab.</span></span>
1. <span data-ttu-id="f641a-285">Vouw het sneltabblad **Gekoppelde guides** uit.</span><span class="sxs-lookup"><span data-stu-id="f641a-285">Expand the **Associated Guides** FastTab.</span></span>
1. <span data-ttu-id="f641a-286">Selecteer **Toevoegen** op de werkbalk **Gekoppelde guides**.</span><span class="sxs-lookup"><span data-stu-id="f641a-286">Select **Add** from the **Associated Guides** toolbar.</span></span> <span data-ttu-id="f641a-287">Er wordt een nieuwe regel aan het raster toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="f641a-287">A new line is added to the grid.</span></span>
1. <span data-ttu-id="f641a-288">Voor de nieuwe regel gebruikt u de vervolgkeuzelijst in de kolom **Naam** om de guide te kiezen die u wilt toewijzen.</span><span class="sxs-lookup"><span data-stu-id="f641a-288">For the new line, use the drop-down list in the **Name** column to choose the Guide you want to assign.</span></span>
    <span data-ttu-id="f641a-289">![Een guide toevoegen aan een stuklijst](media/instruction-guides-BOM.png "Een guide toevoegen aan een stuklijst")</span><span class="sxs-lookup"><span data-stu-id="f641a-289">![Adding a Guide to a BOM](media/instruction-guides-BOM.png "Adding a Guide to a BOM")</span></span>

## <a name="associate-a-guide-to-a-bill-of-materials-version"></a><a name="bom-versions"></a><span data-ttu-id="f641a-290">Een guide aan een stuklijstversie koppelen</span><span class="sxs-lookup"><span data-stu-id="f641a-290">Associate a Guide to a bill of materials version</span></span>

<span data-ttu-id="f641a-291">U kunt een guide toevoegen aan elke willekeurige [stuklijstversie](bill-of-material-bom.md#bom-and-formula-versions).</span><span class="sxs-lookup"><span data-stu-id="f641a-291">You can add a guide to any [bill of materials version](bill-of-material-bom.md#bom-and-formula-versions).</span></span>

### <a name="typical-scenario-using-bill-of-materials-versions"></a><span data-ttu-id="f641a-292">Standaardscenario met stuklijstversies</span><span class="sxs-lookup"><span data-stu-id="f641a-292">Typical scenario using bill of materials versions</span></span>

<span data-ttu-id="f641a-293">Guides die aan een afzonderlijke stuklijstversie zijn gekoppeld, voorzien medewerkers van instructies waarin wordt uitgelegd hoe u materiaal voorbereidt en verwerkt voor een versie van een stuklijst die verschilt van de algemene stuklijst of andere versies van de stuklijst.</span><span class="sxs-lookup"><span data-stu-id="f641a-293">Guides attached to an individual BOM version provide shop floor workers with instructions that explain how to prepare and handle material for a version of a BOM that is different from the generic BOM or other versions of it.</span></span>

> [!NOTE]
> <span data-ttu-id="f641a-294">Er kunnen momenteel geen guides aan afzonderlijke stuklijstregels worden gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="f641a-294">Guides can't currently be attached to individual BOM lines.</span></span>

### <a name="add-a-guide-to-a-bill-of-materials-version"></a><span data-ttu-id="f641a-295">Een guide toevoegen aan een stuklijstversie</span><span class="sxs-lookup"><span data-stu-id="f641a-295">Add a Guide to a bill of materials version</span></span>

<span data-ttu-id="f641a-296">U kunt als volgt een guide toevoegen aan een stuklijstversie:</span><span class="sxs-lookup"><span data-stu-id="f641a-296">To add a Guide to a bill of materials version:</span></span>

1. <span data-ttu-id="f641a-297">Ga naar **Productiegegevensbeheer \> Stuklijsten en formules \> Stuklijsten**.</span><span class="sxs-lookup"><span data-stu-id="f641a-297">Go to **Production information management \> Bills of materials and formulas \> Bills of materials**.</span></span>
1. <span data-ttu-id="f641a-298">Open de stuklijst die een versie bevat waaraan u een guide wilt toewijzen.</span><span class="sxs-lookup"><span data-stu-id="f641a-298">Open the BOM that includes a version that you want to assign a Guide to.</span></span>
1. <span data-ttu-id="f641a-299">Open het tabblad **Koptekst** boven het bovenste sneltabblad.</span><span class="sxs-lookup"><span data-stu-id="f641a-299">Open the **Header** tab above the top FastTab.</span></span>
1. <span data-ttu-id="f641a-300">Selecteer op het sneltabblad **Stuklijstversies** de versie waaraan u een guide wilt toewijzen.</span><span class="sxs-lookup"><span data-stu-id="f641a-300">On the **BOM versions** FastTab, select the version you want to assign a Guide to.</span></span>
1. <span data-ttu-id="f641a-301">Selecteer op de werkbalk **Stuklijstversies** de optie **Gekoppelde guides**.</span><span class="sxs-lookup"><span data-stu-id="f641a-301">On the **BOM versions** toolbar, select **Associated Guides**.</span></span>
    <span data-ttu-id="f641a-302">![De guides openen die aan een geselecteerde stuklijstversie zijn gekoppeld](media/instruction-guides-BOMVersion.png "De guides openen die aan een geselecteerde stuklijstversie zijn gekoppeld")</span><span class="sxs-lookup"><span data-stu-id="f641a-302">![Open the Guides associated with a selected BOM version](media/instruction-guides-BOMVersion.png "Open the Guides associated with a selected BOM version")</span></span>
1. <span data-ttu-id="f641a-303">De pagina **Gekoppelde guides** worden geopend voor uw stuklijstversie.</span><span class="sxs-lookup"><span data-stu-id="f641a-303">The **Associated Guides** page opens for your BOM version.</span></span>
1. <span data-ttu-id="f641a-304">Selecteer **Toevoegen** in het actievenster om nieuwe regel toe te voegen aan het raster.</span><span class="sxs-lookup"><span data-stu-id="f641a-304">Select **Add** on the Action Pane to add a new line to the grid.</span></span>
1. <span data-ttu-id="f641a-305">Voor de nieuwe regel gebruikt u de vervolgkeuzelijst in de kolom **Naam** om de guide te kiezen die u wilt toewijzen.</span><span class="sxs-lookup"><span data-stu-id="f641a-305">For the new line, use the drop-down list in the **Name** column to choose the Guide you want to assign.</span></span>
    <span data-ttu-id="f641a-306">![Een guide toevoegen aan een stuklijstversie](media/instruction-guides-BOMVersionAddGuide.png "Een guide toevoegen aan een stuklijstversie")</span><span class="sxs-lookup"><span data-stu-id="f641a-306">![Adding a Guide to a BOM version](media/instruction-guides-BOMVersionAddGuide.png "Adding a Guide to a BOM version")</span></span>

## <a name="associate-a-guide-to-a-route"></a><a name="routes"></a><span data-ttu-id="f641a-307">Een guide aan een route koppelen</span><span class="sxs-lookup"><span data-stu-id="f641a-307">Associate a Guide to a route</span></span>

<span data-ttu-id="f641a-308">U kunt een guide toevoegen aan een willekeurige [route](routes-operations.md).</span><span class="sxs-lookup"><span data-stu-id="f641a-308">You can add a guide to any [route](routes-operations.md).</span></span>

### <a name="typical-scenario-using-routes"></a><span data-ttu-id="f641a-309">Standaardscenario met routes</span><span class="sxs-lookup"><span data-stu-id="f641a-309">Typical scenario using routes</span></span>

<span data-ttu-id="f641a-310">Routes worden meestal gebruikt om op te geven hoe een bepaald vrijgegeven product moet worden geproduceerd op basis van een stuklijst of stuklijstversie en met een set resources of resourcegroepen.</span><span class="sxs-lookup"><span data-stu-id="f641a-310">Routes are typically used to specify how a certain released product shall be produced based on a BOM or BOM version and with a set of resources or resource groups.</span></span>

<span data-ttu-id="f641a-311">Wijs een guide aan een route toe om stapsgewijze instructies te leveren voor het respectievelijke productieproces.</span><span class="sxs-lookup"><span data-stu-id="f641a-311">Assign a Guide to a route to provide step-by-step instructions for the respective production process.</span></span>

### <a name="add-a-guide-to-a-route"></a><span data-ttu-id="f641a-312">Een guide toevoegen aan een route</span><span class="sxs-lookup"><span data-stu-id="f641a-312">Add a Guide to a route</span></span>

<span data-ttu-id="f641a-313">U kunt als volgt een guide toevoegen aan een route:</span><span class="sxs-lookup"><span data-stu-id="f641a-313">To add a Guide to a route:</span></span>

1. <span data-ttu-id="f641a-314">Ga naar **Productiebeheer \> Alle routes**.</span><span class="sxs-lookup"><span data-stu-id="f641a-314">Go to **Production control \> All routes**.</span></span>
1. <span data-ttu-id="f641a-315">Open de route waaraan u een guide wilt toewijzen.</span><span class="sxs-lookup"><span data-stu-id="f641a-315">Open the route that you want to assign a Guide to.</span></span>
1. <span data-ttu-id="f641a-316">Vouw het sneltabblad **Gekoppelde guides** uit.</span><span class="sxs-lookup"><span data-stu-id="f641a-316">Expand the **Associated Guides** FastTab.</span></span>
1. <span data-ttu-id="f641a-317">Selecteer **Toevoegen** op de werkbalk **Gekoppelde guides**.</span><span class="sxs-lookup"><span data-stu-id="f641a-317">Select **Add** from the **Associated Guides** toolbar.</span></span> <span data-ttu-id="f641a-318">Er wordt een nieuwe regel aan het raster toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="f641a-318">A new line is added to the grid.</span></span>
1. <span data-ttu-id="f641a-319">Voor de nieuwe regel gebruikt u de vervolgkeuzelijst in de kolom **Naam** om de guide te kiezen die u wilt toewijzen.</span><span class="sxs-lookup"><span data-stu-id="f641a-319">For the new line, use the drop-down list in the **Name** column to choose the Guide you want to assign.</span></span>
    <span data-ttu-id="f641a-320">![Een guide toevoegen aan een route](media/instruction-guides-Route.png "Een guide toevoegen aan een route")</span><span class="sxs-lookup"><span data-stu-id="f641a-320">![Adding a Guide to a route](media/instruction-guides-Route.png "Adding a Guide to a route")</span></span>

## <a name="associate-a-guide-to-a-route-version"></a><a name="route-versions"></a><span data-ttu-id="f641a-321">Een guide aan een routeversie koppelen</span><span class="sxs-lookup"><span data-stu-id="f641a-321">Associate a Guide to a route version</span></span>

<span data-ttu-id="f641a-322">U kunt een guide toevoegen aan een willekeurige [routeversie](routes-operations.md#route-versions).</span><span class="sxs-lookup"><span data-stu-id="f641a-322">You can add a guide to any [route version](routes-operations.md#route-versions).</span></span>

### <a name="typical-scenario-using-route-versions"></a><span data-ttu-id="f641a-323">Standaardscenario met routeversies</span><span class="sxs-lookup"><span data-stu-id="f641a-323">Typical scenario using route versions</span></span>

<span data-ttu-id="f641a-324">Routeversies worden meestal gebruikt om varianten van productieprocessen op basis van een bestaande route op te geven.</span><span class="sxs-lookup"><span data-stu-id="f641a-324">Routes versions are typically used to specify variants of production processes based on an existing route.</span></span> <span data-ttu-id="f641a-325">U kunt verschillende guides toewijzen aan elke routeversie.</span><span class="sxs-lookup"><span data-stu-id="f641a-325">You can assign different Guides to each route version.</span></span>

### <a name="add-a-guide-to-a-route-version"></a><span data-ttu-id="f641a-326">Een guide toevoegen aan een routeversie</span><span class="sxs-lookup"><span data-stu-id="f641a-326">Add a Guide to a route version</span></span>

<span data-ttu-id="f641a-327">U kunt als volgt een guide toevoegen aan een routeversie:</span><span class="sxs-lookup"><span data-stu-id="f641a-327">To add a Guide to a route version:</span></span>

1. <span data-ttu-id="f641a-328">Ga naar **Productiebeheer \> Alle routes**.</span><span class="sxs-lookup"><span data-stu-id="f641a-328">Go to **Production control \> All routes**.</span></span>
1. <span data-ttu-id="f641a-329">Open de route waaraan u een guide wilt toewijzen.</span><span class="sxs-lookup"><span data-stu-id="f641a-329">Open the route that you want to assign a Guide to.</span></span>
1. <span data-ttu-id="f641a-330">Selecteer op het sneltabblad **Versies** de versie waaraan u een guide wilt toewijzen.</span><span class="sxs-lookup"><span data-stu-id="f641a-330">On the **Versions** FastTab, select the version you want to assign a Guide to.</span></span>
1. <span data-ttu-id="f641a-331">Selecteer op de werkbalk **Versies** de optie **Gekoppelde guides**.</span><span class="sxs-lookup"><span data-stu-id="f641a-331">On the **Versions** toolbar, select **Associated Guides**.</span></span>
    <span data-ttu-id="f641a-332">![De guides openen die aan een geselecteerde routeversie zijn gekoppeld](media/instruction-guides-RouteVersion.png "De guides openen die aan een geselecteerde routeversie zijn gekoppeld")</span><span class="sxs-lookup"><span data-stu-id="f641a-332">![Open the Guides associated with a selected route version](media/instruction-guides-RouteVersion.png "Open the Guides associated with a selected route version")</span></span>
1. <span data-ttu-id="f641a-333">De pagina **Gekoppelde guides** worden geopend voor uw stuklijstversie.</span><span class="sxs-lookup"><span data-stu-id="f641a-333">The **Associated Guides** page opens for your BOM version.</span></span>
1. <span data-ttu-id="f641a-334">Selecteer **Toevoegen** in het actievenster om nieuwe regel toe te voegen aan het raster.</span><span class="sxs-lookup"><span data-stu-id="f641a-334">Select **Add** on the Action Pane to add a new line to the grid.</span></span>
1. <span data-ttu-id="f641a-335">Voor de nieuwe regel gebruikt u de vervolgkeuzelijst in de kolom **Naam** om de guide te kiezen die u wilt toewijzen.</span><span class="sxs-lookup"><span data-stu-id="f641a-335">For the new line, use the drop-down list in the **Name** column to choose the Guide you want to assign.</span></span>
    <span data-ttu-id="f641a-336">![Een guide toevoegen aan een routeversie](media/instruction-guides-RouteVersionAddGuide.png "Een guide toevoegen aan een routeversie")</span><span class="sxs-lookup"><span data-stu-id="f641a-336">![Adding a Guide to a route version](media/instruction-guides-RouteVersionAddGuide.png "Adding a Guide to a route version")</span></span>

## <a name="associate-a-guide-to-a-route-operation-relation"></a><a name="route-operation-relations"></a><span data-ttu-id="f641a-337">Een guide aan een routebewerkingsrelatie koppelen</span><span class="sxs-lookup"><span data-stu-id="f641a-337">Associate a Guide to a route operation relation</span></span>

<span data-ttu-id="f641a-338">U kunt een guide toevoegen aan een willekeurige [routebewerkingsrelatie](routes-operations.md#operation-relations).</span><span class="sxs-lookup"><span data-stu-id="f641a-338">You can add a guide to any [route operation relation](routes-operations.md#operation-relations).</span></span>

### <a name="typical-scenario-using-route-operation-relations"></a><span data-ttu-id="f641a-339">Standaardscenario met routebewerkingsrelaties</span><span class="sxs-lookup"><span data-stu-id="f641a-339">Typical scenario using route operation relations</span></span>

<span data-ttu-id="f641a-340">Bewerkingsrelaties zijn de meest specifieke manier om richtlijnen toe te voegen aan een productproces en de bijbehorende bewerkingen.</span><span class="sxs-lookup"><span data-stu-id="f641a-340">Operation relations are the most specific way to add guidance to a product process and its related operations.</span></span> <span data-ttu-id="f641a-341">U kunt voor elke bewerking in een route richtlijnen opgeven en verschillende richtlijnen opgeven voor de typen relatiecontext die voor een route is opgegeven, bijvoorbeeld voor specifieke artikelen, configuraties en meer.</span><span class="sxs-lookup"><span data-stu-id="f641a-341">You can specify guidance for each operation in a route and specify different guidance for any type of relation context specified for a route, such as for specific items, configurations, and more.</span></span> <span data-ttu-id="f641a-342">U kunt ook opgeven in welke fasen van de bewerking de richtlijnen van toepassing zijn (zoals instelling, plaatsing in de wachtrij, verwerking of transport).</span><span class="sxs-lookup"><span data-stu-id="f641a-342">You can also specify to which stages in the operation the guidance applies (such as setup, queueing, process, or transport).</span></span>

> [!NOTE]
> <span data-ttu-id="f641a-343">Als u guides opgeeft voor verschillende bewerkingsrelaties van een route, wordt in deze richtlijnen alleen de guides van de meest specifieke relatie weergegeven op de werkvloer voor de gegenereerde taak.</span><span class="sxs-lookup"><span data-stu-id="f641a-343">If you specify guides for several operation relations of a route, among those guides, only the guide from the most specific relation will be show on the shop floor for the generated job.</span></span>

### <a name="add-a-guide-to-a-route-operation-relation"></a><span data-ttu-id="f641a-344">Een guide toevoegen aan een routebewerkingsrelatie</span><span class="sxs-lookup"><span data-stu-id="f641a-344">Add a Guide to a route operation relation</span></span>

<span data-ttu-id="f641a-345">U kunt als volgt een guide toevoegen aan een routebewerkingsrelatie:</span><span class="sxs-lookup"><span data-stu-id="f641a-345">To add a Guide to a route operation relation:</span></span>

1. <span data-ttu-id="f641a-346">Ga naar **Productiebeheer \> Alle routes**.</span><span class="sxs-lookup"><span data-stu-id="f641a-346">Go to **Production control \> All routes**.</span></span>
1. <span data-ttu-id="f641a-347">Open de route waaraan u een guide wilt toewijzen.</span><span class="sxs-lookup"><span data-stu-id="f641a-347">Open the route that you want to assign a Guide to.</span></span>
1. <span data-ttu-id="f641a-348">Open in het actievenster het tabblad **Route** en selecteer in de groep **Onderhouden** de optie **Routedetails**.</span><span class="sxs-lookup"><span data-stu-id="f641a-348">On the Action Pane, open the **Route** tab and from the **Maintain** group, select **Route details**.</span></span>
1. <span data-ttu-id="f641a-349">De pagina **Routedetails** wordt geopend voor de geselecteerde route.</span><span class="sxs-lookup"><span data-stu-id="f641a-349">The **Route details** page opens for your selected rout.</span></span>
1. <span data-ttu-id="f641a-350">Selecteer in het bovenste raster de bewerking waarvoor u richtlijnen wilt opgeven.</span><span class="sxs-lookup"><span data-stu-id="f641a-350">In the top grid, select the operation you want to provide guidance for.</span></span>
1. <span data-ttu-id="f641a-351">Selecteer in het onderste raster een specifieke relatie (of de algemene relatie **Alle** ).</span><span class="sxs-lookup"><span data-stu-id="f641a-351">In the bottom grid, select a specific relation (or the generic **All** relation).</span></span>
    <span data-ttu-id="f641a-352">![Een bewerking en vervolgens een relatie selecteren](media/instruction-guides-RouteOperationRelation.png "Een bewerking en vervolgens een relatie selecteren")</span><span class="sxs-lookup"><span data-stu-id="f641a-352">![Select an operation and then a relation](media/instruction-guides-RouteOperationRelation.png "Select an operation and then a relation")</span></span>
1. <span data-ttu-id="f641a-353">Open boven het onderste raster het tabblad **Gekoppelde guides**. ![Het tabblad Gekoppelde guides](media/instruction-guides-RouteOperationRelation-AddGuide.png "Het tabblad Gekoppelde guides")</span><span class="sxs-lookup"><span data-stu-id="f641a-353">Above the bottom gird, open the **Associated Guides** tab.  ![The Associated Guides tab](media/instruction-guides-RouteOperationRelation-AddGuide.png "The Associated Guides tab")</span></span>
1. <span data-ttu-id="f641a-354">Selecteer **Toevoegen** in de werkbalk boven aan het onderste raster om een nieuwe regel aan het raster toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="f641a-354">Select **Add** from the toolbar at the top of the bottom grid to add a new line to the grid.</span></span>
1. <span data-ttu-id="f641a-355">Gebruik voor de nieuwe rij de vervolgkeuzelijst in de kolom **Naam** om de guide te kiezen die u wilt toewijzen.</span><span class="sxs-lookup"><span data-stu-id="f641a-355">For the new row, use the drop-down list in the **Name** column to choose the Guide you want to assign.</span></span> <span data-ttu-id="f641a-356">Schakel in de rest van de rij het selectievakje in voor elke context waarin de geselecteerde guide beschikbaar moet zijn.</span><span class="sxs-lookup"><span data-stu-id="f641a-356">In the rest of the row, select the check box for each context where the selected Guide should be available.</span></span>

> [!NOTE]
> <span data-ttu-id="f641a-357">U kunt een of meer guides toevoegen voor elke fase van elke bewerking.</span><span class="sxs-lookup"><span data-stu-id="f641a-357">You can add one or more guides for each stage of each operation.</span></span>

## <a name="select-guides-from-the-shop-floor-execution-interface"></a><span data-ttu-id="f641a-358">Guides selecteren in de uitvoeringsinterface van de werkvloer</span><span class="sxs-lookup"><span data-stu-id="f641a-358">Select guides from the shop floor execution interface</span></span>

<span data-ttu-id="f641a-359">Wanneer een medewerker een takenlijst opent in de uitvoeringsinterface voor de werkvloer, worden in Supply Chain Management de relevante guides voor de weergegeven taken gevonden.</span><span class="sxs-lookup"><span data-stu-id="f641a-359">When a worker opens a job list on the shop floor execution interface, Supply Chain Management finds the relevant guides for the jobs shown.</span></span> <span data-ttu-id="f641a-360">Gebruik de knop **Guides** om de relevante guides weer te geven.</span><span class="sxs-lookup"><span data-stu-id="f641a-360">Use the **Guides** button to view the relevant guides.</span></span>

<span data-ttu-id="f641a-361">![Knop Guides in de uitvoeringsinterface van de werkvloer](media/instruction-guides-Shopfloor1.png "Knop Guides in de uitvoeringsinterface van de werkvloer")</span><span class="sxs-lookup"><span data-stu-id="f641a-361">![Guides button in the shop floor execution interface](media/instruction-guides-Shopfloor1.png "Guides button in the shop floor execution interface")</span></span>

<span data-ttu-id="f641a-362">Zet vervolgens een HoloLens op en open de desbetreffende guide door naar de QR-code te kijken en de desbetreffende guide te activeren.</span><span class="sxs-lookup"><span data-stu-id="f641a-362">Then put on a HoloLens and access the respective guide by glancing at the QR code and activating the respective Guide.</span></span>

<span data-ttu-id="f641a-363">![QR-code om toegang te krijgen tot guides via een HoloLens](media/instruction-guides-Shopfloor2.png "QR-code om toegang te krijgen tot guides via een HoloLens")</span><span class="sxs-lookup"><span data-stu-id="f641a-363">![QR code to access guides using a HoloLens](media/instruction-guides-Shopfloor2.png "QR code to access guides using a HoloLens")</span></span>

## <a name="resolving-the-logic-for-selecting-guides"></a><a name="logic"></a><span data-ttu-id="f641a-364">De logica voor het selecteren van guides oplossen</span><span class="sxs-lookup"><span data-stu-id="f641a-364">Resolving the logic for selecting Guides</span></span>

<span data-ttu-id="f641a-365">U kunt guides toevoegen aan de volgende productiegegevens:</span><span class="sxs-lookup"><span data-stu-id="f641a-365">You can add Guides to the following production data:</span></span>

- [<span data-ttu-id="f641a-366">Bronnen</span><span class="sxs-lookup"><span data-stu-id="f641a-366">Resources</span></span>](#resources)
- [<span data-ttu-id="f641a-367">Resourcegroepen</span><span class="sxs-lookup"><span data-stu-id="f641a-367">Resource groups</span></span>](#resource-groups)
- [<span data-ttu-id="f641a-368">Vrijgegeven producten</span><span class="sxs-lookup"><span data-stu-id="f641a-368">Released products</span></span>](#released-products)
- [<span data-ttu-id="f641a-369">Formules</span><span class="sxs-lookup"><span data-stu-id="f641a-369">Formulas</span></span>](#formulas)
- [<span data-ttu-id="f641a-370">Formuleversies</span><span class="sxs-lookup"><span data-stu-id="f641a-370">Formula versions</span></span>](#formula-versions)
- [<span data-ttu-id="f641a-371">Stuklijsten</span><span class="sxs-lookup"><span data-stu-id="f641a-371">Bills of material (BOMs)</span></span>](#bom)
- [<span data-ttu-id="f641a-372">Stuklijstversies</span><span class="sxs-lookup"><span data-stu-id="f641a-372">BOM versions</span></span>](#bom-versions)
- [<span data-ttu-id="f641a-373">Routes</span><span class="sxs-lookup"><span data-stu-id="f641a-373">Routes</span></span>](#routes)
- [<span data-ttu-id="f641a-374">Routeversies</span><span class="sxs-lookup"><span data-stu-id="f641a-374">Route versions</span></span>](#route-versions)
- [<span data-ttu-id="f641a-375">Routebewerkingsrelaties</span><span class="sxs-lookup"><span data-stu-id="f641a-375">Route operation relations</span></span>](#route-operation-relations)

<span data-ttu-id="f641a-376">Wanneer Supply Chain Management de taken voor de productievloer genereert, worden de relevante guides van deze bronnen verzameld.</span><span class="sxs-lookup"><span data-stu-id="f641a-376">When Supply Chain Management generates the jobs for the production floor, it will collect the relevant Guides from those sources.</span></span> <span data-ttu-id="f641a-377">Let op de volgende belangrijke regels.</span><span class="sxs-lookup"><span data-stu-id="f641a-377">Take note of the following important rules.</span></span>

- <span data-ttu-id="f641a-378">Als u een stuklijstversie of formuleversie aan een route of productieorder koppelt, worden alle guides die aan deze versie zijn gekoppeld en ook de guides die aan de bovenliggende stuklijst of formule van die versie zijn gekoppeld, weergegeven in de taak.</span><span class="sxs-lookup"><span data-stu-id="f641a-378">If you attach a BOM version or formula version to a route or production order, then any Guides attached to this version, and also the Guides attached to the parent BOM or formula of that version, will be shown on the job.</span></span>
- <span data-ttu-id="f641a-379">Als u een routeversie of formuleversie aan een productieorder koppelt, worden alle guides die aan deze versie zijn gekoppeld en ook de guides die aan de bovenliggende route van die versie zijn gekoppeld, weergegeven in de taak.</span><span class="sxs-lookup"><span data-stu-id="f641a-379">If you attach a route version to a production order, then any Guides attached to this version, and also the Guides attached to the parent route of that version, will be shown on the job.</span></span>
- <span data-ttu-id="f641a-380">Als u verschillende routebewerkingsrelaties definieert die de relatie *Alle* bevatten en hieraan guides toewijst, worden alleen de guides van de meest specifieke relatie voor de taak weergegeven.</span><span class="sxs-lookup"><span data-stu-id="f641a-380">If you define several route operation relations that include the *All* relation and assign Guides to those, only the Guides from the most specific relation will be shown for the job.</span></span>  

<span data-ttu-id="f641a-381">![Diagram voor het oplossen van de relevante guides](media/instruction-guides-Resolve.png "Diagram voor het oplossen van de relevante guides")</span><span class="sxs-lookup"><span data-stu-id="f641a-381">![Diagram on resolving the relevant Guides](media/instruction-guides-Resolve.png "Diagram on resolving the relevant Guides")</span></span>
