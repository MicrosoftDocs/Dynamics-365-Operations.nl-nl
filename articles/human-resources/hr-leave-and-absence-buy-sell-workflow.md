---
title: Een werkstroom maken voor het aanvragen voor het kopen en verkopen van verlof
description: Maak een werkstroom voor aanvragen voor het kopen en verkopen van verlof om aanvragen voor het kopen en verkopen van verlof op consistente wijze te beheren in Dynamics 365 Human Resources.
author: twheeloc
ms.date: 08/20/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-08-20
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: fabe2333bbf76edf31b77c0d5fce044273333de2
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8869802"
---
# <a name="create-a-buy-and-sell-leave-request-workflow"></a>Een werkstroom maken voor het aanvragen voor het kopen en verkopen van verlof


>[!Important]
>De functionaliteit die in dit artikel wordt vermeld, is momenteel beschikbaar voor klanten van de zelfstandige versie van Dynamics 365 Human Resources. Sommige of alle functionaliteit is beschikbaar als onderdeel van een toekomstige versie van de Finance-infrastructuur na versie 10.0.26 van Finance.


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

5. Gebruik de workflow-editor om een workflow voor uw verlofaanvragen te maken. Zie [Overzicht van workflows maken](../fin-ops-core/fin-ops/organization-administration/create-workflow.md?toc=%2fdynamics365%2fcommerce%2ftoc.json.) voor meer informatie over het werken met workflows.

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

- Gebruik **Ingediend door Human Resources** en **Ingediend door manager** in een automatische actie om aanvragen voor het kopen en verkopen van verlof die deze rollen namens werknemers indienen, automatisch goed te keuren. Zie [Goedkeuringsprocessen in een workflow configureren](../fin-ops-core/fin-ops/organization-administration/configure-approval-process-workflow.md) voor meer informatie over deze automatische acties.

- Gebruik **Verloftype** in een voorwaardelijke instructie of automatische actie om te bepalen hoe aanvragen met bepaalde verloftypen door de workflow worden gerouteerd.

## <a name="see-also"></a>Zie ook

[Overzicht van verlof en verzuim](hr-leave-and-absence-overview.md)<br>
[Beleid voor verlof inkopen/verkopen beheren](hr-leave-and-absence-manage-buy-and-sell-leave-policies.md)<br>
[Verlof inkopen en verkopen](hr-employee-self-service-buy-sell-leave.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
