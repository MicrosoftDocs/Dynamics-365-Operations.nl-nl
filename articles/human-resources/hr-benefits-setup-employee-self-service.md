---
title: Selfservice werknemers configureren
description: ''
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
ms.openlocfilehash: e44a35071b8d0987e6c949fb11312204317b44a1
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/03/2020
ms.locfileid: "3008629"
---
# <a name="configure-employee-self-service"></a><span data-ttu-id="85db1-102">Selfservice werknemers configureren</span><span class="sxs-lookup"><span data-stu-id="85db1-102">Configure employee self service</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="85db1-103">In Microsoft Dynamics 365 Human Resources kunt u tegels configureren voor navigatie op het hoogste niveau in Selfservice werknemer.</span><span class="sxs-lookup"><span data-stu-id="85db1-103">In Microsoft Dynamics 365 Human Resources, you can configure tiles for top-level navigation in Employee self service.</span></span> <span data-ttu-id="85db1-104">Vergoedingsplantegels leiden gebruikers naar vergoedingsplannen waarvoor zij zich kunnen inschrijven.</span><span class="sxs-lookup"><span data-stu-id="85db1-104">Benefit plan tiles direct users to benefit plans that they are eligible to enroll in.</span></span>

## <a name="set-up-a-role-center-tile"></a><span data-ttu-id="85db1-105">Een tegel voor een rollencentrum instellen</span><span class="sxs-lookup"><span data-stu-id="85db1-105">Set up a role center tile</span></span>

1. <span data-ttu-id="85db1-106">Selecteer in het werkgebied **Vergoedingenbeheer** onder **Instellen** de optie **Parameters voor Selfservice werknemer**.</span><span class="sxs-lookup"><span data-stu-id="85db1-106">In the **Benefits management** workspace, under **Setup**, select **Employee self service parameters**.</span></span>

2. <span data-ttu-id="85db1-107">Selecteer het tabblad **Tegel voor rollencentrum instellen** en selecteer vervolgens **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="85db1-107">Select the **Role center tile setup** tab, and then select **New**.</span></span>

3. <span data-ttu-id="85db1-108">Geef de waarden op voor de volgende velden:</span><span class="sxs-lookup"><span data-stu-id="85db1-108">Specify values for the following fields:</span></span>

   | <span data-ttu-id="85db1-109">Veld</span><span class="sxs-lookup"><span data-stu-id="85db1-109">Field</span></span> | <span data-ttu-id="85db1-110">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="85db1-110">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="85db1-111">Tegel-id</span><span class="sxs-lookup"><span data-stu-id="85db1-111">Tile ID</span></span> | <span data-ttu-id="85db1-112">De unieke id voor de tegel.</span><span class="sxs-lookup"><span data-stu-id="85db1-112">The unique identifier for the tile.</span></span> |
   | <span data-ttu-id="85db1-113">Tekst van tegellabel</span><span class="sxs-lookup"><span data-stu-id="85db1-113">Tile label text</span></span> | <span data-ttu-id="85db1-114">De tekst die voor de tegel wordt weergegeven in Selfservice.</span><span class="sxs-lookup"><span data-stu-id="85db1-114">The text that will appear for the tile on Self-service.</span></span> |
   | <span data-ttu-id="85db1-115">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="85db1-115">Description</span></span> | <span data-ttu-id="85db1-116">Een beschrijving van de tegel.</span><span class="sxs-lookup"><span data-stu-id="85db1-116">A description of the tile.</span></span> |
   | <span data-ttu-id="85db1-117">Internetadres</span><span class="sxs-lookup"><span data-stu-id="85db1-117">Internet address</span></span> | <span data-ttu-id="85db1-118">Voer de URL in voor de pagina Selfservice werknemer.</span><span class="sxs-lookup"><span data-stu-id="85db1-118">Enter the URL to the employee self service page.</span></span> |
   | <span data-ttu-id="85db1-119">Tegelgrootte</span><span class="sxs-lookup"><span data-stu-id="85db1-119">Tile size</span></span> | <span data-ttu-id="85db1-120">De grootte van de tegel: klein, normaal of groot.</span><span class="sxs-lookup"><span data-stu-id="85db1-120">The size of the tile: Small, Medium, or Large.</span></span> |
   | <span data-ttu-id="85db1-121">Doel</span><span class="sxs-lookup"><span data-stu-id="85db1-121">Target</span></span> | <span data-ttu-id="85db1-122">Geeft aan of de pagina in een nieuw venster of in het huidige venster moet worden geopend.</span><span class="sxs-lookup"><span data-stu-id="85db1-122">Specifies whether the page should open in a new window or the current window.</span></span> |
   | <span data-ttu-id="85db1-123">Afbeelding voor tegelachtergrond</span><span class="sxs-lookup"><span data-stu-id="85db1-123">Tile background image</span></span> | <span data-ttu-id="85db1-124">De URL van de afbeelding die moet worden gebruikt voor de tegel (optioneel).</span><span class="sxs-lookup"><span data-stu-id="85db1-124">The URL of the image to use for the tile (optional).</span></span> |
   | <span data-ttu-id="85db1-125">Start</span><span class="sxs-lookup"><span data-stu-id="85db1-125">Start</span></span> | <span data-ttu-id="85db1-126">De begindatum en -tijd waarop de tegel beschikbaar moet zijn.</span><span class="sxs-lookup"><span data-stu-id="85db1-126">The beginning date and time the tile should be available.</span></span> |
   | <span data-ttu-id="85db1-127">End</span><span class="sxs-lookup"><span data-stu-id="85db1-127">End</span></span> | <span data-ttu-id="85db1-128">De einddatum en -tijd waarop de tegel beschikbaar moet zijn.</span><span class="sxs-lookup"><span data-stu-id="85db1-128">The end date and time the tile should be available.</span></span> |

