--- 
title: Leveranciersbetalingen maken en exporteren met de ISO20022-betalingsindeling
description: In deze procedure ziet u hoe betalingsregels voor SEPA-kredietoverdracht kunnen worden gemaakt in het betalingsjournaal van de leverancier en hoe een bestand met leveranciersbetalingen kan worden gegenereerd door middel van het ISO2022-kredietoverdrachtvoorbeeld.
author: mrolecki
manager: AnnBe
ms.date: 10/24/2016
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
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 7cc90bc86cd489b124a806c480632dd53ba47f3f
ms.contentlocale: nl-nl
ms.lasthandoff: 09/29/2017

---
# <a name="create-and-export-vendor-payments-using-iso20022-payment-format"></a>Leveranciersbetalingen maken en exporteren met de ISO20022-betalingsindeling

[!include [task guide banner](../../includes/task-guide-banner.md)]

In deze procedure ziet u hoe betalingsregels voor SEPA-kredietoverdracht kunnen worden gemaakt in het betalingsjournaal van de leverancier en hoe een bestand met leveranciersbetalingen kan worden gegenereerd door middel van het ISO2022-kredietoverdrachtvoorbeeld. 

Het demobedrijf dat wordt gebruikt om deze procedure te maken is DEMF.

Dit is de vijfde van vijf taken die het leveranciersbetalingproces toelichten door middel van elektronische rapportageconfiguraties. Deze procedure is voor een functie die in versie 1611 van Dynamics 365 for Operations is toegevoegd.


## <a name="create-payment-lines"></a>Betalingsregels maken
1. Ga naar Leveranciers > Betalingen > Betalingsjournaal.
2. Klik op Nieuw.
3. Markeer in de lijst de geselecteerde rij.
4. Typ of selecteer een waarde in het veld Naam.
5. Klik op Regels.
6. Klik op Betalingsvoorstel.
7. Klik op Betalingsvoorstel maken.
8. Breid de sectie Op te nemen records uit.
9. Klik op Filter.
10. Selecteer in de lijst de rij voor de tabel Leveranciers en het veld Leveranciersrekening.
11. Typ of selecteer een waarde in het veld Criteria.
    * U kunt willekeurige criteria toepassen om van leverancierstransacties te selecteren; gebruik in dit voorbeeldgebruik DE-001 als leveranciersrekening.  
12. Klik op OK.
13. Klik op OK.
14. Klik op Betalingen maken.

## <a name="generate-an-iso20022-payment-file"></a>Een ISO20022-betalingsbestand genereren


