---
title: Pagina's naast elkaar weergeven met de functie Openen in nieuw venster
description: In dit artikel wordt uitgelegd hoe u pagina's naast elkaar kunt weergeven.
author: aneesmsft
manager: AnnBe
ms.date: 11/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.custom: 17611
ms.assetid: fc589d76-3927-4486-ab83-e86b9b47ba2c
ms.search.region: Global
ms.author: aneesa
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5b770fe44e4e12c515ca53def697fa345ce3eba3
ms.sourcegitcommit: f5e31c34640add6d40308ac1365cc0ee60e60e24
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/08/2020
ms.locfileid: "4694440"
---
# <a name="show-pages-side-by-side-using-the-open-in-new-window-feature"></a>Pagina's naast elkaar weergeven met de functie Openen in nieuw venster

[!include [banner](../includes/banner.md)]

In dit artikel wordt uitgelegd hoe u pagina's naast elkaar kunt weergeven.

U kunt meerdere pagina's naast elkaar bekijken om taken snel te voltooien. Als voorbeeld kunt u regels in meer dan één journaal bijvoorbeeld valideren of invoeren. Doorgaans kunt u regels in meer dan één journaal valideren of invoeren door vooruit en terug te gaan naar de pagina die een lijst met journalen weergeeft en de pagina die regels voor een bepaald journaal weergeeft. Echter, met de functie **Openen in nieuw venster** kunt u deze pagina's naast elkaar weergeven zodat u snel uw taken kunt uitvoeren.

Om door te gaan met het bovenstaande voorbeeld, klikt u tijdens het weergeven van de regels op het pictogram **Openen in nieuw venster**.

[![Klik op het pictogram Openen in nieuw venster.](./media/open-in-new-window-icon.png)](./media/open-in-new-window-icon.png)

Als u klikt op het pictogram **Openen in nieuw venster**, wordt de regelspagina geopend in een nieuwe pop-upbrowser en navigeert vervolgens naar de oorspronkelijke browser terug naar de pagina die de lijst met journalen toonde. U kunt beide pagina's naast elkaar weergeven. Wanneer u een journaal hebt bekeken, kunt u het geselecteerde journaal wijzigen op de pagina met de journaallijst, en de regelspagina in het pop-upvenster geeft automatisch de regels van het geselecteerde journaal weer.

[![U kunt vervolgens pagina's naast elkaar weergeven.](./media/pages-show-side-by-side.png)](./media/pages-show-side-by-side.png)

De dynamische koppeling en vernieuwing gebeurt vanwege de relaties tussen de gegevens die deze pagina's ondersteunen. Als het systeem niet bewust is van de relatie tussen de gegevens, wordt het pop-upvenster niet automatisch vernieuwd in reactie op een wijziging in het venster waaruit het afkomstig is.

Sommige pagina's hebben meerdere weergaven zoals de Rasterweergave, Kopweergave en Detailsweergave. Het pictogram **Openen in nieuw venster** zorgt ervoor dat de volledige pagina wordt geopend in het nieuwe browservenster. Daarom kunt u niet twee weergaven van dezelfde pagina naast elkaar behouden met de functie **Openen in nieuw venster**. Echter, bijna alle pagina's hebben een navigatielijst die u kunt gebruiken om tussen records te schakelen om een vergelijkbare ervaring te bereiken.

Voordat u de functie **Openen in nieuw venster** kunt gebruiken, moet u de pop-upblokkering van uw browser zo instellen dat pop-ups van de URL van de site zijn toegestaan. U kunt bijvoorbeeld pop-ups van "\*.dynamics.com" toestaan.

De functie **Openen in nieuw venster** is alleen beschikbaar wanneer er meer dan een pagina is geopend in het venster. Het pop-upvenster wordt ook automatisch gesloten wanneer er geen pagina's meer open zijn (dat wil zeggen wanneer de laatste pagina in dat venster wordt gesloten). Het systeem sluit ook open pagina´s wanneer u navigeert naar een ander gedeelte in de toepassing. Als u dus open pop-upvensters hebt en naar een ander gedeelte in de toepassing navigeert, worden de pop-upvensters automatisch afgesloten omdat de pagina's in die venster door het systeem werden gesloten.

De bovenste balk in de pop-upvensters tonen informatie over het bedrijf waarin de pagina is geopend en is alleen-lezen. De pop-upvensters zijn ook afhankelijk van het hoofdbrowservenster. Als het hoofdvenster wordt gesloten of vernieuwd, worden alle openstaande pop-upvensters alleen-lezen. Als deze situatie zich voordoet, kunt u de informatie in deze vensters nog steeds bekijken, maar is er geen interactie mogelijk.
