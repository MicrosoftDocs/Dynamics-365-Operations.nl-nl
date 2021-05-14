---
title: Gewicht moet positief zijn
description: Gewicht moet positief zijn
author: perlynne
ms.date: 04/15/2021
ms.topic: troubleshooting
ms.search.form: WHSContainerCloseDiag_canClose
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-05-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: dcbcde3143cb509b68b277cb7c709263e2659b5b
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924298"
---
# <a name="weight-must-be-positive"></a>Gewicht moet positief zijn

Foutcode: WeightMustBePositive

## <a name="symptoms"></a>Symptomen

Het systeem toont het volgende foutbericht:

> Gewicht moet positief zijn.

## <a name="cause"></a>Oorzaak

Het veld **Brutogewicht** is ingesteld op *0* (nul) of heeft een negatieve waarde.

## <a name="resolution"></a>Oplossing

Als u een gewicht wilt opgeven, volgt u een van deze stappen.

- Stel een waarde in het veld **Brutogewicht** in. Selecteer vervolgens een eenheid in de vervolgkeuzelijst.
- Selecteer **Systeemgewicht** om de waarde van het **Brutogewicht** te berekenen.
