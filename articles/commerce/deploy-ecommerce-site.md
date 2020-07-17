---
title: Een nieuwe e-commerce-tenant implementeren
description: In dit onderwerp wordt beschreven hoe u een nieuwe e-commerce-tenant implementeert met behulp van Microsoft Dynamics Lifecycle Services (LCS).
author: psimolin
manager: annbe
ms.date: 07/02/2020
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
ms.openlocfilehash: 00f35b516dbf6ab4d4d9171c84a16b89f6afe832
ms.sourcegitcommit: adf196c51e2b6f532d99c177b4c6778cea8a2efc
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 07/02/2020
ms.locfileid: "3533270"
---
# <a name="deploy-a-new-e-commerce-tenant"></a><span data-ttu-id="f7b8d-103">Een nieuwe e-commerce-tenant implementeren</span><span class="sxs-lookup"><span data-stu-id="f7b8d-103">Deploy a new e-Commerce tenant</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="f7b8d-104">In dit onderwerp wordt beschreven hoe u een nieuwe e-commerce-site implementeert met behulp van Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="f7b8d-104">This topic describes how to deploy a new e-Commerce site by using Microsoft Dynamics Lifecycle Services (LCS).</span></span>

## <a name="overview"></a><span data-ttu-id="f7b8d-105">Overzicht</span><span class="sxs-lookup"><span data-stu-id="f7b8d-105">Overview</span></span>

<span data-ttu-id="f7b8d-106">Microsoft Dynamics Lifecycle Services (LCS) is een cloudwerkgebied dat door partners en klanten wordt gebruikt voor het beheer van hun projecten en omgevingen, het weergeven van de meest recente informatie over producten en functies van Microsoft Dynamics en het maken, volgen en zoeken van ondersteuningsaanvragen.</span><span class="sxs-lookup"><span data-stu-id="f7b8d-106">Microsoft Dynamics Lifecycle Services (LCS) is a cloud-based collaborative workspace that partners and customers can use to manage their projects and environments, view the latest information about Microsoft Dynamics products and features, and create, track, and browse support incidents.</span></span> <span data-ttu-id="f7b8d-107">Beheerfuncties voor e-commerce zijn in LCS geïntegreerd.</span><span class="sxs-lookup"><span data-stu-id="f7b8d-107">E-Commerce management features are integrated into LCS.</span></span>

<span data-ttu-id="f7b8d-108">Zie de [gebruikershandleiding van Lifecycle Services](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide) voor meer informatie over LCS.</span><span class="sxs-lookup"><span data-stu-id="f7b8d-108">To learn more about LCS, see the [Lifecycle Services User Guide](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide).</span></span>
    
## <a name="get-started"></a><span data-ttu-id="f7b8d-109">Aan de slag</span><span class="sxs-lookup"><span data-stu-id="f7b8d-109">Get started</span></span>

<span data-ttu-id="f7b8d-110">Voordat u e-commerce kunt initialiseren, moet u een project, een omgeving en een Retail Cloud Scale Unit (RCSU) initialiseren.</span><span class="sxs-lookup"><span data-stu-id="f7b8d-110">Before you can initialize e-Commerce, you must initialize a project, an environment, and a Retail Cloud Scale Unit (RCSU).</span></span> <span data-ttu-id="f7b8d-111">Als u de initialisatie wilt uitvoeren in LCS, moet u machtigingen hebben voor de rol projecteigenaar of omgevingsbeheerder.</span><span class="sxs-lookup"><span data-stu-id="f7b8d-111">To do the initialization in LCS, you must have permissions for either the Project Owner or Environment manager role.</span></span> <span data-ttu-id="f7b8d-112">De topologieën productie en sandbox-omgeving worden ondersteund.</span><span class="sxs-lookup"><span data-stu-id="f7b8d-112">The production and sandbox environment topologies are supported.</span></span>

<span data-ttu-id="f7b8d-113">Zie [Omgevingsplanning](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/imp-lifecycle/environment-planning) voor meer informatie over omgevingen.</span><span class="sxs-lookup"><span data-stu-id="f7b8d-113">For more information about environments, see [Environment planning](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/imp-lifecycle/environment-planning).</span></span> <span data-ttu-id="f7b8d-114">Zie [Retail Cloud Scale Unit initialiseren](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/deployment/initialize-retail-channels)voor meer informatie over RCSU.</span><span class="sxs-lookup"><span data-stu-id="f7b8d-114">For more information about RCSU, see [Initialize Retail Cloud Scale Unit](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/deployment/initialize-retail-channels).</span></span>

