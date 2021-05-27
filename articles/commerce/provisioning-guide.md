---
title: Een evaluatieomgeving voor Dynamics 365 Commerce inrichten
description: In dit onderwerp wordt uitgelegd hoe u een evaluatieomgeving van Microsoft Dynamics 365 Commerce inricht.
author: psimolin
ms.date: 12/17/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 6b675d4af6fb9a080f3f3a13e64b2c5b6ad4b783
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/11/2021
ms.locfileid: "6022417"
---
# <a name="provision-a-dynamics-365-commerce-evaluation-environment"></a><span data-ttu-id="6ea39-103">Een evaluatieomgeving voor Dynamics 365 Commerce inrichten</span><span class="sxs-lookup"><span data-stu-id="6ea39-103">Provision a Dynamics 365 Commerce evaluation environment</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="6ea39-104">In dit onderwerp wordt uitgelegd hoe u een evaluatieomgeving van Microsoft Dynamics 365 Commerce inricht.</span><span class="sxs-lookup"><span data-stu-id="6ea39-104">This topic explains how to provision a Microsoft Dynamics 365 Commerce evaluation environment.</span></span>

<span data-ttu-id="6ea39-105">Voordat u begint, kunt u het beste dit onderwerp snel doorlezen om een idee te krijgen van wat nodig is voor het proces.</span><span class="sxs-lookup"><span data-stu-id="6ea39-105">Before you begin, we recommend that you take a quick scan through this topic to get an idea of what the process requires.</span></span>

> [!NOTE]
> <span data-ttu-id="6ea39-106">Commerce-evaluatieomgevingen zijn doorgaans niet beschikbaar en worden aan partners en klanten op aanvraag ter beschikking gesteld.</span><span class="sxs-lookup"><span data-stu-id="6ea39-106">Commerce evaluation environments aren't generally available, and are granted to partners and customers on a per-request basis.</span></span> <span data-ttu-id="6ea39-107">Neem contact op met uw Microsoft-partner voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="6ea39-107">For more information, reach out to your Microsoft partner contact.</span></span>

<span data-ttu-id="6ea39-108">Als u uw evaluatieomgeving van Commerce wilt inrichten, moet u een project maken met een specifieke productnaam en een specifiek producttype.</span><span class="sxs-lookup"><span data-stu-id="6ea39-108">To successfully provision a Commerce evaluation environment, you must create a project that has a specific product name and type.</span></span> <span data-ttu-id="6ea39-109">De omgeving en Commerce Scale Unit (CSU) beschikken ook over specifieke parameters die u moet gebruiken wanneer u e-Commerce later wilt inrichten.</span><span class="sxs-lookup"><span data-stu-id="6ea39-109">The environment and Commerce Scale Unit (CSU) also have some specific parameters that you must use when you expect to provision e-Commerce later.</span></span> <span data-ttu-id="6ea39-110">De instructies in dit onderwerp beschrijven alle vereiste stappen voor het voltooien van de inrichting en de parameters die u moet gebruiken.</span><span class="sxs-lookup"><span data-stu-id="6ea39-110">The instructions in this topic describe all the steps that are required to complete provisioning and the parameters that you must use.</span></span>

<span data-ttu-id="6ea39-111">Nadat de inrichting van de evaluatieomgeving van Commerce is voltooid, moet u een aantal stappen uitvoeren om de preview-omgeving voor te bereiden.</span><span class="sxs-lookup"><span data-stu-id="6ea39-111">After you successfully provision your Commerce evaluation environment, you must complete a few post-provisioning steps to prepare it for use.</span></span> <span data-ttu-id="6ea39-112">Sommige stappen zijn optioneel, afhankelijk van de aspecten van het systeem die u wilt evalueren.</span><span class="sxs-lookup"><span data-stu-id="6ea39-112">Some steps are optional, depending on the aspects of the system that you want to evaluate.</span></span> <span data-ttu-id="6ea39-113">U kunt de optionele stappen altijd later voltooien.</span><span class="sxs-lookup"><span data-stu-id="6ea39-113">You can always complete the optional steps later.</span></span>

<span data-ttu-id="6ea39-114">Zie [Een evaluatieomgeving van Commerce configureren](cpe-post-provisioning.md) voor meer informatie over hoe u uw evaluatieomgeving voor Commerce configureert nadat u deze hebt ingericht.</span><span class="sxs-lookup"><span data-stu-id="6ea39-114">For information about how to configure your Commerce evaluation environment after you provision it, see [Configure a Commerce evaluation environment](cpe-post-provisioning.md).</span></span> <span data-ttu-id="6ea39-115">Zie [Optionele functies voor een evaluatieomgeving van Commerce configureren](cpe-optional-features.md) voor meer informatie over hoe u optionele functies voor uw evaluatieomgeving van Commerce configureert.</span><span class="sxs-lookup"><span data-stu-id="6ea39-115">For information about how to configure optional features for your Commerce evaluation environment, see [Configure optional features for a Commerce evaluation environment](cpe-optional-features.md).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="6ea39-116">Vereisten</span><span class="sxs-lookup"><span data-stu-id="6ea39-116">Prerequisites</span></span>

