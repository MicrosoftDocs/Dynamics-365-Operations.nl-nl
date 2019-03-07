---
title: Afschrijving naar rato van verbruik
description: Dit artikel biedt een overzicht van de afschrijvingsmethode Verbruik.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 13751
ms.assetid: d25a681f-49a5-4bfc-aa76-1c6373e35dd8
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c0f64fee275f63a3e6b31a196df872e41c84dde6
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/29/2019
ms.locfileid: "319679"
---
# <a name="consumption-depreciation"></a><span data-ttu-id="0be54-103">Afschrijving naar rato van verbruik</span><span class="sxs-lookup"><span data-stu-id="0be54-103">Consumption depreciation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0be54-104">Dit artikel biedt een overzicht van de afschrijvingsmethode Verbruik.</span><span class="sxs-lookup"><span data-stu-id="0be54-104">This article gives an overview of the Consumption method of depreciation.</span></span>

<span data-ttu-id="0be54-105">Wanneer u een profiel voor de afschrijving van vaste activa instelt en **Verbruik** selecteert in het veld **Methode** op de pagina **Afschrijvingsprofielen**, worden vaste activa toegewezen aan het afschrijvingsprofiel op basis van hun gebruik.</span><span class="sxs-lookup"><span data-stu-id="0be54-105">If you set up a depreciation profile for fixed assets and select **Consumption** in the **Method** field on the **Depreciation profiles** page, fixed assets are assigned to the depreciation profile based on their usage.</span></span> <span data-ttu-id="0be54-106">U hoeft geen percentages en intervallen in te stellen op de pagina **Afschrijvingsprofielen**.</span><span class="sxs-lookup"><span data-stu-id="0be54-106">You don't have to set up percentages and intervals on the **Depreciation profiles** page.</span></span> <span data-ttu-id="0be54-107">Wanneer u een afschrijvingsprofiel maakt dat de methode Verbruik gebruikt, kunt u de methode op verschillende manieren instellen.</span><span class="sxs-lookup"><span data-stu-id="0be54-107">After you create a depreciation profile that uses the Consumption method, you can set up the method in various ways.</span></span>

