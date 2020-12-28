---
title: Problemen met magazijnaanvulling oplossen
description: In dit onderwerp wordt beschreven hoe u veelvoorkomende problemen kunt oplossen die kunnen optreden tijdens werken met magazijnaanvulling in Microsoft Dynamics 365 Supply Chain Management.
author: perlynne
manager: tfehr
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: e4d87e85520c2b6f2346fddf3b985d4e17fe35cb
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/25/2020
ms.locfileid: "4644868"
---
# <a name="troubleshoot-warehouse-replenishment"></a>Problemen met magazijnaanvulling oplossen

[!include [banner](../includes/banner.md)]

In dit onderwerp wordt beschreven hoe u veelvoorkomende problemen kunt oplossen die kunnen optreden tijdens werken met magazijnaanvulling in Microsoft Dynamics 365 Supply Chain Management.

## <a name="i-receive-the-following-error-message-work-1-cannot-be-unblocked-because-it-has-unfinished-replenishment-work"></a>Het volgende foutbericht wordt weergegeven: "Werk %1 kan niet ongedaan worden gemaakt omdat het onvoltooid aanvullingswerk bevat."

### <a name="issue-description"></a>Probleembeschrijving

Verzamelwerk wordt geblokkeerd vanwege afhankelijk aanvullingswerk.

### <a name="issue-resolution"></a>Probleemoplossing

Wanneer u wavevraagaanvulling gebruikt en er een verzamellocatie moet worden aangevuld om aan de bronordervraag te voldoen, worden zowel het aanvullingswerk als het verzamelwerk gemaakt. Het verzamelproces wordt echter geblokkeerd totdat het aanvullingswerk is voltooid. Dit gebeurt met opzet, omdat de verzamellocatie onvoldoende voorraad heeft, tenzij het aanvullingswerk is voltooid. Voltooi het aanvullingswerk en verwerk vervolgens het verzamelwerk.
