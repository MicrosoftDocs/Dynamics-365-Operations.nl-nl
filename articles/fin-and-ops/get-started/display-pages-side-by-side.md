---
title: Pagina's naast elkaar weergeven met het pictogram Openen in nieuw venster
description: In dit artikel wordt uitgelegd hoe u pagina's naast elkaar weergeeft in Microsoft Dynamics 365 for Finance and Operations.
author: aneesmsft
manager: AnnBe
ms.date: 09/07/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 17611
ms.assetid: fc589d76-3927-4486-ab83-e86b9b47ba2c
ms.search.region: Global
ms.author: aneesa
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 4a575665a2b893745a2f2044cd97177917ee1a33
ms.contentlocale: nl-nl
ms.lasthandoff: 11/03/2017

---

# <a name="display-pages-side-by-side-using-the-open-in-new-window-icon"></a>Pagina's naast elkaar weergeven met het pictogram Openen in nieuw venster

[!include[banner](../includes/banner.md)]


In dit artikel wordt uitgelegd hoe u pagina's naast elkaar weergeeft in Microsoft Dynamics 365 for Finance and Operations.

Microsoft Dynamics 365 for Finance and Operations helpt u om taken efficiënt uit te voeren. In sommige gevallen kunt u meerdere pagina's naast elkaar bekijken om taken snel te voltooien. Als voorbeeld kunt u regels in meer dan één journaal bijvoorbeeld valideren of invoeren. Doorgaans, om dit te doen moet u vooruit en terug gaan naar de pagina die een lijst met journalen weergeeft, en de pagina die regels voor een bepaald journaal weergeeft. Echter, met de functie **Openen in nieuw venster** kunt u deze pagina's naast elkaar weergeven zodat u snel uw taken kunt uitvoeren. 

Om door te gaan met het bovenstaande voorbeeld, klikt u tijdens het weergeven van de regels op het pictogram **Openen in nieuw venster**. 

[![Pictogram Openen in nieuw venster](./media/open-in-new-window-icon.png)](./media/open-in-new-window-icon.png) 

Als u klikt op het pictogram **Openen in nieuw venster**, wordt de regelspagina geopend in een nieuwe pop-upbrowser en navigeert vervolgens naar de oorspronkelijke browser terug naar de pagina die de lijst met journalen toonde. U kunt beide pagina's naast elkaar weergeven. Wanneer u een journaal hebt bekeken, kunt u het geselecteerde journaal wijzigen op de pagina met de journaallijst, en de regelspagina in het pop-upvenster geeft automatisch de regels van het geselecteerde journaal weer. 

[![Pagina's naast elkaar weergeven](./media/pages-show-side-by-side.png)](./media/pages-show-side-by-side.png) 

De dynamische koppeling en vernieuwing gebeurt vanwege de relaties tussen de gegevens die deze pagina's ondersteunen. Als het systeem niet bewust is van de relatie tussen de gegevens, wordt het pop-upvenster niet automatisch vernieuwd in reactie op een wijziging in het venster waaruit het afkomstig is. 

Sommige pagina's hebben meerdere weergaven zoals de Rasterweergave, Kopweergave en Detailsweergave. Het pictogram **Openen in nieuw venster** zorgt ervoor dat de volledige pagina wordt geopend in het nieuwe browservenster. Daarom kunt u niet twee weergaven van dezelfde pagina naast elkaar behouden met de functie **Openen in nieuw venster**. Echter, bijna alle pagina's hebben een navigatielijst die u kunt gebruiken om tussen records te schakelen om een vergelijkbare ervaring te bereiken. 

Voordat u de functie **Openen in nieuw venster** kunt gebruiken, moet u de pop-upblokkering van uw browser zo instellen dat pop-ups van de URL van Finance and Operations zijn toegestaan. U kunt bijvoorbeeld pop-ups van "\*.dynamics.com" toestaan. 

De functie **Openen in nieuw venster** is alleen beschikbaar wanneer er meer dan een pagina is geopend in het venster. Het pop-upvenster wordt ook automatisch gesloten wanneer er geen pagina's meer open zijn (dat wil zeggen wanneer de laatste pagina in dat venster wordt gesloten). Finance and Operations sluit ook open pagina´s wanneer u navigeert naar een ander gedeelte in de toepassing. Als u dus open pop-upvensters hebt en naar een ander gedeelte in de toepassing navigeert, worden de pop-upvensters automatisch afgesloten omdat de pagina's in die venster door het systeem werden gesloten. 

De bovenste balk in de pop-upvensters tonen informatie over het bedrijf waarin de pagina is geopend en is alleen-lezen. De pop-upvensters zijn ook afhankelijk van het Finance and Operations-browservenster. Als het hoofdvenster wordt gesloten of vernieuwd, worden alle openstaande pop-upvensters alleen-lezen. Dit betekent dat u de informatie in deze vensters kunt nog steeds kunt bekijken, maar er is geen interactie mogelijk.




