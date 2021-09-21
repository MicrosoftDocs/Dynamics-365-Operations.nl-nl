---
title: Kan gedeeltelijk verzonden lading niet opnieuw vrijgeven aan magazijn
description: In eerdere versies kon u een gedeeltelijk verzonden belasting niet opnieuw vrijgeven door bepaalde functies te gebruiken met onvolledige reserveringen. Dit is opgelost.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 0380e1963a38f2be55b31e06b3845f935661eed2
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476029"
---
# <a name="cant-re-release-a-partially-shipped-load-to-the-warehouse"></a>Een gedeeltelijk verzonden lading kan niet worden vrijgegeven aan het magazijn

## <a name="symptoms"></a>Symptomen

U kunt een gedeeltelijk verzonden lading niet vrijgeven aan het magazijn. Wanneer u de vrijgave aan het magazijn uitvoert, wordt er een bericht weergegeven dat de bewerking is voltooid, maar gebeurt er niets en wordt er geen werk gemaakt voor de resterende hoeveelheid. Dit probleem treedt op wanneer u de transportladingsfunctie gebruikt en er een onvolledige reservering is.

## <a name="resolution"></a>Oplossing

[KB-probleem 470069](https://fix.lcs.dynamics.com/Issue/Details?kb=4574490&bugId=470069&dbType=3&qc=84ce1e09d7032d8b8ef86f5a0c68b86badf3dfaf29686c5ebbe97c53c0957b5f) ("Gedeeltelijk verzonden ladingen kunnen opnieuw in een wave worden geplaatst en verwerkt") is in [release 10.0.15 gecorrigeerd](/dynamics365/supply-chain/get-started/whats-new-scm-10-0-15).
