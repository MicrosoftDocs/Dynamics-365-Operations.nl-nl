--- 
title: Maateenheid beheren
description: "Deze procedure laat zien hoe u een maateenheid kunt definiëren, vertalingen voor de eenheid en de beschrijving ervan kunt verstrekken en conversieregels voor gerelateerde eenheden kunt definiëren."
author: sorenva
manager: AnnBe
ms.date: 02/12/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 6bb7a5133e9412f4ed6fb74f0d3ee595c07a0c4b
ms.contentlocale: nl-nl
ms.lasthandoff: 09/29/2017

---
# <a name="manage-unit-of-measure"></a>Maateenheid beheren

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

Deze procedure laat zien hoe u een maateenheid kunt definiëren, vertalingen voor de eenheid en de beschrijving ervan kunt verstrekken en conversieregels voor gerelateerde eenheden kunt definiëren. U kunt deze procedure doorlopen met demogegevens of uw eigen gegevens.

1. Ga naar Vrijgegeven productonderhoud.
2. Klik op Eenheden.

## <a name="create-a-unit-of-measure"></a>Een maateenheid maken
1. Klik op Nieuw.
2. Typ een waarde in het veld Eenheid.
    * Voer de id of het symbool in dat moet worden gebruikt om te verwijzen naar de maateenheid.  
3. Typ een waarde in het veld Omschrijving.
    * Voer een beschrijvende naam in voor de maateenheid in de systeemtaal.  
4. Selecteer een optie in het veld Eenheidsklasse.
    * De eenheidsklasse definieert van welke logische groepering, zoals oppervlakte, massa of hoeveelheid, de maateenheid deel uitmaakt.  
5. Voer een getal in het veld Decimale precisie in.
    * Geef het aantal decimalen op waarop de omgerekende maateenheid wordt afgerond bij voltooiing van een berekening met de maateenheid.  
6. Klik op Opslaan.

## <a name="define-unit-translations"></a>Eenheidsvertalingen definiëren
1. Klik op Eenheidsteksten.
2. Klik op Nieuw.
    * Gebruik eenheidstekst om een vertaling van de id of een symbool te maken waarmee de maateenheid wordt aangeduid voor gebruik op externe documenten in klant- of leverancierspecifieke talen.  
3. Typ of selecteer een waarde in het veld Waarde.
4. Typ een waarde in het veld Tekst.
5. Klik op Opslaan.
6. Sluit de pagina.
7. Klik op Omschrijvingen van vertaalde eenheden.
8. Klik op Nieuw.
    * Definieer taalspecifieke beschrijvingen voor de maateenheid.  
9. Typ of selecteer een waarde in het veld Waarde.
10. Typ een waarde in het veld Omschrijving.
11. Klik op Opslaan.
12. Sluit de pagina.

## <a name="define-unit-conversion-rules"></a>Regels voor eenheidsconversie definiëren
1. Klik op Eenheidsconversies.
    * Definieer regels om de maateenheid te converteren van en naar andere maateenheden in de geselecteerde eenheidsklasse.  
2. Klik op Nieuw om het verwijderdialoogvenster te openen.
3. Voer een getal in het veld Factor in.
    * Conversiefactor tussen Van eenheid en Naar eenheid. De omrekeningsfactor van centimeter naar meter is 100, aangezien er 100 centimeters in 1 meter gaan.  
4. Typ of selecteer een waarde in het veld Naar eenheid.
5. Selecteer een optie in het veld Afronding.
    * Definieer hoe de geconverteerde waarde moet worden afgerond.  
6. Klik op OK.
7. Sluit de pagina.


