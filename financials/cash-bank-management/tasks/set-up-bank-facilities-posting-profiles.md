--- 
title: Bankfaciliteiten en boekingsprofielen voor borgstellingen instellen
description: Deze taak maakt een bankfaciliteit en boekingsprofiel dat nodig is om een borgstelling te verwerken.
author: kweekley
manager: AnnBe
ms.date: 02/10/2016
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
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: a4b7f54dfd4f88688691fd9294d71aaae121382b
ms.contentlocale: nl-nl
ms.lasthandoff: 07/27/2017

---
# <a name="set-up-bank-facilities-and-posting-profiles-for-letters-of-guarantee"></a>Bankfaciliteiten en boekingsprofielen voor borgstellingen instellen

[!include[task guide banner](../../includes/task-guide-banner.md)]

Deze taak maakt een bankfaciliteit en boekingsprofiel dat nodig is om een borgstelling te verwerken.



Bij deze taak wordt het demobedrijf USMF gebruikt. 




## <a name="general-ledger-parameter"></a>Grootboekparameter
1. Ga naar Contanten en bankbeheer > Instellingen > Parameters voor kas- en bankbeheer.
2. Vouw de sectie Bankdocument uit.
3. Selecteer de optie Borgstelling inschakelen.
4. Klik in het veld Transactiejournaal op de vervolgkeuzeknop om de zoekopdracht te openen.
5. Zoek en selecteer het gewenste record in de lijst.
6. Klik in de lijst op de koppeling in de geselecteerde rij.
7. Klik op het tabblad Nummerreeksen.
    * Nummerreekscode definiëren voor verwijzingen naar borgstellingsnummers en borgstellingstransacties  
8. Klik op Opslaan.
9. Sluit de pagina.

## <a name="create-bank-facility"></a>Bankfaciliteit maken
1. Ga naar Kas- en bankbeheer > Instellingen > Bankfaciliteiten.
2. Klik op Nieuw.
3. Voer in het veld Faciliteitsgroep de naam in van de bankfaciliteitsgroep voor de borgstellingstransactie.
4. Typ een waarde in het veld Omschrijving.
5. Klik op Opslaan.
6. Klik op het tabblad Faciliteitstypen.
7. Klik op Nieuw.
8. Voer in het veld Faciliteitstype de naam in van het type bankfaciliteit dat is gekoppeld aan de bankfaciliteitsovereenkomst.
9. Typ een waarde in het veld Omschrijving.
10. Klik in het veld Faciliteitsgroep op de vervolgkeuzeknop om de zoekopdracht te openen.
11. Zoek en selecteer het gewenste record in de lijst.
12. Klik in de lijst op de koppeling in de geselecteerde rij.
13. Selecteer een optie in het veld Faciliteitsaard.
14. Klik op Opslaan.
15. Sluit de pagina.

## <a name="bank-posting-profile"></a>Boekingsprofiel van bank
1. Ga naar Kas- en bankbeheer > Instellingen > Boekingsprofiel van bankdocumenten.
2. Klik op Nieuw.
3. Klik in het veld Rekening/groepsnummer op de vervolgkeuzeknop om de zoekopdracht te openen.
4. Zoek en selecteer het gewenste record in de lijst.
5. Klik in de lijst op de koppeling in de geselecteerde rij.
6. Selecteer in het veld Rekening vereffenen de hoofdrekening voor vereffening.
7. Selecteer in het veld Rekening voor toeslagen de rekening voor onkostentransacties.
8. Selecteer in het veld Margerekening de rekening voor de margetransactie.
9. Selecteer in het veld Liquidatierekening de liquiditeitsrekening voor de borgstellingstransactie. 
10. Klik op Opslaan.
11. Sluit de pagina.

