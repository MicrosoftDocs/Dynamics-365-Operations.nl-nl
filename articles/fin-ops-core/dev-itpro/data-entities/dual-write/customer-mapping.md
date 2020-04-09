---
title: Geïntegreerd klantmodel
description: In dit onderwerp wordt de integratie van klantgegevens tussen Finance and Operations en Common Data Service beschreven.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 07/15/2019
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
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 977b74b10b4549d09a8816264f9ff603fa86e91c
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/27/2020
ms.locfileid: "3172826"
---
# <a name="integrated-customer-master"></a><span data-ttu-id="acbda-103">Model voor geïntegreerde klanten</span><span class="sxs-lookup"><span data-stu-id="acbda-103">Integrated customer master</span></span>

[!include [banner](../../includes/banner.md)]


<span data-ttu-id="acbda-104">Klantgegevens kunnen in meerdere Dynamics 365-toepassingen worden beheerd.</span><span class="sxs-lookup"><span data-stu-id="acbda-104">Customer data can be mastered in more than one Dynamics 365 application.</span></span> <span data-ttu-id="acbda-105">Een klantrecord kan bijvoorbeeld afkomstig zijn van een verkoopactiviteit in Dynamics 365 Sales (een modelgestuurde app in Dynamics 365) of een record die afkomstig is van een detailhandelactiviteit in Dynamics 365 Commerce (een Finance and Operations-app).</span><span class="sxs-lookup"><span data-stu-id="acbda-105">For example, a customer record can originate though sales activity in Dynamics 365 Sales (a model-driven app in Dynamics 365), or a record can originate through retail activity in Dynamics 365 Commerce (a Finance and Operations app).</span></span> <span data-ttu-id="acbda-106">Ongeacht waar de klantgegevens vandaan komen, ze worden achter de schermen geïntegreerd.</span><span class="sxs-lookup"><span data-stu-id="acbda-106">No matter where where the customer data originates, it is integrated behind the scenes.</span></span> <span data-ttu-id="acbda-107">Met het geïntegreerde klantmodel hebt u de flexibiliteit om de hoofdgegevens van klanten te beheren in elke Dynamics 365-toepassing met een uitgebreid overzicht van de klant in de Dynamics 365-toepassingsreeks.</span><span class="sxs-lookup"><span data-stu-id="acbda-107">Integrated customer master gives you the flexibility to master customer data in any Dynamics 365 application and provides a comprehensive view of the customer across the Dynamics 365 application suite.</span></span>

## <a name="customer-data-flow"></a><span data-ttu-id="acbda-108">Klantgegevensstroom</span><span class="sxs-lookup"><span data-stu-id="acbda-108">Customer data flow</span></span>

<span data-ttu-id="acbda-109">*Klant* is een goed gedefinieerd concept in toepassingen.</span><span class="sxs-lookup"><span data-stu-id="acbda-109">*Customer* is a well-defined concept in applications.</span></span> <span data-ttu-id="acbda-110">Daarom bestaat de integratie van klantgegevens alleen uit het harmoniseren van het klantconcept tussen de twee toepassingen.</span><span class="sxs-lookup"><span data-stu-id="acbda-110">Therefore, the integration of customer data just involves harmonizing the customer concept between the two applications.</span></span> <span data-ttu-id="acbda-111">In de volgende afbeelding wordt de klantgegevensstroom weergegeven.</span><span class="sxs-lookup"><span data-stu-id="acbda-111">The following illustration shows the customer data flow.</span></span>

![Klantgegevensstroom](media/dual-write-customer-data-flow.png)

<span data-ttu-id="acbda-113">Klanten kunnen globaal worden ingedeeld in twee typen: commerciële/organisatorische klanten en consumenten/eindgebruikers.</span><span class="sxs-lookup"><span data-stu-id="acbda-113">Customers can be broadly classified into two types: commercial/organizational customers and consumers/end users.</span></span> <span data-ttu-id="acbda-114">Deze twee typen klanten worden in Finance and Operations en Common Data Service op een andere manier opgeslagen en verwerkt.</span><span class="sxs-lookup"><span data-stu-id="acbda-114">These two types of customers are stored and handled differently in Finance and Operations and Common Data Service.</span></span>

