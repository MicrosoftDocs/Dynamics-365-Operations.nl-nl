---
title: Een productieorder beëindigen
description: Deze procedure laat zien hoe u een productieorder beëindigt.
author: johanhoffmann
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bb87a8df77ecced213b4bd61c40fa372b092ab765528e1cd96274cf79537d521
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/05/2021
ms.locfileid: "6765949"
---
# <a name="end-a-production-order"></a>Een productieorder beëindigen

[!include [banner](../../includes/banner.md)]

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


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]