<span data-ttu-id="6ea39-117">Aan de volgende voorwaarden moeten zijn voldaan voordat u uw evaluatieomgeving van Commerce inricht:</span><span class="sxs-lookup"><span data-stu-id="6ea39-117">The following prerequisites must be in place before you can provision your Commerce evaluation environment:</span></span>

- <span data-ttu-id="6ea39-118">U bent geregistreerd voor het evaluatieprogramma en hebt capaciteit gekregen voor een evaluatieomgeving.</span><span class="sxs-lookup"><span data-stu-id="6ea39-118">You have been onboarded into the evaluation program and granted capacity for an evaluation environment.</span></span>
- <span data-ttu-id="6ea39-119">U hebt toegang tot de Microsoft Dynamics Lifecycle Services-portal (LCS).</span><span class="sxs-lookup"><span data-stu-id="6ea39-119">You have access to the Microsoft Dynamics Lifecycle Services (LCS) portal.</span></span>
- <span data-ttu-id="6ea39-120">U bent een bestaande Microsoft Dynamics 365-partner of -klant en kunt een Dynamics 365 Commerce-project maken.</span><span class="sxs-lookup"><span data-stu-id="6ea39-120">You are an existing Microsoft Dynamics 365 partner or customer and are able to create a Dynamics 365 Commerce project.</span></span>
- <span data-ttu-id="6ea39-121">U hebt beheerderstoegang tot uw Microsoft Azure-abonnement of u bent in contact met een abonnementsbeheerder die u kan helpen als dat nodig is.</span><span class="sxs-lookup"><span data-stu-id="6ea39-121">You have administrator access to your Microsoft Azure subscription, or you're in contact with a subscription administrator who can assist you if required.</span></span>
- <span data-ttu-id="6ea39-122">U hebt uw Azure Active Directory-tenant-id (Azure AD) bij de hand.</span><span class="sxs-lookup"><span data-stu-id="6ea39-122">You have your Azure Active Directory (Azure AD) tenant ID available.</span></span>
- <span data-ttu-id="6ea39-123">U hebt een Azure AD-beveiligingsgroep gemaakt om te gebruiken als e-Commerce-systeembeheerdersgroep en u hebt de id bij de hand.</span><span class="sxs-lookup"><span data-stu-id="6ea39-123">You've created an Azure AD security group that can be used as an e-Commerce system admin group, and you have its ID available.</span></span>
- <span data-ttu-id="6ea39-124">U hebt een Azure AD-beveiligingsgroep gemaakt om te gebruiken als moderatorgroep voor beoordelingen en recensies en u hebt de id bij de hand.</span><span class="sxs-lookup"><span data-stu-id="6ea39-124">You've created an Azure AD security group that can be used as a Ratings and Reviews moderator group, and you have its ID available.</span></span> <span data-ttu-id="6ea39-125">(Deze beveiligingsgroep kan dezelfde zijn als de systeembeheerdersgroep van e-Commerce.)</span><span class="sxs-lookup"><span data-stu-id="6ea39-125">(This security group can be the same as the e-Commerce system admin group.)</span></span>

<span data-ttu-id="6ea39-126">Deze lijst is niet volledig.</span><span class="sxs-lookup"><span data-stu-id="6ea39-126">Note that this list isn't exhaustive.</span></span> <span data-ttu-id="6ea39-127">Neem contact op met uw Microsoft-partner voor hulp als u problemen ondervindt.</span><span class="sxs-lookup"><span data-stu-id="6ea39-127">If you experience any issues, reach out to your Microsoft partner contact for assistance.</span></span>

## <a name="provision-your-commerce-evaluation-environment"></a><span data-ttu-id="6ea39-128">Uw evaluatieomgeving van Commerce inrichten</span><span class="sxs-lookup"><span data-stu-id="6ea39-128">Provision your Commerce evaluation environment</span></span>

