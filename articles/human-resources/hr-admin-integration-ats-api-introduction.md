---
title: Integratie-API voor sollicitantenvolgsysteem - Inleiding
description: In dit onderwerp wordt de Dynamics 365 Human Resources integratie-API voor sollicitantenvolgsysteem (ATS) beschreven.
author: andreabichsel
manager: tfehr
ms.date: 02/03/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 48e368fe69443a5105ddba78a887bf9159bfe52a
ms.sourcegitcommit: 33b5c8bc4f9461e290513aa22de1ec1fba3b0742
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/05/2021
ms.locfileid: "5125588"
---
# <a name="applicant-tracking-system-integration-api-introduction"></a><span data-ttu-id="c0132-103">Integratie-API voor sollicitantenvolgsysteem - Inleiding</span><span class="sxs-lookup"><span data-stu-id="c0132-103">Applicant Tracking System integration API introduction</span></span>

<span data-ttu-id="c0132-104">In dit onderwerp wordt de Dynamics 365 Human Resources integratie-API voor sollicitantenvolgsysteem (ATS) beschreven.</span><span class="sxs-lookup"><span data-stu-id="c0132-104">This topic describes the Dynamics 365 Human Resources Applicant Tracking System (ATS) integration API.</span></span> <span data-ttu-id="c0132-105">De API is bedoeld om gestroomlijnde integraties tussen Dynamics 365 Human Resources en ATS-partners mogelijk te maken.</span><span class="sxs-lookup"><span data-stu-id="c0132-105">The intent of the API is to enable streamlined integrations between Dynamics 365 Human Resources and partnering ATSs.</span></span>

![ATS integratiestroom](media/hr-admin-integration-ats-api-introduction-flow.png)

<span data-ttu-id="c0132-107">De geïntegreerde ervaring begint in Human Resources wanneer een aanstellende manager een wervingsaanvraag maakt.</span><span class="sxs-lookup"><span data-stu-id="c0132-107">The integrated experience begins in Human Resources when a hiring manager creates a recruiting request.</span></span> <span data-ttu-id="c0132-108">Wanneer de aanvraag is geactiveerd, haalt de ATS de details op voor de aanvraag om een wervingsproject te maken.</span><span class="sxs-lookup"><span data-stu-id="c0132-108">When the request is activated, the ATS pulls the detail for the request to create a recruiting project.</span></span> <span data-ttu-id="c0132-109">Daarna volgt het de wervingspijplijn om een kandidaat voor de functie(s) te selecteren en aan te stellen.</span><span class="sxs-lookup"><span data-stu-id="c0132-109">Then it follows the recruiting pipeline to select and hire a candidate for the position(s).</span></span> <span data-ttu-id="c0132-110">Ten slotte rondt het ATS de integratie af door de record van de geselecteerde kandidaat naar Human Resources te sturen.</span><span class="sxs-lookup"><span data-stu-id="c0132-110">Finally, the ATS completes the round-trip integration by sending the selected candidate’s record into Human Resources.</span></span> <span data-ttu-id="c0132-111">De record van de kandidaat kan dan door meer onboarding validaties en werkstromen gaan om de werknemerrecord te maken.</span><span class="sxs-lookup"><span data-stu-id="c0132-111">The candidate record can then go through more onboarding validations and workflows to create the employee record.</span></span>

<span data-ttu-id="c0132-112">Human Resources heeft de volgende onderdelen toegevoegd om de integratie in te schakelen:</span><span class="sxs-lookup"><span data-stu-id="c0132-112">To enable the integration, Human Resources has added the following components:</span></span>

1.  <span data-ttu-id="c0132-113">Functionaliteit om een wervingsaanvraag te maken.</span><span class="sxs-lookup"><span data-stu-id="c0132-113">Functionality to create a recruiting request.</span></span>
2.  <span data-ttu-id="c0132-114">Een uitgebreid kandidaatprofiel en gerelateerde werkstromen.</span><span class="sxs-lookup"><span data-stu-id="c0132-114">An expanded candidate profile and related workflows.</span></span>
3.  <span data-ttu-id="c0132-115">Een integratie-API die de nieuwe functionaliteit opent voor de integratie van toepassingen.</span><span class="sxs-lookup"><span data-stu-id="c0132-115">An integration API opening up the new functionality to integrating applications.</span></span>

