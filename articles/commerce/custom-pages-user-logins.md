---
title: Aangepaste pagina's voor gebruikersaanmeldingen instellen
description: In dit onderwerp wordt beschreven hoe u aangepaste pagina's maakt in Microsoft Dynamics 365 Commerce voor het verwerken van aangepaste aanmeldingen voor gebruikers van B2C-tenants (business-to-consumers) met Azure Active Directory (Azure AD).
author: brianshook
manager: annbe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 3328fad5328ae1954a6749f9a5eebcb71c723698
ms.sourcegitcommit: c88b54ba13a4dfe39b844ffaced4dc435560c47d
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/19/2021
ms.locfileid: "5477943"
---
# <a name="set-up-custom-pages-for-user-sign-ins"></a><span data-ttu-id="e5efb-103">Aangepaste pagina's voor gebruikersaanmeldingen instellen</span><span class="sxs-lookup"><span data-stu-id="e5efb-103">Set up custom pages for user sign-ins</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="e5efb-104">In dit onderwerp wordt beschreven hoe u aangepaste pagina's maakt in Microsoft Dynamics 365 Commerce voor het verwerken van aangepaste aanmeldingen voor gebruikers van B2C-tenants (business-to-consumers) met Azure Active Directory (Azure AD).</span><span class="sxs-lookup"><span data-stu-id="e5efb-104">This topic describes how to build custom pages in Microsoft Dynamics 365 Commerce that handle customized sign-ins for users of Azure Active Directory (Azure AD) business-to-consumer (B2C) tenants.</span></span>

<span data-ttu-id="e5efb-105">Als u aangepaste pagina's wilt gebruiken die zijn gemaakt in Dynamics 365 Commerce waarin de aanmeldingsgegevens van gebruikers worden afgehandeld, moet u het Azure AD-beleid instellen waarnaar wordt verwezen in de Commerce-omgeving.</span><span class="sxs-lookup"><span data-stu-id="e5efb-105">To use custom pages that are authored in Dynamics 365 Commerce to handle user sign-in flows, you must set up the Azure AD policies that will be referenced in the Commerce environment.</span></span> <span data-ttu-id="e5efb-106">U kunt Azure AD B2C-beleidsregels configureren voor 'Registreren en aanmelden', 'Profiel bewerken' en 'Wachtwoord opnieuw instellen' met behulp van de Azure AD B2C-toepassing.</span><span class="sxs-lookup"><span data-stu-id="e5efb-106">You can configure the "Sign up and sign in," "Profile editing," and "Password reset" Azure AD B2C policies by using the Azure AD B2C application.</span></span> <span data-ttu-id="e5efb-107">Vervolgens kan worden verwezen naar de namen van de Azure AD B2C-tenant en het beleid tijdens het inrichtingsproces dat voor de Commerce-omgeving wordt uitgevoerd met Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="e5efb-107">The Azure AD B2C tenant and policy names can then be referenced during the provisioning process that is done for the Commerce environment by using Microsoft Dynamics Lifecycle Services (LCS).</span></span>

<span data-ttu-id="e5efb-108">U kunt de aangepaste Commerce-pagina's maken met behulp van de modules voor registreren, aanmelden, accountprofiel bewerken of wachtwoord opnieuw instellen.</span><span class="sxs-lookup"><span data-stu-id="e5efb-108">The custom Commerce pages can be built by using the sign in, sign up, account profile edit, or password reset module.</span></span> <span data-ttu-id="e5efb-109">De pagina-URL's die voor deze aangepaste pagina's worden gepubliceerd, moeten vervolgens worden opgenomen in de Azure AD B2C-beleidsconfiguraties in de Azure-portal.</span><span class="sxs-lookup"><span data-stu-id="e5efb-109">The page URLs that are published for these custom pages should then be referenced in Azure AD B2C policy configurations in the Azure portal.</span></span>

## <a name="set-up-b2c-policies"></a><span data-ttu-id="e5efb-110">B2C-beleid instellen</span><span class="sxs-lookup"><span data-stu-id="e5efb-110">Set up B2C policies</span></span>

<span data-ttu-id="e5efb-111">Nadat u uw Azure AD B2C-tenant hebt ingesteld en deze aan uw Commerce-omgeving hebt gekoppeld, gaat u naar de pagina **Azure AD B2C** in de Azure-portal en selecteert u in het menu **Beleid** de optie **Gebruikersstromen (beleid)**.</span><span class="sxs-lookup"><span data-stu-id="e5efb-111">After you set up your Azure AD B2C tenant and associate it with your Commerce environment, go to the **Azure AD B2C** page in the Azure portal, and then, on the menu, under **Policies**, select **User flows (policies)**.</span></span>

![Gebruikersstromen (beleid), opdracht in het menu](./media/B2C_CustomPage_PoliciesMenu.png)

<span data-ttu-id="e5efb-113">U kunt nu de aanmeldingsstromen configureren voor 'Registreren en aanmelden', 'Profiel bewerken' en 'Wachtwoord opnieuw instellen'.</span><span class="sxs-lookup"><span data-stu-id="e5efb-113">You can now configure the "Sign up and sign in," "Profile editing," and "Password reset" user sign-in flows.</span></span>

