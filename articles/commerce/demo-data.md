---
title: Schermindelingen met demonstratiegegevens in Modern POS (MPOS) en Cloud POS
description: Dit onderwerp bevat informatie over de schermindelingen die zijn opgenomen in de voorbeeldgegevensset voor de POS-ervaringen (Point Of Sale) in Dynamics 365 Commerce.
author: zlinster
manager: AnnBe
ms.date: 10/05/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailTillLayout
audience: Application user
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: zlinster
ms.search.validFrom: 2017-10-05
ms.dyn365.ops.version: Retail April 2017 update
ms.openlocfilehash: 7956eece1a77951795a3f5f66067a2ecfacf3450
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/01/2020
ms.locfileid: "3022085"
---
# <a name="demo-data-screen-layouts-in-modern-pos-mpos-and-cloud-pos"></a><span data-ttu-id="97a8e-103">Schermindelingen met demonstratiegegevens in Modern POS (MPOS) en Cloud POS</span><span class="sxs-lookup"><span data-stu-id="97a8e-103">Demo data screen layouts in Modern POS (MPOS) and Cloud POS</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="97a8e-104">Dit onderwerp bevat informatie over de schermindelingen die zijn opgenomen in de voorbeeldgegevensset voor de POS-ervaringen (Point Of Sale) in Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="97a8e-104">This topic provides information about the screen layouts that are included with the demo data set for the point of sale (POS) experiences in Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="97a8e-105">Overzicht</span><span class="sxs-lookup"><span data-stu-id="97a8e-105">Overview</span></span>

<span data-ttu-id="97a8e-106">De voorbeeldschermindelingen die zijn opgenomen in de Commerce-demonstratiegegevens bieden inhoud die is geoptimaliseerd voor verschillende segmenten van de detailhandel, winkelmedewerkerrollen en apparaten.</span><span class="sxs-lookup"><span data-stu-id="97a8e-106">The sample screen layouts that are included with Commerce demo data provide content that is optimized for various retail segments, store worker roles, and devices.</span></span> <span data-ttu-id="97a8e-107">Eén indeling kan verschillende indelingsformaten en combinaties van knoppenrasters bevatten om in de behoefte te kunnen blijven voorzien wanneer werknemers tussen apparaten en stations schakelen.</span><span class="sxs-lookup"><span data-stu-id="97a8e-107">A single layout can contain several layout sizes and combinations of button grids, to help ensure coverage as store workers move between devices and stations.</span></span> <span data-ttu-id="97a8e-108">Dit onderwerp biedt meer informatie over de verschillen tussen deze indelingen, de mogelijkheden die ze bieden en de algehele ervaring die ze leveren.</span><span class="sxs-lookup"><span data-stu-id="97a8e-108">This topic highlights the differences between these layouts, the operations that they provide, and the overall experiences that they deliver.</span></span>

![Apparaatonafhankelijke demonstratiegegevensindelingen](../commerce/media/demo-screen-layouts-fig-1-1.png)

## <a name="anatomy-of-a-screen-layout-id"></a><span data-ttu-id="97a8e-110">Anatomie van een schermindelings-id</span><span class="sxs-lookup"><span data-stu-id="97a8e-110">Anatomy of a screen layout ID</span></span>

<span data-ttu-id="97a8e-111">Schermindelingen vindt u via **Retail en Commerce** \> **Kanaalinstellingen** \> **POS-instellingen** \> **POS** \> **Schermindelingen**.</span><span class="sxs-lookup"><span data-stu-id="97a8e-111">To find screen layouts, go to **Retail and Commerce** \> **Channel setup** \> **POS setup** \> **POS** \> **Screen layouts**.</span></span>

![Pagina Schermindelingen](../commerce/media/demo-screen-layouts-fig-2-1.png)

<span data-ttu-id="97a8e-113">Schermindeling-id's kunnen uit maximaal 10 tekens bestaan.</span><span class="sxs-lookup"><span data-stu-id="97a8e-113">Screen layout IDs can have a maximum of 10 characters.</span></span> <span data-ttu-id="97a8e-114">De id is een tekenreeks die uit drie soorten informatie bestaat, in de volgende volgorde:</span><span class="sxs-lookup"><span data-stu-id="97a8e-114">The ID is a string that consists of three pieces of information, in this order:</span></span>

1. <span data-ttu-id="97a8e-115">Bedrijf</span><span class="sxs-lookup"><span data-stu-id="97a8e-115">Company</span></span>
2. <span data-ttu-id="97a8e-116">Indelingsversie</span><span class="sxs-lookup"><span data-stu-id="97a8e-116">Layout version</span></span>
3. <span data-ttu-id="97a8e-117">Persona</span><span class="sxs-lookup"><span data-stu-id="97a8e-117">Persona</span></span>

### <a name="company"></a><span data-ttu-id="97a8e-118">Bedrijf</span><span class="sxs-lookup"><span data-stu-id="97a8e-118">Company</span></span>

