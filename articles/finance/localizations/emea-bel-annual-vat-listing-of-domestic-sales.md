---
title: Jaarlijkse btw-lijst van binnenlandse verkopen
description: Dit onderwerp biedt informatie over de jaarlijkse btw-lijst met een aangifte van de binnenlandse verkopen of factuuromzet voor België.
author: andosip
ms.date: 09/09/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Belgium
ms.author: anasyash
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bea209f5a2d5db9cecff392b77818be2cf6f888b
ms.sourcegitcommit: 3f6cbf4fcbe0458b1515c98a1276b5d875c7eda7
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/10/2021
ms.locfileid: "7487063"
---
# <a name="annual-vat-listing-of-domestic-sales"></a>Jaarlijkse btw-lijst van binnenlandse verkopen

[!include [banner](../includes/banner.md)]

Het rapport **Factuuromzet** wordt eenmaal per jaar naar de belastingdienst verzonden. Het wordt gebruikt om de omzet aan te geven voor Belgische btw-geregistreerde klanten, als die omzet hoger is dan een bepaald bedrag. Het rapport bevat facturen van klanttransacties waarbij de klanten een ondernemingsnummer hebben dat is opgemaakt volgens de richtlijnen van de Belgische overheid.

De volgende velden worden weergegeven in het rapport **Factuuromzet**:

- Btw-totaal
- Totale omzet
- Referentie declarant
- Aantal clients
- Vervangen aangifte (indien nodig)
- Btw-nummer van bedrijf
- Bedrijfsnaam
- Postcode van bedrijf
- ISO-landcode van bedrijf
- Aangifteperiode
- Btw-nummer van klant
- Klantomzet
- Btw-bedrag van klant

## <a name="setup"></a>Instelling

### <a name="preliminary-steps"></a>Voorbereidende stappen

De laatste versie van de volgende ER-configuraties (Elektronische Rapportage) importeren:

  - Rapportmodel factuuromzet
  - Rapport factuuromzet (BE)

Meer informatie is te vinden in [ER-configuraties downloaden uit de Algemene opslagplaats van de configuratieservice](../../fin-ops-core/dev-itpro/analytics/er-download-configurations-global-repo.md).

### <a name="create-registration-types-for-company-codes"></a>Registratietypen voor bedrijfscodes maken

U moet twee registratietypen maken voor bedrijfscodes: een voor het btw-nummer en een voor het bedrijfsnummer.

1. Ga naar **Organisatiebeheer** > **Globaal adresboek** > **Registratietypen** > **Registratietypen**.
2. Selecteer in het actievenster de optie **Nieuw** om het registratietype te maken voor het btw-nummer.
3. In het dialoogvenster **Gegevens van registratietype invoeren**, in het veld **Naam**. Voer een naam in voor het nieuwe registratietype. Voer bijvoorbeeld **Btw-nummer** in.
4. Selecteer in het veld **Land/regio** de waarde **BEL**.
5. Selecteer **Maken**.
6. Selecteer in het actievenster de optie **Nieuw** om het registratietype te maken voor het bedrijfsnummer.
7. Voer in het dialoogvenster **Details registratietype invoeren** in het veld **Naam** een naam in voor het nieuwe registratietype. Voer bijvoorbeeld **ENTNUM** in.
8. Selecteer in het veld **Land/regio** de waarde **BEL**.
9. Selecteer **Maken**.

### <a name="match-the-registration-types-with-registration-categories"></a>De registratietypen matchen aan registratiecategorieën

1. Ga naar **Organisatiebeheer** > **Globaal adresboek** > **Registratietypen** > **Registratiecategorieën**.  
2. Voor het registratietype voor het btw-nummer selecteert u de registratiecategorie **Btw-nummer**.
3. Voor het registratietype voor het bedrijfsnummer selecteert u de registratiecategorie **Enterprise ID (COID)**.

### <a name="set-up-a-vat-id-and-enterprise-number-for-your-company"></a>Een btw-nummer en bedrijfsnummer instellen voor uw bedrijf

