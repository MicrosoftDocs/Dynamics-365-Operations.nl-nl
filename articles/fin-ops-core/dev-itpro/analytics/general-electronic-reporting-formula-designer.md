---
title: Formuleontwerper in elektronische rapportage (ER)
description: Dit artikel biedt algemene informatie over het gebruik van de formuleontwerper in ER (Elektronische rapportage).
author: kfend
ms.date: 04/08/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
ms.openlocfilehash: 283c882300ece460c18ffebe572238e7629f8dee
ms.sourcegitcommit: a1d14836b40cfc556f045c6a0d2b4cc71064a6af
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/14/2022
ms.locfileid: "9476796"
---
# <a name="formula-designer-in-electronic-reporting-er"></a>Formuleontwerper in elektronische rapportage (ER)

[!include [banner](../includes/banner.md)]

In dit artikel wordt beschreven hoe de formuleontwerper in elektronische rapportage (ER) wordt gebruikt. Wanneer u een indeling voor een specifiek elektronisch document in ER ontwerpt, kunt u formules gebruiken om gegevens te transformeren om te voldoen aan de vereisten voor de afhandeling en opmaak van het document. Deze formules lijken op formules in Microsoft Excel. Er worden diverse typen functies ondersteund in de formules: tekst, datum en tijd, wiskundig, logisch, informatie, gegevenstypeconversie en andere functies (specifiek voor het zakelijke domein).

## <a name="formula-designer-overview"></a>Overzicht van formuleontwerper

ER ondersteunt de Formuleontwerper. Daarom kunt u tijdens het ontwerpen expressies configureren die kunnen worden gebruikt voor de volgende taken in runtime:

- Het transformeren van gegevens die zijn ontvangen van een toepassingsdatabase en die moeten worden ingevoerd in een ER-gegevensmodel dat is ontworpen als een gegevensbron voor ER-indelingen. (Deze transformaties kunnen bijvoorbeeld filteren, groeperen en conversie van gegevenstype omvatten.)
- Gegevens opmaken die moet worden verzonden naar een genererend elektronisch document conform de indeling en de voorwaarden van een specifieke ER-indeling. (Bijvoorbeeld de opmaak kan worden uitgevoerd in overeenstemming met de aangevraagde taal of cultuur, of de codering.)
- Het proces van het maken van elektronische documenten beheren. (Bijvoorbeeld de expressies kunnen de uitvoer van specifieke elementen van de indeling inschakelen of uitschakelen, afhankelijk van de verwerking van gegevens. Ze kunnen ook het proces voor het maken van documenten onderbreken of berichten aan gebruikers tonen.)

U kunt de pagina **Formuleontwerper** openen wanneer u een van de volgende handelingen uitvoert:

- De binding van gegevensbronartikelen aan gegevensmodelonderdelen.
- De binding van gegevensbronartikelen aan indelingsonderdelen.
- Het onderhoud van berekende velden die deel uitmaken van gegevensbronnen.
- De definitie van zichtbaarheids- en bewerkbaarheidsvoorwaarden voor gebruikersinvoerparameters.
- De definitie van standaardwaarden voor gebruikersinvoerparameters.
- Het ontwerp van transformaties van de indeling.
- De definitie van voorwaarden voor het inschakelen van de indelingsonderdelen.
- De definitie van bestandsnamen voor de bestandsonderdelen van de indeling.
- De definitie van de voorwaarden voor procescontrolevalidaties.
- De definitie van de berichttekst voor procescontrolevalidaties.

## <a name="data-binding"></a><a name="Binding"></a>Gegevensbinding

De ER-formuleontwerper kan worden gebruikt om een expressie te definiëren voor de transformatie van gegevens die worden ontvangen van gegevensbronnen, zodat de gegevens tijdens runtime op de volgende manieren in de gegevensconsument kunnen worden ingevoerd:

- Vanuit toepassingsgegevensbronnen en uitvoeringsparameters naar een ER-gegevensmodel
- Vanuit een ER-gegevensmodel naar een ER-indeling
- Vanuit toepassingsgegevensbronnen en uitvoeringsparameters naar een ER-indeling

