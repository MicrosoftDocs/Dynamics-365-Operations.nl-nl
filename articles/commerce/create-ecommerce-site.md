---
title: Een e-commerce-site maken
description: In dit onderwerp worden de stappen en informatie beschreven die nodig zijn om een nieuwe e-Commerce-site in Dynamics 365 Commerce site builder te maken.
author: bicyclingfool
manager: AnnBe
ms.date: 07/02/2020
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
ms.openlocfilehash: ea3517a4f2b84db8a87a97d2f644bb4436f8693f
ms.sourcegitcommit: adf196c51e2b6f532d99c177b4c6778cea8a2efc
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 07/02/2020
ms.locfileid: "3533431"
---
# <a name="create-an-e-commerce-site"></a><span data-ttu-id="6c0d4-103">Een e-commerce-site maken</span><span class="sxs-lookup"><span data-stu-id="6c0d4-103">Create an e-Commerce site</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="6c0d4-104">In dit onderwerp worden de stappen en informatie beschreven die nodig zijn om een nieuwe e-Commerce-site in Dynamics 365 Commerce site builder te maken.</span><span class="sxs-lookup"><span data-stu-id="6c0d4-104">This topic describes the steps and information required to create a new e-Commerce site in Dynamics 365 Commerce site builder.</span></span>

<span data-ttu-id="6c0d4-105">Wanneer u een licentie neemt voor de functies voor e-Commerce, wordt site builder ingericht met een startsite die u kunt gebruiken als basis voor uw eigen site.</span><span class="sxs-lookup"><span data-stu-id="6c0d4-105">When you license the e-Commerce capabilities, site builder will be provisioned with a starter site that you can use as a basis for your own site.</span></span> <span data-ttu-id="6c0d4-106">Als u echter zelf wilt beginnen of als u een tweede site wilt maken, moet u een nieuwe site maken in de site-ontwerpomgeving.</span><span class="sxs-lookup"><span data-stu-id="6c0d4-106">However, if you want to start from scratch or if you want to establish a second site, you will need to establish a new site in the site authoring environment.</span></span> 

## <a name="set-up-your-site"></a><span data-ttu-id="6c0d4-107">Uw site instellen</span><span class="sxs-lookup"><span data-stu-id="6c0d4-107">Set up your site</span></span>

<span data-ttu-id="6c0d4-108">Ga als volgt te werk als u uw site wilt instellen.</span><span class="sxs-lookup"><span data-stu-id="6c0d4-108">To set up your site, do the following.</span></span>

1. <span data-ttu-id="6c0d4-109">Open de site builder-omgeving.</span><span class="sxs-lookup"><span data-stu-id="6c0d4-109">Open the site builder environment.</span></span> <span data-ttu-id="6c0d4-110">U vindt een koppeling naar de site builder in Microsoft Lifecycle Services (LCS) op de pagina omgevingsfuncties voor Commerce.</span><span class="sxs-lookup"><span data-stu-id="6c0d4-110">You can find a link to site builder in Microsoft Lifecycle Services (LCS) in the environment features page for Commerce.</span></span>
1. <span data-ttu-id="6c0d4-111">Selecteer **Nieuwe site** op de startpagina voor de ontwerpomgeving voor sites.</span><span class="sxs-lookup"><span data-stu-id="6c0d4-111">On the home page for the site authoring environment, select **New site**.</span></span>
1. <span data-ttu-id="6c0d4-112">Geef in het dialoogvenster **Nieuwe site** de volgende informatie op.</span><span class="sxs-lookup"><span data-stu-id="6c0d4-112">In the **New site** dialog box, provide the following information.</span></span>