<span data-ttu-id="6ea39-129">In deze procedures wordt uitgelegd hoe u een evaluatieomgeving van Commerce inricht.</span><span class="sxs-lookup"><span data-stu-id="6ea39-129">These procedures explain how to provision a Commerce evaluation environment.</span></span> <span data-ttu-id="6ea39-130">Als u dit hebt gedaan, is de evaluatieomgeving van Commerce gereed voor configuratie.</span><span class="sxs-lookup"><span data-stu-id="6ea39-130">After you successfully complete them, the Commerce evaluation environment will be ready for configuration.</span></span> <span data-ttu-id="6ea39-131">Alle activiteiten die hier worden beschreven, vinden plaats in de LCS-portal.</span><span class="sxs-lookup"><span data-stu-id="6ea39-131">All the activities that are described here occur in the LCS portal.</span></span>

### <a name="create-a-new-project"></a><span data-ttu-id="6ea39-132">Een nieuw project maken</span><span class="sxs-lookup"><span data-stu-id="6ea39-132">Create a new project</span></span>

<span data-ttu-id="6ea39-133">Ga als volgt te werk om een nieuw project te maken in LCS.</span><span class="sxs-lookup"><span data-stu-id="6ea39-133">To create a new project in LCS, follow these steps.</span></span>

1. <span data-ttu-id="6ea39-134">Selecteer op de LCS-startpagina het plusteken (**+**) om een project te maken.</span><span class="sxs-lookup"><span data-stu-id="6ea39-134">On the LCS home page, select the plus sign (**+**) to create a project.</span></span>
1. <span data-ttu-id="6ea39-135">Volg een van de volgende stappen uit in het rechterdeelvenster:</span><span class="sxs-lookup"><span data-stu-id="6ea39-135">In the right pane, follow one of these steps:</span></span>

    - <span data-ttu-id="6ea39-136">Als u een partner bent, selecteert u **Migreren, oplossingen maken en informatie over**.</span><span class="sxs-lookup"><span data-stu-id="6ea39-136">If you're a partner, select **Migrate, create solutions, and learn**.</span></span>
    - <span data-ttu-id="6ea39-137">Als u een klant bent, selecteert u **Potentiële presales**.</span><span class="sxs-lookup"><span data-stu-id="6ea39-137">If you're a customer, select **Prospective presales**.</span></span>

1. <span data-ttu-id="6ea39-138">Voer een naam, beschrijving en branche in.</span><span class="sxs-lookup"><span data-stu-id="6ea39-138">Enter a name, description, and industry.</span></span>
1. <span data-ttu-id="6ea39-139">Selecteer **Dynamics 365 Commerce** in het veld **Productnaam**.</span><span class="sxs-lookup"><span data-stu-id="6ea39-139">In the **Product name** field, select **Dynamics 365 Commerce**.</span></span>
1. <span data-ttu-id="6ea39-140">Selecteer **Dynamics 365 Commerce** in het veld **Productversie**.</span><span class="sxs-lookup"><span data-stu-id="6ea39-140">In the **Product version** field, select **Dynamics 365 Commerce**.</span></span>
1. <span data-ttu-id="6ea39-141">Selecteer **Implementatiemethodologie voor Dynamics Retail** in het veld **Methodologie**.</span><span class="sxs-lookup"><span data-stu-id="6ea39-141">In the **Methodology** field, select **Dynamics Retail implementation methodology**.</span></span>
1. <span data-ttu-id="6ea39-142">Optioneel: u kunt rollen en gebruikers importeren uit bestaand project.</span><span class="sxs-lookup"><span data-stu-id="6ea39-142">Optional: You can import roles and users from an existing project.</span></span>
1. <span data-ttu-id="6ea39-143">Selecteer **Maken**.</span><span class="sxs-lookup"><span data-stu-id="6ea39-143">Select **Create**.</span></span> <span data-ttu-id="6ea39-144">De projectweergave wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="6ea39-144">The project view appears.</span></span>

### <a name="add-the-azure-connector"></a><span data-ttu-id="6ea39-145">De Azure-connector toevoegen</span><span class="sxs-lookup"><span data-stu-id="6ea39-145">Add the Azure Connector</span></span>

<span data-ttu-id="6ea39-146">Om de Azure-connector aan uw LCS-project toe te voegen volgt u de stappen in de procedure voor [het voltooien van het onboardingproces van Azure Resource Manager (ARM)](../fin-ops-core/dev-itpro/deployment/arm-onboarding.md).</span><span class="sxs-lookup"><span data-stu-id="6ea39-146">To add the Azure Connector to your LCS project, follow the steps in [Complete the Azure Resource Manager (ARM) onboarding process](../fin-ops-core/dev-itpro/deployment/arm-onboarding.md).</span></span>

### <a name="deploy-the-environment"></a><span data-ttu-id="6ea39-147">De omgeving implementeren</span><span class="sxs-lookup"><span data-stu-id="6ea39-147">Deploy the environment</span></span>

<span data-ttu-id="6ea39-148">Ga als volgt te werk om de omgeving te implementeren.</span><span class="sxs-lookup"><span data-stu-id="6ea39-148">To deploy the environment, follow these steps.</span></span>

