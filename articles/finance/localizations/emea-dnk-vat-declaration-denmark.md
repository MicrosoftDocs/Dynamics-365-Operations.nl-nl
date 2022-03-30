---
title: Btw-aangifte (Denemarken)
description: In dit onderwerp wordt beschreven hoe u een voorschot-btw-aangifte voor Denemarken kunt instellen en genereren in de officiële XML-indeling.
author: anasyash
ms.date: 03/10/2022
ms.topic: article
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: anasyash
ms.search.validFrom: ''
ms.openlocfilehash: 4d4a1185fa3c3b059744018b6e4e195de07126c9
ms.sourcegitcommit: 9c19898e1f41495f804c7f07e2636b53a098c4c1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/10/2022
ms.locfileid: "8402980"
---
# <a name="vat-declaration-denmark"></a>Btw-aangifte (Denemarken)

[!include [banner](../includes/banner.md)]

In dit onderwerp wordt beschreven hoe u een voorschot-btw-aangifte voor Denemarken kunt instellen en bekijken in Microsoft Excel.

Als u het rapport automatisch wilt genereren, maakt u eerst voldoende btw-codes om een afzonderlijke btw-boekhouding te behouden voor elk vak in de voorschot-btw-aangifte. In de toepassingsspecifieke parameters van de ER-indeling (elektronische aangifte) voor de voorschot-btw-aangifte koppelt u bovendien btw-codes aan het zoekresultaat van de zoekopdrachten voor de vakken in de btw-aangifte.

