---
title: De uitvoering van reekselementen in ER-indelingen uitstellen
description: In dit onderwerp wordt uitgelegd hoe u de uitvoering van een reekselement uitstelt in een ER-indeling (elektronische rapportage).
author: NickSelin
manager: kfend
ms.date: 03/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: EROperationDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 58771
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-07-01
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 9aa019e20b218fdaad4659fa65d9df629069204b
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/05/2020
ms.locfileid: "4680729"
---
# <a name="defer-the-execution-of-sequence-elements-in-er-formats"></a>De uitvoering van reekselementen in ER-indelingen uitstellen

[!include [banner](../includes/banner.md)]

## <a name="overview"></a>Overzicht

U kunt de Operations-ontwerper van het [ER](general-electronic-reporting.md)-raamwerk gebruiken om de [indelingscomponent](general-electronic-reporting.md#FormatComponentOutbound) te [configureren](tasks/er-format-configuration-2016-11.md) van een ER-oplossing die wordt gebruikt om uitgaande documenten in een tekstindeling te genereren. De hiërarchische structuur van de geconfigureerde indelingscomponent bestaat uit indelingselementen van verschillende typen. Deze indelingselementen worden gebruikt om gegenereerde documenten te vullen met de vereiste informatie tijdens runtime. Wanneer u een ER-indeling uitvoert, worden de indelingselementen standaard in dezelfde volgorde uitgevoerd als waarin deze worden weergegeven in de opmaakhiërarchie: één voor één, van boven naar beneden. In de ontwerpfase kunt u echter de uitvoeringsvolgorde wijzigen voor alle reekselementen van de geconfigureerde indelingscomponent.

Door de optie <a name="DeferredSequenceExecution"></a>**Uitgestelde uitvoering** in te schakelen voor een reeksopmaakelement in de geconfigureerde indeling kunt u de uitvoering van dat element uitstellen. In dat geval wordt het element pas uitgevoerd als alle andere elementen van het bovenliggende element zijn uitgevoerd.

Voor meer informatie over deze functie kunt u het voorbeeld in dit onderwerp uitvoeren.

## <a name="limitations"></a>Beperkingen

De optie **Uitgestelde uitvoering** wordt alleen ondersteund voor reekselementen die zijn geconfigureerd voor een ER-indeling die wordt gebruikt om **uitgaande** documenten in tekstindeling te genereren.

De optie **Uitgestelde uitvoering** is niet van toepassing op reeksen die zijn geconfigureerd als afgekapte reeksen waarvoor de maximumlengte beperkt is.

## <a name="example-defer-the-execution-of-a-sequence-element-in-an-er-format"></a><a name="Example"></a>Voorbeeld: de uitvoering van een reekselement in een ER-indeling

In de volgende stappen wordt uitgelegd hoe een gebruiker in de [rol](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/sysadmin/tasks/assign-users-security-roles) Systeembeheerder of consultant voor elektronische rapportage een ER-indeling kan configureren die een reekselement bevat waarvoor de volgorde van uitvoering verschilt van de volgorde in de indelingshiërarchie.

Deze stappen kunnen in het bedrijf **USMF** worden uitgevoerd in Microsoft Dynamics 365 Finance.

### <a name="prerequisites"></a>Vereisten

Als u de voorbeelden in dit onderwerp wilt voltooien, moet u toegang hebben tot het bedrijf **USMF** in Finance voor een van de volgende rollen:

- Functioneel consultant elektronische rapportage
- Systeembeheerder

Als u het voorbeeld nog niet hebt ingevuld in het onderwerp [De uitvoering van reekselementen in ER-indelingen uitstellen](er-defer-xml-element.md#Example), downloadt u de volgende [configuraties](general-electronic-reporting.md#Configuration) van de voorbeeld-ER-oplossing.

| Omschrijving inhoud            | Bestandsnaam |
|--------------------------------|-----------|
| Configuratie van model voor ER-gegevens    | [Model voor het leren van uitgestelde elementen.versie.1.xml](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |
| Configuratie van ER-modeltoewijzing | [Toewijzing voor het leren van uitgestelde elementen.versie.1.xml](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |

Voordat u begint, moet u ook de volgende configuratie van de voorbeeld-ER-oplossing downloaden en opslaan.

| Omschrijving inhoud     |Bestandsnaam |
|-------------------------|----------|
| ER-indelingsconfiguratie | [Indeling voor het leren van uitgestelde reeksen.versie.1.xml](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |

### <a name="import-the-sample-er-configurations"></a>De voorbeeld-ER-configuraties importeren

1. Ga naar **Organisatiebeheer** \> **Werkgebieden** \> **Elektronische rapportage**.
2. Selecteer **Rapportageconfiguraties**.
3. Als op de pagina **Configuraties** de configuratie **Model voor het leren van uitgestelde elementen** niet beschikbaar is in de configuratiestructuur, importeert u de ER-gegevensmodelconfiguratie:

    1. Selecteer **Uitwisselen** en selecteer vervolgens **Laden uit XML-bestand**.
    2. Selecteer **Bladeren**, zoek en selecteer het bestand **Model om uitgestelde elementen te leren.1.xml** en selecteer vervolgens **OK**.

4. Als de configuratie **Toewijzing voor het leren van uitgestelde elementen** niet beschikbaar is in de configuratiestructuur, importeert u de configuratie van de ER-modeltoewijzing:

    1. Selecteer **Uitwisselen** en selecteer vervolgens **Laden uit XML-bestand**.
    2. Selecteer **Bladeren**, zoek en selecteer het bestand **Toewijzing om uitgestelde elementen te leren.1.1.xml** en selecteer vervolgens **OK**.

5. De ER-indelingsconfiguratie importeren:

    1. Selecteer **Uitwisselen** en selecteer vervolgens **Laden uit XML-bestand**.
    2. Selecteer **Bladeren**, zoek en selecteer het bestand **Indeling om uitgestelde elementen te leren.1.1.xml** en selecteer vervolgens **OK**.

6. Vouw in de configuratiestructuur **Model om uitgestelde elementen te leren** uit.
7. Bekijk de lijst met geïmporteerde ER-configuraties in de configuratiestructuur.

    ![Geïmporteerde ER-configuraties op de pagina Configuratie](./media/ER-DeferredSequence-Configurations.png)

### <a name="activate-a-configurations-provider"></a>Een configuratieprovider activeren

1. Ga naar **Organisatiebeheer** \> **Werkgebieden** \> **Elektronische rapportage**.
2. Controleer op de pagina **Lokalisatieconfiguraties** in de sectie **Configuratieproviders** of de [configuratieprovider](general-electronic-reporting.md#Provider) voor het voorbeeldbedrijf Litware, Inc. (`http://www.litware.com`) wordt vermeld en of het is gemarkeerd als Actief. Als deze configuratieprovider niet wordt vermeld of als deze niet is gemarkeerd als actief, volgt u de stappen in het onderwerp [Een configuratieprovider maken en als actief markeren](./tasks/er-configuration-provider-mark-it-active-2016-11.md).

    ![Voorbeeldbedrijf Litware, Inc. op de pagina Lokalisatieconfiguraties](./media/ER-DeferredSequence-ElectronicReportingWorkspace.png)

### <a name="review-the-imported-model-mapping"></a>De geïmporteerde modeltoewijzing controleren

Controleer de instellingen van de ER-modeltoewijzingscomponent die is geconfigureerd om op verzoek toegang te krijgen tot belastingstransacties en toegang te verlenen tot gegevens waartoe toegang is verkregen.

1. Ga naar **Organisatiebeheer** \> **Werkgebieden** \> **Elektronische rapportage**.
2. Selecteer **Rapportageconfiguraties**.
3. Vouw op de pagina **Configuraties** in de configuratiestructuur **Model voor het leren van uitgestelde elementen uit**.
4. Selecteer de configuratie **Toewijzing voor het leren van uitgestelde elementen**.
5. Selecteer **Ontwerper** om de lijst met toewijzingen te openen.
6. Selecteer **Ontwerper** om de toewijzingsdetails te controleren.
7. Selecteer **Details weergeven**.
8. De gegevensbronnen controleren die zijn geconfigureerd voor toegang tot belastingstransacties:

    - De **Transacties**-gegevensbron van het type *Tabelrecord* is geconfigureerd om toegang te krijgen tot records van de toepassingstabel **TaxTrans**.
    - De gegevensbron **Boekstukken** van het type *Berekende veld* wordt zo geconfigureerd dat de vereiste boekstukcodes (**INV-10000349** en **INV-10000350**) als een lijst met records worden geretourneerd.
    - De gegevensbron **Gefilterd** van het type *Berekend veld* wordt zo geconfigureerd dat er alleen belastingstransacties van de vereiste boekstukken worden geselecteerd in de gegevensbron **Transacties**.
    - Het veld **\$TaxAmount** van het type *Berekend veld* wordt toegevoegd voor de gegevensbron **Gefilterd** om de belastingswaarde beschikbaar te maken die het tegenovergestelde teken heeft.
    - De gegevensbron **Gegroepeerd** van het type *Groeperen op* is geconfigureerd om gefilterde belastingstransacties van de gegevensbron **Gefilterd** te groeperen.
    - Het aggregatieveld **TotalSum** van de gegevensbron **Gegroepeerd** is geconfigureerd om waarden van het veld **\$TaxAmount** van de gegevensbron **Gefilterd** samen te vatten voor alle gefilterde belastingstransacties van die gegevensbron.

        ![Aggregatieveld TotalSum op de pagina 'Groeperen op'-parameters bewerken](./media/ER-DeferredSequence-GroupByParameters.png)

9. Bekijk hoe de geconfigureerde gegevensbronnen aan het gegevensmodel zijn gebonden en hoe ze gegevens waartoe toegang is verkregen, beschikbaar maken in ER-indeling:

    - De gegevensbron **Gefilterd** is gebonden aan het veld **Gegevens.Lijst** van het gegevensmodel.
    - Het veld **\$TaxAmount** van de gegevensbron **Gefilterd** is gebonden aan het veld **Gegevens.Lijst.Waarde** van het gegevensmodel.
    - Het veld **TotalSum** van de gegevensbron **Gegroepeerd** is gebonden aan het veld **Gegevens.Overzicht.Totaal** van het gegevensmodel.

    ![Pagina voor ontwerper van modeltoewijzingen](./media/ER-DeferredSequence-ModelMapping.png)

10. Sluit de pagina's **Ontwerper modeltoewijzing** en **Modeltoewijzingen**.

### <a name="review-the-imported-format"></a>De geïmporteerde indeling controleren

1. Selecteer op de pagina **Configuraties** in de configuratiestructuur de configuratie **Indeling voor het leren van uitgestelde reeksen**.
2. Selecteer **Ontwerper** om de indelingsdetails te controleren.
3. Selecteer **Details weergeven**.
4. Controleer de instellingen van de ER-indelingscomponenten die zijn geconfigureerd voor het genereren van een uitgaand document in tekstindeling dat details bevat van de belastingstransacties:

    - Het reeksindelingselement **Rapport\\Regels** is zo geconfigureerd dat het uitgaande document wordt gevuld met één regel die is gegenereerd op basis van de geneste reekselementen (**Koptekst**, **Record** en **Samenvatting**).

        ![Regelreeksindelingselement en geneste elementen op de pagina Indelingsontwerper](./media/ER-DeferredSequence-Format.png)

    - Het reeksindelingselement **Rapport\\Regels\\Koptekst** indeling is zodanig geconfigureerd dat het uitgaande document wordt gevuld met één koptekstregel die de datum en tijd aangeeft waarop de verwerking begint.
    - Het reeksindelingselement **Rapport \\Regels\\Record** is zo geconfigureerd dat het uitgaande document wordt gevuld met één regel waarin de details van afzonderlijke belastingstransacties worden weergegeven. Deze belastingstransacties worden gescheiden door een puntkomma.

        ![Recordreeksindelingselement dat een puntkomma gebruikt als scheidingsteken](./media/ER-DeferredSequence-Format1.png)

    - Het reeksindelingselement **Rapport\\Regels\\Samenvatting** is zo geconfigureerd dat het uitgaande document wordt gevuld met één samenvattingsregel die de som van de belastingswaarden uit de verwerkte belastingtransacties bevat.

4. Controleer de volgende gegevens op het tabblad **Toewijzing**:

    - Het element **Rapport\\Regels\\Koptekst** hoeft niet aan een gegevensbron te zijn gekoppeld om één regel in een uitgaand document te genereren.
    - Het element **Prefix1** genereert **P1**-symbolen om aan te geven dat de toegevoegde regel de rapportkoptekstregel is.
    - Het element **ExecutionDateTime** genereert de datum en tijd (inclusief milliseconden) wanneer de koptekstregel wordt toegevoegd.
    - Het element **Rapport\\Regels\\Record** is gebonden aan de lijst **model.Gegevens.Lijst** om één regel te genereren voor elke record in de gebonden lijst.
    - Het element **Prefix2** genereert **P2**-symbolen om aan te geven dat de regel is toegevoegd voor de belastingstransactiedetails.
    - Het element **TaxAmount** is aan **model.Gegevens.Lijst.Waarde** gekoppeld (wordt weergegeven als **\@.Waarde** in de relatieve padweergave) om de belastingswaarde van de huidige belastingstransactie te genereren.
    - Het element **RunningTotal** is een tijdelijke aanduiding voor het lopende totaal van de belastingswaarden. Dit element heeft momenteel geen uitvoer, omdat er geen binding of standaardwaarde voor is geconfigureerd.
    - Het element **ExecutionDateTime** genereert de datum en tijd (inclusief milliseconden) wanneer de huidige transactie in dit rapport wordt verwerkt.
    - Het element **Rapport\\Regels\\Samenvatting** hoeft niet aan een gegevensbron te zijn gekoppeld om één regel in een uitgaand document te genereren.
    - Het element **Prefix3** genereert **P3**-symbolen om aan te geven dat de toegevoegde regel totale belastingswaarden bevat.
    - Het element **TotalTaxAmount** is aan **model.Gegevens.Samenvatting.Totaal** gebonden om de som van de belastingswaarden van de verwerkte belastingstransacties te genereren.
    - Het element **ExecutionDateTime** genereert de datum en tijd (inclusief milliseconden) wanneer de samenvatting wordt toegevoegd.

    ![Tabblad Toewijzing op de pagina Indelingsontwerper](./media/ER-DeferredSequence-Format2.png)

### <a name="run-the-imported-format"></a>De geïmporteerde indeling uitvoeren

1. Selecteer **Uitvoeren** op de pagina **Indelingsontwerper**.
2. Download het bestand dat door de webbrowser wordt aangeboden en open het bestand ter controle.

    ![Gedownload bestand](./media/ER-DeferredSequence-Run.png)

U ziet dat overzichtsregel 22 de som van de belastingswaarden voor de verwerkte transacties weergeeft. Omdat de indeling is geconfigureerd voor het gebruik van de binding **model.Gegevens.Samenvatting.Totaal** om dit totaal te retourneren, wordt de som berekend door de **TotalSum**-aggregatie van de gegevensbron **Gegroepeerd** van het type *GroupBy* aan te roepen die de modeltoewijzing gebruikt. Voor het berekenen van deze aggregatie doorloopt de modeltoewijzing bij herhaling alle transacties die in gegevensbron **Gefilterd** zijn geselecteerd. Door de uitvoeringstijden van de regels 21 en 22 te vergelijken kunt u vaststellen dat berekening van de som 10 milliseconden (ms) duurde. Door de uitvoeringstijden van de regels 2 en 21 te vergelijken kunt u vaststellen dat het genereren van alle transactieregels 7 milliseconden (ms) duurde. Daarom was er in totaal 17 ms nodig.

### <a name="modify-the-format-so-that-the-summing-is-based-on-generated-output"></a>De indeling wijzigen zodat de optelling wordt gebaseerd op gegenereerde uitvoer

Als het volume van transacties veel groter is dan het volume in het huidige voorbeeld, kan de optellingstijd toenemen en resulteren in prestatieproblemen. Door de instelling van de indeling te wijzigen kunt u deze prestatieproblemen voorkomen. Aangezien u toegang tot belastingswaarden hebt om deze op te nemen in het gegenereerde rapport, kunt u deze informatie opnieuw gebruiken om belastingswaarden op te tellen. Zie [Indeling configureren voor tellen en totaliseren](./tasks/er-format-counting-summing-1.md) voor meer informatie.

1. Selecteer op de pagina **Indelingsontwerper** op het tabblad **Indeling** het bestandselement **Rapport** in de indelingsstructuur.
2. Stel de optie **Uitvoerdetails verzamelen** in op **Ja**. U kunt deze indeling nu configureren door de inhoud van een bestaand rapport te gebruiken als gegevensbron die toegankelijk is via de ingebouwde ER-functies in de categorie [Gegevensverzameling](er-functions-category-data-collection.md).
3. Selecteer op het tabblad **Toewijzing** het reekselement **Rapport\\Regels**.
4. Configureer de expressie **Sleutelnaam verzamelde gegevens** als `WsColumn`.
5. Configureer de expressie **Sleutelwaarde verzamelde gegevens** als `WsRow`.

    ![Regelreekselement op de pagina Indelingsontwerper](./media/ER-DeferredSequence-Format3.png)

6. Selecteer het numerieke element **Rapport\\Regels\\Record\\TaxAmount**.
7. Configureer de expressie **Sleutelnaam verzamelde gegevens** als `SummingAmountKey`.

    ![Numeriek element TaxAmount op de pagina Indelingsontwerper](./media/ER-DeferredSequence-Format4.png)

    U kunt deze instelling beschouwen als de afhandeling van een virtueel werk blad, waarbij de waarde van cel A1 wordt toegevoegd met de waarde van het belastingsbedrag uit elke verwerkte belastingstransactie.

8. Selecteer het numerieke element **Rapport\\Regels\\Record\\RunningTotal** en selecteer vervolgens **Formule bewerken**.
9. Configureer de `SUMIF(SummingAmountKey, WsColumn, WsRow)`-expressie met behulp van de ingebouwde ER-functie [SUMIF](er-functions-datacollection-sumif.md).
10. Selecteer **Opslaan**.

    ![Expressie SUMIF](./media/ER-DeferredSequence-FormulaDesigner.png)

11. Sluit de pagina **Formuleontwerper**.
12. Selecteer **Opslaan** en vervolgens **Uitvoeren**.
13. Download en controleer het bestand dat door de webbrowser wordt aangeboden.

    ![Gedownload bestand](./media/ER-DeferredSequence-Run1.png)

    Regel 21 bevat het lopende totaal van belastingswaarden die voor alle verwerkte transacties worden berekend door de gegenereerde uitvoer als gegevensbron te gebruiken. Deze gegevensbron begint aan het begin van het rapport en gaat door tot met de laatste belastingstransactie. Regel 22 bevat de som van de belastingswaarden voor alle verwerkte transacties die worden berekend in de modeltoewijzing met behulp van de gegevensbron van het type *GroupBy*. U ziet dat deze waarden gelijk zijn. Daarom kan de op uitvoer gebaseerde optelling worden gebruikt in plaats van **GroupBy**. Door de uitvoeringstijden van de regels 2 en 21 te vergelijken kunt u vaststellen dat het genereren van de transactieregels en het totaliseren 9 milliseconden (ms) duurde. Daarom is de aangepaste indeling ongeveer twee keer sneller dan de oorspronkelijke indeling voor wat betreft het genereren van gedetailleerde regels en het totaliseren van belastingswaarden.

14. Selecteer het numerieke element **Rapport\\Regels\\Samenvatting\\TotalTaxAmount** en selecteer vervolgens **Formule bewerken**.
15. Voer de `SUMIF(SummingAmountKey, WsColumn, WsRow)`-expressie in plaats van de bestaande expressie in.
16. Selecteer **Opslaan** en vervolgens **Uitvoeren**.
17. Download en controleer het bestand dat door de webbrowser wordt aangeboden.

    ![Gedownload bestand](./media/ER-DeferredSequence-Run2.png)

    Zoals u ziet, is het lopende totaal van de belastingswaarden op de laatste transactiegegevensregel gelijk aan de som op de overzichtsregel.

### <a name="put-values-of-output-based-summing-in-the-report-header"></a>Waarden van op uitvoer gebaseerde totalisatie in de rapportkoptekst plaatsen

Als u bijvoorbeeld de som van de belastingswaarden in de koptekst van uw rapport moet presenteren, kunt u de indeling wijzigen.

1. Selecteer op de pagina **Indelingsontwerper** op het tabblad **Indeling** het reekselement **Rapport\\Regels\\Samenvatting**.
2. Selecteer **Omhoog verplaatsen**.
3. Selecteer **Opslaan** en vervolgens **Uitvoeren**.
4. Download en controleer het bestand dat door de webbrowser wordt aangeboden.

    ![Gedownload bestand](./media/ER-DeferredSequence-Run3.png)

    De som van de belastingswaarden op de overzichtsregel 2 is nu gelijk aan 0 (nul), omdat dit totaal nu wordt berekend op basis van de gegenereerde uitvoer. Wanneer regel 2 wordt gegenereerd, bevat de gegenereerde uitvoer nog geen regels met transactiedetails. U kunt deze indeling zo configureren dat de uitvoering van het reekselement **Rapport\\Regels\\Samenvatting** wordt uitgevoerd totdat het reekselement **Rapport\\Regels\\Record** voor alle belastingstransacties is uitgevoerd.

### <a name="defer-the-execution-of-the-summary-sequence-so-that-the-calculated-total-is-used"></a>De uitvoering van de samenvattingsreeks uitstellen zodat het berekende totaal wordt gebruikt

1. Selecteer op de pagina **Indelingsontwerper** op het tabblad **Indeling** het reekselement **Rapport\\Regels\\Samenvatting**.
2. Stel de optie **Uitgestelde uitvoering** in op **Ja**.

    ![Optie Uitgestelde uitvoering van het Samenvatting-reekselement op de pagina Indelingsontwerper](./media/ER-DeferredSequence-Format5.png)

3. Selecteer **Opslaan** en vervolgens **Uitvoeren**.
4. Download en controleer het bestand dat door de webbrowser wordt aangeboden.

    ![Gedownload bestand](./media/ER-DeferredSequence-Run4.png)

    Het reekselement **Rapport\\Regels\\Overzicht** wordt nu alleen uitgevoerd nadat alle andere artikelen die zijn genest onder het bovenliggend element, **Rapport\\Regels**, zijn uitgevoerd. Daarom wordt het uitgevoerd nadat het reekselement **Rapport\\Regels\\Record** is uitgevoerd voor alle belastingstransacties van de gegevensbron **model.Gegevens.Lijst**. De uitvoeringstijden van de regels 1, 2 en 3 en van de laatste regel 22 geven dit feit weer.

## <a name="additional-resources"></a>Aanvullende resources

- [Indeling configureren voor tellen en totaliseren](./tasks/er-format-counting-summing-1.md)
- [Uitvoering van ER-indeling traceren om prestatieproblemen op te lossen](trace-execution-er-troubleshoot-perf.md)
- [De uitvoering van XML-elementen in ER-indelingen uitstellen](er-defer-xml-element.md#Example)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]