---
title: Problemen met uitgaande magazijnbewerkingen oplossen
description: In dit onderwerp wordt beschreven hoe u veelvoorkomende problemen kunt oplossen die kunnen optreden tijdens werken met uitgaande magazijnbewerkingen in Microsoft Dynamics 365 Supply Chain Management.
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
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 165ac8145ad75c2c6619764b9abe855b9d32eb46
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2021
ms.locfileid: "4993973"
---
# <a name="troubleshoot-outbound-warehouse-operations"></a><span data-ttu-id="d81ae-103">Problemen met uitgaande magazijnbewerkingen oplossen</span><span class="sxs-lookup"><span data-stu-id="d81ae-103">Troubleshoot outbound warehouse operations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d81ae-104">In dit onderwerp wordt beschreven hoe u veelvoorkomende problemen kunt oplossen die kunnen optreden tijdens werken met uitgaande magazijnbewerkingen in Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="d81ae-104">This topic describes how to fix common issues that you might encounter while you work with outbound warehouse operations in Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="i-receive-the-following-error-message-sales-order-could-not-be-released"></a><span data-ttu-id="d81ae-105">Het volgende fout bericht wordt weergegeven: "Verkooporder kan niet worden vrijgegeven."</span><span class="sxs-lookup"><span data-stu-id="d81ae-105">I receive the following error message: "Sales order could not be released."</span></span>

### <a name="issue-description"></a><span data-ttu-id="d81ae-106">Probleembeschrijving</span><span class="sxs-lookup"><span data-stu-id="d81ae-106">Issue description</span></span>

<span data-ttu-id="d81ae-107">Dit probleem kan zich om verschillende redenen voordoen.</span><span class="sxs-lookup"><span data-stu-id="d81ae-107">This issue can occur for several reasons.</span></span> <span data-ttu-id="d81ae-108">De order bevindt zich bijvoorbeeld in kredietbeheerblokkering en er kunnen geen zendingen worden gemaakt totdat een geldig postadres is ingevoerd voor alle verkoopregels die aan een verkooporder zijn gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="d81ae-108">For example, the order is on credit management hold, and no shipments can be created until a valid postal address is entered for all sales lines that are associated with a sales order.</span></span> <span data-ttu-id="d81ae-109">Er is ook een orderblokkering die moet worden opgeheven voordat de order aan het magazijn kan worden vrijgegeven.</span><span class="sxs-lookup"><span data-stu-id="d81ae-109">Alternatively, there is an order hold that must be addressed before the order can be released to the warehouse.</span></span> <span data-ttu-id="d81ae-110">Deze blokkering kan orderspecifiek zijn of kan zich op de klantrekening bevinden.</span><span class="sxs-lookup"><span data-stu-id="d81ae-110">This hold might be order-specific, or it might be on the customer account.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="d81ae-111">Probleemoplossing</span><span class="sxs-lookup"><span data-stu-id="d81ae-111">Issue resolution</span></span>

<span data-ttu-id="d81ae-112">Voeg het adres toe of werk het bij op de verkooporder en de orderregels en geef vervolgens de order vrij aan het magazijn.</span><span class="sxs-lookup"><span data-stu-id="d81ae-112">Add or update the address on the sales order and order lines, and then release the order to the warehouse.</span></span> <span data-ttu-id="d81ae-113">Orders kunnen alleen aan het magazijn worden vrijgegeven als ze een geldig afleveradres hebben (volgens de instelling van de adresnotatie in de module **Organisatiebeheer**).</span><span class="sxs-lookup"><span data-stu-id="d81ae-113">Orders can be released to the warehouse only if they have a valid delivery address (per the address format setup in the **Organization administration** module).</span></span>

<span data-ttu-id="d81ae-114">Onderzoek de orderblokkering en los de problemen op.</span><span class="sxs-lookup"><span data-stu-id="d81ae-114">Investigate the order hold, and address the issues.</span></span> <span data-ttu-id="d81ae-115">Vervolgens verwijdert u de blokkering van de order of klant en geeft u de order vrij aan het magazijn.</span><span class="sxs-lookup"><span data-stu-id="d81ae-115">Then remove the hold from the order or customer, and release the order to the warehouse.</span></span>

