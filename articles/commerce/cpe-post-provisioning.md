---
title: Een preview-omgeving van Commerce configureren
description: In dit onderwerp wordt uitgelegd hoe u een preview-omgeving van Microsoft Dynamics 365 Commerce configureert na inrichting.
author: psimolin
manager: annbe
ms.date: 12/10/2019
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
ms.author: psimolin
ms.search.validFrom: 2019-12-10
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: f19d03f3f2f5a9f6f7ba08b682277e4e3b764d10
ms.sourcegitcommit: 610d5c3efadbaf11752b46f24680af619bcd70a6
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/10/2019
ms.locfileid: "2906134"
---
# <a name="configure-a-commerce-preview-environment"></a><span data-ttu-id="c8019-103">Een preview-omgeving van Commerce configureren</span><span class="sxs-lookup"><span data-stu-id="c8019-103">Configure a Commerce preview environment</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="c8019-104">In dit onderwerp wordt uitgelegd hoe u een preview-omgeving van Microsoft Dynamics 365 Commerce configureert na inrichting.</span><span class="sxs-lookup"><span data-stu-id="c8019-104">This topic explains how to configure a Microsoft Dynamics 365 Commerce preview environment after it's provisioned.</span></span>

## <a name="overview"></a><span data-ttu-id="c8019-105">Overzicht</span><span class="sxs-lookup"><span data-stu-id="c8019-105">Overview</span></span>

<span data-ttu-id="c8019-106">Voltooi de procedures in dit onderwerp pas nadat uw preview-omgeving van Commerce is ingericht.</span><span class="sxs-lookup"><span data-stu-id="c8019-106">Complete the procedures in this topic only after your Commerce preview environment has been provisioned.</span></span> <span data-ttu-id="c8019-107">Zie [Een preview-omgeving van Commerce inrichten](provisioning-guide.md) voor meer informatie over hoe u uw preview-omgeving van Commerce inricht.</span><span class="sxs-lookup"><span data-stu-id="c8019-107">For information about how to provision your Commerce preview environment, see [Provision a Commerce preview environment](provisioning-guide.md).</span></span>

<span data-ttu-id="c8019-108">Nadat uw preview-omgeving van Commerce end-to-end is ingericht, moeten extra configuratiestappen worden voltooid voordat u kunt beginnen met het evalueren van de omgeving.</span><span class="sxs-lookup"><span data-stu-id="c8019-108">After your Commerce preview environment has been provisioned end to end, additional post-provisioning configuration steps must be completed before you can start to evaluate the environment.</span></span> <span data-ttu-id="c8019-109">Als u deze stappen wilt uitvoeren, moet u Microsoft Dynamics Lifecycle Services (LCS) Dynamics 365 Commerce en Dynamics 365 Retail gebruiken.</span><span class="sxs-lookup"><span data-stu-id="c8019-109">To complete these steps, you must use Microsoft Dynamics Lifecycle Services (LCS), Dynamics 365 Commerce, and Dynamics 365 Retail.</span></span>

## <a name="before-you-start"></a><span data-ttu-id="c8019-110">Voordat u begint</span><span class="sxs-lookup"><span data-stu-id="c8019-110">Before you start</span></span>

