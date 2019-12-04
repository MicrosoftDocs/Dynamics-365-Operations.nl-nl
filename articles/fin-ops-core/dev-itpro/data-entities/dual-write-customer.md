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
ms.openlocfilehash: 09d985e5c6816ec0c718aaf418f4e85fb828f1c6
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/06/2019
ms.locfileid: "2769678"
---
# <a name="integrated-customer-master"></a>Geïntegreerd klantmodel

[!include [banner](../includes/banner.md)]

Het is gebruikelijk dat klantrecords in meer dan één toepassing worden beheerst. Verkoopactiviteiten kunnen bijvoorbeeld commerciële klantrecords inbrengen via een Sales-toepassing en e-Commerce- of detailhandelsverkopen kunnen klantrecords inbrengen via een Finance and Operations-toepassing. Ongeacht waar de klantgegevens vandaan komen, worden ze achter de schermen geïntegreerd over toepassingsgrenzen en infrastructuurverschillen heen. Geïntegreerd klantbeheer helpt bij het afhandelen van scenario's met meervoudig beheer en biedt een uitgebreid overzicht van de klant naar de Dynamics 365 Application Suite.

## <a name="customer-data-flow"></a>Klantgegevensstroom

*Klant* is een goed gedefinieerd concept in toepassingen. Daarom bestaat de integratie van klantgegevens alleen uit het harmoniseren van het klantconcept tussen de twee toepassingen. In de volgende afbeelding wordt de klantgegevensstroom weergegeven.

![Klantgegevensstroom](media/dual-write-customer-data-flow.png)

Klanten kunnen globaal worden ingedeeld in twee typen: commerciële/organisatorische klanten en consumenten/eindgebruikers. Deze twee typen klanten worden in Finance and Operations en Common Data Service op een andere manier opgeslagen en verwerkt.

In Finance and Operations worden zowel commerciële/organisatorische klanten als consumenten/eindgebruikers in één tabel met de naam **CustTable** (CustomerCustomerV3Entity) beheerd en worden ze geclassificeerd op basis van het kenmerk **Type**. (Als **Type** is ingesteld op **Organisatie**, is de klant een commerciële/organisatorische klant en als **Type** is ingesteld op **Persoon**, is de klant een consument/eindgebruiker.) De primaire contactpersoonsgegevens worden afgehandeld via de entiteit SMMContactPersonEntity.

In Common Data Service worden commerciële/organisatorische klanten beheerd in het entiteit Account en worden ze geïdentificeerd als het kenmerk **RelationshipType** kenmerk is ingesteld op **Klant**. Zowel consumenten/eindgebruikers als de contactpersoon worden vertegenwoordigd door entiteit Contactpersoon. Om een duidelijke scheiding te maken tussen een consument/eindgebruiker en een contactpersoon, heeft de entiteit **Contactpersoon** een Booleaanse vlag met de naam **Verkoopbaar**. Wanneer **Verkoopbaar** de waarde **Waar** heeft, is de contactpersoon een consument/eindgebruiker en kunnen er voor die contactpersoon offertes en orders worden gemaakt. Als **Verkoopbaar** is ingesteld op **Onwaar**, is de contactpersoon slechts een primaire contactpersoon van een klant.

Wanneer een niet-verkoopbare contactpersoon deelneemt aan een offerte- of orderproces, is **Verkoopbaar** ingesteld op **Waar** om de contactpersoon te markeren als een verkoopbaar contact. Een contactpersoon die een verkoopbaar contact is geworden, blijft een verkoopbaar contact.

## <a name="templates"></a>Sjablonen

Klantgegevens omvatten alle informatie over de klant, zoals de klantgroep, adressen, contactgegevens, betalingsprofiel en factuurprofiel. Een verzameling entiteitstoewijzingen werkt samen tijdens interactie met klantgegevens, zoals in de volgende tabel wordt weergegeven.

Finance and Operations-apps | Andere Dynamics 365-apps         | Beschrijving
----------------------------|---------------------------------|------------
CDS-contactpersonen V2             | contacten                        | Met deze sjabloon worden alle primaire, secundaire en tertiaire contactgegevens voor zowel klanten als leveranciers gesynchroniseerd.
Klantengroepen             | msdyn_customergroups            | Met deze sjabloon worden klantengroepgegevens gesynchroniseerd.
Betalingsmethode van klant     | msdyn_customerpaymentmethods    | Met deze sjabloon worden gegevens over de betalingsmethoden van klanten gesynchroniseerd.
Klanten V3                | rekeningen                        | Met deze sjabloon worden klantmodelgegevens voor commerciële en organisatorische klanten gesynchroniseerd.
Klanten V3                | contacten                        | Met deze sjabloon worden klantmodelgegevens voor consumenten en eindgebruikers gesynchroniseerd.
Loyaliteitskaart                | msdyn_loyaltycards              | Met deze sjabloon worden loyaliteitskaartgegevens voor klanten gesynchroniseerd.
Voor- en achtervoegsel naam                | msdyn_nameaffixes               | Met deze sjabloon worden referentiegegevens over voor- en achtervoegsels van namen voor zowel klanten als leveranciers gesynchroniseerd.
Betalingsdagregels CDS V2    | msdyn_paymentdaylines           | Met deze sjabloon worden referentiegegevens over betalingsdagregels voor zowel klanten als leveranciers gesynchroniseerd.
Betalingsdagen CDS            | msdyn_paymentdays               | Met deze sjabloon worden referentiegegevens over betalingsdagen voor zowel klanten als leveranciers gesynchroniseerd.
Regels van betalingsschema      | msdyn_paymentschedulelines      | Met deze sjabloon worden referentiegegevens over betalingsschemaregels voor zowel klanten als leveranciers gesynchroniseerd.
Betalingsplanning            | msdyn_paymentschedules          | Met deze sjabloon worden referentiegegevens over betalingsschema's voor zowel klanten als leveranciers gesynchroniseerd.
Betalingstermijnen            | msdyn_paymentterms              | Met deze sjabloon worden referentiegegevens over betalingsvoorwaarden (voorwaarden voor betaling) voor zowel klanten als leveranciers gesynchroniseerd.

[!include [banner](../includes/dual-write-symbols.md)]

[!include [mapping contacts contacts](dual-write/CDSContactsV2-contacts.md)]

[!include [mapping customer group](dual-write/CustCustomerGroup-msdyn-customergroups.md)]

[!include [mapping customer payment method](dual-write/CustomerPaymentMethod-msdyn-customerpaymentmethods.md)]

[!include [mapping customer accounts](dual-write/CustomersV3-accounts.md)]

[!include [mapping customer contacts](dual-write/CustomersV3-contacts.md)]

[!include [mapping loyalty card](dual-write/LoyaltyCard-msdyn-loyaltycards.md)]

[!include [mapping name affixes](dual-write/NameAffixes-msdyn-nameaffixes.md)]

[!include [mapping payment day lines](dual-write/PaymentDayLinesCdsV2-msdyn-paymentdaylines.md)]

[!include [mapping payment days](dual-write/PaymentDaysCds-msdyn-paymentdays.md)]

[!include [mapping payment schedule lines](dual-write/PaymentScheduleLines-msdyn-paymentschedulelines.md)]

[!include [mapping payment schedules](dual-write/PaymentSchedules-msdyn-paymentschedules.md)]

[!include [mapping terms of payment](dual-write/TermsofPayment-msdyn-paymentterms.md)]
