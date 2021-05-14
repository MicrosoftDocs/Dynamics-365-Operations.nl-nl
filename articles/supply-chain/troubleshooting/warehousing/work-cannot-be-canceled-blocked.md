---
title: Werk kan niet worden geannuleerd omdat het is geblokkeerd
description: Werk kan niet worden geannuleerd omdat het is geblokkeerd
author: perlynne
ms.date: 04/15/2021
ms.topic: troubleshooting
ms.search.form: WHSWorkTable_WHSWorkCancel
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-05-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: a7ab4c7263947767164702fb7dd6da7573175253
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924274"
---
# <a name="work-cant-be-canceled-because-its-blocked"></a><span data-ttu-id="c7e83-103">Werk kan niet worden geannuleerd omdat het is geblokkeerd</span><span class="sxs-lookup"><span data-stu-id="c7e83-103">Work can't be canceled because it's blocked</span></span>

<span data-ttu-id="c7e83-104">Foutcode: WHSCancellationOfWorkBlockedByExecutingWave_ErrorMessage</span><span class="sxs-lookup"><span data-stu-id="c7e83-104">Error code: WHSCancellationOfWorkBlockedByExecutingWave_ErrorMessage</span></span>

## <a name="symptoms"></a><span data-ttu-id="c7e83-105">Symptomen</span><span class="sxs-lookup"><span data-stu-id="c7e83-105">Symptoms</span></span>

<span data-ttu-id="c7e83-106">Het systeem toont het volgende foutbericht:</span><span class="sxs-lookup"><span data-stu-id="c7e83-106">The system shows the following error message:</span></span>

> <span data-ttu-id="c7e83-107">Werk %1 kan niet worden geannuleerd omdat dit is geblokkeerd door reden type %2.</span><span class="sxs-lookup"><span data-stu-id="c7e83-107">Work %1 cannot be cancelled because it is blocked by reason type %2.</span></span> <span data-ttu-id="c7e83-108">Het werk moet worden vrijgegeven voordat het geannuleerd kan worden.</span><span class="sxs-lookup"><span data-stu-id="c7e83-108">The work must be unblocked before it can be cancelled.</span></span>

## <a name="cause"></a><span data-ttu-id="c7e83-109">Oorzaak</span><span class="sxs-lookup"><span data-stu-id="c7e83-109">Cause</span></span>

<span data-ttu-id="c7e83-110">Het werk is geblokkeerd en kan niet worden geannuleerd.</span><span class="sxs-lookup"><span data-stu-id="c7e83-110">The work is blocked and can't be canceled.</span></span>

<span data-ttu-id="c7e83-111">Op de pagina **Werk**, op het tabblad **Algemeen**, is de optie **Geblokkeerd** ingesteld op *Ja*.</span><span class="sxs-lookup"><span data-stu-id="c7e83-111">On the **Work** page, on the **General** tab, the **Blocked** option is set to *Yes*.</span></span> <span data-ttu-id="c7e83-112">Deze instelling geeft aan dat het werk is geblokkeerd.</span><span class="sxs-lookup"><span data-stu-id="c7e83-112">This setting indicates that the work is blocked.</span></span> <span data-ttu-id="c7e83-113">Op het tabblad **Blokkeringsredenen** wordt weergegeven waarom het werk werd geblokkeerd.</span><span class="sxs-lookup"><span data-stu-id="c7e83-113">The **Blocking reasons** tab shows why the work was blocked.</span></span>

## <a name="resolution"></a><span data-ttu-id="c7e83-114">Oplossing</span><span class="sxs-lookup"><span data-stu-id="c7e83-114">Resolution</span></span>

<span data-ttu-id="c7e83-115">Als u de blokkering wilt opheffen, selecteert u het tabblad **Blokkeringsredenen** en volgt u een van deze stappen:</span><span class="sxs-lookup"><span data-stu-id="c7e83-115">To unblock the work, select the **Blocking reasons** tab, and then follow one of these steps:</span></span>

- <span data-ttu-id="c7e83-116">Als het veld **Werkblokkeringsreden** is ingesteld op *Niet-gedefinieerde reden*: op het actiedeelvenser, op het tabblad **Werk**, in de groep **Werk**, selecteer **Werk vrijgeven**.</span><span class="sxs-lookup"><span data-stu-id="c7e83-116">If the **Work blocking reason** field is set to *Undefined reason*: On the Action Pane, on the **Work** tab, in the **Work** group, select **Unblock work**.</span></span>
- <span data-ttu-id="c7e83-117">Als het veld **Werkblokkeringsreden** is ingesteld op *Wave verwerken*: op het actiedeelvenster, op het tabblad **Gerelateerde informatie**, in de groep **Gerelateerde informatie**, selecteert u **Wave**.</span><span class="sxs-lookup"><span data-stu-id="c7e83-117">If the **Work blocking reason** field is set to *Processing wave*: On the Action Pane, on the **Related information** tab, in the **Related information** group, select **Wave**.</span></span> <span data-ttu-id="c7e83-118">Vervolgens, op de pagina **Waves**, op het actiedeelvenster, op het tabblad **Wave**, in de groep **Wave**, selecteert u **Wavegegevens opschonen**.</span><span class="sxs-lookup"><span data-stu-id="c7e83-118">Then, on the **Waves** page, on the Action Pane, on the **Wave** tab, in the **Wave** group, select **Cleanup wave data**.</span></span>

## <a name="workaround"></a><span data-ttu-id="c7e83-119">Tijdelijke oplossing</span><span class="sxs-lookup"><span data-stu-id="c7e83-119">Workaround</span></span>

<span data-ttu-id="c7e83-120">Als het probleem niet is opgelost met voorgaande stappen, kunt u het werk annuleren door deze stappen te volgen.</span><span class="sxs-lookup"><span data-stu-id="c7e83-120">If the previous steps didn't fix the issue, you can cancel the work by following these steps.</span></span>

1. <span data-ttu-id="c7e83-121">Ga naar **Magazijnbeheer \> Periodieke taken \> Opschonen \> Werk annuleren**.</span><span class="sxs-lookup"><span data-stu-id="c7e83-121">Go to **Warehouse management \> Periodic tasks \> Clean up \> Cancel work**.</span></span>
1. <span data-ttu-id="c7e83-122">In het veld **Werk-id**, geeft u de id op van het werk dat u wilt annuleren en dat momenteel in **Werkstatus** een waarde heeft zoals *Open*, *Wordt uitgevoerd*, *Geannuleerd*, *Gecombineerd*, or *Afgesloten*.</span><span class="sxs-lookup"><span data-stu-id="c7e83-122">In the **Work ID** field, specify the ID of the work that you want to cancel, and that currently has a **Work status** value of *Open*, *In progress*, *Canceled*, *Combined*, or *Closed*.</span></span>
1. <span data-ttu-id="c7e83-123">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="c7e83-123">Select **OK**.</span></span>
1. <span data-ttu-id="c7e83-124">Selecteer **Ja** om te bevestigen dat u het werk wilt annuleren.</span><span class="sxs-lookup"><span data-stu-id="c7e83-124">Select **Yes** to confirm that you want to cancel the work.</span></span>

<span data-ttu-id="c7e83-125">Zie [Magazijnwerk voor afhandeling van uitzonderingen annuleren](../../warehousing/cancel-warehouse-work.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="c7e83-125">For more information, see [Cancel warehouse work for exception handling](../../warehousing/cancel-warehouse-work.md).</span></span>
