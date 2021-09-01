---
title: Werk kan niet worden geannuleerd omdat het is geblokkeerd
description: Werk kan niet worden geannuleerd omdat het is geblokkeerd
author: perlynne
ms.date: 04/15/2021
ms.topic: troubleshooting
ms.search.form: WHSWorkTable_WHSWorkCancel
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-05-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: a24f199484c7596189b19e4cddf344e9186c6044edd2906affca9b530de44168
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/05/2021
ms.locfileid: "6722194"
---
# <a name="work-cant-be-canceled-because-its-blocked"></a>Werk kan niet worden geannuleerd omdat het is geblokkeerd

Foutcode: WHSCancellationOfWorkBlockedByExecutingWave_ErrorMessage

## <a name="symptoms"></a>Symptomen

Het systeem toont het volgende foutbericht:

> Werk %1 kan niet worden geannuleerd omdat dit is geblokkeerd door reden type %2. Het werk moet worden vrijgegeven voordat het geannuleerd kan worden.

## <a name="cause"></a>Oorzaak

Het werk is geblokkeerd en kan niet worden geannuleerd.

Op de pagina **Werk**, op het tabblad **Algemeen**, is de optie **Geblokkeerd** ingesteld op *Ja*. Deze instelling geeft aan dat het werk is geblokkeerd. Op het tabblad **Blokkeringsredenen** wordt weergegeven waarom het werk werd geblokkeerd.

## <a name="resolution"></a>Oplossing

Als u de blokkering wilt opheffen, selecteert u het tabblad **Blokkeringsredenen** en volgt u een van deze stappen:

- Als het veld **Werkblokkeringsreden** is ingesteld op *Niet-gedefinieerde reden*: op het actiedeelvenser, op het tabblad **Werk**, in de groep **Werk**, selecteer **Werk vrijgeven**.
- Als het veld **Werkblokkeringsreden** is ingesteld op *Wave verwerken*: op het actiedeelvenster, op het tabblad **Gerelateerde informatie**, in de groep **Gerelateerde informatie**, selecteert u **Wave**. Vervolgens, op de pagina **Waves**, op het actiedeelvenster, op het tabblad **Wave**, in de groep **Wave**, selecteert u **Wavegegevens opschonen**.

## <a name="workaround"></a>Tijdelijke oplossing

Als het probleem niet is opgelost met voorgaande stappen, kunt u het werk annuleren door deze stappen te volgen.

1. Ga naar **Magazijnbeheer \> Periodieke taken \> Opschonen \> Werk annuleren**.
1. In het veld **Werk-id**, geeft u de id op van het werk dat u wilt annuleren en dat momenteel in **Werkstatus** een waarde heeft zoals *Open*, *Wordt uitgevoerd*, *Geannuleerd*, *Gecombineerd*, or *Afgesloten*.
1. Selecteer **OK**.
1. Selecteer **Ja** om te bevestigen dat u het werk wilt annuleren.

Zie [Magazijnwerk voor afhandeling van uitzonderingen annuleren](../../warehousing/cancel-warehouse-work.md) voor meer informatie.