### <a name="configure-the-sign-up-and-sign-in-policy"></a><span data-ttu-id="e5efb-114">Het beleid voor 'Registreren en aanmelden' configureren</span><span class="sxs-lookup"><span data-stu-id="e5efb-114">Configure the "Sign up and sign in" policy</span></span>

<span data-ttu-id="e5efb-115">Voer de volgende stappen uit om het beleid voor 'Registreren en aanmelden' te configureren.</span><span class="sxs-lookup"><span data-stu-id="e5efb-115">To configure the "Sign up and sign in" policy, follow these steps.</span></span>

1. <span data-ttu-id="e5efb-116">Selecteer **Nieuwe gebruikersstroom** en vervolgens op het tabblad **Aanbevolen** het beleid **Registreren en aanmelden**.</span><span class="sxs-lookup"><span data-stu-id="e5efb-116">Select **New user flow**, and then, on the **Recommended** tab, select the **Sign up and sign in** policy.</span></span>
1. <span data-ttu-id="e5efb-117">Voer een naam in voor het beleid (bijvoorbeeld **B2C\_1\_SignInSignUp**).</span><span class="sxs-lookup"><span data-stu-id="e5efb-117">Enter a name for the policy (for example, **B2C\_1\_SignInSignUp**).</span></span>
1. <span data-ttu-id="e5efb-118">Selecteer in de sectie **Identiteitsproviders** de identiteitsproviders die u voor het beleid wilt gebruiken.</span><span class="sxs-lookup"><span data-stu-id="e5efb-118">In the **Identity Providers** section, select the identity providers to use for the policy.</span></span> <span data-ttu-id="e5efb-119">U moet minimaal **E-mailaanmelding** selecteren.</span><span class="sxs-lookup"><span data-stu-id="e5efb-119">At a minimum, **Email signup** must be selected.</span></span>
1. <span data-ttu-id="e5efb-120">Schakel in de kolom **Kenmerk verzamelen** de selectievakjes in voor **E-mailadres**, **Voornaam** en **Achternaam**.</span><span class="sxs-lookup"><span data-stu-id="e5efb-120">In the **Collect attribute** column, select the check boxes for **Email Address**, **Given Name**, and **Surname**.</span></span>
1. <span data-ttu-id="e5efb-121">Schakel in de kolom **Claim terugsturen** de selectievakjes in voor **E-mailadressen**, **Voornaam**, **Identiteitsprovider**, **Achternaam** en **Object-id van de gebruiker**.</span><span class="sxs-lookup"><span data-stu-id="e5efb-121">In the **Return claim** column, select the check boxes for **Email Addresses**, **Given Name**, **Identity Provider**, **Surname**, and **User's Object ID**.</span></span>

    ![Geselecteerde kenmerken en claims](./media/B2C_SignInSignUp_Attributes.png)

1. <span data-ttu-id="e5efb-123">Selecteer **OK** om het beleid te maken.</span><span class="sxs-lookup"><span data-stu-id="e5efb-123">Select **OK** to create the policy.</span></span>
1. <span data-ttu-id="e5efb-124">Dubbelklik op de nieuwe beleidsnaam en selecteer vervolgens **Eigenschappen** in het navigatievenster.</span><span class="sxs-lookup"><span data-stu-id="e5efb-124">Double-click the new policy name, and then, in the navigation pane, select **Properties**.</span></span>
1. <span data-ttu-id="e5efb-125">Stel de optie **Pagina-indeling afdwingen met JavaScript inschakelen (preview)** in op **Aan**.</span><span class="sxs-lookup"><span data-stu-id="e5efb-125">Set the **Enable JavaScript enforcing page layout (preview)** option to **On**.</span></span>

    ![Eigenschappenpagina voor het nieuwe beleid](./media/B2C_SignInSignUp_EnableJavascript.png)

> [!NOTE]
> <span data-ttu-id="e5efb-127">In de Commerce-omgeving wordt verwezen naar de volledig beleidsnaam.</span><span class="sxs-lookup"><span data-stu-id="e5efb-127">The policy name will be fully referenced in the Commerce environment.</span></span> <span data-ttu-id="e5efb-128">(Het voorvoegsel **B2C\_1\_** wordt opgenomen in de verwijzing.) De naam van beleid kan niet worden gewijzigd nadat dit zijn gemaakt.</span><span class="sxs-lookup"><span data-stu-id="e5efb-128">(The **B2C\_1\_** prefix will be included in the reference.) Policies can't be renamed after they are created.</span></span> <span data-ttu-id="e5efb-129">Als u een bestaand beleid vervangt voor uw Commerce-omgeving, kunt u het oorspronkelijke beleid verwijderen en een nieuw beleid met dezelfde naam maken.</span><span class="sxs-lookup"><span data-stu-id="e5efb-129">If you're replacing an existing policy for your Commerce environment, you can delete the original policy and build a new policy that has the same name.</span></span> <span data-ttu-id="e5efb-130">Als de omgeving al is ingericht, kunt u de nieuwe beleidsnaam indienen via een serviceaanvraag.</span><span class="sxs-lookup"><span data-stu-id="e5efb-130">Alternatively, if the environment has already been provisioned, you can submit the new policy name through a service request.</span></span>

