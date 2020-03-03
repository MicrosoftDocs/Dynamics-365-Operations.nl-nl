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
ms.openlocfilehash: 269346d38eeb3812c352d16f9d50fbcd09307c12
ms.sourcegitcommit: 54baab2a04e5c534fc2d1fd67b67e23a152d4e57
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/04/2020
ms.locfileid: "3019723"
---
# <a name="integrated-customer-master"></a><span data-ttu-id="51d38-103">Model voor geïntegreerde klanten</span><span class="sxs-lookup"><span data-stu-id="51d38-103">Integrated customer master</span></span>

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]

<span data-ttu-id="51d38-104">Het is gebruikelijk dat klantrecords in meer dan één toepassing worden beheerst.</span><span class="sxs-lookup"><span data-stu-id="51d38-104">It's typical for customer records to be mastered in more than one application.</span></span> <span data-ttu-id="51d38-105">Verkoopactiviteiten kunnen bijvoorbeeld commerciële klantrecords inbrengen via een Sales-toepassing en e-Commerce- of Retail-verkopen kunnen klantrecords inbrengen via een Finance and Operations-toepassing.</span><span class="sxs-lookup"><span data-stu-id="51d38-105">For example, sales activity can bring in commercial customer records through a Sales application, and e-Commerce or retail sales can bring in customer records through a Finance and Operations application.</span></span> <span data-ttu-id="51d38-106">Ongeacht waar de klantgegevens vandaan komen, worden ze achter de schermen geïntegreerd over toepassingsgrenzen en infrastructuurverschillen heen.</span><span class="sxs-lookup"><span data-stu-id="51d38-106">Regardless of where the customer record originates, it's integrated behind the scenes across application boundaries and infrastructure differences.</span></span> <span data-ttu-id="51d38-107">Geïntegreerd klantbeheer helpt bij het afhandelen van scenario's met meervoudig beheer en biedt een uitgebreid overzicht van de klant naar de Dynamics 365 Application Suite.</span><span class="sxs-lookup"><span data-stu-id="51d38-107">Integrated customer mastering helps handle multi-mastering scenarios and provides a comprehensive view of the customer to the Dynamics 365 application suite.</span></span>

## <a name="customer-data-flow"></a><span data-ttu-id="51d38-108">Klantgegevensstroom</span><span class="sxs-lookup"><span data-stu-id="51d38-108">Customer data flow</span></span>

<span data-ttu-id="51d38-109">*Klant* is een goed gedefinieerd concept in toepassingen.</span><span class="sxs-lookup"><span data-stu-id="51d38-109">*Customer* is a well-defined concept in applications.</span></span> <span data-ttu-id="51d38-110">Daarom bestaat de integratie van klantgegevens alleen uit het harmoniseren van het klantconcept tussen de twee toepassingen.</span><span class="sxs-lookup"><span data-stu-id="51d38-110">Therefore, the integration of customer data just involves harmonizing the customer concept between the two applications.</span></span> <span data-ttu-id="51d38-111">In de volgende afbeelding wordt de klantgegevensstroom weergegeven.</span><span class="sxs-lookup"><span data-stu-id="51d38-111">The following illustration shows the customer data flow.</span></span>

![Klantgegevensstroom](media/dual-write-customer-data-flow.png)

<span data-ttu-id="51d38-113">Klanten kunnen globaal worden ingedeeld in twee typen: commerciële/organisatorische klanten en consumenten/eindgebruikers.</span><span class="sxs-lookup"><span data-stu-id="51d38-113">Customers can be broadly classified into two types: commercial/organizational customers and consumers/end users.</span></span> <span data-ttu-id="51d38-114">Deze twee typen klanten worden in Finance and Operations en Common Data Service op een andere manier opgeslagen en verwerkt.</span><span class="sxs-lookup"><span data-stu-id="51d38-114">These two types of customers are stored and handled differently in Finance and Operations and Common Data Service.</span></span>

<span data-ttu-id="51d38-115">In Finance and Operations worden zowel commerciële/organisatieklanten als consumenten/eindgebruikers in één tabel met de naam **CustTable** (CustomerCustomerV3Entity) beheerd en worden ze geclassificeerd op basis van het kenmerk **Type**.</span><span class="sxs-lookup"><span data-stu-id="51d38-115">In Finance and Operations, both commercial/organizational customers and consumers/end users are mastered in a single table that is named **CustTable** (CustomerCustomerV3Entity), and they are classified based on the **Type** attribute.</span></span> <span data-ttu-id="51d38-116">(Als **Type** is ingesteld op **Organisatie**, is de klant een commerciële/organisatorische klant en als **Type** is ingesteld op **Persoon**, is de klant een consument/eindgebruiker.) De primaire contactpersoonsgegevens worden afgehandeld via de entiteit SMMContactPersonEntity.</span><span class="sxs-lookup"><span data-stu-id="51d38-116">(If **Type** is set to **Organization**, the customer is a commercial/organizational customer, and if **Type** is set to **Person**, the customer is a consumer/end user.) The primary contact person information is handled through the SMMContactPersonEntity entity.</span></span>

