---
title: Locatie en partijrelatietypen toevoegen
description: In dit onderwerp wordt uitgelegd hoe u een nieuwe locatie en partijrelatietype toevoegt.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 13991
ms.assetid: 2a0a4789-8619-4974-bef9-0923cc848420
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2018-05-02
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: e38d0bd75ad865b7885182f798beb43551576beb
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/13/2020
ms.locfileid: "4441992"
---
# <a name="add-location-and-party-relationship-types"></a><span data-ttu-id="46be2-103">Locatie en partijrelatietypen toevoegen</span><span class="sxs-lookup"><span data-stu-id="46be2-103">Add location and party relationship types</span></span> 

[!include [banner](../includes/banner.md)]

## <a name="add-location-roles"></a><span data-ttu-id="46be2-104">Locatierollen toevoegen</span><span class="sxs-lookup"><span data-stu-id="46be2-104">Add location roles</span></span>

<span data-ttu-id="46be2-105">Er zijn twee manieren voor het toevoegen van nieuwe locatierollen voor adres- en contactgegevens:</span><span class="sxs-lookup"><span data-stu-id="46be2-105">There are two ways to add a new location roles for address and contact information:</span></span>

-  <span data-ttu-id="46be2-106">Voeg het toe met de pagina **Doel van adres- en contactgegevens**.</span><span class="sxs-lookup"><span data-stu-id="46be2-106">Add it through the **Address and contact information purpose** page.</span></span> <span data-ttu-id="46be2-107">De nieuwe rol wordt opgeslagen in de tabel **LogisticsLocationRole** met type = 0, waarmee wordt aangegeven dat de rol geen systeemrol is die is gedefinieerd in de opsomming **LogisticsLocationRoleType** en de extensies ervan.</span><span class="sxs-lookup"><span data-stu-id="46be2-107">The new role will be saved to the **LogisticsLocationRole** table with type = 0, which indicates that the role is not a system role defined in the **LogisticsLocationRoleType** enum and its extensions.</span></span> <span data-ttu-id="46be2-108">Een gebruiker kan deze rol gebruiken bij het maken van adres- of contactpersoongegevens.</span><span class="sxs-lookup"><span data-stu-id="46be2-108">A user will be able to use this role when creating address or contact information.</span></span>

    ![Doel van adres- en inhoudsgegevens](media/Address-Contact.PNG)

-  <span data-ttu-id="46be2-110">Voeg het toe aan de opsommingsextensie **LogisticsLocationRoleType** en laat het vullen vanuit het databasesynchronisatieproces.</span><span class="sxs-lookup"><span data-stu-id="46be2-110">Add it to the **LogisticsLocationRoleType** enum extension, and let it populate through the database sync process.</span></span>

    1.  <span data-ttu-id="46be2-111">Maak een extensie van de opsomming **LogisticsLocationRoleType** en voeg de nieuwe rol in de extensie toe.</span><span class="sxs-lookup"><span data-stu-id="46be2-111">Create an extension to the **LogisticsLocationRoleType** enum and add the new role in the extension.</span></span> 
  
        ![Extensie voor opsomming LogisticsLocationRoleType](media/Logistics.PNG)

    2. <span data-ttu-id="46be2-113">Maak een nieuw resourcebestand voor de nieuwe rol en wijs een waarde toe voor de eigenschappen ervan.</span><span class="sxs-lookup"><span data-stu-id="46be2-113">Create a new resource file for the new role, and then assign a value for its properties.</span></span>
     
     ![Nieuw resourcebestand](media/Resource.PNG)
        
    3.  <span data-ttu-id="46be2-115">Maak een klasse van populatiegegevens en bied een handlermethode voor het vullen van de nieuwe rol.</span><span class="sxs-lookup"><span data-stu-id="46be2-115">Create a data population class and provide a handler method to populate the new role.</span></span> 

        ![Invullen van gegevens](media/Dirdata.PNG)

    4.  <span data-ttu-id="46be2-117">Als u het vullen van de nieuwe locatierol wilt testen, kunt u een uitvoerbare klasse maken en DirDataPopulation::insertLogisticsLocationRoles() in Main() aanroepen.</span><span class="sxs-lookup"><span data-stu-id="46be2-117">To test populating the new location role, you can create a runnable class, and call DirDataPopulation::insertLogisticsLocationRoles() in Main().</span></span> <span data-ttu-id="46be2-118">Nadat dit proces voltooid is, ziet u de nieuwe rol ingevuld in de tabel **LogisticsLocationRole** met type \> 0.</span><span class="sxs-lookup"><span data-stu-id="46be2-118">After this process is complete, you should see the new role populated in the **LogisticsLocationRole** table with type \> 0.</span></span> <span data-ttu-id="46be2-119">De nieuwe rol wordt weergegeven op de pagina **Doel van adres- en contactgegevens**.</span><span class="sxs-lookup"><span data-stu-id="46be2-119">The new role will display on the **Address and contact information purpose** page.</span></span>

        ![Nieuwe locatie invoegen](media/InsertNewLocation.PNG)

