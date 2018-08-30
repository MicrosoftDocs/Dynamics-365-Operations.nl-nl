--- 
title: Batchtaken maken
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
ms.sourcegitcommit: e782d33f3748524491dace28008cd9148ae70529
ms.openlocfilehash: b32c16a0c0045e22128746f81c6e9fd03370ac1f
ms.contentlocale: nl-nl
ms.lasthandoff: 08/08/2018

---
# <a name="create-batch-jobs"></a>Batchtaken maken

[!include [task guide banner](../../includes/task-guide-banner.md)]

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