> [!NOTE]
> <span data-ttu-id="6ea39-149">Het is mogelijk dat u de stappen 6, 7 en/of 8 niet hoeft te voltooien, omdat pagina's met één optie worden overgeslagen.</span><span class="sxs-lookup"><span data-stu-id="6ea39-149">You might not have to complete steps 6, 7, and/or 8, because pages that have a single option are skipped.</span></span> <span data-ttu-id="6ea39-150">Controleer in de weergave **Omgevingsparameters** of u de tekst **Dynamics 365 Commerce - Demo (10.0.* x* met Platform update *xx*)\*\* direct boven het veld **Omgevingsnaam** ziet.</span><span class="sxs-lookup"><span data-stu-id="6ea39-150">When you're in the **Environment parameters** view, confirm that the text **Dynamics 365 Commerce - Demo (10.0.* x* with Platform update *xx*)\*\* appears directly above the **Environment name** field.</span></span> <span data-ttu-id="6ea39-151">Zie de afbeelding die na stap 8 wordt weergegeven voor nadere details.</span><span class="sxs-lookup"><span data-stu-id="6ea39-151">For details, see the illustration that appears after step 8.</span></span>

1. <span data-ttu-id="6ea39-152">Selecteer in het bovenste menu de optie **Cloudomgevingen**.</span><span class="sxs-lookup"><span data-stu-id="6ea39-152">On the top menu, select **Cloud-hosted environments**.</span></span>
1. <span data-ttu-id="6ea39-153">Selecteer **Toevoegen** om een omgeving toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="6ea39-153">Select **Add** to add an environment.</span></span>
1. <span data-ttu-id="6ea39-154">Selecteer in het veld **Toepassingsversie** de meest recente versie.</span><span class="sxs-lookup"><span data-stu-id="6ea39-154">In the **Application version** field, select the most current version.</span></span> <span data-ttu-id="6ea39-155">Als u specifiek een andere toepassingsversie dan de meest recente versie wilt selecteren, moet u geen eerdere versie dan **10.0.14** selecteren.</span><span class="sxs-lookup"><span data-stu-id="6ea39-155">If you have a specific need to select an application version other than the most current version, do not select a version prior to **10.0.14**.</span></span>
1. <span data-ttu-id="6ea39-156">Gebruik in het veld **Platformversie** de platform versie die automatisch wordt gekozen voor de toepassingsversie die u hebt geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="6ea39-156">In the **Platform version** field, use the platform version that is automatically chosen for the application version you selected.</span></span> 

    ![Toepassings- en platformversies selecteren](./media/project1.png)

1. <span data-ttu-id="6ea39-158">Selecteer **Volgende**.</span><span class="sxs-lookup"><span data-stu-id="6ea39-158">Select **Next**.</span></span>
1. <span data-ttu-id="6ea39-159">Selecteer **Demo** als de omgevingstopologie.</span><span class="sxs-lookup"><span data-stu-id="6ea39-159">Select **Demo** as the environment topology.</span></span>

    ![De omgevingstopologie 1 selecteren](./media/project2.png)

1. <span data-ttu-id="6ea39-161">Voer op de pagina **Omgeving implementeren** een omgevingsnaam in.</span><span class="sxs-lookup"><span data-stu-id="6ea39-161">On the **Deploy environment** page, enter an environment name.</span></span> <span data-ttu-id="6ea39-162">Laat geavanceerde instellingen ongewijzigd.</span><span class="sxs-lookup"><span data-stu-id="6ea39-162">Leave the advanced settings as they are.</span></span>

    ![De pagina Omgeving implementeren](./media/project4.png)

