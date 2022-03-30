---
title: Op verzoek synchroniseren met de Supply Chain Management-prijsengine
description: In dit onderwerp wordt beschreven hoe u de prijsengine in Microsoft Dynamics 365 Supply Chain Management gebruikt vanuit Microsoft Dynamics 365 Sales.
author: RamaKrishnamoorthy
ms.date: 03/10/2019
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 6b0cc8f403be866ff00b89a33f6c59089c987bb0
ms.sourcegitcommit: 9c19898e1f41495f804c7f07e2636b53a098c4c1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/10/2022
ms.locfileid: "8402825"
---
# <a name="sync-on-demand-with-the-supply-chain-management-pricing-engine"></a>Op verzoek synchroniseren met de Supply Chain Management-prijsengine

[!include [banner](../../includes/banner.md)]

Microsoft Dynamics 365 Supply Chain Management bevat een prijsengine waarmee handelsovereenkomsten, prijslijsten, klantloyaliteitsprogramma's, promoties en kortingen worden afgehandeld. De prijsengine gebruikt complexe regels om de beste prijs voor een bepaalde offerte of order te bepalen. Wanneer u Twee keer wegschrijven gebruikt, gebruikt u statische prijzen of de prijsengine van Supply Chain Management op de pagina's **Offerte** en **Order** in Microsoft Dynamics 365 Sales.

## <a name="use-the-pricing-engine-from-supply-chain-management-in-sales"></a>De prijsengine uit Supply Chain Management in Sales gebruiken

1. Ga in Sales naar **Verkoop \> Orders**.
1. Selecteer **Nieuw** om een nieuwe order te maken of selecteer een bestaande order in de lijst **Mijn orders**.
1. Voeg een nieuwe orderregel toe.
1. Als u een nieuwe order maakt, selecteert u **Prijsorder** in het actievenster. Als u een bestaande order bijwerkt, selecteert u **Opnieuw berekenen** in het actievenster.
1. De volgende kolommen worden automatisch ingevuld:

    - Detailbedrag
    - Kortingspercentage
    - Korting
    - Bedrag vóór vracht
    - Vrachtkosten
    - Totale belasting
    - Totaalbedrag

> [!NOTE]
> Een vergelijkbaar proces is van toepassing wanneer u offertes maakt.

## <a name="how-it-works"></a>Hoe het werkt

Wanneer u een order in Verkoop maakt, wordt deze order onmiddellijk gesynchroniseerd met Supply Chain Management door de waarden te gebruiken die u in Verkoop hebt ingevoerd. Wanneer u **Prijsorder** of **Prijsofferte** selecteert in Verkoop, berekent Supply Chain Management de prijs voor elke orderregel en de totale order op basis van de handelsovereenkomstregels die in Supply Chain Management zijn gedefinieerd. De nieuwe berekende waarden worden vervolgens weer gesynchroniseerd naar Verkoop.

## <a name="set-trade-agreement-evaluation-options-in-supply-chain-management"></a>Evaluatieopties voor handelsovereenkomst instellen in Supply Chain Management

U kunt Supply Chain Management configureren om handelsovereenkomsten te respecteren of te negeren wanneer hiermee de prijs wordt berekend van een order die in Verkoop is gemaakt. Volg deze stappen om deze optie in te stellen.

1. Meld u aan bij uw Supply Chain Management-omgeving.
1. Ga naar **Klanten \> Instellen \> Parameters van module Klanten**.
1. Voeg op het tabblad **Prijzen** in het sneltabblad **Handelsovereenkomstevaluatie** de rij voor het **handmatige invoerbeleid** toe of verwijder deze. De aan- of afwezigheid van dit beleid bepaalt of de verkoopprijs die in Verkoop is ingevoerd, automatisch wordt overschreven door de prijsstellingsenengine van Supply Chain Management.

    - Als het beleid voor **Handmatige invoer** *niet* aanwezig is in de Supply Chain Management-instellingen voor **Evaluatie van handelsovereenkomst**, is Supply Chain Management het prijsmodel. Wanneer een gebruiker een **Prijsorder** of **Prijsofferte** selecteert in het actievenster in verkoop, wordt de Supply Chain Management-prijsenengine aangeroepen en wordt de verkoopprijs die is ingevoerd in Verkoop overschreven, tenzij deze gelijk is aan de verkoopprijs die is berekend in Supply Chain Management.
    - Als het beleid voor **Handmatige invoer** *wel* aanwezig is in de Supply Chain Management-instellingen voor **Evaluatie van handelsovereenkomst**, is Verkoop het prijsmodel. De verkoopprijs die is ingevoerd in Verkoop kan niet automatisch worden overschreven wanneer een gebruiker **Prijsorder** of **Prijsofferte** selecteert in het actievenster in Verkoop.
    - Orderregels en offerteregels met een **prijs per eenheid** en/of **kortingswaarde** van *0* (nul) in Verkoop worden als een speciaal geval behandeld. Als er een relevante handelsovereenkomstprijs beschikbaar is, wordt deze *altijd* toegepast op deze velden, ongeacht de Supply Chain Management-instellingen voor **Evaluatie van de handelsovereenkomst**.

    Bekijk voor elk van deze gevallen de scenario's die volgen.

## <a name="example-scenario-1-trade-agreement-evaluation-without-the-manual-entry-option"></a>Voorbeeldscenario 1: Evaluatie van handelsovereenkomst zonder de optie Handmatige invoer

