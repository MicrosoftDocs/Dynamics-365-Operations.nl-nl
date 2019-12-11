---
title: Waarschuwingsmodule
description: In dit onderwerp wordt beschreven wat waarschuwingsmodules zijn en hoe u ze toevoegt aan sitepagina's in Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 10/31/2019
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
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 82138dd7f0934f732215f67a3726638eb87075d4
ms.sourcegitcommit: 3a4e137ef3a96ba0a58c5352f4a3b57467ace9ae
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/11/2019
ms.locfileid: "2785347"
---
# <a name="alert-module"></a><span data-ttu-id="fcefc-103">Waarschuwingsmodule</span><span class="sxs-lookup"><span data-stu-id="fcefc-103">Alert module</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="fcefc-104">In dit onderwerp wordt beschreven wat waarschuwingsmodules zijn en hoe u ze toevoegt aan sitepagina's in Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="fcefc-104">This topic covers alert modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="fcefc-105">Overzicht</span><span class="sxs-lookup"><span data-stu-id="fcefc-105">Overview</span></span>

<span data-ttu-id="fcefc-106">Een waarschuwingsmodule wordt gebruikt om inline informatieve berichten op een pagina weer te geven.</span><span class="sxs-lookup"><span data-stu-id="fcefc-106">An alert module is used to show inline informational messages on a page.</span></span> <span data-ttu-id="fcefc-107">Waarschuwingsmodules ondersteunen een tekstbericht en een koppeling.</span><span class="sxs-lookup"><span data-stu-id="fcefc-107">Alert modules support a text message and a link.</span></span> <span data-ttu-id="fcefc-108">Ze kunnen worden gebruikt om promoties op alle pagina's van een e-commerce-site weer te geven.</span><span class="sxs-lookup"><span data-stu-id="fcefc-108">They can be used to show site-wide promotions that appear on all pages of an e-Commerce site.</span></span> 

<span data-ttu-id="fcefc-109">Waarschuwingsmodules worden aangestuurd door gegevens van het Content Management System (CMS) en kunnen op elke willekeurige pagina worden geplaatst.</span><span class="sxs-lookup"><span data-stu-id="fcefc-109">Alert modules are driven by data from the content management system (CMS) and can be put on any page.</span></span>

## <a name="examples-of-alert-modules-in-e-commerce"></a><span data-ttu-id="fcefc-110">Voorbeelden van waarschuwingsmodules in e-commerce</span><span class="sxs-lookup"><span data-stu-id="fcefc-110">Examples of alert modules in e-Commerce</span></span>

<span data-ttu-id="fcefc-111">U kunt waarschuwingsmodules in de koptekst van de site gebruiken om promoties of berichten voor de hele site aan te geven.</span><span class="sxs-lookup"><span data-stu-id="fcefc-111">Alert modules can be used in the site header to indicate site-wide promotions or messages.</span></span> <span data-ttu-id="fcefc-112">Hieronder vindt u enkele voorbeelden:</span><span class="sxs-lookup"><span data-stu-id="fcefc-112">Here are some examples:</span></span>

<span data-ttu-id="fcefc-113">"Jaarlijkse uitverkoop eindigt over 10 dagen"</span><span class="sxs-lookup"><span data-stu-id="fcefc-113">"Annual sale ends in 10 days"</span></span>

<span data-ttu-id="fcefc-114">"Grote besparingen bij terug naar school.</span><span class="sxs-lookup"><span data-stu-id="fcefc-114">"Save big with back to school sale.</span></span> <span data-ttu-id="fcefc-115">Winkel nu."</span><span class="sxs-lookup"><span data-stu-id="fcefc-115">Shop Now."</span></span>

## <a name="alert-module-properties"></a><span data-ttu-id="fcefc-116">Eigenschappen van waarschuwingsmodule</span><span class="sxs-lookup"><span data-stu-id="fcefc-116">Alert module properties</span></span>

| <span data-ttu-id="fcefc-117">Naam van eigenschap.</span><span class="sxs-lookup"><span data-stu-id="fcefc-117">Property name</span></span>  | <span data-ttu-id="fcefc-118">Waarde</span><span class="sxs-lookup"><span data-stu-id="fcefc-118">Value</span></span>                              | <span data-ttu-id="fcefc-119">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="fcefc-119">Description</span></span> |
|----------------|------------------------------------|-------------|
| <span data-ttu-id="fcefc-120">Tekst</span><span class="sxs-lookup"><span data-stu-id="fcefc-120">Text</span></span>           | <span data-ttu-id="fcefc-121">Tekst</span><span class="sxs-lookup"><span data-stu-id="fcefc-121">Text</span></span>                               | <span data-ttu-id="fcefc-122">Het tekstbericht dat wordt weergegeven in de waarschuwingsmodule.</span><span class="sxs-lookup"><span data-stu-id="fcefc-122">The text message that appears in the alert module.</span></span> |
| <span data-ttu-id="fcefc-123">Tekstuitlijning</span><span class="sxs-lookup"><span data-stu-id="fcefc-123">Text alignment</span></span> | <span data-ttu-id="fcefc-124">**Rechts**, **Links** of **Midden**</span><span class="sxs-lookup"><span data-stu-id="fcefc-124">**Right**, **Left**, or **Center**</span></span> | <span data-ttu-id="fcefc-125">Een waarde waarmee wordt gedefinieerd hoe tekst in de waarschuwingsmodule wordt uitgelijnd.</span><span class="sxs-lookup"><span data-stu-id="fcefc-125">A value that defines how text is aligned in the alert module.</span></span> |
| <span data-ttu-id="fcefc-126">Waarschuwing negeren</span><span class="sxs-lookup"><span data-stu-id="fcefc-126">Dismiss alert</span></span>  | <span data-ttu-id="fcefc-127">**True** of **False**</span><span class="sxs-lookup"><span data-stu-id="fcefc-127">**True** or **False**</span></span>              | <span data-ttu-id="fcefc-128">Als de waarde is ingesteld op **True**, kan de klant de waarschuwing sluiten.</span><span class="sxs-lookup"><span data-stu-id="fcefc-128">If the value is set to **True**, the customer can dismiss the alert.</span></span> |
| <span data-ttu-id="fcefc-129">Koppeling</span><span class="sxs-lookup"><span data-stu-id="fcefc-129">Link</span></span>           | <span data-ttu-id="fcefc-130">URL</span><span class="sxs-lookup"><span data-stu-id="fcefc-130">URL</span></span>                                | <span data-ttu-id="fcefc-131">Een URL voor een optionele koppeling.</span><span class="sxs-lookup"><span data-stu-id="fcefc-131">The URL for an optional link.</span></span> |

