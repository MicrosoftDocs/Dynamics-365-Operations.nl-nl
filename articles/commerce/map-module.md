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
ms.openlocfilehash: 74991a2979540dab344f39976005250637fab29c
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5252577"
---
# <a name="map-module"></a><span data-ttu-id="952fa-103">Kaartmodule</span><span class="sxs-lookup"><span data-stu-id="952fa-103">Map module</span></span>

[!include [banner](includes/banner.md)]


<span data-ttu-id="952fa-104">In dit onderwerp worden kaartmodules beschreven en hoe u ze configureert in Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="952fa-104">This topic covers map modules and describes how to configure them in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="952fa-105">Een kaartmodule toont de locaties van winkels op een interactieve kaart die wordt gegenereerd met behulp van het [V8-webbesturingselement van Bing Kaarten](https://docs.microsoft.com/bingmaps/v8-web-control/).</span><span class="sxs-lookup"><span data-stu-id="952fa-105">A map module shows the locations of stores on an interactive map that is rendered by using the [Bing Maps V8 Web Control](https://docs.microsoft.com/bingmaps/v8-web-control/).</span></span> <span data-ttu-id="952fa-106">Er is een API-sleutel voor Bing Kaarten vereist. Deze moet worden toegevoegd aan de pagina met gedeelde parameters in Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="952fa-106">A Bing Maps API key is required and must be added to the shared parameters page in Commerce headquarters.</span></span> <span data-ttu-id="952fa-107">Kaartmodules bieden verschillende weergaven, zoals Road, Aerial en Streetside, die gebruikers kunnen selecteren om kaartlocaties weer te geven.</span><span class="sxs-lookup"><span data-stu-id="952fa-107">Map modules provide different views, such as Road, Aerial, and Streetside, that users can select to view map locations.</span></span> <span data-ttu-id="952fa-108">Ze maken ook interacties mogelijk, zoals in- en uitzoomen en gebruik van de locatie van de gebruiker.</span><span class="sxs-lookup"><span data-stu-id="952fa-108">They also allow for interactions such as zooming and using the user's location.</span></span>

<span data-ttu-id="952fa-109">Een kaartmodule werkt samen met de winkelselectiemodule om de geografische locaties van winkels te bepalen die moeten worden weergegeven op een kaart.</span><span class="sxs-lookup"><span data-stu-id="952fa-109">A map module works in conjunction with the store selector module to determine the geographic locations of stores that must be rendered on a map.</span></span> <span data-ttu-id="952fa-110">Winkelselectie- en kaartmodules communiceren wanneer een gebruiker een winkel selecteert in een van deze modules op een sitepagina.</span><span class="sxs-lookup"><span data-stu-id="952fa-110">Store selector and map modules interact when a user selects a store in one of those modules on a site page.</span></span> <span data-ttu-id="952fa-111">Kaartmodules kunnen worden uitgebreid voor andere scenario's, naast interactie met winkelselectiemodules.</span><span class="sxs-lookup"><span data-stu-id="952fa-111">Map modules can be extended for other scenarios, beyond interaction with store selector modules.</span></span> <span data-ttu-id="952fa-112">Het aanpassen van modules is echter vereist.</span><span class="sxs-lookup"><span data-stu-id="952fa-112">However, module customization is required.</span></span>

> [!NOTE]
> <span data-ttu-id="952fa-113">De kaartmodule is beschikbaar in de Dynamics 365 Commerce versie 10.0.13.</span><span class="sxs-lookup"><span data-stu-id="952fa-113">The map module is available in the Dynamics 365 Commerce 10.0.13 release.</span></span>

<span data-ttu-id="952fa-114">De volgende afbeelding toont een voorbeeld van een kaartmodule die wordt gebruikt op winkellocatiepagina.</span><span class="sxs-lookup"><span data-stu-id="952fa-114">The following image shows an example of a map module that is used on a store locations page.</span></span>

![Voorbeeld van een winkelselectiemodule](./media/ecommerce-Storelocator.PNG)

## <a name="module-properties"></a><span data-ttu-id="952fa-116">Module-eigenschappen</span><span class="sxs-lookup"><span data-stu-id="952fa-116">Module properties</span></span>

| <span data-ttu-id="952fa-117">Naam van eigenschap.</span><span class="sxs-lookup"><span data-stu-id="952fa-117">Property name</span></span>             | <span data-ttu-id="952fa-118">Waarde</span><span class="sxs-lookup"><span data-stu-id="952fa-118">Value</span></span>                 | <span data-ttu-id="952fa-119">Omschrijving</span><span class="sxs-lookup"><span data-stu-id="952fa-119">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="952fa-120">Kop</span><span class="sxs-lookup"><span data-stu-id="952fa-120">Heading</span></span> | <span data-ttu-id="952fa-121">Tekst</span><span class="sxs-lookup"><span data-stu-id="952fa-121">Text</span></span> | <span data-ttu-id="952fa-122">De koptekst voor de module.</span><span class="sxs-lookup"><span data-stu-id="952fa-122">The heading for the module.</span></span> |
| <span data-ttu-id="952fa-123">Punaiseopties: standaardpictogram</span><span class="sxs-lookup"><span data-stu-id="952fa-123">Pushpin options: Default icon</span></span> | <span data-ttu-id="952fa-124">Afbeelding</span><span class="sxs-lookup"><span data-stu-id="952fa-124">Image</span></span> | <span data-ttu-id="952fa-125">Het punaisesymbool dat moet worden gebruikt voor winkels die op een kaart worden weergegeven.</span><span class="sxs-lookup"><span data-stu-id="952fa-125">The pushpin symbol image to use for stores that are shown on a map.</span></span> |
| <span data-ttu-id="952fa-126">Punaiseopties: pictogram Actief</span><span class="sxs-lookup"><span data-stu-id="952fa-126">Pushpin options: Active icon</span></span> | <span data-ttu-id="952fa-127">Afbeelding</span><span class="sxs-lookup"><span data-stu-id="952fa-127">Image</span></span> | <span data-ttu-id="952fa-128">Het punaisesymbool dat moet worden gebruikt voor een winkel die op een kaart is geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="952fa-128">The pushpin symbol image to use for a store that is selected on a map.</span></span> |
| <span data-ttu-id="952fa-129">Punaiseopties: standaardpictogramkleur</span><span class="sxs-lookup"><span data-stu-id="952fa-129">Pushpin options: Default icon color</span></span> | <span data-ttu-id="952fa-130">Tekenreeks</span><span class="sxs-lookup"><span data-stu-id="952fa-130">Character string</span></span> | <span data-ttu-id="952fa-131">De tekst of hexadecimale waarde voor de kleur van punaisesymbolen op een kaart.</span><span class="sxs-lookup"><span data-stu-id="952fa-131">The text or hexadecimal value for the color of pushpin symbols on a map.</span></span> |
| <span data-ttu-id="952fa-132">Punaiseopties: actieve pictogramkleur</span><span class="sxs-lookup"><span data-stu-id="952fa-132">Pushpin options: Active icon color</span></span> | <span data-ttu-id="952fa-133">Tekenreeks</span><span class="sxs-lookup"><span data-stu-id="952fa-133">Character string</span></span> | <span data-ttu-id="952fa-134">De tekst of hexadecimale waarde voor de kleur van geselecteerde punaisesymbolen op een kaart.</span><span class="sxs-lookup"><span data-stu-id="952fa-134">The text or hexadecimal value for the color of selected pushpin symbols on a map.</span></span> |
| <span data-ttu-id="952fa-135">Index weergeven</span><span class="sxs-lookup"><span data-stu-id="952fa-135">Show index</span></span> | <span data-ttu-id="952fa-136">**True** of **False**</span><span class="sxs-lookup"><span data-stu-id="952fa-136">**True** or **False**</span></span> | <span data-ttu-id="952fa-137">Als deze eigenschap is ingesteld op **Waar**, wordt voor elk punaisesymbool dat een winkel aangeeft, een index weergegeven.</span><span class="sxs-lookup"><span data-stu-id="952fa-137">If this property is set to **True**, every pushpin symbol that indicates a store will show an index.</span></span> <span data-ttu-id="952fa-138">Deze index komt overeen met de index in de lijstweergave die in de winkelselectiemodule wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="952fa-138">This index will match the index in the list view that the store selector module shows.</span></span> |

## <a name="add-allowed-mapping-urls-to-a-sites-content-security-policy-directives"></a><span data-ttu-id="952fa-139">Toegestane toewijzings-URL's toevoegen aan de beleidsrichtlijnen van de inhoudsbeveiliging van een site</span><span class="sxs-lookup"><span data-stu-id="952fa-139">Add allowed mapping URLs to a site's content security policy directives</span></span>

<span data-ttu-id="952fa-140">Om de kaartmodules te laten communiceren met Bing Kaarten moet u ervoor zorgen dat de volgende toewijzings-URL's zijn toegestaan volgens het inhoudsbeveiligingsbeleid van uw site (CSP).</span><span class="sxs-lookup"><span data-stu-id="952fa-140">For the maps module to interact with Bing Maps, you must ensure that the following mapping URLs are allowed per your site's content security policy (CSP).</span></span> <span data-ttu-id="952fa-141">Deze instelling wordt uitgevoerd in Commerce Site Builder door toegestane URL's toe te voegen aan verschillende CSP-instructies voor de site (bijvoorbeeld **img-src**).</span><span class="sxs-lookup"><span data-stu-id="952fa-141">This setup is done in Commerce site builder, by adding allowed URLs to various site CSP directives (for example, **img-src**).</span></span> <span data-ttu-id="952fa-142">Zie voor meer informatie [Beveiligingsbeleid voor inhoud](manage-csp.md).</span><span class="sxs-lookup"><span data-stu-id="952fa-142">For more information, see [Content security policy](manage-csp.md).</span></span> 

- <span data-ttu-id="952fa-143">Voeg aan de **connect-src**-richtlijn **&#42;.bing.com** toe.</span><span class="sxs-lookup"><span data-stu-id="952fa-143">To the **connect-src** directive, add **&#42;.bing.com**.</span></span>
- <span data-ttu-id="952fa-144">Voeg aan de **img-src**-richtlijn **&#42;.virtualearth.net** toe.</span><span class="sxs-lookup"><span data-stu-id="952fa-144">To the **img-src** directive, add **&#42;.virtualearth.net**.</span></span>
- <span data-ttu-id="952fa-145">Voeg aan de **script-src**-instructie **&#42;.bing.com, &#42;.virtualearth.net** toe.</span><span class="sxs-lookup"><span data-stu-id="952fa-145">To the **script-src** directive, add **&#42;.bing.com, &#42;.virtualearth.net**.</span></span>
- <span data-ttu-id="952fa-146">Voeg aan de **script style-src**-instructie **&#42;.bing.com** toe.</span><span class="sxs-lookup"><span data-stu-id="952fa-146">To the **script style-src** directive, add **&#42;.bing.com**.</span></span>

## <a name="add-a-map-module-to-a-page"></a><span data-ttu-id="952fa-147">Een kaartmodule toevoegen aan een pagina</span><span class="sxs-lookup"><span data-stu-id="952fa-147">Add a map module to a page</span></span>

<span data-ttu-id="952fa-148">Zie [Winkelselectiemodule](store-selector.md) voor meer informatie over het configureren van een kaartmodule op een pagina.</span><span class="sxs-lookup"><span data-stu-id="952fa-148">For detailed information about how to configure a map module on a page, see [Store selector module](store-selector.md).</span></span> 
 
## <a name="additional-resources"></a><span data-ttu-id="952fa-149">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="952fa-149">Additional resources</span></span>

[<span data-ttu-id="952fa-150">Overzicht van modulebibliotheek</span><span class="sxs-lookup"><span data-stu-id="952fa-150">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="952fa-151">Module met vakje voor kopen</span><span class="sxs-lookup"><span data-stu-id="952fa-151">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="952fa-152">Winkelwagenmodule</span><span class="sxs-lookup"><span data-stu-id="952fa-152">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="952fa-153">Winkelselectiemodule</span><span class="sxs-lookup"><span data-stu-id="952fa-153">Store selector module</span></span>](store-selector.md)

[<span data-ttu-id="952fa-154">Bing Kaarten voor uw organisatie beheren</span><span class="sxs-lookup"><span data-stu-id="952fa-154">Manage Bing Maps for your organization</span></span>](./dev-itpro/manage-bing-maps.md)

[<span data-ttu-id="952fa-155">V8-webbesturingselement van Bing Kaarten</span><span class="sxs-lookup"><span data-stu-id="952fa-155">Bing Maps V8 Web Control</span></span>](https://docs.microsoft.com/bingmaps/v8-web-control/)


[!INCLUDE[footer-include](../includes/footer-banner.md)]