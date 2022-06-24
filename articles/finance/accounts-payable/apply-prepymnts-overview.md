---
title: Automatisch vooruitbetalingen op leveranciersfacturen toepassen
description: In dit artikel wordt beschreven hoe u automatisch vooruitbetalingen op leveranciersfacturen toepast.
author: sunfzam
ms.date: 10/19/2021
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.assetid: ''
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2017-08-30
ms.dyn365.ops.version: 10.0.23
ms.openlocfilehash: 547573d187460a900df7f4927ac062bd9d456729
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8900066"
---
# <a name="automatically-apply-to-vendor-invoices"></a>Automatisch toepassen op leveranciersfacturen

[!include [banner](../includes/banner.md)]

In dit artikel wordt beschreven hoe u automatisch vooruitbetalingen op leveranciersfacturen toepast. Er kan een vooruitbetaling worden gemaakt voor een inkooporder als onderdeel van een inkoopovereenkomst. Nadat een leveranciersfactuur is ontvangen, kan de vooruitbetaling worden gebruikt om de te betalen rekeningen te vereffenen met de leveranciersfactuur. De nieuwe functie stelt het systeem in staat om automatisch inkoopordernummers op een leveranciersfactuur te gebruiken om overeenkomende vooruitbetalingen op te zoeken wanneer de leveranciersfactuur wordt geïmporteerd.

Als er vooruitbetalingen worden gevonden en kunnen worden toegepast, worden regels toegevoegd aan de bestaande factuurregels om de vooruitbetalingen toe te passen. Tijdens het factuurvereffeningsproces wordt nooit rekening gehouden met de vooruitbetalingregels.

In de volgende punten wordt beschreven hoe vooruitbetalingen worden toegepast wanneer er verschillende inkoopprocessen worden gevolgd:

- **Eén leveranciersfactuur per inkooporder**: de vooruitbetaling op de inkooporder wordt toegepast op de leveranciersfactuur.
- **Eén leveranciersfactuur voor meerdere inkooporders**: de vooruitbetalingen op alle inkooporder worden toegepast op de leveranciersfactuur.
- **Meerdere leveranciersfacturen per inkooporder**: de vooruitbetaling op de inkooporder wordt toegepast op de als eerste geïmporteerde leveranciersfactuur. Als het vooruitbetalingsbedrag hoger is dan het factuurbedrag, mislukt de vooruitbetalingsaanvraag en moet u de vooruitbetaling handmatig toepassen.
- **Meerdere leveranciersfacturen voor meerdere inkooporders**: de vooruitbetalingen op de inkooporders wordt toegepast op de eerste relevante leveranciersfactuur. Als het vooruitbetalingsbedrag hoger is dan het factuurbedrag, mislukt de vooruitbetalingsaanvraag en moet u de vooruitbetalingen handmatig toepassen. Als eventuele vooruitbetalingen die overblijven nadat vooruitbetalingen zijn toegepast op de eerste factuur, kunnen deze worden toegepast op de facturen die volgen.

Als een poging tot vooruitbetaling mislukt, zijn de volgende stappen afhankelijk van de instelling van de optie **Automatisch opvolgingsproces blokkeren bij fout in toepassing van vooruitbetaling**:

- **Ja**: het foutbericht Automatische toepassing van vooruitbetaling: Mislukt wordt toegevoegd aan de automatiseringsgeschiedenis en de factuur blijft in de lijst met leveranciersfacturen die in behandeling zijn. De factuur blijft geblokkeerd totdat u de vooruitbetaling handmatig toepast.

Ga naar de leveranciersfactuur in behandeling om vooruitbetalingen handmatig toe te passen. Stel op de pagina **Factuurdetails** de optie **Opnemen in automatische verwerking** voor de geblokkeerde factuur in op **Nee**. U kunt de vooruitbetaling nu handmatig toepassen. Nadat de vooruitbetaling is toegepast, stelt u de optie **Opnemen in automatische verwerking** weer in op **Ja** zodat de factuur automatisch kan worden verwerkt.

U kunt de automatische toepassing van de vooruitbetaling ook overslaan door de optie **Opnemen in automatische verwerking** in te stellen op **Nee** en de vooruitbetaling vervolgens weer in te stellen op **Ja**. Het volgende bericht wordt weergegeven: 'Er bestaat al een vooruitbetaling voor de inkooporder. Wilt u deze negeren voor de geselecteerde leveranciersfactuur?' Selecteer **Ja**. Het bericht Toepassing van vooruitbetaling wordt handmatig overgeslagen is toegevoegd in de automatiseringsgeschiedenis en de leveranciersfactuur wordt niet geblokkeerd wanneer het geautomatiseerde proces opnieuw wordt uitgevoerd.

- **Nee**: opvolgen van automatiseringsprocessen wordt voortgezet. U kunt de vooruitbetaling nog wel toepassen tijdens de vereffening.