| <span data-ttu-id="6c0d4-113">Veld</span><span class="sxs-lookup"><span data-stu-id="6c0d4-113">Field</span></span>                               | <span data-ttu-id="6c0d4-114">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="6c0d4-114">Description</span></span> |
|-------------------------------------|-------------|
| <span data-ttu-id="6c0d4-115">Sitenaam</span><span class="sxs-lookup"><span data-stu-id="6c0d4-115">Site name</span></span>                           | <span data-ttu-id="6c0d4-116">Voer de weergavenaam in die moet worden gebruikt voor uw site in de ontwerpomgeving.</span><span class="sxs-lookup"><span data-stu-id="6c0d4-116">Enter the display name that should be used for your site in the site authoring environment.</span></span> <span data-ttu-id="6c0d4-117">Deze naam is alleen zichtbaar in de ontwerpomgeving en wordt niet weergegeven voor klanten.</span><span class="sxs-lookup"><span data-stu-id="6c0d4-117">This name is visible only in the authoring environment and will not be shown to customers.</span></span> |
| <span data-ttu-id="6c0d4-118">Beveiligingsgroep van de sitebeheerder</span><span class="sxs-lookup"><span data-stu-id="6c0d4-118">Site administrator's security group</span></span> | <span data-ttu-id="6c0d4-119">Geef de beveiligingsgroep voor Microsoft Azure Active Directory (Azure AD) op waarmee gebruikers met de rol van sitebeheerder op deze site worden beheerd.</span><span class="sxs-lookup"><span data-stu-id="6c0d4-119">Specify the Microsoft Azure Active Directory (Azure AD) security group that manages users who have the site administrator role in this site.</span></span> |
| <span data-ttu-id="6c0d4-120">Standaardkanaal (nummer operationele eenheid)</span><span class="sxs-lookup"><span data-stu-id="6c0d4-120">Default channel (operating unit number)</span></span> | <span data-ttu-id="6c0d4-121">Selecteer de online winkel waarvoor deze site als webwinkel zal dienen.</span><span class="sxs-lookup"><span data-stu-id="6c0d4-121">Select the online store that this site will serve as the web storefront for.</span></span> <span data-ttu-id="6c0d4-122">Als u wilt dat uw e-commerce-site meerdere online winkels ondersteunt, moet u de winkels aan uw site koppelen in de **Site-instellingen** nadat de site is ingesteld.</span><span class="sxs-lookup"><span data-stu-id="6c0d4-122">If you want your e-Commerce site to support multiple online stores, you must associate the stores with your site in **Site settings** after the site is set up.</span></span> |
| <span data-ttu-id="6c0d4-123">Standaardtaal</span><span class="sxs-lookup"><span data-stu-id="6c0d4-123">Default language</span></span>                            | <span data-ttu-id="6c0d4-124">Geef de standaardtaal op voor deze online winkel en markt.</span><span class="sxs-lookup"><span data-stu-id="6c0d4-124">Specify the default language for this online store and market.</span></span> <span data-ttu-id="6c0d4-125">Een online winkel kan meerdere talen ondersteunen.</span><span class="sxs-lookup"><span data-stu-id="6c0d4-125">An online store can support multiple languages.</span></span> <span data-ttu-id="6c0d4-126">Als u meerdere talen wilt ondersteunen voor deze online winkel of een andere online winkel, kunt u dat configureren in **Site-instellingen** nadat de site is ingesteld.</span><span class="sxs-lookup"><span data-stu-id="6c0d4-126">If you want to support multiple languages for this online store or another online store, you can configure that support in **Site settings** after the site is set up.</span></span>  |
| <span data-ttu-id="6c0d4-127">Domein</span><span class="sxs-lookup"><span data-stu-id="6c0d4-127">Domain</span></span>                              | <span data-ttu-id="6c0d4-128">Selecteer een domein dat als domein zal dienen voor deze online winkel.</span><span class="sxs-lookup"><span data-stu-id="6c0d4-128">Select a domain name that will serve as the domain for this online store.</span></span> <span data-ttu-id="6c0d4-129">Als u geen domeinen in LCS hebt geconfigureerd, kunt u dit veld leeg laten.</span><span class="sxs-lookup"><span data-stu-id="6c0d4-129">If you haven't configured any domains in LCS, you can leave this field blank.</span></span> <span data-ttu-id="6c0d4-130">Nadat uw domein in LCS is geconfigureerd, moet u dit aan uw online winkel toevoegen in de **Site-instellingen**.</span><span class="sxs-lookup"><span data-stu-id="6c0d4-130">After your domain is configured in LCS, you must add it to your online store in **Site settings**.</span></span>  |
| <span data-ttu-id="6c0d4-131">Pad</span><span class="sxs-lookup"><span data-stu-id="6c0d4-131">Path</span></span>                              | <span data-ttu-id="6c0d4-132">Wanneer uw site meerdere talen ondersteunt voor een bepaalde domeinnaam, gebruikt u het padveld om een unieke site-URL te maken voor die domein- en taalcombinatie.</span><span class="sxs-lookup"><span data-stu-id="6c0d4-132">When your site supports more than one language for a given domain name, use the path field to create a unique site URL for that domain and language combination.</span></span> <span data-ttu-id="6c0d4-133">Als de taal die u hebt opgegeven in het veld **Standaardtaal** de enige taal is die u voor dit domein wilt gebruiken of de standaardtaal blijft nadat u uw site hebt gelokaliseerd in extra talen, wordt u aangeraden dit veld leeg te laten.</span><span class="sxs-lookup"><span data-stu-id="6c0d4-133">If the language you specified in the **Default language** field is the only language you will support for this domain, or will continue to be the default language after you have localized your site into additional languages, we recommend that you leave this field empty.</span></span> |


