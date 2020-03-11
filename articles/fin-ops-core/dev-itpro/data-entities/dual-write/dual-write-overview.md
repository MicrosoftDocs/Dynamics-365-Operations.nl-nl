---
title: Overzicht van twee keer wegschrijven
description: Dit onderwerp biedt een overzicht van twee keer wegschrijven. Twee keer wegschrijven is een infrastructuur die vrijwel-realtime interactie biedt tussen modelgestuurde Microsoft Dynamics 365-apps en Finance and Operations-apps.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 02/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 12c6a39700a260c138fab67ed370f94b3aa04213
ms.sourcegitcommit: a688c864fc609e35072ad8fd2c01d71f6a5ee7b9
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/20/2020
ms.locfileid: "3075978"
---
# <a name="dual-write-overview"></a><span data-ttu-id="ccc4c-104">Overzicht van twee keer wegschrijven</span><span class="sxs-lookup"><span data-stu-id="ccc4c-104">Dual-write overview</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

## <a name="what-is-dual-write"></a><span data-ttu-id="ccc4c-105">Wat is twee keer wegschrijven?</span><span class="sxs-lookup"><span data-stu-id="ccc4c-105">What is dual-write?</span></span>

<span data-ttu-id="ccc4c-106">Twee keer wegschrijven is een kant-en-klare infrastructuur die vrijwel-realtime interactie biedt tussen modelgestuurde apps in Microsoft Dynamics 365 en Finance and Operations-apps.</span><span class="sxs-lookup"><span data-stu-id="ccc4c-106">Dual-write is an out-of-box infrastructure that provides near-real-time interaction between model-driven apps in Microsoft Dynamics 365 and Finance and Operations apps.</span></span> <span data-ttu-id="ccc4c-107">Wanneer gegevens over klanten, producten, personen en bewerkingen over de grenzen van toepassingen heen stromen, zijn alle afdelingen in een organisatie gemachtigd.</span><span class="sxs-lookup"><span data-stu-id="ccc4c-107">When data about customers, products, people, and operations flows beyond application boundaries, all departments in an organization are empowered.</span></span>

<span data-ttu-id="ccc4c-108">Twee keer wegschrijven biedt nauw gekoppelde, bidirectionele integratie tussen Finance and Operations-apps en Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="ccc4c-108">Dual-write provides tightly coupled, bidirectional integration between Finance and Operations apps and Common Data Service.</span></span> <span data-ttu-id="ccc4c-109">Alle gegevenswijzigingen in Finance and Operations-apps leiden tot schrijfbewerkingen naar Common Data Service en alle gegevenswijzigingen in Common Data Service resulteren in schrijfbewerkingen naar Finance and Operations-apps.</span><span class="sxs-lookup"><span data-stu-id="ccc4c-109">Any data change in Finance and Operations apps causes writes to Common Data Service, and any data change in Common Data Service causes writes to Finance and Operations apps.</span></span> <span data-ttu-id="ccc4c-110">Deze geautomatiseerde gegevensstroom biedt een geïntegreerde gebruikerservaring over de apps heen.</span><span class="sxs-lookup"><span data-stu-id="ccc4c-110">This automated data flow provides an integrated user experience across the apps.</span></span>

![Gegevensrelatie tussen apps](media/dual-write-overview.jpg)

<span data-ttu-id="ccc4c-112">Twee keer wegschrijven heeft twee aspecten: een *infrastructuuraspect* en een *toepassingsaspect*.</span><span class="sxs-lookup"><span data-stu-id="ccc4c-112">Dual-write has two aspects: an *infrastructure* aspect and an *application* aspect.</span></span>

### <a name="infrastructure"></a><span data-ttu-id="ccc4c-113">Infrastructuur</span><span class="sxs-lookup"><span data-stu-id="ccc4c-113">Infrastructure</span></span>

<span data-ttu-id="ccc4c-114">De infrastructuur voor twee keer wegschrijven is uitbreidbaar en betrouwbaar en bevat de volgende hoofdfuncties:</span><span class="sxs-lookup"><span data-stu-id="ccc4c-114">The dual-write infrastructure is extensible and reliable, and includes the following key features:</span></span>