1. <span data-ttu-id="6ea39-164">Pas de VM-grootte naar wens aan.</span><span class="sxs-lookup"><span data-stu-id="6ea39-164">Adjust the VM size as required.</span></span> <span data-ttu-id="6ea39-165">(We raden VM-voorraadeenheid \[SKU\] **D13 v2** aan.)</span><span class="sxs-lookup"><span data-stu-id="6ea39-165">(We recommend VM stock keeping unit \[SKU\] **D13 v2**.)</span></span>
1. <span data-ttu-id="6ea39-166">Controleer de prijs- en licentievoorwaarden en schakel vervolgens het selectievakje in om aan te geven dat u ermee instemt.</span><span class="sxs-lookup"><span data-stu-id="6ea39-166">Review the pricing and licensing terms, and then select the check box to indicate that you agree to them.</span></span>
1. <span data-ttu-id="6ea39-167">Selecteer **Volgende**.</span><span class="sxs-lookup"><span data-stu-id="6ea39-167">Select **Next**.</span></span>
1. <span data-ttu-id="6ea39-168">Controleer op de bevestigingspagina voor de implementatie of de details juist zijn en klik op **Implementeren**.</span><span class="sxs-lookup"><span data-stu-id="6ea39-168">On the deployment confirmation page, verify that the details are correct, and then select **Deploy**.</span></span> <span data-ttu-id="6ea39-169">U keert terug naar de weergave in **Cloudomgevingen** en uw omgeving wordt weergegeven in de lijst.</span><span class="sxs-lookup"><span data-stu-id="6ea39-169">You're returned to the **Cloud-hosted environments** view, and your environment should appear in the list.</span></span>

    <span data-ttu-id="6ea39-170">Uw aangevraagde omgeving wordt weergegeven in de wachtrij en vervolgens geïmplementeerd.</span><span class="sxs-lookup"><span data-stu-id="6ea39-170">Your requested environment will appear as queued and then deploying.</span></span> <span data-ttu-id="6ea39-171">Het duurt even voordat de werkstromen van de omgeving zijn voltooid.</span><span class="sxs-lookup"><span data-stu-id="6ea39-171">The environment workflows will take some time to be completed.</span></span> <span data-ttu-id="6ea39-172">Controleer dit daarom na ongeveer zes tot negen uur.</span><span class="sxs-lookup"><span data-stu-id="6ea39-172">Therefore, check back after approximately six to nine hours.</span></span>

1. <span data-ttu-id="6ea39-173">Voordat u verdergaat, moet u controleren of de omgevingsstatus **Geïmplementeerd** is.</span><span class="sxs-lookup"><span data-stu-id="6ea39-173">Before you continue, make sure that the status of your environment is **Deployed**.</span></span>

### <a name="initialize-the-commerce-scale-unit-cloud"></a><span data-ttu-id="6ea39-174">Commerce Scale Unit initialiseren (cloud)</span><span class="sxs-lookup"><span data-stu-id="6ea39-174">Initialize the Commerce Scale Unit (cloud)</span></span>

<span data-ttu-id="6ea39-175">Ga als volgt te werk om de CSU te initialiseren.</span><span class="sxs-lookup"><span data-stu-id="6ea39-175">To initialize the CSU, follow these steps.</span></span>

1. <span data-ttu-id="6ea39-176">Selecteer in de weergave **Cloudomgevingen** uw omgeving in de lijst.</span><span class="sxs-lookup"><span data-stu-id="6ea39-176">In the **Cloud-hosted environments** view, select your environment in the list.</span></span>
1. <span data-ttu-id="6ea39-177">Klik op **Volledige details** in de omgevingsweergave rechts.</span><span class="sxs-lookup"><span data-stu-id="6ea39-177">In the environment view on the right, select **Full details**.</span></span> <span data-ttu-id="6ea39-178">De weergave met omgevingsdetails wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="6ea39-178">The environment details view appears.</span></span>
1. <span data-ttu-id="6ea39-179">Selecteer **Beheren** onder **Omgevingsfuncties**.</span><span class="sxs-lookup"><span data-stu-id="6ea39-179">Under **Environment features**, select **Manage**.</span></span>
1. <span data-ttu-id="6ea39-180">Selecteer **Initialiseren** op het tabblad **Commerce**.</span><span class="sxs-lookup"><span data-stu-id="6ea39-180">On the **Commerce** tab, select **Initialize**.</span></span> <span data-ttu-id="6ea39-181">De weergave CSU-initialisatieparameters wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="6ea39-181">The CSU initialization parameters view appears.</span></span>
1. <span data-ttu-id="6ea39-182">Selecteer in het veld **Regio** de regio die gelijk is aan of dichtbij de regio waar u de omgeving hebt geïmplementeerd.</span><span class="sxs-lookup"><span data-stu-id="6ea39-182">In the **Region** field, select the region that is the same or close to the region that you deployed the environment to.</span></span>
1. <span data-ttu-id="6ea39-183">Laat het veld **Versie** ongewijzigd.</span><span class="sxs-lookup"><span data-stu-id="6ea39-183">Leave the **Version** field as it is.</span></span>
1. <span data-ttu-id="6ea39-184">Selecteer **Initialiseren**.</span><span class="sxs-lookup"><span data-stu-id="6ea39-184">Select **Initialize**.</span></span>
1. <span data-ttu-id="6ea39-185">Controleer op de bevestigingspagina voor de implementatie of de details juist zijn en klik op **Ja**.</span><span class="sxs-lookup"><span data-stu-id="6ea39-185">On the deployment confirmation page, verify that the details are correct, and then select **Yes**.</span></span> <span data-ttu-id="6ea39-186">De weergave **Commerce-beheer** wordt opnieuw weergegeven, waarbij het tabblad **Commerce** is geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="6ea39-186">The **Commerce management** view displays again, where the **Commerce** tab is selected.</span></span> <span data-ttu-id="6ea39-187">Uw CSU is in de wachtrij geplaatst voor inrichting.</span><span class="sxs-lookup"><span data-stu-id="6ea39-187">Your CSU has been queued for provisioning.</span></span>
1. <span data-ttu-id="6ea39-188">Voordat u verdergaat, moet u controleren of de CSU-status **Gelukt** is.</span><span class="sxs-lookup"><span data-stu-id="6ea39-188">Before you continue, make sure that the status of your CSU is **Success**.</span></span> <span data-ttu-id="6ea39-189">Initialisatie duurt ongeveer twee tot vijf uur.</span><span class="sxs-lookup"><span data-stu-id="6ea39-189">Initialization takes approximately two to five hours.</span></span>

