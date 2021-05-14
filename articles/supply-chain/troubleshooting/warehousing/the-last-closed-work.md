---
title: De laatst afgesloten werkregel moet een wegzetten zijn
description: De laatst afgesloten werkregel moet een wegzetten zijn
author: perlynne
ms.date: 04/15/2021
ms.topic: troubleshooting
ms.search.form: WHSWorkTable_WHSWorkCancel, WHSWorkTableListPage_WHSWorkCancel
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-05-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: a5b78154b51252b3ac96ba28c254e823caf87019
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924370"
---
# <a name="the-last-closed-work-line-must-be-a-put"></a><span data-ttu-id="3ada4-103">De laatst afgesloten werkregel moet een wegzetten zijn</span><span class="sxs-lookup"><span data-stu-id="3ada4-103">The last closed work line must be a put</span></span>

<span data-ttu-id="3ada4-104">Foutcode: WAX1285</span><span class="sxs-lookup"><span data-stu-id="3ada4-104">Error code: WAX1285</span></span>

## <a name="symptoms"></a><span data-ttu-id="3ada4-105">Symptomen</span><span class="sxs-lookup"><span data-stu-id="3ada4-105">Symptoms</span></span>

<span data-ttu-id="3ada4-106">Het systeem toont het volgende foutbericht:</span><span class="sxs-lookup"><span data-stu-id="3ada4-106">The system shows the following error message:</span></span>

> <span data-ttu-id="3ada4-107">De laatst afgesloten werkregel moet een wegzetten zijn.</span><span class="sxs-lookup"><span data-stu-id="3ada4-107">The last closed work line must be a put.</span></span>

## <a name="cause"></a><span data-ttu-id="3ada4-108">Oorzaak</span><span class="sxs-lookup"><span data-stu-id="3ada4-108">Cause</span></span>

<span data-ttu-id="3ada4-109">Het werk kan in de huidige status niet worden geannuleerd.</span><span class="sxs-lookup"><span data-stu-id="3ada4-109">The work can't be canceled in its current state.</span></span>

<span data-ttu-id="3ada4-110">Op de laatste werkregel is het veld **Werkstatus** ingesteld op *Afgesloten*, maar het veld **Werktype** is niet ingesteld op *Wegzetten*.</span><span class="sxs-lookup"><span data-stu-id="3ada4-110">On the last work line, the **Work status** field is set to *Closed*, but the **Work type** field isn't set to *Put*.</span></span>

## <a name="resolution"></a><span data-ttu-id="3ada4-111">Oplossing</span><span class="sxs-lookup"><span data-stu-id="3ada4-111">Resolution</span></span>

<span data-ttu-id="3ada4-112">Volg deze stappen om werk te annuleren.</span><span class="sxs-lookup"><span data-stu-id="3ada4-112">To cancel the work, follow these steps.</span></span>

1. <span data-ttu-id="3ada4-113">Ga naar **Magazijnbeheer \> Periodieke taken \> Opschonen \> Werk annuleren**.</span><span class="sxs-lookup"><span data-stu-id="3ada4-113">Go to **Warehouse management \> Periodic tasks \> Clean up \> Cancel work**.</span></span>
1. <span data-ttu-id="3ada4-114">In het veld **Werk-id** geeft de id op van het werk dat u wilt annuleren.</span><span class="sxs-lookup"><span data-stu-id="3ada4-114">In the **Work ID** field, specify the ID of the work that you want to cancel.</span></span>
1. <span data-ttu-id="3ada4-115">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="3ada4-115">Select **OK**.</span></span>
1. <span data-ttu-id="3ada4-116">Selecteer **Ja** om te bevestigen dat u het werk wilt annuleren.</span><span class="sxs-lookup"><span data-stu-id="3ada4-116">Select **Yes** to confirm that you want to cancel the work.</span></span>

<span data-ttu-id="3ada4-117">Zie [Magazijnwerk voor afhandeling van uitzonderingen annuleren](../../warehousing/cancel-warehouse-work.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="3ada4-117">For more information, see [Cancel warehouse work for exception handling](../../warehousing/cancel-warehouse-work.md).</span></span>
