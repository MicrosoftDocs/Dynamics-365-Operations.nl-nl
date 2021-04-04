---
title: De parameters van een ER-indeling per rechtspersoon instellen
description: In dit onderwerp wordt uitgelegd hoe u de para meters van een ER-indeling (Elektronische rapportage) per rechts persoon kunt instellen.
author: NickSelin
manager: AnnBe
ms.date: 10/29/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, EROperationDesigner, ERLookupDesigner, ERComponentLookupStructureEditing
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-01-01
ms.dyn365.ops.version: Release 8.1.3
ms.openlocfilehash: eebca6575a0b23f75baabbb91727f498de44d9cb
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/09/2021
ms.locfileid: "5570705"
---
# <a name="set-up-the-parameters-of-an-er-format-per-legal-entity"></a>De parameters van een ER-indeling per rechtspersoon instellen

[!include[banner](../includes/banner.md)]

## <a name="prerequisites"></a>Vereisten

Als u deze stappen wilt voltooien, moet u eerst de stappen in het onderwerp [ER-indelingen configureren om parameters te gebruiken die per rechtspersoon worden opgegeven](er-app-specific-parameters-configure-format.md) uitvoeren.

Als u de voorbeelden in dit onderwerp wilt voltooien, moet u toegang hebben tot Microsoft Dynamics 365 Finance (Finance) voor een van de volgende rollen:

- Ontwikkelaar elektronische rapportage
- Functioneel consultant elektronische rapportage
- Systeembeheerder

## <a name="import-er-configurations"></a>ER-configuraties importeren

1.  Meld u aan bij uw omgeving.
2.  Selecteer **Elektronische aangifte** in het standaarddashboard.
3.  Selecteer **Rapportageconfiguraties**.
4.  Importeer in het huidige exemplaar van Finance de configuraties die u vanuit Regulatory Configuration Services (RCS) hebt geëxporteerd terwijl u de stappen in het onderwerp [ER-indelingen configureren om parameters te gebruiken die per rechtspersoon worden opgegeven](er-app-specific-parameters-configure-format.md) voltooide. Voer de volgende stappen uit voor elke ER-configuratie (Elektronische rapportage) in de onderstaande volgorde: gegevensmodel, modeltoewijzing en indelingen.

    1. Selecteer **Uitwisselen \> Laden uit XML-bestand**.
    2. Selecteer **Bladeren** om het bestand voor de vereiste ER-configuratie in XML-indeling te selecteren.
    3. Selecteer **OK**.
    
    In de volgende afbeelding ziet u de configuraties die u moet hebben wanneer u klaar bent.

    ![Pagina ER-configuraties](./media/GER-AppSpecParms-ImportedConfigurations.PNG)

## <a name="set-up-parameters-for-the-demf-company"></a>Parameters instellen voor het bedrijf DEMF

U kunt het ER-raamwerk gebruiken voor het instellen van toepassingsspecifieke parameters voor een ER-indeling.

1.  Selecteer de rechtspersoon **DEMF**.
2.  Selecteer de indeling **Indeling voor het opzoeken van LE-gegevens** in de configuratiestructuur.
3.  Selecteer in het actievenster op het tabblad **Configuraties** in de groep **Specifieke toepassingsparameters** de optie **Instellen**.

    ![De ER-pagina Specifieke toepassingsparameters](./media/GER-AppSpecParms-LookupForm.PNG)
    
    Op de pagina **Specifieke toepassingsparameters** kunt u de regels voor de gegevensbron **Selector** van de indeling **Indeling voor het opzoeken van LE-gegevens** configureren.
    
    Als de ER-basisindeling meerdere gegevensbronnen van het type **Zoekopdracht** bevat, moet u de gewenste gegevensbron selecteren op het sneltabblad **Zoekopdrachten** voordat u kunt beginnen met het configureren van de set regels voor de gegevensbron.
    
    Voor elke gegevensbron kunt u afzonderlijke regels configureren voor elke versie van de geselecteerde ER-indeling.
    
    Alle set regels voor alle opzoekgegevensbronnen die beschikbaar zijn in de geselecteerde versie van de ER-basisindeling vormen de toepassingsspecifieke parameters voor de ER-indeling.

4.  Selecteer versie **1.1.1** van de ER-indeling.
5.  Selecteer op het sneltabblad **Voorwaarden** de optie **Toevoegen**.
6.  Selecteer in het veld **Code** van de nieuwe record de vervolgkeuzepijl om de zoekopdracht te openen.

    De zoekopdracht bevat de lijst met belastingcodes voor selectie. Deze lijst wordt geretourneerd door de gegevensbron **Model.Data.Tax** die is geconfigureerd in de ER-basisindeling. Omdat deze gegevensbron het veld **Naam** bevat, wordt de naam van elke belastingcode weergegeven in de zoek opdracht.

    ![De ER-pagina Specifieke toepassingsparameters](./media/GER-AppSpecParms-LookupForm-CodeFldPicker.PNG)
    
