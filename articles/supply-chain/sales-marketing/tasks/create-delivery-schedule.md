---
title: Afleveringsschema maken
description: Deze procedure toont hoe een afleveringsschema voor een verkooporder wordt gemaakt.
author: omulvad
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable, SalesDeliverySchedule, SalesEditLines,  SrsReportViewerForm
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: af983b30530a7f5d0a82f98deeb12180c42d86cd
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/02/2020
ms.locfileid: "3215810"
---
# <a name="create-delivery-schedule"></a>Afleveringsschema maken

[!include [banner](../../includes/banner.md)]

Deze procedure toont hoe een afleveringsschema voor een verkooporder wordt gemaakt. Een afleveringsschema wordt gebruikt wanneer een hoeveelheid op een order of offerte wordt gevraagd in meerdere zendingen te leveren. U kunt deze procedure uitvoeren in het demogegevensbedrijf USMF of met uw eigen gegevens.


## <a name="create-delivery-schedule"></a>Afleveringsschema maken
1. Ga naar Alle verkooporders.
2. Klik op Nieuw.
3. Typ of selecteer een waarde in het veld Klantrekening.
4. Klik op OK.
5. Typ of selecteer een waarde in het veld Artikelnummer.
6. Voer in het veld Hoeveelheid een aantal in dat groter is dan 1.
7. Klik op Verkooporderregel.
8. Klik op Afleveringsschema.
    * De pagina Afleveringsschema is de plaats waar u het aantal zendingen kunt opgeven waarin de totale hoeveelheid van de orderregel aan de klant wordt geleverd.    
    * Standaard kopieert het systeem de totale hoeveelheid en andere leveringsdetails van de oorspronkelijke verkoopregel in de eerste afleveringsschemaregel. In dit voorbeeld wordt er een planning voor twee zendingen gemaakt, met de datum van de tweede zending een week later dan de eerste.  
9. Voer in het veld Hoeveelheid een aantal in dat deel is van de totale hoeveelheid.
10. Klik op Nieuw.
11. Voer in het veld Hoeveelheid de resterende hoeveelheid in.
12. Voer in het veld Gewenste verzenddatum een datum in die één week verder is dan de datum van de eerste leveringsregel.
    * De twee opties op het sneltabblad Toeslagenconversie bepalen hoe u wilt dat de kosten worden verdeeld over de afleveringsschemaregels, zodra ze aan de oorspronkelijke orderregel zijn toegewezen. Als u Brutobedragen kopiëren selecteert, wordt hetzelfde toeslagbedrag gekopieerd naar elke regel. De optie Toewijzen aan afleveringsregels verdeelt de toeslagen gelijk over de leveringsregels.  
    * Alleen vaste toeslagen kunnen worden verdeeld, terwijl variabele toeslagen nog steeds naar de regels worden gekopieerd.  
13. Verplaats de cursor weg van de tweede leveringsregel om de pagina bijwerken.
    * U kunt bijhouden welke totale hoeveelheid is toegewezen aan de afleveringsschemaregels door te kijken naar de velden Totaal en Resterend. Als de resterende hoeveelheid nul is, is de volledige hoeveelheid van de oorspronkelijke regel toegewezen aan het schema.   
14. Klik op OK.
    * Het afleveringsschema is nu gekopieerd naar de orderregels.   
    * De oorspronkelijke orderregel, de commerciële regel genoemd, is omgezet in een orderregel met meerdere leveringen. Het is gemarkeerd met een ander pictogram en dient als de kop voor de leveringsregels.  
    * De twee nieuwe regels, die leveringsregels worden genoemd, vormen één afleveringsschema. De order wordt met deze regels en niet de oorspronkelijke regel verwerkt. Als documenten zoals bevestigingsbonnen, orderverzamellijsten, pakbonnen, of facturen worden afgedrukt, worden alleen de leveringsregels weergegeven.   
    * De leveringsregels kunnen verschillende leveringsdatums, hoeveelheden, leveringsmethoden en opslagdimensies, zoals locatie en magazijn, bevatten. De productdimensies moeten echter altijd overeenkomen met de productdimensies op de commerciële regel en kunnen niet worden gewijzigd.  
15. Voer in het veld Hoeveelheid een aantal in dat groter is dan het huidige aantal.
16. Selecteer de commerciële regel om het effect van de hoeveelheidsherberekening te bekijken.
17. Klik in het actievenster op Verzamelen en inpakken.
18. Klik op Pakbon boeken.
19. Vouw de sectie Parameters uit.
20. Selecteer in het veld Hoeveelheid de optie 'Alle'.
    * Merk op dat de pakbon voor de twee afleveringsschemaregels en niet de oorspronkelijke orderregel wordt gemaakt.  
21. Selecteer Ja in het veld Pakbon afdrukken.
22. Klik op OK.
23. Klik op Ja.
24. Sluit de pagina.

