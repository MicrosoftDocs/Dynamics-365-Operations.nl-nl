---
title: Klantorders in Retail Modern POS (MPOS)
description: Dit onderwerp bevat informatie over klantorders in Retail Modern POS (MPOS). Klantorders worden ook wel speciale orders genoemd. In dit onderwerp worden de gerelateerde parameters en transactiestromen besproken.
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailFunctionalityProfile
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 260594
ms.assetid: 6fc835ef-d62e-4f23-9d49-50299be642ca
ms.search.region: global
ms.search.industry: Retail
ms.author: anpurush
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: b54f39cc7896871d77f9371e6197bf6dbaac51de
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/15/2019
ms.locfileid: "1553571"
---
# <a name="customer-orders-in-retail-modern-pos-mpos"></a>Klantorders in Retail Modern POS (MPOS)

[!include [banner](includes/banner.md)]

Dit onderwerp bevat informatie over klantorders in Retail Modern POS (MPOS). Klantorders worden ook wel speciale orders genoemd. In dit onderwerp worden de gerelateerde parameters en transactiestromen besproken.

Veel detailhandelaren bieden de optie van klantorders, oftewel speciale orders, om aan verschillende product- en afhandelingsbehoeften te voldoen. Hierna vindt u enkele typische scenario's:

- Een klant wil dat de producten worden afgeleverd op een specifiek adres op een specifieke datum.
- Een klant wil producten bij een andere winkel of locatie ophalen dan de winkel of locatie waar de klant deze producten heeft gekocht.
- Een klant wil dat iemand anders de gekochte producten ophaalt.

Detailhandelaren gebruiken klantorders ook om verloren verkoop te minimaliseren waarmee anders voorraadtekorten kunnen worden veroorzaakt, omdat de producten op een ander tijdstip of een andere plaats kunnen worden afgeleverd of opgehaald.

## <a name="set-up-customer-orders"></a>Klantorders instellen

Hierna vindt u enkele parameters die kunnen worden ingesteld op de pagina **Parameters detailhandel** om te definiëren hoe klantorders worden afgehandeld:

- **Standaard aanbetalingspercentage**: geef het bedrag op dat de klant moet betalen als een aanbetaling voordat een order kan worden bevestigd. Het standaardaanbetalingsbedrag wordt als een percentage van de orderwaarde berekend. Afhankelijk van de bevoegdheden kan een winkelmedewerker het bedrag overschrijven met behulp van **Deposito overschrijven**.
- **Percentage annuleringskosten**: als een toeslag wordt toegepast wanneer een klantorder wordt geannuleerd, geeft u het bedrag van die toeslag op.
- **Code annuleringskosten**: als een toeslag wordt toegepast wanneer een klantorder wordt geannuleerd, wordt die toeslag weergegeven onder een toeslagcode in de verkooporder. Met deze parameter kunt u de annuleringstoeslagcode definiëren.
- **Code verzendkosten**: detailhandelaren kunnen extra kosten in rekening brengen voor het verzenden van producten aan een klant. Het bedrag van de verzendkosten wordt weergegeven onder een toeslagcode in de verkooporder. Gebruik deze parameter om de verzendkostencode toe te wijzen aan verzendkosten op de klantorder.
- **Verzendkosten terugbetalen**: geef op of verzendkosten die zijn gekoppeld aan een klantorder, kunnen worden gerestitueerd.
- **Maximumbedrag zonder toestemming**: als de verzendkosten kunnen worden gerestitueerd, geeft u het maximale bedrag van verzendkostenrestituties voor retourorders op. Als dit bedrag wordt overschreden, is overschrijving door de manager nodig is om met de restitutie te kunnen doorgaan. Voor de volgende scenario's kan restitutie van verzendkosten hoger zijn dan het bedrag dat oorspronkelijk is betaald:

    - Kosten worden toegepast op het niveau van de verkooporderkoptekst en wanneer een bepaalde hoeveelheid van een productregel wordt geretourneerd, kan de maximale restitutie van verzendkosten die is toegestaan voor de producten en de hoeveelheid, niet worden bepaald op een manier die werkt voor alle detailhandelklanten.
    - Verzendkosten worden voor elke verzending gemaakt. Als een klant producten meerdere keren retourneert en de detailhandelaar volgens het detailhandelaarsbeleid de kosten van gerestitueerde verzendkosten voor rekening neemt, zijn de gerestitueerde verzendkosten hoger dan de werkelijke verzendkosten.

