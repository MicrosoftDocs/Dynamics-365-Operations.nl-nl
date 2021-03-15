---
title: Automatisch serviceorders maken
description: U kunt serviceorders genereren op basis van een serviceovereenkomst voor de periode waarin de serviceovereenkomst van kracht is.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 53369ef2b7ff93ae4f0523accbc31cc88575a383
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2021
ms.locfileid: "5010667"
---
# <a name="automatically-create-service-orders"></a>Automatisch serviceorders maken 

[!include [banner](../includes/banner.md)]


U kunt serviceorders genereren op basis van een serviceovereenkomst voor de periode waarin de serviceovereenkomst van kracht is.

De serviceorders die u van een serviceovereenkomst genereert, worden aan de serviceovereenkomst gekoppeld.

Serviceorders worden automatisch van de volgende instellingen gegenereerd:

  - Het interval dat voor de serviceovereenkomst op de serviceovereenkomstregels is ingesteld. Dat serviceovereenkomstinterval geeft de frequentie aan waarmee serviceorderregels worden gemaakt. Zie voor meer informatie [Service-intervallen](service-intervals.md).

  - De periode die u in de velden **Datum vanaf** en **Datum t/m** in het formulier **Serviceorders maken** opgeeft voor het specificeren van de serviceperiode. Zie voor meer informatie [Serviceorders automatisch maken](create-service-orders-automatically.md).

  - De optie **Serviceorders combineren** in de koptekst van de serviceovereenkomst. Met deze optie wordt aangegeven of serviceorderregels die worden gegenereerd vanuit een serviceovereenkomst, worden gecombineerd op werknemer, diensttaak, serviceobject of serviceovereenkomst. Zie voor meer informatie [Serviceorders combineren](combine-service-orders.md).

  - De optie **Tijdvenster** op de serviceovereenkomstregel. Door het tijdvenster wordt bepaald in hoeverre een serviceorderregel ten opzichte van de berekende datum kan worden verplaatst. Zie voor meer informatie [Tijdvensters](time-windows.md).


> [!NOTE]
> <P>Als de dag die voor een serviceorder is opgegeven, niet is geopend in de kalender die u in het formulier <STRONG>Parameters voor servicebeheer</STRONG> hebt geselecteerd, wordt er melding van een kalenderconflict gemaakt. U kunt dit bericht gewoon negeren. De serviceorder wordt gemaakt, ondanks dat de dag in het kalender is gesloten.</P>

## <a name="example-1"></a>Voorbeeld 1

De serviceovereenkomst loopt van 1 januari 2012 tot en met 31 december 2012. Als de serviceperiode die u hebt opgegeven in het formulier **Serviceorders maken** van 1 november 2012 tot en met 1 februari 2013 loopt, worden er toch alleen serviceorders gemaakt van 1 november 2012 tot en met 31 december 2012.

## <a name="example-2"></a>Voorbeeld 2

De serviceovereenkomst loopt van 1 januari 2012 tot en met 31 december 2012. Aan die serviceovereenkomst zijn twee serviceovereenkomstregels gekoppeld. De eerste serviceovereenkomstregel heeft een begindatum van 2 januari 2012 en een einddatum van 1 maart 2012. De tweede serviceovereenkomstregel heeft een begindatum van 1 april 2012 en een einddatum van 31 december 2012. U geeft in het formulier **Serviceorders maken** een periode op die loopt van 1 oktober 2012 tot en met 31 december 2012. Er worden alleen serviceorders gegenereerd voor de tweede overeenkomstregel, omdat de begin- en einddatum van de eerste overeenkomstregel vóór de periode liggen die u voor de serviceperiode hebt opgegeven.

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]