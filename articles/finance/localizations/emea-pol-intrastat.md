---
title: Poolse Intrastat
description: Dit onderwerp bevat informatie over Intrastat-aangifte in Polen.
author: andosip
ms.date: 11/09/2021
ms.topic: article
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: ''
ms.openlocfilehash: fbacc204208e536291035c6f9bb2ef4fa4038f58
ms.sourcegitcommit: 23588e66e25c05e989f3212ac519d7016820430a
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/13/2022
ms.locfileid: "8566086"
---
# <a name="polish-intrastat"></a>Poolse Intrastat

[!include[banner](../includes/banner.md)]

De pagina **Intrastat** wordt gebruikt om informatie te genereren en rapporteren over handel tussen landen van de EU. De Poolse Intrastat-aangifte bevat informatie over de handel in goederen voor rapportage.

De volgende velden zijn opgenomen in de Poolse Intrastat-aangifte. Alle velden zijn opgenomen bij ontvangsten en verzendingen, behalve voor **RodzajTransportu** (de transportmodus) en **KrajPochodzenia** (het land of de regio van herkomst) die niet zijn opgenomen in verzendingen, en **IdKontrahenta** (het buitenlandse btw-nummer van de klant) dat onderdeel is van de ontvangsten.

| Veldnaam | Description |
|-------------------------|-------------------------|
| Deklaracja Data | De datum waarop het document is gemaakt. |
| Miesiac | De referentiemaand van de aangifte. |
| Rok | Het referentiejaar van de aangifte. |
| Numer | Het aangiftenummer in de referentieperiode. |
| Wersja | Het versienummer van de aangifte. |
| NrWlasny | De aangifte-id. De waarde wordt automatisch gegenereerd. |
| Typ | De rapportrichting.</br><li>Voor ontvangsten wordt 'P' afgedrukt.</li><li>Voor verzendingen wordt 'W' afgedrukt.</li> |
| Rodzaj | Het type aangifte. De waarde geeft aan of het rapport de oorspronkelijke aangifte of een correctieaangifte is. |
| UC | De eenheidscode waar de Intrastat-aangifte aan wordt gericht. De waarde wordt opgegeven in het veld **Btw-vrijstellingsnummer** in de sectie **Btw** op het tabblad **Agent** van de pagina **Parameters buitenlandse handel**. |
| Nazwa | De naam van het bedrijf. |
| Miejscowosc, UlicaNumer, KodPocztowy | Het volledige adres van de rechtspersoon. |
| Nip | Het Poolse btw-nummer (value-added tax [VAT] ID). |
| Regon | Het Poolse statistische identificatienummer (bedrijfsnummer). |
| LacznaWartoscFaktur | De som van de factuurwaarden. |
| LacznaWartoscStatystyczna | De som van de statistische waarden. |
| LacznaLiczbaPozycji | Het totale aantal goederen. |
| PozId | Het volgnummer van een bepaald goederenartikel. |
| OpisTowaru | De handelsnaam van het basisproduct. |
| KrajPochodzeniaWysylki | De ISO-code (International Organization for Standardization) voor het land of de regio van de tegenpartij. |
| WarunkiDostawy | De Intrastat-code voor de leveringsvoorwaarden. |
| RodzajTransakcji | De code die de aard van de transactie aangeeft. Poolse bedrijven gebruiken transactiecodes die uit twee cijfers bestaan. |
| KodTowarowy | De basisproductcode van acht cijfers volgens de gecombineerde nomenclatuur. |
| RodzajTransportu | De Intrastat-code voor de wijze van transport. |
| KrajPochodzenia | De ISO-code voor het land of de regio waar de basisproducten zijn geproduceerd of gefabriceerd. |
| MasaNetto | De netto massa in kilogram. |
| IloscUzupelniajacaJm | De hoeveelheid in de bijkomende maateenheid, in gehele getallen. |
| WartoscFaktury | De factuurwaarde van alle transacties die gedekt worden door één artikel. |
| WartoscStatystyczna | De statistische waarde. |
| Wypelniajacy: NazwiskoImie, Telefon, Faks, Email | De voor- en achternaam, het telefoonnummer, het faxnummer en het e-mailadres van de persoon die de aangifte indient. |
| IdKontrahenta | Het buitenlandse btw-nummer van de klant in een EU-land. |


## <a name="set-up-intrastat"></a>Intrastat instellen

Importeer uit de algemene opslagplaats de meest recente versies van de volgende ER-configuraties (Elektronische rapportage):

   - Intrastat-model
   - Intrastat-rapport
   - Intrastat (PL)

Meer informatie is te vinden in [ER-configuraties downloaden uit de Algemene opslagplaats van de configuratieservice](../../fin-ops-core/dev-itpro/analytics/er-download-configurations-global-repo.md).

## <a name="set-up-a-vat-id-and-an-enterprise-number-for-your-company"></a>Een btw-nummer en een bedrijfsnummer instellen voor uw bedrijf

### <a name="create-registration-types-for-company-codes"></a>Registratietypen voor bedrijfscodes maken

U moet twee registratietypen maken voor bedrijfscodes: een voor het btw-nummer (NIP-code) en een voor het bedrijfsnummer (Regon-code).

1. Ga naar **Organisatiebeheer** > **Globaal adresboek** > **Registratietypen** > **Registratietypen**.
2. Selecteer in het actievenster de optie **Nieuw** om een registratietype te maken voor het btw-nummer.
3. Voer in het dialoogvenster **Details registratietype invoeren** in het veld **Naam** een naam in voor het nieuwe registratietype. Voer bijvoorbeeld **NIP** in.
4. Selecteer in het veld **Land/regio** de waarde **POL**.
5. Selecteer **Maken**.
6. Selecteer in het actievenster de optie **Nieuw** om een registratietype te maken voor het bedrijfsnummer.
7. Voer in het dialoogvenster **Details registratietype invoeren** in het veld **Naam** een naam in voor het nieuwe registratietype. Voer bijvoorbeeld **Regon** in.
8. Selecteer in het veld **Land/regio** de waarde **POL**.
9. Selecteer **Maken**.

### <a name="match-the-registration-types-with-registration-categories"></a>De registratietypen matchen aan registratiecategorieën