7.  Selecteer de belastingcode **VAT19**.
8.  Selecteer in het veld **Zoekresultaat** van de nieuwe record de vervolgkeuzepijl om de zoekopdracht te openen. De lijst met waarden voor de indelingsopsomming TaxationLevel voor selectie wordt weergegeven.

    Als u Duits hebt geselecteerd als de voorkeurstaal van de gebruiker waarmee u bent aangemeld, worden de labels van de waarden in de zoekopdracht in het Duits weer gegeven, op voorwaarde dat deze zijn vertaald in de ER-basisindeling. Als het label van een gegevensbron voor opzoeken is vertaald, wordt dit label ook weergegeven in de voorkeurstaal van de gebruiker op het tabblad **Zoekopdrachten**.

    ![De ER-pagina Specifieke toepassingsparameters](./media/GER-AppSpecParms-LookupForm-LookupFldPicker.PNG)

9.  Selecteer de waarde **Normale belasting**.

    Door deze record toe te voegen, definieert u de volgende regel: wanneer de gegevensbron **Selector** wordt aangevraagd en de belastingcode **VAT19** als een argument wordt doorgegeven, wordt **Normale belasting** geretourneerd als het aangevraagde belastingniveau.

10. Selecteer **Toevoegen** en voer de volgende stappen uit:

    1. Selecteer de belastingcode **InVAT19** in het veld **Code**.
    2. Selecteer de waarde **Normale belasting** in het veld **Zoekresultaat**.
    
11. Selecteer nogmaals **Toevoegen** en voer de volgende stappen uit:

    1. Selecteer de belastingcode **InVAT7** in het veld **Code**.
    2. Selecteer de waarde **Verlaagde belasting** in het veld **Zoekresultaat**.
    
12. Selecteer nogmaals **Toevoegen** en voer de volgende stappen uit:

    1. Selecteer de belastingcode **InVAT7** in het veld **Code**.
    2. Selecteer de waarde **Verlaagde belasting** in het veld **Zoekresultaat**.
    
13. Selecteer nogmaals **Toevoegen** en voer de volgende stappen uit:

    1. Selecteer de belastingcode **THIRD** in het veld **Code**.
    2. Selecteer de waarde **Geen belasting** in het veld **Zoekresultaat**.
    
14. Selecteer nogmaals **Toevoegen** en voer de volgende stappen uit:

    1. Selecteer de belastingcode **InVAT0** in het veld **Code**.
    2. Selecteer de waarde **Geen belasting** in het veld **Zoekresultaat**.
    
15. Selecteer nogmaals **Toevoegen** en voer de volgende stappen uit:

    1. Selecteer de optie **\*Niet leeg\*** in het veld **Code**.
    2. Selecteer de waarde **Overig** in het veld **Zoekresultaat**.
    
    Door deze laatste record toe te voegen, definieert u de volgende regel: wanneer de gegevensbron die als een argument wordt doorgegeven, niet voldoet aan een van de vorige regels, wordt voor de gegevensbron voor opzoeken **Overig** geretourneerd als het aangevraagde belastingniveau.

    ![De ER-pagina Specifieke toepassingsparameters](./media/GER-AppSpecParms-LookupForm-RulesSet.PNG)
    
16. Selecteer **Voltooid** in het veld **Status**.

    Wanneer u een ER-indelingsversie met de status **Voltooid** of **Gedeeld** uitvoert, moet deze set regels de status **Voltooid** hebben. Anders wordt de uitvoering van de ER-basisindeling onderbroken wanneer wordt geprobeerd gegevens uit deze set regels te laden terwijl de gegevensbron voor opzoeken **Selector** wordt uitgevoerd.
    
    Wanneer u een ER-indelingsversie uitvoert met de status **Concept**, heeft de ER-basisindeling toegang tot deze set regels, ongeacht de status.
    
17. Selecteer **Opslaan**.
18. Sluit de pagina **Specifieke toepassingsparameters**.

## <a name="run-the-er-format-in-the-demf-company"></a>De ER-indeling in het bedrijf DEMF uitvoeren

1.  Selecteer de indeling **Indeling voor het opzoeken van LE-gegevens** in de configuratiestructuur.
2.  Selecteer **Uitvoeren** in het actievenster.
3.  Selecteer in het dialoogvenster dat verschijnt **OK**.
4.  Download het gegenereerde overzicht en sla dit lokaal op.

    In het gegenereerde overzicht is de samenvatting van de belastingcode **InVAT7** op het niveau **Verlaagd** geplaatst en de samenvattingen van de belastingcodes **VAT19** en **InVA19** op het niveau **Normaal**. Dit gedrag wordt bepaald door de configuratie in de groep regels die afhankelijk is van de rechtspersoon.
    
