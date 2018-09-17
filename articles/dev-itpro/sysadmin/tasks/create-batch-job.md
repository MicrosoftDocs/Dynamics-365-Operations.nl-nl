--- 
title: Een batchtaak maken
description: Een batchtaak is een groep taken die voor automatische verwerking naar een AOS-exemplaar (Application Object Server) worden verzonden.
author: maertenm
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BatchJob, SysRecurrence, BatchAlerts
audience: Application User
ms.reviewer: margoc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 31c8e2ba87ef8c17a3147e1159104585258d4164
ms.contentlocale: nl-nl
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-batch-job"></a>Een batchtaak maken

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


