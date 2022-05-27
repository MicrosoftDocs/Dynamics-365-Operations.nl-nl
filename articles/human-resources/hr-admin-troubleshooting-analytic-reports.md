---
title: Problemen met analytische rapporten oplossen
description: In dit onderwerp wordt uitgelegd hoe u problemen oplost en diagnosticeert als de gegevenswijzigingen van een klant niet in een van de werkgebieden van de klant worden weergegeven.
author: twheeloc
ms.date: 08/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 7e81bae4d9cb0bb0b77bb57bac16cc67bbbcf9ea
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/04/2022
ms.locfileid: "8694055"
---
# <a name="troubleshoot-analytic-reports"></a>Problemen met analytische rapporten oplossen


[!INCLUDE [PEAP](../includes/peap-2.md)]

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

![Batchtaken.](media/batch-jobs.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
