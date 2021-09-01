---
title: Een nieuwe ER-oplossing ontwerpen om een aangepast rapport af te drukken
description: In dit onderwerp wordt uitgelegd hoe u een oplossing voor elektronische rapportering (ER) kunt ontwerpen om een aangepast rapport af te drukken.
author: NickSelin
ms.date: 08/10/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERParameters, ERDataModelDesigner, ERModelMappingTable, ERModelMappingDesigner, EROperationDesigner, ERVendorTable
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom:
- "220314"
- intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: af610ae86e751ec4425f4c555cdf59c042fabcdb46e6a3a018b0d94a8926d92e
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/05/2021
ms.locfileid: "6770063"
---
# <a name="design-a-new-er-solution-to-print-a-custom-report"></a>Een nieuwe ER-oplossing ontwerpen om een aangepast rapport af te drukken

[!include[banner](../includes/banner.md)]

In de volgende stappen wordt uitgelegd hoe een gebruiker in de rol van systeembeheerder, ER-ontwikkelaar of ER-consultant parameters van het ER-raamwerk kan configureren, de vereiste nieuwe configuraties van een nieuwe ER-oplossing kan ontwerpen om toegang te krijgen tot de gegevens van een bepaald bedrijfsdomein en een aangepast rapport in de Microsoft Office-indeling kan genereren. Deze stappen kunnen in het **USMF**-bedrijf worden uitgevoerd.

