---
title: Kaspositie
description: In dit artikel wordt beschreven hoe u met de functie voor cashflowprognoses de kaspositie van een organisatie voor bepaalde tijdstippen kunt voorspellen. Ook worden de opties beschreven die beschikbaar zijn voor het weergeven van prognoses voor verschillende perioden.
author: ShivamPandey-msft
ms.date: 12/21/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2019-11-06
ms.dyn365.ops.version: AX 10.0.8
ms.openlocfilehash: 7581142348d91b3a37cc75cf801e7bfc098cd604
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8870244"
---
# <a name="cash-position"></a>Kaspositie

[!include [banner](../includes/banner.md)]

Kaspositie is de projectie van de cashflowprognose voor de korte termijn. Dit is gebaseerd op de projectie van contante ontvangsten van klanten die openstaande facturen en orders betalen, en ook op de prognoses voor contante betalingen aan leveranciers voor inkoopfacturen en orders.

Bij het voorspellen van de betalingen van klanten, worden de voorspellingsmodellen voor klantbetalingen gebruikt. Zonder betalingsvoorspellingen wordt de gemiddelde tijd die voor elke klant nodig is om een klantfactuur te converteren naar een betaling, gebruikt om een betalingsdatum te berekenen. Voor openstaande klantorders wordt de factuurdatum berekend op basis van het gemiddelde aantal dagen voor de orderregels die per klant moeten worden gefactureerd. Vervolgens wordt de factuurdatum als invoer gebruikt voor de functionaliteit voor betalingsvoorspelling. Met de functionaliteit voor het voorspellen van klantbetalingen wordt een betalingsdatum voor elke orderregel berekend. 

De betalingsdatum voor openstaande facturen wordt geraamd op basis van de betalingsvoorspellingen door een datum te selecteren die overeenkomt met het vijftigste percentiel van de cumulatieve verdelingsfunctie die uit de waarschijnlijkheid van de voorspelling van de bucket wordt verkregen.

Een vergelijkbare aanpak wordt gebruikt om betalingen aan leveranciers te voorspellen. Het systeem berekent voor elke leverancier de gemiddelde tijd die nodig is om een leveranciersfactuur om te rekenen naar een betaling. Dat aantal dagen wordt vervolgens gebruikt om de betalingsdatum te berekenen. Voor openstaande leveranciersorders wordt de factuurdatum berekend door het gemiddelde aantal dagen te nemen dat is vereist om orderregels te converteren naar een factuur voor elke leverancier. Het systeem berekent vervolgens de betalingsdatum door voor elke leverancier de gemiddelde tijd te nemen die nodig is om een leveranciersfactuur om te rekenen naar een betaling.

Het bovenste gedeelte van het tabblad **Kaspositie** bevat een kaspositiediagram. Dit diagram toont de contante inkomsten en uitgaven en de invloed hiervan op het totale liquiditeitssaldo. De details in het kaspositiediagram kunnen worden weergegeven in dagelijkse, wekelijkse, maandelijkse of driemaandelijkse perioden. Wanneer u **Dagelijks** selecteert, kunt u prognoses voor de volgende 21 dagen weergeven. Wanneer u **Wekelijks** selecteert, kunt u prognoses voor de volgende 20 weken weergeven. Wanneer u **Maandelijks** selecteert, kunt u prognoses voor de volgende 12 maanden weergeven. Wanneer u **Per kwartaal** selecteert, kunt u prognoses voor de volgende 12 kwartalen weergeven. U kunt de grafiek verbergen als u extra ruimte op het scherm nodig hebt om inhoud weer te geven op het tabblad **Kaspositie**.

In het onderste gedeelte van het tabblad **Kaspositie** worden details weergegeven voor de positie, cashflow, verwachte betalingen en bankrekening.

- De informatie in het raster **Positiedetails** wordt weergegeven in drie secties: een lijst met liquiditeitsrekeningen, een lijst met documenten met kasinkomsten en een lijst met documenten met kasuitgaven. Het raster toont ook de kaspositiesaldi. Voor de eerste periode die u bekijkt, is het saldo voor de liquiditeitsrekeningen het beginsaldo. Voor volgende perioden worden de saldi voor de liquiditeitsrekeningen berekend op basis van het toevoegen van kasinkomsten en het aftrekken van kasuitgaven uit vorige perioden. Selecteer de koppeling **Saldo** als u details wilt weergeven van de transacties die in de berekening van het saldo zijn opgenomen.
- In het raster **Cashflow** worden de kasinkomsten en -uitgaven per periode samengevoegd en de invloed op de saldi van de liquiditeitsrekeningen weergegeven. Voor de eerste periode is het saldo voor de liquiditeitsrekeningen het beginsaldo. Voor volgende perioden worden de saldi voor de liquiditeitsrekeningen berekend op basis van het toevoegen van kasinkomsten en het aftrekken van kasuitgaven uit vorige perioden.
- Het raster **Verwacht banksaldo** toont de verwachte kasuitgaven en hun invloed op liquiditeitsrekeningen.
- Het raster **Bankrekening** toont het effect van de verwachte kasinkomsten en -uitgaven op het banksaldo.

Maak een momentopname om de contante positie op te slaan en te bewerken. Zie voor meer informatie over hoe u werkt met momentopnamen [Overzicht van momentopnamen](payment-snapshots.md).

## <a name="details-of-the-cash-position-capability"></a>Details van de functie Kaspositie 

De functie Kaspositie bevat de volgende voorzieningen. 

- Met de functie Kaspositie wordt de cashflow weergegeven op basis van bestaande documenten in het systeem en aan de hand van kasinkomsten- en kasuitgavenregels die vanuit externe systemen zijn geïmporteerd.
- U kunt de cashflowgegevens van externe systemen eenvoudig integreren in Dynamics 365 Finance. Kaspositie kunnen ook gebruikmaken van het raamwerk voor importeren/exporteren van gegevens. Met dit raamwerk is integratie in Excel OData eenvoudig. U kunt ook gegevens uit meerdere bronnen combineren om een allesomvattende oplossing voor de kaspositie te creëren.
- Introduceert een intelligente kaspositie. De kaspositie wordt opgesteld op basis van het betalingsgedrag van de klant om te voorspellen wanneer een bedrijf kan verwachten dat contant geld op hun rekening beschikbaar is.
- Voor klantorders en facturen wordt de AI-functionaliteit voor de voorspelling van klantbetalingen gebruikt om het historische betalingsgedrag van klanten vast te stellen wanneer een order of factuur wordt betaald.
- Voor leveranciersorders en facturen gebruiken we de gemiddelde tijd tussen verzending en factuur en het betalen van een factuur per leverancier om te bepalen wanneer een leveranciersorder of factuur wordt betaald waardoor de kasuitgavenstromen nauwkeuriger worden.

Hierdoor wordt een nauwkeurigere weergave van de cashflow gemaakt op basis van het historische betalingsgedrag voor de financieel beheerder. 

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
