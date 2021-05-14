---
title: Wave komt niet in aanmerking voor opschonen
description: Wave komt niet in aanmerking voor opschonen
author: perlynne
ms.date: 04/15/2021
ms.topic: troubleshooting
ms.search.form: WHSWaveTable_WHSWaveProcessingDataCleanup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-05-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 3e5142cf40a6c0d308e8e952bbe17e85b498826d
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924322"
---
# <a name="wave-isnt-eligible-for-cleanup"></a><span data-ttu-id="89975-103">Wave komt niet in aanmerking voor opschonen</span><span class="sxs-lookup"><span data-stu-id="89975-103">Wave isn't eligible for cleanup</span></span>

<span data-ttu-id="89975-104">Foutcode: WaveNotEligibleForCleanup</span><span class="sxs-lookup"><span data-stu-id="89975-104">Error code: WaveNotEligibleForCleanup</span></span>

## <a name="symptoms"></a><span data-ttu-id="89975-105">Symptomen</span><span class="sxs-lookup"><span data-stu-id="89975-105">Symptoms</span></span>

<span data-ttu-id="89975-106">Het systeem toont het volgende foutbericht:</span><span class="sxs-lookup"><span data-stu-id="89975-106">The system shows the following error message:</span></span>

> <span data-ttu-id="89975-107">Wave %1 komt niet in aanmerking voor opschonen.</span><span class="sxs-lookup"><span data-stu-id="89975-107">Wave %1 is not eligible for cleanup.</span></span>

<span data-ttu-id="89975-108">De gegevens van de wave kunnen niet worden opgeschoond.</span><span class="sxs-lookup"><span data-stu-id="89975-108">The wave data can't be cleaned up.</span></span>  

## <a name="cause"></a><span data-ttu-id="89975-109">Oorzaak</span><span class="sxs-lookup"><span data-stu-id="89975-109">Cause</span></span>

<span data-ttu-id="89975-110">De wave wordt op dit moment verwerkt zoals aangegeven door een van de volgende voorwaarden:</span><span class="sxs-lookup"><span data-stu-id="89975-110">The wave is currently being processed, as indicated by one of the following conditions:</span></span>

- <span data-ttu-id="89975-111">Het veld **Wavestatus** is ingesteld op *Wordt uitgevoerd*.</span><span class="sxs-lookup"><span data-stu-id="89975-111">The **Wave status** field is set to *Executing*.</span></span>
- <span data-ttu-id="89975-112">Als u **Batchtaak** selecteert in de groep **Wave** op het tabblad **Wave** van het actiedeelvenster, is het veld **Status** niet ingesteld op *Beëindigd*, *Fout* of *Geannuleerd*.</span><span class="sxs-lookup"><span data-stu-id="89975-112">When you select **Batch job** in the **Wave** group on the **Wave** tab of the Action Pane, the **Status** field isn't set to *Ended*, *Error*, or *Canceled*.</span></span> <span data-ttu-id="89975-113">Daarom wordt er momenteel een batchtaak uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="89975-113">Therefore, a batch job is currently running.</span></span>

## <a name="resolution"></a><span data-ttu-id="89975-114">Oplossing</span><span class="sxs-lookup"><span data-stu-id="89975-114">Resolution</span></span>

<span data-ttu-id="89975-115">Op het actiedeelvenster, op het tabblad **Wave**, in de groep **Wave**, selecteert u **Batchtaak** en vervolgens volgt u een van deze stappen:</span><span class="sxs-lookup"><span data-stu-id="89975-115">On the Action Pane, on the **Wave** tab, in the **Wave** group, select **Batch job**, and then follow one of these steps:</span></span>

- <span data-ttu-id="89975-116">Als het veld **Status** is ingesteld op *Wordt uitgevoerd*: op het actiedeelvenster, op het tabblad **Batchtaak**, in de groep **Batchtaak**, selecteert u **Taken weergeven**.</span><span class="sxs-lookup"><span data-stu-id="89975-116">If the **Status** field is set to *Executing*: On the Action Pane, on the **Batch job** tab, in the **Batch job** group, select **View tasks**.</span></span> <span data-ttu-id="89975-117">U kunt de voortgang volgen door de pagina **Batchtaken** te vernieuwen.</span><span class="sxs-lookup"><span data-stu-id="89975-117">You can follow the progress by refreshing the **Batch tasks** page.</span></span>
- <span data-ttu-id="89975-118">Als het veld **Status** niet is ingesteld op *Wordt uitgevoerd*: op het actiedeelvenster, op het tabblad **Batchtaak**, in de groep **Functies**, selecteert u **Status wijzigen**.</span><span class="sxs-lookup"><span data-stu-id="89975-118">If the **Status** field isn't set to *Executing*: On the Action Pane, on the **Batch job** tab, in the **Functions** group, select **Change status**.</span></span> <span data-ttu-id="89975-119">In het veld **Nieuwe status selecteren**, selecteert u *Wachten*.</span><span class="sxs-lookup"><span data-stu-id="89975-119">In the **Select new status** field, select *Waiting*.</span></span> <span data-ttu-id="89975-120">Selecteer vervolgens **OK**.</span><span class="sxs-lookup"><span data-stu-id="89975-120">Then select **OK**.</span></span>
