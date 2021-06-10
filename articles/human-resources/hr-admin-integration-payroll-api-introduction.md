---
title: Inleiding bij API voor integratie van salarisadministratie
description: In dit onderwerp wordt de Salarisintegratie-API van Dynamics 365 Human Resources beschreven.
author: andreabichsel
ms.date: 02/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2021-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: e6d8a1cb9619a863184460a74e472af3f06934b6
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/18/2021
ms.locfileid: "6058555"
---
# <a name="payroll-integration-api-introduction"></a><span data-ttu-id="4d451-103">Inleiding bij API voor integratie van salarisadministratie</span><span class="sxs-lookup"><span data-stu-id="4d451-103">Payroll integration API introduction</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="4d451-104">In dit document wordt de Salarisintegratie-API van Dynamics 365 Human Resources beschreven.</span><span class="sxs-lookup"><span data-stu-id="4d451-104">This document describes the Dynamics 365 Human Resources Payroll integration API.</span></span> <span data-ttu-id="4d451-105">De API maakt complete en gestroomlijnde integraties tussen Human Resources en de partneradministratie mogelijk.</span><span class="sxs-lookup"><span data-stu-id="4d451-105">The API enables streamlined end-to-end integrations between Human Resources and partnering payroll systems.</span></span> <span data-ttu-id="4d451-106">De geïntegreerde ervaring begint in Human Resources met werknemersprofiel, salaris, inhoudingen en bijdragegegevens.</span><span class="sxs-lookup"><span data-stu-id="4d451-106">The integrated experience begins in Human Resources with the employee profile, salary and deduction, and contribution information.</span></span> <span data-ttu-id="4d451-107">Wanneer u een werknemer in dienst neemt en het vereiste profiel en salarisgegevens in Human Resources invoert, haalt de salarisadministratie de informatie op die wordt gebruikt bij de verwerking van salarissen.</span><span class="sxs-lookup"><span data-stu-id="4d451-107">When you hire an employee and enter the required profile and pay information into Human Resources, the payroll system pulls this information to use when processing payroll.</span></span> <span data-ttu-id="4d451-108">Updates van de werknemer- of salarisgegevens worden ook uitgevoerd voor latere salarisruns.</span><span class="sxs-lookup"><span data-stu-id="4d451-108">Any updates made to the employee or pay information are also pulled for use in later pay runs.</span></span>

![Integratiestroom van salarisadministratie](media/hr-admin-integration-payroll-api-introduction-flow.png)

<span data-ttu-id="4d451-110">Human Resources bevat de volgende onderdelen om de integratie in te schakelen:</span><span class="sxs-lookup"><span data-stu-id="4d451-110">To enable the integration, Human Resources includes the following components:</span></span>

- <span data-ttu-id="4d451-111">Functionaliteit om een werknemer te markeren als gereed voor betaling</span><span class="sxs-lookup"><span data-stu-id="4d451-111">Functionality to mark an employee as ready to pay</span></span>
- <span data-ttu-id="4d451-112">Een integratie-API die de nieuwe functionaliteit opent voor de integratie van toepassingen</span><span class="sxs-lookup"><span data-stu-id="4d451-112">An integration API opening up the new functionality to integrating applications</span></span>

## <a name="microsoft-dataverse"></a><span data-ttu-id="4d451-113">Microsoft Dataverse</span><span class="sxs-lookup"><span data-stu-id="4d451-113">Microsoft Dataverse</span></span>

<span data-ttu-id="4d451-114">Deze API is gebouwd op Microsoft Dataverse (voorheen Common Data Service).</span><span class="sxs-lookup"><span data-stu-id="4d451-114">This API is built on Microsoft Dataverse (formerly Common Data Service).</span></span> <span data-ttu-id="4d451-115">Alle RESTful-interactie met deze API gaat via de Microsoft Dataverse web-API, die OData gebruikt.</span><span class="sxs-lookup"><span data-stu-id="4d451-115">All RESTful interaction with this API is done via the Microsoft Dataverse Web API, which uses OData.</span></span> <span data-ttu-id="4d451-116">Deze API is een subset van de Dataverse web-API.</span><span class="sxs-lookup"><span data-stu-id="4d451-116">This API is a subset of the Dataverse Web API.</span></span> <span data-ttu-id="4d451-117">De Dataverse web-API definieert kenmerken als verificatie, SLA's, batch, gelijktijdigheidscontrole en foutverwerking.</span><span class="sxs-lookup"><span data-stu-id="4d451-117">The Dataverse Web API defines characteristics such as authentication, SLAs, batch, concurrency control, and error handling.</span></span>

