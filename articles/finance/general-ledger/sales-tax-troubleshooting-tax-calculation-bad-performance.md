---
title: De prestaties van de belastingberekening hebben invloed op transacties
description: Dit artikel bevat informatie over het oplossen van problemen die betrekking hebben op de prestatie van de belastingberekening en de gevolgen ervan op transacties.
author: shtao
ms.date: 04/07/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: kfend
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 3ee0e3a0f8d9c06760776719fbe49e684cb882cf
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8894901"
---
# <a name="tax-calculation-performance-affects-transactions"></a>Prestatie van de belastingberekening heeft gevolgen voor transacties

[!include [banner](../includes/banner.md)]

Soms ondervindt een transactie gevolgen door prestatieproblemen van de belastingberekening. Volg de stappen in de volgende secties zoals vereist om dit probleem op te lossen.

## <a name="review-the-transaction-line-count"></a>Bekijk het aantal transactieregels

Bepaal of de transactie een groot aantal regels heeft (bijvoorbeeld meer dan honderd). Als dat niet zo is, gaat u verder met de volgende sectie. Als de transactie meerdere honderden regels heeft, stel de belastingberekening uit. Zie [Uitgestelde belastingberekening inschakelen in journalen](enable-delayed-tax-calculation.md) voor meer informatie. 

Vervolgens kunt u bepalen of aan een van de volgende voorwaarden wordt voldaan:

- Er zijn importtransacties uit grote bestanden.
- Dezelfde transactie voor belastingberekening wordt tegelijkertijd verwerkt in meerdere sessies.
- De transactie heeft meerdere regels en de weergaven worden realtime bijgewerkt. Het veld **Berekend btw-bedrag** op de pagina **Algemeen journaal** wordt bijvoorbeeld in realtime bijgewerkt als er regelvelden worden veranderd.

   [![Het veld Berekend btw-bedrag op de pagina Journaalboekstuk.](./media/tax-calculation-bad-performance-impacts-transaction-Picture1.png)](./media/tax-calculation-bad-performance-impacts-transaction-Picture1.png)

Als aan een van deze voorwaarden is voldaan, stel de belastingberekening uit.

## <a name="review-the-call-stack"></a>Controleer de aanroepstapel

Controleer de aanroepstapel om te bepalen of de belastingberekening meerdere keren wordt aangeroepen. Als dit niet zo is, gaat u verder met de volgende sectie. Als de aanroepstapel meerdere keren wordt aangeroepen, volgt u deze stappen om de belastingberekeningstijden te verminderen.

1. Als er in het journaal rekening is gehouden met de transactie, stel dan de belastingberekening uit. Zie [Uitgestelde belastingberekening inschakelen in journalen](enable-delayed-tax-calculation.md) voor meer informatie.
2. Als de transactie een inkooporder is en de toepassingsversie is hoger dan 10.0.15, kunt u de belastingberekening uitstellen tot de definitieve berekening door het inschakelen van de flighting voor **PurchTableChangeMgmtDistributionUpdateOnToggle_KillSwitch**.

## <a name="review-the-call-stack-timeline"></a>Controleer de tijdlijn van de aanroepstapel

Controleer de tijdlijn van de aanroepstapel om te bepalen of de volgende problemen bestaan. Als dat zo is, kunt u het probleem oplossen door flighting in te schakelen voor **TaxUncommittedDoIsolateScopeFlighting**.

- De transactie zorgt ervoor dat het systeem niet meer reageert totdat de sessie is beëindigd. Daarom kan de transactie het belastingresultaat niet berekenen. In de volgende afbeelding ziet u het bericht 'Sessie beëindigd' dat u ontvangt.

    [![Bericht Sessie beëindigd.](./media/tax-calculation-bad-performance-impacts-transaction-Picture2.png)](./media/tax-calculation-bad-performance-impacts-transaction-Picture2.png)

- De methoden **TaxUncommitted** hebben meer tijd nodig dan andere methoden. In de volgende afbeelding heeft bijvoorbeeld de methode **TaxUncommitted::updateTaxUncommitted()** 43.347,42 seconden nodig, terwijl andere methoden maar 0,09 seconde nodig hebben.

    [![Duur van methode.](./media/tax-calculation-bad-performance-impacts-transaction-Picture3.png)](./media/tax-calculation-bad-performance-impacts-transaction-Picture3.png)

## <a name="customizing-and-calling-tax-calculation"></a>Belastingberekening aanpassen en aanroepen

Wanneer u een aanpassing maakt, moet u de belastingberekening bij de methode **insert()** of **update()** niet bij elke regel aanroepen. Belastingberekening moet worden aangeroepen op transactieniveau.

## <a name="determine-whether-customization-exists"></a>Bekijk of er een aanpassing bestaat

Als u de stappen in de vorige secties hebt voltooid, maar u hebt het probleem niet gevonden, bekijkt u of er een aanpassing bestaat. Als er geen aanpassing bestaat, opent u een ondersteuningsaanvraag bij Microsoft voor verdere ondersteuning.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
