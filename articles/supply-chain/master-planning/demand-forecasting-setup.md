---
title: Instelling van vraagprognose
description: In dit onderwerp worden de insteltaken beschreven die u moet uitvoeren ter voorbereiding op de vraagprognose.
author: t-benebo
ms.date: 11/23/2021
ms.topic: article
ms.search.form: ReqDemPlanDefaultAlgorithmParameters, ReqDemPlanForecastParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c3b52b970a8040dcba5a1fc59d297dc9ce1a3c53
ms.sourcegitcommit: ad1afc6893a8dc32d1363395666b0fe1d50e983a
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/23/2022
ms.locfileid: "8470004"
---
# <a name="demand-forecasting-setup"></a>Instelling van Vraagprognose

[!include [banner](../includes/banner.md)]

In dit onderwerp wordt beschreven hoe u vraagprognose instelt.  

## <a name="item-allocation-keys"></a>Artikeltoewijzingssleutels

Met artikeltoewijzingssleutels kunt u groepen artikelen maken. Een vraagprognose wordt alleen berekend voor een artikel en de dimensies ervan als het artikel onderdeel uitmaakt van een artikeltoewijzingssleutel. Deze regel wordt afgedwongen om grote aantallen artikelen te groeperen, zodat vraagprognoses sneller kunnen worden gemaakt. Prognoses worden gemaakt op basis van alleen historische gegevens.

Een artikel en de dimensies ervan moeten onderdeel zijn van slechts één artikeltoewijzingssleutel als de artikeltoewijzingssleutel wordt gebruikt tijdens het maken van prognoses.

Volg deze stappen om artikeltoewijzingssleutels te maken en hieraan een SKU (voorraadeenheid) toe te voegen.

1. Ga naar **Hoofdplanning \> Instellen \> Vraagprognose \> Artikeltoewijzingssleutels**.
1. Selecteer een artikeltoewijzingssleutel in het lijstvenster of selecteer **Nieuw** in het actievenster om een nieuwe sleutel te maken. Stel in de koptekst voor de nieuwe of geselecteerde sleutel de volgende velden in:

    - **Artikeltoewijzingssleutel**: geef een unieke naam voor de sleutel op.
    - **Naam**: voer een beschrijvende naam in voor de sleutel.

1. Volg een van deze stappen om artikelen aan de geselecteerde artikeltoewijzingssleutel toe te voegen of artikelen te verwijderen:

    - Gebruik de knoppen **Nieuw** en **Verwijderen** op de werkbalk op het sneltabblad **Artikeltoewijzing** om naar behoefte artikelen toe te voegen en te verwijderen. Selecteer voor elke rij het artikelnummer en wijs vervolgens de gewenste dimensiewaarden toe in de andere kolommen. Selecteer **Dimensies weergeven** op de werkbalk om de set dimensiekolommen te wijzigen die in het raster wordt weergegeven. (De waarde in de kolom **Percentage** wordt genegeerd wanneer vraagprognoses worden gegenereerd.)
    - Als u een groot aantal artikelen aan de sleutel wilt toevoegen, selecteert u **Artikelen toewijzen** in het actievenster om een pagina te openen waarop u meerdere artikelen kunt zoeken en aan de geselecteerde sleutel kunt toewijzen.

> [!IMPORTANT]
> Neem alleen relevante artikelen op in elke artikeltoewijzingssleutel. Onnodige artikelen kunnen verhoogde kosten veroorzaken wanneer u Microsoft Azure Machine Learning gebruikt.

## <a name="intercompany-planning-groups"></a>Intercompany-planningsgroepen

Vraagprognoses kunnen cross-company prognoses genereren. In Dynamics 365 Supply Chain Management worden bedrijven die samen worden gepland, gegroepeerd in dezelfde intercompany-planninggroep. Als u per bedrijf wilt opgeven welke artikeltoewijzingssleutels moeten worden gebruikt voor vraagprognose, koppelt u een artikeltoewijzingssleutel aan het lid van de intercompany-planningsgroep.

> [!IMPORTANT]
> Planningsoptimalisatie biedt op dit moment geen ondersteuning voor intercompany-planningsgroepen. Als u intercompany-planning wilt uitvoeren op basis van Planningsoptimalisatie, stelt u batchtaken voor de hoofdplanning in die hoofdplannen voor alle relevante bedrijven bevatten.

Ga als volgt te werk om de intercompany-planningsgroepen in te stellen.

1. Ga naar **Hoofdplanning \> Instellingen \> Intercompany-planningsgroepen**.
1. Selecteer een planningsgroep in het lijstvenster of selecteer **Nieuw** in het actievenster om een nieuwe groep te maken. Stel in de koptekst voor de nieuwe of geselecteerde groep de volgende velden in:

    - **Naam**: een unieke naam voor de planningsgroep.
    - **Beschrijving**: voer een korte beschrijving van de planningsgroep in.

1. Gebruik op het sneltabblad **Leden van intercompany-planningsgroep** de knoppen op de werkbalk om een rij toe te voegen voor elk bedrijf (rechtspersoon) dat deel moet uitmaken van de groep. Stel voor elke rij de volgende velden in:

    - **Rechtspersoon**: selecteer de naam van een bedrijf (rechtspersoon) dat lid is van de geselecteerde groep.
    - **Planningvolgorde**: de volgorde toewijzen waarin het bedrijf moet worden verwerkt in relatie tot andere bedrijven. Lage waarden worden eerst verwerkt. Deze volgorde kan belangrijk zijn wanneer de vraag voor het ene bedrijf invloed heeft op andere bedrijven. In deze gevallen moet het bedrijf dat de vraag levert als laatste worden verwerkt.
    - **Hoofdplan**: selecteer het hoofdplan dat moet worden geactiveerd voor het huidige bedrijf.
    - **Automatisch naar statisch plan kopiëren**: schakel dit selectievakje in om het resultaat van het plan naar het statische plan te kopiëren.
    - **Automatisch naar dynamisch plan kopiëren**: schakel dit selectievakje in om het resultaat van het plan naar het dynamische plan te kopiëren.

