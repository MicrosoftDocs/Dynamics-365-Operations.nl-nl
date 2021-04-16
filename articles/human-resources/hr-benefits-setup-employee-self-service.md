---
title: Werknemerselfservice configureren
description: In Microsoft Dynamics 365 Human Resources kunt u tegels configureren voor navigatie op het hoogste niveau in Selfservice werknemer.
author: andreabichsel
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 3e763a09e0a0f13eb7222a6ffbcb31b6230b83f4
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/31/2021
ms.locfileid: "5797930"
---
# <a name="configure-employee-self-service"></a><span data-ttu-id="bcd10-103">Werknemerselfservice configureren</span><span class="sxs-lookup"><span data-stu-id="bcd10-103">Configure employee self service</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="bcd10-104">In Microsoft Dynamics 365 Human Resources kunt u tegels configureren voor navigatie op het hoogste niveau in Selfservice werknemer.</span><span class="sxs-lookup"><span data-stu-id="bcd10-104">In Microsoft Dynamics 365 Human Resources, you can configure tiles for top-level navigation in Employee self service.</span></span> <span data-ttu-id="bcd10-105">Vergoedingsplantegels leiden gebruikers naar vergoedingsplannen waarvoor zij in aanmerking komen.</span><span class="sxs-lookup"><span data-stu-id="bcd10-105">Benefit plan tiles direct users to benefit plans that they're eligible for.</span></span>

## <a name="set-up-a-benefit-plans-tile"></a><span data-ttu-id="bcd10-106">Een tegel voor vergoedingsplannen instellen</span><span class="sxs-lookup"><span data-stu-id="bcd10-106">Set up a benefit plans tile</span></span>

1. <span data-ttu-id="bcd10-107">Selecteer in het werkgebied **Vergoedingenbeheer** onder **Instellen** de optie **Parameters voor Selfservice werknemer**.</span><span class="sxs-lookup"><span data-stu-id="bcd10-107">In the **Benefits management** workspace, under **Setup**, select **Employee self service parameters**.</span></span>

2. <span data-ttu-id="bcd10-108">Selecteer het tabblad **Tegel voor vergoedingsplannen instellen** en selecteer vervolgens **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="bcd10-108">Select the **Benefit plans tile setup** tab, and then select **New**.</span></span>

3. <span data-ttu-id="bcd10-109">Geef de waarden op voor de volgende velden:</span><span class="sxs-lookup"><span data-stu-id="bcd10-109">Specify values for the following fields:</span></span>

   | <span data-ttu-id="bcd10-110">Veld</span><span class="sxs-lookup"><span data-stu-id="bcd10-110">Field</span></span> | <span data-ttu-id="bcd10-111">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="bcd10-111">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="bcd10-112">**Tegel-id**</span><span class="sxs-lookup"><span data-stu-id="bcd10-112">**Tile ID**</span></span> | <span data-ttu-id="bcd10-113">De unieke id voor de tegel.</span><span class="sxs-lookup"><span data-stu-id="bcd10-113">The unique identifier for the tile.</span></span> |
   | <span data-ttu-id="bcd10-114">**Tekst van tegellabel**</span><span class="sxs-lookup"><span data-stu-id="bcd10-114">**Tile label text**</span></span> | <span data-ttu-id="bcd10-115">De tekst die voor de tegel wordt weergegeven in Selfservice.</span><span class="sxs-lookup"><span data-stu-id="bcd10-115">The text that will appear for the tile on Self-service.</span></span> |
   | <span data-ttu-id="bcd10-116">**Beschrijving**</span><span class="sxs-lookup"><span data-stu-id="bcd10-116">**Description**</span></span> | <span data-ttu-id="bcd10-117">Een beschrijving van de tegel.</span><span class="sxs-lookup"><span data-stu-id="bcd10-117">A description of the tile.</span></span> |
   | <span data-ttu-id="bcd10-118">**Internetadres**</span><span class="sxs-lookup"><span data-stu-id="bcd10-118">**Internet address**</span></span> | <span data-ttu-id="bcd10-119">Voer de URL in voor de pagina Selfservice werknemer.</span><span class="sxs-lookup"><span data-stu-id="bcd10-119">Enter the URL to the employee self service page.</span></span> |
   | <span data-ttu-id="bcd10-120">**Tegelgrootte**</span><span class="sxs-lookup"><span data-stu-id="bcd10-120">**Tile size**</span></span> | <span data-ttu-id="bcd10-121">De grootte van de tegel: klein, normaal of groot.</span><span class="sxs-lookup"><span data-stu-id="bcd10-121">The size of the tile: Small, Medium, or Large.</span></span> |
   | <span data-ttu-id="bcd10-122">**Doel**</span><span class="sxs-lookup"><span data-stu-id="bcd10-122">**Target**</span></span> | <span data-ttu-id="bcd10-123">Geeft aan of de pagina in een nieuw venster of in het huidige venster moet worden geopend.</span><span class="sxs-lookup"><span data-stu-id="bcd10-123">Specifies whether the page should open in a new window or the current window.</span></span> |
   | <span data-ttu-id="bcd10-124">**Afbeelding voor tegelachtergrond**</span><span class="sxs-lookup"><span data-stu-id="bcd10-124">**Tile background image**</span></span> | <span data-ttu-id="bcd10-125">De URL van de afbeelding die moet worden gebruikt voor de tegel (optioneel).</span><span class="sxs-lookup"><span data-stu-id="bcd10-125">The URL of the image to use for the tile (optional).</span></span> |
   | <span data-ttu-id="bcd10-126">**Start**</span><span class="sxs-lookup"><span data-stu-id="bcd10-126">**Start**</span></span> | <span data-ttu-id="bcd10-127">De begindatum en -tijd waarop de tegel beschikbaar moet zijn.</span><span class="sxs-lookup"><span data-stu-id="bcd10-127">The beginning date and time the tile should be available.</span></span> |
   | <span data-ttu-id="bcd10-128">**End**</span><span class="sxs-lookup"><span data-stu-id="bcd10-128">**End**</span></span> | <span data-ttu-id="bcd10-129">De einddatum en -tijd waarop de tegel beschikbaar moet zijn.</span><span class="sxs-lookup"><span data-stu-id="bcd10-129">The end date and time the tile should be available.</span></span> |

