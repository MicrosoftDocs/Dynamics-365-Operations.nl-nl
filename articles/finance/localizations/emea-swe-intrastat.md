---
title: Zweedse Intrastat
description: Dit onderwerp bevat informatie over Intrastat-aangifte in Zweden.
author: anasyash
ms.date: 8/24/2021
ms.topic: article
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: anasyash
ms.search.validFrom: ''
ms.openlocfilehash: 1031b93950e44fe3b1b6254bf1503b4c09d6fd10
ms.sourcegitcommit: 631d2cea52590af15f208e9af584446e85540fcf
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/07/2022
ms.locfileid: "8727393"
---
# <a name="swedish-intrastat"></a>Zweedse Intrastat

[!include[banner](../includes/banner.md)]

De pagina **Intrastat** wordt gebruikt om informatie te genereren en rapporteren over handel tussen landen van de EU. De Zweedse Intrastat-aangifte bevat informatie over de handel in goederen voor rapportage.

De volgende velden zijn opgenomen in de Zweedse Intrastat-aangifte:

   - ISO-code partnerland
   - Transactiecode
   - Basisproductcode
   - Aanvullende eenheid
   - Gewicht
   - Factuurbedrag

## <a name="set-up-intrastat"></a>Intrastat instellen

De laatste versie van de volgende ER-configuraties (Elektronische Rapportage) importeren:

   - Intrastat-model
   - Intrastat-rapport
   - Intrastat (SE)

Meer informatie is te vinden in [ER-configuraties downloaden uit de Algemene opslagplaats van de configuratieservice](../../fin-ops-core/dev-itpro/analytics/er-download-configurations-global-repo.md).

## <a name="set-up-foreign-trade-parameters"></a>Parameters voor buitenlandse handel instellen

1. Ga in Microsoft Microsoft Dynamics 365 Finance naar **Belasting** > **Instellingen** > **Parameters buitenlandse handel**.
2. Selecteer in het tabblad **Intrastat** in het sneltabblad **Elektronische rapportage** in het veld **Toewijzing bestandsindeling** de waarde **Intrastat (SE)**.
3. Selecteer in het veld **Rapportindelingstoewijzing** de optie **Intrastat-rapport**.
4. Selecteer op het sneltabblad **Hiërarchie van basisproductcodes** in het veld **Categoriehiërarchie** de optie **Intrastat**.
5. Selecteer in het veld **Transactiecode** de transactiecode voor eigenschapsoverdrachten. Deze code wordt gebruikt voor transacties die tot een werkelijke of geplande eigendomsoverdracht tegen vergoeding (financieel of anders) leiden. De code kan ook worden gebruikt voor correcties. Bedrijven in Zweden gebruiken transactiecodes die uit één cijfer bestaan.
6. Selecteer in het veld **Creditnota** de transactiecode voor de retourzending van goederen.
7. Geef in het tabblad **Eigenschappen land/regio** in het veld **Land/regio** een overzicht weer van alle landen of regio's waarmee uw organisatie zaken doet. Selecteer voor elk land of elke regio dat deel uitmaakt van de EU, in het veld **Land-/regiotype** de waarde **EU**, zodat het land in het Intrastat-rapport wordt weergegeven.

## <a name="set-up-the-product-parameters-for-the-intrastat-declaration"></a>De productparameters voor de Intrastat-aangifte instellen

1. Ga naar **Productgegevensbeheer** > **Producten** > **Vrijgegeven producten**.
2. Selecteer een product in het raster.
3. Selecteer in het sneltabblad **Buitenlandse handel** in het gedeelte **Intrastat** in het veld **Basisproduct** de juiste NGP-code.
4. Voer in het sneltabblad **Voorraad beheren** in het veld **Nettogewicht** het gewicht van het product in kilogram in.
5. Ga naar **Belasting** > **Instellingen** > **Buitenlandse handel** > **Compressie van Intrastat** en selecteer de velden die moeten worden vergeleken tijdens het samenvatten van de Intrastat-informatie. Selecteer voor de Zweedse Intrastat de volgende velden:

    - Basisproduct
    - Transactiecode
    - Richting
    - Land/regio
    - Correctie
    - Factuur

## <a name="intrastat-transfer"></a>Intrastat-overboeking

