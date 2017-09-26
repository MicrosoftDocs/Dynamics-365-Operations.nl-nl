--- 
title: Kostenelementen maken
description: Er zijn verschillende manieren om kostenelementen in Kostprijsboekhouding te maken.
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
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 0b1045610881bc272798f1176fbca58731e5d43b
ms.contentlocale: nl-nl
ms.lasthandoff: 07/27/2017

---
# <a name="create-cost-elements"></a>Kostenelementen maken 

[!include[task guide banner](../../includes/task-guide-banner.md)]

Er zijn verschillende manieren om kostenelementen in Kostprijsboekhouding te maken. Deze procedure laat zien hoe u kostenelementen maakt door hoofdrekeningen te importeren via een gegevensconnector. Het demobedrijf USMF wordt gebruikt om deze procedure te maken. Deze procedure is voor een Kostprijsboekhoudingsfunctie die in versie 1611 van Dynamics 365 for Operations is toegevoegd.


## <a name="create-new-cost-elements"></a>Nieuwe kostenelementen maken
1. Ga naar Kostprijsboekhouding > Dimensies > Dimensies van kostenelement.
2. Klik op Nieuw.
3. Typ een waarde in het veld Naam.
4. Typ of selecteer een waarde in het veld Gegevensconnector voor dimensieleden.
5. Typ een waarde in het veld Omschrijving.
6. Klik op Opslaan.

## <a name="configure-the-data-connector"></a>De gegevensconnector configureren
1. Klik op Dimensielidprovider configureren.
2. Typ of selecteer een waarde in het veld Rekeningschema.
    * Selecteer Gedeeld om het gedeelde rekeningschema te gebruiken.  
3. Klik op Nieuw.
4. Markeer in de lijst de geselecteerde rij.
    * U kunt filters op rekeningen toepassen om aan de criteria te voldoen.  
5. Typ of selecteer een waarde in het veld Van hoofdrekening.
6. Typ of selecteer een waarde in het veld Naar hoofdrekening.
7. Klik op OK.

## <a name="import-main-accounts"></a>Hoofdrekeningen importeren
1. Klik op Dimensieleden importeren.
    * Hoofdrekeningen worden in Kostprijsboekhouding geïmporteerd en gebruikt als kostenelementen.  
2. Klik op OK.

## <a name="view-the-imported-accounts-as-cost-elements"></a>De geïmporteerde rekeningen als kostenelementen weergeven
1. Klik op Dimensieleden weergeven.
    * Geef in uw bedrijf de geïmporteerde grootboekrekeningen als kostenelementen weer om de kosten daarnaartoe te laten stromen.  


