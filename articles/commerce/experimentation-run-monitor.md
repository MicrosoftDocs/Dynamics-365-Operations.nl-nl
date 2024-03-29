---
title: Een experiment uitvoeren en controleren
description: In dit artikel wordt beschreven hoe u een experiment in een service van derden uitvoert en controleert. Verder wordt beschreven hoe u wijzigingen aanbrengt in variaties nadat het experiment is gestart.
author: sushma-rao
ms.date: 10/21/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: sushmar
ms.search.validFrom: 2020-09-30
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: c9f62c97b46fa00791de52b2804dad5edde7f625
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8909578"
---
# <a name="run-and-monitor-an-experiment"></a>Een experiment uitvoeren en controleren

In dit artikel wordt beschreven hoe u uw experiment in een app van derden uitvoert en controleert en zo nodig variaties wijzigt. Voordat u de stappen in dit artikel uitvoert, moet u uw experiment eerst [publiceren](experimentation-preview-publish.md) in Commerce. 

In het volgende diagram ziet u alle stappen voor het instellen en uitvoeren van een experiment op een e-Commerce-website in Dynamics 365 Commerce. Extra stappen worden in afzonderlijke artikelen behandeld.

[ ![Traject van gebruiker voor experimenten - uitvoeren en controleren.](./media/experimentation_run_monitor.svg) ](./media/experimentation_run_monitor.svg#lightbox)

Nadat u uw variaties hebt gepubliceerd, zijn alle stappen gereed die u moet uitvoeren in Commerce om uw experiment uit te voeren. De volgende stap bestaat eruit te bepalen welke variatie wordt weergegeven voor elke gebruiker wanneer hij of zij een pagina aanvraagt. Dit wordt door de service van derden bepaald, maar eerst moet u het experiment binnen de service activeren. Omdat de stappen voor het activeren van een experiment van service tot service verschillen, moet u de instructies volgen die door uw service of provider zijn geleverd. Als het experiment niet wordt geactiveerd, zien gebruikers alleen de standaardversie van de pagina (er worden geen variaties weergegeven).

U moet het experiment lang genoeg blijven uitvoeren om gegevens te verzamelen voor statistisch geldige resultaten. Gebruik de service van derden om de experimentgerelateerde gegevens en analyse te controleren terwijl het experiment wordt uitgevoerd.

## <a name="adjust-your-variations"></a>Uw variaties aanpassen
Als u om welke reden dan ook wijzigingen moet aanbrengen in uw variaties, voert u de volgende stappen uit.

> [!IMPORTANT]
> Als u wijzigingen aanbrengt in een live experiment in Commerce of de service van derden, kunnen uw resultaten aanzienlijk worden beïnvloed. Overweeg om het experiment te laten uitvoeren en vervolgens een nieuw experiment te maken voor belangrijke wijzigingen.

1. Selecteer **Experimenten** in het linkernavigatievenster in Commerce Site Builder en selecteer het experiment vervolgens. 
1. Selecteer de variatie die u wilt bijwerken in het vervolgkeuzemenu.
1. Voer eventuele noodzakelijke wijzigingen door en bekijk vervolgens de variaties en publiceer deze. Zie [Preview van een experiment weergeven en een experiment publiceren](experimentation-preview-publish.md) voor meer informatie.
1. Ga naar de service van derden om alle wijzigingen aan te brengen die betrekking hebben op het instellen van het experiment.
    
## <a name="previous-step"></a>Vorige stap
[Preview van een experiment weergeven en een experiment publiceren](experimentation-preview-publish.md)

## <a name="next-step"></a>Volgende stap
[Een variant promoveren en een experiment voltooien](experimentation-review-complete.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]