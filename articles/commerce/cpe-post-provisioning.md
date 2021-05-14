---
title: Een Dynamics 365 Commerce-evaluatieomgeving configureren
description: In dit onderwerp wordt uitgelegd hoe u een evaluatieomgeving van Microsoft Dynamics 365 Commerce configureert na inrichting.
author: psimolin
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-12-10
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: b291a6515c6a3ae7382ea2ad8024ca036489de19
ms.sourcegitcommit: 9eadc7ca08e2db3fd208f5fc835551abe9d06dc8
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/22/2021
ms.locfileid: "5937033"
---
# <a name="configure-a-dynamics-365-commerce-evaluation-environment"></a><span data-ttu-id="a68cc-103">Een Dynamics 365 Commerce-evaluatieomgeving configureren</span><span class="sxs-lookup"><span data-stu-id="a68cc-103">Configure a Dynamics 365 Commerce evaluation environment</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="a68cc-104">In dit onderwerp wordt uitgelegd hoe u een evaluatieomgeving van Microsoft Dynamics 365 Commerce configureert na inrichting.</span><span class="sxs-lookup"><span data-stu-id="a68cc-104">This topic explains how to configure a Microsoft Dynamics 365 Commerce evaluation environment after it's provisioned.</span></span>

<span data-ttu-id="a68cc-105">Voltooi de procedures in dit onderwerp pas nadat uw evaluatieomgeving van Commerce is ingericht.</span><span class="sxs-lookup"><span data-stu-id="a68cc-105">Complete the procedures in this topic only after your Commerce evaluation environment has been provisioned.</span></span> <span data-ttu-id="a68cc-106">Zie [Een evaluatieomgeving van Commerce inrichten](provisioning-guide.md) voor meer informatie over hoe u uw evaluatieomgeving van Commerce inricht.</span><span class="sxs-lookup"><span data-stu-id="a68cc-106">For information about how to provision your Commerce evaluation environment, see [Provision a Commerce evaluation environment](provisioning-guide.md).</span></span>

<span data-ttu-id="a68cc-107">Nadat uw evaluatieomgeving van Commerce end-to-end is ingericht, moeten extra configuratiestappen worden voltooid voordat u kunt beginnen met het evalueren van de omgeving.</span><span class="sxs-lookup"><span data-stu-id="a68cc-107">After your Commerce evaluation environment has been provisioned end to end, additional post-provisioning configuration steps must be completed before you can start to evaluate the environment.</span></span> <span data-ttu-id="a68cc-108">Als u deze stappen wilt uitvoeren, moet u Microsoft Dynamics Lifecycle Services (LCS) en Dynamics 365 Commerce gebruiken.</span><span class="sxs-lookup"><span data-stu-id="a68cc-108">To complete these steps, you must use Microsoft Dynamics Lifecycle Services (LCS) and Dynamics 365 Commerce.</span></span>

## <a name="before-you-start"></a><span data-ttu-id="a68cc-109">Voordat u begint</span><span class="sxs-lookup"><span data-stu-id="a68cc-109">Before you start</span></span>

