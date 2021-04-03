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
# <a name="authentication"></a>Authenticatie

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Dit artikel bevat overzichtsinformatie over het verifiëren met de Application Programming Interface (API) voor Microsoft Dynamics 365 Human Resources.

## <a name="overview"></a>Overzicht

De gegevens-API voor Human Resources is een OData-implementatie. Zie [Open Data Protocol (OData)](../fin-ops-core/dev-itpro/data-entities/odata.md) voor meer informatie.

Uw toepassing moet worden geverifieerd als geautoriseerde aanvrager voordat de API aanvragen van uw toepassing kan verwerken.

## <a name="fundamentals"></a>Basisgegevens

Uw toepassing moet een toegangstoken van het Microsoft-identiteitsplatform verkrijgen om de gegevens-API te kunnen aanroepen. Het toegangstoken bevat informatie over uw toepassing en de machtiging die deze nodig heeft voor het aanroepen van resources in Human Resources.

### <a name="access-token"></a>Toegangstoken

Toegangstokens die door het Microsoft-identiteitsplatform worden uitgegeven, zijn in base64 gecodeerde JSON-webtokens (JavaScript Object Notation) (JWT's). Ze bevatten informatie (claims) die door de gegevens-API (en andere web-API's die zijn beveiligd door het Microsoft-identiteitsplatform) worden gebruikt om de beller te valideren en ervoor te zorgen dat de beller over de juiste machtigingen beschikt om de gevraagde bewerking uit te voeren. Tijdens oproepen kunt u toegangstokens als ondoorzichtig behandelen. U moet toegangstokens altijd via een beveiligd kanaal verzenden, zoals TLS (Transport Layer Security) en HTTPS (Hypertext Transfer Protocol Secure).

Hier volgt een voorbeeld van een toegangstoken dat is uitgegeven door het Microsoft-identiteitsplatform.

```jwt
EwAoA8l6BAAU7p9QDpi/D7xJLwsTgCg3TskyTaQAAXu71AU9f4aS4rOK5xoO/SU5HZKSXtCsDe0Pj7uSc5Ug008qTI+a9M1tBeKoTs7tHzhJNSKgk7pm5e8d3oGWXX5shyOG3cKSqgfwuNDnmmPDNDivwmi9kmKqWIC9OQRf8InpYXH7NdUYNwN+jljffvNTewdZz42VPrvqoMH7hSxiG7A1h8leOv4F3Ek/oeJX6U8nnL9nJ5pHLVuPWD0aNnTPTJD8Y4oQTp5zLhDIIfaJCaGcQperULVF7K6yX8MhHxIBwek418rKIp11om0SWBXOYSGOM0rNNN59qNiKwLNK+MPUf7ObcRBN5I5vg8jB7IMoz66jrNmT2uiWCyI8MmYDZgAACPoaZ9REyqke+AE1/x1ZX0w7OamUexKF8YGZiw+cDpT/BP1GsONnwI4a8M7HsBtDgZPRd6/Hfqlq3HE2xLuhYX8bAc1MUr0gP9KuH6HDQNlIV4KaRZWxyRo1wmKHOF5G5wTHrtxg8tnXylMc1PKOtaXIU4JJZ1l4x/7FwhPmg9M86PBPWr5zwUj2CVXC7wWlL/6M89Mlh8yXESMO3AIuAmEMKjqauPrgi9hAdI2oqnLZWCRL9gcHBida1y0DTXQhcwMv1ORrk65VFHtVgYAegrxu3NDoJiDyVaPZxDwTYRGjPII3va8GALAMVy5xou2ikzRvJjW7Gm3XoaqJCTCExN4m5i/Dqc81Gr4uT7OaeypYTUjnwCh7aMhsOTDJehefzjXhlkn//2eik+NivKx/BTJBEdT6MR97Wh/ns/VcK7QTmbjwbU2cwLngT7Ylq+uzhx54R9JMaSLhnw+/nIrcVkG77Hi3neShKeZmnl5DC9PuwIbtNvVge3Q+V0ws2zsL3z7ndz4tTMYFdvR/XbrnbEErTDLWrV6Lc3JHQMs0bYUyTBg5dThwCiuZ1evaT6BlMMLuSCVxdBGzXTBcvGwihFzZbyNoX+52DS5x+RbIEvd6KWOpQ6Ni+1GAawHDdNUiQTQFXRxLSHfc9fh7hE4qcD7PqHGsykYj7A0XqHCjbKKgWSkcAg==
```

Als u de gegevens-API wilt aanroepen, koppelt u het toegangstoken als een bearertoken aan de autorisatiekoptekst in uw HTTP-aanvraag. Hier volgt een voorbeeld.

```HTTP
HTTP/1.1
Authorization: Bearer EwAoA8l6BAAU ... 7PqHGsykYj7A0XqHCjbKKgWSkcAg==
Host: https://{cluster}.hr.talent.dynamics.com
GET https://{cluster}.hr.talent.dynamics.com/namespaces/{namespace_guid}/data/JobTypes
```

## <a name="register-a-new-application-by-using-the-azure-portal"></a>Een nieuwe toepassing registreren via de Azure-portal

