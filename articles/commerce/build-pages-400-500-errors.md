---
title: Aangepaste antwoordpagina's bouwen voor fouten met de statuscode 4xx/5xx
description: In dit onderwerp wordt beschreven hoe u aangepaste antwoordpagina's kunt maken voor de statusfoutcodes 4xx en 5xx met behulp van de ontwerpfuncties in Microsoft Dynamics 365 Commerce.
author: v-chgri
manager: annbe
ms.date: 10/01/2019
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
ms.openlocfilehash: 4477a0a43971b5322c6acd6971cba2e79e2dc8c6
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/01/2020
ms.locfileid: "3001114"
---
# <a name="build-custom-response-pages-for-4xx5xx-status-code-errors"></a><span data-ttu-id="de94d-103">Aangepaste antwoordpagina's bouwen voor fouten met de statuscode 4xx/5xx</span><span class="sxs-lookup"><span data-stu-id="de94d-103">Build custom response pages for 4xx/5xx status code errors</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="de94d-104">In dit onderwerp wordt beschreven hoe u aangepaste antwoordpagina's kunt maken voor de statusfoutcodes 4xx en 5xx met behulp van de ontwerpfuncties in Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="de94d-104">This topic describes how to build custom response pages for 4xx and 5xx status code errors by using the authoring tools in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="de94d-105">Overzicht</span><span class="sxs-lookup"><span data-stu-id="de94d-105">Overview</span></span>

<span data-ttu-id="de94d-106">Als een aanvraag misukt, verzendt de server een reactie met een HTTP-statuscode.</span><span class="sxs-lookup"><span data-stu-id="de94d-106">If a request isn't successful, the server issues HTTP status code error responses.</span></span> <span data-ttu-id="de94d-107">De 404-statuscode wordt vastgelegd en geretourneerd als een pagina niet wordt gevonden en de 500-statuscode wordt vastgelegd en geretourneerd als er een serverfout optreedt.</span><span class="sxs-lookup"><span data-stu-id="de94d-107">The 404 status code is captured and returned if a page isn't found, and the 500 status code is captured and returned if a server error occurs.</span></span> <span data-ttu-id="de94d-108">In Dynamics 365 Commerce kunnen toepassingsgebruikers aangepaste antwoordpagina's met statusfoutcodes maken die worden weergegeven aan gebruikers als reactie voor deze statuscodes.</span><span class="sxs-lookup"><span data-stu-id="de94d-108">In Dynamics 365 Commerce, application users can build custom status code error response pages that are shown to users for these status code error responses.</span></span>

## <a name="build-a-status-code-error-response-page"></a><span data-ttu-id="de94d-109">Een antwoordpagina maken voor statusfoutcodes</span><span class="sxs-lookup"><span data-stu-id="de94d-109">Build a status code error response page</span></span>

<span data-ttu-id="de94d-110">Ga als volgt te werk om een antwoordpagina voor een statusfoutcode te maken.</span><span class="sxs-lookup"><span data-stu-id="de94d-110">To start to build a status code error response page, follow these steps.</span></span>

1. <span data-ttu-id="de94d-111">Meld u aan bij Dynamics 365 Commerce in de webbrowser van uw voorkeur.</span><span class="sxs-lookup"><span data-stu-id="de94d-111">In your preferred web browser, sign in to Dynamics 365 Commerce.</span></span> 
1. <span data-ttu-id="de94d-112">Selecteer de site waarvoor u een antwoordpagina wilt maken voor fouten met de statuscode 4xx/5xx.</span><span class="sxs-lookup"><span data-stu-id="de94d-112">Select the site that you want to build a 4xx/5xx status code error response page for.</span></span>

### <a name="build-the-template"></a><span data-ttu-id="de94d-113">De sjabloon samenstellen</span><span class="sxs-lookup"><span data-stu-id="de94d-113">Build the template</span></span>

<span data-ttu-id="de94d-114">Ga als volgt te werk om de sjabloon te maken voor een antwoordpagina voor de statusfoutcode.</span><span class="sxs-lookup"><span data-stu-id="de94d-114">To build the template for the status code error response page, follow these steps.</span></span>

1. <span data-ttu-id="de94d-115">Ga naar **Sjablonen \> NIeuwe sjabloon**.</span><span class="sxs-lookup"><span data-stu-id="de94d-115">Go to **Templates \> New template**.</span></span>
1. <span data-ttu-id="de94d-116">Geef de nieuwe sjabloon een naam.</span><span class="sxs-lookup"><span data-stu-id="de94d-116">Name the new template.</span></span>
1. <span data-ttu-id="de94d-117">Bouw de sjabloon op basis van de gewenste structuur voor de antwoordpagina van de statusfoutcode.</span><span class="sxs-lookup"><span data-stu-id="de94d-117">Build the template, based on the structure that you want the status code error response page to have.</span></span>
1. <span data-ttu-id="de94d-118">Check de sjabloon in en publiceer deze.</span><span class="sxs-lookup"><span data-stu-id="de94d-118">Check the template in, and publish it.</span></span>

