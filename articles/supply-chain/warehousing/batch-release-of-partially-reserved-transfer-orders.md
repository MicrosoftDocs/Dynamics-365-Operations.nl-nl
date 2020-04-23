---
title: Batchvrijgave van gedeeltelijk gereserveerde transferorders
description: In dit onderwerp wordt beschreven hoe u de batchvrijgave van gedeeltelijk gereserveerde transferorders vanaf een mobiel apparaat instelt en toepast.
author: pjacobse
manager: tfehr
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLoadPlanningWorkbench
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: pjacobse
ms.search.validFrom: 2017-09-20
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f0707731caaf9b4852e3c19be899ad92f5b84e29
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/02/2020
ms.locfileid: "3201290"
---
# <a name="batch-release-of-partially-reserved-transfer-orders"></a><span data-ttu-id="74ce1-103">Batchvrijgave van gedeeltelijk gereserveerde transferorders</span><span class="sxs-lookup"><span data-stu-id="74ce1-103">Batch release of partially reserved transfer orders</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="74ce1-104">Met de functionaliteit voor batchvrijgave van gedeeltelijk gereserveerde transferorders kunt u transferorders met een batchtaak gedeeltelijk vrijgeven aan een magazijn.</span><span class="sxs-lookup"><span data-stu-id="74ce1-104">The functionality for batch release of partially reserved transfer orders lets you partially release transfer orders to a warehouse by using a batch job.</span></span>
<span data-ttu-id="74ce1-105">Omdat u een gedeeltelijke hoeveelheid kunt vrijgeven, hoeft u niet te wachten tot de hele orderhoeveelheid in het magazijn beschikbaar is voordat u een order vrijgeeft.</span><span class="sxs-lookup"><span data-stu-id="74ce1-105">Because you have the option to release a partial quantity, you don’t have to wait for the whole order quantity to be available in the warehouse before you release an order.</span></span>

<span data-ttu-id="74ce1-106">De vrijgave van orders aan een magazijn is een geavanceerd magazijnbeheerproces.</span><span class="sxs-lookup"><span data-stu-id="74ce1-106">The release of orders to a warehouse is an advanced warehouse management process.</span></span> <span data-ttu-id="74ce1-107">Dit proces omvat activiteiten, zoals orderverzamelen, verpakken en verzenden, die een magazijnmedewerker kan uitvoeren via een mobiel apparaat.</span><span class="sxs-lookup"><span data-stu-id="74ce1-107">This process involves activities, such as picking, packing, and shipping, that a warehouse worker can perform by using a mobile device.</span></span>

## <a name="where-it-applies"></a><span data-ttu-id="74ce1-108">Waar van toepassing</span><span class="sxs-lookup"><span data-stu-id="74ce1-108">Where it applies</span></span>

<span data-ttu-id="74ce1-109">Voor deze functionaliteit worden transferorders met een batchtaak vrijgegeven aan een magazijn.</span><span class="sxs-lookup"><span data-stu-id="74ce1-109">For this functionality, transfer orders are released to a warehouse by using a batch job.</span></span> <span data-ttu-id="74ce1-110">Deze functie is handig wanneer u niet voldoende voorraad in het magazijn hebt, maar nog steeds artikelen van het ene naar het andere magazijn wilt overbrengen.</span><span class="sxs-lookup"><span data-stu-id="74ce1-110">This functionality is useful when you don’t have enough inventory in the warehouse, but you still want to transfer items from one warehouse to another.</span></span>

## <a name="how-it-is-set-up"></a><span data-ttu-id="74ce1-111">De instelling</span><span class="sxs-lookup"><span data-stu-id="74ce1-111">How it is set up</span></span>

### <a name="specify-fulfillment-criteria-for-transfer-orders-and-sales-orders"></a><span data-ttu-id="74ce1-112">Uitvoeringscriteria opgeven voor transfer- en verkooporders</span><span class="sxs-lookup"><span data-stu-id="74ce1-112">Specify fulfillment criteria for transfer orders and sales orders</span></span>

