---
title: Gepostdateerde cheques instellen
description: In dit onderwerp wordt uitgelegd hoe u kunt opgeven of journaalposten voor gepostdateerde cheques moeten worden geboekt en welke boekingsjournalen moeten worden gebruikt om transacties en leveranciersbetalingen te wissen.
author: kweekley
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: BankParameters, VendPaymMode, CustPaymMode
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 645b474b8b4bd13cd47bef404cda002e6b29a1ba
ms.sourcegitcommit: 631d2cea52590af15f208e9af584446e85540fcf
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/07/2022
ms.locfileid: "8724836"
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
> [!NOTE]
> Als u een gepostdateerde cheque wilt boeken naar een bankrekening wanneer de sessiedatum later is dan of gelijk is aan de vervaldatum, moet u de functie **Vervaldatumvalidatie van boeking betalingsjournaal met gepostdateerde cheques naar een bankrekening** inschakelen. Met deze functie kunt u betalingsjournalen boeken voor leveranciers of klanten met gepostdateerde cheques, wanneer de sessiedatum later is dan of gelijk is aan de vervaldatum.
> 
> Bij het instellen van de **Betalingsmethode** (**Crediteuren > Betalingsinstellingen > Betalingsmethoden**) moet u de **Overbruggingsrekening** niet invullen. In dit geval wordt de tegenrekening gevuld met de bankrekening, die is ingesteld in **Betalingsmethode**.
>  
> Wanneer de functie is ingeschakeld en de sessiedatum eerder is dan de vervaldatum, wordt het volgende foutbericht weergegeven bij het boeken van een betalingsjournaal: 'Vervaldatum moet eerder zijn dan of gelijk zijn aan de sessiedatum als het type tegenrekening Bank is'. Als de functie niet is ingeschakeld, kunt u een betalingsjournaal met een gepostdateerde cheque maken wanneer de sessiedatum eerder is dan de vervaldatum.
> Deze functie is beschikbaar in versie 10.0.21 of hoger.    

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
