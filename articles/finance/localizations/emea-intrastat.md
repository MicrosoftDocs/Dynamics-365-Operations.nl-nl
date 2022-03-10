---
title: Intrastat-overzicht
description: Dit onderwerp bevat informatie over Intrastat-rapportage voor de handel van goederen en, in sommige gevallen, diensten tussen landen en regio's van de Europese Unie (EU).
author: EvgenyPopovMBS
ms.date: 01/13/2021
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: Intrastat
audience: Application User
ms.reviewer: kfend
ms.custom:
- "28581"
- intro-internal
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: epopov
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 97c2b4068f3b8d38281e637ec80f04b19d19be61
ms.sourcegitcommit: 3754d916799595eb611ceabe45a52c6280a98992
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2022
ms.locfileid: "7986032"
---
# <a name="intrastat-overview"></a>Intrastat-overzicht

[!include [banner](../includes/banner.md)]

Dit onderwerp bevat informatie over Intrastat-rapportage voor de handel van goederen en, in sommige gevallen, diensten tussen landen en regio's van de Europese Unie (EU). Dit onderwerp bevat ook een overzicht van het rapportageproces en bevat een beschrijving van de vereiste instellingen en vereisten.

Intrastat is het systeem voor het verzamelen van informatie en genereren van statistieken met betrekking tot de handel in artikelen tussen landen en regio's van de Europese Unie (EU). Intrastat-aangifte is vereist wanneer een product de grens van een ander EU-land/regio overschrijdt. In sommige landen/regio's is Intrastat-aangifte ook van toepassing op services. De verplichte en optionele elementen kunnen in Intrastat-aangiftes worden verzameld. De volgende elementen zijn verplicht: het btw-nummer van de partij die de informatie moet verstrekken, de referentieperiode, de stroom (ontvangst of verzending), de achtcijferige basisproductcode, de lidstaat van de partner (lidstaat van verzending voor ontvangsten en lidstaat van bestemming voor verzendingen), de waarde van de goederen, de hoeveelheid goederen (netto massa en bijkomende eenheid) en de aard van de transactie. Landen/regio's kunnen ook optionele elementen verzamelen in diverse situaties. Sommige optionele elementen zijn het land of de regio van herkomst, de leveringsvoorwaarden, de wijze van transport, een meer gedetailleerde basisproductcode dan CN8, de regio van herkomst voor verzendingen en de regio van bestemming voor ontvangsten, de statistische procedure, de statistische waarde, een omschrijving van de goederen, en de haven/de luchthaven waar het product wordt geladen/gelost.

## <a name="overview-of-the-intrastat-reporting-process"></a>Een overzicht van het Intrastat-aangifteproces
De volgende secties beschrijven de gehele stroom van informatie die wordt gebruikt voor Intrastat-aangifte.

### <a name="enter-a-transaction-that-crosses-the-border-of-another-eu-countryregion"></a>Voer een transactie in die de grens met een ander EU-land/regio overschrijdt.

Een klantfactuur, een vrije-tektsfactuur, een inkoopfactuur, een projectfactuur, een pakbon van de klant, een productontvangstbon van de leverancier of een transferorder worden alleen overgeboekt naar het Intrastat-journaal als het type land/regio van de bestemming (voor verzendingen) of verzending (op ontvangsten)**EU** is. Deze functie is uitgebreid voor Microsoft Dynamics 365 for Operations (1611). Met deze functie kunt u vrachtadressen voor een intracommunautaire transactie opgeven. Als een vrachtadres afwijkt van een zakelijk adres van de leverancier (of zakelijk adres van de klant voor retourorder), wordt deze informatie voor de Intrastat-aangifte gebruikt. Wanneer u een verkooporder, een vrije-tektsfactuur, een inkooporder, een leveranciersfactuur, een projectfactuur of een transferorder maakt, hebben sommige velden die aan buitenlandse handel zijn gerelateerd, standaardwaarden in de documentkoptekst of op de regel. De standaardtransactiecode wordt overgenomen uit het overeenkomstige veld op de pagina **Parameters buitenlandse handel**. De standaarbasisproductcode, het land/de regio van herkomst, en staat/provincie van herkomst worden opgehaald van het artikel. U kunt de standaardwaarden wijzigen en ook andere aan buitenlandse handel gerelateerde informatie invullen: de statistische procedure, de transportwijze en de haven.

### <a name="use-the-intrastat-journal-to-generate-information-about-trade-among-eu-countriesregions"></a>Met het Intrastat-journaal kunt u gegevens genereren over handel tussen landen en regio's van de EU.

