---
title: Werknemerselfservice configureren
description: In Microsoft Dynamics 365 Human Resources kunt u tegels configureren voor navigatie op het hoogste niveau in Selfservice werknemer.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 17918fc7b894929c92c54b59b7440ab8aef980bd
ms.sourcegitcommit: f38302b9430f2ab3efe91d0a7beff946bc610e8f
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/28/2020
ms.locfileid: "3092655"
---
# <a name="configure-employee-self-service"></a><span data-ttu-id="8a370-103">Werknemerselfservice configureren</span><span class="sxs-lookup"><span data-stu-id="8a370-103">Configure employee self service</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="8a370-104">In Microsoft Dynamics 365 Human Resources kunt u tegels configureren voor navigatie op het hoogste niveau in Selfservice werknemer.</span><span class="sxs-lookup"><span data-stu-id="8a370-104">In Microsoft Dynamics 365 Human Resources, you can configure tiles for top-level navigation in Employee self service.</span></span> <span data-ttu-id="8a370-105">Vergoedingsplantegels leiden gebruikers naar vergoedingsplannen waarvoor zij zich kunnen inschrijven.</span><span class="sxs-lookup"><span data-stu-id="8a370-105">Benefit plan tiles direct users to benefit plans that they are eligible to enroll in.</span></span>

## <a name="set-up-a-role-center-tile"></a><span data-ttu-id="8a370-106">Een tegel voor een rollencentrum instellen</span><span class="sxs-lookup"><span data-stu-id="8a370-106">Set up a role center tile</span></span>

1. <span data-ttu-id="8a370-107">Selecteer in het werkgebied **Vergoedingenbeheer** onder **Instellen** de optie **Parameters voor Selfservice werknemer**.</span><span class="sxs-lookup"><span data-stu-id="8a370-107">In the **Benefits management** workspace, under **Setup**, select **Employee self service parameters**.</span></span>

2. <span data-ttu-id="8a370-108">Selecteer het tabblad **Tegel voor rollencentrum instellen** en selecteer vervolgens **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="8a370-108">Select the **Role center tile setup** tab, and then select **New**.</span></span>

