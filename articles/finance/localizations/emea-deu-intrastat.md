---
title: Duitse Intrastat
description: Dit onderwerp bevat informatie over Intrastat-aangifte in Duitsland.
author: andosip
ms.date: 08/2/2021
ms.topic: article
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: v-aosipov
ms.search.validFrom: ''
ms.openlocfilehash: e1dbf0997417f9f1ad313e6a7b3c2c9cfae41efc6b1cfda60a5500ae0af94709
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/05/2021
ms.locfileid: "6759838"
---
# <a name="german-intrastat"></a>Duitse Intrastat

De pagina **Intrastat** wordt gebruikt om informatie te genereren en rapporteren over handel tussen landen van de EU. De Duitse Intrastat-aangifte bevat informatie over de handel in goederen voor rapportage.

In de volgende tabel worden de velden weergegeven die worden weergegeven op de Duitse Intrastat-aangifte.

| Velden | Verzendingen | Ontvangsten |
|-------------------------|-------------------------|-------------------------|
| Referentieperiode | X | X |
| Richtingscode | X | X |
| Valuta van de Intrastat-aangifte</br>**Opmerking:** Deze valuta is de <em>valuta voor de boekhouding</em>. | X | X |
| Basisproductcode | X | X |
| Naam basisproduct | X | X |
| Code bijkomende eenheid | X | X |
| Lidstaat van consignatie/bestemming | X | X |
| Netto massa | X | X |
| Hoeveelheid in bijkomende eenheden | X | X |
| Land van oorsprong |  | X |
| Factuurbedrag | X |  |
| Statistische waarde | X | X |
| Aard van transacties | X | X |
| Transportmodus | X | X |
| Regiocode</br>**Opmerking:**</br><ul></br><li>Als het land of de regio van oorsprong Duitsland is en de factuur is voor verzendingen, wordt een Intrastat-code voor de provincie van oorsprong weergegeven.</li></br><li>Als het land of de regio van oorsprong niet Duitsland is en de factuur is voor verzendingen, wordt code **99** weergegeven.</li></br><li>Als de factuur voor ontvangsten is, wordt een Intrastat-code voor de provincie weergegeven.</li></br></ul> | X | X |
| Code haven/luchthaven/binnenhaven | X | X |
| Leveringsvoorwaarden | X | X |


## <a name="set-up-intrastat"></a>Intrastat instellen

1. De codes voor het bedrijf instellen.

    1. Ga naar **Organisatiebeheer** > **Organisaties** > **Rechtspersonen**.
    2. Voer op het sneltabblad **Buitenlandse handel en logistiek** in het gedeelte **Identificatie** in veld **DVR** de ID van de uitwisselingsovereenkomst in. Deze ID wordt in het rapport opgenomen.
    3. Voer in het veld **Vrijstellingsnummer btw voor export** het btw-nummer van uw bedrijf in om te exporteren.
    4. Voer in het veld **Vrijstellingsnummer btw voor import** het btw-nummer van uw bedrijf in om te importeren.
    5. Voer in het veld **Intrastat-code** de Intrastat-code in die aan de rechtspersoon is toegewezen.
    6. Voer op het sneltabblad **Belastingregistratie**, in het veld **Btw-registratienummer** het btw-registratienummer van uw bedrijf in.

    > [!NOTE]
    > Als u een Intrastat-rapport voor partners genereert, voert u in het veld **Belastingregistratienummer** het belastingregistratienummer van uw moederbedrijf in.

