---
title: Een e-commerce-site maken
description: In dit onderwerp worden de stappen en informatie beschreven die nodig zijn om een nieuwe e-Commerce-site in Dynamics 365 Commerce site builder te maken.
author: bicyclingfool
manager: AnnBe
ms.date: 01/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: stuharg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 3d3d8a290f06d9734be21f2d59152acac6857506
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/01/2020
ms.locfileid: "3002008"
---
# <a name="create-an-e-commerce-site"></a><span data-ttu-id="e365e-103">Een e-commerce-site maken</span><span class="sxs-lookup"><span data-stu-id="e365e-103">Create an e-Commerce site</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="e365e-104">In dit onderwerp worden de stappen en informatie beschreven die nodig zijn om een nieuwe e-Commerce-site in Dynamics 365 Commerce site builder te maken.</span><span class="sxs-lookup"><span data-stu-id="e365e-104">This topic describes the steps and information required to create a new e-Commerce site in Dynamics 365 Commerce site builder.</span></span>

<span data-ttu-id="e365e-105">Als u uw e-Commerce-site wilt gaan ontwikkelen, moet u eerst een nieuwe site in site builder maken.</span><span class="sxs-lookup"><span data-stu-id="e365e-105">Before you can start developing your e-Commerce site, you must first establish a new site in site builder.</span></span> 


<span data-ttu-id="e365e-106">Als u uw e-commerce-site wilt gaan ontwikkelen, moet u eerst een nieuwe site in de ontwerpomgeving van de si te maken.</span><span class="sxs-lookup"><span data-stu-id="e365e-106">To start to develop your e-Commerce site, you must first establish a new site in the site authoring environment.</span></span> <span data-ttu-id="e365e-107">Voordat u een nieuwe site kunt maken, moet er minimaal één online winkel zijn gemaakt in Commerce.</span><span class="sxs-lookup"><span data-stu-id="e365e-107">Before you can create a new site, at least one online store must be created in Commerce.</span></span> 


## <a name="set-up-your-site"></a><span data-ttu-id="e365e-108">Uw site instellen</span><span class="sxs-lookup"><span data-stu-id="e365e-108">Set up your site</span></span>

<span data-ttu-id="e365e-109">Ga als volgt te werk als u uw site wilt instellen.</span><span class="sxs-lookup"><span data-stu-id="e365e-109">To set up your site, do the following.</span></span>

1. <span data-ttu-id="e365e-110">Open de site builder-omgeving.</span><span class="sxs-lookup"><span data-stu-id="e365e-110">Open the site builder environment.</span></span> <span data-ttu-id="e365e-111">U vindt een koppeling naar de site builder in Microsoft Lifecycle Services (LCS) op de pagina omgevingsfuncties voor Commerce.</span><span class="sxs-lookup"><span data-stu-id="e365e-111">You can find a link to site builder in Microsoft Lifecycle Services (LCS) in the environment features page for Commerce.</span></span>
1. <span data-ttu-id="e365e-112">Selecteer **Nieuwe site** op de startpagina voor de ontwerpomgeving voor sites.</span><span class="sxs-lookup"><span data-stu-id="e365e-112">On the home page for the site authoring environment, select **New site**.</span></span>
1. <span data-ttu-id="e365e-113">Geef in het dialoogvenster **Nieuwe site** de volgende informatie op.</span><span class="sxs-lookup"><span data-stu-id="e365e-113">In the **New site** dialog box, provide the following information.</span></span>

