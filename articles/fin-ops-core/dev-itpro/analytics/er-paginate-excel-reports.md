---
title: Een ER-indeling ontwerpen om gegenereerde documenten in Excel te pagineren
description: In dit artikel wordt uitgelegd hoe u een ER-indeling (elektronische rapportage) ontwerpt die een gegenereerd document pagineert in Microsoft Excel.
author: NickSelin
ms.date: 09/14/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EROperationDesigner
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2021-08-01
ms.dyn365.ops.version: Version 10.0.22
ms.openlocfilehash: e8edc8bba62f74b4f81d423cf75b5fb87c01e43f
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8909273"
---
# <a name="design-an-er-format-to-paginate-generated-documents-in-excel"></a>Een ER-indeling ontwerpen om gegenereerde documenten in Excel te pagineren

[!include [banner](../includes/banner.md)]

In dit artikel wordt uitgelegd hoe een gebruiker in de rol Systeembeheerder of Functioneel consultant een [ER-indeling (Electronic Reporting)](general-electronic-reporting.md) kan configureren om uitgaande documenten te genereren in Microsoft Excel en paginering van documenten te beheren.

In dit voorbeeld wijzigt u de door Microsoft geleverde ER-indeling die wordt gebruikt om het controlerapport af te drukken wanneer de Intrastat-aangifte wordt [gegenereerd](../../../finance/localizations/tasks/eur-00002-eu-intrastat-declaration.md). Met dit rapport kunt u gerapporteerde Intrastat-transacties bekijken. Na de wijzigingen kunt u de paginering beheren van controlerapporten die worden gegenereerd.

De procedures in dit artikel kunnen in het bedrijf **DEMF** worden uitgevoerd. U hoeft hiervoor geen code te schrijven. Voordat u begint, moet u de volgende bestanden downloaden en opslaan.