## <a name="set-up-and-use-consumption-depreciation"></a><span data-ttu-id="0be54-108">Afschrijving naar rato van verbruik instellen en gebruiken</span><span class="sxs-lookup"><span data-stu-id="0be54-108">Set up and use consumption depreciation</span></span>
1.  <span data-ttu-id="0be54-109">Maak een afschrijvingsprofiel aan op de pagina **Afschrijvingsprofielen**.</span><span class="sxs-lookup"><span data-stu-id="0be54-109">On the **Depreciation profiles** page, create the depreciation profile.</span></span> <span data-ttu-id="0be54-110">Voor verbruikberekeningen moet het afschrijvingsprofiel een ID en een naam hebben, en moet **Verbruik** zijn geselecteerd in het veld **Methode**.</span><span class="sxs-lookup"><span data-stu-id="0be54-110">For consumption calculations, the depreciation profile must have an ID and a name, and **Consumption** must be selected in the **Method** field.</span></span>
2.  <span data-ttu-id="0be54-111">Stel op de pagina **Verbruiksfactoren** de verbruiksfactoren in.</span><span class="sxs-lookup"><span data-stu-id="0be54-111">On the **Consumption factors** page, set up consumption factors.</span></span> <span data-ttu-id="0be54-112">Elke verbruiksfactor moet een ID en een naam hebben, en een verbruiksfactor die is opgegeven als een hoeveelheid of een percentage.</span><span class="sxs-lookup"><span data-stu-id="0be54-112">Each consumption factor must have an ID and a name, and a consumption factor that is specified as either a quantity or a percentage.</span></span>
3.  <span data-ttu-id="0be54-113">Stel op de pagina **Verbruiksfactoren** de verbruikseenheden in.</span><span class="sxs-lookup"><span data-stu-id="0be54-113">On the **Consumption units** page, set up consumption units.</span></span> <span data-ttu-id="0be54-114">Elke verbruikseenheid moet een ID en een naam hebben.</span><span class="sxs-lookup"><span data-stu-id="0be54-114">Each consumption unit must have an ID and a name.</span></span> <span data-ttu-id="0be54-115">De afschrijvingseenheden worden gebruikt om de afschrijving naar rato van verbruik te berekenen op de pagina **Afschrijving naar rato van verbruik**.</span><span class="sxs-lookup"><span data-stu-id="0be54-115">Depreciation units are used to calculate consumption depreciation on the **Consumption depreciation** page.</span></span> <span data-ttu-id="0be54-116">Voorbeelden van eenheden zijn kilometer (km), kilogram (kg) en uur.</span><span class="sxs-lookup"><span data-stu-id="0be54-116">Examples of units are kilometer (km), kilogram (kg), and hour.</span></span>
4.  <span data-ttu-id="0be54-117">Configureer op de pagina **Vaste activa** afzonderlijke vaste activa.</span><span class="sxs-lookup"><span data-stu-id="0be54-117">On the **Fixed assets** page, set up individual fixed assets.</span></span> <span data-ttu-id="0be54-118">Selecteer waardemodellen en afschrijvingsboeken met afschrijvingsprofielen voor elk vast activum.</span><span class="sxs-lookup"><span data-stu-id="0be54-118">For each fixed asset, select value models and depreciation books that have depreciation profiles.</span></span> <span data-ttu-id="0be54-119">U moet waardemodellen of afschrijvingsboeken voor verbruiksafschrijving instellen als u vaste activa met afschrijvingsprofielen hebt die zijn gebaseerd op de methode Verbruik.</span><span class="sxs-lookup"><span data-stu-id="0be54-119">You must set up value models or depreciation books for consumption depreciation if any of your fixed assets use depreciation profiles that are based on the Consumption method.</span></span> <span data-ttu-id="0be54-120">Deze instellingen wordt uitgevoerd op het tabblad **Afschrijving** van de pagina **Waardemodellen**, of op het sneltabblad **Algemeen** van de pagina **Afschrijvingsprofiel**.</span><span class="sxs-lookup"><span data-stu-id="0be54-120">This setup is done either on the **Depreciation** tab of the **Value models** page or on the **General** FastTab of the **Depreciation profile** page.</span></span> <span data-ttu-id="0be54-121">U kunt voor meerdere vaste activa hetzelfde waardemodel gebruiken.</span><span class="sxs-lookup"><span data-stu-id="0be54-121">You can use the same value model for multiple fixed assets.</span></span> <span data-ttu-id="0be54-122">Afschrijvingsprofielen maken deel uit van het waardemodel of afschrijvingsboek dat u voor de vaste activa selecteert.</span><span class="sxs-lookup"><span data-stu-id="0be54-122">Depreciation profiles are part of the value model or depreciation book that you select for each fixed asset.</span></span> <span data-ttu-id="0be54-123">U kunt afschrijvingsprofielen niet rechtstreeks in het formulier **Vaste activa** toevoegen of wijzigen.</span><span class="sxs-lookup"><span data-stu-id="0be54-123">You can't add or modify depreciation profiles directly on the **Fixed assets** page.</span></span> <span data-ttu-id="0be54-124">Afschrijvingsprofielen kunt u alleen op de pagina **Afschrijvingsboeken** wijzigen.</span><span class="sxs-lookup"><span data-stu-id="0be54-124">You can modify depreciation profiles only on the **Depreciation books** page.</span></span>
5.  <span data-ttu-id="0be54-125">Voer op de pagina **Waardemodellen** of de pagina **Afschrijvingsboeken** in de veldgroep **Afschrijving naar rato van verbruik** in de hieronder genoemde velden de volgende gegevens in:</span><span class="sxs-lookup"><span data-stu-id="0be54-125">On the **Value models** page or the **Depreciation books** page, in the **Consumption depreciation** field group, enter information in the following fields:</span></span>
    -   <span data-ttu-id="0be54-126">Verbruiksfactor</span><span class="sxs-lookup"><span data-stu-id="0be54-126">Consumption factor</span></span>
    -   <span data-ttu-id="0be54-127">Eenheid</span><span class="sxs-lookup"><span data-stu-id="0be54-127">Unit</span></span>
    -   <span data-ttu-id="0be54-128">Eenheidsafschrijving</span><span class="sxs-lookup"><span data-stu-id="0be54-128">Unit depreciation</span></span>
    -   <span data-ttu-id="0be54-129">Geraamd verbruik</span><span class="sxs-lookup"><span data-stu-id="0be54-129">Estimated consumption</span></span>

    <span data-ttu-id="0be54-130">Het veld **Geboekt verbruik** bevat de verbruiksafschrijving, in eenheden, die al is geboekt voor de combinatie van het vaste activum en het waardemodel, of voor het afschrijvingsboek.</span><span class="sxs-lookup"><span data-stu-id="0be54-130">The **Posted consumption** field shows the consumption depreciation, in units, that has already been posted either for the combination of the fixed asset and value model, or for the depreciation book.</span></span> <span data-ttu-id="0be54-131">U kunt de waarde in dit veld niet handmatig bijwerken.</span><span class="sxs-lookup"><span data-stu-id="0be54-131">You can't manually update the value in this field.</span></span>

