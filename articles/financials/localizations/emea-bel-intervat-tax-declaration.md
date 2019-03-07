---
title: INTERVAT-belastingaangifte
description: Dit onderwerp biedt land-/regiospecifieke informatie over het instellen en maken van de INTERVAT-belastingaangifte voor rechtspersonen in alleen België.
author: v-oloski
manager: AnnBe
ms.date: 04/10/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxIntervat
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 273023
ms.search.region: Belgium
ms.author: v-oloski
ms.dyn365.ops.version: AX 7.0.1
ms.search.validFrom: 2016-05-31
ms.openlocfilehash: c7c30076abfdfe0758d751559257c0c557ca146e
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/29/2019
ms.locfileid: "371384"
---
# <a name="intervat-tax-declaration"></a>INTERVAT-belastingaangifte

[!include [banner](../includes/banner.md)]

Dit onderwerp biedt land-/regiospecifieke informatie over het instellen en maken van de INTERVAT-belastingaangifte voor rechtspersonen in alleen België.

U kunt de INTERVAT-btw-aangifte als een XML-bestand maken. De INTERVAT-aangifte die u maakt kan tevens correcties van het vorige jaar bevatten. Bovendien kunt u, als u geen transacties had voor een omzetrapport of een jaaroverzicht tijdens het vorige boekjaar, aangeven dat dit een leeg jaaroverzicht is. Gebruikers kunnen correctiegegevens invullen op de pagina **Extra btw-aangiftevakken**. In sommige gevallen zijn btw-correcties verplicht voor de Belgische btw-aangifte (belasting toegevoegde waarde). Voorbeelden zijn btw-aangiftecodes 63 en 64, die worden gebruikt voor btw-geldboetes. Andere voorbeelden zijn btw-aangiftecodes 81, 82, 83 enzovoort. Deze codes worden niet afgedrukt wanneer de totale bedragen van de codes negatief zijn. Deze negatieve bedragen moeten worden afgetrokken van de volgende btw-aangifte, wanneer deze bedragen weer positief zijn. Deze taak moet worden uitgevoerd aan de hand van een btw-correctie. Voordat gebruikers een btw-correctie maken, moeten zij aangeven welke btw-aangiftecodes onderworpen zijn aan btw-correcties.

## <a name="prerequisites"></a>Vereisten
De volgende tabel bevat de vereisten die moeten worden ingesteld voordat u begint te werken met de INTERVAT-belastingaangifte.

