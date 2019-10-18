---
title: Interface van Report Designer
description: In dit artikel wordt uitgelegd hoe u kunt navigeren door Report Designer en hoe u gebruik kunt maken van de verschillende opties om aan uw specifieke vereisten te voldoen.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 59041
ms.assetid: 054de5b0-8618-4195-be12-f031b4bb4d74
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 19729cfd6bfd074c335612a06285bccf425333a4
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/27/2019
ms.locfileid: "2182779"
---
# <a name="report-designer-interface"></a>Interface van Report Designer

[!include [banner](../includes/banner.md)]

In dit artikel wordt uitgelegd hoe u kunt navigeren door Report Designer en hoe u gebruik kunt maken van de verschillende opties om aan uw specifieke vereisten te voldoen.

## <a name="report-designer-menu-commands"></a>Report Designer-menuopdrachten

In de volgende tabellen worden de menuopdrachten en opties beschreven die u kunt gebruiken wanneer u financiële rapporten ontwerpt. Sommige menuopdrachten en opties zijn alleen beschikbaar in bepaalde gevallen. De opdrachten voor het promoveren en degraderen van rapportage-eenheden zijn bijvoorbeeld alleen beschikbaar wanneer u een rapportagestructuurdefinitie wijzigt.

### <a name="file-menu"></a>Menu Bestand

Het menu **Bestand** is beschikbaar voor alle gebruikers en bevat de volgende opdrachten.

| Opdracht                           | Beschrijving |
|-----------------------------------|-------------|
| Nieuw                               | Een nieuwe rij rapportdefinitie, rijdefinitie, kolomdefinitie, rapportagestructuurdefinitie, rapportgroepdefinitie of map maken. Er zijn extra opties beschikbaar, afhankelijk van uw gebruikersrol. |
| Openstaand                              | Een bestaande rijdefinitie, kolomdefinitie, rapportagestructuurdefinitie of rapportdefinitie openen. |
| Afsluiten                             | De huidige bouwsteen sluiten. |
| Alles sluiten                         | Alle bouwstenen sluiten. |
| Opslaan                              | De huidige rijdefinitie, kolomdefinitie, rapportagestructuurdefinitie of rapportdefinitie opslaan. |
| Opslaan als                           | De huidige rijdefinitie, kolomdefinitie, rapportagestructuurdefinitie of rapportdefinitie opslaan met een nieuwe naam. |
| Eigenschappen                        | Het dialoogvenster **Eigenschappen** openen, waarin u de naam en omschrijving van een rapport kunt wijzigen. |
| Genereren                          | Het huidige rapport maken. Deze opdracht is beschikbaar vanuit een rapportdefinitie. |
| Rapport weergeven                       | Open de meest recente versie van het gegenereerde rapport. Deze opdracht is beschikbaar vanuit een rapportdefinitie als u ten minste één rapport hebt gegenereerd. |
| Recente rapportdefinities         | Een lijst weergeven van rapporten die recent zijn gemaakt of gewijzigd. U kunt dan een rapport in de lijst selecteren. |
| Recente rijdefinities            | Een lijst weergeven van rijdefinities die recent zijn gemaakt of gewijzigd. U kunt dan een rijdefinitie in de lijst selecteren. |
| Recente kolomdefinities         | Een lijst weergeven van kolomdefinities die recent zijn gemaakt of gewijzigd. U kunt dan een kolomdefinitie in de lijst selecteren. |
| Recente rapportagestructuurdefinities | Een lijst weergeven van rapportagestructuurdefinities die recent zijn gemaakt of gewijzigd. U kunt dan een rapportagestructuurdefinitie in de lijst selecteren. |
| Afsluiten                              | Report Designer sluiten. |

### <a name="edit-menu"></a>Menu Bewerken

Het menu **Bewerken** is beschikbaar voor gebruikers met de rol **Ontwerper** of **Beheerder**. Dit menu bevat de volgende opdrachten.

