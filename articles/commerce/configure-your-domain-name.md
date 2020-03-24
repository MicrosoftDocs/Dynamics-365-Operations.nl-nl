---
title: Uw domeinnaam configureren
description: In dit onderwerp wordt uitgelegd hoe u een domeinnaam configureert voor Microsoft Dynamics 365 e-commerce-site.
author: psimolin
manager: AnnBe
ms.date: 03/02/2020
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
ms.search.industry: Retail
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 2ad9ca3aee21301ef6d830d7b29982a45cd53f60
ms.sourcegitcommit: 567132f4e4f7a1d76dccf762068209a42c788b52
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/03/2020
ms.locfileid: "3096815"
---
# <a name="configure-your-domain-name"></a><span data-ttu-id="082dc-103">Uw domeinnaam configureren</span><span class="sxs-lookup"><span data-stu-id="082dc-103">Configure your domain name</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="082dc-104">In dit onderwerp wordt uitgelegd hoe u een domeinnaam configureert voor Microsoft Dynamics 365 e-commerce-site.</span><span class="sxs-lookup"><span data-stu-id="082dc-104">This topic explains how to configure a domain name for a Microsoft Dynamics 365 e-commerce site.</span></span> 

## <a name="add-domains-during-e-commerce-initialization"></a><span data-ttu-id="082dc-105">Domeinen toevoegen tijdens e-commerce-initialisatie</span><span class="sxs-lookup"><span data-stu-id="082dc-105">Add domains during e-Commerce initialization</span></span>

<span data-ttu-id="082dc-106">Als u domeinen wilt koppelen aan uw e-commerce-omgeving, initialiseert u e-Commerce zoals beschreven in [Een nieuwe e-commerce-site](deploy-ecommerce-site.md).</span><span class="sxs-lookup"><span data-stu-id="082dc-106">To associate domains with your e-commerce environment, initialize e-Commerce as described in [Deploy a new e-Commerce site](deploy-ecommerce-site.md).</span></span> <span data-ttu-id="082dc-107">Tijdens de initialisatie wordt u gevraagd informatie op te geven die wordt gebruikt om uw e-commerce-omgeving in te richten.</span><span class="sxs-lookup"><span data-stu-id="082dc-107">During initialization, you're asked to provide information that will be used to provision your e-Commerce environment.</span></span> <span data-ttu-id="082dc-108">Voeg in het veld **Ondersteunde hostnamen** alle domeinen toe die u met deze omgeving wilt gebruiken.</span><span class="sxs-lookup"><span data-stu-id="082dc-108">In the **Supported host names** field, add all the domains that you plan to use with this environment.</span></span> <span data-ttu-id="082dc-109">Meerdere domeinen moeten worden gescheiden door een puntkomma.</span><span class="sxs-lookup"><span data-stu-id="082dc-109">Multiple domains should be separated with semi-colon.</span></span> <span data-ttu-id="082dc-110">Op deze manier worden de domeinen geconfigureerd in alle vereiste e-commerce-onderdelen en kunnen ze worden gebruikt wanneer u verkeer van uw CDN (Content Delivery Network) of webserver overbrengt naar de e-commerce front-ends.</span><span class="sxs-lookup"><span data-stu-id="082dc-110">In this way, the domains are configured in all the required e-Commerce components, and they are ready to be used when you switch traffic from your content delivery network (CDN) or web server and point it to the e-Commerce front ends.</span></span>

## <a name="add-domains-after-e-commerce-initialization"></a><span data-ttu-id="082dc-111">Domeinen toevoegen na e-commerce-initialisatie</span><span class="sxs-lookup"><span data-stu-id="082dc-111">Add domains after e-Commerce initialization</span></span>

<span data-ttu-id="082dc-112">Als u na de e-commerce-initialisatie nieuwe domeinen wilt koppelen aan uw e-commerce-omgeving, moet u een serviceaanvraag indienen.</span><span class="sxs-lookup"><span data-stu-id="082dc-112">To associate new domains with your e-Commerce environment after e-Commerce initialization, you must submit a service request.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="082dc-113">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="082dc-113">Additional resources</span></span>

[<span data-ttu-id="082dc-114">Een nieuwe e-commerce-site implementeren</span><span class="sxs-lookup"><span data-stu-id="082dc-114">Deploy a new e-Commerce site</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="082dc-115">Een online winkelafzetkanaal instellen</span><span class="sxs-lookup"><span data-stu-id="082dc-115">Set up an online store channel</span></span>](online-stores.md)

[<span data-ttu-id="082dc-116">Een e-commerce-site maken</span><span class="sxs-lookup"><span data-stu-id="082dc-116">Create an e-Commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="082dc-117">Een online-site koppelen aan een kanaal</span><span class="sxs-lookup"><span data-stu-id="082dc-117">Associate an online site with a channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="082dc-118">Robots.txt-bestanden beheren</span><span class="sxs-lookup"><span data-stu-id="082dc-118">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="082dc-119">URL-omleidingen in bulk uploaden</span><span class="sxs-lookup"><span data-stu-id="082dc-119">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

[<span data-ttu-id="082dc-120">Een B2C-tenant instellen in Commerce</span><span class="sxs-lookup"><span data-stu-id="082dc-120">Set up a B2C tenant in Commerce</span></span>](set-up-B2C-tenant.md)

[<span data-ttu-id="082dc-121">Aangepaste pagina's voor gebruikersaanmeldingen instellen</span><span class="sxs-lookup"><span data-stu-id="082dc-121">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="082dc-122">Meerdere B2C-tenants configureren in een Commerce-omgeving</span><span class="sxs-lookup"><span data-stu-id="082dc-122">Configure multiple B2C tenants in a Commerce environment</span></span>](configure-multi-B2C-tenants.md)

[<span data-ttu-id="082dc-123">Ondersteuning voor een CDN (contentleveringsnetwerk) toevoegen</span><span class="sxs-lookup"><span data-stu-id="082dc-123">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="082dc-124">Detectie van winkels op basis van de locatie inschakelen</span><span class="sxs-lookup"><span data-stu-id="082dc-124">Enable location-based store detection</span></span>](enable-store-detection.md)
