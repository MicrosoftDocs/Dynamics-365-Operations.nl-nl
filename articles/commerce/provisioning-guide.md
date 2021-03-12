---
title: Een evaluatieomgeving voor Dynamics 365 Commerce inrichten
description: In dit onderwerp wordt uitgelegd hoe u een evaluatieomgeving van Microsoft Dynamics 365 Commerce inricht.
author: psimolin
manager: annbe
ms.date: 12/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
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
ms.openlocfilehash: 8cda79a6be1aca7ad3826b9409e110524e6560e3
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2021
ms.locfileid: "4969896"
---
# <a name="provision-a-dynamics-365-commerce-evaluation-environment"></a><span data-ttu-id="ec7d5-103">Een evaluatieomgeving voor Dynamics 365 Commerce inrichten</span><span class="sxs-lookup"><span data-stu-id="ec7d5-103">Provision a Dynamics 365 Commerce evaluation environment</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="ec7d5-104">In dit onderwerp wordt uitgelegd hoe u een evaluatieomgeving van Microsoft Dynamics 365 Commerce inricht.</span><span class="sxs-lookup"><span data-stu-id="ec7d5-104">This topic explains how to provision a Microsoft Dynamics 365 Commerce evaluation environment.</span></span>

<span data-ttu-id="ec7d5-105">Voordat u begint, kunt u het beste dit onderwerp snel doorlezen om een idee te krijgen van wat nodig is voor het proces.</span><span class="sxs-lookup"><span data-stu-id="ec7d5-105">Before you begin, we recommend that you take a quick scan through this topic to get an idea of what the process requires.</span></span>

> [!NOTE]
> <span data-ttu-id="ec7d5-106">Commerce-evaluatieomgevingen zijn doorgaans niet beschikbaar en worden aan partners en klanten op aanvraag ter beschikking gesteld.</span><span class="sxs-lookup"><span data-stu-id="ec7d5-106">Commerce evaluation environments aren't generally available, and are granted to partners and customers on a per-request basis.</span></span> <span data-ttu-id="ec7d5-107">Neem contact op met uw Microsoft-partner voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="ec7d5-107">For more information, reach out to your Microsoft partner contact.</span></span>

## <a name="overview"></a><span data-ttu-id="ec7d5-108">Overzicht</span><span class="sxs-lookup"><span data-stu-id="ec7d5-108">Overview</span></span>

<span data-ttu-id="ec7d5-109">Als u uw evaluatieomgeving van Commerce wilt inrichten, moet u een project maken met een specifieke productnaam en een specifiek producttype.</span><span class="sxs-lookup"><span data-stu-id="ec7d5-109">To successfully provision a Commerce evaluation environment, you must create a project that has a specific product name and type.</span></span> <span data-ttu-id="ec7d5-110">De omgeving en Commerce Scale Unit (CSU) beschikken ook over specifieke parameters die u moet gebruiken wanneer u e-Commerce later wilt inrichten.</span><span class="sxs-lookup"><span data-stu-id="ec7d5-110">The environment and Commerce Scale Unit (CSU) also have some specific parameters that you must use when you expect to provision e-Commerce later.</span></span> <span data-ttu-id="ec7d5-111">De instructies in dit onderwerp beschrijven alle vereiste stappen voor het voltooien van de inrichting en de parameters die u moet gebruiken.</span><span class="sxs-lookup"><span data-stu-id="ec7d5-111">The instructions in this topic describe all the steps that are required to complete provisioning and the parameters that you must use.</span></span>

<span data-ttu-id="ec7d5-112">Nadat de inrichting van de evaluatieomgeving van Commerce is voltooid, moet u een aantal stappen uitvoeren om de preview-omgeving voor te bereiden.</span><span class="sxs-lookup"><span data-stu-id="ec7d5-112">After you successfully provision your Commerce evaluation environment, you must complete a few post-provisioning steps to prepare it for use.</span></span> <span data-ttu-id="ec7d5-113">Sommige stappen zijn optioneel, afhankelijk van de aspecten van het systeem die u wilt evalueren.</span><span class="sxs-lookup"><span data-stu-id="ec7d5-113">Some steps are optional, depending on the aspects of the system that you want to evaluate.</span></span> <span data-ttu-id="ec7d5-114">U kunt de optionele stappen altijd later voltooien.</span><span class="sxs-lookup"><span data-stu-id="ec7d5-114">You can always complete the optional steps later.</span></span>