| Opdracht                                | Beschrijving |
|----------------------------------------|-------------|
| Ongedaan maken                                   | De laatste bewerking ongedaan maken. |
| Opnieuw uitvoeren                                   | De laatste bewerking voor ongedaan maken omkeren. |
| Knippen                                    | De geselecteerde tekst wissen en naar het Klembord kopiëren. |
| Kopiëren                                   | De geselecteerde tekst naar het Klembord kopiëren. |
| Plakken                                  | De meest recent geknipte of gekopieerde tekst van het klembord invoegen. |
| Wissen                                  | De inhoud van de geselecteerde bouwsteencel verwijderen. |
| Zoeken                                   | Het dialoogvenster **Zoeken en vervangen** openen, waarin u tekst in het voorbeeldvenster kunt zoeken. |
| Vervangen                                | Het dialoogvenster **Zoeken en vervangen** openen, waarin u tekst in het voorbeeldvenster kunt zoeken en vervangen. |
| Rijen invoegen van dimensies            | Het dialoogvenster **Rijen invoegen van dimensies** openen, waarin u de dimensiewaarden kunt selecteren die u in de rijdefinitie wilt opnemen. Deze opdracht is beschikbaar vanuit een rijdefinitie. |
| Rijen opnieuw nummeren                          | Alle numerieke rijcodes opnieuw nummeren. Deze opdracht is beschikbaar vanuit een rijdefinitie. |
| Rijkoppelingen                              | Het dialoogvenster **Rijkoppelingen** openen, waarin u de bronnen voor gegevenskoppelingen kunt opgeven in rijdefinities en rapportagestructuurdefinities. Deze opdracht is beschikbaar vanuit een rijdefinitie. |
| Afrondingscorrecties                    | Het dialoogvenster **Afrondingscorrecties** openen, waarin u de parameters voor afronding kunt opgeven. Deze opdracht is beschikbaar vanuit een rijdefinitie. |
| Dimensiesets beheren                  | Het dialoogvenster **Dimensiesets** openen, waarin u dimensiesets kunt maken en wijzigen. Deze opdracht is beschikbaar vanuit een rijdefinitie of rapportagestructuurdefinitie. |
| Rij invoegen                             | Een lege rij invoegen in de rijdefinitie of een lege koptekstrij invoegen in de kolomdefinitie. Deze opdracht is beschikbaar vanuit een rijdefinitie of kolomdefinitie. |
| Rij verwijderen                             | De geselecteerde rij verwijderen uit de rijdefinitie of de geselecteerde koptekstrij van de kolomdefinitie. Deze opdracht is beschikbaar vanuit een rijdefinitie of kolomdefinitie. |
| Kolom invoegen                          | Een lege kolom invoegen in de kolomdefinitie. Deze opdracht is beschikbaar vanuit een kolomdefinitie. |
| Kolom verwijderen                          | De geselecteerde kolom verwijderen uit de kolomdefinitie. Deze opdracht is beschikbaar vanuit een kolomdefinitie. |
| Rapportage-eenheden verwijderen uit dimensies | Het dialoogvenster **Rapportage-eenheden invoegen van dimensies** openen, waarin u de dimensiewaarden kunt selecteren die u in de rapportagestructuurdefinitie wilt opnemen. Deze opdracht is beschikbaar vanuit een rapportagestructuurdefinitie. |
| Hiërarchie van dimensieset importeren         | Het dialoogvenster **Hiërarchie van dimensieset** openen, waarin u een hiërarchie van dimensieset kunt importeren uit de financiële gegevens. Deze opdracht is beschikbaar vanuit een rapportagestructuurdefinitie voor een ..\\financial-dimensions\\op dimensies gebaseerd systeem. |
| Rapporteringseenheid invoegen                  | Een lege rij invoegen in de rapportagestructuurdefinitie. Deze opdracht is beschikbaar vanuit een rapportagestructuurdefinitie. |
| Rapportage-eenheid verwijderen                  | De geselecteerde rapportage-eenheidrij verwijderen uit de rapportagestructuurdefinitie. Deze opdracht is beschikbaar vanuit een rapporteringsstructuurdefinitie. |

