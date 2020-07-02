---
title: Conformiteit van cookie
description: In dit onderwerp worden overwegingen voor compliance op het gebied van cookies en het standaardbeleid in Microsoft Dynamics 365 Commerce beschreven.
author: BrianShook
manager: annbe
ms.date: 06/12/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: e1fa016dc9f46b048220f0f83e4b0783087de91e
ms.sourcegitcommit: c66c4c67a21e7d7d3a94a3fd766c3184b6e65c4e
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/12/2020
ms.locfileid: "3446908"
---
# <a name="cookie-compliance"></a><span data-ttu-id="d7ccc-103">Conformiteit van cookie</span><span class="sxs-lookup"><span data-stu-id="d7ccc-103">Cookie compliance</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="d7ccc-104">In dit onderwerp worden overwegingen voor compliance op het gebied van cookies en het standaardbeleid in Microsoft Dynamics 365 Commerce beschreven.</span><span class="sxs-lookup"><span data-stu-id="d7ccc-104">This topic describes considerations for cookie compliance and the default policies that are included in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="d7ccc-105">Overzicht</span><span class="sxs-lookup"><span data-stu-id="d7ccc-105">Overview</span></span>

<span data-ttu-id="d7ccc-106">Privacy is een belangrijke factor wanneer trackingtechnologieën worden gebruikt die invloed hebben op e-Commerce-klanten.</span><span class="sxs-lookup"><span data-stu-id="d7ccc-106">Privacy is an important factor when tracking technologies that affect e-Commerce customers.</span></span> <span data-ttu-id="d7ccc-107">Vanwege normen voor privacycompliance, zoals de AVG (Algemene Verordening Gegevensbescherming) in de EU (Europese Unie), moeten elektronische privacyrichtlijnen worden overwogen voor elke site die nu actief is.</span><span class="sxs-lookup"><span data-stu-id="d7ccc-107">Because of privacy compliance standards such as the General Data Protection Regulation (GDPR) in the European Union (EU), electronic privacy guidelines must be considered for any site that is active today.</span></span> <span data-ttu-id="d7ccc-108">Omdat veel e-Commerce-sites standaard wereldwijd toegankelijk zijn, is het belangrijk dat u de compliancenormen voor uw e-Commerce-site controleert.</span><span class="sxs-lookup"><span data-stu-id="d7ccc-108">Because many e-Commerce sites are globally accessible by default, it's important that you review the compliance standards for your e-Commerce site.</span></span>

