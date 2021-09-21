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
ms.openlocfilehash: bf6eb0eb755de3f2842c235946bfd7ccad04ccf7
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/07/2021
ms.locfileid: "7474719"
---
# <a name="you-cant-import-an-item-by-using-the-released-products-v2-entity"></a>U kunt een artikel niet importeren via de entiteit Vrijgegeven producten V2

KB-nummer: 4611825

## <a name="symptoms"></a>Symptomen

Wanneer u een artikel probeert te importeren met de entiteit *Vrijgegeven producten V2*, ontvangt u een foutbericht dat op het volgende voorbeeld lijkt:

> Kan geen record maken in Artikelen - traceringsdimensiegroepen (EcoResTrackingDimensionGroupItem). Artikelnummer: 2040663, Batch. Het record bestaat al.

## <a name="resolution"></a>Oplossing

Als u nieuwe vrijgegeven producten wilt importeren, moet u de entiteit *Vrijgegeven product maken V2* gebruiken in plaats van de entiteit *Vrijgegeven producten V2*.
