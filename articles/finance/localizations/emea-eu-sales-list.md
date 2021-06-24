---
title: EU-verkooplijst rapportering
description: Dit artikel biedt informatie over rapportage van de EU-verkooplijst (Europese Unie).
author: EvgenyPopovMBS
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EUSalesList
audience: Application User
ms.reviewer: kfend
ms.custom: 12811
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: epopov
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5d1df15462a39c17710c9300425561bba8b69fc7
ms.sourcegitcommit: ff09736563d3cd2bc74c7664edd1767b218401cb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/04/2021
ms.locfileid: "6188379"
---
# <a name="eu-sales-list-reporting"></a>Rapport ICL-lijst

[!include [banner](../includes/banner.md)]

Dit artikel biedt informatie over rapportage van de EU-verkooplijst (Europese Unie).

## <a name="eu-sales-list-reporting"></a>EU-verkooplijst rapportering

Een leverancier die de intracommunautaire levering van goederen of diensten aan bedrijven uitvoert die binnen De Europese Unie (EU) zijn gevestigd, moeten een Aangifte vanIntracommunautaire Levering (EU-verkooplijst of ESL) indienen. In het algemeen moet ESL bij de belastingdienst worden ingediend, niet later dan de laatste dag van de maand na de kalenderperiode die ESL dekt. De leverancier moet zijn Belasting Toegevoegde Waarde (BTW)-nummer in ESL opgeven en moet ook per klant, de volgende informatie opgeven:

-   BTW-nummber van de EU-klant
-   Totale waarde van intracommunautaire levering van goederen en diensten aan de EU-klant gedurende die periode. De leverancier moet ook de algemene levering van goederen scheiden van de driehoekige handelsleveringen. Een driehoekige handelstransactie omvat directe levering van goederen van de leverancier van de leverancier naar de klant wanneer beide partijen in andere EU-lidstaten zijn geregistreerd.

Door ESL te gebruiken, kunnen de belastingdienst van elke EG-lidstaat controleren of BTW betaald is voor elke intracommunautaire transactie. De combinatie van lijsten en BTW opbrengsten laten de EU-lidstaten informatie uitwisselen betreffende de stroom van goederen door de EU heen.

## <a name="overview-of-the-eu-sales-list-reporting-process"></a>Een overzicht van de EU-verkooplijst rapporteringproces
U kunt de volgende taken uitvoeren voor een EU-verkooplijst rapportering:

-   Verzamelen van informatie over intracommunautaire handelstransacties. Een intracommunautair handelstransactie kan een verkoopfactuur, een vrije-tektsfactuur, een projectfactuur, of een leveranciersfactuur zijn. Een transactie wordt geïdentificeerd op basis van het land of de regio van de tegenpartij. Het intracommunautair handelstransacties van verschillende typen worden verzameld in de EU-verkooplijsttabel, waar deze in het algemene formulier worden weergegeven. Elk record van de ESL-tabel vertegenwoordigt enkele transacties en bestaat uit de BTW-identificatie van een tegenpartij en de totale waarde van goederen en diensten die zijn geleverd.
-   (Optioneel)**Preview de EU-verkooplijstrapport** . U kunt het rapport **EU-verkooplijst** previewen en valideren voor een bepaalde periode in de vorm van een Microsoft Excel-spreadsheet.
-   Genereren van de **EU-Verkooplijst** rapport. Het **EU Verkooplijst** rapport wordt gegenereerd in de vorm van een elektronisch bestand van een gedefinieerde indeling die voor elke EU-lidstaat specifiek is. In het algemeen bevat het **EU-Verkooplijst** rapport bevat basis informatie over de rapporterende partij en de waarde van de levering van goederen en diensten. De informatie worden gegroepeerd op het land en de VAT identificatie van een tegenpartij.
-   Sluit de EU-Verkooplijst rapporteringperiode. Nadat het **EU-Verkooplijst** rapport is gegenereerd en ingediend bij de autoriteiten ingediend, dan kunt u de records markeren van de ESL tabel als **Afgesloten**. Deze transacties worden niet opgenomen in extra rapporten.

