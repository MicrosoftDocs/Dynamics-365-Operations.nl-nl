---
title: Een preview-omgeving inrichten voor Dynamics 365 Commerce
description: In dit onderwerp wordt uitgelegd hoe u een preview-omgeving van Microsoft Dynamics 365 Commerce inricht.
author: psimolin
manager: annbe
ms.date: 06/02/2020
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
ms.openlocfilehash: c109c2326cf01739255b49587c15aa34ad884f6a
ms.sourcegitcommit: be7e4378c8122c6e7cfc4e7991efbdffee45e006
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2020
ms.locfileid: "3426460"
---
# <a name="provision-a-dynamics-365-commerce-preview-environment"></a><span data-ttu-id="3ab50-103">Een preview-omgeving inrichten voor Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="3ab50-103">Provision a Dynamics 365 Commerce preview environment</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="3ab50-104">In dit onderwerp wordt uitgelegd hoe u een preview-omgeving voor Dynamics 365 Commerce inricht.</span><span class="sxs-lookup"><span data-stu-id="3ab50-104">This topic explains how to provision a Dynamics 365 Commerce preview environment.</span></span>

<span data-ttu-id="3ab50-105">Voordat u begint, kunt u het beste dit onderwerp snel doorlezen om een idee te krijgen van wat nodig is voor het proces.</span><span class="sxs-lookup"><span data-stu-id="3ab50-105">Before you begin, we recommend that you take a quick scan through this topic to get an idea of what the process requires.</span></span>

