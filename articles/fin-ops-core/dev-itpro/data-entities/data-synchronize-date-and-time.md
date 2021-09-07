---
title: Datum en tijd in importtaken synchroniseren
description: Gebruik UTC-tijdzones in importtaken om problemen met tijdzoneconversies te voorkomen.
author: peakerbl
ms.date: 12/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: sericks
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2020-12-01
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c76eadc5839785ba1624ee3894ef1d0872369aa9
ms.sourcegitcommit: 7aa7d756e1e98a53da62e03c608a9597ef9893ea
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/20/2021
ms.locfileid: "7403836"
---
# <a name="synchronize-date-and-time-in-import-jobs"></a>Datum en tijd in importtaken synchroniseren

[!include [banner](../includes/banner.md)]

Het is belangrijk om de tijdzone voor uw importtaak in te stellen op UTC (Coordinated Universal Time). Er worden mogelijk onverwachte datums en tijden voor uw geïmporteerde gegevens weergegeven als u een andere instelling gebruikt. Zonder de juiste instelling converteert het importproces de UTC-datum naar de lokale indeling, waarna deze opnieuw wordt geconverteerd via de systeeminstellingen.

Door deze dubbele conversie veranderen de datums tussen toepassingen. Bij de dubbele conversie kan bijvoorbeeld de begindatum van een werknemer verschillen tussen Dynamics 365 Human Resources en Dynamics 365 Finance door verschillen in lokale tijdzones. Als u de importtaak instelt op UTC, wordt dit probleem verholpen.

1. Selecteer in Dynamics 365 Finance and Operations **Gegevensbeheer**.

2. Selecteer **Projecten importeren** en dan het project.

3. Selecteer onder **Brondatumnotatie** de optie **CSV-Unicode**.

   [![De brondatumnotatie wijzigen in UTC.](./media/data-source-date-format.png)](./media/data-source-date-format.png)

4. Wijzig **de tijdzone** in **Coordinated Universal Timezone** en wijzig **Taal** in **En-US**.




[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