4. <span data-ttu-id="bcd10-130">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="bcd10-130">Select **Save**.</span></span>

## <a name="set-up-a-flex-credit-plan-tile"></a><span data-ttu-id="bcd10-131">Een tegel voor een flex-kredietplan instellen</span><span class="sxs-lookup"><span data-stu-id="bcd10-131">Set up a flex credit plan tile</span></span>

1. <span data-ttu-id="bcd10-132">Selecteer in het werkgebied **Vergoedingenbeheer** onder **Instellen** de optie **Parameters voor Selfservice werknemer**.</span><span class="sxs-lookup"><span data-stu-id="bcd10-132">In the **Benefits management** workspace, under **Setup**, select **Employee self service parameters**.</span></span>

2. <span data-ttu-id="bcd10-133">Selecteer het tabblad **Tegel voor flex-kredietplan instellen** en selecteer vervolgens **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="bcd10-133">Select the **Flex credit plan tile setup** tab, and then select **New**.</span></span>

3. <span data-ttu-id="bcd10-134">Geef de waarden op voor de volgende velden:</span><span class="sxs-lookup"><span data-stu-id="bcd10-134">Specify values for the following fields:</span></span>

   | <span data-ttu-id="bcd10-135">Veld</span><span class="sxs-lookup"><span data-stu-id="bcd10-135">Field</span></span> | <span data-ttu-id="bcd10-136">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="bcd10-136">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="bcd10-137">**Tegel-id**</span><span class="sxs-lookup"><span data-stu-id="bcd10-137">**Tile ID**</span></span> | <span data-ttu-id="bcd10-138">De unieke id voor de tegel.</span><span class="sxs-lookup"><span data-stu-id="bcd10-138">The unique identifier for the tile.</span></span> |
   | <span data-ttu-id="bcd10-139">**Tekst van tegellabel**</span><span class="sxs-lookup"><span data-stu-id="bcd10-139">**Tile label text**</span></span> | <span data-ttu-id="bcd10-140">De tekst die voor de tegel wordt weergegeven in Selfservice.</span><span class="sxs-lookup"><span data-stu-id="bcd10-140">The text that will appear for the tile on Self service.</span></span> |
   | <span data-ttu-id="bcd10-141">**Beschrijving**</span><span class="sxs-lookup"><span data-stu-id="bcd10-141">**Description**</span></span> | <span data-ttu-id="bcd10-142">Een beschrijving van de tegel.</span><span class="sxs-lookup"><span data-stu-id="bcd10-142">A description of the tile.</span></span> |
   | <span data-ttu-id="bcd10-143">**Internetadres**</span><span class="sxs-lookup"><span data-stu-id="bcd10-143">**Internet address**</span></span> | <span data-ttu-id="bcd10-144">Voer de URL in voor de pagina Selfservice werknemer.</span><span class="sxs-lookup"><span data-stu-id="bcd10-144">Enter the URL to the employee self service page.</span></span> |
   | <span data-ttu-id="bcd10-145">**Tegelgrootte**</span><span class="sxs-lookup"><span data-stu-id="bcd10-145">**Tile size**</span></span> | <span data-ttu-id="bcd10-146">De grootte van de tegel: klein, normaal of groot.</span><span class="sxs-lookup"><span data-stu-id="bcd10-146">The size of the tile: Small, Medium, or Large.</span></span> |
   | <span data-ttu-id="bcd10-147">**Doel**</span><span class="sxs-lookup"><span data-stu-id="bcd10-147">**Target**</span></span> | <span data-ttu-id="bcd10-148">Geeft aan of de pagina in een nieuw venster of in het huidige venster moet worden geopend.</span><span class="sxs-lookup"><span data-stu-id="bcd10-148">Specifies whether the page should open in a new window or the current window.</span></span> |
   | <span data-ttu-id="bcd10-149">**Afbeelding voor tegelachtergrond**</span><span class="sxs-lookup"><span data-stu-id="bcd10-149">**Tile background image**</span></span> | <span data-ttu-id="bcd10-150">De URL van de afbeelding die moet worden gebruikt voor de tegel (optioneel).</span><span class="sxs-lookup"><span data-stu-id="bcd10-150">The URL of the image to use for the tile (optional).</span></span> |
   | <span data-ttu-id="bcd10-151">**Start**</span><span class="sxs-lookup"><span data-stu-id="bcd10-151">**Start**</span></span> | <span data-ttu-id="bcd10-152">De begindatum en -tijd waarop de tegel beschikbaar moet zijn.</span><span class="sxs-lookup"><span data-stu-id="bcd10-152">The beginning date and time the tile should be available.</span></span> |
   | <span data-ttu-id="bcd10-153">**End**</span><span class="sxs-lookup"><span data-stu-id="bcd10-153">**End**</span></span> | <span data-ttu-id="bcd10-154">De einddatum en -tijd waarop de tegel beschikbaar moet zijn.</span><span class="sxs-lookup"><span data-stu-id="bcd10-154">The end date and time the tile should be available.</span></span> |

4. <span data-ttu-id="bcd10-155">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="bcd10-155">Select **Save**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]