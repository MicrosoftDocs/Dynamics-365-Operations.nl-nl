---
title: Problemen met gedeeltelijke vrijgaven en gedeeltelijke zendingen oplossen
description: In dit onderwerp wordt beschreven hoe u veelvoorkomende problemen kunt oplossen die kunnen optreden tijdens werken gedeeltelijke vrijgaven en gedeeltelijke zendingen in Microsoft Dynamics 365 Supply Chain Management.
author: perlynne
manager: tfehr
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: e89a430f90374733b23fadaf53f5bab598d67d62
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/25/2020
ms.locfileid: "4645943"
---
# <a name="troubleshoot-partial-releases-and-partial-shipments"></a><span data-ttu-id="2d4a8-103">Problemen met gedeeltelijke vrijgaven en gedeeltelijke zendingen oplossen</span><span class="sxs-lookup"><span data-stu-id="2d4a8-103">Troubleshoot partial releases and partial shipments</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2d4a8-104">In dit onderwerp wordt beschreven hoe u veelvoorkomende problemen kunt oplossen die kunnen optreden tijdens werken gedeeltelijke vrijgaven en gedeeltelijke zendingen in Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="2d4a8-104">This topic describes how to fix common issues that you might encounter while you work with partial releases and partial shipments in Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="the-release-status-of-a-sales-order-remains-partially-released-even-after-the-sales-order-is-invoiced"></a><span data-ttu-id="2d4a8-105">De vrijgavestatus van een verkooporder blijft Gedeeltelijk vrijgegeven, zelfs nadat de verkooporder is gefactureerd.</span><span class="sxs-lookup"><span data-stu-id="2d4a8-105">The release status of a sales order remains Partially released even after the sales order is invoiced.</span></span>

### <a name="issue-description"></a><span data-ttu-id="2d4a8-106">Probleembeschrijving</span><span class="sxs-lookup"><span data-stu-id="2d4a8-106">Issue description</span></span>

<span data-ttu-id="2d4a8-107">Een verkooporder is een leveringsorder, maar een of meer artikelen op de order hebben een andere leveringsmethode.</span><span class="sxs-lookup"><span data-stu-id="2d4a8-107">A sales order is a delivery order, but one or more items on it have a different mode of delivery.</span></span> <span data-ttu-id="2d4a8-108">Nadat de order is gefactureerd, heeft deze nog steeds de vrijgavestatus *Gedeeltelijk vrijgegeven*.</span><span class="sxs-lookup"><span data-stu-id="2d4a8-108">After the order is invoiced, it still has a release status of *Partially released*.</span></span>

<span data-ttu-id="2d4a8-109">Een verkooporder heeft bijvoorbeeld twee artikelen: een voor levering en een voor ophalen.</span><span class="sxs-lookup"><span data-stu-id="2d4a8-109">For example, a sales order has two items: one for delivery and one for pickup.</span></span> <span data-ttu-id="2d4a8-110">De levering en het ophalen zijn voltooid.</span><span class="sxs-lookup"><span data-stu-id="2d4a8-110">Both the delivery and the pickup have been done.</span></span> <span data-ttu-id="2d4a8-111">Daarom zijn beide regels gefactureerd.</span><span class="sxs-lookup"><span data-stu-id="2d4a8-111">Therefore, both lines have been invoiced.</span></span> <span data-ttu-id="2d4a8-112">De vrijgavestatus wordt echter nog steeds weergegeven als *Gedeeltelijk vrijgegeven*. Dit is misleidend.</span><span class="sxs-lookup"><span data-stu-id="2d4a8-112">However, the release status is still shown as *Partially released*, which is misleading.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="2d4a8-113">Probleemoplossing</span><span class="sxs-lookup"><span data-stu-id="2d4a8-113">Issue resolution</span></span>

<span data-ttu-id="2d4a8-114">De vrijgavestatus is alleen van toepassing op orderregels met artikelen waarvoor magazijnbeheer is ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="2d4a8-114">The release status applies only to order lines where the items are enabled for warehouse management.</span></span> <span data-ttu-id="2d4a8-115">Daarom blijft de vrijgavestatus *Gedeeltelijk vrijgegeven* in dit scenario.</span><span class="sxs-lookup"><span data-stu-id="2d4a8-115">Therefore, the release status remains *Partially released* in this scenario.</span></span> <span data-ttu-id="2d4a8-116">Microsoft heeft dit probleem beoordeeld en heeft vastgesteld dat het een functiebeperking is.</span><span class="sxs-lookup"><span data-stu-id="2d4a8-116">Microsoft has evaluated this issue and has determined that it's a feature limitation.</span></span> <span data-ttu-id="2d4a8-117">Een uitbreiding kan worden toegevoegd als onderdeel van de pakbon en het factureringsproces om de vrijgavestatus bij te werken.</span><span class="sxs-lookup"><span data-stu-id="2d4a8-117">An extension could be added as part of the packing slip and invoicing process to update the release status.</span></span>