### <a name="view-menu"></a>Menu Beeld

Het menu **Beeld** is beschikbaar voor alle gebruikers en bevat de volgende opdrachten.

| Opdracht         | Beschrijving                                                            |
|-----------------|------------------------------------------------------------------------|
| Navigatievenster | Het navigatievenster weergeven of verbergen.                                      |
| Werkbalken        | De werkbalken selecteren die zichtbaar zijn.                                  |
| Statusbalk      | De statusgegevens weergeven of verbergen in het venster **Report Designer**. |
| Welkomstpagina    | Hiermee opent u de pagina **Welkom**.                                             |

### <a name="format-menu"></a>Het menu Opmaak

Het menu **Opmaak** is beschikbaar voor gebruikers met de rol **Ontwerper** of **Beheerder**. Dit menu bevat de volgende opdrachten.

| Opdracht               | Beschrijving |
|-----------------------|-------------|
| Stijlen en opmaak | Het dialoogvenster **Stijlen en opmaak** openen, waarin u de stijl voor tekst in rijdefinities en kolomdefinities kunt maken en wijzigen. Deze opdracht is beschikbaar vanuit een rijdefinitie of een kolomdefinitie. |
| Kolombreedte          | Het dialoogvenster **Kolombreedte** openen, waarin u de breedte van de geselecteerde kolom kunt instellen. Deze opdracht is beschikbaar vanuit een rijdefinitie, een kolomdefinitie of een rapportagestructuurdefinitie. |
| Verborgen                  | De geselecteerde kolom verbergen. Deze opdracht is beschikbaar vanuit een rijdefinitie, kolomdefinitie of rapportagestructuurdefinitie. |
| Zichtbaar maken                | De verborgen kolommen tussen de geselecteerde kolommen zichtbaar maken. Deze opdracht is beschikbaar vanuit een rijdefinitie, kolomdefinitie of rapportagestructuurdefinitie. |

### <a name="company-menu"></a>Het menu Bedrijf

Het menu **Bedrijf** is beschikbaar voor gebruikers met de rol **Ontwerper** of **Beheerder**. Dit menu bevat de volgende opdrachten.

| Opdracht               | Beschrijving                                                                                                            |
|-----------------------|------------------------------------------------------------------------------------------------------------------------|
| Bedrijven             | Het dialoogvenster **Bedrijven** openen, waarin u bedrijven kunt maken en wijzigen.                                          |
| Bouwsteengroepen | Het dialoogvenster **Bouwsteengroepen** openen, waarin u bouwsteengroepen kunt maken, veranderen, importeren en exporteren. |

### <a name="go-menu"></a>Het menu Ga

Het menu **Ga naar** is toegankelijk voor alle gebruikers en bevat de volgende opdrachten.

> [!NOTE]
> Deze opdrachten hebben alleen een zichtbaar effect als het navigatiedeelvenster wordt weergegeven.

| Opdrachten                   | Beschrijving                                                                        |
|----------------------------|------------------------------------------------------------------------------------|
| Rapportdefinities         | Rapportdefinities weergeven in het navigatievenster.                                    |
| Rijdefinities            | Rijdefinities weergeven in het navigatievenster.                                       |
| Kolomdefinities         | Kolomdefinities weergeven in het navigatievenster.                                    |
| Rapportagestructuurdefinities | Rapportagestructuurdefinities weergeven in het navigatievenster.                            |
| Beveiliging                   | Beveiliginginformatie weergeven voor gebruikers, groepen en bedrijven in het navigatievenster. |

### <a name="tools-menu"></a>Menu Extra

