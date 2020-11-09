---
title: Schakelen tussen leverancierontwerpen
description: In dit onderwerp wordt beschreven hoe u schakelt tussen de integratie van leveranciersgegevens tussen Finance and Operations-apps en Common Data Service.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 09/20/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-09-20
ms.openlocfilehash: 0ecc401706911f8b92146b95bb6415185df8b451
ms.sourcegitcommit: 0a741b131ed71f6345d4219a47cf5f71fec6744b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/13/2020
ms.locfileid: "3997547"
---
# <a name="switch-between-vendor-designs"></a><span data-ttu-id="955ed-103">Schakelen tussen leverancierontwerpen</span><span class="sxs-lookup"><span data-stu-id="955ed-103">Switch between vendor designs</span></span>

[!include [banner](../../includes/banner.md)]



## <a name="vendor-data-flow"></a><span data-ttu-id="955ed-104">Leveranciersgegevensstroom</span><span class="sxs-lookup"><span data-stu-id="955ed-104">Vendor data flow</span></span> 

<span data-ttu-id="955ed-105">Als u ervoor kiest om de entiteit **Rekening** te gebruiken voor de opslag van leveranciers van het type **Organisatie** en de entiteit **Contactpersoon** om leveranciers van het type **Persoon** op te slaan, configureert u de volgende werkstromen.</span><span class="sxs-lookup"><span data-stu-id="955ed-105">If you choose to use the **Account** entity to store vendors of the **Organization** type and the **Contact** entity to store vendors of the **Person** type, configure the following workflows.</span></span> <span data-ttu-id="955ed-106">Anders is deze configuratie niet vereist.</span><span class="sxs-lookup"><span data-stu-id="955ed-106">Otherwise, this configuration isn't required.</span></span>

## <a name="use-the-extended-vendor-design-for-vendors-of-the-organization-type"></a><span data-ttu-id="955ed-107">Het uitgebreide leveranciersontwerp gebruiken voor leveranciers van het type Organisatie</span><span class="sxs-lookup"><span data-stu-id="955ed-107">Use the extended vendor design for vendors of the Organization type</span></span>

<span data-ttu-id="955ed-108">Het oplossingspakket **Dynamics365FinanceExtended** bevat de volgende sjablonen voor werkstroomprocessen.</span><span class="sxs-lookup"><span data-stu-id="955ed-108">The **Dynamics365FinanceExtended** solution package contains the following workflow process templates.</span></span> <span data-ttu-id="955ed-109">U maakt een werkstroom voor elke sjabloon.</span><span class="sxs-lookup"><span data-stu-id="955ed-109">You will create a workflow for each template.</span></span>

+ <span data-ttu-id="955ed-110">Leveranciers maken in entiteit Accounts</span><span class="sxs-lookup"><span data-stu-id="955ed-110">Create Vendors in Accounts Entity</span></span>
+ <span data-ttu-id="955ed-111">Leveranciers maken in entiteit Leveranciers</span><span class="sxs-lookup"><span data-stu-id="955ed-111">Create Vendors in Vendors Entity</span></span>
+ <span data-ttu-id="955ed-112">Leveranciers bijwerken in entiteit Accounts</span><span class="sxs-lookup"><span data-stu-id="955ed-112">Update Vendors in Accounts Entity</span></span>
+ <span data-ttu-id="955ed-113">Leveranciers bijwerken in entiteit Leveranciers</span><span class="sxs-lookup"><span data-stu-id="955ed-113">Update Vendors in Vendors Entity</span></span>

<span data-ttu-id="955ed-114">Ga als volgt te werk om nieuwe werkstroomprocessen te maken op basis van de werkstroomprocessjablonen.</span><span class="sxs-lookup"><span data-stu-id="955ed-114">To create new workflow processes by using the workflow process templates, follow these steps.</span></span>

1. <span data-ttu-id="955ed-115">Maak een nieuw werkstroomproces voor de entiteit **Leverancier** en selecteer de werkstroomprocessjabloon **Leveranciers maken in entiteit Accounts**.</span><span class="sxs-lookup"><span data-stu-id="955ed-115">Create a workflow process for the **Vendor** entity, and select the **Create Vendors in Accounts Entity** workflow process template.</span></span> <span data-ttu-id="955ed-116">Selecteer vervolgens **OK**.</span><span class="sxs-lookup"><span data-stu-id="955ed-116">Then select **OK**.</span></span> <span data-ttu-id="955ed-117">Deze workflow verwerkt het scenario voor het maken van de entiteit **Account**.</span><span class="sxs-lookup"><span data-stu-id="955ed-117">This workflow handles the vendor creation scenario for the **Account** entity.</span></span>

    ![Het werkstroomproces Leveranciers maken in entiteit Accounts](media/create_process.png)