1. Meld u aan bij de [Microsoft Azure-portal](https://portal.azure.com) met een werk- of schoolaccount of een persoonlijk Microsoft-account.

2. Als uw account toegang geeft tot meer dan één tenant, selecteert u uw-account in de rechterbovenhoek en stelt u uw portalsessie in op de gewenste Azure Active Directory-tenant (Azure AD).

3. Selecteer in het linkerdeelvenster de **Azure Active Directory**-service en selecteer vervolgens **App-registraties \> Nieuwe registratie**.

4. Wanneer de pagina **Een toepassing registreren** wordt weergegeven, voert u de registratiegegevens van uw toepassing in:

    - **Naam**: voer een herkenbare toepassingsnaam in die wordt weergegeven aan gebruikers van de app.
    - **Ondersteunde rekeningtypen**: selecteer de typen rekeningen die uw app moet ondersteunen.

        | Ondersteunde rekeningtypen | Beschrijving |
        |-------------------------|-------------|
        | Alleen accounts in deze organisatieadreslijst | Selecteer deze optie als u een LOB-app (Line-Of-Business) wilt maken. Deze optie is alleen beschikbaar als u de app in een adreslijst registreert.<p>Deze optie wordt toegewezen aan **Azure AD alleen enkele tenant**.</p><p>Deze optie is de standaardoptie, tenzij u de app registreert buiten een adreslijst. In dat geval is **Azure AD multi-tenant en persoonlijke Microsoft-accounts** de standaardoptie.</p> |
        | Accounts in een willekeurige organisatieadreslijst | Selecteer deze optie als u alle zakelijke en educatieve klanten wilt bereiken.<p>Deze optie wordt toegewezen aan **Azure AD alleen multi-tenant**.</p><p>Als u de app als **Azure AD alleen enkele tenant** hebt geregistreerd, kunt u de blade **Verificatie** gebruiken om de app bij te werken naar **Azure AD alleen multi-tenant** en vervolgens weer terug naar **Azure AD alleen enkele tenant**.</p> |
        | Rekeningen in een organisatieadreslijst en persoonlijke Microsoft-accounts | Selecteer deze optie als u de breedste groep klanten wilt bereiken.<p>Deze optie wordt toegewezen aan **Azure AD multi-tenant en persoonlijke Microsoft-accounts**.</p><p>Als u de app als **Azure AD multi tenant en persoonlijke Microsoft-accounts** hebt geregistreerd, kunt u deze instelling niet wijzigen in de gebruikersinterface. In plaats daarvan moet u de Application Manifest Editor gebruiken om de ondersteunde rekeningtypen te wijzigen.</p> |

    - **URI omleiden (optioneel)**: selecteer het type app dat u wilt maken: **Web** of **Openbare client (mobiel en bureaublad**). Voer vervolgens de omleidings-URI (of antwoord-URL) in voor de app.

        - Geef voor webapps de basis-URL van de app op. Zo kan `http://localhost:31544` bijvoorbeeld de URL zijn voor een webapp zijn die op uw lokale computer wordt uitgevoerd. Gebruikers kunnen deze URL gebruiken om zich aan te melden bij een webclient-app.
        - Geef voor openbare clientapps de URI op die Azure AD gebruikt wordt voor het retourneren van tokenantwoorden. Voer een waarde in die specifiek is voor uw app, zoals `myapp://auth`.

        Zie de QuickStarts in [Microsoft-identiteitsplatform (voorheen Azure Active Directory voor ontwikkelaars)](https://docs.microsoft.com/azure/active-directory/develop/#quickstarts) voor specifieke voorbeelden van webapps of native apps.

5. Selecteer **Een machtiging toevoegen** onder **API-machtigingen**. Zoek vervolgens op het tabblad **API's die mijn organisatie gebruikt** naar **Dynamics 365 Human Resources** en voeg de machtiging **gebruikers\_imitatie** toe aan uw app. De toepassings-id voor Human Resources is f9be0c49-aa22-4ec6-911a-c5da515226ffis. Gebruik deze id om ervoor te zorgen dat u de juiste toepassing hebt gekozen.

6. Selecteer **Registreren**.

   [![Een nieuwe app registreren in de Azure-portal](media/api-new-app-registration-expanded.png)](media/api-new-app-registration-expanded.png#lightbox)

Azure AD wijst een unieke toepassings-id (client-id) toe aan uw app en brengt u naar de pagina **Overzicht** van uw app. Als u meer mogelijkheden aan uw app wilt toevoegen, kunt u andere configuratieopties selecteren, zoals opties voor huisstijl en voor certificaten en geheimen.

## <a name="retrieving-an-access-token"></a>Een toegangstoken ophalen

De specifieke informatie over hoe u een toegangstoken ophaalt voor het aanroepen van de gegevens-API van Human Resources is afhankelijk van de technologieën die u gebruikt om de clienttoepassing te ontwikkelen. Zo kunt u bijvoorbeeld [testen met een hulpprogramma van derden](../fin-ops-core/dev-itpro/data-entities/third-party-service-test.md) (zoals Postman), een C#-consoletoepassing of -webservice ontwikkelen of een Javascript/TypeScript-client bouwen.

Voorbeeld van C#-clienttoepassing:
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

Wanneer u een toegangstoken hebt opgehaald, geeft u het token in de autorisatiekoptekst door als een bearertoken met elke aanvraag die u naar de gegevens-API verzendt, zoals hierboven is beschreven.


[!INCLUDE[footer-include](../includes/footer-banner.md)]