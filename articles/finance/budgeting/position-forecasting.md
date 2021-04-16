---
title: Prognosepositie
description: De onkosten die aan werknemers zijn gerelateerd vormen vaak een grote deel van de kosten van een organisatie. Positie voorspellen laat u die onkosten plannen en deze opnemen in de planning van budgetten.
author: ShylaThompson
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmPositionForecast
audience: Application User
ms.reviewer: roschlom
ms.custom: 64413
ms.assetid: 35e791d2-1905-4808-a579-7f181ddddd91
ms.search.region: Global
ms.author: sigitac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 03a195c725854eff1fe6d6fa20bb815673e2e307
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/01/2021
ms.locfileid: "5827333"
---
# <a name="position-forecasting"></a>Prognosepositie

[!include [banner](../includes/banner.md)]

De onkosten die aan werknemers zijn gerelateerd vormen vaak een grote deel van de kosten van een organisatie. Positie voorspellen laat u die onkosten plannen en deze opnemen in de planning van budgetten.

## <a name="position-forecasting-in-budget-planning"></a>Positie voorspelling in budget planning

[![Onderdelen van positieprognose](./media/graphic-top.png)](./media/graphic-top.png) 

Positieprognose maakt gebruik van drie hoofdcomponenten om nauwkeurige budgetbedragen voor positiekosten te geven. Deze bedragen kunnen vervolgens in een budgetplan voor budgetberekeningen worden gebracht. 

Het primaire component is **voorspellingpositie**, hetgeen alle kostengegevens vertegenwoordigt die in één positie zijn gekoppeld. U kunt meerdere versies van een voorspellingpositie maken door een ander scenario van het budgetplan aan elke versie toe te wijzen. Meerdere versies maken een iteratieve aanpak van budgettering mogelijk en staan u toe wat-als-scenario's te vergelijken. Elke voorspellingspositie heeft een bijbehorende positie in HRM.

Een **budget kostprijs element** is een installatiecomponent die specifieke kostprijs weergeeft die geassocieerd is aan een positie, zoals basisloon, zorgverzekering, de mobiele telefoon toeslag, enzovoort. Een budget kostprijs element element bevat de hoofdrekening die voor de kosten en de opties voor de berekening wordt gebruikt. Elk budgetkostprijselement kan toegewezen worden aan meerdere voorspellingsposities. 

Een **compensatiegroep** is een optioneel installatiecomponent dat wordt gebruikt om een set budget kostprijselementen en betalingsberekeningen toe te passen op posities die soortgelijke kenmerken hebben. Een compensatiegroep kan een compensatieraster van salaristarieven bevatten. Wanneer de groep aan een voorspellingspositie is toegewezen, kan een niveau en een stap in het raster de inkomsten van de voorspellingspositie toewijzen. De set van kostprijselementen wordt automatisch toegevoegd.

### <a name="position-forecasting-processes"></a>Positie voorspelling processen

[![Afbeelding van processen voor positieprognoses](./media/graphic1b.png)](./media/graphic1b.png) 

In een typisch proces voor positieprognose maakt u eerst de instellingsonderdelen (budgetkostenelementen en compensatiegroepen). Prognoseposities worden vervolgens gegenereerd op basis van bestaande posities. U kunt vervolgens correcties aanbrengen. U kunt bijvoorbeeld posities toevoegen of beëindigen, loontarieven en kosten voor vergoedingen wijzigen en loonstijgingen toevoegen. U kunt meerdere versies van een prognosepositie maken om verschillende budgetscenario's met elkaar te vergelijken. Vervolgens kunt u de prognoseposities opnemen in budgetplannen en de kosten van de prognoseposities invoeren als budgetplanregels.

U kunt extra versies van de prognosepositie maken wanneer de budgetplannen worden gewijzigd. Deze nieuwe versies bieden een basis voor de revisies.

## <a name="position-forecasting-setup"></a>Instelling positievoorspelling
[![Afbeelding met instellingen](./media/graphic2-1024x327.png)](./media/graphic2.png)

### <a name="budget-cost-elements"></a>Budgetkostenelementen

