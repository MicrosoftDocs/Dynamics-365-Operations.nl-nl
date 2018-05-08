---
title: Intrastat
description: Dit artikel bevat informatie over Intrastat-rapportage voor de handel van goederen en, in sommige gevallen, diensten tussen landen en regio's van de Europese Unie (EU). Het biedt een overzicht van het rapportageproces en bevat een beschrijving van de vereiste instellingen en vereisten.
author: EvgenyPopovMBS
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: Intrastat
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 28581
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: epopov
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 2ee60f3d1155b89d342b94832fbdbe898a5063c6
ms.contentlocale: nl-nl
ms.lasthandoff: 04/13/2018

---

# <a name="intrastat"></a>Intrastat

[!include [banner](../includes/banner.md)]

Dit artikel bevat informatie over Intrastat-rapportage voor de handel van goederen en, in sommige gevallen, diensten tussen landen en regio's van de Europese Unie (EU). Het biedt een overzicht van het rapportageproces en bevat een beschrijving van de vereiste instellingen en vereisten.

Intrastat is het systeem voor het verzamelen van informatie en genereren van statistieken met betrekking tot de handel in artikelen tussen landen en regio's van de Europese Unie (EU). Intrastat-aangifte is vereist wanneer een product de grens van een ander EU-land/regio overschrijdt. In sommige landen/regio's is Intrastat-aangifte ook van toepassing op services. De verplichte en optionele elementen kunnen in Intrastat-aangiftes worden verzameld. De volgende elementen zijn verplicht: het btw-nummer van de partij die de informatie moet verstrekken, de referentieperiode, de stroom (ontvangst of verzending), de achtcijferige basisproductcode, de lidstaat van de partner (lidstaat van verzending voor ontvangsten en lidstaat van bestemming voor verzendingen), de waarde van de goederen, de hoeveelheid goederen (netto massa en bijkomende eenheid) en de aard van de transactie. Landen/regio's kunnen ook optionele elementen verzamelen in diverse situaties. Sommige optionele elementen zijn het land of de regio van herkomst, de leveringsvoorwaarden, de wijze van transport, een meer gedetailleerde basisproductcode dan CN8, de regio van herkomst voor verzendingen en de regio van bestemming voor ontvangsten, de statistische procedure, de statistische waarde, een omschrijving van de goederen, en de haven/de luchthaven waar het product wordt geladen/gelost.

## <a name="overview-of-the-intrastat-reporting-process"></a>Een overzicht van het Intrastat-aangifteproces
De volgende secties beschrijven de gehele stroom van informatie die wordt gebruikt voor Intrastat-aangifte.

### <a name="1-enter-a-transaction-that-crosses-the-border-of-another-eu-countryregion"></a>1. Voer een transactie in die de grens met een ander EU-land/regio overschrijdt.

Een klantfactuur, een vrije-tektsfactuur, een inkoopfactuur, een projectfactuur, een pakbon van de klant, een productontvangstbon van de leverancier of een transferorder worden alleen overgeboekt naar het Intrastat-journaal als het type land/regio van de bestemming (voor verzendingen) of verzending (op ontvangsten)**EU** is. Deze functie is uitgebreid voor Microsoft Dynamics 365 for Operations (1611). Met deze functie kunt u vrachtadressen voor een intracommunautaire transactie opgeven. Als een vrachtadres afwijkt van een zakelijk adres van de leverancier (of zakelijk adres van de klant voor retourorder), wordt deze informatie voor de Intrastat-aangifte gebruikt. Wanneer u een verkooporder, een vrije-tektsfactuur, een inkooporder, een leveranciersfactuur, een projectfactuur of een transferorder maakt, hebben sommige velden die aan buitenlandse handel zijn gerelateerd, standaardwaarden in de documentkoptekst of op de regel. De standaardtransactiecode wordt overgenomen uit het overeenkomstige veld op de pagina **Parameters buitenlandse handel**. De standaarbasisproductcode, het land/de regio van herkomst, en staat/provincie van herkomst worden opgehaald van het artikel. U kunt de standaardwaarden wijzigen en ook andere aan buitenlandse handel gerelateerde informatie invullen: de statistische procedure, de transportwijze en de haven.

### <a name="2-use-the-intrastat-journal-to-generate-information-about-trade-among-eu-countriesregions"></a>2. Met het Intrastat-journaal kunt u gegevens genereren over handel tussen landen en regio's van de EU.

