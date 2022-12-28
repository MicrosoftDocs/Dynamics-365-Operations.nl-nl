---
title: Franse Intrastat
description: Dit artikel bevat informatie over Intrastat-aangifte in Frankrijk.
author: anasyash
ms.date: 11/30/2022
ms.topic: article
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: atrukawk
ms.search.validFrom: ''
ms.openlocfilehash: 2076649c7fff9f47b9c1fda62a103168b19bb973
ms.sourcegitcommit: 0c927fcb3afd34d870391f05b5393a4673d916e5
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/08/2022
ms.locfileid: "9831800"
---
# <a name="french-intrastat"></a>Franse Intrastat

[!include[banner](../includes/banner.md)]

Bedrijven in Frankrijk die zijn geregistreerd voor belasting toegevoegde waarde (btw) en die handeldrijven met andere landen van de Europese Unie (EU), moeten de uitwisseling van goederen en diensten van en naar Frankrijk aangeven. De Declaration d'exchanges de biens (Verklaring over handel in goederen, oftewel DEB) is een combinatie van de ICL-lijst en de Intrastat-aangifte. U moet dit maandelijks rapport indienen voor alle intracommunautaire verkopen van goederen.

U kunt het DEB-rapport genereren in een van de twee elektronische bestandsindelingen: SAISUNIC 330 of INTRACOM.

De volgende tabel toont de velden die in de Franse Intrastat-aangifte in SAISUNIC 330-indeling zijn opgenomen. De tabel geeft ook de rapportniveaus van elk veld aan. Een veld kan de volgende rapportniveaus hebben:

- **4** – Belastingaangifte.
- **1** – Statistische respons.
- **5** – Statistische respons op zending en belastingaangifte, en gezamenlijk indienen.

| Veld                       | Aangifteniveaus |
|-----------------------------|---------------|
| Referentieperiode         | 4, 1, 5       |
| Nummer van aangifte       | 4, 1, 5       |
| Regelnummer                 | 4, 1, 5       |
| ISO-landcode (FR)       | 4, 1, 5       |
| Aanvullende code          | 4, 1, 5       |
| Siren-nummer                | 4, 1, 5       |
| Btw-code van klant        | 4, 1, 5       |
| Richtingscode              | 4, 1, 5       |
| Transactietype            | 4, 1, 5       |
| Verplichtingsniveau            | 4, 1, 5       |
| Basisproductcode              | 1, 5          |
| Nationaal NGP                | 1, 5          |
| District (afdeling)         | 1, 5          |
| Aard van transactie       | 1, 5          |
| Land van oorsprong      | 1, 5          |
| Land van oorsprong - Importen | 1, 5          |
| Eindbestemming - Exporten | 1, 5          |
| Factuurwaarde               | 4, 1, 5       |
| Statistische waarde           | 1, 5          |
| Nettogewicht                  | 1, 5          |
| Extra eenheden            | 1, 5          |
| Transportcode              | 1, 5          |

De volgende tabel toont de velden die in de Franse Intrastat-aangifte in INTRACOM-indeling zijn opgenomen. De tabel geeft ook de rapportniveaus van elk veld aan. Een veld kan de volgende rapportniveaus hebben:

- **4** – Belastingaangifte.
- **1** – Statistische respons.
- **5** – Statistische respons op zending en belastingaangifte, en gezamenlijk indienen.

| Veld                       | Aangifteniveaus |
|-----------------------------|---------------|
| Richtingscode              | 4, 1, 5       |
| Nummer van aangifte       | 4, 1, 5       |
| Nummer van regel              | 4, 1, 5       |
| Siren                       | 4, 1, 5       |
| District (afdeling)         | 1, 5          |
| Transportcode              | 1, 5          |
| Land van oorsprong           | 1, 5          |
| Aard van transactie       | 1, 5          |
| Factuurwaarde               | 4, 1, 5       |
| Leveringsmethoden           | 1, 5          |
| Transactietype            | 4, 1, 5       |
| Verplichtingsniveau            | 4, 1, 5       |
| Basisproductcode              | 1, 5          |
| Nationaal NGP                | 1, 5          |
| Nettogewicht                  | 1, 5          |
| Statistische waarde           | 1, 5          |
| Extra eenheden            | 1, 5          |
| Land van oorsprong - Importen | 1, 5          |
| Eindbestemming - Exporten | 1, 5          |
| Btw-code van klant        | 4, 1, 5       |
| Aanvullende code          | 4, 1, 5       |
| Referentieperiode         | 4, 1, 5       |

