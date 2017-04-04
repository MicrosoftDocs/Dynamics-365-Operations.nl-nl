---
title: Elektronische aangifte bij Power BI bevatten met gegevens uit Dynamics 365 voor bewerkingen instellen
description: In dit onderwerp wordt beschreven hoe u uw ER-configuratie kunt gebruiken om gegevens van uw exemplaar van Dynamics 365 for Operations over te dragen naar Power BI-services. Als voorbeeld worden in dit onderwerp Intrastat-transacties gebruikt als zakelijke gegevens die moeten worden overgedragen. Met de Power BI-kaartvisualisering worden deze Intrastat-transactiegegevens gebruikt om een weergave voor analyse van import-/exportactiviteiten in het Power BI-rapport te maken.
author: kfend
manager: AnnBe
ms.date: 2016-10-31 13 - 22 - 29
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, Developer, IT Pro
ms.search.scope: Operations, Core
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 388b6398488e6f316c1ec07a00182e81c1dc8d08
ms.openlocfilehash: ed0192c44b6d7e88120c64e539ebb0ac3b379831
ms.lasthandoff: 03/31/2017


---

# <a name="set-up-electronic-reporting-to-provide-power-bi-with-data-from-dynamics-365-for-operations"></a>Elektronische aangifte bij Power BI bevatten met gegevens uit Dynamics 365 voor bewerkingen instellen

In dit onderwerp wordt beschreven hoe u uw ER-configuratie kunt gebruiken om gegevens van uw exemplaar van Dynamics 365 for Operations over te dragen naar Power BI-services. Als voorbeeld worden in dit onderwerp Intrastat-transacties gebruikt als zakelijke gegevens die moeten worden overgedragen. Met de Power BI-kaartvisualisering worden deze Intrastat-transactiegegevens gebruikt om een weergave voor analyse van import-/exportactiviteiten in het Power BI-rapport te maken.

<a name="overview"></a>Overzicht
--------

Microsoft Power BI bestaat uit een verzameling softwareservices, apps en connectors die samenwerken om externe gegevensbronnen om te zetten in coherente, visueel aantrekkelijk en interactieve inzichten. Met Elektronische rapportage (ER) kunnen gebruikers van Microsoft Dynamics 365 for Operations gemakkelijk gegevensbronnen configureren en de overdracht van gegevens van Dynamics 365 for Operations naar Power BI organiseren. De gegevens worden overgebracht als bestanden in de OpenXML-werkbladindeling (Microsoft Excel-werkmapbestand). De overgebrachte bestanden worden opgeslagen op een Microsoft SharePoint-server die voor dit doel is geconfigureerd. De opgeslagen bestanden worden in Power BI gebruikt om rapporten met visualisaties (tabellen, grafieken, kaarten, enzovoort) te maken. Power BI-rapporten worden gedeeld met Power BI-gebruikers en in Power BI-dashboards en op Dynamics 365 for Operations-pagina's geopend. In dit onderwerp worden de volgende taken beschreven:

-   Dynamics 365 for Operations configureren.
-   Uw configuratie van de ER-indeling voorbereiden om gegevens op te halen uit Dynamics 365 for Operations.
-   De ER-omgeving configureren om gegevens over te dragen naar Power BI.
-   Overgedragen gegevens gebruiken om een Power BI-rapport te maken.
-   Het Power BI-rapport toegankelijk maken in Dynamics 365 for Operations.

## <a name="prerequisites"></a>Vereisten
Om het voorbeeld in dit onderwerp te kunnen voltooien, moet u over de volgende toegangsrechten beschikken:

-   Toegang tot Dynamics 365 for Operations voor een van de volgende functies:
    -   Ontwikkelaar elektronische rapportage
    -   Functioneel consultant elektronische rapportage
    -   Systeembeheerder
-   Toegang tot de SharePoint-server die voor gebruik met Dynamics 365 for Operations is geconfigureerd
-   Toegang tot het Power BI-framework

