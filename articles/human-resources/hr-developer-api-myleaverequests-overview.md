---
title: MyLeaveRequests-overzicht
description: De entiteit MyLeaveRequests in Microsoft Dynamics 365 Human Resources levert de lijst met verlofaanvragen in het systeem, bereiken (beperkt) tot de aanvragen die toegankelijk zijn voor de huidige gebruiker die een query uitvoert op de entiteit.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: f29d5cf1469b58b4ea1837dc82b9513f5c002609
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/18/2021
ms.locfileid: "6054951"
---
# <a name="myleaverequests-overview"></a>MyLeaveRequests-overzicht

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

De entiteit MyLeaveRequests in Microsoft Dynamics 365 Human Resources levert de lijst met verlofaanvragen in het systeem, bereiken (beperkt) tot de aanvragen die toegankelijk zijn voor de huidige gebruiker die een query uitvoert op de entiteit.

## <a name="key"></a>Sleutel

  | Naam van eigenschap | Gegevenstype |
  |---------------|-----------|
  | dataAreaId    | Tekenreeks    |
  | RequestId     | Tekenreeks    |
  | LeaveType     | Tekenreeks    |
  | LeaveDate     | Datum      |
  
## <a name="properties"></a>Eigenschappen

  | Naam van eigenschap     | Gegevenstype | Vereist |
  |-------------------|-----------|----------|
  | dataAreaId        | Tekenreeks    | X        |
  | RequestId         | Tekenreeks    | X        |
  | LeaveType         | Tekenreeks    | X        |
  | LeaveDate         | Datum      | X        |
  | ReasonCodeId      | Tekenreeks    |          |
  | PersonnelNumber   | Tekenreeks    | X        |
  | RequestDate       | Datum      | X        |
  | Opmerking           | Tekenreeks    |          |
  | Status            | Opsomming      | X        |
  | Bedrag            | Real-modus      |          |
  | HalfDayDefinition | Opsomming      |          |

## <a name="actions"></a>Acties

 | Naam actie                               | Beschrijving                                     |
 |-------------------------------------------|-------------------------------------------------|
 | [submit](hr-developer-api-myleaverequests-submit.md)   | De aanvraag indienen om door de workflow te worden verwerkt. |

## <a name="see-also"></a>Zie ook

- [Een verlofverzoek indienen bij een werkstroom](hr-developer-api-myleaverequests-submit.md)
- [Verificatie](hr-developer-api-authentication.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]