---
title: Verkooporder kan niet worden vrijgegeven met uitgaande magazijnbewerkingen
description: Er zijn verschillende redenen waarom u een foutbericht zou kunnen ontvangen dat een verkooporder niet kan worden vrijgegeven. Deze pagina licht toe waarom en hoe u het probleem kunt beperken.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: fca5ee1bc97545ea4de56d940fdedd320a6cfe84
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476027"
---
# <a name="sales-order-could-not-be-released-with-outbound-warehouse-operations"></a>Verkooporder kan niet worden vrijgegeven met uitgaande magazijnbewerkingen

## <a name="symptoms"></a>Symptomen

Wanneer u met uitgaande magazijnbewerkingen werkt, wordt mogelijk het volgende foutbericht weergegeven:

> Verkooporder kon niet worden vrijgegeven.

## <a name="cause"></a>Oorzaak

Dit probleem kan zich om verschillende redenen voordoen. De order bevindt zich bijvoorbeeld in kredietbeheerblokkering en er kunnen geen zendingen worden gemaakt totdat een geldig postadres is ingevoerd voor alle verkoopregels die aan een verkooporder zijn gekoppeld. Er is ook een orderblokkering die moet worden opgeheven voordat de order aan het magazijn kan worden vrijgegeven. Deze blokkering kan orderspecifiek zijn of kan zich op de klantrekening bevinden.

## <a name="resolution"></a>Oplossing

Voeg het adres toe of werk het bij op de verkooporder en de orderregels en geef vervolgens de order vrij aan het magazijn. Orders kunnen alleen aan het magazijn worden vrijgegeven als ze een geldig afleveradres hebben (volgens de instelling van de adresnotatie in de module **Organisatiebeheer**).

Onderzoek de orderblokkering en los de problemen op. Vervolgens verwijdert u de blokkering van de order of klant en geeft u de order vrij aan het magazijn.
