---
title: Hertoewijzing van opbrengsttoerekening - Scenario 3
description: In dit onderwerp wordt een hertoewijzingsscenario besproken waarin een nieuwe regel wordt toegevoegd aan een bestaande gefactureerde verkooporder. Wanneer een nieuw artikel aan een contract wordt toegevoegd, kan het worden toegevoegd aan een nieuwe verkooporder of aan de bestaande verkooporder.
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
ms.openlocfilehash: 51646d27fe8c343c99360815d22949ffe0757979
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2021
ms.locfileid: "5003349"
---
# <a name="revenue-recognition-reallocation--scenario-3"></a>Hertoewijzing van opbrengsttoerekening - Scenario 3

[!include [banner](../includes/banner.md)]

In dit onderwerp wordt een hertoewijzingsscenario besproken waarin een nieuwe regel wordt toegevoegd aan een bestaande gefactureerde verkooporder. Wanneer een nieuw artikel aan een contract wordt toegevoegd, kan het worden toegevoegd aan een nieuwe verkooporder of aan de bestaande verkooporder. Dit scenario laat ook zien wat er gebeurt wanneer Klanten wordt bijgewerkt vanwege de hertoewijzing.

Voor dit scenario is de optie **Factuurcorrecties boeken naar Klanten** ingesteld op **Ja** op het tabblad **Opbrengsttoerekening** van de pagina **Grootboekparameters** (**Opbrengsttoerekening \> Instellen \> Grootboekparameters**).

[![De optie Factuurcorrecties boeken naar Klanten is ingesteld op Ja](./media/25_rev-rec-scenarios.png)](./media/25_rev-rec-scenarios.png)

Er wordt een verkooporder gemaakt voor de klant US\_SI\_0003. De klant koopt een laptop (artikelnummer S0012) en een ondersteuningsplan voor de laptop (artikelnummer S0008, Doorlopende technische service). De opbrengst voor de laptop wordt onmiddellijk toegerekend. De opbrengst voor het ondersteuningsplan wordt uitgesteld en over 12 maanden toegerekend, zoals gedefinieerd door het datumbereik in het contract.

[![Verkooporderregels voor de laptop en het ondersteuningsplan](./media/26_rev-rec-scenarios.png)](./media/26_rev-rec-scenarios.png)

De verkooporder wordt bevestigd. Aangezien voor beide artikelen toewijzing van de opbrengstprijs is ingesteld, wordt de opbrengstprijs berekend wanneer de verkooporder wordt bevestigd. U kunt de toegekende opbrengst weergeven op de pagina **Opbrengstprijstoewijzing** (selecteer **Opbrengstprijstoewijzing** op de pagina **Verkooporder** in het actievenster op het tabblad **Beheren** in de groep **Opbrengsttoerekening**). De opbrengst voor de laptop wordt als bedrag van $ 1008,01 naar de opbrengstrekening geboekt. De opbrengst voor het ondersteuningsplan wordt als bedrag van $ 190,99 naar de rekening voor uitgestelde opbrengst geboekt. Het totaal van de opbrengstprijzen moet gelijk zijn aan het totaal van de regels die zijn ingesteld om de opbrengstprijstoewijzing vast te leggen ($ 1199,00).

[![De pagina Opbrengstprijstoewijzing](./media/27_rev-rec-scenarios.png)](./media/27_rev-rec-scenarios.png)

De verkooporder wordt volledig gefactureerd. In de volgende afbeelding wordt de journaalregel weergegeven die voor de factuur is geboekt.

[![Journaalregel voor de volledig gefactureerde verkooporder](./media/28_rev-rec-scenarios.png)](./media/28_rev-rec-scenarios.png)

Het schema voor opbrengsttoerekening wordt ook gemaakt. Na twee maanden bestaat er voor twee maanden toegerekende opbrengst voor het ondersteuningsplan.

[![De pagina Opbrengsttoerekeningsschema nadat twee maanden zijn verstreken](./media/29_rev-rec-scenarios.png)](./media/29_rev-rec-scenarios.png)

Op dit moment besluit de klant om installatieservices (artikelnummer S0001) toe te voegen. Dit artikel wordt toegevoegd aan de bestaande verkooporder. De klant wordt gevraagd te bevestigen dat hij/zij de volledig gefactureerde verkooporder wil wijzigen en hij/zij selecteert **Ja**.

[![Verkooporder nadat de regel voor installatieservices is toegevoegd](./media/30_rev-rec-scenarios.png)](./media/30_rev-rec-scenarios.png)

Als dit nieuwe artikel de enige wijziging in het contract van de klant is, kan het hertoewijzingsproces nu worden uitgevoerd. Selecteer in de verkooporder de optie **Prijs opnieuw toewijzen met nieuwe orderregels** om de pagina **Prijs opnieuw toewijzen met nieuwe orderregels** te openen. Selecteer alle verkooporderregels voor deze verkooporder en selecteer vervolgens **Hertoewijzing bijwerken**. In de kolom **Opnieuw toegewezen bedrag** wordt de nieuwe opbrengstprijs voor elke verkooporderregel weergegeven.

