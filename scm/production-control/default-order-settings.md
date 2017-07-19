---
title: Standaardorderinstellingen voor dimensies en productvarianten
description: "Standaardorderinstellingen definiëren de locatie en het magazijn waaruit de artikelen worden geleverd of waarin ze worden opgeslagen, de minimum-, maximum-, meervoud- en standaardhoeveelheden die voor handel of voorraadbeheer worden gebruikt, de levertijden, de eindevlag, en de methode voor orderbelofte."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventItemOrderSetup
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations, UnifiedOperations, Retail
ms.custom: 223084
ms.assetid: fbfbcd7b-dc75-44ab-bffc-8bad576804a4
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-11-30T00:00:00.000Z
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: 9262dcaa3b326d8c31b7d7416b102920795da94b
ms.openlocfilehash: b4e8ff363a98f8dfc90af0133807373566531568
ms.contentlocale: nl-nl
ms.lasthandoff: 06/13/2017

---

# <a name="default-order-settings-for-dimensions-and-product-variants"></a>Standaard orderinstellingen voor dimensies en productvarianten

[!include[banner](../includes/banner.md)]

[!include[retail name](../includes/retail-name.md)]


Met standaardorderinstellingen in Microsoft Dynamics 365 for Finance and Operations, Enterpise edition worden de locatie en het magazijn gedefinieerd waaruit de artikelen worden geleverd of waarin ze worden opgeslagen, de minimum-, maximum-, meervoud- en standaardhoeveelheden die voor handel of voorraadbeheer worden gebruikt, de levertijden, de eindevlag, en de methode voor orderbelofte. Standaardorderinstellingen worden gebruikt bij het maken van inkooporders, verkooporders, transferorders, voorraadjournalen, en door de hoofdplanning voor het genereren van geplande orders. Standaardorderinstellingen kunnen specifiek zijn voor het artikel, de locatie, de productvariant of de productdimensie.

U definieert de standaardinstellingen voor orders op de pagina **Standaard orderinstellingen**. U opent deze pagina als volgt: ga naar **Productgegevensbeheer** &gt; **Producten** &gt; **Vrijgegeven producten** &gt;, selecteer een vrijgegeven product &gt; in het actievenster **Plannen** of Voorraadbeheer &gt; **Orderinstellingen** &gt; **Standaardorderinstellingen**.

## <a name="default-order-settings"></a>Standaard orderinstellingen
Er zijn drie typen standaardorderinstellingen: voor inkoop, verkoop en voorraad. De standaardorderinstellingen voor inkoop worden gebruikt wanneer u de volgende items maakt:

-   Inkooporderregels
-   Inkoopovereenkomstregels
-   Offerteaanvraagregels
-   Regels op opdracht tot inkoop
-   Consignatieaanvullingsregels
-   Geplande inkooporders

De standaardorderinstellingen voor verkoop worden gebruikt wanneer u de volgende items maakt:

-   Verkooporderregels
-   Verkoopovereenkomstregels
-   Verkoopofferteregels
-   Retourorderregels en regels voor artikelvervanging
-   Vraagprognoseregels

De standaardorderinstellingen voor verkoop worden ook toegepast wanneer u de volgende items maakt:

-   Projectartikelbehoeften
-   Artikelbehoeften bij serviceorders

De standaardorderinstellingen voor voorraad worden gebruikt wanneer u de volgende items maakt:

-   Voorraadjournalen
-   Transferorders
-   Geplande transferorders

De standaardorderinstellingen voor voorraad worden ook toegepast wanneer u de volgende items maakt:

-   Quarantaineorders
-   Kwaliteitsorders
-   Productieorders
-   Stuklijstregels
-   Geplande productieorders

## <a name="full-definition-of-a-released-product"></a>Volledige definitie van een vrijgegeven product
Wanneer u een transactie maakt, moet u de volledige definitie van een vrijgegeven product op de regel opgeven voordat Finance and Operations de standaardorderinstellingen probeert vast te stellen. De volledige definitie van vrijgegeven producten betekent dat het artikelnummer en alle actieve productdimensies, zoals configuratie, grootte, stijl en kleur, worden opgegeven in de transactie. Als u bijvoorbeeld handmatig een inkooporderregel voor een vrijgegeven productvariant maakt, moet u alle vereiste productdimensies opgeven voordat de locatie, het magazijn, hoeveelheden en de levertijd standaard op de orderregel worden weergegeven. 

