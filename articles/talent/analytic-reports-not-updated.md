---
title: Analytische rapporten worden niet bijgewerkt
description: In dit onderwerp wordt uitgelegd wat u moet doen als de gegevenswijzigingen van een klant niet in een van de werkgebieden van de klant worden weergegeven.
author: Darinkramer
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.translationtype: HT
ms.sourcegitcommit: d3f974f94b6c327fd70b8098d24f9e1f1e1e8eeb
ms.openlocfilehash: 46f426a4b0012e87b4d9d21032870ac7fc33c4ae
ms.contentlocale: nl-nl
ms.lasthandoff: 12/04/2018

---

# <a name="analytic-reports-are-not-updated"></a>Analytische rapporten worden niet bijgewerkt

[!include [banner](includes/banner.md)]

**Probleem**

De gegevenswijzigingen van een klant worden niet op het tabblad **Analyses** van de werkgebieden van de klant weergegeven.

**Oorzaak**

Standaard worden Microsoft Power BI-rapporten elke vier uur vernieuwd, volgens het schema van de batchtaak Meting implementeren.

**Resolutie**

Dit probleem kan ook een kwestie van timing zijn. Volg deze stappen om de batchtaak te starten en de werkgebieden voor analyses bij te werken.

1. Open de pagina **Batchtaken** via **Systeembeheer \> Koppelingen \> Batchtaken \> Batchtaken**. U kunt ook Zoeken gebruiken en **Batchtaken** invoeren.
1. Zoek de taak **Meting implementeren** in de lijst.
1. Selecteer **Bewerken** boven aan de pagina en stel de geplande begindatum/-tijd in waarmee de analyses dichter bij de huidige tijd worden vernieuwd.

![Batchtaken](media/batch-jobs.png)
