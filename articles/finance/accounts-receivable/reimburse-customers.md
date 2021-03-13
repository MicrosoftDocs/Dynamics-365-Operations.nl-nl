---
title: Klanten terugbetalen
description: In dit artikel wordt uitgelegd hoe u terugbetalingstransacties kunt maken voor een groep klanten. Als een klant een creditsaldo heeft, kunt u de klant het saldobedrag terugbetalen.
author: JodiChristiansen
manager: AnnBe
ms.date: 09/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTransCustPaym, LedgerJournalTransVendPaym
audience: Application User
ms.reviewer: roschlom
ms.custom: 14191
ms.assetid: 53533ee3-470e-458a-ac8b-3815aa4cb502
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ae6a3078743fc9cd43c71bc1d4531c0553ee53bb
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2021
ms.locfileid: "5012134"
---
# <a name="reimburse-customers"></a>Klanten terugbetalen

[!include [banner](../includes/banner.md)]

In dit artikel wordt uitgelegd hoe u terugbetalingstransacties kunt maken voor een groep klanten. Als een klant een creditsaldo heeft, kunt u de klant het saldobedrag terugbetalen. 

De volgende tabel geeft de vereisten weer waaraan moet worden voldaan voordat u start.

| Vereiste                                                            | Beschrijving |
|-------------------------------------------------------------------------|-------------|
| Geef het minimale terugbetalingsbedrag voor de rechtspersoon op.          | Voer op de pagina **Parameters van module Klanten** in het gebied **Algemeen** in het veld **Minimum voor terugbetaling** het minimumbedrag in dat voor de klant kan worden terugbetaald. |
| Optioneel: voeg een leveranciersrekening toe voor elke klant die kan worden terugbetaald. | Selecteer op de pagina **Klanten** op het sneltabblad **Overige details** in het veld **Leveranciersrekening** de leveranciersrekening voor de klant. |

Wanneer u terugbetalingstransacties maakt, wordt een leveranciersfactuur gemaakt voor het bedrag van het creditsaldo. Met het terugbetalingsproces wordt het creditsaldo voor de klantrekening verwijderd en wordt een te betalen saldo voor de leveranciersrekening gemaakt die met de klant overeenkomt.

1. Voer in Klanten het proces **Terugbetalings** (**Klanten \> Periodieke taken \> Terugbetalen**).
2. Als u alle transacties wilt groeperen, ongeacht de grootboekdimensies, stelt u de optie **Klant samenvatten** in op **Ja**. Als u alleen transacties met vergelijkbare grootboekdimensies wilt groeperen, stelt u de optie in op **Nee**.
3. Selecteer **Klanten met openstaande debettransacties opnemen** om klanten te selecteren met openstaande debetbedragen.
4. Als u specifieke klantrekeningen wilt terugbetalen, selecteert op het sneltabblad **Records die u wilt opnemen** de optie **Filter** en geeft u vervolgens de klantrekeningen op in de query.

    De creditbedragen worden overgebracht naar de leveranciersrekeningen van de klanten en worden verwerkt als normale betalingen. Als een klant geen leverancierrekening heeft, wordt automatisch een eenmalige leverancierrekening voor de klant gemaakt.

5. Als u de gemaakte terugbetalingstransacties wilt weergeven, gebruikt u het rapport **Terugbetaling** (**Klanten \> Query's en rapporten \> Terugbetalingsrapport**).
6. In Leveranciers maakt u een betaling voor de leveranciersfacturen die met het terugbetalingsproces zijn gemaakt. Zie [Overzicht van leveranciersbetalingen](../accounts-payable/Vendor-payments-workspace.md) voor informatie over het betalen van leverancers.