Niet alle parameters van de standaardorderinstellingen worden toegepast wanneer u een order of journaalregels maakt. Hoeveelheden en levertijden worden alleen standaard weergegeven wanneer dat kan. Bijvoorbeeld bij het tellen van een journaalregel worden alleen de locatie en het magazijn standaard weergegeven wanneer de regel wordt gemaakt. Vanzelfsprekend worden geen standaardhoeveelheden ingevuld of controles op meervouden en minimumhoeveelheden uitgevoerd, wanneer u de regel aanmaakt of het journaal boekt. 

Wanneer u een order of een journaalregel maakt, wordt altijd geprobeerd om een standaardlocatie en standaardmagazijn te vinden. De locatie wordt niet altijd standaard weergegeven vanuit de orderinstellingen. Wanneer u bijvoorbeeld een verkooporder of een inkooporder maakt, wordt de locatie van de orderkoptekst automatisch gebruikt in de orderregels. Wanneer u een stuklijstregel maakt, wordt de locatie van de koptekst van de stuklijst gebruikt. Nadat de locatie is bepaald, wordt deze gebruikt om eventuele locatiespecifieke orderinstellingen te vinden die daarna als standaardinstellingen voor het magazijn kunnen worden gebruikt. 

Het standaardordertype, de inkoop en de levertijden voorraad kunnen worden overschreven door de behoefteplanningsregels van het artikel op de pagina **Artikelbehoefteplanning**. Hoewel de standaardorderinstellingen geen onderscheid kunnen maken tussen de doorlooptijden voor productie en die voor verplaatsing, kunnen de artikelbehoefteplanningsregels hier wel mee overweg. De instellingen voor artikelbehoefteplanning worden echter alleen gebruikt door MRP bij het maken van geplande orders voor productie en transfer, niet wanneer u handmatig productie- en transferorders maakt. 

## <a name="default-order-settings-rules"></a>Regels voor standaardorderinstellingen
U kunt algemene standaardorderinstellingen definiëren, evenals alle benodigde regels voor standaardorderinstellingen die alleen onder bepaalde voorwaarden gelden, zoals locatie of een bepaalde productdimensie of een combinatie van productdimensies. U kunt geen orderinstellingen definiëren die specifiek zijn voor het magazijn.

### <a name="rank-in-default-order-settings"></a>Rangen in standaardorderinstellingen

De regels voor standaardorderinstellingen kennen rangen. Hoe hoger de rang, des te belangrijker de regel is. Dit houdt in dat de regel een hogere prioriteit heeft en wordt toegepast vóór regels met een lagere rang. De algemene standaardorderinstellingen hebben de rang 0 (nul). Deze rang kan niet worden gewijzigd. Er kan slechts één regel zijn met rang 0. Regels kunnen dezelfde rang hebben, als ze worden toegepast op verschillende dimensies. Dit is nuttig wanneer u locatiespecifieke orderinstellingen wilt modelleren. Wanneer een nieuwe regel voor standaardorderinstellingen wordt gemaakt, worden de waarden voor orderwaarden, eindevlag, e.d. overgenomen van de regel met rang 0. Deze waarden kunnen worden overschreven.

### <a name="default-order-settings-for-released-products"></a>Standaardorderinstellingen voor vrijgegeven producten

Voor bepaalde vrijgegeven producten kunt u de algemene orderinstellingen of locatiespecifieke orderinstellingen definiëren. De algemene orderinstellingen hebben altijd rang 0. Als u nieuwe orderinstellingen voor verkoop, inkoop en voorraad tegelijk aanmaakt, wordt het aangeraden om gebruik te maken van de weergave **Details** op de pagina **Standaard orderinstellingen**. Om over te schakelen naar de detailweergave gaat u naar het actievenster **Opties** &gt; **Paginaopties** &gt; **Weergave wijzigen** &gt; **Detailweergave**.

### <a name="site-specific-order-settings"></a>Vestigingspecifieke orderinstellingen

Als u locatiespecifieke orderinstellingen wilt maken, klikt u op **Nieuw**. Vul in de **Detailweergave** de locatie in het veld **Instellingen die van toepassing zijn op** &gt; **Locatie** in. Vul in de **Rasterweergave** de locatie in in de kolom **Locatie**. De nieuwe regel krijgt automatisch een nieuwe rangwaarde die hoger is dan nul. U kunt zoveel locatiespecifieke regels maken als nodig en u kunt alle aan locatiespecifieke regels dezelfde rang toewijzen om aan te geven dat ze even belangrijk zijn. 