> [!NOTE]
> <span data-ttu-id="3ab50-106">Als u nog geen toegang hebt gekregen tot de preview van Dynamics 365 Commerce, kunt u toegang tot de preview-versie aanvragen via de [website van Dynamics 365 Commerce](https://aka.ms/Dynamics365CommerceWebsite).</span><span class="sxs-lookup"><span data-stu-id="3ab50-106">If you haven't yet been granted access to the Dynamics 365 Commerce preview, you can request preview access from the [Dynamics 365 Commerce website](https://aka.ms/Dynamics365CommerceWebsite).</span></span>

## <a name="overview"></a><span data-ttu-id="3ab50-107">Overzicht</span><span class="sxs-lookup"><span data-stu-id="3ab50-107">Overview</span></span>

<span data-ttu-id="3ab50-108">Als u uw preview-omgeving van Commerce wilt inrichten, moet u een project maken met een specifieke productnaam en een specifiek producttype.</span><span class="sxs-lookup"><span data-stu-id="3ab50-108">To successfully provision your Commerce preview environment, you must create a project that has a specific product name and type.</span></span> <span data-ttu-id="3ab50-109">De omgeving en Commerce Scale Unit (CSU) beschikken ook over specifieke parameters die u moet gebruiken wanneer u e-Commerce later inricht.</span><span class="sxs-lookup"><span data-stu-id="3ab50-109">The environment and Commerce Scale Unit (CSU) also have some specific parameters that you must use when you provision e-Commerce later.</span></span> <span data-ttu-id="3ab50-110">De instructies in dit onderwerp beschrijven alle vereiste stappen voor het voltooien van de inrichting en de parameters die u moet gebruiken.</span><span class="sxs-lookup"><span data-stu-id="3ab50-110">The instructions in this topic describe all the steps required to complete provisioning and the parameters that you must use.</span></span>

<span data-ttu-id="3ab50-111">Nadat de inrichting van de preview-omgeving van Commerce is voltooid, moet u een aantal stappen uitvoeren om de preview-omgeving voor te bereiden.</span><span class="sxs-lookup"><span data-stu-id="3ab50-111">After you successfully provision your Commerce preview environment, you must complete a few post-provisioning steps to prepare it.</span></span> <span data-ttu-id="3ab50-112">Sommige stappen zijn optioneel, afhankelijk van de aspecten van het systeem die u wilt evalueren.</span><span class="sxs-lookup"><span data-stu-id="3ab50-112">Some steps are optional, depending on the aspects of the system that you want to evaluate.</span></span> <span data-ttu-id="3ab50-113">U kunt de optionele stappen altijd later voltooien.</span><span class="sxs-lookup"><span data-stu-id="3ab50-113">You can always complete the optional steps later.</span></span>

<span data-ttu-id="3ab50-114">Zie [Een preview-omgeving van Commerce configureren](cpe-post-provisioning.md) voor meer informatie over hoe u uw preview-omgeving voor Commerce configureert nadat u deze hebt ingericht.</span><span class="sxs-lookup"><span data-stu-id="3ab50-114">For information about how to configure your Commerce preview environment after you provision it, see [Configure a Commerce preview environment](cpe-post-provisioning.md).</span></span> <span data-ttu-id="3ab50-115">Zie [Optionele functies voor een preview-omgeving van Commerce configureren](cpe-optional-features.md) voor meer informatie over hoe u optionele functies voor uw preview-omgeving van Commerce configureert.</span><span class="sxs-lookup"><span data-stu-id="3ab50-115">For information about how to configure optional features for your Commerce preview environment, see [Configure optional features for a Commerce preview environment](cpe-optional-features.md).</span></span>

<span data-ttu-id="3ab50-116">Als u vragen hebt over de inrichtingsstappen of als u problemen ondervindt, laat het Microsoft dan weten in de [Microsoft Dynamics 365 Commerce Preview Yammer-groep](https://aka.ms/Dynamics365CommercePreviewYammer).</span><span class="sxs-lookup"><span data-stu-id="3ab50-116">If you have any questions about the provisioning steps, or if you encounter any issues, let Microsoft know in the [Microsoft Dynamics 365 Commerce Preview Yammer group](https://aka.ms/Dynamics365CommercePreviewYammer).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="3ab50-117">Vereisten</span><span class="sxs-lookup"><span data-stu-id="3ab50-117">Prerequisites</span></span>

<span data-ttu-id="3ab50-118">Aan de volgende voorwaarden moeten zijn voldaan voordat u uw preview-omgeving van Commerce inricht:</span><span class="sxs-lookup"><span data-stu-id="3ab50-118">The following prerequisites must be in place before you can provision your Commerce preview environment:</span></span>

- <span data-ttu-id="3ab50-119">U hebt toegang tot de Microsoft Dynamics Lifecycle Services-portal (LCS).</span><span class="sxs-lookup"><span data-stu-id="3ab50-119">You have access to the Microsoft Dynamics Lifecycle Services (LCS) portal.</span></span>
- <span data-ttu-id="3ab50-120">U bent een bestaande Microsoft Dynamics 365-partner of -klant en kunt een Dynamics 365 Commerce-project maken.</span><span class="sxs-lookup"><span data-stu-id="3ab50-120">You are an existing Microsoft Dynamics 365 partner or customer and are able to create a Dynamics 365 Commerce project.</span></span>
- <span data-ttu-id="3ab50-121">U bent geaccepteerd voor het Dynamics 365 Commerce Preview-programma.</span><span class="sxs-lookup"><span data-stu-id="3ab50-121">You've been accepted into the Dynamics 365 Commerce Preview program.</span></span>
- <span data-ttu-id="3ab50-122">U hebt de vereiste machtigingen om een project te maken voor **Migreren, oplossingen maken en informatie over**.</span><span class="sxs-lookup"><span data-stu-id="3ab50-122">You have the required permissions to create a project for **Migrate, create solutions, and learn**.</span></span>
- <span data-ttu-id="3ab50-123">U bent lid van de rol **Omgevingsbeheerder** of **Projecteigenaar** in het project waar u de omgeving gaat inrichten.</span><span class="sxs-lookup"><span data-stu-id="3ab50-123">You're a member of the **Environment manager** or **Project owner** role in the project where you will provision the environment.</span></span>
- <span data-ttu-id="3ab50-124">U hebt beheerderstoegang tot uw Microsoft Azure-abonnement of contact met een abonnementsbeheerder die de twee stappen kan uitvoeren waarvoor beheerdersmachtigingen namens u nodig zijn.</span><span class="sxs-lookup"><span data-stu-id="3ab50-124">You have admin access to your Microsoft Azure subscription, or you're in contact with a subscription admin who can complete the two steps that require admin permissions on your behalf.</span></span>
- <span data-ttu-id="3ab50-125">U hebt uw Azure Active Directory-tenant-id (Azure AD) bij de hand.</span><span class="sxs-lookup"><span data-stu-id="3ab50-125">You have your Azure Active Directory (Azure AD) tenant ID available.</span></span>
- <span data-ttu-id="3ab50-126">U hebt een Azure AD-beveiligingsgroep gemaakt om te gebruiken als e-Commerce-systeembeheerdersgroep en u hebt de id bij de hand.</span><span class="sxs-lookup"><span data-stu-id="3ab50-126">You've created an Azure AD security group that can be used as an e-Commerce system admin group, and you have its ID available.</span></span>
- <span data-ttu-id="3ab50-127">U hebt een Azure AD-beveiligingsgroep gemaakt om te gebruiken als moderatorgroep voor beoordelingen en recensies en u hebt de id bij de hand.</span><span class="sxs-lookup"><span data-stu-id="3ab50-127">You've created an Azure AD security group that can be used as a Ratings and Reviews moderator group, and you have its ID available.</span></span> <span data-ttu-id="3ab50-128">(Deze beveiligingsgroep kan dezelfde zijn als de systeembeheerdersgroep van e-Commerce.)</span><span class="sxs-lookup"><span data-stu-id="3ab50-128">(This security group can be the same as the e-Commerce system admin group.)</span></span>

## <a name="provision-your-commerce-preview-environment"></a><span data-ttu-id="3ab50-129">Uw preview-omgeving van Commerce inrichten</span><span class="sxs-lookup"><span data-stu-id="3ab50-129">Provision your Commerce preview environment</span></span>

<span data-ttu-id="3ab50-130">In deze procedures wordt uitgelegd hoe u een preview-omgeving van Commerce inricht.</span><span class="sxs-lookup"><span data-stu-id="3ab50-130">These procedures explain how to provision a Commerce preview environment.</span></span> <span data-ttu-id="3ab50-131">Als u dit hebt gedaan, is de preview-omgeving van Commerce gereed voor configuratie.</span><span class="sxs-lookup"><span data-stu-id="3ab50-131">After you successfully complete them, the Commerce preview environment will be ready for configuration.</span></span> <span data-ttu-id="3ab50-132">Alle activiteiten die hier worden beschreven, vinden plaats in de LCS-portal.</span><span class="sxs-lookup"><span data-stu-id="3ab50-132">All the activities that are described here occur in the LCS portal.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="3ab50-133">Preview-toegang is gekoppeld aan de LCS-account en organisatie die u hebt opgegeven in uw Commerce preview-toepassing.</span><span class="sxs-lookup"><span data-stu-id="3ab50-133">Preview access is tied to the LCS account and organization that you specified in your Commerce preview application.</span></span> <span data-ttu-id="3ab50-134">U moet dezelfde account gebruiken om de preview-omgeving van Commerce in te richten.</span><span class="sxs-lookup"><span data-stu-id="3ab50-134">You must use the same account to provision the Commerce preview environment.</span></span> <span data-ttu-id="3ab50-135">Als u een andere LCS-account of tenant voor de preview-omgeving van Commerce moet gebruiken, moet u deze gegevens aan Microsoft verstrekken.</span><span class="sxs-lookup"><span data-stu-id="3ab50-135">If you need to use a different LCS account or tenant for the Commerce preview environment, you must provide those details to Microsoft.</span></span> <span data-ttu-id="3ab50-136">Zie de sectie [Ondersteuning voor preview-omgeving van Commerce](#commerce-preview-environment-support) verderop in dit onderwerp voor contactgegevens.</span><span class="sxs-lookup"><span data-stu-id="3ab50-136">For contact information, see the [Commerce preview environment support](#commerce-preview-environment-support) section later in this topic.</span></span>

### <a name="confirm-that-preview-features-are-available-and-turned-on-in-lcs"></a><span data-ttu-id="3ab50-137">Controleren of de preview-functies beschikbaar zijn en zijn ingeschakeld in LCS</span><span class="sxs-lookup"><span data-stu-id="3ab50-137">Confirm that preview features are available and turned on in LCS</span></span>

<span data-ttu-id="3ab50-138">Ga als volgt te werk om te controleren of de preview-functies beschikbaar zijn en zijn ingeschakeld in LCS.</span><span class="sxs-lookup"><span data-stu-id="3ab50-138">To confirm that preview features are available and turned on in LCS, follow these steps.</span></span>

1. <span data-ttu-id="3ab50-139">Meld u aan bij de [LCS-portal](https://lcs.dynamics.com) met dezelfde LCS-account die u hebt gebruikt om toegang tot de preview aan te vragen.</span><span class="sxs-lookup"><span data-stu-id="3ab50-139">Sign in to the [LCS portal](https://lcs.dynamics.com) by using the same LCS account that you used to request access to the preview.</span></span>
1. <span data-ttu-id="3ab50-140">Schuif op de LCS-startpagina helemaal naar rechts en selecteer de tegel **Beheer van voorbeeldfuncties**.</span><span class="sxs-lookup"><span data-stu-id="3ab50-140">On the LCS home page, scroll all the way to the right, and select the **Preview feature management** tile.</span></span>

    ![Tegel Beheer van voorbeeldfuncties](./media/preview1.png)

1. <span data-ttu-id="3ab50-142">Schuif omlaag naar **Particuliere voorbeeldfuncties** en controleer of de volgende functies beschikbaar en ingeschakeld zijn:</span><span class="sxs-lookup"><span data-stu-id="3ab50-142">Scroll down to **Private preview features**, and confirm that the following features are available and turned on:</span></span>

    - <span data-ttu-id="3ab50-143">Evaluatie van e-Commerce</span><span class="sxs-lookup"><span data-stu-id="3ab50-143">e-Commerce Evaluation</span></span>
    - <span data-ttu-id="3ab50-144">Programma-omgevingen voor Commerce Preview</span><span class="sxs-lookup"><span data-stu-id="3ab50-144">Commerce Preview Program Environments</span></span>

    ![Particuliere voorbeeldfuncties](./media/preview2.png)

1. <span data-ttu-id="3ab50-146">Als deze functies niet worden weergegeven in de lijst, neemt u contact op met Microsoft en geef u uw zakelijke e-mailadres, LCS-account en tenantgegevens op.</span><span class="sxs-lookup"><span data-stu-id="3ab50-146">If those features don't appear in the list, contact Microsoft, and provide your work email address, LCS account, and tenant details.</span></span> <span data-ttu-id="3ab50-147">Zie de sectie [Ondersteuning voor preview-omgeving van Commerce](#commerce-preview-environment-support) voor contactgegevens.</span><span class="sxs-lookup"><span data-stu-id="3ab50-147">For contact information, see the [Commerce preview environment support](#commerce-preview-environment-support) section.</span></span>

### <a name="create-a-new-project"></a><span data-ttu-id="3ab50-148">Een nieuw project maken</span><span class="sxs-lookup"><span data-stu-id="3ab50-148">Create a new project</span></span>

<span data-ttu-id="3ab50-149">Ga als volgt te werk om een nieuw project te maken in LCS.</span><span class="sxs-lookup"><span data-stu-id="3ab50-149">To create a new project in LCS, follow these steps.</span></span>

1. <span data-ttu-id="3ab50-150">Selecteer op de LCS-startpagina het plusteken (**+**) om een project te maken.</span><span class="sxs-lookup"><span data-stu-id="3ab50-150">On the LCS home page, select the plus sign (**+**) to create a project.</span></span>
1. <span data-ttu-id="3ab50-151">Volg een van de volgende stappen uit in het rechterdeelvenster:</span><span class="sxs-lookup"><span data-stu-id="3ab50-151">In the right pane, follow one of these steps:</span></span>

    - <span data-ttu-id="3ab50-152">Als u een partner bent, selecteert u **Migreren, oplossingen maken en informatie over**.</span><span class="sxs-lookup"><span data-stu-id="3ab50-152">If you're a partner, select **Migrate, create solutions, and learn**.</span></span>
    - <span data-ttu-id="3ab50-153">Als u een klant bent, selecteert u **Potentiële presales**.</span><span class="sxs-lookup"><span data-stu-id="3ab50-153">If you're a customer, select **Prospective presales**.</span></span>

1. <span data-ttu-id="3ab50-154">Voer een naam, beschrijving en branche in.</span><span class="sxs-lookup"><span data-stu-id="3ab50-154">Enter a name, description, and industry.</span></span>
1. <span data-ttu-id="3ab50-155">Selecteer **Dynamics 365 Retail** in het veld **Productnaam**.</span><span class="sxs-lookup"><span data-stu-id="3ab50-155">In the **Product name** field, select **Dynamics 365 Retail**.</span></span>
1. <span data-ttu-id="3ab50-156">Selecteer **Dynamics 365 Retail** in het veld **Productversie**.</span><span class="sxs-lookup"><span data-stu-id="3ab50-156">In the **Product version** field, select **Dynamics 365 Retail**.</span></span>
1. <span data-ttu-id="3ab50-157">Selecteer **Implementatiemethodologie voor Dynamics Retail** in het veld **Methodologie**.</span><span class="sxs-lookup"><span data-stu-id="3ab50-157">In the **Methodology** field, select **Dynamics Retail implementation methodology**.</span></span>
1. <span data-ttu-id="3ab50-158">Optioneel: u kunt rollen en gebruikers importeren uit bestaand project.</span><span class="sxs-lookup"><span data-stu-id="3ab50-158">Optional: You can import roles and users from an existing project.</span></span>
1. <span data-ttu-id="3ab50-159">Selecteer **Maken**.</span><span class="sxs-lookup"><span data-stu-id="3ab50-159">Select **Create**.</span></span> <span data-ttu-id="3ab50-160">De projectweergave wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="3ab50-160">The project view appears.</span></span>

### <a name="add-the-azure-connector"></a><span data-ttu-id="3ab50-161">De Azure-connector toevoegen</span><span class="sxs-lookup"><span data-stu-id="3ab50-161">Add the Azure Connector</span></span>

<span data-ttu-id="3ab50-162">Ga als volgt te werk om de Azure-connector toe te voegen aan uw LCS-project.</span><span class="sxs-lookup"><span data-stu-id="3ab50-162">To add the Azure Connector to your LCS project, follow these steps.</span></span>

1. <span data-ttu-id="3ab50-163">Volg één van deze stappen:</span><span class="sxs-lookup"><span data-stu-id="3ab50-163">Follow one of these steps:</span></span>

    - <span data-ttu-id="3ab50-164">Als u een partner bent, selecteert u de tegel **Projectinstellingen** uiterst rechts.</span><span class="sxs-lookup"><span data-stu-id="3ab50-164">If you're a partner, select the **Project settings** tile on the far right.</span></span>
    - <span data-ttu-id="3ab50-165">Als u een klant bent, selecteert u **Projectinstellingen** in het bovenste menu.</span><span class="sxs-lookup"><span data-stu-id="3ab50-165">If you're a customer, select **Project settings** on the top menu.</span></span>

1. <span data-ttu-id="3ab50-166">Selecteer **Azure-connectors**.</span><span class="sxs-lookup"><span data-stu-id="3ab50-166">Select **Azure connectors**.</span></span>
1. <span data-ttu-id="3ab50-167">Selecteer **Toevoegen** om de Azure-connector toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="3ab50-167">Select **Add** to add the Azure Connector.</span></span>
1. <span data-ttu-id="3ab50-168">Voer een naam in.</span><span class="sxs-lookup"><span data-stu-id="3ab50-168">Enter a name.</span></span>
1. <span data-ttu-id="3ab50-169">Voer uw Azure-abonnements-id in.</span><span class="sxs-lookup"><span data-stu-id="3ab50-169">Enter your Azure subscription ID.</span></span>
1. <span data-ttu-id="3ab50-170">Schakel de optie **Configureren om Azure Resource Manager (ARM) te gebruiken** in.</span><span class="sxs-lookup"><span data-stu-id="3ab50-170">Turn on the **Configure to use Azure Resource Manager (ARM)** option.</span></span>
1. <span data-ttu-id="3ab50-171">Controleer of de waarde **Azure-abonnement AAD-tenantdomein (of id)** juist is.</span><span class="sxs-lookup"><span data-stu-id="3ab50-171">Verify that the **Azure subscription AAD Tenant Domain (or ID)** value is correct.</span></span> <span data-ttu-id="3ab50-172">Neem zo nodig contact op met uw Azure-abonnementsbeheerder.</span><span class="sxs-lookup"><span data-stu-id="3ab50-172">Consult your Azure subscription admin as required.</span></span>
1. <span data-ttu-id="3ab50-173">Selecteer **Volgende**.</span><span class="sxs-lookup"><span data-stu-id="3ab50-173">Select **Next**.</span></span>
1. <span data-ttu-id="3ab50-174">Volg de instructies op de pagina om de vereiste toepassingen toegang te verlenen tot uw abonnement.</span><span class="sxs-lookup"><span data-stu-id="3ab50-174">Follow the instructions on the page to grant the required applications access to your subscription.</span></span> <span data-ttu-id="3ab50-175">Neem zo nodig contact op met uw Azure-abonnementsbeheerder.</span><span class="sxs-lookup"><span data-stu-id="3ab50-175">Consult your Azure subscription admin as required.</span></span>

    1. <span data-ttu-id="3ab50-176">Meld u aan bij de [Azure-portal](https://portal.azure.com/).</span><span class="sxs-lookup"><span data-stu-id="3ab50-176">Sign in to the [Azure portal](https://portal.azure.com/).</span></span>
    1. <span data-ttu-id="3ab50-177">Zorg ervoor dat de juiste map is geselecteerd en selecteer vervolgens in het menu aan de linkerkant **Abonnementen**.</span><span class="sxs-lookup"><span data-stu-id="3ab50-177">Make sure that the correct directory is selected, and then, on the menu on the left, select **Subscriptions**.</span></span>
    1. <span data-ttu-id="3ab50-178">Zoek het juiste abonnement in de lijst en selecteer dit.</span><span class="sxs-lookup"><span data-stu-id="3ab50-178">Find the correct subscription in the list, and select it.</span></span> <span data-ttu-id="3ab50-179">Gebruik de zoekfunctie zoals vereist.</span><span class="sxs-lookup"><span data-stu-id="3ab50-179">Use the search functionality as required.</span></span>
    1. <span data-ttu-id="3ab50-180">Selecteer **Toegangscontrole (IAM)** in het menu.</span><span class="sxs-lookup"><span data-stu-id="3ab50-180">On the menu, select **Access control (IAM)**.</span></span>
    1. <span data-ttu-id="3ab50-181">Selecteer **Toevoegen** rechts onder **Een roltoewijzing toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="3ab50-181">On the right, under **Add a role assignment**, select **Add**.</span></span> <span data-ttu-id="3ab50-182">Het deelvenster **Roltoewijzing toevoegen** wordt geopend.</span><span class="sxs-lookup"><span data-stu-id="3ab50-182">The **Add role assignment** pane appears.</span></span>
    1. <span data-ttu-id="3ab50-183">Selecteer in het veld **Rol** de waarde **Bijdrager**.</span><span class="sxs-lookup"><span data-stu-id="3ab50-183">In the **Role** field, select **Contributor**.</span></span>
    1. <span data-ttu-id="3ab50-184">Laat in het veld **Toegang toewijzen aan** de standaardwaarde **Azure AD-gebruiker, -groep of serviceprincipal** ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="3ab50-184">In the **Assign access to** field, leave the default value, **Azure AD user, group, or service principal**.</span></span>
    1. <span data-ttu-id="3ab50-185">Klik onder **Selecteren** op **b96b7e94-b82e-4e71-99a0-cf7fb188acea**.</span><span class="sxs-lookup"><span data-stu-id="3ab50-185">Under **Select**, enter **b96b7e94-b82e-4e71-99a0-cf7fb188acea**.</span></span>
    1. <span data-ttu-id="3ab50-186">Selecteer **Dynamics Deployment Services \[wsfed-enabled\]** in de lijst.</span><span class="sxs-lookup"><span data-stu-id="3ab50-186">Select **Dynamics Deployment Services \[wsfed-enabled\]** in the list.</span></span>
    1. <span data-ttu-id="3ab50-187">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="3ab50-187">Select **Save**.</span></span>

1. <span data-ttu-id="3ab50-188">Selecteer **Volgende**.</span><span class="sxs-lookup"><span data-stu-id="3ab50-188">Select **Next**.</span></span>
1. <span data-ttu-id="3ab50-189">Volg de instructies op de pagina om de vereiste toepassingen toegang te verlenen tot uw abonnement.</span><span class="sxs-lookup"><span data-stu-id="3ab50-189">Follow the instructions on the page to grant the required applications access to your subscription.</span></span> <span data-ttu-id="3ab50-190">Neem zo nodig contact op met uw Azure-abonnementsbeheerder.</span><span class="sxs-lookup"><span data-stu-id="3ab50-190">Consult your Azure subscription admin as required.</span></span>
1. <span data-ttu-id="3ab50-191">Selecteer **Volgende**.</span><span class="sxs-lookup"><span data-stu-id="3ab50-191">Select **Next**.</span></span>
1. <span data-ttu-id="3ab50-192">Kies voor **Azure-regio** de optie **VS - oost**, **VS - oost 2**, **VS - west** of **VS - west 2**.</span><span class="sxs-lookup"><span data-stu-id="3ab50-192">In the **Azure region** field, select **East US**, **East US 2**, **West US**, or **West US 2**.</span></span>
1. <span data-ttu-id="3ab50-193">Selecteer **Verbinding maken**.</span><span class="sxs-lookup"><span data-stu-id="3ab50-193">Select **Connect**.</span></span> <span data-ttu-id="3ab50-194">De Azure-connector wordt weergegeven in de lijst.</span><span class="sxs-lookup"><span data-stu-id="3ab50-194">Your Azure Connector should appear in the list.</span></span>

### <a name="import-the-commerce-preview-demo-base-extension"></a><span data-ttu-id="3ab50-195">Extensie voor demobasis van Commerce-preview importeren</span><span class="sxs-lookup"><span data-stu-id="3ab50-195">Import the Commerce Preview Demo Base Extension</span></span>

<span data-ttu-id="3ab50-196">Voer de volgende stappen uit om de extensie voor de demobasis van de Commerce-preview in uw project te importeren.</span><span class="sxs-lookup"><span data-stu-id="3ab50-196">To import the Commerce Preview Demo Base Extension into your project, follow these steps.</span></span>

1. <span data-ttu-id="3ab50-197">Open de startpagina voor uw project door de projectnaam bovenaan te selecteren.</span><span class="sxs-lookup"><span data-stu-id="3ab50-197">Open the home page for your project by selecting the project name at the top.</span></span>
1. <span data-ttu-id="3ab50-198">Volg één van deze stappen:</span><span class="sxs-lookup"><span data-stu-id="3ab50-198">Follow one of these steps:</span></span>

    - <span data-ttu-id="3ab50-199">Als u een partner bent, selecteert u de tegel **Activabibliotheek** uiterst rechts.</span><span class="sxs-lookup"><span data-stu-id="3ab50-199">If you're a partner, select the **Asset library** tile on the far right.</span></span>
    - <span data-ttu-id="3ab50-200">Als u een klant bent, selecteert u **Activabibliotheek** in het bovenste menu.</span><span class="sxs-lookup"><span data-stu-id="3ab50-200">If you're a customer, select **Asset library** on the top menu.</span></span>

1. <span data-ttu-id="3ab50-201">Selecteer **Implementeerbaar softwarepakket** in de lijst aan de linkerkant.</span><span class="sxs-lookup"><span data-stu-id="3ab50-201">In the list on the left, select **Software deployable package**.</span></span>
1. <span data-ttu-id="3ab50-202">Selecteer **Importeren**.</span><span class="sxs-lookup"><span data-stu-id="3ab50-202">Select **Import**.</span></span>
1. <span data-ttu-id="3ab50-203">Selecteer **Extensie voor Commerce Preview-demobasis** in de lijst met activa onder **Bibliotheek voor gedeelde activa**.</span><span class="sxs-lookup"><span data-stu-id="3ab50-203">Under **Shared asset library**, select **Commerce Preview Demo Base Extension** in the list of assets.</span></span>
1. <span data-ttu-id="3ab50-204">Selecteer **Verzamelen**.</span><span class="sxs-lookup"><span data-stu-id="3ab50-204">Select **Pick**.</span></span> <span data-ttu-id="3ab50-205">U keert terug naar de activabibliotheek en de extensie wordt weergegeven in de lijst.</span><span class="sxs-lookup"><span data-stu-id="3ab50-205">You're returned to the Asset library, and you should see the extension in the list.</span></span>

<span data-ttu-id="3ab50-206">In de volgende afbeelding ziet u de acties die moeten worden ondernomen op de LCS-pagina **Activabibliotheek**.</span><span class="sxs-lookup"><span data-stu-id="3ab50-206">The following illustration shows the actions that must be taken on the LCS **Asset library** page.</span></span>

![De extensie voor de demobasis van de Commerce-preview importeren](./media/import.png)

### <a name="deploy-the-environment"></a><span data-ttu-id="3ab50-208">De omgeving implementeren</span><span class="sxs-lookup"><span data-stu-id="3ab50-208">Deploy the environment</span></span>

<span data-ttu-id="3ab50-209">Ga als volgt te werk om de omgeving te implementeren.</span><span class="sxs-lookup"><span data-stu-id="3ab50-209">To deploy the environment, follow these steps.</span></span>

> [!NOTE]
> <span data-ttu-id="3ab50-210">Het is mogelijk dat u de stappen 6, 7 en/of 8 niet hoeft te voltooien, omdat pagina's met één optie worden overgeslagen.</span><span class="sxs-lookup"><span data-stu-id="3ab50-210">You might not have to complete steps 6, 7, and/or 8, because pages that have a single option are skipped.</span></span> <span data-ttu-id="3ab50-211">Controleer in de weergave **Omgevingsparameters** of u de tekst **Dynamics 365 Commerce - Demo (10.0.* x* met Platform update *xx*)\*\* direct boven het veld **Omgevingsnaam** ziet.</span><span class="sxs-lookup"><span data-stu-id="3ab50-211">When you're in the **Environment parameters** view, confirm that the text **Dynamics 365 Commerce - Demo (10.0.* x* with Platform update *xx*)\*\* appears directly above the **Environment name** field.</span></span> <span data-ttu-id="3ab50-212">Zie de afbeelding die na stap 8 wordt weergegeven voor nadere details.</span><span class="sxs-lookup"><span data-stu-id="3ab50-212">For details, see the illustration that appears after step 8.</span></span>

1. <span data-ttu-id="3ab50-213">Selecteer in het bovenste menu de optie **Cloudomgevingen**.</span><span class="sxs-lookup"><span data-stu-id="3ab50-213">On the top menu, select **Cloud-hosted environments**.</span></span>
1. <span data-ttu-id="3ab50-214">Selecteer **Toevoegen** om een omgeving toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="3ab50-214">Select **Add** to add an environment.</span></span>
1. <span data-ttu-id="3ab50-215">Selecteer in het veld **Toepassingsversie** de meest recente versie.</span><span class="sxs-lookup"><span data-stu-id="3ab50-215">In the **Application version** field, select the most current version.</span></span> <span data-ttu-id="3ab50-216">Als u specifiek een andere toepassingsversie dan de meest recente versie wilt selecteren, moet u geen eerdere versie dan **10.0.8** selecteren.</span><span class="sxs-lookup"><span data-stu-id="3ab50-216">If you have a specific need to select an application version other than the most current version, do not select a version prior to **10.0.8**.</span></span>
1. <span data-ttu-id="3ab50-217">Gebruik in het veld **Platformversie** de platform versie die automatisch wordt gekozen voor de toepassingsversie die u hebt geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="3ab50-217">In the **Platform version** field, use the platform version that is automatically chosen for the application version you selected.</span></span> 

    ![Toepassings- en platformversies selecteren](./media/project1.png)

1. <span data-ttu-id="3ab50-219">Selecteer **Volgende**.</span><span class="sxs-lookup"><span data-stu-id="3ab50-219">Select **Next**.</span></span>
1. <span data-ttu-id="3ab50-220">Selecteer **Demo** als de omgevingstopologie.</span><span class="sxs-lookup"><span data-stu-id="3ab50-220">Select **Demo** as the environment topology.</span></span>

    ![De omgevingstopologie 1 selecteren](./media/project2.png)

1. <span data-ttu-id="3ab50-222">Selecteer **Dynamics 365 Commerce - Demo** als de omgevingstopologie.</span><span class="sxs-lookup"><span data-stu-id="3ab50-222">Select **Dynamics 365 Commerce - Demo** as the environment topology.</span></span> <span data-ttu-id="3ab50-223">Als u één Azure-connector eerder hebt geconfigureerd, wordt deze gebruikt voor deze omgeving.</span><span class="sxs-lookup"><span data-stu-id="3ab50-223">If you configured a single Azure Connector earlier, it will be used for this environment.</span></span> <span data-ttu-id="3ab50-224">Als u meerdere Azure-connectors hebt geconfigureerd, kunt u kiezen welke connector u wilt gebruiken: **VS - oost**, **VS - oost 2**, **VS - west**, **VS - west 2**.</span><span class="sxs-lookup"><span data-stu-id="3ab50-224">If you configured multiple Azure Connectors, you can select which connector to use: **East US**, **East US 2**, **West US**, or **West US 2**.</span></span> <span data-ttu-id="3ab50-225">(Voor de beste end-to-end-prestaties raden we aan **VS - west 2** te selecteren.)</span><span class="sxs-lookup"><span data-stu-id="3ab50-225">(For the best end-to-end performance, we recommend that you select **West US 2**.)</span></span>

    ![De omgevingstopologie 2 selecteren](./media/project3.png)

1. <span data-ttu-id="3ab50-227">Voer op de pagina **Omgeving implementeren** een omgevingsnaam in.</span><span class="sxs-lookup"><span data-stu-id="3ab50-227">On the **Deploy environment** page, enter an environment name.</span></span> <span data-ttu-id="3ab50-228">Laat geavanceerde instellingen ongewijzigd.</span><span class="sxs-lookup"><span data-stu-id="3ab50-228">Leave the advanced settings as they are.</span></span>

    ![De pagina Omgeving implementeren](./media/project4.png)

1. <span data-ttu-id="3ab50-230">Pas de VM-grootte naar wens aan.</span><span class="sxs-lookup"><span data-stu-id="3ab50-230">Adjust the VM size as required.</span></span> <span data-ttu-id="3ab50-231">(We raden VM-voorraadeenheid \[SKU\] **D13 v2** aan.)</span><span class="sxs-lookup"><span data-stu-id="3ab50-231">(We recommend VM stock keeping unit \[SKU\] **D13 v2**.)</span></span>
1. <span data-ttu-id="3ab50-232">Controleer de prijs- en licentievoorwaarden en schakel vervolgens het selectievakje in om aan te geven dat u ermee instemt.</span><span class="sxs-lookup"><span data-stu-id="3ab50-232">Review the pricing and licensing terms, and then select the check box to indicate that you agree to them.</span></span>
1. <span data-ttu-id="3ab50-233">Selecteer **Volgende**.</span><span class="sxs-lookup"><span data-stu-id="3ab50-233">Select **Next**.</span></span>
1. <span data-ttu-id="3ab50-234">Controleer op de bevestigingspagina voor de implementatie of de details juist zijn en klik op **Implementeren**.</span><span class="sxs-lookup"><span data-stu-id="3ab50-234">On the deployment confirmation page, verify that the details are correct, and then select **Deploy**.</span></span> <span data-ttu-id="3ab50-235">U keert terug naar de weergave in **Cloudomgevingen** en uw omgeving wordt weergegeven in de lijst.</span><span class="sxs-lookup"><span data-stu-id="3ab50-235">You're returned to the **Cloud-hosted environments** view, and your environment should appear in the list.</span></span>

    <span data-ttu-id="3ab50-236">Uw aangevraagde omgeving wordt weergegeven in de wachtrij en vervolgens geïmplementeerd.</span><span class="sxs-lookup"><span data-stu-id="3ab50-236">Your requested environment will appear as queued and then deploying.</span></span> <span data-ttu-id="3ab50-237">Het duurt even voordat de werkstromen van de omgeving zijn voltooid.</span><span class="sxs-lookup"><span data-stu-id="3ab50-237">The environment workflows will take some time to be completed.</span></span> <span data-ttu-id="3ab50-238">Controleer dit daarom na ongeveer zes tot negen uur.</span><span class="sxs-lookup"><span data-stu-id="3ab50-238">Therefore, check back after approximately six to nine hours.</span></span>

1. <span data-ttu-id="3ab50-239">Voordat u verdergaat, moet u controleren of de omgevingsstatus **Geïmplementeerd** is.</span><span class="sxs-lookup"><span data-stu-id="3ab50-239">Before you continue, make sure that the status of your environment is **Deployed**.</span></span>

### <a name="initialize-the-commerce-scale-unit-cloud"></a><span data-ttu-id="3ab50-240">Commerce Scale Unit initialiseren (cloud)</span><span class="sxs-lookup"><span data-stu-id="3ab50-240">Initialize the Commerce Scale Unit (cloud)</span></span>

<span data-ttu-id="3ab50-241">Ga als volgt te werk om CSU te initialiseren.</span><span class="sxs-lookup"><span data-stu-id="3ab50-241">To initialize CSU, follow these steps.</span></span>

1. <span data-ttu-id="3ab50-242">Selecteer in de weergave **Cloudomgevingen** uw omgeving in de lijst.</span><span class="sxs-lookup"><span data-stu-id="3ab50-242">In the **Cloud-hosted environments** view, select your environment in the list.</span></span>
1. <span data-ttu-id="3ab50-243">Klik op **Volledige details** in de omgevingsweergave rechts.</span><span class="sxs-lookup"><span data-stu-id="3ab50-243">In the environment view on the right, select **Full details**.</span></span> <span data-ttu-id="3ab50-244">De weergave met omgevingsdetails wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="3ab50-244">The environment details view appears.</span></span>
1. <span data-ttu-id="3ab50-245">Selecteer **Beheren** onder **Omgevingsfuncties**.</span><span class="sxs-lookup"><span data-stu-id="3ab50-245">Under **Environment features**, select **Manage**.</span></span>
1. <span data-ttu-id="3ab50-246">Selecteer **Initialiseren** op het tabblad **Commerce**.</span><span class="sxs-lookup"><span data-stu-id="3ab50-246">On the **Commerce** tab, select **Initialize**.</span></span> <span data-ttu-id="3ab50-247">De weergave CSU-initialisatieparameters wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="3ab50-247">The CSU initialization parameters view appears.</span></span>
1. <span data-ttu-id="3ab50-248">Kies voor **Regio** de optie **VS - oost**, **VS - oost 2**, **VS - west** of **VS - west 2**.</span><span class="sxs-lookup"><span data-stu-id="3ab50-248">In the **Region** field, select **East US**, **East US 2**, **West US**, or **West US 2**.</span></span>
1. <span data-ttu-id="3ab50-249">Selecteer in het veld **Versie** de optie **Een versie opgeven** in de lijst en geef **9.18.20014.4** op in het veld dat wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="3ab50-249">In the **Version** field, select **Specify a version** in the list, and then specify **9.18.20014.4** in the field that appears.</span></span> <span data-ttu-id="3ab50-250">Geef de exacte versie op die hier wordt aangegeven.</span><span class="sxs-lookup"><span data-stu-id="3ab50-250">Be sure to specify the exact version that is indicated here.</span></span> <span data-ttu-id="3ab50-251">Anders moet u RCSU later bijwerken naar de juiste versie.</span><span class="sxs-lookup"><span data-stu-id="3ab50-251">Otherwise, you will have to update RCSU to the correct version later.</span></span>
1. <span data-ttu-id="3ab50-252">Schakel de optie **Extensie toepassen** in.</span><span class="sxs-lookup"><span data-stu-id="3ab50-252">Turn on the **Apply extension** option.</span></span>
1. <span data-ttu-id="3ab50-253">Selecteer **Extensie voor Commerce Preview-demobasis** in de lijst met extensies.</span><span class="sxs-lookup"><span data-stu-id="3ab50-253">In the list of extensions, select **Commerce Preview Demo Base Extension**.</span></span>
1. <span data-ttu-id="3ab50-254">Selecteer **Initialiseren**.</span><span class="sxs-lookup"><span data-stu-id="3ab50-254">Select **Initialize**.</span></span>
1. <span data-ttu-id="3ab50-255">Controleer op de bevestigingspagina voor de implementatie of de details juist zijn en klik op **Ja**.</span><span class="sxs-lookup"><span data-stu-id="3ab50-255">On the deployment confirmation page, verify that the details are correct, and then select **Yes**.</span></span> <span data-ttu-id="3ab50-256">De weergave **Commerce-beheer** wordt opnieuw weergegeven, waarbij het tabblad **Commerce** is geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="3ab50-256">The **Commerce management** view displays again, where the **Commerce** tab is selected.</span></span> <span data-ttu-id="3ab50-257">Uw CSU is in de wachtrij geplaatst voor inrichting.</span><span class="sxs-lookup"><span data-stu-id="3ab50-257">Your CSU has been queued for provisioning.</span></span>
1. <span data-ttu-id="3ab50-258">Voordat u verdergaat, moet u controleren of de CSU-status **Gelukt** is.</span><span class="sxs-lookup"><span data-stu-id="3ab50-258">Before you continue, make sure that the status of your CSU is **Success**.</span></span> <span data-ttu-id="3ab50-259">Initialisatie duurt ongeveer twee tot vijf uur.</span><span class="sxs-lookup"><span data-stu-id="3ab50-259">Initialization takes approximately two to five hours.</span></span>

### <a name="initialize-e-commerce"></a><span data-ttu-id="3ab50-260">e-Commerce initialiseren</span><span class="sxs-lookup"><span data-stu-id="3ab50-260">Initialize e-Commerce</span></span>

<span data-ttu-id="3ab50-261">Ga als volgt te werk om e-Commerce te initialiseren.</span><span class="sxs-lookup"><span data-stu-id="3ab50-261">To initialize e-Commerce, follow these steps.</span></span>

1. <span data-ttu-id="3ab50-262">Controleer op het tabblad **e-Commerce** de toestemming voor de preview en selecteer vervolgens **Instellen**.</span><span class="sxs-lookup"><span data-stu-id="3ab50-262">On the **e-Commerce** tab, review the preview consent, and then select **Setup**.</span></span>
1. <span data-ttu-id="3ab50-263">Voer een naam in bij **Tenantnaam e-Commerce**.</span><span class="sxs-lookup"><span data-stu-id="3ab50-263">In the **e-Commerce tenant name** field, enter a name.</span></span> <span data-ttu-id="3ab50-264">Houd er rekening mee dat deze naam wordt weergegeven in sommige URL's die naar uw e-Commerce-exemplaar verwijzen.</span><span class="sxs-lookup"><span data-stu-id="3ab50-264">However, be aware that this name will appear in some of the URLs that point to your e-Commerce instance.</span></span>
1. <span data-ttu-id="3ab50-265">Selecteer in het veld **Naam Commerce Scale Unit** uw CSU in de lijst.</span><span class="sxs-lookup"><span data-stu-id="3ab50-265">In the **Commerce Scale Unit name** field, select your CSU in the list.</span></span> <span data-ttu-id="3ab50-266">(De lijst moet slechts één optie hebben.)</span><span class="sxs-lookup"><span data-stu-id="3ab50-266">(The list should have only one option.)</span></span>

    <span data-ttu-id="3ab50-267">Het veld **Geografie van e-Commerce** wordt automatisch ingevuld en kan niet worden gewijzigd.</span><span class="sxs-lookup"><span data-stu-id="3ab50-267">The **e-Commerce geography** field is set automatically, and the value can't be changed.</span></span>

1. <span data-ttu-id="3ab50-268">Selecteer **Volgende** om door te gaan.</span><span class="sxs-lookup"><span data-stu-id="3ab50-268">Select **Next** to continue.</span></span>
1. <span data-ttu-id="3ab50-269">Voer in het veld **Ondersteunde hostnamen** een geldig domein in, bijvoorbeeld `www.fabrikam.com`.</span><span class="sxs-lookup"><span data-stu-id="3ab50-269">In the **Supported host names** field, enter any valid domain, such as `www.fabrikam.com`.</span></span>
1.  <span data-ttu-id="3ab50-270">Voer in het veld **AAD-beveiligingsgroep voor systeembeheer** de eerste paar letters in van de naam van de beveiligingsgroep die u wilt gebruiken.</span><span class="sxs-lookup"><span data-stu-id="3ab50-270">In the **AAD security group for system admin** field, enter the first few letters of the name of the security group that you want to use.</span></span> <span data-ttu-id="3ab50-271">Selecteer het pictogram van het vergrootglas om de zoekresultaten weer te geven.</span><span class="sxs-lookup"><span data-stu-id="3ab50-271">Select the magnifying class icon to display the search results.</span></span> <span data-ttu-id="3ab50-272">Selecteer de juiste beveiligingsgroep in de lijst.</span><span class="sxs-lookup"><span data-stu-id="3ab50-272">Select the correct security group from the list.</span></span>
2.  <span data-ttu-id="3ab50-273">Voer in het veld **AAD-beveiligingsgroep voor moderator van beoordelingen en recensies** de eerste paar letters in van de naam van de beveiligingsgroep die u wilt gebruiken.</span><span class="sxs-lookup"><span data-stu-id="3ab50-273">In the **AAD security group for ratings and review moderator** field, enter the first few letters of the name of the security group that you want to use.</span></span> <span data-ttu-id="3ab50-274">Selecteer het pictogram van het vergrootglas om de zoekresultaten weer te geven.</span><span class="sxs-lookup"><span data-stu-id="3ab50-274">Select the magnifying class icon to display the search results.</span></span> <span data-ttu-id="3ab50-275">Selecteer de juiste beveiligingsgroep in de lijst.</span><span class="sxs-lookup"><span data-stu-id="3ab50-275">Select the correct security group from the list.</span></span>
1. <span data-ttu-id="3ab50-276">Laat **Service voor beoordelingen en recensies inschakelen** ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="3ab50-276">Leave the **Enable ratings and review service** option turned on.</span></span>
1. <span data-ttu-id="3ab50-277">Selecteer **Initialiseren**.</span><span class="sxs-lookup"><span data-stu-id="3ab50-277">Select **Initialize**.</span></span> <span data-ttu-id="3ab50-278">De weergave **Commerce-beheer** wordt opnieuw weergegeven, waarbij het tabblad **e-Commerce** is geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="3ab50-278">The **Commerce management** view displays again, where the **e-Commerce** tab is selected.</span></span> <span data-ttu-id="3ab50-279">De initialisatie van e-Commerce is gestart.</span><span class="sxs-lookup"><span data-stu-id="3ab50-279">E-Commerce initialization has started.</span></span>
1. <span data-ttu-id="3ab50-280">Voordat u verdergaat, moet u wachten tot de initialisatiestatus van e-Commerce **Geïnitieerd** is.</span><span class="sxs-lookup"><span data-stu-id="3ab50-280">Before you continue, wait until the status of e-Commerce initialization is **Initialization successful**.</span></span>
1. <span data-ttu-id="3ab50-281">Let onder **Koppeling** in de rechterbenedenhoek op de URL's voor de volgende koppelingen en noteer deze:</span><span class="sxs-lookup"><span data-stu-id="3ab50-281">Under **Links** in the lower right, make a note of the URLs for the following links:</span></span>

    * <span data-ttu-id="3ab50-282">**e-Commerce-site**: de koppeling naar de hoofdmap van uw e-Commerce-site.</span><span class="sxs-lookup"><span data-stu-id="3ab50-282">**e-Commerce site** – The link to the root of your e-Commerce site.</span></span>
    * <span data-ttu-id="3ab50-283">**Beheerhulpprogramma van de e-Commerce-site**: de koppeling naar het beheerhulpprogramma van de site.</span><span class="sxs-lookup"><span data-stu-id="3ab50-283">**e-Commerce site management tool** – The link to the site management tool.</span></span>

## <a name="commerce-preview-environment-support"></a><span data-ttu-id="3ab50-284">Ondersteuning voor preview-omgeving van Commerce</span><span class="sxs-lookup"><span data-stu-id="3ab50-284">Commerce preview environment support</span></span>

<span data-ttu-id="3ab50-285">Als u problemen ondervindt tijdens het uitvoeren van de inrichting, gaat u naar de [Microsoft Dynamics 365 Commerce Preview Yammer-groep](https://aka.ms/Dynamics365CommercePreviewYammer) voor hulp.</span><span class="sxs-lookup"><span data-stu-id="3ab50-285">If you experience issues while you're completing the provisioning steps, visit the [Microsoft Dynamics 365 Commerce Preview Yammer group](https://aka.ms/Dynamics365CommercePreviewYammer) for help.</span></span>

## <a name="next-steps"></a><span data-ttu-id="3ab50-286">Volgende stappen</span><span class="sxs-lookup"><span data-stu-id="3ab50-286">Next steps</span></span>

<span data-ttu-id="3ab50-287">Zie [Een preview-omgeving van Commerce configureren](cpe-post-provisioning.md) om door te gaan met het inrichten en configureren van uw preview-omgeving voor Commerce.</span><span class="sxs-lookup"><span data-stu-id="3ab50-287">To continue the process of provisioning and configuring your Commerce preview environment, see [Configure a Commerce preview environment](cpe-post-provisioning.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="3ab50-288">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="3ab50-288">Additional resources</span></span>

[<span data-ttu-id="3ab50-289">Omgevingsoverzicht Dynamics 365 Commerce-preview</span><span class="sxs-lookup"><span data-stu-id="3ab50-289">Dynamics 365 Commerce preview environment overview</span></span>](cpe-overview.md)

[<span data-ttu-id="3ab50-290">Een Dynamics 365 Commerce-preview-omgeving configureren</span><span class="sxs-lookup"><span data-stu-id="3ab50-290">Configure a Dynamics 365 Commerce preview environment</span></span>](cpe-post-provisioning.md)

[<span data-ttu-id="3ab50-291">Optionele functies voor een Dynamics 365 Commerce-preview-omgeving configureren</span><span class="sxs-lookup"><span data-stu-id="3ab50-291">Configure optional features for a Dynamics 365 Commerce preview environment</span></span>](cpe-optional-features.md)

[<span data-ttu-id="3ab50-292">Veelgestelde vragen over Dynamics 365 Commerce-preview-omgeving</span><span class="sxs-lookup"><span data-stu-id="3ab50-292">Dynamics 365 Commerce preview environment FAQ</span></span>](cpe-faq.md)

[<span data-ttu-id="3ab50-293">Microsoft Lifecycle Services (LCS)</span><span class="sxs-lookup"><span data-stu-id="3ab50-293">Microsoft Lifecycle Services (LCS)</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[<span data-ttu-id="3ab50-294">Commerce Scale Unit (cloud)</span><span class="sxs-lookup"><span data-stu-id="3ab50-294">Commerce Scale Unit (cloud)</span></span>](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[<span data-ttu-id="3ab50-295">Microsoft Azure-portal</span><span class="sxs-lookup"><span data-stu-id="3ab50-295">Microsoft Azure portal</span></span>](https://azure.microsoft.com/features/azure-portal)

[<span data-ttu-id="3ab50-296">Dynamics 365 Commerce-website</span><span class="sxs-lookup"><span data-stu-id="3ab50-296">Dynamics 365 Commerce website</span></span>](https://aka.ms/Dynamics365CommerceWebsite)