2. In [Microsoft Dynamics Lifecycle Services (LCS)](https://lcs.dynamics.com/Logon/Index) kunt u in de bibliotheek met gedeelde activa de meest recente versies downloaden van de volgende ER-configuraties (elektronische aangifte) voor de Intrastat-aangifte.

    - Intrastat-model
    - Intrastat-rapport
    - INSTAT XML
    - INSTAT XML (DE)

3. Parameters voor buitenlandse handel instellen:

    1. Ga in Dynamics 365 Finance naar **Belasting** > **Instellingen** > **Parameters buitenlandse handel**.
    2. Selecteer op op het tabblad **Intrastat** in het sneltabblad **Elektronische rapportage** in het veld **Toewijzing bestandsindeling** de waarde **Intrastat XML (DE)**.
    3. Selecteer in het veld **Rapportindelingstoewijzing** de optie **Intrastat-rapport**.
    4. Selecteer op het sneltabblad **Hiërarchie van basisproductcodes** in het veld **Categoriehiërarchie** de optie **Intrastat**.
    5. Selecteer in het veld **Transactiecode** de transactiecode voor eigendomsoverdrachten. Deze code wordt gebruikt voor transacties die tot een werkelijke of geplande overdracht van eigendom tegen vergoeding (financieel of anders) leiden. De code kan ook worden gebruikt voor correcties.
    6. Selecteer in het veld **Creditnota** de transactiecode voor de retourzending van goederen. Deze code wordt gebruikt voor de retourzending van goederen nadat de transactie die oorspronkelijk is geregistreerd onder de transactiecode.
    7. Selecteer in het veld **Instantie** de Intrastat-instantie.
    8. Ga naar **Belasting** > **indirecte belastingen** > **Btw** > **Btw-instantie** en voer de volgende gegevens in voor de Intrastat-instantie die u in de vorige stap geselecteerd:

       - Identificatie van autoriteit
       - Adres
       - Gegevens contactpersoon

    9. Geef op het tabblad **Eigenschappen land/regio** in het veld **Land/regio** een overzicht weer van alle landen of regio's waarmee uw organisatie zaken doet. Selecteer voor elk land of elke regio in het veld **Land-/regiotype** de waarde **EU**, zodat het land of de regio wordt weergegeven in het Intrastat-rapport.

4. Regiocodes instellen.

    1. Ga naar **Organisatiebeheer** > **Globaal adresboek** > **Adressen** > **Instellingen adres**.
    2. Selecteer op het tabblad **Staat/provincie** in het veld **Land/regio** de waarde **DEU** en selecteer daarna **Filter toepassen**.
    3. Selecteer in het raster de provincie. Voer daarna in het veld **Intrastat-code** de unieke Intrastat-code in.

5. Het adres van oorsprong voor een product instellen.

    1. Ga naar **Productgegevensbeheer** > **Producten** > **Vrijgegeven producten**.
    2. Selecteer het product in het raster.
    3. Selecteer op het sneltabblad **Buitenlandse handel** in het gedeelte **Intrastat** in het veld **Land van oorsprong** de waarde **DEU**.

6. Ga naar **Belasting** > **Instellingen** > **Buitenlandse handel** > **Compressie van Intrastat** en selecteer de velden die moeten worden vergeleken bij het samenvatten van Intrastat-informatie. Selecteer voor de Duitse Intrastat de volgende velden:

    - Basisproduct
    - Land/regio
    - Correctie
    - Richting
    - Leveringsvoorwaarden
    - Factuur
    - Land/regio van oorsprong
    - Haven
    - Land/regio van afzender
    - Status van afzender
    - Statistische procedure
    - Transactiecode
    - Transport
    - Btw-nummer

### <a name="intrastat-transfer"></a>Intrastat-overboeking

Selecteer op de pagina **Intrastat** in het deelvenster Actie **Overboeking** om de informatie over intracommunautaire handel automatisch over te brengen van uw verkooporders, vrije-tekstfacturen, inkooporders, leveranciersfacturen, leveranciersproductontvangstbonnen **,** projectfacturen en overboekingsorders. Alleen documenten met een EU-land als land of regio van bestemming (voor verzendingen) of consignatie (voor ontvangsten) worden overgeboekt.

U kunt ook handmatig transacties invoeren door **Nieuw** te selecteren in het actievenster.

### <a name="generate-an-intrastat-report"></a>Een Intrastat-rapport genereren

1. Ga naar **Belasting** > **Aangiften** > **Buitenlandse handel** > **Intrastat**.
2. Selecteer in het deelvenster Actie **Uitvoer** > **Rapport**.
3. Stel in het dialoogvenster **Intrastat-rapport** de volgende velden in.

    | Veld | Beschrijving |
    |-------------------------|-------------------------|
    | Begindatum | Selecteer de begindatum voor het rapport. |
    | Einddatum | Selecteer de einddatum voor het rapport. |
    | Bestand genereren | Stel deze optie in op **Ja** om een XML-bestand te genereren. |
    | Bestandsnaam | Laat dit veld leeg. De bestandsnaam wordt automatisch gegenereerd en bestaat uit de waarde van de XML-tag **&lt;envelopId&gt;** plus de bestandsnaamextensie **.xml**.</br>De waarde van **&lt;idenvelop&gt;** is een samenvoeging van de volgende elementen, in deze volgorde:</br><ol type="1"></br><li>De waarde van het label **&lt;idinterchangeovereenkomst&gt;**</li></br><li>Een koppelteken (-)</li></br><li>De waarde van het label **&lt;referentiePeriode in JJJMM&gt;**</li></br><li>Een koppelteken (-)</li></br><li>De waarde van het label **&lt;envelop/datumtijd/datum in JJJJMMDD&gt;**</li></br><li>Een koppelteken (-)</li></br><li>De waarde van het label **&lt;envelop/datumtijd/tijd in hhmm&gt;**</li></br></ol> |
    | Richting | <ul></br><li>Selecteer **Ontvangsten** om te rapporteren over intracommunautaire ontvangsten.</li></br><li>Selecteer **Verzendingen** om te rapporteren over intracommunautaire verzendingen.</li></br><li>Selecteer **Beide** om te rapporteren over zowel ontvangsten als verzendingen.</li></br></ul> |
    | Belastingregistratienummer | Voer het registratienummer in dat moet worden gebruikt om de identificatiecode van de afzender te genereren, als het nummer verschilt van het belastingregistratienummer van de rechtspersoon. |


## <a name="example"></a>Voorbeeld

Dit voorbeeld laat zien hoe u ontvangsten en verzendingen voor Intrastat kunt boeken. Er wordt gebruikgemaakt van de rechtspersoon **DEMF**.

1. In [LCS](https://lcs.dynamics.com/Logon/Index) kunt u in de bibliotheek met gedeelde activa de meest recente versies downloaden van de volgende ER-configuraties voor de Intrastat-aangifte:

    - Intrastat-model
    - Intrastat-rapport
    - Intrastat XML
    - Intrastat XML (DE)

2. Transactiecodes aanmaken.

    1. Ga naar **Belasting** > **Instellingen** > **Buitenlandse handel** > **Transactiecodes**.
    2. Selecteer **Nieuw** in het actievenster.
    3. Voer in het veld **Transactiecode** de waarde **21** in.
    4. Voer in het veld **Naam** **Retourneren van goederen** in.
    5. Selecteer **Opslaan** in het actievenster.

3. Het identificatienummer van de instantie instellen.

    1. Ga naar **Belasting** > **Indirecte belastingen** > **Btw** > **Btw-instantie**.
    2. Selecteer in de lijst **TA**.
    3. Voer in het veld **Identificatie instantie** **123** in.

4. Regiocodes instellen.

    1. Ga naar **Organisatiebeheer** > **Globaal adresboek** > **Adressen** > **Instellingen adres**.
    2. Selecteer op het tabblad **Staat/provincie** in het veld **Land/regio** de waarde **DEU** en selecteer daarna **Filter toepassen**.
    3. Selecteer in het raster **BE** en voer vervolgens in het veld **Intrastat-code** **11** in.
    4. Selecteer **Opslaan** in het actievenster.

5. Parameters voor buitenlandse handel instellen.

    1. Ga naar **Belasting** > **Instellingen** > **Buitenlandse handel** > **Parameters buitenlandse handel**.
    2. Selecteer op het tabblad **Intrastat** op het sneltabblad **Algemeen** in het veld **Transactiecode** de waarde **11**.
    3. Selecteer in het veld **Creditnota** de waarde **21**.
    4. Selecteer in het veld **Instantie** de waarde **TA**.
    5. Selecteer op het sneltabblad **Elektronische rapportage** in het veld **Toewijzing bestandsindeling** de waarde **Intrastat XML (DE)**.
    6. Selecteer in het veld **Toewijzing rapportindeling** de waarde **Intrastat-rapport**.
    7. Zorg ervoor dat op het sneltabblad **Hiërarchie basisproductcodes** in het veld **Categoriehiërarchie** de waarde **Intrastat** is geselecteerd.
    8. Selecteer op het tabblad **Land-/regio-eigenschappen** de waarde **Nieuw**.
    9. Selecteer in het veld **Land/regio partij** de waarde **FRA**.
    10. Selecteer in het veld **Land-/regiotype** de waarde **EU**.

6. Wijs een basisproductcode aan een product toe en stel de oorsprong van het product in. De velden **Basisproductcode**, **Land/regio van oorsprong** en **Provincie van oorsprong** worden vervolgens automatisch ingesteld op verkoop- en inkooporders wanneer u het product selecteert.

    1. Ga naar **Productgegevensbeheer** > **Producten** > **Vrijgegeven producten**.
    2. Selecteer **D0001** in het raster.
    3. Selecteer op het sneltabblad **Buitenlandse handel** in het gedeelte **Intrastat** in het veld **Basisproduct** de waarde **920 20 34**.
    4. Selecteer in het gedeelte **Oorsprong** in het veld **Land/regio** de waarde **DEU**.
    5. Voer op het sneltabblad **Voorraad beheren** in het gedeelte **Gewichtmetingen** in het veld **Nettogewicht** de waarde **12** in.
    6. Selecteer **Opslaan** in het actievenster.

7. Transport toewijzen aan een leveringsmodus. De transportcode wordt vervolgens automatisch ingesteld op orders wanneer u de leveringsmodus selecteert.

    1. Ga naar **Inkoop en sourcing** > **Instellingen** > **Distributie** > **Leveringsmethoden**.
    2. Selecteer in de lijst **10**.
    3. Selecteer op het sneltabblad **Buitenlandse handel** in het veld **Transport** de waarde **01**.

8. Maak een verkooporder aan met een EU-klant.

    1. Ga naar **Klanten** > **Orders** > **Alle verkooporders**.
    2. Selecteer **Nieuw** in het actievenster.
    3. Selecteer in het dialoogvenster **Verkooporder maken** in het sneltabblad **Klant** in het gedeelte **Klant** in het veld **Klantaccount** de waarde **DE-012**.
    4. Selecteer in het sneltabblad **Algemeen** in het gedeelte **Opslagdimensies** in het veld **Locatie** de waarde **1**.
    5. Selecteer **11** in het veld **Magazijn**.
    6. Selecteer **OK**.
    7. Selecteer op het tabblad **Header** op het sneltabblad **Buitenlandse handel** in het veld **Haven** de waarde **53**.
    8. Selecteer in het veld **Statistische procedure** de waarde **31710**.
    9.  Selecteer op het tabblad **Regels** in het sneltabblad **Verkooporderregels** in het veld **Artikelnummer** de waarde **D0001**. Voer daarna in het veld **Hoeveelheid** de waarde **10** in.
    10. Zorg ervoor dat op het sneltabblad **Regelinformatie** op het tabblad **Buitenlandse handel** de velden **Transactiecode**, **Transport**, **Basisproduct** en **Land/regio van oorsprong** automatisch worden ingesteld.
    11. Selecteer **Opslaan** in het actievenster.
    12. Selecteer in het deelvenster Actie op het tabblad **Factuur** in het gedeelte **Genereren** de waarde **Factuur**.
    13. Selecteer in het dialoogvenster **Factuur boeken** op het sneltabblad **Parameters** in de sectie **Parameters** in het veld **Hoeveelheid** de optie **Alle**.
    14. Selecteer **OK** om de factuur te boeken.

9.  Boek de transactie over naar het Intrastat-journaal en controleer het resultaat.

    1. Ga naar **Belasting** > **Aangiften** > **Buitenlandse handel** > **Intrastat**.
    2. Selecteer in het deelvenster Actie de optie **Overboeken**.
    3. Stel in het dialoogvenster **Intrastat (overboeking)** in de sectie **Parameters** de optie **Klantfactuur** in op **Ja**.
    4. Selecteer **Filter**.
    5. Selecteer in het dialoogvenster **Intrastat-filter** op het tabblad **Bereik** de eerste regel en zorg ervoor dat het veld **Veld** is ingesteld op **Datum**.
    6. Selecteer in het veld **Criteria** de huidige datum.
    7. Selecteer **OK** om het dialoogvenster **Intrastat-filter** te sluiten.
    8. Selecteer **OK** om het dialoogvenster **Intrastat (overboeken)** te sluiten en het resultaat te controleren. De regel staat voor de verkooporder die u eerder hebt aangemaakt.

        ![Regel die staat voor de verkooporder op de Intrastat-pagina](media/intrastat_deu_1.png)

10. Selecteer de transactieregel en selecteer vervolgens het tabblad **Algemeen** om meer informatie te bekijken.

    ![Informatie over een verkooporder op het tabblad Algemeen van de Intrastat-pagina](media/intrastat_deu_2.png)

11. Maak een creditnota aan met behulp van een verkooporder.

    1. Ga naar **Klanten** > **Orders** > **Alle verkooporders**.
    2. Selecteer **Nieuw** in het actievenster.
    3. Selecteer in het dialoogvenster **Verkooporder maken** in het sneltabblad **Klant** in het gedeelte **Klant** in het veld **Klantaccount** de waarde **DE-012**.
    4. Selecteer in het sneltabblad **Algemeen** in het gedeelte **Opslagdimensies** in het veld **Locatie** de waarde **1**.
    5. Selecteer **11** in het veld **Magazijn**.
    6. Selecteer op het tabblad **Header** op het sneltabblad **Buitenlandse handel** in het veld **Haven** de waarde **53**.
    7. Selecteer in het veld **Statistische procedure** de waarde **31710**.
    8. Selecteer op het tabblad **Regels** in het sneltabblad **Verkooporderregels** in het veld **Artikelnummer** de waarde **D0001**. Voer daarna in het veld **Hoeveelheid** de waarde **-2** in.
    9. Selecteer op het sneltabblad **Regeldetails** op het tabblad **Buitenlandse handel** in het veld **Transactiecode** de waarde **21**.
    10. Zorg ervoor dat de velden **Transport**, **Basisproduct** en **Land/regio van oorsprong** automatisch worden ingesteld.
    11. Selecteer **Opslaan** in het actievenster.
    12. Selecteer in het deelvenster Actie op het tabblad **Factuur** in het gedeelte **Genereren** de waarde **Factuur**.
    13. Selecteer in het dialoogvenster **Factuur boeken** op het sneltabblad **Parameters** in de sectie **Parameters** in het veld **Hoeveelheid** de optie **Alle**.
    14. Selecteer **OK** om de factuur te boeken.

12. Boek de transactie over naar het Intrastat-journaal en controleer het resultaat.

    1. Ga naar **Belasting** > **Aangiften** > **Buitenlandse handel** > **Intrastat**.
    2. Selecteer in het deelvenster Actie de optie **Overboeken**.
    3. Stel in het dialoogvenster **Intrastat (overboeking)** in de sectie **Parameters** de optie **Klantfactuur** in op **Ja**.
    4. Selecteer **OK** om het dialoogvenster **Intrastat (overboeken)** te sluiten en het resultaat te controleren. Er is een nieuwe regel toegevoegd waar het veld **Richting** is ingesteld op **Ontvangsten**.            
        Deze regel staat voor het fysiek retourneren van goederen.

        ![Regel voor het fysiek retourneren van goederen op de Intrastat-pagina](media/intrastat_deu_3.png)

13. Selecteer de transactieregel en selecteer vervolgens het tabblad **Algemeen** om meer informatie te bekijken.

    ![Informatie over het fysiek retourneren van goederen op het tabblad Algemeen van de Intrastat-pagina](media/intrastat_deu_4.png)

14. Maak een correctie aan met behulp van een verkooporder:

    1. Ga naar **Klanten** > **Orders** > **Alle verkooporders**.
    2. Selecteer **Nieuw** in het actievenster.
    3. Selecteer in het dialoogvenster **Verkooporder maken** in het sneltabblad **Klant** in het gedeelte **Klant** in het veld **Klantaccount** de waarde **DE-012**.
    4. Selecteer in het sneltabblad **Algemeen** in het gedeelte **Opslagdimensies** in het veld **Locatie** de waarde **1**.
    5. Selecteer **11** in het veld **Magazijn**.
    6. Selecteer op het tabblad **Header** op het sneltabblad **Buitenlandse handel** in het veld **Haven** de waarde **53**.
    7. Selecteer in het veld **Statistische procedure** de waarde **31710**.
    8. Selecteer op het tabblad **Regels** in het sneltabblad **Verkooporderregels** in het veld **Artikelnummer** de waarde **D0001**. Voer daarna in het veld **Hoeveelheid** de waarde **-3** in.
    9. Selecteer op het sneltabblad **Regeldetails** op het tabblad **Buitenlandse handel** in het veld **Transactiecode** de waarde **11**.
    10. Zorg ervoor dat de velden **Transport**, **Basisproduct** en **Land/regio van oorsprong** automatisch worden ingesteld.
    11. Selecteer **Opslaan** in het actievenster.
    12. Zorg dat het veld **Transactiecode** is ingesteld op 11.
    13. Selecteer in het deelvenster Actie op het tabblad **Factuur** in het gedeelte **Genereren** de waarde **Factuur**.
    14. Selecteer in het dialoogvenster **Factuur boeken** op het sneltabblad **Parameters** in de sectie **Parameters** in het veld **Hoeveelheid** de optie **Alle**.
    15. Selecteer **OK** om de factuur te boeken.

15. Boek de transactie over naar het Intrastat-journaal en controleer het resultaat:

    1. Ga naar **Belasting** > **Aangiften** > **Buitenlandse handel** > **Intrastat**.
    2. Selecteer in het deelvenster Actie de optie **Overboeken**.
    3. Stel in het dialoogvenster **Intrastat (overboeking)** in de sectie **Parameters** de optie **Klantfactuur** in op **Ja**.
    4. Selecteer **OK** om het dialoogvenster **Intrastat (overboeken)** te sluiten en het resultaat te controleren. Er is een nieuwe regel toegevoegd waarbij in de kolom **Correctie** een vinkje is toegevoegd.

        ![Regel voor de correctie op de Intrastat-pagina](media/intrastat_deu_5.png)

16. Selecteer de transactieregel en selecteer vervolgens het tabblad **Algemeen** om meer informatie te bekijken.

    ![Informatie over de correctie op het tabblad Algemeen van de Intrastat-pagina](media/intrastat_deu_6.png)

17. Selecteer in het deelvenster Actie **Uitvoer** > **Rapport**.
18. Selecteer in het dialoogvenster **Intrastat-rapport** op het sneltabvenster **Parameters** in de sectie **Datum** de maand van de verkooporder die u hebt gemaakt.
19. Stel in het gedeelte **Exportopties** de optie **Bestand genereren** in op **Ja**.
20. Voer in het veld **Bestandsnaam** de vereiste naam in.
21. Selecteer **OK** en controleer het rapport dat wordt gegenereerd. De volgende tabel bevat de waarden in het voorbeeldrapport.

    | **Naam**                  | **Verkoopfactuur**  |   **Correctie**   | **Creditnota** |
    |---------------------------|--------------------|--------------------|-----------------|
    | id-aangifte             | 2021-07-D          | 2021-07-A          |                 |
    | Referentieperiode           | 2021-07            | 2021-07            |                 |
    | PSIId                     | 11203/118/12345000 | 11203/118/12345000 |                 |
    | functiecode              | O                  | O                  |                 |
    | stroomCode                  | D                  | V                  |                 |
    | CurrencyCode              | EUR                | EUR                |                 |
    | artikelNummer                | 0000362            | 0000362            | 0000361         |
    | CN8Code                   | 9202034            | 9202034            | 9202034         |
    | beschrijvingGoederen          | Spreker            | Spreker            | Spreker         |
    | MSConsBestCode            | FR                 | FR                 | FR              |
    | landVanOorsprongCode       | \-                 | \-                 | DE              |
    | nettoMassa                   | 120                | -36                | 24              |
    | geactureerdBedrag            | 3290               | -987               | \-              |
    | StatistischeWaarde          | 3290               | -987               | 658             |
    | aardVanTransactieACode  | 1                  | 1                  | 2               |
    | aardVanTransactieBCode  | 1                  | 1                  | 1               |
    | TransportmodusCode       | 01                 | 01                 | 01              |
    | regioCode                | 11                 | 11                 | 11              |
    | havenLuchthavenBinnenhavenCode | 53                 | 53                 | 53              |

