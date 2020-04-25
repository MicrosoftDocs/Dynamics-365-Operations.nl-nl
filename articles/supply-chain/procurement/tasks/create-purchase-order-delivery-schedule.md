---
title: Een inkooporder maken met een afleveringsschema
description: Dit onderwerp laat zien hoe u een afleveringsschema voor een inkooporder kunt maken.
author: mkirknel
manager: tfehr
ms.date: 08/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchCreateOrder, InventItemIdLookupPurchase, PurchDeliverySchedule, PurchEditLines
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e16c9adf592282a941b1112e197ea1ce9bdd34f2
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/02/2020
ms.locfileid: "3207710"
---
# <a name="create-a-purchase-order-with-a-delivery-schedule"></a>Een inkooporder maken met een afleveringsschema

[!include [banner](../../includes/banner.md)]

Dit onderwerp laat zien hoe u een afleveringsschema voor een inkooporder kunt maken. Een afleveringsschema wordt gebruikt wanneer wordt gevraagd een hoeveelheid op een order of journaal in meerdere zendingen te leveren. Het voorbeeld dat in deze handleiding wordt weergegeven, kan worden gebruikt in het USMF-demobedrijf. Deze procdure wordt gewoonlijk uitgevoerd door een inkoper.

## <a name="create-a-delivery-schedule"></a>Een afleveringsschema maken
1. Ga in het navigatievenster naar **Modules > Inkoopbeheer > Inkooporders > Alle inkooporders**.
2. Selecteer **Nieuw** in het actievenster.
3. Typ `US-101` in het veld **Leveranciersrekening**.
4. Selecteer **OK**.
5. Typ `M0001` in het veld **Artikelnummer**.
6. Typ `10` in het veld **Hoeveelheid**.
7. Selecteer **Inkooporderregel**.
8. Selecteer **Afleveringsschema**.
- Op de pagina **Afleveringsschema** kunt u het aantal zendingen opgeven waarin de totale hoeveelheid van de orderregel van de leverancier wordt geleverd.  
- Standaard kopieert het systeem de totale hoeveelheid en andere leveringsdetails van de oorspronkelijke inkoopregel in de eerste afleveringsschemaregel. In dit voorbeeld wordt er een planning voor twee zendingen gemaakt, met de datum van de tweede zending een week later dan de eerste.  
9. Wijzig in het veld **Hoeveelheid** het aantal in `4`.
10. Selecteer **Nieuw**.
11. Typ `6` in het veld **Hoeveelheid** als resterende hoeveelheid.
- Selecteer in het veld Leveringsdatum een datum één week na de datum op de eerste leveringsregel.  
- U kunt bijhouden welke totale hoeveelheid is toegewezen aan de afleveringsschemaregels door te kijken naar de velden **Totaal** en **Resterend**. Als de resterende hoeveelheid nul is, is de volledige hoeveelheid van de oorspronkelijke regel toegewezen aan het schema.  
12. Vouw de sectie **Omrekening van toeslagen** uit.
- Met de opties hier kunt u bepalen hoe u kosten wilt verdelen over de afleveringsschemaregels. Als u **Brutobedragen kopiëren** selecteert, wordt het toeslagbedrag op de oorspronkelijke orderregel gekopieerd naar elke leveringsregel. Met de optie **Toewijzen aan afleveringsregels** wordt de oorspronkelijke regeltoeslag verdeeld op basis van de hoeveelheid op elke leveringsregel.  
13. Vouw de sectie **Omrekening van toeslagen** samen.
14. Selecteer **OK**.
- Het afleveringsschema is nu toegepast op de order.  
- De oorspronkelijke orderregel, die nu de commerciële regel wordt genoemd, is omgezet in een orderregel met meerdere leveringen. De regel is gemarkeerd met een specifiek pictogram en dient als de kop voor de leveringsregels.  
15. Selecteer de tweede orderregel. Dit is de eerste van de twee leveringsregels.
- De twee nieuwe regels, die leveringsregels worden genoemd, vormen één afleveringsschema. De order wordt met deze regels en niet de oorspronkelijke regel verwerkt. Als documenten zoals bevestigingen, productontvangstjournalen of facturen worden afgedrukt, worden alleen de leveringsregels weergegeven.  

## <a name="change-the-delivery-schedule"></a>Het afleveringsschema wijzigen
U kunt de hoeveelheid op leveringsregels wijzigen. Als u dit doet, wordt de commerciële regel automatisch bijgewerkt tot de totale hoeveelheid in de leveringsregels.  
1. Wijzig in het veld **Hoeveelheid** van de eerste leveringsregel de hoeveelheid van `4` in `5`.
2. Selecteer de eerste orderregel (de commerciële regel).  
- De hoeveelheid op de commerciële regel is gewijzigd in 11.  

## <a name="process-product-receipt-using-delivery-schedules"></a>Productontvangst verwerken met afleveringsschema's
De inkooporder moet worden bevestigd voordat de productontvangst kan worden verwerkt. In dit voorbeeld wordt de ontvangst direct in de inkooporder vastgelegd. De ontvangst kan ook worden geregistreerd bij aankomst van de goederen in het magazijn.  
1. Selecteer in het actievenster de optie **Inkoop**.
2. Selecteer **Bevestigen**.
3. Selecteer **Ontvangen** in het actievenster.
4. Selecteer **Productontvangstbon**. Typ een willekeurige waarde in het veld **Productontvangstbon**.
- Dit veld wordt gebruikt om een verwijzing in te voeren die als het boekstuk voor productontvangstbonjournaal wordt gebruikt.  
- Selecteer in het veld **Hoeveelheid** de optie **Bestelde hoeveelheid**. Deze optie betekent dat de ontvangst wordt verwerkt voor de hoeveelheid waarmee de orderregels zijn gemaakt.  
- Controleer of het veld **Productontvangstbon afdrukken** is ingesteld op **Nee**. Afdrukken is niet nodig in dit voorbeeld.  
5. Vouw de sectie **Regels** uit.
- Merk op hoe de productontvangstbon wordt gemaakt voor de twee leveringsregels en niet voor de oorspronkelijke orderregel. Als de ontvangst is geregistreerd in het magazijn, kan deze ook worden geregistreerd op de afleveringsschemaregels.  
6. Vouw de sectie **Regels** samen.
7. Selecteer **OK** om de ontvangst te boeken.