<span data-ttu-id="c0132-116">Zie [Kandidaten werven](hr-personnel-recruit.md) voor meer informatie over het instellen en gebruiken van de functionaliteit voor wervingsaanvragen en kandidaten.</span><span class="sxs-lookup"><span data-stu-id="c0132-116">For more information about setting up and using the recruiting request and candidate functionality, see [Recruit job candidates](hr-personnel-recruit.md).</span></span>

## <a name="microsoft-dataverse"></a><span data-ttu-id="c0132-117">Microsoft Dataverse</span><span class="sxs-lookup"><span data-stu-id="c0132-117">Microsoft Dataverse</span></span>

<span data-ttu-id="c0132-118">Deze API is gebouwd op Microsoft Dataverse (voorheen Common Data Service).</span><span class="sxs-lookup"><span data-stu-id="c0132-118">This API is built on Microsoft Dataverse (formerly Common Data Service).</span></span> <span data-ttu-id="c0132-119">Alle RESTful-interactie met deze API gaat via de Microsoft Dataverse web-API, die OData gebruikt.</span><span class="sxs-lookup"><span data-stu-id="c0132-119">All RESTful interaction with this API is done via the Microsoft Dataverse Web API, which uses OData.</span></span> <span data-ttu-id="c0132-120">Deze API is een subset van de Dataverse web-API.</span><span class="sxs-lookup"><span data-stu-id="c0132-120">This API is a subset of the Dataverse Web API.</span></span> <span data-ttu-id="c0132-121">De Dataverse web-API definieert kenmerken als verificatie, SLA's, batch, gelijktijdigheidscontrole en foutverwerking.</span><span class="sxs-lookup"><span data-stu-id="c0132-121">The Dataverse Web API defines characteristics such as authentication, SLAs, batch, concurrency control, and error handling.</span></span>

<span data-ttu-id="c0132-122">Voor meer algemene informatie over de Microsoft Dataverse web-API, zie:</span><span class="sxs-lookup"><span data-stu-id="c0132-122">For more general information about the Microsoft Dataverse Web API, see:</span></span>

