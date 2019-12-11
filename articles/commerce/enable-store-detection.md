---
title: Detectie van winkels op basis van de locatie inschakelen
description: In dit onderwerp wordt beschreven hoe u de detectie van winkels op locatiebasis voor uw Dynamics 365 Commerce-site inschakelt.
author: brianshook
manager: annbe
ms.date: 10/01/2019
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
ms.openlocfilehash: a542d6987280451910b4ff3bcfb3a109a0e028c6
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/01/2019
ms.locfileid: "2697607"
---
# <a name="enable-location-based-store-detection"></a><span data-ttu-id="bc91d-103">Detectie van winkels op basis van de locatie inschakelen</span><span class="sxs-lookup"><span data-stu-id="bc91d-103">Enable location-based store detection</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="bc91d-104">In dit onderwerp wordt beschreven hoe u de detectie van winkels op locatiebasis voor uw Dynamics 365 Commerce-site inschakelt.</span><span class="sxs-lookup"><span data-stu-id="bc91d-104">This topic describes how to turn on location-based store detection for your Dynamics 365 Commerce site.</span></span>

## <a name="overview"></a><span data-ttu-id="bc91d-105">Overzicht</span><span class="sxs-lookup"><span data-stu-id="bc91d-105">Overview</span></span>

<span data-ttu-id="bc91d-106">Met op locatie gebaseerde winkeldetectie in Commerce kunt u aan klanten relevante inhoud voor de site leveren op basis van hun locatie.</span><span class="sxs-lookup"><span data-stu-id="bc91d-106">Location-based store detection in Commerce lets you provide relevant site content to customers, based on their location.</span></span> <span data-ttu-id="bc91d-107">Wanneer op locatie gebaseerde winkeldetectie is ingeschakeld, gebruikt de Commerce-weergaveservice de land-/regiogegevens van het IP-adres van de webbrowser om de klant te leiden naar de beste configuratie voor geografische locaties.</span><span class="sxs-lookup"><span data-stu-id="bc91d-107">When location-based store detection is turned on, the Commerce rendering service uses the country/region information from the IP address of the customer's web browser to direct the customer to the best geographical site configuration that is available.</span></span>

## <a name="privacy-notice"></a><span data-ttu-id="bc91d-108">Privacyverklaring</span><span class="sxs-lookup"><span data-stu-id="bc91d-108">Privacy notice</span></span>

<span data-ttu-id="bc91d-109">Als u de op locatie gebaseerde winkeldetectie inschakelt, worden de gegevens van de klantbrowser naar een Microsoft-locatieservice verzonden.</span><span class="sxs-lookup"><span data-stu-id="bc91d-109">If you turn on the location-based store detection feature, information from the customer's browser is sent to a Microsoft location service.</span></span> <span data-ttu-id="bc91d-110">Deze informatie wordt vervolgens gebruikt om aan de klant inhoud te verstrekken die relevant is voor zijn of haar locatie.</span><span class="sxs-lookup"><span data-stu-id="bc91d-110">This information is then used to provide the customer content that is relevant to his or her location.</span></span> <span data-ttu-id="bc91d-111">Zowel informatie die wordt verzonden vanuit de browser van de klant als de op locatie gebaseerde informatie die naar de klant wordt geretourneerd, vallen onder het beleid voor privacy en cookies.</span><span class="sxs-lookup"><span data-stu-id="bc91d-111">Both the information that is sent from the customer's browser and the location-based information that is returned to the customer are subject to privacy and cookie compliance policies.</span></span>

## <a name="turn-on-location-based-store-detection"></a><span data-ttu-id="bc91d-112">Detectie van winkels op basis van de locatie inschakelen</span><span class="sxs-lookup"><span data-stu-id="bc91d-112">Turn on location-based store detection</span></span>

<span data-ttu-id="bc91d-113">Voer de volgende stappen uit als u winkeldetectie op basis van locatie wilt inschakelen in Commerce.</span><span class="sxs-lookup"><span data-stu-id="bc91d-113">To turn on location-based store detection in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="bc91d-114">Ga in de ontwerpfunctie naar uw site.</span><span class="sxs-lookup"><span data-stu-id="bc91d-114">In the authoring tool, go to your site.</span></span>
1. <span data-ttu-id="bc91d-115">Selecteer **Sitebeheer** in het navigatievenster aan de linkerkant.</span><span class="sxs-lookup"><span data-stu-id="bc91d-115">In the navigation pane on the left, select **Site Management**.</span></span>
1. <span data-ttu-id="bc91d-116">Selecteer **Site-instellingen**.</span><span class="sxs-lookup"><span data-stu-id="bc91d-116">Select **Site Settings**.</span></span>
1. <span data-ttu-id="bc91d-117">Stel de optie **Detectie van winkels op basis van de locatie inschakelen** in op **Aan**.</span><span class="sxs-lookup"><span data-stu-id="bc91d-117">Set the **Enable location based store detection** option to **On**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="bc91d-118">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="bc91d-118">Additional resources</span></span>

[<span data-ttu-id="bc91d-119">Online winkeloverzicht</span><span class="sxs-lookup"><span data-stu-id="bc91d-119">Online store overview</span></span>](online-store-overview.md)

[<span data-ttu-id="bc91d-120">Een e-commerce-site maken</span><span class="sxs-lookup"><span data-stu-id="bc91d-120">Create an e-Commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="bc91d-121">Een nieuwe e-commerce-site implementeren</span><span class="sxs-lookup"><span data-stu-id="bc91d-121">Deploy a new e-Commerce site</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="bc91d-122">Een online-site koppelen aan een kanaal</span><span class="sxs-lookup"><span data-stu-id="bc91d-122">Associate an online site with a channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="bc91d-123">Uw domeinnaam configureren</span><span class="sxs-lookup"><span data-stu-id="bc91d-123">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="bc91d-124">Ondersteuning voor een CDN (contentleveringsnetwerk) toevoegen</span><span class="sxs-lookup"><span data-stu-id="bc91d-124">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="bc91d-125">Aangepaste pagina's voor gebruikersaanmeldingen instellen</span><span class="sxs-lookup"><span data-stu-id="bc91d-125">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)
