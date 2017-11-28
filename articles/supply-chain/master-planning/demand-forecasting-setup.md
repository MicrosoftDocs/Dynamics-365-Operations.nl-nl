---
title: Instelling van vraagprognose
description: In dit onderwerp worden de insteltaken beschreven die u moet uitvoeren ter voorbereiding op de vraagprognose.
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ReqDemPlanDefaultAlgorithmParameters, ReqDemPlanForecastParameters
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 72653
ms.assetid: c5fa4b09-512d-4349-ac51-cc13da69a160
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 974edd06460df4afe594b0a033a042b8c2763f7f
ms.contentlocale: nl-nl
ms.lasthandoff: 11/03/2017

---

# <a name="demand-forecasting-setup"></a>Instelling van vraagprognose

[!include[banner](../includes/banner.md)]


In dit onderwerp worden de insteltaken beschreven die u moet uitvoeren ter voorbereiding op de vraagprognose.  

De insteltaken omvatten het instellen van de volgende gegevens en parameters.

## <a name="item-allocation-key"></a>Artikeltoewijzingssleutel
Een vraagprognose wordt alleen berekend voor een artikel en de dimensies ervan als het artikel onderdeel uitmaakt van een artikeltoewijzingssleutel. Deze regel wordt afgedwongen om grote aantallen artikelen te groeperen, zodat vraagprognoses sneller kunnen worden gemaakt. Het sleutelpercentage voor artikeltoewijzing wordt genegeerd wanneer vraagprognoses worden gegenereerd. Prognoses worden gemaakt op basis van alleen historische gegevens. 

Een artikel en de dimensies ervan moeten onderdeel zijn van slechts één artikeltoewijzingssleutel als de artikeltoewijzingssleutel wordt gebruikt tijdens het maken van prognoses. 

Als u een voorraadeenheid (SKU) aan een artikeltoewijzingssleutel wilt toevoegen, gaat u naar **Hoofdplanning** &gt; **Instellen** &gt; **Vraagprognose** &gt; **Artikeltoewijzingssleutels**. Gebruik de pagina **Artikelen toewijzen** om een artikel aan een toewijzingssleutel toe te wijzen.

## <a name="intercompany-planning-groups"></a>Intercompany-planningsgroepen
Vraagprognoses genereren cross-company prognoses. In Microsoft Dynamics 365 for Finance and Operations worden bedrijven die samen worden gepland, gegroepeerd in één intercompany-planningsgroep. Om per bedrijf op te geven welke artikeltoewijzingssleutels moeten worden meegenomen voor de vraagprognoses , koppelt u een artikeltoewijzingssleutel met het lid van de intercompany-planningsgroep door naar **Hoofdplanning** &gt; **Instellen** &gt; **Intercompany-planningsgroepen** te gaan. 

Als geen artikeltoewijzingssleutels aan leden van intercompany-planningsgroepen worden toegewezen, wordt standaard een vraagprognose berekend voor alle artikelen die worden toegewezen aan alle artikeltoewijzingssleutels vanuit alle Finance and Operations-bedrijven. Extra filteropties voor bedrijven en artikeltoewijzingssleutels zijn beschikbaar op de pagina **Statistische basislijnprognose maken**. 

Controleer het aantal artikelen dat wordt verwacht. Onnodige artikelen kunnen verhoogde kosten veroorzaken wanneer u Microsoft Azure Machine Learning gebruikt.

## <a name="demand-forecasting-parameters"></a>Parameters voor vraagprognose
Als u vraagprognoseparameters wilt instellen, gaat u naar **Hoofdplanning** &gt; **Instellen** &gt; **Parameters voor vraagprognose**. Omdat vraagprognose cross-company wordt uitgevoerd, is de instelling globaal. Met andere woorden, geldt de instelling voor alle bedrijven. 

Vraagprognoses genereren de prognose in hoeveelheden. Daarom moet de maateenheid waarin de hoeveelheid moet worden uitgedrukt worden opgegeven in het veld **Vraagprognose-eenheid**. De maateenheid moet uniek zijn om te helpen waarborgen dat de aggregatie en percentagedistributie relevant zijn. Voor meer informatie over aggregatie en percentagedistributie zie [Handmatige correcties aanbrengen in de basislijnprognose](manual-adjustments-baseline-forecast.md) Voor elke maateenheid die wordt gebruikt voor voorraadeenheden die worden opgenomen in de vraagprognose, moet u ervoor zorgen dat er een conversieregel voor de maateenheid en de algemene maateenheid van de prognose is. Als prognose aanmaken wordt uitgevoerd, wordt de lijst met artikelen die geen maateenheidsconversie hebben geregistreerd, zodat u de installatie gemakkelijk kunt verbeteren. 

