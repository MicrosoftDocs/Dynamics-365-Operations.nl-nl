---
title: Een profiel voor e-mailmeldingen instellen
description: In dit onderwerp wordt beschreven hoe u een profiel voor e-mailmeldingen maakt in Microsoft Dynamics 365 Commerce.
author: bicyclingfool
ms.date: 03/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: stuharg
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 7504b2b36f6869f90de196bf32c09e7bdd51e7b5
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/31/2021
ms.locfileid: "5792652"
---
# <a name="set-up-an-email-notification-profile"></a><span data-ttu-id="9c3b4-103">Een profiel voor e-mailmeldingen instellen</span><span class="sxs-lookup"><span data-stu-id="9c3b4-103">Set up an email notification profile</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="9c3b4-104">In dit onderwerp wordt beschreven hoe u een profiel voor e-mailmeldingen maakt in Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="9c3b4-104">This topic describes how to create an email notification profile in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="9c3b4-105">Wanneer u kanalen maakt, kunt u een e-mailmeldingsprofiel instellen.</span><span class="sxs-lookup"><span data-stu-id="9c3b4-105">When you create channels, you can set up an email notification profile.</span></span> <span data-ttu-id="9c3b4-106">Op die manier kunnen e-mails worden verzonden naar klanten voor verschillende transactiegebeurtenissen, zoals het maken van orders, de verzendingsstatus van de order en het mislukken van een betaling.</span><span class="sxs-lookup"><span data-stu-id="9c3b4-106">In that way, emails can be sent to customers for various transactional events, such as order creation, order shipping status, and payment failure.</span></span>

<span data-ttu-id="9c3b4-107">Zie [E-mail configureren en verzenden](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json) voor meer informatie over het configureren van e-mail.</span><span class="sxs-lookup"><span data-stu-id="9c3b4-107">For additional email configuration information, see [Configure and send email](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json).</span></span>

## <a name="create-an-email-notification-profile"></a><span data-ttu-id="9c3b4-108">Een profiel voor e-mailmeldingen maken</span><span class="sxs-lookup"><span data-stu-id="9c3b4-108">Create an email notification profile</span></span>

<span data-ttu-id="9c3b4-109">Voer de volgende stappen uit om een e-mailmeldingsprofiel te maken.</span><span class="sxs-lookup"><span data-stu-id="9c3b4-109">To create an email notification profile, follow these steps.</span></span>

1. <span data-ttu-id="9c3b4-110">Ga in het navigatievenster naar **Modules \> Detailhandel en Commerce \> Instelling van hoofdkantoor \> E-mailmeldingsprofiel voor Commerce**.</span><span class="sxs-lookup"><span data-stu-id="9c3b4-110">In the navigation pane, go to **Modules \> Retail and commerce \> Headquarters setup \> Commerce email notification profile**.</span></span>
1. <span data-ttu-id="9c3b4-111">Klik in het actievenster op **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="9c3b4-111">On the action pane, click **New**.</span></span>
1. <span data-ttu-id="9c3b4-112">Voer in het veld **E-mailmeldingsprofiel** een naam in om het profiel te identificeren.</span><span class="sxs-lookup"><span data-stu-id="9c3b4-112">In the **Email notification profile** field, enter a name to identify the profile.</span></span>
1. <span data-ttu-id="9c3b4-113">Voer in het veld **Beschrijving** een relevante beschrijving in.</span><span class="sxs-lookup"><span data-stu-id="9c3b4-113">In the **Description** field, enter a relevant description.</span></span>
1. <span data-ttu-id="9c3b4-114">Stel de schakeloptie **Actief** in op **Ja**.</span><span class="sxs-lookup"><span data-stu-id="9c3b4-114">Set the **Active** switch to **Yes**.</span></span>

### <a name="create-an-email-template"></a><span data-ttu-id="9c3b4-115">Een e-mailsjabloon maken</span><span class="sxs-lookup"><span data-stu-id="9c3b4-115">Create an email template</span></span>

