---
title: Locatie en partijrelatietypen toevoegen
description: In dit onderwerp wordt uitgelegd hoe u een nieuwe locatie en partijrelatietype toevoegt.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 13991
ms.assetid: 2a0a4789-8619-4974-bef9-0923cc848420
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2018-05-02
ms.dyn365.ops.version: AX 8.0.0
ms.translationtype: HT
ms.sourcegitcommit: bf971bc6cf4b11de6381e369235d582678d074fc
ms.openlocfilehash: 8de914e0fb853cdc9aa36e55a02156757793abc3
ms.contentlocale: nl-nl
ms.lasthandoff: 06/12/2018

---

# <a name="add-new-location-roles-and-party-relationship-types"></a><span data-ttu-id="29751-103">Nieuwe locatierollen en partijrelatietypen toevoegen</span><span class="sxs-lookup"><span data-stu-id="29751-103">Add new location roles and party relationship types</span></span> 

## <a name="add-new-location-roles"></a><span data-ttu-id="29751-104">Nieuwe locatierollen toevoegen</span><span class="sxs-lookup"><span data-stu-id="29751-104">Add new location roles</span></span>

<span data-ttu-id="29751-105">Er zijn twee manieren voor het toevoegen van nieuwe locatierollen voor adres- en contactgegevens:</span><span class="sxs-lookup"><span data-stu-id="29751-105">There are two ways to add a new location roles for address and contact information:</span></span>

-  <span data-ttu-id="29751-106">Voeg het toe met de pagina **Doel van adres- en contactgegevens**.</span><span class="sxs-lookup"><span data-stu-id="29751-106">Add it through the **Address and contact information purpose** page.</span></span> <span data-ttu-id="29751-107">De nieuwe rol wordt opgeslagen in de tabel **LogisticsLocationRole** met type = 0, waarmee wordt aangegeven dat de rol geen systeemrol is die is gedefinieerd in de opsomming **LogisticsLocationRoleType** en de extensies ervan.</span><span class="sxs-lookup"><span data-stu-id="29751-107">The new role will be saved to the **LogisticsLocationRole** table with type = 0, which indicates that the role is not a system role defined in the **LogisticsLocationRoleType** enum and its extensions.</span></span> <span data-ttu-id="29751-108">Een gebruiker kan deze rol gebruiken bij het maken van adres- of contactpersoongegevens.</span><span class="sxs-lookup"><span data-stu-id="29751-108">A user will be able to use this role when creating address or contact information.</span></span>

    ![Doel van adres- en inhoudsgegevens](media/Address-Contact.PNG)

-  <span data-ttu-id="29751-110">Voeg het toe aan de opsommingsextensie **LogisticsLocationRoleType** en laat het vullen vanuit het databasesynchronisatieproces.</span><span class="sxs-lookup"><span data-stu-id="29751-110">Add it to the **LogisticsLocationRoleType** enum extension, and let it populate through the database sync process.</span></span>

    1.  <span data-ttu-id="29751-111">Maak een extensie van de opsomming **LogisticsLocationRoleType** en voeg de nieuwe rol in de extensie toe.</span><span class="sxs-lookup"><span data-stu-id="29751-111">Create an extension to the **LogisticsLocationRoleType** enum and add the new role in the extension.</span></span> 
  
        ![LogisticsLocationRoleType](media/Logistics.PNG)

    2. <span data-ttu-id="29751-113">Maak een nieuw resourcebestand voor de nieuwe rol en wijs een waarde toe voor de eigenschappen ervan.</span><span class="sxs-lookup"><span data-stu-id="29751-113">Create a new resource file for the new role, and then assign a value for its properties.</span></span>
     
     ![Nieuw resourcebestand](media/Resource.PNG)
        
    3.  <span data-ttu-id="29751-115">Maak een klasse van populatiegegevens en bied een handlermethode voor het vullen van de nieuwe rol.</span><span class="sxs-lookup"><span data-stu-id="29751-115">Create a data population class and provide a handler method to populate the new role.</span></span> 

        ![Invullen van gegevens](media/Dirdata.PNG)

    4.  <span data-ttu-id="29751-117">Als u het vullen van de nieuwe locatierol wilt testen, kunt u een uitvoerbare klasse maken en DirDataPopulation::insertLogisticsLocationRoles() in Main() aanroepen.</span><span class="sxs-lookup"><span data-stu-id="29751-117">To test populating the new location role, you can create a runnable class, and call DirDataPopulation::insertLogisticsLocationRoles() in Main().</span></span> <span data-ttu-id="29751-118">Nadat dit proces voltooid is, ziet u de nieuwe rol ingevuld in de tabel **LogisticsLocationRole** met type \> 0.</span><span class="sxs-lookup"><span data-stu-id="29751-118">After this process is complete, you should see the new role populated in the **LogisticsLocationRole** table with type \> 0.</span></span> <span data-ttu-id="29751-119">De nieuwe rol wordt weergegeven op de pagina **Doel van adres- en contactgegevens**.</span><span class="sxs-lookup"><span data-stu-id="29751-119">The new role will display on the **Address and contact information purpose** page.</span></span>

        ![Nieuwe locatie invoegen](media/InsertNewLocation.PNG)