In het actievenster op de pagina **Intrastat** kunt u **Overboeking** selecteren om de informatie over intracommunautaire handel automatisch over te brengen van uw verkooporders, vrije-tekstfacturen, inkooporders, leveranciersfacturen, leveranciersproductontvangstbonnen, projectfacturen en overboekingsorders. Alleen documenten met een EU-land als land of regio van bestemming (voor verzendingen) of consignatie (voor ontvangsten) worden overgeboekt.

U kunt ook handmatig transacties invoeren door **Nieuw** te selecteren in het actievenster.

### <a name="generate-an-intrastat-report"></a>Een Intrastat-rapport genereren

1. Ga naar **Belasting** > **Aangiften** > **Buitenlandse handel** > **Intrastat**.
2. Selecteer in het actievenster **Uitvoer** > **Rapport**.
3. Stel in het dialoogvenster **Intrastat-rapport** de volgende velden in.

    | Veld            | Beschrijving                                                                                                                         |
    |------------------|-------------------------------------------------------------------------------------------------------------------------------------|
    | Begindatum        | Selecteer de begindatum voor het rapport.                                                                                               |
    | Einddatum          | Selecteer de einddatum voor het rapport.                                                                                                 |
    | Bestand genereren    | Stel deze optie in op **Ja** om een .txt-bestand voor uw Intrastat-rapport te genereren.                                                       |
    | Bestandsnaam        | De naam van het .txt-bestand invoeren.                                                                                                    |
    | Rapport genereren  | Stel deze optie in op **Ja** om een .xlsx-bestand voor uw Intrastat-rapport te genereren.                                                     |
    | Rapportbestandsnaam | De naam van het .xlsx-bestand invoeren.                                                                                                   |
    | Richting        | Selecteer **Ontvangsten** voor een rapport over intracommunautaire ontvangsten. Selecteer **Verzendingen** voor een rapport over intracommunautaire verzendingen. |

4. Selecteer **OK** en controleer de gegenereerde rapporten.

## <a name="example"></a>Voorbeeld

Dit voorbeeld laat zien hoe u ontvangsten en verzendingen voor Intrastat kunt boeken. Er wordt gebruikgemaakt van de rechtspersoon **DEMF**.

### <a name="preliminary-setup"></a>Voorlopige instellingen

1. Ga naar **Organisatiebeheer** > **Organisaties** > **Rechtspersonen** en selecteer de rechtspersoon van **DEMF**.
2. Selecteer **Bewerken** in het sneltabblad **Adressen** en selecteer vervolgens **SWE (Zweden)** in het veld **Land/regio.**.
3. Importeer de laatste versie van de volgende ER-configuraties (Elektronische Rapportage):

    - Intrastat-model
    - Intrastat-rapport
    - Intrastat (SE)

### <a name="create-transaction-codes"></a>Transactiecodes aanmaken

1. Ga naar **Belasting** > **Instellingen** > **Buitenlandse handel** > **Transactiecodes**.
2. Selecteer **Nieuw** in het actievenster.
3. Voer in het veld **Transactiecode** de waarde **1** in.
4. Voer in het veld **Naam** de waarde **Normale transacties** in.
5. Selecteer **Opslaan** in het actievenster.

### <a name="set-up-foreign-trade-parameters"></a>Parameters voor buitenlandse handel instellen

1. Ga naar **Belasting** > **Instellingen** > **Buitenlandse handel** > **Parameters buitenlandse handel**.
2. Selecteer in het tabblad **Intrastat** in het sneltabblad **Algemeen** in het veld **Transactiecode** de waarde **1**.
3. Selecteer in het sneltabblad **Elektronische rapportage** in het veld **Toewijzing bestandsindeling** de waarde **Intrastat (SE)**.
4. Selecteer in het veld **Toewijzing rapportindeling** de waarde **Intrastat-rapport**.
5. Zorg ervoor dat in het sneltabblad **Hiërarchie basisproductcodes** in het veld **Categoriehiërarchie** de waarde **Intrastat** geselecteerd is.
6. Selecteer in het tabblad **Land-/regio eigenschappen** de waarde **Nieuw**.
7. Selecteer in het veld **Land/regio partij** de waarde **SWE**.
8. Selecteer in het veld **Land-/regiotype** de waarde **Binnenland**.
9. Selecteer in het veld **Land/-regio partij** de optie **DEU** en selecteer vervolgens in het veld **Land-/regiotype** de optie **EU**.

### <a name="set-up-product-information"></a>Productgegevens instellen

