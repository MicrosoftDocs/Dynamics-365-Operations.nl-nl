---
title: Veelgestelde vragen workflow
description: In dit onderwerp worden antwoorden op veelgestelde vragen over het workflowsysteem in Microsoft Dynamics 365 for Finance and Operations gegeven.
author: ChrisGarty
manager: AnnBe
ms.date: 05/07/2019
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
ms.openlocfilehash: f6240b1b5136937aa47f455547fed6f0c7c08e2c
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/07/2019
ms.locfileid: "1509286"
---
# <a name="workflow-system"></a>Workflowsysteem

[!include [banner](../includes/banner.md)]

In dit onderwerp worden antwoorden op veelgestelde vragen over het workflowsysteem in Microsoft Dynamics 365 for Finance and Operations gegeven.

## <a name="notifications"></a>Meldingen

### <a name="why-are-multiple-notifications-received-when-a-work-item-is-rejected"></a>Waarom worden er meerdere meldingen ontvangen wanneer een werkitem wordt afgewezen?
Wanneer een werkitem wordt afgewezen, wordt dat werkitem als afgewezen voltooid. Een andere werkitem wordt gemaakt en toegewezen aan de aanvrager. Dit betekent dat er een melding naar de aanvrager voor het afgewezen werkitem gaat en een aparte melding naar de gebruiker die is toegewezen aan het nieuwe werkitem waarvoor 'wijziging is aangevraagd'. 

Elke melding is voor een ander werkitem, maar doordat de meldingen op elkaar lijken kan er verwarring ontstaan. We proberen dit in een toekomstige versie te verbeteren.

### <a name="why-are-my-workflow-exports-failing"></a>Waarom mislukt het exporteren van mijn werkstromen?
Er geldt momenteel een beperking in de functie voor het exporteren van werkstromen waardoor namen van werkstromen niet langer kunnen zijn dan 48 tekens. Als u een naam gebruikt die langer is dan 48 tekens, kan het foutbericht 'Server kon de aanvraag niet verifiëren' worden weergegeven en/of kan worden voorkomen dat een bestand wordt geëxporteerd zonder bestandstype. Het volgende blogbericht bevat nadere details: [Problemen bij het exporteren van werkstromen oplossen](https://community.dynamics.com/ax/b/elandaxdynamicsaxupgradesanddevelopment/archive/2019/04/10/workflow-export-troubleshooting).