<span data-ttu-id="e5efb-131">U keert terug naar dit beleid om de instellingen te voltooien nadat u de aangepaste pagina's hebt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="e5efb-131">You will return to this policy to finish the setup after you've built the custom pages.</span></span> <span data-ttu-id="e5efb-132">Sluit het beleid voor nu af om terug te keren naar de pagina **Gebruikersstromen (beleid)** in de Azure-portal.</span><span class="sxs-lookup"><span data-stu-id="e5efb-132">For now, close the policy to return to the **User flows (policies)** page in the Azure portal.</span></span>

### <a name="configure-the-profile-editing-policy"></a><span data-ttu-id="e5efb-133">Het beleid voor het 'Profiel bewerken' configureren</span><span class="sxs-lookup"><span data-stu-id="e5efb-133">Configure the "Profile editing" policy</span></span>

<span data-ttu-id="e5efb-134">Ga als volgt te werk om het beleid voor 'Profiel bewerken' te configureren.</span><span class="sxs-lookup"><span data-stu-id="e5efb-134">To configure the "Profile editing" policy, follow these steps.</span></span>

1. <span data-ttu-id="e5efb-135">Selecteer **Nieuwe gebruikersstroom** en vervolgens op het tabblad **Aanbevolen** het beleid **Profiel bewerken**.</span><span class="sxs-lookup"><span data-stu-id="e5efb-135">Select **New user flow**, and then, on the **Recommended** tab, select the **Profile editing** policy.</span></span>
1. <span data-ttu-id="e5efb-136">Voer een naam in voor het beleid (bijvoorbeeld **B2C\_1\_EditProfile**).</span><span class="sxs-lookup"><span data-stu-id="e5efb-136">Enter a name for the policy (for example, **B2C\_1\_EditProfile**).</span></span>
1. <span data-ttu-id="e5efb-137">Selecteer in de sectie **Identiteitsproviders** de identiteitsproviders die u voor het beleid wilt gebruiken.</span><span class="sxs-lookup"><span data-stu-id="e5efb-137">In the **Identity Providers** section, select the identity providers to use for the policy.</span></span> <span data-ttu-id="e5efb-138">U moet minimaal een **Aanmelding voor een lokaal account** selecteren.</span><span class="sxs-lookup"><span data-stu-id="e5efb-138">At a minimum, **Local Account SignIn** must be selected.</span></span>
1. <span data-ttu-id="e5efb-139">Schakel in de kolom **Kenmerk verzamelen** de selectievakjes in voor **E-mailadressen** en **Achternaam**.</span><span class="sxs-lookup"><span data-stu-id="e5efb-139">In the **Collect attribute** column, select the check boxes for **Email Addresses** and **Surname**.</span></span>
1. <span data-ttu-id="e5efb-140">Schakel in de kolom **Claim terugsturen** de selectievakjes in voor **E-mailadressen**, **Voornaam**, **Identiteitsprovider**, **Achternaam** en **Object-id van de gebruiker**.</span><span class="sxs-lookup"><span data-stu-id="e5efb-140">In the **Return claim** column, select the check boxes for **Email Addresses**, **Given Name**, **Identity Provider**, **Surname**, and **User's Object ID**.</span></span>
1. <span data-ttu-id="e5efb-141">Selecteer **OK** om het beleid te maken.</span><span class="sxs-lookup"><span data-stu-id="e5efb-141">Select **OK** to create the policy.</span></span>
1. <span data-ttu-id="e5efb-142">Dubbelklik op de nieuwe beleidsnaam en selecteer vervolgens **Eigenschappen** in het navigatievenster.</span><span class="sxs-lookup"><span data-stu-id="e5efb-142">Double-click the new policy name, and then, in the navigation pane, select **Properties**.</span></span>
1. <span data-ttu-id="e5efb-143">Stel de optie **Pagina-indeling afdwingen met JavaScript inschakelen (preview)** in op **Aan**.</span><span class="sxs-lookup"><span data-stu-id="e5efb-143">Set the **Enable JavaScript enforcing page layout (preview)** option to **On**.</span></span>

<span data-ttu-id="e5efb-144">U keert terug naar dit beleid om de instellingen te voltooien nadat u de aangepaste pagina's hebt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="e5efb-144">You will return to this policy to finish the setup after you've built the custom pages.</span></span> <span data-ttu-id="e5efb-145">Sluit het beleid voor nu af om terug te keren naar de pagina **Gebruikersstromen (beleid)** in de Azure-portal.</span><span class="sxs-lookup"><span data-stu-id="e5efb-145">For now, close the policy to return to the **User flows (policies)** page in the Azure portal.</span></span>

### <a name="configure-the-password-reset-policy"></a><span data-ttu-id="e5efb-146">Het beleid voor 'Wachtwoord opnieuw instellen' configureren</span><span class="sxs-lookup"><span data-stu-id="e5efb-146">Configure the "Password reset" policy</span></span>

<span data-ttu-id="e5efb-147">Ga als volgt te werk om het beleid voor 'Wachtwoord opnieuw instellen' te configureren.</span><span class="sxs-lookup"><span data-stu-id="e5efb-147">To configure the "Password reset" policy, follow these steps.</span></span>

1. <span data-ttu-id="e5efb-148">Selecteer **Nieuwe gebruikersstroom** en vervolgens op het tabblad **Preview** het beleid **Wachtwoord opnieuw instellen v1.1**.</span><span class="sxs-lookup"><span data-stu-id="e5efb-148">Select **New user flow**, and then, on the **Preview** tab, select the **Password reset v1.1** policy.</span></span>

    ![Beleid voor Wachtwoord opnieuw instellen v1.1 geselecteerd op het tabblad Preview](./media/B2C_ForgetPassword_Menu.png)

