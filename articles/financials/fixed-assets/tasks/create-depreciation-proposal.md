---
title: Afschrijvingsvoorstel maken
description: Deze procedure beschrijft hoe afschrijvingsbatchvoorstellen werken en verklaart hoe u afschrijving kunt voorstellen voor vaste activa.
author: abruer
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransAsset
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d11554ee5f26ef5a85e799194d2f75757a31c254
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/29/2019
ms.locfileid: "361286"
---
# <a name="create-depreciation-proposal"></a>Afschrijvingsvoorstel maken

[!include [task guide banner](../../includes/task-guide-banner.md)]

Deze procedure beschrijft hoe afschrijvingsbatchvoorstellen werken en verklaart hoe u afschrijving kunt voorstellen voor vaste activa. Deze taak gebruikt het USMF-demobedrijf en de accountantsrol.


## <a name="create-depreciation-proposal"></a>Afschrijvingsvoorstel maken
1. Ga naar Vaste activa > Journaalboekingen > Afschrijvingsvoorstel maken.
2. Klik in het veld Naam van journaal op de vervolgkeuzeknop om de zoekopdracht te openen.
3. Klik in de lijst op de koppeling in de geselecteerde rij.
4. Voer een datum in het veld Einddatum in.
    * Selecteer de optie Afschrijving samenvatten als u maandelijkse afschrijvingen in één journaalregel wilt samenvatten.  
    * Als de waarde van Einddatum bijvoorbeeld 31 maart 2015 is, kan de volgende beschrijving worden gegenereerd: 'Afschrijving sinds 31 januari 2015'. Het veld Datum op de voorgestelde journaalregels wordt dan ingesteld op 31 maart 2015.  
    * Het afschrijvingsvoorstel kan worden gefilterd op activa, activagroep, of andere criteria met de optie Filteren.  
    * Wanneer u het formulier Verwervingsvoorstellen of afschrijvingsvoorstellen maken voor vaste activa gebruikt, kunt u de afschrijving in batches voorstellen. Dit is wat we voorstellen voor grotere voorstellen die meer systeembronnen gebruiken. Als u de batchoptie selecteert, kunt u in die tijd nog andere taken voltooien. Wanneer u op deze manier afschrijving voorstelt, wordt de afschrijving berekend voor waardemodellen voor vaste activa.  
5. Klik op Journaal maken.

## <a name="review-depreciation-entries"></a>Afschrijvingsinvoer controleren
1. Ga naar Vaste activa > Journaalboekingen > Vaste-activajournaal.
2. Zoek en selecteer de gewenste record in de lijst.
3. Klik op Regels.
4. Klik op Boeken.