<span data-ttu-id="9c3b4-116">Voordat een e-mailmeldingstype kan worden ingeschakeld, moet u een e-mailsjabloon van de organisatie maken in Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="9c3b4-116">Before an email notification type can be enabled, you must create an organization email template in Commerce headquarters.</span></span> <span data-ttu-id="9c3b4-117">Met deze sjabloon definieert u het e-mailbericht, de afzender, de standaardtaal en de hoofdtekst van de e-mail voor elke taal die u wilt ondersteunen.</span><span class="sxs-lookup"><span data-stu-id="9c3b4-117">This template defines the email subject, sender, default language, and email body for each language that you want to support.</span></span>

<span data-ttu-id="9c3b4-118">Volg deze stappen om een e-mailsjabloon te maken.</span><span class="sxs-lookup"><span data-stu-id="9c3b4-118">To create an email template, follow these steps.</span></span>

1. <span data-ttu-id="9c3b4-119">Ga in het navigatievenster naar **Modules \> Retail en Commerce \> Instelling van hoofdkantoor \> Parameters \> E-mailsjablonen voor organisatie**.</span><span class="sxs-lookup"><span data-stu-id="9c3b4-119">In the navigation pane, go to **Modules \> Retail and commerce \> Headquarters setup \> Parameters \> Organization email templates**.</span></span>
1. <span data-ttu-id="9c3b4-120">Selecteer **Nieuw** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="9c3b4-120">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="9c3b4-121">Voer in het veld **E-mail-id** een id in om deze sjabloon te helpen identificeren.</span><span class="sxs-lookup"><span data-stu-id="9c3b4-121">In the **Email ID** field, enter an ID to help identify this template.</span></span>
1. <span data-ttu-id="9c3b4-122">Voer in het veld **Naam afzender** de naam van de afzender in.</span><span class="sxs-lookup"><span data-stu-id="9c3b4-122">In the **Sends name** field, enter the senders name.</span></span>
1. <span data-ttu-id="9c3b4-123">Voer in het veld **Beschrijving van e-mail** een betekenisvolle beschrijving in.</span><span class="sxs-lookup"><span data-stu-id="9c3b4-123">In the **Email Description**, enter a meaningful description.</span></span>
1. <span data-ttu-id="9c3b4-124">Voer in het veld **E-mailadres afzender** het e-mailadres van de afzender in.</span><span class="sxs-lookup"><span data-stu-id="9c3b4-124">In the **Sender email**, enter the senders email address.</span></span>
1. <span data-ttu-id="9c3b4-125">Selecteer in de sectie **Algemeen** een standaardtaal voor de e-mailsjabloon.</span><span class="sxs-lookup"><span data-stu-id="9c3b4-125">In the **General** section, select a default language for the email template.</span></span> <span data-ttu-id="9c3b4-126">De standaardtaal wordt gebruikt als er geen gelokaliseerde sjabloon voor de opgegeven taal bestaat.</span><span class="sxs-lookup"><span data-stu-id="9c3b4-126">The default language will be used when no localized template exists for the specified language.</span></span>
1. <span data-ttu-id="9c3b4-127">Vouw de sectie **Inhoud van e-malbericht** uit en selecteer **Nieuw** om de sjablooninhoud te maken.</span><span class="sxs-lookup"><span data-stu-id="9c3b4-127">Expand the **Email message content** section and select **New** to create the template content.</span></span> <span data-ttu-id="9c3b4-128">Selecteer voor elk inhoudsitem de taal en geef de onderwerpregel van het e-mailbericht op.</span><span class="sxs-lookup"><span data-stu-id="9c3b4-128">For each content item, select the language and provide the email subject line.</span></span> <span data-ttu-id="9c3b4-129">Als het e-mailbericht tekst bevat, controleert u of het vak **Heeft hoofdtekst** is ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="9c3b4-129">If the email will have a body, ensure that the **Has body** box is checked.</span></span>
1. <span data-ttu-id="9c3b4-130">Selecteer **E-mailbericht** in het actievenster om een sjabloon voor e-mailteksten op te geven.</span><span class="sxs-lookup"><span data-stu-id="9c3b4-130">On the action pane, select **Email message** to provide an email body template.</span></span>

