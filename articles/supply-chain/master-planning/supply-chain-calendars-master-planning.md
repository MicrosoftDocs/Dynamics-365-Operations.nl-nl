---
title: Kalenders en hoofdplanning
description: Dit onderwerp biedt een overzicht van toeleveringskalenders en hoe deze de hoofdplanning beïnvloeden.
author: t-benebo
manager: tfehr
ms.date: 08/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 2c32957b0bd234ed14e6333a36a46c6a83ec2e91
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/13/2020
ms.locfileid: "4425466"
---
# <a name="calendars-and-master-planning"></a>Kalenders en hoofdplanning

[!include [banner](../includes/banner.md)]

Dit onderwerp biedt een overzicht van toeleveringskalenders en hoe deze de hoofdplanning beïnvloeden.  De verschillende kalenders die in de hoofdplanningsengine worden gebruikt, worden beschreven, inclusief hoe deze van invloed zijn op verzend- en ontvangstdatums in de geplande orders. Ten slotte worden aanbevelingen gedaan met betrekking tot de toewijzing, het gebruik en de update van de kalenders.

## <a name="definition-of-a-calendar"></a>Definitie van een kalender

U kunt een kalender definiëren om te gebruiken in uw organisatie op de pagina **Organisatiebeheer > Instellen > Kalenders > Kalenders**. 

Elk datumitem in een kalender kan **open** of **gesloten** of **basiskalender** zijn. Dit wordt opgegeven in de kolom **Controle** op de pagina **Werktijden**. Voor elke datum: 
- **Open** - geeft aan dat werk wordt uitgevoerd op de geselecteerde dag. De kalender wordt bijgewerkt volgens de werktijdsjabloon.
- **Gesloten** - geeft werk aan dat niet tijdens de dag wordt uitgevoerd. 
- **Basiskalender** - geeft aan dat de specifieke datum de werktijden en open/gesloten overneemt van de basiskalender. Wanneer de basiskalender wordt bijgewerkt, neemt de geselecteerde kalender er daarom bewerkingstijden van over. 

Voor gesloten datums wordt het selectievakje **Gesloten voor ophalen** automatisch toegewezen. Voor open datums kunt u de optie **Gesloten voor ophalen** handmatig selecteren. Dit geeft aan dat werk wordt uitgevoerd op de datum, maar verzending wordt niet uitgevoerd. 

## <a name="calendars-that-affect-master-planning"></a>Kalenders die gevolgen hebben voor de hoofdplanning

### <a name="calendar-for-a-coverage-group"></a>Kalender voor een behoefteplanningsgroep
Een behoefteplanningsgroep geeft aan dat een gemeenschappelijke set parameters wordt gebruikt voor aanvulling van de artikelen die tot de opgegeven behoefteplanningsgroep behoren. 

Als u een kalender voor een behoefteplanningsgroep wilt toevoegen, gaat u naar **Hoofdplanning > Instellen > Behoefteplanning > Behoefteplanningsgroepen**. Zoek de behoefteplanningsgroep waaraan u de kalender wilt toewijzen en selecteer deze in het veld **Kalender**.

De behoefteplanningsgroep kan op verschillende pagina's worden toegewezen: 
    - Op de pagina **Vrijgegeven productdetails** van een artikel. Als u de behoefteplanningsgroep voor een artikel wilt zien, gaat u naar **Productgegevensbeheer > Producten > Vrijgegeven producten** en selecteert u het artikel om naar de pagina **Details van vrijgegeven producten** te gaan. U ziet de behoefteplanningsgroep van het artikel op het sneltabblad **Plannen**.
    - Op de pagina **Artikelbehoefteplanning**. Klik op de pagina Details van vrijgegeven producten op **Artikelbehoefteplanning** om naar de pagina Artikelbehoefteplanning te gaan. Op het overzichtstabblad ziet u verschillende parameters voor aanvulling afhankelijk van de locatie, het magazijn en de productdimensies. De behoefteplanningsgroep voor elk artikel wordt overgenomen van de behoefteplanningsgroep van de pagina **Details van vrijgegeven producten**. Dit kan worden overschreven met behulp van **Specifieke instellingen gebruiken** of **Instellingen behoefteplanningsgroep overschrijven** op het tabblad **Algemeen**.
    - Op de pagina **Parameters hoofdplanning**. Als voor een artikel geen behoefteplanningsgroep is ingesteld op de vorige pagina's, gebruikt hoofdplanning de algemene behoefteplanningsgroep die is ingesteld in hoofdplanningsparameters. Dit wordt ingesteld in **Hoofdplanning > Instellen > Parameters hoofdplanning** in het veld **Algemene behoefteplanningsgroep**. 

