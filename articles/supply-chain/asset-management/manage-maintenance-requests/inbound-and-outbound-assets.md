---
title: Inkomende en uitgaande activa
description: In dit onderwerp wordt uitgelegd hoe u inkomende en uitgaande activa registreert in Activabeheer.
author: josaw1
manager: tfehr
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetOutboundObjectsListPage, EntAssetOutboundObjectsDeliver, EntAssetInboundObjectsListPage, EntAssetInboundObjectsRecieve
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: e6dfadf6824c6a3df7be9b3b6f3d9f5dd2749e34
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/16/2021
ms.locfileid: "5018066"
---
# <a name="inbound-and-outbound-assets"></a><span data-ttu-id="d90ab-103">Inkomende en uitgaande activa</span><span class="sxs-lookup"><span data-stu-id="d90ab-103">Inbound and outbound assets</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="d90ab-104">Als uw bedrijf reparaties of onderhoudstaken uitvoert aan activa die van andere locaties of klanten worden ontvangen, kan Activabeheer zowel inkomende activa die op weg zijn naar uw bedrijf als uitgaande activa die worden geretourneerd volgen.</span><span class="sxs-lookup"><span data-stu-id="d90ab-104">If your company does repair jobs or maintenance jobs on assets that are received from other locations or customers, Asset Management can track both inbound assets that are on their way to your company and outbound assets that are being returned.</span></span>

