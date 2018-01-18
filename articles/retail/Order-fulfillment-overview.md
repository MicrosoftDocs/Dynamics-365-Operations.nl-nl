---
title: Overzicht van winkelorderafhandeling
description: Dit onderwerp bevat een overzicht van de afhandeling van orders in winkels.
author: rubencdelgado
manager: AnnBe
ms.date: 10/30/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-retail
ms.technology: 
ms.search.form: RetailStoreTable, RetailTillLayout
audience: Application User
ms.search.scope: 
ms.search.region: Global
ms.author: rubencdelgado
ms.search.validFrom: 2017-10-30
ms.dyn365.ops.version: 
ms.translationtype: HT
ms.sourcegitcommit: ec6cb212766dd90fa9db7719a2119419ecb935c7
ms.openlocfilehash: e0aa0e576f88fd497472aa4141704a66d51605c3
ms.contentlocale: nl-nl
ms.lasthandoff: 12/20/2017

---

# <a name="store-order-fulfillment"></a>Winkelorderafhandeling

Veel detailhandelaren willen de afhandeling van orders optimaliseren door winkels in staat te stellen orders uit te voeren. Orderafhandeling op winkelniveau kan overbevoorradingsscenario's voor een bepaalde winkel voorkomen of vanuit logistiek oogpunt noodzakelijk zijn in gevallen waarin een winkel extra capaciteit heeft of zich dichter bij de klant bevindt. Om in deze behoefte te voorzien, is er een uniforme orderafhandelingsbewerking beschikbaar in het verkooppunt.

In orders voor afhandeling bij een bepaalde winkel is het magazijn van de winkel opgegeven in de orderkop of -regels. 

De orderafhandelingsbewerking in het verkooppunt biedt één werkgebied in het verkooppunt dat kan worden gebruikt voor het verwerken van orders. Dit omvat alles van het accepteren van de order tot het markeren van de order als verzonden of het initiëren van het ophalen in de winkel. 

## <a name="access-unified-order-fulfillment-in-the-point-of-sale"></a>Toegang tot uniforme orderafhandeling in het verkooppunt

Orderafhandeling, [bewerkings-id 928](https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/pos-operations), kan worden gebruikt om toegang te krijgen tot het werkgebied voor winkelorderafhandeling in het verkooppunt. 

Voor de orderafhandelingsbewerking bestaat geen eigen standaardmachtiging, maar in de toekomst kunnen gebruikers de machtiging **Order ophalen toestaan** gebruiken om de bewerking aan te roepen vanuit het verkooppunt.

Op het winkelniveau is een configuratie-instelling beschikbaar om te bepalen of een orderregel handmatig moet worden geaccepteerd vanuit het verkooppunt. Als deze configuratieoptie niet is ingesteld, worden orderregels standaard geaccepteerd. Als deze configuratieoptie is ingeschakeld, moeten gebruikers bij het verkooppunt de machtiging **Order accepteren toestaan** selecteren om orders vanuit het verkooppunt te accepteren.
Orderregels kunnen ook vanuit het verkooppunt worden afgewezen. Als een orderregel wordt afgewezen, betekent dit dat deze niet wordt afgehandeld in die winkel en naar een andere winkel of een ander magazijn wordt gestuurd om opnieuw te worden toegewezen. Toestemming voor het afwijzen van orderregels wordt verleend met de machtiging **Order afwijzen toestaan**. 

## <a name="order-fulfillment-operation-parameters"></a>Parameters voor de bewerking Orderafhandeling

Orderafhandeling biedt out-of-the-box-parameters die op de bewerking kunnen worden toegepast wanneer deze wordt aangeroepen in het verkooppunt. Wanneer de parameter **Alle orders** is geconfigureerd, worden alle orders weergegeven wanneer de bewerking wordt gebruikt. Met de parameter **Te verzenden orders** worden alleen orders weergegeven die moeten worden verzonden vanuit de winkel. Met **Orders voor afhalen** worden de orders weergegeven die in de winkel worden opgehaald. 

## <a name="orders-for-fulfillment"></a>Orders voor afhandeling

