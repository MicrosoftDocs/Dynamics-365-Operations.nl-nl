---
title: Detectie van winkels op basis van de locatie inschakelen
description: In dit onderwerp wordt beschreven hoe u de detectie van winkels op locatiebasis voor uw Dynamics 365 Commerce-site inschakelt.
author: brianshook
manager: annbe
ms.date: 07/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: f87d29a8cffb70e4dea211cea7538e5e4c85295c
ms.sourcegitcommit: 4bf5ae2f2f144a28e431ed574c7e8438dc5935de
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/13/2020
ms.locfileid: "4517301"
---
# <a name="enable-location-based-store-detection"></a><span data-ttu-id="38212-103">Detectie van winkels op basis van de locatie inschakelen</span><span class="sxs-lookup"><span data-stu-id="38212-103">Enable location-based store detection</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="38212-104">In dit onderwerp wordt beschreven hoe u de detectie van winkels op locatiebasis voor uw Dynamics 365 Commerce-site inschakelt.</span><span class="sxs-lookup"><span data-stu-id="38212-104">This topic describes how to turn on location-based store detection for your Dynamics 365 Commerce site.</span></span>

## <a name="overview"></a><span data-ttu-id="38212-105">Overzicht</span><span class="sxs-lookup"><span data-stu-id="38212-105">Overview</span></span>

<span data-ttu-id="38212-106">Met op locatie gebaseerde winkeldetectie in Commerce kunt u aan klanten relevante inhoud voor de site leveren op basis van hun locatie.</span><span class="sxs-lookup"><span data-stu-id="38212-106">Location-based store detection in Commerce lets you provide relevant site content to customers, based on their location.</span></span> <span data-ttu-id="38212-107">Wanneer op locatie gebaseerde winkeldetectie is ingeschakeld, gebruikt de Commerce-weergaveservice de land-/regiogegevens van het IP-adres van de webbrowser om de klant te leiden naar de beste configuratie voor geografische locaties.</span><span class="sxs-lookup"><span data-stu-id="38212-107">When location-based store detection is turned on, the Commerce rendering service uses the country/region information from the IP address of the customer's web browser to direct the customer to the best geographical site configuration that is available.</span></span>

## <a name="privacy-notice"></a><span data-ttu-id="38212-108">Privacyverklaring</span><span class="sxs-lookup"><span data-stu-id="38212-108">Privacy notice</span></span>

<span data-ttu-id="38212-109">Als u de op locatie gebaseerde winkeldetectie inschakelt, worden de gegevens van de klantbrowser naar een Microsoft-locatieservice verzonden.</span><span class="sxs-lookup"><span data-stu-id="38212-109">If you turn on the location-based store detection feature, information from the customer's browser is sent to a Microsoft location service.</span></span> <span data-ttu-id="38212-110">Deze informatie wordt vervolgens gebruikt om aan de klant inhoud te verstrekken die relevant is voor zijn of haar locatie.</span><span class="sxs-lookup"><span data-stu-id="38212-110">This information is then used to provide the customer content that is relevant to his or her location.</span></span> <span data-ttu-id="38212-111">Zowel informatie die wordt verzonden vanuit de browser van de klant als de op locatie gebaseerde informatie die naar de klant wordt geretourneerd, vallen onder het beleid voor privacy en cookies.</span><span class="sxs-lookup"><span data-stu-id="38212-111">Both the information that is sent from the customer's browser and the location-based information that is returned to the customer are subject to privacy and cookie compliance policies.</span></span>

## <a name="turn-on-location-based-store-detection"></a><span data-ttu-id="38212-112">Detectie van winkels op basis van de locatie inschakelen</span><span class="sxs-lookup"><span data-stu-id="38212-112">Turn on location-based store detection</span></span>

<span data-ttu-id="38212-113">Voer de volgende stappen uit als u winkeldetectie op basis van locatie wilt inschakelen in Commerce.</span><span class="sxs-lookup"><span data-stu-id="38212-113">To turn on location-based store detection in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="38212-114">Ga in de ontwerpfunctie naar uw site.</span><span class="sxs-lookup"><span data-stu-id="38212-114">In the authoring tool, go to your site.</span></span>
1. <span data-ttu-id="38212-115">Selecteer **Sitebeheer** in het navigatievenster aan de linkerkant.</span><span class="sxs-lookup"><span data-stu-id="38212-115">In the navigation pane on the left, select **Site Management**.</span></span>
1. <span data-ttu-id="38212-116">Selecteer **Site-instellingen**.</span><span class="sxs-lookup"><span data-stu-id="38212-116">Select **Site Settings**.</span></span>
1. <span data-ttu-id="38212-117">Stel de optie **Detectie van winkels op basis van de locatie inschakelen** in op **Aan**.</span><span class="sxs-lookup"><span data-stu-id="38212-117">Set the **Enable location based store detection** option to **On**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="38212-118">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="38212-118">Additional resources</span></span>

[<span data-ttu-id="38212-119">Uw domeinnaam configureren</span><span class="sxs-lookup"><span data-stu-id="38212-119">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="38212-120">Een nieuwe e-commerce-tenant implementeren</span><span class="sxs-lookup"><span data-stu-id="38212-120">Deploy a new e-commerce tenant</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="38212-121">Een e-commerce-site maken</span><span class="sxs-lookup"><span data-stu-id="38212-121">Create an e-commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="38212-122">Een Dynamics 365 Commerce-site koppelen aan een online kanaal</span><span class="sxs-lookup"><span data-stu-id="38212-122">Associate a Dynamics 365 Commerce site with an online channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="38212-123">robots.txt-bestanden beheren</span><span class="sxs-lookup"><span data-stu-id="38212-123">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="38212-124">URL-omleidingen in bulk uploaden</span><span class="sxs-lookup"><span data-stu-id="38212-124">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

[<span data-ttu-id="38212-125">Een B2C-tenant instellen in Commerce</span><span class="sxs-lookup"><span data-stu-id="38212-125">Set up a B2C tenant in Commerce</span></span>](set-up-B2C-tenant.md)

[<span data-ttu-id="38212-126">Aangepaste pagina's voor gebruikersaanmeldingen instellen</span><span class="sxs-lookup"><span data-stu-id="38212-126">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="38212-127">Meerdere B2C-tenants configureren in een Commerce-omgeving</span><span class="sxs-lookup"><span data-stu-id="38212-127">Configure multiple B2C tenants in a Commerce environment</span></span>](configure-multi-B2C-tenants.md)

[<span data-ttu-id="38212-128">Ondersteuning voor een CDN (contentleveringsnetwerk) toevoegen</span><span class="sxs-lookup"><span data-stu-id="38212-128">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)
