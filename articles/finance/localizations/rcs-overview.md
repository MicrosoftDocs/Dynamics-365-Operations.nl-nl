---
title: Regulatory Configuration Service
description: In dit onderwerp wordt een overzicht gegeven van de functies van RCS (Regulatory Configuration Service) en wordt uitgelegd hoe u toegang krijgt tot de service.
author: JaneA07
ms.date: 06/04/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RCS, Regulatory Configuration Services, Localization
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-02-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: 7f946988f124c814452e1774c700d5c7354f39b0
ms.sourcegitcommit: 60afcd85b3b5b9e5e8981ebbb57c0161cf05e54b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/09/2021
ms.locfileid: "6216557"
---
# <a name="regulatory-configuration-service"></a><span data-ttu-id="c21dc-103">Regulatory Configuration Service</span><span class="sxs-lookup"><span data-stu-id="c21dc-103">Regulatory Configuration Service</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c21dc-104">Regulatory Configuration Service (RCS) is een zelfstandige ontwerpfunctie en lifecyclebeheerservice voor globalisatiefunctionaliteit zonder code/met weinig code.</span><span class="sxs-lookup"><span data-stu-id="c21dc-104">Regulatory Configuration Service (RCS) is a standalone designer and lifecycle management service for no-code/low-code globalization functionality.</span></span> <span data-ttu-id="c21dc-105">Met RCS kunnen globalisatiepartijen belangrijke globalisatiegebieden van belasting, e-facturering, wettelijke rapportage, bankdocumenten en bedrijfsdocumenten uitbreiden en aanpassen zonder ontwikkelaars.</span><span class="sxs-lookup"><span data-stu-id="c21dc-105">RCS lets globalization stakeholders extend and customize key globalization areas of tax, e-invoicing, regulatory reporting, banking, and business documents without having to involve developers.</span></span> <span data-ttu-id="c21dc-106">Door deze globalisatie zonder code/met weinig code wordt globalisatie eenvoudiger, sneller en effectiever om te maken of uit te breiden.</span><span class="sxs-lookup"><span data-stu-id="c21dc-106">This no-code/low-code globalization approach makes globalization easier, faster, and more cost effective to create or extend.</span></span>

<span data-ttu-id="c21dc-107">RCS biedt de volgende mogelijkheden:</span><span class="sxs-lookup"><span data-stu-id="c21dc-107">RCS provides the following capabilities:</span></span>

- <span data-ttu-id="c21dc-108">Ondersteuning voor alle functionaliteit die wordt geleverd door Elektronische rapportage (ER).</span><span class="sxs-lookup"><span data-stu-id="c21dc-108">Support for all functionality that is provided by Electronic reporting (ER).</span></span>
- <span data-ttu-id="c21dc-109">Een vereiste voor het configureren van nieuwe microservices voor globalisatie.</span><span class="sxs-lookup"><span data-stu-id="c21dc-109">A prerequisite to configure new globalization microservices.</span></span>
- <span data-ttu-id="c21dc-110">Ondersteuning voor Elektronische facturering.</span><span class="sxs-lookup"><span data-stu-id="c21dc-110">Support for Electronic Invoicing.</span></span> <span data-ttu-id="c21dc-111">Zie [Elektronische facturering](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/electronic-invoicing-add-on-dynamics-365-ga) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="c21dc-111">For more information, see [Electronic Invoicing](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/electronic-invoicing-add-on-dynamics-365-ga).</span></span>
- <span data-ttu-id="c21dc-112">Ondersteunt Belastingberekening.</span><span class="sxs-lookup"><span data-stu-id="c21dc-112">Supports for Tax Calculation.</span></span> <span data-ttu-id="c21dc-113">Zie voor meer informatie [Belastingservice](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/tax-service-preview).</span><span class="sxs-lookup"><span data-stu-id="c21dc-113">For more information, see [Tax service](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/tax-service-preview).</span></span>
- <span data-ttu-id="c21dc-114">Ondersteuning voor nieuwe functionaliteit voor globalisatiefuncties die het levenscyclusbeheer van meerdere componentfuncties vereenvoudigt en extra mogelijkheden biedt voor het configureren van acties en het instellen van functieparameters.</span><span class="sxs-lookup"><span data-stu-id="c21dc-114">Support for new globalization feature functionality that simplifies the lifecycle management of multi-component features and provides extra capability to configure actions and set up feature parameters.</span></span> <span data-ttu-id="c21dc-115">Zie [Regulatory Configuration Service – vereenvoudigd globalisatiefunctiebeheer voor globalisatieservices](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/regulatory-configuration-service-simplified-globalization-feature-management-globalization-services)  voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="c21dc-115">For more information, see [Regulatory Configuration Service – simplified globalization feature management for globalization services](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/regulatory-configuration-service-simplified-globalization-feature-management-globalization-services).</span></span>
- <span data-ttu-id="c21dc-116">Ondersteuning voor gecentraliseerde publicatie, opslag en het delen van aangepaste configuraties in de Algemene opslagplaats om configuratiebeheer te vereenvoudigen zonder dat Microsoft Dynamics Lifecycle Services moet worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="c21dc-116">Support for centralized publication, storage, and sharing of custom configurations in the Global repository to simplify configuration management without requiring the use of Microsoft Dynamics Lifecycle Services (LCS).</span></span>

