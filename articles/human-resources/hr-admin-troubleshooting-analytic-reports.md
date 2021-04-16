---
title: Problemen met analytische rapporten oplossen
description: In dit artikel wordt uitgelegd wat u moet doen als de gegevenswijzigingen van een klant niet in een van de werkgebieden van de klant worden weergegeven.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: b500d519d61edfd20456355376e3fc81f16517a0
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/31/2021
ms.locfileid: "5794968"
---
# <a name="troubleshoot-analytic-reports"></a>Problemen met analytische rapporten oplossen

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

**Uitgifte**

De gegevenswijzigingen van een klant worden niet op het tabblad **Analyses** van de werkgebieden van de klant weergegeven.

**Oorzaak**

Standaard worden Microsoft Power BI-rapporten elke vier uur vernieuwd, volgens het schema van de batchtaak Meting implementeren.

**Resolutie**

Dit probleem kan ook een kwestie van timing zijn. Volg deze stappen om de batchtaak te starten en de werkgebieden voor analyses bij te werken.

1. Open de pagina **Batchtaken** via **Systeembeheer \> Koppelingen \> Batchtaken \> Batchtaken**. U kunt ook Zoeken gebruiken en **Batchtaken** invoeren.
1. Zoek de taak **Meting implementeren** in de lijst.
1. Selecteer **Bewerken** boven aan de pagina en stel de geplande begindatum/-tijd in waarmee de analyses dichter bij de huidige tijd worden vernieuwd.

![Batchtaken](media/batch-jobs.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]