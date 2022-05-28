---
title: Een brandstofindex aan een vervoerder koppelen als bijkomende toeslag
description: Deze guide laat zien hoe u een bijkomende toewijzing, een bijkomende toeslag van vervoerder en een bijkomend model voor brandstoftoeslag kunt maken en een brandstofindex vervoerder kunt koppelen aan een vervoerder.
author: Weijiesa
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TMSRatingProfile
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: weijiesa
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d2df77fe94156e2b60b77fa1c995ea10eab048a0
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/03/2022
ms.locfileid: "8670547"
---
# <a name="associate-a-fuel-index-with-a-carrier-as-an-accessorial-charge"></a>Een brandstofindex aan een vervoerder koppelen als bijkomende toeslag

[!include [banner](../../includes/banner.md)]

Deze guide laat zien hoe u een bijkomende toewijzing, een bijkomende toeslag van vervoerder en een bijkomend model voor brandstoftoeslag kunt maken en een brandstofindex vervoerder kunt koppelen aan een vervoerder. U moet een brandstofindex van vervoerder instellen voordat u deze guide uitvoert. U kunt de guide 'Brandstofindex van een vervoerder instellen' gebruiken om dit te doen. Deze instellingstaken worden gewoonlijk uitgevoerd door een logistiek manager. Het bedrijf van de demogegevens dat wordt gebruikt om deze procedure te maken is USMF.


## <a name="create-an-accessorial-master"></a>Een model van extra's maken
1. Ga naar Transportbeheer > Instellingen > Beoordeling > Modellen van extra's.
2. Klik op Nieuw.
3. Typ een waarde in het veld Model van extra's.
4. Typ een waarde in het veld Naam.
5. Klik op Opslaan.

## <a name="create-a-carrier-accessorial-charge"></a>Een bijkomende toeslag van vervoerder maken
1. Ga naar Transportbeheer > Instellingen > Beoordeling > Bijkomende toeslagen van vervoerder.
2. Klik op Nieuw.
3. Typ een waarde in het veld Id extra's vervoerder.
4. Klik in het veld Vervoerder op de vervolgkeuzeknop om de zoekopdracht te openen.
5. Zoek en selecteer de gewenste record in de lijst.
    * In dit voorbeeld, kiest u vervoer per vrachtwagen.  
6. Klik in de lijst op de koppeling in de geselecteerde rij.
7. Klik in het veld Vervoerdersservice op de vervolgkeuzeknop om de zoekopdracht te openen.
8. Klik in de lijst op de koppeling in de geselecteerde rij.
9. Klik in het veld Model van extra's op de vervolgkeuzeknop om de zoekopdracht te openen.
10. Zoek en selecteer de gewenste record in de lijst.
    * In dit voorbeeld, kiest u het nieuw gemaakte Model van extra's.  
11. Klik op Opslaan.

## <a name="create-an-accessorial-assignment"></a>Een toewijzing van extra's maken
1. Klik op Bijkomende toewijzingen.
2. Klik op Nieuw.
3. Typ een waarde in het veld Naam.
4. Schakel de uitbreiding van de sectie Criteria om.
    * In de criteria kunt u altijd de brandstoftoeslag toepassen of bijvoorbeeld ervoor kiezen dat deze alleen binnen een bepaalde regio van toepassing is.  
5. Typ een waarde in het veld Postcode vanaf.
6. Typ een waarde in het veld Postcode tot.
7. Schakel de uitbreiding van de sectie Berekening om.
    * In de berekeningssectie kunt u opgeven hoe de brandstoftoeslag wordt berekend. Deze berekening hangt van de eenheid voor extra's die u als basis voor de berekening hebt gekozen.  
8. Selecteer in het veld Type van kosten van extra's de optie "Brandstoftoeslag".
9. Selecteer "Kilometerstand" in het veld Eenheid voor extra's.
10. Klik in het veld Regio op de vervolgkeuzeknop om de zoekopdracht te openen.
11. Klik in de lijst op de koppeling in de geselecteerde rij.
12. Klik op Opslaan.

## <a name="update-the-carrier-rating-profile"></a>Het beoordelingsprofiel vervoerder bijwerken
1. Ga naar Transportbeheer > Instellingen > Vervoerders > Vervoerders.
2. Zoek en selecteer de gewenste record in de lijst.
3. Schakel de uitbreiding van de sectie Beoordelingsprofielen om.
4. Klik op Bewerken.
5. Klik in het veld Brandstofindex vervoerder op de vervolgkeuzeknop om de zoekopdracht te openen.
6. Klik in de lijst op de koppeling in de geselecteerde rij.
7. Klik op Opslaan.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]