---
title: Serviceobjectrelaties
description: U kunt serviceobjectrelaties maken tussen een serviceobject en een serviceovereenkomst of serviceorder.
author: ShylaThompson
manager: tfehr
ms.date: 02/21/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceObjectRelation
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e2b1b76dffc2751d51c2a25d831fab512b747c15
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/10/2020
ms.locfileid: "3979349"
---
# <a name="service-object-relations"></a><span data-ttu-id="edaba-103">Serviceobjectrelaties</span><span class="sxs-lookup"><span data-stu-id="edaba-103">Service object relations</span></span> 

[!include [banner](../includes/banner.md)]

<span data-ttu-id="edaba-104">U kunt serviceobjectrelaties maken tussen een serviceobject en een serviceovereenkomst of serviceorder.</span><span class="sxs-lookup"><span data-stu-id="edaba-104">You can create service object relations between a service object and a service agreement or service order.</span></span> <span data-ttu-id="edaba-105">Wanneer u een relatie maakt, koppelt u het serviceobject aan de serviceovereenkomst of serviceorder.</span><span class="sxs-lookup"><span data-stu-id="edaba-105">When you create a relation, you attach the service object to the service agreement or service order.</span></span>

<span data-ttu-id="edaba-106">Nadat de relatie is gemaakt, kunt u het serviceobject koppelen aan de regels in de serviceovereenkomst of serviceorder.</span><span class="sxs-lookup"><span data-stu-id="edaba-106">After the relation is created, you can attach the service object to any lines on the service agreement or service order.</span></span>

## <a name="template-boms"></a><span data-ttu-id="edaba-107">Sjabloonstuklijsten</span><span class="sxs-lookup"><span data-stu-id="edaba-107">Template BOMs</span></span>

<span data-ttu-id="edaba-108">U kunt ook een sjabloonstuklijst voor de objectrelatie opgeven.</span><span class="sxs-lookup"><span data-stu-id="edaba-108">You can also specify a template BOM for the object relation.</span></span> <span data-ttu-id="edaba-109">De sjabloonstuklijst is een stuklijst voor het object waarop u service uitvoert.</span><span class="sxs-lookup"><span data-stu-id="edaba-109">The template BOM is a bill of materials for the object on which you perform service.</span></span> <span data-ttu-id="edaba-110">Als u een onderdeel van het serviceobject vervangt tijdens een servicebezoek, kunt u deze wijziging registreren in de servicestuklijst via het formulier Serviceobjecten.</span><span class="sxs-lookup"><span data-stu-id="edaba-110">If you replace a component part of the service object during a service visit, you can register this change in the service BOM by using the Service objects form.</span></span>

## <a name="example"></a><span data-ttu-id="edaba-111">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="edaba-111">Example</span></span>

<span data-ttu-id="edaba-112">U maakt een serviceovereenkomst voor het onderhoud van twee liften op een klantlocatie.</span><span class="sxs-lookup"><span data-stu-id="edaba-112">You create a service agreement for servicing two elevators at a customer site.</span></span>
<span data-ttu-id="edaba-113">Het id van de serviceovereenkomst is ID SAL-001.</span><span class="sxs-lookup"><span data-stu-id="edaba-113">The service agreement has the identifier ID SAL-001.</span></span>

<span data-ttu-id="edaba-114">In het formulier Serviceobjecten zijn de liften ingesteld als de objecten EL-S/1000 en EL-L/1000.</span><span class="sxs-lookup"><span data-stu-id="edaba-114">The elevators are set up in the Service objects form as objects, EL-S/1000 and EL-L/1000.</span></span>

<span data-ttu-id="edaba-115">U koppelt de serviceobjecten EL-S/1000 en EL-L/1000 aan de serviceovereenkomst.</span><span class="sxs-lookup"><span data-stu-id="edaba-115">You attach the service objects, EL-S/1000 and EL-L/1000, to the service agreement.</span></span>

<span data-ttu-id="edaba-116">U wilt de wijzigingen in de stuklijst registreren voor het serviceobject wanneer u onderdelen van het object vervangt. Daarom koppelt u een servicestuklijst aan de serviceobjectrelatie, zoals wordt beschreven in de volgende tabel.</span><span class="sxs-lookup"><span data-stu-id="edaba-116">You want to register changes in the BOM for the service object as you replace component parts of the object, so you attach a service BOM to the service object relation, as described in the following table.</span></span>

