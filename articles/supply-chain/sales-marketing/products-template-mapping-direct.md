---
title: Producten vanuit Finance and Operations direct synchroniseren met producten in Sales
description: In dit onderwerp komen de sjablonen en onderliggende taken aan de orde voor het synchroniseren van producten vanuit Microsoft Dynamics 365 for Finance and Operations naar Microsoft Dynamics 365 for Sales.
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
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: 3ae50372edcd473f2288f8172b71eac33e24b636
ms.contentlocale: nl-nl
ms.lasthandoff: 03/26/2018

---

# <a name="synchronize-products-directly-from-finance-and-operations-to-products-in-sales"></a>Producten van Finance and Operations rechtstreeks synchroniseren met producten in Sales

[!include[banner](../includes/banner.md)]

> [!NOTE]
> Voordat u de oplossing Prospect naar contant geld kunt gebruiken, moet u vertrouwd zijn met [Dynamics 365 Gegevensintegratie](/common-data-service/entity-reference/dynamics-365-integration).

In dit onderwerp komen de sjablonen en onderliggende taken aan de orde voor het rechtstreeks synchroniseren van producten vanuit Microsoft Dynamics 365 for Finance and Operations naar Microsoft Dynamics 365 for Sales.

## <a name="data-flow-in-prospect-to-cash"></a>Gegevensstroom in Prospect naar contant geld

De oplossing Prospect naar contant geld gebruikt de functie Gegevensintegratie om gegevens te synchroniseren tussen exemplaren van Finance and Operations en Sales. De Prospect naar contant geld-sjablonen die beschikbaar zijn in de functie Gegevensintegratie activeren de stroom van gegevens over rekeningen, contactpersonen, producten, verkoopoffertes en verkoopfacturen tussen Finance and Operations en Sales. De volgende afbeelding laat zien hoe de gegevens worden gesynchroniseerd tussen Finance and Operations en Sales.