3. <span data-ttu-id="8a370-109">Geef de waarden op voor de volgende velden:</span><span class="sxs-lookup"><span data-stu-id="8a370-109">Specify values for the following fields:</span></span>

   | <span data-ttu-id="8a370-110">Veld</span><span class="sxs-lookup"><span data-stu-id="8a370-110">Field</span></span> | <span data-ttu-id="8a370-111">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="8a370-111">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="8a370-112">Tegel-id</span><span class="sxs-lookup"><span data-stu-id="8a370-112">Tile ID</span></span> | <span data-ttu-id="8a370-113">De unieke id voor de tegel.</span><span class="sxs-lookup"><span data-stu-id="8a370-113">The unique identifier for the tile.</span></span> |
   | <span data-ttu-id="8a370-114">Tekst van tegellabel</span><span class="sxs-lookup"><span data-stu-id="8a370-114">Tile label text</span></span> | <span data-ttu-id="8a370-115">De tekst die voor de tegel wordt weergegeven in Selfservice.</span><span class="sxs-lookup"><span data-stu-id="8a370-115">The text that will appear for the tile on Self-service.</span></span> |
   | <span data-ttu-id="8a370-116">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="8a370-116">Description</span></span> | <span data-ttu-id="8a370-117">Een beschrijving van de tegel.</span><span class="sxs-lookup"><span data-stu-id="8a370-117">A description of the tile.</span></span> |
   | <span data-ttu-id="8a370-118">Internetadres</span><span class="sxs-lookup"><span data-stu-id="8a370-118">Internet address</span></span> | <span data-ttu-id="8a370-119">Voer de URL in voor de pagina Selfservice werknemer.</span><span class="sxs-lookup"><span data-stu-id="8a370-119">Enter the URL to the employee self service page.</span></span> |
   | <span data-ttu-id="8a370-120">Tegelgrootte</span><span class="sxs-lookup"><span data-stu-id="8a370-120">Tile size</span></span> | <span data-ttu-id="8a370-121">De grootte van de tegel: klein, normaal of groot.</span><span class="sxs-lookup"><span data-stu-id="8a370-121">The size of the tile: Small, Medium, or Large.</span></span> |
   | <span data-ttu-id="8a370-122">Doel</span><span class="sxs-lookup"><span data-stu-id="8a370-122">Target</span></span> | <span data-ttu-id="8a370-123">Geeft aan of de pagina in een nieuw venster of in het huidige venster moet worden geopend.</span><span class="sxs-lookup"><span data-stu-id="8a370-123">Specifies whether the page should open in a new window or the current window.</span></span> |
   | <span data-ttu-id="8a370-124">Afbeelding voor tegelachtergrond</span><span class="sxs-lookup"><span data-stu-id="8a370-124">Tile background image</span></span> | <span data-ttu-id="8a370-125">De URL van de afbeelding die moet worden gebruikt voor de tegel (optioneel).</span><span class="sxs-lookup"><span data-stu-id="8a370-125">The URL of the image to use for the tile (optional).</span></span> |
   | <span data-ttu-id="8a370-126">Start</span><span class="sxs-lookup"><span data-stu-id="8a370-126">Start</span></span> | <span data-ttu-id="8a370-127">De begindatum en -tijd waarop de tegel beschikbaar moet zijn.</span><span class="sxs-lookup"><span data-stu-id="8a370-127">The beginning date and time the tile should be available.</span></span> |
   | <span data-ttu-id="8a370-128">End</span><span class="sxs-lookup"><span data-stu-id="8a370-128">End</span></span> | <span data-ttu-id="8a370-129">De einddatum en -tijd waarop de tegel beschikbaar moet zijn.</span><span class="sxs-lookup"><span data-stu-id="8a370-129">The end date and time the tile should be available.</span></span> |

4. <span data-ttu-id="8a370-130">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="8a370-130">Select **Save**.</span></span>

## <a name="set-up-a-benefit-plans-tile"></a><span data-ttu-id="8a370-131">Een tegel voor vergoedingsplannen instellen</span><span class="sxs-lookup"><span data-stu-id="8a370-131">Set up a benefit plans tile</span></span>

1. <span data-ttu-id="8a370-132">Selecteer in het werkgebied **Vergoedingenbeheer** onder **Instellen** de optie **Parameters voor Selfservice werknemer**.</span><span class="sxs-lookup"><span data-stu-id="8a370-132">In the **Benefits management** workspace, under **Setup**, select **Employee self service parameters**.</span></span>

2. <span data-ttu-id="8a370-133">Selecteer het tabblad **Tegel voor vergoedingsplannen instellen** en selecteer vervolgens **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="8a370-133">Select the **Benefit plans tile setup** tab, and then select **New**.</span></span>

