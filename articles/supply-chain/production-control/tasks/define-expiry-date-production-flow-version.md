---
title: Een vervaldatum voor een productiestroomversie definiëren
description: Om de geldigheid en de verwerking van een productiestroomversie te voltooien op een bepaalde datum of een actieve versie door een nieuwe versie te vervangen, moet u een vervaldatum op de versieregel instellen.
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
ms.openlocfilehash: 9f6ee9177664767c31eaa3e9b65d7559a1a9662f
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/29/2021
ms.locfileid: "7574420"
---
# <a name="define-an-expiry-date-for-a-production-flow-version"></a>Een vervaldatum voor een productiestroomversie definiëren

[!include [banner](../../includes/banner.md)]

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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]