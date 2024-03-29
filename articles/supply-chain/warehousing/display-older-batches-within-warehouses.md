---
title: Weergave oudere batches in magazijn op een mobiel apparaat configureren
description: In dit artikel wordt beschreven hoe u een mobiel apparaat instelt voor het weergeven van locaties met batches die ouder zijn dan de huidige locatie van een werkregel.
author: Mirzaab
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSRFMenuItem
audience: Application User
ms.reviewer: kamaybac
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5788b42483f2c3046b0d20f45115b98d62cce213
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8900530"
---
# <a name="configure-display-older-batches-within-warehouse-on-a-mobile-device"></a>Weergave oudere batches in magazijn op een mobiel apparaat configureren

[!include [banner](../includes/banner.md)]

Met de configuratie van **Weergave oudere batches in magazijn** kunt u een lijst met locaties weergeven met batches die ouder zijn dan de huidige locatie van de werkregel. De lijst met locaties die wordt weergegeven bevat informatie over de batches die ouder zijn op de locatie met de vervaldatum en de fysieke voorraad van elke batch. U kunt kiezen om uit een nieuwe locatie te verzamelen of door te gaan met de huidige locatie. 
- In een nieuwe locatie verzamelen: als u een nieuwe locatie voor het verzamelen selecteert, wordt de huidige werkregel bijgewerkt met de nieuwe locatie en wordt het werk zoals gebruikelijk voortgezet met de nieuwe locatie. De nieuwe locatie is alleen geldig als er een voldoende beschikbare hoeveelheid is voor de hele werkregel. Als de vereiste hoeveelheid niet beschikbaar is, wordt de werkregel niet bijgewerkt en wordt de lijst weergegeven. 
- Doorgaan met orderverzamelen van de huidige locatie: als u met de huidige locatie van de werkregel doorgaat, worden de hoeveelheden voor de werkregel van de oorspronkelijke locatie verzameld.

## <a name="where-it-applies"></a>Waar van toepassing
Oudere batches in magazijn weergeven wordt geconfigureerd in menuopties van mobiele apparaten en beïnvloedt het verzamelen voor de onderste artikelen in de batch.

## <a name="set-up-display-older-batches-within-warehouse"></a>Weergave oudere batches in magazijn instellen
De configuratie **Weergave oudere batches in magazijn** is beschikbaar in menuopties van mobiele apparaten wanneer de optie **Oudste batch verzamelen** is ingesteld op **Waarschuwen**.

- Stel onder **Magazijnbeheer** > **Instellingen** > **Mobiel apparaat** > **Menuopties voor mobiel apparaat** de menuoptie **Bestaand werk gebruiken** in op **Ja** en selecteer **Waarschuwen** in het veld **Oudste batch verzamelen**. 



[!INCLUDE[footer-include](../../includes/footer-banner.md)]