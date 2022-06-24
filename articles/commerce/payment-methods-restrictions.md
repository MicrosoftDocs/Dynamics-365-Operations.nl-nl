---
title: Betalingsmethoden voor retouren zonder ontvangstbewijs beperken
description: In dit artikel wordt beschreven hoe bepaalde betalingstypen kunnen worden beperkt voor restitutie als de retouren worden gemaakt zonder ontvangstbewijs.
author: rapraj
ms.date: 03/05/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailTenderTypeTable
audience: Application User
ms.reviewer: josaw
ms.custom: 15831
ms.assetid: 465893a5-6b4f-4c5f-b305-db071df2d33f
ms.search.region: global
ms.search.industry: Retail
ms.author: yabinl
ms.search.validFrom: 2019-02-01
ms.dyn365.ops.version: AX 10.0.0, Retail Feb 2019 update
ms.openlocfilehash: 091d39ea9fe41d78b7f34f85ecd1894047e022d6
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8896948"
---
# <a name="restrict-payment-methods-for-returns-without-a-receipt"></a>Betalingsmethoden voor retouren zonder ontvangstbewijs beperken


[!include [banner](includes/banner.md)]

Elk betalingstype dat een detailhandelaar accepteert, moet worden geconfigureerd wanneer het systeem wordt ingesteld. In dit artikel wordt beschreven hoe bepaalde betalingstypen kunnen worden beperkt voor restitutie als de retouren worden gemaakt zonder ontvangstbewijs.

## <a name="set-up-payment-methods"></a>Betalingsmethoden instellen

Voor het instellen van betalingsmethoden moet u de volgende taken voltooien.
1. Maak de betalingsmethoden die door de gehele organisatie worden geaccepteerd.
2. Kaarttypen en kaartnummers voor de hele organisatie maken. Als creditcards of betaalpassen worden geaccepteerd, moet u één betalingsmethode maken voor kaarten en vervolgens de typen kaarten en kaartnummers voor de organisatie maken.
3. Stel betalingsmethoden voor winkel in. Koppel betalingsmethoden aan elke winkel en voer vervolgens de winkelspecifieke instellingen in voor elke betalingsmethode.
4. Betalingsmethoden via kaart instellen voor winkels. Voltooi de kaartinstellingen voor alle kaartbetalingsmethoden die door de winkel worden geaccepteerd.

![Winkel instellen.](media/NoReceiptReturns1.png "Instellen van detailhandelwinkel") 


## <a name="restrict-payment-methods-for-returns-without-a-receipt"></a>Betalingsmethoden voor retouren zonder ontvangstbewijs beperken

Stel voor elke betalingsmethode voor winkels op de pagina **Winkelbeheer** onder **Retouren zonder ontvangstbewijs** **Beperken voor restituties zonder ontvangstbewijs** in op **Ja**. 

De standaardwaarde van de wisselknop is **Nee**, waarmee wordt gegarandeerd dat de betalingsmethode is toegestaan voor restituties. 

Wanneer **Beperken voor restituties zonder ontvangstbewijs** is ingesteld op **Ja**, is de geselecteerde betalingsmethode niet toegestaan voor restituties. 

![Betalingsmethode van winkel.](media/NoReceiptReturns3.png "Betalingsmethode detailhandelwinkel") 

> [!NOTE]
> Wanneer een kassamedewerker een betalingsmethode selecteert die is beperkt voor restitutie zonder ontvangstbewijs, verschijnt een bericht om de acceptabele betalingsmethoden te controleren.

![Acceptabele betalingsmethoden.](media/NoReceiptReturns4.png "Acceptabele betalingsmethoden") 

Als een transactie zowel een retour met een ontvangstbewijs als een retour zonder een ontvangstbewijs heeft, worden de beperkingsvoorwaarden niet afgedwongen omdat de transactie een retourwerkstroom met een ontvangstbewijs is. 



[!INCLUDE[footer-include](../includes/footer-banner.md)]