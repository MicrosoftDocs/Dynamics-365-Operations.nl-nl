---
title: Een nieuwe e-commerce-tenant implementeren
description: In dit onderwerp wordt beschreven hoe u een nieuwe e-commerce-tenant implementeert met behulp van Microsoft Dynamics Lifecycle Services (LCS).
author: psimolin
manager: annbe
ms.date: 10/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 10dab1e62446ff7f60ad48fd0841bde5cfd29e12
ms.sourcegitcommit: ef3a1d7527311d00b69a1072ae5eb021ce68034c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/09/2020
ms.locfileid: "2945508"
---
# <a name="deploy-a-new-e-commerce-tenant"></a><span data-ttu-id="73417-103">Een nieuwe e-commerce-tenant implementeren</span><span class="sxs-lookup"><span data-stu-id="73417-103">Deploy a new e-Commerce tenant</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="73417-104">In dit onderwerp wordt beschreven hoe u een nieuwe e-commerce-site implementeert met behulp van Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="73417-104">This topic describes how to deploy a new e-Commerce site by using Microsoft Dynamics Lifecycle Services (LCS).</span></span>

## <a name="overview"></a><span data-ttu-id="73417-105">Overzicht</span><span class="sxs-lookup"><span data-stu-id="73417-105">Overview</span></span>
    
<span data-ttu-id="73417-106">Microsoft Dynamics Lifecycle Services (LCS) is een cloudwerkgebied dat door partners en klanten wordt gebruikt voor het beheer van hun projecten en omgevingen, het weergeven van de meest recente informatie over producten en functies van Microsoft Dynamics en het maken, volgen en zoeken van ondersteuningsaanvragen.</span><span class="sxs-lookup"><span data-stu-id="73417-106">Microsoft Dynamics Lifecycle Services (LCS) is a cloud-based collaborative workspace that partners and customers can use to manage their projects and environments, view the latest information about Microsoft Dynamics products and features, and create, track, and browse support incidents.</span></span> <span data-ttu-id="73417-107">Beheerfuncties voor e-commerce zijn in LCS geïntegreerd.</span><span class="sxs-lookup"><span data-stu-id="73417-107">E-Commerce management features are integrated into LCS.</span></span>

<span data-ttu-id="73417-108">Zie de [gebruikershandleiding van Lifecycle Services](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide) voor meer informatie over LCS.</span><span class="sxs-lookup"><span data-stu-id="73417-108">To learn more about LCS, see the [Lifecycle Services User Guide](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide).</span></span>
    
## <a name="get-started"></a><span data-ttu-id="73417-109">Aan de slag</span><span class="sxs-lookup"><span data-stu-id="73417-109">Get started</span></span>

<span data-ttu-id="73417-110">Voordat u e-commerce kunt initialiseren, moet u een project, een omgeving en een Retail Cloud Scale Unit (RCSU) initialiseren.</span><span class="sxs-lookup"><span data-stu-id="73417-110">Before you can initialize e-Commerce, you must initialize a project, an environment, and a Retail Cloud Scale Unit (RCSU).</span></span> <span data-ttu-id="73417-111">Als u de initialisatie wilt uitvoeren in LCS, moet u machtigingen hebben voor de rol projecteigenaar of omgevingsbeheerder.</span><span class="sxs-lookup"><span data-stu-id="73417-111">To do the initialization in LCS, you must have permissions for either the Project Owner or Environment manager role.</span></span> <span data-ttu-id="73417-112">De topologieën productie en sandbox-omgeving worden ondersteund.</span><span class="sxs-lookup"><span data-stu-id="73417-112">The production and sandbox environment topologies are supported.</span></span>

<span data-ttu-id="73417-113">Zie [Omgevingsplanning](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/imp-lifecycle/environment-planning) voor meer informatie over omgevingen.</span><span class="sxs-lookup"><span data-stu-id="73417-113">For more information about environments, see [Environment planning](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/imp-lifecycle/environment-planning).</span></span> <span data-ttu-id="73417-114">Zie [Retail Cloud Scale Unit initialiseren](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/deployment/initialize-retail-channels)voor meer informatie over RCSU.</span><span class="sxs-lookup"><span data-stu-id="73417-114">For more information about RCSU, see [Initialize Retail Cloud Scale Unit](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/deployment/initialize-retail-channels).</span></span>

## <a name="initialize-e-commerce"></a><span data-ttu-id="73417-115">e-Commerce initialiseren</span><span class="sxs-lookup"><span data-stu-id="73417-115">Initialize e-Commerce</span></span>

<span data-ttu-id="73417-116">Gebruik deze procedure om de e-commerce-functie in een bestaande omgeving te initialiseren.</span><span class="sxs-lookup"><span data-stu-id="73417-116">Use this procedure to initialize the e-Commerce feature in an existing environment.</span></span>

