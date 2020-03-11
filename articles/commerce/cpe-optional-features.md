---
title: Optionele functies voor een Dynamics 365 Commerce-previewomgeving configureren
description: In dit onderwerp wordt uitgelegd hoe u optionele functies voor een preview-omgeving van Microsoft Dynamics 365 Commerce configureert.
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
ms.openlocfilehash: 4b17f8e9b0d8a9a62714d0073561e66642b2eaf9
ms.sourcegitcommit: 12b9d6f2dd24e52e46487748c848864909af6967
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/14/2020
ms.locfileid: "3057735"
---
# <a name="configure-optional-features-for-a-dynamics-365-commerce-preview-environment"></a><span data-ttu-id="b9d73-103">Optionele functies voor een Dynamics 365 Commerce-previewomgeving configureren</span><span class="sxs-lookup"><span data-stu-id="b9d73-103">Configure optional features for a Dynamics 365 Commerce preview environment</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="b9d73-104">In dit onderwerp wordt uitgelegd hoe u optionele functies voor een preview-omgeving van Microsoft Dynamics 365 Commerce configureert.</span><span class="sxs-lookup"><span data-stu-id="b9d73-104">This topic explains how to configure optional features for a Microsoft Dynamics 365 Commerce preview environment.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="b9d73-105">Vereisten</span><span class="sxs-lookup"><span data-stu-id="b9d73-105">Prerequisites</span></span>

<span data-ttu-id="b9d73-106">Als u de transactionele e-mailfuncties wilt evalueren, moet aan de volgende voorwaarden worden voldaan:</span><span class="sxs-lookup"><span data-stu-id="b9d73-106">If you want to evaluate the transactional email features, the following prerequisites must be met:</span></span>

- <span data-ttu-id="b9d73-107">U hebt een e-mailserver beschikbaar (\[SMTP\]-server), die kan worden gebruikt vanuit het Microsoft Azure-abonnement waarin u de preview-omgeving inricht.</span><span class="sxs-lookup"><span data-stu-id="b9d73-107">You have an available email server (Simple Mail Transfer Protocol \[SMTP\] server) that can be used from the Microsoft Azure subscription where you provisioned the preview environment.</span></span>
- <span data-ttu-id="b9d73-108">U hebt het FQDN/IP-adres, het SMTP-poortnummer en de verificatiegegevens van de server beschikbaar.</span><span class="sxs-lookup"><span data-stu-id="b9d73-108">You have the server's fully qualified domain name (FQDN)/IP address, SMTP port number, and authentication details available.</span></span>

<span data-ttu-id="b9d73-109">Als u functies voor beheer van digitale activa wilt evalueren door nieuwe Omnichannel-afbeeldingen op te nemen, moet u de naam van uw CMS-tenant (contentmanagementsysteem) beschikbaar hebben.</span><span class="sxs-lookup"><span data-stu-id="b9d73-109">If you want to evaluate Digital Asset Management features by ingesting new omni-channel images, you must have the name of your content management system (CMS) tenant available.</span></span> <span data-ttu-id="b9d73-110">Instructies voor het vinden van deze naam vindt u verderop in dit onderwerp.</span><span class="sxs-lookup"><span data-stu-id="b9d73-110">Instructions for finding this name are provided later in this topic.</span></span> <span data-ttu-id="b9d73-111">>>>(V: waar zijn de instructies?)</span><span class="sxs-lookup"><span data-stu-id="b9d73-111">>>>(Q: where are the instructions?)</span></span>

## <a name="configure-the-image-back-end"></a><span data-ttu-id="b9d73-112">De backend van de afbeelding configureren</span><span class="sxs-lookup"><span data-stu-id="b9d73-112">Configure the image back end</span></span>

### <a name="find-your-media-base-url"></a><span data-ttu-id="b9d73-113">Uw basis-URL voor media vinden</span><span class="sxs-lookup"><span data-stu-id="b9d73-113">Find your media base URL</span></span>

