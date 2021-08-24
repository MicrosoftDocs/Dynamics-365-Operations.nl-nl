---
title: Franse Intrastat
description: Dit onderwerp bevat informatie over Intrastat-aangifte in Frankrijk.
author: andosip
ms.date: 07/9/2021
ms.topic: article
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: v-aosipov
ms.search.validFrom: ''
ms.openlocfilehash: a0f418aa18db99088db0b75df41f950e67160e3f
ms.sourcegitcommit: 8fb79920bea14746a71551a4456236a6386bfcea
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 07/12/2021
ms.locfileid: "6538873"
---
# <a name="french-intrastat"></a>Franse Intrastat

[!include[banner](../includes/banner.md)]

Bedrijven in Frankrijk die zijn geregistreerd voor belasting toegevoegde waarde (btw) en die handeldrijven met andere landen van de Europese Unie (EU), moeten de uitwisseling van goederen en diensten van en naar Frankrijk aangeven. De Declaration d'exchanges de biens (Verklaring over handel in goederen, oftewel DEB) is een combinatie van de ICL-lijst en de Intrastat-aangifte. U moet dit maandelijks rapport indienen voor alle intracommunautaire verkopen van goederen.

U kunt het DEB-rapport genereren in een van de twee elektronische bestandsindelingen: SAISUNIC 330 of INTRACOM.

De volgende tabel toont de velden die in de Franse Intrastat-aangifte in SAISUNIC 330-indeling zijn opgenomen.

| **Veld**                   | **Aangifteniveau**   |              |
|-----------------------------|--------------------|--------------|
|                             | **4 (vereenvoudigd)** | **1 (volledig)** |
| Referentieperiode         | X                  | X            |
| Nummer van aangifte       | X                  | X            |
| Regelnummer                 | X                  | X            |
| ISO-landcode (FR)       | X                  | X            |
| Aanvullende code          | X                  | X            |
| Siren-nummer                | X                  | X            |
| Btw-code van klant        | X                  | X            |
| Richtingscode              | X                  | X            |
| Transactietype            | X                  | X            |
| Verplichtingsniveau            | X                  | X            |
| Basisproductcode              |                    | X            |
| Nationaal NGP                |                    | X            |
| District (afdeling)         |                    | X            |
| Aard van transactie       |                    | X            |
| Land van oorsprong      |                    | X            |
| Land van oorsprong - Importen |                    | X            |
| Eindbestemming - Exporten |                    | X            |
| Factuurwaarde               | X                  | X            |
| Statistische waarde           |                    | X            |
| Nettogewicht                  |                    | X            |
| Extra eenheden            |                    | X            |
| Transportcode              |                    | X            |

De volgende tabel toont de velden die in de Franse Intrastat-aangifte in INTRACOM-indeling zijn opgenomen.

| **Veld**                   | **Aangifteniveau**   |              |
|-----------------------------|--------------------|--------------|
|                             | **4 (vereenvoudigd)** | **1 (volledig)** |
| Code                        | X                  | X            |
| Nummer van aangifte       | X                  | X            |
| Nummer van regel              | X                  | X            |
| Siren                       | X                  | X            |
| District (afdeling)         |                    | X            |
| Transportcode              |                    | X            |
| Land van oorsprong           |                    | X            |
| Aard van transactie       |                    | X            |
| Factuurwaarde               | X                  | X            |
| Leveringsmethoden           |                    | X            |
| Transactietype            | X                  | X            |
| Verplichtingsniveau            | X                  | X            |
| Basisproductcode              |                    | X            |
| Nationaal NGP                |                    | X            |
| Nettogewicht                  |                    | X            |
| Statistische waarde           |                    | X            |
| Extra eenheden            |                    | X            |
| Land van oorsprong - Importen |                    | X            |
| Eindbestemming - Exporten |                    | X            |
| Btw-code van klant        | X                  | X            |
| Aanvullende code          | X                  | X            |
| Referentieperiode         | X                  | X            |

