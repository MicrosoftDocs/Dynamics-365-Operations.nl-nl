---
title: Gegenereerde rapportresultaten traceren en vergelijken met basislijnwaarden
description: Dit onderwerp biedt informatie over hoe u de resultaten van gegenereerde ER-rapporten (elektronische rapportage) kunt vergelijken met basislijnrapportwaarden.
author: NickSelin
manager: AnnBe
ms.date: 06/17/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-04-01
ms.dyn365.ops.version: Release 8.0
ms.openlocfilehash: 1643e7fb3128faf6ad638d4cdad313b3667463b1
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/27/2019
ms.locfileid: "2181675"
---
# <a name="trace-generated-report-results-and-compare-them-with-baseline-values"></a>Gegenereerde rapportresultaten traceren en vergelijken met basislijnwaarden

[!include[banner](../includes/banner.md)]

U kunt de resultaten van ER-indelingen traceren die uitgaande elektronische documenten genereren. Wanneer het genereren van tracering is ingeschakeld (met de ER-gebruikersparameter **Uitvoeren in foutoplossingsmodus**), wordt elke keer dat een ER-rapport wordt uitgevoerd een nieuwe tracerecord gegenereerd in het uitvoeringslogboek met ER-indeling. De volgende gegevens worden opgeslagen in elke trace die wordt gegenereerd:

- Alle waarschuwingen die zijn gegenereerd door validatieregels
- Alle fouten die zijn gegenereerd door validatieregels
- Alle gegenereerde bestanden die zijn opgeslagen als bijlagen van de traceringsrecord

U kunt afzonderlijke basislijntoepassingsbestanden voor een bepaalde ER-indeling opslaan. Bestanden worden als basislijnbestanden beschouwd wanneer ze de verwachte resultaten beschrijven van rapporten die worden uitgevoerd. Als een basislijnbestand beschikbaar is voor een ER-indeling die wordt uitgevoerd terwijl het genereren van tracering is ingeschakeld, slaat de trace, naast de gegevens die reeds eerder zijn vermeld, het resultaat op van de vergelijking van het gegenereerde elektronische document met het basislijnbestand. Met één klik kunt u ook het gegenereerde elektronische document en het basislijnbestand in een enkel zip-bestand krijgen. Vervolgens kunt u een gedetailleerde vergelijking uitvoeren met behulp van een extern hulpprogramma zoals WinDiff.

U kunt de tracering evalueren om te analyseren of de elektronische documenten die worden gegenereerd, de verwachte inhoud bevatten. U kunt deze evaluatie uitvoeren in een UAT-omgeving (User Acceptance Testing) wanneer de codebasis is gewijzigd (bijvoorbeeld wanneer u bent gemigreerd naar een nieuw exemplaar van de toepassing, hotfixpakketten hebt geïnstalleerd of codewijzigingen hebt geïmplementeerd). Op deze manier kunt u ervoor zorgen dat de evaluatie geen invloed heeft op de uitvoering van ER-rapporten die worden gebruikt. Voor veel ER-rapporten kan de evaluatie plaatsvinden in de modus zonder toezicht.

