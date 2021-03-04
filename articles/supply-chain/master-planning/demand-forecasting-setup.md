---
title: Instelling van vraagprognose
description: In dit onderwerp worden de insteltaken beschreven die u moet uitvoeren ter voorbereiding op de vraagprognose.
author: roxanadiaconu
manager: tfehr
ms.date: 01/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqDemPlanDefaultAlgorithmParameters, ReqDemPlanForecastParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 72653
ms.assetid: c5fa4b09-512d-4349-ac51-cc13da69a160
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6d0de588d54948d89f636cadeb66c3d9e6878015
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/13/2020
ms.locfileid: "4425687"
---
# <a name="demand-forecasting-setup"></a>Instelling van vraagprognose

[!include [banner](../includes/banner.md)]

In dit onderwerp worden de insteltaken beschreven die u moet uitvoeren ter voorbereiding op de vraagprognose.  

De insteltaken omvatten het instellen van de volgende gegevens en parameters.

## <a name="item-allocation-key"></a>Artikeltoewijzingssleutel
Een vraagprognose wordt alleen berekend voor een artikel en de dimensies ervan als het artikel onderdeel uitmaakt van een artikeltoewijzingssleutel. Deze regel wordt afgedwongen om grote aantallen artikelen te groeperen, zodat vraagprognoses sneller kunnen worden gemaakt. Het sleutelpercentage voor artikeltoewijzing wordt genegeerd wanneer vraagprognoses worden gegenereerd. Prognoses worden gemaakt op basis van alleen historische gegevens. 

Een artikel en de dimensies ervan moeten onderdeel zijn van slechts één artikeltoewijzingssleutel als de artikeltoewijzingssleutel wordt gebruikt tijdens het maken van prognoses. 

Als u een voorraadeenheid (SKU) aan een artikeltoewijzingssleutel wilt toevoegen, gaat u naar **Hoofdplanning** &gt; **Instellen** &gt; **Vraagprognose** &gt; **Artikeltoewijzingssleutels**. Gebruik de pagina **Artikelen toewijzen** om een artikel aan een toewijzingssleutel toe te wijzen.

## <a name="intercompany-planning-groups"></a>Intercompany-planningsgroepen
Vraagprognoses genereren cross-company prognoses. In Dynamics 365 Supply Chain Management worden bedrijven die samen worden gepland, gegroepeerd in één intercompany-planninggroep. Om per bedrijf op te geven welke artikeltoewijzingssleutels moeten worden meegenomen voor de vraagprognoses , koppelt u een artikeltoewijzingssleutel met het lid van de intercompany-planningsgroep door naar **Hoofdplanning** &gt; **Instellen** &gt; **Intercompany-planningsgroepen** te gaan. 

Als geen artikeltoewijzingssleutels aan leden van intercompany-planningsgroepen worden toegewezen, wordt standaard een vraagprognose berekend voor alle artikelen die worden toegewezen aan alle artikeltoewijzingssleutels vanuit alle bedrijven. Extra filteropties voor bedrijven en artikeltoewijzingssleutels zijn beschikbaar op de pagina **Statistische basislijnprognose maken**. 

Controleer het aantal artikelen dat wordt verwacht. Onnodige artikelen kunnen verhoogde kosten veroorzaken wanneer u Microsoft Azure Machine Learning gebruikt.

## <a name="demand-forecasting-parameters"></a>Parameters voor vraagprognose
Als u vraagprognoseparameters wilt instellen, gaat u naar **Hoofdplanning** &gt; **Instellen** &gt; **Parameters voor vraagprognose**. Omdat vraagprognose cross-company wordt uitgevoerd, is de instelling globaal. Met andere woorden, geldt de instelling voor alle bedrijven. 