1. Ga naar **Organisatiebeheer** > **Globaal adresboek** > **Registratietypen** > **Registratiecategorieën**.
2. Selecteer **Nieuw** in het actievenster om een koppeling te maken tussen elk registratietype dat u hebt gemaakt en een registratiecategorie.

    - Voor het registratietype voor het btw-nummer (NIP-code) selecteert u de registratiecategorie **Btw-nummer**.
    - Voor het registratietype voor het bedrijfsnummer (Regon-code) selecteert u de registratiecategorie **Bedrijfs-id (COID)**.

### <a name="set-up-a-vat-id-and-an-enterprise-number-for-your-company"></a>Een btw-nummer en een bedrijfsnummer instellen voor uw bedrijf

1. Ga naar **Organisatiebeheer** > **Organisaties** > **Rechtspersonen**.
2. Selecteer uw bedrijf in het raster.
3. Selecteer in het actievenster **Registratie-id's**.
4. Selecteer op het sneltabblad **Registratie-id** de optie **Toevoegen**.
5. Selecteer in het veld **Registratietype** één van de registratietypes die u eerder hebt gemaakt.
6. Voer het btw-nummer (NIP-code) of bedrijfsnummer (Regon-code) van uw bedrijf in, afhankelijk van het registratietype dat u in de vorige stap hebt geselecteerd.
7. Herhaal stap 4 tot en met 6 voor het andere registratietype dat u eerder hebt gemaakt.

## <a name="set-up-a-company-address"></a>Een bedrijfsadres instellen

1. Ga naar **Organisatiebeheer** > **Organisaties** > **Rechtspersonen**.
2. Selecteer uw bedrijf in het raster.
3. Selecteer op het tabblad **Adressen** de optie **Bewerken**.
4. Selecteer de postcode van uw bedrijf in het dialoogvenster **Adres bewerken** in het veld **Postcode**.
5. Voer in het veld **Straat** uw adres in.
6. Selecteer uw woonplaats in het veld **Plaats**.

## <a name="set-up-foreign-trade-parameters"></a>Parameters voor buitenlandse handel instellen

1. Ga naar **Belasting** > **Instellingen** > **Parameters buitenlandse handel**.
2. Selecteer op het tabblad **Intrastat** op het sneltabblad **Elektronische rapportage** in het veld **Toewijzing bestandsindeling** de waarde **Intrastat (PL)**.
3. Selecteer in het veld **Rapportindelingstoewijzing** de optie **Intrastat-rapport**.
4. Selecteer op het sneltabblad **Hiërarchie van basisproductcodes** in het veld **Categoriehiërarchie** de optie **Intrastat**.
5. Selecteer in het veld **Transactiecode** de transactiecode voor eigenschapsoverdrachten. Deze code wordt gebruikt voor transacties die tot een werkelijke of geplande eigendomsoverdracht tegen vergoeding (financieel of anders) leiden. De code kan ook worden gebruikt voor correcties. Bedrijven in Polen gebruiken transactiecodes die uit twee cijfers bestaan.
6. Selecteer in het veld **Creditnota** de transactiecode voor de retourzending van goederen.
7. Geef in het tabblad **Eigenschappen land/regio** in het veld **Land/regio** een overzicht weer van alle landen of regio's waarmee uw organisatie zaken doet. Selecteer **EU** voor elk land of elke regio dat deel uitmaakt van de EU, in het veld **Land-/regiotype**, zodat het land in het Intrastat-rapport wordt weergegeven. Selecteer voor Polen **Binnenlands** in het veld **Land-/regiotype**.
8. Op het tabblad **Agent** op het sneltabblad **Agent** voert u in de sectie **Btw** in het veld **Btw-vrijstellingsnummer** het getal **420000** in om de eenheidscode aan te geven waaraan de Intrastat-aangifte is gericht.
9. Voer op het tabblad **Contactpersoon** de voor- en achternaam, het telefoonnummer, het faxnummer en het e-mailadres in van de persoon die de aangifte indient.
10. Op het tabblad **Nummerreeksen** geeft u in het veld **Nummerreekscode** voor de verwijzing **XML-bestandsnummer** een niet-opeenvolgende nummerreeks in van maximaal negen tekens. Dit veld wordt gebruikt om automatisch een waarde te genereren voor het veld **Aangifte-id** in het Intrastat-rapport.

## <a name="set-up-product-parameters-for-the-intrastat-declaration"></a>Productparameters voor de Intrastat-aangifte instellen

1. Ga naar **Productgegevensbeheer** > **Producten** > **Vrijgegeven producten**.
2. Selecteer een product in het raster.
3. Selecteer in het sneltabblad **Buitenlandse handel** in het gedeelte **Intrastat** in het veld **Basisproduct** de juiste NGP-code. De naam van het basisproduct wordt in het veld **Omschrijving van basisproducten** afgedrukt op het Intrastat-rapport.
4. Selecteer in de sectie **Herkomst** in het veld **Land/regio** het land of de regio van herkomst van het product.
5. Voer in het sneltabblad **Voorraad beheren** in het veld **Nettogewicht** het gewicht van het product in kilogram in.

## <a name="set-up-compression-of-intrastat"></a>Compressie van Intrastat instellen

-   Ga naar **Belasting** > **Instellingen** > **Buitenlandse handel** > **Compressie van Intrastat** en selecteer de velden die moeten worden vergeleken tijdens het samenvatten van de Intrastat-informatie. Selecteer voor de Poolse Intrastat de volgende velden:

    - Basisproduct
    - Transactiecode
    - Land/regio van oorsprong
    - Transport
    - Leveringsvoorwaarden
    - Land/regio van afzender
    - Land/regio
    - Correctie
    - Btw-nummer
    - Richting
    - Factuur

## <a name="set-up-the-transport-method-and-delivery-terms"></a>De transportmethode en leveringsvoorwaarden instellen

1.  Transportcodes instellen.

    1. Ga naar **Belasting** > **Instellingen** > **Buitenlandse handel** > **Transportmethoden**.
    2. Selecteer **Nieuw** in het actievenster.
    3. Typ een unieke code in het veld **Transport**. Poolse bedrijven gebruiken transactiecodes die uit één cijfer bestaan.

