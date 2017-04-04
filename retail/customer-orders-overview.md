---
title: Orders van klanten-overzicht
description: Dit onderwerp biedt informatie over klanten en orders in Retail moderne POS (MPOS). Klantorders zijn ook bekend als speciale orders. Het onderwerp bevat een bespreking van de bijbehorende parameters en -stromen van de transactie.
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 260594
ms.assetid: 6fc835ef-d62e-4f23-9d49-50299be642ca
ms.search.region: global
ms.search.industry: Retail
ms.author: anpurush
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: 2f466dfe53ccf0be15ed0793b4a6dd371bdacc0d
ms.lasthandoff: 03/31/2017


---

# <a name="customer-orders-overview"></a>Orders van klanten-overzicht

Dit onderwerp biedt informatie over klanten en orders in Retail moderne POS (MPOS). Klantorders zijn ook bekend als speciale orders. Het onderwerp bevat een bespreking van de bijbehorende parameters en -stromen van de transactie.

Veel detailhandelaren bevatten de optie van de klant een universeel kanaal retail wereld, orders of speciale orders, verschillende behoeften voor het gewicht en de uitvoering van het product. Hier volgen enkele typische scenario's:

-   Een klant wil dat de producten moeten worden geleverd met een specifiek adres op een bepaalde datum.
-   Een klant wil afhalen producten van een winkel of de locatie die verschilt van de winkel of de locatie waar de klant die producten gekocht.
-   Een klant wil iemand anders om op te halen producten die de klant is gekocht.

Klantorders detailhandelaren ook gebruiken voor het minimaliseren van lagere verkoopcijfers die aandelen storingen anders veroorzaken kunnen, omdat de producten worden geleverd of in een ander tijdstip of plaats opgehaald.

## <a name="set-up-customer-orders"></a>Klantorders instellen
Hier volgen enkele van de parameters die kunnen worden ingesteld op de **parameters detailhandel** pagina kunt u definiëren hoe klantorders is voldaan:

-   **Standaard deposito percentage** : Geef het bedrag dat de klant moet betalen als storting voordat een order kan worden bevestigd. Het standaardbedrag deposito wordt berekend als een percentage van de orderwaarde. Afhankelijk van de bevoegdheden, een Winkelmedewerker mogelijk overschrijft het bedrag met behulp van **deposito overschrijven**.
-   **Percentage annuleringskosten** : als een toeslag wordt toegepast wanneer een klantorder wordt geannuleerd, de hoeveelheid die toeslag opgeven.
-   **Code annuleringskosten** : als een toeslag wordt toegepast wanneer een klantorder wordt geannuleerd, dat toeslagen worden weergegeven onder een code voor toeslagen op de verkooporder in Microsoft Dynamics AX. Met deze parameter kunt u de annulering toeslagcode definiëren.
-   **Transportkostencode** : detailhandelaren kunnen er extra kosten voor het verzenden van producten aan een klant in rekening brengen. Het bedrag van de verzendkosten die worden weergegeven onder een code voor toeslagen op de verkooporder in Dynamics AX. Gebruik deze parameter in de toeslagcode voor de toewijzen aan verzendkosten voor de bestelling.
-   **Betaalt verzendkosten** : Geef aan of de verzendkosten die gekoppeld aan een klantorder zijn terugbetaald.
-   **Maximumbedrag zonder toestemming** : als de verzendkosten worden teruggegeven, de maximale hoeveelheid shipping toeslag restituties voor retourorders opgeven. Als dit bedrag wordt overschreden, manager overschrijving nodig is om te kunnen doorgaan met de restitutie. Ten behoeve van de volgende scenario's, een restitutie van verzendkosten hoger zijn dan het bedrag dat oorspronkelijk is betaald:
    -   Kosten worden toegepast op het niveau van de verkooporderkop en wanneer bepaalde hoeveelheid van de productregel van een wordt geretourneerd, wordt de maximale vergoeding van de verzendkosten die is toegestaan voor de producten en de hoeveelheid kan niet worden bepaald in de manier die geschikt is voor alle detailhandelklanten.
    -   Verzendkosten worden voor elk exemplaar van de verzending gemaakt. Als een klant producten meerdere keren retourneert en van de detailhandelaar beleid bepaalt dat de leverancier de kosten van retouren verzendkosten draagt, niet de retour verzendkosten meer dan de werkelijke verzendkosten.

