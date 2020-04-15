---
title: Een nieuw product maken
description: In dit onderwerp wordt beschreven hoe u een gedeeld product maakt.
author: ShylaThompson
manager: AnnBe
ms.date: 07/22/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductListPage, EcoResProductCreate, EcoResProductDetails, EcoResProductInventoryDimensionGroups
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 611fc0cff7fe2d580e971149630e92afd16be228
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/18/2020
ms.locfileid: "3147843"
---
# <a name="create-a-new-product"></a><span data-ttu-id="eead4-103">Een nieuw product maken</span><span class="sxs-lookup"><span data-stu-id="eead4-103">Create a new product</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="eead4-104">In dit onderwerp wordt beschreven hoe u een gedeeld product maakt.</span><span class="sxs-lookup"><span data-stu-id="eead4-104">This topic describes how to create a new shared product.</span></span> <span data-ttu-id="eead4-105">Het wordt gewoonlijk uitgevoerd door een productontwerper.</span><span class="sxs-lookup"><span data-stu-id="eead4-105">It is usually carried out by a product designer.</span></span> <span data-ttu-id="eead4-106">Het bedrijf van de demogegevens dat wordt gebruikt om deze taak te maken is USMF.</span><span class="sxs-lookup"><span data-stu-id="eead4-106">The demo data company used to create this task is USMF.</span></span>


## <a name="create-a-product"></a><span data-ttu-id="eead4-107">Een product maken</span><span class="sxs-lookup"><span data-stu-id="eead4-107">Create a product</span></span>
1. <span data-ttu-id="eead4-108">Ga in het navigatievenster naar **Modules > Productgegevensbeheer > Producten > Producten**.</span><span class="sxs-lookup"><span data-stu-id="eead4-108">In the Navigation pane, go to **Modules > Product information management > Products > Products**.</span></span>
2. <span data-ttu-id="eead4-109">Selecteer **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="eead4-109">Select **New**.</span></span>
3. <span data-ttu-id="eead4-110">Typ een waarde in het veld **Productnummer**.</span><span class="sxs-lookup"><span data-stu-id="eead4-110">In the **Product number** field, type a value.</span></span> <span data-ttu-id="eead4-111">Als er geen nummerreeks is ingesteld voor het productnummer, moet het nummer handmatig worden ingevoerd.</span><span class="sxs-lookup"><span data-stu-id="eead4-111">If a number sequence has not been set up for the product number, it must be entered manually.</span></span>  
4. <span data-ttu-id="eead4-112">Typ een waarde in het veld **Productnaam**.</span><span class="sxs-lookup"><span data-stu-id="eead4-112">In the **Product name** field, type a value.</span></span> <span data-ttu-id="eead4-113">Voor de productnaam wordt standaard de zoeknaam gebruikt.</span><span class="sxs-lookup"><span data-stu-id="eead4-113">The product name defaults to the search name.</span></span> <span data-ttu-id="eead4-114">U kunt deze zo nodig wijzigen.</span><span class="sxs-lookup"><span data-stu-id="eead4-114">You can change this if needed.</span></span>  
5. <span data-ttu-id="eead4-115">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="eead4-115">Select **OK**.</span></span>

## <a name="set-up-dimension-groups"></a><span data-ttu-id="eead4-116">Dimensiegroepen instellen</span><span class="sxs-lookup"><span data-stu-id="eead4-116">Set up dimension groups</span></span>
1. <span data-ttu-id="eead4-117">Selecteer **Dimensiegroepen** om het uitklapvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="eead4-117">Select **Dimension groups** to open the drop dialog.</span></span>
2. <span data-ttu-id="eead4-118">In het veld **Opslagdimensiegroep** typt of selecteert u een waarde.</span><span class="sxs-lookup"><span data-stu-id="eead4-118">In the **Storage dimension group** field, enter or select a value.</span></span> <span data-ttu-id="eead4-119">De opslagdimensiegroep bepaalt welke opslagdimensies u op elke transactie voor het product moet invoeren en hoe het in voorraad wordt bijgehouden.</span><span class="sxs-lookup"><span data-stu-id="eead4-119">The storage dimension group determines which storage dimensions you must enter on each transaction for the product and how it will be tracked in inventory.</span></span>  
3. <span data-ttu-id="eead4-120">In het veld **Traceringsdimensiegroep** typt of selecteert u een waarde.</span><span class="sxs-lookup"><span data-stu-id="eead4-120">In the **Tracking dimension group** field, enter or select a value.</span></span> <span data-ttu-id="eead4-121">De traceringsdimensiegroep bepaalt welke traceringsdimensies u voor elke transactie voor het product moet invoeren en hoe het in voorraad wordt verwerkt.</span><span class="sxs-lookup"><span data-stu-id="eead4-121">The tracking dimension group determines which tracking dimensions you must enter for each transaction for the product, and how it will be handled in inventory.</span></span>  
4. <span data-ttu-id="eead4-122">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="eead4-122">Select **OK**.</span></span>

