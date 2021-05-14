---
title: Werk blijft geblokkeerd
description: Werk blijft geblokkeerd
author: perlynne
ms.date: 04/15/2021
ms.topic: troubleshooting
ms.search.form: WHSWorkTableListPage_WHSWorkUnblocking
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-05-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: f85364d1ecfadc36b26c3395ab4402d3cb3b1603
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924125"
---
# <a name="work-remains-blocked"></a><span data-ttu-id="74b4a-103">Werk blijft geblokkeerd</span><span class="sxs-lookup"><span data-stu-id="74b4a-103">Work remains blocked</span></span>

<span data-ttu-id="74b4a-104">Foutcode: WHSWorkBlockingExecutingWaveReason_ErrorMessage</span><span class="sxs-lookup"><span data-stu-id="74b4a-104">Error code: WHSWorkBlockingExecutingWaveReason_ErrorMessage</span></span>

## <a name="symptoms"></a><span data-ttu-id="74b4a-105">Symptomen</span><span class="sxs-lookup"><span data-stu-id="74b4a-105">Symptoms</span></span>

<span data-ttu-id="74b4a-106">Het systeem toont het volgende foutbericht:</span><span class="sxs-lookup"><span data-stu-id="74b4a-106">The system shows the following error message:</span></span>

> <span data-ttu-id="74b4a-107">Werk %1 blijft geblokkeerd omdat de bijbehorende wave %2 de status %3 heeft.</span><span class="sxs-lookup"><span data-stu-id="74b4a-107">Work %1 remains blocked because the related wave %2 has status %3.</span></span>

## <a name="cause"></a><span data-ttu-id="74b4a-108">Oorzaak</span><span class="sxs-lookup"><span data-stu-id="74b4a-108">Cause</span></span>

<span data-ttu-id="74b4a-109">Het werk wordt op dit moment verwerkt op een wave en kan niet worden vrijgegeven, zoals aangegeven door een van de volgende voorwaarden:</span><span class="sxs-lookup"><span data-stu-id="74b4a-109">The work is currently being processed on a wave and can't be unblocked, as indicated by one of the following conditions:</span></span>

- <span data-ttu-id="74b4a-110">Op het tabblad **Blokkeringsredenen** is het veld **Werkblokkeringsreden** voor een of meer regels ingesteld op *Wave wordt uitgevoerd*.</span><span class="sxs-lookup"><span data-stu-id="74b4a-110">On the **Blocking reasons** tab, the **Work blocking reason** field for one or more lines is set to *Processing wave*.</span></span>
- <span data-ttu-id="74b4a-111">Als u het **Wave** selecteert in de groep **Gerelateerde informatie** op het tabblad **Gerelateerde informatie** van het actiedeelvenster, is het veld **Wavestatus** ingesteld op *Wordt uitgevoerd*.</span><span class="sxs-lookup"><span data-stu-id="74b4a-111">When you select **Wave** in the **Related information** group on the **Related information** tab of the Action Pane, the **Wave status** field is set to *Processing*.</span></span>

## <a name="resolution"></a><span data-ttu-id="74b4a-112">Oplossing</span><span class="sxs-lookup"><span data-stu-id="74b4a-112">Resolution</span></span>

<span data-ttu-id="74b4a-113">In het actiedeelvenster, op het tabblad **Gerelateerde informatie**, in de groep **Gerelateerde informatie**, selecteert u **Wave**.</span><span class="sxs-lookup"><span data-stu-id="74b4a-113">On the Action Pane, on the **Related information** tab, in the **Related information** group, select **Wave**.</span></span> <span data-ttu-id="74b4a-114">Vervolgens, op de pagina **Waves**, op het actiedeelvenster, op het tabblad **Wave**, in de groep **Wave**, selecteert u **Wavegegevens opschonen**.</span><span class="sxs-lookup"><span data-stu-id="74b4a-114">Then, on the **Waves** page, on the Action Pane, on the **Wave** tab, in the **Wave** group, select **Cleanup wave data**.</span></span>

## <a name="workaround"></a><span data-ttu-id="74b4a-115">Tijdelijke oplossing</span><span class="sxs-lookup"><span data-stu-id="74b4a-115">Workaround</span></span>

<span data-ttu-id="74b4a-116">Als het probleem niet is opgelost met voorgaande stappen, kunt u het werk annuleren door deze stappen te volgen.</span><span class="sxs-lookup"><span data-stu-id="74b4a-116">If the previous steps didn't fix the issue, you can cancel the work by following these steps.</span></span>

1. <span data-ttu-id="74b4a-117">Ga naar **Magazijnbeheer \> Periodieke taken \> Opschonen \> Werk annuleren**.</span><span class="sxs-lookup"><span data-stu-id="74b4a-117">Go to **Warehouse management \> Periodic tasks \> Clean up \> Cancel work**.</span></span>
1. <span data-ttu-id="74b4a-118">In het veld **Werk-id**, geeft u de id op van het werk dat u wilt annuleren en dat momenteel in **Werkstatus** een waarde heeft zoals *Open*, *Wordt uitgevoerd*, *Geannuleerd*, *Gecombineerd*, or *Afgesloten*.</span><span class="sxs-lookup"><span data-stu-id="74b4a-118">In the **Work ID** field, specify the ID of the work that you want to cancel, and that currently has a **Work status** value of *Open*, *In progress*, *Canceled*, *Combined*, or *Closed*.</span></span>
1. <span data-ttu-id="74b4a-119">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="74b4a-119">Select **OK**.</span></span>
1. <span data-ttu-id="74b4a-120">Selecteer **Ja** om te bevestigen dat u het werk wilt annuleren.</span><span class="sxs-lookup"><span data-stu-id="74b4a-120">Select **Yes** to confirm that you want to cancel the work.</span></span>

<span data-ttu-id="74b4a-121">Zie [Magazijnwerk voor afhandeling van uitzonderingen annuleren](../../warehousing/cancel-warehouse-work.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="74b4a-121">For more information, see [Cancel warehouse work for exception handling](../../warehousing/cancel-warehouse-work.md).</span></span>
