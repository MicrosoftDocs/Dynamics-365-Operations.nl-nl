---
title: Authenticatie
description: Dit artikel bevat overzichtsinformatie over het verifiëren met de Application Programming Interface (API) voor Microsoft Dynamics 365 Human Resources.
author: andreabichsel
manager: tfehr
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 60774d162d733404166e710932291a736eb0d8b4
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/17/2021
ms.locfileid: "5465529"
---
# <a name="authentication"></a><span data-ttu-id="15a06-103">Authenticatie</span><span class="sxs-lookup"><span data-stu-id="15a06-103">Authentication</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="15a06-104">Dit artikel bevat overzichtsinformatie over het verifiëren met de Application Programming Interface (API) voor Microsoft Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="15a06-104">This article provides overview information about how to authenticate with the Microsoft Dynamics 365 Human Resources data application programming interface (API).</span></span>

## <a name="overview"></a><span data-ttu-id="15a06-105">Overzicht</span><span class="sxs-lookup"><span data-stu-id="15a06-105">Overview</span></span>

<span data-ttu-id="15a06-106">De gegevens-API voor Human Resources is een OData-implementatie.</span><span class="sxs-lookup"><span data-stu-id="15a06-106">The data API for Human Resources is an OData implementation.</span></span> <span data-ttu-id="15a06-107">Zie [Open Data Protocol (OData)](../fin-ops-core/dev-itpro/data-entities/odata.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="15a06-107">For more information, see [Open Data Protocol (OData)](../fin-ops-core/dev-itpro/data-entities/odata.md).</span></span>

<span data-ttu-id="15a06-108">Uw toepassing moet worden geverifieerd als geautoriseerde aanvrager voordat de API aanvragen van uw toepassing kan verwerken.</span><span class="sxs-lookup"><span data-stu-id="15a06-108">Your application must authenticate as an authorized caller before the API will service requests from your application.</span></span>

## <a name="fundamentals"></a><span data-ttu-id="15a06-109">Basisgegevens</span><span class="sxs-lookup"><span data-stu-id="15a06-109">Fundamentals</span></span>

<span data-ttu-id="15a06-110">Uw toepassing moet een toegangstoken van het Microsoft-identiteitsplatform verkrijgen om de gegevens-API te kunnen aanroepen.</span><span class="sxs-lookup"><span data-stu-id="15a06-110">To call the data API, your application must acquire an access token from the Microsoft identity platform.</span></span> <span data-ttu-id="15a06-111">Het toegangstoken bevat informatie over uw toepassing en de machtiging die deze nodig heeft voor het aanroepen van resources in Human Resources.</span><span class="sxs-lookup"><span data-stu-id="15a06-111">The access token contains information about your application and the permission that it has to call resources in Human Resources.</span></span>

### <a name="access-token"></a><span data-ttu-id="15a06-112">Toegangstoken</span><span class="sxs-lookup"><span data-stu-id="15a06-112">Access token</span></span>

<span data-ttu-id="15a06-113">Toegangstokens die door het Microsoft-identiteitsplatform worden uitgegeven, zijn in base64 gecodeerde JSON-webtokens (JavaScript Object Notation) (JWT's).</span><span class="sxs-lookup"><span data-stu-id="15a06-113">Access tokens issued by the Microsoft identity platform are base64–encoded JavaScript Object Notation (JSON) Web Tokens (JWTs).</span></span> <span data-ttu-id="15a06-114">Ze bevatten informatie (claims) die door de gegevens-API (en andere web-API's die zijn beveiligd door het Microsoft-identiteitsplatform) worden gebruikt om de beller te valideren en ervoor te zorgen dat de beller over de juiste machtigingen beschikt om de gevraagde bewerking uit te voeren.</span><span class="sxs-lookup"><span data-stu-id="15a06-114">They contain information (claims) that the data API (and other web APIs that are secured by the Microsoft identity platform) use to validate the caller and make sure that the caller has the correct permissions to perform the operation they're requesting.</span></span> <span data-ttu-id="15a06-115">Tijdens oproepen kunt u toegangstokens als ondoorzichtig behandelen.</span><span class="sxs-lookup"><span data-stu-id="15a06-115">During calls, you can treat access tokens as opaque.</span></span> <span data-ttu-id="15a06-116">U moet toegangstokens altijd via een beveiligd kanaal verzenden, zoals TLS (Transport Layer Security) en HTTPS (Hypertext Transfer Protocol Secure).</span><span class="sxs-lookup"><span data-stu-id="15a06-116">You should always transmit access tokens over a secure channel, such as Transport Layer Security (TLS) and Hypertext Transfer Protocol Secure (HTTPS).</span></span>

<span data-ttu-id="15a06-117">Hier volgt een voorbeeld van een toegangstoken dat is uitgegeven door het Microsoft-identiteitsplatform.</span><span class="sxs-lookup"><span data-stu-id="15a06-117">Here is an example of an access token that is issued by the Microsoft identity platform.</span></span>

```jwt
EwAoA8l6BAAU7p9QDpi/D7xJLwsTgCg3TskyTaQAAXu71AU9f4aS4rOK5xoO/SU5HZKSXtCsDe0Pj7uSc5Ug008qTI+a9M1tBeKoTs7tHzhJNSKgk7pm5e8d3oGWXX5shyOG3cKSqgfwuNDnmmPDNDivwmi9kmKqWIC9OQRf8InpYXH7NdUYNwN+jljffvNTewdZz42VPrvqoMH7hSxiG7A1h8leOv4F3Ek/oeJX6U8nnL9nJ5pHLVuPWD0aNnTPTJD8Y4oQTp5zLhDIIfaJCaGcQperULVF7K6yX8MhHxIBwek418rKIp11om0SWBXOYSGOM0rNNN59qNiKwLNK+MPUf7ObcRBN5I5vg8jB7IMoz66jrNmT2uiWCyI8MmYDZgAACPoaZ9REyqke+AE1/x1ZX0w7OamUexKF8YGZiw+cDpT/BP1GsONnwI4a8M7HsBtDgZPRd6/Hfqlq3HE2xLuhYX8bAc1MUr0gP9KuH6HDQNlIV4KaRZWxyRo1wmKHOF5G5wTHrtxg8tnXylMc1PKOtaXIU4JJZ1l4x/7FwhPmg9M86PBPWr5zwUj2CVXC7wWlL/6M89Mlh8yXESMO3AIuAmEMKjqauPrgi9hAdI2oqnLZWCRL9gcHBida1y0DTXQhcwMv1ORrk65VFHtVgYAegrxu3NDoJiDyVaPZxDwTYRGjPII3va8GALAMVy5xou2ikzRvJjW7Gm3XoaqJCTCExN4m5i/Dqc81Gr4uT7OaeypYTUjnwCh7aMhsOTDJehefzjXhlkn//2eik+NivKx/BTJBEdT6MR97Wh/ns/VcK7QTmbjwbU2cwLngT7Ylq+uzhx54R9JMaSLhnw+/nIrcVkG77Hi3neShKeZmnl5DC9PuwIbtNvVge3Q+V0ws2zsL3z7ndz4tTMYFdvR/XbrnbEErTDLWrV6Lc3JHQMs0bYUyTBg5dThwCiuZ1evaT6BlMMLuSCVxdBGzXTBcvGwihFzZbyNoX+52DS5x+RbIEvd6KWOpQ6Ni+1GAawHDdNUiQTQFXRxLSHfc9fh7hE4qcD7PqHGsykYj7A0XqHCjbKKgWSkcAg==
```

<span data-ttu-id="15a06-118">Als u de gegevens-API wilt aanroepen, koppelt u het toegangstoken als een bearertoken aan de autorisatiekoptekst in uw HTTP-aanvraag.</span><span class="sxs-lookup"><span data-stu-id="15a06-118">To call the data API, you attach the access token as a bearer token to the authorization header in your HTTP request.</span></span> <span data-ttu-id="15a06-119">Hier volgt een voorbeeld.</span><span class="sxs-lookup"><span data-stu-id="15a06-119">Here is an example.</span></span>

```HTTP
HTTP/1.1
Authorization: Bearer EwAoA8l6BAAU ... 7PqHGsykYj7A0XqHCjbKKgWSkcAg==
Host: https://{cluster}.hr.talent.dynamics.com
GET https://{cluster}.hr.talent.dynamics.com/namespaces/{namespace_guid}/data/JobTypes
```

## <a name="register-a-new-application-by-using-the-azure-portal"></a><span data-ttu-id="15a06-120">Een nieuwe toepassing registreren via de Azure-portal</span><span class="sxs-lookup"><span data-stu-id="15a06-120">Register a new application by using the Azure portal</span></span>

1. <span data-ttu-id="15a06-121">Meld u aan bij de [Microsoft Azure-portal](https://portal.azure.com) met een werk- of schoolaccount of een persoonlijk Microsoft-account.</span><span class="sxs-lookup"><span data-stu-id="15a06-121">Sign in to the [Microsoft Azure portal](https://portal.azure.com) with a work or school account, or a personal Microsoft account.</span></span>

2. <span data-ttu-id="15a06-122">Als uw account toegang geeft tot meer dan één tenant, selecteert u uw-account in de rechterbovenhoek en stelt u uw portalsessie in op de gewenste Azure Active Directory-tenant (Azure AD).</span><span class="sxs-lookup"><span data-stu-id="15a06-122">If your account gives you access to more than one tenant, select your account in the upper-right corner, and set your portal session to the Azure Active Directory (Azure AD) tenant that you want.</span></span>

3. <span data-ttu-id="15a06-123">Selecteer in het linkerdeelvenster de **Azure Active Directory**-service en selecteer vervolgens **App-registraties \> Nieuwe registratie**.</span><span class="sxs-lookup"><span data-stu-id="15a06-123">In the left pane, select the **Azure Active Directory** service, and then select **App registrations \> New registration**.</span></span>

4. <span data-ttu-id="15a06-124">Wanneer de pagina **Een toepassing registreren** wordt weergegeven, voert u de registratiegegevens van uw toepassing in:</span><span class="sxs-lookup"><span data-stu-id="15a06-124">When the **Register an application** page appears, enter your application's registration information:</span></span>

    - <span data-ttu-id="15a06-125">**Naam**: voer een herkenbare toepassingsnaam in die wordt weergegeven aan gebruikers van de app.</span><span class="sxs-lookup"><span data-stu-id="15a06-125">**Name**: Enter a meaningful application name that will be shown to users of the app.</span></span>
    - <span data-ttu-id="15a06-126">**Ondersteunde rekeningtypen**: selecteer de typen rekeningen die uw app moet ondersteunen.</span><span class="sxs-lookup"><span data-stu-id="15a06-126">**Supported account types**: Select the types of accounts that your app should support.</span></span>

        | <span data-ttu-id="15a06-127">Ondersteunde rekeningtypen</span><span class="sxs-lookup"><span data-stu-id="15a06-127">Supported account types</span></span> | <span data-ttu-id="15a06-128">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="15a06-128">Description</span></span> |
        |-------------------------|-------------|
        | <span data-ttu-id="15a06-129">Alleen accounts in deze organisatieadreslijst</span><span class="sxs-lookup"><span data-stu-id="15a06-129">Accounts in this organizational directory only</span></span> | <span data-ttu-id="15a06-130">Selecteer deze optie als u een LOB-app (Line-Of-Business) wilt maken.</span><span class="sxs-lookup"><span data-stu-id="15a06-130">Select this option if you're building a line-of-business app.</span></span> <span data-ttu-id="15a06-131">Deze optie is alleen beschikbaar als u de app in een adreslijst registreert.</span><span class="sxs-lookup"><span data-stu-id="15a06-131">This option isn't available unless you're registering the app in a directory.</span></span><p><span data-ttu-id="15a06-132">Deze optie wordt toegewezen aan **Azure AD alleen enkele tenant**.</span><span class="sxs-lookup"><span data-stu-id="15a06-132">This option is mapped to **Azure AD only single-tenant**.</span></span></p><p><span data-ttu-id="15a06-133">Deze optie is de standaardoptie, tenzij u de app registreert buiten een adreslijst.</span><span class="sxs-lookup"><span data-stu-id="15a06-133">This option is the default option unless you're registering the app outside a directory.</span></span> <span data-ttu-id="15a06-134">In dat geval is **Azure AD multi-tenant en persoonlijke Microsoft-accounts** de standaardoptie.</span><span class="sxs-lookup"><span data-stu-id="15a06-134">In that case, the default option is **Azure AD multi-tenant and personal Microsoft accounts**.</span></span></p> |
        | <span data-ttu-id="15a06-135">Accounts in een willekeurige organisatieadreslijst</span><span class="sxs-lookup"><span data-stu-id="15a06-135">Accounts in any organizational directory</span></span> | <span data-ttu-id="15a06-136">Selecteer deze optie als u alle zakelijke en educatieve klanten wilt bereiken.</span><span class="sxs-lookup"><span data-stu-id="15a06-136">Select this option to target all business and educational customers.</span></span><p><span data-ttu-id="15a06-137">Deze optie wordt toegewezen aan **Azure AD alleen multi-tenant**.</span><span class="sxs-lookup"><span data-stu-id="15a06-137">This option is mapped to **Azure AD only multi-tenant**.</span></span></p><p><span data-ttu-id="15a06-138">Als u de app als **Azure AD alleen enkele tenant** hebt geregistreerd, kunt u de blade **Verificatie** gebruiken om de app bij te werken naar **Azure AD alleen multi-tenant** en vervolgens weer terug naar **Azure AD alleen enkele tenant**.</span><span class="sxs-lookup"><span data-stu-id="15a06-138">If you registered the app as **Azure AD only single-tenant**, you can use the **Authentication** blade to update it to **Azure AD only multi-tenant** and then back to **Azure AD only single-tenant**.</span></span></p> |
        | <span data-ttu-id="15a06-139">Rekeningen in een organisatieadreslijst en persoonlijke Microsoft-accounts</span><span class="sxs-lookup"><span data-stu-id="15a06-139">Accounts in any organizational directory and personal Microsoft accounts</span></span> | <span data-ttu-id="15a06-140">Selecteer deze optie als u de breedste groep klanten wilt bereiken.</span><span class="sxs-lookup"><span data-stu-id="15a06-140">Select this option to target the widest set of customers.</span></span><p><span data-ttu-id="15a06-141">Deze optie wordt toegewezen aan **Azure AD multi-tenant en persoonlijke Microsoft-accounts**.</span><span class="sxs-lookup"><span data-stu-id="15a06-141">This option is mapped to **Azure AD multi-tenant and personal Microsoft accounts**.</span></span></p><p><span data-ttu-id="15a06-142">Als u de app als **Azure AD multi tenant en persoonlijke Microsoft-accounts** hebt geregistreerd, kunt u deze instelling niet wijzigen in de gebruikersinterface.</span><span class="sxs-lookup"><span data-stu-id="15a06-142">If you registered the app as **Azure AD multi-tenant and personal Microsoft accounts**, you can't change this setting in the user interface (UI).</span></span> <span data-ttu-id="15a06-143">In plaats daarvan moet u de Application Manifest Editor gebruiken om de ondersteunde rekeningtypen te wijzigen.</span><span class="sxs-lookup"><span data-stu-id="15a06-143">Instead, you must use the application manifest editor to change the supported account types.</span></span></p> |

    - <span data-ttu-id="15a06-144">**URI omleiden (optioneel)**: selecteer het type app dat u wilt maken: **Web** of **Openbare client (mobiel en bureaublad**).</span><span class="sxs-lookup"><span data-stu-id="15a06-144">**Redirect URI (optional)** – Select the type of app that you're building: **Web** or **Public client (mobile & desktop)**.</span></span> <span data-ttu-id="15a06-145">Voer vervolgens de omleidings-URI (of antwoord-URL) in voor de app.</span><span class="sxs-lookup"><span data-stu-id="15a06-145">Then enter the redirect URI (or reply URL) for the app.</span></span>

        - <span data-ttu-id="15a06-146">Geef voor webapps de basis-URL van de app op.</span><span class="sxs-lookup"><span data-stu-id="15a06-146">For web apps, provide the base URL of the app.</span></span> <span data-ttu-id="15a06-147">Zo kan `http://localhost:31544` bijvoorbeeld de URL zijn voor een webapp zijn die op uw lokale computer wordt uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="15a06-147">For example, `http://localhost:31544` might be the URL for a web app that runs on your local machine.</span></span> <span data-ttu-id="15a06-148">Gebruikers kunnen deze URL gebruiken om zich aan te melden bij een webclient-app.</span><span class="sxs-lookup"><span data-stu-id="15a06-148">Users then use this URL to sign in to a web client app.</span></span>
        - <span data-ttu-id="15a06-149">Geef voor openbare clientapps de URI op die Azure AD gebruikt wordt voor het retourneren van tokenantwoorden.</span><span class="sxs-lookup"><span data-stu-id="15a06-149">For public client apps, provide the URI that Azure AD uses to return token responses.</span></span> <span data-ttu-id="15a06-150">Voer een waarde in die specifiek is voor uw app, zoals `myapp://auth`.</span><span class="sxs-lookup"><span data-stu-id="15a06-150">Enter a value that is specific to your app, such as `myapp://auth`.</span></span>

        <span data-ttu-id="15a06-151">Zie de QuickStarts in [Microsoft-identiteitsplatform (voorheen Azure Active Directory voor ontwikkelaars)](https://docs.microsoft.com/azure/active-directory/develop/#quickstarts) voor specifieke voorbeelden van webapps of native apps.</span><span class="sxs-lookup"><span data-stu-id="15a06-151">To see specific examples for web apps or native apps, see the quickstarts in [Microsoft identity platform (formerly Azure Active Directory for developers)](https://docs.microsoft.com/azure/active-directory/develop/#quickstarts).</span></span>

5. <span data-ttu-id="15a06-152">Selecteer **Een machtiging toevoegen** onder **API-machtigingen**.</span><span class="sxs-lookup"><span data-stu-id="15a06-152">Under **API permissions**, select **Add a permission**.</span></span> <span data-ttu-id="15a06-153">Zoek vervolgens op het tabblad **API's die mijn organisatie gebruikt** naar **Dynamics 365 Human Resources** en voeg de machtiging **gebruikers\_imitatie** toe aan uw app.</span><span class="sxs-lookup"><span data-stu-id="15a06-153">Then, on the **APIs my organization uses** tab, search for **Dynamics 365 Human Resources**, and add the **user\_impersonation** permission to your app.</span></span> <span data-ttu-id="15a06-154">De toepassings-id voor Human Resources is f9be0c49-aa22-4ec6-911a-c5da515226ffis.</span><span class="sxs-lookup"><span data-stu-id="15a06-154">The Application ID for Human Resources is f9be0c49-aa22-4ec6-911a-c5da515226ff.</span></span> <span data-ttu-id="15a06-155">Gebruik deze id om ervoor te zorgen dat u de juiste toepassing hebt gekozen.</span><span class="sxs-lookup"><span data-stu-id="15a06-155">Use this ID to ensure you have chosen the correct application.</span></span>

6. <span data-ttu-id="15a06-156">Selecteer **Registreren**.</span><span class="sxs-lookup"><span data-stu-id="15a06-156">Select **Register**.</span></span>

   <span data-ttu-id="15a06-157">[![Een nieuwe app registreren in de Azure-portal](media/api-new-app-registration-expanded.png)](media/api-new-app-registration-expanded.png#lightbox)</span><span class="sxs-lookup"><span data-stu-id="15a06-157">[![Registering a new app in the Azure portal](media/api-new-app-registration-expanded.png)](media/api-new-app-registration-expanded.png#lightbox)</span></span>

<span data-ttu-id="15a06-158">Azure AD wijst een unieke toepassings-id (client-id) toe aan uw app en brengt u naar de pagina **Overzicht** van uw app.</span><span class="sxs-lookup"><span data-stu-id="15a06-158">Azure AD assigns a unique application ID (client ID) to your app, and takes you to the **Overview** page for your app.</span></span> <span data-ttu-id="15a06-159">Als u meer mogelijkheden aan uw app wilt toevoegen, kunt u andere configuratieopties selecteren, zoals opties voor huisstijl en voor certificaten en geheimen.</span><span class="sxs-lookup"><span data-stu-id="15a06-159">To add more capabilities to your app, you can select other configuration options, such as options for branding and for certificates and secrets.</span></span>

## <a name="retrieving-an-access-token"></a><span data-ttu-id="15a06-160">Een toegangstoken ophalen</span><span class="sxs-lookup"><span data-stu-id="15a06-160">Retrieving an access token</span></span>

<span data-ttu-id="15a06-161">De specifieke informatie over hoe u een toegangstoken ophaalt voor het aanroepen van de gegevens-API van Human Resources is afhankelijk van de technologieën die u gebruikt om de clienttoepassing te ontwikkelen.</span><span class="sxs-lookup"><span data-stu-id="15a06-161">The specifics of how you retrieve an access token for calling the Human Resources data API will depend on what technologies you're using to develop your client application.</span></span> <span data-ttu-id="15a06-162">Zo kunt u bijvoorbeeld [testen met een hulpprogramma van derden](../fin-ops-core/dev-itpro/data-entities/third-party-service-test.md) (zoals Postman), een C#-consoletoepassing of -webservice ontwikkelen of een Javascript/TypeScript-client bouwen.</span><span class="sxs-lookup"><span data-stu-id="15a06-162">For example, you might be [testing with a third party utility](../fin-ops-core/dev-itpro/data-entities/third-party-service-test.md) (such as Postman), developing a C# console application or web service, or building a javascript/TypeScript client.</span></span>

<span data-ttu-id="15a06-163">Voorbeeld van C#-clienttoepassing:</span><span class="sxs-lookup"><span data-stu-id="15a06-163">Example C# client application:</span></span>
```C#
using System;
using System.Net.Http;
using System.Threading.Tasks;

// requires appropriate NuGet package references in the project
using Microsoft.IdentityModel.Clients.ActiveDirectory;

namespace TalentODataPoC
{
    class Program
    {
        // prereq: This client app must be registered in Azure Active Directory. The app must be
        // registered as requiring permission to the Dynamics 365 for Talent API (with the Dynamics
        // HCM Workload delegated permission).
        static string clientId = "4fc703ef-672c-4e2c-813f-2f9d29d726db"; // This value should be obtained from AAD and must match your registered app
        static string talentNamespaceUri = "";

        public static async Task CallTalentODataService()
        {
            // authority URI
            UriBuilder uri = new UriBuilder("https://login.microsoftonline.com/common");
            AuthenticationContext authenticationContext = new AuthenticationContext(uri.ToString());

            // request token for the resource we want to access (Human Resources). This will authenticate
            // the user and return an access token containing claims for the authenticated user.
            var authResult = await authenticationContext.AcquireTokenAsync(
                "http://hr.talent.dynamics.com", /*Talent app id or resource URI*/
                clientId, /*registered client app id*/
                new Uri("https://localhost"), /*redirect URI, as registered in your AAD app*/
                new PlatformParameters(PromptBehavior.SelectAccount));

            // create the authorization header, which needs to be passed in the Header of the HTTP Requests to Talent
            string authHeader = authResult.CreateAuthorizationHeader();

            // HINT: paste the JWT into https://jwt.ms to decode and view it
            Console.Write("authHeader: ");
            Console.WriteLine(authHeader);
            Console.WriteLine();

            HttpClient client = new HttpClient();
            client.DefaultRequestHeaders.Add("Authorization", authHeader);

            string s;

            Console.Write("Talent Namespace URI: ");
            Console.WriteLine(talentNamespaceUri);
            Console.WriteLine();

            // call the OData service to get JobType data from Talent
            var resultOdata = await client.GetAsync(talentNamespaceUri + "data/JobTypes");
            s = await resultOdata.Content.ReadAsStringAsync();
            Console.WriteLine(s);
            Console.WriteLine();
        }

        static void Main(string[] args)
        {
            Console.WriteLine();

            // if the user passes in a single parameter, assume it is the namespaceUri for Talent
            if (args.Length == 1)
            {
                talentNamespaceUri = args[0];
            } else if (args.Length == 0)
            {
                Console.WriteLine("Enter Talent URL including namespace.");
                Console.WriteLine("Example: https://aos-rts-sf-21454f9d830-prod-westus2.hr.talent.dynamics.com/namespaces/2328af1a-2d45-4c6a-99e3-12a4c3867dcf/");
                Console.Write("> ");
                talentNamespaceUri = Console.ReadLine();
                if (!talentNamespaceUri.EndsWith("/"))
                {
                    talentNamespaceUri = talentNamespaceUri + "/";
                }
            } else
            {
                Console.WriteLine("Unexpected Arguments");
                System.Environment.Exit(1);
            }

            Task t = Program.CallTalentODataService();
            t.Wait();
        }
    }
}
```

<span data-ttu-id="15a06-164">Wanneer u een toegangstoken hebt opgehaald, geeft u het token in de autorisatiekoptekst door als een bearertoken met elke aanvraag die u naar de gegevens-API verzendt, zoals hierboven is beschreven.</span><span class="sxs-lookup"><span data-stu-id="15a06-164">Once you've retrieved an access token, you'll pass the token in the Authorization header as a bearer token with each request you send to the data API, as described above.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]