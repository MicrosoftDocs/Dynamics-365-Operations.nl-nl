---
title: Problemen met gedeeltelijke vrijgaven en gedeeltelijke zendingen oplossen
description: In dit onderwerp wordt beschreven hoe u veelvoorkomende problemen kunt oplossen die kunnen optreden tijdens werken gedeeltelijke vrijgaven en gedeeltelijke zendingen in Microsoft Dynamics 365 Supply Chain Management.
author: perlynne
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 5534099f81a97a1dcf4908784fd71dd03cf94eaf
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/01/2021
ms.locfileid: "5828149"
---
# <a name="troubleshoot-partial-releases-and-partial-shipments"></a><span data-ttu-id="55d12-103">Problemen met gedeeltelijke vrijgaven en gedeeltelijke zendingen oplossen</span><span class="sxs-lookup"><span data-stu-id="55d12-103">Troubleshoot partial releases and partial shipments</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="55d12-104">In dit onderwerp wordt beschreven hoe u veelvoorkomende problemen kunt oplossen die kunnen optreden tijdens werken gedeeltelijke vrijgaven en gedeeltelijke zendingen in Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="55d12-104">This topic describes how to fix common issues that you might encounter while you work with partial releases and partial shipments in Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="the-release-status-of-a-sales-order-remains-partially-released-even-after-the-sales-order-is-invoiced"></a><span data-ttu-id="55d12-105">De vrijgavestatus van een verkooporder blijft Gedeeltelijk vrijgegeven, zelfs nadat de verkooporder is gefactureerd.</span><span class="sxs-lookup"><span data-stu-id="55d12-105">The release status of a sales order remains Partially released even after the sales order is invoiced.</span></span>

### <a name="issue-description"></a><span data-ttu-id="55d12-106">Probleembeschrijving</span><span class="sxs-lookup"><span data-stu-id="55d12-106">Issue description</span></span>

<span data-ttu-id="55d12-107">Een verkooporder is een leveringsorder, maar een of meer artikelen op de order hebben een andere leveringsmethode.</span><span class="sxs-lookup"><span data-stu-id="55d12-107">A sales order is a delivery order, but one or more items on it have a different mode of delivery.</span></span> <span data-ttu-id="55d12-108">Nadat de order is gefactureerd, heeft deze nog steeds de vrijgavestatus *Gedeeltelijk vrijgegeven*.</span><span class="sxs-lookup"><span data-stu-id="55d12-108">After the order is invoiced, it still has a release status of *Partially released*.</span></span>

<span data-ttu-id="55d12-109">Een verkooporder heeft bijvoorbeeld twee artikelen: een voor levering en een voor ophalen.</span><span class="sxs-lookup"><span data-stu-id="55d12-109">For example, a sales order has two items: one for delivery and one for pickup.</span></span> <span data-ttu-id="55d12-110">De levering en het ophalen zijn voltooid.</span><span class="sxs-lookup"><span data-stu-id="55d12-110">Both the delivery and the pickup have been done.</span></span> <span data-ttu-id="55d12-111">Daarom zijn beide regels gefactureerd.</span><span class="sxs-lookup"><span data-stu-id="55d12-111">Therefore, both lines have been invoiced.</span></span> <span data-ttu-id="55d12-112">De vrijgavestatus wordt echter nog steeds weergegeven als *Gedeeltelijk vrijgegeven*. Dit is misleidend.</span><span class="sxs-lookup"><span data-stu-id="55d12-112">However, the release status is still shown as *Partially released*, which is misleading.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="55d12-113">Probleemoplossing</span><span class="sxs-lookup"><span data-stu-id="55d12-113">Issue resolution</span></span>

<span data-ttu-id="55d12-114">De vrijgavestatus is alleen van toepassing op orderregels met artikelen waarvoor magazijnbeheer is ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="55d12-114">The release status applies only to order lines where the items are enabled for warehouse management.</span></span> <span data-ttu-id="55d12-115">Daarom blijft de vrijgavestatus *Gedeeltelijk vrijgegeven* in dit scenario.</span><span class="sxs-lookup"><span data-stu-id="55d12-115">Therefore, the release status remains *Partially released* in this scenario.</span></span> <span data-ttu-id="55d12-116">Microsoft heeft dit probleem beoordeeld en heeft vastgesteld dat het een functiebeperking is.</span><span class="sxs-lookup"><span data-stu-id="55d12-116">Microsoft has evaluated this issue and has determined that it's a feature limitation.</span></span> <span data-ttu-id="55d12-117">Een uitbreiding kan worden toegevoegd als onderdeel van de pakbon en het factureringsproces om de vrijgavestatus bij te werken.</span><span class="sxs-lookup"><span data-stu-id="55d12-117">An extension could be added as part of the packing slip and invoicing process to update the release status.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]