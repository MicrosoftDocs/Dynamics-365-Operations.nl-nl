---
title: Rekeningen rechtstreeks vanuit Sales synchroniseren met klanten in Supply Chain Management
description: Dit onderwerp bespreekt de sjablonen en onderliggende taken die worden gebruikt om rekeningen rechtstreeks te synchroniseren van Dynamics 365 Sales naar Supply Chain Management.
author: Henrikan
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
ms.author: henrikan
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: f6f5662427be92ad57def2af772dd69abd575b81
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/29/2021
ms.locfileid: "7566498"
---
# <a name="synchronize-accounts-directly-from-sales-to-customers-in-supply-chain-management"></a>Rekeningen rechtstreeks vanuit Sales synchroniseren met klanten in Supply Chain Management

[!include [banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

> [!NOTE]
> Voordat u de oplossing Prospect naar contant geld kunt gebruiken, moet u vertrouwd zijn met [Gegevens integreren in Microsoft Dataverse for Apps](/powerapps/administrator/data-integrator).

Dit onderwerp bespreekt de sjablonen en onderliggende taken die worden gebruikt om rekeningen rechtstreeks te synchroniseren van Dynamics 365 Sales naar Dynamics 365 Supply Chain Management.

## <a name="data-flow-in-prospect-to-cash"></a>Gegevensstroom in Prospect naar contant geld

De oplossing Prospect naar contant geld gebruikt de functie Gegevensintegratie om gegevens te synchroniseren tussen exemplaren van Supply Chain Management en Sales.  De Prospect naar contant geld-sjablonen die beschikbaar zijn in de functie Gegevensintegratie activeren de stroom van gegevens over rekeningen, contactpersonen, producten, verkoopoffertes en verkoopfacturen tussen Supply Chain Management en Sales. De volgende afbeelding laat zien hoe de gegevens worden gesynchroniseerd tussen Supply Chain Management en Sales.

[![Gegevensstroom in Prospect naar contant geld.](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)

## <a name="templates-and-tasks"></a>Sjablonen en taken

Open het [Power Apps-beheercentrum](https://preview.admin.powerapps.com/dataintegration) om toegang te krijgen tot de beschikbare sjablonen. Selecteer **Projecten** en selecteer vervolgens in de rechterbovenhoek de optie **Nieuw project** om openbare sjablonen te selecteren.

De volgende sjabloon en onderliggende taak worden gebruikt voor het synchroniseren van rekeningen van Sales naar Supply Chain Management.

- **Naam van de sjabloon in Gegevensintegratie:** Rekeningen (Sales naar Fin and Ops) - Direct
- **Naam van de taak in het project:** Rekeningen - Klanten

Er hoeven geen synchronisatietaken te worden uitgevoerd voordat de synchronisatie van rekening/klant kan plaatsvinden.

## <a name="entity-set"></a>Entiteitset

| Verkoop    | Supply Chain Management |
|----------|------------------------|
| Rekeningen | Klanten V2           |

## <a name="entity-flow"></a>Entiteitstroom

Accounts worden beheerd in Sales en als klanten gesynchroniseerd met Supply Chain Management. De eigenschap **Wordt extern beheerd** is voor deze klanten ingesteld op **Ja** voor het volgen van klanten die afkomstig zijn uit Sales. Bij het factureren wordt deze informatie gebruikt voor het filteren van facturen die worden gesynchroniseerd met Sales.

## <a name="prospect-to-cash-solution-for-sales"></a>Oplossing Prospect naar contant geld voor Sales

De kolom **Rekeningnummer** is beschikbaar op de pagina **Rekening**. Het is een natuurlijke en unieke sleutel voor de ondersteuning van de integratie. De functie van de natuurlijke sleutel in de oplossing Customer Relationship Management (CRM) kan van invloed zijn op klanten die al gebruikmaken van de kolom **Rekeningnummer**, maar die geen unieke waarden voor **Rekeningnummer** per rekening gebruiken. De integratie-oplossing ondersteunt op dit moment dit geval niet.

Wanneer een nieuwe rekening wordt gemaakt, als een **rekeningnummer** waarde nog niet bestaat, wordt deze automatisch gegenereerd met behulp van een nummerreeks. De waarde bestaat uit **ACC**, gevolgd door een stijgende nummerreeks en vervolgens een achtervoegsel van zes tekens. Bijvoorbeeld: **ACC-01000-BVRCPS**

Wanneer de integratie-oplossing voor Sales wordt toegepast, stelt een upgradescript de kolom **Rekeningnummer** in voor bestaande rekeningen in Sales. Als er geen waarden zijn voor **Rekeningnummer**, wordt de eerder beschreven nummerreeks gebruikt.

## <a name="preconditions-and-mapping-setup"></a>Voorwaarden en instellingen voor toewijzing

- De toewijzing **CustomerGroupId** moet worden bijgewerkt naar een geldige waarde in Supply Chain Management. U kunt een standaardwaarde opgeven of u kunt de waarde instellen met behulp van een waardetoewijzing.

    De standaardsjabloonwaarde is **10**.

- Door de volgende toewijzingen toe te voegen, verkleint u het aantal vereiste handmatige updates in Supply Chain Management. U kunt een standaardwaarde of een waardetoewijzing gebruiken, bijvoorbeeld: **land/regio** of **plaats**.

    - **SiteId**: een site is vereist voor het genereren van offertes en verkooporderregels in Supply Chain Management. Een standaardsite kan afkomstig zijn uit het product of uit de orderkoptekst van de klant.

        De standaardsjabloonwaarde is **1**.

    - **WarehouseId**: een magazijn is vereist voor het verwerken van offertes en verkooporderregels in Supply Chain Management. Een standaardmagazijn kan afkomstig zijn uit het product of uit de orderkoptekst van de klant in Supply Chain Management.

        De standaardsjabloonwaarde is **13**.

    - **LanguageId**: een taal is vereist voor het genereren van offertes en verkooporders in Supply Chain Management. Standaard wordt de taal uit de orderkoptekst van de klant gebruikt.

        De standaardwaarde van de sjabloon is **en-us**.

## <a name="template-mapping-in-data-integration"></a>Sjabloontoewijzing in Gegevensintegratie

> [!NOTE]
> De kolommen **Betalingsvoorwaarden**, **Leveringscondities**, **Leveringsvoorwaarden**, **Verzendmethode** en **Leveringsmethode** maken geen deel uit van de standaardtoewijzingen. Als u deze kolommen wilt toewijzen, moet u een waardetoewijzing instellen die specifiek is voor de gegevens in de organisaties waartussen de tabel wordt gesynchroniseerd.

In de volgende afbeeldingen ziet u een voorbeeld van sjabloontoewijzing in Gegevensintegratie. 

> [!NOTE]
> Aan de hand van de toewijzing kunt u zien welke kolomgegevens vanuit Sales naar Supply Chain Management worden gesynchroniseerd.

![Sjabloontoewijzing in Gegevensintegratie.](./media/accounts-direct-template-mapping-data-integrator-1.png)

## <a name="related-topics"></a>Verwante onderwerpen


[Van prospect tot contant geld](prospect-to-cash.md)

[Rekeningen rechtstreeks vanuit Sales synchroniseren met klanten in Supply Chain Management](accounts-template-mapping-direct.md)

[Contactpersonen in Sales rechtstreeks synchroniseren met contactpersonen of klanten in Supply Chain Management](contacts-template-mapping-direct.md)

[Verkooporders rechtstreeks tussen Sales en Supply Chain Management synchroniseren](sales-order-template-mapping-direct-two-ways.md)

[Kopteksten en regels in verkoopfacturen rechtstreeks synchroniseren vanuit Supply Chain Management naar Sales](sales-invoice-template-mapping-direct.md)



[!INCLUDE[footer-include](../../includes/footer-banner.md)]