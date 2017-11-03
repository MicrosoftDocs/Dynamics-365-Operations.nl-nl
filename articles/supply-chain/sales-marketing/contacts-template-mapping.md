---
title: Contactpersonen synchroniseren tussen Sales met contactpersonen of klanten in Finance and Operations
description: In dit onderwerp komen de sjablonen en onderliggende taken aan de orde voor het synchroniseren van Contactpersoon (contactpersonen) en Contactpersoon (klanten) tussen Microsoft Dynamics 365 for Sales en Microsoft Dynamics 365 for Finance and Operations, Enterprise edition.
author: ChristianRytt
manager: AnnBe
ms.date: 08/28/2017
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
ms.dyn365.ops.intro: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 47e70cb1291e390b42b7feff844b2aca141f09b7
ms.openlocfilehash: 41e27776b94df059ada13efb9a3dbf6a29d67f36
ms.contentlocale: nl-nl
ms.lasthandoff: 09/29/2017

---

# <a name="synchronize-contacts-from-sales-to-contacts-or-customers-in-finance-and-operations"></a>Contactpersonen synchroniseren tussen Sales met contactpersonen of klanten in Finance and Operations

[!include[banner](../includes/banner.md)]

> [!NOTE]
> Voordat u de oplossing Prospect naar contant geld kunt gebruiken, moet u vertrouwd zijn met de functie [Dynamics 365 Gegevensintegratie](/common-data-service/entity-reference/dynamics-365-integration). 

In dit onderwerp komen de sjablonen en onderliggende taken aan de orde voor het synchroniseren van de entiteiten Contactpersoon (contactpersonen) en Contactpersoon (klanten) tussen Microsoft Dynamics 365 for Sales en Microsoft Dynamics 365 for Finance and Operations, Enterprise edition.

## <a name="templates-and-tasks"></a>Sjablonen en taken

De volgende sjablonen en onderliggende taken worden gebruikt voor het synchroniseren van Contactpersoon (contactpersonen) in Sales met Contactpersoon (klanten) in Finance en Operations:

- **De namen van de sjablonen:**

    - Contactpersonen (Sales met Fin and Ops)
    - Contactpersonen met klant (Sales met Fin and Ops)

- **Namen van de taken in het project:**

    - Contacten
    - ContactToCustomer

De volgende synchronisatietaak is vereist voor de synchronisatie van contactpersonen: rekeningen (Sales met Fin and Ops)

## <a name="entity-sets"></a>Entiteitsets

| Verkoop    | CDS     | Finance en Operations |
|----------|---------|------------------------|
| Contacten | Contactpersoon | CDS-contactpersonen           |
| Contacten | Rekening | Klanten V2           |

## <a name="entity-flow"></a>Entiteitstroom

Contactpersonen worden beheerd in Sales en gesynchroniseerd met Common Data Service (CDS) en Finance and Operations.

Een contactpersoon in Sales wordt een contactpersoon in CDS en Finance and Operations. Het kan ook een rekening worden in CDS en een klant Finance and Operations. Om te bepalen of een contactpersoon moet worden opgehaald in Sales voor synchronisatie met CDS en Finance and Operations (bijvoorbeeld contactpersonen in Sales &gt; Contactpersoon in CDS &gt; Contactpersonen in Finance and Operations), controleert het systeem de volgende eigenschappen van de contactpersoon in Sales:

- **Synchroniseren met Rekening in CDS en Klant in Finance and Operations:** Contactpersonen waarvoor **Is actieve klant** is ingesteld op **Ja**
- **Synchroniseren met Contactpersoon in CDS en Contactpersoon in Finance and Operations:** Contactpersonen waarvoor **Is actieve klant** is ingesteld op **Nee** en **Bedrijf** (Bovenliggende rekening/contactpersoon) verwijst naar een rekening (niet een contactpersoon)

## <a name="prospect-to-cash-solution-for-sales"></a>Oplossing Prospect naar contant geld voor Sales 

Er wordt een nieuw veld **Is actieve klant** toegevoegd aan de contactpersoon. Dit veld wordt gebruikt om onderscheid te maken tussen contactpersonen met verkoopactiviteit en contacten zonder verkoopactiviteiten. **Is actieve klant** is alleen ingesteld op **Ja** voor contactpersonen met gerelateerde offertes, orders of facturen. Alleen die contactpersonen worden als klanten gesynchroniseerd met Finance and Operations.

Er wordt een nieuw veld **IsCompanyAnAccount** toegevoegd aan de contactpersoon. Dit veld wordt gebruikt om aan te geven of een contactpersoon is gekoppeld aan een bedrijf (bovenliggende rekening/contactpersoon) van het type **rekening**. Deze informatie wordt gebruikt ter identificatie van de contactpersonen die als contactpersonen moeten worden gesynchroniseerd met Finance and Operations.

Er wordt een nieuw veld **Contactnummer** toegevoegd aan de Contactpersoon om een natuurlijke en unieke sleutel voor de integratie te garanderen. Wanneer u een nieuwe contactpersoon maakt, wordt automatisch een waarde voor **Contactnummer** gegenereerd met behulp van een nummerreeks. De waarde bestaat uit **CON**, gevolgd door een stijgende nummerreeks en vervolgens een achtervoegsel van zes tekens. Bijvoorbeeld: **CON-01000-BVRCPS**

