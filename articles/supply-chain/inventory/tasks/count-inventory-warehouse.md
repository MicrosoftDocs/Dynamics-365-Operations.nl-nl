---
title: Voorraad in een magazijn tellen
description: Deze procedure begeleidt u door het proces voor het maken en boeken van een voorraadtellingsjournaal om een artikel op een specifieke locatie in het magazijn te tellen.
author: MarkusFogelberg
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: fa72cb0d651f5e60797fa41f6e2b2cf1891730b5
ms.contentlocale: nl-nl
ms.lasthandoff: 09/29/2017

---
# <a name="count-inventory-in-a-warehouse"></a>Voorraad in een magazijn tellen

[!include [task guide banner](../../includes/task-guide-banner.md)]

Deze procedure begeleidt u door het proces voor het maken en boeken van een voorraadtellingsjournaal om een artikel op een specifieke locatie in het magazijn te tellen. De procedure is van toepassing op de functie 'basale magazijnen' die beschikbaar is in de module Voorraadbeheer, niet op de magazijnfunctionaliteit die beschikbaar is in de module magazijnbeheer. U kunt deze procedure met het demobedrijf USMF uitvoeren of uw eigen gegevens gebruiken. Als u uw eigen gegevens gebruikt, moet u ervoor zorgen dat u producten en locaties hebt ingesteld en dat u een voorraadjournaalnaam voor tellingsjournalen hebt gemaakt. Voorraadtelling wordt normaal uitgevoerd door een magazijnwerknemer.


## <a name="create-an-inventory-counting-journal"></a>Een voorraadtellingsjournaal maken
1. Ga naar Voorraadbeheer > Journaalboekingen > Artikeltelling > Tellen.
2. Klik op Nieuw.
3. Klik in het veld Naam op de vervolgkeuzeknop om de zoekopdracht te openen.
4. Klik in de lijst op de naam van het voorraadtellingsjournaal dat u wilt gebruiken
    * Enkele andere velden worden ingevuld op basis van de instellingen van de naam voor het standaardjournaal voor voorraadtelling die u selecteert.  
5. Klik in het veld Medewerker op de vervolgkeuzeknop om de zoekopdracht te openen.
6. Selecteer in de lijst de medewerker die u wilt gebruiken.
7. Klik op Selecteren.
8. Klik op OK.

## <a name="create-journal-lines"></a>Journaalregels maken
1. Klik op Nieuw.
2. Klik in het veld Artikelnummer op de vervolgkeuzeknop om de zoekopdracht te openen.
3. Zoek en selecteer de gewenste record in de lijst.
    * Als u het demobedrijf USMF gebruikt, selecteert u 'A0001'.  
4. Klik in het veld Locatie op de vervolgkeuzeknop om de zoekopdracht te openen.
5. Zoek en selecteer de gewenste record in de lijst.
    * Als u het demobedrijf USMF gebruikt, selecteert u site '2'.  
6. Klik in het veld Magazijn op de vervolgkeuzeknop om de zoekopdracht te openen.
7. Zoek en selecteer de gewenste record in de lijst.
    * Als u het demobedrijf USMF gebruikt, selecteert u magazijn '24'.  
8. Klik in het veld Locatie op de vervolgkeuzeknop om de zoekopdracht te openen.
9. Zoek en selecteer de gewenste record in de lijst.
    * Als u het demobedrijf USMF gebruikt, selecteert u locatie 'BULK-001'.  
10. Voer in het veld Geteld een getal in.
    * Als u een geteld aantal invoert dat verschilt van het nummer dat in het veld In Voorhanden wordt weergegeven, wordt het Veld Hoeveelheid bijgewerkt om het verschil aan te geven.  
11. Klik op Opslaan.

## <a name="post-the-inventory-counting-journal"></a>Het voorraadtellingsjournaal boeken
1. Klik op Boeken.
    * Wanneer u een voorraadtellingsjournaal boekt en als het getelde bedrag afwijkt van het bedrag dat in het veld Voorhanden wordt vermeld, wordt een voorraadontvangst of -uitgifte geboekt, worden het niveau en de waarde van de voorraad gewijzigd en worden grootboektransacties gegenereerd.  
2. Klik op OK.

## <a name="view-inventory-transactions"></a>Voorraadtransacties weergeven
1. Klik op Voorraad.
2. Klik op Transacties.
    * Hier kunt u de verwante transacties bekijken die worden gemaakt wanneer u uw voorraadtellingsjournaal boekt.   