Budgetkostenelementen worden gebruikt om kostendetails te definiëren voor een prognosepositie. Deze details omvatten het type kosten, hoe kosten worden berekend en of de kosten worden toegewezen aan meerdere datums wanneer de prognosepositie wordt opgenomen in een budgetplan. 

De specifieke velden definiëren het gedrag van het budgetkostenelement. Aan elk budgetkostenelement wordt het budgetkostentype **Inkomsten**, **Vergoeding**, **Belasting** of **Overige** toegewezen. De budgetkostentypen worden voornamelijk gebruikt om totalen te berekenen. De waarde **Prognosepositie overschrijven** geeft aan of de bedragen op het element kunnen worden gewijzigd op de prognosepositie. Het veld **Toewijzingsmethode** wordt gebruikt wanneer een prognosepositie aan een budgetplan wordt toegevoegd. U kunt de kostprijs splitsen in afzonderlijke budgetplanregels met verschillende datums per maand, kwartaal, week of twee weken. Door een begindatum te selecteren wijst u de kosten als één bedrag toe aan de begindatum die is ingesteld in de prognosepositie. 

De berekening van de kostprijs van het budgetkostenelement gebruikt ingangsdatums om het gebruik van hetzelfde budgetkostenelement in andere periodes mogelijk te maken. Eén hoofdrekening wordt toegewezen in elke periode, samen met een percentage of een jaarlijks bedrag dat de kostprijs aangeeft. Een budgetkostenelement kan een percentage van andere kostenelementen of een jaarlijks bedrag gebruiken, maar niet beide. U kunt ook een jaarlijkse limiet opgeven. 

Als het kostenelement op een percentage is gebaseerd, moet u de budgetkostenelementen opgeven die als basis voor de berekening worden gebruikt.

**Voorbeeld** 

Jodi's organisatie biedt een trainingstoelage van 5 procent van het basisloon van een werknemer. Jodi wil een budgetkostenelement voor deze kosten maken. Ze maakt een nieuw budgetkostenelement en wijst het budgetkostentype **Vergoeding** toe.

Jodi wil niet dat managers het bedrag van de vergoeding wijzigen. Daarom selecteert ze **Kostenwijzigingen niet toestaan** in het veld **Prognosepositie overschrijven**. De organisatie wil dat deze kosten gelijkmatige worden toegewezen aan elke maand. Daarom selecteert Jodi **Driemaandelijks** in het veld **Toewijzingsmethode**. 

Stel, Jodi vergelijken een kostenberekeningsregel toe, stelt de datums en een hoofdrekening in, en voert **5,00** in als percentage. Haar organisatie heeft een grens van $ 5.000 per jaar voor deze vergoeding. Daarom voert Jodi dat bedrag in als jaarlijkse limiet. 

Ten slotte voegt Jodi alle inkomstenkostenelementen toe die voor basisloon worden gebruikt als berekeningsbasis. Haar budgetkostenelement is nu gereed om te worden gebruikt.

### <a name="compensation-groups"></a>Compensatiegroepen

Compensatiegroepen kunnen worden gebruikt om prognoseposities te groeperen die vergelijkbare compensatiekenmerken hebben. Zij kunnen ook worden gebruikt om de jaarlijkse inkomsten en jaarlijkse verhogingen van een prognosepositie te definiëren en een set gemeenschappelijke budgetkostenelementen toe te wijzen. 

Een basisfunctie van compensatiegroepen is een set budgetkostenelementen aan een prognosepositie toe te wijzen. Daarom kunnen compensatiegroepen worden gebruikt om algemene kosten, zoals vergoedingsplannen en belastingen, toe te voegen. Een manager die een prognosepositie maakt, hoeft niet alle kostenelementen te kennen die moeten worden toegevoegd. In plaats daarvan kunnen de kostenelementen worden toegevoegd wanneer de compensatiegroep is geselecteerd. De elementen worden toegevoegd aan de instellingen van de compensatiegroep op het tabblad **Budgetkostenelementen**. 

