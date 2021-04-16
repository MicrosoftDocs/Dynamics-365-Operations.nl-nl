---
title: Uw organisatiehiërarchie plannen
description: Voordat u de installatieorganisaties en -hiërarchieën instelt, moet u begrijpen hoe u uw bedrijf het beste modelleert.
author: sericks007
ms.date: 02/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: OMHierarchyManager, OMLegalEntity, OMOperatingUnit
audience: Application User
ms.reviewer: sericks
ms.custom: 17404
ms.assetid: babde0c6-bb5d-45ae-95ca-2af75a0ea292
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ec071844f09caca1c83ff35a75b26922c6185c5b
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/31/2021
ms.locfileid: "5747580"
---
# <a name="plan-your-organizational-hierarchy"></a>Uw organisatiehiërarchie plannen

[!include [banner](../includes/banner.md)]

Voordat u de installatieorganisaties en organisatiehiërarchieën instelt, moet u plannen hoe uw bedrijf wordt gemodelleerd. Het organisatiemodel heeft een aanzienlijk effect op de implementatie en op bedrijfsprocessen.

Met organisatiehiërarchieën worden de relaties aangegeven tussen de organisaties waaruit een bedrijf bestaat. Daarom is de structuur van uw bedrijf de meest belangrijke beslissing wanneer u organisaties modelleert. We bevelen u aan om organisatiestructuren te definiëren op basis van de feedback van leidinggevenden en topmanagers uit functiegebieden zoals Finance en Accounting, Human resources, Operations en Verkoop en marketing.

Wanneer u hiërarchieën plant, is het ook van belang om de relatie tussen de organisatiehiërarchie en de financiële dimensies te overwegen. U kunt meerdere organisatiehiërarchieën instellen die verschillende weergaven van het bedrijf weerspiegelen. Via financiële dimensies kunt u rapporten maken die op deze weergaven worden gebaseerd. Werk met uw partner om hiërarchieën te maken die zowel aan zakelijke als wettelijke rapportagevereisten voldoen.

> [!NOTE]
> Hoewel u financiële dimensies kunt gebruiken om rechtspersonen te vertegenwoordigen zonder de entiteiten te maken, zijn financiële dimensies niet bedoeld om de operationele of zakelijke belangen van rechtspersonen te voldoen. De boekhouding tussen eenheden-functie is ontworpen om alleen met de boekhoudkundige vermeldingen te werken die door de transactie worden gemaakt.

> [!IMPORTANT]
> Baseer uw planning voor modelorganisatie niet alleen op de informatie in dit artikel. Deze documentatie is een handleiding. Daarom kunt u ook met uw Partner werken voor meer advies. Uw Partner heeft ervaring opgebouwd in verschillende sectoren bij verschillende klanten.

## <a name="decide-whether-to-model-internal-organizations-as-legal-entities-or-operating-units"></a>Beslis of u interne organisaties als rechtspersonen of operationele eenheden wilt modelleren

U moet ten minste één rechtspersoon hebben die uw bedrijf vertegenwoordigd. Een rechtspersoon kan wettelijk bindende overeenkomsten aangaan en is verplicht financieele overzichten te overleggen.

Rechtspersonen kunnen worden gebruikt voor transactiezaken of voor consolidatie. Dit betekent dat een rechtspersoon in Finance and Operations niet noodzakelijkerwijs een echte rechtspersoon in uw bedrijf vertegenwoordigt. Bijvoorbeeld, een bedrijf dat aan transacties deelneemt kan over dochtermaatschappijen beschikken. In dit scenario, is een rechtspersoon vereist voor transacties, en een virtuele rechtspersoon is vereist om de resultaten en de saldi van de dochtermaatschappijen te consolideren.

De interne organisaties in uw bedrijf, zoals regionale kantor, kunnen als extra rechtspersonen, of als operationele eenheden van de belangrijkste rechtspersoon worden weergegeven. Een operationele eenheid is niet vereist om een wettelijk gedefinieerde organisatie te zijn. De operationele eenheden worden gebruikt om economische middelen en operationele processen in het bedrijf te controleren. Afdelingen en kostenplaatsen zijn bijvoorbeeld operationele eenheden.