2. <span data-ttu-id="955ed-119">Maak een nieuw werkstroomproces voor de entiteit **Leverancier** en selecteer de werkstroomprocessjabloon **Leveranciers bijwerken in entiteit Accounts**.</span><span class="sxs-lookup"><span data-stu-id="955ed-119">Create a workflow process for the **Vendor** entity, and select the **Update Vendors in Accounts Entity** workflow process template.</span></span> <span data-ttu-id="955ed-120">Selecteer vervolgens **OK**.</span><span class="sxs-lookup"><span data-stu-id="955ed-120">Then select **OK**.</span></span> <span data-ttu-id="955ed-121">Deze workflow verwerkt het scenario voor het bijwerken van de entiteit **Account**.</span><span class="sxs-lookup"><span data-stu-id="955ed-121">This workflow handles the vendor update scenario for the **Account** entity.</span></span>
3. <span data-ttu-id="955ed-122">Maak een nieuw werkstroomproces voor de entiteit **Account** en selecteer de werkstroomprocessjabloon **Leveranciers maken in entiteit Leveranciers**.</span><span class="sxs-lookup"><span data-stu-id="955ed-122">Create a workflow process for the **Account** entity, and select the **Create Vendors in Vendors Entity** workflow process template.</span></span>
4. <span data-ttu-id="955ed-123">Maak een nieuw werkstroomproces voor de entiteit **Account** en selecteer de werkstroomprocessjabloon **Leveranciers bijwerken in entiteit Leveranciers**.</span><span class="sxs-lookup"><span data-stu-id="955ed-123">Create a workflow process for the **Account** entity, and select the **Update Vendors in Vendors Entity** workflow process template.</span></span>
5. <span data-ttu-id="955ed-124">U kunt de werkstromen configureren als realtime werkstromen of werkstromen op de achtergrond, afhankelijk van uw vereisten.</span><span class="sxs-lookup"><span data-stu-id="955ed-124">You can configure the workflows as either real-time workflows or background workflows, depending on your requirements.</span></span> <span data-ttu-id="955ed-125">Als u een werkstroom als een achtergrondwerkstroom wilt configureren, selecteert u **Converteren naar een workflow op de achtergrond**.</span><span class="sxs-lookup"><span data-stu-id="955ed-125">To configure a workflow as a background workflow, select **Convert to a background workflow**.</span></span>

    ![De knop Converteren naar een workflow op de achtergrond](media/background_workflow.png)

6. <span data-ttu-id="955ed-127">Activeer de werkstromen die u hebt gemaakt voor de entiteiten **Account** en **Leverancier** om de entiteit **Account** te gebruiken voor het opslaan van leveranciersgegevens van het type **Organisatie**.</span><span class="sxs-lookup"><span data-stu-id="955ed-127">Activate the workflows that you created for the **Account** and **Vendor** entities to start to use the **Account** entity to store information for vendors of the **Organization** type.</span></span>

## <a name="use-the-extended-vendor-design-for-vendors-of-the-person-type"></a><span data-ttu-id="955ed-128">Het uitgebreide leveranciersontwerp gebruiken voor leveranciers van het type Persoon</span><span class="sxs-lookup"><span data-stu-id="955ed-128">Use the extended vendor design for vendors of the Person type</span></span>

<span data-ttu-id="955ed-129">Het oplossingspakket **Dynamics365FinanceExtended** bevat de volgende sjablonen voor werkstroomprocessen.</span><span class="sxs-lookup"><span data-stu-id="955ed-129">The **Dynamics365FinanceExtended** solution package contains the following workflow process templates.</span></span> <span data-ttu-id="955ed-130">U maakt een werkstroom voor elke sjabloon.</span><span class="sxs-lookup"><span data-stu-id="955ed-130">You will create a workflow for each template.</span></span>

+ <span data-ttu-id="955ed-131">Leveranciers van het type Persoon maken in entiteit Leveranciers</span><span class="sxs-lookup"><span data-stu-id="955ed-131">Create Vendors of type Person in Vendors Entity</span></span>
+ <span data-ttu-id="955ed-132">Leveranciers van het type Persoon maken in entiteit Contactpersonen</span><span class="sxs-lookup"><span data-stu-id="955ed-132">Create Vendors of type Person in Contacts Entity</span></span>
+ <span data-ttu-id="955ed-133">Leveranciers van het type Persoon bijwerken in entiteit Contactpersonen</span><span class="sxs-lookup"><span data-stu-id="955ed-133">Update Vendors of type Person in Contacts Entity</span></span>
+ <span data-ttu-id="955ed-134">Leveranciers van het type Persoon bijwerken in entiteit Leveranciers</span><span class="sxs-lookup"><span data-stu-id="955ed-134">Update Vendors of type Person in Vendors Entity</span></span>

