---
title: Betalingsmethoden voor retouren zonder ontvangstbewijs beperken
description: In dit onderwerp wordt beschreven hoe bepaalde betalingstypen kunnen worden beperkt voor restitutie als de retouren worden gemaakt zonder ontvangstbewijs.
author: rapraj
manager: AnnBe
ms.date: 01/24/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailTenderTypeTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 15831
ms.assetid: 465893a5-6b4f-4c5f-b305-db071df2d33f
ms.search.region: global
ms.search.industry: Retail
ms.author: yabinl
ms.search.validFrom: 2019-02-01
ms.dyn365.ops.version: AX 10.0.0, Retail Feb 2019 update
ms.openlocfilehash: 1f84a6382453c0ba7540e618ad90ae1d3c684a2b
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/29/2019
ms.locfileid: "315907"
---
# <a name="restrict-payment-methods-for-returns-without-a-receipt"></a>Betalingsmethoden voor retouren zonder ontvangstbewijs beperken

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Elk betalingstype dat een detailhandelaar accepteert, moet worden geconfigureerd wanneer het systeem wordt ingesteld. In dit onderwerp wordt beschreven hoe bepaalde betalingstypen kunnen worden beperkt voor restitutie als de retouren worden gemaakt zonder ontvangstbewijs.

## <a name="set-up-payment-methods"></a>Betalingsmethoden instellen

Voor het instellen van betalingsmethoden moet u de volgende taken voltooien.
1. Maak de betalingsmethoden die door de gehele organisatie worden geaccepteerd.
2. Kaarttypen en kaartnummers voor de hele organisatie maken. Als creditcards of betaalpassen worden geaccepteerd, moet u één betalingsmethode maken voor kaarten en vervolgens de typen kaarten en kaartnummers voor de organisatie maken.
3. Stel betalingsmethoden voor winkel in. Koppel betalingsmethoden aan elke winkel en voer vervolgens de winkelspecifieke instellingen in voor elke betalingsmethode.
4. Betalingsmethoden via kaart instellen voor winkels. Voltooi de kaartinstellingen voor alle kaartbetalingsmethoden die door de winkel worden geaccepteerd.

![Detailhandelwinkel instellen](media/NoReceiptReturns1.png "Detailhandelwinkel instellen") 


## <a name="restrict-payment-methods-for-returns-without-a-receipt"></a>Betalingsmethoden voor retouren zonder ontvangstbewijs beperken

Stel voor elke betalingsmethode voor winkels op de pagina **Beheer van detailhandelwinkel** onder **Retouren zonder ontvangstbewijs** **Beperken voor restituties zonder ontvangstbewijs** in op **Ja**. 

De standaardwaarde van de wisselknop is **Nee**, waarmee wordt gegarandeerd dat de betalingsmethode is toegestaan voor restituties. 

Wanneer **Beperken voor restituties zonder ontvangstbewijs** is ingesteld op **Ja**, is de geselecteerde betalingsmethode niet toegestaan voor restituties. 

![Betalingsmethode detailhandelwinkel](media/NoReceiptReturns3.png "Betalingsmethode detailhandelwinkel") 

> [!NOTE]
> Wanneer een kassamedewerker een betalingsmethode selecteert die is beperkt voor restitutie zonder ontvangstbewijs, verschijnt een bericht om de acceptabele betalingsmethoden te controleren.

![Acceptabele betalingsmethoden](media/NoReceiptReturns4.png "Acceptabele betalingsmethoden") 

Als een transactie zowel een retour met een ontvangstbewijs als een retour zonder een ontvangstbewijs heeft, worden de beperkingsvoorwaarden niet afgedwongen omdat de transactie een retourwerkstroom met een ontvangstbewijs is. 