1. <span data-ttu-id="e5efb-150">Voer een naam in voor het beleid (bijvoorbeeld **B2C\_1\_ForgetPassword**).</span><span class="sxs-lookup"><span data-stu-id="e5efb-150">Enter a name for the policy (for example, **B2C\_1\_ForgetPassword**).</span></span>
1. <span data-ttu-id="e5efb-151">Selecteer in de sectie **Identiteitsproviders** de optie **Wachtwoord via e-mailadres opnieuw instellen**.</span><span class="sxs-lookup"><span data-stu-id="e5efb-151">In the **Identity Providers** section, select **Reset password using email address**.</span></span>
1. <span data-ttu-id="e5efb-152">Schakel in de kolom **Claim terugsturen** de selectievakjes in voor **E-mailadressen**, **Voornaam**, **Achternaam** en **Object-id van de gebruiker**.</span><span class="sxs-lookup"><span data-stu-id="e5efb-152">In the **Return claim** column, select the check boxes for **Email Addresses**, **Given Name**, **Surname**, and **User's Object ID**.</span></span>

    ![Geselecteerde claims](./media/B2C_ForgetPassword_Attributes.png)

1. <span data-ttu-id="e5efb-154">Selecteer **OK** om het beleid te maken.</span><span class="sxs-lookup"><span data-stu-id="e5efb-154">Select **OK** to create the policy.</span></span>
1. <span data-ttu-id="e5efb-155">Dubbelklik op de nieuwe beleidsnaam en selecteer vervolgens **Eigenschappen** in het navigatievenster.</span><span class="sxs-lookup"><span data-stu-id="e5efb-155">Double-click the new policy name, and then, in the navigation pane, select **Properties**.</span></span>
1. <span data-ttu-id="e5efb-156">Stel de optie **Pagina-indeling afdwingen met JavaScript inschakelen (preview)** in op **Aan**.</span><span class="sxs-lookup"><span data-stu-id="e5efb-156">Set the **Enable JavaScript enforcing page layout (preview)** option to **On**.</span></span>

<span data-ttu-id="e5efb-157">U keert terug naar dit beleid om de instellingen te voltooien nadat u de aangepaste pagina's hebt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="e5efb-157">You will return to this policy to finish the setup after you've built the custom pages.</span></span> <span data-ttu-id="e5efb-158">Sluit het beleid voor nu af om terug te keren naar de pagina **Gebruikersstromen (beleid)** in de Azure-portal.</span><span class="sxs-lookup"><span data-stu-id="e5efb-158">For now, close the policy to return to the **User flows (policies)** page in the Azure portal.</span></span>

## <a name="build-the-custom-pages"></a><span data-ttu-id="e5efb-159">Aangepaste pagina's maken</span><span class="sxs-lookup"><span data-stu-id="e5efb-159">Build the custom pages</span></span>

<span data-ttu-id="e5efb-160">Ga als volgt te werk om de aangepaste pagina's te maken voor het verwerken van gebruikersaanmeldingen.</span><span class="sxs-lookup"><span data-stu-id="e5efb-160">To build the custom pages to handle user sign-ins, follow these steps.</span></span>

1. <span data-ttu-id="e5efb-161">Ga in de Commerce-ontwerpfunctie naar uw site.</span><span class="sxs-lookup"><span data-stu-id="e5efb-161">In the Commerce authoring tools, go to your site.</span></span>
1. <span data-ttu-id="e5efb-162">Maak de volgende vijf sjablonen en vijf pagina's:</span><span class="sxs-lookup"><span data-stu-id="e5efb-162">Build the following five templates and five pages:</span></span>

    - <span data-ttu-id="e5efb-163">Een sjabloon **Aanmelden** en een pagina waarop de aanmeldingsmodule wordt gebruikt.</span><span class="sxs-lookup"><span data-stu-id="e5efb-163">A **Sign In** template and page that use the sign in module.</span></span>
    - <span data-ttu-id="e5efb-164">Een sjabloon **Registreren** en een pagina waarop de registratiemodule wordt gebruikt.</span><span class="sxs-lookup"><span data-stu-id="e5efb-164">A **Sign Up** template and page that use the sign up module.</span></span>
    - <span data-ttu-id="e5efb-165">Een sjabloon **Wachtwoord opnieuw instellen** en een pagina waarop de module Wachtwoord opnieuw instellen wordt gebruikt.</span><span class="sxs-lookup"><span data-stu-id="e5efb-165">A **Password Reset** template and page that use the password reset module.</span></span>
    - <span data-ttu-id="e5efb-166">Een sjabloon **Verificatie voor wachtwoord opnieuw instellen** en een pagina waarop de verificatiemodule voor Wachtwoord opnieuw instellen wordt gebruikt.</span><span class="sxs-lookup"><span data-stu-id="e5efb-166">A **Password Reset verification** template and page that use the password reset verification module.</span></span>
    - <span data-ttu-id="e5efb-167">Een sjabloon **Profiel bewerken** en een pagina waarop de module Accountprofiel bewerken wordt gebruikt</span><span class="sxs-lookup"><span data-stu-id="e5efb-167">A **Profile Edit** template and page that use the account profile edit module</span></span>

