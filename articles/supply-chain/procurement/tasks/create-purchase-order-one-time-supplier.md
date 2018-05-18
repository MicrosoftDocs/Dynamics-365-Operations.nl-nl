--- 
title: Een inkooporder maken voor een eenmalige leverancier
description: Deze procedure laat zien hoe u een inkooporder kunt maken voor een eenmalige leverancier.
author: FrankDahl
manager: AnnBe
ms.date: 08/23/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: fdahl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 2d4dabaf6e1d79cbd626294ee4e327f2725a5e43
ms.contentlocale: nl-nl
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-purchase-order-for-a-one-time-supplier"></a>Een inkooporder maken voor een eenmalige leverancier

[!include [task guide banner](../../includes/task-guide-banner.md)]

Deze procedure laat zien hoe u een inkooporder kunt maken voor een eenmalige leverancier. De leverancier wordt automatisch gemaakt met de inkooporder. De leveranciersrekening hoeft niet handmatig te worden gemaakt. Inkooporders worden meestal gemaakt door een inkoper. Het voorbeeld dat in deze handleiding wordt weergegeven, kan worden gebruikt in het USMF-demobedrijf. Het is een vereiste dat een rekening voor een eenmalige leverancier wordt ingesteld op de pagina Parameters van module Leveranciers.


## <a name="create-a-purchase-order-for-a-one-time-supplier"></a>Een inkooporder maken voor een eenmalige leverancier
1. Ga naar Inkoop en sourcing > Inkooporders > Alle inkooporders.
2. Klik op Nieuw.
3. Selecteer Ja in het veld Eenmalige leverancier.
    * Er wordt automatisch een leveranciersrekening gemaakt en aan de inkooporder toegewezen. De leveranciersrekening wordt gemaakt op basis van de sjabloon die is opgegeven op het tabblad Algemeen op de pagina Parameters van module Leveranciers.  
4. Typ in het veld Naam een naam voor de leverancier.
5. Klik op OK.
    * De inkooporder kan nu worden voltooid en verwerkt als elke andere order. Er zijn geen speciale kenmerken verbonden aan hoe dit gebeurt. Op de factuur wordt een transactie voor de leveranciersrekening aangegeven die met de order is gemaakt, waarna de betaling wordt verwerkt. Wanneer dit is voltooid, kan de leveranciersrekening worden verwijderd. Dit wordt meestal uitgevoerd door de leveranciersafdeling.  