+ <span data-ttu-id="ccc4c-115">Synchrone en bidirectionele gegevensstroom tussen toepassingen</span><span class="sxs-lookup"><span data-stu-id="ccc4c-115">Synchronous and bidirectional data flow between applications</span></span>
+ <span data-ttu-id="ccc4c-116">Synchronisatie, samen met de modi voor afspelen, onderbreken en inhalen, om het systeem te ondersteunen tijdens online en offline/asynchrone modi.</span><span class="sxs-lookup"><span data-stu-id="ccc4c-116">Synchronization, together with play, pause, and catchup modes to support the system during online and offline/asynchronous modes.</span></span>
+ <span data-ttu-id="ccc4c-117">Mogelijkheid om initiële gegevens tussen de toepassingen te synchroniseren</span><span class="sxs-lookup"><span data-stu-id="ccc4c-117">Ability to sync initial data between the applications</span></span>
+ <span data-ttu-id="ccc4c-118">Geconsolideerde weergave van activiteiten- en foutlogbestanden voor gegevensbeheerders</span><span class="sxs-lookup"><span data-stu-id="ccc4c-118">Consolidated view of activity and error logs for data admins</span></span>
+ <span data-ttu-id="ccc4c-119">Mogelijkheid om aangepaste waarschuwingen en drempels te configureren en om zich te abonneren op meldingen</span><span class="sxs-lookup"><span data-stu-id="ccc4c-119">Ability to configure custom alerts and thresholds, and to subscribe to notifications</span></span>
+ <span data-ttu-id="ccc4c-120">Intuïtieve gebruikersinterface (UI) voor filtering en transformaties</span><span class="sxs-lookup"><span data-stu-id="ccc4c-120">Intuitive user interface (UI) for filtering and transformations</span></span>
+ <span data-ttu-id="ccc4c-121">Mogelijkheid om afhankelijkheden en relaties tussen entiteiten in te stellen en weer te geven</span><span class="sxs-lookup"><span data-stu-id="ccc4c-121">Ability to set and view entity dependencies and relationships</span></span>
+ <span data-ttu-id="ccc4c-122">Uitbreidbaarheid voor zowel standaard als aangepaste entiteiten en kaarten</span><span class="sxs-lookup"><span data-stu-id="ccc4c-122">Extensibility for both standard and custom entities and maps</span></span>
+ <span data-ttu-id="ccc4c-123">Betrouwbaar levenscyclusbeheer voor toepassingen</span><span class="sxs-lookup"><span data-stu-id="ccc4c-123">Reliable application lifecycle management</span></span>
+ <span data-ttu-id="ccc4c-124">Kant-en-klare instelling voor nieuwe klanten</span><span class="sxs-lookup"><span data-stu-id="ccc4c-124">Out-of-box setup experience for new customers</span></span>

### <a name="application"></a><span data-ttu-id="ccc4c-125">Aanvraag</span><span class="sxs-lookup"><span data-stu-id="ccc4c-125">Application</span></span>

<span data-ttu-id="ccc4c-126">Met twee keer wegschrijven worden concepten in Finance and Operations-apps gekoppeld aan concepten in modelgestuurde apps in Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="ccc4c-126">Dual-write creates a mapping between concepts in Finance and Operations apps and concepts in model-driven apps in Dynamics 365.</span></span> <span data-ttu-id="ccc4c-127">Deze integratie ondersteunt de volgende scenario's:</span><span class="sxs-lookup"><span data-stu-id="ccc4c-127">This integration supports the following scenarios:</span></span>

