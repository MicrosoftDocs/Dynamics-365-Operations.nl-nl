---
title: Capaciteitsbelasting voor geplande werkorders berekenen
description: In dit artikel wordt uitgelegd hoe u capaciteitsbelasting kunt berekenen voor geplande werkorders in Activabeheer.
author: johanhoffmann
ms.date: 08/19/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 53b147198f6aa9e0254312e5ea48b9ae616a79a9
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8857948"
---
# <a name="calculate-capacity-load-on-scheduled-work-orders"></a>Capaciteitsbelasting voor geplande werkorders berekenen

[!include [banner](../../includes/banner.md)]

 

U kunt de capaciteitsbelasting voor geplande werkorders berekenen om een overzicht te krijgen van de werkbelasting van resources voor een specifieke periode. Er kunnen berekeningen worden uitgevoerd voor de volgende resources: onderhoudsmedewerkers, medewerkersgroepen, hulpmiddelen en activa.

1. Klik op **Activabeheer** > **Query's** > **Planning** > **Capaciteitsbelasting**.

2. Selecteer in het dialoogvenster **Capaciteitsbelasting berekenen** in het veld **Weergeven** het belastingtype dat u wilt berekenen: **Capaciteit**, **Gereserveerd** of **Rest**.

3. Selecteer **Ja** voor de wisselknop **Nul overslaan** als u geen resultaten voor nul wilt weergeven.

4. Selecteer de resourcetypen waarvoor u de capaciteitsbelasting wilt berekenen door **Ja** te selecteren voor de relevante wisselknoppen: **Medewerker**, **Onderhoudsmedewerkersgroep**, **Hulpmiddel** en **Activum**.

5. Selecteer de begindatum voor de berekening in het veld **Begindatum**.

6. Selecteer in het veld **Intervaltype** het interval voor de berekening: **Dag**, **Week**, **Maand** of **Kwartaal**.

7. In het veld **Periodefrequentie** voegt u het aantal intervallen in dat u wilt berekenen. Als u bijvoorbeeld **Dag** hebt geselecteerd als het type interval en u typt het getal 5 in dit veld, wordt er een berekening van vijf dagen vanaf de begindatum uitgevoerd.

8. Klik op **OK** om de berekening te starten.

De volgende afbeelding laat het resultaat zien van een berekening die drie weken omvat voor het belastingtype **Gereserveerd**.

![Figuur 1.](media/08-work-order-scheduling.png)

[!NOTE]
Als u het belastingtype **Capaciteit** of **Rest** selecteert voor de berekening, wordt hetzelfde resultaat weergegeven als er geen reserveringen zijn gemaakt voor de resources in de geselecteerde periode.

Zie [Capaciteitsbelasting berekenen](../capacity-planning/calculate-capacity-load.md) voor informatie over het berekenen van de capaciteitsbelasting voor onderhoudsschemaregels en niet geplande werkorders.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]