---
title: Standaardorderinstellingen voor dimensies en productvarianten
description: Standaardorderinstellingen definiëren de locatie en het magazijn waaruit de artikelen worden geleverd of waarin ze worden opgeslagen, de minimum-, maximum-, meervoud- en standaardhoeveelheden die voor handel of voorraadbeheer worden gebruikt, de levertijden, de eindevlag, en de methode voor orderbelofte.
author: johanhoffmann
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventItemOrderSetup, InventItemIdLookupByDefaultOrderSetting, EcoResProductReleasedStoppedAllChartPart, UnitTestPartitions
audience: Application User
ms.reviewer: kamaybac
ms.custom: 223084
ms.assetid: fbfbcd7b-dc75-44ab-bffc-8bad576804a4
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 2681a2a13754e240dcc4c99792dc47ae734f6e9e
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/29/2021
ms.locfileid: "7579419"
---
# <a name="default-order-settings-for-dimensions-and-product-variants"></a>Standaard orderinstellingen voor dimensies en productvarianten

[!include [banner](../includes/banner.md)]

Standaardorderinstellingen in Dynamics 365 Supply Chain Management definiëren de locatie en het magazijn waaruit de artikelen worden geleverd of waarin ze worden opgeslagen, de minimum-, maximum-, meervoud- en standaardhoeveelheden die voor handel of voorraadbeheer worden gebruikt, de levertijden, de eindevlag, en de methode voor orderbelofte. Standaardorderinstellingen worden gebruikt bij het maken van inkooporders, verkooporders, overboekingsorders, voorraadjournalen, en door de hoofdplanning voor het genereren van geplande orders. Standaardorderinstellingen kunnen specifiek zijn voor het artikel, de locatie, de productvariant of de productdimensie.

Voer de volgende stappen uit om de standaardorderinstellingen voor een product te definiëren.

1. Ga naar **Productgegevensbeheer** &gt; **Producten** &gt; **Vrijgegeven producten**.
1. Selecteer het relevante product in het raster.
1. Voer in het actievenster een van de volgende stappen uit om de pagina **Standaardorderinstellingen** voor het geselecteerde product te openen:

    - Selecteer op het tabblad **Plan** in de groep **Orderinstellingen** de optie **Standaardorderinstellingen**.
    - Selecteer op het tabblad **Voorraadbeheer** in de groep **Orderinstellingen** de optie **Standaardorderinstellingen**.

1. Configureer de instellingen zoals beschreven in de rest van dit onderwerp.

## <a name="default-order-settings"></a>Standaard orderinstellingen

Er zijn drie typen standaardorderinstellingen: voor inkoop, verkoop en voorraad. De standaardorderinstellingen voor inkoop worden gebruikt wanneer u de volgende items maakt:

- Inkooporderregels
- Inkoopovereenkomstregels
- Offerteaanvraagregels
- Regels op opdracht tot inkoop
- Aanvullingsregels van de consignatie (gedeeltelijk ondersteund, zie opmerking)
- Geplande inkooporders

> [!NOTE]
> Voor consignatieaanvullingsorderregels zijn de enige instellingen van het sneltabblad **Inkooporder** van de pagina **Standaard orderinstellingen** die van toepassing zijn, het veld **Standaardsite**, het veld **Standaardmagazijn** en het selectievakje **Gestopt**.

De standaardorderinstellingen voor verkoop worden gebruikt wanneer u de volgende items maakt:

- Verkooporderregels
- Verkoopovereenkomstregels
- Verkoopofferteregels
- Retourorderregels en regels voor artikelvervanging
- Vraagprognoseregels

De standaardorderinstellingen voor verkoop worden ook toegepast wanneer u de volgende items maakt:

- Projectartikelbehoeften
- Artikelbehoeften bij serviceorders

De standaardorderinstellingen voor voorraad worden gebruikt wanneer u de volgende items maakt:

- Voorraadjournalen
- overboekingsorders
- Geplande overboekingsorders

De standaardorderinstellingen voor voorraad worden ook toegepast wanneer u de volgende items maakt:

- Quarantaineorders
- Kwaliteitsorders
- Productieorders
- Stuklijstregels
- Geplande productieorders

