---
title: Gecombineerde nummerplaat ontvangen werkt niet voor beschikkingscodes.
description: Wanneer het veld Actie voor een beschikkingscode is ingesteld op Credit of Uitval, kunt u de menuopdracht Gecombineerde nummerplaat ontvangen alleen gebruiken om geretourneerde artikelen te verwerken.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: b762255bc5ef6a1e15688a9c635940e92e67db3c
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476037"
---
# <a name="mixed-license-plate-receiving-doesnt-work-for-any-disposition-code-but-credit"></a>Gecombineerde nummerplaat ontvangen werkt niet voor beschikkingscodes behalve Credit.

## <a name="symptoms"></a>Symptomen

Wanneer het veld **Actie** voor een beschikkingscode is ingesteld op *Credit* of *Uitval*, kunt u de menuopdracht [Gecombineerde nummerplaat ontvangen](/dynamics365/supply-chain/warehousing/mixed-license-plate-receiving) alleen gebruiken om geretourneerde artikelen te verwerken.

## <a name="resolution"></a>Oplossing

Microsoft heeft dit probleem beoordeeld en heeft vastgesteld dat het een functiebeperking is. Op dit moment worden alleen [beschikkingscodes](/dynamics365/supply-chain/service-management/set-up-disposition-codes) waarvoor het veld **Actie** is ingesteld op *Credit* of *Uitval* ondersteund voor gecombineerde nummerplaat ontvangen.