## <a name="examples"></a><span data-ttu-id="0be54-132">Voorbeelden</span><span class="sxs-lookup"><span data-stu-id="0be54-132">Examples</span></span>
### <a name="example-1"></a><span data-ttu-id="0be54-133">Voorbeeld 1</span><span class="sxs-lookup"><span data-stu-id="0be54-133">Example 1</span></span>

<span data-ttu-id="0be54-134">De volgende verbruiksfactor is ingesteld voor 31 januari:</span><span class="sxs-lookup"><span data-stu-id="0be54-134">The following consumption factor is set up for January 31:</span></span>

-   <span data-ttu-id="0be54-135">De hoeveelheid is 1000.</span><span class="sxs-lookup"><span data-stu-id="0be54-135">The quantity is 1,000.</span></span>
-   <span data-ttu-id="0be54-136">De eenheidsprijs van de afschrijving die is opgegeven voor het vaste activum is 1,5.</span><span class="sxs-lookup"><span data-stu-id="0be54-136">The unit depreciation price that is specified for the fixed asset is 1.5.</span></span>

<span data-ttu-id="0be54-137">Het afschrijvingsvoorstel op 31 januari luidt als volgt: Hoeveelheid x eenheidsafschrijving 1000 x 1,5 = 1500. Als de factor die is ingesteld voor de vaste activa een percentagefactor is, wordt de geraamde hoeveelheid in het veld **Geraamd verbruik** voor het waardemodel van de vaste activa vermenigvuldigd met het percentage dat is ingesteld voor de geselecteerde einddatum.</span><span class="sxs-lookup"><span data-stu-id="0be54-137">The depreciation proposal on January 31 is as follows: Quantity × Unit depreciation 1,000 × 1.5 = 1,500 If the factor that is specified for the fixed asset is a percentage factor, the quantity that is estimated in the **Estimated consumption** field for the value model of the fixed asset is multiplied by the percentage that is set up for the selected end date.</span></span> <span data-ttu-id="0be54-138">De uitkomst van de berekening wordt als hoeveelheid voorgesteld als de afschrijvingshoeveelheid voor de periode.</span><span class="sxs-lookup"><span data-stu-id="0be54-138">The resulting quantity is then suggested as the depreciation quantity for the period.</span></span>

### <a name="example-2"></a><span data-ttu-id="0be54-139">Voorbeeld 2</span><span class="sxs-lookup"><span data-stu-id="0be54-139">Example 2</span></span>

<span data-ttu-id="0be54-140">De volgende factor voor verbruiksafschrijving is ingesteld voor 31 januari:</span><span class="sxs-lookup"><span data-stu-id="0be54-140">The following factor for consumption depreciation is set up for January 31:</span></span>

-   <span data-ttu-id="0be54-141">Het percentage is 10 procent.</span><span class="sxs-lookup"><span data-stu-id="0be54-141">The percentage is 10 percent.</span></span>
-   <span data-ttu-id="0be54-142">De eenheidsprijs van de afschrijving die is opgegeven voor het vaste activum is 1,5.</span><span class="sxs-lookup"><span data-stu-id="0be54-142">The unit depreciation price that is specified for the fixed asset is 1.5.</span></span>
-   <span data-ttu-id="0be54-143">De geschatte hoeveelheid van de vaste activa is 2.000.</span><span class="sxs-lookup"><span data-stu-id="0be54-143">The estimated quantity of the fixed asset is 2,000.</span></span>

<span data-ttu-id="0be54-144">Het afschrijvingsvoorstel op 31 januari luidt als volgt: Geschatte hoeveelheid x percentage x eenheidsafschrijving 2000 x 0,10 x 1,5 = 300</span><span class="sxs-lookup"><span data-stu-id="0be54-144">The depreciation proposal on January 31 is as follows: Estimated quantity × Percentage × Unit depreciation 2,000 × .10 × 1.5 = 300</span></span>



