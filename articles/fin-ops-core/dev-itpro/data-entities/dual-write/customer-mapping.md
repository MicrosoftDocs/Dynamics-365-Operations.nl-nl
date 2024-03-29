---
title: Model voor geïntegreerde klanten
description: In dit artikel wordt de integratie van klantgegevens tussen Finance + Operations en Dataverse beschreven.
author: RamaKrishnamoorthy
ms.date: 07/15/2019
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: ea142aff7c8f4b442d7224325e44359129efe8a8
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/12/2022
ms.locfileid: "9289675"
---
# <a name="integrated-customer-master"></a>Model voor geïntegreerde klanten

[!include [banner](../../includes/banner.md)]



Klantgegevens kunnen in meerdere Dynamics 365-toepassingen worden beheerd. Een klantrij kan bijvoorbeeld afkomstig zijn van een verkoopactiviteit in Dynamics 365 Sales (een klantbetrokkenheidsapp) of een rij die afkomstig is van een detailhandelactiviteit in Dynamics 365 Commerce (een app voor financiële en bedrijfsactiviteiten). Ongeacht waar de klantgegevens vandaan komen, ze worden achter de schermen geïntegreerd. Met het geïntegreerde klantmodel hebt u de flexibiliteit om de hoofdgegevens van klanten te beheren in elke Dynamics 365-toepassing met een uitgebreid overzicht van de klant in de Dynamics 365-toepassingsreeks.

## <a name="customer-data-flow"></a>Klantgegevensstroom

*Klant* is een goed gedefinieerd concept in toepassingen. Daarom bestaat de integratie van klantgegevens alleen uit het harmoniseren van het klantconcept tussen de twee toepassingen. In de volgende afbeelding wordt de klantgegevensstroom weergegeven.

![Klantgegevensstroom.](media/dual-write-customer-data-flow.png)

Klanten kunnen globaal worden ingedeeld in twee typen: commerciële/organisatorische klanten en consumenten/eindgebruikers. Deze twee typen klanten worden in Finance + Operations en Dataverse op een andere manier opgeslagen en verwerkt.

In Finance + Operations worden zowel commerciële/organisatorische klanten als consumenten/eindgebruikers in één tabel met de naam **CustTable** (CustCustomerV3Entity) beheerd en worden ze geclassificeerd op basis van het kenmerk **Type**. (Als **Type** is ingesteld op **Organisatie**, is de klant een commerciële/organisatorische klant en als **Type** is ingesteld op **Persoon**, is de klant een consument/eindgebruiker.) De primaire contactpersoonsgegevens worden afgehandeld via de tabel SMMContactPersonEntity.

In Dataverse worden commerciële/organisatorische klanten beheerd in de tabel Account en worden ze geïdentificeerd als klant als het kenmerk **RelationshipType** is ingesteld op **Klant**. Zowel consumenten/eindgebruikers als de contactpersoon worden vertegenwoordigd door de tabel Contactpersoon. Om een duidelijke scheiding te maken tussen een consument/eindgebruiker en een contactpersoon, heeft de tabel **Contactpersoon** een Booleaanse vlag met de naam **Verkoopbaar**. Wanneer **Verkoopbaar** de waarde **Waar** heeft, is de contactpersoon een consument/eindgebruiker en kunnen er voor die contactpersoon offertes en orders worden gemaakt. Als **Verkoopbaar** is ingesteld op **Onwaar**, is de contactpersoon slechts een primaire contactpersoon van een klant.

Wanneer een niet-verkoopbare contactpersoon deelneemt aan een offerte- of orderproces, is **Verkoopbaar** ingesteld op **Waar** om de contactpersoon te markeren als een verkoopbaar contact. Een contactpersoon die een verkoopbaar contact is geworden, blijft een verkoopbaar contact.

## <a name="templates"></a>Sjablonen

Klantgegevens omvatten alle informatie over de klant, zoals de klantgroep, adressen, contactgegevens, betalingsprofiel en factuurprofiel. Een verzameling tabeltoewijzingen werkt samen tijdens interactie met klantgegevens, zoals in de volgende tabel wordt weergegeven.

Apps voor financiën en bedrijfsactiviteiten | Customer Engagement-apps         | Beschrijving
----------------------------|---------------------------------|------------
[CDS-contactpersonen V2](mapping-reference.md#115) | contacten | Met deze sjabloon worden alle primaire, secundaire en tertiaire contactgegevens voor zowel klanten als leveranciers gesynchroniseerd.
[Klantengroepen](mapping-reference.md#126) | msdyn_customergroups | Met deze sjabloon worden klantengroepgegevens gesynchroniseerd.
[Betalingsmethode van klant](mapping-reference.md#127) | msdyn_customerpaymentmethods | Met deze sjabloon worden gegevens over de betalingsmethoden van klanten gesynchroniseerd.
[Klanten V3](mapping-reference.md#101) | rekeningen | Met deze sjabloon worden klantmodelgegevens voor commerciële en organisatorische klanten gesynchroniseerd.
[Klanten V3](mapping-reference.md#116) | contacten | Met deze sjabloon worden klantmodelgegevens voor consumenten en eindgebruikers gesynchroniseerd.
[Voor- en achtervoegsel naam](mapping-reference.md#155) | msdyn_nameaffixes | Met deze sjabloon worden referentiegegevens over voor- en achtervoegsels van namen voor zowel klanten als leveranciers gesynchroniseerd.
[Betalingsdagregels CDS V2](mapping-reference.md#157) | msdyn_paymentdaylines | Met deze sjabloon worden referentiegegevens over betalingsdagregels voor zowel klanten als leveranciers gesynchroniseerd.
[Betalingsdagen CDS](mapping-reference.md#158) | msdyn_paymentdays | Met deze sjabloon worden referentiegegevens over betalingsdagen voor zowel klanten als leveranciers gesynchroniseerd.
[Regels van betalingsschema](mapping-reference.md#159) | msdyn_paymentschedulelines | Met deze sjabloon worden referentiegegevens over betalingsschemaregels voor zowel klanten als leveranciers gesynchroniseerd.
[Betalingsplanning](mapping-reference.md#160) | msdyn_paymentschedules | Met deze sjabloon worden referentiegegevens over betalingsschema's voor zowel klanten als leveranciers gesynchroniseerd.
[Betalingstermijnen](mapping-reference.md#161) | msdyn_paymentterms | Met deze sjabloon worden referentiegegevens over betalingsvoorwaarden (voorwaarden voor betaling) voor zowel klanten als leveranciers gesynchroniseerd.

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]