<span data-ttu-id="ec7d5-115">Zie [Een evaluatieomgeving van Commerce configureren](cpe-post-provisioning.md) voor meer informatie over hoe u uw evaluatieomgeving voor Commerce configureert nadat u deze hebt ingericht.</span><span class="sxs-lookup"><span data-stu-id="ec7d5-115">For information about how to configure your Commerce evaluation environment after you provision it, see [Configure a Commerce evaluation environment](cpe-post-provisioning.md).</span></span> <span data-ttu-id="ec7d5-116">Zie [Optionele functies voor een evaluatieomgeving van Commerce configureren](cpe-optional-features.md) voor meer informatie over hoe u optionele functies voor uw evaluatieomgeving van Commerce configureert.</span><span class="sxs-lookup"><span data-stu-id="ec7d5-116">For information about how to configure optional features for your Commerce evaluation environment, see [Configure optional features for a Commerce evaluation environment](cpe-optional-features.md).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="ec7d5-117">Vereisten</span><span class="sxs-lookup"><span data-stu-id="ec7d5-117">Prerequisites</span></span>

<span data-ttu-id="ec7d5-118">Aan de volgende voorwaarden moeten zijn voldaan voordat u uw evaluatieomgeving van Commerce inricht:</span><span class="sxs-lookup"><span data-stu-id="ec7d5-118">The following prerequisites must be in place before you can provision your Commerce evaluation environment:</span></span>

- <span data-ttu-id="ec7d5-119">U bent geregistreerd voor het evaluatieprogramma en hebt capaciteit gekregen voor een evaluatieomgeving.</span><span class="sxs-lookup"><span data-stu-id="ec7d5-119">You have been onboarded into the evaluation program and granted capacity for an evaluation environment.</span></span>
- <span data-ttu-id="ec7d5-120">U hebt toegang tot de Microsoft Dynamics Lifecycle Services-portal (LCS).</span><span class="sxs-lookup"><span data-stu-id="ec7d5-120">You have access to the Microsoft Dynamics Lifecycle Services (LCS) portal.</span></span>
- <span data-ttu-id="ec7d5-121">U bent een bestaande Microsoft Dynamics 365-partner of -klant en kunt een Dynamics 365 Commerce-project maken.</span><span class="sxs-lookup"><span data-stu-id="ec7d5-121">You are an existing Microsoft Dynamics 365 partner or customer and are able to create a Dynamics 365 Commerce project.</span></span>
- <span data-ttu-id="ec7d5-122">U hebt beheerderstoegang tot uw Microsoft Azure-abonnement of u bent in contact met een abonnementsbeheerder die u kan helpen als dat nodig is.</span><span class="sxs-lookup"><span data-stu-id="ec7d5-122">You have administrator access to your Microsoft Azure subscription, or you're in contact with a subscription administrator who can assist you if required.</span></span>
- <span data-ttu-id="ec7d5-123">U hebt uw Azure Active Directory-tenant-id (Azure AD) bij de hand.</span><span class="sxs-lookup"><span data-stu-id="ec7d5-123">You have your Azure Active Directory (Azure AD) tenant ID available.</span></span>
- <span data-ttu-id="ec7d5-124">U hebt een Azure AD-beveiligingsgroep gemaakt om te gebruiken als e-Commerce-systeembeheerdersgroep en u hebt de id bij de hand.</span><span class="sxs-lookup"><span data-stu-id="ec7d5-124">You've created an Azure AD security group that can be used as an e-Commerce system admin group, and you have its ID available.</span></span>
- <span data-ttu-id="ec7d5-125">U hebt een Azure AD-beveiligingsgroep gemaakt om te gebruiken als moderatorgroep voor beoordelingen en recensies en u hebt de id bij de hand.</span><span class="sxs-lookup"><span data-stu-id="ec7d5-125">You've created an Azure AD security group that can be used as a Ratings and Reviews moderator group, and you have its ID available.</span></span> <span data-ttu-id="ec7d5-126">(Deze beveiligingsgroep kan dezelfde zijn als de systeembeheerdersgroep van e-Commerce.)</span><span class="sxs-lookup"><span data-stu-id="ec7d5-126">(This security group can be the same as the e-Commerce system admin group.)</span></span>

<span data-ttu-id="ec7d5-127">Deze lijst is niet volledig.</span><span class="sxs-lookup"><span data-stu-id="ec7d5-127">Note that this list isn't exhaustive.</span></span> <span data-ttu-id="ec7d5-128">Neem contact op met uw Microsoft-partner voor hulp als u problemen ondervindt.</span><span class="sxs-lookup"><span data-stu-id="ec7d5-128">If you experience any issues, reach out to your Microsoft partner contact for assistance.</span></span>

## <a name="provision-your-commerce-evaluation-environment"></a><span data-ttu-id="ec7d5-129">Uw evaluatieomgeving van Commerce inrichten</span><span class="sxs-lookup"><span data-stu-id="ec7d5-129">Provision your Commerce evaluation environment</span></span>

