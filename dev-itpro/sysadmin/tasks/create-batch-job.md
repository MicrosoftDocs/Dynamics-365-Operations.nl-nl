--- 
title: Een batchtaak maken
description: Een batchtaak is een groep taken die voor automatische verwerking naar een AOS-exemplaar (Application Object Server) worden verzonden.
author: maertenm
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: ca2b755406fb7fce4b11457be86f6a8685004438
ms.contentlocale: nl-nl
ms.lasthandoff: 07/27/2017

---
# <a name="create-a-batch-job"></a>Een batchtaak maken

[!include[task guide banner](../../includes/task-guide-banner.md)]

Een batchtaak is een groep taken die voor automatische verwerking naar een AOS-exemplaar (Application Object Server) worden verzonden. Batchtaken worden uitgevoerd met behulp van de beveiligingsgegevens van de gebruiker die de taak heeft gemaakt. Voer de volgende procedure uit om een batchtaak te maken. Het bedrijf van de demogegevens dat wordt gebruikt om deze procedure te maken is USMF.


## <a name="create-the-batch-job"></a>De batchtaak maken
1. Ga naar Systeembeheer > Query's > Batchtaken.
2. Klik op Nieuw.
3. Typ een waarde in het veld Taakomschrijving.
4. Typ een datum en een tijd in het veld Geplande begindatum/tijd.
5. Klik op Opslaan.

## <a name="create-a-recurrence"></a>Een terugkeerpatroon maken
1. Klik in het actievenster op Batchtaak.
2. Klik op Terugkeerpatroon.
    * Gebruik deze opties om een bereik en terugkeerpatroon in te voeren.  
3. Klik op OK.

## <a name="add-alerts"></a>Waarschuwingen toevoegen
1. Klik in het actievenster op Batchtaak.
2. Klik op Waarschuwingen.
    * Geef aan of u waarschuwingsberichten wilt laten verzenden wanneer de batchtaak is voltooid, wanneer er een fout optreedt of wanneer de batchtaak wordt geannuleerd. Geef vervolgens op of u waarschuwingen wilt laten weergeven als pop-upberichten.   
3. Klik op OK.