### <a name="build-the-status-code-error-response-page"></a><span data-ttu-id="de94d-119">De antwoordpagina maken voor statusfoutcodes</span><span class="sxs-lookup"><span data-stu-id="de94d-119">Build the status code error response page</span></span>

<span data-ttu-id="de94d-120">Ga als volgt te werk om de antwoordpagina voor een statusfoutcode te maken.</span><span class="sxs-lookup"><span data-stu-id="de94d-120">To build the status code error response page, follow these steps.</span></span>

1. <span data-ttu-id="de94d-121">Ga naar **Pagina's \> Nieuwe pagina**.</span><span class="sxs-lookup"><span data-stu-id="de94d-121">Go to **Pages \> New Page**.</span></span>
1. <span data-ttu-id="de94d-122">Geef de antwoordpagina met de statusfoutcode een naam, maar stel **niet** het **URL**-veld in.</span><span class="sxs-lookup"><span data-stu-id="de94d-122">Name the status code error response page, but do **not** set the **URL** field.</span></span>
1. <span data-ttu-id="de94d-123">Maak de pagina.</span><span class="sxs-lookup"><span data-stu-id="de94d-123">Build the page.</span></span>
1. <span data-ttu-id="de94d-124">Check de pagina in en publiceer deze.</span><span class="sxs-lookup"><span data-stu-id="de94d-124">Check the page in, and publish it.</span></span>

> [!NOTE]
> <span data-ttu-id="de94d-125">U kunt afzonderlijke antwoordpagina's maken voor fouten met de statuscodes 4xx en 5xx.</span><span class="sxs-lookup"><span data-stu-id="de94d-125">You can create separate status code error response pages for 4xx and 5xx status code errors.</span></span> <span data-ttu-id="de94d-126">U kunt ook dezelfde algemene antwoordpagina met de statusfoutcode gebruiken voor beide foutcategorieën.</span><span class="sxs-lookup"><span data-stu-id="de94d-126">Alternatively, you can use the same general status code error response page for both error categories.</span></span>

### <a name="set-up-a-redirect-for-the-status-code-error-response-page"></a><span data-ttu-id="de94d-127">Een omleiding instellen voor de antwoordpagina voor de statusfoutcode</span><span class="sxs-lookup"><span data-stu-id="de94d-127">Set up a redirect for the status code error response page</span></span>

<span data-ttu-id="de94d-128">Ga als volgt te werk om een omleiding te maken voor een antwoordpagina voor de statusfoutcode.</span><span class="sxs-lookup"><span data-stu-id="de94d-128">To set up a redirect for the status code error response page, follow these steps.</span></span>

1. <span data-ttu-id="de94d-129">Ga naar **URL's \> Nieuw \> Nieuwe alias**en selecteer de antwoordpagina voor de statusfoutcode die u eerder hebt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="de94d-129">Go to **URLs \> New \> New Alias**, and select the status code error response page that you built earlier.</span></span>
1. <span data-ttu-id="de94d-130">Voer in het veld **Alias** de waarde **default-4xx** of **default-5xx** in, afhankelijk van de antwoordpagina voor de statusfoutcode waarvoor u een omleiding wilt instellen.</span><span class="sxs-lookup"><span data-stu-id="de94d-130">In the **Alias** field, enter either **default-4xx** or **default-5xx**, depending on the status code error response page that you're setting up a redirect for.</span></span> <span data-ttu-id="de94d-131">Deze aliassen moeten worden gepubliceerd.</span><span class="sxs-lookup"><span data-stu-id="de94d-131">These aliases must be published.</span></span> <span data-ttu-id="de94d-132">Anders werkt de omleiding niet.</span><span class="sxs-lookup"><span data-stu-id="de94d-132">Otherwise, the redirect won't work.</span></span>
1. <span data-ttu-id="de94d-133">Selecteer **OK** om de koppeling uit te voeren.</span><span class="sxs-lookup"><span data-stu-id="de94d-133">Select **OK** to commit the linking.</span></span>

> [!NOTE]
> <span data-ttu-id="de94d-134">Als u één antwoordpagina voor de statusfoutcode gebruikt voor beide foutcategorieën, herhaalt u deze procedure om een alias voor de andere foutcategorie aan dezelfde pagina te koppelen.</span><span class="sxs-lookup"><span data-stu-id="de94d-134">If you're using a single status code error response page for both error categories, repeat this procedure to link an alias for the other error category to the same page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="de94d-135">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="de94d-135">Additional resources</span></span>

[<span data-ttu-id="de94d-136">Werken met sjablonen</span><span class="sxs-lookup"><span data-stu-id="de94d-136">Work with templates</span></span>](work-with-templates.md)

[<span data-ttu-id="de94d-137">Een nieuwe sitepagina toevoegen</span><span class="sxs-lookup"><span data-stu-id="de94d-137">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="de94d-138">Een pagina-URL maken</span><span class="sxs-lookup"><span data-stu-id="de94d-138">Create a page URL</span></span>](create-page-url.md)
