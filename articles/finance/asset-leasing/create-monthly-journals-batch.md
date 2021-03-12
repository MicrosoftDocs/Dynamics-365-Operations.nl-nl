---
title: Maandelijkse journaalposten maken in een batch
description: In dit onderwerp wordt uitgelegd hoe u journaalposten in een batch maakt om de efficiëntie te verhogen wanneer de maandelijkse leasekosten worden vastgelegd.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 7f46f289c58c32c535dd20fb510cf2812625c49c
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2021
ms.locfileid: "4971323"
---
# <a name="create-monthly-journal-entries-in-a-batch"></a><span data-ttu-id="00041-103">Maandelijkse journaalposten maken in een batch</span><span class="sxs-lookup"><span data-stu-id="00041-103">Create monthly journal entries in a batch</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="00041-104">In dit onderwerp wordt uitgelegd hoe u journaalposten in een batch maakt om de efficiëntie te verhogen wanneer de maandelijkse leasekosten worden vastgelegd.</span><span class="sxs-lookup"><span data-stu-id="00041-104">This topic explains how to create journal entries in a batch to help increase efficiency when monthly lease expenses are recorded.</span></span> <span data-ttu-id="00041-105">Batchverwerking kan worden gebruikt om journaalposten te maken op basis van meerdere schema's.</span><span class="sxs-lookup"><span data-stu-id="00041-105">Batch processing can be used to create journal entries from multiple schedules.</span></span> <span data-ttu-id="00041-106">Deze journaalposten kunnen bijvoorbeeld leasebetalingen, afschrijvingen van verplichtingen, afschrijving van RoU-activa en administratieve kosten bevatten.</span><span class="sxs-lookup"><span data-stu-id="00041-106">These journal entries can include lease payments, liability amortization, right-of-use (ROU) asset amortization, and executory cost expenses.</span></span> <span data-ttu-id="00041-107">U kunt ook batchverwerking gebruiken om de eerste toerekening van meerdere leases tegelijk uit te voeren of om tegelijkertijd overgangscorrecties voor meerdere leases te maken.</span><span class="sxs-lookup"><span data-stu-id="00041-107">You can also use batch processing to do the initial recognition of multiple leases at the same time, or to create transition adjustments for multiple leases at the same time.</span></span>

<span data-ttu-id="00041-108">Als u een batchtaak wilt instellen of betalingsfacturen, afschrijving of rente voor meerdere leases wilt verwerken, gaat u naar **Activa leasen \> Periodiek \> Batchjournaal maken**.</span><span class="sxs-lookup"><span data-stu-id="00041-108">To set up a batch job, or to process payment invoices, depreciation, or interest for multiple leases, go to **Asset leasing \> Periodic \> Batch journal creation**.</span></span> <span data-ttu-id="00041-109">In het dialoogvenster dat wordt weergegeven, kunt u de planning selecteren waaruit de journaalposten moeten worden gemaakt.</span><span class="sxs-lookup"><span data-stu-id="00041-109">In the dialog box that appears, you can select the schedule that the journal entries should be created from.</span></span> <span data-ttu-id="00041-110">U kunt ook opgeven of het batchproces moet worden uitgevoerd voor specifieke entiteiten, leasegroepen of leaseboeken.</span><span class="sxs-lookup"><span data-stu-id="00041-110">You can also specify whether the batch process should be run for specific entities, lease groups, or lease books.</span></span>

> [!NOTE]
> <span data-ttu-id="00041-111">Latere transacties, zoals het afschrijvingsschema verplichtingen, betalingen, afschrijving en onkosten, worden pas geboekt nadat de eerste toerekening voor bijbehorende leases is geboekt.</span><span class="sxs-lookup"><span data-stu-id="00041-111">Subsequent transactions, such as liability amortization schedules, payments, depreciation, and expenses, will be posted only after the initial recognition for corresponding leases is posted.</span></span>
>
> <span data-ttu-id="00041-112">De journaalposten worden gemaakt, maar ze worden pas geboekt wanneer u de opdracht **Uitvoeren** selecteert.</span><span class="sxs-lookup"><span data-stu-id="00041-112">The journal entries are created, but they won't be posted until you select the **Run** command.</span></span>