Met de bewerking Orderafhandeling worden alleen orders weergegeven die worden opgehaald in of verzonden uit de huidige winkel. Orders die door andere winkels worden afgehandeld, worden niet weergegeven wanneer u de bewerking Orderafhandeling gebruikt. 

## <a name="line-selection"></a>Regelselectie

Regels kunnen worden geselecteerd met de functie **Selecteren** in het actievenster. Wanneer **Selecteren** is ingeschakeld, kunnen meerdere regels worden geselecteerd voor verwerking. U kunt de selectie van een regel ongedaan maken door nogmaals op de regel te klikken. 

## <a name="line-details"></a>Regeldetails

Regeldetails kunnen worden weergegeven via het fly-outmenu voor regeldetails. Wanneer u dit menu gebruikt, worden er twee tabbladen met aanvullende informatie over de geselecteerde regel weergegeven. Het eerste tabblad, **Regeldetails**, bevat informatie over de regel zelf, zoals de bestelde en de resterende hoeveelheid. Daarnaast vindt u hier informatie over verzamelde, verpakte en gefactureerde aantallen en de leveringsmethode en het afleveradres. Het tabblad **Orderdetails** bevat gegevens uit de orderkoptekst, zoals de klant, de klant-id, het ordernummer, het ordertotaal en het saldo.

Als er meerdere regels zijn geselecteerd, wordt in het fly-outmenu voor orderregeldetails alleen aangeven dat er meerdere regels zijn geselecteerd. Als u details wilt weergeven voor één regel, maakt u de selectie van de overige regels ongedaan. 

## <a name="pending-order-lines"></a>Orderregels in behandeling

Bij uniforme orderafhandeling kunnen orders ook handmatig worden geaccepteerd. Orders voor afhandeling in de winkel zijn standaard al geaccepteerd. Als bedrijfsprocessen echter voorschrijven dat een werknemer op het winkelniveau orders moet accepteren, kan handmatige acceptatie worden ingeschakeld op het niveau van de detailhandelwinkel. Als u orderacceptatie wilt inschakelen, gaat u naar **Detailhandel** > **Kanalen** > **Detailhandelwinkels** > **Alle detailhandelwinkels**. Open de gewenste winkel en ga op het tabblad **Algemeen** naar de subkop **Orderafhandeling**. Deze subkop biedt een optie **Handmatig accepteren** die standaard is ingesteld op **Nee**. Door deze optie in te stellen op **Ja** en de wijzigingen met de kanaaldatabase te synchroniseren, kunt u het acceptatieproces initialiseren voor orderregels.

Werknemers met de machtiging **Order accepteren toestaan** kunnen Orderafhandeling openen en regels voor acceptatie selecteren. Wanneer regels zijn geaccepteerd, wordt de status van **In behandeling** in **Geaccepteerd** gewijzigd en kan de rest van het orderafhandelingsproces worden voortgezet. Wanneer **Handmatig accepteren** is ingeschakeld, worden orders pas verwerkt als ze zijn geaccepteerd. 

Orders voor ophalen in de winkel hebben nooit de status **In behandeling**. Dit gebeurt om te voorkomen dat voor een klant in de winkel de orderregel niet kan worden verwerkt omdat een werknemer met de juiste bevoegdheid niet beschikbaar is.

## <a name="accepted-order-lines"></a>Geaccepteerde orderregels

Orders met de regelstatus **Geaccepteerd** kunnen de rest van het orderafhandelingsproces doorlopen in het verkooppunt. Nadat een order is geaccepteerd, kunnen eventuele resterende acties worden ondernomen met betrekking tot de orderregel. 

Een geaccepteerde orderregel kan bijvoorbeeld worden geselecteerd en vervolgens direct worden opgehaald zonder het proces voor verzameling en verpakking te hoeven doorlopen.

## <a name="line-actions"></a>Regelacties

### <a name="pick"></a>Orderverzamelen

De actiecategorie **Orderverzamelen** is beschikbaar om u te helpen bij het verzamelen van orderregels van planken. De actie Orderverzamelen kan alleen worden uitgevoerd voor orderregels die eerder zijn geaccepteerd. 