## <a name="add-an-alert-module-to-a-page"></a><span data-ttu-id="fcefc-132">Een waarschuwingsmodule toevoegen aan een pagina</span><span class="sxs-lookup"><span data-stu-id="fcefc-132">Add an alert module to a page</span></span> 

<span data-ttu-id="fcefc-133">Voer de volgende stappen uit om een waarschuwingsmodule aan een nieuwe pagina toe te voegen en de vereiste eigenschappen in te stellen.</span><span class="sxs-lookup"><span data-stu-id="fcefc-133">To add an alert module to a page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="fcefc-134">Maak een paginasjabloon met de naam **waarschuwingsjabloon**.</span><span class="sxs-lookup"><span data-stu-id="fcefc-134">Create a page template that is named **alert template**.</span></span>
1. <span data-ttu-id="fcefc-135">Voeg in het **hoofdvak** van de standaardpagina een waarschuwingsmodule toe.</span><span class="sxs-lookup"><span data-stu-id="fcefc-135">In the **Main** slot of the default page, add an alert module.</span></span>
1. <span data-ttu-id="fcefc-136">Check de sjabloon in en publiceer deze.</span><span class="sxs-lookup"><span data-stu-id="fcefc-136">Check in the template, and publish it.</span></span> 
1. <span data-ttu-id="fcefc-137">Gebruik de waarschuwingsjabloon die u zojuist hebt gemaakt om een pagina met de naam **waarschuwingspagina** te maken.</span><span class="sxs-lookup"><span data-stu-id="fcefc-137">Use the alert template that you just created to create a page that is named **alert page**.</span></span> 
1. <span data-ttu-id="fcefc-138">Voeg in het **hoofdvak** van de nieuwe pagina een waarschuwingsmodule toe.</span><span class="sxs-lookup"><span data-stu-id="fcefc-138">In the **Main** slot of the new page, add an alert module.</span></span>
1. <span data-ttu-id="fcefc-139">Voer in de instellingen voor de waarschuwingmodule de waarschuwingstekst in.</span><span class="sxs-lookup"><span data-stu-id="fcefc-139">In the settings for the alert module, enter the alert text.</span></span> <span data-ttu-id="fcefc-140">U kunt de andere eigenschappen bewerken als u de waarschuwingsmodule verder wilt aanpassen.</span><span class="sxs-lookup"><span data-stu-id="fcefc-140">You can edit the other properties if you want to customize the alert module further.</span></span>
1. <span data-ttu-id="fcefc-141">Sla de pagina op en bekijk een voorbeeld.</span><span class="sxs-lookup"><span data-stu-id="fcefc-141">Save and preview the page.</span></span> <span data-ttu-id="fcefc-142">Boven aan de pagina wordt een waarschuwing weergegeven met de tekst die u hebt toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="fcefc-142">At the top of the page, you should see an alert that has the text that you added.</span></span>
1. <span data-ttu-id="fcefc-143">Check de pagina in en publiceer deze.</span><span class="sxs-lookup"><span data-stu-id="fcefc-143">Check in the page, and publish it.</span></span> 

## <a name="additional-resources"></a><span data-ttu-id="fcefc-144">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="fcefc-144">Additional resources</span></span>

[<span data-ttu-id="fcefc-145">Overzicht starterskit</span><span class="sxs-lookup"><span data-stu-id="fcefc-145">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="fcefc-146">Carrouselmodule</span><span class="sxs-lookup"><span data-stu-id="fcefc-146">Carousel module</span></span>](add-carousel.md)

[<span data-ttu-id="fcefc-147">Inhoudsrijke-blokmodule</span><span class="sxs-lookup"><span data-stu-id="fcefc-147">Content rich block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="fcefc-148">Module voor het plaatsen van inhoud</span><span class="sxs-lookup"><span data-stu-id="fcefc-148">Content placement module</span></span>](add-content-placement-modules.md)

[<span data-ttu-id="fcefc-149">Functiemodule</span><span class="sxs-lookup"><span data-stu-id="fcefc-149">Feature module</span></span>](add-feature-module.md)

[<span data-ttu-id="fcefc-150">Heldmodule</span><span class="sxs-lookup"><span data-stu-id="fcefc-150">Hero module</span></span>](add-hero-module.md)

[<span data-ttu-id="fcefc-151">Videospelermodule</span><span class="sxs-lookup"><span data-stu-id="fcefc-151">Video player module</span></span>](add-video-player.md)