Het menu **Extra** is beschikbaar voor alle gebruikers, maar sommige opdrachten hebben beperkte beschikbaarheid. Dit menu bevat de volgende opdrachten.

| Opdracht                       | Beschrijving |
|-------------------------------|-------------|
| Beveiligen                       | Een wachtwoord toepassen op de huidige bouwsteen. Deze opdracht is beschikbaar voor gebruikers met de rol **Ontwerper** of **Beheerder**. |
| Status van de rapportwachtrij           | Het dialoogvenster **Status van de rapportwachtrij** openen, waarin u alle recent gegenereerde rapporten en de details voor elk rapport kunt zien. |
| Bronsysteeminformatie     | De instellingen weergeven voor uw Microsoft Dynamics ERP-systeem. Deze opdracht is beschikbaar voor gebruikers met de rol **Ontwerper** of **Beheerder**. |
| Uitgecheckte artikelen             | De rijdefinities, kolomdefinities, rapportagestructuurdefinities en rapportdefinities weergeven die momenteel geopend zijn. Deze opdracht is beschikbaar voor gebruikers met de rol **Ontwerper** of **Beheerder**. |
| In cache opgeslagen financiële gegevens vernieuwen | De gegevens in de kolom Financiële dimensies bijwerken. |
| Opties                       | Het dialoogvenster **Opties** openen, waarin u gebruikersvoorkeuren voor Report Designer kunt wijzigen. |

### <a name="window-menu"></a>Het menu Venster

Het menu **Venster** is beschikbaar voor alle gebruikers en bevat de volgende opdrachten.

| Opdracht              | Beschrijving |
|----------------------|-------------|
| Horizontaal naast elkaar    | Alle openstaande vensters naast elkaar weergeven. |
| Verticaal naast elkaar      | Alle openstaande vensters weergeven, de ene boven de andere. |
| Trapsgewijs              | Alle openstaande vensters in lagen plaatsen, zodat de titelbalk van elk venster zichtbaar is. |
| Horizontaal blokkeren    | De geselecteerde rij blokkeren, zodat de rij tijdens het bladeren zichtbaar blijft in het venster. Deze opdracht is beschikbaar voor gebruikers met de rol **Ontwerper** of **Beheerder**. |
| Verticaal blokkeren      | De geselecteerde kolom blokkeren, zodat de kolom tijdens het bladeren zichtbaar blijft in het venster. Deze opdracht is beschikbaar voor gebruikers met de rol **Ontwerper** of **Beheerder**. |
| Lijst van openstaande vensters | Een lijst weergeven van vensters die openstaan. Een venster selecteren om het naar de voorgrond te brengen. |

### <a name="help-menu"></a>Menu Help

Het menu **Help** is beschikbaar voor alle gebruikers en bevat de volgende opdrachten.

| Command | Beschrijving                                                              |
|---------|--------------------------------------------------------------------------|
| Help    | Open de onderwerppagina met hulp voor financiële rapportage. |
|         |                                                                          |

## <a name="report-designer-toolbar-buttons"></a>Werkbalkknoppen van Report Designer
In de volgende tabellen worden de werkbalkknoppen beschreven die u kunt gebruiken wanneer u rapporten ontwerpt. Bepaalde werkbalkknoppen zijn alleen in bepaalde gevallen beschikbaar. De knoppen voor het promoveren en degraderen van rapportage-eenheden zijn bijvoorbeeld alleen beschikbaar wanneer u een rapportagestructuurdefinitie wijzigt.

### <a name="standard-toolbar"></a>Standaardwerkbalk

De standaardwerkbalk biedt snelle toegang tot bestands- en bewerkopdrachten. Deze werkbalk bevat de volgende knoppen.

