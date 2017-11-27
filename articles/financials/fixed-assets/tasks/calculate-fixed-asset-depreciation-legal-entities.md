--- 
title: Afschrijving van vaste activa in verschillende rechtspersonen berekenen
description: Deze procedure laat zien hoe u het afschrijvingsproces instelt en uitvoert voor meerdere rechtspersonen.
author: saraschi2
manager: AnnBe
ms.date: 11/02/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d804480167414cd038f8229db312dc9c52d131f8
ms.openlocfilehash: 4c45da124136b7fecb916d2ff9098c8ffeff6cb1
ms.contentlocale: nl-nl
ms.lasthandoff: 11/02/2017

---
# <a name="calculate-fixed-asset-depreciation-across-legal-entities"></a>Afschrijving van vaste activa in verschillende rechtspersonen berekenen

[!include[task guide banner](../../includes/task-guide-banner.md)]

Een afschrijving van vaste activa kan in één stap worden uitgevoerd voor alle rechtspersonen. Deze procedure laat zien hoe u het proces instelt en uitvoert voor meerdere rechtspersonen. Hiervoor wordt de rol Accountant gebruikt.  

Bij deze registratie wordt het demobedrijf USMF gebruikt.


Deeltaak voor stappen (16): afschrijvingsjournalen voor het hele bedrijf instellen 

1. U moet eerst de journalen instellen die in elke rechtspersoon moeten worden gebruikt in de afschrijving voor het hele bedrijf. Ga naar Vaste activa > Instellen > Parameters vaste activa. 
2. Vouw de sectie Voorstellen voor vaste activa uit. 
3. Maak een record met de journaalnaam die moet worden gebruikt voor elke boekingslaag in de rechtspersoon. Als boeken niet naar het grootboek worden geboekt, moet de boekingslaag Geen worden geselecteerd met het bijbehorende journaal. Klik op Toevoegen. 
4. Typ of selecteer een waarde in het veld Boekingslaag. 
5. Typ of selecteer een waarde in het veld Journaalnaam. 
6. Herhaal de journaalinstellingen op de pagina Vaste-activaparameters voor elke rechtspersoon. 

Deeltaak: afschrijving berekenen

1. Op de pagina Afschrijvingsvoorstel maken kunt u uw afschrijvingsjournaal voor rechtspersonen starten. Ga naar Vaste activa > Journaalboekingen > Afschrijvingsvoorstel maken. 
2. Typ of selecteer een waarde in het veld Boekingslaag. 
3. De journaalnaam wordt standaard ingesteld op basis van de vaste-activaparameters. De naam kan hier worden gewijzigd voor de huidige rechtspersoon. 
4. Voer een datum in het veld Einddatum in. 
5. Selecteer de rechtspersonen die in de afschrijvingsuitvoering moeten worden opgenomen. Alleen rechtspersonen met journalen die zijn ingesteld voor voorstellen voor vaste activa op de pagina Voorstellen voor vaste activa worden weergegeven in de lijst. 
6. Indien ingeschakeld worden met de optie Journalen boeken de afschrijvingsjournalen automatisch geboekt wanneer ze worden gemaakt. Als deze optie niet is geselecteerd, worden de journalen gemaakt, maar niet geboekt, zodat u de details vóór het boeken kunt bekijken. Selecteer Ja in het veld Journalen boeken. 
7. Filtervelden omvatten alle vaste activa, groepen en boeken voor de rechtspersonen die zijn geselecteerd voor deze afschrijvingsuitvoering. 
8. De optie Batchverwerking is standaard ingeschakeld. Als deze optie is ingeschakeld, wordt het proces voor maken en boeken van het afschrijvingsjournaal op de achtergrond uitgevoerd. 
9. Klik op Journaal maken. 
10. U moet de afschrijvingsjournalen bekijken die in de betreffende rechtspersonen zijn gemaakt. Ga naar Vaste activa > Journaalboekingen > Vaste-activajournaal.