| <span data-ttu-id="edaba-117">Serviceobject</span><span class="sxs-lookup"><span data-stu-id="edaba-117">Service object</span></span> | <span data-ttu-id="edaba-118">Relatie - Serviceovereenkomst</span><span class="sxs-lookup"><span data-stu-id="edaba-118">Relation – Service agreement</span></span> | <span data-ttu-id="edaba-119">Servicestuklijst</span><span class="sxs-lookup"><span data-stu-id="edaba-119">Service BOM</span></span>   |
|----------------|------------------------------|---------------|
| <span data-ttu-id="edaba-120">EL-S/1000</span><span class="sxs-lookup"><span data-stu-id="edaba-120">EL-S/1000</span></span>      | <span data-ttu-id="edaba-121">ID SAL-001</span><span class="sxs-lookup"><span data-stu-id="edaba-121">ID SAL-001</span></span>                   | <span data-ttu-id="edaba-122">BOM-EL-S/1000</span><span class="sxs-lookup"><span data-stu-id="edaba-122">BOM-EL-S/1000</span></span> |
| <span data-ttu-id="edaba-123">EL-L/1000</span><span class="sxs-lookup"><span data-stu-id="edaba-123">EL-L/1000</span></span>      | <span data-ttu-id="edaba-124">ID SAL-001</span><span class="sxs-lookup"><span data-stu-id="edaba-124">ID SAL-001</span></span>                   | <span data-ttu-id="edaba-125">BOM-EL-L/1000</span><span class="sxs-lookup"><span data-stu-id="edaba-125">BOM-EL-L/1000</span></span> |

<span data-ttu-id="edaba-126">Aangezien er serviceobjectrelaties voor de overeenkomst zijn, kunt u nu serviceovereenkomstregels met deze objecten maken, zoals wordt weergegeven in de volgende tabel.</span><span class="sxs-lookup"><span data-stu-id="edaba-126">Because there are service object relations for the agreement, you can now create service agreement lines with these objects, as shown in the following table.</span></span>

| <span data-ttu-id="edaba-127">Transactietype</span><span class="sxs-lookup"><span data-stu-id="edaba-127">Transaction type</span></span> | <span data-ttu-id="edaba-128">Categorie</span><span class="sxs-lookup"><span data-stu-id="edaba-128">Category</span></span>           | <span data-ttu-id="edaba-129">Serviceobject</span><span class="sxs-lookup"><span data-stu-id="edaba-129">Service object</span></span> |
|------------------|--------------------|----------------|
| <span data-ttu-id="edaba-130">Uur</span><span class="sxs-lookup"><span data-stu-id="edaba-130">Hour</span></span>             | <span data-ttu-id="edaba-131">Inspectie</span><span class="sxs-lookup"><span data-stu-id="edaba-131">Inspection</span></span>         | <span data-ttu-id="edaba-132">EL-S/1000</span><span class="sxs-lookup"><span data-stu-id="edaba-132">EL-S/1000</span></span>      |
| <span data-ttu-id="edaba-133">Uur</span><span class="sxs-lookup"><span data-stu-id="edaba-133">Hour</span></span>             | <span data-ttu-id="edaba-134">Reiniging tandwielkast</span><span class="sxs-lookup"><span data-stu-id="edaba-134">Gear box cleaning</span></span>  | <span data-ttu-id="edaba-135">EL-S/1000</span><span class="sxs-lookup"><span data-stu-id="edaba-135">EL-S/1000</span></span>      |
| <span data-ttu-id="edaba-136">Artikel</span><span class="sxs-lookup"><span data-stu-id="edaba-136">Item</span></span>             | <span data-ttu-id="edaba-137">Schoonmaakmaterialen</span><span class="sxs-lookup"><span data-stu-id="edaba-137">Cleaning materials</span></span> | <span data-ttu-id="edaba-138">EL-S/1000</span><span class="sxs-lookup"><span data-stu-id="edaba-138">EL-S/1000</span></span>      |
| <span data-ttu-id="edaba-139">Uur</span><span class="sxs-lookup"><span data-stu-id="edaba-139">Hour</span></span>             | <span data-ttu-id="edaba-140">Inspectie</span><span class="sxs-lookup"><span data-stu-id="edaba-140">Inspection</span></span>         | <span data-ttu-id="edaba-141">EL-L/1000</span><span class="sxs-lookup"><span data-stu-id="edaba-141">EL-L/1000</span></span>      |
| <span data-ttu-id="edaba-142">Uur</span><span class="sxs-lookup"><span data-stu-id="edaba-142">Hour</span></span>             | <span data-ttu-id="edaba-143">Reiniging tandwielkast</span><span class="sxs-lookup"><span data-stu-id="edaba-143">Gearbox cleaning</span></span>   | <span data-ttu-id="edaba-144">EL-L/1000</span><span class="sxs-lookup"><span data-stu-id="edaba-144">EL-L/1000</span></span>      |
| <span data-ttu-id="edaba-145">Artikel</span><span class="sxs-lookup"><span data-stu-id="edaba-145">Item</span></span>             | <span data-ttu-id="edaba-146">Schoonmaakmaterialen</span><span class="sxs-lookup"><span data-stu-id="edaba-146">Cleaning materials</span></span> | <span data-ttu-id="edaba-147">EL-L/1000</span><span class="sxs-lookup"><span data-stu-id="edaba-147">EL-L/1000</span></span>      |

