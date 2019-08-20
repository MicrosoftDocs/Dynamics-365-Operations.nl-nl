---
title: De overboekingsdocumenten instellen voor goederenverplaatsing in een bedrijf
description: Deze procedure laat zien hoe u overboekingsdocumenten voor goederenverplaatsing binnen een bedrijf maakt.
author: v-oloski
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventTransferOrders, InventLocationIdLookup, TransportationDocument, HcmWorkerLookUp, SrsReportViewerForm, InventTransferParmShip
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: v-oloski
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: fe4dd04595c961e1c66178e6ac6955e945869ded
ms.sourcegitcommit: 16bfa0fd08feec1647829630401ce62ce2ffa1a4
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/02/2019
ms.locfileid: "1852541"
---
# <a name="set-up-the-transfer-documents-for-goods-movement-inside-a-company"></a>De overboekingsdocumenten instellen voor goederenverplaatsing in een bedrijf

[!include [task guide banner](../../includes/task-guide-banner.md)]

Deze procedure laat zien hoe u overboekingsdocumenten voor goederenverplaatsing binnen een bedrijf maakt. Deze procedure is alleen beschikbaar voor rechtspersonen met een primair adres in Litouwen. De procedure is gemaakt met het demobedrijf DEMF met een primair adres in Litouwen. Voordat u deze procedure kunt uitvoeren, moet u de procedure "Overboekingsdocumenten instellen voor goederenverplaatsing binnen een bedrijf" voltooien. Deze procedure is alleen bedoeld voor voorraadboekhouders. Deze procedure is voor een functie die is toegevoegd in Dynamics 365 for Operations, versie 1611.


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

