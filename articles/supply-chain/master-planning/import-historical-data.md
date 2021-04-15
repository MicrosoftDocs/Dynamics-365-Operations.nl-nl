---
title: Historische gegevens voor vraagprognoses importeren
description: Als u nauwkeurige vraagprognoses wilt, hebt u historische vraaggegevens per artikel of artikeltoewijzingssleutel nodig. In dit onderwerp wordt uitgelegd hoe u gegevensentiteiten gebruikt om historische vraaggegevens te importeren uit een willekeurig systeem, zodat u een langere historie van vraagprognosegegevens hebt.
author: roxanadiaconu
ms.date: 05/10/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqDemPlanCreateForecastDialog
audience: Application User
ms.reviewer: kamaybac
ms.assetid: 59c0d269-9db0-48e7-b8c7-9a388781a9ca
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9bb3c178a698bdcd46e7c596247360ba9233b398
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/01/2021
ms.locfileid: "5816479"
---
# <a name="import-historical-data-for-demand-forecasts"></a>Historische gegevens voor vraagprognoses importeren

[!include [banner](../includes/banner.md)]

Om te helpen de nauwkeurigheid van vraagprognoses te garanderen moet u zoveel mogelijk historische vraaggegevens hebben per artikel of artikeltoewijzingssleutel. Als de historische vraaggegevens niet al zijn geïmporteerd, gebruikt u de gegevensentiteit **Historische externe vraag** (ReqDemPlanHistoricalExternalDemandEntity) in Dynamics 365 Supply Chain Management om deze te importeren.

In het werkgebied **Gegevensbeheer** ziet u een overzicht van alle velden in de entiteit.

1. Open het werkgebied **Gegevensbeheer**.
2. Selecteer de tegel **Gegevensentiteiten**.
3. Zoek in de entiteitlijst naar **Historische externe vraag**.
4. Selecteer **Doelvelden**. De volgende entiteitvelden zijn verplicht: locatie (**DeliveringSiteId**), datum (**DemandDate**), hoeveelheid (**DemandQuantity**) en artikelnummer (**ItemNumber**) of artikeltoewijzingssleutel (**ProductAllocationKeyId**).

Als u de gegevensentiteit wilt gebruiken, moet u een Microsoft Excel-bestand of een door komma's gescheiden waarden (CSV)-bestand hebben met de historische vraaggegevens. Het volgende voorbeeld laat zien hoe u gegevens importeert uit een CSV-bestand.

Zie [Gegevensimport- en exporttakenoverzicht](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md) en de gerelateerde onderwerpen voor meer informatie over het importeren van gegevens, waaronder het opschonen van gegevens na een import.

## <a name="example"></a>Voorbeeld

U kunt het volgende bestand als voorbeeld gebruiken. Download de [HistoricalDemandData](https://docs.microsoft.com/dynamics/s-e/). Dit bestand bevat de historische vraaggegevens voor artikel D0001. Het bevat alleen de volgende verplichte velden: locatie, hoeveelheid en vraagdatum.

1. Selecteer het bedrijf waarin de historische vraaggegevens moeten worden geïmporteerd.
2. Open het werkgebied **Gegevensbeheer**.
3. Selecteer de tegel **Importeren**.
4. Voer een naam voor het importproject in, zoals **Historische vraag importeren voor artikel D0001**.
5. Selecteer in het veld **Brongegevensindeling** de bestandsindeling van het bestand dat u importeert. Als u het bestand HistoricalDemandData voor dit voorbeeld wilt importeren, selecteert u **CSV**.
6. Selecteer in het veld **Entiteit** **Historische externe vraag**.
7. Sla het bestand op uw computer op en upload het vervolgens.
8. Selecteer **Importeren**.
9. De pagina **Uitvoeringsoverzicht** wordt automatisch geopend. Controleer de geïmporteerde gegevens op de pagina.

Nadat u de historische vraaggegevens hebt geïmporteerd, kunt u een vraagprognose genereren.

## <a name="additional-resources"></a>Aanvullende bronnen

[Een statistische basislijnprognose genereren](generate-statistical-baseline-forecast.md)  
[Overzicht van Gegevensimport- en exporttaken](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]