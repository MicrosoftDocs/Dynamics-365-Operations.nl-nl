---
title: Entiteiten voor containeractiviteiten
description: Dit artikel bevat informatie over containeractiviteiten die worden gebruikt om de voortgang van verzendcontainers te volgen.
author: yufeihuang
ms.date: 05/27/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2022-05-27
ms.dyn365.ops.version: 10.0.28
ms.openlocfilehash: 6a518003f8624ef05ac86be1b963c3f916420278
ms.sourcegitcommit: 5b34b41ae74269ba639e2876bc5862ef468da1cc
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 07/15/2022
ms.locfileid: "9167568"
---
# <a name="container-activities-entity"></a>Entiteit van containeractiviteiten

[!include [banner](../includes/banner.md)]

Containeractiviteiten worden gebruikt om de voortgang van verzendcontainers te volgen. Er wordt een record gemaakt voor elke etappe die is toegewezen aan de trajectsjabloon die wordt geselecteerd op het moment dat de verzendcontainer wordt gemaakt. Er worden ook records gemaakt wanneer de verzendcontainer wordt gemaakt via een gegevensentiteit.

Informatie over de voortgang van een verzendcontainer in transit wordt vaak ontvangen van een externe bron. Met de entiteit van containeractiviteiten kan een externe bron, zoals een expediteur, de record direct bijwerken. Handmatige update van gegevens is daarom niet vereist.

## <a name="container-activities-itmcontaineractivityentity"></a>Containeractiviteiten (ITMContainerActivityEntity)

U kunt de entiteit van containeractiviteiten (`ITMContainerActivityEntity`) gebruiken om extra activiteitsrecords te maken. Een expediteur kan ook updates doorgeven voor een bevestigde waarde voor **Werkelijke einddatum**.

| Name | Toewijzing | Gegevenstype | Sleutel | Verplicht |
|---|---|---|---|---|
| Werkelijke einddatum | ITMContainerActivityTable.ActualEndDate | Datetime | Nr. | Nr. |
| Leveringsmethode | ITMContainerActivityTable.DlvModeId | Nvarchar(10) | Nr. | Nr. |
| Geraamde einddatum | ITMContainerActivityTable.EsimatedDate | Datetime | Nr. | Nr. |
| Regelnummer | ITMContainerActivityTable.LineNum | Numeric(32, 16) | **Ja** | Nr. |
| Opmerkingen | ITMContainerActivityTable.Notes | nvarchar(MAX) | Nr. | Nr. |
| Activiteit | ITMContainerActivityTable.ShipActivityId | Nvarchar(10) | Nr. | **Ja** |
| Verzendcontainer | ITMContainerActivityTable.ShipContainerId | Nvarchar(20) | **Ja** | **Ja** |
| Reis | ITMContainerActivityTable.ShipId | Nvarchar(20) | **Ja** | **Ja** |
| Etappe | ITMContainerActivityTable.ShipLegId | Nvarchar(20) | Nr. | **Ja** |
| Serviceprovider | ITMContainerActivityTable.ShipServiceProvider | Nvarchar(20) | Nr. | Nr. |
| Temperatuur | ITMContainerActivityTable.ShipTemperature | Numeric(32, 6) | Nr. | Nr. |
| Vaartuig | ITMContainerActivityTable.ShipVesselId | Nvarchar(20) | Nr. | Nr. |
| Begindatum | ITMContainerActivityTable.StartDate | Datetime | Nr. | Nr. |

## <a name="tracking-control"></a>Controlecentrum voor tracering

Met het controlecentrum voor tracering is een update van een opgegeven bronveld mogelijk dat moet worden geactiveerd door een update van een opgegeven doelveld. Als zowel de waarde van het bronveld als de waarde van het doelveld worden bijgewerkt met de entiteit van containeractiviteiten, wordt in het doelveld de entiteitswaarde weergegeven. Dit gedrag is gerelateerd aan traceringscontrolerecords die een **Type maken**-waarde van *Doorlooptijd* hebben.

Voor kostengebieden die een **Type maken**-waarde van *Statusupdate* of *Leeg* hebben (een door de gebruiker gedefinieerde waarde), wordt de reisstatus of het doelveld automatisch bijgewerkt op basis van de traceringscontroleconfiguratie.

## <a name="calculated-fields"></a>Berekende velden

De waarden van de volgende velden in een containeractiviteitsrecord worden berekend op basis van de waarden van andere velden. Hoewel deze berekende velden niet in de gegevensentiteit zijn opgenomen, worden ze wel ingesteld als de velden worden opgegeven waarop de berekeningen zijn gebaseerd.

- **Geschatte dagen** = **Geschatte einddatum** – **Begindatum**
- **Werkelijke dagen** = **Werkelijke einddatum** – **Begindatum**