<span data-ttu-id="9c3b4-131">De volgende afbeelding toont enkele voorbeelden van e-mailsjablooninstellingen.</span><span class="sxs-lookup"><span data-stu-id="9c3b4-131">The following image shows some example email template settings.</span></span>

![Instellingen van e-mailsjabloon](media/email-template.png)

### <a name="create-an-email-event"></a><span data-ttu-id="9c3b4-133">Een e-mailgebeurtenis maken</span><span class="sxs-lookup"><span data-stu-id="9c3b4-133">Create an email event</span></span>

<span data-ttu-id="9c3b4-134">Volg deze stappen om een e-mailgebeurtenis te maken.</span><span class="sxs-lookup"><span data-stu-id="9c3b4-134">To create an email event, follow these steps.</span></span>

1. <span data-ttu-id="9c3b4-135">Ga in het navigatievenster naar **Modules \> Detailhandel en Commerce \> Instelling van hoofdkantoor \> E-mailmeldingsprofiel voor Commerce**.</span><span class="sxs-lookup"><span data-stu-id="9c3b4-135">In the navigation pane, go to **Modules \> Retail and commerce \> Headquarters setup \> Commerce email notification profile**.</span></span>
1. <span data-ttu-id="9c3b4-136">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="9c3b4-136">In the list, find and select the desired record.</span></span> 
1. <span data-ttu-id="9c3b4-137">Selecteer de e-mailsjabloon in de vervolgkeuzelijst **E-mail-id**.</span><span class="sxs-lookup"><span data-stu-id="9c3b4-137">Select the email template from the **Email ID** drop-down list.</span></span>
1. <span data-ttu-id="9c3b4-138">Selecteer het toepasselijke **E-mailmeldingstype** in de vervolgkeuzelijst.</span><span class="sxs-lookup"><span data-stu-id="9c3b4-138">Select the appropriate **Email notification type** from the drop-down list.</span></span>
1. <span data-ttu-id="9c3b4-139">Schakel het selectievakje **Actief** in.</span><span class="sxs-lookup"><span data-stu-id="9c3b4-139">Select the **Active** check box.</span></span>
1. <span data-ttu-id="9c3b4-140">Selecteer **Opslaan** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="9c3b4-140">On the action pane, select **Save**.</span></span>

<span data-ttu-id="9c3b4-141">De volgende afbeelding toont enkele voorbeelden van instellingen voor meldingen van meldingen.</span><span class="sxs-lookup"><span data-stu-id="9c3b4-141">The following image shows some example event notification settings.</span></span>

![Instellingen voor melding van gebeurtenissen](media/email-notification-profile.png)

### <a name="next-steps"></a><span data-ttu-id="9c3b4-143">Volgende stappen</span><span class="sxs-lookup"><span data-stu-id="9c3b4-143">Next steps</span></span>

<span data-ttu-id="9c3b4-144">Voordat u e-mailberichten kunt verzenden, moet u de service voor uitgaande e-mail configureren en een batchtaak instellen.</span><span class="sxs-lookup"><span data-stu-id="9c3b4-144">Before you can send mails, you must configure your outgoing mail service and set up a batch job.</span></span> <span data-ttu-id="9c3b4-145">Zie [E-mail configureren en verzenden](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="9c3b4-145">For more information, see [Configure and send email](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json).</span></span>


## <a name="additional-resources"></a><span data-ttu-id="9c3b4-146">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="9c3b4-146">Additional resources</span></span>

[<span data-ttu-id="9c3b4-147">E-mail configureren en verzenden</span><span class="sxs-lookup"><span data-stu-id="9c3b4-147">Configure and send email</span></span>](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="9c3b4-148">Overzicht van kanalen</span><span class="sxs-lookup"><span data-stu-id="9c3b4-148">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="9c3b4-149">Vereisten voor het instellen van kanalen</span><span class="sxs-lookup"><span data-stu-id="9c3b4-149">Channel setup prerequisites</span></span>](channels-prerequisites.md)

[<span data-ttu-id="9c3b4-150">Overzicht van Organisaties en organisatiehiërarchieën</span><span class="sxs-lookup"><span data-stu-id="9c3b4-150">Organizations and organizational hierarchies overview</span></span>](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
