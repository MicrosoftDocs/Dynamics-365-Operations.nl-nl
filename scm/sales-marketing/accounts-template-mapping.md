---
title: Rekeningen uit Sales synchroniseren met klanten in Finance and Operations
description: In dit onderwerp komen de sjablonen en onderliggende taken aan de orde voor het synchroniseren van rekeningen tussen Microsoft Dynamics 365 for Sales en Microsoft Dynamics 365 for Finance and Operations, Enterprise edition.
author: ChristianRytt
manager: AnnBe
ms.date: 07/03/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: yuyus
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: ChristianRytt
ms.dyn365.ops.intro: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: b497f078d9786a5c7630e924da6bb04cad37f5e9
ms.contentlocale: nl-nl
ms.lasthandoff: 07/27/2017

---

# <a name="synchronize-accounts-from-sales-to-customers-in-finance-and-operations"></a>Rekeningen uit Sales synchroniseren met klanten in Finance and Operations

[!include[banner](../includes/banner.md)]

> [!NOTE]
> Voordat u de oplossing Prospect naar contant geld kunt gebruiken, moet u vertrouwd zijn met de functie [Dynamics 365 Gegevensintegratie](https://docs.microsoft.com/en-us/common-data-service/entity-reference/dynamics-365-integration). 

In dit onderwerp komen de sjablonen en onderliggende taken aan de orde voor het synchroniseren van rekeningen tussen Microsoft Dynamics 365 for Sales (Sales) en Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (Finance and Operations).

## <a name="template-and-task"></a>Sjabloon en taak

De volgende sjablonen en onderliggende taken worden gebruikt voor het synchroniseren van rekeningen tussen Sales en Finance and Operations:

- **Naam van de sjabloon:** Rekeningen (Sales naar Fin and Ops)
- **Naam van de taak in het project:** Rekeningen - Rekening - Klanten

Taken die nodig zijn voor het synchroniseren van rekening/klant: geen

## <a name="entity-set"></a>Entiteitset

| Verkoop    | CDS     | Finance en Operations |
|----------|---------|------------------------|
| Rekeningen | Rekening | Klanten                  |

## <a name="entity-flow"></a>Entiteitstroom

Rekeningen worden beheerd in Sales en gesynchroniseeerd met klanten in Finance and Operations De eigenschap **Wordt extern beheerd** is voor deze klanten ingesteld op **Ja** voor het bijhouden van klanten die afkomstig zijn uit Sales. Bij het factureren wordt deze informatie gebruikt voor het filteren van facturen die worden gesynchroniseerd met Sales.

## <a name="prospect-to-cash-solution-for-sales"></a>Oplossing Prospect naar contant geld voor Sales

Het veld **Rekeningnummer** is beschikbaar op de pagina **Rekening**. Het is een natuurlijke en unieke sleutel voor de ondersteuning van de integratie. De functie van de natuurlijke sleutel in de oplossing Customer Relationship Management (CRM) kan van invloed zijn op klanten die al gebruikmaken van het veld **Rekeningnummer**, maar die geen unieke waarden voor **Rekeningnummer** per rekening gebruiken. De integratie-oplossing ondersteunt op dit moment dit geval niet.

Wanneer een nieuwe rekening wordt gemaakt, als een **rekeningnummer** waarde nog niet bestaat, wordt deze automatisch gegenereerd met behulp van een nummerreeks. De waarde bestaat uit **ACC**, gevolgd door een stijgende nummerreeks en vervolgens een achtervoegsel van zes tekens. Bijvoorbeeld: **ACC-01000-BVRCPS**

Wanneer de integratie-oplossing voor Sales wordt toegepast, stelt een upgradescript het veld **Rekeningnummer** in voor bestaande rekeningen in Sales. Als er geen **rekeningnummer** waarden zijn, wordt de eerder beschreven nummerreeks gebruikt.

## <a name="preconditions-and-mapping-setup"></a>Voorwaarden en instellingen voor toewijzing

- **CustomerGroupId** moet worden bijgewerkt naar een geldige waarde in Finance and Operations. U kunt een standaardwaarde opgeven of u kunt de waarde instellen met behulp van een waardetoewijzing. De standaardsjabloonwaarde is **10**.
- **Land-regiocode adres** is vereist in Finance and Operations. Om synchronisatiefouten te voorkomen kunt u een standaardwaarde opgeven. De standaardwaarde wordt vervolgens gebruikt als het veld is leeg in Sales.

    - De standaardwaarde van de sjabloon voor **AddressCountryRegionISOCode** is **USA**.
    - De standaardwaarde in de sjabloon voor **DeliveryAddressCountryRegionISOCode** is **USA**.

- Door het toevoegen van de volgende toewijzingen uit **CDS &gt; Bestemming**, verkleint u het aantal vereiste handmatige updates in Finance and Operations. U kunt een standaardwaarde of een waardetoewijzing gebruiken, bijvoorbeeld: **land/regio** of **plaats**.

    - **SiteId**: een site is vereist voor het genereren van offertes en verkooporderregels in Finance and Operations. Een standaardsite kan afkomstig zijn uit het product of uit de orderkoptekst van de klant. De standaardwaarde in de sjabloon voor **SiteId** is **1**.
    - **WarehouseId**: een magazijn is vereist voor het verwerken van offertes en verkooporderregels in Finance and Operations. Een standaardmagazijn kan afkomstig zijn uit het product of uit de orderkoptekst van de klant in Finance and Operations. De standaardwaarde in de sjabloon voor **WarehouseId** is **13**.
    - **LanguageId**: een taal is vereist voor het genereren van offertes en verkooporders in Finance and Operations. Standaard wordt de taal uit de orderkoptekst van de klant gebruikt. De standaardwaarde van de sjabloon voor **LanguageId** is **en-us**.

- Werk de CDS-organisatie-id (**Organization_OrganizationId**) bij in de toewijzing **Bron &gt; CDS**. De standaardsjabloonwaarde is **ORG001**.

## <a name="template-mapping-in-data-integrator"></a>Sjabloontoewijzing in gegevensintegrator

> [!NOTE]
> De velden **Vetalingsvoorwaarden**, **Leveringscondities**, **Leveringsvoorwaarden**, **Verzendmethode** en **Leveringsmethode** maken geen deel uit van de standaardtoewijzingen. Als u deze velden wilt toewijzen, moet u een waardetoewijzing instellen. Waardetoewijzingen zijn specifiek voor de gegevens in de organisaties waartussen de entiteit wordt gesynchroniseerd.

In de volgende afbeeldingen ziet u een voorbeeld van de toewijzing van een sjabloon in gegevensintegrator.

![Sjabloontoewijzing in gegevensintegrator](./media/accounts-template-mapping-data-integrator-1.png)

![Sjabloontoewijzing voor Rekeningen in gegevensintegrator](./media/accounts-template-mapping-data-integrator-2.png)

## <a name="related-topics"></a>Verwante onderwerpen

[Producten uit Finance and Operations synchroniseren met producten in Sales](products-template-mapping.md)

[Contactpersonen synchroniseren tussen Sales met contactpersonen of klanten in Finance and Operations](contacts-template-mapping.md)

[Kopteksten en regels van verkoopofferte synchroniseren tussen Sales en Finance and Operations](sales-quotation-template-mapping.md)