Als u in de **Detailweergave** werkt, kunt u niet het overzicht van de regels krijgen die voor het artikel zijn gemaakt. Met de knop **Lijst weergeven/verbergen** kunt u schakelen tussen het wel of niet weergeven van overzichtsgegevens. Wanneer een orderregel van een van de beschikbare typen wordt gemaakt en er geen locatie voor is opgegeven, zoekt Finance and Operations naar een regel waarvoor geen locatie is opgegeven. Dit kan helpen bij het bepalen van een standaardlocatie op de orderregel. Deze locatie wordt vervolgens gebruikt om te zoeken naar een locatiespecifieke regel, waarin een standaardmagazijn kan zijn ingesteld. Dit magazijn wordt dan toegepast op de orderregel.

### <a name="specific-order-settings-for-product-dimension"></a>Specifieke orderinstellingen voor productdimensies

U kunt regels voor standaardorderinstellingen definiëren voor elke actieve productdimensie of voor een combinatie van actieve productdimensies. Als een productdimensieveld leeg wordt gelaten, dan geldt de regel voor alle waarden van de productdimensie. 

Hier volgt een voorbeeldproduct.

|                                                     |                                         |
|-----------------------------------------------------|-----------------------------------------|
| **Productnaam**                                    | Foto-elektrische sensor                    |
| **Artikelnummer**                                     | XW56                                    |
| **Configuratie** (gebruikt om het type licht te modelleren) | C1-zichtbaar rood licht, C2-infrarood licht |
| **Stijl** (gebruikt om de technische revisieniveau te modelleren)  | R1, R2, R3                              |

Stel dat dit product niet is geproduceerd maar aangeschaft. Verder nemen we aan dat configuratie C1 vaker wordt gebruikt, zodat deze kortere levertijden heeft. 

Maak de volgende standaardorderinstellingen aan om dit scenario te modelleren.

| Positie | Vestiging | Configuratie | Opmaakmodel | Inkoop: Standaardinstellingen overschrijven | Inkoopdoorlooptijd | Inkoop: Gestopt | Verkoop: Standaardinstellingen overschrijven | Verkoop: Gestopt |
|------|------|---------------|-------|--------------------------------------|--------------------|--------------------|-----------------------------------|-----------------|
| 10   |      | C1            |       | Ja                                  | 2                  |                    |                                   |                 |
| 0    |      |               |       |                                      | 5                  |                    |                                   |                 |

Wanneer een inkooporderregel of een geplande inkooporder wordt aangemaakt voor XW56, configuratie C1, wordt aangenomen dat de levertijd 2 is, ongeacht de revisie of de locatie waarbij de regel is geplaatst. Stel dat alle revisies zijn gestopt, met uitzondering van R3.

U kunt de volgende regels voor standaardorderinstellingen maken.

| Positie | Vestiging | Configuratie | Opmaakmodel | Inkoop: Standaardinstellingen overschrijven | Inkoopdoorlooptijd | Inkoop: Gestopt | Verkoop: Standaardinstellingen overschrijven | Verkoop: Gestopt |
|------|------|---------------|-------|--------------------------------------|--------------------|--------------------|-----------------------------------|-----------------|
| 20   |      |               | R2    | Ja                                  |                    | Ja                | Ja                               | Ja             |
| 20   |      |               | R1    | Ja                                  |                    | Ja                | Ja                               | Ja             |
| 10   |      | C1            |       | Ja                                  | 2                  |                    |                                   |                 |
| 0    |      |               |       |                                      | 5                  |                    |                                   |                 |

De twee regels voor het stoppen van de oude revisies hebben dezelfde rang, dus zijn ze even belangrijk. Ze hebben beide een hogere rang dan de regel voor configuratie C1, wat betekent dat ze voorrang krijgen op de regel voor configuratie C1. 

In dit voorbeeld wordt uitgelegd waarom de ran noodzakelijk is. Als u een inkooporder voor configuratie C1 en revisie R2 maakt, zouden de twee regels voor R2 en C1 dubbelzinnig zijn als er geen rangen waren toegekend. Om de dubbelzinnigheid op te lossen, doorzoekt Finance and Operations de regels in aflopende volgorde van rang en past de eerste toepasselijke regel toe die wordt gevonden. In het huidige voorbeeld krijgt de gebruiker een waarschuwing wanneer een inkooporderregel voor configuratie C1 en revisie R2 wordt gemaakt. De melding zegt dat het artikel in de wachtstand is gezet vanwege de revisiewaarde. Als de regel voor de configuratie een hogere rang zou hebben dan de regel voor revisie, zou het maken van een inkooporderregel voor configuratie C1 en revisie R2 slagen en krijgt de gebruiker geen melding dat het artikel in de wachtstand staat. 

