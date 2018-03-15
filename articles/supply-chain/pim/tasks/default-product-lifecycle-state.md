--- 
title: Een standaardstatus voor de productlevenscyclus maken
description: Deze procedure laat zien hoe u een standaardstatus voor een productlevenscyclus maakt en hoe u de standaardstatus koppelt aan vrijgegeven producten.
author: cvocph
manager: AnnBe
ms.date: 12/05/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d445ea2f2362f146a1e3e7bcf747898dc2cc89ba
ms.openlocfilehash: 06a6c7c8fa767edf6fdf50c3c971b6d767f8755f
ms.contentlocale: nl-nl
ms.lasthandoff: 02/08/2018

---
# <a name="create-a-default-product-lifecycle-state"></a>Een standaardstatus voor de productlevenscyclus maken

[!include[task guide banner](../../includes/task-guide-banner.md)]

Deze procedure laat zien hoe u een standaardstatus voor een productlevenscyclus maakt en hoe u de standaardstatus koppelt aan vrijgegeven producten.


## <a name="create-a-default-lifecycle-state"></a>Een standaardstatus voor de levenscyclus maken
1. Ga naar Productgegevensbeheer > Instellen > Levenscyclusstatus van product.
2. Klik op Nieuw.
3. Typ een waarde in het veld Status.
4. Selecteer Ja in het veld Standaard bij vrijgave aan rechtspersoon.
5. Typ een waarde in het veld Omschrijving.
6. Selecteer Nee in het veld Is actief voor planning.

> [!NOTE]
> Selecteer Nee, als u een nieuw vrijgegeven product niet wilt opnemen in de Hoofdplanning. Als het wel moet worden opgenomen in de Hoofdplanning, laat u de standaardwaarde Ja staan.  

## <a name="create-a-new-released-product"></a>Een nieuw vrijgegeven product maken
1. Sluit de pagina.
2. Ga naar Productgegevensbeheer > Producten > Vrijgegeven producten.
3. Klik op Nieuw.
4. Typ een waarde in het veld Productnummer.
5. Typ een waarde in het veld Productnaam.
6. Typ een waarde in het veld Zoeknaam.
7. Typ of selecteer een waarde in het veld Artikelmodelgroep.
8. Typ of selecteer een waarde in het veld Artikelgroep.
9. Typ of selecteer een waarde in het veld Opslagdimensiegroep.
10. Typ of selecteer een waarde in het veld Traceringsdimensiegroep.
11. Klik op OK.

> [!NOTE]
> De standaardstatus voor de productlevenscyclus is een algemene definitie.  

## <a name="change-the-product-to-an-active-state"></a>Het product wijzigen in een actieve status
1. Typ of selecteer een waarde in het veld Levenscyclusstatus van product.

> [!NOTE]
> Stel dat u een actieve status hebt ingesteld, dan kunt u nu de actieve status selecteren om toe te staan dat het product wordt gebruikt in de Hoofdplanning en in de berekening op stuklijstniveau. Uiteraard is dit alleen zinvol als de productgegevens zijn opgegeven die vereist zijn voor een consistente planning.  


