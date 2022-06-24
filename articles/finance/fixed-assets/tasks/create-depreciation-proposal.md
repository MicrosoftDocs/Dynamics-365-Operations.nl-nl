---
title: Een afschrijvingsvoorstel maken
description: Dit artikel beschrijft hoe afschrijvingsbatchvoorstellen werken en verklaart hoe u afschrijving kunt voorstellen voor vaste activa.
author: abruer
ms.date: 08/01/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransAsset
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a1f39a1412c6f96fe0a8261602a88a6a3c3cd6b8
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8858491"
---
# <a name="create-a-depreciation-proposal"></a>Een afschrijvingsvoorstel maken

[!include [banner](../../includes/banner.md)]

Dit artikel beschrijft hoe afschrijvingsbatchvoorstellen werken en verklaart hoe u afschrijving kunt voorstellen voor vaste activa. Deze taak gebruikt het USMF-demobedrijf en de accountantsrol.


## <a name="create-a-depreciation-proposal"></a>Een afschrijvingsvoorstel maken
1. Ga in het navigatievenster naar **Vaste activa > Journaalboekingen > Afschrijvingsvoorstel maken**.
2. Selecteer in het veld **Journaalnaam** een optie in het vervolgkeuzemenu.
3. Voer een datum in het veld **Einddatum** in.

    - Selecteer de optie **Afschrijving samenvatten** als u maandelijkse afschrijvingen in één journaalregel wilt samenvatten.  
    - Als de waarde van Einddatum bijvoorbeeld 31 maart 2015 is, kan de volgende beschrijving worden gegenereerd: "Afschrijving sinds 31 januari 2015". Het veld **Datum** op de voorgestelde journaalregels wordt dan ingesteld op 31 maart 2015.  
    - Het afschrijvingsvoorstel kan worden gefilterd op activa, activagroep, of andere criteria met de optie **Filteren**.  
    - Wanneer u het formulier **Verwervingsvoorstellen of afschrijvingsvoorstellen maken voor vaste activa** gebruikt, kunt u de afschrijving in batches voorstellen. Dit is wat we voorstellen voor grotere voorstellen die meer systeembronnen gebruiken. Als u de batchoptie selecteert, kunt u in die tijd nog andere taken voltooien. Wanneer u op deze manier afschrijving voorstelt, wordt de afschrijving berekend voor waardemodellen voor vaste activa.  

4. Selecteer **Journaal maken**.

## <a name="review-depreciation-entries"></a>Afschrijvingsinvoer controleren
1. Ga in het navigatievenster naar **Modules > Vaste activa > Journaalboekingen > Vaste-activajournaal**.
2. Zoek en selecteer de gewenste record in de lijst.
3. Selecteer **Regels**
4. Selecteer **Boeken**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
