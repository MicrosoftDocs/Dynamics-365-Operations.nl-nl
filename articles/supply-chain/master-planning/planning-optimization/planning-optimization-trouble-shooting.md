---
title: Problemen met Planningsoptimalisatie oplossen
description: In dit onderwerp wordt beschreven hoe u problemen kunt oplossen die kunnen optreden tijdens het werken met Planningsoptimalisatie.
author: ChristianRytt
ms.date: 05/07/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2020-5-7
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: 2100235fadabe6af87849aab7d9ec55d85ea66fa
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/01/2021
ms.locfileid: "5812878"
---
# <a name="troubleshoot-planning-optimization"></a>Problemen met Planningsoptimalisatie oplossen 

[!include [banner](../../includes/banner.md)]

In dit onderwerp wordt beschreven hoe u algemene problemen kunt oplossen die kunnen optreden tijdens het werken met Planningsoptimalisatie.

## <a name="installation-of-the-planning-optimization-add-in-doesnt-complete"></a>De installatie van de invoegtoepassing Planningsoptimalisatie wordt niet voltooid

Voor Planningsoptimalisatie is een omgeving met grote beschikbaarheid die Lifecycle Services (LCS) ondersteunt, tier 2 of hoger (geen OneBox-omgeving), met Dynamics 365 Supply Chain Management versie 10.0.7 of hoger vereist. Als u de invoegtoepassing in een OneBox-omgeving probeert te installeren, wordt de installatie niet voltooid.

**Oplossing**: annuleer de installatie en gebruik een omgeving met hoge beschikbaarheid, tier 2 of hoger (geen Onebox-omgeving).

## <a name="planning-of-batch-jobs-fails-when-planning-optimization-is-enabled"></a>Het plannen van batchtaken mislukt wanneer de Planningsoptimalisatie is ingeschakeld

Wanneer u Planningsoptimalisatie inschakelt, wordt de ingebouwde engine voor hoofdplanningen automatisch uitgeschakeld. Als bestaande batchtaken voor hoofdplanningen die zijn gemaakt voor de ingebouwde Supply Chain Management-planningsengine mislukken als zij worden geactiveerd terwijl de optie Planningsoptimalisatie gebruiken is ingeschakeld. Er kan een fout bericht worden weergegeven, zoals *Met deze bewerking wordt een hoofdplanning geactiveerd die niet wordt ondersteund wanneer Planningsoptimalisatie is ingeschakeld*.

**Oplossing**: annuleer alle batchtaken voor hoofdplanningen die zijn gemaakt voor de ingebouwde planningsengine van Supply Chain Management.

## <a name="planning-optimization-results-are-different-from-earlier-results"></a>Resultaten van Planningsoptimalisatie verschillen van eerdere resultaten

Planningsoptimalisatie wijkt op bepaalde gebieden af van het ingebouwde hoofdplanningsontwerp. Dit kan ook worden veroorzaakt door functies die in behandeling zijn.

**Oplossing**: voer Analyse aanpassen aan Planningsoptimalisatie uit en analyseer vervolgens de resultaten terwijl u de bijbehorende documentatie raadpleegt om de gevolgen te begrijpen. Zie [Analyse voor passende Planningsoptimalisatie](planning-optimization-fit-analysis.md) voor meer informatie.

## <a name="cant-enable-planning-optimization"></a>Kan Planningsoptimalisatie niet inschakelen

De **verbindingsstatus** moet **Verbonden** zijn voordat u **Planningsoptimalisatie gebruiken** kunt instellen op **Ja**. Zie [Aan de slag met Planningsoptimalisatie](get-started.md) voor meer informatie.

**Oplossing**: zorg ervoor dat de invoegtoepassing Planningsoptimalisatie correct is geïnstalleerd.

## <a name="error-message-is-shown-during-ctp"></a>Foutbericht wordt weergegeven tijdens CTP

Als u CTP (Capable to Promise) probeert uit te voeren vanuit een verkooporder wanneer Planningsoptimalisatie is ingeschakeld, wordt het volgende foutbericht weergegeven: *Met deze bewerking wordt een hoofdplanning geactiveerd die niet wordt ondersteund wanneer Planningsoptimalisatie is ingeschakeld*.

Dit houdt verband met een functie die in behandeling is en die wordt gepland als onderdeel van de ondersteuning voor productieorders.

**Oplossing:** vermijd CTP-berekeningen wanneer Planningsoptimalisatie is ingeschakeld totdat CTP-ondersteuning beschikbaar is.

## <a name="additional-resources"></a>Aanvullende bronnen

[Aan de slag met Planningsoptimalisatie](get-started.md)

[Analyse aanpassen aan Planningsoptimalisatie](planning-optimization-fit-analysis.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]