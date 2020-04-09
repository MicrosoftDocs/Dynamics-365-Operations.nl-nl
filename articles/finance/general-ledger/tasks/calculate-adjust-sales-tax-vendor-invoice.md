---
title: Btw op een leveranciersfactuur berekenen en corrigeren
description: In dit onderwerp wordt uitgelegd hoe u de btw op een leveranciersfactuur in Dynamics 365 Finance aanpast.
author: twheeloc
manager: AnnBe
ms.date: 07/31/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransVendInvoice, VendTableLookup, TaxTmpWorkTrans
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2f3521f7bc56659fc6f7a6d47f581ddbfea16523
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/18/2020
ms.locfileid: "3139962"
---
# <a name="calculate-and-adjust-sales-tax-on-a-vendor-invoice"></a>Btw op een leveranciersfactuur berekenen en corrigeren

[!include [banner](../../includes/banner.md)]

In dit onderwerp wordt uitgelegd hoe u de btw op een leveranciersfactuur aanpast. Als het oorspronkelijke brondocument verschillende btw-bedragen bevat, zoals berekend, kunt u die bedragen aanpassen voor het boeken. Bij deze taak wordt het demobedrijf DEMF gebruikt.

1. Ga in het navigatiedeelvenster naar **Modules > Leveranciers > Facturen > Factuurjournaal**.
2. Selecteer **Nieuw**.
3. Selecteer in het veld **Naam** van de nieuwe rij een optie in het vervolgkeuzemenu.
4. Selecteer **Regels** in het actievenster.
5. Geef in het veld **Rekening** de gewenste waarden op.
6. Typ een waarde in het veld **Factuur**.
7. Voer in het veld **Krediet** een numerieke waarde in.
8. Geef in het veld **Tegenrekening** de gewenste waarden op.
9. Selecteer **Btw**.
10. Voer in het veld **Totaal werkelijk btw-bedrag** een getal in.
11. Op het tabblad **Correctie** kunnen de btw-bedragen per btw-code worden gecorrigeerd.
12. Selecteer **Werkelijke bedragen opnieuw instellen op basis van berekende**.
13. Selecteer **OK**.
14. Selecteer **Opslaan**.

