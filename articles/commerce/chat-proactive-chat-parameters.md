---
title: Proactieve chatparameters voor Commerce-chatmodule
description: In dit artikel worden de proactieve chatparameters van Commerce-chatmodules in Microsoft Dynamics 365 Commerce beschreven.
author: gvrmohanreddy
ms.date: 10/18/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2022-07-20
ms.openlocfilehash: f3cff89a25ff84414e7fdd32cbb26404c2080187
ms.sourcegitcommit: 40c80a617b903c2b26e44b41147e0021c5cb680d
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/18/2022
ms.locfileid: "9691056"
---
# <a name="commerce-chat-module-proactive-chat-parameters"></a>Proactieve chatparameters voor Commerce-chatmodule

[!include [banner](includes/banner.md)]

In dit artikel worden de proactieve chatparameters van Commerce-chat met Omnichannel voor Customer Service en Commerce-chat met Power Virtual Agents-chatmodules in Microsoft Dynamics 365 Commerce beschreven.

## <a name="proactive-chat-properties"></a>Proactieve chateigenschappen

De proactieve chateigenschappen bevinden zich in het eigenschappenvenster van Commerce-chat met Omnichannel voor Customer Service en Commerce-chat met Power Virtual Agents-modules in Commerce site builder.

> [!NOTE]
> Standaard zijn alle proactieve chateigenschappen die hier worden vermeld leeg. We raden u aan om meer te weten te komen over deze eigenschappen en ze alleen in te stellen als deze vereist zijn. Op deze manier beperkt u het aantal fouten met proactief chats.

### <a name="proactive-chat"></a>Proactieve chat

| Beschrijvende naam | Description | Standaardwaarde |
|---------------|-------------|---------------|
| Ingeschakeld | Maak proactief contact met klanten, op basis van verschillende triggers. | Uitgeschakeld |
| Chatbegroeting | Het begroetingsbericht dat wordt gebruikt wanneer een proactieve chat is geactiveerd. | Leeg |

### <a name="wait-time-proactive-chat"></a>Wachttijd (proactieve chat)

| Beschrijvende naam | Description |
|---------------|-------------|
| Wachttijd (sec.) | De tijd (in seconden) die sitegebruikers besteden op een sitepagina voordat er een proactieve chat wordt geactiveerd. |
| Chatbegroeting | Het begroetingsbericht dat wordt gebruikt wanneer een proactieve chat is geactiveerd. |

### <a name="number-of-page-visits-proactive-chat"></a>Aantal paginabezoeken (proactieve chat)

| Beschrijvende naam | Description |
|---------------|-------------|
| Aantal paginabezoeken | Het aantal paginabezoeken voordat een proactieve chat wordt geactiveerd. Sitegebruikers moeten de prompt eerst accepteren in de banner voor toestemming voor cookies. |
| Chatbegroeting | Het begroetingsbericht dat wordt gebruikt wanneer een proactieve chat is geactiveerd. |

### <a name="specific-pages-proactive-chat"></a>Specifieke pagina('s) (proactieve chat)

| Beschrijvende naam | Description |
|---------------|-------------|
| Pagina('s) | Een lijst met de pagina's die een proactieve chat activeren wanneer ze worden bezocht. |
| Chatbegroeting | Het begroetingsbericht dat wordt gebruikt wanneer een proactieve chat is geactiveerd. |

### <a name="from-specific-pages-proactive-chat"></a>Van specifieke pagina('s) (proactieve chat)

| Beschrijvende naam | Description |
|---------------|-------------|
| Pagina('s) | Een lijst met de pagina's die een proactieve chat activeren wanneer gebruikers wegnavigeren van deze pagina's. |
| Chatbegroeting | Het begroetingsbericht dat wordt gebruikt wanneer een proactieve chat is geactiveerd. |

### <a name="specific-countryregion-proactive-chat"></a>Specifiek(e) land/regio (proactieve chat)

| Beschrijvende naam | Description |
|---------------|-------------|
| Land- of regiocode | Gebruikers die vanuit opgegeven landen of regio's bezoeken, activeren een proactieve chat. Land-/regiocodes moeten uit twee hoofdletters bestaan (bijvoorbeeld **US**). |
| Chatbegroeting | Het begroetingsbericht dat wordt gebruikt wanneer een proactieve chat is geactiveerd. |

### <a name="date-range-proactive-chat"></a>Datumbereik (proactieve chat)

| Beschrijvende naam | Description |
|---------------|-------------|
| Begindatum (dd/mm/jjjj) | De datum waarop of waarna een proactieve chat wordt geactiveerd. |
| Einddatum (dd/mm/jjjj) | De datum waarop of waarvoor een proactieve chat wordt geactiveerd. |
| Chatbegroeting | Het begroetingsbericht dat wordt gebruikt wanneer een proactieve chat is geactiveerd. |

### <a name="total-amount-in-cart-proactive-chat"></a>Totaalbedrag in winkelwagen (proactieve chat)

| Beschrijvende naam | Description |
|---------------|-------------|
| Minimum | Het minimale monetaire bedrag (inclusief) in de winkelwagen dat een proactieve chat activeert als gebruikers de pagina met de winkelwagen bezoeken. |
| Maximum | Het maximale monetaire bedrag (inclusief) in de winkelwagen dat een proactieve chat activeert als gebruikers de pagina met de winkelwagen bezoeken. |
|Chatbegroeting | Het begroetingsbericht dat wordt gebruikt wanneer een proactieve chat is geactiveerd. |

### <a name="total-number-of-items-in-cart-proactive-chat"></a>Totale aantal artikelen in winkelwagen (proactieve chat)

| Beschrijvende naam | Description |
|---------------|-------------|
| Minimum | Het minimale aantal artikelen (inclusief) in de winkelwagen dat een proactieve chat activeert als gebruikers de pagina met de winkelwagen bezoeken. |
| Maximum | Het maximale aantal artikelen (inclusief) in de winkelwagen dat een proactieve chat activeert als gebruikers de pagina met de winkelwagen bezoeken. |
| Chatbegroeting | Het begroetingsbericht dat wordt gebruikt wanneer een proactieve chat is geactiveerd. |

### <a name="specific-products-in-cart-proactive-chat"></a>Specifiek(e) product(en) in winkelwagen (proactieve chat)

| Beschrijvende naam | Description |
|---------------|-------------|
| Id/SKU van product(en) | Een lijst met de product-id's/SKU-nummers die een proactieve chat activeren wanneer gebruikers de winkelwagenpagina bezoeken. |
| Chatbegroeting | Het begroetingsbericht dat wordt gebruikt wanneer een proactieve chat is geactiveerd. |

## <a name="additional-resources"></a>Aanvullende bronnen

[Overzicht van chatfuncties voor Commerce](commerce-chat-overview.md)

[Commerce Chat met module Omnichannel voor Customer Service](commerce-chat-module.md)

[Commerce-chat met Power Virtual Agents-module](chat-module-pva.md)
