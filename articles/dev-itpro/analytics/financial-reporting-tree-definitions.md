---
title: Rapportagestructuurdefinities in financiële rapporten
description: Dit artikel bevat informatie over rapportagestructuurdefinities. Een rapportagestructuurdefinitie is een rapportonderdeel, of bouwsteen, die helpt bij het definiëren van de structuur en de hiërarchie van uw organisatie.
author: ShylaThompson
manager: AnnBe
ms.date: 01/11/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 57592
ms.assetid: 747faa47-9a23-4277-bc11-8d0a1267c3a4
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 00219f21076af60f8e2f16ca365b1138bb279400
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/15/2019
ms.locfileid: "1553869"
---
# <a name="reporting-tree-definitions-in-financial-reports"></a>Rapportagestructuurdefinities in financiële rapporten

[!include [banner](../includes/banner.md)]

Dit artikel bevat informatie over rapportagestructuurdefinities. Een rapportagestructuurdefinitie is een rapportonderdeel, of bouwsteen, die helpt bij het definiëren van de structuur en de hiërarchie van uw organisatie.

Financiële rapportage ondersteunt flexibele rapportage, zodat u gemakkelijk wijzigingen kunt aanbrengen wanneer uw bedrijfsstructuur verandert. Rapporten zijn opgebouwd uit verschillende onderdelen of bouwstenen. Een van deze bouwstenen is een rapportagestructuurdefinitie. Een rapportagestructuurdefinitie helpt bij het definiëren van de structuur en hiërarchie van uw organisatie. Het is een hiërarchische structuur over meerdere dimensies heen die is gebaseerd op de dimensionale relaties in uw financiële gegevens zijn gebaseerd. Het biedt informatie op het niveau van de rapportage-eenheid en op overzichtsniveau voor alle eenheden in de structuur. Rapportagestructuurdefinities kunnen met kolomdefinities en rapportdefinities worden gecombineerd om een bouwsteengroep te maken die door meerdere bedrijven kan worden gebruikt. Een rapportage-eenheid wordt gebruikt voor elk vak in een organogram. Een rapporteringseenheid kan een afzonderlijke afdeling uit de financiële gegevens zijn, of een samenvattingseenheid op een hoger niveau, waarin informatie uit lagere rapporteringseenheden wordt gecombineerd. Voor een rapportdefinitie die een rapportagestructuur bevat, wordt een rapport gegenereerd voor elke rapportage-eenheid en voor het overzichtsniveau. Elk van deze rapporten gebruikt de rij- en kolomdefinities die in de rapportdefinitie zijn opgegeven, tenzij de rapportdefinitie opgeeft dat de rapportagestructuur van de rijdefinitie moet worden gebruikt. Rij- en kolomdefinities zijn belangrijke onderdelen in het ontwerp en de functionaliteit van financiële rapporten. Rapportagestructuren verhogen de kracht van de onderdelen en ondersteunen flexibele rapportage wanneer de bedrijfsstructuur verandert. Financiële rapporten die niet gebaseerd zijn op een rapportagestructuur gebruiken slechts enkele capaciteiten van financiële rapportage. U kunt meerdere rapportagestructuurdefinities gebruiken samen met dezelfde rij- en kolomdefinities om de gegevens van uw organisatie op verschillende manieren weer te geven.

## <a name="reporting-tree-best-practices"></a>Best practices voor rapportagestructuur
Voordat u een rapportagestructuur maakt, moet u rekening houden met de volgende best practices:

- Definieer eerst welke rapportagedimensies uw rechtspersoon of bedrijf nodig heeft.
- Bedenk hoe u uw structuur opgezet en stel vervolgens een organogram van uw bedrijf op. Het organigram biedt visuele ondersteuning bij het groeperen van de rapporteringseenheden in een of meer rapporteringsstructuren.
- Begin met het laagst beschikbare detailniveau, zoals de afdelingen en projecten die in de financiële gegevens worden gedefinieerd. Voeg zoveel vakken aan het detailniveau toe als nodig, om afdelingen of regio's op een hoger niveau weer te geven. Elk vak vertegenwoordigt een potentiële rapportage-eenheid in elke rapportagestructuur die u maakt.
- U moet ook rekening houden met de beste manier om uw structuren te maken. U kunt een geautomatiseerd opbouwproces gebruiken om een rapportagestructuur te genereren. U kunt ook handmatig een rapportagestructuur maken. Het is belangrijk om beide methoden te begrijpen voordat u uw structuren ontwerpt.
- U kunt de rapportage-eenheden die in uw financiële gegevenssysteem worden gedefinieerd gebruiken om rapportage-eenheden toe te voegen aan de rapportagestructuurdefinitie.