### <a name="calendar-for-a-vendor"></a>Kalender voor een leverancier
Om de werkdagen van een leverancier aan te geven kunt u een Inkoopkalender toewijzen aan de leverancier op de pagina **Details over inkooporders**. 

Als u een agenda voor een leverancier wilt instellen, moet u de kalender maken in **Organisatiebeheer > Kalenders > Kalenders**. Wanneer de kalender is gemaakt, moet u deze toewijzen aan de leverancier. Ga naar **Leveranciers > Leveranciers > Alle leveranciers** en selecteer de leverancier aan wie u de kalender wilt toewijzen. Wijs vervolgens op de pagina van de leverancier op het sneltabblad **Details over inkooporders** de nieuwe inkoopkalender toe met behulp van het vervolgkeuzemenu. 

De kalender voor een leverancier geeft de dagen aan waarop de leverancier de plaatsing van de inkooporder accepteert en de datums waarop de leverancier de orders aan uw bedrijf kan leveren. De orderdatums voor inkooporders voor de leverancier met een inkoopkalender zijn daarom datums die als open zijn gedefinieerd in de kalender. De leveringsdatums voor die orders vallen ook op open dagen en zijn dus van invloed op de levertijd van het ingekochte artikel. 

#### <a name="define-the-lead-time-for-a-purchased-item"></a>De doorlooptijd definiëren voor een ingekocht artikel

Als u de inkoopdoorlooptijd wilt opgeven (en als alleen werkdagen moeten worden beschouwd) voor een artikel, moet u naar de pagina met standaardorderinstellingen gaan voor het product, die u vindt onder **Productgegevensbeheer > Producten > Vrijgegeven producten** en selecteer **Standaard orderinstellingen**. 

> [!Note]
> De **werkdagen** onder inkoopdoorlooptijd geven de werkdagen van de leverancier aan. Een kalender voor bijvoorbeeld alleen levering op dinsdagen met een doorlooptijd van 10 dagen en het selectievakje Werkdagen ingeschakeld geeft aan dat het 10 weken (10 dinsdagen) duurt voordat het artikel is geleverd.
Dus in de meeste gevallen wordt het niet aanbevolen werkdagen te selecteren voor inkooporderdoorlooptijden.

#### <a name="define-lead-times-from-the-trade-agreements-page"></a>Doorlooptijden definiëren vanaf de pagina handelsovereenkomsten

Hoofdplanning kan worden ingesteld zodat het alle handelsovereenkomsten voor leveranciers omvat. Handelsovereenkomsten zijn vaste prijzen of kortingsovereenkomsten die zijn ingesteld voor een of meer klanten of leveranciers voor de verkoop of inkoop van afzonderlijke of meerdere producten. Ga naar **Hoofdplanning > Instellen > Parameters hoofdplanning** en selecteer op het tabblad **Geplande orders** **Handelsovereenkomsten zoeken** om de handelsovereenkomsten op te nemen bij het plannen. Hoofdplanning kan de leverancier selecteren met de **Minimale levertijd** of met de **Laagste eenheidsprijs**.

### <a name="calendar-for-a-warehouse"></a>Kalender voor een magazijn
U kunt een kalender toewijzen aan een magazijn om de open datums aan te geven voor ontvangst en verzending. Als er geen kalender is toegewezen aan een magazijn, wordt ervan uitgegaan dat alle dagen open zijn. 

> [!Note]
> Een kalender toewijzen aan een transitmagazijn heeft geen invloed. Transitmagazijnen worden gebruikt voor de ondersteuning van transferorders. De toepasselijke datums voor verzending of ontvangst voor de orders worden gedefinieerd door de open dagen in het magazijn 'Vanaf' en het magazijn 'Naar' en de leveringsmethodekalender.

#### <a name="closed-for-pickup-policy"></a>Beleid Gesloten voor ophalen
Als u wilt aangeven dat een magazijn open is voor ontvangst, maar ophalen niet mogelijk is, kunt u het **Beleid Gesloten voor ophalen** gebruiken binnen de magazijnkalender. Dit geldt ook voor ophalen door klanten. 

### <a name="transport-calendar"></a>Transportkalender 
Om de datums aan te geven die beschikbaar zijn voor het verzenden van transferorders vanuit een **Van magazijn** kunt u een **transportkalender** toewijzen. U kunt een transportkalender per leveringsmethode of per leveringsmodus en van-magazijn instellen. De transportkalender wordt ingesteld in **Verkoop en marketing > Instellen > Distributie > Leveringsmethoden**. Selecteer een leveringsmethode en klik op de knop **Transportkalender**.

