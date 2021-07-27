---
title: Model voor geïntegreerde leveranciers
description: In dit onderwerp wordt de integratie van leveranciersgegevens tussen Finance and Operations en Dataverse beschreven.
author: RamaKrishnamoorthy
ms.date: 07/15/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 7e6ac62b2b289ef818a083b9ae4d1d74946ae3fc
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 07/06/2021
ms.locfileid: "6346491"
---
# <a name="integrated-vendor-master"></a>Model voor geïntegreerde leveranciers

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



De term *leverancier* verwijst naar een leveranciersorganisatie die of eenmansbedrijf dat goederen of diensten levert aan een bedrijf. Hoewel *leverancier* een bestaand concept is in Microsoft Dynamics 365 Supply Chain Management, bestaat het concept leverancier niet in modelgestuurde apps in Dynamics 365. U kunt de tabel **Rekening/contactpersoon** echter overbelasten om leveranciersgegevens op te slaan. Het geïntegreerde leveranciersmodel introduceert een expliciet leveranciersconcept in modelgestuurde apps in Dynamics 365. U kunt het nieuwe leveranciersontwerp gebruiken of leveranciersgegevens opslaan in de tabel **Rekening/contactpersoon**. Twee keer wegschrijven ondersteunt beide methoden.

In beide methoden worden de leveranciersgegevens geïntegreerd tussen Dynamics 365 Supply Chain Management-, Dynamics 365 Sales-, Dynamics 365 Field Service- en Power Apps-portals. In Supply Chain Management zijn de gegevens beschikbaar voor werkstromen zoals opdrachten tot inkoop en inkooporders.

## <a name="vendor-data-flow"></a>Leveranciersgegevensstroom

Als u leveranciersgegevens niet wilt opslaan in de tabel **Rekening/contactpersoon** in Dataverse, kunt u het nieuwe leveranciersontwerp gebruiken.

![Leveranciersgegevensstroom.](media/dual-write-vendor-data-flow.png)

Als u leveranciersgegevens wilt blijven opslaan in de tabel **Rekening/contactpersoon**, kunt u het uitgebreide leveranciersontwerp gebruiken. Als u het uitgebreide leveranciersontwerp wilt gebruiken, moet u de leverancierswerkstromen configureren in het oplossingspakket Twee keer wegschrijven. Zie [Schakelen tussen leverancierontwerpen](vendor-switch.md) voor meer informatie.

![Uitgebreide leveranciersgegevensstroom.](media/dual-write-vendor-detail.jpg)

> [!TIP]
> Als u Power Apps-portals gebruikt voor selfservice leveranciers, kunnen de leveranciersgegevens rechtstreeks naar Finance and Operations-apps stromen.

## <a name="templates"></a>Sjablonen

Leveranciersgegevens omvatten alle informatie over de leverancier, zoals de leveranciersgroep, adressen, contactgegevens, betalingsprofiel en factuurprofiel. Een verzameling tabeltoewijzingen werkt samen tijdens interactie met leveranciersgegevens, zoals in de volgende tabel wordt weergegeven.

Finance and Operations-apps | Andere Dynamics 365-apps     | Beschrijving
----------------------------|-----------------------------|------------
Leverancier V2                   | Rekening                     | Bedrijven die de tabel Rekening gebruiken om leveranciergegevens op te slaan, kunnen deze op dezelfde manier blijven gebruiken. Door integratie met Finance and Operations-apps kunnen ze ook de expliciete leveranciersfunctionaliteit gaan gebruiken die beschikbaar komt.
Leverancier V2                   | Msdyn\_vendors              | Door integratie met Finance and Operations-apps kunnen bedrijven die een aangepaste oplossing voor leveranciers gebruiken, profiteren van het kant-en-klare leveranciersconcept dat in Dataverse wordt geïntroduceerd. 
Leveranciersgroepen               | msdyn\_vendorgroups         | Met deze sjabloon worden leveranciersgroepgegevens gesynchroniseerd.
Leveranciersbetalingsmethode       | msdyn\_vendorpaymentmethods | Met deze sjabloon worden gegevens over de betalingsmethoden van leveranciers gesynchroniseerd.
CDS-contactpersonen V2             | contacten                    | Met de sjabloon [contactpersonen](customer-mapping.md#cds-contacts-v2-to-contacts) worden alle primaire, secundaire en tertiaire contactgegevens voor zowel klanten als leveranciers gesynchroniseerd.
Regels van betalingsschema      | msdyn\_paymentschedulelines | Met de sjabloon voor [betalingsschemaregels](customer-mapping.md#payment-schedule-lines-to-msdyn_paymentschedulelines) worden referentiegegevens voor klanten en leveranciers gesynchroniseerd.
Betalingsplanning            | msdyn\_paymentschedules     | Met de sjabloon voor [betalingsschema's](customer-mapping.md#payment-schedule-to-msdyn_paymentschedules) worden referentiegegevens over betalingsschema's voor zowel klanten als leveranciers gesynchroniseerd.
Betalingsdagregels CDS V2    | msdyn\_paymentdaylines      | Met de sjabloon voor [betalingsdagregels](customer-mapping.md#payment-day-lines-cds-v2-to-msdyn_paymentdaylines) worden referentiegegevens over betalingsdagregels voor klanten en leveranciers gesynchroniseerd.
Betalingsdagen CDS            | msdyn\_paymentdays          | Met de sjabloon voor [betalingsdagen](customer-mapping.md#payment-days-cds-to-msdyn_paymentdays) worden referentiegegevens over betalingsdagen voor zowel klanten als leveranciers gesynchroniseerd.
Betalingstermijn            | msdyn\_paymentterms         | Met de sjabloon voor [betalingsvoorwaarden](customer-mapping.md#terms-of-payment-to-msdyn_paymentterms) worden referentiegegevens over betalingsvoorwaarden voor zowel klanten als leveranciers gesynchroniseerd.
Voor- en achtervoegsel naam                | msdyn\_nameaffixes          | Met de sjabloon voor [voor- en achtervoegsels van namen](customer-mapping.md#name-affixes-to-msdyn_nameaffixes) worden referentiegegevens over voor- en achtervoegsels van namen voor zowel klanten als leveranciers gesynchroniseerd.

[!include [symbols](../../includes/dual-write-symbols.md)]

[!include [Vendors](includes/VendorsV2-msdyn-vendors.md)]

[!include [Vendor groups](includes/VendVendorGroup-msdyn-vendorgroups.md)]

[!include [Vendor payment methods](includes/VendorPaymentMethod-msdyn-vendorpaymentmethods.md)]


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]