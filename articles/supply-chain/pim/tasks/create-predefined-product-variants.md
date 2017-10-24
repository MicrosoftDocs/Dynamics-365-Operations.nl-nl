--- 
title: Vooraf gedefinieerde productvarianten maken
description: Deze procedure begeleidt u bij het maken van productvarianten voor een productmodel met behulp van de combinaties van productdimensies.
author: YuyuScheller
manager: AnnBe
ms.date: 10/27/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Operations
ms.search.region: Global
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: c49d25004b19084276404cf887188e89200afa32
ms.contentlocale: nl-nl
ms.lasthandoff: 09/29/2017

---
# <a name="create-predefined-product-variants"></a>Vooraf gedefinieerde productvarianten maken

[!include[task guide banner](../../includes/task-guide-banner.md)]

Deze procedure begeleidt u bij het maken van productvarianten voor een productmodel met behulp van de combinaties van productdimensies. Het demobedrijf dat wordt gebruikt om deze procedure te maken is USMF.


## <a name="create-a-product-master"></a>Een productmodel maken
1. Ga naar Productgegevensbeheer > Producten > Productmodellen.
2. Klik op Nieuw.
3. Typ een waarde in het veld Productnummer.
    * Handmatig invoeren van een productnummer is alleen verplicht als er geen nummerreeks is ingesteld voor het productnummerveld. Met andere woorden: sla de stap over als een nummerreeks voor het veld is ingesteld.  
4. Typ een waarde in het veld Productnaam.
5. Typ of selecteer een waarde in het veld Productdimensiegroep.
    * Selecteer de productdimensiegroep SizeCol (Grootte en Kleur).  
6. Klik op OK.

## <a name="add-product-dimensions"></a>Productdimensies toevoegen
1. Klik op Productdimensies.
    * Dit voorbeeld toont hoe productdimensies handmatig worden ingevoerd. U kunt er ook voor kiezen een grootte, kleur of een stijlgroep te selecteren die de productdimensiewaarden bevat die u wilt gebruiken.  
2. Klik op Nieuw.
3. Markeer in de lijst de geselecteerde rij.
4. Typ of selecteer een waarde in het veld Grootte.
5. Typ een waarde in het veld Naam.
6. Klik op Nieuw.
7. Markeer in de lijst de geselecteerde rij.
8. Typ of selecteer een waarde in het veld Grootte.
9. Typ een waarde in het veld Naam.
10. Klik op het tabblad Kleuren.
11. Klik op Nieuw.
12. Markeer in de lijst de geselecteerde rij.
13. Typ of selecteer een waarde in het veld Kleur.
14. Typ een waarde in het veld Naam.
15. Klik op Nieuw.
16. Markeer in de lijst de geselecteerde rij.
17. Typ of selecteer een waarde in het veld Kleur.
18. Typ een waarde in het veld Naam.
19. Klik op Opslaan.
20. Sluit de pagina.

## <a name="generate-product-variants"></a>Productvarianten genereren
1. Klik op Productvarianten.
2. Klik op Variantsuggesties.
3. Klik op Alles selecteren.
    * In dit voorbeeld worden alle mogelijke varianten geselecteerd. Als alleen een subset van de mogelijke productdimensiecombinaties wordt gebruikt om varianten te maken, kunt u de afzonderlijke items selecteren.  
4. Klik op Maken.
    * U kunt omschrijvingen voor al uw varianten genereren op basis van de combinatie van productdimensiewaarden. De omschrijvingen zijn optioneel.  
5. Klik op Opslaan.