+ <span data-ttu-id="ccc4c-128">Model voor geïntegreerde klanten</span><span class="sxs-lookup"><span data-stu-id="ccc4c-128">Integrated customer master</span></span>
+ <span data-ttu-id="ccc4c-129">Toegang tot loyaliteitskaarten en beloningspunten van klanten</span><span class="sxs-lookup"><span data-stu-id="ccc4c-129">Access to customer loyalty cards and reward points</span></span>
+ <span data-ttu-id="ccc4c-130">Uniform gebruik van productmodellen</span><span class="sxs-lookup"><span data-stu-id="ccc4c-130">Unified product mastering experience</span></span>
+ <span data-ttu-id="ccc4c-131">Kennis van organisatiehiërarchie</span><span class="sxs-lookup"><span data-stu-id="ccc4c-131">Awareness of organization hierarchy</span></span>
+ <span data-ttu-id="ccc4c-132">Model voor geïntegreerde leveranciers</span><span class="sxs-lookup"><span data-stu-id="ccc4c-132">Integrated vendor master</span></span>
+ <span data-ttu-id="ccc4c-133">Toegang tot referentiegegevens voor financiën en belastingen</span><span class="sxs-lookup"><span data-stu-id="ccc4c-133">Access to finance and tax reference data</span></span>
+ <span data-ttu-id="ccc4c-134">Beschikbaarheid van prijsengine op aanvraag</span><span class="sxs-lookup"><span data-stu-id="ccc4c-134">On-demand price engine experience</span></span>
+ <span data-ttu-id="ccc4c-135">Geïntegreerde ervaring van prospect naar contant geld</span><span class="sxs-lookup"><span data-stu-id="ccc4c-135">Integrated prospect-to-cash experience</span></span>
+ <span data-ttu-id="ccc4c-136">Mogelijkheid om zowel interne activa als klantactiva te bedienen via veldmedewerkers</span><span class="sxs-lookup"><span data-stu-id="ccc4c-136">Ability to serve both in-house assets and customer assets through field agents</span></span>
+ <span data-ttu-id="ccc4c-137">Geïntegreerd proces van inkopen tot betalen</span><span class="sxs-lookup"><span data-stu-id="ccc4c-137">Integrated procure-to-pay experience</span></span>
+ <span data-ttu-id="ccc4c-138">Geïntegreerde activiteiten en notities voor klantgegevens en -documenten</span><span class="sxs-lookup"><span data-stu-id="ccc4c-138">Integrated activities and notes for customer data and documents</span></span>
+ <span data-ttu-id="ccc4c-139">Mogelijkheid om de beschikbaarheid van voorhanden voorraad en details op te zoeken</span><span class="sxs-lookup"><span data-stu-id="ccc4c-139">Ability to look up on-hand inventory availability and details</span></span>
+ <span data-ttu-id="ccc4c-140">Ervaring van project naar contant geld</span><span class="sxs-lookup"><span data-stu-id="ccc4c-140">Project-to-cash experience</span></span>
+ <span data-ttu-id="ccc4c-141">Mogelijkheid om meerdere adressen en rollen te verwerken via het partijconcept</span><span class="sxs-lookup"><span data-stu-id="ccc4c-141">Ability to handle multiple addresses and roles through the party concept</span></span>
+ <span data-ttu-id="ccc4c-142">Een enkel bronbeheer voor gebruikers</span><span class="sxs-lookup"><span data-stu-id="ccc4c-142">Single source management for users</span></span>
+ <span data-ttu-id="ccc4c-143">Geïntegreerde kanalen voor detailhandel en marketing</span><span class="sxs-lookup"><span data-stu-id="ccc4c-143">Integrated channels for retailing and marketing</span></span>
+ <span data-ttu-id="ccc4c-144">Zicht op acties en kortingen</span><span class="sxs-lookup"><span data-stu-id="ccc4c-144">Visibility into promotions and discounts</span></span>
+ <span data-ttu-id="ccc4c-145">Functies voor aanvragen van service</span><span class="sxs-lookup"><span data-stu-id="ccc4c-145">Request-for-service functions</span></span>
+ <span data-ttu-id="ccc4c-146">Gestroomlijnde servicebewerkingen</span><span class="sxs-lookup"><span data-stu-id="ccc4c-146">Streamlined service operations</span></span>

## <a name="top-reasons-to-use-dual-write"></a><span data-ttu-id="ccc4c-147">Belangrijkste redenen voor het gebruik van twee keer wegschrijven</span><span class="sxs-lookup"><span data-stu-id="ccc4c-147">Top reasons to use dual-write</span></span>

<span data-ttu-id="ccc4c-148">Twee keer wegschrijven biedt gegevensintegratie tussen Microsoft Dynamics 365-toepassingen.</span><span class="sxs-lookup"><span data-stu-id="ccc4c-148">Dual-write provides data integration across Microsoft Dynamics 365 applications.</span></span> <span data-ttu-id="ccc4c-149">Dit robuuste raamwerk koppelt omgevingen en zorgen ervoor dat verschillende bedrijfstoepassingen samenwerken.</span><span class="sxs-lookup"><span data-stu-id="ccc4c-149">This robust framework links environments and enables different business applications to work together.</span></span> <span data-ttu-id="ccc4c-150">Dit zijn de belangrijkste redenen voor het gebruik van twee keer wegschrijven:</span><span class="sxs-lookup"><span data-stu-id="ccc4c-150">Here are the top reasons why you should use dual-write:</span></span>