2.  Intrastat-codes voor levering instellen.

    1. Ga naar **Inkoopbeheer** > **Instellingen** > **Distributie** > **Leveringsvoorwaarden**.
    2. Selecteer een verzameling leveringsvoorwaarden in het raster.
    3. Voer op het sneltabblad **Algemeen** in het veld **Intrastat-code** een unieke code in.

## <a name="intrastat-transfer"></a>Intrastat-overboeking

In het actievenster op de pagina **Intrastat** kunt u **Overboeking** selecteren om de informatie over intracommunautaire handel automatisch over te brengen van uw verkooporders, vrije-tekstfacturen, inkooporders, leveranciersfacturen, leveranciersproductontvangstbonnen, projectfacturen en overboekingsorders. Alleen documenten met een EU-land als land of regio van bestemming of consignatie worden overgebracht.

U kunt ook handmatig transacties invoeren door **Nieuw** te selecteren in het actievenster.

### <a name="generate-an-intrastat-report"></a>Een Intrastat-rapport genereren

1. Ga naar **Belasting** > **Aangiften** > **Buitenlandse handel** > **Intrastat**.
2. Selecteer **Uitvoer** &gt; **Rapport** in het actievenster.
3. Stel in het dialoogvenster **Intrastat-rapport** de volgende velden in.

    | Veld | Description |
    |-------------------------|-------------------------|
    | Begindatum | Selecteer de begindatum voor het rapport. |
    | Bestand genereren | Stel deze optie in op **Ja** om een .xml-bestand voor uw Intrastat-rapport te genereren. |
    | Bestandsnaam | Voer de naam van het .xml-bestand in. |
    | Rapport genereren | Stel deze optie in op **Ja** om een .xlsx-bestand voor uw Intrastat-rapport te genereren. |
    | Rapportbestandsnaam | De naam van het .xlsx-bestand invoeren. |
    | Richting | Selecteer **Ontvangsten** voor een rapport over intracommunautaire ontvangsten.</br>Selecteer **Verzendingen** voor een rapport over intracommunautaire verzendingen. |
    | Aangifte-id | De document-id wordt automatisch gegenereerd en kan worden bijgewerkt. |
    | Type aangifte | Selecteer **Aangifte** voor een oorspronkelijke aangifte.</br>Selecteer **Aangiftecorrectie – vervanging** voor een correctieaangifte die is bedoeld om een bestaande, eerder ingediende oorspronkelijke of correctieaangifte volledig te vervangen. |
    | Plaats waar het document is gemaakt | Voer de waarde in die moet worden afgedrukt in het veld **Miejscowosc** op de Intrastat-aangifte. |
    | Datum waarop het document is gemaakt | Voer de waarde in die moet worden afgedrukt in het veld **Deklaracja Data** op de Intrastat-aangifte. |
    | Documentnummer | Voer de waarde in die moet worden afgedrukt in het veld **Numer** op de Intrastat-aangifte. |
    | Documentversie | Voer de waarde in die moet worden afgedrukt in het veld **Wersja** op de Intrastat-aangifte. |

4. Selecteer **OK** en controleer de gegenereerde rapporten.

## <a name="example"></a>Voorbeeld

Dit voorbeeld laat zien hoe u ontvangsten en verzendingen voor Intrastat kunt boeken door de rechtspersoon **DEMF** te gebruiken.

### <a name="preliminary-setup"></a>Voorlopige instellingen

Importeer de laatste versie van de volgende ER-configuraties (Elektronische Rapportage):

   - Intrastat-model
   - Intrastat-rapport
   - Intrastat (PL)

### <a name="set-up-a-company-address"></a>Een bedrijfsadres instellen

1. Ga naar **Organisatiebeheer** > **Globaal adresboek** > **Adressen** > **Instellingen adres**.
2. Selecteer **Nieuw** op het tabblad **Plaats**.
3. Selecteer in het veld **Land/regio** de waarde **POL**.
4. Typ **Warschau** in het veld **Plaats**.
5. Selecteer **Nieuw** op het tabblad **Postcode**.
6. Selecteer in het veld **Land/regio** de waarde **POL**.
7. Selecteer in het veld **Plaats** de stad **Warschau**.
8. Typ in het veld **Postcode** de postcode **00-844**.
9. Ga naar **Organisatiebeheer** > **Organisaties** > **Rechtspersonen** en selecteer de rechtspersoon van **DEMF**.
10. Selecteer in het sneltabblad **Adressen** de optie **Bewerken**.
11. Selecteer in het veld **Land/regio** de waarde **POL**.
12. Selecteer in het veld **Postcode** de postcode **31-111**.
13. Voer in het veld **Straat** het adres **Statystyczna 22/1** in.
14. Selecteer in het veld **Plaats** de stad **Warschau**.
15. Selecteer **OK**.

## <a name="set-up-a-vat-id-and-an-enterprise-number-code-for-your-company"></a>Een btw-nummer en een bedrijfsnummercode instellen voor uw bedrijf

### <a name="create-registration-types-for-company-codes"></a>Registratietypen voor bedrijfscodes maken

1. Ga naar **Organisatiebeheer** > **Globaal adresboek** > **Registratietypen** > **Registratietypen**.
2. Selecteer in het actievenster de optie **Nieuw** om een registratietype te maken voor het btw-nummer (NIP-code).
3. Voer in het dialoogvenster **Gegevens van registratietype invoeren**, in het veld **Naam** **NIP** in.
4. Selecteer in het veld **Land/regio** de waarde **POL**.
5. Selecteer **Maken**.
6. Selecteer in het actievenster de optie **Nieuw** om een registratietype te maken voor het bedrijfsnummer (Regon-code).
7. Voer in het dialoogvenster **Gegevens van registratietype invoeren**, in het veld **Naam** de waarde **Regon** in.
8. Selecteer in het veld **Land/regio** de waarde **POL**.
9. Selecteer **Maken**.

### <a name="match-the-registration-types-with-registration-categories"></a>De registratietypen matchen aan registratiecategorieën

1. Ga naar **Organisatiebeheer** > **Globaal adresboek** > **Registratietypen** > **Registratiecategorieën**.
2. Selecteer **Nieuw** in het actievenster om een koppeling te maken tussen elk registratietype dat u hebt gemaakt en een registratiecategorie.

    - Voor het registratietype **NIP** selecteert u de registratiecategorie **Btw-nummer**.
    - Voor het registratietype **Regon** selecteert u de registratiecategorie **Bedrijfs-id (COID)**.

