---
title: Stuklijst- en formuleregels vrijgeven aan het magazijn
description: In dit onderwerp wordt het proces voor het vrijgeven van grondstoffen voor stuklijst- en formuleregels aan het magazijn beschreven.
author: johanhoffmann
manager: AnnBe
ms.date: 10/30/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SysOperationTemplateForm
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 1705903
ms.search.region: Global
ms.author: johanho
ms.search.validfrom: 2017-12-31
ms.dyn365.ops.version: 7.3
ms.translationtype: HT
ms.sourcegitcommit: 72d4ff5e1311005d3bf43a13e28208cd9b3d1457
ms.openlocfilehash: 838dc1e5867b8380823275aba5fc425003a54523
ms.contentlocale: nl-nl
ms.lasthandoff: 03/07/2018

---

# <a name="release-bom-and-formula-lines-to-the-warehouse"></a>Stuklijst- en formuleregels vrijgeven aan het magazijn

[!include[banner](../includes/banner.md)]

In dit onderwerp wordt het proces voor het vrijgeven van grondstoffen voor stuklijst- en formuleregels aan het magazijn beschreven. Wanneer u een stuklijst- of formuleregel aan het magazijn vrijgeeft, bepaalt het systeem eerst of er al materiaal beschikbaar is op de productie-invoerlocatie op de werkvloer waar het materiaal voor het productieproces wordt verbruikt.

- Als het materiaal beschikbaar is op de productie-invoerlocatie, wordt het materiaal van die locatie verzameld direct nadat het signaal voor de vrijgave van materiaal aan het magazijn is gegeven.
- Als het materiaal niet beschikbaar is op de productie-invoerlocatie, wordt met de materiaalvrijgave aangegeven dat materiaal van locaties in het magazijn moet worden verplaatst naar de productie-invoerlocatie. Het materiaal wordt verplaatst via magazijnwerk voor het verzamelen van grondstoffen. Daarom moeten er magazijnprocessen voor het verzamelen van grondstoffen worden geconfigureerd. Zie voor meer informatie [Aanvulling](../warehousing/replenishment.md) en [Magazijnwerk beheren met werksjablonen en locatierichtlijnen](../warehousing/control-warehouse-location-directives.md).

## <a name="methods-for-releasing-bom-and-formula-lines"></a>Methoden voor het vrijgeven van stuklijst- en formuleregels

U kunt de vrijgave van stuklijst- en formuleregels configureren zodat dit als onderdeel van de vrijgave van een productie- of batchorder plaatsvindt. De vrijgave kan ook worden beheerd met een batchtaak of handmatig worden uitgevoerd.

De methode voor het vrijgeven van stuklijst- en formuleregels wordt beheerd op basis van de parameter **Vrijgave van productielijn**. U vindt deze parameter via **Productiebeheer** \> **Instelling** \> **Productieparameters**.

- **Stuklijst- en formuleregels vrijgeven als onderdeel van vrijgave van productie- of batchorder**: bij deze methode worden stuklijst- en formuleregels voor een productie- of batchorder vrijgegeven als onderdeel van het proces voor het vrijgeven van de order. Normaal gesproken worden tijdens de vrijgave van een productie- of batchorder productietaken vrijgegeven aan de werknemers op de werkvloer en worden productiedocumenten afgedrukt. Tijdens dit proces wordt de status van de order gewijzigd in **Vrijgegeven**.
- **Stuklijst- en formuleregels via een batchtaak of handmatige vrijgeven**: bij deze methode kunnen stuklijst- en formuleregels alleen handmatig of via de batchtaak **Automatische vrijgave van stuklijst en formuleregels** worden vrijgegeven. Als u stuklijst- en formuleregels handmatig wilt vrijgeven, selecteert u op de lijst- of detailpagina van de productieorder in het actievenster de optie **Vrijgave naar magazijn**.

