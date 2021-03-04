---
title: Werken met locatie-instructies
description: In dit onderwerp wordt beschreven hoe u met locatie-instructies werkt. Locatie-instructies zijn door gebruiker gedefinieerde regels voor het aangeven van verzamel- en wegzetlocaties voor voorraadverplaatsingen.
author: Mirzaab
manager: tfehr
ms.date: 11/13/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLocDirTable, WHSLocDirHint, WHSLocDirTableUOM, WHSLocDirFailure
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-11-13
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: f56257fd3f2f681bbd514843d8ddafa2395648d3
ms.sourcegitcommit: 4bf5ae2f2f144a28e431ed574c7e8438dc5935de
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/13/2020
ms.locfileid: "4517471"
---
# <a name="work-with-location-directives"></a>Werken met locatie-instructies

[!include [banner](../includes/banner.md)]

De locatierichtlijnen zijn regels die verzamelings- en wegzetlocaties identificeren voor voorraadverplaatsing. In een verkoopordertransactie kan een locatierichtlijn bijvoorbeeld bepalen waar de artikelen worden verzameld en waar de verzamelde artikelen worden geplaatst. Locatie-instructies bestaan uit een kop en bijbehorende regels. Deze worden gemaakt voor specifieke *werkordertypen*.

> [!NOTE]
> Dit onderwerp geldt voor functies in de module voor **Magazijnbeheer**. Het is niet van toepassing op functies in de module [Voorraadbeheer](../inventory/inventory-home-page.md).

Met locatie-instructies kunt u de volgende taken uitvoeren:

- Binnenkomende artikelen wegzetten.
- Artikelen verzamelen en faseren voor uitgaande transacties.
- Grondstoffen verzamelen en klaarzetten voor productie.
- Locaties aanvullen.

## <a name="prerequisites"></a>Vereisten

Voordat u een locatie-instructie kunt maken, moet u deze stappen volgen om er zeker van te zijn dat aan de vereisten wordt voldaan.