## <a name="create-multiple-reporting-trees"></a>Meerdere rapportagestructuren maken
U kunt een onbeperkt aantal rapportagestructuren maken om de gegevens van uw organisatie op verschillende manieren weer te geven. Elke rapporteringsstructuur kan een willekeurige combinatie van afdelingen en samenvattingseenheden bevatten. Een rapportdefinitie kan een koppeling naar slechts één rapportagestructuur tegelijk bevatten. Door de structuur van de rapportage-eenheden opnieuw te ordenen, kunt u verschillende rapportagestructuren maken. U kunt vervolgens dezelfde rij- en kolomdefinities gebruiken voor elke rapportagestructuur. Op deze manier kunt u snel verschillende indelingen voor financiële rapporten maken. Als u meerdere rapportagestructuren maakt, kunt u elke maand een reeks financiële overzichten afdrukken die de bewerkingen van uw bedrijf op verschillende manieren analyseren en voorstellen. Raadpleeg de voorbeelden van rapportage-eenheidstructuren aan het einde van dit artikel voor meer informatie.

## <a name="create-a-reporting-tree-definition"></a>Een rapportagestructuurdefinitie maken
Een rapportagestructuurdefinitie bevat de kolommen die in de volgende tabel worden omschreven.

| Rapportagestructuurkolom | Beschrijving |
|-----------------------|-------------|
| Bedrijf               | De naam van het bedrijf voor de rapportage-eenheid. Door middel van de waarde **@ANY**, die normaal gesproken alleen op overzichtsniveau wordt toegewezen, kan de rapporteringsstructuur worden gebruikt voor alle bedrijven. Aan alle onderliggende vertakkingen is een bedrijf toegewezen. |
| Naam van eenheid             | De code die deze rapportage-eenheid identificeert in de grafische rapportagestructuur. Zorg ervoor dat u een unieke code vaststelt die consistent is en die gemakkelijk te begrijpen is voor gebruikers. |
| Omschrijving van eenheid      | De titel van de rapportage-eenheid wordt weergegeven in de kop- of voettekst van het rapport als u **UnitDesc** opgeeft als een code in het tabblad **Kop- en voetteksten** van de rapportdefinitie. De titel verschijnt in de omschrijving van de rapportrij als u **UnitDesc** opgeeft in de cel **Omschrijving** van de rijdefinitie. |
| Dimensies            | Een rapportage-eenheid die informatie rechtstreeks uit de financiële gegevens haalt. Deze definieert de logische plaatsing en de lengte voor de rekening en de gerelateerde segmenten. Elke rapportage-eenheidrij moet een dimensie in deze kolom hebben. U kunt ook een dimensie opnemen in een samenvattingseenheidrij (bijvoorbeeld voor uitgaven die rechtstreeks zijn gerelateerd aan die eenheid). Als u een dimensie invoert in een samenvattingseenheidrij, mogen rekeningen die in bovenliggende eenheden worden gebruikt niet in onderliggende eenheden worden gebruikt. Anders kunnen er dubbele bedragen ontstaan. |
| Rijdefinities       | De naam van de rijdefinitie voor de rapportage-eenheid. In alle eenheden van de rapporteringsstructuur wordt dezelfde rijdefinitie gebruikt. Wanneer u een rapport genereert, wordt deze rijdefinitie gebruikt voor elke rapporteringseenheid. De rijdefinitie kan meerdere koppelingen naar financiële dimensies bevatten. Als een rijdefinitie is opgegeven in de rapportagestructuur, schakelt u het selectievakje **Rijdefinitie van rapportagestructuur gebruiken** op het tabblad **Rapport** van de rapportdefinitie in. |
| Rijkoppeling              | De rijkoppeling om voor de rapporteringseenheid te gebruiken. Rijkoppelingen worden gedefinieerd voor de rijdefinitie om de financiële dimensies te identificeren waarmee een koppeling wordt gemaakt. |
| Externe koppeling         | De rijkoppeling om voor deze rapporteringseenheid te gebruiken. Rijkoppelingen worden gedefinieerd voor de rijdefinitie om het rapport te identificeren waarmee moet worden gekoppeld. |
| Extern bestand         | Het bestandspad van het werkblad voor financiële rapportage waaraan gegevens moeten worden ontleend. |
| Paginaopties          | Deze kolom bepaalt of de details voor de rapportage-eenheid worden onderdrukt wanneer het rapport wordt weergegeven of afgedrukt. |
| Samentelling %              | Het percentage van de rapportage-eenheid die aan de bovenliggende eenheid moet worden toegewezen. Het percentage dat u in deze kolom invoert geldt voor elke rij van de rijdefinitie voordat de waarde in de rij aan het bovenliggende rapport wordt toegevoegd. Als een onderliggende eenheid bijvoorbeeld over twee afdelingen moet worden verdeeld, worden de bedragen in elke rij vermenigvuldigd met 50 procent voordat deze aan het afdelingsrapport worden toegevoegd. Eén rapportage-eenheid kan geen twee bovenliggende eenheden hebben. Om de bedragen van een rapportage-eenheid toe te toewijzen aan twee bovenliggende eenheden, maakt u een andere rapportage-eenheid die dezelfde dimensie heeft om de aanvullende 50 procent te totaliseren. Typ gehele percentages zonder een komma. Zo staat bijvoorbeeld **25** voor 25 procent toewijzing aan het bovenliggende object. Als u een komma (**,25**) opneemt, wordt 0,25 procent toegerekend aan het bovenliggende object. Als u een percentage van minder dan 1 procent wilt gebruiken, gebruikt u de optie **Samenstelling &lt;1%** in de rapportdefinitie. Deze optie bevindt zich op het tabblad **Overige opties** in het dialoogvenster **Rapportinstellingen**. U opent dit dialoogvenster met de knop **Overige** op het tabblad **Instellingen** van de rapportdefinitie. |
| Eenheidbeveiliging         | Beperkingen voor de gebruikers en groepen die toegang kunnen krijgen tot de informatie voor de rapportage-eenheid. |
| Extra tekst       | Tekst die in het rapport is opgenomen. |