<span data-ttu-id="d7ccc-109">Bezoek het [Microsoft Vertrouwenscentrum](https://www.microsoft.com/trust-center) voor meer informatie over de basisbeginselen die Microsoft gebruikt voor cookiecompliance.</span><span class="sxs-lookup"><span data-stu-id="d7ccc-109">To learn more about the basic principles that Microsoft uses for cookie compliance, visit the [Microsoft Trust Center](https://www.microsoft.com/trust-center).</span></span> <span data-ttu-id="d7ccc-110">Op die site vindt u ook meer informatie over de compliancegebieden en privacy.</span><span class="sxs-lookup"><span data-stu-id="d7ccc-110">On that site, you can also get more information about areas of compliance and privacy.</span></span>

<span data-ttu-id="d7ccc-111">In de volgende tabel wordt de huidige verwijzingslijst van cookies weergegeven die door Dynamics 365 Commerce-sites zijn geplaatst.</span><span class="sxs-lookup"><span data-stu-id="d7ccc-111">The following table shows the current reference list of cookies placed by Dynamics 365 Commerce sites.</span></span>

| <span data-ttu-id="d7ccc-112">Cookienaam</span><span class="sxs-lookup"><span data-stu-id="d7ccc-112">Cookie name</span></span>                               | <span data-ttu-id="d7ccc-113">Gebruik</span><span class="sxs-lookup"><span data-stu-id="d7ccc-113">Usage</span></span>                                                        |
| ------------------------------------------- | ------------------------------------------------------------ |
| <span data-ttu-id="d7ccc-114">.AspNet.Cookies</span><span class="sxs-lookup"><span data-stu-id="d7ccc-114">.AspNet.Cookies</span></span>                             | <span data-ttu-id="d7ccc-115">Microsoft Azure Active Directory (Azure AD)-verificatiecookies opslaan voor eenmalige aanmelding (SSO).</span><span class="sxs-lookup"><span data-stu-id="d7ccc-115">Store Microsoft Azure Active Directory (Azure AD) authentication cookies for single sign-on (SSO).</span></span> <span data-ttu-id="d7ccc-116">Hiermee wordt gecodeerde informatie over gebruikers opgeslagen (naam, achternaam, e-mail).</span><span class="sxs-lookup"><span data-stu-id="d7ccc-116">Stores encrypted user principal information (name, surname, email).</span></span> |
| <span data-ttu-id="d7ccc-117">&#95;msdyn365___cart&#95;</span><span class="sxs-lookup"><span data-stu-id="d7ccc-117">&#95;msdyn365___cart&#95;</span></span>                           | <span data-ttu-id="d7ccc-118">Winkelwagen-id wordt gebruikt om lijst met producten op te halen die aan het winkelwagenexemplaar zijn toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="d7ccc-118">Store cart ID used to obtain list of products added to cart instance.</span></span> |
| <span data-ttu-id="d7ccc-119">&#95;msdyn365___ucc&#95;</span><span class="sxs-lookup"><span data-stu-id="d7ccc-119">&#95;msdyn365___ucc&#95;</span></span>                            | <span data-ttu-id="d7ccc-120">Toestemming bijhouden voor cookienaleving.</span><span class="sxs-lookup"><span data-stu-id="d7ccc-120">Cookie compliance consent tracking.</span></span>                          |
| <span data-ttu-id="d7ccc-121">ai_session</span><span class="sxs-lookup"><span data-stu-id="d7ccc-121">ai_session</span></span>                                  | <span data-ttu-id="d7ccc-122">Detecteert in hoeveel sessies met gebruikersactiviteit bepaalde pagina's en functies van de app zijn opgenomen.</span><span class="sxs-lookup"><span data-stu-id="d7ccc-122">Detects how many sessions of user activity have included certain pages and features of the app.</span></span> |
| <span data-ttu-id="d7ccc-123">ai_user</span><span class="sxs-lookup"><span data-stu-id="d7ccc-123">ai_user</span></span>                                     | <span data-ttu-id="d7ccc-124">Detecteert hoeveel mensen de app en de bijbehorende functies hebben gebruikt.</span><span class="sxs-lookup"><span data-stu-id="d7ccc-124">Detects how many people used the app and its features.</span></span> <span data-ttu-id="d7ccc-125">Gebruikers worden geteld met behulp van anonieme id's.</span><span class="sxs-lookup"><span data-stu-id="d7ccc-125">Users are counted using anonymous IDs.</span></span> |
| <span data-ttu-id="d7ccc-126">b2cru</span><span class="sxs-lookup"><span data-stu-id="d7ccc-126">b2cru</span></span>                                       | <span data-ttu-id="d7ccc-127">De omleidings-URL wordt dynamisch opgeslagen.</span><span class="sxs-lookup"><span data-stu-id="d7ccc-127">Stores redirect URL dynamically.</span></span>                              |
| <span data-ttu-id="d7ccc-128">JSESSIONID</span><span class="sxs-lookup"><span data-stu-id="d7ccc-128">JSESSIONID</span></span>                                  | <span data-ttu-id="d7ccc-129">Wordt gebruikt door betalingsconnector Adyen om gebruikerssessie op te slaan.</span><span class="sxs-lookup"><span data-stu-id="d7ccc-129">Used by payment connector Adyen to store user session.</span></span>       |
| <span data-ttu-id="d7ccc-130">OpenIdConnect.nonce.&#42;</span><span class="sxs-lookup"><span data-stu-id="d7ccc-130">OpenIdConnect.nonce.&#42;</span></span>                       | <span data-ttu-id="d7ccc-131">Authenticatie</span><span class="sxs-lookup"><span data-stu-id="d7ccc-131">Authentication</span></span>                                               |
| <span data-ttu-id="d7ccc-132">x-ms-cpim-cache:.&#42;</span><span class="sxs-lookup"><span data-stu-id="d7ccc-132">x-ms-cpim-cache:.&#42;</span></span>                          | <span data-ttu-id="d7ccc-133">Wordt gebruikt voor het onderhouden van de aanvraagstatus.</span><span class="sxs-lookup"><span data-stu-id="d7ccc-133">Used for maintaining the request state.</span></span>                      |
| <span data-ttu-id="d7ccc-134">x-ms-cpim-csrf</span><span class="sxs-lookup"><span data-stu-id="d7ccc-134">x-ms-cpim-csrf</span></span>                              | <span data-ttu-id="d7ccc-135">CRSF-token (aanvraagvervalsing op meerdere sites) wordt gebruikt voor de CRSF-beveiliging.</span><span class="sxs-lookup"><span data-stu-id="d7ccc-135">Cross-site request forgery (CRSF) token used for protection from CRSF.</span></span>     |
| <span data-ttu-id="d7ccc-136">x-ms-cpim-dc</span><span class="sxs-lookup"><span data-stu-id="d7ccc-136">x-ms-cpim-dc</span></span>                                | <span data-ttu-id="d7ccc-137">Wordt gebruikt om aanvragen naar het toepasselijke serverexemplaar voor productieverificatie te routeren.</span><span class="sxs-lookup"><span data-stu-id="d7ccc-137">Used to route requests to the appropriate production authentication server instance.</span></span> |
| <span data-ttu-id="d7ccc-138">x-ms-cpim-rc.&#42;</span><span class="sxs-lookup"><span data-stu-id="d7ccc-138">x-ms-cpim-rc.&#42;</span></span>                              | <span data-ttu-id="d7ccc-139">Wordt gebruikt om aanvragen naar het toepasselijke serverexemplaar voor productieverificatie te routeren.</span><span class="sxs-lookup"><span data-stu-id="d7ccc-139">Used to route requests to the appropriate production authentication server instance.</span></span> |
| <span data-ttu-id="d7ccc-140">x-ms-cpim-slice</span><span class="sxs-lookup"><span data-stu-id="d7ccc-140">x-ms-cpim-slice</span></span>                             | <span data-ttu-id="d7ccc-141">Wordt gebruikt om aanvragen naar het toepasselijke serverexemplaar voor productieverificatie te routeren.</span><span class="sxs-lookup"><span data-stu-id="d7ccc-141">Used to route requests to the appropriate production authentication server instance.</span></span> |
| <span data-ttu-id="d7ccc-142">x-ms-cpim-sso:rushmoreb2c.onmicrosoft.com_0</span><span class="sxs-lookup"><span data-stu-id="d7ccc-142">x-ms-cpim-sso:rushmoreb2c.onmicrosoft.com_0</span></span> | <span data-ttu-id="d7ccc-143">Wordt gebruikt voor het onderhouden van de SSO-sessie.</span><span class="sxs-lookup"><span data-stu-id="d7ccc-143">Used for maintaining the SSO session.</span></span>                        |
| <span data-ttu-id="d7ccc-144">x-ms-cpim-trans</span><span class="sxs-lookup"><span data-stu-id="d7ccc-144">x-ms-cpim-trans</span></span>                             | <span data-ttu-id="d7ccc-145">Wordt gebruikt voor het traceren van transacties (het aantal geopende tabbladen dat wordt geverifieerd tegen een Business-to-consumer-site (B2C)), inclusief de huidige transactie.</span><span class="sxs-lookup"><span data-stu-id="d7ccc-145">Used for tracking transactions (the number of open tabs authenticating against a business-to-consumer (B2C) site), including the current transaction.</span></span> |

## <a name="additional-resources"></a><span data-ttu-id="d7ccc-146">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="d7ccc-146">Additional resources</span></span>

[<span data-ttu-id="d7ccc-147">Toegankelijksfuncties en -voorzieningen</span><span class="sxs-lookup"><span data-stu-id="d7ccc-147">Accessibility features and capabilities</span></span>](accessibility.md)

[<span data-ttu-id="d7ccc-148">Conformiteitsoverzicht</span><span class="sxs-lookup"><span data-stu-id="d7ccc-148">Compliance overview</span></span>](compliance-overview.md)

[<span data-ttu-id="d7ccc-149">Een pagina met het privacybeleid toevoegen</span><span class="sxs-lookup"><span data-stu-id="d7ccc-149">Add a privacy policy page</span></span>](add-privacy-page.md)

[<span data-ttu-id="d7ccc-150">Gebruikers-id's vervangen die zijn gekoppeld aan wijzigingen in bijgehouden inhoud</span><span class="sxs-lookup"><span data-stu-id="d7ccc-150">Replace user IDs associated with tracked content changes</span></span>](replace-IDs-tracked-changes.md)
