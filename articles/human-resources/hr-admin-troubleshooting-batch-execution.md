---
title: Vastgelopen batchtaken opnieuw instellen
description: In dit artikel wordt uitgelegd hoe u problemen met vastgelopen batchtaken oplost.
author: twheeloc
ms.date: 03/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2021-03-19
ms.dyn365.ops.version: Platform update 42
ms.openlocfilehash: b56a16257a45dd093d10b7550b13d6a4a1ceb1f7
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8896013"
---
# <a name="reset-stuck-batch-jobs"></a>Vastgelopen batchtaken opnieuw instellen


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

## <a name="issue"></a>Uitgeven

Microsoft Dynamics 365 Human Resources kan problemen ondervinden met batchtaken die vastlopen in de status **Uitvoeren** of **Annuleren** en niet worden voltooid.

## <a name="resolution"></a>Oplossing

Wanneer een batchtaak vastloopt in de status **Uitvoeren** of **Annuleren**, u de status opnieuw instellen door de annulering van de taak af te dwingen. Nadat u deze hebt geannuleerd, kunt u de batchtaak opnieuw instellen door de status **Wachten** in te stellen. De taak wordt vervolgens weer opgehaald voor uitvoering in de volgende geplande batchrun.

1. Selecteer in de werkruimte **Systeembeheer** de pagina **Koppelingen** en selecteer **Batchtaken**.

2. Selecteer op de lijstpagina **Batchtaak** de taak die opnieuw moet worden ingesteld.

3. Selecteer op het actielint de optie **Annuleren afdwingen** en bevestig de actie.

   > [!NOTE]
   > De actie **Annuleren afdwingen** is alleen beschikbaar als de geselecteerde batchtaak de status **Uitvoeren** of **Annuleren** heeft en er geen processen voor batchuitvoering of -annulering worden uitgevoerd voor de taak.

4. Selecteer op het actielint de optie **Status wijzigen**.

5. Selecteer op de pagina **Nieuwe status selecteren** de optie **Wachten** en selecteer vervolgens **OK**.

   ![Een nieuwe batchtaakstatus selecteren.](./media/hr-admin-reset-batch-job-status.png)

## <a name="see-also"></a>Zie ook

[Prestaties optimaliseren door batchtaken buiten werktijd te plannen](hr-admin-troubleshooting-batch-jobs.md)<br>
[Prestaties optimaliseren met automatische opschoningstaken](hr-admin-troubleshooting-batch-history.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
