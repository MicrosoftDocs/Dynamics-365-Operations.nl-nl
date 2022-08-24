---
title: Btw-aangifte (Duitsland)
description: In dit artikel wordt beschreven hoe u een voorschot-btw-aangifte voor Duitsland kunt instellen en genereren in de officiële XML-indeling.
author: AdamTrukawka
ms.date: 03/10/2022
ms.topic: article
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: atrukawk
ms.search.validFrom: ''
ms.openlocfilehash: 8ee288a1ec7ae950bdff9da7d373e29daef74d3c
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/12/2022
ms.locfileid: "9269399"
---
# <a name="vat-declaration-germany"></a>Btw-aangifte (Duitsland)

[!include [banner](../includes/banner.md)]

In dit artikel wordt beschreven hoe u een voorschot-btw-aangifte voor Duitsland kunt instellen en genereren in de officiële XML-indeling. In dit artikel wordt ook uitgelegd hoe u een voorbeeld van de btw-aangifte kunt bekijken in Microsoft Excel.

Als u het rapport automatisch wilt genereren, maakt u voldoende btw-codes om een afzonderlijke btw-boekhouding te behouden voor elk vak in de voorschot-btw-aangifte. In de toepassingsspecifieke parameters van de ER-indeling (elektronische aangifte) voor de voorschot-btw-aangifte koppelt u bovendien btw-codes aan het zoekresultaat van de zoekopdrachten voor de vakken in de btw-aangifte.