Voor statistische doeleinden genereert u elke maand informatie over handel tussen de landen/regio's van de EU. U kunt transacties overboeken van een vrije-tekstfactuur, klantfactuur, klantpakbon, leveranciersfactuur, leverancierspakbon, projectfactuur of transferorder volgens de criteria voor overdracht die zijn geconfigureerd op de pagina **Parameters buitenlandse handel**. U kunt er ook voor kiezen transacties handmatig in te voeren. Overgeboekte transacties kunt u in het Intrastat-journaal handmatig bijwerken, als updates worden vereist. In specifieke omstandigheden die op de pagina **Compressie van Intrastat** worden geconfigureerd, kunt u de transacties in het Intrastat-journaal comprimeren. Sommige landen/regio's laten u een lage transactiedrempel toepassen. U kunt vervolgens transacties rapporteren die onder de opgegeven basisproductcode beneden deze drempel liggen. U kunt de basisproductcode op de bijbehorende Intrastat-journaalregels bijwerken, op basis van de instelling voor **Ondergrens** op de pagina **Parameters buitenlandse handel**. U kunt die transacties ook comprimeren, op basis van de instelling **Compressie van Intrastat**. U kunt valideren of de transacties in het Intrastat-journaal compleet zijn, op basis van de instelling **Instelling controleren** op de pagina **Parameters buitenlandse handel**. De gegevens in bijbehorende velden kunnen op volledigheid worden gecontroleerd: land/regio, staat of provincie, gewicht, basisproductcode, transactiecode, aanvullende eenheid, haven, oorsprong, leveringsvoorwaarden, transportwijze en btw-nummer. De transacties die niet zijn voltooid, worden gemarkeerd als zijnde niet geldig.

### <a name="use-the-intrastat-journal-to-report-information-about-trade-among-eu-countriesregions"></a>Met het Intrastat-journaal kunt u gegevens rapporteren over handel tussen landen en regio's van de EU.

Voor statistische doeleinden rapporteert u elke maand informatie over handel tussen de landen/regio's van de EU. U kunt de Intrastat-aangifte afdrukken, op basis van de instellingen **Toewijzing van rapportindeling** op de pagina **Parameters buitenlandse handel**. U kunt ook een elektronisch bestand genereren, op basis van de instellingen **Toewijzing van bestandsindeling** op de pagina **Parameters buitenlandse handel**. Zie de taakregistraties voor Intrastat-aangifte voor meer informatie over Intrastat-aangifte, waaronder de vereisten:

  - Een EU Intrastat-aangifte genereren
  - Transacties overboeken naar Intrastat
  - Vrachtadres opgeven voor een intracommunautaire transactie

## <a name="prerequisites"></a>Vereisten
In de volgende tabel ziet u de vereisten voor Intrastat-aangifte.