Sommige functies werken anders afhankelijk van of de organisatie een rechtspersoon of operationele eenheid is. Overweeg zorgvuldig de hieronder beschreven functies terwijl u uw keuze maakt.

### <a name="master-data"></a>Hoofdgegevens

#### <a name="if-the-organization-is-modeled-as-a-legal-entity"></a>Als de organisatie als rechtspersoon is gemodelleerd

Sommige hoofdgegevens, zoals klanten, betalingstermijnen, belastingdiensten, en lokale bestellingen, moeten worden ingesteld voor elke rechtspersoon. Enkele hoofdgegevens, zoals gebruikers, producten, en de meeste personeelsgegevens, worden gedeeld door alle rechtspersonen.

#### <a name="if-the-organization-is-modeled-as-an-operating-unit"></a>Als de organisatie als operationele eenheid wordt gemodelleerd

Hoofdgegevens worden gedeeld door de operationele eenheden.

### <a name="module-parameters"></a>Moduleparameters

#### <a name="if-the-organization-is-modeled-as-a-legal-entity"></a>Als de organisatie als rechtspersoon is gemodelleerd

Parameters voor modules, zoals de Debiteuren-parameters, Crediteuren-parameters en contanten en de Contant- en bankbeheer-parameters moet worden ingesteld per rechtspersoon. Omdat de moduleinstallatie voor rechtspersonen afzonderlijk is, kan elke dochtermaatschappij voldoen aan lokale wettelijke verplichtingen en bedrijfspraktijken. Bijvoorbeeld, een rechtspersoon voor bedrijfsdiensten en een rechtspersoon voor productie kunnen verschillende moduleparameters hebben, zelfs als ze aan hetzelfde moederbedrijf rapporteren.

#### <a name="if-the-organization-is-modeled-as-an-operating-unit"></a>Als de organisatie als operationele eenheid wordt gemodelleerd

De moduleparameters worden gedeeld door de operationele eenheden.

### <a name="data-security"></a>Gegevensbeveiliging

#### <a name="if-the-organization-is-modeled-as-a-legal-entity"></a>Als de organisatie als rechtspersoon is gemodelleerd

De meeste gegevens worden automatisch beveiligd door bedrijfs-id Een bedrijf-id is een unieke id voor de gegevens die zijn gekoppeld aan de rechtspersoon. Een bedrijf kan aan slechts één type rechtspersoon worden gekoppeld en een rechtspersoon kan aan slechts één bedrijf worden gekoppeld. Gebruikers hebben alleen toegang tot de gegevens van bedrijven waartoe ze toegang hebben. U hoeft geen aanpassingen uit te voeren om gegevens te beschermen door bedrijfs-id

#### <a name="if-the-organization-is-modeled-as-an-operating-unit"></a>Als de organisatie als operationele eenheid wordt gemodelleerd

De gegevens kunnen per operationele eenheid worden beveiligd door aangepast gegevensbeveiligingsbeleid te maken. Gegevensbeveiligingsbeleid wordt gebruikt om toegang tot gegevens te beperken. Bijvoorbeeld, stel dat een gebruiker alleen inkooporders in een bepaalde operationele eenheid mag maken. Gegevensbeveiligingsbeleid kan worden gemaakt om de gebruiker de toegang te weigeren tot de gegevens van een inkooporder van een andere operationele eenheid. Het volume van het aantal transacties en de hoeveelheid beveiligingsbeleid kunnen prestaties negatief beïnvloeden. Wanneer u beveiligingsbeleid hebt ontworpen, houd u dan rekening met de prestaties.

### <a name="ledgers"></a>Grootboeken

#### <a name="if-the-organization-is-modeled-as-a-legal-entity"></a>Als de organisatie als rechtspersoon is gemodelleerd

Elke rechtspersoon vereist een grootboek dat een rekeningschema, valuta voor boekhouding, aangiftevaluta en fiscale kalender levert. Een balans kan alleen worden gemaakt voor een rechtspersoon. Hoofdrekeningen, dimensies, rekeningstructuren, rekeningschema's en rekeningregels kunnen door meerdere rechtspersonen worden gebruikt.

#### <a name="if-the-organization-is-modeled-as-an-operating-unit"></a>Als de organisatie als operationele eenheid wordt gemodelleerd

