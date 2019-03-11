---
title: Elektronische rapportage (ER) configureren om gegevens op te halen in Power BI
description: In dit onderwerp wordt beschreven hoe u uw ER-configuratie (Electronische rapportage) kunt gebruiken om gegevens van uw exemplaar van Finance and Operations over te dragen naar Power BI-services.
author: NickSelin
manager: AnnBe
ms.date: 06/20/2017
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
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: e2d3c03a75fd03dfd3a96a181eff20f934546ec4
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/29/2019
ms.locfileid: "335779"
---
# <a name="configure-electronic-reporting-er-to-pull-data-into-power-bi"></a>Elektronische rapportage (ER) configureren om gegevens op te halen in Power BI

[!include [banner](../includes/banner.md)]

In dit onderwerp wordt beschreven hoe u uw ER-configuratie (Electronische rapportage) kunt gebruiken om gegevens van uw exemplaar van Finance and Operations over te dragen naar Power BI-services. Als voorbeeld worden in dit onderwerp Intrastat-transacties gebruikt als zakelijke gegevens die moeten worden overgedragen. Met de Power BI-kaartvisualisering worden deze Intrastat-transactiegegevens gebruikt om een weergave voor analyse van import-/exportactiviteiten in het Power BI-rapport te maken.

## <a name="overview"></a>Overzicht

Microsoft Power BI bestaat uit een verzameling softwareservices, apps en connectors die samenwerken om externe gegevensbronnen om te zetten in coherente, visueel aantrekkelijk en interactieve inzichten. Met Elektronische rapportage (ER) kunnen gebruikers van Microsoft Dynamics 365 for Finance and Operations eenvoudig gegevensbronnen configureren en de overdracht van gegevens regelen van Finance and Operations naar Power BI. De gegevens worden overgebracht als bestanden in de OpenXML-werkbladindeling (Microsoft Excel-werkmapbestand). De overgebrachte bestanden worden opgeslagen op een Microsoft SharePoint-server die voor dit doel is geconfigureerd. De opgeslagen bestanden worden in Power BI gebruikt om rapporten met visualisaties (tabellen, grafieken, kaarten, enzovoort) te maken. Power BI-rapporten worden gedeeld met Power BI-gebruikers en in Power BI-dashboards en op Finance and Operations-pagina's geopend. In dit onderwerp worden de volgende taken beschreven:

- Finance and Operations configureren.
- Uw configuratie van de ER-indeling voorbereiden om gegevens op te halen uit Finance and Operations.
- De ER-omgeving configureren om gegevens over te dragen naar Power BI.
- Overgedragen gegevens gebruiken om een Power BI-rapport te maken.
- Het Power BI-rapport toegankelijk maken in Finance and Operations.

## <a name="prerequisites"></a>Vereisten
Om het voorbeeld in dit onderwerp te kunnen voltooien, moet u over de volgende toegangsrechten beschikken:

- Toegang verkrijgen tot Finance and Operations voor een van de volgende rollen:

    - Ontwikkelaar elektronische rapportage
    - Functioneel consultant elektronische rapportage
    - Systeembeheerder

- Toegang verkrijgen tot de SharePoint-server die voor gebruik met Finance and Operations is geconfigureerd
- Toegang tot het Power BI-raamwerk

## <a name="configure-document-management-parameters"></a>Parameters voor documentbeheer configureren
1. Configureer op de pagina **Parameters voor documentbeheer** toegang tot de SharePoint-server die in het bedrijf wordt gebruikt waarbij u bent aangemeld (het bedrijf DEMF in dit voorbeeld).
2. Test de verbinding met de SharePoint-server om er zeker van te zijn dat u toegang hebt gekregen.

    [![Pagina Parameters voor documentbeheer](./media/ger-power-bi-sharepoint-server-setting-1024x369.png)](./media/ger-power-bi-sharepoint-server-setting.png)