> [!NOTE]
> <span data-ttu-id="d90ab-105">Als u de inkomende en uitgaande levenscyclusstatussen wilt gebruiken om de binnenkomende en terugkerende activa te beheren, moet u de levenscyclusstatussen en levenscyclusmodellen voor onderhoudsverzoeken instellen om deze acties te ondersteunen.</span><span class="sxs-lookup"><span data-stu-id="d90ab-105">If you want to use inbound and outbound lifecycle states to manage assets that are coming in and being returned, you must set up maintenance request lifecycle states and lifecycle models to support these actions.</span></span> <span data-ttu-id="d90ab-106">Zie [Onderhoudsaanvragen](../setup-for-maintenance-requests/requests.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="d90ab-106">For more information, see [Maintenance requests](../setup-for-maintenance-requests/requests.md).</span></span>

<span data-ttu-id="d90ab-107">De instellingen van Activabeheer bepalen of u met inkomende en uitgaande activa kunt werken.</span><span class="sxs-lookup"><span data-stu-id="d90ab-107">The setup of Asset Management determines whether you can work with inbound and outbound assets.</span></span>

## <a name="register-assets-as-inbound"></a><span data-ttu-id="d90ab-108">Activa registreren als inkomend</span><span class="sxs-lookup"><span data-stu-id="d90ab-108">Register assets as inbound</span></span>

1. <span data-ttu-id="d90ab-109">Selecteer **Activabeheer** \> **Algemeen** \> **Onderhoudsverzoeken** \> **Actieve onderhoudsverzoeken**.</span><span class="sxs-lookup"><span data-stu-id="d90ab-109">Select **Asset management** \> **Common** \> **Maintenance requests** \> **Active maintenance requests**.</span></span>
2. <span data-ttu-id="d90ab-110">Selecteer het onderhoudsverzoek.</span><span class="sxs-lookup"><span data-stu-id="d90ab-110">Select the maintenance request.</span></span>
3. <span data-ttu-id="d90ab-111">Selecteer **Status van onderhoudsverzoek bijwerken**.</span><span class="sxs-lookup"><span data-stu-id="d90ab-111">Select **Update maintenance request state**.</span></span>
4. <span data-ttu-id="d90ab-112">Selecteer **Inkomend** (of een andere levenscyclusstatus die u hebt gemaakt voor inkomende activa) en selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="d90ab-112">Select **Inbound** (or another lifecycle state that you've created for inbound assets), and then select **OK**.</span></span>

![Activa registreren als inkomend](media/07-manage-maintenance-requests.png)

## <a name="register-inbound-assets-as-received"></a><span data-ttu-id="d90ab-114">Inkomende activa registreren als ontvangen</span><span class="sxs-lookup"><span data-stu-id="d90ab-114">Register inbound assets as received</span></span>

1. <span data-ttu-id="d90ab-115">Selecteer **Activabeheer** \> **Algemeen** \> **Inkomend/uitgaand** \> **Inkomende activa**.</span><span class="sxs-lookup"><span data-stu-id="d90ab-115">Select **Asset management** \> **Common** \> **Inbound/outbound** \> **Inbound assets**.</span></span>
2. <span data-ttu-id="d90ab-116">Selecteer het activum of het onderhoudsverzoek.</span><span class="sxs-lookup"><span data-stu-id="d90ab-116">Select the asset or maintenance request.</span></span>
3. <span data-ttu-id="d90ab-117">Selecteer **Activa ontvangen**.</span><span class="sxs-lookup"><span data-stu-id="d90ab-117">Select **Receive assets**.</span></span>
4. <span data-ttu-id="d90ab-118">Voer de datum en de tijd in het veld **Ontvangen** in.</span><span class="sxs-lookup"><span data-stu-id="d90ab-118">In the **Received** field, enter the date and time.</span></span> <span data-ttu-id="d90ab-119">Selecteer vervolgens **OK**.</span><span class="sxs-lookup"><span data-stu-id="d90ab-119">Then select **OK**.</span></span> <span data-ttu-id="d90ab-120">De record wordt verwijderd uit de pagina met de lijst **Inkomende activa**.</span><span class="sxs-lookup"><span data-stu-id="d90ab-120">The record is removed from the **Inbound assets** list page.</span></span>

![Inkomende activa registreren als ontvangen](media/08-manage-maintenance-requests.png)

## <a name="register-assets-as-outbound"></a><span data-ttu-id="d90ab-122">Activa registreren als uitgaand</span><span class="sxs-lookup"><span data-stu-id="d90ab-122">Register assets as outbound</span></span>

<span data-ttu-id="d90ab-123">Wanneer u de onderhouds- of reparatietaak hebt voltooid, kunt u het activum als geretourneerd registreren.</span><span class="sxs-lookup"><span data-stu-id="d90ab-123">When you've completed the maintenance or repair job, you can register the asset as returned.</span></span>

1. <span data-ttu-id="d90ab-124">Selecteer **Activabeheer** \> **Algemeen** \> **Onderhoudsverzoeken** \> **Actieve onderhoudsverzoeken**.</span><span class="sxs-lookup"><span data-stu-id="d90ab-124">Select **Asset management** \> **Common** \> **Maintenance requests** \> **Active maintenance requests**.</span></span>
2. <span data-ttu-id="d90ab-125">Selecteer het onderhoudsverzoek.</span><span class="sxs-lookup"><span data-stu-id="d90ab-125">Select the maintenance request.</span></span>
3. <span data-ttu-id="d90ab-126">Selecteer **Status van onderhoudsverzoek bijwerken**.</span><span class="sxs-lookup"><span data-stu-id="d90ab-126">Select **Update maintenance request state**.</span></span>
4. <span data-ttu-id="d90ab-127">Selecteer **Uitgaand** (of een andere levenscyclusstatus die u hebt gemaakt voor uitgaande activa) en selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="d90ab-127">Select **Outbound** (or another lifecycle state that you've created for outbound assets), and then select **OK**.</span></span>

## <a name="register-outbound-assets-as-delivered"></a><span data-ttu-id="d90ab-128">Uitgaande activa registreren als afgeleverd</span><span class="sxs-lookup"><span data-stu-id="d90ab-128">Register outbound assets as delivered</span></span>

1. <span data-ttu-id="d90ab-129">Selecteer **Activabeheer** \> **Algemeen** \> **Inkomend/uitgaand** \> **Uitgaande activa**.</span><span class="sxs-lookup"><span data-stu-id="d90ab-129">Select **Asset management** \> **Common** \> **Inbound/outbound** \> **Outbound assets**.</span></span>
2. <span data-ttu-id="d90ab-130">Selecteer het activum of het onderhoudsverzoek.</span><span class="sxs-lookup"><span data-stu-id="d90ab-130">Select the asset or maintenance request.</span></span>
3. <span data-ttu-id="d90ab-131">Selecteer **Activa afleveren**.</span><span class="sxs-lookup"><span data-stu-id="d90ab-131">Select **Deliver assets**.</span></span>
4. <span data-ttu-id="d90ab-132">Voer de datum en de tijd in het veld **Afgeleverd** in.</span><span class="sxs-lookup"><span data-stu-id="d90ab-132">In the **Delivered** field, enter the date and time.</span></span> <span data-ttu-id="d90ab-133">Selecteer vervolgens **OK**.</span><span class="sxs-lookup"><span data-stu-id="d90ab-133">Then select **OK**.</span></span> <span data-ttu-id="d90ab-134">De record wordt verwijderd uit de pagina met de lijst **Uitgaande activa**.</span><span class="sxs-lookup"><span data-stu-id="d90ab-134">The record is removed from the **Outbound assets** list page.</span></span>