<span data-ttu-id="73417-117">Voordat u begint, moet u controleren of u de volgende vereiste informatie hebt:</span><span class="sxs-lookup"><span data-stu-id="73417-117">Before you begin, make sure that you have the following required information:</span></span>

- <span data-ttu-id="73417-118">De RCSU die wordt gebruikt</span><span class="sxs-lookup"><span data-stu-id="73417-118">The RCSU that will be used.</span></span>
- <span data-ttu-id="73417-119">De Microsoft Azure Active Directory-beveiligings groep die wordt gebruikt voor e-commerce-systeembeheerders.</span><span class="sxs-lookup"><span data-stu-id="73417-119">The Microsoft Azure Active Directory security group that will be used for e-Commerce system admins.</span></span>
- <span data-ttu-id="73417-120">De Microsoft Azure Active Directory-beveiligings groep die wordt gebruikt voor moderators van beoordelingen en recensies.</span><span class="sxs-lookup"><span data-stu-id="73417-120">The Microsoft Azure Active Directory security group that will be used for ratings and reviews moderators.</span></span>
- <span data-ttu-id="73417-121">De domeinen die aan de omgeving worden gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="73417-121">The domains that will be associated with the environment.</span></span>

<span data-ttu-id="73417-122">Bovendien kunt u de volgende optionele informatie verzamelen:</span><span class="sxs-lookup"><span data-stu-id="73417-122">In addition, you can collect the following optional information:</span></span>

- <span data-ttu-id="73417-123">Informatie over Azure AD business-to-consumer (B2C):</span><span class="sxs-lookup"><span data-stu-id="73417-123">Azure AD business-to-consumer (B2C) information:</span></span>

    - <span data-ttu-id="73417-124">Naam tenant.</span><span class="sxs-lookup"><span data-stu-id="73417-124">Tenant Name.</span></span>
    - <span data-ttu-id="73417-125">Client-id.</span><span class="sxs-lookup"><span data-stu-id="73417-125">Client ID.</span></span>
    - <span data-ttu-id="73417-126">Aangepast domein voor aanmelding.</span><span class="sxs-lookup"><span data-stu-id="73417-126">Login Custom Domain.</span></span>
    - <span data-ttu-id="73417-127">Antwoord-URL.</span><span class="sxs-lookup"><span data-stu-id="73417-127">Reply URL.</span></span>
    - <span data-ttu-id="73417-128">Beleids-id voor aanmelden registreren.</span><span class="sxs-lookup"><span data-stu-id="73417-128">SignUp SignIn Policy ID.</span></span>
    - <span data-ttu-id="73417-129">Beleid-id voor wachtwoord opnieuw instellen.</span><span class="sxs-lookup"><span data-stu-id="73417-129">Reset password Policy ID.</span></span>
    - <span data-ttu-id="73417-130">Profielbeleid-id bewerken.</span><span class="sxs-lookup"><span data-stu-id="73417-130">Edit Profile Policy ID.</span></span>

[!NOTE]
<span data-ttu-id="73417-131">Deze informatie kan later worden toegevoegd via een serviceaanvraag.</span><span class="sxs-lookup"><span data-stu-id="73417-131">This information can be added later, through a service request.</span></span>

<span data-ttu-id="73417-132">Nadat u de vereiste informatie hebt verzameld, voert u de volgende stappen uit om e-commerce te initialiseren.</span><span class="sxs-lookup"><span data-stu-id="73417-132">After you've collected the required information, follow these steps to initialize e-Commerce.</span></span>

