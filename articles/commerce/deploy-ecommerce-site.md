---
title: Een nieuwe e-commerce-tenant implementeren
description: In dit onderwerp wordt beschreven hoe u een nieuwe Dynamics 365 Commerce e-commerce-site implementeert met behulp van Microsoft Dynamics Lifecycle Services (LCS).
author: psimolin
manager: annbe
ms.date: 07/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: d31e3e7248809a00ad51183b80205d1351567ab3
ms.sourcegitcommit: c88b54ba13a4dfe39b844ffaced4dc435560c47d
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/19/2021
ms.locfileid: "5477871"
---
# <a name="deploy-a-new-e-commerce-tenant"></a><span data-ttu-id="da0e2-103">Een nieuwe e-commerce-tenant implementeren</span><span class="sxs-lookup"><span data-stu-id="da0e2-103">Deploy a new e-commerce tenant</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="da0e2-104">In dit onderwerp wordt beschreven hoe u een nieuwe Dynamics 365 Commerce e-commerce-site implementeert met behulp van Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="da0e2-104">This topic describes how to deploy a new Dynamics 365 Commerce e-commerce site by using Microsoft Dynamics Lifecycle Services (LCS).</span></span>

<span data-ttu-id="da0e2-105">Microsoft Dynamics Lifecycle Services (LCS) is een cloudwerkgebied dat door partners en klanten wordt gebruikt voor het beheer van hun projecten en omgevingen, het weergeven van de meest recente informatie over producten en functies van Microsoft Dynamics en het maken, volgen en zoeken van ondersteuningsaanvragen.</span><span class="sxs-lookup"><span data-stu-id="da0e2-105">Microsoft Dynamics Lifecycle Services (LCS) is a cloud-based collaborative workspace that partners and customers can use to manage their projects and environments, view the latest information about Microsoft Dynamics products and features, and create, track, and browse support incidents.</span></span> <span data-ttu-id="da0e2-106">Beheerfuncties voor e-commerce zijn in LCS geïntegreerd.</span><span class="sxs-lookup"><span data-stu-id="da0e2-106">E-commerce management features are integrated into LCS.</span></span>

<span data-ttu-id="da0e2-107">Zie de [gebruikershandleiding van Lifecycle Services](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide) voor meer informatie over LCS.</span><span class="sxs-lookup"><span data-stu-id="da0e2-107">To learn more about LCS, see the [Lifecycle Services User Guide](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide).</span></span>
    
## <a name="get-started"></a><span data-ttu-id="da0e2-108">Aan de slag</span><span class="sxs-lookup"><span data-stu-id="da0e2-108">Get started</span></span>

<span data-ttu-id="da0e2-109">Voordat u e-commerce kunt initialiseren, moet u een project, een omgeving en een Retail Cloud Scale Unit (RCSU) initialiseren.</span><span class="sxs-lookup"><span data-stu-id="da0e2-109">Before you can initialize e-commerce, you must initialize a project, an environment, and a Retail Cloud Scale Unit (RCSU).</span></span> <span data-ttu-id="da0e2-110">Als u de initialisatie wilt uitvoeren in LCS, moet u machtigingen hebben voor de rol projecteigenaar of omgevingsbeheerder.</span><span class="sxs-lookup"><span data-stu-id="da0e2-110">To do the initialization in LCS, you must have permissions for either the Project Owner or Environment manager role.</span></span> <span data-ttu-id="da0e2-111">De topologieën productie en sandbox-omgeving worden ondersteund.</span><span class="sxs-lookup"><span data-stu-id="da0e2-111">The production and sandbox environment topologies are supported.</span></span>

<span data-ttu-id="da0e2-112">Zie [Omgevingsplanning](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/imp-lifecycle/environment-planning) voor meer informatie over omgevingen.</span><span class="sxs-lookup"><span data-stu-id="da0e2-112">For more information about environments, see [Environment planning](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/imp-lifecycle/environment-planning).</span></span> <span data-ttu-id="da0e2-113">Zie [Retail Cloud Scale Unit initialiseren](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/deployment/initialize-retail-channels)voor meer informatie over RCSU.</span><span class="sxs-lookup"><span data-stu-id="da0e2-113">For more information about RCSU, see [Initialize Retail Cloud Scale Unit](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/deployment/initialize-retail-channels).</span></span>

