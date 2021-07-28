---
title: Optie Dit ophalen wordt niet weergegeven op winkelwagen- of productdetailpagina's
description: Dit onderwerp bevat richtlijnen voor probleemoplossing die kunnen helpen wanneer de optie voor ophalen in een winkel niet wordt weergegeven op de winkelwagen- of productdetailpagina's.
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
ms.openlocfilehash: 3dd4eb576f234e4d75c08b0b5e2fe967500c8c93
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 07/06/2021
ms.locfileid: "6347291"
---
# <a name="pick-this-up-option-doesnt-appear-on-cart-or-product-details-pages"></a>Optie 'Dit ophalen' wordt niet weergegeven op winkelwagen- of productdetailpagina's

[!include [banner](../../includes/banner.md)]

Dit onderwerp bevat richtlijnen voor probleemoplossing die kunnen helpen wanneer de optie voor ophalen in een winkel niet wordt weergegeven op de winkelwagen- of productdetailpagina's.

## <a name="description"></a>Beschrijving

De knop **Dit ophalen** wordt niet weergegeven op de winkelwagen- of productdetailpagina's.

In de volgende afbeelding ziet u een voorbeeld van een pagina met de knop **Dit ophalen**.

![Knop Dit ophalen.](media/pickup-button-missing.jpg)

## <a name="resolution"></a>Oplossing

### <a name="enable-the-bopis-extension-in-commerce-site-builder"></a>De BOPIS-extensie inschakelen in Commerce Site Builder

Volg deze stappen om de extensie 'online kopen, ophalen in winkel' (BOPIS) in Commerce Site Builder in te stellen.

1. Selecteer uw site.
1. Selecteer **Site-instellingen** en selecteer vervolgens **Uitbreidingen**.
1. Zorg ervoor dat de optie **BOPIS uitschakelen** is uitgeschakeld.

### <a name="configure-modes-of-delivery-in-commerce-headquarters"></a>Leveringsmethoden configureren in Commerce Headquarters

Voer deze stappen uit om leveringsmethoden te configureren in Commerce Headquarters.

1. Ga naar **Inkoop en sourcing \> Instellingen \> Leveringsmethoden**.
1. Zorg ervoor dat er een leveringsmodus **Ophalen door klant** is gemaakt en dat er producten en adressen aan zijn toegewezen.
1. Ga naar **Retail en Commerce \> Instelling van hoofdkantoor \> Parameters**.
1. Selecteer **Klantorders** in het navigatievenster aan de linkerkant.
1. Controleer of **Ophaalmodus van levering** correct is geconfigureerd.

### <a name="configure-customer-orders-payments"></a>Betalingen van klantorders configureren

Voer deze stappen uit om betalingen van klantorders te configureren in Commerce Headquarters.

1. Ga naar **Retail en Commerce \> Instelling van hoofdkantoor \> Parameters**.
1. Selecteer **Klantorders** in het navigatievenster aan de linkerkant.
1. Ga naar het sneltabblad **Betalingen** en controleer of de velden **Betalingstermijn** en **Betalingsmethode** correct zijn ingesteld.

## <a name="additional-resources"></a>Aanvullende bronnen

[BOPIS configureren](../cpe-bopis.md)

[Meerdere ophaal- en bezorgmethodes inschakelen voor klantorders](../multiple-pickup-modes.md)

[Commerce-orderbetalingen voor meerdere kanalen](../dev-itpro/commerce-payments.md)

[Winkelselectiemodule](../store-selector.md)
