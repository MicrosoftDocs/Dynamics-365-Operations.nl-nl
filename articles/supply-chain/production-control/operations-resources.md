---
title: Operations-resources
description: Bronnen voor bedrijfsactiviteiten voeren de activiteiten van een project of een productieproces uit. Ze kunnen van verschillende typen zijn en kunnen verschillende capaciteiten hebben.
author: sorenva
manager: AnnBe
ms.date: 11/03/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WrkCtrCapability
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 61943
ms.assetid: a3847f07-fca4-4140-a26f-d83c6ac68dde
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: c4018632e5e20470948ee59e4bb2a1cab905d829
ms.contentlocale: nl-nl
ms.lasthandoff: 11/03/2017

---

# <a name="operations-resources"></a>Operations-resources

[!include[banner](../includes/banner.md)]


Bronnen voor bedrijfsactiviteiten voeren de activiteiten van een project of een productieproces uit. Ze kunnen van verschillende typen zijn en kunnen verschillende capaciteiten hebben. 

<a name="operations-resources"></a>Operations-resources
--------------------

Bronnen voor bedrijfsactiviteiten zijn de machines, de hulpmiddelen, werknemers, faciliteiten, fysieke gebieden of leveranciers die de activiteiten van een project of een productieproces uitvoeren. Ze kunnen van verschillende typen zijn en kunnen verschillende capaciteiten hebben.

-   **Leverancier** – Een externe bron die projectactiviteiten of productiebewerkingen uitvoert. Een voorbeeld is een onderaannemer. Door leveranciersbronnen aan een leveranciersrekening te koppelen, kunt u inkooporders voor onderaannemers genereren op basis van stuklijst- of productieregels.
-   **Human Resources** - Een project- of productiemedewerker die een activiteit uitvoert, ofwel alleen of als operator van een machine of een stuk gereedschap. Als u de functionaliteit Human Resources gebruikt, kunt u human resources aan een werknemer koppelen. De planningsengine kan de resources vervolgens toewijzen, op basis van de competenties die voor de bijbehorende werknemer zijn gedefinieerd.
-   **Machine** - Een machine of andere productieapparatuur die in de productie is vereist.
-   **Hulpmiddel** - Een instrument of een apparaat dat meestal samen met een andere bron worden gebruikt om een activiteit in een project of in productie uit te voeren.
-   **Locatie** - Een fysieke locatie van een bepaalde grootte die nodig is om een activiteit uit te voeren. Een voorbeeld is een assemblagegebied.
-   **Faciliteit** - Een gebouw of een vaste structuur die nodig is om een activiteit uit te voeren.

## <a name="calendars"></a>Kalenders
Een kalender kan aan een bron voor bedrijfsactiviteiten worden toegewezen en beschrijft de capaciteit (in uren) van die bron. De werktijden van de bron voor bedrijfsactiviteiten worden bepaald door de kalender die aan de resourcegroep is toegewezen waarvan de bron voor bedrijfsactiviteiten deel uitmaakt. U kunt een begin- en vervaldatum voor de toegewezen kalender instellen. U kunt dan meer dan een kalender aan een bron voor bedrijfsactiviteiten toewijzen. De datums van de toegewezen kalenders kunnen echter niet overlappen, en de bron voor bedrijfsactiviteiten kan slechts aan één kalender tegelijk toegewezen worden. **Opmerking:** Als er geen geldige werkkalenders zijn voor een resourcegroep (bijvoorbeeld als de laatste toegewezen kalender of de enige toegewezen kalender is vervallen), hebt u niet langer toegang tot de bronnen voor bedrijfsactiviteiten die aan de resourcegroep zijn toegewezen voor productieplanning en bewerkingsplanning. U kunt een kalender ook aan een resourcegroep toewijzen om de werktijden op te geven voor zowel de resourcegroep als alle bronnen voor bedrijfsactiviteiten die aan de resourcegroep zijn toegewezen. De capaciteit van de resourcegroep wordt berekend als de som van capaciteiten van elke bron voor bedrijfsactiviteiten die aan de resourcegroep is toegewezen. De kalender die aan een resourcegroep is toegewezen, kan in de loop der tijd veranderen.

