---
title: Batchkenmerken
description: Dit artikel geeft informatie over batchkenmerken. Batchkenmerken zijn eigenschappen van grondstoffen en eindproducten die samen voorraadbatches vormen. In het artikel wordt ook uitgelegd hoe u batchkenmerken toewijst en hoe u erop kunt zoeken wanneer u batches reserveert.
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PdsBatchAttrib, PdsBatchAttribAssociate, PdsBatchAttribByAttribGroup, PdsBatchAttribByItem, PdsBatchAttribByitemCustomer, PdsBatchAttribGroup
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 19271
ms.assetid: 41de0250-4a96-412e-a412-aa06615b6b1d
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: 0c3f5115377178941984e53749c18cc1c9179812
ms.contentlocale: nl-nl
ms.lasthandoff: 07/18/2017

---

# <a name="batch-attributes"></a><span data-ttu-id="ba57d-105">Batchkenmerken</span><span class="sxs-lookup"><span data-stu-id="ba57d-105">Batch attributes</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="ba57d-106">Dit artikel geeft informatie over batchkenmerken.</span><span class="sxs-lookup"><span data-stu-id="ba57d-106">This article provides information about batch attributes.</span></span> <span data-ttu-id="ba57d-107">Batchkenmerken zijn eigenschappen van grondstoffen en eindproducten die samen voorraadbatches vormen.</span><span class="sxs-lookup"><span data-stu-id="ba57d-107">Batch attributes are characteristics of raw materials and finished products that make up inventory batches.</span></span> <span data-ttu-id="ba57d-108">In het artikel wordt ook uitgelegd hoe u batchkenmerken toewijst en hoe u erop kunt zoeken wanneer u batches reserveert.</span><span class="sxs-lookup"><span data-stu-id="ba57d-108">The article also explains how to assign batch attributes, and how you can search on them when you reserve batches.</span></span>

<span data-ttu-id="ba57d-109">Batchkenmerken zijn eigenschappen van grondstoffen en eindproducten die samen voorraadbatches vormen.</span><span class="sxs-lookup"><span data-stu-id="ba57d-109">Batch attributes are characteristics of raw materials and finished products that make up inventory batches.</span></span> <span data-ttu-id="ba57d-110">Batchkenmerken kunnen verschillen, afhankelijk van zaken als omgevingsfactoren, de kwaliteit van de grondstoffen waarmee de batch wordt geproduceerd of het resultaat van het eindproduct.</span><span class="sxs-lookup"><span data-stu-id="ba57d-110">Batch attributes can vary, depending on factors such as environmental conditions, the quality of the raw materials that are used to produce the batch, or the outcome of the finished product.</span></span> <span data-ttu-id="ba57d-111">Het aantal en de typen batchkenmerken die worden gebruikt, kunnen aanzienlijk verschillen per bedrijfstak.</span><span class="sxs-lookup"><span data-stu-id="ba57d-111">The number and types of batch attributes that are used can vary widely from one industry to another.</span></span> <span data-ttu-id="ba57d-112">Hierna volgen twee voorbeelden van het gebruik van batchkenmerken:</span><span class="sxs-lookup"><span data-stu-id="ba57d-112">Here are two examples that show how to use batch attributes:</span></span>

-   <span data-ttu-id="ba57d-113">In de kaashandel is melk een van de grondstoffen voor de kaasproductie. Deze kan kenmerken hebben, zoals vetgehalte en percentagegewicht.</span><span class="sxs-lookup"><span data-stu-id="ba57d-113">In the cheese industry, milk, which is one of the raw materials that are used to produce the cheese, can have attributes such as fat content and percentage weight.</span></span> <span data-ttu-id="ba57d-114">De kaas die wordt geproduceerd van de melk kan andere kenmerken hebben, zoals vochtgehalte en ouderdom.</span><span class="sxs-lookup"><span data-stu-id="ba57d-114">The cheese that is produced from the milk can have other attributes, such as moisture and age.</span></span>
-   <span data-ttu-id="ba57d-115">In de staalindustrie kan het ijzer dat wordt geproduceerd kenmerken hebben zoals het magnesium-, zilver- en zinkpercentage.</span><span class="sxs-lookup"><span data-stu-id="ba57d-115">In the steel industry, the iron that is produced might have attributes such as the percentages of magnesium content, silver content, and zinc content.</span></span>

<span data-ttu-id="ba57d-116">U kunt het aantal en de typen kenmerken beter beheren door batchkenmerkgroepen te gebruiken.</span><span class="sxs-lookup"><span data-stu-id="ba57d-116">To better manage the number and types of attributes, you can use batch attribute groups.</span></span> <span data-ttu-id="ba57d-117">Op deze manier hoeft u niet elk kenmerk afzonderlijk toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="ba57d-117">In this way, you don't have to add each attribute individually.</span></span>