Als u een rapportagestructuurdefinitie wilt maken, volgt u deze stappen:

1. Open Report Designer.
2. Klik op **Bestand** &gt; **Nieuw** &gt; **Rapportagestructuurdefinitie**.
3. Klik op **Bewerken** &gt; **Rapportage-eenheden uit dimensies invoegen**.
4. Selecteer in het dialoogvenster **Rapportage-eenheden uit dimensies invoegen** het selectievakje voor elke dimensie die u in de rapportagestructuur wilt opnemen. Het dialoogvenster **Rapportage-eenheden uit dimensies invoegen** bevat de volgende secties.

    | Gedeelte                          | Beschrijving |
    |----------------------------------|-------------|
    | Segmentatie rapportagedimensie | Gebruik de knoppen **Segmenten splitsen** en **Segmenten combineren** om het aantal segmenten en de lengte van de segmenten aan te passen.<blockquote>[!NOTE] U kunt alleen segmenten combineren die u hebt gesplitst. Om meerdere dimensies te combineren gebruikt u jokertekens in uw dimensiewaarden.</blockquote> |
    | Opnemen/Tekenpositie       | Deze sectie geeft de dimensies weer die in de financiële gegevens worden gedefinieerd en toont het aantal tekens in de langste waarde die is gedefinieerd voor elke dimensie. Schakel het selectievakje voor een dimensie in om die dimensie op te nemen in de rapportagestructuurhiërarchie. |
    | Segmenthiërarchie en -bereiken     | Deze sectie toont de dimensiehiërarchie. U kunt de dimensies in de lijst verplaatsen om hun rapportagevolgorde te wijzigen. In de velden **Van dimensie** en **Naar dimensie** kunt u een reeks van waarden in elke dimensie opgeven. Als u geen bereik opgeeft, worden alle dimensiewaarden ingevoegd in de rapportagestructuur.<blockquote>[!NOTE] Als u meer dan één dimensie gebruikt, worden alleen de dimensiecombinaties die zijn geboekt in de resultaten weergegeven.</blockquote> |

    Voor een schermopname die een voorbeeld van het dialoogvenster **Rapportage-eenheden uit dimensies invoegen** laat zien, raadpleegt u de sectie 'Voorbeeld van het dialoogvenster Rapportage-eenheden uit dimensies invoegen' verderop in dit artikel.

