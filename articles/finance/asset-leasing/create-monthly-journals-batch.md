---
title: Maandelijkse journaalposten maken in een batch
description: In dit onderwerp wordt uitgelegd hoe u journaalposten in een batch maakt om de efficiëntie te verhogen wanneer de maandelijkse leasekosten worden vastgelegd.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: Dialog
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: ca84e56569ea5ddbb4d5335d0944a6bd8a50a1b1
ms.sourcegitcommit: d18d9cdb175c9d42eafbed66352c24b2aa94258b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/13/2021
ms.locfileid: "5881199"
---
# <a name="create-monthly-journal-entries-in-a-batch"></a><span data-ttu-id="b9995-103">Maandelijkse journaalposten maken in een batch</span><span class="sxs-lookup"><span data-stu-id="b9995-103">Create monthly journal entries in a batch</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b9995-104">In dit onderwerp wordt uitgelegd hoe u journaalposten in een batch maakt om de efficiëntie te verhogen wanneer de maandelijkse leasekosten worden vastgelegd.</span><span class="sxs-lookup"><span data-stu-id="b9995-104">This topic explains how to create journal entries in a batch to help increase efficiency when monthly lease expenses are recorded.</span></span> <span data-ttu-id="b9995-105">Batchverwerking kan worden gebruikt om journaalposten te maken op basis van meerdere schema's.</span><span class="sxs-lookup"><span data-stu-id="b9995-105">Batch processing can be used to create journal entries from multiple schedules.</span></span> <span data-ttu-id="b9995-106">Deze journaalposten kunnen bijvoorbeeld leasebetalingen, afschrijvingen van verplichtingen, afschrijving van RoU-activa en administratieve kosten bevatten.</span><span class="sxs-lookup"><span data-stu-id="b9995-106">These journal entries can include lease payments, liability amortization, right-of-use (ROU) asset amortization, and executory cost expenses.</span></span> <span data-ttu-id="b9995-107">U kunt ook batchverwerking gebruiken om de eerste toerekening van meerdere leases tegelijk uit te voeren of om tegelijkertijd overgangscorrecties voor meerdere leases te maken.</span><span class="sxs-lookup"><span data-stu-id="b9995-107">You can also use batch processing to do the initial recognition of multiple leases at the same time, or to create transition adjustments for multiple leases at the same time.</span></span>

<span data-ttu-id="b9995-108">Als u een batchtaak wilt instellen of betalingsfacturen, afschrijving of rente voor meerdere leases wilt verwerken, gaat u naar **Activa leasen \> Periodiek \> Batchjournaal maken**.</span><span class="sxs-lookup"><span data-stu-id="b9995-108">To set up a batch job, or to process payment invoices, depreciation, or interest for multiple leases, go to **Asset leasing \> Periodic \> Batch journal creation**.</span></span> <span data-ttu-id="b9995-109">In het dialoogvenster dat wordt weergegeven, kunt u de planning selecteren waaruit de journaalposten moeten worden gemaakt.</span><span class="sxs-lookup"><span data-stu-id="b9995-109">In the dialog box that appears, you can select the schedule that the journal entries should be created from.</span></span> <span data-ttu-id="b9995-110">U kunt ook opgeven of het batchproces moet worden uitgevoerd voor specifieke entiteiten, leasegroepen of leaseboeken.</span><span class="sxs-lookup"><span data-stu-id="b9995-110">You can also specify whether the batch process should be run for specific entities, lease groups, or lease books.</span></span>

> [!NOTE]
> <span data-ttu-id="b9995-111">Latere transacties, zoals het afschrijvingsschema verplichtingen, betalingen, afschrijving en onkosten, worden pas geboekt nadat de eerste toerekening voor bijbehorende leases is geboekt.</span><span class="sxs-lookup"><span data-stu-id="b9995-111">Subsequent transactions, such as liability amortization schedules, payments, depreciation, and expenses, will be posted only after the initial recognition for corresponding leases is posted.</span></span>
>
> <span data-ttu-id="b9995-112">De journaalposten worden gemaakt, maar ze worden pas geboekt wanneer u de opdracht **Uitvoeren** selecteert.</span><span class="sxs-lookup"><span data-stu-id="b9995-112">The journal entries are created, but they won't be posted until you select the **Run** command.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
