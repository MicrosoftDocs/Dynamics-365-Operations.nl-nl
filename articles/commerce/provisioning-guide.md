---
title: Een preview-omgeving van Commerce inrichten
description: In dit onderwerp wordt uitgelegd hoe u een preview-omgeving van Microsoft Dynamics 365 Commerce inricht.
author: psimolin
manager: annbe
ms.date: 01/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: b77d2cbbc100aeae5dcd53ddbe69ff2e4435da13
ms.sourcegitcommit: 4d77d06a07ec9e7a3fcbd508afdffaa406fd3dd8
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/06/2020
ms.locfileid: "2934743"
---
# <a name="provision-a-commerce-preview-environment"></a><span data-ttu-id="22491-103">Een preview-omgeving van Commerce inrichten</span><span class="sxs-lookup"><span data-stu-id="22491-103">Provision a Commerce preview environment</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="22491-104">In dit onderwerp wordt uitgelegd hoe u een preview-omgeving van Microsoft Dynamics 365 Commerce inricht.</span><span class="sxs-lookup"><span data-stu-id="22491-104">This topic explains how to provision a Microsoft Dynamics 365 Commerce preview environment.</span></span>

<span data-ttu-id="22491-105">Voordat u begint, is het raadzaam om dit hele onderwerp door te nemen om een idee te krijgen van wat het proces inhoudt en wat dit onderwerp bevat.</span><span class="sxs-lookup"><span data-stu-id="22491-105">Before you begin, we recommend that you at least skim through this whole topic to get an idea of what the process entails and what this topic contains.</span></span>