### <a name="set-up-a-vat-id-and-an-enterprise-number-for-your-company"></a>Een btw-nummer en een bedrijfsnummer instellen voor uw bedrijf

1. Ga naar **Organisatiebeheer** > **Organisaties** > **Rechtspersonen**.
2. Selecteer **DEMF** in het raster.
3. Selecteer in het actievenster **Registratie-id's**.
4. Selecteer op het sneltabblad **Registratie-id** de optie **Toevoegen**.
5. Selecteer in het veld **Registratietype** **NIP**.
6. Voer in het veld **Registratienummer** de waarde **1234567890** in.
7. Selecteer **Toevoegen**.
8. Selecteer in het veld **Registratietype** **Regon**.
9. Voer in het veld **Registratienummer** de waarde **12345678901234** in.

### <a name="set-up-a-number-sequence-code"></a>Een nummerreekscode instellen

1. Ga naar **Organisatiebeheer** > **Nummerreeksen** > **Nummerreeksen**.
2. In het actievenster op het tabblad **Nummerreeks** in de groep **Nieuw** selecteert u **Nummerreeks**.
3. Op het sneltabblad **Identificatie**, in het veld **Nummerreekscode**, voer **XML\_bestand** in.
4. Op het sneltabblad **Bereikparameters**, in het veld **Bereik**, selecteer **Bedrijf**.
5. Selecteer **DEMF** in het veld **Bedrijf**.
6. Op het sneltabblad **Segmenten** in het veld **Lengte** voor het segment **Alfanumeriek** typt u **4**.
7. Stel op het sneltabblad **Algemeen** in de sectie **Instellingen** de optie **Doorlopend** in op **Nee**.
8. Voer in de sectie **Nummertoewijzing** in het veld **Grootste** het getal **9999** in.

### <a name="set-up-foreign-trade-parameters"></a>Parameters voor buitenlandse handel instellen

1. Ga naar **Belasting** > **Instellingen** > **Buitenlandse handel** > **Parameters buitenlandse handel**.
2. Selecteer op het tabblad **Intrastat** op het sneltabblad **Algemeen** in het veld **Transactiecode** de waarde **11**.
3. Selecteer op het sneltabblad **Elektronische rapportage** in het veld **Toewijzing bestandsindeling** de waarde **Intrastat (PL)**.
4. Selecteer in het veld **Toewijzing rapportindeling** de waarde **Intrastat-rapport**.
5. Controleer of op het sneltabblad **Hiërarchie basisproductcodes** in het veld **Categoriehiërarchie** de waarde **Intrastat** is ingesteld.
6. Selecteer in het tabblad **Land-/regio eigenschappen** de waarde **Nieuw**.
7. Selecteer in het veld **Land/regio partij** de waarde **POL**. Selecteer daarna in het veld **Land-/regiotype** de waarde **Binnenlands**.
8. Selecteer in het veld **Land/regio partij** de waarde **DEU**. Selecteer daarna in het veld **Land-/regiotype** de waarde **EU**.
9. Op het tabblad **Agent** op het sneltabblad **Agent** in de sectie **Btw** voert u in het veld **Btw-vrijstellingsnummer** het getal **420000** in.
10. Voer op het tabblad **Contactpersoon** in het veld **Naam** de naam **Manish Chopra** in.
11. Voer in het veld **Telefoon** de waarde **425-555-5068** in.
12. Voer in het veld **Faxnummer** de waarde **425-555-5049** in.
13. Voer in het veld **E-mail** het adres **manishc@contoso.com** in.
14. Op het tabblad **Nummerreeksen** in het veld **Nummerreekscode** voor de referentie **XML-bestandsnummer** selecteert u **XML\_bestand**.

### <a name="set-up-product-information"></a>Productgegevens instellen

1. Ga naar **Productgegevensbeheer** > **Producten** > **Vrijgegeven** **producten**.
2. Selecteer **D0001** in het raster.
3. Selecteer in het sneltabblad **Buitenlandse handel** in het gedeelte **Intrastat** in het veld **Basisproduct** de waarde **100 200 30**.
4. Voer in het sneltabblad **Voorraad beheren** in het gedeelte **Gewichtmetingen** in het veld **Nettogewicht** de waarde **2** in.
5. Selecteer **Opslaan** in het actievenster.
6. Selecteer **D0003** in het raster.
7. Selecteer in het sneltabblad **Buitenlandse handel** in het gedeelte **Intrastat** in het veld **Basisproduct** de waarde **100 200 30**.
8. Selecteer in het gedeelte **Oorsprong** in het veld **Land/regio** de waarde **DEU**.
9. Voer in het sneltabblad **Voorraad beheren** in het gedeelte **Gewichtmetingen** in het veld **Nettogewicht** de waarde **5** in.
10. Selecteer **Opslaan** in het actievenster.

### <a name="change-the-site-address"></a>Het locatieadres wijzigen

1. Ga naar **Magazijnbeheer** > **Instellingen** > **Magazijn** > **Vestigingen**.
2. Selecteer **1** in het raster.
3. Selecteer in het sneltabblad **Adressen** de optie **Bewerken**.
4. Selecteer in het dialoogvenster **Adres bewerken** in het veld **Land/regio** de optie **POL**.
5. Selecteer **OK**.

### <a name="set-up-a-transport-method"></a>Een transportmethode instellen

1. Maak een transportmethode.

    1. Ga naar **Belasting** > **Instellingen** > **Buitenlandse handel** > **Transportmethoden**.
    2. Selecteer **Nieuw** in het actievenster.
    3. Typ in het veld **Transport** het cijfer **3**.
    4. Voer in het veld **Beschrijving** **Wegtransport** in.

2. Wijs de nieuwe transportmethode toe aan een leveringsmethode. Op deze manier stelt u de standaardwaarden in die worden gebruikt voor de transportmethode wanneer de bijbehorende leveringsmethode wordt geselecteerd.

    1. Ga naar **Inkoop en sourcing** > **Instellingen** > **Distributie** > **Leveringsmethoden**.
    2. Selecteer **10** in het raster.
    3. Selecteer op het sneltabblad **Buitenlandse handel** in het veld **Transport** de waarde **3**.