## <a name="resource-capabilities"></a>Bronmogelijkheden
Een capaciteit (mogelijkheid) is het vermogen van een bron voor bedrijfsactiviteiten om een bepaalde activiteit uit te voeren. U kunt een of meer capaciteiten aan een bron voor bedrijfsactiviteiten toewijzen. De planningsengine wijst vervolgens bronnen toe door de bronbehoeften van elke activiteit te vergelijken met de mogelijkheden van de beschikbare bronnen voor bedrijfsactiviteiten. Capaciteiten kunnen aan allerlei soorten bronnen voor bedrijfsactiviteiten worden toegewezen (**Hulpmiddel**, **Leverancier**, **Machine**, **Human resources**, **Locatie** of **Faciliteit**). Als u capaciteiten aan bronnen voor bedrijfsactiviteiten wilt toewijzen voor een bepaalde tijd, definieert u een begindatum en een vervaldatum voor de toewijzing van de capaciteit. Zie [Bronmogelijkheden](resource-capabilities.md) voor meer informatie.

## <a name="resource-groups"></a>Resourcegroepen
Een resourcegroep is een set van bronnen voor bedrijfsactiviteiten die de gedetailleerdheid vertegenwoordigt waarmee u bronnen wilt plannen wanneer u de planningsmethode voor bewerkingen gebruikt. Een resourcegroep correspondeert daarom meestal met de fysieke organisatie van werkcellen, die is gedefinieerd door gele lijnen op de werkvloer van de productie. De resourcegroep definieert de locatie, productie-eenheid en magazijncontext voor bronnen voor bedrijfsactiviteiten die toegewezen worden aan de groep. Wanneer u een bron voor bedrijfsactiviteiten toewijst aan een resourcegroep, kan de bron worden gepland op de locatie waar de resourcegroep zich bevindt. U hoeft de bronnen voor bedrijfsactiviteiten die u voor een resourcegroep maakt niet toewijzen. Een bron voor bedrijfsactiviteiten moet echter wel aan een resourcegroep worden toegewezen voordat deze voor de uitvoering van werk kan worden gepland. Een bron voor bedrijfsactiviteiten kan voor een beperkte tijd aan een resourcegroep worden toegewezen. U kunt een bron voor bedrijfsactiviteiten ook aan meerdere resourcegroepen toewijzen, zodat u de bronnen vervolgens tussen locaties kunt delen. De ingangsdatums en vervaldatums kunnen elkaar echter niet overlappen. U kunt met andere woorden geen bron voor bedrijfsactiviteiten aan twee resourcegroepen tegelijk toewijzen. De wijzigingen in resourcegroeptoewijzingen zijn alleen geldig voor nieuwe resourcetoewijzingen. Capaciteitsreserveringen voor taken, bewerkingen en projectuurprognoses die al zijn gepland worden niet beïnvloed. **Notitie:** Als u bronnen voor bedrijfsactiviteiten van het type **Leverancier** toewijst aan een resourcegroep, moeten alle bronnen voor bedrijfsactiviteiten die aan die resourcegroep zijn toegewezen van het type **Leverancier** zijn en moeten ze aan dezelfde leveranciersrekening zijn gekoppeld.

## <a name="production-units"></a>Productie-eenheden
Een productie-eenheid is een administratieve eenheid waarin een verzameling groepen van bronnen zijn gegroepeerd. Een productie-eenheid kan meerdere groepen van bronnen bevatten, maar een groep van bronnen kan alleen zijn gekoppeld met één productie-eenheid. Een productie-eenheid is de fysieke indeling van productiebronnen en heeft geen effect op transacties of de manier waarop deze worden verwerkt. U moet een productie-eenheid aan een site te koppelen. U kunt ook een orderverzamelmagazijn en een opslagmagazijn toewijzen aan een productie-eenheid. U kunt een productie-eenheid gebruiken om productiegerelateerde gegevens samen te voegen en te filteren. Een werkvloermanager kan bijvoorbeeld een handig overzicht weergeven van de uitstaande werkbelasting en van de beschikbare capaciteit voor een bepaalde productie-eenheid. U kunt de productie-eenheid wijzigen die aan een groep van bronnen is toegewezen. U kunt een productie-eenheid ook verwijderen. Deze wijzigingen in de productie-eenheid zijn echter alleen nuttig voor nieuwe orders die zijn gemaakt nadat de hoofdplanning is uitgevoerd. Als u de productie-eenheidwijziging wilt toepassen op bestaande orders, moet u dit handmatig doen.

