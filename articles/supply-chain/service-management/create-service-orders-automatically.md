---
title: Automatisch serviceorders maken
description: U kunt serviceorders maken voor één serviceovereenkomst of voor meerdere serviceovereenkomsten.
author: ShylaThompson
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7d91ccc6a3ebaff220c8a876944b90d910399660
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/18/2019
ms.locfileid: "2814024"
---
# <a name="create-service-orders-automatically"></a><span data-ttu-id="02e2d-103">Automatisch serviceorders maken</span><span class="sxs-lookup"><span data-stu-id="02e2d-103">Create service orders automatically</span></span>    

[!include [banner](../includes/banner.md)]


<span data-ttu-id="02e2d-104">U kunt serviceorders maken voor één serviceovereenkomst of voor meerdere serviceovereenkomsten.</span><span class="sxs-lookup"><span data-stu-id="02e2d-104">You can create service orders for one service agreement or for several service agreements.</span></span> <span data-ttu-id="02e2d-105">Wanneer deze zijn gemaakt, kunt u uw serviceorders weergeven in het formulier **Serviceorders**.</span><span class="sxs-lookup"><span data-stu-id="02e2d-105">When they are created, you can view your service orders in the **Service orders** form.</span></span>

<span data-ttu-id="02e2d-106">Serviceorders worden alleen gemaakt voor de geldige periode van de serviceovereenkomst.</span><span class="sxs-lookup"><span data-stu-id="02e2d-106">Service orders are created only for the valid period of the service agreement.</span></span> <span data-ttu-id="02e2d-107">Als het interval dat u opgeeft in het dialoogvenster **Serviceorders maken**, vóór de begindatum of na de einddatum van de serviceovereenkomst valt, worden alleen serviceorders gemaakt voor dat deel van het interval dat binnen de datums van de serviceovereenkomst valt.</span><span class="sxs-lookup"><span data-stu-id="02e2d-107">If the interval that you specify in the **Create service orders** form is before the starting date or after the ending date of the service agreement, service orders are created only for the part of the interval that is within the service agreement dates.</span></span>

<span data-ttu-id="02e2d-108">Wanneer u handmatig of automatisch serviceorders maakt vanaf de serviceovereenkomstregel, moet de serviceorder binnen het interval vallen dat met de begindatum en de einddatum voor de regel is ingesteld, tenzij u op de regel geen einddatum hebt ingesteld.</span><span class="sxs-lookup"><span data-stu-id="02e2d-108">When you create service orders manually or automatically from the service agreement line, the service order must be in the time interval that is defined by the starting and ending dates for the line, unless you do not specify an ending date on the line.</span></span>

## <a name="create-service-orders-automatically-for-a-service-agreement"></a><span data-ttu-id="02e2d-109">Automatisch serviceorders maken voor een serviceovereenkomst</span><span class="sxs-lookup"><span data-stu-id="02e2d-109">Create service orders automatically for a service agreement</span></span>

1.  <span data-ttu-id="02e2d-110">Klik op **Servicebeheer** \> **Algemeen** \> **Serviceovereenkomsten** \> **Serviceovereenkomsten**.</span><span class="sxs-lookup"><span data-stu-id="02e2d-110">Click **Service management** \> **Common** \> **Service agreements** \> **Service agreements**.</span></span>

2.  <span data-ttu-id="02e2d-111">Selecteer een serviceovereenkomst.</span><span class="sxs-lookup"><span data-stu-id="02e2d-111">Select a service agreement.</span></span>

3.  <span data-ttu-id="02e2d-112">Klik op het tabblad **Leveren** en klik vervolgens op **Geplande serviceorders**.</span><span class="sxs-lookup"><span data-stu-id="02e2d-112">Click the **Deliver** tab, and then click **Planned service orders**.</span></span>

4.  <span data-ttu-id="02e2d-113">Geef datums op in de velden **Datum vanaf** en **Datum t/m** om de serviceperiode te definiëren.</span><span class="sxs-lookup"><span data-stu-id="02e2d-113">Specify dates in the **From date** and **To date** fields to define the service period.</span></span>

5.  <span data-ttu-id="02e2d-114">Schakel het selectievakje **Infologboek weergeven** in om een lijst weer te geven van de serviceorders die zijn gemaakt.</span><span class="sxs-lookup"><span data-stu-id="02e2d-114">Select the **Show Infolog** check box to display a list of the service orders that are created.</span></span>

6.  <span data-ttu-id="02e2d-115">Selecteer transactietypen in de veldgroep **Transactietypen opnemen**.</span><span class="sxs-lookup"><span data-stu-id="02e2d-115">Select transaction types in the **Include transaction types** field group.</span></span> <span data-ttu-id="02e2d-116">De transactietypen vertegenwoordigen de regels die zijn gemaakt in de serviceovereenkomst en elk transactietype dat u selecteert, genereert verscheidene serviceorders, afhankelijk van de service-interval die is opgegeven op de serviceovereenkomstregel.</span><span class="sxs-lookup"><span data-stu-id="02e2d-116">The transaction types represent the lines that are created in the service agreement, and each transaction type that you select generates several service orders, depending on the service interval that is specified on the service agreement line.</span></span>

7.  <span data-ttu-id="02e2d-117">Schakel het selectievakje **Continu** in om eventuele ontbrekende serviceorders in een continue serie van serviceorders te maken.</span><span class="sxs-lookup"><span data-stu-id="02e2d-117">To create any service orders that are missing from continuous series of service orders, select the **Continuous** check box.</span></span>

8.  <span data-ttu-id="02e2d-118">Klik tot slot op **OK**.</span><span class="sxs-lookup"><span data-stu-id="02e2d-118">Click **OK**.</span></span>

## <a name="create-service-orders-automatically-for-several-service-agreements"></a><span data-ttu-id="02e2d-119">Automatisch serviceorders maken voor meerdere serviceovereenkomsten</span><span class="sxs-lookup"><span data-stu-id="02e2d-119">Create service orders automatically for several service agreements</span></span>

1.  <span data-ttu-id="02e2d-120">Klik op **Servicebeheer** \> **Periodiek** \> **Serviceorders** \> **Serviceorders maken**.</span><span class="sxs-lookup"><span data-stu-id="02e2d-120">Click **Service management** \> **Periodic** \> **Service orders** \> **Create service orders**.</span></span>

2.  <span data-ttu-id="02e2d-121">Klik op **Selecteren** om criteria voor het maken van serviceorders te selecteren en toe te voegen of te verwijderen.</span><span class="sxs-lookup"><span data-stu-id="02e2d-121">Click **Select** to make selections to add or remove criteria to use to create service orders.</span></span>

3.  <span data-ttu-id="02e2d-122">Klik op **OK**.</span><span class="sxs-lookup"><span data-stu-id="02e2d-122">Click **OK**.</span></span>

## <a name="see-also"></a><span data-ttu-id="02e2d-123">Zie ook</span><span class="sxs-lookup"><span data-stu-id="02e2d-123">See also</span></span>

[<span data-ttu-id="02e2d-124">Serviceorders</span><span class="sxs-lookup"><span data-stu-id="02e2d-124">Service orders</span></span>](service-orders.md)

[<span data-ttu-id="02e2d-125">Automatisch serviceorders maken</span><span class="sxs-lookup"><span data-stu-id="02e2d-125">Automatically create service orders</span></span>](auto-create-service-orders.md)

  


