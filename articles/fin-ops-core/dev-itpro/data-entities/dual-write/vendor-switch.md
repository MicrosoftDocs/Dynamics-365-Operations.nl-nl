---
title: Schakelen tussen leverancierontwerpen
description: In dit onderwerp wordt beschreven hoe u schakelt tussen de integratie van leveranciersgegevens tussen Finance and Operations-apps en Dataverse.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 09/20/2019
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 78d4c547f544d95c66490e5610374a5c4598b266
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/09/2021
ms.locfileid: "5565594"
---
# <a name="switch-between-vendor-designs"></a><span data-ttu-id="f9170-103">Schakelen tussen leverancierontwerpen</span><span class="sxs-lookup"><span data-stu-id="f9170-103">Switch between vendor designs</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



## <a name="vendor-data-flow"></a><span data-ttu-id="f9170-104">Leveranciersgegevensstroom</span><span class="sxs-lookup"><span data-stu-id="f9170-104">Vendor data flow</span></span> 

<span data-ttu-id="f9170-105">Als u ervoor kiest om de tabel **Rekening** te gebruiken voor de opslag van leveranciers van het type **Organisatie** en de tabel **Contactpersoon** om leveranciers van het type **Persoon** op te slaan, configureert u de volgende werkstromen.</span><span class="sxs-lookup"><span data-stu-id="f9170-105">If you choose to use the **Account** table to store vendors of the **Organization** type and the **Contact** table to store vendors of the **Person** type, configure the following workflows.</span></span> <span data-ttu-id="f9170-106">Anders is deze configuratie niet vereist.</span><span class="sxs-lookup"><span data-stu-id="f9170-106">Otherwise, this configuration isn't required.</span></span>

## <a name="use-the-extended-vendor-design-for-vendors-of-the-organization-type"></a><span data-ttu-id="f9170-107">Het uitgebreide leveranciersontwerp gebruiken voor leveranciers van het type Organisatie</span><span class="sxs-lookup"><span data-stu-id="f9170-107">Use the extended vendor design for vendors of the Organization type</span></span>

<span data-ttu-id="f9170-108">Het oplossingspakket **Dynamics365FinanceExtended** bevat de volgende sjablonen voor werkstroomprocessen.</span><span class="sxs-lookup"><span data-stu-id="f9170-108">The **Dynamics365FinanceExtended** solution package contains the following workflow process templates.</span></span> <span data-ttu-id="f9170-109">U maakt een werkstroom voor elke sjabloon.</span><span class="sxs-lookup"><span data-stu-id="f9170-109">You will create a workflow for each template.</span></span>

+ <span data-ttu-id="f9170-110">Leveranciers maken in tabel Accounts</span><span class="sxs-lookup"><span data-stu-id="f9170-110">Create Vendors in Accounts Table</span></span>
+ <span data-ttu-id="f9170-111">Leveranciers maken in tabel Leveranciers</span><span class="sxs-lookup"><span data-stu-id="f9170-111">Create Vendors in Vendors Table</span></span>
+ <span data-ttu-id="f9170-112">Leveranciers bijwerken in tabel Accounts</span><span class="sxs-lookup"><span data-stu-id="f9170-112">Update Vendors in Accounts Table</span></span>
+ <span data-ttu-id="f9170-113">Leveranciers bijwerken in tabel Leveranciers</span><span class="sxs-lookup"><span data-stu-id="f9170-113">Update Vendors in Vendors Table</span></span>

<span data-ttu-id="f9170-114">Ga als volgt te werk om nieuwe werkstroomprocessen te maken op basis van de werkstroomprocessjablonen.</span><span class="sxs-lookup"><span data-stu-id="f9170-114">To create new workflow processes by using the workflow process templates, follow these steps.</span></span>

1. <span data-ttu-id="f9170-115">Maak een werkstroomproces voor de tabel **Leverancier** en selecteer de werkstroomprocessjabloon **Leveranciers maken in tabel Rekeningen**.</span><span class="sxs-lookup"><span data-stu-id="f9170-115">Create a workflow process for the **Vendor** table, and select the **Create Vendors in Accounts Table** workflow process template.</span></span> <span data-ttu-id="f9170-116">Selecteer vervolgens **OK**.</span><span class="sxs-lookup"><span data-stu-id="f9170-116">Then select **OK**.</span></span> <span data-ttu-id="f9170-117">Deze werkstroom verwerkt het scenario voor het maken van de tabel **Rekening**.</span><span class="sxs-lookup"><span data-stu-id="f9170-117">This workflow handles the vendor creation scenario for the **Account** table.</span></span>

    ![Het werkstroomproces Leveranciers maken in tabel Accounts](media/create_process.png)

