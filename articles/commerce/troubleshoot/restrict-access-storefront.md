---
title: Toegang tot een winkel beperken tijdens het testen of ontwikkelen
description: In dit onderwerp wordt uitgelegd hoe u de toegang tot een Microsoft Dynamics 365 Commerce-winkel kunt beperken terwijl interne testen of ontwikkeling plaatsvinden.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
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
ms.openlocfilehash: cdc9b6af55bcba98f5ea7607bb1847f61a707778
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/11/2021
ms.locfileid: "6018333"
---
# <a name="restrict-access-to-a-storefront-during-testing-or-development"></a><span data-ttu-id="d301e-103">Toegang tot een winkel beperken tijdens het testen of ontwikkelen</span><span class="sxs-lookup"><span data-stu-id="d301e-103">Restrict access to a storefront during testing or development</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d301e-104">In dit onderwerp wordt uitgelegd hoe u de toegang tot een Microsoft Dynamics 365 Commerce-winkel kunt beperken terwijl interne testen of ontwikkeling plaatsvinden.</span><span class="sxs-lookup"><span data-stu-id="d301e-104">This topic explains how to restrict access to a Microsoft Dynamics 365 Commerce storefront while internal testing or development is occurring.</span></span>

## <a name="description"></a><span data-ttu-id="d301e-105">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="d301e-105">Description</span></span>

<span data-ttu-id="d301e-106">Tijdens het interne testen of tijdens de actieve ontwikkeling wilt u mogelijk de toegang tot uw site beperken om te voorkomen dat externe gebruikers de gepubliceerde pagina's van winkels openen.</span><span class="sxs-lookup"><span data-stu-id="d301e-106">During internal testing or active development, you might want to restrict access to your site to prevent external users from accessing the published storefront pages.</span></span>

## <a name="resolution"></a><span data-ttu-id="d301e-107">Oplossing</span><span class="sxs-lookup"><span data-stu-id="d301e-107">Resolution</span></span>

### <a name="set-up-azure-ad-b2c-by-using-standard-user-flows"></a><span data-ttu-id="d301e-108">Azure AD B2C instellen met behulp van standaardgebruikersstromen</span><span class="sxs-lookup"><span data-stu-id="d301e-108">Set up Azure AD B2C by using standard user flows</span></span>

<span data-ttu-id="d301e-109">Zie [Een B2C-tenant instellen in Commerce](../set-up-b2c-tenant.md) voor informatie over het configureren van Azure Active Directory B2C (Azure AD B2C) voor uw e-commercesite.</span><span class="sxs-lookup"><span data-stu-id="d301e-109">For information about how to configure Azure Active Directory B2C (Azure AD B2C) for your e-commerce site, see [Set up a B2C tenant in Commerce](../set-up-b2c-tenant.md).</span></span>

### <a name="restrict-user-access-to-storefront-pages-and-block-the-creation-of-new-users"></a><span data-ttu-id="d301e-110">Toegang van gebruikers tot winkelpagina's beperken en het maken van nieuwe gebruikers blokkeren</span><span class="sxs-lookup"><span data-stu-id="d301e-110">Restrict user access to storefront pages and block the creation of new users</span></span>

<span data-ttu-id="d301e-111">Volg deze stappen om gebruikerstoegang tot winkelpagina's in Commerce Site Builder te beperken.</span><span class="sxs-lookup"><span data-stu-id="d301e-111">To restrict user access to storefront pages in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="d301e-112">Ga naar uw site.</span><span class="sxs-lookup"><span data-stu-id="d301e-112">Go to your site.</span></span>
1. <span data-ttu-id="d301e-113">Selecteer **Pagina's** en selecteer vervolgens de pagina waarvoor u de gebruikerstoegang wilt beperken.</span><span class="sxs-lookup"><span data-stu-id="d301e-113">Select **Pages**, and then select the page to restrict user access for.</span></span>
1. <span data-ttu-id="d301e-114">Selecteer het module- of fragmentvak en selecteer **Bewerken**.</span><span class="sxs-lookup"><span data-stu-id="d301e-114">Select the module or fragment slot, and then select **Edit**.</span></span>
1. <span data-ttu-id="d301e-115">Selecteer In het eigenschappendeelvenster de optie **Aanmelden vereist?** en selecteer **Bewerken voltooien**.</span><span class="sxs-lookup"><span data-stu-id="d301e-115">In the properties pane, select **Requires sign-in?**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="d301e-116">Selecteer **Publiceren**.</span><span class="sxs-lookup"><span data-stu-id="d301e-116">Select **Publish**.</span></span>

<span data-ttu-id="d301e-117">Volg deze stappen om het maken van nieuwe Azure AD-gebruikers te blokkeren.</span><span class="sxs-lookup"><span data-stu-id="d301e-117">To block the creation of new users in Azure AD, follow these steps.</span></span>

1. <span data-ttu-id="d301e-118">Ga naar de [Azure-portal](https://portal.azure.com/).</span><span class="sxs-lookup"><span data-stu-id="d301e-118">Go to the [Azure portal](https://portal.azure.com/).</span></span>
1. <span data-ttu-id="d301e-119">Selecteer de Azure AD B2C-toepassing die u voor toegang tot uw site hebt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="d301e-119">Select the Azure AD B2C application that you created for your site access.</span></span>
1. <span data-ttu-id="d301e-120">Selecteer **Gebruikersstromen** in het navigatievenster aan de linkerkant.</span><span class="sxs-lookup"><span data-stu-id="d301e-120">In the left navigation, select **User flows**.</span></span>
1. <span data-ttu-id="d301e-121">Selecteer boven aan de pagina **Gebruikersstromen** de optie **Nieuwe gebruikersstroom**.</span><span class="sxs-lookup"><span data-stu-id="d301e-121">At the top of the **User Flows** page, select **New user flow**.</span></span>
1. <span data-ttu-id="d301e-122">Selecteer op de pagina **Een gebruikersstroomtype selecteren** de optie **Voorbeeld**.</span><span class="sxs-lookup"><span data-stu-id="d301e-122">On the **Select a user flow type** page, select **Preview**.</span></span>
1. <span data-ttu-id="d301e-123">Selecteer **Aanmelden v2** op het midden van de pagina.</span><span class="sxs-lookup"><span data-stu-id="d301e-123">In the middle of the page, select **Sign in v2**.</span></span> <span data-ttu-id="d301e-124">Volg daarna de stappen in [Een B2C-tenant instellen in Commerce](../set-up-b2c-tenant.md) om de stroom te configureren als de standaardgebruikersstroom van uw site voor Azure AD B2C tijdens het testen of ontwikkelen.</span><span class="sxs-lookup"><span data-stu-id="d301e-124">Then follow the steps in [Set up a B2C tenant in Commerce](../set-up-b2c-tenant.md) to configure the flow as your site's standard user flow for Azure AD B2C during testing or development.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d301e-125">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="d301e-125">Additional resources</span></span>

[<span data-ttu-id="d301e-126">Een B2C-tenant instellen in Commerce</span><span class="sxs-lookup"><span data-stu-id="d301e-126">Set up a B2C tenant in Commerce</span></span>](../set-up-b2c-tenant.md)

[<span data-ttu-id="d301e-127">Aangepaste pagina's voor gebruikersaanmeldingen instellen</span><span class="sxs-lookup"><span data-stu-id="d301e-127">Set up custom pages for user sign-ins</span></span>](../custom-pages-user-logins.md)