1. Als geen artikeltoewijzingssleutels aan leden van intercompany-planningsgroepen worden toegewezen, wordt standaard een vraagprognose berekend voor alle artikelen die worden toegewezen aan alle artikeltoewijzingssleutels vanuit alle bedrijven. Er zijn extra filteropties voor bedrijven en artikeltoewijzingssleutels beschikbaar in het dialoogvenster **Statistische basislijnprognose genereren** (**Hoofdplanning \> Prognose \> Vraagprognose \> Statistische basislijnprognose maken**). Als u artikeltoewijzingssleutels wilt toewijzen aan een bedrijf in de geselecteerde intercompany-planningsgroep, selecteert u het bedrijf en selecteert u vervolgens **Artikeltoewijzingssleutels** op de werkbalk van het sneltabblad **Intercompany-planningsgroepsleden**.

> [!IMPORTANT]
> Neem alleen relevante artikeltoewijzingssleutels op in elke intercompany-planningsgroep. Onnodige artikelen kunnen verhoogde kosten veroorzaken wanneer u Azure Machine Learning gebruikt.

## <a name="set-up-demand-forecasting-parameters"></a><a name="parameters"></a>Parameters voor vraagprognose instellen

Gebruik de pagina **Parameters voor vraagprognose** om verschillende opties in te stellen die bepalen hoe vraagprognose in het systeem werkt.

### <a name="open-the-demand-forecasting-parameters-page"></a>De pagina Parameters voor vraagprognose openen

Als u vraagprognoseparameters wilt instellen, gaat u naar **Hoofdplanning \> Instellen \> Vraagprognose \> Parameters voor vraagprognose**. Omdat vraagprognose cross-company wordt uitgevoerd, is de instelling globaal. Met andere woorden, dit geldt voor alle rechtspersonen (bedrijven).

### <a name="general-settings"></a>Algemene instellingen

Gebruik het tabblad **Algemeen** van de pagina **Parameters voor vraagprognose** om algemene instellingen te definiëren voor vraagprognose.

#### <a name="demand-forecast-unit"></a>Vraagprognose-eenheid

Vraagprognoses genereren de prognose in hoeveelheden. Daarom moet de maateenheid waarin de hoeveelheid moet worden uitgedrukt worden opgegeven in het veld **Vraagprognose-eenheid**. In dit veld geeft u de eenheid op die wordt gebruikt voor alle vraagprognoses, ongeacht de normale voorraadeenheden voor elk product. Door een consistente prognose-eenheid te gebruiken, zorgt u ervoor dat de aggregatie en percentagedistributie relevant zijn. Voor meer informatie over aggregatie en percentagedistributie zie [Handmatige correcties aanbrengen in de basislijnprognose](manual-adjustments-baseline-forecast.md)

Voor elke maateenheid die wordt gebruikt voor voorraadeenheden die worden opgenomen in de vraagprognose, moet u ervoor zorgen dat er een conversieregel voor de geselecteerde maateenheid en de algemene maateenheid van de prognose is. Als u een prognose genereert, wordt de lijst met artikelen geregistreerd die geen maateenheidsconversie hebben. Zo kunt u de instellingen eenvoudig corrigeren. Zie voor informatie over maateenheden en hoe u deze converteert [Maateenheden beheren](../pim/tasks/manage-unit-measure.md).

#### <a name="transaction-types"></a>Transactietypen

Gebruik de velden op het sneltabblad **Transactietypen** om de transactietypen te selecteren die worden gebruikt bij het genereren van de statistische basislijnprognose.

Vraagprognoses kunnen worden gebruikt voor prognoses van zowel afhankelijke als onafhankelijke vraag. Als bijvoorbeeld alleen de optie **Verkooporder** is ingesteld op *Ja* en alle artikelen die voor de vraagprognose worden beschouwd artikelen zijn die worden verkocht, berekent het systeem onafhankelijke vraag. Kritieke subcomponenten kunnen echter worden toegevoegd aan artikeltoewijzingssleutels en worden opgenomen in vraagprognoses. In dit geval, als de optie **Productieregel** is ingesteld op *Ja*, wordt een afhankelijke prognose berekend.

Via het tabblad **Artikeltoewijzingssleutels** kunt u transactietypen overschrijven voor een of meer specifieke artikeltoewijzingssleutels. Dit tabblad bevat gelijksoortige velden.

#### <a name="choose-how-to-create-the-baseline-forecast"></a>Opgeven hoe de basislijnprognose moet worden maken

Via het veld **Strategie voor aanmaken van vraagprognose** kunt u de methode selecteren die moet worden gebruikt om een basislijnprognose te maken. Er zijn drie methoden beschikbaar:

- *Kopieer over historische vraag*: maak prognoses door historische gegevens te kopiëren.
- *Azure Machine Learning Service*: gebruik een prognosemodel dat Azure Machine Learning Service gebruikt. Azure Machine Learning Service is de huidige machine learning-oplossing voor Azure. Daarom is het raadzaam deze te gebruiken als u een prognosemodel wilt gebruiken.
- *Azure Machine Learning*: gebruik een prognosemodel dat Azure Machine Learning Studio (klassiek) gebruikt. Azure Machine Learning Studio (klassiek) is afgeschaft en wordt binnenkort uit Azure verwijderd. Daarom is het raadzaam om *Azure Machine Learning Service* te selecteren als u voor het eerst vraagprognoses instelt. Als u momenteel Azure Machine Learning Studio (klassiek) gebruikt, moet u van plan zijn om zo snel mogelijk naar Azure Machine Learning Service over te schakelen.

