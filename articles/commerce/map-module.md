---
title: Module Kaarten
description: In dit onderwerp worden kaartmodules beschreven en hoe u ze configureert in Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2020-02-10
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: e93358a9c76e8eb7bfb4ade4f772dece2aa5f7d3
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2021
ms.locfileid: "4982486"
---
# <a name="map-module"></a><span data-ttu-id="c0d9e-103">Module Kaarten</span><span class="sxs-lookup"><span data-stu-id="c0d9e-103">Map module</span></span>

[!include [banner](includes/banner.md)]


<span data-ttu-id="c0d9e-104">In dit onderwerp worden kaartmodules beschreven en hoe u ze configureert in Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="c0d9e-104">This topic covers map modules and describes how to configure them in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="c0d9e-105">Overzicht</span><span class="sxs-lookup"><span data-stu-id="c0d9e-105">Overview</span></span>

<span data-ttu-id="c0d9e-106">Een kaartmodule toont de locaties van winkels op een interactieve kaart die wordt gegenereerd met behulp van het [V8-webbesturingselement van Bing Kaarten](https://docs.microsoft.com/bingmaps/v8-web-control/).</span><span class="sxs-lookup"><span data-stu-id="c0d9e-106">A map module shows the locations of stores on an interactive map that is rendered by using the [Bing Maps V8 Web Control](https://docs.microsoft.com/bingmaps/v8-web-control/).</span></span> <span data-ttu-id="c0d9e-107">Er is een API-sleutel voor Bing Kaarten vereist. Deze moet worden toegevoegd aan de pagina met gedeelde parameters in Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="c0d9e-107">A Bing Maps API key is required and must be added to the shared parameters page in Commerce headquarters.</span></span> <span data-ttu-id="c0d9e-108">Kaartmodules bieden verschillende weergaven, zoals Road, Aerial en Streetside, die gebruikers kunnen selecteren om kaartlocaties weer te geven.</span><span class="sxs-lookup"><span data-stu-id="c0d9e-108">Map modules provide different views, such as Road, Aerial, and Streetside, that users can select to view map locations.</span></span> <span data-ttu-id="c0d9e-109">Ze maken ook interacties mogelijk, zoals in- en uitzoomen en gebruik van de locatie van de gebruiker.</span><span class="sxs-lookup"><span data-stu-id="c0d9e-109">They also allow for interactions such as zooming and using the user's location.</span></span>

<span data-ttu-id="c0d9e-110">Een kaartmodule werkt samen met de winkelselectiemodule om de geografische locaties van winkels te bepalen die moeten worden weergegeven op een kaart.</span><span class="sxs-lookup"><span data-stu-id="c0d9e-110">A map module works in conjunction with the store selector module to determine the geographic locations of stores that must be rendered on a map.</span></span> <span data-ttu-id="c0d9e-111">Winkelselectie- en kaartmodules communiceren wanneer een gebruiker een winkel selecteert in een van deze modules op een sitepagina.</span><span class="sxs-lookup"><span data-stu-id="c0d9e-111">Store selector and map modules interact when a user selects a store in one of those modules on a site page.</span></span> <span data-ttu-id="c0d9e-112">Kaartmodules kunnen worden uitgebreid voor andere scenario's, naast interactie met winkelselectiemodules.</span><span class="sxs-lookup"><span data-stu-id="c0d9e-112">Map modules can be extended for other scenarios, beyond interaction with store selector modules.</span></span> <span data-ttu-id="c0d9e-113">Het aanpassen van modules is echter vereist.</span><span class="sxs-lookup"><span data-stu-id="c0d9e-113">However, module customization is required.</span></span>

> [!NOTE]
> <span data-ttu-id="c0d9e-114">De kaartmodule is beschikbaar in de Dynamics 365 Commerce versie 10.0.13.</span><span class="sxs-lookup"><span data-stu-id="c0d9e-114">The map module is available in the Dynamics 365 Commerce 10.0.13 release.</span></span>

<span data-ttu-id="c0d9e-115">De volgende afbeelding toont een voorbeeld van een kaartmodule die wordt gebruikt op winkellocatiepagina.</span><span class="sxs-lookup"><span data-stu-id="c0d9e-115">The following image shows an example of a map module that is used on a store locations page.</span></span>

![Voorbeeld van een winkelselectiemodule](./media/ecommerce-Storelocator.PNG)

## <a name="module-properties"></a><span data-ttu-id="c0d9e-117">Module-eigenschappen</span><span class="sxs-lookup"><span data-stu-id="c0d9e-117">Module properties</span></span>

| <span data-ttu-id="c0d9e-118">Naam van eigenschap.</span><span class="sxs-lookup"><span data-stu-id="c0d9e-118">Property name</span></span>             | <span data-ttu-id="c0d9e-119">Waarde</span><span class="sxs-lookup"><span data-stu-id="c0d9e-119">Value</span></span>                 | <span data-ttu-id="c0d9e-120">Omschrijving</span><span class="sxs-lookup"><span data-stu-id="c0d9e-120">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="c0d9e-121">Kop</span><span class="sxs-lookup"><span data-stu-id="c0d9e-121">Heading</span></span> | <span data-ttu-id="c0d9e-122">Tekst</span><span class="sxs-lookup"><span data-stu-id="c0d9e-122">Text</span></span> | <span data-ttu-id="c0d9e-123">De koptekst voor de module.</span><span class="sxs-lookup"><span data-stu-id="c0d9e-123">The heading for the module.</span></span> |
| <span data-ttu-id="c0d9e-124">Punaiseopties: standaardpictogram</span><span class="sxs-lookup"><span data-stu-id="c0d9e-124">Pushpin options: Default icon</span></span> | <span data-ttu-id="c0d9e-125">Afbeelding</span><span class="sxs-lookup"><span data-stu-id="c0d9e-125">Image</span></span> | <span data-ttu-id="c0d9e-126">Het punaisesymbool dat moet worden gebruikt voor winkels die op een kaart worden weergegeven.</span><span class="sxs-lookup"><span data-stu-id="c0d9e-126">The pushpin symbol image to use for stores that are shown on a map.</span></span> |
| <span data-ttu-id="c0d9e-127">Punaiseopties: pictogram Actief</span><span class="sxs-lookup"><span data-stu-id="c0d9e-127">Pushpin options: Active icon</span></span> | <span data-ttu-id="c0d9e-128">Afbeelding</span><span class="sxs-lookup"><span data-stu-id="c0d9e-128">Image</span></span> | <span data-ttu-id="c0d9e-129">Het punaisesymbool dat moet worden gebruikt voor een winkel die op een kaart is geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="c0d9e-129">The pushpin symbol image to use for a store that is selected on a map.</span></span> |
| <span data-ttu-id="c0d9e-130">Punaiseopties: standaardpictogramkleur</span><span class="sxs-lookup"><span data-stu-id="c0d9e-130">Pushpin options: Default icon color</span></span> | <span data-ttu-id="c0d9e-131">Tekenreeks</span><span class="sxs-lookup"><span data-stu-id="c0d9e-131">Character string</span></span> | <span data-ttu-id="c0d9e-132">De tekst of hexadecimale waarde voor de kleur van punaisesymbolen op een kaart.</span><span class="sxs-lookup"><span data-stu-id="c0d9e-132">The text or hexadecimal value for the color of pushpin symbols on a map.</span></span> |
| <span data-ttu-id="c0d9e-133">Punaiseopties: actieve pictogramkleur</span><span class="sxs-lookup"><span data-stu-id="c0d9e-133">Pushpin options: Active icon color</span></span> | <span data-ttu-id="c0d9e-134">Tekenreeks</span><span class="sxs-lookup"><span data-stu-id="c0d9e-134">Character string</span></span> | <span data-ttu-id="c0d9e-135">De tekst of hexadecimale waarde voor de kleur van geselecteerde punaisesymbolen op een kaart.</span><span class="sxs-lookup"><span data-stu-id="c0d9e-135">The text or hexadecimal value for the color of selected pushpin symbols on a map.</span></span> |
| <span data-ttu-id="c0d9e-136">Index weergeven</span><span class="sxs-lookup"><span data-stu-id="c0d9e-136">Show index</span></span> | <span data-ttu-id="c0d9e-137">**True** of **False**</span><span class="sxs-lookup"><span data-stu-id="c0d9e-137">**True** or **False**</span></span> | <span data-ttu-id="c0d9e-138">Als deze eigenschap is ingesteld op **Waar**, wordt voor elk punaisesymbool dat een winkel aangeeft, een index weergegeven.</span><span class="sxs-lookup"><span data-stu-id="c0d9e-138">If this property is set to **True**, every pushpin symbol that indicates a store will show an index.</span></span> <span data-ttu-id="c0d9e-139">Deze index komt overeen met de index in de lijstweergave die in de winkelselectiemodule wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="c0d9e-139">This index will match the index in the list view that the store selector module shows.</span></span> |

## <a name="add-allowed-mapping-urls-to-a-sites-content-security-policy-directives"></a><span data-ttu-id="c0d9e-140">Toegestane toewijzings-URL's toevoegen aan de beleidsrichtlijnen van de inhoudsbeveiliging van een site</span><span class="sxs-lookup"><span data-stu-id="c0d9e-140">Add allowed mapping URLs to a site's content security policy directives</span></span>

<span data-ttu-id="c0d9e-141">Om de kaartmodules te laten communiceren met Bing Kaarten moet u ervoor zorgen dat de volgende toewijzings-URL's zijn toegestaan volgens het inhoudsbeveiligingsbeleid van uw site (CSP).</span><span class="sxs-lookup"><span data-stu-id="c0d9e-141">For the maps module to interact with Bing Maps, you must ensure that the following mapping URLs are allowed per your site's content security policy (CSP).</span></span> <span data-ttu-id="c0d9e-142">Deze instelling wordt uitgevoerd in Commerce Site Builder door toegestane URL's toe te voegen aan verschillende CSP-instructies voor de site (bijvoorbeeld **img-src**).</span><span class="sxs-lookup"><span data-stu-id="c0d9e-142">This setup is done in Commerce site builder, by adding allowed URLs to various site CSP directives (for example, **img-src**).</span></span> <span data-ttu-id="c0d9e-143">Zie voor meer informatie [Beveiligingsbeleid voor inhoud](manage-csp.md).</span><span class="sxs-lookup"><span data-stu-id="c0d9e-143">For more information, see [Content security policy](manage-csp.md).</span></span> 

- <span data-ttu-id="c0d9e-144">Voeg aan de **connect-src**-richtlijn **&#42;.bing.com** toe.</span><span class="sxs-lookup"><span data-stu-id="c0d9e-144">To the **connect-src** directive, add **&#42;.bing.com**.</span></span>
- <span data-ttu-id="c0d9e-145">Voeg aan de **img-src**-richtlijn **&#42;.virtualearth.net** toe.</span><span class="sxs-lookup"><span data-stu-id="c0d9e-145">To the **img-src** directive, add **&#42;.virtualearth.net**.</span></span>
- <span data-ttu-id="c0d9e-146">Voeg aan de **script-src**-instructie **&#42;.bing.com, &#42;.virtualearth.net** toe.</span><span class="sxs-lookup"><span data-stu-id="c0d9e-146">To the **script-src** directive, add **&#42;.bing.com, &#42;.virtualearth.net**.</span></span>
- <span data-ttu-id="c0d9e-147">Voeg aan de **script style-src**-instructie **&#42;.bing.com** toe.</span><span class="sxs-lookup"><span data-stu-id="c0d9e-147">To the **script style-src** directive, add **&#42;.bing.com**.</span></span>

## <a name="add-a-map-module-to-a-page"></a><span data-ttu-id="c0d9e-148">Een kaartmodule toevoegen aan een pagina</span><span class="sxs-lookup"><span data-stu-id="c0d9e-148">Add a map module to a page</span></span>

<span data-ttu-id="c0d9e-149">Zie [Winkelselectiemodule](store-selector.md) voor meer informatie over het configureren van een kaartmodule op een pagina.</span><span class="sxs-lookup"><span data-stu-id="c0d9e-149">For detailed information about how to configure a map module on a page, see [Store selector module](store-selector.md).</span></span> 
 
## <a name="additional-resources"></a><span data-ttu-id="c0d9e-150">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="c0d9e-150">Additional resources</span></span>

[<span data-ttu-id="c0d9e-151">Overzicht van modulebibliotheek</span><span class="sxs-lookup"><span data-stu-id="c0d9e-151">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="c0d9e-152">Module met vakje voor kopen</span><span class="sxs-lookup"><span data-stu-id="c0d9e-152">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="c0d9e-153">Winkelwagenmodule</span><span class="sxs-lookup"><span data-stu-id="c0d9e-153">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="c0d9e-154">Winkelselectiemodule</span><span class="sxs-lookup"><span data-stu-id="c0d9e-154">Store selector module</span></span>](store-selector.md)

[<span data-ttu-id="c0d9e-155">Bing Kaarten voor uw organisatie beheren</span><span class="sxs-lookup"><span data-stu-id="c0d9e-155">Manage Bing Maps for your organization</span></span>](./dev-itpro/manage-bing-maps.md)

[<span data-ttu-id="c0d9e-156">V8-webbesturingselement van Bing Kaarten</span><span class="sxs-lookup"><span data-stu-id="c0d9e-156">Bing Maps V8 Web Control</span></span>](https://docs.microsoft.com/bingmaps/v8-web-control/)