## <a name="configure-document-management-parameters"></a>Parameters voor documentbeheer configureren
1.  Configureer op de pagina **Parameters voor documentbeheer** toegang tot de SharePoint-server die in het bedrijf wordt gebruikt waarbij u bent aangemeld (het bedrijf DEMF in dit voorbeeld).
2.  Test de verbinding met de SharePoint-server om er zeker van te zijn dat u toegang hebt gekregen. [![Pagina document management-parameters](./media/ger-power-bi-sharepoint-server-setting-1024x369.png)](./media/ger-power-bi-sharepoint-server-setting.png)
3.  Open de geconfigureerde SharePoint-site. Maak een nieuwe map waarin door ER Excel-bestanden moeten worden opgeslagen die de bedrijfsgegevens bevatten die Power BI-rapporten nodig hebben als bron van Power BI-gegevenssets.
4.  Maak in Dynamics 365 for Operations op de pagina **Documenttypen** een nieuw documenttype dat moet worden gebruikt om toegang te krijgen tot de SharePoint-map die u zojuist hebt gemaakt. Voer **Bestand** in het veld **Groep** en **SharePoint** in het veld **Locatie** in een geef vervolgens het adres van de SharePoint-map op. [![De pagina typen document](./media/ger-power-bi-sharepoint-document-type-1024x485.png)](./media/ger-power-bi-sharepoint-document-type.png)

## <a name="configure-er-parameters"></a>ER-parameters configureren
1.  Klik in de werkruimte **Elektronische rapportage** op de koppeling **Parameters van elektronische rapportage**.
2.  Selecteer op het tabblad **Bijlagen** het documenttype **Bestand** voor alle velden.
3.  Maak in de werkruimte **Elektronische rapportage** de vereiste provider actief door te klikken op **Instellen als actief**. Speel voor meer informatie de taakbegeleiding **ER-serviceprovider selecteren** af.

## <a name="use-an-er-data-model-as-the-source-of-data"></a>Een ER-gegevensmodel als de bron van gegevens selecteren
U moet een ER-gegevensmodel hebben als bron van zakelijke gegevens die worden gebruikt voor Power BI-rapporten. Dit gegevensmodel wordt geüpload vanuit de opslagplaats voor ER-configuraties. Zie voor meer informatie [Elektronische rapportageconfiguraties downloaden van Lifecycle Services](download-electronic-reporting-configuration-lcs.md) of speel de taakbegeleiding **Een ER-configuratie vanuit Lifecycle Services importeren** af. Selecteer **Intrastat **als het te uploaden gegevensmodel vanuit de geselecteerde opslagplaats voor ER-configuraties. (In dit voorbeeld versie 1 van het model wordt gebruikt.) U kunt vervolgens toegang tot de **Intrastat** Emergency Recovery configuratie op de **configuraties** pagina. [![Configuraties pagina](./media/ger-power-bi-data-model-1024x371.png)](./media/ger-power-bi-data-model.png)