Een operationele eenheid kan niet zijn eigen grootboekgegevens hebben. Als uw interne organisaties geen unieke grootboeken vereisen, kunt u deze als operationele eenheden modelleren. De grootboekgegevens worden ingesteld voor de hoofdrechtspersoon in de hiërarchie. De resultatenrekeningen kunnen voor operationele eenheden binnen een rechtspersoon of voor de hoofdrechtspersoon worden gemaakt.

### <a name="fiscal-calendars"></a>Fiscale kalenders

#### <a name="if-the-organization-is-modeled-as-a-legal-entity"></a>Als de organisatie als rechtspersoon is gemodelleerd

Elke rechtspersoon heeft zijn eigen fiscale kalender. Als uw interne organisaties andere boekjaren en fiscale kalenders gebruiken, moet u de organisaties als rechtspersonen modelleren.

#### <a name="if-the-organization-is-modeled-as-an-operating-unit"></a>Als de organisatie als operationele eenheid wordt gemodelleerd

De operationele eenheden moeten een fiscale kalender delen. Als uw interne organisaties dezelfde fiscale jaren en de fiscale kalenders gebruiken, kunt u de organisaties als operationele eenheden modelleren.

### <a name="consolidation"></a>Consolidatie

#### <a name="if-the-organization-is-modeled-as-a-legal-entity"></a>Als de organisatie als rechtspersoon is gemodelleerd

U moet de financiële resultaten voor regionale kantoren in één geconsolideerd bedrijf consolideren om financiële overzichten voor te bereiden.

#### <a name="if-the-organization-is-modeled-as-an-operating-unit"></a>Als de organisatie als operationele eenheid wordt gemodelleerd

De consolidatie is niet vereist, omdat de gegevens al onder operationele eenheden worden gedeeld.

### <a name="centralized-payments"></a>Gecentraliseerde betalingen

#### <a name="if-the-organization-is-modeled-as-a-legal-entity"></a>Als de organisatie als rechtspersoon is gemodelleerd

De centrale betalingen moeten zijn ingesteld zodat de facturen voor alle onderliggende rechtspersonen naar of van een alleenstaande bovenliggende rechtspersoon kunnen worden betaald.

#### <a name="if-the-organization-is-modeled-as-an-operating-unit"></a>Als de organisatie als operationele eenheid wordt gemodelleerd

De gecentraliseerde betalingen zijn niet vereist omdat alle facturen in één rechtspersoon worden geregistreerd.

### <a name="intercompany-transactions"></a>Intercompany-transacties

#### <a name="if-the-organization-is-modeled-as-a-legal-entity"></a>Als de organisatie als rechtspersoon is gemodelleerd

De intercompany-verkooporders, inkooporders, betalingen, of de ontvangsten kunnen op elkaar worden toegepast. U hoeft geen journaalboekstukken gebruiken. U kunt op het subadministratieniveau intercompany-transacties (Klanten, Leveranciers) bekijken. De volgende voorbeelden illustreren hoe de intercompany-transacties worden verwerkt.

##### <a name="example-1-headquarters-provides-services-to-regional-offices-and-must-charge-the-costs-of-those-services-to-the-regional-offices"></a>Voorbeeld 1: Het hoofdkantoor biedt diensten aan regionale kantoren en moet de kosten van deze diensten aan de regionale kantoren in rekening brengen

Als u het regionaal kantoor als rechtspersoon modelleert, hebt u de volgende opties:

- Het hoofdkantoor maakt een journaalpost voor het gekruist in rekening brengen van de onkosten aan het regionale kantoor. De transacties kunnen niet in het verleden worden gemaakt.
- Het hoofdkantoor dient een inkooporder voor de services in bij het regionale kantoor. Een verkooporder wordt automatisch gemaakt in de rechtspersoon van het regionale kantoor, met intercompany-subgrootboektransacties.

##### <a name="example-2-headquarters-procures-and-pays-for-service-that-is-delivered-to-a-regional-office"></a>Voorbeeld 2: Het hoofdkantoor neemt een service af en betaalt voor die service die aan een regionaal kantoor wordt geleverd

Als u het regionaal kantoor als rechtspersoon modelleert, hebt u de volgende opties:

- De factuur en de betaling volgen de wettelijke vereisten van het hoofdkantoor. Het Hoofdkantoor kan een journaalpost maken voor het gekruist in rekening brengen van de onkosten aan het regionale kantoor. De transacties kunnen niet in het verleden worden gemaakt.
- De factuur en de betaling volgen de wettelijke vereisten van het hoofdkantoor. Het hoofdkantoor kan een intercompany-subgrootboektransactie maken.

#### <a name="if-the-organization-is-modeled-as-an-operating-unit"></a>Als de organisatie als operationele eenheid wordt gemodelleerd

Intercompany-transacties binnen operationele eenheden worden alleen ondersteund met journaalboekstukken. Een operationele eenheid kan geen inkooporder, een verkooporder, of een factuur uitgeven of ontvangen voor een andere operationele eenheid in dezelfde rechtspersoon. U kunt intercompany-transacties niet op het subgrootboekniveau (Klanten, Leveranciers) bekijken. De volgende voorbeelden illustreren hoe de intercompany-transacties worden verwerkt.

##### <a name="example-1-headquarters-provides-services-to-regional-offices-and-must-charge-the-costs-of-those-services-to-the-regional-offices"></a>Voorbeeld 1: Het hoofdkantoor biedt diensten aan regionale kantoren en moet de kosten van deze diensten aan de regionale kantoren in rekening brengen

Als u het regionaal kantoor als operationele eenheid modelleert, voert het hoofdkantoor een onkostentransactie in en codeert dit naar het regionaal kantoor.

##### <a name="example-2-headquarters-procures-and-pays-for-service-that-is-delivered-to-a-regional-office"></a>Voorbeeld 2: Het hoofdkantoor neemt een service af en betaalt voor die service die aan een regionaal kantoor wordt geleverd

Als u het kantoor modelleert als regionaal kantoor, volgen de factuur en de betaling de wettelijke vereisten van het hoofdkantoor. De factuur kan gecodeerd worden naar het regionaal kantoor. Gebruik op het inkomensoverzicht een financiële om de kosten van het regionaal kantoor te rapporteren.

### <a name="local-tax-requirements"></a>Lokale belastingeisen

#### <a name="if-the-organization-is-modeled-as-a-legal-entity"></a>Als de organisatie als rechtspersoon is gemodelleerd

Een rechtspersoon is onderworpen aan de belastingwetgevingen van de belastingdienst in het land/regio waar de rechtspersoon wordt geregistreerd. Bijvoorbeeld, een rechtspersoon in Denemarken is geregistreerd valt onder de Deense belastingwetgevingen en regelgeving. Een rechtspersoon kan tot slechts één land/regio behoren. Via het land/regio dat u selecteert voor het hoofdadres van de rechtspersoon, worden de land-/regiospecifieke functies bepaald die beschikbaar zijn voor de rechtspersoon. Wanneer bijvoorbeeld het primaire adres van de rechtspersoon in Denemarken is, komen functies gerelateerd aan Deense belasting- en regelgevingen beschikbaar. Indien uw organisaties in verschillende landen/regio's en lokale zijn en verschillende lokale belastingopties vereisen, moet u de organisaties als wettelijke afzonderlijke rechtspersonen opzetten.

#### <a name="if-the-organization-is-modeled-as-an-operating-unit"></a>Als de organisatie als operationele eenheid wordt gemodelleerd

De operationele eenheden gebruiken de context van het land van de hoofdrechtspersoon. De operationele eenheden in dezelfde rechtspersoon kunnen geen andere land/regiogebonden vereisten hebben. Als uw organisaties in hetzelfde land/regio zijn en dezelfde belastingopties gebruiken, kunt u deze als operationele eenheden instellen.

### <a name="statutory-reporting-for-a-countryregion"></a>Wettelijke rapportage voor een land/regio

#### <a name="if-the-organization-is-modeled-as-a-legal-entity"></a>Als de organisatie als rechtspersoon is gemodelleerd

Voor landen/regio's die ondersteund worden, kunnen de meeste wettelijke rapporten worden gemaakt. 

