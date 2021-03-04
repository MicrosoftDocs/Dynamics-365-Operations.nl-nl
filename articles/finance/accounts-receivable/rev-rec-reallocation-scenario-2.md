---
title: Hertoewijzing van opbrengsttoerekening - Scenario 2
description: In dit onderwerp wordt een hertoewijzingsscenario besproken waarin twee verkooporders worden ingevoerd en de klant vervolgens een artikel aan het contract toevoegt nadat de eerste verkooporder is gefactureerd. Wanneer een nieuw artikel aan een contract wordt toegevoegd, kan het worden toegevoegd aan een nieuwe verkooporder of aan de bestaande verkooporder.
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
ms.openlocfilehash: 30b4c55a82237b5c8b6b41032243da337a5ec969
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2021
ms.locfileid: "5003387"
---
# <a name="revenue-recognition-reallocation--scenario-2"></a>Hertoewijzing van opbrengsttoerekening - Scenario 2

[!include [banner](../includes/banner.md)]

In dit onderwerp wordt een hertoewijzingsscenario besproken waarin twee verkooporders worden ingevoerd en de klant vervolgens een artikel aan het contract toevoegt nadat de eerste verkooporder is gefactureerd. Wanneer een nieuw artikel aan een contract wordt toegevoegd, kan het worden toegevoegd aan een nieuwe verkooporder of aan de bestaande verkooporder.

Voor dit scenario is de optie **Factuurcorrecties boeken naar Klanten** ingesteld op **Nee** op het tabblad **Opbrengsttoerekening** van de pagina **Grootboekparameters** (**Opbrengsttoerekening \> Instellen \> Grootboekparameters**).

[![De optie Factuurcorrecties boeken naar Klanten is ingesteld op Nee](./media/12_rev-rec-scenarios.png)](./media/12_rev-rec-scenarios.png)

Er wordt een verkooporder gemaakt voor de klant US\_SI\_0003. De klant koopt installatieservices (artikelnummer S0001) en een ondersteuningsplan voor de laptop (artikelnummer S0008), maar heeft de laptop nog niet geselecteerd. De opbrengst voor de installatieservices wordt uitgesteld tot de datum waarop de laptop wordt aangeschaft. De opbrengst voor het ondersteuningsplan wordt uitgesteld en over 12 maanden toegerekend, zoals gedefinieerd door het datumbereik in het contract.

[![Verkooporderregels voor de installatieservices en het ondersteuningsplan](./media/13_rev-rec-scenarios.png)](./media/13_rev-rec-scenarios.png)

De verkooporder wordt bevestigd. Aangezien voor beide artikelen toewijzing van de opbrengstprijs is ingesteld, wordt de opbrengstprijs berekend wanneer de verkooporder wordt bevestigd. U kunt de toegekende opbrengst weergeven op de pagina **Opbrengstprijstoewijzing** (selecteer **Opbrengstprijstoewijzing** op de pagina **Verkooporder** in het actievenster op het tabblad **Beheren** in de groep **Opbrengsttoerekening**). De opbrengst voor de installatieservices wordt als bedrag van $ 250,00 naar een rekening voor uitgestelde opbrengst geboekt. De opbrengst van $ 150,00 voor het ondersteuningsplan wordt ook naar de rekening voor uitgestelde opbrengst geboekt. Het totaal van de opbrengstprijzen moet gelijk zijn aan het totaal van de regels die zijn ingesteld om de opbrengstprijstoewijzing vast te leggen ($ 400,00).

[![De pagina Opbrengstprijstoewijzing](./media/14_rev-rec-scenarios.png)](./media/14_rev-rec-scenarios.png)

De verkooporder wordt volledig gefactureerd. In de volgende afbeelding wordt de journaalregel weergegeven die voor de factuur is geboekt.

[![Journaalregel voor de volledig gefactureerde verkooporder](./media/15_rev-rec-scenarios.png)](./media/15_rev-rec-scenarios.png)

Het schema voor opbrengsttoerekening wordt ook gemaakt, maar geen van de opbrengsten is al toegerekend.

[![De pagina Opbrengsttoerekeningsschema](./media/16_rev-rec-scenarios.png)](./media/16_rev-rec-scenarios.png)

Een paar dagen later selecteert de klant een laptop. Er wordt een tweede verkooporder ingevoerd voor de klant.

[![Verkooporderregel voor de laptop](./media/17_rev-rec-scenarios.png)](./media/17_rev-rec-scenarios.png)

De tweede verkooporder wordt bevestigd. Omdat deze verkooporder slechts één regel bevat, wordt geen opbrengstprijstoewijzing uitgevoerd wanneer de verkooporder wordt bevestigd. Opbrengstprijstoewijzing vindt alleen plaats als er twee of meer unieke artikelen zijn en de toewijzing van opbrengstprijzen is ingesteld voor die artikelen.

Als deze nieuwe verkooporder de enige wijziging in het contract van de klant is, kan het hertoewijzingsproces nu worden uitgevoerd. Selecteer in een van de twee verkooporders de optie **Prijs opnieuw toewijzen met nieuwe orderregels** om de pagina **Prijs opnieuw toewijzen met nieuwe orderregels** te openen. U kunt ook naar **Opbrengsttoerekening \> Periodieke taken \> Prijs opnieuw toewijzen met nieuwe orderregels** gaan. Selecteer de twee verkooporders en bijbehorende verkooporderregels en selecteer vervolgens **Hertoewijzing bijwerken**. In de kolom **Opnieuw toegewezen bedrag** wordt de nieuwe opbrengstprijs voor elke verkooporderregel weergegeven.