Een regel kan worden gemaakt voor elk magazijn en elke leveringsmethode, waarbij de kalender wordt toegevoegd aan de kolom **Transportkalender**. Deze geeft de transportkalender op die wordt toegepast wanneer goederen worden verzonden vanuit het magazijn met behulp van de opgegeven leveringsmethode. Als u een transportkalender wilt toepassen op alle zendingen met behulp van een bepaalde leveringsmethode, kan een regel worden gemaakt zonder het magazijn op te geven.  Dit is van invloed op alle zendingen met de opgegeven leveringsmethode, ongeacht het magazijn. 

Als er geen transportkalender is toegewezen, wordt ervan uitgegaan dat alle dagen open zijn voor transport.

### <a name="calendar-for-a-customer"></a>Kalender voor een klant
Als u wilt opgeven op welke datums een klant leveringen kan accepteren, kunt u een ontvangstkalender toewijzen aan de klant. Als er geen kalender is toegewezen aan een klant, wordt ervan uitgegaan dat de klant orders op alle dagen kan ontvangen. Dit heeft invloed op de ontvangstdatum op de verkooporderregels. Als u een datum in de verkooporderregels selecteert die niet 'open' is in de kalender van de klant, geeft het systeem aan dat de ontvangstdatum niet geldig is. 

Opmerking: u kunt slechts één kalender per klant opnemen. Als u een kalender voor elk adres van een klant moet opnemen, kunt u één klant per adres maken en er vervolgens de desbetreffende kalender aan toewijzen. 

De aangevraagde ontvangstdatum op de verkooporderregels is afhankelijk van de kalender van de klant en de controlemethode voor leveringsdatums. U vindt meer informatie over hoe de vroegste leveringsdatum wordt berekend in [Orderbelofte](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/delivery-dates-available-promise-calculations).

### <a name="shipping-calendar-for-a-legal-entity"></a>Verzendkalender voor een rechtspersoon
Om de datums aan te geven waarop een rechtspersoon goederen kan verzenden, kunt u een verzendkalender instellen onder **Organisatiebeheer > Organisaties > Rechtspersonen**. Selecteer de rechtspersoon en voeg de kalender toe op het tabblad **Buitenlandse handel en logistiek**, in het veld **Verzendkalender**. De verzendkalender zal fungeren als een bron van standaardwaarden voor alle magazijnkalenders in de rechtspersoon. 

## <a name="how-calendars-affect-dates-in-planning"></a>Hoe kalenders datums beïnvloeden in de planning

### <a name="order-date-of-a-planned-purchase-order"></a>Orderdatum van een geplande inkooporder 
De orderdatum in een geplande inkooporder geeft de datum aam waarop de order is geplaatst. Dit is een open datum zowel in de leverancierskalender als in de kalender van de behoefteplanningsgroep. Leveranciers moeten soms een paar dagen marge aanhouden tussen wanneer ze de inkooporder ontvangen en wanneer ze de goederen kunnen verzenden. Deze datums worden aangegeven in de margedagen van de leverancier. Als het ingekochte artikel echter is toegewezen aan een behoefteplanningsgroep met margedagen, overschrijven deze margedagen de margedagen van de leverancier.

### <a name="delivery-date-of-a-planned-purchase-order"></a>Leveringsdatum van een geplande inkooporder
De ontvangstdatum van een inkoop geeft de datum aan waarop u de goederen ontvangt. Dit is een open datum in de kalender. De kalender die in aanmerking worden genomen om aan te geven op welke dagen de inkooporders kunnen worden ontvangen, zijn de volgende, op volgorde van hoogste naar laagste prioriteit: 
1. Kalender van leverancier
1. Kalender van behoefteplanningsgroep
1. Magazijnkalender voor het ontvangende magazijn

Houd er rekening mee dat de kalender van de behoefteplanningsgroep kan worden ingesteld op verschillende pagina's en prioriteit heeft in deze volgorde:
1. Artikelbehoefteplanningsgroep op de pagina **Artikelbehoefteplanning**
1. Artikelbehoefteplanningsgroep op de pagina **Details van vrijgegeven producten**
1. Standaard artikelbehoefteplanningsgroep in **Parameters hoofdplanning**

