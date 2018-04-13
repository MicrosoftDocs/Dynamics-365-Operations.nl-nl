---
title: Informatie over werknemers beheren met behulp van workflows
description: In dit onderwerp wordt uitgelegd hoe u de workflowmogelijkheid voor Human resources kunt gebruiken om werknemersgegevens te beheren. U kunt bijvoorbeeld een workflow aan een positie koppelen en een goedkeuringsworkflow configureren die wordt gestart wanneer werknemers hun record wijzigen.
author: rschloma
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, Operations, Talent
ms.custom: 269074
ms.assetid: 426c6127-42ee-4163-8dd0-b2867f95581d
ms.search.region: Global
ms.author: shielas
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: abc52192848649672cbcb8c770d74ba2aef139be
ms.openlocfilehash: cf2200057053f5a6d4754d37111ebe34849bb99d
ms.contentlocale: nl-nl
ms.lasthandoff: 02/14/2018

---

# <a name="use-workflows-to-manage-employee-information"></a>Informatie over werknemers beheren met behulp van workflows

[!INCLUDE [banner](includes/banner.md)]

In dit onderwerp wordt uitgelegd hoe u de workflowmogelijkheid voor Human resources kunt gebruiken om werknemersgegevens te beheren. U kunt bijvoorbeeld een workflow aan een positie koppelen en een goedkeuringsworkflow configureren die wordt gestart wanneer werknemers hun record wijzigen.

De workflowmogelijkheid voor Human resources biedt een groot aantal workflows voor het beheren van human resources-activiteiten. Bovendien zijn er vele opties beschikbaar zodat u specifieke workflows kunt wijzigen en deze aan een rapportagehiërarchie kunt koppelen. Workflows zijn beschikbaar om wijzigingen in verschillende typen werknemersinformatie gemakkelijker te beheren. U kunt een workflow koppelen aan een positie. Vervolgens wordt er, als werknemers hun werknemersrecord wijzigen, een workflow gestart die moet worden goedgekeurd voordat de nieuwe informatie wordt opgeslagen. Workflows worden vooraf gedefinieerd voor de volgende typen informatie om wijzigingen efficiënt te beheren en uw werknemersgegevens nauwkeurig te houden:

-   Identificatienummers
-   Cursussen
-   Opleiding
-   Afbeelding
-   Geleende artikelen
-   Beroepservaring
-   Projectervaring
-   Vaardigheden
-   Vertrouwensposities
-   Acties van Human Resources
-   Cursusregistratie

Wanneer werknemers worden aangesteld of overgeplaatst of wanneer hun dienstverband wordt beëindigd, kan de workflow een controleproces bevatten. Op deze manier kan een document worden herzien of kunnen de voorwaarden van een actie als onderdeel van de workflow worden gedefinieerd. Wanneer het controleproces is voltooid, wordt het document of de actie voltooid en wordt de workflow verplaatst naar een laatste goedkeuringsstap.

## <a name="associate-a-workflow-with-a-position-hierarchy"></a>Een workflow koppelen aan een positiehiërarchie
U kunt een workflow koppelen aan elke hiërarchie die u configureert. Als bijvoorbeeld een positie is gekoppeld aan een matrixrapportagehiërarchie, kunt u een workflow configureren waarmee onkosten voor een bepaald project worden doorgestuurd naar de projectleider in plaats van de manager van de werknemer die is gekoppeld aan die positie. Als u een nieuwe workflow wilt maken of een bestaande workflow wilt wijzigen op de pagina **Workflow voor Human resources**, klikt u op **Nieuw**. Selecteer een workflow in de lijst om de workflowontwerper te starten. U kunt de ontwerper gebruiken om een nieuwe workflow te maken of om de stappen in een bestaande workflow te wijzigen. Wanneer u een bestaande workflow wijzigt, worden uw wijzigingen opgeslagen als een nieuwe versie. U kunt dus altijd teruggaan naar een vorige versie als dat nodig is.

## <a name="configure-a-human-resources-workflow"></a>Een workflow voor Human resources configureren
Voer de volgende stappen uit om een eenvoudige workflow te configureren die wordt gestart wanneer werknemers een wijziging van hun persoonlijke identificatienummer aanvragen.

1.  Klik op de pagina **Human resources-workflows** op **Nieuw**.
2.  Selecteer in de lijst met beschikbare workflows **Identificatienummers**.
3.  Klik op **Uitvoeren** om de workflowontwerper te starten en voer vervolgens uw gebruikersnaam en wachtwoord in wanneer u dat wordt gevraagd.
4.  Sleep het element **Identificatienummer goedkeuren** vanuit de lijst met workflowelementen naar het ontwerperscanvas.
5.  Verbind het goedkeuringselement met **Starten** en **Voltooien**.
6.  Dubbelklik op **Element goedkeuren** en klik vervolgens met de rechtermuisknop en selecteer **Eigenschappen**.
7.  Voer de volgende stappen uit om werkiteminstructies toe te voegen:
    1.  Selecteer **Toewijzing** en selecteer vervolgens **Hiërarchie** onder het toewijzingstype.
    2.  Selecteer onder de sectie **Hiërarchie** **Configureerbare hiërarchie**.
    3.  Voeg een stopvoorwaarde toe en sluit de pagina.

8.  Voer eventuele extra instructies uit (er mogen geen extra waarschuwingen aanwezig zijn).
9.  Klik op **Opslaan en afsluiten**. Activeer de nieuwe workflow wanneer het dialoogvenster wordt geopend en selecteer **Actief maken**.
10. Ga naar **Human Resources** &gt; **Posities** &gt; **Positiehiërarchietypen**.
11. Selecteer **Matrix**.
12. Voeg de workflow **Identificatienummer van werknemer** aan de lijst toe.