3. Selecteer de standaardleveringsmethode voor een klant.

    1. Ga naar **Debiteuren** > **Klanten** > **Alle klanten**.
    2. Selecteer **DE-016** in het raster.
    3. Selecteer op het sneltabblad **Factuur en levering** in het veld **Leveringsmethode** de optie **10**.

4. Selecteer de standaardleveringsmethode voor een leverancier.

    1. Ga naar **Leveranciers** > **Leveranciers** > **Alle leveranciers**.
    2. Selecteer **DE-001** in het raster.
    3. Selecteer op het sneltabblad **Factuur en levering** in het veld **Leveringsmethode** de optie **10**.

### <a name="set-up-codes-for-terms-of-delivery"></a>Codes voor leveringsvoorwaarden instellen

1. Stel een Intrastat-code in voor de leveringsvoorwaarden.

    1. Ga naar **Inkoopbeheer** > **Instellingen** > **Distributie** > **Leveringsvoorwaarden**.
    2. Selecteer **CIF** in het raster.
    3. Voer op het sneltabblad **Algemeen** in het veld **Intrastat** de optie **CIF** in.

2. Selecteer de standaardleveringsvoorwaarden voor een klant.

    1. Ga naar **Debiteuren** > **Klanten** > **Alle klanten**.
    2. Selecteer **DE-016** in het raster.
    3. Selecteer op het sneltabblad **Factuur en levering** in het veld **Leveringsvoorwaarden** de optie **CIF**.

3. Selecteer de standaardleveringsvoorwaarden voor een leverancier.

    1. Ga naar **Leveranciers** > **Leveranciers** > **Alle leveranciers**.
    2. Selecteer **DE-001** in het raster.
    3. Selecteer op het sneltabblad **Factuur en levering** in het veld **Leveringsvoorwaarden** de optie **CIF**.

### <a name="verify-an-eu-customers-tax-exempt-number-code"></a>De btw-vrijstellingsnummercode van een EU-klant controleren

1. Ga naar **Debiteuren** > **Klanten** > **Alle klanten**.
2. Selecteer **DE-016** in het raster.
3. Controleer op het Sneltabblad **Factuur en levering**, in de sectie **Btw** of het veld **Btw-vrijstellingsnummer** is ingesteld op **DE9012**.

### <a name="create-a-sales-order-with-an-eu-customer"></a>Een verkooporder aanmaken met een EU-klant

1. Ga naar **Klanten** > **Orders** > **Alle verkooporders**.
2. Selecteer **Nieuw** in het actievenster.
3. Selecteer in het dialoogvenster **Verkooporder maken** in het sneltabblad **Klant** in het gedeelte **Klant** in het veld **Klantaccount** de waarde **DE-016**.
4. Selecteer in het sneltabblad **Algemeen** in het gedeelte **Opslagdimensies** in het veld **Locatie** de waarde **1**.
5. Selecteer **11** in het veld **Magazijn**.
6. Controleer op het tabblad **Adres** of het veld **Adres** is ingesteld op **Teichgasse 12, Kiel, 24103, DEU** omdat de klant uit Duitsland afkomstig is.
7. Selecteer **OK**.
8. Controleer op het tabblad **Koptekst** op het sneltabblad **Levering** of het veld **Leveringsvoorwaarden** is ingesteld op **CIF** en of het veld **Leveringsmethode** is ingesteld op **10**.
9. Selecteer in het tabblad **Regels** in het sneltabblad **Verkooporderregels** in het veld **Artikelnummer** de waarde **D0001**. Voer daarna in het veld **Hoeveelheid** de waarde **8** in.
10. Controleer op het sneltabblad **Regelgegevens**, op het tabblad **Buitenlandse handel**, of het veld **Transactiecode** is ingesteld op **11**, het veld **Basisproduct** is ingesteld op **100 200 30**, en het veld **Land/regio van herkomst** is ingesteld op **POL**.
11. Selecteer **Opslaan** in het actievenster.
12. Selecteer in het actievenster op het tabblad **Factuur** in de groep **Genereren** de optie **Factuur**.
13. Selecteer in het dialoogvenster **Factuur boeken** op het sneltabblad **Parameters** in de sectie **Parameters** in het veld **Hoeveelheid** de optie **Alle**.
14. Selecteer op het sneltabblad **Instellingen** in het veld **Verkoopdatum** de optie **18-10-2021** (18 oktober 2021).
15. Selecteer **OK** om de factuur te boeken.

### <a name="transfer-the-transaction-to-the-intrastat-journal-and-review-the-result"></a>Boek de transactie over naar het Intrastat-journaal en controleer het resultaat

1. Ga naar **Belasting** > **Aangiften** > **Buitenlandse handel** > **Intrastat**.
2. Selecteer in het actievenster de optie **Overboeken**.
3. Stel in het dialoogvenster **Intrastat (overboeking)** in de sectie **Parameters** de optie **Klantfactuur** in op **Ja**.
4. Selecteer **Filter**.
5. Selecteer in het dialoogvenster **Intrastat-filter** op het tabblad **Bereik** de eerste regel en controleer of het veld **Veld** is ingesteld op **Datum**.
6. Selecteer in het veld **Criteria** de huidige datum.
7. Selecteer **OK** om het dialoogvenster **Intrastat-filter** te sluiten.
8. Selecteer **OK** om het dialoogvenster **Intrastat (overboeken)** te sluiten en het resultaat te controleren. De regel staat voor de verkooporder die u eerder hebt aangemaakt.

    ![Regel die staat voor de verkooporder op de Intrastat-pagina](media/intrastat_pl_1.png)

9. Selecteer de transactieregel en selecteer vervolgens het tabblad **Algemeen** om meer informatie te bekijken.

    ![Informatie over een verkooporder op het tabblad Algemeen van de Intrastat-pagina](media/intrastat_pl_2.png)

