---
title: Instelling van winkelafhandeling
description: Dit onderwerp bevat een overzicht van de wijze waarop u een winkelorderafhandeling instelt.
author: rubencdelgado
manager: AnnBe
ms.date: 10/30/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailStoreTable, RetailTillLayout
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.search.region: Global
ms.search.industry: retail
ms.author: rubencdelgado
ms.search.validFrom: 2017-10-30
ms.dyn365.ops.version: 
ms.translationtype: HT
ms.sourcegitcommit: 72d4ff5e1311005d3bf43a13e28208cd9b3d1457
ms.openlocfilehash: ccff6533257379c0305f7414dd36e17d1c323c21
ms.contentlocale: nl-nl
ms.lasthandoff: 03/07/2018

---


# <a name="set-up-order-fulfillment-for-stores"></a>Orderafhandeling voor winkels instellen

[!include[banner](includes/banner.md)]

## <a name="overview"></a>Overzicht
Veel detailhandelaren willen de afhandeling van orders optimaliseren door winkels in staat te stellen orders uit te voeren. Orderafhandeling op winkelniveau kan overbevoorradingsscenario's voor een bepaalde winkel voorkomen of vanuit logistiek oogpunt noodzakelijk zijn in gevallen waarin een winkel extra capaciteit heeft of zich dichter bij de klant bevindt. Om in deze behoefte te voorzien, is er een uniforme orderafhandelingsbewerking beschikbaar in het verkooppunt.

In orders voor afhandeling bij een bepaalde winkel is het magazijn van de winkel opgegeven in de orderkop of -regels. 

De orderafhandelingsbewerking in het verkooppunt biedt één werkgebied in het verkooppunt dat kan worden gebruikt voor het verwerken van orders. Dit omvat alles van het accepteren van de order tot het markeren van de order als verzonden of het initiëren van het ophalen in de winkel. 

## <a name="set-up-the-order-fulfillment-operation"></a>De bewerking Orderafhandeling instellen

Orderafhandeling, [bewerkings-id 928](https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/pos-operations), kan worden gebruikt om toegang te krijgen tot het werkgebied voor winkelorderafhandeling in het verkooppunt. 

Volg de stappen in [De bewerking toevoegen aan een knoppenraster](https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/pos-screen-layouts) om op te geven welke parameter moet worden gebruikt bij het aanroepen van Orderafhandeling in het verkooppunt. Standaard is **Alle orders** geselecteerd als u de bewerkingen voor orderafhandeling hebt opgegeven. Indien geconfigureerd met deze parameter worden met de bewerking alle orderregels voor afhandeling in de huidige winkel weergegeven. Ook de parameter **Te verzenden orders** is beschikbaar. Deze kan worden toegewezen aan een knop en worden gebruikt als de gebruiker alleen de orders wil zien die vanuit de winkel worden verzonden. Er ten slotte is er **Orders voor afhalen**. Wanneer deze parameter wordt aangeroepen bij het verkooppunt, worden alleen orders weergegeven die moeten worden afgehaald in de winkel. De verschillende parameters kunnen aan verschillende knoppen worden toegewezen om de gebruiker verschillende manieren te bieden om orderafhandeling weer te geven. 

### <a name="enable-users-to-access-order-fulfillment-at-the-point-of-sale"></a>Stel gebruikers in staat om in het verkooppunt toegang te krijgen tot orderafhandeling. 

Voor de orderafhandelingsbewerking bestaat geen eigen standaardmachtiging, maar in de toekomst kunnen gebruikers de machtiging **Order ophalen toestaan** gebruiken om de bewerking aan te roepen vanuit het verkooppunt.

Op het winkelniveau is een configuratie-instelling beschikbaar om te bepalen of een orderregel handmatig moet worden geaccepteerd vanuit het verkooppunt. Als deze configuratieoptie niet is ingesteld, worden orderregels standaard geaccepteerd. Als deze configuratieoptie is ingeschakeld, moeten gebruikers bij het verkooppunt de machtiging **Order accepteren toestaan** selecteren om orders vanuit het verkooppunt te accepteren. 


### <a name="enable-manual-order-acceptance"></a>Handmatige orderacceptatie inschakelen

Standaard worden aan een winkel toegewezen orderregels gemarkeerd als **Geaccepteerd**. Dit betekent dat ervan wordt uitgegaan dat deze worden afgehandeld vanuit de toegewezen winkel en niet meer hoeven te worden toegewezen. In bepaalde gevallen willen detailhandelaren orders mogelijk handmatig accepteren voordat ze kunnen worden afgehandeld. Wanneer in een winkel door onderbezetting bepaalde orders niet kunnen worden afgehandeld, accepteert een winkelmanager bijvoorbeeld slechts zoveel orders als op een bepaalde dag kunnen worden verwerkt. Totdat een order wordt geaccepteerd, kan deze opnieuw worden toegewezen door de backoffice. Op deze manier biedt orderacceptatie ook een manier om aan te geven dat een order is bevestigd door een winkel en wordt afgehandeld. 

