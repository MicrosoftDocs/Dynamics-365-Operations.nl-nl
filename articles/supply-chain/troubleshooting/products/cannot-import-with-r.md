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
ms.openlocfilehash: efd773313f89784d8fca6b37d867e204cb2d06ab29694a19cbec7eed107a8019
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/05/2021
ms.locfileid: "6764687"
---
# <a name="you-cant-import-an-item-by-using-the-released-products-v2-entity"></a>U kunt een artikel niet importeren via de entiteit Vrijgegeven producten V2

KB-nummer: 4611825

## <a name="symptoms"></a>Symptomen

Wanneer u een artikel probeert te importeren met de entiteit *Vrijgegeven producten V2*, ontvangt u een foutbericht dat op het volgende voorbeeld lijkt:

> Kan geen record maken in Artikelen - traceringsdimensiegroepen (EcoResTrackingDimensionGroupItem). Artikelnummer: 2040663, Batch. Het record bestaat al.

## <a name="resolution"></a>Oplossing

Als u nieuwe vrijgegeven producten wilt importeren, moet u de entiteit *Vrijgegeven product maken V2* gebruiken in plaats van de entiteit *Vrijgegeven producten V2*.
