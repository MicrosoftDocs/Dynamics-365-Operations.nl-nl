---
title: Veelgestelde vragen workflow
description: In dit onderwerp worden antwoorden op veelgestelde vragen over het workflowsysteem in Microsoft Dynamics 365 for Finance and Operations gegeven.
author: ChrisGarty
manager: AnnBe
ms.date: 02/28/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f058a450eb18e688efbc5306a42b4efef6aa91e7
ms.sourcegitcommit: 9a723737565ac78c884e40f7129d0f5aad747524
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/01/2019
ms.locfileid: "773203"
---
# <a name="workflow-system"></a>Workflowsysteem

[!include [banner](../includes/banner.md)]

In dit onderwerp worden antwoorden op veelgestelde vragen over het workflowsysteem in Microsoft Dynamics 365 for Finance and Operations gegeven.

## <a name="notifications"></a>Meldingen

### <a name="why-are-multiple-notifications-received-when-a-work-item-is-rejected"></a>Waarom worden er meerdere meldingen ontvangen wanneer een werkitem wordt afgewezen?
Wanneer een werkitem wordt afgewezen, wordt dat werkitem als afgewezen voltooid. Een andere werkitem wordt gemaakt en toegewezen aan de aanvrager. Dit betekent dat er een melding naar de aanvrager voor het afgewezen werkitem gaat en een aparte melding naar de gebruiker die is toegewezen aan het nieuwe werkitem waarvoor 'wijziging is aangevraagd'. 

Elke melding is voor een ander werkitem, maar doordat de meldingen op elkaar lijken kan er verwarring ontstaan. We proberen dit in een toekomstige versie te verbeteren.
