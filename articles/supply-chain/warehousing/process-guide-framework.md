---
title: ProcessGuide-raamwerk
description: Dit artikel bevat informatie over het ProcessGuide-framework voor ontwikkelaars die onze mobiele magazijnprocessen in X++ uitbreiden.
author: Mirzaab
ms.date: 11/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: mirzaab
ms.search.validFrom: 2018-4-30
ms.dyn365.ops.version: 8
ms.openlocfilehash: e88f32e0347a808d03615cf85e50b1592d691670
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8860430"
---
# <a name="process-guide-framework"></a>ProcessGuide-raamwerk

[!include [banner](../includes/banner.md)]

Dit artikel bevat informatie over het ProcessGuide-framework voor ontwikkelaars die de mobiele magazijnprocessen in X++ uitbreiden. De mobiele processen voor magazijnen zijn uitbreidbaar omdat de processen in kleine stappen worden opgesplitst. De opbouw van elke stap in de bedrijfslogica en de gebruikersinterface is opgesplitst in afzonderlijke klassen, wat uitbreiding mogelijk maakt.

## <a name="overview-of-the-existing-design"></a>Overzicht van het bestaande ontwerp

De mobiele uitvoeringsstromen voor magazijnen worden via één aangepast service-eindpunt zichtbaar gemaakt. De aanvraag komt binnen vanuit de mobiele app in de vorm van een XML-tekenreeks, die de metagegevens bevat van de gebruikersinterface die wordt weergegeven in de mobiele app en de waarden die door de gebruiker zijn ingevoerd.

Wanneer de aanvraag is ontvangen, is de eerste stap het deserialiseren van deze XML. Met de klasse **WHSMobileAppServiceXMLTranslator** wordt de XML omgezet in een container, die zowel de controlegegevens als de sessiegegevens bevat.

De gegevens in de container worden vervolgens gebruikt om na te gaan aan welk magazijnproces de gebruiker werkt of op het punt staat te gaan werken (vertegenwoordigd door de opsomming **WHSWorkExecuteMode**) en om op basis daarvan een afgeleide klasse van **WHSWorkExecuteDisplay** te instantiëren. De methode **displayform()** wordt aangeroepen, die vervolgens:

-   de gegevens van de gebruiker verwerkt (gedelegeerd naar de klasse **WHSRFControlData**, maar sommige processen implementeren specifieke logica door de methode **processControl()** te overschrijven);

-   de bedrijfslogica uitvoert;

-   de stap verhoogt;

-   de container bouwt die de nieuwe gebruikersinterface vertegenwoordigt (meestal in een **build...()**-methode).

De container wordt vervolgens geretourneerd naar de vertaler, die vervolgens de XML serialiseert en terugstuurt als een respons naar het mobiele apparaat.

Het volgende volgordediagram toont een overzicht van de uitvoeringsstroom. Houd er rekening mee dat het diagram meer een schematisch overzicht is en geen een-op-eenweergave is van de werkelijke code.

![Schematisch overzicht van het proces.](media/schematic-overview.png) 

### <a name="reason-for-the-redesign"></a>Reden van het nieuwe ontwerp

Het bovenstaande ontwerp biedt een zeer eenvoudig framework voor het bouwen van processen die in mobiele stromen worden gebruikt. Zoals uit het bovenstaande blijkt, nemen de **Displayform()**-methoden echter meerdere verantwoordelijkheden over. Er worden wel verantwoordelijkheden gedelegeerd naar andere methoden en klassen, maar bij gebrek aan concrete klasseverantwoordelijkheden gebeurt dit op een inconsistente manier voor alle klassen. Bovendien kunnen door de organische groei van het aantal ondersteunde scenario's, sommige van deze klassen ook erg complex worden. Om het nog interessanter te maken, worden sommige van deze klassen/methoden overschreven en opnieuw gebruikt op meerdere manieren. Het resultaat is buitengewoon lange methoden met een hoge cyclomatische complexiteit. Hierdoor zijn er in het verleden problemen met het onderhoud geweest. Het repareren van bugs in deze methoden is riskant en kan leiden tot regressie.
Naar de methode **processWorkLine()** in de klasse **WhsWorkExecuteDisplay** wordt bijvoorbeeld verwezen vanuit meerdere processen (in feite overal waar werk wordt uitgevoerd).

Om deze uitbreidbaar te maken, is een van de opties het splitsen van de **displayForm**-methoden in kleinere methoden en het introduceren van uitbreidbaarheidspunten. Vanwege de scenariomatrix kan het echter lastig zijn voor partners om uitbreidingen te schrijven en deze te toetsen aan regressies. En dat niet alleen, want vanwege een gebrek aan de hierboven genoemde gestructureerde verantwoordelijkheidsverdeling, zal de code steeds verder groeien, wat het lastig maakt om kwalitatief goede uitbreidingen te bouwen.

Daarom is dit nieuwe ontwerp een duurzame optie, met als doel om duidelijk gedefinieerde klassen te bieden die onafhankelijke verantwoordelijkheden hebben. Een klasse dient één verantwoordelijkheid te hebben, één reden om te veranderen en één reden om te worden uitgebreid.

## <a name="design-overview"></a>Ontwerpoverzicht

In het opnieuw ontworpen framework bestaat de basisstrategie uit twee principes: de uitvoeringsstroom onderverdelen in afzonderlijke onderdelen met welbepaalde verantwoordelijkheden, en welbepaalde uitbreidingspunten bieden voor elk van de onderdelen.

De naam voor het nieuwe framework is 'ProcessGuide', oftewel'procesgids'. Deze naam is gekozen omdat het doel van deze klassen is het gidsen van een gebruiker door een bedrijfsproces (in tegenstelling tot een rich client die een op een formulier gebaseerde ervaring biedt waarbij de gebruiker meer flexibiliteit heeft bij de interactie met de gegevens en het bepalen van de volgorde waarin deze taken uitvoeren).

> [!NOTE]
> Een noemenswaardig detail is het doelbewust weglaten van het voorvoegsel 'WHS'. De mobiele processen werden in eerste instantie geïntroduceerd voor magazijnbeheer, maar nu worden er verschillende productie- en voorraadbeheerprocessen ondersteund. Daarom is de magazijnverwijzing weggelaten in de naam van het framework.

