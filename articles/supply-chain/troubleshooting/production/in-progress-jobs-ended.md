---
title: Taken die worden uitgevoerd, worden beëindigd wanneer er een gedeeltelijke hoeveelheid voor de laatste taak wordt gerapporteerd
description: Wanneer ik het apparaat voor taakkaarten gebruik om een gedeeltelijke hoeveelheid te rapporteren voor de laatste taak in een productieorder, worden alle eerdere taken met de status In uitvoering beëindigd.
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 11511d4ac7524facdd0d647e9bc38fe09c282be1
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476054"
---
# <a name="previous-in-progress-jobs-are-ended-when-reporting-partial-quantity-on-last-job"></a>Eerdere taken die worden uitgevoerd, worden beëindigd wanneer er een gedeeltelijke hoeveelheid voor de laatste taak wordt gerapporteerd

## <a name="symptoms"></a>Symptomen

Wanneer ik het apparaat voor taakkaarten gebruik om een gedeeltelijke hoeveelheid te rapporteren voor de laatste taak in een productieorder, worden alle eerdere taken op die order met de status In uitvoering automatisch beëindigd.

## <a name="resolution"></a>Oplossing

Dit is zo ontworpen. Op de pagina **Standaardwaarden productieorder**, op het tabblad **Rapporteren als gereed** vind u een optie met de naam **Eindmarkering van route**. Als dit onderwerp is ingesteld op *Ja*, wordt een routekaartjournaal geboekt wanneer een werknemer taakkaartapparaat of taakkaartterminal gebruikt om de laatste bewerking te melden. In dit journaal worden alle bewerkingen gemarkeerd als voltooid en worden alle productietaken beëindigd. Wanneer de optie **Eindmarkering van route** is ingesteld op *Ja*, houdt het systeem geen rekening met de taakstatus die de medewerker heeft geselecteerd bij het melden van de laatste bewerking. Het systeem houdt er ook geen rekening mee of de werk nemer een volledige of gedeeltelijke hoeveelheid rapporteert.
