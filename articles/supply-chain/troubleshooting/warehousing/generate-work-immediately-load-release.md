---
title: Verzamelen werk onmiddellijk genereren wanneer belasting wordt vrijgegeven
description: Als werk onmiddellijk moet worden gegenereerd wanneer de lading wordt vrijgegeven, moet u de wavesjabloon dienovereenkomstig configureren. Deze pagina helpt bij het doorlopen van de stappen.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: fdeb0b27f4d2c1a2cc9f8e0c4ba537cdce604bd2
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476030"
---
# <a name="picking-work-isnt-generated-immediately-when-outbound-load-is-released"></a>Verzamelwerk wordt niet onmiddellijk gegenereerd wanneer een uitgaande belasting wordt vrijgegeven

## <a name="symptoms"></a>Symptomen

U maakt een uitgaande belasting aan door een verkoop- of transferorder te gebruiken en de belasting vrij te geven naar het magazijn. U bemerkt echter dat het verzamelwerk nog moet worden gegenereerd.

## <a name="resolution"></a>Oplossing

Als werk onmiddellijk moet worden gegenereerd wanneer de lading wordt vrijgegeven, moet u de wavesjabloon dienovereenkomstig configureren. Stel op de wavesjabloon de volgende opties in op *Ja*:

- Het maken van waves automatiseren
- Wave verwerken bij vrijgave door magazijn
- Vrijgave wave automatiseren
