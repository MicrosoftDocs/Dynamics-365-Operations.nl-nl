---
title: Een productieorder vrijgeven
description: Deze procedure laat zien hoe u een productieorder vrijgeeft.
author: johanhoffmann
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProdTableListPage, ProdParmRelease, SrsReportViewerForm, ProdSetupRelease
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: beef850e7e58fb58db545c0be5990b52619070d3
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/13/2020
ms.locfileid: "4425139"
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