## <a name="initialize-e-commerce"></a><span data-ttu-id="f7b8d-115">e-Commerce initialiseren</span><span class="sxs-lookup"><span data-stu-id="f7b8d-115">Initialize e-Commerce</span></span>

<span data-ttu-id="f7b8d-116">Gebruik deze procedure om de e-commerce-functie in een bestaande omgeving te initialiseren.</span><span class="sxs-lookup"><span data-stu-id="f7b8d-116">Use this procedure to initialize the e-Commerce feature in an existing environment.</span></span>

<span data-ttu-id="f7b8d-117">Voordat u begint, moet u controleren of u de volgende vereiste informatie hebt:</span><span class="sxs-lookup"><span data-stu-id="f7b8d-117">Before you begin, make sure that you have the following required information:</span></span>

- <span data-ttu-id="f7b8d-118">De RCSU die wordt gebruikt</span><span class="sxs-lookup"><span data-stu-id="f7b8d-118">The RCSU that will be used.</span></span>
- <span data-ttu-id="f7b8d-119">De Microsoft Azure Active Directory-beveiligings groep die wordt gebruikt voor e-commerce-systeembeheerders.</span><span class="sxs-lookup"><span data-stu-id="f7b8d-119">The Microsoft Azure Active Directory security group that will be used for e-Commerce system admins.</span></span>
- <span data-ttu-id="f7b8d-120">De Microsoft Azure Active Directory-beveiligings groep die wordt gebruikt voor moderators van beoordelingen en recensies.</span><span class="sxs-lookup"><span data-stu-id="f7b8d-120">The Microsoft Azure Active Directory security group that will be used for ratings and reviews moderators.</span></span>
- <span data-ttu-id="f7b8d-121">De domeinen die aan de omgeving worden gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="f7b8d-121">The domains that will be associated with the environment.</span></span>

<span data-ttu-id="f7b8d-122">Bovendien kunt u de volgende optionele informatie verzamelen:</span><span class="sxs-lookup"><span data-stu-id="f7b8d-122">In addition, you can collect the following optional information:</span></span>

- <span data-ttu-id="f7b8d-123">Informatie over Azure AD business-to-consumer (B2C):</span><span class="sxs-lookup"><span data-stu-id="f7b8d-123">Azure AD business-to-consumer (B2C) information:</span></span>

    - <span data-ttu-id="f7b8d-124">Naam tenant.</span><span class="sxs-lookup"><span data-stu-id="f7b8d-124">Tenant Name.</span></span>
    - <span data-ttu-id="f7b8d-125">Client-id.</span><span class="sxs-lookup"><span data-stu-id="f7b8d-125">Client ID.</span></span>
    - <span data-ttu-id="f7b8d-126">Aangepast domein voor aanmelding.</span><span class="sxs-lookup"><span data-stu-id="f7b8d-126">Login Custom Domain.</span></span>
    - <span data-ttu-id="f7b8d-127">Antwoord-URL.</span><span class="sxs-lookup"><span data-stu-id="f7b8d-127">Reply URL.</span></span>
    - <span data-ttu-id="f7b8d-128">Beleids-id voor aanmelden registreren.</span><span class="sxs-lookup"><span data-stu-id="f7b8d-128">SignUp SignIn Policy ID.</span></span>
    - <span data-ttu-id="f7b8d-129">Beleid-id voor wachtwoord opnieuw instellen.</span><span class="sxs-lookup"><span data-stu-id="f7b8d-129">Reset password Policy ID.</span></span>
    - <span data-ttu-id="f7b8d-130">Profielbeleid-id bewerken.</span><span class="sxs-lookup"><span data-stu-id="f7b8d-130">Edit Profile Policy ID.</span></span>

> [!NOTE]
> <span data-ttu-id="f7b8d-131">Deze informatie kan later worden toegevoegd via een serviceaanvraag.</span><span class="sxs-lookup"><span data-stu-id="f7b8d-131">This information can be added later, through a service request.</span></span>

<span data-ttu-id="f7b8d-132">Nadat u de vereiste informatie hebt verzameld, voert u de volgende stappen uit om e-commerce te initialiseren.</span><span class="sxs-lookup"><span data-stu-id="f7b8d-132">After you've collected the required information, follow these steps to initialize e-Commerce.</span></span>

