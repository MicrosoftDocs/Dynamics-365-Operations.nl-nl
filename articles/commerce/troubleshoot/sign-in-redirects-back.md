---
title: Aanmeldingskoppeling leidt terug naar een e-commercesite
description: Dit onderwerp bevat richtlijnen voor probleemoplossing die u kunnen helpen als een aanmeldingskoppeling terugleidt naar de e-commercesite in plaats van naar de aanmeldingspagina.
author: Reza-Assadi
manager: AnnBe
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 36f10c9f68570a6c67da6b4b6e4155f4634f633a
ms.sourcegitcommit: 6c108be3378b365e6ec596a1a8666d59b758db25
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/12/2021
ms.locfileid: "5585259"
---
# <a name="sign-in-link-redirects-back-to-an-e-commerce-site"></a><span data-ttu-id="846ae-103">Aanmeldingskoppeling leidt terug naar een e-commercesite</span><span class="sxs-lookup"><span data-stu-id="846ae-103">Sign-in link redirects back to an e-commerce site</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="846ae-104">Dit onderwerp bevat richtlijnen voor probleemoplossing die u kunnen helpen als een aanmeldingskoppeling terugleidt naar de e-commercesite in plaats van naar de aanmeldingspagina.</span><span class="sxs-lookup"><span data-stu-id="846ae-104">This topic provides troubleshooting guidance that can help when a sign-in link redirects back to the e-commerce site instead of going to the sign-in page.</span></span>

## <a name="description"></a><span data-ttu-id="846ae-105">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="846ae-105">Description</span></span>

<span data-ttu-id="846ae-106">Nadat u een nieuwe Microsoft Azure Active Directory B2C-tenant (Azure AD B2C) hebt geconfigureerd in Commerce Site Builder, worden gebruikers die de koppeling **Aanmelden** selecteren teruggeleid naar de hoofdpagina van de e-commercesite zonder naar de aanmeldingspagina te gaan.</span><span class="sxs-lookup"><span data-stu-id="846ae-106">After you configure a new Microsoft Azure Active Directory B2C (Azure AD B2C) tenant in Commerce site builder, users who select the **Sign in** link are redirected back to the main e-commerce landing page without going to the sign-in page.</span></span>

## <a name="resolution"></a><span data-ttu-id="846ae-107">Oplossing</span><span class="sxs-lookup"><span data-stu-id="846ae-107">Resolution</span></span>

### <a name="confirm-that-the-reply-url-is-correctly-configured-in-the-azure-ad-b2c-application"></a><span data-ttu-id="846ae-108">Bevestigen dat de antwoord-URL correct is geconfigureerd in de Azure AD B2C-toepassing</span><span class="sxs-lookup"><span data-stu-id="846ae-108">Confirm that the reply URL is correctly configured in the Azure AD B2C application</span></span>

<span data-ttu-id="846ae-109">Voer deze stappen uit om te bevestigen dat de antwoord-URL correct is geconfigureerd in de Azure AD B2C-toepassing.</span><span class="sxs-lookup"><span data-stu-id="846ae-109">To confirm that the reply URL is correctly configured in the Azure AD B2C application, follow these steps.</span></span>

1. <span data-ttu-id="846ae-110">Ga naar de [Azure-portal](https://portal.azure.com/).</span><span class="sxs-lookup"><span data-stu-id="846ae-110">Go to the [Azure portal](https://portal.azure.com/).</span></span>
1. <span data-ttu-id="846ae-111">Selecteer de Azure AD B2C-toepassing die u voor toegang tot uw site hebt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="846ae-111">Select the Azure AD B2C application that you created for your site access.</span></span>
1. <span data-ttu-id="846ae-112">Selecteer de toepassing die u hebt gemaakt tijdens het instellen van Azure AD B2C.</span><span class="sxs-lookup"><span data-stu-id="846ae-112">Select the application that you created during the Azure AD B2C setup.</span></span>
1. <span data-ttu-id="846ae-113">Zorg er onder **Antwoord-URL** voor dat de lijst vermeldingen bevat voor zowel de URL van het sitedomein als de door e-commerce gegenereerde URL, zoals in het voorbeeld in de volgende afbeelding is weergegeven.</span><span class="sxs-lookup"><span data-stu-id="846ae-113">Under **Reply URL**, make sure that the list includes entries for both the site domain URL and the e-commerce-generated URL, as shown in the example in the following illustration.</span></span>

    ![Vermeldingen van antwoord-URL in Azure AD B2C](media/aad-b2c-reply-url.jpg)

> [!NOTE]
> <span data-ttu-id="846ae-115">Zowel de URL van het sitedomein als de URL die door e-commerce is gegenereerd, moeten een geldige URL-indeling hebben die geen voorloop- of volgslashes bevat.</span><span class="sxs-lookup"><span data-stu-id="846ae-115">Both the site domain URL and the e-commerce-generated URL must be in a valid URL format that doesn't include leading or trailing slashes.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="846ae-116">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="846ae-116">Additional resources</span></span>

[<span data-ttu-id="846ae-117">Een webtoepassing registreren in Azure Active Directory B2C</span><span class="sxs-lookup"><span data-stu-id="846ae-117">Register a web application in Azure Active Directory B2C</span></span>](https://docs.microsoft.com/azure/active-directory-b2c/tutorial-register-applications?tabs=app-reg-ga#register-a-web-application)

[<span data-ttu-id="846ae-118">Een B2C-tenant instellen in Commerce</span><span class="sxs-lookup"><span data-stu-id="846ae-118">Set up a B2C tenant in Commerce</span></span>](../set-up-b2c-tenant.md)