3. Open de geconfigureerde SharePoint-site. Maak een nieuwe map waarin door ER Excel-bestanden moeten worden opgeslagen die de bedrijfsgegevens bevatten die Power BI-rapporten nodig hebben als bron van Power BI-gegevenssets.
4. Maak in Finance and Operations op de pagina **Documenttypen** een nieuw documenttype dat wordt gebruikt om toegang te krijgen tot de SharePoint-map die u zojuist hebt gemaakt. Voer **Bestand** in het veld **Groep** en **SharePoint** in het veld **Locatie** in een geef vervolgens het adres van de SharePoint-map op.

    [![Pagina Documenttypen](./media/ger-power-bi-sharepoint-document-type-1024x485.png)](./media/ger-power-bi-sharepoint-document-type.png)

## <a name="configure-er-parameters"></a>ER-parameters configureren
1. Klik in de werkruimte **Elektronische rapportage** op de koppeling **Parameters van elektronische rapportage**.
2. Selecteer op het tabblad **Bijlagen** het documenttype **Bestand** voor alle velden.
3. Maak in de werkruimte **Elektronische rapportage** de vereiste provider actief door te klikken op **Instellen als actief**. Speel voor meer informatie de taakbegeleiding **ER-serviceprovider selecteren** af.

## <a name="use-an-er-data-model-as-the-source-of-data"></a>Een ER-gegevensmodel als de bron van gegevens selecteren
U moet een ER-gegevensmodel hebben als bron van zakelijke gegevens die worden gebruikt voor Power BI-rapporten. Dit gegevensmodel wordt geüpload vanuit de opslagplaats voor ER-configuraties. Zie voor meer informatie [Elektronische rapportageconfiguraties downloaden van Lifecycle Services](download-electronic-reporting-configuration-lcs.md) of speel de taakbegeleiding **Een ER-configuratie vanuit Lifecycle Services importeren** af. Selecteer **Intrastat** als het te uploaden gegevensmodel vanuit de geselecteerde opslagplaats voor ER-configuraties. (In dit voorbeeld wordt versie 1 van het model gebruikt.) U kunt vervolgens toegang krijgen tot de configuratie **Intrastat** ER-model op de pagina **Configuraties**.

[![Pagina Configuraties](./media/ger-power-bi-data-model-1024x371.png)](./media/ger-power-bi-data-model.png)