<span data-ttu-id="ec7d5-130">In deze procedures wordt uitgelegd hoe u een evaluatieomgeving van Commerce inricht.</span><span class="sxs-lookup"><span data-stu-id="ec7d5-130">These procedures explain how to provision a Commerce evaluation environment.</span></span> <span data-ttu-id="ec7d5-131">Als u dit hebt gedaan, is de evaluatieomgeving van Commerce gereed voor configuratie.</span><span class="sxs-lookup"><span data-stu-id="ec7d5-131">After you successfully complete them, the Commerce evaluation environment will be ready for configuration.</span></span> <span data-ttu-id="ec7d5-132">Alle activiteiten die hier worden beschreven, vinden plaats in de LCS-portal.</span><span class="sxs-lookup"><span data-stu-id="ec7d5-132">All the activities that are described here occur in the LCS portal.</span></span>

### <a name="create-a-new-project"></a><span data-ttu-id="ec7d5-133">Een nieuw project maken</span><span class="sxs-lookup"><span data-stu-id="ec7d5-133">Create a new project</span></span>

<span data-ttu-id="ec7d5-134">Ga als volgt te werk om een nieuw project te maken in LCS.</span><span class="sxs-lookup"><span data-stu-id="ec7d5-134">To create a new project in LCS, follow these steps.</span></span>

1. <span data-ttu-id="ec7d5-135">Selecteer op de LCS-startpagina het plusteken (**+**) om een project te maken.</span><span class="sxs-lookup"><span data-stu-id="ec7d5-135">On the LCS home page, select the plus sign (**+**) to create a project.</span></span>
1. <span data-ttu-id="ec7d5-136">Volg een van de volgende stappen uit in het rechterdeelvenster:</span><span class="sxs-lookup"><span data-stu-id="ec7d5-136">In the right pane, follow one of these steps:</span></span>

    - <span data-ttu-id="ec7d5-137">Als u een partner bent, selecteert u **Migreren, oplossingen maken en informatie over**.</span><span class="sxs-lookup"><span data-stu-id="ec7d5-137">If you're a partner, select **Migrate, create solutions, and learn**.</span></span>
    - <span data-ttu-id="ec7d5-138">Als u een klant bent, selecteert u **Potentiële presales**.</span><span class="sxs-lookup"><span data-stu-id="ec7d5-138">If you're a customer, select **Prospective presales**.</span></span>

1. <span data-ttu-id="ec7d5-139">Voer een naam, beschrijving en branche in.</span><span class="sxs-lookup"><span data-stu-id="ec7d5-139">Enter a name, description, and industry.</span></span>
1. <span data-ttu-id="ec7d5-140">Selecteer **Dynamics 365 Commerce** in het veld **Productnaam**.</span><span class="sxs-lookup"><span data-stu-id="ec7d5-140">In the **Product name** field, select **Dynamics 365 Commerce**.</span></span>
1. <span data-ttu-id="ec7d5-141">Selecteer **Dynamics 365 Commerce** in het veld **Productversie**.</span><span class="sxs-lookup"><span data-stu-id="ec7d5-141">In the **Product version** field, select **Dynamics 365 Commerce**.</span></span>
1. <span data-ttu-id="ec7d5-142">Selecteer **Implementatiemethodologie voor Dynamics Retail** in het veld **Methodologie**.</span><span class="sxs-lookup"><span data-stu-id="ec7d5-142">In the **Methodology** field, select **Dynamics Retail implementation methodology**.</span></span>
1. <span data-ttu-id="ec7d5-143">Optioneel: u kunt rollen en gebruikers importeren uit bestaand project.</span><span class="sxs-lookup"><span data-stu-id="ec7d5-143">Optional: You can import roles and users from an existing project.</span></span>
1. <span data-ttu-id="ec7d5-144">Selecteer **Maken**.</span><span class="sxs-lookup"><span data-stu-id="ec7d5-144">Select **Create**.</span></span> <span data-ttu-id="ec7d5-145">De projectweergave wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="ec7d5-145">The project view appears.</span></span>

### <a name="add-the-azure-connector"></a><span data-ttu-id="ec7d5-146">De Azure-connector toevoegen</span><span class="sxs-lookup"><span data-stu-id="ec7d5-146">Add the Azure Connector</span></span>

<span data-ttu-id="ec7d5-147">Om de Azure-connector aan uw LCS-project toe te voegen volgt u de stappen in de procedure voor [het voltooien van het onboardingproces van Azure Resource Manager (ARM)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/arm-onboarding).</span><span class="sxs-lookup"><span data-stu-id="ec7d5-147">To add the Azure Connector to your LCS project, follow the steps in [Complete the Azure Resource Manager (ARM) onboarding process](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/arm-onboarding).</span></span>

### <a name="deploy-the-environment"></a><span data-ttu-id="ec7d5-148">De omgeving implementeren</span><span class="sxs-lookup"><span data-stu-id="ec7d5-148">Deploy the environment</span></span>