2. <span data-ttu-id="f9170-119">Maak een werkstroomproces voor de tabel **Leverancier** en selecteer de werkstroomprocessjabloon **Leveranciers bijwerken in tabel Rekeningen**.</span><span class="sxs-lookup"><span data-stu-id="f9170-119">Create a workflow process for the **Vendor** table, and select the **Update Vendors in Accounts Table** workflow process template.</span></span> <span data-ttu-id="f9170-120">Selecteer vervolgens **OK**.</span><span class="sxs-lookup"><span data-stu-id="f9170-120">Then select **OK**.</span></span> <span data-ttu-id="f9170-121">Deze werkstroom verwerkt het scenario voor het bijwerken van de tabel **Rekening**.</span><span class="sxs-lookup"><span data-stu-id="f9170-121">This workflow handles the vendor update scenario for the **Account** table.</span></span>
3. <span data-ttu-id="f9170-122">Maak een werkstroomproces voor de tabel **Rekening** en selecteer de werkstroomprocessjabloon **Leveranciers maken in tabel Leveranciers**.</span><span class="sxs-lookup"><span data-stu-id="f9170-122">Create a workflow process for the **Account** table, and select the **Create Vendors in Vendors Table** workflow process template.</span></span>
4. <span data-ttu-id="f9170-123">Maak een werkstroomproces voor de tabel **Rekening** en selecteer de werkstroomprocessjabloon **Leveranciers bijwerken in tabel Leveranciers**.</span><span class="sxs-lookup"><span data-stu-id="f9170-123">Create a workflow process for the **Account** table, and select the **Update Vendors in Vendors Table** workflow process template.</span></span>
5. <span data-ttu-id="f9170-124">U kunt de werkstromen configureren als realtime werkstromen of werkstromen op de achtergrond, afhankelijk van uw vereisten.</span><span class="sxs-lookup"><span data-stu-id="f9170-124">You can configure the workflows as either real-time workflows or background workflows, depending on your requirements.</span></span> <span data-ttu-id="f9170-125">Als u een werkstroom als een achtergrondwerkstroom wilt configureren, selecteert u **Converteren naar een workflow op de achtergrond**.</span><span class="sxs-lookup"><span data-stu-id="f9170-125">To configure a workflow as a background workflow, select **Convert to a background workflow**.</span></span>

    ![De knop Converteren naar een workflow op de achtergrond](media/background_workflow.png)

6. <span data-ttu-id="f9170-127">Activeer de werkstromen die u hebt gemaakt voor de tabellen **Rekening** en **Leverancier** om de tabel **Rekening** te gebruiken voor het opslaan van leveranciersgegevens van het type **Organisatie**.</span><span class="sxs-lookup"><span data-stu-id="f9170-127">Activate the workflows that you created for the **Account** and **Vendor** tables to start to use the **Account** table to store information for vendors of the **Organization** type.</span></span>

## <a name="use-the-extended-vendor-design-for-vendors-of-the-person-type"></a><span data-ttu-id="f9170-128">Het uitgebreide leveranciersontwerp gebruiken voor leveranciers van het type Persoon</span><span class="sxs-lookup"><span data-stu-id="f9170-128">Use the extended vendor design for vendors of the Person type</span></span>

<span data-ttu-id="f9170-129">Het oplossingspakket **Dynamics365FinanceExtended** bevat de volgende sjablonen voor werkstroomprocessen.</span><span class="sxs-lookup"><span data-stu-id="f9170-129">The **Dynamics365FinanceExtended** solution package contains the following workflow process templates.</span></span> <span data-ttu-id="f9170-130">U maakt een werkstroom voor elke sjabloon.</span><span class="sxs-lookup"><span data-stu-id="f9170-130">You will create a workflow for each template.</span></span>

+ <span data-ttu-id="f9170-131">Leveranciers van het type Persoon maken in tabel Leveranciers</span><span class="sxs-lookup"><span data-stu-id="f9170-131">Create Vendors of type Person in Vendors Table</span></span>
+ <span data-ttu-id="f9170-132">Leveranciers van het type Persoon maken in tabel Contactpersonen</span><span class="sxs-lookup"><span data-stu-id="f9170-132">Create Vendors of type Person in Contacts Table</span></span>
+ <span data-ttu-id="f9170-133">Leveranciers van het type Persoon bijwerken in tabel Contactpersonen</span><span class="sxs-lookup"><span data-stu-id="f9170-133">Update Vendors of type Person in Contacts Table</span></span>
+ <span data-ttu-id="f9170-134">Leveranciers van het type Persoon bijwerken in tabel Leveranciers</span><span class="sxs-lookup"><span data-stu-id="f9170-134">Update Vendors of type Person in Vendors Table</span></span>