Vraagprognoses genereren de prognose in hoeveelheden. Daarom moet de maateenheid waarin de hoeveelheid moet worden uitgedrukt worden opgegeven in het veld **Vraagprognose-eenheid**. De maateenheid moet uniek zijn om te helpen waarborgen dat de aggregatie en percentagedistributie relevant zijn. Voor meer informatie over aggregatie en percentagedistributie zie [Handmatige correcties aanbrengen in de basislijnprognose](manual-adjustments-baseline-forecast.md) Voor elke maateenheid die wordt gebruikt voor voorraadeenheden die worden opgenomen in de vraagprognose, moet u ervoor zorgen dat er een conversieregel voor de maateenheid en de algemene maateenheid van de prognose is. Als prognose aanmaken wordt uitgevoerd, wordt de lijst met artikelen die geen maateenheidsconversie hebben geregistreerd, zodat u de installatie gemakkelijk kunt verbeteren. 

Vraagprognoses kunnen worden gebruikt voor prognoses van zowel afhankelijke als onafhankelijke vraag. Als bijvoorbeeld alleen het selectievakje **Verkooporder** is ingeschakeld en als alle artikelen die voor de vraagprognose worden beschouwd, artikelen zijn die worden verkocht, berekent het systeem onafhankelijke vraag. Kritieke subcomponenten kunnen echter worden toegevoegd aan artikeltoewijzingssleutels en worden opgenomen in vraagprognoses. In dit geval, als het selectievakje **Productieregel** is ingeschakeld, wordt een afhankelijke prognose berekend. 

Er zijn twee methoden voor het maken van een basislijnprognose. U kunt prognosemodellen naast historische gegevens gebruiken of u kunt ze eenvoudig over de historische gegevens naar de prognose kopiëren. In het veld **Strategie voor aanmaken van vraagprognose** kunt u tussen deze twee methoden kiezen. Selecteer om prognosemodellen te gebruiken **Azure Machine Learning**. 

Door te klikken op **Prognosedimensies** in het linkerdeelvenster van de pagina **Parameters voor vraagprognose** kunt u de set prognosedimensies selecteren om te gebruiken wanneer de vraagprognose wordt gegenereerd. Een prognosedimensie geeft het detailniveau aan waarvoor de prognose is gedefinieerd. Bedrijf, site en artikeltoewijzingssleutel zijn verplichte prognosedimensies, maar u kunt prognoses ook genereren op het niveau van het magazijn, de voorraadstatus, de klantgroep, de klantrekening, het land/de regio, de status, het artikel en alle artikeldimensieniveaus. 

U kunt op elk moment prognosedimensies toevoegen aan de lijst met dimensies die voor vraagprognoses worden gebruikt. U kunt ook eventueel prognosedimensie uit de lijst verwijderen. Handmatige correcties gaan echter verloren als u een prognosedimensie toevoegt of verwijdert. 

Niet alle artikelen gedragen zich op dezelfde vanuit een vraagprognoseperspectief. Vergelijkbare artikelen kunnen in één artikeltoewijzingssleutel worden gegroepeerd, en de parameters zoals transactietypen en de instellingen voor de prognosemethode kunnen per artikeltoewijzingssleutel worden ingesteld. Klik op **Artikeltoewijzingssleutels** in het linkerdeelvenster van de pagina **Parameters voor vraagprognose**. 

Om de prognose te maken, gebruikt Supply Chain Management een Machine Learning-webservice. Om verbinding met de service te maken, moet u de volgende gegevens verstrekken als u zich aanmeldt bij Microsoft Azure Machine Learning Studio (klassiek):

-   Application Programming Interface (API)-sleutel voor webservice
-   Eindpunt-URL webservice
-   Azure-naam van opslagaccount
-   Azure-sleutel van opslagaccount

> [!NOTE]
> De Azure-opslagaccountnaam en sleutel zijn alleen vereist wanneer u een aangepast opslagaccount gebruikt. Als u de on-premises versie gebruikt, moet u een aangepaste opslagaccount bij Azure hebben, zodat Machine Learning toegang heeft tot de historische gegevens. 

Om vraagvoorspellingen te maken, kunt u uw eigen service implementeren door Machine Learning Studio te gebruiken of de vraagprognose-experimenten van Supply Chain Management. Instructies voor het implementeren van de vraagprognose-experimenten als een webservice, zijn beschikbaar in Supply Chain Management. Op de pagina **Parameters voor vraagprognose** klikt u op het tabblad **Azure Machine Learning**.