1. Ga naar **Productgegevensbeheer** > **Producten** > **Vrijgegeven producten**.
2. Selecteer **D0001** in het raster.
3. Selecteer in het sneltabblad **Buitenlandse handel** in het gedeelte **Intrastat** in het veld **Basisproduct** de waarde **100 200 30**.
4. Voer in het sneltabblad **Voorraad beheren** in het gedeelte **Gewichtmetingen** in het veld **Nettogewicht** de waarde **5** in.
5. Selecteer **Opslaan** in het actievenster.

### <a name="change-the-site-address"></a>Het locatieadres wijzigen

1. Ga naar **Magazijnbeheer** > **Instellingen** > **Magazijn** > **Vestigingen**.
2. Selecteer **1** in het raster.
3. Selecteer in het sneltabblad **Adressen** de optie **Bewerken**.
4. Selecteer in het dialoogvenster **Adres bewerken** in het veld **Land/regio** de optie **SWE**.
5. Selecteer **OK**.

### <a name="create-a-sales-order-with-an-eu-customer"></a>Een verkooporder aanmaken met een EU-klant

1. Ga naar **Klanten** > **Orders** > **Alle verkooporders**.
2. Selecteer **Nieuw** in het actievenster.
3. Selecteer in het dialoogvenster **Verkooporder maken** in het sneltabblad **Klant** in het gedeelte **Klant** in het veld **Klantaccount** de waarde **DE-015**.
4. Selecteer in het sneltabblad **Algemeen** in het gedeelte **Opslagdimensies** in het veld **Locatie** de waarde **1**.
5. Selecteer **11** in het veld **Magazijn**.
6. Selecteer **OK**.
7. Selecteer in het tabblad **Regels** in het sneltabblad **Verkooporderregels** in het veld **Artikelnummer** de waarde **D0001**. Voer daarna in het veld **Hoeveelheid** de waarde **10** in.
8. Zorg ervoor dat in het sneltabblad **Regelinformatie** in het tabblad **Buitenlandse handel** de velden **Transactiecode** en **Basisproduct** automatisch worden ingesteld.
9. Selecteer **Opslaan** in het actievenster.
10. Selecteer in het actievenster in het tabblad **Factuur** in het gedeelte **Genereren** de waarde **Factuur**.
11. Selecteer in het dialoogvenster **Factuur boeken** op het sneltabblad **Parameters** in de sectie **Parameters** in het veld **Hoeveelheid** de optie **Alle**.
12. Selecteer **OK** om de factuur te boeken.

### <a name="transfer-the-transaction-to-the-intrastat-journal-and-review-the-result"></a>Boek de transactie over naar het Intrastat-journaal en controleer het resultaat

1. Ga naar **Belasting** > **Aangiften** > **Buitenlandse handel** > **Intrastat**.
2. Selecteer in het actievenster de optie **Overboeken**.
3. Stel in het dialoogvenster **Intrastat (overboeking)** in de sectie **Parameters** de optie **Klantfactuur** in op **Ja**.
4. Selecteer **Filter**.
5. Selecteer in het dialoogvenster **Intrastat-filter** in het tabblad **Bereik** de eerste regel en zorg ervoor dat het veld **Veld** is ingesteld op **Datum**.
6. Selecteer in het veld **Criteria** de huidige datum.
7. Selecteer **OK** om het dialoogvenster **Intrastat-filter** te sluiten.
8. Selecteer **OK** om het dialoogvenster **Intrastat (overboeken)** te sluiten en het resultaat te controleren. De regel staat voor de verkooporder die u eerder hebt aangemaakt.

    ![Intrastat-journaalregels voor verkooporder](media/swe_intrastat_journal_sales_order.png)

9. Selecteer de transactieregel en selecteer vervolgens het tabblad **Algemeen** om meer informatie te bekijken.

    ![Regeldetails van Intrastat-journaal voor verkooporder](media/swe_intrastat_journal_sales_order_line_details.png)