5. Om aanvullende segmenten te maken (bijvoorbeeld door een segment te splitsen in twee kortere segmenten), klikt u op de juiste locatie in een veld **Tekenpositie** en klikt u vervolgens op **Segmenten splitsen**.
6. Om twee segmenten tot één segment samen te voegen, klikt u in een van de segmentvakken om de segmenten samen te voegen en klikt u vervolgens op **Segmenten combineren**.
7. De hiërarchie bepaalt hoe de dimensies aan elkaar en het bereik voor elke dimensie rapporteren. Als u de hiërarchie van de dimensies wilt wijzigen, selecteert u in het gebied **Segmenthiërarchie en -bereiken**, de dimensie die u wilt verplaatsen en klikt u vervolgens op **Omhoog** of **Omlaag**.
8. Als u een bereik van dimensiewaarden wilt opgeven die aan de nieuwe rapportagestructuur moeten worden toegevoegd, volgt u in het gebied **Segmenthiërarchie en -bereiken** de volgende stappen:

    1. Voer in het veld **Van dimensie** voor die dimensie de eerste waarde in het bereik in.
    2. Voer in het veld **Naar dimensie** de laatste waarde in het bereik in.

9. Herhaal stappen 7 en 8 voor elke dimensie in het gebied **Segmenthiërarchie en -bereiken**.
10. Wanneer u klaar bent met het definiëren van hoe uw rapportage-eenheden in de nieuwe rapportagestructuur moeten worden opgenomen, klikt u op **OK**.
11. Klik op **Bestand** &gt; **Opslaan** om de rapportagestructuur op te slaan. Voer een unieke naam en omschrijving in voor de rapportagestructuur en klik vervolgens op **OK**.

### <a name="open-an-existing-reporting-tree-definition"></a>Een bestaande rapportagestructuurdefinitie openen

1. Klik in Report Designer in het navigatievenster op **Rapportagestructuurdefinities**.
2. Dubbelklik op een naam in de lijst van rapportagestructuren om deze te openen.
3. Als u eventuele bouwstenen wilt weergeven die aan de rapportagestructuur zijn gekoppeld, klikt u met de rechtermuisknop op de rapportagestructuurdefinitie en selecteert u vervolgens **Koppelingen**

### <a name="roll-up-data-in-a-reporting-tree"></a>Gegevens vergaren in een rapportagestructuur

Als u een rapportagestructuur gebruikt, kunt u bedragen van onderliggende rapportage-eenheden samenvoegen op het niveau van de bovenliggende rapportage-eenheid. Deze aggregatie wordt samenvoegen genoemd. De volgende regels worden gebruikt om bedragen samen te voegen met bovenliggende eenheden in een rapportagestructuur:

- In een rapportagestructuur moeten de onderliggende eenheden dimensies bevatten, behalve wanneer de rapportagestructuur een structuur met één niveau betreft. Bovenliggende eenheden bevatten gewoonlijk geen dimensies in een rapportagestructuur.

    > [!NOTE]
    > Als u dimensies opgeeft voor zowel onderliggende eenheden als bovenliggende eenheden, treedt er mogelijk verdubbeling van gegevens op in het rapport.

- Rapportage-eenheden die dimensies in de rapportagestructuur bevatten komen overeen met de dimensies die in de rij- en kolomdefinities worden gebruikt. De combinatie van dimensies bepaalt de bedragen die voor deze eenheid worden geretourneerd. In voorbeeld 2 verderop in dit artikel, retourneren regels 6 en 7 bijvoorbeeld alleen waarden voor afdelingen 00 resp. 01.
- De bedragen voor bovenliggende rapportage-eenheden die geen dimensies in de rapportagestructuur bevatten worden bepaald door het onderliggende eenheidsrapport en voegen het bedrag samen met de opgegeven bovenliggende eenheid. Als de bovenliggende eenheid (zie Contoso USA in voorbeeld 2 van de voorbeelden van het samenvoegen van gegevens) bijvoorbeeld twee onderliggende eenheden (022 en 023) heeft en geen dimensies bevat, wordt een rapport gegenereerd voor elke onderliggende en bovenliggende eenheid. Het bovenliggende totaal is de som van de twee onderliggende bedragen.

