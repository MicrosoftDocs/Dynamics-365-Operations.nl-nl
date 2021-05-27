---
title: Regulatory Configuration Service
description: In dit onderwerp wordt een overzicht gegeven van de functies van RCS (Regulatory Configuration Service) en wordt uitgelegd hoe u toegang krijgt tot de service.
author: JaneA07
ms.date: 04/07/2021
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
ms.openlocfilehash: 1eeac7217290e0583fcecdf5b4b5b9153d266240
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/11/2021
ms.locfileid: "6019389"
---
# <a name="regulatory-configuration-service"></a><span data-ttu-id="70d60-103">Regulatory Configuration Service</span><span class="sxs-lookup"><span data-stu-id="70d60-103">Regulatory Configuration Service</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="70d60-104">Regulatory Configuration Service (RCS) is een zelfstandige ontwerpfunctie en lifecyclebeheerservice voor globalisatiefunctionaliteit zonder code/met weinig code.</span><span class="sxs-lookup"><span data-stu-id="70d60-104">Regulatory Configuration Service (RCS) is a standalone designer and lifecycle management service for no-code/low-code globalization functionality.</span></span> <span data-ttu-id="70d60-105">Met RCS kunnen globalisatiepartijen belangrijke globalisatiegebieden van belasting, e-facturering, wettelijke rapportage, bankdocumenten en bedrijfsdocumenten uitbreiden en aanpassen zonder ontwikkelaars.</span><span class="sxs-lookup"><span data-stu-id="70d60-105">RCS lets globalization stakeholders extend and customize key globalization areas of tax, e-invoicing, regulatory reporting, banking, and business documents without having to involve developers.</span></span> <span data-ttu-id="70d60-106">Door deze globalisatie zonder code/met weinig code wordt globalisatie eenvoudiger, sneller en effectiever om te maken of uit te breiden.</span><span class="sxs-lookup"><span data-stu-id="70d60-106">This no-code/low-code globalization approach makes globalization easier, faster, and more cost effective to create or extend.</span></span>

<span data-ttu-id="70d60-107">RCS biedt de volgende mogelijkheden:</span><span class="sxs-lookup"><span data-stu-id="70d60-107">RCS provides the following capabilities:</span></span>

- <span data-ttu-id="70d60-108">Ondersteuning voor alle functionaliteit die wordt geleverd door Elektronische rapportage (ER).</span><span class="sxs-lookup"><span data-stu-id="70d60-108">Support for all functionality that is provided by Electronic reporting (ER).</span></span>
- <span data-ttu-id="70d60-109">Een vereiste voor het configureren van nieuwe microservices voor globalisatie.</span><span class="sxs-lookup"><span data-stu-id="70d60-109">A prerequisite to configure new globalization microservices.</span></span>
- <span data-ttu-id="70d60-110">Ondersteuning voor Elektronische facturering.</span><span class="sxs-lookup"><span data-stu-id="70d60-110">Support for Electronic Invoicing.</span></span> <span data-ttu-id="70d60-111">Zie [Elektronische facturering](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/electronic-invoicing-add-on-dynamics-365-ga) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="70d60-111">For more information, see [Electronic Invoicing](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/electronic-invoicing-add-on-dynamics-365-ga).</span></span>
- <span data-ttu-id="70d60-112">Ondersteunt Belastingberekening.</span><span class="sxs-lookup"><span data-stu-id="70d60-112">Supports for Tax Calculation.</span></span> <span data-ttu-id="70d60-113">Zie voor meer informatie [Belastingservice](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/tax-service-preview).</span><span class="sxs-lookup"><span data-stu-id="70d60-113">For more information, see [Tax service](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/tax-service-preview).</span></span>
- <span data-ttu-id="70d60-114">Ondersteuning voor nieuwe functionaliteit voor globalisatiefuncties die het levenscyclusbeheer van meerdere componentfuncties vereenvoudigt en extra mogelijkheden biedt voor het configureren van acties en het instellen van functieparameters.</span><span class="sxs-lookup"><span data-stu-id="70d60-114">Support for new globalization feature functionality that simplifies the lifecycle management of multi-component features and provides extra capability to configure actions and set up feature parameters.</span></span> <span data-ttu-id="70d60-115">Zie [Regulatory Configuration Service – vereenvoudigd globalisatiefunctiebeheer voor globalisatieservices](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/regulatory-configuration-service-simplified-globalization-feature-management-globalization-services)  voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="70d60-115">For more information, see [Regulatory Configuration Service – simplified globalization feature management for globalization services](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/regulatory-configuration-service-simplified-globalization-feature-management-globalization-services).</span></span>
- <span data-ttu-id="70d60-116">Ondersteuning voor gecentraliseerde publicatie, opslag en het delen van aangepaste configuraties in de Algemene opslagplaats om configuratiebeheer te vereenvoudigen zonder dat Microsoft Dynamics Lifecycle Services moet worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="70d60-116">Support for centralized publication, storage, and sharing of custom configurations in the Global repository to simplify configuration management without requiring the use of Microsoft Dynamics Lifecycle Services (LCS).</span></span>

## <a name="access-rcs"></a><span data-ttu-id="70d60-117">Toegang tot RCS</span><span class="sxs-lookup"><span data-stu-id="70d60-117">Access RCS</span></span>