[![Nieuwe opbrengstprijzen op de pagina Prijs opnieuw toewijzen met nieuwe orderregels](./media/18_rev-rec-scenarios.png)](./media/18_rev-rec-scenarios.png)

Selecteer vervolgens **Verwacht boekstuk** om de journaalregels weer te geven die alleen naar het grootboek worden geboekt. Omdat de optie **Factuurcorrecties boeken naar Klanten** is ingesteld op **Nee** op de pagina **Grootboekparameters**, wordt er niets gewijzigd in Klanten wanneer de hertoewijzing wordt verwerkt.

[![Journaalregels op de pagina Verwacht boekstuk](./media/19_rev-rec-scenarios.png)](./media/19_rev-rec-scenarios.png)

Op de pagina **Verwacht boekstuk** wordt in de laatste drie regels de oorspronkelijke journaalregel uit de geboekte factuur teruggeboekt. De eerste vier regels vormen de nieuwe journaalregel die is geboekt voor de factuur. Het is belangrijk dat u begrijpt dat er geen nieuwe factuur wordt weergegeven voor de klant. Na de hertoewijzing moet de klant nog steeds $ 426,00 bestalen. Dit is het bedrag dat in de nieuwe journaalregel naar Klanten moet worden geboekt. De tegenrekeningsbelasting en de uitgestelde opbrengst zijn gelijk aan $ 188,69 + $ 314,48 + $ 26,00 = $ 529,17. Het uitgestelde opbrengstbedrag is gewijzigd vanwege de hertoewijzing. Het verschil van $ 103,17 wordt geboekt naar een vereffeningsrekening voor gedeeltelijke factuuropbrengst. Dit saldo wordt gewist wanneer de factuur wordt geboekt voor de tweede verkooporder die in de hertoewijzing is opgenomen.

Selecteer **Verwerken** om de hertoewijzing te voltooien. U wordt gevraagd om een boekingsdatum, zelfs als er niets is geboekt. Nadat de toewijzing is voltooid, wordt op de pagina **Opbrengstprijstoewijzing** voor elke verkooporder de prijstoewijzing voor alle artikelen in beide verkooporders weergegeven. De pagina **Opbrengstprijstoewijzing** voor elke verkooporder bevat dus een artikel dat niet in die verkooporder voorkomt omdat dit artikel wel deel uitmaakt van hetzelfde contract, maar in een andere verkooporder is opgenomen.

> [!TIP]
> Als u context wilt bieden over de reden waarom deze extra artikelen worden weergegeven, kunt u andere kolommen aan het raster toevoegen, zoals **Hertoewijzings-id** en **Verkooporder**.
> 
> [![Extra kolommen op de pagina Opbrengstprijstoewijzingen](./media/20_rev-rec-scenarios.png)](./media/20_rev-rec-scenarios.png)

In verkooporder 00036 is ook het schema voor opbrengsttoerekening bijgewerkt, op basis van de nieuwe prijs van opbrengsthertoewijzing. Open de pagina **Opbrengstherkenningsschema** vanuit deze verkooporder. Eerder waren er 13 regels voor artikel S0008 (een schema van twaalf maanden is toegewezen aan dit artikel). Er zijn nu 39 regels: de 13 oorspronkelijke schemaregels, 13 schemaregels voor terugboeking en 13 regels die zijn gebaseerd op de nieuwe opbrengstprijs.

[![Bijgewerkte pagina Opbrengsttoerekeningsschema met 39 regels voor artikel S0008](./media/21_rev-rec-scenarios.png)](./media/21_rev-rec-scenarios.png)

Op dezelfde manier is het aantal regels voor artikel S0001 nu uitgebreid naar zes.

[![Bijgewerkte pagina Opbrengsttoerekeningsschema met zes regels voor artikel S0001](./media/22_rev-rec-scenarios.png)](./media/22_rev-rec-scenarios.png)

Wanneer u **Boekstuk** selecteert in verkooporder 000036, wordt in het factuurjournaal de oorspronkelijke journaalregel weergegeven. Als u de stornopost en de nieuwe journaalregel uit de verkooporder wilt weergeven, selecteert u **Opbrengstcorrecties** in het actievenster en vervolgens **Boekstuk**.

[![Verkooporder 000036](./media/23_rev-rec-scenarios.png)](./media/23_rev-rec-scenarios.png)

Open de pagina **Alle klanten** (**Klanten \> Klanten \> Alle klanten**), selecteer de klant **US\_SI\_0003** en selecteer **Transacties**. De openstaande factuur uit verkooporder 000036 wordt weergegeven. Als u het boekstuk selecteert, wordt de oorspronkelijke journaalregel weergegeven, niet de nieuwe journaalregel uit de hertoewijzing. De stornopost en de nieuwe journaalregel kunnen niet worden bekeken vanuit Klanten.

De tweede verkooporder wordt nu gefactureerd. De totale factuur voor de klant is voor $ 1099,00 + $ 71,44 btw = $ 1170,44. In de volgende afbeelding wordt de journaalregel weergegeven die is geboekt.

[![De pagina Boekstuktransacties met de geboekte journaalregel](./media/24_rev-rec-scenarios.png)](./media/24_rev-rec-scenarios.png)

Omdat het totaal van de opbrengst en verkopen meer dan $ 1170,44 is, wordt het verschil geboekt voor -$ 130,17. Met dit bedrag wordt het saldo van de vereffeningsrekening voor gedeeltelijke factuuropbrengst gewist. Dat saldo wordt na de hertoewijzing in de nieuwe journaalregel geboekt.