<span data-ttu-id="955ed-135">Ga als volgt te werk om nieuwe werkstroomprocessen te maken op basis van de werkstroomprocessjablonen.</span><span class="sxs-lookup"><span data-stu-id="955ed-135">To create new workflow processes by using the workflow process templates, follow these steps.</span></span>

1. <span data-ttu-id="955ed-136">Maak een nieuw werkstroomproces voor de entiteit **Leverancier** en selecteer de werkstroomprocessjabloon **Leveranciers van het type Persoon maken in entiteit Contactpersonen**.</span><span class="sxs-lookup"><span data-stu-id="955ed-136">Create a workflow process for the **Vendor** entity, and select the **Create Vendors of type Person in Contacts Entity** workflow process template.</span></span> <span data-ttu-id="955ed-137">Selecteer vervolgens **OK**.</span><span class="sxs-lookup"><span data-stu-id="955ed-137">Then select **OK**.</span></span> <span data-ttu-id="955ed-138">Deze werkstroom verwerkt het scenario voor het maken van de entiteit **Contactpersoon**.</span><span class="sxs-lookup"><span data-stu-id="955ed-138">This workflow handles the vendor creation scenario for the **Contact** entity.</span></span>
2. <span data-ttu-id="955ed-139">Maak een nieuw werkstroomproces voor de entiteit **Leverancier** en selecteer de werkstroomprocessjabloon **Leveranciers van het type Persoon bijwerken in entiteit Contactpersonen**.</span><span class="sxs-lookup"><span data-stu-id="955ed-139">Create a workflow process for the **Vendor** entity, and select the **Update Vendors of type Person in Contacts Entity** workflow process template.</span></span> <span data-ttu-id="955ed-140">Selecteer vervolgens **OK**.</span><span class="sxs-lookup"><span data-stu-id="955ed-140">Then select **OK**.</span></span> <span data-ttu-id="955ed-141">Deze werkstroom verwerkt het scenario voor het bijwerken van de entiteit **Contactpersoon**.</span><span class="sxs-lookup"><span data-stu-id="955ed-141">This workflow handles the vendor update scenario for the **Contact** entity.</span></span>
3. <span data-ttu-id="955ed-142">Maak een nieuw werkstroomproces voor de entiteit **Contactpersoon** en selecteer de sjabloon **Leveranciers van het type Persoon maken in entiteit Leveranciers**.</span><span class="sxs-lookup"><span data-stu-id="955ed-142">Create a workflow process for the **Contact** entity, and select the **Create Vendors of type Person in Vendors Entity** template.</span></span>
4. <span data-ttu-id="955ed-143">Maak een nieuw werkstroomproces voor de entiteit **Contactpersoon** en selecteer de sjabloon **Leveranciers van het type Persoon bijwerken in entiteit Leveranciers**.</span><span class="sxs-lookup"><span data-stu-id="955ed-143">Create a workflow process for the **Contact** entity, and select the **Update Vendors of type Person in Vendors Entity** template.</span></span>
5. <span data-ttu-id="955ed-144">U kunt de werkstromen configureren als realtime werkstromen of werkstromen op de achtergrond, afhankelijk van uw vereisten.</span><span class="sxs-lookup"><span data-stu-id="955ed-144">You can configure the workflows as either real-time workflows or background workflows, depending on your requirements.</span></span> <span data-ttu-id="955ed-145">Als u een werkstroom als een achtergrondwerkstroom wilt configureren, selecteert u **Converteren naar een workflow op de achtergrond**.</span><span class="sxs-lookup"><span data-stu-id="955ed-145">To configure a workflow as a background workflow, select **Convert to a background workflow**.</span></span>
6. <span data-ttu-id="955ed-146">Activeer de werkstromen die u hebt gemaakt voor de entiteiten **Contactpersoon** en **Leverancier** om de entiteit **Contactpersoon** te gebruiken voor het opslaan van leveranciersgegevens van het type **Persoon**.</span><span class="sxs-lookup"><span data-stu-id="955ed-146">Activate the workflows that you created on the **Contact** and **Vendor** entities to start to use the **Contact** entity to store information for vendors of the **Person** type.</span></span>