1. Ga naar **Organisatiebeheer** > **Organisaties** > **Rechtspersonen**.
2. Selecteer uw bedrijf in het raster.
3. Selecteer in het actievenster **Registratie-id's**.
4. Selecteer op het sneltabblad **Registratie-id** de optie **Toevoegen**.
5. Selecteer in het veld **Registratietype** één van de registratietypes die u eerder hebt gemaakt.
6. Voer het btw-nummer of bedrijfsnummer van uw bedrijf in, afhankelijk van het registratietype dat u in de vorige stap hebt geselecteerd.
7. Herhaal stap 4 tot en met 6 voor het andere registratietype dat u eerder hebt gemaakt.

### <a name="set-up-a-vat-id-and-enterprise-number-for-all-your-companys-belgian-customers"></a>Een btw-nummer en bedrijfsnummer instellen voor alle Belgische klanten uw bedrijf

1. Ga naar **Debiteuren** > **Klanten** > **Alle klanten**.
2. Selecteer in het actievenster **Registratie-id's**.
3. Selecteer op het sneltabblad **Registratie-id** de optie **Toevoegen**.
4. Selecteer in het veld **Registratietype** één van de registratietypes die u eerder hebt gemaakt.
5. Voer het btw-nummer of bedrijfsnummer van uw klant in, afhankelijk van het registratietype dat u in de vorige stap hebt geselecteerd.
6. Herhaal stap 3 tot en met 5 voor het andere registratietype dat u eerder hebt gemaakt.

### <a name="create-number-sequence-codes-for-the-invoice-turnover-report"></a>Nummerreekscodes maken voor het rapport Factuuromzet

1. Ga naar **Organisatiebeheer** > **Nummerreeksen** > **Nummerreeksen**.
2. Maak een nummerreeks.
3. Verwijder op het sneltabblad **Segmenten** alle regels en selecteer vervolgens **Toevoegen**.
4. Selecteer in het veld **Segment** de optie **Alfanumeriek**.
5. Voer in het veld **Waarde** **\#\#\#\#\#\#\#\#\#** in.
6. Stel in het gedeelte **Instellingen** in het sneltabblad **Algemeen** de optie **Doorlopend** in op **Ja**.
7. Ga naar **Grootboek** > **Grootboek instellen** > **Grootboekparameters**.
8. Selecteer op het tabblad **Nummerreeks** in het veld **Nummerreekscode** voor de referentie **Id van jaarlijkse verkooplijst** de nummerreeks die u zojuist hebt gemaakt.

## <a name="generate-the-invoice-turnover-report"></a>Rapport voor factuuromzet genereren

1. Ga naar **Belasting** > **Query's en rapporten** > **Btw-aangiften** > **Rapport factuuromzet - België**.
2. Stel in het dialoogvenster **Rapport factuuromzet** de volgende velden in.

    | Veld                                 | Beschrijving                                                                                                           |
    |---------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
    | Begindatum                             | De begindatum van het rapport selecteren.                                                                                  |
    | Einddatum                               | De einddatum van het rapport selecteren.                                                                                    |
    | Bedrag                                | Het minimumbedrag selecteren dat in het rapport moet worden opgenomen. Dit bedrag is het totale gefactureerde bedrag door de klant, exclusief btw. |
    | Bestand genereren                         | Stel deze optie in op **Ja** om een XML-bestand te genereren.                                                                  |
    | Bestandsnaam                             | Een naam voor het rapportbestand invoeren.                                                                                  |
    | Rapport genereren                       | Stel deze optie in op **Ja** om een XLSX-bestand te genereren.                                                                 |
    | Rapportbestandsnaam                      | Voer een naam in voor het .xlsx-bestand.                                                                                      |
    | Officiële aangifte                  | Stel deze optie in op **Ja** om aan te geven dat dit rapport definitief is.                                                     |
    | Vervangen aangifte factuuromzet | Als u een rapport moet vervangen, voert u het nummer in van de vervangen aangifte.                                           |
    | Indelingstoewijzing                        | Selecteer **Rapport factuuromzet (BE)** om het rapport **Factuuromzet** te genereren.                                  |

## <a name="example"></a>Voorbeeld