### <a name="manage-reporting-units"></a>Rapportage-eenheden beheren

Elke rapportagestructuurdefinitie wordt in unieke weergaven getoond. Er is een grafische weergave die de bovenliggende/onderliggende hiërarchie laat zien en een werkbladweergave die de specifieke informatie voor elke rapportage-eenheid weergeeft. De grafische weergave en de werkbladweergave zijn gekoppeld. Wanneer u in één weergave een rapportage-eenheid selecteert, wordt deze ook in de andere weergave geselecteerd. U kunt hiërarchieën over meerdere dimensies maken die op de dimensionale relaties in de financiële gegevens zijn gebaseerd. Wanneer u een rapportagestructuurdefinitie maakt, kunt u dezelfde rijdefinities meerdere keren gebruiken, ongeacht of u een overzicht van een afdelingsinkomen of een geconsolideerde samenvatting van een inkomensoverzicht genereert. De dimensies die in de rijdefinitie worden gedefinieerd, kunnen met dimensies in de rapportagestructuurdefinitie worden gecombineerd om verschillende weergaven van de prestaties van uw organisatie te bieden.

### <a name="reporting-unit-structure"></a>Structuur van rapportage-eenheid

De volgende typen rapportage-eenheden worden gebruikt in financiële rapportage:

- Een detaileenheid haalt rechtstreeks informatie uit de financiële gegevens, uit een Excel-werkblad of uit een ander werkblad voor financiële rapportage.
- Een samenvattingseenheid vat gegevens van eenheden op een lager niveau samen.

Een bovenliggende rapportage-eenheid is een samenvattingseenheid die informatie van een detaileenheid samenvoegt. Een samenvattingseenheid kan zowel detail- als een samenvattingseenheid zijn. Daarom kan een samenvattingseenheid informatie ontlenen aan een eenheid van een lager niveau, de financiële gegevens of een Excel-werkblad. Een bovenliggende eenheid kan de onderliggende eenheid van een bovenliggende eenheid van een hoger niveau zijn. Een onderliggende rapportage-eenheid kan een detaileenheid zijn die rechtstreeks informatie uit de financiële gegevens of een Excel-werkblad haalt. Een onderliggende rapportage-eenheid kan ook een tussenliggende samenvattingseenheid zijn. Met andere woorden, het kan de bovenliggende eenheid zijn van een eenheid van een lager niveau en tevens de onderliggende eenheid van een samenvattingseenheid van een hoger niveau. In het bekendste scenario voor rapportage-eenheden hebben bovenliggende eenheden een lege cel in de kolom **Dimensies** en hebben onderliggende eenheden koppelingen naar specifieke combinaties of dimensies met jokertekens.

### <a name="organize-reporting-units"></a>Rapportage-eenheden indelen

U kunt de organisatiestructuur van een rapportagestructuurdefinitie herschikken door rapportage-eenheden in de grafische weergave te verplaatsen. U kunt ook rapportage-eenheden naar een hoger niveau in de rapportagestructuur promoveren of deze naar een lager niveau in de rapportagestructuur verplaatsen.

1. Open in Report Designer de rapportagestructuurdefinitie die u wilt wijzigen.
2. Selecteer een rapportage-eenheid in de grafische weergave van de rapportagestructuurdefinitie.
3. Sleep de eenheid naar een nieuwe positie. U kunt ook met de rechtermuisknop op de eenheid klikken en vervolgens **Rapportage-eenheid promoveren** of **Rapportage-eenheid niveau verlagen** selecteren.
4. Klik op **Bestand** &gt; **Opslaan** om uw wijzigingen op te slaan.

### <a name="add-text-about-a-reporting-unit"></a>Tekst over een rapportage-eenheid toevoegen