<span data-ttu-id="70d60-118">U kunt zich registreren voor RCS of u aanmelden via de pagina [Regulatory Configuration Service](https://marketing.configure.global.dynamics.com/).</span><span class="sxs-lookup"><span data-stu-id="70d60-118">You can sign up for or sign in to RCS from the [Regulatory Configuration Service page](https://marketing.configure.global.dynamics.com/).</span></span>

![Registreren/aanmelden bij RCS](media/202103_RCS%20Marketing%20page_updated_1.jpg)

<span data-ttu-id="70d60-120">Controleer op de pagina **Regulatory Configuration Service** de aanvullende algemene voorwaarden voor gebruik van de service. Accepteer deze en selecteer een van de volgende knoppen:</span><span class="sxs-lookup"><span data-stu-id="70d60-120">On the **Regulatory Configuration Service** page, review and accept the supplemental terms and conditions for use of the service, and then select one of the following buttons:</span></span>

- <span data-ttu-id="70d60-121">**Registreren** als u een nieuwe gebruiker van de service bent en u een bedrijfse-mailadres gebruikt om uw organisatie een serviceomgeving in te richten</span><span class="sxs-lookup"><span data-stu-id="70d60-121">**Sign up** if you're a first-time user of the service, and you're using a business email address to provision your organization a service environment</span></span>
- <span data-ttu-id="70d60-122">**Aanmelden** als u zich eerder hebt aangemeld voor de service en u toegang wilt krijgen tot uw organisatieomgeving</span><span class="sxs-lookup"><span data-stu-id="70d60-122">**Sign in** if you've previously signed up for the service, and you want to access your organization environment</span></span>

## <a name="regional-availability"></a><span data-ttu-id="70d60-123">Regionale beschikbaarheid</span><span class="sxs-lookup"><span data-stu-id="70d60-123">Regional availability</span></span>

<span data-ttu-id="70d60-124">RCS is algemeen beschikbaar in de volgende regio's:</span><span class="sxs-lookup"><span data-stu-id="70d60-124">RCS is generally available in the following regions:</span></span>

- <span data-ttu-id="70d60-125">Verenigde Staten</span><span class="sxs-lookup"><span data-stu-id="70d60-125">United States</span></span>
- <span data-ttu-id="70d60-126">India</span><span class="sxs-lookup"><span data-stu-id="70d60-126">India</span></span>
- <span data-ttu-id="70d60-127">Frankrijk</span><span class="sxs-lookup"><span data-stu-id="70d60-127">France</span></span>
- <span data-ttu-id="70d60-128">Europa</span><span class="sxs-lookup"><span data-stu-id="70d60-128">Europe</span></span>

<span data-ttu-id="70d60-129">Zie [Dynamics 365 en Power Platform: beschikbaarheid, gegevenslocatie, taal en lokalisatie](https://aka.ms/dynamics_365_international_availability_deck) voor een volledige lijst met regio's.</span><span class="sxs-lookup"><span data-stu-id="70d60-129">For a complete list of regions, see [Dynamics 365 and Power Platform: Availability, data location, language, and localization](https://aka.ms/dynamics_365_international_availability_deck).</span></span>

## <a name="related-rcs-documentation"></a><span data-ttu-id="70d60-130">Gerelateerde RCS-documentatie</span><span class="sxs-lookup"><span data-stu-id="70d60-130">Related RCS documentation</span></span>

<span data-ttu-id="70d60-131">Zie de volgende documentatie voor meer informatie over gerelateerde componenten:</span><span class="sxs-lookup"><span data-stu-id="70d60-131">For more information about related components, see the following documentation:</span></span>

- <span data-ttu-id="70d60-132">**Algemene opslagplaats:**</span><span class="sxs-lookup"><span data-stu-id="70d60-132">**Global repository:**</span></span>

    - [<span data-ttu-id="70d60-133">ER-configuratie maken en uploaden naar algemene opslagplaats</span><span class="sxs-lookup"><span data-stu-id="70d60-133">Create ER configuration & upload to Global repo</span></span>](rcs-global-repo-upload.md)
    - [<span data-ttu-id="70d60-134">Configuratie delen in algemene opslagplaats</span><span class="sxs-lookup"><span data-stu-id="70d60-134">Share configuration in Global repo</span></span>](rcs-global-repo-share-configuration.md)
    - [<span data-ttu-id="70d60-135">Verbeterde filters in algemene opslagplaats</span><span class="sxs-lookup"><span data-stu-id="70d60-135">Enhanced filtering in Global repo</span></span>](enhanced-filtering-global-repo.md)
    - [<span data-ttu-id="70d60-136">ER-configuraties downloaden uit de algemene opslagplaats</span><span class="sxs-lookup"><span data-stu-id="70d60-136">Download ER configurations from the Global repository</span></span>](../../fin-ops-core/dev-itpro/analytics/er-download-configurations-global-repo.md)
    - [<span data-ttu-id="70d60-137">Configuraties stopzetten in de algemene opslagplaats</span><span class="sxs-lookup"><span data-stu-id="70d60-137">Discontinuing configurations in Global repo</span></span>](discontinuing-configurations-rcs-global-repo.md)

- <span data-ttu-id="70d60-138">**Globalisatiefunctie:**</span><span class="sxs-lookup"><span data-stu-id="70d60-138">**Globalization feature:**</span></span>

    - [<span data-ttu-id="70d60-139">Regulatory Configuration Service (RCS) - globalisatiefunctie</span><span class="sxs-lookup"><span data-stu-id="70d60-139">Regulatory Configuration Service (RCS) - Globalization feature</span></span>](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/regulatory-configuration-service-simplified-globalization-feature-management-globalization-services)