Vraagprognoses kunnen worden gebruikt voor prognoses van zowel afhankelijke als onafhankelijke vraag. Als bijvoorbeeld alleen het selectievakje **Verkooporder** is ingeschakeld en als alle artikelen die voor de vraagprognose worden beschouwd, artikelen zijn die worden verkocht, berekent het systeem onafhankelijke vraag. Kritieke subcomponenten kunnen echter worden toegevoegd aan artikeltoewijzingssleutels en worden opgenomen in vraagprognoses. In dit geval, als het selectievakje **Productieregel** is ingeschakeld, wordt een afhankelijke prognose berekend. 

Er zijn twee methoden voor het maken van een basislijnprognose in Finance and Operations. U kunt prognosemodellen naast historische gegevens gebruiken of u kunt ze eenvoudig over de historische gegevens naar de prognose kopiëren. In het veld **Strategie voor aanmaken van vraagprognose** kunt u tussen deze twee methoden kiezen. Selecteer om prognosemodellen te gebruiken **Azure Machine Learning**. 

Door te klikken op **Prognosedimensies** in het linkerdeelvenster van de pagina **Parameters voor vraagprognose** kunt u de set prognosedimensies selecteren om te gebruiken wanneer de vraagprognose wordt gegenereerd. Een prognosedimensie geeft het detailniveau aan waarvoor de prognose is gedefinieerd. Bedrijf, site en artikeltoewijzingssleutel zijn verplichte prognosedimensies, maar u kunt prognoses ook genereren op het niveau van het magazijn, de voorraadstatus, de klantgroep, de klantrekening, het land/de regio, de status, het artikel en alle artikeldimensieniveaus. 

U kunt op elk moment prognosedimensies toevoegen aan de lijst met dimensies die voor vraagprognoses worden gebruikt. U kunt ook eventueel prognosedimensie uit de lijst verwijderen. Handmatige correcties gaan echter verloren als u een prognosedimensie toevoegt of verwijdert. 

Niet alle artikelen gedragen zich op dezelfde vanuit een vraagprognoseperspectief. Vergelijkbare artikelen kunnen in één artikeltoewijzingssleutel worden gegroepeerd, en de parameters zoals transactietypen en de instellingen voor de prognosemethode kunnen per artikeltoewijzingssleutel worden ingesteld. Klik op **Artikeltoewijzingssleutels** in het linkerdeelvenster van de pagina **Parameters voor vraagprognose**. 

Om de prognose te maken, gebruikt Finance and Operations een Machine Learning-webservice. Om verbinding met de service te maken, moet u de volgende gegevens aan Finance and Operations verstrekken als u zich aanmeldt bij Microsoft Azure Machine Learning Studio:

-   Application Programming Interface (API)-sleutel voor webservice
-   Eindpunt-URL webservice
-   Azure-naam van opslagaccount
-   Azure-sleutel van opslagaccount

**Opmerking:** De Azure-opslagaccountnaam en sleutel zijn alleen vereist wanneer u een aangepast opslagaccount gebruikt. Als u de on-premises versie gebruikt, moet u een aangepaste opslagaccount bij Azure hebben, zodat de Machine Learning-service toegang heeft tot de historische gegevens. 

Om vraagvoorspellingen te maken, kunt u uw eigen service implementeren door Machine Learning Studio te gebruiken of de vraagprognose-experimenten van Finance and Operations. Instructies voor het implementeren van de vraagprognose-experimenten van Finance and Operations als een webservice, zijn beschikbaar in Finance and Operations. Op de pagina **Parameters voor vraagprognose** klikt u op het tabblad **Azure Machine Learning**.

## <a name="settings-for-the-finance-and-operations-demand-forecasting-machine-learning-service"></a>Instellingen voor de Machine Learning-service voor vraagprognoses van Finance and Operations
Als u de parameters die kunnen worden geconfigureerd voor de Finance and Operations-vraagprognoseservice, gaat u naar **Hoofdplanning** &gt; **Instellen** &gt; **Vraagprognose** &gt; **Parameters van prognosealgoritme**. Op de pagina **Parameters van prognosealgoritme** worden de standaardwaarden voor de parameters weergegeven. U kunt deze parameters overschrijven op de pagina **Parameters voor vraagprognose**. Gebruik het tabblad **Algemeen** om de parameters globaal te overschrijven, of gebruik het tabblad **Artikeltoewijzingssleutels** om de parameters per artikeltoewijzingssleutel te overschrijven. De parameters die voor een artikeltoewijzingssleutel worden overschreven beïnvloeden alleen de prognose van artikelen die aan de artikeltoewijzingssleutel zijn gekoppeld.

<a name="see-also"></a>Zie ook
--------

[Inleiding op vraagprognoses](introduction-demand-forecasting.md)

[Statistische basislijnprognose genereren](generate-statistical-baseline-forecast.md)

[Handmatige correcties aanbrengen in de basislijnprognose](manual-adjustments-baseline-forecast.md)