| <span data-ttu-id="97a8e-119">Brief</span><span class="sxs-lookup"><span data-stu-id="97a8e-119">Letter</span></span> | <span data-ttu-id="97a8e-120">Bedrijf</span><span class="sxs-lookup"><span data-stu-id="97a8e-120">Company</span></span>         |
|--------|-----------------|
| <span data-ttu-id="97a8e-121">V</span><span class="sxs-lookup"><span data-stu-id="97a8e-121">A</span></span>      | <span data-ttu-id="97a8e-122">Adventure Works</span><span class="sxs-lookup"><span data-stu-id="97a8e-122">Adventure Works</span></span> |
| <span data-ttu-id="97a8e-123">F</span><span class="sxs-lookup"><span data-stu-id="97a8e-123">F</span></span>      | <span data-ttu-id="97a8e-124">Fabrikam</span><span class="sxs-lookup"><span data-stu-id="97a8e-124">Fabrikam</span></span>        |
| <span data-ttu-id="97a8e-125">E</span><span class="sxs-lookup"><span data-stu-id="97a8e-125">C</span></span>      | <span data-ttu-id="97a8e-126">Contoso</span><span class="sxs-lookup"><span data-stu-id="97a8e-126">Contoso</span></span>         |

### <a name="layout-version"></a><span data-ttu-id="97a8e-127">Indelingsversie</span><span class="sxs-lookup"><span data-stu-id="97a8e-127">Layout version</span></span>

| <span data-ttu-id="97a8e-128">Versienummer</span><span class="sxs-lookup"><span data-stu-id="97a8e-128">Version number</span></span> | <span data-ttu-id="97a8e-129">Omschrijving</span><span class="sxs-lookup"><span data-stu-id="97a8e-129">Description</span></span>                                                                                |
|----------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="97a8e-130">3</span><span class="sxs-lookup"><span data-stu-id="97a8e-130">3</span></span>              | <span data-ttu-id="97a8e-131">De basisversie die ondersteuning biedt voor meerdere schermformaten voor verschillende apparaten en hoogte-breedteverhoudingen</span><span class="sxs-lookup"><span data-stu-id="97a8e-131">The base version that supports multiple screen sizes for various devices and aspect ratios</span></span> |
| <span data-ttu-id="97a8e-132">3.1</span><span class="sxs-lookup"><span data-stu-id="97a8e-132">3.1</span></span>            | <span data-ttu-id="97a8e-133">De basisversie met extra ondersteuning voor het deelvenster **Aanbevolen producten**</span><span class="sxs-lookup"><span data-stu-id="97a8e-133">The base version that has additional support for the **Recommended products** panel</span></span>        |

### <a name="persona"></a><span data-ttu-id="97a8e-134">Persona</span><span class="sxs-lookup"><span data-stu-id="97a8e-134">Persona</span></span>

