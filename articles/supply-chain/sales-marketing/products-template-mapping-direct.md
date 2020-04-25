---
title: Producten rechtstreeks vanuit Supply Chain Management synchroniseren met producten in Sales
description: Dit onderwerp bespreekt de sjablonen en onderliggende taken die worden gebruikt om producten te synchroniseren van Dynamics 365 Supply Chain Management naar Dynamics 365 Sales.
author: ChristianRytt
manager: tfehr
ms.date: 06/10/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: 85ea6d37079c965ac5ddfdc4cdd20f2f3d184e4f
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/02/2020
ms.locfileid: "3216075"
---
# <a name="synchronize-products-directly-from-supply-chain-management-to-products-in-sales"></a>Producten rechtstreeks vanuit Supply Chain Management synchroniseren met producten in Sales

[!include [banner](../includes/banner.md)]

> [!NOTE]
> Voordat u de oplossing Prospect naar contant geld kunt gebruiken, moet u vertrouwd zijn met [Gegevens integreren in Common Data Service for Apps](https://docs.microsoft.com/powerapps/administrator/data-integrator).

Dit onderwerp bespreekt de sjablonen en onderliggende taken die worden gebruikt om producten rechtstreeks te synchroniseren van Dynamics 365 Supply Chain Management naar Dynamics 365 Sales.

## <a name="data-flow-in-prospect-to-cash"></a>Gegevensstroom in Prospect naar contant geld

De oplossing Prospect naar contant geld gebruikt de functie Gegevensintegratie om gegevens te synchroniseren tussen exemplaren van Supply Chain Management en Sales. De Prospect naar contant geld-sjablonen die beschikbaar zijn in de functie Gegevensintegratie activeren de stroom van gegevens over rekeningen, contactpersonen, producten, verkoopoffertes en verkoopfacturen tussen Supply Chain Management en Sales. De volgende afbeelding laat zien hoe de gegevens worden gesynchroniseerd tussen Supply Chain Management en Sales.

[![Gegevensstroom in Prospect naar contant geld](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)

## <a name="templates-and-tasks"></a>Sjablonen en taken

Open het [Power Apps-beheercentrum](https://admin.powerapps.com/dataintegration) om toegang te krijgen tot de beschikbare sjablonen. Selecteer **Projecten** en selecteer vervolgens in de rechterbovenhoek de optie **Nieuw project** om openbare sjablonen te selecteren.

De volgende sjabloon en onderliggende taken worden gebruikt voor het synchroniseren van producten van Supply Chain Management naar Sales.

- **Naam van de sjabloon in Gegevensintegratie:** Producten (Supply Chain Management naar Sales) - Direct
- **Naam van de taak in het project Gegevensintegratie:** Producten

Er hoeven geen synchronisatietaken te worden uitgevoerd voordat productsynchronisatie kan plaatsvinden.

## <a name="entity-set"></a>Entiteitset

| Supply Chain Management    | Verkoop    |
|----------------------------|----------|
| Verkoopbare vrijgegeven producten | Producten |

## <a name="entity-flow"></a>Entiteitstroom

Producten worden beheerd in Supply Chain Management en gesynchroniseeerd met Sales Met de gegevensentiteit **Verkoopbare vrijgegeven producten** in Supply Chain Management worden alleen producten geëxporteerd die *verkoopbaar* zijn. Verkoopbare producten zijn producten die de informatie bevatten die ze nodig hebben om te kunnen worden gebruikt op een verkooporder. Dezelfde regels zijn van toepassing wanneer een product wordt gevalideerd met de functie **Valideren** op de pagina **Vrijgegeven product**.

Het productnummer wordt gebruikt als een sleutel. Dus wanneer productvarianten worden gesynchroniseerd naar Sales, heeft elke productvariant een afzonderlijke product-id.

## <a name="prospect-to-cash-solution-for-sales"></a>Oplossing Prospect naar contant geld voor Sales

In Sales is het nieuwe veld **Wordt extern beheerd** voor producten toegevoegd om aan te geven dat een bepaald product extern wordt beheerd. Standaard wordt de waarde ingesteld op **Ja** tijdens het importeren naar Sales. De volgende waarden zijn beschikbaar:

- **Ja**: het product is afkomstig uit Supply Chain Management en kan niet worden bewerkt in Sales.
- **Nee**: het product is rechtstreeks in Sales ingevoerd.
- **(Leeg)**: het product bestond in Sales voordat de oplossing Prospect naar contant geld werd ingeschakeld.

Met het veld **Wordt extern beheerd** kunt u ervoor zorgen dat alleen offertes en verkooporders met extern onderhouden producten worden gesynchroniseerd naar Supply Chain Management.

Extern onderhouden producten worden automatisch toegevoegd aan de eerste geldige prijslijst met dezelfde valuta. Prijslijsten worden alfabetisch op naam ingedeeld. De verkoopprijs van het product uit Supply Chain Management wordt gebruikt als de prijs in de prijslijst. Daarom moet er een prijslijst in Sales bestaan voor elke productverkoopvaluta in Supply Chain Management. De valuta voor de vrijgegeven verkoopbare producten wordt ingesteld op de boekhoudvaluta van de rechtspersoon waaruit het product wordt uitgevoerd.

> [!NOTE]
> - Productsynchronisatie lukt alleen als er een prijslijst met een overeenkomende valuta is.
> - U kunt bepalen welke prijslijst wordt gebruikt bij de integratie door pricelevelid.name [Default Price List (Name)] in het project Gegevensintegratie toe te wijzen. Gebruik voor de invoer alleen kleine letters. De standaardwaarde voor een prijslijst in Sales met de naam ‘Standaard’ is bijvoorbeeld als volgt: Doelveld: pricelevelid.name [Default Price List (Name)] en Toewijzingstype: [ { "transformType": "Default", "defaultValue": "standaard" } ].

## <a name="preconditions-and-mapping-setup"></a>Voorwaarden en instellingen voor toewijzing

- Voordat u de synchronisatie voor het eerst uitvoert, vult u de tabel Verschillend product voor bestaande producten in Supply Chain Management. Bestaande producten worden pas gesynchroniseerd als deze taak is voltooid.

    1. Gebruik in Supply Chain Management de zoekfunctie om te zoeken naar **Tabel met verschillende producten vullen**.
    2. Selecteer **Tabel met verschillende producten vullen** om de taak uit te voeren. Deze taak moet slechts één keer worden uitgevoerd.

- Controleer of de vereiste waardetoewijzing voor de verkoopmaateenheid tussen Supply Chain Management en Sales bestaat in de toewijzing van **SalesUnitSymbol** aan **DefaultUnit (Name)**.
- Werk de waardetoewijzing bij voor **Eenhedengroep** (**defaultuomscheduleid.name**) zodat deze overeenkomt met **Eenhedengroepen** in Sales.

    De standaardsjabloonwaarde is **Standaardmaateenheid**.

- Controleer of de verkoopmaateenheden voor alle producten uit Supply Chain Management bestaan in Sales.
- Controleer of prijslijsten bestaan in Sales voor elke productverkoopvaluta in Supply Chain Management.
- Wanneer producten worden gemaakt in Sales, kunnen ze de status **Concept** of **Actief** hebben. Het gedrag wordt beheerd via **Instellingen** > **Beheer** > **Systeeminstellingen** > **Sales** in Sales.

    Producten die de status **Concept** hebben wanneer ze worden gemaakt, moeten worden geactiveerd voordat ze kunnen worden toegevoegd aan offertes of verkooporders.

## <a name="template-mapping-in-data-integration"></a>Sjabloontoewijzing in Gegevensintegratie

In de volgende afbeelding ziet u een voorbeeld van sjabloontoewijzing in Gegevensintegratie. 

> [!NOTE]
> Aan de hand van de toewijzing kunt u zien welke veldgegevens vanuit Sales naar Supply Chain Management worden gesynchroniseerd.

![Sjabloontoewijzing in Gegevensintegrator](./media/products-direct-template-mapping-data-integrator-1.png)


## <a name="related-topics"></a>Verwante onderwerpen

[Van prospect naar contant geld](prospect-to-cash.md)

[Rekeningen rechtstreeks vanuit Sales synchroniseren met klanten in Supply Chain Management](accounts-template-mapping-direct.md)

[Contactpersonen in Sales rechtstreeks synchroniseren met contactpersonen of klanten in Supply Chain Management](contacts-template-mapping-direct.md)

[Verkooporders rechtstreeks tussen Sales en Supply Chain Management synchroniseren](sales-order-template-mapping-direct-two-ways.md)

[Kopteksten en regels in verkoopfacturen rechtstreeks synchroniseren vanuit Supply Chain Management naar Sales](sales-invoice-template-mapping-direct.md)



