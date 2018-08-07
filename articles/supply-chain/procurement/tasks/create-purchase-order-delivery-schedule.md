--- 
title: Een inkooporder maken met een afleveringsschema
description: Deze procedure laat zien hoe u een afleveringsschema voor een inkooporder kunt maken.
author: FrankDahl
manager: AnnBe
ms.date: 08/23/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: fdahl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 1e4a0204d74c8966cd90b52ae13c88e222ebc3ef
ms.contentlocale: nl-nl
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-purchase-order-with-a-delivery-schedule"></a>Een inkooporder maken met een afleveringsschema

[!include [task guide banner](../../includes/task-guide-banner.md)]

Deze procedure laat zien hoe u een afleveringsschema voor een inkooporder kunt maken. Een afleveringsschema wordt gebruikt wanneer wordt gevraagd een hoeveelheid op een order of journaal in meerdere zendingen te leveren. Het voorbeeld dat in deze handleiding wordt weergegeven, kan worden gebruikt in het USMF-demobedrijf. Deze procdure wordt gewoonlijk uitgevoerd door een inkoper.


## <a name="create-a-delivery-schedule"></a>Een afleveringsschema maken
1. Ga naar Inkoop en sourcing > Inkooporders > Alle inkooporders.
2. Klik op Nieuw.
3. Typ in het veld Leveranciersrekening de waarde US-101.
4. Klik op OK.
5. Voer M0001 in het veld Artikelnummer in.
6. Typ 10 in het veld Hoeveelheid.
7. Klik op Inkooporderregel.
8. Klik op Afleveringsschema.
    * Op de pagina Afleveringsschema kunt u het aantal zendingen opgeven waarin de totale hoeveelheid van de orderregel van de leverancier wordt geleverd.  
    * Standaard kopieert het systeem de totale hoeveelheid en andere leveringsdetails van de oorspronkelijke inkoopregel in de eerste afleveringsschemaregel. In dit voorbeeld wordt er een planning voor twee zendingen gemaakt, met de datum van de tweede zending een week later dan de eerste.  
9. Wijzig de hoeveelheid in 4 in het veld Hoeveelheid.
10. Klik op Nieuw.
11. Typ 6 in het veld Hoeveelheid als resterende hoeveelheid.
    * Selecteer in het veld Leveringsdatum een datum één week na de datum op de eerste leveringsregel.  
    * U kunt bijhouden welke totale hoeveelheid is toegewezen aan de afleveringsschemaregels door te kijken naar de velden Totaal en Resterend. Als de resterende hoeveelheid nul is, is de volledige hoeveelheid van de oorspronkelijke regel toegewezen aan het schema.  
12. Vouw de sectie Omrekening van toeslagen uit.
    * Met de opties hier kunt u bepalen hoe u kosten wilt verdelen over de afleveringsschemaregels. Als u Brutobedragen kopiëren selecteert, wordt hetzelfde toeslagbedrag op de oorspronkelijke orderregel gekopieerd naar elke leveringsregel. Met de optie Toewijzen aan afleveringsregels wordt de oorspronkelijke regeltoeslag verdeeld op basis van de hoeveelheid op elke leveringsregel.  
13. Vouw de sectie Omrekening van toeslagen samen.
14. Klik op OK.
    * Het afleveringsschema is nu toegepast op de order.  
    * De oorspronkelijke orderregel, die nu de commerciële regel wordt genoemd, is omgezet in een orderregel met meerdere leveringen. De regel is gemarkeerd met een specifiek pictogram en dient als de kop voor de leveringsregels.  
15. Selecteer de tweede orderregel. Dit is de eerste van de twee leveringsregels.
    * De twee nieuwe regels, die leveringsregels worden genoemd, vormen één afleveringsschema. De order wordt met deze regels en niet de oorspronkelijke regel verwerkt. Als documenten zoals bevestigingen, productontvangstjournalen of facturen worden afgedrukt, worden alleen de leveringsregels weergegeven.  

## <a name="change-the-delivery-schedule"></a>Het afleveringsschema wijzigen
    * U kunt de hoeveelheid op leveringsregels wijzigen. Als u dit doet, wordt de commerciële regel automatisch bijgewerkt tot de totale hoeveelheid in de leveringsregels.  
1. Wijzig in het veld Hoeveelheid van de eerste leveringsregel de hoeveelheid van 4 in 5.
2. Selecteer de eerste orderregel (de commerciële regel).
    * De hoeveelheid op de commerciële regel is gewijzigd in 11.  

## <a name="process-product-receipt-using-delivery-schedules"></a>Productontvangst verwerken met afleveringsschema's
    * De inkooporder moet worden bevestigd voordat een productontvangst kan worden verwerkt. In dit voorbeeld wordt de ontvangst direct in de inkooporder vastgelegd. De ontvangst kan ook worden geregistreerd bij aankomst van de goederen in het magazijn.  
1. Klik in het actievenster op Inkoop.
2. Klik op Bevestigen.
3. Klik in het actievenster op Ontvangen.
4. Klik op Productontvangstbon.
5. Typ een willekeurige waarde in het veld Productontvangstbon.
    * Dit veld wordt gebruikt om een verwijzing in te voeren die als het boekstuk voor productontvangstbonjournaal wordt gebruikt.  
    * Selecteer in het Veld Hoeveelheid de optie 'Bestelde hoeveelheid'. Deze optie betekent dat de ontvangst wordt verwerkt voor de hoeveelheid waarmee de orderregels zijn gemaakt.  
    * Controleer of het veld Productontvangstbon afdrukken is ingesteld op Nee. Afdrukken is niet nodig in dit voorbeeld.  
6. Vouw de sectie Regels uit.
    * Merk op hoe de productontvangstbon wordt gemaakt voor de twee leveringsregels en niet voor de oorspronkelijke orderregel. Als de ontvangst is geregistreerd in het magazijn, kan deze ook worden geregistreerd op de afleveringsschemaregels.  
7. Vouw de sectie Regels samen.
8. Klik op OK om de ontvangst te boeken.


