---
title: Een productieorder beëindigen
description: Deze procedure laat zien hoe u een productieorder beëindigt.
author: johanhoffmann
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
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8f5cb4afdc0285a6ccf28dbd362df3799c0ecc74
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/29/2019
ms.locfileid: "357353"
---
# <a name="end-a-production-order"></a>Een productieorder beëindigen

[!include [task guide banner](../../includes/task-guide-banner.md)]

Deze procedure laat zien hoe u een productieorder beëindigt. Het bedrijf van de demogegevens dat wordt gebruikt om deze procedure te maken is USMF. Dit is de laatste procedure van zeven waarin de levenscyclus van de productieorder wordt uitgelegd.


## <a name="end-a-production-order"></a>Een productieorder beëindigen
1. Ga naar Productiebeheer > Productieorders > Alle productieorders.
    * Selecteer een productieorder die de status Gereedgemeld heeft.  
2. Klik in het actievenster op Productieorder.
3. Klik op Beëindigen.
    * Op deze pagina kunt u bevestigen dat u de productieorder wilt beëindigen.  
4. Klik op het tabblad Algemeen.
5. Voer een datum in het veld Datum in.
6. Selecteer 'Toewijzing' in het veld Uitvalmethode.
    * Wanneer u de methode Toewijzing selecteert, worden kosten van de uitgevallen materialen opgeteld bij de eindproducten.  
7. Klik op OK.

## <a name="validate-calculation-results"></a>Berekeningsresultaten valideren
1. Klik in het actievenster op Kosten beheren.
2. Klik op Kostenvergelijking weergeven.
    * Nadat u de productieorder hebt beëindigd, kunt u de geschatte kostprijs vergelijken met de gerealiseerde kostprijs om een overzicht te krijgen van de productvarianties.  