<span data-ttu-id="edaba-148">Bij een servicebezoek moet u de tandwielkast voor de lift EL-S/1000 vervangen.</span><span class="sxs-lookup"><span data-stu-id="edaba-148">On a service visit, you have to replace the gearbox for elevator EL-S/1000.</span></span> <span data-ttu-id="edaba-149">Als u een onderdeel van het object wilt vervangen, kunt u de stuklijstontwikkelaar openen via de serviceobjectrelatie die u instelt voor de huidige serviceovereenkomst.</span><span class="sxs-lookup"><span data-stu-id="edaba-149">To replace a component part of the object, you can access the BOM Designer by using the service object relation that you set up for the current service agreement.</span></span>

<span data-ttu-id="edaba-150">De stuklijstontwikkelaar openen via een serviceobjectrelatie</span><span class="sxs-lookup"><span data-stu-id="edaba-150">Access the BOM Designer by using a service object relation</span></span>

1. <span data-ttu-id="edaba-151">Serviceovereenkomsten</span><span class="sxs-lookup"><span data-stu-id="edaba-151">Service agreements</span></span>
2. <span data-ttu-id="edaba-152">Dubbelklik op een serviceovereenkomst of klik op Serviceovereenkomst om een nieuwe serviceovereenkomst te maken.</span><span class="sxs-lookup"><span data-stu-id="edaba-152">Double-click a service agreement, or click Service agreement to create a service agreement.</span></span>
3. <span data-ttu-id="edaba-153">Klik op het tabblad Instellingen.</span><span class="sxs-lookup"><span data-stu-id="edaba-153">Click the Setup tab.</span></span>
4. <span data-ttu-id="edaba-154">Klik op Serviceobjecten om een sjabloonstuklijst te koppelen aan de serviceovereenkomst.</span><span class="sxs-lookup"><span data-stu-id="edaba-154">Click Service objects to attach a template BOM to the service agreement.</span></span>
5. <span data-ttu-id="edaba-155">Klik in het formulier Serviceobjecten op Ontwerper om het formulier Ontwerper te openen als u de sjabloonstuklijst wilt wijzigen.</span><span class="sxs-lookup"><span data-stu-id="edaba-155">In the Service objects form, click Designer to open the Designer form to modify the template BOM.</span></span>

## <a name="automatically-created-service-orders"></a><span data-ttu-id="edaba-156">Automatisch gemaakte serviceorders</span><span class="sxs-lookup"><span data-stu-id="edaba-156">Automatically created service orders</span></span>

<span data-ttu-id="edaba-157">Indien u automatisch serviceorders voor een serviceovereenkomst maakt, worden de serviceobjectrelaties in de overeenkomst ook in de serviceorders gemaakt.</span><span class="sxs-lookup"><span data-stu-id="edaba-157">If you automatically create service orders for a service agreement, the service object relations in the agreement are also created in the service orders.</span></span>