<span data-ttu-id="e5efb-168">Volg de volgende richtlijnen wanneer u de pagina's bouwt:</span><span class="sxs-lookup"><span data-stu-id="e5efb-168">When you build the pages, follow these guidelines:</span></span>

- <span data-ttu-id="e5efb-169">Gebruik voor elke pagina of module de indeling en de stijl die het best aansluiten bij uw zakelijke vereisten.</span><span class="sxs-lookup"><span data-stu-id="e5efb-169">For each page or module, use the layout and style that best suit your business requirements.</span></span>
- <span data-ttu-id="e5efb-170">Publiceer alle pagina's en URL's die moeten worden gebruikt in de Azure AD B2C-configuratie.</span><span class="sxs-lookup"><span data-stu-id="e5efb-170">Publish all pages and URLs that must be used in the Azure AD B2C setup.</span></span>
- <span data-ttu-id="e5efb-171">Nadat de pagina's en URL's zijn gepubliceerd, verzamelt u de URL's die moeten worden gebruikt voor de Azure AD B2C-beleidsconfiguraties.</span><span class="sxs-lookup"><span data-stu-id="e5efb-171">After the pages and URLs are published, collect the URLs that must be used for the Azure AD B2C policy configurations.</span></span> <span data-ttu-id="e5efb-172">Het achtervoegsel **?preloadscripts=true** wordt toegevoegd aan elke URL wanneer deze wordt gebruikt.</span><span class="sxs-lookup"><span data-stu-id="e5efb-172">A **?preloadscripts=true** suffix will be added to every URL when it's used.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e5efb-173">Gebruik universele kop- en voetteksten met relatieve koppelingen niet opnieuw.</span><span class="sxs-lookup"><span data-stu-id="e5efb-173">Don't reuse universal headers and footers that have relative links.</span></span> <span data-ttu-id="e5efb-174">Aangezien deze pagina's in het Azure AD B2C-domein worden gehost wanneer ze worden gebruikt, moeten alleen absolute URL's worden gebruikt voor alle koppelingen.</span><span class="sxs-lookup"><span data-stu-id="e5efb-174">Because these pages will be hosted in the Azure AD B2C domain when they are used, only absolute URLs should be used for all links.</span></span>

## <a name="configure-azure-ad-b2c-policies-with-custom-page-information"></a><span data-ttu-id="e5efb-175">Azure AD B2C-beleid configureren met aangepaste paginagegevens</span><span class="sxs-lookup"><span data-stu-id="e5efb-175">Configure Azure AD B2C policies with custom page information</span></span> 

<span data-ttu-id="e5efb-176">Ga in de Azure-portal terug naar de pagina **Azure AD B2C** en selecteer in het menu **Beleid** de optie **Gebruikersstromen (beleid)**.</span><span class="sxs-lookup"><span data-stu-id="e5efb-176">In the Azure portal, return to the **Azure AD B2C** page, and then, on the menu, under **Policies**, select **User flows (policies)**.</span></span>

### <a name="update-the-sign-up-and-sign-in-policy-with-custom-page-information"></a><span data-ttu-id="e5efb-177">Het beleid 'Registreren en aanmelden' bijwerken met aangepaste paginagegevens</span><span class="sxs-lookup"><span data-stu-id="e5efb-177">Update the "Sign up and sign in" policy with custom page information</span></span>

<span data-ttu-id="e5efb-178">Volg deze stappen om het beleid 'Registreren en aanmelden' bij te werken met aangepaste paginagegevens.</span><span class="sxs-lookup"><span data-stu-id="e5efb-178">To update the "Sign up and sign in" policy with custom page information, follow these steps.</span></span>