Een extra tekstinvoer is een statische tekenreeks van maximaal 255 tekens die informatie toevoegt aan de rapportagestructuurdefinitie. De extra tekst kan bijvoorbeeld een korte omschrijving van het bedrijf zijn. U kunt maximaal tien extra tekstinvoeren voor elke rapportage-eenheid in een rapportagestructuurdefinitie maken. De extra tekst wordt weergegeven in het rapport voor de rapportage-eenheid waaraan de tekst is toegewezen. U kunt tekstinvoeren toevoegen vanuit de kolom **Omschrijving** van de rijdefinitie en vanaf het tabblad **Kop- en voetteksten** in de rapportdefinitie.

1. Open in Report Designer de rapportagestructuurdefinitie die u wilt wijzigen.
2. Dubbelklik op de cel **Extra tekst** voor de rapportage-eenheidrij.
3. Voer de tekst in de eerste lege rij van het dialoogvenster **Extra tekst** in. Naar de eerste rij die tekst bevat wordt verwezen als UnitText1, ongeacht de positie ervan in het dialoogvenster **Extra tekst**.
4. Als u meer tekstinvoeren voor deze rapportage-eenheid wilt toevoegen, voert u de tekst in een lege rij in.
5. Klik tot slot op **OK**.

### <a name="remove-additional-text-from-a-reporting-unit"></a>Extra tekst verwijderen uit een rapportage-eenheid

1. Open in Report Designer de rapporteringsstructuurdefinitie die u wilt wijzigen.
2. Dubbelklik op de cel **Aanvullende tekst** voor de rij van de rapporteringseenheid.
3. Selecteer in het dialoogvenster **Extra tekst** de te verwijderen invoer en klik vervolgens op **Wissen**. U kunt ook met de rechtermuisknop op de invoer klikken en vervolgens **Knippen** selecteren.
4. Klik tot slot op **OK**.

### <a name="restrict-access-to-a-reporting-unit"></a>Toegang tot een rapportage-eenheid beperken

U kunt voorkomen dat bepaalde gebruikers en groepen een rapportage-eenheid openen. U kunt ook beperkingen definiëren zodat deze van toepassing zijn op onderliggende rapportage-eenheden van de rapportage-eenheid.

1. Open in Report Designer de rapportagestructuurdefinitie die u wilt wijzigen.
2. Dubbelklik op de cel **Beveiliging van eenheid** voor de rij van de rapporteringseenheid waarvoor u de toegang wilt beperken.
3. Klik in het dialoogvenster **Eenheidbeveiliging** op **Gebruikers en groepen**.
4. Selecteer de gebruikers of groepen die toegang tot de beperkte rapportage-eenheid moeten hebben en klik vervolgens op **OK**.
5. Als u de toegang tot onderliggende rapportage-eenheden wilt beperken, schakelt u het selectievakje **Beveiliging toevoegen aan onderliggende rapportage-eenheden** in.
6. Klik tot slot op **OK**.

### <a name="remove-access-to-a-reporting-unit"></a>Toegang tot een rapportage-eenheid verwijderen

1. Open in Report Designer de rapportagestructuurdefinitie die u wilt wijzigen.
2. Dubbelklik op de cel **Eenheidbeveiliging** voor de rapportage-eenheidrij waarvan u de toegang wilt verwijderen.
3. Selecteer in het dialoogvenster **Eenheidbeveiliging** een naam en klik vervolgens op **Verwijderen**.
4. Klik tot slot op **OK**.

### <a name="link-toreports"></a>Koppelen aan rapporten

Nadat u een  **rapport**kolom hebt gemaakt in de rijdefinitie en het rapport hebt opgegeven voor opname in het rapport, moet u de rapportagestructuur bijwerken met de gekoppelde kolom en de informatie over het rapport. Een rapport kan worden geïmporteerd in elke eenheid in de rapportagestructuur.

### <a name="identify-the-report-in-a-reporting-tree"></a>Het rapport identificeren in een rapportagestructuur

