--- 
title: Kostenobjecten maken
description: "Deze procedure laat zien hoe u kostenobjecten maakt door het importeren van financiële dimensies van Dynamics 365 for Finance and Operations-kostenplaatsen in Kostprijsboekhouding via een gegevensconnector."
author: YuyuScheller
manager: AnnBe
ms.date: 10/25/2016
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
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: 21fa90557b665e0777935cc6bae8cd9f1c29cb60
ms.contentlocale: nl-nl
ms.lasthandoff: 03/26/2018

---
# <a name="create-cost-objects"></a>Kostenobjecten maken 

[!include[task guide banner](../../includes/task-guide-banner.md)]

Deze procedure laat zien hoe u kostenobjecten maakt door het importeren van financiële dimensies van Dynamics 365 for Finance and Operations-kostenplaatsen in Kostprijsboekhouding via een gegevensconnector. Het demobedrijf USMF wordt gebruikt om deze procedure te maken. Deze procedure is voor een Kostprijsboekhoudingsfunctie die in versie 1611 van Dynamics 365 for Operations is toegevoegd.


## <a name="create-new-cost-objects"></a>Nieuwe kostenobjecten maken
1. Ga naar Kostprijsboekhouding > Dimensies > Dimensies van kostenobject.
2. Klik op Nieuw.
3. Typ een waarde in het veld Naam.
4. Typ of selecteer een waarde in het veld Gegevensconnector voor dimensieleden.
5. Typ een waarde in het veld Omschrijving.
6. Klik op Opslaan.

## <a name="configure-the-data-connector"></a>De gegevensconnector configureren
1. Klik op Dimensielidprovider configureren.
    * Selecteer CostCenter om de CostCenter-dimensie in Kostprijsboekhouding te importeren.  
2. Selecteer Kostenplaats In het veld Dimensienaam.
3. Klik op OK.

## <a name="import-cost-centers"></a>Kostenplaatsen importeren
1. Klik op Dimensieleden importeren.
2. Klik op OK.

## <a name="view-the-imported-cost-centers"></a>De geïmporteerde kostenplaatsen weergeven
1. Klik op Dimensieleden weergeven.


