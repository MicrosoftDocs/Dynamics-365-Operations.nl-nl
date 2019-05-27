---
title: Relaties van serviceobjecten maken
description: Dit onderwerp beschrijft hoe u serviceobjectrelaties kunt maken voor een serviceovereenkomst en serviceorder.
author: ShylaThompson
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable, SMAAgreementTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 792ceea52a9caa1a99217c77bb3fe4aafb80a0eb
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/15/2019
ms.locfileid: "1555008"
---
# <a name="create-service-object-relations"></a><span data-ttu-id="941cf-103">Relaties van serviceobjecten maken</span><span class="sxs-lookup"><span data-stu-id="941cf-103">Create service object relations</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="941cf-104">Dit onderwerp beschrijft hoe u serviceobjectrelaties kunt maken voor een serviceovereenkomst en serviceorder.</span><span class="sxs-lookup"><span data-stu-id="941cf-104">This topic describes how to create service object relations for a service agreement and a service order.</span></span> <span data-ttu-id="941cf-105">Wanneer u een serviceobjectrelatie maakt, koppelt u het serviceobject aan een serviceovereenkomst of serviceorder.</span><span class="sxs-lookup"><span data-stu-id="941cf-105">When you a create service object relation, you associate the service object to a service agreement or service order.</span></span> <span data-ttu-id="941cf-106">Wanneer een klant om service voor een artikel aanvraagt dat een serviceobject is, kunt u het serviceobject van de lijst van serviceobjectrelaties selecteren.</span><span class="sxs-lookup"><span data-stu-id="941cf-106">When a customer requests service for an item that is a service object, you can select the service object from the list of service object relations.</span></span>

## <a name="create-a-service-object-relation-for-a-service-agreement"></a><span data-ttu-id="941cf-107">Een serviceobjectrelatie maken voor een serviceovereenkomst</span><span class="sxs-lookup"><span data-stu-id="941cf-107">Create a service object relation for a service agreement</span></span>

<span data-ttu-id="941cf-108">Gebruik de volgende stappen om een nieuwe serviceobjectrelatie te maken voor een serviceovereenkomst:</span><span class="sxs-lookup"><span data-stu-id="941cf-108">Use the following steps to create a service object relation for a service agreement:</span></span>

1.  <span data-ttu-id="941cf-109">Klik op **Servicebeheer** \> **Algemeen** \> **Serviceovereenkomsten** \> **Serviceovereenkomsten**.</span><span class="sxs-lookup"><span data-stu-id="941cf-109">Click **Service management** \> **Common** \> **Service agreements** \> **Service agreements**.</span></span>

2.  <span data-ttu-id="941cf-110">In de lijst **Serviceovereenkomsten** selecteert u een bestaande serviceovereenkomst of klikt u op **Nieuw** om een nieuwe serviceovereenkomst te maken.</span><span class="sxs-lookup"><span data-stu-id="941cf-110">In the **Service agreements** list, select an existing service agreement, or click **New** to create a new service agreement.</span></span>

3.  <span data-ttu-id="941cf-111">Klik in het formulier **Serviceovereenkomsten** in het **Actievenster** op het tabblad **Serviceovereenkomst** in de groep **Relaties** op **Serviceobjecten**.</span><span class="sxs-lookup"><span data-stu-id="941cf-111">In the **Service agreements** form, on the **Action Pane**, on the **Service agreement** tab, in the **Relations** group, click **Service objects**.</span></span>

4.  <span data-ttu-id="941cf-112">Klik in het formulier **Serviceobjecten** op **Nieuw** en selecteer vervolgens een serviceobject voor deze serviceovereenkomst.</span><span class="sxs-lookup"><span data-stu-id="941cf-112">In the **Service objects** form, click **New**, and then select a service object for this service agreement.</span></span>

