---
title: Betalen bij betaling instellen en gebruiken voor leveranciersbetalingen
description: In dit onderwerp wordt uitgelegd hoe u voorwaarden voor betalen bij betaling (PWP) kunt maken, zodat u gedeeltelijke leveranciersbetalingen kunt vrijgeven op basis van klantbetalingen.
author: RadhikaRS
manager: AnnBe
ms.date: 03/30/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: v-radsh
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 390cec62d2790ed10892669e283f2283c6b8e686
ms.sourcegitcommit: 399f128d90b71bd836a1c8c0c8c257b7f9eeb39a
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/23/2020
ms.locfileid: "3284108"
---
# <a name="set-up-and-use-pay-when-paid-vendor-payments"></a>Betalen bij betaling instellen en gebruiken voor leveranciersbetalingen

[!include [banner](../includes/banner.md)]

Als u een leverancier goedkeurt als toeleverancier, wilt u mogelijk de betaling aan de leverancier inhouden tot u voor het project bent betaald door uw klant. Ter ondersteuning van dit scenario stelt u voorwaarden van betalen bij betaling (PWP) in bij het instellen van de inkooporder met de leverancier.

Als een klant bijvoorbeeld een bedrag op een projectfactuur betaalt, kunt u een deel of het hele factuurbedrag van de leverancier vrijgeven. Stel PWP-voorwaarden in om op te geven dat de leverancier wordt betaald nadat u een bepaald percentage van de gerelateerde betaling van de klant ontvangt. Als u een gedeeltelijke betaling van een klant ontvangt, kunt u enkele van de bijbehorende leveranciersfacturen handmatig voor betaling vrijgeven.

In het volgende voorbeeld wordt het proces beschreven wanneer voorwaarden voor betalen bij betaling worden gebruikt.

## <a name="example"></a>Voorbeeld

Uw organisatie gaat ermee akkoord om een klant te voorzien van 100 computers waarop software is geïnstalleerd, voor een prijs van 150,00 USD per computer. Vervolgens verzoekt u een leverancier om u te voorzien van de computers waarop software is geïnstalleerd. Volgens de overeenkomst moet de klant de kwaliteit van de computers goedkeuren voordat de klant uw organisatie betaalt. Het beleid van uw organisatie is om leveranciers te betalen wanneer de klant u heeft betaald. Daarom stelt u het project zo in dat er een PWP-percentage van 100 procent wordt weergegeven.

De leverancier stuurt u de 100 computers waarop software is geïnstalleerd, samen met een factuur voor 10.000,00 USD. Omdat PWP-voorwaarden zijn ingesteld voor uw project, betaalt u de leverancier niet bij de ontvangst van de computers. In plaats daarvan stuurt u de computers samen met een factuur voor 15.000,00 naar de klant. De klant inspecteert de computers en de keurt het volledige bedrag van de projectfactuur goed.

Nadat u de volledige betaling van de klant hebt ontvangen, betaalt u het volledige bedrag 10.000,00 van de leveranciersfactuur.

## <a name="set-up-pwp-terms-for-a-project"></a>PWP-voorwaarden voor een project instellen

Wanneer u PWP-voorwaarden voor een project instelt, moet u, als percentage, het minimumbedrag opgeven dat een klant voor het project moet betalen voordat u de leverancier gaat betalen. Het drempelbedrag wordt automatisch berekend op de klantfacturen voor het project. Volg deze stappen om het drempelpercentage voor PWP-voorwaarden in te stellen.

1. Ga naar **Projectbeheer en boekhouding** \> **Projecten** \> **Alle projecten**.
2. Zoek en open het project waarvoor u PWP-voorwaarden wilt instellen.
3. Selecteer op het sneltabblad **Leveranciersovereenkomsten** de optie **Regel toevoegen**.
3. Selecteer in het veld **Rekeningcode** een van de volgende opties:

    - **Tabel**: de PWP-voorwaarden gelden voor één leverancier.
    - **Groep**: de PWP-voorwaarden gelden voor alle leveranciers in een leveranciersgroep.
    - **Alle**: de PWP-voorwaarden gelden voor alle leveranciers.