10. Selecteer in het actievenster **Uitvoer** > **Rapport**.
11. Selecteer in het dialoogvenster **Intrastat-rapport** op het sneltabblad **Parameters** in de sectie **Datum** in het veld **Begindatum** de eerste dag van de huidige maand.
12. Stel in het gedeelte **Exportopties** de optie **Bestand** **genereren** in op **Ja**. Voer in het veld **Bestandsnaam** vervolgens de vereiste naam in.
13. Stel de optie **Rapport genereren** in op **Ja**. Voer in het veld **Bestandsnaam rapport** vervolgens de vereiste naam in.
14. Selecteer **Verzendingen** in het veld **Richting**.
15. Controleer in de sectie **Bestandsindeling toewijzen** of het veld **Aangiftetype** is ingesteld op **Aangifte**.
16. Voer in het veld **Plaats waar het document is gemaakt** de stad **Krakau** in.
17. Selecteer in het veld **Datum waarop het document is gemaakt** de datum **19-10-2021** (19 oktober 2021).
18. Voer in het veld **Documentnummer** het getal **11** in.
19. Voer in het veld **Documentversie** het getal **22** in.
20. Selecteer **OK** en controleer het rapport dat in XML-indeling is gegenereerd. De volgende tabel bevat de waarden in het voorbeeldrapport.

    <table>
    <tbody>
    <tr>
    <td>
    <p><strong>Veldnaam</strong></p>
    </td>
    <td>
    <p><strong>Veldomschrijving</strong></p>
    </td>
    <td>
    <p><strong>Waarde</strong></p>
    </td>
    </tr>
    <tr>
    <td colspan="3">
    <p><strong>Informatie over het document</strong></p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Deklaracja Data</p>
    </td>
    <td>
    <p>De datum weergeven waarop het document is gemaakt.</p>
    </td>
    <td>
    <p>2021-10-19</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Miejscowosc</p>
    </td>
    <td>
    <p>De plaats waar het document is gemaakt.</p>
    </td>
    <td>
    <p>Krakau</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>LacznaLiczbaPozycji</p>
    </td>
    <td>
    <p>Het totale aantal artikelen.</p>
    </td>
    <td>
    <p>1</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>LacznaWartoscStatystyczna</p>
    </td>
    <td>
    <p>De totale statistische waarde.</p>
    </td>
    <td>
    <p>2632</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>LacznaWartoscFaktur</p>
    </td>
    <td>
    <p>De totale factuurwaarde.</p>
    </td>
    <td>
    <p>2632</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>UC</p>
    </td>
    <td>
    <p>De eenheidscode.</p>
    </td>
    <td>
    <p>420000</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Rodzaj</p>
    </td>
    <td>
    <p>Het type aangifte.</p>
    </td>
    <td>
    <p>D</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Wersja</p>
    </td>
    <td>
    <p>De documentversie.</p>
    </td>
    <td>
    <p>22</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Numer</p>
    </td>
    <td>
    <p>Het documentnummer.</p>
    </td>
    <td>
    <p>11</p>
    </td>
    </tr>
    <tr>
    <td width="191">
    <p>Miesiac</p>
    </td>
    <td width="330">
    <p>De referentiemaand.</p>
    </td>
    <td>
    <p>10</p>
    </td>
    </tr>
    <tr>
    <td width="191">
    <p>Rok</p>
    </td>
    <td width="330">
    <p>Het referentiejaar.</p>
    </td>
    <td>
    <p>2021</p>
    </td>
    </tr>
    <tr>
    <td width="191">
    <p>Typ</p>
    </td>
    <td width="330">
    <p>De rapportrichting.</p>
    </td>
    <td>
    <p>Wo</p>
    </td>
    </tr>
    <tr>
    <td width="191">
    <p>NrWlasny</p>
    </td>
    <td width="330">
    <p>De aangifte-id.</p>
    </td>
    <td>
    <p>21ISTDEMF-0001</p>
    </td>
    </tr>
    <tr>
    <td colspan="3">
    <p><strong>Informatie over het bedrijf</strong></p>
    </td>
    </tr>
    <tr>
    <td width="191">
    <p>Miejscowosc</p>
    </td>
    <td width="330">
    <p>De plaats waarin het bedrijf is gevestigd.</p>
    </td>
    <td>
    <p>Warschau</p>
    </td>
    </tr>
    <tr>
    <td width="191">
    <p>Regon</p>
    </td>
    <td width="330">
    <p>De Regon-code van het bedrijf.</p>
    </td>
    <td>
    <p>12345678901234</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Nip</p>
    </td>
    <td>
    <p>De NIP-code van het bedrijf.</p>
    </td>
    <td>
    <p>1234567890</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>KodPocztowy</p>
    </td>
    <td>
    <p>De postcode van het bedrijf.</p>
    </td>
    <td>
    <p>31-111</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>UlicaNumer</p>
    </td>
    <td>
    <p>De straat waar het bedrijf is gevestigd.</p>
    </td>
    <td>
    <p>Statystyczna 22/1</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Nazwa</p>
    </td>
    <td>
    <p>De naam van het bedrijf.</p>
    </td>
    <td>
    <p>Contoso Entertainment System Germany</p>
    </td>
    </tr>
    <tr>
    <td colspan="3">
    <p><strong>Informatie over het goed</strong></p>
    </td>
    </tr>
    <tr>
    <td>
    <p>WartoscStatystyczna</p>
    </td>
    <td>
    <p>De statistische waarde.</p>
    </td>
    <td>
    <p>2632</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>WartoscFaktury</p>
    </td>
    <td>
    <p>De factuurwaarde.</p>
    </td>
    <td>
    <p>2632</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>MasaNetto</p>
    </td>
    <td>
    <p>De netto massa.</p>
    </td>
    <td>
    <p>16</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>IdKontrahenta</p>
    </td>
    <td>
    <p>Het btw-nummer van de klant.</p>
    </td>
    <td>
    <p>DE9012</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>KodTowarowy</p>
    </td>
    <td>
    <p>De basisproductcode.</p>
    </td>
    <td>
    <p>10020030</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>RodzajTransakcji</p>
    </td>
    <td>
    <p>De transactiecode.</p>
    </td>
    <td>
    <p>11</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>WarunkiDostawy</p>
    </td>
    <td>
    <p>De voorwaarden voor de leveringsmethode.</p>
    </td>
    <td>
    <p>CIF</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>KrajPochodzeniaWysylki</p>
    </td>
    <td>
    <p>De code voor het land of de regio van verzending/bestemming.</p>
    </td>
    <td>
    <p>DE</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>OpisTowaru</p>
    </td>
    <td>
    <p>Een beschrijving van de basisproducten.</p>
    </td>
    <td>
    <p>Hardware</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>PozId</p>
    </td>
    <td>
    <p>Het artikelnummer.</p>
    </td>
    <td>
    <p>1</p>
    </td>
    </tr>
    <tr>
    <td colspan="3">
    <p><strong>Gegevens contactpersoon</strong></p>
    </td>
    </tr>
    <tr>
    <td>
    <p>E-mailadres</p>
    </td>
    <td>
    <p>Het e-mailadres van de indiener.</p>
    </td>
    <td>
    <p>manishc@contoso.com</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Faks</p>
    </td>
    <td>
    <p>Het faxnummer van de indiener.</p>
    </td>
    <td>
    <p>425-555-5049</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Telefon</p>
    </td>
    <td>
    <p>Het telefoonnummer van de indiener.</p>
    </td>
    <td>
    <p>425-555-5068</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>NazwiskoImie</p>
    </td>
    <td>
    <p>De naam van de indiener.</p>
    </td>
    <td>
    <p>Manish Chopra</p>
    </td>
    </tr>
    </tbody>
    </table>