**Actie: Orderverzamelen**

- Resulterende POS-status: Orderverzamelen
- Resulterende status backoffice: Geen wijziging

Nadat een order is geaccepteerd, kunnen regels worden geselecteerd en gemarkeerd als **Orderverzamelen**. Door een regel als **Orderverzamelen** te markeren, kunt u aangeven dat de orderverzameling al wordt uitgevoerd voor een regel. Zo wordt voorkomen dat twee werknemers op hetzelfde moment dezelfde orderregels verzamelen.  

**Actie: Orderverzamellijst afdrukken**

- Resulterende status: Orderverzamelen
- Resulterende status backoffice: Geen wijziging

Orderverzamellijsten kunnen bij het verkooppunt worden afgedrukt om werknemers te ondersteunen tijdens het orderverzamelproces. Een afgedrukte orderverzamellijst kan door de werknemer verantwoordelijk voor het verzamelen van artikelen worden meegenomen en handmatig worden bijgewerkt tijdens het werk. 

De indeling van de orderverzamellijst wordt geconfigureerd in Dynamics 365 for Retail en toegevoegd aan het ontvangstbewijsprofiel. Zie voor meer informatie over het instellen van ontvangstbewijsprofielen [Ontvangstsjablonen en afdrukken](https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/receipt-templates-printing).

Als er regels zijn geselecteerd en er een orderverzamellijst is afgedrukt voor deze regels, worden deze automatisch bijgewerkt met de status **Orderverzameling**. 

**Actie: Markeren als opgenomen**

- Resulterende status: Opgenomen of gedeeltelijk verzameld
- Resulterende status backoffice: Opgenomen of gedeeltelijk verzameld

Nadat het fysieke orderverzamelproces is uitgevoerd, kunnen regels worden gemarkeerd als **Opgenomen**. Wanneer een regel wordt geselecteerd en gemarkeerd als **Opgenomen**, wordt de functie voor het bijwerken van de orderregel in Dynamics 365 for Retail in realtime aangeroepen. Nadat de regel is gemarkeerd als **Opgenomen** bij het verkooppunt, wordt de status in de backoffice ook bijgewerkt naar **Opgenomen** en wordt in voorraadtransacties aangeven dat de opgegeven hoeveelheid is afgetrokken van de totale hoeveelheid.

Wanneer orders na verloop van tijd zijn verwerkt, kunnen er gedeeltelijke hoeveelheden voor een bepaalde regel worden verwerkt. Als een regel is geselecteerd, de actie **Markeren als opgenomen** is ondernomen en de hoeveelheid groter dan 1 is, wordt de gebruiker gevraagd naar de hoeveelheid. De resterende hoeveelheid die moet worden verzameld, wordt dan automatisch ingevuld. Als minder dan de resterende hoeveelheid wordt opgegeven, wordt de status van de regel **Gedeeltelijk verzameld**. Wanneer de orderregel wordt bijgewerkt in de backoffice, is hierin ook de status Gedeeltelijk verzameld verwerkt. De door de gebruiker ingevoerde hoeveelheid word gebruikt voor de voorraadupdate. 

Als een orderregel ten onrechte wordt opgenomen, moet het proces voor het ongedaan maken van de opname voor de orderregel worden uitgevoerd in de backoffice. Voor verkooppunten bestaan nog geen ondersteunde acties voor het ongedaan maken van een opname. 

Orderregels uit verschillende orders kunnen worden geselecteerd en gemarkeerd als **Orderverzamelen**, worden afgedrukt in dezelfde orderverzamellijst of worden gemarkeerd als **Opgenomen**. 

### <a name="pack"></a>Verpakking

Orderregels kunnen op elk moment worden verpakt nadat de orderregel is geaccepteerd. 

**Actie: Pakbon afdrukken**

- Resulterende status: Verpakt of gedeeltelijk verpakt
- Resulterende status backoffice: Geleverd of gedeeltelijk geleverd

