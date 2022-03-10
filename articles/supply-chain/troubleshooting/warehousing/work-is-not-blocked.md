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
ms.openlocfilehash: 6b4361682246397732e8326b98b1b86ff878664e54c8c352296b0d7eaff6bbbd
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/05/2021
ms.locfileid: "6719546"
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