21. Controleer het rapport dat in Excel-indeling gegenereerd wordt.

    ![Intrastat-rapport voor verzendingen](media/intrastat_pl_3.png)

### <a name="create-a-purchase-order"></a>Inkooporder maken

1. Ga naar **Leveranciers** > **Inkooporders** > **Alle inkooporders**.
2. Selecteer **Nieuw** in het actievenster.
3. Ga in het dialoogvenster **Inkooporder maken** naar het sneltabblad **Leveranciersrekening** en selecteer **DE-001**.
4. Selecteer **1** in het veld **Locatie**.
5. Selecteer **11** in het veld **Magazijn**.
6. Selecteer **OK**.
7. Controleer op het tabblad **Koptekst** op het sneltabblad **Levering** of het veld **Leveringsmethode** is ingesteld op **10** en of het veld **Leveringsvoorwaarden** is ingesteld op **CIF**.
8. Selecteer in het tabblad **Regels** in het sneltabblad **Inkooporderregels** in het veld **Artikelnummer** de waarde **D0003**. Voer daarna in het veld **Hoeveelheid** de waarde **6** in.
9. Controleer op het sneltabblad **Regelgegevens**, op het tabblad **Buitenlandse handel**, of het veld **Transactiecode** is ingesteld op **11**, het veld **Transport** is ingesteld op **3**, het veld **Basisproduct** is ingesteld op **100 200 30**, en het veld **Land/regio van herkomst** is ingesteld op **DEU**.
10. Selecteer in het actievenster in het tabblad **Inkoop** in de groep **Acties** de optie **Bevestigen**.
11. Selecteer in het actievenster op het tabblad **Factuur** in de groep **Genereren** de optie **Factuur**.
12. Selecteer **Standaard vanaf** in het actievenster en selecteer in het veld **Standaardhoeveelheid voor regels** de optie **Bestelde hoeveelheid**. Selecteer vervolgens **OK**.
13. Op het sneltabblad **Koptekst leveranciersfactuur**, in de sectie **Factuuridentificatie**, in het veld **Nummer** voert u het getal **00010** in.
14. Selecteer in de sectie **Factuurdatums** in het veld **Factuurdatum** de huidige datum. Deze datum wordt gebruikt voor Intrastat-overboeking.
15. Selecteer in het veld **Document ontvangen op datum** de datum **18-10-2021** (18 oktober 2021).
16. Als u de factuur wilt boeken, selecteert u **Boeken** vanuit het actievenster.

### <a name="create-an-intrastat-declaration-for-arrivals"></a>Een Intrastat-aangifte voor ontvangsten aanmaken

1. Ga naar **Belasting** > **Aangiften** > **Buitenlandse handel** > **Intrastat**.
2. Selecteer in het actievenster de optie **Overboeken**.
3. Stel in het dialoogvenster **Intrastat (overboeking)** de optie **Leveranciersfactuur** in op **Ja**.
4. Selecteer **OK** om de transacties over te boeken en het Intrastat-journaal vervolgens te bekijken.

    ![Regel die staat voor de inkooporder op de Intrastat-pagina](media/intrastat_pl_4.png)

5. Bekijk de informatie op het tabblad **Algemeen** voor de inkooporder.

    ![Informatie over een inkooporder op het tabblad Algemeen van de Intrastat-pagina](media/intrastat_pl_5.png)