| Knop                                                                                       | Beschrijving |
|----------------------------------------------------------------------------------------------|-------------|
| [![De knop Nieuw](./media/rowc130389.png)](./media/rowc130389.png)                              | Een nieuwe (lege) rapportdefinitie, rijdefinitie, kolomdefinitie of rapportagestructuurdefinitie maken. |
| [![De knop Openen](./media/openfolderc130389.png)](./media/openfolderc130389.png)               | Een bestaande rijdefinitie, kolomdefinitie, rapportagestructuurdefinitie of rapportdefinitie openen. |
| [![De knop Opslaan](./media/savec130389.png)](./media/savec130389.png)                           | De huidige rijdefinitie, kolomdefinitie, rapportagestructuurdefinitie of rapportdefinitie opslaan. |
| [![De knop Kopiëren](./media/copyc130389.png)](./media/copyc130389.png)                           | De geselecteerde tekst naar het Klembord kopiëren. |
| [![De knop Knippen](./media/cutc130389.png)](./media/cutc130389.png)                              | De geselecteerde tekst wissen en naar het Klembord kopiëren. |
| [![De knop Plakken](./media/pastec130389.png)](./media/pastec130389.png)                        | De tekst van het klembord invoegen. |
| [![De knop Ongedaan maken](./media/undoc130389.png)](./media/undoc130389.png)                           | De laatste bewerking ongedaan maken. |
| [![De knop Opnieuw uitvoeren](./media/redoc130389.png)](./media/redoc130389.png)                           | De laatste bewerking voor ongedaan maken omkeren. |
| [![De knop Zoeken](./media/findc130389.png)](./media/findc130389.png)                           | Het dialoogvenster **Zoeken en vervangen** openen, waarin u tekst in het actieve venster kunt zoeken en vervangen. |
| [![De knop Rij invoegen](./media/insertrowc130389.png)](./media/insertrowc130389.png)           | Een lege rij invoegen in de rijdefinitie of een lege koptekstrij invoegen in de kolomdefinitie. Deze knop is beschikbaar vanuit een rijdefinitie of kolomdefinitie. |
| [![De knop Kolom invoegen](./media/insertcolumnc130389.png)](./media/insertcolumnc130389.png)  | Een lege kolom invoegen in de kolomdefinitie. Deze knop is beschikbaar vanuit een kolomdefinitie. |
| [![De knop Vergrendelen](./media/lockc130389.png)](./media/lockc130389.png)                           | Een wachtwoord toepassen op de huidige bouwsteen. Deze knop is beschikbaar voor gebruikers met de rol **Ontwerper** of **Beheerder**. |
| [![De knop Rijkoppeling](./media/rowlinkc130389.png)](./media/rowlinkc130389.png)                 | Het dialoogvenster **Rijkoppelingen** openen, waarin u de bronnen voor gegevenskoppelingen kunt opgeven in rijdefinities en rapportagestructuurdefinities. Deze knop is beschikbaar vanuit een rijdefinitie. |
| [![De knop Promoveren](./media/promotec130389.png)](./media/promotec130389.png)                  | Een eenheid van de rapportagestructuurdefinitie promoveren. Als u een onderliggende eenheid selecteert en op **Promoveren** klikt, wordt de onderliggende eenheid verplaatst naar hetzelfde niveau als de bovenliggende eenheid. |
| [![De knop Niveau verlagen](./media/demotec130389.png)](./media/demotec130389.png)                     | Een eenheid van de rapportagestructuurdefinitie een niveau verlagen. Wanneer u een eenheid selecteert en op **Niveau verlagen** klikt, wordt de eenheid een onderliggende eenheid van de eenheid die eraan voorafgaat. |
| [![De knop Uitvouwen](./media/expandtreebuttonc130389.png)](./media/expandtreebuttonc130389.png) | Alle eenheden van de rapportagestructuurdefinitie uitvouwen op het niveau van de geselecteerde eenheid. |
| [![De knop Samenvouwen](./media/collapsec130389.png)](./media/collapsec130389.png)               | De rapportagestructuur samenvouwen. |
| [![De knop Help](./media/helpc130389.png)](./media/helpc130389.png)                           | Open Help. |

