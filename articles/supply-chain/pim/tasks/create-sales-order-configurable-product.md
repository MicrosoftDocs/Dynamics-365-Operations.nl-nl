---
title: Een verkooporder voor een configureerbaar product maken
description: Deze procedure laat zien hoe u een configuratiesjabloon toepast op een product in een verkooporder.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, SalesOrderProcessingWorkspace, SalesCreateOrder, SalesTable, PCRuntimeConfigurator, PCTemplateConfigurationSelection
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8607de5705354aa58c985fb536f3e1d52acd1f37
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/20/2021
ms.locfileid: "5921284"
---
# <a name="create-a-sales-order-for-a-configurable-product"></a><span data-ttu-id="178de-103">Een verkooporder voor een configureerbaar product maken</span><span class="sxs-lookup"><span data-stu-id="178de-103">Create a sales order for a configurable product</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="178de-104">Deze procedure laat zien hoe u een configuratiesjabloon toepast op een product in een verkooporder.</span><span class="sxs-lookup"><span data-stu-id="178de-104">This procedure shows how to apply a configuration template to a product on a sales order.</span></span> <span data-ttu-id="178de-105">In dit voorbeeld wordt het model D0006-luidspreker gebruikt in het demobedrijf USMF.</span><span class="sxs-lookup"><span data-stu-id="178de-105">This example uses the D0006 speaker model in the USMF demo data company.</span></span> <span data-ttu-id="178de-106">Gewoonlijk gebruikt een verkooporderbewerker deze procedure.</span><span class="sxs-lookup"><span data-stu-id="178de-106">Typically, a sales order processor uses this procedure.</span></span>

## <a name="create-a-sales-order"></a><span data-ttu-id="178de-107">Verkooporder maken</span><span class="sxs-lookup"><span data-stu-id="178de-107">Create a sales order</span></span>

1. <span data-ttu-id="178de-108">Ga naar **Verkoop en marketing \> Werkgebieden \> Verkooporderverwerking en -onderzoek**.</span><span class="sxs-lookup"><span data-stu-id="178de-108">Go to **Sales and marketing \> Workspaces \> Sales order processing and inquiry**.</span></span>
1. <span data-ttu-id="178de-109">Selecteer **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="178de-109">Select **New**.</span></span>
1. <span data-ttu-id="178de-110">Selecteer **Verkooporders**.</span><span class="sxs-lookup"><span data-stu-id="178de-110">Select **Sales order**.</span></span>
1. <span data-ttu-id="178de-111">Selecteer *US-001* in het veld **Klantrekening**.</span><span class="sxs-lookup"><span data-stu-id="178de-111">In the **Customer account** field, select *US-001*.</span></span> 
1. <span data-ttu-id="178de-112">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="178de-112">Select **OK**.</span></span>
1. <span data-ttu-id="178de-113">Selecteer in het veld **Artikelnummer** de optie *D0006*.</span><span class="sxs-lookup"><span data-stu-id="178de-113">In the **Item number** field, select *D0006*.</span></span>
    * <span data-ttu-id="178de-114">Voor deze taak moet u een configureerbaar product selecteren.</span><span class="sxs-lookup"><span data-stu-id="178de-114">For this task, you must select a configurable product.</span></span>  
1. <span data-ttu-id="178de-115">Selecteer **Product en voorraad**.</span><span class="sxs-lookup"><span data-stu-id="178de-115">Select **Product and supply**.</span></span>
1. <span data-ttu-id="178de-116">Selecteer **Regel configureren**.</span><span class="sxs-lookup"><span data-stu-id="178de-116">Select **Configure line**.</span></span>
    * <span data-ttu-id="178de-117">Merk op dat de prijs is gewijzigd, op basis van de configuratie die is geselecteerd, en dat het veld **Met kabel** nu op *Waar* is ingesteld.</span><span class="sxs-lookup"><span data-stu-id="178de-117">Note that the price has changed, based on the configuration that was selected, and that the **Include cable** field is now set to *True*.</span></span>  
    * <span data-ttu-id="178de-118">Let op de standaardprijs en de instellingen die voor de kabel worden geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="178de-118">Note the default price and the settings that are selected for the cable.</span></span>  
1. <span data-ttu-id="178de-119">Selecteer **Sjabloon laden**.</span><span class="sxs-lookup"><span data-stu-id="178de-119">Select **Load template**.</span></span>
    * <span data-ttu-id="178de-120">Dit voorbeeld laat zien hoe u een sjabloon kunt toepassen om een vooraf gedefinieerde configuratie te selecteren.</span><span class="sxs-lookup"><span data-stu-id="178de-120">This example shows how you can apply a template to select a predefined configuration.</span></span> <span data-ttu-id="178de-121">Als u deze procedure als taakbegeleider gebruikt en de andere kenmerkwaarden wilt weergeven die beschikbaar zijn, moet u op de knop **Ontgrendelen** klikken.</span><span class="sxs-lookup"><span data-stu-id="178de-121">If you're using this procedure as a task guide and want to see the other attribute values that are available, you must select the **Unlock** button.</span></span>  
1. <span data-ttu-id="178de-122">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="178de-122">Select **OK**.</span></span>
1. <span data-ttu-id="178de-123">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="178de-123">Select **OK**.</span></span>
1. <span data-ttu-id="178de-124">Vouw de sectie **Regeldetails** uit.</span><span class="sxs-lookup"><span data-stu-id="178de-124">Expand the **Line details** section.</span></span>
1. <span data-ttu-id="178de-125">Selecteer het tabblad **Product**.</span><span class="sxs-lookup"><span data-stu-id="178de-125">Select the **Product** tab.</span></span>
    * <span data-ttu-id="178de-126">De configuratie van het artikel wordt nu vermeld onder productdimensies.</span><span class="sxs-lookup"><span data-stu-id="178de-126">The configuration of the item is now listed under the product dimensions.</span></span>  
1. <span data-ttu-id="178de-127">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="178de-127">Close the page.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]