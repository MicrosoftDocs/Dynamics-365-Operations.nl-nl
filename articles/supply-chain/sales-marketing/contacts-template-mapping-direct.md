---
title: Contactpersonen vanuit Sales direct synchroniseren naar contactpersonen of klanten in Finance and Operations
description: In dit onderwerp komen de sjablonen en onderliggende taken aan de orde voor het synchroniseren van de entiteiten in Contactpersoon (contactpersonen) en Contactpersoon (klanten) vanuit Microsoft Dynamics 365 for Sales naar Microsoft Dynamics 365 for Finance and Operations, Enterprise edition.
author: ChristianRytt
manager: AnnBe
ms.date: 10/25/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 0d409b3b7f19ca31d9c720bca191f1ddba81caa3
ms.openlocfilehash: 6269b73dfca46d455784046199463d3f86e653ae
ms.contentlocale: nl-nl
ms.lasthandoff: 03/13/2018

---

# <a name="synchronize-contacts-directly-from-sales-to-contacts-or-customers-in-finance-and-operations"></a>Contactpersonen vanuit Sales direct synchroniseren naar contactpersonen of klanten in Finance and Operations

[!include[banner](../includes/banner.md)]

> [!NOTE]
> Voordat u de oplossing Prospect naar contant geld kunt gebruiken, moet u vertrouwd zijn met [Dynamics 365 Gegevensintegratie](/common-data-service/entity-reference/dynamics-365-integration).

In dit onderwerp komen de sjablonen en onderliggende taken aan de orde voor het direct synchroniseren van de entiteiten in Contactpersoon (contactpersonen) en Contactpersoon (klanten) vanuit Microsoft Dynamics 365 for Sales naar Microsoft Dynamics 365 for Finance and Operations, Enterprise edition.

## <a name="data-flow-in-prospect-to-cash"></a>Gegevensstroom in Prospect naar contant geld

De oplossing Prospect naar contant geld gebruikt de functie Gegevensintegratie om gegevens te synchroniseren tussen exemplaren van Finance and Operations en Sales. De Prospect naar contant geld-sjablonen die beschikbaar zijn in de functie Gegevensintegratie activeren de stroom van gegevens over rekeningen, contactpersonen, producten, verkoopoffertes en verkoopfacturen tussen Finance and Operations en Sales. De volgende afbeelding laat zien hoe de gegevens worden gesynchroniseerd tussen Finance and Operations en Sales.

