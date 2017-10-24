---
title: Productieorders maken
description: "Als een productieorder wordt gemaakt, wordt er een aanvraag geïnitieerd om te beginnen met de productie van een artikel. De productieorder bevat informatie over het artikel dat wordt geproduceerd, het aantal en de geplande einddatum. Het bevat ook informatie over de te verwerken materialen en de processen die moeten worden gevolgd om het artikel te produceren."
author: johanhoffmann
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ProdTable, ProdTableCreate
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 19741
ms.assetid: bbb6e69d-479c-45fc-a0a8-66da5df16c7f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 58213d4d6e8c29ab6605eb7aa5c6cb9ca6ba4a10
ms.contentlocale: nl-nl
ms.lasthandoff: 09/29/2017

---

# <a name="create-production-orders"></a><span data-ttu-id="fe692-105">Productieorders maken</span><span class="sxs-lookup"><span data-stu-id="fe692-105">Create production orders</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="fe692-106">Als een productieorder wordt gemaakt, wordt er een aanvraag geïnitieerd om te beginnen met de productie van een artikel.</span><span class="sxs-lookup"><span data-stu-id="fe692-106">When a production order is created, a request is initiated to start producing an item.</span></span> <span data-ttu-id="fe692-107">De productieorder bevat informatie over het artikel dat wordt geproduceerd, het aantal en de geplande einddatum.</span><span class="sxs-lookup"><span data-stu-id="fe692-107">The production order contains information about what will be produced, the quantity to produce, and the planned finish date.</span></span> <span data-ttu-id="fe692-108">Het bevat ook informatie over de te verwerken materialen en de processen die moeten worden gevolgd om het artikel te produceren.</span><span class="sxs-lookup"><span data-stu-id="fe692-108">It also contains information about which materials to consume and which process to follow to produce the item.</span></span>

<span data-ttu-id="fe692-109">Een productieorder doorloopt fasen van de productielevenscyclus.</span><span class="sxs-lookup"><span data-stu-id="fe692-109">A production order passes through stages of the production life cycle.</span></span> <span data-ttu-id="fe692-110">Bij het maken wordt aan een order de status **Gemaakt** toegewezen.</span><span class="sxs-lookup"><span data-stu-id="fe692-110">When an order is created, it is assigned the status **Created**.</span></span> <span data-ttu-id="fe692-111">Bij het voltooien wordt aan een order de status **Beëindigd** toegewezen.</span><span class="sxs-lookup"><span data-stu-id="fe692-111">When an order is finished, it is assigned the status **Ended**.</span></span> <span data-ttu-id="fe692-112">Met een parameterinstelling in elke fase kan een gebruiker elke stap configureren.</span><span class="sxs-lookup"><span data-stu-id="fe692-112">A parameter setting in each stage allows a user to configure each step.</span></span> <span data-ttu-id="fe692-113">De instelling kan worden opgegeven voor één gebruiker of voor alle gebruikers.</span><span class="sxs-lookup"><span data-stu-id="fe692-113">The setting can be set up for a single user or for all users.</span></span>

<span data-ttu-id="fe692-114">De productiestuklijst en de productieroute zijn de belangrijkste entiteiten van de productieorder.</span><span class="sxs-lookup"><span data-stu-id="fe692-114">The production bill of material and the production route are the main entities of the production order.</span></span> <span data-ttu-id="fe692-115">Ze worden naar de productieorder gekopieerd op basis van het geselecteerde artikel en de hoeveelheid die gaan worden geproduceerd.</span><span class="sxs-lookup"><span data-stu-id="fe692-115">They are copied to the production order based on the selected item and quantity that are going to be produced.</span></span> <span data-ttu-id="fe692-116">Voordat de productieorder is gestart, kunnen de productiestuklijst en route worden bewerkt.</span><span class="sxs-lookup"><span data-stu-id="fe692-116">Before the production order is started, the production bill of material and route can be edited.</span></span>

<span data-ttu-id="fe692-117">Een productieorder kan in de volgende scenario's worden gemaakt:</span><span class="sxs-lookup"><span data-stu-id="fe692-117">A production order can be created in the following scenarios:</span></span>

-   <span data-ttu-id="fe692-118">Gemaakt door hoofdplanningsuitvoering op basis van de vraag naar materiaal.</span><span class="sxs-lookup"><span data-stu-id="fe692-118">Created by master planning execution based on material demand.</span></span>
-   <span data-ttu-id="fe692-119">Rechtstreeks gemaakt van een verkooporderregel of wanneer een productieorder van een hoger niveau wordt gemaakt en geraamd (getraceerd aanbod).</span><span class="sxs-lookup"><span data-stu-id="fe692-119">Created directly from a sales order line or when a higher-level production order is created and estimated (pegged supply).</span></span>
-   <span data-ttu-id="fe692-120">Handmatig gemaakt.</span><span class="sxs-lookup"><span data-stu-id="fe692-120">Created manually.</span></span>





