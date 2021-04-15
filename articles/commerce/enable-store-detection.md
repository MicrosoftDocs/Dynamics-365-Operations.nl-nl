---
title: Detectie van winkels op basis van de locatie inschakelen
description: In dit onderwerp wordt beschreven hoe u de detectie van winkels op locatiebasis voor uw Dynamics 365 Commerce-site inschakelt.
author: brianshook
ms.date: 07/02/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 71e523cab20281d5db7efff40b5ef4f7293a4765
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/31/2021
ms.locfileid: "5799126"
---
# <a name="enable-location-based-store-detection"></a><span data-ttu-id="52d4d-103">Detectie van winkels op basis van de locatie inschakelen</span><span class="sxs-lookup"><span data-stu-id="52d4d-103">Enable location-based store detection</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="52d4d-104">In dit onderwerp wordt beschreven hoe u de detectie van winkels op locatiebasis voor uw Dynamics 365 Commerce-site inschakelt.</span><span class="sxs-lookup"><span data-stu-id="52d4d-104">This topic describes how to turn on location-based store detection for your Dynamics 365 Commerce site.</span></span>

<span data-ttu-id="52d4d-105">Met op locatie gebaseerde winkeldetectie in Commerce kunt u aan klanten relevante inhoud voor de site leveren op basis van hun locatie.</span><span class="sxs-lookup"><span data-stu-id="52d4d-105">Location-based store detection in Commerce lets you provide relevant site content to customers, based on their location.</span></span> <span data-ttu-id="52d4d-106">Wanneer op locatie gebaseerde winkeldetectie is ingeschakeld, gebruikt de Commerce-weergaveservice de land-/regiogegevens van het IP-adres van de webbrowser om de klant te leiden naar de beste configuratie voor geografische locaties.</span><span class="sxs-lookup"><span data-stu-id="52d4d-106">When location-based store detection is turned on, the Commerce rendering service uses the country/region information from the IP address of the customer's web browser to direct the customer to the best geographical site configuration that is available.</span></span>

## <a name="privacy-notice"></a><span data-ttu-id="52d4d-107">Privacyverklaring</span><span class="sxs-lookup"><span data-stu-id="52d4d-107">Privacy notice</span></span>

<span data-ttu-id="52d4d-108">Als u de op locatie gebaseerde winkeldetectie inschakelt, worden de gegevens van de klantbrowser naar een Microsoft-locatieservice verzonden.</span><span class="sxs-lookup"><span data-stu-id="52d4d-108">If you turn on the location-based store detection feature, information from the customer's browser is sent to a Microsoft location service.</span></span> <span data-ttu-id="52d4d-109">Deze informatie wordt vervolgens gebruikt om aan de klant inhoud te verstrekken die relevant is voor zijn of haar locatie.</span><span class="sxs-lookup"><span data-stu-id="52d4d-109">This information is then used to provide the customer content that is relevant to his or her location.</span></span> <span data-ttu-id="52d4d-110">Zowel informatie die wordt verzonden vanuit de browser van de klant als de op locatie gebaseerde informatie die naar de klant wordt geretourneerd, vallen onder het beleid voor privacy en cookies.</span><span class="sxs-lookup"><span data-stu-id="52d4d-110">Both the information that is sent from the customer's browser and the location-based information that is returned to the customer are subject to privacy and cookie compliance policies.</span></span>

## <a name="turn-on-location-based-store-detection"></a><span data-ttu-id="52d4d-111">Detectie van winkels op basis van de locatie inschakelen</span><span class="sxs-lookup"><span data-stu-id="52d4d-111">Turn on location-based store detection</span></span>

<span data-ttu-id="52d4d-112">Voer de volgende stappen uit als u winkeldetectie op basis van locatie wilt inschakelen in Commerce.</span><span class="sxs-lookup"><span data-stu-id="52d4d-112">To turn on location-based store detection in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="52d4d-113">Ga in de ontwerpfunctie naar uw site.</span><span class="sxs-lookup"><span data-stu-id="52d4d-113">In the authoring tool, go to your site.</span></span>
1. <span data-ttu-id="52d4d-114">Selecteer **Sitebeheer** in het navigatievenster aan de linkerkant.</span><span class="sxs-lookup"><span data-stu-id="52d4d-114">In the navigation pane on the left, select **Site Management**.</span></span>
1. <span data-ttu-id="52d4d-115">Selecteer **Site-instellingen**.</span><span class="sxs-lookup"><span data-stu-id="52d4d-115">Select **Site Settings**.</span></span>
1. <span data-ttu-id="52d4d-116">Stel de optie **Detectie van winkels op basis van de locatie inschakelen** in op **Aan**.</span><span class="sxs-lookup"><span data-stu-id="52d4d-116">Set the **Enable location based store detection** option to **On**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="52d4d-117">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="52d4d-117">Additional resources</span></span>

[<span data-ttu-id="52d4d-118">Uw domeinnaam configureren</span><span class="sxs-lookup"><span data-stu-id="52d4d-118">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="52d4d-119">Een nieuwe e-commerce-tenant implementeren</span><span class="sxs-lookup"><span data-stu-id="52d4d-119">Deploy a new e-commerce tenant</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="52d4d-120">Een e-commerce-site maken</span><span class="sxs-lookup"><span data-stu-id="52d4d-120">Create an e-commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="52d4d-121">Een Dynamics 365 Commerce-site koppelen aan een online kanaal</span><span class="sxs-lookup"><span data-stu-id="52d4d-121">Associate a Dynamics 365 Commerce site with an online channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="52d4d-122">robots.txt-bestanden beheren</span><span class="sxs-lookup"><span data-stu-id="52d4d-122">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="52d4d-123">URL-omleidingen in bulk uploaden</span><span class="sxs-lookup"><span data-stu-id="52d4d-123">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

[<span data-ttu-id="52d4d-124">Een B2C-tenant instellen in Commerce</span><span class="sxs-lookup"><span data-stu-id="52d4d-124">Set up a B2C tenant in Commerce</span></span>](set-up-B2C-tenant.md)

[<span data-ttu-id="52d4d-125">Aangepaste pagina's voor gebruikersaanmeldingen instellen</span><span class="sxs-lookup"><span data-stu-id="52d4d-125">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="52d4d-126">Meerdere B2C-tenants configureren in een Commerce-omgeving</span><span class="sxs-lookup"><span data-stu-id="52d4d-126">Configure multiple B2C tenants in a Commerce environment</span></span>](configure-multi-B2C-tenants.md)

[<span data-ttu-id="52d4d-127">Ondersteuning voor een CDN (contentleveringsnetwerk) toevoegen</span><span class="sxs-lookup"><span data-stu-id="52d4d-127">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
