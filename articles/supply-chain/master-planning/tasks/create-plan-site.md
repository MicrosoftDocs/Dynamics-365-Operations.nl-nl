---
title: Een plan voor een vestiging maken
description: De productieplanner berekent het materiaal en de capaciteitsbehoeften voor de productie van een specifiek artikel.
author: t-benebo
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, ReqCreatePlanWorkspace, ReqTransPlanCard, ReqTransPOUrgentFormPart, SysQueryForm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 01c8330fc15074eb59762dac73d0b176bd7faadc
ms.sourcegitcommit: ad1afc6893a8dc32d1363395666b0fe1d50e983a
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/23/2022
ms.locfileid: "8469500"
---
# <a name="create-a-plan-for-a-site"></a>Een plan voor een vestiging maken

[!include [banner](../../includes/banner.md)]

De productieplanner berekent het materiaal en de capaciteitsbehoeften voor de productie van een specifiek artikel. Nadat de sourcingsuggesties zijn gemaakt, vinden productieplanners de orders in de vestiging waarvoor zij een planning maken en zij fiatteren de orders, waarbij met de urgente orders wordt begonnen. De meest urgente orders zijn orders die op de huidige datum moeten worden gefiatteerd. Gebruik het demobedrijf USMF om deze taken uit te voeren.


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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]