| <span data-ttu-id="97a8e-135">Afkorting</span><span class="sxs-lookup"><span data-stu-id="97a8e-135">Abbreviation</span></span> | <span data-ttu-id="97a8e-136">Persona</span><span class="sxs-lookup"><span data-stu-id="97a8e-136">Persona</span></span>       | <span data-ttu-id="97a8e-137">Inhoud</span><span class="sxs-lookup"><span data-stu-id="97a8e-137">Contents</span></span> |
|--------------|---------------|----------|
| <span data-ttu-id="97a8e-138">KAS</span><span class="sxs-lookup"><span data-stu-id="97a8e-138">CSH</span></span>          | <span data-ttu-id="97a8e-139">Kassier</span><span class="sxs-lookup"><span data-stu-id="97a8e-139">Cashier</span></span>       | <span data-ttu-id="97a8e-140">Kassierindelingen bevatten alle transactiegerelateerde bewerkingen, zoals klantorders, retouren, kortingen, ongeldig gemaakte transacties en geschenkbonnen.</span><span class="sxs-lookup"><span data-stu-id="97a8e-140">Cashier layouts include all transaction-related operations, such as customer orders, returns, discounts, voids, and gift cards.</span></span> <span data-ttu-id="97a8e-141">Deze indelingen bevatten ook dagelijkse taken voor voorraadbeheer, zoals prijscontroles, voorraadzoekopdrachten en voorraadtellingen.</span><span class="sxs-lookup"><span data-stu-id="97a8e-141">These layouts also include daily tasks for inventory management, such price checks, inventory lookups, and stock counts.</span></span> <span data-ttu-id="97a8e-142">Daarnaast zijn algemene functies voor ploegenbeheer beschikbaar voor beginbedragen, het uitstellen van diensten en de tijdklok.</span><span class="sxs-lookup"><span data-stu-id="97a8e-142">Basic shift management is also provided for start amounts, suspending shifts, and time clock.</span></span> |
| <span data-ttu-id="97a8e-143">MGR</span><span class="sxs-lookup"><span data-stu-id="97a8e-143">MGR</span></span>          | <span data-ttu-id="97a8e-144">Winkelmanager</span><span class="sxs-lookup"><span data-stu-id="97a8e-144">Store Manager</span></span> | <span data-ttu-id="97a8e-145">Winkelmanagerindelingen bevatten alle transactiegerelateerde bewerkingen die ook te vinden zijn in de indelingen voor kassiers en bevatten daarnaast btw-overschrijvingen.</span><span class="sxs-lookup"><span data-stu-id="97a8e-145">Store Manager layouts include all transaction-related operations that are found in the Cashier layouts but also include tax overrides.</span></span> <span data-ttu-id="97a8e-146">Deze indelingen bevatten ook dagelijkse taken voor voorraadbeheer, zoals prijscontroles, voorraadzoekopdrachten en voorraadtellingen.</span><span class="sxs-lookup"><span data-stu-id="97a8e-146">These layouts also include daily tasks for inventory management, such as price checks, inventory lookups, and stock counts.</span></span> <span data-ttu-id="97a8e-147">Er zijn functies voor ploegenbeheer beschikbaar voor het starten, uitstellen en sluiten van diensten.</span><span class="sxs-lookup"><span data-stu-id="97a8e-147">Shift management is provided for starting, suspending, and closing shifts.</span></span> <span data-ttu-id="97a8e-148">Daarnaast bevatten de indelingen ladebewerkingen voor opnames, verwijderingen, kascontroles en kluis- en bankstortingen.</span><span class="sxs-lookup"><span data-stu-id="97a8e-148">Additionally, the layouts include drawer operations for entries, removals, tender declarations, and safe and bank drops.</span></span> <span data-ttu-id="97a8e-149">Ten slotte bieden deze indelingen toegang tot prestatierapporten en kunnen er X- en Z-rapporten worden afgedrukt.</span><span class="sxs-lookup"><span data-stu-id="97a8e-149">Finally, these layouts include access to performance reports, and enable X and Z reports to be printed.</span></span> |
| <span data-ttu-id="97a8e-150">MMW</span><span class="sxs-lookup"><span data-stu-id="97a8e-150">STK</span></span>          | <span data-ttu-id="97a8e-151">Magazijnmedewerker</span><span class="sxs-lookup"><span data-stu-id="97a8e-151">Stock Clerk</span></span>   | <span data-ttu-id="97a8e-152">Indelingen voor magazijnmedewerkers zijn geoptimaliseerd voor voorraadbeheer.</span><span class="sxs-lookup"><span data-stu-id="97a8e-152">Stock Clerk layouts are optimized for inventory management.</span></span> <span data-ttu-id="97a8e-153">Deze bieden toegang tot dagelijkse taken voor prijscontroles, voorraadzoekopdrachten, orderverzameling en ontvangst, voorraadtellingen en kitdemontage.</span><span class="sxs-lookup"><span data-stu-id="97a8e-153">They include access to daily tasks for price checks, inventory lookups, picking and receiving, stock counts, and kit disassembly.</span></span> <span data-ttu-id="97a8e-154">Deze indelingen bieden ook basisbewerkingen voor ploegen, voor de tijdklok en het uitstellen van diensten.</span><span class="sxs-lookup"><span data-stu-id="97a8e-154">These layouts also provide basic shift operations for time clock and suspending shifts.</span></span> <span data-ttu-id="97a8e-155">Hoewel deze indelingen hoofdzakelijk voor backofficetaken bedoeld zijn, kunnen magazijnmedewerkers dezelfde bewerkingen als kassiers uitvoeren voor transactieschermen.</span><span class="sxs-lookup"><span data-stu-id="97a8e-155">Although these layouts are intended mainly for back-office tasks, stock clerks have the same operations as cashiers for transaction screens.</span></span> |

### <a name="example-layout"></a><span data-ttu-id="97a8e-156">Voorbeeldindeling</span><span class="sxs-lookup"><span data-stu-id="97a8e-156">Example layout</span></span>

<span data-ttu-id="97a8e-157">Hier is een voorbeeld van een schermindelings-id voor het bedrijf Fabrikam, indelingsversie 3, en de persona Winkelmanager:</span><span class="sxs-lookup"><span data-stu-id="97a8e-157">Here is an example of a screen layout ID for the Fabrikam company, layout version 3, and the Store Manager persona:</span></span>

<span data-ttu-id="97a8e-158">F3MGR</span><span class="sxs-lookup"><span data-stu-id="97a8e-158">F3MGR</span></span>

<span data-ttu-id="97a8e-159">In de volgende afbeelding wordt een voorbeeld van het welkomstscherm voor een winkelmanager van Fabrikam weergegeven.</span><span class="sxs-lookup"><span data-stu-id="97a8e-159">The following illustration shows an example of the Welcome screen for a Fabrikam store manager.</span></span>

![Welkomstscherm voor de winkelmanager van Fabrikam](../commerce/media/demo-screen-layouts-fig-2-2.png)

## <a name="layout-sizes"></a><span data-ttu-id="97a8e-161">Indelingsgrootten</span><span class="sxs-lookup"><span data-stu-id="97a8e-161">Layout sizes</span></span>

### <a name="full-vs-compact-layouts"></a><span data-ttu-id="97a8e-162">Volledige versus compacte indelingen</span><span class="sxs-lookup"><span data-stu-id="97a8e-162">Full vs. compact layouts</span></span>