Via het tabblad **Artikeltoewijzingssleutels** kunt u de methode voor het genereren van prognoses overschrijven voor een of meer specifieke artikeltoewijzingssleutels. Dit tabblad bevat gelijksoortige velden.

#### <a name="override-default-forecast-algorithm-parameters-globally"></a>Standaardparameters voor prognosealgoritme globaal overschrijven

Standaardparameters en -waarden voor prognosealgoritmes worden toegewezen op de pagina **Parameters voor vraagprognose** (**Hoofdplanning \> Instellingen \> Vraagprognose \> Parameters voor vraagprognose**). U kunt deze parameters echter globaal overschrijven via het sneltabblad **Parameters van prognosealgoritme** op het tabblad **Algemeen** van de pagina **Parameters voor vraagprognose**. (U kunt deze ook overschrijven voor specifieke toewijzingssleutels via het tabblad **Artikeltoewijzingssleutels** op de pagina **Parameters voor vraagprognose**.)

U kunt de knoppen **Toevoegen** en **Verwijderen** op de werkbalk gebruiken om de vereiste verzameling parameteroverschrijvingen vast te stellen. Selecteer voor elke parameter in de lijst een waarde in het veld **Naam** en geef vervolgens de juiste waarde op in het veld **Waarde**: Alle parameters die hier niet worden weergegeven, nemen hun waarden over van de instellingen op de pagina **Parameters voor vraagprognose**. Zie de sectie [Standaardparameters en -waarden voor vraagprognosemodellen](#model-parameters) voor meer informatie over het gebruik van de standaardset met parameters en het selecteren van waarden hiervoor.

### <a name="set-forecast-dimensions"></a>Prognosedimensies instellen

Een prognosedimensie geeft het detailniveau aan waarvoor de prognose is gedefinieerd. Bedrijf, site en artikeltoewijzingssleutel zijn vereiste prognosedimensies. U kunt prognoses ook genereren op het niveau van het magazijn, de voorraadstatus, de klantgroep, de klantrekening, het land/de regio, de status, het artikel en alle artikeldimensieniveaus. Gebruik het tabblad **Prognosedimensies** op de pagina **Parameters voor vraagprognose** om de set prognosedimensies te selecteren die wordt gebruikt wanneer de vraagprognose wordt gegenereerd.

U kunt op elk moment prognosedimensies toevoegen aan de lijst met dimensies die voor vraagprognoses worden gebruikt. U kunt ook eventueel prognosedimensie uit de lijst verwijderen. Handmatige correcties gaan echter verloren als u een prognosedimensie toevoegt of verwijdert.

### <a name="set-up-overrides-for-specific-item-allocation-keys"></a>Overschrijvingen instellen voor specifieke artikeltoewijzingssleutels

Niet alle artikelen werken op dezelfde manier vanuit een vraagprognoseperspectief. Daarom kunt u overschrijvingen voor specifieke toewijzingssleutels opgeven voor de meeste instellingen die zijn gedefinieerd op het tabblad **Algemeen**. De uitzondering is de vraagprognose-eenheid. Als u overschrijvingen wilt instellen voor een specifieke artikeltoewijzingssleutel, gaat u als volgt te werk.

1. Gebruik op de pagina **Parameters voor vraagprognose** op het tabblad **Artikeltoewijzingssleutels** de werkbalkknoppen om artikeltoewijzingssleutels toe te voegen aan, of desgewenst te verwijderen uit, het raster aan de linkerkant. Selecteer vervolgens de toewijzingssleutel waarvoor u overschrijvingen wilt instellen.
1. Schakel op het sneltabblad **Transactietypen** de transactietypen in die u wilt gebruiken om de statistische basislijnprognose te genereren voor producten die tot de geselecteerde toewijzingssleutel behoren. De instellingen werken net als op het tabblad **Algemeen**, maar ze zijn alleen van toepassing op de geselecteerde artikeltoewijzingssleutel. Alle instellingen hier (de waarden voor *Ja* en *Nee*) overschrijven alle instellingen voor **Transactietypen** op het tabblad **Algemeen**.
1. Selecteer op het sneltabblad **Parameters van prognosealgoritme** de overschrijvingen voor de strategie voor het aanmaken van prognoses en parameters van prognosealgoritmes voor producten die bij de geselecteerde toewijzingssleutel horen. Deze instellingen werken net als op het tabblad **Algemeen**, maar ze zijn alleen van toepassing op de geselecteerde artikeltoewijzingssleutel. U kunt de knoppen **Toevoegen** en **Verwijderen** op de werkbalk gebruiken om de vereiste verzameling parameteroverschrijvingen op te geven. Selecteer voor elke parameter in de lijst een waarde in het veld **Naam** en geef vervolgens de juiste waarde op in het veld **Waarde**: Zie de sectie [Standaardparameters en -waarden voor vraagprognosemodellen](#model-parameters) voor meer informatie over het gebruik van de standaardset met parameters en het selecteren van waarden hiervoor.

### <a name="set-up-the-connection-to-the-azure-machine-learning-service"></a>De verbinding met Azure Machine Learning Service instellen

Gebruik het tabblad **Azure Machine Learning Service** om de verbinding met Azure Machine Learning Service in te stellen. Deze oplossing is een van de opties voor het maken van de basislijnprognose. Deze instellingen op dit tabblad hebben alleen gevolgen wanneer het veld **Strategie voor aanmaken van vraagprognose** is ingesteld op *Azure Machine Learning Service*.

Zie de sectie [Azure Machine Learning Service instellen](#setup-amls) voor meer informatie over het instellen van Azure Machine Learning Service en gebruik vervolgens de instellingen hierin om verbinding met deze service te maken.

### <a name="set-up-the-connection-to-azure-machine-learning-studio-classic"></a>De verbinding met Azure Machine Learning Studio (klassiek) instellen

> [!IMPORTANT]
> Azure Machine Learning Studio (klassiek) is afgeschaft. Daardoor kunt u hiervoor geen nieuwe werkruimten meer maken in Azure. Deze service is vervangen door Azure Machine Learning Service, die vergelijkbare functies biedt en meer. Als u Azure Machine Learning nog niet gebruikt, moet u Azure Machine Learning Service gaan gebruiken. Als u al een werkruimte hebt die gemaakt is voor Azure Machine Learning Studio (klassiek), kunt u deze blijven gebruiken totdat de functie volledig uit Azure is verwijderd. Het is echter raadzaam om zo snel mogelijk bij te werken naar Azure Machine Learning Service. Hoewel de toepassing u blijft waarschuwen dat Azure Machine Learning Studio (klassiek) is afgeschaft, heeft dit geen gevolgen voor het prognoseresultaat. Zie de sectie [Azure Machine Learning Service instellen](#setup-amls) voor meer informatie over het nieuwe Azure Machine Learning Service en het instellen hiervan.
>
> U kunt vrij schakelen tussen het gebruik van de nieuwe en oude machine learning-oplossingen met Supply Chain Management zolang uw oude werkruimte van Azure Machine Learning Studio (klassiek) beschikbaar blijft.

Als u al een beschikbare werkruimte voor Azure Machine Learning Studio (klassiek) hebt, kunt u deze gebruiken om prognoses te genereren door deze met Supply Chain Management te verbinden. U kunt deze verbinding tot stand brengen via het tabblad **Azure Machine Learning** op de pagina **Parameters voor vraagprognose**. (De instellingen op dit tabblad hebben alleen effect wanneer het veld **Strategie voor aanmaken van vraagprognose** is ingesteld op *Azure Machine Learning*.) Voer de volgende gegevens in voor uw werkruimte voor Azure Machine Learning Studio (klassiek):

- Application Programming Interface (API)-sleutel voor webservice
- Eindpunt-URL webservice
- Azure-naam van opslagaccount
- Azure-sleutel van opslagaccount

> [!NOTE]
> De Azure-opslagaccountnaam en sleutel zijn alleen vereist wanneer u een aangepast opslagaccount gebruikt. Als u de on-premises versie gebruikt, moet u een aangepaste opslagaccount voor Azure hebben, zodat Machine Learning toegang heeft tot de historische gegevens.

## <a name="default-parameters-and-values-for-demand-forecasting-models"></a><a name="model-parameters"></a>Standaardparameters en -waarden voor vraagprognosemodellen

Wanneer u machine learning gebruikt om uw prognoseplanningsmodellen te genereren, bepaalt u opties voor machine learning door waarden in te stellen voor *parameters voor prognosealgoritmes*. Deze waarden worden van Supply Chain Management naar Azure Machine Learning verzonden. Gebruik de pagina **Parameters van prognosealgoritme** om te bepalen welke typen waarden moeten worden opgegeven en welke waarden dit moeten zijn.

Als u de standaardparameters en -waarden voor de vraagprognosemodellen wilt instellen, gaat u naar **Hoofdplanning \> Instellen \> Vraagprognose \> Parameters van prognosealgoritme**. Er is een standaardset met parameters beschikbaar. Elke parameter bevat de volgende velden:

- **Naam**: de naam van de parameter, zoals deze wordt gebruikt door Azure. U moet deze naam doorgaans niet wijzigen, tenzij u het experiment hebt aangepast in Azure Machine Learning.
- **Omschrijving:** een veelgebruikte naam voor de parameter. Deze naam wordt gebruikt om de parameter op andere plaatsen van het systeem te identificeren (bijvoorbeeld op de pagina **Parameters voor vraagprognose**).
- **Waarde**: de standaardwaarde voor de parameter. Welke waarde u moet invoeren, is afhankelijk van de parameter die u bewerkt. 
- **Uitleg**: een korte omschrijving van de parameter en hoe u deze gebruikt. Deze omschrijving bevat normaal gesproken advies over geldige waarden voor het veld **Waarde**.

Standaard worden de volgende parameters geleverd. (Als u deze standaardlijst ooit moet herstellen, selecteert u **Herstellen** in het actievenster.)

- **Percentage waarschijnlijkheidsniveau** - een waarschijnlijkheidsinterval bestaat uit een waardebereik dat als goede ramingen voor de vraagprognose fungeert. Een waarschijnlijkheidspercentage van 95% geeft aan dat er een kans van 5% is dat de toekomstige vraag buiten het bereik van het waarschijnlijkheidsinterval valt.
- **Gedwongen seizoensgebondenheid**: hiermee geeft u op of het model moet worden gedwongen om een bepaald type seizoensgebondenheid te gebruiken. Deze parameter geldt alleen voor ARIMA en ETS. Opties: *AUTO (standaard)*, *GEEN*, *ADDITIEF*, *MULTIPLICATIEF*.
- **Prognosemodel**: welk prognosemodel moet worden gebruikt. Opties: *ARIMA*, *ETS*, *STL*, *ETS+ARIMA*, *ETS+STL*, *ALLE*. Gebruik *ALLE* om het meest geschikte model te selecteren.
- **Maximale prognosewaarde** - hiermee geeft u de maximumwaarde op die voor voorspellingen moet worden gebruikt. Indeling: +1E[n] of numerieke constante.
- **Minimale prognosewaarde** - hiermee geeft u de minimumwaarde op die voor voorspellingen moet worden gebruikt. Indeling: -1E[n] of numerieke constante.
- **Vervanging van ontbrekende waarde** - hiermee geeft u op hoe hiaten in historische gegevens worden gevuld. Opties: *numerieke waarde*, *GEMIDDELDE*, *VORIGE*, *LINEAIR INTERPOLEREN*, *MULTINOMIAAL INTERPOLEREN*.
- **Vervangingsbereik van ontbrekende waarde** - hiermee geeft u aan of de vervanging van de waarde alleen van toepassing is op het datumbereik van elk afzonderlijk granulatiekenmerk of op de gehele gegevensset. De volgende opties zijn beschikbaar voor het bepalen van het datumbereik dat door het systeem wordt gebruikt bij het invullen van gaten in historische gegevens:

    - *GLOBAAL*: het systeem gebruikt het volledige datumbereik van alle kenmerken van de granulariteit.
    - *HISTORY_DATE_RANGE*: het systeem gebruikt een specifiek datumbereik dat wordt gedefinieerd door de velden **Begindatum** en **Einddatum** in de sectie **Historische periode** in het dialoogvenster **Statistische basislijnprognose genereren**.
    - *GRANULARITY_ATTRIBUTE*: het systeem gebruikt het datumbereik van het granulariteitskenmerk dat momenteel is verwerkt.

    > [!NOTE]
    > Een granulariteitskenmerk is een combinatie van prognosedimenssie waarmee de prognose wordt uitgevoerd. U kunt parameters voor prognosedimensies definiëren op de pagina **Parameters voor vraagprognose**.

- **Hint seizoensgebondenheid** - voor seizoensgegevens kunt u het prognosemodel een hint geven om de prognosenauwkeurigheid te verbeteren. Indeling: geheel getal dat het aantal buckets aangeeft waarvoor een vraagpatroon zichzelf herhaalt. Voer bijvoorbeeld *6* in voor gegevens die zichzelf elke zes maanden herhalen.
- **Groottepercentage van testset** - percentage van historische gegevens die kunnen worden gebruikt als een testset voor de berekening van prognosenauwkeurigheid.

U kunt de waarden voor deze parameters overschrijven door naar **Hoofdplanning \> Instellingen \> Vraagprognose \> Parameters voor vraagprognose** te gaan. Op de pagina **Parameters voor vraagprognose** kunt u de parameters op de volgende manieren overschrijven:

- Gebruik het tabblad **Algemeen** om de parameters globaal te overschrijven.
- Gebruik het tabblad **Artikeltoewijzingssleutels** om de parameters voor specifieke artikeltoewijzingssleutels te overschrijven. De parameters die voor een specifieke artikeltoewijzingssleutel worden overschreven, beïnvloeden alleen de prognose van artikelen die aan de artikeltoewijzingssleutel zijn gekoppeld.

> [!NOTE]
> Op de pagina **Parameters van prognosealgoritme** kunt u de knoppen in het actievenster gebruiken om parameters aan de lijst toe te voegen of uit de lijst te verwijderen. U moet deze aanpak doorgaans echter niet gebruiken, tenzij u het experiment hebt aangepast in Azure Machine Learning.

## <a name="set-up-the-azure-machine-learning-service"></a><a name="setup-amls"></a>Azure Machine Learning Service instellen

Supply Chain Management berekent vraagprognoses met behulp van Azure Machine Learning Service, dat u moet instellen en uitvoeren onder uw eigen Azure-abonnement. In deze sectie wordt beschreven hoe u Azure Machine Learning Service in Azure in kunt stellen en vervolgens kunt verbinden met uw Supply Chain Management-omgeving.

### <a name="enable-the-azure-machine-learning-service-in-feature-management"></a>Azure Machine Learning Service inschakelen in Functiebeheer

Voordat u Azure Machine Learning Service kunt gebruiken voor vraagprognoses, moet u een functie in Supply Chain Management inschakelen om de integratie mogelijk te maken. Beheerders kunnen gebruikmaken van de instellingen voor [functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) om de status van de functie te controleren en in te schakelen. Schakel in de werkruimte **Functiebeheer** de functie als volgt in:

- **Module:** *Hoofdplanning*
- **Functienaam:** *Azure Machine Learning Service voor vraagprognoses*

### <a name="set-up-machine-learning-in-azure"></a><a name="ml-workspace"></a>Machine learning instellen in Azure

Om Azure in staat te stellen machine learning te gebruiken om uw prognoses te verwerken, moet u voor dit doel een Azure Machine Learning-werkruimte instellen. U hebt twee opties:

- Als u de werkruimte wilt instellen door een script uit te voeren dat wordt geleverd door Microsoft, volgt u de instructies in de sectie [Optie 1: Een script uitvoeren om uw machine learning-werkruimte in te stellen](#ml-workspace-script) en ga vervolgens verder met de sectie [Verbindingsparameters voor Azure Machine Learning Service instellen in Supply Chain Management](#demand-forecast-parameters).
- Als u de werkruimte handmatig wilt instellen, volgt u de instructies in de sectie [Optie 2: Uw machine learning-werkruimte handmatig instellen](#ml-workspace-manual) en ga vervolgens verder met de sectie [Verbindingsparameters voor Azure Machine Learning Service instellen in Supply Chain Management](#demand-forecast-parameters). Deze optie kost meer tijd, maar biedt u meer controle.

#### <a name="option-1-run-a-script-to-automatically-set-up-your-machine-learning-workspace"></a><a name="ml-workspace-script"></a>Optie 1: Een script uitvoeren om uw machine learning-werkruimte automatisch in te stellen

In deze sectie wordt beschreven hoe u uw machine learning-werkruimte in kunt stellen met een geautomatiseerd script dat door Microsoft is geleverd. U kunt zo nodig alle resources handmatig instellen door de instructies in de sectie [Optie 2: Uw machine learning-werkruimte handmatig instellen](#ml-workspace-manual) te volgen. U hoeft niet beide opties te voltooien.

1. Open op GitHub de opslagplaats [Templates for Dynamics 365 Supply Chain Management demand forecasting with Azure Machine Learning](https://github.com/microsoft/Dynamics-365-Supply-Chain-Management-Demand-Forecasting-With-Azure-Machine-Learning-Service) en download de volgende bestanden:

    - quick_setup.ps1
    - sampleInput.csv
    - src/parameters.py
    - src/api_trigger.py
    - src/run.py
    - src/REntryScript/forecast.r

1. Open een PowerShell-venster en voer het script **quick_setup.ps1** uit dat u in de vorige stap hebt gedownload. Volg de instructies op het scherm. Het script stelt de vereiste werkruimte, de opslag, het standaard gegevensarchief en de berekeningsbronnen in. U moet echter nog wel de vereiste pijplijnen maken door de resterende stappen van deze procedure uit te voeren. (Pijplijnen bieden een manier om prognosescripts te starten vanuit Supply Chain Management.)
1. Upload in Azure Machine Learning Studio het bestand **sampleInput.csv** dat u in stap 1 hebt gedownload naar de container met de naam *demplan-azureml*. (Het script quick_setup.ps1 dat deze container heeft gemaakt.) Dit bestand is vereist voor het publiceren van de pijplijn en het genereren van een testprognose. Zie [Een blok-blob uploaden](/azure/storage/blobs/storage-quickstart-blobs-portal#upload-a-block-blob) voor instructies.
1. In Azure Machine Learning Studio selecteert u **Notebooks** in de navigator.
1. Zoek de volgende locatie in de structuur **Bestanden**: **Gebruikers/\[huidige gebruiker\]/src**.
1. Upload de resterende vier bestanden die u in stap 1 hebt gedownload naar de locatie die u in de vorige stap hebt gevonden.
1. Selecteer het bestand **api_trigger.py** dat u zojuist hebt geüpload en voer dit uit. Er wordt een pijplijn gemaakt die kan worden geactiveerd via de API.
1. Uw werkruimte is nu ingesteld. Ga verder naar de sectie [Verbindingsparameters voor Azure Machine Learning Service instellen in Supply Chain Management](#demand-forecast-parameters).

#### <a name="option-2-manually-set-up-your-machine-learning-workspace"></a><a name="ml-workspace-manual"></a>Optie 2: Uw machine learning-werkruimte handmatig instellen

In deze sectie wordt beschreven hoe u uw machine learning-werkruimte handmatig kunt instellen. U moet de procedures in deze sectie alleen voltooien als u hebt besloten het script voor geautomatiseerde instellingen, zoals beschreven in [Optie 1: Een script uitvoeren om uw machine learning-werkruimte automatisch in te stellen](#ml-workspace-script), niet uit te voeren.

##### <a name="step-1-create-a-new-workspace"></a><a name="create-workspace"></a>Stap 1: Een nieuwe werkruimte maken

Gebruik de volgende procedure om een nieuwe machine learning-werkruimte te maken.

1. Meld u aan bij uw Azure-portal.
1. Open de service **Machine learning**.
1. Selecteer **Maken** op de werkbalk om de wizard **Maken** te openen.
1. Voltooi de wizard door de instructies op het scherm te volgen. Houd de volgende punten in gedachten tijdens het werken:

    - Gebruik standaardinstellingen, tenzij op andere punten in deze lijst andere instellingen worden aangeraden.
    - Zorg ervoor dat u de geografische regio selecteert die overeenkomt met de regio waar uw exemplaar van Supply Chain Management is geïmplementeerd. Anders overschrijden sommige gegevens mogelijk regiogrenzen. Zie de [privacyverklaring](#privacy) verderop in dit onderwerp voor meer informatie.
    - Gebruik specifieke resources, zoals resourcegroepen, opslagaccounts, containerregisters, Azure-sleutelkluizen en netwerkbronnen.
    - Op de pagina **Verbindingsparameters voor Azure Machine Learning Service instellen** van de wizard moet u een naam opgeven voor een opslagaccount. Gebruik een account die is toegewezen aan vraagprognoses. Invoer- en uitvoergegevens voor vraagprognoses worden opgeslagen in deze opslagaccount.

Zie [De werkruimte maken](/azure/machine-learning/quickstart-create-resources#create-the-workspace) voor meer informatie.

##### <a name="step-2-configure-storage"></a><a name="config-storage"></a>Stap 2: Opslag configureren

U kunt de volgende procedure gebruiken om uw opslag in te stellen.

1. Open op GitHub de opslagplaats [Templates for Dynamics 365 Supply Chain Management demand forecasting with Azure Machine Learning](https://github.com/microsoft/Dynamics-365-Supply-Chain-Management-Demand-Forecasting-With-Azure-Machine-Learning-Service) en download het bestand **sampleInput.csv**.
1. Open de opslagaccount die u hebt gemaakt in [Stap 1: Een nieuwe werkruimte maken](#create-workspace).
1. Volg de instructies in [Een container maken](/azure/storage/blobs/storage-quickstart-blobs-portal#create-a-container) om een container met de naam *demplan-azureml* te maken.
1. Upload het bestand **sampleInput.csv** dat u in stap 1 hebt gedownload naar de container die u zojuist hebt gemaakt. Dit bestand is vereist voor het publiceren van de pijplijn en het genereren van een testprognose. Zie [Een blok-blob uploaden](/azure/storage/blobs/storage-quickstart-blobs-portal#upload-a-block-blob) voor instructies.

##### <a name="step-3-configure-a-default-datastore"></a>Stap 3: Een standaard gegevensarchief configureren

U kunt de volgende procedure gebruiken om uw standaard gegevensarchief in te stellen.

1. In Azure Machine Learning Studio selecteert u **Gegevensarchieven** in de navigator.
1. Maak een nieuw gegevensarchief van het type *Azure Blob Storage* dat verwijst naar de Blob Storage-container *demplan-azureml* die u in [Stap 2: Opslag configureren](#config-storage) hebt gemaakt. (Als het verificatietype van het nieuwe gegevensarchief *Accountsleutel* is, moet u accountsleutel opgeven voor de gemaakte opslagaccount. Zie [Toegangssleutels voor opslagaccounts beheren](/azure/storage/common/storage-account-keys-manage?tabs=azure-portal) voor instructies.
1. Maak van uw nieuwe gegevensarchief het standaard gegevensarchief door de details te openen en **Instellen als standaard gegevensarchief** te selecteren.

##### <a name="step-4-configure-compute-resources"></a><a name="config-compute-resources"></a>Stap 4: Berekeningsbronnen configureren

Gebruik de volgende procedure om een berekeningsresource in Te stellen in Azure Machine Learning Studio om uw prognosegeneratiescripts uit te voeren.

1. Open de detailpagina voor de machine learning-werkruimte die u hebt gemaakt in [Stap 1: Een nieuwe werkruimte maken](#create-workspace). Zoek de waarde voor **Web-URL voor Studio** en selecteer de koppeling om deze te openen.
1. Selecteer **Berekenen** in het navigatiedeelvenster.
1. Selecteer **Nieuw** op het tabblad **Rekenprocessen** om een wizard te openen die u helpt bij het maken van een nieuw rekenproces. Volg de instructies op het scherm. Het rekenproces wordt gebruikt om de pijplijn voor vraagprognose te maken (deze kan worden verwijderd nadat de pijplijn is gepubliceerd). Gebruik de standaardinstellingen.
1. Selecteer **Nieuw** op het tabblad **Rekenclusters** om een wizard te openen die u helpt bij het maken van een nieuw rekencluster. Volg de instructies op het scherm. Het rekencluster wordt gebruikt om vraagprognoses te genereren. De instellingen zijn van invloed op de prestaties en de maximale parallellisatie van de uitvoering. Stel de volgende velden in, maar gebruik de standaardinstellingen voor alle andere velden:

    - **Naam**: voer *e2ecpucluster* in.
    - **Grootte van virtuele machine**: pas deze instelling aan op basis van het gegevensvolume dat u verwacht te gebruiken als invoer voor vraagprognoses. Het aantal knooppunten mag niet groter zijn dan 11, omdat één knooppunt nodig is om het genereren van vraagprognoses te activeren en het maximum aantal knooppunten dat vervolgens kan worden gebruikt om een prognose te genereren 10 is. (U stelt in [Stap 5: Pijplijnen maken](#create-pipelines) ook het aantal knooppunten in het bestand parameters.py in.) Op elk knooppunt worden verschillende werknemerprocessen uitgevoerd die parallel prognosescripts uitvoeren. Het totale aantal werknemersprocessen in uw taak is *het aantal kernen dat een knooppunt heeft* × *het aantal knooppunten*. Als uw berekeningscluster bijvoorbeeld het type *Standaard\_D4* (acht kernen) en maximaal 11 knooppunten heeft en als de `nodes_count`-waarde in het parameters.py-bestand is ingesteld op *10*, is het parallellisatieniveau 80.

##### <a name="step-5-create-pipelines"></a><a name="create-pipelines"></a>Stap 5: Pijplijnen maken

Pijplijnen bieden een manier om prognosescripts te starten vanuit Supply Chain Management. Met de volgende procedure kunt u de vereiste pijplijnen maken.

1. Open op GitHub de opslagplaats [Templates for Dynamics 365 Supply Chain Management demand forecasting with Azure Machine Learning](https://github.com/microsoft/Dynamics-365-Supply-Chain-Management-Demand-Forecasting-With-Azure-Machine-Learning-Service) en download de volgende bestanden:

    - src/parameters.py
    - src/api_trigger.py
    - src/run.py
    - src/REntryScript/forecast.r

1. In Azure Machine Learning Studio selecteert u **Notebooks** in de navigator.
1. Zoek de volgende locatie in de structuur **Bestanden**: **Gebruikers/\[huidige gebruiker\]/src**.
1. Upload de vier bestanden die u in stap 1 hebt gedownload naar de locatie die u in de vorige stap hebt gevonden.
1. Open in Azure het bestand **parameters.py** dat u zojuist hebt geüpload. Zorg ervoor dat de waarde voor `nodes_count` één waarde kleiner is dan de waarde die u voor het rekencluster hebt geconfigureerd in de sectie [Stap 4: Berekeningsbronnen configureren](#config-compute-resources). Als de waarde voor `nodes_count` hoger dan of gelijk is aan het aantal knooppunten in het rekencluster, kan de pijplijn-uitvoering mogelijk starten. Deze reageert dan echter niet meer terwijl wordt gewacht op de vereiste resources. Zie sectie [Stap 4: Berekeningsresources configureren](#config-compute-resources) voor meer informatie over het aantal knooppunten.
1. Selecteer het bestand **api_trigger.py** dat u zojuist hebt geüpload en voer dit uit. Er wordt een pijplijn gemaakt die kan worden geactiveerd via de API.

### <a name="set-up-a-new-active-directory-application"></a><a name="aad-app"></a>Een nieuwe Active Directory-toepassing instellen

Een Active Directory-toepassing is vereist voor verificatie met de resources die zijn toegewezen aan vraagprognoses met behulp van de serviceprincipal. Daarom moet de toepassing het laagste bevoegdheidsniveau hebben dat nodig is om de prognose te genereren.

1. Meld u aan bij uw Azure-portal.
1. Registreer een nieuwe toepassing in de Azure Active Directory (Azure AD) van de tenant. Zie [De portal gebruiken om een Azure AD-toepassing en een service-principal te maken die toegang hebben tot bronnen](/azure/active-directory/develop/howto-create-service-principal-portal) voor meer informatie.
1. Volg de instructies op het scherm om de wizard te voltooien. Gebruik de standaardinstellingen.
1. Geef uw nieuwe Active Directory-toepassing toegang tot de volgende resources die u hebt gemaakt in de sectie [Machine learning instellen in Azure](#ml-workspace). Zie [Azure-rollen toewijzen via Azure Portal](/azure/role-based-access-control/role-assignments-portal?tabs=current) voor instructies. Met deze stap kan het systeem in staat worden gesteld om prognosegegevens te importeren en te exporteren, en pijplijn-uitvoeren voor machine learning vanuit Supply Chain Management te activeren.

    - Rol van bijdrager voor de machine learning-werkruimte
    - Rol van bijdrager voor de specifieke opslagaccount
    - Rol van bijdrager van gegevens in opslagblob voor de specifieke opslagaccount

1. Maak in de sectie **Certificaten en geheimen** van de gemaakte toepassing een geheim voor de toepassing. Zie [Een clientgeheim toevoegen](/azure/active-directory/develop/quickstart-register-app#add-a-client-secret) voor instructies.
1. Noteer de toepassings-id en het geheim. U hebt de details van deze toepassing later nodig wanneer u de pagina **Parameters voor vraagprognose** in Supply Chain Management instelt.

### <a name="set-up-azure-machine-learning-service-connection-parameters-in-supply-chain-management"></a><a name="demand-forecast-parameters"></a>Verbindingsparameters voor Azure Machine Learning Service instellen in Supply Chain Management

Gebruik de volgende procedure om uw Supply Chain Management-omgeving te verbinden met de machine learning-service die u zojuist hebt ingesteld in Azure.

1. Meld u aan bij Supply Chain Management.
1. Ga naar **Hoofdplanning \> Instellingen \> Vraagprognose \> Parameters voor vraagprognose**.
1. Ga naar het tabblad **Algemeen** en zorg ervoor dat het veld **Strategie voor aanmaken van vraagprognose** is ingesteld op *Azure Machine Learning Service*.
1. Ga naar het tabblad **Artikeltoewijzingssleutels** en zorg ervoor dat het veld **Strategie voor aanmaken van vraagprognose** is ingesteld op *Azure Machine Learning Service* voor elke toewijzingssleutel die Azure Machine Learning Service moet gebruiken voor vraagprognoses.
1. Stel de volgende velden in op het tabblad **Azure Machine Learning Service**:

    - **Tenant-id**: voer de id voor uw Azure-tenant in. Supply Chain Management gebruikt deze id voor verificatie met Azure Machine Learning Service. U kunt uw tenant-id vinden op de pagina **Overzicht** voor Azure AD in Azure Portal.
    - **Toepassings-id serviceprincipal**: voer de toepassings-id in voor de toepassing die u hebt gemaakt in de sectie [Active Directory-toepassing](#aad-app). Deze waarde wordt gebruikt om API-aanvragen voor Azure Machine Learning Service te autoriseren.
    - **Geheim serviceprincipal**: voer het toepassingsgeheim voor de serviceprincipal die u hebt gemaakt in de sectie [Active Directory-toepassing](#aad-app). Deze waarde wordt gebruikt om het toegangstoken te verkrijgen voor de beveiligingsprincipal die u hebt gemaakt om geautoriseerde bewerkingen uit te voeren in Azure Storage en de werkruimte van Azure Machine Language.
    - **Naam opslagaccount**: voer de naam van de Azure-opslagaccount in die u hebt opgegeven bij het uitvoeren van de installatiewizard in uw Azure-werkruimte. (Zie de sectie [Machine learning instellen in Azure](#ml-workspace) voor meer informatie.)
    - **Eindpuntadres pijplijn**: voer de URL van het REST-eindpunt van de pijplijn in voor uw Azure Machine Learning Service. U hebt deze pijplijn gemaakt als laatste stap bij het [instellen van machine learning in Azure](#ml-workspace). Voor de pijplijn-URL moet u zich aanmelden bij Azure Portal en **Pijplijnen** selecteren in de navigatie. Selecteer op het tabblad **Pijplijn** het eindpunt van de pijplijn met de naam **TriggerDemandForecastGeneration**. Kopieer vervolgens het REST-eindpunt dat wordt weergegeven.

    ![Parameters op het tabblad Azure Machine Learning Service van de pagina Parameters voor vraagprognose.](media/azure-ml-service-parameters.png "Parameters op het tabblad Azure Machine Learning Service van de pagina Parameters voor vraagprognose")

## <a name="privacy-notice"></a><a name="privacy"></a>Privacyverklaring

Als u *Azure Machine Learning Service* selecteert als uw strategie voor het maken van prognoses, stuurt Supply Chain Management uw klantgegevens voor historische vraag, zoals verzamelde hoeveelheden, productnamen en hun productdimensies, verzend- en ontvangstlocaties, klant-id's en prognoseparameters zich bevinden, automatisch naar de geografische regio waar de machine learning-werkruimte en de machine learning-werkruimte en de gekoppelde opslagaccount zich bevinden, met het doel toekomstige vraag te voorspellen. Azure Machine Learning Service kan zich in een andere geografische regio bevinden dan de geografische regio waar Supply Chain Management is geïmplementeerd. Sommige gebruikers kunnen bepalen of deze functionaliteit is ingeschakeld door de strategie voor het genereren van prognoses te selecteren op de pagina **Parameters voor vraagprognose**.

## <a name="additional-resources"></a>Aanvullende bronnen

- [Overzicht van Vraagprognose](introduction-demand-forecasting.md)
- [Een statistische basislijnprognose genereren](generate-statistical-baseline-forecast.md)
- [Handmatige correcties aanbrengen in de basislijnprognose](manual-adjustments-baseline-forecast.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
