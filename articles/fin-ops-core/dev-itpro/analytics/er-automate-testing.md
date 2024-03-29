---
title: Testen automatiseren met elektronische rapportage
description: In dit artikel wordt uitgelegd hoe u de functie voor de basislijn van het elektronisch rapportageraamwerk (ER) kunt gebruiken om het testen van functionaliteit te automatiseren.
author: kfend
ms.date: 07/02/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2018-04-01
ms.dyn365.ops.version: Release 8.0
ms.search.form: ERSolutionTable, ERFormatBaselineTable, ERFormatMappingRunLogTable, ERParameters
ms.openlocfilehash: 8c7218ad8dec0d90c44967be902b912e36d97d39
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/12/2022
ms.locfileid: "9281867"
---
# <a name="automate-testing-with-electronic-reporting"></a>Testen automatiseren met elektronische rapportage

[!include[banner](../includes/banner.md)]

In dit artikel wordt uitgelegd hoe u het elektronisch rapportageraamwerk (ER) kunt gebruiken om het testen van sommige functionaliteit te automatiseren. Het voorbeeld in dit artikel laat zien hoe u het testen van de verwerking van leveranciersbetalingen kunt automatiseren.

De toepassing gebruikt het ER-raamwerk om betaling bestanden en bijbehorende documenten te genereren tijdens de verwerking van leveranciersbetalingen. Het ER‑raamwerk bestaat uit een gegevensmodel, modeltoewijzingen en opmaakcomponenten die de verwerking van betalingen voor verschillende betalingstypen en het genereren van documenten in verschillende indelingen ondersteunen. Deze onderdelen kunnen vanuit Microsoft Dynamics Lifecycle Services (LCS) worden gedownload en geïmporteerd in het exemplaar.

U kunt ook elk Microsoft-onderdeel aanpassen en gebruiken als basis voor uw eigen aangepaste component. Door een aangepaste versie te maken, kunt u wijzigingen aanbrengen die specifieke vereisten ondersteunen. U kunt bijvoorbeeld het ER-model en ER modeltoewijzing aanpassen om toegang te krijgen tot klantspecifieke toepassingsgegevens, of u kunt een ER-indeling wijzigen om de indeling van een gegenereerd document te wijzigen.

U kunt aangepaste ER-indelingen gebruiken om betalingsbestanden te verwerken waarmee leveranciersbetalingen worden gegenereerd en ook controlerapporten worden verwerkt. Versiebeheer wordt ondersteund in ER-onderdelen. Microsoft kan daarom bijgewerkte versies van ER-oplossingen leveren voor de verwerking van leveranciersbetalingen, en u kunt de bijgewerkte versie automatisch samenvoegen met uw aangepaste component door deze opnieuw te baseren. U moet echter de hergebaseerde versie testen om er zeker van te zijn dat deze werkt zoals u zou verwachten.

Er-gegevensmodellen en ER-modeltoewijzingen worden vaak gebruikt voor veel ER-indelingen die worden gebruikt om betalingen van verschillende typen te verwerken en om land-/regiospecifieke betalingsdocumenten te genereren. Daarom is het zeer wenselijk om de gebruikersacceptatie en het integratietesten te automatiseren zodat dit automatisch wordt uitgevoerd in meerdere bedrijven, maar de land/regio-context van elk doel bedrijf in overweging neemt, waarbij verschillende gegevenssets worden gebruikt, enzovoort.

Voor meer informatie over het maken van een aangepaste versie van een indeling die is gebaseerd op de indeling die u hebt ontvangen van een configuratieprovider, zie [ER Uw indeling bijwerken door een nieuwe basisversie van die indeling te maken](./tasks/er-upgrade-format.md).

## <a name="key-concepts"></a>Belangrijke concepten

Functionele hoofdgebruikers kunnen gebruikers accepteren en de integratie testen zonder dat ze broncode hoeven te schrijven.