5.  <span data-ttu-id="941cf-113">Klik op **Functies** en selecteer vervolgens **Sjabloonstuklijst toevoegen** om een sjabloonstuklijst aan de serviceovereenkomst te koppelen.</span><span class="sxs-lookup"><span data-stu-id="941cf-113">To assign a template bill of materials (BOM) to the service agreement, click **Functions**, and then select **Attach template BOM**.</span></span> <span data-ttu-id="941cf-114">Selecteer een sjabloon in het formulier **Sjabloonstuklijst selecteren** in het veld **Sjabloonstuklijst**.</span><span class="sxs-lookup"><span data-stu-id="941cf-114">In the **Select template BOM** form, in the **Template BOM** field, select a template.</span></span> 

## <a name="create-a-service-object-relation-for-a-service-order"></a><span data-ttu-id="941cf-115">Een serviceobjectrelatie maken voor een serviceorder</span><span class="sxs-lookup"><span data-stu-id="941cf-115">Create a service object relation for a service order</span></span>

<span data-ttu-id="941cf-116">Gebruik de volgende stappen om een nieuwe serviceobjectrelatie te maken voor een serviceorder:</span><span class="sxs-lookup"><span data-stu-id="941cf-116">Use the following steps to create a service object relation for a service order:</span></span>

1.  <span data-ttu-id="941cf-117">Klik op **Servicebeheer** \> **Algemeen** \> **Serviceorders** \> **Serviceorders**.</span><span class="sxs-lookup"><span data-stu-id="941cf-117">Click **Service management** \> **Common** \> **Service orders** \> **Service orders**.</span></span>

2.  <span data-ttu-id="941cf-118">Selecteer in de lijst **Serviceorders** een bestaande serviceorder of maak een nieuwe serviceorder.</span><span class="sxs-lookup"><span data-stu-id="941cf-118">In the **Service orders** list, select an existing service order, or create a new service order.</span></span>

3.  <span data-ttu-id="941cf-119">Klik in het formulier **Serviceorders** in het **Actievenster** op het tabblad **Serviceorder** in de groep **Relaties** op **Serviceobjecten**.</span><span class="sxs-lookup"><span data-stu-id="941cf-119">In the **Service orders** form, on the **Action Pane**, on the **Service order** tab, in the **Relations** group, click **Service objects**.</span></span>

4.  <span data-ttu-id="941cf-120">Klik in het formulier **Serviceobjecten** op **Nieuw** en selecteer vervolgens een serviceobject voor deze serviceorder.</span><span class="sxs-lookup"><span data-stu-id="941cf-120">In the **Service objects** form, click **New**, and then select a service object for this service order.</span></span>

5.  <span data-ttu-id="941cf-121">Klik op **Functies** en selecteer vervolgens **Sjabloonstuklijst toevoegen** om een sjabloonstuklijst aan de serviceovereenkomst toe te wijzen.</span><span class="sxs-lookup"><span data-stu-id="941cf-121">To assign a template BOM to the service agreement, click **Functions**, and then select **Attach template BOM**.</span></span> <span data-ttu-id="941cf-122">Selecteer een sjabloon in het formulier **Sjabloonstuklijst selecteren** in het veld **Sjabloonstuklijst**.</span><span class="sxs-lookup"><span data-stu-id="941cf-122">In the **Select template BOM** form, in the **Template BOM** field, select a template.</span></span> 


## <a name="see-also"></a><span data-ttu-id="941cf-123">Zie ook</span><span class="sxs-lookup"><span data-stu-id="941cf-123">See also</span></span>

[<span data-ttu-id="941cf-124">Serviceobjecten</span><span class="sxs-lookup"><span data-stu-id="941cf-124">Service objects</span></span>](service-objects.md)

[<span data-ttu-id="941cf-125">serviceobjectrelaties</span><span class="sxs-lookup"><span data-stu-id="941cf-125">service object relations</span></span>](service-object-relations.md)

[<span data-ttu-id="941cf-126">Sjabloonstuklijsten</span><span class="sxs-lookup"><span data-stu-id="941cf-126">Template BOMs</span></span>](template-boms.md)

  


