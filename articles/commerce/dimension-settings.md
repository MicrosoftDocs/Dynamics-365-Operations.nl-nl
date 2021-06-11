---
title: Weergave-instellingen voor productdimensies toepassen
description: In dit onderwerp worden de weergave-instellingen voor productdimensies besproken en wordt beschreven hoe u deze toepast in Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 05/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: b901622bbfc8d6b3066879f6456a4ab618ca4076
ms.sourcegitcommit: 53b797ff1b524f581046b48cdde42f50b37495bc
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/28/2021
ms.locfileid: "6117217"
---
# <a name="apply-display-settings-for-product-dimensions"></a><span data-ttu-id="e452f-103">Weergave-instellingen voor productdimensies toepassen</span><span class="sxs-lookup"><span data-stu-id="e452f-103">Apply display settings for product dimensions</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="e452f-104">In dit onderwerp worden de weergave-instellingen voor productdimensies besproken en wordt beschreven hoe u deze toepast in Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="e452f-104">This topic covers the display settings for product dimensions and describes how to apply them in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="e452f-105">Dynamics 365 Commerce ondersteunt het gebruik van grootte-, stijl- en kleurdimensies om productvarianten te onderscheiden.</span><span class="sxs-lookup"><span data-stu-id="e452f-105">Dynamics 365 Commerce supports size, style, and color dimensions to distinguish product variants.</span></span> <span data-ttu-id="e452f-106">Dimensies worden meestal weergegeven als tekstwaarden, zoals 'Klein', 'Normaal' en 'Groot' voor grootte, en 'Zwart' en 'Bruin' voor kleuren.</span><span class="sxs-lookup"><span data-stu-id="e452f-106">Dimensions are typically shown as text values, such as "Small," "Medium," and "Large" for sizes, and "Black" and "Brown" for colors.</span></span> <span data-ttu-id="e452f-107">Als een product echter veel variaties ondersteunt, kan het moeilijk zijn om door productvarianten te bladeren omdat er meerdere selecties vereist zijn om de afbeelding voor elke variant weer te geven.</span><span class="sxs-lookup"><span data-stu-id="e452f-107">However, if a product supports many variations, it can be difficult to browse product variants, because multiple selections are required to view the image for each variant.</span></span> <span data-ttu-id="e452f-108">Om het gemakkelijker te maken om door productvarianten te bladeren, kunnen in de versie 10.0.20 van Commerce afbeeldingen en hexadecimale (hex) codes worden gebruikt om dimensies weer te geven als stalen.</span><span class="sxs-lookup"><span data-stu-id="e452f-108">To make it easier to browse product variants, the version 10.0.20 release of Commerce can use images and hexadecimal (hex) codes to show dimensions as swatches.</span></span>

<span data-ttu-id="e452f-109">In Commerce Site Builder worden dimensie-instellingen gedefinieerd via **Site-instellingen \> Extensies \> Dimensie-instellingen**.</span><span class="sxs-lookup"><span data-stu-id="e452f-109">In Commerce site builder, dimension settings are defined at **Site Settings \> Extensions \> Dimension Settings**.</span></span> <span data-ttu-id="e452f-110">In de volgende afbeelding ziet u een voorbeeld van dimensie-instellingen in Site Builder.</span><span class="sxs-lookup"><span data-stu-id="e452f-110">The following illustration shows an example of dimension settings in site builder.</span></span>

![Voorbeeld van site-instellingen in Commerce Site Builder](./dev-itpro/media/swatch_site_settings.PNG)

<span data-ttu-id="e452f-112">Er zijn twee dimensie-instellingen beschikbaar:</span><span class="sxs-lookup"><span data-stu-id="e452f-112">Two dimension settings are available:</span></span>

