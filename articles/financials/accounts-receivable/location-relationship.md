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
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 13991
ms.assetid: 2a0a4789-8619-4974-bef9-0923cc848420
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2018-05-02
ms.dyn365.ops.version: AX 8.0.0
ms.translationtype: HT
ms.sourcegitcommit: e0ab9c9894fdd5fba224c166941abbf52172ae46
ms.openlocfilehash: 27819c922832a30eb0b20db6bffdbd4504e6d5e6
ms.contentlocale: nl-nl
ms.lasthandoff: 06/12/2018

---

# <a name="add-location-roles-and-party-relationship-types"></a>Locatierollen en partijrelatietypen toevoegen 

## <a name="add-location-roles"></a>Locatierollen toevoegen

Er zijn twee manieren voor het toevoegen van nieuwe locatierollen voor adres- en contactgegevens:

-  Voeg het toe met de pagina **Doel van adres- en contactgegevens**. De nieuwe rol wordt opgeslagen in de tabel **LogisticsLocationRole** met type = 0, waarmee wordt aangegeven dat de rol geen systeemrol is die is gedefinieerd in de opsomming **LogisticsLocationRoleType** en de extensies ervan. Een gebruiker kan deze rol gebruiken bij het maken van adres- of contactpersoongegevens.

    ![Doel van adres- en inhoudsgegevens](media/Address-Contact.PNG)

-  Voeg het toe aan de opsommingsextensie **LogisticsLocationRoleType** en laat het vullen vanuit het databasesynchronisatieproces.

    1.  Maak een extensie van de opsomming **LogisticsLocationRoleType** en voeg de nieuwe rol in de extensie toe. 
  
        ![LogisticsLocationRoleType](media/Logistics.PNG)

    2. Maak een nieuw resourcebestand voor de nieuwe rol en wijs een waarde toe voor de eigenschappen ervan.
     
     ![Nieuw resourcebestand](media/Resource.PNG)
        
    3.  Maak een klasse van populatiegegevens en bied een handlermethode voor het vullen van de nieuwe rol. 

        ![Invullen van gegevens](media/Dirdata.PNG)

    4.  Als u het vullen van de nieuwe locatierol wilt testen, kunt u een uitvoerbare klasse maken en DirDataPopulation::insertLogisticsLocationRoles() in Main() aanroepen. Nadat dit proces voltooid is, ziet u de nieuwe rol ingevuld in de tabel **LogisticsLocationRole** met type \> 0. De nieuwe rol wordt weergegeven op de pagina **Doel van adres- en contactgegevens**.

        ![Nieuwe locatie invoegen](media/InsertNewLocation.PNG)

## <a name="add-party-relationship-types"></a>Partijrelatietypen toevoegen 

Er zijn twee manieren om een nieuw relatietype toe te voegen:

-   Voeg het toe met de pagina **Relatietypen**. De nieuwe relatie wordt opgeslagen in **DirRelationshipTypeTable** met systemtype = 0.

    ![Relatietypen](media/Relationship.PNG)

-  Voeg het toe aan de extensie van de opsomming **DirSystemRelationshipType** en laat het vullen vanuit het databasesynchronisatieproces.

    1.  Maak een extensie van de opsomming **DirSystemRelationshipType** en voeg het nieuwe relatietype toe.

    2. Maak een initialisatiefunctie voor dit nieuwe type. U vindt enkele voorbeelden in de kerncode. Een ervan is **DirRelationshipTypeChildInitialize**. Dit is een initialisatieklasse voor partijrelatietype 'Onderliggend'. U kunt beginnen met uw initialisatiefunctie door deze code te kopiëren en te plakken en vervolgens de gemarkeerde gebieden bij te werken.
    
    ![DirRelationshipChild](media/DirRelationship.PNG)

    3.  Als u het vullen van het nieuwe relatietype wilt testen, kunt u een uitvoerbare klasse maken en DirDataPopulation::insertDirRelationshipTypes() in Main() aanroepen. U ziet nu het nieuwe relatietype in de **DirRelationshipTypeTable** en het nieuwe relatietype zal beschikbaar zijn op de pagina **Relatietypen**.

        ![Uitvoerbare klasse](media/Runnable.PNG)

