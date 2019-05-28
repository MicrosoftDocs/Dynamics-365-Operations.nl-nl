---
title: Analytische rapporten worden niet bijgewerkt
description: In dit onderwerp wordt uitgelegd wat u moet doen als de gegevenswijzigingen van een klant niet in een van de werkgebieden van de klant worden weergegeven.
author: andreabichsel
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.openlocfilehash: d6a6487b50908093f876237ffef840a3144b3fe6
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/07/2019
ms.locfileid: "1517753"
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
