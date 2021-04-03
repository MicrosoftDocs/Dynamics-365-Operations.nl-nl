---
title: Een workflow voor verlofaanvragen maken
description: Maak een workflow voor verlof- en verzuimaanvragen om verlofaanvragen op consistente wijze te beheren in Dynamics 365 Human Resources.
author: andreabichsel
manager: tfehr
ms.date: 05/08/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: c2c2020c68c4aca3594a2532d32f968ab76f6b7b
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/17/2021
ms.locfileid: "5463305"
---
# <a name="create-a-leave-request-workflow"></a>Een workflow voor verlofaanvragen maken

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

5. Gebruik de workflow-editor om een workflow voor uw verlofaanvragen te maken. Zie [Overzicht van workflows maken](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/create-workflow?toc=/dynamics365/commerce/toc.json.) voor meer informatie over het werken met workflows.

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

- Met **Redencode** in een voorwaardelijke instructie kunt u ziekteverlofaanvragen met de redencode **Operatie** naar HR routeren voor goedkeuring, terwijl u alle andere redencodes aan de manager doorstuurt. Zie [Voorwaardelijke beslissingen in een workflow configureren](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-conditional-decision-workflow) voor meer informatie over voorwaardelijke instructies. 

- Gebruik **Ingediend door Human Resources** en **Ingediend door manager** in een automatische actie om verlofaanvragen die deze rollen namens werknemers indienen, automatisch goed te keuren. Zie [Goedkeuringsprocessen in een workflow configureren](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-approval-process-workflow) voor meer informatie over deze automatische acties.

- Gebruik **Verloftype** in een voorwaardelijke instructie of automatische actie om te bepalen hoe aanvragen met bepaalde verloftypen door de workflow worden gerouteerd.

## <a name="see-also"></a>Zie ook

- [Overzicht van verlof en verzuim](hr-leave-and-absence-overview.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]