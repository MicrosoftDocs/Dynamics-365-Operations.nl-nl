---
title: De ontvangst van goederen registreren voor de inkooporder
description: In dit artikel wordt uitgelegd hoe u de ontvangst van goederen voor een inkooporder direct kunt registreren.
author: GalynaFedorova
ms.date: 07/09/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart, PurchCreateOrder, InventItemIdLookupPurchase, PurchEditLines
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: gfedorova
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 22baf6d0f6db04b3c6ce3c09ee8cb286e9a1e590
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8882455"
---
# <a name="record-the-receipt-of-goods-on-the-purchase-order"></a>De ontvangst van goederen registreren voor de inkooporder

[!include [banner](../../includes/banner.md)]

In dit artikel wordt uitgelegd hoe u de ontvangst van goederen voor een inkooporder direct kunt registreren. Het is ook mogelijk om de productontvangst in het magazijn te registreren en deze later vast te leggen voor de inkooporder. Deze taak wordt gewoonlijk uitgevoerd door een inkoper of een leverancierscoördinator. Het voorbeeld dat in deze handleiding wordt weergegeven, kan worden gebruikt in het USMF-demobedrijf. Het voorbeeld bevat stappen om een eenvoudige inkooporder te maken zodat u de procedure als taakbegeleiding kunt afspelen. Als u de procedure met uw eigen gegevens gebruikt, begint u bij de subtaak **Ontvangst van goederen registreren**.


## <a name="prepare-a-new-purchase-order-for-receipt-of-goods"></a>Een nieuwe inkooporder voor de ontvangst van goederen voorbereiden
1. Ga naar **Navigatievenster > Modules > Inkoopbeheer > Inkooporders > Alle inkooporders**.
2. Selecteer **Nieuw**.
3. Typ `US-101` in het veld **Leveranciersrekening**.
4. Selecteer **OK**.
5. Typ `M0001` in het veld **Artikelnummer**.
6. Typ `5` in het veld **Hoeveelheid**.
7. Selecteer in het actievenster de optie **Inkoop**.
8. Selecteer **Bevestigen**.

## <a name="record-receipt-of-goods"></a>Ontvangst van goederen registreren
1. Selecteer **Ontvangen** in het actievenster.
2. Selecteer **Productontvangstbon**. In het veld **Hoeveelheid** kunt u verschillende opties selecteren voor de hoeveelheid die u wilt ontvangen. Als bijvoorbeeld eerder een hoeveelheid in het magazijn is geregistreerd, kunt u **Geregistreerde hoeveelheid** selecteren. Gebruik voor dit voorbeeld de waarde van **Bestelde hoeveelheid**.
3. Vouw de sectie **Overzicht** uit.
4. Typ een willekeurige waarde in het veld **Productontvangstbon**. Dit veld wordt gebruikt om een verwijzing in te voeren die als het boekstuk voor productontvangstbonjournaal wordt gebruikt.  
5. Vouw de sectie **Regels** uit.
6. Stel **Hoeveelheid** in op '4'. Hier kunt u handmatig de hoeveelheid opgeven die voor elke regel in de order wordt ontvangen.  
7. Selecteer **OK**. De goederen zijn nu geregistreerd zo ontvangen voor de inkooporder, en er is een productontvangstbonjournaal gemaakt als document om dit te reflecteren. U kunt de actie Productontvangstbon gebruiken om de journalen te controleren die bij de inkooporder zijn gemaakt en om te zien wat is ontvangen, en wanneer.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]