4. <span data-ttu-id="85db1-129">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="85db1-129">Select **Save**.</span></span>

## <a name="set-up-a-benefit-plans-tile"></a><span data-ttu-id="85db1-130">Een tegel voor vergoedingsplannen instellen</span><span class="sxs-lookup"><span data-stu-id="85db1-130">Set up a benefit plans tile</span></span>

1. <span data-ttu-id="85db1-131">Selecteer in het werkgebied **Vergoedingenbeheer** onder **Instellen** de optie **Parameters voor Selfservice werknemer**.</span><span class="sxs-lookup"><span data-stu-id="85db1-131">In the **Benefits management** workspace, under **Setup**, select **Employee self service parameters**.</span></span>

2. <span data-ttu-id="85db1-132">Selecteer het tabblad **Tegel voor vergoedingsplannen instellen** en selecteer vervolgens **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="85db1-132">Select the **Benefit plans tile setup** tab, and then select **New**.</span></span>

3. <span data-ttu-id="85db1-133">Geef de waarden op voor de volgende velden:</span><span class="sxs-lookup"><span data-stu-id="85db1-133">Specify values for the following fields:</span></span>

   | <span data-ttu-id="85db1-134">Veld</span><span class="sxs-lookup"><span data-stu-id="85db1-134">Field</span></span> | <span data-ttu-id="85db1-135">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="85db1-135">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="85db1-136">Tegel-id</span><span class="sxs-lookup"><span data-stu-id="85db1-136">Tile ID</span></span> | <span data-ttu-id="85db1-137">De unieke id voor de tegel.</span><span class="sxs-lookup"><span data-stu-id="85db1-137">The unique identifier for the tile.</span></span> |
   | <span data-ttu-id="85db1-138">Tekst van tegellabel</span><span class="sxs-lookup"><span data-stu-id="85db1-138">Tile label text</span></span> | <span data-ttu-id="85db1-139">De tekst die voor de tegel wordt weergegeven in Selfservice.</span><span class="sxs-lookup"><span data-stu-id="85db1-139">The text that will appear for the tile on Self-service.</span></span> |
   | <span data-ttu-id="85db1-140">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="85db1-140">Description</span></span> | <span data-ttu-id="85db1-141">Een beschrijving van de tegel.</span><span class="sxs-lookup"><span data-stu-id="85db1-141">A description of the tile.</span></span> |
   | <span data-ttu-id="85db1-142">Internetadres</span><span class="sxs-lookup"><span data-stu-id="85db1-142">Internet address</span></span> | <span data-ttu-id="85db1-143">Voer de URL in voor de pagina Selfservice werknemer.</span><span class="sxs-lookup"><span data-stu-id="85db1-143">Enter the URL to the employee self service page.</span></span> |
   | <span data-ttu-id="85db1-144">Tegelgrootte</span><span class="sxs-lookup"><span data-stu-id="85db1-144">Tile size</span></span> | <span data-ttu-id="85db1-145">De grootte van de tegel: klein, normaal of groot.</span><span class="sxs-lookup"><span data-stu-id="85db1-145">The size of the tile: Small, Medium, or Large.</span></span> |
   | <span data-ttu-id="85db1-146">Doel</span><span class="sxs-lookup"><span data-stu-id="85db1-146">Target</span></span> | <span data-ttu-id="85db1-147">Geeft aan of de pagina in een nieuw venster of in het huidige venster moet worden geopend.</span><span class="sxs-lookup"><span data-stu-id="85db1-147">Specifies whether the page should open in a new window or the current window.</span></span> |
   | <span data-ttu-id="85db1-148">Afbeelding voor tegelachtergrond</span><span class="sxs-lookup"><span data-stu-id="85db1-148">Tile background image</span></span> | <span data-ttu-id="85db1-149">De URL van de afbeelding die moet worden gebruikt voor de tegel (optioneel).</span><span class="sxs-lookup"><span data-stu-id="85db1-149">The URL of the image to use for the tile (optional).</span></span> |
   | <span data-ttu-id="85db1-150">Start</span><span class="sxs-lookup"><span data-stu-id="85db1-150">Start</span></span> | <span data-ttu-id="85db1-151">De begindatum en -tijd waarop de tegel beschikbaar moet zijn.</span><span class="sxs-lookup"><span data-stu-id="85db1-151">The beginning date and time the tile should be available.</span></span> |
   | <span data-ttu-id="85db1-152">End</span><span class="sxs-lookup"><span data-stu-id="85db1-152">End</span></span> | <span data-ttu-id="85db1-153">De einddatum en -tijd waarop de tegel beschikbaar moet zijn.</span><span class="sxs-lookup"><span data-stu-id="85db1-153">The end date and time the tile should be available.</span></span> |

