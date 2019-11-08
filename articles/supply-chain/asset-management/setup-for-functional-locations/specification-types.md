---
title: Typen onderhoudskenmerken
description: In dit onderwerp wordt uitgelegd hoe u kenmerktypen maakt in Activabeheer.
author: josaw1
manager: AnnBe
ms.date: 06/24/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c07f303b72f286c33979181fca1592b47efa1303
ms.sourcegitcommit: d37fb09101c30858bcb975931b3d8f947d72017b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/10/2019
ms.locfileid: "2571226"
---
# <a name="maintenance-attribute-types"></a><span data-ttu-id="5071c-103">Typen onderhoudskenmerken</span><span class="sxs-lookup"><span data-stu-id="5071c-103">Maintenance attribute types</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="5071c-104">In dit onderwerp wordt uitgelegd hoe u kenmerktypen maakt in Activabeheer.</span><span class="sxs-lookup"><span data-stu-id="5071c-104">This topic explains how to create attribute types in Asset Management.</span></span> <span data-ttu-id="5071c-105">Kenmerken worden gebruikt om de eigenschappen van verschillende elementen te beschrijven.</span><span class="sxs-lookup"><span data-stu-id="5071c-105">Attributes are used to describe the properties of various elements.</span></span> <span data-ttu-id="5071c-106">U kunt kenmerken instellen voor de volgende elementen:</span><span class="sxs-lookup"><span data-stu-id="5071c-106">You can set up attributes on the following elements:</span></span>

- [<span data-ttu-id="5071c-107">Typen functionele locaties</span><span class="sxs-lookup"><span data-stu-id="5071c-107">Functional location types</span></span>](../setup-for-functional-locations/functional-location-types.md)
- [<span data-ttu-id="5071c-108">Functionele locaties</span><span class="sxs-lookup"><span data-stu-id="5071c-108">Functional locations</span></span>](../functional-locations/create-functional-locations.md)
- [<span data-ttu-id="5071c-109">Activatypen</span><span class="sxs-lookup"><span data-stu-id="5071c-109">Asset types</span></span>](../setup-for-objects/object-types.md)
- <span data-ttu-id="5071c-110">Activa</span><span class="sxs-lookup"><span data-stu-id="5071c-110">Assets</span></span>

<span data-ttu-id="5071c-111">De kenmerken die u kunt instellen, variëren, afhankelijk van het element.</span><span class="sxs-lookup"><span data-stu-id="5071c-111">The attributes that you can set up vary, depending on the element.</span></span> <span data-ttu-id="5071c-112">Zo kunt u bijvoorbeeld voor een functionele locatie kenmerken instellen voor de configuratie en de fysieke grootte van de locatie.</span><span class="sxs-lookup"><span data-stu-id="5071c-112">For example, for a functional location, you can set up attributes for the configuration and physical size of the location.</span></span> <span data-ttu-id="5071c-113">Voor een activatype of een activum kunt u kenmerken instellen voor motorinhoud, stroomverbruik en maximale belastingscapaciteit onder verschillende omstandigheden.</span><span class="sxs-lookup"><span data-stu-id="5071c-113">For an asset type or an asset, you can set up attributes for engine volume, power consumption, and maximum load capacity under different conditions.</span></span>

## <a name="create-attribute-types"></a><span data-ttu-id="5071c-114">Kenmerktypen maken</span><span class="sxs-lookup"><span data-stu-id="5071c-114">Create attribute types</span></span>

<span data-ttu-id="5071c-115">U kunt uw eigen kenmerktypen maken</span><span class="sxs-lookup"><span data-stu-id="5071c-115">You can create your own attribute types.</span></span> <span data-ttu-id="5071c-116">Bovendien kunt u productdimensies overbrengen naar de pagina **Kenmerktypen**.</span><span class="sxs-lookup"><span data-stu-id="5071c-116">Additionally, you can transfer product dimensions to the **Attribute types** page.</span></span>

