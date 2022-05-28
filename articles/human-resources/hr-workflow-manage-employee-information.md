---
title: Workflows gebruiken om werknemersgegevens te beheren
description: In dit onderwerp wordt uitgelegd hoe u werkstromen kunt gebruiken om medewerkersgegevens te beheren.
author: twheeloc
ms.date: 11/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: 269074
ms.assetid: 426c6127-42ee-4163-8dd0-b2867f95581d
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 7c416a82976bc39464006325f02f1af4d2f32ea4
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/04/2022
ms.locfileid: "8691521"
---
# <a name="use-workflows-to-manage-employee-information"></a>Workflows gebruiken om werknemersgegevens te beheren


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

In dit onderwerp wordt uitgelegd hoe u de workflowmogelijkheid voor Human resources kunt gebruiken om werknemersgegevens te beheren. U kunt bijvoorbeeld een workflow aan een positie koppelen en een goedkeuringsworkflow configureren die wordt gestart wanneer werknemers hun record wijzigen.

De workflowmogelijkheid voor Human resources biedt een groot aantal workflows voor het beheren van human resources-activiteiten. Bovendien zijn er vele opties beschikbaar zodat u specifieke workflows kunt wijzigen en deze aan een rapportagehiërarchie kunt koppelen. Werkstromen zijn beschikbaar om wijzigingen in verschillende typen medewerkersgegevens gemakkelijker te beheren. U kunt een workflow koppelen aan een positie. Vervolgens wordt er, als werknemers hun werknemersrecord wijzigen, een workflow gestart die moet worden goedgekeurd voordat de nieuwe informatie wordt opgeslagen. Werkstromen worden vooraf gedefinieerd voor de volgende typen informatie om wijzigingen efficiënt te beheren en uw medewerkersgegevens nauwkeurig te houden:

-   Identificatienummers
-   Cursussen
-   Onderwijs
-   Afbeelding
-   Geleende artikelen
-   Beroepservaring
-   Projectervaring
-   Vaardigheden
-   Vertrouwensposities
-   Acties van Human Resources
-   Cursusregistratie

Wanneer werknemers worden aangesteld of overgeplaatst of wanneer hun dienstverband wordt beëindigd, kan de workflow een controleproces bevatten. Op deze manier kan een document worden herzien of kunnen de voorwaarden van een actie als onderdeel van de werkstroom worden gedefinieerd. Wanneer het controleproces is voltooid, wordt het document of de actie voltooid en wordt de workflow verplaatst naar een laatste goedkeuringsstap.

## <a name="associate-a-workflow-with-a-position-hierarchy"></a>Een workflow koppelen aan een positiehiërarchie
U kunt een workflow koppelen aan elke hiërarchie die u configureert. Als bijvoorbeeld een positie is gekoppeld aan een matrixrapportagehiërarchie, kunt u een workflow configureren waarmee onkosten voor een bepaald project worden doorgestuurd naar de projectleider in plaats van de manager van de werknemer die is gekoppeld aan die positie. Als u een nieuwe werkstroom wilt maken of een bestaande werkstroom wilt wijzigen op de pagina **Workflow voor Human resources**, selecteert u **Nieuw**. Selecteer een werkstroom in de lijst om de werkstroomontwerper te openen. U kunt de ontwerper gebruiken om een nieuwe workflow te maken of om de stappen in een bestaande workflow te wijzigen. Wanneer u een bestaande workflow wijzigt, worden uw wijzigingen opgeslagen als een nieuwe versie. U kunt dus altijd teruggaan naar een vorige versie als dat nodig is.

## <a name="configure-a-human-resources-workflow"></a>Een workflow voor Human resources configureren
Voer de volgende stappen uit om een eenvoudige workflow te configureren die wordt gestart wanneer werknemers een wijziging van hun persoonlijke identificatienummer aanvragen.

1.  Op de pagina **Human resources-werkstromen** selecteert u **Nieuw**.
2.  Selecteer in de lijst met beschikbare workflows **Identificatienummers**.
3.  Selecteer **Uitvoeren** om de werkstroomontwerper te openen en voer vervolgens uw gebruikersnaam en wachtwoord in wanneer u dat wordt gevraagd.
4.  Sleep het element **Identificatienummer goedkeuren** vanuit de lijst met workflowelementen naar het ontwerperscanvas.
5.  Verbind het goedkeuringselement met **Starten** en **Voltooien**.
6.  Dubbeltik op (of dubbelklik) op **Element goedkeuren**, selecteer en houd dit vast (of klik met de rechtermuisknop) en selecteer **Eigenschappen**.
7.  Voer de volgende stappen uit om werkiteminstructies toe te voegen:

    1.  Selecteer **Toewijzing** en selecteer vervolgens **Hiërarchie** onder het toewijzingstype.
    2.  Selecteer onder de sectie **Hiërarchie** **Configureerbare hiërarchie**.
    3.  Voeg een stopvoorwaarde toe en sluit de pagina.

8.  Voer eventuele extra instructies uit (er mogen geen extra waarschuwingen aanwezig zijn).
9.  Selecteer **Opslaan en sluiten**. Activeer de nieuwe workflow wanneer het dialoogvenster wordt geopend en selecteer **Actief maken**.
10. Ga naar **Human Resources** &gt; **Posities** &gt; **Positiehiërarchietypen**.
11. Selecteer **Matrix**.
12. Voeg de workflow **Identificatienummer van werknemer** aan de lijst toe.

## <a name="additional-resources"></a>Aanvullende bronnen

[Adreswijzigingen weergeven en beheren](hr-personnel-view-address-changes.md) 





[!INCLUDE[footer-include](../includes/footer-banner.md)]