Met deze actie worden regels gemarkeerd als gedeeltelijk verpakt en wordt een pakbon afgedrukt. Een pakbon kan worden afgedrukt voor het valideren van de producten die samen zijn verpakt. De indeling van de pakbon wordt geconfigureerd in Dynamics 365 for Retail en toegevoegd aan het ontvangstbewijsprofiel. Zie voor meer informatie over het instellen van ontvangstbewijsprofielen [Ontvangstsjablonen en afdrukken](https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/receipt-templates-printing).

**Actie: Markeren als verpakt**

- Resulterende status: Verpakt of gedeeltelijk verpakt
- Resulterende status backoffice: Geleverd of gedeeltelijk geleverd

De actie **Markeren als verpakt** kan worden gebruikt om aan te geven dat regels zijn verpakt zonder een pakbon af te drukken. Zowel **Pakbon afdrukken** als **Markeren als verpakt** resulteert in voorraadtransacties in de backoffice. Verpakkingsregels in het verkooppunt resulteren in het genereren van pakbonjournalen in de backoffice. 

Als een orderregel ten onrechte wordt verpakt, moet het pakbonjournaal worden gecorrigeerd in de backoffice. 

Alleen regels in dezelfde order en met dezelfde leveringsmethode kunnen op hetzelfde moment worden verpakt.

Op dit moment is de optie om regels voor ophalen in de winkel als **Verpakt** te markeren, uitgeschakeld. Deze functionaliteit wordt toegevoegd in een toekomstige versie. Het proces voor het maken van pakbonnen wordt verbeterd om de opname van verzendgegevens van derden in het pakbonproces te ondersteunen.

### <a name="pick-up"></a>Verzamelen

Orders voor afhalen in de winkel kunnen direct worden afgehaald wanneer ze zijn opgehaald in het verkooppunt. Orders voor afhalen in de winkel hoeven niet eerst te worden geaccepteerd. 

**Actie: Afhalen**

- Resulterende status: Gefactureerd of gedeeltelijk gefactureerd
- Resulterende status backoffice: Gefactureerd of gedeeltelijk gefactureerd

Als een regel is geselecteerd voor verzameling vanuit de uniforme orderafhandeling, wordt de hele order geladen in het verkooppunt en wordt de volledige hoeveelheid voor de geselecteerde regel gemarkeerd. Andere regels in de order worden ook in de transactieweergave van het verkooppunt geladen, maar met een hoeveelheid die is gemarkeerd als nul. 

Nadat de regels voor verzamelen in de transactieweergave zijn geladen, kan aan de transactie op de gebruikelijke wijze een betalingsmethode worden toegewezen. 

Regels die volledig zijn gefactureerd bij verzameling worden niet meer weergegeven in de uniforme orderafhandeling. Regels die gedeeltelijk zijn verzameld, worden in de uniforme orderafhandeling weergegeven totdat deze volledig zijn verzameld. 

Als een regel ten onrechte wordt verzameld, moet er een retour worden uitgevoerd om de fout te corrigeren.  

Alleen regels in dezelfde order en met dezelfde leveringsmethode kunnen op hetzelfde moment worden verzameld. 

### <a name="shipping"></a>Verzenden

Orderregels die moeten worden verzonden vanuit de winkel kunnen worden verwerkt door middel van uniforme orderafhandeling met de actie **Verzenden**. Als op kanaalniveau handmatige orderregelacceptatie is geconfigureerd, moeten orders vóór verzending worden geaccepteerd. Als een order is geaccepteerd en de status **In behandeling** of een andere status heeft, kunnen regels worden verzonden. 

**Actie: Verzenden**

- Resulterende status: Gefactureerd of gedeeltelijk gefactureerd
- Resulterende status backoffice: Gefactureerd of gedeeltelijk gefactureerd

Regels die worden verzonden vanuit de uniforme orderafhandelingsbewerking, worden op dezelfde manier vanuit de backoffice gefactureerd als wanneer de order rechtstreeks vanuit de backoffice wordt gefactureerd. Regels die worden verzonden vanuit de uniforme orderafhandelingsbewerking, worden niet geladen in de transactieweergave en er vindt geen offerteproces plaats op het moment dat de regels worden verzonden. 