De volgende afbeelding toont het ontwerp van een expressie van dit type. In dit voorbeeld rondt de expressie de waarde van het veld **Intrastat.AmountMST** in de Intrastat-tabel af op twee decimalen en wordt de afgeronde waarde geretourneerd.

[![De expressie Gegevensbinding.](./media/picture-expression-binding.jpg)](./media/picture-expression-binding.jpg)

De volgende afbeelding toont hoe een expressie van dit type kan worden gebruikt. In dit voorbeeld wordt het resultaat van de ontworpen expressie ingevoerd in het onderdeel **Transaction.InvoicedAmount** van het gegevensmodel **Belastingrapportagemodel**.

[![De expressie Gegevensbinding wordt gebruikt.](./media/picture-expression-binding2.jpg)](./media/picture-expression-binding2.jpg)

Tijdens runtime rondt de ontworpen formule, `ROUND (Intrastat.AmountMST, 2)`, de waarde van het veld **AmountMST** voor elke record in de Intrastat-tabel af op twee decimalen. Vervolgens wordt de afgeronde waarde ingevoerd in het onderdeel **Transaction.InvoicedAmount** van het gegevensmodel **Btw-aangifte**.

## <a name="data-formatting"></a><a name="Transformation"></a>Gegevensnotatie

De ER-formuleontwerper kan worden gebruikt om een expressie te definiëren voor de opmaak van gegevens die worden ontvangen van gegevensbronnen, zodat de gegevens kunnen worden verzonden als onderdeel van het genererende elektronische document. U hebt wellicht opmaak die moet worden toegepast als een normale regel die opnieuw moet worden gebruikt voor een indeling. U kunt in dit geval die opmaak één keer in de indelingsconfiguratie introduceren als een benoemde transformatie die een opmaakexpressie heeft. Deze benoemde transformatie kan vervolgens worden gekoppeld aan vele indelingscomponenten waarvan de uitvoer moet worden opgemaakt volgens de opmaakexpressie die u hebt gemaakt.

De volgende afbeelding toont het ontwerp van een transformatie van dit type. In dit voorbeeld kapt de transformatie **TrimmedString** inkomende gegevens van het gegevenstype *Tekenreeks* af door spaties vooraan en achteraan te verwijderen. Vervolgens wordt de afgekapte waarde geretourneerd.

[![Transformatie.](./media/picture-transformation-design.jpg)](./media/picture-transformation-design.jpg)

De volgende afbeelding toont hoe een transformatie van dit type kan worden gebruikt. In dit voorbeeld wordt met verschillende opmaakonderdelen tijdens runtime tekst als uitvoer verzonden naar het genererende elektronische document. Alle opmaakonderdelen verwijzen bij naam naar de transformatie **TrimmedString**.

[![Transformatie wordt gebruikt.](./media/picture-transformation-usage.jpg)](./media/picture-transformation-usage.jpg)

Wanneer indelingsonderdelen, zoals het onderdeel **partyName** in de vorige illustratie, verwijzen naar de transformatie **TrimmedString**, verzendt de transformatie tekst als uitvoer naar het genererende elektronische document. Deze tekst bevat geen spaties vooraan en achteraan.

Als u een opmaak hebt die afzonderlijk moet worden toegepast, kan deze opmaak als een afzonderlijke expressie van een binding van een specifieke indelingscomponent worden geïntroduceerd. De volgende afbeelding toont een expressie van dit type. In dit voorbeeld is het indelingsonderdeel **partyType** gebonden aan de gegevensbron via een expressie waarmee inkomende gegevens vanuit het veld **Model.Company.RegistrationType** in de gegevensbron worden geconverteerd naar tekst in hoofdletters. Vervolgens wordt die tekst als uitvoer verzonden naar het elektronische document.

[![Opmaak toepassen op een afzonderlijke component.](./media/picture-binding-with-formula.jpg)](./media/picture-binding-with-formula.jpg)

## <a name="process-flow-control"></a><a name="Validation"></a>Processtroombeheer