5.  Ga naar **Belasting \> Indirecte belastingen \> Btw \> Btw-codes**.
6.  Selecteer de belastingcode **InVAT7**.
7.  Selecteer in het actieven ster op het tabblad **Btw-code** in de groep **Query's** de optie **Geboekte btw** om informatie weer te geven over de belastingwaarde en het toegepaste belastingtarief per belastingcode.

    ![Pagina Geboekte btw](./media/GER-AppSpecParms-Statement.PNG)

8.  Sluit de pagina Geboekte btw.

## <a name="set-up-parameters-for-the-usmf-company"></a>Parameters instellen voor het bedrijf USMF

1.  Selecteer de rechtspersoon **USMF**.
2.  Ga naar **Organisatiebeheer \> Elektronische rapportage \> Configuraties**.
3.  Vouw in de configuratiestructuur de items **Model voor het leren van parameteraanroepen** en **Indeling voor het leren van parameteraanroepen** uit en selecteer de indeling **Indeling voor het opzoeken van LE-gegevens**.
4.  Selecteer in het actievenster op het tabblad **Configuraties** in de groep **Specifieke toepassingsparameters** de optie **Instellen**.
5.  Selecteer versie **1.1.1** van de geselecteerde ER-indeling.
6.  Selecteer op het sneltabblad **Voorwaarden** de optie **Toevoegen**.
7.  Selecteer in het veld **Code** van de nieuwe record de vervolgkeuzepijl om de zoekopdracht te openen.

    De zoekopdracht bevat nu de lijst met belastingcodes die kunnen worden geselecteerd voor het bedrijf **USMF**.

    ![De ER-pagina Specifieke toepassingsparameters](./media/GER-AppSpecParms-LookupForm-CodeFldPicker2.PNG)
    
8.  Selecteer de belastingcode **VRIJSTELLING**.
9.  Selecteer de waarde **Geen belasting** in het veld **Zoekresultaat** van de nieuwe record.
10. Selecteer opnieuw **Toevoegen**.
11. Selecteer de optie **\*Niet leeg\*** in het veld **Code** van de nieuwe record.
12. Selecteer de waarde **Normale belasting** in het veld **Zoekresultaat** van de nieuwe record.
13. Selecteer **Voltooid** in het veld **Status**.
14. Selecteer **Opslaan**.

    ![De ER-pagina Specifieke toepassingsparameters](./media/GER-AppSpecParms-LookupForm-RulesSet2.PNG)
    
15. Sluit de pagina **Specifieke toepassingsparameters**.

## <a name="run-the-er-format-in-the-usmf-company"></a>De ER-indeling in het bedrijf USMF uitvoeren

1.  Selecteer de indeling **Indeling voor het opzoeken van LE-gegevens** in de configuratiestructuur.
2.  Selecteer **Uitvoeren** in het actievenster.
3.  Selecteer in het dialoogvenster dat verschijnt **OK**.
4.  Download het gegenereerde overzicht en sla dit lokaal op.

    In het gegenereerde overzicht ziet u dat u nu dezelfde indeling hebt gebruikt voor een andere rechtspersoon, maar zonder wijzigingen aan te brengen in de ER-indeling.

## <a name="reuse-legal-entitydependent-parameters"></a>Van rechtspersonen afhankelijke parameters opnieuw gebruiken

### <a name="export-parameters"></a>Parameters exporteren

1.  Ga naar **Organisatiebeheer \> Werkgebieden \> Elektronische rapportage**.
2.  Selecteer **Rapportageconfiguraties**.
3.  Selecteer de indeling **Indeling voor het opzoeken van LE-gegevens** in de configuratiestructuur.
4.  Selecteer in het actievenster op het tabblad **Configuraties** in de groep **Specifieke toepassingsparameters** de optie **Instellen**.
5.  Selecteer versie **1.1.1** van de ER-indeling.
6.  Selecteer **Exporteren** in het actievenster.
7.  Download het gegenereerde bestand en sla dit lokaal op.

    De geconfigureerde verzameling toepassingsspecifieke parameters is nu geëxporteerd als een XML-bestand.

### <a name="import-parameters"></a>Parameters importeren