+ <span data-ttu-id="ccc4c-151">Met twee keer wegschrijven beschikt u over een strak gekoppelde, bijna realtime en bidirectionele integratie tussen Finance and Operations-apps en modelgestuurde apps in Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="ccc4c-151">Dual-write provides tightly coupled, near-real-time, and bidirectional integration between Finance and Operations apps and model-driven apps in Dynamics 365.</span></span> <span data-ttu-id="ccc4c-152">Door deze integratie is Microsoft Dynamics 365 de plek voor al uw zakelijke oplossingen.</span><span class="sxs-lookup"><span data-stu-id="ccc4c-152">This integration makes Microsoft Dynamics 365 the one-stop shop for all your business solutions.</span></span> <span data-ttu-id="ccc4c-153">Klanten die gebruikmaken van Dynamics 365 Finance en Dynamics 365 Supply Chain Management, maar die niet-Microsoft-oplossingen voor Customer Relationship Management (CRM) gebruiken, stappen over op Dynamics 365 vanwege de ondersteuning voor twee keer wegschrijven.</span><span class="sxs-lookup"><span data-stu-id="ccc4c-153">Customers who use Dynamics 365 Finance and Dynamics 365 Supply Chain Management, but who use non-Microsoft solutions for customer relationship management (CRM), are moving toward Dynamics 365 for its dual-write support.</span></span>
+ <span data-ttu-id="ccc4c-154">Gegevens van klanten, producten, transacties, projecten en het Internet of Things (IoT) stromen automatisch naar Common Data Service via twee keer wegschrijven.</span><span class="sxs-lookup"><span data-stu-id="ccc4c-154">Data from customers, products, operations, projects, and the Internet of Things (IoT) automatically flows to Common Data Service through dual-write.</span></span> <span data-ttu-id="ccc4c-155">Deze verbinding is heel nuttig voor bedrijven die geïnteresseerd zijn in Microsoft Power Platform-uitbreidingen.</span><span class="sxs-lookup"><span data-stu-id="ccc4c-155">This connection is very useful for businesses that are interested in Microsoft Power Platform expansions.</span></span>
+ <span data-ttu-id="ccc4c-156">De infrastructuur voor twee keer wegschrijven volgt het principe van geen code/weinig code.</span><span class="sxs-lookup"><span data-stu-id="ccc4c-156">The dual-write infrastructure follows the no-code/low-code principle.</span></span> <span data-ttu-id="ccc4c-157">Er is minimale technische inspanning vereist om de standaardtoewijzingen van tabel naar tabel uit te breiden en aangepaste toewijzingen op te nemen.</span><span class="sxs-lookup"><span data-stu-id="ccc4c-157">Minimal engineering effort is required to extend the standard table-to-table maps and to include custom maps.</span></span>
+ <span data-ttu-id="ccc4c-158">Twee keer wegschrijven ondersteunt zowel de online modus als de offline modus.</span><span class="sxs-lookup"><span data-stu-id="ccc4c-158">Dual-write supports both online mode and offline mode.</span></span> <span data-ttu-id="ccc4c-159">Microsoft is het enige bedrijf dat ondersteuning biedt voor online en offline modi.</span><span class="sxs-lookup"><span data-stu-id="ccc4c-159">Microsoft is the only company that offers support for online and offline modes.</span></span>

## <a name="what-does-dual-write-mean-for-users-and-architects-of-crm-products"></a><span data-ttu-id="ccc4c-160">Wat betekent twee keer wegschrijven voor gebruikers en architecten van CRM-producten?</span><span class="sxs-lookup"><span data-stu-id="ccc4c-160">What does dual-write mean for users and architects of CRM products?</span></span>

<span data-ttu-id="ccc4c-161">Met twee keer wegschrijven wordt de gegevensstroom tussen Finance and Operations-apps en Common Data Service geautomatiseerd.</span><span class="sxs-lookup"><span data-stu-id="ccc4c-161">Dual-write automates the data flow between Finance and Operations apps and Common Data Service.</span></span> <span data-ttu-id="ccc4c-162">In toekomstige releases worden concepten in modelgestuurde apps in Dynamics 365 (zoals klant, contactpersoon, prijsopgave en order) geschaald naar klanten in de middenmarkt en hogere middenmarkt.</span><span class="sxs-lookup"><span data-stu-id="ccc4c-162">In future releases, concepts in model-driven apps in Dynamics 365 (for example, customer, contact, quotation, and order) will be scaled to mid-market and upper-mid-market customers.</span></span>