<span data-ttu-id="6ea39-190">Als u de koppeling **Beheren** niet kunt vinden in de weergave met omgevingsdetails, neemt u contact op met Microsoft voor hulp.</span><span class="sxs-lookup"><span data-stu-id="6ea39-190">If you can't find the **Manage** link in the environment details view, reach out to your Microsoft contact for assistance.</span></span>

<span data-ttu-id="6ea39-191">Mogelijk wordt het volgende foutbericht weergegeven tijdens het implementatieproces:</span><span class="sxs-lookup"><span data-stu-id="6ea39-191">During the deployment process, you might receive the following error message:</span></span>

> <span data-ttu-id="6ea39-192">Voor evaluatieomgevingen (demo/test) moet de connectortoepassing voor schaaleenheden \<application ID\> in Headquarters worden geregistreerd.</span><span class="sxs-lookup"><span data-stu-id="6ea39-192">Evaluation (demo/test) environments need to register the scale unit connector application \<application ID\> in headquarters.</span></span>

<span data-ttu-id="6ea39-193">Als de CSU-initialisatie mislukt en u dit foutbericht ontvangt, noteert u de toepassings-id (een GUID) en volg vervolgens de stappen in de volgende sectie om de CSU-implementatietoepassing in Commerce Headquarters te registreren.</span><span class="sxs-lookup"><span data-stu-id="6ea39-193">If the CSU initialization fails and you receive this error message, make a note of the application ID, which is a globally unique identifier (GUID), and then follow the steps in the next section to register the CSU deployment application in Commerce headquarters.</span></span>

### <a name="register-the-csu-deployment-application-in-commerce-headquarters-if-required"></a><span data-ttu-id="6ea39-194">De CSU-implementatietoepassing in Commerce Headquarters registreren (indien nodig)</span><span class="sxs-lookup"><span data-stu-id="6ea39-194">Register the CSU deployment application in Commerce headquarters (if required)</span></span>

<span data-ttu-id="6ea39-195">Voer de volgende stappen uit om de CSU-implementatietoepassing in Commerce Headquarters te registreren.</span><span class="sxs-lookup"><span data-stu-id="6ea39-195">To register the CSU deployment application in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="6ea39-196">Ga in Commerce Headquarters naar **Systeembeheer \> Instellen \> Azure Active Directory-toepassingen**.</span><span class="sxs-lookup"><span data-stu-id="6ea39-196">In Commerce headquarters, go to **System administration \> Setup \> Azure Active Directory applications**.</span></span>
1. <span data-ttu-id="6ea39-197">Voer in de kolom **Client-id** de toepassings-id uit het foutbericht voor CSU-initialisatie in dat u hebt ontvangen.</span><span class="sxs-lookup"><span data-stu-id="6ea39-197">In the **Client Id** column, enter the application ID from the CSU initialization error message that you received.</span></span>
1. <span data-ttu-id="6ea39-198">Voer in de kolom **Naam** een beschrijvende tekst in (bijvoorbeeld **CSU-eval**).</span><span class="sxs-lookup"><span data-stu-id="6ea39-198">In the **Name** column, enter any descriptive text (for example, **CSU Eval**).</span></span>
1. <span data-ttu-id="6ea39-199">Voer in de kolom **Gebruikers-id** de tekst **RetailServiceAccount** in.</span><span class="sxs-lookup"><span data-stu-id="6ea39-199">In the **User ID** column, enter **RetailServiceAccount**.</span></span>
1. <span data-ttu-id="6ea39-200">Probeer de CSU-initialisatie en -implementatie opnieuw uit te voeren vanuit LCS.</span><span class="sxs-lookup"><span data-stu-id="6ea39-200">Retry the CSU initialization and deployment from LCS.</span></span>