1. <span data-ttu-id="c8019-111">Meld u aan bij de [LCS-portal](https://lcs.dynamics.com).</span><span class="sxs-lookup"><span data-stu-id="c8019-111">Sign in to the [LCS portal](https://lcs.dynamics.com).</span></span>
1. <span data-ttu-id="c8019-112">Ga naar uw project.</span><span class="sxs-lookup"><span data-stu-id="c8019-112">Go to your project.</span></span>
1. <span data-ttu-id="c8019-113">Selecteer in het bovenste menu de optie **Cloudomgevingen**.</span><span class="sxs-lookup"><span data-stu-id="c8019-113">On the top menu, select **Cloud-hosted environments**.</span></span>
1. <span data-ttu-id="c8019-114">Selecteer uw omgeving in de lijst.</span><span class="sxs-lookup"><span data-stu-id="c8019-114">Select your environment in the list.</span></span>
1. <span data-ttu-id="c8019-115">Klik op **Volledige details** in de omgevingsgegevens rechts.</span><span class="sxs-lookup"><span data-stu-id="c8019-115">In the environment information on the right, select **Full details**.</span></span>
1. <span data-ttu-id="c8019-116">Selecteer **Aanmelden** om een menu te openen en selecteer **Aanmelden bij omgeving**.</span><span class="sxs-lookup"><span data-stu-id="c8019-116">Select **Login** to open a menu, and then select **Log on to environment**.</span></span>
1. <span data-ttu-id="c8019-117">Zorg ervoor dat de rechtspersoon **USRT** is geselecteerd rechtsboven.</span><span class="sxs-lookup"><span data-stu-id="c8019-117">Make sure that the **USRT** legal entity is selected in the upper-right corner.</span></span>

## <a name="configure-the-point-of-sale-in-lcs"></a><span data-ttu-id="c8019-118">Het verkooppunt configureren in LCS</span><span class="sxs-lookup"><span data-stu-id="c8019-118">Configure the point of sale in LCS</span></span>

### <a name="associate-a-worker-with-your-identity"></a><span data-ttu-id="c8019-119">Een medewerker aan uw identiteit koppelen</span><span class="sxs-lookup"><span data-stu-id="c8019-119">Associate a worker with your identity</span></span>

<span data-ttu-id="c8019-120">Ga als volgt te werk om een medewerker te koppelen aan uw identiteit in LCS.</span><span class="sxs-lookup"><span data-stu-id="c8019-120">To associate a worker with your identity in LCS, follow these steps.</span></span>

1. <span data-ttu-id="c8019-121">Ga in het menu links naar **Modules \> Detailhandel \> Werknemers \> Werknemers**.</span><span class="sxs-lookup"><span data-stu-id="c8019-121">Use the menu on the left to go to **Modules \> Retail \> Employees \> Workers**.</span></span>
1. <span data-ttu-id="c8019-122">Zoek en selecteer record **000713 - Andrew Collette**.</span><span class="sxs-lookup"><span data-stu-id="c8019-122">In the list, find and select the following record: **000713 - Andrew Collette**.</span></span>
1. <span data-ttu-id="c8019-123">Selecteer **Detailhandel** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="c8019-123">On the Action Pane, select **Retail**.</span></span>
1. <span data-ttu-id="c8019-124">Selecteer **Bestaande identiteit koppelen**.</span><span class="sxs-lookup"><span data-stu-id="c8019-124">Select **Associate existing identity**.</span></span>
1. <span data-ttu-id="c8019-125">Typ uw e-mailadres in het veld **E-mail** rechts van **Zoeken met behulp van e-mail**.</span><span class="sxs-lookup"><span data-stu-id="c8019-125">In the **Email** field to the right of **Search using email**, enter your email address.</span></span>
1. <span data-ttu-id="c8019-126">Selecteer **Zoeken**.</span><span class="sxs-lookup"><span data-stu-id="c8019-126">Select **Search**.</span></span>
1. <span data-ttu-id="c8019-127">Selecteer de record met uw naam.</span><span class="sxs-lookup"><span data-stu-id="c8019-127">Select the record that has your name.</span></span>
1. <span data-ttu-id="c8019-128">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="c8019-128">Select **OK**.</span></span>
1. <span data-ttu-id="c8019-129">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="c8019-129">Select **Save**.</span></span>

### <a name="activate-cloud-pos"></a><span data-ttu-id="c8019-130">Cloud POS activeren</span><span class="sxs-lookup"><span data-stu-id="c8019-130">Activate Cloud POS</span></span>

<span data-ttu-id="c8019-131">Ga als volgt te werk om Cloud POS in LCS te activeren.</span><span class="sxs-lookup"><span data-stu-id="c8019-131">To activate Cloud POS in LCS, follow these steps.</span></span>

1. <span data-ttu-id="c8019-132">Selecteer in het bovenste menu de optie **Cloudomgevingen**.</span><span class="sxs-lookup"><span data-stu-id="c8019-132">On the top menu, select **Cloud-hosted environments**.</span></span>
1. <span data-ttu-id="c8019-133">Selecteer uw omgeving in de lijst.</span><span class="sxs-lookup"><span data-stu-id="c8019-133">Select your environment in the list.</span></span>
1. <span data-ttu-id="c8019-134">Klik op **Volledige details** in de omgevingsgegevens rechts.</span><span class="sxs-lookup"><span data-stu-id="c8019-134">In the environment information on the right, select **Full details**.</span></span>
1. <span data-ttu-id="c8019-135">Selecteer **Aanmelden** om een menu te openen en selecteer **Aanmelden bij cloud-verkooppunt** om het verkooppunt (POS) te openen.</span><span class="sxs-lookup"><span data-stu-id="c8019-135">Select **Login** to open a menu, and then select **Log on to Cloud Point of Sale** to open the point of sale (POS).</span></span>
1. <span data-ttu-id="c8019-136">Selecteer **Volgende**.</span><span class="sxs-lookup"><span data-stu-id="c8019-136">Select **Next**.</span></span>
1. <span data-ttu-id="c8019-137">Meld u aan met uw Microsoft Azure Active Directory (Azure AD)-account.</span><span class="sxs-lookup"><span data-stu-id="c8019-137">Sign in by using your Microsoft Azure Active Directory (Azure AD) account.</span></span>
1. <span data-ttu-id="c8019-138">Onder **Winkelnaam** selecteert u **San Francisco**.</span><span class="sxs-lookup"><span data-stu-id="c8019-138">Under **Store name**, select **San Francisco**.</span></span>
1. <span data-ttu-id="c8019-139">Selecteer **Volgende**.</span><span class="sxs-lookup"><span data-stu-id="c8019-139">Select **Next**.</span></span>
1. <span data-ttu-id="c8019-140">Onder **Kassa en apparaat** selecteert u **SANFRAN-1**.</span><span class="sxs-lookup"><span data-stu-id="c8019-140">Under **Register and device**, select **SANFRAN-1**.</span></span>
1. <span data-ttu-id="c8019-141">Selecteer **Activeren**.</span><span class="sxs-lookup"><span data-stu-id="c8019-141">Select **Activate**.</span></span> <span data-ttu-id="c8019-142">U bent afgemeld en de POS-aanmeldingspagina wordt geopend.</span><span class="sxs-lookup"><span data-stu-id="c8019-142">You're signed out and taken to the POS sign-in page.</span></span>
1. <span data-ttu-id="c8019-143">U kunt u nu aanmelden bij Cloud POS met operator-id **000713** en wachtwoord **123**.</span><span class="sxs-lookup"><span data-stu-id="c8019-143">You can now sign in to the Cloud POS experience by using operator ID **000713** and password **123**.</span></span>

## <a name="set-up-your-site-in-commerce"></a><span data-ttu-id="c8019-144">Uw site instellen in Commerce</span><span class="sxs-lookup"><span data-stu-id="c8019-144">Set up your site in Commerce</span></span>

<span data-ttu-id="c8019-145">Ga als volgt te werk om te beginnen met het instellen van uw voorbeeldsite in Commerce.</span><span class="sxs-lookup"><span data-stu-id="c8019-145">To start to set up your preview site in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="c8019-146">Meld u aan bij het beheerhulpprogramma van de site met de URL die u hebt genoteerd tijdens de initialisatie van e-Commerce tijdens het inrichten (zie [e-Commerce initialiseren](provisioning-guide.md#initialize-e-commerce)).</span><span class="sxs-lookup"><span data-stu-id="c8019-146">Sign in to the site management tool by using the URL that you made a note of when you initialized e-Commerce during provisioning (see [Initialize e-Commerce](provisioning-guide.md#initialize-e-commerce)).</span></span>
1. <span data-ttu-id="c8019-147">Selecteer **Fabrikam** om het dialoogvenster met instellingen voor de site te openen.</span><span class="sxs-lookup"><span data-stu-id="c8019-147">Select the **Fabrikam** site to open the site setup dialog box.</span></span>
1. <span data-ttu-id="c8019-148">Selecteer het domein dat u hebt ingevoerd bij het initialiseren van e-Commerce.</span><span class="sxs-lookup"><span data-stu-id="c8019-148">Select the domain that you entered when you initialized e-Commerce.</span></span>
1. <span data-ttu-id="c8019-149">Selecteer **Uitgebreide Fabrikam online winkel** als het standaardkanaal.</span><span class="sxs-lookup"><span data-stu-id="c8019-149">Select **Fabrikam extended online store** as the default channel.</span></span> <span data-ttu-id="c8019-150">Zorg ervoor dat u de **uitgebreide** online winkel selecteert.</span><span class="sxs-lookup"><span data-stu-id="c8019-150">(Make sure that you select the **extended** online store.)</span></span>
1. <span data-ttu-id="c8019-151">Als standaardtaal selecteert u **en-us**.</span><span class="sxs-lookup"><span data-stu-id="c8019-151">Select **en-us** as the default language.</span></span>
1. <span data-ttu-id="c8019-152">Laat de waarde van het veld **Pad** ongewijzigd.</span><span class="sxs-lookup"><span data-stu-id="c8019-152">Leave the value of the **Path** field as it is.</span></span>
1. <span data-ttu-id="c8019-153">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="c8019-153">Select **OK**.</span></span> <span data-ttu-id="c8019-154">De lijst met pagina's op de site wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="c8019-154">The list of pages on the site appears.</span></span>

## <a name="enable-jobs-in-retail"></a><span data-ttu-id="c8019-155">Taken inschakelen in Retail</span><span class="sxs-lookup"><span data-stu-id="c8019-155">Enable jobs in Retail</span></span>

<span data-ttu-id="c8019-156">Ga als volgt te werk om taken in Retail in te schakelen.</span><span class="sxs-lookup"><span data-stu-id="c8019-156">To enable jobs in Retail, follow these steps.</span></span>

1. <span data-ttu-id="c8019-157">Meld u aan bij de omgeving (HQ).</span><span class="sxs-lookup"><span data-stu-id="c8019-157">Sign in to the environment (HQ).</span></span>
1. <span data-ttu-id="c8019-158">Ga in het menu links naar **Detailhandel \> Query's en rapporten \> Batchtaken**.</span><span class="sxs-lookup"><span data-stu-id="c8019-158">Use the menu on the left to go to **Retail \> Inquiries and reports \> Batch jobs**.</span></span>

    <span data-ttu-id="c8019-159">De resterende stappen van deze procedure moeten worden voltooid voor elk van de volgende taken:</span><span class="sxs-lookup"><span data-stu-id="c8019-159">The remaining steps of this procedure must be completed for each of the following jobs:</span></span>

    * <span data-ttu-id="c8019-160">E-mailmelding voor detailhandelorder verwerken</span><span class="sxs-lookup"><span data-stu-id="c8019-160">Process retail order email notification</span></span>
    * <span data-ttu-id="c8019-161">Beschikbaarheid product</span><span class="sxs-lookup"><span data-stu-id="c8019-161">Product availability</span></span>
    * <span data-ttu-id="c8019-162">P-0001</span><span class="sxs-lookup"><span data-stu-id="c8019-162">P-0001</span></span>
    * <span data-ttu-id="c8019-163">Taak orders synchroniseren</span><span class="sxs-lookup"><span data-stu-id="c8019-163">Synchronize orders job</span></span>

1. <span data-ttu-id="c8019-164">Gebruik het snelfilter om de taak te zoeken aan de hand van de naam.</span><span class="sxs-lookup"><span data-stu-id="c8019-164">Use the Quick Filter to search for the job by name.</span></span>
1. <span data-ttu-id="c8019-165">Als de status van de taak **Blokkeren** is, voert u de volgende stappen uit:</span><span class="sxs-lookup"><span data-stu-id="c8019-165">If the status of the job is **Withhold**, follow these steps:</span></span>

    1. <span data-ttu-id="c8019-166">Selecteer de record.</span><span class="sxs-lookup"><span data-stu-id="c8019-166">Select the record.</span></span>
    1. <span data-ttu-id="c8019-167">Selecteer in het actievenster op het tabblad **Batchtaak** de optie **Status wijzigen**.</span><span class="sxs-lookup"><span data-stu-id="c8019-167">On the Action Pane, on **Batch job** tab, select **Change status**.</span></span>
    1. <span data-ttu-id="c8019-168">Selecteer **Wachten** en vervolgens **OK**.</span><span class="sxs-lookup"><span data-stu-id="c8019-168">Select **Waiting**, and then select **OK**.</span></span>

### <a name="run-full-data-synchronization-in-retail"></a><span data-ttu-id="c8019-169">Volledige gegevenssynchronisatie uitvoeren in Retail</span><span class="sxs-lookup"><span data-stu-id="c8019-169">Run full data synchronization in Retail</span></span>

<span data-ttu-id="c8019-170">Voer de volgende stappen uit om een volledige gegevenssynchronisatie in Retail uit te voeren.</span><span class="sxs-lookup"><span data-stu-id="c8019-170">To run full data synchronization in Retail, follow these steps.</span></span>

1. <span data-ttu-id="c8019-171">Ga in het menu links naar **Modules \> Detailhandel \> Instelling van hoofdkantoor \> Detailhandel planner \> Kanaaldatabase**.</span><span class="sxs-lookup"><span data-stu-id="c8019-171">Use the menu on the left to go to **Modules \> Retail \> Headquarters setup \> Retail scheduler \> Channel database**.</span></span>
1. <span data-ttu-id="c8019-172">In de lijst links is het kanaal **Standaard** geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="c8019-172">In the list on the left, the **Default** channel is selected.</span></span> <span data-ttu-id="c8019-173">Selecteer het andere beschikbare kanaal.</span><span class="sxs-lookup"><span data-stu-id="c8019-173">Select the other available channel.</span></span> <span data-ttu-id="c8019-174">Dit kanaal heeft de naam **scXXXXXXXXX**.</span><span class="sxs-lookup"><span data-stu-id="c8019-174">This channel is named **scXXXXXXXXX**.</span></span>
1. <span data-ttu-id="c8019-175">Selecteer **Volledige gegevenssynchronisatie** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="c8019-175">On the Action Pane, select **Full data sync**.</span></span>
1. <span data-ttu-id="c8019-176">Voer **9999** in als de distributieplanning.</span><span class="sxs-lookup"><span data-stu-id="c8019-176">Enter **9999** as the distribution schedule.</span></span>
1. <span data-ttu-id="c8019-177">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="c8019-177">Select **OK**.</span></span>
1. <span data-ttu-id="c8019-178">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="c8019-178">Select **OK**.</span></span>

### <a name="test-credit-card-information-to-do-test-purchases"></a><span data-ttu-id="c8019-179">Creditcardgegevens testen voor het uitvoeren van testinkopen</span><span class="sxs-lookup"><span data-stu-id="c8019-179">Test credit card information to do test purchases</span></span>

<span data-ttu-id="c8019-180">Voor het uitvoeren van testtransacties op de site kunt u de volgende creditcardgegevens testen:</span><span class="sxs-lookup"><span data-stu-id="c8019-180">To perform test transactions on the site, you can use the following test credit card information:</span></span>

- <span data-ttu-id="c8019-181">**Kaartnummer:** 4111-1111-1111-1111</span><span class="sxs-lookup"><span data-stu-id="c8019-181">**Card number:** 4111-1111-1111-1111</span></span>
- <span data-ttu-id="c8019-182">**Verloopdatum:** 10/20</span><span class="sxs-lookup"><span data-stu-id="c8019-182">**Expiration date:** 10/20</span></span>
- <span data-ttu-id="c8019-183">**CVV-code:** 737</span><span class="sxs-lookup"><span data-stu-id="c8019-183">**Card verification value (CVV) code:** 737</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c8019-184">Gebruik in geen geval echte creditcardgegevens op de testsite.</span><span class="sxs-lookup"><span data-stu-id="c8019-184">Never, under any circumstances, try to use actual credit card information on the test site.</span></span>

## <a name="next-steps"></a><span data-ttu-id="c8019-185">Volgende stappen</span><span class="sxs-lookup"><span data-stu-id="c8019-185">Next steps</span></span>

<span data-ttu-id="c8019-186">Als de inrichtings- en configuratiestappen zijn voltooid, bent u klaar om uw preview-omgeving te evalueren.</span><span class="sxs-lookup"><span data-stu-id="c8019-186">After the provisioning and configuration steps are completed, you're ready to evaluate your preview environment.</span></span> <span data-ttu-id="c8019-187">Gebruik de URL van het beheerhulpprogramma van de e-Commerce-site om naar de ontwerpomgeving te gaan.</span><span class="sxs-lookup"><span data-stu-id="c8019-187">Use the URL of the Commerce site management tool to go to the authoring experience.</span></span> <span data-ttu-id="c8019-188">Gebruik de URL van de e-Commerce-site om naar de omgeving van de site van de detailhandelklant te gaan.</span><span class="sxs-lookup"><span data-stu-id="c8019-188">Use the URL of the Commerce site to go to the retail customer site experience.</span></span>

<span data-ttu-id="c8019-189">Zie [Optionele functies voor een preview-omgeving van Commerce configureren](cpe-optional-features.md) voor meer informatie over hoe u optionele functies voor uw preview-omgeving van Commerce configureert.</span><span class="sxs-lookup"><span data-stu-id="c8019-189">To configure optional features for your Commerce preview environment, see [Configure optional features for a Commerce preview environment](cpe-optional-features.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c8019-190">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="c8019-190">Additional resources</span></span>

[<span data-ttu-id="c8019-191">Overzicht van Commerce preview-omgeving</span><span class="sxs-lookup"><span data-stu-id="c8019-191">Commerce preview environment overview</span></span>](cpe-overview.md)

[<span data-ttu-id="c8019-192">Een preview-omgeving van Commerce inrichten</span><span class="sxs-lookup"><span data-stu-id="c8019-192">Provision a Commerce preview environment</span></span>](provisioning-guide.md)

[<span data-ttu-id="c8019-193">Optionele functies voor een preview-omgeving van Commerce configureren</span><span class="sxs-lookup"><span data-stu-id="c8019-193">Configure optional features for a Commerce preview environment</span></span>](cpe-optional-features.md)

[<span data-ttu-id="c8019-194">Veelgestelde vragen over de preview-omgeving van Commerce</span><span class="sxs-lookup"><span data-stu-id="c8019-194">Commerce preview environment FAQ</span></span>](cpe-faq.md)

[<span data-ttu-id="c8019-195">Microsoft Lifecycle Services (LCS)</span><span class="sxs-lookup"><span data-stu-id="c8019-195">Microsoft Lifecycle Services (LCS)</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[<span data-ttu-id="c8019-196">Retail Cloud Scale Unit (RCSU)</span><span class="sxs-lookup"><span data-stu-id="c8019-196">Retail Cloud Scale Unit (RCSU)</span></span>](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[<span data-ttu-id="c8019-197">Microsoft Azure-portal</span><span class="sxs-lookup"><span data-stu-id="c8019-197">Microsoft Azure portal</span></span>](https://azure.microsoft.com/features/azure-portal)

[<span data-ttu-id="c8019-198">Dynamics 365 Commerce-website</span><span class="sxs-lookup"><span data-stu-id="c8019-198">Dynamics 365 Commerce website</span></span>](https://aka.ms/Dynamics365CommerceWebsite)

[<span data-ttu-id="c8019-199">Help-bronnen voor Dynamics 365 Retail</span><span class="sxs-lookup"><span data-stu-id="c8019-199">Help resources for Dynamics 365 Retail</span></span>](../retail/index.md)
