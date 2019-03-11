---
title: Bijkomende toeslagen van hub en modellen voor extra's instellen
description: Deze procedure laat zien hoe u een model van extra's voor een hub kunt maken en dat model kunt gebruiken om een bijkomende toeslag van hub te maken.
author: ShylaThompson
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9959c20f9a8fd07cbf0cfd76f7760b44d7b5cae1
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/29/2019
ms.locfileid: "331892"
---
# <a name="set-up-hub-accessorial-charges-and-accessorial-masters"></a>Bijkomende toeslagen van hub en modellen voor extra's instellen

[!include [task guide banner](../../includes/task-guide-banner.md)]

Deze procedure laat zien hoe u een model van extra's voor een hub kunt maken en dat model kunt gebruiken om een bijkomende toeslag van hub te maken. De procedure gebruikt de USMF-dataset. Deze instellingen worden gewoonlijk uitgevoerd door een transportcoördinator.


## <a name="set-up-a-hub-master"></a>Een model voor een hub instellen
1. Ga naar Transportbeheer > Instellingen > Beoordeling > Modellen van extra's.
2. Klik op Nieuw.
3. Typ een waarde in het veld Model van extra's.
4. Typ een waarde in het veld Naam.
5. Selecteer "Hub" in het veld Type van extra's.
6. Klik op Opslaan.
7. Sluit de pagina.

## <a name="set-up-a-hub-accessorial-charge"></a>Een extra toeslag van hub instellen
1. Ga naar Transportbeheer > Instellingen > Beoordeling > Toeslag extra's hub.
2. Klik op Nieuw.
3. Typ een waarde in het veld Id extra's hub.
4. Klik in het veld Hub op de vervolgkeuzeknop om de zoekopdracht te openen.
5. Zoek en selecteer de gewenste record in de lijst.
6. Selecteer een optie in het veld Hubpositie.
    * U kunt de toeslag maken voor ophalen of afleveren. Afhankelijk van uw selectie wordt de toeslag toegepast op het bijbehorende transportsegment op uw route.  
7. Klik in het veld Model van extra's op de vervolgkeuzeknop om de zoekopdracht te openen.
8. Klik in de lijst op de koppeling in de geselecteerde rij.
    * Selecteer het model dat u zojuist hebt gemaakt.  
9. Klik op Opslaan.
10. Sluit de pagina.