### <a name="initialize-e-commerce"></a><span data-ttu-id="6ea39-201">e-Commerce initialiseren</span><span class="sxs-lookup"><span data-stu-id="6ea39-201">Initialize e-Commerce</span></span>

<span data-ttu-id="6ea39-202">Ga als volgt te werk om e-Commerce te initialiseren.</span><span class="sxs-lookup"><span data-stu-id="6ea39-202">To initialize e-Commerce, follow these steps.</span></span>

1. <span data-ttu-id="6ea39-203">Controleer op het tabblad **e-Commerce** de toestemming voor de evaluatie en selecteer vervolgens **Instellen**.</span><span class="sxs-lookup"><span data-stu-id="6ea39-203">On the **e-Commerce** tab, review the evaluation consent, and then select **Setup**.</span></span>
1. <span data-ttu-id="6ea39-204">Voer een naam in bij **Omgevingsnaam e-Commerce**.</span><span class="sxs-lookup"><span data-stu-id="6ea39-204">In the **e-Commerce environment name** field, enter a name.</span></span> <span data-ttu-id="6ea39-205">Houd er rekening mee dat deze naam wordt weergegeven in sommige URL's die naar uw e-Commerce-exemplaar verwijzen.</span><span class="sxs-lookup"><span data-stu-id="6ea39-205">Be aware that this name will appear in some of the URLs that point to your e-Commerce instance.</span></span>
1. <span data-ttu-id="6ea39-206">Selecteer in het veld **Naam Commerce Scale Unit** uw CSU in de lijst.</span><span class="sxs-lookup"><span data-stu-id="6ea39-206">In the **Commerce Scale Unit name** field, select your CSU in the list.</span></span> <span data-ttu-id="6ea39-207">(De lijst moet slechts één optie hebben.)</span><span class="sxs-lookup"><span data-stu-id="6ea39-207">(The list should have only one option.)</span></span>

    <span data-ttu-id="6ea39-208">Het veld **Geografie van e-Commerce** wordt automatisch ingesteld.</span><span class="sxs-lookup"><span data-stu-id="6ea39-208">The **e-Commerce geography** field is set automatically.</span></span>

1. <span data-ttu-id="6ea39-209">Selecteer **Volgende** om door te gaan.</span><span class="sxs-lookup"><span data-stu-id="6ea39-209">Select **Next** to continue.</span></span>
1. <span data-ttu-id="6ea39-210">Voer in het veld **Ondersteunde hostnamen** een geldig domein in, bijvoorbeeld `www.fabrikam.com`.</span><span class="sxs-lookup"><span data-stu-id="6ea39-210">In the **Supported host names** field, enter any valid domain, such as `www.fabrikam.com`.</span></span>
1. <span data-ttu-id="6ea39-211">Voer in het veld **AAD-beveiligingsgroep voor systeembeheer** de eerste paar letters van de naam van de beveiligingsgroep in die u wilt gebruiken en selecteer vervolgens het vergrootglassymbool om de zoekresultaten weer te geven.</span><span class="sxs-lookup"><span data-stu-id="6ea39-211">In the **AAD security group for system admin** field, enter the first few letters of the name of the security group that you want to use, and then select the magnifying glass symbol to view the search results.</span></span> <span data-ttu-id="6ea39-212">Selecteer de juiste beveiligingsgroep in de lijst.</span><span class="sxs-lookup"><span data-stu-id="6ea39-212">Select the correct security group in the list.</span></span>
1.  <span data-ttu-id="6ea39-213">Voer in het veld **AAD-beveiligingsgroep voor moderator van beoordelingen en recensies** de eerste paar letters van de naam van de beveiligingsgroep in die u wilt gebruiken en selecteer vervolgens het vergrootglassymbool om de zoekresultaten weer te geven.</span><span class="sxs-lookup"><span data-stu-id="6ea39-213">In the **AAD security group for ratings and review moderator** field, enter the first few letters of the name of the security group that you want to use, and then select the magnifying glass symbol to view the search results.</span></span> <span data-ttu-id="6ea39-214">Selecteer de juiste beveiligingsgroep in de lijst.</span><span class="sxs-lookup"><span data-stu-id="6ea39-214">Select the correct security group in the list.</span></span>
1. <span data-ttu-id="6ea39-215">Laat de optie **Service voor beoordelingen en recensies inschakelen** op **Ja** staan.</span><span class="sxs-lookup"><span data-stu-id="6ea39-215">Leave the **Enable ratings and review service** option set to **Yes**.</span></span>
1. <span data-ttu-id="6ea39-216">Selecteer **Initialiseren**.</span><span class="sxs-lookup"><span data-stu-id="6ea39-216">Select **Initialize**.</span></span> <span data-ttu-id="6ea39-217">De weergave **Commerce-beheer** wordt opnieuw weergegeven, waarbij het tabblad **e-Commerce** is geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="6ea39-217">The **Commerce management** view displays again, where the **e-Commerce** tab is selected.</span></span> <span data-ttu-id="6ea39-218">De initialisatie van e-Commerce is gestart.</span><span class="sxs-lookup"><span data-stu-id="6ea39-218">E-Commerce initialization has started.</span></span>
1. <span data-ttu-id="6ea39-219">Voordat u verdergaat, moet u wachten tot de initialisatiestatus van e-Commerce **Geïnitieerd** is.</span><span class="sxs-lookup"><span data-stu-id="6ea39-219">Before you continue, wait until the status of e-Commerce initialization is **Initialization successful**.</span></span>
1. <span data-ttu-id="6ea39-220">Let onder **Koppeling** in de rechterbenedenhoek op de URL's voor de volgende koppelingen en noteer deze:</span><span class="sxs-lookup"><span data-stu-id="6ea39-220">Under **Links** in the lower right, make a note of the URLs for the following links:</span></span>

    * <span data-ttu-id="6ea39-221">**e-Commerce-site**: de koppeling naar de hoofdmap van uw e-Commerce-site.</span><span class="sxs-lookup"><span data-stu-id="6ea39-221">**e-Commerce site** – The link to the root of your e-Commerce site.</span></span>
    * <span data-ttu-id="6ea39-222">**Commerce Site Builder**: de koppeling naar het beheerhulpprogramma van de site.</span><span class="sxs-lookup"><span data-stu-id="6ea39-222">**Commerce site builder** – The link to the site management tool.</span></span>