<span data-ttu-id="acbda-115">In Finance and Operations worden zowel commerciële/organisatieklanten als consumenten/eindgebruikers in één tabel met de naam **CustTable** (CustomerCustomerV3Entity) beheerd en worden ze geclassificeerd op basis van het kenmerk **Type**.</span><span class="sxs-lookup"><span data-stu-id="acbda-115">In Finance and Operations, both commercial/organizational customers and consumers/end users are mastered in a single table that is named **CustTable** (CustomerCustomerV3Entity), and they are classified based on the **Type** attribute.</span></span> <span data-ttu-id="acbda-116">(Als **Type** is ingesteld op **Organisatie**, is de klant een commerciële/organisatorische klant en als **Type** is ingesteld op **Persoon**, is de klant een consument/eindgebruiker.) De primaire contactpersoonsgegevens worden afgehandeld via de entiteit SMMContactPersonEntity.</span><span class="sxs-lookup"><span data-stu-id="acbda-116">(If **Type** is set to **Organization**, the customer is a commercial/organizational customer, and if **Type** is set to **Person**, the customer is a consumer/end user.) The primary contact person information is handled through the SMMContactPersonEntity entity.</span></span>

<span data-ttu-id="acbda-117">In Common Data Service worden commerciële/organisatorische klanten beheerd in het entiteit Account en worden ze geïdentificeerd als het kenmerk **RelationshipType** kenmerk is ingesteld op **Klant**.</span><span class="sxs-lookup"><span data-stu-id="acbda-117">In Common Data Service, commercial/organizational customers are mastered in the Account entity and are identified as customers when the **RelationshipType** attribute is set to **Customer**.</span></span> <span data-ttu-id="acbda-118">Zowel consumenten/eindgebruikers als de contactpersoon worden vertegenwoordigd door entiteit Contactpersoon.</span><span class="sxs-lookup"><span data-stu-id="acbda-118">Both consumers/end users and the contact person are represented by the Contact entity.</span></span> <span data-ttu-id="acbda-119">Om een duidelijke scheiding te maken tussen een consument/eindgebruiker en een contactpersoon, heeft de entiteit **Contactpersoon** een Booleaanse vlag met de naam **Verkoopbaar**.</span><span class="sxs-lookup"><span data-stu-id="acbda-119">To provide a clear separation between a consumer/end user and a contact person, the **Contact** entity has a Boolean flag that is named **Sellable**.</span></span> <span data-ttu-id="acbda-120">Wanneer **Verkoopbaar** de waarde **Waar** heeft, is de contactpersoon een consument/eindgebruiker en kunnen er voor die contactpersoon offertes en orders worden gemaakt.</span><span class="sxs-lookup"><span data-stu-id="acbda-120">When **Sellable** is **True**, the contact is a consumer/end user, and quotations and orders can be created for that contact.</span></span> <span data-ttu-id="acbda-121">Als **Verkoopbaar** is ingesteld op **Onwaar**, is de contactpersoon slechts een primaire contactpersoon van een klant.</span><span class="sxs-lookup"><span data-stu-id="acbda-121">When **Sellable** is **False**, the contact is just a primary contact person of a customer.</span></span>

<span data-ttu-id="acbda-122">Wanneer een niet-verkoopbare contactpersoon deelneemt aan een offerte- of orderproces, is **Verkoopbaar** ingesteld op **Waar** om de contactpersoon te markeren als een verkoopbaar contact.</span><span class="sxs-lookup"><span data-stu-id="acbda-122">When a non-sellable contact participates in a quotation or order process, **Sellable** is set to **True** to flag the contact as a sellable contact.</span></span> <span data-ttu-id="acbda-123">Een contactpersoon die een verkoopbaar contact is geworden, blijft een verkoopbaar contact.</span><span class="sxs-lookup"><span data-stu-id="acbda-123">A contact that has become a sellable contact remains a sellable contact.</span></span>

## <a name="templates"></a><span data-ttu-id="acbda-124">Sjablonen</span><span class="sxs-lookup"><span data-stu-id="acbda-124">Templates</span></span>

<span data-ttu-id="acbda-125">Klantgegevens omvatten alle informatie over de klant, zoals de klantgroep, adressen, contactgegevens, betalingsprofiel en factuurprofiel.</span><span class="sxs-lookup"><span data-stu-id="acbda-125">Customer data includes all information about the customer, such as the customer group, addresses, contact information, payment profile, invoice profile, and loyalty status.</span></span> <span data-ttu-id="acbda-126">Een verzameling entiteitstoewijzingen werkt samen tijdens interactie met klantgegevens, zoals in de volgende tabel wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="acbda-126">A collection of entity maps works together during customer data interaction, as shown in the following table.</span></span>