|Categorie|Vereiste||
|---------|----------------------------|---------------------------------------------|
|Instelling|Rechtspersoon|Selecteer op de pagina <strong>Rechtspersonen</strong> (klik op <strong>Organisatiebeheer</strong> &gt; <strong>Organisaties</strong> &gt; <strong>Rechtspersonen</strong>) uw rechtspersoon. Maak een adres op het sneltabblad <strong>Adressen</strong>. Selecteer <strong>België</strong> in het veld <strong>Land/regio</strong>, vul andere adresonderdelen in en markeer het adres als <strong>Primair</strong>. In het Sneltabblad <strong>Belastingregistratie</strong>, in het veld <strong>BTW-registratienummer</strong>, specificeer het BTW-registratienummer van uw bedrijf.|
|Instelling| Registratienummer|Stel op de pagina <strong>Rechtspersonen</strong> het registratienummer in (klik op <strong>Organisatiebeheer</strong> &gt; <strong>Organisaties</strong> &gt; <strong>Rechtspersonen</strong>). Klik op <strong>Registratie-id's</strong> en klik vervolgens op het sneltabblad <strong>Registratie-id</strong> op <strong>Toevoegen</strong>. Selecteer een waarde in het veld <strong>Registratietype</strong> en voer een waarde in het veld <strong>Registratienummer</strong> in. Zie <a href="emea-registration-ids.md">Registratienummer</a> voor meer informatie.|
|Instelling| Nummerreeksen|Stel nummerreeksen in voor <strong>Id van jaarlijkse verkooplijst</strong> en <strong>INTERVAT-id</strong> op het tabblad <strong>Nummerreeksen</strong> van de pagina <strong>Grootboekparameters</strong> (klik op <strong>Grootboek</strong> &gt; <strong>Grootboek instellen</strong> &gt; <strong>Grootboekparameters</strong>).</td>
|Instelling| Boekingsjournaal|Stel boekingsjournalen in op de pagina <strong>Journaal instellen</strong> pagina (klik op <strong>Grootboek</strong> &gt; <strong>Journaal instellen</strong>). </td>
|Instelling| Btw-dienst|Stel btw-diensten in op de pagina <strong>Btw-diensten</strong> (klik op <strong>Btw</strong> &gt; <strong>Indirecte belastingen</strong> &gt; <strong>Btw-diensten</strong>). Het veld <strong>Rapportindeling</strong> moet worden ingesteld op <strong>Indeling van Belgische aangifte</strong>.|
|Instelling| Btw-aangiftecodes|Stel btw-aangiftecodes in op de pagina <strong>Btw-aangiftecodes</strong> pagina (klik op <strong>Btw</strong> &gt; <strong>Instelling</strong> &gt; <strong>Btw</strong> &gt; <strong>Btw-aangiftecodes</strong>). Btw-aangiftecodes waarvoor het selectievakje <strong>Btw-correctie</strong> is ingeschakeld, zijn beschikbaar voor selectie op de pagina <strong>Extra btw-aangiftevakken</strong> (klik op <strong>Btw-correcties</strong> &gt; <strong>Correcties</strong>). Een voorbeeld van btw-aangiftecodes vindt u verderop in dit onderwerp.|
|Instelling| Btw-codes|Vul de velden op de tabbladen <strong>Rapport</strong> en <strong>Rapportinstelling - creditnota</strong> tabbladen van de pagina <strong>Btw-codes</strong> in (klik op <strong>Btw</strong> &gt; <strong>Indirecte belastingen</strong> &gt; <strong>Btw-codes</strong>). Selecteer waarden in de tabel <strong>Btw-aangiftecodes</strong>. |
|Instelling| INTERVAT-instellingen|Maak elementen voor INTERVAT op de pagina <strong>INTERVAT-instellingen</strong> (klik op <strong>Btw</strong> &gt; <strong>Instelling</strong> &gt; <strong>Btw</strong> &gt; <strong>INTERVAT-instellingen</strong>). Met INTERVAT kunt u elektronische belastingaangiften invullen in België. De informatie die u op deze pagina invoert wordt gebruikt wanneer u op <strong>Website openen</strong> op de pagina <strong>INTERVAT-belastingaangifte</strong> klikt. U moet een element maken voor elke taal en voor het programma waarmee u naar websites gaat. Vul de volgende velden in: Taal, Omschrijving, URL.
|Instelling| Btw-nummer|Maak btw-vrijstellingsnummers voor uw tegenpartijen op de pagina <strong>Btw-vrijstellingnummers</strong> (klik op <strong>Belasting</strong> &gt; <strong>Instellen</strong> &gt; <strong>Btw</strong> &gt; <strong>Btw-vrijstellingsnummers</strong>). Voor elk BTW-vrijstellingsnummer, maak een registratie op de pagina, en geef de volgende informatie:|
|     |                  |Land/regio</strong> Selecteer het land of de regio van de btw-registratie van de tegenpartij.|
|     |                  |Btw-vrijstellingsnummer</strong> Voer het btw-vrijstellingsnummer van de tegenpartij in.|
|     |                  |Bedrijfsnaam</strong> (optioneel) Voer de naam van de tegenpartij in.|
|Instelling|Parameters buitenlandse handel|Stel parameters voor buitenlandse handel in op het tabblad <strong>Land-/regio-eigenschappen</strong> van de pagina <strong><strong>Parameters buitenlandse handel</strong></strong> (klik op <strong>Btw</strong> &gt; <strong>Instellen</strong> &gt; <strong>Buitenlandse handel</strong> &gt; <strong>Parameters buitenlandse handel</strong>). |
|Instelling|Configuratie van INTERVAT-belastingaangifte|Configureer een model en indeling voor elektronische aangifte voor het rapport. Zie de sectie &quot;Het model en de indeling voor elektronische aangifte configureren voor het rapport&quot; verderop in dit onderwerp. Informatie over het maken en onderhouden van ER-configuraties is te vinden in de ER-documentatie.|


Meer informatie over het opstellen van het btw-overzicht raadpleegt u [(EU) Btw-aangifte](emea-vat-reporting.md).

### <a name="example-setup-of-sales-tax-reporting-codes"></a>Voorbeeld: instelling van btw-aangiftecodes

De volgende tabel bevat een voorbeeld van de btw-aangiftecodes die kunnen worden gemaakt voor gebruikers in rechtspersonen in België.