## <a name="full-definition-of-a-released-product"></a>Volledige definitie van een vrijgegeven product

Wanneer u een transactie maakt, moet u de volledige definitie van een vrijgegeven product op de regel opgeven zodat Supply Chain Management de standaardorderinstellingen kan vaststellen. De volledige definitie van een vrijgegeven producten betekent dat het artikelnummer en alle actieve productdimensies, zoals configuratie, grootte, stijl, versie en kleur, worden opgegeven in de transactie. Als u bijvoorbeeld handmatig een inkooporderregel voor een vrijgegeven productvariant maakt, moet u alle vereiste productdimensies opgeven voordat de locatie, het magazijn, hoeveelheden en de levertijd standaard op de orderregel worden weergegeven. 

Niet alle parameters van de standaardorderinstellingen worden toegepast wanneer u een order of journaalregels maakt. Hoeveelheden en levertijden worden alleen standaard weergegeven wanneer dat kan. Bijvoorbeeld bij het tellen van een journaalregel worden alleen de locatie en het magazijn standaard weergegeven wanneer de regel wordt gemaakt. Daarom worden geen standaardhoeveelheid of controles op meerdere items en minimumhoeveelheden uitgevoerd wanneer de regel wordt gemaakt of het journaal wordt geboekt. 

Wanneer u een order of een journaalregel maakt, wordt altijd geprobeerd om een standaardlocatie en standaardmagazijn te vinden. De locatie wordt niet altijd standaard weergegeven vanuit de orderinstellingen. Wanneer u bijvoorbeeld een verkooporder of een inkooporder maakt, wordt de locatie van de orderkoptekst automatisch gebruikt in de orderregels. Wanneer u een stuklijstregel maakt, wordt de locatie van de koptekst van de stuklijst gebruikt. Nadat de locatie is bepaald, wordt deze gebruikt om eventuele locatiespecifieke orderinstellingen te vinden die daarna als standaardinstellingen voor het magazijn kunnen worden gebruikt. 

Het standaardordertype, de inkoop en de voorraadlevertijden kunnen worden overschreven door de behoefteplanningsregels van het artikel op de pagina **Artikelbehoefteplanning**. Hoewel de standaardorderinstellingen geen onderscheid kunnen maken tussen de doorlooptijden voor productie en die voor verplaatsing, kunnen de artikelbehoefteplanningsregels hier wel mee overweg. De instellingen voor artikelbehoefteplanning worden echter alleen gebruikt door hoofdplanning (MRP) bij het maken van geplande orders voor productie en transfer, niet wanneer u handmatig productie- en overboekingsorders maakt. 

## <a name="default-order-settings-rules"></a>Regels voor standaardorderinstellingen

U kunt algemene standaardorderinstellingen definiëren, evenals alle benodigde regels voor standaardorderinstellingen die alleen onder bepaalde voorwaarden gelden, zoals locatie of een bepaalde productdimensie of een combinatie van productdimensies. U kunt geen orderinstellingen definiëren die specifiek zijn voor het magazijn.

### <a name="rank-in-default-order-settings"></a>Rangen in standaardorderinstellingen

De regels voor standaardorderinstellingen kennen rangen. Hoe hoger de rang, des te belangrijker de regel is. Dit houdt in dat de regel een hogere prioriteit heeft en wordt toegepast vóór regels met een lagere rang. De algemene standaardorderinstellingen hebben de rang 0 (nul). Deze rang kan niet worden gewijzigd. Er kan slechts één regel zijn met rang 0. Regels kunnen dezelfde rang hebben, als ze worden toegepast op verschillende dimensies. Dit is nuttig wanneer u locatiespecifieke orderinstellingen modelleert. Wanneer een nieuwe regel voor standaardorderinstellingen wordt gemaakt, worden de waarden voor orderwaarden, eindevlag en dergelijke overgenomen van de regel met rang 0. Deze waarden kunnen worden overschreven.

### <a name="default-order-settings-for-released-products"></a>Standaardorderinstellingen voor vrijgegeven producten