<span data-ttu-id="acbda-127">Finance and Operations-apps</span><span class="sxs-lookup"><span data-stu-id="acbda-127">Finance and Operations apps</span></span> | <span data-ttu-id="acbda-128">Andere Dynamics 365-apps</span><span class="sxs-lookup"><span data-stu-id="acbda-128">Other Dynamics 365 apps</span></span>         | <span data-ttu-id="acbda-129">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="acbda-129">Description</span></span>
----------------------------|---------------------------------|------------
<span data-ttu-id="acbda-130">CDS-contactpersonen V2</span><span class="sxs-lookup"><span data-stu-id="acbda-130">CDS Contacts V2</span></span>             | <span data-ttu-id="acbda-131">contacten</span><span class="sxs-lookup"><span data-stu-id="acbda-131">contacts</span></span>                        | <span data-ttu-id="acbda-132">Met deze sjabloon worden alle primaire, secundaire en tertiaire contactgegevens voor zowel klanten als leveranciers gesynchroniseerd.</span><span class="sxs-lookup"><span data-stu-id="acbda-132">This template synchronizes all primary, secondary, and tertiary contact information, for both customers and vendors.</span></span>
<span data-ttu-id="acbda-133">Klantengroepen</span><span class="sxs-lookup"><span data-stu-id="acbda-133">Customer groups</span></span>             | <span data-ttu-id="acbda-134">msdyn_customergroups</span><span class="sxs-lookup"><span data-stu-id="acbda-134">msdyn_customergroups</span></span>            | <span data-ttu-id="acbda-135">Met deze sjabloon worden klantengroepgegevens gesynchroniseerd.</span><span class="sxs-lookup"><span data-stu-id="acbda-135">This template synchronizes customer group information.</span></span>
<span data-ttu-id="acbda-136">Betalingsmethode van klant</span><span class="sxs-lookup"><span data-stu-id="acbda-136">Customer payment method</span></span>     | <span data-ttu-id="acbda-137">msdyn_customerpaymentmethods</span><span class="sxs-lookup"><span data-stu-id="acbda-137">msdyn_customerpaymentmethods</span></span>    | <span data-ttu-id="acbda-138">Met deze sjabloon worden gegevens over de betalingsmethoden van klanten gesynchroniseerd.</span><span class="sxs-lookup"><span data-stu-id="acbda-138">This template synchronizes customer payment method information.</span></span>
<span data-ttu-id="acbda-139">Klanten V3</span><span class="sxs-lookup"><span data-stu-id="acbda-139">Customers V3</span></span>                | <span data-ttu-id="acbda-140">rekeningen</span><span class="sxs-lookup"><span data-stu-id="acbda-140">accounts</span></span>                        | <span data-ttu-id="acbda-141">Met deze sjabloon worden klantmodelgegevens voor commerciële en organisatorische klanten gesynchroniseerd.</span><span class="sxs-lookup"><span data-stu-id="acbda-141">This template synchronizes customer master information for commercial and organizational customers.</span></span>
<span data-ttu-id="acbda-142">Klanten V3</span><span class="sxs-lookup"><span data-stu-id="acbda-142">Customers V3</span></span>                | <span data-ttu-id="acbda-143">contacten</span><span class="sxs-lookup"><span data-stu-id="acbda-143">contacts</span></span>                        | <span data-ttu-id="acbda-144">Met deze sjabloon worden klantmodelgegevens voor consumenten en eindgebruikers gesynchroniseerd.</span><span class="sxs-lookup"><span data-stu-id="acbda-144">This template synchronizes customer master data for consumers and end users.</span></span>
<span data-ttu-id="acbda-145">Voor- en achtervoegsel naam</span><span class="sxs-lookup"><span data-stu-id="acbda-145">Name affixes</span></span>                | <span data-ttu-id="acbda-146">msdyn_nameaffixes</span><span class="sxs-lookup"><span data-stu-id="acbda-146">msdyn_nameaffixes</span></span>               | <span data-ttu-id="acbda-147">Met deze sjabloon worden referentiegegevens over voor- en achtervoegsels van namen voor zowel klanten als leveranciers gesynchroniseerd.</span><span class="sxs-lookup"><span data-stu-id="acbda-147">This template synchronizes name affixes reference data, for both customers and vendors.</span></span>
<span data-ttu-id="acbda-148">Betalingsdagregels CDS V2</span><span class="sxs-lookup"><span data-stu-id="acbda-148">Payment day lines CDS V2</span></span>    | <span data-ttu-id="acbda-149">msdyn_paymentdaylines</span><span class="sxs-lookup"><span data-stu-id="acbda-149">msdyn_paymentdaylines</span></span>           | <span data-ttu-id="acbda-150">Met deze sjabloon worden referentiegegevens over betalingsdagregels voor zowel klanten als leveranciers gesynchroniseerd.</span><span class="sxs-lookup"><span data-stu-id="acbda-150">This template synchronizes payment day lines reference data, for both customers and vendors.</span></span>
<span data-ttu-id="acbda-151">Betalingsdagen CDS</span><span class="sxs-lookup"><span data-stu-id="acbda-151">Payment days CDS</span></span>            | <span data-ttu-id="acbda-152">msdyn_paymentdays</span><span class="sxs-lookup"><span data-stu-id="acbda-152">msdyn_paymentdays</span></span>               | <span data-ttu-id="acbda-153">Met deze sjabloon worden referentiegegevens over betalingsdagen voor zowel klanten als leveranciers gesynchroniseerd.</span><span class="sxs-lookup"><span data-stu-id="acbda-153">This template synchronizes payment days reference data, for both customers and vendors.</span></span>
<span data-ttu-id="acbda-154">Regels van betalingsschema</span><span class="sxs-lookup"><span data-stu-id="acbda-154">Payment schedule lines</span></span>      | <span data-ttu-id="acbda-155">msdyn_paymentschedulelines</span><span class="sxs-lookup"><span data-stu-id="acbda-155">msdyn_paymentschedulelines</span></span>      | <span data-ttu-id="acbda-156">Met deze sjabloon worden referentiegegevens over betalingsschemaregels voor zowel klanten als leveranciers gesynchroniseerd.</span><span class="sxs-lookup"><span data-stu-id="acbda-156">Syncs payment schedule lines reference data, for both customers and vendors.</span></span>
<span data-ttu-id="acbda-157">Betalingsplanning</span><span class="sxs-lookup"><span data-stu-id="acbda-157">Payment schedule</span></span>            | <span data-ttu-id="acbda-158">msdyn_paymentschedules</span><span class="sxs-lookup"><span data-stu-id="acbda-158">msdyn_paymentschedules</span></span>          | <span data-ttu-id="acbda-159">Met deze sjabloon worden referentiegegevens over betalingsschema's voor zowel klanten als leveranciers gesynchroniseerd.</span><span class="sxs-lookup"><span data-stu-id="acbda-159">This template synchronizes payment schedule reference data, for both customers and vendors.</span></span>
<span data-ttu-id="acbda-160">Betalingstermijnen</span><span class="sxs-lookup"><span data-stu-id="acbda-160">Terms of payment</span></span>            | <span data-ttu-id="acbda-161">msdyn_paymentterms</span><span class="sxs-lookup"><span data-stu-id="acbda-161">msdyn_paymentterms</span></span>              | <span data-ttu-id="acbda-162">Met deze sjabloon worden referentiegegevens over betalingsvoorwaarden (voorwaarden voor betaling) voor zowel klanten als leveranciers gesynchroniseerd.</span><span class="sxs-lookup"><span data-stu-id="acbda-162">This template synchronizes payment terms (terms of payment) reference data, for both customers and vendors.</span></span>

[!include [banner](../../includes/dual-write-symbols.md)]

[!include [mapping contacts contacts](includes/CDSContactsV2-contacts.md)]

[!include [mapping customer group](includes/CustCustomerGroup-msdyn-customergroups.md)]

[!include [mapping customer payment method](includes/CustomerPaymentMethod-msdyn-customerpaymentmethods.md)]

[!include [mapping customer accounts](includes/CustomersV3-accounts.md)]

[!include [mapping customer contacts](includes/CustomersV3-contacts.md)]

[!include [mapping name affixes](includes/NameAffixes-msdyn-nameaffixes.md)]

[!include [mapping payment day lines](includes/PaymentDayLinesCdsV2-msdyn-paymentdaylines.md)]

[!include [mapping payment days](includes/PaymentDaysCds-msdyn-paymentdays.md)]

[!include [mapping payment schedule lines](includes/PaymentScheduleLines-msdyn-paymentschedulelines.md)]

[!include [mapping payment schedules](includes/PaymentSchedules-msdyn-paymentschedules.md)]

[!include [mapping terms of payment](includes/TermsofPayment-msdyn-paymentterms.md)]