<span data-ttu-id="97a8e-163">Een schermindeling kan configuraties voor zowel volledige als compacte apparaten bevatten.</span><span class="sxs-lookup"><span data-stu-id="97a8e-163">A screen layout can have configurations for both full devices and compact devices.</span></span> <span data-ttu-id="97a8e-164">Daarom kan een gebruiker worden toegewezen aan één schermindeling die werkt op verschillende afmetingen en vormfactoren in de winkel.</span><span class="sxs-lookup"><span data-stu-id="97a8e-164">Therefore, a user can be assigned to a single screen layout that will work across various sizes and form factors in the store.</span></span>

- <span data-ttu-id="97a8e-165">**Modern POS - volledig**: volledige indelingen zijn normaal gesproken het meest geschikt voor grotere beeldschermen, zoals computerbeeldschermen en tablets.</span><span class="sxs-lookup"><span data-stu-id="97a8e-165">**Modern POS - Full** – Typically, full layouts are best used for larger displays, such as desktop computer monitors or tablets.</span></span> <span data-ttu-id="97a8e-166">Gebruikers kunnen de UI-elementen in de indeling selecteren, de grootte en positie van die elementen opgeven en hun gedetailleerde eigenschappen configureren.</span><span class="sxs-lookup"><span data-stu-id="97a8e-166">Users can select the UI elements that the layout includes, specify the size and placement of those elements, and configure their detailed properties.</span></span> <span data-ttu-id="97a8e-167">Volledige indelingen ondersteunen zowel staande (portrait) als liggende (landscape) configuraties.</span><span class="sxs-lookup"><span data-stu-id="97a8e-167">Full layouts support both portrait and landscape configurations.</span></span>
- <span data-ttu-id="97a8e-168">**Modern POS - compact**: compacte indelingen zijn normaal gesproken het meest geschikt voor telefoons of kleine tablets.</span><span class="sxs-lookup"><span data-stu-id="97a8e-168">**Modern POS - Compact** – Typically, compact layouts are best used for phones or small tablets.</span></span> <span data-ttu-id="97a8e-169">De ontwerpmogelijkheden zijn beperkt voor compacte apparaten.</span><span class="sxs-lookup"><span data-stu-id="97a8e-169">Design possibilities are limited for compact devices.</span></span> <span data-ttu-id="97a8e-170">Gebruikers kunnen de kolommen en velden voor de deelvensters Ontvangstbewijs en Totalen configureren.</span><span class="sxs-lookup"><span data-stu-id="97a8e-170">Users can configure the columns and fields for the receipt pane and the totals pane.</span></span>

### <a name="screen-resolutions-that-are-provided"></a><span data-ttu-id="97a8e-171">Geleverde schermresoluties</span><span class="sxs-lookup"><span data-stu-id="97a8e-171">Screen resolutions that are provided</span></span>

<span data-ttu-id="97a8e-172">In de volgende tabel worden de indelingsformaten weergegeven die beschikbaar zijn voor normale schermresoluties.</span><span class="sxs-lookup"><span data-stu-id="97a8e-172">The following table shows the layout sizes that are provided for typical screen resolutions.</span></span>

| <span data-ttu-id="97a8e-173">Indelingstype</span><span class="sxs-lookup"><span data-stu-id="97a8e-173">Layout type</span></span> | <span data-ttu-id="97a8e-174">Resolutie</span><span class="sxs-lookup"><span data-stu-id="97a8e-174">Resolution</span></span> | <span data-ttu-id="97a8e-175">Hoogte-breedteverhouding</span><span class="sxs-lookup"><span data-stu-id="97a8e-175">Aspect ratio</span></span> | <span data-ttu-id="97a8e-176">Doelweergave</span><span class="sxs-lookup"><span data-stu-id="97a8e-176">Target display</span></span>          |
|-------------|------------|--------------|-------------------------|
| <span data-ttu-id="97a8e-177">Klein\*</span><span class="sxs-lookup"><span data-stu-id="97a8e-177">Compact\*</span></span>   | <span data-ttu-id="97a8e-178">480 × 853</span><span class="sxs-lookup"><span data-stu-id="97a8e-178">480 × 853</span></span>  | <span data-ttu-id="97a8e-179">16:9</span><span class="sxs-lookup"><span data-stu-id="97a8e-179">16:9</span></span>         | <span data-ttu-id="97a8e-180">Telefoons</span><span class="sxs-lookup"><span data-stu-id="97a8e-180">Phones</span></span>                  |
| <span data-ttu-id="97a8e-181">Volledig</span><span class="sxs-lookup"><span data-stu-id="97a8e-181">Full</span></span>        | <span data-ttu-id="97a8e-182">1024 × 768</span><span class="sxs-lookup"><span data-stu-id="97a8e-182">1024 × 768</span></span> | <span data-ttu-id="97a8e-183">4:3</span><span class="sxs-lookup"><span data-stu-id="97a8e-183">4:3</span></span>          | <span data-ttu-id="97a8e-184">Tablets</span><span class="sxs-lookup"><span data-stu-id="97a8e-184">Tablets</span></span>                 |
| <span data-ttu-id="97a8e-185">Volledig\*</span><span class="sxs-lookup"><span data-stu-id="97a8e-185">Full\*</span></span>      | <span data-ttu-id="97a8e-186">1280 × 720</span><span class="sxs-lookup"><span data-stu-id="97a8e-186">1280 × 720</span></span> | <span data-ttu-id="97a8e-187">16:9</span><span class="sxs-lookup"><span data-stu-id="97a8e-187">16:9</span></span>         | <span data-ttu-id="97a8e-188">Tablets</span><span class="sxs-lookup"><span data-stu-id="97a8e-188">Tablets</span></span>                 |
| <span data-ttu-id="97a8e-189">Volledig</span><span class="sxs-lookup"><span data-stu-id="97a8e-189">Full</span></span>        | <span data-ttu-id="97a8e-190">1366 × 768</span><span class="sxs-lookup"><span data-stu-id="97a8e-190">1366 × 768</span></span> | <span data-ttu-id="97a8e-191">16:9</span><span class="sxs-lookup"><span data-stu-id="97a8e-191">16:9</span></span>         | <span data-ttu-id="97a8e-192">Tablets, grotere schermen</span><span class="sxs-lookup"><span data-stu-id="97a8e-192">Tablets, larger screens</span></span> |
| <span data-ttu-id="97a8e-193">Volledig</span><span class="sxs-lookup"><span data-stu-id="97a8e-193">Full</span></span>        | <span data-ttu-id="97a8e-194">1440 × 960</span><span class="sxs-lookup"><span data-stu-id="97a8e-194">1440 × 960</span></span> | <span data-ttu-id="97a8e-195">3:2</span><span class="sxs-lookup"><span data-stu-id="97a8e-195">3:2</span></span>          | <span data-ttu-id="97a8e-196">Tablets, grotere schermen</span><span class="sxs-lookup"><span data-stu-id="97a8e-196">Tablets, larger screens</span></span> |