Voor bepaalde vrijgegeven producten kunt u de algemene orderinstellingen of locatiespecifieke orderinstellingen definiëren. De algemene orderinstellingen hebben altijd rang 0. Als u nieuwe orderinstellingen voor verkoop, inkoop en voorraad tegelijk maakt, wordt het aangeraden om gebruik te maken van de weergave **Details** op de pagina **Standaard orderinstellingen**. Om over te schakelen naar de detailweergave gaat u naar het actievenster **Opties** &gt; **Paginaopties** &gt; **Weergave wijzigen** &gt; **Detailweergave**.

### <a name="site-specific-order-settings"></a>Locatiespecifieke orderinstellingen

Als u locatiespecifieke orderinstellingen wilt maken, selecteert u **Nieuw**. Vul in de **Detailweergave** de locatie in het veld **Locatie** in van de sectie **Instellingen van toepassing op**. Vul in de **Rasterweergave** de locatie in in de kolom **Locatie**. Aan de nieuwe regel wordt automatisch een nieuwe rangwaarde toegewezen die groter is dan 0 (nul). U kunt zoveel locatiespecifieke regels maken als nodig zijn. Om aan te geven dat ze even belangrijk zijn, kunt u dezelfde rangwaarde toewijzen aan alle locatiespecifieke regels.

Als u in de **Detailweergave** werkt, kunt u niet het overzicht van de regels krijgen die voor het artikel zijn gemaakt. Gebruik de knop **Lijst weergeven/verbergen** om overzichtsgegevens te zien. Wanneer een orderregel van een van de beschikbare typen wordt gemaakt en er geen locatie voor is opgegeven, zoekt Supply Chain Management naar een regel waarvoor geen locatie is opgegeven. Dit helpt bij het bepalen van een standaardlocatie op de orderregel. Deze locatie wordt vervolgens gebruikt om te zoeken naar een locatiespecifieke regel, waarin een standaardmagazijn kan zijn ingesteld. Dit magazijn wordt dan toegepast op de orderregel.

### <a name="specific-order-settings-for-product-dimension"></a>Specifieke orderinstellingen voor productdimensies

U kunt regels voor standaardorderinstellingen definiëren voor elke actieve productdimensie of voor een combinatie van actieve productdimensies. Als een productdimensieveld leeg wordt gelaten, geldt de regel voor alle waarden van de productdimensie. 

Hier volgt een voorbeeldproduct.

| Artikel                                                | Waarde                                   |
|-----------------------------------------------------|-----------------------------------------|
| **Productnaam**                                    | Foto-elektrische sensor                    |
| **Artikelnummer**                                     | XW56                                    |
| **Configuratie** (gebruikt om het type licht te modelleren) | C1-zichtbaar rood licht, C2-infrarood licht |
| **Versie** | V1, V2, V3                              |

Stel dat dit product niet is geproduceerd maar aangeschaft. Verder nemen we aan dat configuratie C1 vaker wordt gebruikt, zodat deze kortere levertijden heeft. 

Maak de volgende standaardorderinstellingen aan om dit scenario te modelleren.

| Positie | Locatie | Configuratie | Versie | Inkoop: Standaardinstellingen overschrijven | Inkoopdoorlooptijd | Inkoop: Gestopt | Verkoop: Standaardinstellingen overschrijven | Verkoop: Gestopt |
|------|------|---------------|-------|--------------------------------------|--------------------|--------------------|-----------------------------------|-----------------|
| 10   |      | C1            |       | Ja                                  | 2                  |                    |                                   |                 |
| 0    |      |               |       |                                      | 5                  |                    |                                   |                 |

Wanneer een inkooporderregel of een geplande inkooporder wordt aangemaakt voor artikel XW56, configuratie C1, wordt aangenomen dat de levertijd 2 is, ongeacht de versie of de locatie waar de regel is geplaatst. Stel dat alle versies zijn gestopt, met uitzondering van V3.

U kunt de volgende regels voor standaardorderinstellingen maken.