|  Vereiste  |  Beschrijving  |
|-------------------------|-------------------------|
| Adresinstelling | Configureer ISO-codes (International Organization for Standardization) voor de landen/regio's. |
| Rechtspersoon | Configureer btw-nummers voor import/export, de filiaalnummerextensie voor import/export en de Intrastat-code die aan de rechtspersoon is toegewezen. |
| Productcategoriehiërarchie (verkopenhiërarchie, inkoophiërarchie) | Wijs de Intrastat-basisproductcodes toe aan de categorieknooppunten op het tabblad **Basisproductcodes** op de pagina **Categoriehiërarchie**. Wanneer u een basisproductcode aan een bovenliggende categorieknooppunt toewijst, is die code van toepassing op alle onderliggende categorieknooppunten. De geselecteerde basisproductcodes zijn beschikbaar in de weergave **Geselecteerd**, wanneer u een basisproductcode selecteert in de productdetails, en op regels van verkooporders, inkooporders en transferorders. |
| Vrijgegeven productdetails | Configureer de volgende gegevens voor buitenlandse handel voor vrijgegeven producten:<ul><li>**Basisproductcode**: Selecteer deze in de lijst met geselecteerde basisproducten die is opgehaald uit de toegewezen productcategorieën, of in de volledige lijst van Intrastat-basisproductcodes.</li><li>**Statistieken toeslagenpercentage**</li><li>**Land/regio van oorsprong**: Selecteer het standaardland/de standaardregio waar de goederen volledig werden verkregen of geproduceerd.</li><li>**Staat/provincie van oorsprong of bestemming**: Selecteerd de standaardstaat/-provincie van bestemming voor ontvangsten en de staat/provincie van verzending.</li><li>**Nettogewicht in kg**</li><li>**Uitsluiten**: schakel deze parameter in als u transacties met dit product niet naar Intrastat wilt overboeken</li></ul> |
| Klanten     | Configureer het afleveradres van de klant in het EU-land/de EU-regio. |
| Leveranciers    | Configureer het adres van de leverancier in het EU-land/de EU-regio. |
| Diverse toeslagen | De code voor diverse toeslagen die moet worden opgenomen in het factuurbedrag, het statistische bedrag, of in beide. Op de pagina **Toeslagcodes**, op het tabblad **Buitenlandse handel**, schakelt u **Intrastat-facturenwaarde** in om het toeslagenbedrag toe te voegen aan de factuurwaarde, en schakelt u **Statistische Infrastat-waarde** in om het toeslagenbedrag toe te voegen aan de statistische waarde.</br>Zie het voorbeeld van [Transactiecodes en diverse toeslagen](#transaction-codes-and-miscellaneous-charges) voor meer informatie. |
| Elektronische rapportage | Stel configuraties voor elektronische aangifte in om Intrastat-gegevens te exporteren in een elektronisch bestand met een door de relevante autoriteit vereiste indeling, en waarmee de Infrastat-gegevens kunnen worden weergegeven in een leesbare (gebruikersvriendelijke) indeling (bijvoorbeeld in Microsoft Excel). |
| Magazijnbeheer | Koppel leveranciersrekeningen aan magazijncodes voor het invullen van het btw-nummer bij het overboeken van de transferorder.</br>Bekijk het voorbeeld van [Transferorder](#transfer-order) voor meer informatie.|

## <a name="setup"></a>Instelling
De volgende secties beschrijven de instellingen die voor Intrastat-aangifte zijn vereist.

### <a name="set-up-all-required-intrastat-related-lists"></a>Alle vereiste aan Intrastat gerelateerde lijsten instellen

|   Weergeven   |   Aanvullende gegevens   |
|-------------------------|-------------------------|
| Basisproductcodes | Stel een categoriehiërarchie in van het type **Basisproductcode** en voer alle basisproductcodes in volgens de gecombineerde nomenclatuurlijst. Voor elk basisproduct stelt u de volgende gegevens in:<ul><li>De naam van het basisproduct en de basisproductcode</li><li>De beschrijvende naam en/of de vertaalde naam</li><li>Instellingen voor het rapporteren van aanvullende (bijkomende) eenheden op het tabblad **Buitenlandse handel** tabblad. U kunt de aanvullende eenheid in de eenheidslijst selecteren. U kunt ook opgeven of naast de geselecteerde aanvullende eenheid ook het gewicht van basisproducten moet worden gerapporteerd.</li></ul>Bekijk het voorbeeld van [Extra eenheden](#additional-units) voor meer informatie.|
| Transactiecodes | Stel de aard van de transactie in op basis van de vereisten van uw land/regio. Voor elke transactiecode die u instelt, moet u de regels configureren voor berekening van factuurbedragen en statistische bedragen voor transferorders en verkoop- of inkooporders.<ul><li>Voor transferorders configureert u een van de volgende regels voor berekening van factuurbedragen en statistische bedragen:<ul><li>**Leeg**: Het bedrag is 0 (nul).</li><li>**Financiële kostprijs**: Het bedrag is gelijk aan de financiële kosten.</li><li>**Totale kosten**: Het bedrag is gelijk aan de totale kosten van de transactie.</li><li>**Handmatig**: Het bedrag is gelijk aan het bedrag dat handmatig op de transferorderregel wordt opgegeven.</li></ul></li><li>Voor verkooporders en inkooporders configureert u een van de volgende regels voor berekening van factuurbedragen en statistische bedragen:<ul><li>**Leeg**: Het bedrag is 0 (nul).</li><li>**Factuurbedrag**: Het bedrag is gelijk aan het bedrag dat voor het basisartikel is gefactureerd.</li><li>**Basisbedrag**: Het bedrag is gelijk aan het bedrag dat zou worden gefactureerd voordat eventuele kortingen zijn toegepast.</li></ul></ul>Zie het voorbeeld van [Transactiecodes en diverse toeslagen](#transaction-codes-and-miscellaneous-charges) voor meer informatie. |
| Transportmethoden | Stel de transportwijze in op basis van de vereisten van uw land/regio. Voor elke leveringsmethode kunt u een standaardtransportmethode configureren op het tabblad **Buitenlandse handel**. |
| Havens/luchthavens | Configureer de haven/luchthaven waar de goederen worden geladen of gelost, als deze informatie door uw land/regio wordt verzameld. |
| Statistiekprocedures | Configureer de statistische procedure als deze informatie door uw land/regio wordt verzameld. |



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
<li>De standaardtransactiecodes voor verkooporders, inkooporders, creditnota's en transferorders. De transactiecode die wordt ingesteld voor creditnota's wordt ook gebruikt als de code voor retouren van materiële goederen en voor afwijkende materiële retouren versus corrigerende creditnota's. Retourzendingen van fysieke goederen worden bij Intrastat-overboeking met een andere richting aangegeven. De retour van aankomst wordt gerapporteerd als verzending en de retour van verzending wordt gerapporteerd als aankomst.</li>
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
  <li> <strong>Wisselkoerstype</strong>: u kunt desgewenst een wisselkoers opgeven die moet worden gebruikt om Intrastat-verkoop- en -inkooptransacties te rapporteren in vreemde valuta. Dit wordt gebruikt als de wisselkoers anders is dan is bij het boeken van de transactie toegepast.</li>  
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

## <a name="example"></a>Voorbeeld

### <a name="transaction-codes-and-miscellaneous-charges"></a><a name= "transaction-codes-and-miscellaneous-charges"></a>transactiecodes en diverse toeslagen

Dit onderwerp gaat over een scenario waarbij een bedrijf in Duitsland goederen bij een bedrijf in Italië moet inkopen. Voor deze inkoop moet het Duitse bedrijf nieuwe transactiecodes en berekeningsregels instellen voor het factuurbedrag en het statistische bedrag voor die transactiecodes. Wanneer het bedrijf een factuur maakt, moet het bovendien diverse toeslagen en de percentages opgeven. Er wordt bij het berekenen van de statistische waarde rekening gehouden met deze waarden.

In dit scenario wordt de rechtspersoon **DEMF** gebruikt.

#### <a name="preliminary-setup"></a>Voorlopige instellingen

1. Ga naar **Organisatiebeheer** > **Organisaties** > **Rechtspersonen** en selecteer **DEMF**.
2. Controleer op het sneltabblad **Adressen** of het veld **Land/regio** is ingesteld op **DEU(Duitsland)**.
3. Ga naar **Leveranciers** > **Leveranciers** > **Alle leveranciers**.
4. Selecteer **DE-001** in het raster.
5. Selecteer in het sneltabblad **Adres** de optie **Bewerken**.
6. Selecteer in het dialoogvenster **Adres bewerken** in het veld **Land/regio** de optie **ITA**.
7. Selecteer **OK** om het dialoogvenster te sluiten.

#### <a name="set-up-transaction-codes"></a>Transactiecodes instellen

1. Ga naar **Belasting** > **Instellingen** > **Buitenlandse handel** > **Transactiecodes**.
2. Selecteer **11** in het raster. Selecteer vervolgens **Verwijderen** in het actievenster.
3. Selecteer **Nieuw** in het actievenster.
4. Voer op het sneltabblad **Transactiecodes** in het veld **Transactie** **code** **11** in.
5. Voer in het veld **Naam** de waarde **Directe inkoop/verkoop** in.
6. Selecteer in de sectie **Verkoop en inkoop** in het veld **Factuurbedrag** het **factuurbedrag**.
7. Selecteer **Factuurbedrag** in het veld **Statistisch bedrag**.
8. Selecteer **Opslaan** in het actievenster.

#### <a name="set-up-miscellaneous-charges"></a>Diverse toeslagen instellen

1. Ga naar **Klanten** > **Instelling van toeslagen** > **Toeslagcode**.
2. Selecteer **Vracht** in het raster.
3. Selecteer **Bewerken** in het actievenster.
4. Stel op het sneltabblad **Buitenlandse handel** de opties **Intrastat-factuurwaarde** en **Statistische Intrastat-waarde** in op **Ja**.

#### <a name="set-up-foreign-trade-parameters"></a>Parameters voor buitenlandse handel instellen

1. Ga naar **Belasting** > **Instellingen** > **Buitenlandse handel** > **Parameters buitenlandse handel**.
2. Selecteer in het tabblad **Intrastat** in het sneltabblad **Algemeen** in het veld **Transactiecode** de waarde **11**.
3. Controleer of op het sneltabblad **Hiërarchie basisproductcodes** in het veld **Categoriehiërarchie** de waarde **Intrastat** is ingesteld.

#### <a name="create-a-purchase-order"></a>Inkooporder maken

1. Ga naar **Leveranciers** > **Inkooporders** > **Alle inkooporders**.
2. Selecteer **Nieuw** in het actievenster.
3. Ga in het dialoogvenster **Inkooporder maken** naar het sneltabblad **Leveranciersrekening** en selecteer **DE-001**.
4. Selecteer **OK**.
5. Controleer in het tabblad **Koptekst** in het sneltabblad **Buitenlandse** **handel** of het veld **Transactiecode** ingesteld is op **11**.
6. Selecteer in het tabblad **Regels** in het sneltabblad **Inkooporderregels** in het veld **Artikelnummer** de waarde **D0003**. Voer daarna in het veld **Hoeveelheid** de waarde **10** in.
7. Zorg ervoor dat op het sneltabblad **Regelinformatie** in het tabblad **Buitenlandse handel** het veld **Transactiecode** in de sectie **Buitenlandse handel** automatisch wordt ingesteld.
8. Selecteer **Toeslagen onderhouden** in het sneltabblad **Inkooporderregels** in het menu **Financiële items** in de sectie **Toeslagen**.
9. Selecteer in het veld **Toeslagcode** **VRACHT**.
10. Voer **30** in het veld **Toeslagwaarde** in.
11. Selecteer **Opslaan** in het actievenster. Sluit de pagina vervolgens.
12. Selecteer in het actievenster in het tabblad **Inkoop** in de groep **Acties** de optie **Bevestigen**.
13. Selecteer in het actievenster op het tabblad **Factuur** in de groep **Genereren** de optie **Factuur**.
14. Selecteer in het actievenster **Standaardgegevens**. Selecteer **Bestelde hoeveelheid** in het veld **Standaardhoeveelheid voor regels**. Selecteer vervolgens **OK**.
15. Voer **00100** in het sneltabblad **Koptekst leveranciersfactuur** in, in het gedeelte **Factuuridentificatie** in het veld **Nummer**.
16. Selecteer in de sectie **Factuurdatums** in het veld **Factuurdatum** de waarde **24/11/2021** (24 november 2021).
17. Als u de factuur wilt boeken, selecteert u **Boeken** vanuit het actievenster.

### <a name="transfer-the-vendor-invoice-to-the-intrastat-journal"></a>De leveranciersfactuur overboeken naar het Intrastat-journaal

1. Ga naar **Belasting** > **Aangiften** > **Buitenlandse handel** > **Intrastat**.
2. Selecteer in het actievenster de optie **Overboeken**.
3. Stel in het dialoogvenster **Intrastat (overboeking)** de optie **Leveranciersfactuur** in op **Ja**.
4. Selecteer **OK** om de transacties over te boeken en het Intrastat-journaal te bekijken.

   ![Regel die de inkooporder met diverse toeslagen aangeeft op de Intrastat-pagina](media/intrastat_overview_1.png)

5. Controleer het tabblad **Algemeen** voor de inkooporder. In het veld **Factuurwaarde** staat de som van de velden **Factuurbedrag** en **Factuurbedrag voor toeslagen**, en in het veld **Statistische waarde** staat de som van de velden **Statistisch bedrag** en **Statistisch toeslagbedrag**.

   ![Informatie over een inkooporder met diverse toeslagen op het tabblad Algemeen van de Intrastat-pagina](media/intrastat_overview_2.png)

### <a name="transfer-order"></a>overboekingsorder

In dit voorbeeld moet een bedrijf in Duitsland twee eenheden goederen van een magazijn in Duitsland naar een magazijn in Italië verplaatsen. Toeslagen met een tarief van 20 procent moeten ook voor dit product worden opgegeven in het veld **Statistische waarde** voor de boekhouding. In dit voorbeeld wordt de rechtspersoon **DEMF** gebruikt.

#### <a name="preliminary-setup"></a>Voorlopige instellingen

1. Ga naar **Organisatiebeheer** > **Organisaties** > **Rechtspersonen** en selecteer **DEMF**.
2. Controleer op het sneltabblad **Adressen** of het veld **Land/regio** is ingesteld op **DEU(Duitsland)**.
3. Ga naar **Belasting** > **Instellingen** > **Buitenlandse handel** > **Parameters buitenlandse handel**.
4. Controleer of op het sneltabblad **Hiërarchie basisproductcodes** in het veld **Categoriehiërarchie** de waarde **Intrastat** is ingesteld.
5. Ga naar **Leveranciers** > **Leveranciers** > **Alle leveranciers**.
6. Selecteer **DE-001** in het raster.
7. Selecteer in het sneltabblad **Adres** de optie **Bewerken**.
8. Selecteer in het dialoogvenster **Adres bewerken** in het veld **Land/regio** de optie **ITA**.
9. Selecteer **OK** om het dialoogvenster te sluiten.

#### <a name="set-up-transaction-codes"></a>Transactiecodes instellen

1. Ga naar **Belasting** > **Instellingen** > **Buitenlandse handel** > **Transactiecodes**.
2. Selecteer **11** in het raster. Selecteer vervolgens **Verwijderen** in het actievenster.
3. Selecteer **Nieuw** in het actievenster.
4. Voer op het sneltabblad **Transactiecodes** in het veld **Transactie** **code** **11** in.
5. Voer in het veld **Naam** de waarde **Directe inkoop/verkoop** in.
6. Selecteer **Totale kosten** in de sectie **Transferorder** in het veld **Factuurbedrag**.
7. Selecteer in het veld **Statistisch bedrag** de optie **Totale kosten**.
8. Selecteer **Opslaan** in het actievenster.
9. Ga naar **Belasting** > **Instellingen** > **Buitenlandse handel** > **Parameters buitenlandse handel**.
10. Selecteer op het tabblad **Intrastat** op het sneltabblad **Algemeen** in het veld **Transferorder** de waarde **11**.

#### <a name="set-up-charges-for-an-item"></a>Toeslagen instellen voor een artikel

1. Ga naar **Productgegevensbeheer** > **Producten** > **Vrijgegeven producten**.
2. Selecteer **D0001** in het raster.
3. Selecteer in het sneltabblad **Buitenlandse handel** in het gedeelte **Intrastat** in het veld **Percentage van toeslagen** de waarde **20**.

#### <a name="change-the-site-address"></a>Het locatieadres wijzigen

1. Ga naar **Magazijnbeheer** > **Instellingen** > **Magazijn** > **Vestigingen**.
2. Selecteer **1** in het raster.
3. Selecteer in het sneltabblad **Adressen** de optie **Bewerken**.
4. Selecteer in het dialoogvenster **Adres bewerken** in het veld **Land/regio** de optie **DEU**.
5. Selecteer **OK**.
6. Selecteer **2** in het raster.
7. Selecteer in het sneltabblad **Adressen** de optie **Bewerken**.
8. Selecteer in het dialoogvenster **Adres bewerken** in het veld **Land/regio** de optie **ITA**.
9. Selecteer **OK**.
10. Ga naar **Magazijnbeheer** > **Instellen** > **Magazijn** > **Magazijnen**.
11. Selecteer **21** in het raster.
12. Selecteer in het sneltabblad **Algemeen** in het gedeelte **Verwijzing** in het veld **Leverancierrekening** de waarde **DE-001**.

#### <a name="create-a-transfer-order"></a>Een transferorder maken

1. Ga naar **Voorraadbeheer** > **Inkomende orders** > **Transferorder**.
2. Selecteer **Nieuw** in het actievenster.
3. Selecteer **11** in het veld **Van magazijn** op het sneltabblad **Transferorderkoptekst** op het tabblad **Regels** in de sectie **Overzicht**. Selecteer **21** in het veld **Naar magazijn**.
4. Selecteer **Toevoegen** op het tabblad **Regels** op het sneltabblad **Transferorderregels**.
5. Selecteer in het veld **Artikelnummer** de optie **D0001**. Voer daarna in het veld **Transferhoeveelheid** de waarde **2** in.
6. Zorg ervoor dat op het sneltabblad **Regelinformatie** in het tabblad **Buitenlandse handel** het veld **Transactiecode** in de sectie **Buitenlandse handel** automatisch wordt ingesteld.
7. Selecteer vervolgens in het actievenster op het tabblad **Verzenden** in de groep **Bewerkingen** de optie **Transferorder verzenden**.
8. Selecteer **Alle** in het dialoogvenster **Zending** op het tabblad **Overzicht** in het veld **Bijwerken**.
9. Selecteer **OK** om de order te verzenden.
10. Selecteer in het Actievenster op het tabblad **Ontvangen** in de groep **Bewerkingen** de optie **Ontvangen**.
11. Selecteer **Alle** in het dialoogvenster **Ontvangen** op het tabblad **Overzicht** in het veld **Bijwerken**.
12. Selecteer **OK** om de order te verzenden.

#### <a name="transfer-the-transfer-order-to-the-intrastat-journal"></a>De transferorder overboeken naar het Intrastat-journaal

1. Ga naar **Belasting** > **Aangiften** > **Buitenlandse handel** > **Intrastat**.
2. Selecteer in het actievenster de optie **Overboeken**.
3. Stel in het dialoogvenster **Intrastat (Transfer)** de optie **Transferorder** in op **Ja** en alle andere opties op **Nee**.
4. Selecteer **OK** om de transacties over te boeken en het Intrastat-journaal te bekijken.

   ![Regel die staat voor de transferorder op de Intrastat-pagina](media/intrastat_overview_3.png)

5.  Controleer het tabblad **Algemeen** voor de transferorder.

    De velden in de secties **Factuurwaarde** en **Statistische waarde** worden automatisch ingesteld. De waarden van de velden **Factuurbedrag** en **Statistisch bedrag** zijn gebaseerd op de instellingen op de pagina **Transactiecodes**. De waarde **20** in het veld **Toeslagenpercentage** is de waarde die is ingesteld op de pagina **Vrijgegeven product**. De waarde in het veld **Statistisch toeslagenbedrag** is een kwantitatieve expressie van de toeslagen (omdat 107,24 gelijk is aan 20 procent van 536,18). De waarde van het veld **Statistische waarde** is de som van waarden uit de velden **Statistisch bedrag** en **Statistisch toeslagenbedrag**.

  ![Informatie over een transferorder op het tabblad Algemeen van de Intrastat-pagina](media/intrastat_overview_4.png)

### <a name="additional-units"></a>Extra eenheden

In dit voorbeeld moet een bedrijf in Duitsland 10 eenheden goederen inkopen bij een bedrijf in Italië. Naast basisproductcodes moeten er extra eenheden worden opgegeven voor die goederen. Het voorbeeld laat zien hoe u nieuwe maateenheden maakt, extra eenheden aan de Intrastat-basisproductcode toewijst, transacties met extra eenheden kunt maken en het Intrastat-journaal kunt controleren waarin het veld voor de aanvullende eenheden is ingesteld.

#### <a name="preliminary-setup"></a>Voorlopige instellingen

1. Ga naar **Organisatiebeheer** > **Organisaties** > **Rechtspersonen** en selecteer **DEMF**.
2. Controleer op het sneltabblad **Adressen** of het veld **Land/regio** is ingesteld op **DEU(Duitsland)**.
3. Ga naar **Belasting** > **Instellingen** > **Buitenlandse handel** > **Parameters buitenlandse handel**.
4. Selecteer in het tabblad **Intrastat** in het sneltabblad **Algemeen** in het veld **Transactiecode** de waarde **11**.
5. Controleer of op het sneltabblad **Hiërarchie basisproductcodes** in het veld **Categoriehiërarchie** de waarde **Intrastat** is ingesteld.
6. Ga naar **Leveranciers** > **Leveranciers** > **Alle leveranciers**.
7. Selecteer **DE-001** in het raster.
8. Selecteer in het sneltabblad **Adres** de optie **Bewerken**.
9. Selecteer in het dialoogvenster **Adres bewerken** in het veld **Land/regio** de optie **ITA**.
10. Selecteer **OK** om het dialoogvenster te sluiten.

#### <a name="create-a-unit-of-measure"></a>Een maateenheid maken

1. Ga naar **Organisatiebeheer** > **Instellen** > **Eenheden** > **Eenheden**.
2. Selecteer **Nieuw** in het actievenster.
3. Voer een naam voor de maateenheid in in het veld **Eenheid**. Voer voor dit voorbeeld **GRM** in.
4. Selecteer in het veld **Eenheidsklasse** de eigenschap die de eenheid meet op het sneltabblad **Algemeen** in de sectie **Classificatie**. Selecteer voor dit voorbeeld **Massa**.
5. Selecteer in het veld **Eenhedenstelsel** het meetsysteem waar de eenheid bij hoort. Selecteer bijvoorbeeld **Metrische eenheden**.

#### <a name="set-up-unit-conversions"></a>Eenheidsconversies instellen

1. Ga naar **Organisatiebeheer** > **Instellen** > **Eenheden** > **Eenheidsconversies**.
2. Selecteer **Nieuw** op het tabblad **Omrekeningen tussen klassen**.
3. Selecteer **F00007** in het veld **Product** in het dialoogvenster **Eenheidsconversie**.
4. Selecteer **ea** in het veld **Van eenheid**.
5. Selecteer **GRM** in het veld **Naar eenheid**.
6. Controleer of de omrekeningshoeveelheid **1 = 1** is.
7. Selecteer **OK**.
8. Ga naar **Productgegevensbeheer** > **Producten** > **Vrijgegeven producten**.
9. Selecteer **F00007** in het raster.
10. Voer in het sneltabblad **Voorraad beheren** in het gedeelte **Voorraad** in het veld **Eenheid** de waarde **GRM** in.
11. Selecteer **Opslaan** in het actievenster.

#### <a name="set-up-product-information"></a>Productgegevens instellen

1. Ga naar **Productgegevensbeheer** > **Producten** > **Vrijgegeven producten**.
2. Selecteer **F00007** in het raster.
3. Selecteer op het sneltabblad **Buitenlandse handel** in het gedeelte **Intrastat** in het veld **Basisproduct** de waarde **920 20 34**.
4. Selecteer **Opslaan** in het actievenster.

#### <a name="assign-the-additional-unit-to-an-intrastate-commodity-code"></a>De extra eenheid toewijzen aan een Intrastat-basisproductcode

1. Ga naar **Productgegevensbeheer** > **Instellingen** > **Categorieën en kenmerken** > **Categoriehiërarchieën**.
2. Selecteer **Intrastat** in de lijst.
3. Selecteer **Speaker** in het raster.
4. Selecteer in het sneltabblad **Buitenlandse handel** in het veld **Extra eenheden** de waarde **GRM**.
5. Selecteer **Opslaan** in het actievenster.

   Zie [Maateenheden beheren](../../supply-chain/pim/tasks/manage-unit-measure.md) voor meer informatie.

#### <a name="create-a-purchase-order"></a>Inkooporder maken

1. Ga naar **Leveranciers** > **Inkooporders** > **Alle inkooporders**.
2. Selecteer **Nieuw** in het actievenster.
3. Ga in het dialoogvenster **Inkooporder maken** naar het sneltabblad **Leveranciersrekening** en selecteer **DE-001**.
4. Selecteer **OK**.
5. Controleer in het tabblad **Koptekst** in het sneltabblad **Buitenlandse** **handel** of het veld **Transactiecode** ingesteld is op **11**.
6. Selecteer in het tabblad **Regels** in het sneltabblad **Inkooporderregels** in het veld **Artikelnummer** de waarde **F00007**. Voer daarna in het veld **Hoeveelheid** de waarde **10** in.
7. Zorg ervoor dat op het sneltabblad **Regelinformatie** in het tabblad **Buitenlandse handel** in de sectie **Buitenlandse handel** de velden **Transactiecode** en **Basisproduct** automatisch wordt ingesteld.
8. Selecteer in het actievenster in het tabblad **Inkoop** in de groep **Acties** de optie **Bevestigen**.
9. Selecteer in het actievenster op het tabblad **Factuur** in de groep **Genereren** de optie **Factuur**.
10. Selecteer in het actievenster **Standaardgegevens**. Selecteer **Bestelde hoeveelheid** in het veld **Standaardhoeveelheid voor regels**. Selecteer vervolgens **OK**.
11. Op het sneltabblad **Koptekst leveranciersfactuur**, in de sectie **Factuuridentificatie**, in het veld **Nummer** voert u het getal **VE-0010** in.
12. Selecteer in de sectie **Factuurdatums** in het veld **Factuurdatum** de waarde **5/10/2021** (5 oktober 2021).
13. Als u de factuur wilt boeken, selecteert u **Boeken** vanuit het actievenster.

#### <a name="transfer-the-vendor-invoice-to-the-intrastat-journal"></a>De leveranciersfactuur overboeken naar het Intrastat-journaal

1. Ga naar **Belasting** > **Aangiften** > **Buitenlandse handel** > **Intrastat**.
2. Selecteer in het actievenster de optie **Overboeken**.
3. Stel in het dialoogvenster **Intrastat (overboeking)** de optie **Leveranciersfactuur** in op **Ja**.
4. Selecteer **OK** om de transacties over te boeken en het Intrastat-journaal te bekijken.

   ![Regel die staat voor de inkooporder op de Intrastat-pagina](media/intrastat_overview_5.png)

5. Controleer het tabblad **Algemeen** voor de inkooporder. De velden **Aantal aanvullende eenheden** en **Aanvullende eenheid** in de sectie **Eenheid** worden automatisch ingesteld.

   ![Informatie over een inkooporder op het tabblad Algemeen van de Intrastat-pagina](media/intrastat_overview_6.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
