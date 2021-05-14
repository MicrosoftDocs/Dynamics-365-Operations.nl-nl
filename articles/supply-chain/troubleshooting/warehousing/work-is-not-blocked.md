---
title: Werk wordt niet geblokkeerd
description: Werk wordt niet geblokkeerd
author: perlynne
ms.date: 04/15/2021
ms.topic: troubleshooting
ms.search.form: WHSWorkTable_WHSWorkUnblocking
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-05-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: d64ab282972e46e8857581b59e5705dd15667328
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924199"
---
# <a name="work-isnt-blocked"></a><span data-ttu-id="0aaf0-103">Werk wordt niet geblokkeerd</span><span class="sxs-lookup"><span data-stu-id="0aaf0-103">Work isn't blocked</span></span>

<span data-ttu-id="0aaf0-104">Foutcode: WHSUnblockNotBlockedWorkErrorMessage</span><span class="sxs-lookup"><span data-stu-id="0aaf0-104">Error code: WHSUnblockNotBlockedWorkErrorMessage</span></span>

## <a name="symptoms"></a><span data-ttu-id="0aaf0-105">Symptomen</span><span class="sxs-lookup"><span data-stu-id="0aaf0-105">Symptoms</span></span>

<span data-ttu-id="0aaf0-106">Het systeem toont het volgende foutbericht:</span><span class="sxs-lookup"><span data-stu-id="0aaf0-106">The system shows the following error message:</span></span>

> <span data-ttu-id="0aaf0-107">Werk met id %1 wordt niet geblokkeerd.</span><span class="sxs-lookup"><span data-stu-id="0aaf0-107">Work with Id %1 is not blocked.</span></span>

## <a name="cause"></a><span data-ttu-id="0aaf0-108">Oorzaak</span><span class="sxs-lookup"><span data-stu-id="0aaf0-108">Cause</span></span>

<span data-ttu-id="0aaf0-109">De optie **Geblokkeerde wave** op de wave is ingesteld op *Nee*.</span><span class="sxs-lookup"><span data-stu-id="0aaf0-109">The **Blocked wave** option on the wave is set to *No*.</span></span> <span data-ttu-id="0aaf0-110">Het werk kan niet worden vrijgegeven omdat het momenteel niet is geblokkeerd.</span><span class="sxs-lookup"><span data-stu-id="0aaf0-110">The work can't be unblocked because it isn't currently blocked.</span></span>

## <a name="resolution"></a><span data-ttu-id="0aaf0-111">Oplossing</span><span class="sxs-lookup"><span data-stu-id="0aaf0-111">Resolution</span></span>

 <span data-ttu-id="0aaf0-112">Alleen werk waarbij de optie **Geblokkeerde wave** op *Ja* is ingesteld, kan worden vrijgegeven.</span><span class="sxs-lookup"><span data-stu-id="0aaf0-112">Only work where the **Blocked wave** option is set to *Yes* can be unblocked.</span></span>