4. <span data-ttu-id="85db1-154">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="85db1-154">Select **Save**.</span></span>

## <a name="set-up-a-flex-credit-plan-tile"></a><span data-ttu-id="85db1-155">Een tegel voor een flex-kredietplan instellen</span><span class="sxs-lookup"><span data-stu-id="85db1-155">Set up a flex credit plan tile</span></span>

1. <span data-ttu-id="85db1-156">Selecteer in het werkgebied **Vergoedingenbeheer** onder **Instellen** de optie **Parameters voor Selfservice werknemer**.</span><span class="sxs-lookup"><span data-stu-id="85db1-156">In the **Benefits management** workspace, under **Setup**, select **Employee self service parameters**.</span></span>

2. <span data-ttu-id="85db1-157">Selecteer het tabblad **Tegel voor flex-kredietplan instellen** en selecteer vervolgens **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="85db1-157">Select the **Flex credit plan tile setup** tab, and then select **New**.</span></span>

3. <span data-ttu-id="85db1-158">Geef de waarden op voor de volgende velden:</span><span class="sxs-lookup"><span data-stu-id="85db1-158">Specify values for the following fields:</span></span>

   | <span data-ttu-id="85db1-159">Veld</span><span class="sxs-lookup"><span data-stu-id="85db1-159">Field</span></span> | <span data-ttu-id="85db1-160">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="85db1-160">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="85db1-161">Tegel-id</span><span class="sxs-lookup"><span data-stu-id="85db1-161">Tile ID</span></span> | <span data-ttu-id="85db1-162">De unieke id voor de tegel.</span><span class="sxs-lookup"><span data-stu-id="85db1-162">The unique identifier for the tile.</span></span> |
   | <span data-ttu-id="85db1-163">Tekst van tegellabel</span><span class="sxs-lookup"><span data-stu-id="85db1-163">Tile label text</span></span> | <span data-ttu-id="85db1-164">De tekst die voor de tegel wordt weergegeven in Selfservice.</span><span class="sxs-lookup"><span data-stu-id="85db1-164">The text that will appear for the tile on Self-service.</span></span> |
   | <span data-ttu-id="85db1-165">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="85db1-165">Description</span></span> | <span data-ttu-id="85db1-166">Een beschrijving van de tegel.</span><span class="sxs-lookup"><span data-stu-id="85db1-166">A description of the tile.</span></span> |
   | <span data-ttu-id="85db1-167">Internetadres</span><span class="sxs-lookup"><span data-stu-id="85db1-167">Internet address</span></span> | <span data-ttu-id="85db1-168">Voer de URL in voor de pagina Selfservice werknemer.</span><span class="sxs-lookup"><span data-stu-id="85db1-168">Enter the URL to the employee self service page.</span></span> |
   | <span data-ttu-id="85db1-169">Tegelgrootte</span><span class="sxs-lookup"><span data-stu-id="85db1-169">Tile size</span></span> | <span data-ttu-id="85db1-170">De grootte van de tegel: klein, normaal of groot.</span><span class="sxs-lookup"><span data-stu-id="85db1-170">The size of the tile: Small, Medium, or Large.</span></span> |
   | <span data-ttu-id="85db1-171">Doel</span><span class="sxs-lookup"><span data-stu-id="85db1-171">Target</span></span> | <span data-ttu-id="85db1-172">Geeft aan of de pagina in een nieuw venster of in het huidige venster moet worden geopend.</span><span class="sxs-lookup"><span data-stu-id="85db1-172">Specifies whether the page should open in a new window or the current window.</span></span> |
   | <span data-ttu-id="85db1-173">Afbeelding voor tegelachtergrond</span><span class="sxs-lookup"><span data-stu-id="85db1-173">Tile background image</span></span> | <span data-ttu-id="85db1-174">De URL van de afbeelding die moet worden gebruikt voor de tegel (optioneel).</span><span class="sxs-lookup"><span data-stu-id="85db1-174">The URL of the image to use for the tile (optional).</span></span> |
   | <span data-ttu-id="85db1-175">Start</span><span class="sxs-lookup"><span data-stu-id="85db1-175">Start</span></span> | <span data-ttu-id="85db1-176">De begindatum en -tijd waarop de tegel beschikbaar moet zijn.</span><span class="sxs-lookup"><span data-stu-id="85db1-176">The beginning date and time the tile should be available.</span></span> |
   | <span data-ttu-id="85db1-177">End</span><span class="sxs-lookup"><span data-stu-id="85db1-177">End</span></span> | <span data-ttu-id="85db1-178">De einddatum en -tijd waarop de tegel beschikbaar moet zijn.</span><span class="sxs-lookup"><span data-stu-id="85db1-178">The end date and time the tile should be available.</span></span> |

4. <span data-ttu-id="85db1-179">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="85db1-179">Select **Save**.</span></span>