> [!NOTE]
> Een boekingslaag in het grootboek stelt u in staat tot het aanpassingsvermeldingen in een overkoepelend bedrijf te maken dat een andere boekhoudingsnorm dan het onderliggende bedrijf gebruikt. Bijvoorbeeld, voor een bedrijf dat algemeen geaccepteerde boekhoudkundige praktijken in het Verenigd Koninkrijk (UK GAAP) gebruikt, kunt u aanpassingsvermeldingen maken in de boekingslaag. Deze boekingen kunnen in een moederbedrijf worden geconsolideerd dat algemeen geaccepteerde boekhoudprincipes (GAAP) in de Verenigde Staten gebruikt. De wijzigingsvermeldingen beïnvloeden Britse GAAP-rapportage niet.

#### <a name="if-the-organization-is-modeled-as-an-operating-unit"></a>Als de organisatie als operationele eenheid wordt gemodelleerd

De wettelijke rapporten moet worden gemaakt door een andere toepassing te gebruiken. U moet ervoor zorgen dat de gegevens in Finance and Operations-apps worden vastgelegd om de vereisten van elke operationele eenheid te ondersteunen, waar deze van de behoeften van het hoofdkantoor verschillen.

### <a name="currency"></a>Valuta

#### <a name="if-the-organization-is-modeled-as-a-legal-entity"></a>Als de organisatie als rechtspersoon is gemodelleerd

Als uw organisaties verschillende functionele valuta moeten gebruiken, moet u de organisaties als rechtspersonen modelleren. De gebruikte valuta worden ingesteld per rechtspersoon. Echter, u kunt transacties in meerdere valuta invoeren.

#### <a name="if-the-organization-is-modeled-as-an-operating-unit"></a>Als de organisatie als operationele eenheid wordt gemodelleerd

Als uw organisaties één functionele valuta gebruiken, kunt u de organisaties als operationele eenheden modelleren. De operationele eenheden moeten een functionele valuta hebben. Echter, u kunt transacties invoeren en rapporten in meerdere valuta maken.

### <a name="year-end-closing"></a>Jaarafsluiting

#### <a name="if-the-organization-is-modeled-as-a-legal-entity"></a>Als de organisatie als rechtspersoon is gemodelleerd

Als de wettelijke- en boekhoudingsverantwoordingsmethoden verschillen in de landen/regio's waarin uw organisaties zich bevinden, zijn er misschien verschillende jaareindeprocedures per organisatie vereist. Dit betekent dat u de organisaties als rechtspersonen moet modelleren. Elke rechtspersoon heeft een eigen jaareindeprocedures.

#### <a name="if-the-organization-is-modeled-as-an-operating-unit"></a>Als de organisatie als operationele eenheid wordt gemodelleerd

Als de wettelijke- en boekhoudingsverantwoordingsmethoden gelijk zijn in de landen/regio's waarin uw organisaties zich bevinden, kunt u een set van jaareindeprocedures gebruiken. Dit betekent dat u de organisaties als operationele eenheden kunt modelleren. Alle operationele eenheden moeten dezelfde jaarafsluitingsprocedure gebruiken.

### <a name="number-sequences"></a>Nummerreeksen

#### <a name="if-the-organization-is-modeled-as-a-legal-entity"></a>Als de organisatie als rechtspersoon is gemodelleerd

De nummerreeksen voor sommige verwijzingen kunnen worden ingesteld per rechtspersoon. Sommige nummerreeksen kunnen worden gedeeld.

#### <a name="if-the-organization-is-modeled-as-an-operating-unit"></a>Als de organisatie als operationele eenheid wordt gemodelleerd

De nummerreeksen voor sommige verwijzingen kunnen worden ingesteld per operationele eenheid. Sommige nummerreeksen kunnen worden gedeeld.

### <a name="products"></a>Producten

#### <a name="if-the-organization-is-modeled-as-a-legal-entity"></a>Als de organisatie als rechtspersoon is gemodelleerd

Productdefinities zijn gedeeld en ze moeten beschikbaar worden gemaakt voor individuele rechtspersonen voordat ze in transacties kunnen worden opgenomen. Elke rechtspersoon heeft een eigen set van vrijgegeven producten die in transactiedocumenten kunnen worden opgenomen. Als uw interne organisaties verschillende sets van producten moeten gebruiken, moet u de organisaties als rechtspersonen modelleren.

> [!NOTE]
> Alhoewel productdefinities zijn gedeeld, kunt u in elke rechtspersoon waarin een product is vrijgegeven, verschillende verkoop-, inkoop-, en voorraadparameters voor het artikel op elke voorraadsite opgeven.

