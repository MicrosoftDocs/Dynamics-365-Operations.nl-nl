---
title: Kopteksten en regels in verkoopoffertes vanuit Sales direct synchroniseren naar Finance and Operations
description: In dit onderwerp komen de sjablonen en onderliggende taken aan de orde voor het synchroniseren van kopteksten en regels van verkoopoffertes tussen Microsoft Dynamics 365 for Sales en Microsoft Dynamics 365 for Finance and Operations.
author: ChristianRytt
manager: AnnBe
ms.date: 11/14/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: josaw
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
ms.openlocfilehash: 97536c27dea113cc3c019473f22d1925e7617f8f
ms.contentlocale: nl-nl
ms.lasthandoff: 03/26/2018

---

# <a name="synchronize-sales-quotation-headers-and-lines-directly-from-sales-to-finance-and-operations"></a>Kopteksten en regels in verkoopoffertes vanuit Sales direct synchroniseren naar Finance and Operations

[!include [banner](../includes/banner.md)]

In dit onderwerp komen de sjablonen en onderliggende taken aan de orde voor het synchroniseren van kopteksten en regels van verkoopoffertes tussen Microsoft Dynamics 365 for Sales en Microsoft Dynamics 365 for Finance and Operations.

> [!NOTE]
> Voordat u de oplossing Prospect naar contant geld kunt gebruiken, moet u vertrouwd zijn met [Dynamics 365 Gegevensintegratie](/common-data-service/entity-reference/dynamics-365-integration).

## <a name="template-and-tasks"></a>Sjabloon en taken

De volgende sjabloon en onderliggende taken worden gebruikt voor het direct synchroniseren van kopteksten en regels van verkoopoffertes vanuit Sales naar Finance and Operations:

- **Naam van de sjabloon in Gegevensintegratie:** Verkoopoffertes (Sales naar Fin and Ops) - Direct
- **Namen van de taken in het project Gegevensintegratie:**

    - QuoteHeader
    - QuoteLine

De volgende synchronisatietaken zijn vereist voordat de synchronisatie van de kopteksten en regels van verkoopoffertes kan plaatsvinden:

- Producten (Fin and Ops naar Sales) - Direct
- Rekeningen (Sales naar Fin and Ops) - Direct (indien gebruikt)
- Contactpersonen naar klanten (Sales naar Fin and Ops) - Direct (indien gebruikt)

## <a name="entity-set"></a>Entiteitset

| Verkoop        | Finance en Operations     |
|--------------|----------------------------|
| Citaten       | CDS-verkoopoffertekoptekst |
| QuoteDetails | Regels van CDS-verkoopofferte  |

## <a name="entity-flow"></a>Entiteitstroom

Verkoopoffertes worden gemaakt in Sales en gesynchroniseerd met Finance and Operations.

Verkoopoffertes uit Sales worden alleen gesynchroniseerd als aan de volgende voorwaarden is voldaan:

- Alle offerteproducten in de verkoopofferte worden extern beheerd.
- Als u op **Offerte activeren** klikt, wordt de verkoopofferte actief.

## <a name="prospect-to-cash-solution-for-sales"></a>Oplossing Prospect naar contant geld voor Sales

Het veld **Heeft alleen extern onderhouden producten** is toegevoegd aan de entiteit **Offerte** om consistent bij te houden of de verkoopofferte geheel bestaat uit extern beheerde producten. Als een verkoopofferte alleen extern beheerde producten heeft, worden de producten beheerd in Finance and Operations. Zo garandeert u dat u niet verkoopofferteregels probeert te synchroniseren voor producten die onbekend zijn in Finance and Operations.

Alle offerteproducten in de verkoopofferte worden bijgewerkt met de informatie **Heeft alleen extern onderhouden producten** uit de verkoopoffertekoptekst. Deze informatie vindt u in het veld **Offerte heeft alleen extern onderhouden producten** voor de entiteit **QuoteDetails**.

Er kan een korting worden toegevoegd aan het offerteproduct en deze wordt gesynchroniseerd naar Finance and Operations. De velden **Korting**, **Toeslagen** en **Btw** in de koptekst worden bepaald door een configuratie in Finance and Operations. Deze configuratie biedt momenteel geen ondersteuning voor integratietoewijzing. In het huidige ontwerp worden de velden **Prijs**, **Korting**, **Toeslagen** en **Btw** beheerd en verwerkt in Finance and Operations.

In Sales worden de volgende velden alleen-lezen gemaakt, omdat de waarden niet worden gesynchroniseerd met Finance and Operations:

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

- Zorg ervoor dat de vereiste waardetoewijzing voor **SalesUnitSymbol** in Finance and Operations bestaat.
- Zorg ervoor dat de vereiste eenheden zijn gedefinieerd in Sales.

    Er wordt een sjabloonwaarde met een waardetoewijzing gedefinieerd voor **oumid.name** naar **SalesUnitSymbol**.

- U kunt desgewenst de volgende toewijzingen toevoegen om te garanderen dat verkoopofferteregels worden geïmporteerd in Finance and Operations als er geen standaardgegevens over de klant of het product zijn:

    - **SiteId**: een site is vereist voor het genereren van offertes en verkooporderregels in Finance and Operations. Er is geen standaardwaarde van de sjabloon voor **SiteId**.
    - **WarehouseId**: een magazijn is vereist voor het verwerken van offertes en verkooporderregels in Finance and Operations. Er is geen standaardwaarde van de sjabloon voor **WarehouseId**.

## <a name="template-mapping-in-data-integrator"></a>Sjabloontoewijzing in gegevensintegrator

> [!NOTE]
> - De velden **Korting**, **Toeslagen** en **Btw** worden bepaald door een complexe configuratie in Finance and Operations. Deze configuratie biedt momenteel geen ondersteuning voor integratietoewijzing. In het huidige ontwerp worden de velden **Prijs**, **Korting**, **Toeslagen** en **Btw** verwerkt door Finance and Operations.
> - De velden **Betalingsvoorwaarden**, **Leveringscondities**, **Leveringsvoorwaarden**, **Verzendmethode** en **Leveringsmethode** maken geen deel uit van de standaardtoewijzingen. Als u deze velden wilt toewijzen, moet u een waardetoewijzing instellen die specifiek is voor de gegevens in de organisaties waartussen de entiteit wordt gesynchroniseerd.

In de volgende afbeeldingen ziet u een voorbeeld van de toewijzing van een sjabloon in gegevensintegrator.

### <a name="quoteheader"></a>QuoteHeader

![Sjabloontoewijzing in gegevensintegrator](./media/sales-quotation-direct-template-mapping-data-integrator-1.png)

### <a name="quoteline"></a>QuoteLine

![Sjabloontoewijzing in gegevensintegrator](./media/sales-quotation-direct-template-mapping-data-integrator-2.png)

## <a name="related-topics"></a>Verwante onderwerpen

[Prospect naar contant geld](prospect-to-cash.md)