## <a name="prerequisites"></a>Vereisten
De volgende tabel geeft de vereisten weer waaraan moet worden voldaan voordat u start.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Categorie</th>
<th>Vereiste</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>Instelling:</strong> Rechtspersoon</td>
<td>Het primaire adres van de rechtspersoon moet in een EG-lidstaat zijn. Selecteer op de pagina <strong>Rechtspersonen</strong> (klik op <strong>Organisatiebeheer</strong> &gt; <strong>Organisaties</strong> &gt; <strong>Rechtspersonen</strong>) uw rechtspersoon. OP het Sneltabblad <strong>Adressen</strong>, maken een adres, selecteert een land/regio en andere adrescomponenten, en markeer het adres als <strong>Primair</strong>. In het Sneltabblad <strong>Belastingregistratie</strong>, in het veld <strong>BTW-registratienummer</strong>, specificeer het BTW-registratienummer van uw bedrijf.</td>
</tr>
<tr class="even">
<td><strong>Instellen:</strong> BTW vrijgestelde identificatieparameters</td>
<td>Stel de identificatieparameters voor btw-vrijstelling in op de pagina <strong>Parameters land/regio</strong> (klik op <strong>Belasting</strong> &gt; <strong>Instellen</strong> &gt; <strong>Btw</strong> &gt; <strong>Parameters land/regio</strong>). Voor elk land/regio waar u tegenpartijen hebt, maak een record op de pagina en geef de volgende gegevens:
<ul>
<li><strong>Land/regio</strong> - Selecteer een land of regio om te koppelen aan een BTW-vrijstellingsidentificatie.</li>
<li><strong>BTW</strong> - Voer het BTW-vrijstelling identificatienummer (oftewel het BTW-vrijstellingnummervoorvoegsel) voor het geselecteerde land of de regio.</li>
<li><strong>Controleer BTW-vrijstellingnummer</strong> – Schakel dit selectievakje in als u de btw-vrijstellings-ID voor het land of de regio wilt valideren.</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>Instelling: </strong>BTW-vrijstellingsnummers</td>
<td>Maak btw-vrijstellingsnummers voor uw tegenpartijen op de pagina <strong>Btw-vrijstellingnummers</strong> (klik op <strong>Belasting</strong> &gt; <strong>Instellen</strong> &gt; <strong>Btw</strong> &gt; <strong>Btw-vrijstellingsnummers</strong>). Voor elk BTW-vrijstellingsnummer, maak een registratie op de pagina, en geef de volgende informatie:
<ul>
<li><strong>Land/regio </strong>- Selecteer het land of de regio van de BTW registratie van de tegenpartij.</li>
<li><strong>BTW-vrijstellingsnummer</strong> - Voer het BTW-vrijstellingsnummer van de tegenpartij in.</li>
<li><strong>Bedrijfsnaam</strong> – (Optioneel) Voer de naam van de tegenpartij in.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Instellen: </strong>Belastingregistratie voor tegenpartijen</td>
<td>Stel btw-registratiegegevens in voor uw tegenpartijen op de pagina <strong>Alle klanten</strong> (klik op <strong>Verkoop en marketing</strong> &gt; <strong>Klanten</strong> &gt; <strong>Alle klanten</strong>, selecteer een klantrecord en klik vervolgens op <strong>Opties</strong> &gt; <strong>Weergave wijzigen</strong> &gt; <strong>Detailweergave</strong>) of de pagina <strong>Leveranciers</strong> (klik op <strong>Inkoop en sourcing</strong> &gt; <strong>Leveranciers</strong> &gt; <strong>Leveranciers</strong>, selecteer een leveranciersrecord en klik vervolgens op <strong>Opties</strong> &gt; <strong>Weergave wijzigen</strong> &gt; <strong>Detailweergave</strong>). Op het Sneltabblad <strong>Factuur en levering</strong>, in het veld <strong>Btw-vrijstellingsnummer</strong>, selecteer het belastingregistratienummer.</td>
</tr>
<tr class="odd">
<td><strong>Instelling:</strong> BTW</td>
<td>Stel de btw-codes in die in het rapport <strong>EU-verkooplijst</strong> moeten worden opgenomen op de pagina <strong>Btw-codes</strong> (klik op <strong>Belasting</strong> &gt; <strong>Indirecte belastingen</strong> &gt; <strong>Btw</strong> &gt; <strong>Btw-codes</strong>). Op het sneltabblad <strong>Rapport instellen</strong> heft u voor elke btw-code die in het rapport moet worden opgenomen de selectie van het selectievakje <strong>Uitgesloten</strong> ongedaan. Stel de btw-parameters voor artikelen in op de pagina <strong>Btw-groepen voor artikel</strong> (klik op <strong>Belasting</strong> &gt; <strong>Indirecte belastingen</strong> &gt; <strong>Btw</strong> &gt; <strong>Btw-groepen voor artikel</strong>). Selecteer voor elke btw-groep voor artikelen een waarde in het veld <strong>Rapporteringstype</strong>. De waarde die u selecteert bepaalt de ESL-bedragkolom waarin het lijnbedrag opgenomen wordt.
<ul>
<li><strong>Blanco</strong> – Het lijn bedrag is inbegrepen in de kolom <strong>Niet toegekende waarde</strong>.</li>
<li><strong>Item</strong> – Het lijnbedrag is inbegrepen in de kolom <strong>Itemwaarde</strong>.</li>
<li><strong>Dienst</strong> – Het lijnbedrag is inbegrepen in de kolom <strong>Dienstwaarde</strong>.</li>
<li><strong>Blanco</strong> – Het lijn bedrag is inbegrepen in de kolom <strong>Niet toegekende waarde</strong>. Deze kolom is alleen relevant voor België.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Installatie:</strong> ESL rapporteringconfiguraties</td>
<td>Importeer of maak elektronische rapporteringsconfiguraties voor de ESL. Voor informatie over het maken en onderhouden van elektronische rapporteringsconfiguraties, zie de Elektronische rapporteringsdocumentatie.</td>
</tr>
<tr class="odd">
<td><strong>Installatie: </strong>Algemene parameters</td>
<td>Stel de ESL-rapporteringparameters in op de pagina <strong>Parameters buitenlandse handel</strong> (klik op <strong>Belasting</strong> &gt; <strong>Instellen</strong> &gt; <strong>Buitenlandse handel</strong> &gt; <strong>Parameters buitenlandse handel</strong>). Specificeer de volgende parameters:
<ul>
<li><strong>EU-verkooplijst</strong> tabblad:
<ul>
<li><strong>Contantkorting aangeven</strong> - Selecteer dit selectievakje als een contantkorting in de waarde moet worden opgenomen wanneer een transactie op ESL wordt opgenomen.</li>
<li><strong>Inkopen overboeken</strong> - Schakel dit selectievakje in als u inkopen op ESL wilt opnemen.</li>
<li><strong>Bestandsindelingtoewijzing</strong> - Selecteer de elektronische rapportering-indeling die gebruikt wordt wanneer een elektronische aangifte voor ESL wordt gegenereerd.</li>
<li><strong>Rapportindelingtoewijzing</strong> - Selecteer de elektronische rapportering-indeling die gebruikt wordt wanneer een preview-rapport voor ESL wordt gegenereerd.</li>
<li><strong>Afrondingsregel</strong> - Specificeer een echt getal om te gebruiken voor de afronding. ESL-bedragen worden afgerond naar veelvouden van dit nummer.</li>
<li><strong>Afrondingsmethode</strong> – Selecteer de afrondingsmethode die gebruikt wordt wanner ESL-bedragen worden afgerond (<strong>Normaal</strong>, <strong>Naar beneden</strong>, of <strong>Naar boven afronden</strong>).</li>
<li><strong>Gebruik minimumwaarde</strong> - Selecteer dit selectievakje als u bedragen wilt die kleiner zijn dan het <strong>Afrondingsregel</strong> nummer wordt afgerond naar boven tot het <strong>Afrondingsregel</strong> nummer.</li>
<li><strong>Aantal decimalen</strong> - Specificeer het aantal decimalen die weergegeven worden in ESL-bedragen (zowel in elektronische bestanden als op het rapport <strong>ESL-preview</strong> ).</li>
</ul></li>
<li><strong>Parameters land/regio</strong> tabblad: Identificeer EU-lidstaten. Voor elk EU-lidstaaat, maak een registratie op de pagina, en geef de volgende informatie:
<ul>
<li><strong>Land/regio</strong> Selecteer een land/regio.</li>
<li><strong>Land-/regiotype</strong> Als de <strong>Land/regio</strong> waarde het land of de regio is waar uw bedrijf in wordt geregistreerd, selecteer <strong>Binnenlands</strong>. Als de <strong>Land-/regio</strong> waarde een EU-lidstaat is, anders dan het land/regio waar uw bedrijf is geregistreerd, Selecteer <strong>EU</strong>. Als de <strong>Land/regio</strong>-waarde geen EG-lidstaat is, selecteert u <strong>Derde land/regio</strong>.</li>
</ul></li>
<li><strong>Nummerreeksen</strong> tabblad: Op de regel waarin de <strong>Verwijzing</strong> waarde is <strong>EU-verkooplijst</strong>, selecteer een nummerreekscode.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Gerelateerde transacties</strong></td>
<td><ul>
<li>Registreer een verkoop aan een klant in een andere EG-lidstaat.</li>
<li>Registreer een vrije tekstfactuur aan een klant in een andere EG-lidstaat.</li>
<li>Registreer een projectfactuur aan een klant in een andere EG-lidstaat.</li>
<li>Registreer een factuur van een verkoper in een andere EG-lidstaat.</li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="working-with-the-esl"></a>Werken met de ESL
### <a name="collecting-information-about-intra-community-trade-transactions"></a>Verzamelen van informatie over intracommunautaire handelstransacties.

