---
title: De uitvoering van XML-elementen in ER-indelingen uitstellen
description: In dit onderwerp wordt uitgelegd hoe u de uitvoering van een XML-element uitstelt in een ER-indeling (elektronische rapportage).
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
ms.search.validFrom: 2020-01-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: 6dce3768c886403f789063d516e0e696fc829f81
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/05/2020
ms.locfileid: "4680705"
---
# <a name="defer-the-execution-of-xml-elements-in-er-formats"></a>De uitvoering van XML-elementen in ER-indelingen uitstellen

[!include [banner](../includes/banner.md)]

## <a name="overview"></a>Overzicht

U kunt de Operations-ontwerper van het [ER](general-electronic-reporting.md)-raamwerk gebruiken om de [indelingscomponent](general-electronic-reporting.md#FormatComponentOutbound) te [configureren](./tasks/er-format-configuration-2016-11.md) van een ER-oplossing die wordt gebruikt om uitgaande documenten in een XML-indeling te genereren. De hiërarchische structuur van de geconfigureerde indelingscomponent bestaat uit indelingselementen van verschillende typen. Deze indelingselementen worden gebruikt om gegenereerde documenten te vullen met de vereiste informatie tijdens runtime. Wanneer u een ER-indeling uitvoert, worden de indelingselementen standaard in dezelfde volgorde uitgevoerd als waarin deze worden weergegeven in de opmaakhiërarchie: één voor één, van boven naar beneden. In de ontwerpfase kunt u echter de uitvoeringsvolgorde wijzigen voor alle XML-elementen van de geconfigureerde indelingscomponent.

Door de optie <a name="DeferredXmlElementExecution"></a>**Uitgestelde uitvoering** in te schakelen voor een XML-element in de geconfigureerde indeling kunt u de uitvoering van dat element uitstellen. In dat geval wordt het element pas uitgevoerd als alle andere elementen van het bovenliggende element zijn uitgevoerd.

Voor meer informatie over deze functie kunt u het voorbeeld in dit onderwerp uitvoeren.

## <a name="limitations"></a>Beperkingen

De optie **Uitgestelde uitvoering** wordt alleen ondersteund voor XML-elementen die zijn geconfigureerd voor een ER-indeling die wordt gebruikt om **uitgaande** documenten in XML-indeling te genereren.

De optie **Uitgestelde uitvoering** wordt alleen ondersteund voor XML-elementen die zich in slechts één ander XML-element bevinden. Het is daarom niet van toepassing op XML-elementen die zich in andere typen opmaakelementen bevinden (bijvoorbeeld in **een XML-reeks** element).

De optie **Uitgestelde uitvoering** wordt niet ondersteund voor XML-elementen die zich in het opmaakelement **Common\\File** bevinden wanneer de optie **Bestand splitsen** is ingesteld op **Ja**. Zie voor meer informatie over het splitsen van XML-bestanden [Gegenereerde XML-bestanden splitsen op basis van bestandsgrootte en hoeveelheid inhoud](er-split-files.md).

## <a name="example-defer-the-execution-of-an-xml-element-in-an-er-format"></a><a name="Example"></a>Voorbeeld: de uitvoering van een XML-element in een ER-indeling uitstellen

In de volgende stappen wordt uitgelegd hoe een gebruiker in de [rol](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/sysadmin/tasks/assign-users-security-roles) Systeembeheerder of consultant voor elektronische rapportage een ER-indeling kan configureren die een XML-element bevat waarvoor de volgorde van uitvoering verschilt van de volgorde in de indelingshiërarchie.

Deze stappen kunnen in het bedrijf **USMF** worden uitgevoerd in Microsoft Dynamics 365 Finance.

### <a name="prerequisites"></a>Vereisten

Als u de voorbeelden in dit onderwerp wilt voltooien, moet u toegang hebben tot het bedrijf **USMF** in Finance voor een van de volgende rollen:

- Functioneel consultant elektronische rapportage
- Systeembeheerder

Als u het voorbeeld nog niet hebt ingevuld in het onderwerp [De uitvoering van reekselementen in ER-indelingen uitstellen](er-defer-sequence-element.md#Example), downloadt u de volgende [configuraties](general-electronic-reporting.md#Configuration) van de voorbeeld-ER-oplossing.

| Omschrijving inhoud            | Bestandsnaam |
|--------------------------------|-----------|
| Configuratie van model voor ER-gegevens    | [Model voor het leren van uitgestelde elementen.versie.1.xml](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |
| Configuratie van ER-modeltoewijzing | [Toewijzing voor het leren van uitgestelde elementen.versie.1.xml](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |

Voordat u begint, moet u ook de volgende configuratie van de voorbeeld-ER-oplossing downloaden en opslaan op uw lokale computer.

| Omschrijving inhoud     | Bestandsnaam |
|-------------------------|-----------|
| ER-indelingsconfiguratie | [Indeling voor het leren van uitgestelde XML-elementen.versie.1.1.xml](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |

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
    2. Selecteer **Bladeren**, zoek en selecteer het bestand **Indeling om XML-elementen te leren.1.1.xml** en selecteer vervolgens **OK**.

6. Vouw in de configuratiestructuur **Model om uitgestelde elementen te leren** uit.
7. Bekijk de lijst met geïmporteerde ER-configuraties in de configuratiestructuur.

    ![Geïmporteerde ER-configuraties op de pagina Configuratie](./media/ER-DeferredXml-Configurations.png)

### <a name="activate-a-configuration-provider"></a>Een configuratieprovider activeren

1. Ga naar **Organisatiebeheer** \> **Werkgebieden** \> **Elektronische rapportage**.
2. Controleer op de pagina **Lokalisatieconfiguraties** in de sectie **Configuratieproviders** of de [configuratieprovider](general-electronic-reporting.md#Provider) voor het voorbeeldbedrijf Litware, Inc. (`http://www.litware.com`) wordt vermeld en of het is gemarkeerd als Actief. Als deze configuratieprovider niet wordt vermeld of als deze niet is gemarkeerd als actief, volgt u de stappen in het onderwerp [Een configuratieprovider maken en als actief markeren](./tasks/er-configuration-provider-mark-it-active-2016-11.md).

    ![Voorbeeldbedrijf Litware, Inc. op de pagina Lokalisatieconfiguraties](./media/ER-DeferredXml-ElectronicReportingWorkspace.png)

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

        ![Aggregatieveld TotalSum op de pagina 'Groeperen op'-parameters bewerken](./media/ER-DeferredXml-GroupByParameters.png)

9. Bekijk hoe de geconfigureerde gegevensbronnen aan het gegevensmodel zijn gebonden en hoe ze gegevens waartoe toegang is verkregen, beschikbaar maken in ER-indeling:

    - De gegevensbron **Gefilterd** is gebonden aan het veld **Gegevens.Lijst** van het gegevensmodel.
    - Het veld **\$TaxAmount** van de gegevensbron **Gefilterd** is gebonden aan het veld **Gegevens.Lijst.Waarde** van het gegevensmodel.
    - Het veld **TotalSum** van de gegevensbron **Gegroepeerd** is gebonden aan het veld **Gegevens.Overzicht.Totaal** van het gegevensmodel.

    ![Pagina voor ontwerper van modeltoewijzingen](./media/ER-DeferredXml-ModelMapping.png)

10. Sluit de pagina's **Ontwerper modeltoewijzing** en **Modeltoewijzingen**.

### <a name="review-the-imported-format"></a>De geïmporteerde indeling controleren

1. Selecteer op de pagina **Configuraties** in de configuratiestructuur de configuratie **Indeling voor het leren van XML-elementen**.
2. Selecteer **Ontwerper** om de indelingsdetails te controleren.
3. Selecteer **Details weergeven**.
4. Controleer de instellingen van de ER-indelingscomponenten die zijn geconfigureerd voor het genereren van een uitgaand document in XML-indeling dat details bevat van de belastingstransacties:

    - Het XML-element **Rapport\\Bericht** is zo geconfigureerd dat het uitgaande document wordt gevuld met één knooppunt dat de geneste XML-elementen(**Koptekst**, **Record** en **Samenvatting**) bevat.
    - Het XML-element **Rapport\\Bericht\\Koptekst** is zo geconfigureerd dat het uitgaande document wordt gevuld met één koptekstregel die de datum en tijd aangeeft waarop de verwerking begint.
    - Het XML-element **Rapport \\Bericht\\Record** is zo geconfigureerd dat het uitgaande document wordt gevuld met één recordknooppunt waarin de details van afzonderlijke belastingstransacties worden weergegeven.
    - Het XML-element **Rapport\\Bericht\\Samenvatting** is zo geconfigureerd dat het uitgaande document wordt gevuld met één samenvattingsknooppunt dat de som van de belastingswaarden uit de verwerkte belastingtransacties bevat.

    ![Bericht-XML-element en geneste XML-elementen op de pagina Indelingsontwerper](./media/ER-DeferredXml-Format.png)

5. Controleer de volgende gegevens op het tabblad **Toewijzing**:

    - Het element **Rapport\\Bericht\\Koptekst** hoeft niet aan een gegevensbron te zijn gekoppeld om één knooppunt in een uitgaand document te genereren.
    - Het kenmerk **ExecutionDateTime** genereert de datum en tijd (inclusief milliseconden) wanneer het koptekstknooppunt wordt toegevoegd.
    - Het element **Rapport\\Bericht\\Record** is gebonden aan de lijst **model.Gegevens.Lijst** om één recordknooppunt te genereren voor elke record in de gebonden lijst.
    - Het kenmerk **TaxAmount** is aan **model.Gegevens.Lijst.Waarde** gekoppeld (wordt weergegeven als **\@.Waarde** in de relatieve padweergave) om de belastingswaarde van de huidige belastingstransactie te genereren.
    - Het kenmerk **RunningTotal** is een tijdelijke aanduiding voor het lopende totaal van de belastingswaarden. Dit kenmerk heeft momenteel geen uitvoer, omdat er geen binding of standaardwaarde voor is geconfigureerd.
    - Het kenmerk **ExecutionDateTime** genereert de datum en tijd (inclusief milliseconden) wanneer de huidige transactie in dit rapport wordt verwerkt.
    - Het element **Rapport\\Bericht\\Samenvatting** hoeft niet aan een gegevensbron te zijn gekoppeld om één knooppunt in een uitgaand document te genereren.
    - Het kenmerk **TotalTaxAmount** is aan **model.Gegevens.Samenvatting.Totaal** gebonden om de som van de belastingswaarden van de verwerkte belastingstransacties te genereren.
    - Het kenmerk **ExecutionDateTime** genereert de datum en tijd (inclusief milliseconden) wanneer het samenvattingsknooppunt wordt toegevoegd.

    ![Tabblad Toewijzing op de pagina Indelingsontwerper](./media/ER-DeferredXml-Format2.png)

### <a name="run-the-imported-format"></a>De geïmporteerde indeling uitvoeren

1. Selecteer **Uitvoeren** op de pagina **Indelingsontwerper**.
2. Download het bestand dat door de webbrowser wordt aangeboden en open het bestand ter controle.

    ![Gedownload bestand](./media/ER-DeferredXml-Run.png)

U ziet dat het samenvattingsknooppunt de som van de belastingswaarden voor de verwerkte transacties weergeeft. Omdat de indeling is geconfigureerd voor het gebruik van de binding **model.Gegevens.Samenvatting.Totaal** om dit totaal te retourneren, wordt de som berekend door de **TotalSum**-aggregatie van de gegevensbron **Gegroepeerd** van het type *GroupBy* aan te roepen in de modeltoewijzing. Voor het berekenen van deze aggregatie doorloopt de modeltoewijzing bij herhaling alle transacties die in gegevensbron **Gefilterd** zijn geselecteerd. Door de uitvoeringstijden van het samenvattingsknooppunt en het laatste recordknooppunt te vergelijken kunt u vaststellen dat de berekening van de som 12 milliseconden (ms) duurde. Door de uitvoeringstijden van de het eerste en het laatste recordknooppunt te vergelijken kunt u vaststellen dat het genereren van alle recordknooppunten 9 milliseconden (ms) duurde. Daarom was er in totaal 21 ms nodig.

### <a name="modify-the-format-so-that-the-calculation-is-based-on-generated-output"></a>De indeling wijzigen zodat de berekening wordt gebaseerd op gegenereerde uitvoer

Als het volume van transacties veel groter is dan het volume in het huidige voorbeeld, kan de berekeningstijd toenemen en resulteren in prestatieproblemen. Door de instelling van de indeling te wijzigen kunt u deze prestatieproblemen voorkomen. Aangezien u toegang tot belastingswaarden hebt om deze op te nemen in het gegenereerde rapport, kunt u deze informatie opnieuw gebruiken om belastingswaarden te berekenen. Zie [Indeling configureren voor tellen en totaliseren](./tasks/er-format-counting-summing-1.md) voor meer informatie.

1. Selecteer op de pagina **Indelingsontwerper** op het tabblad **Indeling** het bestandselement **Rapport** in de indelingsstructuur.
2. Stel de optie **Uitvoerdetails verzamelen** in op **Ja**. U kunt deze indeling nu configureren door de inhoud van een gegenereerd rapport te gebruiken als gegevensbron die toegankelijk is via de ingebouwde ER-functies in de categorie [Gegevensverzameling](er-functions-category-data-collection.md).
3. Selecteer op het tabblad **Toewijzing** het XML-element **Rapport\\Bericht\\Record**.
4. Configureer de expressie **Sleutelnaam verzamelde gegevens** als `WsColumn`.
5. Configureer de expressie **Sleutelwaarde verzamelde gegevens** als `WsRow`.

    ![Record-XML-element op de pagina Indelingsontwerper](./media/ER-DeferredXml-Format3.png)

6. Selecteer het kenmerk **Rapport\\Bericht\\Record\\TaxAmount**.
7. Configureer de expressie **Sleutelnaam verzamelde gegevens** als `SummingAmountKey`.

    ![Kenmerk TaxAmount op de pagina Indelingsontwerper](./media/ER-DeferredXml-Format4.png)

    U kunt deze instelling beschouwen als de afhandeling van een virtueel werk blad, waarbij de waarde van cel A1 wordt toegevoegd met de waarde van het belastingsbedrag uit elke verwerkte belastingstransactie.

8. Selecteer het kenmerk **Rapport\\Bericht\\Record\\RunningTotal** en selecteer vervolgens **Formule bewerken**.
9. Configureer de `SUMIF(SummingAmountKey, WsColumn, WsRow)`-expressie met behulp van de ingebouwde ER-functie [SUMIF](er-functions-datacollection-sumif.md) en selecteer vervolgens **Opslaan**.

    ![Expressie SUMIF](./media/ER-DeferredXml-FormulaDesigner.png)

10. Sluit de pagina **Formuleontwerper**.
11. Selecteer **Opslaan** en vervolgens **Uitvoeren**.
12. Download en controleer het bestand dat door de webbrowser wordt aangeboden.

    ![Gedownload bestand](./media/ER-DeferredXml-Run1.png)

    Het laatste recordknooppunt bevat het lopende totaal van belastingswaarden die voor alle verwerkte transacties worden berekend door de gegenereerde uitvoer als gegevensbron te gebruiken. Deze gegevensbron begint aan het begin van het rapport en gaat door tot met de laatste belastingstransactie. Het samenvattingsknooppunt bevat de som van de belastingswaarden voor alle verwerkte transacties die worden berekend in de modeltoewijzing met behulp van de gegevensbron van het type *GroupBy*. U ziet dat deze waarden gelijk zijn. Daarom kan de op uitvoer gebaseerde optelling worden gebruikt in plaats van **GroupBy**. Door de uitvoeringstijden van de het eerste recordknooppunt en het samenvattingsknooppunt te vergelijken kunt u vaststellen dat het genereren van alle recordknooppunten en het totaliseren 11 milliseconden (ms) duurde. Daarom is de aangepaste indeling ongeveer twee keer sneller dan de oorspronkelijke indeling voor wat betreft het genereren van recordknooppunten en het totaliseren van belastingswaarden.

13. Selecteer het kenmerk **Rapport\\Bericht\\Samenvatting\\TotalTaxAmount** en selecteer vervolgens **Formule bewerken**.
14. Voer de `SUMIF(SummingAmountKey, WsColumn, WsRow)`-expressie in plaats van de bestaande expressie in.
15. Selecteer **Opslaan** en vervolgens **Uitvoeren**.
16. Download en controleer het bestand dat door de webbrowser wordt aangeboden.

    ![Gedownload bestand](./media/ER-DeferredXml-Run2.png)

    Zoals u ziet, is het lopende totaal van de belastingswaarden in het laatste recordknooppunt gelijk aan de som in het samenvattingsknooppunt.

### <a name="put-values-of-output-based-summing-in-the-report-header"></a>Waarden van op uitvoer gebaseerde totalisatie in de rapportkoptekst plaatsen

Als u bijvoorbeeld de som van de belastingswaarden in de koptekst van uw rapport moet presenteren, kunt u de indeling wijzigen.

1. Selecteer op de pagina **Indelingsontwerper** op het tabblad **Indeling** het XML-element **Rapport\\Bericht\\Samenvatting**.
2. Selecteer **Omhoog verplaatsen**.
3. Selecteer **Opslaan** en vervolgens **Uitvoeren**.
4. Download en controleer het bestand dat door de webbrowser wordt aangeboden.

    ![Gedownload bestand](./media/ER-DeferredXml-Run3.png)

    De som van de belastingswaarden in het samenvattingsknooppunt is nu gelijk aan 0 (nul), omdat dit totaal nu wordt berekend op basis van de gegenereerde uitvoer. Wanneer het eerste recordknooppunt wordt gegenereerd, bevat de gegenereerde uitvoer nog geen recordknooppunten met transactiedetails. U kunt deze indeling zo configureren dat de uitvoering van het reekselement **Rapport\\Bericht\\Samenvatting** wordt uitgevoerd totdat het element **Rapport\\Bericht\\Record** voor alle belastingstransacties is uitgevoerd.

### <a name="defer-the-execution-of-the-summary-xml-element-so-that-the-calculated-total-is-used"></a>De uitvoering van het samenvattings-XML-element uitstellen zodat het berekende totaal wordt gebruikt

1. Selecteer op de pagina **Indelingsontwerper** op het tabblad **Indeling** het XML-element **Rapport\\Bericht\\Samenvatting**.
2. Stel de optie **Uitgestelde uitvoering** in op **Ja**.

    ![Optie Uitgestelde uitvoering van het samenvattings-XML-element op de pagina Indelingsontwerper](./media/ER-DeferredXml-Format5.png)

3. Selecteer **Opslaan** en vervolgens **Uitvoeren**.
4. Download en controleer het bestand dat door de webbrowser wordt aangeboden.

    ![Gedownload bestand](./media/ER-DeferredXml-Run4.png)

    Het element **Rapport\\Bericht\\Overzicht** wordt nu alleen uitgevoerd nadat alle andere artikelen die zijn genest onder het bovenliggend element, **Rapport\\Bericht**, zijn uitgevoerd. Daarom wordt het uitgevoerd nadat het reekselement **Rapport\\Bericht\\Record** is uitgevoerd voor alle belastingstransacties van de gegevensbron **model.Gegevens.Lijst**. De uitvoeringstijden van het eerste en laatste recordknooppunt en van het koptekst- en samenvattingsknooppunt onthullen dit feit.

## <a name="additional-resources"></a>Aanvullende resources

- [Indeling configureren voor tellen en totaliseren](./tasks/er-format-counting-summing-1.md)
- [Uitvoering van ER-indeling traceren om prestatieproblemen op te lossen](trace-execution-er-troubleshoot-perf.md)
- [De uitvoering van reekselementen in ER-indelingen uitstellen](er-defer-sequence-element.md#Example)
