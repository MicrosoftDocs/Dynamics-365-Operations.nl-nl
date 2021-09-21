---
title: Kan nummerplaat niet verplaatsen als lege uitgifte en lege ontvangst zijn toegestaan
description: U kunt een nummerplaat niet verplaatsen als voor het serienummer lege uitgifte en lege ontvangst zijn toegestaan. Dit zal worden gecorrigeerd door het veld Serienummer optioneel te maken.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 0047f79aa417c8fc910447505f07963d014f54e7
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476004"
---
# <a name="cant-move-license-plate-if-serial-number-has-blank-issue-and-blank-receipt-allowed"></a>Kan nummerplaat niet verplaatsen als voor het serienummer lege uitgifte en lege ontvangst zijn toegestaan

## <a name="symptoms"></a>Symptomen

U kunt een nummerplaat niet verplaatsen via een menuopdracht **Verplaatsing** als voor het serienummer de instellingen *Lege uitgifte is toegestaan* en *Lege ontvangst toegestaan* gelden in de traceringsdimensiegroep en als er meerdere nummerplaten op dezelfde locatie zijn, waarvan sommige serienummers hebben en andere niet.

## <a name="resolution"></a>Oplossing

Dit probleem wordt verholpen door wijzigingen die in [KB 4571546](https://fix.lcs.dynamics.com/Issue/Details?kb=4571546&bugId=467880&dbType=3&qc=5b46d7faa9cc326cebfe9854cb30be8ea30b21ef33d3572c325fbb21202de687) zijn geïmplementeerd. Deze wijzigingen maken het veld **Serienummer** optioneel als lege ontvangst en lege uitgifte zijn toegestaan.
