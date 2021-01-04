---
title: Een leasegroep maken
description: In dit onderwerp wordt uitgelegd hoe u leasegroepen instelt. Leasegroepen zijn vereist om nieuwe leases te maken.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: f8512a59d0e9935090f97a0f0237bfefc8473955
ms.sourcegitcommit: aeee39c01d3f93a6dfcf2013965fa975a740596a
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/28/2020
ms.locfileid: "4442162"
---
# <a name="create-a-lease-group"></a><span data-ttu-id="81478-104">Een leasegroep maken</span><span class="sxs-lookup"><span data-stu-id="81478-104">Create a lease group</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="81478-105">In dit onderwerp wordt uitgelegd hoe u leasegroepen instelt.</span><span class="sxs-lookup"><span data-stu-id="81478-105">This topic explains how to set up lease groups.</span></span> <span data-ttu-id="81478-106">Leasegroepen zijn vereist om nieuwe leases te maken.</span><span class="sxs-lookup"><span data-stu-id="81478-106">Lease groups are required to create new leases.</span></span> <span data-ttu-id="81478-107">Aan elke leasegroep zijn leaseboeken gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="81478-107">Lease books are associated with each lease group.</span></span> <span data-ttu-id="81478-108">Leaseboeken bepalen de standaardboeken die voor elke lease moeten worden gemaakt.</span><span class="sxs-lookup"><span data-stu-id="81478-108">Lease books determine the default books that must be created for each lease.</span></span> <span data-ttu-id="81478-109">U kunt specifieke rekeningen aan een leasegroep toewijzen op de pagina **Leaseboekingsparameters**.</span><span class="sxs-lookup"><span data-stu-id="81478-109">You can assign specific accounts to a lease group on the **Lease posting parameters** page.</span></span>

## <a name="create-a-lease-book-and-add-a-lease-group"></a><span data-ttu-id="81478-110">Een leaseboek maken en een leasegroep toevoegen</span><span class="sxs-lookup"><span data-stu-id="81478-110">Create a lease book and add a lease group</span></span>

1. <span data-ttu-id="81478-111">Ga naar **Activa leasen \> Instellen \> Leasegroepen**.</span><span class="sxs-lookup"><span data-stu-id="81478-111">Go to **Asset leasing \> Setup \> Lease groups**.</span></span>
2. <span data-ttu-id="81478-112">Selecteer **Nieuw** in het actievenster om een leasegroep toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="81478-112">On the Action Pane, select **New** to add a lease group.</span></span> <span data-ttu-id="81478-113">Er wordt een regel aan het raster toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="81478-113">A line is added to the grid.</span></span>
3. <span data-ttu-id="81478-114">Voer op de nieuwe regel in het veld **Leasegroep** een waarde in.</span><span class="sxs-lookup"><span data-stu-id="81478-114">On the new line, in the **Lease group** field, enter a value.</span></span>
4. <span data-ttu-id="81478-115">Voer een waarde in het veld **Beschrijving** in.</span><span class="sxs-lookup"><span data-stu-id="81478-115">In the **Description** field, enter a value.</span></span>

<span data-ttu-id="81478-116">De informatie die u zojuist hebt ingevoerd, wordt toegevoegd aan het veld **Leasegroep** op de pagina **Lease toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="81478-116">The information that you just entered is added to the **Lease group** field on the **Add lease** page.</span></span>

## <a name="associate-a-book-with-a-lease-group"></a><span data-ttu-id="81478-117">Een boek aan een leasegroep koppelen</span><span class="sxs-lookup"><span data-stu-id="81478-117">Associate a book with a lease group</span></span>

<span data-ttu-id="81478-118">Nadat u leasegroepen hebt gemaakt, kunt u boeken aan elke groep toewijzen.</span><span class="sxs-lookup"><span data-stu-id="81478-118">After you create lease groups, you can assign books to each group.</span></span> <span data-ttu-id="81478-119">Wanneer u een lease maakt en deze aan een leasegroep toewijst, maakt het systeem een set schema's voor elk boek dat aan die leasegroep is gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="81478-119">When you create a lease and assign it to a lease group, the system creates a set of schedules for each book that is associated with that lease group.</span></span>

> [!NOTE]
> <span data-ttu-id="81478-120">Boeken moeten worden ingesteld voordat ze aan een leasegroep kunnen worden toegewezen.</span><span class="sxs-lookup"><span data-stu-id="81478-120">Books must be set up before they can be assigned to a lease group.</span></span>

1. <span data-ttu-id="81478-121">Ga naar **Activa leasen \> Instellen \> Leasegroep**.</span><span class="sxs-lookup"><span data-stu-id="81478-121">Go to **Asset leasing \> Setup \> Lease group**.</span></span>
2. <span data-ttu-id="81478-122">Selecteer een leasegroep en selecteer vervolgens **Boeken**.</span><span class="sxs-lookup"><span data-stu-id="81478-122">Select a lease group, and then select **Books**.</span></span>
3. <span data-ttu-id="81478-123">Selecteer **Nieuw** en selecteer vervolgens in het veld **Boektype** het boek dat u wilt toewijzen aan de leasegroep.</span><span class="sxs-lookup"><span data-stu-id="81478-123">Select **New**, and then, in the **Book type** field, select the book to assign to the lease group.</span></span> <span data-ttu-id="81478-124">U kunt meerdere boeken aan een leasegroep toewijzen als een lease op verschillende manieren moet worden verwerkt.</span><span class="sxs-lookup"><span data-stu-id="81478-124">You can assign multiple books to a lease group if a lease must be accounted for in different ways.</span></span>
