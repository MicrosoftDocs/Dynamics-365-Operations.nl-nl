---
title: Een B2C-tenant instellen in Commerce
description: In dit onderwerp wordt beschreven hoe u uw B2C-tenants (business-to-consumers) in Azure Active Directory (Azure AD) instelt voor de verificatie van sitegebruikers in Dynamics 365 Commerce.
author: BrianShook
manager: annbe
ms.date: 03/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: ''
ms.search.region: Global
ms.search.industry: retail
ms.author: BriShoo
ms.search.validFrom: 2020-02-13
ms.dyn365.ops.version: ''
ms.openlocfilehash: a5fca37fb89c723273ef753b102092e2cfb26563
ms.sourcegitcommit: 236672932ffd0a758012ebb7b2df9bc51249c126
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/03/2020
ms.locfileid: "3096497"
---
# <a name="set-up-a-b2c-tenant-in-commerce"></a><span data-ttu-id="cd31a-103">Een B2C-tenant instellen in Commerce</span><span class="sxs-lookup"><span data-stu-id="cd31a-103">Set up a B2C tenant in Commerce</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="cd31a-104">In dit onderwerp wordt beschreven hoe u uw B2C-tenants (business-to-consumers) in Azure Active Directory (Azure AD) instelt voor de verificatie van sitegebruikers in Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="cd31a-104">This topic describes how to set up your Azure Active Directory (Azure AD) business-to-consumer (B2C) tenants for user site authentication in Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="cd31a-105">Overzicht</span><span class="sxs-lookup"><span data-stu-id="cd31a-105">Overview</span></span>

<span data-ttu-id="cd31a-106">Dynamics 365 Commerce gebruikt Azure AD B2C om gebruikersreferenties en verificatiestromen te ondersteunen.</span><span class="sxs-lookup"><span data-stu-id="cd31a-106">Dynamics 365 Commerce uses Azure AD B2C to support user credential and authentication flows.</span></span> <span data-ttu-id="cd31a-107">Een gebruiker kan zich registreren en aanmelden, en vervolgens zijn/haar wachtwoord opnieuw instellen via deze stromen.</span><span class="sxs-lookup"><span data-stu-id="cd31a-107">A user can sign up, sign in, and reset their password through these flows.</span></span> <span data-ttu-id="cd31a-108">Azure AD B2C slaat gevoelige gebruikersverificatiegegevens op, zoals de gebruikersnaam en het wachtwoord.</span><span class="sxs-lookup"><span data-stu-id="cd31a-108">Azure AD B2C stores sensitive user authentication information, such as username and password.</span></span> <span data-ttu-id="cd31a-109">In de gebruikersrecord in de B2C-tenant wordt een record voor een lokale B2C-account of een record voor een B2C-provider van sociale identiteiten opgeslagen.</span><span class="sxs-lookup"><span data-stu-id="cd31a-109">The user record in the B2C tenant will store either a B2C local account record or a B2C social identity provider record.</span></span> <span data-ttu-id="cd31a-110">Deze B2C-records verwijzen weer naar de klantrecord in de Commerce-omgeving.</span><span class="sxs-lookup"><span data-stu-id="cd31a-110">These B2C records will link back to the customer record in the Commerce environment.</span></span>

## <a name="create-or-link-to-an-existing-aad-b2c-tenant-in-the-azure-portal"></a><span data-ttu-id="cd31a-111">Een AAD B2C-tenant maken of een koppeling met een bestaande AAD B2C-tenant instellen in de Azure-portal</span><span class="sxs-lookup"><span data-stu-id="cd31a-111">Create or link to an existing AAD B2C tenant in the Azure portal</span></span>