## <a name="transaction-flow-for-customer-orders"></a>De stroom van de transactie voor klantorders
### <a name="create-a-customer-order-in-retail-modern-pos"></a>Een klantorder maken in moderne detailhandel-POS

1.  Voeg een klant aan de transactie toe.
2.  Producten toevoegen aan de winkelwagen.
3.  Klik op **Klantorder maken**, en selecteer het ordertype. Het ordertype is een **klantorder** of **offerte**.
4.  Klik op **schip geselecteerd** of **Alles verzenden** als u wilt verzenden de producten in een adres voor de klantrekening, geef de gevraagde expeditiedatum en verzendkosten opgeven.
5.  Klik op **ophaling geselecteerd** of **op te halen alle** voor producten die wordt verwerkt vanuit de huidige winkel of een andere winkel op een bepaalde datum.
6.  Het gestorte bedrag verzamelen als een aanbetaling vereist is.

### <a name="edit-an-existing-customer-order"></a>Een bestaande klantorder bewerken

1.  Klik op de startpagina op **vindt u een order**.
2.  Zoek en selecteer de order om te bewerken. Onderaan op de pagina, klikt u op de **bewerken**.

### <a name="pick-up-an-order"></a>Een order ophalen

1.  Klik op de startpagina op **vindt u een order**.
2.  Selecteer de order om op te halen. Onderaan op de pagina, klikt u op **verzamelen en de**.
3.  Klik op **afhalen**.

### <a name="cancel-an-order"></a>Een order annuleren

1.  Klik op de startpagina op **vindt u een order**.
2.  Selecteer de order te annuleren. Onderaan op de pagina, klikt u op **annuleren**.

#### <a name="create-a-return-order"></a>Retourorder maken

1.  Klik op de startpagina op **vindt u een order**.
2.  Selecteer de order die u wilt terugkeren, selecteert u de factuur voor de order en selecteer vervolgens de productregel voor de producten om terug te keren.
3.  Onderaan op de pagina, klikt u op de **retourorder**.

## <a name="asynchronous-transaction-flow-for-customer-orders"></a>Asynchrone transactietransport voor klantorders
Klanten en orders kunnen worden gemaakt vanuit het punt van verkooppunten (POS)-client in de synchrone modus of de asynchrone modus.

### <a name="enable-customer-orders-to-be-created-in-asynchronous-mode"></a>Klanten en orders worden gemaakt in de asynchrone modus inschakelen

1.  In Dynamics AX, klikt u op **detailhandel en commerce**&gt;**instellingen voor het kanaal**&gt;**POS-instellingen**&gt;**POS profiel**&gt;**Functionaliteitsprofielen**.
2.  Op de **algemene** sneltabblad stellen de **Klantorder maken in de modus voor asynchrone** optie naar **Ja**.

Wanneer de **Klantorder maken in de modus voor asynchrone** optie is ingesteld op **Ja**, klanten en orders worden altijd gemaakt in de modus voor asynchrone, zelfs als Retail transactieservice (RTS) is beschikbaar. Als u deze optie instelt op **Nee**, klanten en orders worden altijd gemaakt in de synchrone modus via RTS. Wanneer klanten en orders worden gemaakt in de modus voor asynchrone, zijn ze opgehaald en ingevoegd in Dynamics AX door taken ophalen (P). De bijbehorende verkooporders worden gemaakt in Dynamics AX wanneer **orders synchroniseren** handmatig of via een batchproces wordt uitgevoerd.

<a name="see-also"></a>Zie ook
--------

[Hybride klantorders](hybrid-customer-orders.md)