## <a name="add-party-relationship-types"></a><span data-ttu-id="46be2-121">Partijrelatietypen toevoegen</span><span class="sxs-lookup"><span data-stu-id="46be2-121">Add party relationship types</span></span> 

<span data-ttu-id="46be2-122">Er zijn twee manieren om een nieuw relatietype toe te voegen:</span><span class="sxs-lookup"><span data-stu-id="46be2-122">There are two ways to add a new relationship type:</span></span>

-   <span data-ttu-id="46be2-123">Voeg het toe met de pagina **Relatietypen**.</span><span class="sxs-lookup"><span data-stu-id="46be2-123">Add it through the **Relationship types** page.</span></span> <span data-ttu-id="46be2-124">De nieuwe relatie wordt opgeslagen in **DirRelationshipTypeTable** met systemtype = 0.</span><span class="sxs-lookup"><span data-stu-id="46be2-124">The new relationship will be saved to **DirRelationshipTypeTable** with systemtype = 0.</span></span>

    ![Relatietypen](media/Relationship.PNG)

-  <span data-ttu-id="46be2-126">Voeg het toe aan de extensie van de opsomming **DirSystemRelationshipType** en laat het vullen vanuit het databasesynchronisatieproces.</span><span class="sxs-lookup"><span data-stu-id="46be2-126">Add it to the extension of the **DirSystemRelationshipType** enum, and let it populate through database sync process.</span></span>

    1.  <span data-ttu-id="46be2-127">Maak een extensie van de opsomming **DirSystemRelationshipType** en voeg het nieuwe relatietype toe.</span><span class="sxs-lookup"><span data-stu-id="46be2-127">Create an extension to the **DirSystemRelationshipType** enum and add the new relationship type.</span></span>

    2. <span data-ttu-id="46be2-128">Maak een initialisatiefunctie voor dit nieuwe type.</span><span class="sxs-lookup"><span data-stu-id="46be2-128">Create an initializer for this new type.</span></span> <span data-ttu-id="46be2-129">U vindt enkele voorbeelden in de kerncode. Een ervan is **DirRelationshipTypeChildInitialize**.</span><span class="sxs-lookup"><span data-stu-id="46be2-129">You can find several examples in the core code, one of them is  **DirRelationshipTypeChildInitialize**.</span></span> <span data-ttu-id="46be2-130">Dit is een initialisatieklasse voor partijrelatietype 'Onderliggend'.</span><span class="sxs-lookup"><span data-stu-id="46be2-130">This is an initializer class for party relationship type “Child”.</span></span> <span data-ttu-id="46be2-131">U kunt beginnen met uw initialisatiefunctie door deze code te kopiëren en te plakken en vervolgens de gemarkeerde gebieden bij te werken.</span><span class="sxs-lookup"><span data-stu-id="46be2-131">You can start with your initializer by copying and pasting this code and then update the highlighted areas.</span></span>
    
    ![Initialisatiefunctie DirRelationshipChild](media/DirRelationship.PNG)

    3.  <span data-ttu-id="46be2-133">Als u het vullen van het nieuwe relatietype wilt testen, kunt u een uitvoerbare klasse maken en DirDataPopulation::insertDirRelationshipTypes() in Main() aanroepen.</span><span class="sxs-lookup"><span data-stu-id="46be2-133">To test populating the new relationship type, you can create a runnable class, and call DirDataPopulation::insertDirRelationshipTypes() in Main().</span></span> <span data-ttu-id="46be2-134">U ziet nu het nieuwe relatietype in de **DirRelationshipTypeTable** en het nieuwe relatietype zal beschikbaar zijn op de pagina **Relatietypen**.</span><span class="sxs-lookup"><span data-stu-id="46be2-134">You should see the new relationship type in the **DirRelationshipTypeTable**, and the new relationship type will be available on the **Relationship types** page.</span></span>

        ![Uitvoerbare klasse](media/Runnable.PNG)