In dit scenario is het beleid voor **Handmatige invoer** *niet* aanwezig is in de Supply Chain Management-instellingen voor **Evaluatie van handelsovereenkomst**. Een verkoopgebruiker voert een orderregel in met een niet-nulverkoopprijs in Verkoop en er wordt geen verkoopprijs gedefinieerd voor het artikel in Supply Chain Management.

1. In Verkoop maakt een gebruiker een orderregel met een waarde voor **Prijs per eenheid** van 1 Amerikaanse dollar (USD).
1. De orderregel wordt gesynchroniseerd met Supply Chain Management met een verkoopprijs van 1 USD.
1. In Verkoop selecteert de gebruiker **Prijsorder** in het actievenster.
1. Supply Chain Management zoekt naar relevante prijzen en kortingen en berekent vervolgens totalen. Aangezien het artikel geen verkoopprijs heeft in Supply Chain Management, wordt de regel automatisch bijgewerkt met een verkoopprijs van 0 USD.
1. De nieuwe verkoopprijs van de regel wordt gesynchroniseerd met Verkoop.
1. Het resultaat is een orderregel in Verkoop met een verkoopprijs van 0 USD.

## <a name="example-scenario-2-trade-agreement-evaluation-with-the-manual-entry-option"></a>Voorbeeldscenario 2: Evaluatie van handelsovereenkomst met de optie Handmatige invoer

In dit scenario is het beleid voor **Handmatige invoer** *wel* aanwezig is in de Supply Chain Management-instellingen voor **Evaluatie van handelsovereenkomst**. Een verkoopgebruiker voert in Verkoop een orderregel in met een verkoopprijs die niet nul is. Supply Chain Management bevat een handelsovereenkomst die de verkoopprijs van 2 USD instelt voor het bestelde artikel.

1. In Verkoop maakt een gebruiker een orderregel voor een artikel met een waarde voor **Prijs per eenheid** van 1 USD.
1. De orderregel wordt gesynchroniseerd met Supply Chain Management met een verkoopprijs van 1 USD.
1. In Verkoop selecteert de gebruiker **Prijsorder** in het actievenster.
1. Aangezien de instellingen voor **Evaluatie van handelsovereenkomst** in Supply Chain Management het beleid **Handmatige invoer** bevatten, wordt de verkoopprijs niet gewijzigd, zelfs als een toepasselijke handelsovereenkomst een andere verkoopprijs aangeeft.
1. De verkoopprijs blijft ongewijzigd in Verkoop en in Supply Chain Management.

## <a name="example-scenario-3-trade-agreement-evaluation-for-an-item-that-has-a-sales-price-of-zero-in-sales"></a>Voorbeeldscenario 3: Beoordeling van handelsovereenkomst voor een artikel met een verkoopprijs van nul in Verkoop

In dit scenario is het beleid voor **Handmatige invoer** *wel* aanwezig is in de Supply Chain Management-instellingen voor **Evaluatie van handelsovereenkomst**. Een verkoopgebruiker voert in Verkoop een orderregel in met een verkoopprijs van 0 (nul) is. Supply Chain Management bevat een handelsovereenkomst die de verkoopprijs van 2 USD instelt voor een besteld artikel.

1. In Verkoop maakt een gebruiker een orderregel met de waarde **Prijs per eenheid** van 0 USD en een waarde voor **Regelkorting** van 0 USD.
1. De orderregel wordt gesynchroniseerd met Supply Chain Management met een verkoopprijs van 0 USD.
1. Omdat een orderregel wordt ontvangen met een verkoopprijs van 0 (nul), wordt de prijsengine van Supply Chain Management aanroepen, ook al is de optie **Handmatige invoer** ingeschakeld. De prijsengine retourneert de verkoopprijs van 2 USD die is vastgelegd door de handelsovereenkomst en werkt de orderregel in Supply Chain Management bij.
1. De bijgewerkte verkoopprijs is nog niet gesynchroniseerd met de orderregel in Verkoop.
1. In Verkoop selecteert de gebruiker **Prijsorder** in het actievenster.
1. De orderregel in Supply Chain Management behoudt de verkoopprijs van 2 USD, die nu wordt gesynchroniseerd met Verkoop. Daarom wordt de waarde van **Prijs per eenheid** van de orderregel in Verkoop bijgewerkt van 0 USD naar 2 USD.
1. In Verkoop voert de gebruiker een nieuwe waarde voor **Regelkorting** in van een 0,50 USD. Bij Verkoop wordt nu berekend dat de waarde voor **Uitgebreid bedrag** voor de regel 1,50 USD is.
1. De orderregel wordt gesynchroniseerd met Supply Chain Management met een waarde voor **Regelkorting** van 0,50 USD.
1. In Verkoop selecteert de gebruiker **Prijsorder** in het actievenster.
1. Er worden geen prijzen of kortingen gewijzigd voor de orderregel in Verkoop.

## <a name="limitations"></a>Beperkingen

Wanneer de kolommen in Sales zijn ingevuld, gelden de volgende beperkingen:

- De instellingen van toeslagen en toeslagtoewijzingen in Supply Chain Management worden niet in Sales gerepliceerd.
- Voor prijzen wordt geen rekening gehouden met speciale adviesprijzen die zijn opgegeven in de kolom **Detailhandelafzetkanaal** op de pagina Verkooporderregel in Supply Chain Management.
- Kortingen die zijn gedefinieerd in de sectie **Beheer van handelstoeslag** van Supply Chain Management worden niet meegenomen.
- Bij de prijsbepaling wordt geen rekening gehouden met verkoopovereenkomsten.

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