Als u de onderdelen wilt identificeren, is de eerste stap het bekijken van het productiestartproces (de klasse **WhsWorkExecuteDisplayProdStart**). Hier is een schema van het proces.

![Afbeelding van schematisch proces.](media/production-start-process-schematic.png)

Als je naar de controlestroom kijkt, zijn de volgende onderdelen nodig:

-   Een controller om een samenhangend geheel te maken van het gehele bedrijfsproces.
-   Een stap die verantwoordelijk is voor de uitvoering van een stap in het proces.
-   Een gegevensverwerker voor de verwerking van de gegevens in een stap.
-   Een paginabouwer die verantwoordelijk is voor het maken van de gebruikersinterface voor een stap.
-   Een navigatie-agent die verantwoordelijk is voor de overgangen tussen de stappen.
-   Een klasse die verantwoordelijk is voor de uitvoering van het bedrijfsproces.

Als u in het bovenstaande processtroomdiagram begint bij stap 1 en start met het verwerken van de gegevens uit de vorige stap en vervolgens eindigt met het maken van een gebruikersinterface, zullen de gegevens in de volgende stap verder worden verwerkt. Hierdoor ontstaat een hechte koppeling tussen opeenvolgende stappen en daardoor ziet het nieuwe schema er als volgt uit:

![Afbeelding van het schematische proces op een hoog niveau.](media/high-level-schematic.png)

Hierna volgen de belangrijkste onderdelen in het opnieuw ontworpen proces:

-   **ProcessGuideController** - Deze klasse orkestreert de algehele uitvoering van het bedrijfsproces. Deze klasse definieert de factory's die de stap instantiëren en de navigatie-agent die samen vervolgens zorgen voor de procesuitvoering en voor de opschoonlogica voor annulering of het afsluiten van het proces.

-   **ProcessGuideStep** - Deze klasse staat voor één stap in het bedrijfsproces. Deze klasse bevat een definitie van de factory's die een paginabouwer, acties en gegevensverwerkers instantiëren en is verantwoordelijk voor het aanroepen ervan in de juiste volgorde.

-   **ProcessGuideNavigationAgent**- Deze klasse is verantwoordelijk voor de navigatie tussen de stappen. Wanneer een stap is voltooid, is de navigatie-agent verantwoordelijk voor het definiëren van de volgende stap en geeft alle parameters door die de vorige stap mogelijk nodig heeft om met de volgende stap te communiceren.

-   **ProcessGuidePageBuilder** - Deze klasse is verantwoordelijk voor het instantiëren van de gebruikersinterface.

-   **ProcessGuideAction** - Deze klasse vertegenwoordigt een actie, die als een knop voor de gebruiker wordt weergegeven.

-   **ProcessGuideDataProcessor** - Deze klasse is verantwoordelijk voor de verwerking van de door de gebruiker ingevoerde gegevens in een veld.

## <a name="execution-flow"></a>Uitvoeringsstroom

Het beginpunt van de uitvoeringsstroom verandert niet. Dus de aanvraag komt dus nog steeds via dezelfde eindpunten binnen, gevolgd door het deserialiseren van de XML in de container. Deze container wordt vervolgens doorgegeven aan **getNextFormState()**.

Er zijn drie belangrijke klassen waar u op moet letten:

-  **ProcessGuideSessionState** – Deze klasse bevat de informatie over de sessiestaat: modus, fase, controller en de stap die wordt uitgevoerd, enzovoort.

-  **ProcessGuidePage** – Deze klasse bevat een weergave met strikte typerestricties van de metagegevens van de gebruikersinterface.

-  **ProcessGuideRequest** – Deze klasse bevat de bovenstaande twee klassen als leden en is een weergave met strikte typerestricties van de aanvraag die is ontvangen van het mobiele apparaat.

Deze klassen worden gemaakt met behulp van de containergegevens (zowel statusgegevens als door de gebruiker ingevoerde controlegegevens). Dit is een 'type-veilige' manier om de waarden te openen en te bewerken. Ten opzichte van de procedure waarbij de container herhaaldelijk werd benaderd tijdens het proces, biedt dit voordelen wat betreft zowel de leesbaarheid als de prestaties.

De statusgegevens voor de sessie worden gebruikt om de juiste **ProcessGuideController**-klasse te instantiëren. Zodra deze is geïnstantieerd, wordt de methode **CreateResponse()** in de **ProcessGuideController**-klasse is aangeroepen. Deze methode is het invoerpunt voor de ProcessGuide-logica en komt, na de uitvoering, terug met de respons (die wordt weergegeven in de klasse **ProcessGuideResponse**). De respons wordt vervolgens weer geconverteerd naar de container en teruggegeven aan de verouderde logica, die deze vervolgens naar de XML serialiseert en de respons terugstuurt naar het mobiele apparaat.

Vervolgens moet de controller de volgende stap vinden om uit te voeren. Als dit het begin is van een nieuw proces, roept de controller **initialStep()** aan om de eerste stap in het proces te krijgen. Daarna roept de controller de methode **execute()** aan in de **ProcessGuideStep**. Deze methode instantieert vervolgens een **ProcessGuidePageBuilder**-klasse en roept **buildPage()** aan, die een **ProcessGuidePage**-object retourneert, dat een virtuele weergave is van de gebruikersinterface die aan de gebruiker wordt gepresenteerd. De stap zendt het resultaat vervolgens terug naar de controller, die vervolgens de huidige sessiestatus opslaat en dan het resultaat weer retourneert naar **getNextFormState()** in het formulier van de **ProcessGuideResponse**-klasse. Hierna wordt de respons weer geconverteerd naar de container, waarna serialisatie naar XML plaatsvindt en de respons wordt teruggestuurd naar het mobiele apparaat.

In het volgende volgordediagram wordt deze controlestroom uitgelegd. Houd er rekening mee dat dit de meest voorkomende controlestroom is, die is vereenvoudigd voor de uitleg van het ontwerp.

![Vereenvoudigde controlestroom.](media/control-flow.png)