- Gebruik de ER basisfunctie om de gegenereerde documenten te vergelijken met de hoofdexemplaren. Zie voor meer informatie [Gegenereerde rapportresultaten volgen en vergelijken met de basislijnwaarden](er-trace-reports-compare-baseline.md).
- Gebruik Taakrecorder om testcases vast te leggen en de analyse van basislijnen op te nemen. Zie [Resources voor Taakrecorder](../user-interface/task-recorder.md) voor meer informatie.
- Testcases groeperen voor vereiste testscenario's. Zie [Acceptatietests voor gebruikers maken en automatiseren](../lifecycle-services/using-task-guides-and-bpm-to-create-user-acceptance-tests.md) voor meer informatie.

    - Gebruik de Modelleertool bedrijfsprocessen (BPM) in LCS om bibliotheken te maken voor gebruikersacceptatietesten.
    - Gebruik BPM testbibliotheken om een testplan en testsuites te maken in Microsoft Azure DevOps Services (Azure DevOps).

Functionele hoofdgebruikers kunnen tests uitvoeren voor de acceptatie en integratie van gebruikers.

- Gebruik RSAT (Regression Suite Automation Tool) om testcases van de gewenste testsuite uit te voeren.
- Meld de resultaten van de test naar Azure DevOps en gebruik deze service om deze resultaten te onderzoeken.

## <a name="prerequisites"></a>Vereisten

Voordat u de taken in dit artikel kunt voltooien, moet u de volgende vereisten uitvoeren:

- Implementeer een topologie die testautomatisering ondersteunt. U moet toegang hebben tot het exemplaar van deze topologie voor de rol **Systeembeheerder**. Deze topologie moet de voorbeeldgegevens bevatten die in dit voorbeeld worden gebruikt. Zie [Omgevingen implementeren en gebruiken die continue build- en testautomatisering ondersteunen](../perf-test/continuous-build-test-automation.md) voor meer informatie.
- Als u de gebruikers- en integratietests automatisch wilt uitvoeren, moet u RSAT installeren in de topologie die u gebruikt en deze op de juiste manier configureren. Zie [Regression Suite Automation Tool](https://www.microsoft.com/download/details.aspx?id=57357) voor informatie over het installeren en configureren van RSAT voor het werken met apps voor financiën en bedrijfsactiviteiten en Azure DevOps. Let op de vereisten voor het gebruik van het hulpprogramma. In de volgende afbeelding ziet u een voorbeeld van de RSAT‑instellingen. De blauwe rechthoek omsluit de parameters waarmee toegang wordt gegeven tot Azure DevOps. De groene rechthoek omsluit de parameters waarmee de toegang tot het exemplaar wordt gegeven.

    ![RSAT-instellingen.](media/GER-Configure.png "Schermafbeelding van het dialoogvenster RSAT-instellingen")

- Als u test cases in suites wilt indelen om de juiste volgorde van uitvoering te garanderen, zodat u logboeken van testuitvoeringen voor verdere rapportage en onderzoek kunt verzamelen, moet u toegang hebben tot Azure DevOps vanuit de geïmplementeerde topologie.
- Als u het voorbeeld in dit artikel wilt voltooien, raden we aan [ER‑gebruik voor RSAT‑testen](https://go.microsoft.com/fwlink/?linkid=874684) te downloaden. Dit zip-bestand bevat de volgende taakbegeleidingen:

    | Inhoud                                           | Bestandsnaam en locatie |
    |---------------------------------------------------|------------------------|
    | Voorbeeld van taakregistratie om gegevens voor te bereiden voor het testen | Voorbereiden\\Registreren.xml |
    | Voorbeeld van taakregistratie voor het verwerken van leveranciersbetalingen   | Verwerken\\Registreren.xml |

## <a name="prepare-the-accounts-payable-module-to-process-vendor-payments"></a>De module leveranciers voorbereiden voor het verwerken van leveranciersbetalingen

1. Meld u aan bij uw exemplaar.
2. Download de volgende ER‑configuratie uit LCS. Zie voor instructies [ER Een configuratie importeren vanuit Lifecycle Services](./tasks/er-import-configuration-lifecycle-services.md)

    - ER-modelconfiguratie **Betalingsmodel**
    - **Betalingsmodeltoewijzing 1611** ER modeltoewijzingsconfiguratie
    - **BACS (UK)** ER indelingsconfiguratie

    ![Configuraties van elektronische rapportage.](media/GER-Configurations.png "Schermafbeelding van de configuratiepagina in Elektronische rapportage")

3. Selecteer het **GBSI** voorbeeldgegevensbedrijf, dat een land-/regiocode in Groot-Brittannië heeft.
4. Leveranciersparameters configureren:

    1. Ga naar **Leveranciers \> Betalingsinstelling \> Betalingsmethoden**.
    2. Selecteer **Elektronisch** als de betalingsmethode
    3. De geselecteerde betalingsmethode configureren zodat deze de indeling **BACS (UK)** gebruikt die u eerder hebt gedownload voor de verwerking van leveranciersbetalingen:

        1. Stel op het sneltabblad **Bestandsindelingen** de optie **Algemene elektronische exportindeling** in op **Ja**.
        2. Selecteer in het veld **Indelingsconfiguratie exporteren** **BACS**.

    ![Pagina Betalingsmethoden.](media/GER-APParameters.png "Schermafbeelding van de pagina Betalingsmethoden")

    > [!NOTE]
    > Als u de afgeleide versie van deze ER-indeling hebt die is gemaakt ter ondersteuning van aanpassingen, kunt u deze configuratie selecteren in de **Elektronische** betalingsmethode.

5. Een voorbeeld van een leveranciersbetaling maken:

    1. Ga naar **Leveranciers \> Betalingen \> Betalingsjournaal**.
    2. Zorg ervoor dat u het betalingsjournaal niet hebt geboekt.

        ![Pagina Betalingsjournaal.](media/GER-APJournal.png "Schermafbeelding van de pagina Betalingsjournaal")

    3. Selecteer **Regels** en voer een regel in met de volgende informatie.

        | Veld               | Voorbeeldwaarde   |
        |---------------------|-----------------|
        | Leveranciernaam         | GB\_si\_000001  |
        | Debet               | 1,000.00        |
        | Valuta            | GBP             |
        | Tegenrekeningtype | Bank            |
        | Tegenrekening      | GBSI OPER       |
        | Betalingswijze   | Elektronisch      |

    ![Pagina Leveranciersbetalingen.](media/GER-APJournalLines.png "Schermafbeelding van de pagina Leveranciersbetalingen")

## <a name="prepare-the-er-framework-to-test-vendor-payment-processing"></a>Het ER-Framework voorbereiden om verwerking van leveranciersbetalingen te testen

### <a name="configure-er-parameters"></a>ER-parameters configureren

1. Ga naar **Organisatieadministratie \> Elektronische rapportage \> Parameters Elektronische rapportage**.
2. Selecteer op het tabblad **Bijlagen** in het veld **Basislijn** **Bestand** als het documenttype dat door het Document beheer (DB)-raamwerk wordt gebruikt om documenten met betrekking tot de basislijnfunctie als DM‑bijlagen te behouden.

    ![Pagina Parameters van elektronische rapportage.](media/GER-ERParameters.png "Schermafbeelding van de pagina Parameters van elektronische rapportage")

### <a name="generate-baseline-copies-of-vendor-paymentrelated-documents"></a>Basislijnkopieën van documenten met betrekking tot leveranciersbetalingen genereren

1. Ga naar **Leveranciers \> Betalingen \> Betalingsjournaal**.
2. Selecteer **Regels**
3. Selecteer **Betalingen genereren**.
4. Selecteer **Elektronisch** als de betalingsmethode
5. Selecteer de bankrekening **GBSI OPER**.
6. Zet de optie **Controlerapport afdrukken** op **Ja**.
7. De gegenereerde uitvoer als een zip-bestand downloaden.
8. Open het gedownloade bestand.
9. Pak de volgende bestanden uit het gedownloade bestand uit:

    - **Bestand** betalingsbestand in tekstindeling
    - **ERVendOutPaymControlReport** controlerapportbestand in XLSX-indeling

    ![Uitgepakte bestanden.](media/GER-APJournalProcessed.png "Schermafbeelding van uitgepakte bestandsnamen in Windows Verkenner")

### <a name="turn-on-the-er-baseline-feature"></a>De functie voor ER basislijn inschakelen

1. Ga naar **Organisatiebeheer \> Elektronische rapportage \> Configuraties**.
2. Selecteer in het actievenster op het tabblad **Configuraties** de optie **Gebruikersparameters**.
3. Stel de optie **Uitvoeren in foutoplossingsmodus** in op **Ja**.

Door de parameter **Uitvoeren in foutopsporingsmodus** in te schakelen, dwingt u het ER-raamwerk de volgende acties uit te voeren na de uitvoering van een willekeurige ER‑indeling die uitgaande documenten genereert:

1. Bepalen of een basislijn is geconfigureerd voor een van de onderdelen van de uitgevoerde ER‑indeling.
2. Bepaal of elke geconfigureerde basislijn in de huidige voorwaarden van toepassing is (bedrijfscode van het aangemelde bedrijf, de bestandsnaam en de bestandsnaamextensie van de gegenereerde uitvoer, enzovoort).
3. Voer de volgende acties uit voor elke toepasselijke basislijn:

    1. Vergelijk de uitvoer die wordt gegenereerd tijdens het uitvoeren van de ER-indeling met de bijbehorende basislijn.
    2. Sla de resultaten van de vergelijking op in het logboek voor foutopsporing voor de ER-configuraties.

### <a name="configure-er-baselines-for-vendor-payment-processing"></a>ER‑basislijnen voor de verwerking van leveranciersbetalingen configureren

1. Ga naar **Organisatiebeheer \> Elektronische rapportage \> Configuraties**.
2. Selecteer **Basislijnen**.
3. Selecteer **Nieuw**.
4. Selecteer in het veld **Verwijzing** de indeling **BACS (UK)**.
5. Selecteer **Bijlagen**.
6. Een nieuwe basislijn toevoegen voor het bestand leveranciersbetalingen:

    1. Selecteer **Nieuw**.
    2. Selecteer in het veld **Type** het **Bestand** DB-documenttype dat u hebt geconfigureerd in de ER‑parameters voor het opslaan van basislijn artefacten.
    3. Blader om het lokaal opgeslagen **Bestand** met betalingsbestand in tekstindeling te selecteren.
    4. Voer in het veld **Omschrijving** het **Betalings-txt‑bestand** in.

7. Een nieuwe basislijn toevoegen voor het controlerapport voor de leveranciersbetaling:

    1. Selecteer **Nieuw**.
    2. Selecteer in het veld **Type** het **Bestand** DB-documenttype dat u hebt geconfigureerd in de ER‑parameters voor het opslaan van basislijn artefacten.
    3. Blader om het lokaal opgeslagen **ERVendOutPaymControlReport** controlerapportbestand in XLSX‑indeling te selecteren.
    4. Voer in het veld **Omschrijving** **Betaling XLXS‑controlerapport** in.

    ![Basislijnen voor het leveranciersbetalingsbestand.](media/GER-BaselineAttachments.png "Schermafbeelding van de pagina Configuraties met Betaling XLXS‑controlerapport geselecteerd")

8. Sluit de pagina.
9. Selecteer op het sneltabblad **Basislijnen** **Nieuw** om een basislijn voor het betalingsbestand te configureren:

    1. Noem de regel **Basislijninstelling voor betalingsbestand**.
    2. Selecteer in het veld **Naam bestandsonderdeel** **bestand** om deze basislijn toe te passen op de uitvoer van de ER-indeling die het betalingsbestand genereert in de BACS (UK)-tekstindeling.
    3. Selecteer in het veld **Bedrijven** **GBSI** om deze basislijn toe te passen wanneer de ER‑indeling **BACS (UK)** in het GBSI‑bedrijf wordt uitgevoerd.
    4. Voer in het veld **Masker bestandsnaam** de waarde **\*.TXT** in als u deze basislijn alleen wilt toepassen op uitvoer van het indelingsonderdeel **bestand** dat **.txt** als bestandsnaamextensie heeft.
    5. Selecteer in het veld **Basislijn** **Betaling TXT‑bestand** zodat deze basislijn wordt gebruikt voor vergelijking met de gegenereerde uitvoer.

10. Selecteer **Nieuw** om een basislijn voor het controlerapport te configureren:

    1. Noem de regel **Basislijninstelling voor controlerapport**.
    2. Selecteer in het veld **Naam bestandsonderdeel** **ERVendOutPaymControlReport** om deze basislijn toe te passen op de uitvoer van de ER-indeling die het controlerapport genereert.
    3. Selecteer in het veld **Bedrijven** **GBSI** om deze basislijn toe te passen wanneer de ER‑indeling **BACS (UK)** in het GBSI‑bedrijf wordt uitgevoerd.
    4. Voer in het veld **Masker bestandsnaam** de waarde **\*. XLSX** in als u deze basislijn alleen wilt toepassen op uitvoer van het indelingsonderdeel **ERVendOutPaymControlReport** dat **.xslx** als bestandsnaamextensie heeft.
    5. Selecteer in het veld **Basislijn** **Betaling XLSX controlerapport** zodat deze basislijn wordt gebruikt voor vergelijking met de gegenereerde uitvoer.

    ![Het sneltabblad Basislijnen op de pagina Configuraties.](media/GER-BaselineRules.png "Schermafbeelding van het sneltabblad Basislijnen op de pagina Configuraties")

## <a name="record-tests-to-validate-vendor-payment-processing"></a>Tests vastleggen om verwerking van leveranciersbetalingen te valideren

Als functionele hoofdgebruiker kunt u uw eigen stappen vastleggen om de verwerking van leveranciersbetalingen te testen. Het is raadzaam de taakregistratie **Voorbereiden\\Registreren.xml.** die u eerder hebt gedownload, te bekijken (en te bewerken indien nodig). Deze registratie wordt gebruikt om alle testgegevens de juiste status te geven. Deze stap is vereist omdat het testen meerdere keren kan worden uitgevoerd, en elke test moet gegevens in dezelfde status gebruiken.

### <a name="reset-user-settings"></a>Gebruikersinstellingen opnieuw instellen

1. Open het standaarddashboard.
2. Selecteer de knop **Instellingen** (het tandwielsymbool).
3. Selecteer **Gebruikersopties**.
4. Selecteer **Gebruiksgegevens**.
5. Selecteer **Opnieuw instellen**.
6. Selecteer **Ja** om te bevestigen dat u de gebruiksgegevens opnieuw wilt instellen.
7. Sluit de pagina.

### <a name="record-the-steps-to-prepare-data-for-testing"></a>De stappen registreren om gegevens voor te bereiden voor testen

1. Selecteer de knop **Instellingen** (het tandwielsymbool).
2. Selecteer **Taakrecorder**
3. Selecteer **Registratie afspelen**.
4. Selecteer **Openen vanaf deze pc**.
5. Selecteer **Bladeren** en selecteer het lokaal opgeslagen bestand **Voorbereiden\\Registreren.xml**.
6. Selecteer **Starten**.
7. Selecteer **Volgende stap in behandeling afspelen** totdat alle stappen in de registratie zijn afgespeeld.

Met deze taakregistratie worden de volgende acties uitgevoerd:

1. Stel de status van de verwerkte betalingsregel in op **Geen**.

    ![Taakregistratie stap 3 en 4.](media/GER-Recording1Review1.png "Schermafbeelding van taakregistratiestappen 3 en 4")

2. De ER gebruikersparameter **Uitvoeren in foutopsporingsmodus** inschakelen.

    ![Taakregistratie stap 9 en 10.](media/GER-Recording1Review2.png "Schermafbeelding van taakregistratiestappen 9 en 10")

3. Opschonen van het ER foutopsporingslogboek met de resultaten van de vergelijking van gegenereerde bestanden met basislijnen.

    ![Taakregistratie stap 13 en 15.](media/GER-Recording1Review3.png "Schermafbeelding van taakregistratiestap 13 tot en met 15")

### <a name="record-the-steps-to-test-vendor-payment-processing"></a>De stappen voor het testen van de verwerking van leveranciersbetalingen registreren

Het is raadzaam de taakregistratie **Verwerken\\Registreren.xml.** die u eerder hebt gedownload, te bekijken (en te bewerken indien nodig). Deze registratie wordt gebruikt om leveranciersbetalingen te verwerken en de resultaten van de vergelijking van gegenereerde documenten met overeenkomende basislijnen te valideren.

1. Selecteer de knop **Instellingen** (het tandwielsymbool).
2. Selecteer **Taakrecorder**.
3. Selecteer **Registratie afspelen**.
4. Selecteer **Openen vanaf deze pc**.
5. Selecteer **Bladeren** en selecteer het lokaal opgeslagen bestand **Verwerken\\Registreren.xml**.
6. Selecteer **Starten**.
7. Selecteer **Volgende stap in behandeling afspelen** totdat alle stappen in de registratie zijn afgespeeld.

Met deze taakregistratie worden de volgende acties uitgevoerd:

1. Verwerking leveranciersbetalingen starten.
2. Selecteer de juiste runtime‑parameters en schakel het genereren van een controlerapport in.

    ![Taakregistratie stap 3 en 8.](media/GER-Recording2Review1.png "Schermafbeelding van taakregistratiestap 3 tot en met 8")

3. Openen van het ER foutopsporingslogboek om de resultaten van de vergelijking van gegenereerde uitvoer met corresponderende basislijnen te registreren.

    In het ER logboek voor foutopsporing worden de resultaten van de vergelijking weergegeven in het veld **Gegenereerde tekst**. De velden **Indelingsonderdeel** en **Indelingspad dat een logboekvermelding veroorzaakte** verwijzen naar het bestandsonderdeel waarvoor de gegenereerde uitvoer is vergeleken met de basislijn.

    ![Vermeldingen op de pagina Elektronische uitvoeringslogboeken.](media/GER-ERDebugLog.png "Schermafbeelding van vermeldingen op de pagina Uitvoeringslogboeken voor elektronische rapportage")

4. De vergelijking van de huidige uitvoer met de basislijn wordt vastgelegd met de optie taakregistratie **Valideren** en het selecteren van **Huidige waarde**.

    ![De optie Valideren gebruiken voor vergelijking met de huidige waarde.](media/GER-TRRecordValidation.png "Schermafbeelding van het gebruik van de optie Valideren voor vergelijking met de huidige waarde")

    In de volgende afbeelding ziet u hoe de stappen van geregistreerde validatie eruitzien in de taakregistratie.

    ![Taakregistratie stap 13 en 15.](media/GER-Recording2Review2.png "Schermafbeelding van taakregistratiestappen 13 en 15")

## <a name="add-the-recorded-tests-to-azure-devops"></a>Voeg de geregistreerde tests toe aan Azure DevOps

1. Open de Azure DevOps‑omgeving.
2. Selecteer het project dat u in de RSAT-parameters hebt gedefinieerd toen het u het [hulpprogramma](#prerequisites) configureerde.
3. Selecteer het testplan dat u in de RSAT-parameters hebt gedefinieerd toen het u het [hulpprogramma](#prerequisites) configureerde.
4. Een nieuwe testcase maken voor het geselecteerde testplan:

    1. Geef de testcase een naam **Data voorbereiden voor testverwerking van de elektronische betaling van de leverancier**.
    2. Koppel het bestand **Registreren.xml** vanuit de map **Voorbereiden** die u eerder hebt gedownload.

5. Een nieuwe testcase maken voor het geselecteerde testplan:

    1. Noem de testcase **Test voor verwerking van leveranciersbetalingen met behulp van ER‑indeling BACS (UK)**.
    2. Koppel het bestand **Registreren.xml** vanuit de map **Verwerken** die u eerder hebt gedownload.

    ![Nieuwe testcases voor het geselecteerde testplan.](media/GER-RSAT-DevOps-Tests-Passed.png "Schermafbeelding van de nieuwe testcases voor het geselecteerde testplan")

> [!NOTE]
> Let op de juiste volgorde van uitvoering van de testen die worden toegevoegd.

## <a name="prepare-rsat-to-run-the-recorded-tests"></a>RSAT voorbereiden om de geregistreerde tests uit te voeren

### <a name="load-the-tests-from-azure-devops-to-rsat"></a>De tests van Azure DevOps naar RSAT laden

1. Open de lokale RSAT-toepassing in de huidige topologie.
2. Selecteer **Laden** om de tests te laden die zich momenteel Azure DevOps in RSAT bevinden.

    ![Tests die zijn geladen in RSAT.](media/GER-RSAT-RSAT-Tests-Loaded.png "Schermafbeelding van de tests die in RSAT zijn geladen")

### <a name="create-automation-and-parameters-files"></a>Automatiserings‑ en parameterbestanden maken

1. Selecteer in RSAT de tests die u hebt geladen van Azure DevOps.
2. Selecteer **Nieuw** om RSAT automatiserings‑ en parameterbestanden te maken.

    ![RSAT-automatiserings- en -parameterbestanden die in RSAT zijn gemaakt.](media/GER-RSAT-RSAT-Tests-Initiated.png "Schermafbeelding van de RSAT-automatiserings- en -parameterbestanden die in RSAT zijn gemaakt")

### <a name="modify-the-parameters-files"></a>De parameterbestanden wijzigen

1. Selecteer in RSAT de testcase **Data voorbereiden voor testverwerking van de elektronische betaling van de leverancier**.
2. Selecteer **Bewerken**.
3. Wijzig in de Microsoft Excel‑werkmap die is geopend in het werkblad **Algemeen** de bedrijfscode in **GBSI**, omdat dit bedrijf wordt gebruikt voor de uitvoering van de test.
4. Selecteer in RSAT de testcase **Test voor verwerking van leveranciersbetalingen met behulp van ER‑indeling BACS (UK)**.
5. Selecteer **Bewerken**.
6. Wijzig in de Excel-werkmap die is geopend in het werkblad **Algemeen** de bedrijfscode in **GBSI**.
7. In het werkblad **ERFormatMappingRunLogTable** bevatten de cellen A:3 en C:3 de tekst van de velden in de logboektabel voor ER foutopsporing die wordt gebruikt om de resultaten van de vergelijking van de uitvoer naar de basislijn te valideren. Deze teksten worden gebruikt om logboekrecords voor ER foutopsporing te evalueren die tijdens de testuitvoering worden gemaakt.

    ![Werkblad ERFormatMappingRunLogTable.](media/GER-RSAT-RSAT-ExcelParameters.png "Schermafbeelding van het werkblad ERFormatMappingRunLogTable")

## <a name="run-the-tests-and-analyze-the-results"></a>De tests uitvoeren en de resultaten analyseren

### <a name="run-the-tests-in-rsat"></a>De tests uitvoeren in RSAT

1. Selecteer in RSAT de geladen tests.
2. Selecteer **Uitvoeren**.

U ziet dat testcases automatisch worden uitgevoerd in de toepassing met behulp van een webbrowser.

### <a name="analyze-the-results-of-test-execution"></a>De resultaten van de testuitvoering analyseren

De resultaten van de testuitvoering worden opgeslagen in RSAT. U ziet dat beide tests zijn geslaagd.

![Tests die zijn geslaagd in RSAT.](media/GER-RSAT-RSAT-Tests-Passed.png "Schermafbeelding van tests die zijn geslaagd in RSAT")

De resultaten van de testuitvoering worden eveneens verzonden Azure DevOps, zodat u verdere analyses kunt maken.

![Resultaten van de testuitvoering in Azure DevOps.](media/GER-RSAT-DevOps-Tests-Added.png "Schermafbeelding van de resultaten van testuitvoeringen in Azure DevOps")

### <a name="simulate-a-situation-where-tests-fail"></a>Een situatie simuleren waarbij tests mislukken

Deze testsuite moet mislukken als ten minste één van de gegenereerde uitvoeren niet overeenkomt met de overeenkomstige basislijn. Om deze situatie te verwezenlijken kunt u de afgeleide versie van de **BACS (UK)**-indeling gebruiken waarmee een betalingsbestand wordt gegenereerd met andere inhoud dan de overeenkomstige basislijn. Als u deze situatie wilt simuleren, kunt u dezelfde **BACS (UK)**‑indeling gebruiken, maar het betalingsbedrag op de verwerkte betalingsregel wijzigen.

1. Open de toepassing en ga naar **Leveranciers \> Betalingen \> Betalingsjournaal**.
2. Selecteer **Regels**
3. Selecteer de betalingsregel en selecteer vervolgens **Betalingsstatus \> Geen**.
4. Wijzig in het veld **Debet** de waarde van **1.000,00** in **2.000,00**.
5. Klik op **Opslaan** om uw wijzigingen op te slaan.

### <a name="run-the-tests-in-rsat"></a>De tests uitvoeren in RSAT

1. Selecteer in RSAT de geladen tests.
2. Selecteer **Uitvoeren**.

U ziet dat testcases automatisch worden uitgevoerd in de toepassing met behulp van een webbrowser.

### <a name="analyze-the-results-of-test-execution"></a>De resultaten van de testuitvoering analyseren

De resultaten van de testuitvoering worden opgeslagen in RSAT. De tweede test is mislukt tijdens de tweede uitvoering.

![Mislukte testresultaten in RSAT.](media/GER-RSAT-RSAT-Tests-Failed.png "Schermafbeelding van de mislukte testresultaten in RSAT")

De resultaten van de testuitvoering worden eveneens verzonden Azure DevOps, zodat u verdere analyses kunt maken.

![Mislukte testresultaten in Azure DevOps.](media/GER-RSAT-DevOps-Tests-Failed.png "Schermafbeelding van de mislukte testresultaten in Azure DevOps")

U kunt de status van elke test bekijken. U kunt ook het uitvoeringslogboek openen, zodat u de redenen voor fouten kunt analyseren. In de volgende afbeelding ziet u in het uitvoeringslogboek dat de fout is opgetreden vanwege het verschil in de inhoud tussen het gegenereerde betalingsbestand en de basislijn.

![Uitvoeringslogboek voor analyseren van fout in Azure DevOps.](media/GER-RSAT-DevOps-Tests-Failed-Log.png "Schermafbeelding van het uitvoeringslogboek voor foutanalyse in Azure DevOps")

Zoals u hebt gezien, kan de werking van elke willekeurige ER-indeling automatisch worden geëvalueerd door RSAT als testplatform te gebruiken en door op de Taakrecorder gebaseerde testcases te gebruiken die de ER‑basislijnfunctie gebruiken.

## <a name="additional-resources"></a>Aanvullende resources

- [Resources voor Taakrecorder](../user-interface/task-recorder.md)
- [Regression Suite Automation Tool](https://www.microsoft.com/download/details.aspx?id=57357)
- [Acceptatietests voor gebruikers maken en automatiseren](../lifecycle-services/using-task-guides-and-bpm-to-create-user-acceptance-tests.md)
- [Omgevingen implementeren en gebruiken die continue build- en testautomatisering ondersteunen](../perf-test/continuous-build-test-automation.md)
- [Gegenereerde rapportresultaten volgen en vergelijken met de basislijnwaarden](er-trace-reports-compare-baseline.md)
- [ER Uw indeling upgraden door een nieuwe basisversie van die indeling aan te nemen](tasks/er-upgrade-format.md)
- [Een ER-configuratie vanuit Lifecycle Services importeren](tasks/er-import-configuration-lifecycle-services.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