Orderregels die volledig zijn verzonden, worden niet meer weergegeven in een uniforme orderafhandeling. Regels die gedeeltelijk zijn verzonden, worden in de uniforme orderafhandeling weergegeven totdat deze volledig zijn verzonden. 

Alleen regels uit dezelfde order kunnen op hetzelfde moment worden verzonden. Als voor de regels uit dezelfde order verschillende leveringsmethoden zijn ingesteld, kunnen deze nog steeds worden geselecteerd voor gelijktijdige verzending. 

### <a name="reject"></a>Afwijzen

Regels of gedeeltelijke regels kunnen worden afgewezen. Op deze manier kunnen ze vanuit de backoffice opnieuw worden toegewezen aan een andere winkel of een ander magazijn. Regels kunnen alleen worden afgewezen als ze nog niet zijn verzameld of verpakt. Voor een regel die al is verzameld of verpakt, moet de verzameling of verpakking ongedaan worden gemaakt vanuit de backoffice. 

**Actie: Afwijzen**

- Resulterende status: Afgewezen
- Resulterende status backoffice: Geen wijziging 

De afgewezen orderregels kunnen worden weergegeven vanuit het werkgebied **Verkooporderverwerking en -onderzoek**. Wis het persoonsfilter voor het werkgebied om alle afgewezen orderregels in de winkels weer te geven. Op het tabblad **Afgewezen orderregels** onder **Orders en favorieten** worden de orderregeldetails weergeven. Daarnaast kunnen de gebruikers klikken op de knop **Afgewezen orderregels** onder **Overzicht** om te navigeren naar een verkooporderweergave. Hierin worden alle orders met een of meer afgewezen regels weergegeven. Als de functie voor het beheer van gedistribueerde orders is ingeschakeld, worden deze afgewezen orders automatisch opnieuw toegewezen aan de juiste winkels voor afhandeling, maar deze orderregels kunnen ook handmatig opnieuw worden toegewezen. Hiervoor selecteert u de regel waarvoor **Afhandelingsstatus** als **Afgewezen** wordt weergegeven en wijzigt u zo nodig de locatie of het magazijn. Klik op het vervolgkeuzemenu **Regel bijwerken** en vervolgens op **Uitvoeringsstatus opnieuw instellen** om de afhandelingsstatus van **Afgewezen** in **Geaccepteerd** of **In behandeling** te wijzigen, afhankelijk van de ingestelde orderafhandeling. Als de afhandelingsstatus opnieuw is ingesteld, kunnen de werknemers van de winkel de orderregels weergeven in de POS-client.

## <a name="line-quantity-tracking"></a>Regelhoeveelheid traceren

Een orderregelhoeveelheid van meer dan één kan gedurende een periode worden verwerkt, wat resulteert in meerdere substatussen voor orderregels. Als een aannemer voor een project bijvoorbeeld 500 platen nodig heeft, maar slechts enkele platen per keer ophaalt of laat afleveren gedurende de looptijd van het project, kunnen er tegelijkertijd hoeveelheden worden verzameld, verpakt en verzonden. 

Elk keer dat een regel wordt geselecteerd, wordt de resterende hoeveelheid voor de regel automatisch ingevuld in de veronderstelling dat de resterende hoeveelheid nog wordt verwerkt. Als de aannemer in het bovenstaande voorbeeld al 200 platen heeft verzameld en de regel voor platen is geselecteerd voor verzameling, wordt de resterende hoeveelheid van 300 automatisch ingevuld als hoeveelheid. Ditzelfde geldt als er al 200 platen zijn gefactureerd. In dat geval wordt alleen de resterende hoeveelheid automatisch ingevuld. 

En als er 200 platen zijn gemarkeerd als verpakt en Verzending wordt geselecteerd, wordt de volledige hoeveelheid van 500 automatisch ingevuld. Als slechts platen zijn verzonden, gaat het systeem ervan uit dat de eerder verpakte platen worden verzonden en wordt de verpakte hoeveelheid verlaagd. Als er 201 platen zijn verzonden, wordt eerst het aantal verpakte platen verlaagd en wordt vervolgens die ene resterende plaat afgetrokken van de resterende hoeveelheid. 

