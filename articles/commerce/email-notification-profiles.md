---
title: Een profiel voor e-mailmeldingen instellen
description: In dit onderwerp wordt beschreven hoe u een profiel voor e-mailmeldingen maakt in Microsoft Dynamics 365 Commerce.
author: samjarawan
manager: annbe
ms.date: 01/27/2020
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
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 9e5d90eaf1815bbe54b0bea40d92a0a993a23b75
ms.sourcegitcommit: 141e0239b6310ab4a6a775bc0997120c31634f79
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/10/2020
ms.locfileid: "3113800"
---
# <a name="set-up-an-email-notification-profile"></a><span data-ttu-id="234d1-103">Een profiel voor e-mailmeldingen instellen</span><span class="sxs-lookup"><span data-stu-id="234d1-103">Set up an email notification profile</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="234d1-104">In dit onderwerp wordt beschreven hoe u een profiel voor e-mailmeldingen maakt in Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="234d1-104">This topic describes how to create an email notification profile in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="234d1-105">Overzicht</span><span class="sxs-lookup"><span data-stu-id="234d1-105">Overview</span></span>

<span data-ttu-id="234d1-106">Voordat u kanalen gaat maken, moet u een profiel instellen om ervoor te zorgen dat e-mailmeldingen kunnen worden verzonden voor verschillende gebeurtenissen, zoals het maken van orders, het verzenden van orders en het mislukken van de betaling.</span><span class="sxs-lookup"><span data-stu-id="234d1-106">Before creating channels, you'll want to set up a profile to ensure that email notifications can be sent out for various events, such as order creation, order shipping status, and payment failure.</span></span>

<span data-ttu-id="234d1-107">Zie [E-mail configureren en verzenden](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json) voor meer informatie over het configureren van e-mail.</span><span class="sxs-lookup"><span data-stu-id="234d1-107">For additional email configuration information, see [Configure and send email](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json).</span></span>

## <a name="create-an-email-notification-profile"></a><span data-ttu-id="234d1-108">Een profiel voor e-mailmeldingen maken</span><span class="sxs-lookup"><span data-stu-id="234d1-108">Create an email notification profile</span></span>

<span data-ttu-id="234d1-109">Voer de volgende stappen uit om een e-mailmeldingsprofiel te maken.</span><span class="sxs-lookup"><span data-stu-id="234d1-109">To create an email notification profile, follow these steps.</span></span>

1. <span data-ttu-id="234d1-110">Ga in het navigatievenster naar **Modules \> Detailhandel en Commerce \> Instelling van hoofdkantoor \> E-mailmeldingsprofiel voor Commerce**.</span><span class="sxs-lookup"><span data-stu-id="234d1-110">In the navigation pane, go to **Modules \> Retail and commerce \> Headquarters setup \> Commerce email notification profile**.</span></span>
1. <span data-ttu-id="234d1-111">Klik in het actievenster op **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="234d1-111">On the action pane, click **New**.</span></span>
1. <span data-ttu-id="234d1-112">Voer in het veld **E-mailmeldingsprofiel** een naam in om het profiel te identificeren.</span><span class="sxs-lookup"><span data-stu-id="234d1-112">In the **Email notification profile** field, enter a name to identify the profile.</span></span>
1. <span data-ttu-id="234d1-113">Voer in het veld **Beschrijving** een relevante beschrijving in.</span><span class="sxs-lookup"><span data-stu-id="234d1-113">In the **Description** field, enter a relevant description.</span></span>
1. <span data-ttu-id="234d1-114">Stel de schakeloptie **Actief** in op **Ja**.</span><span class="sxs-lookup"><span data-stu-id="234d1-114">Set the **Active** switch to **Yes**.</span></span>

### <a name="create-an-email-template"></a><span data-ttu-id="234d1-115">Een e-mailsjabloon maken</span><span class="sxs-lookup"><span data-stu-id="234d1-115">Create an email template</span></span>

<span data-ttu-id="234d1-116">Voordat een e-mailmelding kan worden gemaakt, moet u een e-mailsjabloon voor de organisatie maken die de e-mailgegevens van de afzenders en de e-mailsjabloon bevat.</span><span class="sxs-lookup"><span data-stu-id="234d1-116">Before an email notification can be created, you must create an organization email template which contains the senders email information and the email template.</span></span>

<span data-ttu-id="234d1-117">Volg deze stappen om een e-mailsjabloon te maken.</span><span class="sxs-lookup"><span data-stu-id="234d1-117">To create an email template, follow these steps.</span></span>