- [Het ER-raamwerk configureren](#ConfigureFramework)

    - [ER-parameters configureren](#ConfigureParameters)
    - [Een ER-configuratieprovider activeren](#ActivateProvider)

        - [De lijst met ER-configuratie providers bekijken](#ReviewProvidersList)
        - [Een nieuwe ER-configuratieprovider toevoegen](#AddProvider)
        - [Een ER-configuratieprovider activeren](#ActivateAddedProvider)

- [Domeinspecifiek gegevensmodel ontwerpen](#DesignModel)

    - [Een nieuwe gegevensmodelconfiguratie importeren](#ImportDataModel)
    - [Een nieuwe gegevensmodelconfiguratie maken](#DesignDataModel)

        - [Het gegevensmodel een naam geven](#NameDataModel)
        - [Gegevensmodelvelden toevoegen](#FieldsEntry)
        - [Het ontwerp van het gegevensmodel voltooien](#CompleteDataModel)

- [Een modeltoewijzing voor het geconfigureerde gegevensmodel ontwerpen](#DesignMapping)

    - [Een nieuwe configuratie voor de modeltoewijzing importeren](#ImportModelMapping)
    - [Een nieuwe configuratie voor de modeltoewijzing maken](#CreateModelMapping)

        - [Een nieuw modeltoewijzingsonderdeel ontwerpen](#DesignMappingComponent)
        - [Gegevensbronnen toevoegen voor toegang tot toepassingstabellen](#AddMmDataSource1)
        - [Gegevensbronnen toevoegen voor toegang tot toepassingsopsommingen](#AddMmDataSource2)
        - [ER-labels toevoegen om een rapport in een opgegeven taal te genereren](#AddMmLabels)
        - [Een gegevensbron toevoegen om de resultaten van het vergelijken van opsommingswaarden met een tekstwaarde te transformeren](#AddMmDataSource3)
        - [Gegevensbronnen binden aan gegevensmodelvelden](#AddMmBindings1)
        - [Het ontwerp van de modeltoewijzing voltooien](#CompleteModelMapping)

- [Een sjabloon voor een aangepast rapport ontwerpen](#DesignReportTemplate)
- [Een indeling ontwerpen](#DesignFormat)

    - [Een ontworpen indelingsconfiguratie importeren](#FormatImport)
    - [Een nieuwe indelingsconfiguratie maken](#FormatCreate)

        - [Een rapportsjabloon importeren](#ImportReportTemplate)
        - [Een indeling configureren](#ConfigureFormat)
        - [De gegevensbinding voor een rapporttitel definiëren](#DefineFormatBindings)
        - [De gegevensbron van het model controleren](#ReviewModelDataSource)
        - [Indelingselementen aan een gegevensbronvelden binden](#BindFormatElements)

    - [Een ontwerpindeling vanuit ER uitvoeren](#RunFormatFromER)

- [Een ontworpen indeling optimaliseren](#TuneFormat)

    - [Een opmaak wijzigen om de naam van een gegenereerd document te veranderen](#ModifyToChangeName)
    - [Een opmaak wijzigen om de volgorde van vragen te veranderen](#ModifyToOrder)
    - [Een gewijzigde indeling vanuit ER uitvoeren](#RunFormatFromER2)
    - [Het indelingsontwerp voltooien](#CompleteFormat)

- [Toepassingsartefacten ontwikkelen om het ontworpen rapport aan te roepen](#DevelopCustomCode)

    - [Broncode wijzigen](#ModifySourceCode)

        - [Een gegevenscontractklasse toevoegen](#DataContractClass)
        - [Een UI Builder-klasse toevoegen](#UIBuilderClass)
        - [Een gegevensproviderklasse toevoegen](#DataProviderClass)
        - [Een labelbestand toevoegen](#LabelsFile)
        - [Een serviceklasse voor een rapport toevoegen](#ServiceClass)
        - [Een controllerklasse voor een rapport toevoegen](#ControllerClass)
        - [Een menuopdracht toevoegen](#MenuItem)
        - [Een menuopdracht aan een menu toevoegen](#Menu)
        - [Een Visual Studio-project opbouwen](#BuildVSProject)

    - [Een indeling uit de toepassing uitvoeren](#RunFormatFromApp)

- [Een ontworpen ER-oplossing optimaliseren](#TuneSolution)

    - [Een modeltoewijzing wijzigen](#ModifyModelMapping)

        - [Gegevensbronnen toevoegen voor toegang tot een gegevenscontractobject](#AddDataSource1)
        - [Een gegevensbron toevoegen voor toegang tot toewijzingsrecords met een ER-indeling](#AddDataSource2)
        - [Een gegevensbron toevoegen voor toegang tot indelingstoewijzingsrecord van een actieve ER-indeling](#AddDataSource3)
        - [De naam van de actieve ER-indeling in het gegevensmodel invoeren](#AddBinding)
        - [Het ontwerp van de modeltoewijzing voltooien](#CompleteModelMapping2)

    - [Een indeling wijzigen](#ModifyFormat)

        - [Een nieuw opmaakelement toevoegen](#AddFormatElement)
        - [Het toegevoegde indelingselement binden](#BindAddedFormatElement)
        - [Het indelingsontwerp voltooien](#CompleteFormat2)

    - [Een indeling uit de toepassing uitvoeren](#RunFormatFromApp2)
    - [Een indeling vanuit ER uitvoeren](#RunFormatFromER3)
    - [Een indelingsbestemming configureren voor voorvertoning op het scherm](#ConfigureDestination)
    - [Een indeling van de toepassing uitvoeren voor voorvertoning als PDF-document](#RunFormatFromApp3)

- [Aanvullende bronnen](#References)

In dit voorbeeld maakt u een nieuwe ER-oplossing voor de module [Vragenlijst](../../../human-resources/hr-learning-questionnaires.md). Met deze nieuwe ER-oplossing kunt u een rapport ontwerpen met een Microsoft Excel-werkblad als sjabloon. U kunt het rapport **Vragenlijst** vervolgens genereren in Excel- of PDF-indeling, naast het bestaande SSRS-rapport (SQL Server Reporting Services). U kunt het nieuwe rapport ook later wijzigen op verzoek. U hoeft hiervoor geen code te schrijven.

1. Als u het bestaande rapport wilt uitvoeren, gaat u naar **Vragenlijst** \> **Ontwerpen** \> **Rapport vragenlijsten**.

    ![Het menu-item Rapport vragenlijsten selecteren in de module Vragenlijst om het bestaande SSRS-rapport uit te voeren.](./media/er-quick-start1-application-menu-origin.png)

2. Geef selectiecriteria op in het dialoogvenster **Rapport vragenlijsten**. Pas een filter toe zodat het rapport alleen de vragenlijst **SBCCrsExam** bevat.

    ![Selectiecriteria opgeven in het dialoogvenster Rapport vragenlijsten.](./media/er-quick-start1-ssrs-report-dialog.png)

In de volgende afbeelding ziet u de gegenereerde versie van het SSRS-rapport voor de vragenlijst **SBCCrsExam**.

![Gegenereerd SSRS-rapport.](./media/er-quick-start1-ssrs-report.png)

## <a name="configure-the-er-framework"></a><a name="ConfigureFramework"></a>Het ER-raamwerk configureren

Als u een gebruiker bent in de rol ER-ontwikkelaar, moet u de minimale set ER-parameters configureren voordat u het ER-framework kunt gaan gebruiken om een nieuwe ER-oplossing te ontwerpen.

### <a name="configure-er-parameters"></a><a name="ConfigureParameters"></a>ER-parameters configureren

1. Ga naar **Organisatiebeheer** \> **Werkgebieden** \> **Elektronische rapportage**.
2. Selecteer in de werkruimte **Elektronische rapportage** **Parameters van elektronische rapportage**.
3. Stel op de pagina **Parameters van elektronische rapportage** op het tabblad **Algemeen** de optie **Ontwerpmodus inschakelen** in op **Ja**.
4. Stel op het tabblad **Bijlagen** de volgende parameters in:

    - Stel het veld **Configuraties** in op **Bestand** voor het bedrijf **USMF**.
    - Stel de velden **Taakarchief**, **Tijdelijk**, **Basislijn** en **Overige** in op **Bestand**.

Meer informatie over het configureren van ER-parameters vindt u in [Het ER-raamwerk configureren](electronic-reporting-er-configure-parameters.md).

### <a name="activate-an-er-configuration-provider"></a><a name="ActivateProvider"></a>Een ER-configuratieprovider activeren

Elke ER-configuratie wordt gemarkeerd als het eigendom van een ER-configuratieprovider. Daarom moet u een ER-configuratieprovider activeren in de werkruimte **Elektronische rapportage** voordat u een ER-configuratie gaat toevoegen of bewerken.

> [!NOTE]
> Alleen de eigenaar van een ER-configuratie kan deze bewerken. Daarom moet een geschikte ER-configuratieprovider worden geactiveerd in de werkruimte **Elektronische rapportage**, voordat een ER-configuratie kan worden bewerkt.

#### <a name="review-the-list-of-er-configuration-providers"></a><a name="ReviewProvidersList"></a>De lijst met ER-configuratie providers bekijken

1. Ga naar **Organisatiebeheer** \> **Werkgebieden** \> **Elektronische rapportage**.
2. Selecteer in het werkgebied **Elektronische rapportage** in de sectie **Verwante koppelingen** de optie **Configuratieproviders**.
3. Op de pagina **Configuratieproviders** heeft elke providerrecord een unieke naam en een unieke URL. Bekijk de inhoud van deze pagina. Als er al een record bestaat voor **Litware, Inc.** (`https://www.litware.com`), kunt u de volgende procedure, [Een nieuwe ER-configuratieprovider toevoegen](#ActivateProvider), overslaan.

#### <a name="add-a-new-er-configuration-provider"></a><a name="AddProvider"></a>Een nieuwe ER-configuratieprovider toevoegen

1. Selecteer **Nieuw** op de pagina **Configuratieproviders**.
2. Voer in het veld **Naam** de tekst **Litware, Inc.** in.
3. Voer in het veld **Internetadres** de tekst `https://www.litware.com` in.
4. Selecteer **Opslaan**.

#### <a name="activate-an-er-configuration-provider"></a><a name="ActivateAddedProvider"></a>Een ER-configuratieprovider activeren

1. Ga naar **Organisatiebeheer** \> **Werkgebieden** \> **Elektronische rapportage**.
2. Selecteer in het werkgebied **Elektronische rapportage** de configuratieprovider **Litware, Inc.**.
3. Selecteer **Instellingen als actief**.

Meer informatie over ER-configuratieproviders vindt u in [Configuratieproviders maken en deze als actief markeren](tasks/er-configuration-provider-mark-it-active-2016-11.md).

## <a name="design-a-domain-specific-data-model"></a><a name="DesignModel"></a>Domeinspecifiek gegevensmodel ontwerpen

U moet een nieuwe ER-configuratie maken die een onderdeel met een [gegevensmodel](general-electronic-reporting.md#data-model-and-model-mapping-components) bevat voor het bedrijfsdomein **Vragenlijst**. Dit gegevensmodel wordt later gebruikt als gegevensbron wanneer u een ER-indeling ontwerpt om het rapport **Vragenlijst** te genereren.

Door de stappen in de sectie [Een nieuwe gegevensmodelconfiguratie importeren](#ImportDataModel) te voltooien, kunt u het vereiste gegevensmodel importeren uit het opgegeven XML-bestand. U kunt de stappen in de sectie [Een nieuwe gegevensmodelconfiguratie maken](#DesignDataModel) ook uitvoeren als u een helemaal nieuw gegevensmodel wilt ontwerpen.

### <a name="import-a-new-data-model-configuration"></a><a name="ImportDataModel"></a>Een nieuwe gegevensmodelconfiguratie importeren

1. Download het bestand [Questionnaires model.version.1.xml](https://download.microsoft.com/download/b/6/3/b633bd34-d200-4422-96d9-8f62eb5218f8/Questionnaires_model.version.1.xml) en sla het op uw lokale computer op.
2. Ga naar **Organisatiebeheer** \> **Werkgebieden** \> **Elektronische rapportage**.
3. Selecteer in het werkgebied **Elektronische rapportage** de optie **Rapportconfiguraties**.
4. In het actievenster selecteert u **Uitwisselen** \> **Laden uit XML-bestand**.
5. Selecteer **Bladeren** en zoek en selecteer het bestand **Questionnaires model.version.1.xml**.
6. Selecteer **OK** om de configuratie te importeren.

Als u wilt doorgaan, gaat u naar de volgende procedure [Een nieuwe gegevensmodelconfiguratie maken](#DesignDataModel).

### <a name="create-a-new-data-model-configuration"></a><a name="DesignDataModel"></a>Een nieuwe gegevensmodelconfiguratie maken

1. Ga naar **Organisatiebeheer** \> **Werkgebieden** \> **Elektronische rapportage**.
2. Selecteer in het werkgebied **Elektronische rapportage** de optie **Rapportconfiguraties**.
3. Selecteer **Configuratie maken**.
4. Voer in het vervolgkeuzemenu in het veld **Naam** **Vragenlijstmodel** in.
5. Selecteer **Configuratie maken** om de configuratie te maken.

#### <a name="name-the-data-model"></a><a name="NameDataModel"></a>Het gegevensmodel een naam geven

1. Selecteer op de pagina **Configuraties** in de structuur met configuraties **Vragenlijstmodel**.
2. Selecteer **Ontwerper**.
3. Voer op de pagina **Gegevensmodel ontwerpen** op het sneltabblad **Algemeen** in het veld **Naam** <a name="DataModeName"></a>**Vragenlijsten** in.

#### <a name="add-new-data-model-fields"></a><a name="FieldsEntry"></a>Nieuwe gegevensmodelvelden toevoegen

1. Selecteer **Nieuw** op de pagina **Gegevensmodel ontwerpen**.
2. Voer de volgende stappen uit in het vervolgkeuzemenu voor het toevoegen van een knooppunt voor een gegevensmodel:

    1. Selecteer **Modelbasis** als type voor het nieuwe knooppunt.
    2. Voer in het veld **Naam** <a name="RootDefinitionName"></a>**Basis** in.
    3. Selecteer **Toevoegen** om het nieuwe knooppunt toe te voegen.

    Deze basisdescriptor wordt gebruikt om gegevens voor het rapport **Vragenlijst** te leveren. Eén gegevensmodel kan meerdere descriptors hebben. Elke descriptor kan worden opgegeven voor één ER-indeling om gegevens te identificeren die nodig zijn om het rapport te genereren.

3. Selecteer nogmaals **Nieuw** en voer de volgende stappen uit in het vervolgkeuzemenu voor het toevoegen van een knooppunt voor een gegevensmodel:

    1. Selecteer **Onderliggende waarde van een actief knooppunt** als het type van het nieuwe knooppunt.
    2. Voer in het veld **Naam** **BedrijfsNaam** in.
    3. Selecteer in het veld **Itemtype** **Tekenreeks**.
    4. Selecteer **Toevoegen** om het nieuwe veld toe te voegen.

    Dit veld is vereist om de naam van het huidige bedrijf door te geven aan een ER-rapport waarin dit gegevensmodel wordt gebruikt als gegevensbron.

4. Selecteer nogmaals **Nieuw** en voer de volgende stappen uit in het vervolgkeuzemenu voor het toevoegen van een knooppunt voor een gegevensmodel:

    1. Selecteer **Onderliggende waarde van een actief knooppunt** als het type van het nieuwe knooppunt.
    2. Voer in het veld **Naam** **Vragenlijst** in.
    3. Selecteer in het veld **Itemtype** **Recordlijst**.
    4. Selecteer **Toevoegen** om het nieuwe veld toe te voegen.

    Dit veld is vereist om de lijst met vragenlijsten door te geven aan een ER-rapport waarin dit gegevensmodel wordt gebruikt als gegevensbron.

5. Selecteer het knooppunt **Vragenlijst**.
6. Voeg de vereiste velden van het bewerkbare gegevensmodel op dezelfde manier toe totdat u de volgende gegevensmodelstructuur hebt voltooid.

    | Veldpad                                                    | Gegevenstype   | Veldtoewijzing/geretourneerde waarde |
    |---------------------------------------------------------------|-------------|----------------------------------|
    | Hoofdmap                                                          |             | Het referentiepunt voor het aanvragen van vragenlijstgegevens. |
    | Root\\CompanyName                                             | Tekenreeks      | De naam van het huidige bedrijf. |
    | Root\\ExecutionContext                                        | Registreren      | Details voor uitvoering van de indeling. |
    | Root\\ExecutionContext\\FormatName                            | Tekenreeks      | De naam van de ER-indeling die wordt uitgevoerd. |
    | Root\\Questionnaire                                           | Recordlijst | De lijst met vragenlijsten |
    | Root\\Questionnaire\\Active                                   | Tekenreeks      | De status van de huidige vragenlijst. |
    | Root\\Questionnaire\\Code                                     | Tekenreeks      | De code van de huidige vragenlijst. |
    | Root\\Questionnaire\\Description                              | Tekenreeks      | De beschrijving van de huidige vragenlijst. |
    | Root\\Questionnaire\\QuestionnaireType                        | Tekenreeks      | Het type van de huidige vragenlijst. |
    | Root\\Questionnaire\\QuestionOrder                            | Tekenreeks      | De numerieke volgorde van de huidige vragenlijst. |
    | Root\\Questionnaire\\ResultsGroup                             | Registreren      | De resultaatparameters van de huidige vragenlijst. |
    | Root\\Questionnaire\\ResultsGroup\\Code                       | Tekenreeks      | De identificatiecode van de huidige resultaatgroep. |
    | Root\\Questionnaire\\ResultsGroup\\Description                | Tekenreeks      | De beschrijving van de huidige resultaatgroep. |
    | Root\\Questionnaire\\ResultsGroup\\MaxNumberOfPoints          | Real-modus        | Het maximumaantal punten dat kan worden verdiend. |
    | Root\\Questionnaire\\Question                                 | Recordlijst | De lijst met vragen voor de huidige vragenlijst. |
    | Root\\Questionnaire\\Question\\CollectionSequenceNumber       | Geheel getal     | Het volgnummer van de huidige antwoordverzameling. |
    | Root\\Questionnaire\\Question\\Id                             | Tekenreeks      | De identificatiecode van de huidige vraag. |
    | Root\\Questionnaire\\Question\\MustBeCompleted                | Tekenreeks      | Een markering die aangeeft of de huidige vraag moet worden beantwoord. |
    | Root\\Questionnaire\\Question\\PrimaryQuestion                | Tekenreeks      | Een markering die aangeeft of de huidige vraag primair is. |
    | Root\\Questionnaire\\Question\\SequenceNumber                 | Geheel getal     | Het volgnummer van de huidige vraag. |
    | Root\\Questionnaire\\Question\\Text                           | Tekenreeks      | De tekst van de huidige vraag. |
    | Root\\Questionnaire\\Question\\Answer                         | Recordlijst | De lijst met antwoorden voor de huidige vraag. |
    | Root\\Questionnaire\\Question\\Answer\\CorrectAnswer          | Tekenreeks      | Een markering die aangeeft of het huidige antwoord correct is. |
    | Root\\Questionnaire\\Question\\Answer\\Points                 | Real-modus        | De punten die worden verdiend wanneer het huidige antwoord wordt geselecteerd. |
    | Root\\Questionnaire\\Question\\Answer\\SequenceNumber         | Geheel getal     | Het volgnummer van het huidige antwoord. |
    | Root\\Questionnaire\\Question\\Answer\\Text                   | Tekenreeks      | De tekst van het huidige antwoord. |

    In de volgende afbeelding ziet u het voltooide bewerkbare gegevensmodel op de pagina **Gegevensmodel ontwerpen**.

    ![Het geconfigureerde gegevensmodel in de ER-gegevensmodelontwerper.](./media/er-quick-start1-model2.png)

7. Sla de wijzigingen op.
8. Sluit de pagina **Gegevensmodel ontwerpen**.

#### <a name="complete-the-design-of-the-data-model"></a><a name="CompleteDataModel"></a>Het ontwerp van het gegevensmodel voltooien

1. Ga naar **Organisatiebeheer** \> **Elektronische rapportage** \> **Configuraties**.
2. Selecteer op de pagina **Configuraties** in de structuur met configuraties **Vragenlijstmodel**.
3. Selecteer op het sneltabblad **Versies** de configuratieversie met de status **Concept**.
4. Selecteer **Status wijzigen** \> **Voltooien**.

De status van versie 1 van deze configuratie wordt gewijzigd van **Concept** in **Voltooid**. Versie 1 kan niet meer worden gewijzigd. Deze versie bevat het geconfigureerde gegevensmodel en kan worden gebruikt als basis voor andere ER-configuraties. Versie 2 van deze configuratie wordt gemaakt met de status **Concept**. U kunt deze versie bewerken om het gegevensmodel **Vragenlijst** aan te passen.

![Versies van de bewerkbare configuratie op de pagina Configuraties.](./media/er-quick-start1-model-configuration.png)

Zie [Overzicht van Elektronische rapporten (ER)](general-electronic-reporting.md#component-versioning) voor meer informatie over versiebeheer voor ER-configuraties.

> [!NOTE]
> Het geconfigureerde gegevensmodel is uw verkorte weergave van het bedrijfsdomein **Vragenlijst** en bevat geen relaties naar artefacten die specifiek zijn voor Microsoft Dynamics 365 Finance.

## <a name="design-a-model-mapping-for-the-configured-data-model"></a><a name="DesignMapping"></a>Een modeltoewijzing voor het geconfigureerde gegevensmodel ontwerpen

Als gebruiker in de rol van ER-ontwikkelaar moet u een nieuwe ER-configuratie maken die een [modeltoewijzings](general-electronic-reporting.md#data-model-and-model-mapping-components)onderdeel bevat voor het gegevensmodel **Vragenlijst**. Omdat dit onderdeel het geconfigureerde gegevensmodel implementeert voor Finance, is het Finance-specifiek. U moet het modeltoewijzingsonderdeel configureren om de toepassingsobjecten op te geven die moeten worden gebruikt voor het invullen met toepassingsgegevens van het geconfigureerde gegevensmodel tijdens runtime. Als u deze taak wilt voltooien, moet u zich bewust zijn van de implementatiedetails van de gegevensstructuur van het bedrijfsdomein van de **Vragenlijst** in Finance.

Door de stappen in de sectie [Een nieuwe modeltoewijzingsconfiguratie importeren](#ImportModelMapping) te voltooien, kunt u de vereiste modeltoewijzingsconfiguratie importeren uit het opgegeven XML-bestand. U kunt de stappen in de sectie [Een nieuwe modeltoewijzingsconfiguratie maken](#CreateModelMapping) ook uitvoeren als u een helemaal nieuwe modeltoewijzing wilt ontwerpen.

### <a name="import-a-new-model-mapping-configuration"></a><a name="ImportModelMapping"></a>Een nieuwe configuratie voor de modeltoewijzing importeren

1. Download het bestand [Questionnaires mapping.version.1.1.xml](https://download.microsoft.com/download/7/b/2/7b258e4e-4bd5-46a4-8114-27419ae4acd8/Questionnaires_mapping.version.1.1.xml) en sla het op uw lokale computer op.
2. Ga naar **Organisatiebeheer** \> **Werkgebieden** \> **Elektronische rapportage**.
3. Selecteer in het werkgebied **Elektronische rapportage** de optie **Rapportconfiguraties**.
4. In het actievenster selecteert u **Uitwisselen** \> **Laden uit XML-bestand**.
5. Selecteer **Bladeren** en zoek en selecteer het bestand **Questionnaires mapping.version.1.1.xml**.
6. Selecteer **OK** om de configuratie te importeren.

Als u wilt doorgaan, gaat u naar de volgende procedure [Een nieuwe configuratie voor de modeltoewijzing maken](#CreateModelMapping).

### <a name="create-a-new-model-mapping-configuration"></a><a name="CreateModelMapping"></a>Een nieuwe configuratie voor de modeltoewijzing maken

1. Ga naar **Organisatiebeheer** \> **Elektronische rapportage** \> **Configuraties**.
2. Selecteer op de pagina **Configuraties** in de structuur met configuraties **Vragenlijstmodel**.
3. Selecteer **Configuratie maken**.
4. Voer de volgende stappen uit in het dialoogvenster:

    1. Typ in het veld **Nieuw** **Modeltoewijzing gebaseerd op het gegevensmodel Questionnaires**.
    2. Voer in het veld **Naam** in **Questionnaires mapping**.
    3. Selecteer in het veld **Definitie gegevensmodel** de definitie **Root**.
    4. Selecteer **Configuratie maken** om de configuratie te maken.

#### <a name="design-a-new-model-mapping-component"></a><a name="DesignMappingComponent"></a>Een nieuw modeltoewijzingsonderdeel ontwerpen

1. Selecteer op de pagina **Configuraties** in de structuur met configuraties **Vragenlijsttoewijzing**.
2. Selecteer **Ontwerper** om de lijst met toewijzingen te openen.
3. Selecteer de toewijzing **Questionnaires mapping** die automatisch is toegevoegd voor de definitie **Root**
4. Selecteer **Ontwerper** om te beginnen met het configureren van de geselecteerde toewijzing.

Er wordt automatisch een nieuwe toewijzing toegevoegd voor de definitie **Root**. Deze toewijzing heeft de richting **Naar model**. Deze toewijzing kan dus worden gebruikt voor het invullen van een gegevensmodel met vereiste gegevens.

#### <a name="add-data-sources-to-access-application-tables"></a><a name="AddMmDataSource1"></a>Gegevensbronnen toevoegen voor toegang tot toepassingstabellen

U moet gegevensbronnen configureren om toegang te krijgen tot de toepassingstabellen die vragenlijstdetails bevatten.

1. Selecteer op de pagina **Ontwerper modeltoewijzing** in het deelvenster **Typen gegevensbronnen** **Dynamics 365 for Operations\\Tabelrecords**.
2. Voeg een nieuwe gegevensbron toe die wordt gebruikt om toegang te krijgen tot de tabel KMCollection, waarbij elke record één vragenlijst vertegenwoordigt:

    1. Selecteer **Basis toevoegen** in het deelvenster **Gegevensbronnen**.
    2. Voer in het dialoogvenster in het veld **Naam** de tekst **Vragenlijst** in.
    3. Voer in het veld **Tabel** **KMCollection** in.
    4. Stel de optie **Vragen om query** in op **Ja**. Tijdens runtime kunt u vervolgens [filter](../../fin-ops/get-started/advanced-filtering-query-options.md)opties voor deze tabel opgeven in het dialoogvenster voor de systeemquery.
    5. Klik op **OK** om de nieuwe gegevensbron toe te voegen.

3. Selecteer in het deelvenster **Typen gegevensbronnen** **Dynamics 365 for Operations\\Tabelrecords**.
4. Voeg een nieuwe gegevensbron toe die wordt gebruikt om toegang te krijgen tot de tabel KMQuestion, waarbij elke record één vraag in een vragenlijst vertegenwoordigt:

    1. Selecteer **Basis toevoegen** in het deelvenster **Gegevensbronnen**.
    2. Voer in het dialoogvenster in het veld **Naam** de tekst **Vraag** in.
    3. Voer in het veld **Tabel** **KMQuestion** in.
    4. Klik op **OK** om de nieuwe gegevensbron toe te voegen.

5. Selecteer in het deelvenster **Typen gegevensbronnen** **Dynamics 365 for Operations\\Tabelrecords**.
6. Voeg een nieuwe gegevensbron toe die wordt gebruikt om toegang te krijgen tot de tabel KMAnswer, waarbij elke record één antwoord op een vraag in een vragenlijst vertegenwoordigt:

    1. Selecteer **Basis toevoegen** in het deelvenster **Gegevensbronnen**.
    2. Voer in het veld **Naam** de tekst **Antwoord** in.
    3. Voer in het veld **Tabel** **KMAnswer** in.
    4. Klik op **OK** om de nieuwe gegevensbron toe te voegen.

7. Selecteer in het deelvenster **Typen gegevensbronnen** **Functies\\Berekend veld**.
8. Voeg een nieuw berekend veld toe dat wordt gebruikt om toegang te krijgen tot een record in de tabel KMQuestionResultGroup vanuit elke record van de bovenliggende KMCollection-tabel:

    1. Selecteer **Vragenlijst** in het deelvenster **Gegevensbronnen**.
    2. Selecteer **Toevoegen**.
    3. Voer in het dialoogvenster in het veld **Naam** **\$ResultGroup** in.
    4. Selecteer **Formule bewerken**.
    5. Voer in de [ER-formule-editor](general-electronic-reporting-formula-designer.md), in het veld **Formule**, **FIRSTORNULL(\@.'\<Relations'.KMQuestionResultGroup)** in om het [pad](er-formula-language.md#Paths) van de één-op-veel-relatie te gebruiken tussen de tabellen KMCollection en KMQuestionResultGroup.
    6. Selecteer **Opslaan** en sluit de formule-editor.
    7. Klik op **OK** om het nieuwe berekende veld toe te voegen.

9. Selecteer in het deelvenster **Typen gegevensbronnen** **Functies\\Berekend veld**.
10. Voeg een nieuw berekend veld toe dat wordt gebruikt om toegang te krijgen tot vraagrecords in de tabel KMQuestion vanuit elke record van de bovenliggende tabel KMCollectionQuestion:

    1. Selecteer **Vragenlijst** in het deelvenster **Gegevensbronnen**.
    2. Vouw het knooppunt **\<Relaties** uit dat één-op-veel-relaties bevat van de tabel KMCollection.
    3. Selecteer de gerelateerde tabel **KMCollectionQuestion** en selecteer vervolgens **Toevoegen**.
    4. Voer in het dialoogvenster in het veld **Naam** **\$Question** in.
    5. Selecteer **Formule bewerken**.
    6. Voer in de formule-editor, in het veld **Formule** **FIRSTORNULL (FILTER(Question, Question.kmQuestionId = \@.kmQuestionId))** in om de desbetreffende vraagrecords uit de tabel KMQuestion te retourneren..
    7. Selecteer **Opslaan** en sluit de formule-editor.
    8. Klik op **OK** om het nieuwe berekende veld toe te voegen.

11. Selecteer in het deelvenster **Typen gegevensbronnen** **Functies\\Berekend veld**.
12. Voeg een nieuw berekend veld toe dat wordt gebruikt om toegang te krijgen tot antwoordrecords in de tabel KMAnswer vanuit elke record van de bovenliggende tabel KMQuestion:

    1. Selecteer in het deelvenster **Gegevensbronnen** **Questionnaire.\<Relations.KMCollectionQuestion.\$Question**, en vervolgens **Toevoegen**.
    2. Voer in het dialoogvenster in het veld **Naam** **\$Answer** in.
    3. Selecteer **Formule bewerken**.
    4. Voer in de formule-editor, in het veld **Formule** **FILTER (Answer, Answer.kmAnswerCollectionId = \@.kmAnswerCollectionId)** in om de desbetreffende antwoordrecords uit de tabel KMAnswer te retourneren..
    5. Selecteer **Opslaan** en sluit de formule-editor.
    6. Klik op **OK** om het nieuwe berekende veld toe te voegen.

13. Selecteer in het deelvenster **Typen gegevensbronnen** **Dynamics 365 for Operations\\Tabel**.
14. Voeg een nieuwe gegevensbron toe die wordt gebruikt om toegang te krijgen tot methoden in de tabel CompanyInfo. De methode **find()** in deze tabel retourneert een record die een bedrijf vertegenwoordigt van het huidige Finance-exemplaar waarvoor deze toewijzing wordt aangeroepen.

    1. Selecteer **Basis toevoegen** in het deelvenster **Gegevensbronnen**.
    2. Voer in het dialoogvenster in het veld **Naam** **CompanyInfo** in.
    3. Voer in het veld **Tabel** **CompanyInfo** in.
    4. Klik op **OK** om de nieuwe gegevensbron toe te voegen.

#### <a name="add-data-sources-to-access-application-enumerations"></a><a name="AddMmDataSource2"></a>Gegevensbronnen toevoegen voor toegang tot toepassingsopsommingen

U moet gegevensbronnen configureren om toegang te krijgen tot toepassingsopsommingen en hun waarden te vergelijken met waarden van velden van het type **Opsomming** in de toepassingstabellen. U moet het resultaat van de vergelijking gebruiken om de relevante velden van het gegevensmodel in te vullen.

1. Selecteer op de pagina **Ontwerper modeltoewijzing** in het deelvenster **Typen gegevensbronnen** **Dynamics 365 for Operations\\Opsomming**.
2. Voeg een nieuwe gegevensbron toe die wordt gebruikt om toegang te krijgen tot waarden van de opsomming **EnumAppNoYes**:

    1. Selecteer **Basis toevoegen** in het deelvenster **Gegevensbronnen**.
    2. Voer in het dialoogvenster in het veld **Naam** **EnumAppNoYes** in.
    3. Voer in het veld **Opsomming** **NoYes** in.
    4. Klik op **OK** om de nieuwe gegevensbron toe te voegen.

3. Selecteer in het deelvenster **Typen gegevensbronnen** **Dynamics 365 for Operations\\Opsomming**.
4. Voeg een nieuwe gegevensbron toe die wordt gebruikt om toegang te krijgen tot de waarden van de opsomming **KMCollectionQuestionMode**:

    1. Selecteer **Basis toevoegen** in het deelvenster **Gegevensbronnen**.
    2. Voer in het dialoogvenster in het veld **Naam** **EnumAppQuestionOrder** in.
    3. Voer in het veld **Opsomming** **KMCollectionQuestionMode** in.
    4. Klik op **OK** om de nieuwe gegevensbron toe te voegen.

#### <a name="add-er-labels-to-generate-a-report-in-a-specified-language"></a><a name="AddMmLabels"></a>ER-labels toevoegen om een rapport in een opgegeven taal te genereren

U kunt ER-labels toevoegen om een aantal van uw gegevensbronnen te configureren voor het retourneren van waarden die afhankelijk zijn van de taal die is gedefinieerd in de context van het aanroepen van de modeltoewijzing.

1. Selecteer op de pagina **Ontwerper modeltoewijzing** in het deelvenster **Gegevensbronnen** de optie **Antwoord** en vervolgens **Bewerken**.
2. Activeer het veld **Label**.
3. Selecteer **Vertalen**.
4. Voer de volgende stappen uit in het dialoogvenster **Tekstvertaling**:

    1. Voer in het veld **Label-id** **PositiveAnswer** in.
    2. Voer in het veld **Tekst in standaardtaal** **Ja** in.
    3. Selecteer **Vertalen**.
    4. Voer in het veld **Label-id** **NegativeAnswer** in.
    5. Voer in het veld **Tekst in standaardtaal** **Nee** in.
    6. Selecteer **Vertalen**.

5. Sluit het dialoogvenster **Tekstvertaling**.
6. Selecteer **Annuleren**.

![ER-labels toevoegen voor de bewerkbare modeltoewijzing.](./media/er-quick-start1-adding-labels.png)

U hebt voor de standaardtaal alleen ER-labels ingevoerd. Zie [Meertalige rapporten ontwerpen](er-design-multilingual-reports.md) voor informatie over hoe ER-labels kunnen worden vertaald in andere talen.

#### <a name="add-a-data-source-to-transform-the-results-of-comparing-enumeration-values-to-a-text-value"></a><a name="AddMmDataSource3"></a>Een gegevensbron toevoegen om de resultaten van het vergelijken van opsommingswaarden met een tekstwaarde te transformeren

Omdat u de resultaten van de vergelijking tussen opsommingswaarden en tekstwaarden diverse keren moet omrekenen voor verschillen bronnen, is het een goed idee om deze logica als één gegevensbron te configureren. Als u deze gegevens bron herbruikbaar wilt maken, moet u deze vervolgens wel configureren als de gegevensbron met parameters. Zie [Ondersteuning bieden voor parameteraanroepen van ER-gegevensbronnen van het Berekende veld-type](er-calculated-field-type.md) voor meer informatie.

1. Selecteer op de pagina **Ontwerper modeltoewijzing** in het deelvenster **Typen gegevensbronnen** **Algemeen\\Lege container**.
2. Een nieuwe gegevensbron voor een container toevoegen:

    1. Selecteer **Basis toevoegen** in het deelvenster **Gegevensbronnen**.
    2. Voer in het dialoogvenster in het veld **Naam** de tekst **Helper** in.
    3. Klik op **OK** om de nieuwe gegevensbron voor de container toe te voegen.

3. Selecteer in het deelvenster **Typen gegevensbronnen** **Functies\\Berekend veld**.
4. Een nieuwe gegevensbron toevoegen:

    1. Selecteer **Helper** in het deelvenster **Gegevensbron**.
    2. Selecteer **Toevoegen**.
    3. Voer in het dialoogvenster in het veld **Naam** **NoYesEnumToString** in.
    4. Selecteer **Formule bewerken**.
    5. Selecteer in de formule-editor **Parameters**.
    6. Voer de volgende stappen uit om parameters op te geven voor de geconfigureerde expressie:

        1. Selecteer **Nieuw**.
        2. Voer in het dialoogvenster in het veld **Naam** de tekst **Argument** in.
        3. Selecteer in het veld **Type** het gegevenstype **Booleaans**.
        4. Selecteer **OK**.

    7. Voer in het veld **Formule** **IF (Argument = true, \@"GER\_LABEL:PositiveAnswer", \@"GER\_LABEL:NegativeAnswer")** om de tekst van het desbetreffende ER-label te retourneren, afhankelijk van de taal van de uitvoeringscontext en de waarde van de opgegeven parameter.
    8. Selecteer **Opslaan** en sluit de formule-editor.
    9. Klik op **OK** om de nieuwe gegevensbron toe te voegen.

![Geconfigureerde modeltoewijzing in de ER-ontwerper voor de modeltoewijzing.](./media/er-quick-start1-added-data-sources.png)

#### <a name="bind-data-sources-to-data-model-fields"></a><a name="AddMmBindings1"></a>Gegevensbronnen binden aan gegevensmodelvelden

U moet de geconfigureerde gegevensbronnen binden aan de velden van het gegevensmodel om op te geven hoe het gegevensmodel tijdens runtime moet worden gevuld met toepassingsgegevens.

1. Selecteer op de pagina **Ontwerper modeltoewijzing** in het deelvenster **Gegevensmodel** **CompanyName**.
2. Vouw **CompanyInfo** uit in het deelvenster **Gegevensbronnen** en voer vervolgens de volgende stappen uit:

    1. Vouw het knooppunt **CompanyInfo.find()** uit dat de methode **find()** van de tabel CompanyInfo vertegenwoordigt.
    2. Selecteer **CompanyInfo.find().Name**.
    3. Selecteer **Binden** om de naam van het bedrijf in te vullen waarvoor de geconfigureerde modeltoewijzing tijdens runtime wordt aangeroepen.

3. Selecteer **Vragenlijst** in het deelvenster **Gegevensmodel**.
4. Selecteer in het deelvenster **Gegevensbronnen** **Vragenlijst** en selecteer **Binden** om de vragenlijstrecords in te vullen.
5. Vouw **Vragenlijst** uit in het deelvenster **Gegevensmodel** en voer de volgende stappen uit:

    1. Selecteer **Actief** in het deelvenster **Gegevensmodel**.
    2. Selecteer **Bewerken** in het deelvenster **Gegevensmodel**.
    3. Voer in het veld **Formule** **Helper.NoYesEnumToString (\@.Active = EnumAppNoYes.Yes)** in om de tekstafhankelijke en taalafhankelijke resultaten van de vergelijking tussen opsommingswaarden te vullen.

6. Blijf de gegevensbronnen op dezelfde manier binden aan gegevensmodelvelden totdat u het volgende resultaat bereikt.

    | Veldpad                                              | Gegevenstype   | Actie | Bindingsexpressie |
    |---------------------------------------------------------|-------------|--------|--------------------|
    | CompanyName                                             | Tekenreeks      | Binden   | CompanyInfo.'find()'.Name |
    | Vragenlijst                                           | Recordlijst | Binden   | Vragenlijst |
    | Questionnaire\\Active                                   | Tekenreeks      | Bewerken   | Helper.NoYesEnumToString(\@.active = EnumAppNoYes.Yes) |
    | Questionnaire\\Code                                     | Tekenreeks      | Binden   | \@.kmCollectionId |
    | Questionnaire\\Description                              | Tekenreeks      | Binden   | \@.Description |
    | Questionnaire\\QuestionnaireType                        | Tekenreeks      | Binden   | \@.'&gt;Relations'.kmCollectionTypeId.Description |
    | Questionnaire\\QuestionOrder                            | Tekenreeks      | Bewerken   | CASE (\@.questionMode,<br>EnumAppQuestionOrder.Conditional, "Conditional",<br>EnumAppQuestionOrder.Random, "Random (percentage in questionnaire)",<br>EnumAppQuestionOrder.RandomGroup, "Random (percentage in result groups)",<br>EnumAppQuestionOrder.Sequence, "Sequential",<br>"") |
    | Questionnaire\\ResultsGroup                             | Registreren      |        | |
    | Questionnaire\\ResultsGroup\\Code                       | Tekenreeks      | Binden   | \@.'\$ResultGroup'.kmQuestionResultGroupId |
    | Questionnaire\\ResultsGroup\\Description                | Tekenreeks      | Binden   | \@.'\$ResultGroup'.description |
    | Questionnaire\\ResultsGroup\\MaxNumberOfPoints          | Real-modus        | Binden   | \@.'\$ResultGroup'.maxPoint |
    | Questionnaire\\Question                                 | Recordlijst | Binden   | \@.'&lt;Relations'.KMCollectionQuestion |
    | Questionnaire\\Question\\CollectionSequenceNumber       | Geheel getal     | Binden   | \@.answerCollectionSequenceNumber |
    | Questionnaire\\Question\\Id                             | Tekenreeks      | Binden   | \@.kmQuestionId |
    | Questionnaire\\Question\\MustBeCompleted                | Tekenreeks      | Bewerken   | Helper.NoYesEnumToString(\@.mandatory = EnumAppNoYes.Yes) |
    | Questionnaire\\Question\\PrimaryQuestion                | Tekenreeks      | Binden   | \@.parentQuestionId |
    | Questionnaire\\Question\\SequenceNumber                 | Geheel getal     | Binden   | \@.SequenceNumber |
    | Questionnaire\\Question\\Text                           | Tekenreeks      | Binden   | \@.'\$Question'.text |
    | Questionnaire\\Question\\Answer                         | Recordlijst | Binden   | \@.'\$Question'.'\$Answer' |
    | Questionnaire\\Question\\Answer\\CorrectAnswer          | Tekenreeks      | Bewerken   | Helper.NoYesEnumToString(\@.correctAnswer = EnumAppNoYes.Yes) |
    | Questionnaire\\Question\\Answer\\Points                 | Real-modus        | Binden   | \@.point |
    | Questionnaire\\Question\\Answer\\SequenceNumber         | Geheel getal     | Binden   | \@.sequenceNumber |
    | Questionnaire\\Question\\Answer\\Text                   | Tekenreeks      | Binden   | \@.text |

    In de volgende afbeelding wordt de eindstatus van de geconfigureerde modeltoewijzing weergegeven op de pagina **Ontwerper modeltoewijzing**.

    ![Volledig geconfigureerde modeltoewijzing in de ER-ontwerper voor de modeltoewijzing.](./media/er-quick-start1-mapping2.png)

7. Sla de wijzigingen op.
8. Sluit de pagina **Ontwerper modeltoewijzing**.

#### <a name="complete-the-design-of-the-model-mapping"></a><a name="CompleteModelMapping"></a>Het ontwerp van de modeltoewijzing voltooien

1. Ga naar **Organisatiebeheer** \> **Elektronische rapportage** \> **Configuraties**.
2. Selecteer op de pagina **Configuraties** in de structuur met configuraties **Vragenlijsttoewijzing**.
3. Selecteer op het sneltabblad **Versies** de configuratieversie met de status **Concept**.
4. Selecteer **Status wijzigen** \> **Voltooien**.

De status van versie 1.1 van deze configuratie wordt gewijzigd van **Concept** in **Voltooid**. Versie 1.1 kan niet meer worden gewijzigd. Deze versie bevat de geconfigureerde modeltoewijzing en kan worden gebruikt als basis voor andere ER-configuraties. Versie 1.2 van deze configuratie wordt gemaakt met de status **Concept**. U kunt deze versie bewerken om de configuratie **Vragenlijsttoewijzing** aan te passen.

![Versies van de bewerkbare ER-configuratie op de pagina Configuraties.](./media/er-quick-start1-mapping-configuration.png)

> [!NOTE]
> De geconfigureerde modeltoewijzing is uw Finance-specifieke implementatie van het abstracte gegevensmodel dat het bedrijfsdomein **Vragenlijst** vertegenwoordigt.

## <a name="design-a-template-for-a-custom-report"></a><a name="DesignReportTemplate"></a>Een sjabloon voor een aangepast rapport ontwerpen

Het ER-raamwerk gebruikt vooraf gedefinieerde sjablonen om rapporten te genereren in Microsoft Office-indelingen (Excel-werkmappen of Word-documenten). Terwijl het vereiste rapport wordt gegenereerd, wordt een sjabloon gevuld met vereiste gegevens volgens de geconfigureerde gegevensstroom. Daarom moet u eerst een sjabloon voor uw aangepaste rapport ontwerpen. Deze sjabloon moet zijn ontworpen als een Excel-werkmap, waarvan de structuur de indeling van een aangepast rapport vertegenwoordigt. U moet elk Excel-item dat u wilt invullen met vereiste gegevens, een naam geven.

1. Download het bestand [Questionnaires report template.xlsx](https://download.microsoft.com/download/3/8/2/382c3cf0-87bb-473f-b7bb-3015b4facb74/Questionnaires_report_template.xlsx) en sla het op uw lokale computer op.
2. Open het bestand in Excel en bekijk de structuur van de werkmap.

Zoals in de volgende afbeelding wordt weergegeven, is de gedownloade sjabloon ontworpen voor het afdrukken van opgegeven vragenlijsten waarin de vragen van een vragenlijst en de juiste antwoorden worden weergegeven.

![Excel-sjabloon voor het afdrukken van opgegeven vragenlijsten.](./media/er-quick-start1-template-layout.png)

Er zijn Excel-namen aan deze sjabloon toegevoegd om de details van de vragenlijst in te vullen. U kunt Naambeheer gebruiken om de Excel-namen te controleren.

![Naambeheer gebruiken om Excel-namen te controleren in de opgegeven Excel-sjabloon.](./media/er-quick-start1-template-names.png)

Er zijn rapportlabels toegevoegd als vaste tekst in de Engelse taal. U kunt de rapportlabels vervangen door nieuwe Excel-namen waarmee de labels worden ingevuld met taalafhankelijke tekst door gebruik te maken van ER-opmaak[labels](#AddMmLabels) te gebruiken, zoals u ook hebt gedaan voor taalafhankelijke expressies in de geconfigureerde modeltoewijzing. In dit geval moeten ER-labels worden toegevoegd in de bewerkbare ER-indeling.

Zoals u in de volgende afbeelding kunt zien, is de aangepaste rapportkoptekst opgegeven zodat het pagineren in Excel mogelijk is.

![Aangepaste rapportkoptekst in de opgegeven Excel-sjabloon.](./media/er-quick-start1-template-header.png)

## <a name="design-a-format"></a><a name="DesignFormat"></a>Een indeling ontwerpen

Als gebruiker in de rol van ER-functieconsultant moet u een nieuwe configuratie maken die een [indeling](general-electronic-reporting.md#FormatComponentOutbound)sonderdeel bevat. U moet het indelingsonderdeel configureren om op te geven hoe een rapportsjabloon tijdens runtime met vereiste gegevens wordt ingevuld.

Door de stappen in de sectie [Een ontworpen indelingsconfiguratie importeren](#FormatImport) te voltooien, kunt u de vereiste indeling importeren uit het opgegeven XML-bestand. U kunt de stappen in de sectie [Een nieuwe indelingsconfiguratie maken](#FormatCreate) ook uitvoeren als u een helemaal nieuwe indeling wilt ontwerpen.

### <a name="import-a-designed-format-configuration"></a><a name="FormatImport"></a>Een ontworpen indelingsconfiguratie importeren

1. Download het bestand [Questionnaires format.version.1.1.xml](https://download.microsoft.com/download/1/b/a/1ba39ec2-257a-44d8-972f-25bf7d18fb41/Questionnaires_format.version.1.1.xml) en sla het op uw lokale computer op.
2. Ga naar **Organisatiebeheer** \> **Werkgebieden** \> **Elektronische rapportage**.
3. Selecteer in het werkgebied **Elektronische rapportage** de optie **Rapportconfiguraties**.
4. In het actievenster selecteert u **Uitwisselen** \> **Laden uit XML-bestand**.
5. Selecteer **Bladeren** en zoek en selecteer het bestand **Questionnaires format.version.1.1.xml**.
6. Selecteer **OK** om de configuratie te importeren.

Als u wilt doorgaan, gaat u naar de volgende procedure [Een nieuwe indelingsconfiguratie maken](#FormatCreate).

### <a name="create-a-new-format-configuration"></a><a name="FormatCreate"></a>Een nieuwe indelingsconfiguratie maken
 
1. Ga naar **Organisatiebeheer** \> **Elektronische rapportage** \> **Configuraties**.
2. Selecteer op de pagina **Configuraties** in de structuur met configuraties **Vragenlijstmodel**.
3. Selecteer **Configuratie maken**.
4. Voer de volgende stappen uit in het dialoogvenster:

    1. Typ in het veld **Nieuw** **Indeling gebaseerd op het gegevensmodel Questionnaires**.
    2. Voer in het veld **Naam** in **Vragenlijstrapport**.
    3. Selecteer **1** in het veld **Versie gegevensmodel**.

        > [!NOTE]
        > - Als u een specifieke versie van het basisgegevensmodel selecteert, wordt de structuur van de bijbehorende versie van het gegevensmodel weergegeven als de structuur van de **model** gegevensbron in de indeling die wordt gemaakt.
        > - U kunt dit veld leeg laten. In dat geval wordt de structuur van de **concept** versie van het gegevensmodel weergegeven als de structuur van de **model** gegevensbron in de indeling die wordt gemaakt. U kunt vervolgens uw model aanpassen en de aanpassingen onmiddellijk in uw indeling bekijken. Deze benadering kan efficiënter werken voor het onderwerp van de ER-oplossing wanneer u het gegevensmodel, de modeltoewijzing en de indeling tegelijk configureert.
        > - Als u een specifieke versie van het basisgegevensmodel selecteert, kunt u later overschakelen naar de **concept** versie, wanneer u begint met het bewerken van een indeling.

    4. Selecteer in het veld **Definitie gegevensmodel** de definitie **Root**.

5. Selecteer **Configuratie maken** om de configuratie te maken.

#### <a name="import-a-report-template"></a><a name="ImportReportTemplate"></a>Een rapportsjabloon importeren

1. Selecteer op de pagina **Configuraties** in de structuur met configuraties **Vragenlijstrapport**.
2. Selecteer **Ontwerper** als u een aangepaste indeling wilt configureren.
3. Selecteer op de pagina **Indelingsontwerper** in het actievenster de optie **Importeren** \> **Importeren uit Excel**.
4. Voer de volgende stappen uit in het dialoogvenster:

    1. Selecteer **Sjabloon toevoegen**.
    2. Zoek en selecteer het lokaal opgeslagen bestand **Questionnaires report template.xslx** en selecteer **Openen**.
    3. Selecteer **OK** om de sjabloon te importeren.

    ![Een rapportsjabloon importeren.](./media/er-quick-start1-template-import.png)

Het indelingselement **Excel\\File** wordt automatisch aan de bewerkbare indeling toegevoegd als hoofdelement. Bovendien wordt het indelingselement **Excel\\Range** of het indelingselement **Excel\\Cell** automatisch toegevoegd voor elke herkende Excel-naam van de geïmporteerde sjabloon. De indeling **Excel\\Header** met het geneste element **Tekenreeks** wordt automatisch toegevoegd om de koptekstinstellingen van de geïmporteerde sjabloon te weerspiegelen.

![Indelingsstructuur die automatisch toegevoegde elementen bevat in de ER Operation-ontwerper.](./media/er-quick-start1-template-import2.png)

#### <a name="configure-a-format"></a><a name="ConfigureFormat"></a>Een indeling configureren

1. Selecteer op de pagina **Indelingsontwerper** in de indelingsstructuur het hoofdelement **Excel**.
2. Voer op het tabblad **Indeling** aan de rechterkant van de pagina in het veld **Naam** <a name="AddFormatRootElement"></a>**Rapport** in.
3. Selecteer in het veld **Taalvoorkeur** de optie **Gebruikersvoorkeur** om het rapport uit te voeren in de voorkeurstaal van de gebruiker.
4. Selecteer in het veld **Cultuurvoorkeur** de optie **Gebruikersvoorkeur** om het rapport uit te voeren in de voorkeurscultuur van de gebruiker.

    Zie [Meertalige rapporten ontwerpen](er-design-multilingual-reports.md) voor informatie over het opgeven van de taal- en cultuurcontexten voor een ER-proces.

    ![Taal- en cultuurinstellingen voor het ontworpen rapport configureren in de ER Operation-ontwerper.](./media/er-quick-start1-template-format-structure1.png)

5. Vouw in de indelingsstructuur het hoofdknooppunt uit en selecteer **ResultsGroup**.
6. Selecteer op het tabblad **Indeling** in het veld **Replicatierichting** de optie **Geen replicatie**, omdat u niet meerdere resultaatgroepen voor één vragenlijst verwacht.

    ![De replicatierichting definiëren voor elementen in de indeling Range van ER Operation-ontwerper.](./media/er-quick-start1-template-format-structure2.png)

7. Selecteer **Opslaan**.

#### <a name="define-the-data-binding-for-a-report-title"></a><a name="DefineFormatBindings"></a>De gegevensbinding voor een rapporttitel definiëren

U moet een gegevensbinding opgeven voor een opmaakelement dat wordt gebruikt om de titel van een gegenereerd rapport in te vullen.

1. Selecteer op de pagina **Indelingsontwerper** op het tabblad **Toewijzing** aan de rechterkant het element **Report\\ReportTitle**.
2. Selecteer **Formule bewerken**.
3. Selecteer in de formule-editor **Vertalen**.
4. Voer de volgende stappen uit in het dialoogvenster **Tekstvertaling**:

    1. Voer in het veld **Label-id** **ReportTitle** in.
    2. Voer in het veld **Tekst in standaardtaal** de tekst **Questionnaires report** in.
    3. Selecteer **Vertalen** en vervolgens **Opslaan**.
    4. Selecteer **Vertalen** om het dialoogvenster **Tekstvertaling** te sluiten.

5. Sluit de Formule-editor.

    ![De binding configureren om de titel van een gegenereerd rapport in te vullen.](./media/er-quick-start1-add-report-title-label.png)

Met deze techniek kunt u alle andere labels van de huidige sjabloon taalafhankelijk maken. Zie [Meertalige rapporten ontwerpen](er-design-multilingual-reports.md) voor informatie over hoe de toegevoegde labels van één ER-configuratie kunnen worden vertaald in alle ondersteunde talen.

#### <a name="review-model-data-source"></a><a name="ReviewModelDataSource"></a>De gegevensbron van het model controleren

1. Selecteer op de pagina **Indelingsontwerper** op het tabblad **Toewijzing** de <a name="ModelDSName"></a>**model** gegevensbron die het basisgegevensmodel van deze ER-indeling vertegenwoordigt.
2. Selecteer **Bewerken**.
3. Controleer de gegevens in het dialoogvenster **Eigenschappen gegevensbron**. Deze gegevensbron vertegenwoordigt versie 1 van het gegevensmodelonderdeel **Vragenlijsten** dat zich bevindt in de ER-configuratie **Model vragenlijst**.

![Eigenschappen van de modelgegevensbron in de ER Operation-ontwerper.](./media/er-quick-start1-model-data-source.png)

#### <a name="bind-format-elements-to-data-source-fields"></a><a name="BindFormatElements"></a>Indelingselementen aan een gegevensbronvelden binden

Als u wilt opgeven hoe een sjabloon tijdens runtime moet worden ingevuld, moet u elk indelingselement dat aan een geschikte Excel-naam is gekoppeld, binden aan één veld in de gegevensbron van deze indeling.

1. Selecteer op de pagina **Indelingsontwerper** in de indelingsstructuur het indelingselement **Report\\CompanyName**.
2. Selecteer op het tabblad **Toewijzing** het gegevensbronveld **model.CompanyName** van het type **Tekenreeks**.
3. Selecteer **Binden** om een bedrijfsnaam in een sjabloon in te voeren.
4. Selecteer in de indelingsstructuur het element **Report\\Questionnaire**.
5. Selecteer op het tabblad **Toewijzing** het gegevensbronveld **model.Questionnaire** van het type **Recordlijst**.
6. Selecteer **Binden**.
7. Selecteer **Details weergeven** als u meer details voor indelingselementen wilt weergeven.

    Het indelingselement voor het bereik **Vragenlijst** is geconfigureerd als verticaal gerepliceerd. Wanneer het is gebonden aan een gegevensbron van het type **Recordlijst**, wordt het desbetreffende bereik **Vragenlijst** van de Excel-sjabloon herhaald voor elke record van de gebonden gegevensbron.
 
    ![Het indelingselement voor het bereik Vragenlijst binden aan de betreffende Recordlijst-gegevens bronnen in de ER Operation-ontwerper.](./media/er-quick-start1-bindings1.png)

    Aangezien het bereik **Vragenlijst** van de Excel-sjabloon is gedefinieerd tussen de rijen 5 tot en met 14, worden deze rijen herhaald voor elke gerapporteerde vragenlijst.

    ![Rijen in de Excel-sjabloon die in een gegenereerd rapport worden herhaald voor elke record van de Recordlijst-gegevensbronnen.](./media/er-quick-start1-template-questionnaire-range.png)

8. Configureer vergelijkbare bindingen voor de resterende indelingselementen, zoals wordt beschreven in de volgende tabel.

    > [!NOTE]
    > In deze tabel wordt voor de informatie in de kolom "Pad naar gegevensbron" aangenomen dat ER-functie voor het [relatieve pad](relative-path-data-bindings-er-models-format.md) is ingeschakeld.

    | Pad van indelingselement                                      | Pad naar gegevensbron |
    |----------------------------------------------------------|------------------|
    | Excel\\ReportTitle                                       | **\@"GER\_LABEL:ReportTitle"** |
    | Excel\\CompanyName                                       | **model.CompanyName** |
    | Excel\\Questionnaire                                     | **model.Questionnaire** |
    | Excel\\Questionnaire\\Active                             | **\@.Active**, waar **\@** is **model.Questionnaire** |
    | Excel\\Questionnaire\\Code                               | **\@.Code** |
    | Excel\\Questionnaire\\Description                        | **\@.Description** |
    | Excel\\Questionnaire\\QuestionnaireType                  | **\@.QuestionnaireType** |
    | Excel\\Questionnaire\\QuestionOrder                      | **\@.QuestionOrder** |
    | Excel\\Questionnaire\\ResultsGroup\\Code\_               | **\@.ResultsGroup.Code** |
    | Excel\\Questionnaire\\ResultsGroup\\Description\_        | **\@.ResultsGroup.Description** |
    | Excel\\Questionnaire\\ResultsGroup\\MaxNumberOfPoints    | **\@.ResultsGroup.MaxNumberOfPoint** |
    | Excel\\Questionnaire\\Question                           | **\@.Question** |
    | Excel\\Questionnaire\\Question\\CollectionSequenceNumber | **\@.CollectionSequenceNumber**, waar **\@** is **model.Questionnaire.Question** |
    | Excel\\Questionnaire\\Question\\Id                       | **\@.Id** |
    | Excel\\Questionnaire\\Question\\MustBeCompleted          | **\@.MustBeCompleted** |
    | Excel\\Questionnaire\\Question\\PrimaryQuestion          | **\@.PrimaryQuestion** |
    | Excel\\Questionnaire\\Question\\SequenceNumber           | **\@.SequenceNumber** |
    | Excel\\Questionnaire\\Question\\Text                     | **\@.Text** |
    | Excel\\Questionnaire\\Question\\Answer                   | **\@.Answer** |
    | Excel\\Questionnaire\\Question\\Answer\\CorrectAnswer    | **\@.CorrectAnswer**, waar **\@** is **model.Questionnaire.Answer** |
    | Excel\\Questionnaire\\Question\\Answer\\Points           | **\@.Points** |
    | Excel\\Questionnaire\\Question\\Answer\\Text             | **\@.Text** |

9. Wanneer u klaar bent, selecteert u **Opslaan**.

In de volgende afbeelding wordt de eindstatus van de geconfigureerde gegevensbindingen weergegeven op de pagina **Indelingsontwerper**.

![Geconfigureerde gegevensbindingen in de ER Operation-ontwerper.](./media/er-quick-start1-bindings2.png)

> [!IMPORTANT]
> De hele verzameling met opgegeven gegevensbronnen en bindingen vertegenwoordigt een opmaaktoewijzingsonderdeel van de geconfigureerde indeling. Deze indelingstoewijzing wordt aangeroepen wanneer u de geconfigureerde indeling voor het genereren van rapporten uitvoert.

### <a name="run-a-designed-format-from-er"></a><a name="RunFormatFromER"></a>Een ontwerpindeling vanuit ER uitvoeren

U kunt nu een ontworpen indeling voor testdoeleinden uitvoeren vanaf de pagina **Configuraties**.

1. Ga naar **Organisatiebeheer** \> **Elektronische rapportage** \> **Configuraties**.
2. Vouw op de pagina **Configuratie** in de configuratiestructuur **Vragenlijstmodel** uit en selecteer **Vragenlijstrapport**.
3. Selecteer **Ontwerper** voor de indelingsversie met de status **Concept**.
4. Selecteer **Uitvoeren** op de pagina **Indelingsontwerper**.
5. Configureer in het dialoogvenster **ER-parameters** op het sneltabblad **Op te nemen records** de filteroptie zo dat alleen de vragenlijst **SBCCrsExam** wordt opgenomen.
6. Selecteer **OK** om de filteroptie te bevestigen.
7. Selecteer **OK** om het rapport uit te voeren.
8. Controleer het gegenereerde rapport.

[Standaard](electronic-reporting-destinations.md#default-behavior) wordt een gegenereerd rapport afgeleverd als een Excel-bestand dat u kunt downloaden. In de volgende afbeeldingen worden twee pagina's van het gegenereerde rapport in Excel-indeling weergegeven.

![Voorbeeld van een gegenereerd rapport in Excel-indeling, pagina 1.](./media/er-quick-start1-report1a.png)

![Voorbeeld van een gegenereerd rapport in Excel-indeling, pagina 2.](./media/er-quick-start1-report1b.png)

## <a name="tune-a-designed-format"></a><a name="TuneFormat"></a>Een ontworpen indeling optimaliseren

### <a name="modify-a-format-to-change-the-name-of-a-generated-document"></a><a name="ModifyToChangeName"></a>Een opmaak wijzigen om de naam van een gegenereerd document te veranderen

Standaard krijgt een gegenereerd document een naam met behulp van de alias van de huidige gebruiker. Als u de indeling wijzigt, kunt u dit gedrag wijzigen zodat een gegenereerd document een naam krijgt op basis van uw aangepaste logica. De naam van een gegenereerd document kan bijvoorbeeld zijn gebaseerd op de huidige sessiedatum en -tijd en op de titel van het rapport.

1. Ga naar de pagina **Indelingsontwerper** en selecteer het basisitem **Rapport**.
2. Selecteer op het tabblad **Toewijzing** de optie **Bestandsnaam bewerken**.
3. Voer in het veld **Formule** **CONCATENATE (\@"GER\_LABEL:ReportTitle", " - ", DATETIMEFORMAT(SESSIONNOW(), "yyyy-MM-dd hh-mm-ss"))** in.
4. Selecteer **Opslaan** en sluit de formule-editor.
5. Selecteer **Opslaan**.

### <a name="modify-a-format-to-change-the-order-of-questions"></a><a name="ModifyToOrder"></a>Een opmaak wijzigen om de volgorde van vragen te veranderen

De vragen hebben niet de juiste volgorde in een gegenereerd rapport. U kunt de volgorde wijzigen door de indeling te wijzigen.

1. Ga naar de pagina **Indelingsontwerper** en selecteer het basisitem **Rapport**.
2. Vouw op het tabblad **Toewijzing** in de indelingsstructuur **Report\\Questionnaire\\Question** uit.

    ![Vraagindelingselement van het type Bereik in de ER Operation-ontwerper.](./media/er-quick-start1-bindings3.png)

3. Selecteer op het tabblad **Toewijzing** de optie **model.Questionnaire**.
4. Selecteer **Toevoegen** \> **Functies\\Berekend veld**, en voer in het veld **Naam** **OrderedQuestions** in.
5. Selecteer **Formule bewerken**.
6. Voer in de formule-editor in het veld **Formule** **ORDERBY (model.Questionnaire.Question, model.Questionnaire.Question.SequenceNumber)** in om de lijst met vragen van de huidige vragenlijst te ordenen op volgnummer.
7. Selecteer **Opslaan** en sluit de formule-editor.
8. Selecteer **OK** om de invoer van een nieuw berekend veld te voltooien.
9. Selecteer op het tabblad **Toewijzing** de optie **model.Questionnaire.OrderedQuestions**.
10. Selecteer in de indelingsstructuur **Excel\\Questionnaire\\Question**.
11. Selecteer **Binden** en bevestig vervolgens dat het huidige pad **model.Questionnaire.Questions** wordt vervangen door het nieuwe pad **model.Questionnaire. OrderedQuestions** pad in alle bindingen van de geneste elementen.
12. Selecteer **Opslaan**.

![Het indelingselement Vraag binden aan de geconfigureerde gegevensbron OrderedQuestions in de ER Operation-ontwerper.](./media/er-quick-start1-bindings4.png)

### <a name="run-a-modified-format-from-er"></a><a name="RunFormatFromER2"></a>Een gewijzigde indeling vanuit ER uitvoeren

U kunt nu een aangepaste indeling voor testdoeleinden uitvoeren vanuit het ER-raamwerk.

1. Selecteer **Uitvoeren** op de pagina **Indelingsontwerper**.
2. Configureer in het dialoogvenster **ER-parameters** op het sneltabblad **Op te nemen records** de filteroptie zo dat alleen de vragenlijst **SBCCrsExam** wordt opgenomen.
3. Selecteer **OK** om de filteroptie te bevestigen.
4. Selecteer **OK** om het rapport uit te voeren.
5. Controleer het gegenereerde rapport.

In de volgende afbeelding ziet u een gegenereerd rapport in Excel-indeling waarin de vragen op de juiste manier zijn geordend.

![Gegenereerd rapport in Excel-indeling met correct geordende vragen.](./media/er-quick-start1-report2.png)

### <a name="complete-the-format-design"></a><a name="CompleteFormat"></a>Het indelingsontwerp voltooien

1. Ga naar **Organisatiebeheer** \> **Elektronische rapportage** \> **Configuraties**.
2. Vouw op de pagina **Configuraties** in de configuratiestructuur **Vragenlijstmodel** uit en selecteer **Vragenlijstrapport**.
3. Selecteer op het sneltabblad **Versies** de configuratieversie met de status **Concept**.
4. Selecteer **Status wijzigen** \> **Voltooien**.

De status van versie 1.1 van deze configuratie wordt gewijzigd van **Concept** in **Voltooid**. Versie 1.1 kan niet meer worden gewijzigd. Deze versie bevat de geconfigureerde indeling en kan worden gebruikt om het aangepaste rapport af te drukken. Versie 1.2 van deze configuratie wordt gemaakt met de status **Concept**. U kunt deze versie bewerken om de indeling van uw **Vragenlijst** rapport aan te passen.

![Bewerkbare ER-configuratie op de pagina Configuraties.](./media/er-quick-start1-format-configuration.png)

> [!NOTE]
> De geconfigureerde indeling is uw ontwerp van het rapport **Vragenlijst** en bevat geen relaties met de specifieke Finance-artefacten.

## <a name="develop-application-artefacts-to-call-the-designed-report"></a><a name="DevelopCustomCode"></a>Toepassingsartefacten ontwikkelen om het ontworpen rapport aan te roepen

Als gebruiker met de rol systeembeheerder moet u nieuwe logica ontwikkelen, zodat de geconfigureerde ER-indeling kan worden aangeroepen vanuit de gebruikersinterface van de toepassing om uw aangepaste rapport te genereren. Er is momenteel geen mogelijkheid om dit type logica te configureren. Daarom zijn technische aanpassingen vereist. 

Als u nieuwe logica wilt ontwikkelen, moet u een topologie implementeren die ondersteuning biedt voor continu bouwvoorzieningen. Zie [Topologieën implementeren die ondersteuning bieden voor continue bouw- en testautomatisering](../perf-test/continuous-build-test-automation.md) voor meer informatie. U moet ook toegang hebben tot de ontwikkelomgeving voor deze topologie. Meer informatie over de beschikbare ER-API vindt u in [API ER-raamwerk](er-apis-app73.md).

### <a name="modify-source-code"></a><a name="ModifySourceCode"></a>Broncode wijzigen

#### <a name="add-a-data-contract-class"></a><a name="DataContractClass"></a>Een gegevenscontractklasse toevoegen

Voeg de nieuwe klasse **QuestionnairesErReportContract** toe aan uw Microsoft Visual Studio-project en schrijf de code waarin wordt aangegeven welk gegevenscontract moet worden gebruikt om de geconfigureerde ER-indeling uit te voeren.

```xpp
/// <summary>
///     This class is the data contract class for the <c>QuestionnairesErReportDP</c> class.
/// </summary>
/// <remarks>
///    This is the data contract class for the Questionnaires ER report.
/// </remarks>
[
    DataContractAttribute,
    SysOperationContractProcessingAttribute(classStr(QuestionnairesErReportUIBuilder))
    ]
    public class QuestionnairesErReportContract extends ERFormatMappingRunBaseContract implements SysOperationValidatable
{
    ERFormatMappingId formatMapping;

    /// <summary>
    ///    Validates the report parameters.
    /// </summary>
    /// <returns>
    ///    true if no errors; otherwise, false.
    /// </returns>
    public boolean validate()
    {
        boolean ret = true;
        if (!formatMapping)
        {
            ret = checkFailed(strFmt("@SYS26332", new SysDictType(extendedTypeNum(ERFormatMappingId)).label()));
        }
        return ret;
    }
    [
        DataMemberAttribute('FormatMapping'),
        SysOperationLabelAttribute(literalstr("@ElectronicReporting:FormatMapping")),
        SysOperationHelpTextAttribute(literalstr("@ElectronicReporting:FormatMapping"))
    ]
    public ERFormatMappingId parmFormatMapping(ERFormatMappingId _formatMapping = formatMapping)
    {
        formatMapping = _formatMapping;
        return formatMapping;
    }
}
```

#### <a name="add-a-ui-builder-class"></a><a name="UIBuilderClass"></a>Een UI Builder-klasse toevoegen

Voeg de nieuwe klasse **QuestionnairesErReportUIBuilder** toe aan uw Visual Studio-project en schrijf code om een runtime-dialoogvenster te genereren waarin wordt gezocht naar de indelingstoewijzings-id van de ER-indeling die moet worden uitgevoerd. Met de opgegeven code wordt alleen gezocht naar ER-indelingen die een gegevensbron bevatten van het type **gegevensmodel** dat verwijst naar het gegevensmodel **[Vragenlijsten](#DataModeName)** met behulp van de **[basis](#RootDefinitionName)** definitie.

> [!NOTE]
> U kunt ook ER-integratiepunten gebruiken om ER-indelingen te filteren. Zie [API voor het weergeven van een zoekactie voor indelingstoewijzingen](er-apis-app10-0-11.md#api-to-show-a-format-mapping-lookup) voor meer informatie.

```xpp
/// <summary>
/// The UIBuilder class for Questionnaires ER report
/// </summary>
class QuestionnairesErReportUIBuilder extends SysOperationAutomaticUIBuilder
{
    public const str ERQuestionnairesModel = 'Questionnaires';
    public const str ERQuestionnairesDataContainer = 'Root';

    /// <summary>
    /// Action after build of the dialog UI.
    /// </summary>
    public void postBuild()
    {
        DialogField formatMapping;
        super();
        formatMapping = this.bindInfo().getDialogField(this.dataContractObject(),
            methodStr(QuestionnairesErReportContract, parmFormatMapping));
        formatMapping.registerOverrideMethod(
            methodStr(FormReferenceControl, lookupReference),
            methodStr(QuestionnairesErReportUIBuilder, formatMappingLookup),
            this);
    }

    /// <summary>
    /// Performs the lookup form for format mapping.
    /// </summary>
    /// <param name="_referenceGroupControl">
    /// The control to perform lookup form.
    /// </param>
    public void formatMappingLookup(FormReferenceControl _referenceGroupControl)
    {
        ERObjectsFactory::createFormatMappingTableLookupForControlAndModel(
            _referenceGroupControl,
            ERQuestionnairesModel,
            ERQuestionnairesDataContainer).performFormLookup();
    }
}
```

#### <a name="add-a-data-provider-class"></a><a name="DataProviderClass"></a>Een gegevensproviderklasse toevoegen

Voeg de nieuwe klasse **QuestionnairesErReportDP** toe aan uw Microsoft Visual Studio-project en schrijf de code waarin de gegevensprovider wordt aangegeven die moet worden gebruikt om de geconfigureerde ER-indeling uit te voeren. De opgegeven code bevat alleen het gegevenscontract voor deze gegevensprovider.

```xpp
/// <summary>
/// Data provider class for Questionnaires ER report.
/// </summary>
public class QuestionnairesErReportDP
{
    QuestionnairesErReportContract contract;
    public static QuestionnairesErReportDP construct()
    {
        QuestionnairesErReportDP  dataProvider;
        dataProvider = new QuestionnairesErReportDP();
        return dataProvider;
    }
}
```

#### <a name="add-a-labels-file"></a><a name="LabelsFile"></a>Een labelbestand toevoegen

Voeg het nieuwe labelbestand **QuestionnairesErReportLabels\_en-US** toe aan uw Visual Studio-project en geef de volgende labels op voor nieuwe UI-resources:

- Het label **\@QuestionnairesReport** voor een nieuwe menuopdracht met de volgende tekst in het Engels (en-US): **Questionnaires report (powered by ER)**
- Het label **\@QuestionnairesReportBatchJobDescription** voor de titel van een batchtaak als een geselecteerde ER-indeling is gepland voor uitvoering als batchtaak

#### <a name="add-a-report-service-class"></a><a name="ServiceClass"></a>Een serviceklasse voor een rapport toevoegen

Voeg de nieuwe klasse **QuestionnairesErReportService** toe aan uw Visual Studio-project en schrijf code waarmee een ER-indeling wordt aangeroepen en geïdentificeerd met een indelingstoewijzings-id en waarmee een gegevenscontract als parameter wordt verstrekt.

```xpp
using Microsoft.Dynamics365.LocalizationFramework;
/// <summary>
/// The electronic reporting service class for Questionnaires ER report
/// </summary>
class QuestionnairesErReportService extends SysOperationServiceBase
{
    public const str ERModelDataSourceName = 'model';
    public const str DefaultExportedFileName = 'Questionnaires report';
    public const str ParametersDataSourceName = 'RunTimeParameters';

    /// <summary>
    /// Generates report by using Electronic reporting framework
    /// </summary>
    /// <param name = "_contract">The Questionnaires report contract</param>
    public void generateReportByGER(QuestionnairesErReportContract _contract)
    {
        ERFormatMappingId formatMappingId;
        QuestionnairesErReportDP  dataProvider;
        dataProvider = QuestionnairesErReportDP::construct();
        formatMappingId = _contract.parmFormatMapping();
        if (formatMappingId)
        {
            try
            {
                ERIModelDefinitionParamsAction parameters = new ERModelDefinitionParamsUIActionComposite()
                    .add(new ERModelDefinitionObjectParameterAction(ERModelDataSourceName, ParametersDataSourceName, _contract, true));

                // Call ER to generate the report.
                ERIFormatMappingRun formatMappingRun = ERObjectsFactory::createFormatMappingRunByFormatMappingId(formatMappingId, DefaultExportedFileName);
                if (formatMappingRun.parmShowPromptDialog(true))
                {
                    formatMappingRun.withParameter(parameters);
                    formatMappingRun.withFileDestination(_contract.getFileDestination());
                    formatMappingRun.run();
                }
            }
            catch
            {
                // An error occurred while exporting data.
                error("@SYP4861341");
            }
        }
        else
        {
            // There is no data available.
            info("@SYS300117");
        }
    }
}
```

Wanneer u een ER-indeling moet gebruiken waarmee toepassingsgegevens worden uitgevoerd, moet u een gegevensbron van het type **gegevensmodel** configureren in de indelingstoewijzing. Deze gegevensbron verwijst naar een specifiek onderdeel van het opgegeven gegevensmodel met behulp van één basisdefinitie. Wanneer de ER-indeling wordt uitgevoerd, wordt deze gegevensbron aangeroepen om toegang te krijgen tot de bijbehorende ER-modeltoewijzing die is geconfigureerd voor een bepaald model en een bepaalde basisdefinitie.

Alle informatie die u kunt voorbereiden in de broncode en kunt opslaan als onderdeel van het gegevenscontract, kan worden door gegeven aan de uitgevoerde ER-indeling met behulp van een ER-modeltoewijzing van dit type. In de ER-modeltoewijzing moet u een gegevensbron configureren van het **object** type dat naar de klasse **[QuestionnairesErReportContract](#DataContractClass)** verwijst. Als u een modeltoewijzing wilt identificeren, moet u een gegevensbron opgeven waarmee deze modeltoewijzing wordt aangeroepen. In de opgegeven code is deze gegevensbron opgegeven met de **ERModelDataSourceName**-constante die de waarde **[model](#ModelDSName)** bevat. Als u wilt bepalen welke gegevensbron wordt gebruikt om het gegevenscontract in de modeltoewijzing beschikbaar te maken, moet u de naam van een gegevensbron opgeven. In de opgegeven code wordt deze naam opgegeven met de constante **ParametersDataSourceName** die de waarde <a name="DataContractDSName"></a>**RunTimeParameters** bevat.

> [!NOTE]
> In een nieuwe omgeving moet u mogelijk de ER-metagegevens vernieuwen, zodat dit type klasse beschikbaar is in de ER-ontwerper voor modeltoewijzingen. Zie [Raamwerk elektronische rapportage (ER) configureren](electronic-reporting-er-configure-parameters.md#frequently-asked-questions) voor meer informatie.

#### <a name="add-a-report-controller-class"></a><a name="ControllerClass"></a>Een controllerklasse voor een rapport toevoegen

Voeg de nieuwe klasse **QuestionnairesErReportController** toe aan uw Visual Studio-project en schrijf code waarmee een ER-indeling naar wens wordt uitgevoerd in de synchrone of batchmodus, in het dialoogvenster dat wordt gebouwd op basis van de logica van de opgegeven klasse **QuestionnairesErReportUIBuilder**.

```xpp
/// <summary>
/// The controller for Questionnaires ER report
/// </summary>
class QuestionnairesErReportController extends ERFormatMappingRunBaseController
{
    /// <summary>
    /// The main entrance of the controller
    /// </summary>
    /// <param name = "args">The arguments</param>
    public static void main(Args args)
    {
        QuestionnairesErReportController operation;
        operation = new QuestionnairesErReportController(
            classStr(QuestionnairesErReportService),
            methodStr(QuestionnairesErReportService, generateReportByGER),
            SysOperationExecutionMode::Synchronous);
        operation.startOperation();
    }

    /// <summary>
    /// Gets caption of the dialog.
    /// </summary>
    /// <returns>Caption of the dialog</returns>
    public ClassDescription defaultCaption()
    {
        ClassDescription batchDescription;
        batchDescription = "Questionnaires report (powered by ER)";
        return batchDescription;
    }
}
```

#### <a name="add-a-menu-item"></a><a name="MenuItem"></a>Een menuopdracht toevoegen

Voeg de nieuwe menuopdracht **QuestionnairesErReport** toe aan uw Visual Studio-project. In de eigenschap **Object** verwijst deze menuopdracht naar de klasse **QuestionnairesErReportController** en wordt deze gebruikt om een gebruikersmachtiging op te geven voor het selecteren en uitvoeren van een ER-indeling. In de eigenschap **Label** verwijst deze menuopdracht naar het label **\@QuestionnairesReport** dat u eerder hebt gemaakt, zodat de juiste tekst wordt weergegeven in de toepassings-UI.

#### <a name="add-a-menu-item-to-a-menu"></a><a name="Menu"></a>Een menuopdracht aan een menu toevoegen

Voeg het bestaande menu **KM** aan uw Visual Studio-project toe. U moet een nieuw item **QuestionnairesErReport** van het type **Uitvoer** aan dit menu toevoegen. Dit item moet verwijzen naar de menuopdracht **QuestionnairesErReport** die in de vorige sectie is beschreven.

#### <a name="build-a-visual-studio-project"></a><a name="BuildVSProject"></a>Een Visual Studio-project opbouwen

Stel uw project samen om een nieuwe menuopdracht beschikbaar te maken voor gebruikers.

### <a name="run-a-format-from-the-application"></a><a name="RunFormatFromApp"></a>Een indeling uit de toepassing uitvoeren

1. Ga naar **Vragenlijst** \> **Ontwerp** \> **Questionnaires report (powered by ER)**.

    ![De menuopdracht Questionnaires report (powered by ER) selecteren in de module Vragenlijst om de geconfigureerde ER-indeling uit te voeren.](./media/er-quick-start1-application-menu-modified.png)

2. Selecteer in het dialoogvenster **Indelingstoewijzing** **Questionnaires report**.
3. Selecteer **OK**.
4. Configureer in het dialoogvenster **ER-parameters** op het sneltabblad **Op te nemen records** de filteroptie zo dat alleen de vragenlijst **SBCCrsExam** wordt opgenomen.
5. Selecteer **OK** om de filteroptie te bevestigen.
6. Selecteer **OK** om het rapport uit te voeren.

    ![Selectiecriteria opgeven in het dialoogvenster ER-rapport.](./media/er-quick-start1-report-run-dialog-page.png)

7. Controleer het gegenereerde rapport.

## <a name="tune-a-designed-er-solution"></a><a name="TuneSolution"></a>Een ontworpen ER-oplossing optimaliseren

U kunt de geconfigureerde ER-oplossing wijzigen, zodat deze de gegevensproviderklasse gebruikt die u hebt ontwikkeld om toegang te krijgen tot de details van de actieve ER-indeling, zodat de naam van deze ER-indeling wordt ingevoerd in een gegenereerd rapport.

### <a name="modify-a-model-mapping"></a><a name="ModifyModelMapping"></a>Een modeltoewijzing wijzigen

#### <a name="add-data-sources-to-access-a-data-contract-object"></a><a name="AddDataSource1"></a>Gegevensbronnen toevoegen voor toegang tot een gegevenscontractobject

1. Ga naar **Organisatiebeheer** \> **Elektronische rapportage** \> **Configuraties**.
2. Vouw op de pagina **Configuraties** in de configuratiestructuur **Vragenlijstmodel** uit en selecteer **Vragenlijsttoewijzing**.
3. Selecteer **Ontwerper** om de pagina **Model aan gegevensbrontoewijzing** te openen.
4. Selecteer **Ontwerper** om de geselecteerde toewijzing in de modeltoewijzingsontwerper te openen.
5. Selecteer op de pagina **Ontwerper modeltoewijzing** in het deelvenster **Typen gegevensbronnen** **Dynamics 365 for Operations\\Object**.
6. Selecteer **Basis toevoegen** in het deelvenster **Gegevensbronnen**.
7. Voer in het dialoogvenster in het veld **Naam** **[RunTimeParameters](#DataContractDSName)** in, zoals wordt gedefinieerd in de broncode van de klasse **QuestionnairesErReportService**.
8. Voer in het veld **Klasse** **[QuestionnairesErReportContract](#DataContractClass)** in, die eerder is gecodeerd.
9. Selecteer **OK**.
10. Vouw **RunTimeParameters** uit.

De toegevoegde gegevensbron bevat informatie over de record-id van de actieve ER-indelingstoewijzing.

![Gegevensbron toegevoegd aan de ontwerper voor ER-modeltoewijzingen.](./media/er-quick-start1-mapping3.png)

#### <a name="add-a-data-source-to-access-er-format-mapping-records"></a><a name="AddDataSource2"></a>Een gegevensbron toevoegen voor toegang tot toewijzingsrecords met een ER-indeling

Ga door met het bewerken van de geselecteerde modeltoewijzing door een gegevensbron toe te voegen om toegang te krijgen tot toewijzingsrecords voor ER-indeling.

1. Selecteer op de pagina **Ontwerper modeltoewijzing** in het deelvenster **Typen gegevensbronnen** **Dynamics 365 for Operations\\Tabelrecords**.
2. Selecteer **Basis toevoegen** in het deelvenster **Gegevensbronnen**.
3. Voer in het dialoogvenster in het veld **Naam** de tekst **ER1** in.
4. Voer in het veld **Tabel** **ERFormatMappingTable** in.
5. Selecteer **OK**.

#### <a name="add-a-data-source-to-access-a-format-mapping-record-of-a-running-er-format"></a><a name="AddDataSource3"></a>Een gegevensbron toevoegen voor toegang tot indelingstoewijzingsrecord van een actieve ER-indeling

Ga door met het bewerken van de geselecteerde modeltoewijzing door een gegevensbron toe te voegen om toegang te krijgen tot de indelingstoewijzingsrecord van de uit te voeren ER-indeling.

1. Selecteer op de pagina **Ontwerper modeltoewijzing** in het deelvenster **Typen gegevensbronnen** **Functies\\Berekend veld**.
2. Selecteer **Basis toevoegen** in het deelvenster **Gegevensbronnen**.
3. Voer in het dialoogvenster in het veld **Naam** de tekst **ER2** in.
4. Selecteer **Formule bewerken**.
5. Voer in de formule-editor in het veld **Formule** **FIRSTORNULL (FILTER(ER1, ER1.RecId = RunTimeParameters.parmFormatMapping))** in.
6. Selecteer **Opslaan** en sluit de formule-editor.
7. Selecteer **OK**.

#### <a name="enter-the-name-of-the-running-er-format-in-the-data-model"></a><a name="AddBinding"></a>De naam van de actieve ER-indeling in het gegevensmodel invoeren

U kunt doorgaan met het bewerken van de geselecteerde modeltoewijzing, zodat de naam van de actieve ER-indeling in het gegevensmodel wordt ingevoerd.

1. Vouw op de pagina **Ontwerper modeltoewijzing** in het deelvenster **Gegevensmodel** **ExecutionContext**, uit en selecteer **ExecutionContext\\FormatName**.
2. Selecteer **Bewerken** in het deelvenster **Gegevensmodel** om een gegevensbinding te configureren voor het veld van het gegevensmodel.
3. Voer in de formule-editor in het veld **Formule** **FIRSTORNULL (ER2.'\>Relations'.Format).Name** in.
4. Selecteer **Opslaan** en sluit de formule-editor.

Omdat u het **FormatName** hebt gebruikt, stelt de geconfigureerde modeltoewijzing nu de naam van een ER-indeling voor die deze modeltoewijzing aanroept tijdens de uitvoering.

![Het gegevensmodelveld binden aan de methode van de toegevoegde gegevensbron in de ontwerper van ER-modeltoewijzingen.](./media/er-quick-start1-mapping4.png)

#### <a name="complete-the-design-of-the-model-mapping"></a><a name="CompleteModelMapping2"></a>Het ontwerp van de modeltoewijzing voltooien

1. Selecteer **Opslaan** op de pagina **Ontwerper modeltoewijzing**.
2. Sluit de pagina.
3. Sluit de pagina Modeltoewijzingen.
4. Controleer op de pagina **Configuraties** in de configuratiestructuur of de configuratie van de **vragenlijsttoewijzing** nog steeds is geselecteerd. Selecteer vervolgens op het sneltabblad **Versies** de configuratieversie met de status **Concept**.
5. Selecteer **Status wijzigen** \> **Voltooien**.

De status van versie 1.2 van deze configuratie wordt gewijzigd van **Concept** in **Voltooid**. Versie 1.2 kan niet meer worden gewijzigd. Deze versie bevat de geconfigureerde modeltoewijzing en kan worden gebruikt als basis voor andere ER-configuraties. Versie 1.3 van deze configuratie wordt gemaakt met de status **Concept**. U kunt deze versie bewerken om de modeltoewijzing van de **Vragenlijst** aan te passen.

### <a name="modify-a-format"></a><a name="ModifyFormat"></a>Een indeling wijzigen

U kunt de geconfigureerde ER-indeling wijzigen, zodat de naam wordt weergegeven in de voettekst van een rapport dat wordt gegenereerd wanneer de ER-indeling wordt uitgevoerd.

#### <a name="add-a-new-format-element"></a><a name="AddFormatElement"></a>Een nieuw opmaakelement toevoegen

1. Ga naar **Organisatiebeheer** \> **Elektronische rapportage** \> **Configuraties**.
2. Vouw op de pagina **Configuraties** in de configuratiestructuur **Vragenlijstmodel** uit en selecteer **Vragenlijstrapport**.
3. Selecteer **Ontwerper**.
4. Ga naar de pagina **Indelingsontwerper** en selecteer het basisitem **Rapport**.
5. Selecteer **Toevoegen** om een nieuw genest opmaakelement toe te voegen voor het geselecteerde hoofditem **Rapport**.
6. Selecteer **Excel\\Voettekst**.
7. Voer in het veld **Naam** de tekst **Voettekst** in.
8. Selecteer **Report\Footer** en vervolgens **Toevoegen**.
9. Selecteer **Tekst\\Tekenreeks**.

#### <a name="bind-the-added-format-element"></a><a name="BindAddedFormatElement"></a>Het toegevoegde indelingselement binden

1. Selecteer op de pagina **Indelingsontwerper** op het tabblad **Toewijzing** in de indelingsstructuur, **Formule bewerken** voor het actieve element **Voettekst\\Tekenreeks**.
2. Voer in de formule-editor in het veld **Formule** **CONCATENATE ("\&C\&10", FORMAT("Generated by'\%1' ER solution", model.ExecutionContext.FormatName))** in.
3. Selecteer **Opslaan** en sluit de formule-editor.
4. Selecteer **Opslaan**.

De geconfigureerde indeling is nu gewijzigd, zodat de naam in de voettekst van een gegenereerd rapport wordt ingevoerd met het element **Voettekst\\Tekenreeks**.

![Het element voor de voettekstindeling toevoegen aan de geconfigureerde indeling in de ER Operation-ontwerper.](./media/er-quick-start1-template-format-structure3.png)

#### <a name="complete-the-format-design"></a><a name="CompleteFormat2"></a>Het indelingsontwerp voltooien

1. Sluit de pagina **Indelingsontwerper**.
2. Controleer op de pagina **Configuraties** in de configuratiestructuur of de configuratie van het **vragenlijstrappot** nog steeds is geselecteerd. Selecteer vervolgens op het sneltabblad **Versies** de configuratieversie met de status **Concept**.
3. Selecteer **Status wijzigen** \> **Voltooien**.

De status van versie 1.2 van deze configuratie wordt gewijzigd van **Concept** in **Voltooid**. Versie 1.2 kan niet meer worden gewijzigd. Deze versie bevat het geconfigureerde indeling en kan worden gebruikt als basis voor andere ER-configuraties. Versie 1.3 van deze configuratie wordt gemaakt met de status **Concept**. U kunt deze versie bewerken om het rapport **Vragenlijst** aan te passen.

### <a name="run-a-format-from-the-application"></a><a name="RunFormatFromApp2"></a>Een indeling uit de toepassing uitvoeren

1. Ga naar **Vragenlijst** \> **Ontwerp** \> **Questionnaires report (powered by ER)**.
2. Selecteer in het dialoogvenster **Indelingstoewijzing** **Questionnaires report**.
3. Selecteer **OK**.
4. Configureer in het dialoogvenster **ER-parameters** op het sneltabblad **Op te nemen records** de filteroptie zo dat alleen de vragenlijst **SBCCrsExam** wordt opgenomen.
5. Selecteer **OK** om de filteroptie te bevestigen.
6. Selecteer **OK** om het rapport uit te voeren.
7. Controleer het gegenereerde rapport in de Excel-indeling.

De voettekst van het gegenereerde rapport bevat de naam van de ER-indeling die is gebruikt om het rapport te genereren.

![Gegenereerd rapport in de Excel-indeling.](./media/er-quick-start1-report4.png)

### <a name="run-a-format-from-er"></a><a name="RunFormatFromER3"></a>Een indeling vanuit ER uitvoeren

1. Ga naar **Organisatiebeheer** \> **Elektronische rapportage** \> **Configuraties**.
2. Vouw op de pagina **Configuraties** in de configuratiestructuur **Vragenlijstmodel** uit en selecteer **Vragenlijstrapport**.
3. Selecteer **Uitvoeren** in het actievenster.
4. Configureer in het dialoogvenster **ER-parameters** op het sneltabblad **Op te nemen records** de filteroptie zo dat alleen de vragenlijst **SBCCrsExam** wordt opgenomen.
5. Selecteer **OK** om de filteroptie te bevestigen.
6. Selecteer **OK** om het rapport uit te voeren.
7. Controleer het gegenereerde rapport in de Excel-indeling.

Zoals u ziet, bevat de voettekst van het gegenereerde rapport niet de naam van de ER-indeling die is gebruikt om het te genereren, omdat het gegevenscontractobject niet is doorgegeven aan de actieve modeltoewijzing toen het werd aangeroepen door de ER-indeling die vanuit ER werd uitgevoerd.

### <a name="configure-a-format-destination-for-on-screen-preview"></a><a name="ConfigureDestination"></a>Een indelingsbestemming configureren voor voorvertoning op het scherm

1. Ga naar **Organisatiebeheer** \> **Elektronische rapportage** \> **Bestemming elektronische rapportage**.
2. Voeg op de pagina **Bestemming elektronische rapportage** een doelrecord toe voor de geconfigureerde ER-indeling voor het **Vragenlijstrapport**.
3. Stel op het sneltabblad **Bestandsbestemming** de [bestemming](er-destination-type-screen.md) **Scherm** in voor de indelingscomponent **Rapport** die is [toegevoegd](#AddFormatRootElement) als het hoofdelement van de geconfigureerde ER-indeling voor het **vragenlijstrapport**.
4. Configureer op het sneltabblad **Instellingen PDF-conversie** de bestemming om een rapport te converteren naar [PDF-indeling](electronic-reporting-destinations.md#OutputConversionToPDF) waarin de afdrukstand **Liggend** wordt gebruikt.

![De aangepaste schermbestemming configureren voor de ER-indeling op de pagina Bestemming elektronische rapportage.](./media/er-quick-start1-destination.png)

### <a name="run-a-format-from-the-application-to-preview-it-as-a-pdf-document"></a><a name="RunFormatFromApp3"></a>Een indeling van de toepassing uitvoeren voor voorvertoning als PDF-document

1. Ga naar **Vragenlijst** \> **Ontwerp** \> **Questionnaires report (powered by ER)**.
2. Selecteer in het dialoogvenster **Indelingstoewijzing** **Questionnaires report**.
3. Selecteer **OK**.
4. Configureer in het dialoogvenster **ER-parameters** op het sneltabblad **Op te nemen records** de filteroptie zo dat alleen de vragenlijst **SBCCrsExam** wordt opgenomen.
5. Selecteer **OK** om de filteroptie te bevestigen.

    Op het sneltabblad **Bestemmingen** doelen ziet u dat het veld **Uitvoer** is ingesteld op **Scherm**. Als u de geconfigureerde bestemming wilt wijzigen, selecteert u **Wijzigen**.

    ![Dialoogvenster voor ER-rapport in runtime, waarin u de geconfigureerde bestemming kunt wijzigen.](./media/er-quick-start1-run-settings.png)

6. Selecteer **OK** om het rapport uit te voeren.
7. Controleer het gegenereerde rapport in de PDF-indeling.

    ![Voorvertoning op het scherm van het gegenereerde rapport in PDF-indeling.](./media/er-quick-start1-preview-PDF.png)

## <a name="additional-resources"></a><a name="References"></a>Aanvullende bronnen

- [Overzicht van elektronische rapportage](general-electronic-reporting.md)
- [Formuletaal in Elektronische rapportage](er-formula-language.md)
- [Meertalige rapporten ontwerpen](er-design-multilingual-reports.md)
- [API ER-raamwerk](er-apis-app73.md)
- [CASE-functie](er-functions-logical-case.md)
- [CONCATENATE-functie](er-functions-text-concatenate.md)
- [DATETIMEFORMAT-functie](er-functions-datetime-datetimeformat.md)
- [FILTER-functie](er-functions-list-filter.md)
- [FIRSTORNULL-functie](er-functions-list-firstornull.md)
- [FORMAT-functie](er-functions-text-format.md)
- [IF-functie](er-functions-logical-if.md)
- [ORDERBY-functie](er-functions-list-orderby.md)
- [SESSIONNOW-functie](er-functions-datetime-sessionnow.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