Voor Denemarken moet u **Rapportveld zoeken** configureren. Zie de sectie [Toepassingsspecifieke parameters instellen voor btw-aangiftevelden](#set-up-application-specific-parameters) verderop in dit onderwerp voor meer informatie over het instellen van toepassingsspecifieke parameters.

In de volgende tabel ziet u in de kolom 'Opzoekresultaat' het opzoekresultaat dat vooraf is geconfigureerd voor een specifieke btw-aangifterij in de indeling voor de btw-aangifte. Gebruik deze informatie om btw-codes correct aan het opzoekresultaat en vervolgens aan de rij van de btw-aangifte te koppelen.

### <a name="vat-declaration-overview"></a>Overzicht van btw-aangifte

De voorschot-btw-aangifte in Denemarken bevat de volgende informatie.

**VAT te betalen**

| Description                                                  | Belastingbasis/belastingbedrag | Zoekresultaat/totaal                                                                                                                                                                                                                                                                                                                          |
|--------------------------------------------------------------|---------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Te betalen btw                                                   | Btw-bedrag          | **OutputVAT**</br> **DomesticVATUseTax** (ook in het vak Te vorderen btw gemeld)                                                                                                                                                                                                                                                                       |
| Btw op goederen enzovoort. ingekocht in het buitenland                           | Btw-bedrag          | **PurchaseGoodsAbroad**</br>**PurchaseGoodsAbroadUseTax** (ook in het vak Te vorderen btw gemeld)</br>**PurchaseGoodsEU** (de belastingbasis wordt vermeld in vak A - verwerving van goederen.)</br>**PurchaseGoodsEUUseTax** (het belastingbedrag wordt ook in het vak Te vorderen btw gemeld. De belastingbasis wordt vermeld in vak A - verwerving van goederen.)                   |
| Btw op in het buitenland ingekochte diensten waarop een omgekeerde omslag van toepassing is | Btw-bedrag          | **PurchaseServicesAbroad**</br> **PurchaseServicesAbroadUseTax** (ook in het vak Te vorderen btw gemeld)</br>**PurchaseServicesEU** (de belastingbasis wordt vermeld in vak A - verwerving van goederen.)</br>**PurchaseServicesEUUseTax** (het belastingbedrag wordt ook in het vak Te vorderen btw gemeld. De belastingbasis wordt vermeld in vak A - verwerving van diensten.) |
| Totaal te betalen                                                | Btw-bedrag          | Totaal van de vorige drie vakken                                                                                                                                                                                                                                                                                                            |

**Inhoudingen**

| Description                                                                               | Belastingbasis/belastingbedrag | Zoekresultaat/totaal                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|-------------------------------------------------------------------------------------------|---------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Te vorderen btw                                                                                 | Btw-bedrag          | **InputVAT**</br> **DomesticVATUseTax** (ook in het vak Te betalen btw gemeld)</br>**PurchaseGoodsAbroadUseTax** (ook in het vak Btw op goederen enzovoort, ingekocht in het buitenland)</br>**PurchaseServicesAbroadUseTax** (ook gerapporteerd in het vak Btw op ingekochte diensten met omgekeerde toeslag)</br>**PurchaseGoodsEUUseTax** (ook in het vak Btw op goederen enzovoort, ingekocht in het buitenland)</br> **PurchaseServicesEUUseTax** (ook gerapporteerd in het vak Btw op ingekochte diensten met omgekeerde toeslag) |
| Heffingen voor olie en flessengas                                                                  | Btw-bedrag          | **OilGasDuty**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| Heffing voor aardgas en stadsgas                                                             | Btw-bedrag          | **NaturalTownGasDuty**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| Koolstofheffing                                                                               | Btw-bedrag          | **CarbonDuty**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| CO2Duty                                                                                   | Btw-bedrag          | **CO2Duty**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| Waterheffing                                                                              | Btw-bedrag          | **WaterCharge**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| Totaal inhoudingen                                                                          | Btw-bedrag          | Totaal van de vorige zes vakken                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| Totaalbedrag van heffingen (positief bedrag = betalen, negatief bedrag = restitutie ontvangen) | Btw-bedrag          | Totaal te betalen - totaal inhoudingen                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |

**Aanvullende informatie**

| Description                                                                                                                                                                                                                                | Belastingbasis/belastingbedrag | Zoekresultaat/totaal                             |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------|-------------------------------------------------|
| Vak A - verwerving van goederen. De waarde zonder btw voor intracommunautaire verwerving van goederen.                                                                                                                                                   | Btw-basis            | **PurchaseGoodsEU PurchaseGoodsEUUseTax**       |
| Vak A - verwerving van diensten. De waarde zonder btw voor intracommunautaire verwerving van diensten.                                                                                                                                             | Btw-basis            | **PurchaseServicesEU PurchaseServicesEUUseTax** |
| Vak B - levering van goederen - te rapporteren aan EU-verkoop zonder btw/DK VIES. De waarde zonder btw voor intracommunautaire levering van goederen                                                                                                           | Btw-basis            | **SalesGoodsEU**                                |
| Vak B - leveringen - niet te rapporteren aan EU-verkoop zonder btw/DK VIES. De waarde zonder btw van bepaalde intracommunautaire leveringen, bijvoorbeeld installatie, assemblage, verkoop op afstand en nieuwe transportmiddelen voor niet-belastbare personen. | Btw-basis            | **SalesInstallationAssemblyEtcEU**              |
| Box B - levering van diensten. De waarde zonder btw van intracommunautaire levering van diensten waarvoor de koper btw-plichtig via een omgekeerde toeslag - moet ook bij EU-verkoop zonder btw/DK VIES worden gerapporteerd.                          | Btw-basis            | **SalesServicesEU**                             |
| Vak C - overige leveringen. Waarde van de levering van andere goederen en diensten die zonder btw zijn geleverd binnen Denemarken aan andere EU-lidstaten en aan derde landen/regio's of derde gebieden.                                     | Btw-basis            | **OtherSuppliesWithoutVAT**                     |

#### <a name="purchase-reverse-charge-vat"></a>Omgekeerde toeslag van te vorderen btw

Als u btw-codes configureert om inkomende omgekeerde toeslagen te boeken via gebruiksbelasting, koppelt u uw btw-codes aan het opzoekresultaat van **Rapportveld zoeken** dat "UseTax" in de naam heeft.

U kunt ook twee afzonderlijke btw-codes configureren: één voor te betalen btw en één voor btw-aftrek. Koppel vervolgens elke code aan de bijbehorende opzoekresultaten voor **Rapportveld zoeken**.

Zo configureert u bijvoorbeeld voor belastbare intracommunautaire verwervingen met een btw-code **UT_S_EU** met gebruiksbelasting en koppelt u deze aan het opzoekresultaat **PurchaseGoodsEUUseTax** van **Rapportveld zoeken**. In dit geval worden belastingbedragen die gebruikmaken van btw-code **UT_S_EU** weergegeven in de vakken Btw op goederen, enzovoort In het buitenland gekocht en Te vorderen btw. De belastingbasis wordt weergegeven in vak A - verwerving van goederen.

U kunt ook twee btw-codes configureren:

- **VAT_S_EU**, met een btw-tariefwaarde van -25 procent
- **InVAT_S_EU**, met een btw-tariefwaarde van 25 procent

Vervolgens koppelt u als volgt de codes aan opzoekresultaten van **Rapportveld zoeken**:

- Koppel **VAT_S_EU** aan het opzoekresultaat **PurchaseGoodsEU**.
- Koppel **InVAT_S_EU** aan het opzoekresultaat **InputVAT**.

In dit geval worden bedragen die gebruikmaken van btw-code **VAT_S_EU** weergegeven in het vak Btw op goederen enzovoort, in het buitenland gekocht en Vak A - verwerving van goederen. Bedragen die gebruikmaken van de btw-code **InVAT_S_EU** worden weergegeven in het vak Te vorderen btw.

Zie [Terugboekingen](emea-reverse-charge.md) voor meer informatie over het configureren van omgekeerde toeslagen.

## <a name="configure-system-parameters"></a>Systeemparameters configureren

Voor het genereren van een btw-aangifte moet u het btw-nummer configureren.

1. Ga naar **Organisatiebeheer** > **Organisaties** > **Rechtspersonen**.
2. Selecteer de rechtspersoon en selecteer **Registratie-id's**.
3. Selecteer of maak het adres in Denemarken en selecteer vervolgens op het sneltabblad **Registratie-id's** de optie **Toevoegen**.
4. Selecteer in het veld **Registratietype** het registratietype dat is toegewezen aan Denemarken en dat gebruikmaakt van de registratiecategorie **Btw-id**.
5. Voer het btw-nummer in het veld **Registratienummer** in.
6. Voer op het tabblad **Algemeen** in het veld **Geldig vanaf** de datum in waarop het nummer van kracht wordt.

Zie [Registratie-id's](emea-registration-ids.md) voor meer informatie over het instellen van registratiecategorieën en registratietypen.

## <a name="set-up-a-vat-declaration-preview-for-denmark"></a>Een voorbeeld van een btw-aangifte instellen voor Denemarken

### <a name="import-er-configurations"></a>ER-configuraties importeren

Open de werkruimte **Elektronische rapportage** en importeer de ER-indeling **Btw-aangifte Excel (DK)**.

Meer informatie is te vinden in [ER-configuraties downloaden uit de Algemene opslagplaats van de configuratieservice](../../fin-ops-core/dev-itpro/analytics/er-download-configurations-global-repo.md).

### <a name="set-up-application-specific-parameters-for-vat-declaration-fields"></a><a name="set-up-application-specific-parameters"></a>Toepassingsspecifieke parameters instellen voor btw-aangiftevelden

> [!NOTE]
> U kunt het beste de functie **Toepassingsspecifieke parameters van vorige versies van ER-indelingen** inschakelen in de werkruimte **Functiebeheer**. Wanneer deze functie is ingeschakeld, worden parameters die zijn geconfigureerd voor de eerdere versie van een ER-indeling automatisch van toepassing op de latere versie van dezelfde indeling. Als deze functie niet is ingeschakeld, moet u toepassingsspecifieke parameters expliciet voor elke indelingsversie configureren. De functie **Toepassingsspecifieke parameters van vorige versies van ER-indelingen** is beschikbaar in de werkruimte **Functiebeheer** vanaf Finance-versie 10.0.23. Zie [De parameters voor een ER-indeling per rechtspersoon instellen](../../fin-ops-core/dev-itpro/analytics/er-app-specific-parameters-set-up.md) voor meer informatie over het instellen van de parameters van een ER-indeling voor elke rechtspersoon.

Als u automatisch een btw-aangifte wilt genereren, koppelt u btw-codes aan de toepassing en zoekresultaten in de ER-configuratie.

Volg deze stappen om te definiëren door welke btw-codes welke vakken worden gegenereerd in de btw-aangifte.

1. Ga naar **Werkruimten** > **Elektronische rapportage** en selecteer **Rapportageconfiguraties**.
2. Selecteer de configuratie **Btw-aangifte Excel (DK)** en selecteer vervolgens **Configuraties \> Toepassingsspecifieke parameters instellen**.
3. Selecteer op de pagina **Toepassingsspecifieke parameters** op het sneltabblad **Zoekopdrachten** de optie **Rapportveld zoeken**.
4. Stel op het sneltabblad **Voorwaarden** de volgende velden in om de btw-codes en rapportvelden te koppelen.

    | Veld                  | Description                                                                                                                                                                                                                                                                                                          |
    |------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | Zoekresultaat          | Selecteer de waarde van het rapportveld. Zie de sectie eerder in dit onderwerp [Overzicht van btw-aangifte](#vat-declaration-overview) voor meer informatie over de waarden en hun toewijzing aan rijen voor btw-aangifte.                                                                                               |
    | Belastingcode               | Selecteer de btw-code die u aan het rapportveld wilt koppelen. Geboekte btw-transacties die de geselecteerde btw-code gebruiken, worden in het desbetreffende aangiftevak verzameld. Het is raadzaam om btw-codes zo te scheiden, dat één btw-code bedragen in slechts één aangiftevak genereert. |
    | Transactieclassificatie | Als u voldoende btw-codes hebt gemaakt om het aangiftevak te bepalen, selecteert u **\*Niet leeg\***. Als u niet voldoende btw-codes hebt gegenereerd zodat één btw-code bedragen in slechts één aangiftevak genereert, kunt u een transactieclassificatie instellen. De volgende transactieclassificaties zijn beschikbaar:</br>-   **Aankoop**</br>-   **PurchaseExempt** (inkoop met belastingvrijstelling)</br>-   **PurchaseReverseCharge** (terug te ontvangen btw van een omgekeerde toeslag op een inkoopfactuur)</br>-   **Sales**</br>-   **SalesExempt** (verkoop met btw-vrijstelling)</br>-   **SalesReverseCharge** (te betalen btw van een omgekeerde toeslag op een inkoopfactuur of een omgekeerde toeslag op een verkoopfactuur)</br>-   **Gebruiksbelasting**. </br>Voor elke transactieclassificatie is er ook een classificatie voor de creditnota beschikbaar. Een van deze classificaties is bijvoorbeeld **PurchaseCreditNote** (creditnota voor inkoop).</br>Zorg ervoor dat u twee regels maakt voor elke btw-code: een met de waarde van de transactieclassificatie en een met de transactieclassificatie voor de waarde van de creditnota. |


    > [!NOTE]
    > Koppel alle btw-codes aan opzoekresultaten. Als btw-codes geen waarden op de btw-aangifte moeten genereren, koppelt u deze aan het opzoekresultaat **Overige**.

    ![Pagina Toepassingsspecifieke parameters.](media/7db74920fad66a0db7fad60758698cc0.png)


5. Wijzig in het veld **Status** de waarde in **Voltooid**.

### <a name="set-up-the-vat-reporting-format-for-preview-amounts-in-excel"></a>De notatie voor btw-aangifte instellen voor voorbeeldbedragen in Excel

1. Zoek en selecteer in de werkruimte **Functiebeheer** de functie **Indelingsrapporten voor btw-aangifte** in de lijst en selecteer **Nu inschakelen**.
2. Ga naar **Grootboek** > **Instellingen** > **Grootboekparameters**.
3. Selecteer op het tabblad **Btw** op het sneltabblad **Btw-opties** in het veld **Toewijzing indeling btw-overzicht** de ER-indeling **Btw-aangifte Excel (DK)**.

   Deze indeling wordt afgedrukt wanneer u het rapport **Btw rapporteren voor vereffeningsperiode** uitvoert. Deze wordt ook afgedrukt wanneer u **Afdrukken** selecteert op de pagina **Btw-betalingen**.

4. Selecteer op de pagina **Belastingdienst** de belastingdienst en selecteer vervolgens in het veld **Rapportindeling** de optie **Standaard**.

Als u de btw-aangifte configureert in een rechtspersoon met meerdere [btw-registraties](emea-reporting-for-multiple-vat-registrations.md), volgt u deze stappen.

1. Ga naar **Grootboek** \> **Instellen** \> **Grootboekparameters**.
2. Selecteer op het tabblad **Btw-aangifte** op het sneltabblad **Elektronische aangifte voor landen/regio's** op de regel voor **DNK** de ER-indeling **Btw-aangifte Excel (DK)**.

## <a name="set-up-electronic-messages"></a>Elektronische berichten instellen

### <a name="download-and-import-the-data-package-that-has-example-settings-for-electronic-messages"></a>Het gegevenspakket met voorbeeldinstellingen voor elektronische berichten downloaden en importeren

Het gegevenspakket bevat elektronische berichtinstellingen die worden gebruikt om de btw-aangifte te bekijken in Excel. U kunt deze instellingen uitbreiden of uw eigen instellingen maken. Zie [Elektronische berichten](../general-ledger/electronic-messaging.md) voor meer informatie over het werken met elektronische berichten en het maken van uw eigen instellingen.

1. Selecteer in [Microsoft Dynamics Lifecycle Services (LCS)](https://lcs.dynamics.com/v2) in de Bibliotheek voor gedeelde activa de optie **Gegevenspakket** als activatype en download vervolgens **DK pakket voor btw-aangifte**. De naam van het gedownloade bestand is **DK VAT declaration package.zip**.
2. Selecteer in Finance, in het werkgebied **Gegevensbeheer**, de optie **Importeren**.
3. Voer op het sneltabblad **Importeren** in het veld **Groepsnaam** een naam in voor de taak.
4. Selecteer op het sneltabblad **Geselecteerde entiteiten** de optie **Bestand toevoegen**.
5. Controleer in het dialoogvenster **Bestand toevoegen** of het veld **Brongegevensindeling** is ingesteld op **Pakket**, selecteer **Uploaden en toevoegen** en selecteer vervolgens het zip-bestand dat u eerder hebt gedownload.
6. Selecteer **Sluiten**.
7. Nadat de gegevensentiteiten zijn geüpload, selecteert u **Importeren** in het actievenster.
8. Ga naar **Belasting** > **Query's en rapporten en rapporten** > **Elektronische berichten** > **Elektronische berichten** en valideer de verwerking van elektronische berichten die u hebt geïmporteerd (**DK Btw-aangifte**).

### <a name="configure-electronic-messages"></a>Elektronische berichten configureren

1. Ga naar **Belasting** > **Instellingen** > **Elektronische berichten** > **Acties voor invullen van record**.
2. Selecteer de regel voor **DK Records voor btw-retouren invullen** en selecteer vervolgens **Query bewerken**.
3. Gebruik het filter om de vereffeningsperioden op te geven die u in het rapport wilt opnemen.
4. Als u btw-transacties van andere vereffeningsperioden in een andere aangifte moet rapporteren, maakt u een nieuwe actie **Records invullen** en selecteert u de juiste vereffeningsperioden.

## <a name="preview-the-vat-declaration-in-excel"></a>Voorbeeld van de btw-aangifte in Excel

### <a name="preview-the-vat-declaration-in-excel-from-the-report-sales-tax-for-settlement-period-periodic-task"></a><a name="preview-vat-excel"></a>Een voorbeeld weergeven van de btw-aangifte in Excel vanuit de periodieke taak Btw rapporteren voor vereffeningsperiode

1. Ga naar **Belasting** > **Periodieke taken** > **Aangiftens** > **Btw** > **Btw rapporteren voor vereffeningsperiode**.
2. Selecteer een waarde in het veld **Vereffeningsperiode**.
3. Selecteer in het veld **Versie van btw-betaling** een van de volgende waarden:

    - **Oorspronkelijk**: genereer een rapport voor de btw-transacties van de oorspronkelijke btw-betaling of voordat de btw-betaling wordt gegenereerd.
    - **Correcties**: genereer een rapport voor de btw-transacties van alle volgende btw-betalingen voor de periode.
    - **Totaal overzicht**: genereer een rapport voor alle btw-transacties voor de periode, met inbegrip van het origineel en alle correcties.

4. Selecteer in het veld **Begindatum** de begindatum van de rapportageperiode.
5. Selecteer **OK** en bekijk het Excel-rapport.

### <a name="settle-and-post-sales-tax"></a>Btw vereffenen en boeken

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

Wanneer u elektronische berichten gebruikt om het rapport te genereren, kunt u belastinggegevens verzamelen van meerdere rechtspersonen. Zie de sectie [Btw-aangifte uitvoeren voor meerdere rechtspersonen](#run-vat-declaration) verderop in dit onderwerp voor meer informatie.

De volgende procedure is van toepassing op het voorbeeld van de verwerking van elektronische berichten die u eerder hebt geïmporteerd uit de bibliotheek met gedeelde activa van LCS.

1. Ga naar **Belasting \> Query's en rapporten \> Elektronische berichten \> Elektronische berichten**.
2. Selecteer **DK Btw-aangifte** in het linkerdeelvenster.
3. Selecteer op het sneltabblad **Berichten** die optie **Nieuw** en selecteer vervolgens, in het dialoogvenster **Verwerking uitvoeren** de optie **OK**.
4. Selecteer de berichtregel die is gemaakt, voer een beschrijving in en geef vervolgens de begin- en einddatum voor de aangifte op.

   > [!NOTE]
   > Stappen 5 tot en met 7 zijn optioneel.

5. Optioneel: selecteer op het sneltabblad **Berichten** de optie **Gegevens verzamelen** en selecteer vervolgens **OK**. De btw-betalingen die eerder zijn gegenereerd, worden toegevoegd aan het bericht. Zie de sectie [Btw vereffenen en boeken](#settle-and-post-sales-tax) eerder in dit onderwerp voor meer informatie. Als u deze stap overslaat, kunt u nog steeds een btw-aangifte genereren via het veld **Versie btw-aangifte** in het dialoogvenster **Aangifte**.
6. Optioneel: controleer op het sneltabblad **Berichtitems** de btw-betalingen die zijn overgeboekt voor verwerking. Standaard worden alle btw-betalingen opgenomen van de geselecteerde periode die niet in een ander bericht van dezelfde verwerking zijn opgenomen.
7. Optioneel: selecteer **Oorspronkelijk document** om de btw-betalingen te controleren of selecteer **Verwijderen** om de verwerking van btw-betalingen uit te sluiten. Als u deze stap overslaat, kunt u nog steeds een btw-aangifte genereren via het veld **Versie btw-aangifte** in het dialoogvenster **Aangifte**.
8. Selecteer op het sneltabblad **Berichten** de optie **Status bijwerken**. Selecteer in het dialoogvenster **Status bijwerken** de optie **Gereed om te genereren** en selecteer vervolgens **OK**. Controleer of de berichtstatus is gewijzigd in **Gereed om te genereren**.
9. Selecteer **Rapport genereren**. Als u een voorbeeld wilt weergeven van de btw-aangiftebedragen, selecteert u in het dialoogvenster **Verwerking uitvoeren** de optie **Voorbeeldrapport** en selecteert u vervolgens **OK**.
10. Stel in het dialoogvenster **Parameters elektronische rapportage** de velden in zoals beschreven in [Een voorbeeld weergeven van de btw-aangifte in Excel vanuit de periodieke taak Btw rapporteren voor vereffeningsperiode](#preview-vat-excel) eerder in dit onderwerp en selecteer vervolgens **OK**.
11. Selecteer de knop **Bijlagen** (paperclipsymbool) in de rechterbovenhoek van de pagina en vervolgens **Openen** om het bestand te openen. Controleer de bedragen in het Excel-document.

## <a name="run-a-vat-declaration-for-multiple-legal-entities"></a><a name="run-vat-declaration"></a>Een btw-aangifte uitvoeren voor meerdere rechtspersonen

Als u de indelingen wilt gebruiken om de btw-aangifte voor een groep rechtspersonen te rapporteren, moet u eerst toepassingsspecifieke parameters instellen voor de ER-indelingen voor btw-codes van alle vereiste rechtspersonen.

### <a name="set-up-electronic-messages-to-collect-tax-data-from-several-legal-entities"></a>Elektronische berichten instellen om btw-gegevens van verschillende rechtspersonen te verzamelen

Volg deze stappen om elektronische berichten in te stellen om gegevens van meerdere rechtspersonen te verzamelen.

1. Ga naar **Werkruimten** > **Functiebeheer**.
2. Zoek en selecteer de functie **Query's voor meerdere bedrijven voor acties voor het invullen van records** en selecteer vervolgens **Nu inschakelen**.
3. Ga naar **Belasting** > **Instellingen** > **Elektronische berichten** > **Acties voor invullen van record**.
4. Selecteer op de pagina **Actie voor invullen van record** de regel voor **DK Records voor btw-retouren invullen**.

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
