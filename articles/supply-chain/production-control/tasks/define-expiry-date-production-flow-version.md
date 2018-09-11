--- 
title: "Een vervaldatum voor een productiestroomversie definiëren"
description: Om de geldigheid en de verwerking van een productiestroomversie te voltooien op een bepaalde datum of een actieve versie door een nieuwe versie te vervangen, moet u een vervaldatum op de versieregel instellen.
author: cvocph
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LeanProductionFlow
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 6fabeb31720a60bf97d08dabf8ed87ac6af7cbf7
ms.contentlocale: nl-nl
ms.lasthandoff: 09/29/2017

---
# <a name="define-an-expiry-date-for-a-production-flow-version"></a>Een vervaldatum voor een productiestroomversie definiëren

[!include [task guide banner](../../includes/task-guide-banner.md)]

Om de geldigheid en de verwerking van een productiestroomversie te voltooien op een bepaalde datum of een actieve versie door een nieuwe versie te vervangen, moet u een vervaldatum op de versieregel instellen. Het is niet nodig om de versie te deactiveren.


## <a name="set-an-expiration-date-to-end-a-production-flow-version"></a>Stel een vervaldatum in om een productiestroomversie te beëindigen
1. Ga naar Productiebeheer > Instellingen > Lean productiestroom > Productiestromen.
2. Zoek en selecteer de gewenste record in de lijst.
    * Selecteer een productiestroom met een versie die al is gedefinieerd.  
3. Klik in de lijst op de koppeling in de geselecteerde rij.
4. Klik op Bewerken.
5. Markeer in de lijst de geselecteerde rij.
6. Voer in het veld Vervaldatum een datum en tijd in.
    * Een nieuwe versie wordt niet gestart of geactiveerd voor de vervaldatum. Het is ook niet meer mogelijk om taken voor deze productiestroom te maken of te starten. U kunt gestarte taken na de vervaldatum nog uitvoeren.  