<span data-ttu-id="6c0d4-134">Nadat de site is gemaakt, kunt u controleren of deze is gekoppeld aan uw online winkel door het tabblad **Producten** te selecteren. Het assortiment met producten dat aan de online winkel is toegewezen, wordt weergeven.</span><span class="sxs-lookup"><span data-stu-id="6c0d4-134">After your site is created, you can verify that it is associated with your online store by selecting the **Products** tab. You should see the assortment of products that has been allocated to the online store.</span></span> <span data-ttu-id="6c0d4-135">U kunt ook het vervolgkeuzemenu in de linkerbovenhoek van de pagina gebruiken om toegang te krijgen tot de toegewezen producten per categorie.</span><span class="sxs-lookup"><span data-stu-id="6c0d4-135">You can also use the drop-down menu in the upper left of the page to access the allocated products by category.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="6c0d4-136">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="6c0d4-136">Additional resources</span></span>

[<span data-ttu-id="6c0d4-137">Uw domeinnaam configureren</span><span class="sxs-lookup"><span data-stu-id="6c0d4-137">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="6c0d4-138">Een nieuwe e-commerce-site implementeren</span><span class="sxs-lookup"><span data-stu-id="6c0d4-138">Deploy a new e-Commerce site</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="6c0d4-139">Een online-site koppelen aan een kanaal</span><span class="sxs-lookup"><span data-stu-id="6c0d4-139">Associate an online site with a channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="6c0d4-140">robots.txt-bestanden beheren</span><span class="sxs-lookup"><span data-stu-id="6c0d4-140">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="6c0d4-141">URL-omleidingen in bulk uploaden</span><span class="sxs-lookup"><span data-stu-id="6c0d4-141">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

[<span data-ttu-id="6c0d4-142">Een B2C-tenant instellen in Commerce</span><span class="sxs-lookup"><span data-stu-id="6c0d4-142">Set up a B2C tenant in Commerce</span></span>](set-up-B2C-tenant.md)

[<span data-ttu-id="6c0d4-143">Aangepaste pagina's voor gebruikersaanmeldingen instellen</span><span class="sxs-lookup"><span data-stu-id="6c0d4-143">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="6c0d4-144">Meerdere B2C-tenants configureren in een Commerce-omgeving</span><span class="sxs-lookup"><span data-stu-id="6c0d4-144">Configure multiple B2C tenants in a Commerce environment</span></span>](configure-multi-B2C-tenants.md)

[<span data-ttu-id="6c0d4-145">Ondersteuning voor een CDN (contentleveringsnetwerk) toevoegen</span><span class="sxs-lookup"><span data-stu-id="6c0d4-145">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="6c0d4-146">Detectie van winkels op basis van de locatie inschakelen</span><span class="sxs-lookup"><span data-stu-id="6c0d4-146">Enable location-based store detection</span></span>](enable-store-detection.md)