3. <span data-ttu-id="8a370-134">Geef de waarden op voor de volgende velden:</span><span class="sxs-lookup"><span data-stu-id="8a370-134">Specify values for the following fields:</span></span>

   | <span data-ttu-id="8a370-135">Veld</span><span class="sxs-lookup"><span data-stu-id="8a370-135">Field</span></span> | <span data-ttu-id="8a370-136">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="8a370-136">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="8a370-137">Tegel-id</span><span class="sxs-lookup"><span data-stu-id="8a370-137">Tile ID</span></span> | <span data-ttu-id="8a370-138">De unieke id voor de tegel.</span><span class="sxs-lookup"><span data-stu-id="8a370-138">The unique identifier for the tile.</span></span> |
   | <span data-ttu-id="8a370-139">Tekst van tegellabel</span><span class="sxs-lookup"><span data-stu-id="8a370-139">Tile label text</span></span> | <span data-ttu-id="8a370-140">De tekst die voor de tegel wordt weergegeven in Selfservice.</span><span class="sxs-lookup"><span data-stu-id="8a370-140">The text that will appear for the tile on Self-service.</span></span> |
   | <span data-ttu-id="8a370-141">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="8a370-141">Description</span></span> | <span data-ttu-id="8a370-142">Een beschrijving van de tegel.</span><span class="sxs-lookup"><span data-stu-id="8a370-142">A description of the tile.</span></span> |
   | <span data-ttu-id="8a370-143">Internetadres</span><span class="sxs-lookup"><span data-stu-id="8a370-143">Internet address</span></span> | <span data-ttu-id="8a370-144">Voer de URL in voor de pagina Selfservice werknemer.</span><span class="sxs-lookup"><span data-stu-id="8a370-144">Enter the URL to the employee self service page.</span></span> |
   | <span data-ttu-id="8a370-145">Tegelgrootte</span><span class="sxs-lookup"><span data-stu-id="8a370-145">Tile size</span></span> | <span data-ttu-id="8a370-146">De grootte van de tegel: klein, normaal of groot.</span><span class="sxs-lookup"><span data-stu-id="8a370-146">The size of the tile: Small, Medium, or Large.</span></span> |
   | <span data-ttu-id="8a370-147">Doel</span><span class="sxs-lookup"><span data-stu-id="8a370-147">Target</span></span> | <span data-ttu-id="8a370-148">Geeft aan of de pagina in een nieuw venster of in het huidige venster moet worden geopend.</span><span class="sxs-lookup"><span data-stu-id="8a370-148">Specifies whether the page should open in a new window or the current window.</span></span> |
   | <span data-ttu-id="8a370-149">Afbeelding voor tegelachtergrond</span><span class="sxs-lookup"><span data-stu-id="8a370-149">Tile background image</span></span> | <span data-ttu-id="8a370-150">De URL van de afbeelding die moet worden gebruikt voor de tegel (optioneel).</span><span class="sxs-lookup"><span data-stu-id="8a370-150">The URL of the image to use for the tile (optional).</span></span> |
   | <span data-ttu-id="8a370-151">Start</span><span class="sxs-lookup"><span data-stu-id="8a370-151">Start</span></span> | <span data-ttu-id="8a370-152">De begindatum en -tijd waarop de tegel beschikbaar moet zijn.</span><span class="sxs-lookup"><span data-stu-id="8a370-152">The beginning date and time the tile should be available.</span></span> |
   | <span data-ttu-id="8a370-153">End</span><span class="sxs-lookup"><span data-stu-id="8a370-153">End</span></span> | <span data-ttu-id="8a370-154">De einddatum en -tijd waarop de tegel beschikbaar moet zijn.</span><span class="sxs-lookup"><span data-stu-id="8a370-154">The end date and time the tile should be available.</span></span> |

4. <span data-ttu-id="8a370-155">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="8a370-155">Select **Save**.</span></span>

## <a name="set-up-a-flex-credit-plan-tile"></a><span data-ttu-id="8a370-156">Een tegel voor een flex-kredietplan instellen</span><span class="sxs-lookup"><span data-stu-id="8a370-156">Set up a flex credit plan tile</span></span>

1. <span data-ttu-id="8a370-157">Selecteer in het werkgebied **Vergoedingenbeheer** onder **Instellen** de optie **Parameters voor Selfservice werknemer**.</span><span class="sxs-lookup"><span data-stu-id="8a370-157">In the **Benefits management** workspace, under **Setup**, select **Employee self service parameters**.</span></span>

2. <span data-ttu-id="8a370-158">Selecteer het tabblad **Tegel voor flex-kredietplan instellen** en selecteer vervolgens **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="8a370-158">Select the **Flex credit plan tile setup** tab, and then select **New**.</span></span>