1.  Selecteer versie **1.1.2** van de ER-indeling.
2.  Selecteer **Importeren** in het Actievenster.
3.  Selecteer **Ja** als u wilt bevestigen dat de bestaande toepassingsspecifieke parameters voor deze indelingsversie wilt negeren.
4.  Selecteer **Bladeren** om het bestand te zoeken dat de geëxporteerde toepassingsspecifieke parameters voor versie **1.1.1** bevat.
5.  Selecteer **OK**.

    Versie **1.1.2** van de ER-indeling heeft nu dezelfde toepassingsspecifieke parameters die u oorspronkelijk voor versie **1.1.1** hebt geconfigureerd.
    
    De toepassingsspecifieke parameters van een ER-indeling zijn afhankelijk van de rechtspersoon. Als u de geconfigureerde toepassingsspecifieke parameters voor een rechtspersoon opnieuw wilt gebruiken voor een andere rechtspersoon, moet u deze exporteren terwijl u bent aangemeld bij de eerste rechtspersoon en deze vervolgens importeren nadat u zich hebt aangemeld bij de andere rechtspersoon.

    U kunt deze aanpak ook gebruiken om toepassingsspecifieke parameters voor een ER-indeling die oorspronkelijk waren geconfigureerd in het ene exemplaar van Finance over te dragen naar een ander exemplaar van Finance.

    Als u toepassingsspecifieke parameters voor één versie van een ER-indeling configureert en een hogere versie van dezelfde indeling in het huidige Finance-exemplaar importeert, worden de bestaande toepassingsspecifieke parameters niet toegepast voor de geïmporteerde versie.
    
    Wanneer u een bestand selecteert om te importeren, wordt de structuur van de toepassingsspecifieke parameters in dat bestand vergeleken met de structuur van de bijbehorende gegevensbron van het type **Zoekopdracht** in de ER-indeling die is geselecteerd voor importeren. De importbewerking wordt uitgevoerd wanneer de structuur van elke toepassingsspecifieke parameter overeenkomt met de structuur van de bijbehorende gegevensbron in de ER-indeling die is geselecteerd voor importeren. Als de structuren niet overeenkomen, ontvangt u de waarschuwing dat de importbewerking niet kan worden uitgevoerd. Als u de importbewerking afdwingt, worden de bestaande toepassingsspecifieke parameters voor de geselecteerde ER-indeling opgeruimd en moet u deze vanaf het begin instellen.

## <a name="relationship-between-application-specific-parameters-and-an-er-format"></a>Relatie tussen toepassingsspecifieke parameters en een ER-indeling

De relatie tussen een ER-indeling en de toepassingsspecifieke parameters wordt vastgesteld op basis van de exemplaaronafhankelijke unieke id-code van de ER-indeling. Wanneer u een ER-indeling uit Finance verwijdert, worden de toepassingsspecifieke parameters die zijn geconfigureerd voor de ER-indeling bewaard in het huidige exemplaar van Finance. Deze kunnen worden geopend wanneer de ER-basisindeling weer wordt geïmporteerd in dit exemplaar van Finance.

## <a name="access-application-specific-parameters-by-using-the-er-framework"></a>Toepassingsspecifieke parameters openen via het ER-raamwerk

In het vorige voorbeeld hebt u via het ER-raamwerk toegang gekregen tot toepassingsspecifieke parameters van een ER-indeling. Met deze benadering kunt u de toegang tot de toepassingsspecifieke parameters van een specifieke ER-indeling niet beperken. Voer de volgende stappen uit als u dergelijke beperkingen moet toepassen. 

1.  Gebruik een bestaand menu-item **ERSolutionAppSpecificParametersDesigner** of implementeer uw eigen menu-item **ERSolutionAppSpecificParametersDesigner**.

    ![Visual Studio-pagina](./media/GER-AppSpecParms-LookupForm-Access1.PNG)
    
2.  Volg één van deze stappen:

    1.  Maak een nieuwe menu-itemknop en koppel deze aan de bijbehorende record in de tabel **ERSolutionTable** door de eigenschap **Gegevensbron** in te stellen op **ERSolutionTable**.
    
        ![Visual Studio-pagina](./media/GER-AppSpecParms-LookupForm-Access2.PNG)
        
    2.  Maak een eenvoudige knop en negeer de methode **Geklikt**, zoals wordt weer gegeven in het volgende voorbeeld.
    
        Met deze methode kunt u een unieke oplossings-id (gedefinieerd via de waarde voor **GUID**) opgeven om uitsluitend toegang te verlenen tot de toepassingsspecifieke parameters van een specifieke ER-indeling en afstammende kopieën die hiervan zijn afgeleid.
        
        ```xpp
        public void clicked()
            {
                super();

                ERSolutionTable solutionTableRecord = ERSolutionTable::findByGUID(str2Guid('ADACCB2F-EFD1-4C90-877D-7E1E5D1AEE92'));

                Args args = new Args();
                args.record(solutionTableRecord);
                args.caller(this);

                new MenuFunction(menuItemDisplayStr(ERSolutionAppSpecificParametersDesigner), MenuItemType::Display)
                    .run(args);
            }
        ```

## <a name="additional-resources"></a>Aanvullende resources

[Formuleontwerper in elektronische aangifte](general-electronic-reporting-formula-designer.md)

[ER-indelingen configureren om parameters te gebruiken die per rechtspersoon worden opgegeven](er-app-specific-parameters-configure-format.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]