10. Selecteer in het actievenster **Uitvoer** > **Rapport**.
11. Selecteer in het dialoogvenster **Intrastat-rapport** op het sneltabvenster **Parameters** in de sectie **Datum** de maand van de verkooporder die u hebt gemaakt.
12. Stel in het gedeelte **Exportopties** de optie **Bestand genereren** in op **Ja**. Voer in het veld **Bestandsnaam** vervolgens de vereiste naam in.
13. Stel de optie **Rapport genereren** in op **Ja**. Voer in het veld **Bestandsnaam rapport** vervolgens de vereiste naam in.
14. Selecteer **Verzendingen** in het veld **Richting**.
15. Selecteer **OK** en controleer het rapport dat in .txt-indeling gegenereerd wordt. De volgende tabel bevat de waarden in het voorbeeldrapport.

    | ISO-code partnerland | Transactiecode | Basisproductcode | Aanvullende eenheid | Gewicht | Factuurbedrag |
    |--------------------------|------------------|----------------|-----------------|--------|----------------|
    | IT                       | 1                | 10020030       | 0               | 50     | 3290           |

16. Controleer het rapport dat in Excel-indeling gegenereerd wordt.

    ![Intrastat-rapport](media/swe_intrastat_report_for_dispatches.png)

### <a name="create-a-purchase-order"></a>Inkooporder maken

1. Ga naar **Leveranciers** > **Inkooporders** > **Alle inkooporders**.
2. Selecteer **Nieuw** in het actievenster.
3. Ga in het dialoogvenster **Inkooporder maken** naar het sneltabblad **Leveranciersrekening** en selecteer **DE-001**.
4. Selecteer **OK**.
5. Controleer in het tabblad **Koptekst** in het sneltabblad **Buitenlandse** **handel** of het veld **Transactiecode** ingesteld is op **1**.
6. Selecteer in het tabblad **Regels** in het sneltabblad **Inkooporderregels** in het veld **Artikelnummer** de waarde **D0001**. Voer daarna in het veld **Hoeveelheid** de waarde **6** in.
7. Selecteer in het actievenster in het tabblad **Inkoop** in de groep **Acties** de optie **Bevestigen**.
8. Selecteer in het actievenster op het tabblad **Factuur** in de groep **Genereren** de optie **Factuur**.
9. Selecteer in het actievenster **Standaardgegevens**. Selecteer **Bestelde hoeveelheid** in het veld **Standaardhoeveelheid voor regels**. Selecteer vervolgens **OK**.
10. Voer **0001** in het sneltabblad **Koptekst leveranciersfactuur** in, in het gedeelte **Factuuridentificatie** in het veld **Nummer**.
11. Als u de factuur wilt boeken, selecteert u **Boeken** vanuit het actievenster.

### <a name="create-an-intrastat-declaration-for-arrivals"></a>Een Intrastat-aangifte voor ontvangsten aanmaken

1. Ga naar **Belasting** > **Aangiften** > **Buitenlandse handel** > **Intrastat**.
2. Selecteer in het actievenster de optie **Overboeken**.
3. Stel in het dialoogvenster **Intrastat (overboeking)** de optie **Leveranciersfactuur** in op **Ja**.
4. Selecteer **OK** om de transacties over te boeken en het Intrastat-journaal te bekijken.

    ![Intrastat-journaal voor inkooporder](media/swe_intrastat_journal_purchase_order.png)

5. Controleer het tabblad **Algemeen** voor de inkooporder.

    ![Regeldetails van Intrastat-journaal voor inkooporder](media/swe_intrastat_journal_purchase_order_line_details.png)

6. Selecteer in het actievenster **Uitvoer** > **Rapport**.
7. Selecteer in het dialoogvenster **Intrastat-rapport** op het sneltabvenster **Parameters** in de sectie **Datum** de maand van de verkooporder die u hebt gemaakt.
8. Stel in het gedeelte **Exportopties** de optie **Bestand genereren** in op **Ja**. Voer in het veld **Bestandsnaam** vervolgens de vereiste naam in.
9. Stel de optie **Rapport genereren** in op **Ja**. Voer in het veld **Bestandsnaam rapport** vervolgens de vereiste naam in.
10. Selecteer **Ontvangsten** in het veld **Richting**.
11. Selecteer **OK** en controleer het rapport dat in .txt-indeling gegenereerd wordt. De volgende tabel bevat de waarden in het voorbeeldrapport.

    | ISO-code partnerland | Transactiecode | Basisproductcode | Aanvullende eenheid | Gewicht | Factuurbedrag |
    |--------------------------|------------------|----------------|-----------------|--------|----------------|
    | IT                       | 1                | 10020030       | 0               | 30     | 1714           |

12. Controleer het rapport dat in Excel-indeling gegenereerd wordt.

    ![Intrastat-ontvangstenrapport](media/swe_intrastat_arrivals_report.png)