| Btw-rapportcode | Omschrijving                                                                                                                                                                                 |
|--------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 00                       | De verkoop van goederen aan de btw-tarief 0 procent                                                                                                                                           |
| 01                       | Leveringen en diensten die belastbaar zijn tegen het btw-tarief van 6% De levering van een product of service vindt plaats tegen het btw-tarief van 6%                                             |
| 02                       | Leveringen en diensten die belastbaar zijn tegen het btw-tarief van 12% De levering van een product of service vindt plaats tegen het btw-tarief van 12%                                           |
| 03                       | Leveringen en diensten die belastbaar zijn tegen het btw-tarief van 21% De levering van een product of service vindt plaats tegen het btw-tarief van 21%                                           |
| 44                       | Belastbaar bedrag van services aan belastingplichtigen (B2B) in een andere lidstaat van de Europese Unie (EU) waarin de btw moet worden betaald door de contractant die in een andere lidstaat is gevestigd |
| 45                       | Belastbaar bedrag van bouwwerkzaamheden                                                                                                                                                        |
| 46                       | Intracommunautaire levering van goederen en soortgelijke transacties (verzendingen)                                                                                                                        |
| 47                       | De levering van goederen aan een klant in een andere EU-lidstaat De levering van goederen die betrekking hebben op assemblage of installatie in het buitenland, externe verkopen enzovoort                                    |
| 48                       | Creditnota's en andere negatieve correcties voor codes 44 en 46                                                                                                                             |
| 49                       | Opbrengstcorrecties voor codes 00, 01, 02, 03, 45 en 47                                                                                                                                    |
| 54                       | Het totale bedrag aan btw dat moet worden betaald over de omzet die is opgenomen in codes 01, 02 en 03                                                                                            |
| 55                       | Het totale bedrag aan btw dat verschuldigd is voor de bedragen die worden genoemd in codes 86 en 88.                                                                                                   |
| 56                       | Co-contractant goederen en services                                                                                                                                                            |
| 57                       | Niet-EU-import, nationale btw                                                                                                                                                                 |
| 59                       | Het bedrag aan aftrekbare btw dat is opgegeven op binnenkomende facturen die betrekking hebben op de aankoop van goederen en services                                                                  |
| 62                       | Correctie: totale terug te vorderen btw                                                                                                                                                           |
| 64                       | Btw kan worden teruggevorderd voor uitgegeven creditnota's die moeten worden betaald en die betrekking hebben op facturen waarvoor oorspronkelijk btw is opgenomen in code 54.                                                       |
| 81                       | Het bedrag van alle aankopen van goederen, grondstoffen en verbruiksartikelen, plus gerelateerde verwervingskosten                                                                                         |
| 82                       | Het bedrag van diverse goederen en services, ongeacht of hierop btw van toepassing is                                                                                               |
| 83                       | Het bedrag van aankopen van kapitaalgoederen en services, ongeacht of hierop btw van toepassing is                                                                                                     |
| 84                       | Creditnota's die worden ontvangen die betrekking hebben op transacties die betrekking hebben op intracommunautaire verwervingen en intracommunautaire services voor codes 86 en 88                                |
| 85                       | Creditnota's die betrekking hebben op alle transacties met uitzondering van de transactie die zijn opgenomen in code 84                                                                                         |
| 86                       | Intracommunautaire verwervingen en vergelijkbare transacties                                                                                                                                       |

Als u een toewijzing van btw-aangiftecodes aan btw-codes wilt instellen, gaat u naar **Btw-codes** &gt; **Rapportinstelling/Rapportinstelling - creditnota**.

## <a name="configure-the-er-model-and-format-for-the-report"></a>Het ER-model configureren en indelen voor het rapport
Als u de configuratie van de INTERVAT-aangifte wilt controleren of wijzigen voor rechtspersonen in België, selecteert u op de pagina **Rapportconfiguraties** de optie **INTERVAT-model** in de lijst met modellen. Dit model wordt gebruikt voor de Belgische INTERVAT-aangifte. Klik in het actievenster op **Designer** om het model te controleren of te wijzigen. Als u de indeling van de INTERVAT-aangifte wilt controleren of wijzigen voor rechtspersonen in België, selecteert u op de pagina **Rapportconfiguraties** de optie **INTERVAT-model** in de lijst met modellen en selecteert u vervolgens, onder **INTERVAT-model** de optie **Intervat-indeling (BE)**. Klik in het actievenster op **Designer** om de indeling te controleren of te wijzigen.