> [!NOTE]
> <span data-ttu-id="22491-106">Als u nog geen toegang hebt gekregen tot de preview van Dynamics 365 Commerce, kunt u toegang tot de preview-versie aanvragen via de [website van Commerce](https://aka.ms/Dynamics365CommerceWebsite).</span><span class="sxs-lookup"><span data-stu-id="22491-106">If you haven't yet been granted access to the Dynamics 365 Commerce preview, you can request preview access from the [Commerce website](https://aka.ms/Dynamics365CommerceWebsite).</span></span>

## <a name="overview"></a><span data-ttu-id="22491-107">Overzicht</span><span class="sxs-lookup"><span data-stu-id="22491-107">Overview</span></span>

<span data-ttu-id="22491-108">Als u uw preview-omgeving van Commerce wilt inrichten, moet u een project maken met een specifieke productnaam en een specifiek producttype.</span><span class="sxs-lookup"><span data-stu-id="22491-108">To successfully provision your Commerce preview environment, you must create a project that has a specific product name and type.</span></span> <span data-ttu-id="22491-109">De omgeving en Retail Cloud Scale Unit (RCSU) beschikken ook over specifieke parameters die u moet gebruiken wanneer u e-Commerce later inricht.</span><span class="sxs-lookup"><span data-stu-id="22491-109">The environment and Retail Cloud Scale Unit (RCSU) also have some specific parameters that you must use when you provision e-Commerce later.</span></span> <span data-ttu-id="22491-110">De instructies in dit onderwerp beschrijven alle vereiste stappen die u moet voltooien en de parameters die u moet gebruiken.</span><span class="sxs-lookup"><span data-stu-id="22491-110">The instructions in this topic describe all the required steps that you must complete and the parameters that you must use.</span></span>

<span data-ttu-id="22491-111">Nadat de inrichting van de preview-omgeving van Commerce is voltooid, moet u een aantal stappen uitvoeren om de preview-omgeving voor te bereiden.</span><span class="sxs-lookup"><span data-stu-id="22491-111">After you successfully provision your Commerce preview environment, you must complete a few post-provisioning steps to prepare it.</span></span> <span data-ttu-id="22491-112">Sommige stappen zijn optioneel, afhankelijk van de aspecten van het systeem die u wilt evalueren.</span><span class="sxs-lookup"><span data-stu-id="22491-112">Some steps are optional, depending on the aspects of the system that you want to evaluate.</span></span> <span data-ttu-id="22491-113">U kunt de optionele stappen altijd later voltooien.</span><span class="sxs-lookup"><span data-stu-id="22491-113">You can always complete the optional steps later.</span></span>

<span data-ttu-id="22491-114">Zie [Een preview-omgeving van Commerce configureren](cpe-post-provisioning.md) voor meer informatie over hoe u uw preview-omgeving voor Commerce configureert nadat u deze hebt ingericht.</span><span class="sxs-lookup"><span data-stu-id="22491-114">For information about how to configure your Commerce preview environment after you provision it, see [Configure a Commerce preview environment](cpe-post-provisioning.md).</span></span> <span data-ttu-id="22491-115">Zie [Optionele functies voor een preview-omgeving van Commerce configureren](cpe-optional-features.md) voor meer informatie over hoe u optionele functies voor uw preview-omgeving van Commerce configureert.</span><span class="sxs-lookup"><span data-stu-id="22491-115">For information about how to configure optional features for your Commerce preview environment, see [Configure optional features for a Commerce preview environment](cpe-optional-features.md).</span></span>

<span data-ttu-id="22491-116">Als u vragen hebt over de inrichtingsstappen of als u problemen ondervindt, laat het Microsoft dan weten in de [Microsoft Dynamics 365 Commerce Preview Yammer-groep](https://aka.ms/Dynamics365CommercePreviewYammer).</span><span class="sxs-lookup"><span data-stu-id="22491-116">If you have any questions about the provisioning steps, or if you encounter any issues, let Microsoft know in the [Microsoft Dynamics 365 Commerce Preview Yammer group](https://aka.ms/Dynamics365CommercePreviewYammer).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="22491-117">Vereisten</span><span class="sxs-lookup"><span data-stu-id="22491-117">Prerequisites</span></span>

<span data-ttu-id="22491-118">Aan de volgende voorwaarden moeten zijn voldaan voordat u uw preview-omgeving van Commerce inricht:</span><span class="sxs-lookup"><span data-stu-id="22491-118">The following prerequisites must be in place before you can provision your Commerce preview environment:</span></span>

- <span data-ttu-id="22491-119">U hebt toegang tot de Microsoft Dynamics Lifecycle Services-portal (LCS).</span><span class="sxs-lookup"><span data-stu-id="22491-119">You have access to the Microsoft Dynamics Lifecycle Services (LCS) portal.</span></span>
- <span data-ttu-id="22491-120">U bent geaccepteerd voor het Dynamics 365 Commerce Preview-programma.</span><span class="sxs-lookup"><span data-stu-id="22491-120">You've been accepted into the Dynamics 365 Commerce Preview program.</span></span>
- <span data-ttu-id="22491-121">U hebt de vereiste machtigingen om een project te maken voor **Potentiële presales** uitverkoop of **Migreren, oplossingen maken en informatie over**.</span><span class="sxs-lookup"><span data-stu-id="22491-121">You have the required permissions to create a project for **Prospective presales** or **Migrate, create solutions, and learn**.</span></span>
- <span data-ttu-id="22491-122">U bent lid van de rol **Omgevingsbeheerder** of **Projecteigenaar** in het project waar u de omgeving gaat inrichten.</span><span class="sxs-lookup"><span data-stu-id="22491-122">You're a member of the **Environment manager** or **Project owner** role in the project where you will provision the environment.</span></span>
- <span data-ttu-id="22491-123">U hebt beheerderstoegang tot uw Microsoft Azure-abonnement of contact met een abonnementsbeheerder die de twee stappen kan uitvoeren waarvoor beheerdersmachtigingen namens u nodig zijn.</span><span class="sxs-lookup"><span data-stu-id="22491-123">You have admin access to your Microsoft Azure subscription, or you're in contact with a subscription admin who can complete the two steps that require admin permissions on your behalf.</span></span>
- <span data-ttu-id="22491-124">U hebt uw Azure Active Directory-tenant-id (Azure AD) bij de hand.</span><span class="sxs-lookup"><span data-stu-id="22491-124">You have your Azure Active Directory (Azure AD) tenant ID available.</span></span>
- <span data-ttu-id="22491-125">U hebt een Azure AD-beveiligingsgroep gemaakt om te gebruiken als e-Commerce-systeembeheerdersgroep en u hebt de id bij de hand.</span><span class="sxs-lookup"><span data-stu-id="22491-125">You've created an Azure AD security group that can be used as an e-Commerce system admin group, and you have its ID available.</span></span>
- <span data-ttu-id="22491-126">U hebt een Azure AD-beveiligingsgroep gemaakt om te gebruiken als moderatorgroep voor beoordelingen en recensies en u hebt de id bij de hand.</span><span class="sxs-lookup"><span data-stu-id="22491-126">You've created an Azure AD security group that can be used as a Ratings and Reviews moderator group, and you have its ID available.</span></span> <span data-ttu-id="22491-127">(Deze beveiligingsgroep kan dezelfde zijn als de systeembeheerdersgroep van e-Commerce.)</span><span class="sxs-lookup"><span data-stu-id="22491-127">(This security group can be the same as the e-Commerce system admin group.)</span></span>

### <a name="find-your-azure-ad-tenant-id"></a><span data-ttu-id="22491-128">Uw Azure AD-tenant-id zoeken</span><span class="sxs-lookup"><span data-stu-id="22491-128">Find your Azure AD tenant ID</span></span>

<span data-ttu-id="22491-129">Uw Azure AD-tenant-id is een globale unieke id (GUID) met een indeling zoals **72f988bf-86f1-41af-91ab-2d7cd011db47**.</span><span class="sxs-lookup"><span data-stu-id="22491-129">Your Azure AD tenant ID is a globally unique identifier (GUID) that resembles this example: **72f988bf-86f1-41af-91ab-2d7cd011db47**.</span></span>

#### <a name="find-your-azure-ad-tenant-id-by-using-the-azure-portal"></a><span data-ttu-id="22491-130">Uw Azure AD-tenant-id zoeken via de Azure-portal</span><span class="sxs-lookup"><span data-stu-id="22491-130">Find your Azure AD tenant ID by using the Azure portal</span></span>

1. <span data-ttu-id="22491-131">Meld u aan bij de [Azure-portal](https://portal.azure.com/).</span><span class="sxs-lookup"><span data-stu-id="22491-131">Sign in to the [Azure portal](https://portal.azure.com/).</span></span>
1. <span data-ttu-id="22491-132">Controleer of u de juiste map hebt geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="22491-132">Make sure that the correct directory is selected.</span></span>
1. <span data-ttu-id="22491-133">Selecteer **Azure Active Directory** in het linkermenu.</span><span class="sxs-lookup"><span data-stu-id="22491-133">On the menu on the left, select **Azure Active Directory**.</span></span>
1. <span data-ttu-id="22491-134">Selecteer **Eigenschappen** onder **Beheren**.</span><span class="sxs-lookup"><span data-stu-id="22491-134">Under **Manage**, select **Properties**.</span></span> <span data-ttu-id="22491-135">Uw Azure AD-tenant-id wordt weergegeven onder **Directory-id**.</span><span class="sxs-lookup"><span data-stu-id="22491-135">Your Azure AD tenant ID appears under **Directory ID**.</span></span>

#### <a name="find-your-azure-ad-tenant-id-by-using-openid-connect-metadata"></a><span data-ttu-id="22491-136">Uw Azure AD-tenant-id zoeken in metagegevens van OpenID Connect</span><span class="sxs-lookup"><span data-stu-id="22491-136">Find your Azure AD tenant ID by using OpenID Connect metadata</span></span>

<span data-ttu-id="22491-137">Maak een OpenID-URL door **\{UW\_DOMEIN\}** te vervangen door uw domein, bijvoorbeeld `microsoft.com`.</span><span class="sxs-lookup"><span data-stu-id="22491-137">Create an OpenID URL by replacing **\{YOUR\_DOMAIN\}** with your domain, such as `microsoft.com`.</span></span> <span data-ttu-id="22491-138">`https://login.microsoftonline.com/{YOUR_DOMAIN}/.well-known/openid-configuration` wordt bijvoorbeeld `https://login.microsoftonline.com/microsoft.com/.well-known/openid-configuration`.</span><span class="sxs-lookup"><span data-stu-id="22491-138">For example, `https://login.microsoftonline.com/{YOUR_DOMAIN}/.well-known/openid-configuration` will become `https://login.microsoftonline.com/microsoft.com/.well-known/openid-configuration`.</span></span>

1. <span data-ttu-id="22491-139">Ga naar de OpenID-URL die uw domein bevat.</span><span class="sxs-lookup"><span data-stu-id="22491-139">Go to the OpenID URL that contains your domain.</span></span>

    <span data-ttu-id="22491-140">U vindt uw Azure AD-tenant-id in meerdere eigenschapswaarden.</span><span class="sxs-lookup"><span data-stu-id="22491-140">You can find you Azure AD tenant ID in multiple property values.</span></span>

1. <span data-ttu-id="22491-141">Ga naar **authorization\_endpoint** en extraheer de GUID direct na `login.microsoftonline.com/`.</span><span class="sxs-lookup"><span data-stu-id="22491-141">Find **authorization\_endpoint**, and extract the GUID that appears immediately after `login.microsoftonline.com/`.</span></span>

### <a name="find-your-azure-ad-security-group-id"></a><span data-ttu-id="22491-142">De id van uw Azure AD-beveiligingsgroep zoeken</span><span class="sxs-lookup"><span data-stu-id="22491-142">Find your Azure AD security group ID</span></span>

<span data-ttu-id="22491-143">De id van uw Azure AD-beveiligingsgroep is een GUID met een indeling als **436ea7f5-ee6c-40c1-9f08-825c5811066a**.</span><span class="sxs-lookup"><span data-stu-id="22491-143">The ID of your Azure AD security group is a GUID that resembles this example: **436ea7f5-ee6c-40c1-9f08-825c5811066a**.</span></span>

<span data-ttu-id="22491-144">Bij deze procedure wordt ervan uitgegaan dat u lid bent van de groep waarvoor u de id probeert te vinden.</span><span class="sxs-lookup"><span data-stu-id="22491-144">This procedure assumes that you're a member of the group that you're trying to find the ID for.</span></span>

1. <span data-ttu-id="22491-145">Open de [grafiekverkenner](https://developer.microsoft.com/graph/graph-explorer#).</span><span class="sxs-lookup"><span data-stu-id="22491-145">Open the [Graph Explorer](https://developer.microsoft.com/graph/graph-explorer#).</span></span>
1. <span data-ttu-id="22491-146">Selecteer **Aanmelden bij Microsoft** en meld u aan met uw referenties.</span><span class="sxs-lookup"><span data-stu-id="22491-146">Select **Sign In with Microsoft**, and sign in by using your credentials.</span></span>
1. <span data-ttu-id="22491-147">Selecteer **Meer voorbeelden weergeven** links.</span><span class="sxs-lookup"><span data-stu-id="22491-147">On the left, select **show more samples**.</span></span>
1. <span data-ttu-id="22491-148">Schakel **Groepen** in het rechterdeelvenster in.</span><span class="sxs-lookup"><span data-stu-id="22491-148">In the right pane, enable **Groups**.</span></span>
1. <span data-ttu-id="22491-149">Sluit het rechterdeelvenster.</span><span class="sxs-lookup"><span data-stu-id="22491-149">Close the right pane.</span></span>
1. <span data-ttu-id="22491-150">Selecteer **Alle groepen waartoe ik behoor**.</span><span class="sxs-lookup"><span data-stu-id="22491-150">Select **all groups I belong to**.</span></span>
1. <span data-ttu-id="22491-151">Zoek uw groep in het veld **Voorbeeld van antwoord**.</span><span class="sxs-lookup"><span data-stu-id="22491-151">In the **Response Preview** field, find your group.</span></span> <span data-ttu-id="22491-152">De beveiligingsgroep-id wordt weergegeven onder de eigenschap **id**.</span><span class="sxs-lookup"><span data-stu-id="22491-152">The security group ID appears under the **id** property.</span></span>

## <a name="provision-your-commerce-preview-environment"></a><span data-ttu-id="22491-153">Uw preview-omgeving van Commerce inrichten</span><span class="sxs-lookup"><span data-stu-id="22491-153">Provision your Commerce preview environment</span></span>

<span data-ttu-id="22491-154">In deze procedures wordt uitgelegd hoe u een preview-omgeving van Commerce inricht.</span><span class="sxs-lookup"><span data-stu-id="22491-154">These procedures explain how to provision a Commerce preview environment.</span></span> <span data-ttu-id="22491-155">Als u dit hebt gedaan, is de preview-omgeving van Commerce gereed voor configuratie.</span><span class="sxs-lookup"><span data-stu-id="22491-155">After you successfully complete them, the Commerce preview environment will be ready for configuration.</span></span> <span data-ttu-id="22491-156">Alle activiteiten die hier worden beschreven, vinden plaats in de LCS-portal.</span><span class="sxs-lookup"><span data-stu-id="22491-156">All the activities that are described here occur in the LCS portal.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="22491-157">Preview-toegang is gekoppeld aan de LCS-account en organisatie die u hebt opgegeven in uw preview-toepassing.</span><span class="sxs-lookup"><span data-stu-id="22491-157">Preview access is tied to the LCS account and organization that you specified in your preview application.</span></span> <span data-ttu-id="22491-158">U moet dezelfde account gebruiken om de preview-omgeving van Commerce in te richten.</span><span class="sxs-lookup"><span data-stu-id="22491-158">You must use the same account to provision the Commerce preview environment.</span></span> <span data-ttu-id="22491-159">Als u een andere LCS-account of tenant voor de preview-omgeving van Commerce moet gebruiken, moet u deze gegevens aan Microsoft verstrekken.</span><span class="sxs-lookup"><span data-stu-id="22491-159">If you must use a different LCS account or tenant for the Commerce preview environment, you must provide those details to Microsoft.</span></span> <span data-ttu-id="22491-160">Zie de sectie [Ondersteuning voor preview-omgeving van Commerce](#commerce-preview-environment-support) verderop in dit onderwerp voor contactgegevens.</span><span class="sxs-lookup"><span data-stu-id="22491-160">For contact information, see the [Commerce preview environment support](#commerce-preview-environment-support) section later in this topic.</span></span>

### <a name="grant-access-to-e-commerce-applications"></a><span data-ttu-id="22491-161">Toegang verlenen tot e-Commerce-toepassingen</span><span class="sxs-lookup"><span data-stu-id="22491-161">Grant access to e-Commerce applications</span></span>

> [!IMPORTANT]
> <span data-ttu-id="22491-162">De persoon die zich aanmeldt, moet een Azure AD-tenantbeheerder met de Azure AD-tenant-id zijn.</span><span class="sxs-lookup"><span data-stu-id="22491-162">The person who signs in must be an Azure AD tenant admin who has the Azure AD tenant ID.</span></span> <span data-ttu-id="22491-163">Als u deze stap niet kunt voltooien, mislukken de resterende inrichtingsstappen ook.</span><span class="sxs-lookup"><span data-stu-id="22491-163">If this step isn't successfully completed, the remaining provisioning steps will fail.</span></span>

<span data-ttu-id="22491-164">Ga als volgt te werk om e-Commerce-toepassingen te autoriseren voor toegang tot uw Azure-abonnement.</span><span class="sxs-lookup"><span data-stu-id="22491-164">To authorize e-Commerce applications to access your Azure subscription, follow these steps.</span></span>

1. <span data-ttu-id="22491-165">Stel een URL in de volgende indeling samen:</span><span class="sxs-lookup"><span data-stu-id="22491-165">Assemble a URL in the following format:</span></span>

    `https://login.windows.net/{AAD_TENANT_ID}/oauth2/authorize?client_id=fbcbf727-cd18-4422-a723-f8274075331a&response_type=code&redirect_uri=https://sb.manage.commerce.dynamics.com/_commerce/Consent&response_mode=query&prompt=admin_consent&state=12345`

1. <span data-ttu-id="22491-166">Kopieer en plak de URL in uw browser of teksteditor en vervang **\{AAD\_TENANT\_ID\}** door uw Azure AD-tenant-id.</span><span class="sxs-lookup"><span data-stu-id="22491-166">Copy and paste the URL into your browser or text editor, and replace **\{AAD\_TENANT\_ID\}** with your Azure AD tenant ID.</span></span> <span data-ttu-id="22491-167">Open de URL.</span><span class="sxs-lookup"><span data-stu-id="22491-167">Then open the URL.</span></span>
1. <span data-ttu-id="22491-168">Meld u aan in het dialoogvenster voor aanmelding bij Azure AD en bevestig dat u **Dynamics 365 Commerce (preview)** toegang wilt verlenen tot uw abonnement.</span><span class="sxs-lookup"><span data-stu-id="22491-168">In the Azure AD sign-in dialog box, sign in, and confirm that you want to grant **Dynamics 365 Commerce (Preview)** access to your subscription.</span></span> <span data-ttu-id="22491-169">U wordt omgeleid naar een pagina waarop wordt aangegeven of de bewerking is geslaagd.</span><span class="sxs-lookup"><span data-stu-id="22491-169">You're redirected to a page that indicates whether the operation was successful.</span></span>

### <a name="confirm-that-preview-features-are-available-and-turned-on-in-lcs"></a><span data-ttu-id="22491-170">Controleren of de preview-functies beschikbaar zijn en zijn ingeschakeld in LCS</span><span class="sxs-lookup"><span data-stu-id="22491-170">Confirm that preview features are available and turned on in LCS</span></span>

<span data-ttu-id="22491-171">Ga als volgt te werk om te controleren of de preview-functies beschikbaar zijn en zijn ingeschakeld in LCS.</span><span class="sxs-lookup"><span data-stu-id="22491-171">To confirm that preview features are available and turned on in LCS, follow these steps.</span></span>

1. <span data-ttu-id="22491-172">Meld u aan bij de [LCS-portal](https://lcs.dynamics.com) met dezelfde LCS-account die u hebt gebruikt om toegang tot de preview aan te vragen.</span><span class="sxs-lookup"><span data-stu-id="22491-172">Sign in to the [LCS portal](https://lcs.dynamics.com) by using the same LCS account that you used to request access to the preview.</span></span>
1. <span data-ttu-id="22491-173">Schuif op de LCS-startpagina helemaal naar rechts en selecteer de tegel **Beheer van voorbeeldfuncties**.</span><span class="sxs-lookup"><span data-stu-id="22491-173">On the LCS home page, scroll all the way to the right, and select the **Preview feature management** tile.</span></span>

    ![Tegel Beheer van voorbeeldfuncties](./media/preview1.png)

1. <span data-ttu-id="22491-175">Schuif omlaag naar **Particuliere voorbeeldfuncties** en controleer of de volgende functies beschikbaar en ingeschakeld zijn:</span><span class="sxs-lookup"><span data-stu-id="22491-175">Scroll down to **Private preview features**, and confirm that the following features are available and turned on:</span></span>

    - <span data-ttu-id="22491-176">Evaluatie van e-Commerce</span><span class="sxs-lookup"><span data-stu-id="22491-176">e-Commerce Evaluation</span></span>
    - <span data-ttu-id="22491-177">Programma-omgevingen voor Commerce Preview</span><span class="sxs-lookup"><span data-stu-id="22491-177">Commerce Preview Program Environments</span></span>

    ![Particuliere voorbeeldfuncties](./media/preview2.png)

1. <span data-ttu-id="22491-179">Als deze functies niet worden weergegeven in de lijst, neemt u contact op met Microsoft en geef u uw zakelijke e-mailadres, LCS-account en tenantgegevens op.</span><span class="sxs-lookup"><span data-stu-id="22491-179">If those features don't appear in the list, contact Microsoft, and provide your work email address, LCS account, and tenant details.</span></span> <span data-ttu-id="22491-180">Zie de sectie [Ondersteuning voor preview-omgeving van Commerce](#commerce-preview-environment-support) voor contactgegevens.</span><span class="sxs-lookup"><span data-stu-id="22491-180">For contact information, see the [Commerce preview environment support](#commerce-preview-environment-support) section.</span></span>

### <a name="create-a-new-project"></a><span data-ttu-id="22491-181">Een nieuw project maken</span><span class="sxs-lookup"><span data-stu-id="22491-181">Create a new project</span></span>

<span data-ttu-id="22491-182">Ga als volgt te werk om een nieuw project te maken in LCS.</span><span class="sxs-lookup"><span data-stu-id="22491-182">To create a new project in LCS, follow these steps.</span></span>

1. <span data-ttu-id="22491-183">Selecteer op de LCS-startpagina het plusteken (**+**) om een project te maken.</span><span class="sxs-lookup"><span data-stu-id="22491-183">On the LCS home page, select the plus sign (**+**) to create a project.</span></span>
1. <span data-ttu-id="22491-184">Volg een van de volgende stappen uit in het rechterdeelvenster:</span><span class="sxs-lookup"><span data-stu-id="22491-184">In the right pane, follow one of these steps:</span></span>

    - <span data-ttu-id="22491-185">Als u een partner bent, selecteert u **Migreren, oplossingen maken en informatie over**.</span><span class="sxs-lookup"><span data-stu-id="22491-185">If you're a partner, select **Migrate, create solutions, and learn**.</span></span>
    - <span data-ttu-id="22491-186">Als u een klant bent, selecteert u **Potentiële presales**.</span><span class="sxs-lookup"><span data-stu-id="22491-186">If you're a customer, select **Prospective presales**.</span></span>

1. <span data-ttu-id="22491-187">Voer een naam, beschrijving en branche in.</span><span class="sxs-lookup"><span data-stu-id="22491-187">Enter a name, description, and industry.</span></span>
1. <span data-ttu-id="22491-188">Selecteer **Dynamics 365 Retail** in het veld **Productnaam**.</span><span class="sxs-lookup"><span data-stu-id="22491-188">In the **Product name** field, select **Dynamics 365 Retail**.</span></span>
1. <span data-ttu-id="22491-189">Selecteer **Dynamics 365 Retail** in het veld **Productversie**.</span><span class="sxs-lookup"><span data-stu-id="22491-189">In the **Product version** field, select **Dynamics 365 Retail**.</span></span>
1. <span data-ttu-id="22491-190">Selecteer **Implementatiemethodologie voor Dynamics Retail** in het veld **Methodologie**.</span><span class="sxs-lookup"><span data-stu-id="22491-190">In the **Methodology** field, select **Dynamics Retail implementation methodology**.</span></span>
1. <span data-ttu-id="22491-191">Optioneel: u kunt rollen en gebruikers importeren uit bestaand project.</span><span class="sxs-lookup"><span data-stu-id="22491-191">Optional: You can import roles and users from an existing project.</span></span>
1. <span data-ttu-id="22491-192">Selecteer **Maken**.</span><span class="sxs-lookup"><span data-stu-id="22491-192">Select **Create**.</span></span> <span data-ttu-id="22491-193">De projectweergave wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="22491-193">The project view appears.</span></span>

### <a name="add-the-azure-connector"></a><span data-ttu-id="22491-194">De Azure-connector toevoegen</span><span class="sxs-lookup"><span data-stu-id="22491-194">Add the Azure Connector</span></span>

<span data-ttu-id="22491-195">Ga als volgt te werk om de Azure-connector toe te voegen aan uw LCS-project.</span><span class="sxs-lookup"><span data-stu-id="22491-195">To add the Azure Connector to your LCS project, follow these steps.</span></span>

1. <span data-ttu-id="22491-196">Volg één van deze stappen:</span><span class="sxs-lookup"><span data-stu-id="22491-196">Follow one of these steps:</span></span>

    - <span data-ttu-id="22491-197">Als u een partner bent, selecteert u de tegel **Projectinstellingen** uiterst rechts.</span><span class="sxs-lookup"><span data-stu-id="22491-197">If you're a partner, select the **Project settings** tile on the far right.</span></span>
    - <span data-ttu-id="22491-198">Als u een klant bent, selecteert u **Projectinstellingen** in het bovenste menu.</span><span class="sxs-lookup"><span data-stu-id="22491-198">If you're a customer, select **Project settings** on the top menu.</span></span>

1. <span data-ttu-id="22491-199">Selecteer **Azure-connectors**.</span><span class="sxs-lookup"><span data-stu-id="22491-199">Select **Azure connectors**.</span></span>
1. <span data-ttu-id="22491-200">Selecteer **Toevoegen** om de Azure-connector toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="22491-200">Select **Add** to add the Azure Connector.</span></span>
1. <span data-ttu-id="22491-201">Voer een naam in.</span><span class="sxs-lookup"><span data-stu-id="22491-201">Enter a name.</span></span>
1. <span data-ttu-id="22491-202">Voer uw Azure-abonnements-id in.</span><span class="sxs-lookup"><span data-stu-id="22491-202">Enter your Azure subscription ID.</span></span>
1. <span data-ttu-id="22491-203">Schakel de optie **Configureren om Azure Resource Manager (ARM) te gebruiken** in.</span><span class="sxs-lookup"><span data-stu-id="22491-203">Turn on the **Configure to use Azure Resource Manager (ARM)** option.</span></span>
1. <span data-ttu-id="22491-204">Controleer of de waarde **Azure-abonnement AAD-tenantdomein (of id)** juist is.</span><span class="sxs-lookup"><span data-stu-id="22491-204">Verify that the **Azure subscription AAD Tenant Domain (or ID)** value is correct.</span></span> <span data-ttu-id="22491-205">Neem zo nodig contact op met uw Azure-abonnementsbeheerder.</span><span class="sxs-lookup"><span data-stu-id="22491-205">Consult your Azure subscription admin as required.</span></span>
1. <span data-ttu-id="22491-206">Selecteer **Volgende**.</span><span class="sxs-lookup"><span data-stu-id="22491-206">Select **Next**.</span></span>
1. <span data-ttu-id="22491-207">Volg de instructies op de pagina om de vereiste toepassingen toegang te verlenen tot uw abonnement.</span><span class="sxs-lookup"><span data-stu-id="22491-207">Follow the instructions on the page to grant the required applications access to your subscription.</span></span> <span data-ttu-id="22491-208">Neem zo nodig contact op met uw Azure-abonnementsbeheerder.</span><span class="sxs-lookup"><span data-stu-id="22491-208">Consult your Azure subscription admin as required.</span></span>

    1. <span data-ttu-id="22491-209">Meld u aan bij de [Azure-portal](https://portal.azure.com/).</span><span class="sxs-lookup"><span data-stu-id="22491-209">Sign in to the [Azure portal](https://portal.azure.com/).</span></span>
    1. <span data-ttu-id="22491-210">Zorg ervoor dat de juiste map is geselecteerd en selecteer vervolgens in het menu aan de linkerkant **Abonnementen**.</span><span class="sxs-lookup"><span data-stu-id="22491-210">Make sure that the correct directory is selected, and then, on the menu on the left, select **Subscriptions**.</span></span>
    1. <span data-ttu-id="22491-211">Zoek het juiste abonnement in de lijst en selecteer dit.</span><span class="sxs-lookup"><span data-stu-id="22491-211">Find the correct subscription in the list, and select it.</span></span> <span data-ttu-id="22491-212">Gebruik de zoekfunctie zoals vereist.</span><span class="sxs-lookup"><span data-stu-id="22491-212">Use the search functionality as required.</span></span>
    1. <span data-ttu-id="22491-213">Selecteer **Toegangscontrole (IAM)** in het menu.</span><span class="sxs-lookup"><span data-stu-id="22491-213">On the menu, select **Access control (IAM)**.</span></span>
    1. <span data-ttu-id="22491-214">Selecteer **Toevoegen** rechts onder **Een roltoewijzing toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="22491-214">On the right, under **Add a role assignment**, select **Add**.</span></span> <span data-ttu-id="22491-215">Het deelvenster **Roltoewijzing toevoegen** wordt geopend.</span><span class="sxs-lookup"><span data-stu-id="22491-215">The **Add role assignment** pane appears.</span></span>
    1. <span data-ttu-id="22491-216">Selecteer in het veld **Rol** de waarde **Bijdrager**.</span><span class="sxs-lookup"><span data-stu-id="22491-216">In the **Role** field, select **Contributor**.</span></span>
    1. <span data-ttu-id="22491-217">Laat in het veld **Toegang toewijzen aan** de standaardwaarde **Azure AD-gebruiker, -groep of serviceprincipal** ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="22491-217">In the **Assign access to** field, leave the default value, **Azure AD user, group, or service principal**.</span></span>
    1. <span data-ttu-id="22491-218">Klik onder **Selecteren** op **b96b7e94-b82e-4e71-99a0-cf7fb188acea**.</span><span class="sxs-lookup"><span data-stu-id="22491-218">Under **Select**, enter **b96b7e94-b82e-4e71-99a0-cf7fb188acea**.</span></span>
    1. <span data-ttu-id="22491-219">Selecteer **Dynamics Deployment Services \[wsfed-enabled\]** in de lijst.</span><span class="sxs-lookup"><span data-stu-id="22491-219">Select **Dynamics Deployment Services \[wsfed-enabled\]** in the list.</span></span>
    1. <span data-ttu-id="22491-220">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="22491-220">Select **Save**.</span></span>

1. <span data-ttu-id="22491-221">Selecteer **Volgende**.</span><span class="sxs-lookup"><span data-stu-id="22491-221">Select **Next**.</span></span>
1. <span data-ttu-id="22491-222">Volg de instructies op de pagina om de vereiste toepassingen toegang te verlenen tot uw abonnement.</span><span class="sxs-lookup"><span data-stu-id="22491-222">Follow the instructions on the page to grant the required applications access to your subscription.</span></span> <span data-ttu-id="22491-223">Neem zo nodig contact op met uw Azure-abonnementsbeheerder.</span><span class="sxs-lookup"><span data-stu-id="22491-223">Consult your Azure subscription admin as required.</span></span>
1. <span data-ttu-id="22491-224">Selecteer **Volgende**.</span><span class="sxs-lookup"><span data-stu-id="22491-224">Select **Next**.</span></span>
1. <span data-ttu-id="22491-225">Kies voor **Azure-regio** de optie **VS - oost**, **VS - oost 2**, **VS - west** of **VS - west 2**.</span><span class="sxs-lookup"><span data-stu-id="22491-225">In the **Azure region** field, select **East US**, **East US 2**, **West US**, or **West US 2**.</span></span>
1. <span data-ttu-id="22491-226">Selecteer **Verbinding maken**.</span><span class="sxs-lookup"><span data-stu-id="22491-226">Select **Connect**.</span></span> <span data-ttu-id="22491-227">De Azure-connector wordt weergegeven in de lijst.</span><span class="sxs-lookup"><span data-stu-id="22491-227">Your Azure Connector should appear in the list.</span></span>

### <a name="import-the-commerce-preview-demo-base-extension"></a><span data-ttu-id="22491-228">Extensie voor demobasis van Commerce-preview importeren</span><span class="sxs-lookup"><span data-stu-id="22491-228">Import the Commerce Preview Demo Base Extension</span></span>

<span data-ttu-id="22491-229">Voer de volgende stappen uit om de extensie voor de demobasis van de Commerce-preview in uw project te importeren.</span><span class="sxs-lookup"><span data-stu-id="22491-229">To import the Commerce Preview Demo Base Extension into your project, follow these steps.</span></span>

1. <span data-ttu-id="22491-230">Open de startpagina voor uw project door de projectnaam bovenaan te selecteren.</span><span class="sxs-lookup"><span data-stu-id="22491-230">Open the home page for your project by selecting the project name at the top.</span></span>
1. <span data-ttu-id="22491-231">Volg één van deze stappen:</span><span class="sxs-lookup"><span data-stu-id="22491-231">Follow one of these steps:</span></span>

    - <span data-ttu-id="22491-232">Als u een partner bent, selecteert u de tegel **Activabibliotheek** uiterst rechts.</span><span class="sxs-lookup"><span data-stu-id="22491-232">If you're a partner, select the **Asset library** tile on the far right.</span></span>
    - <span data-ttu-id="22491-233">Als u een klant bent, selecteert u **Activabibliotheek** in het bovenste menu.</span><span class="sxs-lookup"><span data-stu-id="22491-233">If you're a customer, select **Asset library** on the top menu.</span></span>

1. <span data-ttu-id="22491-234">Selecteer **Implementeerbaar softwarepakket** in de lijst aan de linkerkant.</span><span class="sxs-lookup"><span data-stu-id="22491-234">In the list on the left, select **Software deployable package**.</span></span>
1. <span data-ttu-id="22491-235">Selecteer **Importeren**.</span><span class="sxs-lookup"><span data-stu-id="22491-235">Select **Import**.</span></span>
1. <span data-ttu-id="22491-236">Selecteer **Extensie voor Commerce Preview-demobasis** in de lijst met activa onder **Bibliotheek voor gedeelde activa**.</span><span class="sxs-lookup"><span data-stu-id="22491-236">Under **Shared asset library**, select **Commerce Preview Demo Base Extension** in the list of assets.</span></span>
1. <span data-ttu-id="22491-237">Selecteer **Verzamelen**.</span><span class="sxs-lookup"><span data-stu-id="22491-237">Select **Pick**.</span></span> <span data-ttu-id="22491-238">U keert terug naar de activabibliotheek en de extensie wordt weergegeven in de lijst.</span><span class="sxs-lookup"><span data-stu-id="22491-238">You're returned to the Asset library, and you should see the extension in the list.</span></span>

<span data-ttu-id="22491-239">In de volgende afbeelding ziet u de acties die moeten worden ondernomen op de LCS-pagina **Activabibliotheek**.</span><span class="sxs-lookup"><span data-stu-id="22491-239">The following illustration shows the actions that must be taken on the LCS **Asset library** page.</span></span>

![De extensie voor de demobasis van de Commerce-preview importeren](./media/import.png)

### <a name="deploy-the-environment"></a><span data-ttu-id="22491-241">De omgeving implementeren</span><span class="sxs-lookup"><span data-stu-id="22491-241">Deploy the environment</span></span>

<span data-ttu-id="22491-242">Ga als volgt te werk om de omgeving te implementeren.</span><span class="sxs-lookup"><span data-stu-id="22491-242">To deploy the environment, follow these steps.</span></span>

> [!NOTE]
> <span data-ttu-id="22491-243">Het is mogelijk dat u de stappen 6, 7 en/of 8 niet hoeft te voltooien, omdat pagina's met één optie worden overgeslagen.</span><span class="sxs-lookup"><span data-stu-id="22491-243">You might not have to complete steps 6, 7, and/or 8, because pages that have a single option are skipped.</span></span> <span data-ttu-id="22491-244">Controleer in de weergave **Omgevingsparameters** of u de tekst **Dynamics 365 Commerce (Preview) - Demo (10.0.6 met Platform update 30)** direct boven het veld **Omgevingsnaam** ziet.</span><span class="sxs-lookup"><span data-stu-id="22491-244">When you're in the **Environment parameters** view, confirm that the text **Dynamics 365 Commerce (Preview) - Demo (10.0.6 with Platform update 30)** appears directly above the **Environment name** field.</span></span> <span data-ttu-id="22491-245">Zie de afbeelding die na stap 8 wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="22491-245">See the illustration that appears after step 8.</span></span>

1. <span data-ttu-id="22491-246">Selecteer in het bovenste menu de optie **Cloudomgevingen**.</span><span class="sxs-lookup"><span data-stu-id="22491-246">On the top menu, select **Cloud-hosted environments**.</span></span>
1. <span data-ttu-id="22491-247">Selecteer **Toevoegen** om een omgeving toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="22491-247">Select **Add** to add an environment.</span></span>
1. <span data-ttu-id="22491-248">Selecteer **10.0.6** in het veld **Toepassingsversie**.</span><span class="sxs-lookup"><span data-stu-id="22491-248">In the **Application version** field, select **10.0.6**.</span></span>
1. <span data-ttu-id="22491-249">Selecteer bij **Platformversie** de optie **Platformupdate 30**.</span><span class="sxs-lookup"><span data-stu-id="22491-249">In the **Platform version** field, select **Platform Update 30**.</span></span>

    ![Toepassings- en platformversies selecteren](./media/project1.png)

1. <span data-ttu-id="22491-251">Selecteer **Volgende**.</span><span class="sxs-lookup"><span data-stu-id="22491-251">Select **Next**.</span></span>
1. <span data-ttu-id="22491-252">Selecteer **Demo** als de omgevingstopologie.</span><span class="sxs-lookup"><span data-stu-id="22491-252">Select **Demo** as the environment topology.</span></span>

    ![De omgevingstopologie 1 selecteren](./media/project2.png)

1. <span data-ttu-id="22491-254">Selecteer **Dynamics 365 Commerce (Preview) - Demo** als de omgevingstopologie.</span><span class="sxs-lookup"><span data-stu-id="22491-254">Select **Dynamics 365 Commerce (Preview) - Demo** as the environment topology.</span></span> <span data-ttu-id="22491-255">Als u één Azure-connector eerder hebt geconfigureerd, wordt deze gebruikt voor deze omgeving.</span><span class="sxs-lookup"><span data-stu-id="22491-255">If you configured a single Azure Connector earlier, it will be used for this environment.</span></span> <span data-ttu-id="22491-256">Als u meerdere Azure-connectors hebt geconfigureerd, kunt u kiezen welke connector u wilt gebruiken: **VS - oost**, **VS - oost 2**, **VS - west**, **VS - west 2**.</span><span class="sxs-lookup"><span data-stu-id="22491-256">If you configured multiple Azure Connectors, you can select which connector to use: **East US**, **East US 2**, **West US**, or **West US 2**.</span></span> <span data-ttu-id="22491-257">(Voor de beste end-to-end-prestaties raden we aan **VS - west 2** te selecteren.)</span><span class="sxs-lookup"><span data-stu-id="22491-257">(For the best end-to-end performance, we recommend that you select **West US 2**.)</span></span>

    ![De omgevingstopologie 2 selecteren](./media/project3.png)

1. <span data-ttu-id="22491-259">Voer op de pagina **Omgeving implementeren** een omgevingsnaam in.</span><span class="sxs-lookup"><span data-stu-id="22491-259">On the **Deploy environment** page, enter an environment name.</span></span> <span data-ttu-id="22491-260">Laat geavanceerde instellingen ongewijzigd.</span><span class="sxs-lookup"><span data-stu-id="22491-260">Leave the advanced settings as they are.</span></span>

    ![De pagina Omgeving implementeren](./media/project4.png)

1. <span data-ttu-id="22491-262">Pas de VM-grootte naar wens aan.</span><span class="sxs-lookup"><span data-stu-id="22491-262">Adjust the VM size as required.</span></span> <span data-ttu-id="22491-263">(We raden VM-voorraadeenheid \[SKU\] **D13 v2** aan.)</span><span class="sxs-lookup"><span data-stu-id="22491-263">(We recommend VM stock keeping unit \[SKU\] **D13 v2**.)</span></span>
1. <span data-ttu-id="22491-264">Controleer de prijs- en licentievoorwaarden en schakel vervolgens het selectievakje in om aan te geven dat u ermee instemt.</span><span class="sxs-lookup"><span data-stu-id="22491-264">Review the pricing and licensing terms, and then select the check box to indicate that you agree to them.</span></span>
1. <span data-ttu-id="22491-265">Selecteer **Volgende**.</span><span class="sxs-lookup"><span data-stu-id="22491-265">Select **Next**.</span></span>
1. <span data-ttu-id="22491-266">Controleer op de bevestigingspagina voor de implementatie of de details juist zijn en klik op **Implementeren**.</span><span class="sxs-lookup"><span data-stu-id="22491-266">On the deployment confirmation page, verify that the details are correct, and then select **Deploy**.</span></span> <span data-ttu-id="22491-267">U keert terug naar de weergave in **Cloudomgevingen** en uw omgeving wordt weergegeven in de lijst.</span><span class="sxs-lookup"><span data-stu-id="22491-267">You're returned to the **Cloud-hosted environments** view, and your environment should appear in the list.</span></span>

    <span data-ttu-id="22491-268">Uw aangevraagde omgeving wordt weergegeven in de wachtrij en vervolgens geïmplementeerd.</span><span class="sxs-lookup"><span data-stu-id="22491-268">Your requested environment will appear as queued and then deploying.</span></span> <span data-ttu-id="22491-269">Het duurt even voordat de werkstromen van de omgeving zijn voltooid.</span><span class="sxs-lookup"><span data-stu-id="22491-269">The environment workflows will take some time to be completed.</span></span> <span data-ttu-id="22491-270">Controleer dit daarom na ongeveer zes tot negen uur.</span><span class="sxs-lookup"><span data-stu-id="22491-270">Therefore, check back after approximately six to nine hours.</span></span>

1. <span data-ttu-id="22491-271">Voordat u verdergaat, moet u controleren of de omgevingsstatus **Geïmplementeerd** is.</span><span class="sxs-lookup"><span data-stu-id="22491-271">Before you continue, make sure that the status of your environment is **Deployed**.</span></span>

### <a name="initialize-rcsu"></a><span data-ttu-id="22491-272">RCSU initialiseren</span><span class="sxs-lookup"><span data-stu-id="22491-272">Initialize RCSU</span></span>

<span data-ttu-id="22491-273">Ga als volgt te werk om RCSU te initialiseren.</span><span class="sxs-lookup"><span data-stu-id="22491-273">To initialize RCSU, follow these steps.</span></span>

1. <span data-ttu-id="22491-274">Selecteer in de weergave **Cloudomgevingen** uw omgeving in de lijst.</span><span class="sxs-lookup"><span data-stu-id="22491-274">In the **Cloud-hosted environments** view, select your environment in the list.</span></span>
1. <span data-ttu-id="22491-275">Klik op **Volledige details** in de omgevingsweergave rechts.</span><span class="sxs-lookup"><span data-stu-id="22491-275">In the environment view on the right, select **Full details**.</span></span> <span data-ttu-id="22491-276">De weergave met omgevingsdetails wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="22491-276">The environment details view appears.</span></span>
1. <span data-ttu-id="22491-277">Selecteer **Beheren** onder **Omgevingsfuncties**.</span><span class="sxs-lookup"><span data-stu-id="22491-277">Under **Environment features**, select **Manage**.</span></span>
1. <span data-ttu-id="22491-278">Selecteer **Initialiseren** op het tabblad **Retail**.</span><span class="sxs-lookup"><span data-stu-id="22491-278">On the **Retail** tab, select **Initialize**.</span></span> <span data-ttu-id="22491-279">De weergave RCSU-initialisatieparameters wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="22491-279">The RCSU initialization parameters view appears.</span></span>
1. <span data-ttu-id="22491-280">Kies voor **Regio** de optie **VS - oost**, **VS - oost 2**, **VS - west** of **VS - west 2**.</span><span class="sxs-lookup"><span data-stu-id="22491-280">In the **Region** field, select **East US**, **East US 2**, **West US**, or **West US 2**.</span></span>
1. <span data-ttu-id="22491-281">Selecteer in het veld **Versie** de optie **Een versie opgeven** in de lijst en geef **9.16.19262.5** op in het veld dat wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="22491-281">In the **Version** field, select **Specify a version** in the list, and then specify **9.16.19262.5** in the field that appears.</span></span> <span data-ttu-id="22491-282">Geef de exacte versie op die hier wordt aangegeven.</span><span class="sxs-lookup"><span data-stu-id="22491-282">Be sure to specify the exact version that is indicated here.</span></span> <span data-ttu-id="22491-283">Anders moet u RCSU later bijwerken naar de juiste versie.</span><span class="sxs-lookup"><span data-stu-id="22491-283">Otherwise, you will have to update RCSU to the correct version later.</span></span>
1. <span data-ttu-id="22491-284">Schakel de optie **Extensie toepassen** in.</span><span class="sxs-lookup"><span data-stu-id="22491-284">Turn on the **Apply extension** option.</span></span>
1. <span data-ttu-id="22491-285">Selecteer **Extensie voor Commerce Preview-demobasis** in de lijst met extensies.</span><span class="sxs-lookup"><span data-stu-id="22491-285">In the list of extensions, select **Commerce Preview Demo Base Extension**.</span></span>
1. <span data-ttu-id="22491-286">Selecteer **Initialiseren**.</span><span class="sxs-lookup"><span data-stu-id="22491-286">Select **Initialize**.</span></span>
1. <span data-ttu-id="22491-287">Controleer op de bevestigingspagina voor de implementatie of de details juist zijn en klik op **Ja**.</span><span class="sxs-lookup"><span data-stu-id="22491-287">On the deployment confirmation page, verify that the details are correct, and then select **Yes**.</span></span> <span data-ttu-id="22491-288">U keert terug naar de weergave **Beheer detailhandel** waar het tabblad **Detailhandel** is geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="22491-288">You're returned to the **Retail management** view, where the **Retail** tab is selected.</span></span> <span data-ttu-id="22491-289">Uw RCSU is in de wachtrij geplaatst voor inrichting.</span><span class="sxs-lookup"><span data-stu-id="22491-289">Your RCSU has been queued for provisioning.</span></span>
1. <span data-ttu-id="22491-290">Voordat u verdergaat, moet u controleren of de RCSU-status **Gelukt** is.</span><span class="sxs-lookup"><span data-stu-id="22491-290">Before you continue, make sure that the status of your RCSU is **Success**.</span></span> <span data-ttu-id="22491-291">Initialisatie duurt ongeveer twee tot vijf uur.</span><span class="sxs-lookup"><span data-stu-id="22491-291">Initialization takes approximately two to five hours.</span></span>

### <a name="initialize-e-commerce"></a><span data-ttu-id="22491-292">e-Commerce initialiseren</span><span class="sxs-lookup"><span data-stu-id="22491-292">Initialize e-Commerce</span></span>

<span data-ttu-id="22491-293">Ga als volgt te werk om e-Commerce te initialiseren.</span><span class="sxs-lookup"><span data-stu-id="22491-293">To initialize e-Commerce, follow these steps.</span></span>

1. <span data-ttu-id="22491-294">Controleer op het tabblad **e-Commerce (preview)** de toestemming voor de preview en selecteer vervolgens **Instellen**.</span><span class="sxs-lookup"><span data-stu-id="22491-294">On the **e-Commerce (Preview)** tab, review the preview consent, and then select **Setup**.</span></span>
1. <span data-ttu-id="22491-295">Voer een naam in bij **Tenantnaam e-Commerce**.</span><span class="sxs-lookup"><span data-stu-id="22491-295">In the **e-Commerce tenant name** field, enter a name.</span></span> <span data-ttu-id="22491-296">Houd er rekening mee dat deze naam wordt weergegeven in sommige URL's die naar uw e-Commerce-exemplaar verwijzen.</span><span class="sxs-lookup"><span data-stu-id="22491-296">However, be aware that this name will appear in some of the URLs that point to your e-Commerce instance.</span></span>
1. <span data-ttu-id="22491-297">Selecteer uw RCSU in de lijst in het veld **Naam Retail Cloud Scale Unit**.</span><span class="sxs-lookup"><span data-stu-id="22491-297">In the **Retail cloud scale unit name** field, select your RCSU in the list.</span></span> <span data-ttu-id="22491-298">(De lijst moet slechts één optie hebben.)</span><span class="sxs-lookup"><span data-stu-id="22491-298">(The list should have only one option.)</span></span>

    <span data-ttu-id="22491-299">Het veld **Geografie van e-Commerce** wordt automatisch ingevuld en kan niet worden gewijzigd.</span><span class="sxs-lookup"><span data-stu-id="22491-299">The **e-Commerce geography** field is set automatically, and the value can't be changed.</span></span>

1. <span data-ttu-id="22491-300">Selecteer **Volgende** om door te gaan.</span><span class="sxs-lookup"><span data-stu-id="22491-300">Select **Next** to continue.</span></span>
1. <span data-ttu-id="22491-301">Voer in het veld **Ondersteunde hostnamen** een geldig domein in, bijvoorbeeld `www.fabrikam.com`.</span><span class="sxs-lookup"><span data-stu-id="22491-301">In the **Supported host names** field, enter any valid domain, such as `www.fabrikam.com`.</span></span>
1.  <span data-ttu-id="22491-302">Voer in het veld **AAD-beveiligingsgroep voor systeembeheer** de eerste paar letters in van de naam van de beveiligingsgroep die u wilt gebruiken.</span><span class="sxs-lookup"><span data-stu-id="22491-302">In the **AAD security group for system admin** field, enter the first few letters of the name of the security group that you want to use.</span></span> <span data-ttu-id="22491-303">Selecteer het pictogram van het vergrootglas om de zoekresultaten weer te geven.</span><span class="sxs-lookup"><span data-stu-id="22491-303">Select the magnifying class icon to display the search results.</span></span> <span data-ttu-id="22491-304">Selecteer een beveiligingsgroep in de lijst.</span><span class="sxs-lookup"><span data-stu-id="22491-304">Select a security group from the list.</span></span>
2.  <span data-ttu-id="22491-305">Voer in het veld **AAD-beveiligingsgroep voor moderator van beoordelingen en recensies** de eerste paar letters in van de naam van de beveiligingsgroep die u wilt gebruiken.</span><span class="sxs-lookup"><span data-stu-id="22491-305">In the **AAD security group for ratings and review moderator** field, enter the first few letters of the name of the security group that you want to use.</span></span> <span data-ttu-id="22491-306">Selecteer het pictogram van het vergrootglas om de zoekresultaten weer te geven.</span><span class="sxs-lookup"><span data-stu-id="22491-306">Select the magnifying class icon to display the search results.</span></span> <span data-ttu-id="22491-307">Selecteer een beveiligingsgroep in de lijst.</span><span class="sxs-lookup"><span data-stu-id="22491-307">Select a security group from the list.</span></span>
1. <span data-ttu-id="22491-308">Laat **Service voor beoordelingen en recensies inschakelen** ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="22491-308">Leave the **Enable ratings and review service** option turned on.</span></span>
1. <span data-ttu-id="22491-309">Als u de stap voor toestemming van Microsoft Azure Active Directory (Azure AD) zoals beschreven in de sectie Toegang verlenen tot e-Commerce-toepassingen al hebt voltooid, schakelt u het selectievakje in om uw toestemming te bevestigen.</span><span class="sxs-lookup"><span data-stu-id="22491-309">If you have already completed the Microsoft Azure Active Directory (Azure AD) consent step as described in the "Grant access to e-Commerce applications" section, select the check box to confirm your consent.</span></span> <span data-ttu-id="22491-310">Als u deze stap nog niet hebt voltooid, moet u dat doen voordat u verdergaat met de initialisatie.</span><span class="sxs-lookup"><span data-stu-id="22491-310">If you have not yet completed this step, you need to do that before proceeding with the initialization.</span></span> <span data-ttu-id="22491-311">Selecteer de koppeling in de tekst naast het selectievakje om het dialoogvenster voor toestemming te openen en de stap te voltooien.</span><span class="sxs-lookup"><span data-stu-id="22491-311">Select the link within the text next to the check box to open the consent dialog box and complete the step.</span></span>
1. <span data-ttu-id="22491-312">Selecteer **Initialiseren**.</span><span class="sxs-lookup"><span data-stu-id="22491-312">Select **Initialize**.</span></span> <span data-ttu-id="22491-313">U keert terug naar de weergave **Beheer detailhandel** waarin het tabblad **e-Commerce (Preview)** is geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="22491-313">You're returned to the **Retail management** view, where the **e-Commerce (Preview)** tab is selected.</span></span> <span data-ttu-id="22491-314">De initialisatie van e-Commerce is gestart.</span><span class="sxs-lookup"><span data-stu-id="22491-314">E-Commerce initialization has started.</span></span>
1. <span data-ttu-id="22491-315">Voordat u verdergaat, moet u wachten tot de initialisatiestatus van e-Commerce **Geïnitieerd** is.</span><span class="sxs-lookup"><span data-stu-id="22491-315">Before you continue, wait until the status of e-Commerce initialization is **Initialization successful**.</span></span>
1. <span data-ttu-id="22491-316">Let onder **Koppeling** in de rechterbenedenhoek op de URL's voor de volgende koppelingen en noteer deze:</span><span class="sxs-lookup"><span data-stu-id="22491-316">Under **Links** in the lower right, make a note of the URLs for the following links:</span></span>

    * <span data-ttu-id="22491-317">**e-Commerce-site**: de koppeling naar de hoofdmap van uw e-Commerce-site.</span><span class="sxs-lookup"><span data-stu-id="22491-317">**e-Commerce site** – The link to the root of your e-Commerce site.</span></span>
    * <span data-ttu-id="22491-318">**Beheerhulpprogramma van de e-Commerce-site**: de koppeling naar het beheerhulpprogramma van de site.</span><span class="sxs-lookup"><span data-stu-id="22491-318">**e-Commerce site management tool** – The link to the site management tool.</span></span>

## <a name="commerce-preview-environment-support"></a><span data-ttu-id="22491-319">Ondersteuning voor preview-omgeving van Commerce</span><span class="sxs-lookup"><span data-stu-id="22491-319">Commerce preview environment support</span></span>

<span data-ttu-id="22491-320">Als u problemen ondervindt tijdens het uitvoeren van de inrichting, gaat u naar de [Microsoft Dynamics 365 Commerce Preview Yammer-groep](https://aka.ms/Dynamics365CommercePreviewYammer) voor hulp.</span><span class="sxs-lookup"><span data-stu-id="22491-320">If you experience issues while you're completing the provisioning steps, visit the [Microsoft Dynamics 365 Commerce Preview Yammer group](https://aka.ms/Dynamics365CommercePreviewYammer) for help.</span></span>

<span data-ttu-id="22491-321">Als u problemen ondervindt wanneer u probeert toegang te krijgen tot de Yammer-groep, kunt u per e-mail contact opnemen met Microsoft via <Dynamics365Commerce@microsoft.com>.</span><span class="sxs-lookup"><span data-stu-id="22491-321">If you experience issues when you try to access the Yammer group, you can contact Microsoft by email at <Dynamics365Commerce@microsoft.com>.</span></span> <span data-ttu-id="22491-322">Dit e-mailadres wordt niet actief gecontroleerd.</span><span class="sxs-lookup"><span data-stu-id="22491-322">This email address isn't actively monitored.</span></span> <span data-ttu-id="22491-323">Verwacht daarom een vertraging in het antwoord.</span><span class="sxs-lookup"><span data-stu-id="22491-323">Therefore, expect a delay in the response.</span></span>

## <a name="next-steps"></a><span data-ttu-id="22491-324">Volgende stappen</span><span class="sxs-lookup"><span data-stu-id="22491-324">Next steps</span></span>

<span data-ttu-id="22491-325">Zie [Een preview-omgeving van Commerce configureren](cpe-post-provisioning.md) om door te gaan met het inrichten en configureren van uw preview-omgeving voor Commerce.</span><span class="sxs-lookup"><span data-stu-id="22491-325">To continue the process of provisioning and configuring your Commerce preview environment, see [Configure a Commerce preview environment](cpe-post-provisioning.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="22491-326">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="22491-326">Additional resources</span></span>

[<span data-ttu-id="22491-327">Overzicht van Commerce preview-omgeving</span><span class="sxs-lookup"><span data-stu-id="22491-327">Commerce preview environment overview</span></span>](cpe-overview.md)

[<span data-ttu-id="22491-328">Een preview-omgeving van Commerce configureren</span><span class="sxs-lookup"><span data-stu-id="22491-328">Configure a Commerce preview environment</span></span>](cpe-post-provisioning.md)

[<span data-ttu-id="22491-329">Optionele functies voor een preview-omgeving van Commerce configureren</span><span class="sxs-lookup"><span data-stu-id="22491-329">Configure optional features for a Commerce preview environment</span></span>](cpe-optional-features.md)

[<span data-ttu-id="22491-330">Veelgestelde vragen over de preview-omgeving van Commerce</span><span class="sxs-lookup"><span data-stu-id="22491-330">Commerce preview environment FAQ</span></span>](cpe-faq.md)

[<span data-ttu-id="22491-331">Microsoft Lifecycle Services (LCS)</span><span class="sxs-lookup"><span data-stu-id="22491-331">Microsoft Lifecycle Services (LCS)</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[<span data-ttu-id="22491-332">Retail Cloud Scale Unit (RCSU)</span><span class="sxs-lookup"><span data-stu-id="22491-332">Retail Cloud Scale Unit (RCSU)</span></span>](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[<span data-ttu-id="22491-333">Microsoft Azure-portal</span><span class="sxs-lookup"><span data-stu-id="22491-333">Microsoft Azure portal</span></span>](https://azure.microsoft.com/features/azure-portal)

[<span data-ttu-id="22491-334">Dynamics 365 Commerce-website</span><span class="sxs-lookup"><span data-stu-id="22491-334">Dynamics 365 Commerce website</span></span>](https://aka.ms/Dynamics365CommerceWebsite)

[<span data-ttu-id="22491-335">Help-bronnen voor Dynamics 365 Retail</span><span class="sxs-lookup"><span data-stu-id="22491-335">Help resources for Dynamics 365 Retail</span></span>](../retail/index.md)