## <a name="design-an-er-format-configuration"></a>Een configuratie voor de ER-indeling ontwerpen
U moet een nieuwe configuratie voor de ER-indeling maken waarbij het gegevensmodel **Intrastat** als bron van zakelijke gegevens wordt gebruikt. Deze indelingsconfiguratie moet uitvoerresultaten als elektronische documenten in de indeling OpenXML (Excel-bestand) genereren. Speel voor meer informatie de taakbegeleiding **ER Een configuratie maken voor het genereren van rapporten in OPENXML-indeling** af. Geef de nieuwe configuratie de naam **Import-/exportactiviteiten**, zoals in de volgende afbeelding. Gebruik het Excel-bestand [ER-gegevens - import- en exportdetails](https://go.microsoft.com/fwlink/?linkid=845208) als sjabloon wanneer u de ER-indeling ontwerpt. (Voor meer informatie over het importeren van een sjabloon voor indeling, spelen de handleiding van de taak.) [![Importeren / activiteiten configuratie exporteren](media/ger-power-bi-format-configuration.png)](media/ger-power-bi-format-configuration.png) wilt wijzigen de **importeren / exporteren activiteiten** configuratie indeling, als volgt te werk.

1.  Klik op **Ontwerper**.
2.  Geef op het tabblad **Indeling** het bestandelement voor deze indeling de naam **Excel-uitvoerbestand**. [![Element voor bestanden van Excel-uitvoer](./media/ger-power-bi-format-configuration-file-element-name-1024x395.png)](./media/ger-power-bi-format-configuration-file-element-name.png)
3.  Geef op het tabblad **Toewijzing** de naam van het Excel-bestand op dat wordt gegenereerd als deze indeling wordt uitgevoerd. Configureer de gerelateerde expressie om de waarde **Import- en exportdetails** te retourneren (de bestandsnaamextensie .xlsx wordt automatisch toegevoegd). [![Format designer](./media/ger-power-bi-format-configuration-output-file-name-1024x396.png)](./media/ger-power-bi-format-configuration-output-file-name.png)
4.  Voeg een nieuw gegevensbronitem voor deze indeling toe. (Deze opsomming is vereist voor verdere gegevensbinding.)
    1.  Naam van de gegevensbron **richting\_enum**.
    2.  Selecteer **Opsomming van gegevensmodel** als gegevensbrontype.
    3.  Verwijs naar de gegevensmodelopsomming **Richting**.

    [![richting\_enum](./media/ger-power-bi-format-configuration-mapping-added-enum-1024x454.png)](./media/ger-power-bi-format-configuration-mapping-added-enum.png)
5.  Voltooi de binding van elementen van het gegevensmodel **Intrastat** en elementen van de ontworpen indeling, zoals in de volgende afbeelding. [![De bindende voltooien](./media/ger-power-bi-format-configuration-mapping-details-1024x454.png)](./media/ger-power-bi-format-configuration-mapping-details.png)

Nadat deze is uitgevoerd, genereert de ER-indeling het uitvoerresultaat in de Excel-indeling. De details van de Intrastat-transacties worden naar het uitvoerresultaat verzonden en hierbij wordt onderscheid gemaakt tussen de transacties die importactiviteiten en exportactiviteiten beschrijven. Klik op **uitgevoerd** om te testen van de nieuwe Emergency Recovery-indeling voor de lijst met Intrastat-transacties op de **Intrastat** pagina (**btw**&gt;**aangiften**&gt;**buitenlandse handel**&gt;**Intrastat**). [![Intrastat-pagina](./media/ger-power-bi-format-test-run-transactions-1024x322.png)](./media/ger-power-bi-format-test-run-transactions.png) het volgende resultaat van de uitvoer wordt gegenereerd. Het bestand wordt **Import- en exportdetails.xlsx** genoemd, zoals u in de indelingsinstellingen hebt opgegeven. [![Details.xlsx importeren en exporteren](./media/ger-power-bi-format-test-run-output-1024x472.png)](./media/ger-power-bi-format-test-run-output.png)

## <a name="configure-the-er-destination"></a>De ER-bestemming configureren
U moet het ER-framework configureren om het uitvoerresultaat van de nieuwe ER-indelingsconfiguratie op een speciale manier te verzenden.

-   Het uitvoerresultaat moet naar de map van de geselecteerde SharePoint-server worden verzonden.
-   Bij elke uitvoering van de indelingsconfiguratie moet een nieuwe versie van hetzelfde Excel-bestand worden gemaakt.

Op de **elektronische aangifte** pagina (**Organisatiebeheer**&gt;**elektronische aangifte**), klikt u op de **elektronische aangifte bestemming** artikel en een nieuwe bestemming toevoegen. In het veld **Verwijzing** selecteert u de indelingsconfiguratie **Import-/exportactiviteiten** die u eerder hebt gemaakt. Ga als volgt te werk om een nieuwe bestandbestemmingsrecord voor de verwijzing te maken.

1.  Voer in het veld **Naam** de titel van de bestandsbestemming in.
2.  In het veld **Bestandsnaam** selecteert u de naam **Excel-uitvoerbestand** als Excel-bestandsindeling.

Klik op de knop **Instellingen** voor de nieuwe bestemmingsrecord. Ga vervolgens in het dialoogvenster **Bestemmingsinstellingen** als volgt te werk.

1.  Stel op het tabblad **Power BI** de optie **Ingeschakeld** in op **Ja**.
2.  Selecteer in het veld **SharePoint** het documenttype **Gedeeld** dat u eerder hebt gemaakt.

## <a name="schedule-execution-of-the-configured-er-format"></a>De uitvoering van de geconfigureerde ER-indeling plannen
Op de **configuraties** pagina (**Organisatiebeheer**&gt;**elektronische aangifte**&gt;**configuraties**), in de structuur van configuraties, selecteert u de **Import / export activiteiten** configuratie die u eerder hebt gemaakt. Wijzig de status van versie 1.1 van **Concept** in **Volledig** om deze indeling voor gebruik beschikbaar te maken. [![Configuraties pagina](./media/ger-power-bi-format-configuration-complete-1024x401.png)](./media/ger-power-bi-format-configuration-complete.png) selecteert u de voltooide versie van de **importeren / exporteren activiteiten** configuratie en klik vervolgens op **uitgevoerd**. De geconfigureerde bestemming wordt toegepast op het uitvoerresultaat dat in de Excel-indeling wordt gegenereerd. Stel de optie **Batchverwerking** in op **Ja** om dit rapport in een modus zonder toezicht uit te voeren. Klik op **Terugkeerpatroon** om het vereiste terugkeerpatroon van deze batchuitvoering te plannen. Met het terugkeerpatroon geeft u op hoe vaak de bijgewerkte gegevens van Dynamics 365 for Operations naar Power BI worden overgedragen. [![Elektronische parameters van het dialoogvenster](./media/ger-power-bi-format-configuration-run-to-schedule-1024x413.png)](./media/ger-power-bi-format-configuration-run-to-schedule.png) nadat deze geconfigureerd, vindt u de taak Emergency Recovery rapport kan worden uitgevoerd op de **batchtaken** pagina (**Systeembeheer &gt;query's &gt;batchtaken**). [![Batch taken pagina](./media/ger-power-bi-format-configuration-running-job-1024x410.png)](./media/ger-power-bi-format-configuration-running-job.png) wanneer deze taak voor de eerste keer wordt uitgevoerd, de bestemming maakt een nieuw Excel-bestand met de geconfigureerde naam in de geselecteerde SharePoint-map. Elke volgende keer dat de taak wordt uitgevoerd, wordt er een nieuwe versie van dit Excel-bestand gemaakt. [![Nieuwe versie van het Excel-bestand](./media/ger-power-bi-output-file-in-sharepoint-server-folder-2-1024x412.png)](./media/ger-power-bi-output-file-in-sharepoint-server-folder-2.png)

## <a name="create-a-power-bi-dataset-by-using-the-output-result-of-the-er-format"></a>Een Power BI-gegevensset maken op basis van het uivoerresultaat van de ER-indeling
Meld u aan bij Power BI en open een bestaande Power BI-groep (werkruimte ) of maak een nieuwe groep. Klikken op **Add** onder **bestanden** in de **importeren of verbinding maken met gegevens** sectie of klik op het plusteken (**+**) naast **gegevenssets** in het linkerdeelvenster. [![Een gegevensset maakt](./media/ger-power-bi-add-dataset-1024x524.png)](./media/ger-power-bi-add-dataset.png) selecteert u de **SharePoint-teamsites** optie en voer vervolgens het pad van de SharePoint-Server die u gebruikt (**https://ax7partner.spoppe.com** in ons voorbeeld). Blader vervolgens naar de map **/Shared Documents/GER data/PowerBI** en selecteer het Excel-bestand dat u als de gegevensbron voor de nieuwe Power BI-gegevensset hebt gemaakt. [![Het Excel-bestand selecteren](./media/ger-power-bi-add-dataset-select-excel-file-1024x522.png)](./media/ger-power-bi-add-dataset-select-excel-file.png) Klik op **verbinden**, en klik vervolgens op **importeren**. Er wordt een nieuwe gegevensset gemaakt die is gebaseerd op het geselecteerde Excel-bestand. De gegevensset kan ook automatisch aan het nieuwe dashboard worden toegevoegd. [![DataSet op het dashboard](./media/ger-power-bi-added-dataset-1024x489.png)](./media/ger-power-bi-added-dataset.png) het schema vernieuwen voor deze dataset forceren van een periodieke update configureren. Bij periodieke updates kunnen nieuwe bedrijfsgegevens worden gebruikt die afkomstig zijn uit Dynamics 365 for Operations via periodieke uitvoering van het ER-rapport door nieuwe versies van het Excel-bestand die op de SharePoint-server worden gemaakt.

## <a name="create-a-power-bi-report-by-using-the-new-dataset"></a>Een Power BI-rapport maken op basis van de nieuwe gegevensset
Als u een nieuw Power BI-rapport wilt maken, klikt u op de Power BI-gegevensset **Import- en exportdetails** die u hebt gemaakt. Configureer vervolgens de visualisering. Selecteer bijvoorbeeld de visualisering **Ingevulde kaart** en configureer deze als volgt:

-   Wijs het gegevenssetveld **Land van oorsprong** aan het veld **Locatie** van de kaartvisualisering toe.
-   Wijs het gegevenssetveld **Hoeveelheid** aan het veld **Kleurverzadiging** van de kaartvisualisering toe.
-   Voeg de gegevenssetvelden **Activiteit** en **Jaar** toe aan de veldverzameling **Filters** van de kaartvisualisering.

Sla het Power BI-rapport op als **Rapport Import- en exportdetails**. [![Importeren en exporteren van gegevens rapport](./media/ger-power-bi-added-report-1024x498.png)](./media/ger-power-bi-added-report.png) Houd er rekening mee dat de tekens wordt ook de landen/regio's die worden vermeld in het Excel-bestand (Oostenrijk en Zwitserland in dit voorbeeld). Met kleuren wordt de verhouding gefactureerde bedragen voor elk weergegeven. Werk de lijst met Intrastat-transacties bij. De exporttransactie uit Italië wordt toegevoegd. [![Lijst met Intrastat-transacties](./media/ger-power-bi-new-run-new-transaction-1024x321.png)](./media/ger-power-bi-new-run-new-transaction.png) wachten op de volgende geplande uitvoering van het rapport ER en de volgende geplande update van de dataset Power BI. Controleer vervolgens het Power BI-rapport (geef alleen geïmporteerde transacties weer). De bijgewerkte kaart bevat nu Italië. [![bijgewerkte toewijzing](./media/ger-power-bi-new-run-new-map-1024x511.png)](./media/ger-power-bi-new-run-new-map.png)

## <a name="access-power-bi-report-in-dynamics-365-for-operations"></a>Power BI-rapport openen in Dynamics 365 for Operations
Stel de integratie tussen Dynamics 365 for Operations en Power BI in. Zie [Power BI-integratie voor werkruimten configureren](configure-power-bi-integration.md) voor meer informatie. Op de **elektronische aangifte** werkruimte pagina die ondersteuning biedt voor Power BI-integratie (**Organisatiebeheer**&gt;**werkruimten**&gt;**elektronische aangifte werkruimte**), klikt u op **opties**&gt;**geopend Rapportcatalogus**. Selecteer het Power BI-rapport **Import- en exportdetails** dat u hebt gemaakt om dat rapport als actie-item weer te geven op de geselecteerde pagina. Klik op het actie-item om de Dynamics 365 for Operations-pagina te openen met het rapport dat u in Power BI hebt ontworpen. [![Rapportdetails importeren en exporteren](./media/ger-power-bi-review-bi-report-in-ax-form-1024x586.png)](./media/ger-power-bi-review-bi-report-in-ax-form.png)

<a name="see-also"></a>Zie ook
--------

[Bestemmingen voor elektronische rapportage](electronic-reporting-destinations.md)

[Overzicht van elektronische rapportage](general-electronic-reporting.md)