Voor meer informatie over deze functie speelt u de taakbegeleidingen **ER-rapporten genereren en resultaten vergelijken (deel 1)** en **ER-rapporten genereren en resultaten vergelijken (deel 2)** af, die deel uitmaken van het bedrijfsproces **7.5.4.3 IT-services en -oplossingen testen ( 10679)** en kunnen worden gedownload uit het [Microsoft Downloadcentrum](https://go.microsoft.com/fwlink/?linkid=874684). Deze taakrichtlijnen begeleiden u bij het proces van het configureren van het ER-raamwerk om basislijnbestanden te gebruiken om gegenereerde elektronische documenten te evalueren.

## <a name="example-trace-generated-report-results-and-compare-them-with-baseline-values"></a>Voorbeeld: Gegenereerde rapportresultaten volgen en vergelijken met de basislijnwaarden

In deze procedure wordt uitgelegd hoe u het ER-Framework kunt configureren voor het verzamelen van informatie over de uitvoering van ER-indelingen en vervolgens de resultaten van die uitvoeringen kunt evalueren. Als onderdeel van deze evaluatie worden gegenereerde documenten vergeleken met hun basislijnbestanden. In dit voorbeeld maakt u de vereiste ER-configuraties voor het voorbeeldbedrijf, Litware, Inc. Deze procedure is bedoeld voor gebruikers met de rol Systeembeheerder of Elektronische aangifteontwikkelaar. Deze stappen kunnen worden voltooid met elke dataset.

Als u de stappen in dit voorbeeld wilt uitvoeren, moet u eerst in RCS de stappen voltooien in [Een configuratieprovider maken en deze als actief markeren](tasks/er-configuration-provider-mark-it-active-2016-11.md).

1. Ga naar **Organisatiebeheer** \> **Werkgebieden** \> **Elektronische rapportage**.
2. Controleer op de pagina **Lokalisatieconfiguraties** in de sectie **Configuratieproviders** of de configuratieprovider voor het voorbeeldbedrijf Litware, Inc. wordt vermeld en of het is gemarkeerd als **Actief**. Als u deze configuratieprovider niet ziet, voltooit u de stappen in [Een configuratieprovider maken en deze als actief markeren](tasks/er-configuration-provider-mark-it-active-2016-11.md).

### <a name="configure-document-management-parameters"></a>Parameters voor documentbeheer configureren

1. Ga naar **Organisatiebeheer** \> **Documentbeheer** \> **Documenttypen** en maak een nieuw documenttype om basislijnbestanden op te slaan.
2. Geef in het veld **Klasse** de tekst **Bestand bijvoegen** op.
3. Geef in het veld **Groep** de tekst **Bestand** op.

![De pagina Documenttypen](media/GER-BaselineSample-SetupDocumentType.PNG "Schermafbeelding van de pagina Documenttypen")

> [!NOTE]
> Een nieuw documenttype met dezelfde naam moet worden geconfigureerd voor elke gegevensset waarvoor u de ER-basislijnfunctie wilt gebruiken.

### <a name="configure-er-parameters-to-start-to-use-the-baseline-feature"></a>ER-parameters configureren om aan de slag te gaan met de basislijnfunctie

1. Selecteer in het werkgebied **Elektronische rapportage** in de sectie **Verwante koppelingen** de optie **Parameters van elektronische rapportage**.

    ![Het werkgebied Elektronische rapportage](media/GER-BaselineSample-ERWorkspace.PNG "Schermafbeelding van het werkgebied Elektronische rapportage")

2. Typ of selecteer op het tabblad **Bijlagen** in het veld **Basislijn** het documenttype dat u zojuist hebt gemaakt.

    ![Het tabblad Bijlagen van de pagina Parameters van elektronische rapportage](media/GER-BaselineSample-ERParameters.PNG "Schermafbeelding van de pagina Parameters van elektronische rapportage")

3. Selecteer **Opslaan**en sluit de pagina **Parameters van elektronische rapportage**.

### <a name="add-a-new-er-model-configuration"></a>Een nieuwe ER-modelconfiguratie toevoegen

1. Selecteer in het werkgebied **Elektronische rapportage** in de sectie **Configuraties** de tegel **Rapportconfiguraties**.
2. Selecteer **Configuratie maken** in het actievenster.
3. Voer in het vervolgkeuzemenu in het veld **Naam** **Model voor leren van ER-basislijnen** in.
4. Selecteer **Configuratie maken** om het maken van een nieuw ER-gegevensmodel te bevestigen.

![Het vervolgkeuzemenu Configuratie maken](media/GER-BaselineSample-ModelAdd.PNG "Schermafbeelding van het vervolgkeuzemenu Configuratie maken")

### <a name="design-a-data-model"></a>Een gegevensmodel ontwerpen

1. Selecteer in het actievenster op de pagina **Configuraties** de optie **Ontwerper**.
2. Selecteer **Nieuw**.
3. Voer in het vervolgkeuzemenu in het veld **Naam** de tekst **Basis** in.
4. Selecteer **Toevoegen**.
5. Selecteer **Basisverwijzing**.
6. Selecteer **OK** en vervolgens **Opslaan**.
7. Sluit de pagina **Modelontwerper**.
8. Selecteer **Status wijzigen**.
9. Selecteer **Voltooid** en vervolgens **OK**.

![De pagina Configuraties](media/GER-BaselineSample-ModelComplete.PNG "Schermafbeelding van de pagina Configuraties")

### <a name="add-a-new-er-format-configuration"></a>Een nieuwe ER-indelingsconfiguratie toevoegen

1. Selecteer in het actievenster op de pagina **Configuraties** de optie **Configuratie maken**.
2. Ga naar het vervolgkeuzemenu en selecteer in de veldgroep **Nieuw** de optie **Indeling gebaseerd op gegevensmodel Model voor leren van ER-basislijnen**.
3. Voer in het veld **Naam** de tekst **Indeling voor leren van ER-basislijnen** in.
4. Selecteer **Configuratie maken** om het maken van een nieuwe ER-indeling te bevestigen.

![Het vervolgkeuzemenu Configuratie maken](media/GER-BaselineSample-FormatAdd.PNG "Schermafbeelding van het vervolgkeuzemenu Configuratie maken")

### <a name="design-a-format"></a>Een indeling ontwerpen

In dit voorbeeld maakt u een eenvoudige ER-indeling voor het genereren van XML-documenten.

1. Selecteer in het actievenster op de pagina **Configuraties** de optie **Ontwerper**.
2. Selecteer **Basis toevoegen**.
2. Voer de volgende stappen uit in het dialoogvenster:

    1. Selecteer **Common\\File** in de structuur.
    2. Voer in het veld **Naam** de tekst **Uitvoer** in.
    3. Selecteer **OK**.

3. Selecteer **Toevoegen**.
4. Voer de volgende stappen uit in het dialoogvenster:

    1. Selecteer **XML\\Element** in de structuur.
    2. Voer in het veld **Naam** de tekst **Document** in.
    3. Selecteer **OK**.

5. Selecteer **Output\\Document** in de structuur.
6. Selecteer **Toevoegen**.
7. Voer de volgende stappen uit in het dialoogvenster:

    1. Selecteer **XML\\Attribute** in de structuur.
    2. Geef in het veld **Naam** de tekst **Id** op.
    3. Selecteer **OK**.

    ![De pagina Indelingsontwerper](media/GER-BaselineSample-FormatLayoutDesign.PNG "Schermafbeelding van de pagina Indelingsontwerper")

8. Selecteer op het tabblad **Toewijzing** de optie **Verwijderen**.
9. Selecteer **Basis toevoegen**.
10. Selecteer in het vervolgkeuzemenu in de structuur **Algemeen\\Gebruikersinvoerparameter** en voer vervolgens de volgende stappen uit:

    1. Geef in het veld **Naam** de tekst **Id** op.
    2. Geef in het veld **Label** de tekst **Id opgeven** op.
    3. Selecteer **OK**.

11. Select **Uitvoer\\Document\\Id** in de structuur.
12. Selecteer **Binden** en vervolgens **Opslaan**.

![De pagina Indelingsontwerper](media/GER-BaselineSample-FormatMappingDesign.PNG "Schermafbeelding van de pagina Indelingsontwerper")

Op basis van de ontworpen structuur genereert de geconfigureerde indeling een XML-bestand. Deze XML bevat het element **Basis** met het kenmerk **Id** dat is ingesteld op de waarde die de gebruiker invoert in het dialoogvenster ER-runtime.

### <a name="generate-a-new-baseline-file-for-a-designed-er-format"></a>Een nieuw basislijnbestand genereren voor een ontworpen ER-indeling

1. Selecteer op de pagina **Configuraties** op het sneltabblad **Versies** de optie **Uitvoeren**.
2. Geef in het veld **Id opgeven** het cijfer **1** op.
3. Selecteer **OK**.

    ![Het dialoogvenster Parameters elektronisch rapport](media/GER-BaselineSample-FormatRunToMakeBaselineFile1.PNG "Schermafbeelding van het dialoogvenster Parameters elektronisch rapport")

4. Sla een lokale kopie op van het gegenereerde bestand **out.Admin.xml**, zodat u het later kunt gebruiken als basislijn voor deze ER-indeling.

    ![Melding over het gegenereerde bestand op de pagina Configuraties](media/GER-BaselineSample-FormatRunToMakeBaselineFile2.PNG "Schermafbeelding van de melding over het gegenereerde bestand op de pagina Configuraties")

### <a name="configure-er-parameters-to-use-the-baseline-feature"></a>ER-parameters configureren om de basislijnfunctie te gebruiken

1. Selecteer op de pagina **Configuraties** in het actievenster op het tabblad **Configuraties** de optie **Gebruikersparameters**.
2. Stel de optie **Uitvoeren in foutoplossingsmodus** in op **Ja**.
3. Selecteer **OK**.

![Het dialoogvenster Gebruikersparameters](media/GER-BaselineSample-ERUserParameters.PNG "Schermafbeelding van het dialoogvenster Gebruikersparameters")

### <a name="add-a-new-baseline-for-designed-er-format"></a>Een nieuwe basislijn voor een ontworpen ER-indeling toevoegen

1. Ga naar **Organisatiebeheer** \> **Elektronische rapportage** \> **Configuraties**.
2. Selecteer **Basislijnen** in het actievenster.

    ![De knop Basislijnen op de pagina Configuraties](media/GER-BaselineSample-OpenBaselinePage.PNG "Schermafbeelding van de knop Basislijnen op de pagina Configuraties")

3. Selecteer **Nieuw** in het actievenster.
4. Selecteer de ER-indeling **Indeling voor leren van ER-basislijnen** die u eerder hebt ontworpen.
5. Selecteer **Opslaan**.

![De pagina Basislijnen voor ER-indeling](media/GER-BaselineSample-AddBaseline.PNG "Schermafbeelding van de pagina Basislijnen voor ER-indeling")

De basislijn wordt toegevoegd voor de indeling **Indeling voor leren van ER-basislijnen**.

### <a name="configure-a-baseline-rule-for-the-added-baseline"></a>Een basislijnregel voor de toegevoegde basislijn configureren

1. Selecteer op de pagina **Basislijnen voor ER-indeling** in het actievenster de knop **Bijlagen** (de paperclip).
2. Selecteer **Nieuw** \> **Bestand** in het actievenster. In de ER-parameters moet het documenttype **Bestand** eerder zijn geselecteerd als het documenttype dat wordt gebruikt voor de opslag van basislijnbestanden.
3. Selecteer **Bladeren**en selecteer de het bestand **out.Admin.xml** dat is gegenereerd toen u de geconfigureerde ER-indeling eerder uitvoerde.

    ![De pagina Bijlagen](media/GER-BaselineSample-UploadBaselineFile.PNG "Schermafbeelding van de pagina Bijlagen")

4. Sluit de pagina **Bijlagen**.
5. Selecteer **Nieuw** op het sneltabblad **Basislijnen**.
6. Voer in het veld **Naam** de tekst **Basislijn 1** in.
7. Selecteer in het veld **Naam bestandsonderdeel** de optie **Uitvoer** of selecteer deze. Deze waarde geeft aan dat de geconfigureerde basislijn wordt vergeleken met een bestand dat met behulp van het indelingselement **Uitvoer** is gegenereerd.
8. Voer in het veld **Masker bestandsnaam** de waarde **\*.xml** in.

    > [!NOTE]
    > U kunt het masker voor de bestandsnaam definiëren. Wanneer het masker voor de bestandsnaam is gedefinieerd, wordt de basislijnrecord alleen gebruikt om de gegenereerde uitvoer te evalueren wanneer de naam van het gegenereerde uitvoerbestand voldoet aan dat masker.

9. Als de geconfigureerde basislijn alleen moet worden gebruikt wanneer de ER-indeling **Indeling voor leren van ER-basislijnen** wordt uitgevoerd door gebruikers die zijn aangemeld bij bepaalde bedrijven, selecteert u die bedrijven in het veld **Bedrijven**.
10. In het veld **Basislijn** typt of selecteert u de bijlage **out.Admin**.
11. Selecteer **Opslaan**.

![De pagina Basislijnen voor ER-indeling](media/GER-BaselineSample-SetupBaselineLine.PNG "Schermafbeelding van de pagina Basislijnen voor ER-indeling")

### <a name="run-the-designed-er-format-and-review-the-log-to-analyze-the-results"></a>De ontworpen ER-indeling uitvoeren en het logboek controleren om de resultaten te analyseren

1. Ga naar **Organisatiebeheer** \> **Elektronische rapportage** \> **Configuraties**.
2. Vouw in de structuur **Model voor leren van ER-basislijnen** uit en selecteer vervolgens **Model voor leren van ER-basislijnen\\Indeling voor leren van ER-basislijnen**.
3. Selecteer op het sneltabblad **Versies** de optie **Uitvoeren**.
4. Geef in het veld **Id opgeven** het cijfer **1** op.
5. Selecteer **OK**.
6. Ga naar **Organisatiebeheer** \> **Elektronische rapportage** \> **Foutopsporingslogboeken voor configuraties**.

    ![De pagina Uitvoeringslogboeken voor elektronische rapportage](media/GER-BaselineSample-ReviewBaselineComparison1.PNG "Schermafbeelding van de pagina Uitvoeringslogboeken voor elektronische rapportage")

    > [!NOTE]
    > Het uitvoeringslogboek bevat informatie over de resultaten van de vergelijking van het gegenereerde bestand met de geconfigureerde basislijn. In dit voorbeeld geeft het logboek aan dat het gegenereerde bestand en de basislijn gelijk zijn.

7. Selecteer **Alles verwijderen**.

### <a name="run-the-designed-er-format-and-review-the-log-to-analyze-the-results"></a>De ontworpen ER-indeling uitvoeren en het logboek controleren om de resultaten te analyseren

1. Ga naar **Organisatiebeheer** \> **Elektronische rapportage** \> **Configuraties**.
2. Vouw in de structuur **Model voor leren van ER-basislijnen** uit en selecteer vervolgens **Model voor leren van ER-basislijnen\\Indeling voor leren van ER-basislijnen**.
3. Selecteer op het sneltabblad **Versies** de optie **Uitvoeren**.
4. Geef in het veld **Id opgeven** het cijfer **2** op.
5. Selecteer **OK**.
6. Ga naar **Organisatiebeheer** \> **Elektronische rapportage** \> **Foutopsporingslogboeken voor configuraties**.

    ![De pagina Uitvoeringslogboeken voor elektronische rapportage](media/GER-BaselineSample-ReviewBaselineComparison2.PNG "Schermafbeelding van de pagina Uitvoeringslogboeken voor elektronische rapportage")

    > [!NOTE]
    > Het uitvoeringslogboek bevat informatie over de resultaten van de vergelijking van het gegenereerde bestand met de geconfigureerde basislijn. In dit voorbeeld geeft het logboek aan dat het gegenereerde bestand en de basislijn niet gelijk zijn.

7. Selecteer **Vergelijken**.

> [!NOTE]
> Het gegenereerde bestand en het basislijnbestand worden als zipbestand aangeboden. U kunt externe vergelijkingsprogramma's, zoals WinDiff, gebruiken om de bestanden te vergelijken en de verschillen te bekijken.

## <a name="additional-resources"></a>Aanvullende resources

- [ER-raamwerk configureren](electronic-reporting-er-configure-parameters.md)