#### <a name="if-the-organization-is-modeled-as-an-operating-unit"></a>Als de organisatie als operationele eenheid wordt gemodelleerd

Alle operationele eenheden delen dezelfde reeks producten. Als uw interne organisaties dezelfde reeks producten kunnen delen, kunt u de organisaties als operationele eenheden modelleren.

### <a name="inquiry-and-reporting"></a>Query en rapportage

#### <a name="if-the-organization-is-modeled-as-a-legal-entity"></a>Als de organisatie als rechtspersoon is gemodelleerd

U moet handmatig bedrijven wijzigen om transacties in te voeren en query's in meerdere rechtspersonen uit te voeren. Vanwege gegevensbeveiliginggrenzen, kan geconsolideerde query en rapportage bronintensief en tijdrovend zijn.

#### <a name="if-the-organization-is-modeled-as-an-operating-unit"></a>Als de organisatie als operationele eenheid wordt gemodelleerd

U hoeft niet van bedrijf te wisselen voor toegang tot gegevens van meerdere operationele eenheden. Geconsolideerde query en rapportage en afzonderlijke regionale query is sneller en eenvoudiger.

## <a name="best-practices-for-modeling-organizations-and-hierarchies"></a>Beste praktijken bij het modelleren van organisaties en hiërarchieën

Houd rekening met de volgende beste praktijken wanneer u een organisatiehiërarchie implementeert:

- Maak een afdeling om de doorsnede tussen een rechtspersoon en een bedrijfseenheid te modelleren. U kunt vervolgens gegevens vergaderen van een afdeling naar een rechtspersoon voor wettelijke aangiften en van een afdeling naar een bedrijfseenheid voor interne rapportage. Afdelingen kunnen als kostenplaatsen worden gebruikt. Als u afdelingen gebruikt, hoeft u niet zowel rechtspersonen als bedrijfseenheden te gebruiken als dimensies in de rekeningstructuur. U kunt gewoon afdelingen als een dimensie gebruiken. U moet zowel kostenplaatsen als afdelingen gebruiken als dimensies in de rekeningstructuur als kostenplaatsen alleen worden gebruikt als kostenaccumulatoren en afdelingen worden gebruikt voor verantwoording van opbrengsten.
- Modelleer meerdere hiërarchieën voor operationele eenheden als u complexe vereisten hebt voor de aangifte van winst en verlies.
- Modelleer geen meerdere hiërarchieën voor hetzelfde hiërarchiedoel in één rechtspersoon.
- Maak geen hiërarchie voor elk doel. Gewoonlijk kunt u één hiërarchie voor meerdere doelen gebruiken. Eén hiërarchie van operationele eenheden kan bijvoorbeeld aan alle beleidsdoelen worden toegewezen.
- Gebalanceerde hiërarchieën maken. In een hiërarchie worden alle knooppunten die zich op dezelfde afstand van het basisknooppunt bevatten als een niveau gedefinieerd. In een gebalanceerde hiërarchie kan slechts één type operationele eenheid voorkomen op elk niveau en de afstand tussen het basisknooppunt en het niveau is consistent. Als er tussenniveaus zijn tussen een afdeling en een rechtspersoon of bedrijfseenheid, zijn er mogelijk placeholderorganisaties vereist om een gebalanceerde hiërarchie te maken.
- Modelleer geen afzonderlijke hiërarchie van operationele eenheden als de structuur voor rechtspersonen ook uw operationele structuur is. Een gemengde hiërarchie van rechtspersonen en operationele eenheden kan voor beide doeleinden worden gebruikt.
- Voordat u belangrijke herstructureringsscenario´s modelleert, gebruikt u de ingangsdatums van de hiërarchie om een impactanalyse en een validatietest uit te voeren.
- Gebruik conceptmodus om een hiërarchie te wijzigen voordat u een nieuwe versie in een productieomgeving publiceert.
- Beperk het aantal mensen met machtigingen om organisaties toe te voegen of te verwijderen uit een hiërarchie in een productieomgeving. Een kleiner aantal beperkt de kans dat kostbare fouten optreden en correcties moeten worden uitgevoerd.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
