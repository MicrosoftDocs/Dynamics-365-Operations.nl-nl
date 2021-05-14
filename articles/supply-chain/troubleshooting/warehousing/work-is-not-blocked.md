---
title: Werk wordt niet geblokkeerd
description: Werk wordt niet geblokkeerd
author: perlynne
ms.date: 04/15/2021
ms.topic: troubleshooting
ms.search.form: WHSWorkTable_WHSWorkUnblocking
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-05-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: d64ab282972e46e8857581b59e5705dd15667328
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924199"
---
# <a name="work-isnt-blocked"></a>Werk wordt niet geblokkeerd

Foutcode: WHSUnblockNotBlockedWorkErrorMessage

## <a name="symptoms"></a>Symptomen

Het systeem toont het volgende foutbericht:

> Werk met id %1 wordt niet geblokkeerd.

## <a name="cause"></a>Oorzaak

De optie **Geblokkeerde wave** op de wave is ingesteld op *Nee*. Het werk kan niet worden vrijgegeven omdat het momenteel niet is geblokkeerd.

## <a name="resolution"></a>Oplossing

 Alleen werk waarbij de optie **Geblokkeerde wave** op *Ja* is ingesteld, kan worden vrijgegeven.
