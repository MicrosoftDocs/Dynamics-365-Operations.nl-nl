---
title: Kaspositie
description: In dit onderwerp wordt beschreven hoe u met de functie voor cashflowprognoses de kaspositie van een organisatie voor bepaalde tijdstippen kunt voorspellen. Ook worden de opties beschreven die beschikbaar zijn voor het weergeven van prognoses voor verschillende perioden.
author: ShivamPandey-msft
ms.date: 11/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2019-11-06
ms.dyn365.ops.version: AX 10.0.8
ms.openlocfilehash: bf99ce5c9de00061cba2f49d00cc9dbc728753a8
ms.sourcegitcommit: 03fa7556840aa59f825697f6f9edeb58ea673fca
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/04/2021
ms.locfileid: "7752875"
---
# <a name="cash-position"></a>Kaspositie

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

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

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