## <a name="transaction-flow-for-customer-orders"></a>Transactiestroom voor klantorders

### <a name="create-a-customer-order-in-retail-modern-pos"></a>Een klantorder maken in Retail Modern POS

1. Voeg een klant aan de transactie toe.
2. Voeg producten aan de winkelwagen toe.
3. Klik op **Klantorder maken** en selecteer vervolgens het ordertype. Het ordertype kan een **Klantorder** of **Offerte** zijn.
4. Klik op **Selectie verzenden** of **Alles verzenden** als u de producten wilt verzenden naar een adres op de klantrekening, geef de gevraagde verzenddatum en de verzendkosten op.
5. Klik op **Selectie ophalen** of **Alles ophalen** om producten te selecteren die worden opgehaald vanuit de huidige winkel of een andere winkel op een bepaalde datum.
6. Het gestorte bedrag innen als een aanbetaling vereist is.

### <a name="edit-an-existing-customer-order"></a>Een bestaande klantorder bewerken

1. Klik op de startpagina op **Een order zoeken**.
2. Zoek en selecteer de order om te bewerken. Klik onder aan de pagina op **Bewerken**.

### <a name="pick-up-an-order"></a>Een order ophalen

1. Klik op de startpagina op **Een order zoeken**.
2. Selecteer de order die moet worden opgehaald. Klik onder aan de pagina op **Verzamelen en verpakken**.
3. Klik op **Ophalen**.

### <a name="cancel-an-order"></a>Een order annuleren

1. Klik op de startpagina op **Een order zoeken**.
2. Selecteer de order die u wilt annuleren. Klik onder aan de pagina op **Annuleren**.

### <a name="create-a-return-order"></a>Retourorder maken

1. Klik op de startpagina op **Een order zoeken**.
2. Selecteer de order die u wilt retourneren, selecteer de factuur voor de order en selecteer vervolgens de productregel voor de producten die moeten worden geretourneerd.
3. Klik onder aan de pagina op **Retourorder**.

## <a name="asynchronous-transaction-flow-for-customer-orders"></a>Asynchrone transactiestroom voor klantorders

Klantorders kunnen worden gemaakt via de POS-client (point of sale) in synchrone modus of de asynchrone modus.

### <a name="enable-customer-orders-to-be-created-in-asynchronous-mode"></a>Mogelijk maken dat klantorders in de asynchrone modus worden gemaakt

1. Klik op **Retail** &gt; **Kanaalinstellingen** &gt; **POS-instellingen** &gt; **POS-profiel** &gt; **Functionaliteitsprofielen**.
2. Stel op het sneltabblad **Algemeen** de optie **Klantorder maken in asynchrone modus** in op **Ja**.

Wanneer de optie **Klantorder maken in asynchrone modus** is ingesteld op **Ja**, worden klantorders altijd in de asynchrone modus gemaakt, zelfs als Retail Transaction Service (RTS) beschikbaar is. Als u deze optie instelt op **Nee**, worden klantorders altijd gemaakt in de synchrone modus via RTS. Wanneer klantorders in de asynchrone modus worden gemaakt, worden ze opgehaald en ingevoegd in Retail door taken op te vragen met Pull (P). De bijbehorende verkooporders worden gemaakt in Retail wanneer **Orders synchroniseren** handmatig of via een batchproces wordt uitgevoerd.

## <a name="additional-resources"></a>Aanvullende resources

[Hybride klantorders](hybrid-customer-orders.md)
