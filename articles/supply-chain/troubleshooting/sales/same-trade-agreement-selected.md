---
title: Dezelfde handelsovereenkomst die is geselecteerd bij het maken van verkooporderregels
description: Als er meer dan één handelsovereenkomst is gedefinieerd voor een bepaalde datum, wordt altijd degene met de laagste prijs geselecteerd bij het aanmaken van verkooporderregels.
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
ms.search.form: SalesTable, SalesTableListPage, SalesTableListPage_SalesCancelOrder
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: a586a399fb349965b972191bec1271651bec5fcb
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476017"
---
# <a name="if-two-trade-agreements-exist-for-overlapping-dates-the-same-one-is-always-selected"></a>Als er twee handelsovereenkomsten bestaan voor overlappende datums, wordt altijd dezelfde overeenkomst geselecteerd

## <a name="symptoms"></a>Symptomen

Als twee handelsovereenkomsten zijn gedefinieerd voor dezelfde periode of overlappende perioden, lijkt telkens dezelfde handelsovereenkomst te worden geselecteerd wanneer u verkooporderregels maakt die die artikelen bevatten.

## <a name="resolution"></a>Oplossing

Als er meer dan één handelsovereenkomst voor een bepaalde datum is, wordt altijd de handelsovereenkomst met de laagste prijs geselecteerd. Download het volgende technische document voor meer informatie: [Handelsovereenkomsten in Microsoft Dynamics AX 2012](https://www.axug.com/HigherLogic/System/DownloadDocumentFile.ashx?DocumentFileKey=3396a3a8-1f48-4d85-8cd6-5fa982f62e90).