<span data-ttu-id="97a8e-197">\* Deze extra indelingsformaten zijn alleen beschikbaar in Adventure Works- en Fabrikam-indelingen.</span><span class="sxs-lookup"><span data-stu-id="97a8e-197">\* These additional layout sizes are available only in Adventure Works and Fabrikam layouts.</span></span>

> [!TIP]
> <span data-ttu-id="97a8e-198">POS selecteert automatisch indelingsformaten, gebaseerd op de dichtstbijzijnde grootte die voor de schermresolutie van het huidige appvenster beschikbaar is.</span><span class="sxs-lookup"><span data-stu-id="97a8e-198">POS automatically selects layout sizes, based on the closest size that is available for the screen resolution of the current app window.</span></span> <span data-ttu-id="97a8e-199">U vindt de schermindelings-id en indelingsresolutie die momenteel worden gebruikt, door Modern POS (MPOS) of Retail Cloud POS (CPOS) te openen, de pagina **Instellingen** te openen en de sectie **Sessie-informatie** te bekijken.</span><span class="sxs-lookup"><span data-stu-id="97a8e-199">To find the screen layout ID and layout resolution that are currently used, in Modern POS (MPOS) or Retail Cloud POS (CPOS), open the **Settings** page, and look in the **Session information** section.</span></span> <span data-ttu-id="97a8e-200">U kunt ook de werkelijke vensterresolutie voor uw huidige toepassing of browserframe bekijken.</span><span class="sxs-lookup"><span data-stu-id="97a8e-200">You can also see the actual window resolution for your current application or browser frame.</span></span> <span data-ttu-id="97a8e-201">Als u deze gegevens hebt, kunt u de bron van de indelingsinhoud vinden door naar **Afzetkanaalinstellingen** \> **POS-instellingen** \> **POS** \> **Schermindelingen** te gaan.</span><span class="sxs-lookup"><span data-stu-id="97a8e-201">After you have this information, you can find the source of the layout content by going to **Channel setup** \> **POS setup** \> **POS** \> **Screen layouts**.</span></span>

![Schermindelingen en indelingsresoluties/-formaten in Commerce en POS](../commerce/media/demo-screen-layouts-fig-3-1.png)

## <a name="companies-and-brands"></a><span data-ttu-id="97a8e-203">Bedrijven en merken</span><span class="sxs-lookup"><span data-stu-id="97a8e-203">Companies and brands</span></span>

<span data-ttu-id="97a8e-204">Elk fictief bedrijf is gericht op een ander segment en bevat productcatalogi die specifiek bedoeld zijn voor de markt van het bedrijf.</span><span class="sxs-lookup"><span data-stu-id="97a8e-204">Each fictitious company is targeted to a different retail segment and includes product catalogs that are tuned for the company's market.</span></span> <span data-ttu-id="97a8e-205">Elk bedrijf heeft een unieke visuele stijl die bij de producten hoort.</span><span class="sxs-lookup"><span data-stu-id="97a8e-205">Each company has a unique visual brand that accompanies its products.</span></span> <span data-ttu-id="97a8e-206">Tot de huisstijlelementen behoren de accentkleur, een donker of licht thema en begeleidende foto's die realistische ervaringen bieden.</span><span class="sxs-lookup"><span data-stu-id="97a8e-206">Branding elements include the accent color, dark or light theme, and accompanying photographs that provide realistic experiences.</span></span>

