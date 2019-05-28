---
title: De ontvangst van goederen registreren voor de inkooporder
description: Deze procedure laat zien hoe u de ontvangst van goederen voor een inkooporder direct kunt registreren.
author: FrankDahl
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchCreateOrder, InventItemIdLookupPurchase, PurchEditLines
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: fdahl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 14d1d43479f9864d8fd5ed94a98a654e75eeedf0
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/15/2019
ms.locfileid: "1551901"
---
# <a name="record-the-receipt-of-goods-on-the-purchase-order"></a>De ontvangst van goederen registreren voor de inkooporder

[!include [task guide banner](../../includes/task-guide-banner.md)]

Deze procedure laat zien hoe u de ontvangst van goederen voor een inkooporder direct kunt registreren. Het is ook mogelijk om de productontvangst in het magazijn te registreren en deze later vast te leggen voor de inkooporder. Deze taak wordt gewoonlijk uitgevoerd door een inkoper of een leverancierscoördinator. Het voorbeeld dat in deze handleiding wordt weergegeven, kan worden gebruikt in het USMF-demobedrijf. Het voorbeeld bevat stappen om een eenvoudige inkooporder te maken zodat u de procedure als taakbegeleiding kunt afspelen. Als u de procedure op uw eigen gegevens gebruikt, begint u bij de subtaak Ontvangst van goederen registreren.


## <a name="prepare-a-new-purchase-order-for-receipt-of-goods"></a>Een nieuwe inkooporder voor de ontvangst van goederen voorbereiden
1. Ga naar Inkoop en sourcing > Inkooporders > Alle inkooporders.
2. Klik op Nieuw.
3. Typ in het veld Leveranciersrekening de waarde US-101.
4. Klik op OK.
5. Voer M0001 in het veld Artikelnummer in.
6. Typ 5 in het veld Hoeveelheid.
7. Klik in het actievenster op Inkoop.
8. Klik op Bevestigen.

## <a name="record-receipt-of-goods"></a>Ontvangst van goederen registreren
1. Klik in het actievenster op Ontvangen.
2. Klik op Productontvangstbon.
    * Met het veld Hoeveelheid kunt u verschillende opties voor de hoeveelheid selecteren die u wilt ontvangen. Als bijvoorbeeld eerder een hoeveelheid in het magazijn is geregistreerd, kunt u Geregistreerde hoeveelheid selecteren.  Gebruik de waarde van Bestelde hoeveelheid voor dit voorbeeld.   
3. Typ een willekeurige waarde in het veld Productontvangstbon.
    * Dit veld wordt gebruikt om een verwijzing in te voeren die als het boekstuk voor productontvangstbonjournaal wordt gebruikt.  
4. Vouw de sectie Regels uit.
5. Stel Hoeveelheid in op '4'.
    * Hier kunt u handmatig de hoeveelheid opgeven die voor elke regel in de order wordt ontvangen.  
6. Vouw de sectie Regels samen.
7. Klik op OK.
    * De goederen zijn nu geregistreerd zo ontvangen voor de inkooporder, en er is een productontvangstbonjournaal gemaakt als document om dit te reflecteren. U kunt de actie Productontvangstbon gebruiken om de journalen te controleren die bij de inkooporder zijn gemaakt en om te zien wat is ontvangen, en wanneer.  