<span data-ttu-id="f9170-135">Ga als volgt te werk om nieuwe werkstroomprocessen te maken op basis van de werkstroomprocessjablonen.</span><span class="sxs-lookup"><span data-stu-id="f9170-135">To create new workflow processes by using the workflow process templates, follow these steps.</span></span>

1. <span data-ttu-id="f9170-136">Maak een werkstroomproces voor de tabel **Leverancier** en selecteer de werkstroomprocessjabloon **Leveranciers van het type Persoon maken in tabel Contactpersonen**.</span><span class="sxs-lookup"><span data-stu-id="f9170-136">Create a workflow process for the **Vendor** table, and select the **Create Vendors of type Person in Contacts Table** workflow process template.</span></span> <span data-ttu-id="f9170-137">Selecteer vervolgens **OK**.</span><span class="sxs-lookup"><span data-stu-id="f9170-137">Then select **OK**.</span></span> <span data-ttu-id="f9170-138">Deze werkstroom verwerkt het scenario voor het maken van de tabel **Contactpersoon**.</span><span class="sxs-lookup"><span data-stu-id="f9170-138">This workflow handles the vendor creation scenario for the **Contact** table.</span></span>
2. <span data-ttu-id="f9170-139">Maak een nieuw werkstroomproces voor de tabel **Leverancier** en selecteer de werkstroomprocessjabloon **Leveranciers van het type Persoon bijwerken in tabel Contactpersonen**.</span><span class="sxs-lookup"><span data-stu-id="f9170-139">Create a workflow process for the **Vendor** table, and select the **Update Vendors of type Person in Contacts Table** workflow process template.</span></span> <span data-ttu-id="f9170-140">Selecteer vervolgens **OK**.</span><span class="sxs-lookup"><span data-stu-id="f9170-140">Then select **OK**.</span></span> <span data-ttu-id="f9170-141">Deze werkstroom verwerkt het scenario voor het bijwerken van de tabel **Contactpersoon**.</span><span class="sxs-lookup"><span data-stu-id="f9170-141">This workflow handles the vendor update scenario for the **Contact** table.</span></span>
3. <span data-ttu-id="f9170-142">Maak een werkstroomproces voor de tabel **Contactpersoon** en selecteer de sjabloon **Leveranciers van het type Persoon maken in tabel Leveranciers**.</span><span class="sxs-lookup"><span data-stu-id="f9170-142">Create a workflow process for the **Contact** table, and select the **Create Vendors of type Person in Vendors Table** template.</span></span>
4. <span data-ttu-id="f9170-143">Maak een werkstroomproces voor de tabel **Contactpersoon** en selecteer de sjabloon **Leveranciers van het type Persoon bijwerken in tabel Leveranciers**.</span><span class="sxs-lookup"><span data-stu-id="f9170-143">Create a workflow process for the **Contact** table, and select the **Update Vendors of type Person in Vendors Table** template.</span></span>
5. <span data-ttu-id="f9170-144">U kunt de werkstromen configureren als realtime werkstromen of werkstromen op de achtergrond, afhankelijk van uw vereisten.</span><span class="sxs-lookup"><span data-stu-id="f9170-144">You can configure the workflows as either real-time workflows or background workflows, depending on your requirements.</span></span> <span data-ttu-id="f9170-145">Als u een werkstroom als een achtergrondwerkstroom wilt configureren, selecteert u **Converteren naar een workflow op de achtergrond**.</span><span class="sxs-lookup"><span data-stu-id="f9170-145">To configure a workflow as a background workflow, select **Convert to a background workflow**.</span></span>
6. <span data-ttu-id="f9170-146">Activeer de werkstromen die u hebt gemaakt voor de tabellen **Contactpersoon** en **Leverancier** om de tabel **Contactpersoon** te gebruiken voor het opslaan van leveranciersgegevens van het type **Persoon**.</span><span class="sxs-lookup"><span data-stu-id="f9170-146">Activate the workflows that you created on the **Contact** and **Vendor** tables to start to use the **Contact** table to store information for vendors of the **Person** type.</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]