## <a name="access-rcs"></a><span data-ttu-id="c21dc-117">Toegang tot RCS</span><span class="sxs-lookup"><span data-stu-id="c21dc-117">Access RCS</span></span>

<span data-ttu-id="c21dc-118">U kunt zich registreren voor RCS of u aanmelden via de pagina [Regulatory Configuration Service](https://marketing.configure.global.dynamics.com/).</span><span class="sxs-lookup"><span data-stu-id="c21dc-118">You can sign up for or sign in to RCS from the [Regulatory Configuration Service page](https://marketing.configure.global.dynamics.com/).</span></span>

![Registreren/aanmelden bij RCS](media/202103_RCS%20Marketing%20page_updated_1.jpg)

<span data-ttu-id="c21dc-120">Controleer op de pagina **Regulatory Configuration Service** de aanvullende algemene voorwaarden voor gebruik van de service. Accepteer deze en selecteer een van de volgende knoppen:</span><span class="sxs-lookup"><span data-stu-id="c21dc-120">On the **Regulatory Configuration Service** page, review and accept the supplemental terms and conditions for use of the service, and then select one of the following buttons:</span></span>

- <span data-ttu-id="c21dc-121">**Registreren** als u een nieuwe gebruiker van de service bent en u een bedrijfse-mailadres gebruikt om uw organisatie een serviceomgeving in te richten</span><span class="sxs-lookup"><span data-stu-id="c21dc-121">**Sign up** if you're a first-time user of the service, and you're using a business email address to provision your organization a service environment</span></span>
- <span data-ttu-id="c21dc-122">**Aanmelden** als u zich eerder hebt aangemeld voor de service en u toegang wilt krijgen tot uw organisatieomgeving</span><span class="sxs-lookup"><span data-stu-id="c21dc-122">**Sign in** if you've previously signed up for the service, and you want to access your organization environment</span></span>

## <a name="regional-availability"></a><span data-ttu-id="c21dc-123">Regionale beschikbaarheid</span><span class="sxs-lookup"><span data-stu-id="c21dc-123">Regional availability</span></span>

<span data-ttu-id="c21dc-124">RCS is algemeen beschikbaar in de volgende regio's:</span><span class="sxs-lookup"><span data-stu-id="c21dc-124">RCS is generally available in the following regions:</span></span>

- <span data-ttu-id="c21dc-125">Verenigde Staten</span><span class="sxs-lookup"><span data-stu-id="c21dc-125">United States</span></span>
- <span data-ttu-id="c21dc-126">India</span><span class="sxs-lookup"><span data-stu-id="c21dc-126">India</span></span>
- <span data-ttu-id="c21dc-127">Frankrijk</span><span class="sxs-lookup"><span data-stu-id="c21dc-127">France</span></span>
- <span data-ttu-id="c21dc-128">Europa</span><span class="sxs-lookup"><span data-stu-id="c21dc-128">Europe</span></span>

<span data-ttu-id="c21dc-129">Zie [Dynamics 365 en Power Platform: beschikbaarheid, gegevenslocatie, taal en lokalisatie](https://aka.ms/dynamics_365_international_availability_deck) voor een volledige lijst met regio's.</span><span class="sxs-lookup"><span data-stu-id="c21dc-129">For a complete list of regions, see [Dynamics 365 and Power Platform: Availability, data location, language, and localization](https://aka.ms/dynamics_365_international_availability_deck).</span></span>

## <a name="rcs-default-company"></a><span data-ttu-id="c21dc-130">RCS-standaardbedrijf</span><span class="sxs-lookup"><span data-stu-id="c21dc-130">RCS default company</span></span>

<span data-ttu-id="c21dc-131">Ontwerptijdfunctionaliteit die wordt gebruikt in RCS, wordt gedeeld door alle bedrijven.</span><span class="sxs-lookup"><span data-stu-id="c21dc-131">Design time functionality that is used in RCS is shared across all companies.</span></span> <span data-ttu-id="c21dc-132">Er is geen bedrijfsspecifieke functionaliteit.</span><span class="sxs-lookup"><span data-stu-id="c21dc-132">There is no company-specific functionality.</span></span> <span data-ttu-id="c21dc-133">Daarom is het raadzaam dat u één bedrijf, **DAT**, gebruikt voor uw RCS-omgeving.</span><span class="sxs-lookup"><span data-stu-id="c21dc-133">Therefore, we recommend that you use one company, **DAT**, with your RCS environment.</span></span>

<span data-ttu-id="c21dc-134">In sommige scenario's wilt u echter dat ER-indelingen gebruikmaken van parameters die aan een bepaalde rechtspersoon zijn gerelateerd.</span><span class="sxs-lookup"><span data-stu-id="c21dc-134">However, in some scenarios, you might want to make ER formats use parameters that are related to a specific legal entity.</span></span> <span data-ttu-id="c21dc-135">Uitsluitend in deze scenario's moet u de standaardbedrijfsschakelknop gebruiken.</span><span class="sxs-lookup"><span data-stu-id="c21dc-135">In these scenarios only, you should use the default company switcher.</span></span> <span data-ttu-id="c21dc-136">Zie [ER-indelingen configureren om parameters te gebruiken die per rechtspersoon worden opgegeven](../../fin-ops-core/dev-itpro/analytics/er-app-specific-parameters-configure-format.md) voor een voorbeeld.</span><span class="sxs-lookup"><span data-stu-id="c21dc-136">For an example, see [Configure ER format to use parameters that are specified per legal entity](../../fin-ops-core/dev-itpro/analytics/er-app-specific-parameters-configure-format.md).</span></span>

## <a name="related-rcs-documentation"></a><span data-ttu-id="c21dc-137">Gerelateerde RCS-documentatie</span><span class="sxs-lookup"><span data-stu-id="c21dc-137">Related RCS documentation</span></span>

<span data-ttu-id="c21dc-138">Zie de volgende onderwerpen voor meer informatie over gerelateerde onderdelen:</span><span class="sxs-lookup"><span data-stu-id="c21dc-138">For more information about related components, see the following topics:</span></span>

- <span data-ttu-id="c21dc-139">**RCS:**</span><span class="sxs-lookup"><span data-stu-id="c21dc-139">**RCS:**</span></span>

    - [<span data-ttu-id="c21dc-140">ER-configuraties maken in RCS en ze uploaden naar de algemene opslagplaats</span><span class="sxs-lookup"><span data-stu-id="c21dc-140">Create ER configurations in RCS and upload them to the Global repository</span></span>](rcs-global-repo-upload.md)

- <span data-ttu-id="c21dc-141">**Algemene opslagplaats:**</span><span class="sxs-lookup"><span data-stu-id="c21dc-141">**Global repository:**</span></span>

    - [<span data-ttu-id="c21dc-142">ER-configuratie maken en uploaden naar algemene opslagplaats</span><span class="sxs-lookup"><span data-stu-id="c21dc-142">Create ER configuration & upload to Global repo</span></span>](rcs-global-repo-upload.md)
    - [<span data-ttu-id="c21dc-143">Configuratie delen in algemene opslagplaats</span><span class="sxs-lookup"><span data-stu-id="c21dc-143">Share configuration in Global repo</span></span>](rcs-global-repo-share-configuration.md)
    - [<span data-ttu-id="c21dc-144">Verbeterde filters in algemene opslagplaats</span><span class="sxs-lookup"><span data-stu-id="c21dc-144">Enhanced filtering in Global repo</span></span>](enhanced-filtering-global-repo.md)
    - [<span data-ttu-id="c21dc-145">ER-configuraties downloaden uit de algemene opslagplaats</span><span class="sxs-lookup"><span data-stu-id="c21dc-145">Download ER configurations from the Global repository</span></span>](../../fin-ops-core/dev-itpro/analytics/er-download-configurations-global-repo.md)
    - [<span data-ttu-id="c21dc-146">Configuraties stopzetten in de algemene opslagplaats</span><span class="sxs-lookup"><span data-stu-id="c21dc-146">Discontinuing configurations in Global repo</span></span>](discontinuing-configurations-rcs-global-repo.md)
    - [<span data-ttu-id="c21dc-147">Afschaffing Regulatory Configuration Service (RCS) – Lifecycle Services (LCS) Storage</span><span class="sxs-lookup"><span data-stu-id="c21dc-147">Regulatory Configuration Service (RCS) – Lifecycle Services (LCS) storage deprecation</span></span>](rcs-lcs-repo-dep-faq.md)

- <span data-ttu-id="c21dc-148">**Globalisatiefunctie:**</span><span class="sxs-lookup"><span data-stu-id="c21dc-148">**Globalization feature:**</span></span>

    - [<span data-ttu-id="c21dc-149">Regulatory Configuration Service (RCS) - globalisatiefunctie</span><span class="sxs-lookup"><span data-stu-id="c21dc-149">Regulatory Configuration Service (RCS) - Globalization feature</span></span>](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/regulatory-configuration-service-simplified-globalization-feature-management-globalization-services)


## <a name="troubleshooting-rcs-sign-up"></a><span data-ttu-id="c21dc-150">Problemen met RCS-registratie oplossen</span><span class="sxs-lookup"><span data-stu-id="c21dc-150">Troubleshooting RCS sign-up</span></span>

<span data-ttu-id="c21dc-151">Wanneer u zich via de servicepagina bij RCS aanmeldt, kunt u een probleem aantreffen dat betrekking heeft op Azure Active Directory (Azure AD).</span><span class="sxs-lookup"><span data-stu-id="c21dc-151">When you sign up for RCS from the service page, you might encounter an issue that is related to Azure Active Directory (Azure AD).</span></span> <span data-ttu-id="c21dc-152">Het foutbericht dat u ontvangt, geeft aan dat de aanmelding bij RCS momenteel is uitgeschakeld en moet worden ingeschakeld voordat u het aanmeldingsproces kunt voltooien.</span><span class="sxs-lookup"><span data-stu-id="c21dc-152">The error message that you receive indicates that sign-up for RCS is currently turned off and must be turned on before you can complete the sign-up process.</span></span>

![Foutbericht voor RCS-registratie](media/01_RCSSignUpError.jpg)

<span data-ttu-id="c21dc-154">Het probleem treedt op omdat u bent geblokkeerd voor het aanmelden voor ad-hoc abonnementen en de eigenschap `AllowAdHocSubscriptions` moet zijn ingeschakeld in uw tenant.</span><span class="sxs-lookup"><span data-stu-id="c21dc-154">The issue occurs because you're blocked from signing up for ad-hoc subscriptions, and the `AllowAdHocSubscriptions` property must be enabled in your tenant.</span></span> 

- <span data-ttu-id="c21dc-155">Als uw IT-afdeling de Azure-tenants van uw organisatie beheert, neem dan contact op met die afdeling om het probleem te melden.</span><span class="sxs-lookup"><span data-stu-id="c21dc-155">If your IT department manages your organization's Azure tenants, contact that department to report the issue.</span></span>
- <span data-ttu-id="c21dc-156">Als u verantwoordelijk bent voor het beheer van uw Azure-tenants, kunt u de problemen oplossen door de stappen in [Wat is selfserviceaanmelding voor Azure Active Directory](/azure/active-directory/enterprise-users/directory-self-service-signup#how-do-i-control-self-service-settings) uit te voeren.</span><span class="sxs-lookup"><span data-stu-id="c21dc-156">If you're responsible for managing your Azure tenants, you can fix the issues by following the steps in [What is self-service sign-up for Azure Active Directory](/azure/active-directory/enterprise-users/directory-self-service-signup#how-do-i-control-self-service-settings).</span></span>
