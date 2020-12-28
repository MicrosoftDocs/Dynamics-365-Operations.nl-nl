---
title: Wizard voor instellen van hoofdplanning
description: Dit onderwerp beschrijft diverse belangrijke strategieën en parameters die worden gebruikt voor het instellen van de hoofdplanning.
author: t-benebo
manager: tfehr
ms.date: 10/21/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2019-05-31
ms.dyn365.ops.version: AX 10.0.0
ms.openlocfilehash: b38009cbfdd5444c6643c5c0159a1aa475aaa3ac
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/13/2020
ms.locfileid: "4425573"
---
# <a name="master-planning-setup-wizard"></a>Wizard voor instellen van hoofdplanning

[!include [banner](../includes/banner.md)]

Dit onderwerp bevat een handleiding voor de **wizard Hoofdplanning instellen**. Hierin wordt uitgelegd hoe parametersuggesties worden berekend en bevat ook voorbeelden die laten zien hoe verschillende bedrijven de hoofdplanning instellen op basis van hun bedrijfsbehoeften.

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE3YnSB]

De video [Wizard voor instellen van hoofdplanning in Dynamics 365 Supply Chain Management](https://youtu.be/c-e6n-8rZb4) (zie hierboven) is opgenomen in de [Finance and Operations-afspeellijst](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) die beschikbaar is op YouTube.


## <a name="specific-requirements-of-your-company"></a>Specifieke eisen van uw bedrijf

Op de eerste pagina van de wizard wordt gevraagd naar de specifieke vereisten van uw bedrijf. Uw antwoorden op deze vragen hoeven niet exact te zijn, maar u moet wel in staat zijn een ruwe schatting te geven van het aantal items en geplande orders dat er voor de rechtspersoon zal zijn. Uw antwoorden worden gebruikt om parameters te configureren die van toepassing zijn op uw rechtspersoon, niet alleen op het hoofdplan dat u hebt geselecteerd. De volgende secties beschrijven de parameters die worden berekend en de formules die worden gebruikt.

### <a name="number-of-threads"></a>Aantal threads

- **Als u (een van) de volgende artikelen produceert:** Aantal threads = aantal geplande orders ÷ 1000
- **Als u geen van de volgende artikelen produceert:** Aantal threads = aantal artikelen ÷ 1000

Als het aantal threads dat wordt berekend groter is dan 75 procent van het beschikbare aantal threads, wordt deze beperkt tot 75 procent van het aantal threads dat beschikbaar is voor elke klant. (Het aantal beschikbare threads wordt voor elke klant bepaald.)

Zie [Aantal threads](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/master-planning/master-planning-performance#number-of-threads) voor meer informatie.

### <a name="bundle-size"></a>Bundelgrootte

De bundelgrootte wordt ingesteld op **1**. Deze waarde is vaak de beste, omdat de prestaties van de Hoofdplanning hierdoor mede worden verbeterd.

Zie [Aantal taken in de taakbundel van de helper](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/master-planning/master-planning-performance#number-of-tasks-in-helper-task-bundle) voor meer informatie.

### <a name="firming-bundle-size"></a>Grootte van fiatteringsbundel

- **Als u (een van) de volgende artikelen produceert:** de grootte van de fiatteringsbundel wordt ingesteld op de grootste van deze twee waarden: **10** of de bundelberekening
- **Als u geen van de volgende artikelen produceert:** de grootte van de fiatteringsbundel wordt ingesteld op de grootste van deze twee waarden: **50** of de bundelberekening

Bundelberekening = (aantal geplande orders × (timefence voor fiattering ÷ timefence voor behoefteplanning) ÷ aantal threads) ÷ 10

### <a name="cache-size"></a>Cachegrootte

De cachegrootte wordt ingesteld op **Maximum**. Deze waarde is vaak de beste, omdat de prestaties van de Hoofdplanning hierdoor mede worden verbeterd.

Zie [Tijd toewijzen aan taken in een takenbundel](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/production-control/allocate-time-jobs-job-bundle) voor meer informatie.

### <a name="manufacturing-setup"></a>Productie-instellingen

Als u artikelen produceert, wordt later in de wizard een pagina **Productie-instellingen** weergegeven.

## <a name="scope-of-the-current-plan"></a>Bereik van het huidige plan

Op de pagina **Bereik van de huidige plan** van de wizard beantwoordt u vragen die betrekking hebben op hoe ver in de toekomst verschillende behoeften worden meegenomen en berekend in de Hoofdplanning. Bij elke vraag wordt gevraagd of u een functie wilt gebruiken en hoe u deze wilt configureren.

Voor de prognoseplanfunctie vraagt de wizard bijvoorbeeld of u een prognoseplan wilt gebruiken in de Hoofdplanning, zodat er geplande orders worden voorgesteld om aan de voorspelde vraag te voldoen?

De volgende opties zijn beschikbaar:

- **Nee** – de Hoofdplanning zal geen geplande orders voorstellen om een prognose te vervullen. Op het tabblad **Timefences** van de pagina **Hoofdplannen** (**Hoofdplanning \> Instellen \> Plannen \> Hoofdplannen**), stelt de wizard de optie **Prognoseplan (timefence)** in op **Ja** en het aantal dagen op **0** (nul). Deze instelling overschrijft de timefence die is opgegeven in de behoefteplanningsgroep. Omdat het aantal dagen is ingesteld op **0** (nul), wordt de functie niet gebruikt.
- **Ja, zoals gedefinieerd in dit hoofdplan** – er wordt een veld beschikbaar, waarin u het aantal dagen kunt invoeren dat de Hoofdplanning geplande orders zal voorstellen om aan de voorspelde vraag te voldoen. De wizard stelt de optie **Prognoseplan (timefence)** in op **Ja** en het aantal dagen op het aantal dagen dat is ingevoerd in het veld **Prognoseplan** op het tabblad **Timefences** van de pagina **Hoofdplannen**. Deze instelling overschrijft de waarden die zijn ingesteld bij de behoefteplanningsgroepen.
- **Ja, zoals gedefinieerd in de behoefteplanning** – de wizard stelt de optie **Prognoseplan (timefence)** in op **Nee**. De timefences die in de behoefteplanningsgroep zijn opgegeven, worden gebruikt om aan te geven hoe lang u de prognose wilt plannen.

De resterende vragen op deze pagina en hun antwoorden volgen hetzelfde schema:

- **Nee** – de optie **Prognoseplan (timefence)** wordt ingesteld op **Ja** en het aantal dagen wordt ingesteld op **0** (nul).
- **Ja, zoals gedefinieerd in deze hoofdplanning** – de wizard stelt de optie **Prognoseplan (timefence)** in op **Ja**. Het aantal dagen dat u invoert, wordt gebruikt en overschrijft de waarden die zijn ingesteld bij de behoefteplanningsgroepen.
- **Ja, zoals gedefinieerd in de behoefteplanningsgroep** – de wizard stelt de optie **Prognoseplan (timefence)** in op **Nee**.

Zie [Taakplanning](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/production-control/job-scheduling) voor meer informatie.

## <a name="scheduling-options"></a>Planningsopties

De pagina **Planningsopties** wordt alleen weergegeven als u **Ja** hebt geantwoord op de vraag 'Produceert u (een van) de geplande artikelen?' op de eerste pagina van de wizard.

Uw antwoord op de eerste vraag op deze pagina ('Wilt u bewerkingen plannen die zijn onderverdeeld in afzonderlijke taken?') bepaalt de planningsmethode op het tabblad **Algemeen** van de pagina **Hoofdplannen**.

- **Ja** – Taakplanning wordt gebruikt.
- **Nee** – Bewerkingsplanning wordt gebruikt.

Zie [Bewerkingsplanning](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/production-control/operations-scheduling) en [Taakplanning](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/production-control/job-scheduling) voor meer informatie.

## <a name="updates-of-demand-and-supply"></a>Updates van vraag en aanbod

De vragen op de pagina **Updates van vraag en aanbod** zijn gerelateerd aan fiattering, actieberichten en vertragingen.

De configuratie van de Hoofdplanning wordt bijgewerkt op basis van uw antwoorden, volgens hetzelfde schema dat in de vorige sectie is beschreven:

- **Nee** – de optie **Timefence** op de pagina **Hoofdplannen** wordt ingesteld op **Ja** en het aantal dagen wordt ingesteld op **0** (nul).
- **Ja, zoals gedefinieerd in deze Hoofdplanning** – de optie **Timefence** wordt ingesteld op **Ja**. Het aantal dagen dat u invoert, wordt gebruikt en overschrijft de waarden die zijn ingesteld bij de behoefteplanningsgroepen.
- **Ja, zoals gedefinieerd in de behoefteplanningsgroep** – de optie **Timefence** wordt ingesteld op **Nee**.

Voor berekende vertragingen worden met uw antwoorden op de vragen in de wizard de corresponderende parameters bijgewerkt op het tabblad **Berekende vertragingen** van de pagina **Hoofdplannen**.

## <a name="summary-of-your-changes"></a>Overzicht van uw wijzigingen

Op de laatste pagina van de wizard worden de wijzigingen weergegeven die op basis van uw antwoorden worden aanbevolen. Het toont zowel de waarde in uw instellingen (**Huidige instellingen**) en de waarde die de wizard aanbeveelt (**Nieuwe configuratie**).

U kunt ook de parameters in de nieuwe configuratie wijzigen. De parameters worden gescheiden in parameters die van toepassing zijn op uw rechtspersoon en parameters die alleen van toepassing zijn op het hoofdplan dat u hebt geselecteerd. Als u alle instellingsparameters wilt weergeven die kunnen worden gewijzigd met de wizard, selecteert u **Alle parameters weergeven** onder aan de pagina. U kunt dan de parameters wijzigen.

Tot slot, wanneer u **Voltooien** selecteert, wordt de nieuwe configuratie toegepast. Als u **Annuleren** selecteert, worden geen wijzigingen toegepast.

## <a name="examples"></a>Voorbeelden

In deze sectie worden de instellingen van twee fictieve bedrijven beschreven om te laten zien hoe de instellingen kunnen wijzigen op basis van de behoeften van elk bedrijf.

### <a name="example-1-contoso-manufacturer"></a>Voorbeeld 1: Contoso Manufacturer

Contoso Manufacturer is een productiebedrijf dat luidsprekers maakt. Het koopt de verschillende grondstoffen en componenten die voor de eindproducten (luidsprekers) worden gebruikt van verschillende leveranciers. Hier zijn enkele kenmerken van zijn toelevering en productie:

- De eindproducten die door het bedrijf worden gemaakt, hebben een stuklijststructuur.
- Alle eindproducten en onderdelen worden gepland op grond van de Hoofdplanning. Er wordt geen handmatige planning uitgevoerd.
- Er wordt een traject van bewerkingen gedefinieerd voor de fabricage van elk eindproduct.
- De eindproducten worden op de fabriek gemaakt. Het bedrijf heeft een bepaald aantal frees- en boormachines gedefinieerd dat wordt gebruikt om de componenten te verwerken. De verschillende componenten moeten door deze machines worden verwerkt.
- Er zijn veel leveranciers. De gemiddelde doorlooptijd voor producten is één week. Een groep producten van dezelfde leverancier krijgt een doorlooptijd van zeven weken.

In de wizard worden de volgende waarden ingevoerd voor Contoso Manufacturer:

- **Behoefteplanning:**

    - **Vraag:** 'Wilt u het aantal dagen van uw planningshorizon opgeven?'
    - **Antwoord:** 'Ja, zoals gedefinieerd in de behoefteplanningsgroepen.'

    Omdat de doorlooptijd voor artikelen heel verschillend is, hoeft Contoso niet alle artikelen voor dezelfde periode in de toekomst te plannen. Er worden behoefteplanningsgroepen voor de artikelen gemaakt. Artikelen met een vergelijkbare doorlooptijd worden toegewezen aan dezelfde behoefteplanningsgroep. De planningshorizon voor elke behoefteplanningsgroep (de timefence voor behoefteplanning) is ongeveer de doorlooptijd plus een marge van één week. De Hoofdplanning zorgt er vervolgens voor dat de artikelen vooraf worden gepland, op basis van hun doorlooptijd.

    Daarom worden er twee behoefteplanningsgroepen gemaakt voor dit voorbeeld. Een behoefteplanningsgroep heeft een timefence voor behoefteplanning van twee weken en de andere heeft een timefence voor behoefteplanning van acht weken.

    Als **Ja, zoals gedefinieerd in dit hoofdplan** als antwoord is geselecteerd, moet het aantal dagen dat wordt ingevoerd meer zijn dan de langste doorlooptijd van alle artikelen. Omdat veel artikelen echter niet zo ver van tevoren hoeven te worden gepland, worden veel geplande orders berekend maar nooit gebruikt. Daarom neemt de runtime van de hoofdplanning toe.

- **Planning:**

    - **Vraag:** 'Moet u bewerkingen plannen die zijn onderverdeeld in afzonderlijke taken?'
    - **Antwoord:** 'Ja'.

    Contoso Manufacturer moet de afzonderlijke taken die worden uitgevoerd op de werkvloer plannen. Daarom wordt Taakplanning gebruikt.

- **Capaciteit:**

    - **Vraag:** 'Wilt u plannen met behulp van de capaciteit van resources?'
    - **Antwoord:** 'Ja, zoals gedefinieerd in dit hoofdplan.' **10 dagen** wordt ingevoerd.

    Het aantal frees- en boormachines is beperkt. De productieplanning moet rekening houden met deze beperking en de taken in de tijd regelen op basis van de capaciteit van de resources. Met andere woorden, de taken die zijn gepland, worden opnieuw gepland op basis van de beperkingen van de resources. Voor de planning wordt naast de gedefinieerde periode de doorlooptijd gebruikt. (Geplande productieorders kunnen elkaar overlappen.) Omdat de productielevertijd voor de artikelen zeven dagen is, wordt de capaciteit van de resources voor de Hoofdplanning gedurende tien dagen meegenomen.

- **Sequentiëren:**

    - **Vraag:** 'Wilt u de volgorde van geplande orders bepalen met behulp van de sequentiewaarden van het product?'
    - **Antwoord:** 'Ja, zoals gedefinieerd in de behoefteplanningsgroepen.'

    Er wordt een traject gedefinieerd voor de fabricage van elk eindproduct. Daarom zal de Hoofdplanning de orders op tijd plannen volgens de gedefinieerde trajecten.

- **Explosie:**

    - **Vraag:** 'Wilt u orders plannen voor alle elementen in een stuklijst (plan voor de bovenliggende en alle onderliggende items)?"
    - **Antwoord:** 'Ja, zoals gedefinieerd in de behoefteplanningsgroepen.'

    Alle artikelen die voor de productie worden gebruikt, moeten worden gepland. Omdat de artikelen zeer verschillende doorlooptijden hebben, levert de Hoofdplanning betere resultaten op wanneer behoefteplanningsgroepen worden gebruikt. Nogmaals, een marge van één week kan worden ingevoerd en explosie kan worden gedaan voor dezelfde tijd als de behoefteplanning.

### <a name="example-2-contoso-retailer"></a>Voorbeeld 2: Contoso Retailer

Contoso Retailer is een distributiebedrijf in de modebranche. De Hoofdplanning wordt gebruikt om te berekenen wanneer inkooporders moeten worden geplaatst, op basis van de voorspelde verkoop. Hier zijn enkele van de kenmerken:

- Contoso Retailer maakt gebruik van een vraagprognose om de verkoop te voorspellen. Inkooporders worden gepland op basis van de prognose.
- Winkels gebruiken bestelopdrachten voor aanvulling.
- De doorlooptijd van het hoofdmagazijn naar elke winkel is ongeveer twee weken voor alle artikelen.

In de wizard worden de volgende waarden ingevoerd voor Contoso Retailer:

- **Vraagprognose:**

    - **Vraag:** 'Wilt u een prognoseplan gebruiken in de Hoofdplanning, zodat er geplande orders worden voorgesteld om aan de voorspelde vraag te voldoen?'
    - **Antwoord:** 'Ja, zoals gedefinieerd in dit hoofdplan.'

    Contoso heeft een vraagprognose opgenomen om de verkoop te voorspellen. Daarom moet de Hoofdplanning geplande orders aanbevelen om aan de prognose te voldoen.

- **Fiattering:**

    - **Vraag:** 'Wilt u dat de Hoofdplanning automatisch geplande orders fiatteert in orderdocumenten, bijvoorbeeld productie- of inkooporders?"
    - **Antwoord:** 'Ja, zoals gedefinieerd in dit hoofdplan.' **1 dag** wordt ingevoerd.

    Omdat Contoso Retailer inkooporders rechtstreeks vanuit de geplande inkooporders maakt, is het handig als de geplande inkooporders automatisch worden gefiatteerd. Omdat het bedrijf elke dag een Hoofdplanning uitvoert, worden alle orders die voor de volgende dag nodig zijn, automatisch gefiatteerd door een timefence voor fiattering van één dag.

- **Goedgekeurde bestelopdrachten:**

    - **Vraag:** 'Wilt u de vraag van goedgekeurde opdrachten opnemen om winkels aan te vullen?'
    - **Antwoord:** 'Ja, zoals gedefinieerd in dit hoofdplan.' **1 dag** wordt ingevoerd.

    Contoso gebruikt de goedgekeurde bestelopdrachten van de winkels om geplande inkooporders te maken om deze winkels aan te vullen. Omdat de Hoofdplanning elke dag wordt uitgevoerd, worden de bestelopdrachten van de laatste dag opgenomen in de planning.
