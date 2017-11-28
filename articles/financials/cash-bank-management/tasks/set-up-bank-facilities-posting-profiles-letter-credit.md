--- 
title: Bankfaciliteiten en boekingsprofielen voor kredietbrief instellen
description: Deze procedure doorloopt het maken van een bankfaciliteit en boekingsprofiel dat vereist is om borgstellingen te verwerken.
author: kweekley
manager: AnnBe
ms.date: 10/27/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 18ad27eb673745d09569f6a49c8bc66132550f35
ms.openlocfilehash: 9ad19534091bdbd8924f90174b720d818b9ed778
ms.contentlocale: nl-nl
ms.lasthandoff: 10/27/2017

---
# <a name="set-up-bank-facilities-and-posting-profiles-for-letter-of-credit"></a>Bankfaciliteiten en boekingsprofielen voor kredietbrief instellen

[!include[task guide banner](../../includes/task-guide-banner.md)]

Deze procedure doorloopt het maken van een bankfaciliteit en boekingsprofiel dat vereist is om borgstellingen te verwerken. 

Bij deze taak wordt het demobedrijf USMF gebruikt.






## <a name="general-ledger-parameter"></a>Grootboekparameter
1. Ga naar Contanten en bankbeheer > Instellingen > Parameters voor kas- en bankbeheer.
2. Vouw de sectie Bankdocument uit.
3. Schakel de optie Importkredietbrief inschakelen in.
4. Schakel de optie Exportkredietbrief inschakelen in.
5. Klik op Opslaan.
6. Sluit de pagina.

## <a name="create-bank-facility"></a>Bankfaciliteit maken
1. Ga naar Kas- en bankbeheer > Instellingen > Bankfaciliteiten.
2. Klik op Nieuw.
3. Voer in het veld Faciliteitsgroep de groepsnaam van de bankfaciliteiten in.
4. Voer in het veld Beschrijving de beschrijving in van de bankfaciliteitsgroep.
5. Klik op Opslaan.
6. Klik op het tabblad Faciliteitstypen.
7. Klik op Nieuw.
8. Voer in het veld Faciliteittype een unieke code in.
9. Typ een waarde in het veld Omschrijving.
10. Klik in het veld Faciliteitsgroep op de vervolgkeuzeknop om de zoekopdracht te openen.
11. Zoek en selecteer het gewenste record in de lijst.
12. Klik in de lijst op de koppeling in de geselecteerde rij.
13. Selecteer in het veld Faciliteitsaard de aard van de bankfaciliteit.
14. Klik op Opslaan.
15. Sluit de pagina.

## <a name="bank-posting-profile"></a>Boekingsprofiel van bank
1. Ga naar Kas- en bankbeheer > Instellingen > Boekingsprofiel van bankdocumenten.
2. Klik op Nieuw.
3. Klik in het veld Rekening/groepsnummer op de vervolgkeuzeknop om de zoekopdracht te openen.
4. Zoek en selecteer het gewenste record in de lijst.
5. Klik in de lijst op de koppeling in de geselecteerde rij.
6. Selecteer de hoofdrekening voor vereffening.
    * Deze rekening wordt gebruikt bij de berekening van de cashflowprognose.  
7. Selecteer in het veld Rekening voor toeslagen de rekening voor onkostentransacties.
8. Selecteer in het veld Margerekening de rekening voor margetransacties.
    * Deze rekening wordt gedebiteerd wanneer de openingsmarge wordt geboekt en gecrediteerd wanneer de betaling wordt geboekt.  
9. Klik op Opslaan.


