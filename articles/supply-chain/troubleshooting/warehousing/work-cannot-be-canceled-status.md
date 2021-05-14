---
title: Werk kan niet worden geannuleerd vanwege de status ervan
description: Werk kan niet worden geannuleerd vanwege de status ervan
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
ms.openlocfilehash: 60b4da44ca5e6790302e0797640317cef8493db7
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924250"
---
# <a name="work-cant-be-canceled-because-of-its-status"></a><span data-ttu-id="05e3d-103">Werk kan niet worden geannuleerd vanwege de status ervan</span><span class="sxs-lookup"><span data-stu-id="05e3d-103">Work can't be canceled because of its status</span></span>

<span data-ttu-id="05e3d-104">Foutcode: WAX2190</span><span class="sxs-lookup"><span data-stu-id="05e3d-104">Error code: WAX2190</span></span>

## <a name="symptoms"></a><span data-ttu-id="05e3d-105">Symptomen</span><span class="sxs-lookup"><span data-stu-id="05e3d-105">Symptoms</span></span>

<span data-ttu-id="05e3d-106">Het systeem toont het volgende foutbericht:</span><span class="sxs-lookup"><span data-stu-id="05e3d-106">The system shows the following error message:</span></span>

> <span data-ttu-id="05e3d-107">U kunt het werk %1 niet annuleren omdat het een status van %2 heeft.</span><span class="sxs-lookup"><span data-stu-id="05e3d-107">You cannot cancel work %1 because it has a status of %2.</span></span>

## <a name="cause"></a><span data-ttu-id="05e3d-108">Oorzaak</span><span class="sxs-lookup"><span data-stu-id="05e3d-108">Cause</span></span>

<span data-ttu-id="05e3d-109">Het werk kan in de huidige status niet worden geannuleerd.</span><span class="sxs-lookup"><span data-stu-id="05e3d-109">The work can't be canceled in its current state.</span></span>

<span data-ttu-id="05e3d-110">De werkkoptekst of werkregels hebben niet de verwachte **Werkstatus**-waarde.</span><span class="sxs-lookup"><span data-stu-id="05e3d-110">The work header or work lines don't have the expected **Work status** value.</span></span> <span data-ttu-id="05e3d-111">Het veld **Werkstatus** in de werkkoptekst is niet ingesteld op *Open* of *Wordt uitgevoerd*.</span><span class="sxs-lookup"><span data-stu-id="05e3d-111">The **Work status** field on the work header isn't set to *Open* or *In progress*.</span></span>

## <a name="resolution"></a><span data-ttu-id="05e3d-112">Oplossing</span><span class="sxs-lookup"><span data-stu-id="05e3d-112">Resolution</span></span>

<span data-ttu-id="05e3d-113">Volg deze stappen om werk te annuleren.</span><span class="sxs-lookup"><span data-stu-id="05e3d-113">To cancel the work, follow these steps.</span></span>

1. <span data-ttu-id="05e3d-114">Ga naar **Magazijnbeheer \> Periodieke taken \> Opschonen \> Werk annuleren**.</span><span class="sxs-lookup"><span data-stu-id="05e3d-114">Go to **Warehouse management \> Periodic tasks \> Clean up \> Cancel work**.</span></span>
1. <span data-ttu-id="05e3d-115">In het veld **Werk-id** geeft de id op van het werk dat u wilt annuleren.</span><span class="sxs-lookup"><span data-stu-id="05e3d-115">In the **Work ID** field, specify the ID of the work that you want to cancel.</span></span>
1. <span data-ttu-id="05e3d-116">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="05e3d-116">Select **OK**.</span></span>
1. <span data-ttu-id="05e3d-117">Selecteer **Ja** om te bevestigen dat u het werk wilt annuleren.</span><span class="sxs-lookup"><span data-stu-id="05e3d-117">Select **Yes** to confirm that you want to cancel the work.</span></span>

<span data-ttu-id="05e3d-118">Zie [Magazijnwerk voor afhandeling van uitzonderingen annuleren](../../warehousing/cancel-warehouse-work.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="05e3d-118">For more information, see [Cancel warehouse work for exception handling](../../warehousing/cancel-warehouse-work.md).</span></span>
