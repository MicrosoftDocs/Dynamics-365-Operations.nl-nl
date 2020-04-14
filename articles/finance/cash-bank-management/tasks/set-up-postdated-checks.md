---
title: Gepostdateerde cheques instellen
description: In dit onderwerp wordt uitgelegd hoe u kunt opgeven of journaalposten voor gepostdateerde cheques moeten worden geboekt en welke boekingsjournalen moeten worden gebruikt om transacties en leveranciersbetalingen te wissen.
author: kweekley
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankParameters, VendPaymMode, CustPaymMode
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 22e67aa051b5ea8267df7efac40e007d0f11a83d
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/18/2020
ms.locfileid: "3141103"
---
# <a name="set-up-postdated-checks"></a>Gepostdateerde cheques instellen

[!include [banner](../../includes/banner.md)]

In dit onderwerp wordt uitgelegd hoe u kunt opgeven of journaalposten voor gepostdateerde cheques moeten worden geboekt en welke boekingsjournalen moeten worden gebruikt om transacties en leveranciersbetalingen te wissen. U kunt tijdelijke rekeningen opgeven voor uitgegeven cheques, ontvangen cheques en bronbelasting. Gepostdateerde cheques zijn cheques die worden uitgegeven om betalingen op een datum in de toekomst uit te voeren en te ontvangen. U kunt opgeven of de cheque vóór de vervaldatum in uw boekhoudingsstukken moet worden weerspiegeld.



De rol van deze procedure is penningmeester. Bij deze procedure wordt het demobedrijf USMF gebruikt.


## <a name="set-up-postdated-checks"></a>Gepostdateerde cheques instellen
1. Ga naar Contanten en bankbeheer > Instellingen > Parameters voor kas- en bankbeheer.
2. Klik op het tabblad Gepostdateerde cheques.
3. Schakel het selectievakje Gepostdateerde cheques inschakelen in of uit.
4. Schakel het selectievakje Journaalboekingen voor gepostdateerde cheques uitvoeren in of uit.
5. Geef in het veld Aflossingsrekening voor uitgegeven cheques de gewenste waarden op.
6. Geef in het veld Aflossingsrekening voor ontvangen cheques de gewenste waarden op.
7. Typ een waarde in het veld Algemeen journaal voor aflossingstransacties.
8. Typ een waarde in het veld Gepostdateerde cheques overboeken naar dit leveranciersbetalingsjournaal.
9. Geef de gewenste waarden op in het veld Aflossingsrekening bronbelasting.
10. Klik op Opslaan.
11. Sluit de pagina.
12. Ga naar Leveranciers > Betalingsinstelling > Betalingsmethoden.
13. Klik op Nieuw.
14. Typ een waarde in het veld Betalingsmethode.
15. Selecteer de optie Boeking van aflossing gepostdateerde cheque om aan te geven dat het bedrag van de cheque naar een tijdelijke rekening wordt geboekt.
16. Selecteer Bank in het veld Bankrekening.
    * De tegenrekening van de betalingsmethode zal een bank zijn.  
17. Geef in het veld Betalingsrekening de gewenste waarden op.
    * Selecteer de bankrekening die wordt gebruikt om het factuurbedrag af te trekken.  
18. Klik op Opslaan.
19. Sluit de pagina.

