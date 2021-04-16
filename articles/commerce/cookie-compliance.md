---
title: Conformiteit van cookie
description: In dit onderwerp worden overwegingen voor compliance op het gebied van cookies en het standaardbeleid in Microsoft Dynamics 365 Commerce beschreven.
author: BrianShook
ms.date: 08/31/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 2cc2089bc3052c0c59cb0414f8301123a9a30df2
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/31/2021
ms.locfileid: "5796022"
---
# <a name="cookie-compliance"></a><span data-ttu-id="fc790-103">Conformiteit van cookie</span><span class="sxs-lookup"><span data-stu-id="fc790-103">Cookie compliance</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="fc790-104">In dit onderwerp worden overwegingen voor compliance op het gebied van cookies en het standaardbeleid in Microsoft Dynamics 365 Commerce beschreven.</span><span class="sxs-lookup"><span data-stu-id="fc790-104">This topic describes considerations for cookie compliance and the default policies that are included in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="fc790-105">Privacy is een belangrijke factor wanneer trackingtechnologieën worden gebruikt die invloed hebben op e-Commerce-klanten.</span><span class="sxs-lookup"><span data-stu-id="fc790-105">Privacy is an important factor when tracking technologies that affect e-Commerce customers.</span></span> <span data-ttu-id="fc790-106">Vanwege normen voor privacycompliance, zoals de AVG (Algemene Verordening Gegevensbescherming) in de EU (Europese Unie), moeten elektronische privacyrichtlijnen worden overwogen voor elke site die nu actief is.</span><span class="sxs-lookup"><span data-stu-id="fc790-106">Because of privacy compliance standards such as the General Data Protection Regulation (GDPR) in the European Union (EU), electronic privacy guidelines must be considered for any site that is active today.</span></span> <span data-ttu-id="fc790-107">Omdat veel e-Commerce-sites standaard wereldwijd toegankelijk zijn, is het belangrijk dat u de compliancenormen voor uw e-Commerce-site controleert.</span><span class="sxs-lookup"><span data-stu-id="fc790-107">Because many e-Commerce sites are globally accessible by default, it's important that you review the compliance standards for your e-Commerce site.</span></span>