4. Als u in de vorige stap **Tabel** of **Groep** hebt geselecteerd, selecteert u in het veld **Leverancier/leveranciersgroep** de leverancier of leveranciersgroep waarop de PWP-voorwaarden van toepassing zijn. Als u **Alle** hebt geselecteerd in de vorige stap, kan het veld **Leverancier/leveranciersgroep** niet worden bewerkt.
5. Als inhoudingstermijnen voor leveranciers zijn ingesteld voor de leverancier in het project, selecteert u in het veld **Inhoudingstermijnen voor leverancier** de regel-id voor de inhoudingstermijnen.
6. Voer in het veld **PWP-drempelpercentage** de drempelpercentage voor het project in. Het percentage dat u invoert voor het project stelt het minimumbedrag in dat de klant aan u moet betalen voordat u de leverancier betaalt.

## <a name="create-a-po-that-has-pwp-terms"></a>Een inkooporder met PWP-voorwaarden maken

Wanneer u een factuur van de leverancier boekt en voor de leverancier PWP-voorwaarden gelden, worden deze weergegeven op de inkooporderregels. Voer de volgende stappen uit om een inkooporder te maken met PWP-voorwaarden.

1. Ga naar **Inkoop en sourcing** \> **Inkooporders** \> **Alle inkooporders**.
2. Selecteer **Nieuw** in het actievenster. Voer vervolgens in het dialoogvenster **Inkooporder maken** de vereiste informatie in en klik op **OK**.

    U kunt ook een bestaande inkooporder openen op de lijstpagina **Alle inkooporders**.

4. Bekijk op de pagina **Inkooporder** op het sneltabblad **Inkooporderregels** de details van de inkooporderregel voor de leverancier. De optie **Betalen bij betaling** wordt automatisch geselecteerd en de waarde voor **PWP-drempelpercentage** wordt automatisch gekopieerd naar het veld **PWP-drempelpercentage** op de pagina **Projecten** .
6. Als u de PWP-voorwaarden niet wilt toepassen op de leverancier voor een inkooporderregel , schakelt u de optie **Betalen bij betaling** uit. In dit geval wordt het veld **PWP-drempelpercentage** voor de inkooporderregel ingesteld op 0 (nul).

## <a name="update-a-customer-payment-and-pay-the-vendor"></a>Betalingsgegevens van een klant bijwerken en de leverancier betalen

Wanneer een leverancier het werk aan een project heeft voltooid en u een factuur stuurt, moet u de projectstatus en de klantfacturen bekijken om te bepalen of aan de PWP-voorwaarden voor het project is voldaan. Als aan de PWP-termijnen voor de leverancier is voldaan, kunt u bepalen welke regels op de leveranciersfactuur betaald worden, gebaseerd op de klantbetalingen voor het project. Als u de leverancier betaalt ook als niet is voldaan aan de PWP-voorwaarden, kunt u de PWP-voorwaarden op de pagina **Leveranciersfactuur met betalen bij betaling** overschrijven.

1. Ga naar **Projectbeheer en boekhouding** \> **Query's en rapporten** \> **Inhoudingsquery's** \> **Leveranciersfactuur met betalen bij betaling**.
2. Voer op de pagina **Leveranciersfactuur met betalen bij betaling** om het zoekveld waarden in om de leveranciersfactuur te vinden die u wilt bekijken en selecteer **Zoeken**.
3. Selecteer op het sneltabblad **Leveranciersfactuurregels** de regels die u wilt wijzigen.
4. Als aan de voorwaarden voor **Betalen bij betaling** wordt voldaan voor de factuurregel, selecteert u **Leveranciersbetaling vrijgeven**. Hiermee wordt de optie **Betaal bij betaling** gewist en de waarde in het veld **Gereed voor betaling** veranderd naar **Ja**.
