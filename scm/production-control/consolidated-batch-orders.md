---
title: Geconsolideerde batchorders
description: In dit artikel wordt het concept van geconsolideerde batchorders beschreven.
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: PmfAddToConsOrder, PmfBulkItemConv, PmfBulkPackOnHand, PmfConsOrderListPage
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 19291
ms.assetid: e97f1d3d-1306-4c42-b2bc-d1755fe574d5
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: fed4856d3b4533287097122f89c4daab580cbfd3
ms.contentlocale: nl-nl
ms.lasthandoff: 04/25/2017


---

# <a name="consolidated-batch-orders"></a>Geconsolideerde batchorders

[!include[banner](../includes/banner.md)]


In dit artikel wordt het concept van geconsolideerde batchorders beschreven.

Een bulkartikel dat is geproduceerd wordt beschouwd als een bovenliggend artikel, terwijl een verpakt artikel wordt beschouwd als een onderliggend artikel. De relatie tussen het bulkartikel en het verpakte artikel wordt uitgedrukt in een bulkartikelconversie. Deze bulkartikelconversie is gedefinieerd op het bulkartikel zelf.  

Verpakte artikelen kunnen verpakt zijn in containers van één of meerdere maten die als één eenheid worden beschouwd. Door de orders voor een bulkartikel te consolideren, kunt u alle gerelateerde batchorders in één weergave bekijken zodat u kunt bepalen of er nog werk moet worden voltooid.  

Een geconsolideerde batchorder kan elke combinatie van de volgende orders bevatten:

-   Één bulkorder en meerdere verpakte orders
-   Meerdere bulkorders en meerdere verpakte orders
-   Meerdere bulkorder en één verpakte order
-   Alleen verpakte orders