<span data-ttu-id="4d451-118">Voor meer algemene informatie over de Microsoft Dataverse web-API, zie:</span><span class="sxs-lookup"><span data-stu-id="4d451-118">For more general information about the Microsoft Dataverse Web API, see:</span></span>

- [<span data-ttu-id="4d451-119">Wat is Microsoft Dataverse?</span><span class="sxs-lookup"><span data-stu-id="4d451-119">What is Microsoft Dataverse?</span></span>](/powerapps/maker/data-platform/data-platform-intro)
- [<span data-ttu-id="4d451-120">De Microsoft Dataverse web-API gebruiken</span><span class="sxs-lookup"><span data-stu-id="4d451-120">Use the Microsoft Dataverse Web API</span></span>](/powerapps/developer/data-platform/webapi/overview)
- [<span data-ttu-id="4d451-121">Microsoft Dataverse ontwikkelaarshandleiding</span><span class="sxs-lookup"><span data-stu-id="4d451-121">Microsoft Dataverse developer guide</span></span>](/powerapps/developer/data-platform)

<span data-ttu-id="4d451-122">Deze documentatie bevat details en richtlijnen voor ontwikkelaars van de Dataverse-web-API, waaronder de volgende onderwerpen:</span><span class="sxs-lookup"><span data-stu-id="4d451-122">This documentation includes details and developer guidance for using the Dataverse Web API, including the following topics:</span></span>

- [<span data-ttu-id="4d451-123">Verifiëren bij Microsoft Dataverse met de web-API</span><span class="sxs-lookup"><span data-stu-id="4d451-123">Authenticate to Microsoft Dataverse with the Web API</span></span>](/powerapps/developer/data-platform/webapi/authenticate-web-api)
- [<span data-ttu-id="4d451-124">Bewerkingen uitvoeren met de web-API</span><span class="sxs-lookup"><span data-stu-id="4d451-124">Perform operations using the Web API</span></span>](/powerapps/developer/data-platform/webapi/perform-operations-web-api)
- [<span data-ttu-id="4d451-125">Postman gebruiken met de web-API</span><span class="sxs-lookup"><span data-stu-id="4d451-125">Use Postman with the Web API</span></span>](/powerapps/developer/data-platform/webapi/use-postman-web-api)
- [<span data-ttu-id="4d451-126">Wijzigingen bijhouden voor het synchroniseren van gegevens met externe systemen</span><span class="sxs-lookup"><span data-stu-id="4d451-126">Use change tracking to synchronize data with external systems</span></span>](/powerapps/developer/data-platform/use-change-tracking-synchronize-data-external-systems)

### <a name="virtual-tables-for-human-resources-in-dataverse"></a><span data-ttu-id="4d451-127">Virtuele tabellen in Dataverse voor Human Resources</span><span class="sxs-lookup"><span data-stu-id="4d451-127">Virtual tables for Human Resources in Dataverse</span></span>

<span data-ttu-id="4d451-128">De eindpunten voor de API voor Salarisintegratie maken gebruik van de mogelijkheden van het virtuele tabelplatform van Microsoft Dataverse.</span><span class="sxs-lookup"><span data-stu-id="4d451-128">The endpoints for the Payroll integration API use the virtual table platform capabilities of Microsoft Dataverse.</span></span> <span data-ttu-id="4d451-129">Standaard worden de virtuele tabellen en de bijbehorende API-eindpunten niet geïmplementeerd voor Human Resources-omgevingen, waardoor organisaties kunnen bepalen welke OData-eindpunten beschikbaar worden voor de omgeving.</span><span class="sxs-lookup"><span data-stu-id="4d451-129">By default, the virtual tables and their associated API endpoints aren't deployed for Human Resources environments, enabling organizations to determine which OData endpoints will be exposed for the environment.</span></span> <span data-ttu-id="4d451-130">Als u de API wilt gebruiken, moeten de virtuele tabellen voor de Human Resources-entiteiten worden gegenereerd voor de omgeving.</span><span class="sxs-lookup"><span data-stu-id="4d451-130">To use the API, the virtual tables for the Human Resources entities must be generated for the environment.</span></span>

<span data-ttu-id="4d451-131">Zie [Dataverse virtuele tabellen configureren](./hr-admin-integration-common-data-service-virtual-entities.md) voor informatie over het genereren van de virtuele tabellen voor de API.</span><span class="sxs-lookup"><span data-stu-id="4d451-131">For information on generating the virtual tables for the API, see [Configure Dataverse virtual tables](./hr-admin-integration-common-data-service-virtual-entities.md).</span></span>

## <a name="data-model"></a><span data-ttu-id="4d451-132">Gegevensmodel</span><span class="sxs-lookup"><span data-stu-id="4d451-132">Data model</span></span>