### <a name="formatting-toolbar"></a>De werkbalk Opmaak

De werkbalk Opmaak biedt gemakkelijke toegang tot stijlopdrachten. Deze werkbalk bevat de volgende knoppen.

| Knop                                                                                                       | Beschrijving                                             |
|--------------------------------------------------------------------------------------------------------------|---------------------------------------------------------|
| [![De knop Tekenstijl](./media/formattingc130389.png)](./media/formattingc130389.png)                         | De geselecteerde tekenstijl toepassen op de huidige tekst.      |
| [![De knop Lettertype](./media/fonttype.png)](./media/fonttype.png)                                                 | De huidige tekst instellen op het geselecteerde lettertype.              |
| [![De knop Tekengrootte](./media/fontsize.png)](./media/fontsize.png)                                            | De huidige tekst instellen op de geselecteerde tekengrootte (in punten). |
| [![De knop Vet](./media/boldc130389.png)](./media/boldc130389.png)                                           | De huidige tekst vet maken.                             |
| [![De knop Cursief](./media/italicsc130389.png)](./media/italicsc130389.png)                                   | De huidige tekst cursief maken.                           |
| [![De knop Onderstrepen](./media/underlinec130389.png)](./media/underlinec130389.png)                            | De huidige tekst onderstrepen.                             |
| [![De knop Inspringing verkleinen](./media/outdentlsc130389.png)](./media/outdentlsc130389.png)                      | De inspringing van de huidige tekst verlagen.                |
| [![De knop Inspringing vergroten](./media/indentlsc130389.png)](./media/indentlsc130389.png)                        | De inspringing van de huidige tekst vergroten.                |
| [![De knop Achtergrondkleur](./media/fillbackgroundcolorc130389.png)](./media/fillbackgroundcolorc130389.png) | De achtergrondkleur van de huidige cel veranderen.        |
| [![De knop Tekenkleur](./media/fontcolorc130389.png)](./media/fontcolorc130389.png)                           | De kleur van de huidige tekst veranderen.                   |

### <a name="report-designer-toolbar"></a>Werkbalk van Report Designer

De werkbalk van Report Designer biedt snelle toegang tot opdrachten voor het navigeren in Report Designer. Deze werkbalk bevat de volgende knoppen.

| Knop                                                                                              | Beschrijving |
|-----------------------------------------------------------------------------------------------------|-------------|
| [![De knop Rapportdefinitie](./media/reportc130389.png)](./media/reportc130389.png)                 | De rapportdefinitie weergeven die in het menu **Venster** wordt vermeld. |
| [![De knop Rijdefinitie](./media/rowc130389.png)](./media/rowc130389.png)                          | De rijdefinitie weergeven die aan de actieve rapportdefinitie is toegewezen. |
| [![De knop Kolomdefinitie](./media/columnc130389.png)](./media/columnc130389.png)                 | De kolomdefinitie weergeven die aan de actieve rapportdefinitie is toegewezen. |
| [![De knop Rapportagestructuurdefinitie](./media/treec130389.png)](./media/treec130389.png)             | De rapportagestructuurdefinitie weergeven die aan de actieve rapportdefinitie is toegewezen. |
| [![De knop Report Viewer](./media/reportviewerc130389.png)](./media/reportviewerc130389.png)         | De Report Viewer starten en de meest recente versie van het gegenereerde rapport weergeven. Deze knop is beschikbaar vanuit een rapportdefinitie als u ten minste één rapport hebt gegenereerd. |
| [![De knop Rapport genereren](./media/generate-to-ddvc130389.png)](./media/generate-to-ddvc130389.png) | Genereer een rapport op basis van de actieve rapportdefinitie. Deze knop is beschikbaar vanuit een rapportdefinitie. |

## <a name="additional-resources"></a>Aanvullende resources

[Financiële rapportage](financial-reporting-intro.md)

[Een financieel rapport genereren](generate-financial-report.md)