1. <span data-ttu-id="5071c-117">Selecteer **Activabeheer** \> **Instellingen** \> **Kenmerktypen**.</span><span class="sxs-lookup"><span data-stu-id="5071c-117">Select **Asset management** \> **Setup** \> **Attribute types**.</span></span>
2. <span data-ttu-id="5071c-118">Wanneer u voor het eerst kenmerktypen instelt, selecteert u **Productdimensies maken** om automatisch standaard productdimensies over te zetten.</span><span class="sxs-lookup"><span data-stu-id="5071c-118">The first time that you set up attribute types, select **Create product dimensions** to automatically transfer standard product dimensions.</span></span>
3. <span data-ttu-id="5071c-119">Selecteer **Nieuw** om een nieuw kenmerktype te maken.</span><span class="sxs-lookup"><span data-stu-id="5071c-119">Select **New** to create a new attribute type.</span></span>
4. <span data-ttu-id="5071c-120">Voer in het veld **Kenmerktype** een naam in voor het kenmerktype.</span><span class="sxs-lookup"><span data-stu-id="5071c-120">In the **Attribute type** field, enter a name for the attribute type.</span></span>
5. <span data-ttu-id="5071c-121">Voer in het veld **Beschrijving** een beschrijving in.</span><span class="sxs-lookup"><span data-stu-id="5071c-121">In the **Description** field, enter a description.</span></span>
6. <span data-ttu-id="5071c-122">Selecteer indien nodig in het veld **Eenheid** de relevante kenmerkeenheid.</span><span class="sxs-lookup"><span data-stu-id="5071c-122">In the **Unit** field, select the relevant attribute unit, as required.</span></span>
7. <span data-ttu-id="5071c-123">Selecteer in het veld **Gegevenstype** een gegevenstype voor de eenheid.</span><span class="sxs-lookup"><span data-stu-id="5071c-123">In the **Data type** field, select a data type for the unit.</span></span>
8. <span data-ttu-id="5071c-124">Als u **Tekenreeks** hebt geselecteerd als gegevenstype, voert u de volgende stappen uit om waarden voor het kenmerktype te maken:</span><span class="sxs-lookup"><span data-stu-id="5071c-124">If you selected **String** as the data type, follow these steps to create values for the attribute type:</span></span>

    1. <span data-ttu-id="5071c-125">Selecteer het kenmerktype en selecteer vervolgens **Waarden**.</span><span class="sxs-lookup"><span data-stu-id="5071c-125">Select the attribute type, and then select **Values**.</span></span>
    2. <span data-ttu-id="5071c-126">Selecteer **Nieuw** in het veld **Kenmerkwaarden**.</span><span class="sxs-lookup"><span data-stu-id="5071c-126">In the **Attribute values** field, select **New**.</span></span>
    3. <span data-ttu-id="5071c-127">Selecteer een kenmerktype (dimensie) in het veld **Kenmerktype**.</span><span class="sxs-lookup"><span data-stu-id="5071c-127">In the **Attribute type** field, select an attribute type (dimension).</span></span>
    4. <span data-ttu-id="5071c-128">Voer een gerelateerde waarde in het veld **Waarde** in.</span><span class="sxs-lookup"><span data-stu-id="5071c-128">In the **Value** field, enter a related value.</span></span>
    5. <span data-ttu-id="5071c-129">Voer in het veld **Beschrijving** een beschrijving in.</span><span class="sxs-lookup"><span data-stu-id="5071c-129">In the **Description** field, enter a description.</span></span>
    6. <span data-ttu-id="5071c-130">Sla de record op.</span><span class="sxs-lookup"><span data-stu-id="5071c-130">Save the record.</span></span>
    7. <span data-ttu-id="5071c-131">Ga terug naar de pagina **Kenmerktypen**.</span><span class="sxs-lookup"><span data-stu-id="5071c-131">Return to the **Attribute types** page.</span></span>

9. <span data-ttu-id="5071c-132">Sla de record op.</span><span class="sxs-lookup"><span data-stu-id="5071c-132">Save the record.</span></span>

    <span data-ttu-id="5071c-133">Het veld **Typen functionele locatie** bevat het aantal functionele locaties dat het kenmerktype gebruikt.</span><span class="sxs-lookup"><span data-stu-id="5071c-133">The **Functional location types** field shows the number of functional locations that are using the attribute type.</span></span> <span data-ttu-id="5071c-134">Het veld **Activatypen** bevat het aantal activatypen dat hiervan gebruikmaakt.</span><span class="sxs-lookup"><span data-stu-id="5071c-134">The **Asset types** field shows the number of asset types that are using it.</span></span>
