---
title: Serviceovereenkomsten maken
description: In dit onderwerp wordt beschreven hoe u serviceovereenkomsten maakt met de functies in de modules Servicebeheer en Projectbeheer en boekhouding.
author: ShylaThompson
manager: AnnBe
ms.date: 02/19/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMAAgreementTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: a094ce9f0d9323b089055e74d41cf1f45323a7d4
ms.contentlocale: nl-nl
ms.lasthandoff: 08/07/2018

---

# <a name="create-service-agreements"></a><span data-ttu-id="8e914-103">Serviceovereenkomsten maken</span><span class="sxs-lookup"><span data-stu-id="8e914-103">Create service agreements</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8e914-104">In dit onderwerp wordt beschreven hoe u serviceovereenkomsten maakt met de functies in de modules Servicebeheer en Projectbeheer en boekhouding.</span><span class="sxs-lookup"><span data-stu-id="8e914-104">This topic describes how to use features in the Service management and the Project management and accounting modules to create service agreements.</span></span>

## <a name="create-a-service-agreement-from-service-management"></a><span data-ttu-id="8e914-105">Een serviceovereenkomst maken via Servicebeheer</span><span class="sxs-lookup"><span data-stu-id="8e914-105">Create a service agreement from Service management</span></span>

1. <span data-ttu-id="8e914-106">Ga naar **Servicebeheer**.</span><span class="sxs-lookup"><span data-stu-id="8e914-106">Navigate to **Service management**.</span></span>
2. <span data-ttu-id="8e914-107">Klik op **Serviceovereenkomsten** om in de koptekst van de pagina een nieuwe serviceovereenkomstregel te maken.</span><span class="sxs-lookup"><span data-stu-id="8e914-107">Click **Service agreements** to create a new service agreement line in the page header.</span></span> 
3. <span data-ttu-id="8e914-108">Klik op **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="8e914-108">Click **New**.</span></span> <span data-ttu-id="8e914-109">Voer een omschrijving in, selecteer een verwijzing naar een project in het veld **Project-id** en vul de rest van de velden en regels voor de serviceovereenkomst in.</span><span class="sxs-lookup"><span data-stu-id="8e914-109">Enter a description, select a reference to a project in the **Project ID** field, and fill in the rest of the fields and lines for the service agreement.</span></span> <span data-ttu-id="8e914-110">Klik op **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="8e914-110">Click **Save**.</span></span>
4. <span data-ttu-id="8e914-111">Selecteer op het tabblad **Relaties** de optie **Serviceobjecten** of **Servicetaken** om serviceobject- of servicetaakrelaties voor de serviceovereenkomst te maken.</span><span class="sxs-lookup"><span data-stu-id="8e914-111">On the **Relations** tab, select **Service objects** or **Service tasks** to create service object relations or service task relations for the service agreement.</span></span> <span data-ttu-id="8e914-112">U kunt de serviceobjecten en -taken waarvoor u relaties hebt gemaakt, toevoegen aan de regels van de serviceovereenkomst.</span><span class="sxs-lookup"><span data-stu-id="8e914-112">The service objects and tasks that you have created relations for can be attached on the lines of the service agreement.</span></span>
5. <span data-ttu-id="8e914-113">Maak serviceovereenkomstregels in het onderste deel van de pagina door regels te kopiëren uit een servicesjabloon of een andere serviceovereenkomst of door de serviceovereenkomstregels handmatig te maken.</span><span class="sxs-lookup"><span data-stu-id="8e914-113">In the lower half of the page, create service agreement lines by copying lines from a service template, another service agreement, or manually creating the service-agreement lines.</span></span>