[![Nieuwe opbrengstprijzen op de pagina Prijs opnieuw toewijzen met nieuwe orderregels](./media/31_rev-rec-scenarios.png)](./media/31_rev-rec-scenarios.png)

Selecteer vervolgens **Verwacht boekstuk** om de journaalregels weer te geven. Omdat de optie **Factuurcorrecties boeken naar Klanten** is ingesteld op **Ja** op de pagina **Grootboekparameters**, worden deze journaalregels naar Grootboek geboekt via het creditdocument en wordt er een nieuwe factuur gemaakt in Klanten.

[![Journaalregels op de pagina Verwacht boekstuk](./media/32_rev-rec-scenarios.png)](./media/32_rev-rec-scenarios.png)

Op de pagina **Verwacht boekstuk** wordt in de laatste vier regels de oorspronkelijke journaalregel uit de geboekte factuur teruggeboekt. De eerste vijf regels zijn de nieuwe journaalregels die zijn geboekt voor de factuur. Het is belangrijk dat u begrijpt dat er geen nieuwe factuur wordt weergegeven voor de klant. Na de hertoewijzing moet de klant nog steeds $ 1276,94 betalen. Dit is het bedrag dat in de nieuwe journaalregel naar Klanten moet worden geboekt. De tegenrekeningsbelasting en de opbrengst of uitgestelde opbrengst zijn gelijk aan $ 995,83 + $ 188,69 + $ 77,94 = $ 1262,46. De opbrengst of het uitgestelde opbrengstbedrag is gewijzigd vanwege de hertoewijzing. Het verschil van $ 14,48 wordt geboekt naar een vereffeningsrekening voor gedeeltelijke factuuropbrengst. Dit saldo wordt gewist wanneer de factuur wordt geboekt voor het nieuwe artikel dat aan de verkooporder is toegewezen.

Selecteer **Verwerken** om de hertoewijzing te voltooien. Er wordt een boekingsdatum ingevoerd. Nadat de hertoewijzing is voltooid, wordt op de pagina **Opbrengstprijstoewijzing** de prijshertoewijzing voor alle drie de artikelen weergegeven.

[![Prijshertoewijzing voor alle drie de artikelen op de pagina Opbrengstprijstoewijzing](./media/33_rev-rec-scenarios.png)](./media/33_rev-rec-scenarios.png)

Het schema voor opbrengsttoerekening is bijgewerkt op basis van de nieuwe prijs van opbrengsthertoewijzing. Open de pagina **Opbrengstherkenningsschema** vanuit de verkooporder. Eerder waren er 13 regels voor artikel S0008 (een schema van twaalf maanden is toegewezen aan dit artikel). Er zijn nu 39 regels: de 13 oorspronkelijke schemaregels, 13 schemaregels voor terugboeking en 13 regels die zijn gebaseerd op de nieuwe opbrengstprijs.

[![Bijgewerkte pagina Opbrengsttoerekeningsschema met 39 regels voor artikel S0008](./media/34_rev-rec-scenarios.png)](./media/34_rev-rec-scenarios.png)

Wanneer u **Boekstuk** selecteert, wordt in het factuurjournaal de oorspronkelijke journaalregel weergegeven. Als u de stornopost en de nieuwe journaalregel uit de verkooporder wilt weergeven, selecteert u **Opbrengstcorrecties** in het actievenster en vervolgens **Boekstuk**.

Open de pagina **Alle klanten** (**Klanten \> Klanten \> Alle klanten**), selecteer de klant **US\_SI\_0003** en selecteer **Transacties**. Op de pagina **Klanttransacties** worden de oorspronkelijke factuur (000006), het terugboekingsdocument (000006-1) en de nieuwe factuur (000006-2) weergegeven. De oorspronkelijke factuur en het terugboekingsdocument worden met elkaar vereffend en hebben een saldo van 0 (nul). Bekijk het boekstuk voor elk document om het effect in Grootboek te bekijken.

[![Oorspronkelijke factuur, terugboekingsdocument en nieuwe factuur op de pagina Klanttransacties](./media/35_rev-rec-scenarios.png)](./media/35_rev-rec-scenarios.png)

De verkooporder wordt opnieuw gefactureerd voor het artikel dat is toegevoegd. De totale factuur voor de klant is voor $ 300,00 + $ 19,50 btw = $ 319,50. In de volgende afbeelding wordt de journaalregel weergegeven die is geboekt.

[![De pagina Boekstuktransacties met de geboekte journaalregel](./media/36_rev-rec-scenarios.png)](./media/36_rev-rec-scenarios.png)

Omdat het totaal van de opbrengst en verkopen meer dan $ 319,50 is, wordt het verschil geboekt voor $ 14,48. Met dit bedrag wordt het saldo van de vereffeningsrekening voor gedeeltelijke factuuropbrengst gewist. Dat saldo was bijgewerkt in de nieuwe journaalregel die was geboekt na de hertoewijzing.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]