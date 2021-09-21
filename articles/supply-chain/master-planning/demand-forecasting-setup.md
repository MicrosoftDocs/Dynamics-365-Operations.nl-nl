---
title: Instelling van vraagprognose
description: In dit onderwerp worden de insteltaken beschreven die u moet uitvoeren ter voorbereiding op de vraagprognose.
author: roxanadiaconu
ms.date: 08/09/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqDemPlanDefaultAlgorithmParameters, ReqDemPlanForecastParameters
audience: Application User
ms.reviewer: kamaybac
ms.custom: 72653
ms.assetid: c5fa4b09-512d-4349-ac51-cc13da69a160
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 81fec20130a1621d4cb55394db75a7ac0a16fdf3
ms.sourcegitcommit: 4fbf031319109660c0462a800f85848571eb040d
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/02/2021
ms.locfileid: "7471330"
---
# <a name="demand-forecasting-setup"></a>Instelling van vraagprognose

[!include [banner](../includes/banner.md)]

In dit onderwerp worden de insteltaken beschreven die u moet uitvoeren ter voorbereiding op de vraagprognose.  

De insteltaken omvatten het instellen van de volgende gegevens en parameters.

## <a name="item-allocation-keys"></a>Artikeltoewijzingssleutels

Een vraagprognose wordt alleen berekend voor een artikel en de dimensies ervan als het artikel onderdeel uitmaakt van een artikeltoewijzingssleutel. Deze regel wordt afgedwongen om grote aantallen artikelen te groeperen, zodat vraagprognoses sneller kunnen worden gemaakt. Het sleutelpercentage voor artikeltoewijzing wordt genegeerd wanneer vraagprognoses worden gegenereerd. Prognoses worden gemaakt op basis van alleen historische gegevens.

Een artikel en de dimensies ervan moeten onderdeel zijn van slechts één artikeltoewijzingssleutel als de artikeltoewijzingssleutel wordt gebruikt tijdens het maken van prognoses.

Als u een voorraadeenheid (SKU) aan een artikeltoewijzingssleutel wilt toevoegen, gaat u naar **Hoofdplanning \> Instellen \> Vraagprognose \> Artikeltoewijzingssleutels**. Gebruik de pagina **Artikelen toewijzen** om een artikel aan een toewijzingssleutel toe te wijzen.

## <a name="intercompany-planning-groups"></a>Intercompany-planningsgroepen

Vraagprognoses genereren cross-company prognoses. In Dynamics 365 Supply Chain Management worden bedrijven die samen worden gepland, gegroepeerd in één intercompany-planninggroep. Om per bedrijf op te geven welke artikeltoewijzingssleutels moeten worden meegenomen voor de vraagprognoses , koppelt u een artikeltoewijzingssleutel met het lid van de intercompany-planningsgroep door naar **Hoofdplanning \> Instellen \> Intercompany-planningsgroepen** te gaan.

Als geen artikeltoewijzingssleutels aan leden van intercompany-planningsgroepen worden toegewezen, wordt standaard een vraagprognose berekend voor alle artikelen die worden toegewezen aan alle artikeltoewijzingssleutels vanuit alle bedrijven. Extra filteropties voor bedrijven en artikeltoewijzingssleutels zijn beschikbaar op de pagina **Statistische basislijnprognose maken**.

Controleer het aantal artikelen dat wordt verwacht. Onnodige artikelen kunnen verhoogde kosten veroorzaken wanneer u Microsoft Azure Machine Learning gebruikt.

## <a name="demand-forecasting-parameters"></a>Parameters voor vraagprognose

Als u vraagprognoseparameters wilt instellen, gaat u naar **Hoofdplanning \> Instellen \> \> Vraagprognose \> Parameters voor vraagprognose**. Omdat vraagprognose cross-company wordt uitgevoerd, is de instelling globaal. Dit houdt in dat de instelling voor alle bedrijven geldt.

Vraagprognoses genereren de prognose in hoeveelheden. Daarom moet de maateenheid waarin de hoeveelheid moet worden uitgedrukt worden opgegeven in het veld **Vraagprognose-eenheid**. De maateenheid moet uniek zijn om te helpen waarborgen dat de aggregatie en percentagedistributie relevant zijn. Voor meer informatie over aggregatie en percentagedistributie zie [Handmatige correcties aanbrengen in de basislijnprognose](manual-adjustments-baseline-forecast.md) Voor elke maateenheid die wordt gebruikt voor voorraadeenheden die worden opgenomen in de vraagprognose, moet u ervoor zorgen dat er een conversieregel voor de maateenheid en de algemene maateenheid van de prognose is. Als prognose aanmaken wordt uitgevoerd, wordt de lijst met artikelen die geen maateenheidsconversie hebben geregistreerd, zodat u de installatie gemakkelijk kunt verbeteren.