## <a name="add-new-party-relationship-types"></a><span data-ttu-id="29751-121">Nieuwe partijrelatietypen toevoegen</span><span class="sxs-lookup"><span data-stu-id="29751-121">Add new party relationship types</span></span> 

<span data-ttu-id="29751-122">Er zijn twee manieren om een nieuw relatietype toe te voegen:</span><span class="sxs-lookup"><span data-stu-id="29751-122">There are two ways to add a new relationship type:</span></span>

-   <span data-ttu-id="29751-123">Voeg het toe met de pagina **Relatietypen**.</span><span class="sxs-lookup"><span data-stu-id="29751-123">Add it through the **Relationship types** page.</span></span> <span data-ttu-id="29751-124">De nieuwe relatie wordt opgeslagen in **DirRelationshipTypeTable** met systemtype = 0.</span><span class="sxs-lookup"><span data-stu-id="29751-124">The new relationship will be saved to **DirRelationshipTypeTable** with systemtype = 0.</span></span>

    ![Relatietypen](media/Relationship.PNG)

-  <span data-ttu-id="29751-126">Voeg het toe aan de extensie van de opsomming **DirSystemRelationshipType** en laat het vullen vanuit het databasesynchronisatieproces.</span><span class="sxs-lookup"><span data-stu-id="29751-126">Add it to the extension of the **DirSystemRelationshipType** enum, and let it populate through database sync process.</span></span>

    1.  <span data-ttu-id="29751-127">Maak een extensie van de opsomming **DirSystemRelationshipType** en voeg het nieuwe relatietype toe.</span><span class="sxs-lookup"><span data-stu-id="29751-127">Create an extension to the **DirSystemRelationshipType** enum and add the new relationship type.</span></span>

    2. <span data-ttu-id="29751-128">Maak een initialisatiefunctie voor dit nieuwe type.</span><span class="sxs-lookup"><span data-stu-id="29751-128">Create an initializer for this new type.</span></span> <span data-ttu-id="29751-129">U vindt enkele voorbeelden in de kerncode. Een ervan is **DirRelationshipTypeChildInitialize**.</span><span class="sxs-lookup"><span data-stu-id="29751-129">You can find several examples in the core code, one of them is  **DirRelationshipTypeChildInitialize**.</span></span> <span data-ttu-id="29751-130">Dit is een initialisatieklasse voor partijrelatietype 'Onderliggend'.</span><span class="sxs-lookup"><span data-stu-id="29751-130">This is an initializer class for party relationship type “Child”.</span></span> <span data-ttu-id="29751-131">U kunt beginnen met uw initialisatiefunctie door deze code te kopiëren en te plakken en vervolgens de gemarkeerde gebieden bij te werken.</span><span class="sxs-lookup"><span data-stu-id="29751-131">You can start with your initializer by copying and pasting this code and then update the highlighted areas.</span></span>
    
    ![DirRelationshipChild](media/DirRelationship.PNG)

    3.  <span data-ttu-id="29751-133">Als u het vullen van het nieuwe relatietype wilt testen, kunt u een uitvoerbare klasse maken en DirDataPopulation::insertDirRelationshipTypes() in Main() aanroepen.</span><span class="sxs-lookup"><span data-stu-id="29751-133">To test populating the new relationship type, you can create a runnable class, and call DirDataPopulation::insertDirRelationshipTypes() in Main().</span></span> <span data-ttu-id="29751-134">U ziet nu het nieuwe relatietype in de **DirRelationshipTypeTable** en het nieuwe relatietype zal beschikbaar zijn op de pagina **Relatietypen**.</span><span class="sxs-lookup"><span data-stu-id="29751-134">You should see the new relationship type in the **DirRelationshipTypeTable**, and the new relationship type will be available on the **Relationship types** page.</span></span>

        ![Uitvoerbare klasse](media/Runnable.PNG)

