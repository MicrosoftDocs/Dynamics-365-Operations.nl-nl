---
title: E-mailinstellingen configureren in Microsoft Dynamics 365 Talent - Attract
description: In dit onderwerp wordt uitgelegd hoe u instellingen configureert voor e-mail die door Microsoft Dynamcis 365 Talent - Attract wordt verzonden.
author: andreabichsel
manager: AnnBe
ms.date: 06/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.search.industry: ''
ms.author: anbichse
ms.search.validFrom: 2019-06-04
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: c891a36f01d36774bd921475fa5995d207cd2d51
ms.sourcegitcommit: 434dd21450bddcd891aba0555b9853d9ba0afb6f
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/23/2019
ms.locfileid: "2008657"
---
# <a name="configure-email-settings"></a><span data-ttu-id="f7379-103">E-mailinstellingen configureren</span><span class="sxs-lookup"><span data-stu-id="f7379-103">Configure email settings</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="f7379-104">Uw merk wekt vertrouwen en helpt u al een vertrouwensrelatie tot stand te brengen met kandidaten voordat deze solliciteren voor uw functies.</span><span class="sxs-lookup"><span data-stu-id="f7379-104">Your brand establishes trust and helps you build a relationship with candidates before they even apply for your positions.</span></span> <span data-ttu-id="f7379-105">Een positieve merkperceptie trekt de beste talenten aan en vergroot de loyaliteit van bestaande werknemers.</span><span class="sxs-lookup"><span data-stu-id="f7379-105">Positive brand perception attracts top talent and increases the loyalty of existing employees.</span></span> <span data-ttu-id="f7379-106">Met Microsoft Dynamics 365 Talent: Attract kunt u e-mailberichten zo configureren dat deze het merk van uw bedrijf weerspiegelen.</span><span class="sxs-lookup"><span data-stu-id="f7379-106">Microsoft Dynamics 365 Talent: Attract lets you configure emails so that they reflect your company's brand.</span></span> <span data-ttu-id="f7379-107">Zo kunt u functiekandidaten een consistente ervaring bieden tijdens het sollicitatieproces.</span><span class="sxs-lookup"><span data-stu-id="f7379-107">Therefore, you can provide a consistent experience to job candidates as they progress through the application process.</span></span>

<span data-ttu-id="f7379-108">Met Attract kunt u de volgende acties uitvoeren:</span><span class="sxs-lookup"><span data-stu-id="f7379-108">Attract lets you perform these actions:</span></span>

- <span data-ttu-id="f7379-109">E-mailinstellingen configureren zodat de Microsoft Exchange-e-mailserviceaccount van het bedrijf wordt gebruikt.</span><span class="sxs-lookup"><span data-stu-id="f7379-109">Configure email settings so that your company's Microsoft Exchange email service account is used.</span></span> <span data-ttu-id="f7379-110">Op deze manier weten kandidaten dat de e-mails afkomstig zijn van uw bedrijf.</span><span class="sxs-lookup"><span data-stu-id="f7379-110">In this way, candidates know that the emails are coming from your company.</span></span> <span data-ttu-id="f7379-111">U kunt de instellingen bijvoorbeeld zo configureren dat kandidaten e-mails ontvangen van `recruiting@contoso.com` in plaats van `contoso@microsoft.com`.</span><span class="sxs-lookup"><span data-stu-id="f7379-111">For example, you can configure your settings so that candidates receive emails from `recruiting@contoso.com` instead of `contoso@microsoft.com`.</span></span>
- <span data-ttu-id="f7379-112">Zorg voor een consistent merkbeeld voor alle e-mailcommunicatie door een globale kop- en voettekst voor alle e-mailsjablonen in te stellen.</span><span class="sxs-lookup"><span data-stu-id="f7379-112">Create consistent branding for all your email communications by setting a global header and footer for email templates.</span></span> 

> [!NOTE]
> <span data-ttu-id="f7379-113">Als u Attract zo wilt configureren dat het e-mailserviceaccount van uw bedrijf wordt gebruikt om e-mail te verzenden, hebt u Uitgebreide invoegtoepassing voor aanstellingen nodig.</span><span class="sxs-lookup"><span data-stu-id="f7379-113">To configure Attract so that it uses your company's email service account to send email, you need the Comprehensive hiring add-on.</span></span>

## <a name="connect-an-email-service-account"></a><span data-ttu-id="f7379-114">Een e-mailserviceaccount verbinden</span><span class="sxs-lookup"><span data-stu-id="f7379-114">Connect an email service account</span></span>

<span data-ttu-id="f7379-115">Door de e-mailserviceaccount van uw bedrijf te verbinden, kunt u een e-mailervaring met een huisstijl maken voor uw sollicitanten.</span><span class="sxs-lookup"><span data-stu-id="f7379-115">By connecting your company's email service account, you can create a branded email experience for your job candidates.</span></span> <span data-ttu-id="f7379-116">Als u de bedrijfsaccount niet verbindt, wordt de standaard e-mailserviceaccount van Microsoft gebruikt.</span><span class="sxs-lookup"><span data-stu-id="f7379-116">If you don't connect your company account, Attract uses the default Microsoft-branded email service account.</span></span>