## <a name="generate-an-intervat-tax-declaration"></a>Een INTERVAT-btw-aangifte genereren
Voer aan het einde van de btw-periode de INTERVAT-belastingaangifte uit (klik op **Btw** &gt; **Aangiften** &gt; **Btw**) om aangifteregels te berekenen voor de definitie van de btw-aangiftecodes die u hebt gemaakt. In de volgende tabel worden de velden beschreven die u moet instellen.

| Veld                    | Omschrijving                                                                                                                                                                                                                                                                                                                                                    |
|--------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Vereffeningsperiode        | Selecteer de toepasselijke aangifteperiode.                                                                                                                                                                                                                                                                                                                        |
| Begindatum                | Voer de eerste dag van de btw-vereffeningsperiode in waarvoor btw moet worden berekend. Deze waarde komt overeen met de datum in het veld **Van** op de pagina **Btw-vereffeningsperioden**.                                                                                                                                                                      |
| Transactiedatum         | Voer de datum in waarvoor de btw-aangifte wordt berekend. De standaardwaarde is de huidige datum. De einddatum van de vereffeningsperiode die wordt weergegeven in het veld **Van** komt overeen met het veld **Tot** op de pagina **Btw-vereffeningsperioden**. De btw-betaling wordt berekend voor alle transacties die zijn geboekt tijdens de vereffeningsperiode. |
| Bijwerken                   | Schakel dit selectievakje in om een aangifte bij te werken die eerder is ingediend.                                                                                                                                                                                                                                                                                   |
| Vervangen btw-aangifte | Voer het identificatienummer in van de te vervangen aangifte.                                                                                                                                                                                                                                                                                                 |
| Bestand                     | Voer de bestandsnaam in waarnaar de INTERVAT-belastingaangifte zal worden geëxporteerd.                                                                                                                                                                                                                                                                                     |
| Indelingstoewijzing           | Geef **INTERVAT-indeling (BE)** op.                                                                                                                                                                                                                                                                                                                              |

Het systeem genereert automatisch een INTERVAT XML-bestand en biedt vervolgens aan om dit te openen.

## <a name="generate-an-intervat-summary-tax-declaration"></a>Een samenvatting van een INTERVAT-belastingaangifte genereren
Als u een INTERVAT-belastingaangifte voor verschillende perioden en INTERVAT-belastingaangifte-id's wilt maken, klikt u op **Btw** &gt; **Query´s en rapporten** &gt; **Btw-aangiften** &gt; **Samenvatting INTERVAT-belastingaangifte** en gebruikt u vervolgens de filters om criteria op te geven voor het selecteren van gegevens.

## <a name="additional-sales-tax-report-boxes"></a>Aanvullende btw-rapportvakken
Als u correcties van de INTERVAT-belastingaangifte voor de vorige periode wilt maken, klikt u op **Btw** &gt; **Aangiften** &gt; **Btw** &gt; **Extra btw-aangiftevakken**. In de volgende tabel worden de velden beschreven die u moet instellen.

| Veld             | Omschrijving                                                                                                                                                                               |
|-------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Vereffeningsperiode | Selecteer de toepasselijke aangifteperiode.                                                                                                                                                   |
| Begindatum         | Voer de eerste dag van de btw-vereffeningsperiode in waarvoor btw moet worden berekend. Deze waarde komt overeen met de datum in het veld **Van** op de pagina **Btw-vereffeningsperioden**. |
| Einddatum           | Voer de laatste datum in.                                                                                                                                                                      |

Voer correcties in door op **Btw-correcties** &gt; **Correcties** te klikken en de volgende velden in te vullen.

| Veld             | Omschrijving                                                                                                                                                                               |
|-------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Vereffeningsperiode | Selecteer de toepasselijke aangifteperiode.                                                                                                                                                   |
| Begindatum         | Voer de eerste dag van de btw-vereffeningsperiode in waarvoor btw moet worden berekend. Deze waarde komt overeen met de datum in het veld **Van** op de pagina **Btw-vereffeningsperioden**. |
| Einddatum           | Voer de laatste datum in.                                                                                                                                                                      |
| Aangiftecode    | Selecteer rapportcode. Alleen de aangiftecodes waarvoor btw-correcties zijn ingeschakeld zijn beschikbaar tijdens het invoeren van btw-correcties.                                                       |
| Bedrag            | Voer het correctiebedrag in.                                                                                                                                                              |



<a name="additional-resources"></a>Aanvullende bronnen
--------

[Belgische btw-aangiftecodes](http://www.taxexpert.be/bestand/Betekenis%20vakken%20BTW-aangifte.pdf)