De ER-formuleontwerper kan worden gebruikt om expressies te definiëren die de processtroom beheren voor het genereren van elektronische documenten. U kunt de volgende taken uitvoeren:

- Definieer voorwaarden die bepalen wanneer het maken van een document moet worden gestopt.
- Geef expressies op waarmee berichten voor gebruikers over gestopte processen of uitvoeringslogboekberichten over het voortzetten van het genereren van rapporten worden gemaakt.
- Geef de bestandsnamen op van genererende elektronische documenten en beheer de voorwaarden voor het maken hiervan.

Elke regel van het processtroombeheer is ontworpen als afzonderlijke validatie. De volgende afbeelding toont een validatie van dit type. Hier volgt een uitleg van de configuratie in dit voorbeeld:

- De validatie wordt geëvalueerd als het knooppunt **INSTAT** tijdens het genereren van het XML-bestand wordt gemaakt.
- Als de lijst met transacties leeg is, stopt de validatie het uitvoeringsproces en retourneert **FALSE**.
- De validatie retourneert een foutbericht dat de tekst van label SYS70894 bevat in de voorkeurstaal van de gebruiker.

[![Validatie.](./media/picture-validation.jpg)](./media/picture-validation.jpg)

De ER-formuleontwerper kan ook worden gebruikt om een bestandsnaam te genereren voor een genererend elektronisch document en om het proces voor het maken van bestanden te beheren. De volgende afbeelding toont het ontwerp van een processtroombesturingselement van dit type. Hier volgt een uitleg van de configuratie in dit voorbeeld:

- De lijst met records uit de gegevensbron **model.Intrastat** is verdeeld in batches. Elke batch bevat maximaal 1000 records.
- De uitvoer maakt een zipbestand dat een bestand in XML-indeling bevat voor elke batch die is gemaakt.
- Een expressie retourneert een bestandsnaam voor genererende elektronische documenten door de bestandsnaam en bestandsextensie aaneen te schakelen. Voor de tweede en alle volgende batches bevat de bestandsnaam de batch-id als achtervoegsel.
- Een expressie activeert (door **TRUE** te retourneren) het maken van een bestand voor batches die ten minste één record bevatten.

[![Processtroombeheer.](./media/picture-file-control.jpg)](./media/picture-file-control.jpg)

## <a name="document-content-control"></a><a name="Enabled"></a>Besturingselement voor documentinhoud

U kunt de ER-formuleontwerper gebruiken om expressies te configureren die bepalen welke gegevens tijdens runtime in gegenereerde elektronische documenten worden geplaatst. De expressies kunnen de uitvoer van specifieke elementen van de indeling inschakelen of uitschakelen, afhankelijk van de verwerking van gegevens en de geconfigureerde logica. Deze expressies kunnen worden ingevoerd voor één opmaakelement in het veld **Ingeschakeld** op het tabblad **Toewijzing** van de pagina **Operations-ontwerper**. U de expressies invoeren als een logische voorwaarde die een *Booleaanse* waarde retourneert:

- Als de voorwaarde **True** retourneert, wordt het huidige indelingselement uitgevoerd.
- Als de voorwaarde **False** retourneert, wordt het huidige indelingselement overgeslagen.

De volgende afbeelding toont expressies van dit type. (Versie 11.12.11 van de **ISO20022-indelingsconfiguratie voor kredietoverdrachtbetalingen (NO)** die wordt geleverd door Microsoft wordt gebruikt als voorbeeld.) Het indelingsonderdeel **XMLHeader** is zo geconfigureerd dat de structuur van het bericht over de kredietoverdracht wordt beschreven volgens de norm ISO 20022 XML-berichtstandaarden. De indelingsonderdeel **XMLHeader/Document/CstmrCdtTrfInitn/PmtInf/CdtTrfTxInf/RmtInf/Ustrd** is geconfigureerd om het XML-element **Ustrd** toe te voegen aan het gegenereerde bericht, en de remisegegevens in een niet-gestructureerde indeling te plaatsen als tekst van de volgende XML-elementen:

