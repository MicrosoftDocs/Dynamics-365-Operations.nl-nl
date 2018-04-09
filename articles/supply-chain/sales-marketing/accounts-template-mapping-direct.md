---
title: Rekeningen in Sales direct synchroniseren naar klanten in Finance and Operations
description: In dit onderwerp komen de sjablonen en onderliggende taken aan de orde voor het synchroniseren van accounts vanuit Microsoft Dynamics 365 for Sales naar Microsoft Dynamics 365 for Finance and Operations .
author: ChristianRytt
manager: AnnBe
ms.date: 10/26/2017
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
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: fb694db32638756328623c186594cf5ba2e7d6b8
ms.contentlocale: nl-nl
ms.lasthandoff: 03/26/2018

---

# <a name="synchronize-accounts-directly-from-sales-to-customers-in-finance-and-operations"></a>Accounts in Sales rechtstreeks synchroniseren met klanten in Finance and Operations

[!include[banner](../includes/banner.md)]

> [!NOTE]
> Voordat u de oplossing Prospect naar contant geld kunt gebruiken, moet u vertrouwd zijn met [Dynamics 365 Gegevensintegratie](/common-data-service/entity-reference/dynamics-365-integration).

In dit onderwerp komen de sjablonen en onderliggende taken aan de orde voor het rechtstreeks synchroniseren van accounts vanuit Microsoft Dynamics 365 for Sales naar Microsoft Dynamics 365 for Finance and Operations.

## <a name="data-flow-in-prospect-to-cash"></a>Gegevensstroom in Prospect naar contant geld

De oplossing Prospect naar contant geld gebruikt de functie Gegevensintegratie om gegevens te synchroniseren tussen exemplaren van Finance and Operations en Sales.  De Prospect naar contant geld-sjablonen die beschikbaar zijn in de functie Gegevensintegratie activeren de stroom van gegevens over rekeningen, contactpersonen, producten, verkoopoffertes en verkoopfacturen tussen Finance and Operations en Sales. De volgende afbeelding laat zien hoe de gegevens worden gesynchroniseerd tussen Finance and Operations en Sales.