Voor statistische doeleinden genereert u elke maand informatie over handel tussen de landen/regio's van de EU. U kunt transacties overboeken van een vrije-tekstfactuur, klantfactuur, klantpakbon, leveranciersfactuur, leverancierspakbon, projectfactuur of transferorder volgens de criteria voor overdracht die zijn geconfigureerd op de pagina **Parameters buitenlandse handel**. U kunt er ook voor kiezen transacties handmatig in te voeren. Overgeboekte transacties kunt u in het Intrastat-journaal handmatig bijwerken, als updates worden vereist. In specifieke omstandigheden die op de pagina **Compressie van Intrastat** worden geconfigureerd, kunt u de transacties in het Intrastat-journaal comprimeren. Sommige landen/regio's laten u een lage transactiedrempel toepassen. U kunt vervolgens transacties rapporteren die onder de opgegeven basisproductcode beneden deze drempel liggen. U kunt de basisproductcode op de bijbehorende Intrastat-journaalregels bijwerken, op basis van de instelling voor **Ondergrens** op de pagina **Parameters buitenlandse handel**. U kunt die transacties ook comprimeren, op basis van de instelling **Compressie van Intrastat**. U kunt valideren of de transacties in het Intrastat-journaal compleet zijn, op basis van de instelling **Instelling controleren** op de pagina **Parameters buitenlandse handel**. De gegevens in bijbehorende velden kunnen op volledigheid worden gecontroleerd: land/regio, staat of provincie, gewicht, basisproductcode, transactiecode, aanvullende eenheid, haven, oorsprong, leveringsvoorwaarden, transportwijze en btw-nummer. De transacties die niet zijn voltooid, worden gemarkeerd als zijnde niet geldig.

### <a name="3-use-the-intrastat-journal-to-report-information-about-trade-among-eu-countriesregions"></a>3. Met het Intrastat-journaal kunt u gegevens rapporteren over handel tussen landen en regio's van de EU.

Voor statistische doeleinden rapporteert u elke maand informatie over handel tussen de landen/regio's van de EU. U kunt de Intrastat-aangifte afdrukken, op basis van de instellingen **Toewijzing van rapportindeling** op de pagina **Parameters buitenlandse handel**. U kunt ook een elektronisch bestand genereren, op basis van de instellingen **Toewijzing van bestandsindeling** op de pagina **Parameters buitenlandse handel**. Zie de taakregistraties voor Intrastat-aangifte voor meer informatie over Intrastat-aangifte, waaronder de vereisten:

-   Een EU Intrastat-aangifte genereren
-   Transacties overboeken naar Intrastat
-   Vrachtadres opgeven voor een intracommunautaire transactie

## <a name="prerequisites"></a>Vereisten
In de volgende tabel ziet u de vereisten voor Intrastat-aangifte.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Vereiste</th>
<th>Beschrijving</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Adresinstelling</td>
<td>Configureer ISO-codes (International Organization for Standardization) voor de landen/regio's.</td>
</tr>
<tr class="even">
<td>Rechtspersoon</td>
<td>Configureer btw-nummers voor import/export, de filiaalnummerextensie voor import/export en de Intrastat-code die aan de rechtspersoon is toegewezen.</td>
</tr>
<tr class="odd">
<td>Productcategoriehiërarchie (verkopenhiërarchie, inkoophiërarchie)</td>
<td>Wijs de Intrastat-basisproductcodes toe aan de categorieknooppunten op het tabblad <strong>Basisproductcodes</strong> op de pagina <strong>Categoriehiërarchie</strong>. Wanneer u een basisproductcode aan een bovenliggende categorieknooppunt toewijst, is die code van toepassing op alle onderliggende categorieknooppunten. De geselecteerde basisproductcodes zijn beschikbaar in de weergave <strong>Geselecteerd</strong>, wanneer u een basisproductcode selecteert in de details van een vrijgegeven product, en op regels van verkooporders, inkooporders, en transferorders.</td>
</tr>
<tr class="even">
<td>Vrijgegeven productdetails</td>
<td>Configureer de volgende gegevens voor buitenlandse handel voor vrijgegeven producten:
<ul>
<li><strong>Basisproductcode</strong>: Selecteer deze in de lijst met geselecteerde basisproducten die is opgehaald uit de toegewezen productcategorieën, of in de volledige lijst van Intrastat-basisproductcodes.</li>
<li><strong>Statistieken toeslagenpercentage</strong></li>
<li><strong>Land/regio van oorsprong</strong>: Selecteer het standaardland/de standaardregio waar de goederen volledig werden verkregen of geproduceerd.</li>
<li><strong>Staat/provincie van oorsprong of bestemming</strong>: Selecteerd de standaardstaat/-provincie van bestemming voor ontvangsten en de staat/provincie van verzending.</li>
<li><strong>Nettogewicht in kg</strong></li>
</ul></td>
</tr>
<tr class="odd">
<td>Klanten</td>
<td>Configureer het afleveradres van de klant in het EU-land/de EU-regio.</td>
</tr>
<tr class="even">
<td>Leveranciers   </td>
<td>Configureer het adres van de leverancier in het EU-land/de EU-regio.</td>
</tr>
<tr class="odd">
<td>Diverse toeslagen</td>
<td>De code voor diverse toeslagen die moet worden opgenomen in het factuurbedrag, het statistische bedrag, of in beide. Op de pagina <strong>Toeslagcodes</strong>, op het tabblad <strong>Buitenlandse handel</strong>, schakelt u <strong>Intrastat-facturenwaarde</strong> in om het toeslagenbedrag toe te voegen aan de factuurwaarde, en schakelt u <strong>Statistische Infrastat-waarde</strong> in om het toeslagenbedrag toe te voegen aan de statistische waarde.</td>
</tr>
<tr class="even">
<td>Elektronische rapportage</td>
<td>Stel configuraties voor elektronische aangifte in om Intrastat-gegevens te exporteren in een elektronisch bestand met een door de relevante autoriteit vereiste indeling, en waarmee de Infrastat-gegevens kunnen worden weergegeven in een leesbare (gebruikersvriendelijke) indeling (bijvoorbeeld in Microsoft Excel).</td>
</tr>
<tr class="even">
<td>Magazijnbeheer</td>
<td>Koppel leveranciersrekeningen aan magazijncodes voor het invullen van het btw-nummer bij het overboeken van de transferorder.</td>
</tr>
</tbody>
</table>

