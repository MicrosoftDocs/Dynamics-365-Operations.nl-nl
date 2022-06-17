---
title: Regels uitschakelen die worden gebruikt tijdens het validatieproces voor transacties
description: In dit artikel wordt de functionaliteit beschreven voor het uitschakelen van de regels voor transactievalidatie in Microsoft Dynamics 365 Commerce.
author: analpert
ms.date: 12/11/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: ''
ms.openlocfilehash: 7d566aa3b829dad281528925a341382f9637fdba
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8884871"
---
# <a name="disable-rules-used-in-the-transaction-validation-process"></a>Regels uitschakelen die worden gebruikt tijdens het validatieproces voor transacties

[!include [banner](../includes/banner.md)]

Detailhandelaren kunnen bedrijfsscenario's en processen hebben die uniek zijn. Daarom zijn niet alle regels die zijn opgenomen in het proces voor validatie van transacties van toepassing op alle retailers. Om verschillen te kunnen verwerken, biedt Microsoft Dynamics 365 Commerce functionaliteit die kan worden gebruikt voor het uitschakelen van regels die niet van toepassing zijn.

Als u de lijst met regels wilt weergeven die beschikbaar zijn in het transactievalidatieproces in uw omgeving en als u de status van elke regel wilt weergeven, gaat u naar **Retail en Commerce \> Instelling van hoofdkantoor \> Parameters \> Commerce-parameters** en selecteert u het tabblad **Transactievalidatie**. Alle ingeschakelde regels worden gebruikt om transacties te valideren tijdens het proces **Winkeltransacties valideren** en moeten geslaagd zijn om transacties te kunnen verzamelen en boeken in een transactieoverzicht.

Standaard is de status van elke regel ingesteld op **Ingeschakeld**. Daarom worden alle regels gebruikt om detailhandelstransacties te valideren voordat ze in de handelstransactieoverzichten kunnen worden opgenomen. Als u een regel wilt uitschakelen, wijzigt u de status in **Uitgeschakeld**. Uitgeschakelde regels worden niet meegenomen wanneer transacties worden gevalideerd tijdens het proces **Winkeltransacties valideren**.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