## <a name="initialize-e-commerce"></a><span data-ttu-id="da0e2-114">e-Commerce initialiseren</span><span class="sxs-lookup"><span data-stu-id="da0e2-114">Initialize e-commerce</span></span>

<span data-ttu-id="da0e2-115">Gebruik deze procedure om de e-commerce-functie in een bestaande omgeving te initialiseren.</span><span class="sxs-lookup"><span data-stu-id="da0e2-115">Use this procedure to initialize the e-commerce feature in an existing environment.</span></span>

<span data-ttu-id="da0e2-116">Voordat u begint, moet u controleren of u de volgende vereiste informatie hebt:</span><span class="sxs-lookup"><span data-stu-id="da0e2-116">Before you begin, make sure that you have the following required information:</span></span>

- <span data-ttu-id="da0e2-117">De RCSU die wordt gebruikt</span><span class="sxs-lookup"><span data-stu-id="da0e2-117">The RCSU that will be used.</span></span>
- <span data-ttu-id="da0e2-118">De Microsoft Azure Active Directory-beveiligings groep die wordt gebruikt voor e-commerce-systeembeheerders.</span><span class="sxs-lookup"><span data-stu-id="da0e2-118">The Microsoft Azure Active Directory security group that will be used for e-commerce system admins.</span></span>
- <span data-ttu-id="da0e2-119">De Microsoft Azure Active Directory-beveiligings groep die wordt gebruikt voor moderators van beoordelingen en recensies.</span><span class="sxs-lookup"><span data-stu-id="da0e2-119">The Microsoft Azure Active Directory security group that will be used for ratings and reviews moderators.</span></span>
- <span data-ttu-id="da0e2-120">De domeinen die aan de omgeving worden gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="da0e2-120">The domains that will be associated with the environment.</span></span>

<span data-ttu-id="da0e2-121">Bovendien kunt u de volgende optionele informatie verzamelen:</span><span class="sxs-lookup"><span data-stu-id="da0e2-121">In addition, you can collect the following optional information:</span></span>

- <span data-ttu-id="da0e2-122">Informatie over Azure AD business-to-consumer (B2C):</span><span class="sxs-lookup"><span data-stu-id="da0e2-122">Azure AD business-to-consumer (B2C) information:</span></span>

    - <span data-ttu-id="da0e2-123">Naam tenant.</span><span class="sxs-lookup"><span data-stu-id="da0e2-123">Tenant Name.</span></span>
    - <span data-ttu-id="da0e2-124">Client-id.</span><span class="sxs-lookup"><span data-stu-id="da0e2-124">Client ID.</span></span>
    - <span data-ttu-id="da0e2-125">Aangepast domein voor aanmelding.</span><span class="sxs-lookup"><span data-stu-id="da0e2-125">Login Custom Domain.</span></span>
    - <span data-ttu-id="da0e2-126">Antwoord-URL.</span><span class="sxs-lookup"><span data-stu-id="da0e2-126">Reply URL.</span></span>
    - <span data-ttu-id="da0e2-127">Beleids-id voor aanmelden registreren.</span><span class="sxs-lookup"><span data-stu-id="da0e2-127">SignUp SignIn Policy ID.</span></span>
    - <span data-ttu-id="da0e2-128">Beleid-id voor wachtwoord opnieuw instellen.</span><span class="sxs-lookup"><span data-stu-id="da0e2-128">Reset password Policy ID.</span></span>
    - <span data-ttu-id="da0e2-129">Profielbeleid-id bewerken.</span><span class="sxs-lookup"><span data-stu-id="da0e2-129">Edit Profile Policy ID.</span></span>

> [!NOTE]
> <span data-ttu-id="da0e2-130">Deze informatie kan later worden toegevoegd via een serviceaanvraag.</span><span class="sxs-lookup"><span data-stu-id="da0e2-130">This information can be added later, through a service request.</span></span>

<span data-ttu-id="da0e2-131">Nadat u de vereiste informatie hebt verzameld, voert u de volgende stappen uit om e-commerce te initialiseren.</span><span class="sxs-lookup"><span data-stu-id="da0e2-131">After you've collected the required information, follow these steps to initialize e-commerce.</span></span>

