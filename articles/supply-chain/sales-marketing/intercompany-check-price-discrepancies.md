---
title: Prijsverschillen in intercompany-orders controleren
description: In dit artikel wordt uitgelegd hoe u prijsverschillen in intercompany-orders controleert
author: Henrikan
ms.date: 09/01/2021
ms.topic: article
ms.search.form: PurchTable, PurchTablePart, PurchLineOpenOrder
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: ca27e86545ba8179c595e55487dbbf49cd9ec528
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8890678"
---
# <a name="check-intercompany-order-price-discrepancies"></a>Prijsverschillen in intercompany-orders controleren

[!include [banner](../../includes/banner.md)]

U kunt deze procedure gebruiken om intercompany-orders op prijsverschillen te controleren.

1. Ga naar **Inkoopbeheer \> Periodiek \> Opschonen \> Prijsverschillen in intercompany-order controleren**.
1. Stel een batchtaak in als dat nodig is en selecteer vervolgens op **OK** om de prijzen en kortingen voor intercompany-verkoop- en inkooporders te controleren. Selecteer anders **Annuleren** om de pagina te sluiten zonder de controle uit te voeren.

    > [!TIP]
    > Eventuele problemen met synchronisatie of prijzen worden vermeld in een informatieve melding die wordt weergegeven. U kunt de informatieve melding ter referentie afdrukken.

1. Selecteer in de informatieve melding de relevante regel om de order in de huidige rechtspersoon te openen. Open de order in de gerelateerde rechtspersoon door **Intercompany** en vervolgens **Intercompany-inkooporder** of **Intercompany-verkooporder** te selecteren.

    > [!NOTE]
    > Ga als volgt te werk om het bijwerken van de intercompany-order toe te staan:
    >
    > 1. Ga naar **Klanten \> Klanten \> Alle klanten**.
    > 1. Selecteer in het actievenster het tabblad **Algemeen** en selecteer vervolgens **Intercompany**.
    > 1. Selecteer op de pagina **Intercompany** de optie **Inkooporderbeleid** of **Verkooporderbeleid**.
    > 1. Selecteer **Bewerking van prijs toestaan** en **Bewerking van korting toestaan** in beide gebieden.

1. Open de relevante intercompany-order waar u de prijs wilt bewaren.
1. Wijzig voor elke orderregel het veld **Eenheidsprijs** en stel deze vervolgens weer in op de oorspronkelijke waarde. Stel de oorspronkelijke waarde van het veld **Korting** voor de regel in en stel de waarde weer opnieuw in en wijzig ook de relevante velden **Toeslagen op inkopen** of **Toeslagen op verkopen** en stel ze weer opnieuw in. Door de waarden weer op de oorspronkelijke waarden in te stellen en vervolgens weer opnieuw in te stellen, worden de prijzen, kortingen en toeslagen van deze intercompany-orderregel gesynchroniseerd naar de intercompany-orderregel waarnaar wordt verwezen zodat ze automatisch worden afgestemd.

    > [!NOTE]
    > Deze synchronisatie is alleen geldig als de intercompany-verkooporder niet is gefactureerd. Als de intercompany-verkooporder is geboekt als factuur en er een klantfactuurjournaal is gemaakt, moeten wijzigingen rechtstreeks op de intercompany-inkooporderregels worden uitgevoerd door de prijzen, kortingen en diverse toeslagen op dezelfde waarden in te stellen als die op het intercompany-klantfactuurjournaal. Als u dit niet doet, kan de intercompany-inkooporder niet als factuur worden geboekt, omdat de ordertotalen niet overeenkomen.

1. Herhaal de procedure totdat alle intercompany-inkooporders en intercompany-verkooporders zijn gesynchroniseerd.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
