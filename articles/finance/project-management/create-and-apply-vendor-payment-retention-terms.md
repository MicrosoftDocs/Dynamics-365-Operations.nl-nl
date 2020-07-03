---
title: Inhoudingstermijnen voor leveranciersbetalingen maken en toepassen
description: Dit onderwerp bevat informatie over het instellen en beheren van inhoudingstermijnen leveranciersbetalingen.
author: kfend
manager: AnnBe
ms.date: 05/26/2020
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
ms.openlocfilehash: 0e14050a79220b5d02763a025040edb934489d00
ms.sourcegitcommit: cecd97fd74ff7b31f1a677e8fdf3e233aa28ef5a
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/28/2020
ms.locfileid: "3410209"
---
# <a name="create-and-apply-vendor-payment-retention-terms"></a>Inhoudingstermijnen voor leveranciersbetalingen maken en toepassen

[!include [banner](../includes/banner.md)] 

Het instellen van inhoudingstermijnen voor leveranciersbetalingen voor een project is handig wanneer uw organisatie een deel van de betalingen die aan een leverancier zijn gedaan wil inhouden. Bijvoorbeeld wanneer u de betaling aan een leverancier wilt inhouden totdat de geleverde producten aan uw verwachtingen voldoen. Wanneer u over een leverancierscontract onderhandelt, kunt u de voorwaarden voor betalingsinhouding aan de leverancier opgeven.

## <a name="create-vendor-payment-retention-terms"></a>Inhoudingstermijnen voor leveranciersbetaling maken

U kunt het percentage van een leveranciersbetaling voor inhouding invoeren dat u wilt inhouden en het percentage van de eerder ingehouden bedragen dat u wilt vrijgeven. Bedragen worden automatisch op leveranciersfacturen ingehouden, totdat het desbetreffende voltooiingsniveau is bereikt. Nadat u de inhoudingstermijnen voor een leverancier hebt ingesteld, kunt u deze toepassen op elk project voor die leverancier.

Gebruik de volgende stappen om inhoudingstermijnen voor leveranciersbetalingen in te stellen. 

1. Ga naar **Projectbeheer en boekhouding** > **Inhouding** > **Inhoudingstermijnen voor leveranciersbetaling**.
2. Selecteer **Nieuw** om een nieuwe inhoudingstermijn voor een leverancier toe te voegen. De waarde van **Regel-ID** voor de nieuwe voorwaarde wordt automatisch ingevoerd. 
3. Voer een korte omschrijving in het veld **Omschrijving** in en selecteer op het sneltabblad **Voorwaarden** de optie **Regel toevoegen** om waarden voor de volgende instellingen op te geven:

   - **Percentage geleverde eenheden**: voer een voltooiingspercentage voor de termijn in. Bedragen worden automatisch op leveranciersfacturen ingehouden totdat de voltooiingsfase van het project gelijk is aan het opgegeven percentage. Als u bijvoorbeeld 50,00 invoert, worden bedragen ingehouden totdat 50% van het project is voltooid.
   - **In te houden percentage**: voer een percentage van het bedrag van de leveranciersfactuur in dat ingehouden moet worden. Als u in dit veld bijvoorbeeld 10,00 invoert, wordt 10 procent van het bedrag op een leveranciersfactuur ingehouden totdat het project het voltooiingspercentage bereikt dat u instelt in het veld **Percentage geleverde eenheden**.
   - **Vrij te geven percentage**: selecteer **Regel toevoegen** om een percentage van eventuele eerder ingehouden bedragen in te voeren die moeten worden vrijgegeven bij het aangewezen voltooiingsniveau van het project.

> [!NOTE]
> Als er meer dan één mijlpaal is ingesteld voor verschillende voltooiingsniveaus van een project, voert u een afzonderlijke inhoudingstermijn voor leverancier in voor elke inhoudingsregel. Elke regel kan een ander inhoudingspercentage betekenen en een ander vrij te geven percentage voor elk aangewezen voltooiingsniveau van een project.

Nadat u inhoudingstermijnen voor een leverancier hebt ingesteld, kunt u deze toepassen op de termijnen voor een project.

## <a name="apply-vendor-retention-terms-to-a-project"></a>Inhoudingstermijnen voor leveranciers toepassen op een project

1. Ga naar **Projectbeheer en boekhouding** > **Projecten** > **Alle projecten** en open een project vanuit de projectlijstpagina.
2. Selecteer op het sneltabblad **Leveranciersovereenkomsten** de optie **Regel toevoegen**.
3. Selecteer in het veld **Rekeningcode** een van de volgende opties: 

   - **Tabel**: de inhoudingstermijnen voor leveranciers gelden voor één leverancier.
   - **Groep**: de inhoudingstermijnen voor een leverancier gelden voor alle leveranciers in een leveranciersgroep.
   - **Alle**: de inhoudingstermijnen voor een leverancier gelden voor alle leveranciers.

4. Selecteer in het veld **Leverancier/Leveranciersgroep** de leverancier of leveranciersgroep waarop de inhoudingstermijnen van toepassing zijn. Als u **Alle** hebt geselecteerd in de vorige stap is dit veld niet beschikbaar.
5. Selecteer in het veld **Inhoudingstermijnen voor leverancier** de inhoudingstermijnen die u in de vorige procedure hebt gemaakt.
6. Indien ook betalen bij betaling (PWP) is ingesteld bij het project voor die leverancier, voert u het drempelpercentage voor het project in het veld **PWP drempelpercentage** in.

De inhoudingsvoorwaarden voor leveranciers worden ook weergegeven op inkooporders die u voor de leverancier maakt.