1. Open in Report Designer de rapportagestructuurdefinitie die u wilt wijzigen.
2. In de kolom **Rijdefinities** is de informatie in de cellen gebaseerd op de informatie voor de geselecteerde rij, omdat dezelfde rijdefinitie moet worden gebruikt in alle eenheden van de rapportagestructuur. Dubbelklik op de cel **Rijdefinities** en selecteer vervolgens de rijdefinitie die informatie over het rapport bevat.
3. Selecteer in de cel **Werkbladkoppeling** voor een rapportage-eenheid de naam van de koppeling die overeenkomt met het rapport.
4. Voer in de cel **Werkmap- of rapportpad** voor een rapportage-eenheid de naam van het rapport in of blader om het rapport te selecteren.
5. Voer, als u een werkblad in een rapport wilt opgeven, de naam van het werkblad in de cel **Naam van werkblad** in.
6. Herhaal stappen 3 tot en met 5 voor elke rapportage-eenheid die gegevens uit een rapport moet ontvangen. Om te voorkomen dat foutieve gegevens in het rapport worden weergegeven, moet u ervoor zorgen dat de juiste namen van rapporten worden weergegeven in de bijbehorende eenheid van de rapportage-structuur.

## <a name="examples"></a>Voorbeelden
### <a name="reporting-unit-structure--example-1"></a>Structuur van rapportage-eenheid – Voorbeeld 1

Hier is de structuur van de rapportage-eenheden in de volgende rapportagestructuur:

- De rapportage-eenheid Contoso Japan is een bovenliggende eenheid van de onderliggende eenheden Contoso Japan Sales en Contoso Japan Consulting.
- De afdelingseenheid Contoso Japan Sales is zowel een onderliggende eenheid van de eenheid Contoso Japan als een bovenliggende eenheid van de eenheden Home Sales en Auto Sales.
- De rapportage-eenheden op het laagste detailniveau (Home Sales, Auto Sales, Client Services en Operations) zijn afdelingen in de financiële gegevens. Deze rapportage-eenheden bevinden zich in het gearceerde gebied van het diagram.
- De samenvattingseenheden op hoger niveau vatten informatie van de detaileenheden samen.

[![ContosoEntertainmentSummaryReportStructure](./media/contosoentertainmentsummaryreportstructure.png)](./media/contosoentertainmentsummaryreportstructure.png)

### <a name="reporting-unit-structure--example-2"></a>Structuur van rapportage-eenheid – Voorbeeld 2

In het volgende diagram heeft de rapportagestructuur een organisatiestructuur die op bedrijfsfunctie is verdeeld.

[![summaryofallunitscontoso](./media/summaryofallunitscontoso.png)](./media/summaryofallunitscontoso.png)

### <a name="example-of-the-insert-reporting-units-from-dimensions-dialog-box"></a>Voorbeeld van het dialoogvenster Rapportage-eenheden uit dimensies invoegen

De volgende afbeelding toont een voorbeeld van het dialoogvenster **Rapportage-eenheden uit dimensies invoegen**. In dit voorbeeld retourneren de resultaten de combinatie van business units, kostenplaatsen en afdelingen.

[![InsertReportingUnits](./media/insertreportingunits.png)](./media/insertreportingunits.png)

De resulterende rapportagestructuurdefinitie is gesorteerd op business unit, vervolgens op kostenplaats en tot slot op afdeling. De dimensie voor de vijfde rapportage-eenheid is **Bedrijfseenheid = \[001\], Kostenplaats =\[\], Afdeling = \[022\]** en identificeert een rapportage-eenheid voor rekeningen die specifiek zijn voor bedrijfseenheid 001 en afdeling 022.

[![ReportingTree](./media/reportingtree-1024x646.png)](./media/reportingtree.png)

### <a name="examples-of-data-roll-up"></a>Voorbeelden van samenvoeging van gegevens

De volgende voorbeelden geven mogelijke informatie weer die worden gebruikt in een rapportagestructuurdefinitie voor het samenvoegen van gegevens.

#### <a name="example-1"></a>Voorbeeld 1

[![MutliCompanyRollUp](./media/mutlicompanyrollup.png)](./media/mutlicompanyrollup.png)

#### <a name="example-2"></a>Voorbeeld 2

[![CrossCompanyDepartmentRollUp](./media/crosscompanydepartmentrollup.png)](./media/crosscompanydepartmentrollup.png)

## <a name="additional-resources"></a>Aanvullende resources

[Financiële rapportage](financial-reporting-intro.md)