1. <span data-ttu-id="234d1-118">Ga in het navigatievenster naar **Modules \> Retail en Commerce \> Instelling van hoofdkantoor \> Parameters \> E-mailsjablonen voor organisatie**.</span><span class="sxs-lookup"><span data-stu-id="234d1-118">In the navigation pane, go to **Modules \> Retail and commerce \> Headquarters setup \> Parameters \> Organization email templates**.</span></span>
1. <span data-ttu-id="234d1-119">Selecteer **Nieuw** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="234d1-119">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="234d1-120">Voer in het veld **E-mail-id** een id in om deze sjabloon te helpen identificeren.</span><span class="sxs-lookup"><span data-stu-id="234d1-120">In the **Email ID** field, enter an ID to help identify this template.</span></span>
1. <span data-ttu-id="234d1-121">Voer in het veld **Naam afzender** de naam van de afzender in.</span><span class="sxs-lookup"><span data-stu-id="234d1-121">In the **Sends name** field, enter the senders name.</span></span>
1. <span data-ttu-id="234d1-122">Voer in het veld **Beschrijving van e-mail** een betekenisvolle beschrijving in.</span><span class="sxs-lookup"><span data-stu-id="234d1-122">In the **Email Description**, enter a meaningful description.</span></span>
1. <span data-ttu-id="234d1-123">Voer in het veld **E-mailadres afzender** het e-mailadres van de afzender in.</span><span class="sxs-lookup"><span data-stu-id="234d1-123">In the **Sender email**, enter the senders email address.</span></span>
1. <span data-ttu-id="234d1-124">Vul in de sectie **Algemeen** alle optionele informatie in die nodig is (zoals de e-mailprioriteit).</span><span class="sxs-lookup"><span data-stu-id="234d1-124">In the **General** section, fill out any optional information needed (such as the email priority).</span></span>
1. <span data-ttu-id="234d1-125">Vouw de sectie **Inhoud van e-malbericht** uit en selecteer **Nieuw** om de sjablooninhoud te maken.</span><span class="sxs-lookup"><span data-stu-id="234d1-125">Expand the **Email message content** section and select **New** to create the template content.</span></span> <span data-ttu-id="234d1-126">Selecteer voor elk inhoudsitem de taal en geef de onderwerpregel van het e-mailbericht op.</span><span class="sxs-lookup"><span data-stu-id="234d1-126">For each content item, select the language and provide the email subject line.</span></span> <span data-ttu-id="234d1-127">Als het e-mailbericht tekst bevat, controleert u of het vak **Heeft hoofdtekst** is ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="234d1-127">If the email will have a body, ensure that the **Has body** box is checked.</span></span>
1. <span data-ttu-id="234d1-128">Selecteer **E-mailbericht** in het actievenster om een sjabloon voor e-mailteksten op te geven.</span><span class="sxs-lookup"><span data-stu-id="234d1-128">On the action pane, select **Email message** to provide an email body template.</span></span>

<span data-ttu-id="234d1-129">De volgende afbeelding toont enkele voorbeelden van e-mailsjablooninstellingen.</span><span class="sxs-lookup"><span data-stu-id="234d1-129">The following image shows some example email template settings.</span></span>

![Instellingen van e-mailsjabloon](media/email-template.png)

### <a name="create-an-email-event"></a><span data-ttu-id="234d1-131">Een e-mailgebeurtenis maken</span><span class="sxs-lookup"><span data-stu-id="234d1-131">Create an email event</span></span>

<span data-ttu-id="234d1-132">Volg deze stappen om een e-mailgebeurtenis te maken.</span><span class="sxs-lookup"><span data-stu-id="234d1-132">To create an email event, follow these steps.</span></span>

1. <span data-ttu-id="234d1-133">Ga in het navigatievenster naar **Modules \> Detailhandel en Commerce \> Instelling van hoofdkantoor \> E-mailmeldingsprofiel voor Commerce**.</span><span class="sxs-lookup"><span data-stu-id="234d1-133">In the navigation pane, go to **Modules \> Retail and commerce \> Headquarters setup \> Commerce email notification profile**.</span></span>
1. <span data-ttu-id="234d1-134">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="234d1-134">In the list, find and select the desired record.</span></span> 
1. <span data-ttu-id="234d1-135">Selecteer de e-mailsjabloon in de vervolgkeuzelijst **E-mail-id**.</span><span class="sxs-lookup"><span data-stu-id="234d1-135">Select the email template from the **Email ID** drop-down list.</span></span>
1. <span data-ttu-id="234d1-136">Selecteer het toepasselijke **E-mailmeldingstype** in de vervolgkeuzelijst.</span><span class="sxs-lookup"><span data-stu-id="234d1-136">Select the appropriate **Email notification type** from the drop-down list.</span></span>
1. <span data-ttu-id="234d1-137">Schakel het selectievakje **Actief** in.</span><span class="sxs-lookup"><span data-stu-id="234d1-137">Select the **Active** check box.</span></span>
1. <span data-ttu-id="234d1-138">Selecteer **Opslaan** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="234d1-138">On the action pane, select **Save**.</span></span>

<span data-ttu-id="234d1-139">De volgende afbeelding toont enkele voorbeelden van instellingen voor meldingen van meldingen.</span><span class="sxs-lookup"><span data-stu-id="234d1-139">The following image shows some example event notification settings.</span></span>

![Instellingen voor melding van gebeurtenissen](media/email-notification-profile.png)

## <a name="additional-resources"></a><span data-ttu-id="234d1-141">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="234d1-141">Additional resources</span></span>

[<span data-ttu-id="234d1-142">E-mail configureren en verzenden</span><span class="sxs-lookup"><span data-stu-id="234d1-142">Configure and send email</span></span>](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="234d1-143">Overzicht van kanalen</span><span class="sxs-lookup"><span data-stu-id="234d1-143">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="234d1-144">Vereisten voor het instellen van kanalen</span><span class="sxs-lookup"><span data-stu-id="234d1-144">Channel setup prerequisites</span></span>](channels-prerequisites.md)

[<span data-ttu-id="234d1-145">Overzicht van Organisaties en organisatiehiërarchieën</span><span class="sxs-lookup"><span data-stu-id="234d1-145">Organizations and organizational hierarchies overview</span></span>](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)
