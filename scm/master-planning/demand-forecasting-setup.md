---
title: Instelling van vraagprognose
description: In dit onderwerp worden de insteltaken beschreven die u moet uitvoeren ter voorbereiding op de vraagprognose.
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: ReqDemPlanDefaultAlgorithmParameters, ReqDemPlanForecastParameters
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 72653
ms.assetid: c5fa4b09-512d-4349-ac51-cc13da69a160
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: f629329f4f50bd7c8edcfd70641bace01a1c53aa
ms.lasthandoff: 03/31/2017


---

# <a name="demand-forecasting-setup"></a>Instelling van vraagprognose

In dit onderwerp worden de insteltaken beschreven die u moet uitvoeren ter voorbereiding op de vraagprognose.  

De insteltaken omvatten het instellen van de volgende gegevens en parameters.

## <a name="item-allocation-key"></a>Artikeltoewijzingssleutel
Een vraagprognose wordt alleen berekend voor een artikel en de dimensies ervan als het artikel onderdeel uitmaakt van een artikeltoewijzingssleutel. Deze regel wordt afgedwongen naar grote aantallen van artikelen, groep, zodat vraagprognoses sneller kunnen worden gemaakt. De belangrijkste toewijzingspercentage van het artikel wordt genegeerd wanneer vraagprognoses worden gegenereerd. Prognoses worden gemaakt op basis van alleen historische gegevens. 

Een artikel en de dimensies ervan moeten onderdeel zijn van slechts één artikeltoewijzingssleutel als de artikeltoewijzingssleutel wordt gebruikt tijdens het maken van prognoses. 

Als u wilt een voorraadeenheid (SKU) toevoegen aan een artikeltoewijzingssleutel, gaat u naar **hoofdplanning**&gt;**Setup**&gt;**vraagprognose**&gt;**artikel toewijzingssleutels**. Gebruik de pagina **Artikelen toewijzen** om een artikel aan een toewijzingssleutel toe te wijzen.

## <a name="intercompany-planning-groups"></a>Intercompany-planningsgroepen
Vraagprognoses genereren cross-company prognoses. In Microsoft Dynamics 365 voor bewerkingen, worden de bedrijven die samen worden gepland in een intercompany-planningsgroep gegroepeerd. Om op te geven per bedrijf, welke Artikeltoewijzingssleutels moeten worden genomen voor vraagprognose, koppelt u een artikeltoewijzingssleutel aan de intercompany-planning groeplid gaat u naar **hoofdplanning**&gt;**Setup**&gt;**intercompany-planningsgroepen**. 

Als er geen artikeltoewijzingssleutels zijn toegewezen aan een intercompany-planning groepsleden, wordt een vraagprognose standaard berekend voor alle artikelen die zijn toegewezen aan alle Artikeltoewijzingssleutels uit alle Dynamics 365 voor bewerkingen bedrijven. Extra filteropties voor bedrijven en artikeltoewijzingssleutels zijn beschikbaar op de pagina **Statistische basislijnprognose maken**. 

Controleer het aantal artikelen dat wordt verwacht. Onnodige artikelen kunnen verhoogde kosten veroorzaken wanneer u Microsoft Azure Machine Learning gebruikt.

## <a name="demand-forecasting-parameters"></a>Parameters voor vraagprognose
Als u de vraag, prognoses van de parameters instellen, gaat u naar **hoofdplanning**&gt;**Setup**&gt;**vraag prognoses van de parameters**. Omdat vraagprognose cross-company wordt uitgevoerd, is de instelling globaal. Met andere woorden, geldt de instelling voor alle bedrijven. 

Vraagprognoses genereren de prognose in hoeveelheden. Daarom moet de maateenheid waarin de hoeveelheid moet worden uitgedrukt worden opgegeven in het veld **Vraagprognose-eenheid**. De maateenheid moet uniek zijn om te helpen waarborgen dat de aggregatie en percentagedistributie relevant zijn. Voor meer informatie over aggregatie en percentagedistributie zie [Handmatige correcties aanbrengen in de basislijnprognose](manual-adjustments-baseline-forecast.md) Voor elke maateenheid die wordt gebruikt voor voorraadeenheden die worden opgenomen in de vraagprognose, moet u ervoor zorgen dat er een conversieregel voor de maateenheid en de algemene maateenheid van de prognose is. Als prognose aanmaken wordt uitgevoerd, wordt de lijst met artikelen die geen maateenheidsconversie hebben geregistreerd, zodat u de installatie gemakkelijk kunt verbeteren. 