<span data-ttu-id="ec7d5-149">Ga als volgt te werk om de omgeving te implementeren.</span><span class="sxs-lookup"><span data-stu-id="ec7d5-149">To deploy the environment, follow these steps.</span></span>

> [!NOTE]
> <span data-ttu-id="ec7d5-150">Het is mogelijk dat u de stappen 6, 7 en/of 8 niet hoeft te voltooien, omdat pagina's met één optie worden overgeslagen.</span><span class="sxs-lookup"><span data-stu-id="ec7d5-150">You might not have to complete steps 6, 7, and/or 8, because pages that have a single option are skipped.</span></span> <span data-ttu-id="ec7d5-151">Controleer in de weergave **Omgevingsparameters** of u de tekst **Dynamics 365 Commerce - Demo (10.0.* x* met Platform update *xx*)\*\* direct boven het veld **Omgevingsnaam** ziet.</span><span class="sxs-lookup"><span data-stu-id="ec7d5-151">When you're in the **Environment parameters** view, confirm that the text **Dynamics 365 Commerce - Demo (10.0.* x* with Platform update *xx*)\*\* appears directly above the **Environment name** field.</span></span> <span data-ttu-id="ec7d5-152">Zie de afbeelding die na stap 8 wordt weergegeven voor nadere details.</span><span class="sxs-lookup"><span data-stu-id="ec7d5-152">For details, see the illustration that appears after step 8.</span></span>

1. <span data-ttu-id="ec7d5-153">Selecteer in het bovenste menu de optie **Cloudomgevingen**.</span><span class="sxs-lookup"><span data-stu-id="ec7d5-153">On the top menu, select **Cloud-hosted environments**.</span></span>
1. <span data-ttu-id="ec7d5-154">Selecteer **Toevoegen** om een omgeving toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="ec7d5-154">Select **Add** to add an environment.</span></span>
1. <span data-ttu-id="ec7d5-155">Selecteer in het veld **Toepassingsversie** de meest recente versie.</span><span class="sxs-lookup"><span data-stu-id="ec7d5-155">In the **Application version** field, select the most current version.</span></span> <span data-ttu-id="ec7d5-156">Als u specifiek een andere toepassingsversie dan de meest recente versie wilt selecteren, moet u geen eerdere versie dan **10.0.14** selecteren.</span><span class="sxs-lookup"><span data-stu-id="ec7d5-156">If you have a specific need to select an application version other than the most current version, do not select a version prior to **10.0.14**.</span></span>
1. <span data-ttu-id="ec7d5-157">Gebruik in het veld **Platformversie** de platform versie die automatisch wordt gekozen voor de toepassingsversie die u hebt geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="ec7d5-157">In the **Platform version** field, use the platform version that is automatically chosen for the application version you selected.</span></span> 

    ![Toepassings- en platformversies selecteren](./media/project1.png)

1. <span data-ttu-id="ec7d5-159">Selecteer **Volgende**.</span><span class="sxs-lookup"><span data-stu-id="ec7d5-159">Select **Next**.</span></span>
1. <span data-ttu-id="ec7d5-160">Selecteer **Demo** als de omgevingstopologie.</span><span class="sxs-lookup"><span data-stu-id="ec7d5-160">Select **Demo** as the environment topology.</span></span>

    ![De omgevingstopologie 1 selecteren](./media/project2.png)

1. <span data-ttu-id="ec7d5-162">Voer op de pagina **Omgeving implementeren** een omgevingsnaam in.</span><span class="sxs-lookup"><span data-stu-id="ec7d5-162">On the **Deploy environment** page, enter an environment name.</span></span> <span data-ttu-id="ec7d5-163">Laat geavanceerde instellingen ongewijzigd.</span><span class="sxs-lookup"><span data-stu-id="ec7d5-163">Leave the advanced settings as they are.</span></span>

    ![De pagina Omgeving implementeren](./media/project4.png)