## <a name="setup"></a>Instelling
De volgende secties beschrijven de instellingen die voor Intrastat-aangifte zijn vereist.

### <a name="set-up-all-required-intrastat-related-lists"></a>Alle vereiste aan Intrastat gerelateerde lijsten instellen

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Weergeven</th>
<th>Aanvullende gegevens</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Basisproductcodes</td>
<td>Stel een categoriehiërarchie in van het type <strong>Basisproductcode</strong> en voer alle basisproductcodes in volgens de gecombineerde nomenclatuurlijst. Voor elk basisproduct stelt u de volgende gegevens in:
<ul>
<li>De naam van het basisproduct en de basisproductcode</li>
<li>De beschrijvende naam en/of de vertaalde naam</li>
<li>Instellingen voor het rapporteren van aanvullende (bijkomende) eenheden op het tabblad <strong>Buitenlandse handel</strong> tabblad. U kunt de aanvullende eenheid in de eenheidslijst selecteren. U kunt ook opgeven of naast de geselecteerde aanvullende eenheid ook het gewicht van basisproducten moet worden gerapporteerd.</li>
</ul></td>
</tr>
<tr class="even">
<td>Transactiecodes</td>
<td>Stel de aard van de transactie in op basis van de vereisten van uw land/regio. Voor elke transactiecode die u instelt, moet u de regels configureren voor berekening van factuurbedragen en statistische bedragen voor transferorders en verkoop- of inkooporders.
<ul>
<li>Voor transferorders configureert u een van de volgende regels voor berekening van factuurbedragen en statistische bedragen:
<ul>
<li><strong>Leeg</strong>: Het bedrag is 0 (nul).</li>
<li><strong>Financiële kostprijs</strong>: Het bedrag is gelijk aan de financiële kosten.</li>
<li><strong>Totale kosten</strong>: Het bedrag is gelijk aan de totale kosten van de transactie.</li>
<li><strong>Handmatig</strong>: Het bedrag is gelijk aan het bedrag dat handmatig op de transferorderregel wordt opgegeven.</li>
</ul></li>
<li>Voor verkooporders en inkooporders configureert u een van de volgende regels voor berekening van factuurbedragen en statistische bedragen:
<ul>
<li><strong>Leeg</strong>: Het bedrag is 0 (nul).</li>
<li><strong>Factuurbedrag</strong>: Het bedrag is gelijk aan het bedrag dat voor het basisartikel is gefactureerd.</li>
<li><strong>Basisbedrag</strong>: Het bedrag is gelijk aan het bedrag dat zou worden gefactureerd voordat eventuele kortingen zijn toegepast.</li>
</ul></li>
</ul></td>
</tr>
<tr class="odd">
<td>Transportmethoden</td>
<td>Stel de transportwijze in op basis van de vereisten van uw land/regio. Voor elke leveringsmethode kunt u een standaardtransportmethode configureren op het tabblad <strong>Buitenlandse handel</strong>.</td>
</tr>
<tr class="even">
<td>Havens/luchthavens</td>
<td>Configureer de haven/luchthaven waar de goederen worden geladen of gelost, als deze informatie door uw land/regio wordt verzameld.</td>
</tr>
<tr class="odd">
<td>Statistiekprocedures</td>
<td>Configureer de statistische procedure als deze informatie door uw land/regio wordt verzameld.</td>
</tr>
</tbody>
</table>