Bekijk deze korte YouTube-video voor een snelle demonstratie van het vrijgeven van stuklijst- en formuleregels voor productie met behulp van een batchtaak:
[!Video https://www.youtube.com/embed/8urAJn50dQ8]

## <a name="releasing-the-bom-and-formula-lines-by-using-a-batch-job"></a>De stuklijst- en formuleregels vrijgeven met een batchtaak

De batchtaak **Automatische vrijgave van stuklijst en formuleregels** doorloopt de geselecteerde stuklijst- en formuleregels met een resterende vrij te geven hoeveelheid. Alleen orders met de status **Vrijgegeven**, **Gestart** of **Gereedgemeld** worden gecontroleerd. Als een stuklijst- of formuleregel een resterende vrij te geven hoeveelheid bevat, wordt de hoeveelheid vrijgegeven die kan worden gedekt door de hoeveelheid die al fysiek is gereserveerd en de hoeveelheid die fysiek beschikbaar is.

### <a name="example-of-a-batch-job-release"></a>Voorbeeld van een batchtaakvrijgave

| Scenario's | Resterende hoeveelheid voor vrijgave | Fysieke gereserveerde hoeveelheid | Beschikbare fysieke hoeveelheid | Hoeveelheid die door de batchtaak wordt vrijgegeven |
|----------|-------------------------------|------------------------------|-------------------------------|------------------------------------|
| 1        | 100                           | 20                           | 90                            | 100                                |
| 2        | 100                           | 20                           | 70                            | 90                                 |
| 3        | 100                           | 0                            | 90                            | 90                                 |
| 4        | 100                           | 0                            | 110                           | 100                                |
| 5        | 100                           | 20                           | 0                             | 20                                 |

### <a name="batch-job-setup"></a>Instellingen van batchtaak

In de query voor de batchtaak **Automatische vrijgave van stuklijst en formuleregels** kunt u een filtercriterium instellen om op te geven hoeveel dagen van tevoren er moet worden gezocht naar regels met niet-vrijgegeven hoeveelheden. Gebruik in de query voor de taak in het **Datum van grondstoffen** de functie **(LessThanDate())** als een filtercriterium.

In de volgende afbeelding ziet u een productieorder met twee taken, 10 en 20, die betrekking hebben op de assemblage en verpakking voor de productieorder. Elke taak is ingesteld om een hoeveelheid materiaal te verbruiken. In deze afbeelding staat de time fence voor vrijgave, die wordt aangeduid door de groene pijl onder tijdlijn, gelijk aan het aantal dagen dat is opgegeven in het criterium **(LessThanDate())**. **(LessThanDate(2))** geeft bijvoorbeeld aan dat met de taak alleen moet worden gezocht naar niet-vrijgegeven hoeveelheden binnen een time fence van twee dagen.

![Voorbeeld van een productieorder met twee batchtaken](media/bach-job-setup.PNG)

## <a name="releasing-material-per-operation-number-or-in-proportion-to-the-amount-of-finished-goods"></a>Materiaal per bewerkingsnummer of in verhouding tot het aantal eindproducten vrijgeven

Als u materialen vrijgeeft op basis van de parameterinstelling **Bij vrijgave van productieorder**, hebt u bij een handmatige vrijgave twee mogelijkheden voor het beheren van de materiaalvrijgave:

- Materiaal op bewerkingsnummer vrijgeven.
- Materiaal vrijgeven in verhouding tot het aantal eindproducten.

### <a name="release-material-per-operation-number"></a>Materiaal op bewerkingsnummer vrijgeven

Als u wilt beheren voor welke bewerkingen materiaal moet worden vrijgegeven, gaat u naar de pagina **Vrijgave naar magazijn**.

- Selecteer **Productiebeheer** \> **Productieorders** \> **Alle productieorders**, selecteer een productieorder en selecteer op het tabblad **Magazijn** de optie **Vrijgave naar magazijn**. Gebruik vervolgens de velden **Van bewerkingsnummer** en **Tot bewerkingsnummer** om het bereik aan bewerkingsnummers op te geven.

In de volgende afbeelding wordt een productieorder met de twee bewerkingen 10 en 20 weergegeven. In dit voorbeeld wordt alleen het materiaal M9203 vrijgegeven als u de vrijgave beperkt tot bewerking 10.

![Voorbeeld van de vrijgave van materiaal op bewerkingsnummer](media/two-operations.PNG)

Bekijk deze korte YouTube-video voor een snelle demonstratie van het vrijgeven van materiaal in verhouding tot de hoeveelheid eindproducten:
[!Video https://www.youtube.com/embed/Rm3ojAz6Zu0]

### <a name="release-material-in-proportion-to-the-amount-of-finished-goods"></a>Materiaal vrijgeven in verhouding tot het aantal eindproducten

U kunt grondstoffen voor een gedeeltelijke hoeveelheid van eindproducten of in een specifieke eenheid vrijgeven.

- Als u grondstoffen voor een gedeeltelijke hoeveelheid van eindproducten wilt vrijgeven, selecteert u **Productiebeheer** \> **Productieorders** \> **Alle productieorders**, selecteert u een productieorder en selecteert u op het tabblad **Magazijn** de optie **Vrijgave naar magazijn**. Voer in het veld **Hoeveelheid** een hoeveelheid in.

    Er kan bijvoorbeeld een productieorder worden gemaakt en gepland voor 1000 stuks. De werkvloersupervisor plant de productie van 100 stuks voor de volgende ploegendienst en wil alleen materialen vrijgeven voor die ploegendienst. In dit geval kan de supervisor het veld **Hoeveelheid** gebruiken voor het vrijgeven van materialen voor de 100 stuks die zijn gepland voor de volgende ploegendienst.

- Als u grondstoffen in een specifieke eenheid wilt vrijgeven, selecteert u **Productiebeheer** \> **Productieorders** \> **Alle productieorders**, selecteert u een productieorder en selecteert u op het tabblad **Magazijn** de optie **Vrijgave naar magazijn**. Gebruik vervolgens het veld **Eenheid** om de eenheid te selecteren waarin het materiaal voor het eindproduct moet worden vrijgegeven.

    De eenheden die beschikbaar zijn, worden gedefinieerd in de volgordegroep-id voor de eenheid van het eindproduct.

    Voor een eindproduct kan bijvoorbeeld de volgende eenheidsomrekening tussen kilo's (kg) en pallets (PL) bestaan: 1 PL = 100 kg. Als u een productieorder voor 10.000 kg van het eindproduct wilt maken, kunt u grondstoffen vrijgeven voor het aantal pallets dat u wilt produceren. Selecteer **PL** als de eenheid en selecteer vervolgens de bijbehorende waarde in het veld **Hoeveelheid**.