Bekijk de volgende regels voor standaardorderinstellingen eens.

| Positie | Vestiging | Configuratie | Opmaakmodel | Standaardsite | Standaardmagazijn | Inkoop: Standaard opslagdimensies overschrijven | Inkoopmagazijn |
|------|------|---------------|-------|--------------|-------------------|------------------------------------------------|--------------------|
| 20   | 2    |               |       |              |                   | Ja                                            | 22                 |
| 10   |      | C1            |  R2   |  2           |  21               |                                                |                    |
| 0    |      |               |       | 1            | 11                |                                                |                    |

Het systeem onderzoekt de set regels twee keer om de locatie en het magazijn te bepalen. Wanneer een inkooporderregel wordt gemaakt voor de configuratie van C1, stijl R2, kan de locatie worden bepaald op basis van de regel met positie 10. Vervolgens wordt gezocht naar een regel voor locatie 2 om een magazijn te bepalen. Regel 20 wordt gevonden en omdat deze een hogere rang heeft, wordt het magazijn voor de inkooporderregel ingesteld op 22 in plaats van 21. 

Algemeen gesproken worden hogere rangen toegekend aan specifieke regels en regels voor dimensies die belangrijker dan andere dimensies zijn. Meer algemene regels krijgen lagere rangen. 

De regel met rang 0 dient als vangnet. Als geen andere regels van toepassing zijn, worden de standaardorderinstellingen van regel 0 gebruikt. 

Omdat het rangnummer zo belangrijk is, vindt u in het actievenster **Standaard orderinstellingen** functies om een regel omhoog of omlaag te verplaatsen en de regels nieuwe nummers te geven, zodat deze altijd oplopen in stappen van 10. 

Er kunnen veel regels worden aangemaakt voor een vrijgegeven product. Om beter te begrijpen wat elke regel overschrijft en waarom dit nodig is, wordt het aangeraden om de **Rasterweergave** op de pagina **Standaard orderinstellingen** te gebruiken. U kunt de rasterweergave inschakelen door naar het actievenster **Opties** &gt; **Paginaopties** &gt; **Weergave wijzigen** &gt; **Rasterweergave** te gaan. In het raster kan een aanzienlijk aantal kolommen worden weergegeven, met name op de tabbladen voor verkoop en voorraad. U kunt het aantal in het raster zichbare kolommen beperken door groepen van kolommen te verbergen of weer te geven met de knoppen op de pagina **Standaardorderinstellingen** &gt; **Kolomweergave**.

### <a name="specific-order-settings-for-released-product-variant"></a>Specifieke orderinstellingen voor vrijgegeven productvarianten

Als het systeem van regels voor de standaardorderinstellingen te omslachtig wordt, is er de optie om eenvoudig voor elke productvariant standaardorderinstellingen te definiëren. In de volgende voorbeelden wordt getoond hoe dit eruit ziet voor het hierboven beschreven product en de verschillende scenario's.

| Positie | Vestiging | Configuratie | Opmaakmodel | Inkoop: Standaardinstellingen overschrijven | Inkoopdoorlooptijd | Inkoop: Gestopt | Verkoop: Standaardinstellingen overschrijven | Verkoop: Gestopt |
|------|------|---------------|-------|--------------------------------------|--------------------|--------------------|-----------------------------------|-----------------|
| 10   |      | C2            | R3    | Ja                                  | 5                  |                    |                                   |                 |
| 10   |      | C2            | R2    | Ja                                  | 5                  | Ja                | Ja                               | Ja             |
| 10   |      | C2            | R1    | Ja                                  | 5                  | Ja                | Ja                               | Ja             |
| 10   |      | C1            | R3    | Ja                                  | 2                  |                    |                                   |                 |
| 10   |      | C1            | R2    | Ja                                  | 2                  | Ja                | Ja                               | Ja             |
| 10   |      | C1            | R1    | Ja                                  | 2                  | Ja                | Ja                               | Ja             |
| 0    |      |               |       |                                      | 5                  |                    |                                   |                 |

De rang is in dit geval niet echt van belang, en u kunt ervoor kiezen om dit te verbergen. Deze oplossing brengt mogelijk problemen op gebied van onderhoud met zich mee. Het kan echter zinvol zijn om deze configuratie te overwegen, als u bijvoorbeeld ook een integratie met systemen voor productlevenscyclusbeheer als optie ziet.




