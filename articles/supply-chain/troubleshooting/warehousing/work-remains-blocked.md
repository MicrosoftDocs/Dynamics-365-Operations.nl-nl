---
title: Werk blijft geblokkeerd
description: Werk blijft geblokkeerd
author: perlynne
ms.date: 04/15/2021
ms.topic: troubleshooting
ms.search.form: WHSWorkTableListPage_WHSWorkUnblocking
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-05-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 898390c78bb26fb8a44f77a10ad27a00720f7d1a3396cec5fff10e9d6b93364d
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/05/2021
ms.locfileid: "6768565"
---
# <a name="work-remains-blocked"></a>Werk blijft geblokkeerd

Foutcode: WHSWorkBlockingExecutingWaveReason_ErrorMessage

## <a name="symptoms"></a>Symptomen

Het systeem toont het volgende foutbericht:

> Werk %1 blijft geblokkeerd omdat de bijbehorende wave %2 de status %3 heeft.

## <a name="cause"></a>Oorzaak

Het werk wordt op dit moment verwerkt op een wave en kan niet worden vrijgegeven, zoals aangegeven door een van de volgende voorwaarden:

- Op het tabblad **Blokkeringsredenen** is het veld **Werkblokkeringsreden** voor een of meer regels ingesteld op *Wave wordt uitgevoerd*.
- Als u het **Wave** selecteert in de groep **Gerelateerde informatie** op het tabblad **Gerelateerde informatie** van het actiedeelvenster, is het veld **Wavestatus** ingesteld op *Wordt uitgevoerd*.

## <a name="resolution"></a>Oplossing

In het actiedeelvenster, op het tabblad **Gerelateerde informatie**, in de groep **Gerelateerde informatie**, selecteert u **Wave**. Vervolgens, op de pagina **Waves**, op het actiedeelvenster, op het tabblad **Wave**, in de groep **Wave**, selecteert u **Wavegegevens opschonen**.

## <a name="workaround"></a>Tijdelijke oplossing

Als het probleem niet is opgelost met voorgaande stappen, kunt u het werk annuleren door deze stappen te volgen.

1. Ga naar **Magazijnbeheer \> Periodieke taken \> Opschonen \> Werk annuleren**.
1. In het veld **Werk-id**, geeft u de id op van het werk dat u wilt annuleren en dat momenteel in **Werkstatus** een waarde heeft zoals *Open*, *Wordt uitgevoerd*, *Geannuleerd*, *Gecombineerd*, or *Afgesloten*.
1. Selecteer **OK**.
1. Selecteer **Ja** om te bevestigen dat u het werk wilt annuleren.

Zie [Magazijnwerk voor afhandeling van uitzonderingen annuleren](../../warehousing/cancel-warehouse-work.md) voor meer informatie.
