---
title: Optionele functies voor een Dynamics 365 Commerce-evaluatieomgeving configureren
description: In dit onderwerp wordt uitgelegd hoe u optionele functies voor een evaluatieomgeving van Microsoft Dynamics 365 Commerce configureert.
author: psimolin
manager: annbe
ms.date: 07/16/2020
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
ms.openlocfilehash: 6f7ba7e6de3791720458b509059f008423c73a82
ms.sourcegitcommit: 5175e3fae432016246244cf70fe05465f43de88c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 07/17/2020
ms.locfileid: "3599815"
---
# <a name="configure-optional-features-for-a-dynamics-365-commerce-evaluation-environment"></a><span data-ttu-id="695cf-103">Optionele functies voor een Dynamics 365 Commerce-evaluatieomgeving configureren</span><span class="sxs-lookup"><span data-stu-id="695cf-103">Configure optional features for a Dynamics 365 Commerce evaluation environment</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="695cf-104">In dit onderwerp wordt uitgelegd hoe u optionele functies voor een evaluatieomgeving van Microsoft Dynamics 365 Commerce configureert.</span><span class="sxs-lookup"><span data-stu-id="695cf-104">This topic explains how to configure optional features for a Microsoft Dynamics 365 Commerce evaluation environment.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="695cf-105">Vereisten</span><span class="sxs-lookup"><span data-stu-id="695cf-105">Prerequisites</span></span>

<span data-ttu-id="695cf-106">Als u de transactionele e-mailfuncties wilt evalueren, moet aan de volgende voorwaarden worden voldaan:</span><span class="sxs-lookup"><span data-stu-id="695cf-106">If you want to evaluate the transactional email features, the following prerequisites must be met:</span></span>

- <span data-ttu-id="695cf-107">U hebt een e-mailserver beschikbaar (\[SMTP\]-server), die kan worden gebruikt vanuit het Microsoft Azure-abonnement waarin u de evaluatieomgeving inricht.</span><span class="sxs-lookup"><span data-stu-id="695cf-107">You have an available email server (Simple Mail Transfer Protocol \[SMTP\] server) that can be used from the Microsoft Azure subscription where you provisioned the evaluation environment.</span></span>
- <span data-ttu-id="695cf-108">U hebt het FQDN/IP-adres, het SMTP-poortnummer en de verificatiegegevens van de server beschikbaar.</span><span class="sxs-lookup"><span data-stu-id="695cf-108">You have the server's fully qualified domain name (FQDN)/IP address, SMTP port number, and authentication details available.</span></span>

## <a name="configure-the-image-back-end"></a><span data-ttu-id="695cf-109">De backend van de afbeelding configureren</span><span class="sxs-lookup"><span data-stu-id="695cf-109">Configure the image back end</span></span>

### <a name="find-your-media-base-url"></a><span data-ttu-id="695cf-110">Uw basis-URL voor media vinden</span><span class="sxs-lookup"><span data-stu-id="695cf-110">Find your media base URL</span></span>