Wanneer de gebruiker een actie onderneemt op het mobiele apparaat door op een knop te klikken (of een waarde te scannen, waarmee meestal de standaardactie wordt geactiveerd), arriveert de aanvraag bij de methode **createResponse()** in de klasse **ProcessGuideController** via dezelfde route. Deze keer weet de controller echter op basis van de sessie-statusgegevens in welke stap de gebruiker zich bevindt. Op basis daarvan instantieert de controller de juiste **ProcessGuideStep**-klasse en roept de controller de uitvoermethode aan. De **ProcessGuideStep** leest op zijn beurt de actienaam die door de gebruiker is aangeroepen en instantieert vervolgens de juiste **ProcessGuideAction**-klasse en roept **execute()** aan.

De **ProcessGuideAction**-klasse is verantwoordelijk voor het uitvoeren van de specifieke actie, maar er zijn twee belangrijke uitzonderingen.

De eerste is de klasse **ProcessGuideOKAction**. Deze actie impliceert dat de gebruiker wil bevestigen en vooruit wil gaan in het proces. In overeenstemming hiermee voert deze methode feitelijk een callback uit naar de ProcessGuideStep-klasse, wat betekent dat de stap **processData()** aanroept in de **ProcessGuideDataProcessor**. Deze verwerkt de gegevens die de gebruiker heeft ingevoerd en werkt vervolgens de status van de stap bij en stuurt het resultaat terug naar de controller. Afhankelijk van de resultaten van deze gegevensverwerker, roept de stap de paginabouwer aan om de juiste gebruikersinterface te maken of stelt de status van de stap in als voltooid. Dit wordt weergegeven in de bovenste helft van het onderstaande volgordediagram.

De andere uitzondering is de annuleringsactie die is geïmplementeerd in de klassen **ProcessGuideCancelResetProcessAction** en **ProcessGuideCancelExitProcessAction**. Deze acties vertegenwoordigen een bedoeling om het proces te annuleren en terug te gaan naar het begin van het proces of het proces helemaal af te sluiten. Net als bij de **OK**-actie voeren deze acties ook een callback uit naar de stap, waarmee de intentie wordt doorgegeven aan de **ProcessGuideController**. De controller voert vervolgens de benodigde opschoning van statusvariabelen uit en verplaatst de controle naar de eerste stap in het proces of beëindigt het proces volledig.

Als nadat de stap is voltooid, de status van de stap op **Voltooid** wordt ingesteld, instantieert de controller de **ProcessGuideNavigationAgent**, die de naam van de volgende stap retourneert. De controller instantieert deze stap vervolgens en roept de methode **execute()**, waarna de cyclus wordt voortgezet. Meestal roept de nieuwe stap de bijbehorende **ProcessGuidePageBuilder** aan om de gebruikersinterface te bouwen voor het volgende scherm dat moet worden gepresenteerd aan de gebruiker, dat vervolgens wordt teruggestuurd. Deze stroom wordt weergegeven in de onderste helft van het onderstaande volgordediagram.

![volgordediagram.](media/sequence-diagram.png)

## <a name="building-a-new-process-using-the-processguide-framework"></a>Een nieuw proces maken met behulp van het ProcessGuide-framework

De beste manier om de controlestroom uit te leggen is door een voorbeeld te gebruiken dat aanwezig is in de toepassing: het productiestartproces.

## <a name="overview-of-the-production-start-process"></a>Overzicht van het productiestartproces

Laten we beginnen met het begrijpen van de processtroom. In de eerste stap wordt de gebruiker gevraagd om de productieorder-id.

![Vraag om productie-id.](media/production-id-prompt.png)

Wanneer de gebruiker de productieorder-id invoert, wordt het ordernummer gevalideerd. Sommige van de validaties die worden uitgevoerd, zijn gebaseerd op de vraag of de order zich in hetzelfde magazijn bevindt waarvoor de gebruiker zich heeft aangemeld en de vraag welke status de order heeft. Als de validatie mislukt, wordt er een foutbericht weergegeven voor de gebruiker. Als de validatie slaagt, worden details van de productieorder en het artikel weergegeven voor de gebruiker.

De gebruiker kan annuleren om terug te gaan naar het begin van het proces of op **OK** klikken om te bevestigen. In het laatste geval wordt de productieorder ingesteld op de status **Gestart**, worden de overeenkomstige journalen geboekt, gaat de controle terug naar de eerste stap en wordt het bericht 'Werk voltooid' weergegeven voor de gebruiker.


## <a name="creating-the-controller"></a>De controller maken

De eerste stap bij het opbouwen van het bedrijfsproces is het maken van de controllerklasse, die een uitbreiding vormt van de abstracte klasse **ProcessGuideController** die het standaardgedrag van een controller implementeert. De nieuwe klassenaam is **ProdProcessGuideproductionStartController** en deze wordt voorzien van de waarde **WHSWorkExecuteMode** van **StartProdOrder**. Er wordt gebruikgemaakt van dezelfde op **SysExtension** gebaseerde instantiëring die is gebruikt in de **WHSWorkExecuteDisplay**-klassen, wat helpt bij het instantiëren van de controller wanneer de gebruiker een menu-item voor deze modus uitvoert.

```xpp
[WHSWorkExecuteMode(WHSWorkExecuteMode::StartProdOrder)]
public class ProdProcessGuideProductionStartController extends ProcessGuideController
```

> [!NOTE]
> Het naampatroon van de klasse is **\<FunctionalArea\>ProcessGuide\<Businessprocessname\>Controller**. Dit is het patroon dat wordt gebruikt voor de controllerklassen en om uit te breiden naar andere klassen.


## <a name="building-the-first-step"></a>De eerste stap maken

Als u vervolgens de eerste stap wilt definiëren, maakt u de klasse **ProdProcessGuidePromptProductionIdStep** die een uitbreiding vormt van de **ProcessGuideStep**.

De taak van het instantiëren van de klasse is gedelegeerd naar een stap-factory, die wordt aangeroepen door de basisklasse **ProcessGuideController**. De standaardimplementatie van de factory instantieert de stap op basis van de naam. Als u daarom **ProdProcessGuidePromptProductionIdStep** wilt instantiëren als eerste stap in de controller, moet u twee zaken doen:

-   De klasse **ProdProcessGuidePromptProductionIdStep** voorzien van een **ProcessGuideStepName**-kenmerk.

    ```xpp
    [ProcessGuideStepName(classStr(ProdProcessGuidePromptProductionIdStep))] public class ProdProcessGuidePromptProductionIdStep extends ProcessGuideStep
    ```

-   Implementeer in de controllerklasse de abstracte methode **initialStepName()** om de stapnaam te retourneren.

    ```xpp
    protected final ProcessGuideStepName initialStepName()
    {
        return classStr(ProdProcessGuidePromptProductionIdStep);
    }
    ````   
    
> [!NOTE]
> De waarde in het kenmerk **ProcessGuideStepName** hoeft niet exact overeen te komen met de klassenaam zoals hierboven is weergegeven. Als u dit implementeert, zorgt u echter voor uniformiteit en type-veiligheid rond kruisverwijzingen bij het gebruik van de klasse. Het gebruik van deze naamgevingsconventie wordt aanbevolen.
>
> De op de **ProcessGuideStepName** gebaseerde instantiëring van de stap wordt geïmplementeerd in de klasse **ProcessGuideStepDefaultFactory**. In het zeldzame geval dat u een andere strategie wilt gebruiken voor het instantiëren van de stap, moet u het volgende doen:
> -   Maak een nieuwe factory-klasse die kenmerken overneemt van **ProcessGuidStepAbstractFactory**.
> -   Maak eventueel een nieuwe parameterklasse door het implementeren van de **ProcessGuideIStepCreationParameters**-interface, die de parameters bevat die de facatory nodig heeft.
> -   Overschrijf in uw controllerklasse de methoden **stepFactory()** en **stepCreationParameters()** om de bovenstaande factory en parameters te retourneren.

De volgende stap is het implementeren van de functionaliteit van de klasse **ProdProcessGuidePromptProductionIdStep**. U moet de logica implementeren voor het maken van de gebruikersinterface, het verwerken van de door de gebruiker ingevoerde gegevens en het bepalen wanneer de stap is voltooid.

### <a name="building-the-user-interface-for-the-first-step"></a>De gebruikersinterface voor de eerste stap maken

De gebruikersinterface wordt gemaakt met behulp van een klasse die kenmerken overneemt van de abstracte klasse **ProcessGuidePageBuilder**. Geef voor deze stap de klasse een naam die aangeeft wat de klasse doet: **ProdProcessGuidePromptProductionIdPageBuilder**.

Het instantiëringsmechanisme van de klasse is vergelijkbaar met de manier waarop de stap is geïnstantieerd vanuit de controller. 

-   Voorzie de klasse **ProdProcessGuidePromptProductionIdPageBuilder** van een **ProcessGuidePageBuilderName**-kenmerk.

    ```xpp
    [ProcessGuidePageBuilderName(classStr(ProdProcessGuidePromptProductionIdPageBuilder))] public class ProdProcessGuidePromptProductionIdPageBuilder extends ProcessGuidePageBuilder
    ```

-   Implementeer in de klasse **ProdProcessGuidePromptProductionIdStep** de abstracte methode **pageBuilderName()** om deze naam te retourneren.

    ```xpp
    protected final ProcessGuidePageBuilderName pageBuilderName()
    {
        return classStr(ProdProcessGuidePromptProductionIdPageBuilder);
    }
    ```    

> [!TIP]
> Vergelijkbaar met de stap-factory, is er ook een abstract factory-patroon geïmplementeerd voor de paginabouwers-factory. Dus in het zeldzame geval dat u een andere strategie wilt gebruiken voor het instantiëren van de paginabouwer, kunt u het volgende doen:
> - Maak een nieuwe factory-klasse die kenmerken overneemt van **ProcessGuidePageBuilderAbstractFactory**.
> - Maak eventueel een nieuwe parameterklasse door het implementeren van de **ProcessGuideIPageBuilderCreationParameters**-interface, die de parameters bevat die de facatory nodig heeft.
> - Overschrijf in uw stapklasse de methoden **pageBuilderFactory()** en **pageBuilderCreationParameters()** om de bovenstaande factory en parameters te retourneren.

Voor het implementeren van de gebruikersinterface hebt u een pagina met één tekstvak nodig om de productieorder-id in te voeren, plus een knop **OK** en een knop **Annuleren**. De knop **Annuleren** moet het proces afsluiten.

Om dit te implementeren, moet u twee methoden overschrijven in de klasse **ProdProcessGuidePromptProductionIdPageBuilder**:

-   Gebruik de methode **addDataControls()** om het tekstvak toe te voegen.

    ```xpp
    protected final void addDataControls(ProcessGuidePage _page)
    {
        _page.addTextBox(ProcessGuideDataTypeNames::ProdId, "@SYS4398", extendedTypeNum(ProdId));
    }
    ```   

-   Gebruik de methode **addActionControls()** om de knoppen **OK** en **Annuleren** toe te voegen.

    ```xpp
    protected final void addActionControls(ProcessGuidePage _page)
    {
        #ProcessGuideActionNames
        _page.addButton(step.createAction(#ActionOK), true);
        _page.addButton(step.createAction(#ActionCancelExitProcess));
    }
    ``` 

Hiermee worden de gegevensbesturingselementen toegevoegd, gevolgd door de knoppen. Als u echter een scherm wilt maken met afwisselend besturingselementen en knoppen voor gegevens, kunt u in plaats daarvan de methode **addControls()** overschrijven voor flexibiliteit.

Een extra scenario om te overwegen is het scenario voor het opnieuw bouwen van de pagina in geval van validatieproblemen, bijvoorbeeld als de gebruiker een onjuiste productieorder-id invoert. De basisklasse **ProcessGuidePageBuilder** implementeert het standaardgedrag, dat de gebruikersinterface opnieuw bouwt, de gescande waarde opschoont en het besturingselement voor fouten toevoegt met het foutbericht. Omdat dit het standaardgedrag is dat u wilt gebruiken, hoeft u geen code voor het verwerken van fouten toe te voegen.

> [!TIP]
> Als u aangepast gedrag voor de gebruikersinterface voor foutsituaties wilt implementeren, kunt u een of meer van de volgende methoden overschrijven: **rebuildFromRequestPage()**, **isErrorState()** en **reuseRequestPageOnError()**.

### <a name="processing-the-user-entered-data-in-the-first-step"></a>De door de gebruiker ingevoerde gegevens verwerken in de eerste stap

De verwerking van de gegevens wordt uitgevoerd in de klasse **ProcessGuideDataProcessorDefault**, die op zijn beurt de verouderde klasse **WhsRfControlData** aanroept. Er hoeven geen wijzigingen in dit standaardgedrag te worden aangebracht en **WhsRfControlData** heeft al logica voor het valideren van het veld **ProdId**. U hoeft dus geen logica voor het verwerken hiervan te maken. Voor het geval er uitbreidingen vereist zijn voor de validatielogica, kunt u overwegen het op **WhsControl** gebaseerde uitbreidingsmechanisme te gebruiken.

### <a name="determine-if-the-first-step-is-complete"></a>Bepalen of de eerste stap is voltooid

Wanneer de validatie is geslaagd, is het tijd om de stap als voltooid te markeren. Dit wordt gedaan in de basisklasse, maar u moet de voorwaarde implementeren om de voltooiing van de stap te bepalen. De volgende overschreven methode doet dat.

```xpp
protected final boolean isComplete()
{
    WhsrfPassthrough pass = controller.parmSessionState().parmPass();
    ProdId prodId = pass.lookup(ProcessGuideDataTypeNames::ProdId);
        return (prodId != '');
}
```   

### <a name="step-two-view-order-details-and-confirm"></a>Stap twee: Orderdetails weergeven en bevestigen

In de tweede stap van het proces wordt aan de gebruiker een scherm getoond met details over de order. De gebruiker kan op de knop **OK** klikken om de start van de productieorder te bevestigen of op **Annuleren** klikken om terug te gaan naar het begin van het proces. Geef voor dit voorbeeld de stap de naam **ProdProcessGuideConfirmProductionOrderStep** en de paginabouwersklasse de naam **ProdProcessGuideConfirmProductionOrderPageBuilder**.

De klasse ProdProcessGuideConfirmProductionOrderStep ziet er als volgt uit.

```xpp
[ProcessGuideStepName(classStr(ProdProcessGuideConfirmProductionOrderStep))]
public class ProdProcessGuideConfirmProductionOrderStep extends ProcessGuideStep
{
    protected final ProcessGuidePageBuilderName pageBuilderName()
    {
        return classStr(ProdProcessGuideConfirmProductionOrderPageBuilder);
     }
}
```     

Aangezien de gebruiker hier geen waarden hoeft in te voeren, hoeft u de methode **isComplete()** niet te overschrijven. De stap is voltooid wanneer de gebruiker op **OK** klikt.

De paginabouwersklasse overschrijft de methode **addDataControls()** om drie labels toe te voegen. Het eerste label toont de productieorder-id, het tweede label bevat artikelinformatie (zoals artikel-id, afmetingen of omschrijving) en het derde label bevat de hoeveelheid en de maateenheid.

Vervolgens wordt **addActionControls()** overschreven om twee knoppen toe te voegen: de knop **OK** en de knop **Annuleren** om het proces te annuleren en terug te gaan naar het begin van het proces.

```xpp
/// <summary>
/// The <c>ProdProcessGuideConfirmProductionOrderPageBuilder</c> builds a page that allows the user to see details of a production order
/// and then confirm.
/// </summary>
[ProcessGuidePageBuilderName(classStr(ProdProcessGuideConfirmProductionOrderPageBuilder))]
public class ProdProcessGuideConfirmProductionOrderPageBuilder extends ProcessGuidePageBuilder
{
    protected void addDataControls(ProcessGuidePage _page)
    {
        WhsrfPassthrough pass = controller.parmSessionState().parmPass();
        ProdTable prodTable = ProdTable::find(pass.lookup(ProcessGuideDataTypeNames::ProdId));
        UnitOfMeasureSymbol inventUOM = InventTableModule::find(prodTable.ItemId, ModuleInventPurchSales::Invent).UnitId;
        
        _page.addLabel(ProcessGuideDataTypeNames::ProdIdLabelName, strFmt("@WAX1684", prodTable.ProdId), extendedTypeNum(ProdId));
        _page.addLabel(ProcessGuideDataTypeNames::ItemInfo, this.generateItemInfoForProdId(pass.lookup(ProcessGuideDataTypeNames::ProdId)), extendedTypeNum(WHSRFUndefinedDataType));
        _page.addLabel(ProcessGuideDataTypeNames::QtyLabelName, strFmt("@WAX1685", WHSWorkExecuteDisplay::num2StrDisplay(ProdUpdStartUp::proposalStartUpQty(prodTable.ProdId)), inventUOM), extendedTypeNum(WHSRFQuantityAndUOM));

        if (PdsGlobal::pdsIsCWItem(prodTable.ItemId))
        {
            _page.addLabel(ProcessGuideDataTypeNames::InventQtyLabelName, strFmt("@WAX1685", WHSWorkExecuteDisplay::num2StrDisplay(ProdUpdStartUp::pdsCWProposalStartupQty(prodTable.ProdId)), PdsCatchWeightItem::pdsCWUnitId(prodTable.ItemId)), extendedTypeNum(WHSRFQuantityAndUOM));
        }
    }

    protected void addActionControls(ProcessGuidePage _page)
    {
        #ProcessGuideActionNames
        _page.addButton(step.createAction(#ActionOK), true);
        _page.addButton(step.createAction(#ActionCancelResetProcess));
    }
```

> [!NOTE]
> U kunt dezelfde broncode vinden voor de X++-methoden in dit artikel met behulp van de Toepassingsverkenner. Filter op de klassenaam en klik vervolgens met de rechtermuisknop op de klassenaam en selecteer **Code weergeven**.

### <a name="step-3-start-the-production-order"></a>Stap 3: De productieorder starten

In de derde stap wordt de bedrijfslogica van het starten van de productieorder uitgevoerd. Deze stap verschilt enigszins van de vorige stappen, omdat deze stap geen gebruikersinterface heeft. Deze stap wordt op de achtergrond uitgevoerd wanneer de gebruiker op **OK** klikt in de vorige stap.

De abstracte klasse **ProcessGuideStepWithoutPrompt** implementeert het standaardgedrag voor dergelijke stappen. De huidige stap moet daarom de klasse **ProcessGuideStepWithoutPrompt** uitbreiden en de methode **doExecute()** overschrijven.

In het volgende codevoorbeeld ziet u de klasse en de implementatie van de methode **doExecute()**. De methode haalt eenvoudig de order-id en de gebruikers-id op uit de sessiestatus en roept de methode aan om deze productieorder te starten.

```xpp
/// <summary>
/// The <c>ProdProcessGuideStartProductionOrderStep</c> represents a step that starts a production order.
/// </summary>
[ProcessGuideStepName(classStr(ProdProcessGuideStartProductionOrderStep))]
public class ProdProcessGuideStartProductionOrderStep extends ProcessGuideStepWithoutPrompt
{
    protected final void doExecute()
    {
        WhsrfPassthrough pass = controller.parmSessionState().parmPass();
        WHSUserId userId = pass.lookup(ProcessGuideDataTypeNames::UserId);
        ProdTable prodTable = ProdTable::find(pass.lookup(ProcessGuideDataTypeNames::ProdId));
        WhsWorkExecute workExecute = WhsWorkExecute::construct();
        workExecute.prodStartUp(prodTable.ProdId, ProdUpdStartUp::proposalStartUpQty(prodTable.ProdId), userId);

        this.addProcessCompletionMessage();

        super();
    }

}
```

In het geval van een uitzondering, zorgt de logica voor het verwerken van van uitzonderingen van het framework ervoor dat het proces wordt teruggedraaid naar de vorige stap.

> [!NOTE]
> Met de aanroep van **addProcessCompletionMessage()** wordt het bericht 'Werk voltooid' toegevoegd aan de navigatieparameters. Dit bericht wordt weergegeven in de volgende stap (ervan uitgaande dat deze een gebruikersinterface heeft). De basisklassen verwerken deze logica. Er hoeft geen specifieke code aan de procesklassen te worden toegevoegd om dit gedrag te bereiken.


### <a name="building-the-navigation-through-the-steps"></a>De navigatie door de stappen bouwen

De basisklasse **ProcessGuideController** instantieert de klasse **ProcessGuideNavigationAgentDefault**, die afhankelijk is van een vooraf gedefinieerde navigatieroute, die een eenvoudige kaart van bron- en doelstappen is. Voor het productiestartscenario is deze implementatie voldoende, omdat er geen voorwaardelijke vertakkingen zijn. Daarom hoeft u alleen maar de methode **initializeNavigationRoute()** te overschrijven om de navigatieroute te definiëren.

```xpp
    protected ProcessGuideNavigationRoute initializeNavigationRoute()
    {
        ProcessGuideNavigationRoute navigationRoute = new ProcessGuideNavigationRoute();
        navigationRoute.addFollowingStep(classStr(ProdProcessGuidePromptProductionIdStep), classStr(ProdProcessGuideConfirmProductionOrderStep));
        navigationRoute.addFollowingStep(classStr(ProdProcessGuideConfirmProductionOrderStep), classStr(ProdProcessGuideStartProductionOrderStep));
        navigationRoute.addFollowingStep(classStr(ProdProcessGuideStartProductionOrderStep), classStr(ProdProcessGuidePromptProductionIdStep));

        return navigationRoute;
    }
```

Er zijn processen met voorwaardelijke vertakkingen (op basis van gebruikersacties of andere voorwaarden). Dergelijke processen moeten het volgende doen:

-   Specifieke navigatie-agents implementeren die zijn overgenomen van de klasse **ProcessGuideNavigationAgent**.

-   De specifieke navigatie-agent-factory implementeren die is overgenomen van de klasse **ProcessGuideNavigationAgentAbstractFactory** en die logica bevat om de juiste navigatie-agent te instantiëren op basis van de huidige stap, de status van de sessie, een gebruikersactie of andere logica.

-   Optioneel **navigationAgentCreationParameters()** in de controllerklasse overschrijven om geschikte parameters door te geven.

-   De methode **navigationAgentFactory()** in de controller overschrijven om de navigatie-agent-factory die hierboven is gemaakt, te instantiëren.

### <a name="action-classes"></a>Actieklassen

Actieklassen vertegenwoordigen gebruikersacties, dus in dit voorbeeld wordt de **OK**-actie gebruikt om te laten zien hoe de acties worden gemaakt.

```xpp
[ProcessGuideActionName(#ActionOK)]
public class ProcessGuideOKAction extends ProcessGuideAction
{
    public final str label()
    {
        return "@SYS5473";
     }
     protected final void doExecute()
     {
        step.executeOKAction();
      }
}
```    

De klasse moet twee abstracte methoden implementeren:

-   **label()** waarmee het label wordt geretourneerd dat moet worden weergegeven in een knopbesturingselement dat aan deze actie is gekoppeld.

-   **doExecute()** waarmee de actie wordt uitgevoerd. Zoals eerder is vermeld, voert de knop **OK** gewoon een callback uit naar de stap. Andere acties kunnen echter een complexere logica hebben.

De acties worden geïnstantieerd met het **SysExtension**-framework op basis van het kenmerk **ProcessGuideActionName**. De stapklasse implementeert de standaardactie-factory (vergelijkbaar met de instantiëring van paginabouwers) en het is mogelijk om deze te overschrijven. De paginabouwer voegt een knopbesturingselement toe zoals dit.

```xpp
_page.addButton(step.createAction(#ActionOK), true);
```

Door dat te doen, wordt aan de stap gevraagd om een actieklasse te maken voor de doorgegeven naam en wordt die actie met de knop verbonden.

### <a name="summary"></a>Samenvatting

Om alles wat in dit artikel is uitgelegd samen te vatten, is hier een uitgebreid overzicht van de code die nodig is voor het proces:

1.  **ProdProcessGuideProductionStartController**

    1.  Overschrijf **initialStepName()** om de naam van de eerste stap op te geven.
    2.  Overschrijf **initializeNavigationRoute()** om de navigatiemap te maken.

        ```xpp
        /// <summary>
        /// The <c>ProdProcessGuideProductionStartController</c> class is the controller class for the production order start process guide.
        /// </summary>
        [WHSWorkExecuteMode(WHSWorkExecuteMode::StartProdOrder)]
        public class ProdProcessGuideProductionStartController extends ProcessGuideController
        {
            protected ProcessGuideStepName initialStepName()
            {
                return classStr(ProdProcessGuidePromptProductionIdStep);
            }

            protected ProcessGuideNavigationRoute initializeNavigationRoute()
            {
                ProcessGuideNavigationRoute navigationRoute = new ProcessGuideNavigationRoute();
                navigationRoute.addFollowingStep(classStr(ProdProcessGuidePromptProductionIdStep), classStr(ProdProcessGuideConfirmProductionOrderStep));
                navigationRoute.addFollowingStep(classStr(ProdProcessGuideConfirmProductionOrderStep), classStr(ProdProcessGuideStartProductionOrderStep));
                navigationRoute.addFollowingStep(classStr(ProdProcessGuideStartProductionOrderStep), classStr(ProdProcessGuidePromptProductionIdStep));

                return navigationRoute;
            }

        }
        ```

2.  **ProdProcessGuidePromptProductionIdStep**

    1.  Overschrijf **isComplete()** om op te geven wanneer de stap als voltooid wordt beschouwd.
    2.  Overschrijf **pageBuilderName()** om de paginabouwer op te geven die moet worden gebruikt.

        ```xpp
        /// <summary>
        /// The <c>ProdProcessGuidePromptProductionIdStep</c> represents a step that 
        /// that prompts the user for a production order id.
        /// </summary>
        [ProcessGuideStepName(classStr(ProdProcessGuidePromptProductionIdStep))]
        public class ProdProcessGuidePromptProductionIdStep extends ProcessGuideStep
        {
            protected boolean isComplete()
            {
                WhsrfPassthrough pass = controller.parmSessionState().parmPass();
                ProdId prodId = pass.lookup(ProcessGuideDataTypeNames::ProdId);

                return (prodId != '');
            }

            protected ProcessGuidePageBuilderName pageBuilderName()
            {
                return classStr(ProdProcessGuidePromptProductionIdPageBuilder);
            }

        }
        ```

3.  **ProdProcessGuidePromptProductionIdPageBuilder**

    1.  Overschrijf **addDataControls()** om het tekstvak **Prod ID** toe te voegen.
    2.  Overschrijf **addActionControls()** om de knoppen **OK** en **Annuleren** toe te voegen.
        
        ```xpp
        /// <summary>
        /// The <c>ProdProcessGuidePromptProductionIdPageBuilder</c> class builds a page 
        /// that prompts the user for a production order id.
        /// </summary>
        [ProcessGuidePageBuilderName(classStr(ProdProcessGuidePromptProductionIdPageBuilder))]
        public class ProdProcessGuidePromptProductionIdPageBuilder extends ProcessGuidePageBuilder
        {
            protected void addDataControls(ProcessGuidePage _page)
            {
                _page.addTextBox(ProcessGuideDataTypeNames::ProdId, "@SYS4398", extendedTypeNum(ProdId));
            }

            protected void addActionControls(ProcessGuidePage _page)
            {
                #ProcessGuideActionNames
                _page.addButton(step.createAction(#ActionOK), true);
                _page.addButton(step.createAction(#ActionCancelExitProcess));
            }

        }
        ```

4.  **ProdProcessGuideConfirmProductionOrderStep**

    1.  Overschrijf **pageBuilderName()** om de paginabouwer op te geven die moet worden gebruikt.
        
        ```xpp
        /// <summary>
        /// The <c>ProdProcessGuideConfirmProductionOrderStep</c> class represents the step for viewing production order
        /// details and confirming the same.
        /// </summary>
        [ProcessGuideStepName(classStr(ProdProcessGuideConfirmProductionOrderStep))]
        public class ProdProcessGuideConfirmProductionOrderStep extends ProcessGuideStep
        {    
            protected ProcessGuidePageBuilderName pageBuilderName()
            {
                return classStr(ProdProcessGuideConfirmProductionOrderPageBuilder);
            }

        }
        ```

3.  **ProdProcessGuideConfirmProductionOrderPageBuilder**

    1.  Overschrijf **addDataControls()** om de informatielabels voor order, artikel en hoeveelheid toe te voegen.

    2.  Overschrijf **addActionControls()** om de knoppen **OK** en **Annuleren** toe te voegen.
        
        ```xpp
        /// <summary>
        /// The <c>ProdProcessGuideConfirmProductionOrderPageBuilder</c> builds a page that allows the user to see details of a production order
        /// and then confirm.
        /// </summary>
        [ProcessGuidePageBuilderName(classStr(ProdProcessGuideConfirmProductionOrderPageBuilder))]
        public class ProdProcessGuideConfirmProductionOrderPageBuilder extends ProcessGuidePageBuilder
        {
            protected void addDataControls(ProcessGuidePage _page)
            {
                WhsrfPassthrough pass = controller.parmSessionState().parmPass();
                ProdTable prodTable = ProdTable::find(pass.lookup(ProcessGuideDataTypeNames::ProdId));
                UnitOfMeasureSymbol inventUOM = InventTableModule::find(prodTable.ItemId, ModuleInventPurchSales::Invent).UnitId;

                _page.addLabel(ProcessGuideDataTypeNames::ProdIdLabelName, strFmt("@WAX1684", prodTable.ProdId), extendedTypeNum(ProdId));
                _page.addLabel(ProcessGuideDataTypeNames::ItemInfo, this.generateItemInfoForProdId(pass.lookup(ProcessGuideDataTypeNames::ProdId)), extendedTypeNum(WHSRFUndefinedDataType));
                _page.addLabel(ProcessGuideDataTypeNames::QtyLabelName, strFmt("@WAX1685", WHSWorkExecuteDisplay::num2StrDisplay(ProdUpdStartUp::proposalStartUpQty(prodTable.ProdId)), inventUOM), extendedTypeNum(WHSRFQuantityAndUOM));

                if (PdsGlobal::pdsIsCWItem(prodTable.ItemId))
                {
                    _page.addLabel(ProcessGuideDataTypeNames::InventQtyLabelName, strFmt("@WAX1685", WHSWorkExecuteDisplay::num2StrDisplay(ProdUpdStartUp::pdsCWProposalStartupQty(prodTable.ProdId)), PdsCatchWeightItem::pdsCWUnitId(prodTable.ItemId)), extendedTypeNum(WHSRFQuantityAndUOM));
                }
            }

            protected void addActionControls(ProcessGuidePage _page)
            {
                #ProcessGuideActionNames
                _page.addButton(step.createAction(#ActionOK), true);
                _page.addButton(step.createAction(#ActionCancelResetProcess));
            }

        ```

        > [!NOTE]
        > De methode **generateItemInfoForProdId()** die wordt gebruikt voor het genereren van de artikelinformatielabels, is weggelaten in dit artikel. Deze methode voert query's uit op enkele tabellen om de id, omschrijving en afmetingen van een artikel te krijgen. Als u beter inzicht wilt in **generateItemInfoForProdId()**, bekijkt u de broncode.

4.  **ProdProcessGuideStartProductionOrderStep**

    1.  Overschrijf **doExecute()** om het productieproces uit te voeren en het bericht voor de voltooiing van het proces toe te voegen.

        ```xpp
        /// <summary>
        /// The <c>ProdProcessGuideStartProductionOrderStep</c> represents a step that starts a production order.
        /// </summary>
        [ProcessGuideStepName(classStr(ProdProcessGuideStartProductionOrderStep))]
        public class ProdProcessGuideStartProductionOrderStep extends ProcessGuideStepWithoutPrompt
        {
            protected final void doExecute()
            {
                WhsrfPassthrough pass = controller.parmSessionState().parmPass();
                WHSUserId userId = pass.lookup(ProcessGuideDataTypeNames::UserId);
                ProdTable prodTable = ProdTable::find(pass.lookup(ProcessGuideDataTypeNames::ProdId));
                WhsWorkExecute workExecute = WhsWorkExecute::construct();
                workExecute.prodStartUp(prodTable.ProdId, ProdUpdStartUp::proposalStartUpQty(prodTable.ProdId), userId);

                this.addProcessCompletionMessage();

                super();
            }

        }
        ```

> [!NOTE]
> Een groot aantal veelvoorkomende patronen (regeneratie van de gebruikersinterface bij een fout, het instellen van het voltooiingsbericht voor het proces, **OK** en **Annuleren**) zijn verplaatst naar het framework. Op deze manier hoeft de toepassingsontwikkelaar geen boilerplate-code (standaardcode) te schrijven die foutgevoelig is en het risico heeft dat er in verschillende processen inconsistent gedrag ontstaat. Voor het geval het scenario moet afwijken van het 'gewone pad', is de toepassingsontwikkelaar echter voorzien van de optie om geschikte methoden te overschrijven. Maar in dat geval gaat het om een bewuste afwijking, die zowel expliciet als herleidbaar is.


### <a name="extending-a-business-process"></a>Een bedrijfsproces uitbreiden

Tot nu toe is in dit artikel besproken hoe u een nieuw proces kunt maken met behulp van het **ProcessGuide**-framework. In dit laatste gedeelte vindt u enkele voorbeelden van de manier waarop dit bedrijfsproces kan worden uitgebreid.

### <a name="add-a-step-in-a-flow-using-processguidenavigationagentdefault"></a>Een stap in een stroom toevoegen (met ProcessGuideNavigationAgentDefault)

Waar uitbreiden:

-   Onderliggende klasse van de klasse **ProcessGuideController** voor het proces.

Hoe uitbreiden:

-   Breid de methode **initializeNavigationRoute()** uit in de controllerklasse en roep **addFollowingStep()** aan in de klasse **ProcessGuideNavigationRoute**.

### <a name="add-a-step-in-a-flow-using-custom-navigation-agent"></a>Een stap in een stroom toevoegen (met de aangepaste navigatie-agent)

Waar uitbreiden:

-   Onderliggend item van **ProdProcessGuideNavigationAgentFactory/ProdProcessGuideNavigationAgent**.

Hoe uitbreiden:

-   Maak een nieuwe onderliggende klasse van **ProcessGuideNavigationAgent** die de gewenste stapnaam retourneert.

-   Maak een nieuwe klasse die is afgeleid van **ProcessGuideNavigationAgentFactory**, die de navigatie-agent die hierboven is gemaakt, voorwaardelijk retourneert.

-   Breid de methode **navigationAgentFactory()** in de controllerklasse uit om de hierboven gemaakte factory te retourneren.

### <a name="add-a-new-control-in-the-ui-of-an-existing-step"></a>Een nieuw besturingselement toevoegen aan de gebruikersinterface van een bestaande stap 

Waar uitbreiden:

-   Onderliggend item van **ProdProcessGuidePageBuilder** voor de stap.

Hoe uitbreiden:

-   Breid de methode **addDataControls()** uit en voeg het extra besturingselenent toe.

### <a name="complete-overhaul-of-the-user-interface-in-an-existing-step"></a>De gebruikersinterface in een bestaande stap compleet herzien

Waar uitbreiden:

-   Onderliggend item van **ProdProcessGuideStep**.

Hoe uitbreiden:

-   Maak een nieuwe onderliggende klasse van de klasse **ProdProcessGuidePageBuilder** en implementeer de gewenste gebruikersinterface.

-   Breid de methode **pageBuildeName()** uit in de stapklasse om de **ProcessGuidePageBuilderNameAttribute** te retourneren voor de hierboven gemaakte klasse.

### <a name="alter-logic-when-a-step-is-considered-complete"></a>Logica wijzigen wanneer een stap als voltooid wordt beschouwd

Waar uitbreiden:

-   Onderliggend item van **ProdProcessGuideStep**.

Hoe uitbreiden:

-   Breid de methode **IsComplete()** uit om de aanvullende logica te maken.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]