1. Controleer of de vereiste licentiesleutel is ingeschakeld. Ga naar **Systeembeheer \> Setup \> Licentieconfiguratie**, vouw de licentiesleutel **Handel** uit en selecteer de configuratiesleutel **Magazijn- en transportbeheer**. Beheerderstoegang is vereist voor deze stap.
1. Ga naar **Magazijnbeheer \> Instellen \> Magazijn \> Magazijnen**.
1. Een magazijn maken.
1. Stel op het sneltabblad **Magazijn** de optie **Magazijnbeheerprocessen gebruiken** in op *Ja*.
1. Locaties, locatietypen, locatieprofielen en locatie-indelingen maken. Zie [Locaties configureren in een magazijn met WMS-ondersteuning](https://docs.microsoft.com/dynamics365/supply-chain/warehousing/tasks/configure-locations-wms-enabled-warehouse) voor meer informatie.
1. Maak locaties, zones en zonegroepen. Zie [Magazijn instellen](https://docs.microsoft.com/dynamics365/commerce/channels-setup-warehouse) en [Locaties configureren in een magazijn met WMS-ondersteuning](https://docs.microsoft.com/dynamics365/supply-chain/warehousing/tasks/configure-locations-wms-enabled-warehouse) voor meer informatie.

## <a name="work-order-types-for-location-directives"></a>Werkordertypen voor locatie-instructies

Veel van de velden die kunnen worden ingesteld voor locatie-instructies, gelden voor alle werkordertypen. Andere velden zijn echter specifiek voor bepaalde typen werkorders.

![Werkordertypen voor locatie-instructies](media/Location_Directives_Work_Order_Types.png "Werkordertypen voor locatie-instructies")

> [!NOTE]
> Twee werkordertypen, *Geannuleerd werk* en *Cyclustelling*, worden alleen door het systeem gebruikt. Er kunnen geen locatie-instructies worden gemaakt voor deze typen werkorders.

In de tabellen in de volgende subsecties worden de algemene velden en de specifieke velden voor werkordertypen weergegeven die beschikbaar zijn wanneer u een locatie-instructie instelt.

### <a name="fields-that-are-common-to-all-work-order-types"></a>Velden die gemeenschappelijk zijn voor alle werkordertypen

In de volgende tabel worden de velden weergegeven die voor alle werkordertypen gelden.

| Sneltabblad | Veld |
|---|---|
| Locatie-instructies | Werktype |
| Locatie-instructies | Locatie |
| Locatie-instructies | Magazijn |
| Locatie-instructies | Instructiecode |
| Locatie-instructies | Meerdere SKU's |
| Regels | Volgnummer |
| Regels | Vanaf hoeveelheid |
| Regels | Tot hoeveelheid |
| Regels | Eenheid |
| Regels | Hoeveelheid plaatsen |
| Regels | Beperken op eenheid |
| Regels | Naar eenheid afronden |
| Regels | Zoek verpakkingshoeveelheid |
| Regels | Splitsing toestaan |
| Locatie-instructieacties | Volgnummer |
| Locatie-instructieacties | Naam |
| Locatie-instructieacties | Gebruik vaste locaties |
| Locatie-instructieacties | Negatieve voorraad toestaan |
| Locatie-instructieacties | Batch ingeschakeld |
| Locatie-instructieacties | Strategie |

### <a name="fields-that-are-specific-to-work-order-types"></a><a name="fields-specific-types"></a>Velden die specifiek zijn voor bepaalde werkordertypen

In de volgende tabel worden de velden weergegeven die specifiek zijn voor bepaalde werkordertypen.

| Sneltabblad | Veld | Werkordertype |
|---|---|---|
| Locatie-instructies | Zoeken op | Inkooporders |
| Locatie-instructies | Toepasbare beschikkingscode | Inkooporders |
| Locatie-instructies | Beschikkingscode | Inkooporders |
| Locatie-instructies | Toepasbare beschikkingscode | Eindproducten wegzetten |
| Locatie-instructies | Beschikkingscode | Eindproducten wegzetten |
| Locatie-instructies | Toepasbare beschikkingscode | Retourorders |
| Locatie-instructies | Beschikkingscode | Retourorders |
| Locatie-instructies | Toepasbare beschikkingscode | Kanban wegzetten |
| Locatie-instructies | Toepasbare beschikkingscode | Kanbanorderverzameling |
| Regels | Sjabloon voor directe aanvulling | Verkooporders |
| Regels | Sjabloon voor directe aanvulling | Orderverzameling van grondstoffen |
| Regels | Sjabloon voor directe aanvulling | Overboekingsuitgifte |
| Regels | Sjabloon voor directe aanvulling | Kanbanorderverzameling |

## <a name="open-the-location-directives-page"></a>Open de pagina Locatie-instructies

Om de pagina **Locatie-instructies** te openen, gaat u naar **Magazijnbeheer \> Setup \> Locatie-instructies**.

Hier kunt u de locatie-instructies weergeven, maken en bewerken met de opdrachten in het actiedeelvenster. Zie de overige secties van dit onderwerp voor informatie over het gebruik van alle velden die beschikbaar zijn op de pagina.

## <a name="action-pane"></a>Actievenster

Het actiedeelvenster op de pagina **Locatie-instructies** bevat knoppen die u kunt gebruiken voor het maken, bewerken en verwijderen van instructies (**bewerken**, **Nieuw** en **Verwijderen**). Het bevat ook de volgende knoppen waarmee u de volgorde kunt aanpassen waarin de instructie voor de locatie wordt verwerkt en een query configureert die de criteria voor het toepassen van de locatie-instructie definieert:

- **Omhoog**: verplaats de geselecteerde locatie-instructie omhoog in de volgorde. U kunt deze bijvoorbeeld verplaatsen van volgnummer 4 naar volgnummer 3.
- **Omlaag**: verplaats de geselecteerde locatie-instructie omlaag in de volgorde. U kunt deze bijvoorbeeld verplaatsen van volgnummer 4 naar volgnummer 5.
- **Query bewerken**: hiermee opent u een dialoogvenster waarin u de voorwaarden kunt definiëren volgens welke de geselecteerde locatie-instructie moet worden verwerkt. U wilt bijvoorbeeld dat het alleen op een specifiek magazijn van toepassing is.

## <a name="location-directives-header"></a>Kop van locatie-instructie

De kop van de locatie-instructie bevat de volgende velden voor het volgnummer en de beschrijvende naam van de locatie-instructie:

- **Volgnummer**: dit veld geeft de volgorde aan waarop het systeem probeert elke locatie-instructie toe te passen op het geselecteerde werkordertype. De laagste nummers worden het eerst toegepast. U kunt de volgorde wijzigen met de knoppen **Omhoog** en **Omlaag** in het actiedeelvenster.
- **Naam**: voer een beschrijvende naam voor de locatie-instructie in. Deze naam moet helpen bij het identificeren van het algemene doel van de instructie. Voer bijvoorbeeld *Verkooporders verzamelen in magazijn 24* in.

## <a name="location-directives-fasttab"></a>Sneltabblad Locatierichtlijnen

De velden op het sneltabblad **Locatie-instructies** zijn specifiek voor het werkordertype dat is geselecteerd in het veld **Werkordertype** in het lijstdeelvenster.

- **Werktype**: selecteer het type werk dat moet worden uitgevoerd. De beschikbare waarden hangen af van het type voorraadtransactie dat u in het veld **Werkordertype** hebt geselecteerd. Selecteer een van de volgende waarden:

    - **Neerzetten**: de locatie-instructie zoekt naar de best mogelijke locatie voor het plaatsen of vinden van voorraad die in het systeem komt vanuit ontvangst, productie of voorraadcorrecties. Het kan ook worden gebruikt om de faseringslocatie voor neerzetten of de laaddeur voor de uiteindelijke verzendlocatie te definiëren.
    - **Verzamelen**: de locatie-instructie probeert de best mogelijke locaties te vinden voor het fysiek reserveren van voorraad (dat wil zeggen, werk maken). De verzameling kan ook worden voltooid (verzamelwerkregel kan worden gesloten) als het werk niet is voltooid. De gebruiker kan de fysieke orderverzameling voltooien. In het systeem is die actie een verzamelstap. De gebruiker kan vervolgens annuleren vanaf het mobiele apparaat en het werk later voltooien. De werkkoptekst wordt echter pas gesloten wanneer de laatste plaatsing is voltooid.

    > [!IMPORTANT]
    > De andere waarden in het veld **Werktype** zijn niet relevant voor locatie-instructies. Deze worden alleen weergegeven omdat het veld niet is gefilterd, zodat dit overeenkomt met het geselecteerde werkordertype.

- **Site**: dit is een verplicht veld omdat de locatie-instructie moet kunnen bepalen voor welke site en magazijn deze geldig is.
- **Magazijn**: dit is een verplicht veld omdat de locatie-instructie moet kunnen bepalen voor welke site en magazijn deze geldig is.
- **Instructiecode**: selecteer de instructiecode om aan een werksjabloon of aanvullingssjabloon te koppelen. Op de pagina **Instructiecode** kunt u nieuwe codes maken die kunnen worden gebruikt om werksjablonen of aanvullingssjablonen te koppelen aan locatie-instructies. Instructiecodes kunnen ook worden gebruikg om een koppeling tussen een werksjabloonregel en een locatie-instructie tot stand te brengen (zoals een laaddeur of faseringslocatie).

    > [!TIP]
    > Als er een instructiecode is ingesteld, zoekt het systeem niet naar locatie-instructies op volgnummer wanneer er werk moet worden gegenereerd. In plaats daarvan wordt gezocht op instructiecode. Zo kunt u specifiek opgeven welke locatiesjabloon wordt gebruikt voor een bepaalde stap in een werksjabloon, zoals de stap voor de fasering van materialen.

- **Meerdere SKU's**: stel deze optie in op *Ja* om meerdere voorraadeenheden (SKU's) op een locatie te kunnen gebruiken. Er moeten bijvoorbeeld meerdere SKU's worden ingeschakeld voor de laaddeurlocatie. Als u meerdere SKU's inschakelt, wordt uw neerzetlocatie volgens verwachting opgegeven bij werk. De neerzetlocatie kan echter alleen een locatie met meerdere artikelen verwerken (als het werk bestaat uit verschillende SKU's die moeten worden verzameld en opgeslagen). Het is niet mogelijk een neerzetlocatie met één SKU te verwerken. Als u deze optie op *Nee* instelt, wordt de neetzetlocatie alleen opgegeven als deze slechts één type SKU heeft.

    > [!IMPORTANT]
    > U moet twee regels met dezelfde structuur en instelling opgeven, maar u moet de optie **Meerdere SKU's** op *Ja* instellen voor één regel en *Nee* voor de andere, zodat u zowel sets met meerdere artikelen als sets met één SKU kunt doen. Daarom hebt u voor neerzetbewerkingen twee identieke locatie-instructies nodig, zelfs als u geen onderscheid hoeft te maken tussen enkele en meerdere SKU's op een werk-id. Als u deze locatie-instructies niet instelt, komen er onverwachte locaties voor bedrijfsprocessen uit de toegepaste locatie-instructie. U moet een vergelijkbare instelling gebruiken voor locatie-instructies met het **Werktype** *Verzamelen* als u orders met meerdere SKU's wilt verwerken.

    Gebruik de optie **Meerdere SKU's** voor werkregels die meer dan één artikelnummer verwerken. (Het artikelnummer is leeg bij de werkdetails en wordt weergegeven als **Meerdere** op de verwerkingspagina's in de magazijn-app.)

    In een typisch voorbeeldscenario is een werksjabloon zo ingesteld dat deze over meerdere verzamel/neerzetparen beschikt. In dat geval kunt u zoeken naar een specifieke faseringslocatie voor regels met het **Werktype** *Neerzetten*.

    > [!NOTE]
    > Als de optie **Meerdere SKU's** is ingesteld op *Ja*, kunt u niet **Query bewerken** selecteren in het actiedeelvenster, omdat de query niet op artikelniveau kan worden geëvalueerd wanneer er meerdere artikelen zijn. Om er zeker van te zijn dat de gewenste locatie-instructie wordt geselecteerd, gebruikt u het veld **Instructiecode** om de selectie van de locatie-instructie te leiden die is gerelateerd aan de neerzetregels waarin deze instructiecode is toegewezen in de werksjabloon.

    Tenzij u altijd werkt met bewerkingen voor ofwel één of artikel ofwel gemengde artikelen , is het belangrijk dat u twee locatie-instructies definieert voor het werktype *Neerzetten*: een waarbij de optie **Meerdere SKU's** is ingesteld op *Ja* en een locatie waar deze is ingesteld op *Nee*.

- **Toepasselijke beschikkingscode**: geef op of de beschikkingscode van de locatie-instructie moet overeenkomen met de beschikkingscode die wordt toegepast wanneer het artikel wordt ontvangen of dat de locatie-instructie op basis van elke beschikkingscode kan worden geselecteerd. Als u *Exacte overeenkomst* selecteert en het veld **Beschikkingscode** leeg is, worden alleen lege beschikkingscodes gebruikt voor deze locatie-instructie.

    > [!NOTE]
    > Dit veld is alleen beschikbaar voor de geselecteerde werkordertypen waar aanvulling is toegestaan. Zie voor een volledige lijst de sectie [Velden die specifiek zijn voor werkordertypen](#fields-specific-types) eerder in dit onderwerp.

- **Zoeken op**: geef op of de wegzethoeveelheid de gehele hoeveelheid op de nummerplaat moet zijn of dat deze per artikel moet zijn. Gebruik dit veld om ervoor te zorgen dat alle inhoud van een nummerplaat op één locatie wordt geplaatst en dat het systeem niet suggereert dat u de inhoud opsplitst in verschillende locaties voor **ASN** (nummerplaat voor ontvangen), **Gecombineerde nummerplaat** voor ontvangen en **Cluster** ontvangstprocessen. (Het **Cluster** ontvangstproces vereist dat de *functie Cluster wegzetten* wordt ingeschakeld.) Het gedrag van de query voor locatie-instructies, de regels en de locatie-instructieacties zijn afhankelijk van de waarde die u selecteert. Het sneltabblad **Regels** regels wordt alleen gebruikt wanneer **Zoeken op** is ingesteld op *Artikel*.

    > [!NOTE]
    > Dit veld is alleen beschikbaar voor de geselecteerde werkordertypen waar aanvulling is toegestaan. Zie voor een volledige lijst de sectie [Velden die specifiek zijn voor werkordertypen](#fields-specific-types).

- **Beschikkingscode**: dit veld wordt gebruikt voor locatie-instructies met het werkordertype *Inkooporders*, *Eindproducten wegzetten* of *Retourorders* en een werktype *Neerzetten*. Gebruik dit om de stroom te leiden voor het gebruik van een specifieke locatie-instructie, afhankelijk van de beschikkingscode die een medewerker in de magazijn-app heeft geselecteerd. U kunt bijvoorbeeld terugkerende goederen naar een inspectielocatie sturen voordat deze naar de voorraad worden geretourneerd. U kunt een beschikkingscode koppelen aan een voorraadstatus. Op deze manier kan deze worden gebruikt om de voorraadstatus te wijzigen als onderdeel van een ontvangstproces. U hebt bijvoorbeeld een beschikkingscode *QA* die de voorraadstatus instelt op *QA*. U kunt vervolgens een afzonderlijke locatie-instructie krijgen om die voorraad naar een quarantainelocatie te verplaatsen.

    > [!NOTE]
    > Dit veld is alleen beschikbaar voor de geselecteerde werkordertypen waar aanvulling is toegestaan. Zie voor een volledige lijst de sectie [Velden die specifiek zijn voor werkordertypen](#fields-specific-types).

## <a name="lines-fasttab"></a>Sneltabblad Regels

Gebruik het sneltabblad **Regels** om voorwaarden vast te leggen voor het toepassen van de gerelateerde acties die zijn opgegeven op het sneltabblad **Locatie-instructieacties**. Voor elke regel kiunt u de minimumhoeveelheid en een maximumhoeveelheid opgeven waarop de acties moeten worden toegepast. U kunt ook opgeven dat de acties moeten worden toegepast op een specifieke voorraadeenheid.

- **Volgnummer**: voer de volgorde in waarin elke locatie-instructie moet worden verwerkt voor het geselecteerde werktype. U kunt de volgorde desgewenst wijzigen met de knoppen **Omhoog** en **Omlaag** op de werkbalk.
- **Van hoeveelheid**: geef het begin op van het bereik van de hoeveelheden waarop de regel van toepassing is. Geef de hoeveelheid op in de maateenheid die is geselecteerd in het veld **Eenheid**.
- **Tot hoeveelheid**: geef het einde op van het bereik van de hoeveelheden waarop de regel van toepassing is. Geef de hoeveelheid op in de maateenheid die is geselecteerd in het veld **Eenheid**.
- **Eenheid**: selecteer de maateenheid voor de artikelen. U kunt een minimale en maximale hoeveelheid opgeven waarop de richtlijn wordt toegepast en u kunt opgeven dat de richtlijn voor een specifieke voorraadeenheid moet zijn. Het veld **Eenheid** wordt *alleen* gebruikt voor de evaluatie van de hoeveelheid. Om vast te stellen of de location-instructieregel van toepassing is, gebruikt het systeem de hoeveelheid in de eenheid die op deze regel is opgegeven. Elke keer dat het een locatie-instructieregel bereikt, wordt geprobeerd de vraageenheid om te zetten in een eenheid die is opgegeven op de regel. Als de maateenheidomrekening niet bestaat, gaat het systeem naar de volgende regel.
- **Hoeveelheid zoeken**: dit veld wordt alleen gebruikt tijdens pogingen om artikelen in het magazijn neer te zetten of te zoeken. (Het is dus alleen van toepassing wanneer het veld **Werktype** is ingesteld op *Neerzetten*). Selecteer een van de volgende waarden om de hoeveelheid op te geven die wordt gebruikt om te bepalen of een hoeveelheid binnen het bereik **Van hoeveelheid** naar **Tot hoeveelheid** valt:

    - **Hoeveelheid nummerplaat**: gebruik de hoeveelheid op de ontvangen nummerplaat.
    - **In eenheden omgezette hoeveelheid**: gebruik de hoeveelheid die tijdens de transactie wordt gebruikt. U ontvangt bijvoorbeeld een hoeveelheid van 1000 in een magazijn en deze wordt opgesplitst in 10 nummerplaten, elk met een hoeveelheid van 100. In dit geval kunt u een hoeveelheid van 1000 artikelen gebruiken in plaats van de hoeveelheid 100 van de nummerplaat.
    - **Resterende hoeveelheid**: gebruik de hoeveelheid die nog moet worden ontvangen op de inkooporderregel die wordt verwerkt.
    - **Verwachte hoeveelheid**: gebruik de totale hoeveelheid van de inkooporderregel, ongeacht wat al is ontvangen.

- **Beperken per eenheid**: met dit selectievakje kunt u de regel van de locatie-instructie voor een bepaalde maateenheid of meerdere maateenheden instellen. Schakel het in om de maateenheden te beperken die als geldige selectiecriteria worden beschouwd voor de locatie-instructieregels. Deze functionaliteit werkt alleen voor locatie-instructies waarvoor het veld **Werktype** is ingesteld op *Verzamelen*.

    Wanneer u bijvoorbeeld hoeveelheden reserveert, wilt u pallets alleen reserveren op een bepaalde set locaties. In dat geval worden deze reeksen door de regels beperkt tot pallets, zodat elke hoeveelheid die kleiner is dan een pallet, niet wordt geselecteerd voor de locatie-instructie.

    In het selectievakje **Beperken op eenheid** worden echter niet de eenheden bepaald die op werkregels zijn toegepast. De eenheidsbeperking geldt alleen voor eenheden die beschikbaar worden gemaakt via de eenheidsvolgordegroep. Een artikel is bijvoorbeeld gekoppeld aan een eenheidsvolgordegroep die zowel de eenheid *pallets* als de eenheid *stuks* bevat. Er is een maateenheid gedefinieerd waarbij 1 pallet = 100 stuks en de locatie-instructie gebruikt de functionaliteit **Beperken op eenheid** alleen voor pallets. Bovendien is er een werksjabloon gedefinieerd die het maken van de werkkoptekst beperkt tot 50 stuks. In dit geval worden werkregels van 50 stuks gemaakt. Voer de volgende stappen uit om de maateenheid voor de beperking op te geven:

    1. Selecteer op sneltabblad **Regels** de optie **Beperken per eenheid** op de werkbalk. (Deze knop is alleen beschikbaar als u het selectievakje **Beperken op eenheid** op de regel hebt ingeschakeld en vervolgens **Opslaan** hebt geselecteerd.)
    1. Selecteer op de pagina **Beperken per eenheid** in het veld **Eenheid** de maateenheid waarvoor u een beperking wilt instellen voor het verzamel- en neerzetproces.

- **Naar boven afronden op eenheid**: dit veld werkt samen met het selectievakje **Beperken per eenheid**. Als de locatie-instructieregel **Beperken op eenheid** en **Naar boven afronden op eenheid** bijvoorbeeld zijn geselecteerd op de locatie-instructieregel, moet het werk dat uit de instructie voor grondstoffen verzamelen is gegenereerd, naar boven worden afgerond tot een veelvoud van de materiaalverwerkingseenheid die is opgegeven op de pagina **Beperken op eenheid**.

    > [!NOTE]
    > Deze instelling **Naar boven afronden op eenheid** werkt alleen voor het werkordertype *Grondstoffen verzamelen* en alleen voor locatie-instructies waarvoor het veld **Werktype** is ingesteld op *Verzamelen*.

- **Verpakkingshoeveelheid zoeken**: als u een verpakkingshoeveelheid opgeeft op een verkooporder, een transferorder of een productieorder, kunt u met dit selectievakje het systeem beperken, zodat er alleen locaties met minimaal die verpakkingshoeveelheid kunnen worden geselecteerd.

    > [!NOTE]
    > Dit werkt alleen voor locatie-instructies van het type *Verzamelen*.

- **Splitsen toestaan**: geef op of de locatie-instructie de hoeveeldheid kan splitsen die wordt ontvangen of gereserveerd in meerdere magazijnlocaties, of dat de hele hoeveelheid zich in één locatie moet bevinden of vanuit één locatie moet worden gereserveerd om werk te maken.
- **Sjabloon voor directe aanvulling**: gebruik dit veld om een verbinding te maken met een aanvullingssjabloon, zodat de aanvulling direct wordt gestart als artikelen niet zijn toegewezen. Als u het veld leeg laat, wordt de aanvulling van artikelen pas gestart nadat alle regels van de locatie-instructie zijn verwerkt.

    > [!NOTE]
    > Dit veld is alleen beschikbaar voor de geselecteerde werkordertypen waar aanvulling is toegestaan. Zie voor een volledige lijst de sectie [Velden die specifiek zijn voor werkordertypen](#fields-specific-types).

## <a name="location-directive-actions-fasttab"></a>Sneltabblad Locatie-instructieacties

U kunt meerdere locatierichtlijnacties voor elke regel definiëren. Een volgnummer wordt dus gebruikt om de volgorde te bepalen waarin de acties worden beoordeeld. Op dit niveau kunt u een zoekopdracht instellen om te definiëren hoe de beste locatie kan worden gevonden. U kunt ook vooraf gedefinieerde waarden voor **Strategie** gebruiken om een optimale locatie te zoeken.

- **Volgnummer**: in dit veld wordt de volgorde weergegeven waarin de acties worden verwerkt voor het geselecteerde werktype. U kunt de volgorde wijzigen met de knoppen **Omhoog** en **Omlaag** op de werkbalk.
- **Naam**: voer in dit veld de naam in voor de locatie-instructieactie. Wees specifiek, zodat de actie die wordt uitgevoerd, duidelijk aan de naam te zien is.
- **Gebruik vaste locaties**: geef op welke locaties de locatie-instructie moet meenemen. Selecteer een van de volgende waarden:

    - **Vaste en niet-vaste locaties**: alle locaties komen in aanmerking voor de locatie-instructie.
    - **Alleen vaste locaties voor het product**: alleen vaste locaties voor producten komen in aanmerking voor de locatie-instructie.
    - **Alleen vaste locaties voor de productvariant**: alleen vaste locaties voor productvarianten komen in aanmerking voor de locatie-instructie.

- **Negatieve voorraad toestaan**: schakel dit selectievakje in om negatieve voorraad op de opgegeven magazijnlocatie in locatie-instructies toe te staan.
- **Batch ingeschakeld**: schakel dit selectievakje in om batchstrategieën voor de artikelen te gebruiken waarvoor batches zijn ingeschakeld. Het is belangrijk dat u dit selectievakje inschakelt voor processen die locatie-instructies gebruiken om locaties te vinden voor het verzamelen van met batchnummer getraceerde artikelen. Op deze manier wordt de zoekopdracht naar locaties met artikelen opgenomen die met batchnummers worden getraceerd. Als dit selectievakje is ingeschakeld en het veld **Strategie** is ingesteld op *Geen*, gaat het systeem verder naar de volgende actieregel.
- **Strategie**: om gemakkelijker en sneller de acties te definiëren die zijn gekoppeld aan elke locatie-instructieregel, kunt u een van de volgende vooraf gedefinieerde strategieën selecteren:

    - **Geen**: er wordt geen strategie gebruikt.
    - **Verpakkingshoeveelheid afstemmen**: deze strategie controleert of een orderverzamellocatie de benodigde verpakkingshoeveelheid heeft. Deze strategie is alleen geldig als het veld **Werktype** is ingesteld op *Orderverzamelen*.
    - **Consolideren**: deze strategie wordt gebruikt om artikelen in een bepaalde locatie te consolideren wanneer vergelijkbare artikelen beschikbaar zijn. Deze strategie is alleen geldig als het veld **Werktype** is ingesteld op *Wegzetten*. Een standaardinstelling voor neerzetten probeert op de eerste actieregel te consolideren en probeert vervolgens op de tweede actieregel neer te zetten zonder consolidatie. Door goederen te consolideren wordt orderverzamelen later efficiënter.
    - **FEFO-batchreservering**: deze strategie maakt gebruik van FEFO-batchreserveringen (first expired, first out: eerst verlopen, eerst eruit). Gebruik deze strategie wanneer de voorraad wordt gevonden aan de hand van eenv batchvervaldatum en waarvoor een batchreservering is toegewezen. U kunt deze strategie alleen maar voor batch ingeschakelde artikelen gebruiken. Deze strategie is alleen geldig wanneer het veld **Werktype** is ingesteld op *Verzamelen*.
    - **Naar boven afronden tot de volledige LP- en FEFO-batch**: deze strategie combineert de elementen van de strategieën *FEFO-batchreservering* en *Naar boven afronden tot de volledige LP*. Deze is alleen geldig voor batchartikelen en locatie-instructies met het werktype *Verzamelen*. Voor de regel moet batch zijn ingeschakeld voor het gebruik van de strategie *FEFO-batchreservering* en de strategie *Afronden naar boven tot de volledige LP* kan alleen worden gebruikt voor aanvulling. Als deze strategie samen met een locatievoorraadlimiet wordt geconfigureerd, kan hierdoor de geselecteerde neerzetwerklocatie overbelast raken en de voorraadlimieten worden genegeerd.
    - **Afronden naar boven tot volledige LP**: deze strategie wordt gebruikt om de voorraadhoeveelheid naar boven af te ronden om overeen te komen met de nummerplaathoeveelheid die is toegewezen aan de artikelen die moeten worden verzameld. U kunt deze strategie alleen gebruiken voor locatie-instructies voor aanvullen van het type *Verzamelen*. Als deze strategie samen met een locatievoorraadlimiet wordt geconfigureerd, kan hierdoor de geselecteerde neerzetwerklocatie overbelast raken en de voorraadlimieten worden genegeerd.
    - **Nummerplaatgeleid**: gebruik deze strategie wanneer u de order aan het magazijn vrijgeeft om verzamel-en-neerzetwerkzaamheden te maken. U kunt deze aanpak gebruiken voor meerdere nummerplaten. Deze strategie probeert orderverzamelingswerk te reserveren en te maken voor de locaties die de gevraagde nummerplaten bevatten die aan de transferorderregels zijn gekoppeld. Als deze acties echter niet kunnen worden voltooid, maar u nog steeds orderverzamelingstaken wilt maken, moet u terugvallen op een andere strategie voor locatie-instructieacties. Afhankelijk van de vereisten voor uw bedrijfsproces wilt u mogelijk ook naar voorraad zoeken in een ander gebied van het magazijn.
    - **Lege locatie zonder inkomend werk**: gebruik deze strategie om lege locaties te vinden. Een locatie wordt beschouwd als leeg als het geen fysieke voorraad en geen verwacht inkomend werk heeft. U kunt deze strategie alleen gebruiken voor locatie-instructies die het werktype *Verzamelen* hebben.
    - **Oudercom locatie FIFO**: gebruik de FIFO-strategie (first in, first out: eerste erin, eerste eruit) om artikelen met en zonder batchtracering te verzenden, op basis van de datum waarop de voorraad in het magazijn binnenkomt. Deze mogelijkheid kan vooral nuttig zijn voor voorraad zonder batchtracering, waarbij geen vervaldatum beschikbaar is voor sorteren. De FIFO-strategie zoekt naar de locatie die de oudste ouderdomsdatum bevat en wijst dan op basis van die ouderdomsdatum orderverzamelen toe.
    - **Oudercom locatie LIFO**: gebruik de LIFO-strategie (last in, last out: laatste erin, laatste eruit) om artikelen met en zonder batchtracering te verzenden, op basis van de datum waarop de voorraad in het magazijn binnenkomt. Deze mogelijkheid kan vooral nuttig zijn voor voorraad zonder batchtracering, waarbij geen vervaldatum beschikbaar is voor sorteren. De LIFO-strategie zoekt naar de locatie die de nieuwste ouderdomsdatum bevat en wijst dan op basis van die ouderdomsdatum orderverzamelen toe.

## <a name="example-using-location-directives"></a>Voorbeeld: locatie-instructies gebruiken

Voor dit voorbeeld kijken we naar een inkooporderproces waar de locatie-instructie vrije capaciteit in een magazijn moet zoeken voor voorraadartikelen die zojuist zijn geregistreerd in het ontvangende dok. Eerst moet u we beschikbare capaciteit in het magazijn vinden door te consolideren met bestaande voorhanden voorraad. Als consolidatie niet mogelijk is, moet u een lege locatie zoeken.

Voor dit scenario moet u twee locatie-instructieacties definiëren. De eerste actie in de reeks moet de *consolidatie*-strategie gebruiken, de tweede de *Lege locatie met geen inkomend werk*-strategie. Tenzij u een derde actie definieert om een overloopscenario te dekken, zijn er twee resultaten mogelijk wanneer er geen capaciteit meer is in het magazijn: werk kan worden gemaakt zonder dat er locaties worden gedefinieerd of het werkaanmaakproces mislukt. Het resultaat wordt gedefinieerd door de instellingen op de pagina **Fouten bij locatie-instructie**, waar u kunt kiezen om de optie **Werk stoppen bij fout van locatie-instructie** voor elk type werkorder te selecteren.

## <a name="next-step"></a>Volgende stap

Nadat u locatie-instructies hebt gemaakt, kunt u elke instructiecode aan een werksjablooncode voor het maken van werk koppelen. Zie voor meer informatie [Magazijnwerk beheren met werksjablonen en locatie-instructies](https://docs.microsoft.com/dynamics365/supply-chain/warehousing/control-warehouse-location-directives).

## <a name="additional-resources"></a>Aanvullende bronnen

- Video: [Configuratie van magazijnbeheer: diepgravend](https://community.dynamics.com/365/b/techtalks/posts/warehouse-management-configuration-deep-dive-october-14-2020)
- Help-onderwerp: [Magazijnwerk beheren met werksjablonen en locatierichtlijnen](control-warehouse-location-directives.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]