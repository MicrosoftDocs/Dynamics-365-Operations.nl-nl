---
title: Wave komt niet in aanmerking voor opschonen
description: Wave komt niet in aanmerking voor opschonen
author: perlynne
ms.date: 04/15/2021
ms.topic: troubleshooting
ms.search.form: WHSWaveTable_WHSWaveProcessingDataCleanup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-05-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 3e5142cf40a6c0d308e8e952bbe17e85b498826d
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924322"
---
# <a name="wave-isnt-eligible-for-cleanup"></a>Wave komt niet in aanmerking voor opschonen

Foutcode: WaveNotEligibleForCleanup

## <a name="symptoms"></a>Symptomen

Het systeem toont het volgende foutbericht:

> Wave %1 komt niet in aanmerking voor opschonen.

De gegevens van de wave kunnen niet worden opgeschoond.  

## <a name="cause"></a>Oorzaak

De wave wordt op dit moment verwerkt zoals aangegeven door een van de volgende voorwaarden:

- Het veld **Wavestatus** is ingesteld op *Wordt uitgevoerd*.
- Als u **Batchtaak** selecteert in de groep **Wave** op het tabblad **Wave** van het actiedeelvenster, is het veld **Status** niet ingesteld op *Beëindigd*, *Fout* of *Geannuleerd*. Daarom wordt er momenteel een batchtaak uitgevoerd.

## <a name="resolution"></a>Oplossing

Op het actiedeelvenster, op het tabblad **Wave**, in de groep **Wave**, selecteert u **Batchtaak** en vervolgens volgt u een van deze stappen:

- Als het veld **Status** is ingesteld op *Wordt uitgevoerd*: op het actiedeelvenster, op het tabblad **Batchtaak**, in de groep **Batchtaak**, selecteert u **Taken weergeven**. U kunt de voortgang volgen door de pagina **Batchtaken** te vernieuwen.
- Als het veld **Status** niet is ingesteld op *Wordt uitgevoerd*: op het actiedeelvenster, op het tabblad **Batchtaak**, in de groep **Functies**, selecteert u **Status wijzigen**. In het veld **Nieuwe status selecteren**, selecteert u *Wachten*. Selecteer vervolgens **OK**.