| Positie | Locatie | Configuratie | Versie | Inkoop: Standaardinstellingen overschrijven | Inkoopdoorlooptijd | Inkoop: Gestopt | Verkoop: Standaardinstellingen overschrijven | Verkoop: Gestopt |
|------|------|---------------|-------|--------------------------------------|--------------------|--------------------|-----------------------------------|-----------------|
| 20   |      |               | V2    | Ja                                  |                    | Ja                | Ja                               | Ja             |
| 20   |      |               | V1    | Ja                                  |                    | Ja                | Ja                               | Ja             |
| 10   |      | C1            |       | Ja                                  | 2                  |                    |                                   |                 |
| 0    |      |               |       |                                      | 5                  |                    |                                   |                 |

De twee regels voor het stoppen van de oude versies hebben dezelfde rang. Daarom zijn ze even belangrijk. Omdat beide regels een hogere rang hebben dan de regel voor configuratie C1, hebben ze voorrang op de regel voor configuratie C1. 

In dit voorbeeld wordt uitgelegd waarom de ran noodzakelijk is. Als de rang niet wordt gebruikt als u een inkooporder voor configuratie C1 en versie V2 maakt, zijn de twee regels voor V2 en C1 dubbelzinnig. Om de dubbelzinnigheid op te lossen, doorzoekt Supply Chain Management de regels in aflopende volgorde van rang en past de eerste toepasselijke regel toe die wordt gevonden. In het huidige voorbeeld krijgt de gebruiker een waarschuwing wanneer een inkooporderregel voor configuratie C1 en versie V2 wordt gemaakt. De melding zegt dat het artikel in de wachtstand is gezet vanwege de versiewaarde. Als de regel voor de configuratie een hogere rang zou hebben dan de regel voor de versie, zou het maken van een inkooporderregel voor configuratie C1 en versie V2 slagen en krijgt de gebruiker geen melding dat het artikel in de wachtstand staat. 

Bekijk de volgende regels voor standaardorderinstellingen eens.

| Positie | Locatie | Configuratie | Versie | Standaardsite | Standaardmagazijn | Inkoop: Standaard opslagdimensies overschrijven | Inkoopmagazijn |
|------|------|---------------|-------|--------------|-------------------|------------------------------------------------|--------------------|
| 20   | 2    |               |       |              |                   | Ja                                            | 22                 |
| 10   |      | C1            |  V2   |  2           |  21               |                                                |                    |
| 0    |      |               |       | 1            | 11                |                                                |                    |

Het systeem onderzoekt de set regels twee keer om de locatie en het magazijn te bepalen. Wanneer een inkooporderregel wordt gemaakt voor de configuratie van C1,versie V2, kan de locatie worden bepaald op basis van de regel met rang 10. Vervolgens wordt gezocht naar een regel voor locatie 2 om een magazijn te bepalen. Regel 20 wordt gevonden en omdat deze een hogere rang heeft, wordt het magazijn voor de inkooporderregel ingesteld op 22 en niet op 21.

Algemeen gesproken worden hogere rangen toegekend aan specifieke regels en regels voor dimensies die belangrijker dan andere dimensies zijn. Meer algemene regels krijgen lagere rangen. 

De regel met rang 0 dient als vangnet. Als geen andere regels van toepassing zijn, worden de standaardorderinstellingen van regel 0 gebruikt. 

Omdat het rangnummer zo belangrijk is, vindt u in het actievenster **Standaard orderinstellingen** functies om een regel omhoog of omlaag te verplaatsen en de regels nieuwe nummers te geven, zodat deze altijd oplopen in stappen van 10. 

Er kunnen veel regels worden aangemaakt voor een vrijgegeven product. Om beter te begrijpen wat elke regel overschrijft en waarom dit nodig is, wordt het aangeraden om de **Rasterweergave** op de pagina **Standaard orderinstellingen** te gebruiken. U kunt de rasterweergave inschakelen door naar **Opties** &gt; **Paginaopties** &gt; **Weergave wijzigen** &gt; **Rasterweergave** te gaan. In het raster kan een aanzienlijk aantal kolommen worden weergegeven, met name op de tabbladen voor verkoop en voorraad. U kunt het aantal in het raster zichbare kolommen beperken door groepen van kolommen te verbergen of weer te geven met de knoppen op de pagina **Standaardorderinstellingen** &gt; **Kolomweergave**.

### <a name="specific-order-settings-for-released-product-variant"></a>Specifieke orderinstellingen voor vrijgegeven productvarianten

