---
title: De uitvoering van ER-indelingen traceren om prestatieproblemen op te lossen
description: Dit artikel bevat informatie over het gebruik van de functie voor prestatietracering in Elektronische rapportage (ER) om prestatieproblemen op te lossen.
author: kfend
ms.date: 06/22/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.1
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.openlocfilehash: 9f088228b140a42ee097c9e810166550ab0fae81
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/12/2022
ms.locfileid: "9289939"
---
# <a name="trace-the-execution-of-er-formats-to-troubleshoot-performance-issues"></a>De uitvoering van ER-indelingen traceren om prestatieproblemen op te lossen

[!include[banner](../includes/banner.md)]

Als onderdeel van het proces van het ontwerpen van configuraties voor Elektronische rapportage om elektronische documenten te genereren, definieert u de methode die wordt gebruikt om gegevens uit de toepassing te halen en deze in te voeren in de gegenereerde uitvoer. Met de functie voor ER-prestatietracering kunt u aanzienlijk besparen op de tijd en kosten van het verzamelen van gegevens over de uitvoering van ER-indelingen zodat u deze kunt investeren in het oplossen van prestatieproblemen. In deze zelfstudie vindt u richtlijnen voor het traceren van prestaties voor uitgevoerde ER-indelingen. Daarnaast wordt aangegeven hoe u de informatie uit deze traceringen gebruikt om de prestaties te verbeteren.

## <a name="prerequisites"></a>Vereisten

Om de voorbeelden in deze zelfstudie te kunnen voltooien, moet u toegang tot het volgende hebben:

- Toegang tot een van de volgende rollen:

    - Ontwikkelaar elektronische rapportage
    - Functioneel consultant elektronische rapportage
    - Systeembeheerder

- Toegang tot het exemplaar van Regulatory Configuration Services (RCS) dat is ingericht voor dezelfde tenant als de toepassing, voor een van de volgende rollen:

    - Ontwikkelaar elektronische rapportage
    - Functioneel consultant elektronische rapportage
    - Systeembeheerder

U moet ook de volgende bestanden downloaden en lokaal opslaan.