## <a name="settings-for-the-demand-forecasting-machine-learning-service"></a>Instellingen machine learning-service voor vraagprognoses
Als u de parameters die kunnen worden geconfigureerd voor de vraagprognoseservice, gaat u naar **Hoofdplanning** &gt; **Instellen** &gt; **Vraagprognose** &gt; **Parameters van prognosealgoritme**. Op de pagina **Parameters van prognosealgoritme** worden de standaardwaarden voor de parameters weergegeven. U kunt deze parameters overschrijven op de pagina **Parameters voor vraagprognose**. Gebruik het tabblad **Algemeen** om de parameters globaal te overschrijven, of gebruik het tabblad **Artikeltoewijzingssleutels** om de parameters per artikeltoewijzingssleutel te overschrijven. De parameters die voor een artikeltoewijzingssleutel worden overschreven beïnvloeden alleen de prognose van artikelen die aan de artikeltoewijzingssleutel zijn gekoppeld.

### <a name="forecast-algorithm-parameters"></a>Parameters van prognosealgoritme

Op het tabblad **Toewijzingssleutels** kunt u de **Parameters van prognosealgoritme** instellen voor elke artikeltoewijzingssleutel. De volgende opties zijn beschikbaar.
- **Percentage waarschijnlijkheidsniveau**: een waarschijnlijkheidsinterval bestaat uit een waardebereik dat als goede ramingen voor de vraagprognose fungeert. Een waarschijnlijkheidspercentage van 95% geeft aan dat er een kans van 5% is dat de toekomstige vraag buiten het bereik van het waarschijnlijkheidsinterval valt.
- **Gedwongen seizoensgebondenheid**: hiermee geeft u op of het model moet worden gedwongen om een bepaald type seizoensgebondenheid te gebruiken. Dit geldt alleen voor ARIMA en ETS. Opties: AUTO (standaard), GEEN, ADDITIEF, MULTIPLICATIEF.
- **Prognosemodel**: opties: ARIMA, ETS, STL, ETS+ARIMA, ETS+STL, ALLE. Gebruik **ALLE** om het meest geschikte model te selecteren.
- **Maximale prognosewaarde**: hiermee geeft u de maximumwaarde op die voor voorspellingen moet worden gebruikt. Indeling: +1E[n] of numerieke constante.
- **Minimale prognosewaarde**: hiermee geeft u de minimumwaarde op die voor voorspellingen moet worden gebruikt. Indeling: -1E[n] of numerieke constante.
- **Vervanging van ontbrekende waarde**: hiermee geeft u op hoe hiaten in historische gegevens worden gevuld. Opties: numerieke waarde, GEMIDDELDE, VORIGE, LINEAIR INTERPOLEREN, MULTINOMIAAL INTERPOLEREN.
- **Vervangingsbereik van ontbrekende waarde**: hiermee geeft u aan of de vervanging van de waarde alleen van toepassing is op het gegevensbereik van elk afzonderlijk granulatiekenmerk of op de gehele gegevensset. Opties: GRANULARITY_ATTRIBUTE (standaard), ALGEMEEN.
- **Hint seizoensgebondenheid**: voor seizoensgegevens kunt u het prognosemodel een hint geven om de prognosenauwkeurigheid te verbeteren. Indeling: geheel getal dat het aantal buckets aangeeft waarvoor een vraagpatroon zichzelf herhaalt. Voer bijvoorbeeld "6" in voor gegevens die zichzelf elke 6 maanden herhalen.
- **Groottepercentage van testset**: percentage van historische gegevens die kunnen worden gebruikt als een testset voor de berekening van prognosenauwkeurigheid. 

<a name="additional-resources"></a>Aanvullende resources
--------

[Overzicht van Vraagprognose](introduction-demand-forecasting.md)

[Een statistische basislijnprognose genereren](generate-statistical-baseline-forecast.md)

[Handmatige correcties aanbrengen in de basislijnprognose](manual-adjustments-baseline-forecast.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]