### <a name="set-up-rules-for-compressing-intrastat-transactions"></a>Configureer regels voor het comprimeren van Intrastat-transacties

Op de pagina **Compressie van Intrastat** kunt u de velden selecteren die voor compressie moeten worden gebruikt. Alle transacties met dezelfde combinatie van waarden voor de geselecteerde velden in het Intrastat-journaal worden in één transactie gecomprimeerd, wanneer u de functie Comprimeren uitvoert in het Intrastat-journaal.

### <a name="set-up-foreign-trade-parameters"></a>Parameters voor buitenlandse handel instellen

Gebruik de pagina **Parameters buitenlandse handel** om de parameters in de volgende tabel in te stellen.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Tabblad</th>
<th>Parameters</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Algemeen</td>
<td><ul>
<li><strong>Algemeen</strong>: Geef de volgende informatie op:
<ul>
<li>De standaardtransactiecodes voor verkooporders, inkooporders, creditnota's en transferorders. De transactiecode die wordt ingesteld voor creditnota's wordt ook gebruikt als de code voor retouren van materiële goederen en voor afwijkende materiële retouren versus corrigerende creditnota's.</li>
<li>De werknemer die verantwoordelijk is voor het voorbereiden van Intrastat-aangiften.</li>
</ul></li>
<li><strong>Ondergrens</strong>: Geef de instellingen op voor het bijwerken van transacties die onder de drempel liggen:
<ul>
<li>Bedrag en gewicht van de drempel</li>
<li>De basisproductcode die wordt toegepast op transacties die onder de drempel liggen</li>
</ul></li>
<li><strong>Overboeken</strong>: Geef de criteria voor het overboeken van transacties naar het Intrastat-journaal. U kunt opgeven dat de transacties alleen mogen worden overgeboekt wanneer de artikelen aan een of alle van de volgende criteria voldoen:
<ul>
<li>De artikelen zijn geen serviceartikelen.</li>
<li>De artikelen hebben een basisproductcode.</li>
<li>De artikelen hebben een gewicht.</li>
<li>De artikelen hebben aanvullende eenheden.</li>
</ul></li>
<li><strong>Instelling contoleren</strong>: Geef de regels op voor het valideren van de volledigheid van Intrastat-gegevens. U kunt selecteren welke gegevens worden gevalideerd.</li>
<li><strong>Afrondingsregels</strong>: Geef de volgende instellingen op voor afrondingsbedragen en gewichten in Intrastat-aangifte:
<ul>
<li>De afrondingsregel (precisie)</li>
<li>De afrondingsmethode: naar boven, naar beneden of normaal</li>
<li>Het aantal decimalen voor bedragen en gewichten</li>
<li>Instructies voor het afronden van gewichten die kleiner dan 1 kilogram (kg) zijn: naar 1 kg, normaal of geen afronding</li>
</ul></li>
<li><strong>Elektronische aangifte</strong>: Geef verwijzingen op naar configuraties voor elektronische aangifte, zodat u een elektronisch bestand en een rapport kunt genereren.</li>
<li><strong>Hiërarchie van basisproductcodes</strong>: Geef de categoriehiërarchie op van het type <strong>basisproductcode</strong> dat Intrastat-basisproductcode CN8 vertegenwoordigt.</li>
</ul></td>
</tr>
<tr class="even">
<td>Contactgegevens van medewerkers</td>
<td>Geef de naam, het adres, btw-nummer, telefoonnummer en faxnummer van de medewerker op.</td>
</tr>
<tr class="odd">
<td>Land-/regio-eigenschappen</td>
<td>Stel het land/de regio van de huidige rechtspersoon in op <strong>Binnenlands</strong>. Stel het land of de regio van de landen/regio's in de EU, die deelnemen aan EU-handel met de huidige rechtspersoon, in op <strong>EU</strong>. Voor elk land/regio geeft u ook de land-/regiocode voor buitenlandse handelsdoeleinden op.</td>
</tr>
<tr class="even">
<td>Nummerreeks</td>
<td>Geef het volgnummer op voor het Intrastat-journaal.</td>
</tr>
</tbody>
</table>