- Het onderdeel **PaymentNotes** wordt gebruikt om de tekst van betalingsnotities te genereren.
- Het onderdeel **DelimitedSequence** genereert door komma's gescheiden factuurnummers die worden gebruikt om de huidige kredietoverdracht te vereffenen.

[![De onderdelen PaymentNotes en DelimitedSequence.](./media/GER-FormulaEditor-ControlContent-1.png)](./media/GER-FormulaEditor-ControlContent-1.png)

> [!NOTE]
> De onderdelen **PaymentNotes** en **DelimitedSequence** worden aangeduid met een vraagteken. Een vraagteken geeft aan dat het gebruik van een onderdeel voorwaardelijk is. In dit geval wordt het gebruik van de onderdelen gebaseerd op de volgende criteria:
>
> - Door de expressie `@.PaymentsNotes <> ""`, die is gedefinieerd voor het onderdeel **PaymentNotes**, kan door **TRUE** te retourneren het XML-element **Ustrd** worden gevuld met de tekst van betalingsnotities, als deze tekst niet leeg is voor de huidige kredietoverdracht.
>
>    [![Expressie voor het onderdeel PaymentNotes.](./media/GER-FormulaEditor-ControlContent-2.png)](./media/GER-FormulaEditor-ControlContent-2.png)
>
> - Door de expressie `@.PaymentsNotes = ""`, die is gedefinieerd voor het onderdeel **DelimitedSequence**, kan door **TRUE** te retourneren het XML-element **Ustrd** worden gevuld met een door komma's gescheiden lijst met de factuurnummers die worden gebruikt om de huidige kredietoverdracht te vereffenen, als de tekst van betalingsnotities voor die kredietoverdracht leeg is.
>
>    [![Expressie voor het onderdeel DelimitedSequence.](./media/GER-FormulaEditor-ControlContent-3.png)](./media/GER-FormulaEditor-ControlContent-3.png)
> 
> Op basis van deze instelling bevat het gegenereerde bericht voor alle debiteurenbetalingen het XML-element **Ustrd**, de tekst van de betalingsnotities of, wanneer deze tekst leeg is, een door komma's gescheiden lijst met factuurnummers die worden gebruikt om de betaling te vereffenen.

## <a name="assistance-in-formulas-writing"></a>Hulp bij het schrijven van formules

### <a name="data-sources-navigator"></a>Navigator voor gegevensbronnen