| Beschrijving       | Bestandsnaam |
|-------------------|-----------| 
| Rapportsjabloon 1 | [ERIntrastatReportDemo1.xlsx](https://download.microsoft.com/download/7/2/a/72ae292a-8bb2-4b9d-8397-9764218f6fa8/ERIntrastatReportDemo1%20.xlsx) |
| Rapportsjabloon 2 | [ERIntrastatReportDemo2.xlsx](https://download.microsoft.com/download/7/d/1/7d15858d-6260-4afa-9dda-d8b955e59b1a/ERIntrastatReportDemo2.xlsx) |

## <a name="configure-the-er-framework"></a>Het ER-raamwerk configureren

Voer de stappen in [Het ER-raamwerk configureren](er-quick-start2-customize-report.md#ConfigureFramework) uit om de minimale set ER-parameters in te stellen. U moet deze instellingen voltooien voordat u het ER-framework gaat gebruiken om een aangepaste versie van een standaard ER-indeling te ontwerpen.

## <a name="import-the-standard-er-format-configuration"></a>Standaardconfiguratie voor ER-indeling importeren

Volg de stappen in [Standaardconfiguratie voor ER-indeling importeren](er-quick-start2-customize-report.md#ImportERSolution1) om de standaard ER-configuraties toe te voegen aan de actuele instantie van Dynamics 365 Finance. Importeer versie **1.9** van de indelingsconfiguratie van het **Intrastat-rapport**. Basisversie 1 van de basisconfiguratie van het **Intrastat-model** wordt automatisch geïmporteerd uit de opslagplaats.

## <a name="customize-the-standard-er-format"></a>De standaard-ER-indeling aanpassen

### <a name="create-the-custom-er-format"></a>De aangepaste ER-indeling maken

In dit scenario bent u vertegenwoordiger van Litware, Inc., dat momenteel is geselecteerd als de actieve ER-configuratieprovider. U moet een nieuwe ER-indelingsconfiguratie maken en daarbij de configuratie van het **Intrastat-rapport** gebruiken als basis.

1. Ga naar **Organisatiebeheer** \> **Elektronische rapportage** \> **Configuraties**.
2. Vouw op de pagina **Configuraties** in de configuratiestructuur in het linkerdeelvenster **Instrastat-model** uit en selecteer **intrastat-rapport**. Litware, Inc. gebruikt versie 1.9 van deze ER-indelingsconfiguratie als basis voor de aangepaste versie.
3. Klik op **Configuratie maken** om het dialoogvenster met de vervolgkeuzelijst te openen. Met behulp van dit dialoogvenster kunt u een nieuwe configuratie voor een aangepaste betalingsindeling maken.
4. Selecteer in de veldgroep **Nieuw** de optie **Afleiden van naam: Intrastat report, Microsoft**.
5. Voer in het veld **Naam** de waarde **Intrastat report Litware** in.
6. Selecteer **Configuratie maken** om de nieuwe indeling te maken.

Versie 1.9.1 van de ER-indelingsconfiguratie **Intrastat report Litware** wordt gemaakt. Deze versie heeft de [status](general-electronic-reporting.md#component-versioning) **Concept** en kan worden bewerkt. De huidige inhoud van uw aangepaste ER-indeling komt overeen met de inhoud van de indeling die wordt geleverd door Microsoft.

### <a name="make-the-custom-format-runnable"></a>De aangepaste indeling uitvoerbaar maken

Nu de eerste versie van uw aangepaste indeling is gemaakt en de status **Concept** heeft , kunt u de indeling uitvoeren om hem te testen. Om het rapport uit te voeren, verwerkt u een leveranciersbetaling met behulp van de betalingsmethode die verwijst naar door u aangepaste ER-indeling. Wanneer u een ER-indeling aanroept vanuit de toepassing, worden standaard alleen de versies met de status **Voltooid** en **Gedeeld** [meegenomen](general-electronic-reporting.md#component-versioning). Dit gedrag voorkomt dat ER-indelingsprofielen met niet-voltooide ontwerpen worden gebruikt. Voor het testen kunt u de toepassing dwingen de versie van de ER-indeling te gebruiken met de status **Concept**. Op deze manier kunt u de versie van de huidige indelingsversie aanpassen als er wijzigingen nodig zijn. Meer informatie over dit onderwerp vindt u in [Toepasbaarheid](electronic-reporting-destinations.md#applicability).

Als u de conceptversie van een ER-indeling wilt gebruiken, moet u de ER-indeling expliciet markeren.

1. Ga naar **Organisatiebeheer** \> **Elektronische rapportage** \> **Configuraties**.
2. Selecteer op de pagina **Configuraties** in het actievenster op het tabblad **Configuraties** in de groep **Geavanceerde instellingen** de optie **Gebruikersparameters**.
3. Stel in het dialoogvenster **Gebruikersparameters** de optie **Uitvoeringsinstellingen** in op **Ja** en selecteer **OK**.
4. Selecteer zo nodig **Bewerken** om de huidige pagina bewerkbaar te maken.
5. Selecteer in de configuratiestructuur in het linkerdeelvenster **Intrastat rapport Litware**.
6. Stel de optie **Concept uitvoeren** in op **Ja** en selecteer vervolgens **Opslaan**.

    ![De optie Concept uitvoeren op de pagina Configuraties.](./media/er-paginate-excel-reports-derived-format-configuration.png)

## <a name="set-up-foreign-trade-parameters-to-use-the-custom-er-format"></a>Parameters buitenlandse handel instellen om de aangepaste ER-indeling te gebruiken

Voer deze stappen uit om parameters voor buitenlandse handel zo te configureren dat u de aangepaste indeling kunt gebruiken.

1. Ga naar **Belasting** \> **Instellingen** \> **Buitenlandse handel** \> **Parameters buitenlandse handel**.
2. Selecteer op de pagina **Parameter buitenlandse handel** in het sneltabblad **Elektronische rapportage** in het veld **Toewijzing bestandsindeling** de waarde **Intrastat-rapport Litware**.
3. Selecteer in het veld **Toewijzing rapportindeling** de waarde **Intrastat-rapport Litware**.
4. Selecteer **Opslaan**.

## <a name="configure-the-custom-format-to-use-the-downloaded-report-template"></a>De aangepaste indeling configureren om de gedownloade rapportsjabloon te gebruiken

### <a name="review-the-first-downloaded-excel-template"></a>De eerste gedownloade Excel-sjabloon controleren

1. Open in de Excel-bureaubladtoepassing het sjabloonbestand **ERIntrastatReportDemo1.xlsx** dat u eerder hebt gedownload.
2. Controleer of de sjabloon de genoemde bereiken bevat om secties voor rapportkoptekst, rapportdetails en rapportvoettekst te maken in gegenereerde documenten.

    ![Lay-out van Excel-sjabloon 1 in de bureaubladtoepassing.](./media/er-paginate-excel-reports-template1.gif)

### <a name="replace-the-current-excel-template-in-the-custom-er-format"></a><a id="replace-template"></a>De huidige Excel-sjabloon vervangen in de aangepaste ER-indeling

U moet een nieuwe Excel-sjabloon toevoegen aan de aangepaste ER-indeling.

1. Ga naar **Organisatiebeheer** \> **Elektronische rapportage** \> **Configuraties**.
2. Vouw op de pagina **Configuraties** in de configuratiestructuur in het linkerdeelvenster **Instrastat-model** \> **Intrastat-rapport** uit en selecteer de configuratie **Intrastat-rapport Litware**.
3. Selecteer **Ontwerper**.
4. Selecteer op de pagina **Indelingsontwerper** in het actievenster de optie **Details weergeven**.
5. Zorg ervoor dat de hoofdindelingscomponent **Intrastat: Excel** is geselecteerd. Selecteer vervolgens in het actievenster op het tabblad **Importeren** in de groep **Importeren** de optie **Bijwerken vanuit Excel**.
6. Selecteer in het het dialoogvenster **Bijwerken vanuit Excel** de optie **Sjabloon bijwerken**.
7. Blader in het dialoogvenster **Openen** naar het bestand **ERIntrastatReportDemo1.xlsx** dat u eerder hebt gedownload, en selecteer vervolgens **Openen**.
8. Selecteer **OK**.
9. Selecteer **Opslaan**.

![De opmaakstructuur in de ER-indelingsontwerper na toevoegen van de nieuwe Excel-sjabloon.](./media/er-paginate-excel-reports-format1.png)

## <a name="change-the-data-binding-to-show-the-item-description-on-a-generated-report"></a>De gegevensbinding wijzigen om de artikelomschrijving weer te geven in een gegenereerd rapport

1. Ga naar de pagina **Indelingsontwerper** en selecteer het tabblad **Toewijzing**.
2. Vouw **Intrastat** \> **Rapportregels** uit en selecteer de component **Basisproductcode**.
3. Selecteer **Formule bewerken**.
4. Wijzig de bindingformule van `@.CommodityCode` in `CONCATENATE(@.CommodityCode, " ", @.ProductName)`.
5. Selecteer **Opslaan**.

![Geconfigureerde binding voor weergeven van de artikelomschrijving in de ER-indelingsontwerper.](./media/er-paginate-excel-reports-format1a.png)

## <a name="generate-an-intrastat-declaration-control-report"></a><a id="generate-intrastat-control-report"></a>Een controlerapport Intrastat-aangifte genereren

Zorg er eerst voor dat er Intrastat-transacties voor rapportage op de pagina **Intrastat** staan.

![Transacties op pagina Intrastat.](./media/er-paginate-excel-reports-transactions1.gif)

Gebruik vervolgens de aangepaste ER-indeling om het controlerapport van de Intrastat-aangifte te genereren.

1. Ga naar **Belasting** \> **Aangiften** \> **Buitenlandse handel** \> **Intrastat**.
2. Ga naar de pagina **Intrastat**, het actiepaneel en selecteer **Uitvoer** \> **Rapport**.
3. Voer de volgende stappen uit in het dialoogvenster **Intrastat-rapport** om het rapport uit te voeren:

    1. Stel de velden **Begindatum** en **Einddatum** in om specifieke Intrastat-transacties op te nemen in het rapport.
    2. Stel de optie **Bestand genereren** in op **Nee**.
    3. Stel de optie **Rapport genereren** in op **Ja**.
    4. Selecteer **OK**.

4. Download het gegenereerde document en sla dit op.
5. Open document en in Excel en beoordeel het.

    ![Gegenereerd Excel-document in de bureaubladtoepassing.](./media/er-paginate-excel-reports-document1.png)

## <a name="configure-the-custom-format-to-paginate-generated-documents"></a>De aangepaste indeling configureren voor het pagineren van gegenereerde documenten

### <a name="review-the-second-downloaded-excel-template"></a>De tweede gedownloade Excel-sjabloon controleren

1. Open in Excel het sjabloonbestand **ERIntrastatReportDemo2.xlsx** dat u eerder hebt gedownload.
2. Vergelijk deze sjabloon met de sjabloon **ERIntrastatReportDemo1.xlsx** en controleer of deze verscheidene nieuwe Excel-namen bevat om paginaspecifieke secties te maken en in gegenereerde documenten te vullen:

    - Het bereik **ReportPageHeader** wordt toegevoegd om kopteksten op de pagina te maken.
    - Het bereik **ReportPageFooter** wordt toegevoegd om voetteksten op de pagina te maken.
    - De **cel ReportPageFooter\_PageLines** is zo geconfigureerd dat het aantal transacties per pagina wordt weergegeven.
    - De **cel ReportPageFooter\_PageAmount** is zo geconfigureerd dat het totaalbedrag van transacties per pagina wordt weergegeven.
    - De **cel ReportPageFooter\_PageWeight** is zo geconfigureerd dat het totaalgewicht van transacties per pagina wordt weergegeven.
    - De cel **ReportPageFooter\_RunningCounterLines** is zo geconfigureerd dat de lopende teller van transacties wordt weergegeven vanaf het begin van het rapport tot en met huidige pagina.
    - De cel **ReportPageFooter\_RunningTotalAmount** is zo geconfigureerd dat het lopende totaalbedrag van alle transacties wordt weergegeven vanaf het begin van het rapport tot en met huidige pagina.
    - De cel **ReportPageFooter\_RunningTotalWeight** is zo geconfigureerd dat het lopende totaalgewicht van alle transacties wordt weergegeven vanaf het begin van het rapport tot en met huidige pagina.

    ![Lay-out van Excel-sjabloon 2 in de bureaubladtoepassing.](./media/er-paginate-excel-reports-template2a.gif)

    De cel **CommodityCode** van deze sjabloon is geconfigureerd voor tekst in de cel te laten teruglopen. Aangezien de rij met transactiedetails zo is geconfigureerd dat deze automatisch aan de hoogte van een rij wordt aangepast, moet de hoogte van de hele rij automatisch wijzigen wanneer de tekst in de cel **CommodityCode** terugloopt.

    ![De cel CommodityCode die is geconfigureerd voor het teruglopen van tekst.](./media/er-paginate-excel-reports-template2b.gif)

### <a name="repeat-the-replacement-of-the-current-excel-template-in-the-custom-er-format"></a>Herhaal de vervanging van de huidige Excel-sjabloon in de aangepaste ER-indeling

1. Volg de stappen in de sectie [De huidige Excel-sjabloon vervangen in de aangepaste ER-indeling](#replace-template) van dit artikel. Selecteer echter in stap 7 het bestand **ERIntrastatReportDemo2.xlsx**.
2. Ga naar de pagina **Indelingsontwerper** en vouw **Intrastat** uit.
3. Geef de indelingscomponenten [Bereik](er-fillable-excel.md#range-component) op die zijn toegevoegd aan de bewerkbare ER-indeling om de structuur te synchroniseren met de structuur van de toegepaste Excel-sjabloon:

    1. Selecteer de component **Bereik** die is gekoppeld aan de Excel-naam **ReportPageHeader**.
    2. Voer op het tabblad **Opmaak**, in het veld **Naam**, de **koptekst van de rapportpagina** in.
    3. Selecteer de component **Bereik** die is gekoppeld aan de Excel-naam **ReportPageFooter**.
    4. Voer op het tabblad **Opmaak**, in het veld **Naam**, de **voettekst van de rapportpagina** in.

4. Selecteer **Opslaan**.

![De opmaakstructuur in de ER-indelingsontwerper na het vervangen van de Excel-sjabloon.](./media/er-paginate-excel-reports-format2.png)

### <a name="change-the-format-structure-to-implement-document-pagination"></a>De indelingsstructuur wijzigen om documentpaginering te implementeren

1. Selecteer op de pagina **Indelingsontwerper**, in de opmaakstructuur in het linkerdeelvenster, de hoofdcomponent **Intrastat**.
2. Selecteer **Toevoegen**.
3. Selecteer in het dialoogvenster **Toevoegen** het onderdeel [Pagina](er-fillable-excel.md#page-component) in de **Excel**-groep met onderdelen.
4. Voer in het dialoogvenster **Onderdeeleigenschappen**, in het veld **Naam**, **Rapportpagina** in. Selecteer vervolgens **OK**.
5. Voer de volgende stappen uit om het onderdeel **Paginakoptekst van rapport** als paginakoptekst te gebruiken op elke gegenereerde pagina:

    1. Selecteer het onderdeel **Paginakoptekst van rapport** en selecteer vervolgens **Knippen**.
    2. Selecteer het onderdeel **Rapportpagina** en selecteer vervolgens **Plakken**.
    3. Vouw de **Rapportpagina** uit.
    4. Als u wilt afdwingen dat het onderdeel **Pagina** dit bereik [beschouwt](er-fillable-excel.md#page-component-structure) als paginakoptekst, selecteert u **Paginakoptekst van rapport**. Selecteer vervolgens op het tabblad **Opmaak** in het veld **Replicatierichting** de optie **Geen replicatie**.

6. Voer deze stappen uit om een gegenereerd document te pagineren zodat rekening wordt gehouden met de inhoud op rapportregels:

    1. Selecteer het onderdeel **Rapportregels** en selecteer vervolgens **Knippen**.
    2. Selecteer het onderdeel **Rapportpagina** en selecteer vervolgens **Plakken**.

7. Voer deze stappen uit om de voettekst van het rapport op te nemen na de rapportregels, maar vóór de laatste voettekst van de pagina:

    1. Selecteer het onderdeel **Rapportvoettekst** en selecteer vervolgens **Knippen**.
    2. Selecteer het onderdeel **Rapportpagina** en selecteer vervolgens **Plakken**.

8. Voer de volgende stappen uit om het onderdeel **Paginavoettekst van rapport** als paginavoettekst te gebruiken op elke gegenereerde pagina:

    1. Selecteer het onderdeel **Paginavoettekst van rapport** en selecteer vervolgens **Knippen**.
    2. Selecteer het onderdeel **Rapportpagina** en selecteer vervolgens **Plakken**.
    3. Als u wilt afdwingen dat het onderdeel **Pagina** dit bereik [beschouwt](er-fillable-excel.md#page-component-structure) als paginavoettekst, selecteert u **Paginavoettekst van rapport**. Selecteer vervolgens op het tabblad **Opmaak** in het veld **Replicatierichting** de optie **Geen replicatie**.

![De opmaakstructuur in de ER-indelingsontwerper na implementeren van documentpaginering.](./media/er-paginate-excel-reports-format3.png)

### <a name="add-data-sources-to-calculate-page-footer-totals"></a>Gegevensbronnen toevoegen om de totalen voor paginavoettekst te berekenen

U moet nieuwe gegevensbronnen configureren om het paginatotaal, de lopende teller en de lopende totaalwaarden te berekenen en om deze weer te geven in de sectie paginavoettekst. We raden aan om gegevensbronnen van [Gegevensverzameling](er-data-collection-data-sources.md) te gebruiken voor dit doel.

1. Ga naar de pagina **Indelingsontwerper** en selecteer het tabblad **Toewijzing**.
2. Selecteer **Basis toevoegen** en voer vervolgens de volgende stappen uit:

    1. Ga in het dialoogvenster **Gegevensbron toevoegen** naar de sectie **Algemeen** en selecteer **Lege container**.
    2. Voer in het dialoogvenster **Gegevensbroneigenschappen lege container** in het veld **Naam** de waarde **Total** in.
    3. Selecteer **OK**.

3. Selecteer de gegevensbron **Total**, selecteer **Toevoegen** en ga daarna als volgt te werk:

    1. Ga in het dialoogvenster **Gegevensbron toevoegen** naar de sectie **Algemeen** en selecteer **Lege container**.
    2. Voer in het dialoogvenster **Gegevensbroneigenschappen lege container** in het veld **Naam** de waarde **Pagina** in.
    3. Selecteer **OK**.

4. Selecteer nogmaals **Toevoegen** en voer de volgende stappen uit:

    1. Ga in het dialoogvenster **Gegevensbron toevoegen** naar de sectie **Algemeen** en selecteer **Lege container**.
    2. Voer in het dialoogvenster **Gegevensbroneigenschappen lege container** in het veld **Naam** de waarde **Running** in.
    3. Selecteer **OK**.

5. Selecteer de gegevensbron **Total.Page**, selecteer **Toevoegen** en ga daarna als volgt te werk:

    1. Ga in het dialoogvenster **Gegevensbron toevoegen** naar de sectie **Functies** en selecteer **Gegevensverzameling**.
    2. Voer in het dialoogvenster **Gegevensbroneigenschappen Gegevensverzameling** in het veld **Naam** de waarde **Bedrag** in.
    3. Selecteer in het veld **Itemtype** **Werkelijk**.
    4. Stel de optie **Alle waarden verzamelen** in op **Ja**.
    5. Selecteer **OK**.

6. Selecteer nogmaals **Toevoegen** en voer de volgende stappen uit:

    1. Ga in het dialoogvenster **Gegevensbron toevoegen** naar de sectie **Functies** en selecteer **Gegevensverzameling**.
    2. Voer in het dialoogvenster **Gegevensbroneigenschappen Gegevensverzameling** in het veld **Naam** de waarde **Gewicht** in.
    3. Selecteer in het veld **Itemtype** **Werkelijk**.
    4. Stel de optie **Alle waarden verzamelen** in op **Ja**.
    5. Selecteer **OK**.

7. Selecteer de gegevensbron **Total.Running**, selecteer **Toevoegen** en ga daarna als volgt te werk:

    1. Ga in het dialoogvenster **Gegevensbron toevoegen** naar de sectie **Functies** en selecteer **Gegevensverzameling**.
    2. Voer in het dialoogvenster **Gegevensbroneigenschappen Gegevensverzameling** in het veld **Naam** de waarde **Bedrag** in.
    3. Selecteer in het veld **Itemtype** **Werkelijk**.
    4. Stel het veld **Alle waarden verzamelen** in op **Ja**.
    5. Selecteer **OK**.

8. Selecteer nogmaals **Toevoegen** en voer de volgende stappen uit:

    1. Ga in het dialoogvenster **Gegevensbron toevoegen** naar de sectie **Functies** en selecteer **Gegevensverzameling**.
    2. Voer in het dialoogvenster **Gegevensbroneigenschappen Gegevensverzameling** in het veld **Naam** de waarde **Gewicht** in.
    3. Selecteer in het veld **Itemtype** **Werkelijk**.
    4. Stel het veld **Alle waarden verzamelen** in op **Ja**.
    5. Selecteer **OK**.

9. Selecteer nogmaals **Toevoegen** en voer de volgende stappen uit:

    1. Ga in het dialoogvenster **Gegevensbron toevoegen** naar de sectie **Functies** en selecteer **Gegevensverzameling**.
    2. Voer in het dialoogvenster **Gegevensbroneigenschappen Gegevensverzameling** in het veld **Naam** de waarde **Regels** in.
    3. Selecteer in het veld **Itemtype** de waarde **Geheel getal**.
    4. Stel het veld **Alle waarden verzamelen** in op **Ja**.
    5. Selecteer **OK**.

10. Selecteer **Opslaan**.

### <a name="add-data-sources-to-control-page-footer-visibility"></a>Gegevensbronnen toevoegen om de zichtbaarheid van de paginavoettekst te sturen

Als u de zichtbaarheid van de paginavoettekst wilt sturen en de voettekst niet wilt opnemen op de laatste pagina als deze transacties bevat, configureert u een nieuwe gegevensbron om de vereiste lopende teller te berekenen.

1. Ga naar de pagina **Indelingsontwerper** en selecteer het tabblad **Toewijzing**.
2. Selecteer de gegevensbron **Total.Running** en selecteer **Toevoegen**.
3. Ga in het dialoogvenster **Gegevensbron toevoegen** naar de sectie **Functies** en selecteer **Gegevensverzameling**.
4. Voer in het dialoogvenster **Gegevensbroneigenschappen Gegevensverzameling** in het veld **Naam** de waarde **Regels2** in.
5. Selecteer in het veld **Itemtype** de waarde **Geheel getal**.
6. Stel de optie **Alle waarden verzamelen** in op **Ja**.
7. Selecteer **OK**.
8. Selecteer **Opslaan**.

![Toegevoegde gegevensbronnen in de ER-indelingsontwerper.](./media/er-paginate-excel-reports-format4.png)

### <a name="configure-bindings-to-collect-total-values"></a>Bindingen configureren om totaalwaarden te verzamelen

1. Vouw op de pagina **Indelingsontwerper**, in de opmaakstructuur, het onderdeel **Rapportregels** uit en selecteer het geneste onderdeel **Factuurwaarde**.
2. Selecteer **Formule bewerken**.
3. Wijzig de bindingformule van `NUMBERVALUE(NUMBERFORMAT(@.InvoiceValue, "F"&TEXT(model.Parameters.IntrastatAmountDecimals)), ".", "")` in `Total.Page.Amount.Collect(NUMBERVALUE(NUMBERFORMAT(@.InvoiceValue, "F"&TEXT(model.Parameters.IntrastatAmountDecimals)), ".", ""))`.

    > [!NOTE]
    > Deze binding plaatst niet alleen de bedragwaarde voor elke geïtereerde transactie in een Excel-cel, maar verzamelt de waarde ook in de gegevensbron **Total.Page.Amount**.

4. Selecteer het geneste onderdeel **Gewicht**.
5. Selecteer **Formule bewerken**.
6. Wijzig de bindingformule van `@.'$RoundedWeight'` in `Total.Page.Weight.Collect(@.'$RoundedWeight')`.

    > [!NOTE]
    > Deze binding plaatst niet alleen de gewichtwaarde voor elke geïtereerde transactie in een Excel-cel, maar verzamelt de waarde ook in de gegevensbron **Total.Page.Weight**.

![Geconfigureerde bindingen voor verzamelen van totaalwaarden in de ER-indelingsontwerper.](./media/er-paginate-excel-reports-format5.png)

### <a name="configure-bindings-to-fill-in-page-footer-totals"></a>Bindingen configureren om totalen in paginavoetteksten in te vullen

1. Vouw op de pagina **indelingsontwerper**, in de indelingsstructuur, het onderdeel **Paginavoettekst van rapport** uit, selecteer het geneste onderdeel **Bereik** dat verwijst naar de Excel-cel **ReportPageFooter\_PageAmount** en ga daarna als volgt te werk:

    1. Selecteer in de gegevensbronnenstructuur in het rechterdeelvenster het item **Total.Page.Amount.Sum()**.
    2. Selecteer **Binden**.
    3. Selecteer **Formule bewerken**.
    4. Werk de formule bij naar `Total.Page.Amount.Sum(false)`.

    > [!NOTE]
    > U moet het argument van deze functie opgeven als **Onwaar** om verzamelde gegevens voor de huidige pagina te bewaren, omdat deze gegevens vereist zijn voor het berekenen van het bedrag van het lopende totaal, het totale aantal regels per pagina en de lopende teller van regels.

2. Selecteer in de indelingsstructuur het geneste onderdeel **Bereik** dat verwijst naar de Excel-cel **ReportPageFooter\_PageWeight**, en voer vervolgens deze stappen uit:

    1. Selecteer in de gegevensbronnenstructuur in het rechterdeelvenster het item **Total.Page.Weight.Sum()**.
    2. Selecteer **Binden**.
    3. Selecteer **Formule bewerken**.
    4. Werk de formule bij naar `Total.Page.Weight.Sum(false)`.

### <a name="configure-bindings-to-fill-in-page-running-totals"></a>Bindingen configureren om lopende totalen in pagina's in te vullen

1. Vouw op de pagina **indelingsontwerper**, in de indelingsstructuur, het onderdeel **Paginavoettekst van rapport** uit, selecteer het geneste onderdeel **Bereik** dat verwijst naar de Excel-cel **ReportPageFooter\_RunningTotalAmount** en ga daarna als volgt te werk:

    1. Selecteer in de gegevensbronnenstructuur in het rechterdeelvenster het item **Total.Running.Amount.Collect()**.
    2. Selecteer **Binden**.
    3. Selecteer **Formule bewerken**.
    4. Werk de formule bij naar `Total.Running.Amount.Sum(false)+Total.Running.Amount.Collect(Total.Page.Amount.Sum(true))`.

    > [!NOTE]
    > De operand `Total.Running.Amount.Sum(false)` retourneert het eerder verzamelde bedrag van het lopende totaal. De operand `Total.Running.Amount.Collect(Total.Page.Amount.Sum(true))` retourneert het totaalbedrag van de huidige pagina. U moet het argument opgeven van de geneste functie van de tweede operand als **Waar** om de gegevensverzameling `Total.Page.Amount` te resetten zodra deze waarde wordt geplaatst in de verzameling lopende totalen `Total.Running.Amount` . Het opgegeven argument moet beginnen met het verzamelen van het totaal voor de volgende pagina vanaf een nulwaarde (0).
    >
    > De functie `Total.Running.Amount.Sum(false)` wordt aangeroepen om het lopende totaalbedrag in te voeren in de Excel-cel **ReportPageFooter\_RunningTotalAmount** op de huidige pagina.

2. Selecteer in de indelingsstructuur het geneste onderdeel **Bereik** dat verwijst naar de Excel-cel **ReportPageFooter\_RunningTotalWeight**, en voer vervolgens deze stappen uit:

    1. Selecteer in de gegevensbronnenstructuur in het rechterdeelvenster het item **Total.Running.Weight.Collect()**.
    2. Selecteer **Binden**.
    3. Selecteer **Formule bewerken**.
    4. Werk de formule bij naar `Total.Running.Weight.Sum(false)+Total.Running.Weight.Collect(Total.Page.Weight.Sum(true))`.

### <a name="configure-bindings-to-fill-in-the-page-running-counter"></a>Bindingen configureren om lopende teller in pagina's in te vullen

1. Vouw op de pagina **indelingsontwerper**, in de indelingsstructuur, het onderdeel **Paginavoettekst van rapport** uit, en selecteer het geneste onderdeel **Bereik** dat verwijst naar de Excel-cel **ReportPageFooter\_RunningCounterLines**.
2. Selecteer **Formule bewerken**.
3. Voeg de formule `Total.Running.Lines.Collect(COUNT(Total.Page.Amount.Result))` toe.

    > [!NOTE]
    > Deze formule retourneert het aantal verzamelde bedragwaarden voor het hele rapport. Dit aantal is gelijk aan het aantal transacties dat op dat moment is geïtereerd. Tegelijkertijd verzamelt de formule de geretourneerde waarde in de verzameling **Total.Running.Lines**.

### <a name="configure-bindings-to-fill-in-the-page-footer-counter"></a>Bindingen configureren om de teller in paginavoetteksten in te vullen

1. Vouw op de pagina **indelingsontwerper**, in de indelingsstructuur, het onderdeel **Paginavoettekst van rapport** uit, en selecteer het geneste onderdeel **Bereik** dat verwijst naar de Excel-cel **ReportPageFooter\_PageLines**.
2. Selecteer **Formule bewerken**.
3. Voeg de formule `COUNT(Total.Page.Amount.Result)-Total.Running.Lines.Sum(false)` toe.

    > [!NOTE]
    > Met deze formule wordt het aantal transacties op de huidige pagina berekend als het verschil tussen het aantal transacties dat is verzameld in **Total.Page.Amount.Result** voor het hele rapport, en het aantal transacties dat in deze fase is opgeslagen in **Total.Running.Lines.Sum**. Omdat het aantal transacties voor de huidige pagina wordt opgeslagen in **Total.Running.Lines** in de binding van het onderdeel **Bereik** dat verwijst naar de Excel-cel **ReportPageFooter\_RunningCounterLines**, is het aantal transacties op de huidige pagina onderdeel nog niet opgenomen. Daarom is dit verschil gelijk aan het aantal transacties op de huidige pagina.

![Geconfigureerde bindingen om de voettekstteller van de pagina in te vullen in de ER-indelingsontwerper.](./media/er-paginate-excel-reports-format6.png)

### <a name="configure-component-visibility"></a>Zichtbaarheid van onderdelen configureren

U kunt de zichtbaarheid van de paginakop- en voettekst op een specifieke pagina van een gegenereerd document wijzigen om de volgende elementen te verbergen:

- De paginakoptekst op de eerste pagina, omdat de rapportkop al kolomtitels bevat
- De paginakoptekst op elke pagina zonder transacties die voor de laatste pagina kunnen optreden
- De paginavoettekst op elke pagina zonder transacties die voor de laatste pagina kunnen optreden

Als u de zichtbaarheid wilt wijzigen, moet u de eigenschap **Ingeschakeld** van de onderdelen **Paginakoptekst van rapport** en **Paginavoettekst van rapport** bijwerken.

1. Vouw op de pagina **Indelingsontwerper**, in de opmaakstructuur, het onderdeel **Rapportpagina** uit, selecteer het geneste onderdeel **Paginakoptekst van rapport** en voer deze stappen uit:

    1. Selecteer **Bewerken** voor het veld **Ingeschakeld**.
    2. Voer op de pagina **Formuleontwerper** in het veld **Formule** de volgende expressie in:

        `AND(`<br>
        `COUNT(Total.Page.Amount.Result)<>0,`<br>
        `COUNT(Total.Page.Amount.Result)<>COUNT(model.CommodityRecord)`<br>
        `)`

2. Selecteer in de opmaakstructuur het geneste onderdeel **Paginavoettekst van rapport** en ga als volgt te werk:

    1. Selecteer **Bewerken** voor het veld **Ingeschakeld**.
    2. Voer op de pagina **Formuleontwerper** in het veld **Formule** de volgende expressie in:

        `(`<br>
        `COUNT(Total.Page.Amount.Result)-Total.Running.Lines2.Sum(false)+`<br>
        `0*Total.Running.Lines2.Collect(COUNT(Total.Page.Amount.Result))`<br>
        `)<>0`

    > [!NOTE]
    > De constructie `COUNT(Total.Page.Amount.Result)-Total.Running.Lines2.Sum(false)` wordt gebruikt om het aantal transacties op de huidige pagina te berekenen. De constructie `0*Total.Running.Lines2.Collect(COUNT(Total.Page.Amount.Result)` wordt gebruikt om het aantal transacties op de huidige pagina aan de verzameling toe te voegen, om de zichtbaarheid van de volgende pagina op de juiste manier af te handelen.
    >
    > De verzameling `Total.Running.Lines` kan hier niet worden hergebruikt, omdat de eigenschap **Ingeschakeld** van een basiscomponent wordt verwerkt **nadat** de bindingen van geneste onderdelen zijn verwerkt. Wanneer de eigenschap **Ingeschakeld** wordt verwerkt, wordt de verzameling `Total.Running.Lines` al opgehoogd met het aantal transacties op de huidige pagina.

3. Selecteer **Opslaan**.

## <a name="generate-an-intrastat-declaration-control-report-updated"></a>Een controlerapport Intrastat-aangifte genereren (bijgewerkt)

1. Zorg ervoor dat er 24 transacties op de pagina **Intrastat** staan. Herhaal de stappen in de sectie [Een controlerapport Intrastat-aangifte genereren](#generate-intrastat-control-report) van dit artikel om het controlerapport te genereren en te controleren.

    Alle transacties worden op de eerste pagina weergegeven. De paginatotalen en -tellers zijn gelijk aan de rapporttotalen en -tellers. Het bereik paginakoptekst is verborgen op de eerste pagina omdat de rapportkop al kolomtitels bevat. De paginakoptekst en -voettekst zijn verborgen op de tweede pagina omdat die pagina geen transacties bevat.

    ![Gegenereerd Excel-document in bureaubladtoepassing.](./media/er-paginate-excel-reports-document2.gif)

2. Werk twee transacties bij op de pagina **Intrastat** door de code **Artikelnummer** te wijzigen van **D00006** in **L0010**. De productnaam van het nieuwe artikel, **Actieve stereoluidsprekers**, is langer dan de productnaam van het oorspronkelijke artikel, **Standaardluidspreker**. Deze situatie dwingt tekstterugloop af in de bijbehorende cel van het gegenereerde document. Documentpaginering en paginagerelateerde totalisering en telling moeten nu worden bijgewerkt. Herhaal de stappen in de sectie [Een controlerapport Intrastat-aangifte genereren](#generate-intrastat-control-report) om het controlerapport te genereren en te controleren.

    Op dit moment worden transacties op twee pagina's weergegeven en zijn de paginatotalen en tellers correct berekend. Het paginakoptekstbereik is correct verborgen op de eerste pagina en zichtbaar op de tweede pagina. De paginavoettekst is zichtbaar op beide pagina's omdat ze transacties bevatten.

    ![Bijgewerkt gegenereerd Excel-document in de bureaubladtoepassing.](./media/er-paginate-excel-reports-document3.gif)

## <a name="frequently-asked-questions"></a>Veelgestelde vragen

### <a name="is-there-any-way-to-recognize-when-the-final-page-is-processed-by-the-page-format-component"></a>Is er een manier om te herkennen wanneer de laatste pagina wordt verwerkt door het onderdeel Pagina-indeling?

Het onderdeel **Pagina** geeft [geen informatie](er-fillable-excel.md#page-component-limitations) weer over het aantal verwerkte pagina's en het totale aantal pagina's in een gegenereerd document. Het is echter mogelijk om ER [formules](er-formula-language.md) zo te configureren dat de laatste pagina wordt herkend. Dit is een voorbeeld:

- Bereken het totale aantal transacties dat al is verwerkt met behulp van het onderdeel **Rapportpagina**. U kunt deze berekening uitvoeren met de formule `COUNT(Total.Page.Amount.Result)`. 
- Het totale aantal transacties berekenen dat moet worden verwerkt op basis van de binding `model.CommodityRecord` die is geconfigureerd voor het onderdeel **Rapportregels**. U kunt deze berekening uitvoeren met de formule `COUNT(model.CommodityRecord)`.
- Vergelijk twee getallen om de laatste pagina te herkennen. Als beide waarden gelijk zijn, wordt de laatste pagina gegenereerd.

> [!NOTE]
> We raden aan deze methode alleen te gebruiken wanneer de eigenschap **Ingeschakeld** van het onderdeel **Rapportregels** geen formule bevat die [Onwaar](er-formula-supported-data-types-primitive.md#boolean) kan retourneren bij runtime voor sommige geïtereerde [records](er-formula-supported-data-types-composite.md#record) in de gebonden [Recordlijst](er-formula-supported-data-types-composite.md#record-list).

## <a name="additional-resources"></a>Aanvullende bronnen

- [Een configuratie ontwerpen voor het genereren van documenten in Excel-indeling](er-fillable-excel.md)
- [Gegevensbronnen voor GEGEVENSVERZAMELING in elektronische rapportageindelingen (ER) gebruiken](er-data-collection-data-sources.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