- <span data-ttu-id="e452f-113">**Dimensies die als afbeelding moeten worden weergegeven**: opgeven welke dimensies als stalen moeten worden weergegeven op pagina's met e-commercesite's, zoals productdetailpagina's (PDP's) en lijstpagina's met zoekresultaten.</span><span class="sxs-lookup"><span data-stu-id="e452f-113">**Dimensions to display as image** – Specify which dimensions should appear as swatches on e-commerce site pages such as product details pages (PDPs) and search result list pages.</span></span> <span data-ttu-id="e452f-114">Elke combinatie van kleur-, grootte- en stijldimensies kan als een staal worden weergegeven.</span><span class="sxs-lookup"><span data-stu-id="e452f-114">Any combination of color, size, and style dimensions can be shown as a swatch.</span></span> <span data-ttu-id="e452f-115">Als een dimensie wordt geselecteerd voor weergave als een staal, wordt met de rendering van de Commerce-module gezocht naar een beschikbare configuratie van een hexcodestaal.</span><span class="sxs-lookup"><span data-stu-id="e452f-115">If a dimension is selected for display as a swatch, Commerce module rendering will look for an available configuration of a hex code swatch.</span></span> <span data-ttu-id="e452f-116">Als er geen hexcode is geconfigureerd, wordt via de systeemlogica naar een configuratie van een staal op basis van een afbeeldings-URL gezocht.</span><span class="sxs-lookup"><span data-stu-id="e452f-116">If no hex code is configured, system logic will look for a configuration of an image URL swatch.</span></span> <span data-ttu-id="e452f-117">Als noch een hexcode noch een afbeeldings-URL is geconfigureerd, wordt tekst weergegeven.</span><span class="sxs-lookup"><span data-stu-id="e452f-117">If neither a hex code nor an image URL is configured, text will be shown.</span></span>

    <span data-ttu-id="e452f-118">De onderstaande afbeelding toont een voorbeeld waarin een PDP op een e-commercesite kleur- en groottestalen bevat.</span><span class="sxs-lookup"><span data-stu-id="e452f-118">The following illustration shows an example where a PDP on an e-commerce site includes color and size swatches.</span></span> <span data-ttu-id="e452f-119">In dit voorbeeld wordt een hexcode geconfigureerd voor de kleurdimensie.</span><span class="sxs-lookup"><span data-stu-id="e452f-119">In this example, a hex code is configured for the color dimension.</span></span> <span data-ttu-id="e452f-120">Daarom worden stalen als kleuren weergegeven.</span><span class="sxs-lookup"><span data-stu-id="e452f-120">Therefore, swatches are shown as colors.</span></span> <span data-ttu-id="e452f-121">Voor de groottedimensie worden echter noch hexcodes noch afbeeldings-URL´s geconfigureerd.</span><span class="sxs-lookup"><span data-stu-id="e452f-121">However, neither a hex code nor an image URL is configured for the size dimension.</span></span> <span data-ttu-id="e452f-122">Daarom wordt tekst weergegeven.</span><span class="sxs-lookup"><span data-stu-id="e452f-122">Therefore, text is shown.</span></span>

    ![Voorbeeld van de kleurdimensie die als stalen op een pagina met productdetails voor e-commerce wordt weergegeven](./dev-itpro/media/swatch_pdp.png)

- <span data-ttu-id="e452f-124">**Dimensies die op een productkaart moeten worden weergegeven** – opgeven welke dimensies moeten worden weergegeven op productkaarten die worden weergegeven in lijsten en op lijstpagina's.</span><span class="sxs-lookup"><span data-stu-id="e452f-124">**Dimensions to display in product card** – Specify which dimensions should appear on product cards that are shown in lists and on list pages.</span></span> <span data-ttu-id="e452f-125">Voordat een dimensie op een productkaart kan worden weergegeven, moet deze instelling voor die dimensie zijn ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="e452f-125">Before a dimension can appear on a product card, this setting must be enabled for that dimension.</span></span> <span data-ttu-id="e452f-126">De instelling **Dimensies die als afbeelding moeten worden weergegeven** moet ook worden ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="e452f-126">The **Dimensions to display as image** setting should also be enabled.</span></span> <span data-ttu-id="e452f-127">Het gedrag van staalselectie op productkaarten is geoptimaliseerd voor de kleurdimensie.</span><span class="sxs-lookup"><span data-stu-id="e452f-127">The swatch selection behavior on product cards is optimized for the color dimension.</span></span> <span data-ttu-id="e452f-128">Voor andere dimensies is mogelijk een weergave-extensie vereist voor het aanpassen van het gedrag van staalselectie.</span><span class="sxs-lookup"><span data-stu-id="e452f-128">For other dimensions, a view extension might be required to customize swatch selection behavior.</span></span>

    <span data-ttu-id="e452f-129">De onderstaande afbeelding toont een voorbeeld waarbij een lijstpagina op een e-commercesite productkaarten bevat die kleurstalen bevatten.</span><span class="sxs-lookup"><span data-stu-id="e452f-129">The following illustration shows an example where a list page on an e-commerce site contains product cards that include color swatches.</span></span>

    ![Voorbeeld van de kleurdimensie die als stalen op een lijstpagina voor e-commerce wordt weergegeven](./dev-itpro/media/swatch_searchresults.PNG)

<span data-ttu-id="e452f-131">Zie [Productdimensiewaarden configureren zodat deze als stalen worden weergegeven](./dev-itpro/dimensions-swatch.md) voor informatie over het configureren van productdimensies zodat deze worden weergegeven als stalen op sitepagina´s.</span><span class="sxs-lookup"><span data-stu-id="e452f-131">For information about how to configure product dimensions so that they are shown as swatches on site pages, see [Configure product dimension values to appear as swatches](./dev-itpro/dimensions-swatch.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e452f-132">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="e452f-132">Additional resources</span></span>

[<span data-ttu-id="e452f-133">Overzicht van modulebibliotheek</span><span class="sxs-lookup"><span data-stu-id="e452f-133">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="e452f-134">Module voor zoekresultaten</span><span class="sxs-lookup"><span data-stu-id="e452f-134">Search results module</span></span>](search-result-module.md)

[<span data-ttu-id="e452f-135">Module met vakje voor kopen</span><span class="sxs-lookup"><span data-stu-id="e452f-135">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="e452f-136">Productdimensiewaarden configureren die als stalen moeten worden weergegeven</span><span class="sxs-lookup"><span data-stu-id="e452f-136">Configure product dimension values to appear as swatches</span></span>](./dev-itpro/dimensions-swatch.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
