---
title: Orderwachtstanden
description: In dit onderwerp worden de orderwachtstanden beschreven in Dynamics 365 for Retail.
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: MCRHoldCodeTable, MCRSalesTableOrderHistory, MCRHoldCodeTrans
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 79132
ms.assetid: 7c00dc35-73e5-400a-8587-22f37ddfc0e0
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 8b4c8ecbef1dc667d3b60411a53f0c63686529c2
ms.contentlocale: nl-nl
ms.lasthandoff: 11/03/2017

---

# <a name="order-holds"></a>Orderwachtstanden

[!INCLUDE [banner](includes/banner.md)]

In dit onderwerp worden de orderwachtstanden beschreven in Dynamics 365 for Retail.

Een order kan om diverse redenen in wachtstand worden geplaatst. U kunt bijvoorbeeld een order in wachtstand plaatsen tot een klantadres of betalingsmethode kan worden geverifieerd of tot een manager de kredietlimiet van de klant kan controleren. Tijdens het verkoopproces zijn er momenten waarop verkooporders in de wachtstand moeten worden geplaatst. Een verkooporder kan bijvoorbeeld in wachtstand worden geplaatst omwille van problemen met een klantbetaling, vanwege vermoede fraude of omdat een manager de order moet controleren. Wanneer een verkooporder in de wachtstand is geplaatst, wordt een code van de orderwachtstand aan de verkooporder toegewezen om de reden voor de wachtstand op te geven. Wachtstandcodes van verkooporders worden geconfigureerd in **Verkoop en marketing** &gt; **Instellingen** &gt; **Verkooporders** &gt; **Wachtstandcodes van verkooporders**. Een verkooporder kan handmatig in de wachtstand worden geplaatst op het moment dat de order wordt gemaakt of later. Bovendien kan een order automatisch in de wachtstand worden geplaatst, gebaseerd op frauderegels. Wanneer een verkooporder in wachtstand staat, moet u deze mogelijke met meer informatie bijwerken. Als alternatief kunt u de verkooporder uitchecken terwijl u eraan blijft werken. U kunt een verkooporder uitchecken, opnieuw inchecken en het uitchecken door een andere gebruiker zelfs overschrijven door de workbench voor orderwachtstanden te gebruiken (**Retail** &gt; **Klanten** &gt; **Orderwachtstanden**). Wanneer een order klaar is om te worden voltooid, moet u de wachtstand verwijderen voordat u het orderproces kunt voltooien.