<span data-ttu-id="ccc4c-163">In de eerste release wordt de meeste automatisering verzorgd door oplossingen voor twee keer wegschrijven.</span><span class="sxs-lookup"><span data-stu-id="ccc4c-163">In the first release, most of the automation is handled by dual-write solutions.</span></span> <span data-ttu-id="ccc4c-164">In toekomstige releases worden deze oplossingen onderdeel van Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="ccc4c-164">In future releases, those solutions will become part of Common Data Service.</span></span> <span data-ttu-id="ccc4c-165">Door de aanstaande wijzigingen in Common Data Service te begrijpen, kunt u uw inspanningen op lange termijn beperken.</span><span class="sxs-lookup"><span data-stu-id="ccc4c-165">By understanding the upcoming changes to Common Data Service, you can save yourself effort in the long term.</span></span> <span data-ttu-id="ccc4c-166">Hier volgen enkele van de belangrijke wijzigingen:</span><span class="sxs-lookup"><span data-stu-id="ccc4c-166">Here are some of the crucial changes:</span></span>

+ <span data-ttu-id="ccc4c-167">Common Data Service krijgt nieuwe concepten, zoals bedrijf en partij.</span><span class="sxs-lookup"><span data-stu-id="ccc4c-167">Common Data Service will have new concepts, such as company and party.</span></span> <span data-ttu-id="ccc4c-168">Deze concepten zijn van invloed op alle apps die op Common Data Service zijn gebouwd, zoals Dynamics 365 Sales, Dynamics 365 Marketing, Dynamics 365 Customer Service en Dynamics 365 Field Service.</span><span class="sxs-lookup"><span data-stu-id="ccc4c-168">These concepts will affect all apps that are built on Common Data Service, such as Dynamics 365 Sales, Dynamics 365 Marketing, Dynamics 365 Customer Service, and Dynamics 365 Field Service.</span></span>
+ <span data-ttu-id="ccc4c-169">Activiteiten en notities worden gecombineerd en uitgebreid om zowel C1's (gebruikers van het systeem) als C2's (klanten van het systeem) te ondersteunen.</span><span class="sxs-lookup"><span data-stu-id="ccc4c-169">Activities and notes are unified and expanded to support both C1s (users of the system) and C2s (customers of the system).</span></span>
+ <span data-ttu-id="ccc4c-170">Hier volgen enkele van de komende wijzigingen in Common Data Service:</span><span class="sxs-lookup"><span data-stu-id="ccc4c-170">Here are some of the upcoming changes in Common Data Service:</span></span>

    - <span data-ttu-id="ccc4c-171">Het gegevenstype decimaal vervangt het gegevenstype geld.</span><span class="sxs-lookup"><span data-stu-id="ccc4c-171">The decimal data type will replace the money data type.</span></span>
    - <span data-ttu-id="ccc4c-172">Datumeffectiviteit biedt ondersteuning voor vroegere, huidige en toekomstige datums op dezelfde locatie.</span><span class="sxs-lookup"><span data-stu-id="ccc4c-172">Date effectivity will support past, present, and future data in the same place.</span></span>
    - <span data-ttu-id="ccc4c-173">Er wordt meer ondersteuning geboden voor valuta en wisselkoersen en API (Application Programming Interface) voor **Wisselkoers** wordt herzien.</span><span class="sxs-lookup"><span data-stu-id="ccc4c-173">There will be more support for currency and exchange rates, and the **Exchange Rate** application programming interface (API) will be revised.</span></span>
    - <span data-ttu-id="ccc4c-174">Eenheidsomrekeningen worden ondersteund.</span><span class="sxs-lookup"><span data-stu-id="ccc4c-174">Unit conversions will be supported.</span></span>

<span data-ttu-id="ccc4c-175">Zie [Gegevens in Common Data Service – fase 1 en 2](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/extensibility/extensibility-roadmap) voor meer informatie over aanstaande wijzigingen.</span><span class="sxs-lookup"><span data-stu-id="ccc4c-175">For more information about upcoming changes, see [Data in Common Data Service – phase 1 & 2](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/extensibility/extensibility-roadmap).</span></span>
