---
title: Kostenobjecten maken
description: Deze procedure laat zien hoe u kostenobjecten maakt door het importeren van financiële dimensies van kostenplaatsen in Kostprijsboekhouding via een gegevensconnector.
author: twheeloc
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: CAMDimension, CAMAXFinancialDimensionMemberProviderConfiguration, CAMDimensionMember
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 88196ea19488cd8572bf0e7883298317c9c84696
ms.sourcegitcommit: 5d1772bdeb21a9bec6dc49e64550aaf34127a4e2
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/10/2022
ms.locfileid: "8734125"
---
# <a name="create-cost-objects"></a>Kostenobjecten maken 

[!include [banner](../../includes/banner.md)]

Deze procedure laat zien hoe u kostenobjecten maakt door het importeren van financiële dimensies van kostenplaatsen in Kostprijsboekhouding via een gegevensconnector. Het demobedrijf USMF wordt gebruikt om deze procedure te maken. 


## <a name="create-new-cost-objects"></a>Nieuwe kostenobjecten maken
1. Ga naar **Kostprijsboekhouding > Dimensies > Dimensies van kostenobject**.
2. Klik op **Nieuw**.
3. Typ een waarde in het veld **Naam**.
4. Typ of selecteer een waarde in het veld **Gegevensconnector voor dimensieleden**.
5. Typ een waarde in het veld **Beschrijving**.
6. Klik op **Opslaan**.

## <a name="configure-the-data-connector"></a>De gegevensconnector configureren
1. Klik op **Dimensielidprovider configureren**.
    * Selecteer CostCenter om de CostCenter-dimensie in Kostprijsboekhouding te importeren.  
2. Selecteer Kostenplaats In het veld **Dimensienaam**.
3. Klik op **OK**.

## <a name="import-cost-centers"></a>Kostenplaatsen importeren
1. Klik op **Dimensieleden importeren**.
2. Klik op **OK**.

## <a name="view-the-imported-cost-centers"></a>De geïmporteerde kostenplaatsen weergeven
1. Klik op **Dimensieleden weergeven**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
