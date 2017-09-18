--- 
title: Een productieorder gereedmelden
description: Deze procedure toont aan hoe u een productieorder gereedmeldt.
author: johanhoffmann
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 9b947a02be981155053e33a4ef20e19bf2a194a5
ms.openlocfilehash: ff651be006b4bbe205aa9937bd7927e37a83a558
ms.contentlocale: nl-nl
ms.lasthandoff: 07/27/2017

---
# <a name="report-a-production-order-as-finished"></a>Een productieorder gereedmelden

[!include[task guide banner](../../includes/task-guide-banner.md)]

Deze procedure toont aan hoe u een productieorder gereedmeldt. Het bedrijf van de demogegevens dat wordt gebruikt om deze procedure te maken is USMF. Dit is de zesde procedure van zeven die de productieorderlevenscyclus beschrijven.


## <a name="report-a-production-order-as-finished"></a>Een productieorder gereedmelden
1. Ga naar Productiebeheer > Productieorders > Alle productieorders.
    * Selecteer een productieorder met de status Gestart.  
2. Klik in het actievenster op Productieorder.
3. Klik op Gereedmelden.
    * Op deze pagina kunt u de hoeveelheid bevestigen van het eindproduct die moet worden gereedgemeld.  
4. Klik op het tabblad Algemeen.
5. Stel Goede hoeveelheid in op '18'.
6. Stel Slechte hoeveelheid in op '2'.
7. Selecteer 'Materiaal' in het veld Foutoorzaak.
8. Schakel selectievakje Taak beëindigen in of uit.
9. Schakel het selectievakje Fout accepteren in of uit.
10. Klik op OK.

## <a name="verify-the-report-as-finished-journal"></a>Het gereedmeldingsjournaal verifiëren
1. Klik in het actievenster op Weergeven.
2. Klik op Gereedgemeld.
3. Markeer in de lijst de geselecteerde rij.
4. Klik in de lijst op de koppeling in de geselecteerde rij.
    * Het gereedmeldingsjournaal is geboekt. Als u aan het journaal correcties wilt aanbrengen, kunt u handmatig een nieuw journaal maken waarin u wijzigingen kunt aanbrengen.  

