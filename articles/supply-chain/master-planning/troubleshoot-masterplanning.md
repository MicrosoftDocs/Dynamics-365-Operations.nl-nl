---
title: Problemen met hoofdplanning oplossen
description: In dit onderwerp wordt beschreven hoe u problemen kunt oplossen die kunnen optreden tijdens het werken met hoofdplanning.
author: SmithaNataraj
ms.date: 11/04/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-11-04
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 4dc3c5c8a1597fce4cc61461d16cd11ad80426eb8841871278772fcd7b8c86b1
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/05/2021
ms.locfileid: "6766626"
---
# <a name="troubleshoot-master-planning"></a>Problemen met hoofdplanning oplossen

In dit onderwerp wordt beschreven hoe u problemen kunt oplossen die kunnen optreden tijdens het werken met hoofdplanning.

## <a name="bill-of-materials-explosion-behaves-differently-for-firmed-production-orders-and-for-estimated-production-orders-for-manually-created-work"></a>De explosie van stuklijsten werkt anders voor gefiatteerde productieorders en voor geraamde productieorders voor handmatig gemaakt werk.

### <a name="issue-description"></a>Probleembeschrijving

Wanneer een productieorder wordt gefiatteerd, worden de artikelen niet geëxplodeerd wanneer u de stuklijst explodeert. Wanneer u echter handmatig een werkorder maakt en vervolgens de productieorder raamt, worden de artikelen geëxplodeerd.

### <a name="issue-resolution"></a>Probleemoplossing

Het systeem werkt naar behoren. De explosie die plaatsvindt wanneer de productieorder wordt gefiatteerd, verwijst naar de geplande order, maar er wordt in dat geval niet aangegeven dat de geplande order momenteel is gefiatteerd. Als de productieorder echter is geraamd, wordt de explosie geactiveerd vanuit de vrijgegeven productieorder waarvoor geen geplande order bestaat.

## <a name="the-delay-value-isnt-updated-when-i-reschedule-a-planned-order"></a>De waarde van de vertraging wordt niet bijgewerkt wanneer ik een geplande order opnieuw plan.

Als u de vertraging voor geplande orders wilt bijwerken, opent u het dialoogvenster **Opnieuw plannen** voor de geplande order. Controleer op het sneltabblad **Explosie** of de optie **Explosie uitvoeren na herplanning** is ingesteld op *Ja*.

## <a name="production-scheduling-doesnt-consider-the-safety-margins-that-are-set-on-the-item-coverage-for-pegged-supply"></a>Productieplanning houdt geen rekening met de veiligheidsmarges die zijn ingesteld voor de artikelbehoefte voor getraceerd aanbod.

### <a name="issue-description"></a>Probleembeschrijving

Met de veiligheidsmarges wordt in de hoofdplanning rekening gehouden. De veiligheidsmarges worden echter genegeerd wanneer geplande productieorders worden gepland.

### <a name="issue-resolution"></a>Probleemoplossing

Met marges wordt alleen rekening gehouden tijdens de hoofdplanning, niet tijdens handmatige planning. Marges zijn ontworpen om als een buffer te fungeren tijdens de planningsfase, om enige speling te bieden voor het feitelijke proces.

U kunt het gewenste resultaat weergeven door de marge te verwijderen. De route moet vervolgens worden bijgewerkt zodat deze de gewenste tijd omvat (bijvoorbeeld de wachttijd voor de wachtrijen). De hoofdplanning en de handmatige planning moeten vervolgens hetzelfde resultaat opleveren.

## <a name="planned-orders-are-generated-even-though-we-have-items-in-stock-and-production-orders-already-exist-for-them"></a>Er worden geplande orders gegenereerd, hoewel er al artikelen in voorraad of productieorders voor zijn.

U kunt dit probleem mogelijk oplossen door de waarde van de **Positieve dagen** te verhogen voor de relevante groepen op de pagina **Behoefteplanningsgroep**. Door deze wijziging wordt door het systeem bepaald of de voorhanden voorraad voor de vraag kan worden gebruikt. Er wordt dan geen nieuwe geplande order gegenereerd voor de artikelen die in voorraad zijn.

## <a name="master-planning-doesnt-seem-to-respect-capacity-limitations-and-is-scheduling-more-than-the-available-capacity"></a>De capaciteitsbeperkingen worden niet door de hoofdplanning in acht genomen en er wordt meer dan de beschikbare capaciteit gepland.

### <a name="issue-description"></a>Probleembeschrijving

Wanneer u bewerkingsplanning gebruikt waarbij er sprake is van een eindige capaciteit en waar in de route een combinatie van vereisten voor zowel een resourcegroep als afzonderlijke resources is opgegeven, is er een kleine kans op overboeking door de manier waarop het algoritme de validatie van capaciteitsconflicten valideert. Deze overboeking kan optreden wanneer u helpers gebruikt om de hoofdplanning uit te voeren. Dit wordt waarschijnlijk veroorzaakt door een groot aantal taken met een relatief korte runtime.

### <a name="issue-resolution"></a>Probleemoplossing

Als het van essentieel belang is dat er geen overboekingen plaatsvinden voor de bewerkingsplanning, kunt u het planningsgedeelte van de hoofdplanning met afzonderlijke threads maken door de optie **Nauwkeurige eindige capaciteit voor bewerkingsplanning** in te schakelen op de pagina **Parameters hoofdplanning**. Deze optie is niet standaard beschikbaar. U moet dit handmatig aan de pagina toevoegen met behulp van de functies voor persoonlijke instellingen. Wanneer u deze optie gebruikt, wordt de planning langzamer uitgevoerd vanwege het gebrek aan parallelle verwerking.

## <a name="planned-orders-take-a-long-time-to-update"></a>Het bijwerken van geplande orders duurt erg lang.

### <a name="issue-description"></a>Probleembeschrijving

Wanneer u de behoeftehoeveelheid en/of leveringsdatum op een geplande order bijwerkt, duurt het doorgaans minimaal 30 seconden per order om de update op te slaan.

### <a name="issue-resolution"></a>Probleemoplossing

Dit is een bekend probleem met de ingebouwde hoofdplanningsengine. Dit wordt veroorzaakt door de onderliggende automatische explosie via de stuklijststructuur tijdens bewerkingen. Dit probleem wordt verholpen in planningsoptimalisatie, waarbij een planner de relevante orders kan bijwerken en goedkeuren en zo nodig een planningsuitvoering kan activeren om geplande orders voor de onderliggende stuklijststructuur bij te werken.

Een manier om de prestaties te verbeteren met de ingebouwde hoofdplanningsengine bestaat uit de volgende stappen:

1. Ga naar **Hoofdplanning \> Instellen \> Plannen \> Hoofdplannen**.
1. Een plan selecteren.
1. Vouw het sneltabblad **Time fence in dagen** uit.
1. Stel **Explosie** in op *Ja* en stel het veld onder deze instelling in op 0 (nul).

> [!NOTE]
> Hierdoor wordt de periode voor explosies die voor dit hoofdplan worden uitgevoerd tot één dag beperkt.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]