<span data-ttu-id="4d451-133">In het volgende diagram worden de relaties binnen de API weergegeven.</span><span class="sxs-lookup"><span data-stu-id="4d451-133">The following diagram illustrates relationships within the API.</span></span> <span data-ttu-id="4d451-134">Verschillende typen hebben refererende sleutels voor andere, bestaande entiteiten in HumanResources die hier niet worden geïllustreerd.</span><span class="sxs-lookup"><span data-stu-id="4d451-134">Several types have foreign keys to other, pre-existing entities in Human Resources that aren't illustrated here.</span></span> <span data-ttu-id="4d451-135">Dit document bevat informatie over entiteiten die specifiek zijn voor salarisintegratiescenario's.</span><span class="sxs-lookup"><span data-stu-id="4d451-135">This document provides information on entities that are specific to payroll integration scenarios.</span></span> <span data-ttu-id="4d451-136">De Dataverse web-API voor Human Resources bevat echter een groot aantal andere entiteiten die ook relevant kunnen zijn voor uw integratie.</span><span class="sxs-lookup"><span data-stu-id="4d451-136">However, there are many other entities in the Dataverse Web API for Human Resources that may also be relevant to your integration.</span></span> <span data-ttu-id="4d451-137">Naar sommige van deze entiteiten worden verwezen in refererende sleutelrelaties of navigatie-eigenschappen.</span><span class="sxs-lookup"><span data-stu-id="4d451-137">Some of these entities are referenced in foreign key relationships or navigation properties.</span></span>

![Salarisintegratie API-gegevensmodel](media/hr-admin-payroll-api-data-model.png)

## <a name="payroll-employee-and-related-entities"></a><span data-ttu-id="4d451-139">Salariswerker en gerelateerde entiteiten</span><span class="sxs-lookup"><span data-stu-id="4d451-139">Payroll employee and related entities</span></span>

<span data-ttu-id="4d451-140">Entiteiten:</span><span class="sxs-lookup"><span data-stu-id="4d451-140">Entities:</span></span>

- [<span data-ttu-id="4d451-141">Werknemer in salarisadministratie</span><span class="sxs-lookup"><span data-stu-id="4d451-141">Payroll employee</span></span>](hr-admin-integration-payroll-api-payroll-employee.md)
- [<span data-ttu-id="4d451-142">Adres medewerker salarisadministratie</span><span class="sxs-lookup"><span data-stu-id="4d451-142">Payroll worker address</span></span>](hr-admin-integration-payroll-api-payroll-worker-address.md)
- [<span data-ttu-id="4d451-143">Vast compensatieplan in salarisadministratie</span><span class="sxs-lookup"><span data-stu-id="4d451-143">Payroll fixed compensation plan</span></span>](hr-admin-integration-ats-api-recruiting-request-education.md)
- [<span data-ttu-id="4d451-144">Salarispositiefunctie</span><span class="sxs-lookup"><span data-stu-id="4d451-144">Payroll position job</span></span>](hr-admin-integration-payroll-api-payroll-position-job.md)
- [<span data-ttu-id="4d451-145">Salarispositie</span><span class="sxs-lookup"><span data-stu-id="4d451-145">Payroll position</span></span>](hr-admin-integration-payroll-api-payroll-position.md)

## <a name="see-also"></a><span data-ttu-id="4d451-146">Zie ook</span><span class="sxs-lookup"><span data-stu-id="4d451-146">See also</span></span>

[<span data-ttu-id="4d451-147">Entiteiten voor salarisadministratie genereren en beoordelen</span><span class="sxs-lookup"><span data-stu-id="4d451-147">Generate and review payroll entities</span></span>](hr-admin-integration-payroll-api-generate-review-entities.md)<br>
[<span data-ttu-id="4d451-148">Human Resources-parameters configureren</span><span class="sxs-lookup"><span data-stu-id="4d451-148">Configure Human Resources parameters</span></span>](hr-setup-parameters.md)<br>
[<span data-ttu-id="4d451-149">Gedeelde Human Resources-parameters onderhouden</span><span class="sxs-lookup"><span data-stu-id="4d451-149">Configure Human Resources shared parameters</span></span>](hr-setup-shared-parameters.md)<br>
[<span data-ttu-id="4d451-150">Wat is Microsoft Dataverse?</span><span class="sxs-lookup"><span data-stu-id="4d451-150">What is Microsoft Dataverse?</span></span>](/powerapps/maker/data-platform/data-platform-intro)<br>
[<span data-ttu-id="4d451-151">De Microsoft Dataverse web-API gebruiken</span><span class="sxs-lookup"><span data-stu-id="4d451-151">Use the Microsoft Dataverse Web API</span></span>](/powerapps/developer/data-platform/webapi/overview)<br>

[!INCLUDE[footer-include](../includes/footer-banner.md)]