<span data-ttu-id="51d38-117">In Common Data Service worden commerciële/organisatorische klanten beheerd in het entiteit Account en worden ze geïdentificeerd als het kenmerk **RelationshipType** kenmerk is ingesteld op **Klant**.</span><span class="sxs-lookup"><span data-stu-id="51d38-117">In Common Data Service, commercial/organizational customers are mastered in the Account entity and are identified as customers when the **RelationshipType** attribute is set to **Customer**.</span></span> <span data-ttu-id="51d38-118">Zowel consumenten/eindgebruikers als de contactpersoon worden vertegenwoordigd door entiteit Contactpersoon.</span><span class="sxs-lookup"><span data-stu-id="51d38-118">Both consumers/end users and the contact person are represented by the Contact entity.</span></span> <span data-ttu-id="51d38-119">Om een duidelijke scheiding te maken tussen een consument/eindgebruiker en een contactpersoon, heeft de entiteit **Contactpersoon** een Booleaanse vlag met de naam **Verkoopbaar**.</span><span class="sxs-lookup"><span data-stu-id="51d38-119">To provide a clear separation between a consumer/end user and a contact person, the **Contact** entity has a Boolean flag that is named **Sellable**.</span></span> <span data-ttu-id="51d38-120">Wanneer **Verkoopbaar** de waarde **Waar** heeft, is de contactpersoon een consument/eindgebruiker en kunnen er voor die contactpersoon offertes en orders worden gemaakt.</span><span class="sxs-lookup"><span data-stu-id="51d38-120">When **Sellable** is **True**, the contact is a consumer/end user, and quotations and orders can be created for that contact.</span></span> <span data-ttu-id="51d38-121">Als **Verkoopbaar** is ingesteld op **Onwaar**, is de contactpersoon slechts een primaire contactpersoon van een klant.</span><span class="sxs-lookup"><span data-stu-id="51d38-121">When **Sellable** is **False**, the contact is just a primary contact person of a customer.</span></span>

<span data-ttu-id="51d38-122">Wanneer een niet-verkoopbare contactpersoon deelneemt aan een offerte- of orderproces, is **Verkoopbaar** ingesteld op **Waar** om de contactpersoon te markeren als een verkoopbaar contact.</span><span class="sxs-lookup"><span data-stu-id="51d38-122">When a non-sellable contact participates in a quotation or order process, **Sellable** is set to **True** to flag the contact as a sellable contact.</span></span> <span data-ttu-id="51d38-123">Een contactpersoon die een verkoopbaar contact is geworden, blijft een verkoopbaar contact.</span><span class="sxs-lookup"><span data-stu-id="51d38-123">A contact that has become a sellable contact remains a sellable contact.</span></span>

## <a name="templates"></a><span data-ttu-id="51d38-124">Sjablonen</span><span class="sxs-lookup"><span data-stu-id="51d38-124">Templates</span></span>

<span data-ttu-id="51d38-125">Klantgegevens omvatten alle informatie over de klant, zoals de klantgroep, adressen, contactgegevens, betalingsprofiel en factuurprofiel.</span><span class="sxs-lookup"><span data-stu-id="51d38-125">Customer data includes all information about the customer, such as the customer group, addresses, contact information, payment profile, invoice profile, and loyalty status.</span></span> <span data-ttu-id="51d38-126">Een verzameling entiteitstoewijzingen werkt samen tijdens interactie met klantgegevens, zoals in de volgende tabel wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="51d38-126">A collection of entity maps works together during customer data interaction, as shown in the following table.</span></span>