Wanneer de integratie-oplossing voor Sales wordt toegevoegd aan Sales, stelt een upgradescript het veld **Contactnummer** in voor bestaande contactpersonen met behulp van de vermelde nummerreeks. Het upgradescript stelt ook het veld **Is actieve klant** in op **Ja** voor contactpersonen met verkoopactiviteiten.

## <a name="in-finance-and-operations"></a>In Finance and Operations 

Contactpersonen worden gelabeld met de eigenschap **IsContactPersonExternallyMaintained**. Deze eigenschap geeft aan dat een bepaalde contactpersoon extern wordt beheerd. In dit geval worden extern beheerde contactpersonen onderhouden in Sales.

## <a name="preconditions-and-mapping-setup"></a>Voorwaarden en instellingen voor toewijzing

### <a name="contact-to-contact"></a>Contact met Contact

- Werk **CDS-organisatie-id** bij in de toewijzing **Bron &gt; CDS**.

    - De standaardwaarde van de sjabloon voor **Organization_OrganizationId [Organization ID]** is **ORG001**.
    - De standaardwaarde van de sjabloon voor **PrimaryAccount_Organization_OrganizationId [Organization ID]** is **ORG001**.

- **Land-regiocode adres** is vereist in Finance and Operations. Om synchronisatiefouten te voorkomen kunt u een standaardwaarde opgeven in de toewijzing **CDS &gt; Operations**. De standaardwaarde wordt vervolgens gebruikt als het veld is leeg in Sales. De standaardwaarde in de sjabloon voor **PrimaryAddressCountryRegionISOCode** is **USA**.
- Zorg ervoor dat er een waarde voor het volgende veld bestaat in Finance and Operations. Als de informatie niet is vereist in Finance and Operations, kunt u de toewijzing verwijderen uit de toewijzing **CDS &gt; bestemming**.

    - **De naam in Finance and Operations.:** Beslissing
    - **Toewijzing:** PrimaryAccountRole = DecisionMakingRole

### <a name="contact-to-customer"></a>Contactpersoon met klant

- Werk **CDS-organisatie-id** bij in de toewijzing **Bron &gt; CDS**. De standaardwaarde van de sjabloon voor **Organization_OrganizationId [Organization ID]** is **ORG001**.
- **Land-regiocode adres** is vereist in Finance and Operations. Om synchronisatiefouten te voorkomen kunt u een standaardwaarde opgeven in de toewijzing **CDS &gt; Bestemming**. De standaardwaarde wordt vervolgens gebruikt als het veld is leeg in Sales. De standaardwaarde in de sjabloon voor **PrimaryAddressCountryRegionISOCode** is **USA**.
- **Klantgroep** is vereist in Finance and Operations. Om synchronisatiefouten te voorkomen kunt u een standaardwaarde opgeven in de toewijzing **CDS &gt; Bestemming**. De standaardwaarde wordt vervolgens gebruikt als het veld is leeg in Sales. De standaardwaarde in de sjabloon voor **CustomerGroupId** is **10**.
- Door het toevoegen van de volgende toewijzingen uit **CDS &gt; Bestemming**, verkleint u het aantal handmatige updates in Finance and Operations. U kunt een standaardwaarde of een waardetoewijzing gebruiken, bijvoorbeeld: **land/regio** of **plaats**.

    - **SiteId**: een standaardlocatie kan ook worden gedefinieerd voor producten in Finance and Operations. Een site is vereist voor het genereren van offertes en verkooporders in Finance and Operations. Er is geen sjabloonwaarde voor **SiteId** gedefinieerd.
    - **WarehouseId**: een standaardmagazijn kan ook worden gedefinieerd voor producten in Finance and Operations. Een magazijn is vereist voor het genereren van offertes en verkooporders in Finance and Operations. Er is geen sjabloonwaarde voor **WarehouseId** gedefinieerd.
    - **LanguageId**: een taal is vereist voor het genereren van offertes en verkooporders in Finance and Operations. De standaardwaarde van de sjabloon voor **LanguageId** is **en-us**.

## <a name="template-mapping-in-data-integrator"></a>Sjabloontoewijzing in gegevensintegrator

In de volgende afbeeldingen ziet u een voorbeeld van de toewijzing van een sjabloon in gegevensintegrator.

### <a name="contact-to-contact"></a>Contact met Contact

![Sjabloontoewijzing in gegevensintegrator](./media/contacts-template-mapping-data-integrator-1.png)

![Sjabloontoewijzing voor Contactpersonen in gegevensintegrator](./media/contacts-template-mapping-data-integrator-2.png)

### <a name="contact-to-customer"></a>Contactpersoon met klant

![Sjabloontoewijzing in gegevensintegrator](./media/contacts-template-mapping-data-integrator-3.png)

![Sjabloontoewijzing voor Contactpersonen in gegevensintegrator](./media/contacts-template-mapping-data-integrator-4.png)


## <a name="related-topics"></a>Verwante onderwerpen

[Producten uit Finance and Operations synchroniseren met producten in Sales](products-template-mapping.md)

[Rekeningen uit Sales synchroniseren met klanten in Finance and Operations](accounts-template-mapping.md)

[Kopteksten en regels in verkoopoffertes vanuit Sales synchroniseren naar Finance and Operations](sales-quotation-template-mapping.md)

[Kopteksten en regels in verkooporders synchroniseren vanuit Finance and Operations naar Sales](sales-order-template-mapping.md)

[Kopteksten en regels in verkoopfacturen synchroniseren vanuit Finance and Operations naar Sales](sales-invoice-template-mapping.md)