### <a name="set-up-intrastat"></a>Intrastat instellen

1.  In [Microsoft Dynamics Lifecycle Services (LCS)](https://lcs.dynamics.com/Logon/Index) kunt u in de bibliotheek met gedeelde activa de meest recente versies downloaden van de volgende ER-configuraties (elektronische aangifte) voor de Intrastat-aangifte:

-   Intrastat-model

-   Intrastat-rapport

-   Intrastat INTRACOM (FR)

-   Intrastat SAISUNIC (FR)

Zie voor meer informatie [Elektronische rapportageconfiguraties downloaden vanuit Lifecycle Services](../../fin-ops-core/dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md).

2.  Ga in Dynamics 365 Finance naar **Belasting** &gt; **Instellingen** &gt; **Buitenlandse handel** &gt; **Parameters buitenlandse handel** en voer deze stappen uit:

    1.  Selecteer op het tabblad **Intrastat** op het sneltabblad **Elektronische aangifte** in het veld **Bestandsindelingstoewijzing** de optie **Intrastat INTRACOM (FR)** of **Intrastat SAISUNIC (FR)**.

    2.  Selecteer in het veld **Rapportindelingstoewijzing** de optie **Intrastat-rapport**.

    3.  Selecteer op het sneltabblad **Hiërarchie van basisproductcodes** in het veld **Categoriehiërarchie** de optie **Intrastat**.

    4.  Selecteer in het veld **Transactiecode** op het sneltabblad **Algemeen** de code die wordt gebruikt voor het overboeken van goederen.

    5.  Selecteer in het veld **Creditnota** de code die wordt gebruikt voor het retourneren van goederen.

    6.  Voer in het veld **Verplichtingsniveau voor export** het detailniveau voor het exportrapport in. Het geselecteerde niveau heeft invloed op de regels die in het rapport worden weergegeven. Zie de tabellen aan het begin van dit onderwerp voor meer informatie.

3.  Ga naar **Organisatiebeheer** &gt; **Organisaties** &gt; **Rechtspersonen**, selecteer uw bedrijf en voer vervolgens deze stappen uit:

    1.  Voer op het sneltabblad **Registratienummers** in het veld **NAF-code** uw NAF-code in. Zie [FR-00003 NAF-codes en Siret-nummers](tasks/fr-00003-naf-codes-siret-numbers.md) voor meer informatie.

    2.  Stel op het sneltabblad **Buitenlandse handel en logistiek** in de sectie **Intrastat** de velden **Btw-nummer voor export** en **Btw-nummer voor import** in.

    3.  Voer op het sneltabblad **Belastingregistratie**, in het veld **Btw-registratienummer** het btw-registratienummer van uw bedrijf in.

4.  U kunt NAF-codes en btw-nummers voor klanten opgeven door naar **Klanten** &gt; **Klanten** &gt; **Alle klanten** te gaan en deze stappen uit te voeren:

    1.  Selecteer een klant.

    2.  Voer op het Sneltabblad **Factuur en levering**, in de sectie **Btw** in het veld **Btw-nummer** het btw-nummer van de klant in.

    3.  Voer op het sneltabblad **Demografische verkoopgegevens** in het veld **Franse Siret** het Siret-nummer van het bedrijf in.

    4.  Voer in het veld **NAF-code** de NAF-code van het bedrijf in.

    5.  Herhaal deze stappen voor andere klanten.

5.  U kunt NAF-codes en btw-nummers voor leveranciers opgeven door naar **Leveranciers** &gt; **Leveranciers** &gt; **Alle leveranciers** te gaan en deze stappen uit te voeren:

    1.  Selecteer een leverancier.

    2.  Voer op het Sneltabblad **Factuur en levering**, in de sectie **Btw** in het veld **Btw-nummer** het btw-nummer van de leverancier in.

    3.  Voer op het sneltabblad **Demografische gegevens inkopen** in het veld **Franse Siret** het Siret-nummer van het bedrijf in.

    4.  Voer in het veld **NAF-code** de NAF-code van het bedrijf in.

    5.  Herhaal deze stappen voor andere leveranciers.

6.  Ga naar **Belasting** &gt; **Instellingen** &gt; **Buitenlandse handel** &gt; **Compressie van Intrastat** en selecteer de velden die moeten worden vergeleken bij het samenvatten van Intrastat-informatie. Selecteer voor Franse Intrastat de opties **Statistiekprocedure**, **Staat van oorsprong**, **Land/regio van oorsprong**, **Leveringsvoorwaarden**, **Transport**, **Correctie**, **Land/regio**, **Graafschap van oorsprong/bestemming**, **Richting**, **Land/regio van afzender**, **Staat van afzender**, **Staat**, **Transactiecode** en **Basisproduct**.

7.  Ga naar **Magazijnbeheer** &gt; **Instellingen** &gt; **Magazijn** &gt; **Magazijnen**, selecteer een magazijn en voer daarna de volgende stappen uit:

    1.  Selecteer **Toevoegen** of **Bewerken** op het sneltabblad **Adressen**.

    2.  Selecteer in het dialoogvenster **Plaats** de plaats van het magazijn. De staat van de plaats wordt gebruikt als een district voor uw DEB-rapport.

### <a name="ngp-codes"></a>NGP-codes

In het DEB-rapport bestaat de codificatie van producten uit de volgende elementen:

1.  De achtcijferige CN8-code die de tarief- en statistische classificatie van de EU vertegenwoordigt.

2.  Indien van toepassing, de eencijferige nationale artikelcode NGP (Nomenclature Générale des Produits).

In 2021 is de NGP slechts op drie typen producten van toepassing:

-   Sommige producten van koeien, schapen en geiten

-   Militaire uitrusting

-   Franse wijnen

U moet de NGP-codes instellen en deze aan gerelateerde producten toewijzen. Het veld **NGP** wordt vervolgens automatisch ingesteld op de pagina **Intrastat-journaal**.

#### <a name="set-up-an-ngp-code"></a>Een NGP-code instellen

1.  Ga naar **Belasting** &gt; **Instellingen** &gt; **Buitenlandse handel** &gt; **NGP-codes**.

2.  Selecteer in het actievenster **Nieuw** om een NGP-code te maken.

3.  Voer in het veld **NGP** een code van één cijfer in.

4.  Voer in het veld **Beschrijving** een beschrijving voor de code in.

#### <a name="assign-an-ngp-code-to-a-product"></a>Een NGP-code toewijzen aan een product

1.  Ga naar **Productgegevensbeheer** &gt; **Producten** &gt; **Vrijgegeven producten**.

2.  Selecteer een product in het raster.

3.  Selecteer op het sneltabblad **Buitenlandse handel** in de sectie **Intrastat** in het veld **NGP** de juiste NGP-code.

## <a name="intrastat-journal"></a>Intrastat-journaal

Ga naar **Belasting** &gt; **Aangiften** &gt; **Buitenlandse** **handel** &gt; **Intrastat** om uw transacties te beheren die van toepassing zijn op buitenlandse handel met EU-landen. Zie [Overzicht van Intrastat](emea-intrastat.md) voor meer informatie.

De kolom **NGP** is specifiek voor Frankrijk. Deze toont de NGP-code voor het product. Als de NGP niet van toepassing is op een product, wordt **0** (nul) weergegeven. U kunt de NGP-code aanpassen. Selecteer de transactie en selecteer vervolgens op het tabblad **Algemeen** in de sectie **Codes** in het veld **NGP** de vereiste NGP-code.

### <a name="intrastat-transfer"></a>Intrastat-overboeking

In het actievenster op de pagina **Intrastat** kunt u **Overboeking** selecteren om de informatie over intracommunautaire handel automatisch over te brengen van uw verkooporders, vrije-tekstfacturen, inkooporders, leveranciersfacturen, leveranciersproductontvangstbonnen, projectfacturen en overboekingsorders. Alleen documenten met een EU-land als land of regio van bestemming (voor verzendingen) of consignatie (voor ontvangsten) worden overgeboekt.

Aangezien het DEB-rapport een combinatie is van de ICL-lijst en het Intrastat-rapport, bevat het ook *triangulaire* transacties, waarbij directe levering wordt gedaan vanuit een EU-land (partij A) naar een ander EU-land (partij C) en een Franse rechtspersoon (partij B) als bemiddelaar optreedt bij de triangulatie-actie.

### <a name="generate-a-deb-intrastat-report"></a>Een DEB-rapport (Intrastat) genereren

1.  Ga naar **Belasting** &gt; **Aangiften** &gt; **Buitenlandse handel** &gt; **Intrastat**.

2.  Selecteer **Uitvoer** &gt; **Rapport** in het actievenster.

3.  Stel in het dialoogvenster **Intrastat-rapport** de volgende velden in.

| Veld            | Beschrijving                                                                                                                         |
|------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| Begindatum        | Selecteer de begindatum voor het rapport.                                                                                               |
| Einddatum          | Selecteer de einddatum voor het rapport.                                                                                                 |
| Bestand genereren    | Stel deze optie in op **Ja** om een TXT-bestand te genereren.                                                                                 |
| Bestandsnaam        | Voer de naam van het TXT-bestand in voor uw Intrastat-rapport.                                                                          |
| Rapport genereren  | Stel deze optie in op **Ja** om een XML-bestand te genereren.                                                                                |
| Rapportbestandsnaam | Voer de vereiste naam in.                                                                                                            |
| Alleen correcties | Stel deze optie in op **Ja** als u alleen correcties wilt aangeven. Stel het in op **Nee** om zowel normale transacties als correcties in het rapport op te geven.         |
| Richting        | Selecteer **Ontvangsten** voor een rapport over intracommunautaire ontvangsten. Selecteer **Verzendingen** voor een rapport over intracommunautaire verzendingen. |

## <a name="example"></a>Voorbeeld

In het volgende voorbeeld kunt u zien hoe u NGP-codes kunt instellen en gebruiken. Er wordt gebruikgemaakt van de rechtspersoon **DEMF**.

1.  In [Microsoft Dynamics Lifecycle Services (LCS)](https://lcs.dynamics.com/Logon/Index) kunt u in de bibliotheek met gedeelde activa de meest recente versies downloaden van de volgende ER-configuraties (elektronische aangifte) voor de Intrastat-aangifte:

-   Intrastat-model

-   Intrastat-rapport

-   Intrastat INTRACOM (FR)

2.  Stel in Finance een transactiecode in:

    1.  Ga naar **Belasting** &gt; **Instellingen** &gt; **Buitenlandse handel** &gt; **Transactiecodes**.

    2.  Selecteer **Nieuw** in het actievenster.

    3.  Voer in het veld **Transactiecode** de waarde **11** in.

    4.  Voer in het veld **Naam** de waarde **Inkoop of Verkoop** in.

    5.  Selecteer **Opslaan** in het actievenster.

3.  Een producthiërarchie instellen:

    1.  Ga naar **Productgegevensbeheer** &gt; **Instellingen** &gt; **Categorieën en kenmerken** &gt; **Categoriehiërarchieën**.

    2.  Selecteer **Intrastat** in het raster. Selecteer vervolgens in het actievenster op het tabblad **Categoriehiërarchie** in de groep **Onderhouden** de optie **Bewerken**.

    3.  Selecteer in het actievenster de optie **Nieuw categorieknooppunt**.

    4.  Voer in het veld **Naam** de waarde **Autres Libournais** in.

    5.  Voer in het veld **Code** de waarde **2204 21 42** in.

    6.  Selecteer **Opslaan** in het actievenster.

4.  Ga naar **Belasting** &gt; **Instellingen** &gt; **Buitenlandse handel** &gt; **Parameters buitenlandse handel** en voer deze stappen uit:

    1.  Selecteer op het tabblad **Intrastat** op het sneltabblad **Algemeen** in het veld **Transactiecode** de waarde **11**.

    2.  Selecteer op het sneltabblad **Elektronische rapportage** in het veld **Bestandsindelingtoewijzing** de optie **Intrastat INTRACOM (FR)**.

    3.  Selecteer in het veld **Rapportindelingstoewijzing** de optie **Intrastat-rapport**.

    4.  Selecteer op het sneltabblad **Hiërarchie van basisproductcodes** in het veld **Categoriehiërarchie** de optie **Intrastat**.

5.  Een NGP-code instellen:

    1.  Ga naar **Belasting** &gt; **Instellingen** &gt; **Buitenlandse handel** &gt; **NGP-codes**.

    2.  Selecteer **Nieuw** in het actievenster.

    3.  Voer de waarde **8** in het veld **NGP** in.

    4.  Voer in het veld **Naam beschrijving** de waarde **NGP 8** in.

    5.  Selecteer **Opslaan** in het actievenster.

6.  De NGP-code toewijzen aan een product:

    1.  Ga naar **Productgegevensbeheer** &gt; **Producten** &gt; **Vrijgegeven producten**.

    2.  Selecteer **0001** in het raster.

    3.  Selecteer op het sneltabblad **Buitenlandse handel** in het veld **NGP** de waarde **8**.

    4.  Selecteer in het veld **Basisproduct** de waarde **2204 21 42**.

    5.  Selecteer **Opslaan** in het actievenster.

7.  Maak een verkooporder die het nieuwe product bevat:

    1.  Ga naar **Klanten** &gt; **Orders** &gt; **Alle verkooporders**.

    2.  Selecteer **Nieuw** in het actievenster.

    3.  Selecteer in het dialoogvenster **Verkooporder** **maken** in de sectie **Klant** in het veld **Klantaccount** de waarde **100001**.

    4.  Selecteer in de sectie **Adres** , in het veld **Afleveradres**, het plusteken (**+**) om een adres te maken.

    5.  Voer in het dialoogvenster **Nieuw adres** in het veld **Naam van beschrijving** de waarde **Duitsland** in.

    6.  Selecteer in het veld **Land/regio** de waarde **DEU**.

    7.  Selecteer **OK**.

    8.  Selecteer **OK** in het dialoogvenster **Verkooporder maken**.

    9.  Selecteer op het sneltabblad **Verkooporderregels** in het veld **Artikelnummer** de waarde **0001**.

    10. Selecteer **Opslaan** in het actievenster.

    11. Selecteer in het actievenster op het tabblad **Factuur** in de groep **Genereren** de optie **Factuur**.

    12. Selecteer in het dialoogvenster **Factuur boeken** op het sneltabblad **Parameters** in de sectie **Parameters** in het veld **Hoeveelheid** de optie **Alle**. Selecteer vervolgens **OK** om de factuur boeken.

8.  Het DEB-rapport maken:

    1.  Ga naar **Belasting** &gt; **Aangiften** &gt; **Buitenlandse handel** &gt; **Intrastat**:

    2.  In het actievenster. selecteer **Overboeken**.

    3.  Stel in het dialoogvenster **Intrastat (overboeking)** in de sectie **Parameters** de optie **Klantfactuur** in op **Ja**. Selecteer vervolgens **OK**.

    4.  Sorteer transacties op het veld **Datum**. De bovenste transactie is de resultaattransactie. Het veld **NGP** wordt automatisch ingesteld.

    5.  Selecteer **Uitvoer** &gt; **Rapport** in het actievenster.

    6.  Selecteer in het dialoogvenster **Intrastat-rapport** op het sneltabvenster **Parameters** in de sectie **Datum** de maand van de verkooporder die u hebt gemaakt.

    7.  Stel in de sectie **Exportopties** de optie **Bestand genereren** in op **Ja**.

    8.  Voer in het veld **Bestandsnaam** de vereiste naam in.

    9.  Selecteer **OK** en bekijk het rapport.