## <a name="line-statuses"></a>Regelstatussen

Orderregels in het verkooppunt hebben verschillende statussen om de status van de orderregel aan te geven. De statussen in het verkooppunt en de backoffice komen niet in alle gevallen overeen. De orderregelstatus kan via het verkooppunt worden weergegeven met de orderafhandelingsbewerkingen. In de backoffice kunnen orderregels worden weergegeven vanuit de orderdetails. Orderdetails zijn toegankelijk zijn via **Detailhandel** > **Klanten** > **Alle klantorders**. Selecteer de **order-id** om de orderdetails te bekijken. Selecteer vanuit de orderdetails het tabblad **Verkooporder** en selecteer vervolgens **Gedetailleerde status** onder de subkop **Weergave**. 

**In behandeling**: orderregels die zijn toegewezen aan een winkel, maar nog niet zijn geaccepteerd, hebben de status **In behandeling** wanneer ze worden weergegeven bij het verkooppunt. Regels in afwachting van goedkeuring in het verkooppunt hebben de status **Orderverwerking** in de backoffice.

**Geaccepteerd**: orderregels die handmatig of automatisch zijn geaccepteerd, hebben de status **Geaccepteerd** wanneer deze worden weergegeven bij het verkooppunt. Regels met de status **Geaccepteerd** worden weergegeven als **Orderverwerking** in de backoffice.

**Orderverzameling**: regels die momenteel worden verzameld op winkelniveau hebben de status **Orderverzameling**. Dezelfde regels worden in de backoffice weergegeven als **Orderverwerking**.

**Verzameld** en **Gedeeltelijk verzameld**: regels die zijn verzameld of gedeeltelijk zijn verzameld bij het verkooppunt krijgen de status **Verzameld** of **Gedeeltelijk verzameld**. Dezelfde regels worden in de backoffice ook weergegeven als **Verzameld** of **Gedeeltelijk verzameld**.

**Verpakt** en **Gedeeltelijk verpakt**: regels die zijn verpakt of gedeeltelijk zijn verpakt bij het verkooppunt krijgen de status **Verpakt** of **Gedeeltelijk verpakt**. Dezelfde regels worden in de backoffice ook weergegeven als **Geleverd** of **Gedeeltelijk geleverd**.

**Gedeeltelijk gefactureerd**: regels die gedeeltelijk zijn verzameld of gedeeltelijk zijn verzonden, krijgen de status **Gedeeltelijk gefactureerd** bij het verkooppunt en in de backoffice.

**Gefactureerd**: regels die volledig zijn gefactureerd bij het verkooppunt worden niet meer weergegeven voor afhandeling. In de backoffice is de status voor deze regels **Gefactureerd**.

## <a name="order-fulfillment-filtering"></a>Filteren van orderafhandeling

Orderafhandeling in het verkooppunt omvat allerlei filters, zodat gebruikers gemakkelijk vinden wat ze nodig hebben. Filters kunnen via het actievenster onder in het scherm **Verkooppunt** worden gewijzigd. Standaard wordt een filter **Leveringstype** toegepast, afhankelijk van hoe de bewerking is ingesteld. Als de bewerking is ingesteld met de parameter **Alle orders**, wordt dit filter toegepast bij het openen van Orderafhandeling. Hetzelfde geldt voor de parameters **Ophalen in de winkel** en **Verzenden uit winkel**. Andere filters die kunnen worden toegepast op de weergave Orderafhandeling zijn onder andere:

  - Klantnummer
  - Klantnaam
  - E-mail klant
  - Ordernummer
  - Leveringsmethode
  - Ontvangstbewijsnummer
  - Afzetkanaalverwijzings-ID
  - Oorspronkelijk winkelnummer
  - Regelstatus
  - Gemaakt op
  - Leveringsdatum
  - Ontvangstdatum

