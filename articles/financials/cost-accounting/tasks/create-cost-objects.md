--- 
title: Kostenobjecten maken
description: "Deze procedure laat zien hoe u kostenobjecten maakt door het importeren van financiële dimensies van Dynamics 365 for Finance and Operations, Enterprise edition-kostenplaatsen in Kostprijsboekhouding via een gegevensconnector."
author: ShylaThompson
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CAMDimension, CAMAXFinancialDimensionMemberProviderConfiguration, CAMDimensionMember
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 5d43274aed2edbb91fd4e399cb8d45e91646b055
ms.contentlocale: nl-nl
ms.lasthandoff: 09/29/2017

---
# <a name="create-cost-objects"></a>Kostenobjecten maken 

[!include [task guide banner](../../includes/task-guide-banner.md)]

Deze procedure laat zien hoe u kostenobjecten maakt door het importeren van financiële dimensies van Dynamics 365 for Finance and Operations, Enterprise edition-kostenplaatsen in Kostprijsboekhouding via een gegevensconnector. Het demobedrijf USMF wordt gebruikt om deze procedure te maken. Deze procedure is voor een Kostprijsboekhoudingsfunctie die in versie 1611 van Dynamics 365 for Operations is toegevoegd.


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


