---
title: Geplande productieorder moet worden gepland voordat deze kan worden gefiatteerd
description: Wanneer u een geplande order probeert te gefiatteerd, ontvangt u een foutbericht dat de order moet worden gepland voordat deze kan worden gefiatteerd.
author: ankubik
ms.date: 06/10/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ankubik
ms.search.validFrom: 2021-06-10
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: a360cb3cbd26e1bc1ebb1baf1a6a4d8282c28c5c
ms.sourcegitcommit: 18ca2df785e9656fdd4e8c0734eca2b2624fda10
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/22/2021
ms.locfileid: "6294051"
---
# <a name="planned-production-order-must-be-scheduled-before-it-can-be-firmed"></a><span data-ttu-id="5b300-103">Geplande productieorder moet worden gepland voordat deze kan worden gefiatteerd</span><span class="sxs-lookup"><span data-stu-id="5b300-103">Planned production order must be scheduled before it can be firmed</span></span>

<span data-ttu-id="5b300-104">Foutcode: SYS309802</span><span class="sxs-lookup"><span data-stu-id="5b300-104">Error code: SYS309802</span></span>

## <a name="symptoms"></a><span data-ttu-id="5b300-105">Symptomen</span><span class="sxs-lookup"><span data-stu-id="5b300-105">Symptoms</span></span>

<span data-ttu-id="5b300-106">Wanneer u een geplande order probeert te fiatteren, wordt het volgende foutbericht weergegeven:</span><span class="sxs-lookup"><span data-stu-id="5b300-106">When you try to firm a planned order, you receive the following error message:</span></span>

> <span data-ttu-id="5b300-107">De geplande productieorder moet worden gepland voordat deze kan worden gefiatteerd.</span><span class="sxs-lookup"><span data-stu-id="5b300-107">The planned production order must be scheduled before it can be firmed.</span></span>

## <a name="cause"></a><span data-ttu-id="5b300-108">Oorzaak</span><span class="sxs-lookup"><span data-stu-id="5b300-108">Cause</span></span>

<span data-ttu-id="5b300-109">De geplande begindatum en einddatum mogen niet leeg zijn.</span><span class="sxs-lookup"><span data-stu-id="5b300-109">The scheduled start and end dates can't be blank.</span></span>

## <a name="resolution"></a><span data-ttu-id="5b300-110">Oplossing</span><span class="sxs-lookup"><span data-stu-id="5b300-110">Resolution</span></span>

<span data-ttu-id="5b300-111">Als u de begin- en einddatum voor de geplande order wilt opgeven, gaat u als volgt te werk.</span><span class="sxs-lookup"><span data-stu-id="5b300-111">To specify start and end dates for the planned order, follow these steps.</span></span>

1. <span data-ttu-id="5b300-112">Ga naar **Hoofdplanning \> Hoofdplanning \> Geplande orders**.</span><span class="sxs-lookup"><span data-stu-id="5b300-112">Go to **Master planning \> Master planning \> Planned orders**.</span></span>
1. <span data-ttu-id="5b300-113">Open de betreffende geplande order.</span><span class="sxs-lookup"><span data-stu-id="5b300-113">Open the relevant planned order.</span></span>
1. <span data-ttu-id="5b300-114">Geef in het sneltabblad **Algemeen** in de sectie **Gepland** datums op in de velden **Begindatum** en **Einddatum**.</span><span class="sxs-lookup"><span data-stu-id="5b300-114">On the **General** FastTab, in the **Scheduled** section, specify dates in the **Start date** and **End date** fields.</span></span>