### <a name="company-segment-and-visual-characteristics"></a><span data-ttu-id="97a8e-207">Bedrijfssegment en visuele kenmerken</span><span class="sxs-lookup"><span data-stu-id="97a8e-207">Company segment and visual characteristics</span></span>

| <span data-ttu-id="97a8e-208">Bedrijf</span><span class="sxs-lookup"><span data-stu-id="97a8e-208">Company</span></span>         | <span data-ttu-id="97a8e-209">Locatie</span><span class="sxs-lookup"><span data-stu-id="97a8e-209">Location</span></span> | <span data-ttu-id="97a8e-210">Segment</span><span class="sxs-lookup"><span data-stu-id="97a8e-210">Segment</span></span>        | <span data-ttu-id="97a8e-211">Accent</span><span class="sxs-lookup"><span data-stu-id="97a8e-211">Accent</span></span> | <span data-ttu-id="97a8e-212">Thema</span><span class="sxs-lookup"><span data-stu-id="97a8e-212">Theme</span></span> |
|-----------------|----------|----------------|--------|-------|
| <span data-ttu-id="97a8e-213">Adventure Works</span><span class="sxs-lookup"><span data-stu-id="97a8e-213">Adventure Works</span></span> | <span data-ttu-id="97a8e-214">Seattle</span><span class="sxs-lookup"><span data-stu-id="97a8e-214">Seattle</span></span>  | <span data-ttu-id="97a8e-215">Sportartikelen</span><span class="sxs-lookup"><span data-stu-id="97a8e-215">Sporting Goods</span></span> | <span data-ttu-id="97a8e-216">Blauw</span><span class="sxs-lookup"><span data-stu-id="97a8e-216">Blue</span></span>   | <span data-ttu-id="97a8e-217">Donker</span><span class="sxs-lookup"><span data-stu-id="97a8e-217">Dark</span></span>  |
| <span data-ttu-id="97a8e-218">Fabrikam</span><span class="sxs-lookup"><span data-stu-id="97a8e-218">Fabrikam</span></span>        | <span data-ttu-id="97a8e-219">Houston</span><span class="sxs-lookup"><span data-stu-id="97a8e-219">Houston</span></span>  | <span data-ttu-id="97a8e-220">Mode</span><span class="sxs-lookup"><span data-stu-id="97a8e-220">Fashion</span></span>        | <span data-ttu-id="97a8e-221">Groen</span><span class="sxs-lookup"><span data-stu-id="97a8e-221">Green</span></span>  | <span data-ttu-id="97a8e-222">Licht</span><span class="sxs-lookup"><span data-stu-id="97a8e-222">Light</span></span> |
| <span data-ttu-id="97a8e-223">Contoso</span><span class="sxs-lookup"><span data-stu-id="97a8e-223">Contoso</span></span>         | <span data-ttu-id="97a8e-224">Boston</span><span class="sxs-lookup"><span data-stu-id="97a8e-224">Boston</span></span>   | <span data-ttu-id="97a8e-225">Elektronica</span><span class="sxs-lookup"><span data-stu-id="97a8e-225">Electronics</span></span>    | <span data-ttu-id="97a8e-226">Rood</span><span class="sxs-lookup"><span data-stu-id="97a8e-226">Red</span></span>    | <span data-ttu-id="97a8e-227">Donker</span><span class="sxs-lookup"><span data-stu-id="97a8e-227">Dark</span></span>  |

> [!NOTE]
> <span data-ttu-id="97a8e-228">Adventure Works en Fabrikam zijn de twee vlaggenschipmerken.</span><span class="sxs-lookup"><span data-stu-id="97a8e-228">Adventure Works and Fabrikam are the two flagship brands.</span></span> <span data-ttu-id="97a8e-229">Contoso is beschikbaar, maar niet alle indelingen.</span><span class="sxs-lookup"><span data-stu-id="97a8e-229">Contoso is available, but not all layouts have been provided.</span></span>

<span data-ttu-id="97a8e-230">In de volgende afbeeldingen ziet u voorbeelden van de welkomstpagina en transactiepagina voor de drie fictieve bedrijven.</span><span class="sxs-lookup"><span data-stu-id="97a8e-230">The following illustrations show examples of the welcome page and transaction page for the three fictitious companies.</span></span>

### <a name="adventure-works"></a><span data-ttu-id="97a8e-231">Adventure Works</span><span class="sxs-lookup"><span data-stu-id="97a8e-231">Adventure Works</span></span>

![Welkomstpagina met demonstratiegegevens voor Adventure Works](../commerce/media/demo-screen-layouts-fig-4-1a.png)

![Transactiepagina met demonstratiegegevens voor Adventure Works](../commerce/media/demo-screen-layouts-fig-4-1b.png)

### <a name="fabrikam"></a><span data-ttu-id="97a8e-234">Fabrikam</span><span class="sxs-lookup"><span data-stu-id="97a8e-234">Fabrikam</span></span>

