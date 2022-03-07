---
title: Een productieorder vrijgeven
description: Deze procedure laat zien hoe u een productieorder vrijgeeft.
author: johanhoffmann
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ProdTableListPage, ProdParmRelease, SrsReportViewerForm, ProdSetupRelease
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f6d0db7f93e113d8f41effd68ce19aa065b031fd
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/29/2021
ms.locfileid: "7573652"
---
# <a name="release-a-production-order"></a>Een productieorder vrijgeven

[!include [banner](../../includes/banner.md)]

Deze procedure laat zien hoe u een productieorder vrijgeeft. Het bedrijf van de demogegevens dat wordt gebruikt om deze procedure te maken is USMF. Dit is de vierde procedure van zeven die de productieorderlevenscyclus beschrijven.

1. Ga naar Productiebeheer > Productieorders > Alle productieorders.
    * Selecteer in het raster een productieorder met de status Gepland.  
2. Klik in het actievenster op Productieorder.
3. Klik op Vrijgave.
    * Op deze pagina kunt u de vrijgave bevestigen van het geselecteerde bereik van productieorders. Klik op Selecteren als u orders wilt toevoegen.  
    * De stap Vrijgave geeft aan wanneer de productieorder aan de werkvloer van productie wordt vrijgegeven zodat de werkvloeroperators de voortgang van productietaken kunnen melden. Productiedocumenten die relevante informatie over het verwerken van de taken bevatten kunnen worden uitgegeven. Het magazijnwerk voor het verzamelen van grondstoffen wordt gegenereerd voor de artikelen die voor het magazijnproces zijn ingesteld.  
4. Klik op het tabblad Algemeen.
    * Selecteer welke productierapporten moeten worden afgedrukt. Het taakkaartrapport drukt een pagina af voor elke geplande taak en vereist dat de productieorder wordt gepland op taakniveau. Het rapport bevat informatie over de geplande begin- en eindtijd, de te produceren hoeveelheid en welke resource de taak verwerkt. Het routetaakrapport verzamelt dezelfde informatie over dezelfde pagina, maar drukt geen pagina af voor elke taak. Het routekaartrapport geeft alleen de bewerkingen weer maar niet de taken. Daarom vereist dit rapport geen taakplanning, maar kan het worden gebruikt wanneer productieorders op het bewerkingsniveau worden gepland.  
5. Klik op het selectievakje Routekaart afdrukken.
6. Klik op OK.
7. Sluit de pagina.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]