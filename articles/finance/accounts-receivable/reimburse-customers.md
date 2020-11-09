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
ms.search.scope: Core, Operations
ms.custom: 14191
ms.assetid: 53533ee3-470e-458a-ac8b-3815aa4cb502
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bceeaf99437f6ef66bd3b4e1710b469c262e693e
ms.sourcegitcommit: 9e7ceb5604472f3088f611aa0360bd6a716db32b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4022538"
---
# <a name="reimburse-customers"></a>Klanten terugbetalen

[!include [banner](../includes/banner.md)]

In dit artikel wordt uitgelegd hoe u terugbetalingstransacties kunt maken voor een groep klanten. Als een klant een creditsaldo heeft, kunt u de klant het saldobedrag terugbetalen. 

De volgende tabel geeft de vereisten weer waaraan moet worden voldaan voordat u start.

| Vereiste                                                            | Beschrijving                                                                                                                                                                                 |
|-------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Geef het minimale terugbetalingsbedrag voor de rechtspersoon op.          | Voer op de pagina **Parameters van module Klanten** in het gebied **Algemeen** in het veld **Minimum voor terugbetaling** het minimumbedrag in dat voor de klant kan worden terugbetaald. |
| Optioneel: voeg een leveranciersrekening toe voor elke klant die kan worden terugbetaald. | Selecteer op de pagina **Klanten** op het sneltabblad **Overige details** in het veld **Leveranciersrekening** de leveranciersrekening voor de klant.                                           |

Wanneer u terugbetalingstransacties maakt, wordt een leveranciersfactuur gemaakt voor het bedrag van het creditsaldo. Met het terugbetalingsproces wordt het creditsaldo voor de klantrekening verwijderd en wordt een te betalen saldo voor de leveranciersrekening gemaakt die met de klant overeenkomt.

1.  Voer in Klanten het proces **Terugbetaling** uit.
2.  Volg één van deze stappen:
    -   Als u wilt terugbetalen aan specifieke klantrekeningen, klikt u op **Selecteren** en geeft u de klantrekeningen in de query op.
    -   Klik op **OK** als u wilt terugbetalen aan alle klantrekeningen.

    De creditbedragen worden overgebracht naar de leveranciersrekeningen van de klanten en worden verwerkt als normale betalingen. Als een klant geen leverancierrekening heeft, wordt automatisch een eenmalige leverancierrekening voor de klant gemaakt.
3.  Als u de terugbetalingstransacties wilt weergeven die zijn gemaakt, gebruikt u de pagina **Terugbetaling**.
4.  In Leveranciers maakt u een betaling voor de leveranciersfacturen die met het terugbetalingsproces zijn gemaakt.




