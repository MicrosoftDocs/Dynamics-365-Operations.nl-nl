---
title: Op verzoek synchroniseren met de Supply Chain Management-prijsengine
description: In dit onderwerp wordt beschreven hoe u de prijsengine in Microsoft Dynamics 365 Supply Chain Management gebruikt vanuit Dynamics 365 Sales.
author: RamaKrishnamoorthy
ms.date: 03/10/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-10
ms.openlocfilehash: bf4154816f01040a236dde77b92ee69396158614
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/31/2021
ms.locfileid: "5750759"
---
# <a name="sync-on-demand-with-the-supply-chain-management-pricing-engine"></a>Op verzoek synchroniseren met de Supply Chain Management-prijsengine

[!include [banner](../../includes/banner.md)]



Microsoft Dynamics 365 Supply Chain Management bevat een prijsengine waarmee handelsovereenkomsten, prijslijsten, klantloyaliteitsprogramma's, promoties en kortingen worden afgehandeld. De prijsengine gebruikt complexe regels om de beste prijs voor een bepaalde offerte of order te bepalen. Wanneer u Twee keer wegschrijven gebruikt, gebruikt u statische prijzen of de prijsengine van Dynamics 365 Supply Chain Management op de offerte- en orderpagina's in Dynamics 365 Sales.

## <a name="use-the-pricing-engine-from-supply-chain-management-in-sales"></a>De prijsengine uit Supply Chain Management in Sales gebruiken

1. Ga in Sales naar **Verkoop \> Orders**.
2. Selecteer **Nieuw** om een nieuwe order te maken of selecteer een bestaande order in de lijst **Mijn orders**.
3. Voeg een nieuwe orderregel toe.
4. Als u een nieuwe order maakt, selecteert u **Prijsorder** in het actievenster. Als u een bestaande order bijwerkt, selecteert u **Opnieuw berekenen** in het actievenster.

    De volgende kolommen worden automatisch ingevuld:

    + Detailbedrag
    + Kortingspercentage
    + Korting
    + Bedrag vóór vracht
    + Vrachtkosten
    + Totaal belasting
    + Totaalbedrag
    
5. Om ervoor te zorgen dat het systeem handel- en verkoopovereenkomsten meeneemt bij het berekenen van de prijs:
    1. Ga naar uw Supply Chain Management-omgeving.
    2. Navigeer naar **Klanten \> Instellen \> Parameters van Klanten**.
    3. Selecteer het tabblad **Prijzen** op de navigatiebalk aan de zijkant.
    4. Schakel de optie **Handmatige invoer** uit op het sneltabblad **Evaluatie van handelsovereenkomst**.

## <a name="how-it-works"></a>Hoe het werkt

Wanneer u **Prijsorder** selecteert in Sales, wordt de functie **Totalen** op het tabblad **Verkooporder \> Weergeven** in Supply Chain Management aangeroepen voor de bijbehorende verkooporder. De waarden in het ordertotaal in Sales worden gebruikt om de overeenkomende kolommen in Supply Chain Management in te vullen.

Wanneer het verkoopordertotaal wordt berekend in Supply Chain Management, worden de bestaande handelsovereenkomsten en verkoopovereenkomsten voor de klant en de producten in de verkooporder geëvalueerd. Deze informatie wordt gebruikt om de totalen te berekenen. Wanneer **Prijsorder** is geselecteerd, worden in Sales automatisch alle instellingen weergegeven die zijn geconfigureerd in Supply Chain Management.

## <a name="limitations"></a>Beperkingen

Wanneer de kolommen in Sales zijn ingevuld, gelden de volgende beperkingen:

+ De instellingen van toeslagen en toeslagtoewijzingen in Supply Chain Management worden niet in Sales gerepliceerd.
+ Voor prijzen wordt geen rekening gehouden met speciale adviesprijzen die zijn opgegeven in de kolom **Detailhandelafzetkanaal** op de pagina Verkooporderregel in Supply Chain Management.
+ Kortingen die zijn gedefinieerd in de sectie **Beheer van handelstoeslag** van Supply Chain Management worden niet meegenomen.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]