--- 
title: Betalingen aanmaken voor klanten met mandaten voor automatische afschrijving
description: In deze procedure ziet u hoe u een automatisch ISO20022-afschrijvingsbestand genereert voor een klant waarvoor automatische afschrijving is geconfigureerd en die een factuur moet betalen.
author: mrolecki
manager: AnnBe
ms.date: 10/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: acd6a8076288d8d1d1aa05af33e306c6a29780f7
ms.contentlocale: nl-nl
ms.lasthandoff: 09/29/2017

---
# <a name="create-payments-for-a-customer-who-have-direct-debit-mandates"></a>Betalingen aanmaken voor klanten met mandaten voor automatische afschrijving

[!include [task guide banner](../../includes/task-guide-banner.md)]

In deze procedure ziet u hoe u een automatisch ISO20022-afschrijvingsbestand genereert voor een klant waarvoor automatische afschrijving is geconfigureerd en die een factuur moet betalen. Maken en boeken van een factuur zijn optioneel. In plaats van een te betalen factuur kunt u een mandaat in een journaal selecteren voordat een betalingsbestand wordt gegenereerd, om een scenario met vooruitbetaling door de klant te ondersteunen.



Het demobedrijf dat wordt gebruikt om deze procedure te maken is DEMF.



Dit is de vijfde van vijf procedures die het proces weergeven voor innen van klantbetalingen via configuraties voor elektronische rapportage. U moet alle voorgaande taken hebben voltooid voordat u deze taak kunt uitvoeren. U moet eerst configuraties voor elektronische rapportage van klantbetaling importeren, methode van betalingen configureren en uw bedrijfs- en klantgegevens instellen. 


## <a name="post-a-free-text-invoice-with-direct-debit-information"></a>Een vrije-tekstfactuur met gegevens voor automatische afschrijving boeken
1. Ga naar Klanten > Facturen > Alle vrije-tekstfacturen.
2. Klik op Nieuw.
3. Typ of selecteer een waarde in het veld Klantrekening.
    * Selecteer bijvoorbeeld DE-010.  
4. Typ of selecteer een waarde in het veld Betalingsmethode.
    * 2: Huidige gebeurtenis: het huidige product wordt verzonden. selecteer Elektronisch.  
5. Typ of selecteer een waarde in het veld Mandaat-id voor automatische afschrijving.
6. Klik op Regel toevoegen.
7. Typ een waarde in het veld Omschrijving.
8. Geef in het veld Hoofdrekening de gewenste waarden op.
9. Voer in het veld Eenheidsprijs een getal in.
10. Klik op Boeken.
11. Klik op OK.

## <a name="create-a-payment"></a>Een betaling maken
1. Ga naar Klanten > Betalingen > Betalingsjournaal.
2. Klik op Nieuw.
3. Typ of selecteer een waarde in het veld Naam.
4. Klik op Regels.
5. Klik op Betalingsvoorstel.
6. Klik op Betalingsvoorstel maken.
7. Breid de sectie Op te nemen records uit.
8. Klik op Filter.
9. Selecteer in de lijst de rij voor de tabel Klanttransacties en het veld Betalingsmethode.
    * U kunt alle criteria voor het selecteren van te betalen klanttransacties toepassen. Gebruik voor dit voorbeeld 'Elektronisch' als de betalingsmethode om transacties te filteren.  
10. Typ of selecteer een waarde in het veld Criteria.
11. Klik op OK.
12. Klik op OK.
13. Klik op Betalingen maken.

## <a name="generate-a-payment-file"></a>Een betalingsbestand genereren


