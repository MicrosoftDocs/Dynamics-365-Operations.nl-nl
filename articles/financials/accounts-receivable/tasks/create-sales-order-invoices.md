---
title: Facturen van verkooporder maken
description: Deze taakbegeleiding beschrijft het factureren van een verkooporder, waaronder samenvoegen van facturen en batchverwerking.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesTableListPage, SalesEditLines,  SysQueryForm, SysRecurrence
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5a57d204c0dcb44cbce7a0cc4d2f00b75b57e219
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/15/2019
ms.locfileid: "1565201"
---
# <a name="create-sales-order-invoices"></a>Facturen van verkooporder maken

[!include [task guide banner](../../includes/task-guide-banner.md)]

Deze taakbegeleiding beschrijft het factureren van een verkooporder, waaronder samenvoegen van facturen en batchverwerking. Bij deze procedure wordt het demobedrijf USMF gebruikt.


## <a name="create-an-invoice-from-a-sales-order"></a>Maak een factuur van een verkooporder
1. Ga naar Klanten > Orders > Verzonden maar niet gefactureerde verkooporders.
2. Selecteer een verkooporder in de lijst. 
3. Klik in het actievenster op Factuur.
4. Klik op Factuur.
    * Merk op dat aan deze verkooporder meerdere pakbonnen zijn gekoppeld. Het bevat alleen het woord <multiple> in plaats van het pakbonnummer.  
5. Vouw de sectie Parameters uit.
    * Het boeken moet worden ingesteld op Ja om de factuur te boeken. U kunt het boeken ook uitschakelen en de factuur alleen afdrukken. Echter, u kunt hetzelfde resultaat verwezenlijken door een pro-formafactuur in plaats van een factuur te maken.  
    * Deze optie wordt gebruikt voor batchtaken. De query wordt uitgevoerd wanneer de batchtaak wordt uitgevoerd.    
6. Selecteer Na in het veld Afdrukken.
7. Selecteer Ja voor Factuur afdrukken.
    * Afdrukbeheer kan meerdere kopieën van de factuur afdrukken en de factuur ook via e-mail verzenden als PDF-bestand.  
8. Selecteer Samenvatten in het veld Toeslagen afdrukken.
9. Selecteer Saldo in het veld Kredietlimiet controleren.
10. Klik op Annuleren.

## <a name="combine-orders-into-a-single-invoice"></a>Combineer orders in één factuur
1. Ga naar Klanten > Orders > Alle verkooporders.
2. Zoek een klant die meerdere open facturen heeft.
3. Selecteer een openstaande verkooporder.
4. Selecteer een andere open verkooporder voor dezelfde klant.
5. Klik in het actievenster op Factuur.
6. Klik op Factuur.
7. Vouw de sectie Parameters uit.
8. Selecteer in het veld Hoeveelheid de optie 'Alle'.
    * Merk op dat er twee facturen in de overzichtssectie zijn vermeld. We voegen ze samen in één factuur.  
9. Selecteer Factuurrekening in het veld Overzicht bijwerken voor.
10. Klik op Schikken om de verkooporders samen te voegen in één factuur.
    * De twee verkooporders worden nu samengevoegd in één factuur.   
11. Klik op Annuleren.
12. Klik op Ja.

## <a name="post-invoices-in-a-batch"></a>Boek facturen in een batch
1. Ga naar Klanten > Facturen > Batchfacturering > Factuur.
2. Klik op Selecteren.
3. Klik op OK.
4. Klik op Batch.
5. Klik op Ja als u batchverwerking wilt inschakelen.
6. Klik op Terugkeerpatroon.
7. Dagen selecteren
8. Klik op OK.
9. Klik op OK.
10. Klik op Annuleren.
11. Klik op Ja.

