---
title: TaxTrans-record is niet gegenereerd
description: Dit onderwerp bevat informatie voor het oplossen van problemen wanneer een TaxTrans-record niet wordt gegenereerd.
author: qire
ms.date: 04/13/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 74987506699834d86703702106e5abf87bfa45da
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/11/2021
ms.locfileid: "6018776"
---
# <a name="taxtrans-record-isnt-generated"></a>TaxTrans-record is niet gegenereerd

[!include [banner](../includes/banner.md)]

Als u **Geboekte btw** voor een transactie selecteert, maar op de pagina **Geboekte btw** worden geen belastingregels weergegeven of er ontbreekt een belastingregel, is de **TaxTrans**-record mogelijk niet gegenereerd.

[![Pagina Geboekte btw zonder regelartikelen](./media/taxtrans-is-not-generated-Picture1.png)](./media/taxtrans-is-not-generated-Picture1.png)

Volg de stappen in de volgende secties zoals vereist om dit probleem op te lossen.

## <a name="check-the-sales-tax-before-you-post-the-transaction"></a>Controleer de btw voordat u een transactie boekt

1. Voordat u de transactie boekt, selecteert u op de pagina **Factuur boeken** de **Btw** om de berekening te controleren.

    [![Knop btw op de pagina Factuur boeken](./media/taxtrans-is-not-generated-Picture2.png)](./media/taxtrans-is-not-generated-Picture2.png)

2. Controleer op de pagina **Tijdelijke btw-transacties** het resultaat van de berekening. Als er geen belasting is berekend, ga naar [Belasting is niet berekend of belastingbedrag is nul](sales-tax-troubleshooting-tax-not-calculated-amount-zero.md).

## <a name="find-the-taxtrans-record-in-all-posted-sales-tax"></a>Zoek de TaxTrans-record in alle geboekte btw

1. Ga naar **Belasting** \> **Query's en rapporten** \> **Vragen over btw** > **Geboekte btw**.
2. Selecteer in de kolomkop **Boekstuk** het filtersymbool om de **TaxTrans**-record te zoeken.
3. Als u de btw-records heeft gevonden, controleert u de datum. Als de datum verschilt van de datum van de journaalkoptekst, opent u een Microsoft-serviceaanvraag voor extra ondersteuning.

    [![Pagina Geboekte btw](./media/taxtrans-is-not-generated-Picture4.png)](./media/taxtrans-is-not-generated-Picture4.png)

## <a name="debug-to-check-details"></a>Foutopsporing voor het controleren van details

1. Voor meer informatie over foutopsporing en te bepalen of **TmpTaxWorkTrans** en **TaxUncommitted** juist zijn gegenereerd, ga naar [Veldwaarde in TaxTrans is onjuist](sales-tax-troubleshooting-field-value-taxtrans-incorrect.md).
2. Als **TaxTmpWorkTrans** of **TaxUncommitted** juist zijn gegenereerd, voegt u een onderbrekingspunt toe bij **TaxPost::SaveAndPost()** en **Tax::SaveAndPost** om erachter te komen waarom **TaxTrans** niet is ingevoegd.

    [![Onderbrekingspunten toegevoegd in code](./media/taxtrans-is-not-generated-Picture5.png)](./media/taxtrans-is-not-generated-Picture5.png)

    [![Resultaten van toegevoegde onderbrekingspunten](./media/taxtrans-is-not-generated-Picture6.png)](./media/taxtrans-is-not-generated-Picture6.png)

## <a name="determine-whether-customization-exists"></a>Bekijk of er een aanpassing bestaat

Als u de stappen in de vorige secties hebt voltooid, maar u hebt het probleem niet gevonden, bekijkt u of er een aanpassing bestaat. Als er geen aanpassing bestaat, opent u een ondersteuningsaanvraag bij Microsoft voor verdere ondersteuning.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
