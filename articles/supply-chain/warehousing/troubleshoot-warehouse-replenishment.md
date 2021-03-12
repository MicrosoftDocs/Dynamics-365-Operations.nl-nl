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
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 7748a18d2b6f612b3ac9ac1a75efb6ae5f13859a
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2021
ms.locfileid: "4993864"
---
# <a name="troubleshoot-warehouse-replenishment"></a>Problemen met magazijnaanvulling oplossen

[!include [banner](../includes/banner.md)]

In dit onderwerp wordt beschreven hoe u veelvoorkomende problemen kunt oplossen die kunnen optreden tijdens werken met magazijnaanvulling in Microsoft Dynamics 365 Supply Chain Management.

## <a name="i-receive-the-following-error-message-work-1-cannot-be-unblocked-because-it-has-unfinished-replenishment-work"></a>Het volgende foutbericht wordt weergegeven: "Werk %1 kan niet ongedaan worden gemaakt omdat het onvoltooid aanvullingswerk bevat."

### <a name="issue-description"></a>Probleembeschrijving

Verzamelwerk wordt geblokkeerd vanwege afhankelijk aanvullingswerk.

### <a name="issue-resolution"></a>Probleemoplossing

Wanneer u wavevraagaanvulling gebruikt en er een verzamellocatie moet worden aangevuld om aan de bronordervraag te voldoen, worden zowel het aanvullingswerk als het verzamelwerk gemaakt. Het verzamelproces wordt echter geblokkeerd totdat het aanvullingswerk is voltooid. Dit gebeurt met opzet, omdat de verzamellocatie onvoldoende voorraad heeft, tenzij het aanvullingswerk is voltooid. Voltooi het aanvullingswerk en verwerk vervolgens het verzamelwerk.