![Welkomstpagina met demonstratiegegevens voor Fabrikam](../commerce/media/demo-screen-layouts-fig-4-2a.png)

![Transactiepagina met demonstratiegegevens voor Fabrikam](../commerce/media/demo-screen-layouts-fig-4-2b.png)

### <a name="contoso"></a><span data-ttu-id="97a8e-237">Contoso</span><span class="sxs-lookup"><span data-stu-id="97a8e-237">Contoso</span></span>

![Indelingen met demonstratiegegevens voor Contoso](../commerce/media/demo-screen-layouts-fig-4-3.png)

## <a name="user-sign-in-matrix"></a><span data-ttu-id="97a8e-239">Matrix voor gebruikersaanmelding</span><span class="sxs-lookup"><span data-stu-id="97a8e-239">User sign in matrix</span></span>

<span data-ttu-id="97a8e-240">Er zijn al gebruikers opgegeven voor de verschillende schermindelingen.</span><span class="sxs-lookup"><span data-stu-id="97a8e-240">Users have been provided for the various screen layouts.</span></span> <span data-ttu-id="97a8e-241">Met behulp van de volgende tabel moet u toegang kunnen krijgen tot elk van deze schermen.</span><span class="sxs-lookup"><span data-stu-id="97a8e-241">By using the following table, you should be able to access any of the screens.</span></span> <span data-ttu-id="97a8e-242">U hoeft u alleen maar aan te melden met een juiste operator-id.</span><span class="sxs-lookup"><span data-stu-id="97a8e-242">Just sign in by using an appropriate operator ID.</span></span>

| <span data-ttu-id="97a8e-243">Bedrijf</span><span class="sxs-lookup"><span data-stu-id="97a8e-243">Company</span></span>         | <span data-ttu-id="97a8e-244">Schermindelings-id</span><span class="sxs-lookup"><span data-stu-id="97a8e-244">Screen layout ID</span></span> | <span data-ttu-id="97a8e-245">Persona</span><span class="sxs-lookup"><span data-stu-id="97a8e-245">Persona</span></span>       | <span data-ttu-id="97a8e-246">Operator-id's</span><span class="sxs-lookup"><span data-stu-id="97a8e-246">Operator IDs</span></span>           |
|-----------------|------------------|---------------|------------------------|
| <span data-ttu-id="97a8e-247">Adventure Works</span><span class="sxs-lookup"><span data-stu-id="97a8e-247">Adventure Works</span></span> | <span data-ttu-id="97a8e-248">A3MGR</span><span class="sxs-lookup"><span data-stu-id="97a8e-248">A3MGR</span></span>            | <span data-ttu-id="97a8e-249">Winkelmanager</span><span class="sxs-lookup"><span data-stu-id="97a8e-249">Store Manager</span></span> | <span data-ttu-id="97a8e-250">000154, 000137, 000073</span><span class="sxs-lookup"><span data-stu-id="97a8e-250">000154, 000137, 000073</span></span> |
| <span data-ttu-id="97a8e-251">Adventure Works</span><span class="sxs-lookup"><span data-stu-id="97a8e-251">Adventure Works</span></span> | <span data-ttu-id="97a8e-252">A3KAS</span><span class="sxs-lookup"><span data-stu-id="97a8e-252">A3CSH</span></span>            | <span data-ttu-id="97a8e-253">Kassier</span><span class="sxs-lookup"><span data-stu-id="97a8e-253">Cashier</span></span>       | <span data-ttu-id="97a8e-254">000150, 000175, 000165</span><span class="sxs-lookup"><span data-stu-id="97a8e-254">000150, 000175, 000165</span></span> |
| <span data-ttu-id="97a8e-255">Adventure Works</span><span class="sxs-lookup"><span data-stu-id="97a8e-255">Adventure Works</span></span> | <span data-ttu-id="97a8e-256">A3MMW</span><span class="sxs-lookup"><span data-stu-id="97a8e-256">A3STK</span></span>            | <span data-ttu-id="97a8e-257">Magazijnmedewerker</span><span class="sxs-lookup"><span data-stu-id="97a8e-257">Stock Clerk</span></span>   | <span data-ttu-id="97a8e-258">000155, 000181, 000152</span><span class="sxs-lookup"><span data-stu-id="97a8e-258">000155, 000181, 000152</span></span> |
| <span data-ttu-id="97a8e-259">Fabrikam</span><span class="sxs-lookup"><span data-stu-id="97a8e-259">Fabrikam</span></span>        | <span data-ttu-id="97a8e-260">F3MGR</span><span class="sxs-lookup"><span data-stu-id="97a8e-260">F3MGR</span></span>            | <span data-ttu-id="97a8e-261">Winkelmanager</span><span class="sxs-lookup"><span data-stu-id="97a8e-261">Store Manager</span></span> | <span data-ttu-id="97a8e-262">000160, 000168, 000163</span><span class="sxs-lookup"><span data-stu-id="97a8e-262">000160, 000168, 000163</span></span> |
| <span data-ttu-id="97a8e-263">Fabrikam</span><span class="sxs-lookup"><span data-stu-id="97a8e-263">Fabrikam</span></span>        | <span data-ttu-id="97a8e-264">F3KAS</span><span class="sxs-lookup"><span data-stu-id="97a8e-264">F3CSH</span></span>            | <span data-ttu-id="97a8e-265">Kassier</span><span class="sxs-lookup"><span data-stu-id="97a8e-265">Cashier</span></span>       | <span data-ttu-id="97a8e-266">000161, 000113, 000114</span><span class="sxs-lookup"><span data-stu-id="97a8e-266">000161, 000113, 000114</span></span> |
| <span data-ttu-id="97a8e-267">Fabrikam</span><span class="sxs-lookup"><span data-stu-id="97a8e-267">Fabrikam</span></span>        | <span data-ttu-id="97a8e-268">F3MMW</span><span class="sxs-lookup"><span data-stu-id="97a8e-268">F3STK</span></span>            | <span data-ttu-id="97a8e-269">Magazijnmedewerker</span><span class="sxs-lookup"><span data-stu-id="97a8e-269">Stock Clerk</span></span>   | <span data-ttu-id="97a8e-270">000164, 000112, 000123</span><span class="sxs-lookup"><span data-stu-id="97a8e-270">000164, 000112, 000123</span></span> |
| <span data-ttu-id="97a8e-271">Contoso</span><span class="sxs-lookup"><span data-stu-id="97a8e-271">Contoso</span></span>         | <span data-ttu-id="97a8e-272">C3MGR</span><span class="sxs-lookup"><span data-stu-id="97a8e-272">C3MGR</span></span>            | <span data-ttu-id="97a8e-273">Winkelmanager</span><span class="sxs-lookup"><span data-stu-id="97a8e-273">Store Manager</span></span> | <span data-ttu-id="97a8e-274">000100, 000111</span><span class="sxs-lookup"><span data-stu-id="97a8e-274">000100, 000111</span></span>         |
| <span data-ttu-id="97a8e-275">Contoso</span><span class="sxs-lookup"><span data-stu-id="97a8e-275">Contoso</span></span>         | <span data-ttu-id="97a8e-276">C3KAS</span><span class="sxs-lookup"><span data-stu-id="97a8e-276">C3CSH</span></span>            | <span data-ttu-id="97a8e-277">Kassier</span><span class="sxs-lookup"><span data-stu-id="97a8e-277">Cashier</span></span>       | <span data-ttu-id="97a8e-278">000110, 000120</span><span class="sxs-lookup"><span data-stu-id="97a8e-278">000110, 000120</span></span>         |
| <span data-ttu-id="97a8e-279">Contoso</span><span class="sxs-lookup"><span data-stu-id="97a8e-279">Contoso</span></span>         | <span data-ttu-id="97a8e-280">Niet van toepassing</span><span class="sxs-lookup"><span data-stu-id="97a8e-280">Not applicable</span></span>   | <span data-ttu-id="97a8e-281">Magazijnmedewerker</span><span class="sxs-lookup"><span data-stu-id="97a8e-281">Stock Clerk</span></span>   | <span data-ttu-id="97a8e-282">Niet van toepassing</span><span class="sxs-lookup"><span data-stu-id="97a8e-282">Not applicable</span></span>         |

