---
title: Regels in de consistentiecontrole voor detailhandeltransacties uitschakelen
description: In dit onderwerp wordt de functionaliteit voor het uitschakelen van de regels in de consistentiecontrole voor detailhandeltransacties in Microsoft Dynamics 365 Retail beschreven.
author: josaw1
manager: AnnBe
ms.date: 10/15/2019
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: ''
ms.openlocfilehash: 4bf8df2fb9f8f5c33ceb13eb012fb6879f81ec66
ms.sourcegitcommit: bdbca89bd9b328c282ebfb681f75b8f1ed96e7a8
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/14/2019
ms.locfileid: "2586292"
---
# <a name="disable-rules-in-the-retail-transaction-consistency-checker"></a>Regels in de consistentiecontrole voor detailhandeltransacties uitschakelen 

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

Detailhandelaren kunnen bedrijfsscenario's en processen hebben die uniek zijn. Daarom zijn niet alle regels die standaard zijn opgenomen in de consistentiecontrole voor detailhandeltransacties van toepassing op alle detailhandelaren. Om verschillen te kunnen verwerken biedt Microsoft Dynamics 365 Retail functionaliteit die kan worden gebruikt om de regels die niet van toepassing zijn, uit te schakelen.

Voor het weergeven van de lijst met regels die beschikbaar zijn in de consistentiecontrole voor detailhandeltransacties in uw omgeving en om de status van elke regel weer te geven, gaat u naar **Detailhandel \> Instelling van hoofdkantoor \> Parameters \> Detailhandelparameters** en selecteert u het tabblad **Transactievalidatie**.

Standaard is de status van elke regel ingesteld op **Ingeschakeld**. Daarom worden alle regels gebruikt om detailhandeltransacties te valideren voordat ze in de detailhandeloverzichten worden opgenomen. Als u een regel wilt uitschakelen, wijzigt u de status in **Uitgeschakeld**. Uitgeschakelde regels worden niet meegenomen wanneer detailhandeltransacties worden gevalideerd tijdens het berekeningsproces van het overzicht.

Als u het gehele validatieproces wilt overslaan, ongeacht de ingeschakelde regels, gaat u naar **Detailhandel \> Instelling van hoofdkantoor \> Parameters \> Detailhandelparameters** en stelt u op het tabblad **Transactievalidatie** de optie **Consistentiecontrole voor detailhandeltransacties uitschakelen** in op **Ja**. Als deze optie is ingesteld op **Nee**, kan deze niet worden teruggezet op **Ja** vanuit de gebruikersinterface.
