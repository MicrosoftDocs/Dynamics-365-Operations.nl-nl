---
title: Aangepaste antwoordpagina's bouwen voor fouten met de statuscode 4xx/5xx
description: In dit onderwerp wordt beschreven hoe u aangepaste antwoordpagina's kunt maken voor de statusfoutcodes 4xx en 5xx met behulp van de ontwerpfuncties in Microsoft Dynamics 365 Commerce.
author: v-chgri
manager: annbe
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: josaw
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 060f5e5616624279711f61f582e6a898c7eb7785
ms.sourcegitcommit: 7a1d01122790b904e2d96a7ea9f1d003392358a6
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/17/2020
ms.locfileid: "3269539"
---
# <a name="build-custom-response-pages-for-4xx5xx-status-code-errors"></a><span data-ttu-id="d8236-103">Aangepaste antwoordpagina's bouwen voor fouten met de statuscode 4xx/5xx</span><span class="sxs-lookup"><span data-stu-id="d8236-103">Build custom response pages for 4xx/5xx status code errors</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="d8236-104">In dit onderwerp wordt beschreven hoe u aangepaste antwoordpagina's kunt maken voor de statusfoutcodes 4xx en 5xx met behulp van de ontwerpfuncties in Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="d8236-104">This topic describes how to build custom response pages for 4xx and 5xx status code errors by using the authoring tools in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="d8236-105">Overzicht</span><span class="sxs-lookup"><span data-stu-id="d8236-105">Overview</span></span>

<span data-ttu-id="d8236-106">Als een aanvraag misukt, verzendt de server een reactie met een HTTP-statuscode.</span><span class="sxs-lookup"><span data-stu-id="d8236-106">If a request isn't successful, the server issues HTTP status code error responses.</span></span> <span data-ttu-id="d8236-107">De 404-statuscode wordt vastgelegd en geretourneerd als een pagina niet wordt gevonden en de 500-statuscode wordt vastgelegd en geretourneerd als er een serverfout optreedt.</span><span class="sxs-lookup"><span data-stu-id="d8236-107">The 404 status code is captured and returned if a page isn't found, and the 500 status code is captured and returned if a server error occurs.</span></span> <span data-ttu-id="d8236-108">In Dynamics 365 Commerce kunnen toepassingsgebruikers aangepaste antwoordpagina's met statusfoutcodes maken die worden weergegeven aan gebruikers als reactie voor deze statuscodes.</span><span class="sxs-lookup"><span data-stu-id="d8236-108">In Dynamics 365 Commerce, application users can build custom status code error response pages that are shown to users for these status code error responses.</span></span>

## <a name="build-a-status-code-error-response-page"></a><span data-ttu-id="d8236-109">Een antwoordpagina maken voor statusfoutcodes</span><span class="sxs-lookup"><span data-stu-id="d8236-109">Build a status code error response page</span></span>

<span data-ttu-id="d8236-110">Ga als volgt te werk om een antwoordpagina voor een statusfoutcode te maken.</span><span class="sxs-lookup"><span data-stu-id="d8236-110">To start to build a status code error response page, follow these steps.</span></span>

1. <span data-ttu-id="d8236-111">Meld u aan bij Dynamics 365 Commerce in de webbrowser van uw voorkeur.</span><span class="sxs-lookup"><span data-stu-id="d8236-111">In your preferred web browser, sign in to Dynamics 365 Commerce.</span></span> 
1. <span data-ttu-id="d8236-112">Selecteer de site waarvoor u een antwoordpagina wilt maken voor fouten met de statuscode 4xx/5xx.</span><span class="sxs-lookup"><span data-stu-id="d8236-112">Select the site that you want to build a 4xx/5xx status code error response page for.</span></span>

### <a name="build-the-template"></a><span data-ttu-id="d8236-113">De sjabloon samenstellen</span><span class="sxs-lookup"><span data-stu-id="d8236-113">Build the template</span></span>

<span data-ttu-id="d8236-114">Ga als volgt te werk om de sjabloon te maken voor een antwoordpagina voor de statusfoutcode.</span><span class="sxs-lookup"><span data-stu-id="d8236-114">To build the template for the status code error response page, follow these steps.</span></span>

1. <span data-ttu-id="d8236-115">Ga naar **Sjablonen**.</span><span class="sxs-lookup"><span data-stu-id="d8236-115">Go to **Templates**.</span></span>
1. <span data-ttu-id="d8236-116">Selecteer **Nieuw** om een paginasjabloon te maken.</span><span class="sxs-lookup"><span data-stu-id="d8236-116">Select **New** to create a page template.</span></span>
1. <span data-ttu-id="d8236-117">Voer in het dialoogvenster **Nieuwe sjabloon** onder **Sjabloonnaam** een naam in voor de nieuwe sjabloon en selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="d8236-117">In the **New Template** dialog box, under **Template Name**, enter a name for the new template, and then select **OK**.</span></span>
1. <span data-ttu-id="d8236-118">Bouw de sjabloon op basis van de gewenste structuur voor de antwoordpagina van de statusfoutcode.</span><span class="sxs-lookup"><span data-stu-id="d8236-118">Build the template, based on the structure that you want the status code error response page to have.</span></span>
1. <span data-ttu-id="d8236-119">Selecteer **Opslaan**, selecteer **Bewerken voltooien** om de sjabloon in te checken en selecteer **Publiceren** om te publiceren.</span><span class="sxs-lookup"><span data-stu-id="d8236-119">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span> 