[![Gegevensstroom in Prospect naar contant geld](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)

## <a name="templates-and-tasks"></a>Sjablonen en taken

Open het [PowerApps-beheercentrum](https://preview.admin.powerapps.com/dataintegration) om toegang te krijgen tot de beschikbare sjablonen. Selecteer **Projecten** en selecteer vervolgens in de rechterbovenhoek de optie **Nieuw project** om openbare sjablonen te selecteren.

De volgende sjabloon en onderliggende taken worden gebruikt voor het synchroniseren van producten van Finance and Operations naar Sales.

- **Naam van de sjabloon in Gegevensintegratie:** Producten (Fin and Ops naar Sales) - Direct
- **Naam van de taak in het project Gegevensintegratie:** Producten

Er hoeven geen synchronisatietaken te worden uitgevoerd voordat productsynchronisatie kan plaatsvinden.

## <a name="entity-set"></a>Entiteitset

| Finance en Operations     | Verkoop    |
|----------------------------|----------|
| Verkoopbare vrijgegeven producten | Producten |

## <a name="entity-flow"></a>Entiteitstroom

Producten worden beheerd in Finance and Operations en gesynchroniseeerd met Sales Met de gegevensentiteit **Verkoopbare vrijgegeven producten** in Finance and Operations worden alleen producten geëxporteerd die *verkoopbaar* zijn. Verkoopbare producten zijn producten die de informatie bevatten die ze nodig hebben om te kunnen worden gebruikt op een verkooporder. Dezelfde regels zijn van toepassing wanneer een product wordt gevalideerd met de functie **Valideren** op de pagina **Vrijgegeven product**.

Het productnummer wordt gebruikt als een sleutel. Dus wanneer productvarianten worden gesynchroniseerd naar Sales, heeft elke productvariant een afzonderlijke product-id.

## <a name="prospect-to-cash-solution-for-sales"></a>Oplossing Prospect naar contant geld voor Sales

In Sales is het nieuwe veld **Wordt extern beheerd** voor producten toegevoegd om aan te geven dat een bepaald product extern wordt beheerd. Standaard wordt de waarde ingesteld op **Ja** tijdens het importeren naar Sales. De volgende waarden zijn beschikbaar:

- **Ja**: het product is afkomstig uit Finance and Operations en kan niet worden bewerkt in Sales.
- **Nee**: het product is rechtstreeks in Sales ingevoerd.
- **(Leeg)**: het product bestond in Sales voordat de oplossing Prospect naar contant geld werd ingeschakeld.

Met het veld **Wordt extern beheerd** kunt u ervoor zorgen dat alleen offertes en verkooporders met extern onderhouden producten worden gesynchroniseerd naar Finance and Operations.

Extern onderhouden producten worden automatisch toegevoegd aan de eerste geldige prijslijst met dezelfde valuta. Prijslijsten worden alfabetisch op naam ingedeeld. De verkoopprijs van het product uit Finance and Operations wordt gebruikt als de prijs in de prijslijst. Daarom moet er een prijslijst in Sales bestaan voor elke productverkoopvaluta in Finance and Operations. De valuta voor de vrijgegeven verkoopbare producten wordt ingesteld op de boekhoudvaluta van de rechtspersoon waaruit het product wordt uitgevoerd.

> [!NOTE]
> Productsynchronisatie lukt alleen als er een prijslijst met een overeenkomende valuta is.

## <a name="preconditions-and-mapping-setup"></a>Voorwaarden en instellingen voor toewijzing

- Voordat u de synchronisatie voor het eerst uitvoert, vult u de tabel Verschillend product voor bestaande producten in Finance and Operations in. Bestaande producten worden pas gesynchroniseerd als deze taak is voltooid.

    1. Gebruik in Finance and Operations de zoekfunctie om te zoeken naar **Tabel met verschillende producten vullen**.
    2. Selecteer **Tabel met verschillende producten vullen** om de taak uit te voeren. Deze taak moet slechts één keer worden uitgevoerd.

- Zorg ervoor dat de vereiste waardetoewijzing voor de verkoopmaateenheid tussen Finance and Operations en Sales bestaat in de toewijzing van **SalesUnitSymbol** naar **DefaultUnit (Name)**.
- Werk de waardetoewijzing bij voor **Eenhedengroep** (**defaultuomscheduleid.name**) zodat deze overeenkomt met **Eenhedengroepen** in Sales.

    De standaardsjabloonwaarde is **Standaardmaateenheid**.

- Controleer of de verkoopmaateenheden voor alle producten uit Finance and Operations bestaan in Sales.
- Controleer of prijslijsten bestaan in Sales voor elke productverkoopvaluta in Finance and Operations.
- Wanneer producten worden gemaakt in Sales, kunnen ze de status **Concept** of **Actief** hebben. Het gedrag wordt beheerd via **Instellingen** > **Beheer** > **Systeeminstellingen** > **Sales** in Sales.

    Producten die de status **Concept** hebben wanneer ze worden gemaakt, moeten worden geactiveerd voordat ze kunnen worden toegevoegd aan offertes of verkooporders.

## <a name="template-mapping-in-data-integration"></a>Sjabloontoewijzing in Gegevensintegratie

In de volgende afbeelding ziet u een voorbeeld van sjabloontoewijzing in Gegevensintegratie. 

> [!NOTE]
> Aan de hand van de toewijzing kunt u zien welke veldgegevens vanuit Sales naar Finance and Operations worden gesynchroniseerd.

![Sjabloontoewijzing in Gegevensintegrator](./media/products-direct-template-mapping-data-integrator-1.png)


## <a name="related-topics"></a>Verwante onderwerpen

[Prospect naar contant geld](prospect-to-cash.md)

[Rekeningen in Sales direct synchroniseren naar klanten in Finance and Operations](accounts-template-mapping-direct.md)

[Contactpersonen vanuit Sales direct synchroniseren naar contactpersonen of klanten in Finance and Operations](contacts-template-mapping-direct.md)

[Kopteksten en regels in verkooporders rechtstreeks synchroniseren vanuit Finance and Operations naar Sales](sales-order-template-mapping-direct-two-ways.md)

[Kopteksten en regels in verkoopfacturen direct vanuit Finance and Operations synchroniseren naar Sales](sales-invoice-template-mapping-direct.md)




