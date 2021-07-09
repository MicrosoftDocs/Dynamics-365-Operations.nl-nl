---
title: Geannuleerde productontvangstbonnen zorgen er niet voor dat de transactiestatus wordt bijgewerkt naar Geregistreerd
description: Wanneer u productontvangstbonnen bij een inkomende lading hebt geannuleerd, wordt de status van de voorraadtransactie automatisch bijgewerkt van Ontvangen naar Besteld.
author: GalynaFedorova
ms.date: 06/11/2021
ms.topic: troubleshooting
ms.search.form: WMSPickingRegistration
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-06-11
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 9c86457d50a7a9ac2a699a0e0a9c7bdf4cd7c67b
ms.sourcegitcommit: 18ca2df785e9656fdd4e8c0734eca2b2624fda10
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/22/2021
ms.locfileid: "6294045"
---
# <a name="canceled-product-receipts-dont-update-transaction-status-to-registered"></a>Geannuleerde productontvangstbonnen zorgen er niet voor dat de transactiestatus wordt bijgewerkt naar Geregistreerd

## <a name="symptoms"></a>Symptomen

Wanneer u de actie **Productontvangstbonnen annuleren** bij een inkomende lading uitvoert, wordt de status van voorraadtransacties automatisch bijgewerkt van *Ontvangen* naar *Besteld*.

## <a name="resolution"></a>Oplossing

Wanneer pakbonnen worden geannuleerd voor uitgaande ladingen, blijft de status van voorraadtransacties *Opgenomen*. Wanneer productontvangstbonnen van een inkomende lading echter worden geannuleerd, wordt de status van voorraadtransacties niet teruggezet naar *Geregistreerd*. Nadat een productontvangstbon van een inkomende belasting is geannuleerd, moet de magazijnmedewerker daarom de artikelhoeveelheden voor de ladingen opnieuw registreren.

Zie [Artikelhoeveelheden registreren die binnenkomen op een inkomende lading](/dynamics365/supply-chain/warehousing/inbound-load-handling#register-item-quantities-arriving) voor meer informatie.