## <a name="i-receive-the-following-message-the-shipment-for-load-1-has-been-confirmed-however-no-lines-are-posted"></a><span data-ttu-id="d81ae-116">Het volgende bericht wordt weergegeven: "De zending voor de lading 1% is bevestigd."</span><span class="sxs-lookup"><span data-stu-id="d81ae-116">I receive the following message: "The shipment for load 1% has been confirmed."</span></span> <span data-ttu-id="d81ae-117">Er worden echter geen regels geboekt.</span><span class="sxs-lookup"><span data-stu-id="d81ae-117">However, no lines are posted.</span></span>

### <a name="issue-description"></a><span data-ttu-id="d81ae-118">Probleembeschrijving</span><span class="sxs-lookup"><span data-stu-id="d81ae-118">Issue description</span></span>

<span data-ttu-id="d81ae-119">Een zending in een lading is bevestigd, maar er is geen verdere boeking uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="d81ae-119">A shipment on a load was confirmed, but no further posting occurred.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="d81ae-120">Probleemoplossing</span><span class="sxs-lookup"><span data-stu-id="d81ae-120">Issue resolution</span></span>

<span data-ttu-id="d81ae-121">De zendingsbevestiging heeft geen invloed op de boeking.</span><span class="sxs-lookup"><span data-stu-id="d81ae-121">Shipment confirmation doesn't affect posting.</span></span> <span data-ttu-id="d81ae-122">Hiermee wordt alleen de zendings- en ladingstatus bijgewerkt.</span><span class="sxs-lookup"><span data-stu-id="d81ae-122">It just updates the shipment and load status.</span></span> <span data-ttu-id="d81ae-123">De boeking moet plaatsvinden in een afzonderlijk proces.</span><span class="sxs-lookup"><span data-stu-id="d81ae-123">Posting must occur in a separate process.</span></span>

## <a name="i-receive-the-following-error-message-direct-delivery-is-not-able-to-process-for-warehouse-1-as-it-has-warehouse-management-enabled-please-specify-another-warehouse-that-is-not-enabled-for-warehouse-management"></a><span data-ttu-id="d81ae-124">Het volgende foutbericht wordt weergegeven: "Rechtstreekse levering verwerken kan niet voor magazijn 1% omdat magazijnbeheer is ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="d81ae-124">I receive the following error message: "Direct delivery is not able to process for warehouse 1% as it has warehouse management enabled.</span></span> <span data-ttu-id="d81ae-125">Geef een ander magazijn op waarvoor magazijnbeheer niet is ingeschakeld."</span><span class="sxs-lookup"><span data-stu-id="d81ae-125">Please specify another warehouse that is not enabled for warehouse management."</span></span>

### <a name="issue-description"></a><span data-ttu-id="d81ae-126">Probleembeschrijving</span><span class="sxs-lookup"><span data-stu-id="d81ae-126">Issue description</span></span>

<span data-ttu-id="d81ae-127">Er wordt een artikel toegevoegd aan een verkoopregel voor rechtstreekse levering vanuit een magazijn dat is ingeschakeld voor magazijnbeheer (WMS).</span><span class="sxs-lookup"><span data-stu-id="d81ae-127">An item is added to a sales line for direct delivery from a warehouse that is enabled for warehouse management (WMS).</span></span> <span data-ttu-id="d81ae-128">Dit foutbericht wordt weergegeven wanneer de verkoopregel wordt bijgewerkt.</span><span class="sxs-lookup"><span data-stu-id="d81ae-128">You receive this error message when the sales line is updated.</span></span> 

### <a name="issue-resolution"></a><span data-ttu-id="d81ae-129">Probleemoplossing</span><span class="sxs-lookup"><span data-stu-id="d81ae-129">Issue resolution</span></span>

<span data-ttu-id="d81ae-130">Microsoft heeft dit probleem beoordeeld en heeft vastgesteld dat het een functiebeperking is.</span><span class="sxs-lookup"><span data-stu-id="d81ae-130">Microsoft has evaluated this issue and has determined that it's a feature limitation.</span></span> <span data-ttu-id="d81ae-131">In WMS wordt rechtstreekse levering momenteel niet ondersteund.</span><span class="sxs-lookup"><span data-stu-id="d81ae-131">Currently, WMS doesn't support direct delivery.</span></span> <span data-ttu-id="d81ae-132">Als u rechtstreekse levering wilt gebruiken, moet u dus een niet-WMS artikel en -magazijn selecteren.</span><span class="sxs-lookup"><span data-stu-id="d81ae-132">Therefore, to use direct delivery, you must select a non-WMS item and warehouse.</span></span>
