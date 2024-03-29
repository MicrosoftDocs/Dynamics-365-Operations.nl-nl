---
title: Een productiestroomversie deactiveren
description: Als een actieve productiestroomversie niet meer nodig is, kan deze worden gedeactiveerd.
author: johanhoffmann
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LeanProductionFlow
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1691dc644e2e191a9e74980784d6dcf741dcd598
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/29/2021
ms.locfileid: "7576755"
---
# <a name="deactivate-a-production-flow-version"></a>Een productiestroomversie deactiveren

[!include [banner](../../includes/banner.md)]

Als een actieve productiestroomversie niet meer nodig is, kan deze worden gedeactiveerd. U kunt deze optie alleen gebruiken als alle kanbanregels en activiteiten zijn beëindigd en niet opnieuw worden geactiveerd. Merk op dat de vervaldatum van alle kanbanregels voor deze productiestroomversie wordt bijgewerkt met de huidige datum en tijd. 

Als u een actieve productiestroomversie wilt wijzigen, kunt u een vervaldatum instellen voor de actieve versie en een nieuwe versie maken. Hierdoor kunt u uw productiebewerkingen voortzetten tijdens het voorbereiden van de nieuwe versie en gerelateerde kanbanregels. 

Als u een actieve productiestroomversie wilt laten vervallen, stelt u een vervaldatum in. In dit opzicht is deactivering meer een uitzondering dan een regel. 

Voor deze procedure hebt u een productiestroom nodig met een versie die kan worden gedeactiveerd. Probeer dit niet in een productieomgeving als u niet 100% zeker weet of de versie volledig verouderd is.


## <a name="deactivate-a-production-flow-version"></a>Een productiestroomversie deactiveren
1. Ga naar Productiebeheer > Instellingen > Lean productiestroom > Productiestromen.
2. Zoek en selecteer de gewenste record in de lijst.
3. Klik in de lijst op de koppeling in de geselecteerde rij.
4. Zoek en selecteer de gewenste record in de lijst.
5. Klik op Deactiveren.
    * Ga niet verder als u niet 100% zeker weet of deze productiestroomversie verouderd is. Als u op OK klikt, verlopen alle actieve kanbanregels en wordt een direct einde gemaakt aan alle productie- en aanvulactiviteiten van deze productiestroomversie.  
6. Klik op OK.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]