## <a name="resource-scheduling"></a>Resourceplanning
Bronnen voor bedrijfsactiviteiten worden toegewezen aan activiteiten wanneer een project of een productie wordt gepland. Er zijn twee planningsmethoden beschikbaar: planning van bewerkingen en taakplanning. Als u bewerkingsplanning gebruikt, wordt elke bewerking of projectactiviteit gepland voor de resourcegroep die bronnen voor bedrijfsactiviteiten bevat die aan de bronbehoeften voldoen die voor de bewerking zijn opgegeven. Als een specifieke bron voor bedrijfsactiviteiten voor de bewerking is vereist, reserveert de planning alleen capaciteit voor een specifieke bron voor bedrijfsactiviteiten in de groep. Taakplanning is een meer gedetailleerde vorm van planning dan bewerkingsplanning. Elke bewerking wordt onderverdeeld in de afzonderlijke taken. Deze taken worden vervolgens toegewezen de bronnen voor bedrijfsactiviteiten die deze zullen uitvoeren. Planning reserveert capaciteit voor de resourcegroepen op basis van de bewerkingstijden die voor de productieroute of projectactiviteiten zijn gedefinieerd. Als u met een beperkte capaciteit werkt, hangt de planning af van de beschikbaarheid van de bronnen voor bedrijfsactiviteiten die nodig zijn om de activiteit te voltooien. Voor planning van bewerkingen is de capaciteit van de resourcegroep de som van de beschikbare capaciteit van de bronnen voor bedrijfsactiviteiten die deel uitmaken van die groep. Capaciteitsreserveringen die al voor de bronnen van bedrijfsactiviteiten bestaan worden beschouwd als capaciteit die niet beschikbaar is. Indien de beschikbare capaciteit ontoereikend is voor de productie, kunnen de productieorders worden uitgesteld of zelfs gestopt. U kunt op de pagina **Resources** verschillende eigenschappen definiëren die bepalen hoe de capaciteitsreserveringen worden gemaakt:

-   **Capaciteit** - Geef de capaciteit van de bron voor bedrijfsactiviteiten per uur in termen van de capaciteitseenheid op.
-   **Batchcapaciteit** – Geef het maximum aantal stuks op dat de bron voor bedrijfsactiviteiten kan verwerken per uitvoering.
-   **Efficiëntiepercentage** – Geef de efficiëntie op die u van de bron voor bedrijfsactiviteiten verwacht. Het efficiëntiepercentage past de doorvoercapaciteit van de bron voor bedrijfsactiviteiten aan en beïnvloedt de tijd die voor de bron is gereserveerd. De doorlooptijden voor de bewerkingen die de bron voor bedrijfsactiviteiten gebruiken worden overeenkomstig aangepast. De berekening gebruikt deze formule: Planningstijd = Tijd × 100 ÷ Efficiëntiepercentage. In deze formule omvat *Tijd* zowel de uitvoerings- als insteltijd.
-   **Percentage bewerkingsplanning** – Geef het maximumpercentage van de capaciteit van de bron voor bedrijfsactiviteiten op die u in bewerkingsplanning wilt gebruiken. Dit percentage moet minder dan 100 procent zijn voor flexibiliteit in de capaciteit bij het plannen van taken.
-   **Eindige capaciteit** – Stel deze optie in op **Ja** als de bron voor bedrijfsactiviteiten moet worden gepland op basis van de werkelijke capaciteit die beschikbaar is, en als de bestaande capaciteitsreserveringen in aanmerking moeten worden genomen. Als deze optie is ingesteld op **Nee**, wordt aangenomen dat de bron voor bedrijfsactiviteiten oneindige capaciteit heeft, en kan bron worden overboekt.
-   **Beperking** - Stel deze optie in op **Ja** als u wilt dat de bron voor bedrijfsactiviteiten wordt gepland op basis van de werkelijke capaciteit die met betrekking tot de vereiste werktijdplanningseigenschappen beschikbaar is.
-   **Exclusief** – Stel deze optie in op **Ja** als u niet wilt dat de bron voor bedrijfsactiviteiten voor een andere taak of andere bewerking beschikbaar is zolang de huidige productie niet voltooid is. In dit geval kan de bron voor bedrijfsactiviteiten niet worden gebruikt, zelfs niet als er gaten vallen in de uitvoeringstijd van de bron.
-   **Bottleneck resource** - Definieer de bron voor bedrijfsactiviteiten als een knelpuntbron. Een knelpuntbron wordt gepland door eindige capaciteit te gebruiken wanneer de opties **Eindige capaciteit** en **Planning knelpunt** op de pagina **Hoofdplannen** worden geselecteerd.