## <a name="set-up-intrastat"></a>Intrastat instellen

- In [Microsoft Dynamics Lifecycle Services](https://lcs.dynamics.com/Logon/Index) kunt u in de bibliotheek met gedeelde activa de meest recente versies downloaden van de volgende ER-configuraties (elektronische aangifte) voor de Intrastat-aangifte:

    - Intrastat-model
    - Intrastat-rapport
    - Intrastat INTRACOM (FR)
    - Intrastat SAISUNIC (FR)

    Zie voor meer informatie [Elektronische rapportageconfiguraties downloaden vanuit Lifecycle Services](../../fin-ops-core/dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md).

### <a name="set-up-vat-ids"></a>Btw-id's instellen

#### <a name="set-up-vat-codes-for-your-company"></a>Btw-codes instellen voor uw bedrijf

1. Ga naar **Belasting** \> **Instellen** \> **Btw** \> **Btw-vrijstellingsnummers**.
2. Selecteer **Nieuw** in het actievenster.
3. Selecteer in het veld **Land/regio** de waarde **FRA**.
4. Voer in het veld **Btw-nummer** de btw-nummercode van uw bedrijf in.
5. Ga naar **Organisatiebeheer** \> **Organisaties** \> **Rechtspersonen** en selecteer uw bedrijf.
6. Stel op het sneltabblad **Buitenlandse handel en logistiek** in de sectie **Intrastat** de velden **Btw-nummer voor export** en **Btw-nummer voor import** in bij de code die u in stap 4 hebt gemaakt.
7. Voer op het sneltabblad **Belastingregistratie**, in het veld **Btw-registratienummer** het btw-registratienummer van uw bedrijf in.

#### <a name="set-up-the-vat-ids-for-trading-partners"></a>De btw-id's voor handelspartners instellen

##### <a name="create-a-registration-type-for-the-company-code"></a>Een registratietype voor de bedrijfscode maken

U moet btw-id-registratietypen maken voor alle landen of regio's waar uw bedrijf zaken mee doet.

1. Ga naar **Organisatiebeheer** \> **Globaal adresboek** \> **Registratietypen** \> **Registratietypen**.
2. Selecteer in het actievenster de optie **Nieuw** om een registratietype te maken voor het btw-nummer.
3. Voer in het dialoogvenster **Details registratietype invoeren** in het veld **Naam** een naam in voor het nieuwe registratietype. Voer bijvoorbeeld **Btw-nummer** in.
4. Selecteer in het veld **Land/regio** het land of de regio van de handelspartner
5. Selecteer **Maken**.

##### <a name="match-the-registration-type-with-a-registration-category"></a>Het registratietype matchen aan een registratiecategorie

1. Ga naar **Organisatiebeheer** \> **Globaal adresboek** \> **Registratietypen** \> **Registratiecategorieën**.
2. Selecteer **Nieuw** in het actievenster om een koppeling te maken tussen een registratietype en een registratiecategorie.
3. Voor het registratietype voor het btw-nummer selecteert u de registratiecategorie **Btw-nummer**.
4. Herhaal stap 2 en 3 voor de andere registratietypen die u hebt gemaakt voor de landen of regio's met wie uw bedrijf zaken doet.

##### <a name="set-up-the-vat-number-of-a-trading-partner"></a>Het btw-nummer van een handelspartner instellen

1. Ga naar **Klanten** \> **Klanten** \> **Alle klanten**.
2. Selecteer een klant in het raster.
3. Selecteer in het actievenster op het tabblad **Klant** in de groep **Registratie** de optie **Registratie-id's**.
4. Selecteer **Toevoegen** op het sneltabblad **Registratie-id** en maak een registratie-id.
5. Selecteer in het veld **Registratietype** het registratietype dat u hebt gemaakt voor de bedrijfscode.
6. Voer het btw-nummer van het bedrijf in het veld **Registratienummer** in.
7. Selecteer **Opslaan** in het actievenster en sluit vervolgens de pagina.

Zie [Registratie-id's](emea-registration-ids.md) voor meer informatie.

### <a name="set-up-foreign-trade-parameters"></a>Parameters voor buitenlandse handel instellen

1. Ga naar **Belasting** \> **Instellingen** \> **Buitenlandse handel** \> **Parameters buitenlandse handel**.
2. Selecteer op het tabblad **Intrastat** op het sneltabblad **Elektronische aangifte** in het veld **Bestandsindelingstoewijzing** de optie **Intrastat INTRACOM (FR)** of **Intrastat SAISUNIC (FR)**.
3. Selecteer in het veld **Rapportindelingstoewijzing** de optie **Intrastat-rapport**.
4. Selecteer op het sneltabblad **Hiërarchie van basisproductcodes** in het veld **Categoriehiërarchie** de optie **Intrastat**.
5. Selecteer in het veld **Transactiecode** op het sneltabblad **Algemeen** de code die wordt gebruikt voor het overboeken van goederen.
6. Selecteer in het veld **Creditnota** de code die wordt gebruikt voor het retourneren van goederen.
7. Selecteer in het veld **Werknemer** de naam van de contactpersoon.
8. Voeg op het tabblad **Contactpersoon** informatie toe over de contactpersoon:

    - Voer in het veld **Telefoon** het telefoonnummer van de contactpersoon in.
    - Voer in het veld **Fax** het faxnummer van de contactpersoon in.

9. Geef in het tabblad **Eigenschappen land/regio** in het veld **Land/regio** een overzicht weer van alle landen of regio's waarmee uw organisatie zaken doet. Selecteer **EU** voor elk land of elke regio dat deel uitmaakt van de EU, in het veld **Land-/regiotype**, zodat het land in het Intrastat-rapport wordt weergegeven. Selecteer voor Frankrijk **Binnenlands** in het veld **Land-/regiotype**.

### <a name="set-up-compression-of-intrastat"></a>Compressie van Intrastat instellen

- Ga naar **Belasting** \> **Instellingen** \> **Buitenlandse handel** \> **Compressie van Intrastat** en selecteer de velden die moeten worden vergeleken bij het samenvatten van Intrastat-informatie. Selecteer voor de Franse Intrastat de volgende velden:
 
    - Statistiekprocedure
    - Land/regio van oorsprong
    - Transport
    - Correctie
    - Land/regio
    - Graafschap van oorsprong/bestemming
    - Richting
    - Land/regio van afzender
    - Transactiecode
    - Basisproduct

### <a name="set-up-product-parameters-for-the-intrastat-declaration"></a>Productparameters voor de Intrastat-aangifte instellen

1. Ga naar **Productgegevensbeheer** \> **Producten** \> **Vrijgegeven producten**.
2. Selecteer een product in het raster.
3. Selecteer in het sneltabblad **Buitenlandse handel** in het gedeelte **Intrastat** in het veld **Basisproduct** de juiste NGP-code. De naam van het basisproduct wordt in het veld **Omschrijving van basisproducten** afgedrukt op het Intrastat-rapport.
4. Selecteer in de sectie **Herkomst** in het veld **Land/regio** het land of de regio van herkomst van het product.
5. Voer in het sneltabblad **Voorraad beheren** in het veld **Nettogewicht** het gewicht van het product in kilogram in.

### <a name="ngp-codes"></a>NGP-codes

In het DEB-rapport bestaat de codificatie van producten uit de volgende elementen:

- De achtcijferige CN8-code die de tarief- en statistische classificatie van de EU vertegenwoordigt.
- Indien van toepassing, de eencijferige nationale artikelcode NGP (Nomenclature Générale des Produits).

In 2022 is de NGP slechts op drie typen producten van toepassing:

- Sommige producten van koeien, schapen en geiten
- Militaire uitrusting
- Franse wijnen

U moet de NGP-codes instellen en deze aan gerelateerde producten toewijzen. Het veld **NGP** wordt vervolgens automatisch ingesteld op de pagina **Intrastat-journaal**.

#### <a name="set-up-an-ngp-code"></a>Een NGP-code instellen

1. Ga naar **Belasting** \> **Instellingen** \> **Buitenlandse handel** \> **NGP-codes**.
2. Selecteer **Nieuw** in het actievenster.
3. Voer in het veld **NGP** een code van één cijfer in.
4. Voer in het veld **Beschrijving** een beschrijving voor de code in.

#### <a name="assign-an-ngp-code-to-a-product"></a>Een NGP-code toewijzen aan een product

1. Ga naar **Productgegevensbeheer** \> **Producten** \> **Vrijgegeven producten**.
2. Selecteer een product in het raster.
3. Selecteer op het sneltabblad **Buitenlandse handel** in de sectie **Intrastat** in het veld **NGP** de juiste NGP-code.

### <a name="set-up-warehouse-parameters-for-the-intrastat-declaration"></a>Magazijnparameters voor de Intrastat-aangifte instellen

1. Ga naar **Magazijnbeheer** \> **Instellen** \> **Magazijn** \> **Magazijnen**.
2. Selecteer een magazijn en selecteer vervolgens **Toevoegen** of **Bewerken** op het sneltab **Adressen**.
3. Selecteer in het dialoogvenster **Plaats** de plaats van het magazijn. De staat of provincie van de plaats wordt gebruikt als een district voor uw DEB-rapport.

### <a name="set-up-the-transport-method"></a>De transportmethode instellen

1. Ga naar **Belasting** \> **Instellen** \> **Buitenlandse handel** \> **Transportmethode**.
2. Selecteer **Nieuw** in het actievenster.
3. Typ een unieke code in het veld **Transport**. Bedrijven in Frankrijk gebruiken transactiecodes die uit één cijfer bestaan.

### <a name="intrastat-journal"></a>Intrastat-journaal

Ga naar **Belasting** \> **Aangiften** \> **Buitenlandse handel** \> **Intrastat** om uw transacties te beheren die van toepassing zijn op buitenlandse handel met EU-landen. Zie [Overzicht van Intrastat](emea-intrastat.md) voor meer informatie.

De **NGP**-kolom is specifiek voor Frankrijk en toont de NGP-code voor het product. Als de NGP niet van toepassing is op een product, wordt **0** (nul) weergegeven. Als u de NGP-code wilt aanpassen, selecteert u de transactie en vervolgens selecteert u op het tabblad **Algemeen** in de sectie **Codes** in het veld **NGP** de vereiste NGP-code.

#### <a name="intrastat-transfer"></a>Intrastat-overboeking

In het actievenster op de pagina **Intrastat** kunt u **Overboeking** selecteren om de informatie over intracommunautaire handel automatisch over te brengen van uw verkooporders, vrije-tekstfacturen, inkooporders, leveranciersfacturen, leveranciersproductontvangstbonnen, projectfacturen en overboekingsorders. Alleen documenten met een EU-land als land of regio van bestemming (voor verzendingen) of consignatie (voor ontvangsten) worden overgeboekt.

Aangezien het DEB-rapport een combinatie is van de ICL-lijst en het Intrastat-rapport, bevat het ook *triangulaire* transacties, waarbij directe levering wordt gedaan vanuit een EU-land (partij A) naar een ander EU-land (partij C) en een Franse rechtspersoon (partij B) als bemiddelaar optreedt bij de triangulatie-actie.

#### <a name="generate-a-deb-intrastat-report"></a>Een DEB-rapport (Intrastat) genereren

1. Ga naar **Belasting** \> **Aangiften** \> **Buitenlandse handel** \> **Intrastat**.
2. Selecteer **Uitvoer** \> **Rapport** in het actievenster.
3. Stel in het dialoogvenster **Intrastat-rapport** de volgende velden in.

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

4. Selecteer **OK** om het dialoogvenster **Intrastat-rapport** te sluiten.
5. Selecteer het rapportniveau in het veld **Rapportniveau** op het sneltabblad **Parameters** in het dialoogvenster **Parameters elektronisch rapport**. Het rapportniveau kan zijn: **1 - statistisch antwoord**, **4 - belastingaangifte** of **5 - statistische respons op zending en belastingaangifte**.

## <a name="example"></a>voorbeeld

In het volgende voorbeeld ziet u hoe u Franse Intrastat kunt instellen en het DEB-rapport maakt. Er wordt gebruikgemaakt van de rechtspersoon **DEMF**.

### <a name="preliminary-setup"></a>Voorlopige instellingen

1. In [Microsoft Dynamics Lifecycle Services](https://lcs.dynamics.com/Logon/Index) kunt u in de bibliotheek met gedeelde activa de meest recente versies downloaden van de volgende ER-configuraties (elektronische aangifte) voor de Intrastat-aangifte:

    - Intrastat-model
    - Intrastat-rapport
    - Intrastat INTRACOM (FR)

2. Een producthiërarchie instellen:

    1. Ga naar **Productgegevensbeheer** \> **Instellingen** \> **Categorieën en kenmerken** \> **Categoriehiërarchieën**.
    2. Selecteer **Intrastat** in het raster.
    3. Selecteer in het actievenster op het tabblad **Categoriehiërarchie** in de groep **Onderhouden** de optie **Bewerken**.
    4. Selecteer in het actievenster de optie **Nieuw categorieknooppunt**.
    5. Voer in het veld **Naam** de waarde **Autres Libournais** in.
    6. Voer in het veld **Code** de waarde **2204 21 42** in.
    7. Selecteer **Opslaan** in het actievenster.

### <a name="set-up-vat-ids"></a>Btw-id's instellen

#### <a name="set-up-vat-codes-for-your-company"></a>Btw-codes instellen voor uw bedrijf

1. Ga naar **Belasting** \> **Instellen** \> **Btw** \> **Btw-vrijstellingsnummers**.
2. Selecteer **Nieuw** in het actievenster.
3. Selecteer in het veld **Land/regio** de waarde **FRA**.
4. Voer in het veld **Btw-nummer** **MS123456** in.
5. Ga naar **Organisatiebeheer** \> **Organisaties** \> **Rechtspersonen** en selecteer **DEMF**.
6. Stel op het sneltabblad **Buitenlandse handel en logistiek** in de sectie **Intrastat** de velden **Btw-nummer voor export** en **Btw-nummer voor import** in bij de code die u in stap 4 hebt gemaakt.
7. Voer het op het sneltabblad **Belastingregistratie** in het veld **Btw-registratienummer** **123456789** in.

#### <a name="set-up-the-vat-ids-for-trading-partners"></a>De btw-id's voor handelspartners instellen

##### <a name="create-a-registration-type-for-the-company-code"></a>Een registratietype voor de bedrijfscode maken

1. Ga naar **Organisatiebeheer** \> **Globaal adresboek** \> **Registratietypen** \> **Registratietypen**.
2. Selecteer in het actievenster de optie **Nieuw** om een registratietype te maken voor het btw-nummer.
3. Voer in het dialoogvenster **Gegevens van registratietype invoeren**, in het veld **Naam**, een **Btw-nummer** in.
4. Selecteer in het veld **Land/regio** de waarde **DEU**.
5. Selecteer **Maken**.

##### <a name="match-the-registration-type-with-a-registration-category"></a>Het registratietype matchen aan een registratiecategorie

1. Ga naar **Organisatiebeheer** \> **Globaal adresboek** \> **Registratietypen** \> **Registratiecategorieën**.
2. Selecteer **Nieuw** in het actievenster om een koppeling te maken tussen het registratietype en de registratiecategorie.
3. Voor het registratietype voor het **Btw-nummer** van het **DEU**-land selecteert u de registratiecategorie **Btw-nummer**.

##### <a name="set-up-the-customers-vat-registration-number"></a>Btw-registratienummer van klant instellen

1. Ga naar **Klanten** \> **Klanten** \> **Alle klanten**.
2. Selecteer **DE-016** in het raster.
3. Selecteer in het actievenster op het tabblad **Klant** in de groep **Registratie** de optie **Registratie-id's**.
4. Selecteer **Toevoegen** op het sneltabblad **Registratie-id** en maak een registratie-id.
5. Selecteer in het veld **Registratietype** **Btw-nummer**.
6. Voer in het veld **Registratienummer** de waarde **DE9012** in.
7. Selecteer **Opslaan** in het actievenster en sluit vervolgens de pagina.
8. Selecteer op het sneltabblad **Factuur en levering**, in de sectie **Btw** in het veld **Btw-nummer** de optie **DE9012**.

### <a name="set-up-foreign-trade-parameters"></a>Parameters voor buitenlandse handel instellen

1. Ga naar **Belasting** \> **Instellingen** \> **Buitenlandse handel** \> **Parameters buitenlandse handel**.
2. Selecteer op het tabblad **Intrastat** op het sneltabblad **Algemeen** in het veld **Transactiecode** de waarde **11**.
3. Selecteer op het sneltabblad **Elektronische rapportage** in het veld **Bestandsindelingtoewijzing** de optie **Intrastat INTRACOM (FR)**.
4. Selecteer in het veld **Rapportindelingstoewijzing** de optie **Intrastat-rapport**.
5. Selecteer op het sneltabblad **Hiërarchie van basisproductcodes** in het veld **Categoriehiërarchie** de optie **Intrastat**.
6. Selecteer een record in het veld **Werknemer**.
7. Voer op het tabblad **Contactpersoon** in het veld **Telefoon** het telefoonnummer van de contactpersoon in.
8. Voer in het veld **Fax** het faxnummer van de contactpersoon in.

### <a name="create-ngp-code"></a>Een NGP-code maken

1. Ga naar **Belasting** \> **Instellingen** \> **Buitenlandse handel** \> **NGP-codes**.
2. Selecteer **Nieuw** in het actievenster.
3. Voer de waarde **8** in het veld **NGP** in.
4. Voer in het veld **Naam beschrijving** de waarde **NGP 8** in.
5. Selecteer **Opslaan** in het actievenster.

### <a name="set-up-product-information"></a>Productgegevens instellen

1. Ga naar **Productgegevensbeheer** \> **Producten** \> **Vrijgegeven producten**.
2. Selecteer **D0001** in het raster.
3. Selecteer in het sneltabblad **Buitenlandse handel** in het gedeelte **Intrastat** in het veld **NGP** de waarde **8**.
4. Selecteer in het veld **Basisproduct** de waarde **2204 21 42**.
5. Selecteer in het gedeelte **Oorsprong** in het veld **Land/regio** de waarde **FRA**.
6. Voer in het sneltabblad **Voorraad beheren** in het gedeelte **Gewichtmetingen** in het veld **Nettogewicht** de waarde **2** in.
7. Selecteer **Opslaan** in het actievenster en sluit vervolgens de pagina.
8. Selecteer **D0003** in het raster.
9. Selecteer in het sneltabblad **Buitenlandse handel** in het gedeelte **Intrastat** in het veld **Basisproduct** de waarde **100 200 30**.
10. Selecteer in het gedeelte **Oorsprong** in het veld **Land/regio** de waarde **DEU**.
11. Voer in het sneltabblad **Voorraad beheren** in het gedeelte **Gewichtmetingen** in het veld **Nettogewicht** de waarde **5** in.
12. Selecteer **Opslaan** in het actievenster.

### <a name="set-up-regime-codes"></a>Regimecodes instellen

1. Ga naar **Belasting** \> **Instellingen** \> **Buitenlandse handel** \> **Statistiekprocedure**.
2. Selecteer **Nieuw** in het actievenster.
3. Voer in het veld **Statistiekprocedure** de waarde **21**.
4. Voer in het veld **Tekst 1** **Regimecode 21** in.

### <a name="change-the-site-address"></a>Het locatieadres wijzigen

1. Ga naar **Magazijnbeheer** \> **Instellingen** \> **Magazijn** \> **Vestigingen**.
2. Selecteer **1** in het raster.
3. Selecteer in het sneltabblad **Adressen** de optie **Bewerken**.
4. Selecteer in het dialoogvenster **Adres bewerken** in het veld **Land/regio** de optie **FRA**.
5. Selecteer **OK**.
6. Ga naar **Magazijnbeheer** \> **Instellingen** \> **Magazijn** \> **Magazijnen**, selecteer een magazijn en selecteer een magazijn.
7. Selecteer in het sneltabblad **Adressen** de optie **Toevoegen**.
8. Selecteer in het dialoogvenster **Nieuw adres** in het veld **Land/regio** de optie **FRA**.
9. Selecteer in het veld **Stad** de stad **Bordeaux**.
10. Selecteer **OK** om het dialoogvenster te sluiten.

### <a name="set-up-a-transport-method"></a>Een transportmethode instellen

1. Ga naar **Belasting** \> **Instellen** \> **Buitenlandse handel** \> **Transportmethode**.
2. Selecteer **Nieuw** in het actievenster.
3. Typ in het veld **Transport** het cijfer **3**.
4. Voer in het veld **Beschrijving** **Wegtransport** in.

### <a name="assign-a-transport-mode-to-a-mode-of-delivery"></a>Een transportwijze toewijzen aan een leveringsmodus

1. Ga naar **Inkoop en sourcing** \> **Instellen** \> **Distributie** \> **Leveringsmethoden**.
2. Selecteer **50** in het raster.
3. Selecteer op het sneltabblad **Buitenlandse handel** in het veld **Transport** de waarde **3**.

### <a name="create-a-sales-order-with-an-eu-customer-that-includes-the-new-product"></a>Een verkooporder maken voor een EU-klant, die het nieuwe product bevat

1. Ga naar **Klanten** \> **Orders** \> **Alle verkooporders**.
2. Selecteer **Nieuw** in het actievenster.
3. Selecteer in het dialoogvenster **Verkooporder maken** in de sectie **Klant** in het veld **Klantaccount** de waarde **DE-016**.
4. Selecteer in de sectie **Adres** , in het veld **Afleveradres**, het plusteken (**+**) om een adres te maken.
5. Voer in het dialoogvenster **Nieuw adres** in het veld **Naam van beschrijving** de waarde **Duitsland** in.
6. Selecteer in het veld **Land/regio** de waarde **DEU**.
7. Selecteer **OK**.
8. Selecteer **OK** in het dialoogvenster **Verkooporder maken**.
9. Selecteer op het sneltabblad **Verkooporderregels** in het veld **Artikelnummer** de waarde **0001**.
10. Selecteer op het sneltabblad **Regeldetails** op het tabblad **Buitenlandse handel** in het veld **Statistiekprocedure** de waarde **21**.
11. Selecteer in het veld **Provincie van oorsprong** de optie **AL**
12. Selecteer **Opslaan** in het actievenster.
13. Op het tabblad **Koptekst** moet u op het sneltabblad **Levering** in het veld **Leveringsmethode** controleren of **50** is geselecteerd.
14. Selecteer in het actievenster op het tabblad **Factuur** in de groep **Genereren** de optie **Factuur**.
15. Selecteer in het dialoogvenster **Factuur boeken** op het sneltabblad **Parameters** in de sectie **Parameters** in het veld **Hoeveelheid** de optie **Alle**. Selecteer vervolgens **OK** om de factuur boeken.

### <a name="transfer-the-transaction-to-the-intrastat-journal-and-review-the-result"></a>Boek de transactie over naar het Intrastat-journaal en controleer het resultaat

1. Ga naar **Belasting** \> **Aangiften** \> **Buitenlandse handel** \> **Intrastat**.
2. Selecteer in het actievenster de optie **Overboeken**.
3. Stel in het dialoogvenster **Intrastat (overboeking)** in de sectie **Parameters** de optie **Klantfactuur** in op **Ja**. Selecteer vervolgens **OK**.
4. Sorteer transacties op het veld **Datum**. De bovenste transactie is de resultaattransactie.

    ![Regel die staat voor de verkooporder op de Intrastat-pagina.](media/intrastat_fr_1.png)

5. Selecteer de transactieregel en selecteer vervolgens het tabblad **Algemeen** om meer informatie te bekijken.

    ![Informatie over een verkooporder op het tabblad Algemeen van de Intrastat-pagina.](media/intrastat_fr_2.png)

6. Selecteer **Uitvoer** \> **Rapport** in het actievenster.
7. Selecteer in het dialoogvenster **Intrastat-rapport** op het sneltabvenster **Parameters** in de sectie **Datum** de maand van de verkooporder die u hebt gemaakt.
8. Stel in de sectie **Exportopties** de optie **Bestand genereren** in op **Ja**.
9. Voer in het veld **Bestandsnaam** de vereiste naam in.
10. Selecteer **OK** om het dialoogvenster **Intrastat-rapport** te sluiten.
11. Selecteer in het dialoogvenster **Parameters van elektronisch rapport** op het sneltabblad **Parameters** in het veld **Rapportniveau** **5 - statistische respons op verzending en belastingaangifte** en controleer het rapport.

    ![Intrastat Intracom-rapport voor verzendingen.](media/intrastat_fr_3.png)

12. Controleer het gegenereerde Excel-rapport.

    ![Intrastat-rapport voor verzendingen.](media/intrastat_fr_4.png)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
