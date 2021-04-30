---
title: Vastgelopen batchtaken opnieuw instellen
description: In dit onderwerp wordt uitgelegd hoe u problemen met vastgelopen batchtaken oplost.
author: andreabichsel
ms.date: 03/19/2021
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
ms.search.validFrom: 2021-03-19
ms.dyn365.ops.version: Platform update 42
ms.openlocfilehash: 906a391b3c28d15445f6ddf0fc547ebcf842ba19
ms.sourcegitcommit: d18d9cdb175c9d42eafbed66352c24b2aa94258b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/13/2021
ms.locfileid: "5881755"
---
# <a name="reset-stuck-batch-jobs"></a>Vastgelopen batchtaken opnieuw instellen

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

   ![Een nieuwe batchtaakstatus selecteren](./media/hr-admin-reset-batch-job-status.png)

## <a name="see-also"></a>Zie ook

[Prestaties optimaliseren door batchtaken buiten werktijd te plannen](hr-admin-troubleshooting-batch-jobs.md)<br>
[Prestaties optimaliseren met automatische opschoningstaken](hr-admin-troubleshooting-batch-history.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