1. <span data-ttu-id="ec7d5-165">Pas de VM-grootte naar wens aan.</span><span class="sxs-lookup"><span data-stu-id="ec7d5-165">Adjust the VM size as required.</span></span> <span data-ttu-id="ec7d5-166">(We raden VM-voorraadeenheid \[SKU\] **D13 v2** aan.)</span><span class="sxs-lookup"><span data-stu-id="ec7d5-166">(We recommend VM stock keeping unit \[SKU\] **D13 v2**.)</span></span>
1. <span data-ttu-id="ec7d5-167">Controleer de prijs- en licentievoorwaarden en schakel vervolgens het selectievakje in om aan te geven dat u ermee instemt.</span><span class="sxs-lookup"><span data-stu-id="ec7d5-167">Review the pricing and licensing terms, and then select the check box to indicate that you agree to them.</span></span>
1. <span data-ttu-id="ec7d5-168">Selecteer **Volgende**.</span><span class="sxs-lookup"><span data-stu-id="ec7d5-168">Select **Next**.</span></span>
1. <span data-ttu-id="ec7d5-169">Controleer op de bevestigingspagina voor de implementatie of de details juist zijn en klik op **Implementeren**.</span><span class="sxs-lookup"><span data-stu-id="ec7d5-169">On the deployment confirmation page, verify that the details are correct, and then select **Deploy**.</span></span> <span data-ttu-id="ec7d5-170">U keert terug naar de weergave in **Cloudomgevingen** en uw omgeving wordt weergegeven in de lijst.</span><span class="sxs-lookup"><span data-stu-id="ec7d5-170">You're returned to the **Cloud-hosted environments** view, and your environment should appear in the list.</span></span>

    <span data-ttu-id="ec7d5-171">Uw aangevraagde omgeving wordt weergegeven in de wachtrij en vervolgens geïmplementeerd.</span><span class="sxs-lookup"><span data-stu-id="ec7d5-171">Your requested environment will appear as queued and then deploying.</span></span> <span data-ttu-id="ec7d5-172">Het duurt even voordat de werkstromen van de omgeving zijn voltooid.</span><span class="sxs-lookup"><span data-stu-id="ec7d5-172">The environment workflows will take some time to be completed.</span></span> <span data-ttu-id="ec7d5-173">Controleer dit daarom na ongeveer zes tot negen uur.</span><span class="sxs-lookup"><span data-stu-id="ec7d5-173">Therefore, check back after approximately six to nine hours.</span></span>

1. <span data-ttu-id="ec7d5-174">Voordat u verdergaat, moet u controleren of de omgevingsstatus **Geïmplementeerd** is.</span><span class="sxs-lookup"><span data-stu-id="ec7d5-174">Before you continue, make sure that the status of your environment is **Deployed**.</span></span>

### <a name="initialize-the-commerce-scale-unit-cloud"></a><span data-ttu-id="ec7d5-175">Commerce Scale Unit initialiseren (cloud)</span><span class="sxs-lookup"><span data-stu-id="ec7d5-175">Initialize the Commerce Scale Unit (cloud)</span></span>

<span data-ttu-id="ec7d5-176">Ga als volgt te werk om de CSU te initialiseren.</span><span class="sxs-lookup"><span data-stu-id="ec7d5-176">To initialize the CSU, follow these steps.</span></span>

1. <span data-ttu-id="ec7d5-177">Selecteer in de weergave **Cloudomgevingen** uw omgeving in de lijst.</span><span class="sxs-lookup"><span data-stu-id="ec7d5-177">In the **Cloud-hosted environments** view, select your environment in the list.</span></span>
1. <span data-ttu-id="ec7d5-178">Klik op **Volledige details** in de omgevingsweergave rechts.</span><span class="sxs-lookup"><span data-stu-id="ec7d5-178">In the environment view on the right, select **Full details**.</span></span> <span data-ttu-id="ec7d5-179">De weergave met omgevingsdetails wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="ec7d5-179">The environment details view appears.</span></span>
1. <span data-ttu-id="ec7d5-180">Selecteer **Beheren** onder **Omgevingsfuncties**.</span><span class="sxs-lookup"><span data-stu-id="ec7d5-180">Under **Environment features**, select **Manage**.</span></span>
1. <span data-ttu-id="ec7d5-181">Selecteer **Initialiseren** op het tabblad **Commerce**.</span><span class="sxs-lookup"><span data-stu-id="ec7d5-181">On the **Commerce** tab, select **Initialize**.</span></span> <span data-ttu-id="ec7d5-182">De weergave CSU-initialisatieparameters wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="ec7d5-182">The CSU initialization parameters view appears.</span></span>
1. <span data-ttu-id="ec7d5-183">Selecteer in het veld **Regio** de regio die gelijk is aan of dichtbij de regio waar u de omgeving hebt geïmplementeerd.</span><span class="sxs-lookup"><span data-stu-id="ec7d5-183">In the **Region** field, select the region that is the same or close to the region that you deployed the environment to.</span></span>
1. <span data-ttu-id="ec7d5-184">Laat het veld **Versie** ongewijzigd.</span><span class="sxs-lookup"><span data-stu-id="ec7d5-184">Leave the **Version** field as it is.</span></span>
1. <span data-ttu-id="ec7d5-185">Selecteer **Initialiseren**.</span><span class="sxs-lookup"><span data-stu-id="ec7d5-185">Select **Initialize**.</span></span>
1. <span data-ttu-id="ec7d5-186">Controleer op de bevestigingspagina voor de implementatie of de details juist zijn en klik op **Ja**.</span><span class="sxs-lookup"><span data-stu-id="ec7d5-186">On the deployment confirmation page, verify that the details are correct, and then select **Yes**.</span></span> <span data-ttu-id="ec7d5-187">De weergave **Commerce-beheer** wordt opnieuw weergegeven, waarbij het tabblad **Commerce** is geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="ec7d5-187">The **Commerce management** view displays again, where the **Commerce** tab is selected.</span></span> <span data-ttu-id="ec7d5-188">Uw CSU is in de wachtrij geplaatst voor inrichting.</span><span class="sxs-lookup"><span data-stu-id="ec7d5-188">Your CSU has been queued for provisioning.</span></span>
1. <span data-ttu-id="ec7d5-189">Voordat u verdergaat, moet u controleren of de CSU-status **Gelukt** is.</span><span class="sxs-lookup"><span data-stu-id="ec7d5-189">Before you continue, make sure that the status of your CSU is **Success**.</span></span> <span data-ttu-id="ec7d5-190">Initialisatie duurt ongeveer twee tot vijf uur.</span><span class="sxs-lookup"><span data-stu-id="ec7d5-190">Initialization takes approximately two to five hours.</span></span>