1. <span data-ttu-id="e5efb-179">Selecteer In het beleid voor **Registreren en aanmelden** dat u eerder hebt geconfigureerd, de optie **Pagina-indelingen** in het navigatievenster.</span><span class="sxs-lookup"><span data-stu-id="e5efb-179">In the **Sign in and sign up** policy that you configured earlier, in the navigation pane, select **Page layouts**.</span></span>
1. <span data-ttu-id="e5efb-180">Selecteer de indeling voor **Gecombineerde pagina voor Registreren en aanmelden**.</span><span class="sxs-lookup"><span data-stu-id="e5efb-180">Select the **Unified sign up or sign in page** layout.</span></span>
1. <span data-ttu-id="e5efb-181">Stel de optie **Aangepaste paginainhoud gebruiken** in op **Ja**.</span><span class="sxs-lookup"><span data-stu-id="e5efb-181">Set the **Use custom page content** option to **Yes**.</span></span>
1. <span data-ttu-id="e5efb-182">Voer in het veld **Aangepaste pagina-URI** de volledige aanmeldings-URL in.</span><span class="sxs-lookup"><span data-stu-id="e5efb-182">In the **Custom page URI** field, enter the full sign-in URL.</span></span> <span data-ttu-id="e5efb-183">Neem het achtervoegsel **?preloadscripts=true** op.</span><span class="sxs-lookup"><span data-stu-id="e5efb-183">Include the **?preloadscripts=true** suffix.</span></span> <span data-ttu-id="e5efb-184">Voer bijvoorbeeld ``www.<my domain>.com/sign-in?preloadscripts=true`` in.</span><span class="sxs-lookup"><span data-stu-id="e5efb-184">For example, enter ``www.<my domain>.com/sign-in?preloadscripts=true``.</span></span>
1. <span data-ttu-id="e5efb-185">Selecteer in het veld **Versie van pagina-indeling (Preview)** **1.2.0**.</span><span class="sxs-lookup"><span data-stu-id="e5efb-185">In the **Page Layout Version (Preview)** field, select **1.2.0**.</span></span>
1. <span data-ttu-id="e5efb-186">Selecteer de indeling **Lokale accountaanmeldingspagina**.</span><span class="sxs-lookup"><span data-stu-id="e5efb-186">Select the **Local account sign up page** layout.</span></span>
1. <span data-ttu-id="e5efb-187">Stel de optie **Aangepaste paginainhoud gebruiken** in op **Ja**.</span><span class="sxs-lookup"><span data-stu-id="e5efb-187">Set the **Use custom page content** option to **Yes**.</span></span>
1. <span data-ttu-id="e5efb-188">Voer in het veld **Aangepaste pagina-URI** de volledige aanmeldings-URL in.</span><span class="sxs-lookup"><span data-stu-id="e5efb-188">In the **Custom page URI** field, enter the full sign-up URL.</span></span> <span data-ttu-id="e5efb-189">Neem het achtervoegsel **?preloadscripts=true** op.</span><span class="sxs-lookup"><span data-stu-id="e5efb-189">Include the **?preloadscripts=true** suffix.</span></span> <span data-ttu-id="e5efb-190">Voer bijvoorbeeld ``www.<my domain>.com/sign-up?preloadscripts=true`` in.</span><span class="sxs-lookup"><span data-stu-id="e5efb-190">For example, enter ``www.<my domain>.com/sign-up?preloadscripts=true``.</span></span>
1. <span data-ttu-id="e5efb-191">Selecteer in het veld **Versie van pagina-indeling (Preview)** **1.2.0**.</span><span class="sxs-lookup"><span data-stu-id="e5efb-191">In the **Page Layout Version (Preview)** field, select **1.2.0**.</span></span>
1. <span data-ttu-id="e5efb-192">Voer de volgende stappen uit in de sectie **Gebruikerskenmerken**:</span><span class="sxs-lookup"><span data-stu-id="e5efb-192">In the **User attributes** section, follow these steps:</span></span>

    1. <span data-ttu-id="e5efb-193">Selecteer **Nee** in het veld **Verificatie vereist** voor de kenmerken **E-mailadres**, **Voornaam** en **Achternaam**.</span><span class="sxs-lookup"><span data-stu-id="e5efb-193">For the **Email Address**, **Given Name**, and **Surname** attributes, select **No** in the **Requires Verification** field.</span></span>
    1. <span data-ttu-id="e5efb-194">Selecteer **Nee** in het veld **Optioneel** voor de kenmerken **Voornaam** en **Achternaam**.</span><span class="sxs-lookup"><span data-stu-id="e5efb-194">For the **Given Name** and **Surname** attributes, select **No** in the **Optional** field.</span></span>

    ![Configuratie van het beleid voor lokale accountaanmeldingspagina](./media/B2C_SignUp_PageURLConfig.png)

### <a name="update-the-profile-editing-policy-with-custom-page-information"></a><span data-ttu-id="e5efb-196">Het beleid 'Profiel bewerken' bijwerken met aangepaste paginagegevens</span><span class="sxs-lookup"><span data-stu-id="e5efb-196">Update the "Profile editing" policy with custom page information</span></span>

<span data-ttu-id="e5efb-197">Volg deze stappen om het beleid 'Profiel bewerken' bij te werken met aangepaste paginagegevens.</span><span class="sxs-lookup"><span data-stu-id="e5efb-197">To update the "Profile editing" policy with custom page information, follow these steps.</span></span>

1. <span data-ttu-id="e5efb-198">Selecteer In het beleid voor **Profiel bewerken** dat u eerder hebt geconfigureerd, de optie **Pagina-indelingen** in het navigatievenster.</span><span class="sxs-lookup"><span data-stu-id="e5efb-198">In the **Profile Editing** policy that you configured earlier, in the navigation pane, select **Page layouts**.</span></span>
1. <span data-ttu-id="e5efb-199">Selecteer de indeling voor de **pagina Profiel bewerken**.</span><span class="sxs-lookup"><span data-stu-id="e5efb-199">Select the **Profile edit page** layout.</span></span>
1. <span data-ttu-id="e5efb-200">Stel de optie **Aangepaste paginainhoud gebruiken** in op **Ja**.</span><span class="sxs-lookup"><span data-stu-id="e5efb-200">Set the **Use custom page content** option to **Yes**.</span></span>
1. <span data-ttu-id="e5efb-201">Voer in het veld **Aangepaste pagina-URI** de volledige URL voor profielbewerking in.</span><span class="sxs-lookup"><span data-stu-id="e5efb-201">In the **Custom page URI** field, enter the full profile edit URL.</span></span> <span data-ttu-id="e5efb-202">Neem het achtervoegsel **?preloadscripts=true** op.</span><span class="sxs-lookup"><span data-stu-id="e5efb-202">Include the **?preloadscripts=true** suffix.</span></span> <span data-ttu-id="e5efb-203">Voer bijvoorbeeld ``www.<my domain>.com/profile-edit?preloadscripts=true`` in.</span><span class="sxs-lookup"><span data-stu-id="e5efb-203">For example, enter ``www.<my domain>.com/profile-edit?preloadscripts=true``.</span></span>
1. <span data-ttu-id="e5efb-204">Selecteer in het veld **Versie van pagina-indeling (Preview)** **1.2.0**.</span><span class="sxs-lookup"><span data-stu-id="e5efb-204">In the **Page Layout Version (Preview)** field, select **1.2.0**.</span></span>
1. <span data-ttu-id="e5efb-205">Voer de volgende stappen uit in de sectie **Gebruikerskenmerken**:</span><span class="sxs-lookup"><span data-stu-id="e5efb-205">In the **User attributes** section, follow these steps:</span></span>

    1. <span data-ttu-id="e5efb-206">Selecteer **Nee** in het veld **Verificatie vereist** voor de kenmerken **E-mailadres** en **Voornaam**.</span><span class="sxs-lookup"><span data-stu-id="e5efb-206">For the **Email Address**, **Given Name** attributes, select **No** in the **Requires Verification** field.</span></span>
    1. <span data-ttu-id="e5efb-207">Selecteer **Nee** in het veld **Optioneel** voor de kenmerken **Voornaam** en **Achternaam**.</span><span class="sxs-lookup"><span data-stu-id="e5efb-207">For the **Given Name** and **Surname** attributes, select **No** in the **Optional** field.</span></span>