Vraagprognoses kunnen worden gebruikt voor prognoses van zowel afhankelijke als onafhankelijke vraag. Als bijvoorbeeld alleen het selectievakje **Verkooporder** is ingeschakeld en als alle artikelen die voor de vraagprognose worden beschouwd, artikelen zijn die worden verkocht, berekent het systeem onafhankelijke vraag. Kritieke subcomponenten kunnen echter worden toegevoegd aan artikeltoewijzingssleutels en worden opgenomen in vraagprognoses. In dit geval, als het selectievakje **Productieregel** is ingeschakeld, wordt een afhankelijke prognose berekend.

Er zijn twee methoden voor het maken van een basislijnprognose. U kunt prognosemodellen naast historische gegevens gebruiken of u kunt ze eenvoudig over de historische gegevens naar de prognose kopiëren. In het veld **Strategie voor aanmaken van vraagprognose** kunt u tussen deze twee methoden kiezen. Selecteer om prognosemodellen te gebruiken **Azure Machine Learning**.

Door **Prognosedimensies** te selecteren in het linkerdeelvenster van de pagina **Parameters voor vraagprognose** kunt u de set prognosedimensies selecteren om te gebruiken wanneer de vraagprognose wordt gegenereerd. Een prognosedimensie geeft het detailniveau aan waarvoor de prognose is gedefinieerd. Bedrijf, site en artikeltoewijzingssleutel zijn vereiste prognosedimensies, maar u kunt prognoses ook genereren op het niveau van het magazijn, de voorraadstatus, de klantgroep, de klantrekening, het land/de regio, de status, het artikel en alle artikeldimensieniveaus.

U kunt op elk moment prognosedimensies toevoegen aan de lijst met dimensies die voor vraagprognoses worden gebruikt. U kunt ook eventueel prognosedimensie uit de lijst verwijderen. Handmatige correcties gaan echter verloren als u een prognosedimensie toevoegt of verwijdert.

Niet alle artikelen presteren op dezelfde manier vanuit een vraagprognoseperspectief. Vergelijkbare artikelen kunnen in één artikeltoewijzingssleutel worden gegroepeerd, en de parameters zoals transactietypen en de instellingen voor de prognosemethode kunnen per artikeltoewijzingssleutel worden ingesteld. Selecteer **Artikeltoewijzingssleutels** in het linkerdeelvenster van de pagina **Parameters voor vraagprognose**.

Om de prognose te genereren, gebruikt Supply Chain Management een Machine Learning-webservice. Om verbinding met de service te maken, moet u de volgende gegevens verstrekken als u zich aanmeldt bij Microsoft Azure Machine Learning Studio (klassiek):

- Application Programming Interface (API)-sleutel voor webservice
- Eindpunt-URL webservice
- Azure-naam van opslagaccount
- Azure-sleutel van opslagaccount

> [!NOTE]
> De Azure-opslagaccountnaam en sleutel zijn alleen vereist wanneer u een aangepast opslagaccount gebruikt. Als u de on-premises versie gebruikt, moet u een aangepaste opslagaccount bij Azure hebben, zodat Machine Learning toegang heeft tot de historische gegevens.

Om vraagvoorspellingen te maken, kunt u uw eigen service implementeren door Machine Learning Studio te gebruiken of de vraagprognose-experimenten van Supply Chain Management. Instructies voor het implementeren van de vraagprognose-experimenten als een webservice, zijn beschikbaar in Supply Chain Management. Open op de pagina **Parameters voor vraagprognose** het tabblad **Azure Machine Learning**.

## <a name="settings-for-the-demand-forecasting-machine-learning-service"></a>Instellingen machine learning-service voor vraagprognoses

Als u de parameters die kunnen worden geconfigureerd voor de vraagprognoseservice, gaat u naar **Hoofdplanning \> Instellen \> Vraagprognose \> Parameters van prognosealgoritme**. Op de pagina **Standaardparameters van prognosealgoritme** worden de standaardwaarden voor de parameters weergegeven. U kunt deze parameters overschrijven door naar **Hoofdplanning \> Instellingen \> Vraagprognose \> Parameters voor vraagprognose** te gaan, waar u het volgende kunt doen:

- Gebruik het tabblad **Algemeen** om de parameters globaal te overschrijven.
- Gebruik het tabblad **Artikeltoewijzingssleutels** om de parameters per artikeltoewijzingssleutel te overschrijven. De parameters die voor een artikeltoewijzingssleutel worden overschreven beïnvloeden alleen de prognose van artikelen die aan de artikeltoewijzingssleutel zijn gekoppeld.

### <a name="forecast-algorithm-parameters"></a>Parameters van prognosealgoritme

Op het tabblad **Artikeltoewijzingssleutels** van de pagina **Parameters voor vraagprognose** kunt u het sneltabblad **Parameters prognosealgoritme** gebruiken om parameters voor het prognosealgoritme toe te wijzen voor de artikeltoewijzingssleutel die u hebt geselecteerd in het raster aan de linkerkant. U kunt de knoppen **Toevoegen** en **Verwijderen** op de werkbalk gebruiken om de vereiste verzameling parameters vast te stellen. Selecteer voor elke parameter in de lijst een van de volgende waarden in het veld **Naam** en geef vervolgens de juiste waarde op in het veld **Waarde**:

- **Percentage waarschijnlijkheidsniveau** - een waarschijnlijkheidsinterval bestaat uit een waardebereik dat als goede ramingen voor de vraagprognose fungeert. Een waarschijnlijkheidspercentage van 95% geeft aan dat er een kans van 5% is dat de toekomstige vraag buiten het bereik van het waarschijnlijkheidsinterval valt.
- **Gedwongen seizoensgebondenheid** - hiermee geeft u op of het model moet worden gedwongen om een bepaald type seizoensgebondenheid te gebruiken. Dit geldt alleen voor ARIMA en ETS. Opties: AUTO (standaard), GEEN, ADDITIEF, MULTIPLICATIEF.
- **Prognosemodel** - opties: ARIMA, ETS, STL, ETS+ARIMA, ETS+STL, ALLE. Gebruik **ALLE** om het meest geschikte model te selecteren.
- **Maximale prognosewaarde** - hiermee geeft u de maximumwaarde op die voor voorspellingen moet worden gebruikt. Indeling: +1E[n] of numerieke constante.
- **Minimale prognosewaarde** - hiermee geeft u de minimumwaarde op die voor voorspellingen moet worden gebruikt. Indeling: -1E[n] of numerieke constante.
- **Vervanging van ontbrekende waarde** - hiermee geeft u op hoe hiaten in historische gegevens worden gevuld. Opties: numerieke waarde, GEMIDDELDE, VORIGE, LINEAIR INTERPOLEREN, MULTINOMIAAL INTERPOLEREN.
- **Vervangingsbereik van ontbrekende waarde** - hiermee geeft u aan of de vervanging van de waarde alleen van toepassing is op het datumbereik van elk afzonderlijk granulatiekenmerk of op de gehele gegevensset. De volgende opties zijn beschikbaar voor het bepalen van het datumbereik dat door het systeem wordt gebruikt bij het invullen van gaten in historische gegevens:

  - GLOBAAL - het systeem gebruikt het volledige datumbereik van alle kenmerken van de granulariteit.
  - HISTORY_DATE_RANGE - Het systeem gebruikt een specifiek datumbereik dat wordt gedefinieerd door de velden **Begindatum** en **Einddatum** in de veldgroep **Historische periode** in het dialoogvenster **Statistische basislijnprognose genereren**.
  - GRANULARITY_ATTRIBUTE - het systeem gebruikt het datumbereik van het kenmerk granulariteit dat momenteel is verwerkt.

  > [!NOTE]
  > Een granulariteitskenmerk is een combinatie van prognosedimenssie waarmee de prognose wordt uitgevoerd. U kunt parameters voor prognosedimensies definiëren op de pagina **Parameters voor vraagprognose**.

- **Hint seizoensgebondenheid** - voor seizoensgegevens kunt u het prognosemodel een hint geven om de prognosenauwkeurigheid te verbeteren. Indeling: geheel getal dat het aantal buckets aangeeft waarvoor een vraagpatroon zichzelf herhaalt. Voer bijvoorbeeld "6" in voor gegevens die zichzelf elke 6 maanden herhalen.
- **Groottepercentage van testset** - percentage van historische gegevens die kunnen worden gebruikt als een testset voor de berekening van prognosenauwkeurigheid.

## <a name="additional-resources"></a>Aanvullende resources

- [Overzicht van Vraagprognose](introduction-demand-forecasting.md)
- [Een statistische basislijnprognose genereren](generate-statistical-baseline-forecast.md)
- [Handmatige correcties aanbrengen in de basislijnprognose](manual-adjustments-baseline-forecast.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
