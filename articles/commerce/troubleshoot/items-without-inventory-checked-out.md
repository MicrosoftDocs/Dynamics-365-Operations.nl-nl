---
title: Artikelen zonder voorraad kunnen worden uitgecheckt
description: Dit onderwerp biedt richtlijnen voor probleemoplossing die u kunnen helpen wanneer klanten artikelen uit voorraad aan hun winkelwagentje kunnen toevoegen en kunnen uitchecken.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 4fa7769044c45faffd9ff61b3de8e6217a5e0354
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/11/2021
ms.locfileid: "6018453"
---
# <a name="items-without-inventory-can-be-checked-out"></a>Artikelen zonder voorraad kunnen worden uitgecheckt

[!include [banner](../../includes/banner.md)]

Dit onderwerp biedt richtlijnen voor probleemoplossing die u kunnen helpen wanneer klanten artikelen uit voorraad aan hun winkelwagentje kunnen toevoegen en kunnen uitchecken.

## <a name="description"></a>Beschrijving

Gebruikers kunnen een artikel aan hun winkelwagentje toevoegen, zelfs als er geen voorhanden voorraad is in de winkel, en vervolgens doorgaan naar de uitcheckpagina.

## <a name="resolution"></a>Oplossing

### <a name="enable-the-show-out-of-stock-errors-property-in-commerce-site-builder"></a>De eigenschap Fouten voor niet op voorraad weergeven inschakelen in Commerce Site Builder

Voer deze stappen uit om de eigenschap **Fouten voor niet op voorraad weergeven** inschakelen in Commerce Site Builder.

1. Selecteer de site waaraan u werkt.
1. Selecteer **Pagina's** in het navigatievenster aan de linkerkant.
1. Selecteer **CartPage** om deze te openen.
1. Selecteer het vak **Winkelwagen 1**, selecteer **Bewerken** en schakel vervolgens, in het eigenschappenvenster, het selectievakje **‭Fouten voor niet op voorraad weergeven** in.
1. Sla de pagina op en publiceer deze.

## <a name="additional-resources"></a>Aanvullende bronnen

[Voorraadinstellingen toepassen](../inventory-settings.md)

[Voorraadbeschikbaarheid voor Retail-kanalen berekenen](../calculated-inventory-retail-channels.md)

[Voorraadbuffers en voorraadniveaus configureren](../inventory-buffers-levels.md)