Orderregels voor afhalen in de winkel zijn gemarkeerd als **In behandeling** en hoeven niet te worden geaccepteerd.

Als u handmatige acceptatie voor orderregels wilt inschakelen, gaat u naar **Detailhandel** > **Kanalen** > **Detailhandelwinkels** > **Alle detailhandelwinkels**. Selecteer de winkel en klik op de winkel-id om de details van de winkel te bekijken. Klik op **Bewerken**. Zoek op het sneltabblad **Algemeen** de subkop **Orderafhandeling** en wijzig **Handmatig accepteren** van **Nee** in **Ja**. 

### <a name="enable-reject-order-line-capability"></a>De functie voor het afwijzen van orderregels inschakelen

Orderregels kunnen ook vanuit het verkooppunt worden afgewezen. Als een orderregel wordt afgewezen, betekent dit dat deze niet wordt afgehandeld in die winkel en naar een andere winkel of een ander magazijn wordt gestuurd om opnieuw te worden toegewezen. De machtiging voor het afwijzen van orderregels wordt verleend via de machtiging **Afwijzen van order toestaan** in de POS-machtigingsgroep die is gekoppeld aan de werknemer. Detailhandelaren kunnen hun werknemers ertoe verplichten een reden op te geven wanneer ze een regel afwijzen. U kunt dit doen met behulp van informatiecodes van het type **Infocode voor activiteit** voor **Orderafhandeling** en door de informatiecode toe te wijzen aan **Orderregel afwijzen** in het functionaliteitsprofiel dat is gekoppeld aan het kanaal. 

>[!Note]
>Alleen informatiecodes van het type **Infocode voor activiteit** voor **Orderafhandeling** kunnen worden toegewezen aan de actie **Orderregel afwijzen**.

### <a name="synchronize-changes-to-the-channel-database"></a>Wijzigingen synchroniseren met de afzetkanaaldatabase

Nadat de bewerking aan een knoppenraster is toegewezen, de juiste machtigingen zijn toegewezen en het kanaal is geconfigureerd, moeten de wijzigingen worden gesynchroniseerd naar de kanaaldatabase. Ga hiervoor naar **Detailhandel** > **IT detailhandel** > **Distributieplanning**. Selecteer de planning 1090-Kassa's om knoppenrasterwijzigingen te synchroniseren en klik op **Nu uitvoeren**. Synchroniseer vervolgens wijzigingen in machtigingen door 1060-Personeel te selecteren en op **Nu uitvoeren** te klikken. Synchroniseer vervolgens kanaalwijzigingen door 1070-Kanaalconfiguratie te selecteren en op **Nu uitvoeren** te klikken. Synchroniseer ten slotte de zojuist gemaakte informatiecode voor de afwijzingsreden door 1110-Algemene configuratie te selecteren en op **Nu uitvoeren** te klikken.

## <a name="use-order-fulfillment-at-the-point-of-sale"></a>Orderafhandeling gebruiken in het verkooppunt

Open het verkooppunt en selecteer de bewerking voor orderafhandeling. Afhankelijk van de configuratie, worden alle regels, orderregels voor ophalen of orderregels voor verzending weergegeven. 

### <a name="order-fulfillment-view"></a>Weergave voor orderafhandeling 

In de weergave voor orderafhandeling worden de orderregels voor afhandeling in de winkel weergegeven. De weergave biedt de volgende kolommen:

  - Ordernummer
  - Productnummer
  - Omschrijving
  - Bestelde hoeveelheid
  - Gevraagde leveringsdatum
  - Klantnaam
  - Afhandelingsstatus
  
U kunt extra informatie voor een bepaalde orderregel weergeven door de orderregel te selecteren en vervolgens het fly-outmenu te openen dat zich net onder de weergegeven aangemelde gebruiker/dienstinformatie in de koptekst bevindt. Dit menu bevat twee tabbladen: één voor regeldetails en een ander voor orderdetails. Het tabblad voor regeldetails bevat de volgende informatie:

  - Bestelde hoeveelheid
  - Hoeveelheid die nog moet worden verzonden/opgehaald
  - Opgenomen hoeveelheid
  - Verpakte hoeveelheid
  - Gefactureerde hoeveelheid (al afgehaald of verzonden)
  - Leveringsmethode
  - Afleveradres
  
Het fly-outmenu met details bevat ook een tabblad met meer orderniveaudetails, waaronder:

  - Klantnaam
  - Klant-ID
  - Ordernummer
  - Ordertotaal
  - Ordersaldo
  
Onder in de weergave voor orderafhandeling bevindt zich een actievenster. Dit venster bevat alle acties die kunnen worden uitgevoerd voor een orderregel. Als een actie niet beschikbaar is op basis van de status van een regel, is die actie niet beschikbaar. 

