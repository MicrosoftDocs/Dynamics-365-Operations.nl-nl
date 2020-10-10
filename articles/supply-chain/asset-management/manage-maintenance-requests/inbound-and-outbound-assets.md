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
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: a7239bf5f8e53e61c4259abbcbf2ff740f4cef55
ms.sourcegitcommit: c986d5234b81d31cc6d054298be6f6ec92c1754c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/25/2020
ms.locfileid: "3889932"
---
# <a name="inbound-and-outbound-assets"></a><span data-ttu-id="4d0fd-103">Inkomende en uitgaande activa</span><span class="sxs-lookup"><span data-stu-id="4d0fd-103">Inbound and outbound assets</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="4d0fd-104">Als uw bedrijf reparaties of onderhoudstaken uitvoert aan activa die van andere locaties of klanten worden ontvangen, kan Activabeheer zowel inkomende activa die op weg zijn naar uw bedrijf als uitgaande activa die worden geretourneerd volgen.</span><span class="sxs-lookup"><span data-stu-id="4d0fd-104">If your company does repair jobs or maintenance jobs on assets that are received from other locations or customers, Asset Management can track both inbound assets that are on their way to your company and outbound assets that are being returned.</span></span>

> [!NOTE]
> <span data-ttu-id="4d0fd-105">Als u de inkomende en uitgaande levenscyclusstatussen wilt gebruiken om de binnenkomende en terugkerende activa te beheren, moet u de levenscyclusstatussen en levenscyclusmodellen voor onderhoudsverzoeken instellen om deze acties te ondersteunen.</span><span class="sxs-lookup"><span data-stu-id="4d0fd-105">If you want to use inbound and outbound lifecycle states to manage assets that are coming in and being returned, you must set up maintenance request lifecycle states and lifecycle models to support these actions.</span></span> <span data-ttu-id="4d0fd-106">Zie [Onderhoudsaanvragen](../setup-for-maintenance-requests/requests.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="4d0fd-106">For more information, see [Maintenance requests](../setup-for-maintenance-requests/requests.md).</span></span>

<span data-ttu-id="4d0fd-107">De instellingen van Activabeheer bepalen of u met inkomende en uitgaande activa kunt werken.</span><span class="sxs-lookup"><span data-stu-id="4d0fd-107">The setup of Asset Management determines whether you can work with inbound and outbound assets.</span></span>

## <a name="register-assets-as-inbound"></a><span data-ttu-id="4d0fd-108">Activa registreren als inkomend</span><span class="sxs-lookup"><span data-stu-id="4d0fd-108">Register assets as inbound</span></span>

1. <span data-ttu-id="4d0fd-109">Selecteer **Activabeheer** \> **Algemeen** \> **Onderhoudsverzoeken** \> **Actieve onderhoudsverzoeken**.</span><span class="sxs-lookup"><span data-stu-id="4d0fd-109">Select **Asset management** \> **Common** \> **Maintenance requests** \> **Active maintenance requests**.</span></span>
2. <span data-ttu-id="4d0fd-110">Selecteer het onderhoudsverzoek.</span><span class="sxs-lookup"><span data-stu-id="4d0fd-110">Select the maintenance request.</span></span>
3. <span data-ttu-id="4d0fd-111">Selecteer **Status van onderhoudsverzoek bijwerken**.</span><span class="sxs-lookup"><span data-stu-id="4d0fd-111">Select **Update maintenance request state**.</span></span>
4. <span data-ttu-id="4d0fd-112">Selecteer **Inkomend** (of een andere levenscyclusstatus die u hebt gemaakt voor inkomende activa) en selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="4d0fd-112">Select **Inbound** (or another lifecycle state that you've created for inbound assets), and then select **OK**.</span></span>

![Activa registreren als inkomend](media/07-manage-maintenance-requests.png)

## <a name="register-inbound-assets-as-received"></a><span data-ttu-id="4d0fd-114">Inkomende activa registreren als ontvangen</span><span class="sxs-lookup"><span data-stu-id="4d0fd-114">Register inbound assets as received</span></span>

1. <span data-ttu-id="4d0fd-115">Selecteer **Activabeheer** \> **Algemeen** \> **Inkomend/uitgaand** \> **Inkomende activa**.</span><span class="sxs-lookup"><span data-stu-id="4d0fd-115">Select **Asset management** \> **Common** \> **Inbound/outbound** \> **Inbound assets**.</span></span>
2. <span data-ttu-id="4d0fd-116">Selecteer het activum of het onderhoudsverzoek.</span><span class="sxs-lookup"><span data-stu-id="4d0fd-116">Select the asset or maintenance request.</span></span>
3. <span data-ttu-id="4d0fd-117">Selecteer **Activa ontvangen**.</span><span class="sxs-lookup"><span data-stu-id="4d0fd-117">Select **Receive assets**.</span></span>
4. <span data-ttu-id="4d0fd-118">Voer de datum en de tijd in het veld **Ontvangen** in.</span><span class="sxs-lookup"><span data-stu-id="4d0fd-118">In the **Received** field, enter the date and time.</span></span> <span data-ttu-id="4d0fd-119">Selecteer vervolgens **OK**.</span><span class="sxs-lookup"><span data-stu-id="4d0fd-119">Then select **OK**.</span></span> <span data-ttu-id="4d0fd-120">De record wordt verwijderd uit de pagina met de lijst **Inkomende activa**.</span><span class="sxs-lookup"><span data-stu-id="4d0fd-120">The record is removed from the **Inbound assets** list page.</span></span>

![Inkomende activa registreren als ontvangen](media/08-manage-maintenance-requests.png)

## <a name="register-assets-as-outbound"></a><span data-ttu-id="4d0fd-122">Activa registreren als uitgaand</span><span class="sxs-lookup"><span data-stu-id="4d0fd-122">Register assets as outbound</span></span>

<span data-ttu-id="4d0fd-123">Wanneer u de onderhouds- of reparatietaak hebt voltooid, kunt u het activum als geretourneerd registreren.</span><span class="sxs-lookup"><span data-stu-id="4d0fd-123">When you've completed the maintenance or repair job, you can register the asset as returned.</span></span>

1. <span data-ttu-id="4d0fd-124">Selecteer **Activabeheer** \> **Algemeen** \> **Onderhoudsverzoeken** \> **Actieve onderhoudsverzoeken**.</span><span class="sxs-lookup"><span data-stu-id="4d0fd-124">Select **Asset management** \> **Common** \> **Maintenance requests** \> **Active maintenance requests**.</span></span>
2. <span data-ttu-id="4d0fd-125">Selecteer het onderhoudsverzoek.</span><span class="sxs-lookup"><span data-stu-id="4d0fd-125">Select the maintenance request.</span></span>
3. <span data-ttu-id="4d0fd-126">Selecteer **Status van onderhoudsverzoek bijwerken**.</span><span class="sxs-lookup"><span data-stu-id="4d0fd-126">Select **Update maintenance request state**.</span></span>
4. <span data-ttu-id="4d0fd-127">Selecteer **Uitgaand** (of een andere levenscyclusstatus die u hebt gemaakt voor uitgaande activa) en selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="4d0fd-127">Select **Outbound** (or another lifecycle state that you've created for outbound assets), and then select **OK**.</span></span>

## <a name="register-outbound-assets-as-delivered"></a><span data-ttu-id="4d0fd-128">Uitgaande activa registreren als afgeleverd</span><span class="sxs-lookup"><span data-stu-id="4d0fd-128">Register outbound assets as delivered</span></span>

1. <span data-ttu-id="4d0fd-129">Selecteer **Activabeheer** \> **Algemeen** \> **Inkomend/uitgaand** \> **Uitgaande activa**.</span><span class="sxs-lookup"><span data-stu-id="4d0fd-129">Select **Asset management** \> **Common** \> **Inbound/outbound** \> **Outbound assets**.</span></span>
2. <span data-ttu-id="4d0fd-130">Selecteer het activum of het onderhoudsverzoek.</span><span class="sxs-lookup"><span data-stu-id="4d0fd-130">Select the asset or maintenance request.</span></span>
3. <span data-ttu-id="4d0fd-131">Selecteer **Activa afleveren**.</span><span class="sxs-lookup"><span data-stu-id="4d0fd-131">Select **Deliver assets**.</span></span>
4. <span data-ttu-id="4d0fd-132">Voer de datum en de tijd in het veld **Afgeleverd** in.</span><span class="sxs-lookup"><span data-stu-id="4d0fd-132">In the **Delivered** field, enter the date and time.</span></span> <span data-ttu-id="4d0fd-133">Selecteer vervolgens **OK**.</span><span class="sxs-lookup"><span data-stu-id="4d0fd-133">Then select **OK**.</span></span> <span data-ttu-id="4d0fd-134">De record wordt verwijderd uit de pagina met de lijst **Uitgaande activa**.</span><span class="sxs-lookup"><span data-stu-id="4d0fd-134">The record is removed from the **Outbound assets** list page.</span></span>