1. <span data-ttu-id="a68cc-110">Meld u aan bij de [LCS-portal](https://lcs.dynamics.com).</span><span class="sxs-lookup"><span data-stu-id="a68cc-110">Sign in to the [LCS portal](https://lcs.dynamics.com).</span></span>
1. <span data-ttu-id="a68cc-111">Ga naar uw project.</span><span class="sxs-lookup"><span data-stu-id="a68cc-111">Go to your project.</span></span>
1. <span data-ttu-id="a68cc-112">Selecteer in het bovenste menu de optie **Cloudomgevingen**.</span><span class="sxs-lookup"><span data-stu-id="a68cc-112">On the top menu, select **Cloud-hosted environments**.</span></span>
1. <span data-ttu-id="a68cc-113">Selecteer uw omgeving in de lijst.</span><span class="sxs-lookup"><span data-stu-id="a68cc-113">Select your environment in the list.</span></span>
1. <span data-ttu-id="a68cc-114">Klik op **Aanmelden bij omgeving** in de omgevingsgegevens rechts.</span><span class="sxs-lookup"><span data-stu-id="a68cc-114">In the environment information on the right, select **Log on to environment**.</span></span> <span data-ttu-id="a68cc-115">U wordt doorgestuurd naar Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="a68cc-115">You will be sent to Commerce headquarters.</span></span>
1. <span data-ttu-id="a68cc-116">Zorg ervoor dat de rechtspersoon **USRT** is geselecteerd rechtsboven.</span><span class="sxs-lookup"><span data-stu-id="a68cc-116">Make sure that the **USRT** legal entity is selected in the upper-right corner.</span></span>

<span data-ttu-id="a68cc-117">Controleer tijdens het activiteiten na het inrichting in Commerce Headquarters of de rechtspersoon **USRT** altijd is geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="a68cc-117">During post-provisioning activities in Commerce headquarters, make sure that the **USRT** legal entity is always selected.</span></span>

## <a name="configure-the-point-of-sale"></a><span data-ttu-id="a68cc-118">Het verkooppunt configureren</span><span class="sxs-lookup"><span data-stu-id="a68cc-118">Configure the point of sale</span></span>

### <a name="associate-a-worker-with-your-identity"></a><span data-ttu-id="a68cc-119">Een medewerker aan uw identiteit koppelen</span><span class="sxs-lookup"><span data-stu-id="a68cc-119">Associate a worker with your identity</span></span>

<span data-ttu-id="a68cc-120">Ga als volgt te werk om een medewerker te koppelen aan uw identiteit in Commerce Headquarters</span><span class="sxs-lookup"><span data-stu-id="a68cc-120">To associate a worker with your identity, follow these steps in Commerce headquarters.</span></span>

1. <span data-ttu-id="a68cc-121">Ga in het menu links naar **Modules \> Detailhandel en commerce \> Werknemers \> Medewerkers**.</span><span class="sxs-lookup"><span data-stu-id="a68cc-121">Use the menu on the left to go to **Modules \> Retail and commerce \> Employees \> Workers**.</span></span>
1. <span data-ttu-id="a68cc-122">Zoek en selecteer record **000713 - Andrew Collette**.</span><span class="sxs-lookup"><span data-stu-id="a68cc-122">In the list, find and select the following record: **000713 - Andrew Collette**.</span></span>
1. <span data-ttu-id="a68cc-123">Selecteer in het actievenster de optie **Commerce**.</span><span class="sxs-lookup"><span data-stu-id="a68cc-123">On the Action Pane, select **Commerce**.</span></span>
1. <span data-ttu-id="a68cc-124">Selecteer **Bestaande identiteit koppelen**.</span><span class="sxs-lookup"><span data-stu-id="a68cc-124">Select **Associate existing identity**.</span></span>
1. <span data-ttu-id="a68cc-125">Typ uw e-mailadres in het veld **E-mail** rechts van **Zoeken met behulp van e-mail**.</span><span class="sxs-lookup"><span data-stu-id="a68cc-125">In the **Email** field to the right of **Search using email**, enter your email address.</span></span>
1. <span data-ttu-id="a68cc-126">Selecteer **Zoeken**.</span><span class="sxs-lookup"><span data-stu-id="a68cc-126">Select **Search**.</span></span>
1. <span data-ttu-id="a68cc-127">Selecteer de record met uw naam.</span><span class="sxs-lookup"><span data-stu-id="a68cc-127">Select the record that has your name.</span></span>
1. <span data-ttu-id="a68cc-128">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="a68cc-128">Select **OK**.</span></span>
1. <span data-ttu-id="a68cc-129">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="a68cc-129">Select **Save**.</span></span>

### <a name="activate-cloud-pos"></a><span data-ttu-id="a68cc-130">Cloud POS activeren</span><span class="sxs-lookup"><span data-stu-id="a68cc-130">Activate Cloud POS</span></span>

<span data-ttu-id="a68cc-131">Ga als volgt te werk om Cloud POS in LCS te activeren.</span><span class="sxs-lookup"><span data-stu-id="a68cc-131">To activate Cloud POS, follow these steps in LCS.</span></span>

1. <span data-ttu-id="a68cc-132">Selecteer in het bovenste menu de optie **Cloudomgevingen**.</span><span class="sxs-lookup"><span data-stu-id="a68cc-132">On the top menu, select **Cloud-hosted environments**.</span></span>
1. <span data-ttu-id="a68cc-133">Selecteer uw omgeving in de lijst.</span><span class="sxs-lookup"><span data-stu-id="a68cc-133">Select your environment in the list.</span></span>
1. <span data-ttu-id="a68cc-134">Klik op **Aanmelden bij cloud-verkooppunt** in de omgevingsgegevens rechts.</span><span class="sxs-lookup"><span data-stu-id="a68cc-134">In the environment information on the right, select **Log on to Cloud Point of Sale**.</span></span>
1. <span data-ttu-id="a68cc-135">Klik op **Volgende** om het dialoogvenster **Voordat u begint** te openen.</span><span class="sxs-lookup"><span data-stu-id="a68cc-135">Select **Next** to open the **Before you start** dialog box.</span></span>
1. <span data-ttu-id="a68cc-136">Laat het veld **Server-URL** ongewijzigd.</span><span class="sxs-lookup"><span data-stu-id="a68cc-136">Leave the **Server URL** field as it is.</span></span> <span data-ttu-id="a68cc-137">Selecteer **Volgende**.</span><span class="sxs-lookup"><span data-stu-id="a68cc-137">Select **Next**.</span></span>
1. <span data-ttu-id="a68cc-138">Meld u aan met uw Microsoft Azure Active Directory (Azure AD)-account.</span><span class="sxs-lookup"><span data-stu-id="a68cc-138">Sign in by using your Microsoft Azure Active Directory (Azure AD) account.</span></span>
1. <span data-ttu-id="a68cc-139">Selecteer onder **Winkelnaam** **San Francisco** en selecteer **Volgende**.</span><span class="sxs-lookup"><span data-stu-id="a68cc-139">Under **Store name**, select **San Francisco**, and then select **Next**.</span></span>
1. <span data-ttu-id="a68cc-140">Onder **Kassa en apparaat** selecteert u **SANFRAN-1**.</span><span class="sxs-lookup"><span data-stu-id="a68cc-140">Under **Register and device**, select **SANFRAN-1**.</span></span>
1. <span data-ttu-id="a68cc-141">Selecteer **Activeren**.</span><span class="sxs-lookup"><span data-stu-id="a68cc-141">Select **Activate**.</span></span> <span data-ttu-id="a68cc-142">U bent afgemeld en de POS-aanmeldingspagina wordt geopend.</span><span class="sxs-lookup"><span data-stu-id="a68cc-142">You're signed out and taken to the POS sign-in page.</span></span>
1. <span data-ttu-id="a68cc-143">U kunt u nu aanmelden bij Cloud POS met operator-id **000713** en wachtwoord **123**.</span><span class="sxs-lookup"><span data-stu-id="a68cc-143">You can now sign in to the Cloud POS experience by using operator ID **000713** and password **123**.</span></span>

## <a name="set-up-your-site-in-commerce"></a><span data-ttu-id="a68cc-144">Uw site instellen in Commerce</span><span class="sxs-lookup"><span data-stu-id="a68cc-144">Set up your site in Commerce</span></span>

<span data-ttu-id="a68cc-145">Ga als volgt te werk om te beginnen met het instellen van uw evaluatiesite in Commerce.</span><span class="sxs-lookup"><span data-stu-id="a68cc-145">To start to set up your evaluation site in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="a68cc-146">Meld u aan bij de site builder met de URL die u hebt genoteerd tijdens de initialisatie van e-Commerce tijdens het inrichten (zie [e-Commerce initialiseren](provisioning-guide.md#initialize-e-commerce)).</span><span class="sxs-lookup"><span data-stu-id="a68cc-146">Sign in to site builder by using the URL that you made a note of when you initialized e-Commerce during provisioning (see [Initialize e-Commerce](provisioning-guide.md#initialize-e-commerce)).</span></span>
1. <span data-ttu-id="a68cc-147">Selecteer **Fabrikam** om het dialoogvenster met instellingen voor de site te openen.</span><span class="sxs-lookup"><span data-stu-id="a68cc-147">Select the **Fabrikam** site to open the site setup dialog box.</span></span>
1. <span data-ttu-id="a68cc-148">Selecteer het domein dat u hebt ingevoerd bij het initialiseren van e-Commerce.</span><span class="sxs-lookup"><span data-stu-id="a68cc-148">Select the domain that you entered when you initialized e-Commerce.</span></span>
1. <span data-ttu-id="a68cc-149">Selecteer **Uitgebreide Fabrikam online winkel** als het standaardkanaal.</span><span class="sxs-lookup"><span data-stu-id="a68cc-149">Select **Fabrikam extended online store** as the default channel.</span></span> <span data-ttu-id="a68cc-150">Zorg ervoor dat u de **uitgebreide** online winkel selecteert.</span><span class="sxs-lookup"><span data-stu-id="a68cc-150">(Make sure that you select the **extended** online store.)</span></span>
1. <span data-ttu-id="a68cc-151">Als standaardtaal selecteert u **en-us**.</span><span class="sxs-lookup"><span data-stu-id="a68cc-151">Select **en-us** as the default language.</span></span>
1. <span data-ttu-id="a68cc-152">Laat de waarde van het veld **Pad** ongewijzigd.</span><span class="sxs-lookup"><span data-stu-id="a68cc-152">Leave the value of the **Path** field as it is.</span></span>
1. <span data-ttu-id="a68cc-153">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="a68cc-153">Select **OK**.</span></span> <span data-ttu-id="a68cc-154">De lijst met pagina's op de site wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="a68cc-154">The list of pages on the site appears.</span></span>

## <a name="enable-jobs"></a><span data-ttu-id="a68cc-155">Taken inschakelen</span><span class="sxs-lookup"><span data-stu-id="a68cc-155">Enable jobs</span></span>

<span data-ttu-id="a68cc-156">Ga als volgt te werk om taken in Commerce in te schakelen.</span><span class="sxs-lookup"><span data-stu-id="a68cc-156">To enable jobs in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="a68cc-157">Meld u aan bij de omgeving (HQ).</span><span class="sxs-lookup"><span data-stu-id="a68cc-157">Sign in to the environment (HQ).</span></span>
1. <span data-ttu-id="a68cc-158">Ga in het menu links naar **Detailhandel en commerce \> Query's en rapporten \> Batchtaken**.</span><span class="sxs-lookup"><span data-stu-id="a68cc-158">Use the menu on the left to go to **Retail and commerce \> Inquiries and reports \> Batch jobs**.</span></span>

    <span data-ttu-id="a68cc-159">De resterende stappen van deze procedure moeten worden voltooid voor elk van de volgende taken:</span><span class="sxs-lookup"><span data-stu-id="a68cc-159">The remaining steps of this procedure must be completed for each of the following jobs:</span></span>

    * <span data-ttu-id="a68cc-160">E-mailmelding voor detailhandelorder verwerken</span><span class="sxs-lookup"><span data-stu-id="a68cc-160">Process retail order email notification</span></span>
    * <span data-ttu-id="a68cc-161">Beschikbaarheid product</span><span class="sxs-lookup"><span data-stu-id="a68cc-161">Product availability</span></span>
    * <span data-ttu-id="a68cc-162">P-0001</span><span class="sxs-lookup"><span data-stu-id="a68cc-162">P-0001</span></span>
    * <span data-ttu-id="a68cc-163">Taak orders synchroniseren</span><span class="sxs-lookup"><span data-stu-id="a68cc-163">Synchronize orders job</span></span>

1. <span data-ttu-id="a68cc-164">Gebruik het snelfilter om de taak te zoeken aan de hand van de naam.</span><span class="sxs-lookup"><span data-stu-id="a68cc-164">Use the Quick Filter to search for the job by name.</span></span>
1. <span data-ttu-id="a68cc-165">Als de status van de taak **Uitvoeren** is, voert u de volgende stappen uit:</span><span class="sxs-lookup"><span data-stu-id="a68cc-165">If the status of the job is **Executing**, follow these steps:</span></span>

    1. <span data-ttu-id="a68cc-166">Selecteer de record.</span><span class="sxs-lookup"><span data-stu-id="a68cc-166">Select the record.</span></span>
    1. <span data-ttu-id="a68cc-167">Selecteer in het actievenster op het tabblad **Batchtaak** de optie **Status wijzigen**.</span><span class="sxs-lookup"><span data-stu-id="a68cc-167">On the Action Pane, on **Batch job** tab, select **Change status**.</span></span>
    1. <span data-ttu-id="a68cc-168">Selecteer **Annuleren** en vervolgens **OK**.</span><span class="sxs-lookup"><span data-stu-id="a68cc-168">Select **Canceling**, and then select **OK**.</span></span>

<span data-ttu-id="a68cc-169">U kunt desgewenst ook het terugkeerinterval instellen op één (1) minuut voor de volgende taken:</span><span class="sxs-lookup"><span data-stu-id="a68cc-169">Optionally, you can also set the recurrence interval to one (1) minute for the following jobs:</span></span>

* <span data-ttu-id="a68cc-170">E-mailmeldingtaak voor detailhandelorder verwerken</span><span class="sxs-lookup"><span data-stu-id="a68cc-170">Process retail order email notification job</span></span>
* <span data-ttu-id="a68cc-171">P-0001 taak</span><span class="sxs-lookup"><span data-stu-id="a68cc-171">P-0001 job</span></span>
* <span data-ttu-id="a68cc-172">Taak orders synchroniseren</span><span class="sxs-lookup"><span data-stu-id="a68cc-172">Synchronize orders job</span></span>

### <a name="run-full-data-synchronization"></a><span data-ttu-id="a68cc-173">Volledige gegevenssynchronisatie uitvoeren</span><span class="sxs-lookup"><span data-stu-id="a68cc-173">Run full data synchronization</span></span>

<span data-ttu-id="a68cc-174">Voer de volgende stappen uit om een volledige gegevenssynchronisatie in Commerce Headquarters uit te voeren.</span><span class="sxs-lookup"><span data-stu-id="a68cc-174">To run full data synchronization in Commerce, follow these steps in Commerce headquarters.</span></span>

1. <span data-ttu-id="a68cc-175">Ga in het menu links naar **Modules \> Detailhandel en commerce \> Instelling van hoofdkantoor \> Commerce-planner \> Kanaaldatabase**.</span><span class="sxs-lookup"><span data-stu-id="a68cc-175">Use the menu on the left to go to **Modules \> Retail and commerce \> Headquarters setup \> Commerce scheduler \> Channel database**.</span></span>
1. <span data-ttu-id="a68cc-176">Selecteer het kanaal met de naam **scXXXXXXXXX**.</span><span class="sxs-lookup"><span data-stu-id="a68cc-176">Select the channel that is named **scXXXXXXXXX**.</span></span>
1. <span data-ttu-id="a68cc-177">Selecteer **Volledige gegevenssynchronisatie** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="a68cc-177">On the Action Pane, select **Full data sync**.</span></span>
1. <span data-ttu-id="a68cc-178">Voer **9999** in als de distributieplanning.</span><span class="sxs-lookup"><span data-stu-id="a68cc-178">Enter **9999** as the distribution schedule.</span></span>
1. <span data-ttu-id="a68cc-179">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="a68cc-179">Select **OK**.</span></span>
1. <span data-ttu-id="a68cc-180">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="a68cc-180">Select **OK**.</span></span>

### <a name="test-credit-card-information-to-do-test-purchases"></a><span data-ttu-id="a68cc-181">Creditcardgegevens testen voor het uitvoeren van testinkopen</span><span class="sxs-lookup"><span data-stu-id="a68cc-181">Test credit card information to do test purchases</span></span>

<span data-ttu-id="a68cc-182">Voor het uitvoeren van testtransacties op de site kunt u de volgende creditcardgegevens testen:</span><span class="sxs-lookup"><span data-stu-id="a68cc-182">To perform test transactions on the site, you can use the following test credit card information:</span></span>

- <span data-ttu-id="a68cc-183">**Kaartnummer:** 4111-1111-1111-1111</span><span class="sxs-lookup"><span data-stu-id="a68cc-183">**Card number:** 4111-1111-1111-1111</span></span>
- <span data-ttu-id="a68cc-184">**Verloopdatum:** 10/20</span><span class="sxs-lookup"><span data-stu-id="a68cc-184">**Expiration date:** 10/20</span></span>
- <span data-ttu-id="a68cc-185">**CVV-code:** 737</span><span class="sxs-lookup"><span data-stu-id="a68cc-185">**Card verification value (CVV) code:** 737</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a68cc-186">Gebruik in geen geval echte creditcardgegevens op de testsite.</span><span class="sxs-lookup"><span data-stu-id="a68cc-186">Never, under any circumstances, try to use actual credit card information on the test site.</span></span>

## <a name="next-steps"></a><span data-ttu-id="a68cc-187">Volgende stappen</span><span class="sxs-lookup"><span data-stu-id="a68cc-187">Next steps</span></span>

<span data-ttu-id="a68cc-188">Als de inrichtings- en configuratiestappen zijn voltooid, bent u klaar om uw evaluatieomgeving te gebruiken.</span><span class="sxs-lookup"><span data-stu-id="a68cc-188">After the provisioning and configuration steps are completed, you can start to use your evaluation environment.</span></span> <span data-ttu-id="a68cc-189">Gebruik de site builder-URL voor de Commerce-site om naar de ontwerpomgeving te gaan.</span><span class="sxs-lookup"><span data-stu-id="a68cc-189">Use the Commerce site builder URL to go to the authoring experience.</span></span> <span data-ttu-id="a68cc-190">Gebruik de URL van de Commerce-site om naar de omgeving van de site van de detailhandelklant te gaan.</span><span class="sxs-lookup"><span data-stu-id="a68cc-190">Use the Commerce site URL to go to the retail customer site experience.</span></span>

<span data-ttu-id="a68cc-191">Zie [Optionele functies voor een evaluatieomgeving van Commerce configureren](cpe-optional-features.md) voor meer informatie over hoe u optionele functies voor uw evaluatieomgeving van Commerce configureert.</span><span class="sxs-lookup"><span data-stu-id="a68cc-191">To configure optional features for your Commerce evaluation environment, see [Configure optional features for a Commerce evaluation environment](cpe-optional-features.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a68cc-192">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="a68cc-192">Additional resources</span></span>

[<span data-ttu-id="a68cc-193">Overzicht van de evaluatieomgeving voor Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="a68cc-193">Dynamics 365 Commerce evaluation environment overview</span></span>](cpe-overview.md)

[<span data-ttu-id="a68cc-194">Een evaluatieomgeving voor Dynamics 365 Commerce inrichten</span><span class="sxs-lookup"><span data-stu-id="a68cc-194">Provision a Dynamics 365 Commerce evaluation environment</span></span>](provisioning-guide.md)

[<span data-ttu-id="a68cc-195">Optionele functies voor een Dynamics 365 Commerce-evaluatieomgeving configureren</span><span class="sxs-lookup"><span data-stu-id="a68cc-195">Configure optional features for a Dynamics 365 Commerce evaluation environment</span></span>](cpe-optional-features.md)

[<span data-ttu-id="a68cc-196">BOPIS configureren in een Dynamics 365 Commerce-evaluatieomgeving</span><span class="sxs-lookup"><span data-stu-id="a68cc-196">Configure BOPIS in a Dynamics 365 Commerce evaluation environment</span></span>](cpe-bopis.md)

[<span data-ttu-id="a68cc-197">Veelgestelde vragen over evaluatieomgeving voor Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="a68cc-197">Dynamics 365 Commerce evaluation environment FAQ</span></span>](cpe-faq.md)

[<span data-ttu-id="a68cc-198">Microsoft Lifecycle Services (LCS)</span><span class="sxs-lookup"><span data-stu-id="a68cc-198">Microsoft Lifecycle Services (LCS)</span></span>](/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[<span data-ttu-id="a68cc-199">Retail Cloud Scale Unit (RCSU)</span><span class="sxs-lookup"><span data-stu-id="a68cc-199">Retail Cloud Scale Unit (RCSU)</span></span>](/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[<span data-ttu-id="a68cc-200">Microsoft Azure-portal</span><span class="sxs-lookup"><span data-stu-id="a68cc-200">Microsoft Azure portal</span></span>](https://azure.microsoft.com/features/azure-portal)

[<span data-ttu-id="a68cc-201">Dynamics 365 Commerce-website</span><span class="sxs-lookup"><span data-stu-id="a68cc-201">Dynamics 365 Commerce website</span></span>](https://aka.ms/Dynamics365CommerceWebsite)


[!INCLUDE[footer-include](../includes/footer-banner.md)]