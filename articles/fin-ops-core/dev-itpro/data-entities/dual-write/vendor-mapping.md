---
title: Model voor geïntegreerde leveranciers
description: In dit onderwerp wordt de integratie van leveranciersgegevens tussen Finance and Operations en Dataverse beschreven.
author: RamaKrishnamoorthy
ms.date: 07/15/2019
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 36cfed92535c1df3ba55fd56bc8aa2f9eccf3003
ms.sourcegitcommit: f65bde9ab0bf4c12a3250e7c9b2abb1555cd7931
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 07/13/2021
ms.locfileid: "6542434"
---
# <a name="integrated-vendor-master"></a>Model voor geïntegreerde leveranciers

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

De term *leverancier* verwijst naar een leveranciersorganisatie die of eenmansbedrijf dat goederen of diensten levert aan een bedrijf. Hoewel *leverancier* een bestaand concept is in Microsoft Dynamics 365 Supply Chain Management, bestaat het concept leverancier niet in apps voor klantbetrokkenheid. U kunt de tabel **Rekening/contactpersoon** echter overbelasten om leveranciersgegevens op te slaan. Het geïntegreerde leveranciersmodel introduceert een expliciet leveranciersconcept in apps voor klantbetrokkenheid. U kunt het nieuwe leveranciersontwerp gebruiken of leveranciersgegevens opslaan in de tabel **Rekening/contactpersoon**. Twee keer wegschrijven ondersteunt beide methoden.

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

Finance and Operations-apps | Customer Engagement-apps     | Beschrijving
----------------------------|-----------------------------|------------
[CDS-contactpersonen V2](mapping-reference.md#115) | contacten | Met deze sjabloon worden alle primaire, secundaire en tertiaire contactgegevens voor zowel klanten als leveranciers gesynchroniseerd.
[Voor- en achtervoegsel naam](mapping-reference.md#155) | msdyn_nameaffixes | Met deze sjabloon worden referentiegegevens over voor- en achtervoegsels van namen voor zowel klanten als leveranciers gesynchroniseerd.
[Betalingsdagregels CDS V2](mapping-reference.md#157) | msdyn_paymentdaylines | Met deze sjabloon worden referentiegegevens over betalingsdagregels voor zowel klanten als leveranciers gesynchroniseerd.
[Betalingsdagen CDS](mapping-reference.md#158) | msdyn_paymentdays | Met deze sjabloon worden referentiegegevens over betalingsdagen voor zowel klanten als leveranciers gesynchroniseerd.
[Regels van betalingsschema](mapping-reference.md#159) | msdyn_paymentschedulelines | Met deze sjabloon worden referentiegegevens over betalingsschemaregels voor zowel klanten als leveranciers gesynchroniseerd.
[Betalingsplanning](mapping-reference.md#160) | msdyn_paymentschedules | Met deze sjabloon worden referentiegegevens over betalingsschema's voor zowel klanten als leveranciers gesynchroniseerd.
[Betalingstermijnen](mapping-reference.md#161) | msdyn_paymentterms | Met deze sjabloon worden referentiegegevens over betalingsvoorwaarden (voorwaarden voor betaling) voor zowel klanten als leveranciers gesynchroniseerd.
[Leveranciers V2](mapping-reference.md#202) | msdyn_vendors | Door integratie met Finance and Operations-apps kunnen bedrijven die een aangepaste oplossing voor leveranciers gebruiken, profiteren van het kant-en-klare leveranciersconcept dat in Dataverse wordt geïntroduceerd.
[Leveranciersgroepen](mapping-reference.md#200) | msdyn_vendorgroups | Met deze sjabloon worden leveranciersgroepgegevens gesynchroniseerd.
[Leveranciersbetalingsmethode](mapping-reference.md#201) | msdyn_vendorpaymentmethods | Met deze sjabloon worden gegevens over de betalingsmethoden van leveranciers gesynchroniseerd.

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