## <a name="assign-batch-attributes"></a><span data-ttu-id="ba57d-118">Batchkenmerken toewijzen</span><span class="sxs-lookup"><span data-stu-id="ba57d-118">Assign batch attributes</span></span>
<span data-ttu-id="ba57d-119">U kunt batchkenmerken toewijzen aan afzonderlijke producten die zijn opgeslagen in voorraadbatches of aan producten die zijn gekoppeld aan specifieke klanten.</span><span class="sxs-lookup"><span data-stu-id="ba57d-119">You can assign batch attributes to individual products that are held in inventory batches, or you can assign them to products that are associated with specific customers.</span></span> <span data-ttu-id="ba57d-120">Voordat u een batchkenmerk kunt toewijzen op klantniveau, moet u dit eerst toewijzen op productniveau.</span><span class="sxs-lookup"><span data-stu-id="ba57d-120">Before you can assign a batch attribute at the customer level, you must assign it at the product level.</span></span> <span data-ttu-id="ba57d-121">Het product moet een batchdimensie hebben die is ingesteld op **Actief** in de trackingdimensiegroep.</span><span class="sxs-lookup"><span data-stu-id="ba57d-121">The product must have the batch dimension set to **Active** in the tracking dimension group.</span></span> <span data-ttu-id="ba57d-122">Gebruik de productgebonden pagina om een batchkenmerk toe te wijzen aan een afzonderlijk product.</span><span class="sxs-lookup"><span data-stu-id="ba57d-122">To assign a batch attribute to an individual product, use the product-specific page.</span></span> <span data-ttu-id="ba57d-123">Gebruik de klantgebonden pagina als het kenmerk specifiek is voor een product voor een bepaalde klant.</span><span class="sxs-lookup"><span data-stu-id="ba57d-123">If the attribute is specific to a product for a customer, use the customer-specific page.</span></span> <span data-ttu-id="ba57d-124">Wanneer u een kenmerk toevoegt aan een product, definieert u ook andere parameters.</span><span class="sxs-lookup"><span data-stu-id="ba57d-124">When you add an attribute to a product, you also define other parameters.</span></span> <span data-ttu-id="ba57d-125">Hieronder vindt u enkele voorbeelden:</span><span class="sxs-lookup"><span data-stu-id="ba57d-125">Here are some examples:</span></span>

-   <span data-ttu-id="ba57d-126">Het minimum- en maximumbereik voor een kenmerk van het type **Geheel getal** of **Breuk**.</span><span class="sxs-lookup"><span data-stu-id="ba57d-126">The minimum and maximum ranges for an attribute of the **Integer** or **Fraction** type.</span></span>
-   <span data-ttu-id="ba57d-127">De tolerantieacties voor een kenmerk van het type **Geheel getal** of **Breuk**.</span><span class="sxs-lookup"><span data-stu-id="ba57d-127">The tolerance actions for an attribute of the **Integer** or **Fraction** type.</span></span> <span data-ttu-id="ba57d-128">Als de waarde van het kenmerk buiten het minimum- of maximumbereik valt, kan de actie een waarschuwingsbericht zijn of een foutbericht.</span><span class="sxs-lookup"><span data-stu-id="ba57d-128">If the value of the attribute falls outside the minimum and maximum range, the action can be either a warning message or an error message.</span></span>
-   <span data-ttu-id="ba57d-129">De doelwaarde voor het kenmerk.</span><span class="sxs-lookup"><span data-stu-id="ba57d-129">The target value for the attribute.</span></span> <span data-ttu-id="ba57d-130">Dit is de optimale waard van het kenmerk, die van toepassing is op alle kenmerktypen.</span><span class="sxs-lookup"><span data-stu-id="ba57d-130">This value is the optimal value of the attribute, and it applies to all attribute types.</span></span>

<span data-ttu-id="ba57d-131">U kunt de pagina's openen voor producten die u selecteert op de pagina **Vrijgegeven producten** in Productgegevensbeheer.</span><span class="sxs-lookup"><span data-stu-id="ba57d-131">You can access the pages for products that you select on the **Released products** page in Product information management.</span></span> <span data-ttu-id="ba57d-132">Wanneer u batchkenmerken aan een product hebt toegewezen, kunt u vervolgens specifieke waarden toevoegen aan de kenmerken op de pagina **Voorraadbatchkenmerken**.</span><span class="sxs-lookup"><span data-stu-id="ba57d-132">After you assign batch attributes to a product, you can add specific values to the attributes on the **Inventory batch attributes** page.</span></span>

## <a name="reserve-batches"></a><span data-ttu-id="ba57d-133">Reservebatches</span><span class="sxs-lookup"><span data-stu-id="ba57d-133">Reserve batches</span></span>
<span data-ttu-id="ba57d-134">U kunt zoeken op batchkenmerken wanneer u batchreserveringen voor een verkooporder uitvoert om de order van een klant te vervullen of bij het verzamelen en reserveren van batches voor een productieorder.</span><span class="sxs-lookup"><span data-stu-id="ba57d-134">You can search on batch attributes when you do batch reservations for a sales order to fullfill a customer's order, or when you pick and reserve batches for a production order.</span></span> <span data-ttu-id="ba57d-135">De zoekactie helpt bij het opsporen van een voorraadbatch die het product bevat met de batchkenmerken die u wilt.</span><span class="sxs-lookup"><span data-stu-id="ba57d-135">The search helps locate an inventory batch that contains the product that has the batch attribute that you want.</span></span> <span data-ttu-id="ba57d-136">Nadat u de batch of batches hebt gevonden, kunt u het product reserveren voor de oorspronkelijke voorraadtransactieregel.</span><span class="sxs-lookup"><span data-stu-id="ba57d-136">After you locate the batch or batches, you can reserve the product to the originating inventory transaction line.</span></span>




