---
title: Informatie over medewerkers met behulp van werkstromen
description: Dit onderwerp wordt uitgelegd hoe u de mogelijkheid van de workflow voor Human resources kunt gebruiken om werknemersgegevens te beheren. U kunt bijvoorbeeld een workflow aan een positie koppelen en configureren van een goedkeuringsworkflow die wordt gestart wanneer werknemers hun record wijzigt.
author: rschloma
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 269074
ms.assetid: 426c6127-42ee-4163-8dd0-b2867f95581d
ms.search.region: Global
ms.author: shielas
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: a76ec0cd86bcc810b42ae3cd8efd8a584e6c4da3
ms.openlocfilehash: f286436aa4833babaeb3de875ee393d18e5f8eea
ms.lasthandoff: 03/31/2017


---

# <a name="use-workflows-to-manage-employee-information"></a>Informatie over medewerkers met behulp van werkstromen

Dit onderwerp wordt uitgelegd hoe u de mogelijkheid van de workflow voor Human resources kunt gebruiken om werknemersgegevens te beheren. U kunt bijvoorbeeld een workflow aan een positie koppelen en configureren van een goedkeuringsworkflow die wordt gestart wanneer werknemers hun record wijzigt.

De mogelijkheid van de workflow voor Human resources biedt een groot aantal werkstromen voor het beheren van human resources-activiteiten. Bovendien zijn vele opties beschikbaar zodat u kunt specifieke workflows wijzigen en deze aan een hiërarchie koppelen. Er zijn workflows beschikbaar waarmee wijzigingen in standaardkosten soorten werknemersinformatie beheren. U kunt een werkstroom koppelen aan een positie. Vervolgens, als werknemers hun werknemerrecord wijzigt, wordt een workflow die moet worden goedgekeurd gestart voordat de nieuwe informatie wordt opgeslagen. Workflows voor de volgende soorten informatie om te voorkomen dat uw werknemers gegevens nauwkeurig en efficiënt beheren wijzigingen vooraf zijn gedefinieerd:

-   Identificatienummers
-   Cursussen
-   Opleiding
-   Afbeelding
-   Geleende artikelen
-   Beroepservaring
-   Projectervaring
-   Vaardigheden
-   Vertrouwensposities
-   Human resources-acties
-   Cursusregistratie

Wanneer werknemers worden aangesteld, overgedragen of beëindigd, kan de werkstroom een controleproces opnemen. Op deze manier een document kan worden herzien of de voorwaarden van een actie kunnen worden gedefinieerd als onderdeel van de workflow. Wanneer het controleproces is voltooid, wordt het document of de actie is voltooid en de workflow wordt verplaatst naar een laatste goedkeuringsstap.

## <a name="associate-a-workflow-with-a-position-hierarchy"></a>Een werkstroom koppelen aan een positiehiërarchie
U kunt een werkstroom koppelen aan elke hiërarchie die u configureert. Als een positie gekoppeld aan een matrixhiërarchie is, kunt u bijvoorbeeld een workflow waarmee onkosten voor een bepaald project naar de projectleider in plaats van de manager van de werknemer die gekoppeld aan die positie is doorgestuurd configureren. Een nieuwe workflow maken of een bestaande workflow wijzigen op de **Human resources-workflow** pagina, klikt u op **New**. Selecteer een werkstroom in de lijst om de workflow designer te starten. De ontwerper kunt u een nieuwe workflow maken of wijzigen van de stappen in een bestaande workflow. Wanneer u een bestaande workflow wijzigt, worden uw wijzigingen worden opgeslagen als een nieuwe versie. Dus kunt u altijd teruggaan naar een vorige versie als u wilt.

## <a name="configure-a-human-resources-workflow"></a>Een Human resources-workflow configureren
Volg deze stappen voor het configureren van een eenvoudige werkstroom die wordt gestart wanneer werknemers hun persoonlijke identificatienummer wijzigingen aanvragen.

1.  Op de **workflows voor HRM** pagina, klikt u op **New**.
2.  Selecteer in de lijst met beschikbare werkstromen, **-id's**.
3.  Klik op **uitgevoerd** om de workflow designer te starten en voer vervolgens uw gebruikersnaam en wachtwoord wanneer u wordt gevraagd.
4.  Sleep de **goedkeuren identificatienummer** element in de lijst met workflowelementen op het tekenpapier ontwerper.
5.  Verbinding maken met het goedkeuringselement naar **starten** en **voltooien**.
6.  Dubbelklik op **goedkeuren element**, en klik vervolgens met de rechtermuisknop en selecteer **eigenschappen**.
7.  Ga als volgt te werk als u wilt werkinstructies artikel toevoegen:
    1.  Selecteer **toewijzing**, en selecteer vervolgens **hiërarchie** onder het toewijzingstype.
    2.  Onder de **hiërarchie** selectie, selecteert **configureerbaar hiërarchie**.
    3.  Een stop-voorwaarde toevoegen en de pagina te sluiten.

8.  Voer eventuele extra aanwijzingen (er worden geen extra waarschuwingen moeten worden gedefinieerd).
9.  Klik op **Opslaan en afsluiten**. De nieuwe workflow activeren wanneer het dialoogvenster wordt geopend in en selecteer **activeren**.
10. Ga naar **Human Resources**&gt;**posities**&gt;**plaats typen categoriehiërarchieën**.
11. Selecteer **Matrix**.
12. Toevoegen de **werknemer-id-nummer** werkstroom aan de lijst.