De transacties van de volgende typen kunnen als intracommunautair handelsverkeer transacties worden beschouwd:

-   Verkoopfacturen
-   Vrije-tekstfacturen
-   Projectfacturen
-   Leveranciersfacturen

Een transactie wordt beschouwd als intracommunautair handelsverkeer transactie als het afleveradres van de transactie in een lidstatus gevestigd is. Voor dergelijke landen/regios moet een registratie bestaan op het tabblad **Parameters land/regio** van de pagina **Buitenlandse handel parameters**, en de waarde **Land/regio type** moet worden ingesteld op **EU**. Intracommunautair handelsverkeer transacties worden gemarkeerd in het **Lijstcode** veld. Met dit veld, kunt u algemene intracommunautair handelsverkeertransacties scheiden van driehoekige handelstransacties. U kunt informatie over intracommunautaire handelsverkeertransacties verzamelen op de pagina **EU-verkooplijst** (klik op **Belasting** &gt; **Aangiften** &gt; **Buitenlandse handel** &gt; **EU-verkooplijst**) door de functie **Overboeken** te gebruiken. Met deze functie kunt u transacties opnemen die bedragen van verschillende rapportage typen (dat wil zeggen, artikelen of diensten), volgens de item BTW-groepen die zijn gespecificeerd op transactieregels. U kunt ook andere filters toepassen om de transacties te definiëren die moeten worden opgenomen. De **Overboeken** functie maakt een registratie op de **EU-verkooplijst** pagina voor elke intracommunautaire handelsverkeertransactie die is opgenomen is en specificeerd een tegenpartijaccountnummer, een land/regio, een BTW-vrijstellingsnummer, een factuurnummer en datum, en de totaal aantal regels per rapportage type. Het kopieert ook de **Lijstcode** waarde van de transactie. U kunt de lijstcode voor een transactie handmatig wijzigen op de **EU-verkooplijst** pagina. De **Overboeken** functie maakt registraties waarin de **Rapportage status** waarde is ingesteld op **Opgenomen**. U kunt de gegevens valideren die op de pagina **EU-verkooplijst** met de functie te **Valideren** gebruiken wordt verzameld.