<span data-ttu-id="ec7d5-191">Als u de koppeling **Beheren** niet kunt vinden in de weergave met omgevingsdetails, neemt u contact op met Microsoft voor hulp.</span><span class="sxs-lookup"><span data-stu-id="ec7d5-191">If you can't find the **Manage** link in the environment details view, reach out to your Microsoft contact for assistance.</span></span>

<span data-ttu-id="ec7d5-192">Mogelijk wordt het volgende foutbericht weergegeven tijdens het implementatieproces:</span><span class="sxs-lookup"><span data-stu-id="ec7d5-192">During the deployment process, you might receive the following error message:</span></span>

> <span data-ttu-id="ec7d5-193">Voor evaluatieomgevingen (demo/test) moet de connectortoepassing voor schaaleenheden \<application ID\> in Headquarters worden geregistreerd.</span><span class="sxs-lookup"><span data-stu-id="ec7d5-193">Evaluation (demo/test) environments need to register the scale unit connector application \<application ID\> in headquarters.</span></span>

<span data-ttu-id="ec7d5-194">Als de CSU-initialisatie mislukt en u dit foutbericht ontvangt, noteert u de toepassings-id (een GUID) en volg vervolgens de stappen in de volgende sectie om de CSU-implementatietoepassing in Commerce Headquarters te registreren.</span><span class="sxs-lookup"><span data-stu-id="ec7d5-194">If the CSU initialization fails and you receive this error message, make a note of the application ID, which is a globally unique identifier (GUID), and then follow the steps in the next section to register the CSU deployment application in Commerce headquarters.</span></span>

### <a name="register-the-csu-deployment-application-in-commerce-headquarters-if-required"></a><span data-ttu-id="ec7d5-195">De CSU-implementatietoepassing in Commerce Headquarters registreren (indien nodig)</span><span class="sxs-lookup"><span data-stu-id="ec7d5-195">Register the CSU deployment application in Commerce headquarters (if required)</span></span>

<span data-ttu-id="ec7d5-196">Voer de volgende stappen uit om de CSU-implementatietoepassing in Commerce Headquarters te registreren.</span><span class="sxs-lookup"><span data-stu-id="ec7d5-196">To register the CSU deployment application in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="ec7d5-197">Ga in Commerce Headquarters naar **Systeembeheer \> Instellen \> Azure Active Directory-toepassingen**.</span><span class="sxs-lookup"><span data-stu-id="ec7d5-197">In Commerce headquarters, go to **System administration \> Setup \> Azure Active Directory applications**.</span></span>
1. <span data-ttu-id="ec7d5-198">Voer in de kolom **Client-id** de toepassings-id uit het foutbericht voor CSU-initialisatie in dat u hebt ontvangen.</span><span class="sxs-lookup"><span data-stu-id="ec7d5-198">In the **Client Id** column, enter the application ID from the CSU initialization error message that you received.</span></span>
1. <span data-ttu-id="ec7d5-199">Voer in de kolom **Naam** een beschrijvende tekst in (bijvoorbeeld **CSU-eval**).</span><span class="sxs-lookup"><span data-stu-id="ec7d5-199">In the **Name** column, enter any descriptive text (for example, **CSU Eval**).</span></span>
1. <span data-ttu-id="ec7d5-200">Voer in de kolom **Gebruikers-id** de tekst **RetailServiceAccount** in.</span><span class="sxs-lookup"><span data-stu-id="ec7d5-200">In the **User ID** column, enter **RetailServiceAccount**.</span></span>
1. <span data-ttu-id="ec7d5-201">Probeer de CSU-initialisatie en -implementatie opnieuw uit te voeren vanuit LCS.</span><span class="sxs-lookup"><span data-stu-id="ec7d5-201">Retry the CSU initialization and deployment from LCS.</span></span>