## <a name="next-steps"></a><span data-ttu-id="6ea39-223">Volgende stappen</span><span class="sxs-lookup"><span data-stu-id="6ea39-223">Next steps</span></span>

<span data-ttu-id="6ea39-224">Zie [Een evaluatieomgeving van Commerce configureren](cpe-post-provisioning.md) om door te gaan met het inrichten en configureren van uw evaluatieomgeving voor Commerce.</span><span class="sxs-lookup"><span data-stu-id="6ea39-224">To continue the process of provisioning and configuring your Commerce evaluation environment, see [Configure a Commerce evaluation environment](cpe-post-provisioning.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="6ea39-225">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="6ea39-225">Additional resources</span></span>

[<span data-ttu-id="6ea39-226">Overzicht van de evaluatieomgeving voor Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="6ea39-226">Dynamics 365 Commerce evaluation environment overview</span></span>](cpe-overview.md)

[<span data-ttu-id="6ea39-227">Een Dynamics 365 Commerce-evaluatieomgeving configureren</span><span class="sxs-lookup"><span data-stu-id="6ea39-227">Configure a Dynamics 365 Commerce evaluation environment</span></span>](cpe-post-provisioning.md)

[<span data-ttu-id="6ea39-228">BOPIS configureren in een Dynamics 365 Commerce-evaluatieomgeving</span><span class="sxs-lookup"><span data-stu-id="6ea39-228">Configure BOPIS in a Dynamics 365 Commerce evaluation environment</span></span>](cpe-bopis.md)

[<span data-ttu-id="6ea39-229">Optionele functies voor een Dynamics 365 Commerce-evaluatieomgeving configureren</span><span class="sxs-lookup"><span data-stu-id="6ea39-229">Configure optional features for a Dynamics 365 Commerce evaluation environment</span></span>](cpe-optional-features.md)

[<span data-ttu-id="6ea39-230">Veelgestelde vragen over evaluatieomgeving voor Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="6ea39-230">Dynamics 365 Commerce evaluation environment FAQ</span></span>](cpe-faq.md)

[<span data-ttu-id="6ea39-231">Microsoft Lifecycle Services (LCS)</span><span class="sxs-lookup"><span data-stu-id="6ea39-231">Microsoft Lifecycle Services (LCS)</span></span>](/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[<span data-ttu-id="6ea39-232">Commerce Scale Unit (cloud)</span><span class="sxs-lookup"><span data-stu-id="6ea39-232">Commerce Scale Unit (cloud)</span></span>](/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[<span data-ttu-id="6ea39-233">Microsoft Azure-portal</span><span class="sxs-lookup"><span data-stu-id="6ea39-233">Microsoft Azure portal</span></span>](https://azure.microsoft.com/features/azure-portal)

[<span data-ttu-id="6ea39-234">Dynamics 365 Commerce-website</span><span class="sxs-lookup"><span data-stu-id="6ea39-234">Dynamics 365 Commerce website</span></span>](https://aka.ms/Dynamics365CommerceWebsite)


[!INCLUDE[footer-include](../includes/footer-banner.md)]