Compensatiegroepen kunnen ook de inkomstentarieven voor een prognosepositie bepalen. U stelt een groep in om inkomsten van de prognosepositie te berekenen per uur of op basis van een jaarsalaris. Op het tabblad **Compensatietarieftabellen** bepaalt een compensatieraster van salaristarieven de inkomsten die aan een prognosepositie worden toegevoegd, gebaseerd op een toegewezen niveau en stap. Deze rasters kunnen zijn gebaseerd op bestaande compensatierasters in Human resources. Als alternatief kunt u nieuwe compensatierasters maken voor de budgetplanning. 

Met de ingangsdatums en vervaldatums op de tabellen met het compensatietarief kunt u de loontarieven op een willekeurige datum wijzigen. Deze functie is nuttig als een onderhandelingseenheid heeft onderhandeld voor een algemene verhoging in het midden van een budgetcyclus. In dit geval, wijzigt u de vervaldatum van de bestaande tabel naar de dag vóór de datum van de tariefwijziging en voegt u een nieuwe tarieftabel toe die begint op de nieuwe datum. Wanneer u een nieuwe tarieftabel maakt en u **Een nieuw compensatieraster maken op basis van een bestaand raster** selecteert, kunt u een bestaande tarieftabel selecteren uit Human Resources. Op de tarieftabel die wordt gemaakt, kunt u met de optie **Massawijziging** een percentage of een vlakke bedragverhoging of een -verlaging toepassen op alle tarieven in het raster. 

De velden **Planning verhogen** en **Datum van verhoging** in de compensatiegroep worden gebruikt wanneer u salarisverhogingen moet maken omdat de posities naar een volgende stap gaan. Een jaarlijks loonsverhoging is een veel voorkomend scenario. De verhogingsplanning bepaalt of de jubileumdatum van de positie of één gemeenschappelijke datum voor de stapverhoging wordt gebruikt. De verhogingsplanning is van toepassing op alle prognoseposities in de compensatiegroep. 

Het inkomstenkostenelement dat op de compensatiegroep wordt geselecteerd, wordt gebruikt wanneer u inkomsten maakt voor de prognoseposities in de groep, waaronder hun basisloon en eventuele stapverhogingen. Het veld **Vastecompensatieplan** koppelt de compensatiegroep aan een vastecompensatieplan in Human resources. Deze koppeling kan de gegevens over de vaste compensatie van een werknemer aan een prognosepositie toewijzen en kan daarom de budgetplanning nauwkeuriger maken. Denk eraan dat de structuur van het compensatieraster (de niveaus en de stappen) voor de compensatiegroep overeen moet komen met de structuur van het geselecteerde vastecompensatieplan. Anders kan het systeem de compensatiegroep en het vastecompensatieplan niet correct koppelen.

## <a name="creating-forecast-positions"></a>Prognoseposities maken
[![Afbeelding van het maken van prognoseposities](./media/graphic3-1024x327.png)](./media/graphic3.png)

### <a name="creating-forecast-positions-for-existing-positions"></a>Prognoseposities maken voor bestaande posities

Voor de nauwkeurigste budgetplanning kunt u prognoseposities maken door gegevens van bestaande posities te gebruiken, ongeacht of de positie momenteel is vervuld of niet. 

De functie **Bestaande posities toevoegen** geeft alle posities weer voor een organisatie. Door de datum in te stellen op **Vanaf** kunt u de lijst met posities wijzigen zodat deze de posities bevat die bestonden op een datum in het verleden of, vaker, in de toekomst (bijvoorbeeld, het begin van de volgende budgetcyclus). Selecteer een planningsproces en budgetplanscenario, selecteer posities in de lijst, en klik vervolgens in **OK** om prognoseposities voor de geselecteerde functies te maken. Merk op dat u slechts één prognosepositie voor elke bestaande positie in een budgetplanningsproces en -scenario kunt maken. U kunt echter extra versies maken door andere budgetplanscenario's toe te wijzen. 

Als de budgetkostenelementen zijn toegewezen aan de positie in Human resources, worden die budgetkostenelementen ook toegewezen aan de prognosepositie en gebruiken ze de standaardbedragen. Het veld **Toegewezen werknemer** op de prognosepositie wordt ingesteld op de naam van de werknemer die aan de positie is toegewezen, als er een werknemer is toegewezen. Dit veld is een eenvoudig tekstveld. Geen directe koppeling wordt gemaakt. 