1. <span data-ttu-id="73417-133">Meld u aan bij [LCS](https://lcs.dynamics.com).</span><span class="sxs-lookup"><span data-stu-id="73417-133">Sign in to [LCS](https://lcs.dynamics.com).</span></span>
1. <span data-ttu-id="73417-134">Open het project dat de omgeving bevat waarin u e-commerce wilt initialiseren.</span><span class="sxs-lookup"><span data-stu-id="73417-134">Open the project that contains the environment where you want to initialize e-Commerce.</span></span>
1. <span data-ttu-id="73417-135">Selecteer de omgeving in de sectie **Omgevingen**.</span><span class="sxs-lookup"><span data-stu-id="73417-135">In the **Environments** section, select the environment.</span></span>
1. <span data-ttu-id="73417-136">Selecteer de koppeling **Retail beheren** onder **Omgevingsfuncties**.</span><span class="sxs-lookup"><span data-stu-id="73417-136">Under **Environment features**, select the **Retail manage** link.</span></span>
1. <span data-ttu-id="73417-137">Selecteer op het tabblad **e-Commerce** de optie **Instellingen**.</span><span class="sxs-lookup"><span data-stu-id="73417-137">On the **e-Commerce** tab, select **Setup**.</span></span> <span data-ttu-id="73417-138">Er wordt een dialoogvenster weergegeven, waarin u de vereiste gegevens voor de inrichting moet invoeren.</span><span class="sxs-lookup"><span data-stu-id="73417-138">A dialog box appears, where you must enter the information that is required for provisioning.</span></span>
1. <span data-ttu-id="73417-139">Vul de vereiste informatie in en ga naar de volgende pagina.</span><span class="sxs-lookup"><span data-stu-id="73417-139">Fill in the required information, and then go to the next page.</span></span>
1. <span data-ttu-id="73417-140">Vul de vereiste informatie in op de volgende pagina en verzend het formulier.</span><span class="sxs-lookup"><span data-stu-id="73417-140">On the next page, fill in the required information, and then submit the form.</span></span> <span data-ttu-id="73417-141">U keert terug naar het tabblad **e-Commerce** en u ziet dat de initialisatie is gestart.</span><span class="sxs-lookup"><span data-stu-id="73417-141">You're returned to the **e-Commerce** tab, where you should see that initialization has been started.</span></span>
1. <span data-ttu-id="73417-142">Als u de initialisatiestatus wilt weergeven, kiest u **Vernieuwen** of keert u later terug naar het tabblad **e-Commerce**.</span><span class="sxs-lookup"><span data-stu-id="73417-142">To view the initialization status, either **Refresh** or return to the **e-Commerce** tab later.</span></span>
    
<span data-ttu-id="73417-143">Wanneer e-Commerce via LCS wordt geïnitialiseerd, worden verscheidene onderdelen ingesteld die nodig zijn voor e-commerce en die aan de omgeving worden gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="73417-143">When e-Commerce is initialized from LCS, the system provisions several components that are required for e-Commerce and associates them with the environment.</span></span> <span data-ttu-id="73417-144">Nadat de inrichting is voltooid, wordt het tabblad **e-Commerce** op de pagina **Beheer detailhandel** bijgewerkt om de inrichting weer te geven.</span><span class="sxs-lookup"><span data-stu-id="73417-144">After provisioning is completed, the **e-Commerce** tab on the **Retail management** page is updated to reflect the provisioning.</span></span> <span data-ttu-id="73417-145">Op de pagina worden de nieuwste implementaties van aanpassingen en de status van andere lopende implementaties weergegeven.</span><span class="sxs-lookup"><span data-stu-id="73417-145">The page shows the latest customization deployments and the status of any other ongoing deployments.</span></span> <span data-ttu-id="73417-146">De pagina bevat ook koppelingen naar de e-commerce-site en het hulpprogramma voor e-commerce-sitebeheer (het ontwerpgereedschap).</span><span class="sxs-lookup"><span data-stu-id="73417-146">It also includes links to the e-Commerce site and the e-Commerce site management tool (the authoring tool).</span></span>

## <a name="access-the-authoring-environment"></a><span data-ttu-id="73417-147">Toegang tot de ontwerpomgeving</span><span class="sxs-lookup"><span data-stu-id="73417-147">Access the authoring environment</span></span>

<span data-ttu-id="73417-148">Ga naar het tabblad **e-Commerce** op de pagina **Detailhandelbeheer** om de ontwerpomgeving te openen.</span><span class="sxs-lookup"><span data-stu-id="73417-148">To access the authoring environment, go to the **e-Commerce** tab on the **Retail management** page.</span></span> <span data-ttu-id="73417-149">Hier vindt u koppelingen naar uw e-commerce-site en het hulpprogramma voor sitebeheer.</span><span class="sxs-lookup"><span data-stu-id="73417-149">There, you will find links to your e-Commerce site and the site management tool.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="73417-150">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="73417-150">Additional resources</span></span>

[<span data-ttu-id="73417-151">Uw domeinnaam configureren</span><span class="sxs-lookup"><span data-stu-id="73417-151">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="73417-152">Een e-commerce-site maken</span><span class="sxs-lookup"><span data-stu-id="73417-152">Create an e-Commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="73417-153">Een online-site koppelen aan een kanaal</span><span class="sxs-lookup"><span data-stu-id="73417-153">Associate an online site with a channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="73417-154">Robots.txt-bestanden beheren</span><span class="sxs-lookup"><span data-stu-id="73417-154">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="73417-155">Aangepaste pagina's voor gebruikersaanmeldingen instellen</span><span class="sxs-lookup"><span data-stu-id="73417-155">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="73417-156">Ondersteuning voor een CDN (contentleveringsnetwerk) toevoegen</span><span class="sxs-lookup"><span data-stu-id="73417-156">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="73417-157">Detectie van winkels op basis van de locatie inschakelen</span><span class="sxs-lookup"><span data-stu-id="73417-157">Enable location-based store detection</span></span>](enable-store-detection.md)