<span data-ttu-id="fc790-108">Bezoek het [Microsoft Vertrouwenscentrum](https://www.microsoft.com/trust-center) voor meer informatie over de basisbeginselen die Microsoft gebruikt voor cookiecompliance.</span><span class="sxs-lookup"><span data-stu-id="fc790-108">To learn more about the basic principles that Microsoft uses for cookie compliance, visit the [Microsoft Trust Center](https://www.microsoft.com/trust-center).</span></span> <span data-ttu-id="fc790-109">Op die site vindt u ook meer informatie over de compliancegebieden en privacy.</span><span class="sxs-lookup"><span data-stu-id="fc790-109">On that site, you can also get more information about areas of compliance and privacy.</span></span>

<span data-ttu-id="fc790-110">In de volgende tabel wordt de huidige verwijzingslijst van cookies weergegeven die door Dynamics 365 Commerce-sites zijn geplaatst.</span><span class="sxs-lookup"><span data-stu-id="fc790-110">The following table shows the current reference list of cookies placed by Dynamics 365 Commerce sites.</span></span>

| <span data-ttu-id="fc790-111">Cookienaam</span><span class="sxs-lookup"><span data-stu-id="fc790-111">Cookie name</span></span>                               | <span data-ttu-id="fc790-112">Gebruik</span><span class="sxs-lookup"><span data-stu-id="fc790-112">Usage</span></span>                                                        |
| ------------------------------------------- | ------------------------------------------------------------ |
| <span data-ttu-id="fc790-113">.AspNet.Cookies</span><span class="sxs-lookup"><span data-stu-id="fc790-113">.AspNet.Cookies</span></span>                             | <span data-ttu-id="fc790-114">Microsoft Azure Active Directory (Azure AD)-verificatiecookies opslaan voor eenmalige aanmelding (SSO).</span><span class="sxs-lookup"><span data-stu-id="fc790-114">Store Microsoft Azure Active Directory (Azure AD) authentication cookies for single sign-on (SSO).</span></span> <span data-ttu-id="fc790-115">Hiermee wordt gecodeerde informatie over gebruikers opgeslagen (naam, achternaam, e-mail).</span><span class="sxs-lookup"><span data-stu-id="fc790-115">Stores encrypted user principal information (name, surname, email).</span></span> |
| <span data-ttu-id="fc790-116">&#95;msdyn365___cart&#95;</span><span class="sxs-lookup"><span data-stu-id="fc790-116">&#95;msdyn365___cart&#95;</span></span>                           | <span data-ttu-id="fc790-117">Winkelwagen-id wordt gebruikt om lijst met producten op te halen die aan het winkelwagenexemplaar zijn toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="fc790-117">Store cart ID used to obtain list of products added to cart instance.</span></span> |
| <span data-ttu-id="fc790-118">&#95;msdyn365___ucc&#95;</span><span class="sxs-lookup"><span data-stu-id="fc790-118">&#95;msdyn365___ucc&#95;</span></span>                            | <span data-ttu-id="fc790-119">Toestemming bijhouden voor cookienaleving.</span><span class="sxs-lookup"><span data-stu-id="fc790-119">Cookie compliance consent tracking.</span></span>                          |
| <span data-ttu-id="fc790-120">ai_session</span><span class="sxs-lookup"><span data-stu-id="fc790-120">ai_session</span></span>                                  | <span data-ttu-id="fc790-121">Detecteert in hoeveel sessies met gebruikersactiviteit bepaalde pagina's en functies van de app zijn opgenomen.</span><span class="sxs-lookup"><span data-stu-id="fc790-121">Detects how many sessions of user activity have included certain pages and features of the app.</span></span> |
| <span data-ttu-id="fc790-122">ai_user</span><span class="sxs-lookup"><span data-stu-id="fc790-122">ai_user</span></span>                                     | <span data-ttu-id="fc790-123">Detecteert hoeveel mensen de app en de bijbehorende functies hebben gebruikt.</span><span class="sxs-lookup"><span data-stu-id="fc790-123">Detects how many people used the app and its features.</span></span> <span data-ttu-id="fc790-124">Gebruikers worden geteld met behulp van anonieme id's.</span><span class="sxs-lookup"><span data-stu-id="fc790-124">Users are counted using anonymous IDs.</span></span> |
| <span data-ttu-id="fc790-125">b2cru</span><span class="sxs-lookup"><span data-stu-id="fc790-125">b2cru</span></span>                                       | <span data-ttu-id="fc790-126">De omleidings-URL wordt dynamisch opgeslagen.</span><span class="sxs-lookup"><span data-stu-id="fc790-126">Stores redirect URL dynamically.</span></span>                              |
| <span data-ttu-id="fc790-127">JSESSIONID</span><span class="sxs-lookup"><span data-stu-id="fc790-127">JSESSIONID</span></span>                                  | <span data-ttu-id="fc790-128">Wordt gebruikt door betalingsconnector Adyen om gebruikerssessie op te slaan.</span><span class="sxs-lookup"><span data-stu-id="fc790-128">Used by payment connector Adyen to store user session.</span></span>       |
| <span data-ttu-id="fc790-129">OpenIdConnect.nonce.&#42;</span><span class="sxs-lookup"><span data-stu-id="fc790-129">OpenIdConnect.nonce.&#42;</span></span>                       | <span data-ttu-id="fc790-130">Authenticatie</span><span class="sxs-lookup"><span data-stu-id="fc790-130">Authentication</span></span>                                               |
| <span data-ttu-id="fc790-131">x-ms-cpim-cache:.&#42;</span><span class="sxs-lookup"><span data-stu-id="fc790-131">x-ms-cpim-cache:.&#42;</span></span>                          | <span data-ttu-id="fc790-132">Wordt gebruikt voor het onderhouden van de aanvraagstatus.</span><span class="sxs-lookup"><span data-stu-id="fc790-132">Used for maintaining the request state.</span></span>                      |
| <span data-ttu-id="fc790-133">x-ms-cpim-csrf</span><span class="sxs-lookup"><span data-stu-id="fc790-133">x-ms-cpim-csrf</span></span>                              | <span data-ttu-id="fc790-134">CRSF-token (aanvraagvervalsing op meerdere sites) wordt gebruikt voor de CRSF-beveiliging.</span><span class="sxs-lookup"><span data-stu-id="fc790-134">Cross-site request forgery (CRSF) token used for protection from CRSF.</span></span>     |
| <span data-ttu-id="fc790-135">x-ms-cpim-dc</span><span class="sxs-lookup"><span data-stu-id="fc790-135">x-ms-cpim-dc</span></span>                                | <span data-ttu-id="fc790-136">Wordt gebruikt om aanvragen naar het toepasselijke serverexemplaar voor productieverificatie te routeren.</span><span class="sxs-lookup"><span data-stu-id="fc790-136">Used to route requests to the appropriate production authentication server instance.</span></span> |
| <span data-ttu-id="fc790-137">x-ms-cpim-rc.&#42;</span><span class="sxs-lookup"><span data-stu-id="fc790-137">x-ms-cpim-rc.&#42;</span></span>                              | <span data-ttu-id="fc790-138">Wordt gebruikt om aanvragen naar het toepasselijke serverexemplaar voor productieverificatie te routeren.</span><span class="sxs-lookup"><span data-stu-id="fc790-138">Used to route requests to the appropriate production authentication server instance.</span></span> |
| <span data-ttu-id="fc790-139">x-ms-cpim-slice</span><span class="sxs-lookup"><span data-stu-id="fc790-139">x-ms-cpim-slice</span></span>                             | <span data-ttu-id="fc790-140">Wordt gebruikt om aanvragen naar het toepasselijke serverexemplaar voor productieverificatie te routeren.</span><span class="sxs-lookup"><span data-stu-id="fc790-140">Used to route requests to the appropriate production authentication server instance.</span></span> |
| <span data-ttu-id="fc790-141">x-ms-cpim-sso:rushmoreb2c.onmicrosoft.com_0</span><span class="sxs-lookup"><span data-stu-id="fc790-141">x-ms-cpim-sso:rushmoreb2c.onmicrosoft.com_0</span></span> | <span data-ttu-id="fc790-142">Wordt gebruikt voor het onderhouden van de SSO-sessie.</span><span class="sxs-lookup"><span data-stu-id="fc790-142">Used for maintaining the SSO session.</span></span>                        |
| <span data-ttu-id="fc790-143">x-ms-cpim-trans</span><span class="sxs-lookup"><span data-stu-id="fc790-143">x-ms-cpim-trans</span></span>                             | <span data-ttu-id="fc790-144">Wordt gebruikt voor het traceren van transacties (het aantal geopende tabbladen dat wordt geverifieerd tegen een Business-to-consumer-site (B2C)), inclusief de huidige transactie.</span><span class="sxs-lookup"><span data-stu-id="fc790-144">Used for tracking transactions (the number of open tabs authenticating against a business-to-consumer (B2C) site), including the current transaction.</span></span> |

## <a name="site-user-cookie-consent-on-an-e-commerce-site"></a><span data-ttu-id="fc790-145">Cookietoestemming van sitegebruiker op een e-Commerce-site</span><span class="sxs-lookup"><span data-stu-id="fc790-145">Site user cookie consent on an e-Commerce site</span></span> 

<span data-ttu-id="fc790-146">Als een functie of module van een e-Commerce-site een niet-essentiële cookie gebruikt, moet de toestemming van de sitegebruiker worden verkregen voordat de cookie wordt gevolgd.</span><span class="sxs-lookup"><span data-stu-id="fc790-146">If an e-Commerce site feature or module uses a non-essential cookie, a site user's consent must be obtained before the cookie is tracked.</span></span> <span data-ttu-id="fc790-147">Als u wilt dat sitegebruikers cookietoestemming op de e-Commerce-site, moet een auteur van een site een cookietoestemmingsmodule toevoegen en configureren in de koptekstmodule van de pagina om ervoor te zorgen dat de toestemming wordt gevraagd en ontvangen.</span><span class="sxs-lookup"><span data-stu-id="fc790-147">To allow site users to provide cookie consent on the e-Commerce site, a site author must add and configure a cookie consent module in the page's header module to ensure that the consent is prompted for and received.</span></span> <span data-ttu-id="fc790-148">Toestemming van de sitegebruiker moet worden verleend voordat een functie of module met een niet-essentiële cookie kan worden weergegeven op een sitepagina.</span><span class="sxs-lookup"><span data-stu-id="fc790-148">Site user consent must be given before a feature or module using a non-essential cookie can be rendered on a site page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="fc790-149">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="fc790-149">Additional resources</span></span>

[<span data-ttu-id="fc790-150">Toegankelijksfuncties en -voorzieningen</span><span class="sxs-lookup"><span data-stu-id="fc790-150">Accessibility features and capabilities</span></span>](accessibility.md)

[<span data-ttu-id="fc790-151">Conformiteitsoverzicht</span><span class="sxs-lookup"><span data-stu-id="fc790-151">Compliance overview</span></span>](compliance-overview.md)

[<span data-ttu-id="fc790-152">Een pagina met het privacybeleid toevoegen</span><span class="sxs-lookup"><span data-stu-id="fc790-152">Add a privacy policy page</span></span>](add-privacy-page.md)

[<span data-ttu-id="fc790-153">Gebruikers-id's vervangen die zijn gekoppeld aan wijzigingen in bijgehouden inhoud</span><span class="sxs-lookup"><span data-stu-id="fc790-153">Replace user IDs associated with tracked content changes</span></span>](replace-IDs-tracked-changes.md)

[<span data-ttu-id="fc790-154">Cookietoestemmingsmodule</span><span class="sxs-lookup"><span data-stu-id="fc790-154">Cookie consent module</span></span>](cookie-consent-module.md) 
 
[<span data-ttu-id="fc790-155">Koptekstmodule</span><span class="sxs-lookup"><span data-stu-id="fc790-155">Header module</span></span>](author-header-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
