---
title: Geïntegreerd leveranciersmodel
description: In dit onderwerp wordt de integratie van leveranciersgegevens tussen apps voor financiële en bedrijfsactiviteiten en Dataverse beschreven.
author: RamaKrishnamoorthy
ms.date: 07/15/2019
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 7794f33aed7364b76a7d5ffd08a068342887e468
ms.sourcegitcommit: 4be1473b0a4ddfc0ba82c07591f391e89538f1c3
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/31/2022
ms.locfileid: "8063157"
---
# <a name="integrated-vendor-master"></a>Model voor geïntegreerde leveranciers

[!include [banner](../../includes/banner.md)]



De term *leverancier* verwijst naar een leveranciersorganisatie die of eenmansbedrijf dat goederen of diensten levert aan een bedrijf. Hoewel *leverancier* een bestaand concept is in Microsoft Dynamics 365 Supply Chain Management, bestaat het concept leverancier niet in apps voor klantbetrokkenheid. U kunt de tabel **Rekening/contactpersoon** echter overbelasten om leveranciersgegevens op te slaan. Het geïntegreerde leveranciersmodel introduceert een expliciet leveranciersconcept in apps voor klantbetrokkenheid. U kunt het nieuwe leveranciersontwerp gebruiken of leveranciersgegevens opslaan in de tabel **Rekening/contactpersoon**. Twee keer wegschrijven ondersteunt beide methoden.

In beide methoden worden de leveranciersgegevens geïntegreerd tussen Dynamics 365 Supply Chain Management-, Dynamics 365 Sales-, Dynamics 365 Field Service- en Power Apps-portals. In Supply Chain Management zijn de gegevens beschikbaar voor werkstromen zoals opdrachten tot inkoop en inkooporders.

## <a name="vendor-data-flow"></a>Leveranciersgegevensstroom

Als u leveranciersgegevens niet wilt opslaan in de tabel **Rekening/contactpersoon** in Dataverse, kunt u het nieuwe leveranciersontwerp gebruiken.

![Leveranciersgegevensstroom.](media/dual-write-vendor-data-flow.png)

Als u leveranciersgegevens wilt blijven opslaan in de tabel **Rekening/contactpersoon**, kunt u het uitgebreide leveranciersontwerp gebruiken. Als u het uitgebreide leveranciersontwerp wilt gebruiken, moet u de leverancierswerkstromen configureren in het oplossingspakket Twee keer wegschrijven. Zie [Schakelen tussen leverancierontwerpen](vendor-switch.md) voor meer informatie.

![Uitgebreide leveranciersgegevensstroom.](media/dual-write-vendor-detail.jpg)

> [!TIP]
> Als u Power Apps-portals gebruikt voor selfservice leveranciers, kunnen de leveranciersgegevens rechtstreeks naar apps voor financiële en bedrijfsactiviteiten stromen.

## <a name="templates"></a>Sjablonen

Leveranciersgegevens omvatten alle informatie over de leverancier, zoals de leveranciersgroep, adressen, contactgegevens, betalingsprofiel en factuurprofiel. Een verzameling tabeltoewijzingen werkt samen tijdens interactie met leveranciersgegevens, zoals in de volgende tabel wordt weergegeven.

Apps voor financiële en bedrijfsactiviteiten | Customer Engagement-apps     | Beschrijving
----------------------------|-----------------------------|------------
[CDS-contactpersonen V2](mapping-reference.md#115) | contacten | Met deze sjabloon worden alle primaire, secundaire en tertiaire contactgegevens voor zowel klanten als leveranciers gesynchroniseerd.
[Voor- en achtervoegsel naam](mapping-reference.md#155) | msdyn_nameaffixes | Met deze sjabloon worden referentiegegevens over voor- en achtervoegsels van namen voor zowel klanten als leveranciers gesynchroniseerd.
[Betalingsdagregels CDS V2](mapping-reference.md#157) | msdyn_paymentdaylines | Met deze sjabloon worden referentiegegevens over betalingsdagregels voor zowel klanten als leveranciers gesynchroniseerd.
[Betalingsdagen CDS](mapping-reference.md#158) | msdyn_paymentdays | Met deze sjabloon worden referentiegegevens over betalingsdagen voor zowel klanten als leveranciers gesynchroniseerd.
[Regels van betalingsschema](mapping-reference.md#159) | msdyn_paymentschedulelines | Met deze sjabloon worden referentiegegevens over betalingsschemaregels voor zowel klanten als leveranciers gesynchroniseerd.
[Betalingsplanning](mapping-reference.md#160) | msdyn_paymentschedules | Met deze sjabloon worden referentiegegevens over betalingsschema's voor zowel klanten als leveranciers gesynchroniseerd.
[Betalingstermijnen](mapping-reference.md#161) | msdyn_paymentterms | Met deze sjabloon worden referentiegegevens over betalingsvoorwaarden (voorwaarden voor betaling) voor zowel klanten als leveranciers gesynchroniseerd.
[Leveranciers V2](mapping-reference.md#202) | msdyn_vendors | Door integratie met apps voor financiële en bedrijfsactiviteiten kunnen bedrijven die een aangepaste oplossing voor leveranciers gebruiken, profiteren van het kant-en-klare leveranciersconcept dat in Dataverse wordt geïntroduceerd.
[Leveranciersgroepen](mapping-reference.md#200) | msdyn_vendorgroups | Met deze sjabloon worden leveranciersgroepgegevens gesynchroniseerd.
[Leveranciersbetalingsmethode](mapping-reference.md#201) | msdyn_vendorpaymentmethods | Met deze sjabloon worden gegevens over de betalingsmethoden van leveranciers gesynchroniseerd.

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
