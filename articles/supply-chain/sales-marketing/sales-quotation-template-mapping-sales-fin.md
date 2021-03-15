---
title: Kopteksten en regels in verkoopoffertes rechtstreeks synchroniseren vanuit Sales naar Supply Chain Management
description: In dit onderwerp worden de sjablonen en onderliggende taken besproken die worden gebruikt voor het rechtstreeks synchroniseren van kopteksten en regels van verkoopoffertes van Dynamics 365 Sales naar Dynamics 365 Supply Chain Management.
author: ChristianRytt
manager: tfehr
ms.date: 10/25/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
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
ms.openlocfilehash: 19c7de1436b2fe4a859ac20d3db1fefa445a115f
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2021
ms.locfileid: "4991860"
---
# <a name="synchronize-sales-quotation-headers-and-lines-directly-from-sales-to-supply-chain-management"></a>Kopteksten en regels in verkoopoffertes rechtstreeks synchroniseren vanuit Sales naar Supply Chain Management

[!include [banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

In dit onderwerp worden de sjablonen en onderliggende taken besproken die worden gebruikt voor het rechtstreeks synchroniseren van kopteksten en regels van verkoopoffertes van Dynamics 365 Sales naar Dynamics 365 Supply Chain Management.

> [!NOTE]
> Voordat u de oplossing Prospect naar contant geld kunt gebruiken, moet u vertrouwd zijn met [Gegevens integreren in Microsoft Dataverse for Apps](https://docs.microsoft.com/powerapps/administrator/data-integrator).

## <a name="data-flow-in-prospect-to-cash"></a>Gegevensstroom in Prospect naar contant geld

De oplossing Prospect naar contant geld gebruikt de functie Gegevensintegratie om gegevens te synchroniseren tussen exemplaren van Supply Chain Management en Sales. De Prospect naar contant geld-sjablonen die beschikbaar zijn in de functie Gegevensintegratie activeren de stroom van gegevens voor rekeningen, contactpersonen, producten, verkoopoffertes en verkoopfacturen tussen Supply Chain Management en Sales. De volgende afbeelding laat zien hoe de gegevens worden gesynchroniseerd tussen Supply Chain Management en Sales.

[![Gegevensstroom in Prospect naar contant geld](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)

## <a name="template-and-tasks"></a>Sjabloon en taken

De volgende sjabloon en onderliggende taken worden gebruikt voor het direct synchroniseren van kopteksten en regels van verkoopoffertes vanuit Sales naar Supply Chain Management:

- **Naam van de sjabloon in Gegevensintegratie:** Verkoopoffertes (Sales naar Supply Chain Management) - Direct
- **Namen van de taken in het project Gegevensintegratie:**

    - QuoteHeader
    - QuoteLine

De volgende synchronisatietaken zijn vereist voordat de synchronisatie van de kopteksten en regels van verkoopoffertes kan plaatsvinden:

- Producten (Supply Chain Management naar Sales) - Direct
- Rekeningen (Supply Chain Management naar Sales) - Direct (wanneer gebruikt)
- Contactpersonen naar klanten (Sales naar Supply Chain Management) - Direct (indien gebruikt)

## <a name="entity-set"></a>Entiteitset

| Verkopen        | Supply Chain Management     |
|--------------|----------------------------|
| Citaten       | Dataverse-verkoopoffertekoptekst |
| QuoteDetails | Dataverse-verkoopofferteregels  |

## <a name="entity-flow"></a>Entiteitstroom

Verkoopoffertes worden gemaakt in Sales en gesynchroniseerd met Supply Chain Management.

Verkoopoffertes uit Sales worden alleen gesynchroniseerd als aan de volgende voorwaarden is voldaan:

- Alle offerteproducten in de verkoopofferte worden extern beheerd.
- Als u op **Offerte activeren** klikt, wordt de verkoopofferte actief.

## <a name="prospect-to-cash-solution-for-sales"></a>Oplossing Prospect naar contant geld voor Sales

Het veld **Heeft alleen extern onderhouden producten** is toegevoegd aan de entiteit **Offerte** om consistent bij te houden of de verkoopofferte geheel bestaat uit extern beheerde producten. Als een verkoopofferte alleen extern beheerde producten heeft, worden de producten beheerd in Supply Chain Management. Zo garandeert u dat u niet verkoopofferteregels probeert te synchroniseren voor producten die onbekend zijn bij Supply Chain Management.

Alle offerteproducten in de verkoopofferte worden bijgewerkt met de informatie **Heeft alleen extern onderhouden producten** uit de verkoopoffertekoptekst. Deze informatie vindt u in het veld **Offerte heeft alleen extern onderhouden producten** voor de entiteit **QuoteDetails**.

Er kan een korting worden toegevoegd aan het offerteproduct en deze wordt gesynchroniseerd naar Supply Chain Management. De velden **Korting**, **Toeslagen** en **Btw** in de koptekst worden bepaald door een configuratie in Supply Chain Management. Deze configuratie biedt momenteel geen ondersteuning voor integratietoewijzing. In het huidige ontwerp worden de velden **Prijs**, **Korting**, **Toeslagen** en **Btw** beheerd en verwerkt in Supply Chain Management.

In Sales worden de volgende velden alleen-lezen gemaakt, omdat de waarden niet worden gesynchroniseerd met Supply Chain Management.

- Alleen-lezenvelden in de koptekst van de verkoopofferte: **Kortingspercentage**, **Korting** en **Vrachtkosten**
- Alleen-lezenvelden voor offerteproducten: **Btw**

## <a name="preconditions-and-mapping-setup"></a>Voorwaarden en instellingen voor toewijzing

Voordat u verkoopoffertes synchroniseert, is het belangrijk de volgende instellingen bij te werken.

### <a name="setup-in-sales"></a>Instellingen in Sales

- Zorg ervoor dat er machtigingen zijn ingesteld voor het team waaraan de gebruiker uit uw verbindingsset in Sales is toegewezen. Als u voorbeeldgegevens gebruikt, heeft de gebruiker meestal beheerderstoegang, maar het team niet. Als het team geen beheerderstoegang heeft wanneer u het project uitvoert vanuit Gegevensintegratie, wordt een foutbericht weergegeven waarin wordt aangegeven dat het hoofdteam ontbreekt.

    Als u machtigingen voor het team wilt instellen, gaat u naar **instellingen** &gt; **Beveiliging** &gt; **Teams** en selecteert u het gewenste team. Selecteer **Rollen beheren** en selecteer vervolgens een rol met de gewenste machtigingen, zoals **Systeembeheerder**.

- Ga naar **Instellingen** &gt; **Beheer** &gt; **Systeeminstellingen** &gt; **Sales** en zorg ervoor dat de volgende instellingen worden gebruikt:

    - De optie **Systeem voor berekenen van systeemprijzen gebruiken** is ingesteld op **Ja**.
    - Het veld **Berekeningsmethode korting** is ingesteld op **Regelartikel**.

### <a name="setup-in-the-data-integration-project"></a>Instellingen in het project Gegevensintegratie

#### <a name="quoteheader"></a>QuoteHeader

- Zorg ervoor dat de vereiste toewijzing bestaat voor **Shipto\_country** naar **DeliveryAddressCountryRegionISOCode**. In de waardetoewijzing kunt u een standaardwaarde opgeven die moet worden gebruikt als de waarde leeg wordt gelaten. Laat de linkerkant leeg laat en stel de rechterkant in op het gewenste land of de gewenste regio. Op deze manier hoeft u geen land of regio op te geven voor nationale orders.

    De sjabloonwaarde is een toewijzingswaarde waarbij verschillende landen of regio's worden toegewezen en waarbij een lege waarde gelijk is aan de waarde **VS**.

#### <a name="quoteline"></a>QuoteLine

- Zorg ervoor dat de vereiste waardetoewijzing voor **SalesUnitSymbol** in Supply Chain Management bestaat.
- Zorg ervoor dat de vereiste eenheden zijn gedefinieerd in Sales.

    Er wordt een sjabloonwaarde met een waardetoewijzing gedefinieerd voor **oumid.name** naar **SalesUnitSymbol**.

- U kunt desgewenst de volgende toewijzingen toevoegen om te garanderen dat verkoopofferteregels worden geïmporteerd in Supply Chain Management als er geen standaardgegevens over de klant of het product zijn:

    - **SiteId**: een site is vereist voor het genereren van offertes en verkooporderregels in Supply Chain Management. Er is geen standaardwaarde van de sjabloon voor **SiteId**.
    - **WarehouseId**: een magazijn is vereist voor het verwerken van offertes en verkooporderregels in Supply Chain Management. Er is geen standaardwaarde van de sjabloon voor **WarehouseId**.

## <a name="template-mapping-in-data-integrator"></a>Sjabloontoewijzing in gegevensintegrator

> [!NOTE]
> - De velden **Korting**, **Toeslagen** en **Btw** in de koptekst worden bepaald door een complexe configuratie in Supply Chain Management. Deze configuratie biedt momenteel geen ondersteuning voor integratietoewijzing. In het huidige ontwerp worden de velden **Prijs**, **Korting**, **Toeslagen** en **Btw** verwerkt door Supply Chain Management.
> - De velden **Betalingsvoorwaarden**, **Leveringscondities**, **Leveringsvoorwaarden**, **Verzendmethode** en **Leveringsmethode** maken geen deel uit van de standaardtoewijzingen. Als u deze velden wilt toewijzen, moet u een waardetoewijzing instellen die specifiek is voor de gegevens in de organisaties waartussen de entiteit wordt gesynchroniseerd.

In de volgende afbeeldingen ziet u een voorbeeld van de toewijzing van een sjabloon in gegevensintegrator.

### <a name="quoteheader"></a>QuoteHeader

![Sjabloontoewijzing in gegevensintegrator](./media/sales-quotation-direct-template-mapping-data-integrator-1.png)

### <a name="quoteline"></a>QuoteLine

![Sjabloontoewijzing in gegevensintegrator](./media/sales-quotation-direct-template-mapping-data-integrator-2.png)

## <a name="related-topics"></a>Verwante onderwerpen

[Prospect naar contant geld](prospect-to-cash.md)



[!INCLUDE[footer-include](../../includes/footer-banner.md)]