6. Selecteer in het actievenster **Uitvoer** > **Rapport**.
7. Selecteer in het dialoogvenster **Intrastat-rapport** op het sneltabblad **Parameters** in de sectie **Datum** in het veld **Begindatum** de eerste dag van de huidige maand.
8. Stel in het gedeelte **Exportopties** de optie **Bestand genereren** in op **Ja**. Voer in het veld **Bestandsnaam** vervolgens de vereiste naam in.
9. Stel de optie **Rapport genereren** in op **Ja**. Voer in het veld **Bestandsnaam rapport** vervolgens de vereiste naam in.
10. Selecteer **Ontvangsten** in het veld **Richting**.
11. Controleer in de sectie **Bestandsindeling toewijzen** of het veld **Aangiftetype** is ingesteld op **Aangifte**.
12. Voer in het veld **Plaats waar het document is gemaakt** de stad **Krakau** in.
13. Selecteer in het veld **Datum waarop het document is gemaakt** de datum **19-10-2021** (19 oktober 2021).
14. Voer in het veld **Documentnummer** het getal **11** in.
15. Voer in het veld **Documentversie** het getal **22** in.
16. Selecteer **OK** en controleer het rapport dat in XML-indeling is gegenereerd. De volgende tabel bevat de waarden in het voorbeeldrapport.

    <table>
    <tbody>
    <tr>
    <td>
    <p><strong>Veldnaam</strong></p>
    </td>
    <td>
    <p><strong>Veldomschrijving</strong></p>
    </td>
    <td>
    <p><strong>Waarde</strong></p>
    </td>
    </tr>
    <tr>
    <td colspan="3">
    <p align=center><strong>Informatie over het document</strong></p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Deklaracja Data</p>
    </td>
    <td>
    <p>De datum weergeven waarop het document is gemaakt.</p>
    </td>
    <td>
    <p>2021-10-19</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Miejscowosc</p>
    </td>
    <td>
    <p>De plaats waar het document is gemaakt.</p>
    </td>
    <td>
    <p>Krakau</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>LacznaLiczbaPozycji</p>
    </td>
    <td>
    <p>Het totale aantal artikelen.</p>
    </td>
    <td>
    <p>1</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>LacznaWartoscStatystyczna</p>
    </td>
    <td>
    <p>De totale statistische waarde.</p>
    </td>
    <td>
    <p>965</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>LacznaWartoscFaktur</p>
    </td>
    <td>
    <p>De totale factuurwaarde.</p>
    </td>
    <td>
    <p>965</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>UC</p>
    </td>
    <td>
    <p>De eenheidscode.</p>
    </td>
    <td>
    <p>420000</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Rodzaj</p>
    </td>
    <td>
    <p>Het type aangifte.</p>
    </td>
    <td>
    <p>D</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Wersja</p>
    </td>
    <td>
    <p>De documentversie.</p>
    </td>
    <td>
    <p>22</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Numer</p>
    </td>
    <td>
    <p>Het documentnummer.</p>
    </td>
    <td>
    <p>11</p>
    </td>
    </tr>
    <tr>
    <td width="191">
    <p>Miesiac</p>
    </td>
    <td width="332">
    <p>De referentiemaand.</p>
    </td>
    <td>
    <p>10</p>
    </td>
    </tr>
    <tr>
    <td width="191">
    <p>Rok</p>
    </td>
    <td width="332">
    <p>Het referentiejaar.</p>
    </td>
    <td>
    <p>2021</p>
    </td>
    </tr>
    <tr>
    <td width="191">
    <p>Typ</p>
    </td>
    <td width="332">
    <p>De rapportrichting.</p>
    </td>
    <td>
    <p>W</p>
    </td>
    </tr>
    <tr>
    <td width="191">
    <p>NrWlasny</p>
    </td>
    <td width="332">
    <p>De aangifte-id.</p>
    </td>
    <td>
    <p>21ISTDEMF-0002</p>
    </td>
    </tr>
    <tr>
    <td colspan="3">
    <p align=center><strong>Informatie over het bedrijf</strong></p>
    </td>
    </tr>
    <tr>
    <td width="191">
    <p>Miejscowosc</p>
    </td>
    <td width="332">
    <p>De plaats waarin het bedrijf is gevestigd.</p>
    </td>
    <td>
    <p>Warschau</p>
    </td>
    </tr>
    <tr>
    <td width="191">
    <p>Regon</p>
    </td>
    <td width="332">
    <p>De Regon-code van het bedrijf.</p>
    </td>
    <td>
    <p>12345678901234</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Nip</p>
    </td>
    <td>
    <p>De NIP-code van het bedrijf.</p>
    </td>
    <td>
    <p>1234567890</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>KodPocztowy</p>
    </td>
    <td>
    <p>De postcode van het bedrijf.</p>
    </td>
    <td>
    <p>31-111</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>UlicaNumer</p>
    </td>
    <td>
    <p>De straat waar het bedrijf is gevestigd.</p>
    </td>
    <td>
    <p>Statystyczna 22/1</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Nazwa</p>
    </td>
    <td>
    <p>De naam van het bedrijf.</p>
    </td>
    <td>
    <p>Contoso Entertainment System Germany</p>
    </td>
    </tr>
    <tr>
    <td colspan="3">
    <p align=center><strong>Informatie over het goed</strong></p>
    </td>
    </tr>
    <tr>
    <td>
    <p>WartoscStatystyczna</p>
    </td>
    <td>
    <p>De statistische waarde.</p>
    </td>
    <td>
    <p>965</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>WartoscFaktury</p>
    </td>
    <td>
    <p>De factuurwaarde.</p>
    </td>
    <td>
    <p>965</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>MasaNetto</p>
    </td>
    <td>
    <p>De netto massa.</p>
    </td>
    <td>
    <p>30</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>KrajPochodzenia</p>
    </td>
    <td>
    <p>De code voor het land of de regio van herkomst.</p>
    </td>
    <td>
    <p>DE</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>RodzajTransportu</p>
    </td>
    <td>
    <p>De code voor de transportmethode.</p>
    </td>
    <td>
    <p>3</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>KodTowarowy</p>
    </td>
    <td>
    <p>De basisproductcode.</p>
    </td>
    <td>
    <p>10020030</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>RodzajTransakcji</p>
    </td>
    <td>
    <p>De transactiecode.</p>
    </td>
    <td>
    <p>11</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>WarunkiDostawy</p>
    </td>
    <td>
    <p>De voorwaarden voor de leveringsmethode.</p>
    </td>
    <td>
    <p>CIF</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>KrajPochodzeniaWysylki</p>
    </td>
    <td>
    <p>De code voor het land of de regio van verzending/bestemming.</p>
    </td>
    <td>
    <p>DE</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>OpisTowaru</p>
    </td>
    <td>
    <p>Een beschrijving van de basisproducten.</p>
    </td>
    <td>
    <p>Hardware</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>PozId</p>
    </td>
    <td>
    <p>Het artikelnummer.</p>
    </td>
    <td>
    <p>1</p>
    </td>
    </tr>
    <tr>
    <td colspan="3">
    <p align=center><strong>Gegevens contactpersoon</strong></p>
    </td>
    </tr>
    <tr>
    <td>
    <p>E-mailadres</p>
    </td>
    <td>
    <p>Het e-mailadres van de indiener.</p>
    </td>
    <td>
    <p>manishc@contoso.com</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Faks</p>
    </td>
    <td>
    <p>Het faxnummer van de indiener.</p>
    </td>
    <td>
    <p>425-555-5049</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Telefon</p>
    </td>
    <td>
    <p>Het telefoonnummer van de indiener.</p>
    </td>
    <td>
    <p>425-555-5068</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>NazwiskoImie</p>
    </td>
    <td>
    <p>De naam van de indiener.</p>
    </td>
    <td>
    <p>Manish Chopra</p>
    </td>
    </tr>
    </tbody>
    </table>

17. Controleer het rapport dat in Excel-indeling gegenereerd wordt.

    ![Intrastat-rapport over ontvangsten](media/intrastat_pl_6.png)
