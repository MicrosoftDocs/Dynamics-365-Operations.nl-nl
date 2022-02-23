---
title: Hertoewijzing van opbrengsttoerekening - Scenario 1
description: In dit onderwerp wordt een hertoewijzingsscenario besproken waarin twee verkooporders worden ingevoerd, maar alleen worden bevestigd. Hetzelfde scenario levert vergelijkbare resultaten op als meer dan twee verkooporders zijn bevestigd.
author: kweekley
manager: aolson
ms.date: 12/21/2020
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: Customer
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2020-12-21
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 2a0add2d4bc01127c1f359736398123a6a3df9fe
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2021
ms.locfileid: "4969647"
---
# <a name="revenue-recognition-reallocation--scenario-1"></a>Hertoewijzing van opbrengsttoerekening - Scenario 1

[!include [banner](../includes/banner.md)]

In dit onderwerp wordt een hertoewijzingsscenario besproken waarin twee verkooporders worden ingevoerd, maar alleen worden bevestigd. Hetzelfde scenario levert vergelijkbare resultaten op als meer dan twee verkooporders zijn bevestigd.

Voor dit scenario is de optie **Factuurcorrecties boeken naar Klanten** ingesteld op **Nee** op het tabblad **Opbrengsttoerekening** van de pagina **Grootboekparameters** (**Opbrengsttoerekening \> Instellen \> Grootboekparameters**).

[![De optie Factuurcorrecties boeken naar Klanten is ingesteld op Nee](./media/06_rev-rec-scenarios.png)](./media/06_rev-rec-scenarios.png)

Er wordt een verkooporder gemaakt voor de klant US\_SI\_0003. De klant koopt een laptop (artikelnummer S0012) en een ondersteuningsplan voor de laptop (artikelnummer S0008, Doorlopende technische service). De opbrengst voor de laptop wordt onmiddellijk toegerekend (er is geen schema voor opbrengsttoerekening). De opbrengst voor het ondersteuningsplan wordt uitgesteld en over 12 maanden toegerekend, zoals gedefinieerd door het datumbereik in het contract.

[![Verkooporderregels voor de laptop en het ondersteuningsplan](./media/07_rev-rec-scenarios.png)](./media/07_rev-rec-scenarios.png)

De verkooporder wordt bevestigd. Aangezien voor beide artikelen toewijzing van de opbrengstprijs is ingesteld, wordt de opbrengstprijs berekend wanneer de verkooporder wordt bevestigd. U kunt de toegekende opbrengst weergeven op de pagina **Opbrengstprijstoewijzing** (selecteer **Opbrengstprijstoewijzing** op de pagina **Verkooporder** in het actievenster op het tabblad **Beheren** in de groep **Opbrengsttoerekening**). De opbrengst voor de laptop wordt als bedrag van $ 1008,01 naar de opbrengstrekening geboekt. De opbrengst voor het ondersteuningsplan wordt als bedrag van $ 190,99 naar de rekening voor uitgestelde opbrengst geboekt. Het totaal van de opbrengstprijzen moet gelijk zijn aan het totaal van de regels die zijn ingesteld om de opbrengstprijstoewijzing vast te leggen ($ 1199,00).

[![De pagina Opbrengstprijstoewijzing](./media/08_rev-rec-scenarios.png)](./media/08_rev-rec-scenarios.png)

De klant koos er op het moment van verkoop voor om geen installatieservices (artikelnummer S0001) aan te schaffen, maar is later van gedachten veranderd. Daarom wordt een tweede verkooporder ingevoerd voor dezelfde klant.

[![Verkooporderregel voor installatieservices](./media/09_rev-rec-scenarios.png)](./media/09_rev-rec-scenarios.png)

De tweede verkooporder wordt bevestigd. Omdat deze verkooporder slechts één regel bevat, wordt geen opbrengstprijstoewijzing uitgevoerd wanneer de verkooporder wordt bevestigd. Opbrengstprijstoewijzing vindt alleen plaats als er twee of meer unieke artikelen zijn en de toewijzing van opbrengstprijzen is ingesteld voor die artikelen.

Als deze nieuwe verkooporder de enige wijziging in het contract van de klant is, kan het hertoewijzingsproces nu worden uitgevoerd. Selecteer in een van de twee verkooporders de optie **Prijs opnieuw toewijzen met nieuwe orderregels** om de pagina **Prijs opnieuw toewijzen met nieuwe orderregels** te openen. U kunt ook naar **Opbrengsttoerekening \> Periodieke taken \> Prijs opnieuw toewijzen met nieuwe orderregels** gaan. Selecteer de twee verkooporders en bijbehorende verkooporderregels en selecteer vervolgens **Hertoewijzing bijwerken**. In de kolom **Opnieuw toegewezen bedrag** wordt de nieuwe opbrengstprijs voor elke verkooporderregel weergegeven.

[![Nieuwe opbrengstprijzen op de pagina Prijs opnieuw toewijzen met nieuwe orderregels](./media/10_rev-rec-scenarios.png)](./media/10_rev-rec-scenarios.png)

Als u **Verwacht boekstuk** selecteert, wordt er niets weergegeven omdat er geen facturen zijn geboekt.

Selecteer **Verwerken** om de hertoewijzing te voltooien. U wordt gevraagd om een boekingsdatum, zelfs als er niets is geboekt. Nadat de toewijzing is voltooid, wordt op de pagina **Opbrengstprijstoewijzing** voor elke verkooporder de prijstoewijzing voor alle artikelen in beide verkooporders weergegeven. De pagina **Opbrengstprijstoewijzing** voor elke verkooporder bevat dus een artikel dat niet in die verkooporder voorkomt omdat dit artikel wel deel uitmaakt van hetzelfde contract, maar in een andere verkooporder is opgenomen.

> [!TIP]
> Als u context wilt bieden over de reden waarom deze extra artikelen worden weergegeven, kunt u andere kolommen aan het raster toevoegen, zoals **Hertoewijzings-id** en **Verkooporder**.
> 
> [![Extra kolommen op de pagina Opbrengstprijstoewijzingen](./media/11_rev-rec-scenarios.png)](./media/11_rev-rec-scenarios.png)