3. <span data-ttu-id="8a370-159">Geef de waarden op voor de volgende velden:</span><span class="sxs-lookup"><span data-stu-id="8a370-159">Specify values for the following fields:</span></span>

   | <span data-ttu-id="8a370-160">Veld</span><span class="sxs-lookup"><span data-stu-id="8a370-160">Field</span></span> | <span data-ttu-id="8a370-161">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="8a370-161">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="8a370-162">Tegel-id</span><span class="sxs-lookup"><span data-stu-id="8a370-162">Tile ID</span></span> | <span data-ttu-id="8a370-163">De unieke id voor de tegel.</span><span class="sxs-lookup"><span data-stu-id="8a370-163">The unique identifier for the tile.</span></span> |
   | <span data-ttu-id="8a370-164">Tekst van tegellabel</span><span class="sxs-lookup"><span data-stu-id="8a370-164">Tile label text</span></span> | <span data-ttu-id="8a370-165">De tekst die voor de tegel wordt weergegeven in Selfservice.</span><span class="sxs-lookup"><span data-stu-id="8a370-165">The text that will appear for the tile on Self-service.</span></span> |
   | <span data-ttu-id="8a370-166">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="8a370-166">Description</span></span> | <span data-ttu-id="8a370-167">Een beschrijving van de tegel.</span><span class="sxs-lookup"><span data-stu-id="8a370-167">A description of the tile.</span></span> |
   | <span data-ttu-id="8a370-168">Internetadres</span><span class="sxs-lookup"><span data-stu-id="8a370-168">Internet address</span></span> | <span data-ttu-id="8a370-169">Voer de URL in voor de pagina Selfservice werknemer.</span><span class="sxs-lookup"><span data-stu-id="8a370-169">Enter the URL to the employee self service page.</span></span> |
   | <span data-ttu-id="8a370-170">Tegelgrootte</span><span class="sxs-lookup"><span data-stu-id="8a370-170">Tile size</span></span> | <span data-ttu-id="8a370-171">De grootte van de tegel: klein, normaal of groot.</span><span class="sxs-lookup"><span data-stu-id="8a370-171">The size of the tile: Small, Medium, or Large.</span></span> |
   | <span data-ttu-id="8a370-172">Doel</span><span class="sxs-lookup"><span data-stu-id="8a370-172">Target</span></span> | <span data-ttu-id="8a370-173">Geeft aan of de pagina in een nieuw venster of in het huidige venster moet worden geopend.</span><span class="sxs-lookup"><span data-stu-id="8a370-173">Specifies whether the page should open in a new window or the current window.</span></span> |
   | <span data-ttu-id="8a370-174">Afbeelding voor tegelachtergrond</span><span class="sxs-lookup"><span data-stu-id="8a370-174">Tile background image</span></span> | <span data-ttu-id="8a370-175">De URL van de afbeelding die moet worden gebruikt voor de tegel (optioneel).</span><span class="sxs-lookup"><span data-stu-id="8a370-175">The URL of the image to use for the tile (optional).</span></span> |
   | <span data-ttu-id="8a370-176">Start</span><span class="sxs-lookup"><span data-stu-id="8a370-176">Start</span></span> | <span data-ttu-id="8a370-177">De begindatum en -tijd waarop de tegel beschikbaar moet zijn.</span><span class="sxs-lookup"><span data-stu-id="8a370-177">The beginning date and time the tile should be available.</span></span> |
   | <span data-ttu-id="8a370-178">End</span><span class="sxs-lookup"><span data-stu-id="8a370-178">End</span></span> | <span data-ttu-id="8a370-179">De einddatum en -tijd waarop de tegel beschikbaar moet zijn.</span><span class="sxs-lookup"><span data-stu-id="8a370-179">The end date and time the tile should be available.</span></span> |

4. <span data-ttu-id="8a370-180">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="8a370-180">Select **Save**.</span></span>