Als een budgetkostenelement wordt geselecteerd, wordt het jaarlijkse bedrag van de vaste compensatie toegewezen aan de prognosepositie met behulp van het geselecteerde kostenelement, op voorwaarde dat de toegewezen werknemer een vastecompensatieplan heeft. Als de werknemer geen vastecompensatieplan heeft of als er geen werknemer is toegewezen, wordt het standaardbedrag gebruikt voor het budgetkostenelement. 

Wanneer de optie **Een compensatiegroep toewijzen** is ingesteld op **Ja**, worden, als de werknemer die aan de positie is toegewezen een stapgebaseerd vast compensatieplan heeft dat aan een compensatiegroep (zoals eerder beschreven) is gekoppeld, het niveau en de stap voor de werknemer toegewezen aan de prognosepositie, samen met de compensatiegroep. Het budgetkostenelement voor opbrengsten van de compensatiegroep wordt toegevoegd aan de prognosepositie en het salaristarief op het niveau en de stap van de compensatiegroep worden gebruikt. 

De instelling van de optie **Een compensatiegroep toewijzen** heeft voorrang boven de instelling **Toewijzing van budgetkostenelement**. De twee instellingen kunnen tegelijkertijd worden gebruikt. 

[![Het diagram Een compensatiegroep toewijzen](./media/graphic4.png)](./media/graphic4.png) 

Een andere optie is het toewijzen van een jubileumdatum. De geselecteerde datum (gecorrigeerde begindatum, begindatum van medewerker, begindatum van dienstverband of anciënniteitsdatum) van de toegewezen medewerker wordt vervolgens ingesteld als jubileumdatum van de prognosepositie en gebruikt voor informatie en bij het genereren van loonsverhogingen.

### <a name="creating-new-forecast-positions"></a>Nieuwe prognoseposities maken

U kunt nieuwe prognoseposities op twee manieren maken: door een bestaande prognosepositie te kopiëren en door een geheel nieuwe prognosepositie te maken. 

Wanneer een prognosepositie is geselecteerd, selecteert u **De geselecteerde prognosepositie kopiëren** om een nieuwe prognosepositie te maken met de prognosestatus **Voorgesteld**. Deze prognosepositie bevat dezelfde gegevens als de prognosepositie die is gekopieerd, behalve de toegewezen werknemer en eventuele notities over de budgetkostenelementen. Merk op dat er ook een bijbehorende nieuwe positie wordt gemaakt in Human resources. Deze positie is een beschrijving **Gemaakt door prognose**. 

U kunt ook een geheel nieuwe prognosepositie maken. Selecteer een bestaande taak, en selecteer tevens het budgetplanningsproces en budgetplanscenario. U kunt vervolgens andere gegevens toevoegen. Wederom wordt tegelijkertijd een nieuwe gemaakt positie tegelijk in Human resources.

## <a name="working-with-forecast-positions"></a>Werken met prognoseposities
[![Afbeelding van het wijzigen van prognoseposities](./media/graphic5-1024x327.png)](./media/graphic5.png)

### <a name="multiple-versions-of-a-forecast-position"></a>Meerdere versies van een prognosepositie

U kunt prognoseposities wijzigen om bekende wijzigingen voor de budgetcyclus toe te passen of om voorgestelde wijzigingen te modelleren. Een veelvoorkomende praktijk is een basislijnset met prognoseposities te maken, kopieën te maken van die prognoseposities en vervolgens de kopieën te gebruiken om verschillende sets wijzigingen te modelleren. Kopieën worden toegewezen aan een ander budgetplanscenario maar zijn, ten minste tot er wijzigingen worden aangebracht, gelijk aan de prognoseposities waarvan ze van zijn gekopieerd. De voor originelen en kopieën delen dezelfde positie in Human resources. 

De functie **Naar scenario kopiëren** functie biedt deze functionaliteit. Merk op dat elke Human resources-positie slechts één prognosepositie kan hebben in elk afzonderlijk budgetplanscenario.

### <a name="modifying-forecast-positions"></a>Prognoseposities wijzigen

