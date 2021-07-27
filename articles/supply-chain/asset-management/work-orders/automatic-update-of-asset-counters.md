---
title: Automatisch bijwerken van activatellers
description: Dit onderwerp beschrijft het automatisch bijwerken van activatellers in Activabeheer.
author: johanhoffmann
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: d1e8a3b34cb359b7ea7f7181d2308f8e021f3c95
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 07/06/2021
ms.locfileid: "6359120"
---
# <a name="automatic-update-of-asset-counters"></a>Automatisch bijwerken van activatellers

[!include [banner](../../includes/banner.md)]

Zie [Handmatig bijwerken van activatellers](../work-orders/manual-update-of-asset-counters.md) voor meer informatie over de handmatige registratie van activatellers. Zie [Tellers](../setup-for-objects/counters.md)voor meer informatie over het instellen van activatellers.

Tellerwaarden kunnen ook automatisch worden bijgewerkt vanuit productieregistraties, op basis van de productie-uren of de productiehoeveelheid (oftewel de hoeveelheid die is geproduceerd). Deze update wordt uitgevoerd op de pagina **Activatellers bijwerken**. U kunt een of meer activa bijwerken door één parameter in te stellen: **Begindatum**. Deze parameter geeft de begindatum voor productieregistraties (productie-uren of productiehoeveelheden) aan. Met andere woorden, het geeft de datum aan vanaf wanneer de tellerwaarden moeten worden bijgewerkt.

Alle activa die gerelateerd zijn aan een resource *en* die activatellers hebben die zijn ingesteld om te worden bijgewerkt op basis van de productie-uren of geproduceerde hoeveelheid, worden opgenomen in een automatische update. Er worden nieuwe tellerwaarden gemaakt.

Voor tellers die zijn gebaseerd op de productiehoeveelheid, bevat de telling zowel de goede hoeveelheid als de foute hoeveelheid die is geregistreerd. Als de eenheid die wordt gebruikt voor het registreren van de productiehoeveelheid verschilt van de eenheid die wordt gebruikt voor de teller, wordt de hoeveelheid geconverteerd zodat deze overeenkomt met de tellereenheid.

Zoals hierboven aangegeven, kunnen automatische tellers worden bijgewerkt vanuit productieregistraties. Daarom moet het activum waarvoor u tellers automatisch wilt bijwerken aan een resource (machine) zijn gekoppeld. Wanneer de geproduceerde hoeveelheden of productie-uren zijn geregistreerd voor de resource, kunt u de gerelateerde activatellers bijwerken.

1. Selecteer **Activabeheer** > **Periodiek** > **Activa** > **Activumtellers bijwerken**.

2. Selecteer in het veld **Begindatum** de begindatum van de automatische update.

    >[!NOTE]
    >De datum in dit veld is de datum voor onderhanden werk uit **Routetransacties** (**Productiebeheer** > **Query's en rapporten** > **Productie** > **Routetransacties** > **Fysieke datum**).

3. Op het sneltabblad **Op te nemen records** kunt u specifieke activa, activatypen of resources voor de automatische update selecteren. Selecteer **Filter** en selecteer de relevante selecties.

4. Indien nodig kunt u de automatische update op het Sneltabblad **Op de achtergrond uitvoeren** instellen als een batchtaak.

    In de onderstaande afbeelding ziet u een voorbeeld van het dialoogvenster **Activumtellers bijwerken**.

    ![Figuur 1.](media/12-work-orders.png)

5. Selecteer **OK**. 

Nadat de automatische update van de activumteller is uitgevoerd, kunt u de tellerregistraties bekijken die zijn gerelateerd aan het activum op de pagina **Activumtellers**. Selecteer **Activabeheer** > **Algemeen** > **Activa** > **Alle activa**, selecteer het activum en selecteer daarna in het actievenster op het tabblad **Activum** in de groep **Preventief** de optie **Tellers**.

Op de pagina **Samengevoegde waarde van activa** kunt u een overzicht krijgen van de als laatste gemaakte registratie voor alle tellertypen voor alle activa. Selecteer **Activabeheer** > **Query's** > **Activa** > **Samengevoegde waarde van activa**. Deze pagina lijkt op de pagina **Activatellers**, maar u kunt geen registraties toevoegen of bewerken. Deze is alleen bedoeld als overzicht.

In de onderstaande afbeelding ziet u een voorbeeld van de pagina **Samengevoegde waarde van activa**.

![Figuur 2.](media/13-work-orders.png)

Let op de volgende punten:

- U kunt nog steeds handmatige registraties voor tellerwaarden maken voor tellertypen die automatisch worden bijgewerkt. Zie [Handmatig bijwerken van activatellers](../work-orders/manual-update-of-asset-counters.md) voor meer informatie.

- U kunt tellers instellen die zijn gerelateerd aan een andere teller. In dit geval worden gerelateerde tellers tegelijkertijd automatisch bijgewerkt wanneer een teller wordt bijgewerkt. Zie [Tellers](../setup-for-objects/counters.md) voor meer informatie over het instellen van gerelateerde tellers.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]