Voor Duitsland moet u **Rapportveld zoeken** configureren. Zie de sectie [Toepassingsspecifieke parameters instellen voor btw-aangiftevelden](#set-up-application-specific-parameters-for-vat-declaration-fields) verderop in dit artikel voor meer informatie over het instellen van toepassingsspecifieke parameters.

In de volgende tabel ziet u in de kolom 'Opzoekresultaat' het opzoekresultaat dat vooraf is geconfigureerd voor een specifieke btw-aangifterij in de indeling voor de btw-aangifte. Gebruik deze informatie om btw-codes correct aan het opzoekresultaat en vervolgens aan de rij van de btw-aangifte te koppelen.

### <a name="vat-declaration-overview"></a><a name="vat-declaration-overview"></a>Overzicht van btw-aangifte

De voorschot-btw-aangifte in Duitsland bevat de volgende informatie.

**SECTIE – LEVERINGEN EN ANDERE SERVICES**

**Belastbare verkoop**

| Rij | Vak – Belastingbasis | Vak – belastingbedrag | Description                                                                                                                                      | Zoekresultaat                                                                             |
|-----|----------------|------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| 20  | 81             | Zonder code     | Belastbare verkoop tegen een btw-percentage van 19 procent.                                                                                                       | 20-TaxableSalesStandard</br>73-BadDebtsWriteOffStandard (81/50) – met minteken             |
| 21  | 86             | Zonder code     | Belastbare verkoop tegen een btw-percentage van 7 procent.                                                                                                        | 21-TaxableSalesReduced</br>73-BadDebtsWriteOffReduced (86/50) – met minteken               |
| 22  | 35             | 36               | Belastbare verkoop tegen andere btw-tarieven.                                                                                                                | 22-TaxableSalesOtherRates</br>73-BadDebtsWriteOffOtherRates (35/36/50) – met minteken      |
| 23  | 77             | *Geen belastingbedrag*  | Leveringen van land- en bosbouwbedrijven in overeenstemming met artikel 24 van de Duitse btw-wet (UStG) aan klanten met een btw-nummer. | 23-EUSalesAverageRate24</br>73-BadDebtsWriteOffEUSalesAverageRate24 (77/50) – met minteken |
| 24  | 76             | 80               | Verkoop waarvoor belasting moet worden betaald, overeenkomstig artikel 24 van de UStG (houtzagerijproducten, dranken en alcoholische vloeistoffen).                                | 24-SalesAverageRate24</br>73-BadDebtsWriteOffSalesAverageRate24 (76/80/50)                    |

**Belastingvrije verkopen met aftrek van invoerbelasting**

| Rij | Vak – Belastingbasis | Vak – belastingbedrag | Description                                                                       | Zoekresultaat                       |
|-----|----------------|------------------|-----------------------------------------------------------------------------------|-------------------------------------|
| 26  | 41             | *Geen belastingbedrag*  | Intracommunautaire leveringen aan klanten met een btw-nummer.                       | 26-EUSales                          |
| 27  | 44             | *Geen belastingbedrag*  | Intracommunautaire leveringen van nieuwe voertuigen aan inkopers zonder btw-nummer.    | 27-EUSalesNewVehicles               |
| 28  | 49             | *Geen belastingbedrag*  | Intracommunautaire leveringen van nieuwe voertuigen buiten een bedrijf                     | 28-EUSalesNewVehiclesOutsideCompany |
| 29  | 43             | *Geen belastingbedrag*  | Andere belastingvrije verkoop met een invoerbelastingaftrek, zoals exportleveringen. | 29-ExportOtherTaxFreeSales          |

**Belastingvrije verkopen zonder aftrek van invoerbelasting**

| Rij | Vak – Belastingbasis | Vak – belastingbedrag | Description                                            | Zoekresultaat                           |
|-----|----------------|------------------|--------------------------------------------------------|-----------------------------------------|
| 30  | 48             | *Geen belastingbedrag*  | Belastingvrije verkoop zonder invoerbelastingaftrek. | 30-TaxFreeSalesWithoutInputTaxDeduction |

**Intracommunautaire verwervingen**

| Rij | Vak – Belastingbasis | Vak – belastingbedrag | Description                                                                                                                   | Zoekresultaat                                                    |
|-----|----------------|------------------|-------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| 33  | 91             | *Geen belastingbedrag*  | Belastingvrije intracommunautaire verwervingen van sommige objecten en investeringsgoud.                                                    | 33-TaxFreeEUPurchase                                             |
| 34  | 89             | Zonder code     | Belastbare intracommunautaire verwervingen met een btw-tarief van 19 procent.                                                             | 34-EUPurchaseStandard</br>34-UseTaxEUPurchaseStandard (89/61)        |
| 35  | 93             | Zonder code     | Belastbare intracommunautaire verwervingen met een btw-tarief van 7 procent.                                                              | 35-EUPurchaseReduced</br>35-UseTaxEUPurchaseReduced (93/61)          |
| 36  | 95             | 98               | Belastbare intracommunautaire verwervingen tegen andere btw-tarieven.                                                                      | 36-EUPurchaseOtherRates</br>36-UseTaxEUPurchaseOtherRates (95/98/61) |
| 37  | 94             | 96               | Belastbare intracommunautaire verwervingen van nieuwe voertuigen van leveranciers die geen btw-nummer hebben, tegen het algemene btw-tarief. | 37-EUPurchaseVehicles</br>37-UseTaxEUPurchaseVehicles (94/96/61)     |

**SECTIE – BEGUNSTIGDE ALS BTW-DEBITEUR**

| Rij | Vak – Belastingbasis | Vak – belastingbedrag | Description                                                                        | Zoekresultaat                                                                                        |
|-----|----------------|------------------|------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| 40  | 46             | 47               | Andere services van een ondernemer, op basis van de rest van het Community-gebied.        | 40-BeneficiaryTaxDebtor</br>40-UseTaxBeneficiaryTaxDebtor (46/47/66)                                                                              |
| 41  | 73             | 74               | Verkoop die onder sectie 13b (2) nr. 3 van de UStG valt.                               | 41-BeneficiaryTaxDebtorRealEstateTransfer</br>41-UseTaxBeneficiaryTaxDebtorRealEstateTransfer (73/74/67) |
| 42  | 84             | 85               | Andere services die onder sectie 13b (2) nr. 1, 2 en 4 tot en met 12 van de UStG vallen. | 42-BeneficiaryTaxDebtorOther</br>42-UseTaxBeneficiaryTaxDebtorOther (84/85/67)                           |

**SECTIE – BIJKOMENDE INFORMATIE OVER VERKOOP**

| Rij | Vak – Belastingbasis  | Vak – belastingbedrag | Description                                                                                                | Zoekresultaat                                                                                    |
|-----|-----------------|------------------|------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| 48  | 42              | *Geen belastingbedrag*  | Leveringen door de eerste klant in het geval van intracommunautaire driehoekstransacties.                   | 48-DeliveriesFirstCustomerEUTriangular                                                           |
| 49  | 60              | *Geen belastingbedrag*  | Belastbare verkoop van de uitvoerende ondernemer waarvoor de ontvanger van de service de btw is verschuldigd. | 49-SalesServicesReverseCharge                                                                    |
| 50  | 21              | *Geen belastingbedrag*  | Andere niet-belastbare services.                                                                                | 50-OtherServicesNonTaxable                                                                       |
| 51  | 45              | *Geen belastingbedrag*  | Andere niet-belastbare verkoop als de prestatieplaats zich niet in Duitsland bevindt.                                    | 51-OtherSalesNonTaxable                                                                          |
| 52  | *Geen belastingbedrag* | *Geen belastingbedrag*  | Btw.                                                                                                       | Rij 20 + Rij 21 + Rij 22 + Rij 24 + Rij 34 + Rij 35 + Rij 36 + Rij 37 + Rij 40 + Rij 41 + Rij 42 + Rij 42 |

**SECTIE – AFTREKBARE INVOERBELASTING**

| Rij | Vak – belastingbedrag | Description                                                                                                | Zoekresultaat                                                                                                                                                                |
|-----|------------------|------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 55  | 66               | Bedragen voor invoerfactuurbelasting van andere bedrijven, services en intracommunautaire driehoekstransacties.     | 55-InputTax 40-UseTaxBeneficiaryTaxDebtor (46/47/66)</br>74-BadDebtsWriteOffInputTax (66/37) – met minteken                                                                   |
| 56  | 61               | Invoerbelastingbedragen uit de intracommunautaire verwerving van goederen.                                           | 56-InputTaxEUPurchase 34-UseTaxEUPurchaseStandard (89/61)</br>35-UseTaxEUPurchaseReduced (93/61)</br>36-UseTaxEUPurchaseOtherRates (95/98/61)</br>37-UseTaxEUPurchaseVehicles (94/96/61) |
| 57  | 62               | Gemaakte invoerbelasting.                                                                                 | 57-InputTaxImport                                                                                                                                                            |
| 58  | 67               | Invoerbelastingbedragen van services overeenkomstig artikel 13b van de UStG.                                        | 58-InputTaxServices</br>41-UseTaxBeneficiaryTaxDebtorRealEstateTransfer (73/74/67)</br>42-UseTaxBeneficiaryTaxDebtorOther (84/85/67)                                                 |
| 59  | 63               | Invoerbelastingbedragen die worden berekend volgens de algemene gemiddelde tarieven.                                  | 59-InputTaxAverageRates</br>74-BadDebtsWriteOffInputTaxAverageRates (63/37) – met minteken                                                                                    |
| 60  | 59               | Btw-inhouding voor intracommunautaire leveringen van nieuwe voertuigen buiten een bedrijf en kleine ondernemingen. | 60-InputTaxEUPurchaseNewVehicles</br>74-BadDebtsWriteOffInputTaxEUPurchaseNewVehicles (59/37) – met minteken                                                                  |
| 61  | 64               | Correctie van de invoerbelastingaftrek.                                                                     | 61-InputTaxCorrection                                                                                                                                                        |
| 62  | \-               | Het resterende bedrag.                                                                                      | Rij 52 – Rij 55 – Rij 56 – Rij 57 – Rij 58 – Rij 50 – Rij 60 – Rij 61                                                                                                        |

**SECTIE – OVERIGE BTW-BEDRAGEN**

| Rij | Vak – belastingbedrag | Description                                                                                                                                                                                                                                                         | Zoekresultaat                                 |
|-----|------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| 64  | 65               | Belasting vanwege een wijziging in de vorm van belastingheffing en extra belasting op betalingen met verlaagde belasting als gevolg van een wijziging in het btw-tarief.                                                                                                                                        | 64-AdditionalTaxDueChangeTaxRate              |
| 65  | 69               | Onjuiste of niet-gerechtvaardigde belastingbedragen die op facturen worden weergegeven en belastingbedragen die verschuldigd zijn overeenkomstig sectie 6a (4) zin 2, sectie 17 (1) zin 7 of sectie 25b (2) van de UStG of die verschuldigd zijn door een uitbestedingsbedrijf of depothouder. | 65-TaxDecreaseCorrection                      |
| 67  | 39               | Korting op de vaste speciale voorschotbetaling voor permanente verlenging. Deze rij wordt meestal alleen gevuld met de laatste voorschotmelding van de btw-periode.                                                                                                  | Gebruikersinvoerparameter in het rapportdialoogvenster |
| 68  | 83               | De resterende voorschot-btw-betaling en het resterende overtollige bedrag. Neem een minteken op vóór het bedrag.                                                                                                                                                          | Rij 62 + Rij 64 – Rij 65 – Rij 66             |

**SECTIE – BIJKOMENDE INFORMATIE OVER AFTREK**

| Rij | Vak – Belastingbasis | Vak – belastingbedrag | Description                                                            | Zoekresultaat                                                                                                                                                                                                    |
|-----|----------------|------------------|------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 73  | 50             | \-               | Reductie van de btw-basis op regels 20 tot en met 24.                      | 73-BadDebtsWriteOffStandard (81/50)</br>73-BadDebtsWriteOffReduced (86/50)</br>73-BadDebtsWriteOffOtherRates (35/36/50)</br>73-BadDebtsWriteOffEUSalesAverageRate24 (77/50)</br>73-BadDebtsWriteOffSalesAverageRate24 (76/80/50) |
| 74  | \-             | 37               | Reductie van het aftrekbare invoerbelastingbedrag op regels 55, 59 en 60. | 74-BadDebtsWriteOffInputTax (66/37)</br>74-BadDebtsWriteOffInputTaxAverageRates (63/37)</br>74-BadDebtsWriteOffInputTaxEUPurchaseNewVehicles (59/37)                                                                     |

#### <a name="purchase-reverse-charge-vat"></a>Omgekeerde toeslag van te vorderen btw

Als u btw-codes configureert om inkomende omgekeerde toeslagen te boeken via gebruiksbelasting, koppelt u uw btw-codes aan het opzoekresultaat van **Rapportveld zoeken** dat "UseTax" in de naam heeft.

U kunt ook twee afzonderlijke btw-codes configureren: één voor te betalen btw en één voor btw-aftrek. Koppel vervolgens elke code aan de bijbehorende opzoekresultaten voor **Rapportveld zoeken**.

Zo configureert u bijvoorbeeld voor belastbare intracommunautaire verwervingen met een standaardtarief btw-code **UT_S_EU** met gebruiksbelasting en koppelt u deze aan het opzoekresultaat **34-UseTaxEUPurchaseStandard** van **Rapportveld zoeken**. In dit geval worden bedragen die gebruikmaken van btw-code **UT_S_EU** weergegeven in de vakken 089 en 061 (rijen 34 en 56).

U kunt ook twee btw-codes configureren:

  - **VAT_S_EU**, met een btw-tariefwaarde van -19 procent
  - **InVAT_S_EU**, met een btw-tariefwaarde van 19 procent

Vervolgens koppelt u als volgt de codes aan opzoekresultaten van **Rapportveld zoeken**:

  - Koppel **VAT_S_EU** aan het opzoekresultaat **34-EUPurchaseStandard**.
  - Koppel **InVAT_S_EU** aan het opzoekresultaat **56-InputTaxEUPurchase**.

In dit geval worden bedragen die gebruikmaken van btw-code **VAT_S_EU** weergegeven in vak 089 (rij 34). Bedragen die gebruikmaken van de btw-code **InVAT_S_EU** worden weergegeven in vak 061 (rij 56).

Zie [Terugboekingen](emea-reverse-charge.md) voor meer informatie over het configureren van omgekeerde toeslagen.

## <a name="configure-system-parameters"></a>Systeemparameters configureren

Voor het genereren van een btw-aangifte moet u het btw-nummer (Steuernummer) van uw organisatie configureren.

1. Ga naar **Organisatiebeheer** > **Organisaties** > **Rechtspersonen**.
2. Selecteer de rechtspersoon en selecteer **Registratie-id's**.
3. Selecteer of maak het adres in Duitsland en selecteer vervolgens op het sneltabblad **Registratie-id's** de optie **Toevoegen**.
4. Selecteer in het veld **Registratietype** het registratietype dat is toegewezen aan Duitsland en dat gebruikmaakt van de registratiecategorie **Ondernemings-id (COID)**.
5. Voer het btw-nummer in het veld **Registratienummer** in.
6. Voer op het tabblad **Algemeen** in het veld **Geldig vanaf** de datum in waarop het nummer van kracht wordt.

Zie [Registratie-id's](emea-registration-ids.md) voor meer informatie over het instellen van registratiecategorieën en registratietypen.

## <a name="set-up-a-vat-declaration-for-germany"></a>Een Btw-aangifte instellen voor Duitsland

### <a name="import-er-configurations"></a>ER-configuraties importeren

Open de werkruimte **Elektronische rapportage** en mporteer de volgende versies of een latere versie van deze ER-indelingen:

   - Btw-aangifte Excel (DE).version.101.16.12.xml
   - Btw-aangifte XML (DE).version.101.16.xml

### <a name="set-up-application-specific-parameters-for-vat-declaration-fields"></a><a name="set-up-application-specific-parameters-for-vat-declaration-fields"></a>Toepassingsspecifieke parameters instellen voor btw-aangiftevelden

Als u automatisch een btw-aangifte wilt genereren, koppelt u btw-codes aan de toepassing en zoekresultaten in de ER-configuratie.

> [!NOTE]
> U kunt het beste de functie **Toepassingsspecifieke parameters van vorige versies van ER-indelingen** inschakelen in de werkruimte **Functiebeheer**. Wanneer deze functie is ingeschakeld, worden parameters die zijn geconfigureerd voor de eerdere versie van een ER-indeling automatisch van toepassing op de latere versie van dezelfde indeling. Als deze functie niet is ingeschakeld, moet u toepassingsspecifieke parameters expliciet voor elke indelingsversie configureren. De functie **Toepassingsspecifieke parameters van vorige versies van ER-indelingen** is beschikbaar in de werkruimte **Functiebeheer** vanaf Finance-versie 10.0.23. Zie [De parameters voor een ER-indeling per rechtspersoon instellen](../../fin-ops-core/dev-itpro/analytics/er-app-specific-parameters-set-up.md) voor meer informatie over het instellen van de parameters van een ER-indeling voor elke rechtspersoon.

Volg deze stappen om te definiëren door welke btw-codes welke vakken worden gegenereerd in de btw-aangifte.

1. Ga naar **Werkruimten** > **Elektronische rapportage** en selecteer **Rapportageconfiguraties**.
2. Selecteer de configuratie **Btw-aangifte XML (DE)** en selecteer vervolgens **Configuraties \> Toepassingsspecifieke parameters instellen**.
3. Selecteer op de pagina **Toepassingsspecifieke parameters** op het sneltabblad **Zoekopdrachten** de optie **Rapportveld zoeken**.
4. Stel op het sneltabblad **Voorwaarden** de volgende velden in om de btw-codes en rapportvelden te koppelen.

    | Veld                  | Description                                                                                                                                                                                                                                                                                                          |
    |------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | Zoekresultaat          | Selecteer de waarde van het rapportveld. Zie de sectie eerder in dit artikel [Overzicht van btw-aangifte](#vat-declaration-overview) voor meer informatie over de waarden en hun toewijzing aan rijen voor btw-aangifte.                                                                                               |
    | Belastingcode               | Selecteer de btw-code die u aan het rapportveld wilt koppelen. Geboekte btw-transacties die de geselecteerde btw-code gebruiken, worden in het desbetreffende aangiftevak verzameld. Het is raadzaam om btw-codes zo te scheiden, dat één btw-code bedragen in slechts één aangiftevak genereert. |
    | Transactieclassificatie | Als u voldoende btw-codes hebt gemaakt om het aangiftevak te bepalen, selecteert u **\*Niet leeg\***. Als u niet voldoende btw-codes hebt gegenereerd zodat één btw-code bedragen in slechts één aangiftevak genereert, kunt u een transactieclassificatie instellen. De volgende transactieclassificaties zijn beschikbaar:</br>-   **Aankoop**</br>-   **PurchaseExempt** (inkoop met belastingvrijstelling)</br>-   **PurchaseReverseCharge** (terug te ontvangen btw van een omgekeerde toeslag op een inkoopfactuur)</br>-   **Sales**</br>-   **SalesExempt** (verkoop met btw-vrijstelling)</br>-   **SalesReverseCharge** (te betalen btw van een omgekeerde toeslag op een inkoopfactuur of een omgekeerde toeslag op een verkoopfactuur)</br>-   **Gebruiksbelasting**. </br>Voor elke transactieclassificatie is er ook een classificatie voor de creditnota beschikbaar. Een van deze classificaties is bijvoorbeeld **PurchaseCreditNote** (creditnota voor inkoop).</br>Zorg ervoor dat u twee regels maakt voor elke btw-code: een met de waarde van de transactieclassificatie en een met de transactieclassificatie voor de waarde van de creditnota. |

    > [!NOTE]
    > Koppel alle btw-codes aan opzoekresultaten. Als btw-codes geen waarden op de btw-aangifte moeten genereren, koppelt u deze aan het opzoekresultaat **Overige**.

    ![Pagina Toepassingsspecifieke parameters](media/69ecb881f12819259ca166b9b98b8303.jpg)

5. Wijzig in het veld **Status** de waarde in **Voltooid**.
6. Selecteer in het actievenster de optie **Exporteren** om de instellingen van de toepassingsspecifieke parameters te exporteren.
7. Selecteer de configuratie **Btw-aangifte Excel (DE)** en selecteer vervolgens in het actievenster de optie **Importeren** om de parameters te importeren die u hebt geconfigureerd voor **BTW-aangifte XML (DE)**.
8. Selecteer **Voltooid** in het veld **Status**.

### <a name="set-up-the-vat-reporting-format-for-preview-amounts-in-excel"></a>De notatie voor btw-aangifte instellen voor voorbeeldbedragen in Excel

1. Zoek in de werkruimte **Functiebeheer** de functie **Indelingsrapporten voor btw-aangifte** en schakel deze in.
2. Ga naar **Grootboek** > **Instellingen** > **Grootboekparameters**.
3. Selecteer op het tabblad **Btw** op het sneltabblad **Btw-opties** in het veld **Toewijzing indeling btw-overzicht** de optie **Btw-aangifte Excel (DE)**.

   Deze indeling wordt afgedrukt wanneer u het rapport **Btw rapporteren voor vereffeningsperiode** uitvoert. Deze wordt ook afgedrukt wanneer u **Afdrukken** selecteert op de pagina **Btw-betalingen**.

4. Selecteer op de pagina **Belastingdienst** de belastingdienst en selecteer vervolgens in het veld **Rapportindeling** de optie **Standaard**.

Als u de btw-aangifte configureert in een rechtspersoon met meerdere [btw-registraties](emea-reporting-for-multiple-vat-registrations.md), volgt u deze stappen:

1. Ga naar **Grootboek** > **Instellingen** > **Grootboekparameters**.
2. Selecteer op het tabblad **Btw-aangifte** op het sneltabblad **Elektronische aangifte voor landen/regio's** op de regel voor **DEU** de ER-indeling **Btw-aangifte Excel (DE)**.

## <a name="set-up-electronic-messages"></a>Elektronische berichten instellen

### <a name="download-and-import-the-data-package-that-has-example-settings-for-electronic-messages"></a>Het gegevenspakket met voorbeeldinstellingen voor elektronische berichten downloaden en importeren

Het gegevenspakket bevat elektronische berichtinstellingen die worden gebruikt om de btw-aangifte te genereren in de XML-indeling en vervolgens een voorbeeld hiervan weer te geven in Excel. U kunt deze instellingen uitbreiden of uw eigen instellingen maken. Zie [Elektronische berichten](../general-ledger/electronic-messaging.md) voor meer informatie over het werken met elektronische berichten en het maken van uw eigen instellingen.

1. Selecteer in [Microsoft Dynamics Lifecycle Services (LCS)](https://lcs.dynamics.com/v2) in de Bibliotheek voor gedeelde activa de optie **Gegevenspakket** als activatype en download vervolgens **DE EM-pakket voor btw-aangifte**. De naam van het gedownloade bestand is **DE VAT declaration EM package.zip**.
2. Selecteer in Dynamics 365 Finance, in het werkgebied **Gegevensbeheer**, de optie **Importeren**.
3. Voer op het sneltabblad **Importeren** in het veld **Groepsnaam** een naam in voor de taak.
4. Selecteer op het sneltabblad **Geselecteerde entiteiten** de optie **Bestand toevoegen**.
5. Controleer in het dialoogvenster **Bestand toevoegen** of het veld **Brongegevensindeling** is ingesteld op **Pakket**, selecteer **Uploaden en toevoegen** en selecteer vervolgens het zip-bestand dat u eerder hebt gedownload.
6. Selecteer **Sluiten**.
7. Nadat de gegevensentiteiten zijn geüpload, selecteert u **Importeren** in het actievenster.
8. Ga naar **Belasting** > **Query's en rapporten en rapporten** > **Elektronische berichten** > **Elektronische berichten** en valideer de verwerking van elektronische berichten die u hebt geïmporteerd.

### <a name="configure-electronic-messages"></a>Elektronische berichten configureren

1. Ga naar **Belasting** > **Instellingen** > **Elektronische berichten** > **Acties voor invullen van record**.
2. Selecteer de regel voor **DE Records voor btw-retouren invullen** en selecteer vervolgens **Query bewerken**.
3. Gebruik het filter om de vereffeningsperioden op te geven die u in het rapport wilt opnemen.
4. Als u btw-transacties van andere vereffeningsperioden in een andere aangifte moet rapporteren, maakt u een nieuwe actie **Records invullen** en selecteert u de juiste vereffeningsperioden.

## <a name="preview-the-vat-declaration-in-excel"></a>Voorbeeld van de btw-aangifte in Excel

### <a name="preview-the-vat-declaration-in-excel-from-the-report-sales-tax-for-settlement-period-periodic-task"></a>Een voorbeeld weergeven van de btw-aangifte in Excel vanuit de periodieke taak Btw rapporteren voor vereffeningsperiode

1. Ga naar **Belasting** > **Periodieke taken** > **Aangiftens** > **Btw** > **Btw rapporteren voor vereffeningsperiode**.
2. Selecteer een waarde in het veld **Vereffeningsperiode**.
3. Selecteer in het veld **Versie van btw-betaling** een van de volgende waarden:

    - **Oorspronkelijk**: genereer een rapport voor de btw-transacties van de oorspronkelijke btw-betaling of voordat de btw-betaling wordt gegenereerd.
    - **Correcties**: genereer een rapport voor de btw-transacties van alle volgende btw-betalingen voor de periode.
    - **Totaal overzicht**: genereer een rapport voor alle btw-transacties voor de periode, met inbegrip van het origineel en alle correcties.

4. Selecteer in het veld **Begindatum** de begindatum van de rapportageperiode.
5. Selecteer **OK** en bekijk het Excel-rapport.

### <a name="settle-and-post-sales-tax"></a><a name="settle-and-post-sales-tax"></a>Btw vereffenen en boeken

1. Ga naar **Belasting** > **Periodieke taken** > **Aangiften** > **Btw** > **Btw vereffenen en boeken**.
2. Selecteer een waarde in het veld **Vereffeningsperiode**.
3. Selecteer in het veld **Versie van btw-betaling** een van de volgende waarden:

    - **Oorspronkelijk**: genereer de oorspronkelijke btw-betaling voor de vereffeningsperiode.
    - **Laatste correcties**: genereer een correctie-btw-betaling nadat de oorspronkelijke btw-betaling is gemaakt voor de vereffeningsperiode.

4. Selecteer in het veld **Begindatum** de begindatum van de rapportageperiode.
5. Selecteer **OK**.

### <a name="preview-the-vat-declaration-in-excel-from-a-sales-tax-payment"></a>Een voorbeeld van de btw-aangifte in Excel weergeven vanuit een btw-betaling

1. Ga naar **Belasting** > **Query's en rapporten** > **Vragen over btw** > **Btw-betalingen** en selecteer een btw-betalingsregel.
2. Selecteer **Rapport afdrukken** en selecteer **OK**.
3. Controleer het Excel-bestand dat is gegenereerd voor de geselecteerde btw-betalingsregel.

    > [!NOTE]
    > Het rapport wordt alleen gegenereerd voor de geselecteerde regel van de btw-betaling. Als u bijvoorbeeld een correctieaangifte wilt genereren die alle correcties voor de periode bevat, of een vervangende aangifte met de oorspronkelijke gegevens en alle correcties, gebruikt u de periodieke taak **Btw rapporteren voor de vereffeningsperiode**.

## <a name="generate-a-vat-declaration-from-electronic-messages"></a>Een btw-aangifte genereren vanuit elektronische berichten

Wanneer u elektronische berichten gebruikt om het rapport te genereren, kunt u belastinggegevens verzamelen van meerdere rechtspersonen. Zie de sectie [Btw-aangifte uitvoeren voor meerdere rechtspersonen](#run-a-vat-declaration-for-multiple-legal-entities) verderop in dit artikel voor meer informatie.

De volgende procedure is van toepassing op het voorbeeld van de verwerking van elektronische berichten die u hebt geïmporteerd uit de bibliotheek met gedeelde activa van LCS.

1. Ga naar **Belasting** > **Query's en rapporten** > **Elektronische berichten** > **Elektronische berichten**.
2. Selecteer **DE Btw-aangifte** in het linkerdeelvenster.
3. Selecteer op het sneltabblad **Berichten** die optie **Nieuw** en selecteer vervolgens, in het dialoogvenster **Verwerking uitvoeren** de optie **OK**.
4. Selecteer de berichtregel die is gemaakt, voer een beschrijving in en geef vervolgens de begin- en einddatum voor de aangifte op.

    > [!NOTE]
    > Stappen 5 tot en met 7 zijn optioneel.

5. Optioneel: selecteer op het sneltabblad **Berichten** de optie **Gegevens verzamelen** en selecteer vervolgens **OK**. De btw-betalingen die eerder zijn gegenereerd, worden toegevoegd aan het bericht. Zie de sectie [Btw vereffenen en boeken](#settle-and-post-sales-tax) eerder in dit artikel voor meer informatie. Als u deze stap overslaat, kunt u nog steeds een btw-aangifte genereren via het veld **Versie btw-aangifte** in het dialoogvenster **Aangifte**.
6. Optioneel: controleer op het sneltabblad **Berichtitems** de btw-betalingen die zijn overgeboekt voor verwerking. Standaard worden alle btw-betalingen opgenomen van de geselecteerde periode die niet in een ander bericht van dezelfde verwerking zijn opgenomen.
7. Optioneel: selecteer **Oorspronkelijk document** om de btw-betalingen te controleren of selecteer **Verwijderen** om de verwerking van btw-betalingen uit te sluiten. Als u deze stap overslaat, kunt u nog steeds een btw-aangifte genereren via het veld **Versie btw-aangifte** in het dialoogvenster **Aangifte**.
8. Selecteer op het sneltabblad **Berichten** de optie **Status bijwerken**. Selecteer in het dialoogvenster **Status bijwerken** de optie **Gereed om te genereren** en selecteer vervolgens **OK**. Controleer of de berichtstatus is gewijzigd in **Gereed om te genereren**.
9. Selecteer **Rapport genereren**. Als u een voorbeeld wilt weergeven van de btw-aangiftebedragen, selecteert u in het dialoogvenster **Verwerking uitvoeren** de optie **Voorbeeldrapport** en selecteert u vervolgens **OK**.
10. Stel in het dialoogvenster **Parameters van elektronische rapportage** de volgende velden in en selecteer vervolgens **OK**.

    | **Veld**                                   | **Beschrijving**                                                                                                                                                                                                              |
    |---------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | Vereffeningsperiode                           | Selecteer de vereffeningsperiode. Als u in stap 5 **Gegevens verzamelen** hebt geselecteerd, kunt u dit veld leeg laten. Het rapport wordt gegenereerd voor de btw-transacties die zijn opgenomen in de verzamelde btw-betalingen. |
    | Versie van btw-aangifte                     | Selecteer een van de volgende waarden:</br>-   **Oorspronkelijk**: genereer een rapport voor de btw-transacties van de oorspronkelijke btw-betaling of voordat de btw-betaling wordt gegenereerd.</br>-   **Correcties**: genereer een rapport voor de btw-transacties van alle volgende btw-betalingen voor de periode.</br>-   **Totaal overzicht**: genereer een rapport voor alle btw-transacties voor de periode, met inbegrip van het origineel en alle correcties.|
    | Fiscaal vertegenwoordiger | Selecteer de partij die zo nodig een belastingvertegenwoordiger voor btw-aangifte is. Informatie over de geselecteerde partij wordt geëxporteerd naar het XML-element **DatenLieferant**. |
    | Contactpersoon | Selecteer een persoon in de organisatie die een gegevensleverancier is. Informatie over de geselecteerde persoon wordt geëxporteerd naar het XML-element **DatenLieferant**. |
    | Corrigerende teruggave | Selecteer **Ja** als dit een btw-aangifte ter correctie is. In dit geval heeft XML-element KZ10 de waarde **1**.|
    | Ondersteunende documenten | Selecteer **Ja** als u ook ondersteunende documenten verzendt. In dit geval heeft XML-element KZ22 de waarde **1**.|
    | Het SEPA-mandaat voor automatische afschrijving wordt bij uitzondering ingetrokken| Selecteer **Ja** als het SEPA-mandaat voor automatische afschrijving wordt ingetrokken als uitzondering voor deze voorregistratieperiode. Bijvoorbeeld vanwege tegenrekeningsaanvragen. Elk resterend saldo moet afzonderlijk worden betaald. In dit geval heeft XML-element KZ26 de waarde **1**. |
    | Gewenste tegenrekening van het terugbetalingsbedrag | Selecteer **Ja** als een tegenrekening van het gezochte terugbetalingsbedrag is toegekend of als het terugbetalingsbedrag is toegekend. In dit geval heeft XML-element KZ29 de waarde **1**. |
    | Permanente verlenging voor speciale voorschotbetaling | Voer het inhoudingsbedrag van de vaste speciale voorschotbetaling voor permanente verlenging in. Dit inhoudingsbedrag wordt gewoonlijk alleen ingevuld bij de laatste voorregistratie van de belastingperiode. Het bedrag wordt geëxporteerd in rij 67 (vak 39) en XML-element KZ39 van de btw-aangifte. |

11. Selecteer **Bijlagen** in de rechterbovenhoek van de pagina en selecteer vervolgens **Openen**.
12. Controleer de bedragen in het Excel-document en selecteer vervolgens **Rapport genereren**.
13. Als u een btw-aangifte in XML-indeling wilt genereren, selecteert u in het dialoogvenster **Verwerking uitvoeren** de optie **Rapport genereren** en selecteert u vervolgens **OK**.
14. Stel in het dialoogvenster **Parameters van elektronische rapportage** de velden in zoals beschreven in stap 10.
15. Selecteer **Bijlagen** in de rechterbovenhoek van de pagina, download het bestand en gebruik dit voor indiening bij de belastingdienst.

## <a name="run-a-vat-declaration-for-multiple-legal-entities"></a><a name="run-a-vat-declaration-for-multiple-legal-entities"></a>Een btw-aangifte uitvoeren voor meerdere rechtspersonen

Als u de indelingen wilt gebruiken om de btw-aangifte voor een groep rechtspersonen te rapporteren, moet u eerst toepassingsspecifieke parameters instellen voor de ER-indelingen voor btw-codes van alle vereiste rechtspersonen.

### <a name="set-up-electronic-messages-to-collect-tax-data-from-several-legal-entities"></a>Elektronische berichten instellen om btw-gegevens van verschillende rechtspersonen te verzamelen

Volg deze stappen om elektronische berichten in te stellen die gegevens van meerdere rechtspersonen zullen verzamelen.

1. Ga naar **Werkruimten** > **Functiebeheer**.
2. Zoek en selecteer de functie **Query's voor meerdere bedrijven voor acties voor het invullen van records** en selecteer vervolgens **Nu inschakelen**.
3. Ga naar **Belasting** > **Instellingen** > **Elektronische berichten \> Acties voor invullen van record**.
4. Selecteer op de pagina **Actie voor invullen van record** de regel voor **DE Records voor btw-retouren invullen**.

   In het raster **Instelling van gegevensbronnen** is een nieuw veld **Bedrijf** beschikbaar. Voor bestaande records toont dit veld de identificatie van de huidige rechtspersoon.

5. Voeg in het raster **Instelling voor gegevensbronnen** een regel toe voor elke aanvullende rechtspersoon die in de rapportage moet worden opgenomen. Stel voor elke nieuwe regel de volgende velden in.

    | Veld                  | Description                                                                                                                   |
    |------------------------|-------------------------------------------------------------------------------------------------------------------------------|
    | Name                   | Voer een waarde in om beter te begrijpen waar deze record vandaan komt. Voer bijvoorbeeld **Btw-betaling van dochtermaatschappij 1** in. |
    | Type berichtitem      | Selecteer **Btw-retour**. Dit is de enige waarde die beschikbaar is voor alle records.                                    |
    | Rekeningtype           | Selecteer **Alles**.                                                                                                               |
    | Naam van hoofdtabel      | Geef **TaxReportVoucher** op voor alle records.                                                                             |
    | Veld met documentnummer  | Geef **Voucher** op voor alle records.                                                                                      |
    | Veld met documentdatum    | Geef **TransDate** op voor alle records.                                                                                    |
    | Accountveld van document | Geef **TaxPeriod** op voor alle records.                                                                                    |
    | Bedrijf                | Selecteer de id van de rechtspersoon.                                                                                            |
    | Gebruikersquery             | Dit selectievakje wordt automatisch ingeschakeld wanneer u criteria definieert door **Query bewerken** te selecteren.                                 |

6. Selecteer voor elke nieuwe regel de optie **Query bewerken** en geef een gerelateerde vereffeningsperiode op voor de rechtspersoon die is opgegeven in het veld **Bedrijf** op de regel.

Wanneer de instelling is voltooid, verzamelt de functie **Gegevens verzamelen** op de pagina **Elektronische berichten** btw-betalingen van alle rechtspersonen die u hebt gedefinieerd.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