Wijzigingen die zijn gemaakt om posities te prognosticeren, zijn beperkt tot die prognoseposities. De wijzigingen beïnvloeden niet de Positierecords in Human resources. De meeste wijzigingen zijn ook beperkt tot de prognosepositie die wordt bewerkt. Met andere woorden, de wijzigingen zijn specifiek voor het budgetplanningsproces en het budgetplanscenario die zijn toegewezen. De uitzonderingen zijn wijzigingen aan velden die voor de positie over processen en scenario's worden gedeeld. Deze velden omvatten de velden op het tabblad **Algemeen** en het tabblad **Financiële dimensies**. Als deze velden worden gewijzigd, gelden de nieuwe waarden op de positie in alle budgetplanningscenario's. Daarom kunt u met deze velden snel alle versies bijwerken.

#### <a name="budget-cost-elements"></a>Budgetkostenelementen

Budgetkostenelementen bieden de belangrijkste informatie voor budgetplannen: het budgetbedrag en de hoofdrekening. De budgetbedrag is het bedrag dat aan het budgetplan wordt verzonden wanneer een prognosepositie in een plan wordt opgenomen. De budgetbedrag wordt berekend en kan niet direct worden gewijzigd. Dit bedrag is het jaarlijkse bedrag of een berekening van het percentage de basiselementen van het jaarlijkse bedrag (zoals gedefinieerd in de instellingen van het budgetkostenelement). Het bedrag wordt vervolgens berekend met het aantal dagen in het datumbereik van het element (begindatum tot einddatum) en ook door de waarde **Voltijdse equivalent** (FTE) voor de prognosepositie. 

Een budgetkostenelementregel van 1 januari 2017 tot 30 juni 2017 die een jaarlijks bedrag heeft van 100.000 en een FTE-waarde van **0,50**, wordt bijvoorbeeld berekend als 100.000 × (181 dagen ÷ 365 dagen) × 0,50 = 24.794,52. 

De budgetkostenelementenregels moeten worden opnieuw berekend wanneer de FTE-waarde op de prognosepositie wordt gewijzigd. De regels moeten ook worden opnieuw berekend wanneer de activering datums of buitengebruikstellingsdata worden gewijzigd. Wijzigingen in deze datums kunnen een update van de begin- en einddatum van het budgetkostenelement veroorzaken, die moet liggen tussen de datums van de prognosepositie. Wanneer de herberekening wordt vereist, wordt de knop **Opnieuw berekenen** beschikbaar, en wordt het bericht 'Vereist berekening' weergegeven. De herberekening is ook verplicht als een budgetkostenelement toevoegt of een verwijdert.

**Voorbeeld** 

De organisatie overweegt twee opties om de kosten van een accountantspositie te drukken. Een optie is om de positie halverwege het jaar te beëindigen. De andere optie is om de positie naar parttime te wijzigen voor het hele jaar. Brad heeft een prognosepositie gemaakt voor de bestaande accountantspositie in een basislijnscenario. Hij kopieert deze basislijnprognosepositie naar scenario A, stelt de persioneringsdatum in op 31 mei en berekent opnieuw. Brad kopieert vervolgens de basislijnprognosepositie naar B, wijzigt de FTE-waarde in **0,50** en berekent opnieuw. Brad heeft nu drie versies, elk waarvan totalen heeft die op zijn opties zijn afgestemd.

#### <a name="assigning-a-compensation-group"></a>Een compensatiegroep toewijzen

Als u voor het eerst een compensatiegroep aan een prognosepositie toewijst, worden de standaard budgetkostenelementen van de compensatiegroep toegevoegd. Als kostenelementen al aan de prognosepositie zijn toegewezen, blijven deze kostenelementen. Als een compensatiegroep al is toegewezen en wordt gewijzigd, worden de bestaande budgetkostenelementen verwijderd en vervangen door de set uit de compensatiegroep. 

