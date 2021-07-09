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
# <a name="canceled-product-receipts-dont-update-transaction-status-to-registered"></a><span data-ttu-id="7c9a8-103">Geannuleerde productontvangstbonnen zorgen er niet voor dat de transactiestatus wordt bijgewerkt naar Geregistreerd</span><span class="sxs-lookup"><span data-stu-id="7c9a8-103">Canceled product receipts don't update transaction status to Registered</span></span>

## <a name="symptoms"></a><span data-ttu-id="7c9a8-104">Symptomen</span><span class="sxs-lookup"><span data-stu-id="7c9a8-104">Symptoms</span></span>

<span data-ttu-id="7c9a8-105">Wanneer u de actie **Productontvangstbonnen annuleren** bij een inkomende lading uitvoert, wordt de status van voorraadtransacties automatisch bijgewerkt van *Ontvangen* naar *Besteld*.</span><span class="sxs-lookup"><span data-stu-id="7c9a8-105">After you run the **Cancel product receipts** action on an inbound load, the system automatically updates the status of inventory transactions from *Received* to *Ordered*.</span></span>

## <a name="resolution"></a><span data-ttu-id="7c9a8-106">Oplossing</span><span class="sxs-lookup"><span data-stu-id="7c9a8-106">Resolution</span></span>

<span data-ttu-id="7c9a8-107">Wanneer pakbonnen worden geannuleerd voor uitgaande ladingen, blijft de status van voorraadtransacties *Opgenomen*.</span><span class="sxs-lookup"><span data-stu-id="7c9a8-107">When packing slips are canceled for outbound loads, the status of inventory transactions remains *Picked*.</span></span> <span data-ttu-id="7c9a8-108">Wanneer productontvangstbonnen van een inkomende lading echter worden geannuleerd, wordt de status van voorraadtransacties niet teruggezet naar *Geregistreerd*.</span><span class="sxs-lookup"><span data-stu-id="7c9a8-108">However, when product receipts from an inbound load are canceled, the status of inventory transactions isn't restored to *Registered*.</span></span> <span data-ttu-id="7c9a8-109">Nadat een productontvangstbon van een inkomende belasting is geannuleerd, moet de magazijnmedewerker daarom de artikelhoeveelheden voor de ladingen opnieuw registreren.</span><span class="sxs-lookup"><span data-stu-id="7c9a8-109">Therefore, after a product receipt from an inbound load is canceled, the warehouse worker must re-register item quantities for the loads.</span></span>

<span data-ttu-id="7c9a8-110">Zie [Artikelhoeveelheden registreren die binnenkomen op een inkomende lading](/dynamics365/supply-chain/warehousing/inbound-load-handling#register-item-quantities-arriving) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="7c9a8-110">For more information, see [Register item quantities that arrive on an inbound load](/dynamics365/supply-chain/warehousing/inbound-load-handling#register-item-quantities-arriving).</span></span>
