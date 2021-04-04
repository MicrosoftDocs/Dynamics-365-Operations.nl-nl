---
title: Een werkstroom maken voor het aanvragen voor het kopen en verkopen van verlof
description: Maak een werkstroom voor aanvragen voor het kopen en verkopen van verlof om aanvragen voor het kopen en verkopen van verlof op consistente wijze te beheren in Dynamics 365 Human Resources.
author: andreabichsel
manager: tfehr
ms.date: 08/20/2020
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
ms.search.validFrom: 2020-08-20
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 16260c66c2e92fb06664a8f20a5fc3ed4a964609
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/17/2021
ms.locfileid: "5468126"
---
# <a name="create-a-buy-and-sell-leave-request-workflow"></a>Een werkstroom maken voor het aanvragen voor het kopen en verkopen van verlof

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

U kunt in Dynamics 365 Human Resources een werkstroom maken om aanvragen voor het kopen en verkopen van verlof op consistente wijze te beheren. Met een werkstroom voor het **kopen en verkopen van verlof** kunt u:

- Taken definiëren
- Bepalen wie de taken moet voltooien
- Opgeven wie aanvragen kan goedkeuren of afwijzen

## <a name="create-a-buy-and-sell-leave-request-workflow"></a>Een werkstroom maken voor het aanvragen voor het kopen en verkopen van verlof

1. Selecteer op de pagina **Verlof en verzuim** het tabblad **Koppelingen**.

2. Selecteer onder **Instellen** de optie **Workflows voor Human resources**.

3. Selecteer **Nieuw** en selecteer vervolgens **Aanvraag om verlof te kopen en verkopen**. 

4. Wanneer het berichtvenster **Dit bestand openen?** verschijnt, selecteert u **Openen** en meldt u zich aan en met uw bedrijfsreferenties.

5. Gebruik de workflow-editor om een workflow voor uw verlofaanvragen te maken. Zie [Overzicht van workflows maken](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/create-workflow?toc=/dynamics365/commerce/toc.json.) voor meer informatie over het werken met workflows.

## <a name="leave-and-absence-request-workflow-data-elements"></a>Gegevenselementen van workflow voor verlof- en verzuimaanvragen

U kunt de volgende gegevenselementen gebruiken om voorwaardelijke of automatische goedkeuringen te maken in werkstromen voor aanvragen om verlof te kopen en verkopen:

- **Bedrag**
- **Beleid voor verlof inkopen/verkopen**
- **Bedrijf**
- **Gemaakt door**
- **Aanmaakdatum en -tijd**
- **Einddatum**
- **Verloftype**
- **Gewijzigd door**
- **Wijzigingsdatum en -tijd**
- **Aanvraag-ID**
- **Begindatum**
- **Status** 
- **Datum van indiening**
- **Ingediend door**
- **Ingediend door Human Resources**
- **Ingediend door manager**
- **Ingediend namens**
- **Werknemer**

## <a name="workflow-examples"></a>Voorbeelden van werkstromen

In deze voorbeelden ziet u hoe u verschillende typen workflowvoorwaarden kunt maken met behulp van deze gegevenselementen:

- Gebruik **Ingediend door Human Resources** en **Ingediend door manager** in een automatische actie om aanvragen voor het kopen en verkopen van verlof die deze rollen namens werknemers indienen, automatisch goed te keuren. Zie [Goedkeuringsprocessen in een workflow configureren](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-approval-process-workflow) voor meer informatie over deze automatische acties.

- Gebruik **Verloftype** in een voorwaardelijke instructie of automatische actie om te bepalen hoe aanvragen met bepaalde verloftypen door de workflow worden gerouteerd.

## <a name="see-also"></a>Zie ook

[Overzicht van verlof en verzuim](hr-leave-and-absence-overview.md)<br>
[Beleid voor verlof inkopen/verkopen beheren](hr-leave-and-absence-manage-buy-and-sell-leave-policies.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]