Wanneer u en compensatieniveau en -stap selecteert, wordt een budgetkostenelement voor opbrengsten (zoals gedefinieerd in de compensatiegroep) toegevoegd. Het jaarlijkse bedrag wordt berekend voor het gebruik van het tarief in het geselecteerde niveau en de stap, en jaarlijkse uren in de compensatiegroep (of, voor een salaris op jaarbasis , het volledige bedrag in het niveau en de stap.) Wederom wordt dit bedrag berekend aan de hand van het datumbereik van de kostenelementregel en de FTE-waarde de prognosepositie.

#### <a name="generating-increases"></a>Verhogingen genereren

Jaarlijkse verhogingen (één per kalenderjaar) kunnen automatisch worden gemaakt voor prognoseposities met een stapgebaseerde toegewezen compensatiegroep. Klik op **Verhogingen genereren** om een kostenelement inkomstenbudget toe te voegen aan de volgende hoogste stap. De begindatum van het nieuwe budgetkostenelement voor opbrengsten is de geplande verhogingsdatum die op de prognosepositie wordt weergegeven. Deze datum wordt op een van de volgende twee manieren ingesteld op basis van de compensatiegroep. Als de verhogingsplanning van de compensatiegroep is ingesteld op **Gemeenschappelijke datum**, wordt de datum van de verhoging opgegeven in de compensatiegroep. Als de verhogingsplanning is ingesteld op **Jubileumdatum**, wordt het jubileumdatumveld in de prognosepositie gebruikt en levert de budgetcyclus het jaar. Als een budgetcyclus meerdere kalenderjaren bevat, worden er meerdere verhogingen toegevoegd. 

De einddatum van de huidige budgetkostenelement voor opbrengsten wordt bijgewerkt met de dag vóór de verhogingsdatum. Het herberekeningsproces wordt automatisch gebruikt wanneer de verhogingen worden gegenereerd. Daarom hoeft u niet handmatig opnieuw te berekenen. 

Als u een tweede keer op **Verhogingen genereren** klikt, wordt het proces opnieuw uitgevoerd, maar worden niet meer records toegevoegd. Slechts één verhoging per kalenderjaar wordt gemaakt.

#### <a name="changes-from-other-pages"></a>Wijzigingen vanuit andere pagina's

De updates voor prognoseposities kunnen ook uit andere gebieden komen, zoals het budgetkostenelement element en pagina's voor compensatiegroepinstellingen. U kunt prognoseposities ook wijzigen door het massabijwerkproces te gebruiken. 

Twee opties zijn beschikbaar op de instelpagina **Budgetkostenelement**: **Aan posities toevoegen** en **Posities bijwerken**. De optie **Aan posities toevoegen** voegt het budgetkostenelement toe aan de geselecteerde prognoseposities. Als het element al aan een prognosepositie is toegewezen, wordt deze prognosepositie overgeslagen. De optie **Posities bijwerken** past de huidige waarden (de hoofdrekening, procent, jaarlijks bedrag, enzovoort) toe op de geselecteerde prognoseposities. 

Elk proces heeft een vergelijkbare pagina waarin u prognoseposities kunt selecteren. De pagina **Aan posities toevoegen** bevat alle prognoseposities die beschikbaar zijn voor selectie, terwijl de pagina **Posities bijwerken** alleen die prognoseposities weergeeft die al een budgetkostenelement toegewezen hebben gekregen. (Daarom biedt de pagina **Posities bijwerken** een manier om erachter te komen aan welke prognoseposities al het kostenelement is gekoppeld.) U verplaatst prognoseposities van het bovenste raster naar een lager raster om ze in de update op te nemen. 

Merk op dat de **Wijzigingsdata** functie op het **Kostenberekening** tabblad de begin- en einddata van het budgetkostenelement onmiddellijk wijzigt op de prognoseposities. Er zijn geen selectieopties beschikbaar. 

Op de **Compensatiegroep** pagina past de functie **Positietarieven bijwerken**, de huidige tarieven uit de huidige compensatietarieventabel toe op de prognoseposities die zijn toegewezen aan de groep. De percentages worden bijgewerkt en extra kostelementregels worden toegevoegd voor alle nieuwe tarieftabelregels (op datums gebaseerd.) De budgetkostenelementen en de verhogingsdatums worden echter niet bijgewerkt. U kunt selecteren welke budgetplanningsprocessen en budgetplanscenario's worden bijgewerkt. Daarom kunt u één scenario bijwerken maar andere scenario's ongewijzigd laten voor vergelijking. 

