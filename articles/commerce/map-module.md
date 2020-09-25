---
title: Module Kaarten
description: In dit onderwerp worden kaartmodules beschreven en hoe u ze configureert in Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 07/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2020-02-10
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: ca531e6cbf0a1044b0a13e5cdf42c7b4f0498fe5
ms.sourcegitcommit: 629988f1a704d62648d98649056931b8c33b9e08
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/14/2020
ms.locfileid: "3811179"
---
# <a name="map-module"></a><span data-ttu-id="cb301-103">Module Kaarten</span><span class="sxs-lookup"><span data-stu-id="cb301-103">Map module</span></span>

[!include [banner](includes/banner.md)]


<span data-ttu-id="cb301-104">In dit onderwerp worden kaartmodules beschreven en hoe u ze configureert in Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="cb301-104">This topic covers map modules and describes how to configure them in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="cb301-105">Overzicht</span><span class="sxs-lookup"><span data-stu-id="cb301-105">Overview</span></span>

<span data-ttu-id="cb301-106">Een kaartmodule toont de locaties van winkels op een interactieve kaart die wordt gegenereerd met behulp van het [V8-webbesturingselement van Bing Kaarten](https://docs.microsoft.com/bingmaps/v8-web-control/).</span><span class="sxs-lookup"><span data-stu-id="cb301-106">A map module shows the locations of stores on an interactive map that is rendered by using the [Bing Maps V8 Web Control](https://docs.microsoft.com/bingmaps/v8-web-control/).</span></span> <span data-ttu-id="cb301-107">Er is een API-sleutel voor Bing Kaarten vereist. Deze moet worden toegevoegd aan de pagina met gedeelde parameters in Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="cb301-107">A Bing Maps API key is required and must be added to the shared parameters page in Commerce headquarters.</span></span> <span data-ttu-id="cb301-108">Kaartmodules bieden verschillende weergaven, zoals Road, Aerial en Streetside, die gebruikers kunnen selecteren om kaartlocaties weer te geven.</span><span class="sxs-lookup"><span data-stu-id="cb301-108">Map modules provide different views, such as Road, Aerial, and Streetside, that users can select to view map locations.</span></span> <span data-ttu-id="cb301-109">Ze maken ook interacties mogelijk, zoals in- en uitzoomen en gebruik van de locatie van de gebruiker.</span><span class="sxs-lookup"><span data-stu-id="cb301-109">They also allow for interactions such as zooming and using the user's location.</span></span>

<span data-ttu-id="cb301-110">Een kaartmodule werkt samen met de winkelselectiemodule om de geografische locaties van winkels te bepalen die moeten worden weergegeven op een kaart.</span><span class="sxs-lookup"><span data-stu-id="cb301-110">A map module works in conjunction with the store selector module to determine the geographic locations of stores that must be rendered on a map.</span></span> <span data-ttu-id="cb301-111">Winkelselectie- en kaartmodules communiceren wanneer een gebruiker een winkel selecteert in een van deze modules op een sitepagina.</span><span class="sxs-lookup"><span data-stu-id="cb301-111">Store selector and map modules interact when a user selects a store in one of those modules on a site page.</span></span> <span data-ttu-id="cb301-112">Kaartmodules kunnen worden uitgebreid voor andere scenario's, naast interactie met winkelselectiemodules.</span><span class="sxs-lookup"><span data-stu-id="cb301-112">Map modules can be extended for other scenarios, beyond interaction with store selector modules.</span></span> <span data-ttu-id="cb301-113">Het aanpassen van modules is echter vereist.</span><span class="sxs-lookup"><span data-stu-id="cb301-113">However, module customization is required.</span></span>

<span data-ttu-id="cb301-114">De kaartmodule is geïntroduceerd in Commerce versie 10.0.13.</span><span class="sxs-lookup"><span data-stu-id="cb301-114">The map module was introduced in Commerce version 10.0.13.</span></span>

<span data-ttu-id="cb301-115">De volgende afbeelding toont een voorbeeld van een kaartmodule die wordt gebruikt op winkellocatiepagina.</span><span class="sxs-lookup"><span data-stu-id="cb301-115">The following image shows an example of a map module that is used on a store locations page.</span></span>

![Voorbeeld van een winkelselectiemodule](./media/ecommerce-Storelocator.PNG)

## <a name="module-properties"></a><span data-ttu-id="cb301-117">Module-eigenschappen</span><span class="sxs-lookup"><span data-stu-id="cb301-117">Module properties</span></span>

| <span data-ttu-id="cb301-118">Naam van eigenschap.</span><span class="sxs-lookup"><span data-stu-id="cb301-118">Property name</span></span>             | <span data-ttu-id="cb301-119">Waarde</span><span class="sxs-lookup"><span data-stu-id="cb301-119">Value</span></span>                 | <span data-ttu-id="cb301-120">Omschrijving</span><span class="sxs-lookup"><span data-stu-id="cb301-120">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="cb301-121">Kop</span><span class="sxs-lookup"><span data-stu-id="cb301-121">Heading</span></span> | <span data-ttu-id="cb301-122">Tekst</span><span class="sxs-lookup"><span data-stu-id="cb301-122">Text</span></span> | <span data-ttu-id="cb301-123">De koptekst voor de module.</span><span class="sxs-lookup"><span data-stu-id="cb301-123">The heading for the module.</span></span> |
| <span data-ttu-id="cb301-124">Punaiseopties: standaardpictogram</span><span class="sxs-lookup"><span data-stu-id="cb301-124">Pushpin options: Default icon</span></span> | <span data-ttu-id="cb301-125">Afbeelding</span><span class="sxs-lookup"><span data-stu-id="cb301-125">Image</span></span> | <span data-ttu-id="cb301-126">Het punaisesymbool dat moet worden gebruikt voor winkels die op een kaart worden weergegeven.</span><span class="sxs-lookup"><span data-stu-id="cb301-126">The pushpin symbol image to use for stores that are shown on a map.</span></span> |
| <span data-ttu-id="cb301-127">Punaiseopties: pictogram Actief</span><span class="sxs-lookup"><span data-stu-id="cb301-127">Pushpin options: Active icon</span></span> | <span data-ttu-id="cb301-128">Afbeelding</span><span class="sxs-lookup"><span data-stu-id="cb301-128">Image</span></span> | <span data-ttu-id="cb301-129">Het punaisesymbool dat moet worden gebruikt voor een winkel die op een kaart is geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="cb301-129">The pushpin symbol image to use for a store that is selected on a map.</span></span> |
| <span data-ttu-id="cb301-130">Punaiseopties: standaardpictogramkleur</span><span class="sxs-lookup"><span data-stu-id="cb301-130">Pushpin options: Default icon color</span></span> | <span data-ttu-id="cb301-131">Tekenreeks</span><span class="sxs-lookup"><span data-stu-id="cb301-131">Character string</span></span> | <span data-ttu-id="cb301-132">De tekst of hexadecimale waarde voor de kleur van punaisesymbolen op een kaart.</span><span class="sxs-lookup"><span data-stu-id="cb301-132">The text or hexadecimal value for the color of pushpin symbols on a map.</span></span> |
| <span data-ttu-id="cb301-133">Punaiseopties: actieve pictogramkleur</span><span class="sxs-lookup"><span data-stu-id="cb301-133">Pushpin options: Active icon color</span></span> | <span data-ttu-id="cb301-134">Tekenreeks</span><span class="sxs-lookup"><span data-stu-id="cb301-134">Character string</span></span> | <span data-ttu-id="cb301-135">De tekst of hexadecimale waarde voor de kleur van geselecteerde punaisesymbolen op een kaart.</span><span class="sxs-lookup"><span data-stu-id="cb301-135">The text or hexadecimal value for the color of selected pushpin symbols on a map.</span></span> |
| <span data-ttu-id="cb301-136">Index weergeven</span><span class="sxs-lookup"><span data-stu-id="cb301-136">Show index</span></span> | <span data-ttu-id="cb301-137">**True** of **False**</span><span class="sxs-lookup"><span data-stu-id="cb301-137">**True** or **False**</span></span> | <span data-ttu-id="cb301-138">Als deze eigenschap is ingesteld op **Waar**, wordt voor elk punaisesymbool dat een winkel aangeeft, een index weergegeven.</span><span class="sxs-lookup"><span data-stu-id="cb301-138">If this property is set to **True**, every pushpin symbol that indicates a store will show an index.</span></span> <span data-ttu-id="cb301-139">Deze index komt overeen met de index in de lijstweergave die in de winkelselectiemodule wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="cb301-139">This index will match the index in the list view that the store selector module shows.</span></span> |

## <a name="add-allowed-mapping-urls-to-a-sites-content-security-policy-directives"></a><span data-ttu-id="cb301-140">Toegestane toewijzings-URL's toevoegen aan de beleidsrichtlijnen van de inhoudsbeveiliging van een site</span><span class="sxs-lookup"><span data-stu-id="cb301-140">Add allowed mapping URLs to a site's content security policy directives</span></span>

<span data-ttu-id="cb301-141">Om de kaartmodules te laten communiceren met Bing Kaarten moet u ervoor zorgen dat de volgende toewijzings-URL's zijn toegestaan (ook wel 'whitelisted' genoemd) volgens het inhoudsbeveiligingsbeleid van uw site (CSP).</span><span class="sxs-lookup"><span data-stu-id="cb301-141">For the maps module to interact with Bing Maps, you must ensure that the following mapping URLs are allowed (also known as "whitelisted") per your site's content security policy (CSP).</span></span> <span data-ttu-id="cb301-142">Deze instelling wordt uitgevoerd in Commerce Site Builder door toegestane URL's toe te voegen aan verschillende CSP-instructies voor de site (bijvoorbeeld **img-src**).</span><span class="sxs-lookup"><span data-stu-id="cb301-142">This setup is done in Commerce site builder, by adding allowed URLs to various site CSP directives (for example, **img-src**).</span></span> <span data-ttu-id="cb301-143">Zie voor meer informatie [Beveiligingsbeleid voor inhoud](manage-csp.md).</span><span class="sxs-lookup"><span data-stu-id="cb301-143">For more information, see [Content security policy](manage-csp.md).</span></span> 

- <span data-ttu-id="cb301-144">Voeg aan de **connect-src**-richtlijn **&#42;.bing.com** toe.</span><span class="sxs-lookup"><span data-stu-id="cb301-144">To the **connect-src** directive, add **&#42;.bing.com**.</span></span>
- <span data-ttu-id="cb301-145">Voeg aan de **img-src**-richtlijn **&#42;.virtualearth.net** toe.</span><span class="sxs-lookup"><span data-stu-id="cb301-145">To the **img-src** directive, add **&#42;.virtualearth.net**.</span></span>
- <span data-ttu-id="cb301-146">Voeg aan de **script-src**-instructie **&#42;.bing.com, &#42;.virtualearth.net** toe.</span><span class="sxs-lookup"><span data-stu-id="cb301-146">To the **script-src** directive, add **&#42;.bing.com, &#42;.virtualearth.net**.</span></span>
- <span data-ttu-id="cb301-147">Voeg aan de **script style-src**-instructie **&#42;.bing.com** toe.</span><span class="sxs-lookup"><span data-stu-id="cb301-147">To the **script style-src** directive, add **&#42;.bing.com**.</span></span>

## <a name="add-a-map-module-to-a-page"></a><span data-ttu-id="cb301-148">Een kaartmodule toevoegen aan een pagina</span><span class="sxs-lookup"><span data-stu-id="cb301-148">Add a map module to a page</span></span>

<span data-ttu-id="cb301-149">Zie [Winkelselectiemodule](store-selector.md) voor meer informatie over het configureren van een kaartmodule op een pagina.</span><span class="sxs-lookup"><span data-stu-id="cb301-149">For detailed information about how to configure a map module on a page, see [Store selector module](store-selector.md).</span></span> 
 
## <a name="additional-resources"></a><span data-ttu-id="cb301-150">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="cb301-150">Additional resources</span></span>

[<span data-ttu-id="cb301-151">Overzicht starterskit</span><span class="sxs-lookup"><span data-stu-id="cb301-151">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="cb301-152">Module met vakje voor kopen</span><span class="sxs-lookup"><span data-stu-id="cb301-152">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="cb301-153">Winkelwagenmodule</span><span class="sxs-lookup"><span data-stu-id="cb301-153">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="cb301-154">Winkelselectiemodule</span><span class="sxs-lookup"><span data-stu-id="cb301-154">Store selector module</span></span>](store-selector.md)

[<span data-ttu-id="cb301-155">Bing Kaarten voor uw organisatie beheren</span><span class="sxs-lookup"><span data-stu-id="cb301-155">Manage Bing Maps for your organization</span></span>](./dev-itpro/manage-bing-maps.md)

[<span data-ttu-id="cb301-156">V8-webbesturingselement van Bing Kaarten</span><span class="sxs-lookup"><span data-stu-id="cb301-156">Bing Maps V8 Web Control</span></span>](https://docs.microsoft.com/bingmaps/v8-web-control/)