### <a name="initialize-e-commerce"></a><span data-ttu-id="ec7d5-202">e-Commerce initialiseren</span><span class="sxs-lookup"><span data-stu-id="ec7d5-202">Initialize e-Commerce</span></span>

<span data-ttu-id="ec7d5-203">Ga als volgt te werk om e-Commerce te initialiseren.</span><span class="sxs-lookup"><span data-stu-id="ec7d5-203">To initialize e-Commerce, follow these steps.</span></span>

1. <span data-ttu-id="ec7d5-204">Controleer op het tabblad **e-Commerce** de toestemming voor de evaluatie en selecteer vervolgens **Instellen**.</span><span class="sxs-lookup"><span data-stu-id="ec7d5-204">On the **e-Commerce** tab, review the evaluation consent, and then select **Setup**.</span></span>
1. <span data-ttu-id="ec7d5-205">Voer een naam in bij **Omgevingsnaam e-Commerce**.</span><span class="sxs-lookup"><span data-stu-id="ec7d5-205">In the **e-Commerce environment name** field, enter a name.</span></span> <span data-ttu-id="ec7d5-206">Houd er rekening mee dat deze naam wordt weergegeven in sommige URL's die naar uw e-Commerce-exemplaar verwijzen.</span><span class="sxs-lookup"><span data-stu-id="ec7d5-206">Be aware that this name will appear in some of the URLs that point to your e-Commerce instance.</span></span>
1. <span data-ttu-id="ec7d5-207">Selecteer in het veld **Naam Commerce Scale Unit** uw CSU in de lijst.</span><span class="sxs-lookup"><span data-stu-id="ec7d5-207">In the **Commerce Scale Unit name** field, select your CSU in the list.</span></span> <span data-ttu-id="ec7d5-208">(De lijst moet slechts één optie hebben.)</span><span class="sxs-lookup"><span data-stu-id="ec7d5-208">(The list should have only one option.)</span></span>

    <span data-ttu-id="ec7d5-209">Het veld **Geografie van e-Commerce** wordt automatisch ingesteld.</span><span class="sxs-lookup"><span data-stu-id="ec7d5-209">The **e-Commerce geography** field is set automatically.</span></span>

1. <span data-ttu-id="ec7d5-210">Selecteer **Volgende** om door te gaan.</span><span class="sxs-lookup"><span data-stu-id="ec7d5-210">Select **Next** to continue.</span></span>
1. <span data-ttu-id="ec7d5-211">Voer in het veld **Ondersteunde hostnamen** een geldig domein in, bijvoorbeeld `www.fabrikam.com`.</span><span class="sxs-lookup"><span data-stu-id="ec7d5-211">In the **Supported host names** field, enter any valid domain, such as `www.fabrikam.com`.</span></span>
1. <span data-ttu-id="ec7d5-212">Voer in het veld **AAD-beveiligingsgroep voor systeembeheer** de eerste paar letters van de naam van de beveiligingsgroep in die u wilt gebruiken en selecteer vervolgens het vergrootglassymbool om de zoekresultaten weer te geven.</span><span class="sxs-lookup"><span data-stu-id="ec7d5-212">In the **AAD security group for system admin** field, enter the first few letters of the name of the security group that you want to use, and then select the magnifying glass symbol to view the search results.</span></span> <span data-ttu-id="ec7d5-213">Selecteer de juiste beveiligingsgroep in de lijst.</span><span class="sxs-lookup"><span data-stu-id="ec7d5-213">Select the correct security group in the list.</span></span>
1.  <span data-ttu-id="ec7d5-214">Voer in het veld **AAD-beveiligingsgroep voor moderator van beoordelingen en recensies** de eerste paar letters van de naam van de beveiligingsgroep in die u wilt gebruiken en selecteer vervolgens het vergrootglassymbool om de zoekresultaten weer te geven.</span><span class="sxs-lookup"><span data-stu-id="ec7d5-214">In the **AAD security group for ratings and review moderator** field, enter the first few letters of the name of the security group that you want to use, and then select the magnifying glass symbol to view the search results.</span></span> <span data-ttu-id="ec7d5-215">Selecteer de juiste beveiligingsgroep in de lijst.</span><span class="sxs-lookup"><span data-stu-id="ec7d5-215">Select the correct security group in the list.</span></span>
1. <span data-ttu-id="ec7d5-216">Laat de optie **Service voor beoordelingen en recensies inschakelen** op **Ja** staan.</span><span class="sxs-lookup"><span data-stu-id="ec7d5-216">Leave the **Enable ratings and review service** option set to **Yes**.</span></span>
1. <span data-ttu-id="ec7d5-217">Selecteer **Initialiseren**.</span><span class="sxs-lookup"><span data-stu-id="ec7d5-217">Select **Initialize**.</span></span> <span data-ttu-id="ec7d5-218">De weergave **Commerce-beheer** wordt opnieuw weergegeven, waarbij het tabblad **e-Commerce** is geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="ec7d5-218">The **Commerce management** view displays again, where the **e-Commerce** tab is selected.</span></span> <span data-ttu-id="ec7d5-219">De initialisatie van e-Commerce is gestart.</span><span class="sxs-lookup"><span data-stu-id="ec7d5-219">E-Commerce initialization has started.</span></span>
1. <span data-ttu-id="ec7d5-220">Voordat u verdergaat, moet u wachten tot de initialisatiestatus van e-Commerce **Geïnitieerd** is.</span><span class="sxs-lookup"><span data-stu-id="ec7d5-220">Before you continue, wait until the status of e-Commerce initialization is **Initialization successful**.</span></span>
1. <span data-ttu-id="ec7d5-221">Let onder **Koppeling** in de rechterbenedenhoek op de URL's voor de volgende koppelingen en noteer deze:</span><span class="sxs-lookup"><span data-stu-id="ec7d5-221">Under **Links** in the lower right, make a note of the URLs for the following links:</span></span>

    * <span data-ttu-id="ec7d5-222">**e-Commerce-site**: de koppeling naar de hoofdmap van uw e-Commerce-site.</span><span class="sxs-lookup"><span data-stu-id="ec7d5-222">**e-Commerce site** – The link to the root of your e-Commerce site.</span></span>
    * <span data-ttu-id="ec7d5-223">**Commerce Site Builder**: de koppeling naar het beheerhulpprogramma van de site.</span><span class="sxs-lookup"><span data-stu-id="ec7d5-223">**Commerce site builder** – The link to the site management tool.</span></span>