| Bestand                                  | Inhoud                               |
|---------------------------------------|---------------------------------------|
| Versie 1 prestatietraceringsmodel     | [Voorbeeldconfiguratie van model voor ER-gegevens](https://download.microsoft.com/download/0/a/a/0aa84e48-8040-4c46-b542-e3bf15c9b2ad/Performancetracemodelversion.1.xml)    |
| Versie 1 metagegevens voor prestatietracering  | [Voorbeeldconfiguratie van ER-metagegevens](https://download.microsoft.com/download/a/9/3/a937e8c4-1f8a-43e4-83ee-7d599cf7d983/Performancetracemetadataversion.1.xml)      |
| Versie 1.1 Toewijzing voor prestatietracering | [Voorbeeldconfiguratie van ER-modeltoewijzing](https://download.microsoft.com/download/7/7/3/77379bdc-7b22-4cfc-9b64-a9147599f931/Performancetracemappingversion1.1.xml) |
| Versie 1.1 Indeling voor prestatietracering  | [Voorbeeldconfiguratie van ER-indeling](https://download.microsoft.com/download/8/6/8/868ba581-5a06-459e-b173-fb00f038b37f/Performancetraceformatversion1.1.xml)       |

### <a name="configure-er-parameters"></a>ER-parameters configureren

Elke ER-prestatietracering die wordt gegenereerd in de toepassing, wordt opgeslagen als een bijlage van de uitvoeringslogboekrecord. Het Raamwerk voor documentbeheer (DM) wordt gebruikt om deze bijlagen te beheren. U moet ER-parameters vooraf configureren om het documenttype voor documentbeheer op te geven dat moet worden gebruikt voor het bijvoegen van prestatietraceringen. Selecteer in de werkruimte **Elektronische rapportage** **Parameters van elektronische rapportage**. Selecteer vervolgens op de pagina **Parameters van elektronische rapportage** op het tabblad **Bijlagen** in het veld **Andere** het documenttype voor documentbeheer dat voor prestatietraceringen moet worden gebruikt.

![Pagina Parameters van elektronische rapportage.](./media/GER-PerfTrace-GER-Parameters-DocumentType.png)

Om beschikbaar te zijn in het opzoekveld **Andere** moet een documenttype voor documentbeheer op de volgende manier worden geconfigureerd op de pagina **Documenttypen** (**Organisatiebeheer \> Documentbeheer \> Documenttypen**):

- **Klasse:** Bestand koppelen
- **Groep:** Bestand

![Pagina Documenttypen.](./media/GER-PerfTrace-DM-DocumentType.png)

> [!NOTE]
> Het geselecteerde documenttype moet beschikbaar zijn in elk bedrijf van het huidige exemplaar omdat bijlagen voor documentbeheer bedrijfsspecifiek zijn.

### <a name="configure-rcs-parameters"></a>RCS-parameters configureren

ER-prestatietraceringen die zijn gegenereerd, worden geïmporteerd in RCS voor analyse met behulp van de ER-indelingsontwerper en de ER-toewijzingsontwerper. Omdat ER-prestatietraceringen worden opgeslagen als bijlagen van de uitvoeringslogboekrecord die is gerelateerd aan de ER-indeling, moet u RCS-parameters vooraf configureren om het documenttype voor documentbeheer op te geven dat moet worden gebruikt voor het koppelen van prestatietraceringen. In het exemplaar van RCS dat is ingericht voor uw bedrijf selecteert u in de werkruimte **Elektronische rapportage** de optie **Parameters van elektronische rapportage**. Selecteer vervolgens op de pagina **Parameters van elektronische rapportage** op het tabblad **Bijlagen** in het veld **Andere** het documenttype voor documentbeheer dat voor prestatietraceringen moet worden gebruikt.

![Pagina Parameters van elektronische rapportage in RCS.](./media/GER-PerfTrace-RCS-Parameters-DocumentType.png)

Om beschikbaar te zijn in het opzoekveld **Andere** moet een documenttype voor documentbeheer op de volgende manier worden geconfigureerd op de pagina **Documenttypen** (**Organisatiebeheer \> Documentbeheer \> Documenttypen**):

- **Klasse:** Bestand koppelen
- **Groep:** Bestand

## <a name="design-an-er-solution"></a>Een ER-oplossing ontwerpen

Stel dat u bent begonnen met het ontwerpen van een nieuwe ER-oplossing om een nieuw rapport te genereren waarin leverancierstransacties worden gepresenteerd. Op dit moment kunt u de transacties voor een geselecteerde leverancier vinden op de pagina **Leveranciertransacties** (ga naar **Leveranciers \> Leveranciers \> Alle leveranciers**, selecteer een leverancier en selecteer in het actievenster op het tabblad **Leverancier** in de groep **Transacties** de optie **Transacties**). U wilt echter alle leverancierstransacties tegelijk in één elektronisch document in XML-indeling hebben. Deze oplossing bestaat uit verschillende ER-configuraties met het vereiste gegevensmodel en de vereiste metagegevens, modeltoewijzing en indelingscomponenten.

1. Meld u aan bij het exemplaar van RCS dat is ingericht voor uw bedrijf.
2. In deze zelfstudie maakt en wijzigt u configuraties voor het voorbeeldbedrijf **Litware, Inc.** Zorg er daarom voor dat deze configuratieprovider is toegevoegd aan RCS en als actief is geselecteerd. Zie de procedure [Aanbieders van configuraties maken en deze als actief markeren](tasks/er-configuration-provider-mark-it-active-2016-11.md) voor instructies.
3. Selecteer in het werkgebied **Elektronische rapportage** de tegel **Rapportconfiguraties**.
4. Importeer op de pagina **Configuraties** de ER-configuraties die u als vereiste hebt gedownload in RCS, in de volgende volgorde: gegevensmodel, metagegevens, modeltoewijzing, indeling. Volg deze stappen voor elke configuratie:

    1. In het actievenster selecteert u **Uitwisselen \> Laden uit XML-bestand**.
    2. Selecteer **Bladeren** om het juiste bestand voor de vereiste ER-configuratie in XML-indeling te selecteren.
    3. Selecteer **OK**.

    ![Pagina Configuraties in RCS.](./media/GER-PerfTrace-RCS-ImportedConfigurations.png)

## <a name="run-the-er-solution-to-trace-execution"></a>De ER-oplossing uitvoeren om de uitvoering te traceren

Stel dat u klaar bent met het ontwerpen van de eerste versie van de ER-oplossing. U moet deze nu testen in uw exemplaar en de uitvoeringsprestaties analyseren.

### <a name="import-an-er-configuration-from-rcs-into-finance-and-operations"></a><a id='import-configuration'></a>Een ER-configuratie uit RCS importeren naar apps voor financiën en bedrijfsactiviteiten

1. Meld u aan bij uw exemplaat van de toepassing.
2. Voor deze zelfstudie importeert u configuraties vanuit uw RCS-exemplaar (waarin u de ER-onderdelen ontwerpt) in uw exemplaar (waar u ze test en uiteindelijk gebruikt). Daarom moet u ervoor zorgen dat alle vereiste artefacten zijn voorbereid. Zie voor meer instructies de procedure [Configuraties voor Elektronische rapportage (ER) importeren uit Regulatory Configuration Services (RCS)](rcs-download-configurations.md).
3. Voer de volgende stappen uit om de configuraties uit RCS in de toepassing te importeren:

    1. Selecteer in het werkgebied **Elektronische rapportage** op de tegel voor de configuratieprovider **Litware, Inc.** de optie **Opslagplaatsen**.
    2. Selecteer in het raster op de pagina **Opslagplaats van configuraties** de opslagplaats van het type **RCS** en selecteer vervolgens **Openen**.
    3. Selecteer op het sneltabblad **Configuraties** de configuratie **Indeling voor prestatietracering**.
    4. Selecteer op het sneltabblad **Versies** versie **1.1** van de geselecteerde configuratie en selecteer vervolgens **Importeren**.

    ![Configuratie archiefpagina.](./media/GER-PerfTrace-GER-ImportedConfigurations.png)

De bijbehorende versies van de gegevensmodel- en modeltoewijzingsconfiguraties worden automatisch geïmporteerd als vereisten voor de geïmporteerde ER-indelingsconfiguratie.

### <a name="turn-on-the-er-performance-trace"></a>De ER-prestatietracering inschakelen

1. Ga naar **Organisatiebeheer \> Elektronische rapportage \> Configuraties**.
2. Selecteer op de pagina **Configuraties** in het actievenster op het tabblad **Configuraties** in de groep **Geavanceerde instellingen** de optie **Gebruikersparameters**.
3. Voer de volgende stappen uit in de sectie **Uitvoeringstracering** van het dialoogvenster **Gebruikersparameters**:

    1. In het veld **Indeling van uitvoeringstracering** geeft u de indeling op van de gegenereerde prestatietracering waarin de uitvoeringsdetails moeten worden opgeslagen voor de ER-indelingselementen en ER-toewijzingselementen:

        - **Traceringsindeling voor foutopsporing**: selecteer deze waarde als u van plan bent om een ER-indeling met een korte uitvoeringstijd interactief uit te voeren. Het verzamelen van details over de uitvoering van ER-indeling wordt vervolgens gestart. Wanneer deze waarde wordt geselecteerd, verzamelt de prestatietracering informatie over de tijd die wordt besteed aan de volgende acties:

            - Het uitvoeren van elke gegevensbron in de modeltoewijzing die wordt aangeroepen om gegevens op te halen
            - Het verwerken van elk indelingsitem om gegevens in te voeren in de gegenereerde uitvoer

            Als u de waarde **Traceringsindeling voor foutopsporing** selecteert, kunt u de inhoud van de tracering in de ER Operation-ontwerper analyseren. Hier kunt u de ER-indeling of toewijzingselementen weergeven die in de tracering worden genoemd.

        - **Traceringsindeling voor samenvoeging**: selecteer deze waarde als u van plan bent om een ER-indeling met een lange uitvoeringstijd in batchmodus uit te voeren. Het verzamelen van samengevoegde details over de uitvoering van ER-indeling wordt vervolgens gestart. Wanneer deze waarde wordt geselecteerd, verzamelt de prestatietracering informatie over de tijd die wordt besteed aan de volgende acties:

            - Het uitvoeren van elke gegevensbron in de modeltoewijzing die wordt aangeroepen om gegevens op te halen
            - Elke gegevensbron uitvoeren in de indelingstoewijzing die wordt aangeroepen om gegevens op te halen
            - Het verwerken van elk indelingsitem om gegevens in te voeren in de gegenereerde uitvoer

            De waarde van de **Samengevoegde traceerindeling** is beschikbaar in Microsoft Dynamics 365 Finance versie 10.0.20 en later.

            In de ER-indelingsontwerper en ER-modeltoewijzingsontwerper kunt u de totale uitvoeringstijd voor één component weergeven. De tracering bevat bovendien details over de uitvoering, zoals het aantal uitvoeringen en de minimale en maximale tijd van één uitvoering.

            > [!NOTE]
            > Deze tracering wordt verzameld op basis van het pad van de getraceerde componenten. De statistieken zijn daarom mogelijk onjuist wanneer één bovenliggende component verschillende onbenoemde onderliggende componenten bevat of wanneer verschillende onderliggende componenten dezelfde naam hebben.

    2. Stel de volgende opties in op **Ja** om specifieke details te verzamelen over de uitvoering van de ER-modeltoewijzing en ER-indelingsonderdelen:

        - **Statistieken voor query's verzamelen**: wanneer deze optie is ingeschakeld, wordt met de prestatietracering de volgende informatie verzameld:

            - Het aantal databaseaanroepen door gegevensbronnen
            - Het aantal dubbele aanroepen naar de database
            - Details van de SQL-instructies die zijn gebruikt voor databaseaanroepen

        - **Toegang tot caching traceren**: wanneer deze optie is ingeschakeld, wordt bij de prestatietracering informatie verzameld over het cachegebruik van de ER-modeltoewijzing.
        - **Gegevenstoegang traceren**: wanneer deze optie is ingeschakeld, wordt bij de prestatietracering informatie verzameld over het aantal aanroepen naar de database voor uitgevoerde gegevensbronnen van het recordlijsttype.
        - **Opsomming traceringslijst**: wanneer deze optie is ingeschakeld, wordt bij de prestatietracering informatie verzameld over het aantal records dat is aangevraagd vanuit gegevensbronnen van het recordlijsttype.

    > [!NOTE]
    > De parameters in het dialoogvenster **Gebruikersparameters** zijn specifiek voor de gebruiker en het huidige bedrijf.

    ![Dialoogvenster voor gebruikersparameters.](./media/GER-PerfTrace-GER-UserParameters.png)

### <a name="run-the-er-format"></a><a id='run-format'></a>De ER-indeling uitvoeren

1. Selecteer het bedrijf **DEMF**.
2. Ga naar **Organisatiebeheer \> Elektronische rapportage \> Configuraties**.
3. Selecteer op de pagina **Configuraties** in de configuratiestructuur het item **Indeling voor prestatietracering**.
4. Selecteer **Uitvoeren** in het actievenster.

Het bestand dat wordt gegenereerd, bevat informatie over 265 transacties voor zes leveranciers.

## <a name="review-the-execution-trace"></a>De uitvoeringstracering controleren

### <a name="export-the-generated-trace-from-the-application"></a><a id='export-trace'></a>De gegenereerde tracering vanuit de toepassing exporteren

Prestatietraceringen worden losgekoppeld van de ER-bronindeling en kunnen worden geserialiseerd naar een extern zipbestand.

1. Ga naar **Organisatiebeheer \> Elektronische rapportage \> Foutopsporingslogboeken voor configuraties**.
2. Selecteer op de pagina **Uitvoeringslogboeken voor elektronische rapportage** in het linkerdeelvenster in het veld **Configuratienaam** de optie **Indeling voor prestatietracering** om de logboekrecords te vinden die zijn gegenereerd door de uitvoering van de configuratie **Indeling voor prestatietracering**.
3. Selecteer de knop **Bijlagen** (de paperclip) in de rechterbovenhoek van de pagina of druk op **Ctrl+Shift+A**.

    ![Knop Bijlagen op de pagina Elektronische uitvoeringslogboeken.](./media/GER-PerfTrace-GER-DebugLog.png)

4. Op de pagina **Bijlagen voor uitvoeringslogboeken voor elektronische rapportage** selecteert u in het actievenster de optie **Openen** om de prestatietracering als een zipbestand te ontvangen en lokaal op te slaan.

    ![Bijlagen bij Elektronische uitvoeringslogboeken.](./media/GER-PerfTrace-GER-DebugLog-AttachedTrace.png)

> [!NOTE]
> De tracering die wordt gegenereerd, bevat een verwijzing naar het ER-bronrapport via een unieke rapport-id in de **GUID-indeling**. Er wordt geen rekening gehouden met de versienummers van de indeling.

De koppeling tussen de prestatietracering die is gegenereerd voor de uitgevoerde ER-indeling en de ER-modeltoewijzing is gebaseerd op de gebruikte basisdescriptor en het gemeenschappelijke gegevensmodel. Er wordt geen rekening gehouden met de versienummers van de indelings- en modeltoewijzing. Ook de instelling van de markering **Standaard voor modeltoewijzing** voor de modeltoewijzing wordt niet in overweging genomen.

### <a name="import-the-generated-trace-into-rcs"></a><a id='import-trace'></a>De gegenereerde tracering in RCS importeren

1. Selecteer in RCS in het werkgebied **Elektronische rapportage** de tegel **Rapportconfiguraties**.
2. Vouw op de pagina **Configuraties** in de configuratiestructuur het item **Prestatietraceringsmodel** uit en selecteer het item **Indeling voor prestatietracering**.
3. Selecteer **Ontwerper** in het actievenster.
4. Selecteer op de pagina **Indelingsontwerper** in het actievenster de optie **Prestatietracering**.
5. Selecteer in het dialoogvenster **Instellingen voor resultaat van prestatietracering** de optie **Prestatietracering importeren**.
6. Selecteer **Bladeren** en selecteer het zip-bestand dat u eerder hebt geëxporteerd.
7. Selecteer **OK**.

    ![Dialoogvenster Instellingen voor resultaat van prestatietracering in RCS.](./media/GER-PerfTrace-RCS-ImportedPerfTrace.png)

### <a name="use-the-performance-trace-for-analysis-in-rcs--format-execution"></a>De prestatietracering gebruiken voor analyse in RCS – Uitvoering van indeling

1. Selecteer in RCS op de pagina **Indelingsontwerper** de optie **Uitvouwen/samenvouwen** om de inhoud van alle indelingsitems uit te vouwen.

    U ziet dat voor sommige items van de huidige indeling aanvullende informatie wordt weergegeven:

    - De werkelijke tijd die is besteed aan het invoeren van gegevens in de gegenereerde uitvoer met behulp van het indelingsitem
    - Dezelfde tijd uitgedrukt als een percentage van de totale tijd die is besteed aan het genereren van de gehele uitvoer

    ![Pagina Indelingsontwerper in RCS.](./media/GER-PerfTrace-RCS-TraceInfoInFormat.png)

2. Sluit de pagina **Indelingsontwerper**.

### <a name="use-the-performance-trace-for-analysis-in-rcs--model-mapping"></a><a id='use-trace'></a>De prestatietracering gebruiken voor analyse in RCS – Modeltoewijzing

1. Selecteer in RCS op de pagina **Configuraties** in de configuratiestructuur het item **Toewijzing voor prestatietracering**.
2. Selecteer **Ontwerper** in het actievenster.
3. Selecteer **Ontwerper**.
4. Selecteer op de pagina **Ontwerper modeltoewijzing** in het actievenster de optie **Prestatietracering**.
5. Selecteer de tracering die u eerder hebt geïmporteerd.
6. Selecteer **OK**.

U ziet dat nieuwe informatie beschikbaar wordt voor bepaalde gegevensbronitems van de huidige modeltoewijzing:

- De werkelijke tijd die is besteed aan het ophalen van gegevens met behulp van de gegevensbron
- Dezelfde tijd uitgedrukt als een percentage van de totale tijd die is besteed aan het uitvoeren van de gehele modeltoewijzing

Er verschijnt een bericht met de mededeling dat de huidige modeltoewijzing databaseaanvragen dupliceert terwijl de gegevensbron VendTable/\<Relations/VendTrans.VendTable\_AccountNum wordt uitgevoerd. Deze duplicatiefout doet zich voor omdat de lijst met leveranciertransacties twee keer wordt aangeroepen voor elke herhaalde leveranciersrecord:

- Eén aanroep wordt uitgevoerd om details in te voeren van elke transactie in het gegevensmodel, op basis van de geconfigureerde bindingen.
- Eén oproep wordt uitgevoerd om het berekende aantal transacties per leverancier in het gegevensmodel in te voeren.

![Bericht over dubbele databaseaanvragen op de pagina Ontwerper modeltoewijzing in RCS.](./media/GER-PerfTrace-RCS-TraceInfoInMapping1.png)

De waarde **\[Q:530\]** geeft aan dat de VendTrans-tabel 530 keer is aangeroepen om een record uit die tabel te retourneren naar de gegevensbron VendTable/\<Relations/VendTrans.VendTable\_AccountNum. De waarde **\[530\]** geeft aan dat de gegevensbron VendTable/\<Relations/VendTrans.VendTable\_AccountNum 530 keer is aangeroepen om een record uit die gegevensbron te retourneren en de details op te geven in het gegevensmodel.

We raden u aan cache te gebruiken voor de gegevensbron VendTable/\<Relations/VendTrans.VendTable\_AccountNum om het aantal aanroepen te beperken en de details van 265 transacties te verkrijgen en de prestaties van de modeltoewijzing te verbeteren.

Het kan ook handig zijn om het aantal aanroepen naar de gegevensbron LedgerTransTypeList te beperken. Deze gegevensbron wordt gebruikt om elke waarde van de opsomming **LedgerTransType** te koppelen aan het label. Door deze gegevensbron te gebruiken, kunt u een geschikt label zoeken en in het gegevensmodel invoeren voor elke leverancierstransactie. Het huidige aantal aanroepen naar deze gegevensbron (9.027) is zeer hoog voor 265 transacties.

![De pagina Ontwerper modeltoewijzing in RCS met 9027 aanroepen naar de gegevensbron.](./media/GER-PerfTrace-RCS-TraceInfoInMapping1a.png)

## <a name="improve-the-model-mapping-based-on-information-from-the-execution-trace"></a>De modeltoewijzing verbeteren op basis van informatie uit de uitvoeringstracering

### <a name="modify-the-logic-of-the-model-mapping"></a>De logica van de modeltoewijzing wijzigen

1. Voer deze stappen uit om caching te gebruiken om dubbele aanroepen naar de database te voorkomen:

    1. In RCS selecteert u op de pagina **Ontwerper modeltoewijzing** in het deelvenster **Gegevensbronnen** het item **VendTable**.
    2. Selecteer **Cache**.
    3. Vouw het item **VendTable** uit, vouw de lijst met één-op-veel-relaties uit voor de gegevensbron VendTable(het item **\<Relaties**) en selecteer het item **VendTrans.VendTable\_AccountNum**.
    4. Selecteer **Cache**.

    ![Cache-instellingen om dubbele aanroepen te voorkomen.](./media/GER-PerfTrace-RCS-ChangeMapping-Cache.png)

2. Voer de volgende stappen uit om de gegevensbron LedgerTransTypeList in het bereik van de gegevensbron VendTable te brengen:

    1. Vouw in het deelvenster **Typen gegevensbronnen** het item **Functies** uit en selecteer het item **Berekend veld**.
    2. Selecteer in het deelvenster **Gegevensbronnen** het item **VendTable**.
    3. Selecteer **Toevoegen**.
    4. Voer in het veld **Naam** de tekst **\$TransType** in.
    5. Selecteer **Formule bewerken**.
    6. Typ in het veld **Formule** de tekst **LedgerTransTypeList**.
    7. Selecteer **Opslaan**.
    8. Sluit de pagina **Formule-editor**.
    9. Klik op **OK**.

3. Voer de volgende stappen uit om de caching van het veld **\$TransType** uit te voeren:

    1. Selecteer het item **LedgerTransTypeList**.
    2. Selecteer **Cache**.
    3. Selecteer het item **VendTable.\$TransType**.
    4. Selecteer **Cache**.

    ![Cache-instellingen voor het veld $TransType.](./media/GER-PerfTrace-RCS-ChangeMapping-Cache2.png)

4. Voer de volgende stappen uit om het veld **\$TransTypeRecord** zo te wijzigen dat het veld **\$TransType** in cache wordt gebruikt:

    1. Vouw in het deelvenster **Gegevensbronnen** de items **VendTable**, **\<Relations** en **VendTrans.VendTable\_AccountNum** uit en selecteer vervolgens het item **VendTable. VendTrans.VendTable\_AccountNum.\$TransTypeRecord**.
    2. Selecteer **Bewerken**.
    3. Selecteer **Formule bewerken**.
    4. Zoek in het veld **Formule** de volgende expressie:

        FIRSTORNULL (WHERE (LedgerTransTypeList, LedgerTransTypeList.Enum = \@.TransType))

    5. Voer in het veld **Formule** de volgende expressie in:

        FIRSTORNULL (WHERE (VendTable.'\$TransType', VendTable.'\$TransType'.Enum = \@.TransType)).

    6. Selecteer **Opslaan**.
    7. Sluit de pagina **Formule-editor**.
    8. Selecteer **OK**.

5. Selecteer **Opslaan**.
6. Sluit de pagina **Ontwerper modeltoewijzing**.
7. Sluit de pagina **Modeltoewijzingen**.

### <a name="complete-the-modified-version-of-the-er-model-mapping"></a>De gewijzigde versie van de ER-modeltoewijzing voltooien

1. In RCS selecteert u op de pagina **Configuraties** op het sneltabblad **Versies** versie **1.2** van de configuratie **Toewijzing voor prestatietracering**.
2. Selecteer **Status wijzigen**.
3. Selecteer **Voltooien**.

### <a name="import-the-modified-er-model-mapping-configuration-from-rcs-into-the-application"></a>De gewijzigde configuratie voor ER-modeltoewijzing vanuit RCS in de toepassing importeren

Herhaal de stappen uit het gedeelte [Een ER-configuratie uit RCS importeren naar apps voor financiën en bedrijfsactiviteiten](#import-configuration) eerder in dit artikel om versie 1.2 van de configuratie **Toewijzing voor prestatietracering** te importeren.

## <a name="run-the-modified-er-solution-to-trace-execution"></a>De gewijzigde ER-oplossing uitvoeren om de uitvoering te traceren

### <a name="run-the-er-format"></a>De ER-indeling uitvoeren

Herhaal de stappen uit het gedeelte [De ER-indeling uitvoeren](#run-format) eerder in dit artikel om een nieuwe prestatietracering te genereren.

## <a name="work-with-the-execution-trace"></a>Werken met de uitvoeringstracering

### <a name="export-the-generated-trace-from-the-application"></a>De gegenereerde tracering exporteren vanuit de toepassing

Herhaal de stappen uit het gedeelte [De gegenereerde tracering exporteren vanuit de toepassing](#export-trace) eerder in dit artikel om een nieuwe prestatietracering lokaal op te slaan.

### <a name="import-the-generated-trace-into-rcs"></a>De gegenereerde tracering in RCS importeren

Herhaal de stappen uit het gedeelte [De gegenereerde tracering in RCS importeren](#import-trace) eerder in dit artikel om de nieuwe prestatietracering in RCS te importeren.

### <a name="use-the-performance-trace-for-analysis-in-rcs--model-mapping"></a>De prestatietracering gebruiken voor analyse in RCS – Modeltoewijzing

Herhaal de stappen uit het gedeelte [De prestatietracering gebruiken voor analyse in RCS – Modeltoewijzing](#use-trace) eerder in dit artikel om de meest recente prestatietracering te analyseren.

Door uw aanpassingen in de modeltoewijzing worden er geen dubbele query's meer uitgevoerd in de database. Het aantal aanroepen naar databasetabellen en gegevensbronnen voor deze modeltoewijzing is ook beperkt. Hierdoor zijn de prestaties van de hele ER-oplossing verbeterd.

![Traceringsgegevens voor de gegevensbron VendTable op de pagina Ontwerper modeltoewijzing in RCS.](./media/GER-PerfTrace-RCS-TraceInfoInMapping2.png)

In de traceringsgegevens geeft de waarde **\[12\]** voor de gegevensbron VendTable aan dat deze gegevensbron 12 maal is aangeroepen. De waarde **\[Q:6\]** geeft aan dat er zes aanroepen zijn omgezet in databaseaanroepen naar de tabel VendTable. De waarde **\[C:6\]** geeft aan dat de records die uit de database zijn opgehaald in de cache zijn opgeslagen en zes andere aanroepen zijn verwerkt met behulp van de cache.

Het aantal aanroepen naar de gegevensbron LedgerTransTypeList is van 9027 verlaagd naar 240.

![Traceringsgegevens voor de gegevensbron LedgerTransTypeList op de pagina Ontwerper modeltoewijzing in RCS.](./media/GER-PerfTrace-RCS-TraceInfoInMapping2a.png)

## <a name="review-the-execution-trace-in-the-application"></a>De tracering van uitvoering in de toepassing controleren

Naast RCS bieden sommige versies mogelijk functies voor het ontwerpen van een ER-raamwerk. Deze versies bevatten een optie **Ontwerpmodus inschakelen** die kan worden ingeschakeld. Deze optie is te vinden op het tabblad **Algemeen** van de pagina **Parameters van elektronische rapportage**, die u kunt openen vanuit het werkgebied **Elektronische rapportage**.

![De optie ontwerpmodus inschakelen op de pagina Parameters voor elektronische rapportage.](./media/GER-PerfTrace-GER-Parameters-DesignMode.png)

Als u een van deze versies gebruikt, kunt u de details van gegenereerde prestatietraceringen direct in de toepassing analyseren. U hoeft deze niet vanuit de toepassing te exporteren en in RCS te importeren.

## <a name="review-the-execution-trace-by-using-external-tools"></a>De uitvoeringstracering via externe hulpprogramma's controleren

### <a name="configure-user-parameters"></a>Gebruikersparameters configureren

1. Ga naar **Organisatiebeheer \> Elektronische rapportage \> Configuraties**.
2. Selecteer op de pagina **Configuraties** in het actievenster op het tabblad **Configuraties** in de groep **Geavanceerde instellingen** de optie **Gebruikersparameters**.
3. Selecteer in het dialoogvenster **Gebruikersparameters** in de sectie **Uitvoeringstracering** in het veld **Opmaak van uitvoeringstracering** de optie **PerfView XML**.

### <a name="run-the-er-format"></a>De ER-indeling uitvoeren

Herhaal de stappen uit het gedeelte [De ER-indeling uitvoeren](#run-format) eerder in dit artikel om een nieuwe prestatietracering te genereren.

U ziet dat de webbrowser een zipbestand voor downloaden biedt. Dit bestand bevat de prestatietracering in PerfView-indeling. Vervolgens kunt u het PerfView-hulpprogramma voor prestatieanalyse gebruiken om de details van de ER-indelingsuitvoering te analyseren.

![Prestatietraceringsgegevens in PerfView-indeling.](./media/GER-PerfTrace2-PerfViewTrace1.PNG)

## <a name="use-external-tools-to-review-an-execution-trace-that-includes-database-queries"></a>Externe hulpprogramma's gebruiken om een uitvoeringstracering met databasequery's te controleren.

Vanwege verbeteringen in het ER-raamwerk biedt de prestatietracering die in de PerfView-indeling wordt gegenereerd nu meer informatie over het uitvoeren van ER-indelingen. In Microsoft Dynamics 365 Finance 10.0.4 (juli 2019) kan deze tracering ook details van uitgevoerde SQL-query's naar de toepassingsdatabase bevatten.

### <a name="configure-user-parameters"></a>Gebruikersparameters configureren

1. Ga naar **Organisatiebeheer** \> **Elektronische rapportage** \> **Configuraties**.
2. Selecteer op de pagina **Configuraties** in het actievenster op het tabblad **Configuraties** in de groep **Geavanceerde instellingen** de optie **Gebruikersparameters**.
3. Stel de volgende parameters in de sectie **Uitvoeringstracering** van het dialoogvenster **Gebruikersparameters** in:

    - Selecteer **PerfView XML** in het veld **Opmaak van uitvoeringstracering**.
    - Stel de optie **Statistieken voor query's verzamelen** in op **Ja**.
    - Stel de optie **Query traceren** in op **Ja**.

    ![De sectie Uitvoeringstracering, dialoogvenster Gebruikersparameters.](./media/GER-PerfTrace2-GER-UserParameters.PNG)

### <a name="run-the-er-format"></a>De ER-indeling uitvoeren

Herhaal de stappen uit het gedeelte [De ER-indeling uitvoeren](#run-format) eerder in dit artikel om een nieuwe prestatietracering te genereren.

U ziet dat de webbrowser een zipbestand voor downloaden biedt. Dit bestand bevat de prestatietracering in PerfView-indeling. Vervolgens kunt u het PerfView-hulpprogramma voor prestatieanalyse gebruiken om de details van de ER-indelingsuitvoering te analyseren. Deze tracering bevat nu de details van SQL-databasetoegang tijdens de uitvoering van de ER-indeling.

![Traceringsgegeven voor de uitgevoerde ER-indeling in PerfView.](./media/GER-PerfTrace2-PerfViewTrace2.PNG)

## <a name="additional-resources"></a>Aanvullende bronnen

- [Overzicht van elektronische rapportage](general-electronic-reporting.md)
- [De prestaties van ER-oplossingen verbeteren door BEREKEND VELD-gegevensbronnen met parameters toe te voegen](er-calculated-field-ds-performance.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

