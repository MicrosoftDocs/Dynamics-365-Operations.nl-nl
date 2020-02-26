---
title: Model voor geïntegreerde leveranciers
description: In dit onderwerp wordt de integratie van leveranciersgegevens tussen Finance and Operations en Common Data Service beschreven.
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
ms.openlocfilehash: 2442a6869daac22a435c1a7504b93ea4b5c14747
ms.sourcegitcommit: 54baab2a04e5c534fc2d1fd67b67e23a152d4e57
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/04/2020
ms.locfileid: "3019714"
---
# <a name="integrated-vendor-master"></a>Model voor geïntegreerde leveranciers

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]

De term *leverancier* verwijst naar een leveranciersorganisatie of één eigenaar die deel uitmaakt van het toeleveringsproces, en die goederen levert voor het bedrijf. Hoewel *leverancier* een bestaand concept is in Finance and Operations-apps, bestaat het concept leverancier niet in andere Dynamics 365-apps. In plaats daarvan wordt de entiteit Account door een aantal bedrijven overbelast door er zowel klant- als leveranciersgegevens in op te slaan. Andere bedrijven gebruiken een aangepast leveranciersconcept. Common Data Service-integratie ondersteunt beide ontwerpen. Daarom kunt u, afhankelijk van uw bedrijfsscenario, een van de ontwerpen inschakelen.

Door integratie van leveranciersgegevens tussen Finance and Operations-apps en Dynamics 365-apps kunt u de gegevens meervoudig beheren. Ongeacht waar de leveranciersgegevens vandaan komen, worden ze achter de schermen geïntegreerd over toepassingsgrenzen en infrastructuurverschillen heen. 

### <a name="vendor-data-flow"></a>Leveranciersgegevensstroom

Als u andere Dynamics 365-apps wilt gebruiken voor leveranciersbeheer en u leveranciergegevens wilt isoleren van klantgegevens, kunt u het nieuwe leveranciersontwerp gebruiken.

![Leveranciersgegevensstroom](media/dual-write-vendor-data-flow.png)

Als u andere Dynamics 365-apps wilt gebruiken voor leveranciersbeheer en u de accountentiteit wilt blijven gebruiken voor de opslag van leveranciergegevens, kunt u het nieuwe uitgebreide leveranciersontwerp gebruiken. In dit ontwerp worden uitgebreide leveranciersgegevens, zoals leveranciersgroep en het boekingsprofiel van de leverancier, opgeslagen als onderdeel van de leveranciersgegevens.

![Uitgebreide leveranciersgegevensstroom](media/dual-write-vendor-detail.jpg)

Contactgegevens van de leverancier lijken op contactgegevens van de klant. Achter de schermen worden de gegevens van de contactpersoon opgeslagen en opgehaald uit dezelfde entiteiten.

## <a name="templates"></a>Sjablonen

Leveranciersgegevens omvatten alle informatie over de leverancier, zoals de leveranciersgroep, adressen, contactgegevens, betalingsprofiel en factuurprofiel. Een verzameling entiteitstoewijzingen werkt samen tijdens interactie met leveranciersgegevens, zoals in de volgende tabel wordt weergegeven.

Finance and Operations-apps | Andere Dynamics 365-apps         | Beschrijving
----------------------------|---------------------------------|------------
Leverancier V2               | Rekening | Bedrijven die de accountentiteit gebruiken om leveranciergegevens op te slaan, kunnen deze op dezelfde manier blijven gebruiken. Door integratie met Finance and Operations-apps kunnen ze ook de expliciete leveranciersfunctionaliteit gaan gebruiken die beschikbaar komt.
Leverancier V2               | Msdyn\_vendors | Door integratie met Finance and Operations-apps kunnen bedrijven die een aangepaste oplossing voor leveranciers gebruiken, profiteren van het kant-en-klare leveranciersconcept dat in Common Data Service wordt geïntroduceerd. 
Leveranciersgroepen | msdyn_vendorgroups | Met deze sjabloon worden leveranciersgroepgegevens gesynchroniseerd.
Leveranciersbetalingsmethode | msdyn_vendorpaymentmethods | Met deze sjabloon worden gegevens over de betalingsmethoden van leveranciers gesynchroniseerd.
CDS-contactpersonen V2             | contacten                        | Met de sjabloon [contactpersonen](customer-mapping.md#cds-contacts-v2-to-contacts) worden alle primaire, secundaire en tertiaire contactgegevens voor zowel klanten als leveranciers gesynchroniseerd.
Regels van betalingsschema      | msdyn_paymentschedulelines      | Met de sjabloon voor [betalingsschemaregels](customer-mapping.md#payment-schedule-lines-to-msdyn_paymentschedulelines) worden referentiegegevens voor klanten en leveranciers gesynchroniseerd.
Betalingsplanning            | msdyn_paymentschedules          | Met de sjabloon voor [betalingsschema's](customer-mapping.md#payment-schedule-to-msdyn_paymentschedules) worden referentiegegevens over betalingsschema's voor zowel klanten als leveranciers gesynchroniseerd.
Betalingsdagregels CDS V2    | msdyn_paymentdaylines           | Met de sjabloon voor [betalingsdagregels](customer-mapping.md#payment-day-lines-cds-v2-to-msdyn_paymentdaylines) worden referentiegegevens over betalingsdagregels voor klanten en leveranciers gesynchroniseerd.
Betalingsdagen CDS            | msdyn_paymentdays               | Met de sjabloon voor [betalingsdagen](customer-mapping.md#payment-days-cds-to-msdyn_paymentdays) worden referentiegegevens over betalingsdagen voor zowel klanten als leveranciers gesynchroniseerd.
Betalingstermijnen            | msdyn_paymentterms              | Met de sjabloon voor [betalingsvoorwaarden](customer-mapping.md#terms-of-payment-to-msdyn_paymentterms) worden referentiegegevens over betalingsvoorwaarden voor zowel klanten als leveranciers gesynchroniseerd.
Voor- en achtervoegsel naam                | msdyn_nameaffixes               | Met de sjabloon voor [voor- en achtervoegsels van namen](customer-mapping.md#name-affixes-to-msdyn_nameaffixes) worden referentiegegevens over voor- en achtervoegsels van namen voor zowel klanten als leveranciers gesynchroniseerd.

[!include [symbols](../../includes/dual-write-symbols.md)]

[!include [Vendors](includes/VendorsV2-msdyn-vendors.md)]

[!include [Vendor groups](includes/VendVendorGroup-msdyn-vendorgroups.md)]

[!include [Vendor payment methods](includes/VendorPaymentMethod-msdyn-vendorpaymentmethods.md)]
