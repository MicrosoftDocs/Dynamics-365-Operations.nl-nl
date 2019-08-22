---
title: Activummetingen
description: In dit onderwerp wordt uitgelegd hoe u metingtypen voor activa maakt in Activabeheer.
author: josaw1
manager: AnnBe
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d9c445832a649c4f6a6642036ecab325e8aa2079
ms.sourcegitcommit: 747bcd25ce7c6c20ce9eaa0027e730f74d4fd6aa
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 07/23/2019
ms.locfileid: "1783189"
---
# <a name="asset-measures"></a>Activummetingen

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

In dit onderwerp wordt uitgelegd hoe u metingtypen voor activa maakt in Activabeheer. Metingtypen voor activa worden gebruikt om metingregistraties te maken voor activa, bijvoorbeeld met betrekking tot het aantal productieuren of de hoeveelheid die op het activum wordt geproduceerd. De activatypen zijn gerelateerd aan de metingtypen voor activa. Dit betekent dat een activummeting alleen voor een activum kan worden gebruikt als de activummeting is ingesteld voor het activumtype dat met het activum wordt gebruikt.

Voordat u metingregistraties voor activa kunt maken, maakt u in **Tellers** eerst de metingtypen voor activa die u wilt gebruiken. Vervolgens kunt u metingregistraties voor activa maken in **Activummetingen**. 

Activummetingen kunnen worden gebruikt in onderhoudsplannen. Een onderhoudsplanregel kan van het type "Teller" zijn, bijvoorbeeld als het gaat om het aantal productieuren of de geproduceerde hoeveelheid. 

Een registratie van activummeting kan handmatig of automatisch worden bijgewerkt op basis van productieuren of de geproduceerde hoeveelheid. Een activummeting kan worden ingesteld voor het gebruiken van een van deze drie bijwerkmethoden (geselecteerd in het veld **Bijwerken** in **Tellers**):
  
- Handmatig: u moet de waarden van de activummeting handmatig registreren.  
- Productieuren: de teller wordt automatisch bijgewerkt op basis van het aantal productieuren.  
- Productiehoeveelheid: de teller wordt automatisch bijgewerkt op basis van de geproduceerde hoeveelheid.  

>[!NOTE]
>Als geproduceerde hoeveelheid wordt gebruikt, worden *alle* geregistreerde artikelen opgenomen in de metingregistratie, zowel de goede artikelen als artikelen met fouten. Het is altijd mogelijk om een handmatige registratie van de activummetingen te doen, als dat nodig is.

## <a name="create-counter-types-for-asset-counter-registrations"></a>Tellertypen maken voor registraties van activatellers

1. Selecteer **Activabeheer** > **Instellen** > **Activumtypen** > **Tellers**.
2. Selecteer **Nieuw** om een nieuw metingtype voor activa te maken.
3. Geef een id op in het veld **Teller** en een tellernaam in het veld **Naam**.
4. Selecteer op het sneltabblad **Algemeen** een maateenheid in het veld **Eenheid**.
5. Selecteer in het veld **Bijwerken** de bijwerkmethode die voor de activummeting moet worden gebruikt.
6. Selecteer "Ja" op de wisselknop **Tellerwaarden overnemen** als onderliggende activa in een activastructuur automatisch de geregistreerde activummeting moeten overnemen van het bovenliggende activum.
7. Selecteer in het veld **Totaal samengevoegd** de totaliseringsmethode die moet worden gebruikt voor een activummeting met dit metingtype voor activa. "Totaal" is de standaardselectie die wordt gebruikt om voortdurend geregistreerde waarden aan de totale waarde toe te voegen. "Gemiddelde" kan worden gebruikt als een activummeting is ingesteld om een drempel te bewaken, bijvoorbeeld met betrekking tot temperatuur, trillingen of slijtage van een activum. 
8. In het veld **Afwijking boven** voegt u in procenten het hoogste niveau voor validatie in als handmatige registraties van activummetingen binnen een verwacht bereik liggen. De validatie is gebaseerd op een lineaire toename van bestaande registraties van activummetingen.
9. In het veld **Afwijking onder** voegt u in procenten het laagste niveau voor validatie in als handmatige registraties van activummetingen binnen een verwacht bereik liggen. De validatie is gebaseerd op een lineaire afname van bestaande registraties van activummetingen.
10. Selecteer in het veld **Type** het type bericht (informatie, waarschuwing, fout) dat moet worden weergegeven als afwijkingen buiten het gedefinieerde bereik optreden bij handmatige registraties van activummetingen.
11. Voeg op het sneltabblad **Activumtypen** de activumtypen toe die de activummeting kunnen gebruiken.
12. Voeg op het sneltabblad **Gerelateerde activummetingen** de activummetingen toe die u automatisch wilt bijwerken wanneer deze activummeting wordt bijgewerkt.


>[!NOTE]
>Een gerelateerde activummeting wordt alleen automatisch bijgewerkt als voor de bijbehorende activummeting het activumtype, waaraan deze is gerelateerd, is vermeld in de instellingen voor de activummeting. Bijvoorbeeld: u stelt een activummeting in voor "Productieuren" en voegt het activumtype "Truckmotor" toe. Wanneer de activummeting wordt bijgewerkt, wordt een samenhangende teller "Olie" ook bijgewerkt met dezelfde waarden van de activummeting. De instellingen in **Tellers** omvatten de instellingen voor "Uren". Ook moet voor de activummeting "Olie" het activumtype "Truckmotor" worden toegevoegd aan het sneltabblad **Activumtypen** om de relatie met de activummeting te garanderen. Zie de onderstaande schermafbeeldingen voor een voorbeeld van de instellingen voor de activummetingen voor Uren en Olie.

Wanneer activumtypen worden toegevoegd aan een activummeting van het type **Tellers**, wordt die activummeting automatisch toegevoegd aan de activumtypen op het sneltabblad **Tellers** in [Activumtypen](../setup-for-objects/object-types.md).

![Figuur 1](media/071-setup-for-objects.png)


