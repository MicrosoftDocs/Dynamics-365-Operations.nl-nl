---
title: Een inkooporder maken voor een eenmalige leverancier
description: Deze procedure laat zien hoe u een inkooporder kunt maken voor een eenmalige leverancier.
author: FrankDahl
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchCreateOrder
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: fdahl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a55cd8f21b99589a44f7509123d3417fd9dc07f6
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/18/2020
ms.locfileid: "3147429"
---
# <a name="create-a-purchase-order-for-a-one-time-supplier"></a>Een inkooporder maken voor een eenmalige leverancier

[!include [banner](../../includes/banner.md)]

Deze procedure laat zien hoe u een inkooporder kunt maken voor een eenmalige leverancier. De leverancier wordt automatisch gemaakt met de inkooporder. De leveranciersrekening hoeft niet handmatig te worden gemaakt. Inkooporders worden meestal gemaakt door een inkoper. Het voorbeeld dat in deze handleiding wordt weergegeven, kan worden gebruikt in het USMF-demobedrijf. Het is een vereiste dat een rekening voor een eenmalige leverancier wordt ingesteld op de pagina Parameters van module Leveranciers.


## <a name="create-a-purchase-order-for-a-one-time-supplier"></a>Een inkooporder maken voor een eenmalige leverancier
1. Ga naar Inkoop en sourcing > Inkooporders > Alle inkooporders.
2. Klik op Nieuw.
3. Selecteer Ja in het veld Eenmalige leverancier.
    * Er wordt automatisch een leveranciersrekening gemaakt en aan de inkooporder toegewezen. De leveranciersrekening wordt gemaakt op basis van de sjabloon die is opgegeven op het tabblad Algemeen op de pagina Parameters van module Leveranciers.  
4. Typ in het veld Naam een naam voor de leverancier.
5. Klik op OK.
    * De inkooporder kan nu worden voltooid en verwerkt als elke andere order. Er zijn geen speciale kenmerken verbonden aan hoe dit gebeurt. Op de factuur wordt een transactie voor de leveranciersrekening aangegeven die met de order is gemaakt, waarna de betaling wordt verwerkt.

