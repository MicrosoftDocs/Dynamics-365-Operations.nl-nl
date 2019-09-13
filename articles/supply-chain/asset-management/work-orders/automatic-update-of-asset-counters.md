---
title: Automatisch bijwerken van activatellers
description: Dit onderwerp beschrijft het automatisch bijwerken van activatellers in Activabeheer.
author: josaw1
manager: AnnBe
ms.date: 08/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-15
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 97e6912cd37d6f82d8bf022141f04645a3364ee1
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875595"
---
# <a name="automatic-update-of-asset-counters"></a>Automatisch bijwerken van activatellers

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

In het vorige gedeelte wordt de handmatige registratie van activatellers beschreven. Het instellen van activatellers wordt beschreven in [Tellers](../setup-for-objects/counters.md).

Tellerwaarden kunnen ook automatisch worden bijgewerkt vanuit productieregistraties, op basis van productie-uren of de productiehoeveelheid. Dit gebeurt in **Activumtellers bijwerken**. U kunt een of meer activa bijwerken door één parameter, **Begindatum**, in te voegen. Met deze parameter wordt de begin datum voor productieregistraties (uren of geproduceerde hoeveelheid) opgegeven. Dit betekent de begindatum vanaf welke de tellerwaarden moeten worden bijgewerkt.

Alle activa die gerelateerd zijn aan een resource *en* activatellers hebben die zijn ingesteld om te worden bijgewerkt op basis van de geproduceerde hoeveelheid of productie-uren, worden opgenomen in een automatische update en nieuwe tellerwaarden worden gemaakt.

Voor tellers op basis van de productiehoeveelheid wordt zowel de goede hoeveelheid als de geregistreerde fouthoeveelheid in de telling opgenomen. Als de eenheid die wordt gebruikt voor het registreren van geproduceerde hoeveelheden verschilt van de eenheid die wordt gebruikt voor de teller, wordt de hoeveelheid geconverteerd zodat deze overeenkomt met de tellereenheid.

Zoals hierboven aangegeven, kunnen automatische tellers worden bijgewerkt vanuit productieregistraties. Daarom moet het activum waarvoor u tellers automatisch wilt bijwerken aan een resource (machine) zijn gekoppeld. De volgende omschrijvingen geven een overzicht van de instellingen en verwerking van productieorders (in de module **Productiebeheer**), die als basis dient voor het automatisch bijwerken van tellers voor een activum in de module **Activabeheer**.

Wanneer de geproduceerde hoeveelheden of productie-uren zijn geregistreerd voor de resource, kunt u de gerelateerde activatellers bijwerken.

1. Klik op **Activabeheer** > **Periodiek** > **Activa** > **Activumtellers bijwerken**.

2. Selecteer de begindatum van de automatische update in het veld **Begindatum**.

>[!NOTE]
>De datum in dit veld is de datum voor onderhanden werk uit **Routetransacties** (**Productiebeheer** > **Query's en rapporten** > **Productie** > **Routetransacties** > **Fysieke datum**).

3. Als u specifieke activa, activumtypen of resources wilt selecteren, klikt u op **Filteren** op het sneltabblad **Records die moeten worden opgenomen** en selecteert u de betreffende items.

4. Indien nodig kunt u de automatische update op het sneltabblad **Op de achtergrond uitvoeren** instellen als een batchtaak.

![Figuur 1](media/12-work-orders.png)

5. Klik op **OK**. Wanneer de automatische update van de activumteller is uitgevoerd, ziet u de tellerregistraties die gerelateerd zijn aan het activum in **Activumtellers** (**Activabeheer** > **Algemeen** > **Activa** > **Alle activa** > het activum selecteren > de knop **Teller**).

In **Totalen van activateller** kunt u een overzicht krijgen van de laatste gemaakte registratie voor alle tellertypen voor alle activa. Klik op **Activabeheer** > **Query's** > **Activa** > **Samengevoegde waarde van activa**. De weergave is vergelijkbaar met **Activumtellers**, maar u kunt geen registraties toevoegen of bewerken in **Samengevoegde waarde van activa**. Deze is alleen bedoeld als overzicht.

![Figuur 2](media/13-work-orders.png)


- Het is nog steeds mogelijk om handmatige registraties voor tellerwaarden te maken voor tellertypen die automatisch worden bijgewerkt. Zie Handmatig bijwerken van activatellers voor meer informatie.
- U kunt tellers instellen die gerelateerd zijn aan een andere teller. Dit betekent dat gerelateerde tellers automatisch tegelijkertijd worden bijgewerkt wanneer een teller wordt bijgewerkt. Zie het onderwerp [Tellers](../setup-for-objects/counters.md) voor het instellen van gerelateerde tellers.