## <a name="next-steps"></a><span data-ttu-id="ec7d5-224">Volgende stappen</span><span class="sxs-lookup"><span data-stu-id="ec7d5-224">Next steps</span></span>

<span data-ttu-id="ec7d5-225">Zie [Een evaluatieomgeving van Commerce configureren](cpe-post-provisioning.md) om door te gaan met het inrichten en configureren van uw evaluatieomgeving voor Commerce.</span><span class="sxs-lookup"><span data-stu-id="ec7d5-225">To continue the process of provisioning and configuring your Commerce evaluation environment, see [Configure a Commerce evaluation environment](cpe-post-provisioning.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ec7d5-226">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="ec7d5-226">Additional resources</span></span>

[<span data-ttu-id="ec7d5-227">Overzicht van de evaluatieomgeving voor Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="ec7d5-227">Dynamics 365 Commerce evaluation environment overview</span></span>](cpe-overview.md)

[<span data-ttu-id="ec7d5-228">Een Dynamics 365 Commerce-evaluatieomgeving configureren</span><span class="sxs-lookup"><span data-stu-id="ec7d5-228">Configure a Dynamics 365 Commerce evaluation environment</span></span>](cpe-post-provisioning.md)

[<span data-ttu-id="ec7d5-229">BOPIS configureren in een Dynamics 365 Commerce-evaluatieomgeving</span><span class="sxs-lookup"><span data-stu-id="ec7d5-229">Configure BOPIS in a Dynamics 365 Commerce evaluation environment</span></span>](cpe-bopis.md)

[<span data-ttu-id="ec7d5-230">Optionele functies voor een Dynamics 365 Commerce-evaluatieomgeving configureren</span><span class="sxs-lookup"><span data-stu-id="ec7d5-230">Configure optional features for a Dynamics 365 Commerce evaluation environment</span></span>](cpe-optional-features.md)

[<span data-ttu-id="ec7d5-231">Veelgestelde vragen over evaluatieomgeving voor Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="ec7d5-231">Dynamics 365 Commerce evaluation environment FAQ</span></span>](cpe-faq.md)

[<span data-ttu-id="ec7d5-232">Microsoft Lifecycle Services (LCS)</span><span class="sxs-lookup"><span data-stu-id="ec7d5-232">Microsoft Lifecycle Services (LCS)</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[<span data-ttu-id="ec7d5-233">Commerce Scale Unit (cloud)</span><span class="sxs-lookup"><span data-stu-id="ec7d5-233">Commerce Scale Unit (cloud)</span></span>](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[<span data-ttu-id="ec7d5-234">Microsoft Azure-portal</span><span class="sxs-lookup"><span data-stu-id="ec7d5-234">Microsoft Azure portal</span></span>](https://azure.microsoft.com/features/azure-portal)

[<span data-ttu-id="ec7d5-235">Dynamics 365 Commerce-website</span><span class="sxs-lookup"><span data-stu-id="ec7d5-235">Dynamics 365 Commerce website</span></span>](https://aka.ms/Dynamics365CommerceWebsite)