Om meerdere bronnen voor bedrijfsactiviteiten tegelijk te plannen, om bijvoorbeeld een bewerking in productie uit te voeren, moet u de vereisten voor de diverse bronnen opgeven door primaire en secundaire bewerkingen te gebruiken. U kunt dan ook meerdere bronnen voor bedrijfsactiviteiten reserveren die verschillende capaciteiten hebben. De bronnen voor bedrijfsactiviteiten die voor de primaire bewerking worden gepland, bepalen de duur van de activiteit.

## <a name="lean-work-cells"></a>Lean werkcellen
U kunt opgeven dat een resourcegroep een lean werkcel is. De resourcegroep kan dan deel uitmaken van een productiestroom. Door een resourcegroep als een lean werkcel op te geven, voorkomt u ook dat de resourcegroep en de toegewezen bronnen voor bedrijfsactiviteiten aan de bewerkingen van een productieorder of een projecturenprognose worden toegewezen. Voor elke resourcegroep die als lean werkcel fungeert, moet u de volgende gegevens opgeven:

-   **Kalender** - De werkkalender van de werkcel, die de eigenschap van een standaardwerkdag moet hebben.
-   **Invoermagazijn en - locatie** - De standaardlocatie die wordt gebruikt om materiaal voor een activiteit te verzamelen.
-   **Uitvoermagazijn en - locatie** De standaardlocatie waar uitvoer van de werkcel wordt geplaatst.
-   **Kostencategorie voor uitvoering** - Deze categorie moet voor de werkcel zijn gedefinieerd als de directe arbeidskosten in kostprijsberekening worden bijgehouden.

Wanneer een resourcegroep als lean werkcel wordt gebruikt, wordt de capaciteit van de werkcel direct op de resourcegroep opgegeven. U hoeft daarom geen bronnen voor bedrijfsactiviteiten aan de resourcegroep toe te wijzen. Alleen als de werkcel door een onderaannemer wordt beheerd, moet een bron voor bedrijfsactiviteiten van het type **Leverancier** aan de werkcel worden toegewezen. Als u een bron voor bedrijfsactiviteiten toewijst aan een resourcegroep die als werkcel is gemarkeerd, wordt de capaciteit van de werkcel niet beïnvloed.

## <a name="costing-resources"></a>Kostprijsberekeningsresources
Wanneer u een activiteit zoals een routebewerking of een projecturenprognose definieert, kunt u de behoefte voor een specifieke bron voor bedrijfsactiviteiten of resourcegroep opgeven. U kunt ook de behoefte voor een bron voor bedrijfsactiviteiten van een specifiek type opgeven, of een bron voor bedrijfsactiviteiten die een specifieke mogelijkheid of competentie heeft. Om deze reden wordt de werkelijke brontoewijzing pas gemaakt als de activiteit is gepland en de capaciteit is gereserveerd. Daarom kunt u op een routebewerking opgeven dat de raming en de stuklijstberekening op een bepaalde bron voor bedrijfsactiviteiten moet worden gebaseerd. Deze bron voor bedrijfsactiviteiten wordt de kostprijsberekeningsbron genoemd. U kunt kostencategorieën en bewerkingstijden ook van de kostprijsberekeningsbron naar de activiteit overbrengen. Wanneer de bewerking is gepland, vinden schatting en stuklijstberekening plaats door de bron voor bedrijfsactiviteiten te gebruiken die werkelijk is gepland.