1. <span data-ttu-id="f7b8d-133">Meld u aan bij [LCS](https://lcs.dynamics.com).</span><span class="sxs-lookup"><span data-stu-id="f7b8d-133">Sign in to [LCS](https://lcs.dynamics.com).</span></span>
1. <span data-ttu-id="f7b8d-134">Open het project dat de omgeving bevat waarin u e-commerce wilt initialiseren.</span><span class="sxs-lookup"><span data-stu-id="f7b8d-134">Open the project that contains the environment where you want to initialize e-Commerce.</span></span>
1. <span data-ttu-id="f7b8d-135">Selecteer de omgeving in de sectie **Omgevingen**.</span><span class="sxs-lookup"><span data-stu-id="f7b8d-135">In the **Environments** section, select the environment.</span></span>
1. <span data-ttu-id="f7b8d-136">Selecteer de koppeling **Retail beheren** onder **Omgevingsfuncties**.</span><span class="sxs-lookup"><span data-stu-id="f7b8d-136">Under **Environment features**, select the **Retail manage** link.</span></span>
1. <span data-ttu-id="f7b8d-137">Selecteer op het tabblad **e-Commerce** de optie **Instellingen**.</span><span class="sxs-lookup"><span data-stu-id="f7b8d-137">On the **e-Commerce** tab, select **Setup**.</span></span> <span data-ttu-id="f7b8d-138">Er wordt een dialoogvenster weergegeven, waarin u de vereiste gegevens voor de inrichting moet invoeren.</span><span class="sxs-lookup"><span data-stu-id="f7b8d-138">A dialog box appears, where you must enter the information that is required for provisioning.</span></span>
1. <span data-ttu-id="f7b8d-139">Vul de vereiste informatie in en ga naar de volgende pagina.</span><span class="sxs-lookup"><span data-stu-id="f7b8d-139">Fill in the required information, and then go to the next page.</span></span>
1. <span data-ttu-id="f7b8d-140">Vul de vereiste informatie in op de volgende pagina en verzend het formulier.</span><span class="sxs-lookup"><span data-stu-id="f7b8d-140">On the next page, fill in the required information, and then submit the form.</span></span> <span data-ttu-id="f7b8d-141">U keert terug naar het tabblad **e-Commerce** en u ziet dat de initialisatie is gestart.</span><span class="sxs-lookup"><span data-stu-id="f7b8d-141">You're returned to the **e-Commerce** tab, where you should see that initialization has been started.</span></span>
1. <span data-ttu-id="f7b8d-142">Als u de initialisatiestatus wilt weergeven, kiest u **Vernieuwen** of keert u later terug naar het tabblad **e-Commerce**.</span><span class="sxs-lookup"><span data-stu-id="f7b8d-142">To view the initialization status, either **Refresh** or return to the **e-Commerce** tab later.</span></span>
    
<span data-ttu-id="f7b8d-143">Wanneer e-Commerce via LCS wordt geïnitialiseerd, worden verscheidene onderdelen ingesteld die nodig zijn voor e-commerce en die aan de omgeving worden gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="f7b8d-143">When e-Commerce is initialized from LCS, the system provisions several components that are required for e-Commerce and associates them with the environment.</span></span> <span data-ttu-id="f7b8d-144">Nadat de inrichting is voltooid, wordt het tabblad **e-Commerce** op de pagina **Retail-beheer** bijgewerkt om de inrichting weer te geven.</span><span class="sxs-lookup"><span data-stu-id="f7b8d-144">After provisioning is complete, the **e-Commerce** tab on the **Retail management** page is updated to reflect the provisioning.</span></span> <span data-ttu-id="f7b8d-145">Op de pagina worden de nieuwste implementaties van aanpassingen en de status van andere lopende implementaties weergegeven.</span><span class="sxs-lookup"><span data-stu-id="f7b8d-145">The page shows the latest customization deployments and the status of any other ongoing deployments.</span></span> <span data-ttu-id="f7b8d-146">De pagina bevat ook koppelingen naar de e-Commerce-site en de site builder voor de e-Commerce-site waar sites worden geschreven.</span><span class="sxs-lookup"><span data-stu-id="f7b8d-146">It also includes links to the e-Commerce site and the e-Commerce site builder where sites are authored.</span></span>

## <a name="access-site-builder"></a><span data-ttu-id="f7b8d-147">Site builder openen</span><span class="sxs-lookup"><span data-stu-id="f7b8d-147">Access site builder</span></span>

<span data-ttu-id="f7b8d-148">Ga naar het tabblad **e-Commerce** op de pagina **Retail-beheer** in LCS en selecteer de koppeling **Beheerhulpprogramma van de e-Commerce-site** om toegang te krijgen tot site builder.</span><span class="sxs-lookup"><span data-stu-id="f7b8d-148">To access site builder, go to the **e-Commerce** tab on the **Retail management** page in LCS and select the **e-Commerce site management tool** link.</span></span> <span data-ttu-id="f7b8d-149">De landingspagina voor site builder is een weergave op tenantniveau.</span><span class="sxs-lookup"><span data-stu-id="f7b8d-149">The site builder landing page displays a tenant-level view.</span></span> <span data-ttu-id="f7b8d-150">Op deze pagina kunt u het volgende doen:</span><span class="sxs-lookup"><span data-stu-id="f7b8d-150">From this page, you can:</span></span>

- <span data-ttu-id="f7b8d-151">Instellingen op tenantniveau wijzigen.</span><span class="sxs-lookup"><span data-stu-id="f7b8d-151">Modify tenant-level settings.</span></span>
- <span data-ttu-id="f7b8d-152">Naar een site gaan die u hebt gemaakt en waarvoor u weergavemachtiging hebt.</span><span class="sxs-lookup"><span data-stu-id="f7b8d-152">Navigate to any site you have created, and have permission to view.</span></span> 
- <span data-ttu-id="f7b8d-153">Toegang verkrijgen tot beoordelingsfuncties, zoals moderator en rapportage.</span><span class="sxs-lookup"><span data-stu-id="f7b8d-153">Access Reviews features such as moderation and reporting.</span></span>
- <span data-ttu-id="f7b8d-154">Maak een nieuwe site.</span><span class="sxs-lookup"><span data-stu-id="f7b8d-154">Create a new site.</span></span> <span data-ttu-id="f7b8d-155">Zie [Een e-Commerce-site maken](create-ecommerce-site.md) voor meer informatie over het maken van een nieuwe site.</span><span class="sxs-lookup"><span data-stu-id="f7b8d-155">For more information about how to create a new site, see [Create an e-Commerce site](create-ecommerce-site.md) .</span></span> 

## <a name="additional-resources"></a><span data-ttu-id="f7b8d-156">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="f7b8d-156">Additional resources</span></span>

[<span data-ttu-id="f7b8d-157">Uw domeinnaam configureren</span><span class="sxs-lookup"><span data-stu-id="f7b8d-157">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="f7b8d-158">Een e-commerce-site maken</span><span class="sxs-lookup"><span data-stu-id="f7b8d-158">Create an e-Commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="f7b8d-159">Een online-site koppelen aan een kanaal</span><span class="sxs-lookup"><span data-stu-id="f7b8d-159">Associate an online site with a channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="f7b8d-160">Robots.txt-bestanden beheren</span><span class="sxs-lookup"><span data-stu-id="f7b8d-160">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="f7b8d-161">URL-omleidingen in bulk uploaden</span><span class="sxs-lookup"><span data-stu-id="f7b8d-161">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

[<span data-ttu-id="f7b8d-162">Een B2C-tenant instellen in Commerce</span><span class="sxs-lookup"><span data-stu-id="f7b8d-162">Set up a B2C tenant in Commerce</span></span>](set-up-B2C-tenant.md)

[<span data-ttu-id="f7b8d-163">Aangepaste pagina's voor gebruikersaanmeldingen instellen</span><span class="sxs-lookup"><span data-stu-id="f7b8d-163">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="f7b8d-164">Meerdere B2C-tenants configureren in een Commerce-omgeving</span><span class="sxs-lookup"><span data-stu-id="f7b8d-164">Configure multiple B2C tenants in a Commerce environment</span></span>](configure-multi-B2C-tenants.md)

[<span data-ttu-id="f7b8d-165">Ondersteuning voor een CDN (contentleveringsnetwerk) toevoegen</span><span class="sxs-lookup"><span data-stu-id="f7b8d-165">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="f7b8d-166">Detectie van winkels op basis van de locatie inschakelen</span><span class="sxs-lookup"><span data-stu-id="f7b8d-166">Enable location-based store detection</span></span>](enable-store-detection.md)