Standaard hebben orders de status **Geaccepteerd**. De orderstatus kan worden weergegeven als een kolom in de lijst met orderregels. Als **Handmatig accepteren** is geconfigureerd op het kanaalniveau, worden alle te verzenden regels als **In behandeling** weergegeven en moeten deze worden geaccepteerd voordat ze kunnen worden afgehandeld. Orders voor afhalen in de winkel zijn standaard **In behandeling** en hoeven niet te worden geaccepteerd.

### <a name="order-fulfillment-line-actions"></a>Regelacties voor orderafhandeling

**Bewerken**: als een orderstatus in behandeling is, kan de order worden bewerkt in het verkooppunt. Orders die al gedeeltelijk verzameld, verpakt of gefactureerd zijn, kunnen niet worden bewerkt vanuit de weergave voor orderafhandeling.

**Accepteren**: als **Handmatig accepteren** is geconfigureerd op kanaalniveau, moeten regels worden geaccepteerd voordat ze het orderafhandelingsproces kunnen doorlopen.

**Orderverzamelen**: deze actie ondersteunt verschillende acties. Met **Orderverzamelen** wordt de status van de orderregel bijgewerkt zodat anderen in de winkel niet proberen deze regel te verzamelen. Vervolgens wordt met **Orderverzamellijst afdrukken** een orderverzamellijst voor de geselecteerde regel of regels afgedrukt en wordt de status ervan bijgewerkt naar **Orderverzameling**. Orderverzamellijstindelingen worden beheerd als onderdeel van ontvangstbewijsindelingen. Zie voor meer informatie over het instellen van ontvangstbewijsindelingen [Ontvangstsjablonen en afdrukken](https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/receipt-templates-printing). Ten slotte wordt met **Markeren als opgenomen** aangegeven dat de regel is verzameld. **Markeren als opgenomen** initieert de bijbehorende voorraadtransacties in de backoffice. Verzamelacties kunnen tegelijkertijd voor meerdere orderregels in verschillende orders en voor alle leveringsmethoden worden uitgevoerd.

**Afwijzen**: regels of gedeeltelijke regels kunnen worden afgewezen. Op deze manier kunnen ze vanuit de backoffice opnieuw worden toegewezen aan een andere winkel of een ander magazijn. Regels kunnen alleen worden afgewezen als ze nog niet zijn verzameld of verpakt. Voor een regel die al is verzameld of verpakt, moet de verzameling of verpakking ongedaan worden gemaakt vanuit de backoffice. 

**Verpakking**: de verpakkingsoptie ondersteunt twee acties. Met **Pakbon afdrukken** wordt een pakbon voor de geselecteerde regels afgedrukt en met **Markeren als verpakt** worden de regels als verpakt gemarkeerd en worden de regels als geleverd gemarkeerd in de backoffice. Alleen orderregels die bij dezelfde order horen en dezelfde leveringsmethode hebben, kunnen op hetzelfde moment worden verpakt. Pakbonindelingen worden beheerd als onderdeel van ontvangstbewijsindelingen. Zie voor meer informatie over het instellen van ontvangstbewijsindelingen [Ontvangstsjablonen en afdrukken](https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/receipt-templates-printing).

**Verzenden**: met de verzendactie worden geselecteerde regels als **Geleverd** gemarkeerd in de backoffice. Als een regel volledig is verzonden, wordt deze niet meer weergegeven in de weergave voor orderafhandeling.

**Afhalen**: met de afhaalactie worden de regels toegevoegd aan de transactieweergave voor afhalen. Als de order nog andere regels bevat die momenteel niet worden afgehaald, worden deze met de hoeveelheid nul toegevoegd aan de transactieweergave. Als een regel volledig is afgehaald, wordt deze niet meer weergegeven in de weergave voor orderafhandeling. 

### <a name="order-fulfillment-filtering"></a>Filteren van orderafhandeling

Orderafhandeling in het verkooppunt omvat allerlei filters, zodat gebruikers gemakkelijk vinden wat ze nodig hebben. Filters kunnen in het actievenster onder in het scherm **Verkooppunt** worden gewijzigd. Standaard wordt een filter **Leveringstype** toegepast, afhankelijk van hoe de bewerking is ingesteld. Als de bewerking is ingesteld met de parameter **Alle orders**, wordt dit filter toegepast bij het openen van Orderafhandeling. Hetzelfde geldt voor de parameters **Ophalen in de winkel** en **Verzenden uit winkel**. Andere filters die kunnen worden toegepast op de weergave Orderafhandeling zijn onder andere:

  - Klantnummer
  - Klantnaam
  - E-mail klant
  - Ordernummer
  - Leveringsmethode
  - Ontvangstbewijsnummer
  - Afzetkanaalverwijzings-id
  - Oorspronkelijk winkelnummer
  - Regelstatus
  - Gemaakt op
  - Leveringsdatum
  - Ontvangstdatum