Door prognoseposities te selecteren en vervolgens op **Groepsgewijs bijwerken** te klikken kunt u meerdere prognoseposities tegelijk toevoegen of wijzigen. Er zijn verschillende opties beschikbaar. Een optie op het **Financiële dimensies** tabblad verschilt iets van de andere en is gerelateerd aan budgetkostenelementen. U kunt budgetkostenelementen toevoegen door de optie **Budgetstandaarden** in te stellen op **Ja**. Als geen budgetkostenelementen zijn geselecteerd, maar **Budgetstandaarden** is ingesteld op **Ja**, worden alle budgetkostenelementen die momenteel zijn toegewezen, verwijderd. 

Het herberekeningsproces wordt automatisch gebruikt op elke prognosepositie die is gewijzigd.

## <a name="bringing-forecast-positions-into-budget-plans"></a>Prognoseposities naar budgetplannen brengen

[![Afbeelding van toevoegen aan budgetplan](./media/graphic6-1024x327.png)](./media/graphic6.png)

Het maken en wijzigen van prognoseposities heeft als doel om ze toe te voegen aan budgetplannen, zodat de budgetplannen de nauwkeurigste budgetbedragen bevatten. Er zijn twee methoden voor het toevoegen van prognoseposities aan budgetplannen. U kunt een proces voor het genereren of selecteren gebruiken voor het budgetplan.

### <a name="generating-a-budget-plan-from-forecast-positions"></a>Budgetplan genereren op basis van prognoseposities

De optie **Budgetplan genereren op basis van prognoseposities** maakt budgetplannen of werkt deze bij, zodat ze de budgetbedragen en FTE-tellingen van de prognoseposities hebben. De budgetbedragen van de prognosepositie worden de regelbedragen van het budgetplan en worden samengevoegd aan de hand van financiële dimensiewaarden en ingangsdatum. Het generatieproces wijst de bronprognosepositie toe aan de budgetplanregel. U kunt de positie weergeven door de prognosepositie toe te voegen als rij in de budgetplanindeling of door de query **Budgetplanregels** te gebruiken. Als u deze toewijzing wilt overslaan, stelt u **Positie opnemen op budgetplanregel** in op **Nee**. 

U kunt een FTE-scenario van een budgetplan selecteren om het aantal FTE's in het budgetplan op te nemen. U kunt alleen scenario's selecteren van het hoeveelheidstype dat is opgenomen in de indeling van het doelbudgetplan. Wanneer u een FTE-scenario selecteert, moet u ook een FTE-hoofdrekening opgeven. Deze rekening wordt gebruikt om de regels van hoeveelheidsbudgetplan te maken. 

Het budgetplanningsproces en budgetplanscenario die in de bron zijn geselecteerd bepalen het budgetplanningsproces en budgetplanscenario van het doelscenario. Omdat deze kenmerken aan prognoseposities worden toegewezen, moeten ze gesynchroniseerd zijn met het budgetplan. Daarom kunnen de kenmerken in de doelstelling niet worden bewerkt. 

Net als bij andere genereerprocessen zijn er drie opties beschikbaar:

-   **Een nieuw budgetplan maken** – maakt een nieuw plan dat de kenmerken heeft die in de sectie **Doel** worden geselecteerd.
-   **Vervang het bestaande budgetplanscenario** – Verwijdert alle gegevens in het doelbudgetplan in het geselecteerde budgetplanscenario en maakt nieuwe regels die de geselecteerde prognosepositiegegevens bevatten.
-   **Het bestaande budgetplanscenario bijwerken en nieuwe gegevens toevoegen** – Werkt bestaande regels in het doelplan bij die overeenkomen met de bronregels en voegt ook nieuwe regels voor nieuwe gegevens toe. De vereffening is gebaseerd op de grootboekrekening, de datum, budgetklasse, en andere waarden, zoals de prognosepositie. Alle regels die een positienummer hebben dat overeenkomt met de bronpositie, worden vervangen door de nieuwe regels uit de bron.