Als het systeem van regels voor de standaardorderinstellingen te omslachtig wordt, is er de optie om voor elke productvariant standaardorderinstellingen te definiëren. In het volgende voorbeeld wordt getoond hoe dit eruit ziet voor het hierboven beschreven product en de verschillende scenario's.

| Positie | Locatie | Configuratie | Versie | Inkoop: Standaardinstellingen overschrijven | Inkoopdoorlooptijd | Inkoop: Gestopt | Verkoop: Standaardinstellingen overschrijven | Verkoop: Gestopt |
|------|------|---------------|-------|--------------------------------------|--------------------|--------------------|-----------------------------------|-----------------|
| 10   |      | C2            | V3    | Ja                                  | 5                  |                    |                                   |                 |
| 10   |      | C2            | V2    | Ja                                  | 5                  | Ja                | Ja                               | Ja             |
| 10   |      | C2            | V1    | Ja                                  | 5                  | Ja                | Ja                               | Ja             |
| 10   |      | C1            | V3    | Ja                                  | 2                  |                    |                                   |                 |
| 10   |      | C1            | V2    | Ja                                  | 2                  | Ja                | Ja                               | Ja             |
| 10   |      | C1            | V1    | Ja                                  | 2                  | Ja                | Ja                               | Ja             |
| 0    |      |               |       |                                      | 5                  |                    |                                   |                 |

De rang is in dit geval niet echt van belang, en u kunt ervoor kiezen om dit te verbergen. Deze oplossing brengt mogelijk problemen op gebied van onderhoud met zich mee. Het kan echter zinvol zijn om deze configuratie te overwegen, als u bijvoorbeeld ook een integratie met systemen voor productlevenscyclusbeheer als optie ziet.

## <a name="use-strict-or-standard-validation-of-default-order-quantities"></a>Strikte of standaardvalidatie van standaardorderhoeveelheden gebruiken

U kunt kiezen hoe strikt het systeem moet zijn bij het valideren van hoeveelheden die zijn ingevoerd in de **standaardorderinstellingen** voor een product. Wanneer u de nieuwe strikte optie gebruikt, moet de **standaardorderhoeveelheid** altijd een veelvoud zijn van de opgegeven **Meerdere** waarde voor inkooporders, voorraad en verkooporders. Als u strikte validatie gebruikt, kunt u geen standaardorderinstellingen opslaan die niet aan deze vereiste voldoen (en wordt een fout weergegeven op de berichtenbalk). 

Strikte validatie is van toepassing op **standaardorderhoeveelheden** die zijn opgegeven op de pagina's **Inkooporder**, **Voorraad** en **Verkooporder** van de pagina **Standaard orderinstellingen**. Elk sneltabblad heeft een eigen instelling **Meerdere**, die wordt gebruikt om de **standaardorderhoeveelheid** te valideren die voor dat sneltabblad is opgegeven.

### <a name="enable-the-strict-validation-option"></a>De strikte validatieoptie inschakelen

Voordat u de strikte validatieoptie kunt gebruiken, moet deze zijn ingeschakeld in uw systeem. Beheerders kunnen gebruikmaken van de pagina [Functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) om de status van de functie te controleren en deze zo nodig in te schakelen. Hier ziet u de functie als:

- **Module** - *Productgegevensbeheer*
- **Functienaam** - *Strikte validatie van standaardorderhoeveelheden*

### <a name="set-the-validation-option"></a>De validatieoptie instellen

De validatieoptie instellen:

1. Ga naar **Productgegevensbeheer \> Instellen \> Parameters productgegevensbeheer**.
1. Stel op het tabblad **Algemeen** **Validatie van standaardorderhoeveelheden** in op een van de volgende waarden:
    - **Strikt**: selecteer deze optie om ervoor te zorgen dat alle waarden voor de **standaardorderhoeveelheid** een veelvoud zijn van de waarde **Meerdere** voor elk sneltabblad (**Inkooporder**, **Voorraad** en **Verkooporder**).
    - **Standaard**: selecteer deze optie om standaardvalidatie te gebruiken (dit werkt hetzelfde als wanneer deze functie niet is ingeschakeld).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]