<span data-ttu-id="74ce1-113">Voordat een order gedeeltelijk kan worden vrijgegeven aan een magazijn in een batch, moet aan de uitvoeringscriteria worden voldaan.</span><span class="sxs-lookup"><span data-stu-id="74ce1-113">Before an order can be partially released to a warehouse in a batch, the fulfillment criteria must be met.</span></span> <span data-ttu-id="74ce1-114">Deze uitvoeringscriteria worden bepaald door het uitvoeringsbeleid.</span><span class="sxs-lookup"><span data-stu-id="74ce1-114">These fulfillment criteria are determined by the fulfillment policy.</span></span>

<span data-ttu-id="74ce1-115">Uitvoeringsbeleid voor transferorders en verkooporders wordt opgegeven op bedrijfsniveau.</span><span class="sxs-lookup"><span data-stu-id="74ce1-115">Fulfillment policies for transfer orders and sales orders are specified at the company level.</span></span> <span data-ttu-id="74ce1-116">Afhankelijk van de instellingen van het uitvoeringsbeleid, wordt de vrijgave van orders in een batch goedgekeurd of afgekeurd.</span><span class="sxs-lookup"><span data-stu-id="74ce1-116">Depending on the setup of the fulfillment policy, the release of orders in a batch will be accepted or rejected.</span></span> <span data-ttu-id="74ce1-117">De orders worden vervolgens dienovereenkomstig verwerkt.</span><span class="sxs-lookup"><span data-stu-id="74ce1-117">The orders will then be processed accordingly.</span></span>

-   <span data-ttu-id="74ce1-118">Als u uitvoeringsbeleid wilt maken voor transfer- en verkooporders, klikt u op **Magazijnbeheer** \> **Instellingen** \> **Vrijgave naar magazijn** \> **Uitvoeringsbeleid** en maakt u een uitvoeringsbeleid door een naam en een omschrijving in te voeren.</span><span class="sxs-lookup"><span data-stu-id="74ce1-118">To create fulfillment policies for transfer orders and sales orders, click **Warehouse management** \> **Setup** \> **Release to warehouse** \> **Fulfillment policy**, and then create a fulfillment policy by entering a name and a description.</span></span>

-   <span data-ttu-id="74ce1-119">Als u een uitvoeringsverhouding, een waardetype en een bericht wilt opgeven dat moet worden weergegeven als het uitvoeringsbeleid wordt geschonden, klikt u op **Magazijnbeheer** \> **Instellingen** \> **Vrijgave naar magazijn** \> **Uitvoeringsbeleid** en stelt u de velden **Uitvoeringsverhouding**, **Waardetype** en **Berichten uitvoeringschending** in.</span><span class="sxs-lookup"><span data-stu-id="74ce1-119">To specify a fulfillment rate, a value type, and the message that is shown if the fulfillment policy is violated, click **Warehouse management** \> **Setup** \> **Release to warehouse** \> **Fulfillment policy**, and then set the **Fulfillment rate**, **Value type**, and **Fulfillment violation message** fields.</span></span>

### <a name="set-the-fulfillment-policies-for-transfer-orders-and-sales-orders"></a><span data-ttu-id="74ce1-120">Het uitvoeringsbeleid opgeven voor transfer- en verkooporders</span><span class="sxs-lookup"><span data-stu-id="74ce1-120">Set the fulfillment policies for transfer orders and sales orders</span></span>

-   <span data-ttu-id="74ce1-121">Als u het uitvoeringsbeleid voor transferorders wilt instellen, klikt u op **Voorraadbeheer** \> **Instellingen** \> **Parameters voor voorraad- en magazijnbeheer** \> **Transferorders** \> **Magazijnbeheer** en selecteert u een uitvoeringsbeleid voor transferorders.</span><span class="sxs-lookup"><span data-stu-id="74ce1-121">To set the fulfillment policies for transfer orders, click **Inventory management** \> **Setup** \> **Inventory and warehouse management parameters** \> **Transfer orders** \> **Warehouse management**, and then select a transfer order fulfillment policy.</span></span>