### <a name="shipping-date-of-a-planned-transfer-order"></a>Verzenddatum van een geplande transferorder
Bij het maken van een transferorder tussen twee magazijnen worden de verzenddatum en de ontvangstdatum opgenomen in de transferorderkop, samen met het 'Van'-magazijn en het 'Naar'-magazijn. Het verschil tussen deze twee datums is de verwachte transporttijd (in dagen) tussen de magazijnen.

De verzenddatum van een geplande transferorder geeft de datum aan waarop de goederen worden verzonden vanuit het 'Van'-magazijn. De kalenders die worden gebruikt voor het opgeven van de beschikbare verzenddatum, worden op prioriteit weergegeven: 
1. Magazijnkalender van het 'Van'-magazijn
1. Behoefteplanningsgroepskalender (zie terugvalorder voor deze kalender hierboven); als er een magazijnkalenderset is, is de verzenddatum een open datum in de kalender. Als er geen magazijnkalender is, wordt de kalender van de behoefteplanningsgroep gebruikt. 

### <a name="receipt-date-of-a-planned-transfer-order"></a>Ontvangstdatum van een geplande transferorder
De ontvangstdatum van een transferorder geeft de datum aan waarop de goederen worden ontvangen in het 'Naar'-magazijn.

De kalenders die worden gebruikt voor het opgeven van de ontvangstdatum, worden op prioriteit weergegeven: 
1. Kalender van behoefteplanningsgroep 
1. Magazijnkalender van het 'Naar'-magazijn; als er een behoefteplanningskalenderset is, is de ontvangstdatum een open datum in de kalender. Als er geen behoefteplanningsgroepskalender is, wordt de magazijnkalender gebruikt. 

Wanneer de verzend- en ontvangstdatum voor de geplande transfer wordt gezocht, wordt ook rekening gehouden met de marges die door de gebruiker zijn ingesteld voor verzending en ontvangst. 

## <a name="using-calendars-in-master-planning"></a>Kalenders gebruiken in hoofdplanning

### <a name="assignment-of-scm-calendars"></a>Toewijzing van SCM-kalenders
Het is belangrijk om de kalenders in te stellen ter identificatie van de werkdagen van het bedrijf. De beste implementatie is een kalender in te stellen voor elk element met verschillende werkdagen. Met andere woorden, alle externe kalenders (klant, leverancier) en alle interne (magazijn, behoefteplanningsgroep en leveringsmethode) die zijn gerelateerd aan het bedrijf.

### <a name="recommendation-on-warehouse-calendars"></a>Aanbeveling voor magazijnkalenders
Het wordt aanbevolen één kalender per magazijn te gebruiken om de specifieke wijzigingen op te nemen die alleen gevolgen hebben voor het magazijn. Twee of meer magazijnen kunnen bijvoorbeeld de dezelfde werkdagen maar een ander ophaalbeleid hebben. In dat geval is een kalender voor elk van de magazijnen met het respectievelijke ophaalbeleid de beste implementatie voor het systeem om de beste datums voor geplande inkoop-, transfer- en productieorders op te nemen. Als er geen magazijnkalenders zijn ingesteld, kan de kalender van de rechtspersoon worden gebruikt als een bron van standaardwaarden voor de magazijnkalender. 

### <a name="recommendation-of-coverage-group-calendars"></a>Aanbeveling voor behoefteplanningsgroepskalenders
Met betrekking tot de behoefteplanningsgroepkalender is het van belang er rekening mee te houden dat die ontvangstdatums in hoofdplanning overschrijft. Het verdient aanbeveling deze voorzichtig te gebruiken. Het is met name nuttig wanneer aanvulling voor specifieke dagen in de week moet worden uitgevoerd. 

### <a name="updating-scm-related-calendars"></a>SCM-gerelateerde kalenders bijwerken
Het is belangrijk dat alle relevante kalenders hun respectieve plaats toegewezen krijgen (leverancier, klant, magazijn, leveringsmethode of behoefteplanningsgroep), maar deze kalenders bijwerken is net zo belangrijk, zodat ze de wijzigingen bevatten. Het systeem definieert de productie-, transfer-, inkoop- en verkooporderdatums afhankelijk van de combinatie van de toegewezen kalenders. Het is raadzaam om aan te geven wie verantwoordelijk is voor het toewijzen en bijwerken van de kalenders op de corresponderende gebieden. In geval van een uitval of andere ongebruikelijke wijziging in de werkdagen is het essentieel de kalenders dienovereenkomstig bij te werken. Alle taken die afhankelijk zijn van kalenders, zoals de hoofdplanning en de productieplanning moeten opnieuw worden uitgevoerd wanneer kalenders worden bijgewerkt. 