<span data-ttu-id="51d38-127">Finance and Operations-apps</span><span class="sxs-lookup"><span data-stu-id="51d38-127">Finance and Operations apps</span></span> | <span data-ttu-id="51d38-128">Andere Dynamics 365-apps</span><span class="sxs-lookup"><span data-stu-id="51d38-128">Other Dynamics 365 apps</span></span>         | <span data-ttu-id="51d38-129">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="51d38-129">Description</span></span>
----------------------------|---------------------------------|------------
<span data-ttu-id="51d38-130">CDS-contactpersonen V2</span><span class="sxs-lookup"><span data-stu-id="51d38-130">CDS Contacts V2</span></span>             | <span data-ttu-id="51d38-131">contacten</span><span class="sxs-lookup"><span data-stu-id="51d38-131">contacts</span></span>                        | <span data-ttu-id="51d38-132">Met deze sjabloon worden alle primaire, secundaire en tertiaire contactgegevens voor zowel klanten als leveranciers gesynchroniseerd.</span><span class="sxs-lookup"><span data-stu-id="51d38-132">This template synchronizes all primary, secondary, and tertiary contact information, for both customers and vendors.</span></span>
<span data-ttu-id="51d38-133">Klantengroepen</span><span class="sxs-lookup"><span data-stu-id="51d38-133">Customer groups</span></span>             | <span data-ttu-id="51d38-134">msdyn_customergroups</span><span class="sxs-lookup"><span data-stu-id="51d38-134">msdyn_customergroups</span></span>            | <span data-ttu-id="51d38-135">Met deze sjabloon worden klantengroepgegevens gesynchroniseerd.</span><span class="sxs-lookup"><span data-stu-id="51d38-135">This template synchronizes customer group information.</span></span>
<span data-ttu-id="51d38-136">Betalingsmethode van klant</span><span class="sxs-lookup"><span data-stu-id="51d38-136">Customer payment method</span></span>     | <span data-ttu-id="51d38-137">msdyn_customerpaymentmethods</span><span class="sxs-lookup"><span data-stu-id="51d38-137">msdyn_customerpaymentmethods</span></span>    | <span data-ttu-id="51d38-138">Met deze sjabloon worden gegevens over de betalingsmethoden van klanten gesynchroniseerd.</span><span class="sxs-lookup"><span data-stu-id="51d38-138">This template synchronizes customer payment method information.</span></span>
<span data-ttu-id="51d38-139">Klanten V3</span><span class="sxs-lookup"><span data-stu-id="51d38-139">Customers V3</span></span>                | <span data-ttu-id="51d38-140">rekeningen</span><span class="sxs-lookup"><span data-stu-id="51d38-140">accounts</span></span>                        | <span data-ttu-id="51d38-141">Met deze sjabloon worden klantmodelgegevens voor commerciële en organisatorische klanten gesynchroniseerd.</span><span class="sxs-lookup"><span data-stu-id="51d38-141">This template synchronizes customer master information for commercial and organizational customers.</span></span>
<span data-ttu-id="51d38-142">Klanten V3</span><span class="sxs-lookup"><span data-stu-id="51d38-142">Customers V3</span></span>                | <span data-ttu-id="51d38-143">contacten</span><span class="sxs-lookup"><span data-stu-id="51d38-143">contacts</span></span>                        | <span data-ttu-id="51d38-144">Met deze sjabloon worden klantmodelgegevens voor consumenten en eindgebruikers gesynchroniseerd.</span><span class="sxs-lookup"><span data-stu-id="51d38-144">This template synchronizes customer master data for consumers and end users.</span></span>
<span data-ttu-id="51d38-145">Loyaliteitskaart</span><span class="sxs-lookup"><span data-stu-id="51d38-145">Loyalty card</span></span>                | <span data-ttu-id="51d38-146">msdyn_loyaltycards</span><span class="sxs-lookup"><span data-stu-id="51d38-146">msdyn_loyaltycards</span></span>              | <span data-ttu-id="51d38-147">Met deze sjabloon worden loyaliteitskaartgegevens voor klanten gesynchroniseerd.</span><span class="sxs-lookup"><span data-stu-id="51d38-147">This template synchronizes customer loyalty card information.</span></span>
<span data-ttu-id="51d38-148">Voor- en achtervoegsel naam</span><span class="sxs-lookup"><span data-stu-id="51d38-148">Name affixes</span></span>                | <span data-ttu-id="51d38-149">msdyn_nameaffixes</span><span class="sxs-lookup"><span data-stu-id="51d38-149">msdyn_nameaffixes</span></span>               | <span data-ttu-id="51d38-150">Met deze sjabloon worden referentiegegevens over voor- en achtervoegsels van namen voor zowel klanten als leveranciers gesynchroniseerd.</span><span class="sxs-lookup"><span data-stu-id="51d38-150">This template synchronizes name affixes reference data, for both customers and vendors.</span></span>
<span data-ttu-id="51d38-151">Betalingsdagregels CDS V2</span><span class="sxs-lookup"><span data-stu-id="51d38-151">Payment day lines CDS V2</span></span>    | <span data-ttu-id="51d38-152">msdyn_paymentdaylines</span><span class="sxs-lookup"><span data-stu-id="51d38-152">msdyn_paymentdaylines</span></span>           | <span data-ttu-id="51d38-153">Met deze sjabloon worden referentiegegevens over betalingsdagregels voor zowel klanten als leveranciers gesynchroniseerd.</span><span class="sxs-lookup"><span data-stu-id="51d38-153">This template synchronizes payment day lines reference data, for both customers and vendors.</span></span>
<span data-ttu-id="51d38-154">Betalingsdagen CDS</span><span class="sxs-lookup"><span data-stu-id="51d38-154">Payment days CDS</span></span>            | <span data-ttu-id="51d38-155">msdyn_paymentdays</span><span class="sxs-lookup"><span data-stu-id="51d38-155">msdyn_paymentdays</span></span>               | <span data-ttu-id="51d38-156">Met deze sjabloon worden referentiegegevens over betalingsdagen voor zowel klanten als leveranciers gesynchroniseerd.</span><span class="sxs-lookup"><span data-stu-id="51d38-156">This template synchronizes payment days reference data, for both customers and vendors.</span></span>
<span data-ttu-id="51d38-157">Regels van betalingsschema</span><span class="sxs-lookup"><span data-stu-id="51d38-157">Payment schedule lines</span></span>      | <span data-ttu-id="51d38-158">msdyn_paymentschedulelines</span><span class="sxs-lookup"><span data-stu-id="51d38-158">msdyn_paymentschedulelines</span></span>      | <span data-ttu-id="51d38-159">Met deze sjabloon worden referentiegegevens over betalingsschemaregels voor zowel klanten als leveranciers gesynchroniseerd.</span><span class="sxs-lookup"><span data-stu-id="51d38-159">Syncs payment schedule lines reference data, for both customers and vendors.</span></span>
<span data-ttu-id="51d38-160">Betalingsplanning</span><span class="sxs-lookup"><span data-stu-id="51d38-160">Payment schedule</span></span>            | <span data-ttu-id="51d38-161">msdyn_paymentschedules</span><span class="sxs-lookup"><span data-stu-id="51d38-161">msdyn_paymentschedules</span></span>          | <span data-ttu-id="51d38-162">Met deze sjabloon worden referentiegegevens over betalingsschema's voor zowel klanten als leveranciers gesynchroniseerd.</span><span class="sxs-lookup"><span data-stu-id="51d38-162">This template synchronizes payment schedule reference data, for both customers and vendors.</span></span>
<span data-ttu-id="51d38-163">Betalingstermijnen</span><span class="sxs-lookup"><span data-stu-id="51d38-163">Terms of payment</span></span>            | <span data-ttu-id="51d38-164">msdyn_paymentterms</span><span class="sxs-lookup"><span data-stu-id="51d38-164">msdyn_paymentterms</span></span>              | <span data-ttu-id="51d38-165">Met deze sjabloon worden referentiegegevens over betalingsvoorwaarden (voorwaarden voor betaling) voor zowel klanten als leveranciers gesynchroniseerd.</span><span class="sxs-lookup"><span data-stu-id="51d38-165">This template synchronizes payment terms (terms of payment) reference data, for both customers and vendors.</span></span>

[!include [banner](../../includes/dual-write-symbols.md)]

[!include [mapping contacts contacts](includes/CDSContactsV2-contacts.md)]

[!include [mapping customer group](includes/CustCustomerGroup-msdyn-customergroups.md)]

[!include [mapping customer payment method](includes/CustomerPaymentMethod-msdyn-customerpaymentmethods.md)]

[!include [mapping customer accounts](includes/CustomersV3-accounts.md)]

[!include [mapping customer contacts](includes/CustomersV3-contacts.md)]

[!include [mapping loyalty card](includes/LoyaltyCard-msdyn-loyaltycards.md)]

[!include [mapping name affixes](includes/NameAffixes-msdyn-nameaffixes.md)]

[!include [mapping payment day lines](includes/PaymentDayLinesCdsV2-msdyn-paymentdaylines.md)]

[!include [mapping payment days](includes/PaymentDaysCds-msdyn-paymentdays.md)]

[!include [mapping payment schedule lines](includes/PaymentScheduleLines-msdyn-paymentschedulelines.md)]

[!include [mapping payment schedules](includes/PaymentSchedules-msdyn-paymentschedules.md)]

[!include [mapping terms of payment](includes/TermsofPayment-msdyn-paymentterms.md)]