-   <span data-ttu-id="74ce1-122">Als u het uitvoeringsbeleid voor verkooporders wilt instellen, klikt u op **Klanten** \> **Instellingen** \> **Parameters van module Klanten** \> **Magazijnbeheer** en selecteert u een uitvoeringsbeleid voor verkooporders.</span><span class="sxs-lookup"><span data-stu-id="74ce1-122">To set the fulfillment policies for sales orders, click **Accounts receivable** \> **Setup** \> **Accounts receivable parameters** \> **Warehouse management**, and then select a sales order fulfillment policy.</span></span>

## <a name="allow-release-in-a-batch-and-specify-the-quantity-that-should-be-release-in-a-batch"></a><span data-ttu-id="74ce1-123">Vrijgave in een batch toestaan en de hoeveelheid opgeven die in een batch moet worden vrijgegeven</span><span class="sxs-lookup"><span data-stu-id="74ce1-123">Allow release in a batch and specify the quantity that should be release in a batch</span></span>

<span data-ttu-id="74ce1-124">Een batchtaak wordt gebruikt voor het vrijgeven van orders naar een magazijn in een batch.</span><span class="sxs-lookup"><span data-stu-id="74ce1-124">A batch job is used to release orders to a warehouse in a batch.</span></span> <span data-ttu-id="74ce1-125">De parameters waarmee onderscheid wordt gemaakt tussen de orders die moeten worden uitgevoerd in een batchtaak, worden ingesteld voor de batchtaak zelf.</span><span class="sxs-lookup"><span data-stu-id="74ce1-125">The parameters that distinguish the orders that should be run in a batch job are set on the batch job itself.</span></span>

<span data-ttu-id="74ce1-126">De parameter **Hoeveelheid** bepaalt of de gehele hoeveelheid of de fysiek gereserveerde hoeveelheid in de batch moet worden vrijgegeven.</span><span class="sxs-lookup"><span data-stu-id="74ce1-126">The **Quantity** parameter specifies whether the whole quantity or the physically reserved quantity should be released in the batch.</span></span> <span data-ttu-id="74ce1-127">De parameter **Vrijgave van gedeeltelijk vrijgegeven orders toestaan** bepaalt of orders in de batch moeten worden geaccepteerd of afgewezen als ze eerder gedeeltelijk zijn vrijgegeven.</span><span class="sxs-lookup"><span data-stu-id="74ce1-127">The **Allow release of partially released orders** parameter determines whether orders in the batch should be accepted or rejected if they were partially released earlier.</span></span>

-   <span data-ttu-id="74ce1-128">Als u de parameters **Hoeveelheid** en **Vrijgave van gedeeltelijk vrijgegeven orders toestaan** wilt instellen voor transferorders, klikt u op **Magazijnbeheer** \> **Vrijgave naar magazijn** \> **Transferorders automatisch vrijgeven**.</span><span class="sxs-lookup"><span data-stu-id="74ce1-128">To set the **Quantity** and **Allow release of partially released orders** parameters for transfer orders, click **Warehouse management** \> **Release to warehouse** \> **Automatic release of transfer orders**.</span></span>

-   <span data-ttu-id="74ce1-129">Als u de parameters **Hoeveelheid** en **Vrijgave van gedeeltelijk vrijgegeven orders toestaan** wilt instellen voor verkooporders, klikt u op **Magazijnbeheer** \> **Vrijgave naar magazijn** \> **Verkooporders automatisch vrijgeven**.</span><span class="sxs-lookup"><span data-stu-id="74ce1-129">To set the **Quantity** and **Allow release of partially released orders** parameters for sales orders, click **Warehouse management** \> **Release to warehouse** \> **Automatic release of sales orders**.</span></span>