### <a name="selecting-forecast-positions"></a>Prognoseposities selecteren

U kunt de budgetbedragen van de prognosepositie ook direct aan een budgetplan toevoegen. Gebruik de functie **Posities toevoegen** boven de budgetplanregels om de prognoseposities te selecteren die u wilt opnemen. 

De budgetplanscenario's die u als de bron kunt selecteren zijn beperkt tot scenario's die in de indeling van het plan zijn opgenomen. Met een optie op het **Doel** tabblad kunt u opgeven dat het FTE-scenario en de hoofdrekening beschikbaar zijn om FTE-tellingen in op te nemen, maar dat dit niet verplicht is. 

Dit selectieproces gedraagt zich als de optie **Het bestaande budgetplanscenario bijwerken en nieuwe gegevens toevoegen** voor een genereerproces. Alle bestaande budgetplanregels waar de prognosepositie wordt toegevoegd, worden verwijderd en vervangen door nieuwe regels die zijn gebaseerd op de huidige status van de prognosepositie.

#### <a name="date-options"></a>Datumopties

Voor zowel het genereer- als het selectieproces bepaalt de begindatum op de budgetkostenelementregel de ingangsdatum van de bijbehorende budgetplanregel. Het veld **Toewijzingsmethode** op de instelpagina van het budgetkostenelement vermeldt de toewijzingsmethode:

-   **Begindatum** - De begindatum van het budgetkostenelement wordt gebruikt als de ingangsdatum van de budgetplanregel.
-   **Maandelijks** - Het budgetbedrag wordt evenredig gedeeld door het aantal maanden van het datumbereik om een typisch maandelijks bedrag te produceren dat op de eerste dag van elke maand wordt toegewezen. Als de eerste periode een gedeeltelijke maand is, wordt het bedrag voor die maand verrekend met het aantal dagen dat de kosten actief zijn in die maand en wordt het resultaat toegewezen aan de begindatum. Het bedrag van de laatste maand is het verschil tussen het totale budgetbedrag en de som van alle andere maanden. Daarom is de afronding mogelijk van invloed op het bedrag voor de laatste maand.
-   **Per kwartaal** - Deze methode is gelijk aan **Maandelijks**, maar de berekeningen worden uitgevoerd voor perioden van drie maanden.
-   **Wekelijks** - De logica lijkt op de logica van de methoden **Maandelijks** en **Driemaandelijks**. Het budgetbedrag wordt evenredig gedeeld door het aantal weken van het datumbereik om een typisch wekelijks bedrag te produceren dat op de eerste dag van elke week wordt toegewezen. Als de eerste periode een gedeeltelijke week is, wordt het bedrag voor die week verrekend met het aantal dagen dat de kosten actief zijn in die week en wordt het resultaat toegewezen aan de begindatum. Het bedrag van de laatste week is het verschil tussen het totale budgetbedrag en de som van alle andere weken. Daarom is de afronding mogelijk van invloed op het bedrag voor de laatste week.
-   **Om de twee weken** - Deze methode is gelijk aan **Wekelijks**, maar de berekeningen worden uitgevoerd voor perioden van twee weken.

#### <a name="changing-budget-plan-lines-that-have-forecast-positions"></a>Budgetplanregels wijzigen die prognoseposities hebben

Budgetplanregels tonen de bron van de budgetbedragen (het nummer van de prognosepositie), maar zijn niet gekoppeld. Daarom worden wijzigingen in de prognosepositie niet weergegeven op de regel van het budgetplan en worden wijzigingen in de regel van het budgetplan weergegeven in de prognosepositie. Als u een prognosepositie wijzigt en wilt dat de updates worden opgenomen in een budgetplan, moet u de prognosepositie weer in het plan opnemen. Dit proces verwijdert echter alle regels waar die prognosepositie wordt toegewezen. Daarom worden alle wijzigingen die u hebt aangebracht in die regels verwijderd. 

Om te zien in welke budgetplannen een prognosepositie is opgenomen, kunt u in het rapport **Prognoseposities per budgetplan** genereren. Als alternatief kunt u op de prognosepositie het feitenvak **Gekoppelde budgetplannen** openen om de plannen weer te geven.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]