- [<span data-ttu-id="c0132-123">Wat is Microsoft Dataverse?</span><span class="sxs-lookup"><span data-stu-id="c0132-123">What is Microsoft Dataverse?</span></span>](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro)
- [<span data-ttu-id="c0132-124">De Microsoft Dataverse web-API gebruiken</span><span class="sxs-lookup"><span data-stu-id="c0132-124">Use the Microsoft Dataverse Web API</span></span>](https://docs.microsoft.com/powerapps/developer/data-platform/webapi/overview)
- [<span data-ttu-id="c0132-125">Microsoft Dataverse ontwikkelaarshandleiding</span><span class="sxs-lookup"><span data-stu-id="c0132-125">Microsoft Dataverse developer guide</span></span>](https://docs.microsoft.com/powerapps/developer/data-platform)

<span data-ttu-id="c0132-126">De bovenstaande documentatie bevat gedetailleerde informatie en richtlijnen voor ontwikkelaars voor het gebruik van de Dataverse web-API, zoals [verificatie beheren](https://docs.microsoft.com/powerapps/developer/data-platform/webapi/authenticate-web-api), [bewerkingen uitvoeren](https://docs.microsoft.com/powerapps/developer/data-platform/webapi/perform-operations-web-api), [Postman gebruiken met de API](https://docs.microsoft.com/powerapps/developer/data-platform/webapi/use-postman-web-api) en [wijzigingen bijhouden of deltatokens gebruiken](https://docs.microsoft.com/powerapps/developer/data-platform/use-change-tracking-synchronize-data-external-systems) met de API.</span><span class="sxs-lookup"><span data-stu-id="c0132-126">The above documentation includes detail and developer guidance on using the Dataverse Web API, such as [managing authentication](https://docs.microsoft.com/powerapps/developer/data-platform/webapi/authenticate-web-api), [performing operations](https://docs.microsoft.com/powerapps/developer/data-platform/webapi/perform-operations-web-api), [using Postman with the API](https://docs.microsoft.com/powerapps/developer/data-platform/webapi/use-postman-web-api), and [using change tracking or delta tokens](https://docs.microsoft.com/powerapps/developer/data-platform/use-change-tracking-synchronize-data-external-systems) with the API.</span></span>

### <a name="option-sets"></a><span data-ttu-id="c0132-127">Optiesets</span><span class="sxs-lookup"><span data-stu-id="c0132-127">Option sets</span></span>

<span data-ttu-id="c0132-128">Het gegevensmodel voor de API voor ATS-integratie die in dit document wordt beschreven, bevat optiesets die opgesomde waarden bevatten die aan entiteitseigenschappen zijn gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="c0132-128">The data model for the ATS integration API described in this document includes option sets that provide enumerated values associated with entity properties.</span></span> <span data-ttu-id="c0132-129">Zie [Optiesets maken en bijwerken met de web-API](https://docs.microsoft.com/powerapps/developer/data-platform/webapi/create-update-optionsets) voor gedetailleerde informatie over het werken met optiesets in de Dataverse web-API.</span><span class="sxs-lookup"><span data-stu-id="c0132-129">For detail on working with option sets in the Dataverse Web API, see [Create and update option sets using the Web API](https://docs.microsoft.com/powerapps/developer/data-platform/webapi/create-update-optionsets).</span></span> <span data-ttu-id="c0132-130">Voor elke Dataverse-omgeving worden optiesets gedefinieerd.</span><span class="sxs-lookup"><span data-stu-id="c0132-130">Option sets are defined for each Dataverse environment.</span></span>

### <a name="virtual-tables-for-human-resources-in-dataverse"></a><span data-ttu-id="c0132-131">Virtuele tabellen in Dataverse voor Human Resources</span><span class="sxs-lookup"><span data-stu-id="c0132-131">Virtual tables for Human Resources in Dataverse</span></span>

<span data-ttu-id="c0132-132">De eindpunten voor de API voor ATS-integratie maken gebruik van de mogelijkheden van het virtuele tabelplatform van Microsoft Dataverse.</span><span class="sxs-lookup"><span data-stu-id="c0132-132">The endpoints for the ATS integration API use the virtual table platform capabilities of Microsoft Dataverse.</span></span> <span data-ttu-id="c0132-133">Standaard worden de virtuele tabellen en de bijbehorende API-eindpunten niet geïmplementeerd voor Human Resources-omgevingen, waardoor organisaties kunnen bepalen welke OData-eindpunten beschikbaar worden voor de omgeving.</span><span class="sxs-lookup"><span data-stu-id="c0132-133">By default, the virtual tables and their associated API endpoints are not deployed for Human Resources environments, enabling organizations to determine which OData endpoints will be exposed for the environment.</span></span> <span data-ttu-id="c0132-134">Als u de API wilt gebruiken, moeten de virtuele tabellen voor de Human Resources-entiteiten worden gegenereerd voor de omgeving.</span><span class="sxs-lookup"><span data-stu-id="c0132-134">To use the API, the virtual tables for the Human Resources entities must be generated for the environment.</span></span> 

<span data-ttu-id="c0132-135">Zie [Dataverse virtuele tabellen configureren](https://docs.microsoft.com/dynamics365/human-resources/hr-admin-integration-common-data-service-virtual-entities) voor informatie over het genereren van de virtuele tabellen voor de API.</span><span class="sxs-lookup"><span data-stu-id="c0132-135">For information on generating the virtual tables for the API, see [Configure Dataverse virtual tables](https://docs.microsoft.com/dynamics365/human-resources/hr-admin-integration-common-data-service-virtual-entities).</span></span>

## <a name="data-model"></a><span data-ttu-id="c0132-136">Gegevensmodel</span><span class="sxs-lookup"><span data-stu-id="c0132-136">Data model</span></span>

<span data-ttu-id="c0132-137">Het gegevensmodel is gericht op twee hoofdentiteiten:</span><span class="sxs-lookup"><span data-stu-id="c0132-137">The data model is centered around two main entities:</span></span>

- <span data-ttu-id="c0132-138">**Wervingsaanvraag** geeft een aanvraag aan een ATS weer om te werven voor een of meer vacatures. Zie [Voorbeeldquery voor wervingsaanvraag](hr-admin-integration-ats-api-recruiting-request-example-query.md) voor een voorbeeldquery.</span><span class="sxs-lookup"><span data-stu-id="c0132-138">**RecruitingRequest** represents a request to an ATS to recruit for one or more open positions.For an example query, see [Example query for Recruiting request](hr-admin-integration-ats-api-recruiting-request-example-query.md).</span></span>
- <span data-ttu-id="c0132-139">**Kandidaten voor aanstelling** geeft details weer van een kandidaat die een aanbod voor een functie heeft geaccepteerd.</span><span class="sxs-lookup"><span data-stu-id="c0132-139">**CandidateToHire** represents details of a candidate who has accepted an offer for a position.</span></span> <span data-ttu-id="c0132-140">**Persoon** geeft de persoon weer die de kandidaat is.</span><span class="sxs-lookup"><span data-stu-id="c0132-140">**Person** represents the individual who is the candidate.</span></span> <span data-ttu-id="c0132-141">Een persoon kan meerdere rollen in het bedrijf hebben, zoals kandidaat, werknemer, medewerker of contractant.</span><span class="sxs-lookup"><span data-stu-id="c0132-141">A person can have multiple roles in the company, such as candidate, worker, employee, or contractor.</span></span> <span data-ttu-id="c0132-142">Zie [Voorbeeldquery voor Kandidaten voor aanstelling](hr-admin-integration-ats-api-candidate-to-hire-example-query.md) voor een voorbeeldquery.</span><span class="sxs-lookup"><span data-stu-id="c0132-142">For an example query, see [Example query for Candidate to hire](hr-admin-integration-ats-api-candidate-to-hire-example-query.md).</span></span>

<span data-ttu-id="c0132-143">In het volgende diagram worden de relaties binnen de API weergegeven.</span><span class="sxs-lookup"><span data-stu-id="c0132-143">The following diagram illustrates relationships within the API.</span></span> <span data-ttu-id="c0132-144">Verschillende typen hebben refererende sleutels voor andere, bestaande entiteiten in HumanResources die hier niet worden geïllustreerd.</span><span class="sxs-lookup"><span data-stu-id="c0132-144">Several types have foreign keys to other, pre-existing entities in Human Resources that aren't illustrated here.</span></span> <span data-ttu-id="c0132-145">Dit document bevat informatie over entiteiten die specifiek zijn voor wervingsintegratiescenario's.</span><span class="sxs-lookup"><span data-stu-id="c0132-145">This document provides information on entities that are specific to recruiting integration scenarios.</span></span> <span data-ttu-id="c0132-146">De Dataverse web-API voor Dynamics 365 Human Resources bevat echter een groot aantal andere entiteiten die ook relevant kunnen zijn voor uw integratie.</span><span class="sxs-lookup"><span data-stu-id="c0132-146">However, there are many other entities in the Dataverse Web API for Dynamics 365 Human Resources that may also be relevant to your integration.</span></span> <span data-ttu-id="c0132-147">U hebt bijvoorbeeld ook details nodig voor werknemers, functies, posities of andere entiteiten die hier niet zijn gedefinieerd.</span><span class="sxs-lookup"><span data-stu-id="c0132-147">For example, you may also need detail for workers, jobs, positions, or other entities not defined here.</span></span> <span data-ttu-id="c0132-148">Naar veel van deze entiteiten worden verwezen in refererende sleutelrelaties of navigatie-eigenschappen.</span><span class="sxs-lookup"><span data-stu-id="c0132-148">Many of these entities are referenced in foreign key relationships or navigation properties.</span></span>

![ATS-integratie API-gegevensmodel](media/hr-admin-integration-ats-api-data-model.png)

## <a name="recruiting-request-and-related-entities-and-option-sets"></a><span data-ttu-id="c0132-150">Wervingsaanvragen en gerelateerde entiteiten en optiesets</span><span class="sxs-lookup"><span data-stu-id="c0132-150">Recruiting request and related entities and option sets</span></span>

<span data-ttu-id="c0132-151">Voorbeeldquery:</span><span class="sxs-lookup"><span data-stu-id="c0132-151">Example query:</span></span> 

- [<span data-ttu-id="c0132-152">Voorbeeldquery voor wervingsaanvraag</span><span class="sxs-lookup"><span data-stu-id="c0132-152">Example query for Recruiting request</span></span>](hr-admin-integration-ats-api-recruiting-request-example-query.md)

<span data-ttu-id="c0132-153">Entiteiten:</span><span class="sxs-lookup"><span data-stu-id="c0132-153">Entities:</span></span>

- [<span data-ttu-id="c0132-154">Wervingsaanvraag</span><span class="sxs-lookup"><span data-stu-id="c0132-154">Recruiting request</span></span>](hr-admin-integration-ats-api-recruiting-request.md)
- [<span data-ttu-id="c0132-155">Positie van wervingsaanvraag</span><span class="sxs-lookup"><span data-stu-id="c0132-155">Recruiting request position</span></span>](hr-admin-integration-ats-api-recruiting-request-position.md)
- [<span data-ttu-id="c0132-156">Vaardigheid wervingsaanvraag</span><span class="sxs-lookup"><span data-stu-id="c0132-156">Recruiting request skill</span></span>](hr-admin-integration-ats-api-recruiting-request-skill.md)
- [<span data-ttu-id="c0132-157">Opleiding wervingsaanvraag</span><span class="sxs-lookup"><span data-stu-id="c0132-157">Recruiting request education</span></span>](hr-admin-integration-ats-api-recruiting-request-education.md)
- [<span data-ttu-id="c0132-158">Locatie van wervingsaanvraag</span><span class="sxs-lookup"><span data-stu-id="c0132-158">Recruiting request location</span></span>](hr-admin-integration-ats-api-recruiting-request-location.md)

<span data-ttu-id="c0132-159">Optiesets:</span><span class="sxs-lookup"><span data-stu-id="c0132-159">Option sets:</span></span>

- [<span data-ttu-id="c0132-160">Vrijstellingsstatus taak</span><span class="sxs-lookup"><span data-stu-id="c0132-160">Job exempt status</span></span>](hr-admin-integration-ats-api-job-exempt-status.md)
- [<span data-ttu-id="c0132-161">Positiestatus voor wervingsaanvragen</span><span class="sxs-lookup"><span data-stu-id="c0132-161">Recruiting request position status</span></span>](hr-admin-integration-ats-api-recruiting-request-position-status.md)
- [<span data-ttu-id="c0132-162">Status wervingsaanvraag</span><span class="sxs-lookup"><span data-stu-id="c0132-162">Recruiting request status</span></span>](hr-admin-integration-ats-api-recruiting-request-status.md)
- [<span data-ttu-id="c0132-163">Wettelijke taakcategorie</span><span class="sxs-lookup"><span data-stu-id="c0132-163">Regulatory job category</span></span>](hr-admin-integration-ats-api-regulatory-job-category.md)

## <a name="candidate-to-hire-and-related-entities-and-option-sets"></a><span data-ttu-id="c0132-164">Aan te stelledn kandidaat en gerelateerde entiteiten en optiesets</span><span class="sxs-lookup"><span data-stu-id="c0132-164">Candidate to hire and related entities and option sets</span></span>

<span data-ttu-id="c0132-165">Voorbeeldquery:</span><span class="sxs-lookup"><span data-stu-id="c0132-165">Example query:</span></span>

- [<span data-ttu-id="c0132-166">Voorbeeldquery voor Kandidaten voor aanstelling</span><span class="sxs-lookup"><span data-stu-id="c0132-166">Example query for Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)

<span data-ttu-id="c0132-167">Entiteiten:</span><span class="sxs-lookup"><span data-stu-id="c0132-167">Entities:</span></span>

- [<span data-ttu-id="c0132-168">Kandidaten voor aanstelling</span><span class="sxs-lookup"><span data-stu-id="c0132-168">Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire.md)
- [<span data-ttu-id="c0132-169">Persoon</span><span class="sxs-lookup"><span data-stu-id="c0132-169">Person</span></span>](hr-admin-integration-ats-api-person.md)
- [<span data-ttu-id="c0132-170">Opleiding van persoon</span><span class="sxs-lookup"><span data-stu-id="c0132-170">Person education</span></span>](hr-admin-integration-ats-api-person-education.md)
- [<span data-ttu-id="c0132-171">Werkervaring van persoon</span><span class="sxs-lookup"><span data-stu-id="c0132-171">Person professional experience</span></span>](hr-admin-integration-ats-api-person-professional-experience.md)
- [<span data-ttu-id="c0132-172">Adres van persoon</span><span class="sxs-lookup"><span data-stu-id="c0132-172">Person address</span></span>](hr-admin-integration-ats-api-person-address.md)
- [<span data-ttu-id="c0132-173">Contactpersoon partij</span><span class="sxs-lookup"><span data-stu-id="c0132-173">Party contact</span></span>](hr-admin-integration-ats-api-party-contact.md)
- [<span data-ttu-id="c0132-174">Vaardigheid van persoon</span><span class="sxs-lookup"><span data-stu-id="c0132-174">Person skill</span></span>](hr-admin-integration-ats-api-person-skill.md)
- [<span data-ttu-id="c0132-175">Beoordelingsniveau</span><span class="sxs-lookup"><span data-stu-id="c0132-175">Rating level</span></span>](hr-admin-integration-ats-api-rating-level.md)
- [<span data-ttu-id="c0132-176">Certificaat van persoon</span><span class="sxs-lookup"><span data-stu-id="c0132-176">Person certificate</span></span>](hr-admin-integration-ats-api-person-certificate.md)
- [<span data-ttu-id="c0132-177">Type certificaat</span><span class="sxs-lookup"><span data-stu-id="c0132-177">Certificate type</span></span>](hr-admin-integration-ats-api-certificate-type.md)
- [<span data-ttu-id="c0132-178">Persoonscreening</span><span class="sxs-lookup"><span data-stu-id="c0132-178">Person screening</span></span>](hr-admin-integration-ats-api-person-screening.md)
- [<span data-ttu-id="c0132-179">Screeningtypen</span><span class="sxs-lookup"><span data-stu-id="c0132-179">Screening types</span></span>](hr-admin-integration-ats-api-screening-types.md)
- [<span data-ttu-id="c0132-180">Persoonlijk identificatienummer</span><span class="sxs-lookup"><span data-stu-id="c0132-180">Person identification number</span></span>](hr-admin-integration-ats-api-person-identification-number.md)

<span data-ttu-id="c0132-181">Optiesets:</span><span class="sxs-lookup"><span data-stu-id="c0132-181">Option sets:</span></span>

- [<span data-ttu-id="c0132-182">Integratieresultaat van sollicitant</span><span class="sxs-lookup"><span data-stu-id="c0132-182">Applicant integration result</span></span>](hr-admin-integration-ats-api-applicant-integration-result.md)
- [<span data-ttu-id="c0132-183">Leeg Ja Nee</span><span class="sxs-lookup"><span data-stu-id="c0132-183">Blank Yes No</span></span>](hr-admin-integration-ats-api-blank-yes-no.md)
- [<span data-ttu-id="c0132-184">Status van voltooiing</span><span class="sxs-lookup"><span data-stu-id="c0132-184">Completion status</span></span>](hr-admin-integration-ats-api-completion-status.md)
- [<span data-ttu-id="c0132-185">Type contact</span><span class="sxs-lookup"><span data-stu-id="c0132-185">Contact type</span></span>](hr-admin-integration-ats-api-contact-type.md)
- [<span data-ttu-id="c0132-186">Basis van educatief tegoed</span><span class="sxs-lookup"><span data-stu-id="c0132-186">Education credit basis</span></span>](hr-admin-integration-ats-api-education-credit-basis.md)
- [<span data-ttu-id="c0132-187">Geslacht</span><span class="sxs-lookup"><span data-stu-id="c0132-187">Gender</span></span>](hr-admin-integration-ats-api-gender.md)
- [<span data-ttu-id="c0132-188">Burgerlijke staat</span><span class="sxs-lookup"><span data-stu-id="c0132-188">Marital status</span></span>](hr-admin-integration-ats-api-marital-status.md)
- [<span data-ttu-id="c0132-189">Maanden van jaar</span><span class="sxs-lookup"><span data-stu-id="c0132-189">Months of year</span></span>](hr-admin-integration-ats-api-months-of-year.md)
- [<span data-ttu-id="c0132-190">Nee Ja</span><span class="sxs-lookup"><span data-stu-id="c0132-190">No Yes</span></span>](hr-admin-integration-ats-api-no-yes.md)
- [<span data-ttu-id="c0132-191">Periode-eenheid</span><span class="sxs-lookup"><span data-stu-id="c0132-191">Period unit</span></span>](hr-admin-integration-ats-api-period-unit.md)
- [<span data-ttu-id="c0132-192">Screeningfrequentie</span><span class="sxs-lookup"><span data-stu-id="c0132-192">Screening frequency</span></span>](hr-admin-integration-ats-api-screening-frequency.md)
- [<span data-ttu-id="c0132-193">Screeningfrequentie genereren op basis van</span><span class="sxs-lookup"><span data-stu-id="c0132-193">Screening frequency generate from</span></span>](hr-admin-integration-ats-api-screening-frequency-generate-from.md)
- [<span data-ttu-id="c0132-194">Type vaardigheidsniveau</span><span class="sxs-lookup"><span data-stu-id="c0132-194">Skill level type</span></span>](hr-admin-integration-ats-api-skill-level-type.md)

## <a name="see-also"></a><span data-ttu-id="c0132-195">Zie ook</span><span class="sxs-lookup"><span data-stu-id="c0132-195">See also</span></span>

[<span data-ttu-id="c0132-196">Kandidaten werven</span><span class="sxs-lookup"><span data-stu-id="c0132-196">Recruit job candidates</span></span>](hr-personnel-recruit.md)<br>
[<span data-ttu-id="c0132-197">Wat is Microsoft Dataverse?</span><span class="sxs-lookup"><span data-stu-id="c0132-197">What is Microsoft Dataverse?</span></span>](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro)<br>
[<span data-ttu-id="c0132-198">De Microsoft Dataverse web-API gebruiken</span><span class="sxs-lookup"><span data-stu-id="c0132-198">Use the Microsoft Dataverse Web API</span></span>](https://docs.microsoft.com/powerapps/developer/data-platform/webapi/overview)<br>
[<span data-ttu-id="c0132-199">Optiesets maken en bijwerken met de web-API</span><span class="sxs-lookup"><span data-stu-id="c0132-199">Create and update option sets using the Web API</span></span>](https://docs.microsoft.com/powerapps/developer/data-platform/webapi/create-update-optionsets)<br>