1. Download in [Microsoft Dynamics Lifecycle Services (LCS)](https://lcs.dynamics.com/Logon/Index) in de bibliotheek met gedeelde activa de laatste versie van de volgende ER-configuraties:

    - Rapportmodel factuuromzet
    - Rapport factuuromzet (BE)

2. Ga naar **Organisatiebeheer** > **Globaal adresboek** > **Registratietypen** > **Registratietypen** en voer deze stappen uit:

    1. Selecteer **Nieuw** in het actievenster.
    2. Voer in het dialoogvenster **Gegevens van registratietype invoeren**, in het veld **Naam**, een **Btw-nummer** in.
    3. Selecteer in het veld **Land/regio** de waarde **BEL**.
    4. Selecteer **Maken**.
    5. Selecteer **Nieuw** in het actievenster.
    6. Voer in het dialoogvenster **Gegevens van registratietype invoeren**, in het veld **Naam** de waarde **ENTNUM** in.
    7. Selecteer in het veld **Land/regio** de waarde **BEL**.
    8. Selecteer **Maken**.

3. Ga naar **Organisatiebeheer** > **Globaal adresboek** > **Registratietypen** > **Registratiecategorieën** en voer deze stappen uit:

    1. Selecteer **Nieuw** in het actievenster.
    2. Selecteer in het veld **Registratietype** **Btw-nummer**.
    3. Selecteer in het veld **Registratiecategorie** **Btw-nummer**.
    4. Selecteer **Nieuw** in het actievenster.
    5. Selecteer in het veld **Registratietype** **ENTNUM**.
    6. Selecteer in het veld **Registratiecategorie** **Enterprise ID (COID)**.

4. Ga naar **Organisatiebeheer** > **Globaal adresboek** > **Adressen** > **Instellingen adres** en voer deze stappen uit:

    1. Selecteer **Nieuw** op het tabblad **Postcodes**.
    2. Selecteer in het veld **Land/regio** de waarde **BEL**.
    3. Voer **B-1014** in het veld **Postcode** in.
    4. Selecteer **Opslaan** in het actievenster.

5. Ga naar **Organisatiebeheer** > **Organisaties** > **Rechtspersonen** en voer deze stappen uit:

    1. Selecteer **DEMF** in het raster.
    2. Selecteer in het sneltabblad **Adressen** de optie **Bewerken**.
    3. Selecteer in het dialoogvenster **Adres bewerken** in het veld **Land/regio** de optie **BEL**.
    4. Selecteer **B-1014** in het veld **Postcode** in.
    5. Voer het op het sneltabblad **Belastingregistratie** in het veld **Btw-registratienummer** **0466.158.640** in.
    6. Selecteer in het actievenster **Registratie-id's**.
    7. Selecteer op het sneltabblad **Registratie-id** de optie **Toevoegen**.
    8. Selecteer in het veld **Registratietype** **ENTNUM**.
    9. Voer in het veld **Registratienummer** de waarde **BTW BE 0466.158.640** in.
    10. Selecteer **Toevoegen**.
    11. Selecteer in het veld **Registratietype** **Btw-nummer**.
    12. Voer in het veld **Registratienummer** de waarde **BE 0466.158.640** in.

6. Ga naar **Belasting** > **Instellingen** > **Btw** > **BTW-vrijstellingsnummers**, en voer deze stappen uit:

    1. Selecteer **Nieuw** in het actievenster.
    2. Selecteer in het veld **Land/regio** de waarde **BEL**.
    3. Voer in het veld **BTW-vrijstellingsnummer** de waarde **BTW BE 0420.429.375** in.

7. Ga naar **Klanten** > **Klanten** > **Alle klanten** en ga als volgt te werk:

    1. Selecteer **DE-010** in het raster.
    2. Selecteer in het sneltabblad **Adressen** de optie **Bewerken**.
    3. Selecteer in het veld **Land/regio** de waarde **BEL**.
    4. Selecteer op het Sneltabblad **Factuur en levering**, in de sectie **Btw** in het veld **Btw-nummer** de optie **BTW BE 0420.429.375**.
    5. In het actievenster op het tabblad **Klant** in de sectie **Registratie** selecteer **Registratie-id's**.
    6. Selecteer op het sneltabblad **Registratie-id** de optie **Toevoegen**.
    7. Selecteer in het veld **Registratietype** **Btw-nummer**.
    8. Voer in het veld **Registratienummer** de waarde **BE 0420.429.375** in.
    9. Selecteer **Toevoegen**.
    10. Selecteer in het veld **Registratietype** **Btw-nummer**.
    11. Voer in het veld **Registratienummer** de waarde **BTW BE 0420.429.375** in.

8. Ga naar **Organisatiebeheer** > **Nummerreeksen** > **Nummerreeksen** en voer deze stappen uit:

    1. In het actievenster op het tabblad **Nummerreeks** in de sectie **Nieuw** selecteer **Nummerreeks**.
    2. Op het sneltabblad **Identificatie**, in het veld **Nummerreekscode**, voer **Gene\_BE01** in.
    3. Op het sneltabblad **Bereikparameters**, in het veld **Bereik**, selecteer **Bedrijf**.
    4. Selecteer **DEMF** in het veld **Bedrijf**.
    5. Verwijder op het sneltabblad **Segmenten** alle regels en selecteer vervolgens **Toevoegen**.
    6. Selecteer in het veld **Segment** de optie **Alfanumeriek**.
    7. Voer in het veld **Waarde** **\#\#\#\#\#\#\#\#\#** in.
    8. Op het sneltabblad **Algemeen** in de sectie **Instellingen**. Stel de optie **Continu** in op **Ja**.

9. Ga naar **Grootboek** > **Journaalinstellingen** > **Boekingsjournalen**. Selecteer **Maken** in het actievenster.
10. Ga naar **Grootboek** > **Grootboek instellen** > **Grootboekparameters**. Op het tabblad **Nummerreeks** in het veld **Nummerreekscode** voor de referentie **Id van jaarlijkse verkooplijst** selecteer **Gene\_BE01**.
11. Ga naar **Klanten** > **Facturen** > **Alle vrije-tekstfacturen**, en voer deze stappen uit:

    1. Selecteer **Nieuw** in het actievenster.
    2. Op het sneltabblad **Koptekst vrije-tekstfactuur**, in de sectie **Klant**, in het veld **Klantrekening**, selecteer **DE-010**.
    3. Op het sneltabblad **Factuurregels**, in het veld **Hoofdrekening**, selecteer **110130**.
    4. Zorg ervoor dat het veld **Btw-groep** is ingesteld op **AR-DOM**.
    5. Selecteer in het veld **Btw-groep item** de optie **VOL**.
    6. Voer in het veld **Eenheidsprijs** **100** in.
    7. Selecteer **Boeken** in het actievenster.
    8. Selecteer in het dialoogvenster **Vrije-tekstfactuur boeken** **OK**.

12. Ga naar **Belasting** > **Query's en rapporten** > **Btw-aangiften** > **Rapport factuuromzet - België** en voer deze stappen uit:

    1. Op het sneltabblad **Parameters**, in de sectie **Criteria**, in de velden **Begindatum** en **Einddatum**, stel het interval in voor het rapport dat overeenkomt met de datums van de vrije-tekstfactuur die u eerder hebt gemaakt.
    2. Stel in de sectie **Exportopties** de optie **Bestand genereren** in op **Ja**.
    3. In de sectie **Elektronische rapportage**, in het veld **Indelingstoewijzing**, selecteer **Rapport factuuromzet (BE)**.
    4. Selecteer **OK**, en controleer het bestand voor het rapport. De volgende tabel bevat de waarden voor het voorbeeldrapport.

        | Veldnaam                     | Waarde                                |
        |--------------------------------|--------------------------------------|
        | ClientListingsNbr              | 1                                    |
        | ClientListing VATAmountSum     | 19                                   |
        | TurnOverSum                    | 100                                  |
        | ClientsNbr                     | 1                                    |
        | SequenceNumber                 | 1                                    |
        | common:VATNumber               | 0466158640                           |
        | common:Name                    | Contoso Entertainment System Germany |
        | common:PostCode                | B-1014                               |
        | common:CountryCode             | BE                                   |
        | Client SequenceNumber          | 1                                    |
        | CompanyVATNumber issuedBy="BE" | 0420429375                           |
        | TurnOver                       | 100                                  |
        | VATAmount                      | 19                                   |

5. Controleer het rapport in .xlsx-indeling.

    ![Tabelomschrijving automatisch gegenereerd.](media/emea-bel-turnover-report.png)
    

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