[![Gegevensstroom in Prospect naar contant geld](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)

## <a name="templates-and-tasks"></a>Sjablonen en taken

Open het [PowerApps-beheercentrum](https://preview.admin.powerapps.com/dataintegration) om toegang te krijgen tot de beschikbare sjablonen. Selecteer **Projecten** en selecteer vervolgens in de rechterbovenhoek de optie **Nieuw project** om openbare sjablonen te selecteren.

De volgende sjablonen en onderliggende taken worden gebruikt voor het synchroniseren van entiteiten in Contactpersoon (contactpersonen) in Sales naar entiteiten in Contactpersoon (klanten) in Finance and Operations:

- **Namen van de sjablonen in Gegevensintegratie:**

    - Contactpersonen (Sales naar Fin and Ops) - Direct
    - Contactpersonen met klant (Sales naar Fin and Ops) - Direct

- **Namen van de taken in het project Gegevensintegratie:**

    - Contacten
    - ContactToCustomer

De volgende synchronisatietaak is vereist voor de synchronisatie van contactpersonen: rekeningen (Sales naar Fin and Ops)

## <a name="entity-sets"></a>Entiteitsets

| Verkoop    | Finance en Operations |
|----------|------------------------|
| Contacten | CDS-contactpersonen           |
| Contacten | Klanten V2           |

## <a name="entity-flow"></a>Entiteitstroom

Contactpersonen worden beheerd in Sales en gesynchroniseerd naar Finance and Operations.

Een contactpersoon in Sales kan een contactpersoon of klant worden in Finance and Operations. Om te bepalen of een contactpersoon in Sales als een contactpersoon of klant moet worden gesynchroniseerd met Finance and Operations, wordt in het systeem naar de volgende eigenschappen van de contactpersoon in Sales gekeken:

- **Synchronisatie met een klant in Finance and Operations:** contactpersonen waarvoor **Is actieve klant** is ingesteld op **Ja**
- **Synchronisatie met een contactpersoon in Finance and Operations:** contactpersonen waarvoor **Is actieve klant** is ingesteld op **Nee** en **Bedrijf** (bovenliggende rekening/contactpersoon) verwijst naar een rekening (niet een contactpersoon)

## <a name="prospect-to-cash-solution-for-sales"></a>Oplossing Prospect naar contant geld voor Sales

Er is een nieuw veld **Is actieve klant** toegevoegd aan de contactpersoon. Dit veld wordt gebruikt om onderscheid te maken tussen contactpersonen met verkoopactiviteiten en contactpersonen zonder verkoopactiviteiten. **Is actieve klant** is alleen ingesteld op **Ja** voor contactpersonen met gerelateerde offertes, orders of facturen. Alleen die contactpersonen worden als klanten gesynchroniseerd met Finance and Operations.

Er wordt een nieuw veld **IsCompanyAnAccount** toegevoegd aan de contactpersoon. In dit veld wordt aangegeven of een contactpersoon is gekoppeld aan een bedrijf (bovenliggende rekening/contactpersoon) van het type **Rekening**. Deze informatie wordt gebruikt ter identificatie van contactpersonen die als contactpersonen moeten worden gesynchroniseerd met Finance and Operations.

Er is een nieuw veld **Contactnummer** toegevoegd aan de contactpersoon om een natuurlijke en unieke sleutel voor de integratie te garanderen. Wanneer u een nieuwe contactpersoon maakt, wordt automatisch een waarde voor **Contactnummer** gegenereerd op basis van een nummerreeks. De waarde bestaat uit **CON**, gevolgd door een stijgende nummerreeks en vervolgens een achtervoegsel van zes tekens. Bijvoorbeeld: **CON-01000-BVRCPS**

Wanneer de integratieoplossing voor Sales wordt toegepast, stelt een upgradescript het veld **Contactnummer** in voor bestaande contactpersonen op basis van de eerder genoemde nummerreeks. Het upgradescript stelt ook het veld **Is actieve klant** in op **Ja** voor contactpersonen met verkoopactiviteiten.

## <a name="in-finance-and-operations"></a>In Finance and Operations

Contactpersonen worden gelabeld met de eigenschap **IsContactPersonExternallyMaintained**. Deze eigenschap geeft aan dat een bepaalde contactpersoon extern wordt beheerd. In dit geval worden extern beheerde contactpersonen beheerd in Sales.

## <a name="preconditions-and-mapping-setup"></a>Voorwaarden en instellingen voor toewijzing

### <a name="contact-to-customer"></a>Contactpersoon met klant

- **Klantgroep** is vereist in Finance and Operations. Om synchronisatiefouten te voorkomen, kunt u een standaardwaarde opgeven in de toewijzing. De standaardwaarde wordt vervolgens gebruikt als het veld is leeg in Sales.

    De standaardsjabloonwaarde is **10**.

- Door de volgende toewijzingen toe te voegen, verkleint u het aantal vereiste handmatige updates in Finance and Operations. U kunt een standaardwaarde of een waardetoewijzing gebruiken, bijvoorbeeld: **land/regio** of **plaats**.

    - **SiteId**: een standaardlocatie kan ook worden gedefinieerd voor producten in Finance and Operations. Een site is vereist voor het genereren van offertes en verkooporders in Finance and Operations.

        Er is geen sjabloonwaarde voor **SiteId** gedefinieerd.

    - **WarehouseId**: een standaardmagazijn kan ook worden gedefinieerd voor producten in Finance and Operations. Een magazijn is vereist voor het genereren van offertes en verkooporders in Finance and Operations.

        Er is geen sjabloonwaarde voor **WarehouseId** gedefinieerd.

    - **LanguageId**: een taal is vereist voor het genereren van offertes en verkooporders in Finance and Operations.
    
        De standaardwaarde van de sjabloon is **en-us**.

## <a name="template-mapping-in-data-integration"></a>Sjabloontoewijzing in Gegevensintegratie

In de volgende afbeeldingen ziet u een voorbeeld van sjabloontoewijzing in Gegevensintegratie. 

> [!NOTE]
> Aan de hand van de toewijzing kunt u zien welke veldgegevens vanuit Sales naar Finance and Operations worden gesynchroniseerd.

### <a name="contact-to-contact"></a>Contactpersoon met contactpersoon

![Sjabloontoewijzing in Gegevensintegrator](./media/contacts-direct-template-mapping-data-integrator-1.png)

### <a name="contact-to-customer"></a>Contactpersoon met klant

![Sjabloontoewijzing in Gegevensintegrator](./media/contacts-direct-template-mapping-data-integrator-2.png)


## <a name="related-topics"></a>Verwante onderwerpen

[Prospect naar contant geld](prospect-to-cash.md)

[Rekeningen in Sales direct synchroniseren naar klanten in Finance and Operations](accounts-template-mapping-direct.md)

[Producten vanuit Finance and Operations direct synchroniseren met producten in Sales](products-template-mapping-direct.md)

[Kopteksten en regels in verkooporders direct vanuit Finance and Operations synchroniseren naar Sales](sales-order-template-mapping-direct-two-ways.md)

[Kopteksten en regels in verkoopfacturen direct vanuit Finance and Operations synchroniseren naar Sales](sales-invoice-template-mapping-direct.md)



