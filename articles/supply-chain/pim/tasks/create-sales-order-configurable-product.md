--- 
title: Een verkooporder voor een configureerbaar product maken
description: Deze procedure laat zien hoe u een configuratiesjabloon toepast op een product in een verkooporder.
author: YuyuScheller
manager: AnnBe
ms.date: 10/12/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: e9b42a7343dacc1bcd995c10a4b90a87998a31ba
ms.contentlocale: nl-nl
ms.lasthandoff: 05/08/2018

---
# <a name="create-a-sales-order-for-a-configurable-product"></a><span data-ttu-id="f087e-103">Een verkooporder voor een configureerbaar product maken</span><span class="sxs-lookup"><span data-stu-id="f087e-103">Create a sales order for a configurable product</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f087e-104">Deze procedure laat zien hoe u een configuratiesjabloon toepast op een product in een verkooporder.</span><span class="sxs-lookup"><span data-stu-id="f087e-104">This procedure shows how to apply a configuration template to a product on a sales order.</span></span> <span data-ttu-id="f087e-105">In dit voorbeeld wordt het model D0006-luidspreker gebruikt in het demobedrijf USMF.</span><span class="sxs-lookup"><span data-stu-id="f087e-105">This example uses the D0006 speaker model in the USMF demo data company.</span></span> <span data-ttu-id="f087e-106">Gewoonlijk gebruikt een verkooporderbewerker deze procedure.</span><span class="sxs-lookup"><span data-stu-id="f087e-106">Typically, a sales order processor uses this procedure.</span></span>


## <a name="create-a-sales-order"></a><span data-ttu-id="f087e-107">Verkooporder maken</span><span class="sxs-lookup"><span data-stu-id="f087e-107">Create a sales order</span></span>
1. <span data-ttu-id="f087e-108">Klik op Verkooporderverwerking en -onderzoek.</span><span class="sxs-lookup"><span data-stu-id="f087e-108">Click Sales order processing and inquiry.</span></span>
2. <span data-ttu-id="f087e-109">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="f087e-109">Click New.</span></span>
3. <span data-ttu-id="f087e-110">Klik op Verkooporder.</span><span class="sxs-lookup"><span data-stu-id="f087e-110">Click Sales order.</span></span>
4. <span data-ttu-id="f087e-111">Selecteer US-001 in het veld Klantrekening.</span><span class="sxs-lookup"><span data-stu-id="f087e-111">In the Customer account field, select US-001.</span></span> 
5. <span data-ttu-id="f087e-112">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="f087e-112">Click OK.</span></span>
6. <span data-ttu-id="f087e-113">Selecteer D0006 in het veld Artikelnummer.</span><span class="sxs-lookup"><span data-stu-id="f087e-113">In the Item number field, select D0006.</span></span>
    * <span data-ttu-id="f087e-114">Voor deze taak moet u een configureerbaar product selecteren.</span><span class="sxs-lookup"><span data-stu-id="f087e-114">For this task, you must select a configurable product.</span></span>  
7. <span data-ttu-id="f087e-115">Klik op Product en voorraad.</span><span class="sxs-lookup"><span data-stu-id="f087e-115">Click Product and supply.</span></span>
8. <span data-ttu-id="f087e-116">Klik op Regel configureren.</span><span class="sxs-lookup"><span data-stu-id="f087e-116">Click Configure line.</span></span>
    * <span data-ttu-id="f087e-117">Merk op dat de prijs is gewijzigd, op basis van de configuratie die is geselecteerd, en dat het veld Met kabel nu op Waar is ingesteld.</span><span class="sxs-lookup"><span data-stu-id="f087e-117">Note that the price has changed, based on the configuration that was selected, and that the Include cable field is now set to True.</span></span>  
    * <span data-ttu-id="f087e-118">Let op de standaardprijs en de instellingen die voor de kabel worden geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="f087e-118">Note the default price and the settings that are selected for the cable.</span></span>  
9. <span data-ttu-id="f087e-119">Klik op Sjabloon laden.</span><span class="sxs-lookup"><span data-stu-id="f087e-119">Click Load template.</span></span>
    * <span data-ttu-id="f087e-120">Dit voorbeeld laat zien hoe u een sjabloon kunt toepassen om een vooraf gedefinieerde configuratie te selecteren.</span><span class="sxs-lookup"><span data-stu-id="f087e-120">This example shows how you can apply a template to select a predefined configuration.</span></span> <span data-ttu-id="f087e-121">Als u deze procedure als taakbegeleider gebruikt en de andere kenmerkwaarden wilt weergeven die beschikbaar zijn, moet u op de knop Ontgrendelen klikken.</span><span class="sxs-lookup"><span data-stu-id="f087e-121">If you’re using this procedure as a task guide and want to see the other attribute values that are available, you must click the Unlock button.</span></span>  
10. <span data-ttu-id="f087e-122">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="f087e-122">Click OK.</span></span>
11. <span data-ttu-id="f087e-123">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="f087e-123">Click OK.</span></span>
12. <span data-ttu-id="f087e-124">Vouw de sectie Regeldetails uit.</span><span class="sxs-lookup"><span data-stu-id="f087e-124">Expand the Line details section.</span></span>
13. <span data-ttu-id="f087e-125">Klik op het tabblad Product.</span><span class="sxs-lookup"><span data-stu-id="f087e-125">Click the Product tab.</span></span>
    * <span data-ttu-id="f087e-126">De configuratie van het artikel wordt nu vermeld onder productdimensies.</span><span class="sxs-lookup"><span data-stu-id="f087e-126">The configuration of the item is now listed under the product dimensions.</span></span>  
14. <span data-ttu-id="f087e-127">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="f087e-127">Close the page.</span></span>

## <a name="select-the-product-configuration"></a><span data-ttu-id="f087e-128">Selecteer de productconfiguratie</span><span class="sxs-lookup"><span data-stu-id="f087e-128">Select the product configuration</span></span>


