---
title: Afschrijving van vaste activa in verschillende rechtspersonen berekenen
description: Een afschrijving van vaste activa kan in één stap worden uitgevoerd voor alle rechtspersonen.
author: saraschi2
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetParameters, AssetProposalDepreciation, DefaultDashboard, LedgerJournalTable
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8d228c387e8a6bf956f729a69e2296130db32dbd
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5210042"
---
# <a name="calculate-fixed-asset-depreciation-across-legal-entities"></a>Afschrijving van vaste activa in verschillende rechtspersonen berekenen

[!include [banner](../../includes/banner.md)]

Een afschrijving van vaste activa kan in één stap worden uitgevoerd voor alle rechtspersonen. Deze procedure laat zien hoe u het proces instelt en uitvoert voor meerdere rechtspersonen. Het gebruikt de rol Accountant en demogegevens voor de USMF-rechtspersoon.


## <a name="set-up-cross-company-depreciation-run-journals"></a>Afschrijvingsjournalen voor het hele bedrijf instellen
1. Ga naar Vaste activa > Instellen > Parameters vaste activa.
2. Vouw de sectie Voorstellen voor vaste activa uit.
3. Klik op Toevoegen.
4. Typ of selecteer een waarde in het veld Boekingslaag.
5. Typ of selecteer een waarde in het veld Journaalnaam.
    * Herhaal de journaalinstellingen op de pagina Vaste-activaparameters voor elke rechtspersoon.  

## <a name="depreciation-run"></a>Afschrijving uitvoeren
1. Ga naar Vaste activa > Journaalboekingen > Afschrijvingsvoorstel maken.
2. Typ of selecteer een waarde in het veld Boekingslaag.
    * De journaalnaam wordt standaard ingesteld op basis van de vaste-activaparameters. De naam kan hier worden gewijzigd voor de huidige rechtspersoon.  
3. Voer een datum in het veld Einddatum in.
    * Selecteer de rechtspersonen die in de afschrijvingsuitvoering moeten worden opgenomen.  
    * Alleen rechtspersonen met journalen die zijn ingesteld voor voorstellen voor vaste activa op de pagina Voorstellen voor vaste activa worden weergegeven in de lijst.  
4. Selecteer Ja in het veld Journalen boeken.
    * Filtervelden omvatten alle vaste activa, groepen en boeken voor de rechtspersonen die zijn geselecteerd voor deze afschrijvingsuitvoering.  
    * De optie Batchverwerking is standaard ingeschakeld. Als deze optie is ingeschakeld, wordt het proces voor maken en boeken van het afschrijvingsjournaal op de achtergrond uitgevoerd.  
5. Klik op Journaal maken.
6. Ga naar Vaste activa > Journaalboekingen > Vaste-activajournaal.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]