> [!NOTE]
> <span data-ttu-id="b9d73-114">Voordat u deze procedure kunt uitvoeren, moet u de stappen in [Uw site instellen in Commerce](cpe-post-provisioning.md#set-up-your-site-in-commerce) voltooien.</span><span class="sxs-lookup"><span data-stu-id="b9d73-114">Before you can complete this procedure, you must complete the steps in [Set up your site in Commerce](cpe-post-provisioning.md#set-up-your-site-in-commerce).</span></span>

1. <span data-ttu-id="b9d73-115">Meld u aan bij het beheerhulpprogramma van de e-Commerce-site met de URL die u hebt genoteerd tijdens de initialisatie van e-Commerce tijdens het inrichten (zie [e-Commerce initialiseren](provisioning-guide.md#initialize-e-commerce)).</span><span class="sxs-lookup"><span data-stu-id="b9d73-115">Sign in to the Commerce site management tool by using the URL you made a note of when you initialized e-Commerce during provisioning (see [Initialize e-Commerce](provisioning-guide.md#initialize-e-commerce)).</span></span>
1. <span data-ttu-id="b9d73-116">Open de site **Fabrikam**.</span><span class="sxs-lookup"><span data-stu-id="b9d73-116">Open the **Fabrikam** site.</span></span>
1. <span data-ttu-id="b9d73-117">Selecteer **Activa** in het linkermenu.</span><span class="sxs-lookup"><span data-stu-id="b9d73-117">On the menu on the left, select **Assets**.</span></span>
1. <span data-ttu-id="b9d73-118">Selecteer één afbeeldingsactivum.</span><span class="sxs-lookup"><span data-stu-id="b9d73-118">Select any single image asset.</span></span>
1. <span data-ttu-id="b9d73-119">Zoek in de eigenschappencontrole aan de rechterkant de eigenschap **Openbare URL**.</span><span class="sxs-lookup"><span data-stu-id="b9d73-119">In the property inspector on the right, find the **Public URL** property.</span></span> <span data-ttu-id="b9d73-120">De waarde is een URL.</span><span class="sxs-lookup"><span data-stu-id="b9d73-120">The value is a URL.</span></span> <span data-ttu-id="b9d73-121">Dit is een voorbeeld:</span><span class="sxs-lookup"><span data-stu-id="b9d73-121">Here is an example:</span></span>

    <span data-ttu-id="b9d73-122">`https://images-us-sb.cms.commerce.dynamics.com/cms/api/fabrikam/imageFileData/MA1nQC`.</span><span class="sxs-lookup"><span data-stu-id="b9d73-122">`https://images-us-sb.cms.commerce.dynamics.com/cms/api/fabrikam/imageFileData/MA1nQC`.</span></span>

1. <span data-ttu-id="b9d73-123">Vervang de laatste id in de URL (**MA1nQC** in het voorbeeld hierboven) door de volgende tekenreeks: **search?fileName=**.</span><span class="sxs-lookup"><span data-stu-id="b9d73-123">Replace the last identifier in the URL (**MA1nQC** in the preceding example) with the string **search?fileName=**.</span></span> <span data-ttu-id="b9d73-124">De voorbeeld-URL ziet er zo uit nadat deze wijziging is doorgevoerd:</span><span class="sxs-lookup"><span data-stu-id="b9d73-124">Here is what the example URL looks like after this change is made:</span></span>

    `https://images-us-sb.cms.commerce.dynamics.com/cms/api/fabrikam/imageFileData/search?fileName=`

    <span data-ttu-id="b9d73-125">Deze URL is uw basis-URL voor media.</span><span class="sxs-lookup"><span data-stu-id="b9d73-125">This URL is your media base URL.</span></span> <span data-ttu-id="b9d73-126">Noteer deze.</span><span class="sxs-lookup"><span data-stu-id="b9d73-126">Make a note of it.</span></span>

### <a name="update-the-media-base-url"></a><span data-ttu-id="b9d73-127">De basis-URL voor media bijwerken</span><span class="sxs-lookup"><span data-stu-id="b9d73-127">Update the media base URL</span></span>

1. <span data-ttu-id="b9d73-128">Meld u aan bij Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="b9d73-128">Sign in to Dynamics 365 Commerce.</span></span>
1. <span data-ttu-id="b9d73-129">Ga in het menu links naar **Modules \> Detailhandel en commerce \> Afzetkanaalinstellingen \> Afzetkanaalprofielen**.</span><span class="sxs-lookup"><span data-stu-id="b9d73-129">Use the menu on the left to go to **Modules \> Retail and commerce \> Channel setup \> Channel profiles**.</span></span>
1. <span data-ttu-id="b9d73-130">Selecteer **Bewerken**.</span><span class="sxs-lookup"><span data-stu-id="b9d73-130">Select **Edit**.</span></span>
1. <span data-ttu-id="b9d73-131">Vervang onder **Profieleigenschappen** de waarde voor **Basis-URL voor mediaserver** door de basis-URL voor media die u eerder hebt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="b9d73-131">Under **Profile properties**, replace the value for the **Media Server Base URL** property with the media base URL that you created earlier.</span></span>
1. <span data-ttu-id="b9d73-132">Selecteer het andere kanaal in de lijst aan de linkerkant, onder het **standaardkanaal**.</span><span class="sxs-lookup"><span data-stu-id="b9d73-132">In the list on the left, under the **Default** channel, select the other channel.</span></span>
1. <span data-ttu-id="b9d73-133">Selecteer onder **Profieleigenschappen** de optie **Toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="b9d73-133">Under **Profile properties**, select **Add**.</span></span>
1. <span data-ttu-id="b9d73-134">Voor de eigenschap die is toegevoegd, selecteert **Basis-URL voor mediaserver** als de eigenschapssleutel.</span><span class="sxs-lookup"><span data-stu-id="b9d73-134">For the property that was added, select **Media Server Base URL** as the property key.</span></span> <span data-ttu-id="b9d73-135">Voer als de waarde van de eigenschap de basis-URL voor de media in die u eerder hebt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="b9d73-135">As the property value, enter the media base URL that you created earlier.</span></span>
1. <span data-ttu-id="b9d73-136">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="b9d73-136">Select **Save**.</span></span>

## <a name="configure-the-email-server"></a><span data-ttu-id="b9d73-137">De e-mailserver configureren</span><span class="sxs-lookup"><span data-stu-id="b9d73-137">Configure the email server</span></span>

> [!NOTE]
> <span data-ttu-id="b9d73-138">De SMTP-server of e-mailservice die u hier invoert, moet toegankelijk zijn vanuit het Azure-abonnement dat u voor de omgeving gebruikt.</span><span class="sxs-lookup"><span data-stu-id="b9d73-138">The SMTP server or email service that you enter here must be accessible from the Azure subscription that you're using for the environment.</span></span>

1. <span data-ttu-id="b9d73-139">Meld u aan bij Commerce.</span><span class="sxs-lookup"><span data-stu-id="b9d73-139">Sign in to Commerce.</span></span>
1. <span data-ttu-id="b9d73-140">Ga in het menu links naar **Modules \> Systeembeheer \> Instellingen \> E-mail \> E-mailparameters**.</span><span class="sxs-lookup"><span data-stu-id="b9d73-140">Use the menu on the left to go to **Modules \> System administration \> Setup \> Email \> Email parameters**.</span></span>
1. <span data-ttu-id="b9d73-141">Voer op het tabblad **SMTP-instellingen** in het veld **Naam SMTP-relaisserver** de FQDN-naam of het IP-adres in van de SMTP-server of e-mailservice.</span><span class="sxs-lookup"><span data-stu-id="b9d73-141">On the **SMTP settings** tab, in the **Outgoing mail server** field, enter the FQDN or IP address of your SMTP server or email service.</span></span>
1. <span data-ttu-id="b9d73-142">Voer in het veld **SMTP-poortnummer** het poortnummer in.</span><span class="sxs-lookup"><span data-stu-id="b9d73-142">In the **SMTP port number** field, enter the port number.</span></span> <span data-ttu-id="b9d73-143">(Als u SSL \[Secure Sockets Layer \] gebruikt, is het standaardpoortnummer **25**.)</span><span class="sxs-lookup"><span data-stu-id="b9d73-143">(If you aren't using Secure Sockets Layer \[SSL\], the default port number is **25**.)</span></span>
1. <span data-ttu-id="b9d73-144">Als verificatie vereist is, voert u waarden in de velden **Gebruikersnaam** en **Wachtwoord** in.</span><span class="sxs-lookup"><span data-stu-id="b9d73-144">If authentication is required, enter values in the **User name** and **Password** fields.</span></span>
1. <span data-ttu-id="b9d73-145">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="b9d73-145">Select **Save**.</span></span>
1. <span data-ttu-id="b9d73-146">Selecteer **Vernieuwen**.</span><span class="sxs-lookup"><span data-stu-id="b9d73-146">Select **Refresh**.</span></span>
1. <span data-ttu-id="b9d73-147">Selecteer op het tabblad **Testbericht** in het veld **E-mailprovider** de optie **SMTP**.</span><span class="sxs-lookup"><span data-stu-id="b9d73-147">On the **Test email** tab, in the **Email provider** field, select **SMTP**.</span></span>
1. <span data-ttu-id="b9d73-148">Voer in het veld **Verzenden naar** het e-mailadres in waar u het testbericht wilt afleveren.</span><span class="sxs-lookup"><span data-stu-id="b9d73-148">In the **Send to** field, enter the email address that the test email should be delivered to.</span></span>
1. <span data-ttu-id="b9d73-149">Selecteer **Testbericht verzenden**.</span><span class="sxs-lookup"><span data-stu-id="b9d73-149">Select **Send test email**.</span></span>

## <a name="configure-email-templates"></a><span data-ttu-id="b9d73-150">E-mailsjablonen configureren</span><span class="sxs-lookup"><span data-stu-id="b9d73-150">Configure email templates</span></span>

<span data-ttu-id="b9d73-151">Voor elke transactionele gebeurtenis waarvoor u e-mailberichten wilt verzenden, moet u de e-mailsjabloon bijwerken met een geldig e-mailadres van de afzender.</span><span class="sxs-lookup"><span data-stu-id="b9d73-151">For each transactional event that you want to send emails for, you must update the email template with a valid sender email address.</span></span>

1. <span data-ttu-id="b9d73-152">Meld u aan bij Commerce.</span><span class="sxs-lookup"><span data-stu-id="b9d73-152">Sign in to Commerce.</span></span>
1. <span data-ttu-id="b9d73-153">Ga in het menu links naar **Modules \> Organisatiebeheer \> Instellingen \> E-mailsjablonen van organisatie**.</span><span class="sxs-lookup"><span data-stu-id="b9d73-153">Use the menu on the left to go to **Modules \> Organization administration \> Setup \> Organization email templates**.</span></span>
1. <span data-ttu-id="b9d73-154">Selecteer **Lijst weergeven**.</span><span class="sxs-lookup"><span data-stu-id="b9d73-154">Select **Show list**.</span></span>
1. <span data-ttu-id="b9d73-155">Volg deze stappen voor elke sjabloon in de lijst:</span><span class="sxs-lookup"><span data-stu-id="b9d73-155">For each template in the list, follow these steps:</span></span>

    1. <span data-ttu-id="b9d73-156">Voer in het veld **E-mailadres afzender** het e-mailadres van de afzender in.</span><span class="sxs-lookup"><span data-stu-id="b9d73-156">In the **Sender email** field, enter the sender email address.</span></span>
    1. <span data-ttu-id="b9d73-157">Optioneel: voer in het veld **Naam van afzender** de naam in die moet worden gebruikt als de naam van de afzender.</span><span class="sxs-lookup"><span data-stu-id="b9d73-157">Optional: In the **Sender name** field, enter the name that should be used as the sender name.</span></span>

1. <span data-ttu-id="b9d73-158">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="b9d73-158">Select **Save**.</span></span>

## <a name="customize-email-templates"></a><span data-ttu-id="b9d73-159">E-mailsjablonen aanpassen</span><span class="sxs-lookup"><span data-stu-id="b9d73-159">Customize email templates</span></span>

<span data-ttu-id="b9d73-160">Mogelijk wilt u de e-mailsjablonen aanpassen zodat deze verschillende afbeeldingen gebruiken.</span><span class="sxs-lookup"><span data-stu-id="b9d73-160">You might want to customize the email templates so that they use different images.</span></span> <span data-ttu-id="b9d73-161">U kunt ook de koppelingen in de sjablonen bijwerken, zodat deze naar uw preview-omgeving leiden.</span><span class="sxs-lookup"><span data-stu-id="b9d73-161">Or you might want to update the links in the templates so that they go to your preview environment.</span></span> <span data-ttu-id="b9d73-162">In deze procedure wordt uitgelegd hoe u de standaardsjablonen kunt downloaden, aanpassen en bijwerken in het systeem.</span><span class="sxs-lookup"><span data-stu-id="b9d73-162">This procedure explains how to download the default templates, customize them, and update the templates in the system.</span></span>

1. <span data-ttu-id="b9d73-163">Download via een webbrowser [het zipbestand met standaard e-mailsjablonen voor Microsoft Dynamics 365 Commerce Preview](https://download.microsoft.com/download/d/7/b/d7b6c4d4-fe09-4922-9551-46bbb29d202d/Commerce.Preview.Default.Email.Templates.zip) naar uw lokale computer.</span><span class="sxs-lookup"><span data-stu-id="b9d73-163">In a web browser, download the [Microsoft Dynamics 365 Commerce Preview default email templates zip file](https://download.microsoft.com/download/d/7/b/d7b6c4d4-fe09-4922-9551-46bbb29d202d/Commerce.Preview.Default.Email.Templates.zip) to your local computer.</span></span> <span data-ttu-id="b9d73-164">Dit bestand bevat de volgende HTML-documenten:</span><span class="sxs-lookup"><span data-stu-id="b9d73-164">This file contains the following HTML documents:</span></span>

    - <span data-ttu-id="b9d73-165">Sjabloon voor orderbevestiging</span><span class="sxs-lookup"><span data-stu-id="b9d73-165">Order confirmation template</span></span>
    - <span data-ttu-id="b9d73-166">Sjabloon voor uitgifte van geschenkbon</span><span class="sxs-lookup"><span data-stu-id="b9d73-166">Issue gift card template</span></span>
    - <span data-ttu-id="b9d73-167">Sjabloon voor nieuwe order</span><span class="sxs-lookup"><span data-stu-id="b9d73-167">New order template</span></span>
    - <span data-ttu-id="b9d73-168">Sjabloon voor verpakkingsorder</span><span class="sxs-lookup"><span data-stu-id="b9d73-168">Pack order template</span></span>
    - <span data-ttu-id="b9d73-169">Sjabloon voor orderverzameling</span><span class="sxs-lookup"><span data-stu-id="b9d73-169">Pick order template</span></span>

1. <span data-ttu-id="b9d73-170">Pas de sjablonen aan met een tekst- of HTML-editor.</span><span class="sxs-lookup"><span data-stu-id="b9d73-170">Customize the templates by using a text or HTML editor.</span></span> <span data-ttu-id="b9d73-171">Zie de lijst met [ondersteunde tokens](#supported-tokens-in-the-email-template) verderop in dit onderwerp.</span><span class="sxs-lookup"><span data-stu-id="b9d73-171">See the list of [supported tokens](#supported-tokens-in-the-email-template) later in this topic.</span></span>
1. <span data-ttu-id="b9d73-172">Meld u aan bij Commerce.</span><span class="sxs-lookup"><span data-stu-id="b9d73-172">Sign in to Commerce.</span></span>
1. <span data-ttu-id="b9d73-173">Ga in het menu links naar **Modules \> Organisatiebeheer \> Instellingen \> E-mailsjablonen van organisatie**.</span><span class="sxs-lookup"><span data-stu-id="b9d73-173">Use the menu on the left to go to **Modules \> Organization administration \> Setup \> Organization email templates**.</span></span>
1. <span data-ttu-id="b9d73-174">Vouw de lijst links uit om alle sjablonen te bekijken.</span><span class="sxs-lookup"><span data-stu-id="b9d73-174">Expand the list on the left to see all the templates.</span></span>
1. <span data-ttu-id="b9d73-175">Voer de volgende stappen uit voor elke sjabloon die u wilt aanpassen:</span><span class="sxs-lookup"><span data-stu-id="b9d73-175">For each template that you want to customize, follow these steps:</span></span>

    1. <span data-ttu-id="b9d73-176">Selecteer de sjabloon in de lijst.</span><span class="sxs-lookup"><span data-stu-id="b9d73-176">Select the template in the list.</span></span>
    1. <span data-ttu-id="b9d73-177">Selecteer onder **Inhoud van e-mailbericht** de toepasselijke taalversie in de lijst.</span><span class="sxs-lookup"><span data-stu-id="b9d73-177">Under **Email message content**, select the appropriate language version in the list.</span></span> <span data-ttu-id="b9d73-178">De standaardtaal is **en-us**.</span><span class="sxs-lookup"><span data-stu-id="b9d73-178">(The default language is **en-us**.)</span></span>
    1. <span data-ttu-id="b9d73-179">Selecteer **Bewerken** onder **Inhoud van e-mailbericht**.</span><span class="sxs-lookup"><span data-stu-id="b9d73-179">Under **Email message content**, select **Edit**.</span></span> <span data-ttu-id="b9d73-180">Het deelvenster **E-mailsjabloon uploaden** wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="b9d73-180">The **Upload email template** pane appears.</span></span>
    1. <span data-ttu-id="b9d73-181">Selecteer **Bladeren** en zoek het HTML-bestand met de aangepaste inhoud.</span><span class="sxs-lookup"><span data-stu-id="b9d73-181">Select **Browse**, and find the HTML file that has the customized content.</span></span>
    1. <span data-ttu-id="b9d73-182">Selecteer **Uploaden**.</span><span class="sxs-lookup"><span data-stu-id="b9d73-182">Select **Upload**.</span></span> <span data-ttu-id="b9d73-183">De sjabloon wordt geüpload naar het systeem en er wordt een voorbeeld weergegeven.</span><span class="sxs-lookup"><span data-stu-id="b9d73-183">The template is uploaded into the system, and a preview is shown.</span></span>
    1. <span data-ttu-id="b9d73-184">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="b9d73-184">Select **OK**.</span></span>
    1. <span data-ttu-id="b9d73-185">Optioneel: pas de eigenschap **Onderwerp** van de sjabloon aan.</span><span class="sxs-lookup"><span data-stu-id="b9d73-185">Optional: Customize the **Subject** property of the template.</span></span>
    1. <span data-ttu-id="b9d73-186">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="b9d73-186">Select **Save**.</span></span>

### <a name="supported-tokens-in-the-email-template"></a><span data-ttu-id="b9d73-187">Ondersteunde tokens in de e-mailsjabloon</span><span class="sxs-lookup"><span data-stu-id="b9d73-187">Supported tokens in the email template</span></span>

<span data-ttu-id="b9d73-188">Als de e-mail wordt weergegeven, worden deze tokens vervangen door de werkelijke waarden die van toepassing zijn op de klant en de klantorder.</span><span class="sxs-lookup"><span data-stu-id="b9d73-188">When the email is rendered, these tokens are replaced with actual values that apply to the customer and the customer's order.</span></span>

#### <a name="sales-order"></a><span data-ttu-id="b9d73-189">Verkooporder</span><span class="sxs-lookup"><span data-stu-id="b9d73-189">Sales order</span></span>

<span data-ttu-id="b9d73-190">De volgende tokens gelden voor de algehele verkooporder.</span><span class="sxs-lookup"><span data-stu-id="b9d73-190">The following tokens apply to the overall sales order.</span></span>

| <span data-ttu-id="b9d73-191">Naam van token</span><span class="sxs-lookup"><span data-stu-id="b9d73-191">Name of the token</span></span> | <span data-ttu-id="b9d73-192">Token </span><span class="sxs-lookup"><span data-stu-id="b9d73-192">Token</span></span> |
|-------------------|-------|
| <span data-ttu-id="b9d73-193">Ordernummer</span><span class="sxs-lookup"><span data-stu-id="b9d73-193">Order number</span></span>      | <span data-ttu-id="b9d73-194">%salesid%</span><span class="sxs-lookup"><span data-stu-id="b9d73-194">%salesid%</span></span> |
| <span data-ttu-id="b9d73-195">Naam van klant</span><span class="sxs-lookup"><span data-stu-id="b9d73-195">Customer's name</span></span>   | <span data-ttu-id="b9d73-196">%customername%</span><span class="sxs-lookup"><span data-stu-id="b9d73-196">%customername%</span></span> |
| <span data-ttu-id="b9d73-197">Afleveradres</span><span class="sxs-lookup"><span data-stu-id="b9d73-197">Delivery address</span></span>  | <span data-ttu-id="b9d73-198">%deliveryaddress%</span><span class="sxs-lookup"><span data-stu-id="b9d73-198">%deliveryaddress%</span></span> |
| <span data-ttu-id="b9d73-199">Factureringsadres</span><span class="sxs-lookup"><span data-stu-id="b9d73-199">Billing address</span></span>   | <span data-ttu-id="b9d73-200">%customeraddress%</span><span class="sxs-lookup"><span data-stu-id="b9d73-200">%customeraddress%</span></span> |
| <span data-ttu-id="b9d73-201">Besteldatum</span><span class="sxs-lookup"><span data-stu-id="b9d73-201">Order date</span></span>        | <span data-ttu-id="b9d73-202">%shipdate%</span><span class="sxs-lookup"><span data-stu-id="b9d73-202">%shipdate%</span></span> |
| <span data-ttu-id="b9d73-203">Bezorgingsmodus</span><span class="sxs-lookup"><span data-stu-id="b9d73-203">Delivery mode</span></span>     | <span data-ttu-id="b9d73-204">%modeofdelivery%</span><span class="sxs-lookup"><span data-stu-id="b9d73-204">%modeofdelivery%</span></span> |
| <span data-ttu-id="b9d73-205">Korting</span><span class="sxs-lookup"><span data-stu-id="b9d73-205">Discount</span></span>          | <span data-ttu-id="b9d73-206">%discount%</span><span class="sxs-lookup"><span data-stu-id="b9d73-206">%discount%</span></span> |
| <span data-ttu-id="b9d73-207">Btw</span><span class="sxs-lookup"><span data-stu-id="b9d73-207">Sales tax</span></span>         | <span data-ttu-id="b9d73-208">%tax%</span><span class="sxs-lookup"><span data-stu-id="b9d73-208">%tax%</span></span> |
| <span data-ttu-id="b9d73-209">Ordertotaal</span><span class="sxs-lookup"><span data-stu-id="b9d73-209">Order total</span></span>       | <span data-ttu-id="b9d73-210">%total%</span><span class="sxs-lookup"><span data-stu-id="b9d73-210">%total%</span></span> |

#### <a name="sales-line"></a><span data-ttu-id="b9d73-211">Verkoopregel</span><span class="sxs-lookup"><span data-stu-id="b9d73-211">Sales line</span></span>

<span data-ttu-id="b9d73-212">De volgende tokens worden voor elk product in de order vervangen door waarden.</span><span class="sxs-lookup"><span data-stu-id="b9d73-212">The following tokens are replaced with values for each product in the order.</span></span>

> [!NOTE]
> <span data-ttu-id="b9d73-213">Plaats het token **Productlijst - begin** aan het begin van het HTML-blok dat wordt herhaald voor elk product en plaats het token **Productlijst - eind** aan het einde van het blok.</span><span class="sxs-lookup"><span data-stu-id="b9d73-213">Put the **Product list - start** token at the beginning of the HTML block that is repeated for every product, and put the **Product list - end** token at the end of the block.</span></span>

| <span data-ttu-id="b9d73-214">Naam van token</span><span class="sxs-lookup"><span data-stu-id="b9d73-214">Name of the token</span></span>      | <span data-ttu-id="b9d73-215">Token </span><span class="sxs-lookup"><span data-stu-id="b9d73-215">Token</span></span> |
|------------------------|-------|
| <span data-ttu-id="b9d73-216">Productlijst - begin</span><span class="sxs-lookup"><span data-stu-id="b9d73-216">Product list - start</span></span>   | <span data-ttu-id="b9d73-217">\<!--%tablebegin.salesline% --\></span><span class="sxs-lookup"><span data-stu-id="b9d73-217">\<!--%tablebegin.salesline% --\></span></span> |
| <span data-ttu-id="b9d73-218">Productlijst - eind</span><span class="sxs-lookup"><span data-stu-id="b9d73-218">Product list - end</span></span>     | <span data-ttu-id="b9d73-219">\<!--%tableend.salesline%--\></span><span class="sxs-lookup"><span data-stu-id="b9d73-219">\<!--%tableend.salesline%--\></span></span> |
| <span data-ttu-id="b9d73-220">Productnaam</span><span class="sxs-lookup"><span data-stu-id="b9d73-220">Product name</span></span>           | <span data-ttu-id="b9d73-221">%lineproductname%</span><span class="sxs-lookup"><span data-stu-id="b9d73-221">%lineproductname%</span></span> |
| <span data-ttu-id="b9d73-222">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="b9d73-222">Description</span></span>            | <span data-ttu-id="b9d73-223">%lineproductdescription%</span><span class="sxs-lookup"><span data-stu-id="b9d73-223">%lineproductdescription%</span></span> |
| <span data-ttu-id="b9d73-224">Hoeveelheid</span><span class="sxs-lookup"><span data-stu-id="b9d73-224">Quantity</span></span>               | <span data-ttu-id="b9d73-225">%linequantity%</span><span class="sxs-lookup"><span data-stu-id="b9d73-225">%linequantity%</span></span> |
| <span data-ttu-id="b9d73-226">Regel met eenheidsprijs</span><span class="sxs-lookup"><span data-stu-id="b9d73-226">Line unit price</span></span>        | <span data-ttu-id="b9d73-227">%lineprice% (controleren)</span><span class="sxs-lookup"><span data-stu-id="b9d73-227">%lineprice% (verify)</span></span> |
| <span data-ttu-id="b9d73-228">totaal regelartikel</span><span class="sxs-lookup"><span data-stu-id="b9d73-228">line item total</span></span>        | <span data-ttu-id="b9d73-229">%linenetamount%</span><span class="sxs-lookup"><span data-stu-id="b9d73-229">%linenetamount%</span></span> |
| <span data-ttu-id="b9d73-230">regelkorting</span><span class="sxs-lookup"><span data-stu-id="b9d73-230">line discount</span></span>          | <span data-ttu-id="b9d73-231">%linediscount%</span><span class="sxs-lookup"><span data-stu-id="b9d73-231">%linediscount%</span></span> |
| <span data-ttu-id="b9d73-232">Verzenddatum</span><span class="sxs-lookup"><span data-stu-id="b9d73-232">Ship date</span></span>              | <span data-ttu-id="b9d73-233">%lineshipdate%</span><span class="sxs-lookup"><span data-stu-id="b9d73-233">%lineshipdate%</span></span> |
| <span data-ttu-id="b9d73-234">Aanschaffingsmethode</span><span class="sxs-lookup"><span data-stu-id="b9d73-234">Procurement method</span></span>     | <span data-ttu-id="b9d73-235">%linedeliverymode%</span><span class="sxs-lookup"><span data-stu-id="b9d73-235">%linedeliverymode%</span></span> |
| <span data-ttu-id="b9d73-236">afleveradres</span><span class="sxs-lookup"><span data-stu-id="b9d73-236">delivery address</span></span>       | <span data-ttu-id="b9d73-237">%linedeliveryaddress%</span><span class="sxs-lookup"><span data-stu-id="b9d73-237">%linedeliveryaddress%</span></span> |
| <span data-ttu-id="b9d73-238">Verkoopeenheid van regel</span><span class="sxs-lookup"><span data-stu-id="b9d73-238">Sales unit of the line</span></span> | <span data-ttu-id="b9d73-239">%lineunit%</span><span class="sxs-lookup"><span data-stu-id="b9d73-239">%lineunit%</span></span> |

## <a name="additional-resources"></a><span data-ttu-id="b9d73-240">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="b9d73-240">Additional resources</span></span>

[<span data-ttu-id="b9d73-241">Omgevingsoverzicht Dynamics 365 Commerce-preview</span><span class="sxs-lookup"><span data-stu-id="b9d73-241">Dynamics 365 Commerce preview environment overview</span></span>](cpe-overview.md)

[<span data-ttu-id="b9d73-242">Een previewomgeving voor Dynamics 365 Commerce inrichten</span><span class="sxs-lookup"><span data-stu-id="b9d73-242">Provision a Dynamics 365 Commerce preview environment</span></span>](provisioning-guide.md)

[<span data-ttu-id="b9d73-243">Een Dynamics 365 Commerce-preview-omgeving configureren</span><span class="sxs-lookup"><span data-stu-id="b9d73-243">Configure a Dynamics 365 Commerce preview environment</span></span>](cpe-post-provisioning.md)

[<span data-ttu-id="b9d73-244">Veelgestelde vragen over Dynamics 365 Commerce-preview-omgeving</span><span class="sxs-lookup"><span data-stu-id="b9d73-244">Dynamics 365 Commerce preview environment FAQ</span></span>](cpe-faq.md)

[<span data-ttu-id="b9d73-245">Microsoft Lifecycle Services (LCS)</span><span class="sxs-lookup"><span data-stu-id="b9d73-245">Microsoft Lifecycle Services (LCS)</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[<span data-ttu-id="b9d73-246">Retail Cloud Scale Unit (RCSU)</span><span class="sxs-lookup"><span data-stu-id="b9d73-246">Retail Cloud Scale Unit (RCSU)</span></span>](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[<span data-ttu-id="b9d73-247">Microsoft Azure-portal</span><span class="sxs-lookup"><span data-stu-id="b9d73-247">Microsoft Azure portal</span></span>](https://azure.microsoft.com/features/azure-portal)

[<span data-ttu-id="b9d73-248">Dynamics 365 Commerce-website</span><span class="sxs-lookup"><span data-stu-id="b9d73-248">Dynamics 365 Commerce website</span></span>](https://aka.ms/Dynamics365CommerceWebsite)