1. <span data-ttu-id="cd31a-112">Meld u aan bij de [Azure-portal](https://portal.azure.com/).</span><span class="sxs-lookup"><span data-stu-id="cd31a-112">Sign in to the [Azure portal](https://portal.azure.com/).</span></span>
1. <span data-ttu-id="cd31a-113">Selecteer **Een resource maken** in het menu van Azure Portal.</span><span class="sxs-lookup"><span data-stu-id="cd31a-113">From the Azure portal menu, select **Create a resource**.</span></span> <span data-ttu-id="cd31a-114">Gebruik het abonnement en de map die met uw Commerce-omgeving worden verbonden.</span><span class="sxs-lookup"><span data-stu-id="cd31a-114">Be sure to use the subscription and directory that will be connected with your Commerce environment.</span></span>

    ![Een resource maken in Azure Portal](./media/B2CImage_1.png)

1. <span data-ttu-id="cd31a-116">Ga naar **Identiteit \> Azure Active Directory B2C**.</span><span class="sxs-lookup"><span data-stu-id="cd31a-116">Go to **Identity \> Azure Active Directory B2C**.</span></span>
1. <span data-ttu-id="cd31a-117">Op de pagina **Nieuwe B2C-tenant maken of koppelen aan bestaande tenant maken** gebruikt u een van de volgende opties die het beste aansluit bij de behoeften van uw bedrijf:</span><span class="sxs-lookup"><span data-stu-id="cd31a-117">Once on the **Create New B2C Tenant or Link to existing Tenant** page, use one of the options below that best suits your company's needs:</span></span>

    - <span data-ttu-id="cd31a-118">**Een nieuwe Azure AD B2C-tenant maken**: gebruik deze optie om een nieuwe AAD B2C-tenant te maken.</span><span class="sxs-lookup"><span data-stu-id="cd31a-118">**Create a new Azure AD B2C Tenant**: Use this option to create a new AAD B2C tenant.</span></span>
        1. <span data-ttu-id="cd31a-119">Selecteer **Een nieuwe Azure AD B2C-tenant maken**.</span><span class="sxs-lookup"><span data-stu-id="cd31a-119">Select **Create a new Azure AD B2C Tenant**.</span></span>
        1. <span data-ttu-id="cd31a-120">Voer onder **Naam van organisatie** de naam van de organisatie in.</span><span class="sxs-lookup"><span data-stu-id="cd31a-120">Under **Organization name**, enter the organization name.</span></span>
        1. <span data-ttu-id="cd31a-121">Voer bij **Oorspronkelijke domeinnaam** de oorspronkelijke domeinnaam in.</span><span class="sxs-lookup"><span data-stu-id="cd31a-121">Under **Initial domain name**, enter the initial domain name.</span></span>
        1. <span data-ttu-id="cd31a-122">Selecteer het land of de regio bij **Land of regio**.</span><span class="sxs-lookup"><span data-stu-id="cd31a-122">For **Country or region**, select the country or region.</span></span>
        1. <span data-ttu-id="cd31a-123">Selecteer **Maken** om de tenant te maken.</span><span class="sxs-lookup"><span data-stu-id="cd31a-123">Select **Create** to create the tenant.</span></span>

     ![Een nieuwe Azure AD-tenant maken](./media/B2CImage_2.png)

     - <span data-ttu-id="cd31a-125">**Een bestaande Azure AD B2C-tenant koppelen aan mijn Azure-abonnement**: gebruik deze optie als u al een Azure AD B2C-tenant hebt waarmee u een koppeling tot stand wilt brengen.</span><span class="sxs-lookup"><span data-stu-id="cd31a-125">**Link an existing Azure AD B2C Tenant to my Azure subscription**: Use this option if you already have an Azure AD B2C tenant you want to link to.</span></span>
        1. <span data-ttu-id="cd31a-126">Selecteer **Een bestaande Azure AD B2C-tenant koppelen aan mijn Azure-abonnement**.</span><span class="sxs-lookup"><span data-stu-id="cd31a-126">Select **Link an existing Azure AD B2C Tenant to my Azure subscription**.</span></span>
        1. <span data-ttu-id="cd31a-127">Selecteer bij **Azure AD B2C-tenant** de geschikte B2C-tenant.</span><span class="sxs-lookup"><span data-stu-id="cd31a-127">For **Azure AD B2C Tenant**, select the appropriate B2C tenant.</span></span> <span data-ttu-id="cd31a-128">Als het bericht Geen B2C-tenants gevonden die in aanmerking komen wordt weergegeven in het selectievak, beschikt u niet over een bestaande B2C-tenant die in aanmerking komt en moet u een nieuwe maken.</span><span class="sxs-lookup"><span data-stu-id="cd31a-128">If the message "No eligible B2C Tenants found" appears in the selection box, you do not have an existing eligible B2C tenant and will need to create a new one.</span></span>
        1. <span data-ttu-id="cd31a-129">Selecteer **Nieuwe maken** voor **Resourcegroep**.</span><span class="sxs-lookup"><span data-stu-id="cd31a-129">For **Resource group**, select **Create new**.</span></span> <span data-ttu-id="cd31a-130">Voer een **naam** in voor de resourcegroep die de tenant moet bevatten, selecteer **de locatie de resourcegroep** en selecteer vervolgens **Maken**.</span><span class="sxs-lookup"><span data-stu-id="cd31a-130">Enter a **Name** for the resource group that will contain the tenant, select the **Resource group location**, and then select **Create**.</span></span>

    ![Een bestaande Azure AD B2C-tenant koppelen aan een Azure-abonnement](./media/B2CImage_3.png)

1. <span data-ttu-id="cd31a-132">Zodra de nieuwe Azure AD B2C-map is gemaakt (dit kan even duren), wordt een koppeling naar de nieuwe map weergegeven op het dashboard.</span><span class="sxs-lookup"><span data-stu-id="cd31a-132">Once the new Azure AD B2C directory is created (this may take a few moments), a link to the new directory will appear on the dashboard.</span></span> <span data-ttu-id="cd31a-133">Met deze koppeling wordt u naar de pagina Welkom bij Azure Active Directory B2C geleid.</span><span class="sxs-lookup"><span data-stu-id="cd31a-133">This link will direct you to the "Welcome to Azure Active Directory B2C" page.</span></span>

    ![Koppeling naar nieuwe AAD-map](./media/B2CImage_4.png)

> [!NOTE]
> <span data-ttu-id="cd31a-135">Als u meerdere abonnementen hebt in uw Azure-account of als u de B2C-tenant hebt ingesteld zonder deze aan een actief abonnement te koppelen, kunt u via een banner **Problemen oplossen** de tenant aan een abonnement koppelen.</span><span class="sxs-lookup"><span data-stu-id="cd31a-135">If you have multiple subscriptions within your Azure account or have set up the B2C tenant without linking to an active subscription, a **Troubleshoot** banner will direct you to link the tenant to a subscription.</span></span> <span data-ttu-id="cd31a-136">Selecteer het probleemoplossingsbericht en volg de instructies om het probleem met het abonnement op te lossen.</span><span class="sxs-lookup"><span data-stu-id="cd31a-136">Select the troubleshooting message and follow the instructions to resolve the subscription issue.</span></span>

<span data-ttu-id="cd31a-137">In de volgende afbeelding ziet u een voorbeeld van een Azure AD B2C-banner **Problemen oplossen**.</span><span class="sxs-lookup"><span data-stu-id="cd31a-137">The following image shows an example of an Azure AD B2C **Troubleshoot** banner.</span></span>

![Waarschuwing met de melding dat voor de map geen actief abonnement bestaat](./media/B2CImage_5.png)

## <a name="create-the-b2c-application"></a><span data-ttu-id="cd31a-139">De B2C-toepassing maken</span><span class="sxs-lookup"><span data-stu-id="cd31a-139">Create the B2C application</span></span>

<span data-ttu-id="cd31a-140">Nadat de B2C-tenant is gemaakt, maakt u een B2C-toepassing in de tenant om te communiceren met de Commerce-acties.</span><span class="sxs-lookup"><span data-stu-id="cd31a-140">Once the B2C tenant has been created, you will create a B2C application within the tenant to interact with the Commerce actions.</span></span>

<span data-ttu-id="cd31a-141">Ga als volgt te werk om de B2C-toepassing te maken:</span><span class="sxs-lookup"><span data-stu-id="cd31a-141">To create the B2C application, follow these steps.</span></span>

1. <span data-ttu-id="cd31a-142">Selecteer **Toepassingen** in de Azure-portal en selecteer vervolgens **Toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="cd31a-142">In the Azure portal, select **Applications** and then select **Add**.</span></span>
1. <span data-ttu-id="cd31a-143">Voer onder **Naam** de naam in van de gewenste AAD B2C-toepassing.</span><span class="sxs-lookup"><span data-stu-id="cd31a-143">Under **Name**, enter the name of the desired AAD B2C application.</span></span>
1. <span data-ttu-id="cd31a-144">Selecteer onder **Web-app/web-API** voor **Web-app/web-API opnemen** de optie **Ja**.</span><span class="sxs-lookup"><span data-stu-id="cd31a-144">Under **Web App/Web API**, for **Include web app / web API**, select **Yes**.</span></span>
1. <span data-ttu-id="cd31a-145">Selecteer **Ja** (de standaardwaarde) voor **Impliciete stroom toestaan**.</span><span class="sxs-lookup"><span data-stu-id="cd31a-145">For **Allow implicit flow**, select **Yes** (the default value).</span></span>
1. <span data-ttu-id="cd31a-146">Voer onder **Antwoord-URL** uw specifieke antwoord-URL's in.</span><span class="sxs-lookup"><span data-stu-id="cd31a-146">Under **Reply URL**, enter your dedicated reply URLs.</span></span> <span data-ttu-id="cd31a-147">Zie [Antwoord-URL's](#reply-urls) hieronder voor informatie over antwoord-URL's en hoe u deze hier kunt indelen.</span><span class="sxs-lookup"><span data-stu-id="cd31a-147">See [Reply URLs](#reply-urls) below for information on reply URLs and how to format them here.</span></span>
1. <span data-ttu-id="cd31a-148">Selecteer **Nee** (de standaard waarde) bij **Systeemeigen client opnemen**.</span><span class="sxs-lookup"><span data-stu-id="cd31a-148">For **Include native client**, select **No** (the default value).</span></span>
1. <span data-ttu-id="cd31a-149">Selecteer **Maken**.</span><span class="sxs-lookup"><span data-stu-id="cd31a-149">Select **Create**.</span></span>

### <a name="reply-urls"></a><span data-ttu-id="cd31a-150">Antwoord-URL's</span><span class="sxs-lookup"><span data-stu-id="cd31a-150">Reply URLs</span></span>

<span data-ttu-id="cd31a-151">Antwoord-URL's zijn belangrijk omdat ze een witte lijst van de retourdomeinen toestaan wanneer uw site Azure AD B2C aanroept om een gebruiker te verifiëren.</span><span class="sxs-lookup"><span data-stu-id="cd31a-151">Reply URLs are important as they allow a whitelist of the return domains when your site calls Azure AD B2C to authenticate a user.</span></span> <span data-ttu-id="cd31a-152">Hierdoor kan de geverifieerde gebruiker worden geretourneerd naar het domein waarbij ze zich aanmelden (uw sitedomein).</span><span class="sxs-lookup"><span data-stu-id="cd31a-152">This allows the return of the authenticated user back to the domain from which they are signing into (your site domain).</span></span> 

<span data-ttu-id="cd31a-153">In het **Antwoord-URL** in het scherm **Azure AD B2C -Toepassingen \> Nieuwe toepassing** moet u afzonderlijke regels toevoegen voor uw sitedomein en (zodra uw omgeving is ingericht) de door Commerce gegenereerde URL.</span><span class="sxs-lookup"><span data-stu-id="cd31a-153">In the **Reply URL** box on the **Azure AD B2c - Applications \> New application** screen, you need to add separate lines for both your site domain and (once your environment is provisioned) the Commerce-generated URL.</span></span> <span data-ttu-id="cd31a-154">Deze URL's moeten altijd een geldige URL-indeling gebruiken en mogen alleen basis-URL's (geen navolgende slashes of paden) zijn.</span><span class="sxs-lookup"><span data-stu-id="cd31a-154">These URLs must always use a valid URL format and must be base URLs only (no trailing forward slashes or paths).</span></span> <span data-ttu-id="cd31a-155">De tekenreeks ``/_msdyn365/authresp`` moet vervolgens worden toegevoegd aan de basis-URL's, zoals in de volgende voorbeelden.</span><span class="sxs-lookup"><span data-stu-id="cd31a-155">The string ``/_msdyn365/authresp`` then needs to be appended to the base URLs, as in the following examples.</span></span>

- ``https://fabrikam.com/_msdyn365/authresp``
- ``https://fabrikam-prod.commerce.dynamics.com/_msdyn365/authresp``

## <a name="create-user-flow-policies"></a><span data-ttu-id="cd31a-156">Beleid voor gebruikersstromen maken</span><span class="sxs-lookup"><span data-stu-id="cd31a-156">Create user flow policies</span></span>

<span data-ttu-id="cd31a-157">Gebruikersstromen zijn de beleidsregels die Azure AD B2C gebruikt om veilige gebruikerservaringen voor registeren, aanmelden, profielbewerkingen en vergeten wachtwoorden te bieden.</span><span class="sxs-lookup"><span data-stu-id="cd31a-157">User flows are the policies Azure AD B2C uses to provide secure sign in, sign up, edit profile, and forget password user experiences.</span></span> <span data-ttu-id="cd31a-158">Dynamics 365 Commerce gebruikt deze stromen om de beleidsacties uit te voeren om te communiceren met de Azure AD B2C-tenant.</span><span class="sxs-lookup"><span data-stu-id="cd31a-158">Dynamics 365 Commerce uses these flows to perform the policy actions to interact with the Azure AD B2C tenant.</span></span> <span data-ttu-id="cd31a-159">Wanneer een gebruiker met dit beleid communiceert, wordt deze omgeleid naar de Azure AD B2C-tenant om de acties uit te voeren.</span><span class="sxs-lookup"><span data-stu-id="cd31a-159">When a user interacts with these policies, they are redirected to the Azure AD B2C tenant to perform the actions.</span></span>

<span data-ttu-id="cd31a-160">Azure AD B2C biedt drie algemene typen gebruikersstromen:</span><span class="sxs-lookup"><span data-stu-id="cd31a-160">Azure AD B2C provides three basic user flow types:</span></span>
- <span data-ttu-id="cd31a-161">Registreren en aanmelden</span><span class="sxs-lookup"><span data-stu-id="cd31a-161">Sign up and sign in</span></span>
- <span data-ttu-id="cd31a-162">Profiel bewerken</span><span class="sxs-lookup"><span data-stu-id="cd31a-162">Profile editing</span></span>
- <span data-ttu-id="cd31a-163">Wachtwoord opnieuw instellen</span><span class="sxs-lookup"><span data-stu-id="cd31a-163">Password reset</span></span>

<span data-ttu-id="cd31a-164">U kunt ervoor kiezen om de standaardgebruikersstromen van Azure AD te gebruiken. Vervolgens wordt er een pagina weergegeven die wordt gehost door AAD B2C.</span><span class="sxs-lookup"><span data-stu-id="cd31a-164">You can choose to use the default user flows provided by Azure AD, which will display a page hosted by AAD B2C.</span></span> <span data-ttu-id="cd31a-165">U kunt ook een HTML-pagina maken om het uiterlijk van deze gebruikersstroomervaringen te bepalen.</span><span class="sxs-lookup"><span data-stu-id="cd31a-165">Alternately, you can create an HTML page to control the look and feel of these user flow experiences.</span></span> 

<span data-ttu-id="cd31a-166">Zie [Aangepaste pagina's voor gebruikersaanmeldingen instellen](custom-pages-user-logins.md) als u de gebruikersbeleidspagina's voor Dynamics 365 Commerce wilt aanpassen.</span><span class="sxs-lookup"><span data-stu-id="cd31a-166">To customize the user policy pages for Dynamics 365 Commerce, see [Set up custom pages for user logins](custom-pages-user-logins.md).</span></span> <span data-ttu-id="cd31a-167">Zie voor aanvullende informatie [De interface met gebruikerservaringen in Azure Active Directory B2C aanpassen](https://docs.microsoft.com/azure/active-directory-b2c/tutorial-customize-ui).</span><span class="sxs-lookup"><span data-stu-id="cd31a-167">For additional information, see [Customize the interface of user experiences in Azure Active Directory B2C](https://docs.microsoft.com/azure/active-directory-b2c/tutorial-customize-ui).</span></span>

### <a name="create-a-sign-up-and-sign-in-user-flow-policy"></a><span data-ttu-id="cd31a-168">Een gebruikersstroombeleid voor registreren en aanmelden maken</span><span class="sxs-lookup"><span data-stu-id="cd31a-168">Create a sign up and sign in user flow policy</span></span>

<span data-ttu-id="cd31a-169">Voer de volgende stappen uit om een gebruikersstroombeleid voor registreren en aanmelden te maken.</span><span class="sxs-lookup"><span data-stu-id="cd31a-169">To create a sign up and sign in user flow policy, follow these steps.</span></span>

1. <span data-ttu-id="cd31a-170">Selecteer **Gebruikersstromen (beleid)** in het linkernavigatievenster van de Azure-portal.</span><span class="sxs-lookup"><span data-stu-id="cd31a-170">In the Azure portal, select **User flows (policies)** in the left navigation pane.</span></span>
1. <span data-ttu-id="cd31a-171">Selecteer op de pagina **Azure AD B2C - Gebruikersstromen (beleid)** de optie **Nieuwe gebruikersstroom**.</span><span class="sxs-lookup"><span data-stu-id="cd31a-171">On the **Azure AD B2C – User flows (policies)** page, select **New User Flow**.</span></span>
1. <span data-ttu-id="cd31a-172">Selecteer **Registreren en aanmelden** op het tabblad **Aanbevolen**.</span><span class="sxs-lookup"><span data-stu-id="cd31a-172">On the **Recommended** tab, select **Sign up and sign in**.</span></span>
1. <span data-ttu-id="cd31a-173">Voer een beleidsnaam in onder **Naam**.</span><span class="sxs-lookup"><span data-stu-id="cd31a-173">Under **Name**, enter a policy name.</span></span> <span data-ttu-id="cd31a-174">Deze naam wordt vervolgens weer gegeven met een voorvoegsel dat wordt toegewezen door de portal (bijvoorbeeld B2C_1_).</span><span class="sxs-lookup"><span data-stu-id="cd31a-174">This name will display afterwards with a prefix the portal assigns (for example, "B2C_1_").</span></span>
1. <span data-ttu-id="cd31a-175">Schakel onder **Identiteitsproviders** het desbetreffende selectievakje in.</span><span class="sxs-lookup"><span data-stu-id="cd31a-175">Under **Identity providers**, select the appropriate check box.</span></span>
1. <span data-ttu-id="cd31a-176">Selecteer de juiste keuze voor uw bedrijf onder **Meervoudige verificatie**.</span><span class="sxs-lookup"><span data-stu-id="cd31a-176">Under **Multifactor Authentication**, select the appropriate choice for your company.</span></span> 
1. <span data-ttu-id="cd31a-177">Selecteer onder **Gebruikerskenmerken en claims** opties om kenmerken te verzamelen of claims naar wens te retourneren.</span><span class="sxs-lookup"><span data-stu-id="cd31a-177">Under **User attributes and claims**, select options to collect attributes or return claims as appropriate.</span></span> <span data-ttu-id="cd31a-178">Voor Commerce zijn de volgende standaardopties vereist:</span><span class="sxs-lookup"><span data-stu-id="cd31a-178">Commerce requires the following default options:</span></span>

    | <span data-ttu-id="cd31a-179">**Kenmerk verzamelen**</span><span class="sxs-lookup"><span data-stu-id="cd31a-179">**Collect  attribute**</span></span> | <span data-ttu-id="cd31a-180">**Claim retourneren**</span><span class="sxs-lookup"><span data-stu-id="cd31a-180">**Return  claim**</span></span> |
    | ---------------------- | ----------------- |
    |                        | <span data-ttu-id="cd31a-181">E-mailadressen</span><span class="sxs-lookup"><span data-stu-id="cd31a-181">Email Addresses</span></span>   |
    | <span data-ttu-id="cd31a-182">Voornaam</span><span class="sxs-lookup"><span data-stu-id="cd31a-182">Given Name</span></span>             | <span data-ttu-id="cd31a-183">Voornaam</span><span class="sxs-lookup"><span data-stu-id="cd31a-183">Given Name</span></span>        |
    |                        | <span data-ttu-id="cd31a-184">Identiteitsprovider</span><span class="sxs-lookup"><span data-stu-id="cd31a-184">Identity Provider</span></span> |
    | <span data-ttu-id="cd31a-185">Achternaam</span><span class="sxs-lookup"><span data-stu-id="cd31a-185">Surname</span></span>                | <span data-ttu-id="cd31a-186">Achternaam</span><span class="sxs-lookup"><span data-stu-id="cd31a-186">Surname</span></span>           |
    |                        | <span data-ttu-id="cd31a-187">De object-id van de gebruiker</span><span class="sxs-lookup"><span data-stu-id="cd31a-187">User’s Object ID</span></span>  |

1. <span data-ttu-id="cd31a-188">Selecteer **Maken**.</span><span class="sxs-lookup"><span data-stu-id="cd31a-188">Select **Create**.</span></span>

<span data-ttu-id="cd31a-189">De volgende afbeelding is een voorbeeld van de gebruikersstroom voor registreren en aanmelden voor Azure AD B2C.</span><span class="sxs-lookup"><span data-stu-id="cd31a-189">The following image is an example of the Azure AD B2C sign up and sign in user flow.</span></span>

![Beleidsinstellingen voor registreren en aanmelden](./media/B2CImage_11.png)

<span data-ttu-id="cd31a-191">In de volgende afbeelding ziet de optie **Gebruikersstroom uitvoeren** in de in de gebruikers stroom voor registreren en aanmelden in Azure AD B2C.</span><span class="sxs-lookup"><span data-stu-id="cd31a-191">The following image shows the **Run user flow** option in the Azure AD B2C sign up and sign in user flow.</span></span>

![De optie Gebruikersstroom uitvoeren in de beleidsstroom](./media/B2CImage_23.png)
   
### <a name="create-a-profile-editing-user-flow-policy"></a><span data-ttu-id="cd31a-193">Een beleid voor de gebruikersstroom voor het bewerken van profielen maken</span><span class="sxs-lookup"><span data-stu-id="cd31a-193">Create a profile editing user flow policy</span></span>

<span data-ttu-id="cd31a-194">Voer de volgende stappen uit om een gebruikersstroombeleid voor het bewerken van profielen te maken.</span><span class="sxs-lookup"><span data-stu-id="cd31a-194">To create a profile editing user flow policy, follow these steps.</span></span>

1. <span data-ttu-id="cd31a-195">Selecteer **Gebruikersstromen (beleid)** in het linkernavigatievenster van de Azure-portal.</span><span class="sxs-lookup"><span data-stu-id="cd31a-195">In the Azure portal, select **User flows (policies)** in the left navigation pane.</span></span>
1. <span data-ttu-id="cd31a-196">Selecteer op de pagina **Azure AD B2C - Gebruikersstromen (beleid)** de optie **Nieuwe gebruikersstroom**.</span><span class="sxs-lookup"><span data-stu-id="cd31a-196">On the **Azure AD B2C – User flows (policies)** page, select **New User Flow**.</span></span>
1. <span data-ttu-id="cd31a-197">Selecteer op het tabblad **Aanbevolen** de optie **Profiel bewerken**.</span><span class="sxs-lookup"><span data-stu-id="cd31a-197">On the **Recommended** tab, select **Profile editing**.</span></span>
1. <span data-ttu-id="cd31a-198">Voer onder **Naam** de gebruikersstroom voor het bewerken van profielen in.</span><span class="sxs-lookup"><span data-stu-id="cd31a-198">Under **Name**, enter the profile editing user flow.</span></span> <span data-ttu-id="cd31a-199">Deze naam wordt vervolgens weer gegeven met een voorvoegsel dat wordt toegewezen door de portal (bijvoorbeeld B2C_1_).</span><span class="sxs-lookup"><span data-stu-id="cd31a-199">This name will display afterwards with a prefix the portal assigns (for example, "B2C_1_").</span></span>
1. <span data-ttu-id="cd31a-200">Selecteer onder **Identiteitsproviders** de optie **Aanmelden met een lokaal account**.</span><span class="sxs-lookup"><span data-stu-id="cd31a-200">Under **Identity providers**, select **Local Account SignIn**.</span></span>
1. <span data-ttu-id="cd31a-201">Schakel onder **Gebruikerskenmerken** de volgende selectievakjes in:</span><span class="sxs-lookup"><span data-stu-id="cd31a-201">Under **User attributes**, select the following check boxes:</span></span>
    - <span data-ttu-id="cd31a-202">**E-mailadressen** (alleen **Claim retourneren**)</span><span class="sxs-lookup"><span data-stu-id="cd31a-202">**Email Addresses** (**Return claim** only)</span></span>
    - <span data-ttu-id="cd31a-203">**Voornaam** (**Kenmerk verzamelen** en **Claim retourneren**)</span><span class="sxs-lookup"><span data-stu-id="cd31a-203">**Given Name** (**Collect attribute** and **Return claim**)</span></span>
    - <span data-ttu-id="cd31a-204">**Identiteitsprovider** (alleen **Claim retourneren**)</span><span class="sxs-lookup"><span data-stu-id="cd31a-204">**Identity Provider** (**Return claim** only)</span></span>
    - <span data-ttu-id="cd31a-205">**Achternaam** (**Kenmerk verzamelen** en **Claim retourneren**)</span><span class="sxs-lookup"><span data-stu-id="cd31a-205">**Surname** (**Collect attribute** and **Return claim**)</span></span>
    - <span data-ttu-id="cd31a-206">**De object-id van de gebruiker** (alleen **Claim retourneren**)</span><span class="sxs-lookup"><span data-stu-id="cd31a-206">**User's Object ID** (**Return claim** only)</span></span>
1. <span data-ttu-id="cd31a-207">Selecteer **Maken**.</span><span class="sxs-lookup"><span data-stu-id="cd31a-207">Select **Create**.</span></span>

<span data-ttu-id="cd31a-208">In de volgende afbeelding ziet u een voorbeeld van de gebruikersstroom voor het bewerken van profielen in Azure AD B2C.</span><span class="sxs-lookup"><span data-stu-id="cd31a-208">The following image shows an example of the Azure AD B2C profile editing user flow.</span></span>

![De gebruikersstroom voor het bewerken van profielen maken](./media/B2CImage_12.png)

### <a name="create-a-password-reset-user-flow-policy"></a><span data-ttu-id="cd31a-210">Een beleid voor de gebruikersstroom voor het opnieuw instellen van wachtwoorden maken</span><span class="sxs-lookup"><span data-stu-id="cd31a-210">Create a password reset user flow policy</span></span>

<span data-ttu-id="cd31a-211">Voer de volgende stappen uit om een gebruikersstroombeleid voor het opnieuw instellen van wachtwoorden te maken.</span><span class="sxs-lookup"><span data-stu-id="cd31a-211">To create a password reset user flow policy, follow these steps.</span></span>

1. <span data-ttu-id="cd31a-212">Selecteer **Gebruikersstromen (beleid)** in het linkernavigatievenster van de Azure-portal.</span><span class="sxs-lookup"><span data-stu-id="cd31a-212">In the Azure portal, select **User flows (policies)** in the left navigation pane.</span></span>
1. <span data-ttu-id="cd31a-213">Selecteer op de pagina **Azure AD B2C - Gebruikersstromen (beleid)** de optie **Nieuwe gebruikersstroom**.</span><span class="sxs-lookup"><span data-stu-id="cd31a-213">On the **Azure AD B2C – User flows (policies)** page, select **New User Flow**.</span></span>
1. <span data-ttu-id="cd31a-214">Selecteer op het tabblad **Aanbevolen** de optie **Wachtwoord opnieuw instellen**.</span><span class="sxs-lookup"><span data-stu-id="cd31a-214">On the **Recommended** tab, select **Password Reset**.</span></span>
1. <span data-ttu-id="cd31a-215">Voer onder **Naam** een naam in voor de gebruikersstroom voor het opnieuw instellen van wachtwoorden.</span><span class="sxs-lookup"><span data-stu-id="cd31a-215">Under **Name**, enter a name for the password reset user flow.</span></span>
1. <span data-ttu-id="cd31a-216">Selecteer onder **Identiteitsproviders** de optie **Wachtwoord via e-mailadres opnieuw instellen**.</span><span class="sxs-lookup"><span data-stu-id="cd31a-216">Under **Identity providers**, select **Reset password using email address**.</span></span>
1. <span data-ttu-id="cd31a-217">Selecteer **Maken**.</span><span class="sxs-lookup"><span data-stu-id="cd31a-217">Select **Create**.</span></span>
1. <span data-ttu-id="cd31a-218">Schakel onder **Toepassingsclaims** de volgende selectievakjes in:</span><span class="sxs-lookup"><span data-stu-id="cd31a-218">Under **Application claims**, select the following check boxes:</span></span>
    - <span data-ttu-id="cd31a-219">**E-mailadres**</span><span class="sxs-lookup"><span data-stu-id="cd31a-219">**Email**</span></span>
    - <span data-ttu-id="cd31a-220">**Adressen**</span><span class="sxs-lookup"><span data-stu-id="cd31a-220">**Addresses**</span></span>
    - <span data-ttu-id="cd31a-221">**Voornaam**</span><span class="sxs-lookup"><span data-stu-id="cd31a-221">**Given Name**</span></span>
    - <span data-ttu-id="cd31a-222">**Achternaam**</span><span class="sxs-lookup"><span data-stu-id="cd31a-222">**Surname**</span></span>
    - <span data-ttu-id="cd31a-223">**De object-id van de gebruiker**</span><span class="sxs-lookup"><span data-stu-id="cd31a-223">**User's Object ID**</span></span>
1. <span data-ttu-id="cd31a-224">Selecteer **Maken**.</span><span class="sxs-lookup"><span data-stu-id="cd31a-224">Select **Create**.</span></span>

<span data-ttu-id="cd31a-225">De volgende afbeelding geeft aan waar het **wachtwoord via het e-mailadres opnieuw moet worden ingesteld** in de gebruikersstroom voor het opnieuw instellen van wachtwoorden in Azure AD B2C.</span><span class="sxs-lookup"><span data-stu-id="cd31a-225">The following image shows where to set **Reset Password using mail address** in the Azure AD B2C password reset user flow.</span></span>

![Wachtwoord opnieuw instellen via e-mailadres instellen in het beleid Wachtwoord opnieuw instellen](./media/B2CImage_13.png)

## <a name="add-social-identity-providers-optional"></a><span data-ttu-id="cd31a-227">Providers van sociale identiteiten toevoegen (optioneel)</span><span class="sxs-lookup"><span data-stu-id="cd31a-227">Add social identity providers (Optional)</span></span>

<span data-ttu-id="cd31a-228">Providers van sociale identiteiten stellen gebruikers in staat hun sociale accounts te gebruiken voor verificatie.</span><span class="sxs-lookup"><span data-stu-id="cd31a-228">Social identity providers allow users to use their social accounts for authentication.</span></span> <span data-ttu-id="cd31a-229">Het toevoegen van verificatie via providers van sociale identiteiten is optioneel in Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="cd31a-229">Adding social identity provider authentication is optional in Dynamics 365 Commerce.</span></span> 

<span data-ttu-id="cd31a-230">Als geen verificatie via de provider van sociale identiteiten wordt toegevoegd, zijn de standaardprofielen voor Azure AD B2C de hoofdprofielen voor uw gebruikers.</span><span class="sxs-lookup"><span data-stu-id="cd31a-230">If social identity provider authentication is not added, the default Azure AD B2C profiles will be the main profiles for your user base.</span></span> <span data-ttu-id="cd31a-231">Gebruikers selecteren hun eigen gebruikersnaam (hun gewenste e-mailadres) en stellen een wachtwoord in.</span><span class="sxs-lookup"><span data-stu-id="cd31a-231">Users will select their own username (their preferred email address) and set a password.</span></span> <span data-ttu-id="cd31a-232">Azure AD B2C verifieert gebruikers rechtstreeks.</span><span class="sxs-lookup"><span data-stu-id="cd31a-232">Azure AD B2C will authenticate users directly.</span></span> 

<span data-ttu-id="cd31a-233">Als verificatie via de provider van sociale identiteiten wordt toegevoegd en een gebruiker een van de aangeboden providers van sociale identiteiten kiest, wordt er nog steeds een entiteit gemaakt in de Azure AD B2C-tenant.</span><span class="sxs-lookup"><span data-stu-id="cd31a-233">If social identity provider authentication is added and a user chooses one of the social identity providers offered, an entity is still created in the Azure AD B2C tenant.</span></span> <span data-ttu-id="cd31a-234">Azure AD B2C verifieert vervolgens de referenties van de gebruiker met de provider van sociale identiteiten.</span><span class="sxs-lookup"><span data-stu-id="cd31a-234">Azure AD B2C will then authenticate the user's credentials with the social identity provider.</span></span>

> [!NOTE]
> <span data-ttu-id="cd31a-235">Er wordt een record van de aanmelding via de identiteitsprovider gemaakt in de B2C-Tenant, maar in een andere indeling dan lokale accounts, aangezien de externe provider van de sociale identiteiten wordt aangeroepen voor verificatie.</span><span class="sxs-lookup"><span data-stu-id="cd31a-235">The identity provider sign in creates a record in the B2C tenant, but in a different format than local accounts since it will call the external social identity provider reference for authentication.</span></span> <span data-ttu-id="cd31a-236">De gebruiker kan hetzelfde e-mailadres gebruiken voor providers van sociale identiteiten, wat inhoudt dat de e-mailgebruikersnaam die voor verificatie wordt gebruikt mogelijk niet uniek is voor de tenant.</span><span class="sxs-lookup"><span data-stu-id="cd31a-236">The user can use the same email address across social identity providers, meaning that the email username used for authentication may not be unique to the tenant.</span></span> <span data-ttu-id="cd31a-237">Azure AD B2C dwingt alleen af dat gebruikers een uniek e-mailadres hebben op lokale B2C-accounts.</span><span class="sxs-lookup"><span data-stu-id="cd31a-237">Azure AD B2C will only enforce that users have a unique email address on local B2C accounts.</span></span>

<span data-ttu-id="cd31a-238">Voordat u een provider van sociale identiteiten voor verificatie kunt toevoegen, moet u naar de portal van de identiteitsprovider gaan en een toepassing van de identiteitsprovider instellen, zoals aangegeven in de documentatie van Azure AD B2C.</span><span class="sxs-lookup"><span data-stu-id="cd31a-238">Before you can add a social identity provider for authentication, you must go to the identity provider's portal and set up an identity provider application as instructed in the Azure AD B2C documentation.</span></span> <span data-ttu-id="cd31a-239">Hieronder vindt u een lijst met koppelingen naar de documentatie.</span><span class="sxs-lookup"><span data-stu-id="cd31a-239">A list of links to the documentation is provided below.</span></span>

- [<span data-ttu-id="cd31a-240">Amazon</span><span class="sxs-lookup"><span data-stu-id="cd31a-240">Amazon</span></span>](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-setup-amzn-app)
- [<span data-ttu-id="cd31a-241">Azure AD (Eén tenant)</span><span class="sxs-lookup"><span data-stu-id="cd31a-241">Azure AD (Single Tenant)</span></span>](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-setup-oidc-azure-active-directory)
- [<span data-ttu-id="cd31a-242">Microsoft-account</span><span class="sxs-lookup"><span data-stu-id="cd31a-242">Microsoft Account</span></span>](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-setup-msa-app)
- [<span data-ttu-id="cd31a-243">Facebook</span><span class="sxs-lookup"><span data-stu-id="cd31a-243">Facebook</span></span>](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-setup-fb-app)
- [<span data-ttu-id="cd31a-244">GitHub</span><span class="sxs-lookup"><span data-stu-id="cd31a-244">GitHub</span></span>](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-setup-github-app)
- [<span data-ttu-id="cd31a-245">Google</span><span class="sxs-lookup"><span data-stu-id="cd31a-245">Google</span></span>](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-setup-goog-app)
- [<span data-ttu-id="cd31a-246">LinkedIn</span><span class="sxs-lookup"><span data-stu-id="cd31a-246">LinkedIn</span></span>](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-setup-li-app)
- [<span data-ttu-id="cd31a-247">OpenID Connect</span><span class="sxs-lookup"><span data-stu-id="cd31a-247">OpenID Connect</span></span>](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-setup-oidc-idp)
- [<span data-ttu-id="cd31a-248">Twitter</span><span class="sxs-lookup"><span data-stu-id="cd31a-248">Twitter</span></span>](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-setup-twitter-app)

### <a name="add-and-set-up-a-social-identity-provider"></a><span data-ttu-id="cd31a-249">Een provider van sociale identiteiten toevoegen en instellen</span><span class="sxs-lookup"><span data-stu-id="cd31a-249">Add and set up a social identity provider</span></span>

<span data-ttu-id="cd31a-250">Voer de volgende stappen uit om een provider van sociale identiteiten toe te voegen en in te stellen.</span><span class="sxs-lookup"><span data-stu-id="cd31a-250">To add and set up a social identity provider, follow these steps.</span></span>  

1. <span data-ttu-id="cd31a-251">Navigeer in de Azure-portal naar **Identiteitsproviders**.</span><span class="sxs-lookup"><span data-stu-id="cd31a-251">In the Azure portal, navigate to **Identity Providers**.</span></span>
1. <span data-ttu-id="cd31a-252">Selecteer **Toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="cd31a-252">Select **Add**.</span></span> <span data-ttu-id="cd31a-253">Het scherm **Identiteitsprovider toevoegen** wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="cd31a-253">The **Add identity provider** screen appears.</span></span>
1. <span data-ttu-id="cd31a-254">Voer onder **Naam** de naam in die voor gebruikers moet worden weergegeven in uw aanmeldingsscherm.</span><span class="sxs-lookup"><span data-stu-id="cd31a-254">Under **Name**, enter the name to be displayed to users on your sign in screen.</span></span>
1. <span data-ttu-id="cd31a-255">Selecteer onder **Type identiteitsprovider** een identiteitsprovider in de lijst.</span><span class="sxs-lookup"><span data-stu-id="cd31a-255">Under **Identity provider type**, select an identity provider from the list.</span></span>
1. <span data-ttu-id="cd31a-256">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="cd31a-256">Select **OK**.</span></span>
1. <span data-ttu-id="cd31a-257">Selecteer **Deze identiteitsprovider instellen** voor toegang tot het scherm **De provider van identiteiten instellen**.</span><span class="sxs-lookup"><span data-stu-id="cd31a-257">Select **Set up this identity provider** to access the **Set up the social identity provider** screen.</span></span>
1. <span data-ttu-id="cd31a-258">Voer onder **Client-id** de client-id in die u hebt opgehaald uit de toepassingsinstellingen van de identiteitsprovider.</span><span class="sxs-lookup"><span data-stu-id="cd31a-258">Under **Client ID**, enter the client ID as obtained from the identity provider application setup.</span></span>
1. <span data-ttu-id="cd31a-259">Voer onder **Clientgeheim** het clientgeheim in dat u hebt opgehaald uit de toepassingsinstellingen van de identiteitsprovider.</span><span class="sxs-lookup"><span data-stu-id="cd31a-259">Under **Client secret**, enter the client secret as obtained from the identity provider application setup.</span></span>
1. <span data-ttu-id="cd31a-260">Gebruikersstroom voor beleid voor registreren en aanmelden koppelen:</span><span class="sxs-lookup"><span data-stu-id="cd31a-260">Attach user flow for sign in sign up policies:</span></span>
1. <span data-ttu-id="cd31a-261">Ga naar **Azure AD B2C - Gebruikersstromen (beleid) \> {uw beleid voor registreren en aanmelden} \> Identiteitsproviders**.</span><span class="sxs-lookup"><span data-stu-id="cd31a-261">Go to **Azure AD B2C – User flows (policies) \> {your sign-in sign-up policy} \> Identity providers**.</span></span>
1. <span data-ttu-id="cd31a-262">Als u het beleid voor gebruikersstromen voor registreren/aanmelden wilt bijvoegen, selecteert u de identiteitsproviders die u hebt ingesteld voor uw account.</span><span class="sxs-lookup"><span data-stu-id="cd31a-262">To attach the sign in/sign up user flow policy, select each identity provider you have set up for your account.</span></span> <span data-ttu-id="cd31a-263">Als u deze wilt testen, selecteert u **Gebruikersstroom uitvoeren** voor elke identiteitsprovider.</span><span class="sxs-lookup"><span data-stu-id="cd31a-263">To test these, select **Run user flow** for each identity provider.</span></span> <span data-ttu-id="cd31a-264">Op een nieuw tabblad wordt de aanmeldingspagina weergegeven met het selectievakje voor de nieuwe identiteitsprovider.</span><span class="sxs-lookup"><span data-stu-id="cd31a-264">A new tab will display the sign-in page displaying the new identity provider selection box.</span></span>

<span data-ttu-id="cd31a-265">In de volgende afbeelding ziet u voorbeelden van de schermen **Identiteitsprovider toevoegen** en **De provider van identiteiten instellen** in Azure AD B2C.</span><span class="sxs-lookup"><span data-stu-id="cd31a-265">The following image shows examples of the **Add identity provider** and **Set up the social identity provider** screens in Azure AD B2C.</span></span>

![Een provider van sociale identiteiten toevoegen aan uw toepassing](./media/B2CImage_14.png)

<span data-ttu-id="cd31a-267">De volgende afbeelding toont een voorbeeld van hoe u identiteitsproviders selecteert op de pagina Azure AD B2C-pagina **Identiteitsproviders**.</span><span class="sxs-lookup"><span data-stu-id="cd31a-267">The following image shows an example of how to select identity providers on the Azure AD B2C **Identity Providers** page.</span></span>

![De providers van sociale identiteiten selecteren die u wilt inschakelen voor uw beleid](./media/B2CImage_16.png)

<span data-ttu-id="cd31a-269">In de volgende afbeelding ziet u een voorbeeld van een standaardscherm voor aanmelding waarin een knop voor aanmelding via de provider van de sociale identiteit wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="cd31a-269">The following image shows an example of a default sign-in screen with a social identity provider sign-in button displayed.</span></span>

![Voorbeeld van standaardaanmeldingsscherm met knop voor aanmelding via provider van sociale identiteiten](./media/B2CImage_17.png)

## <a name="update-commerce-headquarters-with-the-new-azure-ad-b2c-information"></a><span data-ttu-id="cd31a-271">Commerce Headquarters bijwerken met de nieuwe Azure AD B2C-informatie</span><span class="sxs-lookup"><span data-stu-id="cd31a-271">Update Commerce headquarters with the new Azure AD B2C information</span></span>

<span data-ttu-id="cd31a-272">Als de bovenstaande Azure AD B2C-inrichtingsstappen zijn voltooid, moet de Azure AD B2C-toepassing in uw Dynamics 365 Commerce-omgeving zijn geregistreerd.</span><span class="sxs-lookup"><span data-stu-id="cd31a-272">Once the Azure AD B2C provisioning steps above are completed, the Azure AD B2C application must be registered in your Dynamics 365 Commerce environment.</span></span>

<span data-ttu-id="cd31a-273">Voer de volgende stappen uit Headquarters bij te werken met de nieuwe Azure AD B2C-informatie.</span><span class="sxs-lookup"><span data-stu-id="cd31a-273">To update headquarters with the new Azure AD B2C information, follow these steps.</span></span>

1. <span data-ttu-id="cd31a-274">Ga in Commerce naar **Gedeelde Commerce-parameters** en selecteer **Identiteitsproviders** in het linkermenu.</span><span class="sxs-lookup"><span data-stu-id="cd31a-274">In Commerce, go to **Commerce Shared Parameters** and select **Identity Providers** in the left menu.</span></span>
1. <span data-ttu-id="cd31a-275">Onder **Identiteitsproviders** doet u het volgende:</span><span class="sxs-lookup"><span data-stu-id="cd31a-275">Under **Identity Providers**, do the following:</span></span>
    1. <span data-ttu-id="cd31a-276">Voer in het vak **Uitgever** de URL van de uitgevende identiteitsprovider in.</span><span class="sxs-lookup"><span data-stu-id="cd31a-276">In the **Issuer** box, enter the identity provider issuer URL.</span></span> <span data-ttu-id="cd31a-277">Zie [Uitgevers-URL ophalen](#obtain-issuer-url) om de uitgevers-URL te vinden.</span><span class="sxs-lookup"><span data-stu-id="cd31a-277">To find your issuer URL, see [Obtain issuer URL](#obtain-issuer-url) below.</span></span>
    1. <span data-ttu-id="cd31a-278">Typ in het vak **Naam** een naam voor de uitgeversrecord.</span><span class="sxs-lookup"><span data-stu-id="cd31a-278">In the **Name** box, enter a name for your issuer record.</span></span>
    1. <span data-ttu-id="cd31a-279">Voer in het vak **Type** de tekst **Azure AD B2C (id_token)** in.</span><span class="sxs-lookup"><span data-stu-id="cd31a-279">In the **Type** box, enter **Azure AD B2C (id_token)**.</span></span>
1. <span data-ttu-id="cd31a-280">Doe het volgende onder **Relying Party's** terwijl het bovenstaande item voor B2C-identiteitsproviders is geselecteerd:</span><span class="sxs-lookup"><span data-stu-id="cd31a-280">Under **Relying Parties**, with the above B2C identity provider item selected, do the following:</span></span>
    1. <span data-ttu-id="cd31a-281">Voer in het vak **ClientID** de id van uw B2C-toepassing in.</span><span class="sxs-lookup"><span data-stu-id="cd31a-281">In the **ClientID** box, enter your B2C application ID.</span></span> <span data-ttu-id="cd31a-282">U vindt deze in het vak **Toepassings-id** op de eigenschappenpagina van de B2C-toepassing.</span><span class="sxs-lookup"><span data-stu-id="cd31a-282">You can find this in the **Application ID** box of your B2C application's properties page.</span></span>
    1. <span data-ttu-id="cd31a-283">Typ **Openbaar** in het vak **Type**.</span><span class="sxs-lookup"><span data-stu-id="cd31a-283">In the **Type** box, enter **Public**.</span></span>
    1. <span data-ttu-id="cd31a-284">Typ **Klant** in het vak **Gebruikerstype**.</span><span class="sxs-lookup"><span data-stu-id="cd31a-284">In the **User Type** box, enter **Customer**.</span></span>
1. <span data-ttu-id="cd31a-285">Selecteer **Opslaan** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="cd31a-285">On the action pane, select **Save**.</span></span>
1. <span data-ttu-id="cd31a-286">Zoek in het Commerce-zoekvak naar **Nummerreeksen** (Organisatiebeheer > Nummerreeksen).</span><span class="sxs-lookup"><span data-stu-id="cd31a-286">In the Commerce search box, search for **Number sequences** (Organization administration > Number sequences).</span></span>
1. <span data-ttu-id="cd31a-287">Selecteer onder het actievenster de optie **Bewerken** onder **Onderhouden**.</span><span class="sxs-lookup"><span data-stu-id="cd31a-287">Under the action pane, select **Edit** under **Maintain**.</span></span>
1. <span data-ttu-id="cd31a-288">Selecteer op het sneltabblad **Algemeen** de optie **Nee** voor **Handmatig**.</span><span class="sxs-lookup"><span data-stu-id="cd31a-288">On the **General** fast tab, select **No** for **Manual**.</span></span>
1. <span data-ttu-id="cd31a-289">Selecteer **Opslaan** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="cd31a-289">On the action pane, select **Save**.</span></span> 
1. <span data-ttu-id="cd31a-290">Zoek in het Commerce-zoekvak naar **Distributieplanning**.</span><span class="sxs-lookup"><span data-stu-id="cd31a-290">In the Commerce search box, search for **Distribution schedule**</span></span>
1. <span data-ttu-id="cd31a-291">Selecteer in het linkernavigatiemenu van de pagina **Distributieplanningen** de taak **1110 Algemene configuratie**.</span><span class="sxs-lookup"><span data-stu-id="cd31a-291">In the left navigation menu of the **Distribution schedules** page, select job **1110 Global configuration**.</span></span>
1. <span data-ttu-id="cd31a-292">Selecteer **Nu uitvoeren** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="cd31a-292">On the action pane, select **Run Now**.</span></span>

### <a name="obtain-issuer-url"></a><span data-ttu-id="cd31a-293">Uitgevers-URL ophalen</span><span class="sxs-lookup"><span data-stu-id="cd31a-293">Obtain issuer URL</span></span>

<span data-ttu-id="cd31a-294">Voer de volgende stappen uit om de uitgevers-URL van de identiteitsprovider te krijgen.</span><span class="sxs-lookup"><span data-stu-id="cd31a-294">To obtain your identity provider issuer URL, follow these steps.</span></span>

1. <span data-ttu-id="cd31a-295">Maak metagegevensadres-URL met de volgende indeling met uw B2C-tenant en -beleid: ``https://<B2CTENANTNAME>.b2clogin.com/<B2CTENANTNAME>.onmicrosoft.com/v2.0/.well-known/openid-configuration?p=<B2CSIGN-INPOLICY>``</span><span class="sxs-lookup"><span data-stu-id="cd31a-295">Create a metadata address URL in the following format using your B2C tenant and policy: ``https://<B2CTENANTNAME>.b2clogin.com/<B2CTENANTNAME>.onmicrosoft.com/v2.0/.well-known/openid-configuration?p=<B2CSIGN-INPOLICY>``</span></span>
    - <span data-ttu-id="cd31a-296">Voorbeeld: ``https://d365plc.b2clogin.com/d365plc.onmicrosoft.com/v2.0/.well-known/openid-configuration?p=B2C_1_signinup``.</span><span class="sxs-lookup"><span data-stu-id="cd31a-296">Example: ``https://d365plc.b2clogin.com/d365plc.onmicrosoft.com/v2.0/.well-known/openid-configuration?p=B2C_1_signinup``.</span></span>
1. <span data-ttu-id="cd31a-297">Voer de metagegevensadres-URL in een browseradresbalk in.</span><span class="sxs-lookup"><span data-stu-id="cd31a-297">Enter the metadata address URL into a browser address bar.</span></span>
1. <span data-ttu-id="cd31a-298">Kopieer in de metagegevens de uitgevers-URL van de identiteitsprovider (de waarde voor **"issuer"**).</span><span class="sxs-lookup"><span data-stu-id="cd31a-298">In the metadata, copy the identity provider issuer URL (the value for **"issuer"**).</span></span>
    - <span data-ttu-id="cd31a-299">Voorbeeld: ``https://login.fabrikam.com/073405c3-0113-4f43-b5e2-df01266e24ae/v2.0/``.</span><span class="sxs-lookup"><span data-stu-id="cd31a-299">Example: ``https://login.fabrikam.com/073405c3-0113-4f43-b5e2-df01266e24ae/v2.0/``.</span></span>

## <a name="configure-your-b2c-tenant-in-commerce-site-builder"></a><span data-ttu-id="cd31a-300">Uw B2C-tenant configureren in Commerce Site Builder</span><span class="sxs-lookup"><span data-stu-id="cd31a-300">Configure your B2C tenant in Commerce site builder</span></span>

<span data-ttu-id="cd31a-301">Nadat de installatie van uw Azure AD B2C-tenant is voltooid, moet u de B2C-tenant configureren in Commerce Site Builder.</span><span class="sxs-lookup"><span data-stu-id="cd31a-301">Once setup of your Azure AD B2C tenant is completed, you must configure the B2C tenant in Commerce site builder.</span></span> <span data-ttu-id="cd31a-302">Configuratiestappen zijn onder andere het verzamelen van B2C-toepassingsgegevens van de Azure-portal, het invoeren van die B2C-toepassingsgegevens in Site Builder en vervolgens het koppelen van de B2C-toepassing aan uw site en kanaal.</span><span class="sxs-lookup"><span data-stu-id="cd31a-302">Configuration steps include collecting B2C application information from the Azure portal, entering that B2C application information into site builder, and then associating the B2C application with your site and channel.</span></span>

### <a name="collect-the-required-application-information"></a><span data-ttu-id="cd31a-303">De vereiste toepassingsgegevens verzamelen</span><span class="sxs-lookup"><span data-stu-id="cd31a-303">Collect the required application information</span></span>

<span data-ttu-id="cd31a-304">Voer de volgende stappen uit om de vereiste toepassingsgegevens te verzamelen.</span><span class="sxs-lookup"><span data-stu-id="cd31a-304">To collect the required application information, follow these steps.</span></span>

1. <span data-ttu-id="cd31a-305">Ga in de Azure-portal naar **Start \> Azure AD B2C - Toepassingen**.</span><span class="sxs-lookup"><span data-stu-id="cd31a-305">In the Azure portal, go to **Home \> Azure AD B2C - Applications**.</span></span>
1. <span data-ttu-id="cd31a-306">Selecteer de gewenste toepassing en selecteer in het linkernavigatievenster **Eigenschappen** om de toepassingsgegevens op te halen.</span><span class="sxs-lookup"><span data-stu-id="cd31a-306">Select your application, and then in the left navigation pane select **Properties** to obtain the application details.</span></span>
1. <span data-ttu-id="cd31a-307">Verzamel in het vak **Toepassings-id** de toepassings-id van de B2C-toepassing die in de B2C-tenant is gemaakt.</span><span class="sxs-lookup"><span data-stu-id="cd31a-307">From the **Application ID** box, collect the application ID of the B2C application created in your B2C tenant.</span></span> <span data-ttu-id="cd31a-308">Deze wordt later ingevoerd als **client-GUID** in Site Builder.</span><span class="sxs-lookup"><span data-stu-id="cd31a-308">This will later be entered as the **Client GUID** in site builder.</span></span>
1. <span data-ttu-id="cd31a-309">Verzamel de antwoord-URL onder **Antwoord-URL**.</span><span class="sxs-lookup"><span data-stu-id="cd31a-309">Under **Reply URL**, collect the reply URL.</span></span>
1. <span data-ttu-id="cd31a-310">Ga naar **Start \> Azure AD B2C – Gebruikersstromen (beleid)** en verzamel vervolgens de namen van elk gebruikersstroombeleid.</span><span class="sxs-lookup"><span data-stu-id="cd31a-310">Go to **Home \> Azure AD B2C – User flows (policies)**, and then collect the names of each user flow policy.</span></span>

<span data-ttu-id="cd31a-311">In de volgende afbeelding ziet u een voorbeeld van de pagina **Azure AD B2C - Toepassingen**.</span><span class="sxs-lookup"><span data-stu-id="cd31a-311">The following image shows an example of the **Azure AD B2C - Applications** page.</span></span>

![Naar de B2C-toepassing navigeren binnen uw tenant](./media/B2CImage_19.png)

<span data-ttu-id="cd31a-313">In de volgende afbeelding ziet u een voorbeeld van de pagina **Eigenschappen** van een toepassing in Azure AD B2C.</span><span class="sxs-lookup"><span data-stu-id="cd31a-313">The following image shows an example of an application **Properties** page in Azure AD B2C.</span></span> 

![De toepassings-id uit de eigenschappen van de B2C-toepassing kopiëren](./media/B2CImage_21.png)

<span data-ttu-id="cd31a-315">De volgende afbeelding toont een voorbeeld van een beleid voor gebruikersstromen op de pagina **Azure AD B2C – Gebruikersstromen (beleid)**.</span><span class="sxs-lookup"><span data-stu-id="cd31a-315">The following image shows an example of user flow policies on the **Azure AD B2C – User flows (policies)** page.</span></span>

![De namen van elke B2C-beleidsstroom verzamelen](./media/B2CImage_22.png)

### <a name="enter-your-aad-b2c-tenant-application-information-into-commerce"></a><span data-ttu-id="cd31a-317">De toepassingsgegevens van de AAD B2C-tenant invoeren in Commerce</span><span class="sxs-lookup"><span data-stu-id="cd31a-317">Enter your AAD B2C tenant application information into Commerce</span></span>

<span data-ttu-id="cd31a-318">U moet gegevens van de Azure AD B2C-tenant invoeren in Commerce Site Builder voordat u de B2C-tenant aan uw site(s) koppelt.</span><span class="sxs-lookup"><span data-stu-id="cd31a-318">You must enter details of the Azure AD B2C tenant into Commerce site builder before associating the B2C tenant with your site(s).</span></span>

<span data-ttu-id="cd31a-319">Ga als volgt te werk om uw toepassingsgegevens voor AAD B2C-tenants toe te voegen aan Commerce.</span><span class="sxs-lookup"><span data-stu-id="cd31a-319">To add your AAD B2C tenant application information to Commerce, follow these steps.</span></span>

1. <span data-ttu-id="cd31a-320">Meld u aan als beheerder van Commerce Site Builder voor uw omgeving.</span><span class="sxs-lookup"><span data-stu-id="cd31a-320">Sign in as an administrator to Commerce site builder for your environment.</span></span>
1. <span data-ttu-id="cd31a-321">Selecteer in het linkernavigatievenster de optie **Tenantinstellingen** om deze uit te vouwen.</span><span class="sxs-lookup"><span data-stu-id="cd31a-321">In the left navigation pane, select **Tenant Settings**  to expand it.</span></span>
1. <span data-ttu-id="cd31a-322">Selecteer **B2C-instellingen** onder **Tenantinstellingen**.</span><span class="sxs-lookup"><span data-stu-id="cd31a-322">Under **Tenant Settings**, select **B2C Settings**.</span></span> 
1. <span data-ttu-id="cd31a-323">Selecteer **Beheren** in het hoofdvenster naast **B2C-toepassingen**.</span><span class="sxs-lookup"><span data-stu-id="cd31a-323">In the main window next **B2C Applications**, select **Manage**.</span></span> <span data-ttu-id="cd31a-324">(Als uw tenant wordt weergegeven in de lijst met B2C-toepassingen, was deze al toegevoegd door een beheerder.</span><span class="sxs-lookup"><span data-stu-id="cd31a-324">(If your tenant appears in the B2C Applications list, then it was already added by an administrator.</span></span> <span data-ttu-id="cd31a-325">Controleer of de items in stap 6 hieronder overeenkomen met de B2C-toepassing.)</span><span class="sxs-lookup"><span data-stu-id="cd31a-325">Verify that the items in step 6 below match your B2C Application.)</span></span>
1. <span data-ttu-id="cd31a-326">Selecteer **B2C-toepassing toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="cd31a-326">Select **Add B2C Application**.</span></span>
1. <span data-ttu-id="cd31a-327">Voer de volgende vereiste items in het weergegeven formulier in met waarden uit uw B2C-tenant en -toepassing.</span><span class="sxs-lookup"><span data-stu-id="cd31a-327">Enter the following required items in the form displayed, using values from your B2C tenant and application.</span></span> <span data-ttu-id="cd31a-328">Velden die niet vereist zijn (zonder sterretje) kunnen leeg worden gelaten.</span><span class="sxs-lookup"><span data-stu-id="cd31a-328">Fields that are not required (those without an asterisk) may be left blank.</span></span>

    - <span data-ttu-id="cd31a-329">**Toepassingsnaam**: de naam voor uw B2C-toepassing, bijvoorbeeld Fabrikam B2C.</span><span class="sxs-lookup"><span data-stu-id="cd31a-329">**Application Name**: The name for your B2C Application, for example "Fabrikam B2C".</span></span>
    - <span data-ttu-id="cd31a-330">**Tenantnaam**: de naam van uw B2C-tenant, bijvoorbeeld Fabrikam.</span><span class="sxs-lookup"><span data-stu-id="cd31a-330">**Tenant Name**: The name of your B2C Tenant, for example "Fabrikam".</span></span>
    - <span data-ttu-id="cd31a-331">**Id beleid voor vergeten wachtwoorden**: de id van het beleid voor de gebruikersstroom voor vergeten wachtwoorden, bijvoorbeeld B2C_1_PasswordReset.</span><span class="sxs-lookup"><span data-stu-id="cd31a-331">**Forget Password Policy ID**: The forget password user flow policy ID, for example "B2C_1_PasswordReset".</span></span>
    - <span data-ttu-id="cd31a-332">**Beleids-id voor aanmelden registreren**: de beleids-id voor registreren en aanmelden, bijvoorbeeld B2C_1_signup_signin.</span><span class="sxs-lookup"><span data-stu-id="cd31a-332">**Signup Signin Policy ID**: The sign up and sign in user flow policy ID, for example "B2C_1_signup_signin".</span></span>
    - <span data-ttu-id="cd31a-333">**Client-GUID**: de B2C-toepassings-id, bijvoorbeeld 22290eb2-c52e-42e9-8b35-a2b0a3bcb9e6.</span><span class="sxs-lookup"><span data-stu-id="cd31a-333">**Client GUID**: The B2C application ID, for example "22290eb2-c52e-42e9-8b35-a2b0a3bcb9e6".</span></span>
    - <span data-ttu-id="cd31a-334">**Profielbeleid-id bewerken**: de beleids-id voor het bewerken van gebruikersprofielen, bijvoorbeeld B2C_1A_ProfileEdit.</span><span class="sxs-lookup"><span data-stu-id="cd31a-334">**Edit Profile Policy ID**: The profile editing user flow policy ID, for example "B2C_1A_ProfileEdit".</span></span>

1. <span data-ttu-id="cd31a-335">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="cd31a-335">Select **OK**.</span></span> <span data-ttu-id="cd31a-336">De naam van de B2C-toepassing wordt nu weergegeven in de lijst.</span><span class="sxs-lookup"><span data-stu-id="cd31a-336">You should now see the name of your B2C application appear in the list.</span></span>

### <a name="associate-the-b2c-application-to-your-site-and-channel"></a><span data-ttu-id="cd31a-337">De B2C-toepassing koppelen aan uw site en kanaal</span><span class="sxs-lookup"><span data-stu-id="cd31a-337">Associate the B2C application to your site and channel</span></span>

> [!WARNING]
> <span data-ttu-id="cd31a-338">Als uw site al is gekoppeld aan een B2C-toepassing, worden bij het overschakelen naar een andere B2C-toepassing de huidige referenties verwijderd voor gebruikers die zich al hebben aangemeld in deze omgeving.</span><span class="sxs-lookup"><span data-stu-id="cd31a-338">If your site is already associated with a B2C application, changing to a different B2C application will remove the current references established for users already signed up in this environment.</span></span> <span data-ttu-id="cd31a-339">Na wijziging zijn de referenties die aan de momenteel toegewezen B2C-toepassing zijn gekoppeld niet beschikbaar voor gebruikers.</span><span class="sxs-lookup"><span data-stu-id="cd31a-339">If changed, any credentials associated with the currently-assigned B2C application will not be available to users.</span></span> 
> 
> <span data-ttu-id="cd31a-340">Werk de B2C-toepassing alleen bij als u de B2C-toepassing voor het kanaal voor de eerste keer instelt of als u wilt dat gebruikers zich opnieuw moeten aanmelden met nieuwe referenties voor dit kanaal met de nieuwe B2C-toepassing.</span><span class="sxs-lookup"><span data-stu-id="cd31a-340">Only update the B2C application if you are setting up the channel's B2C application for the first time or if you intend to have users re-sign up with new credentials to this channel with the new B2C application.</span></span> <span data-ttu-id="cd31a-341">Wees voorzichtig bij het koppelen van kanalen aan B2C-toepassingen en benoem toepassingen duidelijk.</span><span class="sxs-lookup"><span data-stu-id="cd31a-341">Take caution when associating channels to B2C applications, and name applications clearly.</span></span> <span data-ttu-id="cd31a-342">Als een kanaal niet is gekoppeld aan een B2C-toepassing in de onderstaande stappen, worden gebruikers die zich bij dat kanaal voor uw site aanmelden, in de B2C-toepassing ingevoerd als **standaard** in de lijst met B2C-toepassingen onder **Tenantinstellingen \> B2C-instellingen**.</span><span class="sxs-lookup"><span data-stu-id="cd31a-342">If a channel is not associated to a B2C application in the steps below, users signing into that channel for your site will be entered into the B2C application showing as **default** in the **Tenant Settings \> B2C Settings** list of B2C applications.</span></span>

<span data-ttu-id="cd31a-343">Ga als volgt te werk om de B2C-toepassing te koppelen aan uw site en kanaal.</span><span class="sxs-lookup"><span data-stu-id="cd31a-343">To associate the B2C application to your site and channel, follow these steps.</span></span>

1. <span data-ttu-id="cd31a-344">Ga naar de site in Commerce Site Builder.</span><span class="sxs-lookup"><span data-stu-id="cd31a-344">Navigate to your site in Commerce site builder.</span></span>
1. <span data-ttu-id="cd31a-345">Selecteer in het linkernavigatievenster de optie **Site-instellingen** om deze uit te vouwen.</span><span class="sxs-lookup"><span data-stu-id="cd31a-345">In the left navigation pane, select **Site Settings** to expand it.</span></span>
1. <span data-ttu-id="cd31a-346">Selecteer **Kanalen** onder **Site-instellingen**.</span><span class="sxs-lookup"><span data-stu-id="cd31a-346">Below **Site Settings**, select **Channels**.</span></span>
1. <span data-ttu-id="cd31a-347">Selecteer uw kanaal in het hoofdvenster onder **Kanalen**.</span><span class="sxs-lookup"><span data-stu-id="cd31a-347">In the main window under **Channels**, select your channel.</span></span>
1. <span data-ttu-id="cd31a-348">Selecteer in het deelvenster voor kanaaleigenschappen aan de rechterkant de naam van de B2C-toepassing in de vervolgkeuzelijst **B2C-toepassing selecteren**.</span><span class="sxs-lookup"><span data-stu-id="cd31a-348">In the channel properties pane on the right, select your B2C application name from the **Select B2C Application** drop down menu.</span></span>
1. <span data-ttu-id="cd31a-349">Selecteer **Sluiten** en selecteer vervolgens **Opslaan en publiceren**.</span><span class="sxs-lookup"><span data-stu-id="cd31a-349">Select **Close**, and then select **Save and Publish**.</span></span>

## <a name="additional-b2c-information"></a><span data-ttu-id="cd31a-350">Aanvullende B2C-gegevens</span><span class="sxs-lookup"><span data-stu-id="cd31a-350">Additional B2C information</span></span>

### <a name="customer-migration"></a><span data-ttu-id="cd31a-351">Klantmigratie</span><span class="sxs-lookup"><span data-stu-id="cd31a-351">Customer migration</span></span>

<span data-ttu-id="cd31a-352">Als u overweegt om klantrecords te migreren van een eerder platform van een identiteitsprovider, kunt u met het team van Dynamics 365 Commerce samenwerken om uw klantmigratiebehoeften te bekijken.</span><span class="sxs-lookup"><span data-stu-id="cd31a-352">If you are considering migrating customer records from a previous identity provider platform, please work with the Dynamics 365 Commerce team to review your customer migration needs.</span></span>

<span data-ttu-id="cd31a-353">Zie [Gebruikers migreren naar Azure Active Directory B2C](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-user-migration) voor aanvullende Azure AD B2C-documentatie over klantmigratie.</span><span class="sxs-lookup"><span data-stu-id="cd31a-353">For additional Azure AD B2C documentation on customer migration, see [Migrate users to Azure Active Directory B2C](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-user-migration).</span></span>

### <a name="custom-policies"></a><span data-ttu-id="cd31a-354">Aangepast beleid</span><span class="sxs-lookup"><span data-stu-id="cd31a-354">Custom policies</span></span>

<span data-ttu-id="cd31a-355">Zie voor aanvullende informatie over het aanpassen van Azure AD B2C-interacties en beleidsstromen die verdergaan dan wat wordt aangeboden op basis van B2C-standaardbeleid [Aangepaste beleid in Azure Active Directory B2C](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-overview-custom).</span><span class="sxs-lookup"><span data-stu-id="cd31a-355">For additional information regarding customizing Azure AD B2C interactions and policy flows beyond what is offered by B2C standard policies, see [Custom policies in Azure Active Directory B2C](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-overview-custom).</span></span> 

### <a name="secondary-admin"></a><span data-ttu-id="cd31a-356">Secundaire beheerder</span><span class="sxs-lookup"><span data-stu-id="cd31a-356">Secondary admin</span></span>

<span data-ttu-id="cd31a-357">U kunt een optionele, secundaire beheerdersaccount toevoegen in de sectie **Gebruikers** van uw B2C-tenant.</span><span class="sxs-lookup"><span data-stu-id="cd31a-357">An optional, secondary administrator account can be added in the **Users** section of your B2C tenant.</span></span> <span data-ttu-id="cd31a-358">Dit kan een directe account of een algemene account zijn.</span><span class="sxs-lookup"><span data-stu-id="cd31a-358">This can be a direct account or a general account.</span></span> <span data-ttu-id="cd31a-359">Als u een account wilt delen tussen teamresources, kan ook een algemene account worden gemaakt.</span><span class="sxs-lookup"><span data-stu-id="cd31a-359">If you need to share an account across team resources, a common account can also be created.</span></span> <span data-ttu-id="cd31a-360">Vanwege de gevoeligheid van de gegevens die zijn opgeslagen in Azure AD B2C, moet een gemeenschappelijke account nauwkeurig worden gemonitord volgens de beveiligingsprocedures van uw bedrijf.</span><span class="sxs-lookup"><span data-stu-id="cd31a-360">Due to the sensitivity of the data stored in Azure AD B2C, a common account should be monitored closely per your company's security practices.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="cd31a-361">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="cd31a-361">Additional resources</span></span>

[<span data-ttu-id="cd31a-362">Uw domeinnaam configureren</span><span class="sxs-lookup"><span data-stu-id="cd31a-362">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="cd31a-363">Een nieuwe e-commerce-site implementeren</span><span class="sxs-lookup"><span data-stu-id="cd31a-363">Deploy a new e-Commerce site</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="cd31a-364">Een e-commerce-site maken</span><span class="sxs-lookup"><span data-stu-id="cd31a-364">Create an e-Commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="cd31a-365">Een online-site koppelen aan een kanaal</span><span class="sxs-lookup"><span data-stu-id="cd31a-365">Associate an online site with a channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="cd31a-366">Robots.txt-bestanden beheren</span><span class="sxs-lookup"><span data-stu-id="cd31a-366">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="cd31a-367">URL-omleidingen in bulk uploaden</span><span class="sxs-lookup"><span data-stu-id="cd31a-367">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

[<span data-ttu-id="cd31a-368">Aangepaste pagina's voor gebruikersaanmeldingen instellen</span><span class="sxs-lookup"><span data-stu-id="cd31a-368">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="cd31a-369">Meerdere B2C-tenants configureren in een Commerce-omgeving</span><span class="sxs-lookup"><span data-stu-id="cd31a-369">Configure multiple B2C tenants in a Commerce environment</span></span>](configure-multi-B2C-tenants.md)

[<span data-ttu-id="cd31a-370">Ondersteuning voor een CDN (contentleveringsnetwerk) toevoegen</span><span class="sxs-lookup"><span data-stu-id="cd31a-370">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="cd31a-371">Detectie van winkels op basis van de locatie inschakelen</span><span class="sxs-lookup"><span data-stu-id="cd31a-371">Enable location-based store detection</span></span>](enable-store-detection.md)
