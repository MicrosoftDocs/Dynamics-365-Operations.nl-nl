---
title: Contactpersonen in Sales rechtstreeks synchroniseren met contactpersonen of klanten in Supply Chain Management
description: Dit onderwerp bepreekt de sjablonen en onderliggende taken die worden gebruikt om entiteiten van het type Contactpersoon (contactpersonen) en Contactpersoon (klanten) te synchroniseren rechtstreeks vanuit Dynamics 365 Sales naar Dynamics 365 Supply Chain Management.
author: ChristianRytt
ms.date: 10/25/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: 084030ab6ff06a1140621bb91435edf6cff4f82cc4bbc13813ab46f76e42174d
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/05/2021
ms.locfileid: "6756842"
---
# <a name="synchronize-contacts-directly-from-sales-to-contacts-or-customers-in-supply-chain-management"></a>Contactpersonen in Sales rechtstreeks synchroniseren met contactpersonen of klanten in Supply Chain Management

[!include [banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

> [!NOTE]
> Voordat u de oplossing Prospect naar contant geld kunt gebruiken, moet u vertrouwd zijn met [Gegevens integreren in Microsoft Dataverse for Apps](/powerapps/administrator/data-integrator).

Dit onderwerp bepreekt de sjablonen en onderliggende taken die worden gebruikt om tabellen van het type Contactpersoon (contactpersonen) en Contactpersoon (klanten) te synchroniseren rechtstreeks vanuit Dynamics 365 Sales naar Dynamics 365 Supply Chain Management.

## <a name="data-flow-in-prospect-to-cash"></a>Gegevensstroom in Prospect naar contant geld

De oplossing Prospect naar contant geld gebruikt de functie Gegevensintegratie om gegevens te synchroniseren tussen exemplaren van Supply Chain Management en Sales. De Prospect naar contant geld-sjablonen die beschikbaar zijn in de functie Gegevensintegratie activeren de stroom van gegevens over rekeningen, contactpersonen, producten, verkoopoffertes en verkoopfacturen tussen Supply Chain Management en Sales. De volgende afbeelding laat zien hoe de gegevens worden gesynchroniseerd tussen Supply Chain Management en Sales.

[![Gegevensstroom in Prospect naar contant geld.](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)

## <a name="templates-and-tasks"></a>Sjablonen en taken

Open het [PowerApps-beheercentrum](https://preview.admin.powerapps.com/dataintegration) om toegang te krijgen tot de beschikbare sjablonen. Selecteer **Projecten** en selecteer vervolgens in de rechterbovenhoek de optie **Nieuw project** om openbare sjablonen te selecteren.

De volgende sjablonen en onderliggende taken worden gebruikt voor het synchroniseren van tabellen Contactpersoon (contactpersonen) in Sales naar tabellen Contactpersoon (klanten) in Supply Chain Management:

- **Namen van de sjablonen in Gegevensintegratie**

    - Contacten (Sales naar Supply Chain Management) - Direct
    - Contactpersonen naar klant (Sales naar Supply Chain Management) - Direct

- **Namen van de taken in het project Gegevensintegratie**

    - Contacten
    - ContactToCustomer

De volgende synchronisatietaak is vereist voor de synchronisatie van contactpersonen: rekeningen (Sales naar Supply Chain Management)

## <a name="entity-sets"></a>Entiteitsets

| Verkopen    | Supply Chain Management |
|----------|------------------------|
| Contactpersonen | Dataverse-contactpersonen           |
| Contactpersonen | Klanten V2           |

## <a name="entity-flow"></a>Entiteitstroom

Contacten worden beheerd in Sales en gesynchroniseerd met Supply Chain Management

Een contactpersoon in Sales kan een contactpersoon of klant worden in Supply Chain Management. Om te bepalen of een contactpersoon in Sales als een contactpersoon of klant moet worden gesynchroniseerd met Supply Chain Management, wordt in het systeem naar de volgende eigenschappen van de contactpersoon in Sales gekeken:

- **Synchronisatie met een klant in Supply Chain Management:** contactpersonen waarvoor **Is actieve klant** is ingesteld op **Ja**
- **Synchronisatie met een contactpersoon in Supply Chain Management:** contactpersonen waarvoor **Is actieve klant** is ingesteld op **Nee** en **Bedrijf** (bovenliggende rekening/contactpersoon) verwijst naar een rekening (niet een contactpersoon)

## <a name="prospect-to-cash-solution-for-sales"></a>Oplossing Prospect naar contant geld voor Sales

Er is een nieuwe kolom **Is actieve klant** toegevoegd aan de contactpersoon. Deze kolom wordt gebruikt om onderscheid te maken tussen contactpersonen met verkoopactiviteiten en contactpersonen zonder verkoopactiviteiten. **Is actieve klant** is alleen ingesteld op **Ja** voor contactpersonen met gerelateerde offertes, orders of facturen. Alleen die contactpersonen worden als klanten gesynchroniseerd met Supply Chain Management.

Er wordt een nieuwe kolom **IsCompanyAnAccount** toegevoegd aan de contactpersoon. In deze kolom wordt aangegeven of een contactpersoon is gekoppeld aan een bedrijf (bovenliggend account/contactpersoon) van het type **Account**. Deze informatie wordt gebruikt ter identificatie van contactpersonen die als contactpersonen moeten worden gesynchroniseerd met Supply Chain Management.

Er is een nieuwe kolom **Contactnummer** toegevoegd aan de contactpersoon om een natuurlijke en unieke sleutel voor de integratie te garanderen. Wanneer u een nieuwe contactpersoon maakt, wordt automatisch een waarde voor **Contactnummer** gegenereerd op basis van een nummerreeks. De waarde bestaat uit **CON**, gevolgd door een stijgende nummerreeks en vervolgens een achtervoegsel van zes tekens. Bijvoorbeeld: **CON-01000-BVRCPS**

Wanneer de integratieoplossing voor Sales wordt toegepast, stelt een upgradescript de kolom **Contactnummer** in voor bestaande contactpersonen op basis van de eerder genoemde nummerreeks. Het upgradescript stelt ook de kolom **Is actieve klant** in op **Ja** voor contactpersonen met verkoopactiviteiten.

## <a name="in-supply-chain-management"></a>In Supply Chain Management

Contactpersonen worden gelabeld met de eigenschap **IsContactPersonExternallyMaintained**. Deze eigenschap geeft aan dat een bepaalde contactpersoon extern wordt beheerd. In dit geval worden extern beheerde contactpersonen beheerd in Sales.

## <a name="preconditions-and-mapping-setup"></a>Voorwaarden en instellingen voor toewijzing

### <a name="contact-to-customer"></a>Contactpersoon met klant

- **CustomerGroup** is vereist in Supply Chain Management. Om synchronisatiefouten te voorkomen, kunt u een standaardwaarde opgeven in de toewijzing. De standaardwaarde wordt vervolgens gebruikt als de kolom leeg is in Sales.

    De standaardsjabloonwaarde is **10**.

- Door de volgende toewijzingen toe te voegen, verkleint u het aantal vereiste handmatige updates in Supply Chain Management. U kunt een standaardwaarde of een waardetoewijzing gebruiken, bijvoorbeeld: **land/regio** of **plaats**.

    - **SiteId**: een standaardlocatie kan ook worden gedefinieerd voor producten in Supply Chain Management. SiteId: een site is vereist voor het genereren van offertes en verkooporders in Supply Chain Management.

        Er is geen sjabloonwaarde voor **SiteId** gedefinieerd.

    - **WarehouseId**: een standaardmagazijn kan ook worden gedefinieerd voor producten in Supply Chain Management. Een magazijn is vereist voor het genereren van offertes en verkooporders in Supply Chain Management.

        Er is geen sjabloonwaarde voor **WarehouseId** gedefinieerd.

    - **LanguageId**: een taal is vereist voor het genereren van offertes en verkooporders in Supply Chain Management.
    
        De standaardwaarde van de sjabloon is **en-us**.

## <a name="template-mapping-in-data-integration"></a>Sjabloontoewijzing in Gegevensintegratie

In de volgende afbeeldingen ziet u een voorbeeld van sjabloontoewijzing in Gegevensintegratie. 

> [!NOTE]
> Aan de hand van de toewijzing kunt u zien welke kolomgegevens vanuit Sales naar Supply Chain Management worden gesynchroniseerd.

### <a name="contact-to-contact"></a>Contactpersoon met contactpersoon

![Sjabloontoewijzing in gegevensintegrator.](./media/contacts-direct-template-mapping-data-integrator-1.png)

### <a name="contact-to-customer"></a>Contactpersoon met klant

![Sjabloontoewijzing in gegevensintegrator.](./media/contacts-direct-template-mapping-data-integrator-2.png)


## <a name="related-topics"></a>Verwante onderwerpen

[Van prospect tot contant geld](prospect-to-cash.md)

[Rekeningen rechtstreeks vanuit Sales synchroniseren met klanten in Supply Chain Management](accounts-template-mapping-direct.md)

[Producten rechtstreeks vanuit Supply Chain Management synchroniseren met producten in Sales](products-template-mapping-direct.md)

[Verkooporders rechtstreeks tussen Sales en Supply Chain Management synchroniseren](sales-order-template-mapping-direct-two-ways.md)

[Kopteksten en regels in verkoopfacturen rechtstreeks synchroniseren vanuit Supply Chain Management naar Sales](sales-invoice-template-mapping-direct.md)




[!INCLUDE[footer-include](../../includes/footer-banner.md)]