> [!NOTE]
> <span data-ttu-id="695cf-111">Voordat u deze procedure kunt uitvoeren, moet u de stappen in [Uw site instellen in Commerce](cpe-post-provisioning.md#set-up-your-site-in-commerce) voltooien.</span><span class="sxs-lookup"><span data-stu-id="695cf-111">Before you can complete this procedure, you must complete the steps in [Set up your site in Commerce](cpe-post-provisioning.md#set-up-your-site-in-commerce).</span></span>

1. <span data-ttu-id="695cf-112">Meld u aan bij de Commerce Site Builder met de URL die u hebt genoteerd tijdens de initialisatie van e-Commerce tijdens het inrichten (zie [e-Commerce initialiseren](provisioning-guide.md#initialize-e-commerce)).</span><span class="sxs-lookup"><span data-stu-id="695cf-112">Sign in to the Commerce site builder by using the URL you made a note of when you initialized e-Commerce during provisioning (see [Initialize e-Commerce](provisioning-guide.md#initialize-e-commerce)).</span></span>
1. <span data-ttu-id="695cf-113">Open de site **Fabrikam**.</span><span class="sxs-lookup"><span data-stu-id="695cf-113">Open the **Fabrikam** site.</span></span>
1. <span data-ttu-id="695cf-114">Selecteer **Mediabibliotheek** in het linkermenu.</span><span class="sxs-lookup"><span data-stu-id="695cf-114">On the menu on the left, select **Media Library**.</span></span>
1. <span data-ttu-id="695cf-115">Selecteer één afbeeldingsactivum.</span><span class="sxs-lookup"><span data-stu-id="695cf-115">Select any single image asset.</span></span>
1. <span data-ttu-id="695cf-116">Zoek in de eigenschappencontrole aan de rechterkant de eigenschap **Openbare URL**.</span><span class="sxs-lookup"><span data-stu-id="695cf-116">In the property inspector on the right, find the **Public URL** property.</span></span> <span data-ttu-id="695cf-117">De waarde is een URL.</span><span class="sxs-lookup"><span data-stu-id="695cf-117">The value is a URL.</span></span> <span data-ttu-id="695cf-118">Dit is een voorbeeld:</span><span class="sxs-lookup"><span data-stu-id="695cf-118">Here is an example:</span></span>

    <span data-ttu-id="695cf-119">`https://images-us-sb.cms.commerce.dynamics.com/cms/api/fabrikam/imageFileData/MA1nQC`.</span><span class="sxs-lookup"><span data-stu-id="695cf-119">`https://images-us-sb.cms.commerce.dynamics.com/cms/api/fabrikam/imageFileData/MA1nQC`.</span></span>

1. <span data-ttu-id="695cf-120">Vervang de laatste id in de URL (**MA1nQC** in het voorbeeld hierboven) door de volgende tekenreeks: **search?fileName=**.</span><span class="sxs-lookup"><span data-stu-id="695cf-120">Replace the last identifier in the URL (**MA1nQC** in the preceding example) with the string **search?fileName=**.</span></span> <span data-ttu-id="695cf-121">De voorbeeld-URL ziet er zo uit nadat deze wijziging is doorgevoerd:</span><span class="sxs-lookup"><span data-stu-id="695cf-121">Here is what the example URL looks like after this change is made:</span></span>

    `https://images-us-sb.cms.commerce.dynamics.com/cms/api/fabrikam/imageFileData/search?fileName=`

    <span data-ttu-id="695cf-122">Deze URL is uw basis-URL voor media.</span><span class="sxs-lookup"><span data-stu-id="695cf-122">This URL is your media base URL.</span></span> <span data-ttu-id="695cf-123">Noteer deze.</span><span class="sxs-lookup"><span data-stu-id="695cf-123">Make a note of it.</span></span>

### <a name="update-the-media-base-url"></a><span data-ttu-id="695cf-124">De basis-URL voor media bijwerken</span><span class="sxs-lookup"><span data-stu-id="695cf-124">Update the media base URL</span></span>

1. <span data-ttu-id="695cf-125">Meld u aan bij Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="695cf-125">Sign in to Commerce headquarters.</span></span>
1. <span data-ttu-id="695cf-126">Ga in het menu links naar **Modules \> Detailhandel en commerce \> Afzetkanaalinstellingen \> Afzetkanaalprofielen**.</span><span class="sxs-lookup"><span data-stu-id="695cf-126">Use the menu on the left to go to **Modules \> Retail and commerce \> Channel setup \> Channel profiles**.</span></span>
1. <span data-ttu-id="695cf-127">Selecteer **Bewerken**.</span><span class="sxs-lookup"><span data-stu-id="695cf-127">Select **Edit**.</span></span>
1. <span data-ttu-id="695cf-128">Vervang onder **Profieleigenschappen** de waarde voor **Basis-URL voor mediaserver** door de basis-URL voor media die u eerder hebt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="695cf-128">Under **Profile properties**, replace the value for the **Media Server Base URL** property with the media base URL that you created earlier.</span></span>
1. <span data-ttu-id="695cf-129">Selecteer het kanaal met de naam **scXXXXXXXXX**.</span><span class="sxs-lookup"><span data-stu-id="695cf-129">Select the channel that is named **scXXXXXXXXX**.</span></span>
1. <span data-ttu-id="695cf-130">Selecteer onder **Profieleigenschappen** de optie **Toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="695cf-130">Under **Profile properties**, select **Add**.</span></span>
1. <span data-ttu-id="695cf-131">Voor de eigenschap die is toegevoegd, selecteert **Basis-URL voor mediaserver** als de eigenschapssleutel.</span><span class="sxs-lookup"><span data-stu-id="695cf-131">For the property that was added, select **Media Server Base URL** as the property key.</span></span> <span data-ttu-id="695cf-132">Voer als de waarde van de eigenschap de basis-URL voor de media in die u eerder hebt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="695cf-132">As the property value, enter the media base URL that you created earlier.</span></span>
1. <span data-ttu-id="695cf-133">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="695cf-133">Select **Save**.</span></span>

## <a name="configure-and-test-the-email-server"></a><span data-ttu-id="695cf-134">De e-mailserver configureren en testen</span><span class="sxs-lookup"><span data-stu-id="695cf-134">Configure and test the email server</span></span>

> [!NOTE]
> <span data-ttu-id="695cf-135">De SMTP-server of e-mailservice die u hier invoert, moet toegankelijk zijn vanuit het Azure-abonnement dat u voor de omgeving gebruikt.</span><span class="sxs-lookup"><span data-stu-id="695cf-135">The SMTP server or email service that you enter here must be accessible from the Azure subscription that you're using for the environment.</span></span>

1. <span data-ttu-id="695cf-136">Meld u aan bij Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="695cf-136">Sign in to Commerce headquarters.</span></span>
1. <span data-ttu-id="695cf-137">Ga via het menu links naar **Modules \> Retail en Commerce \> Instelling van hoofdkantoor \> Parameters \> E-mailparameters**.</span><span class="sxs-lookup"><span data-stu-id="695cf-137">Use the menu on the left to go to **Modules \> Retail and Commerce \> Headquarters setup \> Parameters \> Email parameters**.</span></span>
1. <span data-ttu-id="695cf-138">Voer op het tabblad **SMTP-instellingen** in het veld **Naam SMTP-relaisserver** de FQDN-naam of het IP-adres in van de SMTP-server of e-mailservice.</span><span class="sxs-lookup"><span data-stu-id="695cf-138">On the **SMTP settings** tab, in the **Outgoing mail server** field, enter the FQDN or IP address of your SMTP server or email service.</span></span>
1. <span data-ttu-id="695cf-139">Voer in het veld **SMTP-poortnummer** het poortnummer in.</span><span class="sxs-lookup"><span data-stu-id="695cf-139">In the **SMTP port number** field, enter the port number.</span></span> <span data-ttu-id="695cf-140">(Als u SSL \[Secure Sockets Layer \] gebruikt, is het standaardpoortnummer **25**.)</span><span class="sxs-lookup"><span data-stu-id="695cf-140">(If you aren't using Secure Sockets Layer \[SSL\], the default port number is **25**.)</span></span>
1. <span data-ttu-id="695cf-141">Als verificatie vereist is, voert u waarden in de velden **Gebruikersnaam** en **Wachtwoord** in.</span><span class="sxs-lookup"><span data-stu-id="695cf-141">If authentication is required, enter values in the **User name** and **Password** fields.</span></span>
1. <span data-ttu-id="695cf-142">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="695cf-142">Select **Save**.</span></span>
1. <span data-ttu-id="695cf-143">Selecteer **Vernieuwen**.</span><span class="sxs-lookup"><span data-stu-id="695cf-143">Select **Refresh**.</span></span>
1. <span data-ttu-id="695cf-144">Selecteer op het tabblad **Testbericht** in het veld **E-mailprovider** de optie **SMTP**.</span><span class="sxs-lookup"><span data-stu-id="695cf-144">On the **Test email** tab, in the **Email provider** field, select **SMTP**.</span></span>
1. <span data-ttu-id="695cf-145">Voer in het veld **Verzenden naar** het e-mailadres in waar u het testbericht wilt afleveren.</span><span class="sxs-lookup"><span data-stu-id="695cf-145">In the **Send to** field, enter the email address that the test email should be delivered to.</span></span>
1. <span data-ttu-id="695cf-146">Selecteer **Testbericht verzenden**.</span><span class="sxs-lookup"><span data-stu-id="695cf-146">Select **Send test email**.</span></span>

## <a name="configure-email-templates"></a><span data-ttu-id="695cf-147">E-mailsjablonen configureren</span><span class="sxs-lookup"><span data-stu-id="695cf-147">Configure email templates</span></span>

<span data-ttu-id="695cf-148">Voor elke transactionele gebeurtenis waarvoor u e-mailberichten wilt verzenden, moet u de e-mailsjabloon bijwerken met een geldig e-mailadres van de afzender.</span><span class="sxs-lookup"><span data-stu-id="695cf-148">For each transactional event that you want to send emails for, you must update the email template with a valid sender email address.</span></span>

1. <span data-ttu-id="695cf-149">Meld u aan bij Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="695cf-149">Sign in to Commerce headquarters.</span></span>
1. <span data-ttu-id="695cf-150">Ga via het menu links naar **Modules \> Retail en Commerce \> Instelling van hoofdkantoor \> Parameters \> E-mailsjablonen van organisatie**.</span><span class="sxs-lookup"><span data-stu-id="695cf-150">Use the menu on the left to go to **Modules \> Retail and Commerce \> Headquarters setup \> Parameters \> Organization email templates**.</span></span>
1. <span data-ttu-id="695cf-151">Selecteer **Lijst weergeven**.</span><span class="sxs-lookup"><span data-stu-id="695cf-151">Select **Show list**.</span></span>
1. <span data-ttu-id="695cf-152">Volg deze stappen voor elke sjabloon in de lijst:</span><span class="sxs-lookup"><span data-stu-id="695cf-152">For each template in the list, follow these steps:</span></span>

    1. <span data-ttu-id="695cf-153">Voer in het veld **E-mailadres afzender** het e-mailadres van de afzender in.</span><span class="sxs-lookup"><span data-stu-id="695cf-153">In the **Sender email** field, enter the sender email address.</span></span>
    1. <span data-ttu-id="695cf-154">Optioneel: voer in het veld **Naam van afzender** de naam in die moet worden gebruikt als de naam van de afzender.</span><span class="sxs-lookup"><span data-stu-id="695cf-154">Optional: In the **Sender name** field, enter the name that should be used as the sender name.</span></span>

1. <span data-ttu-id="695cf-155">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="695cf-155">Select **Save**.</span></span>

## <a name="customize-email-templates"></a><span data-ttu-id="695cf-156">E-mailsjablonen aanpassen</span><span class="sxs-lookup"><span data-stu-id="695cf-156">Customize email templates</span></span>

<span data-ttu-id="695cf-157">Mogelijk wilt u de e-mailsjablonen aanpassen zodat deze verschillende afbeeldingen gebruiken.</span><span class="sxs-lookup"><span data-stu-id="695cf-157">You might want to customize the email templates so that they use different images.</span></span> <span data-ttu-id="695cf-158">U kunt ook de koppelingen in de sjablonen bijwerken, zodat deze naar uw evaluatieomgeving leiden.</span><span class="sxs-lookup"><span data-stu-id="695cf-158">Or you might want to update the links in the templates so that they go to your evaluation environment.</span></span> <span data-ttu-id="695cf-159">In deze procedure wordt uitgelegd hoe u de standaardsjablonen kunt downloaden, aanpassen en bijwerken in het systeem.</span><span class="sxs-lookup"><span data-stu-id="695cf-159">This procedure explains how to download the default templates, customize them, and update the templates in the system.</span></span>

1. <span data-ttu-id="695cf-160">Download via een webbrowser [het zipbestand met standaard e-mailsjablonen voor Microsoft Dynamics 365 Commerce-evaluatie](https://download.microsoft.com/download/d/7/b/d7b6c4d4-fe09-4922-9551-46bbb29d202d/Commerce.Preview.Default.Email.Templates.zip) naar uw lokale computer.</span><span class="sxs-lookup"><span data-stu-id="695cf-160">In a web browser, download the [Microsoft Dynamics 365 Commerce Evaluation default email templates zip file](https://download.microsoft.com/download/d/7/b/d7b6c4d4-fe09-4922-9551-46bbb29d202d/Commerce.Preview.Default.Email.Templates.zip) to your local computer.</span></span> <span data-ttu-id="695cf-161">Dit bestand bevat de volgende HTML-documenten:</span><span class="sxs-lookup"><span data-stu-id="695cf-161">This file contains the following HTML documents:</span></span>

    - <span data-ttu-id="695cf-162">Sjabloon voor orderbevestiging</span><span class="sxs-lookup"><span data-stu-id="695cf-162">Order confirmation template</span></span>
    - <span data-ttu-id="695cf-163">Sjabloon voor uitgifte van geschenkbon</span><span class="sxs-lookup"><span data-stu-id="695cf-163">Issue gift card template</span></span>
    - <span data-ttu-id="695cf-164">Sjabloon voor nieuwe order</span><span class="sxs-lookup"><span data-stu-id="695cf-164">New order template</span></span>
    - <span data-ttu-id="695cf-165">Sjabloon voor verpakkingsorder</span><span class="sxs-lookup"><span data-stu-id="695cf-165">Pack order template</span></span>
    - <span data-ttu-id="695cf-166">Sjabloon voor orderverzameling</span><span class="sxs-lookup"><span data-stu-id="695cf-166">Pick order template</span></span>

1. <span data-ttu-id="695cf-167">Pas de sjablonen aan met een tekst- of HTML-editor.</span><span class="sxs-lookup"><span data-stu-id="695cf-167">Customize the templates by using a text or HTML editor.</span></span> <span data-ttu-id="695cf-168">Zie de lijst met [ondersteunde tokens](#supported-tokens-in-the-email-template) verderop in dit onderwerp.</span><span class="sxs-lookup"><span data-stu-id="695cf-168">See the list of [supported tokens](#supported-tokens-in-the-email-template) later in this topic.</span></span>
1. <span data-ttu-id="695cf-169">Meld u aan bij Commerce.</span><span class="sxs-lookup"><span data-stu-id="695cf-169">Sign in to Commerce.</span></span>
1. <span data-ttu-id="695cf-170">Ga in het menu links naar **Modules \> Organisatiebeheer \> Instellingen \> E-mailsjablonen van organisatie**.</span><span class="sxs-lookup"><span data-stu-id="695cf-170">Use the menu on the left to go to **Modules \> Organization administration \> Setup \> Organization email templates**.</span></span>
1. <span data-ttu-id="695cf-171">Vouw de lijst links uit om alle sjablonen te bekijken.</span><span class="sxs-lookup"><span data-stu-id="695cf-171">Expand the list on the left to see all the templates.</span></span>
1. <span data-ttu-id="695cf-172">Voer de volgende stappen uit voor elke sjabloon die u wilt aanpassen:</span><span class="sxs-lookup"><span data-stu-id="695cf-172">For each template that you want to customize, follow these steps:</span></span>

    1. <span data-ttu-id="695cf-173">Selecteer de sjabloon in de lijst.</span><span class="sxs-lookup"><span data-stu-id="695cf-173">Select the template in the list.</span></span>
    1. <span data-ttu-id="695cf-174">Selecteer onder **Inhoud van e-mailbericht** de toepasselijke taalversie in de lijst.</span><span class="sxs-lookup"><span data-stu-id="695cf-174">Under **Email message content**, select the appropriate language version in the list.</span></span> <span data-ttu-id="695cf-175">De standaardtaal is **en-us**.</span><span class="sxs-lookup"><span data-stu-id="695cf-175">(The default language is **en-us**.)</span></span>
    1. <span data-ttu-id="695cf-176">Selecteer **Bewerken** onder **Inhoud van e-mailbericht**.</span><span class="sxs-lookup"><span data-stu-id="695cf-176">Under **Email message content**, select **Edit**.</span></span> <span data-ttu-id="695cf-177">Het deelvenster **E-mailsjabloon uploaden** wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="695cf-177">The **Upload email template** pane appears.</span></span>
    1. <span data-ttu-id="695cf-178">Selecteer **Bladeren** en zoek het HTML-bestand met de aangepaste inhoud.</span><span class="sxs-lookup"><span data-stu-id="695cf-178">Select **Browse**, and find the HTML file that has the customized content.</span></span>
    1. <span data-ttu-id="695cf-179">Selecteer **Uploaden**.</span><span class="sxs-lookup"><span data-stu-id="695cf-179">Select **Upload**.</span></span> <span data-ttu-id="695cf-180">De sjabloon wordt geüpload naar het systeem en er wordt een voorbeeld weergegeven.</span><span class="sxs-lookup"><span data-stu-id="695cf-180">The template is uploaded into the system, and a preview is shown.</span></span>
    1. <span data-ttu-id="695cf-181">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="695cf-181">Select **OK**.</span></span>
    1. <span data-ttu-id="695cf-182">Optioneel: pas de eigenschap **Onderwerp** van de sjabloon aan.</span><span class="sxs-lookup"><span data-stu-id="695cf-182">Optional: Customize the **Subject** property of the template.</span></span>
    1. <span data-ttu-id="695cf-183">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="695cf-183">Select **Save**.</span></span>

### <a name="supported-tokens-in-the-email-template"></a><span data-ttu-id="695cf-184">Ondersteunde tokens in de e-mailsjabloon</span><span class="sxs-lookup"><span data-stu-id="695cf-184">Supported tokens in the email template</span></span>

<span data-ttu-id="695cf-185">Als de e-mail wordt weergegeven, worden deze tokens vervangen door de werkelijke waarden die van toepassing zijn op de klant en de klantorder.</span><span class="sxs-lookup"><span data-stu-id="695cf-185">When the email is rendered, these tokens are replaced with actual values that apply to the customer and the customer's order.</span></span>

#### <a name="sales-order"></a><span data-ttu-id="695cf-186">Verkooporder</span><span class="sxs-lookup"><span data-stu-id="695cf-186">Sales order</span></span>

<span data-ttu-id="695cf-187">De volgende tokens gelden voor de algehele verkooporder.</span><span class="sxs-lookup"><span data-stu-id="695cf-187">The following tokens apply to the overall sales order.</span></span>

| <span data-ttu-id="695cf-188">Naam van token</span><span class="sxs-lookup"><span data-stu-id="695cf-188">Name of the token</span></span> | <span data-ttu-id="695cf-189">Token </span><span class="sxs-lookup"><span data-stu-id="695cf-189">Token</span></span> |
|-------------------|-------|
| <span data-ttu-id="695cf-190">Ordernummer</span><span class="sxs-lookup"><span data-stu-id="695cf-190">Order number</span></span>      | <span data-ttu-id="695cf-191">%salesid%</span><span class="sxs-lookup"><span data-stu-id="695cf-191">%salesid%</span></span> |
| <span data-ttu-id="695cf-192">Naam van klant</span><span class="sxs-lookup"><span data-stu-id="695cf-192">Customer's name</span></span>   | <span data-ttu-id="695cf-193">%customername%</span><span class="sxs-lookup"><span data-stu-id="695cf-193">%customername%</span></span> |
| <span data-ttu-id="695cf-194">Afleveradres</span><span class="sxs-lookup"><span data-stu-id="695cf-194">Delivery address</span></span>  | <span data-ttu-id="695cf-195">%deliveryaddress%</span><span class="sxs-lookup"><span data-stu-id="695cf-195">%deliveryaddress%</span></span> |
| <span data-ttu-id="695cf-196">Factureringsadres</span><span class="sxs-lookup"><span data-stu-id="695cf-196">Billing address</span></span>   | <span data-ttu-id="695cf-197">%customeraddress%</span><span class="sxs-lookup"><span data-stu-id="695cf-197">%customeraddress%</span></span> |
| <span data-ttu-id="695cf-198">Besteldatum</span><span class="sxs-lookup"><span data-stu-id="695cf-198">Order date</span></span>        | <span data-ttu-id="695cf-199">%shipdate%</span><span class="sxs-lookup"><span data-stu-id="695cf-199">%shipdate%</span></span> |
| <span data-ttu-id="695cf-200">Bezorgingsmodus</span><span class="sxs-lookup"><span data-stu-id="695cf-200">Delivery mode</span></span>     | <span data-ttu-id="695cf-201">%modeofdelivery%</span><span class="sxs-lookup"><span data-stu-id="695cf-201">%modeofdelivery%</span></span> |
| <span data-ttu-id="695cf-202">Korting</span><span class="sxs-lookup"><span data-stu-id="695cf-202">Discount</span></span>          | <span data-ttu-id="695cf-203">%discount%</span><span class="sxs-lookup"><span data-stu-id="695cf-203">%discount%</span></span> |
| <span data-ttu-id="695cf-204">Btw</span><span class="sxs-lookup"><span data-stu-id="695cf-204">Sales tax</span></span>         | <span data-ttu-id="695cf-205">%tax%</span><span class="sxs-lookup"><span data-stu-id="695cf-205">%tax%</span></span> |
| <span data-ttu-id="695cf-206">Ordertotaal</span><span class="sxs-lookup"><span data-stu-id="695cf-206">Order total</span></span>       | <span data-ttu-id="695cf-207">%total%</span><span class="sxs-lookup"><span data-stu-id="695cf-207">%total%</span></span> |

#### <a name="sales-line"></a><span data-ttu-id="695cf-208">Verkoopregel</span><span class="sxs-lookup"><span data-stu-id="695cf-208">Sales line</span></span>

<span data-ttu-id="695cf-209">De volgende tokens worden voor elk product in de order vervangen door waarden.</span><span class="sxs-lookup"><span data-stu-id="695cf-209">The following tokens are replaced with values for each product in the order.</span></span>

> [!NOTE]
> <span data-ttu-id="695cf-210">Plaats het token **Productlijst - begin** aan het begin van het HTML-blok dat wordt herhaald voor elk product en plaats het token **Productlijst - eind** aan het einde van het blok.</span><span class="sxs-lookup"><span data-stu-id="695cf-210">Put the **Product list - start** token at the beginning of the HTML block that is repeated for every product, and put the **Product list - end** token at the end of the block.</span></span>

| <span data-ttu-id="695cf-211">Naam van token</span><span class="sxs-lookup"><span data-stu-id="695cf-211">Name of the token</span></span>      | <span data-ttu-id="695cf-212">Token</span><span class="sxs-lookup"><span data-stu-id="695cf-212">Token</span></span> |
|------------------------|-------|
| <span data-ttu-id="695cf-213">Productlijst - begin</span><span class="sxs-lookup"><span data-stu-id="695cf-213">Product list - start</span></span>   | \<!--%tablebegin.salesline% --\> |
| <span data-ttu-id="695cf-214">Productlijst - eind</span><span class="sxs-lookup"><span data-stu-id="695cf-214">Product list - end</span></span>     | \<!--%tableend.salesline%--\> |
| <span data-ttu-id="695cf-215">Productnaam</span><span class="sxs-lookup"><span data-stu-id="695cf-215">Product name</span></span>           | <span data-ttu-id="695cf-216">%lineproductname%</span><span class="sxs-lookup"><span data-stu-id="695cf-216">%lineproductname%</span></span> |
| <span data-ttu-id="695cf-217">Omschrijving</span><span class="sxs-lookup"><span data-stu-id="695cf-217">Description</span></span>            | <span data-ttu-id="695cf-218">%lineproductdescription%</span><span class="sxs-lookup"><span data-stu-id="695cf-218">%lineproductdescription%</span></span> |
| <span data-ttu-id="695cf-219">Hoeveelheid</span><span class="sxs-lookup"><span data-stu-id="695cf-219">Quantity</span></span>               | <span data-ttu-id="695cf-220">%linequantity%</span><span class="sxs-lookup"><span data-stu-id="695cf-220">%linequantity%</span></span> |
| <span data-ttu-id="695cf-221">Regel met eenheidsprijs</span><span class="sxs-lookup"><span data-stu-id="695cf-221">Line unit price</span></span>        | <span data-ttu-id="695cf-222">%lineprice% (controleren)</span><span class="sxs-lookup"><span data-stu-id="695cf-222">%lineprice% (verify)</span></span> |
| <span data-ttu-id="695cf-223">totaal regelartikel</span><span class="sxs-lookup"><span data-stu-id="695cf-223">line item total</span></span>        | <span data-ttu-id="695cf-224">%linenetamount%</span><span class="sxs-lookup"><span data-stu-id="695cf-224">%linenetamount%</span></span> |
| <span data-ttu-id="695cf-225">regelkorting</span><span class="sxs-lookup"><span data-stu-id="695cf-225">line discount</span></span>          | <span data-ttu-id="695cf-226">%linediscount%</span><span class="sxs-lookup"><span data-stu-id="695cf-226">%linediscount%</span></span> |
| <span data-ttu-id="695cf-227">Verzenddatum</span><span class="sxs-lookup"><span data-stu-id="695cf-227">Ship date</span></span>              | <span data-ttu-id="695cf-228">%lineshipdate%</span><span class="sxs-lookup"><span data-stu-id="695cf-228">%lineshipdate%</span></span> |
| <span data-ttu-id="695cf-229">Aanschaffingsmethode</span><span class="sxs-lookup"><span data-stu-id="695cf-229">Procurement method</span></span>     | <span data-ttu-id="695cf-230">%linedeliverymode%</span><span class="sxs-lookup"><span data-stu-id="695cf-230">%linedeliverymode%</span></span> |
| <span data-ttu-id="695cf-231">afleveradres</span><span class="sxs-lookup"><span data-stu-id="695cf-231">delivery address</span></span>       | <span data-ttu-id="695cf-232">%linedeliveryaddress%</span><span class="sxs-lookup"><span data-stu-id="695cf-232">%linedeliveryaddress%</span></span> |
| <span data-ttu-id="695cf-233">Verkoopeenheid van regel</span><span class="sxs-lookup"><span data-stu-id="695cf-233">Sales unit of the line</span></span> | <span data-ttu-id="695cf-234">%lineunit%</span><span class="sxs-lookup"><span data-stu-id="695cf-234">%lineunit%</span></span> |

## <a name="additional-resources"></a><span data-ttu-id="695cf-235">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="695cf-235">Additional resources</span></span>

[<span data-ttu-id="695cf-236">Overzicht van de evaluatieomgeving voor Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="695cf-236">Dynamics 365 Commerce evaluation environment overview</span></span>](cpe-overview.md)

[<span data-ttu-id="695cf-237">Een evaluatieomgeving voor Dynamics 365 Commerce inrichten</span><span class="sxs-lookup"><span data-stu-id="695cf-237">Provision a Dynamics 365 Commerce evaluation environment</span></span>](provisioning-guide.md)

[<span data-ttu-id="695cf-238">Een Dynamics 365 Commerce-evaluatieomgeving configureren</span><span class="sxs-lookup"><span data-stu-id="695cf-238">Configure a Dynamics 365 Commerce evaluation environment</span></span>](cpe-post-provisioning.md)

[<span data-ttu-id="695cf-239">BOPIS configureren in een Dynamics 365 Commerce-evaluatieomgeving</span><span class="sxs-lookup"><span data-stu-id="695cf-239">Configure BOPIS in a Dynamics 365 Commerce evaluation environment</span></span>](cpe-bopis.md)

[<span data-ttu-id="695cf-240">Veelgestelde vragen over evaluatieomgeving voor Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="695cf-240">Dynamics 365 Commerce evaluation environment FAQ</span></span>](cpe-faq.md)

[<span data-ttu-id="695cf-241">Microsoft Lifecycle Services (LCS)</span><span class="sxs-lookup"><span data-stu-id="695cf-241">Microsoft Lifecycle Services (LCS)</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[<span data-ttu-id="695cf-242">Retail Cloud Scale Unit (RCSU)</span><span class="sxs-lookup"><span data-stu-id="695cf-242">Retail Cloud Scale Unit (RCSU)</span></span>](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[<span data-ttu-id="695cf-243">Microsoft Azure-portal</span><span class="sxs-lookup"><span data-stu-id="695cf-243">Microsoft Azure portal</span></span>](https://azure.microsoft.com/features/azure-portal)

[<span data-ttu-id="695cf-244">Dynamics 365 Commerce-website</span><span class="sxs-lookup"><span data-stu-id="695cf-244">Dynamics 365 Commerce website</span></span>](https://aka.ms/Dynamics365CommerceWebsite)
