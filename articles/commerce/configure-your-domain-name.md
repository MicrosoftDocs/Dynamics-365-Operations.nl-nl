---
title: Uw domeinnaam configureren
description: In dit onderwerp wordt uitgelegd hoe u een domeinnaam configureert voor Microsoft Dynamics 365 e-commerce-site.
author: psimolin
ms.date: 07/02/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 3d41168da44100a09c58b8c05367ab45bbd62a30
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/31/2021
ms.locfileid: "5796046"
---
# <a name="configure-your-domain-name"></a><span data-ttu-id="95d32-103">Uw domeinnaam configureren</span><span class="sxs-lookup"><span data-stu-id="95d32-103">Configure your domain name</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="95d32-104">In dit onderwerp wordt uitgelegd hoe u een domeinnaam configureert voor Microsoft Dynamics 365 e-commerce-site.</span><span class="sxs-lookup"><span data-stu-id="95d32-104">This topic explains how to configure a domain name for a Microsoft Dynamics 365 e-commerce site.</span></span> 

## <a name="add-domains-during-e-commerce-initialization"></a><span data-ttu-id="95d32-105">Domeinen toevoegen tijdens e-commerce-initialisatie</span><span class="sxs-lookup"><span data-stu-id="95d32-105">Add domains during e-commerce initialization</span></span>

<span data-ttu-id="95d32-106">Als u domeinen wilt koppelen aan uw Dynamics 365 Commerce e-commerce-omgeving, initialiseert u e-Commerce zoals beschreven in [Een nieuwe e-commerce-tenant implementeren](deploy-ecommerce-site.md).</span><span class="sxs-lookup"><span data-stu-id="95d32-106">To associate domains with your Dynamics 365 Commerce e-commerce environment, initialize e-commerce as described in [Deploy a new e-commerce tenant](deploy-ecommerce-site.md).</span></span> <span data-ttu-id="95d32-107">Tijdens de initialisatie wordt u gevraagd informatie op te geven die wordt gebruikt om uw e-commerce-omgeving in te richten.</span><span class="sxs-lookup"><span data-stu-id="95d32-107">During initialization, you're asked to provide information that will be used to provision your e-commerce environment.</span></span> <span data-ttu-id="95d32-108">Voeg in het veld **Ondersteunde hostnamen** alle domeinen toe die u met deze omgeving wilt gebruiken.</span><span class="sxs-lookup"><span data-stu-id="95d32-108">In the **Supported host names** field, add all the domains that you plan to use with this environment.</span></span> <span data-ttu-id="95d32-109">Meerdere domeinen moeten worden gescheiden door een puntkomma.</span><span class="sxs-lookup"><span data-stu-id="95d32-109">Multiple domains should be separated with semi-colon.</span></span> <span data-ttu-id="95d32-110">Op deze manier worden de domeinen geconfigureerd in alle vereiste e-commerce-onderdelen en kunnen ze worden gebruikt wanneer u verkeer van uw CDN (Content Delivery Network) of webserver overbrengt naar de e-commerce front-ends.</span><span class="sxs-lookup"><span data-stu-id="95d32-110">In this way, the domains are configured in all the required Commerce components, and they are ready to be used when you switch traffic from your content delivery network (CDN) or web server and point it to the e-commerce front ends.</span></span>

## <a name="add-domains-after-e-commerce-initialization"></a><span data-ttu-id="95d32-111">Domeinen toevoegen na e-commerce-initialisatie</span><span class="sxs-lookup"><span data-stu-id="95d32-111">Add domains after e-commerce initialization</span></span>

<span data-ttu-id="95d32-112">Als u na de e-commerce-initialisatie nieuwe domeinen wilt koppelen aan uw e-commerce-omgeving, moet u een serviceaanvraag indienen.</span><span class="sxs-lookup"><span data-stu-id="95d32-112">To associate new domains with your e-commerce environment after e-commerce initialization, you must submit a service request.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="95d32-113">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="95d32-113">Additional resources</span></span>

[<span data-ttu-id="95d32-114">Een nieuwe e-commerce-tenant implementeren</span><span class="sxs-lookup"><span data-stu-id="95d32-114">Deploy a new e-commerce tenant</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="95d32-115">Een e-commerce-site maken</span><span class="sxs-lookup"><span data-stu-id="95d32-115">Create an e-commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="95d32-116">Een Dynamics 365 Commerce-site koppelen aan een online kanaal</span><span class="sxs-lookup"><span data-stu-id="95d32-116">Associate a Dynamics 365 Commerce site with an online channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="95d32-117">robots.txt-bestanden beheren</span><span class="sxs-lookup"><span data-stu-id="95d32-117">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="95d32-118">URL-omleidingen in bulk uploaden</span><span class="sxs-lookup"><span data-stu-id="95d32-118">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

[<span data-ttu-id="95d32-119">Een B2C-tenant instellen in Commerce</span><span class="sxs-lookup"><span data-stu-id="95d32-119">Set up a B2C tenant in Commerce</span></span>](set-up-B2C-tenant.md)

[<span data-ttu-id="95d32-120">Aangepaste pagina's voor gebruikersaanmeldingen instellen</span><span class="sxs-lookup"><span data-stu-id="95d32-120">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="95d32-121">Meerdere B2C-tenants configureren in een Commerce-omgeving</span><span class="sxs-lookup"><span data-stu-id="95d32-121">Configure multiple B2C tenants in a Commerce environment</span></span>](configure-multi-B2C-tenants.md)

[<span data-ttu-id="95d32-122">Ondersteuning voor een CDN (contentleveringsnetwerk) toevoegen</span><span class="sxs-lookup"><span data-stu-id="95d32-122">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="95d32-123">Detectie van winkels op basis van de locatie inschakelen</span><span class="sxs-lookup"><span data-stu-id="95d32-123">Enable location-based store detection</span></span>](enable-store-detection.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]