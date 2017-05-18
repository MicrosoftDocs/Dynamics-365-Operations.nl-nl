---
title: Orderwachtstanden
description: Dit onderwerp beschrijft blokkeringen op orders die Detailhandel en commerce in Dynamics AX gebruiken.
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core, Retail
ms.custom: 79132
ms.assetid: 7c00dc35-73e5-400a-8587-22f37ddfc0e0
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 6b1f91f863c8da35362ebb3036e76aa10d95ba65
ms.openlocfilehash: 82a0354901a665480b8854ce2527e35490ac5562
ms.contentlocale: nl-nl
ms.lasthandoff: 04/26/2017


---

# <a name="order-holds"></a>Orderwachtstanden

[!include[banner](includes/banner.md)]


Dit onderwerp beschrijft blokkeringen op orders die Detailhandel en commerce in Dynamics AX gebruiken.

Een order kan om diverse redenen in wachtstand worden geplaatst. U kunt bijvoorbeeld een order in wachtstand plaatsen tot een klantadres of betalingsmethode kan worden geverifieerd of tot een manager de kredietlimiet van de klant kan controleren. Tijdens het verkoopproces zijn er momenten waarop verkooporders in de wachtstand moeten worden geplaatst. Een verkooporder kan bijvoorbeeld in wachtstand worden geplaatst omwille van problemen met een klantbetaling, vanwege vermoede fraude of omdat een manager de order moet controleren. Wanneer een verkooporder in de wachtstand is geplaatst, wordt een code van de orderwachtstand aan de verkooporder toegewezen om de reden voor de wachtstand op te geven. Wachtstandcodes van verkooporders worden geconfigureerd in **Verkoop en marketing** &gt; **Instellingen** &gt; **Verkooporders** &gt; **Wachtstandcodes van verkooporders**. Een verkooporder kan handmatig in de wachtstand worden geplaatst op het moment dat de order wordt gemaakt of later. Bovendien kan een order automatisch in de wachtstand worden geplaatst, gebaseerd op frauderegels. Wanneer een verkooporder in wachtstand staat, moet u deze mogelijke met meer informatie bijwerken. Als alternatief kunt u de verkooporder uitchecken terwijl u eraan blijft werken. U kunt een verkooporder uitchecken, opnieuw inchecken en het uitchecken door een andere gebruiker zelfs overschrijven door de workbench voor orderwachtstanden te gebruiken (**Detailhandel en commerce** &gt; **Klanten** &gt; **Orderwachtstanden**). Wanneer een order klaar is om te worden voltooid, moet u de wachtstand verwijderen voordat u het orderproces kunt voltooien.