> [!NOTE]
> <span data-ttu-id="8e914-114">Als u regels vanuit een andere serviceovereenkomst kopieert naar de desbetreffende serviceovereenkomst, kunt u aangeven of u ook serviceobject- en servicetaakrelaties wilt kopiëren.</span><span class="sxs-lookup"><span data-stu-id="8e914-114">If you copy lines into the service agreement from another service agreement, you can indicate whether you also want to copy service object and service task relations.</span></span> <span data-ttu-id="8e914-115">Als u deze relaties kopieert, worden deze toegevoegd aan de bestaande relaties in de serviceovereenkomst.</span><span class="sxs-lookup"><span data-stu-id="8e914-115">If you copy these relations, they are added to any existing relations on the service agreement.</span></span> <span data-ttu-id="8e914-116">Als u serviceovereenkomstregels kopieert uit een servicesjabloon, worden de serviceobject- en servicetaakrelaties automatisch naar de nieuwe serviceovereenkomstregels gekopieerd als serviceobjectrelaties en servicetaakrelaties.</span><span class="sxs-lookup"><span data-stu-id="8e914-116">If you copy service-agreement lines from a service template, the service-object and service-task relations are automatically copied as service-object relations and service-task relations on the new service-agreement lines.</span></span>

## <a name="create-service-agreement-lines-manually"></a><span data-ttu-id="8e914-117">Handmatig serviceovereenkomstregels maken</span><span class="sxs-lookup"><span data-stu-id="8e914-117">Create service agreement lines manually</span></span>

1. <span data-ttu-id="8e914-118">Voeg vanaf de pagina **Serviceovereenkomsten** een serviceovereenkomstregel toe in het lijnenraster.</span><span class="sxs-lookup"><span data-stu-id="8e914-118">From the **Service agreements** page, add a service agreement line in the lines grid.</span></span> 
2. <span data-ttu-id="8e914-119">Voer de juiste gegevens voor de serviceovereenkomstregel in.</span><span class="sxs-lookup"><span data-stu-id="8e914-119">Enter the appropriate information for the service agreement line.</span></span> 
3. <span data-ttu-id="8e914-120">Druk op **CTRL+S** om de regel op te slaan en sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="8e914-120">Press **CTRL+S** to save the line, and then close the page.</span></span>

## <a name="create-a-service-agreement-from-project"></a><span data-ttu-id="8e914-121">Een serviceovereenkomst maken via Project</span><span class="sxs-lookup"><span data-stu-id="8e914-121">Create a service agreement from Project</span></span>

1. <span data-ttu-id="8e914-122">Klik op **Projectbeheer en boekhouding**.</span><span class="sxs-lookup"><span data-stu-id="8e914-122">Click **Project management and accounting**.</span></span>
2. <span data-ttu-id="8e914-123">Klik op **Alle projecten**.</span><span class="sxs-lookup"><span data-stu-id="8e914-123">Click **All projects**.</span></span>
3. <span data-ttu-id="8e914-124">Selecteer het project in de lijst.</span><span class="sxs-lookup"><span data-stu-id="8e914-124">Select the project from the list.</span></span>
4. <span data-ttu-id="8e914-125">Klik in het **actievenster** op **Beheren**.</span><span class="sxs-lookup"><span data-stu-id="8e914-125">On the **Action Pane**, click **Manage**.</span></span> <span data-ttu-id="8e914-126">Klik in de groep **Nieuwe actie** op **Service** en selecteer **Serviceovereenkomst**.</span><span class="sxs-lookup"><span data-stu-id="8e914-126">In the **New** Action group, click **Service** and select **Service agreement**.</span></span>
5. <span data-ttu-id="8e914-127">Voer de beschreven stappen in de sectie **Een serviceovereenkomst maken** uit om de projectverwijzing in te voeren.</span><span class="sxs-lookup"><span data-stu-id="8e914-127">Follow the steps in the section titled **Create a service agreement** as described earlier in this topic to enter the project reference.</span></span>


## <a name="related-topics"></a><span data-ttu-id="8e914-128">Verwante onderwerpen</span><span class="sxs-lookup"><span data-stu-id="8e914-128">Related topics</span></span>

[<span data-ttu-id="8e914-129">Serviceovereenkomsten</span><span class="sxs-lookup"><span data-stu-id="8e914-129">Service agreements</span></span>](service-agreements.md)



