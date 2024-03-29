---
title: Bankfaciliteiten en boekingsprofielen voor kredietbrief instellen
description: Deze procedure doorloopt het maken van een bankfaciliteit en boekingsprofiel dat vereist is om borgstellingen te verwerken.
author: kweekley
ms.date: 11/15/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: BankParameters, DefaultDashboard, BankDocumentSetup, BankDocumentPosting
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7fe5b2ba43c4fcb4855c742bdb6f8209ebd92d68
ms.sourcegitcommit: cf6b764824bd1cf2c0dde6d37ddd0a7abab87ff0
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/16/2022
ms.locfileid: "9779457"
---
# <a name="set-up-bank-facilities-and-posting-profiles-for-letter-of-credit"></a>Bankfaciliteiten en boekingsprofielen voor kredietbrief instellen

[!include [banner](../../includes/banner.md)]

Deze procedure doorloopt het maken van een bankfaciliteit en boekingsprofiel dat vereist is om borgstellingen te verwerken. 

Deze taken gebruiken het demobedrijf 'USMF'.


## <a name="general-ledger-parameter"></a>Grootboekparameter
1. Ga naar **Contanten en bankbeheer > Instellingen > Parameters voor kas- en bankbeheer**.
2. Vouw de sectie **Bankdocument** uit.
3. Schakel de optie **Importkredietbrief inschakelen** in.
4. Schakel de optie **Exportkredietbrief inschakelen** in.
5. Klik op **Opslaan**.
6. Sluit de pagina.

## <a name="create-bank-facility"></a>Bankfaciliteit maken
1. Ga naar **Kas- en bankbeheer > Instellingen > Bankfaciliteiten**.
2. Klik op **Nieuw**.
3. Voer in het veld **Faciliteitsgroep** de groepsnaam van de bankfaciliteiten in.
4. Voer in het veld **Beschrijving** de beschrijving in van de bankfaciliteitsgroep.
5. Klik op **Opslaan**.
6. Klik op het tabblad **Faciliteitstypen**.
7. Klik op **Nieuw**.
8. Voer in het veld **Faciliteittype** een unieke code in.
9. Typ een waarde in het veld **Beschrijving**.
10. Klik in het veld **Faciliteitsgroep** op de vervolgkeuzeknop om de zoekopdracht te openen.
11. Zoek en selecteer het gewenste record in de lijst.
12. Klik in de lijst op de koppeling in de geselecteerde rij.
13. Selecteer in het veld **Faciliteitsaard** de aard van de bankfaciliteit.
14. Klik op **Opslaan**.
15. Sluit de pagina.

## <a name="bank-posting-profile"></a>Boekingsprofiel van bank
1. Ga naar **Kas- en bankbeheer > Instellingen > Boekingsprofiel van bankdocumenten**.
2. Klik op **Nieuw**.
3. Klik in het veld **Rekening/groepsnummer** op de vervolgkeuzeknop om de zoekopdracht te openen.
4. Zoek en selecteer het gewenste record in de lijst.
5. Klik in de lijst op de koppeling in de geselecteerde rij.
6. Selecteer de hoofdrekening voor vereffening.
    * Deze rekening wordt gebruikt bij de berekening van de cashflowprognose.  
7. Selecteer in het veld **Rekening voor toeslagen** de rekening voor onkostentransacties.
8. Selecteer in het veld **Margerekening** de rekening voor margetransacties.
    * Deze rekening wordt gedebiteerd wanneer de openingsmarge wordt geboekt en gecrediteerd wanneer de betaling wordt geboekt.  
9. Klik op **Opslaan**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
