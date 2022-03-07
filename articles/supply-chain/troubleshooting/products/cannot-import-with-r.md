---
title: U kunt een artikel niet importeren via de entiteit Vrijgegeven producten V2
description: U kunt een artikel niet importeren via de entiteit Vrijgegeven producten V2.
author: t-benebo
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: EcoResProductDetailsExtended, DataManagementWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: myvakalo
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 8182f2f83f6a3e4cf54fe6fa64b25a2f461ff541
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026397"
---
# <a name="you-cant-import-an-item-by-using-the-released-products-v2-entity"></a>U kunt een artikel niet importeren via de entiteit Vrijgegeven producten V2

KB-nummer: 4611825

## <a name="symptoms"></a>Symptomen

Wanneer u een artikel probeert te importeren met de entiteit *Vrijgegeven producten V2*, ontvangt u een foutbericht dat op het volgende voorbeeld lijkt:

> Kan geen record maken in Artikelen - traceringsdimensiegroepen (EcoResTrackingDimensionGroupItem). Artikelnummer: 2040663, Batch. Het record bestaat al.

## <a name="resolution"></a>Oplossing

Als u nieuwe vrijgegeven producten wilt importeren, moet u de entiteit *Vrijgegeven product maken V2* gebruiken in plaats van de entiteit *Vrijgegeven producten V2*.