## <a name="design-an-er-format-configuration"></a>Een configuratie voor de ER-indeling ontwerpen
U moet een nieuwe configuratie voor de ER-indeling maken waarbij het gegevensmodel **Intrastat** als bron van zakelijke gegevens wordt gebruikt. Deze indelingsconfiguratie moet uitvoerresultaten als elektronische documenten in de indeling OpenXML (Excel-bestand) genereren. Speel voor meer informatie de taakbegeleiding **ER Een configuratie maken voor het genereren van rapporten in OPENXML-indeling** af. Geef de nieuwe configuratie de naam **Import-/exportactiviteiten**, zoals in de volgende afbeelding. Gebruik het Excel-bestand [ER-gegevens - import- en exportdetails](https://go.microsoft.com/fwlink/?linkid=845208) als sjabloon wanneer u de ER-indeling ontwerpt. (Speel de taakbegeleiding af voor informatie over het importeren van een indelingssjabloon.)

[![Configuratie van Import-/exportactiviteiten](media/ger-power-bi-format-configuration.png)](media/ger-power-bi-format-configuration.png)

Ga als volgt te werk om de indelingsconfiguratie **Import-/exportactiviteiten** te wijzigen.

1. Klik op **Ontwerper**.
2. Geef op het tabblad **Indeling** het bestandelement voor deze indeling de naam **Excel-uitvoerbestand**.

    [![Element Excel-uitvoerbestand](./media/ger-power-bi-format-configuration-file-element-name-1024x395.png)](./media/ger-power-bi-format-configuration-file-element-name.png)

3. Geef op het tabblad **Toewijzing** de naam van het Excel-bestand op dat wordt gegenereerd als deze indeling wordt uitgevoerd. Configureer de gerelateerde expressie om de waarde **Import- en exportdetails** te retourneren (de bestandsnaamextensie .xlsx wordt automatisch toegevoegd).

    [![Indelingsontwerper](./media/ger-power-bi-format-configuration-output-file-name-1024x396.png)](./media/ger-power-bi-format-configuration-output-file-name.png)

4. Voeg een nieuw gegevensbronitem voor deze indeling toe. (Deze opsomming is vereist voor verdere gegevensbinding.)

    1. Geef de gegevensbron de naam **richting\_opsomm**.
    2. Selecteer **Opsomming van gegevensmodel** als gegevensbrontype.
    3. Verwijs naar de gegevensmodelopsomming **Richting**.

    [![direction_enum](./media/ger-power-bi-format-configuration-mapping-added-enum-1024x454.png)](./media/ger-power-bi-format-configuration-mapping-added-enum.png)

5. Voltooi de binding van elementen van het gegevensmodel **Intrastat** en elementen van de ontworpen indeling, zoals in de volgende afbeelding.

    [![De binding voltooien](./media/ger-power-bi-format-configuration-mapping-details-1024x454.png)](./media/ger-power-bi-format-configuration-mapping-details.png)

Nadat deze is uitgevoerd, genereert de ER-indeling het uitvoerresultaat in de Excel-indeling. De details van de Intrastat-transacties worden naar het uitvoerresultaat verzonden en hierbij wordt onderscheid gemaakt tussen de transacties die importactiviteiten en exportactiviteiten beschrijven. Klik op **Uitvoeren** om de nieuwe ER-indeling voor de lijst met Intrastat-transacties op de pagina **Intrastat** (**Belasting** &gt; **Aangiften** &gt; **Buitenlandse handel** &gt; **Intrastat**) te testen.

[![Pagina Intrastat](./media/ger-power-bi-format-test-run-transactions-1024x322.png)](./media/ger-power-bi-format-test-run-transactions.png)

Het volgende uitvoerresultaat wordt gegenereerd. Het bestand wordt **Import- en exportdetails.xlsx** genoemd, zoals u in de indelingsinstellingen hebt opgegeven.

[![Import- en exportdetails.xlsx](./media/ger-power-bi-format-test-run-output-1024x472.png)](./media/ger-power-bi-format-test-run-output.png)

## <a name="configure-the-er-destination"></a>De ER-bestemming configureren
U moet het ER-framework configureren om het uitvoerresultaat van de nieuwe ER-indelingsconfiguratie op een speciale manier te verzenden.

- Het uitvoerresultaat moet naar de map van de geselecteerde SharePoint-server worden verzonden.
- Bij elke uitvoering van de indelingsconfiguratie moet een nieuwe versie van hetzelfde Excel-bestand worden gemaakt.

Op de pagina **Elektronische rapportage** (**Organisatiebeheer** &gt; **Elektronische rapportage**) klikt u op het item **Bestemming elektronische rapportage** en voegt u een nieuwe bestemming toe. In het veld **Verwijzing** selecteert u de indelingsconfiguratie **Import-/exportactiviteiten** die u eerder hebt gemaakt. Ga als volgt te werk om een nieuwe bestandbestemmingsrecord voor de verwijzing te maken.

1. Voer in het veld **Naam** de titel van de bestandsbestemming in.
2. In het veld **Bestandsnaam** selecteert u de naam **Excel-uitvoerbestand** als Excel-bestandsindeling.

Klik op de knop **Instellingen** voor de nieuwe bestemmingsrecord. Ga vervolgens in het dialoogvenster **Bestemmingsinstellingen** als volgt te werk.

1. Stel op het tabblad **Power BI** de optie **Ingeschakeld** in op **Ja**.
2. Selecteer in het veld **SharePoint** het documenttype **Gedeeld** dat u eerder hebt gemaakt.

## <a name="schedule-execution-of-the-configured-er-format"></a>De uitvoering van de geconfigureerde ER-indeling plannen
1. Selecteer op de pagina **Configuraties** (**Organisatiebeheer** &gt; **Elektronische rapportage** &gt; **Configuraties**) in de configuratiestructuur de configuratie **Import-/exportactiviteiten** die u eerder hebt gemaakt.
2. Wijzig de status van versie 1.1 van **Concept** in **Volledig** om deze indeling voor gebruik beschikbaar te maken.

    [![Pagina Configuraties](./media/ger-power-bi-format-configuration-complete-1024x401.png)](./media/ger-power-bi-format-configuration-complete.png)

3. Selecteer de voltooide versie van de configuratie **Import-/exportactiviteiten** en klik op **Uitvoeren**. De geconfigureerde bestemming wordt toegepast op het uitvoerresultaat dat in de Excel-indeling wordt gegenereerd.
4. Stel de optie **Batchverwerking** in op **Ja** om dit rapport in een modus zonder toezicht uit te voeren.
5. Klik op **Terugkeerpatroon** om het vereiste terugkeerpatroon van deze batchuitvoering te plannen. Met het terugkeerpatroon geeft u op hoe vaak de bijgewerkte gegevens van Finance and Operations naar Power BI worden overgedragen.

    [![Dialoogvenster Parameters elektronisch rapport](./media/ger-power-bi-format-configuration-run-to-schedule-1024x413.png)](./media/ger-power-bi-format-configuration-run-to-schedule.png)

6. Na de configuratie vindt u de taak van de ER-rapportuitvoering op de pagina **Batchtaken** (**Systeembeheer &gt; Query's &gt; Batchtaken**).

    [![Pagina Batchtaken](./media/ger-power-bi-format-configuration-running-job-1024x410.png)](./media/ger-power-bi-format-configuration-running-job.png)

7. Als deze taak voor het eerst wordt uitgevoerd, wordt een nieuw Excel-bestand met de geconfigureerde naam in de geselecteerde SharePoint-map gemaakt. Elke volgende keer dat de taak wordt uitgevoerd, wordt er een nieuwe versie van dit Excel-bestand gemaakt.

    [![Nieuwe versie van het Excel-bestand](./media/ger-power-bi-output-file-in-sharepoint-server-folder-2-1024x412.png)](./media/ger-power-bi-output-file-in-sharepoint-server-folder-2.png)

## <a name="create-a-power-bi-dataset-by-using-the-output-result-of-the-er-format"></a>Een Power BI-gegevensset maken op basis van het uivoerresultaat van de ER-indeling
1. Meld u aan bij Power BIen open een bestaande Power BI-groep (werkruimte ) of maak een nieuwe groep. Klik op **Toevoegen** onder **Bestanden** in het gedeelte **Importeren of verbinden met gegevens** of klik op het plusteken (**+**) naast **Gegevenssets** in het linkerdeelvenster.

    [![Een gegevensset maken](./media/ger-power-bi-add-dataset-1024x524.png)](./media/ger-power-bi-add-dataset.png)

2. Selecteer de optie **SharePoint – Teamsites** en voer vervolgens het pad in van de SharePoint-server die u gebruik (`https://ax7partner.litware.com` in ons voorbeeld).
3. Blader naar de map **/Shared Documents/GER data/PowerBI** en selecteer het Excel-bestand dat u als de gegevensbron voor de nieuwe Power BI-gegevensset hebt gemaakt.

    [![Het Excel-bestand selecteren](./media/ger-power-bi-add-dataset-select-excel-file-1024x522.png)](./media/ger-power-bi-add-dataset-select-excel-file.png)

4. Klik op **Verbinden** en klik vervolgens op **Importeren**. Er wordt een nieuwe gegevensset gemaakt die is gebaseerd op het geselecteerde Excel-bestand. De gegevensset kan ook automatisch aan het nieuwe dashboard worden toegevoegd.

    [![Gegevensset op het dashboard](./media/ger-power-bi-added-dataset-1024x489.png)](./media/ger-power-bi-added-dataset.png)

5. Configureer het schema voor vernieuwen voor deze gegevensset om een periodieke update af te dwingen. Bij periodieke updates kunnen nieuwe bedrijfsgegevens worden gebruikt die afkomstig zijn uit Finance and Operations via periodieke uitvoering van het ER-rapport door nieuwe versies van het Excel-bestand die op de SharePoint-server worden gemaakt.

## <a name="create-a-power-bi-report-by-using-the-new-dataset"></a>Een Power BI-rapport maken op basis van de nieuwe gegevensset
1. Klik op de Power BI-gegevensset **Import- en exportdetails** die u hebt gemaakt.
2. Configureer de visualisering. Selecteer bijvoorbeeld de visualisering **Ingevulde kaart** en configureer deze als volgt:

    - Wijs het gegevenssetveld **Land van oorsprong** aan het veld **Locatie** van de kaartvisualisering toe.
    - Wijs het gegevenssetveld **Hoeveelheid** aan het veld **Kleurverzadiging** van de kaartvisualisering toe.
    - Voeg de gegevenssetvelden **Activiteit** en **Jaar** toe aan de veldverzameling **Filters** van de kaartvisualisering.

3. Sla het Power BI-rapport op als **Rapport Import- en exportdetails**.

    [![Rapport Import- en exportdetails](./media/ger-power-bi-added-report-1024x498.png)](./media/ger-power-bi-added-report.png)

    Op de kaart worden de landen/regio's weergegeven die in het Excel-bestand worden vermeld (Oostenrijk en Zwitserland in dit voorbeeld). Met kleuren wordt de verhouding gefactureerde bedragen voor elk weergegeven.

4. Werk de lijst met Intrastat-transacties bij. De exporttransactie uit Italië wordt toegevoegd.

    [![Lijst Intrastat-transacties](./media/ger-power-bi-new-run-new-transaction-1024x321.png)](./media/ger-power-bi-new-run-new-transaction.png)

5. Wacht tot de volgende geplande uitvoering van het ER-rapport en de volgende geplande update van de Power BI-gegevensset. Controleer vervolgens het Power BI-rapport (geef alleen geïmporteerde transacties weer). De bijgewerkte kaart bevat nu Italië.

    [![Bijgewerkte kaart](./media/ger-power-bi-new-run-new-map-1024x511.png)](./media/ger-power-bi-new-run-new-map.png)

## <a name="access-power-bi-report-in-finance-and-operations"></a>Het Power BI-rapport toegankelijk maken in Finance and Operations.
De integratie tussen Finance and Operations en Power BI instellen. Zie voor meer informatie [Power BI-integratie voor werkgebieden configureren](configure-power-bi-integration.md).

1. Klik op de werkgebiedpagina **Elektronische rapportage** die Power BI-integratie ondersteunt (**Organisatiebeheer** &gt; **Werkgebieden** &gt; **Werkgebied Elektronische rapportage**) op **Opties** &gt; **Rapportcatalogus openen**.
2. Selecteer het Power BI-rapport **Import- en exportdetails** dat u hebt gemaakt om dat rapport als actie-item weer te geven op de geselecteerde pagina.
3. Klik op het actie-item om de Finance and Operations-pagina te openen met het rapport dat u in Power BI hebt ontworpen.

    [![Rapport Import- en exportdetails](./media/ger-power-bi-review-bi-report-in-ax-form-1024x586.png)](./media/ger-power-bi-review-bi-report-in-ax-form.png)

## <a name="additional-resources"></a>Aanvullende bronnen

[Bestemmingen van elektronische rapportage](electronic-reporting-destinations.md)

[Overzicht van elektronische rapportage](general-electronic-reporting.md)
