---
title: Een workflow voor verlofaanvragen maken
description: Maak een workflow voor verlof- en verzuimaanvragen om verlofaanvragen op consistente wijze te beheren in Dynamics 365 Human Resources.
author: twheeloc
ms.date: 10/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 707b986c41cde2d4e26bdb4c5218b87b27702cee
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/31/2022
ms.locfileid: "8065171"
---
# <a name="create-a-leave-request-workflow"></a>Een workflow voor verlofaanvragen maken


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

U kunt een workflow maken in Dynamics 365 Human Resources voor het op consistente wijze beheren van uw verlof- en verzuimaanvragen. Met een workflow voor **Verlof en verzuim** kunt u:

- Taken definiëren
- Bepalen wie de taken moet voltooien
- Opgeven wie aanvragen kan goedkeuren of afwijzen

## <a name="create-a-leave-and-absence-request-workflow"></a>Een workflow voor verlof- en verzuimaanvragen maken

1. Selecteer op de pagina **Verlof en verzuim** het tabblad **Koppelingen**.

2. Selecteer onder **Instellen** de optie **Workflows voor Human resources**.

3. Selecteer **Nieuw** en selecteer vervolgens **Verlof- en verzuimaanvraag**. 

4. Wanneer het berichtvenster **Dit bestand openen?** verschijnt, selecteert u **Openen** en meldt u zich aan en met uw bedrijfsreferenties.

5. Gebruik de workflow-editor om een workflow voor uw verlofaanvragen te maken. Zie [Overzicht van workflows maken](../fin-ops-core/fin-ops/organization-administration/create-workflow.md?toc=%2fdynamics365%2fcommerce%2ftoc.json.) voor meer informatie over het werken met workflows.

## <a name="leave-and-absence-request-workflow-data-elements"></a>Gegevenselementen van workflow voor verlof- en verzuimaanvragen

U kunt de volgende gegevenselementen gebruiken om voorwaardelijke of automatische goedkeuringen te maken in workflows voor verlof- en verzuimaanvragen:

- **Bedrag**
- **Opmerking**
- **Bedrijf**
- **Gemaakt door**
- **Aanmaakdatum en -tijd**
- **Einddatum**
- **Verloftype**
- **Gewijzigd door**
- **Wijzigingsdatum en -tijd**
- **Redencode**
- **Aanvraag-ID**
- **Begindatum**
- **Status** 
- **Datum van indiening**
- **Ingediend door**
- **Ingediend door Human Resources**
- **Ingediend door manager**
- **Ingediend namens**
- **Werknemer**
- **Type medewerker**

In deze voorbeelden ziet u hoe u verschillende typen workflowvoorwaarden kunt maken met behulp van deze gegevenselementen:

- Met **Redencode** in een voorwaardelijke instructie kunt u ziekteverlofaanvragen met de redencode **Operatie** naar HR routeren voor goedkeuring, terwijl u alle andere redencodes aan de manager doorstuurt. Zie [Voorwaardelijke beslissingen in een workflow configureren](../fin-ops-core/fin-ops/organization-administration/configure-conditional-decision-workflow.md) voor meer informatie over voorwaardelijke instructies. 

- Gebruik **Ingediend door Human Resources** en **Ingediend door manager** in een automatische actie om verlofaanvragen die deze rollen namens werknemers indienen, automatisch goed te keuren. Zie [Goedkeuringsprocessen in een workflow configureren](../fin-ops-core/fin-ops/organization-administration/configure-approval-process-workflow.md) voor meer informatie over deze automatische acties.

- Gebruik **Verloftype** in een voorwaardelijke instructie of automatische actie om te bepalen hoe aanvragen met bepaalde verloftypen door de workflow worden gerouteerd.

## <a name="see-also"></a>Zie ook

- [Overzicht van verlof en verzuim](hr-leave-and-absence-overview.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