### <a name="generating-the-eu-sales-list-report"></a>Genereren van de EU-Verkooplijst rapport.

U kunt een rapport **EU-verkooplijst** genereren door de functie **Rapportering** gte ebruiken op de pagina **EU-verkooplijst**. Met de functie kunt u een rapportperiode selecteren en filters toepassen om de ESL-registraties te definiëren. Bovendien, kunt u andere parameters opgeven die voor elk land/regio specifiek zijn. U kunt ook kiezen om een voorbeeldrapport, een elektronisch bestand, of beide te genereren. De **Rapportering** functie gebruikt het rapport en de bestandsindeling instellingen op de pagina **Parameters buitenlandse handel** worden opgegeven. In het algemeen bestaat een **EU-verkooplijst** rapport uit afzonderlijke regels die de totale bedragen noteren van leveringen per tegenpartij land/regio, BTW-vrijstellingnummer en rapportage type (de driehoekige handelstransacties zijn opgenomen). Nadat u een rapport **EU-verkooplijst** genereert voor een bepaalde periode, kunt u de ESL-registraties markeren die in het rapport zijn bijgevoegd door de waarde **Rapportage status** in te stellen op **Gerapporteerd**. Om deze status in te stellen, gebruik de **Markeren als gerapporteerd** functie op de **EU-verkooplijst** pagina.

### <a name="closing-the-eu-sales-list-reporting-period"></a>Sluiten van de EU-Verkooplijst rapporteringperiode.

Als u het rapportageproces voor een specifieke periode (bijvoorbeeld, wanneer de belastingdienst de **EU-verkooplijst** rapport accepteerd), kunt u de ESL registraties markeren die bijgesloten zijn in het rapport voor de periode door het instellen van de **Rapportage status** waarde op **Gesloten**. Om deze status in te stellen, gebruik de **Markeren als gesloten** functie op de **EU-verkooplijst** pagina. Als u de afsluiting van de periode omkeert, kunt u ESL-registraties markeren door de **Rapportage status** waarde in te stellen op **Opgenomen**. Deze records kunnen vervolgens opnieuw op een rapport **EU-verkooplijst** worden opgenomen. Om deze status in te stellen, gebruik de **Markeren als** **Inclusief** functie op de **EU-verkooplijst** pagina.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]