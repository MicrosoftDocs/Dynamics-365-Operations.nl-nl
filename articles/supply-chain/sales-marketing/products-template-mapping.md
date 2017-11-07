---
title: Producten uit Finance and Operations synchroniseren met producten in Sales
description: In dit onderwerp komen de sjablonen en onderliggende taken aan de orde voor het synchroniseren van producten tussen Microsoft Dynamics 365 for Finance and Operations, Enterprise edition en Microsoft Dynamics 365 for Sales.
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
ms.openlocfilehash: 063a20f133a00620bdf389b0a52a90bc61e2f7d4
ms.contentlocale: nl-nl
ms.lasthandoff: 09/29/2017

---

# <a name="synchronize-products-from-finance-and-operations-to-products-in-sales"></a>Producten uit Finance and Operations synchroniseren met producten in Sales

[!include[banner](../includes/banner.md)]

> [!NOTE]
> Voordat u de oplossing Prospect naar contant geld kunt gebruiken, moet u vertrouwd zijn met de functie [Dynamics 365 Gegevensintegratie](/common-data-service/entity-reference/dynamics-365-integration). 

In dit onderwerp komen de sjablonen en onderliggende taken aan de orde voor het synchroniseren van producten tussen Microsoft Dynamics 365 for Finance and Operations, Enterprise edition en Microsoft Dynamics 365 for Sales.

## <a name="template-and-task"></a>Sjabloon en taak

De volgende sjablonen en onderliggende taken worden gebruikt voor het synchroniseren van producten tussen Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (Finance and Operations) en Microsoft Dynamics 365 for Sales (Sales).

-   Naam van de sjabloon: Producten (Fin and Ops naar Sales)

-   Naam van taak in project: Producten

Taken die nodig zijn voor het synchroniseren van product: geen

## <a name="entity-set"></a>Entiteitset

| **Finance and Operations** | **CDS** | **Verkoop**  |
|----------------------------|---------|------------|
| Verkoopbare vrijgegeven producten | Artikel | Producten   |

## <a name="entity-flow"></a>Entiteitstroom

Producten worden beheerd in Finance and Operations en gesynchroniseeerd met Sales De gegevensentiteit **Verkoopbare vrijgegeven producten** in Finance and Operations exporteert alleen producten die verkoopbaar zijn, wat betekent dat de producten de informatie bevatten die nodig is om te worden gebruikt op een verkooporder. Dezelfde regels zijn van toepassing wanneer een product wordt gevalideerd met de functie **Valideren** op de pagina **Vrijgegeven product**.

Het **Productnummer** wordt gebruikt als sleutel, wat betekent dat productvarianten met CDS en Sales worden gesynchroniseerd met afzonderlijke **product-id's** per **productvariant**.

## <a name="prospect-to-cash-solution-for-sales"></a>Oplossing Prospect naar contant geld voor Sales

In Sales wordt een nieuw veld **Wordt extern beheerd** voor de producten toegevoegd om aan te geven dat een bepaald product extern wordt beheerd. De waarde wordt standaard ingesteld op **Ja** tijdens het importeren in Sales.

-   **Wordt extern beheerd = Ja**: product is afkomstig uit Finance and Operations en kan niet worden bewerkt in Sales.

-   **Wordt extern beheerd = Nee**: product wordt rechtstreeks ingevoerd in Sales.

-   **Wordt extern beheerd = blanco**: product bestaat in Sales vóór het inschakelen van de oplossing Prospect naar contant geld.

De gegevens van **Wordt extern beheerd** worden gebruikt om ervoor te zorgen dat alleen **offertes** en **verkooporders** met **extern onderhouden producten** worden gesynchroniseerd met Finance and Operations.

**Extern onderhouden producten** worden automatisch toegevoegd aan de eerste geldige **prijslijst** met dezelfde valuta. Houd er rekening mee dat de lijst alfabetisch is ingedeeld op **Naam**. De verkoopprijs van het product van Finance and Operations wordt gebruikt als prijs op de **prijslijst**. Dit houdt in dat er in Sales een **prijslijst** moet zijn voor elke **productverkoopvaluta** in Finance and Operations. Valuta op de vrijgegeven verkoopbare producten wordt ingesteld op de boekhoudvaluta van de rechtspersoon, waaruit het product wordt uitgevoerd.

> [!NOTE]
> Productsynchronisatie mislukt zonder een **prijslijst** met de overeenkomende valuta.

## <a name="preconditions-and-mapping-setup"></a>Voorwaarden en instellingen voor toewijzing

-   Voordat u de allereerste synchronisatie uitvoert, vult u de **tabel Verschillend product** voor bestaande producten in Finance and Operations. Bestaande producten worden niet gesynchroniseerd totdat deze taak is voltooid.

    -   Gebruik in Finance and Operations de zoekfunctie om te zoeken naar **Tabel met verschillende producten vullen**.

    -   Klik op **Tabel met verschillende producten vullen** om de taak uit te voeren. Deze taak hoeft slechts één keer te worden uitgevoerd.

-   Controleer of de benodigde **ValueMap** voor **Maateenheid** voor verkopen voorkomt in Finance and Operations in **Bron \> CDS-toewijzing SalesUnitSymbol / DefaultSellingUnitOfMeasure**.

-   Werk de **CDS-organisatie-id Organization_OrganizationId** bij in **Bron -\> CDS**.

    -   De standaardsjabloonwaarde is ORG001.

-   Werk **ValueMap** bij voor **Eenhedengroep** (**defaultuomscheduleid.name**) in **CDS \> Bestemming** zodat deze overenkomt met de **Eenhedengroepen** in Sales.

    -   De standaardsjabloonwaarde is ingesteld op **Standaardmaateenheid**.

-   Controleer of alle verkoopmaateenheden voor producten van Finance and Operations bestaan in Sales met de waarde **CDS-selectielijsten**.

-   Controleer of **Prijslijsten** bestaan in Sales voor elke productverkoopvaluta in Finance and Operations.

-   Producten kunnen worden gemaakt in Sales met de status **Concept** of **Actief**. Dit wordt bepaald in **Systeeminstellingen** onder **Sales** in Sales.

    -   Producten die zijn gemaakt met de conceptstatus moeten worden geactiveerd voordat ze kunnen worden toegevoegd aan **Offerte** of **Verkooporder**.

## <a name="template-mapping-in-data-integrator"></a>Sjabloontoewijzing in gegevensintegrator

In de volgende afbeeldingen ziet u een voorbeeld van de toewijzing van een sjabloon in gegevensintegrator.

![sjabloontoewijzing in gegevensintegrator](./media/products-template-mapping-data-integrator-1.png)

![sjabloontoewijzing voor producten in gegevensintegrator](./media/products-template-mapping-data-integrator-2.png)

## <a name="related-topics"></a>Verwante onderwerpen

[Rekeningen uit Sales synchroniseren met klanten in Finance and Operations](accounts-template-mapping.md)

[Contactpersonen in Sales synchroniseren naar contactpersonen of klanten in Finance and Operations](contacts-template-mapping.md)

[Kopteksten en regels in verkoopoffertes vanuit Sales synchroniseren naar Finance and Operations](sales-quotation-template-mapping.md)

[Kopteksten en regels in verkooporders synchroniseren vanuit Finance and Operations naar Sales](sales-order-template-mapping.md)

[Kopteksten en regels in verkoopfacturen synchroniseren vanuit Finance and Operations naar Sales](sales-invoice-template-mapping.md)


