---
title: JOIN-gegevensbronnen gebruiken in ER-modeltoewijzingen om gegevens uit meerdere toepassingstabellen op te halen
description: In dit onderwerp wordt uitgelegd hoe u gegevensbronnen van het type JOIN kunt gebruiken in elektronische rapportage (ER).
author: NickSelin
manager: AnnBe
ms.date: 10/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERModelMappingDesigner, EROperationDesigner
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-03-01
ms.dyn365.ops.version: Release 10.0.1
ms.openlocfilehash: 224acc19ee5dda430cd9471aa50e9d870a4f8c60
ms.sourcegitcommit: 564aa8eec89defdbe2abaf38d0ebc4cca3e28109
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/28/2019
ms.locfileid: "2667949"
---
# <a name="use-join-data-sources-to-get-data-from-multiple-application-tables-in-electronic-reporting-er-model-mappings"></a>JOIN-gegevensbronnen gebruiken om gegevens uit meerdere toepassingstabellen op te halen in ER-modeltoewijzingen (elektronische rapportage)

[!include[banner](../includes/banner.md)]

Tijdens het configureren van ER-modeltoewijzingen of -indelingen (elektronische rapportage) kunt u vereiste gegevensbronnen van het type **Join** [toevoegen](#review). Tijdens de ontwerpfase wordt een **Join**-gegevensbron geconfigureerd als een set van verschillende gegevensbronnen die elk een lijst met records als resultaat geven. Voor elke gegevensbron, met uitzondering van de eerste, moet u de noodzakelijke voorwaarden definiëren om records van de huidige en eerdere gegevensbronnen samen te voegen. Tijdens runtime [retourneert](#executeERformat) een geconfigureerde gegevensbron van het type **Join** een enkele gekoppelde lijst met records die velden bevatten uit de records van geneste gegevensbronnen.

Momenteel worden de volgende typen joins ondersteund:

- Outer (linker) join:
    - Hierbij worden alle records van de eerste (meest linkse) gegevensbron samengevoegd gevolgd door eventuele overeenkomsten op basis van geconfigureerde voorwaardenrecords van de tweede (meest rechtse) gegevensbron.
- Inner (rechter) join:
    - Hierbij worden alleen records van de eerste (meest linkse) gegevensbron samengevoegd en alleen records van de tweede (meest rechtse) gegevens die overeenkomen op basis van geconfigureerde voorwaarden.

Wanneer in de geconfigureerde **Join**-gegevensbron alle gegevensbronnen van het type **Tabelrecords** zijn, kan de uitvoering van de Join-gegevensbron worden [uitgevoerd op databaseniveau](#analyze) via een enkele SQL-instructie. Hierdoor wordt het aantal databaseaanroepen verminderd, waardoor de prestaties van de modeltoewijzing verbeteren. Anders wordt de uitvoering de **Join**-gegevensbron in het geheugen uitgevoerd.

> [!NOTE]
> Het gebruik van de functie **VALUEIN** in ER-expressies die voorwaarden specificeren voor het samenvoegen van records in gegevensbronnen van het type Join wordt nog niet ondersteund. Bezoek de pagina [Formuleontwerper in elektronische rapportage](general-electronic-reporting-formula-designer.md) voor meer informatie.

Voor meer informatie over deze functie kunt u het voorbeeld in dit onderwerp uitvoeren.

## <a name="example-use-join-data-sources-in-er-model-mappings"></a>Voorbeeld: JOIN-gegevensbronnen gebruiken in ER-modeltoewijzingen

In de volgende stappen wordt uitgelegd hoe de systeembeheerder of de ontwikkelaar van elektronische rapportage een ER-modeltoewijzing (elektronische rapportage) kan configureren om gegevens uit meerdere toepassingstabellen tegelijk op te halen door gegevensbronnen van het type **Join** te gebruiken om de gegevenstoegang te verbeteren. Deze stappen kunnen worden uitgevoerd voor elk bedrijf van Dynamics 365 Finance of in Regulatory Configuration Services (RCS).

### <a name="prerequisites"></a>Vereisten

Als u de voorbeelden in dit onderwerp wilt voltooien, moet u toegang hebben tot een van de volgende services, afhankelijk van de service die wordt gebruikt om deze stappen uit te voeren:

**Toegang tot Financiën voor een van de volgende rollen:**

- Ontwikkelaar elektronische rapportage
- Functioneel consultant elektronische rapportage
- Systeembeheerder

**Toegang tot RCS voor een van de volgende rollen:**

- Ontwikkelaar elektronische rapportage
- Functioneel consultant elektronische rapportage
- Systeembeheerder

U moet ook eerst de stappen in de procedure [Een configuratieprovider maken en deze als actief markeren](tasks/er-configuration-provider-mark-it-active-2016-11.md) voltooien.

U moet echter ook downloaden vanuit het [Microsoft Downloadcentrum](https://go.microsoft.com/fwlink/?linkid=000000) en lokaal de volgende voorbeeldconfiguratiebestanden voor ER opslaan:

| **Omschrijving inhoud**  | **Bestandsnaam**   |
|--------------------------|-----------------|
| Voorbeeld van configuratiebestand voor **ER-gegevensmodel**, dat wordt gebruikt als de gegevensbron voor de voorbeelden.| [Model voor het leren van JOIN-gegevensbronnen.versie.1.1.xml](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |
| Voorbeeld van configuratiebestand voor **ER-modeltoewijzing**, dat het ER-gegevensmodel implementeert voor de voorbeelden. | [Toewijzing voor het leren van JOIN-gegevensbronnen.versie.1.1.xml](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |
| Voorbeeld van configuratiebestand van **ER-indeling**. In dit bestand worden de gegevens beschreven om het onderdeel van de ER-indeling te vullen voor de voorbeelden. | [Indeling voor het leren van JOIN-gegevensbronnen.versie.1.1.xml](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |

### <a name="activate-a-configurations-provider"></a>Een configuratieprovider activeren

1. Open Finance of RCS in de eerste sessie van uw webbrowser.
2. Ga naar **Organisatiebeheer \> Werkgebieden \> Elektronische rapportage**.
3. Controleer op de pagina **Lokalisatieconfiguraties** in de sectie **Configuratieproviders** of de configuratieprovider voor het voorbeeldbedrijf Litware, Inc. (http://www.litware.com) wordt vermeld en of het is gemarkeerd als **Actief**. Als u deze configuratieprovider niet ziet, voltooit u de stappen in de procedure [Een configuratieprovider maken en deze als actief markeren](tasks/er-configuration-provider-mark-it-active-2016-11.md).

    ![Werkgebied voor elektronische rapportage](./media/GER-JoinDS-ActiveProvider.PNG)

### <a name="import-sample-er-configuration-files"></a>Voorbeeld van ER-configuratiebestanden importeren

1. Selecteer **Rapportageconfiguraties**.
2. Importeer het configuratiebestand voor het ER-gegevensmodel.
    1. Selecteer **Uitwisselen**.
    2. Selecteer **Laden uit XML-bestand**.
    3. Selecteer **bladeren** om het bestand **Model voor het leren van JOIN-gegevensbronnen.versie.1.1.xml** te zoeken.
    4. Selecteer **OK**.
3. Importeer het configuratiebestand voor de ER-modeltoewijzing.
    1. Selecteer **Uitwisselen**.
    2. Selecteer **Laden uit XML-bestand**.
    3. Selecteer **bladeren** om het bestand **Toewijzing voor het leren van JOIN-gegevensbronnen.versie.1.1.xml** te zoeken.
    4. Selecteer **OK**.
4.  Importeer het configuratiebestand voor ER-indeling.
    1. Selecteer **Uitwisselen**.
    2. Selecteer **Laden uit XML-bestand**.
    3. Selecteer **bladeren** om het bestand **Indeling voor het leren van JOIN-gegevensbronnen.versie.1.1.xml** te zoeken.
    4. Selecteer **OK**.
5.  Vouw in de configuratiestructuur het item **Model voor het leren van JOIN-gegevensbronnen** en andere modelitems uit (indien beschikbaar).
6.  Bekijk de lijst met ER-configuraties in de structuur en de versiegegevens op het sneltabblad **Versies**. Deze worden gebruikt als gegevensbron voor uw voorbeeldrapport.

    ![Pagina met configuraties voor elektronische rapportage](./media/GER-JoinDS-ConfigurationsTree.PNG)

### <a name="turn-on-execution-trace-options"></a>Opties voor uitvoeringstracering inschakelen
1.  Selecteer **CONFIGURATIES**.
2.  Selecteer **Gebruikersparameters**.
3.  Stel parameters voor uitvoeringstracering zoals in de onderstaande schermopname worden weergegeven.

    ![Pagina met gebruikersparameters voor elektronische rapportage](./media/GER-JoinDS-Parameters.PNG)

    Wanneer deze parameters zijn ingeschakeld, wordt voor elke uitvoering van het geïmporteerde ER-indelingsbestand de uitvoeringstracering gegenereerd. Met behulp van details van gegenereerde uitvoeringstraceringen kunt u de uitvoering van onderdelen van de ER-indeling en ER-modeltoewijzing analyseren. Ga naar de pagina [Uitvoering van ER-indeling traceren om prestatieproblemen op te lossen](trace-execution-er-troubleshoot-perf.md) voor meer informatie over de functie voor ER-uitvoeringstracering.

### <a name="review-er-model-mapping-part-1"></a>ER-modeltoewijzing controleren (deel 1)

Controleer de instellingen van het onderdeel voor ER-modeltoewijzing. Het onderdeel is geconfigureerd om toegang te krijgen tot informatie over versies van ER-configuraties, details van configuraties en configuratieproviders zonder gegevensbronnen van het type **Join** te gebruiken.

1.  Selecteer de configuratie **Toewijzing voor het leren van JOIN-gegevensbronnen**.
2.  Selecteer **Ontwerper** om de lijst met toewijzingen te openen.
3.  Selecteer **Ontwerper** om de toewijzingsdetails te controleren. 
4.  Selecteer **Details weergeven**.
5.  Vouw in de configuratiestructuur de gegevensmodelitems **Set1** en **Set1.Details** uit:

    1. Binding **Details: Record list = Versions** geeft aan dat het item **Set1.Details** is gebonden aan de gegevensbron **Versions** die records uit de tabel **ERSolutionVersionTable** retourneert. Elke record van deze tabel vertegenwoordigt een enkele versie van een ER-configuratie. De inhoud van deze tabel wordt weergegeven op het sneltabblad **Versies** op de pagina **Configuraties**.
    2. Binding **ConfigurationVersion: String = @.PublicVersionNumber** houdt in dat de waarde van de openbare versie van elke versie van de ER-configuratie wordt opgehaald uit het veld **PublicVersionNumber** van de tabel **ERSolutionVersionTable** en in het item **ConfigurationVersion** geplaatst.
    3. Binding **ConfigurationTitle: String = @.'>Relations'.Solution.Name** geeft aan dat de naam van een ER-configuratie wordt opgehaald uit het veld **Naam** van de tabel **ERSolutionTable** met beoordeling van de veel-op-één-relatie (**'Relations'**) tussen de tabellen **ERSolutionVersionTable** en **ERSolutionTable**. Namen van de ER-configuraties van het huidige toepassingsexemplaar worden weergegeven in de configuratiestructuur op de pagina **Configuraties**.
    4. Binding **@.'>Relations'.Solution.'>Relations'.SolutionVendor.Name** geeft aan dat de naam van de configuratieprovider die eigenaar is van de huidige configuratie wordt opgehaald uit het veld **Naam** van de tabel **ERVendorTable** met beoordeling van de veel-op-één-relatie tussen de tabellen **ERSolutionTable** en **ERVendorTable**. Namen van de ER-configuratieproviders worden weergegeven in de configuratiestructuur op de pagina **Configuraties** in de paginakoptekst voor elke configuratie. De volledige lijst van ER-configuratieproviders is te vinden op de tabelpagina **Organisatiebeheer \> Elektronische rapportage \> Configuratieprovider**.

    ![Pagina voor ontwerper van ER-modeltoewijzingen](./media/GER-JoinDS-Set1Review.PNG)

6.  Vouw in de configuratiestructuur het gegevensmodelitem **Set1.Summary** uit:

    1. Binding **VersionsNumber: Integer = VersionsSummary.aggregated.VersionsNumber** geeft aan dat het item **Set1.Summary.VersionsNumber** is gebonden aan het aggregatieveld **VersionsNumber** van de gegevensbron **VersionsSummary** van het type **GroupBy** dat is geconfigureerd om het aantal records van de tabel **ERSolutionVersionTable** te retourneren via de gegevensbron **Versions**.

    ![Pagina voor parameters van GROUPBY-gegevensbron](./media/GER-JoinDS-Set1GroupByReview.PNG)

7.  Sluit de pagina.

### <a name="review"></a> ER-modeltoewijzing controleren (deel 2)

Controleer de instellingen van het onderdeel voor ER-modeltoewijzing. Het onderdeel is geconfigureerd om toegang te krijgen tot informatie over versies van ER-configuraties, details van configuraties en configuratieproviders door een gegevensbron van het type **Join** te gebruiken.

1.  Vouw in de configuratiestructuur de gegevensmodelitems **Set2** en **Set2.Details** uit. De binding **Details: Record list = Details** geeft aan dat het item **Set2.Details** is gekoppeld aan de gegevensbron **Details** die is geconfigureerd als gegevensbron van het type **Join**.

    ![Pagina voor ontwerper van ER-modeltoewijzingen](./media/GER-JoinDS-Set2Review.PNG)

    De **Join**-gegevensbron kan worden toegevoegd door de gegevensbron **Functions\Join** te selecteren:

    ![Pagina voor ontwerper van ER-modeltoewijzingen](./media/GER-JoinDS-AddJoinDS.PNG)

2.  Selecteer de gegevensbron **Details**.
3.  Selecteer **Bewerken** in het deelvenster **Gegevensbronnen**.
4.  Selecteer **Join bewerken**.
5.  Selecteer **Details weergeven**.

    ![Pagina voor parameters van JOIN-gegevensbron](./media/GER-JoinDS-JoinDSEditor.PNG)

    Deze pagina wordt gebruikt om de vereiste gegevensbron van het **Join-type** te ontwerpen. Tijdens runtime maakt deze gegevensbron een enkele gekoppelde lijst met records uit de gegevensbronnen in het raster **Gecombineerde lijst**. Het koppelen van records begint bij de gegevensbron **ConfigurationProviders** die zich als eerste in het raster bevindt (de kolom **Type** is hiervoor leeg). Records van elke andere gegevensbron worden vervolgens samengevoegd met de records van de bovenliggende gegevensbron op basis van de volgorde in dit raster. Elke gegevensbron voor samenvoegen moet worden geconfigureerd als een gegevensbron die is genest onder een doelgegevensbron (gegevensbron **1Versions** is genest onder **1Configurations**; gegevensbron **1Configurations** is genest onder **ConfigurationProviders**). Elke geconfigureerde gegevensbron moet de voorwaarden voor de join bevatten. In de gegevensbron voor deze specifieke **Join** worden de volgende joins gedefinieerd:

    - Elke record van de gegevensbron **ConfigurationProviders** (waarnaar wordt verwezen in de tabel **ERVendorTable**) wordt samengevoegd met alleen records van de gegevensbron **1Configurations** (waarnaar wordt verwezen in de tabel **ERSolutionTable**) met dezelfde waarde in de velden **SolutionVendor** en **RecId**. Het type **Inner join** wordt voor deze join en voor de volgende voorwaarden voor overeenkomende records gebruikt: 

    FILTER (Configurations, Configurations.SolutionVendor = ConfigurationProviders.RecId)

    - Elke record van de gegevensbron **1Configurations** (waarnaar wordt verwezen in de tabel **ERSolutionTable**) wordt samengevoegd met alleen records van de gegevensbron **1Versions** (waarnaar wordt verwezen in de tabel **ERSolutionVersionTable**) met dezelfde waarde in de velden **Solution** en **RecId**. Het type **Inner join** wordt voor deze join en voor de volgende voorwaarden voor overeenkomende records gebruikt:

    FILTER (ConfigurationVersions, ConfigurationVersions.Solution = ConfigurationProviders.'1Configurations'.RecId)

    - De optie **Uitvoeren** is geconfigureerd als **Query**, wat betekent dat deze join-gegevensbron tijdens runtime als een directe SQL-oproep wordt uitgevoerd op databaseniveau.

    Als u records wilt samenvoegen van gegevensbronnen die toepassingstabellen vertegenwoordigen, kunt u join-voorwaarden opgeven door andere veldenparen te gebruiken die bestaande AOT-relaties tussen deze tabellen beschrijven. Dit type join kan ook worden geconfigureerd voor uitvoering op databaseniveau.

6.  Sluit de pagina.
7.  Selecteer **Annuleren**.
8.  Vouw in de configuratiestructuur het gegevensmodelitem **Set2.Summary** uit:

    - Binding **VersionsNumber: Integer = DetailsSummary.aggregated.VersionsNumber** geeft aan dat het item **Set2.Summary.VersionsNumber** is gebonden aan het aggregatieveld **VersionsNumber** van de gegevensbron **DetailsSummary** van het type **GroupBy** dat is geconfigureerd om het aantal samengevoegde records van de gegevensbron **Details** van het type **Join** te retourneren.
    - De locatieoptie **Uitvoering** is geconfigureerd als **Query**, wat betekent dat deze **GroupBy**-gegevensbron tijdens runtime als een directe SQL-oproep wordt uitgevoerd op databaseniveau. Dit is mogelijk omdat de basisgegevensbron **Details** van het type **Join** wordt geconfigureerd als uitgevoerd op databaseniveau.

    ![Pagina voor parameters van GROUPBY-gegevensbron](./media/GER-JoinDS-Set2GroupByReview.PNG)

9.  Sluit de pagina.
10. Selecteer **Annuleren**.

### <a name="executeERformat"></a> ER-indeling uitvoeren

1.  Open Finance of RCS in de tweede sessie van uw webbrowser met dezelfde referenties en hetzelfde bedrijf als bij de eerste sessie.
2.  Ga naar **Organisatiebeheer \> Elektronische rapportage \> Configuraties**.
3.  Vouw de configuratie **Model voor het leren van JOIN-gegevensbronnen** uit.
4.  Selecteer de configuratie **Indeling voor het leren van JOIN-gegevensbronnen**.
5.  Selecteer **Ontwerper**.
6.  Selecteer **Details weergeven**.
7.  Selecteer **Toewijzing**.
8.  Selecteer **Uitvouwen/samenvouwen**.

    Deze indeling is bedoeld voor het vullen van een gegenereerd tekstbestand met een nieuwe regel voor elke versie van een ER-configuratie (**Version**-reeks). Elke gegenereerde regel bevat de naam van een configuratieprovider die eigenaar is van de huidige configuratie, de configuratienaam en de configuratieversie, gescheiden door puntkomma's. De laatste regel van het gegenereerde bestand bevat het aantal ontdekte versies van de ER-configuraties (**Summary**-reeks).

    ![Pagina voor ontwerper van ER-indeling](./media/GER-JoinDS-FormatReview.PNG)

    De gegevensbronnen **Data** en **Summary** worden gebruikt om de details van de configuratieversie in te vullen voor het gegenereerde bestand:

    - Informatie uit het **Set1**-gegevensmodel wordt gebruikt wanneer u **Nee** kiest voor de gegevensbron **Selector** tijdens runtime op de pagina met de gebruikersdialoog bij het uitvoeren van een ER-indeling.
    - Informatie uit het **Set2**-gegevensmodel wordt gebruikt wanneer u **Ja** kiest voor de gegevensbron **Selector** tijdens runtime op de pagina met de gebruikersdialoog bij het uitvoeren van een ER-indeling.

    ![Pagina voor ontwerper van ER-indeling](./media/GER-JoinDS-FormatMappingReview.PNG)

9.  Selecteer **Uitvoeren**.
10. Selecteer op de dialoogpagina de optie **Nee** in het veld **JOIN-gegevensbron gebruiken**.
11. Selecteer **OK**.
12. Gegenereerd bestand controleren

    ![Pagina met ER-gebruikersdialoog](./media/GER-JoinDS-Set1Run.PNG)

#### <a name="analyze-er-format-execution-trace"></a>Uitvoeringstracering van ER-indeling analyseren

1.  Selecteer **Ontwerper** in de eerste sessie van Finance of RCS.
2.  Selecteer **Prestatietracering**.
3.  Selecteer in het raster **Prestatietracering** de bovenste record van de meest recente uitvoeringstracering van een ER-indeling die het huidige onderdeel voor modeltoewijzing heeft gebruikt.
4.  Selecteer **OK**.

    In de uitvoeringsstatistieken wordt u op de hoogte gesteld van dubbele aanroepen van toepassingstabellen:

    - **ERSolutionTable** is zo vaak aangeroepen als u configuratieversierecords hebt in de tabel **ERSolutionVersionTable**, terwijl het aantal van dergelijke aanroepen op bepaalde momenten kan worden teruggebracht voor prestatieverbetering.
    - **ERVendorTable** is tweemaal aangeroepen voor elke configuratieversierecords die is gedetecteerd in de tabel **ERSolutionVersionTable**, terwijl het aantal van dergelijke aanroepen eveneens kan worden teruggebracht.

    ![Pagina voor ontwerper van ER-modeltoewijzingen](./media/GER-JoinDS-Set1Run2.PNG)

5.  Sluit de pagina.

### <a name="execute-er-format"></a>ER-indeling uitvoeren

1.  Ga naar het tabblad in uw webbrowser met de tweede sessie van Finance of RCS.
2.  Selecteer **Uitvoeren**.
3.  Selecteer op de dialoogpagina de optie **Ja** in het veld **JOIN-gegevensbron gebruiken**.
4.  Selecteer **OK**.
5.  Gegenereerd bestand controleren

    ![Pagina met ER-gebruikersdialoog](./media/GER-JoinDS-Set2Run.PNG)

#### <a name="analyze"></a> Uitvoeringstracering van ER-indeling analyseren

1.  Selecteer **Ontwerper** in de eerste sessie van Finance of RCS.
2.  Selecteer **Prestatietracering**.
3.  Selecteer in het raster **Prestatietracering** de bovenste record die de meest recente uitvoeringstracering van een ER-indeling aangeeft die het huidige onderdeel voor modeltoewijzing heeft gebruikt.
4.  Selecteer **OK**.

    In de uitvoeringsstatistieken wordt het volgende aangegeven:

    - De toepassingsdatabase is eenmaal aangeroepen om records op te halen uit de tabellen **ERVendorTable**, **ERSolutionTable** en **ERSolutionVersionTable** om toegang te krijgen tot vereiste velden.

    ![Pagina voor ontwerper van ER-modeltoewijzingen](./media/GER-JoinDS-Set2Run2.PNG)

    - De toepassingsdatabase wordt eenmaal aangeroepen om het aantal configuratieversies te berekenen met behulp van joins die zijn geconfigureerd in de gegevensbron **Details**.

    ![Pagina voor ontwerper van ER-modeltoewijzingen](./media/GER-JoinDS-Set2Run3.PNG)

## <a name="additional-resources"></a>Aanvullende resources

[Formuleontwerper in elektronische aangifte](general-electronic-reporting-formula-designer.md)

[Uitvoering van ER-indeling traceren om prestatieproblemen op te lossen](trace-execution-er-troubleshoot-perf.md)

