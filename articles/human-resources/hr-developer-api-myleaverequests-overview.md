---
title: MyLeaveRequests-overzicht
description: De entiteit MyLeaveRequests in Microsoft Dynamics 365 Human Resources voorziet in de lijst met verlofaanvragen.
author: twheeloc
ms.date: 02/03/2020
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 20cc53ec3bcf38444ccf75f81e28d5efd9fc4537
ms.sourcegitcommit: 1d2eeacad11c28889681504cdc509c90e3e8ea86
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/05/2022
ms.locfileid: "8717050"
---
# <a name="myleaverequests-overview"></a>MyLeaveRequests-overzicht


[!INCLUDE [PEAP](../includes/peap-1.md)]

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