U kunt een formule bewerken die een element van een gestructureerde gegevensbron vertegenwoordigt. Wanneer u de ER-parameters hebt geconfigureerd om het pad naar een element van een gestructureerde gegevensbron te presenteren als het [relatieve pad](relative-path-data-bindings-er-models-format.md), wordt het apestaartje-teken (@) [weergegeven](er-formula-language.md#relative-path) in de formule, in plaats van het resterende deel van het absolute pad van de hiërarchische boomstructuur die wordt gebruikt. Het resterende deel van het absolute pad wijst naar een bovenliggend element van het bewerkbare pad. In Finance, versie **10.0.30 en hoger** kunt u op de pagina **Formuleontwerper**, in het deelvenster **Gegevensbronnen**, de optie **Ga naar @** selecteren om de cursor van de gegevensbronnenstructuur te plaatsen in een element dat het bovenliggende element van het bewerkbare element is. De structuur van alle samengevouwen oplopende elementen wordt automatisch en recursief uitgevouwen als dat nodig is. Door dit uit te vouwen, kunt u snel het basiselement van het bewerkbare element visualiseren, elementen op hetzelfde niveau als het bewerkbare element in de gegevensbronnenstructuur bekijken en elk van deze elementen zo nodig in de formule voor het bewerkbare element gebruiken.

![Gebruik de optie 'Ga naar@' om de cursor van de gegevensbronnenstructuur te plaatsen op een element dat het bovenliggende element van het bewerkbare element is op de pagina Formuleontwerper.](./media/er_formula-designer-data-sources-navigator.gif)

### <a name="data-sources-picker"></a>Kiezer voor gegevensbronnen

Selecteer op de pagina **Formuleontwerper** in het deelvenster **Gegevensbronnen** aan de linkerkant een element van een gegevensbron dat u wilt toevoegen aan de bewerkbare formule. Selecteer vervolgens **Gegevensbron toevoegen**. Het geselecteerde element is toegevoegd aan de tekst van de bewerkbare formule.

> [!TIP]
> Wanneer u de optie **Gegevensbron toevoegen** gebruikt in de standaardformule-editor, wordt het geselecteerde element altijd toegevoegd aan het einde van de formuletekst. Wanneer u hetzelfde doet in de [geavanceerde formule-editor](er-advanced-formula-editor.md), wordt het geselecteerde element ingevoegd in de formuletekst op de actuele cursorpositie.

### <a name="built-in-functions-picker"></a>Kiezer voor ingebouwde functies

Selecteer op de pagina **Formuleontwerper** in het deelvenster **Functies** aan de rechterkant een ingebouwde ER-functie die u wilt toevoegen aan de bewerkbare formule. Selecteer vervolgens **Functie toevoegen**. De geselecteerde functie is toegevoegd aan de tekst van de bewerkbare formule.

> [!TIP]
> Wanneer u de optie **Functie toevoegen** gebruikt in de standaardformule-editor, wordt de geselecteerde functie altijd toegevoegd aan het einde van de formuletekst. Wanneer u hetzelfde doet in de [geavanceerde formule-editor](er-advanced-formula-editor.md), wordt de geselecteerde functie ingevoegd in de formuletekst op de actuele cursorpositie.

### <a name="validation-of-configured-formulas"></a><a name="TestFormula"></a>Validatie van geconfigureerde formules

Selecteer op de pagina **Formuleontwerper** de optie **Testen** om te valideren hoe de geconfigureerde formule werkt.

[![Test selecteren om een formule te valideren.](./media/ER-FormulaTest-Start.png)](./media/ER-FormulaTest-Start.png)

Wanneer de waarden van formuleargumenten vereist zijn, kunt u het dialoogvenster **Expressie testen** openen via de pagina **Formuleontwerper**. In de meeste gevallen moeten deze argumenten handmatig worden gedefinieerd, omdat de geconfigureerde bindingen niet worden uitgevoerd tijdens de ontwerpperiode. Op het tabblad **Testresultaat** op de pagina **Formuleontwerper** wordt het resultaat van de uitvoering van de geconfigureerde formule weergegeven.

In het volgende voorbeeld ziet u hoe u de formule kunt testen die is geconfigureerd voor het buitenlandse handelsdomein om ervoor te zorgen dat de Intrastat-basisproductcode alleen cijfers bevat.

Wanneer u deze formule test, kunt u het dialoogvenster **Expressie testen** gebruiken om de waarde van de Intrastat-basisproductcode voor het testen op te geven.

[![De Intrastat-basisproductcode voor het testen opgeven.](./media/ER-FormulaTest-Start-EnterArguments.png)](./media/ER-FormulaTest-Start-EnterArguments.png)

Nadat u de Intrastat-basisproductcode hebt opgegeven en **OK** hebt geselecteerd, wordt op het tabblad **Testresultaat** op de pagina **Formuleontwerper** het resultaat van de uitvoering van de geconfigureerde formule weergegeven. U kunt vervolgens beoordelen of het resultaat acceptabel is. Als het resultaat niet acceptabel is, kunt u de formule bijwerken en opnieuw testen.

[![Testresultaat.](./media/ER-FormulaTest-Result.png)](./media/ER-FormulaTest-Result.png)

Sommige formules kunnen niet worden getest tijdens de ontwerpperiode. Een formule kan bijvoorbeeld een resultaat opleveren van een gegevenstype dat niet kan worden weergegeven op het tabblad **Testresultaat**. In dit geval wordt een foutbericht weergegeven waarin wordt gesteld dat de formule niet kan worden getest.

[![Foutmelding.](./media/ER-FormulaTest-Error.png)](./media/ER-FormulaTest-Error.png)

## <a name="additional-resources"></a>Aanvullende bronnen

- [Overzicht van elektronische rapportage](general-electronic-reporting.md)
- [Formuletaal in Elektronische rapportage](er-formula-language.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