| <span data-ttu-id="e365e-114">Veld</span><span class="sxs-lookup"><span data-stu-id="e365e-114">Field</span></span>                               | <span data-ttu-id="e365e-115">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="e365e-115">Description</span></span> |
|-------------------------------------|-------------|
| <span data-ttu-id="e365e-116">Sitenaam</span><span class="sxs-lookup"><span data-stu-id="e365e-116">Site name</span></span>                           | <span data-ttu-id="e365e-117">Voer de weergavenaam in die moet worden gebruikt voor uw site in de ontwerpomgeving.</span><span class="sxs-lookup"><span data-stu-id="e365e-117">Enter the display name that should be used for your site in the site authoring environment.</span></span> <span data-ttu-id="e365e-118">Deze naam is alleen zichtbaar in de ontwerpomgeving en wordt niet weergegeven voor klanten.</span><span class="sxs-lookup"><span data-stu-id="e365e-118">This name is visible only in the authoring environment and will not be shown to customers.</span></span> |
| <span data-ttu-id="e365e-119">Beveiligingsgroep van de sitebeheerder</span><span class="sxs-lookup"><span data-stu-id="e365e-119">Site administrator's security group</span></span> | <span data-ttu-id="e365e-120">Geef de beveiligingsgroep voor Microsoft Azure Active Directory (Azure AD) op waarmee gebruikers met de rol van sitebeheerder op deze site worden beheerd.</span><span class="sxs-lookup"><span data-stu-id="e365e-120">Specify the Microsoft Azure Active Directory (Azure AD) security group that manages users who have the site administrator role in this site.</span></span> |
| <span data-ttu-id="e365e-121">Standaardkanaal (nummer operationele eenheid)</span><span class="sxs-lookup"><span data-stu-id="e365e-121">Default channel (operating unit number)</span></span> | <span data-ttu-id="e365e-122">Selecteer de online winkel waarvoor deze site als webwinkel zal dienen.</span><span class="sxs-lookup"><span data-stu-id="e365e-122">Select the online store that this site will serve as the web storefront for.</span></span> <span data-ttu-id="e365e-123">Als u wilt dat uw e-commerce-site meerdere online winkels ondersteunt, moet u de winkels aan uw site koppelen in de **Site-instellingen** nadat de site is ingesteld.</span><span class="sxs-lookup"><span data-stu-id="e365e-123">If you want your e-Commerce site to support multiple online stores, you must associate the stores with your site in **Site settings** after the site is set up.</span></span> |
| <span data-ttu-id="e365e-124">Standaardtaal</span><span class="sxs-lookup"><span data-stu-id="e365e-124">Default language</span></span>                            | <span data-ttu-id="e365e-125">Geef de standaardtaal op voor deze online winkel en markt.</span><span class="sxs-lookup"><span data-stu-id="e365e-125">Specify the default language for this online store and market.</span></span> <span data-ttu-id="e365e-126">Een online winkel kan meerdere talen ondersteunen.</span><span class="sxs-lookup"><span data-stu-id="e365e-126">An online store can support multiple languages.</span></span> <span data-ttu-id="e365e-127">Als u meerdere talen wilt ondersteunen voor deze online winkel of een andere online winkel, kunt u dat configureren in **Site-instellingen** nadat de site is ingesteld.</span><span class="sxs-lookup"><span data-stu-id="e365e-127">If you want to support multiple languages for this online store or another online store, you can configure that support in **Site settings** after the site is set up.</span></span>  |
| <span data-ttu-id="e365e-128">Domein</span><span class="sxs-lookup"><span data-stu-id="e365e-128">Domain</span></span>                              | <span data-ttu-id="e365e-129">Selecteer een domein dat als domein zal dienen voor deze online winkel.</span><span class="sxs-lookup"><span data-stu-id="e365e-129">Select a domain name that will serve as the domain for this online store.</span></span> <span data-ttu-id="e365e-130">Als u geen domeinen in LCS hebt geconfigureerd, kunt u dit veld leeg laten.</span><span class="sxs-lookup"><span data-stu-id="e365e-130">If you haven't configured any domains in LCS, you can leave this field blank.</span></span> <span data-ttu-id="e365e-131">Nadat uw domein in LCS is geconfigureerd, moet u dit aan uw online winkel toevoegen in de **Site-instellingen**.</span><span class="sxs-lookup"><span data-stu-id="e365e-131">After your domain is configured in LCS, you must add it to your online store in **Site settings**.</span></span>  |
| <span data-ttu-id="e365e-132">Pad</span><span class="sxs-lookup"><span data-stu-id="e365e-132">Path</span></span>                              | <span data-ttu-id="e365e-133">Wanneer uw site meerdere talen ondersteunt voor een bepaalde domeinnaam, gebruikt u het padveld om een unieke site-URL te maken voor die domein- en taalcombinatie.</span><span class="sxs-lookup"><span data-stu-id="e365e-133">When your site supports more than one language for a given domain name, use the path field to create a unique site URL for that domain and language combination.</span></span> <span data-ttu-id="e365e-134">Als de taal die u hebt opgegeven in het veld **Standaardtaal** de enige taal is die u voor dit domein wilt gebruiken of de standaardtaal blijft nadat u uw site hebt gelokaliseerd in extra talen, wordt u aangeraden dit veld leeg te laten.</span><span class="sxs-lookup"><span data-stu-id="e365e-134">If the language you specified in the **Default language** field is the only language you will support for this domain, or will continue to be the default language after you have localized your site into additional languages, we recommend that you leave this field empty.</span></span> |


<span data-ttu-id="e365e-135">Nadat de site is gemaakt, kunt u controleren of deze is gekoppeld aan uw online winkel door het tabblad **Producten** te selecteren. Het assortiment met producten dat aan de online winkel is toegewezen, wordt weergeven.</span><span class="sxs-lookup"><span data-stu-id="e365e-135">After your site is created, you can verify that it is associated with your online store by selecting the **Products** tab. You should see the assortment of products that has been allocated to the online store.</span></span> <span data-ttu-id="e365e-136">U kunt ook het vervolgkeuzemenu in de linkerbovenhoek van de pagina gebruiken om toegang te krijgen tot de toegewezen producten per categorie.</span><span class="sxs-lookup"><span data-stu-id="e365e-136">You can also use the drop-down menu in the upper left of the page to access the allocated products by category.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e365e-137">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="e365e-137">Additional resources</span></span>

[<span data-ttu-id="e365e-138">Uw domeinnaam configureren</span><span class="sxs-lookup"><span data-stu-id="e365e-138">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="e365e-139">Een nieuwe e-commerce-site implementeren</span><span class="sxs-lookup"><span data-stu-id="e365e-139">Deploy a new e-Commerce site</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="e365e-140">Een online-site koppelen aan een kanaal</span><span class="sxs-lookup"><span data-stu-id="e365e-140">Associate an online site with a channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="e365e-141">Robots.txt-bestanden beheren</span><span class="sxs-lookup"><span data-stu-id="e365e-141">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="e365e-142">Aangepaste pagina's voor gebruikersaanmeldingen instellen</span><span class="sxs-lookup"><span data-stu-id="e365e-142">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="e365e-143">Ondersteuning voor een CDN (contentleveringsnetwerk) toevoegen</span><span class="sxs-lookup"><span data-stu-id="e365e-143">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="e365e-144">Detectie van winkels op basis van de locatie inschakelen</span><span class="sxs-lookup"><span data-stu-id="e365e-144">Enable location-based store detection</span></span>](enable-store-detection.md)