### <a name="update-the-password-reset-policy-with-custom-page-information"></a><span data-ttu-id="e5efb-208">Het beleid 'Wachtwoord opnieuw instellen' bijwerken met aangepaste paginagegevens</span><span class="sxs-lookup"><span data-stu-id="e5efb-208">Update the "Password reset" policy with custom page information</span></span>

<span data-ttu-id="e5efb-209">Volg deze stappen om het beleid 'Wachtwoord opnieuw instellen' bij te werken met aangepaste paginagegevens.</span><span class="sxs-lookup"><span data-stu-id="e5efb-209">To update the "Password reset" policy with custom page information, follow these steps.</span></span>

1. <span data-ttu-id="e5efb-210">Selecteer In het beleid voor **Wachtwoord opnieuw instellen** dat u eerder hebt geconfigureerd, de optie **Pagina-indelingen** in het navigatievenster.</span><span class="sxs-lookup"><span data-stu-id="e5efb-210">In the **Password Reset** policy that you configured earlier, in the navigation pane, select **Page layouts**.</span></span>
1. <span data-ttu-id="e5efb-211">Selecteer de indeling voor de **pagina Nieuw wachtwoord**.</span><span class="sxs-lookup"><span data-stu-id="e5efb-211">Select the **New password page** layout.</span></span>
1. <span data-ttu-id="e5efb-212">Stel de optie **Aangepaste paginainhoud gebruiken** in op **Ja**.</span><span class="sxs-lookup"><span data-stu-id="e5efb-212">Set the **Use custom page content** option to **Yes**.</span></span>
1. <span data-ttu-id="e5efb-213">Voer in het veld **Aangepaste pagina-URI** de volledige URL voor het opnieuw instellen van het wachtwoord in.</span><span class="sxs-lookup"><span data-stu-id="e5efb-213">In the **Custom page URI** field, enter the full password reset URL.</span></span> <span data-ttu-id="e5efb-214">Neem het achtervoegsel **?preloadscripts=true** op.</span><span class="sxs-lookup"><span data-stu-id="e5efb-214">Include the **?preloadscripts=true** suffix.</span></span> <span data-ttu-id="e5efb-215">Voer bijvoorbeeld ``www.<my domain>.com/passwordreset?preloadscripts=true`` in.</span><span class="sxs-lookup"><span data-stu-id="e5efb-215">For example, enter ``www.<my domain>.com/passwordreset?preloadscripts=true``.</span></span>
1. <span data-ttu-id="e5efb-216">Selecteer in het veld **Versie van pagina-indeling (Preview)** **1.2.0**.</span><span class="sxs-lookup"><span data-stu-id="e5efb-216">In the **Page Layout Version (Preview)** field, select **1.2.0**.</span></span>
1. <span data-ttu-id="e5efb-217">Selecteer de indeling voor de **pagina Accountverificatie**.</span><span class="sxs-lookup"><span data-stu-id="e5efb-217">Select the **Account verification page** layout.</span></span>
1. <span data-ttu-id="e5efb-218">Stel de optie **Aangepaste paginainhoud gebruiken** in op **Ja**.</span><span class="sxs-lookup"><span data-stu-id="e5efb-218">Set the **Use custom page content** option to **Yes**.</span></span>
1. <span data-ttu-id="e5efb-219">Voer in het veld **Aangepaste pagina-URI** de volledige URL voor verificatie voor het opnieuw instellen van het wachtwoord in.</span><span class="sxs-lookup"><span data-stu-id="e5efb-219">In the **Custom page URI** field, enter the full password reset verification URL.</span></span> <span data-ttu-id="e5efb-220">Neem het achtervoegsel **?preloadscripts=true** op.</span><span class="sxs-lookup"><span data-stu-id="e5efb-220">Include the **?preloadscripts=true** suffix.</span></span> <span data-ttu-id="e5efb-221">Voer bijvoorbeeld ``www.<my domain>.com/passwordreset-verification?preloadscripts=true`` in.</span><span class="sxs-lookup"><span data-stu-id="e5efb-221">For example, enter ``www.<my domain>.com/passwordreset-verification?preloadscripts=true``.</span></span>
1. <span data-ttu-id="e5efb-222">Selecteer in het veld **Versie van pagina-indeling (Preview)** **1.2.0**.</span><span class="sxs-lookup"><span data-stu-id="e5efb-222">In the **Page Layout Version (Preview)** field, select **1.2.0**.</span></span>



