---
title: Een afschrijvingsvoorstel maken
description: Dit onderwerp beschrijft hoe afschrijvingsbatchvoorstellen werken en verklaart hoe u afschrijving kunt voorstellen voor vaste activa.
author: abruer
manager: AnnBe
ms.date: 08/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransAsset
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 07337063c01f146c72ca6d9e0f9096907cdc9638
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/13/2020
ms.locfileid: "4442053"
---
# <a name="create-a-depreciation-proposal"></a>Een afschrijvingsvoorstel maken

[!include [banner](../../includes/banner.md)]

Dit onderwerp beschrijft hoe afschrijvingsbatchvoorstellen werken en verklaart hoe u afschrijving kunt voorstellen voor vaste activa. Deze taak gebruikt het USMF-demobedrijf en de accountantsrol.


## <a name="create-a-depreciation-proposal"></a>Een afschrijvingsvoorstel maken
1. Ga in het navigatievenster naar **Modules > Vaste activa > Journaalboekingen > Afschrijvingsvoorstel maken**.
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