### <a name="build-the-status-code-error-response-page"></a><span data-ttu-id="d8236-120">De antwoordpagina maken voor statusfoutcodes</span><span class="sxs-lookup"><span data-stu-id="d8236-120">Build the status code error response page</span></span>

<span data-ttu-id="d8236-121">Ga als volgt te werk om de antwoordpagina voor een statusfoutcode te maken.</span><span class="sxs-lookup"><span data-stu-id="d8236-121">To build the status code error response page, follow these steps.</span></span>

1. <span data-ttu-id="d8236-122">Ga naar **Pagina's**.</span><span class="sxs-lookup"><span data-stu-id="d8236-122">Go to **Pages**.</span></span>
1. <span data-ttu-id="d8236-123">Selecteer **Nieuw** om een pagina te maken.</span><span class="sxs-lookup"><span data-stu-id="d8236-123">Select **New** to create a page.</span></span>
1. <span data-ttu-id="d8236-124">Selecteer in het dialoogvenster **Een sjabloon kiezen** een sjabloon en voer vervolgens onder **Paginanaam** een naam in voor de pagina met de statusfoutcode.</span><span class="sxs-lookup"><span data-stu-id="d8236-124">In the **Choose a template** dialog box, select a template, and then, under **Page name**, enter a name for the status code error response page.</span></span> <span data-ttu-id="d8236-125">Laat het veld **Pagina-URL** leeg.</span><span class="sxs-lookup"><span data-stu-id="d8236-125">Leave the **Page URL** field blank.</span></span>
1. <span data-ttu-id="d8236-126">Maak de pagina.</span><span class="sxs-lookup"><span data-stu-id="d8236-126">Build the page.</span></span>
1. <span data-ttu-id="d8236-127">Selecteer **Opslaan**, selecteer **Bewerken voltooien** om de pagina in te checken en selecteer **Publiceren** om te publiceren.</span><span class="sxs-lookup"><span data-stu-id="d8236-127">Select **Save**, select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

> [!NOTE]
> <span data-ttu-id="d8236-128">U kunt afzonderlijke antwoordpagina's maken voor fouten met de statuscodes 4xx en 5xx.</span><span class="sxs-lookup"><span data-stu-id="d8236-128">You can create separate status code error response pages for 4xx and 5xx status code errors.</span></span> <span data-ttu-id="d8236-129">U kunt ook dezelfde algemene antwoordpagina met de statusfoutcode gebruiken voor beide foutcategorieën.</span><span class="sxs-lookup"><span data-stu-id="d8236-129">Alternatively, you can use the same general status code error response page for both error categories.</span></span>

### <a name="set-up-a-redirect-for-the-status-code-error-response-page"></a><span data-ttu-id="d8236-130">Een omleiding instellen voor de antwoordpagina voor de statusfoutcode</span><span class="sxs-lookup"><span data-stu-id="d8236-130">Set up a redirect for the status code error response page</span></span>

<span data-ttu-id="d8236-131">Ga als volgt te werk om een omleiding te maken voor een antwoordpagina voor de statusfoutcode.</span><span class="sxs-lookup"><span data-stu-id="d8236-131">To set up a redirect for the status code error response page, follow these steps.</span></span>

1. <span data-ttu-id="d8236-132">Ga naar **URL's \> Nieuw \> Nieuwe alias**en selecteer de antwoordpagina voor de statusfoutcode die u eerder hebt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="d8236-132">Go to **URLs \> New \> New Alias**, and select the status code error response page that you built earlier.</span></span>
1. <span data-ttu-id="d8236-133">Voer in het veld **Alias** de waarde **default-4xx** of **default-5xx** in, afhankelijk van de antwoordpagina voor de statusfoutcode waarvoor u een omleiding wilt instellen.</span><span class="sxs-lookup"><span data-stu-id="d8236-133">In the **Alias** field, enter either **default-4xx** or **default-5xx**, depending on the status code error response page that you're setting up a redirect for.</span></span> <span data-ttu-id="d8236-134">Deze aliassen moeten worden gepubliceerd.</span><span class="sxs-lookup"><span data-stu-id="d8236-134">These aliases must be published.</span></span> <span data-ttu-id="d8236-135">Anders werkt de omleiding niet.</span><span class="sxs-lookup"><span data-stu-id="d8236-135">Otherwise, the redirect won't work.</span></span>
1. <span data-ttu-id="d8236-136">Selecteer **OK** om de koppeling uit te voeren.</span><span class="sxs-lookup"><span data-stu-id="d8236-136">Select **OK** to commit the linking.</span></span>

> [!NOTE]
> <span data-ttu-id="d8236-137">Als u één antwoordpagina voor de statusfoutcode gebruikt voor beide foutcategorieën, herhaalt u deze procedure om een alias voor de andere foutcategorie aan dezelfde pagina te koppelen.</span><span class="sxs-lookup"><span data-stu-id="d8236-137">If you're using a single status code error response page for both error categories, repeat this procedure to link an alias for the other error category to the same page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d8236-138">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="d8236-138">Additional resources</span></span>

[<span data-ttu-id="d8236-139">Werken met sjablonen</span><span class="sxs-lookup"><span data-stu-id="d8236-139">Work with templates</span></span>](work-with-templates.md)

[<span data-ttu-id="d8236-140">Een nieuwe sitepagina toevoegen</span><span class="sxs-lookup"><span data-stu-id="d8236-140">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="d8236-141">Een pagina-URL maken</span><span class="sxs-lookup"><span data-stu-id="d8236-141">Create a page URL</span></span>](create-page-url.md)