[![Gegevensstroom in Prospect naar contant geld](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)

## <a name="templates-and-tasks"></a>Sjablonen en taken

Open het [PowerApps-beheercentrum](https://preview.admin.powerapps.com/dataintegration) om toegang te krijgen tot de beschikbare sjablonen. Selecteer **Projecten** en selecteer vervolgens in de rechterbovenhoek de optie **Nieuw project** om openbare sjablonen te selecteren.

De volgende sjabloon en onderliggende taak worden gebruikt voor het synchroniseren van rekeningen tussen Sales en Finance and Operations:

- **Naam van de sjabloon in Gegevensintegratie:** Rekeningen (Sales naar Fin and Ops) - Direct
- **Naam van de taak in het project:** Rekeningen - Klanten

Er hoeven geen synchronisatietaken te worden uitgevoerd voordat de synchronisatie van rekening/klant kan plaatsvinden.

## <a name="entity-set"></a>Entiteitset

| Verkoop    | Finance en Operations |
|----------|------------------------|
| Rekeningen | Klanten V2           |

## <a name="entity-flow"></a>Entiteitstroom

Rekeningen worden beheerd in Sales en als klanten gesynchroniseerd naar Finance and Operations. De eigenschap **Wordt extern beheerd** is voor deze klanten ingesteld op **Ja** voor het volgen van klanten die afkomstig zijn uit Sales. Bij het factureren wordt deze informatie gebruikt voor het filteren van facturen die worden gesynchroniseerd met Sales.

## <a name="prospect-to-cash-solution-for-sales"></a>Oplossing Prospect naar contant geld voor Sales

Het veld **Rekeningnummer** is beschikbaar op de pagina **Rekening**. Het is een natuurlijke en unieke sleutel voor de ondersteuning van de integratie. De functie van de natuurlijke sleutel in de oplossing Customer Relationship Management (CRM) kan van invloed zijn op klanten die al gebruikmaken van het veld **Rekeningnummer**, maar die geen unieke waarden voor **Rekeningnummer** per rekening gebruiken. De integratie-oplossing ondersteunt op dit moment dit geval niet.

Wanneer een nieuwe rekening wordt gemaakt, als een **rekeningnummer** waarde nog niet bestaat, wordt deze automatisch gegenereerd met behulp van een nummerreeks. De waarde bestaat uit **ACC**, gevolgd door een stijgende nummerreeks en vervolgens een achtervoegsel van zes tekens. Bijvoorbeeld: **ACC-01000-BVRCPS**

Wanneer de integratie-oplossing voor Sales wordt toegepast, stelt een upgradescript het veld **Rekeningnummer** in voor bestaande rekeningen in Sales. Als er geen waarden zijn voor **Rekeningnummer**, wordt de eerder beschreven nummerreeks gebruikt.

## <a name="preconditions-and-mapping-setup"></a>Voorwaarden en instellingen voor toewijzing

- De toewijzing **CustomerGroupId** moet worden bijgewerkt naar een geldige waarde in Finance and Operations. U kunt een standaardwaarde opgeven of u kunt de waarde instellen met behulp van een waardetoewijzing.

    De standaardsjabloonwaarde is **10**.

- Door de volgende toewijzingen toe te voegen, verkleint u het aantal vereiste handmatige updates in Finance and Operations. U kunt een standaardwaarde of een waardetoewijzing gebruiken, bijvoorbeeld: **land/regio** of **plaats**.

    - **SiteId**: een site is vereist voor het genereren van offertes en verkooporderregels in Finance and Operations. Een standaardsite kan afkomstig zijn uit het product of uit de orderkoptekst van de klant.

        De standaardsjabloonwaarde is **1**.

    - **WarehouseId**: een magazijn is vereist voor het verwerken van offertes en verkooporderregels in Finance and Operations. Een standaardmagazijn kan afkomstig zijn uit het product of uit de orderkoptekst van de klant in Finance and Operations.

        De standaardsjabloonwaarde is **13**.

    - **LanguageId**: een taal is vereist voor het genereren van offertes en verkooporders in Finance and Operations. Standaard wordt de taal uit de orderkoptekst van de klant gebruikt.

        De standaardwaarde van de sjabloon is **en-us**.

## <a name="template-mapping-in-data-integration"></a>Sjabloontoewijzing in Gegevensintegratie

> [!NOTE]
> De velden **Vetalingsvoorwaarden**, **Leveringscondities**, **Leveringsvoorwaarden**, **Verzendmethode** en **Leveringsmethode** maken geen deel uit van de standaardtoewijzingen. Als u deze velden wilt toewijzen, moet u een waardetoewijzing instellen die specifiek is voor de gegevens in de organisaties waartussen de entiteit wordt gesynchroniseerd.

In de volgende afbeeldingen ziet u een voorbeeld van sjabloontoewijzing in Gegevensintegratie. 

> [!NOTE]
> Aan de hand van de toewijzing kunt u zien welke veldgegevens vanuit Sales naar Finance and Operations worden gesynchroniseerd.

![Sjabloontoewijzing in Gegevensintegratie](./media/accounts-direct-template-mapping-data-integrator-1.png)

## <a name="related-topics"></a>Verwante onderwerpen


[Prospect naar contant geld](prospect-to-cash.md)

[Rekeningen in Sales direct synchroniseren naar klanten in Finance and Operations](accounts-template-mapping-direct.md)

[Contactpersonen vanuit Sales direct synchroniseren naar contactpersonen of klanten in Finance and Operations](contacts-template-mapping-direct.md)

[Kopteksten en regels in verkooporders rechtstreeks synchroniseren vanuit Finance and Operations naar Sales](sales-order-template-mapping-direct-two-ways.md)

[Kopteksten en regels in verkoopfacturen direct vanuit Finance and Operations synchroniseren naar Sales](sales-invoice-template-mapping-direct.md)


