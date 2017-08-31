--- 
title: Een plan voor een vestiging maken
description: De productieplanner berekent het materiaal en de capaciteitsbehoeften voor de productie van een specifiek artikel.
author: YuyuScheller
manager: AnnBe
ms.date: 06/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: d89d34d4d429faf87c70943961f7141a6258d482
ms.contentlocale: nl-nl
ms.lasthandoff: 07/27/2017

---
# <a name="create-a-plan-for-a-site"></a>Een plan voor een vestiging maken

[!include[task guide banner](../../includes/task-guide-banner.md)]

De productieplanner berekent het materiaal en de capaciteitsbehoeften voor de productie van een specifiek artikel. Nadat de sourcingsuggesties zijn gemaakt, vindt de productieplanner de orders in de vestiging waarvoor hij/zij een planning maakt en hij/zij fiatteert de orders, waarbij met de urgente orders wordt begonnen. De meest urgente orders zijn orders die op de huidige datum moeten worden gefiatteerd. Gebruik het demobedrijf USMF om deze taken uit te voeren.


## <a name="create-a-materials-and-capacity-plan-for-an-item"></a>Materialen en een capaciteitsplan maken voor een artikel
1. Klik op Hoofdplanning.
    * U moet naar het standaarddashboard navigeren.  
2. Klik op Uitvoeren.
3. Breid de sectie Op te nemen records uit.
4. Klik op Filter.
5. Markeer in de lijst de geselecteerde rij.
6. Typ een waarde in het veld Criteria.
    * Voorbeeld: D0001  
7. Klik op OK.
8. Klik op OK.
    * Dit kan enkele minuten in beslag nemen.  
9. Vernieuw de pagina.

## <a name="identify-the-urgent-planned-orders-for-the-item"></a>De urgente geplande orders voor het artikel identificeren
1. Open het filter van de kolom Artikelnummer.
2. Pas een filter toe op het veld Artikelnummer met een waarde D0001 en de filteroperator ´begint met´.
3. Open de kolomfilter Orderdatum.
4. Pas een filter op het veld "Orderdatum" met een waarde van huidige datum toe met behulp van de operator "is exact".

## <a name="firm-all-the-urgent-orders-for-the-item"></a>Alle urgente orders voor het artikel fiatteren
1. Selecteer of deselecteer alle rijen in de lijst.
2. Klik op Fiatteren.
3. Klik op OK.


