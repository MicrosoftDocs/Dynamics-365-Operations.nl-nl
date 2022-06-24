---
title: Subtotaal van orderoverzicht bevat geen btw voor toeslagen bij het gebruik van modules voor aangepaste orderoverzichten
description: Dit artikel biedt richtlijnen voor het oplossen van problemen die kunnen helpen als u aangepaste orderoverzichtmodules gebruikt en het subtotaal van het orderoverzicht geen belastingen op toeslagen bevat in het scenario 'Prijs inclusief btw'.
author: gvrmohanreddy
ms.date: 05/17/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2022-04-22
ms.openlocfilehash: 260dcb6bc1585615195e32adfcd1da6bfbca294e
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8848832"
---
# <a name="order-summary-subtotal-doesnt-include-taxes-on-charges-when-using-customized-order-summary-modules"></a>Subtotaal van orderoverzicht bevat geen btw voor toeslagen bij het gebruik van modules voor aangepaste orderoverzichten

Dit artikel biedt richtlijnen voor het oplossen van problemen die kunnen helpen als u aangepaste orderoverzichtmodules gebruikt en het subtotaal van het orderoverzicht geen belastingen op toeslagen bevat in het scenario 'Prijs inclusief btw'.

## <a name="description"></a>Description

In release Microsoft Dynamics 365 Commerce versie 10.0.27 zijn de volgende wijzigingen aangebracht in het scenario 'prijs inclusief btw' om u een consistente ervaring te bieden met de modules voor orderoverzichten op alle e-commercesitepagina's.

- Er zijn twee nieuwe velden toegevoegd: **TaxOnShippingCharge** en **TaxOnNonShippingCharges**.
- De API´s (Application Programming Interfaces) **GetSalesOrderBySalesId** en **GetSalesOrderByTransactionId** hebben nauwkeurige waarden voor de volgende velden in het scenario 'Prijs inclusief btw':

    - SubtotalSalesAmount
    - SubtotalAmountWithoutTax
    - SubtotalAmount
    - ShippingChargeAmount
    - OtherChargeAmount

Als u echter aangepaste orderoverzichtmodules gebruikt, kunnen deze wijzigingen gevolgen hebben voor de subtotaalwaarden van het orderoverzicht door belastingen op toeslagen niet op te nemen.

## <a name="resolution"></a>Oplossing

Als u aangepaste orderoverzichtmodules gebruikt en de wijzigingen die in het scenario 'prijs inclusief btw' zijn aangebracht niet wilt overnemen in Commerce versie 10.0.27 en later, volgt u de instructies in dit gedeelte.

Door terug te keren naar het vorige (vóór versie 10.0.27) orderoverzichtgedrag van de velden **salesTransaction.SubtotalAmount** en **salesTransaction.SubtotalAmountWithoutTax** herstelt u de opname van het totale toeslagbelastingbedrag (**TaxOnShippingCharge** en **TaxOnNonShippingCharges**) in de subtotaalbedragen (**SubtotalAmount** en **SubtotalAmountWithoutTax**).

Voer de volgende stappen uit om terug te keren naar het vorige orderoverzichtgedrag.

1. Open in Commerce headquarters de pagina Commerce-parameters (**Detailhandel en Commerce \> Instelling van hoofdkantoor \> Parameters \> Commerce-parameters**).
1. Selecteer in het linkernavigatievenster de optie **Configuratieparameters**.
1. Voeg de volgende configuratieparameters toe en stel de waarde van elk van de parameters in op **waar**:

    - IsLegacyTaxOnChargeInSubtotalAmountIncludedInTaxIncusiveEnabled
    - IsLegacyOrderSummaryHydrationEnabled

> [!NOTE]
> Als u de configuratieparameter **IsUpdatedPriceIncludesTaxSubtotalCalculationEnabled** eerder gebruikte en hetzelfde gedrag wilt behouden voor de eigenschap **order.NetAmountWithoutTax**, moet u ook de configuratieparameter **IsLegacyPriceIncludesTaxNetAmountWithoutTaxCalculationEnabled** toevoegen en de waarde ervan instellen op **waar**.

## <a name="additional-resources"></a>Aanvullende bronnen

[Btw-opsplitsing verbergen in orderoverzichten](../hide-taxes-breakup.md)
