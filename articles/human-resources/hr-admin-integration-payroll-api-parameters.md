---
title: Parameters voor integratie van salarisadministratie
description: In dit onderwerp worden de parameters voor Salarisintegratie in Dynamics 365 Human Resources beschreven.
author: marcelbf
ms.date: 06/17/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-06-17
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 37d4dc52e7fe5ddd95f43d98267db819a275bd92
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/31/2022
ms.locfileid: "8069852"
---
# <a name="payroll-integration-parameters"></a>Parameters voor integratie van salarisadministratie


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Voordat u Salarisintegratie van Dynamics 365 Human Resources kunt gebruiken, moet u de parameters instellen die in dit onderwerp worden beschreven.

## <a name="enable-payroll-address"></a>Adres salarisadministratie inschakelen

Als u het adres salarisadministratie wilt gebruiken, moet u dit inschakelen vanuit het [formulier voor gedeelde parameters](hr-setup-shared-parameters.md) op het tabblad Salarisintegratie.

## <a name="define-the-identification-type"></a>Het type identificatie definiëren

Als u de id van het identificatietype beschikbaar wilt maken in de [entiteit Werknemer in salarisadministratie](hr-admin-integration-payroll-api-payroll-employee.md), moet u [Human resources-parameters configureren](hr-setup-shared-parameters.md) voor elk bedrijf.

1. Selecteer in het werkgebied **Vergoedingenbeheer** onder koppelingen de optie **Parameters voor Human Resources**. 
2. Geef op het tabblad **Salarisintegratie** de waarde van de volgende velden op.

| Veld | Beschrijving |
| --- | --- |
| Identificatietypen gebruiken in salarisverwerking | Als deze optie is geselecteerd, wordt de geselecteerde type-id beschikbaar gemaakt voor de entiteit Werknemer in salarisadministratie. |
| Identificatietype | Het identificatietype dat zichtbaar moet worden gemaakt in het veld **mshr_payrollemployeeentityid** van de [entiteit Werknemer in salarisadministratie](hr-admin-integration-payroll-api-payroll-employee.md). |

## <a name="see-also"></a>Zie ook

[Inleiding bij API voor integratie van salarisadministratie](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