1. <span data-ttu-id="da0e2-132">Meld u aan bij [LCS](https://lcs.dynamics.com).</span><span class="sxs-lookup"><span data-stu-id="da0e2-132">Sign in to [LCS](https://lcs.dynamics.com).</span></span>
1. <span data-ttu-id="da0e2-133">Open het project dat de omgeving bevat waarin u e-commerce wilt initialiseren.</span><span class="sxs-lookup"><span data-stu-id="da0e2-133">Open the project that contains the environment where you want to initialize e-commerce.</span></span>
1. <span data-ttu-id="da0e2-134">Selecteer de omgeving in de sectie **Omgevingen**.</span><span class="sxs-lookup"><span data-stu-id="da0e2-134">In the **Environments** section, select the environment.</span></span>
1. <span data-ttu-id="da0e2-135">Selecteer de koppeling **Retail beheren** onder **Omgevingsfuncties**.</span><span class="sxs-lookup"><span data-stu-id="da0e2-135">Under **Environment features**, select the **Retail manage** link.</span></span>
1. <span data-ttu-id="da0e2-136">Selecteer op het tabblad **e-Commerce** de optie **Instellingen**.</span><span class="sxs-lookup"><span data-stu-id="da0e2-136">On the **e-Commerce** tab, select **Setup**.</span></span> <span data-ttu-id="da0e2-137">Er wordt een dialoogvenster weergegeven, waarin u de vereiste gegevens voor de inrichting moet invoeren.</span><span class="sxs-lookup"><span data-stu-id="da0e2-137">A dialog box appears, where you must enter the information that is required for provisioning.</span></span>
1. <span data-ttu-id="da0e2-138">Vul de vereiste informatie in en ga naar de volgende pagina.</span><span class="sxs-lookup"><span data-stu-id="da0e2-138">Fill in the required information, and then go to the next page.</span></span>
1. <span data-ttu-id="da0e2-139">Vul de vereiste informatie in op de volgende pagina en verzend het formulier.</span><span class="sxs-lookup"><span data-stu-id="da0e2-139">On the next page, fill in the required information, and then submit the form.</span></span> <span data-ttu-id="da0e2-140">U keert terug naar het tabblad **e-Commerce** en u ziet dat de initialisatie is gestart.</span><span class="sxs-lookup"><span data-stu-id="da0e2-140">You're returned to the **e-Commerce** tab, where you should see that initialization has been started.</span></span>
1. <span data-ttu-id="da0e2-141">Als u de initialisatiestatus wilt weergeven, kiest u **Vernieuwen** of keert u later terug naar het tabblad **e-Commerce**.</span><span class="sxs-lookup"><span data-stu-id="da0e2-141">To view the initialization status, either **Refresh** or return to the **e-Commerce** tab later.</span></span>
    
<span data-ttu-id="da0e2-142">Wanneer e-Commerce via LCS wordt geïnitialiseerd, worden verscheidene onderdelen ingesteld die nodig zijn voor e-commerce en die aan de omgeving worden gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="da0e2-142">When e-commerce is initialized from LCS, the system provisions several components that are required for e-commerce and associates them with the environment.</span></span> <span data-ttu-id="da0e2-143">Nadat de inrichting is voltooid, wordt het tabblad **e-Commerce** op de pagina **Retail-beheer** bijgewerkt om de inrichting weer te geven.</span><span class="sxs-lookup"><span data-stu-id="da0e2-143">After provisioning is complete, the **e-Commerce** tab on the **Retail management** page is updated to reflect the provisioning.</span></span> <span data-ttu-id="da0e2-144">Op de pagina worden de nieuwste implementaties van aanpassingen en de status van andere lopende implementaties weergegeven.</span><span class="sxs-lookup"><span data-stu-id="da0e2-144">The page shows the latest customization deployments and the status of any other ongoing deployments.</span></span> <span data-ttu-id="da0e2-145">De pagina bevat ook koppelingen naar de e-Commerce-site en de site builder voor de e-Commerce-site waar sites worden geschreven.</span><span class="sxs-lookup"><span data-stu-id="da0e2-145">It also includes links to the e-commerce site and the Commerce site builder where sites are authored.</span></span>

## <a name="access-commerce-site-builder"></a><span data-ttu-id="da0e2-146">Commerce-site builder openen</span><span class="sxs-lookup"><span data-stu-id="da0e2-146">Access Commerce site builder</span></span>

<span data-ttu-id="da0e2-147">Ga naar het tabblad **e-Commerce** op de pagina **Retail-beheer** in LCS en selecteer de koppeling **Beheerhulpprogramma van de e-Commerce-site** om toegang te krijgen tot site builder.</span><span class="sxs-lookup"><span data-stu-id="da0e2-147">To access Commerce site builder, go to the **e-Commerce** tab on the **Retail management** page in LCS and select the **e-Commerce site management tool** link.</span></span> <span data-ttu-id="da0e2-148">De landingspagina voor site builder is een weergave op tenantniveau.</span><span class="sxs-lookup"><span data-stu-id="da0e2-148">The site builder landing page displays a tenant-level view.</span></span> <span data-ttu-id="da0e2-149">Op deze pagina kunt u het volgende doen:</span><span class="sxs-lookup"><span data-stu-id="da0e2-149">From this page, you can:</span></span>

- <span data-ttu-id="da0e2-150">Instellingen op tenantniveau wijzigen.</span><span class="sxs-lookup"><span data-stu-id="da0e2-150">Modify tenant-level settings.</span></span>
- <span data-ttu-id="da0e2-151">Naar een site gaan die u hebt gemaakt en waarvoor u weergavemachtiging hebt.</span><span class="sxs-lookup"><span data-stu-id="da0e2-151">Navigate to any site you have created, and have permission to view.</span></span> 
- <span data-ttu-id="da0e2-152">Toegang verkrijgen tot beoordelingsfuncties, zoals moderator en rapportage.</span><span class="sxs-lookup"><span data-stu-id="da0e2-152">Access Reviews features such as moderation and reporting.</span></span>
- <span data-ttu-id="da0e2-153">Maak een nieuwe site.</span><span class="sxs-lookup"><span data-stu-id="da0e2-153">Create a new site.</span></span> <span data-ttu-id="da0e2-154">Zie [Een e-Commerce-site maken](create-ecommerce-site.md) voor meer informatie over het maken van een nieuwe site.</span><span class="sxs-lookup"><span data-stu-id="da0e2-154">For more information about how to create a new site, see [Create an e-commerce site](create-ecommerce-site.md) .</span></span> 

## <a name="additional-resources"></a><span data-ttu-id="da0e2-155">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="da0e2-155">Additional resources</span></span>

[<span data-ttu-id="da0e2-156">Uw domeinnaam configureren</span><span class="sxs-lookup"><span data-stu-id="da0e2-156">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="da0e2-157">Een e-commerce-site maken</span><span class="sxs-lookup"><span data-stu-id="da0e2-157">Create an e-commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="da0e2-158">Een Dynamics 365 Commerce-site koppelen aan een online kanaal</span><span class="sxs-lookup"><span data-stu-id="da0e2-158">Associate a Dynamics 365 Commerce site with an online channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="da0e2-159">robots.txt-bestanden beheren</span><span class="sxs-lookup"><span data-stu-id="da0e2-159">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="da0e2-160">URL-omleidingen in bulk uploaden</span><span class="sxs-lookup"><span data-stu-id="da0e2-160">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

[<span data-ttu-id="da0e2-161">Een B2C-tenant instellen in Commerce</span><span class="sxs-lookup"><span data-stu-id="da0e2-161">Set up a B2C tenant in Commerce</span></span>](set-up-B2C-tenant.md)

[<span data-ttu-id="da0e2-162">Aangepaste pagina's voor gebruikersaanmeldingen instellen</span><span class="sxs-lookup"><span data-stu-id="da0e2-162">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="da0e2-163">Meerdere B2C-tenants configureren in een Commerce-omgeving</span><span class="sxs-lookup"><span data-stu-id="da0e2-163">Configure multiple B2C tenants in a Commerce environment</span></span>](configure-multi-B2C-tenants.md)

[<span data-ttu-id="da0e2-164">Ondersteuning voor een CDN (contentleveringsnetwerk) toevoegen</span><span class="sxs-lookup"><span data-stu-id="da0e2-164">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="da0e2-165">Detectie van winkels op basis van de locatie inschakelen</span><span class="sxs-lookup"><span data-stu-id="da0e2-165">Enable location-based store detection</span></span>](enable-store-detection.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
