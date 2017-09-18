--- 
title: "Een vervaldatum voor een productiestroomversie definiëren"
description: Om de geldigheid en de verwerking van een productiestroomversie te voltooien op een bepaalde datum of een actieve versie door een nieuwe versie te vervangen, moet u een vervaldatum op de versieregel instellen.
author: cvocph
manager: AnnBe
ms.date: 10/07/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 9b947a02be981155053e33a4ef20e19bf2a194a5
ms.openlocfilehash: b968502de357779b7d26a5780f3febc3076dd9ad
ms.contentlocale: nl-nl
ms.lasthandoff: 07/27/2017

---
# <a name="define-an-expiry-date-for-a-production-flow-version"></a>Een vervaldatum voor een productiestroomversie definiëren

[!include[task guide banner](../../includes/task-guide-banner.md)]

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