1. <span data-ttu-id="f7379-117">Selecteer **Instellingen** (het tandwielsymbool) in de rechterbovenhoek en selecteer vervolgens **Beheercentrum**.</span><span class="sxs-lookup"><span data-stu-id="f7379-117">Select **Settings** (the gear symbol in the upper-right corner), and then select **Admin center**.</span></span>
2. <span data-ttu-id="f7379-118">Selecteer op het tabblad **E-mailinstellingen** onder **E-mailserviceaccounts** de optie **Een bedrijfsacccount verbinden**.</span><span class="sxs-lookup"><span data-stu-id="f7379-118">On the **Email settings** tab, under **Email service accounts**, select **Connect a company account**.</span></span>

    ![De e-mailserviceaccount van het bedrijf verbinden in Attract](./media/attract-admin-email-service-accounts.png)

    <span data-ttu-id="f7379-120">Zie [Gedeelde postvakken in Exchange Online](https://docs.microsoft.com/exchange/collaboration-exo/shared-mailboxes) voor meer informatie over het maken van een gedeelde e-mailaccount.</span><span class="sxs-lookup"><span data-stu-id="f7379-120">For more information about how to create a shared email account, see [Shared mailboxes in Exchange Online](https://docs.microsoft.com/exchange/collaboration-exo/shared-mailboxes).</span></span>

3. <span data-ttu-id="f7379-121">Meld u aan met uw bedrijfsreferenties aan in het aanmeldingsvenster van Microsoft.</span><span class="sxs-lookup"><span data-stu-id="f7379-121">In the Microsoft sign-in window, sign in by using your corporate credentials.</span></span>
4. <span data-ttu-id="f7379-122">Als u nog geen e-mailserviceaccount hebt ingesteld of als u een nieuwe wilt toevoegen, selecteert **Nieuwe serviceaccount toevoegen** en geeft u vervolgens uw e-mailgegevens op.</span><span class="sxs-lookup"><span data-stu-id="f7379-122">If you haven't yet set up an email service account, or if you want to add a new one, select **Add new service account**, and then enter your email information.</span></span> <span data-ttu-id="f7379-123">Als u de e-mailserviceaccount die u wilt gebruiken al hebt ingesteld, selecteert u deze.</span><span class="sxs-lookup"><span data-stu-id="f7379-123">If you've already set up the email service account that you want to use, select it.</span></span>

<span data-ttu-id="f7379-124">Wanneer uw e-mailserviceaccount is geconfigureerd, wordt deze weergegeven onder **E-mailserviceaccounts**.</span><span class="sxs-lookup"><span data-stu-id="f7379-124">When your email service account is successfully configured, you will see it listed under **Email service accounts**.</span></span>

## <a name="disconnect-an-email-service-account"></a><span data-ttu-id="f7379-125">De verbinding met een e-mailserviceaccount verbreken</span><span class="sxs-lookup"><span data-stu-id="f7379-125">Disconnect an email service account</span></span>

<span data-ttu-id="f7379-126">Als u het domein van uw bedrijf niet meer wilt gebruiken in e-mailcommunicatie via Attract, kunt u de verbinding met een e-mailserviceaccount verbreken.</span><span class="sxs-lookup"><span data-stu-id="f7379-126">If you want to stop using your company's domain in email communications through Attract, you can disconnect an email service account.</span></span>

1. <span data-ttu-id="f7379-127">Selecteer **Instellingen** (het tandwielsymbool) in de rechterbovenhoek en selecteer vervolgens **Beheercentrum**.</span><span class="sxs-lookup"><span data-stu-id="f7379-127">Select **Settings** (the gear symbol in the upper-right corner), and then select **Admin center**.</span></span>
2. <span data-ttu-id="f7379-128">Selecteer op het tabblad **E-mailinstellingen** onder **E-mailserviceaccounts** de knop **Meer** (drie verticale punten) naast de e-mailserviceaccount waarmee u de verbinding wilt verbreken.</span><span class="sxs-lookup"><span data-stu-id="f7379-128">On the **Email settings** tab, under **Email service accounts**, select the **More** button (three vertical dots) next to the email service account that you want to disconnect.</span></span>
3. <span data-ttu-id="f7379-129">Selecteer **Verbinding met e-mailaccount verbreken**.</span><span class="sxs-lookup"><span data-stu-id="f7379-129">Select **Disconnect email account**.</span></span>

    ![De verbinding met de e-mailserviceaccount van het bedrijf verbreken](./media/attract-admin-disconnect-email-account.png)

4. <span data-ttu-id="f7379-131">Selecteer **Verbinding verbreken** wanneer u wordt gevraagd de bewerking te bevestigen.</span><span class="sxs-lookup"><span data-stu-id="f7379-131">When you're prompted to confirm the operation, select **Disconnect**.</span></span>

    ![Het verbreken van de verbinding met de e-mailserviceaccount van het bedrijf bevestigen](./media/attract-admin-email-confirm-disconnect.png)

<span data-ttu-id="f7379-133">Als u geen andere e-mailserviceaccount verbindt, wordt voor e-mails die worden verzonden vanuit Attract de standaard-e-mailserviceaccount van Microsoft gebruikt.</span><span class="sxs-lookup"><span data-stu-id="f7379-133">If you don't connect a different email service account, emails that are sent from Attract will use the default Microsoft-branded email service account.</span></span>

## <a name="configure-email-template-settings"></a><span data-ttu-id="f7379-134">E-mailsjablooninstellingen configureren</span><span class="sxs-lookup"><span data-stu-id="f7379-134">Configure email template settings</span></span>

<span data-ttu-id="f7379-135">U kunt een afbeelding van het logo van uw bedrijf en andere informatie uploaden als huisstijlkoptekst voor uw e-mailberichten.</span><span class="sxs-lookup"><span data-stu-id="f7379-135">You can upload an image of your company's logo and other information as a branded header for your emails.</span></span> <span data-ttu-id="f7379-136">U kunt ook koppelingen naar uw privacybeleid en gebruiksvoorwaarden in e-mailvoetteksten opgeven.</span><span class="sxs-lookup"><span data-stu-id="f7379-136">You can also provide links to your privacy policy and terms of use in email footers.</span></span>

> [!NOTE]
> <span data-ttu-id="f7379-137">U moet voldoen aan alle toepasselijke wetgeving van uw land of regio en de wetgeving die van toepassing is in het land of de regio van de e-mailontvanger.</span><span class="sxs-lookup"><span data-stu-id="f7379-137">You must comply with all applicable laws of your country or region, and also the country or region that governs the email recipient.</span></span> <span data-ttu-id="f7379-138">Deze wetten omvatten voorschriften voor ongewenste e-mail.</span><span class="sxs-lookup"><span data-stu-id="f7379-138">These laws include anti-spam regulations.</span></span>

1. <span data-ttu-id="f7379-139">Selecteer **Instellingen** (het tandwielsymbool) in de rechterbovenhoek en selecteer vervolgens **Beheercentrum**.</span><span class="sxs-lookup"><span data-stu-id="f7379-139">Select **Settings** (the gear symbol in the upper-right corner), and then select **Admin center**.</span></span>
2. <span data-ttu-id="f7379-140">Sleep op het tabblad **E-mailinstellingen** onder **Instellingen van e-mailsjabloon** de afbeelding die u als uw e-mailkoptekst wilt gebruiken naar het afbeeldingsvak of klik in het afbeeldingsvak om het bestand te zoeken.</span><span class="sxs-lookup"><span data-stu-id="f7379-140">On the **Email settings** tab, under **Email template settings**, drag the image that you want to use as your email header into the image box, or click in the image box to browse for the file.</span></span> <span data-ttu-id="f7379-141">Als u een bestaande afbeelding wilt vervangen, moet u eerst **Verwijderen** ernaast selecteren.</span><span class="sxs-lookup"><span data-stu-id="f7379-141">To replace an existing image, you must first select **Remove** next to it.</span></span> <span data-ttu-id="f7379-142">De afbeelding moet een JPEG-, JPG-, PNG- of SVG-bestand zijn.</span><span class="sxs-lookup"><span data-stu-id="f7379-142">The image must be a JPEG, JPG, PNG, or SVG file.</span></span> <span data-ttu-id="f7379-143">De aanbevolen grootte voor afbeeldingen ligt tussen 25 en 800 pixels breed en 25 en 150 pixels hoog.</span><span class="sxs-lookup"><span data-stu-id="f7379-143">The recommended size for images is between 25 and 800 pixels wide, and between 25 and 150 pixels high.</span></span> <span data-ttu-id="f7379-144">De maximale bestandsgrootte voor de koptekst is 1 MB.</span><span class="sxs-lookup"><span data-stu-id="f7379-144">The maximum file size for the header is 1 megabyte (MB).</span></span>

    ![Een afbeelding toevoegen voor de e-mailkoptekst van uw bedrijf](./media/attract-admin-email-header.png)

3. <span data-ttu-id="f7379-146">Geef onder **Uw privacybeleid voor communicatie** een koppeling naar het privacybeleid van uw bedrijf op.</span><span class="sxs-lookup"><span data-stu-id="f7379-146">Under **Your Privacy policy for communications**, provide a link to your company's privacy policy.</span></span> <span data-ttu-id="f7379-147">Geef onder **Uw algemene voorwaarden voor communicatie** een koppeling naar de gebruiksvoorwaarden van uw bedrijf op.</span><span class="sxs-lookup"><span data-stu-id="f7379-147">Under **Your Terms and conditions for communication**, provide a link to your company's terms of use.</span></span>

    ![Koppelingen naar het privacybeleid en de gebruiksvoorwaarden van uw bedrijf toevoegen voor de e-mailvoettekst](./media/attract-admin-email-footer.png)

4. <span data-ttu-id="f7379-149">Selecteer **Opslaan** om de e-mailsjablooninstellingen op te slaan.</span><span class="sxs-lookup"><span data-stu-id="f7379-149">Select **Save** to save your email template settings.</span></span>