## <a name="customize-default-text-strings-for-labels-and-descriptions"></a><span data-ttu-id="e5efb-223">Standaard tekstreeksen aanpassen voor labels en omschrijvingen</span><span class="sxs-lookup"><span data-stu-id="e5efb-223">Customize default text strings for labels and descriptions</span></span>

<span data-ttu-id="e5efb-224">In de modulebibliotheek worden aanmeldingsmodules vooraf ingevuld met standaard tekstreeksen voor de labels en omschrijvingen.</span><span class="sxs-lookup"><span data-stu-id="e5efb-224">In the module library, sign-in modules are prefilled with default text strings for the labels and descriptions.</span></span> <span data-ttu-id="e5efb-225">U kunt deze reeksen aanpassen in de Software Development Kit (SDK) door de waarden in het global.json-bestand voor de logboekmodule bij te werken.</span><span class="sxs-lookup"><span data-stu-id="e5efb-225">You can customize these strings in the software development kit (SDK) by updating the values in the global.json file for the sign in module.</span></span>

<span data-ttu-id="e5efb-226">De standaardtekst voor de koppeling voor vergeten wachtwoord is bijvoorbeeld **Vergeten wachtwoord?**.</span><span class="sxs-lookup"><span data-stu-id="e5efb-226">For example, the default text for the forgotten password link is **Forgotten password?**.</span></span> <span data-ttu-id="e5efb-227">Hieronder ziet u deze standaardtekst op de aanmeldingspagina.</span><span class="sxs-lookup"><span data-stu-id="e5efb-227">The following shows this default text on the sign-in page.</span></span>

![Standaardtekst van de koppeling voor vergeten wachtwoord op de aanmeldingspagina](./media/B2C_SignUp_ModuleFace.png)

<span data-ttu-id="e5efb-229">In het bestand global.json voor de aanmeldingsmodule van de modulebibliotheek kunt u de tekst echter wijzigen in **Wachtwoord vergeten?**, zoals u in de volgende afbeelding kunt zien.</span><span class="sxs-lookup"><span data-stu-id="e5efb-229">However, in the global.json file for the module library sign-in module, you can edit the text to **Forgot Password?**, as shown in the following illustration.</span></span>

![Bijgewerkte koppelingstekst in het bestand global.json van het aanmeldingsmodule](./media/B2C_CustomizingStringsForModule.png)

<span data-ttu-id="e5efb-231">Nadat u het bestand Global.json hebt bijgewerkt en uw wijzigingen hebt gepubliceerd, wordt de tekst van de nieuwe koppeling weergegeven in de aanmeldingsmodule in Commerce en op de live aanmeldingspagina.</span><span class="sxs-lookup"><span data-stu-id="e5efb-231">After you update the global.json file and publish your changes, the new link text appears in the sign-in module in both Commerce and on the live sign-in page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e5efb-232">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="e5efb-232">Additional resources</span></span>

[<span data-ttu-id="e5efb-233">Uw domeinnaam configureren</span><span class="sxs-lookup"><span data-stu-id="e5efb-233">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="e5efb-234">Een nieuwe e-commerce-tenant implementeren</span><span class="sxs-lookup"><span data-stu-id="e5efb-234">Deploy a new e-commerce tenant</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="e5efb-235">Een e-commerce-site maken</span><span class="sxs-lookup"><span data-stu-id="e5efb-235">Create an e-commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="e5efb-236">Een Dynamics 365 Commerce-site koppelen aan een online kanaal</span><span class="sxs-lookup"><span data-stu-id="e5efb-236">Associate a Dynamics 365 Commerce site with an online channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="e5efb-237">robots.txt-bestanden beheren</span><span class="sxs-lookup"><span data-stu-id="e5efb-237">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="e5efb-238">URL-omleidingen in bulk uploaden</span><span class="sxs-lookup"><span data-stu-id="e5efb-238">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

[<span data-ttu-id="e5efb-239">Een B2C-tenant instellen in Commerce</span><span class="sxs-lookup"><span data-stu-id="e5efb-239">Set up a B2C tenant in Commerce</span></span>](set-up-B2C-tenant.md)

[<span data-ttu-id="e5efb-240">Meerdere B2C-tenants configureren in een Commerce-omgeving</span><span class="sxs-lookup"><span data-stu-id="e5efb-240">Configure multiple B2C tenants in a Commerce environment</span></span>](configure-multi-B2C-tenants.md)

[<span data-ttu-id="e5efb-241">Ondersteuning voor een CDN (contentleveringsnetwerk) toevoegen</span><span class="sxs-lookup"><span data-stu-id="e5efb-241">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="e5efb-242">Detectie van winkels op basis van de locatie inschakelen</span><span class="sxs-lookup"><span data-stu-id="e5efb-242">Enable location-based store detection</span></span>](enable-store-detection.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
