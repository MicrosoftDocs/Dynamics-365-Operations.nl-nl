---
title: Activummetingen
description: In dit onderwerp wordt uitgelegd hoe u metingtypen voor activa maakt in Activabeheer.
author: johanhoffmann
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetObjectCounterPart, EntAssetObjectCounterLookup, EntAssetCounterType, EntAssetObjectCounterTotals
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: fc515615afaa172e1832508d79e202b166f134a9171a0a35ea4f372f9d19b7e2
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/05/2021
ms.locfileid: "6723570"
---
# <a name="counters"></a>Tellers

[!include [banner](../../includes/banner.md)]

In dit onderwerp wordt uitgelegd hoe u tellertypen maakt in Activabeheer. Tellertypen worden gebruikt om tellerregistraties te maken voor activa, bijvoorbeeld met betrekking tot het aantal productie-uren of de hoeveelheid die op het activum wordt geproduceerd. De activatypen zijn gerelateerd aan de tellertypen. Dit betekent dat een teller alleen voor een activum kan worden gebruikt als de teller is ingesteld voor het activumtype dat met het activum wordt gebruikt.

Voordat u tellerregistraties voor activa kunt maken, maakt u in **Tellers** eerst de tellertypen die u wilt gebruiken. Vervolgens kunt u tellerregistraties voor activa maken in **Tellers**. 

Tellers kunnen worden gebruikt in onderhoudsplannen. Een onderhoudsplanregel kan van het type "Teller" zijn, bijvoorbeeld als het gaat om het aantal productie-uren of de geproduceerde hoeveelheid. 

Een tellerregistratie kan handmatig of automatisch worden bijgewerkt op basis van productie-uren of de geproduceerde hoeveelheid. Een teller kan worden ingesteld voor het gebruiken van een van deze drie bijwerkmethoden (geselecteerd in het veld **Bijwerken** in **Tellers**):
  
- Handmatig: u moet de waarden van de teller handmatig registreren.  
- Productie-uren: de teller wordt automatisch bijgewerkt op basis van het aantal productie-uren.  
- Productiehoeveelheid: de teller wordt automatisch bijgewerkt op basis van de geproduceerde hoeveelheid.  

>[!NOTE]
>Als geproduceerde hoeveelheid wordt gebruikt, worden *alle* geregistreerde artikelen opgenomen in de tellerregistratie, zowel de goede artikelen als artikelen met fouten. Het is altijd mogelijk om een handmatige registratie van de tellers te doen, als dat nodig is.

## <a name="create-counter-types-for-asset-counter-registrations"></a>Tellertypen maken voor registraties van activatellers

1. Selecteer **Activabeheer** > **Instellen** > **Activumtypen** > **Tellers**.
2. Selecteer **Nieuw** om een nieuw tellertype te maken.
3. Geef een id op in het veld **Teller** en een tellernaam in het veld **Naam**.
4. Selecteer op het sneltabblad **Algemeen** een tellereenheid in het veld **Eenheid**.
5. Selecteer in het veld **Bijwerken** de bijwerkmethode die voor de teller moet worden gebruikt.
6. Selecteer "Ja" op de wisselknop **Tellerwaarden overnemen** als onderliggende activa in een activastructuur automatisch tellerregistraties moeten overnemen van het bovenliggende activum.
7. Selecteer in het veld **Totaal samengevoegd** de totaliseringsmethode die moet worden gebruikt voor een teller met dit tellertype. "Totaal" is de standaardselectie die wordt gebruikt om voortdurend geregistreerde waarden aan de totale waarde toe te voegen. "Gemiddelde" kan worden gebruikt als een teller is ingesteld om een drempel te bewaken, bijvoorbeeld met betrekking tot temperatuur, trillingen of slijtage van een activum. 
8. In het veld **Afwijking boven** voegt u in procenten het hoogste niveau voor validatie in als handmatige tellerregistraties binnen een verwacht bereik liggen. De validatie is gebaseerd op een lineaire toename van bestaande tellerregistraties.
9. In het veld **Afwijking onder** voegt u in procenten het laagste niveau voor validatie in als handmatige tellerregistraties binnen een verwacht bereik liggen. De validatie is gebaseerd op een lineaire afname van bestaande tellerregistraties.
10. Selecteer in het veld **Type** het type bericht (informatie, waarschuwing, fout) dat moet worden weergegeven als afwijkingen buiten het gedefinieerde bereik optreden bij handmatige tellerregistraties.
11. Voeg op het sneltabblad **Activumtypen** de activumtypen toe die de teller kunnen gebruiken.
12. Voeg op het sneltabblad **Gerelateerde activumtellers** de teller toe die u automatisch wilt bijwerken wanneer deze teller wordt bijgewerkt.


>[!NOTE]
>Een gerelateerde activummeting wordt alleen automatisch bijgewerkt als voor de bijbehorende teller het activumtype, waaraan deze is gerelateerd, is vermeld in de instellingen voor de teller. Bijvoorbeeld: u stelt een teller in voor "Productie-uren" en voegt het activumtype "Truckmotor" toe. Wanneer de teller wordt bijgewerkt, wordt een samenhangende teller "Olie" ook bijgewerkt met dezelfde tellerwaarden. De instellingen in **Tellers** omvatten de instellingen voor "Uren". Ook moet voor de teller "Olie" het activumtype "Truckmotor" worden toegevoegd aan het sneltabblad **Activumtypen** om de relatie met de teller te garanderen. Zie de onderstaande schermafbeeldingen voor een voorbeeld van de instellingen voor de tellers voor Uren en Olie.

Wanneer activumtypen worden toegevoegd aan een teller van het type **Tellers**, wordt die teller automatisch toegevoegd aan de activumtypen op het sneltabblad **Tellers** in [Activumtypen](../setup-for-objects/object-types.md).

![Figuur 1.](media/071-setup-for-objects.png)



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]