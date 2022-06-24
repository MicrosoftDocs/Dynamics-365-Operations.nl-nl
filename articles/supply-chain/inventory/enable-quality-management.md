---
title: Beheer van kwaliteit en niet-conformeringen inschakelen
description: Dit artikel bevat een overzicht van het proces voor het instellen en configureren van de functies voor beheer van kwaliteit en niet-conformeringen in Microsoft Dynamics 365 Supply Chain Management.
author: yufeihuang
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTestAssociationTable, InventTestGroup, InventTestItemQualityGroup, InventTestTable, InventTestVariable, InventTestVariableOutcome, InventParameters, InventProblemType, InventProblemTypeSetup, InventQuarantineZone, InventTestDiagnosticType, InventTestReportSetup, SysUserManagement, InventTestRelatedOperations
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yufeihuang
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 66229e3692e87f774c553eae955794330602598c
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8874038"
---
# <a name="enable-quality-and-nonconformance-management"></a>Beheer van kwaliteit en niet-conformeringen inschakelen

[!include [banner](../includes/banner.md)]

Dit artikel bevat een overzicht van het proces voor het instellen en configureren van de functies voor beheer van kwaliteit en niet-conformeringen in Microsoft Dynamics 365 Supply Chain Management.

## <a name="enable-quality-and-nonconformance-management"></a><a name="enable-qm"></a>Beheer van kwaliteit en niet-conformeringen inschakelen

Volg deze stappen om kwaliteitsbeheer op uw systeem in te schakelen.

1. Ga naar **Voorraadbeheer \> Instellen \> Parameters voor voorraad- en magazijnbeheer**.
1. Stel op het tabblad **Kwaliteitsbeheer** de optie **Kwaliteitsbeheer gebruiken** in op *Ja*.
1. Voer in het veld **Uurtarief** een uurtarief in de lokale valuta in. Het uurtarief wordt gebruikt voor het berekenen van de kosten voor bewerkingen die zijn gerelateerd aan een niet-conformering. Het uurtarief en de berekende kosten vormen referentiegegevens voor een niet-conformering. Ze worden niet samen met andere functies gebruikt.
1. Selecteer **Rapportinstellingen**.
1. Voeg nieuwe regels toe voor de verschillende rapporttypen en selecteer het type document dat u voor elk rapport wilt gebruiken.
1. Sluit de pagina.
1. Sluit de pagina.

## <a name="quality-management-configuration-process"></a>Het proces voor configureren van kwaliteitsbeheer

Voordat u de functies voor kwaliteitsbeheer kunt gebruiken en kwaliteitsorders kunt genereren, moet u het systeem en de vereisten configureren. Hieronder volgt een lijst met de stappen die nodig zijn om kwaliteitsbeheer te configureren.

1. [Beheer van kwaliteit en niet-conformeringen inschakelen](#enable-qm).
1. Optioneel: [Testinstrumenten configureren](quality-test-instruments.md).
1. [Tests configureren](quality-tests.md).
1. [Testvariabelen en resultaten configureren](quality-test-variables.md).
1. [Testgroepen configureren](quality-test-groups.md).
1. Optioneel: [Kwaliteitsgroepen configureren en aan producten koppelen](quality-groups.md).
1. Optioneel: [Kwaliteitskoppelingen configureren](quality-associations.md).

Nadat het configureren is voltooid, kunt u beginnen met het maken en verwerken van kwaliteitsorders. Meer informatie over het maken van en werken met kwaliteitsorders vindt u in [Kwaliteitsorders](quality-orders.md).

## <a name="nonconformance-management-configuration-process"></a>Het proces voor configureren van niet-conformeringen

Voordat u de functies voor beheer van niet-conformeringen kunt gebruiken en niet-conformeringen kunt genereren, moet u het systeem en de vereisten configureren. Hieronder volgt een lijst met de stappen die nodig zijn om het beheer van niet-conformeringen te configureren.

1. [Beheer van kwaliteit en niet-conformeringen inschakelen](#enable-qm).
1. [Medewerkers configureren die verantwoordelijk zijn voor het goedkeuren van niet-conformeringen](quality-responsible-workers.md).
1. [Probleemtypen configureren](quality-problem-types.md).
1. [Quarantainezones configureren](quality-quarantine-zones.md).
1. [Diagnosetypen configureren](quality-diagnostic-types.md).
1. [Bewerkingen configureren](quality-operations.md).
1. Optioneel: [Kwaliteitstoeslagen configureren](quality-charges.md).

Nadat het configureren is voltooid, kunt u beginnen met het maken en verwerken van niet-conformeringen. Meer informatie over het maken van en werken met niet-conformeringen vindt u in [Niet-conformeringen maken en verwerken](tasks/create-process-non-conformance.md).

## <a name="additional-resources"></a>Aanvullende bronnen

- [Overzicht van kwaliteitsbeheer](quality-management-processes.md)
- [Beheer van kwaliteit en niet-conformeringen inschakelen](enable-quality-management.md)
- [Kwaliteitsbeheer voor magazijnprocessen](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
