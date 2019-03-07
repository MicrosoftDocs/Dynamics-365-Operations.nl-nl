---
title: Een batchtaak maken
description: Een batchtaak is een groep taken die voor automatische verwerking naar een AOS-exemplaar (Application Object Server) worden verzonden.
author: maertenm
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BatchJob, SysRecurrence, BatchAlerts
audience: Application User
ms.reviewer: margoc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: fbb844ebcf8d4b47b127132a5bf0ea45fa40f747
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/29/2019
ms.locfileid: "313354"
---
# <a name="create-a-batch-job"></a><span data-ttu-id="ec4a3-103">Een batchtaak maken</span><span class="sxs-lookup"><span data-stu-id="ec4a3-103">Create a batch job</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="ec4a3-104">Een batchtaak is een groep taken die voor automatische verwerking naar een AOS-exemplaar (Application Object Server) worden verzonden.</span><span class="sxs-lookup"><span data-stu-id="ec4a3-104">A batch job is a group of tasks that are submitted to an Application Object Server (AOS) instance for automatic processing.</span></span> <span data-ttu-id="ec4a3-105">Batchtaken worden uitgevoerd met behulp van de beveiligingsgegevens van de gebruiker die de taak heeft gemaakt.</span><span class="sxs-lookup"><span data-stu-id="ec4a3-105">Batch jobs are run by using the security credentials of the user who created the job.</span></span> <span data-ttu-id="ec4a3-106">Voer de volgende procedure uit om een batchtaak te maken.</span><span class="sxs-lookup"><span data-stu-id="ec4a3-106">Use the following procedure to create a batch job.</span></span> <span data-ttu-id="ec4a3-107">Het bedrijf van de demogegevens dat wordt gebruikt om deze procedure te maken is USMF.</span><span class="sxs-lookup"><span data-stu-id="ec4a3-107">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-the-batch-job"></a><span data-ttu-id="ec4a3-108">De batchtaak maken</span><span class="sxs-lookup"><span data-stu-id="ec4a3-108">Create the batch job</span></span>
1. <span data-ttu-id="ec4a3-109">Ga naar Systeembeheer > Query's > Batchtaken.</span><span class="sxs-lookup"><span data-stu-id="ec4a3-109">Go to System administration > Inquiries > Batch jobs.</span></span>
2. <span data-ttu-id="ec4a3-110">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="ec4a3-110">Click New.</span></span>
3. <span data-ttu-id="ec4a3-111">Typ een waarde in het veld Taakomschrijving.</span><span class="sxs-lookup"><span data-stu-id="ec4a3-111">In the Job description field, type a value.</span></span>
4. <span data-ttu-id="ec4a3-112">Typ een datum en een tijd in het veld Geplande begindatum/tijd.</span><span class="sxs-lookup"><span data-stu-id="ec4a3-112">In the Scheduled start date/time field, enter a date and time.</span></span>
5. <span data-ttu-id="ec4a3-113">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="ec4a3-113">Click Save.</span></span>

## <a name="create-a-recurrence"></a><span data-ttu-id="ec4a3-114">Een terugkeerpatroon maken</span><span class="sxs-lookup"><span data-stu-id="ec4a3-114">Create a recurrence</span></span>
1. <span data-ttu-id="ec4a3-115">Klik in het actievenster op Batchtaak.</span><span class="sxs-lookup"><span data-stu-id="ec4a3-115">On the Action Pane, click Batch job.</span></span>
2. <span data-ttu-id="ec4a3-116">Klik op Terugkeerpatroon.</span><span class="sxs-lookup"><span data-stu-id="ec4a3-116">Click Recurrence.</span></span>
    * <span data-ttu-id="ec4a3-117">Gebruik deze opties om een bereik en terugkeerpatroon in te voeren.</span><span class="sxs-lookup"><span data-stu-id="ec4a3-117">Use these options to enter a range and pattern for the recurrence.</span></span>  
3. <span data-ttu-id="ec4a3-118">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="ec4a3-118">Click OK.</span></span>

## <a name="add-alerts"></a><span data-ttu-id="ec4a3-119">Waarschuwingen toevoegen</span><span class="sxs-lookup"><span data-stu-id="ec4a3-119">Add alerts</span></span>
1. <span data-ttu-id="ec4a3-120">Klik in het actievenster op Batchtaak.</span><span class="sxs-lookup"><span data-stu-id="ec4a3-120">On the Action Pane, click Batch job.</span></span>
2. <span data-ttu-id="ec4a3-121">Klik op Waarschuwingen.</span><span class="sxs-lookup"><span data-stu-id="ec4a3-121">Click Alerts.</span></span>
    * <span data-ttu-id="ec4a3-122">Geef aan of u waarschuwingsberichten wilt laten verzenden wanneer de batchtaak is voltooid, wanneer er een fout optreedt of wanneer de batchtaak wordt geannuleerd.</span><span class="sxs-lookup"><span data-stu-id="ec4a3-122">Indicate if you want alert messages sent when the batch job ends, has an error, or is canceled.</span></span> <span data-ttu-id="ec4a3-123">Geef vervolgens op of u waarschuwingen wilt laten weergeven als pop-upberichten.</span><span class="sxs-lookup"><span data-stu-id="ec4a3-123">Then specify if you want the alerts to be displayed as pop-up messages.</span></span>   
3. <span data-ttu-id="ec4a3-124">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="ec4a3-124">Click OK.</span></span>