> [!TIP]
> <span data-ttu-id="97a8e-283">Activeer voor de beste resultaten een journaal in de bijbehorende winkellocatie en stel het bedrijf in op de persona waarmee u zich wilt aanmelden.</span><span class="sxs-lookup"><span data-stu-id="97a8e-283">For best results, activate a register in the corresponding store location, and set the company to the company of the persona that you plan to use when you sign in.</span></span> <span data-ttu-id="97a8e-284">Op deze manier kunt u ervoor zorgen dat het visuele profiel en brandingafbeeldingen consistent op elkaar zijn afgestemd.</span><span class="sxs-lookup"><span data-stu-id="97a8e-284">In this way, you help guarantee that the visual profile and branding images are aligned across the experience.</span></span> <span data-ttu-id="97a8e-285">Als u een Fabrikam-indeling voor een kassamedewerker wilt bekijken, moet u bijvoorbeeld een journaal in de winkel in Houston activeren.</span><span class="sxs-lookup"><span data-stu-id="97a8e-285">For example, if you're interested in seeing a Fabrikam layout for a cashier, you should activate a register in the Houston store.</span></span>

<!-- Hiding until the content page is available on CustomerSource -->

<!-- ## Reference icons and images -->

<!-- The screen layouts, button grids, and visual profiles were created using images and icons that can be found in **Retail and Commerce \> Channel setup \> POS setup \> POS \> Images**. -->

<!-- ![Images in Dynamics 365 Commerce](../commerce/media/demo-screen-layouts-fig-5-1.png) -->

<!-- Use the [POS Icon and Image Mapping](../commerce/media/POS_Icon_and_Image_Mapping.xlsx) reference spreadsheet to locate operation icons, reference photos, swap logos, or provide new images of your own that can be referenced in custom designs. -->

<!-- END HIDDEN CONTENT -->