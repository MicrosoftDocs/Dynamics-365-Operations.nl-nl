--- 
title: Een overboekingsdocument genereren voor een interne voorraadoverboeking
description: Deze procedure laat zien hoe u overboekingsdocumenten voor goederenverplaatsing binnen een bedrijf maakt.
author: EvgenyPopovMBS
manager: AnnBe
ms.date: 10/27/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 0fe3d735d6309bf87047a27f9e68c579ca052012
ms.contentlocale: nl-nl
ms.lasthandoff: 07/27/2017

---
# <a name="generate-a-transfer-document-for-an-internal-inventory-transfer"></a>Een overboekingsdocument genereren voor een interne voorraadoverboeking

[!include[task guide banner](../../includes/task-guide-banner.md)]

Deze procedure laat zien hoe u overboekingsdocumenten voor goederenverplaatsing binnen een bedrijf maakt. Deze procedure is alleen beschikbaar voor rechtspersonen met een primair adres in Litouwen. De procedure is gemaakt met het demobedrijf DEMF met een primair adres in Litouwen. Voordat u deze procedure kunt uitvoeren, moet u de procedure "Overboekingsdocumenten instellen voor goederenverplaatsing binnen een bedrijf" voltooien. Deze procedure is alleen bedoeld voor voorraadboekhouders. Deze procedure is voor een functie die in versie 1611 van Dynamics 365 for Operations is toegevoegd.


## <a name="create-a-transfer-order"></a>Een transferorder maken
1. Ga naar Voorraadbeheer > Inkomende orders > Transferorder.
2. Klik op Nieuw.
3. Typ of selecteer een waarde in het veld Van magazijn.
4. Typ of selecteer een waarde in het veld Naar magazijn.
5. Klik op Toevoegen.
6. Markeer in de lijst de geselecteerde rij.
7. Typ of selecteer een waarde in het veld Artikelnummer.

## <a name="enter-transportation-details-for-the-transfer-order"></a>Transportgegevens invoeren voor de transferorder
1. Klik op Opslaan.
2. Klik in het actievenster op Verzenden.
3. Klik op Transportgegevens.
4. Selecteer Ja in de veld Transportgegevens afdrukken.
5. Typ of selecteer een waarde in het veld Afgegeven goederen.
6. Typ een waarde in het veld Verpakking.
7. Typ een waarde in het veld Risiconiveau van de lading.
8. Typ of selecteer een waarde in het veld Vervoerder.
9. Typ of selecteer een waarde in het veld Model.
10. Typ een waarde in het veld Registratienummer.
11. Typ een waarde in het veld Trailerregistratienummer.
12. Typ of selecteer een waarde in het veld Chauffeur.
13. Typ een waarde in het veld Naam chauffeur.
14. Klik op Opslaan.
15. Sluit de pagina.

## <a name="view-the-packing-slip-for-the-unposted-transfer-order"></a>Pakbon voor de niet-geboekte transferferorder weergeven
1. Klik op Pakbon.
2. Klik op OK.
3. Sluit de pagina.

## <a name="view-the-packing-slip-for-the-posted-transfer-order"></a>Pakbon voor de geboekte transferferorder weergeven
1. Klik in het actievenster op Transferorder.
2. Klik in het actievenster op Verzenden.
3. Klik op Verzenden transferorders.
4. Klik op het tabblad Algemeen.
5. Selecteer een optie in het veld Bijwerken.
6. Klik op het tabblad Overzicht.
7. Typ een waarde in het veld Pakbon.
8. Klik op OK.
9. Klik in het actievenster op Verzenden.
10. Klik op Pakbon.
11. Klik op OK.