Vraagprognoses kunnen worden gebruikt voor prognoses van zowel afhankelijke als onafhankelijke vraag. Als bijvoorbeeld alleen het selectievakje **Verkooporder** is ingeschakeld en als alle artikelen die voor de vraagprognose worden beschouwd, artikelen zijn die worden verkocht, berekent het systeem onafhankelijke vraag. Kritieke subcomponenten kunnen echter worden toegevoegd aan artikeltoewijzingssleutels en worden opgenomen in vraagprognoses. In dit geval, als het selectievakje **Productieregel** is ingeschakeld, wordt een afhankelijke prognose berekend. 

Er zijn twee methoden voor het maken van een basislijn prognose in Dynamics 365 voor bewerkingen. U kunt prognosemodellen naast historische gegevens gebruiken of u kunt ze eenvoudig over de historische gegevens naar de prognose kopiëren. In het veld **Strategie voor aanmaken van vraagprognose** kunt u tussen deze twee methoden kiezen. Selecteer om prognosemodellen te gebruiken **Azure Machine Learning**. 

Door te klikken op **Prognosedimensies** in het linkerdeelvenster van de pagina **Parameters voor vraagprognose** kunt u de set prognosedimensies selecteren om te gebruiken wanneer de vraagprognose wordt gegenereerd. Een prognosedimensie geeft het detailniveau aan waarvoor de prognose is gedefinieerd. Bedrijf, site en artikeltoewijzingssleutel zijn verplichte prognosedimensies, maar u kunt prognoses ook genereren op het niveau van het magazijn, de voorraadstatus, de klantgroep, de klantrekening, het land/de regio, de status, het artikel en alle artikeldimensieniveaus. 

U kunt op elk moment prognosedimensies toevoegen aan de lijst met dimensies die voor vraagprognoses worden gebruikt. U kunt ook eventueel prognosedimensie uit de lijst verwijderen. Handmatige correcties gaan echter verloren als u een prognosedimensie toevoegt of verwijdert. 

Niet alle artikelen gedragen zich op dezelfde vanuit een vraagprognoseperspectief. Vergelijkbare artikelen kunnen in één artikeltoewijzingssleutel worden gegroepeerd, en de parameters zoals transactietypen en de instellingen voor de prognosemethode kunnen per artikeltoewijzingssleutel worden ingesteld. Klik op **Artikeltoewijzingssleutels** in het linkerdeelvenster van de pagina **Parameters voor vraagprognose**. 

Dynamics 365 for Operations gebruikt voor het genereren van de prognose, een webservice Machine leren. Als u wilt verbinding maken met de service, moet u opgeven Dynamics 365 voor bewerkingen de volgende informatie als u bij Microsoft Azure Machine Learning Studio aanmelden:

-   Application Programming Interface (API)-sleutel voor webservice
-   Eindpunt-URL webservice
-   Azure-naam van opslagaccount
-   Azure-sleutel van opslagaccount

**Opmerking:** De Azure-opslagaccountnaam en sleutel zijn alleen vereist wanneer u een aangepast opslagaccount gebruikt. Als u de versie op lokalen implementeert, hebt u moet een account aangepaste opslag op Azure, zodat de Machine Learning-service toegang heeft tot de historische gegevens. 

U kunt uw eigen service via Machine Learning Studio of de Dynamics 365 voor bewerkingen vraag prognoses experimenten implementeren voor het maken van prognoses van de vraag. Instructies voor het implementeren van de Dynamics 365 voor bewerkingen vraag experimenten prognoses als webservice zijn beschikbaar voor Dynamics 365 voor bewerkingen. Op de pagina **Parameters voor vraagprognose** klikt u op het tabblad **Azure Machine Learning**.

## <a name="settings-for-the-dynamics-365-for-operations-demand-forecasting-machine-learning-service"></a>Instellingen voor de Dynamics 365 for Operations vraag opdrachtgever machine learning-service
De parameters die kunnen worden geconfigureerd voor de Dynamics 365 voor bewerkingen vraag opdrachtgever service, Ga naar **hoofdplanning**&gt;**Setup**&gt;**vraagprognose**&gt;**prognoses van de parameters van algoritme**. De **prognoses van de parameters van algoritme** pagina worden de standaardwaarden voor de parameters. U kunt deze parameters overschrijven in de **vraag prognoses van de parameters** pagina. Gebruik het tabblad **Algemeen** om de parameters globaal te overschrijven, of gebruik het tabblad **Artikeltoewijzingssleutels** om de parameters per artikeltoewijzingssleutel te overschrijven. De parameters die voor een artikeltoewijzingssleutel worden overschreven beïnvloeden alleen de prognose van artikelen die aan de artikeltoewijzingssleutel zijn gekoppeld.

<a name="see-also"></a>Zie ook
--------

[Introduction to demand forecasting](introduction-demand-forecasting.md)

[Generating a statistical baseline forecast](generate-statistical-baseline-forecast.md)

[Making manual adjustments to the baseline forecast](manual-adjustments-baseline-forecast.md)


