---
title: Facturen van verkooporder maken
description: Deze taakbegeleiding beschrijft het factureren van een verkooporder, waaronder samenvoegen van facturen en batchverwerking.
author: ShivamPandey-msft
ms.date: 06/25/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SalesTableListPage, SalesEditLines,  SysQueryForm, SysRecurrence
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8a6556838a2843f961e1538947a6eda090b94894ed4df8476ea60abeda8056b6
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/05/2021
ms.locfileid: "6771819"
---
# <a name="create-sales-order-invoices"></a>Facturen van verkooporder maken

[!include [banner](../../includes/banner.md)]

Deze taakbegeleiding beschrijft het factureren van een verkooporder, waaronder samenvoegen van facturen en batchverwerking. Bij deze procedure wordt het demobedrijf USMF gebruikt.


## <a name="create-an-invoice-from-a-sales-order"></a>Maak een factuur van een verkooporder
1. Ga naar het **Navigatiedeelvenster > Modules > Klanten > Orders > Verzonden maar nog niet gefactureerde verkooporders**.
2. Selecteer een verkooporder in de lijst. 
3. Klik in het **actievenster** op **Factuur > Genereren > Factuur**. Merk op dat aan deze verkooporder meerdere pakbonnen zijn gekoppeld. Het bevat alleen het woord <multiple> in plaats van het pakbonnummer.  
4. Vouw de sectie **Parameters** uit.
    - Het boeken moet worden ingesteld op Ja om de factuur te boeken. U kunt het boeken ook uitschakelen en de factuur alleen afdrukken. Echter, u kunt hetzelfde resultaat verwezenlijken door een pro-formafactuur in plaats van een factuur te maken.  
    - Deze optie wordt gebruikt voor batchtaken. De query wordt uitgevoerd wanneer de batchtaak wordt uitgevoerd.
5. Selecteer 'Na' in het veld **Afdrukken**.
6. Selecteer **Ja** voor **Factuur afdrukken**. Afdrukbeheer kan meerdere kopieën van de factuur afdrukken en de factuur ook via e-mail verzenden als PDF-bestand.  
7. Selecteer 'Samenvatten' in het veld **Toeslagen afdrukken**.
8. Selecteer 'Saldo' in het veld **Kredietlimiet controleren**.
9. Klik op **Annuleren**.

## <a name="combine-orders-into-a-single-invoice"></a>Combineer orders in één factuur
1. Ga naar **Navigatievenster > Modules > Klanten > Orders > Alle verkooporders**.
2. Zoek een klant die meerdere open facturen heeft.
3. Selecteer meerdere openstaande verkooporders van dezelfde klant.
4. Klik in het **actievenster** op **Factuur > Genereren > Factuur**.
5. Vouw de sectie **Parameters** uit.
6. Selecteer in het veld **Hoeveelheid** de optie Alle. Merk op dat er twee facturen in de overzichtssectie zijn vermeld. We voegen ze samen in één factuur.  
7. Selecteer 'Factuurrekening' in het veld **Overzicht bijwerken voor**.
8. Klik op **Schikken** om de verkooporders samen te voegen in één factuur. De twee verkooporders worden nu samengevoegd in één factuur.   
9. Klik op **Annuleren**.
10. Klik op **Ja**.

## <a name="post-invoices-in-a-batch"></a>Boek facturen in een batch
1. Ga naar het **Navigatievenster > Modules > Klanten > Facturen > Batchfacturering > Factuur**.
2. Klik op **Selecteren**.
3. Klik op **OK**.
4. Klik op **Batch**.
5. Selecteer **Ja** voor **Batchverwerking**.
6. Klik op **Terugkeerpatroon**.
7. Selecteer **Dagen**.
8. Klik op **OK**.
9. Klik op **OK**.
10. Klik op **Annuleren**.
11. Klik op **Ja**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]